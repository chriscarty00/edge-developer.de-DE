---
title: Netzwerkanalyse Referenz
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/10/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Web-Entwicklung, F12-Tools, devtools
ms.openlocfilehash: 7e7ac287e116e28773a42456c21ec4ba07647f04
ms.sourcegitcommit: f010f43604bd4363af6827f79dbc071b9afcb667
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2020
ms.locfileid: "10709263"
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

# <span data-ttu-id="020d1-103">Netzwerkanalyse Referenz</span><span class="sxs-lookup"><span data-stu-id="020d1-103">Network Analysis Reference</span></span>  

<span data-ttu-id="020d1-104">Entdecken Sie neue Möglichkeiten zur Analyse, wie Ihre Seite in dieser umfassenden Referenz der Microsoft Edge devtools-Netzwerkanalyse Features geladen werden kann.</span><span class="sxs-lookup"><span data-stu-id="020d1-104">Discover new ways to analyze how your page loads in this comprehensive reference of Microsoft Edge DevTools network analysis features.</span></span>  

<!--
> [!NOTE]
> This reference is based on Microsoft Edge 58.  If you use another version of Microsoft Edge, the UI, and features of DevTools may be different.  Check `edge://help` to see what version of Microsoft Edge you are running.  
-->

## <span data-ttu-id="020d1-105">Aufzeichnen von Netzwerkanforderungen</span><span class="sxs-lookup"><span data-stu-id="020d1-105">Record network requests</span></span>  

<span data-ttu-id="020d1-106">Standardmäßig zeichnet devtools alle Netzwerkanforderungen im Netzwerk Panel auf, solange devtools geöffnet ist.</span><span class="sxs-lookup"><span data-stu-id="020d1-106">By default, DevTools records all network requests in the Network panel, so long as DevTools is open.</span></span>  

:::image type="complex" source="../media/network-network-panel.msft.png" alt-text="Netzwerk Panel" lightbox="../media/network-network-panel.msft.png":::
   <span data-ttu-id="020d1-108">Abbildung 1: **Netzwerk** Panel</span><span class="sxs-lookup"><span data-stu-id="020d1-108">Figure 1:  The **Network** panel</span></span>  
:::image-end:::  

### <span data-ttu-id="020d1-109">Beenden der Aufzeichnung von Netzwerkanforderungen</span><span class="sxs-lookup"><span data-stu-id="020d1-109">Stop recording network requests</span></span>  

<span data-ttu-id="020d1-110">Führen Sie die folgenden Schritte aus, um die Aufzeichnung von Anforderungen zu beenden.</span><span class="sxs-lookup"><span data-stu-id="020d1-110">To stop recording requests, complete the following steps.</span></span>  

1.  <span data-ttu-id="020d1-111">Wählen **Stop recording network log** Sie ![ ][ImageRecordOnIcon] auf der Registerkarte **Netzwerk** die Option Aufzeichnung des Netzwerkprotokolls beenden Aufzeichnung beenden aus.</span><span class="sxs-lookup"><span data-stu-id="020d1-111">Select **Stop recording network log** ![Stop recording network log][ImageRecordOnIcon] on the **Network** panel.</span></span>  <span data-ttu-id="020d1-112">Es wird grau, um anzugeben, dass devtools keine Anforderungen mehr aufzeichnet.</span><span class="sxs-lookup"><span data-stu-id="020d1-112">It turns grey to indicate that DevTools is no longer recording requests.</span></span>  
1.  <span data-ttu-id="020d1-113">Drücken Sie `Control` + `E` \ (Windows \) oder `Command` + `E` \ (macOS \), während sich der Fokus des **Netzwerk** Panels befindet.</span><span class="sxs-lookup"><span data-stu-id="020d1-113">Press `Control`+`E` \(Windows\) or `Command`+`E` \(macOS\) while the **Network** panel is in focus.</span></span>  

### <span data-ttu-id="020d1-114">Löschen von Anforderungen</span><span class="sxs-lookup"><span data-stu-id="020d1-114">Clear requests</span></span>  

<span data-ttu-id="020d1-115">Wählen **Sie** ![ ][ImageClearIcon] im Netzwerk Panel löschen aus, um alle Anforderungen aus der Tabelle Anforderungen zu löschen.</span><span class="sxs-lookup"><span data-stu-id="020d1-115">Select **Clear** ![Clear][ImageClearIcon] on the Network panel to clear all requests from the Requests table.</span></span>  

:::image type="complex" source="../media/network-network-clear-button.msft.png" alt-text="Die Schaltfläche "Löschen"" lightbox="../media/network-network-clear-button.msft.png":::
   <span data-ttu-id="020d1-117">Abbildung 2: die Schaltfläche " **Löschen** "</span><span class="sxs-lookup"><span data-stu-id="020d1-117">Figure 2:  The **Clear** button</span></span>  
:::image-end:::  

### <span data-ttu-id="020d1-118">Speichern von Anforderungen über Seitenlasten hinweg</span><span class="sxs-lookup"><span data-stu-id="020d1-118">Save requests across page loads</span></span>  

<span data-ttu-id="020d1-119">Aktivieren Sie das Kontrollkästchen **Protokoll beibehalten** auf der Registerkarte Netzwerk, um Anforderungen zwischen den Seitenlasten zu speichern.</span><span class="sxs-lookup"><span data-stu-id="020d1-119">To save requests across page loads, check the **Preserve log** checkbox on the Network panel.</span></span>  <span data-ttu-id="020d1-120">DevTools speichert alle Anforderungen, bis Sie **Protokoll beibehalten**deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="020d1-120">DevTools saves all requests until you disable **Preserve log**.</span></span>  

:::image type="complex" source="../media/network-network-preserve-log.msft.png" alt-text="Kontrollkästchen "Protokoll beibehalten"" lightbox="../media/network-network-preserve-log.msft.png":::
   <span data-ttu-id="020d1-122">Abbildung 3: Kontrollkästchen " **Protokoll beibehalten** "</span><span class="sxs-lookup"><span data-stu-id="020d1-122">Figure 3:  The **Preserve Log** checkbox</span></span>  
:::image-end:::  

### <span data-ttu-id="020d1-123">Aufzeichnen von Screenshots beim Laden der Seite</span><span class="sxs-lookup"><span data-stu-id="020d1-123">Capture screenshots during page load</span></span>  

<span data-ttu-id="020d1-124">Erfassen Sie Screenshots, um zu analysieren, was die Benutzer sehen, während Sie auf Ihre Seite warten, um Sie zu laden.</span><span class="sxs-lookup"><span data-stu-id="020d1-124">Capture screenshots to analyze what users see as they wait for your page to load.</span></span>  

<span data-ttu-id="020d1-125">Wenn Sie Screenshots aktivieren möchten, wählen Sie **Netzwerkeinstellungen** und dann auf der Registerkarte **Netzwerk** das Kontrollkästchen **Screenshots aufzeichnen** aus.</span><span class="sxs-lookup"><span data-stu-id="020d1-125">To enable screenshots, select **Network settings** and select **Capture screenshots** checkbox on the **Network** panel.</span></span>  

<span data-ttu-id="020d1-126">Laden Sie die Seite neu, während sich das **Netzwerk** Panel im Fokus befindet, um Screenshots zu erfassen.</span><span class="sxs-lookup"><span data-stu-id="020d1-126">Reload the page while the **Network** panel is in focus to capture screenshots.</span></span>  

<span data-ttu-id="020d1-127">Nachdem Sie einen Screenshot aufgezeichnet haben, interagieren Sie mit ihm auf die folgende Weise.</span><span class="sxs-lookup"><span data-stu-id="020d1-127">After capturing a screenshot, you interact with it in the following ways.</span></span>  

*   <span data-ttu-id="020d1-128">Zeigen Sie mit der Maus auf einen Screenshot, um den Punkt anzuzeigen, an dem dieser Screenshot aufgenommen wurde.</span><span class="sxs-lookup"><span data-stu-id="020d1-128">Hover over a screenshot to view the point at which that screenshot was captured.</span></span>  <span data-ttu-id="020d1-129">Im Bereich " **Übersicht** " wird eine gelbe Zeile angezeigt.</span><span class="sxs-lookup"><span data-stu-id="020d1-129">A yellow line appears on the **Overview** pane.</span></span>  
*   <span data-ttu-id="020d1-130">Wählen Sie die Miniaturansicht eines Bildschirms aus, um alle Anforderungen zu filtern, die nach dem Erfassen des Screenshots aufgetreten sind.</span><span class="sxs-lookup"><span data-stu-id="020d1-130">Select the thumbnail of a screen to filter out any requests that occurred after the screenshot was captured.</span></span>  
*   <span data-ttu-id="020d1-131">Doppelklicken Sie auf eine Miniaturansicht, um Sie zu vergrößern.</span><span class="sxs-lookup"><span data-stu-id="020d1-131">Double-click a thumbnail to zoom into it.</span></span>  

:::image type="complex" source="../media/network-network-screenshot-hover.msft.png" alt-text="Zeigen auf einen Screenshot" lightbox="../media/network-network-screenshot-hover.msft.png":::
   <span data-ttu-id="020d1-133">Abbildung 4: Bewegen des Mauszeigers über einen Screenshot</span><span class="sxs-lookup"><span data-stu-id="020d1-133">Figure 4:  Hovering over a screenshot</span></span>  
:::image-end:::  

<!--  ### Replay XHR request  -->

<!--  To replay an XHR request, hover on the request in the Requests table, open the contextual menu \(right-click\), and select **Replay XHR**.  -->

<!--  
:::image type="complex" source="../media/network-replay-xhr.msft.png" alt-text="Selecting Replay XHR" lightbox="../media/network-replay-xhr.msft.png":::
   Old Figure 5:  Selecting Replay XHR  
:::image-end:::  
-->  

## <span data-ttu-id="020d1-134">Ändern des Ladeverhaltens</span><span class="sxs-lookup"><span data-stu-id="020d1-134">Change loading behavior</span></span>  

### <span data-ttu-id="020d1-135">Emulieren eines erstmaligen Besuchers durch Deaktivieren des Browsercaches</span><span class="sxs-lookup"><span data-stu-id="020d1-135">Emulate a first-time visitor by disabling the browser cache</span></span>  

<span data-ttu-id="020d1-136">Aktivieren Sie das Kontrollkästchen **Cache deaktivieren** , um zu emulieren, wie ein Erstbenutzer Ihre Website erlebt.</span><span class="sxs-lookup"><span data-stu-id="020d1-136">To emulate how a first-time user experiences your site, check the **Disable cache** checkbox.</span></span>  <span data-ttu-id="020d1-137">DevTools deaktiviert den Browsercache.</span><span class="sxs-lookup"><span data-stu-id="020d1-137">DevTools disables the browser cache.</span></span>  <span data-ttu-id="020d1-138">Dadurch wird die Benutzererfahrung des ersten Benutzers genauer emuliert, da Anforderungen im Browsercache bei wiederholten Besuchen bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="020d1-138">This more accurately emulates a first-time user's experience, because requests are served from the browser cache on repeat visits.</span></span>  

:::image type="complex" source="../media/network-network-disable-cache-checkbox.msft.png" alt-text="Kontrollkästchen "Cache deaktivieren"" lightbox="../media/network-network-disable-cache-checkbox.msft.png":::
   <span data-ttu-id="020d1-140">Abbildung 5: Kontrollkästchen " **Cache deaktivieren** "</span><span class="sxs-lookup"><span data-stu-id="020d1-140">Figure 5:  The **Disable Cache** checkbox</span></span>  
:::image-end:::  

#### <span data-ttu-id="020d1-141">Deaktivieren des Browser-Caches aus der Schublade "Netzwerkbedingungen"</span><span class="sxs-lookup"><span data-stu-id="020d1-141">Disable the browser cache from the Network Conditions drawer</span></span>  

<span data-ttu-id="020d1-142">Wenn Sie den Cache während der Arbeit in anderen devtools-Panels deaktivieren möchten, verwenden Sie die Schublade Netzwerkbedingungen.</span><span class="sxs-lookup"><span data-stu-id="020d1-142">If you want to disable the cache while working in other DevTools panels, use the Network Conditions drawer.</span></span>  

1.  <span data-ttu-id="020d1-143">Öffnen Sie die Schublade **Netzwerkbedingungen** .</span><span class="sxs-lookup"><span data-stu-id="020d1-143">Open the **Network Conditions** drawer.</span></span>  
1.  <span data-ttu-id="020d1-144">Aktivieren oder deaktivieren Sie das Kontrollkästchen **Cache deaktivieren** .</span><span class="sxs-lookup"><span data-stu-id="020d1-144">Check or uncheck the **Disable cache** checkbox.</span></span>  

<!--todo: add network condition section when available -->  

