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
# <span data-ttu-id="49252-104">Unterstützung für Offline-und Netzwerkkonnektivität in progressiven Web-Apps</span><span class="sxs-lookup"><span data-stu-id="49252-104">Offline and network connectivity support in Progressive Web Apps</span></span>

<span data-ttu-id="49252-105">Viele Jahre lang zögerten Organisationen nicht, stark in webbasierte Software über native Software zu investieren, da Webanwendungen von stabilen Netzwerkverbindungen abhingen.</span><span class="sxs-lookup"><span data-stu-id="49252-105">For many years organizations were reluctant to invest heavily in web-based software over native software because web applications depended on stable network connections.</span></span> <span data-ttu-id="49252-106">Heute bietet die Webplattform nun robuste Optionen, mit denen Benutzer weiterhin arbeiten können, auch wenn die Netzwerkverbindung instabil wird oder vollständig offline geht.</span><span class="sxs-lookup"><span data-stu-id="49252-106">Today, the web platform now offers robust options that enable users to continue working, even if the network connection becomes unstable or goes completely offline.</span></span>

## <span data-ttu-id="49252-107">Verwenden der Zwischenspeicherung zum Verbessern der Leistung von PWAs</span><span class="sxs-lookup"><span data-stu-id="49252-107">Use the caching to improve performance of PWAs</span></span>

<span data-ttu-id="49252-108">Mit der Einführung von [Service Mitarbeitern][MDNServiceWorker]hat die Webplattform die API hinzugefügt, `Cache` um den Zugriff auf verwaltete zwischengespeicherte Ressourcen zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="49252-108">With the introduction of [Service Workers][MDNServiceWorker], the web platform added the `Cache` API to provide access to managed cached resources.</span></span> <span data-ttu-id="49252-109">Mit dieser Promise-basierten API können Entwickler viele Webressourcen speichern und Abrufen – HTML, CSS, JavaScript, Bilder, JSON usw.</span><span class="sxs-lookup"><span data-stu-id="49252-109">This Promise-based API allows developers to store and retrieve many web resources—HTML, CSS, JavaScript, images, JSON, and so on.</span></span> <span data-ttu-id="49252-110">In der Regel wird die Cache-API innerhalb des Kontexts eines Dienstmitarbeiter verwendet, ist aber auch im Hauptthread des Objekts verfügbar `window` .</span><span class="sxs-lookup"><span data-stu-id="49252-110">Usually, the Cache API is used within the context of a Service Worker, but it is also available in the main thread on the `window` object.</span></span>

<span data-ttu-id="49252-111">Eine häufige Verwendung für die `Cache` API besteht darin, wichtige Ressourcen vor dem Cache zu speichern, wenn ein Dienstmitarbeiter installiert wird, wie im folgenden Codeausschnitt dargestellt.</span><span class="sxs-lookup"><span data-stu-id="49252-111">One common use for the `Cache` API is to pre-cache critical resources when a Service Worker is installed, as shown in the following code snippet.</span></span>  

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

<span data-ttu-id="49252-112">Dieser Code, der während des Lebenszyklus des Service Worker `install` -Ereignisses ausgeführt wird, öffnet einen Cache mit dem Namen `static-cache` und fügt ihm dann mit der Methode vier Ressourcen hinzu, wenn er über einen Zeiger auf den Cache verfügt `addAll()` .</span><span class="sxs-lookup"><span data-stu-id="49252-112">This code, which runs during the Service Worker `install` life cycle event, opens a cache named `static-cache` and then, when it has a pointer to the cache, adds four resources to it using the `addAll()` method.</span></span>  <span data-ttu-id="49252-113">Häufig ist der Ansatz mit dem Abrufen des Caches während eines Ereignisses gekoppelt. `fetch`</span><span class="sxs-lookup"><span data-stu-id="49252-113">Often the approach is coupled with cache retrieval during a `fetch` event</span></span>   

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

