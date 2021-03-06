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
# <a name="offline-and-network-connectivity-support-in-progressive-web-apps"></a><span data-ttu-id="e703e-104">Unterstützung für Offline- und Netzwerkkonnektivität in Progressive Web Apps</span><span class="sxs-lookup"><span data-stu-id="e703e-104">Offline and network connectivity support in Progressive Web Apps</span></span>

<span data-ttu-id="e703e-105">Viele Jahre lang waren Organisationen ungern bereit, in webbasierte Software über systemeigene Software zu investieren, da Webanwendungen von stabilen Netzwerkverbindungen abhängig waren.</span><span class="sxs-lookup"><span data-stu-id="e703e-105">For many years organizations were reluctant to invest heavily in web-based software over native software because web applications depended on stable network connections.</span></span> <span data-ttu-id="e703e-106">Heute bietet die Webplattform robuste Optionen, mit denen Benutzer weiterhin arbeiten können, auch wenn die Netzwerkverbindung instabil wird oder vollständig offline geht.</span><span class="sxs-lookup"><span data-stu-id="e703e-106">Today, the web platform now offers robust options that enable users to continue working, even if the network connection becomes unstable or goes completely offline.</span></span>

## <a name="use-the-caching-to-improve-performance-of-pwas"></a><span data-ttu-id="e703e-107">Verwenden der Zwischenspeicherung zur Verbesserung der Leistung von PWAs</span><span class="sxs-lookup"><span data-stu-id="e703e-107">Use the caching to improve performance of PWAs</span></span>

<span data-ttu-id="e703e-108">Mit der Einführung von [Service Workers][MDNServiceWorker]hat die Webplattform die API hinzugefügt, um Zugriff `Cache` auf verwaltete zwischengespeicherte Ressourcen zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="e703e-108">With the introduction of [Service Workers][MDNServiceWorker], the web platform added the `Cache` API to provide access to managed cached resources.</span></span> <span data-ttu-id="e703e-109">Diese zusagebasierte API ermöglicht Entwicklern das Speichern und Abrufen vieler Webressourcen – HTML, CSS, JavaScript, Bilder, JSON und so weiter.</span><span class="sxs-lookup"><span data-stu-id="e703e-109">This Promise-based API allows developers to store and retrieve many web resources—HTML, CSS, JavaScript, images, JSON, and so on.</span></span> <span data-ttu-id="e703e-110">In der Regel wird die Cache-API im Kontext eines Service Workers verwendet, ist aber auch im Hauptthread des Objekts `window` verfügbar.</span><span class="sxs-lookup"><span data-stu-id="e703e-110">Usually, the Cache API is used within the context of a Service Worker, but it is also available in the main thread on the `window` object.</span></span>

<span data-ttu-id="e703e-111">Eine häufige Verwendung für die API ist das Vorabcachen kritischer Ressourcen, wenn ein Service Worker installiert wird, wie im folgenden Codeausschnitt `Cache` gezeigt.</span><span class="sxs-lookup"><span data-stu-id="e703e-111">One common use for the `Cache` API is to pre-cache critical resources when a Service Worker is installed, as shown in the following code snippet.</span></span>  

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

<span data-ttu-id="e703e-112">Dieser Code, der während des Lebenszyklusereignis "Service Worker" ausgeführt wird, öffnet einen Cache mit dem Namen und fügt dann, wenn er über einen Zeiger auf den Cache verfügt, vier Ressourcen mithilfe der `install` `static-cache` -Methode `addAll()` hinzu.</span><span class="sxs-lookup"><span data-stu-id="e703e-112">This code, which runs during the Service Worker `install` life cycle event, opens a cache named `static-cache` and then, when it has a pointer to the cache, adds four resources to it using the `addAll()` method.</span></span>  <span data-ttu-id="e703e-113">Häufig wird der Ansatz mit dem Cacheabruf während eines Ereignisses `fetch` gekoppelt.</span><span class="sxs-lookup"><span data-stu-id="e703e-113">Often the approach is coupled with cache retrieval during a `fetch` event</span></span>   

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

