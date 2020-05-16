---
title: Unterstützung für Offline-und Netzwerkkonnektivität in progressiven Web-Apps
description: Erfahren Sie, wie Sie mithilfe von unterstützenden Technologien elastische Erfahrungen erstellen, um unterschiedliche Netzwerkbedingungen zu erfüllen.
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/15/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: pwa
keywords: Progressive Web-Apps, PWA, Edge, JavaScript, Windows, UWP, Microsoft Store
ms.openlocfilehash: 58ffb8e9ae596dec4b99143a3061995a6598ce44
ms.sourcegitcommit: d9cc829deb709b0866f6b43a5f4733682ddae5ca
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/16/2020
ms.locfileid: "10659307"
---
# Unterstützung für Offline-und Netzwerkkonnektivität in progressiven Web-Apps

Viele Jahre lang zögerten Organisationen nicht, stark in webbasierte Software über native Software zu investieren, da Webanwendungen von stabilen Netzwerkverbindungen abhingen. Heute bietet die Webplattform nun robuste Optionen, mit denen Benutzer weiterhin arbeiten können, auch wenn die Netzwerkverbindung instabil wird oder vollständig offline geht.

## Verwenden der Zwischenspeicherung zum Verbessern der Leistung von PWAs

Mit der Einführung von [Service Mitarbeitern][MDNServiceWorker]hat die Webplattform die API hinzugefügt, `Cache` um den Zugriff auf verwaltete zwischengespeicherte Ressourcen zu ermöglichen. Mit dieser Promise-basierten API können Entwickler viele Webressourcen speichern und Abrufen – HTML, CSS, JavaScript, Bilder, JSON usw. In der Regel wird die Cache-API innerhalb des Kontexts eines Dienstmitarbeiter verwendet, ist aber auch im Hauptthread des Objekts verfügbar `window` .

Eine häufige Verwendung für die `Cache` API besteht darin, wichtige Ressourcen vor dem Cache zu speichern, wenn ein Dienstmitarbeiter installiert wird, wie im folgenden Codeausschnitt dargestellt.  

```javascript
self.addEventListener( "install", function( event ){
    event.waitUntil(
        caches.open( "static-cache" )
              .then(function( cache ){
            return cache.addAll([
                "/css/main.css",
                "/js/main.js",
                "/img/favicon.png",
                "/offline/"
            ]);
        })
    );
});
```  

Dieser Code, der während des Lebenszyklus des Service Worker `install` -Ereignisses ausgeführt wird, öffnet einen Cache mit dem Namen `static-cache` und fügt ihm dann mit der Methode vier Ressourcen hinzu, wenn er über einen Zeiger auf den Cache verfügt `addAll()` .  Häufig ist der Ansatz mit dem Abrufen des Caches während eines Ereignisses gekoppelt. `fetch`   

```javascript
self.addEventListener( "fetch", event => {
    const request = event.request,
                    url = request.url;
    
    // If we are requesting an HTML page.
    if ( request.headers.get("Accept").includes("text/html") ) {
        event.respondWith(
            // Check the cache first to see if the asset exists, and if it does, return the cached asset.
            caches.match( request )
                  .then( cached_result => {
                if ( cached_result ) {
                    return cached_result;
                }
                // If the asset is not in the cache, fallback to a network request for the asset, and proceed to cache the result.
                return fetch( request )
                       .then( response => {
                    const copy = response.clone();
                    // Wait until the response we received is added to the cache.
                    event.waitUntil(
                        caches.open( "pages" )
                              .then( cache => {
                            return cache.put( request, response );
                        });
                    );
                    return response;
                })
                // If the network is unavailable to make a request, pull the offline page out of the cache.
                .catch(() => caches.match( "/offline/" ));
            })
        ); // end respondWith
    } // end if HTML
});
```  

Der Codeausschnitt wird innerhalb des Dienst Arbeitsthreads ausgeführt, wenn der Browser eine `fetch` Anforderung für diese Website vornimmt. Innerhalb dieses Ereignisses gibt es eine bedingte Anweisung, die ausgeführt wird, wenn die Anforderung eine HTML-Datei ist. Der Dienstmitarbeiter überprüft, ob die Datei bereits in einem beliebigen Cache vorhanden ist \ (mit der `match()` Methode \). Wenn die Anforderung im Cache vorhanden ist, wird das zwischengespeicherte Ergebnis zurückgegeben. Wenn dies nicht der Fall ist, wird eine neue `fetch` für diese Ressource ausgeführt, eine Kopie der Antwort wird für später zwischengespeichert, und die Antwort wird zurückgegeben. Wenn das `fetch` fehlschlägt, weil das Netzwerk nicht verfügbar ist, wird die Offline Seite aus dem Cache zurückgegeben.