<span data-ttu-id="49252-114">Der Codeausschnitt wird innerhalb des Dienst Arbeitsthreads ausgeführt, wenn der Browser eine `fetch` Anforderung für diese Website vornimmt.</span><span class="sxs-lookup"><span data-stu-id="49252-114">The code snippet runs within the Service Worker whenever the browser makes a `fetch` request for this site.</span></span> <span data-ttu-id="49252-115">Innerhalb dieses Ereignisses gibt es eine bedingte Anweisung, die ausgeführt wird, wenn die Anforderung eine HTML-Datei ist.</span><span class="sxs-lookup"><span data-stu-id="49252-115">Within that event, there is a conditional statement that runs if the request is for an HTML file.</span></span> <span data-ttu-id="49252-116">Der Dienstmitarbeiter überprüft, ob die Datei bereits in einem beliebigen Cache vorhanden ist \ (mit der `match()` Methode \).</span><span class="sxs-lookup"><span data-stu-id="49252-116">The Service Worker checks to see if the file already exists in any cache \(using the `match()` method\).</span></span> <span data-ttu-id="49252-117">Wenn die Anforderung im Cache vorhanden ist, wird das zwischengespeicherte Ergebnis zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="49252-117">If the request exists in the cache, that cached result is returned.</span></span> <span data-ttu-id="49252-118">Wenn dies nicht der Fall ist, wird eine neue `fetch` für diese Ressource ausgeführt, eine Kopie der Antwort wird für später zwischengespeichert, und die Antwort wird zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="49252-118">If not, a new `fetch` for that resource is run, a copy of the response is cached for later, and the response is returned.</span></span> <span data-ttu-id="49252-119">Wenn das `fetch` fehlschlägt, weil das Netzwerk nicht verfügbar ist, wird die Offline Seite aus dem Cache zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="49252-119">If the `fetch` fails because the network is unavailable, the offline page is returned from the cache.</span></span>

<span data-ttu-id="49252-120">Diese einfache Einführung zeigt, wie Sie die Zwischenspeicherung in ihrer Progressive Web App (PWA) verwenden.</span><span class="sxs-lookup"><span data-stu-id="49252-120">This simple introduction shows how to use caching in your progressive web app (PWA).</span></span> <span data-ttu-id="49252-121">Jede PWA ist anders und kann unterschiedliche Zwischenspeicherungsstrategien verwenden.</span><span class="sxs-lookup"><span data-stu-id="49252-121">Each PWA is different and may use different caching strategies.</span></span> <span data-ttu-id="49252-122">Ihr Code sieht möglicherweise anders aus, und Sie können unterschiedliche Zwischenspeicherungsstrategien für verschiedene Routen innerhalb der gleichen Anwendung verwenden.</span><span class="sxs-lookup"><span data-stu-id="49252-122">Your code may look different, and you may use different caching strategies for different routes within the same application.</span></span>

## <span data-ttu-id="49252-123">Verwenden von IndexedDB in ihrer PWA zum Speichern strukturierter Daten</span><span class="sxs-lookup"><span data-stu-id="49252-123">Use IndexedDB in your PWA to store structured data</span></span>

`IndexedDB` <span data-ttu-id="49252-124">ist eine API zum Speichern strukturierter Daten.</span><span class="sxs-lookup"><span data-stu-id="49252-124">is an API for storing structured data.</span></span> <span data-ttu-id="49252-125">Ähnlich wie bei der `Cache` API ist Sie auch asynchron, was bedeutet, dass Sie Sie im Hauptthread oder mit webarbeitern wie Dienst Mitarbeitern verwenden können.</span><span class="sxs-lookup"><span data-stu-id="49252-125">Similar to the `Cache` API, it is also asynchronous, which means you may use it in the main thread or with Web Workers such as Service Workers.</span></span> <span data-ttu-id="49252-126">Verwenden Sie die `IndexedDB` API zum Speichern einer beträchtlichen Menge strukturierter Daten auf dem Client oder Binärdaten wie verschlüsselte Medienobjekte.</span><span class="sxs-lookup"><span data-stu-id="49252-126">Use the `IndexedDB` API for storing a significant amount of structured data on the client, or binary data, such as encrypted media objects.</span></span> <span data-ttu-id="49252-127">Weitere Informationen finden Sie unter [MDN Primer][MDNIndexeddbApiUsing]für die Verwendung von IndexedDB.</span><span class="sxs-lookup"><span data-stu-id="49252-127">For more information, see [MDN primer on using IndexedDB][MDNIndexeddbApiUsing].</span></span>

## <span data-ttu-id="49252-128">Grundlegendes zu den Speicheroptionen für PWAs</span><span class="sxs-lookup"><span data-stu-id="49252-128">Understand storage options for PWAs</span></span>

<span data-ttu-id="49252-129">Manchmal müssen Sie möglicherweise kleine Datenmengen speichern, um Ihren Benutzern eine bessere Offline Nutzung zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="49252-129">Sometimes you may need to store small amounts of data in order to provide a better offline experience for your users.</span></span> <span data-ttu-id="49252-130">Wenn dies der Fall ist, können Sie feststellen, dass die Einfachheit des Schlüssel-Wert-Paar-Systems für Webspeicher Ihren Anforderungen entspricht.</span><span class="sxs-lookup"><span data-stu-id="49252-130">If that is the case, you may find the simplicity of the key-value pair system of web storage meets your needs.</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="49252-131">Der Webspeicher ist ein synchroner Prozess und steht nicht zur Verwendung in Arbeitsthreads wie Service Mitarbeitern zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="49252-131">Web Storage is a synchronous process and is not available for use within worker threads such as Service Workers.</span></span> <span data-ttu-id="49252-132">Eine starke Nutzung kann zu Leistungsproblemen für Ihre Anwendung führen.</span><span class="sxs-lookup"><span data-stu-id="49252-132">Heavy usage may create performance issues for your application.</span></span> 


