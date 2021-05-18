---
description: Eine umfassende Referenz zu Microsoft Edge DevTools Network Panel Features.
title: Netzwerkanalysereferenz
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, Entwicklungstools
ms.openlocfilehash: bdb1145e7ee8ed7865b68f9fd632c4b1a30007e9
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/13/2021
ms.locfileid: "11564833"
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
# <a name="network-analysis-reference"></a><span data-ttu-id="51f5a-104">Netzwerkanalysereferenz</span><span class="sxs-lookup"><span data-stu-id="51f5a-104">Network Analysis reference</span></span>  

<span data-ttu-id="51f5a-105">Entdecken Sie neue Möglichkeiten, wie Ihre Seite geladen wird, in diesem umfassenden Verweis Microsoft Edge DevTools-Netzwerkanalysefeatures.</span><span class="sxs-lookup"><span data-stu-id="51f5a-105">Discover new ways to analyze how your page loads in this comprehensive reference of Microsoft Edge DevTools network analysis features.</span></span>  

## <a name="record-network-requests"></a><span data-ttu-id="51f5a-106">Aufzeichnen von Netzwerkanforderungen</span><span class="sxs-lookup"><span data-stu-id="51f5a-106">Record network requests</span></span>  

<span data-ttu-id="51f5a-107">Standardmäßig zeichnen DevTools alle Netzwerkanforderungen im **Netzwerktool** auf, solange DevTools geöffnet ist.</span><span class="sxs-lookup"><span data-stu-id="51f5a-107">By default, DevTools record all network requests in the **Network** tool, so long as DevTools is open.</span></span>  

:::image type="complex" source="../media/network-network-panel.msft.png" alt-text="Netzwerkbereich" lightbox="../media/network-network-panel.msft.png":::
   <span data-ttu-id="51f5a-109">Das **Netzwerktool**</span><span class="sxs-lookup"><span data-stu-id="51f5a-109">The **Network** tool</span></span>  
:::image-end:::  

### <a name="stop-recording-network-requests"></a><span data-ttu-id="51f5a-110">Beenden der Aufzeichnung von Netzwerkanforderungen</span><span class="sxs-lookup"><span data-stu-id="51f5a-110">Stop recording network requests</span></span>  

<span data-ttu-id="51f5a-111">Führen Sie die folgenden Schritte aus, um aufzeichnungsanforderungen zu beenden.</span><span class="sxs-lookup"><span data-stu-id="51f5a-111">To stop recording requests, complete the following steps.</span></span>  

