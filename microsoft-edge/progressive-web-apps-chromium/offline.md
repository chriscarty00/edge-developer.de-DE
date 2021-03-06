---
title: Unterstützung für Offline- und Netzwerkkonnektivität in Progressive Web Apps
description: Erfahren Sie, wie Sie unterstützende Technologien verwenden, um ausfallsichere Erfahrungen für unterschiedliche Netzwerkbedingungen zu erstellen.
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/07/2021
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: pwa
keywords: progressive Web-Apps, PWA, Edge, JavaScript, Windows, UWP, Microsoft Store
ms.openlocfilehash: 6b6031aac10161c16195c83496f8d8b5b842628e
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398077"
---
# <a name="offline-and-network-connectivity-support-in-progressive-web-apps"></a>Unterstützung für Offline- und Netzwerkkonnektivität in Progressive Web Apps

Viele Jahre lang waren Organisationen ungern bereit, in webbasierte Software über systemeigene Software zu investieren, da Webanwendungen von stabilen Netzwerkverbindungen abhängig waren. Heute bietet die Webplattform robuste Optionen, mit denen Benutzer weiterhin arbeiten können, auch wenn die Netzwerkverbindung instabil wird oder vollständig offline geht.

## <a name="use-the-caching-to-improve-performance-of-pwas"></a>Verwenden der Zwischenspeicherung zur Verbesserung der Leistung von PWAs

Mit der Einführung von [Service Workers][MDNServiceWorker]hat die Webplattform die API hinzugefügt, um Zugriff `Cache` auf verwaltete zwischengespeicherte Ressourcen zu ermöglichen. Diese zusagebasierte API ermöglicht Entwicklern das Speichern und Abrufen vieler Webressourcen – HTML, CSS, JavaScript, Bilder, JSON und so weiter. In der Regel wird die Cache-API im Kontext eines Service Workers verwendet, ist aber auch im Hauptthread des Objekts `window` verfügbar.

Eine häufige Verwendung für die API ist das Vorabcachen kritischer Ressourcen, wenn ein Service Worker installiert wird, wie im folgenden Codeausschnitt `Cache` gezeigt.  

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

Dieser Code, der während des Lebenszyklusereignis "Service Worker" ausgeführt wird, öffnet einen Cache mit dem Namen und fügt dann, wenn er über einen Zeiger auf den Cache verfügt, vier Ressourcen mithilfe der `install` `static-cache` -Methode `addAll()` hinzu.  Häufig wird der Ansatz mit dem Cacheabruf während eines Ereignisses `fetch` gekoppelt.   

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

Der Codeausschnitt wird im Service Worker ausgeführt, wenn der Browser `fetch` eine Anforderung für diese Website stellt. Innerhalb dieses Ereignisses gibt es eine bedingte Anweisung, die ausgeführt wird, wenn die Anforderung für eine HTML-Datei ist. Der Dienstmitarbeiter überprüft, ob die Datei bereits in einem beliebigen Cache vorhanden ist \(mithilfe der `match()` Methode\). Wenn die Anforderung im Cache vorhanden ist, wird dieses zwischengespeicherte Ergebnis zurückgegeben. Andernfalls wird eine neue für diese Ressource ausgeführt, eine Kopie der Antwort wird für einen späteren Zeitpunkt zwischengespeichert, und die `fetch` Antwort wird zurückgegeben. Wenn der `fetch` Fehler auftritt, da das Netzwerk nicht verfügbar ist, wird die Offlineseite aus dem Cache zurückgegeben.

Diese einfache Einführung zeigt, wie Sie die Zwischenspeicherung in Ihrer progressiven Web-App (PWA) verwenden. Jede PWA ist unterschiedlich und kann unterschiedliche Zwischenspeicherungsstrategien verwenden. Ihr Code sieht möglicherweise anders aus, und Sie können unterschiedliche Zwischenspeicherungsstrategien für verschiedene Routen innerhalb derselben Anwendung verwenden.

## <a name="use-indexeddb-in-your-pwa-to-store-structured-data"></a>Verwenden von IndexedDB in Ihrem PWA zum Speichern strukturierter Daten

`IndexedDB` ist eine API zum Speichern strukturierter Daten. Ähnlich wie die API ist sie auch asynchron, was bedeutet, dass Sie sie im Hauptthread oder mit Web Workers wie `Cache` Service Workers verwenden können. Verwenden Sie die API zum Speichern einer großen Menge strukturierter Daten auf dem Client oder binärer Daten, z. B. `IndexedDB` verschlüsselter Medienobjekte. Weitere Informationen finden Sie unter [MDN primer on using IndexedDB][MDNIndexeddbApiUsing].

## <a name="understand-storage-options-for-pwas"></a>Verstehen von Speicheroptionen für PWAs

Manchmal müssen Sie kleine Datenmengen speichern, um ihren Benutzern eine bessere Offlineerfahrung zu bieten. Wenn dies der Fall ist, können Sie feststellen, dass die Einfachheit des Schlüssel-Wert-Paar-Systems von Webspeicher ihren Anforderungen entspricht.  

> [!IMPORTANT]
> Webspeicher ist ein synchroner Prozess und steht nicht für die Verwendung in Arbeitsthreads wie z. B. Service Workers zur Verfügung. Eine hohe Auslastung kann zu Leistungsproblemen für Ihre Anwendung führen. 


