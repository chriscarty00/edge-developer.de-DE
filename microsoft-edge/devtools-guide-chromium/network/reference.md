---
description: Eine umfassende Referenz zu den Features des Microsoft Edge devtools-Netzwerk Panels.
title: Netzwerkanalyse Referenz
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/08/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: 4d4dc8ad5102766f3ad3c8322dbf9342a69e9097
ms.sourcegitcommit: 6571bcc0b7f1c4c9d6ead65081374bab87cd4469
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "11203906"
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

# <span data-ttu-id="8682e-104">Netzwerkanalyse Referenz</span><span class="sxs-lookup"><span data-stu-id="8682e-104">Network Analysis reference</span></span>  

<span data-ttu-id="8682e-105">Entdecken Sie neue Möglichkeiten zur Analyse, wie Ihre Seite in dieser umfassenden Referenz der Microsoft Edge devtools-Netzwerkanalyse Features geladen werden kann.</span><span class="sxs-lookup"><span data-stu-id="8682e-105">Discover new ways to analyze how your page loads in this comprehensive reference of Microsoft Edge DevTools network analysis features.</span></span>  

## <span data-ttu-id="8682e-106">Aufzeichnen von Netzwerkanforderungen</span><span class="sxs-lookup"><span data-stu-id="8682e-106">Record network requests</span></span>  

<span data-ttu-id="8682e-107">Standardmäßig zeichnet devtools alle Netzwerkanforderungen im **Netzwerk** Panel auf, solange devtools geöffnet ist.</span><span class="sxs-lookup"><span data-stu-id="8682e-107">By default, DevTools record all network requests in the **Network** panel, so long as DevTools is open.</span></span>  

:::image type="complex" source="../media/network-network-panel.msft.png" alt-text="Netzwerk Panel" lightbox="../media/network-network-panel.msft.png":::
   <span data-ttu-id="8682e-109">**Netzwerk** Panel</span><span class="sxs-lookup"><span data-stu-id="8682e-109">The **Network** panel</span></span>  
:::image-end:::  

### <span data-ttu-id="8682e-110">Beenden der Aufzeichnung von Netzwerkanforderungen</span><span class="sxs-lookup"><span data-stu-id="8682e-110">Stop recording network requests</span></span>  

<span data-ttu-id="8682e-111">Führen Sie die folgenden Schritte aus, um die Aufzeichnung von Anforderungen zu beenden.</span><span class="sxs-lookup"><span data-stu-id="8682e-111">To stop recording requests, complete the following steps.</span></span>  

1.  <span data-ttu-id="8682e-112">Wählen Sie im **Netzwerk** Panel die Option **Aufzeichnung des Netzwerkprotokolls beenden** \ ( ![ Aufzeichnung des Netzwerkprotokolls beenden ][ImageRecordOnIcon] \) aus.</span><span class="sxs-lookup"><span data-stu-id="8682e-112">On the **Network** panel, choose **Stop recording network log** \(![Stop recording network log][ImageRecordOnIcon]\).</span></span>  <span data-ttu-id="8682e-113">Es wird grau, um anzugeben, dass devtools keine Anforderungen mehr aufzeichnet.</span><span class="sxs-lookup"><span data-stu-id="8682e-113">It turns grey to indicate that DevTools is no longer recording requests.</span></span>  
1.  <span data-ttu-id="8682e-114">Wählen Sie `Control` + `E` \ (Windows, Linux \) oder `Command` + `E` \ (macOS \) aus, während sich der Fokus des **Netzwerk** Panels befindet.</span><span class="sxs-lookup"><span data-stu-id="8682e-114">Select `Control`+`E` \(Windows, Linux\) or `Command`+`E` \(macOS\) while the **Network** panel is in focus.</span></span>  

### <span data-ttu-id="8682e-115">Löschen von Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8682e-115">Clear requests</span></span>  

<span data-ttu-id="8682e-116">Wählen Sie im Netzwerk Panel die Option **"Löschen"** ![ ][ImageClearIcon] aus, um alle Anforderungen aus der Tabelle "Anforderungen" zu löschen. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="8682e-116">Choose **Clear** \(![Clear][ImageClearIcon]\) on the **Network** panel to clear all requests from the Requests table.</span></span>  

:::image type="complex" source="../media/network-network-clear-button.msft.png" alt-text="Die Schaltfläche "Löschen"" lightbox="../media/network-network-clear-button.msft.png":::
   <span data-ttu-id="8682e-118">Die Schaltfläche " **Löschen** "</span><span class="sxs-lookup"><span data-stu-id="8682e-118">The **Clear** button</span></span>  
:::image-end:::  

### <span data-ttu-id="8682e-119">Speichern von Anforderungen über Seitenlasten hinweg</span><span class="sxs-lookup"><span data-stu-id="8682e-119">Save requests across page loads</span></span>  

<span data-ttu-id="8682e-120">Wenn Sie Anforderungen zwischen Seitenlasten speichern möchten, aktivieren Sie im **Netzwerk** Panel das Kontrollkästchen **Protokoll beibehalten** .</span><span class="sxs-lookup"><span data-stu-id="8682e-120">To save requests across page loads, on the **Network** panel, turn on the **Preserve log** checkbox.</span></span>  <span data-ttu-id="8682e-121">DevTools speichert alle Anforderungen, bis Sie **Protokoll beibehalten**deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="8682e-121">DevTools saves all requests until you disable **Preserve log**.</span></span>  

:::image type="complex" source="../media/network-network-preserve-log.msft.png" alt-text="Kontrollkästchen "Protokoll beibehalten"" lightbox="../media/network-network-preserve-log.msft.png":::
   <span data-ttu-id="8682e-123">Kontrollkästchen " **Protokoll beibehalten** "</span><span class="sxs-lookup"><span data-stu-id="8682e-123">The **Preserve Log** checkbox</span></span>  
:::image-end:::  

### <span data-ttu-id="8682e-124">Aufzeichnen von Screenshots beim Laden der Seite</span><span class="sxs-lookup"><span data-stu-id="8682e-124">Capture screenshots during page load</span></span>  

<span data-ttu-id="8682e-125">Screenshots aufzeichnen, um zu analysieren, was für Benutzer angezeigt wird, während Sie darauf warten, dass Ihre Seite geladen wird.</span><span class="sxs-lookup"><span data-stu-id="8682e-125">Capture screenshots to analyze what displays for users while waiting for your page to load.</span></span>  

<span data-ttu-id="8682e-126">Wenn Sie Screenshots aktivieren möchten, wählen Sie **Netzwerkeinstellungen**aus, und aktivieren Sie auf der Registerkarte **Netzwerk** das Kontrollkästchen **Screenshots aufnehmen** .</span><span class="sxs-lookup"><span data-stu-id="8682e-126">To enable screenshots, choose **Network settings**, and on the **Network** panel, turn on the **Capture screenshots** checkbox.</span></span>  

<span data-ttu-id="8682e-127">Aktualisieren Sie die Seite, während sich das **Netzwerk** Panel im Fokus befindet, um Screenshots zu erfassen.</span><span class="sxs-lookup"><span data-stu-id="8682e-127">Refresh the page while the **Network** panel is in focus to capture screenshots.</span></span>  

<span data-ttu-id="8682e-128">Nachdem Sie einen Screenshot aufgezeichnet haben, interagieren Sie mit ihm auf die folgende Weise.</span><span class="sxs-lookup"><span data-stu-id="8682e-128">After capturing a screenshot, you interact with it in the following ways.</span></span>  

*   <span data-ttu-id="8682e-129">Zeigen Sie auf einen Screenshot, um den Punkt anzuzeigen, an dem dieser Screenshot aufgenommen wurde.</span><span class="sxs-lookup"><span data-stu-id="8682e-129">Hover on a screenshot to display the point at which that screenshot was captured.</span></span>  <span data-ttu-id="8682e-130">Im Bereich " **Übersicht** " wird eine gelbe Zeile angezeigt.</span><span class="sxs-lookup"><span data-stu-id="8682e-130">A yellow line is displayed on the **Overview** pane.</span></span>  
*   <span data-ttu-id="8682e-131">Wählen Sie die Miniaturansicht eines Bildschirms aus, um alle Anforderungen zu filtern, die nach dem Erfassen des Screenshots aufgetreten sind.</span><span class="sxs-lookup"><span data-stu-id="8682e-131">Choose the thumbnail of a screen to filter out any requests that occurred after the screenshot was captured.</span></span>  
*   <span data-ttu-id="8682e-132">Doppelklicken Sie auf eine Miniaturansicht, um Sie zu vergrößern.</span><span class="sxs-lookup"><span data-stu-id="8682e-132">Double-click a thumbnail to zoom into it.</span></span>  

:::image type="complex" source="../media/network-network-screenshot-hover.msft.png" alt-text="Zeigen Sie auf einen Screenshot." lightbox="../media/network-network-screenshot-hover.msft.png":::
   <span data-ttu-id="8682e-134">Zeigen Sie auf einen Screenshot.</span><span class="sxs-lookup"><span data-stu-id="8682e-134">Hover on a screenshot</span></span>  
:::image-end:::  

<!--  ### Replay XHR request  -->

<!--  To replay an XHR request, hover on the request in the Requests table, open the contextual menu \(right-click\), and choose **Replay XHR**.  -->

<!--  
:::image type="complex" source="../media/network-replay-xhr.msft.png" alt-text="Choose Replay XHR" lightbox="../media/network-replay-xhr.msft.png":::
   Choose Replay XHR  
:::image-end:::  
-->  

## <span data-ttu-id="8682e-135">Ändern des Ladeverhaltens</span><span class="sxs-lookup"><span data-stu-id="8682e-135">Change loading behavior</span></span>  

### <span data-ttu-id="8682e-136">Emulieren eines erstmaligen Besuchers durch Deaktivieren des Browsercaches</span><span class="sxs-lookup"><span data-stu-id="8682e-136">Emulate a first-time visitor by disabling the browser cache</span></span>  

<span data-ttu-id="8682e-137">Aktivieren Sie das Kontrollkästchen **Cache deaktivieren** , um zu emulieren, wie ein Erstbenutzer Ihre Website erlebt.</span><span class="sxs-lookup"><span data-stu-id="8682e-137">To emulate how a first-time user experiences your site, turn on the **Disable cache** checkbox.</span></span>  <span data-ttu-id="8682e-138">DevTools deaktiviert den Browsercache.</span><span class="sxs-lookup"><span data-stu-id="8682e-138">DevTools disables the browser cache.</span></span>  <span data-ttu-id="8682e-139">Dieses Feature emuliert die Benutzerfreundlichkeit des ersten Benutzers genauer, da Anforderungen im Browser-Cache für wiederholte Besuche bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="8682e-139">This feature more accurately emulates a first-time user's experience, because requests are served from the browser cache on repeat visits.</span></span>  

:::image type="complex" source="../media/network-network-disable-cache-checkbox.msft.png" alt-text="Kontrollkästchen "Cache deaktivieren"" lightbox="../media/network-network-disable-cache-checkbox.msft.png":::
   <span data-ttu-id="8682e-141">Kontrollkästchen " **Cache deaktivieren** "</span><span class="sxs-lookup"><span data-stu-id="8682e-141">The **Disable Cache** checkbox</span></span>  
:::image-end:::  

#### <span data-ttu-id="8682e-142">Deaktivieren des Browser-Caches aus der Schublade "Netzwerkbedingungen"</span><span class="sxs-lookup"><span data-stu-id="8682e-142">Disable the browser cache from the Network Conditions drawer</span></span>  

<span data-ttu-id="8682e-143">Wenn Sie den Cache während der Arbeit in anderen devtools-Panels deaktivieren möchten, verwenden Sie die Schublade Netzwerkbedingungen.</span><span class="sxs-lookup"><span data-stu-id="8682e-143">If you want to disable the cache while working in other DevTools panels, use the Network Conditions drawer.</span></span>  

1.  <span data-ttu-id="8682e-144">Öffnen Sie die Schublade **Netzwerkbedingungen** .</span><span class="sxs-lookup"><span data-stu-id="8682e-144">Open the **Network Conditions** drawer.</span></span>  
1.  <span data-ttu-id="8682e-145">Aktivieren Sie das Kontrollkästchen **Cache deaktivieren** .</span><span class="sxs-lookup"><span data-stu-id="8682e-145">Turn on \(or off\) the **Disable cache** checkbox.</span></span>  

<!--todo: add network condition section when available -->  

### <span data-ttu-id="8682e-146">Manuelles Löschen des Browsercaches</span><span class="sxs-lookup"><span data-stu-id="8682e-146">Manually clear the browser cache</span></span>  

<span data-ttu-id="8682e-147">Wenn Sie den Browser-Cache jederzeit manuell löschen möchten, öffnen Sie das Kontextmenü \ (Klicken Sie mit der rechten Maustaste auf \) an einer beliebigen Stelle in der Tabelle Anforderungen, und wählen Sie **Browsercache löschen**aus.</span><span class="sxs-lookup"><span data-stu-id="8682e-147">To manually clear the browser cache at any time, open the contextual menu \(right-click\) anywhere in the Requests table and choose **Clear Browser Cache**.</span></span>  

