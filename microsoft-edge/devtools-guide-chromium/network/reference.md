---
title: Netzwerkanalyse Referenz
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/30/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Web-Entwicklung, F12-Tools, devtools
ms.openlocfilehash: 460ad05983e7615e8739953ce3cb7d559492bc90
ms.sourcegitcommit: 33663cd7838dddee86228dde469a5e9551bddb02
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/30/2020
ms.locfileid: "10611840"
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







# <span data-ttu-id="6fc3d-103">Netzwerkanalyse Referenz</span><span class="sxs-lookup"><span data-stu-id="6fc3d-103">Network Analysis Reference</span></span>   



<span data-ttu-id="6fc3d-104">Entdecken Sie neue Möglichkeiten zur Analyse, wie Ihre Seite in dieser umfassenden Referenz der Microsoft Edge devtools-Netzwerkanalyse Features geladen werden kann.</span><span class="sxs-lookup"><span data-stu-id="6fc3d-104">Discover new ways to analyze how your page loads in this comprehensive reference of Microsoft Edge DevTools network analysis features.</span></span>  

<!--
> [!NOTE]
> This reference is based on Microsoft Edge 58.  If you use another version of Microsoft Edge, the UI, and features of DevTools may be different.  Check `edge://help` to see what version of Microsoft Edge you are running.  
-->

## <span data-ttu-id="6fc3d-105">Aufzeichnen von Netzwerkanforderungen</span><span class="sxs-lookup"><span data-stu-id="6fc3d-105">Record network requests</span></span>   

<span data-ttu-id="6fc3d-106">Standardmäßig zeichnet devtools alle Netzwerkanforderungen im Netzwerk Panel auf, solange devtools geöffnet ist.</span><span class="sxs-lookup"><span data-stu-id="6fc3d-106">By default, DevTools records all network requests in the Network panel, so long as DevTools is open.</span></span>  

> ##### <span data-ttu-id="6fc3d-107">Abbildung1</span><span class="sxs-lookup"><span data-stu-id="6fc3d-107">Figure 1</span></span>  
> <span data-ttu-id="6fc3d-108">Netzwerk Panel</span><span class="sxs-lookup"><span data-stu-id="6fc3d-108">The Network panel</span></span>  
> ![Netzwerk Panel][ImageNetworkPanel]  

### <span data-ttu-id="6fc3d-110">Beenden der Aufzeichnung von Netzwerkanforderungen</span><span class="sxs-lookup"><span data-stu-id="6fc3d-110">Stop recording network requests</span></span>   

<span data-ttu-id="6fc3d-111">So beenden Sie die Aufzeichnung von Anforderungen:</span><span class="sxs-lookup"><span data-stu-id="6fc3d-111">To stop recording requests:</span></span>  

*   <span data-ttu-id="6fc3d-112">Wählen **Stop recording network log** Sie ![ ][ImageRecordOnIcon] auf der Registerkarte **Netzwerk** die Option Aufzeichnung des Netzwerkprotokolls beenden Aufzeichnung beenden aus.</span><span class="sxs-lookup"><span data-stu-id="6fc3d-112">Select **Stop recording network log** ![Stop recording network log][ImageRecordOnIcon] on the **Network** panel.</span></span>  <span data-ttu-id="6fc3d-113">Es wird grau, um anzugeben, dass devtools keine Anforderungen mehr aufzeichnet.</span><span class="sxs-lookup"><span data-stu-id="6fc3d-113">It turns grey to indicate that DevTools is no longer recording requests.</span></span>  
*   <span data-ttu-id="6fc3d-114">Drücken Sie `Control` + `E` \ (Windows \) oder `Command` + `E` \ (macOS \), während sich der Fokus des **Netzwerk** Panels befindet.</span><span class="sxs-lookup"><span data-stu-id="6fc3d-114">Press `Control`+`E` \(Windows\) or `Command`+`E` \(macOS\) while the **Network** panel is in focus.</span></span>  

### <span data-ttu-id="6fc3d-115">Löschen von Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6fc3d-115">Clear requests</span></span>   

<span data-ttu-id="6fc3d-116">Wählen **Sie** ![ ][ImageClearIcon] im Netzwerk Panel löschen aus, um alle Anforderungen aus der Tabelle Anforderungen zu löschen.</span><span class="sxs-lookup"><span data-stu-id="6fc3d-116">Select **Clear** ![Clear][ImageClearIcon] on the Network panel to clear all requests from the Requests table.</span></span>  

> ##### <span data-ttu-id="6fc3d-117">Abbildung2</span><span class="sxs-lookup"><span data-stu-id="6fc3d-117">Figure 2</span></span>  
> <span data-ttu-id="6fc3d-118">Die Schaltfläche "Löschen"</span><span class="sxs-lookup"><span data-stu-id="6fc3d-118">The Clear button</span></span>  
> ![Die Schaltfläche "Löschen"][ImageClearButton]  

### <span data-ttu-id="6fc3d-120">Speichern von Anforderungen über Seitenlasten hinweg</span><span class="sxs-lookup"><span data-stu-id="6fc3d-120">Save requests across page loads</span></span>   

<span data-ttu-id="6fc3d-121">Aktivieren Sie das Kontrollkästchen **Protokoll beibehalten** auf der Registerkarte Netzwerk, um Anforderungen zwischen den Seitenlasten zu speichern.</span><span class="sxs-lookup"><span data-stu-id="6fc3d-121">To save requests across page loads, check the **Preserve log** checkbox on the Network panel.</span></span>  <span data-ttu-id="6fc3d-122">DevTools speichert alle Anforderungen, bis Sie **Protokoll beibehalten**deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="6fc3d-122">DevTools saves all requests until you disable **Preserve log**.</span></span>  

> ##### <span data-ttu-id="6fc3d-123">Abbildung 3</span><span class="sxs-lookup"><span data-stu-id="6fc3d-123">Figure 3</span></span>  
> <span data-ttu-id="6fc3d-124">Kontrollkästchen "Protokoll beibehalten"</span><span class="sxs-lookup"><span data-stu-id="6fc3d-124">The Preserve Log checkbox</span></span>  
> ![Kontrollkästchen "Protokoll beibehalten"][ImagePreserveLogCheckBox]  

### <span data-ttu-id="6fc3d-126">Aufzeichnen von Screenshots beim Laden der Seite</span><span class="sxs-lookup"><span data-stu-id="6fc3d-126">Capture screenshots during page load</span></span>   

<span data-ttu-id="6fc3d-127">Erfassen Sie Screenshots, um zu analysieren, was die Benutzer sehen, während Sie auf Ihre Seite warten, um Sie zu laden.</span><span class="sxs-lookup"><span data-stu-id="6fc3d-127">Capture screenshots to analyze what users see as they wait for your page to load.</span></span>  

<span data-ttu-id="6fc3d-128">Wenn Sie Screenshots aktivieren möchten, wählen Sie **Netzwerkeinstellungen** und dann auf der Registerkarte **Netzwerk** das Kontrollkästchen **Screenshots aufzeichnen** aus.</span><span class="sxs-lookup"><span data-stu-id="6fc3d-128">To enable screenshots, select **Network settings** and select **Capture screenshots** checkbox on the **Network** panel.</span></span>  

<span data-ttu-id="6fc3d-129">Laden Sie die Seite neu, während sich das **Netzwerk** Panel im Fokus befindet, um Screenshots zu erfassen.</span><span class="sxs-lookup"><span data-stu-id="6fc3d-129">Reload the page while the **Network** panel is in focus to capture screenshots.</span></span>  

<span data-ttu-id="6fc3d-130">Nachdem Sie einen Screenshot aufgezeichnet haben, interagieren Sie mit ihm auf die folgende Weise.</span><span class="sxs-lookup"><span data-stu-id="6fc3d-130">After capturing a screenshot, you interact with it in the following ways.</span></span>  

*   <span data-ttu-id="6fc3d-131">Zeigen Sie mit der Maus auf einen Screenshot, um den Punkt anzuzeigen, an dem dieser Screenshot aufgenommen wurde.</span><span class="sxs-lookup"><span data-stu-id="6fc3d-131">Hover over a screenshot to view the point at which that screenshot was captured.</span></span>  <span data-ttu-id="6fc3d-132">Im Bereich " **Übersicht** " wird eine gelbe Zeile angezeigt.</span><span class="sxs-lookup"><span data-stu-id="6fc3d-132">A yellow line appears on the **Overview** pane.</span></span>  
*   <span data-ttu-id="6fc3d-133">Wählen Sie die Miniaturansicht eines Bildschirms aus, um alle Anforderungen zu filtern, die nach dem Erfassen des Screenshots aufgetreten sind.</span><span class="sxs-lookup"><span data-stu-id="6fc3d-133">Select the thumbnail of a screen to filter out any requests that occurred after the screenshot was captured.</span></span>  
*   <span data-ttu-id="6fc3d-134">Doppelklicken Sie auf eine Miniaturansicht, um Sie zu vergrößern.</span><span class="sxs-lookup"><span data-stu-id="6fc3d-134">Double-click a thumbnail to zoom in on it.</span></span>  

> ##### <span data-ttu-id="6fc3d-135">Abbildung4</span><span class="sxs-lookup"><span data-stu-id="6fc3d-135">Figure 4</span></span>  
> <span data-ttu-id="6fc3d-136">Zeigen auf einen Screenshot</span><span class="sxs-lookup"><span data-stu-id="6fc3d-136">Hovering over a screenshot</span></span>  
> ![Zeigen auf einen Screenshot][ImageScreenshotHover]  

<!--  ### Replay XHR request   -->

<!--  To replay an XHR request, right-click the request in the Requests table and select **Replay XHR**.  -->

<!--  
> ##### Old Figure 5  
> Selecting Replay XHR  
> ![Selecting Replay XHR][ImageReplayXHR]  
-->  

## <span data-ttu-id="6fc3d-138">Ändern des Ladeverhaltens</span><span class="sxs-lookup"><span data-stu-id="6fc3d-138">Change loading behavior</span></span>  

### <span data-ttu-id="6fc3d-139">Emulieren eines erstmaligen Besuchers durch Deaktivieren des Browsercaches</span><span class="sxs-lookup"><span data-stu-id="6fc3d-139">Emulate a first-time visitor by disabling the browser cache</span></span>   

<span data-ttu-id="6fc3d-140">Aktivieren Sie das Kontrollkästchen **Cache deaktivieren** , um zu emulieren, wie ein Erstbenutzer Ihre Website erlebt.</span><span class="sxs-lookup"><span data-stu-id="6fc3d-140">To emulate how a first-time user experiences your site, check the **Disable cache** checkbox.</span></span>  <span data-ttu-id="6fc3d-141">DevTools deaktiviert den Browsercache.</span><span class="sxs-lookup"><span data-stu-id="6fc3d-141">DevTools disables the browser cache.</span></span>  <span data-ttu-id="6fc3d-142">Dadurch wird die Benutzererfahrung des ersten Benutzers genauer emuliert, da Anforderungen im Browsercache bei wiederholten Besuchen bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="6fc3d-142">This more accurately emulates a first-time user's experience, because requests are served from the browser cache on repeat visits.</span></span>  

> ##### <span data-ttu-id="6fc3d-143">Abbildung5</span><span class="sxs-lookup"><span data-stu-id="6fc3d-143">Figure 5</span></span>  
> <span data-ttu-id="6fc3d-144">Kontrollkästchen "Cache deaktivieren"</span><span class="sxs-lookup"><span data-stu-id="6fc3d-144">The Disable Cache checkbox</span></span>  
> <span data-ttu-id="6fc3d-145">! [Das Kontrollkästchen Cache deaktivieren] [ImageDisableCacheCheckBox]</span><span class="sxs-lookup"><span data-stu-id="6fc3d-145">![The Disable Cache checkbox][ImageDisableCacheCheckBox]</span></span>  

#### <span data-ttu-id="6fc3d-146">Deaktivieren des Browser-Caches aus der Schublade "Netzwerkbedingungen"</span><span class="sxs-lookup"><span data-stu-id="6fc3d-146">Disable the browser cache from the Network Conditions drawer</span></span>   

<span data-ttu-id="6fc3d-147">Wenn Sie den Cache während der Arbeit in anderen devtools-Panels deaktivieren möchten, verwenden Sie die Schublade Netzwerkbedingungen.</span><span class="sxs-lookup"><span data-stu-id="6fc3d-147">If you want to disable the cache while working in other DevTools panels, use the Network Conditions drawer.</span></span>  

1.  <span data-ttu-id="6fc3d-148">Öffnen Sie die Schublade **Netzwerkbedingungen** .</span><span class="sxs-lookup"><span data-stu-id="6fc3d-148">Open the **Network Conditions** drawer.</span></span>  
1.  <span data-ttu-id="6fc3d-149">Aktivieren oder deaktivieren Sie das Kontrollkästchen **Cache deaktivieren** .</span><span class="sxs-lookup"><span data-stu-id="6fc3d-149">Check or uncheck the **Disable cache** checkbox.</span></span>  

<!--todo: add network condition section when available -->  

### <span data-ttu-id="6fc3d-150">Manuelles Löschen des Browsercaches</span><span class="sxs-lookup"><span data-stu-id="6fc3d-150">Manually clear the browser cache</span></span>   

<span data-ttu-id="6fc3d-151">Wenn Sie den Browser-Cache jederzeit manuell löschen möchten, klicken Sie mit der rechten Maustaste auf eine beliebige Stelle in der Tabelle Anforderungen, und wählen Sie **Browsercache löschen**aus.</span><span class="sxs-lookup"><span data-stu-id="6fc3d-151">To manually clear the browser cache at any time, right-click anywhere in the Requests table and select **Clear Browser Cache**.</span></span>  

> ##### <span data-ttu-id="6fc3d-152">Abbildung6</span><span class="sxs-lookup"><span data-stu-id="6fc3d-152">Figure 6</span></span>  
> <span data-ttu-id="6fc3d-153">Auswählen des Browser Cache löschen</span><span class="sxs-lookup"><span data-stu-id="6fc3d-153">Selecting Clear Browser Cache</span></span>  
> <span data-ttu-id="6fc3d-154">! [Auswahl löschen des Browser Caches] [ImageClearBrowserCache]</span><span class="sxs-lookup"><span data-stu-id="6fc3d-154">![Selecting Clear Browser Cache][ImageClearBrowserCache]</span></span>  

### <span data-ttu-id="6fc3d-155">Offline emulieren</span><span class="sxs-lookup"><span data-stu-id="6fc3d-155">Emulate offline</span></span>   

