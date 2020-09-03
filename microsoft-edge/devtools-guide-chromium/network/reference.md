---
description: Eine umfassende Referenz zu den Features des Microsoft Edge devtools-Netzwerk Panels.
title: Netzwerkanalyse Referenz
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: 38570e6d196314aa6315a34f0b8b1b0b0d740c91
ms.sourcegitcommit: 63e6d34ff483f3b419a0e271a3513874e6ce6c79
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/02/2020
ms.locfileid: "10993618"
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

# <span data-ttu-id="e3bae-104">Netzwerkanalyse Referenz</span><span class="sxs-lookup"><span data-stu-id="e3bae-104">Network Analysis Reference</span></span>  

<span data-ttu-id="e3bae-105">Entdecken Sie neue Möglichkeiten zur Analyse, wie Ihre Seite in dieser umfassenden Referenz der Microsoft Edge devtools-Netzwerkanalyse Features geladen werden kann.</span><span class="sxs-lookup"><span data-stu-id="e3bae-105">Discover new ways to analyze how your page loads in this comprehensive reference of Microsoft Edge DevTools network analysis features.</span></span>  

<!--
> [!NOTE]
> This reference is based on Microsoft Edge 58.  If you use another version of Microsoft Edge, the UI, and features of DevTools may be different.  Check `edge://help` to see what version of Microsoft Edge you are running.  
-->

## <span data-ttu-id="e3bae-106">Aufzeichnen von Netzwerkanforderungen</span><span class="sxs-lookup"><span data-stu-id="e3bae-106">Record network requests</span></span>  

<span data-ttu-id="e3bae-107">Standardmäßig zeichnet devtools alle Netzwerkanforderungen im Netzwerk Panel auf, solange devtools geöffnet ist.</span><span class="sxs-lookup"><span data-stu-id="e3bae-107">By default, DevTools records all network requests in the Network panel, so long as DevTools is open.</span></span>  

:::image type="complex" source="../media/network-network-panel.msft.png" alt-text="Netzwerk Panel" lightbox="../media/network-network-panel.msft.png":::
   <span data-ttu-id="e3bae-109">Abbildung 1: **Netzwerk** Panel</span><span class="sxs-lookup"><span data-stu-id="e3bae-109">Figure 1:  The **Network** panel</span></span>  
:::image-end:::  

### <span data-ttu-id="e3bae-110">Beenden der Aufzeichnung von Netzwerkanforderungen</span><span class="sxs-lookup"><span data-stu-id="e3bae-110">Stop recording network requests</span></span>  

<span data-ttu-id="e3bae-111">Führen Sie die folgenden Schritte aus, um die Aufzeichnung von Anforderungen zu beenden.</span><span class="sxs-lookup"><span data-stu-id="e3bae-111">To stop recording requests, complete the following steps.</span></span>  

1.  <span data-ttu-id="e3bae-112">Wählen **Stop recording network log** Sie ![ ][ImageRecordOnIcon] auf der Registerkarte **Netzwerk** die Option Aufzeichnung des Netzwerkprotokolls beenden Aufzeichnung beenden aus.</span><span class="sxs-lookup"><span data-stu-id="e3bae-112">Select **Stop recording network log** ![Stop recording network log][ImageRecordOnIcon] on the **Network** panel.</span></span>  <span data-ttu-id="e3bae-113">Es wird grau, um anzugeben, dass devtools keine Anforderungen mehr aufzeichnet.</span><span class="sxs-lookup"><span data-stu-id="e3bae-113">It turns grey to indicate that DevTools is no longer recording requests.</span></span>  
1.  <span data-ttu-id="e3bae-114">Drücken Sie `Control` + `E` \ (Windows \) oder `Command` + `E` \ (macOS \), während sich der Fokus des **Netzwerk** Panels befindet.</span><span class="sxs-lookup"><span data-stu-id="e3bae-114">Press `Control`+`E` \(Windows\) or `Command`+`E` \(macOS\) while the **Network** panel is in focus.</span></span>  

### <span data-ttu-id="e3bae-115">Löschen von Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e3bae-115">Clear requests</span></span>  

<span data-ttu-id="e3bae-116">Wählen **Sie** ![ ][ImageClearIcon] im Netzwerk Panel löschen aus, um alle Anforderungen aus der Tabelle Anforderungen zu löschen.</span><span class="sxs-lookup"><span data-stu-id="e3bae-116">Select **Clear** ![Clear][ImageClearIcon] on the Network panel to clear all requests from the Requests table.</span></span>  

:::image type="complex" source="../media/network-network-clear-button.msft.png" alt-text="Die Schaltfläche "Löschen"" lightbox="../media/network-network-clear-button.msft.png":::
   <span data-ttu-id="e3bae-118">Abbildung 2: die Schaltfläche " **Löschen** "</span><span class="sxs-lookup"><span data-stu-id="e3bae-118">Figure 2:  The **Clear** button</span></span>  
:::image-end:::  

### <span data-ttu-id="e3bae-119">Speichern von Anforderungen über Seitenlasten hinweg</span><span class="sxs-lookup"><span data-stu-id="e3bae-119">Save requests across page loads</span></span>  

<span data-ttu-id="e3bae-120">Aktivieren Sie das Kontrollkästchen **Protokoll beibehalten** auf der Registerkarte Netzwerk, um Anforderungen zwischen den Seitenlasten zu speichern.</span><span class="sxs-lookup"><span data-stu-id="e3bae-120">To save requests across page loads, check the **Preserve log** checkbox on the Network panel.</span></span>  <span data-ttu-id="e3bae-121">DevTools speichert alle Anforderungen, bis Sie **Protokoll beibehalten**deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="e3bae-121">DevTools saves all requests until you disable **Preserve log**.</span></span>  

:::image type="complex" source="../media/network-network-preserve-log.msft.png" alt-text="Kontrollkästchen "Protokoll beibehalten"" lightbox="../media/network-network-preserve-log.msft.png":::
   <span data-ttu-id="e3bae-123">Abbildung 3: Kontrollkästchen " **Protokoll beibehalten** "</span><span class="sxs-lookup"><span data-stu-id="e3bae-123">Figure 3:  The **Preserve Log** checkbox</span></span>  
:::image-end:::  

### <span data-ttu-id="e3bae-124">Aufzeichnen von Screenshots beim Laden der Seite</span><span class="sxs-lookup"><span data-stu-id="e3bae-124">Capture screenshots during page load</span></span>  

<span data-ttu-id="e3bae-125">Erfassen Sie Screenshots, um zu analysieren, was die Benutzer sehen, während Sie auf Ihre Seite warten, um Sie zu laden.</span><span class="sxs-lookup"><span data-stu-id="e3bae-125">Capture screenshots to analyze what users see as they wait for your page to load.</span></span>  

<span data-ttu-id="e3bae-126">Wenn Sie Screenshots aktivieren möchten, wählen Sie **Netzwerkeinstellungen** und dann auf der Registerkarte **Netzwerk** das Kontrollkästchen **Screenshots aufzeichnen** aus.</span><span class="sxs-lookup"><span data-stu-id="e3bae-126">To enable screenshots, select **Network settings** and select **Capture screenshots** checkbox on the **Network** panel.</span></span>  

<span data-ttu-id="e3bae-127">Aktualisieren Sie die Seite, während sich das **Netzwerk** Panel im Fokus befindet, um Screenshots zu erfassen.</span><span class="sxs-lookup"><span data-stu-id="e3bae-127">Refresh the page while the **Network** panel is in focus to capture screenshots.</span></span>  

<span data-ttu-id="e3bae-128">Nachdem Sie einen Screenshot aufgezeichnet haben, interagieren Sie mit ihm auf die folgende Weise.</span><span class="sxs-lookup"><span data-stu-id="e3bae-128">After capturing a screenshot, you interact with it in the following ways.</span></span>  

*   <span data-ttu-id="e3bae-129">Zeigen Sie mit der Maus auf einen Screenshot, um den Punkt anzuzeigen, an dem dieser Screenshot aufgenommen wurde.</span><span class="sxs-lookup"><span data-stu-id="e3bae-129">Hover over a screenshot to view the point at which that screenshot was captured.</span></span>  <span data-ttu-id="e3bae-130">Im Bereich " **Übersicht** " wird eine gelbe Zeile angezeigt.</span><span class="sxs-lookup"><span data-stu-id="e3bae-130">A yellow line appears on the **Overview** pane.</span></span>  
*   <span data-ttu-id="e3bae-131">Wählen Sie die Miniaturansicht eines Bildschirms aus, um alle Anforderungen zu filtern, die nach dem Erfassen des Screenshots aufgetreten sind.</span><span class="sxs-lookup"><span data-stu-id="e3bae-131">Select the thumbnail of a screen to filter out any requests that occurred after the screenshot was captured.</span></span>  
*   <span data-ttu-id="e3bae-132">Doppelklicken Sie auf eine Miniaturansicht, um Sie zu vergrößern.</span><span class="sxs-lookup"><span data-stu-id="e3bae-132">Double-click a thumbnail to zoom into it.</span></span>  

:::image type="complex" source="../media/network-network-screenshot-hover.msft.png" alt-text="Zeigen auf einen Screenshot" lightbox="../media/network-network-screenshot-hover.msft.png":::
   <span data-ttu-id="e3bae-134">Abbildung 4: Bewegen des Mauszeigers über einen Screenshot</span><span class="sxs-lookup"><span data-stu-id="e3bae-134">Figure 4:  Hovering over a screenshot</span></span>  
:::image-end:::  

<!--  ### Replay XHR request  -->

<!--  To replay an XHR request, hover on the request in the Requests table, open the contextual menu \(right-click\), and select **Replay XHR**.  -->

<!--  
:::image type="complex" source="../media/network-replay-xhr.msft.png" alt-text="Selecting Replay XHR" lightbox="../media/network-replay-xhr.msft.png":::
   Old Figure 5:  Selecting Replay XHR  
:::image-end:::  
-->  

## <span data-ttu-id="e3bae-135">Ändern des Ladeverhaltens</span><span class="sxs-lookup"><span data-stu-id="e3bae-135">Change loading behavior</span></span>  

### <span data-ttu-id="e3bae-136">Emulieren eines erstmaligen Besuchers durch Deaktivieren des Browsercaches</span><span class="sxs-lookup"><span data-stu-id="e3bae-136">Emulate a first-time visitor by disabling the browser cache</span></span>  

<span data-ttu-id="e3bae-137">Aktivieren Sie das Kontrollkästchen **Cache deaktivieren** , um zu emulieren, wie ein Erstbenutzer Ihre Website erlebt.</span><span class="sxs-lookup"><span data-stu-id="e3bae-137">To emulate how a first-time user experiences your site, check the **Disable cache** checkbox.</span></span>  <span data-ttu-id="e3bae-138">DevTools deaktiviert den Browsercache.</span><span class="sxs-lookup"><span data-stu-id="e3bae-138">DevTools disables the browser cache.</span></span>  <span data-ttu-id="e3bae-139">Dadurch wird die Benutzererfahrung des ersten Benutzers genauer emuliert, da Anforderungen im Browsercache bei wiederholten Besuchen bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="e3bae-139">This more accurately emulates a first-time user's experience, because requests are served from the browser cache on repeat visits.</span></span>  

:::image type="complex" source="../media/network-network-disable-cache-checkbox.msft.png" alt-text="Kontrollkästchen "Cache deaktivieren"" lightbox="../media/network-network-disable-cache-checkbox.msft.png":::
   <span data-ttu-id="e3bae-141">Abbildung 5: Kontrollkästchen " **Cache deaktivieren** "</span><span class="sxs-lookup"><span data-stu-id="e3bae-141">Figure 5:  The **Disable Cache** checkbox</span></span>  
:::image-end:::  

#### <span data-ttu-id="e3bae-142">Deaktivieren des Browser-Caches aus der Schublade "Netzwerkbedingungen"</span><span class="sxs-lookup"><span data-stu-id="e3bae-142">Disable the browser cache from the Network Conditions drawer</span></span>  

<span data-ttu-id="e3bae-143">Wenn Sie den Cache während der Arbeit in anderen devtools-Panels deaktivieren möchten, verwenden Sie die Schublade Netzwerkbedingungen.</span><span class="sxs-lookup"><span data-stu-id="e3bae-143">If you want to disable the cache while working in other DevTools panels, use the Network Conditions drawer.</span></span>  

1.  <span data-ttu-id="e3bae-144">Öffnen Sie die Schublade **Netzwerkbedingungen** .</span><span class="sxs-lookup"><span data-stu-id="e3bae-144">Open the **Network Conditions** drawer.</span></span>  
1.  <span data-ttu-id="e3bae-145">Aktivieren oder deaktivieren Sie das Kontrollkästchen **Cache deaktivieren** .</span><span class="sxs-lookup"><span data-stu-id="e3bae-145">Check or uncheck the **Disable cache** checkbox.</span></span>  