:::image type="complex" source="../media/network-network-clear-browser-cache.msft.png" alt-text="Wählen Sie Browser Cache löschen aus." lightbox="../media/network-network-clear-browser-cache.msft.png":::
   <span data-ttu-id="8682e-149">Wählen Sie **Browser Cache löschen** aus.</span><span class="sxs-lookup"><span data-stu-id="8682e-149">Choose **Clear Browser Cache**</span></span>  
:::image-end:::  

### <span data-ttu-id="8682e-150">Offline emulieren</span><span class="sxs-lookup"><span data-stu-id="8682e-150">Emulate offline</span></span>  

<span data-ttu-id="8682e-151">Eine neue Klasse von Web-Apps mit dem Namen " [Progressive Web Apps][DevtoolsProgressiveWebApps]" funktioniert mit Hilfe von **Servicemitarbeitern**offline.</span><span class="sxs-lookup"><span data-stu-id="8682e-151">A new class of web apps, named [Progressive Web Apps][DevtoolsProgressiveWebApps], functions offline with the help of **service workers**.</span></span>  <span data-ttu-id="8682e-152">Möglicherweise ist es hilfreich, ein Gerät, das keine Datenverbindung aufweist, schnell zu simulieren, wenn Sie diese Art von App erstellen.</span><span class="sxs-lookup"><span data-stu-id="8682e-152">You may find it useful to quickly simulate a device that has no data connection when you are building this type of app.</span></span>  

<!--[ServiceWorkers]: /web/fundamentals/getting-started/primers/service-workers  -->

<span data-ttu-id="8682e-153">Wählen Sie das Dropdownmenü **Online** aus, suchen Sie unter **Voreinstellungen**, und wählen Sie **Offline** aus, um eine Offlinenetzwerk Umgebung zu simulieren.</span><span class="sxs-lookup"><span data-stu-id="8682e-153">Choose the **Online** dropdown menu, search under **Presets**, and choose **Offline** to simulate an offline network experience.</span></span>  

:::image type="complex" source="../media/network-network-offline-dropdown.msft.png" alt-text="Das Offline-Dropdownmenü" lightbox="../media/network-network-offline-dropdown.msft.png":::
   <span data-ttu-id="8682e-155">Das **Offline** -Dropdownmenü</span><span class="sxs-lookup"><span data-stu-id="8682e-155">The **Offline** dropdown menu</span></span>  
:::image-end:::  

### <span data-ttu-id="8682e-156">Emulieren langsamer Netzwerkverbindungen</span><span class="sxs-lookup"><span data-stu-id="8682e-156">Emulate slow network connections</span></span>  

<span data-ttu-id="8682e-157">Emulieren Sie langsames 3G, fast 3G und andere Verbindungsgeschwindigkeiten über das **Online-Dropdown-** Menü.</span><span class="sxs-lookup"><span data-stu-id="8682e-157">Emulate Slow 3G, Fast 3G, and other connection speeds from the **Online** dropdown menu.</span></span>  

:::image type="complex" source="../media/network-network-throttling-menu.msft.png" alt-text="Dropdownmenü "Drosselung"" lightbox="../media/network-network-throttling-menu.msft.png":::
   <span data-ttu-id="8682e-159">Dropdownmenü " **Drosselung** "</span><span class="sxs-lookup"><span data-stu-id="8682e-159">The **Throttling** dropdown menu</span></span>  
:::image-end:::  

<span data-ttu-id="8682e-160">Sie haben die Wahl zwischen verschiedenen Voreinstellungen wie Slow 3G oder fast 3G.</span><span class="sxs-lookup"><span data-stu-id="8682e-160">You may choose from different presets, such as Slow 3G or Fast 3G.</span></span>  <span data-ttu-id="8682e-161">Wenn Sie eigene benutzerdefinierte Voreinstellungen hinzufügen möchten, öffnen Sie das Menü Drosselung, und wählen Sie **benutzerdefiniertes**  >  **Add**aus.</span><span class="sxs-lookup"><span data-stu-id="8682e-161">To add your own custom presets, open the Throttling menu, and choose **Custom** > **Add**.</span></span>  

<span data-ttu-id="8682e-162">DevTools zeigt ein Warnungssymbol neben der Registerkarte " **Netzwerk** " an, um Sie daran zu erinnern, dass die Drosselung aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="8682e-162">DevTools displays a warning icon next to the **Network** tab to remind you that throttling is enabled.</span></span>  

#### <span data-ttu-id="8682e-163">Emulieren von langsamen Netzwerkverbindungen über die Netzwerkbedingungen Schublade</span><span class="sxs-lookup"><span data-stu-id="8682e-163">Emulate slow network connections from the Network Conditions drawer</span></span>  

<span data-ttu-id="8682e-164">Wenn Sie die Netzwerkverbindung während der Arbeit in anderen devtools-Panels Drosseln möchten, verwenden Sie den Netzwerkbedingungen-Einzug.</span><span class="sxs-lookup"><span data-stu-id="8682e-164">If you want to throttle the network connection while working in other DevTools panels, use the Network Conditions drawer.</span></span>  

1.  <span data-ttu-id="8682e-165">Öffnen Sie die Schublade **Netzwerkbedingungen** .</span><span class="sxs-lookup"><span data-stu-id="8682e-165">Open the **Network Conditions** drawer.</span></span>  
1.  <span data-ttu-id="8682e-166">Wählen Sie Ihre Verbindungsgeschwindigkeit im Menü " **Drosselung** " aus.</span><span class="sxs-lookup"><span data-stu-id="8682e-166">Choose your connection speed from the **Throttling** menu.</span></span>  

<!--todo: add network condition section when available -->  

### <span data-ttu-id="8682e-167">Manuelles Löschen von Browser-Cookies</span><span class="sxs-lookup"><span data-stu-id="8682e-167">Manually clear browser cookies</span></span>  

<span data-ttu-id="8682e-168">Wenn Sie Browser-Cookies jederzeit manuell löschen möchten, zeigen Sie mit der Maus auf eine beliebige Stelle in der Tabelle Anforderungen, öffnen Sie das Kontextmenü \ (Klicken Sie mit der rechten Maustaste auf \), und wählen Sie **Browser-Cookies löschen**aus.</span><span class="sxs-lookup"><span data-stu-id="8682e-168">To manually clear browser cookies at any time, hover anywhere in the Requests table, open the contextual menu \(right-click\), and choose **Clear Browser Cookies**.</span></span>  

:::image type="complex" source="../media/network-network-clear-browser-cookies.msft.png" alt-text="Auswählen von Browser-Cookies löschen" lightbox="../media/network-network-clear-browser-cookies.msft.png":::
   <span data-ttu-id="8682e-170">Auswählen von **Browser-Cookies löschen**</span><span class="sxs-lookup"><span data-stu-id="8682e-170">Choose **Clear Browser Cookies**</span></span>  
:::image-end:::  

### <span data-ttu-id="8682e-171">Überschreiben des Benutzer-Agents</span><span class="sxs-lookup"><span data-stu-id="8682e-171">Override the user agent</span></span>  

<span data-ttu-id="8682e-172">Führen Sie die folgenden Schritte aus, um den Benutzer-Agent manuell zu überschreiben.</span><span class="sxs-lookup"><span data-stu-id="8682e-172">To manually override the user agent, use the following steps.</span></span>  

1.  <span data-ttu-id="8682e-173">Öffnen Sie die Schublade **Netzwerkbedingungen** .</span><span class="sxs-lookup"><span data-stu-id="8682e-173">Open the **Network Conditions** drawer.</span></span>  
1.  <span data-ttu-id="8682e-174">Deaktivieren Sie das Kontrollkästchen **automatisch auswählen** .</span><span class="sxs-lookup"><span data-stu-id="8682e-174">Turn off the **Select automatically** checkbox.</span></span>  
1.  <span data-ttu-id="8682e-175">Wählen Sie eine Option für den Benutzer-Agent aus dem Menü aus, oder geben Sie eine benutzerdefinierte Option in das Textfeld ein.</span><span class="sxs-lookup"><span data-stu-id="8682e-175">Choose a user agent option from the menu, or enter a custom one in the text box.</span></span>  

<!--todo: add network condition section when available -->  

## <span data-ttu-id="8682e-176">Filter Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8682e-176">Filter requests</span></span>  

### <span data-ttu-id="8682e-177">Filtern von Anforderungen nach Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="8682e-177">Filter requests by properties</span></span>  

<span data-ttu-id="8682e-178">Verwenden Sie das Textfeld **Filtern** , um Anforderungen nach Eigenschaften wie der Domäne oder der Größe der Anforderung zu filtern.</span><span class="sxs-lookup"><span data-stu-id="8682e-178">Use the **Filter** text box to filter requests by properties, such as the domain or size of the request.</span></span>  

