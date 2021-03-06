---
title: Verwalten von Netzwerkanforderungen und Pushbenachrichtigungen mithilfe von Service Workers
description: Service Workers sind Web Workers, die dazu beitragen, die Leistung zu verbessern, auf unterschiedliche Netzwerkbedingungen zu reagieren und die Konnektivität mit Ihrer Webanwendung zu erhöhen.
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/07/2021
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: pwa
keywords: progressive Web-Apps, PWA, Edge, JavaScript, Windows, UWP, Microsoft Store
ms.openlocfilehash: 314acbbd5a2f423c274f92e815b2be4329ace9b8
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "11399134"
---
# <a name="use-service-workers-to-manage-network-requests-and-push-notifications"></a><span data-ttu-id="c430a-104">Verwalten von Netzwerkanforderungen und Pushbenachrichtigungen mithilfe von Service Workers</span><span class="sxs-lookup"><span data-stu-id="c430a-104">Use Service Workers to manage network requests and push notifications</span></span>

<span data-ttu-id="c430a-105">Service Workers sind ein spezieller Typ von Web Worker mit der Möglichkeit, alle Netzwerkanforderungen mithilfe der API abzufangen, zu ändern und auf diese zu `Fetch` reagieren.</span><span class="sxs-lookup"><span data-stu-id="c430a-105">Service Workers are a special type of Web Worker with the ability to intercept, modify, and respond to all network requests using the `Fetch` API.</span></span>  <span data-ttu-id="c430a-106">Service Workers kann auf die API und asynchrone clientseitige Datenspeicher zugreifen, z. B. `Cache` , um Ressourcen zu `IndexedDB` speichern.</span><span class="sxs-lookup"><span data-stu-id="c430a-106">Service Workers can access the `Cache` API, and asynchronous client-side data stores, such as `IndexedDB`, to store resources.</span></span>  

## <a name="registering-a-service-worker"></a><span data-ttu-id="c430a-107">Registrieren eines Dienstmitarbeiters</span><span class="sxs-lookup"><span data-stu-id="c430a-107">Registering a Service Worker</span></span>  

<span data-ttu-id="c430a-108">Ähnlich wie andere Web Workers müssen Service Workers in einer separaten Datei vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="c430a-108">Similar to other Web Workers, Service Workers must exist in a separate file.</span></span> <span data-ttu-id="c430a-109">Sie verweisen bei der Registrierung des Service Worker auf diese Datei, wie im folgenden Codeausschnitt gezeigt.</span><span class="sxs-lookup"><span data-stu-id="c430a-109">You reference this file when registering the Service Worker, as shown in the following code snippet.</span></span>  

```javascript
if ( "serviceWorker" in navigator ) {
    navigator.serviceWorker.register( "/serviceworker.min.js" );
}
```  