<span data-ttu-id="6fc3d-156">Eine neue Klasse von Web-Apps, so genannte [Progressive Web-Apps][DevtoolsProgressiveWebApps], funktioniert mit Hilfe von **Servicemitarbeitern**offline.</span><span class="sxs-lookup"><span data-stu-id="6fc3d-156">A new class of web apps, called [Progressive Web Apps][DevtoolsProgressiveWebApps], functions offline with the help of **service workers**.</span></span>  <span data-ttu-id="6fc3d-157">Möglicherweise ist es hilfreich, ein Gerät, das keine Datenverbindung aufweist, schnell zu simulieren, wenn Sie diese Art von App erstellen.</span><span class="sxs-lookup"><span data-stu-id="6fc3d-157">You may find it useful to quickly simulate a device that has no data connection when you are building this type of app.</span></span>  

<!--[ServiceWorkers]: /web/fundamentals/getting-started/primers/service-workers  -->

<span data-ttu-id="6fc3d-158">Wählen Sie das Dropdownmenü **Online** aus, suchen Sie unter **Voreinstellungen**, und wählen Sie **Offline** aus, um eine vollständig Offlinenetzwerk Umgebung zu simulieren.</span><span class="sxs-lookup"><span data-stu-id="6fc3d-158">Select the **Online** dropdown menu, search under **Presets**, and select **Offline** to simulate a completely offline network experience.</span></span>  

> ##### <span data-ttu-id="6fc3d-159">Abbildung7</span><span class="sxs-lookup"><span data-stu-id="6fc3d-159">Figure 7</span></span>  
> <span data-ttu-id="6fc3d-160">Das Offline-Dropdownmenü</span><span class="sxs-lookup"><span data-stu-id="6fc3d-160">The Offline dropdown menu</span></span>  
> <span data-ttu-id="6fc3d-161">! [Das Offline-Dropdownmenü] [ImageOfflineDropdown]</span><span class="sxs-lookup"><span data-stu-id="6fc3d-161">![The Offline dropdown menu][ImageOfflineDropdown]</span></span>  

### <span data-ttu-id="6fc3d-162">Emulieren langsamer Netzwerkverbindungen</span><span class="sxs-lookup"><span data-stu-id="6fc3d-162">Emulate slow network connections</span></span>   

<span data-ttu-id="6fc3d-163">Emulieren Sie langsames 3G, fast 3G und andere Verbindungsgeschwindigkeiten über das **Online-Dropdown-** Menü.</span><span class="sxs-lookup"><span data-stu-id="6fc3d-163">Emulate Slow 3G, Fast 3G, and other connection speeds from the **Online** dropdown menu.</span></span>  

> ##### <span data-ttu-id="6fc3d-164">Abbildung8</span><span class="sxs-lookup"><span data-stu-id="6fc3d-164">Figure 8</span></span>  
> <span data-ttu-id="6fc3d-165">Dropdownmenü "Drosselung"</span><span class="sxs-lookup"><span data-stu-id="6fc3d-165">The Throttling dropdown menu</span></span>  
> <span data-ttu-id="6fc3d-166">! [Das Dropdownmenü ' Drosselung '] [ImageNetworkThrottlingMenu]</span><span class="sxs-lookup"><span data-stu-id="6fc3d-166">![The Throttling dropdown menu][ImageNetworkThrottlingMenu]</span></span>  

<span data-ttu-id="6fc3d-167">Sie können aus einer Vielzahl von Voreinstellungen auswählen, wie etwa langsames 3G oder fast 3G.</span><span class="sxs-lookup"><span data-stu-id="6fc3d-167">You may select from a variety of presets, such as Slow 3G or Fast 3G.</span></span>  <span data-ttu-id="6fc3d-168">Sie können auch eigene benutzerdefinierte Voreinstellungen hinzufügen, indem Sie das Menü Drosselung öffnen und **benutzerdefiniertes**  >  **Add**auswählen.</span><span class="sxs-lookup"><span data-stu-id="6fc3d-168">You may also add your own custom presets by opening the Throttling menu and selecting **Custom** > **Add**.</span></span>  

<span data-ttu-id="6fc3d-169">DevTools zeigt ein Warnungssymbol neben der Registerkarte " **Netzwerk** " an, um Sie daran zu erinnern, dass die Drosselung aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="6fc3d-169">DevTools displays a warning icon next to the **Network** tab to remind you that throttling is enabled.</span></span>  

#### <span data-ttu-id="6fc3d-170">Emulieren von langsamen Netzwerkverbindungen über die Netzwerkbedingungen Schublade</span><span class="sxs-lookup"><span data-stu-id="6fc3d-170">Emulate slow network connections from the Network Conditions drawer</span></span>   

<span data-ttu-id="6fc3d-171">Wenn Sie die Netzwerkverbindung während der Arbeit in anderen devtools-Panels Drosseln möchten, verwenden Sie den Netzwerkbedingungen-Einzug.</span><span class="sxs-lookup"><span data-stu-id="6fc3d-171">If you want to throttle the network connection while working in other DevTools panels, use the Network Conditions drawer.</span></span>  

1.  <span data-ttu-id="6fc3d-172">Öffnen Sie die Schublade **Netzwerkbedingungen** .</span><span class="sxs-lookup"><span data-stu-id="6fc3d-172">Open the **Network Conditions** drawer.</span></span>  
1.  <span data-ttu-id="6fc3d-173">Wählen Sie die gewünschte Verbindungsgeschwindigkeit im Menü " **Drosselung** " aus.</span><span class="sxs-lookup"><span data-stu-id="6fc3d-173">Select your desired connection speed from the **Throttling** menu.</span></span>  

<!--todo: add network condition section when available -->  

### <span data-ttu-id="6fc3d-174">Manuelles Löschen von Browser-Cookies</span><span class="sxs-lookup"><span data-stu-id="6fc3d-174">Manually clear browser cookies</span></span>   

<span data-ttu-id="6fc3d-175">Wenn Sie Browser-Cookies jederzeit manuell löschen möchten, klicken Sie mit der rechten Maustaste auf eine beliebige Stelle in der Tabelle Anforderungen, und wählen Sie **Browser-Cookies löschen**aus.</span><span class="sxs-lookup"><span data-stu-id="6fc3d-175">To manually clear browser cookies at any time, right-click anywhere in the Requests table and select **Clear Browser Cookies**.</span></span>  

> ##### <span data-ttu-id="6fc3d-176">Abbildung 9</span><span class="sxs-lookup"><span data-stu-id="6fc3d-176">Figure 9</span></span>  
> <span data-ttu-id="6fc3d-177">Auswählen von Browser-Cookies löschen</span><span class="sxs-lookup"><span data-stu-id="6fc3d-177">Selecting Clear Browser Cookies</span></span>  
> <span data-ttu-id="6fc3d-178">! [Auswahl von Browser-Cookies löschen] [ImageClearBrowserCookies]</span><span class="sxs-lookup"><span data-stu-id="6fc3d-178">![Selecting Clear Browser Cookies][ImageClearBrowserCookies]</span></span>  

### <span data-ttu-id="6fc3d-179">Überschreiben des Benutzer-Agents</span><span class="sxs-lookup"><span data-stu-id="6fc3d-179">Override the user agent</span></span>   

<span data-ttu-id="6fc3d-180">So überschreiben Sie den Benutzer-Agent manuell:</span><span class="sxs-lookup"><span data-stu-id="6fc3d-180">To manually override the user agent:</span></span>  

1.  <span data-ttu-id="6fc3d-181">Öffnen Sie die Schublade **Netzwerkbedingungen** .</span><span class="sxs-lookup"><span data-stu-id="6fc3d-181">Open the **Network Conditions** drawer.</span></span>  
1.  <span data-ttu-id="6fc3d-182">Deaktivieren **Sie SELECT automatisch**.</span><span class="sxs-lookup"><span data-stu-id="6fc3d-182">Uncheck **Select automatically**.</span></span>  
1.  <span data-ttu-id="6fc3d-183">Wählen Sie eine Option für den Benutzer-Agent aus dem Menü aus, oder geben Sie eine benutzerdefinierte Option in das Textfeld ein.</span><span class="sxs-lookup"><span data-stu-id="6fc3d-183">Choose a user agent option from the menu, or enter a custom one in the text box.</span></span>  

<!--todo: add network condition section when available -->  

## <span data-ttu-id="6fc3d-184">Filter Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6fc3d-184">Filter requests</span></span>   

### <span data-ttu-id="6fc3d-185">Filtern von Anforderungen nach Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6fc3d-185">Filter requests by properties</span></span>   

<span data-ttu-id="6fc3d-186">Verwenden Sie das Textfeld **Filtern** , um Anforderungen nach Eigenschaften wie der Domäne oder der Größe der Anforderung zu filtern.</span><span class="sxs-lookup"><span data-stu-id="6fc3d-186">Use the **Filter** text box to filter requests by properties, such as the domain or size of the request.</span></span>  