Es gibt zwei Arten von Webspeicher: `localStorage` und `sessionStorage` . Jeder wird als separater Datenspeicher verwaltet, der für die Domäne isoliert ist, von der er erstellt wurde. `sessionStorage` wird nur für die Dauer der Browsersitzung beibehalten (z. B. während des geöffneten Browsers, einschließlich Aktualisierung und Wiederherstellung). `localStorage` bleibt so lange erhalten, bis die Daten durch den Code, den Benutzer oder den Browser entfernt werden (z. B. wenn begrenzter Speicherplatz verfügbar ist). Der folgende Codeausschnitt zeigt, wie sie `localStorage` verwendet werden. Dies ähnelt der `sessionStorage` Verwendung.

```javascript
var data = {
    title: document.querySelector("[property='og:title']").getAttribute("content"),
    description: document.querySelector( "meta[name='description']" ).getAttribute("content")
};
localStorage.setItem( window.location, JSON.stringify(data) );
```  

Dieser Codeausschnitt greift Metadaten zur aktuellen Seite auf und speichert sie in einem JavaScript-Objekt. Anschließend speichert sie diesen Wert als JSON unter Verwendung der Methode und weist einen Schlüssel `localStorage` gleich der aktuellen URL `setItem()` `window.location` zu. Sie können die Informationen mithilfe der `localStorage` -Methode `getItem()` abrufen. 

Der folgende Codeausschnitt zeigt, wie Zwischenspeicherung mit zum Aufzählen zwischengespeicherter Seiten und Extrahieren von Metadaten verwendet wird, um eine Aufgabe auszuführen, z. B. das Erstellen einer Liste `localstorage` von Links.

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

Die `insertOfflineLink()` Methode übergibt die URL der Anforderung an die `localStorage.getItem()` -Methode, um alle gespeicherten Metadaten abzurufen. Die abgerufenen Daten werden überprüft, um zu sehen, ob sie vorhanden sind, und in diesem Fällen kann eine Aktion für die Daten wie das Erstellen und Einfügen des Markups zum Anzeigen der Daten ergriffen werden.

## <a name="test-for-network-connections-in-your-pwa"></a>Testen auf Netzwerkverbindungen in Ihrem PWA

Neben dem Speichern von Informationen für die Offlineverwendung ist es hilfreich zu wissen, wann eine Netzwerkverbindung verfügbar ist, um Daten zu synchronisieren oder Benutzer darüber zu informieren, dass sich der Netzwerkstatus geändert hat. Verwenden Sie die folgenden Optionen, um die Netzwerkkonnektivität zu testen.

### <a name="navigatoronline"></a>navigator.onLine  

Die `navigator.onLine` Eigenschaft ist ein boolescher Wert, mit dem Sie den aktuellen Status des Netzwerks kennen. Wenn der Wert `true` ist, ist der Benutzer online, andernfalls ist der Benutzer offline.

### <a name="online-and-offline-events"></a>Online- und Offlineereignisse  

Es ist hilfreich, zu wissen, ob das Netzwerk verfügbar ist, sie sollten jedoch möglicherweise Maßnahmen ergreifen, wenn sich die Netzwerkverbindung ändert. In dieser Situation können Sie als Reaktion auf Netzwerkereignisse zuhören und Maßnahmen ergreifen. Die Ereignisse sind für die `window` , `document` und -Elemente verfügbar, wie im folgenden `document.body` Codeausschnitt angezeigt.

```javascript
window.addEventListener("online",  function(){
    console.log("You are online!");
});
window.addEventListener("offline", function(){
    console.log("Oh no, you lost your network connection.");
});
```  

## <a name="see-also"></a>Weitere Informationen  

Weitere Informationen zum Verwalten von Offlineszenarien finden Sie auf den folgenden Seiten.  

*   [Cache][MDNCache]  
*   [IndexedDB][MDNIndexeddbApi]  
*   [Service Worker][MDNServiceWorker]  
*   [Webspeicher][MDNWebStorageApi]  
*   [navigator.onLine][MDNNavigatoronline]  
*   [Online- und Offlineereignisse][MDNNavigatoronlineOfflineEvents]  
*   [Anforderung mit Absicht: Zwischenspeichern von Strategien im Alter von PWAs][AlistapartRequestIntentCachingStrategiesAgePwas]
    
<!-- links -->  

[MDNCache]: https://developer.mozilla.org/docs/Web/API/Cache "Cache | MDN"  
[MDNIndexeddbApi]: https://developer.mozilla.org/docs/Web/API/IndexedDB_API "IndexedDB-API-| MDN"  
[MDNIndexeddbApiUsing]: https://developer.mozilla.org/docs/Web/API/IndexedDB_API/Using_IndexedDB "Verwenden von IndexDb – IndexDB-API-| MDN"  
[MDNServiceWorker]: https://developer.mozilla.org/docs/Web/API/ServiceWorker "ServiceWorker-| MDN"  
[MDNWebStorageApi]: https://developer.mozilla.org/docs/Web/API/Web_Storage_API "Webspeicher-API-| MDN"  
[MDNNavigatoronline]: https://developer.mozilla.org/docs/Web/API/NavigatorOnLine "NavigatorOnLine | MDN"  
[MDNNavigatoronlineOfflineEvents]: https://developer.mozilla.org/docs/Web/API/NavigatorOnLine/Online_and_offline_events "Online- und Offlineereignisse – NavigatorOnLine | MDN"  

[AbookapartGoingOffline]: https://abookapart.com/products/going-offline "Going Offline by Jeremy | A Book Apart"  

[AlistapartRequestIntentCachingStrategiesAgePwas]: https://alistapart.com/article/request-with-intent-caching-strategies-in-the-age-of-pwas "Request with Intent: Caching Strategies in the Age of PWAs von Aaron | Eine Voneinander entfernte Liste"  
