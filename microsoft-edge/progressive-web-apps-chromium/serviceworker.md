---
title: Verwenden von Service Mitarbeitern zum Verwalten von Netzwerkanforderungen und Push-Benachrichtigungen
description: Dienstmitarbeiter sind webarbeiter, die dazu beitragen, die Leistung zu verbessern, auf unterschiedliche Netzwerkbedingungen zu reagieren und die Konnektivität mit Ihrer Web-Anwendung zu erhöhen.
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/15/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: pwa
keywords: Progressive Web-Apps, PWA, Edge, JavaScript, Windows, UWP, Microsoft Store
ms.openlocfilehash: 9bf573b668ade351716b69965f653e05857c32ec
ms.sourcegitcommit: d9cc829deb709b0866f6b43a5f4733682ddae5ca
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/16/2020
ms.locfileid: "10659300"
---
# <span data-ttu-id="988b8-104">Verwenden von Service Mitarbeitern zum Verwalten von Netzwerkanforderungen und Push-Benachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="988b8-104">Use Service Workers to manage network requests and push notifications</span></span>

<span data-ttu-id="988b8-105">Dienstmitarbeiter sind eine spezielle Art von Web-Worker mit der Möglichkeit, mithilfe der API alle Netzwerkanforderungen abzufangen, zu ändern und auf Sie zu reagieren `Fetch` .</span><span class="sxs-lookup"><span data-stu-id="988b8-105">Service Workers are a special type of Web Worker with the ability to intercept, modify, and respond to all network requests using the `Fetch` API.</span></span>  <span data-ttu-id="988b8-106">Dienstmitarbeiter können auf die `Cache` API und asynchrone clientseitige Datenspeicher zugreifen, beispielsweise `IndexedDB` zum Speichern von Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="988b8-106">Service Workers can access the `Cache` API, and asynchronous client-side data stores, such as `IndexedDB`, to store resources.</span></span>  

## <span data-ttu-id="988b8-107">Registrieren eines Dienst Mitarbeiters</span><span class="sxs-lookup"><span data-stu-id="988b8-107">Registering a Service Worker</span></span>  

<span data-ttu-id="988b8-108">Ähnlich wie andere Web-Worker müssen Service Mitarbeiter in einer separaten Datei vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="988b8-108">Similar to other Web Workers, Service Workers must exist in a separate file.</span></span> <span data-ttu-id="988b8-109">Sie verweisen auf diese Datei, wenn Sie den Dienstmitarbeiter registrieren, wie im folgenden Codeausschnitt dargestellt.</span><span class="sxs-lookup"><span data-stu-id="988b8-109">You reference this file when registering the Service Worker, as shown in the following code snippet.</span></span>  

```javascript
if ( "serviceWorker" in navigator ) {
    navigator.serviceWorker.register( "/serviceworker.min.js" );
}
```  

