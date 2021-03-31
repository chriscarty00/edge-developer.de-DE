---
description: Verwenden Sie den Anwendungsbereich, um Web-App-Manifeste, Servicemitarbeiter und Dienstmitarbeitercaches zu überprüfen, zu ändern und zu debuggen.
title: Debuggen progressiver Web-Apps
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, Entwicklungstools
ms.openlocfilehash: aea01d25474a030e78ac0eaeaef3954ab7f4539f
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398539"
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

# <a name="debug-progressive-web-apps"></a><span data-ttu-id="35bb9-104">Debuggen progressiver Web-Apps</span><span class="sxs-lookup"><span data-stu-id="35bb9-104">Debug Progressive Web Apps</span></span>  

<span data-ttu-id="35bb9-105">Verwenden Sie **den Anwendungsbereich,** um Web-App-Manifeste, Servicemitarbeiter und Dienstmitarbeitercaches zu überprüfen, zu ändern und zu debuggen.</span><span class="sxs-lookup"><span data-stu-id="35bb9-105">Use the **Application** panel to inspect, modify, and debug web app manifests, service workers, and service worker caches.</span></span>  

<!--Related Guides:  

*   [Progressive Web Apps](/web/progressive-web-apps)  -->

<!--TODO:  Link web "Progressive Web Apps" section when available. -->

<span data-ttu-id="35bb9-106">In diesem Handbuch werden nur die Progressive Web App-Features des **Anwendungsbereichs** erläutert.</span><span class="sxs-lookup"><span data-stu-id="35bb9-106">This guide only discusses the Progressive Web App features of the **Application** panel.</span></span>  <!--If you're looking for help on the other panes, check out the last section of this guide, [Other Application panel guides](#other-application-panel-guides).  -->

<!--TODO:  Link to sections when available. -->

### <a name="summary"></a><span data-ttu-id="35bb9-107">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="35bb9-107">Summary</span></span>  

*   <span data-ttu-id="35bb9-108">Verwenden Sie den **Manifestbereich,** um Ihr Web-App-Manifest zu überprüfen und Add to Homescreen-Ereignisse auszulösen.</span><span class="sxs-lookup"><span data-stu-id="35bb9-108">Use the **Manifest** pane to inspect your web app manifest and trigger Add to Homescreen events.</span></span>  
*   <span data-ttu-id="35bb9-109">Verwenden Sie **den Bereich Service Workers** für eine ganze Reihe von aufgabenbezogenen Aufgaben, z. B. aufheben der Registrierung oder Aktualisierung eines Diensts, Emulieren von Pushereignissen, Offlinemodus oder Beenden eines Dienstmitarbeiters.</span><span class="sxs-lookup"><span data-stu-id="35bb9-109">Use the **Service Workers** pane for a whole range of service-worker-related tasks, like unregistering or updating a service, emulating push events, going offline, or stopping a service worker.</span></span>  
*   <span data-ttu-id="35bb9-110">Anzeigen des Dienstarbeitscaches im **Cachespeicherbereich.**</span><span class="sxs-lookup"><span data-stu-id="35bb9-110">View your service worker cache from the **Cache Storage** pane.</span></span>  
*   <span data-ttu-id="35bb9-111">Aufheben der Registrierung eines Dienstmitarbeiters und Löschen aller Speicher und Caches mit einer einzelnen Schaltfläche wählen Sie aus dem **Bereich Speicher löschen** aus.</span><span class="sxs-lookup"><span data-stu-id="35bb9-111">Unregister a service worker and clear all storage and caches with a single button choose from the **Clear storage** pane.</span></span>  
    
## <a name="web-app-manifest"></a><span data-ttu-id="35bb9-112">Web-App-Manifest</span><span class="sxs-lookup"><span data-stu-id="35bb9-112">Web app manifest</span></span>  