<span data-ttu-id="e703e-114">Der Codeausschnitt wird im Service Worker ausgeführt, wenn der Browser `fetch` eine Anforderung für diese Website stellt.</span><span class="sxs-lookup"><span data-stu-id="e703e-114">The code snippet runs within the Service Worker whenever the browser makes a `fetch` request for this site.</span></span> <span data-ttu-id="e703e-115">Innerhalb dieses Ereignisses gibt es eine bedingte Anweisung, die ausgeführt wird, wenn die Anforderung für eine HTML-Datei ist.</span><span class="sxs-lookup"><span data-stu-id="e703e-115">Within that event, there is a conditional statement that runs if the request is for an HTML file.</span></span> <span data-ttu-id="e703e-116">Der Dienstmitarbeiter überprüft, ob die Datei bereits in einem beliebigen Cache vorhanden ist \(mithilfe der `match()` Methode\).</span><span class="sxs-lookup"><span data-stu-id="e703e-116">The Service Worker checks to see if the file already exists in any cache \(using the `match()` method\).</span></span> <span data-ttu-id="e703e-117">Wenn die Anforderung im Cache vorhanden ist, wird dieses zwischengespeicherte Ergebnis zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="e703e-117">If the request exists in the cache, that cached result is returned.</span></span> <span data-ttu-id="e703e-118">Andernfalls wird eine neue für diese Ressource ausgeführt, eine Kopie der Antwort wird für einen späteren Zeitpunkt zwischengespeichert, und die `fetch` Antwort wird zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="e703e-118">If not, a new `fetch` for that resource is run, a copy of the response is cached for later, and the response is returned.</span></span> <span data-ttu-id="e703e-119">Wenn der `fetch` Fehler auftritt, da das Netzwerk nicht verfügbar ist, wird die Offlineseite aus dem Cache zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="e703e-119">If the `fetch` fails because the network is unavailable, the offline page is returned from the cache.</span></span>

<span data-ttu-id="e703e-120">Diese einfache Einführung zeigt, wie Sie die Zwischenspeicherung in Ihrer progressiven Web-App (PWA) verwenden.</span><span class="sxs-lookup"><span data-stu-id="e703e-120">This simple introduction shows how to use caching in your progressive web app (PWA).</span></span> <span data-ttu-id="e703e-121">Jede PWA ist unterschiedlich und kann unterschiedliche Zwischenspeicherungsstrategien verwenden.</span><span class="sxs-lookup"><span data-stu-id="e703e-121">Each PWA is different and may use different caching strategies.</span></span> <span data-ttu-id="e703e-122">Ihr Code sieht möglicherweise anders aus, und Sie können unterschiedliche Zwischenspeicherungsstrategien für verschiedene Routen innerhalb derselben Anwendung verwenden.</span><span class="sxs-lookup"><span data-stu-id="e703e-122">Your code may look different, and you may use different caching strategies for different routes within the same application.</span></span>

## <a name="use-indexeddb-in-your-pwa-to-store-structured-data"></a><span data-ttu-id="e703e-123">Verwenden von IndexedDB in Ihrem PWA zum Speichern strukturierter Daten</span><span class="sxs-lookup"><span data-stu-id="e703e-123">Use IndexedDB in your PWA to store structured data</span></span>