<span data-ttu-id="8682e-179">Wenn das Textfeld nicht angezeigt wird, ist der **Filter** Bereich wahrscheinlich ausgeblendet.</span><span class="sxs-lookup"><span data-stu-id="8682e-179">If the text box is not displayed, the **Filters** pane is probably hidden.</span></span>  
<span data-ttu-id="8682e-180">Wenn Sie weitere Informationen erhalten möchten, navigieren Sie zum [Ausblenden des Filters-Bereichs](#hide-the-filters-pane).</span><span class="sxs-lookup"><span data-stu-id="8682e-180">For more information, navigate to [Hide the Filters pane](#hide-the-filters-pane).</span></span>  

:::image type="complex" source="../media/network-network-filters-textbox.msft.png" alt-text="Das Textfeld "Filter"" lightbox="../media/network-network-filters-textbox.msft.png":::
   <span data-ttu-id="8682e-182">Das Textfeld " **Filter** "</span><span class="sxs-lookup"><span data-stu-id="8682e-182">The **Filter** text box</span></span>  
:::image-end:::  

<span data-ttu-id="8682e-183">Sie können mehrere Eigenschaften gleichzeitig verwenden, indem Sie jede Eigenschaft mit einem Leerzeichen voneinander trennen.</span><span class="sxs-lookup"><span data-stu-id="8682e-183">You may use multiple properties simultaneously by separating each property with a space.</span></span>  <span data-ttu-id="8682e-184">Zeigt beispielsweise `mime-type:image/png larger-than:1K` alle PNGs an, die größer als 1 KB sind.</span><span class="sxs-lookup"><span data-stu-id="8682e-184">For example, `mime-type:image/png larger-than:1K` displays all PNGs that are larger than 1 kilobyte.</span></span>  <span data-ttu-id="8682e-185">Die Filter für mehrere Eigenschaften sind äquivalent zu `AND` Vorgängen.</span><span class="sxs-lookup"><span data-stu-id="8682e-185">The multi-property filters are equivalent to `AND` operations.</span></span>  `OR` <span data-ttu-id="8682e-186">Vorgänge werden zurzeit nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="8682e-186">operations are currently not supported.</span></span>  

<span data-ttu-id="8682e-187">Die vollständige Liste der unterstützten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="8682e-187">The complete list of supported properties.</span></span>  

| <span data-ttu-id="8682e-188">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="8682e-188">Property</span></span> | <span data-ttu-id="8682e-189">Details</span><span class="sxs-lookup"><span data-stu-id="8682e-189">Details</span></span> |  
|:--- | :--- |  
| `domain` | <span data-ttu-id="8682e-190">Zeigt nur Ressourcen aus der angegebenen Domäne an.</span><span class="sxs-lookup"><span data-stu-id="8682e-190">Only display resources from the specified domain.</span></span>  <span data-ttu-id="8682e-191">Sie können ein Platzhalterzeichen \ ( `*` \) verwenden, um mehrere Domänen einzubeziehen.</span><span class="sxs-lookup"><span data-stu-id="8682e-191">You may use a wildcard character \(`*`\) to include multiple domains.</span></span>  <span data-ttu-id="8682e-192">Zeigt beispielsweise `*.com` Ressourcen aus allen Domänennamen an, die in endet `.com` .</span><span class="sxs-lookup"><span data-stu-id="8682e-192">For example, `*.com` displays resources from all domain names ending in `.com`.</span></span>  <span data-ttu-id="8682e-193">DevTools füllen Sie das Dropdownmenü AutoVervollständigen mit allen gefundenen Domänen auf.</span><span class="sxs-lookup"><span data-stu-id="8682e-193">DevTools populate the autocomplete dropdown menu with all of the domains that are found.</span></span> |  
| `has-response-header` | <span data-ttu-id="8682e-194">Zeigt die Ressourcen an, die den angegebenen HTTP-Antwortheader enthalten.</span><span class="sxs-lookup"><span data-stu-id="8682e-194">Displays the resources that contain the specified HTTP response header.</span></span>  <span data-ttu-id="8682e-195">DevTools füllen Sie die Dropdownliste AutoVervollständigen mit allen gefundenen Antwortheadern auf.</span><span class="sxs-lookup"><span data-stu-id="8682e-195">DevTools populate the autocomplete dropdown with all of the response headers that are found.</span></span> |  
| `is` | <span data-ttu-id="8682e-196">Verwendet `is:running` , um `WebSocket` Ressourcen zu finden.</span><span class="sxs-lookup"><span data-stu-id="8682e-196">Use `is:running` to find `WebSocket` resources.</span></span> |  
| `larger-than` | <span data-ttu-id="8682e-197">Zeigt Ressourcen an, die größer als die angegebene Größe in Bytes sind.</span><span class="sxs-lookup"><span data-stu-id="8682e-197">Displays resources that are larger than the specified size, in bytes.</span></span>  <span data-ttu-id="8682e-198">Das Festlegen eines Werts von entspricht dem `1000` Festlegen eines Werts von `1k` .</span><span class="sxs-lookup"><span data-stu-id="8682e-198">Setting a value of `1000` is equivalent to setting a value of `1k`.</span></span> |  
| `method` | <span data-ttu-id="8682e-199">Zeigt Ressourcen an, die über einen angegebenen http-Methodentyp abgerufen wurden.</span><span class="sxs-lookup"><span data-stu-id="8682e-199">Displays resources that were retrieved over a specified HTTP method type.</span></span>  <span data-ttu-id="8682e-200">DevTools füllen Sie die Dropdownliste mit allen gefundenen HTTP-Methoden auf.</span><span class="sxs-lookup"><span data-stu-id="8682e-200">DevTools populate the dropdown with all of the HTTP methods  that are found.</span></span> |  
| `mime-type` | <span data-ttu-id="8682e-201">Zeigt Ressourcen eines angegebenen MIME-Typs an.</span><span class="sxs-lookup"><span data-stu-id="8682e-201">Displays resources of a specified MIME type.</span></span>  <span data-ttu-id="8682e-202">DevTools füllen Sie die Dropdownliste mit allen gefundenen MIME-Typen auf.</span><span class="sxs-lookup"><span data-stu-id="8682e-202">DevTools populate the dropdown with all MIME types  that are found.</span></span> |  
| `mixed-content` | <span data-ttu-id="8682e-203">Alle gemischten Inhalts Ressourcen anzeigen \ ( `mixed-content:all` \) oder nur diejenigen, die aktuell angezeigt werden \ ( `mixed-content:displayed` \).</span><span class="sxs-lookup"><span data-stu-id="8682e-203">Show all mixed content resources \(`mixed-content:all`\) or just the ones that are currently displayed \(`mixed-content:displayed`\).</span></span> |  
| `scheme` | <span data-ttu-id="8682e-204">Zeigt Ressourcen an, die über ungeschützten http \ ( `scheme:http` \) oder geschütztes HTTPS \ ( `scheme:https` \) abgerufen wurden.</span><span class="sxs-lookup"><span data-stu-id="8682e-204">Displays resources retrieved over unprotected HTTP \(`scheme:http`\) or protected HTTPS \(`scheme:https`\).</span></span> |  
| `set-cookie-domain` | <span data-ttu-id="8682e-205">Zeigt Ressourcen `Set-Cookie` mit einer Kopfzeile mit einem `Domain` Attribut an, das dem angegebenen Wert entspricht.</span><span class="sxs-lookup"><span data-stu-id="8682e-205">Displays resources that have a `Set-Cookie` header with a `Domain` attribute that matches the specified value.</span></span>  <span data-ttu-id="8682e-206">DevTools füllen Sie das AutoVervollständigen mit allen gefundenen Cookie-Domänen auf.</span><span class="sxs-lookup"><span data-stu-id="8682e-206">DevTools populate the autocomplete with all of the cookie domains that are found.</span></span> |  
| `set-cookie-name` | <span data-ttu-id="8682e-207">Zeigt Ressourcen `Set-Cookie` mit einer Kopfzeile mit einem Namen an, der dem angegebenen Wert entspricht.</span><span class="sxs-lookup"><span data-stu-id="8682e-207">Displays resources that have a `Set-Cookie` header with a name that matches the specified value.</span></span>  <span data-ttu-id="8682e-208">DevTools füllen Sie die AutoVervollständigen-Datei mit allen gefundenen Cookienamen auf.</span><span class="sxs-lookup"><span data-stu-id="8682e-208">DevTools populate the autocomplete with all of the cookie names that are found.</span></span> |  
| `set-cookie-value` | <span data-ttu-id="8682e-209">Zeigt Ressourcen `Set-Cookie` mit einer Kopfzeile mit einem Wert an, der dem angegebenen Wert entspricht.</span><span class="sxs-lookup"><span data-stu-id="8682e-209">Displays resources that have a `Set-Cookie` header with a value that matches the specified value.</span></span>  <span data-ttu-id="8682e-210">DevTools füllen Sie das AutoVervollständigen mit allen gefundenen Cookie-Werten auf.</span><span class="sxs-lookup"><span data-stu-id="8682e-210">DevTools populate the autocomplete with all of the cookie values that are found.</span></span> |  
| `status-code` | <span data-ttu-id="8682e-211">Zeigt Ressourcen an, die dem spezifischen HTTP-Statuscode entsprechen.</span><span class="sxs-lookup"><span data-stu-id="8682e-211">Displays resources that match the specific HTTP status code.</span></span>  <span data-ttu-id="8682e-212">DevTools füllt das Dropdownmenü AutoVervollständigen mit allen gefundenen Statuscodes auf.</span><span class="sxs-lookup"><span data-stu-id="8682e-212">DevTools populates the autocomplete dropdown menu with all of the status codes that are found.</span></span> |  

### <span data-ttu-id="8682e-213">Filtern von Anforderungen nach Typ</span><span class="sxs-lookup"><span data-stu-id="8682e-213">Filter requests by type</span></span>  

<span data-ttu-id="8682e-214">Wenn Sie Anforderungen nach Anforderungsfiltern möchten, wählen Sie eine der folgenden Schaltflächen im **Netzwerk** Panel aus.</span><span class="sxs-lookup"><span data-stu-id="8682e-214">To filter requests by request type, choose the one of the following buttons on the **Network** panel.</span></span>  

:::row:::
   :::column span="1":::
      **<span data-ttu-id="8682e-215">XMLHttpRequest</span><span class="sxs-lookup"><span data-stu-id="8682e-215">XHR</span></span>**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="8682e-216">JS</span><span class="sxs-lookup"><span data-stu-id="8682e-216">JS</span></span>**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="8682e-217">CSS</span><span class="sxs-lookup"><span data-stu-id="8682e-217">CSS</span></span>**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="8682e-218">IMG</span><span class="sxs-lookup"><span data-stu-id="8682e-218">Img</span></span>**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="8682e-219">Media</span><span class="sxs-lookup"><span data-stu-id="8682e-219">Media</span></span>**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="8682e-220">Font</span><span class="sxs-lookup"><span data-stu-id="8682e-220">Font</span></span>**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="8682e-221">Doc</span><span class="sxs-lookup"><span data-stu-id="8682e-221">Doc</span></span>**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="8682e-222">WS</span><span class="sxs-lookup"><span data-stu-id="8682e-222">WS</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="8682e-223">WebSocket.</span><span class="sxs-lookup"><span data-stu-id="8682e-223">WebSocket.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="8682e-224">Manifest</span><span class="sxs-lookup"><span data-stu-id="8682e-224">Manifest</span></span>**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="8682e-225">Other</span><span class="sxs-lookup"><span data-stu-id="8682e-225">Other</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="8682e-226">Jeder andere Typ, der nicht aufgeführt ist.</span><span class="sxs-lookup"><span data-stu-id="8682e-226">Any other type not listed.</span></span>  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="8682e-227">Wenn die Schaltflächen nicht angezeigt werden, ist der Bereich " **Filter** " möglicherweise ausgeblendet.</span><span class="sxs-lookup"><span data-stu-id="8682e-227">If the buttons do not display, the **Filters** pane may be hidden.</span></span>  
<span data-ttu-id="8682e-228">Wenn Sie weitere Informationen erhalten möchten, navigieren Sie zum [Ausblenden des Filters-Bereichs](#hide-the-filters-pane).</span><span class="sxs-lookup"><span data-stu-id="8682e-228">For more information, navigate to [Hide the Filters pane](#hide-the-filters-pane).</span></span>  

<span data-ttu-id="8682e-229">Wenn Sie mehrere Typen Filter gleichzeitig aktivieren möchten, halten `Control` Sie \ (Windows, Linux \) oder `Command` \ (macOS \) gedrückt, und wählen Sie dann aus.</span><span class="sxs-lookup"><span data-stu-id="8682e-229">To enable multiple type filters simultaneously, hold `Control` \(Windows, Linux\) or `Command` \(macOS\) and then choose.</span></span>  

:::image type="complex" source="../media/network-network-type-filters.msft.png" alt-text="Verwenden des Typs "Filter" zum Anzeigen von JS-, CSS-und Dokument Ressourcen" lightbox="../media/network-network-type-filters.msft.png":::
   <span data-ttu-id="8682e-231">Verwenden des Typs "Filter" zum Anzeigen von JS-, CSS-und Dokument Ressourcen</span><span class="sxs-lookup"><span data-stu-id="8682e-231">Use the Type filters to display JS, CSS, and Document resources</span></span>  
:::image-end:::  

### <span data-ttu-id="8682e-232">Filtern von Anforderungen nach Zeit</span><span class="sxs-lookup"><span data-stu-id="8682e-232">Filter requests by time</span></span>  

<span data-ttu-id="8682e-233">Wählen Sie aus, und ziehen **Sie im Übersichtsbereich nach** Links oder rechts, um nur Anforderungen anzuzeigen, die während dieses Zeitrahmens aktiv waren.</span><span class="sxs-lookup"><span data-stu-id="8682e-233">Choose and drag left or right on the **Overview** pane to only display requests that were active during that time frame.</span></span>  <span data-ttu-id="8682e-234">Der Filter ist inklusive.</span><span class="sxs-lookup"><span data-stu-id="8682e-234">The filter is inclusive.</span></span>  <span data-ttu-id="8682e-235">Jede Anforderung, die während der hervorgehobenen Zeit aktiv war, wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="8682e-235">Any request that was active during the highlighted time is shown.</span></span>  

:::image type="complex" source="../media/network-network-overview-filter.msft.png" alt-text="Herausfiltern aller Anforderungen, die um 300 ms inaktiv waren" lightbox="../media/network-network-overview-filter.msft.png":::
   <span data-ttu-id="8682e-237">Herausfiltern aller Anforderungen, die um 300 ms inaktiv waren</span><span class="sxs-lookup"><span data-stu-id="8682e-237">Filter out any requests that were inactive around 300 ms</span></span>  
:::image-end:::  

### <span data-ttu-id="8682e-238">Ausblenden von Daten-URLs</span><span class="sxs-lookup"><span data-stu-id="8682e-238">Hide data URLs</span></span>  

<span data-ttu-id="8682e-239">[Daten-URLs][MDNHTTPDataURIs] sind kleine Dateien, die in andere Dokumente eingebettet sind.</span><span class="sxs-lookup"><span data-stu-id="8682e-239">[Data URLs][MDNHTTPDataURIs] are small files embedded into other documents.</span></span>  <span data-ttu-id="8682e-240">Jede Anforderung, die in der Tabelle "Anforderungen" angezeigt wird, beginnt mit `data:` einer Daten-URL.</span><span class="sxs-lookup"><span data-stu-id="8682e-240">Any request that displays in the Requests table that starts with `data:` is a data URL.</span></span>  

<span data-ttu-id="8682e-241">Wenn Sie die Anforderungen ausblenden möchten, deaktivieren Sie das Kontrollkästchen **Daten-URLs ausblenden** .</span><span class="sxs-lookup"><span data-stu-id="8682e-241">To hide the requests, turn off the **Hide data URLs** checkbox.</span></span>  

:::image type="complex" source="../media/network-network-hide-data-urls.msft.png" alt-text="Das Kontrollkästchen "Daten-URLs ausblenden"" lightbox="../media/network-network-hide-data-urls.msft.png":::
   <span data-ttu-id="8682e-243">Das Kontrollkästchen " **Daten-URLs ausblenden** "</span><span class="sxs-lookup"><span data-stu-id="8682e-243">The **Hide Data URLs** checkbox</span></span>  
:::image-end:::  

## <span data-ttu-id="8682e-244">Sortieren von Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8682e-244">Sort requests</span></span>  

<span data-ttu-id="8682e-245">Standardmäßig werden die Anforderungen in der Tabelle Anforderungen nach Initiierungs Zeit sortiert, aber Sie können die Tabelle mit anderen Kriterien sortieren.</span><span class="sxs-lookup"><span data-stu-id="8682e-245">By default, the requests in the Requests table are sorted by initiation time, but you may sort the table using other criteria.</span></span>  

### <span data-ttu-id="8682e-246">Nach Spalte sortieren</span><span class="sxs-lookup"><span data-stu-id="8682e-246">Sort by column</span></span>  

<span data-ttu-id="8682e-247">Wählen Sie die Kopfzeile einer beliebigen Spalte in den Anforderungen aus, um Anforderungen nach dieser Spalte zu sortieren.</span><span class="sxs-lookup"><span data-stu-id="8682e-247">Choose the header of any column in the Requests to sort requests by that column.</span></span>  

### <span data-ttu-id="8682e-248">Nach Aktivitätsphase sortieren</span><span class="sxs-lookup"><span data-stu-id="8682e-248">Sort by activity phase</span></span>  

<span data-ttu-id="8682e-249">Wenn Sie ändern möchten, wie der Wasserfall Anforderungen sortiert, zeigen Sie auf die Kopfzeile der Tabelle Anforderungen, öffnen Sie das Kontextmenü \ (Klicken Sie mit der rechten Maustaste auf \), zeigen Sie auf **Wasserfall**, und wählen Sie eine der folgenden Optionen aus.</span><span class="sxs-lookup"><span data-stu-id="8682e-249">To change how the Waterfall sorts requests, hover on the header of the Requests table, open the contextual menu \(right-click\), hover on **Waterfall**, and choose one of the following options.</span></span>  

:::row:::
   :::column span="1":::
      **<span data-ttu-id="8682e-250">Startzeit</span><span class="sxs-lookup"><span data-stu-id="8682e-250">Start Time</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="8682e-251">Die erste Anforderung, die initiiert wurde, ist oben.</span><span class="sxs-lookup"><span data-stu-id="8682e-251">The first request that was initiated is at the top.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="8682e-252">Antwortzeit</span><span class="sxs-lookup"><span data-stu-id="8682e-252">Response Time</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="8682e-253">Die erste Anforderung, die den Download begonnen hat, ist ganz oben.</span><span class="sxs-lookup"><span data-stu-id="8682e-253">The first request that started downloading is at the top.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="8682e-254">Endzeit</span><span class="sxs-lookup"><span data-stu-id="8682e-254">End Time</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="8682e-255">Die erste abgeschlossene Anforderung ist oben.</span><span class="sxs-lookup"><span data-stu-id="8682e-255">The first request that finished is at the top.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="8682e-256">Gesamtdauer</span><span class="sxs-lookup"><span data-stu-id="8682e-256">Total Duration</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="8682e-257">Die Anforderung mit den kürzesten Verbindungseinstellungen und der Anforderung oder Antwort ist oben.</span><span class="sxs-lookup"><span data-stu-id="8682e-257">The request with the shortest connection settings and request or response is at the top.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="8682e-258">Latenz</span><span class="sxs-lookup"><span data-stu-id="8682e-258">Latency</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="8682e-259">Die Anforderung, die die kürzeste Zeit für eine Antwort gewartet hat, ist oben.</span><span class="sxs-lookup"><span data-stu-id="8682e-259">The request that waited the shortest time for a response is at the top.</span></span>  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="8682e-260">Bei diesen Beschreibungen wird davon ausgegangen, dass die jeweilige Option von kürzester bis längster Position bewertet wird.</span><span class="sxs-lookup"><span data-stu-id="8682e-260">These descriptions assume that each respective option is ranked from shortest to longest.</span></span>  <span data-ttu-id="8682e-261">Wählen Sie die Kopfzeile der Spalte **Wasserfall** aus, um die Reihenfolge umzukehren.</span><span class="sxs-lookup"><span data-stu-id="8682e-261">Choose the header of the **Waterfall** column to reverse the order.</span></span>  

:::image type="complex" source="../media/network-network-waterfall-total-duration.msft.png" alt-text="Sortieren des Wasserfalls nach Gesamtdauer" lightbox="../media/network-network-waterfall-total-duration.msft.png":::
   <span data-ttu-id="8682e-263">Sortieren des Wasserfalls nach Gesamtdauer \ (der leichtere Teil der einzelnen Balken ist die Zeit, die gewartet wird, und der dunklere Teil ist die Zeit, die zum Herunterladen von Bytes verwendet wird \)</span><span class="sxs-lookup"><span data-stu-id="8682e-263">Sort the Waterfall by total duration  \(The lighter portion of each bar is time spent waiting and the darker portion is time spent downloading bytes\)</span></span>  
:::image-end:::  

## <span data-ttu-id="8682e-264">Analysieren von Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8682e-264">Analyze requests</span></span>  

<span data-ttu-id="8682e-265">Solange devtools geöffnet sind, werden alle Anforderungen im **Netzwerk** Panel protokolliert.</span><span class="sxs-lookup"><span data-stu-id="8682e-265">So long as DevTools are open, it logs all requests in the **Network** panel.</span></span>  
<span data-ttu-id="8682e-266">Verwenden Sie das Netzwerk Panel, um Anforderungen zu analysieren.</span><span class="sxs-lookup"><span data-stu-id="8682e-266">Use the Network panel to analyze requests.</span></span>  

### <span data-ttu-id="8682e-267">Anzeigen eines Protokolls der Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8682e-267">Display a log of requests</span></span>  

<span data-ttu-id="8682e-268">Verwenden Sie die Tabelle "Anforderungen", um ein Protokoll aller Anforderungen anzuzeigen, die während der devtools geöffnet wurden.</span><span class="sxs-lookup"><span data-stu-id="8682e-268">Use the Requests table to display a log of all requests made while DevTools have been open.</span></span>  <span data-ttu-id="8682e-269">Wenn Sie weitere Informationen zu den einzelnen Elementen sehen möchten, wählen oder zeigen Sie auf Anfragen.</span><span class="sxs-lookup"><span data-stu-id="8682e-269">To reveals more information about each item, choose or hover on requests.</span></span>  

:::image type="complex" source="../media/network-network-requests-table.msft.png" alt-text="Die Tabelle "Anforderungen"" lightbox="../media/network-network-requests-table.msft.png":::
   <span data-ttu-id="8682e-271">Die Tabelle "Anforderungen"</span><span class="sxs-lookup"><span data-stu-id="8682e-271">The Requests table</span></span>  
:::image-end:::  

<span data-ttu-id="8682e-272">In der Tabelle Anforderungen werden standardmäßig die folgenden Spalten angezeigt.</span><span class="sxs-lookup"><span data-stu-id="8682e-272">The Requests table displays the following columns by default.</span></span>  

:::row:::
   :::column span="1":::
      **<span data-ttu-id="8682e-273">Name</span><span class="sxs-lookup"><span data-stu-id="8682e-273">Name</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="8682e-274">Der Dateiname von oder ein Bezeichner für die Ressource.</span><span class="sxs-lookup"><span data-stu-id="8682e-274">The filename of, or an identifier for, the resource.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="8682e-275">Status</span><span class="sxs-lookup"><span data-stu-id="8682e-275">Status</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="8682e-276">Der HTTP-Statuscode.</span><span class="sxs-lookup"><span data-stu-id="8682e-276">The HTTP status code.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="8682e-277">Typ</span><span class="sxs-lookup"><span data-stu-id="8682e-277">Type</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="8682e-278">Der MIME-Typ der angeforderten Ressource.</span><span class="sxs-lookup"><span data-stu-id="8682e-278">The MIME type of the requested resource.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="8682e-279">Initiator</span><span class="sxs-lookup"><span data-stu-id="8682e-279">Initiator</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="8682e-280">Die folgenden Objekte oder Prozesse initiieren Anforderungen.</span><span class="sxs-lookup"><span data-stu-id="8682e-280">The following objects or processes initiate requests.</span></span>  
      
      *   <span data-ttu-id="8682e-281">**Parser**  Der HTML-Parser für Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="8682e-281">**Parser**  The HTML parser for Microsoft Edge.</span></span>  
      *   <span data-ttu-id="8682e-282">**Umleitung**  Eine HTTP-Umleitung.</span><span class="sxs-lookup"><span data-stu-id="8682e-282">**Redirect**  An HTTP redirect.</span></span>  
      *   <span data-ttu-id="8682e-283">**Skript**  Eine JavaScript-Funktion.</span><span class="sxs-lookup"><span data-stu-id="8682e-283">**Script**  A JavaScript function.</span></span>  
      *   <span data-ttu-id="8682e-284">**Andere**  Personen  Einige andere Prozesse oder Aktionen, wie das Navigieren zu einer Seite mithilfe eines Links oder das Eingeben einer URL in der Adressleiste.</span><span class="sxs-lookup"><span data-stu-id="8682e-284">**Other**  Some other process or action, such as navigating to a page using a link or entering a URL in the address bar.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="8682e-285">Size</span><span class="sxs-lookup"><span data-stu-id="8682e-285">Size</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="8682e-286">Die kombinierte Größe der Antwortheader sowie des Antworttexts, wie vom Server bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="8682e-286">The combined size of the response headers plus the response body, as delivered by the server.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="8682e-287">Zeit</span><span class="sxs-lookup"><span data-stu-id="8682e-287">Time</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="8682e-288">Die Gesamtdauer vom Anfang der Anforderung bis zum Empfang des letzten Bytes in der Antwort.</span><span class="sxs-lookup"><span data-stu-id="8682e-288">The total duration, from the start of the request to the receipt of the final byte in the response.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [<span data-ttu-id="8682e-289">Wasserfall</span><span class="sxs-lookup"><span data-stu-id="8682e-289">Waterfall</span></span>](#display-the-timing-relationship-of-requests)  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="8682e-290">Eine visuelle Gliederung der Aktivität für jede Anforderung.</span><span class="sxs-lookup"><span data-stu-id="8682e-290">A visual breakdown of the activity for each request.</span></span>  
   :::column-end:::
:::row-end:::  

#### <span data-ttu-id="8682e-291">Hinzufügen oder Entfernen von Spalten</span><span class="sxs-lookup"><span data-stu-id="8682e-291">Add or remove columns</span></span>  

<span data-ttu-id="8682e-292">Zeigen Sie auf die Kopfzeile der Tabelle Anforderungen, öffnen Sie das Kontextmenü \ (Klicken Sie mit der rechten Maustaste auf \), und wählen Sie eine Option aus, um sie auszublenden oder anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="8682e-292">Hover on the header of the Requests table, open the contextual menu \(right-click\), and choose an option to hide or show it.</span></span>  <span data-ttu-id="8682e-293">Die aktuell angezeigten Optionen verfügen über Kontrollkästchen neben den einzelnen Elementen.</span><span class="sxs-lookup"><span data-stu-id="8682e-293">Currently displayed options have checkmarks next to each item.</span></span>  

:::image type="complex" source="../media/network-network-requests-add-column.msft.png" alt-text="Hinzufügen einer Spalte zur Tabelle "Anforderungen"" lightbox="../media/network-network-requests-add-column.msft.png":::
   <span data-ttu-id="8682e-295">Hinzufügen einer Spalte zur Tabelle "Anforderungen"</span><span class="sxs-lookup"><span data-stu-id="8682e-295">Add a column to the Requests table</span></span>  
:::image-end:::  

#### <span data-ttu-id="8682e-296">Hinzufügen benutzerdefinierter Spalten</span><span class="sxs-lookup"><span data-stu-id="8682e-296">Add custom columns</span></span>  

<span data-ttu-id="8682e-297">Wenn Sie der Tabelle Anforderungen eine benutzerdefinierte Spalte hinzufügen möchten, zeigen Sie auf die Kopfzeile der Tabelle Anforderungen, öffnen Sie das Kontextmenü \ (Klicken Sie mit der rechten Maustaste auf \), und wählen Sie **Antwortheader**  >  **Verwalten von Kopfzeilen Spalten**aus.</span><span class="sxs-lookup"><span data-stu-id="8682e-297">To add a custom column to the Requests table, hover on the header of the Requests table, open the contextual menu \(right-click\), and choose **Response Headers** > **Manage Header Columns**.</span></span>  

:::image type="complex" source="../media/network-network-requests-add-custom.msft.png" alt-text="Hinzufügen einer benutzerdefinierten Spalte zur Tabelle "Anforderungen"" lightbox="../media/network-network-requests-add-custom.msft.png":::
   <span data-ttu-id="8682e-299">Hinzufügen einer benutzerdefinierten Spalte zur Tabelle "Anforderungen"</span><span class="sxs-lookup"><span data-stu-id="8682e-299">Add a custom column to the Requests table</span></span>  
:::image-end:::  

### <span data-ttu-id="8682e-300">Anzeigen der Zeit Steuerungsbeziehung von Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8682e-300">Display the timing relationship of requests</span></span>  

<span data-ttu-id="8682e-301">Verwenden Sie den Wasserfall, um die Timing-Beziehungen von Anforderungen anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="8682e-301">Use the Waterfall to display the timing relationships of requests.</span></span>  
<span data-ttu-id="8682e-302">Die Standardorganisation des Wasserfalls verwendet die Startzeit der Anforderungen.</span><span class="sxs-lookup"><span data-stu-id="8682e-302">The default organization of the Waterfall uses the start time of the requests.</span></span>  
<span data-ttu-id="8682e-303">Anforderungen, die weiter Links sind, wurden früher als die Anforderungen weiter rechts gestartet.</span><span class="sxs-lookup"><span data-stu-id="8682e-303">So, requests that are farther to the left started earlier than the requests that are farther to the right.</span></span>  

<span data-ttu-id="8682e-304">Wenn Sie die verschiedenen Möglichkeiten zum Sortieren des Wasserfalls überprüfen möchten, navigieren Sie zu nach [Aktivitätsphase sortieren](#sort-by-activity-phase).</span><span class="sxs-lookup"><span data-stu-id="8682e-304">To review the different ways that you may sort the Waterfall, navigate to [Sort by activity phase](#sort-by-activity-phase).</span></span>  

:::image type="complex" source="../media/network-network-requests-waterfall.msft.png" alt-text="Spalte "Wasserfall" im Bereich "Anforderungen"" lightbox="../media/network-network-requests-waterfall.msft.png":::
   <span data-ttu-id="8682e-306">Spalte "Wasserfall" im Bereich " **Anforderungen** "</span><span class="sxs-lookup"><span data-stu-id="8682e-306">The Waterfall column of the **Requests** pane</span></span>  
:::image-end:::  

<!-- ### Analyze the frames of a WebSocket Connection  -->

<!--To review the frames of a WebSocket connection, use the following steps.  

1.  Choose the URL of the WebSocket connection, under the **Name** column of the Requests table.  
1.  Choose the **Frames** tab.  The table shows the last 100 frames.  

To refresh the table, re-choose the name of the WebSocket connection under the **Name** column of the Requests table.  -->

<!--
:::image type="complex" source="../media/network-frames.msft.png" alt-text="The Frames tab" lightbox="../media/network-frames.msft.png":::
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

### <span data-ttu-id="8682e-307">Anzeigen einer Vorschau eines Antworttexts</span><span class="sxs-lookup"><span data-stu-id="8682e-307">Display a preview of a response body</span></span>  

<span data-ttu-id="8682e-308">Führen Sie die folgenden Schritte aus, um eine Vorschau eines Antworttexts anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="8682e-308">To display a preview of a response body, use the following steps.</span></span>  

1.  <span data-ttu-id="8682e-309">Wählen Sie die URL der Anforderung unter der Spalte **Name** der Tabelle Anforderungen aus.</span><span class="sxs-lookup"><span data-stu-id="8682e-309">Choose the URL of the request, under the **Name** column of the Requests table.</span></span>  
1.  <span data-ttu-id="8682e-310">Wählen Sie die Registerkarte **Vorschau** aus.</span><span class="sxs-lookup"><span data-stu-id="8682e-310">Choose the **Preview** tab.</span></span>  

<span data-ttu-id="8682e-311">Die Registerkarte Vorschau ist meist nützlich, um Bilder anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="8682e-311">The Preview tab is mostly useful to display images.</span></span>  

:::image type="complex" source="../media/network-network-resources-preview.msft.png" alt-text="Registerkarte "Vorschau"" lightbox="../media/network-network-resources-preview.msft.png":::
   <span data-ttu-id="8682e-313">Registerkarte " **Vorschau** "</span><span class="sxs-lookup"><span data-stu-id="8682e-313">The **Preview** tab</span></span>  
:::image-end:::  

### <span data-ttu-id="8682e-314">Anzeigen eines Antworttexts</span><span class="sxs-lookup"><span data-stu-id="8682e-314">Display a response body</span></span>  

<span data-ttu-id="8682e-315">Führen Sie die folgenden Schritte aus, um den Antworttext einer Anforderung anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="8682e-315">To display the response body to a request, use the following steps.</span></span>  

1.  <span data-ttu-id="8682e-316">Wählen Sie die URL der Anforderung unter der Spalte **Name** der Tabelle Anforderungen aus.</span><span class="sxs-lookup"><span data-stu-id="8682e-316">Choose the URL of the request, under the **Name** column of the Requests table.</span></span>  
1.  <span data-ttu-id="8682e-317">Wählen Sie die Registerkarte **Antwort** aus.</span><span class="sxs-lookup"><span data-stu-id="8682e-317">Choose the **Response** tab.</span></span>  

:::image type="complex" source="../media/network-network-resources-response.msft.png" alt-text="Die Registerkarte "Antwort"" lightbox="../media/network-network-resources-response.msft.png":::
   <span data-ttu-id="8682e-319">Die Registerkarte " **Antwort** "</span><span class="sxs-lookup"><span data-stu-id="8682e-319">The **Response** tab</span></span>  
:::image-end:::  

### <span data-ttu-id="8682e-320">Anzeigen von HTTP-Headern</span><span class="sxs-lookup"><span data-stu-id="8682e-320">Display HTTP headers</span></span>  

<span data-ttu-id="8682e-321">Führen Sie die folgenden Schritte aus, um HTTP-Header Daten zu einer Anforderung anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="8682e-321">To display HTTP header data about a request, use the following steps.</span></span>  

1.  <span data-ttu-id="8682e-322">Wählen Sie die URL der Anforderung unter der Spalte **Name** der Tabelle Anforderungen aus.</span><span class="sxs-lookup"><span data-stu-id="8682e-322">Choose the URL of the request, under the **Name** column of the Requests table.</span></span>  
1.  <span data-ttu-id="8682e-323">Wählen Sie die Registerkarte über **Schriften** aus.</span><span class="sxs-lookup"><span data-stu-id="8682e-323">Choose the **Headers** tab.</span></span>  

:::image type="complex" source="../media/network-resources-headers.msft.png" alt-text="Die Registerkarte "Überschriften"" lightbox="../media/network-resources-headers.msft.png":::
   <span data-ttu-id="8682e-325">Die Registerkarte "über **Schriften** "</span><span class="sxs-lookup"><span data-stu-id="8682e-325">The **Headers** tab</span></span>  
:::image-end:::  

#### <span data-ttu-id="8682e-326">Anzeigen der HTTP-Header Quelle</span><span class="sxs-lookup"><span data-stu-id="8682e-326">Display HTTP header source</span></span>  

<span data-ttu-id="8682e-327">Standardmäßig werden auf der Registerkarte Kopfzeilennamen in alphabetischer Reihenfolge angezeigt.</span><span class="sxs-lookup"><span data-stu-id="8682e-327">By default, the Headers tab shows header names alphabetically.</span></span>  <span data-ttu-id="8682e-328">Führen Sie die folgenden Schritte aus, um die HTTP-Headernamen in der empfangenen Reihenfolge Enddatum.</span><span class="sxs-lookup"><span data-stu-id="8682e-328">To dsiplay the HTTP header names in the order received, use the following steps.</span></span>  

1.  <span data-ttu-id="8682e-329">Öffnen Sie die Registerkarte über **Schriften** für die Anforderung, die Sie interessiert.</span><span class="sxs-lookup"><span data-stu-id="8682e-329">Open the **Headers** tab for the request that interests you.</span></span>  <span data-ttu-id="8682e-330">Weitere Informationen finden Sie unter [Anzeigen von HTTP-Kopfzeilen](#display-http-headers).</span><span class="sxs-lookup"><span data-stu-id="8682e-330">For more information, navigate to [Display HTTP headers](#display-http-headers).</span></span>  
1.  <span data-ttu-id="8682e-331">Wählen Sie **Quelle anzeigen**neben dem Abschnitt **Anforderungs Kopfzeile** oder **Antwort Kopf** aus.</span><span class="sxs-lookup"><span data-stu-id="8682e-331">Choose **view source**, next to the **Request Header** or **Response Header** section.</span></span>  

### <span data-ttu-id="8682e-332">Anzeigen von Abfragezeichenfolgenparametern</span><span class="sxs-lookup"><span data-stu-id="8682e-332">Display query string parameters</span></span>  

<span data-ttu-id="8682e-333">Führen Sie die folgenden Schritte aus, um die Abfragezeichenfolgenparameter einer URL in einem menschlich lesbaren Format anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="8682e-333">To display the query string parameters of a URL in a human-readable format, use the following steps.</span></span>  

1.  <span data-ttu-id="8682e-334">Öffnen Sie die Registerkarte über **Schriften** für die Anforderung, die Sie interessiert.</span><span class="sxs-lookup"><span data-stu-id="8682e-334">Open the **Headers** tab for the request that interests you.</span></span>  <span data-ttu-id="8682e-335">Weitere Informationen finden Sie unter [Anzeigen von HTTP-Kopfzeilen](#display-http-headers).</span><span class="sxs-lookup"><span data-stu-id="8682e-335">For more information, navigate to [Display HTTP headers](#display-http-headers).</span></span>  
1.  <span data-ttu-id="8682e-336">Wechseln Sie zum Abschnitt **Abfragezeichenfolgenparameter** .</span><span class="sxs-lookup"><span data-stu-id="8682e-336">Go to the **Query String Parameters** section.</span></span>  

:::image type="complex" source="../media/network-network-resources-headers-query-string-parameters.msft.png" alt-text="Der Abfragezeichenfolgenparameter Abschnitt" lightbox="../media/network-network-resources-headers-query-string-parameters.msft.png":::
   <span data-ttu-id="8682e-338">Der **Abfragezeichenfolgenparameter** Abschnitt</span><span class="sxs-lookup"><span data-stu-id="8682e-338">The **Query String Parameters** section</span></span>  
:::image-end:::  

#### <span data-ttu-id="8682e-339">Anzeigen der Parameterquelle für Abfragezeichenfolgen</span><span class="sxs-lookup"><span data-stu-id="8682e-339">Display query string parameters source</span></span>  

<span data-ttu-id="8682e-340">Führen Sie die folgenden Schritte aus, um die Abfragezeichenfolgenparameter Quelle einer Anforderung anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="8682e-340">To display the query string parameter source of a request, use the following steps.</span></span>  

1.  <span data-ttu-id="8682e-341">Wechseln Sie zum Abschnitt Abfragezeichenfolgenparameter.</span><span class="sxs-lookup"><span data-stu-id="8682e-341">Go to the Query String Parameters section.</span></span>  <span data-ttu-id="8682e-342">Weitere Informationen finden Sie unter [Anzeigen von Abfragezeichenfolgenparametern](#display-query-string-parameters).</span><span class="sxs-lookup"><span data-stu-id="8682e-342">For more information, navigate to [Display query string parameters](#display-query-string-parameters).</span></span>  
1.  <span data-ttu-id="8682e-343">Wählen Sie **Quelltext anzeigen**aus.</span><span class="sxs-lookup"><span data-stu-id="8682e-343">Choose **view source**.</span></span>  

#### <span data-ttu-id="8682e-344">Anzeigen von URL-codierten Abfragezeichenfolgenparametern</span><span class="sxs-lookup"><span data-stu-id="8682e-344">Display URL-encoded query string parameters</span></span>  

<span data-ttu-id="8682e-345">Führen Sie die folgenden Schritte aus, um Abfragezeichenfolgenparameter in einem menschlich lesbaren Format, jedoch mit erhaltenen Codierungen, anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="8682e-345">To display query string parameters in a human-readable format, but with encodings preserved, use the following steps.</span></span>  

1.  <span data-ttu-id="8682e-346">Wechseln Sie zum Abschnitt Abfragezeichenfolgenparameter.</span><span class="sxs-lookup"><span data-stu-id="8682e-346">Go to the Query String Parameters section.</span></span>  <span data-ttu-id="8682e-347">Weitere Informationen finden Sie unter [Anzeigen von Abfragezeichenfolgenparametern](#display-query-string-parameters).</span><span class="sxs-lookup"><span data-stu-id="8682e-347">For more information, navigate to [Display query string parameters](#display-query-string-parameters).</span></span>  
1.  <span data-ttu-id="8682e-348">Wählen Sie **View URL encoded**aus.</span><span class="sxs-lookup"><span data-stu-id="8682e-348">Choose **view URL encoded**.</span></span>  

### <span data-ttu-id="8682e-349">Anzeigen von Cookies</span><span class="sxs-lookup"><span data-stu-id="8682e-349">Display cookies</span></span>  

<span data-ttu-id="8682e-350">Führen Sie die folgenden Schritte aus, um die im HTTP-Header einer Anforderung gesendeten Cookies anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="8682e-350">To display the cookies sent in the HTTP header of a request, use the following steps.</span></span>  

1.  <span data-ttu-id="8682e-351">Wählen Sie die URL der Anforderung unter der Spalte **Name** der Tabelle Anforderungen aus.</span><span class="sxs-lookup"><span data-stu-id="8682e-351">Choose the URL of the request, under the **Name** column of the Requests table.</span></span>  
1.  <span data-ttu-id="8682e-352">Wählen Sie die Registerkarte **Cookies** aus.</span><span class="sxs-lookup"><span data-stu-id="8682e-352">Choose the **Cookies** tab.</span></span>  

<!--For more information about each of the columns, navigate to [Fields][ManageDataCookiesFields].  -->  

<!--[ManageDataCookiesFields]: manage-data/cookies#fields  -->  
<!--TODO: add link when section is available -->  

:::image type="complex" source="../media/network-network-resources-cookies.msft.png" alt-text="Die Registerkarte "Cookies"" lightbox="../media/network-network-resources-cookies.msft.png":::
   <span data-ttu-id="8682e-354">Die Registerkarte "Cookies"</span><span class="sxs-lookup"><span data-stu-id="8682e-354">The Cookies tab</span></span>  
:::image-end:::  

### <span data-ttu-id="8682e-355">Anzeigen der Zeit Plan Aufteilung einer Anforderung</span><span class="sxs-lookup"><span data-stu-id="8682e-355">Display the timing breakdown of a request</span></span>  

<span data-ttu-id="8682e-356">Führen Sie die folgenden Schritte aus, um die Anzeigedauer einer Anforderung anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="8682e-356">To display the timing breakdown of a request, use the following steps.</span></span>  

1.  <span data-ttu-id="8682e-357">Wählen Sie die URL der Anforderung unter der Spalte **Name** der Tabelle Anforderungen aus.</span><span class="sxs-lookup"><span data-stu-id="8682e-357">Choose the URL of the request, under the **Name** column of the Requests table.</span></span>  
1.  <span data-ttu-id="8682e-358">Wählen Sie die Registerkarte **Anzeige** Dauer aus.</span><span class="sxs-lookup"><span data-stu-id="8682e-358">Choose the **Timing** tab.</span></span>  

<span data-ttu-id="8682e-359">Um eine schnellere Möglichkeit für den Zugriff auf die Daten zu erhalten, navigieren Sie zu [Vorschau einer Anzeige](#preview-a-timing-breakdown)Dauer.</span><span class="sxs-lookup"><span data-stu-id="8682e-359">For a faster way to access the data, navigate to [Preview a timing breakdown](#preview-a-timing-breakdown).</span></span>  

<span data-ttu-id="8682e-360">Weitere Informationen zu den einzelnen Phasen, die möglicherweise auf der Registerkarte **Anzeige** Dauer angezeigt werden, finden Sie unter [erläuterte](#timing-breakdown-phases-explained)Phasen der Anzeigedauer.</span><span class="sxs-lookup"><span data-stu-id="8682e-360">For more information about each of the phases that may be displayed in the **Timing** tab, navigate to [Timing breakdown phases explained](#timing-breakdown-phases-explained).</span></span>  

:::image type="complex" source="../media/network-network-resources-timing.msft.png" alt-text="Registerkarte "Anzeigedauer"" lightbox="../media/network-network-resources-timing.msft.png":::
   <span data-ttu-id="8682e-362">Registerkarte " **Anzeige** Dauer"</span><span class="sxs-lookup"><span data-stu-id="8682e-362">The **Timing** tab</span></span>  
:::image-end:::  

<span data-ttu-id="8682e-363">Weitere Informationen zu den einzelnen Phasen.</span><span class="sxs-lookup"><span data-stu-id="8682e-363">More information about each of the phases.</span></span>  

<span data-ttu-id="8682e-364">Weitere Informationen zum Zugriff auf die Anzeige finden Sie unter [Aufschlüsselung](#display-the-timing-breakdown-of-a-request)der Anzeigedauer.</span><span class="sxs-lookup"><span data-stu-id="8682e-364">For more information about accessing the display, navigate to [Display timing breakdown](#display-the-timing-breakdown-of-a-request).</span></span>  

#### <span data-ttu-id="8682e-365">Anzeigen einer Vorschau einer Anzeigedauer</span><span class="sxs-lookup"><span data-stu-id="8682e-365">Preview a timing breakdown</span></span>  

<span data-ttu-id="8682e-366">Wenn Sie eine Vorschau der Zeit Plan Aufteilung einer Anforderung anzeigen möchten, zeigen Sie in der Spalte **Wasserfall** der Tabelle Anforderungen auf den Eintrag für die Anforderung.</span><span class="sxs-lookup"><span data-stu-id="8682e-366">To display a preview of the timing breakdown of a request, in the **Waterfall** column of the Requests table, hover on the entry for the request.</span></span>  

<span data-ttu-id="8682e-367">Wenn Sie weitere Informationen dazu benötigen, wie Sie auf die Daten zugreifen können, ohne die Maus zu zeigen, navigieren Sie zum [Anzeigen der Zeit Plan Verteilung einer Anforderung](#display-the-timing-breakdown-of-a-request).</span><span class="sxs-lookup"><span data-stu-id="8682e-367">For more information about how to access the data without hovering, navigate to [Display the timing breakdown of a request](#display-the-timing-breakdown-of-a-request).</span></span>  

:::image type="complex" source="../media/network-network-resources-waterfall-hover.msft.png" alt-text="> anzeigen einer Vorschau der Anzeigedauer einer Anforderung" lightbox="../media/network-network-resources-waterfall-hover.msft.png":::
   <span data-ttu-id="8682e-369">Anzeigen einer Vorschau der Anzeigedauer einer Anforderung</span><span class="sxs-lookup"><span data-stu-id="8682e-369">Preview the timing breakdown of a request</span></span>  
:::image-end:::  

#### <span data-ttu-id="8682e-370">Erläuterte Phasen Aufgliederungs Phasen</span><span class="sxs-lookup"><span data-stu-id="8682e-370">Timing breakdown phases explained</span></span>  

<span data-ttu-id="8682e-371">Weitere Informationen zu den einzelnen Phasen **, die auf der Registerkarte** Anzeigedauer angezeigt werden können.</span><span class="sxs-lookup"><span data-stu-id="8682e-371">More information about each of the phases that may display in the **Timing** tab.</span></span>  

:::row:::
   :::column span="1":::
      **<span data-ttu-id="8682e-372">Queueing</span><span class="sxs-lookup"><span data-stu-id="8682e-372">Queueing</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="8682e-373">Der Browser Warteschlangenanforderungen, wenn eine der folgenden Bedingungen erfüllt ist.</span><span class="sxs-lookup"><span data-stu-id="8682e-373">The browser queues requests when any of the following are true.</span></span>  
      
      *   <span data-ttu-id="8682e-374">Anforderungen mit höherer Priorität bestehen.</span><span class="sxs-lookup"><span data-stu-id="8682e-374">Higher priority requests exist.</span></span>  
      *   <span data-ttu-id="8682e-375">Sechs TCP-Verbindungen sind für denselben Ursprung geöffnet, was die Grenze ist.</span><span class="sxs-lookup"><span data-stu-id="8682e-375">Six TCP connections are open for the same origin, which is the limit.</span></span>  <span data-ttu-id="8682e-376">Gilt nur für HTTP/1.0 und HTTP/1.1.</span><span class="sxs-lookup"><span data-stu-id="8682e-376">Applies to HTTP/1.0 and HTTP/1.1 only.</span></span>  
      *   <span data-ttu-id="8682e-377">Der Browser reserviert kurzzeitig Speicherplatz im Datenträgercache.</span><span class="sxs-lookup"><span data-stu-id="8682e-377">The browser is briefly allocating space in the disk cache.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="8682e-378">Blockiert</span><span class="sxs-lookup"><span data-stu-id="8682e-378">Stalled</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="8682e-379">Die Anforderung wird aus den in der **Warteschlange**beschriebenen Gründen angehalten.</span><span class="sxs-lookup"><span data-stu-id="8682e-379">The request is stalled for any of the reasons described in **Queueing**.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="8682e-380">DNS-Lookup</span><span class="sxs-lookup"><span data-stu-id="8682e-380">DNS Lookup</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="8682e-381">Der Browser löst die IP-Adresse für die Anforderung auf.</span><span class="sxs-lookup"><span data-stu-id="8682e-381">The browser is resolving the IP address for the request.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="8682e-382">Anfängliche Verbindung</span><span class="sxs-lookup"><span data-stu-id="8682e-382">Initial connection</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="8682e-383">Der Browser stellt eine Verbindung her, einschließlich TCP-Handshakes, TCP-Wiederholungen und verhandelt eine sichere Socketebene.</span><span class="sxs-lookup"><span data-stu-id="8682e-383">The browser establishes a connection including TCP handshakes, TCP retries, and negotiates a Secure Socket Layer.</span></span>
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="8682e-384">Proxy Verhandlung</span><span class="sxs-lookup"><span data-stu-id="8682e-384">Proxy negotiation</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="8682e-385">Der Browser verhandelt die Anforderung mit einem [Proxy Server][WikiProxyServer].</span><span class="sxs-lookup"><span data-stu-id="8682e-385">The browser is negotiating the request with a [proxy server][WikiProxyServer].</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="8682e-386">Anfrage gesendet</span><span class="sxs-lookup"><span data-stu-id="8682e-386">Request sent</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="8682e-387">Die Anfrage wird gesendet.</span><span class="sxs-lookup"><span data-stu-id="8682e-387">The request is being sent.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="8682e-388">ServiceWorker-Vorbereitung</span><span class="sxs-lookup"><span data-stu-id="8682e-388">ServiceWorker Preparation</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="8682e-389">Der Browser startet den Dienstmitarbeiter.</span><span class="sxs-lookup"><span data-stu-id="8682e-389">The browser is starting the service worker.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="8682e-390">Anforderung an ServiceWorker</span><span class="sxs-lookup"><span data-stu-id="8682e-390">Request to ServiceWorker</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="8682e-391">Die Anforderung wird an den Dienstmitarbeiter gesendet.</span><span class="sxs-lookup"><span data-stu-id="8682e-391">The request is being sent to the service worker.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="8682e-392">Waiting \ (TTFB \)</span><span class="sxs-lookup"><span data-stu-id="8682e-392">Waiting \(TTFB\)</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="8682e-393">Der Browser wartet auf das erste Byte einer Antwort.</span><span class="sxs-lookup"><span data-stu-id="8682e-393">The browser is waiting for the first byte of a response.</span></span>  <span data-ttu-id="8682e-394">TTFB steht für Time to First Byte.</span><span class="sxs-lookup"><span data-stu-id="8682e-394">TTFB stands for Time To First Byte.</span></span>  <span data-ttu-id="8682e-395">Dieser Zeitpunkt umfasst eine Roundtrip-Wartezeit und die Zeitdauer, die der Server zum Vorbereiten der Antwort benötigte.</span><span class="sxs-lookup"><span data-stu-id="8682e-395">This timing includes one round trip of latency and the time the server took to prepare the response.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="8682e-396">Herunterladen von Inhalten</span><span class="sxs-lookup"><span data-stu-id="8682e-396">Content Download</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="8682e-397">Der Browser empfängt die Antwort.</span><span class="sxs-lookup"><span data-stu-id="8682e-397">The browser is receiving the response.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="8682e-398">Empfangen von Push</span><span class="sxs-lookup"><span data-stu-id="8682e-398">Receiving Push</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="8682e-399">Der Browser empfängt Daten für diese Antwort über http/2 Server Push.</span><span class="sxs-lookup"><span data-stu-id="8682e-399">The browser is receiving data for this response via HTTP/2 Server Push.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="8682e-400">Lese Push</span><span class="sxs-lookup"><span data-stu-id="8682e-400">Reading Push</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="8682e-401">Der Browser liest die zuvor empfangenen lokalen Daten.</span><span class="sxs-lookup"><span data-stu-id="8682e-401">The browser is reading the local data previously received.</span></span>  
   :::column-end:::
:::row-end:::  

### <span data-ttu-id="8682e-402">Anzeigen von Initiatoren und Abhängigkeiten</span><span class="sxs-lookup"><span data-stu-id="8682e-402">Display initiators and dependencies</span></span>  

<span data-ttu-id="8682e-403">Wenn Sie die Initiatoren und Abhängigkeiten einer Anforderung anzeigen möchten, halten Sie `Shift` die Anforderung in der Tabelle Anforderungen gedrückt, und zeigen Sie darauf.</span><span class="sxs-lookup"><span data-stu-id="8682e-403">To display the initiators and dependencies of a request, hold `Shift`and hover on the request in the Requests table.</span></span>  <span data-ttu-id="8682e-404">DevTools Farben: Initiatoren werden in grün angezeigt, und Abhängigkeiten werden in rot angezeigt.</span><span class="sxs-lookup"><span data-stu-id="8682e-404">DevTools colors: initiators are shown in green and dependencies are shown in red.</span></span>  

:::image type="complex" source="../media/network-network-resources-initiators-dependencies.msft.png" alt-text="Anzeigen der Initiatoren und Abhängigkeiten einer Anforderung" lightbox="../media/network-network-resources-initiators-dependencies.msft.png":::
   <span data-ttu-id="8682e-406">Anzeigen der Initiatoren und Abhängigkeiten einer Anforderung</span><span class="sxs-lookup"><span data-stu-id="8682e-406">Display the initiators and dependencies of a request</span></span>  
:::image-end:::  

<span data-ttu-id="8682e-407">Wenn die Anforderungstabelle chronologisch geordnet ist, wenn Sie auf eine Zeile zeigen, wird in der davor liegenden Zeile eine grüne Anforderung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="8682e-407">When the Requests table is ordered chronologically, if you hover on a line, the line preceding it displays a green request.</span></span>  <span data-ttu-id="8682e-408">Die grüne Anforderung ist der Initiator der Abhängigkeit.</span><span class="sxs-lookup"><span data-stu-id="8682e-408">The green request is the initiator of the dependency.</span></span>  <span data-ttu-id="8682e-409">Wenn zuvor eine andere grüne Anforderung in der Zeile angezeigt wird, ist diese höhere Anforderung der Initiator des Initiators.</span><span class="sxs-lookup"><span data-stu-id="8682e-409">If another green request is displayed on the line before that, that higher request is the initiator of the initiator.</span></span>  <span data-ttu-id="8682e-410">Und so weiter.</span><span class="sxs-lookup"><span data-stu-id="8682e-410">And so on.</span></span>  

### <span data-ttu-id="8682e-411">Laden Ereignisse anzeigen</span><span class="sxs-lookup"><span data-stu-id="8682e-411">Display load events</span></span>  

<span data-ttu-id="8682e-412">DevTools zeigt die Anzeigedauer der `DOMContentLoaded` `load` Ereignisse und Ereignisse an mehreren Stellen im **Netzwerk** Panel an.</span><span class="sxs-lookup"><span data-stu-id="8682e-412">DevTools displays the timing of the `DOMContentLoaded` and `load` events in multiple places on the **Network** panel.</span></span>  <span data-ttu-id="8682e-413">Das `DOMContentLoaded` Ereignis ist blau gefärbt, und das `load` Ereignis ist rot.</span><span class="sxs-lookup"><span data-stu-id="8682e-413">The `DOMContentLoaded` event is colored blue, and the `load` event is red.</span></span>  

:::image type="complex" source="../media/network-network-requests-load-events.msft.png" alt-text="Die Speicherorte der DOMContentLoaded-und Load-Ereignisse im Netzwerk Panel" lightbox="../media/network-network-requests-load-events.msft.png":::
   <span data-ttu-id="8682e-415">Die Speicherorte der `DOMContentLoaded` und- `load` Ereignisse im **Netzwerk** Panel</span><span class="sxs-lookup"><span data-stu-id="8682e-415">The locations of the `DOMContentLoaded` and `load` events on the **Network** panel</span></span>  
:::image-end:::  

### <span data-ttu-id="8682e-416">Anzeigen der Gesamtzahl der Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8682e-416">Display the total number of requests</span></span>  

<span data-ttu-id="8682e-417">Die Gesamtzahl der Anforderungen wird im Bereich " **Zusammenfassung** " unten im **Netzwerk** Bereich aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="8682e-417">The total number of requests is listed in the **Summary** pane, at the bottom of the **Network** panel.</span></span>  

> [!CAUTION]
> <span data-ttu-id="8682e-418">Diese Nummer verfolgt nur Anforderungen, die seit dem Öffnen von devtools protokolliert wurden.</span><span class="sxs-lookup"><span data-stu-id="8682e-418">This number only tracks requests that have been logged since DevTools was opened.</span></span>  <span data-ttu-id="8682e-419">Wenn vor dem Öffnen von devtools andere Anforderungen aufgetreten sind, werden diese Anforderungen nicht gezählt.</span><span class="sxs-lookup"><span data-stu-id="8682e-419">If other requests occurred before DevTools was opened, those requests are not counted.</span></span>  

:::image type="complex" source="../media/network-network-total-requests.msft.png" alt-text="Die Gesamtzahl der Anforderungen seit dem Öffnen von devtools" lightbox="../media/network-network-total-requests.msft.png":::
   <span data-ttu-id="8682e-421">Die Gesamtzahl der Anforderungen seit dem Öffnen von devtools</span><span class="sxs-lookup"><span data-stu-id="8682e-421">The total number of requests since DevTools were opened</span></span>  
:::image-end:::  

### <span data-ttu-id="8682e-422">Anzeigen der Gesamtgröße des Downloads</span><span class="sxs-lookup"><span data-stu-id="8682e-422">Display the total download size</span></span>  

<span data-ttu-id="8682e-423">Die Gesamtgröße der Downloadanforderungen wird im Bereich " **Zusammenfassung** " am unteren Rand des **Netzwerk** Bereichs angezeigt.</span><span class="sxs-lookup"><span data-stu-id="8682e-423">The total download size of requests is listed in the **Summary** pane, at the bottom of the **Network** panel.</span></span>  

> [!CAUTION]
> <span data-ttu-id="8682e-424">Diese Nummer verfolgt nur Anforderungen, die seit dem Öffnen von devtools protokolliert wurden.</span><span class="sxs-lookup"><span data-stu-id="8682e-424">This number only tracks requests that have been logged since DevTools was opened.</span></span>  <span data-ttu-id="8682e-425">Wenn vor dem Öffnen von devtools andere Anforderungen aufgetreten sind, werden die vorherigen Anforderungen nicht gezählt.</span><span class="sxs-lookup"><span data-stu-id="8682e-425">If other requests occurred before DevTools was opened, the previous requests are not counted.</span></span>  

:::image type="complex" source="../media/network-network-total-download-size.msft.png" alt-text="Die Gesamtgröße der Downloads von Anforderungen" lightbox="../media/network-network-total-download-size.msft.png":::
   <span data-ttu-id="8682e-427">Die Gesamtgröße der Downloads von Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8682e-427">The total download size of requests</span></span>  
:::image-end:::  

<span data-ttu-id="8682e-428">Navigieren Sie zum [Anzeigen der unkomprimierten Größe einer Ressource](#display-the-uncompressed-size-of-a-resource), um zu überprüfen, wie umfangreiche Ressourcen sind, nachdem der Browser die einzelnen Elemente dekomprimiert hat.</span><span class="sxs-lookup"><span data-stu-id="8682e-428">To verify how large resources are after the browser uncompresses each item, navigate to [display the uncompressed size of a resource](#display-the-uncompressed-size-of-a-resource).</span></span>  

### <span data-ttu-id="8682e-429">Anzeigen der Stapelüberwachung, die eine Anforderung verursacht hat</span><span class="sxs-lookup"><span data-stu-id="8682e-429">Display the stack trace that caused a request</span></span>  

<span data-ttu-id="8682e-430">Nachdem eine JavaScript-Anweisung eine Ressource angefordert hat, zeigen Sie auf die Spalte **Initiator** , um die Stapelüberwachung anzuzeigen, die zur Anforderung führt.</span><span class="sxs-lookup"><span data-stu-id="8682e-430">After a JavaScript statement requests a resource, hover on the **Initiator** column to display the stack trace leading up to the request.</span></span>  

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
   <span data-ttu-id="8682e-432">Die Stapelüberwachung, die zu einer Ressourcenanforderung führt</span><span class="sxs-lookup"><span data-stu-id="8682e-432">The stack trace leading up to a resource request</span></span>  
:::image-end:::  

### <span data-ttu-id="8682e-433">Anzeigen der unkomprimierten Größe einer Ressource</span><span class="sxs-lookup"><span data-stu-id="8682e-433">Display the uncompressed size of a resource</span></span>  

<span data-ttu-id="8682e-434">Aktivieren Sie das Kontrollkästchen **große Anforderungs Zeilen verwenden** , und überprüfen Sie dann den niedrigsten Wert der Spalte **Größe** .</span><span class="sxs-lookup"><span data-stu-id="8682e-434">Turn on the **Use large request rows** checkbox and then review the bottom value of the **Size** column.</span></span>  

:::image type="complex" source="../media/network-network-requests-uncompressed-compare.msft.png" alt-text="Beispiel für nicht komprimierte Ressourcen" lightbox="../media/network-network-requests-uncompressed-compare.msft.png":::
   <span data-ttu-id="8682e-436">Ein Beispiel für unkomprimierte Ressourcen \ (die komprimierte Größe der `jquery-3.3.1.min.js` Datei, die über das Netzwerk gesendet wurde `29.9 KB` , während die unkomprimierte Größe `84.9 KB` \) war</span><span class="sxs-lookup"><span data-stu-id="8682e-436">An example of uncompressed resources  \(The compressed size of the `jquery-3.3.1.min.js` file that was sent over the network was `29.9 KB`, whereas the uncompressed size was `84.9 KB`\)</span></span>  
:::image-end:::  

## <span data-ttu-id="8682e-437">Exportieren von Anforderungsdaten</span><span class="sxs-lookup"><span data-stu-id="8682e-437">Export requests data</span></span>  

### <span data-ttu-id="8682e-438">Speichern aller Netzwerkanforderungen in einer har-Datei</span><span class="sxs-lookup"><span data-stu-id="8682e-438">Save all network requests to a HAR file</span></span>  

<span data-ttu-id="8682e-439">Führen Sie die folgenden Schritte aus, um alle Netzwerkanforderungen in einer har-Datei zu speichern.</span><span class="sxs-lookup"><span data-stu-id="8682e-439">To save all network requests to a HAR file, complete the following steps.</span></span>  

1.  <span data-ttu-id="8682e-440">Zeigen Sie auf jede Anforderung in der Tabelle Anforderungen, und öffnen Sie das Kontextmenü \ (mit der rechten Maustaste auf \).</span><span class="sxs-lookup"><span data-stu-id="8682e-440">Hover on any request in the Requests table and open the contextual menu \(right-click\).</span></span>  
1.  <span data-ttu-id="8682e-441">Wählen Sie **als har mit Inhalt speichern**aus.</span><span class="sxs-lookup"><span data-stu-id="8682e-441">Choose **Save as HAR with Content**.</span></span>  <span data-ttu-id="8682e-442">DevTools speichert alle Anforderungen, die seit dem Öffnen von devtools in der har-Datei aufgetreten sind.</span><span class="sxs-lookup"><span data-stu-id="8682e-442">DevTools saves all requests that have occurred since you opened DevTools to the HAR file.</span></span>  <span data-ttu-id="8682e-443">Sie können keine Anforderungen filtern.</span><span class="sxs-lookup"><span data-stu-id="8682e-443">You are not able to filter requests.</span></span>  <span data-ttu-id="8682e-444">Sie können auch keine einzelne Anfrage speichern.</span><span class="sxs-lookup"><span data-stu-id="8682e-444">You are also not able to save a single request.</span></span>  

<span data-ttu-id="8682e-445">Nachdem Sie eine har-Datei gespeichert haben, können Sie Sie für die Analyse wieder in devtools importieren.</span><span class="sxs-lookup"><span data-stu-id="8682e-445">Once you save a HAR file, you may import it back into DevTools for analysis.</span></span>  <span data-ttu-id="8682e-446">Ziehen Sie die har-Datei einfach per Drag & Drop in die Tabelle "Anforderungen".</span><span class="sxs-lookup"><span data-stu-id="8682e-446">Just drag-and-drop the HAR file into the Requests table.</span></span>  
<!--For more information, navigate to also [HAR Analyzer][HARAnalyzer].  -->  

<!--[HARAnalyzer]: https://toolbox.alphabetapps.com/apps/har_analyzer  -->  
<!--Todo: add section link when content is available  -->  

:::image type="complex" source="../media/network-network-requests-save-har-content.msft.png" alt-text="Auswählen von "als har mit Inhalt speichern"" lightbox="../media/network-network-requests-save-har-content.msft.png":::
   <span data-ttu-id="8682e-448">Auswählen **von "als har mit Inhalt speichern** "</span><span class="sxs-lookup"><span data-stu-id="8682e-448">Choose **Save as HAR with Content**</span></span>  
:::image-end:::  

### <span data-ttu-id="8682e-449">Kopieren einer oder mehrerer Anforderungen in die Zwischenablage</span><span class="sxs-lookup"><span data-stu-id="8682e-449">Copy one or more requests to the clipboard</span></span>  

<span data-ttu-id="8682e-450">Zeigen Sie unter der Spalte **Name** der Tabelle Anforderungen auf eine Anforderung, öffnen Sie das Kontextmenü \ (Klicken Sie mit der rechten Maustaste auf \), zeigen Sie auf **Kopieren**, und wählen Sie eine der folgenden Optionen aus.</span><span class="sxs-lookup"><span data-stu-id="8682e-450">Under the **Name** column of the Requests table, hover on a request, open the contextual menu \(right-click\), hover on **Copy**, and choose one of the following options.</span></span>  

| <span data-ttu-id="8682e-451">Name</span><span class="sxs-lookup"><span data-stu-id="8682e-451">Name</span></span> | <span data-ttu-id="8682e-452">Details</span><span class="sxs-lookup"><span data-stu-id="8682e-452">Details</span></span> |  
|:--- |:--- |  
| **<span data-ttu-id="8682e-453">Link Adresse kopieren</span><span class="sxs-lookup"><span data-stu-id="8682e-453">Copy Link Address</span></span>** | <span data-ttu-id="8682e-454">Kopieren Sie die URL der Anforderung in die Zwischenablage.</span><span class="sxs-lookup"><span data-stu-id="8682e-454">Copy the URL of the request to the clipboard.</span></span> |  
| **<span data-ttu-id="8682e-455">Antwort kopieren</span><span class="sxs-lookup"><span data-stu-id="8682e-455">Copy Response</span></span>** | <span data-ttu-id="8682e-456">Kopieren Sie den Antworttext in die Zwischenablage.</span><span class="sxs-lookup"><span data-stu-id="8682e-456">Copy the response body to the clipboard.</span></span> |  
| **<span data-ttu-id="8682e-457">Als FETCH kopieren</span><span class="sxs-lookup"><span data-stu-id="8682e-457">Copy as Fetch</span></span>** | &nbsp; |  
| **<span data-ttu-id="8682e-458">Als curl kopieren</span><span class="sxs-lookup"><span data-stu-id="8682e-458">Copy as cURL</span></span>** | <span data-ttu-id="8682e-459">Kopieren Sie die Anforderung als curl-Befehl.</span><span class="sxs-lookup"><span data-stu-id="8682e-459">Copy the request as a cURL command.</span></span> |  
| **<span data-ttu-id="8682e-460">Alle als FETCH kopieren</span><span class="sxs-lookup"><span data-stu-id="8682e-460">Copy All as Fetch</span></span>** | &nbsp; |  
| **<span data-ttu-id="8682e-461">Alle als curl kopieren</span><span class="sxs-lookup"><span data-stu-id="8682e-461">Copy All as cURL</span></span>** | <span data-ttu-id="8682e-462">Kopieren Sie alle Anforderungen als eine Kette von curl-Befehlen.</span><span class="sxs-lookup"><span data-stu-id="8682e-462">Copy all requests as a chain of cURL commands.</span></span> |  
| **<span data-ttu-id="8682e-463">Alle als har kopieren</span><span class="sxs-lookup"><span data-stu-id="8682e-463">Copy All as HAR</span></span>** | <span data-ttu-id="8682e-464">Kopieren Sie alle Anforderungen als har-Daten.</span><span class="sxs-lookup"><span data-stu-id="8682e-464">Copy all requests as HAR data.</span></span> |  

<!--
:::row:::
   :::column span="1":::
      **Copy Link Address**  
   :::column-end:::
   :::column span="2":::
      Copy the URL of the request to the clipboard.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Copy Response**  
   :::column-end:::
   :::column span="2":::
      Copy the response body to the clipboard.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Copy as Fetch**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Copy as cURL**  
   :::column-end:::
   :::column span="2":::
      Copy the request as a cURL command.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Copy All as Fetch**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Copy All as cURL**  
   :::column-end:::
   :::column span="2":::
      Copy all requests as a chain of cURL commands.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Copy All as HAR**  
   :::column-end:::
   :::column span="2":::
      Copy all requests as HAR data.  
   :::column-end:::
:::row-end:::  
-->  

:::image type="complex" source="../media/network-network-requests-copy-response.msft.png" alt-text="Wählen Sie Antwort kopieren aus." lightbox="../media/network-network-requests-copy-response.msft.png":::
   <span data-ttu-id="8682e-466">Wählen Sie **Antwort kopieren** aus.</span><span class="sxs-lookup"><span data-stu-id="8682e-466">Choose **Copy Response**</span></span>  
:::image-end:::  

### <span data-ttu-id="8682e-467">Kopieren der formatierten Antwort JSON in die Zwischenablage</span><span class="sxs-lookup"><span data-stu-id="8682e-467">Copy formatted response JSON to the clipboard</span></span>  

<span data-ttu-id="8682e-468">Wählen Sie eine Netzwerkanforderung aus, und navigieren Sie zum Bereich über **Schriften** .</span><span class="sxs-lookup"><span data-stu-id="8682e-468">Choose a network request and navigate to the **Headers** pane.</span></span>  <span data-ttu-id="8682e-469">Wenn Sie den JSON-Wert einer Antwort kopieren möchten, navigieren Sie zu **Anforderungsnutzlast**, zeigen Sie auf den JSON-Antwortinhalt, öffnen Sie das Kontextmenü \ (Klicken Sie mit der rechten Maustaste auf \), und wählen Sie **Wert kopieren**aus.</span><span class="sxs-lookup"><span data-stu-id="8682e-469">To copy the JSON value of a response, navigate to **Request payload**, hover on the JSON response content, open the contextual menu \(right-click\), and choose **Copy Value**.</span></span>  

:::row:::
   :::column span="":::
        :::image type="complex" source="../media/network-header-copy-property-value.msft.png" alt-text="Wert im Kontextmenü Kopieren" lightbox="../media/network-header-copy-property-value.msft.png":::
          <span data-ttu-id="8682e-471">**Wert** im Kontextmenü Kopieren</span><span class="sxs-lookup"><span data-stu-id="8682e-471">**Copy Value** in contextual menu</span></span>  
        :::image-end:::  
   :::column-end:::
   :::column span="":::
        :::image type="complex" source="../media/network-header-paste-property-value.msft.png" alt-text="Visual Studio-Code mit JSON für formatierte Antwort" lightbox="../media/network-header-paste-property-value.msft.png":::
          <span data-ttu-id="8682e-473">Einfügen einer formatierten Antwort JSON in Visual Studio-Code</span><span class="sxs-lookup"><span data-stu-id="8682e-473">Pasting formatted response JSON in Visual Studio Code</span></span>  
        :::image-end:::  
   :::column-end:::
:::row-end:::  

### <span data-ttu-id="8682e-474">Kopieren von Eigenschaftswerten aus Netzwerkanforderungen in Ihre Zwischenablage</span><span class="sxs-lookup"><span data-stu-id="8682e-474">Copy property values from network requests to your clipboard</span></span>  

<span data-ttu-id="8682e-475">Führen Sie die folgenden Aktionen aus, um Eigenschaftswerte aus Netzwerkanforderungen in Ihre Zwischenablage zu kopieren.</span><span class="sxs-lookup"><span data-stu-id="8682e-475">To copy property values from network requests to your clipboard, complete the following actions.</span></span>  

1.  <span data-ttu-id="8682e-476">Öffnen des Bereichs "über **Schriften** "</span><span class="sxs-lookup"><span data-stu-id="8682e-476">Open the **Headers** pane.</span></span>  
1.  <span data-ttu-id="8682e-477">Öffnen Sie einen der folgenden Kopfzeilen Abschnitte.</span><span class="sxs-lookup"><span data-stu-id="8682e-477">Open one of the following header sections.</span></span>  
    *   <span data-ttu-id="8682e-478">Nutzlast anfordern \ (JSON \)</span><span class="sxs-lookup"><span data-stu-id="8682e-478">Request payload \(JSON\)</span></span>  
    *   <span data-ttu-id="8682e-479">Formulardaten</span><span class="sxs-lookup"><span data-stu-id="8682e-479">Form Data</span></span>  
    *   <span data-ttu-id="8682e-480">Abfragezeichenfolgenparameter</span><span class="sxs-lookup"><span data-stu-id="8682e-480">Query String Parameters</span></span>  
    *   <span data-ttu-id="8682e-481">Anforderungs Kopfzeilen</span><span class="sxs-lookup"><span data-stu-id="8682e-481">Request Headers</span></span>  
    *   <span data-ttu-id="8682e-482">Antwortheader</span><span class="sxs-lookup"><span data-stu-id="8682e-482">Response Headers</span></span>  
1.  <span data-ttu-id="8682e-483">Öffnen Sie das Kontextmenü \ (Klicken Sie mit der rechten Maustaste auf \) > **Wert kopieren**.</span><span class="sxs-lookup"><span data-stu-id="8682e-483">Open the contextual menu \(right-click\) > **Copy value**.</span></span>  <span data-ttu-id="8682e-484">Sie können den Wert jetzt in einen beliebigen Editor einfügen, um ihn zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="8682e-484">You can now paste the value into any editor to review it.</span></span>  
    
## <span data-ttu-id="8682e-485">Ändern des Layouts des Netzwerk Panels</span><span class="sxs-lookup"><span data-stu-id="8682e-485">Change the layout of the Network panel</span></span>  

<span data-ttu-id="8682e-486">Sie können Abschnitte der **Netzwerk** Panel-UI erweitern oder reduzieren, um wichtige Informationen zu konzentrieren.</span><span class="sxs-lookup"><span data-stu-id="8682e-486">You may expand or collapse sections of the **Network** panel UI to focus important information.</span></span>  

### <span data-ttu-id="8682e-487">Ausblenden des Bereichs "Filter"</span><span class="sxs-lookup"><span data-stu-id="8682e-487">Hide the Filters pane</span></span>  

<span data-ttu-id="8682e-488">Standardmäßig zeigt devtools den Bereich " **Filter** " an.</span><span class="sxs-lookup"><span data-stu-id="8682e-488">By default, DevTools show the **Filters** pane.</span></span>  
<span data-ttu-id="8682e-489">Wählen Sie **Filter** \ ( ![ Filter ][ImageFilterIcon] \) aus, um sie auszublenden.</span><span class="sxs-lookup"><span data-stu-id="8682e-489">Choose **Filter** \(![Filter][ImageFilterIcon]\) to hide it.</span></span>  

:::image type="complex" source="../media/network-network-resources-hide-filters-button.msft.png" alt-text="Schaltfläche "Filter ausblenden"" lightbox="../media/network-network-resources-hide-filters-button.msft.png":::
   <span data-ttu-id="8682e-491">Schaltfläche "Filter ausblenden"</span><span class="sxs-lookup"><span data-stu-id="8682e-491">The Hide Filters button</span></span>  
:::image-end:::  

### <span data-ttu-id="8682e-492">Verwenden von umfangreichen Anforderungs Zeilen</span><span class="sxs-lookup"><span data-stu-id="8682e-492">Use large request rows</span></span>  

<span data-ttu-id="8682e-493">Verwenden Sie große Zeilen, wenn in Ihrer Netzwerk Anforderungstabelle mehr Leerzeichen verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="8682e-493">Use large rows when you want more whitespace in your network requests table.</span></span>  <span data-ttu-id="8682e-494">Einige Spalten liefern auch ein wenig mehr Informationen, wenn Sie große Zeilen verwenden.</span><span class="sxs-lookup"><span data-stu-id="8682e-494">Some columns also provide a little more information when using large rows.</span></span>  <span data-ttu-id="8682e-495">Der untere Wert der Spalte **size** entspricht beispielsweise der unkomprimierten Größe einer Anforderung.</span><span class="sxs-lookup"><span data-stu-id="8682e-495">For example, the bottom value of the **Size** column is the uncompressed size of a request.</span></span>  

:::image type="complex" source="../media/network-network-requests-large-request-rows.msft.png" alt-text="Ein Beispiel für große Anforderungs Zeilen im Bereich "Anforderungen"" lightbox="../media/network-network-requests-large-request-rows.msft.png":::
   <span data-ttu-id="8682e-497">Ein Beispiel für große Anforderungs Zeilen im Bereich " **Anforderungen** "</span><span class="sxs-lookup"><span data-stu-id="8682e-497">An example of large request rows in the **Requests** pane</span></span>  
:::image-end:::  

<span data-ttu-id="8682e-498">Wenn Sie große Zeilen aktivieren möchten, aktivieren Sie das Kontrollkästchen **große Anforderungs Zeilen verwenden** .</span><span class="sxs-lookup"><span data-stu-id="8682e-498">To enable large rows, turn on the **Use large request rows** checkbox.</span></span>  

:::image type="complex" source="../media/network-network-requests-use-large-request-rows-on.msft.png" alt-text="Das Kontrollkästchen "große Anforderungs Zeilen verwenden"" lightbox="../media/network-network-requests-use-large-request-rows-on.msft.png":::
   <span data-ttu-id="8682e-500">Das Kontrollkästchen " **große Anforderungs Zeilen verwenden** "</span><span class="sxs-lookup"><span data-stu-id="8682e-500">The **Use large request rows** checkbox</span></span>  
:::image-end:::  

### <span data-ttu-id="8682e-501">Ausblenden des Bereichs "Übersicht"</span><span class="sxs-lookup"><span data-stu-id="8682e-501">Hide the Overview pane</span></span>  

<span data-ttu-id="8682e-502">Standardmäßig zeigt devtools den Bereich " **Übersicht** " an.</span><span class="sxs-lookup"><span data-stu-id="8682e-502">By default, DevTools displays the **Overview** pane.</span></span>  <span data-ttu-id="8682e-503">Deaktivieren Sie das Kontrollkästchen **Übersicht anzeigen** , um es auszublenden.</span><span class="sxs-lookup"><span data-stu-id="8682e-503">To hide it, turn off the **Show Overview** checkbox.</span></span>  

:::image type="complex" source="../media/network-network-requests-show-overview-off.msft.png" alt-text="Kontrollkästchen ' Übersicht anzeigen '" lightbox="../media/network-network-requests-show-overview-off.msft.png":::
   <span data-ttu-id="8682e-505">Kontrollkästchen ' **Übersicht anzeigen** '</span><span class="sxs-lookup"><span data-stu-id="8682e-505">The **Show Overview** checkbox</span></span>  
:::image-end:::  

## <span data-ttu-id="8682e-506">Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen</span><span class="sxs-lookup"><span data-stu-id="8682e-506">Getting in touch with the Microsoft Edge DevTools team</span></span>  

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
> <span data-ttu-id="8682e-510">Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8682e-510">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="8682e-511">Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/network/reference) und wird von [Kayce Basken][KayceBasques] (Technical Writer, Chrome devtools \ & Lighthouse \) erstellt.</span><span class="sxs-lookup"><span data-stu-id="8682e-511">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/network/reference) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
<span data-ttu-id="8682e-513">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="8682e-513">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