### <span data-ttu-id="020d1-145">Manuelles Löschen des Browsercaches</span><span class="sxs-lookup"><span data-stu-id="020d1-145">Manually clear the browser cache</span></span>  

<span data-ttu-id="020d1-146">Wenn Sie den Browser-Cache jederzeit manuell löschen möchten, öffnen Sie das Kontextmenü \ (Klicken Sie mit der rechten Maustaste auf \) an einer beliebigen Stelle in der Tabelle Anforderungen, und wählen Sie **Browsercache löschen**aus.</span><span class="sxs-lookup"><span data-stu-id="020d1-146">To manually clear the browser cache at any time, open the contextual menu \(right-click\) anywhere in the Requests table and select **Clear Browser Cache**.</span></span>  

:::image type="complex" source="../media/network-network-clear-browser-cache.msft.png" alt-text="Auswählen des Browser Cache löschen" lightbox="../media/network-network-clear-browser-cache.msft.png":::
   <span data-ttu-id="020d1-148">Abbildung 6: Auswählen des **Browser Cache löschen**</span><span class="sxs-lookup"><span data-stu-id="020d1-148">Figure 6:  Selecting **Clear Browser Cache**</span></span>  
:::image-end:::  

### <span data-ttu-id="020d1-149">Offline emulieren</span><span class="sxs-lookup"><span data-stu-id="020d1-149">Emulate offline</span></span>  

<span data-ttu-id="020d1-150">Eine neue Klasse von Web-Apps mit dem Namen " [Progressive Web Apps][DevtoolsProgressiveWebApps]" funktioniert mit Hilfe von **Servicemitarbeitern**offline.</span><span class="sxs-lookup"><span data-stu-id="020d1-150">A new class of web apps, named [Progressive Web Apps][DevtoolsProgressiveWebApps], functions offline with the help of **service workers**.</span></span>  <span data-ttu-id="020d1-151">Möglicherweise ist es hilfreich, ein Gerät, das keine Datenverbindung aufweist, schnell zu simulieren, wenn Sie diese Art von App erstellen.</span><span class="sxs-lookup"><span data-stu-id="020d1-151">You may find it useful to quickly simulate a device that has no data connection when you are building this type of app.</span></span>  

<!--[ServiceWorkers]: /web/fundamentals/getting-started/primers/service-workers  -->

<span data-ttu-id="020d1-152">Wählen Sie das Dropdownmenü **Online** aus, suchen Sie unter **Voreinstellungen**, und wählen Sie **Offline** aus, um eine vollständig Offlinenetzwerk Umgebung zu simulieren.</span><span class="sxs-lookup"><span data-stu-id="020d1-152">Select the **Online** dropdown menu, search under **Presets**, and select **Offline** to simulate a completely offline network experience.</span></span>  

:::image type="complex" source="../media/network-network-offline-dropdown.msft.png" alt-text="Das Offline-Dropdownmenü" lightbox="../media/network-network-offline-dropdown.msft.png":::
   <span data-ttu-id="020d1-154">Abbildung 7: **Offline** -Dropdownmenü</span><span class="sxs-lookup"><span data-stu-id="020d1-154">Figure 7:  The **Offline** dropdown menu</span></span>  
:::image-end:::  

### <span data-ttu-id="020d1-155">Emulieren langsamer Netzwerkverbindungen</span><span class="sxs-lookup"><span data-stu-id="020d1-155">Emulate slow network connections</span></span>  

<span data-ttu-id="020d1-156">Emulieren Sie langsames 3G, fast 3G und andere Verbindungsgeschwindigkeiten über das **Online-Dropdown-** Menü.</span><span class="sxs-lookup"><span data-stu-id="020d1-156">Emulate Slow 3G, Fast 3G, and other connection speeds from the **Online** dropdown menu.</span></span>  

:::image type="complex" source="../media/network-network-throttling-menu.msft.png" alt-text="Dropdownmenü "Drosselung"" lightbox="../media/network-network-throttling-menu.msft.png":::
   <span data-ttu-id="020d1-158">Abbildung 8: das Dropdownmenü " **Drosselung** "</span><span class="sxs-lookup"><span data-stu-id="020d1-158">Figure 8:  The **Throttling** dropdown menu</span></span>  
:::image-end:::  

<span data-ttu-id="020d1-159">Sie können aus einer Vielzahl von Voreinstellungen auswählen, wie etwa langsames 3G oder fast 3G.</span><span class="sxs-lookup"><span data-stu-id="020d1-159">You may select from a variety of presets, such as Slow 3G or Fast 3G.</span></span>  <span data-ttu-id="020d1-160">Sie können auch eigene benutzerdefinierte Voreinstellungen hinzufügen, indem Sie das Menü Drosselung öffnen und **benutzerdefiniertes**  >  **Add**auswählen.</span><span class="sxs-lookup"><span data-stu-id="020d1-160">You may also add your own custom presets by opening the Throttling menu and selecting **Custom** > **Add**.</span></span>  

<span data-ttu-id="020d1-161">DevTools zeigt ein Warnungssymbol neben der Registerkarte " **Netzwerk** " an, um Sie daran zu erinnern, dass die Drosselung aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="020d1-161">DevTools displays a warning icon next to the **Network** tab to remind you that throttling is enabled.</span></span>  

#### <span data-ttu-id="020d1-162">Emulieren von langsamen Netzwerkverbindungen über die Netzwerkbedingungen Schublade</span><span class="sxs-lookup"><span data-stu-id="020d1-162">Emulate slow network connections from the Network Conditions drawer</span></span>  

<span data-ttu-id="020d1-163">Wenn Sie die Netzwerkverbindung während der Arbeit in anderen devtools-Panels Drosseln möchten, verwenden Sie den Netzwerkbedingungen-Einzug.</span><span class="sxs-lookup"><span data-stu-id="020d1-163">If you want to throttle the network connection while working in other DevTools panels, use the Network Conditions drawer.</span></span>  

1.  <span data-ttu-id="020d1-164">Öffnen Sie die Schublade **Netzwerkbedingungen** .</span><span class="sxs-lookup"><span data-stu-id="020d1-164">Open the **Network Conditions** drawer.</span></span>  
1.  <span data-ttu-id="020d1-165">Wählen Sie die gewünschte Verbindungsgeschwindigkeit im Menü " **Drosselung** " aus.</span><span class="sxs-lookup"><span data-stu-id="020d1-165">Select your desired connection speed from the **Throttling** menu.</span></span>  

<!--todo: add network condition section when available -->  

### <span data-ttu-id="020d1-166">Manuelles Löschen von Browser-Cookies</span><span class="sxs-lookup"><span data-stu-id="020d1-166">Manually clear browser cookies</span></span>  

<span data-ttu-id="020d1-167">Wenn Sie Browser-Cookies jederzeit manuell löschen möchten, öffnen Sie das Kontextmenü \ (Klicken Sie mit der rechten Maustaste auf \) an einer beliebigen Stelle in der Tabelle Anforderungen, und wählen Sie **Browser-Cookies löschen**aus.</span><span class="sxs-lookup"><span data-stu-id="020d1-167">To manually clear browser cookies at any time, open the contextual menu \(right-click\) anywhere in the Requests table and select **Clear Browser Cookies**.</span></span>  

:::image type="complex" source="../media/network-network-clear-browser-cookies.msft.png" alt-text="Auswählen von Browser-Cookies löschen" lightbox="../media/network-network-clear-browser-cookies.msft.png":::
   <span data-ttu-id="020d1-169">Abbildung 9: Auswählen von **Browser-Cookies löschen**</span><span class="sxs-lookup"><span data-stu-id="020d1-169">Figure 9:  Selecting **Clear Browser Cookies**</span></span>  
:::image-end:::  

### <span data-ttu-id="020d1-170">Überschreiben des Benutzer-Agents</span><span class="sxs-lookup"><span data-stu-id="020d1-170">Override the user agent</span></span>  

<span data-ttu-id="020d1-171">So überschreiben Sie den Benutzer-Agent manuell:</span><span class="sxs-lookup"><span data-stu-id="020d1-171">To manually override the user agent:</span></span>  

1.  <span data-ttu-id="020d1-172">Öffnen Sie die Schublade **Netzwerkbedingungen** .</span><span class="sxs-lookup"><span data-stu-id="020d1-172">Open the **Network Conditions** drawer.</span></span>  
1.  <span data-ttu-id="020d1-173">Deaktivieren **Sie SELECT automatisch**.</span><span class="sxs-lookup"><span data-stu-id="020d1-173">Uncheck **Select automatically**.</span></span>  
1.  <span data-ttu-id="020d1-174">Wählen Sie eine Option für den Benutzer-Agent aus dem Menü aus, oder geben Sie eine benutzerdefinierte Option in das Textfeld ein.</span><span class="sxs-lookup"><span data-stu-id="020d1-174">Choose a user agent option from the menu, or enter a custom one in the text box.</span></span>  

<!--todo: add network condition section when available -->  

## <span data-ttu-id="020d1-175">Filter Anforderungen</span><span class="sxs-lookup"><span data-stu-id="020d1-175">Filter requests</span></span>  

### <span data-ttu-id="020d1-176">Filtern von Anforderungen nach Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="020d1-176">Filter requests by properties</span></span>  

<span data-ttu-id="020d1-177">Verwenden Sie das Textfeld **Filtern** , um Anforderungen nach Eigenschaften wie der Domäne oder der Größe der Anforderung zu filtern.</span><span class="sxs-lookup"><span data-stu-id="020d1-177">Use the **Filter** text box to filter requests by properties, such as the domain or size of the request.</span></span>  

