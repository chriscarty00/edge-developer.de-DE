---
description: FEATURES für das Debuggen von CSS-Rastern, Bearbeiten und Wiedergeben von Anforderungen mit der Netzwerkkonsole und vieles mehr.
title: Neues in DevTools (Microsoft Edge 85)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, Entwicklungstools
ms.openlocfilehash: 3085153b87f09c1b5aba8fbe43c42cef0851fa9c
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "11397755"
---
# <a name="whats-new-in-devtools-microsoft-edge-85"></a><span data-ttu-id="60a57-104">Neues in DevTools (Microsoft Edge 85)</span><span class="sxs-lookup"><span data-stu-id="60a57-104">What's New In DevTools (Microsoft Edge 85)</span></span>  

## <a name="announcements-from-the-microsoft-edge-devtools-team"></a><span data-ttu-id="60a57-105">Ankündigungen des Microsoft Edge DevTools-Teams</span><span class="sxs-lookup"><span data-stu-id="60a57-105">Announcements from the Microsoft Edge DevTools team</span></span>  

<span data-ttu-id="60a57-106">Die folgenden Abschnitte sind eine Liste der Ankündigungen, die Sie möglicherweise vom Microsoft Edge DevTools-Team verpasst haben.</span><span class="sxs-lookup"><span data-stu-id="60a57-106">The following sections are a list of announcements you may have missed from the Microsoft Edge DevTools team.</span></span>  <span data-ttu-id="60a57-107">Sehen Sie sich die Ankündigungen an, um neue Features in devTools, Microsoft Visual Studio Codeerweiterungen zu testen und vieles mehr.</span><span class="sxs-lookup"><span data-stu-id="60a57-107">Check out the announcements to try new features in the DevTools, Microsoft Visual Studio Code extensions, and more.</span></span>  <span data-ttu-id="60a57-108">Laden Sie die Microsoft Edge-Vorschaukanäle herunter, und folgen [][MicrosoftEdgePreviewChannels] Sie dem [Microsoft Edge DevTools-Team auf Twitter,][EdgeDevToolsTwitterAccount]um auf dem neuesten Stand zu bleiben.</span><span class="sxs-lookup"><span data-stu-id="60a57-108">To stay up to date on all the latest and greatest features in your developer tools, download the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] and [follow the Microsoft Edge DevTools team on Twitter][EdgeDevToolsTwitterAccount].</span></span>  

### <a name="css-grid-debugging-features"></a><span data-ttu-id="60a57-109">Features zum Debuggen von CSS-Rastern</span><span class="sxs-lookup"><span data-stu-id="60a57-109">CSS grid debugging features</span></span>  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Experimentelles Feature":::
   <span data-ttu-id="60a57-111">Experimentelles Feature</span><span class="sxs-lookup"><span data-stu-id="60a57-111">Experimental feature</span></span>  
:::image-end:::  

<span data-ttu-id="60a57-112">Das Microsoft Edge DevTools-Team arbeitet mit dem Chrome DevTools-Team und der Chromium-Community zusammen, um DevTools neue FEATURES für das CSS-Rasterdebuding hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="60a57-112">The Microsoft Edge DevTools team is collaborating with the Chrome DevTools team and Chromium community to add new CSS grid debugging features to DevTools.</span></span>  <span data-ttu-id="60a57-113">Sie können nun Gitternetzliniennummern, Gitternetzlücken und erweiterte Gitternetzlinien als on-page-Überlagerung anzeigen.</span><span class="sxs-lookup"><span data-stu-id="60a57-113">You are now able to display grid line numbers, grid gaps, and extended grid lines as an on-page overlay.</span></span>  <span data-ttu-id="60a57-114">Darüber hinaus werden in Kürze weitere Verbesserungen an den Rastertools vorgenommen.</span><span class="sxs-lookup"><span data-stu-id="60a57-114">Plus, more improvements to the grid tools are coming soon.</span></span>  

:::image type="complex" source="../../media/2020/06/experiments-grid.msft.png" alt-text="Features zum Debuggen von CSS-Rastern" lightbox="../../media/2020/06/experiments-grid.msft.png":::
   <span data-ttu-id="60a57-116">Features zum Debuggen von CSS-Rastern</span><span class="sxs-lookup"><span data-stu-id="60a57-116">CSS grid debugging features</span></span>
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="60a57-117">Navigieren Sie zum Aktivieren des Experiments zu Aktivieren experimenteller [Features,][DevtoolsExperimentalFeaturesTurnOn] und aktivieren Sie das Kontrollkästchen neben **Neue CSS Grid-Debuggingfeatures aktivieren.**</span><span class="sxs-lookup"><span data-stu-id="60a57-117">To enable the experiment, navigate to [Turn on experimental features][DevtoolsExperimentalFeaturesTurnOn] and select the checkbox next to **Enable new CSS Grid debugging features**.</span></span>  
> 
> <span data-ttu-id="60a57-118">Wenn Sie das Experiment mit einem Beispiel ausprobieren möchten, navigieren Sie zu [CSS Grid Planner(Beispiel).][CodepenRachelweilYzwBzKM]</span><span class="sxs-lookup"><span data-stu-id="60a57-118">To try out the experiment with a sample, navigate to [CSS Grid planner example][CodepenRachelweilYzwBzKM].</span></span>  