<span data-ttu-id="6fc3d-187">Wenn das Textfeld nicht angezeigt wird, ist der Bereich Filter wahrscheinlich ausgeblendet.</span><span class="sxs-lookup"><span data-stu-id="6fc3d-187">If you do not see the text box, the Filters pane is probably hidden.</span></span>  
<span data-ttu-id="6fc3d-188">Weitere Informationen finden Sie unter [Ausblenden des Filters-Bereichs](#hide-the-filters-pane).</span><span class="sxs-lookup"><span data-stu-id="6fc3d-188">See [Hide the Filters pane](#hide-the-filters-pane).</span></span>  

> ##### <span data-ttu-id="6fc3d-189">Abbildung 10</span><span class="sxs-lookup"><span data-stu-id="6fc3d-189">Figure 10</span></span>  
> <span data-ttu-id="6fc3d-190">Das Textfeld "Filter"</span><span class="sxs-lookup"><span data-stu-id="6fc3d-190">The Filters text box</span></span>  
> <span data-ttu-id="6fc3d-191">! [Das Textfeld "Filter"] [ImageFilterTextBox]</span><span class="sxs-lookup"><span data-stu-id="6fc3d-191">![The Filters text box][ImageFilterTextBox]</span></span>  

<span data-ttu-id="6fc3d-192">Sie können mehrere Eigenschaften gleichzeitig verwenden, indem Sie jede Eigenschaft mit einem Leerzeichen voneinander trennen.</span><span class="sxs-lookup"><span data-stu-id="6fc3d-192">You may use multiple properties simultaneously by separating each property with a space.</span></span>  <span data-ttu-id="6fc3d-193">Zeigt beispielsweise `mime-type:image/png larger-than:1K` alle PNGs an, die größer als ein Kilobyte sind.</span><span class="sxs-lookup"><span data-stu-id="6fc3d-193">For example, `mime-type:image/png larger-than:1K` displays all PNGs that are larger than one kilobyte.</span></span>  <span data-ttu-id="6fc3d-194">Diese Filter mit mehreren Eigenschaften sind äquivalent zu `AND` Vorgängen.</span><span class="sxs-lookup"><span data-stu-id="6fc3d-194">These multi-property filters are equivalent to `AND` operations.</span></span>  `OR` <span data-ttu-id="6fc3d-195">Vorgänge werden zurzeit nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="6fc3d-195">operations are currently not supported.</span></span>  

<span data-ttu-id="6fc3d-196">Die vollständige Liste der unterstützten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="6fc3d-196">The complete list of supported properties.</span></span>  

| <span data-ttu-id="6fc3d-197">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="6fc3d-197">Property</span></span> | <span data-ttu-id="6fc3d-198">Details</span><span class="sxs-lookup"><span data-stu-id="6fc3d-198">Details</span></span> |  
|:--- | :--- |  
| `domain` | <span data-ttu-id="6fc3d-199">Zeigt nur Ressourcen aus der angegebenen Domäne an.</span><span class="sxs-lookup"><span data-stu-id="6fc3d-199">Only display resources from the specified domain.</span></span>  <span data-ttu-id="6fc3d-200">Sie können ein Platzhalterzeichen \ ( `*` \) verwenden, um mehrere Domänen einzubeziehen.</span><span class="sxs-lookup"><span data-stu-id="6fc3d-200">You may use a wildcard character \(`*`\) to include multiple domains.</span></span>  <span data-ttu-id="6fc3d-201">Zeigt beispielsweise `*.com` Ressourcen aus allen Domänennamen an, die in endet `.com` .</span><span class="sxs-lookup"><span data-stu-id="6fc3d-201">For example, `*.com` displays resources from all domain names ending in `.com`.</span></span>  <span data-ttu-id="6fc3d-202">DevTools füllt das Dropdownmenü AutoVervollständigen mit allen Domänen auf, die es gefunden hat.</span><span class="sxs-lookup"><span data-stu-id="6fc3d-202">DevTools populates the autocomplete dropdown menu with all of the domains it has encountered.</span></span> |  
| `has-response-header` | <span data-ttu-id="6fc3d-203">Anzeigen der Ressourcen, die den angegebenen HTTP-Antwortheader enthalten</span><span class="sxs-lookup"><span data-stu-id="6fc3d-203">Show the resources that contain the specified HTTP response header.</span></span>  <span data-ttu-id="6fc3d-204">DevTools füllt die Dropdownliste AutoVervollständigen mit allen Antwortheadern auf, die Sie gefunden hat.</span><span class="sxs-lookup"><span data-stu-id="6fc3d-204">DevTools populates the autocomplete dropdown with all of the response headers that it has encountered.</span></span> |  
| `is` | <span data-ttu-id="6fc3d-205">Verwendet `is:running` , um `WebSocket` Ressourcen zu finden.</span><span class="sxs-lookup"><span data-stu-id="6fc3d-205">Use `is:running` to find `WebSocket` resources.</span></span> |  
| `larger-than` | <span data-ttu-id="6fc3d-206">Zeigen Sie Ressourcen an, die größer als die angegebene Größe in Bytes sind.</span><span class="sxs-lookup"><span data-stu-id="6fc3d-206">Show resources that are larger than the specified size, in bytes.</span></span>  <span data-ttu-id="6fc3d-207">Das Festlegen eines Werts von entspricht dem `1000` Festlegen eines Werts von `1k` .</span><span class="sxs-lookup"><span data-stu-id="6fc3d-207">Setting a value of `1000` is equivalent to setting a value of `1k`.</span></span> |  
| `method` | <span data-ttu-id="6fc3d-208">Zeigen Sie Ressourcen an, die über einen angegebenen http-Methodentyp abgerufen wurden.</span><span class="sxs-lookup"><span data-stu-id="6fc3d-208">Show resources that were retrieved over a specified HTTP method type.</span></span>  <span data-ttu-id="6fc3d-209">DevTools füllt die Dropdownliste mit allen HTTP-Methoden auf, die Sie gefunden hat.</span><span class="sxs-lookup"><span data-stu-id="6fc3d-209">DevTools populates the dropdown with all of the HTTP methods it has encountered.</span></span> |  
| `mime-type` | <span data-ttu-id="6fc3d-210">Anzeigen von Ressourcen eines angegebenen MIME-Typs</span><span class="sxs-lookup"><span data-stu-id="6fc3d-210">Show resources of a specified MIME type.</span></span>  <span data-ttu-id="6fc3d-211">DevTools füllt die Dropdownliste mit allen MIME-Typen auf, die Sie gefunden hat.</span><span class="sxs-lookup"><span data-stu-id="6fc3d-211">DevTools populates the dropdown with all MIME types it has encountered.</span></span> |  
| `mixed-content` | <span data-ttu-id="6fc3d-212">Alle gemischten Inhalts Ressourcen anzeigen \ ( `mixed-content:all` \) oder nur diejenigen, die aktuell angezeigt werden \ ( `mixed-content:displayed` \).</span><span class="sxs-lookup"><span data-stu-id="6fc3d-212">Show all mixed content resources \(`mixed-content:all`\) or just the ones that are currently displayed \(`mixed-content:displayed`\).</span></span> |  
| `scheme` | <span data-ttu-id="6fc3d-213">Zeigt Ressourcen an, die über ungeschützten http \ ( `scheme:http` \) oder geschütztes HTTPS \ ( `scheme:https` \) abgerufen wurden.</span><span class="sxs-lookup"><span data-stu-id="6fc3d-213">Show resources retrieved over unprotected HTTP \(`scheme:http`\) or protected HTTPS \(`scheme:https`\).</span></span> |  
| `set-cookie-domain` | <span data-ttu-id="6fc3d-214">Zeigen Sie die Ressourcen mit einer `Set-Cookie` Kopfzeile mit einem `Domain` Attribut an, das dem angegebenen Wert entspricht.</span><span class="sxs-lookup"><span data-stu-id="6fc3d-214">Show the resources that have a `Set-Cookie` header with a `Domain` attribute that matches the specified value.</span></span>  <span data-ttu-id="6fc3d-215">DevTools füllt das AutoVervollständigen mit allen Cookie-Domänen auf, die es gefunden hat.</span><span class="sxs-lookup"><span data-stu-id="6fc3d-215">DevTools populates the autocomplete with all of the cookie domains that it has encountered.</span></span> |  
| `set-cookie-name` | <span data-ttu-id="6fc3d-216">Zeigen Sie die Ressourcen mit einer `Set-Cookie` Kopfzeile mit einem Namen an, der dem angegebenen Wert entspricht.</span><span class="sxs-lookup"><span data-stu-id="6fc3d-216">Show the resources that have a `Set-Cookie` header with a name that matches the specified value.</span></span>  <span data-ttu-id="6fc3d-217">DevTools füllt das AutoVervollständigen mit allen Cookie-Namen auf, die es gefunden hat.</span><span class="sxs-lookup"><span data-stu-id="6fc3d-217">DevTools populates the autocomplete with all of the cookie names that it has encountered.</span></span> |  
| `set-cookie-value` | <span data-ttu-id="6fc3d-218">Zeigen Sie die Ressourcen mit einer `Set-Cookie` Kopfzeile mit einem Wert an, der dem angegebenen Wert entspricht.</span><span class="sxs-lookup"><span data-stu-id="6fc3d-218">Show the resources that have a `Set-Cookie` header with a value that matches the specified value.</span></span>  <span data-ttu-id="6fc3d-219">DevTools füllt das AutoVervollständigen mit allen Cookie-Werten auf, die es gefunden hat.</span><span class="sxs-lookup"><span data-stu-id="6fc3d-219">DevTools populates the autocomplete with all of the cookie values that it has encountered.</span></span> |  
| `status-code` | <span data-ttu-id="6fc3d-220">Nur die Ressourcen anzeigen, für die der HTTP-Statuscode mit dem angegebenen Code übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="6fc3d-220">Show only the resources for which the HTTP status code matches the specified code.</span></span>  <span data-ttu-id="6fc3d-221">DevTools füllt das Dropdownmenü AutoVervollständigen mit allen Statuscodes auf, die es gefunden hat.</span><span class="sxs-lookup"><span data-stu-id="6fc3d-221">DevTools populates the autocomplete dropdown menu with all of the status codes it has encountered.</span></span> |  

### <span data-ttu-id="6fc3d-222">Filtern von Anforderungen nach Typ</span><span class="sxs-lookup"><span data-stu-id="6fc3d-222">Filter requests by type</span></span>   

<span data-ttu-id="6fc3d-223">Wenn Sie Anforderungen nach Anforderungsfiltern möchten, wählen Sie die Schaltflächen **XMLHttpRequest**, **js**, **CSS**, **IMG**, **Media**, **Font**, **doc**, **WS** \ (WebSocket \), **Manifest**oder **andere** \ (alle anderen Typen, die hier nicht aufgelistet sind) im Netzwerk Panel aus.</span><span class="sxs-lookup"><span data-stu-id="6fc3d-223">To filter requests by request type, select the **XHR**, **JS**, **CSS**, **Img**, **Media**, **Font**, **Doc**, **WS** \(WebSocket\), **Manifest**, or **Other** \(any other type not listed here\) buttons on the Network panel.</span></span>  

<span data-ttu-id="6fc3d-224">Wenn diese Schaltflächen nicht angezeigt werden, ist der Bereich Filter wahrscheinlich ausgeblendet.</span><span class="sxs-lookup"><span data-stu-id="6fc3d-224">If you do not see these buttons, the Filters pane is probably hidden.</span></span>  
<span data-ttu-id="6fc3d-225">Weitere Informationen finden Sie unter [Ausblenden des Filters-Bereichs](#hide-the-filters-pane).</span><span class="sxs-lookup"><span data-stu-id="6fc3d-225">See [Hide the Filters pane](#hide-the-filters-pane).</span></span>  

<span data-ttu-id="6fc3d-226">Wenn Sie mehrere Typfilter gleichzeitig aktivieren möchten, halten `Control` Sie \ (Windows \) oder `Command` \ (macOS \) gedrückt, und wählen Sie dann aus.</span><span class="sxs-lookup"><span data-stu-id="6fc3d-226">To enable multiple type filters simultaneously, hold `Control` \(Windows\) or `Command` \(macOS\) and then select.</span></span>  

> ##### <span data-ttu-id="6fc3d-227">Abbildung 11</span><span class="sxs-lookup"><span data-stu-id="6fc3d-227">Figure 11</span></span>  
> <span data-ttu-id="6fc3d-228">Verwenden des Typs "Filter" zum Anzeigen von JS-, CSS-und Dokument Ressourcen</span><span class="sxs-lookup"><span data-stu-id="6fc3d-228">Using the Type filters to display JS, CSS, and Document resources</span></span>  
> <span data-ttu-id="6fc3d-229">! [Verwenden der Typen Filter zum Anzeigen von JS-, CSS-und Dokument Ressourcen] [ImageMultiTypeFilter]</span><span class="sxs-lookup"><span data-stu-id="6fc3d-229">![Using the Type filters to display JS, CSS, and Document resources][ImageMultiTypeFilter]</span></span>  

### <span data-ttu-id="6fc3d-230">Filtern von Anforderungen nach Zeit</span><span class="sxs-lookup"><span data-stu-id="6fc3d-230">Filter requests by time</span></span>   

<span data-ttu-id="6fc3d-231">Wählen Sie aus, und ziehen Sie im Übersichtsbereich nach links oder rechts, um nur Anforderungen anzuzeigen, die während dieses Zeitrahmens aktiv waren.</span><span class="sxs-lookup"><span data-stu-id="6fc3d-231">Select and drag left or right on the Overview pane to only display requests that were active during that time frame.</span></span>  <span data-ttu-id="6fc3d-232">Der Filter ist inklusive.</span><span class="sxs-lookup"><span data-stu-id="6fc3d-232">The filter is inclusive.</span></span>  <span data-ttu-id="6fc3d-233">Jede Anforderung, die während der hervorgehobenen Zeit aktiv war, wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="6fc3d-233">Any request that was active during the highlighted time is shown.</span></span>  

> ##### <span data-ttu-id="6fc3d-234">Abbildung 12</span><span class="sxs-lookup"><span data-stu-id="6fc3d-234">Figure 12</span></span>  
> <span data-ttu-id="6fc3d-235">Herausfiltern von Anforderungen, die um 300 m inaktiv waren</span><span class="sxs-lookup"><span data-stu-id="6fc3d-235">Filtering out any requests that were inactive around 300ms</span></span>  
> <span data-ttu-id="6fc3d-236">! [Filtert alle Anforderungen, die um 300 m inaktiv waren] [ImageOverviewFilter]</span><span class="sxs-lookup"><span data-stu-id="6fc3d-236">![Filtering out any requests that were inactive around 300ms][ImageOverviewFilter]</span></span>  

### <span data-ttu-id="6fc3d-237">Ausblenden von Daten-URLs</span><span class="sxs-lookup"><span data-stu-id="6fc3d-237">Hide data URLs</span></span>  

<span data-ttu-id="6fc3d-238">[Daten-URLs][MDNHTTPDataURIs] sind kleine Dateien, die in andere Dokumente eingebettet sind.</span><span class="sxs-lookup"><span data-stu-id="6fc3d-238">[Data URLs][MDNHTTPDataURIs] are small files embedded into other documents.</span></span>  <span data-ttu-id="6fc3d-239">Jede Anforderung, die Sie in der Tabelle Anforderungen sehen, die mit beginnt, `data:` ist eine Daten-URL.</span><span class="sxs-lookup"><span data-stu-id="6fc3d-239">Any request that you see in the Requests table that starts with `data:` is a data URL.</span></span>  

<span data-ttu-id="6fc3d-240">Aktivieren Sie das Kontrollkästchen **Daten-URLs ausblenden** , um diese Anforderungen auszublenden.</span><span class="sxs-lookup"><span data-stu-id="6fc3d-240">Check the **Hide data URLs** checkbox to hide these requests.</span></span>  

> ##### <span data-ttu-id="6fc3d-241">Abbildung 13</span><span class="sxs-lookup"><span data-stu-id="6fc3d-241">Figure 13</span></span>  
> <span data-ttu-id="6fc3d-242">Das Kontrollkästchen "Daten-URLs ausblenden"</span><span class="sxs-lookup"><span data-stu-id="6fc3d-242">The Hide Data URLs checkbox</span></span>  
> <span data-ttu-id="6fc3d-243">! [Das Kontrollkästchen ' Daten-URLs ausblenden '] [ImageHideDataURLsCheckBox]</span><span class="sxs-lookup"><span data-stu-id="6fc3d-243">![The Hide Data URLs checkbox][ImageHideDataURLsCheckBox]</span></span>  

## <span data-ttu-id="6fc3d-244">Sortieren von Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6fc3d-244">Sort requests</span></span>  

<span data-ttu-id="6fc3d-245">Standardmäßig werden die Anforderungen in der Tabelle Anforderungen nach Initiierungs Zeit sortiert, aber Sie können die Tabelle mit anderen Kriterien sortieren.</span><span class="sxs-lookup"><span data-stu-id="6fc3d-245">By default, the requests in the Requests table are sorted by initiation time, but you may sort the table using other criteria.</span></span>  

### <span data-ttu-id="6fc3d-246">Nach Spalte sortieren</span><span class="sxs-lookup"><span data-stu-id="6fc3d-246">Sort by column</span></span>   

<span data-ttu-id="6fc3d-247">Wählen Sie die Kopfzeile einer beliebigen Spalte in den Anforderungen aus, um Anforderungen nach dieser Spalte zu sortieren.</span><span class="sxs-lookup"><span data-stu-id="6fc3d-247">Select the header of any column in the Requests to sort requests by that column.</span></span>  

### <span data-ttu-id="6fc3d-248">Nach Aktivitätsphase sortieren</span><span class="sxs-lookup"><span data-stu-id="6fc3d-248">Sort by activity phase</span></span>   

<span data-ttu-id="6fc3d-249">Wenn Sie ändern möchten, wie der Wasserfall Anforderungen sortiert, klicken Sie mit der rechten Maustaste auf die Kopfzeile der Tabelle Anforderungen, zeigen Sie mit dem Mauszeiger auf **Wasserfall**, und wählen Sie eine der folgenden Optionen aus.</span><span class="sxs-lookup"><span data-stu-id="6fc3d-249">To change how the Waterfall sorts requests, right-click the header of the Requests table, hover over **Waterfall**, and select one of the following options.</span></span>  

*   <span data-ttu-id="6fc3d-250">**Startzeit**.</span><span class="sxs-lookup"><span data-stu-id="6fc3d-250">**Start Time**.</span></span>  <span data-ttu-id="6fc3d-251">Die erste Anforderung, die initiiert wurde, ist oben.</span><span class="sxs-lookup"><span data-stu-id="6fc3d-251">The first request that was initiated is at the top.</span></span>  
*   <span data-ttu-id="6fc3d-252">**Antwortzeit**.</span><span class="sxs-lookup"><span data-stu-id="6fc3d-252">**Response Time**.</span></span>  <span data-ttu-id="6fc3d-253">Die erste Anforderung, die den Download begonnen hat, ist ganz oben.</span><span class="sxs-lookup"><span data-stu-id="6fc3d-253">The first request that started downloading is at the top.</span></span>  
*   <span data-ttu-id="6fc3d-254">**Endzeit**.</span><span class="sxs-lookup"><span data-stu-id="6fc3d-254">**End Time**.</span></span>  <span data-ttu-id="6fc3d-255">Die erste abgeschlossene Anforderung ist oben.</span><span class="sxs-lookup"><span data-stu-id="6fc3d-255">The first request that finished is at the top.</span></span>  
*   <span data-ttu-id="6fc3d-256">**Gesamtdauer**.</span><span class="sxs-lookup"><span data-stu-id="6fc3d-256">**Total Duration**.</span></span>  <span data-ttu-id="6fc3d-257">Die Anforderung mit der kürzesten Verbindungseinrichtung und Anforderung/Antwort ist oben.</span><span class="sxs-lookup"><span data-stu-id="6fc3d-257">The request with the shortest connection setup and request / response is at the top.</span></span>  
*   <span data-ttu-id="6fc3d-258">**Latenz**.</span><span class="sxs-lookup"><span data-stu-id="6fc3d-258">**Latency**.</span></span>  <span data-ttu-id="6fc3d-259">Die Anforderung, die die kürzeste Zeit für eine Antwort gewartet hat, ist oben.</span><span class="sxs-lookup"><span data-stu-id="6fc3d-259">The request that waited the shortest time for a response is at the top.</span></span>  

<span data-ttu-id="6fc3d-260">Bei diesen Beschreibungen wird davon ausgegangen, dass die jeweilige Option von kürzester bis längster Position bewertet wird.</span><span class="sxs-lookup"><span data-stu-id="6fc3d-260">These descriptions assume that each respective option is ranked from shortest to longest.</span></span>  <span data-ttu-id="6fc3d-261">Wenn Sie die Kopfzeile der Spalte **Wasserfall** auswählen, wird die Reihenfolge umgekehrt.</span><span class="sxs-lookup"><span data-stu-id="6fc3d-261">Selecting the header of the **Waterfall** column reverses the order.</span></span>  

> ##### <span data-ttu-id="6fc3d-262">Abbildung 14</span><span class="sxs-lookup"><span data-stu-id="6fc3d-262">Figure 14</span></span>  
> <span data-ttu-id="6fc3d-263">Sortieren des Wasserfalls nach Gesamtdauer \ (der leichtere Teil der einzelnen Balken ist die Zeit, die gewartet wird, und der dunklere Teil ist die Zeit, die zum Herunterladen von Bytes verwendet wird \)</span><span class="sxs-lookup"><span data-stu-id="6fc3d-263">Sorting the Waterfall by total duration  \(The lighter portion of each bar is time spent waiting and the darker portion is time spent downloading bytes\)</span></span>  
> <span data-ttu-id="6fc3d-264">! [Sortieren des Wasserfalls nach Gesamtdauer] [ImageWaterfallTotalDuration]</span><span class="sxs-lookup"><span data-stu-id="6fc3d-264">![Sorting the Waterfall by total duration][ImageWaterfallTotalDuration]</span></span>  

## <span data-ttu-id="6fc3d-265">Analysieren von Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6fc3d-265">Analyze requests</span></span>   

<span data-ttu-id="6fc3d-266">Solange devtools geöffnet ist, werden alle Anforderungen im Netzwerk Panel protokolliert.</span><span class="sxs-lookup"><span data-stu-id="6fc3d-266">So long as DevTools is open, it logs all requests in the Network panel.</span></span>  
<span data-ttu-id="6fc3d-267">Verwenden Sie das Netzwerk Panel, um Anforderungen zu analysieren.</span><span class="sxs-lookup"><span data-stu-id="6fc3d-267">Use the Network panel to analyze requests.</span></span>  

### <span data-ttu-id="6fc3d-268">Anzeigen eines Protokolls der Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6fc3d-268">View a log of requests</span></span>   

<span data-ttu-id="6fc3d-269">Verwenden Sie die Tabelle "Anforderungen", um ein Protokoll aller Anforderungen anzuzeigen, die während der devtools geöffnet wurden.</span><span class="sxs-lookup"><span data-stu-id="6fc3d-269">Use the Requests table to view a log of all requests made while DevTools has been open.</span></span>  <span data-ttu-id="6fc3d-270">Wenn Sie über Anforderungen auswählen oder darauf zeigen, werden weitere Informationen zu den einzelnen Elementen eingeblendet.</span><span class="sxs-lookup"><span data-stu-id="6fc3d-270">Selecting or hovering over requests reveals more information about each item.</span></span>  

> ##### <span data-ttu-id="6fc3d-271">Abbildung 15</span><span class="sxs-lookup"><span data-stu-id="6fc3d-271">Figure 15</span></span>  
> <span data-ttu-id="6fc3d-272">Die Tabelle "Anforderungen"</span><span class="sxs-lookup"><span data-stu-id="6fc3d-272">The Requests table</span></span>  
> <span data-ttu-id="6fc3d-273">! [Anfragetabelle] [Imagerequestable]</span><span class="sxs-lookup"><span data-stu-id="6fc3d-273">![The Requests table][ImageRequestsTable]</span></span>  

<span data-ttu-id="6fc3d-274">In der Tabelle "Anforderungen" werden standardmäßig die folgenden Spalten angezeigt:</span><span class="sxs-lookup"><span data-stu-id="6fc3d-274">The Requests table displays the following columns by default:</span></span>  

*   <span data-ttu-id="6fc3d-275">**Name**</span><span class="sxs-lookup"><span data-stu-id="6fc3d-275">**Name**.</span></span>  <span data-ttu-id="6fc3d-276">Der Dateiname von oder ein Bezeichner für die Ressource.</span><span class="sxs-lookup"><span data-stu-id="6fc3d-276">The filename of, or an identifier for, the resource.</span></span>  
*   <span data-ttu-id="6fc3d-277">**Status**aus.</span><span class="sxs-lookup"><span data-stu-id="6fc3d-277">**Status**.</span></span>  <span data-ttu-id="6fc3d-278">Der HTTP-Statuscode.</span><span class="sxs-lookup"><span data-stu-id="6fc3d-278">The HTTP status code.</span></span>  
*   <span data-ttu-id="6fc3d-279">**Typ**.</span><span class="sxs-lookup"><span data-stu-id="6fc3d-279">**Type**.</span></span>  <span data-ttu-id="6fc3d-280">Der MIME-Typ der angeforderten Ressource.</span><span class="sxs-lookup"><span data-stu-id="6fc3d-280">The MIME type of the requested resource.</span></span>  
*   <span data-ttu-id="6fc3d-281">**Initiator**.</span><span class="sxs-lookup"><span data-stu-id="6fc3d-281">**Initiator**.</span></span>  <span data-ttu-id="6fc3d-282">Die folgenden Objekte oder Prozesse initiieren Anforderungen:</span><span class="sxs-lookup"><span data-stu-id="6fc3d-282">The following objects or processes initiate requests:</span></span>  
    *   <span data-ttu-id="6fc3d-283">**Parser**aus.</span><span class="sxs-lookup"><span data-stu-id="6fc3d-283">**Parser**.</span></span>  <span data-ttu-id="6fc3d-284">Der HTML-Parser für Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="6fc3d-284">The HTML parser for Microsoft Edge.</span></span>  
    *   <span data-ttu-id="6fc3d-285">**Umleiten**.</span><span class="sxs-lookup"><span data-stu-id="6fc3d-285">**Redirect**.</span></span>  <span data-ttu-id="6fc3d-286">Eine HTTP-Umleitung.</span><span class="sxs-lookup"><span data-stu-id="6fc3d-286">An HTTP redirect.</span></span>  
    *   <span data-ttu-id="6fc3d-287">**Skript**aus.</span><span class="sxs-lookup"><span data-stu-id="6fc3d-287">**Script**.</span></span>  <span data-ttu-id="6fc3d-288">Eine JavaScript-Funktion.</span><span class="sxs-lookup"><span data-stu-id="6fc3d-288">A JavaScript function.</span></span>  
    *   <span data-ttu-id="6fc3d-289">**Andere**.</span><span class="sxs-lookup"><span data-stu-id="6fc3d-289">**Other**.</span></span>  <span data-ttu-id="6fc3d-290">Einige andere Prozesse oder Aktionen, wie das Navigieren zu einer Seite über einen Link oder das Eingeben einer URL in die Adressleiste.</span><span class="sxs-lookup"><span data-stu-id="6fc3d-290">Some other process or action, such as navigating to a page via a link or entering a URL in the address bar.</span></span>  
*   <span data-ttu-id="6fc3d-291">**Größe**aus.</span><span class="sxs-lookup"><span data-stu-id="6fc3d-291">**Size**.</span></span>  <span data-ttu-id="6fc3d-292">Die kombinierte Größe der Antwortheader sowie des Antworttexts, wie vom Server bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="6fc3d-292">The combined size of the response headers plus the response body, as delivered by the server.</span></span>  
*   <span data-ttu-id="6fc3d-293">**Zeit**.</span><span class="sxs-lookup"><span data-stu-id="6fc3d-293">**Time**.</span></span>  <span data-ttu-id="6fc3d-294">Die Gesamtdauer vom Anfang der Anforderung bis zum Empfang des letzten Bytes in der Antwort.</span><span class="sxs-lookup"><span data-stu-id="6fc3d-294">The total duration, from the start of the request to the receipt of the final byte in the response.</span></span>  
*   <span data-ttu-id="6fc3d-295">[**Wasserfall**](#view-the-timing-of-requests-in-relation-to-one-another).</span><span class="sxs-lookup"><span data-stu-id="6fc3d-295">[**Waterfall**](#view-the-timing-of-requests-in-relation-to-one-another).</span></span>  <span data-ttu-id="6fc3d-296">Eine visuelle Gliederung der Aktivität für jede Anforderung.</span><span class="sxs-lookup"><span data-stu-id="6fc3d-296">A visual breakdown of the activity for each request.</span></span>  

#### <span data-ttu-id="6fc3d-297">Hinzufügen oder Entfernen von Spalten</span><span class="sxs-lookup"><span data-stu-id="6fc3d-297">Add or remove columns</span></span>   

<span data-ttu-id="6fc3d-298">Klicken Sie mit der rechten Maustaste auf die Kopfzeile der Tabelle Anforderungen, und wählen Sie eine Option aus, um sie auszublenden oder anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="6fc3d-298">Right-click the header of the Requests table and select an option to hide or show it.</span></span>  <span data-ttu-id="6fc3d-299">Die aktuell angezeigten Optionen verfügen über Kontrollkästchen neben den einzelnen Elementen.</span><span class="sxs-lookup"><span data-stu-id="6fc3d-299">Currently displayed options have checkmarks next to each item.</span></span>  

> ##### <span data-ttu-id="6fc3d-300">Abbildung 16</span><span class="sxs-lookup"><span data-stu-id="6fc3d-300">Figure 16</span></span>  
> <span data-ttu-id="6fc3d-301">Hinzufügen einer Spalte zur Tabelle "Anforderungen"</span><span class="sxs-lookup"><span data-stu-id="6fc3d-301">Adding a column to the Requests table</span></span>  
> <span data-ttu-id="6fc3d-302">! [Hinzufügen einer Spalte zur Tabelle "Anforderungen"] [ImageRequestsTableAddColumn]</span><span class="sxs-lookup"><span data-stu-id="6fc3d-302">![Adding a column to the Requests table][ImageRequestsTableAddColumn]</span></span>  

#### <span data-ttu-id="6fc3d-303">Hinzufügen benutzerdefinierter Spalten</span><span class="sxs-lookup"><span data-stu-id="6fc3d-303">Add custom columns</span></span>   

<span data-ttu-id="6fc3d-304">Wenn Sie der Tabelle Anforderungen eine benutzerdefinierte Spalte hinzufügen möchten, klicken Sie mit der rechten Maustaste auf die Kopfzeile der Tabelle Anforderungen, und wählen Sie **Antwortheader**  >  **Verwalten von Kopfzeilen Spalten**aus.</span><span class="sxs-lookup"><span data-stu-id="6fc3d-304">To add a custom column to the Requests table, right-click the header of the Requests table and select **Response Headers** > **Manage Header Columns**.</span></span>  

> ##### <span data-ttu-id="6fc3d-305">Abbildung 17</span><span class="sxs-lookup"><span data-stu-id="6fc3d-305">Figure 17</span></span>  
> <span data-ttu-id="6fc3d-306">Hinzufügen einer benutzerdefinierten Spalte zur Tabelle "Anforderungen"</span><span class="sxs-lookup"><span data-stu-id="6fc3d-306">Adding a custom column to the Requests table</span></span>  
> <span data-ttu-id="6fc3d-307">! [Hinzufügen einer benutzerdefinierten Spalte zur Tabelle "Anforderungen"] [ImageRequestsTableCustomColumn]</span><span class="sxs-lookup"><span data-stu-id="6fc3d-307">![Adding a custom column to the Requests table][ImageRequestsTableCustomColumn]</span></span>  

### <span data-ttu-id="6fc3d-308">Anzeigen der Anzeigedauer von Anforderungen im Verhältnis zueinander</span><span class="sxs-lookup"><span data-stu-id="6fc3d-308">View the timing of requests in relation to one another</span></span>   

<span data-ttu-id="6fc3d-309">Verwenden Sie den Wasserfall, um die Anzeigedauer von Anforderungen im Verhältnis zueinander anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="6fc3d-309">Use the Waterfall to view the timing of requests in relation to one another.</span></span>  
<span data-ttu-id="6fc3d-310">Standardmäßig wird der Wasserfall nach dem Anfangszeitpunkt der Anforderungen organisiert.</span><span class="sxs-lookup"><span data-stu-id="6fc3d-310">By default, the Waterfall is organized by the start time of the requests.</span></span>  
<span data-ttu-id="6fc3d-311">Anfragen, die weiter Links sind, wurden früher als die weiter rechts eingegangenen Anforderungen gestartet.</span><span class="sxs-lookup"><span data-stu-id="6fc3d-311">So, requests that are farther to the left started earlier than those that are farther to the right.</span></span>  

<span data-ttu-id="6fc3d-312">Sehen Sie sich die verschiedenen Arten an, wie Sie den Wasserfall sortieren können, [indem Sie nach Aktivitätsphase sortieren](#sort-by-activity-phase) .</span><span class="sxs-lookup"><span data-stu-id="6fc3d-312">See [Sort by activity phase](#sort-by-activity-phase) to see the different ways that you may sort the Waterfall.</span></span>  

> ##### <span data-ttu-id="6fc3d-313">Abbildung 18</span><span class="sxs-lookup"><span data-stu-id="6fc3d-313">Figure 18</span></span>  
> <span data-ttu-id="6fc3d-314">Spalte "Wasserfall" im Bereich "Anforderungen"</span><span class="sxs-lookup"><span data-stu-id="6fc3d-314">The Waterfall column of the Requests pane</span></span>  
> <span data-ttu-id="6fc3d-315">! [Die Wasserfall Spalte des Bereichs ' Anforderungen '] [ImageRequestsTableWaterfallColumn]</span><span class="sxs-lookup"><span data-stu-id="6fc3d-315">![The Waterfall column of the Requests pane][ImageRequestsTableWaterfallColumn]</span></span>  

<!-- ### Analyze the frames of a WebSocket Connection   -->

<!--To view the frames of a WebSocket connection:  

1.  Select the URL of the WebSocket connection, under the **Name** column of the Requests table.  
1.  Select the **Frames** tab.  The table shows the last 100 frames.  

To refresh the table, re-click the name of the WebSocket connection under the **Name** column of the Requests table.  -->

<!--
> ##### Old Figure 20  
> The Frames tab  
> ![The Frames tab][ImageFrames]  
-->

<!--The table contains three columns:  

*   **Data**.  The message payload.  If the message is plain text, it is displayed here.  For binary opcodes, this column displays the name and code of the opcode.  The following opcodes are supported: Continuation Frame, Binary Frame, Connection Close Frame, Ping Frame, and Pong Frame.  
*   **Length**.  The length of the message payload, in bytes.  
*   **Time**.  The time when the message was received or sent.  -->

<!--Messages are color-coded according to their type:  

*   Outgoing text messages are light-green.  
*   Incoming text messages are white.  
*   WebSocket opcodes are light-yellow.  
*   Errors are light-red.  -->

### <span data-ttu-id="6fc3d-316">Anzeigen einer Vorschau eines Antworttexts</span><span class="sxs-lookup"><span data-stu-id="6fc3d-316">View a preview of a response body</span></span>   

<span data-ttu-id="6fc3d-317">So zeigen Sie eine Vorschau eines Antworttexts an:</span><span class="sxs-lookup"><span data-stu-id="6fc3d-317">To view a preview of a response body:</span></span>  

1.  <span data-ttu-id="6fc3d-318">Wählen Sie die URL der Anforderung unter der Spalte **Name** der Tabelle Anforderungen aus.</span><span class="sxs-lookup"><span data-stu-id="6fc3d-318">Select the URL of the request, under the **Name** column of the Requests table.</span></span>  
1.  <span data-ttu-id="6fc3d-319">Wählen Sie die Registerkarte **Vorschau** aus.</span><span class="sxs-lookup"><span data-stu-id="6fc3d-319">Select the **Preview** tab.</span></span>  

<span data-ttu-id="6fc3d-320">Diese Registerkarte ist hauptsächlich für die Anzeige von Bildern hilfreich.</span><span class="sxs-lookup"><span data-stu-id="6fc3d-320">This tab is mostly useful for viewing images.</span></span>  

> ##### <span data-ttu-id="6fc3d-321">Abbildung 19</span><span class="sxs-lookup"><span data-stu-id="6fc3d-321">Figure 19</span></span>  
> <span data-ttu-id="6fc3d-322">Registerkarte "Vorschau"</span><span class="sxs-lookup"><span data-stu-id="6fc3d-322">The Preview tab</span></span>  
> <span data-ttu-id="6fc3d-323">! [Vorschau-Reiter] [Imagepreview]</span><span class="sxs-lookup"><span data-stu-id="6fc3d-323">![The Preview tab][ImagePreview]</span></span>  

### <span data-ttu-id="6fc3d-324">Anzeigen eines Antworttexts</span><span class="sxs-lookup"><span data-stu-id="6fc3d-324">View a response body</span></span>   

<span data-ttu-id="6fc3d-325">So zeigen Sie den Antworttext auf eine Anforderung an:</span><span class="sxs-lookup"><span data-stu-id="6fc3d-325">To view the response body to a request:</span></span>  

1.  <span data-ttu-id="6fc3d-326">Wählen Sie die URL der Anforderung unter der Spalte **Name** der Tabelle Anforderungen aus.</span><span class="sxs-lookup"><span data-stu-id="6fc3d-326">Select the URL of the request, under the **Name** column of the Requests table.</span></span>  
1.  <span data-ttu-id="6fc3d-327">Wählen Sie die Registerkarte **Antwort** aus.</span><span class="sxs-lookup"><span data-stu-id="6fc3d-327">Select the **Response** tab.</span></span>  

> ##### <span data-ttu-id="6fc3d-328">Abbildung 20</span><span class="sxs-lookup"><span data-stu-id="6fc3d-328">Figure 20</span></span>  
> <span data-ttu-id="6fc3d-329">Die Registerkarte "Antwort"</span><span class="sxs-lookup"><span data-stu-id="6fc3d-329">The Response tab</span></span>  
> <span data-ttu-id="6fc3d-330">! [Die Registerkarte ' Antwort '] [Imageresponse]</span><span class="sxs-lookup"><span data-stu-id="6fc3d-330">![The Response tab][ImageResponse]</span></span>  

### <span data-ttu-id="6fc3d-331">Anzeigen von HTTP-Headern</span><span class="sxs-lookup"><span data-stu-id="6fc3d-331">View HTTP headers</span></span>   

<span data-ttu-id="6fc3d-332">So zeigen Sie HTTP-Header Daten zu einer Anforderung an:</span><span class="sxs-lookup"><span data-stu-id="6fc3d-332">To view HTTP header data about a request:</span></span>  

1.  <span data-ttu-id="6fc3d-333">Wählen Sie die URL der Anforderung unter der Spalte **Name** der Tabelle Anforderungen aus.</span><span class="sxs-lookup"><span data-stu-id="6fc3d-333">Select the URL of the request, under the **Name** column of the Requests table.</span></span>  
1.  <span data-ttu-id="6fc3d-334">Wählen Sie die Registerkarte über **Schriften** aus.</span><span class="sxs-lookup"><span data-stu-id="6fc3d-334">Select the **Headers** tab.</span></span>  

> ##### <span data-ttu-id="6fc3d-335">Abbildung 21</span><span class="sxs-lookup"><span data-stu-id="6fc3d-335">Figure 21</span></span>  
> <span data-ttu-id="6fc3d-336">Die Registerkarte "Überschriften"</span><span class="sxs-lookup"><span data-stu-id="6fc3d-336">The Headers tab</span></span>  
> <span data-ttu-id="6fc3d-337">! [Die Registerkarte ' Überschriften '] [Imageheaders]</span><span class="sxs-lookup"><span data-stu-id="6fc3d-337">![The Headers tab][ImageHeaders]</span></span>  

#### <span data-ttu-id="6fc3d-338">Anzeigen der HTTP-Header Quelle</span><span class="sxs-lookup"><span data-stu-id="6fc3d-338">View HTTP header source</span></span>   

<span data-ttu-id="6fc3d-339">Standardmäßig werden auf der Registerkarte Kopfzeilennamen in alphabetischer Reihenfolge angezeigt.</span><span class="sxs-lookup"><span data-stu-id="6fc3d-339">By default, the Headers tab shows header names alphabetically.</span></span>  <span data-ttu-id="6fc3d-340">So zeigen Sie die HTTP-Headernamen in der Reihenfolge an, in der Sie empfangen wurden:</span><span class="sxs-lookup"><span data-stu-id="6fc3d-340">To view the HTTP header names in the order they were received:</span></span>  

1.  <span data-ttu-id="6fc3d-341">Öffnen Sie die Registerkarte über **Schriften** für die Anforderung, die Sie interessiert.</span><span class="sxs-lookup"><span data-stu-id="6fc3d-341">Open the **Headers** tab for the request that interests you.</span></span>  <span data-ttu-id="6fc3d-342">Siehe [Anzeigen von HTTP-Kopfzeilen](#view-http-headers).</span><span class="sxs-lookup"><span data-stu-id="6fc3d-342">See [View HTTP headers](#view-http-headers).</span></span>  
1.  <span data-ttu-id="6fc3d-343">Wählen Sie **Quelle anzeigen**neben dem Abschnitt **Anforderungs Kopfzeile** oder **Antwort Kopf** aus.</span><span class="sxs-lookup"><span data-stu-id="6fc3d-343">Select **view source**, next to the **Request Header** or **Response Header** section.</span></span>  

### <span data-ttu-id="6fc3d-344">Anzeigen von Abfragezeichenfolgenparametern</span><span class="sxs-lookup"><span data-stu-id="6fc3d-344">View query string parameters</span></span>   

<span data-ttu-id="6fc3d-345">So zeigen Sie die Abfragezeichenfolgenparameter einer URL in einem Menschen lesbaren Format an:</span><span class="sxs-lookup"><span data-stu-id="6fc3d-345">To view the query string parameters of a URL in a human-readable format:</span></span>  

1.  <span data-ttu-id="6fc3d-346">Öffnen Sie die Registerkarte über **Schriften** für die Anforderung, die Sie interessiert.</span><span class="sxs-lookup"><span data-stu-id="6fc3d-346">Open the **Headers** tab for the request that interests you.</span></span>  <span data-ttu-id="6fc3d-347">Siehe [Anzeigen von HTTP-Kopfzeilen](#view-http-headers).</span><span class="sxs-lookup"><span data-stu-id="6fc3d-347">See [View HTTP headers](#view-http-headers).</span></span>  
1.  <span data-ttu-id="6fc3d-348">Wechseln Sie zum Abschnitt **Abfragezeichenfolgenparameter** .</span><span class="sxs-lookup"><span data-stu-id="6fc3d-348">Go to the **Query String Parameters** section.</span></span>  

> ##### <span data-ttu-id="6fc3d-349">Abbildung 22</span><span class="sxs-lookup"><span data-stu-id="6fc3d-349">Figure 22</span></span>  
> <span data-ttu-id="6fc3d-350">Der Abfragezeichenfolgenparameter Abschnitt</span><span class="sxs-lookup"><span data-stu-id="6fc3d-350">The Query String Parameters section</span></span>  
> <span data-ttu-id="6fc3d-351">! [Der Abschnitt ' Abfragezeichenfolgen-Parameter] [Imagequerystringparameter]</span><span class="sxs-lookup"><span data-stu-id="6fc3d-351">![The Query String Parameters section][ImageQueryStringParameters]</span></span>  

#### <span data-ttu-id="6fc3d-352">Anzeigen der Parameterquelle für Abfragezeichenfolgen</span><span class="sxs-lookup"><span data-stu-id="6fc3d-352">View query string parameters source</span></span>   

<span data-ttu-id="6fc3d-353">So zeigen Sie die Abfragezeichenfolgenparameter Quelle einer Anforderung an:</span><span class="sxs-lookup"><span data-stu-id="6fc3d-353">To view the query string parameter source of a request:</span></span>  

1.  <span data-ttu-id="6fc3d-354">Wechseln Sie zum Abschnitt Abfragezeichenfolgenparameter.</span><span class="sxs-lookup"><span data-stu-id="6fc3d-354">Go to the Query String Parameters section.</span></span>  <span data-ttu-id="6fc3d-355">Weitere Informationen finden Sie unter [Anzeigen von Abfragezeichenfolgenparametern](#view-query-string-parameters).</span><span class="sxs-lookup"><span data-stu-id="6fc3d-355">See [View query string parameters](#view-query-string-parameters).</span></span>  
1.  <span data-ttu-id="6fc3d-356">Wählen Sie **Quelltext anzeigen**aus.</span><span class="sxs-lookup"><span data-stu-id="6fc3d-356">Select **view source**.</span></span>  

#### <span data-ttu-id="6fc3d-357">Anzeigen von URL-codierten Abfragezeichenfolgenparametern</span><span class="sxs-lookup"><span data-stu-id="6fc3d-357">View URL-encoded query string parameters</span></span>   

<span data-ttu-id="6fc3d-358">So zeigen Sie Abfragezeichenfolgenparameter in einem menschlich lesbaren Format an, jedoch mit erhaltenen Codierungen:</span><span class="sxs-lookup"><span data-stu-id="6fc3d-358">To view query string parameters in a human-readable format, but with encodings preserved:</span></span>  

1.  <span data-ttu-id="6fc3d-359">Wechseln Sie zum Abschnitt Abfragezeichenfolgenparameter.</span><span class="sxs-lookup"><span data-stu-id="6fc3d-359">Go to the Query String Parameters section.</span></span>  <span data-ttu-id="6fc3d-360">Weitere Informationen finden Sie unter [Anzeigen von Abfragezeichenfolgenparametern](#view-query-string-parameters).</span><span class="sxs-lookup"><span data-stu-id="6fc3d-360">See [View query string parameters](#view-query-string-parameters).</span></span>  
1.  <span data-ttu-id="6fc3d-361">Wählen Sie **URL-codiert anzeigen**aus.</span><span class="sxs-lookup"><span data-stu-id="6fc3d-361">Select **view URL encoded**.</span></span>  

### <span data-ttu-id="6fc3d-362">Cookies anzeigen</span><span class="sxs-lookup"><span data-stu-id="6fc3d-362">View cookies</span></span>   

<span data-ttu-id="6fc3d-363">So zeigen Sie die im HTTP-Header einer Anforderung gesendeten Cookies an:</span><span class="sxs-lookup"><span data-stu-id="6fc3d-363">To view the cookies sent in the HTTP header of a request:</span></span>  

1.  <span data-ttu-id="6fc3d-364">Wählen Sie die URL der Anforderung unter der Spalte **Name** der Tabelle Anforderungen aus.</span><span class="sxs-lookup"><span data-stu-id="6fc3d-364">Select the URL of the request, under the **Name** column of the Requests table.</span></span>  
1.  <span data-ttu-id="6fc3d-365">Wählen Sie die Registerkarte **Cookies** aus.</span><span class="sxs-lookup"><span data-stu-id="6fc3d-365">Select the **Cookies** tab.</span></span>  

<!--See [Fields][ManageDataCookiesFields] for a description of each of the columns.  -->

<!--[ManageDataCookiesFields]: manage-data/cookies#fields  -->
<!--TODO: add link when section is available -->

> ##### <span data-ttu-id="6fc3d-366">Abbildung 23</span><span class="sxs-lookup"><span data-stu-id="6fc3d-366">Figure 23</span></span>  
> <span data-ttu-id="6fc3d-367">Die Registerkarte "Cookies"</span><span class="sxs-lookup"><span data-stu-id="6fc3d-367">The Cookies tab</span></span>  
> <span data-ttu-id="6fc3d-368">! [Die Registerkarte ' Cookies '] [Imagecookies]</span><span class="sxs-lookup"><span data-stu-id="6fc3d-368">![The Cookies tab][ImageCookies]</span></span>  

### <span data-ttu-id="6fc3d-369">Anzeigen der Zeit Plan Aufteilung einer Anforderung</span><span class="sxs-lookup"><span data-stu-id="6fc3d-369">View the timing breakdown of a request</span></span>   

<span data-ttu-id="6fc3d-370">So zeigen Sie die Anzeigedauer einer Anforderung an:</span><span class="sxs-lookup"><span data-stu-id="6fc3d-370">To view the timing breakdown of a request:</span></span>  

1.  <span data-ttu-id="6fc3d-371">Wählen Sie die URL der Anforderung unter der Spalte **Name** der Tabelle Anforderungen aus.</span><span class="sxs-lookup"><span data-stu-id="6fc3d-371">Select the URL of the request, under the **Name** column of the Requests table.</span></span>  
1.  <span data-ttu-id="6fc3d-372">Wählen Sie die Registerkarte **Anzeige** Dauer aus.</span><span class="sxs-lookup"><span data-stu-id="6fc3d-372">Select the **Timing** tab.</span></span>  

<span data-ttu-id="6fc3d-373">Eine schnellere Möglichkeit für den Zugriff auf diese Daten finden Sie unter [Anzeigen einer Zeit Plan Vorschau](#preview-a-timing-breakdown) .</span><span class="sxs-lookup"><span data-stu-id="6fc3d-373">See [Preview a timing breakdown](#preview-a-timing-breakdown) for a faster way to access this data.</span></span>  

<span data-ttu-id="6fc3d-374">Weitere Informationen zu den einzelnen Phasen, die auf der Registerkarte "Anzeigedauer" angezeigt werden, finden Sie unter [erläuterte Phasen der zeitlichen Verteilung](#timing-breakdown-phases-explained) .</span><span class="sxs-lookup"><span data-stu-id="6fc3d-374">See [Timing breakdown phases explained](#timing-breakdown-phases-explained) for more information about each of the phases that you may see in the Timing tab.</span></span>  

> ##### <span data-ttu-id="6fc3d-375">Abbildung 24</span><span class="sxs-lookup"><span data-stu-id="6fc3d-375">Figure 24</span></span>  
> <span data-ttu-id="6fc3d-376">Registerkarte "Anzeigedauer"</span><span class="sxs-lookup"><span data-stu-id="6fc3d-376">The Timing tab</span></span>  
> <span data-ttu-id="6fc3d-377">! [Die Registerkarte Anzeigedauer] [Imagetiming]</span><span class="sxs-lookup"><span data-stu-id="6fc3d-377">![The Timing tab][ImageTiming]</span></span>  

<span data-ttu-id="6fc3d-378">Weitere Informationen zu den einzelnen Phasen.</span><span class="sxs-lookup"><span data-stu-id="6fc3d-378">More information about each of the phases.</span></span>  

<span data-ttu-id="6fc3d-379">Eine weitere Möglichkeit für den Zugriff auf diese Ansicht finden Sie unter [Aufschlüsselung der Anzeige](#view-the-timing-breakdown-of-a-request) Dauer.</span><span class="sxs-lookup"><span data-stu-id="6fc3d-379">See [View timing breakdown](#view-the-timing-breakdown-of-a-request) for another way to access this view.</span></span>  

#### <span data-ttu-id="6fc3d-380">Anzeigen einer Vorschau einer Anzeigedauer</span><span class="sxs-lookup"><span data-stu-id="6fc3d-380">Preview a timing breakdown</span></span>   

<span data-ttu-id="6fc3d-381">Wenn Sie eine Vorschau der Anzeigedauer einer Anforderung anzeigen möchten, zeigen Sie in der Spalte **Wasserfall** in der Tabelle Anforderungen auf den Eintrag für die Anforderung.</span><span class="sxs-lookup"><span data-stu-id="6fc3d-381">To view a preview of the timing breakdown of a request, hover over the entry for the request in the **Waterfall** column of the Requests table.</span></span>  

<span data-ttu-id="6fc3d-382">Weitere Informationen finden Sie unter [Anzeigen der zeitlichen Aufschlüsselung einer Anforderung](#view-the-timing-breakdown-of-a-request) für eine Möglichkeit, auf diese Daten zuzugreifen, für die kein Hovern erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="6fc3d-382">See [View the timing breakdown of a request](#view-the-timing-breakdown-of-a-request) for a way to access this data that does not require hovering.</span></span>  

> ##### <span data-ttu-id="6fc3d-383">Abbildung 25</span><span class="sxs-lookup"><span data-stu-id="6fc3d-383">Figure 25</span></span>  
> <span data-ttu-id="6fc3d-384">Anzeigen einer Vorschau der Anzeigedauer einer Anforderung</span><span class="sxs-lookup"><span data-stu-id="6fc3d-384">Previewing the timing breakdown of a request</span></span>  
> <span data-ttu-id="6fc3d-385">! [Vorschau der zeitlichen Aufschlüsselung einer Anforderung] [ImageWaterfallHover]</span><span class="sxs-lookup"><span data-stu-id="6fc3d-385">![Previewing the timing breakdown of a request][ImageWaterfallHover]</span></span>  

#### <span data-ttu-id="6fc3d-386">Erläuterte Phasen Aufgliederungs Phasen</span><span class="sxs-lookup"><span data-stu-id="6fc3d-386">Timing breakdown phases explained</span></span>   

<span data-ttu-id="6fc3d-387">Weitere Informationen zu den einzelnen Phasen, die auf der Registerkarte Anzeigedauer angezeigt werden, finden Sie unter:</span><span class="sxs-lookup"><span data-stu-id="6fc3d-387">More information about each of the phases you may see in the Timing tab:</span></span>  

*   <span data-ttu-id="6fc3d-388">**Warteschlange**.</span><span class="sxs-lookup"><span data-stu-id="6fc3d-388">**Queueing**.</span></span>  <span data-ttu-id="6fc3d-389">Der Browser Warteschlangenanforderungen, wenn:</span><span class="sxs-lookup"><span data-stu-id="6fc3d-389">The browser queues requests when:</span></span>  
    *   <span data-ttu-id="6fc3d-390">Es gibt Anforderungen mit höherer Priorität.</span><span class="sxs-lookup"><span data-stu-id="6fc3d-390">There are higher priority requests.</span></span>  
    *   <span data-ttu-id="6fc3d-391">Für diesen Ursprung sind bereits sechs TCP-Verbindungen geöffnet, was die Grenze ist.</span><span class="sxs-lookup"><span data-stu-id="6fc3d-391">There are already six TCP connections open for this origin, which is the limit.</span></span>  <span data-ttu-id="6fc3d-392">Gilt nur für HTTP/1.0 und HTTP/1.1.</span><span class="sxs-lookup"><span data-stu-id="6fc3d-392">Applies to HTTP/1.0 and HTTP/1.1 only.</span></span>  
    *   <span data-ttu-id="6fc3d-393">Der Browser reserviert kurzzeitig Speicherplatz im Datenträgercache.</span><span class="sxs-lookup"><span data-stu-id="6fc3d-393">The browser is briefly allocating space in the disk cache.</span></span>  
*   <span data-ttu-id="6fc3d-394">Im **Stall**.</span><span class="sxs-lookup"><span data-stu-id="6fc3d-394">**Stalled**.</span></span>  <span data-ttu-id="6fc3d-395">Die Anforderung konnte aus einem der in der **Warteschlange**beschriebenen Gründe blockiert werden.</span><span class="sxs-lookup"><span data-stu-id="6fc3d-395">The request could be stalled for any of the reasons described in **Queueing**.</span></span>  
*   <span data-ttu-id="6fc3d-396">**DNS-Lookup**.</span><span class="sxs-lookup"><span data-stu-id="6fc3d-396">**DNS Lookup**.</span></span>  <span data-ttu-id="6fc3d-397">Der Browser löst die IP-Adresse für die Anforderung auf.</span><span class="sxs-lookup"><span data-stu-id="6fc3d-397">The browser is resolving the IP address for the request.</span></span>  
*   <span data-ttu-id="6fc3d-398">**Proxy Verhandlung**.</span><span class="sxs-lookup"><span data-stu-id="6fc3d-398">**Proxy negotiation**.</span></span>  <span data-ttu-id="6fc3d-399">Der Browser verhandelt die Anforderung mit einem [Proxy Server][WikiProxyServer].</span><span class="sxs-lookup"><span data-stu-id="6fc3d-399">The browser is negotiating the request with a [proxy server][WikiProxyServer].</span></span>  
*   <span data-ttu-id="6fc3d-400">**Anfrage gesendet**.</span><span class="sxs-lookup"><span data-stu-id="6fc3d-400">**Request sent**.</span></span>  <span data-ttu-id="6fc3d-401">Die Anfrage wird gesendet.</span><span class="sxs-lookup"><span data-stu-id="6fc3d-401">The request is being sent.</span></span>  
*   <span data-ttu-id="6fc3d-402">**ServiceWorker-Vorbereitung**.</span><span class="sxs-lookup"><span data-stu-id="6fc3d-402">**ServiceWorker Preparation**.</span></span>  <span data-ttu-id="6fc3d-403">Der Browser startet den Dienstmitarbeiter.</span><span class="sxs-lookup"><span data-stu-id="6fc3d-403">The browser is starting up the service worker.</span></span>  
*   <span data-ttu-id="6fc3d-404">**Anforderung an ServiceWorker**.</span><span class="sxs-lookup"><span data-stu-id="6fc3d-404">**Request to ServiceWorker**.</span></span>  <span data-ttu-id="6fc3d-405">Die Anforderung wird an den Dienstmitarbeiter gesendet.</span><span class="sxs-lookup"><span data-stu-id="6fc3d-405">The request is being sent to the service worker.</span></span>  
*   <span data-ttu-id="6fc3d-406">**Waiting \ (TTFB \)**.</span><span class="sxs-lookup"><span data-stu-id="6fc3d-406">**Waiting \(TTFB\)**.</span></span>  <span data-ttu-id="6fc3d-407">Der Browser wartet auf das erste Byte einer Antwort.</span><span class="sxs-lookup"><span data-stu-id="6fc3d-407">The browser is waiting for the first byte of a response.</span></span>  
  <span data-ttu-id="6fc3d-408">TTFB steht für Time to First Byte.</span><span class="sxs-lookup"><span data-stu-id="6fc3d-408">TTFB stands for Time To First Byte.</span></span>  <span data-ttu-id="6fc3d-409">Diese Anzeigedauer umfasst eine Roundtrip-Wartezeit und den Zeitpunkt, zu dem der Server die Antwort vorbereitet hat.</span><span class="sxs-lookup"><span data-stu-id="6fc3d-409">This timing includes 1 round trip of latency and the time the server took to prepare the response.</span></span>  
*   <span data-ttu-id="6fc3d-410">**Inhalt herunterladen**.</span><span class="sxs-lookup"><span data-stu-id="6fc3d-410">**Content Download**.</span></span>  <span data-ttu-id="6fc3d-411">Der Browser empfängt die Antwort.</span><span class="sxs-lookup"><span data-stu-id="6fc3d-411">The browser is receiving the response.</span></span>  
*   <span data-ttu-id="6fc3d-412">**Push wird empfangen**.</span><span class="sxs-lookup"><span data-stu-id="6fc3d-412">**Receiving Push**.</span></span>  <span data-ttu-id="6fc3d-413">Der Browser empfängt Daten für diese Antwort über http/2 Server Push.</span><span class="sxs-lookup"><span data-stu-id="6fc3d-413">The browser is receiving data for this response via HTTP/2 Server Push.</span></span>  
*   <span data-ttu-id="6fc3d-414">**Lese Push**.</span><span class="sxs-lookup"><span data-stu-id="6fc3d-414">**Reading Push**.</span></span>  <span data-ttu-id="6fc3d-415">Der Browser liest die zuvor empfangenen lokalen Daten.</span><span class="sxs-lookup"><span data-stu-id="6fc3d-415">The browser is reading the local data previously received.</span></span>  

### <span data-ttu-id="6fc3d-416">Anzeigen von Initiatoren und Abhängigkeiten</span><span class="sxs-lookup"><span data-stu-id="6fc3d-416">View initiators and dependencies</span></span>   

<span data-ttu-id="6fc3d-417">Wenn Sie die Initiatoren und Abhängigkeiten einer Anforderung anzeigen möchten, halten Sie `Shift` die Anforderung in der Tabelle Anforderungen gedrückt, und zeigen Sie darauf.</span><span class="sxs-lookup"><span data-stu-id="6fc3d-417">To view the initiators and dependencies of a request, hold `Shift`and hover over the request in the Requests table.</span></span>  <span data-ttu-id="6fc3d-418">DevTools Farben: Initiatoren werden in grün angezeigt, und Abhängigkeiten werden in rot angezeigt.</span><span class="sxs-lookup"><span data-stu-id="6fc3d-418">DevTools colors: initiators are shown in green and dependencies are shown in red.</span></span>  

> ##### <span data-ttu-id="6fc3d-419">Abbildung 26</span><span class="sxs-lookup"><span data-stu-id="6fc3d-419">Figure 26</span></span>  
> <span data-ttu-id="6fc3d-420">Anzeigen der Initiatoren und Abhängigkeiten einer Anforderung</span><span class="sxs-lookup"><span data-stu-id="6fc3d-420">Viewing the initiators and dependencies of a request</span></span>  
> <span data-ttu-id="6fc3d-421">! [Anzeigen der Initiatoren und Abhängigkeiten einer Anforderung] [ImageRequestInitiatorsDependencies]</span><span class="sxs-lookup"><span data-stu-id="6fc3d-421">![Viewing the initiators and dependencies of a request][ImageRequestInitiatorsDependencies]</span></span>  

<span data-ttu-id="6fc3d-422">Wenn die Anforderungstabelle chronologisch geordnet ist, ist die erste grüne Anforderung oberhalb des Cursors der Initiator der Abhängigkeit.</span><span class="sxs-lookup"><span data-stu-id="6fc3d-422">When the Requests table is ordered chronologically, the first green request above the one you are hovering is the initiator of the dependency.</span></span>  <span data-ttu-id="6fc3d-423">Wenn darüber eine weitere grüne Anforderung angezeigt wird, ist diese höhere Anforderung der Initiator des Initiators.</span><span class="sxs-lookup"><span data-stu-id="6fc3d-423">If another green request appears above that, that higher request is the initiator of the initiator.</span></span>  <span data-ttu-id="6fc3d-424">Und so weiter.</span><span class="sxs-lookup"><span data-stu-id="6fc3d-424">And so on.</span></span>  

### <span data-ttu-id="6fc3d-425">Laden Ereignisse anzeigen</span><span class="sxs-lookup"><span data-stu-id="6fc3d-425">View load events</span></span>   

<span data-ttu-id="6fc3d-426">DevTools zeigt die Anzeigedauer der `DOMContentLoaded` `load` Ereignisse und Ereignisse an mehreren Stellen im Netzwerk Panel an.</span><span class="sxs-lookup"><span data-stu-id="6fc3d-426">DevTools displays the timing of the `DOMContentLoaded` and `load` events in multiple places on the Network panel.</span></span>  <span data-ttu-id="6fc3d-427">Das `DOMContentLoaded` Ereignis ist blau gefärbt, und das `load` Ereignis ist rot.</span><span class="sxs-lookup"><span data-stu-id="6fc3d-427">The `DOMContentLoaded` event is colored blue, and the `load` event is red.</span></span>  

> ##### <span data-ttu-id="6fc3d-428">Abbildung 27</span><span class="sxs-lookup"><span data-stu-id="6fc3d-428">Figure 27</span></span>  
> <span data-ttu-id="6fc3d-429">Die Speicherorte der `DOMContentLoaded` und- `load` Ereignisse im Netzwerk Panel</span><span class="sxs-lookup"><span data-stu-id="6fc3d-429">The locations of the `DOMContentLoaded` and `load` events on the Network panel</span></span>  
> <span data-ttu-id="6fc3d-430">! [Die Speicherorte der DOMContentLoaded-und Load-Ereignisse im Netzwerk Panel] [ImageNetworkPanelDOMContentLoadedLoadEvents]</span><span class="sxs-lookup"><span data-stu-id="6fc3d-430">![The locations of the DOMContentLoaded and load events on the Network panel][ImageNetworkPanelDOMContentLoadedLoadEvents]</span></span>  

### <span data-ttu-id="6fc3d-431">Anzeigen der Gesamtzahl der Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6fc3d-431">View the total number of requests</span></span>   

<span data-ttu-id="6fc3d-432">Die Gesamtzahl der Anforderungen wird im Bereich "Zusammenfassung" unten im Netzwerkbereich aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="6fc3d-432">The total number of requests is listed in the Summary pane, at the bottom of the Network panel.</span></span>  

> [!CAUTION]
> <span data-ttu-id="6fc3d-433">Diese Nummer verfolgt nur Anforderungen, die seit dem Öffnen von devtools protokolliert wurden.</span><span class="sxs-lookup"><span data-stu-id="6fc3d-433">This number only tracks requests that have been logged since DevTools was opened.</span></span>  <span data-ttu-id="6fc3d-434">Wenn vor dem Öffnen von devtools andere Anforderungen aufgetreten sind, werden diese Anforderungen nicht gezählt.</span><span class="sxs-lookup"><span data-stu-id="6fc3d-434">If other requests occurred before DevTools was opened, those requests are not counted.</span></span>  

> ##### <span data-ttu-id="6fc3d-435">Abbildung 28</span><span class="sxs-lookup"><span data-stu-id="6fc3d-435">Figure 28</span></span>  
> <span data-ttu-id="6fc3d-436">Die Gesamtzahl der Anforderungen seit dem Öffnen von devtools</span><span class="sxs-lookup"><span data-stu-id="6fc3d-436">The total number of requests since DevTools was opened</span></span>  
> <span data-ttu-id="6fc3d-437">! [Die Gesamtzahl der Anforderungen seit dem Öffnen von devtools] [ImageTotalRequests]</span><span class="sxs-lookup"><span data-stu-id="6fc3d-437">![The total number of requests since DevTools was opened][ImageTotalRequests]</span></span>  

### <span data-ttu-id="6fc3d-438">Anzeigen der Gesamtgröße des Downloads</span><span class="sxs-lookup"><span data-stu-id="6fc3d-438">View the total download size</span></span>   

<span data-ttu-id="6fc3d-439">Die Gesamtgröße der Downloadanforderungen wird im Bereich "Zusammenfassung" am unteren Rand des Netzwerkbereichs angezeigt.</span><span class="sxs-lookup"><span data-stu-id="6fc3d-439">The total download size of requests is listed in the Summary pane, at the bottom of the Network panel.</span></span>  

> [!CAUTION]
> <span data-ttu-id="6fc3d-440">Diese Nummer verfolgt nur Anforderungen, die seit dem Öffnen von devtools protokolliert wurden.</span><span class="sxs-lookup"><span data-stu-id="6fc3d-440">This number only tracks requests that have been logged since DevTools was opened.</span></span>  <span data-ttu-id="6fc3d-441">Wenn vor dem Öffnen von devtools andere Anforderungen aufgetreten sind, werden diese Anforderungen nicht gezählt.</span><span class="sxs-lookup"><span data-stu-id="6fc3d-441">If other requests occurred before DevTools was opened, those requests are not counted.</span></span>  

> ##### <span data-ttu-id="6fc3d-442">Abbildung 29</span><span class="sxs-lookup"><span data-stu-id="6fc3d-442">Figure 29</span></span>  
> <span data-ttu-id="6fc3d-443">Die Gesamtgröße der Downloads von Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6fc3d-443">The total download size of requests</span></span>  
> <span data-ttu-id="6fc3d-444">! [Gesamtgröße der Downloadanforderungen] [ImageTotalSize]</span><span class="sxs-lookup"><span data-stu-id="6fc3d-444">![The total download size of requests][ImageTotalSize]</span></span>  

<span data-ttu-id="6fc3d-445">Weitere Informationen finden Sie unter [Anzeigen der unkomprimierten Größe einer Ressource](#view-the-uncompressed-size-of-a-resource) , um zu sehen, wie groß die Ressourcen sind, nachdem der Browser die einzelnen Elemente dekomprimiert hat.</span><span class="sxs-lookup"><span data-stu-id="6fc3d-445">See [View the uncompressed size of a resource](#view-the-uncompressed-size-of-a-resource) to see how large resources are after the browser uncompresses each item.</span></span>  

### <span data-ttu-id="6fc3d-446">Anzeigen der Stapelüberwachung, die eine Anforderung verursacht hat</span><span class="sxs-lookup"><span data-stu-id="6fc3d-446">View the stack trace that caused a request</span></span>   

<span data-ttu-id="6fc3d-447">Nachdem eine JavaScript-Anweisung eine Ressource angefordert hat, zeigen Sie mit der Maus auf die Spalte **Initiator** , um die Stapelüberwachung anzuzeigen, die zur Anforderung führt.</span><span class="sxs-lookup"><span data-stu-id="6fc3d-447">After a JavaScript statement requests a resource, hover over the **Initiator** column to view the stack trace leading up to the request.</span></span>  

<!-- [codepen.io/contoso/pen/yLBrOWa?editors=0010#0](https://codepen.io/contoso/pen/yLBrOWa?editors=0010#0) -->  

<!--
```javascript
function init() {
  getData();
}

function getData() {
  fetch('https:/httpbin.org/get?message=hi');
}

init();
```  
-->  

> ##### <span data-ttu-id="6fc3d-448">Abbildung 30</span><span class="sxs-lookup"><span data-stu-id="6fc3d-448">Figure 30</span></span>  
> <span data-ttu-id="6fc3d-449">Die Stapelüberwachung, die zu einer Ressourcenanforderung führt</span><span class="sxs-lookup"><span data-stu-id="6fc3d-449">The stack trace leading up to a resource request</span></span>  
> <span data-ttu-id="6fc3d-450">! [Die Stapelüberwachung führt zu einer Ressourcenanforderung] [ImageInitiatorStack]</span><span class="sxs-lookup"><span data-stu-id="6fc3d-450">![The stack trace leading up to a resource request][ImageInitiatorStack]</span></span>  

### <span data-ttu-id="6fc3d-451">Anzeigen der unkomprimierten Größe einer Ressource</span><span class="sxs-lookup"><span data-stu-id="6fc3d-451">View the uncompressed size of a resource</span></span>   

<span data-ttu-id="6fc3d-452">Aktivieren Sie das Kontrollkästchen **große Anforderungs Zeilen verwenden** , und schauen Sie sich den niedrigsten Wert der Spalte **Größe** an.</span><span class="sxs-lookup"><span data-stu-id="6fc3d-452">Select the **Use large request rows** checkbox and then look at the bottom value of the **Size** column.</span></span>  

> ##### <span data-ttu-id="6fc3d-453">Abbildung 31</span><span class="sxs-lookup"><span data-stu-id="6fc3d-453">Figure 31</span></span>  
> <span data-ttu-id="6fc3d-454">Ein Beispiel für unkomprimierte Ressourcen \ (die komprimierte Größe der `jquery-3.3.1.min.js` Datei, die über das Netzwerk gesendet wurde `29.9 KB` , während die unkomprimierte Größe `84.9 KB` \) war</span><span class="sxs-lookup"><span data-stu-id="6fc3d-454">An example of uncompressed resources  \(The compressed size of the `jquery-3.3.1.min.js` file that was sent over the network was `29.9 KB`, whereas the uncompressed size was `84.9 KB`\)</span></span>  
> <span data-ttu-id="6fc3d-455">! [Ein Beispiel für nicht komprimierte Ressourcen] [ImageUncompressedResources]</span><span class="sxs-lookup"><span data-stu-id="6fc3d-455">![An example of uncompressed resources][ImageUncompressedResources]</span></span>  

## <span data-ttu-id="6fc3d-456">Exportieren von Anforderungsdaten</span><span class="sxs-lookup"><span data-stu-id="6fc3d-456">Export requests data</span></span>   

### <span data-ttu-id="6fc3d-457">Speichern aller Netzwerkanforderungen in einer har-Datei</span><span class="sxs-lookup"><span data-stu-id="6fc3d-457">Save all network requests to a HAR file</span></span>   

<span data-ttu-id="6fc3d-458">So speichern Sie alle Netzwerkanforderungen in einer har-Datei:</span><span class="sxs-lookup"><span data-stu-id="6fc3d-458">To save all network requests to a HAR file:</span></span>  

1.  <span data-ttu-id="6fc3d-459">Klicken Sie mit der rechten Maustaste auf eine beliebige Anforderung in der Tabelle Anforderungen.</span><span class="sxs-lookup"><span data-stu-id="6fc3d-459">Right-click any request in the Requests table.</span></span>  
1.  <span data-ttu-id="6fc3d-460">Wählen Sie **als har mit Inhalt speichern**aus.</span><span class="sxs-lookup"><span data-stu-id="6fc3d-460">Select **Save as HAR with Content**.</span></span>  <span data-ttu-id="6fc3d-461">DevTools speichert alle Anforderungen, die seit dem Öffnen von devtools in der har-Datei aufgetreten sind.</span><span class="sxs-lookup"><span data-stu-id="6fc3d-461">DevTools saves all requests that have occurred since you opened DevTools to the HAR file.</span></span>  <span data-ttu-id="6fc3d-462">Es gibt keine Möglichkeit, Anforderungen zu filtern oder nur eine einzige Anforderung zu speichern.</span><span class="sxs-lookup"><span data-stu-id="6fc3d-462">There is no way to filter requests, or to save just a single request.</span></span>  

<span data-ttu-id="6fc3d-463">Nachdem Sie eine har-Datei gespeichert haben, können Sie Sie für die Analyse wieder in devtools importieren.</span><span class="sxs-lookup"><span data-stu-id="6fc3d-463">Once you save a HAR file, you may import it back into DevTools for analysis.</span></span>  <span data-ttu-id="6fc3d-464">Ziehen Sie die har-Datei einfach per Drag & Drop in die Tabelle "Anforderungen".</span><span class="sxs-lookup"><span data-stu-id="6fc3d-464">Just drag-and-drop the HAR file into the Requests table.</span></span>  
<!--See also [HAR Analyzer][HARAnalyzer].  -->  

<!--[HARAnalyzer]: https://toolbox.alphabetapps.com/apps/har_analyzer  -->  
<!--Todo: add section link when content is available  -->  

> ##### <span data-ttu-id="6fc3d-465">Abbildung 32</span><span class="sxs-lookup"><span data-stu-id="6fc3d-465">Figure 32</span></span>  
> <span data-ttu-id="6fc3d-466">Auswählen von "als har mit Inhalt speichern"</span><span class="sxs-lookup"><span data-stu-id="6fc3d-466">Selecting Save as HAR with Content</span></span>  
> <span data-ttu-id="6fc3d-467">! [Auswählen von "als har mit Inhalt speichern" [ImageSaveAsHAR]</span><span class="sxs-lookup"><span data-stu-id="6fc3d-467">![Selecting Save as HAR with Content][ImageSaveAsHAR]</span></span>  

### <span data-ttu-id="6fc3d-468">Kopieren einer oder mehrerer Anforderungen in die Zwischenablage</span><span class="sxs-lookup"><span data-stu-id="6fc3d-468">Copy one or more requests to the clipboard</span></span>   

<span data-ttu-id="6fc3d-469">Klicken Sie unter der Spalte **Name** der Tabelle Anforderungen mit der rechten Maustaste auf eine Anforderung, zeigen Sie mit der Maus auf **Kopieren**, und wählen Sie eine der folgenden Optionen aus:</span><span class="sxs-lookup"><span data-stu-id="6fc3d-469">Under the **Name** column of the Requests table, right-click a request, hover over **Copy**, and select one of the following options:</span></span>  

*   <span data-ttu-id="6fc3d-470">**Link Adresse kopieren**</span><span class="sxs-lookup"><span data-stu-id="6fc3d-470">**Copy Link Address**.</span></span>  <span data-ttu-id="6fc3d-471">Kopieren Sie die URL der Anforderung in die Zwischenablage.</span><span class="sxs-lookup"><span data-stu-id="6fc3d-471">Copy the URL of the request to the clipboard.</span></span>  
*   <span data-ttu-id="6fc3d-472">**Antwort kopieren**</span><span class="sxs-lookup"><span data-stu-id="6fc3d-472">**Copy Response**.</span></span>  <span data-ttu-id="6fc3d-473">Kopieren Sie den Antworttext in die Zwischenablage.</span><span class="sxs-lookup"><span data-stu-id="6fc3d-473">Copy the response body to the clipboard.</span></span>  
*   <span data-ttu-id="6fc3d-474">**Als FETCH kopieren**</span><span class="sxs-lookup"><span data-stu-id="6fc3d-474">**Copy as Fetch**.</span></span>  
*   <span data-ttu-id="6fc3d-475">**Als curl kopieren**</span><span class="sxs-lookup"><span data-stu-id="6fc3d-475">**Copy as cURL**.</span></span>  <span data-ttu-id="6fc3d-476">Kopieren Sie die Anforderung als curl-Befehl.</span><span class="sxs-lookup"><span data-stu-id="6fc3d-476">Copy the request as a cURL command.</span></span>  
*   <span data-ttu-id="6fc3d-477">**Kopieren Sie alle als FETCH**.</span><span class="sxs-lookup"><span data-stu-id="6fc3d-477">**Copy All as Fetch**.</span></span>  
*   <span data-ttu-id="6fc3d-478">**Kopieren Sie alle als curl**.</span><span class="sxs-lookup"><span data-stu-id="6fc3d-478">**Copy All as cURL**.</span></span>  <span data-ttu-id="6fc3d-479">Kopieren Sie alle Anforderungen als eine Kette von curl-Befehlen.</span><span class="sxs-lookup"><span data-stu-id="6fc3d-479">Copy all requests as a chain of cURL commands.</span></span>  
*   <span data-ttu-id="6fc3d-480">**Kopieren Sie alle als har**.</span><span class="sxs-lookup"><span data-stu-id="6fc3d-480">**Copy All as HAR**.</span></span>  <span data-ttu-id="6fc3d-481">Kopieren Sie alle Anforderungen als har-Daten.</span><span class="sxs-lookup"><span data-stu-id="6fc3d-481">Copy all requests as HAR data.</span></span>  

> ##### <span data-ttu-id="6fc3d-482">Abbildung 33</span><span class="sxs-lookup"><span data-stu-id="6fc3d-482">Figure 33</span></span>  
> <span data-ttu-id="6fc3d-483">Auswählen von "Antwort kopieren"</span><span class="sxs-lookup"><span data-stu-id="6fc3d-483">Selecting Copy Response</span></span>  
> <span data-ttu-id="6fc3d-484">! [Auswahl von Antwort kopieren] [ImageCopyResponse]</span><span class="sxs-lookup"><span data-stu-id="6fc3d-484">![Selecting Copy Response][ImageCopyResponse]</span></span>  

## <span data-ttu-id="6fc3d-485">Ändern des Layouts des Netzwerk Panels</span><span class="sxs-lookup"><span data-stu-id="6fc3d-485">Change the layout of the Network panel</span></span>  

<span data-ttu-id="6fc3d-486">Sie können Abschnitte der Netzwerk Panel-UI erweitern oder reduzieren, um wichtige Informationen zu konzentrieren.</span><span class="sxs-lookup"><span data-stu-id="6fc3d-486">You may expand or collapse sections of the Network panel UI to focus important information.</span></span>  

### <span data-ttu-id="6fc3d-487">Ausblenden des Bereichs "Filter"</span><span class="sxs-lookup"><span data-stu-id="6fc3d-487">Hide the Filters pane</span></span>   

<span data-ttu-id="6fc3d-488">Standardmäßig zeigt devtools den **Bereich "Filter"** an.</span><span class="sxs-lookup"><span data-stu-id="6fc3d-488">By default, DevTools shows the **Filters pane**.</span></span>  
<span data-ttu-id="6fc3d-489">Wählen Sie **Filter** ![ Filter aus ][ImageFilterIcon] , um sie auszublenden.</span><span class="sxs-lookup"><span data-stu-id="6fc3d-489">Select **Filter** ![Filter][ImageFilterIcon]  to hide it.</span></span>  

> ##### <span data-ttu-id="6fc3d-490">Abbildung 34</span><span class="sxs-lookup"><span data-stu-id="6fc3d-490">Figure 34</span></span>  
> <span data-ttu-id="6fc3d-491">Schaltfläche "Filter ausblenden"</span><span class="sxs-lookup"><span data-stu-id="6fc3d-491">The Hide Filters button</span></span>  
> <span data-ttu-id="6fc3d-492">! [Die Schaltfläche ' Filter ausblenden '] [ImageHideFiltersButton]</span><span class="sxs-lookup"><span data-stu-id="6fc3d-492">![The Hide Filters button][ImageHideFiltersButton]</span></span>  

### <span data-ttu-id="6fc3d-493">Verwenden von umfangreichen Anforderungs Zeilen</span><span class="sxs-lookup"><span data-stu-id="6fc3d-493">Use large request rows</span></span>   

<span data-ttu-id="6fc3d-494">Verwenden Sie große Zeilen, wenn in Ihrer Netzwerk Anforderungstabelle mehr Leerzeichen verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="6fc3d-494">Use large rows when you want more whitespace in your network requests table.</span></span>  <span data-ttu-id="6fc3d-495">Einige Spalten liefern auch ein wenig mehr Informationen, wenn Sie große Zeilen verwenden.</span><span class="sxs-lookup"><span data-stu-id="6fc3d-495">Some columns also provide a little more information when using large rows.</span></span>  <span data-ttu-id="6fc3d-496">Der untere Wert der Spalte **size** entspricht beispielsweise der unkomprimierten Größe einer Anforderung.</span><span class="sxs-lookup"><span data-stu-id="6fc3d-496">For example, the bottom value of the **Size** column is the uncompressed size of a request.</span></span>  

> ##### <span data-ttu-id="6fc3d-497">Abbildung 35</span><span class="sxs-lookup"><span data-stu-id="6fc3d-497">Figure 35</span></span>  
> <span data-ttu-id="6fc3d-498">Ein Beispiel für große Anforderungs Zeilen im Bereich "Anforderungen"</span><span class="sxs-lookup"><span data-stu-id="6fc3d-498">An example of large request rows in the Requests pane</span></span>  
> <span data-ttu-id="6fc3d-499">! [Ein Beispiel für große Anforderungs Zeilen im Bereich "Anforderungen"] [ImageLargeRequestRows]</span><span class="sxs-lookup"><span data-stu-id="6fc3d-499">![An example of large request rows in the Requests pane][ImageLargeRequestRows]</span></span>  

<span data-ttu-id="6fc3d-500">Aktivieren Sie das Kontrollkästchen **große Anforderungs Zeilen verwenden** , um große Zeilen zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="6fc3d-500">Select the **Use large request rows** checkbox to enable large rows.</span></span>  

> ##### <span data-ttu-id="6fc3d-501">Abbildung 36</span><span class="sxs-lookup"><span data-stu-id="6fc3d-501">Figure 36</span></span>  
> <span data-ttu-id="6fc3d-502">Das Kontrollkästchen ' große Anforderungs Zeilen '</span><span class="sxs-lookup"><span data-stu-id="6fc3d-502">The Large Request Rows checkbox</span></span>  
> <span data-ttu-id="6fc3d-503">! [Das Kontrollkästchen ' große Anforderungs Zeilen '] [ImageLargeRequestRowsCheckbox]</span><span class="sxs-lookup"><span data-stu-id="6fc3d-503">![The Large Request Rows checkbox][ImageLargeRequestRowsCheckbox]</span></span>  

### <span data-ttu-id="6fc3d-504">Ausblenden des Bereichs "Übersicht"</span><span class="sxs-lookup"><span data-stu-id="6fc3d-504">Hide the Overview pane</span></span>   

<span data-ttu-id="6fc3d-505">Standardmäßig zeigt devtools den **Bereich "Übersicht"** an.</span><span class="sxs-lookup"><span data-stu-id="6fc3d-505">By default, DevTools shows the **Overview pane**.</span></span>  
<span data-ttu-id="6fc3d-506">Deaktivieren Sie das Kontrollkästchen " **Übersicht anzeigen** ", um es auszublenden.</span><span class="sxs-lookup"><span data-stu-id="6fc3d-506">Deselect the **Show Overview** checkbox to hide it.</span></span>  

> ##### <span data-ttu-id="6fc3d-507">Abbildung 37</span><span class="sxs-lookup"><span data-stu-id="6fc3d-507">Figure 37</span></span>  
> <span data-ttu-id="6fc3d-508">Kontrollkästchen ' Übersicht anzeigen '</span><span class="sxs-lookup"><span data-stu-id="6fc3d-508">The Show Overview checkbox</span></span>  
> <span data-ttu-id="6fc3d-509">! [Kontrollkästchen ' Übersicht anzeigen '] [ImageHideOverviewCheckbox]</span><span class="sxs-lookup"><span data-stu-id="6fc3d-509">![The Show Overview checkbox][ImageHideOverviewCheckbox]</span></span>  

<!-->   -->  

  

<!-- image links -->  

[ImageCaptureScreenshotsIcon]: /microsoft-edge/devtools-guide-chromium/media/capture-screenshots-icon.msft.png  
[ImageClearIcon]: /microsoft-edge/devtools-guide-chromium/media/clear-requests-icon.msft.png  
[ImageFilterIcon]: /microsoft-edge/devtools-guide-chromium/media/filter-icon.msft.png  
[ImageHideIcon]: /microsoft-edge/devtools-guide-chromium/media/hide-overview-icon.msft.png  
[ImageLargeResourceRowsIcon]: /microsoft-edge/devtools-guide-chromium/media/large-resource-rows-button-icon.msft.png  
[ImageRecordOnIcon]: /microsoft-edge/devtools-guide-chromium/media/record-on-icon.msft.png  

[ImageNetworkPanel]: /microsoft-edge/devtools-guide-chromium/media/network-network-panel.msft.png "Abbildung 1: Netzwerk Panel"  
[ImageClearButton]: /microsoft-edge/devtools-guide-chromium/media/network-network-clear-button.msft.png "Abbildung 2: die Schaltfläche "Löschen""  
[ImagePreserveLogCheckBox]: /microsoft-edge/devtools-guide-chromium/media/network-network-preserve-log.msft.png "Abbildung 3: Kontrollkästchen "Protokoll beibehalten""  
[ImageScreenshotHover]: /microsoft-edge/devtools-guide-chromium/media/network-network-screenshot-hover.msft.png "Abbildung 4: Bewegen des Mauszeigers über einen Screenshot"  
<!--[ImageReplayXHR]: /microsoft-edge/devtools-guide-chromium/media/network-replay-xhr.msft.png "Old Figure 5: Selecting Replay XHR"  -->  
[ImageDisableCacheCheckBox]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Network-Disable-Cache-CheckBox.msft.png "Abbildung 5: Kontrollkästchen" Cache deaktivieren "  
[ImageClearBrowserCache]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Network-Clear-Browser-Cache.msft.png "Abbildung 6: Auswählen des Browsercache löschen"  
[ImageOfflineDropdown]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Network-Offline-Dropdown.msft.png "Abbildung 7: das Offline-Dropdownmenü"  
[ImageNetworkThrottlingMenu]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Network-Throttling-Menu.msft.png "Abbildung 8: Netzwerk Einschränkungs Menü"  
[ImageClearBrowserCookies]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Network-Clear-Browser-Cookies.msft.png "Abbildung 9: Auswählen von Browser-Cookies löschen"  
[ImageFilterTextBox]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Network-Filters-TextBox.msft.png "Abbildung 10: das Textfeld" Filter "  
[ImageMultiTypeFilter]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Network-Type-Filters.msft.png "Abbildung 11: Verwenden der Typfilter zum Anzeigen von JS-, CSS-und Dokument Ressourcen"  
[ImageOverviewFilter]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Network-Overview-Filter.msft.png "Abbildung 12: Filtern von Anforderungen, die um 300m inaktiv waren"  
[ImageHideDataURLsCheckBox]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Network-Hide-Data-URLs.msft.png "Abbildung 13: Kontrollkästchen" Daten-URLs ausblenden "  
[ImageWaterfallTotalDuration]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Network-Waterfall-Total-Duration.msft.png "Abbildung 14: Sortieren des Wasserfalls nach Gesamtdauer"  
[Imagerequestable]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Network-Requests-Table.msft.png "Abbildung 15: die Tabelle" Anforderungen "
[ImageRequestsTable]: /microsoft-edge/devtools-guide-chromium/media/network-network-requests-table.msft.png "Figure 15: The Requests table"  
[ImageRequestsTableAddColumn]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Network-Requests-Add-Column.msft.png "Abbildung 16: Hinzufügen einer Spalte zur Tabelle" Anforderungen "  
[ImageRequestsTableCustomColumn]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Network-Requests-Add-Custom.msft.png "Abbildung 17: Hinzufügen einer benutzerdefinierten Spalte zur Tabelle" Anforderungen "  
[ImageRequestsTableWaterfallColumn]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Network-Requests-Waterfall.msft.png "Abbildung 18: die Spalte Wasserfall im Bereich" Anforderungen "  
[Imagepreview]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Network-Resources-Preview.msft.png "Abbildung 19: die Registerkarte" Vorschau "
[ImagePreview]: /microsoft-edge/devtools-guide-chromium/media/network-network-resources-preview.msft.png "Figure 19: The Preview tab"  
<!--[ImageFrames]: /microsoft-edge/devtools-guide-chromium/media/network-frames.msft.png "Old Figure 20: The Frames tab"  -->  
[Imageresponse]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Network-Resources-Response.msft.png "Abbildung 20: die Registerkarte" Antwort "
[ImageResponse]: /microsoft-edge/devtools-guide-chromium/media/network-network-resources-response.msft.png "Figure 20: The Response tab"  
[Imageheaders]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Resources-Headers.msft.png "Abbildung 21: die Registerkarte" Überschriften "
[ImageHeaders]: /microsoft-edge/devtools-guide-chromium/media/network-resources-headers.msft.png "Figure 21: The Headers tab"  
[Imagequerystringparameter]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Network-Resources-Headers-Query-String-Parameters.msft.png "Abbildung 22: der Abfragezeichenfolgenparameter Abschnitt"
[ImageQueryStringParameters]: /microsoft-edge/devtools-guide-chromium/media/network-network-resources-headers-query-string-parameters.msft.png "Figure 22: The Query String Parameters section"  
[Imagecookies]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Network-Resources-Cookies.msft.png "Abbildung 23: die Registerkarte" Cookies "
[ImageCookies]: /microsoft-edge/devtools-guide-chromium/media/network-network-resources-cookies.msft.png "Figure 23: The Cookies tab"  
[Imagetiming]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Network-Resources-Timing.msft.png "Abbildung 24: die Registerkarte" Anzeigedauer "
[ImageTiming]: /microsoft-edge/devtools-guide-chromium/media/network-network-resources-timing.msft.png "Figure 24: The Timing tab"  
[ImageWaterfallHover]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Network-Resources-Waterfall-Hover.msft.png "Abbildung 25: Vorschau der Anzeigedauer einer Anforderung"  
[ImageRequestInitiatorsDependencies]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Network-Resources-Initiators-dependencies.msft.png "Abbildung 26: Anzeigen der Initiatoren und Abhängigkeiten einer Anforderung"  
[ImageNetworkPanelDOMContentLoadedLoadEvents]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Network-Requests-Load-Events.msft.png "Abbildung 27: die Speicherorte der DOMContentLoaded-und Load-Ereignisse im Netzwerk Panel"  
[ImageTotalRequests]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Network-Total-Requests.msft.png "Abbildung 28: die Gesamtzahl der Anforderungen seit dem Öffnen von devtools"  
[ImageTotalSize]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Network-Total-Download-size.msft.png "Abbildung 29: die Gesamtgröße der Downloadanforderungen"  
[ImageInitiatorStack]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Network-Requests-Initiator-Stack.msft.png "Abbildung 30: die Stapelüberwachung, die zu einer Ressourcenanforderung führt"  
[ImageUncompressedResources]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Network-Requests-uncompressed-Compare.msft.png "Abbildung 31: ein Beispiel für nicht komprimierte Ressourcen"  
[ImageSaveAsHAR]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Network-Requests-Save-har-Content.msft.png "Abbildung 32: Auswählen von" als har mit Inhalt speichern "  
[ImageCopyResponse]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Network-Requests-Copy-Response.msft.png "Abbildung 33: Auswählen von" Antwort kopieren "  
[ImageHideFiltersButton]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Network-Resources-Hide-Filters-Button.msft.png "Abbildung 34: die Schaltfläche" Filter ausblenden "  
[ImageLargeRequestRows]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Network-Requests-Large-Request-Rows.msft.png "Abbildung 35: ein Beispiel für große Anforderungs Zeilen im Bereich" Anforderungen "  
[ImageLargeRequestRowsCheckbox]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Network-Requests-use-Large-Request-Rows-on.msft.png "Abbildung 36: das Kontrollkästchen" große Anforderungs Zeilen "  
[ImageHideOverviewCheckbox]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Network-Requests-Show-Overview-off.msft.png "Abbildung 37: Kontrollkästchen" Übersicht ausblenden "  

<!-- links -->  

[DevtoolsProgressiveWebApps]: /microsoft-edge/devtools-guide-chromium/network/progressive-web-apps "Debuggen von progressiven Web-Apps"  

<!--[NetworkConditions]: /microsoft-edge/devtools-guide-chromium/network/network-conditions "Optimize Performance Under Varying Network Conditions"  -->  

[MDNHTTPDataURIs]: https://developer.mozilla.org/docs/Web/HTTP/Basics_of_HTTP/Data_URIs "Daten-URLs | MDN"  

[WikiProxyServer]: https://en.wikipedia.org/wiki/Proxy_server "Proxy Server – Wikipedia"  

> [!NOTE]
> <span data-ttu-id="6fc3d-550">Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6fc3d-550">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="6fc3d-551">Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/network/reference) und wird von [Kayce Basken][KayceBasques] (Technical Writer, Chrome devtools \ & Lighthouse \) erstellt.</span><span class="sxs-lookup"><span data-stu-id="6fc3d-551">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/network/reference) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
<span data-ttu-id="6fc3d-553">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="6fc3d-553">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