<span data-ttu-id="c430a-110">Moderne Browser bieten unterschiedliche Unterstützungsebenen für Service Workers.</span><span class="sxs-lookup"><span data-stu-id="c430a-110">Modern browsers provide different levels of support for Service Workers.</span></span> <span data-ttu-id="c430a-111">Daher ist es eine bewährte Methode, das Vorhandensein des Objekts zu testen, bevor Sie service `serviceWorker` workerbezogenen Code ausführen.</span><span class="sxs-lookup"><span data-stu-id="c430a-111">As such, it is a good practice to test for the existence of the `serviceWorker` object before running any Service Worker-related code.</span></span> <span data-ttu-id="c430a-112">Im obigen Codeausschnitt wird ein Service Worker mithilfe der Datei registriert, die sich `serviceworker.min.js` im Stammverzeichnis der Website befindet.</span><span class="sxs-lookup"><span data-stu-id="c430a-112">In the above code snippet, a Service Worker is registered using the `serviceworker.min.js` file located at the root of the site.</span></span> <span data-ttu-id="c430a-113">Stellen Sie sicher, dass die JavaScript-Datei, die Ihren Dienstarbeitsmitarbeiter definiert, in dem Verzeichnis auf höchster Ebene vorhanden ist, das sie verwalten soll \(das als Bereich des Dienstarbeitsmitarbeiters\ bezeichnet wird).</span><span class="sxs-lookup"><span data-stu-id="c430a-113">Ensure that the JavaScript file that defines your Service Worker exists in the highest-level directory that you want it to manage \(which is referred to as the scope of the Service Worker\).</span></span>  <span data-ttu-id="c430a-114">Im vorherigen Codeausschnitt wird die Datei im Stammverzeichnis gespeichert, und der Service Worker verwaltet alle Seiten in der Domäne.</span><span class="sxs-lookup"><span data-stu-id="c430a-114">In the previous code snippet, the file is stored in the root, and the Service Worker manages all pages in the domain.</span></span> <span data-ttu-id="c430a-115">Wenn die Dienstarbeitsdatei in einem Verzeichnis gespeichert wurde, würde der Bereich des Dienstarbeitsmitarbeiters das Verzeichnis und `js` `js` alle Unterverzeichnisse sein.</span><span class="sxs-lookup"><span data-stu-id="c430a-115">If the Service Worker file was stored in a `js` directory, the scope of the Service Worker would be the `js` directory and any subdirectories.</span></span>  <span data-ttu-id="c430a-116">Als bewährte Methode sollten Sie die Dienstarbeitsdatei im Stammverzeichnis Ihrer Website platzieren, es sei denn, Sie müssen den Umfang Ihres Dienstmitarbeiters reduzieren.</span><span class="sxs-lookup"><span data-stu-id="c430a-116">As a best practice, place the Service Worker file in the root of your site, unless you need to reduce the scope of your Service Worker.</span></span>  

## <a name="the-service-worker-lifecycle"></a><span data-ttu-id="c430a-117">Der Service Worker-Lebenszyklus</span><span class="sxs-lookup"><span data-stu-id="c430a-117">The Service Worker lifecycle</span></span>  

<span data-ttu-id="c430a-118">Der Lebenszyklus eines Service Worker besteht aus mehreren Schritten, bei der jeder Schritt ein Ereignis auslöst.</span><span class="sxs-lookup"><span data-stu-id="c430a-118">The lifecycle of a Service Worker consists of multiple steps, with each step triggering an event.</span></span> <span data-ttu-id="c430a-119">Sie können diesen Ereignissen Listener hinzufügen, um Code zum Ausführen einer Aktion ausführen zu können.</span><span class="sxs-lookup"><span data-stu-id="c430a-119">You can add listeners to these events to run code to perform an action.</span></span> <span data-ttu-id="c430a-120">Die folgende Liste enthält eine übersichtsbezogene Ansicht des Lebenszyklus und der zugehörigen Ereignisse von Servicemitarbeitern.</span><span class="sxs-lookup"><span data-stu-id="c430a-120">The following list presents a high-level view of the lifecycle and related events of service workers.</span></span> 

1.  <span data-ttu-id="c430a-121">Registrieren Sie den Service Worker.</span><span class="sxs-lookup"><span data-stu-id="c430a-121">Register the Service Worker.</span></span>  
1.  <span data-ttu-id="c430a-122">Der Browser lädt die JavaScript-Datei herunter, installiert den Service Worker und löst das Ereignis `install` aus.</span><span class="sxs-lookup"><span data-stu-id="c430a-122">The browser downloads the JavaScript file, installs the Service Worker, and triggers the `install` event.</span></span> <span data-ttu-id="c430a-123">Sie können das Ereignis verwenden, um wichtige und langlebige Dateien wie `install` CSS-Dateien, JavaScript-Dateien, Logobilder, Offlineseiten und so weiter von Ihrer Website vorab zwischenspeichern.</span><span class="sxs-lookup"><span data-stu-id="c430a-123">You can use the `install` event to pre-cache any important and long-lived files, such as CSS files, JavaScript files, logo images, offline pages, and so on from your website.</span></span>  
    
    ```javascript
    self.addEventListener( "install", function( event ){
        console.log( "WORKER: install event in progress." );
    });
    ```  
    