Diese einfache Einführung zeigt, wie Sie die Zwischenspeicherung in ihrer Progressive Web App (PWA) verwenden. Jede PWA ist anders und kann unterschiedliche Zwischenspeicherungsstrategien verwenden. Ihr Code sieht möglicherweise anders aus, und Sie können unterschiedliche Zwischenspeicherungsstrategien für verschiedene Routen innerhalb der gleichen Anwendung verwenden.

## Verwenden von IndexedDB in ihrer PWA zum Speichern strukturierter Daten

`IndexedDB` ist eine API zum Speichern strukturierter Daten. Ähnlich wie bei der `Cache` API ist Sie auch asynchron, was bedeutet, dass Sie Sie im Hauptthread oder mit webarbeitern wie Dienst Mitarbeitern verwenden können. Verwenden Sie die `IndexedDB` API zum Speichern einer beträchtlichen Menge strukturierter Daten auf dem Client oder Binärdaten wie verschlüsselte Medienobjekte. Weitere Informationen finden Sie unter [MDN Primer][MDNIndexeddbApiUsing]für die Verwendung von IndexedDB.

## Grundlegendes zu den Speicheroptionen für PWAs

Manchmal müssen Sie möglicherweise kleine Datenmengen speichern, um Ihren Benutzern eine bessere Offline Nutzung zu ermöglichen. Wenn dies der Fall ist, können Sie feststellen, dass die Einfachheit des Schlüssel-Wert-Paar-Systems für Webspeicher Ihren Anforderungen entspricht.  

> [!IMPORTANT]
> Der Webspeicher ist ein synchroner Prozess und steht nicht zur Verwendung in Arbeitsthreads wie Service Mitarbeitern zur Verfügung. Eine starke Nutzung kann zu Leistungsproblemen für Ihre Anwendung führen. 


Es gibt zwei Arten von Webspeicher: `localStorage` und `sessionStorage` . Jeder wird als separater Datenspeicher für die Domäne isoliert verwaltet, die ihn erstellt hat. `sessionStorage` wird nur für die Dauer der Browsersitzung beibehalten (beispielsweise, während der Browser geöffnet ist, der Aktualisierungen und Wiederherstellung umfasst). `localStorage` bleibt bestehen, bis die Daten vom Code, vom Benutzer oder vom Browser entfernt wurden (beispielsweise, wenn nur ein limitierter Speicher verfügbar ist). Der folgende Codeausschnitt zeigt, wie die Verwendung `localStorage` erfolgt, was mit der Verwendung vergleichbar ist `sessionStorage` .

```javascript
var data = {
    title: document.querySelector("[property='og:title']").getAttribute("content"),
    description: document.querySelector( "meta[name='description']" ).getAttribute("content")
};
localStorage.setItem( window.location, JSON.stringify(data) );
```  

Dieser Codeausschnitt greift Metadaten über die aktuelle Seite auf und speichert Sie in einem JavaScript-Objekt. Anschließend speichert Sie diesen Wert als JSON-Datei unter `localStorage` Verwendung der `setItem()` Methode und weist einen Schlüssel zu, der der aktuellen `window.location` URL entspricht. Sie können die Informationen aus `localStorage` der Verwendung der `getItem()` Methode abrufen. 

Der folgende Codeausschnitt zeigt, wie Sie mithilfe der Zwischenspeicherung `localstorage` zwischengespeicherte Seiten auflisten und Metadaten extrahieren können, um eine Aufgabe auszuführen, beispielsweise das Erstellen einer Liste von Links.

```javascript
caches.open( "pages" )
      .then( cache => {
    cache.keys()
         .then( keys => {
        if ( keys.length )
        {
            keys.forEach( insertOfflineLink );
        }
    })
});

function insertOfflineLink( request ) {
    var data = JSON.parse( localStorage.getItem( request.url ) );
    // If data exists and this page is not an offline page, assuming that offline pages have the word offline in the URL.
    if ( data && request.url.indexOf('offline') < 0  )
    {
        // Build a link and insert it into the page.
    }
}
```  