<span data-ttu-id="60a57-119">[Chromium-Problem #1047356][CR1047356]</span><span class="sxs-lookup"><span data-stu-id="60a57-119">Chromium issue [#1047356][CR1047356]</span></span>  

### <a name="edit-and-replay-requests-with-the-network-console"></a><span data-ttu-id="60a57-120">Bearbeiten und Wiedergeben von Anforderungen mit der Netzwerkkonsole</span><span class="sxs-lookup"><span data-stu-id="60a57-120">Edit and Replay requests with the Network Console</span></span>  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Experimentelles Feature":::
   <span data-ttu-id="60a57-122">Experimentelles Feature</span><span class="sxs-lookup"><span data-stu-id="60a57-122">Experimental feature</span></span>  
:::image-end:::  

<span data-ttu-id="60a57-123">Sie können jetzt \*\*\*\* Bearbeiten und Wiedergeben für Anforderungen im [Netzwerkprotokoll][DevtoolsNetworkIndexLogActivity] mithilfe der **Netzwerkkonsole verwenden.**</span><span class="sxs-lookup"><span data-stu-id="60a57-123">You are now able to use **Edit and Replay** on requests in the [Network Log][DevtoolsNetworkIndexLogActivity] using the **Network Console**.</span></span>  

:::image type="complex" source="../../media/2020/06/experiments-network-console-edit-and-replay.msft.png" alt-text="Bearbeiten und Wiedergeben einer Anforderung im NetworkLog mit der Netzwerkkonsole" lightbox="../../media/2020/06/experiments-network-console-edit-and-replay.msft.png":::
   <span data-ttu-id="60a57-125">Bearbeiten und Wiedergeben einer Anforderung im [NetworkLog mit][DevtoolsNetworkIndexLogActivity] der **Netzwerkkonsole**</span><span class="sxs-lookup"><span data-stu-id="60a57-125">Edit and Replay a request in the [NetworkLog][DevtoolsNetworkIndexLogActivity] with the **Network Console**</span></span>  
:::image-end:::  

<span data-ttu-id="60a57-126">Ein neuer Bereich, die **Netzwerkkonsole** wird in der [DevTools-Schublade][DevtoolsCustomizeIndexDrawer] geöffnet und automatisch mit Informationen für die HTTP-Anforderung auffüllt.</span><span class="sxs-lookup"><span data-stu-id="60a57-126">A new panel, the **Network Console** opens in the [DevTools Drawer][DevtoolsCustomizeIndexDrawer] and automatically populates with information for the HTTP request.</span></span>  <span data-ttu-id="60a57-127">Bearbeiten Sie die Anforderung \(falls erforderlich\), und wählen Sie Senden aus, um die vom Server zurückgegebene Antwort **anzeigen zu können.**</span><span class="sxs-lookup"><span data-stu-id="60a57-127">To display the response returned from the server, edit the request \(if needed\) and select **Send**.</span></span>  

<span data-ttu-id="60a57-128">Sie können auch die **Netzwerkkonsole verwenden,** um HTTP-Anforderungen direkt von devTools zu erstellen und zu senden.</span><span class="sxs-lookup"><span data-stu-id="60a57-128">You may also use the **Network Console** to create and send HTTP requests directly from the DevTools.</span></span>  

:::image type="complex" source="../../media/2020/06/experiments-network-console.msft.png" alt-text="Netzwerkkonsolenbereich" lightbox="../../media/2020/06/experiments-network-console.msft.png":::
   <span data-ttu-id="60a57-130">**Netzwerkkonsolenbereich**</span><span class="sxs-lookup"><span data-stu-id="60a57-130">The **Network Console** panel</span></span>  
:::image-end:::  

> [!TIP]
> <span data-ttu-id="60a57-131">Navigieren Sie **zum** Verschieben von Tools zwischen Den Panels, um die Netzwerkkonsole im Hauptbereich \(top\) anstelle der [DevTools-Drawer][DevtoolsCustomizeIndexDrawer] [anzeigen zu können.](#move-tools-between-panels)</span><span class="sxs-lookup"><span data-stu-id="60a57-131">To display **Network Console** in the main \(top\) panel instead of the [DevTools Drawer][DevtoolsCustomizeIndexDrawer], navigate to [moving tools between panels](#move-tools-between-panels).</span></span>  

> [!NOTE]
> <span data-ttu-id="60a57-132">Navigieren Sie zum Aktivieren des Experiments zu Aktivieren experimenteller [Features,][DevtoolsExperimentalFeaturesTurnOn] und aktivieren Sie das Kontrollkästchen neben **Netzwerkkonsole aktivieren.**</span><span class="sxs-lookup"><span data-stu-id="60a57-132">To enable the experiment, navigate to [Turn on experimental features][DevtoolsExperimentalFeaturesTurnOn] and choose the checkbox next to **Enable Network Console**.</span></span>  
> 
> <span data-ttu-id="60a57-133">Öffnen Sie [das Netzwerkprotokoll,][DevtoolsNetworkIndexLogActivity]öffnen Sie das Kontextmenü \(klicken Sie mit der rechten Maustaste\), und wählen Sie **Bearbeiten und Wiedergabe aus.**</span><span class="sxs-lookup"><span data-stu-id="60a57-133">Open the [Network Log][DevtoolsNetworkIndexLogActivity], open the contextual menu \(right-click\), and choose **Edit and Replay**.</span></span>  

<span data-ttu-id="60a57-134">[Chromium-#1093687][CR1093687]</span><span class="sxs-lookup"><span data-stu-id="60a57-134">Chromium issue [#1093687][CR1093687]</span></span>  

### <a name="service-worker-respondwith-events-in-the-timing-tab"></a><span data-ttu-id="60a57-135">Service worker respondWith events in the Timing tab</span><span class="sxs-lookup"><span data-stu-id="60a57-135">Service worker respondWith events in the Timing tab</span></span>  

<span data-ttu-id="60a57-136">Die **Registerkarte Timing** des **Netzwerktools** enthält jetzt `respondWith` Dienstarbeitsereignisse.</span><span class="sxs-lookup"><span data-stu-id="60a57-136">The **Timing** tab of the **Network** tool now includes `respondWith` service worker events.</span></span>  <span data-ttu-id="60a57-137">Das Service Worker-Ereignis zeigt die Dauer von der Zeit unmittelbar vor dem Ausführen des Service Worker-Ereignishandlers bis zu dem Zeitpunkt an, zu dem die Zusage des `respondWith` `fetch` `respondWith` `fetch` Handlers abgerechnet wird.</span><span class="sxs-lookup"><span data-stu-id="60a57-137">The `respondWith` service worker event shows the duration from the time immediately before the service worker `fetch` event handler starts running to the time when the `respondWith` promise of the `fetch` handler is settled.</span></span>  

:::image type="complex" source="../../media/2020/06/timing-tab.msft.png" alt-text="Das RespondWith-Dienstarbeitsereignis auf der Registerkarte Timing des Netzwerkbereichs" lightbox="../../media/2020/06/timing-tab.msft.png":::
   <span data-ttu-id="60a57-139">Das `respondWith` Dienstarbeitsereignis auf der **Registerkarte Timing** des **Netzwerktools**</span><span class="sxs-lookup"><span data-stu-id="60a57-139">The `respondWith` service worker event in the **Timing** tab of the **Network** tool</span></span>  
:::image-end:::  

<span data-ttu-id="60a57-140">Erweitern **Sie die empfangene** Antwort, um zusätzliche Informationen aus der `fetch` Antwort wie , und zu `CacheStorageCacheName` `serviceWorkerResponseSource` `ResponseTime` anzeigen.</span><span class="sxs-lookup"><span data-stu-id="60a57-140">Expand **Response received** to display additional information from the `fetch` response like `CacheStorageCacheName`, `serviceWorkerResponseSource`, and `ResponseTime`.</span></span>  

:::image type="complex" source="../../media/2020/06/timing-tab2.msft.png" alt-text="Expand Response received to display additional information from the fetch response" lightbox="../../media/2020/06/timing-tab2.msft.png":::
   <span data-ttu-id="60a57-142">Expand **Response received** to display additional information from the `fetch` response</span><span class="sxs-lookup"><span data-stu-id="60a57-142">Expand **Response received** to display additional information from the `fetch` response</span></span>  
:::image-end:::  

<span data-ttu-id="60a57-143">[Chromium-Problem #1066579][CR1066579]</span><span class="sxs-lookup"><span data-stu-id="60a57-143">Chromium issue [#1066579][CR1066579]</span></span>  

### <a name="webhint-feedback-in-the-issues-panel"></a><span data-ttu-id="60a57-144">Webhintfeedback im Problembereich</span><span class="sxs-lookup"><span data-stu-id="60a57-144">webhint feedback in the Issues panel</span></span>  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Experimentelles Feature":::
   <span data-ttu-id="60a57-146">Experimentelles Feature</span><span class="sxs-lookup"><span data-stu-id="60a57-146">Experimental feature</span></span>  
:::image-end:::  

<span data-ttu-id="60a57-147">[webhint][WebhintMain] ist ein Open-Source-Tool, das Feedback in Echtzeit zu Barrierefreiheit, browserübergreifender Kompatibilität, Sicherheit, Leistung, PWAs und anderen allgemeinen Webentwicklungsproblemen von Websites liefert.</span><span class="sxs-lookup"><span data-stu-id="60a57-147">[webhint][WebhintMain] is an open-source tool that provides real-time feedback on the accessibility, cross-browser compatibility, security, performance, PWAs, and other common web development issues of websites.</span></span>  <span data-ttu-id="60a57-148">So überprüfen Sie das Webhintfeedback im [Bereich Probleme.][DevtoolsIssues]</span><span class="sxs-lookup"><span data-stu-id="60a57-148">To review webhint feedback in the [Issues][DevtoolsIssues] panel.</span></span>  

:::image type="complex" source="../../media/2020/06/experiments-webhint.msft.png" alt-text="Webhintfeedback im Problembereich" lightbox="../../media/2020/06/experiments-webhint.msft.png":::
   <span data-ttu-id="60a57-150">Webhintfeedback im Problembereich</span><span class="sxs-lookup"><span data-stu-id="60a57-150">webhint feedback in the Issues panel</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="60a57-151">Navigieren Sie zum Aktivieren des Experiments zu Aktivieren experimenteller [Features,][DevtoolsExperimentalFeaturesTurnOn] und aktivieren Sie das Kontrollkästchen neben **Webhint aktivieren.**</span><span class="sxs-lookup"><span data-stu-id="60a57-151">To enable the experiment, navigate to [Turn on experimental features][DevtoolsExperimentalFeaturesTurnOn] and choose the checkbox next to **Enable webhint**.</span></span>  
> 
> <span data-ttu-id="60a57-152">Öffnen Sie den [Bereich][DevtoolsIssues] Probleme, um Feedback von Webhint einblenden zu können.</span><span class="sxs-lookup"><span data-stu-id="60a57-152">Open the [Issues][DevtoolsIssues] panel to display feedback from webhint.</span></span>  

<span data-ttu-id="60a57-153">[Chromium-#1070378][CR1070378]</span><span class="sxs-lookup"><span data-stu-id="60a57-153">Chromium issue [#1070378][CR1070378]</span></span>  

### <a name="move-tools-between-panels"></a><span data-ttu-id="60a57-154">Verschieben von Tools zwischen Panels</span><span class="sxs-lookup"><span data-stu-id="60a57-154">Move tools between panels</span></span>  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Experimentelles Feature":::
   <span data-ttu-id="60a57-156">Experimentelles Feature</span><span class="sxs-lookup"><span data-stu-id="60a57-156">Experimental feature</span></span>  
:::image-end:::  

<span data-ttu-id="60a57-157">Normalerweise können Tools wie **Elemente** und **Netzwerk** nur im Hauptbereich \(top\) von DevTools geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="60a57-157">Normally, tools such as **Elements** and **Network** may only be opened in the main \(top\) panel of DevTools.</span></span>  <span data-ttu-id="60a57-158">Ebenso können Tools wie **3D-Ansicht** und Probleme nur im Drawer \(bottom\)-Bereich von DevTools geöffnet werden. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="60a57-158">Similarly, tools such as **3D View** and **Issues** may only be opened in the drawer \(bottom\) panel of DevTools.</span></span>  <span data-ttu-id="60a57-159">Sie können nun Ihr DevTools-Layout anpassen, indem Sie Tools zwischen dem oberen und unteren Bereich verschieben.</span><span class="sxs-lookup"><span data-stu-id="60a57-159">You are now able to customize your DevTools layout by moving tools between the top and bottom panels.</span></span>  

:::image type="complex" source="../../media/2020/06/experiments-move-panels.msft.png" alt-text="Verschieben von Tools zwischen Panels" lightbox="../../media/2020/06/experiments-move-panels.msft.png":::
   <span data-ttu-id="60a57-161">Verschieben von Tools zwischen Panels</span><span class="sxs-lookup"><span data-stu-id="60a57-161">Move tools between panels</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="60a57-162">Navigieren Sie zum Aktivieren des Experiments zu Aktivieren experimenteller [Features,][DevtoolsExperimentalFeaturesTurnOn] und aktivieren Sie das Kontrollkästchen neben Unterstützung aktivieren, um **Registerkarten zwischen Panels zu verschieben.**</span><span class="sxs-lookup"><span data-stu-id="60a57-162">To enable the experiment, navigate to [Turn on experimental features][DevtoolsExperimentalFeaturesTurnOn] and choose the checkbox next to **Enable support to move tabs between panels**.</span></span>  

<span data-ttu-id="60a57-163">[Chromium-Problem #897944][CR897944]</span><span class="sxs-lookup"><span data-stu-id="60a57-163">Chromium issue [#897944][CR897944]</span></span>  

### <a name="improved-initiator-tooltip-in-the-network-panel"></a><span data-ttu-id="60a57-164">Verbesserte Initiator-QuickInfo im Netzwerkbereich</span><span class="sxs-lookup"><span data-stu-id="60a57-164">Improved Initiator tooltip in the Network panel</span></span>  

<span data-ttu-id="60a57-165">In Microsoft Edge 83 und 84 werden QuickInfos für die Spalte Initiator, die die Ursache der Ressourcenanforderung zeigt, im [Netzwerkprotokoll][DevtoolsNetworkIndexLogActivity] angezeigt, das mit einer horizontalen Bildlaufleiste angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="60a57-165">In Microsoft Edge 83 and 84, tooltips for the Initiator column, which shows the cause of the resource request, in the [Network Log][DevtoolsNetworkIndexLogActivity] displayed with a horizontal scrollbar.</span></span>  <span data-ttu-id="60a57-166">Sie konnten nur die Aufrufliste anzeigen, die die Anforderung initiiert hat, indem Sie einen horizontalen Bildlauf in der QuickInfo durchführen.</span><span class="sxs-lookup"><span data-stu-id="60a57-166">You were only able to display the call stack that initiated the request by scrolling horizontally in the tooltip.</span></span>  

:::image type="complex" source="../../media/2020/06/initiator-tooltip-84.msft.png" alt-text="Die QuickInfo "Initiator" in Microsoft Edge 84" lightbox="../../media/2020/06/initiator-tooltip-84.msft.png":::
   <span data-ttu-id="60a57-168">Die QuickInfo "Initiator" in Microsoft Edge 84</span><span class="sxs-lookup"><span data-stu-id="60a57-168">The Initiator tooltip in Microsoft Edge 84</span></span>  
:::image-end:::  

<span data-ttu-id="60a57-169">Ab Microsoft Edge 85 können Sie nun die Aufrufliste des Initiators in der QuickInfo ohne horizontalen Bildlauf anzeigen.</span><span class="sxs-lookup"><span data-stu-id="60a57-169">Starting with Microsoft Edge 85, you are now able to display the Initiator call stack in the tooltip without scrolling horizontally.</span></span>  

:::image type="complex" source="../../media/2020/06/initiator-tooltip-85.msft.png" alt-text="Die QuickInfo "Initiator" in Microsoft Edge 85" lightbox="../../media/2020/06/initiator-tooltip-85.msft.png":::
   <span data-ttu-id="60a57-171">Die QuickInfo "Initiator" in Microsoft Edge 85</span><span class="sxs-lookup"><span data-stu-id="60a57-171">The Initiator tooltip in Microsoft Edge 85</span></span>
:::image-end:::  

<span data-ttu-id="60a57-172">[Chromium-#1069404][CR1069404]</span><span class="sxs-lookup"><span data-stu-id="60a57-172">Chromium issue [#1069404][CR1069404]</span></span>  

## <a name="announcements-from-the-chromium-project"></a><span data-ttu-id="60a57-173">Ankündigungen aus dem Chromium-Projekt</span><span class="sxs-lookup"><span data-stu-id="60a57-173">Announcements from the Chromium project</span></span>  

<span data-ttu-id="60a57-174">In den folgenden Abschnitten werden zusätzliche Features angekündigt, die in Microsoft Edge 85 verfügbar sind und zum Open Source Chromium-Projekt beigetragen haben.</span><span class="sxs-lookup"><span data-stu-id="60a57-174">The following sections announce additional features available in Microsoft Edge 85 that were contributed to the open source Chromium project.</span></span>  

### <a name="style-editing-for-css-in-js-frameworks"></a><span data-ttu-id="60a57-175">Formatvorlagenbearbeitung für CSS-in-JS-Frameworks</span><span class="sxs-lookup"><span data-stu-id="60a57-175">Style editing for CSS-in-JS frameworks</span></span>  

<span data-ttu-id="60a57-176">Der **Bereich** Formatvorlagen bietet nun eine bessere Unterstützung für Bearbeitungsstile, die mit den [CSSOM-APIs (CSSOM)][CsswgDraftsCssom] erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="60a57-176">The **Styles** pane now has better support for editing styles that were created with the [CSS Object Model (CSSOM)][CsswgDraftsCssom] APIs.</span></span>  <span data-ttu-id="60a57-177">Viele CSS-in-JS-Frameworks und -Bibliotheken verwenden die CSSOM-APIs unter der Blende, um Formatvorlagen zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="60a57-177">Many CSS-in-JS frameworks and libraries use the CSSOM APIs under the hood to construct styles.</span></span>  

<span data-ttu-id="60a57-178">Sie können jetzt in JavaScript hinzugefügte Formatvorlagen mithilfe [von Constructable Stylesheets bearbeiten.][WicgConstructStylesheet]</span><span class="sxs-lookup"><span data-stu-id="60a57-178">You are now able to edit styles added in JavaScript using [Constructable Stylesheets][WicgConstructStylesheet].</span></span>  <span data-ttu-id="60a57-179">Constructable Stylesheets sind eine neue Möglichkeit zum Erstellen und Verteilen wiederverwendbarer Formatvorlagen bei Verwendung von [Shadow DOM][MdnShadowDom].</span><span class="sxs-lookup"><span data-stu-id="60a57-179">Constructable Stylesheets are a new way to create and distribute reusable styles when using [Shadow DOM][MdnShadowDom].</span></span>  

<span data-ttu-id="60a57-180">Beispielsweise waren die `h1` mit `CSSStyleSheet` \(CSSOM-APIs\) hinzugefügten Formatvorlagen zuvor nicht bearbeitbar.</span><span class="sxs-lookup"><span data-stu-id="60a57-180">For example, the `h1` styles added with `CSSStyleSheet` \(CSSOM APIs\) were not editable previously.</span></span>  <span data-ttu-id="60a57-181">Die Formatvorlagen können jetzt im **Formatvorlagenbereich bearbeitet** werden.</span><span class="sxs-lookup"><span data-stu-id="60a57-181">The styles are editable now in the **Styles** panel.</span></span>  

:::image type="complex" source="../../media/2020/06/css-in-js.msft.png" alt-text="Ändern der Hintergrundeigenschaft der mit CSSStyleSheet hinzugefügten h1-Formatvorlagen von pink in lightblue" lightbox="../../media/2020/06/css-in-js.msft.png":::
   <span data-ttu-id="60a57-183">Ändern der `background` Eigenschaft der `h1` mit hinzugefügten `CSSStyleSheet` Formatvorlagen in `pink` `lightblue` .</span><span class="sxs-lookup"><span data-stu-id="60a57-183">Changing the `background` property of the `h1` styles added with `CSSStyleSheet` from `pink` to `lightblue`.</span></span>
:::image-end:::  

<span data-ttu-id="60a57-184">Testen Sie dieses Feature mit einem [Beispiel, das CSS-in-JS verwendet.][CodepenZoherghadyaliAbdgrpz]</span><span class="sxs-lookup"><span data-stu-id="60a57-184">Give this feature a try with a [sample that uses CSS-in-JS][CodepenZoherghadyaliAbdgrpz].</span></span>

<span data-ttu-id="60a57-185">[Chromium-#946975][CR946975]</span><span class="sxs-lookup"><span data-stu-id="60a57-185">Chromium issue [#946975][CR946975]</span></span>  

### <a name="lighthouse-6-in-the-lighthouse-panel"></a><span data-ttu-id="60a57-186">Leuchtturm 6 im Leuchtturmpanel</span><span class="sxs-lookup"><span data-stu-id="60a57-186">Lighthouse 6 in the Lighthouse panel</span></span>  

<span data-ttu-id="60a57-187">Im **Bereich "Leuchttürme"** wird jetzt "6" ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="60a57-187">The **Lighthouse** panel is now running Lighthouse 6.</span></span>  <span data-ttu-id="60a57-188">Eine vollständige Liste aller Änderungen finden Sie unter [Versionshinweise zu v6.0.0][GithubGoogleChromeLighthouse600].</span><span class="sxs-lookup"><span data-stu-id="60a57-188">For a full list of all changes, navigate to [v6.0.0 release notes][GithubGoogleChromeLighthouse600].</span></span>  

<span data-ttu-id="60a57-189">Mit Dem Bericht von "Farot 6.0" werden drei neue Metriken hinzugefügt: "Largest Contentful Paint \(LCP\"), Cumulative Layout Shift \(CLS\) und Total Blocking Time \(TBT\).</span><span class="sxs-lookup"><span data-stu-id="60a57-189">Lighthouse 6.0 introduces three new metrics to the report:  Largest Contentful Paint \(LCP\), Cumulative Layout Shift \(CLS\), and Total Blocking Time \(TBT\).</span></span>  

<span data-ttu-id="60a57-190">Die Formel für die Leistungspunktzahl wurde ebenfalls neu gewichtet, um die Ladeerfahrung des Benutzers besser widerspiegeln zu können.</span><span class="sxs-lookup"><span data-stu-id="60a57-190">The performance score formula has also been reweighted to better reflect the loading experience of the user.</span></span>  

<span data-ttu-id="60a57-191">[Chromium-#772558][CR772558]</span><span class="sxs-lookup"><span data-stu-id="60a57-191">Chromium issue [#772558][CR772558]</span></span>  

#### <a name="first-meaningful-paint-deprecation"></a><span data-ttu-id="60a57-192">First Meaningful Paint deprecation</span><span class="sxs-lookup"><span data-stu-id="60a57-192">First Meaningful Paint deprecation</span></span>  

<span data-ttu-id="60a57-193">First Meaningful Paint \(FMP\) ist in "6.0" veraltet.</span><span class="sxs-lookup"><span data-stu-id="60a57-193">First Meaningful Paint \(FMP\) is deprecated in Lighthouse 6.0.</span></span>  <span data-ttu-id="60a57-194">FMP wurde auch aus dem Bereich **Leistung** entfernt.</span><span class="sxs-lookup"><span data-stu-id="60a57-194">FMP has also been removed from the **Performance** panel.</span></span>  <span data-ttu-id="60a57-195">**Die größte Inhaltsfarbe** ist der empfohlene Ersatz für FMP.</span><span class="sxs-lookup"><span data-stu-id="60a57-195">**Largest Contentful Paint** is the recommended replacement for FMP.</span></span>  <!--For an explanation of why it was deprecated, navigate to [First Meaningful Paint][WebDevFirstMeaningfulPaint].  -->  

<!--todo: add Largest Contentful Paint when section available  -->  
<!--todo: add First Meaningful Paint link and note when available  -->  

<span data-ttu-id="60a57-196">[Chromium-Problem #1096008][CR1096008]</span><span class="sxs-lookup"><span data-stu-id="60a57-196">Chromium issue [#1096008][CR1096008]</span></span>  

### <a name="support-for-new-javascript-features"></a><span data-ttu-id="60a57-197">Unterstützung für neue JavaScript-Features</span><span class="sxs-lookup"><span data-stu-id="60a57-197">Support for new JavaScript features</span></span>  

<span data-ttu-id="60a57-198">DevTools bietet jetzt eine bessere Unterstützung für einige der neuesten JavaScript-Sprachfeatures.</span><span class="sxs-lookup"><span data-stu-id="60a57-198">DevTools now has better support for some of the latest JavaScript language features.</span></span>  

:::row:::
   :::column span="1":::
      <span data-ttu-id="60a57-199">[Optionale Verkettungssyntax][V8DevOptionalChaining] autocompletion</span><span class="sxs-lookup"><span data-stu-id="60a57-199">[Optional chaining][V8DevOptionalChaining] syntax autocompletion</span></span>  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="60a57-200">Die automatische Vervollständigung der Eigenschaft in der **Konsole** unterstützt jetzt optionale Verkettungssyntax, z. B. funktioniert jetzt  `name?.` zusätzlich zu und `name.` `name[` .</span><span class="sxs-lookup"><span data-stu-id="60a57-200">Property auto-completion in the **Console** now supports optional chaining syntax, for example,  `name?.` now works in addition to `name.` and `name[`.</span></span>  
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="1":::
      <span data-ttu-id="60a57-201">Syntaxhervor hervorheben für [private Felder][V8DevClassFieldsPrivate]</span><span class="sxs-lookup"><span data-stu-id="60a57-201">Syntax highlighting for [private fields][V8DevClassFieldsPrivate]</span></span>  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="60a57-202">Felder für private Klassen sind nun ordnungsgemäß syntax hervorgehoben und im Bereich Quellen ziemlich **gedruckt.**</span><span class="sxs-lookup"><span data-stu-id="60a57-202">private class fields are now properly syntax-highlighted and pretty-printed in the **Sources** panel.</span></span>  
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="1":::
      <span data-ttu-id="60a57-203">Syntaxhervor hervorheben für [#A0][V8DevNullishCoalescing]</span><span class="sxs-lookup"><span data-stu-id="60a57-203">Syntax highlighting for [Nullish coalescing operator][V8DevNullishCoalescing]</span></span>
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="60a57-204">DevTools druckt jetzt den Nullish-Koeescing-Operator im **Bereich Quellen ordnungsgemäß.**</span><span class="sxs-lookup"><span data-stu-id="60a57-204">DevTools now properly pretty-prints the nullish coalescing operator in the **Sources** panel.</span></span>  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="60a57-205">[Chromium-Probleme #1073903][CR1073903], [#1083214][CR1083214], [#1083797][CR1083797]</span><span class="sxs-lookup"><span data-stu-id="60a57-205">Chromium issues [#1073903][CR1073903], [#1083214][CR1083214], [#1083797][CR1083797]</span></span>  

### <a name="new-app-shortcut-warnings-in-the-manifest-pane"></a><span data-ttu-id="60a57-206">Warnungen für neue App-Verknüpfungen im Manifestbereich</span><span class="sxs-lookup"><span data-stu-id="60a57-206">New app shortcut warnings in the Manifest pane</span></span>  

<span data-ttu-id="60a57-207">**Mithilfe von App-Verknüpfungen** können Benutzer häufige oder empfohlene Aufgaben in einer Web-App schnell starten.</span><span class="sxs-lookup"><span data-stu-id="60a57-207">**App shortcuts** help users quickly start common or recommended tasks within a web app.</span></span>  

<!--todo: add App shortcuts when section is live  -->  

<span data-ttu-id="60a57-208">Der **Manifestbereich** zeigt nun Warnungen für die folgenden Bedingungen an.</span><span class="sxs-lookup"><span data-stu-id="60a57-208">The **Manifest** pane now shows warnings for the following conditions.</span></span>  

* <span data-ttu-id="60a57-209">Die App-Verknüpfungssymbole sind kleiner als 96 x 96 Pixel</span><span class="sxs-lookup"><span data-stu-id="60a57-209">The app shortcut icons are smaller than 96x96 pixels</span></span>  
* <span data-ttu-id="60a57-210">Die App-Verknüpfungssymbole und Manifestsymbole sind nicht quadratisch \(da die Symbole ignoriert werden\)</span><span class="sxs-lookup"><span data-stu-id="60a57-210">The app shortcut icons and manifest icons are not square \(since the icons are ignored\)</span></span>  

:::image type="complex" source="../../media/2020/06/app-shortcut-warnings.msft.png" alt-text="Warnungen zu App-Verknüpfungen" lightbox="../../media/2020/06/app-shortcut-warnings.msft.png":::
   <span data-ttu-id="60a57-212">Warnungen zu App-Verknüpfungen</span><span class="sxs-lookup"><span data-stu-id="60a57-212">App shortcut warnings</span></span>  
:::image-end:::  

<span data-ttu-id="60a57-213">[Chromium-Problem #955497][CR955497]</span><span class="sxs-lookup"><span data-stu-id="60a57-213">Chromium issue [#955497][CR955497]</span></span>  

### <a name="consistent-display-of-the-computed-pane"></a><span data-ttu-id="60a57-214">Konsistente Anzeige des Berechneten Bereichs</span><span class="sxs-lookup"><span data-stu-id="60a57-214">Consistent display of the Computed pane</span></span>  

<span data-ttu-id="60a57-215">Der **Berechnete** Bereich im **Elementtool** wird nun konsistent als Bereich in allen Ansichtsfenstergrößen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="60a57-215">The **Computed** pane in the **Elements** tool now displays consistently as a pane across all viewport sizes.</span></span>  <span data-ttu-id="60a57-216">Zuvor wurde **der Berechnete** Bereich im Bereich **Formatvorlagen** zusammengeführt, wenn die Breite des DevTools-Viewports schmal war.</span><span class="sxs-lookup"><span data-stu-id="60a57-216">Previously the **Computed** pane merged inside the **Styles** pane when the width of the DevTools viewport was narrow.</span></span>  

:::image type="complex" source="../../media/2020/06/computed-pane.msft.png" alt-text="Der Berechnete Bereich wird konsistent als separater Bereich angezeigt, auch wenn die DevTools schmal sind" lightbox="../../media/2020/06/computed-pane.msft.png":::
   <span data-ttu-id="60a57-218">Der **Berechnete** Bereich wird konsistent als separater Bereich angezeigt, auch wenn die DevTools schmal sind.</span><span class="sxs-lookup"><span data-stu-id="60a57-218">The **Computed** pane consistently displays as a separate pane even when the DevTools are narrow.</span></span>
:::image-end:::  

<span data-ttu-id="60a57-219">[Chromium-#1073899][CR1073899]</span><span class="sxs-lookup"><span data-stu-id="60a57-219">Chromium issue [#1073899][CR1073899]</span></span>  

### <a name="bytecode-offsets-for-webassembly-files"></a><span data-ttu-id="60a57-220">Bytecodeoffsets für WebAssembly-Dateien</span><span class="sxs-lookup"><span data-stu-id="60a57-220">Bytecode offsets for WebAssembly files</span></span>  

<span data-ttu-id="60a57-221">DevTools verwendet jetzt Bytecodeoffsets zum Anzeigen von Zeilennummern der Wasm-Demontage.</span><span class="sxs-lookup"><span data-stu-id="60a57-221">DevTools now uses bytecode offsets for displaying line numbers of Wasm disassembly.</span></span>  
<span data-ttu-id="60a57-222">Die Zeilennummern machen deutlich, dass Sie binäre Daten sehen, und ist konsistenter mit der Referenz der Wasm-Laufzeit auf Speicherorte.</span><span class="sxs-lookup"><span data-stu-id="60a57-222">The line numbers make it clearer that you are looking at binary data, and is more consistent with how the Wasm runtime references locations.</span></span>  

<span data-ttu-id="60a57-223">[Chromium-#1071432][CR1071432]</span><span class="sxs-lookup"><span data-stu-id="60a57-223">Chromium issue [#1071432][CR1071432]</span></span>  

### <a name="line-wise-copy-and-cut-in-sources-panel"></a><span data-ttu-id="60a57-224">Zeilenweises Kopieren und Ausschneiden im Quellenbereich</span><span class="sxs-lookup"><span data-stu-id="60a57-224">Line-wise copy and cut in Sources Panel</span></span>  

<span data-ttu-id="60a57-225">Bei der Ausführung von Kopieren oder Ausschneiden ohne Auswahl im [Editor][DevtoolsSourcesEditCssJavascript]des Quellenbereichs kopiert devTools die aktuelle Inhaltszeile oder schneidet sie aus.</span><span class="sxs-lookup"><span data-stu-id="60a57-225">When performing copy or cut with no selection in the [Sources panel editor][DevtoolsSourcesEditCssJavascript], DevTools copies or cuts the current line of content.</span></span>  

:::image type="complex" source="../../media/2020/06/line-wise-cut.msft.png" alt-text="Kopieren Sie mit dem Cursor am Ende von Zeile 5 die gesamte Zeile aus pen.js devTools und einfügen in Visual Studio Code" lightbox="../../media/2020/06/line-wise-cut.msft.png":::
   <span data-ttu-id="60a57-227">Kopieren Sie mit dem Cursor am Ende von Zeile 5 die gesamte Zeile auspen.js\*\* devTools \*\* und einfügen in [Visual Studio Code][VisualStudioCode].</span><span class="sxs-lookup"><span data-stu-id="60a57-227">With the cursor at the end of Line 5, copying the whole line from **pen.js** in the DevTools and pasting in [Visual Studio Code][VisualStudioCode].</span></span>
:::image-end:::  

<span data-ttu-id="60a57-228">[Chromium-Problem #800028][CR800028]</span><span class="sxs-lookup"><span data-stu-id="60a57-228">Chromium issue [#800028][CR800028]</span></span>

### <a name="console-settings-updates"></a><span data-ttu-id="60a57-229">Aktualisierungen der Konsoleneinstellungen</span><span class="sxs-lookup"><span data-stu-id="60a57-229">Console Settings updates</span></span>  

#### <a name="ungroup-same-console-messages"></a><span data-ttu-id="60a57-230">Aufheben der Gruppierung derselben Konsolennachrichten</span><span class="sxs-lookup"><span data-stu-id="60a57-230">Ungroup same console messages</span></span>  

<span data-ttu-id="60a57-231">Der **Umschalter Gruppe ähnlich** in konsoleneinstellungen gilt jetzt für doppelte Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="60a57-231">The **Group similar** toggle in Console Settings now applies to duplicate messages.</span></span>  <span data-ttu-id="60a57-232">Zuvor wurde es nur auf ähnliche Nachrichten angewendet.</span><span class="sxs-lookup"><span data-stu-id="60a57-232">Previously it just applied to similar messages.</span></span>  

<span data-ttu-id="60a57-233">In früheren Beispielen hat DevTools die Gruppierung der Nachrichten nicht deaktiviert, obwohl die Gruppierung `hello` **ähnlich** deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="60a57-233">For example, previously, DevTools did not ungroup the `hello` messages even though **Group similar** is unchecked.</span></span>  <span data-ttu-id="60a57-234">Jetzt werden `hello` die Nachrichten nicht mehr in die Gruppe eingruppiert.</span><span class="sxs-lookup"><span data-stu-id="60a57-234">Now, the `hello` messages are ungrouped.</span></span>  

:::image type="complex" source="../../media/2020/06/ungroup-similar.msft.png" alt-text="Wenn "Gruppe ähnlich" deaktiviert ist, werden die Hello-Nachrichten nicht in die Gruppe eingruppiert." lightbox="../../media/2020/06/ungroup-similar.msft.png":::
   <span data-ttu-id="60a57-236">Wenn **"Gruppe ähnlich"** deaktiviert ist, werden `hello` die Nachrichten ungruppiert.</span><span class="sxs-lookup"><span data-stu-id="60a57-236">When **Group similar** is unchecked, the `hello` messages are ungrouped</span></span>
:::image-end:::  

<span data-ttu-id="60a57-237">Testen Sie dieses Feature mit einem [Beispiel, das doppelte Nachrichten an die Konsole sendet.][CodepenZoherghadyaliZyrjgdJ]</span><span class="sxs-lookup"><span data-stu-id="60a57-237">Give this feature a try with a [sample that sends duplicate messages to the Console][CodepenZoherghadyaliZyrjgdJ].</span></span>  

<span data-ttu-id="60a57-238">[Chromium-#1082963][CR1082963]</span><span class="sxs-lookup"><span data-stu-id="60a57-238">Chromium issue [#1082963][CR1082963]</span></span>  

### <a name="persisting-selected-context-only-settings"></a><span data-ttu-id="60a57-239">Einstellungen nur für den ausgewählten Kontext beibehalten</span><span class="sxs-lookup"><span data-stu-id="60a57-239">Persisting Selected context only settings</span></span>  

<span data-ttu-id="60a57-240">Die **Einstellungen für "Nur ausgewählter** Kontext" in den Konsoleneinstellungen werden nun beibehalten.</span><span class="sxs-lookup"><span data-stu-id="60a57-240">The **Selected context only** settings in Console Settings is now persisted.</span></span>  <span data-ttu-id="60a57-241">Zuvor wurden die Einstellungen jedes Mal zurückgesetzt, wenn Sie DevTools geschlossen und erneut geöffnet haben.</span><span class="sxs-lookup"><span data-stu-id="60a57-241">Previously the settings were reset every time you closed and reopened DevTools.</span></span>  <span data-ttu-id="60a57-242">Durch die Änderung wird das Einstellungsverhalten mit anderen Optionen für Konsoleneinstellungen konsistent.</span><span class="sxs-lookup"><span data-stu-id="60a57-242">The change makes the setting behavior consistent with other Console Settings options.</span></span>  

:::image type="complex" source="../../media/2020/06/selected-context.msft.png" alt-text="Einstellung nur für ausgewählten Kontext" lightbox="../../media/2020/06/selected-context.msft.png":::
   <span data-ttu-id="60a57-244">**Einstellung nur für ausgewählten** Kontext</span><span class="sxs-lookup"><span data-stu-id="60a57-244">**Selected context only** setting</span></span>  
:::image-end:::  

<span data-ttu-id="60a57-245">[Chromium-#1055875][CR1055875]</span><span class="sxs-lookup"><span data-stu-id="60a57-245">Chromium issue [#1055875][CR1055875]</span></span>  

### <a name="performance-panel-updates"></a><span data-ttu-id="60a57-246">Aktualisierungen des Leistungsbereichs</span><span class="sxs-lookup"><span data-stu-id="60a57-246">Performance panel updates</span></span>  

#### <a name="javascript-compilation-cache-information-in-performance-tool"></a><span data-ttu-id="60a57-247">JavaScript-Kompilierungscacheinformationen im **Leistungstool**</span><span class="sxs-lookup"><span data-stu-id="60a57-247">JavaScript compilation cache information in **Performance** tool</span></span>  

<span data-ttu-id="60a57-248">[JavaScript-Kompilierungscacheinformationen][V8DevCodeCaching] werden jetzt immer im **Zusammenfassungsbereich** des **Leistungstools** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="60a57-248">[JavaScript compilation cache information][V8DevCodeCaching] is now always displayed in the **Summary** panel of the **Performance** tool.</span></span>  <span data-ttu-id="60a57-249">Bisher hat DevTools nichts im Zusammenhang mit der Zwischenspeicherung von Code gezeigt, wenn keine Code zwischenspeichert wurde.</span><span class="sxs-lookup"><span data-stu-id="60a57-249">Previously, DevTools did not show anything related to code caching if code caching did not happen.</span></span>  

:::image type="complex" source="../../media/2020/06/js-compilation-cache.msft.png" alt-text="JavaScript-Kompilierungscacheinformationen" lightbox="../../media/2020/06/js-compilation-cache.msft.png":::
   <span data-ttu-id="60a57-251">JavaScript-Kompilierungscacheinformationen</span><span class="sxs-lookup"><span data-stu-id="60a57-251">JavaScript compilation cache information</span></span>  
:::image-end:::  

<span data-ttu-id="60a57-252">[Chromium-Problem #912581][CR912581]</span><span class="sxs-lookup"><span data-stu-id="60a57-252">Chromium issue [#912581][CR912581]</span></span>  

#### <a name="navigation-timing-alignment-in-the-performance-panel"></a><span data-ttu-id="60a57-253">Ausrichtung der Navigationszeit im Leistungsbereich</span><span class="sxs-lookup"><span data-stu-id="60a57-253">Navigation timing alignment in the Performance panel</span></span>  

<span data-ttu-id="60a57-254">Der **Leistungsbereich,** der zum Anzeigen von Zeiten in den Lineals verwendet wurde, basierend auf dem Beginn der Aufzeichnung.</span><span class="sxs-lookup"><span data-stu-id="60a57-254">The **Performance** panel used to show times in the rulers based on when the recording started.</span></span>  <span data-ttu-id="60a57-255">Das Timing hat sich nun für Aufzeichnungen geändert, in denen der Benutzer navigiert, wobei DevTools jetzt Linealzeiten relativ zur Navigation zeigt.</span><span class="sxs-lookup"><span data-stu-id="60a57-255">The timing has now changed for recordings where the user navigates, where DevTools now shows ruler times relative to the navigation instead.</span></span>  

:::image type="complex" source="../../media/2020/06/nav-timing.msft.png" alt-text="Ausrichten der Navigationszeit im Leistungstool" lightbox="../../media/2020/06/nav-timing.msft.png":::
   <span data-ttu-id="60a57-257">Ausrichten der Navigationszeit im **Leistungstool**</span><span class="sxs-lookup"><span data-stu-id="60a57-257">Align navigation timing in **Performance** tool</span></span>  
:::image-end:::  

<span data-ttu-id="60a57-258">Die Zeiten für , First Paint, First Contentful Paint und Largest Contentful Paint -Ereignisse werden so aktualisiert, dass sie relativ zum Start der Navigation sind, was bedeutet, dass die Zeitplanung mit den von gemeldeten `DOMContentLoaded` Timings `PerformanceObserver` entspricht.</span><span class="sxs-lookup"><span data-stu-id="60a57-258">The times for `DOMContentLoaded`, First Paint, First Contentful Paint, and Largest Contentful Paint events are updated to be relative to the start of the navigation, which means the timing matches the timings reported by `PerformanceObserver`.</span></span>  

<span data-ttu-id="60a57-259">[Chromium-#974550][CR974550]</span><span class="sxs-lookup"><span data-stu-id="60a57-259">Chromium issue [#974550][CR974550]</span></span>  

### <a name="new-icons-for-breakpoints-conditional-breakpoints-and-logpoints"></a><span data-ttu-id="60a57-260">Neue Symbole für Haltepunkte, bedingte Haltepunkte und Protokollpunkte</span><span class="sxs-lookup"><span data-stu-id="60a57-260">New icons for breakpoints, conditional breakpoints, and logpoints</span></span>  

<span data-ttu-id="60a57-261">Der **Bereich** Quellen verfügt über neue Designs für Haltepunkte, bedingte Haltepunkte und Protokollpunkte.</span><span class="sxs-lookup"><span data-stu-id="60a57-261">The **Sources** panel has new designs for breakpoints, conditional breakpoints, and logpoints.</span></span>  <span data-ttu-id="60a57-262">Haltepunkte werden durch einen roten Kreis dargestellt, genau wie Visual Studio [Code][VisualStudioCode] und [Visual Studio][VisualStudio].</span><span class="sxs-lookup"><span data-stu-id="60a57-262">Breakpoints are represented by a red circle, just like [Visual Studio Code][VisualStudioCode] and [Visual Studio][VisualStudio].</span></span>  <span data-ttu-id="60a57-263">Symbole werden hinzugefügt, um bedingte Haltepunkte und Protokollpunkte zu unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="60a57-263">Icons are added to differentiate conditional breakpoints and logpoints.</span></span>  

:::image type="complex" source="../../media/2020/06/breakpoints.msft.png" alt-text="Breakpoints" lightbox="../../media/2020/06/breakpoints.msft.png":::
   <span data-ttu-id="60a57-265">Breakpoints</span><span class="sxs-lookup"><span data-stu-id="60a57-265">Breakpoints</span></span>  
:::image-end:::  

<span data-ttu-id="60a57-266">[Chromium-#1041830][CR1041830]</span><span class="sxs-lookup"><span data-stu-id="60a57-266">Chromium issue [#1041830][CR1041830]</span></span>  

## <a name="download-the-microsoft-edge-preview-channels"></a><span data-ttu-id="60a57-267">Herunterladen der Microsoft Edge-Vorschaukanäle</span><span class="sxs-lookup"><span data-stu-id="60a57-267">Download the Microsoft Edge preview channels</span></span>  

<span data-ttu-id="60a57-268">Wenn Sie unter Windows oder macOS sind, sollten Sie die [Microsoft Edge-Vorschaukanäle][MicrosoftEdgePreviewChannels] als Standardentwicklungsbrowser verwenden.</span><span class="sxs-lookup"><span data-stu-id="60a57-268">If you are on Windows or macOS, consider using the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] as your default development browser.</span></span>  <span data-ttu-id="60a57-269">Über die Vorschaukanäle erhalten Sie Zugriff auf die neuesten DevTools-Features.</span><span class="sxs-lookup"><span data-stu-id="60a57-269">The preview channels give you access to the latest DevTools features.</span></span>  

## <a name="getting-in-touch-with-microsoft-edge-devtools-team"></a><span data-ttu-id="60a57-270">Mit dem Microsoft Edge DevTools-Team Kontakt aufnehmen</span><span class="sxs-lookup"><span data-stu-id="60a57-270">Getting in touch with Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]  

<!-- links -->  

[DevtoolsMain]: /microsoft-edge/devtools-guide-chromium "Microsoft Edge (Chromium) Developer Tools | Microsoft Docs"  
[DevtoolsCommandMenu]: /microsoft-edge/devtools-guide-chromium/command-menu "Führen Sie Befehle mit dem Microsoft Edge DevTools-Befehlsmenü | Microsoft Docs"
[DevtoolsCustomizeIndexDrawer]: /microsoft-edge/devtools-guide-chromium/customize/index#drawer "Drawer – Anpassen von Microsoft Edge DevTools | Microsoft Docs"
[DevtoolsExperimentalFeaturesTurnOn]: /microsoft-edge/devtools-guide-chromium/experimental-features#turn-on-experimental-features "Aktivieren experimenteller Features – Experimentelle Features | Microsoft Docs"  
[DevtoolsIssues]: /microsoft-edge/devtools-guide-chromium/issues "Erkennen und Beheben von Problemen mit dem Microsoft Edge DevTools-Tool „Probleme“ | Microsoft Docs"
[DevtoolsSourcesEditCssJavascript]: /microsoft-edge/devtools-guide-chromium/sources#edit-css-and-javascript "Bearbeiten von CSS und JavaScript – Übersicht über den Quellenbereich | Microsoft Docs"  
[DevtoolsNetworkIndexLogActivity]: /microsoft-edge/devtools-guide-chromium/network/index#log-network-activity "Protokollnetzwerkaktivität – Überprüfen der Netzwerkaktivität in Microsoft Edge DevTools | Microsoft Docs"

[CodepenZoherghadyaliAbdgrpz]: https://codepen.io/zoherghadyali/full/abdGrPZ "Formatbearbeitung für CSS-in-JS-Frameworks | CodePen"
[CodepenZoherghadyaliZyrjgdJ]: https://codepen.io/zoherghadyali/full/zYrjgdJ "Senden doppelter Nachrichten an konsolen | CodePen"
[CodepenRachelweilYzwBzKM]: https://codepen.io/hxlnt/full/YzwBzKM "CSS-Rasterplanerbeispiel | CodePen"

[CRIssuesList]: https://bugs.chromium.org/p/chromium/issues/list "Chromium-Fehler"  

[CR772558]: https://crbug.com/772558 "DevTools: Aktualisieren auf die neueste Version von "| Chromium-Fehler"  
[CR800028]: https://crbug.com/800028 "Doppelte Zeilenverknüpfung im Entwicklertools-Editor funktioniert nach dem Chrome-Update nicht | Chromium-Fehler"  
[CR912581]: https://crbug.com/912581 "Verfügbar machen, welche Skripts von V8 in DevTools/about:tracing zwischengespeichert | Chromium-Fehler"  
[CR946975]: https://crbug.com/946975 "DevTools Styles Sidebar funktioniert nicht mit erstellten Stylesheets | Chromium-Fehler"  
[CR955497]: https://crbug.com/955497 "Kontextmenü "App-Symbol" für PWAs | Chromium-Fehler"  
[CR974550]: https://crbug.com/974550 "Metrikkonflikt zwischen Perf-Bereich und performanceObserver-| Chromium-Fehler"  
[CR1041830]: https://crbug.com/1041830 "Verbessern von Farben für Haltepunkte | Chromium-Fehler"  
[CR1055875]: https://crbug.com/1055875 "Der Wert der Konsoleneinstellung Nur Ausgewählter Kontext bleibt nach dem Schließen und erneuten Öffnen von Entwicklertools nicht | Chromium-Fehler"  
[CR1066579]: https://crbug.com/1066579 "DevTools: Show ServiceWorkers Fetch Timeline per request in Network panel | Chromium-Fehler"  
[CR1071432]: https://crbug.com/1071432 "Wasm Basic Developer Experience | Chromium-Fehler"  
[CR1073899]: https://crbug.com/1073899 "Registerkarte "Berechnete Formatvorlage" wird im reaktionsschnellen Modus | Chromium-Fehler"  
[CR1073903]: https://crbug.com/1073903 "DevTools: Syntax highlighting doesn't work with private fields | Chromium-Fehler"  
[CR1082963]: https://crbug.com/1082963 "Das Gruppenverhalten ähnlicher Nachrichten der Konsole kann nicht deaktiviert | Chromium-Fehler"  
[CR1083214]: https://crbug.com/1083214 "acorn unterstützt keine optionale Verkettung | Chromium-Fehler"  
[CR1083797]: https://crbug.com/1083797 "Ziemliches Drucken unterbrochen für nullish koescing | Chromium-Fehler"  
[CR1096008]: https://crbug.com/1096008 "Entfernen von FMP-| Chromium-Fehler"  
[CR1047356]: https://crbug.com/1047356 "CSS Grid/Flexbox/Table tooling | Chromium-Fehler"  
[CR1093687]: https://crbug.com/1093687 "Erstellen eines Tools zum Erstellen und Wiedergeben synthetischer Netzwerkanforderungen | Chromium-Fehler"  
[CR1070378]: https://crbug.com/1070378 "Integrieren von Webhint in DevTools | Chromium-Fehler"  
[CR1069404]: https://crbug.com/1069404 "[Dev Tools] Widget-Popups sind zu eng | Chromium-Fehler"  
[CR897944]: https://crbug.com/897944 "Draggable devtool panels | Chromium-Fehler"

[GithubGoogleChromeLighthouse600]: https://github.com/GoogleChrome/lighthouse/releases/tag/v6.0.0 "v6.0.0 – GoogleChrome/| GitHub"  

[GitHubMicrosoftDocsEdgeDeveloperNewIssue]: https://github.com/MicrosoftDocs/edge-developer/issues/new?title=[DevTools%20Docs%20Feedback] "Neues Problem – MicrosoftDocs/edge-developer"  

[MdnShadowDom]: https://developer.mozilla.org/docs/Web/Web_Components/Using_shadow_DOM "Verwenden von Schatten-DOM-| MDN"

[MicrosoftEdgePreviewChannels]: https://www.microsoftedgeinsider.com/download/ "Microsoft Edge Preview Channels"  

[VisualStudio]: https://visualstudio.microsoft.com/ "Visual Studio"
[VisualStudioCode]: https://code.visualstudio.com/ "Visual Studio Code"  

[CsswgDraftsCssom]: https://drafts.csswg.org/cssom "CSS-Objektmodell (CSSOM) | W3C CSS Working Group Editor Drafts"  

[PostTweetEdgeDevTools]: https://twitter.com/intent/tweet?text=@EdgeDevTools "@EdgeDevTools | Veröffentlichen eines Tweets"  
[EdgeDevToolsTwitterAccount]: https://twitter.com/EdgeDevTools "@EdgeDevTools, Twitter-Konto"  

[V8DevClassFieldsPrivate]: https://v8.dev/features/class-fields#private-class-fields "Private Klassenfelder – Öffentliche und private Klassenfelder | V8. Dev"  
[V8DevCodeCaching]: https://v8.dev/blog/code-caching-for-devs "Code zwischenspeichern für JavaScript-Entwickler | V8. Dev"  
[V8DevNullishCoalescing]: https://v8.dev/features/nullish-coalescing "Nullish-Koescing-| V8. Dev"  
[V8DevOptionalChaining]: https://v8.dev/features/optional-chaining "Optionale Verkettungs| V8. Dev"  

[WebhintMain]: https://webhint.io "webhint"  

[WicgConstructStylesheet]: https://wicg.github.io/construct-stylesheets/ "Constructable Stylesheet Objects | Web Incubator CG"

<!--[WebDevLighthouseWhatsNew60]: https://web.dev/lighthouse-whats-new-6.0 "What's New in Lighthouse 6.0 | Web.Dev"  -->  
<!--[WebDevVitalsCoreWeb]: https://web.dev/vitals#core-web-vitals "Core Web Vitals - Web Vitals | Web.Dev"  -->  
<!--[WebdevAppShortcuts]: https://alphabet-dev/app-shortcuts "Get things done quickly with app shortcuts | alphabet-dev"  -->  
<!--[WebdevCls]: https://alphabet-dev/cls "Cumulative Layout Shift (CLS) | alphabet-dev"  -->  
<!--[WebdevControlFocus]: https://alphabet-dev/control-focus-with-tabindex "Control focus with tabindex | alphabet-dev"  -->  
<!--[WebdevMeasureSpeedLabField]: https://alphabet-dev/how-to-measure-speed#lab-data-vs-field-data "Lab data vs Field data - How to measure speed? | alphabet-dev"  -->  
<!--[WebdevLabelsText]: https://alphabet-dev/labels-and-text-alternatives "Labels and text alternatives | alphabet-dev"  -->  
<!--[WebdevTbt]: https://alphabet-dev/tbt "Total Blocking Time (TBT) | alphabet-dev"  -->  
<!--[WebFundamentalComponentsShadowdom]: /web/fundamentals/web-components/shadowdom  -->  
<!--[WebDevLcp]: https://web.dev/lcp "Largest Contentful Paint (LCP) | Web.Dev"  -->  
<!--[WebDevFirstMeaningfulPaint]: https://web.dev/first-meaningful-paint "First Meaningful Paint | Web.Dev"  -->  
<!--[WhatsNew201902ConstructableStylesheets]: ../../2019/02/constructable-stylesheets.md "Constructable Stylesheets: seamless reusable styles | Microsoft Docs"  -->  

[TheWebWeWant]: https://webwewant.fyi/ "The Web We Want"  

> [!NOTE]
> <span data-ttu-id="60a57-319">Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="60a57-319">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="60a57-320">Die ursprüngliche Seite findet sich [hier](https://developers.google.com/web/updates/2020/06/devtools/index) und wurde von [Jecelyn Yeen][JecelynYeen] \(Developer Advocate, Chrome DevTools\) erstellt.</span><span class="sxs-lookup"><span data-stu-id="60a57-320">The original page is found [here](https://developers.google.com/web/updates/2020/06/devtools/index) and is authored by [Jecelyn Yeen][JecelynYeen] \(Developer advocate, Chrome DevTools\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="60a57-322">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="60a57-322">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[JecelynYeen]: https://developers.google.com/web/resources/contributors/jecelynyeen  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