1.  <span data-ttu-id="c430a-124">Der Dienstmitarbeiter wird aktiviert, wodurch das Ereignis ausgelöst `activate` wird.</span><span class="sxs-lookup"><span data-stu-id="c430a-124">The Service Worker is activated, which triggers the `activate` event.</span></span>  <span data-ttu-id="c430a-125">Verwenden Sie dieses Ereignis, um veraltete Caches zu bereinigen.</span><span class="sxs-lookup"><span data-stu-id="c430a-125">Use this event to clean up outdated caches.</span></span>  
    
    ```javascript
    self.addEventListener( "activate", event => {
        console.log('WORKER: activate event in progress.');
    });
    ```  
    
1.  <span data-ttu-id="c430a-126">Der Dienstmitarbeiter kann ausgeführt werden, wenn die Seite aktualisiert wird oder wenn der Benutzer zu einer neuen Seite auf der Website navigiert.</span><span class="sxs-lookup"><span data-stu-id="c430a-126">The Service Worker is ready to run when the page is refreshed or when the user navigates to a new page on the site.</span></span> <span data-ttu-id="c430a-127">Wenn Sie den Service Worker ohne Wartezeit ausführen möchten, verwenden Sie die `self.skipWaiting()` -Methode während des `install` Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="c430a-127">If you want to run the Service Worker without waiting, use the `self.skipWaiting()` method during the `install` event.</span></span>  
    
    ```javascript
    self.addEventListener( "install", event => {
        self.skipWaiting();
        // …
    });
    ```
    
1.  <span data-ttu-id="c430a-128">Der Dienstmitarbeiter wird jetzt ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c430a-128">The Service Worker is now running.</span></span>     
    
## <a name="using-fetch-in-service-workers"></a><span data-ttu-id="c430a-129">Verwenden des Abrufs in Service Workers</span><span class="sxs-lookup"><span data-stu-id="c430a-129">Using fetch in Service Workers</span></span>  

<span data-ttu-id="c430a-130">Das Hauptereignis, das Sie in einem Service Worker verwenden, ist das `fetch` Ereignis.</span><span class="sxs-lookup"><span data-stu-id="c430a-130">The main event that you use in a Service Worker is the `fetch` event.</span></span>  <span data-ttu-id="c430a-131">Das Ereignis wird jedes Mal ausgeführt, wenn der Browser versucht, auf `fetch` Inhalte im Bereich des Service Workers zu zugreifen.</span><span class="sxs-lookup"><span data-stu-id="c430a-131">The `fetch` event runs every time the browser attempts to access content within the scope of the Service Worker.</span></span> <span data-ttu-id="c430a-132">Der folgende Codeausschnitt zeigt, wie Sie dem Fetch-Ereignis einen Listener hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="c430a-132">The following code snippet shows how to add a listener to the fetch event.</span></span>  

```javascript
self.addEventListener( "fetch", event => {
  console.log('WORKER: Fetching', event.request);
});
```  

<span data-ttu-id="c430a-133">Innerhalb des Handlers können Sie steuern, ob eine Anforderung an das Netzwerk geht, aus dem Cache zurückgeht `fetch` und so weiter.</span><span class="sxs-lookup"><span data-stu-id="c430a-133">Within the `fetch` handler, you may control whether a request goes to the network, pulls from the cache, and so on.</span></span>  <span data-ttu-id="c430a-134">Der von Ihnen verwendete Ansatz variiert je nach Art der angeforderten Ressource, der Anzahl der Aktualisierungen und der anderen geschäftsbezogenen Logik, die für Ihre Anwendung eindeutig ist.</span><span class="sxs-lookup"><span data-stu-id="c430a-134">The approach you take likely varies based upon the type of resource being requested, how frequently it is updated, and other business logic unique to your application.</span></span>  <span data-ttu-id="c430a-135">Im Folgenden finden Sie einige Beispiele dafür, was Sie tun können:</span><span class="sxs-lookup"><span data-stu-id="c430a-135">Here are a few examples of what you may do:</span></span>  