Die `insertOfflineLink()` Methode übergibt die URL der Anforderung `localStorage.getItem()` an die Methode, um gespeicherte Metadaten abzurufen. Die abgerufenen Daten werden überprüft, um festzustellen, ob Sie vorhanden sind, und wenn dies der Fall ist, kann eine Aktion für die Daten ausgeführt werden, beispielsweise das Erstellen und Einfügen des Markups, um es anzuzeigen.

## Testen auf Netzwerkverbindungen in ihrer PWA

Neben dem Speichern von Informationen für die Offlineverwendung ist es hilfreich zu wissen, wann eine Netzwerkverbindung verfügbar ist, um Daten zu synchronisieren oder Benutzer darüber zu informieren, dass sich der Netzwerkstatus geändert hat. Verwenden Sie die folgenden Optionen, um die Netzwerkkonnektivität zu testen.

### Navigator. Online  

Die `navigator.onLine` Eigenschaft ist ein boolescher Wert, mit dem Sie den aktuellen Status des Netzwerks ermitteln können. Wenn der Wert lautet `true` , ist der Benutzer online, ansonsten ist der Benutzer offline.

### Online-und Offline Ereignisse  

Es ist hilfreich, zu wissen, ob das Netzwerk verfügbar ist, aber Sie möchten möglicherweise Maßnahmen ergreifen, wenn sich die Netzwerkverbindung ändert. In diesem Fall möchten Sie möglicherweise zuhören und als Reaktion auf Netzwerkereignisse Maßnahmen ergreifen. Die Ereignisse sind für die `window` Elemente, `document` und verfügbar, `document.body` wie im folgenden Codeausschnitt angezeigt.

```javascript
window.addEventListener("online",  function(){
    console.log("You are online!");
});
window.addEventListener("offline", function(){
    console.log("Oh no, you lost your network connection.");
});
```  

## Weitere Informationen  

Weitere Informationen zum Verwalten von Offlineszenarien finden Sie auf den folgenden Seiten.  

*   [Cache][MDNCache]  
*   [IndexedDB][MDNIndexeddbApi]  
*   [Dienstmitarbeiter][MDNServiceWorker]  
*   [Web Storage][MDNWebStorageApi]  
*   [Navigator. Online][MDNNavigatoronline]  
*   [Online-und Offline Ereignisse][MDNNavigatoronlineOfflineEvents]  
*   [Anforderung mit Absicht: Caching-Strategien im Zeitalter der PWAs][AlistapartRequestIntentCachingStrategiesAgePwas]

<!-- links -->  

[MDNCache]: https://developer.mozilla.org/docs/Web/API/Cache "Cache | MDN"  
[MDNIndexeddbApi]: https://developer.mozilla.org/docs/Web/API/IndexedDB_API "IndexedDB-API | MDN"  
[MDNIndexeddbApiUsing]: https://developer.mozilla.org/docs/Web/API/IndexedDB_API/Using_IndexedDB "Verwenden der IndexDb-IndexDb-API | MDN"  
[MDNServiceWorker]: https://developer.mozilla.org/docs/Web/API/ServiceWorker "ServiceWorker | MDN"  
[MDNWebStorageApi]: https://developer.mozilla.org/docs/Web/API/Web_Storage_API "Web Storage-API | MDN"  
[MDNNavigatoronline]: https://developer.mozilla.org/docs/Web/API/NavigatorOnLine "NavigatorOnLine | MDN"  
[MDNNavigatoronlineOfflineEvents]: https://developer.mozilla.org/docs/Web/API/NavigatorOnLine/Online_and_offline_events "Online-und Offlineereignisse – NavigatorOnLine | MDN"  

[AbookapartGoingOffline]: https://abookapart.com/products/going-offline "Going Offline von Jeremy Keith | Ein Buch auseinander"  

[AlistapartRequestIntentCachingStrategiesAgePwas]: https://alistapart.com/article/request-with-intent-caching-strategies-in-the-age-of-pwas "Anforderung mit Absicht: Caching-Strategien im Zeitalter der PWAs von Aaron Gustafson | Eine Liste auseinander"  