`IndexedDB` <span data-ttu-id="e703e-124">ist eine API zum Speichern strukturierter Daten.</span><span class="sxs-lookup"><span data-stu-id="e703e-124">is an API for storing structured data.</span></span> <span data-ttu-id="e703e-125">Ähnlich wie die API ist sie auch asynchron, was bedeutet, dass Sie sie im Hauptthread oder mit Web Workers wie `Cache` Service Workers verwenden können.</span><span class="sxs-lookup"><span data-stu-id="e703e-125">Similar to the `Cache` API, it is also asynchronous, which means you may use it in the main thread or with Web Workers such as Service Workers.</span></span> <span data-ttu-id="e703e-126">Verwenden Sie die API zum Speichern einer großen Menge strukturierter Daten auf dem Client oder binärer Daten, z. B. `IndexedDB` verschlüsselter Medienobjekte.</span><span class="sxs-lookup"><span data-stu-id="e703e-126">Use the `IndexedDB` API for storing a significant amount of structured data on the client, or binary data, such as encrypted media objects.</span></span> <span data-ttu-id="e703e-127">Weitere Informationen finden Sie unter [MDN primer on using IndexedDB][MDNIndexeddbApiUsing].</span><span class="sxs-lookup"><span data-stu-id="e703e-127">For more information, navigate to [MDN primer on using IndexedDB][MDNIndexeddbApiUsing].</span></span>

## <a name="understand-storage-options-for-pwas"></a><span data-ttu-id="e703e-128">Verstehen von Speicheroptionen für PWAs</span><span class="sxs-lookup"><span data-stu-id="e703e-128">Understand storage options for PWAs</span></span>

<span data-ttu-id="e703e-129">Manchmal müssen Sie kleine Datenmengen speichern, um ihren Benutzern eine bessere Offlineerfahrung zu bieten.</span><span class="sxs-lookup"><span data-stu-id="e703e-129">Sometimes you may need to store small amounts of data in order to provide a better offline experience for your users.</span></span> <span data-ttu-id="e703e-130">Wenn dies der Fall ist, können Sie feststellen, dass die Einfachheit des Schlüssel-Wert-Paar-Systems von Webspeicher ihren Anforderungen entspricht.</span><span class="sxs-lookup"><span data-stu-id="e703e-130">If that is the case, you may find the simplicity of the key-value pair system of web storage meets your needs.</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="e703e-131">Webspeicher ist ein synchroner Prozess und steht nicht für die Verwendung in Arbeitsthreads wie z. B. Service Workers zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="e703e-131">Web Storage is a synchronous process and is not available for use within worker threads such as Service Workers.</span></span> <span data-ttu-id="e703e-132">Eine hohe Auslastung kann zu Leistungsproblemen für Ihre Anwendung führen.</span><span class="sxs-lookup"><span data-stu-id="e703e-132">Heavy usage may create performance issues for your application.</span></span> 


<span data-ttu-id="e703e-133">Es gibt zwei Arten von Webspeicher: `localStorage` und `sessionStorage` .</span><span class="sxs-lookup"><span data-stu-id="e703e-133">There are 2 types of Web Storage: `localStorage` and `sessionStorage`.</span></span> <span data-ttu-id="e703e-134">Jeder wird als separater Datenspeicher verwaltet, der für die Domäne isoliert ist, von der er erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="e703e-134">Each is maintained as a separate data store isolated to the domain that created it.</span></span> `sessionStorage` <span data-ttu-id="e703e-135">wird nur für die Dauer der Browsersitzung beibehalten (z. B. während des geöffneten Browsers, einschließlich Aktualisierung und Wiederherstellung).</span><span class="sxs-lookup"><span data-stu-id="e703e-135">persists only for the duration of the browsing session (for example, while the browser is open, which includes refresh and restores).</span></span> `localStorage` <span data-ttu-id="e703e-136">bleibt so lange erhalten, bis die Daten durch den Code, den Benutzer oder den Browser entfernt werden (z. B. wenn begrenzter Speicherplatz verfügbar ist).</span><span class="sxs-lookup"><span data-stu-id="e703e-136">persists until the data is removed by the code, the user, or the browser (for example, when there is limited storage available).</span></span> <span data-ttu-id="e703e-137">Der folgende Codeausschnitt zeigt, wie sie `localStorage` verwendet werden. Dies ähnelt der `sessionStorage` Verwendung.</span><span class="sxs-lookup"><span data-stu-id="e703e-137">The following code snippet shows how to use `localStorage`, which is similar to how `sessionStorage` is used.</span></span>