<!--todo: add network condition section when available -->  

### <span data-ttu-id="e3bae-146">Manuelles Löschen des Browsercaches</span><span class="sxs-lookup"><span data-stu-id="e3bae-146">Manually clear the browser cache</span></span>  

<span data-ttu-id="e3bae-147">Wenn Sie den Browser-Cache jederzeit manuell löschen möchten, öffnen Sie das Kontextmenü \ (Klicken Sie mit der rechten Maustaste auf \) an einer beliebigen Stelle in der Tabelle Anforderungen, und wählen Sie **Browsercache löschen**aus.</span><span class="sxs-lookup"><span data-stu-id="e3bae-147">To manually clear the browser cache at any time, open the contextual menu \(right-click\) anywhere in the Requests table and select **Clear Browser Cache**.</span></span>  

:::image type="complex" source="../media/network-network-clear-browser-cache.msft.png" alt-text="Auswählen des Browser Cache löschen" lightbox="../media/network-network-clear-browser-cache.msft.png":::
   <span data-ttu-id="e3bae-149">Abbildung 6: Auswählen des **Browser Cache löschen**</span><span class="sxs-lookup"><span data-stu-id="e3bae-149">Figure 6:  Selecting **Clear Browser Cache**</span></span>  
:::image-end:::  

### <span data-ttu-id="e3bae-150">Offline emulieren</span><span class="sxs-lookup"><span data-stu-id="e3bae-150">Emulate offline</span></span>  

<span data-ttu-id="e3bae-151">Eine neue Klasse von Web-Apps mit dem Namen " [Progressive Web Apps][DevtoolsProgressiveWebApps]" funktioniert mit Hilfe von **Servicemitarbeitern**offline.</span><span class="sxs-lookup"><span data-stu-id="e3bae-151">A new class of web apps, named [Progressive Web Apps][DevtoolsProgressiveWebApps], functions offline with the help of **service workers**.</span></span>  <span data-ttu-id="e3bae-152">Möglicherweise ist es hilfreich, ein Gerät, das keine Datenverbindung aufweist, schnell zu simulieren, wenn Sie diese Art von App erstellen.</span><span class="sxs-lookup"><span data-stu-id="e3bae-152">You may find it useful to quickly simulate a device that has no data connection when you are building this type of app.</span></span>  

<!--[ServiceWorkers]: /web/fundamentals/getting-started/primers/service-workers  -->

<span data-ttu-id="e3bae-153">Wählen Sie das Dropdownmenü **Online** aus, suchen Sie unter **Voreinstellungen**, und wählen Sie **Offline** aus, um eine vollständig Offlinenetzwerk Umgebung zu simulieren.</span><span class="sxs-lookup"><span data-stu-id="e3bae-153">Select the **Online** dropdown menu, search under **Presets**, and select **Offline** to simulate a completely offline network experience.</span></span>  

:::image type="complex" source="../media/network-network-offline-dropdown.msft.png" alt-text="Das Offline-Dropdownmenü" lightbox="../media/network-network-offline-dropdown.msft.png":::
   <span data-ttu-id="e3bae-155">Abbildung 7: **Offline** -Dropdownmenü</span><span class="sxs-lookup"><span data-stu-id="e3bae-155">Figure 7:  The **Offline** dropdown menu</span></span>  
:::image-end:::  

### <span data-ttu-id="e3bae-156">Emulieren langsamer Netzwerkverbindungen</span><span class="sxs-lookup"><span data-stu-id="e3bae-156">Emulate slow network connections</span></span>  

<span data-ttu-id="e3bae-157">Emulieren Sie langsames 3G, fast 3G und andere Verbindungsgeschwindigkeiten über das **Online-Dropdown-** Menü.</span><span class="sxs-lookup"><span data-stu-id="e3bae-157">Emulate Slow 3G, Fast 3G, and other connection speeds from the **Online** dropdown menu.</span></span>  

:::image type="complex" source="../media/network-network-throttling-menu.msft.png" alt-text="Dropdownmenü "Drosselung"" lightbox="../media/network-network-throttling-menu.msft.png":::
   <span data-ttu-id="e3bae-159">Abbildung 8: das Dropdownmenü " **Drosselung** "</span><span class="sxs-lookup"><span data-stu-id="e3bae-159">Figure 8:  The **Throttling** dropdown menu</span></span>  
:::image-end:::  

<span data-ttu-id="e3bae-160">Sie können aus einer Vielzahl von Voreinstellungen auswählen, wie etwa langsames 3G oder fast 3G.</span><span class="sxs-lookup"><span data-stu-id="e3bae-160">You may select from a variety of presets, such as Slow 3G or Fast 3G.</span></span>  <span data-ttu-id="e3bae-161">Sie können auch eigene benutzerdefinierte Voreinstellungen hinzufügen, indem Sie das Menü Drosselung öffnen und **benutzerdefiniertes**  >  **Add**auswählen.</span><span class="sxs-lookup"><span data-stu-id="e3bae-161">You may also add your own custom presets by opening the Throttling menu and selecting **Custom** > **Add**.</span></span>  

<span data-ttu-id="e3bae-162">DevTools zeigt ein Warnungssymbol neben der Registerkarte " **Netzwerk** " an, um Sie daran zu erinnern, dass die Drosselung aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="e3bae-162">DevTools displays a warning icon next to the **Network** tab to remind you that throttling is enabled.</span></span>  

#### <span data-ttu-id="e3bae-163">Emulieren von langsamen Netzwerkverbindungen über die Netzwerkbedingungen Schublade</span><span class="sxs-lookup"><span data-stu-id="e3bae-163">Emulate slow network connections from the Network Conditions drawer</span></span>  

<span data-ttu-id="e3bae-164">Wenn Sie die Netzwerkverbindung während der Arbeit in anderen devtools-Panels Drosseln möchten, verwenden Sie den Netzwerkbedingungen-Einzug.</span><span class="sxs-lookup"><span data-stu-id="e3bae-164">If you want to throttle the network connection while working in other DevTools panels, use the Network Conditions drawer.</span></span>  

1.  <span data-ttu-id="e3bae-165">Öffnen Sie die Schublade **Netzwerkbedingungen** .</span><span class="sxs-lookup"><span data-stu-id="e3bae-165">Open the **Network Conditions** drawer.</span></span>  
1.  <span data-ttu-id="e3bae-166">Wählen Sie die gewünschte Verbindungsgeschwindigkeit im Menü " **Drosselung** " aus.</span><span class="sxs-lookup"><span data-stu-id="e3bae-166">Select your desired connection speed from the **Throttling** menu.</span></span>  

<!--todo: add network condition section when available -->  

### <span data-ttu-id="e3bae-167">Manuelles Löschen von Browser-Cookies</span><span class="sxs-lookup"><span data-stu-id="e3bae-167">Manually clear browser cookies</span></span>  

<span data-ttu-id="e3bae-168">Wenn Sie Browser-Cookies jederzeit manuell löschen möchten, öffnen Sie das Kontextmenü \ (Klicken Sie mit der rechten Maustaste auf \) an einer beliebigen Stelle in der Tabelle Anforderungen, und wählen Sie **Browser-Cookies löschen**aus.</span><span class="sxs-lookup"><span data-stu-id="e3bae-168">To manually clear browser cookies at any time, open the contextual menu \(right-click\) anywhere in the Requests table and select **Clear Browser Cookies**.</span></span>  

:::image type="complex" source="../media/network-network-clear-browser-cookies.msft.png" alt-text="Auswählen von Browser-Cookies löschen" lightbox="../media/network-network-clear-browser-cookies.msft.png":::
   <span data-ttu-id="e3bae-170">Abbildung 9: Auswählen von **Browser-Cookies löschen**</span><span class="sxs-lookup"><span data-stu-id="e3bae-170">Figure 9:  Selecting **Clear Browser Cookies**</span></span>  
:::image-end:::  

### <span data-ttu-id="e3bae-171">Überschreiben des Benutzer-Agents</span><span class="sxs-lookup"><span data-stu-id="e3bae-171">Override the user agent</span></span>  

<span data-ttu-id="e3bae-172">So überschreiben Sie den Benutzer-Agent manuell:</span><span class="sxs-lookup"><span data-stu-id="e3bae-172">To manually override the user agent:</span></span>  

1.  <span data-ttu-id="e3bae-173">Öffnen Sie die Schublade **Netzwerkbedingungen** .</span><span class="sxs-lookup"><span data-stu-id="e3bae-173">Open the **Network Conditions** drawer.</span></span>  
1.  <span data-ttu-id="e3bae-174">Deaktivieren **Sie SELECT automatisch**.</span><span class="sxs-lookup"><span data-stu-id="e3bae-174">Uncheck **Select automatically**.</span></span>  
1.  <span data-ttu-id="e3bae-175">Wählen Sie eine Option für den Benutzer-Agent aus dem Menü aus, oder geben Sie eine benutzerdefinierte Option in das Textfeld ein.</span><span class="sxs-lookup"><span data-stu-id="e3bae-175">Choose a user agent option from the menu, or enter a custom one in the text box.</span></span>  

<!--todo: add network condition section when available -->  

## <span data-ttu-id="e3bae-176">Filter Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e3bae-176">Filter requests</span></span>  

### <span data-ttu-id="e3bae-177">Filtern von Anforderungen nach Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e3bae-177">Filter requests by properties</span></span>  

<span data-ttu-id="e3bae-178">Verwenden Sie das Textfeld **Filtern** , um Anforderungen nach Eigenschaften wie der Domäne oder der Größe der Anforderung zu filtern.</span><span class="sxs-lookup"><span data-stu-id="e3bae-178">Use the **Filter** text box to filter requests by properties, such as the domain or size of the request.</span></span>  