<span data-ttu-id="988b8-110">Moderne Browser bieten unterschiedliche Supportstufen für Dienstmitarbeiter.</span><span class="sxs-lookup"><span data-stu-id="988b8-110">Modern browsers provide different levels of support for Service Workers.</span></span> <span data-ttu-id="988b8-111">Daher empfiehlt es sich, das vorhanden sein des Objekts zu testen, bevor ein `serviceWorker` Dienstmitarbeiter bezogener Code ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="988b8-111">As such, it is a good practice to test for the existence of the `serviceWorker` object before running any Service Worker-related code.</span></span> <span data-ttu-id="988b8-112">Im obigen Codeausschnitt wird ein Dienstmitarbeiter mit der Datei registriert, die sich im `serviceworker.min.js` Stammverzeichnis der Website befindet.</span><span class="sxs-lookup"><span data-stu-id="988b8-112">In the above code snippet, a Service Worker is registered using the `serviceworker.min.js` file located at the root of the site.</span></span> <span data-ttu-id="988b8-113">Stellen Sie sicher, dass die JavaScript-Datei, die ihren Dienstmitarbeiter definiert, im Verzeichnis der obersten Ebene vorhanden ist, das verwaltet werden soll \ (das als Bereich der Dienstmitarbeiter bezeichnet wird).</span><span class="sxs-lookup"><span data-stu-id="988b8-113">Ensure that the JavaScript file that defines your Service Worker exists in the highest-level directory that you want it to manage \(which is referred to as the scope of the Service Worker\).</span></span>  <span data-ttu-id="988b8-114">Im obigen Codeausschnitt wird die Datei im Stammverzeichnis gespeichert, und der Dienstmitarbeiter verwaltet alle Seiten in der Domäne.</span><span class="sxs-lookup"><span data-stu-id="988b8-114">In the above code snippet, the file is stored in the root, and the Service Worker manages all pages in the domain.</span></span> <span data-ttu-id="988b8-115">Wenn die Dienst Arbeitskraft Datei in einem Verzeichnis gespeichert wurde `js` , würde der Bereich des Dienst Arbeitsthreads das `js` Verzeichnis und alle Unterverzeichnisse sein.</span><span class="sxs-lookup"><span data-stu-id="988b8-115">If the Service Worker file was stored in a `js` directory, the scope of the Service Worker would be the `js` directory and any subdirectories.</span></span>  <span data-ttu-id="988b8-116">Als bewährte Methode sollten Sie die Service Worker-Datei im Stammverzeichnis Ihrer Website platzieren, es sei denn, Sie müssen den Umfang ihrer Dienstmitarbeiter reduzieren.</span><span class="sxs-lookup"><span data-stu-id="988b8-116">As a best practice, place the Service Worker file in the root of your site, unless you need to reduce the scope of your Service Worker.</span></span>  

## <span data-ttu-id="988b8-117">Der Service Worker-Lebenszyklus</span><span class="sxs-lookup"><span data-stu-id="988b8-117">The Service Worker lifecycle</span></span>  

<span data-ttu-id="988b8-118">Der Lebenszyklus eines Dienstmitarbeiter besteht aus mehreren Schritten, wobei jeder Schritt ein Ereignis auslöst.</span><span class="sxs-lookup"><span data-stu-id="988b8-118">The lifecycle of a Service Worker consists of multiple steps, with each step triggering an event.</span></span> <span data-ttu-id="988b8-119">Sie können diesen Ereignissen Listener hinzufügen, um Code auszuführen, um eine Aktion auszuführen.</span><span class="sxs-lookup"><span data-stu-id="988b8-119">You can add listeners to these events to run code to perform an action.</span></span> <span data-ttu-id="988b8-120">Die folgende Liste enthält eine allgemeine Übersicht über den Lebenszyklus und verwandte Ereignisse von Servicemitarbeitern.</span><span class="sxs-lookup"><span data-stu-id="988b8-120">The following list presents a high-level view of the lifecycle and related events of service workers.</span></span> 

1. <span data-ttu-id="988b8-121">Registrieren Sie den Dienstmitarbeiter.</span><span class="sxs-lookup"><span data-stu-id="988b8-121">Register the Service Worker.</span></span>  
1.  <span data-ttu-id="988b8-122">Der Browser lädt die JavaScript-Datei herunter, installiert den Dienstmitarbeiter und löst das `install` Ereignis aus.</span><span class="sxs-lookup"><span data-stu-id="988b8-122">The browser downloads the JavaScript file, installs the Service Worker, and triggers the `install` event.</span></span> <span data-ttu-id="988b8-123">Sie können das `install` Ereignis verwenden, um wichtige und langlebige Dateien, wie etwa CSS-Dateien, JavaScript-Dateien, Logo Bilder, Offlineseiten usw., auf Ihrer Website vorab zwischenzuspeichern.</span><span class="sxs-lookup"><span data-stu-id="988b8-123">You can use the `install` event to pre-cache any important and long-lived files, such as CSS files, JavaScript files, logo images, offline pages, and so on from your website.</span></span>  
    
    ```javascript
    self.addEventListener( "install", function( event ){
        console.log( "WORKER: install event in progress." );
    });
    ```  
    