```javascript
var data = {
    title: document.querySelector("[property='og:title']").getAttribute("content"),
    description: document.querySelector( "meta[name='description']" ).getAttribute("content")
};
localStorage.setItem( window.location, JSON.stringify(data) );
```  

<span data-ttu-id="e703e-138">Dieser Codeausschnitt greift Metadaten zur aktuellen Seite auf und speichert sie in einem JavaScript-Objekt.</span><span class="sxs-lookup"><span data-stu-id="e703e-138">This code snippet grabs metadata about the current page and stores it in a JavaScript object.</span></span> <span data-ttu-id="e703e-139">Anschließend speichert sie diesen Wert als JSON unter Verwendung der Methode und weist einen Schlüssel `localStorage` gleich der aktuellen URL `setItem()` `window.location` zu.</span><span class="sxs-lookup"><span data-stu-id="e703e-139">Then it stores that value as JSON in `localStorage` using the `setItem()` method, and assigns a key equal to the current `window.location` URL.</span></span> <span data-ttu-id="e703e-140">Sie können die Informationen mithilfe der `localStorage` -Methode `getItem()` abrufen.</span><span class="sxs-lookup"><span data-stu-id="e703e-140">You may retrieve the information from `localStorage` using the `getItem()` method.</span></span> 

<span data-ttu-id="e703e-141">Der folgende Codeausschnitt zeigt, wie Zwischenspeicherung mit zum Aufzählen zwischengespeicherter Seiten und Extrahieren von Metadaten verwendet wird, um eine Aufgabe auszuführen, z. B. das Erstellen einer Liste `localstorage` von Links.</span><span class="sxs-lookup"><span data-stu-id="e703e-141">The following code snippet shows how to use caching with `localstorage` to enumerate cached pages and extract metadata to perform a task, such as building a list of links.</span></span>

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

<span data-ttu-id="e703e-142">Die `insertOfflineLink()` Methode übergibt die URL der Anforderung an die `localStorage.getItem()` -Methode, um alle gespeicherten Metadaten abzurufen.</span><span class="sxs-lookup"><span data-stu-id="e703e-142">The `insertOfflineLink()` method passes the URL of the request into the `localStorage.getItem()` method to retrieve any stored metadata.</span></span> <span data-ttu-id="e703e-143">Die abgerufenen Daten werden überprüft, um zu sehen, ob sie vorhanden sind, und in diesem Fällen kann eine Aktion für die Daten wie das Erstellen und Einfügen des Markups zum Anzeigen der Daten ergriffen werden.</span><span class="sxs-lookup"><span data-stu-id="e703e-143">The retrieved data is checked to see if it exists, and if it does, an action can be taken on the data, such as building and inserting the markup to display it.</span></span>

## <a name="test-for-network-connections-in-your-pwa"></a><span data-ttu-id="e703e-144">Testen auf Netzwerkverbindungen in Ihrem PWA</span><span class="sxs-lookup"><span data-stu-id="e703e-144">Test for network connections in your PWA</span></span>

<span data-ttu-id="e703e-145">Neben dem Speichern von Informationen für die Offlineverwendung ist es hilfreich zu wissen, wann eine Netzwerkverbindung verfügbar ist, um Daten zu synchronisieren oder Benutzer darüber zu informieren, dass sich der Netzwerkstatus geändert hat.</span><span class="sxs-lookup"><span data-stu-id="e703e-145">In addition to storing information for offline use, it is helpful to know when a network connection is available in order to synchronize data or inform users that the network status has changed.</span></span> <span data-ttu-id="e703e-146">Verwenden Sie die folgenden Optionen, um die Netzwerkkonnektivität zu testen.</span><span class="sxs-lookup"><span data-stu-id="e703e-146">Use the following options to test for network connectivity.</span></span>

### <a name="navigatoronline"></a><span data-ttu-id="e703e-147">navigator.onLine</span><span class="sxs-lookup"><span data-stu-id="e703e-147">navigator.onLine</span></span>  

