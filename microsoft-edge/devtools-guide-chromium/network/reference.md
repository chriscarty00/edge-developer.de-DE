---
description: Eine umfassende Referenz zu den Features des Microsoft Edge devtools-Netzwerk Panels.
title: Netzwerkanalyse Referenz
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/19/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: 8123fbebadf1d43fd1460ecebf91190cac793e19
ms.sourcegitcommit: 99eee78698dc95b2a3fa638a5b063ef449899cda
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/20/2020
ms.locfileid: "11125370"
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

# <span data-ttu-id="200bd-104">Netzwerkanalyse Referenz</span><span class="sxs-lookup"><span data-stu-id="200bd-104">Network Analysis reference</span></span>  

<span data-ttu-id="200bd-105">Entdecken Sie neue Möglichkeiten zur Analyse, wie Ihre Seite in dieser umfassenden Referenz der Microsoft Edge devtools-Netzwerkanalyse Features geladen werden kann.</span><span class="sxs-lookup"><span data-stu-id="200bd-105">Discover new ways to analyze how your page loads in this comprehensive reference of Microsoft Edge DevTools network analysis features.</span></span>  

<!--
> [!NOTE]
> This reference is based on Microsoft Edge 58.  If you use another version of Microsoft Edge, the UI, and features of DevTools may be different.  To verify which version of Microsoft Edge you are running, navigate to `edge://help`.  
-->

## <span data-ttu-id="200bd-106">Aufzeichnen von Netzwerkanforderungen</span><span class="sxs-lookup"><span data-stu-id="200bd-106">Record network requests</span></span>  

<span data-ttu-id="200bd-107">Standardmäßig zeichnet devtools alle Netzwerkanforderungen im Netzwerk Panel auf, solange devtools geöffnet ist.</span><span class="sxs-lookup"><span data-stu-id="200bd-107">By default, DevTools record all network requests in the Network panel, so long as DevTools is open.</span></span>  

:::image type="complex" source="../media/network-network-panel.msft.png" alt-text="Netzwerk Panel" lightbox="../media/network-network-panel.msft.png":::
   <span data-ttu-id="200bd-109">**Netzwerk** Panel</span><span class="sxs-lookup"><span data-stu-id="200bd-109">The **Network** panel</span></span>  
:::image-end:::  

### <span data-ttu-id="200bd-110">Beenden der Aufzeichnung von Netzwerkanforderungen</span><span class="sxs-lookup"><span data-stu-id="200bd-110">Stop recording network requests</span></span>  

<span data-ttu-id="200bd-111">Führen Sie die folgenden Schritte aus, um die Aufzeichnung von Anforderungen zu beenden.</span><span class="sxs-lookup"><span data-stu-id="200bd-111">To stop recording requests, complete the following steps.</span></span>  

1.  <span data-ttu-id="200bd-112">Wählen Sie im Netzwerk Panel die Option **Aufzeichnung** ![ des Netzwerkprotokolls beenden aufzeichnen ][ImageRecordOnIcon] aus. **Network**</span><span class="sxs-lookup"><span data-stu-id="200bd-112">Choose **Stop recording network log** ![Stop recording network log][ImageRecordOnIcon] on the **Network** panel.</span></span>  <span data-ttu-id="200bd-113">Es wird grau, um anzugeben, dass devtools keine Anforderungen mehr aufzeichnet.</span><span class="sxs-lookup"><span data-stu-id="200bd-113">It turns grey to indicate that DevTools is no longer recording requests.</span></span>  
1.  <span data-ttu-id="200bd-114">Wählen Sie `Control` + `E` \ (Windows, Linux \) oder `Command` + `E` \ (macOS \) aus, während sich der Fokus des **Netzwerk** Panels befindet.</span><span class="sxs-lookup"><span data-stu-id="200bd-114">Select `Control`+`E` \(Windows, Linux\) or `Command`+`E` \(macOS\) while the **Network** panel is in focus.</span></span>  

### <span data-ttu-id="200bd-115">Löschen von Anforderungen</span><span class="sxs-lookup"><span data-stu-id="200bd-115">Clear requests</span></span>  

<span data-ttu-id="200bd-116">Wählen Sie im Netzwerk Panel die Option **"Löschen"** ![ ][ImageClearIcon] aus, um alle Anforderungen aus der Tabelle "Anforderungen" zu löschen.</span><span class="sxs-lookup"><span data-stu-id="200bd-116">Choose **Clear** \(![Clear][ImageClearIcon]\) on the Network panel to clear all requests from the Requests table.</span></span>  

:::image type="complex" source="../media/network-network-clear-button.msft.png" alt-text="Netzwerk Panel" lightbox="../media/network-network-clear-button.msft.png":::
   <span data-ttu-id="200bd-118">Die Schaltfläche " **Löschen** "</span><span class="sxs-lookup"><span data-stu-id="200bd-118">The **Clear** button</span></span>  
:::image-end:::  

### <span data-ttu-id="200bd-119">Speichern von Anforderungen über Seitenlasten hinweg</span><span class="sxs-lookup"><span data-stu-id="200bd-119">Save requests across page loads</span></span>  

<span data-ttu-id="200bd-120">Aktivieren Sie das Kontrollkästchen **Protokoll beibehalten** auf der Registerkarte Netzwerk, um Anforderungen zwischen den Seitenlasten zu speichern.</span><span class="sxs-lookup"><span data-stu-id="200bd-120">To save requests across page loads, check the **Preserve log** checkbox on the Network panel.</span></span>  <span data-ttu-id="200bd-121">DevTools speichert alle Anforderungen, bis Sie **Protokoll beibehalten**deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="200bd-121">DevTools saves all requests until you disable **Preserve log**.</span></span>  

:::image type="complex" source="../media/network-network-preserve-log.msft.png" alt-text="Netzwerk Panel" lightbox="../media/network-network-preserve-log.msft.png":::
   <span data-ttu-id="200bd-123">Kontrollkästchen " **Protokoll beibehalten** "</span><span class="sxs-lookup"><span data-stu-id="200bd-123">The **Preserve Log** checkbox</span></span>  
:::image-end:::  

### <span data-ttu-id="200bd-124">Aufzeichnen von Screenshots beim Laden der Seite</span><span class="sxs-lookup"><span data-stu-id="200bd-124">Capture screenshots during page load</span></span>  

<span data-ttu-id="200bd-125">Screenshots aufzeichnen, um zu analysieren, was für Benutzer angezeigt wird, während Sie darauf warten, dass Ihre Seite geladen wird.</span><span class="sxs-lookup"><span data-stu-id="200bd-125">Capture screenshots to analyze what displays for users while waiting for your page to load.</span></span>  

<span data-ttu-id="200bd-126">Wenn Sie Screenshots aktivieren möchten, wählen Sie **Netzwerkeinstellungen** und dann auf der Registerkarte **Netzwerk** die Option **Screenshots aufzeichnen** aus.</span><span class="sxs-lookup"><span data-stu-id="200bd-126">To enable screenshots, choose **Network settings** and choose **Capture screenshots** checkbox on the **Network** panel.</span></span>  

<span data-ttu-id="200bd-127">Aktualisieren Sie die Seite, während sich das **Netzwerk** Panel im Fokus befindet, um Screenshots zu erfassen.</span><span class="sxs-lookup"><span data-stu-id="200bd-127">Refresh the page while the **Network** panel is in focus to capture screenshots.</span></span>  

<span data-ttu-id="200bd-128">Nachdem Sie einen Screenshot aufgezeichnet haben, interagieren Sie mit ihm auf die folgende Weise.</span><span class="sxs-lookup"><span data-stu-id="200bd-128">After capturing a screenshot, you interact with it in the following ways.</span></span>  

*   <span data-ttu-id="200bd-129">Zeigen Sie mit der Maus auf einen Screenshot, um den Punkt anzuzeigen, an dem dieser Screenshot aufgenommen wurde.</span><span class="sxs-lookup"><span data-stu-id="200bd-129">Hover over a screenshot to view the point at which that screenshot was captured.</span></span>  <span data-ttu-id="200bd-130">Im Bereich " **Übersicht** " wird eine gelbe Zeile angezeigt.</span><span class="sxs-lookup"><span data-stu-id="200bd-130">A yellow line is displayed on the **Overview** pane.</span></span>  
*   <span data-ttu-id="200bd-131">Wählen Sie die Miniaturansicht eines Bildschirms aus, um alle Anforderungen zu filtern, die nach dem Erfassen des Screenshots aufgetreten sind.</span><span class="sxs-lookup"><span data-stu-id="200bd-131">Select the thumbnail of a screen to filter out any requests that occurred after the screenshot was captured.</span></span>  
*   <span data-ttu-id="200bd-132">Doppelklicken Sie auf eine Miniaturansicht, um Sie zu vergrößern.</span><span class="sxs-lookup"><span data-stu-id="200bd-132">Double-click a thumbnail to zoom into it.</span></span>  

:::image type="complex" source="../media/network-network-screenshot-hover.msft.png" alt-text="Netzwerk Panel" lightbox="../media/network-network-screenshot-hover.msft.png":::
   <span data-ttu-id="200bd-134">Zeigen auf einen Screenshot</span><span class="sxs-lookup"><span data-stu-id="200bd-134">Hovering over a screenshot</span></span>  
:::image-end:::  

<!--  ### Replay XHR request  -->

<!--  To replay an XHR request, hover on the request in the Requests table, open the contextual menu \(right-click\), and choose **Replay XHR**.  -->

<!--  
:::image type="complex" source="../media/network-replay-xhr.msft.png" alt-text="Netzwerk Panel" lightbox="../media/network-replay-xhr.msft.png":::
   Selecting Replay XHR  
:::image-end:::  
-->  

## <span data-ttu-id="200bd-135">Ändern des Ladeverhaltens</span><span class="sxs-lookup"><span data-stu-id="200bd-135">Change loading behavior</span></span>  

### <span data-ttu-id="200bd-136">Emulieren eines erstmaligen Besuchers durch Deaktivieren des Browsercaches</span><span class="sxs-lookup"><span data-stu-id="200bd-136">Emulate a first-time visitor by disabling the browser cache</span></span>  

<span data-ttu-id="200bd-137">Aktivieren Sie das Kontrollkästchen **Cache deaktivieren** , um zu emulieren, wie ein Erstbenutzer Ihre Website erlebt.</span><span class="sxs-lookup"><span data-stu-id="200bd-137">To emulate how a first-time user experiences your site, check the **Disable cache** checkbox.</span></span>  <span data-ttu-id="200bd-138">DevTools deaktiviert den Browsercache.</span><span class="sxs-lookup"><span data-stu-id="200bd-138">DevTools disables the browser cache.</span></span>  <span data-ttu-id="200bd-139">Dieses Feature emuliert die Benutzerfreundlichkeit des ersten Benutzers genauer, da Anforderungen im Browser-Cache für wiederholte Besuche bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="200bd-139">This feature more accurately emulates a first-time user's experience, because requests are served from the browser cache on repeat visits.</span></span>  

:::image type="complex" source="../media/network-network-disable-cache-checkbox.msft.png" alt-text="Netzwerk Panel" lightbox="../media/network-network-disable-cache-checkbox.msft.png":::
   <span data-ttu-id="200bd-141">Kontrollkästchen " **Cache deaktivieren** "</span><span class="sxs-lookup"><span data-stu-id="200bd-141">The **Disable Cache** checkbox</span></span>  
:::image-end:::  

#### <span data-ttu-id="200bd-142">Deaktivieren des Browser-Caches aus der Schublade "Netzwerkbedingungen"</span><span class="sxs-lookup"><span data-stu-id="200bd-142">Disable the browser cache from the Network Conditions drawer</span></span>  

<span data-ttu-id="200bd-143">Wenn Sie den Cache während der Arbeit in anderen devtools-Panels deaktivieren möchten, verwenden Sie die Schublade Netzwerkbedingungen.</span><span class="sxs-lookup"><span data-stu-id="200bd-143">If you want to disable the cache while working in other DevTools panels, use the Network Conditions drawer.</span></span>  

1.  <span data-ttu-id="200bd-144">Öffnen Sie die Schublade **Netzwerkbedingungen** .</span><span class="sxs-lookup"><span data-stu-id="200bd-144">Open the **Network Conditions** drawer.</span></span>  
1.  <span data-ttu-id="200bd-145">Aktivieren oder deaktivieren Sie das Kontrollkästchen **Cache deaktivieren** .</span><span class="sxs-lookup"><span data-stu-id="200bd-145">Check or uncheck the **Disable cache** checkbox.</span></span>  