1.  <span data-ttu-id="988b8-124">Der Dienstmitarbeiter wird aktiviert, wodurch das Ereignis ausgelöst wird `activate` .</span><span class="sxs-lookup"><span data-stu-id="988b8-124">The Service Worker is activated, which triggers the `activate` event.</span></span>  <span data-ttu-id="988b8-125">Verwenden Sie dieses Ereignis, um veraltete Caches zu bereinigen.</span><span class="sxs-lookup"><span data-stu-id="988b8-125">Use this event to clean up outdated caches.</span></span>  
    
    ```javascript
    self.addEventListener( "activate", event => {
        console.log('WORKER: activate event in progress.');
    });
    ```  
    
1.  <span data-ttu-id="988b8-126">Der Dienstmitarbeiter kann ausgeführt werden, wenn die Seite aktualisiert wird, oder wenn der Benutzer zu einer neuen Seite auf der Website navigiert.</span><span class="sxs-lookup"><span data-stu-id="988b8-126">The Service Worker is ready to run when the page is refreshed or when the user navigates to a new page on the site.</span></span> <span data-ttu-id="988b8-127">Wenn Sie den Dienstmitarbeiter ohne Wartezeit ausführen möchten, verwenden Sie die `self.skipWaiting()` Methode während des `install` Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="988b8-127">If you want to run the Service Worker without waiting, use the `self.skipWaiting()` method during the `install` event.</span></span>  
    
    ```javascript
    self.addEventListener( "install", event => {
        self.skipWaiting();
        // …
    });
    ```
    
1.  <span data-ttu-id="988b8-128">Der Dienstmitarbeiter wird nun ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="988b8-128">The Service Worker is now running.</span></span>     
    
## <span data-ttu-id="988b8-129">Verwenden von FETCH in Service Mitarbeitern</span><span class="sxs-lookup"><span data-stu-id="988b8-129">Using fetch in Service Workers</span></span>  

<span data-ttu-id="988b8-130">Das Hauptereignis, das Sie in einem Dienstmitarbeiter verwenden, ist das `fetch` Ereignis.</span><span class="sxs-lookup"><span data-stu-id="988b8-130">The main event that you use in a Service Worker is the `fetch` event.</span></span>  <span data-ttu-id="988b8-131">Das `fetch` Ereignis wird jedes Mal ausgeführt, wenn der Browser versucht, auf Inhalte im Bereich der Dienstmitarbeiter zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="988b8-131">The `fetch` event runs every time the browser attempts to access content within the scope of the Service Worker.</span></span> <span data-ttu-id="988b8-132">Der folgende Codeausschnitt zeigt, wie dem FETCH-Ereignis ein Listener hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="988b8-132">The following code snippet shows how to add a listener to the fetch event.</span></span>  

```javascript
self.addEventListener( "fetch", event => {
  console.log('WORKER: Fetching', event.request);
});
```  

<span data-ttu-id="988b8-133">Innerhalb des `fetch` Handlers können Sie steuern, ob eine Anforderung an das Netzwerk wechselt, aus dem Cache abgerufen wird usw.</span><span class="sxs-lookup"><span data-stu-id="988b8-133">Within the `fetch` handler, you may control whether a request goes to the network, pulls from the cache, and so on.</span></span>  <span data-ttu-id="988b8-134">Der von Ihnen verwendete Ansatz variiert je nach Art der angeforderten Ressource, wie häufig Sie aktualisiert wird, und der anderen Geschäftslogik, die für Ihre Anwendung eindeutig ist.</span><span class="sxs-lookup"><span data-stu-id="988b8-134">The approach you take likely varies based upon the type of resource being requested, how frequently it is updated, and other business logic unique to your application.</span></span>  <span data-ttu-id="988b8-135">Hier sind einige Beispiele dafür, was Sie tun können:</span><span class="sxs-lookup"><span data-stu-id="988b8-135">Here are a few examples of what you may do:</span></span>  