<span data-ttu-id="e703e-148">Die `navigator.onLine` Eigenschaft ist ein boolescher Wert, mit dem Sie den aktuellen Status des Netzwerks kennen.</span><span class="sxs-lookup"><span data-stu-id="e703e-148">The `navigator.onLine` property is a boolean that lets you know the current status of the network.</span></span> <span data-ttu-id="e703e-149">Wenn der Wert `true` ist, ist der Benutzer online, andernfalls ist der Benutzer offline.</span><span class="sxs-lookup"><span data-stu-id="e703e-149">If the value is `true`, the user is online, otherwise the user is offline.</span></span>

### <a name="online-and-offline-events"></a><span data-ttu-id="e703e-150">Online- und Offlineereignisse</span><span class="sxs-lookup"><span data-stu-id="e703e-150">Online and Offline Events</span></span>  

<span data-ttu-id="e703e-151">Es ist hilfreich, zu wissen, ob das Netzwerk verfügbar ist, sie sollten jedoch möglicherweise Maßnahmen ergreifen, wenn sich die Netzwerkverbindung ändert.</span><span class="sxs-lookup"><span data-stu-id="e703e-151">Knowing whether the network is available is helpful, but you may want to take action  when your network connectivity changes.</span></span> <span data-ttu-id="e703e-152">In dieser Situation können Sie als Reaktion auf Netzwerkereignisse zuhören und Maßnahmen ergreifen.</span><span class="sxs-lookup"><span data-stu-id="e703e-152">In this situation, you may want to listen and take action in response to network events.</span></span> <span data-ttu-id="e703e-153">Die Ereignisse sind für die `window` , `document` und -Elemente verfügbar, wie im folgenden `document.body` Codeausschnitt angezeigt.</span><span class="sxs-lookup"><span data-stu-id="e703e-153">The events are available on the `window`, `document`, and `document.body` elements as displayed in the following code snippet.</span></span>

```javascript
window.addEventListener("online",  function(){
    console.log("You are online!");
});
window.addEventListener("offline", function(){
    console.log("Oh no, you lost your network connection.");
});
```  

## <a name="see-also"></a><span data-ttu-id="e703e-154">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="e703e-154">See also</span></span>  

<span data-ttu-id="e703e-155">Weitere Informationen zum Verwalten von Offlineszenarien finden Sie auf den folgenden Seiten.</span><span class="sxs-lookup"><span data-stu-id="e703e-155">To learn more about managing offline scenarios, navigate to the following pages.</span></span>  

*   [<span data-ttu-id="e703e-156">Cache</span><span class="sxs-lookup"><span data-stu-id="e703e-156">Cache</span></span>][MDNCache]  
*   [<span data-ttu-id="e703e-157">IndexedDB</span><span class="sxs-lookup"><span data-stu-id="e703e-157">IndexedDB</span></span>][MDNIndexeddbApi]  
*   [<span data-ttu-id="e703e-158">Service Worker</span><span class="sxs-lookup"><span data-stu-id="e703e-158">Service Worker</span></span>][MDNServiceWorker]  
*   [<span data-ttu-id="e703e-159">Webspeicher</span><span class="sxs-lookup"><span data-stu-id="e703e-159">Web Storage</span></span>][MDNWebStorageApi]  
*   [<span data-ttu-id="e703e-160">navigator.onLine</span><span class="sxs-lookup"><span data-stu-id="e703e-160">navigator.onLine</span></span>][MDNNavigatoronline]  
*   [<span data-ttu-id="e703e-161">Online- und Offlineereignisse</span><span class="sxs-lookup"><span data-stu-id="e703e-161">Online and Offline Events</span></span>][MDNNavigatoronlineOfflineEvents]  
*   [<span data-ttu-id="e703e-162">Anforderung mit Absicht: Zwischenspeichern von Strategien im Alter von PWAs</span><span class="sxs-lookup"><span data-stu-id="e703e-162">Request with Intent: Caching Strategies in the Age of PWAs</span></span>][AlistapartRequestIntentCachingStrategiesAgePwas]
    
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