<span data-ttu-id="e3bae-179">Wenn das Textfeld nicht angezeigt wird, ist der Bereich Filter wahrscheinlich ausgeblendet.</span><span class="sxs-lookup"><span data-stu-id="e3bae-179">If you do not see the text box, the Filters pane is probably hidden.</span></span>  
<span data-ttu-id="e3bae-180">Weitere Informationen finden Sie unter [Ausblenden des Filters-Bereichs](#hide-the-filters-pane).</span><span class="sxs-lookup"><span data-stu-id="e3bae-180">See [Hide the Filters pane](#hide-the-filters-pane).</span></span>  

:::image type="complex" source="../media/network-network-filters-textbox.msft.png" alt-text="Das Textfeld "Filter"" lightbox="../media/network-network-filters-textbox.msft.png":::
   <span data-ttu-id="e3bae-182">Abbildung 10: das Textfeld " **Filter** "</span><span class="sxs-lookup"><span data-stu-id="e3bae-182">Figure 10:  The **Filter** text box</span></span>  
:::image-end:::  

<span data-ttu-id="e3bae-183">Sie können mehrere Eigenschaften gleichzeitig verwenden, indem Sie jede Eigenschaft mit einem Leerzeichen voneinander trennen.</span><span class="sxs-lookup"><span data-stu-id="e3bae-183">You may use multiple properties simultaneously by separating each property with a space.</span></span>  <span data-ttu-id="e3bae-184">Zeigt beispielsweise `mime-type:image/png larger-than:1K` alle PNGs an, die größer als ein Kilobyte sind.</span><span class="sxs-lookup"><span data-stu-id="e3bae-184">For example, `mime-type:image/png larger-than:1K` displays all PNGs that are larger than one kilobyte.</span></span>  <span data-ttu-id="e3bae-185">Diese Filter mit mehreren Eigenschaften sind äquivalent zu `AND` Vorgängen.</span><span class="sxs-lookup"><span data-stu-id="e3bae-185">These multi-property filters are equivalent to `AND` operations.</span></span>  `OR` <span data-ttu-id="e3bae-186">Vorgänge werden zurzeit nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e3bae-186">operations are currently not supported.</span></span>  

<span data-ttu-id="e3bae-187">Die vollständige Liste der unterstützten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="e3bae-187">The complete list of supported properties.</span></span>  

| <span data-ttu-id="e3bae-188">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="e3bae-188">Property</span></span> | <span data-ttu-id="e3bae-189">Details</span><span class="sxs-lookup"><span data-stu-id="e3bae-189">Details</span></span> |  
|:--- | :--- |  
| `domain` | <span data-ttu-id="e3bae-190">Zeigt nur Ressourcen aus der angegebenen Domäne an.</span><span class="sxs-lookup"><span data-stu-id="e3bae-190">Only display resources from the specified domain.</span></span>  <span data-ttu-id="e3bae-191">Sie können ein Platzhalterzeichen \ ( `*` \) verwenden, um mehrere Domänen einzubeziehen.</span><span class="sxs-lookup"><span data-stu-id="e3bae-191">You may use a wildcard character \(`*`\) to include multiple domains.</span></span>  <span data-ttu-id="e3bae-192">Zeigt beispielsweise `*.com` Ressourcen aus allen Domänennamen an, die in endet `.com` .</span><span class="sxs-lookup"><span data-stu-id="e3bae-192">For example, `*.com` displays resources from all domain names ending in `.com`.</span></span>  <span data-ttu-id="e3bae-193">DevTools füllt das Dropdownmenü AutoVervollständigen mit allen Domänen auf, die es gefunden hat.</span><span class="sxs-lookup"><span data-stu-id="e3bae-193">DevTools populates the autocomplete dropdown menu with all of the domains it has encountered.</span></span> |  
| `has-response-header` | <span data-ttu-id="e3bae-194">Anzeigen der Ressourcen, die den angegebenen HTTP-Antwortheader enthalten</span><span class="sxs-lookup"><span data-stu-id="e3bae-194">Show the resources that contain the specified HTTP response header.</span></span>  <span data-ttu-id="e3bae-195">DevTools füllt die Dropdownliste AutoVervollständigen mit allen Antwortheadern auf, die Sie gefunden hat.</span><span class="sxs-lookup"><span data-stu-id="e3bae-195">DevTools populates the autocomplete dropdown with all of the response headers that it has encountered.</span></span> |  
| `is` | <span data-ttu-id="e3bae-196">Verwendet `is:running` , um `WebSocket` Ressourcen zu finden.</span><span class="sxs-lookup"><span data-stu-id="e3bae-196">Use `is:running` to find `WebSocket` resources.</span></span> |  
| `larger-than` | <span data-ttu-id="e3bae-197">Zeigen Sie Ressourcen an, die größer als die angegebene Größe in Bytes sind.</span><span class="sxs-lookup"><span data-stu-id="e3bae-197">Show resources that are larger than the specified size, in bytes.</span></span>  <span data-ttu-id="e3bae-198">Das Festlegen eines Werts von entspricht dem `1000` Festlegen eines Werts von `1k` .</span><span class="sxs-lookup"><span data-stu-id="e3bae-198">Setting a value of `1000` is equivalent to setting a value of `1k`.</span></span> |  
| `method` | <span data-ttu-id="e3bae-199">Zeigen Sie Ressourcen an, die über einen angegebenen http-Methodentyp abgerufen wurden.</span><span class="sxs-lookup"><span data-stu-id="e3bae-199">Show resources that were retrieved over a specified HTTP method type.</span></span>  <span data-ttu-id="e3bae-200">DevTools füllt die Dropdownliste mit allen HTTP-Methoden auf, die Sie gefunden hat.</span><span class="sxs-lookup"><span data-stu-id="e3bae-200">DevTools populates the dropdown with all of the HTTP methods it has encountered.</span></span> |  
| `mime-type` | <span data-ttu-id="e3bae-201">Anzeigen von Ressourcen eines angegebenen MIME-Typs</span><span class="sxs-lookup"><span data-stu-id="e3bae-201">Show resources of a specified MIME type.</span></span>  <span data-ttu-id="e3bae-202">DevTools füllt die Dropdownliste mit allen MIME-Typen auf, die Sie gefunden hat.</span><span class="sxs-lookup"><span data-stu-id="e3bae-202">DevTools populates the dropdown with all MIME types it has encountered.</span></span> |  
| `mixed-content` | <span data-ttu-id="e3bae-203">Alle gemischten Inhalts Ressourcen anzeigen \ ( `mixed-content:all` \) oder nur diejenigen, die aktuell angezeigt werden \ ( `mixed-content:displayed` \).</span><span class="sxs-lookup"><span data-stu-id="e3bae-203">Show all mixed content resources \(`mixed-content:all`\) or just the ones that are currently displayed \(`mixed-content:displayed`\).</span></span> |  
| `scheme` | <span data-ttu-id="e3bae-204">Zeigt Ressourcen an, die über ungeschützten http \ ( `scheme:http` \) oder geschütztes HTTPS \ ( `scheme:https` \) abgerufen wurden.</span><span class="sxs-lookup"><span data-stu-id="e3bae-204">Show resources retrieved over unprotected HTTP \(`scheme:http`\) or protected HTTPS \(`scheme:https`\).</span></span> |  
| `set-cookie-domain` | <span data-ttu-id="e3bae-205">Zeigen Sie die Ressourcen mit einer `Set-Cookie` Kopfzeile mit einem `Domain` Attribut an, das dem angegebenen Wert entspricht.</span><span class="sxs-lookup"><span data-stu-id="e3bae-205">Show the resources that have a `Set-Cookie` header with a `Domain` attribute that matches the specified value.</span></span>  <span data-ttu-id="e3bae-206">DevTools füllt das AutoVervollständigen mit allen Cookie-Domänen auf, die es gefunden hat.</span><span class="sxs-lookup"><span data-stu-id="e3bae-206">DevTools populates the autocomplete with all of the cookie domains that it has encountered.</span></span> |  
| `set-cookie-name` | <span data-ttu-id="e3bae-207">Zeigen Sie die Ressourcen mit einer `Set-Cookie` Kopfzeile mit einem Namen an, der dem angegebenen Wert entspricht.</span><span class="sxs-lookup"><span data-stu-id="e3bae-207">Show the resources that have a `Set-Cookie` header with a name that matches the specified value.</span></span>  <span data-ttu-id="e3bae-208">DevTools füllt das AutoVervollständigen mit allen Cookie-Namen auf, die es gefunden hat.</span><span class="sxs-lookup"><span data-stu-id="e3bae-208">DevTools populates the autocomplete with all of the cookie names that it has encountered.</span></span> |  
| `set-cookie-value` | <span data-ttu-id="e3bae-209">Zeigen Sie die Ressourcen mit einer `Set-Cookie` Kopfzeile mit einem Wert an, der dem angegebenen Wert entspricht.</span><span class="sxs-lookup"><span data-stu-id="e3bae-209">Show the resources that have a `Set-Cookie` header with a value that matches the specified value.</span></span>  <span data-ttu-id="e3bae-210">DevTools füllt das AutoVervollständigen mit allen Cookie-Werten auf, die es gefunden hat.</span><span class="sxs-lookup"><span data-stu-id="e3bae-210">DevTools populates the autocomplete with all of the cookie values that it has encountered.</span></span> |  
| `status-code` | <span data-ttu-id="e3bae-211">Nur die Ressourcen anzeigen, für die der HTTP-Statuscode mit dem angegebenen Code übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="e3bae-211">Show only the resources for which the HTTP status code matches the specified code.</span></span>  <span data-ttu-id="e3bae-212">DevTools füllt das Dropdownmenü AutoVervollständigen mit allen Statuscodes auf, die es gefunden hat.</span><span class="sxs-lookup"><span data-stu-id="e3bae-212">DevTools populates the autocomplete dropdown menu with all of the status codes it has encountered.</span></span> |  

### <span data-ttu-id="e3bae-213">Filtern von Anforderungen nach Typ</span><span class="sxs-lookup"><span data-stu-id="e3bae-213">Filter requests by type</span></span>  

<span data-ttu-id="e3bae-214">Wenn Sie Anforderungen nach Anforderungsfiltern möchten, wählen Sie die Schaltflächen **XMLHttpRequest**, **js**, **CSS**, **IMG**, **Media**, **Font**, **doc**, **WS** \ (WebSocket \), **Manifest**oder **andere** \ (alle anderen Typen, die hier nicht aufgelistet sind) im Netzwerk Panel aus.</span><span class="sxs-lookup"><span data-stu-id="e3bae-214">To filter requests by request type, select the **XHR**, **JS**, **CSS**, **Img**, **Media**, **Font**, **Doc**, **WS** \(WebSocket\), **Manifest**, or **Other** \(any other type not listed here\) buttons on the Network panel.</span></span>  

<span data-ttu-id="e3bae-215">Wenn diese Schaltflächen nicht angezeigt werden, ist der Bereich Filter wahrscheinlich ausgeblendet.</span><span class="sxs-lookup"><span data-stu-id="e3bae-215">If you do not see these buttons, the Filters pane is probably hidden.</span></span>  
<span data-ttu-id="e3bae-216">Weitere Informationen finden Sie unter [Ausblenden des Filters-Bereichs](#hide-the-filters-pane).</span><span class="sxs-lookup"><span data-stu-id="e3bae-216">See [Hide the Filters pane](#hide-the-filters-pane).</span></span>  

<span data-ttu-id="e3bae-217">Wenn Sie mehrere Typfilter gleichzeitig aktivieren möchten, halten `Control` Sie \ (Windows \) oder `Command` \ (macOS \) gedrückt, und wählen Sie dann aus.</span><span class="sxs-lookup"><span data-stu-id="e3bae-217">To enable multiple type filters simultaneously, hold `Control` \(Windows\) or `Command` \(macOS\) and then select.</span></span>  

:::image type="complex" source="../media/network-network-type-filters.msft.png" alt-text="Verwenden des Typs "Filter" zum Anzeigen von JS-, CSS-und Dokument Ressourcen" lightbox="../media/network-network-type-filters.msft.png":::
   <span data-ttu-id="e3bae-219">Abbildung 11: Verwenden der Typfilter zum Anzeigen von JS-, CSS-und Dokument Ressourcen</span><span class="sxs-lookup"><span data-stu-id="e3bae-219">Figure 11:  Using the Type filters to display JS, CSS, and Document resources</span></span>  
:::image-end:::  

### <span data-ttu-id="e3bae-220">Filtern von Anforderungen nach Zeit</span><span class="sxs-lookup"><span data-stu-id="e3bae-220">Filter requests by time</span></span>  

<span data-ttu-id="e3bae-221">Wählen Sie aus, und ziehen Sie im Übersichtsbereich nach links oder rechts, um nur Anforderungen anzuzeigen, die während dieses Zeitrahmens aktiv waren.</span><span class="sxs-lookup"><span data-stu-id="e3bae-221">Select and drag left or right on the Overview pane to only display requests that were active during that time frame.</span></span>  <span data-ttu-id="e3bae-222">Der Filter ist inklusive.</span><span class="sxs-lookup"><span data-stu-id="e3bae-222">The filter is inclusive.</span></span>  <span data-ttu-id="e3bae-223">Jede Anforderung, die während der hervorgehobenen Zeit aktiv war, wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="e3bae-223">Any request that was active during the highlighted time is shown.</span></span>  

:::image type="complex" source="../media/network-network-overview-filter.msft.png" alt-text="Herausfiltern von Anforderungen, die um 300 m inaktiv waren" lightbox="../media/network-network-overview-filter.msft.png":::
   <span data-ttu-id="e3bae-225">Abbildung 12: Filtern von Anforderungen, die um 300 m inaktiv waren</span><span class="sxs-lookup"><span data-stu-id="e3bae-225">Figure 12:  Filtering out any requests that were inactive around 300ms</span></span>  
:::image-end:::  

### <span data-ttu-id="e3bae-226">Ausblenden von Daten-URLs</span><span class="sxs-lookup"><span data-stu-id="e3bae-226">Hide data URLs</span></span>  

<span data-ttu-id="e3bae-227">[Daten-URLs][MDNHTTPDataURIs] sind kleine Dateien, die in andere Dokumente eingebettet sind.</span><span class="sxs-lookup"><span data-stu-id="e3bae-227">[Data URLs][MDNHTTPDataURIs] are small files embedded into other documents.</span></span>  <span data-ttu-id="e3bae-228">Jede Anforderung, die Sie in der Tabelle Anforderungen sehen, die mit beginnt, `data:` ist eine Daten-URL.</span><span class="sxs-lookup"><span data-stu-id="e3bae-228">Any request that you see in the Requests table that starts with `data:` is a data URL.</span></span>  

<span data-ttu-id="e3bae-229">Aktivieren Sie das Kontrollkästchen **Daten-URLs ausblenden** , um die Anforderungen auszublenden.</span><span class="sxs-lookup"><span data-stu-id="e3bae-229">Check the **Hide data URLs** checkbox to hide the requests.</span></span>  

:::image type="complex" source="../media/network-network-hide-data-urls.msft.png" alt-text="Das Kontrollkästchen "Daten-URLs ausblenden"" lightbox="../media/network-network-hide-data-urls.msft.png":::
   <span data-ttu-id="e3bae-231">Abbildung 13: Kontrollkästchen " **Daten-URLs ausblenden** "</span><span class="sxs-lookup"><span data-stu-id="e3bae-231">Figure 13:  The **Hide Data URLs** checkbox</span></span>  
:::image-end:::  

## <span data-ttu-id="e3bae-232">Sortieren von Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e3bae-232">Sort requests</span></span>  

<span data-ttu-id="e3bae-233">Standardmäßig werden die Anforderungen in der Tabelle Anforderungen nach Initiierungs Zeit sortiert, aber Sie können die Tabelle mit anderen Kriterien sortieren.</span><span class="sxs-lookup"><span data-stu-id="e3bae-233">By default, the requests in the Requests table are sorted by initiation time, but you may sort the table using other criteria.</span></span>  

### <span data-ttu-id="e3bae-234">Nach Spalte sortieren</span><span class="sxs-lookup"><span data-stu-id="e3bae-234">Sort by column</span></span>  

<span data-ttu-id="e3bae-235">Wählen Sie die Kopfzeile einer beliebigen Spalte in den Anforderungen aus, um Anforderungen nach dieser Spalte zu sortieren.</span><span class="sxs-lookup"><span data-stu-id="e3bae-235">Select the header of any column in the Requests to sort requests by that column.</span></span>  

### <span data-ttu-id="e3bae-236">Nach Aktivitätsphase sortieren</span><span class="sxs-lookup"><span data-stu-id="e3bae-236">Sort by activity phase</span></span>  

<span data-ttu-id="e3bae-237">Wenn Sie ändern möchten, wie der Wasserfall Anforderungen sortiert, zeigen Sie auf die Kopfzeile der Tabelle Anforderungen, öffnen Sie das Kontextmenü \ (Klicken Sie mit der rechten Maustaste auf \), zeigen Sie mit der Maus auf **Wasserfall**, und wählen Sie eine der folgenden Optionen aus.</span><span class="sxs-lookup"><span data-stu-id="e3bae-237">To change how the Waterfall sorts requests, hover on the header of the Requests table, open the contextual menu \(right-click\), hover over **Waterfall**, and select one of the following options.</span></span>  

*   <span data-ttu-id="e3bae-238">**Startzeit**.</span><span class="sxs-lookup"><span data-stu-id="e3bae-238">**Start Time**.</span></span>  <span data-ttu-id="e3bae-239">Die erste Anforderung, die initiiert wurde, ist oben.</span><span class="sxs-lookup"><span data-stu-id="e3bae-239">The first request that was initiated is at the top.</span></span>  
*   <span data-ttu-id="e3bae-240">**Antwortzeit**.</span><span class="sxs-lookup"><span data-stu-id="e3bae-240">**Response Time**.</span></span>  <span data-ttu-id="e3bae-241">Die erste Anforderung, die den Download begonnen hat, ist ganz oben.</span><span class="sxs-lookup"><span data-stu-id="e3bae-241">The first request that started downloading is at the top.</span></span>  
*   <span data-ttu-id="e3bae-242">**Endzeit**.</span><span class="sxs-lookup"><span data-stu-id="e3bae-242">**End Time**.</span></span>  <span data-ttu-id="e3bae-243">Die erste abgeschlossene Anforderung ist oben.</span><span class="sxs-lookup"><span data-stu-id="e3bae-243">The first request that finished is at the top.</span></span>  
*   <span data-ttu-id="e3bae-244">**Gesamtdauer**.</span><span class="sxs-lookup"><span data-stu-id="e3bae-244">**Total Duration**.</span></span>  <span data-ttu-id="e3bae-245">Die Anforderung mit der kürzesten Verbindungseinrichtung und Anforderung/Antwort ist oben.</span><span class="sxs-lookup"><span data-stu-id="e3bae-245">The request with the shortest connection setup and request / response is at the top.</span></span>  
*   <span data-ttu-id="e3bae-246">**Latenz**.</span><span class="sxs-lookup"><span data-stu-id="e3bae-246">**Latency**.</span></span>  <span data-ttu-id="e3bae-247">Die Anforderung, die die kürzeste Zeit für eine Antwort gewartet hat, ist oben.</span><span class="sxs-lookup"><span data-stu-id="e3bae-247">The request that waited the shortest time for a response is at the top.</span></span>  

<span data-ttu-id="e3bae-248">Bei diesen Beschreibungen wird davon ausgegangen, dass die jeweilige Option von kürzester bis längster Position bewertet wird.</span><span class="sxs-lookup"><span data-stu-id="e3bae-248">These descriptions assume that each respective option is ranked from shortest to longest.</span></span>  <span data-ttu-id="e3bae-249">Wenn Sie die Kopfzeile der Spalte **Wasserfall** auswählen, wird die Reihenfolge umgekehrt.</span><span class="sxs-lookup"><span data-stu-id="e3bae-249">Selecting the header of the **Waterfall** column reverses the order.</span></span>  

:::image type="complex" source="../media/network-network-waterfall-total-duration.msft.png" alt-text="Sortieren des Wasserfalls nach Gesamtdauer" lightbox="../media/network-network-waterfall-total-duration.msft.png":::
   <span data-ttu-id="e3bae-251">Abbildung 14: Sortieren des Wasserfalls nach Gesamtdauer \ (der leichtere Teil der einzelnen Balken ist die Zeit, die gewartet wird, und der dunklere Teil ist die Zeit, die zum Herunterladen von Bytes verwendet wird \)</span><span class="sxs-lookup"><span data-stu-id="e3bae-251">Figure 14:  Sorting the Waterfall by total duration  \(The lighter portion of each bar is time spent waiting and the darker portion is time spent downloading bytes\)</span></span>  
:::image-end:::  

## <span data-ttu-id="e3bae-252">Analysieren von Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e3bae-252">Analyze requests</span></span>  

<span data-ttu-id="e3bae-253">Solange devtools geöffnet ist, werden alle Anforderungen im Netzwerk Panel protokolliert.</span><span class="sxs-lookup"><span data-stu-id="e3bae-253">So long as DevTools is open, it logs all requests in the Network panel.</span></span>  
<span data-ttu-id="e3bae-254">Verwenden Sie das Netzwerk Panel, um Anforderungen zu analysieren.</span><span class="sxs-lookup"><span data-stu-id="e3bae-254">Use the Network panel to analyze requests.</span></span>  

### <span data-ttu-id="e3bae-255">Anzeigen eines Protokolls der Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e3bae-255">View a log of requests</span></span>  

<span data-ttu-id="e3bae-256">Verwenden Sie die Tabelle "Anforderungen", um ein Protokoll aller Anforderungen anzuzeigen, die während der devtools geöffnet wurden.</span><span class="sxs-lookup"><span data-stu-id="e3bae-256">Use the Requests table to view a log of all requests made while DevTools has been open.</span></span>  <span data-ttu-id="e3bae-257">Wenn Sie über Anforderungen auswählen oder darauf zeigen, werden weitere Informationen zu den einzelnen Elementen eingeblendet.</span><span class="sxs-lookup"><span data-stu-id="e3bae-257">Selecting or hovering over requests reveals more information about each item.</span></span>  

:::image type="complex" source="../media/network-network-requests-table.msft.png" alt-text="Die Tabelle "Anforderungen"" lightbox="../media/network-network-requests-table.msft.png":::
   <span data-ttu-id="e3bae-259">Abbildung 15: die Tabelle "Anforderungen"</span><span class="sxs-lookup"><span data-stu-id="e3bae-259">Figure 15:  The Requests table</span></span>  
:::image-end:::  

<span data-ttu-id="e3bae-260">In der Tabelle Anforderungen werden standardmäßig die folgenden Spalten angezeigt.</span><span class="sxs-lookup"><span data-stu-id="e3bae-260">The Requests table displays the following columns by default.</span></span>  

*   <span data-ttu-id="e3bae-261">**Name**</span><span class="sxs-lookup"><span data-stu-id="e3bae-261">**Name**.</span></span>  <span data-ttu-id="e3bae-262">Der Dateiname von oder ein Bezeichner für die Ressource.</span><span class="sxs-lookup"><span data-stu-id="e3bae-262">The filename of, or an identifier for, the resource.</span></span>  
*   <span data-ttu-id="e3bae-263">**Status**aus.</span><span class="sxs-lookup"><span data-stu-id="e3bae-263">**Status**.</span></span>  <span data-ttu-id="e3bae-264">Der HTTP-Statuscode.</span><span class="sxs-lookup"><span data-stu-id="e3bae-264">The HTTP status code.</span></span>  
*   <span data-ttu-id="e3bae-265">**Typ**.</span><span class="sxs-lookup"><span data-stu-id="e3bae-265">**Type**.</span></span>  <span data-ttu-id="e3bae-266">Der MIME-Typ der angeforderten Ressource.</span><span class="sxs-lookup"><span data-stu-id="e3bae-266">The MIME type of the requested resource.</span></span>  
*   <span data-ttu-id="e3bae-267">**Initiator**.</span><span class="sxs-lookup"><span data-stu-id="e3bae-267">**Initiator**.</span></span>  <span data-ttu-id="e3bae-268">Die folgenden Objekte oder Prozesse initiieren Anforderungen:</span><span class="sxs-lookup"><span data-stu-id="e3bae-268">The following objects or processes initiate requests:</span></span>  
    *   <span data-ttu-id="e3bae-269">**Parser**aus.</span><span class="sxs-lookup"><span data-stu-id="e3bae-269">**Parser**.</span></span>  <span data-ttu-id="e3bae-270">Der HTML-Parser für Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="e3bae-270">The HTML parser for Microsoft Edge.</span></span>  
    *   <span data-ttu-id="e3bae-271">**Umleiten**.</span><span class="sxs-lookup"><span data-stu-id="e3bae-271">**Redirect**.</span></span>  <span data-ttu-id="e3bae-272">Eine HTTP-Umleitung.</span><span class="sxs-lookup"><span data-stu-id="e3bae-272">An HTTP redirect.</span></span>  
    *   <span data-ttu-id="e3bae-273">**Skript**aus.</span><span class="sxs-lookup"><span data-stu-id="e3bae-273">**Script**.</span></span>  <span data-ttu-id="e3bae-274">Eine JavaScript-Funktion.</span><span class="sxs-lookup"><span data-stu-id="e3bae-274">A JavaScript function.</span></span>  
    *   <span data-ttu-id="e3bae-275">**Andere**.</span><span class="sxs-lookup"><span data-stu-id="e3bae-275">**Other**.</span></span>  <span data-ttu-id="e3bae-276">Einige andere Prozesse oder Aktionen, wie das Navigieren zu einer Seite über einen Link oder das Eingeben einer URL in die Adressleiste.</span><span class="sxs-lookup"><span data-stu-id="e3bae-276">Some other process or action, such as navigating to a page via a link or entering a URL in the address bar.</span></span>  
*   <span data-ttu-id="e3bae-277">**Größe**aus.</span><span class="sxs-lookup"><span data-stu-id="e3bae-277">**Size**.</span></span>  <span data-ttu-id="e3bae-278">Die kombinierte Größe der Antwortheader sowie des Antworttexts, wie vom Server bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="e3bae-278">The combined size of the response headers plus the response body, as delivered by the server.</span></span>  
*   <span data-ttu-id="e3bae-279">**Zeit**.</span><span class="sxs-lookup"><span data-stu-id="e3bae-279">**Time**.</span></span>  <span data-ttu-id="e3bae-280">Die Gesamtdauer vom Anfang der Anforderung bis zum Empfang des letzten Bytes in der Antwort.</span><span class="sxs-lookup"><span data-stu-id="e3bae-280">The total duration, from the start of the request to the receipt of the final byte in the response.</span></span>  
*   <span data-ttu-id="e3bae-281">[**Wasserfall**](#view-the-timing-of-requests-in-relation-to-one-another).</span><span class="sxs-lookup"><span data-stu-id="e3bae-281">[**Waterfall**](#view-the-timing-of-requests-in-relation-to-one-another).</span></span>  <span data-ttu-id="e3bae-282">Eine visuelle Gliederung der Aktivität für jede Anforderung.</span><span class="sxs-lookup"><span data-stu-id="e3bae-282">A visual breakdown of the activity for each request.</span></span>  

#### <span data-ttu-id="e3bae-283">Hinzufügen oder Entfernen von Spalten</span><span class="sxs-lookup"><span data-stu-id="e3bae-283">Add or remove columns</span></span>  

<span data-ttu-id="e3bae-284">Zeigen Sie auf die Kopfzeile der Tabelle Anforderungen, öffnen Sie das Kontextmenü \ (Klicken Sie mit der rechten Maustaste auf \), und wählen Sie eine Option aus, um sie auszublenden oder anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="e3bae-284">Hover on the header of the Requests table, open the contextual menu \(right-click\), and select an option to hide or show it.</span></span>  <span data-ttu-id="e3bae-285">Die aktuell angezeigten Optionen verfügen über Kontrollkästchen neben den einzelnen Elementen.</span><span class="sxs-lookup"><span data-stu-id="e3bae-285">Currently displayed options have checkmarks next to each item.</span></span>  

:::image type="complex" source="../media/network-network-requests-add-column.msft.png" alt-text="Hinzufügen einer Spalte zur Tabelle "Anforderungen"" lightbox="../media/network-network-requests-add-column.msft.png":::
   <span data-ttu-id="e3bae-287">Abbildung 16: Hinzufügen einer Spalte zur Tabelle "Anforderungen"</span><span class="sxs-lookup"><span data-stu-id="e3bae-287">Figure 16:  Adding a column to the Requests table</span></span>  
:::image-end:::  

#### <span data-ttu-id="e3bae-288">Hinzufügen benutzerdefinierter Spalten</span><span class="sxs-lookup"><span data-stu-id="e3bae-288">Add custom columns</span></span>  

<span data-ttu-id="e3bae-289">Wenn Sie der Tabelle Anforderungen eine benutzerdefinierte Spalte hinzufügen möchten, zeigen Sie auf die Kopfzeile der Tabelle Anforderungen, öffnen Sie das Kontextmenü \ (Klicken Sie mit der rechten Maustaste auf \), und wählen Sie **Antwortheader**  >  **Verwalten von Kopfzeilen Spalten**aus.</span><span class="sxs-lookup"><span data-stu-id="e3bae-289">To add a custom column to the Requests table, hover on the header of the Requests table, open the contextual menu \(right-click\), and select **Response Headers** > **Manage Header Columns**.</span></span>  

:::image type="complex" source="../media/network-network-requests-add-custom.msft.png" alt-text="Hinzufügen einer benutzerdefinierten Spalte zur Tabelle "Anforderungen"" lightbox="../media/network-network-requests-add-custom.msft.png":::
   <span data-ttu-id="e3bae-291">Abbildung 17: Hinzufügen einer benutzerdefinierten Spalte zur Tabelle "Anforderungen"</span><span class="sxs-lookup"><span data-stu-id="e3bae-291">Figure 17:  Adding a custom column to the Requests table</span></span>  
:::image-end:::  

### <span data-ttu-id="e3bae-292">Anzeigen der Anzeigedauer von Anforderungen im Verhältnis zueinander</span><span class="sxs-lookup"><span data-stu-id="e3bae-292">View the timing of requests in relation to one another</span></span>  

<span data-ttu-id="e3bae-293">Verwenden Sie den Wasserfall, um die Anzeigedauer von Anforderungen im Verhältnis zueinander anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="e3bae-293">Use the Waterfall to view the timing of requests in relation to one another.</span></span>  
<span data-ttu-id="e3bae-294">Standardmäßig wird der Wasserfall nach dem Anfangszeitpunkt der Anforderungen organisiert.</span><span class="sxs-lookup"><span data-stu-id="e3bae-294">By default, the Waterfall is organized by the start time of the requests.</span></span>  
<span data-ttu-id="e3bae-295">Anfragen, die weiter Links sind, wurden früher als die weiter rechts eingegangenen Anforderungen gestartet.</span><span class="sxs-lookup"><span data-stu-id="e3bae-295">So, requests that are farther to the left started earlier than those that are farther to the right.</span></span>  

<span data-ttu-id="e3bae-296">Sehen Sie sich die verschiedenen Arten an, wie Sie den Wasserfall sortieren können, [indem Sie nach Aktivitätsphase sortieren](#sort-by-activity-phase) .</span><span class="sxs-lookup"><span data-stu-id="e3bae-296">See [Sort by activity phase](#sort-by-activity-phase) to see the different ways that you may sort the Waterfall.</span></span>  

:::image type="complex" source="../media/network-network-requests-waterfall.msft.png" alt-text="Spalte "Wasserfall" im Bereich "Anforderungen"" lightbox="../media/network-network-requests-waterfall.msft.png":::
   <span data-ttu-id="e3bae-298">Abbildung 18: Spalte "Wasserfall" im Bereich " **Anforderungen** "</span><span class="sxs-lookup"><span data-stu-id="e3bae-298">Figure 18:  The Waterfall column of the **Requests** pane</span></span>  
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

### <span data-ttu-id="e3bae-299">Anzeigen einer Vorschau eines Antworttexts</span><span class="sxs-lookup"><span data-stu-id="e3bae-299">View a preview of a response body</span></span>  

<span data-ttu-id="e3bae-300">So zeigen Sie eine Vorschau eines Antworttexts an:</span><span class="sxs-lookup"><span data-stu-id="e3bae-300">To view a preview of a response body:</span></span>  

1.  <span data-ttu-id="e3bae-301">Wählen Sie die URL der Anforderung unter der Spalte **Name** der Tabelle Anforderungen aus.</span><span class="sxs-lookup"><span data-stu-id="e3bae-301">Select the URL of the request, under the **Name** column of the Requests table.</span></span>  
1.  <span data-ttu-id="e3bae-302">Wählen Sie die Registerkarte **Vorschau** aus.</span><span class="sxs-lookup"><span data-stu-id="e3bae-302">Select the **Preview** tab.</span></span>  

<span data-ttu-id="e3bae-303">Diese Registerkarte ist hauptsächlich für die Anzeige von Bildern hilfreich.</span><span class="sxs-lookup"><span data-stu-id="e3bae-303">This tab is mostly useful for viewing images.</span></span>  

:::image type="complex" source="../media/network-network-resources-preview.msft.png" alt-text="Registerkarte "Vorschau"" lightbox="../media/network-network-resources-preview.msft.png":::
   <span data-ttu-id="e3bae-305">Abbildung 19: Registerkarte " **Vorschau** "</span><span class="sxs-lookup"><span data-stu-id="e3bae-305">Figure 19:  The **Preview** tab</span></span>  
:::image-end:::  

### <span data-ttu-id="e3bae-306">Anzeigen eines Antworttexts</span><span class="sxs-lookup"><span data-stu-id="e3bae-306">View a response body</span></span>  

<span data-ttu-id="e3bae-307">So zeigen Sie den Antworttext auf eine Anforderung an:</span><span class="sxs-lookup"><span data-stu-id="e3bae-307">To view the response body to a request:</span></span>  

1.  <span data-ttu-id="e3bae-308">Wählen Sie die URL der Anforderung unter der Spalte **Name** der Tabelle Anforderungen aus.</span><span class="sxs-lookup"><span data-stu-id="e3bae-308">Select the URL of the request, under the **Name** column of the Requests table.</span></span>  
1.  <span data-ttu-id="e3bae-309">Wählen Sie die Registerkarte **Antwort** aus.</span><span class="sxs-lookup"><span data-stu-id="e3bae-309">Select the **Response** tab.</span></span>  

:::image type="complex" source="../media/network-network-resources-response.msft.png" alt-text="Die Registerkarte "Antwort"" lightbox="../media/network-network-resources-response.msft.png":::
   <span data-ttu-id="e3bae-311">Abbildung 20: die Registerkarte " **Antwort** "</span><span class="sxs-lookup"><span data-stu-id="e3bae-311">Figure 20:  The **Response** tab</span></span>  
:::image-end:::  

### <span data-ttu-id="e3bae-312">Anzeigen von HTTP-Headern</span><span class="sxs-lookup"><span data-stu-id="e3bae-312">View HTTP headers</span></span>  

<span data-ttu-id="e3bae-313">So zeigen Sie HTTP-Header Daten zu einer Anforderung an:</span><span class="sxs-lookup"><span data-stu-id="e3bae-313">To view HTTP header data about a request:</span></span>  

1.  <span data-ttu-id="e3bae-314">Wählen Sie die URL der Anforderung unter der Spalte **Name** der Tabelle Anforderungen aus.</span><span class="sxs-lookup"><span data-stu-id="e3bae-314">Select the URL of the request, under the **Name** column of the Requests table.</span></span>  
1.  <span data-ttu-id="e3bae-315">Wählen Sie die Registerkarte über **Schriften** aus.</span><span class="sxs-lookup"><span data-stu-id="e3bae-315">Select the **Headers** tab.</span></span>  

:::image type="complex" source="../media/network-resources-headers.msft.png" alt-text="Die Registerkarte "Überschriften"" lightbox="../media/network-resources-headers.msft.png":::
   <span data-ttu-id="e3bae-317">Abbildung 21: Registerkarte "über **Schriften** "</span><span class="sxs-lookup"><span data-stu-id="e3bae-317">Figure 21:  The **Headers** tab</span></span>  
:::image-end:::  

#### <span data-ttu-id="e3bae-318">Anzeigen der HTTP-Header Quelle</span><span class="sxs-lookup"><span data-stu-id="e3bae-318">View HTTP header source</span></span>  

<span data-ttu-id="e3bae-319">Standardmäßig werden auf der Registerkarte Kopfzeilennamen in alphabetischer Reihenfolge angezeigt.</span><span class="sxs-lookup"><span data-stu-id="e3bae-319">By default, the Headers tab shows header names alphabetically.</span></span>  <span data-ttu-id="e3bae-320">So zeigen Sie die HTTP-Headernamen in der Reihenfolge an, in der Sie empfangen wurden:</span><span class="sxs-lookup"><span data-stu-id="e3bae-320">To view the HTTP header names in the order they were received:</span></span>  

1.  <span data-ttu-id="e3bae-321">Öffnen Sie die Registerkarte über **Schriften** für die Anforderung, die Sie interessiert.</span><span class="sxs-lookup"><span data-stu-id="e3bae-321">Open the **Headers** tab for the request that interests you.</span></span>  <span data-ttu-id="e3bae-322">Siehe [Anzeigen von HTTP-Kopfzeilen](#view-http-headers).</span><span class="sxs-lookup"><span data-stu-id="e3bae-322">See [View HTTP headers](#view-http-headers).</span></span>  
1.  <span data-ttu-id="e3bae-323">Wählen Sie **Quelle anzeigen**neben dem Abschnitt **Anforderungs Kopfzeile** oder **Antwort Kopf** aus.</span><span class="sxs-lookup"><span data-stu-id="e3bae-323">Select **view source**, next to the **Request Header** or **Response Header** section.</span></span>  

### <span data-ttu-id="e3bae-324">Anzeigen von Abfragezeichenfolgenparametern</span><span class="sxs-lookup"><span data-stu-id="e3bae-324">View query string parameters</span></span>  

<span data-ttu-id="e3bae-325">So zeigen Sie die Abfragezeichenfolgenparameter einer URL in einem Menschen lesbaren Format an:</span><span class="sxs-lookup"><span data-stu-id="e3bae-325">To view the query string parameters of a URL in a human-readable format:</span></span>  

1.  <span data-ttu-id="e3bae-326">Öffnen Sie die Registerkarte über **Schriften** für die Anforderung, die Sie interessiert.</span><span class="sxs-lookup"><span data-stu-id="e3bae-326">Open the **Headers** tab for the request that interests you.</span></span>  <span data-ttu-id="e3bae-327">Siehe [Anzeigen von HTTP-Kopfzeilen](#view-http-headers).</span><span class="sxs-lookup"><span data-stu-id="e3bae-327">See [View HTTP headers](#view-http-headers).</span></span>  
1.  <span data-ttu-id="e3bae-328">Wechseln Sie zum Abschnitt **Abfragezeichenfolgenparameter** .</span><span class="sxs-lookup"><span data-stu-id="e3bae-328">Go to the **Query String Parameters** section.</span></span>  

:::image type="complex" source="../media/network-network-resources-headers-query-string-parameters.msft.png" alt-text="Der Abfragezeichenfolgenparameter Abschnitt" lightbox="../media/network-network-resources-headers-query-string-parameters.msft.png":::
   <span data-ttu-id="e3bae-330">Abbildung 22: Abschnitt " **Abfragezeichenfolgen-Parameter** "</span><span class="sxs-lookup"><span data-stu-id="e3bae-330">Figure 22:  The **Query String Parameters** section</span></span>  
:::image-end:::  

#### <span data-ttu-id="e3bae-331">Anzeigen der Parameterquelle für Abfragezeichenfolgen</span><span class="sxs-lookup"><span data-stu-id="e3bae-331">View query string parameters source</span></span>  

<span data-ttu-id="e3bae-332">So zeigen Sie die Abfragezeichenfolgenparameter Quelle einer Anforderung an:</span><span class="sxs-lookup"><span data-stu-id="e3bae-332">To view the query string parameter source of a request:</span></span>  

1.  <span data-ttu-id="e3bae-333">Wechseln Sie zum Abschnitt Abfragezeichenfolgenparameter.</span><span class="sxs-lookup"><span data-stu-id="e3bae-333">Go to the Query String Parameters section.</span></span>  <span data-ttu-id="e3bae-334">Weitere Informationen finden Sie unter [Anzeigen von Abfragezeichenfolgenparametern](#view-query-string-parameters).</span><span class="sxs-lookup"><span data-stu-id="e3bae-334">See [View query string parameters](#view-query-string-parameters).</span></span>  
1.  <span data-ttu-id="e3bae-335">Wählen Sie **Quelltext anzeigen**aus.</span><span class="sxs-lookup"><span data-stu-id="e3bae-335">Select **view source**.</span></span>  

#### <span data-ttu-id="e3bae-336">Anzeigen von URL-codierten Abfragezeichenfolgenparametern</span><span class="sxs-lookup"><span data-stu-id="e3bae-336">View URL-encoded query string parameters</span></span>  

<span data-ttu-id="e3bae-337">So zeigen Sie Abfragezeichenfolgenparameter in einem menschlich lesbaren Format an, jedoch mit erhaltenen Codierungen:</span><span class="sxs-lookup"><span data-stu-id="e3bae-337">To view query string parameters in a human-readable format, but with encodings preserved:</span></span>  

1.  <span data-ttu-id="e3bae-338">Wechseln Sie zum Abschnitt Abfragezeichenfolgenparameter.</span><span class="sxs-lookup"><span data-stu-id="e3bae-338">Go to the Query String Parameters section.</span></span>  <span data-ttu-id="e3bae-339">Weitere Informationen finden Sie unter [Anzeigen von Abfragezeichenfolgenparametern](#view-query-string-parameters).</span><span class="sxs-lookup"><span data-stu-id="e3bae-339">See [View query string parameters](#view-query-string-parameters).</span></span>  
1.  <span data-ttu-id="e3bae-340">Wählen Sie **URL-codiert anzeigen**aus.</span><span class="sxs-lookup"><span data-stu-id="e3bae-340">Select **view URL encoded**.</span></span>  

### <span data-ttu-id="e3bae-341">Cookies anzeigen</span><span class="sxs-lookup"><span data-stu-id="e3bae-341">View cookies</span></span>  

<span data-ttu-id="e3bae-342">So zeigen Sie die im HTTP-Header einer Anforderung gesendeten Cookies an:</span><span class="sxs-lookup"><span data-stu-id="e3bae-342">To view the cookies sent in the HTTP header of a request:</span></span>  

1.  <span data-ttu-id="e3bae-343">Wählen Sie die URL der Anforderung unter der Spalte **Name** der Tabelle Anforderungen aus.</span><span class="sxs-lookup"><span data-stu-id="e3bae-343">Select the URL of the request, under the **Name** column of the Requests table.</span></span>  
1.  <span data-ttu-id="e3bae-344">Wählen Sie die Registerkarte **Cookies** aus.</span><span class="sxs-lookup"><span data-stu-id="e3bae-344">Select the **Cookies** tab.</span></span>  

<!--See [Fields][ManageDataCookiesFields] for a description of each of the columns.  -->

<!--[ManageDataCookiesFields]: manage-data/cookies#fields  -->
<!--TODO: add link when section is available -->

:::image type="complex" source="../media/network-network-resources-cookies.msft.png" alt-text="Die Registerkarte "Cookies"" lightbox="../media/network-network-resources-cookies.msft.png":::
   <span data-ttu-id="e3bae-346">Abbildung 23: die Registerkarte "Cookies"</span><span class="sxs-lookup"><span data-stu-id="e3bae-346">Figure 23:  The Cookies tab</span></span>  
:::image-end:::  

### <span data-ttu-id="e3bae-347">Anzeigen der Zeit Plan Aufteilung einer Anforderung</span><span class="sxs-lookup"><span data-stu-id="e3bae-347">View the timing breakdown of a request</span></span>  

<span data-ttu-id="e3bae-348">So zeigen Sie die Anzeigedauer einer Anforderung an:</span><span class="sxs-lookup"><span data-stu-id="e3bae-348">To view the timing breakdown of a request:</span></span>  

1.  <span data-ttu-id="e3bae-349">Wählen Sie die URL der Anforderung unter der Spalte **Name** der Tabelle Anforderungen aus.</span><span class="sxs-lookup"><span data-stu-id="e3bae-349">Select the URL of the request, under the **Name** column of the Requests table.</span></span>  
1.  <span data-ttu-id="e3bae-350">Wählen Sie die Registerkarte **Anzeige** Dauer aus.</span><span class="sxs-lookup"><span data-stu-id="e3bae-350">Select the **Timing** tab.</span></span>  

<span data-ttu-id="e3bae-351">Eine schnellere Möglichkeit für den Zugriff auf diese Daten finden Sie unter [Anzeigen einer Zeit Plan Vorschau](#preview-a-timing-breakdown) .</span><span class="sxs-lookup"><span data-stu-id="e3bae-351">See [Preview a timing breakdown](#preview-a-timing-breakdown) for a faster way to access this data.</span></span>  

<span data-ttu-id="e3bae-352">Weitere Informationen zu den einzelnen Phasen, die auf der Registerkarte "Anzeigedauer" angezeigt werden, finden Sie unter [erläuterte Phasen der zeitlichen Verteilung](#timing-breakdown-phases-explained) .</span><span class="sxs-lookup"><span data-stu-id="e3bae-352">See [Timing breakdown phases explained](#timing-breakdown-phases-explained) for more information about each of the phases that you may see in the Timing tab.</span></span>  

:::image type="complex" source="../media/network-network-resources-timing.msft.png" alt-text="Registerkarte "Anzeigedauer"" lightbox="../media/network-network-resources-timing.msft.png":::
   <span data-ttu-id="e3bae-354">Abbildung 24: Registerkarte " **Anzeige** Dauer"</span><span class="sxs-lookup"><span data-stu-id="e3bae-354">Figure 24:  The **Timing** tab</span></span>  
:::image-end:::  

<span data-ttu-id="e3bae-355">Weitere Informationen zu den einzelnen Phasen.</span><span class="sxs-lookup"><span data-stu-id="e3bae-355">More information about each of the phases.</span></span>  

<span data-ttu-id="e3bae-356">Eine weitere Möglichkeit für den Zugriff auf diese Ansicht finden Sie unter [Aufschlüsselung der Anzeige](#view-the-timing-breakdown-of-a-request) Dauer.</span><span class="sxs-lookup"><span data-stu-id="e3bae-356">See [View timing breakdown](#view-the-timing-breakdown-of-a-request) for another way to access this view.</span></span>  

#### <span data-ttu-id="e3bae-357">Anzeigen einer Vorschau einer Anzeigedauer</span><span class="sxs-lookup"><span data-stu-id="e3bae-357">Preview a timing breakdown</span></span>  

<span data-ttu-id="e3bae-358">Wenn Sie eine Vorschau der Anzeigedauer einer Anforderung anzeigen möchten, zeigen Sie in der Spalte **Wasserfall** in der Tabelle Anforderungen auf den Eintrag für die Anforderung.</span><span class="sxs-lookup"><span data-stu-id="e3bae-358">To view a preview of the timing breakdown of a request, hover over the entry for the request in the **Waterfall** column of the Requests table.</span></span>  

<span data-ttu-id="e3bae-359">Weitere Informationen finden Sie unter [Anzeigen der zeitlichen Aufschlüsselung einer Anforderung](#view-the-timing-breakdown-of-a-request) für eine Möglichkeit, auf diese Daten zuzugreifen, für die kein Hovern erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="e3bae-359">See [View the timing breakdown of a request](#view-the-timing-breakdown-of-a-request) for a way to access this data that does not require hovering.</span></span>  

:::image type="complex" source="../media/network-network-resources-waterfall-hover.msft.png" alt-text="> Vorschau der Anzeigedauer einer Anforderung" lightbox="../media/network-network-resources-waterfall-hover.msft.png":::
   <span data-ttu-id="e3bae-361">Abbildung 25: Anzeigen einer Vorschau der Anzeigedauer einer Anforderung</span><span class="sxs-lookup"><span data-stu-id="e3bae-361">Figure 25:  Previewing the timing breakdown of a request</span></span>  
:::image-end:::  

#### <span data-ttu-id="e3bae-362">Erläuterte Phasen Aufgliederungs Phasen</span><span class="sxs-lookup"><span data-stu-id="e3bae-362">Timing breakdown phases explained</span></span>  

<span data-ttu-id="e3bae-363">Weitere Informationen zu den einzelnen Phasen, die auf der Registerkarte **Anzeige** Dauer angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="e3bae-363">More information about each of the phases you may see in the **Timing** tab.</span></span>  

*   <span data-ttu-id="e3bae-364">**Warteschlange**.</span><span class="sxs-lookup"><span data-stu-id="e3bae-364">**Queueing**.</span></span>  <span data-ttu-id="e3bae-365">Der Browser Warteschlangenanforderungen, wenn:</span><span class="sxs-lookup"><span data-stu-id="e3bae-365">The browser queues requests when:</span></span>  
    *   <span data-ttu-id="e3bae-366">Es gibt Anforderungen mit höherer Priorität.</span><span class="sxs-lookup"><span data-stu-id="e3bae-366">There are higher priority requests.</span></span>  
    *   <span data-ttu-id="e3bae-367">Für diesen Ursprung sind bereits sechs TCP-Verbindungen geöffnet, was die Grenze ist.</span><span class="sxs-lookup"><span data-stu-id="e3bae-367">There are already six TCP connections open for this origin, which is the limit.</span></span>  <span data-ttu-id="e3bae-368">Gilt nur für HTTP/1.0 und HTTP/1.1.</span><span class="sxs-lookup"><span data-stu-id="e3bae-368">Applies to HTTP/1.0 and HTTP/1.1 only.</span></span>  
    *   <span data-ttu-id="e3bae-369">Der Browser reserviert kurzzeitig Speicherplatz im Datenträgercache.</span><span class="sxs-lookup"><span data-stu-id="e3bae-369">The browser is briefly allocating space in the disk cache.</span></span>  
*   <span data-ttu-id="e3bae-370">Im **Stall**.</span><span class="sxs-lookup"><span data-stu-id="e3bae-370">**Stalled**.</span></span>  <span data-ttu-id="e3bae-371">Die Anforderung konnte aus einem der in der **Warteschlange**beschriebenen Gründe blockiert werden.</span><span class="sxs-lookup"><span data-stu-id="e3bae-371">The request could be stalled for any of the reasons described in **Queueing**.</span></span>  
*   <span data-ttu-id="e3bae-372">**DNS-Lookup**.</span><span class="sxs-lookup"><span data-stu-id="e3bae-372">**DNS Lookup**.</span></span>  <span data-ttu-id="e3bae-373">Der Browser löst die IP-Adresse für die Anforderung auf.</span><span class="sxs-lookup"><span data-stu-id="e3bae-373">The browser is resolving the IP address for the request.</span></span>  
*   <span data-ttu-id="e3bae-374">**Anfängliche Verbindung**.</span><span class="sxs-lookup"><span data-stu-id="e3bae-374">**Initial connection**.</span></span>  <span data-ttu-id="e3bae-375">Der Browser stellt eine Verbindung her, einschließlich TCP-Handshakes, TCP-Wiederholungen und Aushandeln eines SSL.</span><span class="sxs-lookup"><span data-stu-id="e3bae-375">The browser is establishing a connection including TCP handshakes, TCP retries, and negotiating an SSL.</span></span>
*   <span data-ttu-id="e3bae-376">**Proxy Verhandlung**.</span><span class="sxs-lookup"><span data-stu-id="e3bae-376">**Proxy negotiation**.</span></span>  <span data-ttu-id="e3bae-377">Der Browser verhandelt die Anforderung mit einem [Proxy Server][WikiProxyServer].</span><span class="sxs-lookup"><span data-stu-id="e3bae-377">The browser is negotiating the request with a [proxy server][WikiProxyServer].</span></span>  
*   <span data-ttu-id="e3bae-378">**Anfrage gesendet**.</span><span class="sxs-lookup"><span data-stu-id="e3bae-378">**Request sent**.</span></span>  <span data-ttu-id="e3bae-379">Die Anfrage wird gesendet.</span><span class="sxs-lookup"><span data-stu-id="e3bae-379">The request is being sent.</span></span>  
*   <span data-ttu-id="e3bae-380">**ServiceWorker-Vorbereitung**.</span><span class="sxs-lookup"><span data-stu-id="e3bae-380">**ServiceWorker Preparation**.</span></span>  <span data-ttu-id="e3bae-381">Der Browser startet den Dienstmitarbeiter.</span><span class="sxs-lookup"><span data-stu-id="e3bae-381">The browser is starting up the service worker.</span></span>  
*   <span data-ttu-id="e3bae-382">**Anforderung an ServiceWorker**.</span><span class="sxs-lookup"><span data-stu-id="e3bae-382">**Request to ServiceWorker**.</span></span>  <span data-ttu-id="e3bae-383">Die Anforderung wird an den Dienstmitarbeiter gesendet.</span><span class="sxs-lookup"><span data-stu-id="e3bae-383">The request is being sent to the service worker.</span></span>  
*   <span data-ttu-id="e3bae-384">**Waiting \ (TTFB \)**.</span><span class="sxs-lookup"><span data-stu-id="e3bae-384">**Waiting \(TTFB\)**.</span></span>  <span data-ttu-id="e3bae-385">Der Browser wartet auf das erste Byte einer Antwort.</span><span class="sxs-lookup"><span data-stu-id="e3bae-385">The browser is waiting for the first byte of a response.</span></span>  <span data-ttu-id="e3bae-386">TTFB steht für Time to First Byte.</span><span class="sxs-lookup"><span data-stu-id="e3bae-386">TTFB stands for Time To First Byte.</span></span>  <span data-ttu-id="e3bae-387">Diese Anzeigedauer umfasst eine Roundtrip-Wartezeit und den Zeitpunkt, zu dem der Server die Antwort vorbereitet hat.</span><span class="sxs-lookup"><span data-stu-id="e3bae-387">This timing includes 1 round trip of latency and the time the server took to prepare the response.</span></span>  
*   <span data-ttu-id="e3bae-388">**Inhalt herunterladen**.</span><span class="sxs-lookup"><span data-stu-id="e3bae-388">**Content Download**.</span></span>  <span data-ttu-id="e3bae-389">Der Browser empfängt die Antwort.</span><span class="sxs-lookup"><span data-stu-id="e3bae-389">The browser is receiving the response.</span></span>  
*   <span data-ttu-id="e3bae-390">**Push wird empfangen**.</span><span class="sxs-lookup"><span data-stu-id="e3bae-390">**Receiving Push**.</span></span>  <span data-ttu-id="e3bae-391">Der Browser empfängt Daten für diese Antwort über http/2 Server Push.</span><span class="sxs-lookup"><span data-stu-id="e3bae-391">The browser is receiving data for this response via HTTP/2 Server Push.</span></span>  
*   <span data-ttu-id="e3bae-392">**Lese Push**.</span><span class="sxs-lookup"><span data-stu-id="e3bae-392">**Reading Push**.</span></span>  <span data-ttu-id="e3bae-393">Der Browser liest die zuvor empfangenen lokalen Daten.</span><span class="sxs-lookup"><span data-stu-id="e3bae-393">The browser is reading the local data previously received.</span></span>  

### <span data-ttu-id="e3bae-394">Anzeigen von Initiatoren und Abhängigkeiten</span><span class="sxs-lookup"><span data-stu-id="e3bae-394">View initiators and dependencies</span></span>  

<span data-ttu-id="e3bae-395">Wenn Sie die Initiatoren und Abhängigkeiten einer Anforderung anzeigen möchten, halten Sie `Shift` die Anforderung in der Tabelle Anforderungen gedrückt, und zeigen Sie darauf.</span><span class="sxs-lookup"><span data-stu-id="e3bae-395">To view the initiators and dependencies of a request, hold `Shift`and hover over the request in the Requests table.</span></span>  <span data-ttu-id="e3bae-396">DevTools Farben: Initiatoren werden in grün angezeigt, und Abhängigkeiten werden in rot angezeigt.</span><span class="sxs-lookup"><span data-stu-id="e3bae-396">DevTools colors: initiators are shown in green and dependencies are shown in red.</span></span>  

:::image type="complex" source="../media/network-network-resources-initiators-dependencies.msft.png" alt-text="Anzeigen der Initiatoren und Abhängigkeiten einer Anforderung" lightbox="../media/network-network-resources-initiators-dependencies.msft.png":::
   <span data-ttu-id="e3bae-398">Abbildung 26: Anzeigen der Initiatoren und Abhängigkeiten einer Anforderung</span><span class="sxs-lookup"><span data-stu-id="e3bae-398">Figure 26:  Viewing the initiators and dependencies of a request</span></span>  
:::image-end:::  

<span data-ttu-id="e3bae-399">Wenn die Anforderungstabelle chronologisch geordnet ist, ist die erste grüne Anforderung oberhalb des Cursors der Initiator der Abhängigkeit.</span><span class="sxs-lookup"><span data-stu-id="e3bae-399">When the Requests table is ordered chronologically, the first green request above the one you are hovering is the initiator of the dependency.</span></span>  <span data-ttu-id="e3bae-400">Wenn darüber eine weitere grüne Anforderung angezeigt wird, ist diese höhere Anforderung der Initiator des Initiators.</span><span class="sxs-lookup"><span data-stu-id="e3bae-400">If another green request appears above that, that higher request is the initiator of the initiator.</span></span>  <span data-ttu-id="e3bae-401">Und so weiter.</span><span class="sxs-lookup"><span data-stu-id="e3bae-401">And so on.</span></span>  

### <span data-ttu-id="e3bae-402">Laden Ereignisse anzeigen</span><span class="sxs-lookup"><span data-stu-id="e3bae-402">View load events</span></span>  

<span data-ttu-id="e3bae-403">DevTools zeigt die Anzeigedauer der `DOMContentLoaded` `load` Ereignisse und Ereignisse an mehreren Stellen im Netzwerk Panel an.</span><span class="sxs-lookup"><span data-stu-id="e3bae-403">DevTools displays the timing of the `DOMContentLoaded` and `load` events in multiple places on the Network panel.</span></span>  <span data-ttu-id="e3bae-404">Das `DOMContentLoaded` Ereignis ist blau gefärbt, und das `load` Ereignis ist rot.</span><span class="sxs-lookup"><span data-stu-id="e3bae-404">The `DOMContentLoaded` event is colored blue, and the `load` event is red.</span></span>  

:::image type="complex" source="../media/network-network-requests-load-events.msft.png" alt-text="Die Speicherorte der DOMContentLoaded-und Load-Ereignisse im Netzwerk Panel" lightbox="../media/network-network-requests-load-events.msft.png":::
   <span data-ttu-id="e3bae-406">Abbildung 27: die Speicherorte der `DOMContentLoaded` und- `load` Ereignisse im Netzwerk Panel</span><span class="sxs-lookup"><span data-stu-id="e3bae-406">Figure 27:  The locations of the `DOMContentLoaded` and `load` events on the Network panel</span></span>  
:::image-end:::  

### <span data-ttu-id="e3bae-407">Anzeigen der Gesamtzahl der Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e3bae-407">View the total number of requests</span></span>  

<span data-ttu-id="e3bae-408">Die Gesamtzahl der Anforderungen wird im Bereich "Zusammenfassung" unten im Netzwerkbereich aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="e3bae-408">The total number of requests is listed in the Summary pane, at the bottom of the Network panel.</span></span>  

> [!CAUTION]
> <span data-ttu-id="e3bae-409">Diese Nummer verfolgt nur Anforderungen, die seit dem Öffnen von devtools protokolliert wurden.</span><span class="sxs-lookup"><span data-stu-id="e3bae-409">This number only tracks requests that have been logged since DevTools was opened.</span></span>  <span data-ttu-id="e3bae-410">Wenn vor dem Öffnen von devtools andere Anforderungen aufgetreten sind, werden diese Anforderungen nicht gezählt.</span><span class="sxs-lookup"><span data-stu-id="e3bae-410">If other requests occurred before DevTools was opened, those requests are not counted.</span></span>  

:::image type="complex" source="../media/network-network-total-requests.msft.png" alt-text="Die Gesamtzahl der Anforderungen seit dem Öffnen von devtools" lightbox="../media/network-network-total-requests.msft.png":::
   <span data-ttu-id="e3bae-412">Abbildung 28: die Gesamtzahl der Anforderungen seit dem Öffnen von devtools</span><span class="sxs-lookup"><span data-stu-id="e3bae-412">Figure 28:  The total number of requests since DevTools was opened</span></span>  
:::image-end:::  

### <span data-ttu-id="e3bae-413">Anzeigen der Gesamtgröße des Downloads</span><span class="sxs-lookup"><span data-stu-id="e3bae-413">View the total download size</span></span>  

<span data-ttu-id="e3bae-414">Die Gesamtgröße der Downloadanforderungen wird im Bereich "Zusammenfassung" am unteren Rand des Netzwerkbereichs angezeigt.</span><span class="sxs-lookup"><span data-stu-id="e3bae-414">The total download size of requests is listed in the Summary pane, at the bottom of the Network panel.</span></span>  

> [!CAUTION]
> <span data-ttu-id="e3bae-415">Diese Nummer verfolgt nur Anforderungen, die seit dem Öffnen von devtools protokolliert wurden.</span><span class="sxs-lookup"><span data-stu-id="e3bae-415">This number only tracks requests that have been logged since DevTools was opened.</span></span>  <span data-ttu-id="e3bae-416">Wenn vor dem Öffnen von devtools andere Anforderungen aufgetreten sind, werden die vorherigen Anforderungen nicht gezählt.</span><span class="sxs-lookup"><span data-stu-id="e3bae-416">If other requests occurred before DevTools was opened, the previous requests are not counted.</span></span>  

:::image type="complex" source="../media/network-network-total-download-size.msft.png" alt-text="Die Gesamtgröße der Downloads von Anforderungen" lightbox="../media/network-network-total-download-size.msft.png":::
   <span data-ttu-id="e3bae-418">Abbildung 29: die Gesamtgröße der Downloads von Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e3bae-418">Figure 29:  The total download size of requests</span></span>  
:::image-end:::  

<span data-ttu-id="e3bae-419">Weitere Informationen finden Sie unter [Anzeigen der unkomprimierten Größe einer Ressource](#view-the-uncompressed-size-of-a-resource) , um zu sehen, wie groß die Ressourcen sind, nachdem der Browser die einzelnen Elemente dekomprimiert hat.</span><span class="sxs-lookup"><span data-stu-id="e3bae-419">See [View the uncompressed size of a resource](#view-the-uncompressed-size-of-a-resource) to see how large resources are after the browser uncompresses each item.</span></span>  

### <span data-ttu-id="e3bae-420">Anzeigen der Stapelüberwachung, die eine Anforderung verursacht hat</span><span class="sxs-lookup"><span data-stu-id="e3bae-420">View the stack trace that caused a request</span></span>  

<span data-ttu-id="e3bae-421">Nachdem eine JavaScript-Anweisung eine Ressource angefordert hat, zeigen Sie mit der Maus auf die Spalte **Initiator** , um die Stapelüberwachung anzuzeigen, die zur Anforderung führt.</span><span class="sxs-lookup"><span data-stu-id="e3bae-421">After a JavaScript statement requests a resource, hover over the **Initiator** column to view the stack trace leading up to the request.</span></span>  

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
   <span data-ttu-id="e3bae-423">Abbildung 30: die Stapelüberwachung, die zu einer Ressourcenanforderung führt</span><span class="sxs-lookup"><span data-stu-id="e3bae-423">Figure 30:  The stack trace leading up to a resource request</span></span>  
:::image-end:::  

### <span data-ttu-id="e3bae-424">Anzeigen der unkomprimierten Größe einer Ressource</span><span class="sxs-lookup"><span data-stu-id="e3bae-424">View the uncompressed size of a resource</span></span>  

<span data-ttu-id="e3bae-425">Aktivieren Sie das Kontrollkästchen **große Anforderungs Zeilen verwenden** , und schauen Sie sich den niedrigsten Wert der Spalte **Größe** an.</span><span class="sxs-lookup"><span data-stu-id="e3bae-425">Select the **Use large request rows** checkbox and then look at the bottom value of the **Size** column.</span></span>  

:::image type="complex" source="../media/network-network-requests-uncompressed-compare.msft.png" alt-text="Beispiel für nicht komprimierte Ressourcen" lightbox="../media/network-network-requests-uncompressed-compare.msft.png":::
   <span data-ttu-id="e3bae-427">Abbildung 31: ein Beispiel für nicht komprimierte Ressourcen \ (die komprimierte Größe der `jquery-3.3.1.min.js` Datei, die über das Netzwerk gesendet wurde `29.9 KB` , während die unkomprimierte Größe `84.9 KB` \) war</span><span class="sxs-lookup"><span data-stu-id="e3bae-427">Figure 31:  An example of uncompressed resources  \(The compressed size of the `jquery-3.3.1.min.js` file that was sent over the network was `29.9 KB`, whereas the uncompressed size was `84.9 KB`\)</span></span>  
:::image-end:::  

## <span data-ttu-id="e3bae-428">Exportieren von Anforderungsdaten</span><span class="sxs-lookup"><span data-stu-id="e3bae-428">Export requests data</span></span>  

### <span data-ttu-id="e3bae-429">Speichern aller Netzwerkanforderungen in einer har-Datei</span><span class="sxs-lookup"><span data-stu-id="e3bae-429">Save all network requests to a HAR file</span></span>  

<span data-ttu-id="e3bae-430">Führen Sie die folgenden Schritte aus, um alle Netzwerkanforderungen in einer har-Datei zu speichern.</span><span class="sxs-lookup"><span data-stu-id="e3bae-430">To save all network requests to a HAR file, complete the following steps.</span></span>  

1.  <span data-ttu-id="e3bae-431">Zeigen Sie auf jede Anforderung in der Tabelle Anforderungen, und öffnen Sie das Kontextmenü \ (mit der rechten Maustaste auf \).</span><span class="sxs-lookup"><span data-stu-id="e3bae-431">Hover on any request in the Requests table and open the contextual menu \(right-click\).</span></span>  
1.  <span data-ttu-id="e3bae-432">Wählen Sie **als har mit Inhalt speichern**aus.</span><span class="sxs-lookup"><span data-stu-id="e3bae-432">Select **Save as HAR with Content**.</span></span>  <span data-ttu-id="e3bae-433">DevTools speichert alle Anforderungen, die seit dem Öffnen von devtools in der har-Datei aufgetreten sind.</span><span class="sxs-lookup"><span data-stu-id="e3bae-433">DevTools saves all requests that have occurred since you opened DevTools to the HAR file.</span></span>  <span data-ttu-id="e3bae-434">Es gibt keine Möglichkeit, Anforderungen zu filtern oder nur eine einzige Anforderung zu speichern.</span><span class="sxs-lookup"><span data-stu-id="e3bae-434">There is no way to filter requests, or to save just a single request.</span></span>  

<span data-ttu-id="e3bae-435">Nachdem Sie eine har-Datei gespeichert haben, können Sie Sie für die Analyse wieder in devtools importieren.</span><span class="sxs-lookup"><span data-stu-id="e3bae-435">Once you save a HAR file, you may import it back into DevTools for analysis.</span></span>  <span data-ttu-id="e3bae-436">Ziehen Sie die har-Datei einfach per Drag & Drop in die Tabelle "Anforderungen".</span><span class="sxs-lookup"><span data-stu-id="e3bae-436">Just drag-and-drop the HAR file into the Requests table.</span></span>  
<!--See also [HAR Analyzer][HARAnalyzer].  -->  

<!--[HARAnalyzer]: https://toolbox.alphabetapps.com/apps/har_analyzer  -->  
<!--Todo: add section link when content is available  -->  

:::image type="complex" source="../media/network-network-requests-save-har-content.msft.png" alt-text="Auswählen von "als har mit Inhalt speichern"" lightbox="../media/network-network-requests-save-har-content.msft.png":::
   <span data-ttu-id="e3bae-438">Abbildung 32: auswählen **von "als har mit Inhalt speichern** "</span><span class="sxs-lookup"><span data-stu-id="e3bae-438">Figure 32:  Selecting **Save as HAR with Content**</span></span>  
:::image-end:::  

### <span data-ttu-id="e3bae-439">Kopieren einer oder mehrerer Anforderungen in die Zwischenablage</span><span class="sxs-lookup"><span data-stu-id="e3bae-439">Copy one or more requests to the clipboard</span></span>  

<span data-ttu-id="e3bae-440">Zeigen Sie unter der Spalte **Name** der Tabelle Anforderungen auf eine Anforderung, öffnen Sie das Kontextmenü \ (Klicken Sie mit der rechten Maustaste auf \), zeigen Sie auf **Kopieren**, und wählen Sie eine der folgenden Optionen aus.</span><span class="sxs-lookup"><span data-stu-id="e3bae-440">Under the **Name** column of the Requests table, hover on a request, open the contextual menu \(right-click\), hover over **Copy**, and select one of the following options.</span></span>  

*   <span data-ttu-id="e3bae-441">**Link Adresse kopieren**</span><span class="sxs-lookup"><span data-stu-id="e3bae-441">**Copy Link Address**.</span></span>  <span data-ttu-id="e3bae-442">Kopieren Sie die URL der Anforderung in die Zwischenablage.</span><span class="sxs-lookup"><span data-stu-id="e3bae-442">Copy the URL of the request to the clipboard.</span></span>  
*   <span data-ttu-id="e3bae-443">**Antwort kopieren**</span><span class="sxs-lookup"><span data-stu-id="e3bae-443">**Copy Response**.</span></span>  <span data-ttu-id="e3bae-444">Kopieren Sie den Antworttext in die Zwischenablage.</span><span class="sxs-lookup"><span data-stu-id="e3bae-444">Copy the response body to the clipboard.</span></span>  
*   <span data-ttu-id="e3bae-445">**Als FETCH kopieren**</span><span class="sxs-lookup"><span data-stu-id="e3bae-445">**Copy as Fetch**.</span></span>  
*   <span data-ttu-id="e3bae-446">**Als curl kopieren**</span><span class="sxs-lookup"><span data-stu-id="e3bae-446">**Copy as cURL**.</span></span>  <span data-ttu-id="e3bae-447">Kopieren Sie die Anforderung als curl-Befehl.</span><span class="sxs-lookup"><span data-stu-id="e3bae-447">Copy the request as a cURL command.</span></span>  
*   <span data-ttu-id="e3bae-448">**Kopieren Sie alle als FETCH**.</span><span class="sxs-lookup"><span data-stu-id="e3bae-448">**Copy All as Fetch**.</span></span>  
*   <span data-ttu-id="e3bae-449">**Kopieren Sie alle als curl**.</span><span class="sxs-lookup"><span data-stu-id="e3bae-449">**Copy All as cURL**.</span></span>  <span data-ttu-id="e3bae-450">Kopieren Sie alle Anforderungen als eine Kette von curl-Befehlen.</span><span class="sxs-lookup"><span data-stu-id="e3bae-450">Copy all requests as a chain of cURL commands.</span></span>  
*   <span data-ttu-id="e3bae-451">**Kopieren Sie alle als har**.</span><span class="sxs-lookup"><span data-stu-id="e3bae-451">**Copy All as HAR**.</span></span>  <span data-ttu-id="e3bae-452">Kopieren Sie alle Anforderungen als har-Daten.</span><span class="sxs-lookup"><span data-stu-id="e3bae-452">Copy all requests as HAR data.</span></span>  

:::image type="complex" source="../media/network-network-requests-copy-response.msft.png" alt-text="Auswählen von "Antwort kopieren"" lightbox="../media/network-network-requests-copy-response.msft.png":::
   <span data-ttu-id="e3bae-454">Abbildung 33: Auswählen von " **Antwort kopieren** "</span><span class="sxs-lookup"><span data-stu-id="e3bae-454">Figure 33:  Selecting **Copy Response**</span></span>  
:::image-end:::  

## <span data-ttu-id="e3bae-455">Ändern des Layouts des Netzwerk Panels</span><span class="sxs-lookup"><span data-stu-id="e3bae-455">Change the layout of the Network panel</span></span>  

<span data-ttu-id="e3bae-456">Sie können Abschnitte der Netzwerk Panel-UI erweitern oder reduzieren, um wichtige Informationen zu konzentrieren.</span><span class="sxs-lookup"><span data-stu-id="e3bae-456">You may expand or collapse sections of the Network panel UI to focus important information.</span></span>  

### <span data-ttu-id="e3bae-457">Ausblenden des Bereichs "Filter"</span><span class="sxs-lookup"><span data-stu-id="e3bae-457">Hide the Filters pane</span></span>  

<span data-ttu-id="e3bae-458">Standardmäßig zeigt devtools den **Bereich "Filter"** an.</span><span class="sxs-lookup"><span data-stu-id="e3bae-458">By default, DevTools shows the **Filters pane**.</span></span>  
<span data-ttu-id="e3bae-459">Wählen Sie **Filter** ![ Filter aus ][ImageFilterIcon] , um sie auszublenden.</span><span class="sxs-lookup"><span data-stu-id="e3bae-459">Select **Filter** ![Filter][ImageFilterIcon] to hide it.</span></span>  

:::image type="complex" source="../media/network-network-resources-hide-filters-button.msft.png" alt-text="Schaltfläche "Filter ausblenden"" lightbox="../media/network-network-resources-hide-filters-button.msft.png":::
   <span data-ttu-id="e3bae-461">Abbildung 34: die Schaltfläche "Filter ausblenden"</span><span class="sxs-lookup"><span data-stu-id="e3bae-461">Figure 34:  The Hide Filters button</span></span>  
:::image-end:::  

### <span data-ttu-id="e3bae-462">Verwenden von umfangreichen Anforderungs Zeilen</span><span class="sxs-lookup"><span data-stu-id="e3bae-462">Use large request rows</span></span>  

<span data-ttu-id="e3bae-463">Verwenden Sie große Zeilen, wenn in Ihrer Netzwerk Anforderungstabelle mehr Leerzeichen verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="e3bae-463">Use large rows when you want more whitespace in your network requests table.</span></span>  <span data-ttu-id="e3bae-464">Einige Spalten liefern auch ein wenig mehr Informationen, wenn Sie große Zeilen verwenden.</span><span class="sxs-lookup"><span data-stu-id="e3bae-464">Some columns also provide a little more information when using large rows.</span></span>  <span data-ttu-id="e3bae-465">Der untere Wert der Spalte **size** entspricht beispielsweise der unkomprimierten Größe einer Anforderung.</span><span class="sxs-lookup"><span data-stu-id="e3bae-465">For example, the bottom value of the **Size** column is the uncompressed size of a request.</span></span>  

:::image type="complex" source="../media/network-network-requests-large-request-rows.msft.png" alt-text="Ein Beispiel für große Anforderungs Zeilen im Bereich "Anforderungen"" lightbox="../media/network-network-requests-large-request-rows.msft.png":::
   <span data-ttu-id="e3bae-467">Abbildung 35: ein Beispiel für große Anforderungs Zeilen im Bereich " **Anforderungen** "</span><span class="sxs-lookup"><span data-stu-id="e3bae-467">Figure 35:  An example of large request rows in the **Requests** pane</span></span>  
:::image-end:::  

<span data-ttu-id="e3bae-468">Aktivieren Sie das Kontrollkästchen **große Anforderungs Zeilen verwenden** , um große Zeilen zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="e3bae-468">Select the **Use large request rows** checkbox to enable large rows.</span></span>  

:::image type="complex" source="../media/network-network-requests-use-large-request-rows-on.msft.png" alt-text="Das Kontrollkästchen "große Anforderungs Zeilen verwenden"" lightbox="../media/network-network-requests-use-large-request-rows-on.msft.png":::
   <span data-ttu-id="e3bae-470">Abbildung 36: Kontrollkästchen " **große Anforderungs Zeilen verwenden** "</span><span class="sxs-lookup"><span data-stu-id="e3bae-470">Figure 36:  The **Use large request rows** checkbox</span></span>  
:::image-end:::  

### <span data-ttu-id="e3bae-471">Ausblenden des Bereichs "Übersicht"</span><span class="sxs-lookup"><span data-stu-id="e3bae-471">Hide the Overview pane</span></span>  

<span data-ttu-id="e3bae-472">Standardmäßig zeigt devtools den **Bereich "Übersicht"** an.</span><span class="sxs-lookup"><span data-stu-id="e3bae-472">By default, DevTools shows the **Overview pane**.</span></span>  <span data-ttu-id="e3bae-473">Deaktivieren Sie das Kontrollkästchen " **Übersicht anzeigen** ", um es auszublenden.</span><span class="sxs-lookup"><span data-stu-id="e3bae-473">Deselect the **Show Overview** checkbox to hide it.</span></span>  

:::image type="complex" source="../media/network-network-requests-show-overview-off.msft.png" alt-text="Kontrollkästchen ' Übersicht anzeigen '" lightbox="../media/network-network-requests-show-overview-off.msft.png":::
   <span data-ttu-id="e3bae-475">Abbildung 37: Kontrollkästchen ' **Übersicht anzeigen** '</span><span class="sxs-lookup"><span data-stu-id="e3bae-475">Figure 37:  The **Show Overview** checkbox</span></span>  
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
> <span data-ttu-id="e3bae-479">Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e3bae-479">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="e3bae-480">Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/network/reference) und wird von [Kayce Basken][KayceBasques] (Technical Writer, Chrome devtools \ & Lighthouse \) erstellt.</span><span class="sxs-lookup"><span data-stu-id="e3bae-480">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/network/reference) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
<span data-ttu-id="e3bae-482">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="e3bae-482">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