<span data-ttu-id="49252-133">Es gibt zwei Arten von Webspeicher: `localStorage` und `sessionStorage` .</span><span class="sxs-lookup"><span data-stu-id="49252-133">There are 2 types of Web Storage: `localStorage` and `sessionStorage`.</span></span> <span data-ttu-id="49252-134">Jeder wird als separater Datenspeicher für die Domäne isoliert verwaltet, die ihn erstellt hat.</span><span class="sxs-lookup"><span data-stu-id="49252-134">Each is maintained as a separate data store isolated to the domain that created it.</span></span> `sessionStorage` <span data-ttu-id="49252-135">wird nur für die Dauer der Browsersitzung beibehalten (beispielsweise, während der Browser geöffnet ist, der Aktualisierungen und Wiederherstellung umfasst).</span><span class="sxs-lookup"><span data-stu-id="49252-135">persists only for the duration of the browsing session (for example, while the browser is open, which includes refresh and restores).</span></span> `localStorage` <span data-ttu-id="49252-136">bleibt bestehen, bis die Daten vom Code, vom Benutzer oder vom Browser entfernt wurden (beispielsweise, wenn nur ein limitierter Speicher verfügbar ist).</span><span class="sxs-lookup"><span data-stu-id="49252-136">persists until the data is removed by the code, the user, or the browser (for example, when there is limited storage available).</span></span> <span data-ttu-id="49252-137">Der folgende Codeausschnitt zeigt, wie die Verwendung `localStorage` erfolgt, was mit der Verwendung vergleichbar ist `sessionStorage` .</span><span class="sxs-lookup"><span data-stu-id="49252-137">The following code snippet shows how to use `localStorage`, which is similar to how `sessionStorage` is used.</span></span>

```javascript
var data = {
    title: document.querySelector("[property='og:title']").getAttribute("content"),
    description: document.querySelector( "meta[name='description']" ).getAttribute("content")
};
localStorage.setItem( window.location, JSON.stringify(data) );
```  

<span data-ttu-id="49252-138">Dieser Codeausschnitt greift Metadaten über die aktuelle Seite auf und speichert Sie in einem JavaScript-Objekt.</span><span class="sxs-lookup"><span data-stu-id="49252-138">This code snippet grabs metadata about the current page and stores it in a JavaScript object.</span></span> <span data-ttu-id="49252-139">Anschließend speichert Sie diesen Wert als JSON-Datei unter `localStorage` Verwendung der `setItem()` Methode und weist einen Schlüssel zu, der der aktuellen `window.location` URL entspricht.</span><span class="sxs-lookup"><span data-stu-id="49252-139">Then it stores that value as JSON in `localStorage` using the `setItem()` method, and assigns a key equal to the current `window.location` URL.</span></span> <span data-ttu-id="49252-140">Sie können die Informationen aus `localStorage` der Verwendung der `getItem()` Methode abrufen.</span><span class="sxs-lookup"><span data-stu-id="49252-140">You may retrieve the information from `localStorage` using the `getItem()` method.</span></span> 

<span data-ttu-id="49252-141">Der folgende Codeausschnitt zeigt, wie Sie mithilfe der Zwischenspeicherung `localstorage` zwischengespeicherte Seiten auflisten und Metadaten extrahieren können, um eine Aufgabe auszuführen, beispielsweise das Erstellen einer Liste von Links.</span><span class="sxs-lookup"><span data-stu-id="49252-141">The following code snippet shows how to use caching with `localstorage` to enumerate cached pages and extract metadata to perform a task, such as building a list of links.</span></span>

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

<span data-ttu-id="49252-142">Die `insertOfflineLink()` Methode übergibt die URL der Anforderung `localStorage.getItem()` an die Methode, um gespeicherte Metadaten abzurufen.</span><span class="sxs-lookup"><span data-stu-id="49252-142">The `insertOfflineLink()` method passes the URL of the request into the `localStorage.getItem()` method to retrieve any stored metadata.</span></span> <span data-ttu-id="49252-143">Die abgerufenen Daten werden überprüft, um festzustellen, ob Sie vorhanden sind, und wenn dies der Fall ist, kann eine Aktion für die Daten ausgeführt werden, beispielsweise das Erstellen und Einfügen des Markups, um es anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="49252-143">The retrieved data is checked to see if it exists, and if it does, an action can be taken on the data, such as building and inserting the markup to display it.</span></span>

## <span data-ttu-id="49252-144">Testen auf Netzwerkverbindungen in ihrer PWA</span><span class="sxs-lookup"><span data-stu-id="49252-144">Test for network connections in your PWA</span></span>