<span data-ttu-id="35bb9-113">Wenn Sie möchten, dass Ihre Benutzer Ihre App ihren mobilen Startseiten hinzufügen können, benötigen Sie ein Web-App-Manifest.</span><span class="sxs-lookup"><span data-stu-id="35bb9-113">If you want your users to be able to add your app to their mobile homescreens, you need a web app manifest.</span></span>  <span data-ttu-id="35bb9-114">Das Manifest definiert, wie die App auf dem Startbildschirm angezeigt wird, wo der Benutzer beim Starten vom Startbildschirm direkt angezeigt werden soll und wie die App beim Start aussieht.</span><span class="sxs-lookup"><span data-stu-id="35bb9-114">The manifest defines how the app appears on the homescreen, where to direct the user when launching from homescreen, and what the app looks like on launch.</span></span>  

<!--Related Guides:  

*   [Improve user experiences with a Web App Manifest](/web/fundamentals/web-app-manifest)  
*   [Using App Install Banners](/web/fundamentals/app-install-banners)  -->

<!--TODO:  Link to sections when available. -->

<span data-ttu-id="35bb9-115">Nachdem Sie Ihr Manifest eingerichtet haben, können Sie  den **Manifestbereich** des Anwendungsbereichs verwenden, um es zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="35bb9-115">After you have your manifest set up, you may use the **Manifest** pane of the **Application** panel to inspect it.</span></span>  

:::image type="complex" source="../media/manifest-pane.msft.png" alt-text="Der Manifestbereich" lightbox="../media/manifest-pane.msft.png":::
   <span data-ttu-id="35bb9-117">Der **Manifestbereich**</span><span class="sxs-lookup"><span data-stu-id="35bb9-117">The **Manifest** Pane</span></span>  
:::image-end:::  

*   <span data-ttu-id="35bb9-118">Um die Manifestquelle zu sehen, wählen Sie den Link unter **App-Manifestbeschriftung** \( `https://airhorner.com/manifest.json` in der vorherigen Abbildung\).</span><span class="sxs-lookup"><span data-stu-id="35bb9-118">To look at the manifest source, choose the link below **App Manifest** label \(`https://airhorner.com/manifest.json` in the previous figure\).</span></span>  
<!-- *   Choose the **Add to homescreen** button to simulate an Add to Homescreen event.  Check out the next section for more information.  -->  
*   <span data-ttu-id="35bb9-119">In **den Abschnitten** **Identity und Presentation** werden nur Felder aus der Manifestquelle in einer benutzerfreundlicheren Anzeige angezeigt.</span><span class="sxs-lookup"><span data-stu-id="35bb9-119">The **Identity** and **Presentation** sections just display fields from the manifest source in a more user-friendly display.</span></span>  
*   <span data-ttu-id="35bb9-120">Im **Abschnitt Symbole** werden alle von Ihnen angegebenen Symbole angezeigt.</span><span class="sxs-lookup"><span data-stu-id="35bb9-120">The **Icons** section displays every icon that you've specified.</span></span>  
    
<!--### Simulate Add to Homescreen events  -->

<!--A web app may only be added to a homescreen when the site is visited at least twice, with at least five minutes between visits.  While developing or debugging your Add to Homescreen workflow, the criteria is potentially inconvenient.  
The **Add to homescreen** button on the **App Manifest** pane lets you simulate Add to Homescreen events whenever you want.  -->