1.  <span data-ttu-id="51f5a-112">Wählen Sie **im Tool** Netzwerk die Option **Aufzeichnungsnetzwerkprotokoll beenden** \( ![ Aufzeichnungsnetzwerkprotokoll beenden ](../media/record-on-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="51f5a-112">On the **Network** tool, choose **Stop recording network log** \(![Stop recording network log](../media/record-on-icon.msft.png)\).</span></span>  <span data-ttu-id="51f5a-113">Es wird grau, um anzugeben, dass DevTools keine Anforderungen mehr aufzeichnen.</span><span class="sxs-lookup"><span data-stu-id="51f5a-113">It turns grey to indicate that DevTools is no longer recording requests.</span></span>  
1.  <span data-ttu-id="51f5a-114">Wählen `Control` + `E` Sie \(Windows, Linux\) oder `Command` + `E` \(macOS\)aus, während das Netzwerktool im Fokus steht.</span><span class="sxs-lookup"><span data-stu-id="51f5a-114">Select `Control`+`E` \(Windows, Linux\) or `Command`+`E` \(macOS\) while the **Network** tool is in focus.</span></span>  

### <a name="clear-requests"></a><span data-ttu-id="51f5a-115">Löschen von Anforderungen</span><span class="sxs-lookup"><span data-stu-id="51f5a-115">Clear requests</span></span>  

<span data-ttu-id="51f5a-116">Klicken **Sie im** Netzwerktool auf Löschen \( Löschen \), um alle Anforderungen aus der Tabelle Anforderungen zu ![ ](../media/clear-requests-icon.msft.png) löschen. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="51f5a-116">Choose **Clear** \(![Clear](../media/clear-requests-icon.msft.png)\) on the **Network** tool to clear all requests from the Requests table.</span></span>  

:::image type="complex" source="../media/network-network-clear-button.msft.png" alt-text="Die Schaltfläche Löschen" lightbox="../media/network-network-clear-button.msft.png":::
   <span data-ttu-id="51f5a-118">Die **Schaltfläche Löschen**</span><span class="sxs-lookup"><span data-stu-id="51f5a-118">The **Clear** button</span></span>  
:::image-end:::  

### <a name="save-requests-across-page-loads"></a><span data-ttu-id="51f5a-119">Speichern von Anforderungen über Seitenlasten hinweg</span><span class="sxs-lookup"><span data-stu-id="51f5a-119">Save requests across page loads</span></span>  

<span data-ttu-id="51f5a-120">Aktivieren Sie zum Speichern vonAnforderungen über Seitenlasten hinweg das Kontrollkästchen Protokoll **beibehalten** im Netzwerktool.</span><span class="sxs-lookup"><span data-stu-id="51f5a-120">To save requests across page loads, on the **Network** tool, turn on the **Preserve log** checkbox.</span></span>  <span data-ttu-id="51f5a-121">DevTools speichert alle Anforderungen, bis Sie **preserve log deaktivieren.**</span><span class="sxs-lookup"><span data-stu-id="51f5a-121">DevTools saves all requests until you disable **Preserve log**.</span></span>  

:::image type="complex" source="../media/network-network-preserve-log.msft.png" alt-text="Das Kontrollkästchen Protokoll beibehalten" lightbox="../media/network-network-preserve-log.msft.png":::
   <span data-ttu-id="51f5a-123">Das **Kontrollkästchen Protokoll** beibehalten</span><span class="sxs-lookup"><span data-stu-id="51f5a-123">The **Preserve Log** checkbox</span></span>  
:::image-end:::  

### <a name="capture-screenshots-during-page-load"></a><span data-ttu-id="51f5a-124">Erfassen von Screenshots beim Laden der Seite</span><span class="sxs-lookup"><span data-stu-id="51f5a-124">Capture screenshots during page load</span></span>  

<span data-ttu-id="51f5a-125">Erfassen Sie Screenshots, um zu analysieren, was für Benutzer angezeigt wird, während Sie darauf warten, dass Ihre Seite geladen wird.</span><span class="sxs-lookup"><span data-stu-id="51f5a-125">Capture screenshots to analyze what displays for users while waiting for your page to load.</span></span>  

<span data-ttu-id="51f5a-126">Um Screenshots zu aktivieren, wählen Sie **Netzwerkeinstellungen**aus, und aktivieren Sie im **Netzwerktool** das Kontrollkästchen Screenshots **erfassen.**</span><span class="sxs-lookup"><span data-stu-id="51f5a-126">To enable screenshots, choose **Network settings**, and on the **Network** tool, turn on the **Capture screenshots** checkbox.</span></span>  

<span data-ttu-id="51f5a-127">Aktualisieren Sie die Seite, während das **Netzwerktool** im Fokus steht, um Screenshots zu erfassen.</span><span class="sxs-lookup"><span data-stu-id="51f5a-127">Refresh the page while the **Network** tool is in focus to capture screenshots.</span></span>  

<span data-ttu-id="51f5a-128">Nachdem Sie einen Screenshot erfasst haben, interagieren Sie wie folgt mit ihm.</span><span class="sxs-lookup"><span data-stu-id="51f5a-128">After capturing a screenshot, you interact with it in the following ways.</span></span>  

*   <span data-ttu-id="51f5a-129">Zeigen Sie auf einen Screenshot, um den Punkt zu zeigen, an dem dieser Screenshot aufgenommen wurde.</span><span class="sxs-lookup"><span data-stu-id="51f5a-129">Hover on a screenshot to display the point at which that screenshot was captured.</span></span>  <span data-ttu-id="51f5a-130">Im Bereich Übersicht wird eine gelbe **Linie** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="51f5a-130">A yellow line is displayed on the **Overview** pane.</span></span>  
*   <span data-ttu-id="51f5a-131">Wählen Sie die Miniaturansicht eines Bildschirms aus, um alle Anforderungen herausfiltern zu können, die nach der Aufnahme des Screenshots aufgetreten sind.</span><span class="sxs-lookup"><span data-stu-id="51f5a-131">Choose the thumbnail of a screen to filter out any requests that occurred after the screenshot was captured.</span></span>  
*   <span data-ttu-id="51f5a-132">Doppelklicken Sie auf eine Miniaturansicht, um sie zu vergrößern.</span><span class="sxs-lookup"><span data-stu-id="51f5a-132">Double-click a thumbnail to zoom into it.</span></span>  

:::image type="complex" source="../media/network-network-screenshot-hover.msft.png" alt-text="Zeigen auf einen Screenshot" lightbox="../media/network-network-screenshot-hover.msft.png":::
   <span data-ttu-id="51f5a-134">Zeigen auf einen Screenshot</span><span class="sxs-lookup"><span data-stu-id="51f5a-134">Hover on a screenshot</span></span>  
:::image-end:::  

<!--  ### Replay XHR request  -->

<!--  To replay an XHR request, hover on the request in the Requests table, open the contextual menu \(right-click\), and choose **Replay XHR**.  -->

<!--  
:::image type="complex" source="../media/network-replay-xhr.msft.png" alt-text="Choose Replay XHR" lightbox="../media/network-replay-xhr.msft.png":::
   Choose Replay XHR  
:::image-end:::  
-->  

## <a name="change-loading-behavior"></a><span data-ttu-id="51f5a-135">Ändern des Ladeverhaltens</span><span class="sxs-lookup"><span data-stu-id="51f5a-135">Change loading behavior</span></span>  

### <a name="emulate-a-first-time-visitor-by-disabling-the-browser-cache"></a><span data-ttu-id="51f5a-136">Emulieren eines ersten Besuchers durch Deaktivieren des Browsercaches</span><span class="sxs-lookup"><span data-stu-id="51f5a-136">Emulate a first-time visitor by disabling the browser cache</span></span>  

<span data-ttu-id="51f5a-137">Aktivieren Sie das Kontrollkästchen Cache deaktivieren, umzu emulieren, wie ein Benutzer ihre Website zum ersten Mal erlebt.</span><span class="sxs-lookup"><span data-stu-id="51f5a-137">To emulate how a first-time user experiences your site, turn on the **Disable cache** checkbox.</span></span>  <span data-ttu-id="51f5a-138">DevTools deaktiviert den Browsercache.</span><span class="sxs-lookup"><span data-stu-id="51f5a-138">DevTools disables the browser cache.</span></span>  <span data-ttu-id="51f5a-139">Dieses Feature emuliert die Benutzererfahrung eines Erstbenutzers genauer, da Anforderungen beim wiederholten Besuch aus dem Browsercache übermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="51f5a-139">This feature more accurately emulates a first-time user's experience, because requests are served from the browser cache on repeat visits.</span></span>  

:::image type="complex" source="../media/network-network-disable-cache-checkbox.msft.png" alt-text="Das Kontrollkästchen Cache deaktivieren" lightbox="../media/network-network-disable-cache-checkbox.msft.png":::
   <span data-ttu-id="51f5a-141">Das **Kontrollkästchen Cache** deaktivieren</span><span class="sxs-lookup"><span data-stu-id="51f5a-141">The **Disable Cache** checkbox</span></span>  
:::image-end:::  

#### <a name="disable-the-browser-cache-from-the-network-conditions-drawer"></a><span data-ttu-id="51f5a-142">Deaktivieren des Browsercaches aus der Schublade "Netzwerkbedingungen"</span><span class="sxs-lookup"><span data-stu-id="51f5a-142">Disable the browser cache from the Network Conditions drawer</span></span>  

<span data-ttu-id="51f5a-143">Wenn Sie den Cache deaktivieren möchten, während Sie in anderen DevTools-Panels arbeiten, verwenden Sie die Schublade Netzwerkbedingungen.</span><span class="sxs-lookup"><span data-stu-id="51f5a-143">If you want to disable the cache while working in other DevTools panels, use the Network Conditions drawer.</span></span>  

1.  <span data-ttu-id="51f5a-144">Öffnen Sie **die Schublade Netzwerkbedingungen.**</span><span class="sxs-lookup"><span data-stu-id="51f5a-144">Open the **Network Conditions** drawer.</span></span>  
1.  <span data-ttu-id="51f5a-145">Aktivieren Sie \(or off\) das **Kontrollkästchen Cache deaktivieren.**</span><span class="sxs-lookup"><span data-stu-id="51f5a-145">Turn on \(or off\) the **Disable cache** checkbox.</span></span>  

<!--todo: add network condition section when available -->  

### <a name="manually-clear-the-browser-cache"></a><span data-ttu-id="51f5a-146">Löschen des Browsercaches manuell</span><span class="sxs-lookup"><span data-stu-id="51f5a-146">Manually clear the browser cache</span></span>  

<span data-ttu-id="51f5a-147">Um den Browsercache jederzeit manuell zu löschen, öffnen Sie das Kontextmenü \(rechtsklicken\) an einer beliebigen Stelle in der Tabelle Anforderungen, und wählen Sie **Browsercache löschen aus.**</span><span class="sxs-lookup"><span data-stu-id="51f5a-147">To manually clear the browser cache at any time, open the contextual menu \(right-click\) anywhere in the Requests table and choose **Clear Browser Cache**.</span></span>  

:::image type="complex" source="../media/network-network-clear-browser-cache.msft.png" alt-text="Wählen Sie Browsercache löschen aus" lightbox="../media/network-network-clear-browser-cache.msft.png":::
   <span data-ttu-id="51f5a-149">Wählen **Sie Browsercache löschen aus**</span><span class="sxs-lookup"><span data-stu-id="51f5a-149">Choose **Clear Browser Cache**</span></span>  
:::image-end:::  

### <a name="emulate-offline"></a><span data-ttu-id="51f5a-150">Emulieren offline</span><span class="sxs-lookup"><span data-stu-id="51f5a-150">Emulate offline</span></span>  

<span data-ttu-id="51f5a-151">Eine neue Klasse von Web-Apps namens [Progressive Web Apps][DevtoolsProgressiveWebApps]funktioniert offline mit Hilfe von **Servicemitarbeitern.**</span><span class="sxs-lookup"><span data-stu-id="51f5a-151">A new class of web apps, named [Progressive Web Apps][DevtoolsProgressiveWebApps], functions offline with the help of **service workers**.</span></span>  <span data-ttu-id="51f5a-152">Möglicherweise ist es hilfreich, beim Erstellen dieser Art von App schnell ein Gerät zu simulieren, das keine Datenverbindung hat.</span><span class="sxs-lookup"><span data-stu-id="51f5a-152">You may find it useful to quickly simulate a device that has no data connection when you are building this type of app.</span></span>  

<!--[ServiceWorkers]: /web/fundamentals/getting-started/primers/service-workers  -->

<span data-ttu-id="51f5a-153">Wählen Sie das **Dropdownmenü Online** aus, suchen Sie unter **Presets,** und wählen Sie **Offline** aus, um eine Offlinenetzwerkerfahrung zu simulieren.</span><span class="sxs-lookup"><span data-stu-id="51f5a-153">Choose the **Online** dropdown menu, search under **Presets**, and choose **Offline** to simulate an offline network experience.</span></span>  

:::image type="complex" source="../media/network-network-offline-dropdown.msft.png" alt-text="Das Dropdownmenü Offline" lightbox="../media/network-network-offline-dropdown.msft.png":::
   <span data-ttu-id="51f5a-155">Das **Dropdownmenü Offline**</span><span class="sxs-lookup"><span data-stu-id="51f5a-155">The **Offline** dropdown menu</span></span>  
:::image-end:::  

### <a name="emulate-slow-network-connections"></a><span data-ttu-id="51f5a-156">Emulieren langsamer Netzwerkverbindungen</span><span class="sxs-lookup"><span data-stu-id="51f5a-156">Emulate slow network connections</span></span>  

<span data-ttu-id="51f5a-157">Emulieren Sie langsame 3G, schnelle 3G und andere Verbindungsgeschwindigkeiten aus dem **Online-Dropdownmenü.**</span><span class="sxs-lookup"><span data-stu-id="51f5a-157">Emulate Slow 3G, Fast 3G, and other connection speeds from the **Online** dropdown menu.</span></span>  

:::image type="complex" source="../media/network-network-throttling-menu.msft.png" alt-text="Das Dropdownmenü Einschränkung" lightbox="../media/network-network-throttling-menu.msft.png":::
   <span data-ttu-id="51f5a-159">Das **Dropdownmenü Einschränkung**</span><span class="sxs-lookup"><span data-stu-id="51f5a-159">The **Throttling** dropdown menu</span></span>  
:::image-end:::  

<span data-ttu-id="51f5a-160">Sie können aus verschiedenen Voreinstellungen auswählen, z. B. Slow 3G oder Fast 3G.</span><span class="sxs-lookup"><span data-stu-id="51f5a-160">You may choose from different presets, such as Slow 3G or Fast 3G.</span></span>  <span data-ttu-id="51f5a-161">Öffnen Sie zum Hinzufügen eigener benutzerdefinierter Voreinstellungen das Menü Einschränkung, und wählen Sie **Benutzerdefiniertes**  >  **Hinzufügen aus.**</span><span class="sxs-lookup"><span data-stu-id="51f5a-161">To add your own custom presets, open the Throttling menu, and choose **Custom** > **Add**.</span></span>  

<span data-ttu-id="51f5a-162">DevTools zeigt ein Warnsymbol neben dem **Netzwerktool** an, um Sie daran zu erinnern, dass die Drosselung aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="51f5a-162">DevTools displays a warning icon next to the **Network** tool to remind you that throttling is enabled.</span></span>  

#### <a name="emulate-slow-network-connections-from-the-network-conditions-drawer"></a><span data-ttu-id="51f5a-163">Emulieren langsamer Netzwerkverbindungen aus der Schublade "Netzwerkbedingungen"</span><span class="sxs-lookup"><span data-stu-id="51f5a-163">Emulate slow network connections from the Network Conditions drawer</span></span>  

<span data-ttu-id="51f5a-164">Wenn Sie die Netzwerkverbindung drosseln möchten, während Sie in anderen DevTools-Panels arbeiten, verwenden Sie die Schublade Netzwerkbedingungen.</span><span class="sxs-lookup"><span data-stu-id="51f5a-164">If you want to throttle the network connection while working in other DevTools panels, use the Network Conditions drawer.</span></span>  

1.  <span data-ttu-id="51f5a-165">Öffnen Sie **die Schublade Netzwerkbedingungen.**</span><span class="sxs-lookup"><span data-stu-id="51f5a-165">Open the **Network Conditions** drawer.</span></span>  
1.  <span data-ttu-id="51f5a-166">Wählen Sie ihre Verbindungsgeschwindigkeit im Menü **Einschränkung** aus.</span><span class="sxs-lookup"><span data-stu-id="51f5a-166">Choose your connection speed from the **Throttling** menu.</span></span>  

<!--todo: add network condition section when available -->  

### <a name="manually-clear-browser-cookies"></a><span data-ttu-id="51f5a-167">Löschen von Browsercookies manuell</span><span class="sxs-lookup"><span data-stu-id="51f5a-167">Manually clear browser cookies</span></span>  

<span data-ttu-id="51f5a-168">Wenn Sie Browsercookies jederzeit manuell löschen möchten, zeigen Sie auf eine beliebige Stelle in der Tabelle Anforderungen, öffnen Sie das Kontextmenü \(klicken Sie mit der rechten Maustaste auf\), und wählen Sie Browsercookies **löschen aus.**</span><span class="sxs-lookup"><span data-stu-id="51f5a-168">To manually clear browser cookies at any time, hover anywhere in the Requests table, open the contextual menu \(right-click\), and choose **Clear Browser Cookies**.</span></span>  

:::image type="complex" source="../media/network-network-clear-browser-cookies.msft.png" alt-text="Wählen Sie Browsercookies löschen aus" lightbox="../media/network-network-clear-browser-cookies.msft.png":::
   <span data-ttu-id="51f5a-170">Wählen **Sie Browsercookies löschen aus**</span><span class="sxs-lookup"><span data-stu-id="51f5a-170">Choose **Clear Browser Cookies**</span></span>  
:::image-end:::  

### <a name="override-the-user-agent"></a><span data-ttu-id="51f5a-171">Überschreiben des Benutzer-Agents</span><span class="sxs-lookup"><span data-stu-id="51f5a-171">Override the user agent</span></span>  

<span data-ttu-id="51f5a-172">Verwenden Sie die folgenden Schritte, um den Benutzer-Agent manuell außer Kraft zu setzen.</span><span class="sxs-lookup"><span data-stu-id="51f5a-172">To manually override the user agent, use the following steps.</span></span>  

1.  <span data-ttu-id="51f5a-173">Öffnen Sie **die Schublade Netzwerkbedingungen.**</span><span class="sxs-lookup"><span data-stu-id="51f5a-173">Open the **Network Conditions** drawer.</span></span>  
1.  <span data-ttu-id="51f5a-174">Deaktivieren Sie das **Kontrollkästchen Automatisch** auswählen.</span><span class="sxs-lookup"><span data-stu-id="51f5a-174">Turn off the **Select automatically** checkbox.</span></span>  
1.  <span data-ttu-id="51f5a-175">Wählen Sie im Menü eine Benutzer-Agent-Option aus, oder geben Sie eine benutzerdefinierte Option in das Textfeld ein.</span><span class="sxs-lookup"><span data-stu-id="51f5a-175">Choose a user agent option from the menu, or enter a custom one in the text box.</span></span>  

<!--todo: add network condition section when available -->  

## <a name="filter-requests"></a><span data-ttu-id="51f5a-176">Filteranforderungen</span><span class="sxs-lookup"><span data-stu-id="51f5a-176">Filter requests</span></span>  

### <a name="filter-requests-by-properties"></a><span data-ttu-id="51f5a-177">Filtern von Anforderungen nach Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="51f5a-177">Filter requests by properties</span></span>  

<span data-ttu-id="51f5a-178">Verwenden Sie **das Textfeld Filter,** um Anforderungen nach Eigenschaften zu filtern, z. B. der Domäne oder der Größe der Anforderung.</span><span class="sxs-lookup"><span data-stu-id="51f5a-178">Use the **Filter** text box to filter requests by properties, such as the domain or size of the request.</span></span>  

<span data-ttu-id="51f5a-179">Wenn das Textfeld nicht angezeigt wird, **ist** der Filterbereich wahrscheinlich ausgeblendet.</span><span class="sxs-lookup"><span data-stu-id="51f5a-179">If the text box is not displayed, the **Filters** pane is probably hidden.</span></span>  
<span data-ttu-id="51f5a-180">Weitere Informationen finden Sie unter [Ausblenden des Filterbereichs.](#hide-the-filters-pane)</span><span class="sxs-lookup"><span data-stu-id="51f5a-180">For more information, navigate to [Hide the Filters pane](#hide-the-filters-pane).</span></span>  

:::image type="complex" source="../media/network-network-filters-textbox.msft.png" alt-text="Das Textfeld Filter" lightbox="../media/network-network-filters-textbox.msft.png":::
   <span data-ttu-id="51f5a-182">Das **Textfeld Filter**</span><span class="sxs-lookup"><span data-stu-id="51f5a-182">The **Filter** text box</span></span>  
:::image-end:::  

<span data-ttu-id="51f5a-183">Sie können mehrere Eigenschaften gleichzeitig verwenden, indem Sie jede Eigenschaft durch ein Leerzeichen trennen.</span><span class="sxs-lookup"><span data-stu-id="51f5a-183">You may use multiple properties simultaneously by separating each property with a space.</span></span>  <span data-ttu-id="51f5a-184">Zeigt beispielsweise `mime-type:image/png larger-than:1K` alle PNGs an, die größer als 1 KB sind.</span><span class="sxs-lookup"><span data-stu-id="51f5a-184">For example, `mime-type:image/png larger-than:1K` displays all PNGs that are larger than 1 kilobyte.</span></span>  <span data-ttu-id="51f5a-185">Die Filter mit mehreren Eigenschaften entsprechen `AND` Vorgängen.</span><span class="sxs-lookup"><span data-stu-id="51f5a-185">The multi-property filters are equivalent to `AND` operations.</span></span>  `OR` <span data-ttu-id="51f5a-186">vorgänge werden derzeit nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="51f5a-186">operations are currently not supported.</span></span>  

<span data-ttu-id="51f5a-187">Die vollständige Liste der unterstützten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="51f5a-187">The complete list of supported properties.</span></span>  

| <span data-ttu-id="51f5a-188">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="51f5a-188">Property</span></span> | <span data-ttu-id="51f5a-189">Details</span><span class="sxs-lookup"><span data-stu-id="51f5a-189">Details</span></span> |  
|:--- | :--- |  
| `domain` | <span data-ttu-id="51f5a-190">Nur Ressourcen aus der angegebenen Domäne anzeigen.</span><span class="sxs-lookup"><span data-stu-id="51f5a-190">Only display resources from the specified domain.</span></span>  <span data-ttu-id="51f5a-191">Sie können ein Platzhalterzeichen \( \) verwenden, `*` um mehrere Domänen zu enthalten.</span><span class="sxs-lookup"><span data-stu-id="51f5a-191">You may use a wildcard character \(`*`\) to include multiple domains.</span></span>  <span data-ttu-id="51f5a-192">Zeigt beispielsweise `*.com` Ressourcen aus allen Domänennamen an, die in enden. `.com`</span><span class="sxs-lookup"><span data-stu-id="51f5a-192">For example, `*.com` displays resources from all domain names ending in `.com`.</span></span>  <span data-ttu-id="51f5a-193">DevTools füllen das Dropdownmenü autocomplete mit allen gefundenen Domänen auf.</span><span class="sxs-lookup"><span data-stu-id="51f5a-193">DevTools populate the autocomplete dropdown menu with all of the domains that are found.</span></span> |  
| `has-response-header` | <span data-ttu-id="51f5a-194">Zeigt die Ressourcen an, die den angegebenen HTTP-Antwortheader enthalten.</span><span class="sxs-lookup"><span data-stu-id="51f5a-194">Displays the resources that contain the specified HTTP response header.</span></span>  <span data-ttu-id="51f5a-195">DevTools füllen das Dropdownmenü autocomplete mit allen gefundenen Antwortkopfzeilen auf.</span><span class="sxs-lookup"><span data-stu-id="51f5a-195">DevTools populate the autocomplete dropdown with all of the response headers that are found.</span></span> |  
| `is` | <span data-ttu-id="51f5a-196">Verwenden `is:running` Sie zum Suchen von `WebSocket` Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="51f5a-196">Use `is:running` to find `WebSocket` resources.</span></span> |  
| `larger-than` | <span data-ttu-id="51f5a-197">Zeigt Ressourcen an, die größer als die angegebene Größe in Byte sind.</span><span class="sxs-lookup"><span data-stu-id="51f5a-197">Displays resources that are larger than the specified size, in bytes.</span></span>  <span data-ttu-id="51f5a-198">Das Festlegen eines `1000` Werts von entspricht dem Festlegen eines Werts von `1k` .</span><span class="sxs-lookup"><span data-stu-id="51f5a-198">Setting a value of `1000` is equivalent to setting a value of `1k`.</span></span> |  
| `method` | <span data-ttu-id="51f5a-199">Zeigt Ressourcen an, die über einen angegebenen HTTP-Methodentyp abgerufen wurden.</span><span class="sxs-lookup"><span data-stu-id="51f5a-199">Displays resources that were retrieved over a specified HTTP method type.</span></span>  <span data-ttu-id="51f5a-200">DevTools füllen das Dropdown mit allen gefundenen HTTP-Methoden auf.</span><span class="sxs-lookup"><span data-stu-id="51f5a-200">DevTools populate the dropdown with all of the HTTP methods  that are found.</span></span> |  
| `mime-type` | <span data-ttu-id="51f5a-201">Zeigt Ressourcen eines angegebenen MIME-Typs an.</span><span class="sxs-lookup"><span data-stu-id="51f5a-201">Displays resources of a specified MIME type.</span></span>  <span data-ttu-id="51f5a-202">DevTools füllen die Dropdownliste mit allen gefundenen MIME-Typen auf.</span><span class="sxs-lookup"><span data-stu-id="51f5a-202">DevTools populate the dropdown with all MIME types  that are found.</span></span> |  
| `mixed-content` | <span data-ttu-id="51f5a-203">Zeigen Sie alle gemischten Inhaltsressourcen \( \) oder nur die Ressourcen an, die derzeit `mixed-content:all` angezeigt werden \( `mixed-content:displayed` \).</span><span class="sxs-lookup"><span data-stu-id="51f5a-203">Show all mixed content resources \(`mixed-content:all`\) or just the ones that are currently displayed \(`mixed-content:displayed`\).</span></span> |  
| `scheme` | <span data-ttu-id="51f5a-204">Zeigt Ressourcen an, die über ungeschütztes HTTP \( `scheme:http` \) oder geschütztes HTTPS \( `scheme:https` \) abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="51f5a-204">Displays resources retrieved over unprotected HTTP \(`scheme:http`\) or protected HTTPS \(`scheme:https`\).</span></span> |  
| `set-cookie-domain` | <span data-ttu-id="51f5a-205">Zeigt Ressourcen mit einem `Set-Cookie` Header mit einem Attribut `Domain` an, das dem angegebenen Wert entspricht.</span><span class="sxs-lookup"><span data-stu-id="51f5a-205">Displays resources that have a `Set-Cookie` header with a `Domain` attribute that matches the specified value.</span></span>  <span data-ttu-id="51f5a-206">DevTools füllen das autocomplete mit allen gefundenen Cookiedomänen auf.</span><span class="sxs-lookup"><span data-stu-id="51f5a-206">DevTools populate the autocomplete with all of the cookie domains that are found.</span></span> |  
| `set-cookie-name` | <span data-ttu-id="51f5a-207">Zeigt Ressourcen an, die über `Set-Cookie` einen Header mit einem Namen verfügen, der dem angegebenen Wert entspricht.</span><span class="sxs-lookup"><span data-stu-id="51f5a-207">Displays resources that have a `Set-Cookie` header with a name that matches the specified value.</span></span>  <span data-ttu-id="51f5a-208">DevTools füllen das AutoComplete mit allen gefundenen Cookienamen auf.</span><span class="sxs-lookup"><span data-stu-id="51f5a-208">DevTools populate the autocomplete with all of the cookie names that are found.</span></span> |  
| `set-cookie-value` | <span data-ttu-id="51f5a-209">Zeigt Ressourcen an, die über `Set-Cookie` einen Header mit einem Wert verfügen, der dem angegebenen Wert entspricht.</span><span class="sxs-lookup"><span data-stu-id="51f5a-209">Displays resources that have a `Set-Cookie` header with a value that matches the specified value.</span></span>  <span data-ttu-id="51f5a-210">DevTools füllen das AutoComplete mit allen gefundenen Cookiewerten auf.</span><span class="sxs-lookup"><span data-stu-id="51f5a-210">DevTools populate the autocomplete with all of the cookie values that are found.</span></span> |  
| `status-code` | <span data-ttu-id="51f5a-211">Zeigt Ressourcen an, die dem spezifischen HTTP-Statuscode entsprechen.</span><span class="sxs-lookup"><span data-stu-id="51f5a-211">Displays resources that match the specific HTTP status code.</span></span>  <span data-ttu-id="51f5a-212">DevTools füllt das Dropdownmenü für die automatische Vervollständigung mit allen gefundenen Statuscodes auf.</span><span class="sxs-lookup"><span data-stu-id="51f5a-212">DevTools populates the autocomplete dropdown menu with all of the status codes that are found.</span></span> |  

### <a name="filter-requests-by-type"></a><span data-ttu-id="51f5a-213">Filtern von Anforderungen nach Typ</span><span class="sxs-lookup"><span data-stu-id="51f5a-213">Filter requests by type</span></span>  

<span data-ttu-id="51f5a-214">Um Anforderungen nach Anforderungstyp zu filtern, wählen Sie eine der folgenden Schaltflächen im **Netzwerktool** aus.</span><span class="sxs-lookup"><span data-stu-id="51f5a-214">To filter requests by request type, choose the one of the following buttons on the **Network** tool.</span></span>  

:::row:::
   :::column span="1":::
      **<span data-ttu-id="51f5a-215">XHR</span><span class="sxs-lookup"><span data-stu-id="51f5a-215">XHR</span></span>**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="51f5a-216">JS</span><span class="sxs-lookup"><span data-stu-id="51f5a-216">JS</span></span>**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="51f5a-217">CSS</span><span class="sxs-lookup"><span data-stu-id="51f5a-217">CSS</span></span>**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="51f5a-218">Img</span><span class="sxs-lookup"><span data-stu-id="51f5a-218">Img</span></span>**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="51f5a-219">Medien</span><span class="sxs-lookup"><span data-stu-id="51f5a-219">Media</span></span>**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="51f5a-220">Font</span><span class="sxs-lookup"><span data-stu-id="51f5a-220">Font</span></span>**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="51f5a-221">Doc</span><span class="sxs-lookup"><span data-stu-id="51f5a-221">Doc</span></span>**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="51f5a-222">WS</span><span class="sxs-lookup"><span data-stu-id="51f5a-222">WS</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="51f5a-223">WebSocket.</span><span class="sxs-lookup"><span data-stu-id="51f5a-223">WebSocket.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="51f5a-224">Manifest</span><span class="sxs-lookup"><span data-stu-id="51f5a-224">Manifest</span></span>**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="51f5a-225">Other</span><span class="sxs-lookup"><span data-stu-id="51f5a-225">Other</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="51f5a-226">Alle anderen Nicht aufgeführten Typen.</span><span class="sxs-lookup"><span data-stu-id="51f5a-226">Any other type not listed.</span></span>  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="51f5a-227">Wenn die Schaltflächen nicht angezeigt werden, **wird** der Filterbereich möglicherweise ausgeblendet.</span><span class="sxs-lookup"><span data-stu-id="51f5a-227">If the buttons do not display, the **Filters** pane may be hidden.</span></span>  
<span data-ttu-id="51f5a-228">Weitere Informationen finden Sie unter [Ausblenden des Filterbereichs.](#hide-the-filters-pane)</span><span class="sxs-lookup"><span data-stu-id="51f5a-228">For more information, navigate to [Hide the Filters pane](#hide-the-filters-pane).</span></span>  

<span data-ttu-id="51f5a-229">Um mehrere Filter gleichzeitig zu aktivieren, halten Sie `Control` \(Windows, Linux\) oder \(macOS\) fest, und wählen `Command` Sie dann aus.</span><span class="sxs-lookup"><span data-stu-id="51f5a-229">To enable multiple type filters simultaneously, hold `Control` \(Windows, Linux\) or `Command` \(macOS\) and then choose.</span></span>  

:::image type="complex" source="../media/network-network-type-filters.msft.png" alt-text="Verwenden der Typfilter zum Anzeigen von JS-, CSS- und Dokumentressourcen" lightbox="../media/network-network-type-filters.msft.png":::
   <span data-ttu-id="51f5a-231">Verwenden der Typfilter zum Anzeigen von JS-, CSS- und Dokumentressourcen</span><span class="sxs-lookup"><span data-stu-id="51f5a-231">Use the Type filters to display JS, CSS, and Document resources</span></span>  
:::image-end:::  

### <a name="filter-requests-by-time"></a><span data-ttu-id="51f5a-232">Filtern von Anforderungen nach Zeit</span><span class="sxs-lookup"><span data-stu-id="51f5a-232">Filter requests by time</span></span>  

<span data-ttu-id="51f5a-233">Klicken Sie im BereichÜbersicht nach links oder rechts, und ziehen Sie es, um nur Anforderungen anzuzeigen, die während dieses Zeitrahmens aktiv waren.</span><span class="sxs-lookup"><span data-stu-id="51f5a-233">Choose and drag left or right on the **Overview** pane to only display requests that were active during that time frame.</span></span>  <span data-ttu-id="51f5a-234">Der Filter ist inklusive.</span><span class="sxs-lookup"><span data-stu-id="51f5a-234">The filter is inclusive.</span></span>  <span data-ttu-id="51f5a-235">Jede Anforderung, die während der hervorgehobenen Zeit aktiv war, wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="51f5a-235">Any request that was active during the highlighted time is shown.</span></span>  

:::image type="complex" source="../media/network-network-overview-filter.msft.png" alt-text="Filtern von Anforderungen, die etwa 300 ms inaktiv waren" lightbox="../media/network-network-overview-filter.msft.png":::
   <span data-ttu-id="51f5a-237">Filtern von Anforderungen, die etwa 300 ms inaktiv waren</span><span class="sxs-lookup"><span data-stu-id="51f5a-237">Filter out any requests that were inactive around 300 ms</span></span>  
:::image-end:::  

### <a name="hide-data-urls"></a><span data-ttu-id="51f5a-238">Ausblenden von Daten-URLs</span><span class="sxs-lookup"><span data-stu-id="51f5a-238">Hide data URLs</span></span>  

<span data-ttu-id="51f5a-239">[Daten-URLs][MDNHTTPDataURIs] sind kleine Dateien, die in andere Dokumente eingebettet sind.</span><span class="sxs-lookup"><span data-stu-id="51f5a-239">[Data URLs][MDNHTTPDataURIs] are small files embedded into other documents.</span></span>  <span data-ttu-id="51f5a-240">Jede Anforderung, die in der Tabelle Anforderungen angezeigt wird, die mit `data:` beginnt, ist eine Daten-URL.</span><span class="sxs-lookup"><span data-stu-id="51f5a-240">Any request that displays in the Requests table that starts with `data:` is a data URL.</span></span>  

<span data-ttu-id="51f5a-241">Deaktivieren Sie das Kontrollkästchen **Daten-URLs** ausblenden, um die Anforderungen auszublenden.</span><span class="sxs-lookup"><span data-stu-id="51f5a-241">To hide the requests, turn off the **Hide data URLs** checkbox.</span></span>  

:::image type="complex" source="../media/network-network-hide-data-urls.msft.png" alt-text="Das Kontrollkästchen Daten-URLs ausblenden" lightbox="../media/network-network-hide-data-urls.msft.png":::
   <span data-ttu-id="51f5a-243">Das **Kontrollkästchen Daten-URLs** ausblenden</span><span class="sxs-lookup"><span data-stu-id="51f5a-243">The **Hide Data URLs** checkbox</span></span>  
:::image-end:::  

## <a name="sort-requests"></a><span data-ttu-id="51f5a-244">Sortieren von Anforderungen</span><span class="sxs-lookup"><span data-stu-id="51f5a-244">Sort requests</span></span>  

<span data-ttu-id="51f5a-245">Standardmäßig werden die Anforderungen in der Tabelle Anforderungen nach Initiierungszeit sortiert, Sie können die Tabelle jedoch anhand anderer Kriterien sortieren.</span><span class="sxs-lookup"><span data-stu-id="51f5a-245">By default, the requests in the Requests table are sorted by initiation time, but you may sort the table using other criteria.</span></span>  

### <a name="sort-by-column"></a><span data-ttu-id="51f5a-246">Sortieren nach Spalte</span><span class="sxs-lookup"><span data-stu-id="51f5a-246">Sort by column</span></span>  

<span data-ttu-id="51f5a-247">Wählen Sie die Kopfzeile einer beliebigen Spalte in der Spalte Anforderungen zum Sortieren von Anforderungen nach dieser Spalte aus.</span><span class="sxs-lookup"><span data-stu-id="51f5a-247">Choose the header of any column in the Requests to sort requests by that column.</span></span>  

### <a name="sort-by-activity-phase"></a><span data-ttu-id="51f5a-248">Sortieren nach Aktivitätsphase</span><span class="sxs-lookup"><span data-stu-id="51f5a-248">Sort by activity phase</span></span>  

<span data-ttu-id="51f5a-249">Wenn Sie ändern möchten, wie der Wasserfall Anforderungen sortiert, zeigen Sie auf die Kopfzeile der Tabelle Anforderungen, öffnen Sie das Kontextmenü \(rechtsklicken\), zeigen Sie auf **Wasserfall,** und wählen Sie eine der folgenden Optionen aus.</span><span class="sxs-lookup"><span data-stu-id="51f5a-249">To change how the Waterfall sorts requests, hover on the header of the Requests table, open the contextual menu \(right-click\), hover on **Waterfall**, and choose one of the following options.</span></span>  

:::row:::
   :::column span="1":::
      **<span data-ttu-id="51f5a-250">Startzeit</span><span class="sxs-lookup"><span data-stu-id="51f5a-250">Start Time</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="51f5a-251">Die erste Anforderung, die initiiert wurde, befindet sich oben.</span><span class="sxs-lookup"><span data-stu-id="51f5a-251">The first request that was initiated is at the top.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="51f5a-252">Antwortzeit</span><span class="sxs-lookup"><span data-stu-id="51f5a-252">Response Time</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="51f5a-253">Die erste Anforderung, die mit dem Herunterladen begonnen hat, befindet sich oben.</span><span class="sxs-lookup"><span data-stu-id="51f5a-253">The first request that started downloading is at the top.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="51f5a-254">Endzeit</span><span class="sxs-lookup"><span data-stu-id="51f5a-254">End Time</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="51f5a-255">Die erste abgeschlossene Anforderung befindet sich oben.</span><span class="sxs-lookup"><span data-stu-id="51f5a-255">The first request that finished is at the top.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="51f5a-256">Gesamtdauer</span><span class="sxs-lookup"><span data-stu-id="51f5a-256">Total Duration</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="51f5a-257">Die Anforderung mit den kürzesten Verbindungseinstellungen und Anforderung oder Antwort befindet sich oben.</span><span class="sxs-lookup"><span data-stu-id="51f5a-257">The request with the shortest connection settings and request or response is at the top.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="51f5a-258">Latenz</span><span class="sxs-lookup"><span data-stu-id="51f5a-258">Latency</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="51f5a-259">Die Anforderung, die die kürzeste Zeit auf eine Antwort gewartet hat, befindet sich oben.</span><span class="sxs-lookup"><span data-stu-id="51f5a-259">The request that waited the shortest time for a response is at the top.</span></span>  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="51f5a-260">In diesen Beschreibungen wird davon ausgegangen, dass jede option vom kürzesten zum längsten rangiert wird.</span><span class="sxs-lookup"><span data-stu-id="51f5a-260">These descriptions assume that each respective option is ranked from shortest to longest.</span></span>  <span data-ttu-id="51f5a-261">Wählen Sie die Kopfzeile der **Spalte Wasserfall** aus, um die Reihenfolge umzukehren.</span><span class="sxs-lookup"><span data-stu-id="51f5a-261">Choose the header of the **Waterfall** column to reverse the order.</span></span>  

:::image type="complex" source="../media/network-network-waterfall-total-duration.msft.png" alt-text="Sortieren des Wasserfalls nach Gesamtdauer" lightbox="../media/network-network-waterfall-total-duration.msft.png":::
   <span data-ttu-id="51f5a-263">Sortieren Sie den Wasserfall nach gesamter Dauer \(Der hellere Teil jeder Leiste ist die Wartezeit, und der dunklere Teil ist die Zeit für das Herunterladen von Bytes\)</span><span class="sxs-lookup"><span data-stu-id="51f5a-263">Sort the Waterfall by total duration  \(The lighter portion of each bar is time spent waiting and the darker portion is time spent downloading bytes\)</span></span>  
:::image-end:::  

## <a name="analyze-requests"></a><span data-ttu-id="51f5a-264">Analysieren von Anforderungen</span><span class="sxs-lookup"><span data-stu-id="51f5a-264">Analyze requests</span></span>  

<span data-ttu-id="51f5a-265">Solange DevTools geöffnet sind, werden alle Anforderungen im **Netzwerktool** protokolliert.</span><span class="sxs-lookup"><span data-stu-id="51f5a-265">So long as DevTools are open, it logs all requests in the **Network** tool.</span></span>  
<span data-ttu-id="51f5a-266">Verwenden Sie den Netzwerkbereich, um Anforderungen zu analysieren.</span><span class="sxs-lookup"><span data-stu-id="51f5a-266">Use the Network panel to analyze requests.</span></span>  

### <a name="display-a-log-of-requests"></a><span data-ttu-id="51f5a-267">Anzeigen eines Protokolls mit Anforderungen</span><span class="sxs-lookup"><span data-stu-id="51f5a-267">Display a log of requests</span></span>  

<span data-ttu-id="51f5a-268">Verwenden Sie die Tabelle Anforderungen, um ein Protokoll aller Anforderungen anzeigen zu können, die während des Öffnens von DevTools vorgenommen wurden.</span><span class="sxs-lookup"><span data-stu-id="51f5a-268">Use the Requests table to display a log of all requests made while DevTools have been open.</span></span>  <span data-ttu-id="51f5a-269">Um weitere Informationen zu jedem Element zu erhalten, wählen Oder zeigen Sie auf Anforderungen.</span><span class="sxs-lookup"><span data-stu-id="51f5a-269">To reveals more information about each item, choose or hover on requests.</span></span>  

:::image type="complex" source="../media/network-network-requests-table.msft.png" alt-text="Die Tabelle Anforderungen" lightbox="../media/network-network-requests-table.msft.png":::
   <span data-ttu-id="51f5a-271">Die Tabelle Anforderungen</span><span class="sxs-lookup"><span data-stu-id="51f5a-271">The Requests table</span></span>  
:::image-end:::  

<span data-ttu-id="51f5a-272">In der Tabelle Anforderungen werden standardmäßig die folgenden Spalten angezeigt.</span><span class="sxs-lookup"><span data-stu-id="51f5a-272">The Requests table displays the following columns by default.</span></span>  

:::row:::
   :::column span="1":::
      **<span data-ttu-id="51f5a-273">Name</span><span class="sxs-lookup"><span data-stu-id="51f5a-273">Name</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="51f5a-274">Der Dateiname oder ein Bezeichner für die Ressource.</span><span class="sxs-lookup"><span data-stu-id="51f5a-274">The filename of, or an identifier for, the resource.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="51f5a-275">Status</span><span class="sxs-lookup"><span data-stu-id="51f5a-275">Status</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="51f5a-276">Der HTTP-Statuscode.</span><span class="sxs-lookup"><span data-stu-id="51f5a-276">The HTTP status code.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="51f5a-277">Typ</span><span class="sxs-lookup"><span data-stu-id="51f5a-277">Type</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="51f5a-278">Der MIME-Typ der angeforderten Ressource.</span><span class="sxs-lookup"><span data-stu-id="51f5a-278">The MIME type of the requested resource.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="51f5a-279">Initiator</span><span class="sxs-lookup"><span data-stu-id="51f5a-279">Initiator</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="51f5a-280">Die folgenden Objekte oder Prozesse initiieren Anforderungen.</span><span class="sxs-lookup"><span data-stu-id="51f5a-280">The following objects or processes initiate requests.</span></span>  
      
      *   <span data-ttu-id="51f5a-281">**Parser**  Der HTML-Parser für Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="51f5a-281">**Parser**  The HTML parser for Microsoft Edge.</span></span>  
      *   <span data-ttu-id="51f5a-282">**Umleitung**  Eine HTTP-Umleitung.</span><span class="sxs-lookup"><span data-stu-id="51f5a-282">**Redirect**  An HTTP redirect.</span></span>  
      *   <span data-ttu-id="51f5a-283">**Skript**  Eine JavaScript-Funktion.</span><span class="sxs-lookup"><span data-stu-id="51f5a-283">**Script**  A JavaScript function.</span></span>  
      *   <span data-ttu-id="51f5a-284">**Andere**  Ein anderer Prozess oder eine andere Aktion, z. B. das Navigieren zu einer Seite mithilfe eines Links oder das Eingeben einer URL in der Adressleiste.</span><span class="sxs-lookup"><span data-stu-id="51f5a-284">**Other**  Some other process or action, such as navigating to a page using a link or entering a URL in the address bar.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="51f5a-285">Size</span><span class="sxs-lookup"><span data-stu-id="51f5a-285">Size</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="51f5a-286">Die kombinierte Größe der Antwortkopfzeilen und des Antworttexts, wie vom Server zugestellt.</span><span class="sxs-lookup"><span data-stu-id="51f5a-286">The combined size of the response headers plus the response body, as delivered by the server.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="51f5a-287">Zeit</span><span class="sxs-lookup"><span data-stu-id="51f5a-287">Time</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="51f5a-288">Die Gesamtdauer vom Beginn der Anforderung bis zum Eingang des letzten Bytes in der Antwort.</span><span class="sxs-lookup"><span data-stu-id="51f5a-288">The total duration, from the start of the request to the receipt of the final byte in the response.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [<span data-ttu-id="51f5a-289">Wasserfall</span><span class="sxs-lookup"><span data-stu-id="51f5a-289">Waterfall</span></span>](#display-the-timing-relationship-of-requests)  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="51f5a-290">Eine visuelle Aufschlüsselung der Aktivität für jede Anforderung.</span><span class="sxs-lookup"><span data-stu-id="51f5a-290">A visual breakdown of the activity for each request.</span></span>  
   :::column-end:::
:::row-end:::  

#### <a name="add-or-remove-columns"></a><span data-ttu-id="51f5a-291">Hinzufügen oder Entfernen von Spalten</span><span class="sxs-lookup"><span data-stu-id="51f5a-291">Add or remove columns</span></span>  

<span data-ttu-id="51f5a-292">Zeigen Sie auf die Kopfzeile der Tabelle Anforderungen, öffnen Sie das Kontextmenü \(klicken Sie mit der rechten Maustaste\), und wählen Sie eine Option aus, um sie auszublenden oder anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="51f5a-292">Hover on the header of the Requests table, open the contextual menu \(right-click\), and choose an option to hide or show it.</span></span>  <span data-ttu-id="51f5a-293">Derzeit angezeigte Optionen verfügen neben jedem Element über Häkchen.</span><span class="sxs-lookup"><span data-stu-id="51f5a-293">Currently displayed options have checkmarks next to each item.</span></span>  

:::image type="complex" source="../media/network-network-requests-add-column.msft.png" alt-text="Hinzufügen einer Spalte zur Tabelle Anforderungen" lightbox="../media/network-network-requests-add-column.msft.png":::
   <span data-ttu-id="51f5a-295">Hinzufügen einer Spalte zur Tabelle Anforderungen</span><span class="sxs-lookup"><span data-stu-id="51f5a-295">Add a column to the Requests table</span></span>  
:::image-end:::  

#### <a name="add-custom-columns"></a><span data-ttu-id="51f5a-296">Hinzufügen benutzerdefinierter Spalten</span><span class="sxs-lookup"><span data-stu-id="51f5a-296">Add custom columns</span></span>  

<span data-ttu-id="51f5a-297">Wenn Sie der Tabelle Anforderungen eine benutzerdefinierte Spalte hinzufügen möchten, zeigen Sie auf die Kopfzeile der Tabelle Anforderungen, öffnen Sie das Kontextmenü \(rechtsklicken\), und wählen Sie **Antwortkopfzeilen**Kopfzeilen verwalten  >  **aus.**</span><span class="sxs-lookup"><span data-stu-id="51f5a-297">To add a custom column to the Requests table, hover on the header of the Requests table, open the contextual menu \(right-click\), and choose **Response Headers** > **Manage Header Columns**.</span></span>  

:::image type="complex" source="../media/network-network-requests-add-custom.msft.png" alt-text="Hinzufügen einer benutzerdefinierten Spalte zur Tabelle Anforderungen" lightbox="../media/network-network-requests-add-custom.msft.png":::
   <span data-ttu-id="51f5a-299">Hinzufügen einer benutzerdefinierten Spalte zur Tabelle Anforderungen</span><span class="sxs-lookup"><span data-stu-id="51f5a-299">Add a custom column to the Requests table</span></span>  
:::image-end:::  

### <a name="display-the-timing-relationship-of-requests"></a><span data-ttu-id="51f5a-300">Anzeigen der Zeitlichen Beziehung von Anforderungen</span><span class="sxs-lookup"><span data-stu-id="51f5a-300">Display the timing relationship of requests</span></span>  

<span data-ttu-id="51f5a-301">Verwenden Sie den Wasserfall, um die Zeitlichen Beziehungen von Anforderungen anzeigen.</span><span class="sxs-lookup"><span data-stu-id="51f5a-301">Use the Waterfall to display the timing relationships of requests.</span></span>  
<span data-ttu-id="51f5a-302">Die Standardorganisation des Wasserfalls verwendet die Startzeit der Anforderungen.</span><span class="sxs-lookup"><span data-stu-id="51f5a-302">The default organization of the Waterfall uses the start time of the requests.</span></span>  
<span data-ttu-id="51f5a-303">Anforderungen, die weiter links liegen, wurden also früher gestartet als die Anforderungen, die weiter rechts liegen.</span><span class="sxs-lookup"><span data-stu-id="51f5a-303">So, requests that are farther to the left started earlier than the requests that are farther to the right.</span></span>  

<span data-ttu-id="51f5a-304">Um die verschiedenen Methoden zum Sortieren des Wasserfalls zu überprüfen, navigieren Sie zu [Sortieren nach Aktivitätsphase](#sort-by-activity-phase).</span><span class="sxs-lookup"><span data-stu-id="51f5a-304">To review the different ways that you may sort the Waterfall, navigate to [Sort by activity phase](#sort-by-activity-phase).</span></span>  

:::image type="complex" source="../media/network-network-requests-waterfall.msft.png" alt-text="Die Spalte Wasserfall im Bereich Anforderungen" lightbox="../media/network-network-requests-waterfall.msft.png":::
   <span data-ttu-id="51f5a-306">Die Spalte "Wasserfall" im **Bereich Anforderungen**</span><span class="sxs-lookup"><span data-stu-id="51f5a-306">The Waterfall column of the **Requests** pane</span></span>  
:::image-end:::  

<!-- ### Analyze the frames of a WebSocket Connection  -->

<!--To review the frames of a WebSocket connection, use the following steps.  

1.  Choose the URL of the WebSocket connection, under the **Name** column of the Requests table.  
1.  Choose the **Frames** panel.  The table shows the last 100 frames.  

To refresh the table, re-choose the name of the WebSocket connection under the **Name** column of the Requests table.  -->

<!--
:::image type="complex" source="../media/network-frames.msft.png" alt-text="The Frames panel" lightbox="../media/network-frames.msft.png":::
   The **Frames** panel  
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

### <a name="display-a-preview-of-a-response-body"></a><span data-ttu-id="51f5a-307">Anzeigen einer Vorschau eines Antworttexts</span><span class="sxs-lookup"><span data-stu-id="51f5a-307">Display a preview of a response body</span></span>  

<span data-ttu-id="51f5a-308">Um eine Vorschau eines Antworttexts anzuzeigen, verwenden Sie die folgenden Schritte.</span><span class="sxs-lookup"><span data-stu-id="51f5a-308">To display a preview of a response body, use the following steps.</span></span>  

1.  <span data-ttu-id="51f5a-309">Wählen Sie die URL der Anforderung unter der **Spalte Name** der Tabelle Anforderungen aus.</span><span class="sxs-lookup"><span data-stu-id="51f5a-309">Choose the URL of the request, under the **Name** column of the Requests table.</span></span>  
1.  <span data-ttu-id="51f5a-310">Wählen Sie den **Bereich Vorschau** aus.</span><span class="sxs-lookup"><span data-stu-id="51f5a-310">Choose the **Preview** panel.</span></span>  

<span data-ttu-id="51f5a-311">Die Registerkarte Vorschau ist hauptsächlich hilfreich, um Bilder anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="51f5a-311">The Preview tab is mostly useful to display images.</span></span>  

:::image type="complex" source="../media/network-network-resources-preview.msft.png" alt-text="Der Vorschaubereich" lightbox="../media/network-network-resources-preview.msft.png":::
   <span data-ttu-id="51f5a-313">Der **Vorschaubereich**</span><span class="sxs-lookup"><span data-stu-id="51f5a-313">The **Preview** panel</span></span>  
:::image-end:::  

### <a name="display-a-response-body"></a><span data-ttu-id="51f5a-314">Anzeigen eines Antworttexts</span><span class="sxs-lookup"><span data-stu-id="51f5a-314">Display a response body</span></span>  

<span data-ttu-id="51f5a-315">Zum Anzeigen des Antworttexts für eine Anforderung verwenden Sie die folgenden Schritte.</span><span class="sxs-lookup"><span data-stu-id="51f5a-315">To display the response body to a request, use the following steps.</span></span>  

1.  <span data-ttu-id="51f5a-316">Wählen Sie die URL der Anforderung unter der **Spalte Name** der Tabelle Anforderungen aus.</span><span class="sxs-lookup"><span data-stu-id="51f5a-316">Choose the URL of the request, under the **Name** column of the Requests table.</span></span>  
1.  <span data-ttu-id="51f5a-317">Wählen Sie den **Antwortbereich** aus.</span><span class="sxs-lookup"><span data-stu-id="51f5a-317">Choose the **Response** panel.</span></span>  

:::image type="complex" source="../media/network-network-resources-response.msft.png" alt-text="Der Antwortbereich" lightbox="../media/network-network-resources-response.msft.png":::
   <span data-ttu-id="51f5a-319">Der **Antwortbereich**</span><span class="sxs-lookup"><span data-stu-id="51f5a-319">The **Response** panel</span></span>  
:::image-end:::  

### <a name="display-http-headers"></a><span data-ttu-id="51f5a-320">Anzeigen von HTTP-Headern</span><span class="sxs-lookup"><span data-stu-id="51f5a-320">Display HTTP headers</span></span>  

<span data-ttu-id="51f5a-321">Zum Anzeigen von HTTP-Headerdaten zu einer Anforderung verwenden Sie die folgenden Schritte.</span><span class="sxs-lookup"><span data-stu-id="51f5a-321">To display HTTP header data about a request, use the following steps.</span></span>  

1.  <span data-ttu-id="51f5a-322">Wählen Sie die URL der Anforderung unter der **Spalte Name** der Tabelle Anforderungen aus.</span><span class="sxs-lookup"><span data-stu-id="51f5a-322">Choose the URL of the request, under the **Name** column of the Requests table.</span></span>  
1.  <span data-ttu-id="51f5a-323">Wählen Sie **das Kopfzeilen-Karussell** aus.</span><span class="sxs-lookup"><span data-stu-id="51f5a-323">Choose the **Headers** psanel.</span></span>  

:::image type="complex" source="../media/network-resources-headers.msft.png" alt-text="Der Kopfzeilenbereich" lightbox="../media/network-resources-headers.msft.png":::
   <span data-ttu-id="51f5a-325">Der **Kopfzeilenbereich**</span><span class="sxs-lookup"><span data-stu-id="51f5a-325">The **Headers** panel</span></span>  
:::image-end:::  

#### <a name="display-http-header-source"></a><span data-ttu-id="51f5a-326">Anzeigen der HTTP-Headerquelle</span><span class="sxs-lookup"><span data-stu-id="51f5a-326">Display HTTP header source</span></span>  

<span data-ttu-id="51f5a-327">Standardmäßig werden im **Kopfzeilenbereich** Kopfzeilennamen alphabetisch angezeigt.</span><span class="sxs-lookup"><span data-stu-id="51f5a-327">By default, the **Headers** panel shows header names alphabetically.</span></span>  <span data-ttu-id="51f5a-328">Verwenden Sie die folgenden Schritte, um die HTTP-Headernamen in der empfangenen Reihenfolge zu spielen.</span><span class="sxs-lookup"><span data-stu-id="51f5a-328">To dsiplay the HTTP header names in the order received, use the following steps.</span></span>  

1.  <span data-ttu-id="51f5a-329">Öffnen Sie **den Bereich** Kopfzeilen für die Anforderung, die Sie interessiert.</span><span class="sxs-lookup"><span data-stu-id="51f5a-329">Open the **Headers** panel for the request that interests you.</span></span>  <span data-ttu-id="51f5a-330">Weitere Informationen finden Sie unter [Anzeigen von HTTP-Headern](#display-http-headers).</span><span class="sxs-lookup"><span data-stu-id="51f5a-330">For more information, navigate to [Display HTTP headers](#display-http-headers).</span></span>  
1.  <span data-ttu-id="51f5a-331">Wählen **Sie Neben dem**Abschnitt **Anforderungsheader** oder **Antwortkopf** die Option Quelle anzeigen aus.</span><span class="sxs-lookup"><span data-stu-id="51f5a-331">Choose **view source**, next to the **Request Header** or **Response Header** section.</span></span>  

### <a name="display-query-string-parameters"></a><span data-ttu-id="51f5a-332">Anzeigen von Abfragezeichenfolgenparametern</span><span class="sxs-lookup"><span data-stu-id="51f5a-332">Display query string parameters</span></span>  

<span data-ttu-id="51f5a-333">Wenn Sie die Abfragezeichenfolgenparameter einer URL in einem lesbaren Format anzeigen möchten, verwenden Sie die folgenden Schritte.</span><span class="sxs-lookup"><span data-stu-id="51f5a-333">To display the query string parameters of a URL in a human-readable format, use the following steps.</span></span>  

1.  <span data-ttu-id="51f5a-334">Öffnen Sie **den Bereich** Kopfzeilen für die Anforderung, die Sie interessiert.</span><span class="sxs-lookup"><span data-stu-id="51f5a-334">Open the **Headers** panel for the request that interests you.</span></span>  <span data-ttu-id="51f5a-335">Weitere Informationen finden Sie unter [Anzeigen von HTTP-Headern](#display-http-headers).</span><span class="sxs-lookup"><span data-stu-id="51f5a-335">For more information, navigate to [Display HTTP headers](#display-http-headers).</span></span>  
1.  <span data-ttu-id="51f5a-336">Navigieren Sie zum **Abschnitt Abfragezeichenfolgenparameter.**</span><span class="sxs-lookup"><span data-stu-id="51f5a-336">Navigate to the **Query String Parameters** section.</span></span>  

:::image type="complex" source="../media/network-network-resources-headers-query-string-parameters.msft.png" alt-text="Der Abschnitt Abfragezeichenfolgenparameter" lightbox="../media/network-network-resources-headers-query-string-parameters.msft.png":::
   <span data-ttu-id="51f5a-338">Der **Abschnitt Abfragezeichenfolgenparameter**</span><span class="sxs-lookup"><span data-stu-id="51f5a-338">The **Query String Parameters** section</span></span>  
:::image-end:::  

#### <a name="display-query-string-parameters-source"></a><span data-ttu-id="51f5a-339">Quelle für Abfragezeichenfolgenparameter anzeigen</span><span class="sxs-lookup"><span data-stu-id="51f5a-339">Display query string parameters source</span></span>  

<span data-ttu-id="51f5a-340">Zum Anzeigen der Abfragezeichenfolgenparameterquelle einer Anforderung verwenden Sie die folgenden Schritte.</span><span class="sxs-lookup"><span data-stu-id="51f5a-340">To display the query string parameter source of a request, use the following steps.</span></span>  

1.  <span data-ttu-id="51f5a-341">Navigieren Sie zum Abschnitt Abfragezeichenfolgenparameter.</span><span class="sxs-lookup"><span data-stu-id="51f5a-341">Navigate to the Query String Parameters section.</span></span>  <span data-ttu-id="51f5a-342">Weitere Informationen finden Sie unter Anzeigen von [Abfragezeichenfolgenparametern.](#display-query-string-parameters)</span><span class="sxs-lookup"><span data-stu-id="51f5a-342">For more information, navigate to [Display query string parameters](#display-query-string-parameters).</span></span>  
1.  <span data-ttu-id="51f5a-343">Wählen **Sie Ansichtsquelle**aus.</span><span class="sxs-lookup"><span data-stu-id="51f5a-343">Choose **view source**.</span></span>  

#### <a name="display-url-encoded-query-string-parameters"></a><span data-ttu-id="51f5a-344">Anzeigen von URL-codierten Abfragezeichenfolgenparametern</span><span class="sxs-lookup"><span data-stu-id="51f5a-344">Display URL-encoded query string parameters</span></span>  

<span data-ttu-id="51f5a-345">Verwenden Sie die folgenden Schritte, um Abfragezeichenfolgenparameter in einem vom Menschen lesbaren Format, jedoch bei beibehaltenen Codierungen, anzeigen zu können.</span><span class="sxs-lookup"><span data-stu-id="51f5a-345">To display query string parameters in a human-readable format, but with encodings preserved, use the following steps.</span></span>  

1.  <span data-ttu-id="51f5a-346">Navigieren Sie zum Abschnitt Abfragezeichenfolgenparameter.</span><span class="sxs-lookup"><span data-stu-id="51f5a-346">Navigate to the Query String Parameters section.</span></span>  <span data-ttu-id="51f5a-347">Weitere Informationen finden Sie unter Anzeigen von [Abfragezeichenfolgenparametern.](#display-query-string-parameters)</span><span class="sxs-lookup"><span data-stu-id="51f5a-347">For more information, navigate to [Display query string parameters](#display-query-string-parameters).</span></span>  
1.  <span data-ttu-id="51f5a-348">Wählen **Sie die url-codierte Ansicht aus.**</span><span class="sxs-lookup"><span data-stu-id="51f5a-348">Choose **view URL encoded**.</span></span>  

### <a name="display-cookies"></a><span data-ttu-id="51f5a-349">Anzeigen von Cookies</span><span class="sxs-lookup"><span data-stu-id="51f5a-349">Display cookies</span></span>  

<span data-ttu-id="51f5a-350">Verwenden Sie die folgenden Schritte, um die im HTTP-Header einer Anforderung gesendeten Cookies anzeigen zu können.</span><span class="sxs-lookup"><span data-stu-id="51f5a-350">To display the cookies sent in the HTTP header of a request, use the following steps.</span></span>  

1.  <span data-ttu-id="51f5a-351">Wählen Sie die URL der Anforderung unter der **Spalte Name** der Tabelle Anforderungen aus.</span><span class="sxs-lookup"><span data-stu-id="51f5a-351">Choose the URL of the request, under the **Name** column of the Requests table.</span></span>  
1.  <span data-ttu-id="51f5a-352">Wählen Sie den **Bereich Cookies** aus.</span><span class="sxs-lookup"><span data-stu-id="51f5a-352">Choose the **Cookies** panel.</span></span>  

<!--For more information about each of the columns, navigate to [Fields][ManageDataCookiesFields].  -->  

<!--[ManageDataCookiesFields]: manage-data/cookies#fields  -->  
<!--TODO: add link when section is available -->  

:::image type="complex" source="../media/network-network-resources-cookies.msft.png" alt-text="Der Bereich Cookies" lightbox="../media/network-network-resources-cookies.msft.png":::
   <span data-ttu-id="51f5a-354">Der Bereich "Cookies"</span><span class="sxs-lookup"><span data-stu-id="51f5a-354">The Cookies panel</span></span>  
:::image-end:::  

### <a name="display-the-timing-breakdown-of-a-request"></a><span data-ttu-id="51f5a-355">Anzeigen der Zeitlichen Aufschlüsselung einer Anforderung</span><span class="sxs-lookup"><span data-stu-id="51f5a-355">Display the timing breakdown of a request</span></span>  

<span data-ttu-id="51f5a-356">Verwenden Sie die folgenden Schritte, um die Zeitliche Aufschlüsselung einer Anforderung zu zeigen.</span><span class="sxs-lookup"><span data-stu-id="51f5a-356">To display the timing breakdown of a request, use the following steps.</span></span>  

1.  <span data-ttu-id="51f5a-357">Wählen Sie die URL der Anforderung unter der **Spalte Name** der Tabelle Anforderungen aus.</span><span class="sxs-lookup"><span data-stu-id="51f5a-357">Choose the URL of the request, under the **Name** column of the Requests table.</span></span>  
1.  <span data-ttu-id="51f5a-358">Wählen Sie den **Zeitsteuerungsbereich** aus.</span><span class="sxs-lookup"><span data-stu-id="51f5a-358">Choose the **Timing** panel.</span></span>  

<span data-ttu-id="51f5a-359">Wenn Sie schneller auf die Daten zugreifen möchten, navigieren Sie zu [Vorschau einer Zeitplanungsaufschlüsselung.](#preview-a-timing-breakdown)</span><span class="sxs-lookup"><span data-stu-id="51f5a-359">For a faster way to access the data, navigate to [Preview a timing breakdown](#preview-a-timing-breakdown).</span></span>  

<span data-ttu-id="51f5a-360">Weitere Informationen zu den einzelnen Phasen, die möglicherweiseim Zeitsteuerungsfenster angezeigt werden, finden Sie unter [Timing breakdown phases explained](#timing-breakdown-phases-explained).</span><span class="sxs-lookup"><span data-stu-id="51f5a-360">For more information about each of the phases that may be displayed in the **Timing** panel, navigate to [Timing breakdown phases explained](#timing-breakdown-phases-explained).</span></span>  

:::image type="complex" source="../media/network-network-resources-timing.msft.png" alt-text="Der Zeitsteuerungsbereich" lightbox="../media/network-network-resources-timing.msft.png":::
   <span data-ttu-id="51f5a-362">Der **Zeitsteuerungsbereich**</span><span class="sxs-lookup"><span data-stu-id="51f5a-362">The **Timing** panel</span></span>  
:::image-end:::  

<span data-ttu-id="51f5a-363">Weitere Informationen zu den einzelnen Phasen.</span><span class="sxs-lookup"><span data-stu-id="51f5a-363">More information about each of the phases.</span></span>  

<span data-ttu-id="51f5a-364">Weitere Informationen zum Zugriff auf die Anzeige finden Sie unter [Anzeigezeitplan .](#display-the-timing-breakdown-of-a-request)</span><span class="sxs-lookup"><span data-stu-id="51f5a-364">For more information about accessing the display, navigate to [Display timing breakdown](#display-the-timing-breakdown-of-a-request).</span></span>  

#### <a name="preview-a-timing-breakdown"></a><span data-ttu-id="51f5a-365">Vorschau einer Zeitlichen Aufschlüsselung</span><span class="sxs-lookup"><span data-stu-id="51f5a-365">Preview a timing breakdown</span></span>  

<span data-ttu-id="51f5a-366">Wenn Sie eine Vorschau der Zeitlichen Aufschlüsselung einer Anforderung anzeigen möchten, zeigen Sie in der **Spalte Wasserfall** der Tabelle Anforderungen auf den Eintrag für die Anforderung.</span><span class="sxs-lookup"><span data-stu-id="51f5a-366">To display a preview of the timing breakdown of a request, in the **Waterfall** column of the Requests table, hover on the entry for the request.</span></span>  

<span data-ttu-id="51f5a-367">Weitere Informationen dazu, wie Sie auf die Daten zugreifen können, ohne darauf zu zeigen, finden Sie unter Anzeigen der Zeitlichen [Aufschlüsselung einer Anforderung.](#display-the-timing-breakdown-of-a-request)</span><span class="sxs-lookup"><span data-stu-id="51f5a-367">For more information about how to access the data without hovering, navigate to [Display the timing breakdown of a request](#display-the-timing-breakdown-of-a-request).</span></span>  

:::image type="complex" source="../media/network-network-resources-waterfall-hover.msft.png" alt-text="> Vorschau der Zeitlichen Aufschlüsselung einer Anforderung" lightbox="../media/network-network-resources-waterfall-hover.msft.png":::
   <span data-ttu-id="51f5a-369">Vorschau der Zeitlichen Aufschlüsselung einer Anforderung</span><span class="sxs-lookup"><span data-stu-id="51f5a-369">Preview the timing breakdown of a request</span></span>  
:::image-end:::  

#### <a name="timing-breakdown-phases-explained"></a><span data-ttu-id="51f5a-370">Erläuterte Phasen für die Zeitliche Aufschlüsselung</span><span class="sxs-lookup"><span data-stu-id="51f5a-370">Timing breakdown phases explained</span></span>  

<span data-ttu-id="51f5a-371">Weitere Informationen zu den einzelnen Phasen, die möglicherweise im **Zeitsteuerungsfenster angezeigt** werden.</span><span class="sxs-lookup"><span data-stu-id="51f5a-371">More information about each of the phases that may display in the **Timing** panel.</span></span>  

:::row:::
   :::column span="1":::
      **<span data-ttu-id="51f5a-372">Warteschlangen</span><span class="sxs-lookup"><span data-stu-id="51f5a-372">Queueing</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="51f5a-373">Der Browser warteschlanget Anforderungen, wenn eine der folgenden Bedingungen zutrifft.</span><span class="sxs-lookup"><span data-stu-id="51f5a-373">The browser queues requests when any of the following are true.</span></span>  
      
      *   <span data-ttu-id="51f5a-374">Anforderungen mit höherer Priorität sind vorhanden.</span><span class="sxs-lookup"><span data-stu-id="51f5a-374">Higher priority requests exist.</span></span>  
      *   <span data-ttu-id="51f5a-375">Sechs TCP-Verbindungen sind für denselben Ursprung geöffnet, d. h. die Grenze.</span><span class="sxs-lookup"><span data-stu-id="51f5a-375">Six TCP connections are open for the same origin, which is the limit.</span></span>  <span data-ttu-id="51f5a-376">Gilt nur für HTTP/1.0 und HTTP/1.1.</span><span class="sxs-lookup"><span data-stu-id="51f5a-376">Applies to HTTP/1.0 and HTTP/1.1 only.</span></span>  
      *   <span data-ttu-id="51f5a-377">Der Browser verteilt kurz Speicherplatz im Datenträgercache.</span><span class="sxs-lookup"><span data-stu-id="51f5a-377">The browser is briefly allocating space in the disk cache.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="51f5a-378">Ins Stocken geraten</span><span class="sxs-lookup"><span data-stu-id="51f5a-378">Stalled</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="51f5a-379">Die Anforderung wird aus einem der unter Warteschlangen **beschriebenen Gründe ins Stocken geraten.**</span><span class="sxs-lookup"><span data-stu-id="51f5a-379">The request is stalled for any of the reasons described in **Queueing**.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="51f5a-380">DNS-Nachschlage</span><span class="sxs-lookup"><span data-stu-id="51f5a-380">DNS Lookup</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="51f5a-381">Der Browser aufgelöst die IP-Adresse für die Anforderung.</span><span class="sxs-lookup"><span data-stu-id="51f5a-381">The browser is resolving the IP address for the request.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="51f5a-382">Anfängliche Verbindung</span><span class="sxs-lookup"><span data-stu-id="51f5a-382">Initial connection</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="51f5a-383">Der Browser richtet eine Verbindung ein, einschließlich TCP-Handshakes, TCP-Wiederholungen und aushandelt eine Secure Socket Layer.</span><span class="sxs-lookup"><span data-stu-id="51f5a-383">The browser establishes a connection including TCP handshakes, TCP retries, and negotiates a Secure Socket Layer.</span></span>
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="51f5a-384">Proxyaushandlung</span><span class="sxs-lookup"><span data-stu-id="51f5a-384">Proxy negotiation</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="51f5a-385">Der Browser handelt die Anforderung mit einem [Proxyserver aus.][WikiProxyServer]</span><span class="sxs-lookup"><span data-stu-id="51f5a-385">The browser is negotiating the request with a [proxy server][WikiProxyServer].</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="51f5a-386">Gesendete Anforderung</span><span class="sxs-lookup"><span data-stu-id="51f5a-386">Request sent</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="51f5a-387">Die Anforderung wird gesendet.</span><span class="sxs-lookup"><span data-stu-id="51f5a-387">The request is being sent.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="51f5a-388">ServiceWorker-Vorbereitung</span><span class="sxs-lookup"><span data-stu-id="51f5a-388">ServiceWorker Preparation</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="51f5a-389">Der Browser startet den Dienstmitarbeiter.</span><span class="sxs-lookup"><span data-stu-id="51f5a-389">The browser is starting the service worker.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="51f5a-390">Anforderung an ServiceWorker</span><span class="sxs-lookup"><span data-stu-id="51f5a-390">Request to ServiceWorker</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="51f5a-391">Die Anforderung wird an den Servicemitarbeiter gesendet.</span><span class="sxs-lookup"><span data-stu-id="51f5a-391">The request is being sent to the service worker.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="51f5a-392">Waiting \(TTFB\)</span><span class="sxs-lookup"><span data-stu-id="51f5a-392">Waiting \(TTFB\)</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="51f5a-393">Der Browser wartet auf das erste Byte einer Antwort.</span><span class="sxs-lookup"><span data-stu-id="51f5a-393">The browser is waiting for the first byte of a response.</span></span>  <span data-ttu-id="51f5a-394">TTFB steht für Time To First Byte.</span><span class="sxs-lookup"><span data-stu-id="51f5a-394">TTFB stands for Time To First Byte.</span></span>  <span data-ttu-id="51f5a-395">Dieser Zeitpunkt umfasst eine Roundtrip-Wartezeit und die Zeit, die der Server zum Vorbereiten der Antwort brauchte.</span><span class="sxs-lookup"><span data-stu-id="51f5a-395">This timing includes one round trip of latency and the time the server took to prepare the response.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="51f5a-396">Herunterladen von Inhalten</span><span class="sxs-lookup"><span data-stu-id="51f5a-396">Content Download</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="51f5a-397">Der Browser empfängt die Antwort.</span><span class="sxs-lookup"><span data-stu-id="51f5a-397">The browser is receiving the response.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="51f5a-398">Empfangen von Push</span><span class="sxs-lookup"><span data-stu-id="51f5a-398">Receiving Push</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="51f5a-399">Der Browser empfängt Daten für diese Antwort über HTTP/2 Server Push.</span><span class="sxs-lookup"><span data-stu-id="51f5a-399">The browser is receiving data for this response via HTTP/2 Server Push.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="51f5a-400">Lese-Push</span><span class="sxs-lookup"><span data-stu-id="51f5a-400">Reading Push</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="51f5a-401">Der Browser liest die zuvor empfangenen lokalen Daten.</span><span class="sxs-lookup"><span data-stu-id="51f5a-401">The browser is reading the local data previously received.</span></span>  
   :::column-end:::
:::row-end:::  

### <a name="display-initiators-and-dependencies"></a><span data-ttu-id="51f5a-402">Anzeigen von Initiatoren und Abhängigkeiten</span><span class="sxs-lookup"><span data-stu-id="51f5a-402">Display initiators and dependencies</span></span>  

<span data-ttu-id="51f5a-403">Um die Initiatoren und Abhängigkeiten einer Anforderung anzuzeigen, halten Sie die Anforderung in der Tabelle Anforderungen, und zeigen Sie `Shift` auf die Anforderung.</span><span class="sxs-lookup"><span data-stu-id="51f5a-403">To display the initiators and dependencies of a request, hold `Shift`and hover on the request in the Requests table.</span></span>  <span data-ttu-id="51f5a-404">DevTools-Farben: Initiatoren werden grün und Abhängigkeiten in Rot angezeigt.</span><span class="sxs-lookup"><span data-stu-id="51f5a-404">DevTools colors: initiators are shown in green and dependencies are shown in red.</span></span>  

:::image type="complex" source="../media/network-network-resources-initiators-dependencies.msft.png" alt-text="Anzeigen der Initiatoren und Abhängigkeiten einer Anforderung" lightbox="../media/network-network-resources-initiators-dependencies.msft.png":::
   <span data-ttu-id="51f5a-406">Anzeigen der Initiatoren und Abhängigkeiten einer Anforderung</span><span class="sxs-lookup"><span data-stu-id="51f5a-406">Display the initiators and dependencies of a request</span></span>  
:::image-end:::  

<span data-ttu-id="51f5a-407">Wenn die Tabelle Anforderungen chronologisch geordnet ist, zeigt die zeile vor der Tabelle eine grüne Anforderung an, wenn Sie auf eine Linie zeigen.</span><span class="sxs-lookup"><span data-stu-id="51f5a-407">When the Requests table is ordered chronologically, if you hover on a line, the line preceding it displays a green request.</span></span>  <span data-ttu-id="51f5a-408">Die grüne Anforderung ist der Initiator der Abhängigkeit.</span><span class="sxs-lookup"><span data-stu-id="51f5a-408">The green request is the initiator of the dependency.</span></span>  <span data-ttu-id="51f5a-409">Wenn zuvor eine weitere grüne Anforderung in der Zeile angezeigt wird, ist diese höhere Anforderung der Initiator des Initiators.</span><span class="sxs-lookup"><span data-stu-id="51f5a-409">If another green request is displayed on the line before that, that higher request is the initiator of the initiator.</span></span>  <span data-ttu-id="51f5a-410">Und so weiter.</span><span class="sxs-lookup"><span data-stu-id="51f5a-410">And so on.</span></span>  

### <a name="display-load-events"></a><span data-ttu-id="51f5a-411">Anzeigen von Lastereignissen</span><span class="sxs-lookup"><span data-stu-id="51f5a-411">Display load events</span></span>  

<span data-ttu-id="51f5a-412">DevTools zeigt das Timing der `DOMContentLoaded` Ereignisse und `load` an mehreren Stellen im **Netzwerktool** an.</span><span class="sxs-lookup"><span data-stu-id="51f5a-412">DevTools displays the timing of the `DOMContentLoaded` and `load` events in multiple places on the **Network** tool.</span></span>  <span data-ttu-id="51f5a-413">Das `DOMContentLoaded` Ereignis ist blau gefärbt, und das Ereignis ist `load` rot.</span><span class="sxs-lookup"><span data-stu-id="51f5a-413">The `DOMContentLoaded` event is colored blue, and the `load` event is red.</span></span>  

:::image type="complex" source="../media/network-network-requests-load-events.msft.png" alt-text="Die Speicherorte der DOMContentLoaded- und Load-Ereignisse im Netzwerkbereich" lightbox="../media/network-network-requests-load-events.msft.png":::
   <span data-ttu-id="51f5a-415">Die Speicherorte und `DOMContentLoaded` `load` Ereignisse im **Netzwerktool**</span><span class="sxs-lookup"><span data-stu-id="51f5a-415">The locations of the `DOMContentLoaded` and `load` events on the **Network** tool</span></span>  
:::image-end:::  

### <a name="display-the-total-number-of-requests"></a><span data-ttu-id="51f5a-416">Anzeigen der Gesamtzahl der Anforderungen</span><span class="sxs-lookup"><span data-stu-id="51f5a-416">Display the total number of requests</span></span>  

<span data-ttu-id="51f5a-417">Die Gesamtanzahl der Anforderungen wirdim Zusammenfassungsbereich unten im **Netzwerktool** aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="51f5a-417">The total number of requests is listed in the **Summary** pane, at the bottom of the **Network** tool.</span></span>  

> [!CAUTION]
> <span data-ttu-id="51f5a-418">Diese Zahl verfolgt nur Anforderungen, die seit dem Öffnen von DevTools protokolliert wurden.</span><span class="sxs-lookup"><span data-stu-id="51f5a-418">This number only tracks requests that have been logged since DevTools was opened.</span></span>  <span data-ttu-id="51f5a-419">Wenn vor dem Öffnen von DevTools andere Anforderungen aufgetreten sind, werden diese Anforderungen nicht gezählt.</span><span class="sxs-lookup"><span data-stu-id="51f5a-419">If other requests occurred before DevTools was opened, those requests are not counted.</span></span>  

:::image type="complex" source="../media/network-network-total-requests.msft.png" alt-text="Die Gesamtzahl der Anforderungen seit dem Öffnen von DevTools" lightbox="../media/network-network-total-requests.msft.png":::
   <span data-ttu-id="51f5a-421">Die Gesamtzahl der Anforderungen seit dem Öffnen von DevTools</span><span class="sxs-lookup"><span data-stu-id="51f5a-421">The total number of requests since DevTools were opened</span></span>  
:::image-end:::  

### <a name="display-the-total-download-size"></a><span data-ttu-id="51f5a-422">Anzeigen der Downloadgröße insgesamt</span><span class="sxs-lookup"><span data-stu-id="51f5a-422">Display the total download size</span></span>  

<span data-ttu-id="51f5a-423">Die Gesamtgröße der Downloads vonAnforderungen wird im Zusammenfassungsbereich unten im **Netzwerktool** aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="51f5a-423">The total download size of requests is listed in the **Summary** pane, at the bottom of the **Network** tool.</span></span>  

> [!CAUTION]
> <span data-ttu-id="51f5a-424">Diese Zahl verfolgt nur Anforderungen, die seit dem Öffnen von DevTools protokolliert wurden.</span><span class="sxs-lookup"><span data-stu-id="51f5a-424">This number only tracks requests that have been logged since DevTools was opened.</span></span>  <span data-ttu-id="51f5a-425">Wenn vor dem Öffnen von DevTools andere Anforderungen aufgetreten sind, werden die vorherigen Anforderungen nicht gezählt.</span><span class="sxs-lookup"><span data-stu-id="51f5a-425">If other requests occurred before DevTools was opened, the previous requests are not counted.</span></span>  

:::image type="complex" source="../media/network-network-total-download-size.msft.png" alt-text="Die Gesamtgröße der Downloads von Anforderungen" lightbox="../media/network-network-total-download-size.msft.png":::
   <span data-ttu-id="51f5a-427">Die Gesamtgröße der Downloads von Anforderungen</span><span class="sxs-lookup"><span data-stu-id="51f5a-427">The total download size of requests</span></span>  
:::image-end:::  

<span data-ttu-id="51f5a-428">Navigieren Sie, um zu überprüfen, wie groß ressourcen sind, nachdem der Browser die Komprimierung der einzelnen Elemente deaktiviert hat, um die nicht komprimierte Größe [einer Ressource anzuzeigen.](#display-the-uncompressed-size-of-a-resource)</span><span class="sxs-lookup"><span data-stu-id="51f5a-428">To verify how large resources are after the browser uncompresses each item, navigate to [display the uncompressed size of a resource](#display-the-uncompressed-size-of-a-resource).</span></span>  

### <a name="display-the-stack-trace-that-caused-a-request"></a><span data-ttu-id="51f5a-429">Anzeigen der Stapelverfolgung, die eine Anforderung verursacht hat</span><span class="sxs-lookup"><span data-stu-id="51f5a-429">Display the stack trace that caused a request</span></span>  

<span data-ttu-id="51f5a-430">Nachdem eine JavaScript-Anweisung eine Ressource anfordert, zeigen Sie auf die **Spalte Initiator,** um die Stapelverfolgung zu zeigen, die zur Anforderung führt.</span><span class="sxs-lookup"><span data-stu-id="51f5a-430">After a JavaScript statement requests a resource, hover on the **Initiator** column to display the stack trace leading up to the request.</span></span>  

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

:::image type="complex" source="../media/network-network-requests-initiator-stack.msft.png" alt-text="Die Stapelverfolgung, die zu einer Ressourcenanforderung führt" lightbox="../media/network-network-requests-initiator-stack.msft.png":::
   <span data-ttu-id="51f5a-432">Die Stapelverfolgung, die zu einer Ressourcenanforderung führt</span><span class="sxs-lookup"><span data-stu-id="51f5a-432">The stack trace leading up to a resource request</span></span>  
:::image-end:::  

### <a name="display-the-uncompressed-size-of-a-resource"></a><span data-ttu-id="51f5a-433">Anzeigen der unkomprimierten Größe einer Ressource</span><span class="sxs-lookup"><span data-stu-id="51f5a-433">Display the uncompressed size of a resource</span></span>  

<span data-ttu-id="51f5a-434">Aktivieren Sie das **Kontrollkästchen Große Anforderungszeilen** verwenden, und überprüfen Sie dann den unteren Wert der **Spalte Größe.**</span><span class="sxs-lookup"><span data-stu-id="51f5a-434">Turn on the **Use large request rows** checkbox and then review the bottom value of the **Size** column.</span></span>  

:::image type="complex" source="../media/network-network-requests-uncompressed-compare.msft.png" alt-text="Beispiel für nicht komprimierte Ressourcen" lightbox="../media/network-network-requests-uncompressed-compare.msft.png":::
   <span data-ttu-id="51f5a-436">Ein Beispiel für nicht komprimierte Ressourcen \(Die komprimierte Größe der Datei, die über das Netzwerk gesendet wurde, war , während die nicht komprimierte `jquery-3.3.1.min.js` `29.9 KB` Größe `84.9 KB` \) war.</span><span class="sxs-lookup"><span data-stu-id="51f5a-436">An example of uncompressed resources  \(The compressed size of the `jquery-3.3.1.min.js` file that was sent over the network was `29.9 KB`, whereas the uncompressed size was `84.9 KB`\)</span></span>  
:::image-end:::  

## <a name="export-requests-data"></a><span data-ttu-id="51f5a-437">Exportieren von Anforderungensdaten</span><span class="sxs-lookup"><span data-stu-id="51f5a-437">Export requests data</span></span>  

### <a name="save-all-network-requests-to-a-har-file"></a><span data-ttu-id="51f5a-438">Speichern aller Netzwerkanforderungen in einer HAR-Datei</span><span class="sxs-lookup"><span data-stu-id="51f5a-438">Save all network requests to a HAR file</span></span>  

<span data-ttu-id="51f5a-439">Führen Sie die folgenden Schritte aus, um alle Netzwerkanforderungen in einer HAR-Datei zu speichern.</span><span class="sxs-lookup"><span data-stu-id="51f5a-439">To save all network requests to a HAR file, complete the following steps.</span></span>  

1.  <span data-ttu-id="51f5a-440">Zeigen Sie auf eine beliebige Anforderung in der Tabelle Anforderungen, und öffnen Sie das Kontextmenü \(klicken Sie mit der rechten Maustaste\).</span><span class="sxs-lookup"><span data-stu-id="51f5a-440">Hover on any request in the Requests table and open the contextual menu \(right-click\).</span></span>  
1.  <span data-ttu-id="51f5a-441">Wählen **Sie Speichern als HAR mit Inhalt aus.**</span><span class="sxs-lookup"><span data-stu-id="51f5a-441">Choose **Save as HAR with Content**.</span></span>  <span data-ttu-id="51f5a-442">DevTools speichert alle Anforderungen, die seit dem Öffnen von DevTools in der HAR-Datei aufgetreten sind.</span><span class="sxs-lookup"><span data-stu-id="51f5a-442">DevTools saves all requests that have occurred since you opened DevTools to the HAR file.</span></span>  <span data-ttu-id="51f5a-443">Anforderungen können nicht gefiltert werden.</span><span class="sxs-lookup"><span data-stu-id="51f5a-443">You are not able to filter requests.</span></span>  <span data-ttu-id="51f5a-444">Sie können auch keine einzelne Anforderung speichern.</span><span class="sxs-lookup"><span data-stu-id="51f5a-444">You are also not able to save a single request.</span></span>  

<span data-ttu-id="51f5a-445">Nachdem Sie eine HAR-Datei gespeichert haben, können Sie sie zur Analyse wieder in DevTools importieren.</span><span class="sxs-lookup"><span data-stu-id="51f5a-445">Once you save a HAR file, you may import it back into DevTools for analysis.</span></span>  <span data-ttu-id="51f5a-446">Ziehen Sie einfach die HAR-Datei per Drag -and-Drop in die Requests-Tabelle.</span><span class="sxs-lookup"><span data-stu-id="51f5a-446">Just drag-and-drop the HAR file into the Requests table.</span></span>  
<!--For more information, navigate to also [HAR Analyzer][HARAnalyzer].  -->  

<!--[HARAnalyzer]: https://toolbox.alphabetapps.com/apps/har_analyzer  -->  
<!--Todo: add section link when content is available  -->  

:::image type="complex" source="../media/network-network-requests-save-har-content.msft.png" alt-text="Wählen Sie Speichern als HAR mit Inhalt aus" lightbox="../media/network-network-requests-save-har-content.msft.png":::
   <span data-ttu-id="51f5a-448">Wählen **Sie Speichern als HAR mit Inhalt aus**</span><span class="sxs-lookup"><span data-stu-id="51f5a-448">Choose **Save as HAR with Content**</span></span>  
:::image-end:::  

### <a name="copy-one-or-more-requests-to-the-clipboard"></a><span data-ttu-id="51f5a-449">Kopieren einer oder mehreren Anforderungen in die Zwischenablage</span><span class="sxs-lookup"><span data-stu-id="51f5a-449">Copy one or more requests to the clipboard</span></span>  

<span data-ttu-id="51f5a-450">Zeigen Sie in der Spalte **Name** der Tabelle Anforderungen auf eine Anforderung, öffnen Sie das Kontextmenü \(mit der rechten Maustaste auf\), zeigen Sie auf **Kopieren,** und wählen Sie eine der folgenden Optionen aus.</span><span class="sxs-lookup"><span data-stu-id="51f5a-450">Under the **Name** column of the Requests table, hover on a request, open the contextual menu \(right-click\), hover on **Copy**, and choose one of the following options.</span></span>  

| <span data-ttu-id="51f5a-451">Name</span><span class="sxs-lookup"><span data-stu-id="51f5a-451">Name</span></span> | <span data-ttu-id="51f5a-452">Details</span><span class="sxs-lookup"><span data-stu-id="51f5a-452">Details</span></span> |  
|:--- |:--- |  
| **<span data-ttu-id="51f5a-453">Linkadresse kopieren</span><span class="sxs-lookup"><span data-stu-id="51f5a-453">Copy Link Address</span></span>** | <span data-ttu-id="51f5a-454">Kopieren Sie die URL der Anforderung in die Zwischenablage.</span><span class="sxs-lookup"><span data-stu-id="51f5a-454">Copy the URL of the request to the clipboard.</span></span> |  
| **<span data-ttu-id="51f5a-455">Antwort kopieren</span><span class="sxs-lookup"><span data-stu-id="51f5a-455">Copy Response</span></span>** | <span data-ttu-id="51f5a-456">Kopieren Sie den Antworttext in die Zwischenablage.</span><span class="sxs-lookup"><span data-stu-id="51f5a-456">Copy the response body to the clipboard.</span></span> |  
| **<span data-ttu-id="51f5a-457">Kopieren als Abrufen</span><span class="sxs-lookup"><span data-stu-id="51f5a-457">Copy as Fetch</span></span>** | &nbsp; |  
| **<span data-ttu-id="51f5a-458">Kopieren als cURL</span><span class="sxs-lookup"><span data-stu-id="51f5a-458">Copy as cURL</span></span>** | <span data-ttu-id="51f5a-459">Kopieren Sie die Anforderung als cURL-Befehl.</span><span class="sxs-lookup"><span data-stu-id="51f5a-459">Copy the request as a cURL command.</span></span> |  
| **<span data-ttu-id="51f5a-460">Copy All as Fetch</span><span class="sxs-lookup"><span data-stu-id="51f5a-460">Copy All as Fetch</span></span>** | &nbsp; |  
| **<span data-ttu-id="51f5a-461">Copy All as cURL</span><span class="sxs-lookup"><span data-stu-id="51f5a-461">Copy All as cURL</span></span>** | <span data-ttu-id="51f5a-462">Kopieren Sie alle Anforderungen als Kette von cURL-Befehlen.</span><span class="sxs-lookup"><span data-stu-id="51f5a-462">Copy all requests as a chain of cURL commands.</span></span> |  
| **<span data-ttu-id="51f5a-463">Copy All as HAR</span><span class="sxs-lookup"><span data-stu-id="51f5a-463">Copy All as HAR</span></span>** | <span data-ttu-id="51f5a-464">Kopieren Sie alle Anforderungen als HAR-Daten.</span><span class="sxs-lookup"><span data-stu-id="51f5a-464">Copy all requests as HAR data.</span></span> |  

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

:::image type="complex" source="../media/network-network-requests-copy-response.msft.png" alt-text="Wählen Sie Antwort kopieren aus" lightbox="../media/network-network-requests-copy-response.msft.png":::
   <span data-ttu-id="51f5a-466">Wählen Sie **Antwort kopieren aus**</span><span class="sxs-lookup"><span data-stu-id="51f5a-466">Choose **Copy Response**</span></span>  
:::image-end:::  

### <a name="copy-formatted-response-json-to-the-clipboard"></a><span data-ttu-id="51f5a-467">Formatierte Antwort-JSON in die Zwischenablage kopieren</span><span class="sxs-lookup"><span data-stu-id="51f5a-467">Copy formatted response JSON to the clipboard</span></span>  

<span data-ttu-id="51f5a-468">Wählen Sie eine Netzwerkanforderung aus, und navigieren Sie zum **Bereich Kopfzeilen.**</span><span class="sxs-lookup"><span data-stu-id="51f5a-468">Choose a network request and navigate to the **Headers** pane.</span></span>  <span data-ttu-id="51f5a-469">Navigieren Sie zum Kopieren des JSON-Werts einer Antwort zu Nutzlast **anfordern,** zeigen Sie auf den Inhalt der JSON-Antwort, öffnen Sie das Kontextmenü \(rechtsklicken\), und wählen Sie **Wert kopieren aus.**</span><span class="sxs-lookup"><span data-stu-id="51f5a-469">To copy the JSON value of a response, navigate to **Request payload**, hover on the JSON response content, open the contextual menu \(right-click\), and choose **Copy Value**.</span></span>  

:::row:::
   :::column span="":::
        :::image type="complex" source="../media/network-header-copy-property-value.msft.png" alt-text="Wert im Kontextmenü kopieren" lightbox="../media/network-header-copy-property-value.msft.png":::
          <span data-ttu-id="51f5a-471">**Wert im** Kontextmenü kopieren</span><span class="sxs-lookup"><span data-stu-id="51f5a-471">**Copy Value** in contextual menu</span></span>  
        :::image-end:::  
   :::column-end:::
   :::column span="":::
        :::image type="complex" source="../media/network-header-paste-property-value.msft.png" alt-text="Microsoft Visual Studio Code mit formatierter Antwort-JSON" lightbox="../media/network-header-paste-property-value.msft.png":::
          <span data-ttu-id="51f5a-473">Pasting formatted response JSON in Microsoft Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="51f5a-473">Pasting formatted response JSON in Microsoft Visual Studio Code</span></span>  
        :::image-end:::  
   :::column-end:::
:::row-end:::  

### <a name="copy-property-values-from-network-requests-to-your-clipboard"></a><span data-ttu-id="51f5a-474">Kopieren von Eigenschaftswerten aus Netzwerkanforderungen in die Zwischenablage</span><span class="sxs-lookup"><span data-stu-id="51f5a-474">Copy property values from network requests to your clipboard</span></span>  

<span data-ttu-id="51f5a-475">Führen Sie die folgenden Aktionen aus, um Eigenschaftswerte aus Netzwerkanforderungen in die Zwischenablage zu kopieren.</span><span class="sxs-lookup"><span data-stu-id="51f5a-475">To copy property values from network requests to your clipboard, complete the following actions.</span></span>  

1.  <span data-ttu-id="51f5a-476">Öffnen Sie den **Bereich Kopfzeilen.**</span><span class="sxs-lookup"><span data-stu-id="51f5a-476">Open the **Headers** pane.</span></span>  
1.  <span data-ttu-id="51f5a-477">Öffnen Sie einen der folgenden Kopfzeilenabschnitte.</span><span class="sxs-lookup"><span data-stu-id="51f5a-477">Open one of the following header sections.</span></span>  
    *   <span data-ttu-id="51f5a-478">Anforderungsnutzlast \(JSON\)</span><span class="sxs-lookup"><span data-stu-id="51f5a-478">Request payload \(JSON\)</span></span>  
    *   <span data-ttu-id="51f5a-479">Formulardaten</span><span class="sxs-lookup"><span data-stu-id="51f5a-479">Form Data</span></span>  
    *   <span data-ttu-id="51f5a-480">Abfragezeichenfolgenparameter</span><span class="sxs-lookup"><span data-stu-id="51f5a-480">Query String Parameters</span></span>  
    *   <span data-ttu-id="51f5a-481">Anforderungsheader</span><span class="sxs-lookup"><span data-stu-id="51f5a-481">Request Headers</span></span>  
    *   <span data-ttu-id="51f5a-482">Antwortheader</span><span class="sxs-lookup"><span data-stu-id="51f5a-482">Response Headers</span></span>  
1.  <span data-ttu-id="51f5a-483">Öffnen Sie das Kontextmenü \(klicken Sie mit der rechten Maustaste\) > **Wert kopieren**.</span><span class="sxs-lookup"><span data-stu-id="51f5a-483">Open the contextual menu \(right-click\) > **Copy value**.</span></span>  <span data-ttu-id="51f5a-484">Sie können den Wert nun in einen beliebigen Editor einfügen, um ihn zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="51f5a-484">You may now paste the value into any editor to review it.</span></span>  
    
## <a name="change-the-layout-of-the-network-panel"></a><span data-ttu-id="51f5a-485">Ändern des Layouts des Netzwerkbereichs</span><span class="sxs-lookup"><span data-stu-id="51f5a-485">Change the layout of the Network panel</span></span>  

<span data-ttu-id="51f5a-486">Sie können Abschnitte derBenutzeroberfläche des Netzwerktools erweitern oder reduzieren, um wichtige Informationen zu fokussieren.</span><span class="sxs-lookup"><span data-stu-id="51f5a-486">You may expand or collapse sections of the **Network** tool UI to focus important information.</span></span>  

### <a name="hide-the-filters-pane"></a><span data-ttu-id="51f5a-487">Ausblenden des Bereichs Filter</span><span class="sxs-lookup"><span data-stu-id="51f5a-487">Hide the Filters pane</span></span>  

<span data-ttu-id="51f5a-488">In DevTools wird standardmäßig der Bereich **Filter** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="51f5a-488">By default, DevTools show the **Filters** pane.</span></span>  
<span data-ttu-id="51f5a-489">Wählen **Sie Filter** \( Filter ![ ](../media/filter-icon.msft.png) \) aus, um ihn auszublenden.</span><span class="sxs-lookup"><span data-stu-id="51f5a-489">Choose **Filter** \(![Filter](../media/filter-icon.msft.png)\) to hide it.</span></span>  

:::image type="complex" source="../media/network-network-resources-hide-filters-button.msft.png" alt-text="Schaltfläche Filter ausblenden" lightbox="../media/network-network-resources-hide-filters-button.msft.png":::
   <span data-ttu-id="51f5a-491">Schaltfläche Filter ausblenden</span><span class="sxs-lookup"><span data-stu-id="51f5a-491">The Hide Filters button</span></span>  
:::image-end:::  

### <a name="use-large-request-rows"></a><span data-ttu-id="51f5a-492">Verwenden großer Anforderungszeilen</span><span class="sxs-lookup"><span data-stu-id="51f5a-492">Use large request rows</span></span>  

<span data-ttu-id="51f5a-493">Verwenden Sie große Zeilen, wenn Sie mehr Leerzeichen in ihrer Netzwerkanforderungentabelle wünschen.</span><span class="sxs-lookup"><span data-stu-id="51f5a-493">Use large rows when you want more whitespace in your network requests table.</span></span>  <span data-ttu-id="51f5a-494">Einige Spalten bieten auch ein wenig mehr Informationen, wenn große Zeilen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="51f5a-494">Some columns also provide a little more information when using large rows.</span></span>  <span data-ttu-id="51f5a-495">Der untere Wert der Spalte **Größe** ist beispielsweise die nicht komprimierte Größe einer Anforderung.</span><span class="sxs-lookup"><span data-stu-id="51f5a-495">For example, the bottom value of the **Size** column is the uncompressed size of a request.</span></span>  

:::image type="complex" source="../media/network-network-requests-large-request-rows.msft.png" alt-text="Ein Beispiel für große Anforderungszeilen im Bereich Anforderungen" lightbox="../media/network-network-requests-large-request-rows.msft.png":::
   <span data-ttu-id="51f5a-497">Ein Beispiel für große Anforderungszeilen im **Bereich Anforderungen**</span><span class="sxs-lookup"><span data-stu-id="51f5a-497">An example of large request rows in the **Requests** pane</span></span>  
:::image-end:::  

<span data-ttu-id="51f5a-498">Aktivieren Sie zum Aktivieren großer Zeilen das Kontrollkästchen **Große Anforderungszeilen** verwenden.</span><span class="sxs-lookup"><span data-stu-id="51f5a-498">To enable large rows, turn on the **Use large request rows** checkbox.</span></span>  

:::image type="complex" source="../media/network-network-requests-use-large-request-rows-on.msft.png" alt-text="Das Kontrollkästchen Große Anforderungszeilen verwenden" lightbox="../media/network-network-requests-use-large-request-rows-on.msft.png":::
   <span data-ttu-id="51f5a-500">Das **Kontrollkästchen Große Anforderungszeilen** verwenden</span><span class="sxs-lookup"><span data-stu-id="51f5a-500">The **Use large request rows** checkbox</span></span>  
:::image-end:::  

### <a name="hide-the-overview-pane"></a><span data-ttu-id="51f5a-501">Ausblenden des Übersichtsbereichs</span><span class="sxs-lookup"><span data-stu-id="51f5a-501">Hide the Overview pane</span></span>  

<span data-ttu-id="51f5a-502">Standardmäßig zeigt DevTools den Bereich **Übersicht** an.</span><span class="sxs-lookup"><span data-stu-id="51f5a-502">By default, DevTools displays the **Overview** pane.</span></span>  <span data-ttu-id="51f5a-503">Deaktivieren Sie zum Ausblenden das Kontrollkästchen **Übersicht** anzeigen.</span><span class="sxs-lookup"><span data-stu-id="51f5a-503">To hide it, turn off the **Show Overview** checkbox.</span></span>  

:::image type="complex" source="../media/network-network-requests-show-overview-off.msft.png" alt-text="Das Kontrollkästchen Übersicht anzeigen" lightbox="../media/network-network-requests-show-overview-off.msft.png":::
   <span data-ttu-id="51f5a-505">Das **Kontrollkästchen Übersicht** anzeigen</span><span class="sxs-lookup"><span data-stu-id="51f5a-505">The **Show Overview** checkbox</span></span>  
:::image-end:::  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="51f5a-506">Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen</span><span class="sxs-lookup"><span data-stu-id="51f5a-506">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsProgressiveWebApps]: ../progressive-web-apps/index.md "Debuggen von Progressive Web Apps | Microsoft Docs"  

<!--[NetworkConditions]: /microsoft-edge/devtools-guide-chromium/network/network-conditions "Optimize Performance Under Varying Network Conditions | Microsoft Docs"  -->  

[MDNHTTPDataURIs]: https://developer.mozilla.org/docs/Web/HTTP/Basics_of_HTTP/Data_URIs "Daten-URLs | MDN"  

[WikiProxyServer]: https://en.wikipedia.org/wiki/Proxy_server "Proxyserver – Wikipedia"  

> [!NOTE]
> <span data-ttu-id="51f5a-510">Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="51f5a-510">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="51f5a-511">Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/network/reference) und wird von [Kayce Basken][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\) verfasst.</span><span class="sxs-lookup"><span data-stu-id="51f5a-511">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/network/reference) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="51f5a-513">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="51f5a-513">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  
