---
description: Verwenden Sie den Anwendungs Panel, um Web App-Manifeste, Dienstmitarbeiter und Service Worker-Caches zu prüfen, zu ändern und zu debuggen.
title: Debuggen von progressiven Web-Apps
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: 7eb71d0d57d8a9227a54b921f15dfe434ad6e65b
ms.sourcegitcommit: 63e6d34ff483f3b419a0e271a3513874e6ce6c79
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/02/2020
ms.locfileid: "10993604"
---
<!-- Copyright Kayce Basques 

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->  





# <span data-ttu-id="f7ee5-104">Debuggen von progressiven Web-Apps</span><span class="sxs-lookup"><span data-stu-id="f7ee5-104">Debug Progressive Web Apps</span></span>   



<span data-ttu-id="f7ee5-105">Verwenden Sie den **Anwendungs** Panel, um Web App-Manifeste, Dienstmitarbeiter und Service Worker-Caches zu prüfen, zu ändern und zu debuggen.</span><span class="sxs-lookup"><span data-stu-id="f7ee5-105">Use the **Application** panel to inspect, modify, and debug web app manifests, service workers, and service worker caches.</span></span>  

<!--Related Guides:  

*   [Progressive Web Apps](/web/progressive-web-apps)  -->

<!--TODO:  Link web "Progressive Web Apps" section when available. -->

<span data-ttu-id="f7ee5-106">In diesem Leitfaden werden nur die fortschrittlichen Web App-Features des **Anwendungs** Panels erläutert.</span><span class="sxs-lookup"><span data-stu-id="f7ee5-106">This guide only discusses the Progressive Web App features of the **Application** panel.</span></span>  <!--If you're looking for help on the other panes, check out the last section of this guide, [Other Application panel guides](#other-application-panel-guides).  -->

<!--TODO:  Link to sections when available. -->

### <span data-ttu-id="f7ee5-107">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="f7ee5-107">Summary</span></span>  

*   <span data-ttu-id="f7ee5-108">Verwenden Sie den Bereich **Manifest** , um das Web App-Manifest zu überprüfen und auf Homescreen-Ereignisse hinzufügen zu starten.</span><span class="sxs-lookup"><span data-stu-id="f7ee5-108">Use the **Manifest** pane to inspect your web app manifest and trigger Add to Homescreen events.</span></span>  
*   <span data-ttu-id="f7ee5-109">Verwenden Sie den Bereich " **Dienstmitarbeiter** " für eine ganze Reihe von Dienstmitarbeiter bezogenen Aufgaben, wie das Aufheben der Registrierung oder Aktualisierung eines Diensts, das Emulieren von Push-Ereignissen, das offline schalten oder Beenden eines Dienst Mitarbeiters.</span><span class="sxs-lookup"><span data-stu-id="f7ee5-109">Use the **Service Workers** pane for a whole range of service-worker-related tasks, like unregistering or updating a service, emulating push events, going offline, or stopping a service worker.</span></span>  
*   <span data-ttu-id="f7ee5-110">Zeigen Sie den Service Worker-Cache im **Cachespeicher** Bereich an.</span><span class="sxs-lookup"><span data-stu-id="f7ee5-110">View your service worker cache from the **Cache Storage** pane.</span></span>  
*   <span data-ttu-id="f7ee5-111">Heben Sie die Registrierung eines Dienstmitarbeiter auf, und löschen Sie alle Speicher und Caches mit einem einzigen Mausklick aus dem Bereich " **Speicher löschen** ".</span><span class="sxs-lookup"><span data-stu-id="f7ee5-111">Unregister a service worker and clear all storage and caches with a single button click from the **Clear storage** pane.</span></span>  
    
## <span data-ttu-id="f7ee5-112">Web App-Manifest</span><span class="sxs-lookup"><span data-stu-id="f7ee5-112">Web app manifest</span></span>   

<span data-ttu-id="f7ee5-113">Wenn Sie möchten, dass Ihre Benutzer Ihre APP ihren mobilen Homescreens hinzufügen können, benötigen Sie ein Web App-Manifest.</span><span class="sxs-lookup"><span data-stu-id="f7ee5-113">If you want your users to be able to add your app to their mobile homescreens, you need a web app manifest.</span></span>  <span data-ttu-id="f7ee5-114">Das Manifest definiert, wie die APP auf dem Homescreen angezeigt wird, wo der Benutzer beim Start von Homescreen weitergeleitet wird und wie die APP beim Start aussieht.</span><span class="sxs-lookup"><span data-stu-id="f7ee5-114">The manifest defines how the app appears on the homescreen, where to direct the user when launching from homescreen, and what the app looks like on launch.</span></span>  