<span data-ttu-id="49252-145">Neben dem Speichern von Informationen für die Offlineverwendung ist es hilfreich zu wissen, wann eine Netzwerkverbindung verfügbar ist, um Daten zu synchronisieren oder Benutzer darüber zu informieren, dass sich der Netzwerkstatus geändert hat.</span><span class="sxs-lookup"><span data-stu-id="49252-145">In addition to storing information for offline use, it is helpful to know when a network connection is available in order to synchronize data or inform users that the network status has changed.</span></span> <span data-ttu-id="49252-146">Verwenden Sie die folgenden Optionen, um die Netzwerkkonnektivität zu testen.</span><span class="sxs-lookup"><span data-stu-id="49252-146">Use the following options to test for network connectivity.</span></span>

### <span data-ttu-id="49252-147">Navigator. Online</span><span class="sxs-lookup"><span data-stu-id="49252-147">navigator.onLine</span></span>  

<span data-ttu-id="49252-148">Die `navigator.onLine` Eigenschaft ist ein boolescher Wert, mit dem Sie den aktuellen Status des Netzwerks ermitteln können.</span><span class="sxs-lookup"><span data-stu-id="49252-148">The `navigator.onLine` property is a boolean that lets you know the current status of the network.</span></span> <span data-ttu-id="49252-149">Wenn der Wert lautet `true` , ist der Benutzer online, ansonsten ist der Benutzer offline.</span><span class="sxs-lookup"><span data-stu-id="49252-149">If the value is `true`, the user is online, otherwise the user is offline.</span></span>

### <span data-ttu-id="49252-150">Online-und Offline Ereignisse</span><span class="sxs-lookup"><span data-stu-id="49252-150">Online and Offline Events</span></span>  

<span data-ttu-id="49252-151">Es ist hilfreich, zu wissen, ob das Netzwerk verfügbar ist, aber Sie möchten möglicherweise Maßnahmen ergreifen, wenn sich die Netzwerkverbindung ändert.</span><span class="sxs-lookup"><span data-stu-id="49252-151">Knowing whether the network is available is helpful, but you may want to take action  when your network connectivity changes.</span></span> <span data-ttu-id="49252-152">In diesem Fall möchten Sie möglicherweise zuhören und als Reaktion auf Netzwerkereignisse Maßnahmen ergreifen.</span><span class="sxs-lookup"><span data-stu-id="49252-152">In this situation, you may want to listen and take action in response to network events.</span></span> <span data-ttu-id="49252-153">Die Ereignisse sind für die `window` Elemente, `document` und verfügbar, `document.body` wie im folgenden Codeausschnitt angezeigt.</span><span class="sxs-lookup"><span data-stu-id="49252-153">The events are available on the `window`, `document`, and `document.body` elements as displayed in the following code snippet.</span></span>

```javascript
window.addEventListener("online",  function(){
    console.log("You are online!");
});
window.addEventListener("offline", function(){
    console.log("Oh no, you lost your network connection.");
});
```  

## <span data-ttu-id="49252-154">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="49252-154">See also</span></span>  

<span data-ttu-id="49252-155">Weitere Informationen zum Verwalten von Offlineszenarien finden Sie auf den folgenden Seiten.</span><span class="sxs-lookup"><span data-stu-id="49252-155">To learn more about managing offline scenarios, see the following pages.</span></span>  

*   [<span data-ttu-id="49252-156">Cache</span><span class="sxs-lookup"><span data-stu-id="49252-156">Cache</span></span>][MDNCache]  
*   [<span data-ttu-id="49252-157">IndexedDB</span><span class="sxs-lookup"><span data-stu-id="49252-157">IndexedDB</span></span>][MDNIndexeddbApi]  
*   [<span data-ttu-id="49252-158">Dienstmitarbeiter</span><span class="sxs-lookup"><span data-stu-id="49252-158">Service Worker</span></span>][MDNServiceWorker]  
*   [<span data-ttu-id="49252-159">Web Storage</span><span class="sxs-lookup"><span data-stu-id="49252-159">Web Storage</span></span>][MDNWebStorageApi]  
*   [<span data-ttu-id="49252-160">Navigator. Online</span><span class="sxs-lookup"><span data-stu-id="49252-160">navigator.onLine</span></span>][MDNNavigatoronline]  
*   [<span data-ttu-id="49252-161">Online-und Offline Ereignisse</span><span class="sxs-lookup"><span data-stu-id="49252-161">Online and Offline Events</span></span>][MDNNavigatoronlineOfflineEvents]  
*   [<span data-ttu-id="49252-162">Anforderung mit Absicht: Caching-Strategien im Zeitalter der PWAs</span><span class="sxs-lookup"><span data-stu-id="49252-162">Request with Intent: Caching Strategies in the Age of PWAs</span></span>][AlistapartRequestIntentCachingStrategiesAgePwas]

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