<!--todo: add network condition section when available -->  

### <span data-ttu-id="200bd-146">Manuelles Löschen des Browsercaches</span><span class="sxs-lookup"><span data-stu-id="200bd-146">Manually clear the browser cache</span></span>  

<span data-ttu-id="200bd-147">Wenn Sie den Browser-Cache jederzeit manuell löschen möchten, öffnen Sie das Kontextmenü \ (Klicken Sie mit der rechten Maustaste auf \) an einer beliebigen Stelle in der Tabelle Anforderungen, und wählen Sie **Browsercache löschen**aus.</span><span class="sxs-lookup"><span data-stu-id="200bd-147">To manually clear the browser cache at any time, open the contextual menu \(right-click\) anywhere in the Requests table and choose **Clear Browser Cache**.</span></span>  

:::image type="complex" source="../media/network-network-clear-browser-cache.msft.png" alt-text="Netzwerk Panel" lightbox="../media/network-network-clear-browser-cache.msft.png":::
   <span data-ttu-id="200bd-149">Auswählen des **Browser Cache löschen**</span><span class="sxs-lookup"><span data-stu-id="200bd-149">Selecting **Clear Browser Cache**</span></span>  
:::image-end:::  

### <span data-ttu-id="200bd-150">Offline emulieren</span><span class="sxs-lookup"><span data-stu-id="200bd-150">Emulate offline</span></span>  

<span data-ttu-id="200bd-151">Eine neue Klasse von Web-Apps mit dem Namen " [Progressive Web Apps][DevtoolsProgressiveWebApps]" funktioniert mit Hilfe von **Servicemitarbeitern**offline.</span><span class="sxs-lookup"><span data-stu-id="200bd-151">A new class of web apps, named [Progressive Web Apps][DevtoolsProgressiveWebApps], functions offline with the help of **service workers**.</span></span>  <span data-ttu-id="200bd-152">Möglicherweise ist es hilfreich, ein Gerät, das keine Datenverbindung aufweist, schnell zu simulieren, wenn Sie diese Art von App erstellen.</span><span class="sxs-lookup"><span data-stu-id="200bd-152">You may find it useful to quickly simulate a device that has no data connection when you are building this type of app.</span></span>  

<!--[ServiceWorkers]: /web/fundamentals/getting-started/primers/service-workers  -->

<span data-ttu-id="200bd-153">Wählen Sie das Dropdownmenü **Online** aus, suchen Sie unter **Voreinstellungen**, und wählen Sie **Offline** aus, um eine Offlinenetzwerk Umgebung zu simulieren.</span><span class="sxs-lookup"><span data-stu-id="200bd-153">Select the **Online** dropdown menu, search under **Presets**, and choose **Offline** to simulate an offline network experience.</span></span>  

:::image type="complex" source="../media/network-network-offline-dropdown.msft.png" alt-text="Netzwerk Panel" lightbox="../media/network-network-offline-dropdown.msft.png":::
   <span data-ttu-id="200bd-155">Das **Offline** -Dropdownmenü</span><span class="sxs-lookup"><span data-stu-id="200bd-155">The **Offline** dropdown menu</span></span>  
:::image-end:::  

### <span data-ttu-id="200bd-156">Emulieren langsamer Netzwerkverbindungen</span><span class="sxs-lookup"><span data-stu-id="200bd-156">Emulate slow network connections</span></span>  

<span data-ttu-id="200bd-157">Emulieren Sie langsames 3G, fast 3G und andere Verbindungsgeschwindigkeiten über das **Online-Dropdown-** Menü.</span><span class="sxs-lookup"><span data-stu-id="200bd-157">Emulate Slow 3G, Fast 3G, and other connection speeds from the **Online** dropdown menu.</span></span>  

:::image type="complex" source="../media/network-network-throttling-menu.msft.png" alt-text="Netzwerk Panel" lightbox="../media/network-network-throttling-menu.msft.png":::
   <span data-ttu-id="200bd-159">Dropdownmenü " **Drosselung** "</span><span class="sxs-lookup"><span data-stu-id="200bd-159">The **Throttling** dropdown menu</span></span>  
:::image-end:::  

<span data-ttu-id="200bd-160">Sie können aus unterschiedlichen Voreinstellungen wie Slow 3G oder fast 3G wählen.</span><span class="sxs-lookup"><span data-stu-id="200bd-160">You may select from different presets, such as Slow 3G or Fast 3G.</span></span>  <span data-ttu-id="200bd-161">Sie können auch eigene benutzerdefinierte Voreinstellungen hinzufügen, indem Sie das Menü Drosselung öffnen und **benutzerdefiniertes**  >  **Add**auswählen.</span><span class="sxs-lookup"><span data-stu-id="200bd-161">You may also add your own custom presets by opening the Throttling menu and selecting **Custom** > **Add**.</span></span>  

<span data-ttu-id="200bd-162">DevTools zeigt ein Warnungssymbol neben der Registerkarte " **Netzwerk** " an, um Sie daran zu erinnern, dass die Drosselung aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="200bd-162">DevTools displays a warning icon next to the **Network** tab to remind you that throttling is enabled.</span></span>  

#### <span data-ttu-id="200bd-163">Emulieren von langsamen Netzwerkverbindungen über die Netzwerkbedingungen Schublade</span><span class="sxs-lookup"><span data-stu-id="200bd-163">Emulate slow network connections from the Network Conditions drawer</span></span>  

<span data-ttu-id="200bd-164">Wenn Sie die Netzwerkverbindung während der Arbeit in anderen devtools-Panels Drosseln möchten, verwenden Sie den Netzwerkbedingungen-Einzug.</span><span class="sxs-lookup"><span data-stu-id="200bd-164">If you want to throttle the network connection while working in other DevTools panels, use the Network Conditions drawer.</span></span>  

1.  <span data-ttu-id="200bd-165">Öffnen Sie die Schublade **Netzwerkbedingungen** .</span><span class="sxs-lookup"><span data-stu-id="200bd-165">Open the **Network Conditions** drawer.</span></span>  
1.  <span data-ttu-id="200bd-166">Wählen Sie im Menü **Drosselung** Ihre Verbindungsgeschwindigkeit aus.</span><span class="sxs-lookup"><span data-stu-id="200bd-166">Select your connection speed from the **Throttling** menu.</span></span>  

<!--todo: add network condition section when available -->  

### <span data-ttu-id="200bd-167">Manuelles Löschen von Browser-Cookies</span><span class="sxs-lookup"><span data-stu-id="200bd-167">Manually clear browser cookies</span></span>  

<span data-ttu-id="200bd-168">Wenn Sie Browser-Cookies jederzeit manuell löschen möchten, öffnen Sie das Kontextmenü \ (Klicken Sie mit der rechten Maustaste auf \) an einer beliebigen Stelle in der Tabelle Anforderungen, und wählen Sie **Browser-Cookies löschen**aus.</span><span class="sxs-lookup"><span data-stu-id="200bd-168">To manually clear browser cookies at any time, open the contextual menu \(right-click\) anywhere in the Requests table and choose **Clear Browser Cookies**.</span></span>  

:::image type="complex" source="../media/network-network-clear-browser-cookies.msft.png" alt-text="Netzwerk Panel" lightbox="../media/network-network-clear-browser-cookies.msft.png":::
   <span data-ttu-id="200bd-170">Auswählen von **Browser-Cookies löschen**</span><span class="sxs-lookup"><span data-stu-id="200bd-170">Selecting **Clear Browser Cookies**</span></span>  
:::image-end:::  

### <span data-ttu-id="200bd-171">Überschreiben des Benutzer-Agents</span><span class="sxs-lookup"><span data-stu-id="200bd-171">Override the user agent</span></span>  

<span data-ttu-id="200bd-172">Führen Sie die folgenden Schritte aus, um den Benutzer-Agent manuell zu überschreiben.</span><span class="sxs-lookup"><span data-stu-id="200bd-172">To manually override the user agent, use the following steps.</span></span>  

1.  <span data-ttu-id="200bd-173">Öffnen Sie die Schublade **Netzwerkbedingungen** .</span><span class="sxs-lookup"><span data-stu-id="200bd-173">Open the **Network Conditions** drawer.</span></span>  
1.  <span data-ttu-id="200bd-174">Deaktivieren **Sie SELECT automatisch**.</span><span class="sxs-lookup"><span data-stu-id="200bd-174">Uncheck **Select automatically**.</span></span>  
1.  <span data-ttu-id="200bd-175">Wählen Sie eine Option für den Benutzer-Agent aus dem Menü aus, oder geben Sie eine benutzerdefinierte Option in das Textfeld ein.</span><span class="sxs-lookup"><span data-stu-id="200bd-175">Choose a user agent option from the menu, or enter a custom one in the text box.</span></span>  

<!--todo: add network condition section when available -->  

## <span data-ttu-id="200bd-176">Filter Anforderungen</span><span class="sxs-lookup"><span data-stu-id="200bd-176">Filter requests</span></span>  

### <span data-ttu-id="200bd-177">Filtern von Anforderungen nach Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="200bd-177">Filter requests by properties</span></span>  

<span data-ttu-id="200bd-178">Verwenden Sie das Textfeld **Filtern** , um Anforderungen nach Eigenschaften wie der Domäne oder der Größe der Anforderung zu filtern.</span><span class="sxs-lookup"><span data-stu-id="200bd-178">Use the **Filter** text box to filter requests by properties, such as the domain or size of the request.</span></span>  