<!--Related Guides:  

*   [Improve user experiences with a Web App Manifest](/web/fundamentals/web-app-manifest)  
*   [Using App Install Banners](/web/fundamentals/app-install-banners)  -->

<!--TODO:  Link to sections when available. -->

<span data-ttu-id="f7ee5-115">Nachdem Sie Ihr Manifest eingerichtet haben, können Sie es über den Bereich **Manifest** des **Anwendungs** Bereichs überprüfen.</span><span class="sxs-lookup"><span data-stu-id="f7ee5-115">After you have your manifest set up, you can use the **Manifest** pane of the **Application** panel to inspect it.</span></span>  

:::image type="complex" source="./media/manifest-pane.msft.png" alt-text="Bereich ' Manifest '" lightbox="./media/manifest-pane.msft.png":::
   <span data-ttu-id="f7ee5-117">Bereich ' **Manifest** '</span><span class="sxs-lookup"><span data-stu-id="f7ee5-117">The **Manifest** Pane</span></span>  
:::image-end:::  

*   <span data-ttu-id="f7ee5-118">Wenn Sie sich die Manifest-Quelle ansehen möchten, klicken Sie auf den Link unter **App-Manifest** -Beschriftung \ ( `https://airhorner.com/manifest.json` in der vorhergehenden Abbildung).</span><span class="sxs-lookup"><span data-stu-id="f7ee5-118">To look at the manifest source, click the link below **App Manifest** label \(`https://airhorner.com/manifest.json` in the previous figure\).</span></span>  
<!-- *   Press the **Add to homescreen** button to simulate an Add to Homescreen event.  Check out the next section for more information.  -->  
*   <span data-ttu-id="f7ee5-119">In den Abschnitten **Identität** und **Präsentation** werden nur Felder aus der Manifestdatei in einer benutzerfreundlicheren Anzeige angezeigt.</span><span class="sxs-lookup"><span data-stu-id="f7ee5-119">The **Identity** and **Presentation** sections just display fields from the manifest source in a more user-friendly display.</span></span>  
*   <span data-ttu-id="f7ee5-120">Im Abschnitt "Symbole" werden alle von Ihnen angegebenen **Symbole** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="f7ee5-120">The **Icons** section displays every icon that you've specified.</span></span>  
    
<!--### Simulate Add to Homescreen events   -->

<!--A web app can only be added to a homescreen when the site is visited at least twice, with at least five minutes between visits.  While developing or debugging your Add to Homescreen workflow, this criteria can be inconvenient.  
The **Add to homescreen** button on the **App Manifest** pane lets you simulate Add to Homescreen events whenever you want.  -->