*   <span data-ttu-id="c430a-136">Wenn verfügbar, geben Sie eine Antwort aus dem Cache zurück, andernfalls fallback, um die Ressource über das Netzwerk an anforderung.</span><span class="sxs-lookup"><span data-stu-id="c430a-136">If available, return a response from the cache, otherwise fallback to request the resource over the network.</span></span>  
*   <span data-ttu-id="c430a-137">Rufen Sie eine Ressource aus dem Netzwerk ab, speichern Sie eine Kopie zwischen, und geben Sie die Antwort zurück.</span><span class="sxs-lookup"><span data-stu-id="c430a-137">Fetch a resource from the network, cache a copy, and return the response.</span></span>
*   <span data-ttu-id="c430a-138">Zulassen, dass Benutzer eine Einstellung zum Speichern von Daten angeben.</span><span class="sxs-lookup"><span data-stu-id="c430a-138">Allow user's to specify a preference to save data.</span></span> 
*   <span data-ttu-id="c430a-139">Geben Sie ein Platzhalterbild für bestimmte Bildanforderungen an.</span><span class="sxs-lookup"><span data-stu-id="c430a-139">Supply a placeholder image for certain image requests.</span></span>  
*   <span data-ttu-id="c430a-140">Generieren Sie eine Antwort direkt im Service Worker.</span><span class="sxs-lookup"><span data-stu-id="c430a-140">Generate a response directly in the Service Worker.</span></span>  
    
## <a name="push-notifications"></a><span data-ttu-id="c430a-141">Pushbenachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="c430a-141">Push Notifications</span></span>  

<span data-ttu-id="c430a-142">Servicemitarbeiter können Benachrichtigungen per Push an Benutzer senden.</span><span class="sxs-lookup"><span data-stu-id="c430a-142">Service workers can push notifications to users.</span></span> <span data-ttu-id="c430a-143">Pushbenachrichtigungen sind hilfreich, um Benutzer zum erneuten Interagieren mit Ihrer Anwendung nach einiger Zeit aufforderen.</span><span class="sxs-lookup"><span data-stu-id="c430a-143">Push Notifications are helpful to prompt users to re-engage with your application after some time has elapsed.</span></span> <span data-ttu-id="c430a-144">Weitere Informationen finden Sie unter Exemplarische Vorgehensweise und Demo zu [Pushbenachrichtigungen.][AzurewebsitesWebpushdemo]</span><span class="sxs-lookup"><span data-stu-id="c430a-144">For more information, navigate to [Push Notifications walkthrough and demo][AzurewebsitesWebpushdemo].</span></span>  

## <a name="see-also"></a><span data-ttu-id="c430a-145">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="c430a-145">See also</span></span>  

<span data-ttu-id="c430a-146">Weitere Informationen zu Service Workers finden Sie in der folgenden Liste verwandter Themen.</span><span class="sxs-lookup"><span data-stu-id="c430a-146">To learn more about Service Workers, navigate to the following list of related topics.</span></span>  

*   [<span data-ttu-id="c430a-147">Offlinebetrieb von PWAs mit Servicemitarbeitern</span><span class="sxs-lookup"><span data-stu-id="c430a-147">Making PWAs work offline with Service workers</span></span>][MDNPwasMakingOfflineServiceWorkers]  
*   [<span data-ttu-id="c430a-148">So können Sie PWAs mithilfe von Benachrichtigungen und Push wieder aktivieren</span><span class="sxs-lookup"><span data-stu-id="c430a-148">How to make PWAs re-engageable using Notifications and Push</span></span>][MDNPwasMakeReengageablesingNotificationsPush]  
    
<!-- links -->  

[AzurewebsitesWebpushdemo]: https://webpushdemo.azurewebsites.net "Web-Pushbenachrichtigungen |  Microsoft Edge Demos"  

[MDNPwasMakingOfflineServiceWorkers]: https://developer.mozilla.org/docs/Web/Progressive_web_apps/Offline_Service_workers "Offlinebetrieb von PWAs mit Servicemitarbeitern – PWAs | MDN"  
[MDNPwasMakeReengageablesingNotificationsPush]: https://developer.mozilla.org/docs/Web/Progressive_web_apps/Re-engageable_Notifications_Push "So können Sie PWAs mithilfe von Benachrichtigungen und Push wieder aktivieren – PWAs | MDN"  