<!--You may test out this feature with the [Microsoft I/O 2016 progressive web app](https://events.alpahabet.com/io2016/), which has proper support for Add to Homescreen.  Choosing on **Add to Homescreen** while the app is open prompts Microsoft Edge to display the "add this site to your shelf" banner, which is the desktop equivalent of the "add to homescreen" banner for mobile devices.  -->

<!--  
:::image type="complex" source="../media/io.msft.png" alt-text="Add to desktop shelf" lightbox="../media/io.msft.png":::
   Add to desktop shelf  
:::image-end:::
-->  

<!--
> [!Tip]
> Keep the **Console** drawer open while simulating Add to Homescreen events.  The Console tells you if your manifest has any issues and logs other information about the Add to Homescreen lifecycle.  -->

<!--The **Add to Homescreen** feature may not yet simulate the workflow for mobile devices.  Notice how the "add to shelf" prompt was triggered in the screenshot above, even though DevTools is in Device Mode.  However, if you may successfully add your app to your desktop shelf, then it works for mobile, too.  -->

<!-- TODO: Rework content after sample app is created. -->

<!--If you want to test out the genuine mobile experience, you may connect a real mobile device to DevTools via **remote debugging**, and then choose the **Add to Homescreen** button \(on DevTools\) to trigger the "add to homescreen" prompt on the connected mobile device.  -->

<!--TODO:  Link Debug "remote debugging" sections when available. -->

## <a name="service-workers"></a><span data-ttu-id="35bb9-121">Service Workers</span><span class="sxs-lookup"><span data-stu-id="35bb9-121">Service workers</span></span>  

<span data-ttu-id="35bb9-122">Servicemitarbeiter sind eine grundlegende Technologie in der zukünftigen Webplattform.</span><span class="sxs-lookup"><span data-stu-id="35bb9-122">Service workers are a fundamental technology in the future web platform.</span></span>  <span data-ttu-id="35bb9-123">Dabei handelt es sich um Skripts, die im Hintergrund ausgeführt werden, getrennt von einer Webseite.</span><span class="sxs-lookup"><span data-stu-id="35bb9-123">They are scripts that the browser runs in the background, separate from a web page.</span></span>  <span data-ttu-id="35bb9-124">Mit den Skripts können Sie auf Features zugreifen, die ohne eine Webseite oder Benutzerinteraktion wie Pushbenachrichtigungen, Hintergrundsynchronisierung und Offlineerfahrungen erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="35bb9-124">The scripts allow you to access features that without the need of a web page or user interaction, like push notifications, background sync, and offline experiences.</span></span>  

<!--Related Guides:  

*   [Intro to Service Workers](/web/fundamentals/primers/service-worker)  
*   [Push Notifications: Timely, Relevant, and Precise](/web/fundamentals/push-notifications)  -->  
    
<!--TODO:  Link to sections when available. -->  

<span data-ttu-id="35bb9-125">Der **Bereich "Service Workers"** im **Bereich "Anwendung"** ist der wichtigste Ort in DevTools zum Überprüfen und Debuggen von Servicemitarbeitern.</span><span class="sxs-lookup"><span data-stu-id="35bb9-125">The **Service Workers** pane in the **Application** panel is the main place in DevTools to inspect and debug service workers.</span></span>  

:::image type="complex" source="../media/service-workers-pane.msft.png" alt-text="Der Bereich Service Workers" lightbox="../media/service-workers-pane.msft.png":::
   <span data-ttu-id="35bb9-127">Der **Bereich "Service Workers"**</span><span class="sxs-lookup"><span data-stu-id="35bb9-127">The **Service Workers** pane</span></span>  
:::image-end:::  

*   <span data-ttu-id="35bb9-128">Wenn ein Dienstmitarbeiter auf der derzeit geöffneten Seite installiert ist, wird er in diesem Bereich aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="35bb9-128">If a service worker is installed to the currently open page, then it is listed on this pane.</span></span>  <span data-ttu-id="35bb9-129">In der vorherigen Abbildung ist beispielsweise ein Dienstmitarbeiter für den Bereich `https://weather-pwa-sample.firebaseapp.com` installiert.</span><span class="sxs-lookup"><span data-stu-id="35bb9-129">For example, in the previous figure, there is a service worker installed for the scope of `https://weather-pwa-sample.firebaseapp.com`.</span></span>  
*   <span data-ttu-id="35bb9-130">Das **Kontrollkästchen Offline** versetzt DevTools in den Offlinemodus.</span><span class="sxs-lookup"><span data-stu-id="35bb9-130">The **Offline** checkbox puts DevTools into offline mode.</span></span>  <span data-ttu-id="35bb9-131">Dies entspricht dem Offlinemodus, der über **das** Netzwerktool verfügbar ist, oder der Option `Go offline` im [Befehlsmenü][DevtoolsCommandMenuIndex].</span><span class="sxs-lookup"><span data-stu-id="35bb9-131">This is equivalent to the offline mode available from the **Network** tool, or the `Go offline` option in the [Command Menu][DevtoolsCommandMenuIndex].</span></span>  
*   <span data-ttu-id="35bb9-132">Das **Kontrollkästchen Beim Erneutladen** aktualisieren erzwingt, dass der Dienstmitarbeiter bei jeder Seitenlast aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="35bb9-132">The **Update on reload** checkbox forces the service worker to update on every page load.</span></span>  
*   <span data-ttu-id="35bb9-133">Das **Kontrollkästchen Netzwerkumgehung** umgehen umgeht den Dienstmitarbeiter und zwingt den Browser, für angeforderte Ressourcen in das Netzwerk zu wechseln.</span><span class="sxs-lookup"><span data-stu-id="35bb9-133">The **Bypass for network** checkbox bypasses the service worker and forces the browser to go to the network for requested resources.</span></span>  
*   <span data-ttu-id="35bb9-134">Die **Schaltfläche** Aktualisieren führt eine einmalaktualisierung des angegebenen Dienstmitarbeiters durch.</span><span class="sxs-lookup"><span data-stu-id="35bb9-134">The **Update** button performs a one-time update of the specified service worker.</span></span>  
*   <span data-ttu-id="35bb9-135">Die **Schaltfläche Push** emuliert eine Pushbenachrichtigung ohne Nutzlast \(auch als **Tickle \)** bekannt.</span><span class="sxs-lookup"><span data-stu-id="35bb9-135">The **Push** button emulates a push notification without a payload \(also known as a **tickle**\).</span></span>  
*   <span data-ttu-id="35bb9-136">Die **Schaltfläche Synchronisierung** emuliert ein Hintergrundsynchronisierungsereignis.</span><span class="sxs-lookup"><span data-stu-id="35bb9-136">The **Sync** button emulates a background sync event.</span></span>  
*   <span data-ttu-id="35bb9-137">Mit **der Schaltfläche** Aufheben der Registrierung wird die Registrierung des angegebenen Dienstmitarbeiters aufgehoben.</span><span class="sxs-lookup"><span data-stu-id="35bb9-137">The **Unregister** button unregisters the specified service worker.</span></span>  <span data-ttu-id="35bb9-138">Weitere Informationen zum [Aufheben der](#clear-storage) Registrierung eines Dienstmitarbeiters und zum Löschen von Speicher und Zwischenspeichern mit einer einzelnen Schaltfläche finden Sie unter Löschen des Speichers.</span><span class="sxs-lookup"><span data-stu-id="35bb9-138">Check out [Clear storage](#clear-storage) for a way to unregister a service worker and wipe storage and caches with a single button choose.</span></span>  
*   <span data-ttu-id="35bb9-139">Die **Zeile Source** informiert Sie, wann der derzeit ausgeführte Dienstmitarbeiter installiert wurde.</span><span class="sxs-lookup"><span data-stu-id="35bb9-139">The **Source** line tells you when the currently running service worker was installed.</span></span>  <span data-ttu-id="35bb9-140">Der Link ist der Name der Quelldatei des Dienstmitarbeiters.</span><span class="sxs-lookup"><span data-stu-id="35bb9-140">The link is the name of the source file of the service worker.</span></span>  <span data-ttu-id="35bb9-141">Wenn Sie den Link auswählen, werden Sie an die Quelle des Servicemitarbeiters übermittelt.</span><span class="sxs-lookup"><span data-stu-id="35bb9-141">Choosing on the link sends you to the source of the service worker.</span></span>  
*   <span data-ttu-id="35bb9-142">In **der Zeile Status** wird der Status des Servicemitarbeiters angezeigt.</span><span class="sxs-lookup"><span data-stu-id="35bb9-142">The **Status** line tells you the status of the service worker.</span></span>  <span data-ttu-id="35bb9-143">Die ID-Nummer neben dem grünen Statusindikator \( in der vorherigen Abbildung\) ist für den `#36` derzeit aktiven Service Worker.</span><span class="sxs-lookup"><span data-stu-id="35bb9-143">The ID number next to the green status indicator \(`#36` in previous figure\) is for the currently active Service Worker.</span></span>  <span data-ttu-id="35bb9-144">Neben dem Status  wird eine Startschaltfläche \(wenn der  Dienstmitarbeiter beendet wird\) oder eine Stoppschaltfläche \(wenn der Dienstmitarbeiter ausgeführt wird\) angezeigt.</span><span class="sxs-lookup"><span data-stu-id="35bb9-144">Next to the status, a **start** button \(if the service worker is stopped\) or a **stop** button \(if the service worker is running\) is displayed.</span></span>  <span data-ttu-id="35bb9-145">Servicemitarbeiter sind so konzipiert, dass sie jederzeit vom Browser angehalten und gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="35bb9-145">Service workers are designed to be stopped and started by the browser at any time.</span></span>  <span data-ttu-id="35bb9-146">Das explizite Beenden des Dienstmitarbeiters **mithilfe** der Stoppschaltfläche kann dies simulieren.</span><span class="sxs-lookup"><span data-stu-id="35bb9-146">Explicitly stopping your service worker using the **stop** button may simulate that.</span></span>  <span data-ttu-id="35bb9-147">Das Beenden des Dienstmitarbeiters ist eine hervorragende Möglichkeit, um zu testen, wie sich Ihr Code verhält, wenn der Dienstmitarbeiter wieder hoch startet.</span><span class="sxs-lookup"><span data-stu-id="35bb9-147">Stopping your service worker is a great way to test how your code behaves when the service worker starts back up again.</span></span>  <span data-ttu-id="35bb9-148">Aufgrund fehlerhafter Annahmen über den dauerhaften globalen Zustand werden häufig Fehler gemeldet.</span><span class="sxs-lookup"><span data-stu-id="35bb9-148">It frequently reveals bugs due to faulty assumptions about persistent global state.</span></span>  
*   <span data-ttu-id="35bb9-149">Die **Zeile Clients** teilt Ihnen den Ursprung mit, auf den der Dienstmitarbeiter begrenzt ist.</span><span class="sxs-lookup"><span data-stu-id="35bb9-149">The **Clients** line tells you the origin that the service worker is scoped to.</span></span>  <span data-ttu-id="35bb9-150">Die **Fokusschaltfläche** ist hauptsächlich hilfreich, wenn Sie das Kontrollkästchen Alle **Anzeigen** aktiviert haben.</span><span class="sxs-lookup"><span data-stu-id="35bb9-150">The **focus** button is mostly useful when you've enabled the **show all** checkbox.</span></span>  <span data-ttu-id="35bb9-151">Wenn dieses Kontrollkästchen aktiviert ist, werden alle registrierten Servicemitarbeiter aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="35bb9-151">When that checkbox is enabled, all registered service workers are listed.</span></span>  <span data-ttu-id="35bb9-152">Wenn Sie die **Fokusschaltfläche** neben einem Servicemitarbeiter auswählen, der auf einer anderen Registerkarte ausgeführt wird, konzentriert sich Microsoft Edge auf diese Registerkarte.</span><span class="sxs-lookup"><span data-stu-id="35bb9-152">If you choose on the **focus** button next to a service worker that is running in a different tab, Microsoft Edge focuses on that tab.</span></span>  
    
<span data-ttu-id="35bb9-153">Wenn der Dienstmitarbeiter Fehler verursacht, wird eine neue Bezeichnung **namens Errors** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="35bb9-153">If the service worker causes any errors, a new label called **Errors** shows up.</span></span>  

<!--  
:::image type="complex" source="../media/sw-error.msft.png" alt-text="Service worker with errors" lightbox="../media/sw-error.msft.png":::
   Service worker with errors  
:::image-end:::
-->  

<!--TODO:  Capture Service Worker Errors sample when available. -->
<!--TODO:  Link Web "How tickle works" sections when available. -->

## <a name="service-worker-caches"></a><span data-ttu-id="35bb9-154">Dienstarbeitscaches</span><span class="sxs-lookup"><span data-stu-id="35bb9-154">Service worker caches</span></span>  

<span data-ttu-id="35bb9-155">Der **Bereich Cachespeicher** enthält eine schreibgeschützte Liste der Ressourcen, die mithilfe der Cache-API \(Service Worker\) [zwischengespeichert wurden.][MDNWebCacheAPI]</span><span class="sxs-lookup"><span data-stu-id="35bb9-155">The **Cache Storage** pane provides a read-only list of resources that have been cached using the \(service worker\) [Cache API][MDNWebCacheAPI].</span></span>  

:::image type="complex" source="../media/cache-pane-cache-storage-resources.msft.png" alt-text="Cachespeicherbereich" lightbox="../media/cache-pane-cache-storage-resources.msft.png":::
   <span data-ttu-id="35bb9-157">**Cachespeicherbereich**</span><span class="sxs-lookup"><span data-stu-id="35bb9-157">The **Cache Storage** Pane</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="35bb9-158">Wenn Sie zum ersten Mal einen Cache öffnen und eine Ressource hinzufügen, erkennt DevTools die Änderung möglicherweise nicht.</span><span class="sxs-lookup"><span data-stu-id="35bb9-158">The first time you open a cache and add a resource to it, DevTools may not detect the change.</span></span>  <span data-ttu-id="35bb9-159">Aktualisieren Sie die Seite, und zeigen Sie den Cache an.</span><span class="sxs-lookup"><span data-stu-id="35bb9-159">Refresh the page and to display the cache.</span></span>  

<span data-ttu-id="35bb9-160">Wenn sie zwei oder mehr Caches geöffnet haben, werden die Caches im folgenden **Dropdownmenü Cachespeicher** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="35bb9-160">If you have two or more caches open, the caches display under the following **Cache Storage** dropdown.</span></span>  

:::image type="complex" source="../media/cache-pane-cache-storage.msft.png" alt-text="Dropdownliste Cachespeicher" lightbox="../media/cache-pane-cache-storage.msft.png":::
   <span data-ttu-id="35bb9-162">Dropdownliste **Cachespeicher**</span><span class="sxs-lookup"><span data-stu-id="35bb9-162">The **Cache Storage** dropdown</span></span>  
:::image-end:::  

## <a name="quota-usage"></a><span data-ttu-id="35bb9-163">Kontingentverwendung</span><span class="sxs-lookup"><span data-stu-id="35bb9-163">Quota usage</span></span>  

<span data-ttu-id="35bb9-164">Einige Antworten im **Bereich Cachespeicher** werden möglicherweise als "undurchsichtig" gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="35bb9-164">Some responses within the **Cache Storage** pane may be flagged as being "opaque".</span></span>  <span data-ttu-id="35bb9-165">Dies bezieht sich auf eine Antwort, die von einem anderen Ursprung abgerufen wird, z. B. aus einem **CDN** oder einer Remote-API, wenn [CORS][FetchHttpCorsProtocol] nicht aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="35bb9-165">This refers to a response retrieved from a different origin, like from a **CDN** or remote API, when [CORS][FetchHttpCorsProtocol] is not enabled.</span></span>  

<!--TODO:  Link Web "CDN" section when available. -->  
<!--TODO:  Link Web "opaque" section when available. -->

<span data-ttu-id="35bb9-166">Um ein Leck an domänenübergreifenden Informationen zu vermeiden, wird der Größe einer undurchsichtigen Antwort, die zum Berechnen von Speicherkontingentgrenzen verwendet wird \(z. B. ob eine Ausnahme ausgelöst wird\) und von der API gemeldet, ein erheblicher Abstand `QuotaExceeded` `navigator.storage` hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="35bb9-166">In order to avoid leakage of cross-domain information, significant padding is added to the size of an opaque response used for calculating storage quota limits \(for example whether a `QuotaExceeded` exception is thrown\) and reported by the `navigator.storage` API.</span></span>  

<!--TODO:  Link Estimating "`navigator.storage` API" sections when available. -->

<span data-ttu-id="35bb9-167">Die Details dieses Abstands variieren von Browser zu Browser, für  Microsoft Edge bedeutet dies jedoch, dass die Mindestgröße, die eine einzelne zwischengespeicherte undurchsichtige Antwort zur Gesamtspeichernutzung beiträgt, ca. 7 MB [beträgt.][ChromiumIssues796060#c17]</span><span class="sxs-lookup"><span data-stu-id="35bb9-167">The details of this padding vary from browser to browser, but for Microsoft Edge, this means that the **minimum size** that any single cached opaque response contributes to the overall storage usage is [approximately 7 megabytes][ChromiumIssues796060#c17].</span></span>  <span data-ttu-id="35bb9-168">Denken Sie an den Abstand, wenn Sie bestimmen, wie viele undurchsichtige Antworten Zwischenspeicherung erfordern, da Speicherkontingentbeschränkungen möglicherweise viel früher überschritten werden, als Sie es basierend auf der tatsächlichen Größe der undurchsichtigen Ressourcen sonst erwarten.</span><span class="sxs-lookup"><span data-stu-id="35bb9-168">Remember the padding when determining how many opaque responses you want to cache, since you may easily exceed storage quota limitations much sooner than you otherwise expect based on the actual size of the opaque resources.</span></span>  

<span data-ttu-id="35bb9-169">Verwandte Leitfäden:</span><span class="sxs-lookup"><span data-stu-id="35bb9-169">Related Guides:</span></span>  

*   [<span data-ttu-id="35bb9-170">Stack Overflow: Welche Einschränkungen gelten für undurchsichtige Antworten?</span><span class="sxs-lookup"><span data-stu-id="35bb9-170">Stack Overflow: What limitations apply to opaque responses?</span></span>][StackOverflowLimitationsForOpaqueResponses]  
<!--*   [Alphabet work container: Understanding Storage Quota](/web/tools/Alphabet-work-container/guides/storage-quota#beware_of_opaque_responses)  -->
    
<!--TODO:  Link Work container storage quota for opaque responses section when available. -->

## <a name="clear-storage"></a><span data-ttu-id="35bb9-171">Löschen des Speichers</span><span class="sxs-lookup"><span data-stu-id="35bb9-171">Clear storage</span></span>  

<span data-ttu-id="35bb9-172">Der **Bereich Speicher löschen** ist ein sehr nützliches Feature bei der Entwicklung progressiver Web-Apps.</span><span class="sxs-lookup"><span data-stu-id="35bb9-172">The **Clear Storage** pane is a very useful feature when developing progressive web apps.</span></span>  <span data-ttu-id="35bb9-173">In diesem Bereich können Sie die Registrierung von Servicemitarbeitern aufheben und alle Caches und Speicher mit einer einzigen Schaltfläche löschen.</span><span class="sxs-lookup"><span data-stu-id="35bb9-173">This pane lets you unregister service workers and clear all caches and storage with a single button choose.</span></span>  <!--Check out the section below to learn more.  -->

<!--Related Guides:  

*   [Clear Storage](/iterate/manage-data/local-storage#clear-storage)  -->
    
<!--TODO:  Link to sections when available. -->

<!--## Other Application panel guides   

Check out the guides below for more help on the other panes of the **Application** panel.  

Related Guides:  

*   [Inspect page resources](/iterate/manage-data/page-resources)  
*   [Inspect and manage local storage and caches](/iterate/manage-data/local-storage)  -->
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="35bb9-174">Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen</span><span class="sxs-lookup"><span data-stu-id="35bb9-174">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsCommandMenuIndex]: ../command-menu/index.md "Ausführen von Befehlen mit der Microsoft Edge DevTools-Befehlsmenüleiste | Microsoft Docs"  

[ChromiumIssues796060#c17]: https://bugs.chromium.org/p/chromium/issues/detail?id=796060#c17 "Chromium Issue 796060: Cache Storage value rises on each refresh when Analytics code is in the html"  

[FetchHttpCorsProtocol]: https://fetch.spec.whatwg.org/#http-cors-protocol  

[MDNWebCacheAPI]: https://developer.mozilla.org/docs/Web/API/Cache "Cache – Web-APIs | MDN"  

[StackOverflowLimitationsForOpaqueResponses]: https://stackoverflow.com/q/39109789/385997 "Stack Overflow: Welche Einschränkungen gelten für undurchsichtige Antworten?"  

<!--[WebEstimatingAvailableStorageSpace]: whats-new/2017/08/estimating-available-storage-space  -->
<!--[RemoteDebugging]: /debug/remote-debugging/remote-debugging  -->

<!--[WebHowPushWorks]: /web/fundamentals/push-notifications/how-push-works  -->  
<!--[WebGlossaryCDN]: /web/fundamentals/glossary#CDN  -->
<!--[WebGlossaryOpaque]: /web/fundamentals/glossary#opaque-response  -->

> [!NOTE]
> <span data-ttu-id="35bb9-179">Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="35bb9-179">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="35bb9-180">Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/progressive-web-apps) und wird von [Kayce Basken][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\) verfasst.</span><span class="sxs-lookup"><span data-stu-id="35bb9-180">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/progressive-web-apps) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="35bb9-182">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="35bb9-182">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