*   <span data-ttu-id="988b8-136">Falls verfügbar, geben Sie eine Antwort aus dem Cache zurück, andernfalls Fallback, um die Ressource über das Netzwerk anzufordern.</span><span class="sxs-lookup"><span data-stu-id="988b8-136">If available, return a response from the cache, otherwise fallback to request the resource over the network.</span></span>  
*   <span data-ttu-id="988b8-137">Abrufen einer Ressource aus dem Netzwerk, Zwischenspeichern einer Kopie und Zurückgeben der Antwort.</span><span class="sxs-lookup"><span data-stu-id="988b8-137">Fetch a resource from the network, cache a copy, and return the response.</span></span>
*   <span data-ttu-id="988b8-138">Zulassen, dass Benutzer eine Einstellung zum Speichern von Daten angeben.</span><span class="sxs-lookup"><span data-stu-id="988b8-138">Allow user's to specify a preference to save data.</span></span> 
*   <span data-ttu-id="988b8-139">Stellen Sie für bestimmte Bildanforderungen ein Platzhalterbild zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="988b8-139">Supply a placeholder image for certain image requests.</span></span>  
*   <span data-ttu-id="988b8-140">Direktes Generieren einer Antwort im Dienstmitarbeiter.</span><span class="sxs-lookup"><span data-stu-id="988b8-140">Generate a response directly in the Service Worker.</span></span>  

## <span data-ttu-id="988b8-141">Pushbenachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="988b8-141">Push Notifications</span></span>  

<span data-ttu-id="988b8-142">Dienstmitarbeiter können Benachrichtigungen an Benutzer senden.</span><span class="sxs-lookup"><span data-stu-id="988b8-142">Service workers can push notifications to users.</span></span> <span data-ttu-id="988b8-143">Push-Benachrichtigungen sind hilfreich, wenn Benutzer aufgefordert werden sollen, Ihre Anwendung nach Ablauf einiger Zeit erneut zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="988b8-143">Push Notifications are helpful to prompt users to re-engage with your application after some time has elapsed.</span></span> <span data-ttu-id="988b8-144">Weitere Informationen finden Sie unter [Exemplarische Vorgehensweise und Demo zu Push-Benachrichtigungen][AzurewebsitesWebpushdemo].</span><span class="sxs-lookup"><span data-stu-id="988b8-144">For more information, see [Push Notifications walkthrough and demo][AzurewebsitesWebpushdemo].</span></span>  

## <span data-ttu-id="988b8-145">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="988b8-145">See also</span></span>  

<span data-ttu-id="988b8-146">Weitere Informationen zu Service Mitarbeitern finden Sie in der folgenden Liste verwandter Themen.</span><span class="sxs-lookup"><span data-stu-id="988b8-146">To learn more about Service Workers, see the following list of related topics.</span></span>  

*   [<span data-ttu-id="988b8-147">Offline Arbeiten von PWAs mit Service Mitarbeitern</span><span class="sxs-lookup"><span data-stu-id="988b8-147">Making PWAs work offline with Service workers</span></span>][MDNPwasMakingOfflineServiceWorkers]  
*   [<span data-ttu-id="988b8-148">So aktivieren Sie PWAs mit Benachrichtigungen und Push</span><span class="sxs-lookup"><span data-stu-id="988b8-148">How to make PWAs re-engageable using Notifications and Push</span></span>][MDNPwasMakeReengageablesingNotificationsPush]  

<!-- links -->  

[AzurewebsitesWebpushdemo]: https://webpushdemo.azurewebsites.net "Web-Push-Benachrichtigungen |  Microsoft Edge-Demos"  

[MDNPwasMakingOfflineServiceWorkers]: https://developer.mozilla.org/docs/Web/Progressive_web_apps/Offline_Service_workers "Offline Arbeiten von PWAs mit Service Mitarbeitern – PWAs | MDN"  
[MDNPwasMakeReengageablesingNotificationsPush]: https://developer.mozilla.org/docs/Web/Progressive_web_apps/Re-engageable_Notifications_Push "So aktivieren Sie PWAs mit Benachrichtigungen und Push-PWAs | MDN"  