<span data-ttu-id="020d1-178">Wenn das Textfeld nicht angezeigt wird, ist der Bereich Filter wahrscheinlich ausgeblendet.</span><span class="sxs-lookup"><span data-stu-id="020d1-178">If you do not see the text box, the Filters pane is probably hidden.</span></span>  
<span data-ttu-id="020d1-179">Weitere Informationen finden Sie unter [Ausblenden des Filters-Bereichs](#hide-the-filters-pane).</span><span class="sxs-lookup"><span data-stu-id="020d1-179">See [Hide the Filters pane](#hide-the-filters-pane).</span></span>  

:::image type="complex" source="../media/network-network-filters-textbox.msft.png" alt-text="Das Textfeld "Filter"" lightbox="../media/network-network-filters-textbox.msft.png":::
   <span data-ttu-id="020d1-181">Abbildung 10: das Textfeld " **Filter** "</span><span class="sxs-lookup"><span data-stu-id="020d1-181">Figure 10:  The **Filter** text box</span></span>  
:::image-end:::  

<span data-ttu-id="020d1-182">Sie können mehrere Eigenschaften gleichzeitig verwenden, indem Sie jede Eigenschaft mit einem Leerzeichen voneinander trennen.</span><span class="sxs-lookup"><span data-stu-id="020d1-182">You may use multiple properties simultaneously by separating each property with a space.</span></span>  <span data-ttu-id="020d1-183">Zeigt beispielsweise `mime-type:image/png larger-than:1K` alle PNGs an, die größer als ein Kilobyte sind.</span><span class="sxs-lookup"><span data-stu-id="020d1-183">For example, `mime-type:image/png larger-than:1K` displays all PNGs that are larger than one kilobyte.</span></span>  <span data-ttu-id="020d1-184">Diese Filter mit mehreren Eigenschaften sind äquivalent zu `AND` Vorgängen.</span><span class="sxs-lookup"><span data-stu-id="020d1-184">These multi-property filters are equivalent to `AND` operations.</span></span>  `OR` <span data-ttu-id="020d1-185">Vorgänge werden zurzeit nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="020d1-185">operations are currently not supported.</span></span>  

<span data-ttu-id="020d1-186">Die vollständige Liste der unterstützten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="020d1-186">The complete list of supported properties.</span></span>  

| <span data-ttu-id="020d1-187">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="020d1-187">Property</span></span> | <span data-ttu-id="020d1-188">Details</span><span class="sxs-lookup"><span data-stu-id="020d1-188">Details</span></span> |  
|:--- | :--- |  
| `domain` | <span data-ttu-id="020d1-189">Zeigt nur Ressourcen aus der angegebenen Domäne an.</span><span class="sxs-lookup"><span data-stu-id="020d1-189">Only display resources from the specified domain.</span></span>  <span data-ttu-id="020d1-190">Sie können ein Platzhalterzeichen \ ( `*` \) verwenden, um mehrere Domänen einzubeziehen.</span><span class="sxs-lookup"><span data-stu-id="020d1-190">You may use a wildcard character \(`*`\) to include multiple domains.</span></span>  <span data-ttu-id="020d1-191">Zeigt beispielsweise `*.com` Ressourcen aus allen Domänennamen an, die in endet `.com` .</span><span class="sxs-lookup"><span data-stu-id="020d1-191">For example, `*.com` displays resources from all domain names ending in `.com`.</span></span>  <span data-ttu-id="020d1-192">DevTools füllt das Dropdownmenü AutoVervollständigen mit allen Domänen auf, die es gefunden hat.</span><span class="sxs-lookup"><span data-stu-id="020d1-192">DevTools populates the autocomplete dropdown menu with all of the domains it has encountered.</span></span> |  
| `has-response-header` | <span data-ttu-id="020d1-193">Anzeigen der Ressourcen, die den angegebenen HTTP-Antwortheader enthalten</span><span class="sxs-lookup"><span data-stu-id="020d1-193">Show the resources that contain the specified HTTP response header.</span></span>  <span data-ttu-id="020d1-194">DevTools füllt die Dropdownliste AutoVervollständigen mit allen Antwortheadern auf, die Sie gefunden hat.</span><span class="sxs-lookup"><span data-stu-id="020d1-194">DevTools populates the autocomplete dropdown with all of the response headers that it has encountered.</span></span> |  
| `is` | <span data-ttu-id="020d1-195">Verwendet `is:running` , um `WebSocket` Ressourcen zu finden.</span><span class="sxs-lookup"><span data-stu-id="020d1-195">Use `is:running` to find `WebSocket` resources.</span></span> |  
| `larger-than` | <span data-ttu-id="020d1-196">Zeigen Sie Ressourcen an, die größer als die angegebene Größe in Bytes sind.</span><span class="sxs-lookup"><span data-stu-id="020d1-196">Show resources that are larger than the specified size, in bytes.</span></span>  <span data-ttu-id="020d1-197">Das Festlegen eines Werts von entspricht dem `1000` Festlegen eines Werts von `1k` .</span><span class="sxs-lookup"><span data-stu-id="020d1-197">Setting a value of `1000` is equivalent to setting a value of `1k`.</span></span> |  
| `method` | <span data-ttu-id="020d1-198">Zeigen Sie Ressourcen an, die über einen angegebenen http-Methodentyp abgerufen wurden.</span><span class="sxs-lookup"><span data-stu-id="020d1-198">Show resources that were retrieved over a specified HTTP method type.</span></span>  <span data-ttu-id="020d1-199">DevTools füllt die Dropdownliste mit allen HTTP-Methoden auf, die Sie gefunden hat.</span><span class="sxs-lookup"><span data-stu-id="020d1-199">DevTools populates the dropdown with all of the HTTP methods it has encountered.</span></span> |  
| `mime-type` | <span data-ttu-id="020d1-200">Anzeigen von Ressourcen eines angegebenen MIME-Typs</span><span class="sxs-lookup"><span data-stu-id="020d1-200">Show resources of a specified MIME type.</span></span>  <span data-ttu-id="020d1-201">DevTools füllt die Dropdownliste mit allen MIME-Typen auf, die Sie gefunden hat.</span><span class="sxs-lookup"><span data-stu-id="020d1-201">DevTools populates the dropdown with all MIME types it has encountered.</span></span> |  
| `mixed-content` | <span data-ttu-id="020d1-202">Alle gemischten Inhalts Ressourcen anzeigen \ ( `mixed-content:all` \) oder nur diejenigen, die aktuell angezeigt werden \ ( `mixed-content:displayed` \).</span><span class="sxs-lookup"><span data-stu-id="020d1-202">Show all mixed content resources \(`mixed-content:all`\) or just the ones that are currently displayed \(`mixed-content:displayed`\).</span></span> |  
| `scheme` | <span data-ttu-id="020d1-203">Zeigt Ressourcen an, die über ungeschützten http \ ( `scheme:http` \) oder geschütztes HTTPS \ ( `scheme:https` \) abgerufen wurden.</span><span class="sxs-lookup"><span data-stu-id="020d1-203">Show resources retrieved over unprotected HTTP \(`scheme:http`\) or protected HTTPS \(`scheme:https`\).</span></span> |  
| `set-cookie-domain` | <span data-ttu-id="020d1-204">Zeigen Sie die Ressourcen mit einer `Set-Cookie` Kopfzeile mit einem `Domain` Attribut an, das dem angegebenen Wert entspricht.</span><span class="sxs-lookup"><span data-stu-id="020d1-204">Show the resources that have a `Set-Cookie` header with a `Domain` attribute that matches the specified value.</span></span>  <span data-ttu-id="020d1-205">DevTools füllt das AutoVervollständigen mit allen Cookie-Domänen auf, die es gefunden hat.</span><span class="sxs-lookup"><span data-stu-id="020d1-205">DevTools populates the autocomplete with all of the cookie domains that it has encountered.</span></span> |  
| `set-cookie-name` | <span data-ttu-id="020d1-206">Zeigen Sie die Ressourcen mit einer `Set-Cookie` Kopfzeile mit einem Namen an, der dem angegebenen Wert entspricht.</span><span class="sxs-lookup"><span data-stu-id="020d1-206">Show the resources that have a `Set-Cookie` header with a name that matches the specified value.</span></span>  <span data-ttu-id="020d1-207">DevTools füllt das AutoVervollständigen mit allen Cookie-Namen auf, die es gefunden hat.</span><span class="sxs-lookup"><span data-stu-id="020d1-207">DevTools populates the autocomplete with all of the cookie names that it has encountered.</span></span> |  
| `set-cookie-value` | <span data-ttu-id="020d1-208">Zeigen Sie die Ressourcen mit einer `Set-Cookie` Kopfzeile mit einem Wert an, der dem angegebenen Wert entspricht.</span><span class="sxs-lookup"><span data-stu-id="020d1-208">Show the resources that have a `Set-Cookie` header with a value that matches the specified value.</span></span>  <span data-ttu-id="020d1-209">DevTools füllt das AutoVervollständigen mit allen Cookie-Werten auf, die es gefunden hat.</span><span class="sxs-lookup"><span data-stu-id="020d1-209">DevTools populates the autocomplete with all of the cookie values that it has encountered.</span></span> |  
| `status-code` | <span data-ttu-id="020d1-210">Nur die Ressourcen anzeigen, für die der HTTP-Statuscode mit dem angegebenen Code übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="020d1-210">Show only the resources for which the HTTP status code matches the specified code.</span></span>  <span data-ttu-id="020d1-211">DevTools füllt das Dropdownmenü AutoVervollständigen mit allen Statuscodes auf, die es gefunden hat.</span><span class="sxs-lookup"><span data-stu-id="020d1-211">DevTools populates the autocomplete dropdown menu with all of the status codes it has encountered.</span></span> |  

### <span data-ttu-id="020d1-212">Filtern von Anforderungen nach Typ</span><span class="sxs-lookup"><span data-stu-id="020d1-212">Filter requests by type</span></span>  

<span data-ttu-id="020d1-213">Wenn Sie Anforderungen nach Anforderungsfiltern möchten, wählen Sie die Schaltflächen **XMLHttpRequest**, **js**, **CSS**, **IMG**, **Media**, **Font**, **doc**, **WS** \ (WebSocket \), **Manifest**oder **andere** \ (alle anderen Typen, die hier nicht aufgelistet sind) im Netzwerk Panel aus.</span><span class="sxs-lookup"><span data-stu-id="020d1-213">To filter requests by request type, select the **XHR**, **JS**, **CSS**, **Img**, **Media**, **Font**, **Doc**, **WS** \(WebSocket\), **Manifest**, or **Other** \(any other type not listed here\) buttons on the Network panel.</span></span>  

<span data-ttu-id="020d1-214">Wenn diese Schaltflächen nicht angezeigt werden, ist der Bereich Filter wahrscheinlich ausgeblendet.</span><span class="sxs-lookup"><span data-stu-id="020d1-214">If you do not see these buttons, the Filters pane is probably hidden.</span></span>  
<span data-ttu-id="020d1-215">Weitere Informationen finden Sie unter [Ausblenden des Filters-Bereichs](#hide-the-filters-pane).</span><span class="sxs-lookup"><span data-stu-id="020d1-215">See [Hide the Filters pane](#hide-the-filters-pane).</span></span>  

<span data-ttu-id="020d1-216">Wenn Sie mehrere Typfilter gleichzeitig aktivieren möchten, halten `Control` Sie \ (Windows \) oder `Command` \ (macOS \) gedrückt, und wählen Sie dann aus.</span><span class="sxs-lookup"><span data-stu-id="020d1-216">To enable multiple type filters simultaneously, hold `Control` \(Windows\) or `Command` \(macOS\) and then select.</span></span>  

:::image type="complex" source="../media/network-network-type-filters.msft.png" alt-text="Verwenden des Typs "Filter" zum Anzeigen von JS-, CSS-und Dokument Ressourcen" lightbox="../media/network-network-type-filters.msft.png":::
   <span data-ttu-id="020d1-218">Abbildung 11: Verwenden der Typfilter zum Anzeigen von JS-, CSS-und Dokument Ressourcen</span><span class="sxs-lookup"><span data-stu-id="020d1-218">Figure 11:  Using the Type filters to display JS, CSS, and Document resources</span></span>  
:::image-end:::  

### <span data-ttu-id="020d1-219">Filtern von Anforderungen nach Zeit</span><span class="sxs-lookup"><span data-stu-id="020d1-219">Filter requests by time</span></span>  

<span data-ttu-id="020d1-220">Wählen Sie aus, und ziehen Sie im Übersichtsbereich nach links oder rechts, um nur Anforderungen anzuzeigen, die während dieses Zeitrahmens aktiv waren.</span><span class="sxs-lookup"><span data-stu-id="020d1-220">Select and drag left or right on the Overview pane to only display requests that were active during that time frame.</span></span>  <span data-ttu-id="020d1-221">Der Filter ist inklusive.</span><span class="sxs-lookup"><span data-stu-id="020d1-221">The filter is inclusive.</span></span>  <span data-ttu-id="020d1-222">Jede Anforderung, die während der hervorgehobenen Zeit aktiv war, wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="020d1-222">Any request that was active during the highlighted time is shown.</span></span>  

:::image type="complex" source="../media/network-network-overview-filter.msft.png" alt-text="Herausfiltern von Anforderungen, die um 300 m inaktiv waren" lightbox="../media/network-network-overview-filter.msft.png":::
   <span data-ttu-id="020d1-224">Abbildung 12: Filtern von Anforderungen, die um 300 m inaktiv waren</span><span class="sxs-lookup"><span data-stu-id="020d1-224">Figure 12:  Filtering out any requests that were inactive around 300ms</span></span>  
:::image-end:::  

### <span data-ttu-id="020d1-225">Ausblenden von Daten-URLs</span><span class="sxs-lookup"><span data-stu-id="020d1-225">Hide data URLs</span></span>  

<span data-ttu-id="020d1-226">[Daten-URLs][MDNHTTPDataURIs] sind kleine Dateien, die in andere Dokumente eingebettet sind.</span><span class="sxs-lookup"><span data-stu-id="020d1-226">[Data URLs][MDNHTTPDataURIs] are small files embedded into other documents.</span></span>  <span data-ttu-id="020d1-227">Jede Anforderung, die Sie in der Tabelle Anforderungen sehen, die mit beginnt, `data:` ist eine Daten-URL.</span><span class="sxs-lookup"><span data-stu-id="020d1-227">Any request that you see in the Requests table that starts with `data:` is a data URL.</span></span>  

<span data-ttu-id="020d1-228">Aktivieren Sie das Kontrollkästchen **Daten-URLs ausblenden** , um die Anforderungen auszublenden.</span><span class="sxs-lookup"><span data-stu-id="020d1-228">Check the **Hide data URLs** checkbox to hide the requests.</span></span>  

:::image type="complex" source="../media/network-network-hide-data-urls.msft.png" alt-text="Das Kontrollkästchen "Daten-URLs ausblenden"" lightbox="../media/network-network-hide-data-urls.msft.png":::
   <span data-ttu-id="020d1-230">Abbildung 13: Kontrollkästchen " **Daten-URLs ausblenden** "</span><span class="sxs-lookup"><span data-stu-id="020d1-230">Figure 13:  The **Hide Data URLs** checkbox</span></span>  
:::image-end:::  

## <span data-ttu-id="020d1-231">Sortieren von Anforderungen</span><span class="sxs-lookup"><span data-stu-id="020d1-231">Sort requests</span></span>  

<span data-ttu-id="020d1-232">Standardmäßig werden die Anforderungen in der Tabelle Anforderungen nach Initiierungs Zeit sortiert, aber Sie können die Tabelle mit anderen Kriterien sortieren.</span><span class="sxs-lookup"><span data-stu-id="020d1-232">By default, the requests in the Requests table are sorted by initiation time, but you may sort the table using other criteria.</span></span>  

### <span data-ttu-id="020d1-233">Nach Spalte sortieren</span><span class="sxs-lookup"><span data-stu-id="020d1-233">Sort by column</span></span>  

<span data-ttu-id="020d1-234">Wählen Sie die Kopfzeile einer beliebigen Spalte in den Anforderungen aus, um Anforderungen nach dieser Spalte zu sortieren.</span><span class="sxs-lookup"><span data-stu-id="020d1-234">Select the header of any column in the Requests to sort requests by that column.</span></span>  

### <span data-ttu-id="020d1-235">Nach Aktivitätsphase sortieren</span><span class="sxs-lookup"><span data-stu-id="020d1-235">Sort by activity phase</span></span>  

<span data-ttu-id="020d1-236">Wenn Sie ändern möchten, wie der Wasserfall Anforderungen sortiert, zeigen Sie auf die Kopfzeile der Tabelle Anforderungen, öffnen Sie das Kontextmenü \ (Klicken Sie mit der rechten Maustaste auf \), zeigen Sie mit der Maus auf **Wasserfall**, und wählen Sie eine der folgenden Optionen aus.</span><span class="sxs-lookup"><span data-stu-id="020d1-236">To change how the Waterfall sorts requests, hover on the header of the Requests table, open the contextual menu \(right-click\), hover over **Waterfall**, and select one of the following options.</span></span>  

*   <span data-ttu-id="020d1-237">**Startzeit**.</span><span class="sxs-lookup"><span data-stu-id="020d1-237">**Start Time**.</span></span>  <span data-ttu-id="020d1-238">Die erste Anforderung, die initiiert wurde, ist oben.</span><span class="sxs-lookup"><span data-stu-id="020d1-238">The first request that was initiated is at the top.</span></span>  
*   <span data-ttu-id="020d1-239">**Antwortzeit**.</span><span class="sxs-lookup"><span data-stu-id="020d1-239">**Response Time**.</span></span>  <span data-ttu-id="020d1-240">Die erste Anforderung, die den Download begonnen hat, ist ganz oben.</span><span class="sxs-lookup"><span data-stu-id="020d1-240">The first request that started downloading is at the top.</span></span>  
*   <span data-ttu-id="020d1-241">**Endzeit**.</span><span class="sxs-lookup"><span data-stu-id="020d1-241">**End Time**.</span></span>  <span data-ttu-id="020d1-242">Die erste abgeschlossene Anforderung ist oben.</span><span class="sxs-lookup"><span data-stu-id="020d1-242">The first request that finished is at the top.</span></span>  
*   <span data-ttu-id="020d1-243">**Gesamtdauer**.</span><span class="sxs-lookup"><span data-stu-id="020d1-243">**Total Duration**.</span></span>  <span data-ttu-id="020d1-244">Die Anforderung mit der kürzesten Verbindungseinrichtung und Anforderung/Antwort ist oben.</span><span class="sxs-lookup"><span data-stu-id="020d1-244">The request with the shortest connection setup and request / response is at the top.</span></span>  
*   <span data-ttu-id="020d1-245">**Latenz**.</span><span class="sxs-lookup"><span data-stu-id="020d1-245">**Latency**.</span></span>  <span data-ttu-id="020d1-246">Die Anforderung, die die kürzeste Zeit für eine Antwort gewartet hat, ist oben.</span><span class="sxs-lookup"><span data-stu-id="020d1-246">The request that waited the shortest time for a response is at the top.</span></span>  

<span data-ttu-id="020d1-247">Bei diesen Beschreibungen wird davon ausgegangen, dass die jeweilige Option von kürzester bis längster Position bewertet wird.</span><span class="sxs-lookup"><span data-stu-id="020d1-247">These descriptions assume that each respective option is ranked from shortest to longest.</span></span>  <span data-ttu-id="020d1-248">Wenn Sie die Kopfzeile der Spalte **Wasserfall** auswählen, wird die Reihenfolge umgekehrt.</span><span class="sxs-lookup"><span data-stu-id="020d1-248">Selecting the header of the **Waterfall** column reverses the order.</span></span>  

:::image type="complex" source="../media/network-network-waterfall-total-duration.msft.png" alt-text="Sortieren des Wasserfalls nach Gesamtdauer" lightbox="../media/network-network-waterfall-total-duration.msft.png":::
   <span data-ttu-id="020d1-250">Abbildung 14: Sortieren des Wasserfalls nach Gesamtdauer \ (der leichtere Teil der einzelnen Balken ist die Zeit, die gewartet wird, und der dunklere Teil ist die Zeit, die zum Herunterladen von Bytes verwendet wird \)</span><span class="sxs-lookup"><span data-stu-id="020d1-250">Figure 14:  Sorting the Waterfall by total duration  \(The lighter portion of each bar is time spent waiting and the darker portion is time spent downloading bytes\)</span></span>  
:::image-end:::  

## <span data-ttu-id="020d1-251">Analysieren von Anforderungen</span><span class="sxs-lookup"><span data-stu-id="020d1-251">Analyze requests</span></span>  

<span data-ttu-id="020d1-252">Solange devtools geöffnet ist, werden alle Anforderungen im Netzwerk Panel protokolliert.</span><span class="sxs-lookup"><span data-stu-id="020d1-252">So long as DevTools is open, it logs all requests in the Network panel.</span></span>  
<span data-ttu-id="020d1-253">Verwenden Sie das Netzwerk Panel, um Anforderungen zu analysieren.</span><span class="sxs-lookup"><span data-stu-id="020d1-253">Use the Network panel to analyze requests.</span></span>  

### <span data-ttu-id="020d1-254">Anzeigen eines Protokolls der Anforderungen</span><span class="sxs-lookup"><span data-stu-id="020d1-254">View a log of requests</span></span>  

<span data-ttu-id="020d1-255">Verwenden Sie die Tabelle "Anforderungen", um ein Protokoll aller Anforderungen anzuzeigen, die während der devtools geöffnet wurden.</span><span class="sxs-lookup"><span data-stu-id="020d1-255">Use the Requests table to view a log of all requests made while DevTools has been open.</span></span>  <span data-ttu-id="020d1-256">Wenn Sie über Anforderungen auswählen oder darauf zeigen, werden weitere Informationen zu den einzelnen Elementen eingeblendet.</span><span class="sxs-lookup"><span data-stu-id="020d1-256">Selecting or hovering over requests reveals more information about each item.</span></span>  

:::image type="complex" source="../media/network-network-requests-table.msft.png" alt-text="Die Tabelle "Anforderungen"" lightbox="../media/network-network-requests-table.msft.png":::
   <span data-ttu-id="020d1-258">Abbildung 15: die Tabelle "Anforderungen"</span><span class="sxs-lookup"><span data-stu-id="020d1-258">Figure 15:  The Requests table</span></span>  
:::image-end:::  

<span data-ttu-id="020d1-259">In der Tabelle Anforderungen werden standardmäßig die folgenden Spalten angezeigt.</span><span class="sxs-lookup"><span data-stu-id="020d1-259">The Requests table displays the following columns by default.</span></span>  

*   <span data-ttu-id="020d1-260">**Name**</span><span class="sxs-lookup"><span data-stu-id="020d1-260">**Name**.</span></span>  <span data-ttu-id="020d1-261">Der Dateiname von oder ein Bezeichner für die Ressource.</span><span class="sxs-lookup"><span data-stu-id="020d1-261">The filename of, or an identifier for, the resource.</span></span>  
*   <span data-ttu-id="020d1-262">**Status**aus.</span><span class="sxs-lookup"><span data-stu-id="020d1-262">**Status**.</span></span>  <span data-ttu-id="020d1-263">Der HTTP-Statuscode.</span><span class="sxs-lookup"><span data-stu-id="020d1-263">The HTTP status code.</span></span>  
*   <span data-ttu-id="020d1-264">**Typ**.</span><span class="sxs-lookup"><span data-stu-id="020d1-264">**Type**.</span></span>  <span data-ttu-id="020d1-265">Der MIME-Typ der angeforderten Ressource.</span><span class="sxs-lookup"><span data-stu-id="020d1-265">The MIME type of the requested resource.</span></span>  
*   <span data-ttu-id="020d1-266">**Initiator**.</span><span class="sxs-lookup"><span data-stu-id="020d1-266">**Initiator**.</span></span>  <span data-ttu-id="020d1-267">Die folgenden Objekte oder Prozesse initiieren Anforderungen:</span><span class="sxs-lookup"><span data-stu-id="020d1-267">The following objects or processes initiate requests:</span></span>  
    *   <span data-ttu-id="020d1-268">**Parser**aus.</span><span class="sxs-lookup"><span data-stu-id="020d1-268">**Parser**.</span></span>  <span data-ttu-id="020d1-269">Der HTML-Parser für Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="020d1-269">The HTML parser for Microsoft Edge.</span></span>  
    *   <span data-ttu-id="020d1-270">**Umleiten**.</span><span class="sxs-lookup"><span data-stu-id="020d1-270">**Redirect**.</span></span>  <span data-ttu-id="020d1-271">Eine HTTP-Umleitung.</span><span class="sxs-lookup"><span data-stu-id="020d1-271">An HTTP redirect.</span></span>  
    *   <span data-ttu-id="020d1-272">**Skript**aus.</span><span class="sxs-lookup"><span data-stu-id="020d1-272">**Script**.</span></span>  <span data-ttu-id="020d1-273">Eine JavaScript-Funktion.</span><span class="sxs-lookup"><span data-stu-id="020d1-273">A JavaScript function.</span></span>  
    *   <span data-ttu-id="020d1-274">**Andere**.</span><span class="sxs-lookup"><span data-stu-id="020d1-274">**Other**.</span></span>  <span data-ttu-id="020d1-275">Einige andere Prozesse oder Aktionen, wie das Navigieren zu einer Seite über einen Link oder das Eingeben einer URL in die Adressleiste.</span><span class="sxs-lookup"><span data-stu-id="020d1-275">Some other process or action, such as navigating to a page via a link or entering a URL in the address bar.</span></span>  
*   <span data-ttu-id="020d1-276">**Größe**aus.</span><span class="sxs-lookup"><span data-stu-id="020d1-276">**Size**.</span></span>  <span data-ttu-id="020d1-277">Die kombinierte Größe der Antwortheader sowie des Antworttexts, wie vom Server bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="020d1-277">The combined size of the response headers plus the response body, as delivered by the server.</span></span>  
*   <span data-ttu-id="020d1-278">**Zeit**.</span><span class="sxs-lookup"><span data-stu-id="020d1-278">**Time**.</span></span>  <span data-ttu-id="020d1-279">Die Gesamtdauer vom Anfang der Anforderung bis zum Empfang des letzten Bytes in der Antwort.</span><span class="sxs-lookup"><span data-stu-id="020d1-279">The total duration, from the start of the request to the receipt of the final byte in the response.</span></span>  
*   <span data-ttu-id="020d1-280">[**Wasserfall**](#view-the-timing-of-requests-in-relation-to-one-another).</span><span class="sxs-lookup"><span data-stu-id="020d1-280">[**Waterfall**](#view-the-timing-of-requests-in-relation-to-one-another).</span></span>  <span data-ttu-id="020d1-281">Eine visuelle Gliederung der Aktivität für jede Anforderung.</span><span class="sxs-lookup"><span data-stu-id="020d1-281">A visual breakdown of the activity for each request.</span></span>  

#### <span data-ttu-id="020d1-282">Hinzufügen oder Entfernen von Spalten</span><span class="sxs-lookup"><span data-stu-id="020d1-282">Add or remove columns</span></span>  

<span data-ttu-id="020d1-283">Zeigen Sie auf die Kopfzeile der Tabelle Anforderungen, öffnen Sie das Kontextmenü \ (Klicken Sie mit der rechten Maustaste auf \), und wählen Sie eine Option aus, um sie auszublenden oder anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="020d1-283">Hover on the header of the Requests table, open the contextual menu \(right-click\), and select an option to hide or show it.</span></span>  <span data-ttu-id="020d1-284">Die aktuell angezeigten Optionen verfügen über Kontrollkästchen neben den einzelnen Elementen.</span><span class="sxs-lookup"><span data-stu-id="020d1-284">Currently displayed options have checkmarks next to each item.</span></span>  

:::image type="complex" source="../media/network-network-requests-add-column.msft.png" alt-text="Hinzufügen einer Spalte zur Tabelle "Anforderungen"" lightbox="../media/network-network-requests-add-column.msft.png":::
   <span data-ttu-id="020d1-286">Abbildung 16: Hinzufügen einer Spalte zur Tabelle "Anforderungen"</span><span class="sxs-lookup"><span data-stu-id="020d1-286">Figure 16:  Adding a column to the Requests table</span></span>  
:::image-end:::  

#### <span data-ttu-id="020d1-287">Hinzufügen benutzerdefinierter Spalten</span><span class="sxs-lookup"><span data-stu-id="020d1-287">Add custom columns</span></span>  

<span data-ttu-id="020d1-288">Wenn Sie der Tabelle Anforderungen eine benutzerdefinierte Spalte hinzufügen möchten, zeigen Sie auf die Kopfzeile der Tabelle Anforderungen, öffnen Sie das Kontextmenü \ (Klicken Sie mit der rechten Maustaste auf \), und wählen Sie **Antwortheader**  >  **Verwalten von Kopfzeilen Spalten**aus.</span><span class="sxs-lookup"><span data-stu-id="020d1-288">To add a custom column to the Requests table, hover on the header of the Requests table, open the contextual menu \(right-click\), and select **Response Headers** > **Manage Header Columns**.</span></span>  

:::image type="complex" source="../media/network-network-requests-add-custom.msft.png" alt-text="Hinzufügen einer benutzerdefinierten Spalte zur Tabelle "Anforderungen"" lightbox="../media/network-network-requests-add-custom.msft.png":::
   <span data-ttu-id="020d1-290">Abbildung 17: Hinzufügen einer benutzerdefinierten Spalte zur Tabelle "Anforderungen"</span><span class="sxs-lookup"><span data-stu-id="020d1-290">Figure 17:  Adding a custom column to the Requests table</span></span>  
:::image-end:::  

### <span data-ttu-id="020d1-291">Anzeigen der Anzeigedauer von Anforderungen im Verhältnis zueinander</span><span class="sxs-lookup"><span data-stu-id="020d1-291">View the timing of requests in relation to one another</span></span>  

<span data-ttu-id="020d1-292">Verwenden Sie den Wasserfall, um die Anzeigedauer von Anforderungen im Verhältnis zueinander anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="020d1-292">Use the Waterfall to view the timing of requests in relation to one another.</span></span>  
<span data-ttu-id="020d1-293">Standardmäßig wird der Wasserfall nach dem Anfangszeitpunkt der Anforderungen organisiert.</span><span class="sxs-lookup"><span data-stu-id="020d1-293">By default, the Waterfall is organized by the start time of the requests.</span></span>  
<span data-ttu-id="020d1-294">Anfragen, die weiter Links sind, wurden früher als die weiter rechts eingegangenen Anforderungen gestartet.</span><span class="sxs-lookup"><span data-stu-id="020d1-294">So, requests that are farther to the left started earlier than those that are farther to the right.</span></span>  

<span data-ttu-id="020d1-295">Sehen Sie sich die verschiedenen Arten an, wie Sie den Wasserfall sortieren können, [indem Sie nach Aktivitätsphase sortieren](#sort-by-activity-phase) .</span><span class="sxs-lookup"><span data-stu-id="020d1-295">See [Sort by activity phase](#sort-by-activity-phase) to see the different ways that you may sort the Waterfall.</span></span>  

:::image type="complex" source="../media/network-network-requests-waterfall.msft.png" alt-text="Spalte "Wasserfall" im Bereich "Anforderungen"" lightbox="../media/network-network-requests-waterfall.msft.png":::
   <span data-ttu-id="020d1-297">Abbildung 18: Spalte "Wasserfall" im Bereich " **Anforderungen** "</span><span class="sxs-lookup"><span data-stu-id="020d1-297">Figure 18:  The Waterfall column of the **Requests** pane</span></span>  
:::image-end:::  

<!-- ### Analyze the frames of a WebSocket Connection  -->

<!--To view the frames of a WebSocket connection:  

1.  Select the URL of the WebSocket connection, under the **Name** column of the Requests table.  
1.  Select the **Frames** tab.  The table shows the last 100 frames.  

To refresh the table, re-select the name of the WebSocket connection under the **Name** column of the Requests table.  -->

<!--
:::image type="complex" source="../media/network-frames.msft.png" alt-text="The Frames tab" lightbox="../media/network-frames.msft.png":::
   Old Figure 20:  The **Frames** tab  
:::image-end:::  
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

### <span data-ttu-id="020d1-298">Anzeigen einer Vorschau eines Antworttexts</span><span class="sxs-lookup"><span data-stu-id="020d1-298">View a preview of a response body</span></span>  

<span data-ttu-id="020d1-299">So zeigen Sie eine Vorschau eines Antworttexts an:</span><span class="sxs-lookup"><span data-stu-id="020d1-299">To view a preview of a response body:</span></span>  

1.  <span data-ttu-id="020d1-300">Wählen Sie die URL der Anforderung unter der Spalte **Name** der Tabelle Anforderungen aus.</span><span class="sxs-lookup"><span data-stu-id="020d1-300">Select the URL of the request, under the **Name** column of the Requests table.</span></span>  
1.  <span data-ttu-id="020d1-301">Wählen Sie die Registerkarte **Vorschau** aus.</span><span class="sxs-lookup"><span data-stu-id="020d1-301">Select the **Preview** tab.</span></span>  

<span data-ttu-id="020d1-302">Diese Registerkarte ist hauptsächlich für die Anzeige von Bildern hilfreich.</span><span class="sxs-lookup"><span data-stu-id="020d1-302">This tab is mostly useful for viewing images.</span></span>  

:::image type="complex" source="../media/network-network-resources-preview.msft.png" alt-text="Registerkarte "Vorschau"" lightbox="../media/network-network-resources-preview.msft.png":::
   <span data-ttu-id="020d1-304">Abbildung 19: Registerkarte " **Vorschau** "</span><span class="sxs-lookup"><span data-stu-id="020d1-304">Figure 19:  The **Preview** tab</span></span>  
:::image-end:::  

### <span data-ttu-id="020d1-305">Anzeigen eines Antworttexts</span><span class="sxs-lookup"><span data-stu-id="020d1-305">View a response body</span></span>  

<span data-ttu-id="020d1-306">So zeigen Sie den Antworttext auf eine Anforderung an:</span><span class="sxs-lookup"><span data-stu-id="020d1-306">To view the response body to a request:</span></span>  

1.  <span data-ttu-id="020d1-307">Wählen Sie die URL der Anforderung unter der Spalte **Name** der Tabelle Anforderungen aus.</span><span class="sxs-lookup"><span data-stu-id="020d1-307">Select the URL of the request, under the **Name** column of the Requests table.</span></span>  
1.  <span data-ttu-id="020d1-308">Wählen Sie die Registerkarte **Antwort** aus.</span><span class="sxs-lookup"><span data-stu-id="020d1-308">Select the **Response** tab.</span></span>  

:::image type="complex" source="../media/network-network-resources-response.msft.png" alt-text="Die Registerkarte "Antwort"" lightbox="../media/network-network-resources-response.msft.png":::
   <span data-ttu-id="020d1-310">Abbildung 20: die Registerkarte " **Antwort** "</span><span class="sxs-lookup"><span data-stu-id="020d1-310">Figure 20:  The **Response** tab</span></span>  
:::image-end:::  

### <span data-ttu-id="020d1-311">Anzeigen von HTTP-Headern</span><span class="sxs-lookup"><span data-stu-id="020d1-311">View HTTP headers</span></span>  

<span data-ttu-id="020d1-312">So zeigen Sie HTTP-Header Daten zu einer Anforderung an:</span><span class="sxs-lookup"><span data-stu-id="020d1-312">To view HTTP header data about a request:</span></span>  

1.  <span data-ttu-id="020d1-313">Wählen Sie die URL der Anforderung unter der Spalte **Name** der Tabelle Anforderungen aus.</span><span class="sxs-lookup"><span data-stu-id="020d1-313">Select the URL of the request, under the **Name** column of the Requests table.</span></span>  
1.  <span data-ttu-id="020d1-314">Wählen Sie die Registerkarte über **Schriften** aus.</span><span class="sxs-lookup"><span data-stu-id="020d1-314">Select the **Headers** tab.</span></span>  

:::image type="complex" source="../media/network-resources-headers.msft.png" alt-text="Die Registerkarte "Überschriften"" lightbox="../media/network-resources-headers.msft.png":::
   <span data-ttu-id="020d1-316">Abbildung 21: Registerkarte "über **Schriften** "</span><span class="sxs-lookup"><span data-stu-id="020d1-316">Figure 21:  The **Headers** tab</span></span>  
:::image-end:::  

#### <span data-ttu-id="020d1-317">Anzeigen der HTTP-Header Quelle</span><span class="sxs-lookup"><span data-stu-id="020d1-317">View HTTP header source</span></span>  

<span data-ttu-id="020d1-318">Standardmäßig werden auf der Registerkarte Kopfzeilennamen in alphabetischer Reihenfolge angezeigt.</span><span class="sxs-lookup"><span data-stu-id="020d1-318">By default, the Headers tab shows header names alphabetically.</span></span>  <span data-ttu-id="020d1-319">So zeigen Sie die HTTP-Headernamen in der Reihenfolge an, in der Sie empfangen wurden:</span><span class="sxs-lookup"><span data-stu-id="020d1-319">To view the HTTP header names in the order they were received:</span></span>  

1.  <span data-ttu-id="020d1-320">Öffnen Sie die Registerkarte über **Schriften** für die Anforderung, die Sie interessiert.</span><span class="sxs-lookup"><span data-stu-id="020d1-320">Open the **Headers** tab for the request that interests you.</span></span>  <span data-ttu-id="020d1-321">Siehe [Anzeigen von HTTP-Kopfzeilen](#view-http-headers).</span><span class="sxs-lookup"><span data-stu-id="020d1-321">See [View HTTP headers](#view-http-headers).</span></span>  
1.  <span data-ttu-id="020d1-322">Wählen Sie **Quelle anzeigen**neben dem Abschnitt **Anforderungs Kopfzeile** oder **Antwort Kopf** aus.</span><span class="sxs-lookup"><span data-stu-id="020d1-322">Select **view source**, next to the **Request Header** or **Response Header** section.</span></span>  

### <span data-ttu-id="020d1-323">Anzeigen von Abfragezeichenfolgenparametern</span><span class="sxs-lookup"><span data-stu-id="020d1-323">View query string parameters</span></span>  

<span data-ttu-id="020d1-324">So zeigen Sie die Abfragezeichenfolgenparameter einer URL in einem Menschen lesbaren Format an:</span><span class="sxs-lookup"><span data-stu-id="020d1-324">To view the query string parameters of a URL in a human-readable format:</span></span>  

1.  <span data-ttu-id="020d1-325">Öffnen Sie die Registerkarte über **Schriften** für die Anforderung, die Sie interessiert.</span><span class="sxs-lookup"><span data-stu-id="020d1-325">Open the **Headers** tab for the request that interests you.</span></span>  <span data-ttu-id="020d1-326">Siehe [Anzeigen von HTTP-Kopfzeilen](#view-http-headers).</span><span class="sxs-lookup"><span data-stu-id="020d1-326">See [View HTTP headers](#view-http-headers).</span></span>  
1.  <span data-ttu-id="020d1-327">Wechseln Sie zum Abschnitt **Abfragezeichenfolgenparameter** .</span><span class="sxs-lookup"><span data-stu-id="020d1-327">Go to the **Query String Parameters** section.</span></span>  

:::image type="complex" source="../media/network-network-resources-headers-query-string-parameters.msft.png" alt-text="Der Abfragezeichenfolgenparameter Abschnitt" lightbox="../media/network-network-resources-headers-query-string-parameters.msft.png":::
   <span data-ttu-id="020d1-329">Abbildung 22: Abschnitt " **Abfragezeichenfolgen-Parameter** "</span><span class="sxs-lookup"><span data-stu-id="020d1-329">Figure 22:  The **Query String Parameters** section</span></span>  
:::image-end:::  

#### <span data-ttu-id="020d1-330">Anzeigen der Parameterquelle für Abfragezeichenfolgen</span><span class="sxs-lookup"><span data-stu-id="020d1-330">View query string parameters source</span></span>  

<span data-ttu-id="020d1-331">So zeigen Sie die Abfragezeichenfolgenparameter Quelle einer Anforderung an:</span><span class="sxs-lookup"><span data-stu-id="020d1-331">To view the query string parameter source of a request:</span></span>  

1.  <span data-ttu-id="020d1-332">Wechseln Sie zum Abschnitt Abfragezeichenfolgenparameter.</span><span class="sxs-lookup"><span data-stu-id="020d1-332">Go to the Query String Parameters section.</span></span>  <span data-ttu-id="020d1-333">Weitere Informationen finden Sie unter [Anzeigen von Abfragezeichenfolgenparametern](#view-query-string-parameters).</span><span class="sxs-lookup"><span data-stu-id="020d1-333">See [View query string parameters](#view-query-string-parameters).</span></span>  
1.  <span data-ttu-id="020d1-334">Wählen Sie **Quelltext anzeigen**aus.</span><span class="sxs-lookup"><span data-stu-id="020d1-334">Select **view source**.</span></span>  

#### <span data-ttu-id="020d1-335">Anzeigen von URL-codierten Abfragezeichenfolgenparametern</span><span class="sxs-lookup"><span data-stu-id="020d1-335">View URL-encoded query string parameters</span></span>  

<span data-ttu-id="020d1-336">So zeigen Sie Abfragezeichenfolgenparameter in einem menschlich lesbaren Format an, jedoch mit erhaltenen Codierungen:</span><span class="sxs-lookup"><span data-stu-id="020d1-336">To view query string parameters in a human-readable format, but with encodings preserved:</span></span>  

1.  <span data-ttu-id="020d1-337">Wechseln Sie zum Abschnitt Abfragezeichenfolgenparameter.</span><span class="sxs-lookup"><span data-stu-id="020d1-337">Go to the Query String Parameters section.</span></span>  <span data-ttu-id="020d1-338">Weitere Informationen finden Sie unter [Anzeigen von Abfragezeichenfolgenparametern](#view-query-string-parameters).</span><span class="sxs-lookup"><span data-stu-id="020d1-338">See [View query string parameters](#view-query-string-parameters).</span></span>  
1.  <span data-ttu-id="020d1-339">Wählen Sie **URL-codiert anzeigen**aus.</span><span class="sxs-lookup"><span data-stu-id="020d1-339">Select **view URL encoded**.</span></span>  

### <span data-ttu-id="020d1-340">Cookies anzeigen</span><span class="sxs-lookup"><span data-stu-id="020d1-340">View cookies</span></span>  

<span data-ttu-id="020d1-341">So zeigen Sie die im HTTP-Header einer Anforderung gesendeten Cookies an:</span><span class="sxs-lookup"><span data-stu-id="020d1-341">To view the cookies sent in the HTTP header of a request:</span></span>  

1.  <span data-ttu-id="020d1-342">Wählen Sie die URL der Anforderung unter der Spalte **Name** der Tabelle Anforderungen aus.</span><span class="sxs-lookup"><span data-stu-id="020d1-342">Select the URL of the request, under the **Name** column of the Requests table.</span></span>  
1.  <span data-ttu-id="020d1-343">Wählen Sie die Registerkarte **Cookies** aus.</span><span class="sxs-lookup"><span data-stu-id="020d1-343">Select the **Cookies** tab.</span></span>  

<!--See [Fields][ManageDataCookiesFields] for a description of each of the columns.  -->

<!--[ManageDataCookiesFields]: manage-data/cookies#fields  -->
<!--TODO: add link when section is available -->

:::image type="complex" source="../media/network-network-resources-cookies.msft.png" alt-text="Die Registerkarte "Cookies"" lightbox="../media/network-network-resources-cookies.msft.png":::
   <span data-ttu-id="020d1-345">Abbildung 23: die Registerkarte "Cookies"</span><span class="sxs-lookup"><span data-stu-id="020d1-345">Figure 23:  The Cookies tab</span></span>  
:::image-end:::  

### <span data-ttu-id="020d1-346">Anzeigen der Zeit Plan Aufteilung einer Anforderung</span><span class="sxs-lookup"><span data-stu-id="020d1-346">View the timing breakdown of a request</span></span>  

<span data-ttu-id="020d1-347">So zeigen Sie die Anzeigedauer einer Anforderung an:</span><span class="sxs-lookup"><span data-stu-id="020d1-347">To view the timing breakdown of a request:</span></span>  

1.  <span data-ttu-id="020d1-348">Wählen Sie die URL der Anforderung unter der Spalte **Name** der Tabelle Anforderungen aus.</span><span class="sxs-lookup"><span data-stu-id="020d1-348">Select the URL of the request, under the **Name** column of the Requests table.</span></span>  
1.  <span data-ttu-id="020d1-349">Wählen Sie die Registerkarte **Anzeige** Dauer aus.</span><span class="sxs-lookup"><span data-stu-id="020d1-349">Select the **Timing** tab.</span></span>  

<span data-ttu-id="020d1-350">Eine schnellere Möglichkeit für den Zugriff auf diese Daten finden Sie unter [Anzeigen einer Zeit Plan Vorschau](#preview-a-timing-breakdown) .</span><span class="sxs-lookup"><span data-stu-id="020d1-350">See [Preview a timing breakdown](#preview-a-timing-breakdown) for a faster way to access this data.</span></span>  

<span data-ttu-id="020d1-351">Weitere Informationen zu den einzelnen Phasen, die auf der Registerkarte "Anzeigedauer" angezeigt werden, finden Sie unter [erläuterte Phasen der zeitlichen Verteilung](#timing-breakdown-phases-explained) .</span><span class="sxs-lookup"><span data-stu-id="020d1-351">See [Timing breakdown phases explained](#timing-breakdown-phases-explained) for more information about each of the phases that you may see in the Timing tab.</span></span>  

:::image type="complex" source="../media/network-network-resources-timing.msft.png" alt-text="Registerkarte "Anzeigedauer"" lightbox="../media/network-network-resources-timing.msft.png":::
   <span data-ttu-id="020d1-353">Abbildung 24: Registerkarte " **Anzeige** Dauer"</span><span class="sxs-lookup"><span data-stu-id="020d1-353">Figure 24:  The **Timing** tab</span></span>  
:::image-end:::  

<span data-ttu-id="020d1-354">Weitere Informationen zu den einzelnen Phasen.</span><span class="sxs-lookup"><span data-stu-id="020d1-354">More information about each of the phases.</span></span>  

<span data-ttu-id="020d1-355">Eine weitere Möglichkeit für den Zugriff auf diese Ansicht finden Sie unter [Aufschlüsselung der Anzeige](#view-the-timing-breakdown-of-a-request) Dauer.</span><span class="sxs-lookup"><span data-stu-id="020d1-355">See [View timing breakdown](#view-the-timing-breakdown-of-a-request) for another way to access this view.</span></span>  

#### <span data-ttu-id="020d1-356">Anzeigen einer Vorschau einer Anzeigedauer</span><span class="sxs-lookup"><span data-stu-id="020d1-356">Preview a timing breakdown</span></span>  

<span data-ttu-id="020d1-357">Wenn Sie eine Vorschau der Anzeigedauer einer Anforderung anzeigen möchten, zeigen Sie in der Spalte **Wasserfall** in der Tabelle Anforderungen auf den Eintrag für die Anforderung.</span><span class="sxs-lookup"><span data-stu-id="020d1-357">To view a preview of the timing breakdown of a request, hover over the entry for the request in the **Waterfall** column of the Requests table.</span></span>  

<span data-ttu-id="020d1-358">Weitere Informationen finden Sie unter [Anzeigen der zeitlichen Aufschlüsselung einer Anforderung](#view-the-timing-breakdown-of-a-request) für eine Möglichkeit, auf diese Daten zuzugreifen, für die kein Hovern erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="020d1-358">See [View the timing breakdown of a request](#view-the-timing-breakdown-of-a-request) for a way to access this data that does not require hovering.</span></span>  

:::image type="complex" source="../media/network-network-resources-waterfall-hover.msft.png" alt-text="> Vorschau der Anzeigedauer einer Anforderung" lightbox="../media/network-network-resources-waterfall-hover.msft.png":::
   <span data-ttu-id="020d1-360">Abbildung 25: Anzeigen einer Vorschau der Anzeigedauer einer Anforderung</span><span class="sxs-lookup"><span data-stu-id="020d1-360">Figure 25:  Previewing the timing breakdown of a request</span></span>  
:::image-end:::  

#### <span data-ttu-id="020d1-361">Erläuterte Phasen Aufgliederungs Phasen</span><span class="sxs-lookup"><span data-stu-id="020d1-361">Timing breakdown phases explained</span></span>  

<span data-ttu-id="020d1-362">Weitere Informationen zu den einzelnen Phasen, die auf der Registerkarte **Anzeige** Dauer angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="020d1-362">More information about each of the phases you may see in the **Timing** tab.</span></span>  

*   <span data-ttu-id="020d1-363">**Warteschlange**.</span><span class="sxs-lookup"><span data-stu-id="020d1-363">**Queueing**.</span></span>  <span data-ttu-id="020d1-364">Der Browser Warteschlangenanforderungen, wenn:</span><span class="sxs-lookup"><span data-stu-id="020d1-364">The browser queues requests when:</span></span>  
    *   <span data-ttu-id="020d1-365">Es gibt Anforderungen mit höherer Priorität.</span><span class="sxs-lookup"><span data-stu-id="020d1-365">There are higher priority requests.</span></span>  
    *   <span data-ttu-id="020d1-366">Für diesen Ursprung sind bereits sechs TCP-Verbindungen geöffnet, was die Grenze ist.</span><span class="sxs-lookup"><span data-stu-id="020d1-366">There are already six TCP connections open for this origin, which is the limit.</span></span>  <span data-ttu-id="020d1-367">Gilt nur für HTTP/1.0 und HTTP/1.1.</span><span class="sxs-lookup"><span data-stu-id="020d1-367">Applies to HTTP/1.0 and HTTP/1.1 only.</span></span>  
    *   <span data-ttu-id="020d1-368">Der Browser reserviert kurzzeitig Speicherplatz im Datenträgercache.</span><span class="sxs-lookup"><span data-stu-id="020d1-368">The browser is briefly allocating space in the disk cache.</span></span>  
*   <span data-ttu-id="020d1-369">Im **Stall**.</span><span class="sxs-lookup"><span data-stu-id="020d1-369">**Stalled**.</span></span>  <span data-ttu-id="020d1-370">Die Anforderung konnte aus einem der in der **Warteschlange**beschriebenen Gründe blockiert werden.</span><span class="sxs-lookup"><span data-stu-id="020d1-370">The request could be stalled for any of the reasons described in **Queueing**.</span></span>  
*   <span data-ttu-id="020d1-371">**DNS-Lookup**.</span><span class="sxs-lookup"><span data-stu-id="020d1-371">**DNS Lookup**.</span></span>  <span data-ttu-id="020d1-372">Der Browser löst die IP-Adresse für die Anforderung auf.</span><span class="sxs-lookup"><span data-stu-id="020d1-372">The browser is resolving the IP address for the request.</span></span>  
*   <span data-ttu-id="020d1-373">**Anfängliche Verbindung**.</span><span class="sxs-lookup"><span data-stu-id="020d1-373">**Initial connection**.</span></span>  <span data-ttu-id="020d1-374">Der Browser stellt eine Verbindung her, einschließlich TCP-Handshakes, TCP-Wiederholungen und Aushandeln eines SSL.</span><span class="sxs-lookup"><span data-stu-id="020d1-374">The browser is establishing a connection including TCP handshakes, TCP retries, and negotiating an SSL.</span></span>
*   <span data-ttu-id="020d1-375">**Proxy Verhandlung**.</span><span class="sxs-lookup"><span data-stu-id="020d1-375">**Proxy negotiation**.</span></span>  <span data-ttu-id="020d1-376">Der Browser verhandelt die Anforderung mit einem [Proxy Server][WikiProxyServer].</span><span class="sxs-lookup"><span data-stu-id="020d1-376">The browser is negotiating the request with a [proxy server][WikiProxyServer].</span></span>  
*   <span data-ttu-id="020d1-377">**Anfrage gesendet**.</span><span class="sxs-lookup"><span data-stu-id="020d1-377">**Request sent**.</span></span>  <span data-ttu-id="020d1-378">Die Anfrage wird gesendet.</span><span class="sxs-lookup"><span data-stu-id="020d1-378">The request is being sent.</span></span>  
*   <span data-ttu-id="020d1-379">**ServiceWorker-Vorbereitung**.</span><span class="sxs-lookup"><span data-stu-id="020d1-379">**ServiceWorker Preparation**.</span></span>  <span data-ttu-id="020d1-380">Der Browser startet den Dienstmitarbeiter.</span><span class="sxs-lookup"><span data-stu-id="020d1-380">The browser is starting up the service worker.</span></span>  
*   <span data-ttu-id="020d1-381">**Anforderung an ServiceWorker**.</span><span class="sxs-lookup"><span data-stu-id="020d1-381">**Request to ServiceWorker**.</span></span>  <span data-ttu-id="020d1-382">Die Anforderung wird an den Dienstmitarbeiter gesendet.</span><span class="sxs-lookup"><span data-stu-id="020d1-382">The request is being sent to the service worker.</span></span>  
*   <span data-ttu-id="020d1-383">**Waiting \ (TTFB \)**.</span><span class="sxs-lookup"><span data-stu-id="020d1-383">**Waiting \(TTFB\)**.</span></span>  <span data-ttu-id="020d1-384">Der Browser wartet auf das erste Byte einer Antwort.</span><span class="sxs-lookup"><span data-stu-id="020d1-384">The browser is waiting for the first byte of a response.</span></span>  <span data-ttu-id="020d1-385">TTFB steht für Time to First Byte.</span><span class="sxs-lookup"><span data-stu-id="020d1-385">TTFB stands for Time To First Byte.</span></span>  <span data-ttu-id="020d1-386">Diese Anzeigedauer umfasst eine Roundtrip-Wartezeit und den Zeitpunkt, zu dem der Server die Antwort vorbereitet hat.</span><span class="sxs-lookup"><span data-stu-id="020d1-386">This timing includes 1 round trip of latency and the time the server took to prepare the response.</span></span>  
*   <span data-ttu-id="020d1-387">**Inhalt herunterladen**.</span><span class="sxs-lookup"><span data-stu-id="020d1-387">**Content Download**.</span></span>  <span data-ttu-id="020d1-388">Der Browser empfängt die Antwort.</span><span class="sxs-lookup"><span data-stu-id="020d1-388">The browser is receiving the response.</span></span>  
*   <span data-ttu-id="020d1-389">**Push wird empfangen**.</span><span class="sxs-lookup"><span data-stu-id="020d1-389">**Receiving Push**.</span></span>  <span data-ttu-id="020d1-390">Der Browser empfängt Daten für diese Antwort über http/2 Server Push.</span><span class="sxs-lookup"><span data-stu-id="020d1-390">The browser is receiving data for this response via HTTP/2 Server Push.</span></span>  
*   <span data-ttu-id="020d1-391">**Lese Push**.</span><span class="sxs-lookup"><span data-stu-id="020d1-391">**Reading Push**.</span></span>  <span data-ttu-id="020d1-392">Der Browser liest die zuvor empfangenen lokalen Daten.</span><span class="sxs-lookup"><span data-stu-id="020d1-392">The browser is reading the local data previously received.</span></span>  

### <span data-ttu-id="020d1-393">Anzeigen von Initiatoren und Abhängigkeiten</span><span class="sxs-lookup"><span data-stu-id="020d1-393">View initiators and dependencies</span></span>  

<span data-ttu-id="020d1-394">Wenn Sie die Initiatoren und Abhängigkeiten einer Anforderung anzeigen möchten, halten Sie `Shift` die Anforderung in der Tabelle Anforderungen gedrückt, und zeigen Sie darauf.</span><span class="sxs-lookup"><span data-stu-id="020d1-394">To view the initiators and dependencies of a request, hold `Shift`and hover over the request in the Requests table.</span></span>  <span data-ttu-id="020d1-395">DevTools Farben: Initiatoren werden in grün angezeigt, und Abhängigkeiten werden in rot angezeigt.</span><span class="sxs-lookup"><span data-stu-id="020d1-395">DevTools colors: initiators are shown in green and dependencies are shown in red.</span></span>  

:::image type="complex" source="../media/network-network-resources-initiators-dependencies.msft.png" alt-text="Anzeigen der Initiatoren und Abhängigkeiten einer Anforderung" lightbox="../media/network-network-resources-initiators-dependencies.msft.png":::
   <span data-ttu-id="020d1-397">Abbildung 26: Anzeigen der Initiatoren und Abhängigkeiten einer Anforderung</span><span class="sxs-lookup"><span data-stu-id="020d1-397">Figure 26:  Viewing the initiators and dependencies of a request</span></span>  
:::image-end:::  

<span data-ttu-id="020d1-398">Wenn die Anforderungstabelle chronologisch geordnet ist, ist die erste grüne Anforderung oberhalb des Cursors der Initiator der Abhängigkeit.</span><span class="sxs-lookup"><span data-stu-id="020d1-398">When the Requests table is ordered chronologically, the first green request above the one you are hovering is the initiator of the dependency.</span></span>  <span data-ttu-id="020d1-399">Wenn darüber eine weitere grüne Anforderung angezeigt wird, ist diese höhere Anforderung der Initiator des Initiators.</span><span class="sxs-lookup"><span data-stu-id="020d1-399">If another green request appears above that, that higher request is the initiator of the initiator.</span></span>  <span data-ttu-id="020d1-400">Und so weiter.</span><span class="sxs-lookup"><span data-stu-id="020d1-400">And so on.</span></span>  

### <span data-ttu-id="020d1-401">Laden Ereignisse anzeigen</span><span class="sxs-lookup"><span data-stu-id="020d1-401">View load events</span></span>  

<span data-ttu-id="020d1-402">DevTools zeigt die Anzeigedauer der `DOMContentLoaded` `load` Ereignisse und Ereignisse an mehreren Stellen im Netzwerk Panel an.</span><span class="sxs-lookup"><span data-stu-id="020d1-402">DevTools displays the timing of the `DOMContentLoaded` and `load` events in multiple places on the Network panel.</span></span>  <span data-ttu-id="020d1-403">Das `DOMContentLoaded` Ereignis ist blau gefärbt, und das `load` Ereignis ist rot.</span><span class="sxs-lookup"><span data-stu-id="020d1-403">The `DOMContentLoaded` event is colored blue, and the `load` event is red.</span></span>  

:::image type="complex" source="../media/network-network-requests-load-events.msft.png" alt-text="Die Speicherorte der DOMContentLoaded-und Load-Ereignisse im Netzwerk Panel" lightbox="../media/network-network-requests-load-events.msft.png":::
   <span data-ttu-id="020d1-405">Abbildung 27: die Speicherorte der `DOMContentLoaded` und- `load` Ereignisse im Netzwerk Panel</span><span class="sxs-lookup"><span data-stu-id="020d1-405">Figure 27:  The locations of the `DOMContentLoaded` and `load` events on the Network panel</span></span>  
:::image-end:::  

### <span data-ttu-id="020d1-406">Anzeigen der Gesamtzahl der Anforderungen</span><span class="sxs-lookup"><span data-stu-id="020d1-406">View the total number of requests</span></span>  

<span data-ttu-id="020d1-407">Die Gesamtzahl der Anforderungen wird im Bereich "Zusammenfassung" unten im Netzwerkbereich aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="020d1-407">The total number of requests is listed in the Summary pane, at the bottom of the Network panel.</span></span>  

> [!CAUTION]
> <span data-ttu-id="020d1-408">Diese Nummer verfolgt nur Anforderungen, die seit dem Öffnen von devtools protokolliert wurden.</span><span class="sxs-lookup"><span data-stu-id="020d1-408">This number only tracks requests that have been logged since DevTools was opened.</span></span>  <span data-ttu-id="020d1-409">Wenn vor dem Öffnen von devtools andere Anforderungen aufgetreten sind, werden diese Anforderungen nicht gezählt.</span><span class="sxs-lookup"><span data-stu-id="020d1-409">If other requests occurred before DevTools was opened, those requests are not counted.</span></span>  

:::image type="complex" source="../media/network-network-total-requests.msft.png" alt-text="Die Gesamtzahl der Anforderungen seit dem Öffnen von devtools" lightbox="../media/network-network-total-requests.msft.png":::
   <span data-ttu-id="020d1-411">Abbildung 28: die Gesamtzahl der Anforderungen seit dem Öffnen von devtools</span><span class="sxs-lookup"><span data-stu-id="020d1-411">Figure 28:  The total number of requests since DevTools was opened</span></span>  
:::image-end:::  

### <span data-ttu-id="020d1-412">Anzeigen der Gesamtgröße des Downloads</span><span class="sxs-lookup"><span data-stu-id="020d1-412">View the total download size</span></span>  

<span data-ttu-id="020d1-413">Die Gesamtgröße der Downloadanforderungen wird im Bereich "Zusammenfassung" am unteren Rand des Netzwerkbereichs angezeigt.</span><span class="sxs-lookup"><span data-stu-id="020d1-413">The total download size of requests is listed in the Summary pane, at the bottom of the Network panel.</span></span>  

> [!CAUTION]
> <span data-ttu-id="020d1-414">Diese Nummer verfolgt nur Anforderungen, die seit dem Öffnen von devtools protokolliert wurden.</span><span class="sxs-lookup"><span data-stu-id="020d1-414">This number only tracks requests that have been logged since DevTools was opened.</span></span>  <span data-ttu-id="020d1-415">Wenn vor dem Öffnen von devtools andere Anforderungen aufgetreten sind, werden die vorherigen Anforderungen nicht gezählt.</span><span class="sxs-lookup"><span data-stu-id="020d1-415">If other requests occurred before DevTools was opened, the previous requests are not counted.</span></span>  

:::image type="complex" source="../media/network-network-total-download-size.msft.png" alt-text="Die Gesamtgröße der Downloads von Anforderungen" lightbox="../media/network-network-total-download-size.msft.png":::
   <span data-ttu-id="020d1-417">Abbildung 29: die Gesamtgröße der Downloads von Anforderungen</span><span class="sxs-lookup"><span data-stu-id="020d1-417">Figure 29:  The total download size of requests</span></span>  
:::image-end:::  

<span data-ttu-id="020d1-418">Weitere Informationen finden Sie unter [Anzeigen der unkomprimierten Größe einer Ressource](#view-the-uncompressed-size-of-a-resource) , um zu sehen, wie groß die Ressourcen sind, nachdem der Browser die einzelnen Elemente dekomprimiert hat.</span><span class="sxs-lookup"><span data-stu-id="020d1-418">See [View the uncompressed size of a resource](#view-the-uncompressed-size-of-a-resource) to see how large resources are after the browser uncompresses each item.</span></span>  

### <span data-ttu-id="020d1-419">Anzeigen der Stapelüberwachung, die eine Anforderung verursacht hat</span><span class="sxs-lookup"><span data-stu-id="020d1-419">View the stack trace that caused a request</span></span>  

<span data-ttu-id="020d1-420">Nachdem eine JavaScript-Anweisung eine Ressource angefordert hat, zeigen Sie mit der Maus auf die Spalte **Initiator** , um die Stapelüberwachung anzuzeigen, die zur Anforderung führt.</span><span class="sxs-lookup"><span data-stu-id="020d1-420">After a JavaScript statement requests a resource, hover over the **Initiator** column to view the stack trace leading up to the request.</span></span>  

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

:::image type="complex" source="../media/network-network-requests-initiator-stack.msft.png" alt-text="Die Stapelüberwachung, die zu einer Ressourcenanforderung führt" lightbox="../media/network-network-requests-initiator-stack.msft.png":::
   <span data-ttu-id="020d1-422">Abbildung 30: die Stapelüberwachung, die zu einer Ressourcenanforderung führt</span><span class="sxs-lookup"><span data-stu-id="020d1-422">Figure 30:  The stack trace leading up to a resource request</span></span>  
:::image-end:::  

### <span data-ttu-id="020d1-423">Anzeigen der unkomprimierten Größe einer Ressource</span><span class="sxs-lookup"><span data-stu-id="020d1-423">View the uncompressed size of a resource</span></span>  

<span data-ttu-id="020d1-424">Aktivieren Sie das Kontrollkästchen **große Anforderungs Zeilen verwenden** , und schauen Sie sich den niedrigsten Wert der Spalte **Größe** an.</span><span class="sxs-lookup"><span data-stu-id="020d1-424">Select the **Use large request rows** checkbox and then look at the bottom value of the **Size** column.</span></span>  

:::image type="complex" source="../media/network-network-requests-uncompressed-compare.msft.png" alt-text="Beispiel für nicht komprimierte Ressourcen" lightbox="../media/network-network-requests-uncompressed-compare.msft.png":::
   <span data-ttu-id="020d1-426">Abbildung 31: ein Beispiel für nicht komprimierte Ressourcen \ (die komprimierte Größe der `jquery-3.3.1.min.js` Datei, die über das Netzwerk gesendet wurde `29.9 KB` , während die unkomprimierte Größe `84.9 KB` \) war</span><span class="sxs-lookup"><span data-stu-id="020d1-426">Figure 31:  An example of uncompressed resources  \(The compressed size of the `jquery-3.3.1.min.js` file that was sent over the network was `29.9 KB`, whereas the uncompressed size was `84.9 KB`\)</span></span>  
:::image-end:::  

## <span data-ttu-id="020d1-427">Exportieren von Anforderungsdaten</span><span class="sxs-lookup"><span data-stu-id="020d1-427">Export requests data</span></span>  

### <span data-ttu-id="020d1-428">Speichern aller Netzwerkanforderungen in einer har-Datei</span><span class="sxs-lookup"><span data-stu-id="020d1-428">Save all network requests to a HAR file</span></span>  

<span data-ttu-id="020d1-429">Führen Sie die folgenden Schritte aus, um alle Netzwerkanforderungen in einer har-Datei zu speichern.</span><span class="sxs-lookup"><span data-stu-id="020d1-429">To save all network requests to a HAR file, complete the following steps.</span></span>  

1.  <span data-ttu-id="020d1-430">Zeigen Sie auf jede Anforderung in der Tabelle Anforderungen, und öffnen Sie das Kontextmenü \ (mit der rechten Maustaste auf \).</span><span class="sxs-lookup"><span data-stu-id="020d1-430">Hover on any request in the Requests table and open the contextual menu \(right-click\).</span></span>  
1.  <span data-ttu-id="020d1-431">Wählen Sie **als har mit Inhalt speichern**aus.</span><span class="sxs-lookup"><span data-stu-id="020d1-431">Select **Save as HAR with Content**.</span></span>  <span data-ttu-id="020d1-432">DevTools speichert alle Anforderungen, die seit dem Öffnen von devtools in der har-Datei aufgetreten sind.</span><span class="sxs-lookup"><span data-stu-id="020d1-432">DevTools saves all requests that have occurred since you opened DevTools to the HAR file.</span></span>  <span data-ttu-id="020d1-433">Es gibt keine Möglichkeit, Anforderungen zu filtern oder nur eine einzige Anforderung zu speichern.</span><span class="sxs-lookup"><span data-stu-id="020d1-433">There is no way to filter requests, or to save just a single request.</span></span>  

<span data-ttu-id="020d1-434">Nachdem Sie eine har-Datei gespeichert haben, können Sie Sie für die Analyse wieder in devtools importieren.</span><span class="sxs-lookup"><span data-stu-id="020d1-434">Once you save a HAR file, you may import it back into DevTools for analysis.</span></span>  <span data-ttu-id="020d1-435">Ziehen Sie die har-Datei einfach per Drag & Drop in die Tabelle "Anforderungen".</span><span class="sxs-lookup"><span data-stu-id="020d1-435">Just drag-and-drop the HAR file into the Requests table.</span></span>  
<!--See also [HAR Analyzer][HARAnalyzer].  -->  

<!--[HARAnalyzer]: https://toolbox.alphabetapps.com/apps/har_analyzer  -->  
<!--Todo: add section link when content is available  -->  

:::image type="complex" source="../media/network-network-requests-save-har-content.msft.png" alt-text="Auswählen von "als har mit Inhalt speichern"" lightbox="../media/network-network-requests-save-har-content.msft.png":::
   <span data-ttu-id="020d1-437">Abbildung 32: auswählen **von "als har mit Inhalt speichern** "</span><span class="sxs-lookup"><span data-stu-id="020d1-437">Figure 32:  Selecting **Save as HAR with Content**</span></span>  
:::image-end:::  

### <span data-ttu-id="020d1-438">Kopieren einer oder mehrerer Anforderungen in die Zwischenablage</span><span class="sxs-lookup"><span data-stu-id="020d1-438">Copy one or more requests to the clipboard</span></span>  

<span data-ttu-id="020d1-439">Zeigen Sie unter der Spalte **Name** der Tabelle Anforderungen auf eine Anforderung, öffnen Sie das Kontextmenü \ (Klicken Sie mit der rechten Maustaste auf \), zeigen Sie auf **Kopieren**, und wählen Sie eine der folgenden Optionen aus.</span><span class="sxs-lookup"><span data-stu-id="020d1-439">Under the **Name** column of the Requests table, hover on a request, open the contextual menu \(right-click\), hover over **Copy**, and select one of the following options.</span></span>  

*   <span data-ttu-id="020d1-440">**Link Adresse kopieren**</span><span class="sxs-lookup"><span data-stu-id="020d1-440">**Copy Link Address**.</span></span>  <span data-ttu-id="020d1-441">Kopieren Sie die URL der Anforderung in die Zwischenablage.</span><span class="sxs-lookup"><span data-stu-id="020d1-441">Copy the URL of the request to the clipboard.</span></span>  
*   <span data-ttu-id="020d1-442">**Antwort kopieren**</span><span class="sxs-lookup"><span data-stu-id="020d1-442">**Copy Response**.</span></span>  <span data-ttu-id="020d1-443">Kopieren Sie den Antworttext in die Zwischenablage.</span><span class="sxs-lookup"><span data-stu-id="020d1-443">Copy the response body to the clipboard.</span></span>  
*   <span data-ttu-id="020d1-444">**Als FETCH kopieren**</span><span class="sxs-lookup"><span data-stu-id="020d1-444">**Copy as Fetch**.</span></span>  
*   <span data-ttu-id="020d1-445">**Als curl kopieren**</span><span class="sxs-lookup"><span data-stu-id="020d1-445">**Copy as cURL**.</span></span>  <span data-ttu-id="020d1-446">Kopieren Sie die Anforderung als curl-Befehl.</span><span class="sxs-lookup"><span data-stu-id="020d1-446">Copy the request as a cURL command.</span></span>  
*   <span data-ttu-id="020d1-447">**Kopieren Sie alle als FETCH**.</span><span class="sxs-lookup"><span data-stu-id="020d1-447">**Copy All as Fetch**.</span></span>  
*   <span data-ttu-id="020d1-448">**Kopieren Sie alle als curl**.</span><span class="sxs-lookup"><span data-stu-id="020d1-448">**Copy All as cURL**.</span></span>  <span data-ttu-id="020d1-449">Kopieren Sie alle Anforderungen als eine Kette von curl-Befehlen.</span><span class="sxs-lookup"><span data-stu-id="020d1-449">Copy all requests as a chain of cURL commands.</span></span>  
*   <span data-ttu-id="020d1-450">**Kopieren Sie alle als har**.</span><span class="sxs-lookup"><span data-stu-id="020d1-450">**Copy All as HAR**.</span></span>  <span data-ttu-id="020d1-451">Kopieren Sie alle Anforderungen als har-Daten.</span><span class="sxs-lookup"><span data-stu-id="020d1-451">Copy all requests as HAR data.</span></span>  

:::image type="complex" source="../media/network-network-requests-copy-response.msft.png" alt-text="Auswählen von "Antwort kopieren"" lightbox="../media/network-network-requests-copy-response.msft.png":::
   <span data-ttu-id="020d1-453">Abbildung 33: Auswählen von " **Antwort kopieren** "</span><span class="sxs-lookup"><span data-stu-id="020d1-453">Figure 33:  Selecting **Copy Response**</span></span>  
:::image-end:::  

## <span data-ttu-id="020d1-454">Ändern des Layouts des Netzwerk Panels</span><span class="sxs-lookup"><span data-stu-id="020d1-454">Change the layout of the Network panel</span></span>  

<span data-ttu-id="020d1-455">Sie können Abschnitte der Netzwerk Panel-UI erweitern oder reduzieren, um wichtige Informationen zu konzentrieren.</span><span class="sxs-lookup"><span data-stu-id="020d1-455">You may expand or collapse sections of the Network panel UI to focus important information.</span></span>  

### <span data-ttu-id="020d1-456">Ausblenden des Bereichs "Filter"</span><span class="sxs-lookup"><span data-stu-id="020d1-456">Hide the Filters pane</span></span>  

<span data-ttu-id="020d1-457">Standardmäßig zeigt devtools den **Bereich "Filter"** an.</span><span class="sxs-lookup"><span data-stu-id="020d1-457">By default, DevTools shows the **Filters pane**.</span></span>  
<span data-ttu-id="020d1-458">Wählen Sie **Filter** ![ Filter aus ][ImageFilterIcon] , um sie auszublenden.</span><span class="sxs-lookup"><span data-stu-id="020d1-458">Select **Filter** ![Filter][ImageFilterIcon] to hide it.</span></span>  

:::image type="complex" source="../media/network-network-resources-hide-filters-button.msft.png" alt-text="Schaltfläche "Filter ausblenden"" lightbox="../media/network-network-resources-hide-filters-button.msft.png":::
   <span data-ttu-id="020d1-460">Abbildung 34: die Schaltfläche "Filter ausblenden"</span><span class="sxs-lookup"><span data-stu-id="020d1-460">Figure 34:  The Hide Filters button</span></span>  
:::image-end:::  

### <span data-ttu-id="020d1-461">Verwenden von umfangreichen Anforderungs Zeilen</span><span class="sxs-lookup"><span data-stu-id="020d1-461">Use large request rows</span></span>  

<span data-ttu-id="020d1-462">Verwenden Sie große Zeilen, wenn in Ihrer Netzwerk Anforderungstabelle mehr Leerzeichen verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="020d1-462">Use large rows when you want more whitespace in your network requests table.</span></span>  <span data-ttu-id="020d1-463">Einige Spalten liefern auch ein wenig mehr Informationen, wenn Sie große Zeilen verwenden.</span><span class="sxs-lookup"><span data-stu-id="020d1-463">Some columns also provide a little more information when using large rows.</span></span>  <span data-ttu-id="020d1-464">Der untere Wert der Spalte **size** entspricht beispielsweise der unkomprimierten Größe einer Anforderung.</span><span class="sxs-lookup"><span data-stu-id="020d1-464">For example, the bottom value of the **Size** column is the uncompressed size of a request.</span></span>  

:::image type="complex" source="../media/network-network-requests-large-request-rows.msft.png" alt-text="Ein Beispiel für große Anforderungs Zeilen im Bereich "Anforderungen"" lightbox="../media/network-network-requests-large-request-rows.msft.png":::
   <span data-ttu-id="020d1-466">Abbildung 35: ein Beispiel für große Anforderungs Zeilen im Bereich " **Anforderungen** "</span><span class="sxs-lookup"><span data-stu-id="020d1-466">Figure 35:  An example of large request rows in the **Requests** pane</span></span>  
:::image-end:::  

<span data-ttu-id="020d1-467">Aktivieren Sie das Kontrollkästchen **große Anforderungs Zeilen verwenden** , um große Zeilen zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="020d1-467">Select the **Use large request rows** checkbox to enable large rows.</span></span>  

:::image type="complex" source="../media/network-network-requests-use-large-request-rows-on.msft.png" alt-text="Das Kontrollkästchen "große Anforderungs Zeilen verwenden"" lightbox="../media/network-network-requests-use-large-request-rows-on.msft.png":::
   <span data-ttu-id="020d1-469">Abbildung 36: Kontrollkästchen " **große Anforderungs Zeilen verwenden** "</span><span class="sxs-lookup"><span data-stu-id="020d1-469">Figure 36:  The **Use large request rows** checkbox</span></span>  
:::image-end:::  

### <span data-ttu-id="020d1-470">Ausblenden des Bereichs "Übersicht"</span><span class="sxs-lookup"><span data-stu-id="020d1-470">Hide the Overview pane</span></span>  

<span data-ttu-id="020d1-471">Standardmäßig zeigt devtools den **Bereich "Übersicht"** an.</span><span class="sxs-lookup"><span data-stu-id="020d1-471">By default, DevTools shows the **Overview pane**.</span></span>  <span data-ttu-id="020d1-472">Deaktivieren Sie das Kontrollkästchen " **Übersicht anzeigen** ", um es auszublenden.</span><span class="sxs-lookup"><span data-stu-id="020d1-472">Deselect the **Show Overview** checkbox to hide it.</span></span>  

:::image type="complex" source="../media/network-network-requests-show-overview-off.msft.png" alt-text="Kontrollkästchen ' Übersicht anzeigen '" lightbox="../media/network-network-requests-show-overview-off.msft.png":::
   <span data-ttu-id="020d1-474">Abbildung 37: Kontrollkästchen ' **Übersicht anzeigen** '</span><span class="sxs-lookup"><span data-stu-id="020d1-474">Figure 37:  The **Show Overview** checkbox</span></span>  
:::image-end:::  

<!-- image links -->  

[ImageCaptureScreenshotsIcon]: ../media/capture-screenshots-icon.msft.png  
[ImageClearIcon]: ../media/clear-requests-icon.msft.png  
[ImageFilterIcon]: ../media/filter-icon.msft.png  
[ImageHideIcon]: ../media/hide-overview-icon.msft.png  
[ImageLargeResourceRowsIcon]: ../media/large-resource-rows-button-icon.msft.png  
[ImageRecordOnIcon]: ../media/record-on-icon.msft.png  

<!-- links -->  

[DevtoolsProgressiveWebApps]: /microsoft-edge/devtools-guide-chromium/network/progressive-web-apps "Debuggen von progressiven Web-Apps"  

<!--[NetworkConditions]: /microsoft-edge/devtools-guide-chromium/network/network-conditions "Optimize Performance Under Varying Network Conditions"  -->  

[MDNHTTPDataURIs]: https://developer.mozilla.org/docs/Web/HTTP/Basics_of_HTTP/Data_URIs "Daten-URLs | MDN"  

[WikiProxyServer]: https://en.wikipedia.org/wiki/Proxy_server "Proxy Server – Wikipedia"  

> [!NOTE]
> <span data-ttu-id="020d1-478">Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="020d1-478">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="020d1-479">Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/network/reference) und wird von [Kayce Basken][KayceBasques] (Technical Writer, Chrome devtools \ & Lighthouse \) erstellt.</span><span class="sxs-lookup"><span data-stu-id="020d1-479">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/network/reference) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
<span data-ttu-id="020d1-481">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="020d1-481">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