<span data-ttu-id="200bd-179">Wenn das Textfeld nicht angezeigt wird, ist der **Filter** Bereich wahrscheinlich ausgeblendet.</span><span class="sxs-lookup"><span data-stu-id="200bd-179">If the text box is not displayed, the **Filters** pane is probably hidden.</span></span>  
<span data-ttu-id="200bd-180">Wenn Sie weitere Informationen erhalten möchten, navigieren Sie zum [Ausblenden des Filters-Bereichs](#hide-the-filters-pane).</span><span class="sxs-lookup"><span data-stu-id="200bd-180">For more information, navigate to [Hide the Filters pane](#hide-the-filters-pane).</span></span>  

:::image type="complex" source="../media/network-network-filters-textbox.msft.png" alt-text="Netzwerk Panel" lightbox="../media/network-network-filters-textbox.msft.png":::
   <span data-ttu-id="200bd-182">Das Textfeld " **Filter** "</span><span class="sxs-lookup"><span data-stu-id="200bd-182">The **Filter** text box</span></span>  
:::image-end:::  

<span data-ttu-id="200bd-183">Sie können mehrere Eigenschaften gleichzeitig verwenden, indem Sie jede Eigenschaft mit einem Leerzeichen voneinander trennen.</span><span class="sxs-lookup"><span data-stu-id="200bd-183">You may use multiple properties simultaneously by separating each property with a space.</span></span>  <span data-ttu-id="200bd-184">Zeigt beispielsweise `mime-type:image/png larger-than:1K` alle PNGs an, die größer als 1 KB sind.</span><span class="sxs-lookup"><span data-stu-id="200bd-184">For example, `mime-type:image/png larger-than:1K` displays all PNGs that are larger than 1 kilobyte.</span></span>  <span data-ttu-id="200bd-185">Die Filter für mehrere Eigenschaften sind äquivalent zu `AND` Vorgängen.</span><span class="sxs-lookup"><span data-stu-id="200bd-185">The multi-property filters are equivalent to `AND` operations.</span></span>  `OR` <span data-ttu-id="200bd-186">Vorgänge werden zurzeit nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="200bd-186">operations are currently not supported.</span></span>  

<span data-ttu-id="200bd-187">Die vollständige Liste der unterstützten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="200bd-187">The complete list of supported properties.</span></span>  

| <span data-ttu-id="200bd-188">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="200bd-188">Property</span></span> | <span data-ttu-id="200bd-189">Details</span><span class="sxs-lookup"><span data-stu-id="200bd-189">Details</span></span> |  
|:--- | :--- |  
| `domain` | <span data-ttu-id="200bd-190">Zeigt nur Ressourcen aus der angegebenen Domäne an.</span><span class="sxs-lookup"><span data-stu-id="200bd-190">Only display resources from the specified domain.</span></span>  <span data-ttu-id="200bd-191">Sie können ein Platzhalterzeichen \ ( `*` \) verwenden, um mehrere Domänen einzubeziehen.</span><span class="sxs-lookup"><span data-stu-id="200bd-191">You may use a wildcard character \(`*`\) to include multiple domains.</span></span>  <span data-ttu-id="200bd-192">Zeigt beispielsweise `*.com` Ressourcen aus allen Domänennamen an, die in endet `.com` .</span><span class="sxs-lookup"><span data-stu-id="200bd-192">For example, `*.com` displays resources from all domain names ending in `.com`.</span></span>  <span data-ttu-id="200bd-193">DevTools füllen Sie das Dropdownmenü AutoVervollständigen mit allen gefundenen Domänen auf.</span><span class="sxs-lookup"><span data-stu-id="200bd-193">DevTools populate the autocomplete dropdown menu with all of the domains that are found.</span></span> |  
| `has-response-header` | <span data-ttu-id="200bd-194">Zeigt die Ressourcen an, die den angegebenen HTTP-Antwortheader enthalten.</span><span class="sxs-lookup"><span data-stu-id="200bd-194">Displays the resources that contain the specified HTTP response header.</span></span>  <span data-ttu-id="200bd-195">DevTools füllen Sie die Dropdownliste AutoVervollständigen mit allen gefundenen Antwortheadern auf.</span><span class="sxs-lookup"><span data-stu-id="200bd-195">DevTools populate the autocomplete dropdown with all of the response headers that are found.</span></span> |  
| `is` | <span data-ttu-id="200bd-196">Verwendet `is:running` , um `WebSocket` Ressourcen zu finden.</span><span class="sxs-lookup"><span data-stu-id="200bd-196">Use `is:running` to find `WebSocket` resources.</span></span> |  
| `larger-than` | <span data-ttu-id="200bd-197">Zeigt Ressourcen an, die größer als die angegebene Größe in Bytes sind.</span><span class="sxs-lookup"><span data-stu-id="200bd-197">Displays resources that are larger than the specified size, in bytes.</span></span>  <span data-ttu-id="200bd-198">Das Festlegen eines Werts von entspricht dem `1000` Festlegen eines Werts von `1k` .</span><span class="sxs-lookup"><span data-stu-id="200bd-198">Setting a value of `1000` is equivalent to setting a value of `1k`.</span></span> |  
| `method` | <span data-ttu-id="200bd-199">Zeigt Ressourcen an, die über einen angegebenen http-Methodentyp abgerufen wurden.</span><span class="sxs-lookup"><span data-stu-id="200bd-199">Displays resources that were retrieved over a specified HTTP method type.</span></span>  <span data-ttu-id="200bd-200">DevTools füllen Sie die Dropdownliste mit allen gefundenen HTTP-Methoden auf.</span><span class="sxs-lookup"><span data-stu-id="200bd-200">DevTools populate the dropdown with all of the HTTP methods  that are found.</span></span> |  
| `mime-type` | <span data-ttu-id="200bd-201">Zeigt Ressourcen eines angegebenen MIME-Typs an.</span><span class="sxs-lookup"><span data-stu-id="200bd-201">Displays resources of a specified MIME type.</span></span>  <span data-ttu-id="200bd-202">DevTools füllen Sie die Dropdownliste mit allen gefundenen MIME-Typen auf.</span><span class="sxs-lookup"><span data-stu-id="200bd-202">DevTools populate the dropdown with all MIME types  that are found.</span></span> |  
| `mixed-content` | <span data-ttu-id="200bd-203">Alle gemischten Inhalts Ressourcen anzeigen \ ( `mixed-content:all` \) oder nur diejenigen, die aktuell angezeigt werden \ ( `mixed-content:displayed` \).</span><span class="sxs-lookup"><span data-stu-id="200bd-203">Show all mixed content resources \(`mixed-content:all`\) or just the ones that are currently displayed \(`mixed-content:displayed`\).</span></span> |  
| `scheme` | <span data-ttu-id="200bd-204">Zeigt Ressourcen an, die über ungeschützten http \ ( `scheme:http` \) oder geschütztes HTTPS \ ( `scheme:https` \) abgerufen wurden.</span><span class="sxs-lookup"><span data-stu-id="200bd-204">Displays resources retrieved over unprotected HTTP \(`scheme:http`\) or protected HTTPS \(`scheme:https`\).</span></span> |  
| `set-cookie-domain` | <span data-ttu-id="200bd-205">Zeigt Ressourcen `Set-Cookie` mit einer Kopfzeile mit einem `Domain` Attribut an, das dem angegebenen Wert entspricht.</span><span class="sxs-lookup"><span data-stu-id="200bd-205">Displays resources that have a `Set-Cookie` header with a `Domain` attribute that matches the specified value.</span></span>  <span data-ttu-id="200bd-206">DevTools füllen Sie das AutoVervollständigen mit allen gefundenen Cookie-Domänen auf.</span><span class="sxs-lookup"><span data-stu-id="200bd-206">DevTools populate the autocomplete with all of the cookie domains that are found.</span></span> |  
| `set-cookie-name` | <span data-ttu-id="200bd-207">Zeigt Ressourcen `Set-Cookie` mit einer Kopfzeile mit einem Namen an, der dem angegebenen Wert entspricht.</span><span class="sxs-lookup"><span data-stu-id="200bd-207">Displays resources that have a `Set-Cookie` header with a name that matches the specified value.</span></span>  <span data-ttu-id="200bd-208">DevTools füllen Sie die AutoVervollständigen-Datei mit allen gefundenen Cookienamen auf.</span><span class="sxs-lookup"><span data-stu-id="200bd-208">DevTools populate the autocomplete with all of the cookie names that are found.</span></span> |  
| `set-cookie-value` | <span data-ttu-id="200bd-209">Zeigt Ressourcen `Set-Cookie` mit einer Kopfzeile mit einem Wert an, der dem angegebenen Wert entspricht.</span><span class="sxs-lookup"><span data-stu-id="200bd-209">Displays resources that have a `Set-Cookie` header with a value that matches the specified value.</span></span>  <span data-ttu-id="200bd-210">DevTools füllen Sie das AutoVervollständigen mit allen gefundenen Cookie-Werten auf.</span><span class="sxs-lookup"><span data-stu-id="200bd-210">DevTools populate the autocomplete with all of the cookie values that are found.</span></span> |  
| `status-code` | <span data-ttu-id="200bd-211">Zeigt Ressourcen an, die dem spezifischen HTTP-Statuscode entsprechen.</span><span class="sxs-lookup"><span data-stu-id="200bd-211">Displays resources that match the specific HTTP status code.</span></span>  <span data-ttu-id="200bd-212">DevTools füllt das Dropdownmenü AutoVervollständigen mit allen gefundenen Statuscodes auf.</span><span class="sxs-lookup"><span data-stu-id="200bd-212">DevTools populates the autocomplete dropdown menu with all of the status codes that are found.</span></span> |  

### <span data-ttu-id="200bd-213">Filtern von Anforderungen nach Typ</span><span class="sxs-lookup"><span data-stu-id="200bd-213">Filter requests by type</span></span>  

<span data-ttu-id="200bd-214">Wenn Sie Anforderungen nach Anforderungsfiltern möchten, wählen Sie eine der folgenden Schaltflächen im **Netzwerk** Panel aus.</span><span class="sxs-lookup"><span data-stu-id="200bd-214">To filter requests by request type, select the one of the following buttons on the **Network** panel.</span></span>  

:::row:::
   :::column span="1":::
      **<span data-ttu-id="200bd-215">XMLHttpRequest</span><span class="sxs-lookup"><span data-stu-id="200bd-215">XHR</span></span>**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="200bd-216">JS</span><span class="sxs-lookup"><span data-stu-id="200bd-216">JS</span></span>**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="200bd-217">CSS</span><span class="sxs-lookup"><span data-stu-id="200bd-217">CSS</span></span>**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="200bd-218">IMG</span><span class="sxs-lookup"><span data-stu-id="200bd-218">Img</span></span>**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="200bd-219">Media</span><span class="sxs-lookup"><span data-stu-id="200bd-219">Media</span></span>**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="200bd-220">Font</span><span class="sxs-lookup"><span data-stu-id="200bd-220">Font</span></span>**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="200bd-221">Doc</span><span class="sxs-lookup"><span data-stu-id="200bd-221">Doc</span></span>**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="200bd-222">WS</span><span class="sxs-lookup"><span data-stu-id="200bd-222">WS</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="200bd-223">WebSocket.</span><span class="sxs-lookup"><span data-stu-id="200bd-223">WebSocket.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="200bd-224">Manifest</span><span class="sxs-lookup"><span data-stu-id="200bd-224">Manifest</span></span>**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="200bd-225">Other</span><span class="sxs-lookup"><span data-stu-id="200bd-225">Other</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="200bd-226">Jeder andere Typ, der nicht aufgeführt ist.</span><span class="sxs-lookup"><span data-stu-id="200bd-226">Any other type not listed.</span></span>  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="200bd-227">Wenn die Schaltflächen nicht angezeigt werden, ist der Bereich " **Filter** " möglicherweise ausgeblendet.</span><span class="sxs-lookup"><span data-stu-id="200bd-227">If the buttons do not display, the **Filters** pane may be hidden.</span></span>  
<span data-ttu-id="200bd-228">Wenn Sie weitere Informationen erhalten möchten, navigieren Sie zum [Ausblenden des Filters-Bereichs](#hide-the-filters-pane).</span><span class="sxs-lookup"><span data-stu-id="200bd-228">For more information, navigate to [Hide the Filters pane](#hide-the-filters-pane).</span></span>  

<span data-ttu-id="200bd-229">Wenn Sie mehrere Typen Filter gleichzeitig aktivieren möchten, halten `Control` Sie \ (Windows, Linux \) oder `Command` \ (macOS \), und wählen Sie dann aus.</span><span class="sxs-lookup"><span data-stu-id="200bd-229">To enable multiple type filters simultaneously, hold `Control` \(Windows, Linux\) or `Command` \(macOS\) and then select.</span></span>  

:::image type="complex" source="../media/network-network-type-filters.msft.png" alt-text="Netzwerk Panel" lightbox="../media/network-network-type-filters.msft.png":::
   <span data-ttu-id="200bd-231">Verwenden des Typs "Filter" zum Anzeigen von JS-, CSS-und Dokument Ressourcen</span><span class="sxs-lookup"><span data-stu-id="200bd-231">Using the Type filters to display JS, CSS, and Document resources</span></span>  
:::image-end:::  

### <span data-ttu-id="200bd-232">Filtern von Anforderungen nach Zeit</span><span class="sxs-lookup"><span data-stu-id="200bd-232">Filter requests by time</span></span>  

<span data-ttu-id="200bd-233">Wählen Sie aus, und ziehen Sie im Übersichtsbereich nach links oder rechts, um nur Anforderungen anzuzeigen, die während dieses Zeitrahmens aktiv waren.</span><span class="sxs-lookup"><span data-stu-id="200bd-233">Select and drag left or right on the Overview pane to only display requests that were active during that time frame.</span></span>  <span data-ttu-id="200bd-234">Der Filter ist inklusive.</span><span class="sxs-lookup"><span data-stu-id="200bd-234">The filter is inclusive.</span></span>  <span data-ttu-id="200bd-235">Jede Anforderung, die während der hervorgehobenen Zeit aktiv war, wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="200bd-235">Any request that was active during the highlighted time is shown.</span></span>  

:::image type="complex" source="../media/network-network-overview-filter.msft.png" alt-text="Netzwerk Panel" lightbox="../media/network-network-overview-filter.msft.png":::
   <span data-ttu-id="200bd-237">Herausfiltern von Anforderungen, die um 300 ms inaktiv waren</span><span class="sxs-lookup"><span data-stu-id="200bd-237">Filtering out any requests that were inactive around 300 ms</span></span>  
:::image-end:::  

### <span data-ttu-id="200bd-238">Ausblenden von Daten-URLs</span><span class="sxs-lookup"><span data-stu-id="200bd-238">Hide data URLs</span></span>  

<span data-ttu-id="200bd-239">[Daten-URLs][MDNHTTPDataURIs] sind kleine Dateien, die in andere Dokumente eingebettet sind.</span><span class="sxs-lookup"><span data-stu-id="200bd-239">[Data URLs][MDNHTTPDataURIs] are small files embedded into other documents.</span></span>  <span data-ttu-id="200bd-240">Jede Anforderung, die in der Tabelle "Anforderungen" angezeigt wird, beginnt mit `data:` einer Daten-URL.</span><span class="sxs-lookup"><span data-stu-id="200bd-240">Any request that displays in the Requests table that starts with `data:` is a data URL.</span></span>  

<span data-ttu-id="200bd-241">Aktivieren Sie das Kontrollkästchen **Daten-URLs ausblenden** , um die Anforderungen auszublenden.</span><span class="sxs-lookup"><span data-stu-id="200bd-241">Check the **Hide data URLs** checkbox to hide the requests.</span></span>  

:::image type="complex" source="../media/network-network-hide-data-urls.msft.png" alt-text="Netzwerk Panel" lightbox="../media/network-network-hide-data-urls.msft.png":::
   <span data-ttu-id="200bd-243">Das Kontrollkästchen " **Daten-URLs ausblenden** "</span><span class="sxs-lookup"><span data-stu-id="200bd-243">The **Hide Data URLs** checkbox</span></span>  
:::image-end:::  

## <span data-ttu-id="200bd-244">Sortieren von Anforderungen</span><span class="sxs-lookup"><span data-stu-id="200bd-244">Sort requests</span></span>  

<span data-ttu-id="200bd-245">Standardmäßig werden die Anforderungen in der Tabelle Anforderungen nach Initiierungs Zeit sortiert, aber Sie können die Tabelle mit anderen Kriterien sortieren.</span><span class="sxs-lookup"><span data-stu-id="200bd-245">By default, the requests in the Requests table are sorted by initiation time, but you may sort the table using other criteria.</span></span>  

### <span data-ttu-id="200bd-246">Nach Spalte sortieren</span><span class="sxs-lookup"><span data-stu-id="200bd-246">Sort by column</span></span>  

<span data-ttu-id="200bd-247">Wählen Sie die Kopfzeile einer beliebigen Spalte in den Anforderungen aus, um Anforderungen nach dieser Spalte zu sortieren.</span><span class="sxs-lookup"><span data-stu-id="200bd-247">Select the header of any column in the Requests to sort requests by that column.</span></span>  

### <span data-ttu-id="200bd-248">Nach Aktivitätsphase sortieren</span><span class="sxs-lookup"><span data-stu-id="200bd-248">Sort by activity phase</span></span>  

<span data-ttu-id="200bd-249">Wenn Sie ändern möchten, wie der Wasserfall Anforderungen sortiert, zeigen Sie auf die Kopfzeile der Tabelle Anforderungen, öffnen Sie das Kontextmenü \ (Klicken Sie mit der rechten Maustaste auf \), zeigen Sie mit der Maus auf **Wasserfall**, und wählen Sie eine der folgenden Optionen aus.</span><span class="sxs-lookup"><span data-stu-id="200bd-249">To change how the Waterfall sorts requests, hover on the header of the Requests table, open the contextual menu \(right-click\), hover over **Waterfall**, and select one of the following options.</span></span>  

:::row:::
   :::column span="1":::
      **<span data-ttu-id="200bd-250">Startzeit</span><span class="sxs-lookup"><span data-stu-id="200bd-250">Start Time</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="200bd-251">Die erste Anforderung, die initiiert wurde, ist oben.</span><span class="sxs-lookup"><span data-stu-id="200bd-251">The first request that was initiated is at the top.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="200bd-252">Antwortzeit</span><span class="sxs-lookup"><span data-stu-id="200bd-252">Response Time</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="200bd-253">Die erste Anforderung, die den Download begonnen hat, ist ganz oben.</span><span class="sxs-lookup"><span data-stu-id="200bd-253">The first request that started downloading is at the top.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="200bd-254">Endzeit</span><span class="sxs-lookup"><span data-stu-id="200bd-254">End Time</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="200bd-255">Die erste abgeschlossene Anforderung ist oben.</span><span class="sxs-lookup"><span data-stu-id="200bd-255">The first request that finished is at the top.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="200bd-256">Gesamtdauer</span><span class="sxs-lookup"><span data-stu-id="200bd-256">Total Duration</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="200bd-257">Die Anforderung mit den kürzesten Verbindungseinstellungen und der Anforderung oder Antwort ist oben.</span><span class="sxs-lookup"><span data-stu-id="200bd-257">The request with the shortest connection settings and request or response is at the top.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="200bd-258">Latenz</span><span class="sxs-lookup"><span data-stu-id="200bd-258">Latency</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="200bd-259">Die Anforderung, die die kürzeste Zeit für eine Antwort gewartet hat, ist oben.</span><span class="sxs-lookup"><span data-stu-id="200bd-259">The request that waited the shortest time for a response is at the top.</span></span>  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="200bd-260">Bei diesen Beschreibungen wird davon ausgegangen, dass die jeweilige Option von kürzester bis längster Position bewertet wird.</span><span class="sxs-lookup"><span data-stu-id="200bd-260">These descriptions assume that each respective option is ranked from shortest to longest.</span></span>  <span data-ttu-id="200bd-261">Wenn Sie die Kopfzeile der Spalte **Wasserfall** auswählen, wird die Reihenfolge umgekehrt.</span><span class="sxs-lookup"><span data-stu-id="200bd-261">Selecting the header of the **Waterfall** column reverses the order.</span></span>  

:::image type="complex" source="../media/network-network-waterfall-total-duration.msft.png" alt-text="Netzwerk Panel" lightbox="../media/network-network-waterfall-total-duration.msft.png":::
   <span data-ttu-id="200bd-263">Sortieren des Wasserfalls nach Gesamtdauer \ (der leichtere Teil der einzelnen Balken ist die Zeit, die gewartet wird, und der dunklere Teil ist die Zeit, die zum Herunterladen von Bytes verwendet wird \)</span><span class="sxs-lookup"><span data-stu-id="200bd-263">Sorting the Waterfall by total duration  \(The lighter portion of each bar is time spent waiting and the darker portion is time spent downloading bytes\)</span></span>  
:::image-end:::  

## <span data-ttu-id="200bd-264">Analysieren von Anforderungen</span><span class="sxs-lookup"><span data-stu-id="200bd-264">Analyze requests</span></span>  

<span data-ttu-id="200bd-265">Solange devtools geöffnet sind, werden alle Anforderungen im Netzwerk Panel protokolliert.</span><span class="sxs-lookup"><span data-stu-id="200bd-265">So long as DevTools are open, it logs all requests in the Network panel.</span></span>  
<span data-ttu-id="200bd-266">Verwenden Sie das Netzwerk Panel, um Anforderungen zu analysieren.</span><span class="sxs-lookup"><span data-stu-id="200bd-266">Use the Network panel to analyze requests.</span></span>  

### <span data-ttu-id="200bd-267">Anzeigen eines Protokolls der Anforderungen</span><span class="sxs-lookup"><span data-stu-id="200bd-267">View a log of requests</span></span>  

<span data-ttu-id="200bd-268">Verwenden Sie die Tabelle "Anforderungen", um ein Protokoll aller Anforderungen anzuzeigen, die während der devtools geöffnet wurden.</span><span class="sxs-lookup"><span data-stu-id="200bd-268">Use the Requests table to view a log of all requests made while DevTools have been open.</span></span>  <span data-ttu-id="200bd-269">Wenn Sie über Anforderungen auswählen oder darauf zeigen, werden weitere Informationen zu den einzelnen Elementen eingeblendet.</span><span class="sxs-lookup"><span data-stu-id="200bd-269">Selecting or hovering over requests reveals more information about each item.</span></span>  

:::image type="complex" source="../media/network-network-requests-table.msft.png" alt-text="Netzwerk Panel" lightbox="../media/network-network-requests-table.msft.png":::
   <span data-ttu-id="200bd-271">Die Tabelle "Anforderungen"</span><span class="sxs-lookup"><span data-stu-id="200bd-271">The Requests table</span></span>  
:::image-end:::  

<span data-ttu-id="200bd-272">In der Tabelle Anforderungen werden standardmäßig die folgenden Spalten angezeigt.</span><span class="sxs-lookup"><span data-stu-id="200bd-272">The Requests table displays the following columns by default.</span></span>  

:::row:::
   :::column span="1":::
      **<span data-ttu-id="200bd-273">Name</span><span class="sxs-lookup"><span data-stu-id="200bd-273">Name</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="200bd-274">Der Dateiname von oder ein Bezeichner für die Ressource.</span><span class="sxs-lookup"><span data-stu-id="200bd-274">The filename of, or an identifier for, the resource.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="200bd-275">Status</span><span class="sxs-lookup"><span data-stu-id="200bd-275">Status</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="200bd-276">Der HTTP-Statuscode.</span><span class="sxs-lookup"><span data-stu-id="200bd-276">The HTTP status code.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="200bd-277">Typ</span><span class="sxs-lookup"><span data-stu-id="200bd-277">Type</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="200bd-278">Der MIME-Typ der angeforderten Ressource.</span><span class="sxs-lookup"><span data-stu-id="200bd-278">The MIME type of the requested resource.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="200bd-279">Initiator</span><span class="sxs-lookup"><span data-stu-id="200bd-279">Initiator</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="200bd-280">Die folgenden Objekte oder Prozesse initiieren Anforderungen.</span><span class="sxs-lookup"><span data-stu-id="200bd-280">The following objects or processes initiate requests.</span></span>  
      
      *   <span data-ttu-id="200bd-281">**Parser**  Der HTML-Parser für Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="200bd-281">**Parser**  The HTML parser for Microsoft Edge.</span></span>  
      *   <span data-ttu-id="200bd-282">**Umleitung**  Eine HTTP-Umleitung.</span><span class="sxs-lookup"><span data-stu-id="200bd-282">**Redirect**  An HTTP redirect.</span></span>  
      *   <span data-ttu-id="200bd-283">**Skript**  Eine JavaScript-Funktion.</span><span class="sxs-lookup"><span data-stu-id="200bd-283">**Script**  A JavaScript function.</span></span>  
      *   <span data-ttu-id="200bd-284">**Andere**  Personen  Einige andere Prozesse oder Aktionen, wie das Navigieren zu einer Seite mithilfe eines Links oder das Eingeben einer URL in der Adressleiste.</span><span class="sxs-lookup"><span data-stu-id="200bd-284">**Other**  Some other process or action, such as navigating to a page using a link or entering a URL in the address bar.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="200bd-285">Size</span><span class="sxs-lookup"><span data-stu-id="200bd-285">Size</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="200bd-286">Die kombinierte Größe der Antwortheader sowie des Antworttexts, wie vom Server bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="200bd-286">The combined size of the response headers plus the response body, as delivered by the server.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="200bd-287">Zeit</span><span class="sxs-lookup"><span data-stu-id="200bd-287">Time</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="200bd-288">Die Gesamtdauer vom Anfang der Anforderung bis zum Empfang des letzten Bytes in der Antwort.</span><span class="sxs-lookup"><span data-stu-id="200bd-288">The total duration, from the start of the request to the receipt of the final byte in the response.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [<span data-ttu-id="200bd-289">Wasserfall</span><span class="sxs-lookup"><span data-stu-id="200bd-289">Waterfall</span></span>](#view-the-timing-relationship-of-requests)  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="200bd-290">Eine visuelle Gliederung der Aktivität für jede Anforderung.</span><span class="sxs-lookup"><span data-stu-id="200bd-290">A visual breakdown of the activity for each request.</span></span>  
   :::column-end:::
:::row-end:::  

#### <span data-ttu-id="200bd-291">Hinzufügen oder Entfernen von Spalten</span><span class="sxs-lookup"><span data-stu-id="200bd-291">Add or remove columns</span></span>  

<span data-ttu-id="200bd-292">Zeigen Sie auf die Kopfzeile der Tabelle Anforderungen, öffnen Sie das Kontextmenü \ (Klicken Sie mit der rechten Maustaste auf \), und wählen Sie eine Option aus, um sie auszublenden oder anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="200bd-292">Hover on the header of the Requests table, open the contextual menu \(right-click\), and select an option to hide or show it.</span></span>  <span data-ttu-id="200bd-293">Die aktuell angezeigten Optionen verfügen über Kontrollkästchen neben den einzelnen Elementen.</span><span class="sxs-lookup"><span data-stu-id="200bd-293">Currently displayed options have checkmarks next to each item.</span></span>  

:::image type="complex" source="../media/network-network-requests-add-column.msft.png" alt-text="Netzwerk Panel" lightbox="../media/network-network-requests-add-column.msft.png":::
   <span data-ttu-id="200bd-295">Hinzufügen einer Spalte zur Tabelle "Anforderungen"</span><span class="sxs-lookup"><span data-stu-id="200bd-295">Adding a column to the Requests table</span></span>  
:::image-end:::  

#### <span data-ttu-id="200bd-296">Hinzufügen benutzerdefinierter Spalten</span><span class="sxs-lookup"><span data-stu-id="200bd-296">Add custom columns</span></span>  

<span data-ttu-id="200bd-297">Wenn Sie der Tabelle Anforderungen eine benutzerdefinierte Spalte hinzufügen möchten, zeigen Sie auf die Kopfzeile der Tabelle Anforderungen, öffnen Sie das Kontextmenü \ (Klicken Sie mit der rechten Maustaste auf \), und wählen Sie **Antwortheader**  >  **Verwalten von Kopfzeilen Spalten**aus.</span><span class="sxs-lookup"><span data-stu-id="200bd-297">To add a custom column to the Requests table, hover on the header of the Requests table, open the contextual menu \(right-click\), and choose **Response Headers** > **Manage Header Columns**.</span></span>  

:::image type="complex" source="../media/network-network-requests-add-custom.msft.png" alt-text="Netzwerk Panel" lightbox="../media/network-network-requests-add-custom.msft.png":::
   <span data-ttu-id="200bd-299">Hinzufügen einer benutzerdefinierten Spalte zur Tabelle "Anforderungen"</span><span class="sxs-lookup"><span data-stu-id="200bd-299">Adding a custom column to the Requests table</span></span>  
:::image-end:::  

### <span data-ttu-id="200bd-300">Anzeigen der Zeit Steuerungsbeziehung von Anforderungen</span><span class="sxs-lookup"><span data-stu-id="200bd-300">View the timing relationship of requests</span></span>  

<span data-ttu-id="200bd-301">Verwenden Sie den Wasserfall, um die Timing-Beziehungen von Anforderungen anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="200bd-301">Use the Waterfall to view the timing relationships of requests.</span></span>  
<span data-ttu-id="200bd-302">Die Standardorganisation des Wasserfalls verwendet die Startzeit der Anforderungen.</span><span class="sxs-lookup"><span data-stu-id="200bd-302">The default organization of the Waterfall uses the start time of the requests.</span></span>  
<span data-ttu-id="200bd-303">Anforderungen, die weiter Links sind, wurden früher als die Anforderungen weiter rechts gestartet.</span><span class="sxs-lookup"><span data-stu-id="200bd-303">So, requests that are farther to the left started earlier than the requests that are farther to the right.</span></span>  

<span data-ttu-id="200bd-304">Wenn Sie die verschiedenen Möglichkeiten zum Sortieren des Wasserfalls überprüfen möchten, navigieren Sie zu nach [Aktivitätsphase sortieren](#sort-by-activity-phase).</span><span class="sxs-lookup"><span data-stu-id="200bd-304">To review the different ways that you may sort the Waterfall, navigate to [Sort by activity phase](#sort-by-activity-phase).</span></span>  

:::image type="complex" source="../media/network-network-requests-waterfall.msft.png" alt-text="Netzwerk Panel" lightbox="../media/network-network-requests-waterfall.msft.png":::
   <span data-ttu-id="200bd-306">Spalte "Wasserfall" im Bereich " **Anforderungen** "</span><span class="sxs-lookup"><span data-stu-id="200bd-306">The Waterfall column of the **Requests** pane</span></span>  
:::image-end:::  

<!-- ### Analyze the frames of a WebSocket Connection  -->

<!--To view the frames of a WebSocket connection, use the following steps.  

1.  Select the URL of the WebSocket connection, under the **Name** column of the Requests table.  
1.  Select the **Frames** tab.  The table shows the last 100 frames.  

To refresh the table, re-select the name of the WebSocket connection under the **Name** column of the Requests table.  -->

<!--
:::image type="complex" source="../media/network-frames.msft.png" alt-text="Netzwerk Panel" lightbox="../media/network-frames.msft.png":::
   The **Frames** tab  
:::image-end:::  
-->

<!--The table contains the following three columns.  

*   **Data**.  The message payload.  If the message is plain text, it is displayed here.  For binary opcodes, this column displays the name and code of the opcode.  The following opcodes are supported: Continuation Frame, Binary Frame, Connection Close Frame, Ping Frame, and Pong Frame.  
*   **Length**.  The length of the message payload, in bytes.  
*   **Time**.  The time when the message was received or sent.  -->

<!--Messages are color-coded according to each type.  

*   Outgoing text messages are light-green.  
*   Incoming text messages are white.  
*   WebSocket opcodes are light-yellow.  
*   Errors are light-red.  -->

### <span data-ttu-id="200bd-307">Anzeigen einer Vorschau eines Antworttexts</span><span class="sxs-lookup"><span data-stu-id="200bd-307">View a preview of a response body</span></span>  

<span data-ttu-id="200bd-308">Führen Sie die folgenden Schritte aus, um eine Vorschau eines Antworttexts anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="200bd-308">To view a preview of a response body, use the following steps.</span></span>  

1.  <span data-ttu-id="200bd-309">Wählen Sie die URL der Anforderung unter der Spalte **Name** der Tabelle Anforderungen aus.</span><span class="sxs-lookup"><span data-stu-id="200bd-309">Select the URL of the request, under the **Name** column of the Requests table.</span></span>  
1.  <span data-ttu-id="200bd-310">Wählen Sie die Registerkarte **Vorschau** aus.</span><span class="sxs-lookup"><span data-stu-id="200bd-310">Select the **Preview** tab.</span></span>  

<span data-ttu-id="200bd-311">Diese Registerkarte ist hauptsächlich für die Anzeige von Bildern hilfreich.</span><span class="sxs-lookup"><span data-stu-id="200bd-311">This tab is mostly useful for viewing images.</span></span>  

:::image type="complex" source="../media/network-network-resources-preview.msft.png" alt-text="Netzwerk Panel" lightbox="../media/network-network-resources-preview.msft.png":::
   <span data-ttu-id="200bd-313">Registerkarte " **Vorschau** "</span><span class="sxs-lookup"><span data-stu-id="200bd-313">The **Preview** tab</span></span>  
:::image-end:::  

### <span data-ttu-id="200bd-314">Anzeigen eines Antworttexts</span><span class="sxs-lookup"><span data-stu-id="200bd-314">View a response body</span></span>  

<span data-ttu-id="200bd-315">Führen Sie die folgenden Schritte aus, um den Antworttext für eine Anforderung anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="200bd-315">To view the response body to a request, use the following steps.</span></span>  

1.  <span data-ttu-id="200bd-316">Wählen Sie die URL der Anforderung unter der Spalte **Name** der Tabelle Anforderungen aus.</span><span class="sxs-lookup"><span data-stu-id="200bd-316">Select the URL of the request, under the **Name** column of the Requests table.</span></span>  
1.  <span data-ttu-id="200bd-317">Wählen Sie die Registerkarte **Antwort** aus.</span><span class="sxs-lookup"><span data-stu-id="200bd-317">Select the **Response** tab.</span></span>  

:::image type="complex" source="../media/network-network-resources-response.msft.png" alt-text="Netzwerk Panel" lightbox="../media/network-network-resources-response.msft.png":::
   <span data-ttu-id="200bd-319">Die Registerkarte " **Antwort** "</span><span class="sxs-lookup"><span data-stu-id="200bd-319">The **Response** tab</span></span>  
:::image-end:::  

### <span data-ttu-id="200bd-320">Anzeigen von HTTP-Headern</span><span class="sxs-lookup"><span data-stu-id="200bd-320">View HTTP headers</span></span>  

<span data-ttu-id="200bd-321">Führen Sie die folgenden Schritte aus, um die HTTP-Header Daten zu einer Anforderung anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="200bd-321">To view HTTP header data about a request, use the following steps.</span></span>  

1.  <span data-ttu-id="200bd-322">Wählen Sie die URL der Anforderung unter der Spalte **Name** der Tabelle Anforderungen aus.</span><span class="sxs-lookup"><span data-stu-id="200bd-322">Select the URL of the request, under the **Name** column of the Requests table.</span></span>  
1.  <span data-ttu-id="200bd-323">Wählen Sie die Registerkarte über **Schriften** aus.</span><span class="sxs-lookup"><span data-stu-id="200bd-323">Select the **Headers** tab.</span></span>  

:::image type="complex" source="../media/network-resources-headers.msft.png" alt-text="Netzwerk Panel" lightbox="../media/network-resources-headers.msft.png":::
   <span data-ttu-id="200bd-325">Die Registerkarte "über **Schriften** "</span><span class="sxs-lookup"><span data-stu-id="200bd-325">The **Headers** tab</span></span>  
:::image-end:::  

#### <span data-ttu-id="200bd-326">Anzeigen der HTTP-Header Quelle</span><span class="sxs-lookup"><span data-stu-id="200bd-326">View HTTP header source</span></span>  

<span data-ttu-id="200bd-327">Standardmäßig werden auf der Registerkarte Kopfzeilennamen in alphabetischer Reihenfolge angezeigt.</span><span class="sxs-lookup"><span data-stu-id="200bd-327">By default, the Headers tab shows header names alphabetically.</span></span>  <span data-ttu-id="200bd-328">Führen Sie die folgenden Schritte aus, um die HTTP-Headernamen in der eingegangenen Reihenfolge anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="200bd-328">To view the HTTP header names in the order received, use the following steps.</span></span>  

1.  <span data-ttu-id="200bd-329">Öffnen Sie die Registerkarte über **Schriften** für die Anforderung, die Sie interessiert.</span><span class="sxs-lookup"><span data-stu-id="200bd-329">Open the **Headers** tab for the request that interests you.</span></span>  <span data-ttu-id="200bd-330">Weitere Informationen finden Sie unter [Anzeigen von HTTP-Kopfzeilen](#view-http-headers).</span><span class="sxs-lookup"><span data-stu-id="200bd-330">For more information, navigate to [View HTTP headers](#view-http-headers).</span></span>  
1.  <span data-ttu-id="200bd-331">Wählen Sie **Quelle anzeigen**neben dem Abschnitt **Anforderungs Kopfzeile** oder **Antwort Kopf** aus.</span><span class="sxs-lookup"><span data-stu-id="200bd-331">Choose **view source**, next to the **Request Header** or **Response Header** section.</span></span>  

### <span data-ttu-id="200bd-332">Anzeigen von Abfragezeichenfolgenparametern</span><span class="sxs-lookup"><span data-stu-id="200bd-332">View query string parameters</span></span>  

<span data-ttu-id="200bd-333">Führen Sie die folgenden Schritte aus, um die Abfragezeichenfolgenparameter einer URL in einem menschlich lesbaren Format anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="200bd-333">To view the query string parameters of a URL in a human-readable format, use the following steps.</span></span>  

1.  <span data-ttu-id="200bd-334">Öffnen Sie die Registerkarte über **Schriften** für die Anforderung, die Sie interessiert.</span><span class="sxs-lookup"><span data-stu-id="200bd-334">Open the **Headers** tab for the request that interests you.</span></span>  <span data-ttu-id="200bd-335">Weitere Informationen finden Sie unter [Anzeigen von HTTP-Kopfzeilen](#view-http-headers).</span><span class="sxs-lookup"><span data-stu-id="200bd-335">For more information, navigate to [View HTTP headers](#view-http-headers).</span></span>  
1.  <span data-ttu-id="200bd-336">Wechseln Sie zum Abschnitt **Abfragezeichenfolgenparameter** .</span><span class="sxs-lookup"><span data-stu-id="200bd-336">Go to the **Query String Parameters** section.</span></span>  

:::image type="complex" source="../media/network-network-resources-headers-query-string-parameters.msft.png" alt-text="Netzwerk Panel" lightbox="../media/network-network-resources-headers-query-string-parameters.msft.png":::
   <span data-ttu-id="200bd-338">Der **Abfragezeichenfolgenparameter** Abschnitt</span><span class="sxs-lookup"><span data-stu-id="200bd-338">The **Query String Parameters** section</span></span>  
:::image-end:::  

#### <span data-ttu-id="200bd-339">Anzeigen der Parameterquelle für Abfragezeichenfolgen</span><span class="sxs-lookup"><span data-stu-id="200bd-339">View query string parameters source</span></span>  

<span data-ttu-id="200bd-340">Führen Sie die folgenden Schritte aus, um die Abfragezeichenfolgenparameter Quelle einer Anforderung anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="200bd-340">To view the query string parameter source of a request, use the following steps.</span></span>  

1.  <span data-ttu-id="200bd-341">Wechseln Sie zum Abschnitt Abfragezeichenfolgenparameter.</span><span class="sxs-lookup"><span data-stu-id="200bd-341">Go to the Query String Parameters section.</span></span>  <span data-ttu-id="200bd-342">Weitere Informationen finden Sie unter [Anzeigen von Abfragezeichenfolgenparametern](#view-query-string-parameters).</span><span class="sxs-lookup"><span data-stu-id="200bd-342">For more information, navigate to [View query string parameters](#view-query-string-parameters).</span></span>  
1.  <span data-ttu-id="200bd-343">Wählen Sie **Quelltext anzeigen**aus.</span><span class="sxs-lookup"><span data-stu-id="200bd-343">Choose **view source**.</span></span>  

#### <span data-ttu-id="200bd-344">Anzeigen von URL-codierten Abfragezeichenfolgenparametern</span><span class="sxs-lookup"><span data-stu-id="200bd-344">View URL-encoded query string parameters</span></span>  

<span data-ttu-id="200bd-345">Führen Sie die folgenden Schritte aus, um Abfragezeichenfolgenparameter in einem menschlich lesbaren Format anzuzeigen, jedoch mit erhaltenen Codierungen.</span><span class="sxs-lookup"><span data-stu-id="200bd-345">To view query string parameters in a human-readable format, but with encodings preserved, use the following steps.</span></span>  

1.  <span data-ttu-id="200bd-346">Wechseln Sie zum Abschnitt Abfragezeichenfolgenparameter.</span><span class="sxs-lookup"><span data-stu-id="200bd-346">Go to the Query String Parameters section.</span></span>  <span data-ttu-id="200bd-347">Weitere Informationen finden Sie unter [Anzeigen von Abfragezeichenfolgenparametern](#view-query-string-parameters).</span><span class="sxs-lookup"><span data-stu-id="200bd-347">For more information, navigate to [View query string parameters](#view-query-string-parameters).</span></span>  
1.  <span data-ttu-id="200bd-348">Wählen Sie **View URL encoded**aus.</span><span class="sxs-lookup"><span data-stu-id="200bd-348">Choose **view URL encoded**.</span></span>  

### <span data-ttu-id="200bd-349">Cookies anzeigen</span><span class="sxs-lookup"><span data-stu-id="200bd-349">View cookies</span></span>  

<span data-ttu-id="200bd-350">Führen Sie die folgenden Schritte aus, um die im HTTP-Header einer Anforderung gesendeten Cookies anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="200bd-350">To view the cookies sent in the HTTP header of a request, use the following steps.</span></span>  

1.  <span data-ttu-id="200bd-351">Wählen Sie die URL der Anforderung unter der Spalte **Name** der Tabelle Anforderungen aus.</span><span class="sxs-lookup"><span data-stu-id="200bd-351">Select the URL of the request, under the **Name** column of the Requests table.</span></span>  
1.  <span data-ttu-id="200bd-352">Wählen Sie die Registerkarte **Cookies** aus.</span><span class="sxs-lookup"><span data-stu-id="200bd-352">Select the **Cookies** tab.</span></span>  

<!--For more information about each of the columns, navigate to [Fields][ManageDataCookiesFields].  -->  

<!--[ManageDataCookiesFields]: manage-data/cookies#fields  -->  
<!--TODO: add link when section is available -->  

:::image type="complex" source="../media/network-network-resources-cookies.msft.png" alt-text="Netzwerk Panel" lightbox="../media/network-network-resources-cookies.msft.png":::
   <span data-ttu-id="200bd-354">Die Registerkarte "Cookies"</span><span class="sxs-lookup"><span data-stu-id="200bd-354">The Cookies tab</span></span>  
:::image-end:::  

### <span data-ttu-id="200bd-355">Anzeigen der Zeit Plan Aufteilung einer Anforderung</span><span class="sxs-lookup"><span data-stu-id="200bd-355">View the timing breakdown of a request</span></span>  

<span data-ttu-id="200bd-356">Führen Sie die folgenden Schritte aus, um die Anzeigedauer einer Anforderung anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="200bd-356">To view the timing breakdown of a request, use the following steps.</span></span>  

1.  <span data-ttu-id="200bd-357">Wählen Sie die URL der Anforderung unter der Spalte **Name** der Tabelle Anforderungen aus.</span><span class="sxs-lookup"><span data-stu-id="200bd-357">Select the URL of the request, under the **Name** column of the Requests table.</span></span>  
1.  <span data-ttu-id="200bd-358">Wählen Sie die Registerkarte **Anzeige** Dauer aus.</span><span class="sxs-lookup"><span data-stu-id="200bd-358">Select the **Timing** tab.</span></span>  

<span data-ttu-id="200bd-359">Um eine schnellere Möglichkeit für den Zugriff auf die Daten zu erhalten, navigieren Sie zu [Vorschau einer Anzeige](#preview-a-timing-breakdown)Dauer.</span><span class="sxs-lookup"><span data-stu-id="200bd-359">For a faster way to access the data, navigate to [Preview a timing breakdown](#preview-a-timing-breakdown).</span></span>  

<span data-ttu-id="200bd-360">Weitere Informationen zu den einzelnen Phasen, die möglicherweise auf der Registerkarte **Anzeige** Dauer angezeigt werden, finden Sie unter [erläuterte](#timing-breakdown-phases-explained)Phasen der Anzeigedauer.</span><span class="sxs-lookup"><span data-stu-id="200bd-360">For more information about each of the phases that may be displayed in the **Timing** tab, navigate to [Timing breakdown phases explained](#timing-breakdown-phases-explained).</span></span>  

:::image type="complex" source="../media/network-network-resources-timing.msft.png" alt-text="Netzwerk Panel" lightbox="../media/network-network-resources-timing.msft.png":::
   <span data-ttu-id="200bd-362">Registerkarte " **Anzeige** Dauer"</span><span class="sxs-lookup"><span data-stu-id="200bd-362">The **Timing** tab</span></span>  
:::image-end:::  

<span data-ttu-id="200bd-363">Weitere Informationen zu den einzelnen Phasen.</span><span class="sxs-lookup"><span data-stu-id="200bd-363">More information about each of the phases.</span></span>  

<span data-ttu-id="200bd-364">Weitere Informationen zum Zugriff auf die Ansicht finden Sie unter [Aufschlüsselung](#view-the-timing-breakdown-of-a-request)der Anzeigedauer.</span><span class="sxs-lookup"><span data-stu-id="200bd-364">For more information about accessing the view, navigate to [View timing breakdown](#view-the-timing-breakdown-of-a-request).</span></span>  

#### <span data-ttu-id="200bd-365">Anzeigen einer Vorschau einer Anzeigedauer</span><span class="sxs-lookup"><span data-stu-id="200bd-365">Preview a timing breakdown</span></span>  

<span data-ttu-id="200bd-366">Wenn Sie eine Vorschau der Zeit Plan Aufteilung einer Anforderung anzeigen möchten, zeigen Sie in der Spalte **Wasserfall** der Tabelle Anforderungen auf den Eintrag für die Anforderung.</span><span class="sxs-lookup"><span data-stu-id="200bd-366">To view a preview of the timing breakdown of a request, in the **Waterfall** column of the Requests table, hover on the entry for the request.</span></span>  

<span data-ttu-id="200bd-367">Weitere Informationen dazu, wie Sie auf die Daten zugreifen können, ohne zu schweben, finden Sie unter [Anzeigen der Anzeigedauer einer Anforderung](#view-the-timing-breakdown-of-a-request).</span><span class="sxs-lookup"><span data-stu-id="200bd-367">For more information about how to access the data without hovering, navigate to [View the timing breakdown of a request](#view-the-timing-breakdown-of-a-request).</span></span>  

:::image type="complex" source="../media/network-network-resources-waterfall-hover.msft.png" alt-text="Netzwerk Panel" lightbox="../media/network-network-resources-waterfall-hover.msft.png":::
   <span data-ttu-id="200bd-369">Anzeigen einer Vorschau der Anzeigedauer einer Anforderung</span><span class="sxs-lookup"><span data-stu-id="200bd-369">Previewing the timing breakdown of a request</span></span>  
:::image-end:::  

#### <span data-ttu-id="200bd-370">Erläuterte Phasen Aufgliederungs Phasen</span><span class="sxs-lookup"><span data-stu-id="200bd-370">Timing breakdown phases explained</span></span>  

<span data-ttu-id="200bd-371">Weitere Informationen zu den einzelnen Phasen **, die auf der Registerkarte** Anzeigedauer angezeigt werden können.</span><span class="sxs-lookup"><span data-stu-id="200bd-371">More information about each of the phases that may display in the **Timing** tab.</span></span>  

:::row:::
   :::column span="1":::
      **<span data-ttu-id="200bd-372">Queueing</span><span class="sxs-lookup"><span data-stu-id="200bd-372">Queueing</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="200bd-373">Der Browser Warteschlangenanforderungen, wenn eine der folgenden Bedingungen erfüllt ist.</span><span class="sxs-lookup"><span data-stu-id="200bd-373">The browser queues requests when any of the following are true.</span></span>  
      *   <span data-ttu-id="200bd-374">Anforderungen mit höherer Priorität bestehen.</span><span class="sxs-lookup"><span data-stu-id="200bd-374">Higher priority requests exist.</span></span>  
      *   <span data-ttu-id="200bd-375">Sechs TCP-Verbindungen sind für denselben Ursprung geöffnet, was die Grenze ist.</span><span class="sxs-lookup"><span data-stu-id="200bd-375">Six TCP connections are open for the same origin, which is the limit.</span></span>  <span data-ttu-id="200bd-376">Gilt nur für HTTP/1.0 und HTTP/1.1.</span><span class="sxs-lookup"><span data-stu-id="200bd-376">Applies to HTTP/1.0 and HTTP/1.1 only.</span></span>  
      *   <span data-ttu-id="200bd-377">Der Browser reserviert kurzzeitig Speicherplatz im Datenträgercache.</span><span class="sxs-lookup"><span data-stu-id="200bd-377">The browser is briefly allocating space in the disk cache.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="200bd-378">Blockiert</span><span class="sxs-lookup"><span data-stu-id="200bd-378">Stalled</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="200bd-379">Die Anforderung wird aus den in der **Warteschlange**beschriebenen Gründen angehalten.</span><span class="sxs-lookup"><span data-stu-id="200bd-379">The request is stalled for any of the reasons described in **Queueing**.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="200bd-380">DNS-Lookup</span><span class="sxs-lookup"><span data-stu-id="200bd-380">DNS Lookup</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="200bd-381">Der Browser löst die IP-Adresse für die Anforderung auf.</span><span class="sxs-lookup"><span data-stu-id="200bd-381">The browser is resolving the IP address for the request.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="200bd-382">Anfängliche Verbindung</span><span class="sxs-lookup"><span data-stu-id="200bd-382">Initial connection</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="200bd-383">Der Browser stellt eine Verbindung her, einschließlich TCP-Handshakes, TCP-Wiederholungen und verhandelt eine sichere Socketebene.</span><span class="sxs-lookup"><span data-stu-id="200bd-383">The browser establishes a connection including TCP handshakes, TCP retries, and negotiates a Secure Socket Layer.</span></span>
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="200bd-384">Proxy Verhandlung</span><span class="sxs-lookup"><span data-stu-id="200bd-384">Proxy negotiation</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="200bd-385">Der Browser verhandelt die Anforderung mit einem [Proxy Server][WikiProxyServer].</span><span class="sxs-lookup"><span data-stu-id="200bd-385">The browser is negotiating the request with a [proxy server][WikiProxyServer].</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="200bd-386">Anfrage gesendet</span><span class="sxs-lookup"><span data-stu-id="200bd-386">Request sent</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="200bd-387">Die Anfrage wird gesendet.</span><span class="sxs-lookup"><span data-stu-id="200bd-387">The request is being sent.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="200bd-388">ServiceWorker-Vorbereitung</span><span class="sxs-lookup"><span data-stu-id="200bd-388">ServiceWorker Preparation</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="200bd-389">Der Browser startet den Dienstmitarbeiter.</span><span class="sxs-lookup"><span data-stu-id="200bd-389">The browser is starting the service worker.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="200bd-390">Anforderung an ServiceWorker</span><span class="sxs-lookup"><span data-stu-id="200bd-390">Request to ServiceWorker</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="200bd-391">Die Anforderung wird an den Dienstmitarbeiter gesendet.</span><span class="sxs-lookup"><span data-stu-id="200bd-391">The request is being sent to the service worker.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="200bd-392">Waiting \ (TTFB \)</span><span class="sxs-lookup"><span data-stu-id="200bd-392">Waiting \(TTFB\)</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="200bd-393">Der Browser wartet auf das erste Byte einer Antwort.</span><span class="sxs-lookup"><span data-stu-id="200bd-393">The browser is waiting for the first byte of a response.</span></span>  <span data-ttu-id="200bd-394">TTFB steht für Time to First Byte.</span><span class="sxs-lookup"><span data-stu-id="200bd-394">TTFB stands for Time To First Byte.</span></span>  <span data-ttu-id="200bd-395">Dieser Zeitpunkt umfasst eine Roundtrip-Wartezeit und die Zeitdauer, die der Server zum Vorbereiten der Antwort benötigte.</span><span class="sxs-lookup"><span data-stu-id="200bd-395">This timing includes one round trip of latency and the time the server took to prepare the response.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="200bd-396">Herunterladen von Inhalten</span><span class="sxs-lookup"><span data-stu-id="200bd-396">Content Download</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="200bd-397">Der Browser empfängt die Antwort.</span><span class="sxs-lookup"><span data-stu-id="200bd-397">The browser is receiving the response.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="200bd-398">Empfangen von Push</span><span class="sxs-lookup"><span data-stu-id="200bd-398">Receiving Push</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="200bd-399">Der Browser empfängt Daten für diese Antwort über http/2 Server Push.</span><span class="sxs-lookup"><span data-stu-id="200bd-399">The browser is receiving data for this response via HTTP/2 Server Push.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="200bd-400">Lese Push</span><span class="sxs-lookup"><span data-stu-id="200bd-400">Reading Push</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="200bd-401">Der Browser liest die zuvor empfangenen lokalen Daten.</span><span class="sxs-lookup"><span data-stu-id="200bd-401">The browser is reading the local data previously received.</span></span>  
   :::column-end:::
:::row-end:::  

### <span data-ttu-id="200bd-402">Anzeigen von Initiatoren und Abhängigkeiten</span><span class="sxs-lookup"><span data-stu-id="200bd-402">View initiators and dependencies</span></span>  

<span data-ttu-id="200bd-403">Wenn Sie die Initiatoren und Abhängigkeiten einer Anforderung anzeigen möchten, halten Sie `Shift` die Anforderung in der Tabelle Anforderungen gedrückt, und zeigen Sie darauf.</span><span class="sxs-lookup"><span data-stu-id="200bd-403">To view the initiators and dependencies of a request, hold `Shift`and hover over the request in the Requests table.</span></span>  <span data-ttu-id="200bd-404">DevTools Farben: Initiatoren werden in grün angezeigt, und Abhängigkeiten werden in rot angezeigt.</span><span class="sxs-lookup"><span data-stu-id="200bd-404">DevTools colors: initiators are shown in green and dependencies are shown in red.</span></span>  

:::image type="complex" source="../media/network-network-resources-initiators-dependencies.msft.png" alt-text="Netzwerk Panel" lightbox="../media/network-network-resources-initiators-dependencies.msft.png":::
   <span data-ttu-id="200bd-406">Anzeigen der Initiatoren und Abhängigkeiten einer Anforderung</span><span class="sxs-lookup"><span data-stu-id="200bd-406">Viewing the initiators and dependencies of a request</span></span>  
:::image-end:::  

<span data-ttu-id="200bd-407">Wenn die Anforderungstabelle chronologisch geordnet ist, wenn Sie auf eine Zeile zeigen, wird in der davor liegenden Zeile eine grüne Anforderung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="200bd-407">When the Requests table is ordered chronologically, if you hover on a line, the line preceding it displays a green request.</span></span>  <span data-ttu-id="200bd-408">Die grüne Anforderung ist der Initiator der Abhängigkeit.</span><span class="sxs-lookup"><span data-stu-id="200bd-408">The green request is the initiator of the dependency.</span></span>  <span data-ttu-id="200bd-409">Wenn zuvor eine andere grüne Anforderung in der Zeile angezeigt wird, ist diese höhere Anforderung der Initiator des Initiators.</span><span class="sxs-lookup"><span data-stu-id="200bd-409">If another green request is displayed on the line before that, that higher request is the initiator of the initiator.</span></span>  <span data-ttu-id="200bd-410">Und so weiter.</span><span class="sxs-lookup"><span data-stu-id="200bd-410">And so on.</span></span>  

### <span data-ttu-id="200bd-411">Laden Ereignisse anzeigen</span><span class="sxs-lookup"><span data-stu-id="200bd-411">View load events</span></span>  

<span data-ttu-id="200bd-412">DevTools zeigt die Anzeigedauer der `DOMContentLoaded` `load` Ereignisse und Ereignisse an mehreren Stellen im Netzwerk Panel an.</span><span class="sxs-lookup"><span data-stu-id="200bd-412">DevTools displays the timing of the `DOMContentLoaded` and `load` events in multiple places on the Network panel.</span></span>  <span data-ttu-id="200bd-413">Das `DOMContentLoaded` Ereignis ist blau gefärbt, und das `load` Ereignis ist rot.</span><span class="sxs-lookup"><span data-stu-id="200bd-413">The `DOMContentLoaded` event is colored blue, and the `load` event is red.</span></span>  

:::image type="complex" source="../media/network-network-requests-load-events.msft.png" alt-text="Netzwerk Panel" lightbox="../media/network-network-requests-load-events.msft.png":::
   <span data-ttu-id="200bd-415">Die Speicherorte der `DOMContentLoaded` und- `load` Ereignisse im Netzwerk Panel</span><span class="sxs-lookup"><span data-stu-id="200bd-415">The locations of the `DOMContentLoaded` and `load` events on the Network panel</span></span>  
:::image-end:::  

### <span data-ttu-id="200bd-416">Anzeigen der Gesamtzahl der Anforderungen</span><span class="sxs-lookup"><span data-stu-id="200bd-416">View the total number of requests</span></span>  

<span data-ttu-id="200bd-417">Die Gesamtzahl der Anforderungen wird im Bereich "Zusammenfassung" unten im Netzwerkbereich aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="200bd-417">The total number of requests is listed in the Summary pane, at the bottom of the Network panel.</span></span>  

> [!CAUTION]
> <span data-ttu-id="200bd-418">Diese Nummer verfolgt nur Anforderungen, die seit dem Öffnen von devtools protokolliert wurden.</span><span class="sxs-lookup"><span data-stu-id="200bd-418">This number only tracks requests that have been logged since DevTools was opened.</span></span>  <span data-ttu-id="200bd-419">Wenn vor dem Öffnen von devtools andere Anforderungen aufgetreten sind, werden diese Anforderungen nicht gezählt.</span><span class="sxs-lookup"><span data-stu-id="200bd-419">If other requests occurred before DevTools was opened, those requests are not counted.</span></span>  

:::image type="complex" source="../media/network-network-total-requests.msft.png" alt-text="Netzwerk Panel" lightbox="../media/network-network-total-requests.msft.png":::
   <span data-ttu-id="200bd-421">Die Gesamtzahl der Anforderungen seit dem Öffnen von devtools</span><span class="sxs-lookup"><span data-stu-id="200bd-421">The total number of requests since DevTools were opened</span></span>  
:::image-end:::  

### <span data-ttu-id="200bd-422">Anzeigen der Gesamtgröße des Downloads</span><span class="sxs-lookup"><span data-stu-id="200bd-422">View the total download size</span></span>  

<span data-ttu-id="200bd-423">Die Gesamtgröße der Downloadanforderungen wird im Bereich "Zusammenfassung" am unteren Rand des Netzwerkbereichs angezeigt.</span><span class="sxs-lookup"><span data-stu-id="200bd-423">The total download size of requests is listed in the Summary pane, at the bottom of the Network panel.</span></span>  

> [!CAUTION]
> <span data-ttu-id="200bd-424">Diese Nummer verfolgt nur Anforderungen, die seit dem Öffnen von devtools protokolliert wurden.</span><span class="sxs-lookup"><span data-stu-id="200bd-424">This number only tracks requests that have been logged since DevTools was opened.</span></span>  <span data-ttu-id="200bd-425">Wenn vor dem Öffnen von devtools andere Anforderungen aufgetreten sind, werden die vorherigen Anforderungen nicht gezählt.</span><span class="sxs-lookup"><span data-stu-id="200bd-425">If other requests occurred before DevTools was opened, the previous requests are not counted.</span></span>  

:::image type="complex" source="../media/network-network-total-download-size.msft.png" alt-text="Netzwerk Panel" lightbox="../media/network-network-total-download-size.msft.png":::
   <span data-ttu-id="200bd-427">Die Gesamtgröße der Downloads von Anforderungen</span><span class="sxs-lookup"><span data-stu-id="200bd-427">The total download size of requests</span></span>  
:::image-end:::  

<span data-ttu-id="200bd-428">Navigieren Sie zum [Anzeigen der unkomprimierten Größe einer Ressource](#view-the-uncompressed-size-of-a-resource), um zu überprüfen, wie umfangreiche Ressourcen sind, nachdem der Browser die einzelnen Elemente dekomprimiert hat.</span><span class="sxs-lookup"><span data-stu-id="200bd-428">To verify how large resources are after the browser uncompresses each item, navigate to [View the uncompressed size of a resource](#view-the-uncompressed-size-of-a-resource).</span></span>  

### <span data-ttu-id="200bd-429">Anzeigen der Stapelüberwachung, die eine Anforderung verursacht hat</span><span class="sxs-lookup"><span data-stu-id="200bd-429">View the stack trace that caused a request</span></span>  

<span data-ttu-id="200bd-430">Nachdem eine JavaScript-Anweisung eine Ressource angefordert hat, zeigen Sie mit der Maus auf die Spalte **Initiator** , um die Stapelüberwachung anzuzeigen, die zur Anforderung führt.</span><span class="sxs-lookup"><span data-stu-id="200bd-430">After a JavaScript statement requests a resource, hover over the **Initiator** column to view the stack trace leading up to the request.</span></span>  

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

:::image type="complex" source="../media/network-network-requests-initiator-stack.msft.png" alt-text="Netzwerk Panel" lightbox="../media/network-network-requests-initiator-stack.msft.png":::
   <span data-ttu-id="200bd-432">Die Stapelüberwachung, die zu einer Ressourcenanforderung führt</span><span class="sxs-lookup"><span data-stu-id="200bd-432">The stack trace leading up to a resource request</span></span>  
:::image-end:::  

### <span data-ttu-id="200bd-433">Anzeigen der unkomprimierten Größe einer Ressource</span><span class="sxs-lookup"><span data-stu-id="200bd-433">View the uncompressed size of a resource</span></span>  

<span data-ttu-id="200bd-434">Aktivieren Sie das Kontrollkästchen **große Anforderungs Zeilen verwenden** , und schauen Sie sich den niedrigsten Wert der Spalte **Größe** an.</span><span class="sxs-lookup"><span data-stu-id="200bd-434">Select the **Use large request rows** checkbox and then look at the bottom value of the **Size** column.</span></span>  

:::image type="complex" source="../media/network-network-requests-uncompressed-compare.msft.png" alt-text="Netzwerk Panel" lightbox="../media/network-network-requests-uncompressed-compare.msft.png":::
   <span data-ttu-id="200bd-436">Ein Beispiel für unkomprimierte Ressourcen \ (die komprimierte Größe der `jquery-3.3.1.min.js` Datei, die über das Netzwerk gesendet wurde `29.9 KB` , während die unkomprimierte Größe `84.9 KB` \) war</span><span class="sxs-lookup"><span data-stu-id="200bd-436">An example of uncompressed resources  \(The compressed size of the `jquery-3.3.1.min.js` file that was sent over the network was `29.9 KB`, whereas the uncompressed size was `84.9 KB`\)</span></span>  
:::image-end:::  

## <span data-ttu-id="200bd-437">Exportieren von Anforderungsdaten</span><span class="sxs-lookup"><span data-stu-id="200bd-437">Export requests data</span></span>  

### <span data-ttu-id="200bd-438">Speichern aller Netzwerkanforderungen in einer har-Datei</span><span class="sxs-lookup"><span data-stu-id="200bd-438">Save all network requests to a HAR file</span></span>  

<span data-ttu-id="200bd-439">Führen Sie die folgenden Schritte aus, um alle Netzwerkanforderungen in einer har-Datei zu speichern.</span><span class="sxs-lookup"><span data-stu-id="200bd-439">To save all network requests to a HAR file, complete the following steps.</span></span>  

1.  <span data-ttu-id="200bd-440">Zeigen Sie auf jede Anforderung in der Tabelle Anforderungen, und öffnen Sie das Kontextmenü \ (mit der rechten Maustaste auf \).</span><span class="sxs-lookup"><span data-stu-id="200bd-440">Hover on any request in the Requests table and open the contextual menu \(right-click\).</span></span>  
1.  <span data-ttu-id="200bd-441">Wählen Sie **als har mit Inhalt speichern**aus.</span><span class="sxs-lookup"><span data-stu-id="200bd-441">Choose **Save as HAR with Content**.</span></span>  <span data-ttu-id="200bd-442">DevTools speichert alle Anforderungen, die seit dem Öffnen von devtools in der har-Datei aufgetreten sind.</span><span class="sxs-lookup"><span data-stu-id="200bd-442">DevTools saves all requests that have occurred since you opened DevTools to the HAR file.</span></span>  <span data-ttu-id="200bd-443">Sie können keine Anforderungen filtern.</span><span class="sxs-lookup"><span data-stu-id="200bd-443">You are not able to filter requests.</span></span>  <span data-ttu-id="200bd-444">Sie können auch keine einzelne Anfrage speichern.</span><span class="sxs-lookup"><span data-stu-id="200bd-444">You are also not able to save a single request.</span></span>  

<span data-ttu-id="200bd-445">Nachdem Sie eine har-Datei gespeichert haben, können Sie Sie für die Analyse wieder in devtools importieren.</span><span class="sxs-lookup"><span data-stu-id="200bd-445">Once you save a HAR file, you may import it back into DevTools for analysis.</span></span>  <span data-ttu-id="200bd-446">Ziehen Sie die har-Datei einfach per Drag & Drop in die Tabelle "Anforderungen".</span><span class="sxs-lookup"><span data-stu-id="200bd-446">Just drag-and-drop the HAR file into the Requests table.</span></span>  
<!--For more information, navigate to also [HAR Analyzer][HARAnalyzer].  -->  

<!--[HARAnalyzer]: https://toolbox.alphabetapps.com/apps/har_analyzer  -->  
<!--Todo: add section link when content is available  -->  

:::image type="complex" source="../media/network-network-requests-save-har-content.msft.png" alt-text="Netzwerk Panel" lightbox="../media/network-network-requests-save-har-content.msft.png":::
   <span data-ttu-id="200bd-448">Auswählen **von "als har mit Inhalt speichern** "</span><span class="sxs-lookup"><span data-stu-id="200bd-448">Selecting **Save as HAR with Content**</span></span>  
:::image-end:::  

### <span data-ttu-id="200bd-449">Kopieren einer oder mehrerer Anforderungen in die Zwischenablage</span><span class="sxs-lookup"><span data-stu-id="200bd-449">Copy one or more requests to the clipboard</span></span>  

<span data-ttu-id="200bd-450">Zeigen Sie unter der Spalte **Name** der Tabelle Anforderungen auf eine Anforderung, öffnen Sie das Kontextmenü \ (Klicken Sie mit der rechten Maustaste auf \), zeigen Sie auf **Kopieren**, und wählen Sie eine der folgenden Optionen aus.</span><span class="sxs-lookup"><span data-stu-id="200bd-450">Under the **Name** column of the Requests table, hover on a request, open the contextual menu \(right-click\), hover over **Copy**, and select one of the following options.</span></span>  

:::row:::
   :::column span="1":::
      **<span data-ttu-id="200bd-451">Link Adresse kopieren</span><span class="sxs-lookup"><span data-stu-id="200bd-451">Copy Link Address</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="200bd-452">Kopieren Sie die URL der Anforderung in die Zwischenablage.</span><span class="sxs-lookup"><span data-stu-id="200bd-452">Copy the URL of the request to the clipboard.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="200bd-453">Antwort kopieren</span><span class="sxs-lookup"><span data-stu-id="200bd-453">Copy Response</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="200bd-454">Kopieren Sie den Antworttext in die Zwischenablage.</span><span class="sxs-lookup"><span data-stu-id="200bd-454">Copy the response body to the clipboard.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="200bd-455">Als FETCH kopieren</span><span class="sxs-lookup"><span data-stu-id="200bd-455">Copy as Fetch</span></span>**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="200bd-456">Als curl kopieren</span><span class="sxs-lookup"><span data-stu-id="200bd-456">Copy as cURL</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="200bd-457">Kopieren Sie die Anforderung als curl-Befehl.</span><span class="sxs-lookup"><span data-stu-id="200bd-457">Copy the request as a cURL command.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="200bd-458">Alle als FETCH kopieren</span><span class="sxs-lookup"><span data-stu-id="200bd-458">Copy All as Fetch</span></span>**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="200bd-459">Alle als curl kopieren</span><span class="sxs-lookup"><span data-stu-id="200bd-459">Copy All as cURL</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="200bd-460">Kopieren Sie alle Anforderungen als eine Kette von curl-Befehlen.</span><span class="sxs-lookup"><span data-stu-id="200bd-460">Copy all requests as a chain of cURL commands.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="200bd-461">Alle als har kopieren</span><span class="sxs-lookup"><span data-stu-id="200bd-461">Copy All as HAR</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="200bd-462">Kopieren Sie alle Anforderungen als har-Daten.</span><span class="sxs-lookup"><span data-stu-id="200bd-462">Copy all requests as HAR data.</span></span>  
   :::column-end:::
:::row-end:::  

:::image type="complex" source="../media/network-network-requests-copy-response.msft.png" alt-text="Netzwerk Panel" lightbox="../media/network-network-requests-copy-response.msft.png":::
   <span data-ttu-id="200bd-464">Auswählen von " **Antwort kopieren** "</span><span class="sxs-lookup"><span data-stu-id="200bd-464">Selecting **Copy Response**</span></span>  
:::image-end:::  

## <span data-ttu-id="200bd-465">Ändern des Layouts des Netzwerk Panels</span><span class="sxs-lookup"><span data-stu-id="200bd-465">Change the layout of the Network panel</span></span>  

<span data-ttu-id="200bd-466">Sie können Abschnitte der Netzwerk Panel-UI erweitern oder reduzieren, um wichtige Informationen zu konzentrieren.</span><span class="sxs-lookup"><span data-stu-id="200bd-466">You may expand or collapse sections of the Network panel UI to focus important information.</span></span>  

### <span data-ttu-id="200bd-467">Ausblenden des Bereichs "Filter"</span><span class="sxs-lookup"><span data-stu-id="200bd-467">Hide the Filters pane</span></span>  

<span data-ttu-id="200bd-468">Standardmäßig zeigt devtools den **Bereich "Filter"** an.</span><span class="sxs-lookup"><span data-stu-id="200bd-468">By default, DevTools show the **Filters pane**.</span></span>  
<span data-ttu-id="200bd-469">Wählen Sie **Filter** \ ( ![ Filter ][ImageFilterIcon] \) aus, um sie auszublenden.</span><span class="sxs-lookup"><span data-stu-id="200bd-469">Choose **Filter** \(![Filter][ImageFilterIcon]\) to hide it.</span></span>  

:::image type="complex" source="../media/network-network-resources-hide-filters-button.msft.png" alt-text="Netzwerk Panel" lightbox="../media/network-network-resources-hide-filters-button.msft.png":::
   <span data-ttu-id="200bd-471">Schaltfläche "Filter ausblenden"</span><span class="sxs-lookup"><span data-stu-id="200bd-471">The Hide Filters button</span></span>  
:::image-end:::  

### <span data-ttu-id="200bd-472">Verwenden von umfangreichen Anforderungs Zeilen</span><span class="sxs-lookup"><span data-stu-id="200bd-472">Use large request rows</span></span>  

<span data-ttu-id="200bd-473">Verwenden Sie große Zeilen, wenn in Ihrer Netzwerk Anforderungstabelle mehr Leerzeichen verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="200bd-473">Use large rows when you want more whitespace in your network requests table.</span></span>  <span data-ttu-id="200bd-474">Einige Spalten liefern auch ein wenig mehr Informationen, wenn Sie große Zeilen verwenden.</span><span class="sxs-lookup"><span data-stu-id="200bd-474">Some columns also provide a little more information when using large rows.</span></span>  <span data-ttu-id="200bd-475">Der untere Wert der Spalte **size** entspricht beispielsweise der unkomprimierten Größe einer Anforderung.</span><span class="sxs-lookup"><span data-stu-id="200bd-475">For example, the bottom value of the **Size** column is the uncompressed size of a request.</span></span>  

:::image type="complex" source="../media/network-network-requests-large-request-rows.msft.png" alt-text="Netzwerk Panel" lightbox="../media/network-network-requests-large-request-rows.msft.png":::
   <span data-ttu-id="200bd-477">Ein Beispiel für große Anforderungs Zeilen im Bereich " **Anforderungen** "</span><span class="sxs-lookup"><span data-stu-id="200bd-477">An example of large request rows in the **Requests** pane</span></span>  
:::image-end:::  

<span data-ttu-id="200bd-478">Aktivieren Sie das Kontrollkästchen **große Anforderungs Zeilen verwenden** , um große Zeilen zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="200bd-478">Select the **Use large request rows** checkbox to enable large rows.</span></span>  

:::image type="complex" source="../media/network-network-requests-use-large-request-rows-on.msft.png" alt-text="Netzwerk Panel" lightbox="../media/network-network-requests-use-large-request-rows-on.msft.png":::
   <span data-ttu-id="200bd-480">Das Kontrollkästchen " **große Anforderungs Zeilen verwenden** "</span><span class="sxs-lookup"><span data-stu-id="200bd-480">The **Use large request rows** checkbox</span></span>  
:::image-end:::  

### <span data-ttu-id="200bd-481">Ausblenden des Bereichs "Übersicht"</span><span class="sxs-lookup"><span data-stu-id="200bd-481">Hide the Overview pane</span></span>  

<span data-ttu-id="200bd-482">Standardmäßig zeigt devtools den **Bereich "Übersicht"** an.</span><span class="sxs-lookup"><span data-stu-id="200bd-482">By default, DevTools show the **Overview pane**.</span></span>  <span data-ttu-id="200bd-483">Deaktivieren Sie das Kontrollkästchen " **Übersicht anzeigen** ", um es auszublenden.</span><span class="sxs-lookup"><span data-stu-id="200bd-483">Deselect the **Show Overview** checkbox to hide it.</span></span>  

:::image type="complex" source="../media/network-network-requests-show-overview-off.msft.png" alt-text="Netzwerk Panel" lightbox="../media/network-network-requests-show-overview-off.msft.png":::
   <span data-ttu-id="200bd-485">Kontrollkästchen ' **Übersicht anzeigen** '</span><span class="sxs-lookup"><span data-stu-id="200bd-485">The **Show Overview** checkbox</span></span>  
:::image-end:::  

## <span data-ttu-id="200bd-486">Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen</span><span class="sxs-lookup"><span data-stu-id="200bd-486">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageCaptureScreenshotsIcon]: ../media/capture-screenshots-icon.msft.png  
[ImageClearIcon]: ../media/clear-requests-icon.msft.png  
[ImageFilterIcon]: ../media/filter-icon.msft.png  
[ImageHideIcon]: ../media/hide-overview-icon.msft.png  
[ImageLargeResourceRowsIcon]: ../media/large-resource-rows-button-icon.msft.png  
[ImageRecordOnIcon]: ../media/record-on-icon.msft.png  

<!-- links -->  

[DevtoolsProgressiveWebApps]: ../progressive-web-apps.md "Debuggen von progressiven Web-Apps | Microsoft docs"  

<!--[NetworkConditions]: /microsoft-edge/devtools-guide-chromium/network/network-conditions "Optimize Performance Under Varying Network Conditions | Microsoft Docs"  -->  

[MDNHTTPDataURIs]: https://developer.mozilla.org/docs/Web/HTTP/Basics_of_HTTP/Data_URIs "Daten-URLs | MDN"  

[WikiProxyServer]: https://en.wikipedia.org/wiki/Proxy_server "Proxy Server – Wikipedia"  

> [!NOTE]
> <span data-ttu-id="200bd-490">Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="200bd-490">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="200bd-491">Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/network/reference) und wird von [Kayce Basken][KayceBasques] (Technical Writer, Chrome devtools \ & Lighthouse \) erstellt.</span><span class="sxs-lookup"><span data-stu-id="200bd-491">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/network/reference) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
<span data-ttu-id="200bd-493">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="200bd-493">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