<!--You can test out this feature with the [Microsoft I/O 2016 progressive web app](https://events.alpahabet.com/io2016/), which has proper support for Add to Homescreen.  Clicking on **Add to Homescreen** while the app is open prompts Microsoft Edge to display the "add this site to your shelf" banner, which is the desktop equivalent of the "add to homescreen" banner for mobile devices.  -->

<!--  
:::image type="complex" source="./media/io.msft.png" alt-text="Bereich ' Manifest '" lightbox="./media/io.msft.png":::
   Add to desktop shelf  
:::image-end:::
-->  

<!--
> [!Tip]
> Keep the **Console** drawer open while simulating Add to Homescreen events.  The Console tells you if your manifest has any issues and logs other information about the Add to Homescreen lifecycle.  -->

<!--The **Add to Homescreen** feature cannot yet simulate the workflow for mobile devices.  Notice how the "add to shelf" prompt was triggered in the screenshot above, even though DevTools is in Device Mode.  However, if you can successfully add your app to your desktop shelf, then it'll work for mobile, too.  -->

<!-- TODO: Rework content after sample app is created. -->

<!--If you want to test out the genuine mobile experience, you can connect a real mobile device to DevTools via **remote debugging**, and then click the **Add to Homescreen** button \(on DevTools\) to trigger the "add to homescreen" prompt on the connected mobile device.  -->

<!--TODO:  Link Debug "remote debugging" sections when available. -->

## <span data-ttu-id="f7ee5-121">Dienstmitarbeiter</span><span class="sxs-lookup"><span data-stu-id="f7ee5-121">Service workers</span></span>   

<span data-ttu-id="f7ee5-122">Service Mitarbeiter sind eine grundlegende Technologie in der zukünftigen Web-Plattform.</span><span class="sxs-lookup"><span data-stu-id="f7ee5-122">Service workers are a fundamental technology in the future web platform.</span></span>  <span data-ttu-id="f7ee5-123">Dabei handelt es sich um Skripts, die der Browser im Hintergrund ausführt, und zwar unabhängig von einer Webseite.</span><span class="sxs-lookup"><span data-stu-id="f7ee5-123">They are scripts that the browser runs in the background, separate from a web page.</span></span>  <span data-ttu-id="f7ee5-124">Diese Skripts ermöglichen Ihnen den Zugriff auf Features, die keine Webseite oder Benutzerinteraktion benötigen, wie Push-Benachrichtigungen, Hintergrundsynchronisierung und Offline-Erlebnisse.</span><span class="sxs-lookup"><span data-stu-id="f7ee5-124">These scripts enable you to access features that don't need a web page or user interaction, like push notifications, background sync, and offline experiences.</span></span>  

<!--Related Guides:  

*   [Intro to Service Workers](/web/fundamentals/primers/service-worker)  
*   [Push Notifications: Timely, Relevant, and Precise](/web/fundamentals/push-notifications)  -->  
    
<!--TODO:  Link to sections when available. -->  

<span data-ttu-id="f7ee5-125">Der Bereich " **Dienstmitarbeiter** " im Bereich " **Anwendung** " ist der wichtigste Ort in devtools zum Überprüfen und Debuggen von Dienst Mitarbeitern.</span><span class="sxs-lookup"><span data-stu-id="f7ee5-125">The **Service Workers** pane in the **Application** panel is the main place in DevTools to inspect and debug service workers.</span></span>  

:::image type="complex" source="./media/service-workers-pane.msft.png" alt-text="Bereich ' Manifest '" lightbox="./media/service-workers-pane.msft.png":::
   <span data-ttu-id="f7ee5-127">Der Bereich " **Dienstmitarbeiter** "</span><span class="sxs-lookup"><span data-stu-id="f7ee5-127">The **Service Workers** pane</span></span>  
:::image-end:::  

*   <span data-ttu-id="f7ee5-128">Wenn ein Dienstmitarbeiter auf der aktuell geöffneten Seite installiert ist, wird er in diesem Bereich aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="f7ee5-128">If a service worker is installed to the currently open page, then you'll see it listed on this pane.</span></span>  <span data-ttu-id="f7ee5-129">In der vorherigen Abbildung ist beispielsweise ein Dienstmitarbeiter für den Bereich von installiert `https://weather-pwa-sample.firebaseapp.com` .</span><span class="sxs-lookup"><span data-stu-id="f7ee5-129">For example, in the previous figure, there is a service worker installed for the scope of `https://weather-pwa-sample.firebaseapp.com`.</span></span>  
*   <span data-ttu-id="f7ee5-130">Mit dem Kontrollkästchen **Offline** wird devtools in den Offlinemodus versetzt.</span><span class="sxs-lookup"><span data-stu-id="f7ee5-130">The **Offline** checkbox puts DevTools into offline mode.</span></span>  <span data-ttu-id="f7ee5-131">Dies entspricht dem Offlinemodus, der über das **Netzwerk** Panel zur Verfügung steht, oder die `Go offline` Option im [Menübefehl][DevtoolsCommandMenuIndex].</span><span class="sxs-lookup"><span data-stu-id="f7ee5-131">This is equivalent to the offline mode available from the **Network** panel, or the `Go offline` option in the [Command Menu][DevtoolsCommandMenuIndex].</span></span>  
*   <span data-ttu-id="f7ee5-132">Das Kontrollkästchen " **beim erneuten Laden aktualisieren** " zwingt den Dienstmitarbeiter, bei jeder Seitenauslastung zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="f7ee5-132">The **Update on reload** checkbox forces the service worker to update on every page load.</span></span>  
*   <span data-ttu-id="f7ee5-133">Das Kontrollkästchen " **für Netzwerk umgehen** " umgeht den Dienstmitarbeiter und zwingt den Browser, für angeforderte Ressourcen zum Netzwerk zu wechseln.</span><span class="sxs-lookup"><span data-stu-id="f7ee5-133">The **Bypass for network** checkbox bypasses the service worker and forces the browser to go to the network for requested resources.</span></span>  
*   <span data-ttu-id="f7ee5-134">Die Schaltfläche " **Aktualisieren** " führt eine einmalige Aktualisierung der angegebenen Dienstmitarbeiter aus.</span><span class="sxs-lookup"><span data-stu-id="f7ee5-134">The **Update** button performs a one-time update of the specified service worker.</span></span>  
*   <span data-ttu-id="f7ee5-135">Die Schaltfläche " **Push** " emuliert eine Push-Benachrichtigung ohne Nutzlast \ (auch bekannt als " **Tickle**\").</span><span class="sxs-lookup"><span data-stu-id="f7ee5-135">The **Push** button emulates a push notification without a payload \(also known as a **tickle**\).</span></span>  
*   <span data-ttu-id="f7ee5-136">Die Schaltfläche " **Synchronisieren** " emuliert ein Hintergrund Synchronisierungsereignis.</span><span class="sxs-lookup"><span data-stu-id="f7ee5-136">The **Sync** button emulates a background sync event.</span></span>  
*   <span data-ttu-id="f7ee5-137">Mit der Schaltfläche zum **aufheben** der Registrierung wird der angegebene Dienstmitarbeiter aufgehoben.</span><span class="sxs-lookup"><span data-stu-id="f7ee5-137">The **Unregister** button unregisters the specified service worker.</span></span>  <span data-ttu-id="f7ee5-138">Schauen Sie sich das Kontrollkästchen [Speicher löschen](#clear-storage) an, um eine Möglichkeit zum Aufheben der Registrierung eines Dienstmitarbeiter und zum Löschen von Speicher und Zwischenspeichern mit einem einzigen Mausklick zu finden.</span><span class="sxs-lookup"><span data-stu-id="f7ee5-138">Check out [Clear storage](#clear-storage) for a way to unregister a service worker and wipe storage and caches with a single button click.</span></span>  
*   <span data-ttu-id="f7ee5-139">Die **Quell** Zeile zeigt an, wann der aktuell ausgeführte Dienstmitarbeiter installiert wurde.</span><span class="sxs-lookup"><span data-stu-id="f7ee5-139">The **Source** line tells you when the currently running service worker was installed.</span></span>  <span data-ttu-id="f7ee5-140">Bei dem Link handelt es sich um den Namen der Quelldatei des Dienst Mitarbeiters.</span><span class="sxs-lookup"><span data-stu-id="f7ee5-140">The link is the name of the service worker's source file.</span></span>  <span data-ttu-id="f7ee5-141">Wenn Sie auf den Link klicken, werden Sie an die Quelle des Dienst Mitarbeiters gesendet.</span><span class="sxs-lookup"><span data-stu-id="f7ee5-141">Clicking on the link sends you to the service worker's source.</span></span>  
*   <span data-ttu-id="f7ee5-142">In der **Status** Zeile wird der Status der Dienstmitarbeiter angezeigt.</span><span class="sxs-lookup"><span data-stu-id="f7ee5-142">The **Status** line tells you the status of the service worker.</span></span>  <span data-ttu-id="f7ee5-143">Die ID-Nummer neben dem grünen Statusindikator \ ( `#36` in der vorherigen Abbildung \) ist für den aktuell aktiven Dienstmitarbeiter.</span><span class="sxs-lookup"><span data-stu-id="f7ee5-143">The ID number next to the green status indicator \(`#36` in previous figure\) is for the currently active Service Worker.</span></span>  <span data-ttu-id="f7ee5-144">Neben dem Status wird die Schaltfläche **Start** \ (wenn der Dienstmitarbeiter angehalten wird) oder eine Schaltfläche " **Beenden** " \ (wenn der Dienstmitarbeiter ausgeführt wird) angezeigt.</span><span class="sxs-lookup"><span data-stu-id="f7ee5-144">Next to the status you'll see a **start** button \(if the service worker is stopped\) or a **stop** button \(if the service worker is running\).</span></span>  <span data-ttu-id="f7ee5-145">Dienstmitarbeiter sind so konzipiert, dass Sie jederzeit angehalten und vom Browser gestartet werden können.</span><span class="sxs-lookup"><span data-stu-id="f7ee5-145">Service workers are designed to be stopped and started by the browser at any time.</span></span>  <span data-ttu-id="f7ee5-146">Das explizite beenden Ihrer Dienstmitarbeiter mithilfe der Schaltfläche " **Beenden** " kann dies simulieren.</span><span class="sxs-lookup"><span data-stu-id="f7ee5-146">Explicitly stopping your service worker using the **stop** button can simulate that.</span></span>  <span data-ttu-id="f7ee5-147">Das Beenden Ihrer Dienstmitarbeiter stellt eine hervorragende Möglichkeit dar, zu testen, wie sich der Code verhält, wenn der Dienstmitarbeiter wieder startet.</span><span class="sxs-lookup"><span data-stu-id="f7ee5-147">Stopping your service worker is a great way to test how your code behaves when the service worker starts back up again.</span></span>  <span data-ttu-id="f7ee5-148">Sie zeigt häufig Fehler aufgrund fehlerhafter Annahmen über den persistenten globalen Zustand.</span><span class="sxs-lookup"><span data-stu-id="f7ee5-148">It frequently reveals bugs due to faulty assumptions about persistent global state.</span></span>  
*   <span data-ttu-id="f7ee5-149">Die Zeile " **Clients** " gibt den Ursprung an, auf den sich der Dienstmitarbeiter beläuft.</span><span class="sxs-lookup"><span data-stu-id="f7ee5-149">The **Clients** line tells you the origin that the service worker is scoped to.</span></span>  <span data-ttu-id="f7ee5-150">Die Schaltfläche " **Fokus** " ist meist hilfreich, wenn Sie das Kontrollkästchen " **Alle anzeigen** " aktiviert haben.</span><span class="sxs-lookup"><span data-stu-id="f7ee5-150">The **focus** button is mostly useful when you've enabled the **show all** checkbox.</span></span>  <span data-ttu-id="f7ee5-151">Wenn dieses Kontrollkästchen aktiviert ist, werden alle registrierten Dienstmitarbeiter aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="f7ee5-151">When that checkbox is enabled, all registered service workers are listed.</span></span>  <span data-ttu-id="f7ee5-152">Wenn Sie auf die Schaltfläche **Fokus** neben einem Dienstmitarbeiter klicken, der auf einer anderen Registerkarte ausgeführt wird, konzentriert sich Microsoft Edge auf die Registerkarte.</span><span class="sxs-lookup"><span data-stu-id="f7ee5-152">If you click on the **focus** button next to a service worker that is running in a different tab, Microsoft Edge focuses on that tab.</span></span>  
    
<span data-ttu-id="f7ee5-153">Wenn der Dienstmitarbeiter Fehler verursacht, wird eine neue Bezeichnung mit dem Namen **Fehler** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="f7ee5-153">If the service worker causes any errors, a new label called **Errors** shows up.</span></span>  

<!--  
:::image type="complex" source="./media/sw-error.msft.png" alt-text="Bereich ' Manifest '" lightbox="./media/sw-error.msft.png":::
   Service worker with errors  
:::image-end:::
-->  

<!--TODO:  Capture Service Worker Errors sample when available. -->
<!--TODO:  Link Web "How tickle works" sections when available. -->

## <span data-ttu-id="f7ee5-154">Dienst Worker-Caches</span><span class="sxs-lookup"><span data-stu-id="f7ee5-154">Service worker caches</span></span> 

<span data-ttu-id="f7ee5-155">Der Bereich **Cache-Speicher** bietet eine schreibgeschützte Liste der Ressourcen, die mit der [Cache-API][MDNWebCacheAPI]\ (Service Worker \) zwischengespeichert wurden.</span><span class="sxs-lookup"><span data-stu-id="f7ee5-155">The **Cache Storage** pane provides a read-only list of resources that have been cached using the \(service worker\) [Cache API][MDNWebCacheAPI].</span></span>  

:::image type="complex" source="./media/cache-pane-cache-storage-resources.msft.png" alt-text="Bereich ' Manifest '" lightbox="./media/cache-pane-cache-storage-resources.msft.png":::
   <span data-ttu-id="f7ee5-157">Der **Cache Speicher** Bereich</span><span class="sxs-lookup"><span data-stu-id="f7ee5-157">The **Cache Storage** Pane</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="f7ee5-158">Wenn Sie zum ersten Mal einen Cache öffnen und ihm eine Ressource hinzufügen, erkennt devtools die Änderung möglicherweise nicht.</span><span class="sxs-lookup"><span data-stu-id="f7ee5-158">The first time you open a cache and add a resource to it, DevTools might not detect the change.</span></span>  <span data-ttu-id="f7ee5-159">Laden Sie die Seite neu, und Sie sollten den Cache sehen.</span><span class="sxs-lookup"><span data-stu-id="f7ee5-159">Reload the page and you should see the cache.</span></span>  

<span data-ttu-id="f7ee5-160">Wenn zwei oder mehr Caches geöffnet sind, werden Sie unter der Dropdownliste **Cachespeicher** aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="f7ee5-160">If you have two or more caches open, you'll see them listed below the **Cache Storage** dropdown.</span></span>  

:::image type="complex" source="./media/cache-pane-cache-storage.msft.png" alt-text="Bereich ' Manifest '" lightbox="./media/cache-pane-cache-storage.msft.png":::
   <span data-ttu-id="f7ee5-162">Die Dropdownliste " **Cache Speicher** "</span><span class="sxs-lookup"><span data-stu-id="f7ee5-162">The **Cache Storage** dropdown</span></span>  
:::image-end:::  

## <span data-ttu-id="f7ee5-163">Kontingent Verwendung</span><span class="sxs-lookup"><span data-stu-id="f7ee5-163">Quota usage</span></span> 

<span data-ttu-id="f7ee5-164">Einige Antworten innerhalb des **Cache Speicher** Bereichs werden möglicherweise als "undurchsichtig" gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="f7ee5-164">Some responses within the **Cache Storage** pane may be flagged as being "opaque".</span></span>  <span data-ttu-id="f7ee5-165">Dies bezieht sich auf eine Antwort, die von einem anderen Ursprung abgerufen wurde, wie etwa von einem **CDN** oder einer Remote-API, wenn [CORS][FetchHttpCorsProtocol] nicht aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="f7ee5-165">This refers to a response retrieved from a different origin, like from a **CDN** or remote API, when [CORS][FetchHttpCorsProtocol] is not enabled.</span></span>  

<!--TODO:  Link Web "CDN" section when available. -->  
<!--TODO:  Link Web "opaque" section when available. -->

<span data-ttu-id="f7ee5-166">Um das Auslaufen von domänenübergreifenden Informationen zu vermeiden, wird die Größe einer undurchsichtigen Antwort, die für die Berechnung von Speicherkontingent Grenzwerten verwendet wird, erheblich erweitert (beispielsweise, ob eine `QuotaExceeded` Ausnahme ausgelöst wird \) und von der `navigator.storage` API gemeldet.</span><span class="sxs-lookup"><span data-stu-id="f7ee5-166">In order to avoid leakage of cross-domain information, there's significant padding added to the size of an opaque response used for calculating storage quota limits \(for example whether a `QuotaExceeded` exception is thrown\) and reported by the `navigator.storage` API.</span></span>  

<!--TODO:  Link Estimating "`navigator.storage` API" sections when available. -->

<span data-ttu-id="f7ee5-167">Die Details dieses Textabstands variieren von Browser zu Browser, aber für Microsoft Edge bedeutet dies, dass die **Mindestgröße** , die eine einzelne zwischengespeicherte undurchsichtige Antwort zur allgemeinen Speichernutzung beiträgt, [ungefähr 7 Megabyte][ChromiumIssues796060#c17]beträgt.</span><span class="sxs-lookup"><span data-stu-id="f7ee5-167">The details of this padding vary from browser to browser, but for Microsoft Edge, this means that the **minimum size** that any single cached opaque response contributes to the overall storage usage is [approximately 7 megabytes][ChromiumIssues796060#c17].</span></span>  <span data-ttu-id="f7ee5-168">Beachten Sie Folgendes, wenn Sie ermitteln möchten, wie viele undurchsichtige Antworten Sie zwischenspeichern möchten, da Sie die Speicherkontingent Einschränkungen auf einfache Weise überschreiten können, die auf der tatsächlichen Größe der opaken Ressourcen basiert.</span><span class="sxs-lookup"><span data-stu-id="f7ee5-168">You should keep this in mind when determining how many opaque responses you want to cache, since you could easily exceeded storage quota limitations much sooner than you'd otherwise expect based on the actual size of the opaque resources.</span></span>  

<span data-ttu-id="f7ee5-169">Verwandte Leitfäden:</span><span class="sxs-lookup"><span data-stu-id="f7ee5-169">Related Guides:</span></span>  

*   [<span data-ttu-id="f7ee5-170">Stapelüberlauf: Welche Einschränkungen gelten für undurchsichtige Antworten?</span><span class="sxs-lookup"><span data-stu-id="f7ee5-170">Stack Overflow: What limitations apply to opaque responses?</span></span>][StackOverflowLimitationsForOpaqueResponses]  
<!--*   [Alphabet work container: Understanding Storage Quota](/web/tools/Alphabet-work-container/guides/storage-quota#beware_of_opaque_responses)  -->
    
<!--TODO:  Link Work container storage quota for opaque responses section when available. -->

## <span data-ttu-id="f7ee5-171">Speicher löschen</span><span class="sxs-lookup"><span data-stu-id="f7ee5-171">Clear storage</span></span> 

<span data-ttu-id="f7ee5-172">Der Bereich " **Speicher löschen** " ist eine sehr nützliche Funktion, wenn Sie Progressive Web-Apps entwickeln.</span><span class="sxs-lookup"><span data-stu-id="f7ee5-172">The **Clear Storage** pane is a very useful feature when developing progressive web apps.</span></span>  <span data-ttu-id="f7ee5-173">In diesem Bereich können Sie die Registrierung von Dienst Mitarbeitern aufheben und alle Caches und den Speicher mit einem einzigen Klick auf die Schaltfläche Löschen.</span><span class="sxs-lookup"><span data-stu-id="f7ee5-173">This pane lets you unregister service workers and clear all caches and storage with a single button click.</span></span>  <!--Check out the section below to learn more.  -->

<!--Related Guides:  

*   [Clear Storage](/iterate/manage-data/local-storage#clear-storage)  -->
    
<!--TODO:  Link to sections when available. -->

<!--## Other Application panel guides 

Check out the guides below for more help on the other panes of the **Application** panel.  

Related Guides:  

*   [Inspect page resources](/iterate/manage-data/page-resources)  
*   [Inspect and manage local storage and caches](/iterate/manage-data/local-storage)  -->
    
<!--TODO  -->

<!--  
 


-->  

<!-- links -->  

[DevtoolsCommandMenuIndex]: ./command-menu/index.md "Ausführen von Befehlen mit dem Befehlsmenü von Microsoft Edge devtools | Microsoft docs"  

[ChromiumIssues796060#c17]: https://bugs.chromium.org/p/chromium/issues/detail?id=796060#c17 "Chrom Problem 796060: der Cache Speicherwert steigt bei jeder Aktualisierung, wenn sich der Analysecode im HTML-Code befindet"  

[FetchHttpCorsProtocol]: https://fetch.spec.whatwg.org/#http-cors-protocol  

[MDNWebCacheAPI]: https://developer.mozilla.org/docs/Web/API/Cache "Cache-Web-APIs | MDN"  

[StackOverflowLimitationsForOpaqueResponses]: https://stackoverflow.com/q/39109789/385997 "Stapelüberlauf: Welche Einschränkungen gelten für undurchsichtige Antworten?"  

<!--[WebEstimatingAvailableStorageSpace]: whats-new/2017/08/estimating-available-storage-space  -->
<!--[RemoteDebugging]: /debug/remote-debugging/remote-debugging  -->

<!--[WebHowPushWorks]: /web/fundamentals/push-notifications/how-push-works  -->  
<!--[WebGlossaryCDN]: /web/fundamentals/glossary#CDN  -->
<!--[WebGlossaryOpaque]: /web/fundamentals/glossary#opaque-response  -->

> [!NOTE]
> <span data-ttu-id="f7ee5-178">Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f7ee5-178">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="f7ee5-179">Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/progressive-web-apps) und wird von [Kayce Basken][KayceBasques] (Technical Writer, Chrome devtools \ & Lighthouse \) erstellt.</span><span class="sxs-lookup"><span data-stu-id="f7ee5-179">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/progressive-web-apps) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
<span data-ttu-id="f7ee5-181">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="f7ee5-181">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
