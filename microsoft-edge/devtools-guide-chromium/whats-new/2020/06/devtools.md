---
description: Debuggen von CSS-Raster Features, bearbeiten und Wiedergeben von Anforderungen mit der Netzwerk Konsole und vieles mehr.
title: Neuerungen in devtools (Microsoft Edge 85)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/11/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: 01651bdf0f36f7c175f843655c275695a680b6c1
ms.sourcegitcommit: b337717957529239434b4e8e1e167aebf0543518
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/15/2020
ms.locfileid: "11015461"
---
# <span data-ttu-id="273e0-104">Neuerungen in devtools (Microsoft Edge 85)</span><span class="sxs-lookup"><span data-stu-id="273e0-104">What's New In DevTools (Microsoft Edge 85)</span></span>  

## <span data-ttu-id="273e0-105">Ankündigungen des Microsoft Edge devtools-Teams</span><span class="sxs-lookup"><span data-stu-id="273e0-105">Announcements from the Microsoft Edge DevTools team</span></span>  

<span data-ttu-id="273e0-106">In den folgenden Abschnitten finden Sie eine Liste der Ankündigungen, die Sie möglicherweise im Microsoft Edge devtools-Team verpasst haben.</span><span class="sxs-lookup"><span data-stu-id="273e0-106">The following sections are a list of announcements you may have missed from the Microsoft Edge DevTools team.</span></span>  <span data-ttu-id="273e0-107">Schauen Sie sich die Ankündigungen an, um neue Features im devtools, Visual Studio-Code Erweiterungen und vieles mehr zu testen.</span><span class="sxs-lookup"><span data-stu-id="273e0-107">See the announcements to try new features in the DevTools, Visual Studio Code extensions, and more.</span></span>  <span data-ttu-id="273e0-108">Wenn Sie über die neuesten und besten Funktionen Ihrer Entwicklertools auf dem Laufenden bleiben möchten, laden Sie die [Microsoft Edge Preview-Kanäle][MicrosoftEdgePreviewChannels] herunter, und [folgen Sie dem Microsoft Edge devtools-Team auf Twitter][EdgeDevToolsTwitterAccount].</span><span class="sxs-lookup"><span data-stu-id="273e0-108">To stay up to date on all the latest and greatest features in your developer tools, download the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] and [follow the Microsoft Edge DevTools team on Twitter][EdgeDevToolsTwitterAccount].</span></span>  

### <span data-ttu-id="273e0-109">Debuggen von CSS-Raster Features</span><span class="sxs-lookup"><span data-stu-id="273e0-109">CSS grid debugging features</span></span>  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Experimentelle Funktion":::
   <span data-ttu-id="273e0-111">Experimentelle Funktion</span><span class="sxs-lookup"><span data-stu-id="273e0-111">Experimental feature</span></span>  
:::image-end:::  

<span data-ttu-id="273e0-112">Das Microsoft Edge devtools-Team kooperiert mit der Chrome-devtools-Team-und Chrom-Community, um neue CSS-Raster Debugging-Features zu devtools hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="273e0-112">The Microsoft Edge DevTools team is collaborating with the Chrome DevTools team and Chromium community to add new CSS grid debugging features to DevTools.</span></span>  <span data-ttu-id="273e0-113">Sie können nun Rasterlinien Nummern, Rasterabstände und erweiterte Rasterlinien als eine auf Seiten Überlagerungen anzeigen.</span><span class="sxs-lookup"><span data-stu-id="273e0-113">You are now able to display grid line numbers, grid gaps, and extended grid lines as an on-page overlay.</span></span>  <span data-ttu-id="273e0-114">Darüber hinaus werden in Kürze weitere Verbesserungen an den Grid-Tools durchkommen.</span><span class="sxs-lookup"><span data-stu-id="273e0-114">Plus, more improvements to the grid tools are coming soon.</span></span>  

:::image type="complex" source="../../media/2020/06/experiments-grid.msft.png" alt-text="Experimentelle Funktion" lightbox="../../media/2020/06/experiments-grid.msft.png":::
   <span data-ttu-id="273e0-116">Debuggen von CSS-Raster Features</span><span class="sxs-lookup"><span data-stu-id="273e0-116">CSS grid debugging features</span></span>
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="273e0-117">Wenn Sie das Experiment aktivieren möchten, lesen Sie aktivieren [von experimentellen Features][DevtoolsExperimentalFeaturesTurnOn] , und aktivieren Sie das Kontrollkästchen neben " **neue CSS-Raster Debuggen"-Features aktivieren**.</span><span class="sxs-lookup"><span data-stu-id="273e0-117">To enable the experiment, see [Turn on experimental features][DevtoolsExperimentalFeaturesTurnOn] and select the checkbox next to **Enable new CSS Grid debugging features**.</span></span>  
> 
> <span data-ttu-id="273e0-118">Wenn Sie das Experiment mit einem Beispiel testen möchten, lesen Sie [Beispiel für CSS-Raster Planner][CodepenRachelweilYzwBzKM].</span><span class="sxs-lookup"><span data-stu-id="273e0-118">To try out the experiment with a sample, see [CSS Grid planner example][CodepenRachelweilYzwBzKM].</span></span>  

<span data-ttu-id="273e0-119">Chrom Problem [#1047356][CR1047356]</span><span class="sxs-lookup"><span data-stu-id="273e0-119">Chromium issue [#1047356][CR1047356]</span></span>  

### <span data-ttu-id="273e0-120">Bearbeiten und Wiedergeben von Anforderungen mit der Netzwerk Konsole</span><span class="sxs-lookup"><span data-stu-id="273e0-120">Edit and Replay requests with the Network Console</span></span>  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Experimentelle Funktion":::
   <span data-ttu-id="273e0-122">Experimentelle Funktion</span><span class="sxs-lookup"><span data-stu-id="273e0-122">Experimental feature</span></span>  
:::image-end:::  

<span data-ttu-id="273e0-123">Sie können jetzt die **Bearbeitung und Wiedergabe** von Anforderungen im [Netzwerkprotokoll][DevtoolsNetworkIndexLogActivity] über die **Netzwerk Konsole**verwenden.</span><span class="sxs-lookup"><span data-stu-id="273e0-123">You are now able to use **Edit and Replay** on requests in the [Network Log][DevtoolsNetworkIndexLogActivity] using the **Network Console**.</span></span>  

:::image type="complex" source="../../media/2020/06/experiments-network-console-edit-and-replay.msft.png" alt-text="Experimentelle Funktion" lightbox="../../media/2020/06/experiments-network-console-edit-and-replay.msft.png":::
   <span data-ttu-id="273e0-125">Bearbeiten und Wiedergeben einer Anforderung im [NetworkLog][DevtoolsNetworkIndexLogActivity] mit der **Netzwerk Konsole**</span><span class="sxs-lookup"><span data-stu-id="273e0-125">Edit and Replay a request in the [NetworkLog][DevtoolsNetworkIndexLogActivity] with the **Network Console**</span></span>  
:::image-end:::  

<span data-ttu-id="273e0-126">Ein neues Panel, die **Netzwerk Konsole** wird im [devtools-Einzug][DevtoolsCustomizeIndexDrawer] geöffnet und füllt automatisch Informationen für die HTTP-Anforderung auf.</span><span class="sxs-lookup"><span data-stu-id="273e0-126">A new panel, the **Network Console** opens in the [DevTools Drawer][DevtoolsCustomizeIndexDrawer] and automatically populates with information for the HTTP request.</span></span>  <span data-ttu-id="273e0-127">Um die vom Server zurückgegebene Antwort anzuzeigen, bearbeiten Sie die Anforderung \ (falls erforderlich \), und wählen Sie **senden**aus.</span><span class="sxs-lookup"><span data-stu-id="273e0-127">To see the response returned from the server, edit the request \(if needed\) and select **Send**.</span></span>  

<span data-ttu-id="273e0-128">Sie können auch die **Netzwerk Konsole** verwenden, um HTTP-Anforderungen direkt aus dem devtools zu erstellen und zu senden.</span><span class="sxs-lookup"><span data-stu-id="273e0-128">You may also use the **Network Console** to create and send HTTP requests directly from the DevTools.</span></span>  

:::image type="complex" source="../../media/2020/06/experiments-network-console.msft.png" alt-text="Experimentelle Funktion" lightbox="../../media/2020/06/experiments-network-console.msft.png":::
   <span data-ttu-id="273e0-130">Das **Netzwerkkonsolen** Panel</span><span class="sxs-lookup"><span data-stu-id="273e0-130">The **Network Console** panel</span></span>  
:::image-end:::  

> [!TIP]
> <span data-ttu-id="273e0-131">Informationen zum Anzeigen der **Netzwerk Konsole** im Hauptbereich \ (oben \) anstelle der [devtools-Schublade][DevtoolsCustomizeIndexDrawer]finden Sie unter [Verschieben von Tools zwischen Bereichen](#move-tools-between-panels).</span><span class="sxs-lookup"><span data-stu-id="273e0-131">To see **Network Console** in the main \(top\) panel instead of the [DevTools Drawer][DevtoolsCustomizeIndexDrawer], see [moving tools between panels](#move-tools-between-panels).</span></span>  

> [!NOTE]
> <span data-ttu-id="273e0-132">Wenn Sie das Experiment aktivieren möchten, lesen Sie aktivieren [von experimentellen Features][DevtoolsExperimentalFeaturesTurnOn] , und aktivieren Sie das Kontrollkästchen neben **Netzwerk Konsole aktivieren**.</span><span class="sxs-lookup"><span data-stu-id="273e0-132">To enable the experiment, see [Turn on experimental features][DevtoolsExperimentalFeaturesTurnOn] and select the checkbox next to **Enable Network Console**.</span></span>  
> 
> <span data-ttu-id="273e0-133">Öffnen Sie das [Netzwerkprotokoll][DevtoolsNetworkIndexLogActivity], öffnen Sie das Kontextmenü \ (Klicken Sie mit der rechten Maustaste auf \), und wählen Sie **Bearbeiten und wiedergeben**aus.</span><span class="sxs-lookup"><span data-stu-id="273e0-133">Open the [Network Log][DevtoolsNetworkIndexLogActivity], open the contextual menu \(right-click\), and select **Edit and Replay**.</span></span>  

<span data-ttu-id="273e0-134">Chrom Problem [#1093687][CR1093687]</span><span class="sxs-lookup"><span data-stu-id="273e0-134">Chromium issue [#1093687][CR1093687]</span></span>  

### <span data-ttu-id="273e0-135">Service Worker-respondWith-Ereignisse auf der Registerkarte "Anzeigedauer"</span><span class="sxs-lookup"><span data-stu-id="273e0-135">Service worker respondWith events in the Timing tab</span></span>  

<span data-ttu-id="273e0-136">Die Registerkarte " **Anzeige** Dauer" des **Netzwerk** Panels enthält jetzt `respondWith` Service Worker-Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="273e0-136">The **Timing** tab of the **Network** panel now includes `respondWith` service worker events.</span></span>  <span data-ttu-id="273e0-137">Das `respondWith` Dienst Arbeitskraft-Ereignis zeigt die Dauer ab dem Zeitpunkt an, zu dem der Service Worker- `fetch` Ereignishandler mit dem Zeitpunkt beginnt, zu dem das `respondWith` Versprechen des `fetch` Handlers abgerechnet wird.</span><span class="sxs-lookup"><span data-stu-id="273e0-137">The `respondWith` service worker event shows the duration from the time immediately before the service worker `fetch` event handler starts running to the time when the `respondWith` promise of the `fetch` handler is settled.</span></span>  

:::image type="complex" source="../../media/2020/06/timing-tab.msft.png" alt-text="Experimentelle Funktion" lightbox="../../media/2020/06/timing-tab.msft.png":::
   <span data-ttu-id="273e0-139">Das `respondWith` Service Worker-Ereignis auf der Registerkarte " **Anzeige** Dauer" des **Netzwerk** Panels</span><span class="sxs-lookup"><span data-stu-id="273e0-139">The `respondWith` service worker event in the **Timing** tab of the **Network** panel</span></span>  
:::image-end:::  

<span data-ttu-id="273e0-140">Erweitern der **empfangenen Antwort** , um weitere Informationen aus der `fetch` Antwort wie `CacheStorageCacheName` , `serviceWorkerResponseSource` und anzuzeigen `ResponseTime` .</span><span class="sxs-lookup"><span data-stu-id="273e0-140">Expand **Response received** to see additional information from the `fetch` response like `CacheStorageCacheName`, `serviceWorkerResponseSource`, and `ResponseTime`.</span></span>  

:::image type="complex" source="../../media/2020/06/timing-tab2.msft.png" alt-text="Experimentelle Funktion" lightbox="../../media/2020/06/timing-tab2.msft.png":::
   <span data-ttu-id="273e0-142">Erweitern der **empfangenen Antwort** , um weitere Informationen aus der `fetch` Antwort anzuzeigen</span><span class="sxs-lookup"><span data-stu-id="273e0-142">Expand **Response received** to see additional information from the `fetch` response</span></span>  
:::image-end:::  

<span data-ttu-id="273e0-143">Chrom Problem [#1066579][CR1066579]</span><span class="sxs-lookup"><span data-stu-id="273e0-143">Chromium issue [#1066579][CR1066579]</span></span>  

### <span data-ttu-id="273e0-144">webhint-Feedback im Bereich "Probleme"</span><span class="sxs-lookup"><span data-stu-id="273e0-144">webhint feedback in the Issues panel</span></span>  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Experimentelle Funktion":::
   <span data-ttu-id="273e0-146">Experimentelle Funktion</span><span class="sxs-lookup"><span data-stu-id="273e0-146">Experimental feature</span></span>  
:::image-end:::  

<span data-ttu-id="273e0-147">[webhint][WebhintMain] ist ein Open-Source-Tool, das in Echtzeit Feedback zur Barrierefreiheit, browserübergreifenden Kompatibilität, Sicherheit, Leistung, PWAs und anderen gängigen Webentwicklungs Problemen von Websites bietet.</span><span class="sxs-lookup"><span data-stu-id="273e0-147">[webhint][WebhintMain] is an open-source tool that provides real-time feedback on the accessibility, cross-browser compatibility, security, performance, PWAs, and other common web development issues of websites.</span></span>  <span data-ttu-id="273e0-148">Sie können jetzt webhint-Feedback im [Problem][DevtoolsIssues] Bereich anzeigen.</span><span class="sxs-lookup"><span data-stu-id="273e0-148">You are now able to see webhint feedback in the [Issues][DevtoolsIssues] panel.</span></span>  

:::image type="complex" source="../../media/2020/06/experiments-webhint.msft.png" alt-text="Experimentelle Funktion" lightbox="../../media/2020/06/experiments-webhint.msft.png":::
   <span data-ttu-id="273e0-150">webhint-Feedback im Bereich "Probleme"</span><span class="sxs-lookup"><span data-stu-id="273e0-150">webhint feedback in the Issues panel</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="273e0-151">Wenn Sie das Experiment aktivieren möchten, lesen Sie aktivieren [von experimentellen Features][DevtoolsExperimentalFeaturesTurnOn] , und aktivieren Sie das Kontrollkästchen neben **webhint aktivieren**.</span><span class="sxs-lookup"><span data-stu-id="273e0-151">To enable the experiment, see [Turn on experimental features][DevtoolsExperimentalFeaturesTurnOn] and select the checkbox next to **Enable webhint**.</span></span>  
> 
> <span data-ttu-id="273e0-152">Öffnen Sie den Bereich [Probleme][DevtoolsIssues] , um Feedback von webhint anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="273e0-152">Open the [Issues][DevtoolsIssues] panel to see feedback from webhint.</span></span>  

<span data-ttu-id="273e0-153">Chrom Problem [#1070378][CR1070378]</span><span class="sxs-lookup"><span data-stu-id="273e0-153">Chromium issue [#1070378][CR1070378]</span></span>  

### <span data-ttu-id="273e0-154">Verschieben von Tools zwischen Bereichen</span><span class="sxs-lookup"><span data-stu-id="273e0-154">Move tools between panels</span></span>  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Experimentelle Funktion":::
   <span data-ttu-id="273e0-156">Experimentelle Funktion</span><span class="sxs-lookup"><span data-stu-id="273e0-156">Experimental feature</span></span>  
:::image-end:::  

<span data-ttu-id="273e0-157">In der Regel können Tools, wie **Elemente** und **Netzwerke** , nur im Hauptbereich \ (oben \) von devtools geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="273e0-157">Normally, tools such as **Elements** and **Network** may only be opened in the main \(top\) panel of DevTools.</span></span>  <span data-ttu-id="273e0-158">Auf ähnliche Weise können Tools wie **3D-Ansicht** und **Probleme** nur im Bereich "drawer \ (unten \)" von devtools geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="273e0-158">Similarly, tools such as **3D View** and **Issues** may only be opened in the drawer \(bottom\) panel of DevTools.</span></span>  <span data-ttu-id="273e0-159">Sie können jetzt Ihr devtools-Layout anpassen, indem Sie die Tools zwischen dem oberen und unteren Bereich verschieben.</span><span class="sxs-lookup"><span data-stu-id="273e0-159">You are now able to customize your DevTools layout by moving tools between the top and bottom panels.</span></span>  

:::image type="complex" source="../../media/2020/06/experiments-move-panels.msft.png" alt-text="Experimentelle Funktion" lightbox="../../media/2020/06/experiments-move-panels.msft.png":::
   <span data-ttu-id="273e0-161">Verschieben von Tabstopps zwischen Bereichen</span><span class="sxs-lookup"><span data-stu-id="273e0-161">Moving tabs between panels</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="273e0-162">Wenn Sie das Experiment aktivieren möchten, lesen Sie aktivieren [von experimentellen Features][DevtoolsExperimentalFeaturesTurnOn] , und aktivieren Sie das Kontrollkästchen neben **Unterstützung aktivieren, um Tabstopps zwischen Bereichen zu verschieben**.</span><span class="sxs-lookup"><span data-stu-id="273e0-162">To enable the experiment, see [Turn on experimental features][DevtoolsExperimentalFeaturesTurnOn] and select the checkbox next to **Enable support to move tabs between panels**.</span></span>  

<span data-ttu-id="273e0-163">Chrom Problem [#897944][CR897944]</span><span class="sxs-lookup"><span data-stu-id="273e0-163">Chromium issue [#897944][CR897944]</span></span>  

### <span data-ttu-id="273e0-164">Verbesserte QuickInfo des Initiators im Netzwerk Panel</span><span class="sxs-lookup"><span data-stu-id="273e0-164">Improved Initiator tooltip in the Network panel</span></span>  

<span data-ttu-id="273e0-165">In Microsoft Edge 83 und 84 werden QuickInfos für die Initiator-Spalte, die die Ursache der Ressourcenanforderung zeigt, im [Netzwerkprotokoll][DevtoolsNetworkIndexLogActivity] mit einer horizontalen Bildlaufleiste angezeigt.</span><span class="sxs-lookup"><span data-stu-id="273e0-165">In Microsoft Edge 83 and 84, tooltips for the Initiator column, which shows the cause of the resource request, in the [Network Log][DevtoolsNetworkIndexLogActivity] displayed with a horizontal scrollbar.</span></span>  <span data-ttu-id="273e0-166">Sie konnten nur den Aufruf Stapel sehen, der die Anforderung initiiert hat, indem Sie in der QuickInfo horizontal scrollen.</span><span class="sxs-lookup"><span data-stu-id="273e0-166">You were only able to see the call stack that initiated the request by scrolling horizontally in the tooltip.</span></span>  

:::image type="complex" source="../../media/2020/06/initiator-tooltip-84.msft.png" alt-text="Experimentelle Funktion" lightbox="../../media/2020/06/initiator-tooltip-84.msft.png":::
   <span data-ttu-id="273e0-168">Die QuickInfo des Initiators in Microsoft Edge 84</span><span class="sxs-lookup"><span data-stu-id="273e0-168">The Initiator tooltip in Microsoft Edge 84</span></span>  
:::image-end:::  

<span data-ttu-id="273e0-169">Ab Microsoft Edge 85 können Sie jetzt den Initiator-Aufruf Stapel in der QuickInfo anzeigen, ohne horizontal scrollen zu müssen.</span><span class="sxs-lookup"><span data-stu-id="273e0-169">Starting with Microsoft Edge 85, you are now able to see the Initiator call stack in the tooltip without scrolling horizontally.</span></span>  

:::image type="complex" source="../../media/2020/06/initiator-tooltip-85.msft.png" alt-text="Experimentelle Funktion" lightbox="../../media/2020/06/initiator-tooltip-85.msft.png":::
   <span data-ttu-id="273e0-171">Die QuickInfo des Initiators in Microsoft Edge 85</span><span class="sxs-lookup"><span data-stu-id="273e0-171">The Initiator tooltip in Microsoft Edge 85</span></span>
:::image-end:::  

<span data-ttu-id="273e0-172">Chrom Problem [#1069404][CR1069404]</span><span class="sxs-lookup"><span data-stu-id="273e0-172">Chromium issue [#1069404][CR1069404]</span></span>  

## <span data-ttu-id="273e0-173">Ankündigungen aus dem Chromium-Projekt</span><span class="sxs-lookup"><span data-stu-id="273e0-173">Announcements from the Chromium project</span></span>  

<span data-ttu-id="273e0-174">In den folgenden Abschnitten werden weitere in Microsoft Edge 85 verfügbare Features angekündigt, die zum Open-Source-Projekt Chromium beigetragen haben.</span><span class="sxs-lookup"><span data-stu-id="273e0-174">The following sections announce additional features available in Microsoft Edge 85 that were contributed to the open source Chromium project.</span></span>  

### <span data-ttu-id="273e0-175">Format Bearbeitung für CSS-in-JS-Frameworks</span><span class="sxs-lookup"><span data-stu-id="273e0-175">Style editing for CSS-in-JS frameworks</span></span>  

<span data-ttu-id="273e0-176">Der Bereich " **Formatvorlagen** " bietet nun eine bessere Unterstützung für die Bearbeitung von Formatvorlagen, die mit den [CSSOM-APIs (CSS Object Model)][CsswgDraftsCssom] erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="273e0-176">The **Styles** pane now has better support for editing styles that were created with the [CSS Object Model (CSSOM)][CsswgDraftsCssom] APIs.</span></span>  <span data-ttu-id="273e0-177">Viele CSS-in-JS-Frameworks und-Bibliotheken verwenden die CSSOM-APIs unter der Haube zum Erstellen von Formatvorlagen.</span><span class="sxs-lookup"><span data-stu-id="273e0-177">Many CSS-in-JS frameworks and libraries use the CSSOM APIs under the hood to construct styles.</span></span>  

<span data-ttu-id="273e0-178">Sie können jetzt in JavaScript hinzugefügte Formatvorlagen mithilfe von Konstruktions fähigen [Stylesheets][WicgConstructStylesheet]bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="273e0-178">You are now able to edit styles added in JavaScript using [Constructable Stylesheets][WicgConstructStylesheet].</span></span>  <span data-ttu-id="273e0-179">Konstruktable-Stylesheets sind eine neue Möglichkeit zum Erstellen und Verteilen von wiederverwendbaren Formatvorlagen bei Verwendung des [Schatten-Dom][MdnShadowDom].</span><span class="sxs-lookup"><span data-stu-id="273e0-179">Constructable Stylesheets are a new way to create and distribute reusable styles when using [Shadow DOM][MdnShadowDom].</span></span>  

<span data-ttu-id="273e0-180">Beispielsweise wurden die `h1` mit `CSSStyleSheet` \ (CSSOM-APIs \) hinzugefügten Formatvorlagen zuvor nicht bearbeitet.</span><span class="sxs-lookup"><span data-stu-id="273e0-180">For example, the `h1` styles added with `CSSStyleSheet` \(CSSOM APIs\) were not editable previously.</span></span>  <span data-ttu-id="273e0-181">Die Formatvorlagen können jetzt im Bereich " **Formatvorlagen** " bearbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="273e0-181">The styles are editable now in the **Styles** pane.</span></span>  

:::image type="complex" source="../../media/2020/06/css-in-js.msft.png" alt-text="Experimentelle Funktion" lightbox="../../media/2020/06/css-in-js.msft.png":::
   <span data-ttu-id="273e0-183">Ändern der `background` Eigenschaft der `h1` mit `CSSStyleSheet` from `pink` to hinzugefügten Formatvorlagen `lightblue`</span><span class="sxs-lookup"><span data-stu-id="273e0-183">Changing the `background` property of the `h1` styles added with `CSSStyleSheet` from `pink` to `lightblue`.</span></span>
:::image-end:::  

<span data-ttu-id="273e0-184">Geben Sie diesem Feature einen Versuch mit einem [Beispiel, in dem CSS-in-JS verwendet wird][CodepenZoherghadyaliAbdgrpz].</span><span class="sxs-lookup"><span data-stu-id="273e0-184">Give this feature a try with a [sample that uses CSS-in-JS][CodepenZoherghadyaliAbdgrpz].</span></span>

<span data-ttu-id="273e0-185">Chrom Problem [#946975][CR946975]</span><span class="sxs-lookup"><span data-stu-id="273e0-185">Chromium issue [#946975][CR946975]</span></span>  

### <span data-ttu-id="273e0-186">Leuchtturm 6 im Leuchtturm-Panel</span><span class="sxs-lookup"><span data-stu-id="273e0-186">Lighthouse 6 in the Lighthouse panel</span></span>  

<span data-ttu-id="273e0-187">Auf dem **Leuchtturm** -Panel läuft nun Lighthouse 6.</span><span class="sxs-lookup"><span data-stu-id="273e0-187">The **Lighthouse** panel is now running Lighthouse 6.</span></span>  <span data-ttu-id="273e0-188">Eine vollständige Liste aller Änderungen finden Sie unter [v 6.0.0-Versionshinweise][GithubGoogleChromeLighthouse600].</span><span class="sxs-lookup"><span data-stu-id="273e0-188">For a full list of all changes, see [v6.0.0 release notes][GithubGoogleChromeLighthouse600].</span></span>  

<span data-ttu-id="273e0-189">Lighthouse 6,0 führt drei neue Metriken in den Bericht ein: größter Content-Paint \ (LCP \), kumulative Layout-UMSCHALT \ (CLS \) und Gesamt Blockierungszeit \ (TBT \).</span><span class="sxs-lookup"><span data-stu-id="273e0-189">Lighthouse 6.0 introduces three new metrics to the report:  Largest Contentful Paint \(LCP\), Cumulative Layout Shift \(CLS\), and Total Blocking Time \(TBT\).</span></span>  

<span data-ttu-id="273e0-190">Die Formel für die Leistungsbewertung wurde ebenfalls umgewichtet, um die Lade Erfahrung des Benutzers besser wiederzugeben.</span><span class="sxs-lookup"><span data-stu-id="273e0-190">The performance score formula has also been reweighted to better reflect the loading experience of the user.</span></span>  

<span data-ttu-id="273e0-191">Chrom Problem [#772558][CR772558]</span><span class="sxs-lookup"><span data-stu-id="273e0-191">Chromium issue [#772558][CR772558]</span></span>  

#### <span data-ttu-id="273e0-192">Erste aussagekräftige Paint-Missbilligung</span><span class="sxs-lookup"><span data-stu-id="273e0-192">First Meaningful Paint deprecation</span></span>  

<span data-ttu-id="273e0-193">Die erste aussagekräftige Farbe \ (Unterstützung \) ist in Lighthouse 6,0 veraltet.</span><span class="sxs-lookup"><span data-stu-id="273e0-193">First Meaningful Paint \(FMP\) is deprecated in Lighthouse 6.0.</span></span>  <span data-ttu-id="273e0-194">In der **Leistungs** Palette wurde auch das Unternehmen entfernt.</span><span class="sxs-lookup"><span data-stu-id="273e0-194">FMP has also been removed from the **Performance** panel.</span></span>  <span data-ttu-id="273e0-195">Der **größte zufriedene Anstrich** ist der empfohlene Ersatz für die Verwendung von "mehr".</span><span class="sxs-lookup"><span data-stu-id="273e0-195">**Largest Contentful Paint** is the recommended replacement for FMP.</span></span>  <!--See [First Meaningful Paint][WebDevFirstMeaningfulPaint] for an explanation of why it was deprecated.  -->  

<!--todo: add Largest Contentful Paint when section available  -->  
<!--todo: add First Meaningful Paint link and note when available  -->  

<span data-ttu-id="273e0-196">Chrom Problem [#1096008][CR1096008]</span><span class="sxs-lookup"><span data-stu-id="273e0-196">Chromium issue [#1096008][CR1096008]</span></span>  

### <span data-ttu-id="273e0-197">Unterstützung für neue JavaScript-Features</span><span class="sxs-lookup"><span data-stu-id="273e0-197">Support for new JavaScript features</span></span>  

<span data-ttu-id="273e0-198">DevTools bietet nun eine bessere Unterstützung für einige der neuesten JavaScript-Sprachfeatures.</span><span class="sxs-lookup"><span data-stu-id="273e0-198">DevTools now has better support for some of the latest JavaScript language features.</span></span>  

:::row:::
   :::column span="1":::
      <span data-ttu-id="273e0-199">[Optionale Verkettungs][V8DevOptionalChaining] Syntax Autovervollständigung</span><span class="sxs-lookup"><span data-stu-id="273e0-199">[Optional chaining][V8DevOptionalChaining] syntax autocompletion</span></span>  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="273e0-200">Die automatische Vervollständigung von Eigenschaften in der **Konsole** unterstützt jetzt optionale Verkettungs Syntax, beispielsweise  `name?.` jetzt zusätzlich zu `name.` und `name[` .</span><span class="sxs-lookup"><span data-stu-id="273e0-200">Property auto-completion in the **Console** now supports optional chaining syntax, for example,  `name?.` now works in addition to `name.` and `name[`.</span></span>  
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="1":::
      <span data-ttu-id="273e0-201">Syntax Hervorhebung für [private Felder][V8DevClassFieldsPrivate]</span><span class="sxs-lookup"><span data-stu-id="273e0-201">Syntax highlighting for [private fields][V8DevClassFieldsPrivate]</span></span>  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="273e0-202">Private Kurs Felder werden jetzt ordnungsgemäß in der Syntax hervorgehoben und im **Quellen** Panel hübsch gedruckt.</span><span class="sxs-lookup"><span data-stu-id="273e0-202">private class fields are now properly syntax-highlighted and pretty-printed in the **Sources** panel.</span></span>  
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="1":::
      <span data-ttu-id="273e0-203">Syntax Hervorhebung für [ungültigen][V8DevNullishCoalescing] Vereinigungsoperator</span><span class="sxs-lookup"><span data-stu-id="273e0-203">Syntax highlighting for [Nullish coalescing operator][V8DevNullishCoalescing]</span></span>
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="273e0-204">DevTools nun richtig hübsch – druckt den ungültigen Vereinigungsoperator im **Quellen** Panel.</span><span class="sxs-lookup"><span data-stu-id="273e0-204">DevTools now properly pretty-prints the nullish coalescing operator in the **Sources** panel.</span></span>  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="273e0-205">Chrom Probleme [#1073903][CR1073903], [#1083214][CR1083214], [#1083797][CR1083797]</span><span class="sxs-lookup"><span data-stu-id="273e0-205">Chromium issues [#1073903][CR1073903], [#1083214][CR1083214], [#1083797][CR1083797]</span></span>  

### <span data-ttu-id="273e0-206">Neue APP-Verknüpfungs Warnungen im Bereich "Manifest"</span><span class="sxs-lookup"><span data-stu-id="273e0-206">New app shortcut warnings in the Manifest pane</span></span>  

<span data-ttu-id="273e0-207">**App-Tastenkombinationen** helfen Benutzern, häufige oder empfohlene Aufgaben in einer Web-App schnell zu starten.</span><span class="sxs-lookup"><span data-stu-id="273e0-207">**App shortcuts** help users quickly start common or recommended tasks within a web app.</span></span>  

<!--todo: add App shortcuts when section is live  -->  

<span data-ttu-id="273e0-208">Der Bereich **Manifest** zeigt nun Warnungen für die folgenden Bedingungen an.</span><span class="sxs-lookup"><span data-stu-id="273e0-208">The **Manifest** pane now shows warnings for the following conditions.</span></span>  

* <span data-ttu-id="273e0-209">Die APP-Verknüpfungssymbole sind kleiner als 96x96 Pixel</span><span class="sxs-lookup"><span data-stu-id="273e0-209">The app shortcut icons are smaller than 96x96 pixels</span></span>  
* <span data-ttu-id="273e0-210">Die APP-Verknüpfungssymbole und Manifest-Symbole sind nicht quadratisch \ (da die Symbole ignoriert werden \)</span><span class="sxs-lookup"><span data-stu-id="273e0-210">The app shortcut icons and manifest icons are not square \(since the icons are ignored\)</span></span>  

:::image type="complex" source="../../media/2020/06/app-shortcut-warnings.msft.png" alt-text="Experimentelle Funktion" lightbox="../../media/2020/06/app-shortcut-warnings.msft.png":::
   <span data-ttu-id="273e0-212">App-Verknüpfungs Warnungen</span><span class="sxs-lookup"><span data-stu-id="273e0-212">App shortcut warnings</span></span>  
:::image-end:::  

<span data-ttu-id="273e0-213">Chrom Problem [#955497][CR955497]</span><span class="sxs-lookup"><span data-stu-id="273e0-213">Chromium issue [#955497][CR955497]</span></span>  

### <span data-ttu-id="273e0-214">Konsistente Anzeige des berechneten Bereichs</span><span class="sxs-lookup"><span data-stu-id="273e0-214">Consistent display of the Computed pane</span></span>  

<span data-ttu-id="273e0-215">Der **berechnete** Bereich im **Element** Bereich wird nun einheitlich als Bereich für alle Ansichtsfenster Größen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="273e0-215">The **Computed** pane in the **Elements** panel now displays consistently as a pane across all viewport sizes.</span></span>  <span data-ttu-id="273e0-216">Zuvor wurde der **berechnete** Bereich im Bereich " **Formatvorlagen** " zusammengeführt, wenn die Breite des devtools-Viewports schmal war.</span><span class="sxs-lookup"><span data-stu-id="273e0-216">Previously the **Computed** pane merged inside the **Styles** pane when the width of the DevTools viewport was narrow.</span></span>  

:::image type="complex" source="../../media/2020/06/computed-pane.msft.png" alt-text="Experimentelle Funktion" lightbox="../../media/2020/06/computed-pane.msft.png":::
   <span data-ttu-id="273e0-218">Der **berechnete** Bereich wird konsistent als separater Bereich angezeigt, auch wenn die devtools schmal sind.</span><span class="sxs-lookup"><span data-stu-id="273e0-218">The **Computed** pane consistently displays as a separate pane even when the DevTools are narrow.</span></span>
:::image-end:::  

<span data-ttu-id="273e0-219">Chrom Problem [#1073899][CR1073899]</span><span class="sxs-lookup"><span data-stu-id="273e0-219">Chromium issue [#1073899][CR1073899]</span></span>  

### <span data-ttu-id="273e0-220">Bytecode-Offsets für webassemblydateien</span><span class="sxs-lookup"><span data-stu-id="273e0-220">Bytecode offsets for WebAssembly files</span></span>  

<span data-ttu-id="273e0-221">DevTools verwendet jetzt Bytecode-Offsets zum Anzeigen von WASM-Disassembly-Nummern.</span><span class="sxs-lookup"><span data-stu-id="273e0-221">DevTools now uses bytecode offsets for displaying line numbers of Wasm disassembly.</span></span>  
<span data-ttu-id="273e0-222">Durch die Zahlen in der Zeile wird deutlicher, dass Sie Binärdaten suchen, und es ist konsistenter, wie die WASM-Laufzeit auf Speicherorte verweist.</span><span class="sxs-lookup"><span data-stu-id="273e0-222">The line numbers make it clearer that you are looking at binary data, and is more consistent with how the Wasm runtime references locations.</span></span>  

<span data-ttu-id="273e0-223">Chrom Problem [#1071432][CR1071432]</span><span class="sxs-lookup"><span data-stu-id="273e0-223">Chromium issue [#1071432][CR1071432]</span></span>  

### <span data-ttu-id="273e0-224">Kopieren und Ausschneiden der Zeile im Quellen Panel</span><span class="sxs-lookup"><span data-stu-id="273e0-224">Line-wise copy and cut in Sources Panel</span></span>  

<span data-ttu-id="273e0-225">Beim Ausführen von kopieren oder Ausschneiden ohne Auswahl im [Quellcode-Panel-Editor][DevtoolsSourcesEditCssJavascript]kopiert devtools die aktuelle Inhaltszeile oder schneidet sie aus.</span><span class="sxs-lookup"><span data-stu-id="273e0-225">When performing copy or cut with no selection in the [Sources panel editor][DevtoolsSourcesEditCssJavascript], DevTools copies or cuts the current line of content.</span></span>  

:::image type="complex" source="../../media/2020/06/line-wise-cut.msft.png" alt-text="Experimentelle Funktion" lightbox="../../media/2020/06/line-wise-cut.msft.png":::
   <span data-ttu-id="273e0-227">Mit dem Cursor am Ende der Zeile 5, kopieren Sie die gesamte Zeile aus **pen.js** im devtools, und fügen Sie Sie in [Visual Studio-Code][VSCode]ein.</span><span class="sxs-lookup"><span data-stu-id="273e0-227">With the cursor at the end of Line 5, copying the whole line from **pen.js** in the DevTools and pasting in [Visual Studio Code][VSCode].</span></span>
:::image-end:::  

<span data-ttu-id="273e0-228">Chrom Problem [#800028][CR800028]</span><span class="sxs-lookup"><span data-stu-id="273e0-228">Chromium issue [#800028][CR800028]</span></span>

### <span data-ttu-id="273e0-229">Updates für Konsoleneinstellungen</span><span class="sxs-lookup"><span data-stu-id="273e0-229">Console Settings updates</span></span>  

#### <span data-ttu-id="273e0-230">Aufheben der Gruppierung derselben Konsolen Nachrichten</span><span class="sxs-lookup"><span data-stu-id="273e0-230">Ungroup same console messages</span></span>  

<span data-ttu-id="273e0-231">Die **Gruppe ähnliche** Umschalter in den Konsoleneinstellungen gilt jetzt für doppelte Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="273e0-231">The **Group similar** toggle in Console Settings now applies to duplicate messages.</span></span>  <span data-ttu-id="273e0-232">Zuvor hat es gerade auf ähnliche Nachrichten angewendet.</span><span class="sxs-lookup"><span data-stu-id="273e0-232">Previously it just applied to similar messages.</span></span>  

<span data-ttu-id="273e0-233">Zuvor hat devtools die Gruppierung der Nachrichten nicht aufheben, obwohl `hello` **Gruppe ähnlich** deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="273e0-233">For example, previously, DevTools did not ungroup the `hello` messages even though **Group similar** is unchecked.</span></span>  <span data-ttu-id="273e0-234">Nun werden die `hello` Nachrichten nicht gruppiert.</span><span class="sxs-lookup"><span data-stu-id="273e0-234">Now, the `hello` messages are ungrouped.</span></span>  

:::image type="complex" source="../../media/2020/06/ungroup-similar.msft.png" alt-text="Experimentelle Funktion" lightbox="../../media/2020/06/ungroup-similar.msft.png":::
   <span data-ttu-id="273e0-236">Wenn **"Gruppe ähnlich"** deaktiviert ist, `hello` werden die Nachrichten nicht gruppiert</span><span class="sxs-lookup"><span data-stu-id="273e0-236">When **Group similar** is unchecked, the `hello` messages are ungrouped</span></span>
:::image-end:::  

<span data-ttu-id="273e0-237">Geben Sie diesem Feature einen Versuch mit einem [Beispiel, mit dem doppelte Nachrichten an die Konsole gesendet werden][CodepenZoherghadyaliZyrjgdJ].</span><span class="sxs-lookup"><span data-stu-id="273e0-237">Give this feature a try with a [sample that sends duplicate messages to the Console][CodepenZoherghadyaliZyrjgdJ].</span></span>  

<span data-ttu-id="273e0-238">Chrom Problem [#1082963][CR1082963]</span><span class="sxs-lookup"><span data-stu-id="273e0-238">Chromium issue [#1082963][CR1082963]</span></span>  

### <span data-ttu-id="273e0-239">Nur ausgewählte Kontext Einstellungen beibehalten</span><span class="sxs-lookup"><span data-stu-id="273e0-239">Persisting Selected context only settings</span></span>  

<span data-ttu-id="273e0-240">Die Einstellungen für den **ausgewählten Kontext nur** in den Konsoleneinstellungen werden nun beibehalten.</span><span class="sxs-lookup"><span data-stu-id="273e0-240">The **Selected context only** settings in Console Settings is now persisted.</span></span>  <span data-ttu-id="273e0-241">Zuvor wurden die Einstellungen jedes Mal zurückgesetzt, wenn Sie devtools geschlossen und wieder geöffnet haben.</span><span class="sxs-lookup"><span data-stu-id="273e0-241">Previously the settings were reset every time you closed and reopened DevTools.</span></span>  <span data-ttu-id="273e0-242">Durch die Änderung wird das Einstellungsverhalten mit anderen Optionen für Konsoleneinstellungen konsistent.</span><span class="sxs-lookup"><span data-stu-id="273e0-242">The change makes the setting behavior consistent with other Console Settings options.</span></span>  

:::image type="complex" source="../../media/2020/06/selected-context.msft.png" alt-text="Experimentelle Funktion" lightbox="../../media/2020/06/selected-context.msft.png":::
   <span data-ttu-id="273e0-244">**Nur ausgewählte Kontext** Einstellung</span><span class="sxs-lookup"><span data-stu-id="273e0-244">**Selected context only** setting</span></span>  
:::image-end:::  

<span data-ttu-id="273e0-245">Chrom Problem [#1055875][CR1055875]</span><span class="sxs-lookup"><span data-stu-id="273e0-245">Chromium issue [#1055875][CR1055875]</span></span>  

### <span data-ttu-id="273e0-246">Updates für das Leistungs Panel</span><span class="sxs-lookup"><span data-stu-id="273e0-246">Performance panel updates</span></span>  

#### <span data-ttu-id="273e0-247">Informationen zum Cache für JavaScript-Kompilierung im Leistungs Panel</span><span class="sxs-lookup"><span data-stu-id="273e0-247">JavaScript compilation cache information in Performance panel</span></span>  

<span data-ttu-id="273e0-248">Die [Informationen im JavaScript-Kompilierungs Cache][V8DevCodeCaching] werden jetzt immer auf der Registerkarte "Zusammenfassung" im Leistungsfenster angezeigt.</span><span class="sxs-lookup"><span data-stu-id="273e0-248">[JavaScript compilation cache information][V8DevCodeCaching] is now always displayed in the Summary tab of the Performance panel.</span></span>  <span data-ttu-id="273e0-249">Zuvor zeigten devtools nichts im Zusammenhang mit der Code Zwischenspeicherung an, wenn die Code Zwischenspeicherung nicht statt fand.</span><span class="sxs-lookup"><span data-stu-id="273e0-249">Previously, DevTools did not show anything related to code caching if code caching did not happen.</span></span>  

:::image type="complex" source="../../media/2020/06/js-compilation-cache.msft.png" alt-text="Experimentelle Funktion" lightbox="../../media/2020/06/js-compilation-cache.msft.png":::
   <span data-ttu-id="273e0-251">Informationen zum Cache für JavaScript-Kompilierung</span><span class="sxs-lookup"><span data-stu-id="273e0-251">JavaScript compilation cache information</span></span>  
:::image-end:::  

<span data-ttu-id="273e0-252">Chrom Problem [#912581][CR912581]</span><span class="sxs-lookup"><span data-stu-id="273e0-252">Chromium issue [#912581][CR912581]</span></span>  

#### <span data-ttu-id="273e0-253">Ausrichtung der Navigationsanzeige im Leistungsbereich</span><span class="sxs-lookup"><span data-stu-id="273e0-253">Navigation timing alignment in the Performance panel</span></span>  

<span data-ttu-id="273e0-254">Im **Leistungs** Panel werden die Zeiten in den Linealen basierend auf dem Beginn der Aufzeichnung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="273e0-254">The **Performance** panel used to show times in the rulers based on when the recording started.</span></span>  <span data-ttu-id="273e0-255">Die Anzeigedauer wurde für Aufzeichnungen geändert, in denen der Benutzer navigiert, wobei in devtools nun stattdessen die linealzeiten relativ zur Navigation angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="273e0-255">The timing has now changed for recordings where the user navigates, where DevTools now shows ruler times relative to the navigation instead.</span></span>  

:::image type="complex" source="../../media/2020/06/nav-timing.msft.png" alt-text="Experimentelle Funktion" lightbox="../../media/2020/06/nav-timing.msft.png":::
   <span data-ttu-id="273e0-257">Ausrichten der Navigationsanzeige im **Leistungs** Bereich</span><span class="sxs-lookup"><span data-stu-id="273e0-257">Align navigation timing in **Performance** panel</span></span>  
:::image-end:::  

<span data-ttu-id="273e0-258">Die Zeiten für `DOMContentLoaded` , erster Anstrich, erster Inhaltsbezogener Paint und die größten inhaltsabhängigen Paint-Ereignisse werden relativ zum Anfang der Navigation aktualisiert, was bedeutet, dass die Anzeigedauer den angegebenen Anzeigedauern entspricht `PerformanceObserver` .</span><span class="sxs-lookup"><span data-stu-id="273e0-258">The times for `DOMContentLoaded`, First Paint, First Contentful Paint, and Largest Contentful Paint events are updated to be relative to the start of the navigation, which means the timing matches the timings reported by `PerformanceObserver`.</span></span>  

<span data-ttu-id="273e0-259">Chrom Problem [#974550][CR974550]</span><span class="sxs-lookup"><span data-stu-id="273e0-259">Chromium issue [#974550][CR974550]</span></span>  

### <span data-ttu-id="273e0-260">Neue Symbole für Haltepunkte, bedingte Haltepunkte und logpoints</span><span class="sxs-lookup"><span data-stu-id="273e0-260">New icons for breakpoints, conditional breakpoints, and logpoints</span></span>  

<span data-ttu-id="273e0-261">Das **Quellen** Panel enthält neue Designs für Haltepunkte, bedingte Haltepunkte und logpoints.</span><span class="sxs-lookup"><span data-stu-id="273e0-261">The **Sources** panel has new designs for breakpoints, conditional breakpoints, and logpoints.</span></span>  <span data-ttu-id="273e0-262">Haltepunkte werden durch einen roten Kreis dargestellt, genau wie [Visual Studio-Code][VSCode] und [Visual Studio][VS].</span><span class="sxs-lookup"><span data-stu-id="273e0-262">Breakpoints are represented by a red circle, just like [Visual Studio Code][VSCode] and [Visual Studio][VS].</span></span>  <span data-ttu-id="273e0-263">Symbole werden hinzugefügt, um bedingte Haltepunkte und logpoints zu unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="273e0-263">Icons are added to differentiate conditional breakpoints and logpoints.</span></span>  

:::image type="complex" source="../../media/2020/06/breakpoints.msft.png" alt-text="Experimentelle Funktion" lightbox="../../media/2020/06/breakpoints.msft.png":::
   <span data-ttu-id="273e0-265">Breakpoints</span><span class="sxs-lookup"><span data-stu-id="273e0-265">Breakpoints</span></span>  
:::image-end:::  

<span data-ttu-id="273e0-266">Chrom Problem [#1041830][CR1041830]</span><span class="sxs-lookup"><span data-stu-id="273e0-266">Chromium issue [#1041830][CR1041830]</span></span>  

## <span data-ttu-id="273e0-267">Herunterladen der Microsoft Edge Preview-Kanäle</span><span class="sxs-lookup"><span data-stu-id="273e0-267">Download the Microsoft Edge preview channels</span></span>  

<span data-ttu-id="273e0-268">Wenn Sie unter Windows oder macOS arbeiten, sollten Sie die [Microsoft Edge Preview-Kanäle][MicrosoftEdgePreviewChannels] als Standard Entwicklungsbrowser verwenden.</span><span class="sxs-lookup"><span data-stu-id="273e0-268">If you are on Windows or macOS, consider using the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] as your default development browser.</span></span>  <span data-ttu-id="273e0-269">Über die Vorschau Kanäle erhalten Sie Zugriff auf die neuesten devtools-Funktionen.</span><span class="sxs-lookup"><span data-stu-id="273e0-269">The preview channels give you access to the latest DevTools features.</span></span>  

## <span data-ttu-id="273e0-270">Kontakt mit dem Microsoft Edge devtools-Team</span><span class="sxs-lookup"><span data-stu-id="273e0-270">Getting in touch with Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]  

<!-- links -->  

[DevtoolsMain]: /microsoft-edge/devtools-guide-chromium "Microsoft Edge (Chrom)-Entwickler Tools | Microsoft docs"  
[DevtoolsCommandMenu]: /microsoft-edge/devtools-guide-chromium/command-menu "Ausführen von Befehlen mit dem Befehlsmenü von Microsoft Edge devtools | Microsoft docs"
[DevtoolsCustomizeIndexDrawer]: /microsoft-edge/devtools-guide-chromium/customize/index#drawer "Schublade – Anpassen von Microsoft Edge devtools | Microsoft docs"
[DevtoolsExperimentalFeaturesTurnOn]: /microsoft-edge/devtools-guide-chromium/experimental-features#turn-on-experimental-features "Aktivieren von experimentellen Features – experimentelle Features | Microsoft docs"  
[DevtoolsIssues]: /microsoft-edge/devtools-guide-chromium/issues "Suchen und Beheben von Problemen mit dem Microsoft Edge devtools Issues Tool | Microsoft docs"
[DevtoolsSourcesEditCssJavascript]: /microsoft-edge/devtools-guide-chromium/sources#edit-css-and-javascript "Bearbeiten von CSS und JavaScript – Übersicht über das Quellen Panel | Microsoft docs"  
[DevtoolsNetworkIndexLogActivity]: /microsoft-edge/devtools-guide-chromium/network/index#log-network-activity "Protokollieren von Netzwerkaktivitäten – Überprüfen der Netzwerkaktivität in Microsoft Edge devtools | Microsoft docs"

[CodepenZoherghadyaliAbdgrpz]: https://codepen.io/zoherghadyali/full/abdGrPZ "Format Bearbeitung für CSS-in-JS-Frameworks | CodePen"
[CodepenZoherghadyaliZyrjgdJ]: https://codepen.io/zoherghadyali/full/zYrjgdJ "Doppelte Nachrichten an Konsole senden | CodePen"
[CodepenRachelweilYzwBzKM]: https://codepen.io/hxlnt/full/YzwBzKM "CSS-Raster Planner-Beispiel | CodePen"

[CRIssuesList]: https://bugs.chromium.org/p/chromium/issues/list "Chrom Fehler"  

[CR772558]: https://crbug.com/772558 "DevTools: Update auf die neueste Version von Lighthouse | Chrom Fehler"  
[CR800028]: https://crbug.com/800028 "Verknüpfung "doppelte Zeile" im Entwickler Tools-Editor funktioniert nach dem Chrome-Update nicht Chrom Fehler"  
[CR912581]: https://crbug.com/912581 "Verfügbar machen, welche Skripts vom V8-Code zwischengespeichert wurden in devtools/about: Ablaufverfolgung | Chrom Fehler"  
[CR946975]: https://crbug.com/946975 "DevTools-Formatvorlagen-Seitenleiste funktioniert nicht mit konstruierten Stylesheets | Chrom Fehler"  
[CR955497]: https://crbug.com/955497 "Kontextmenü für App-Symbole für PWAs | Chrom Fehler"  
[CR974550]: https://crbug.com/974550 "Metrische Diskrepanz zwischen perf Panel und performanceObserver | Chrom Fehler"  
[CR1041830]: https://crbug.com/1041830 "Verbessern der Farben für Haltepunkte | Chrom Fehler"  
[CR1055875]: https://crbug.com/1055875 "Der Wert der Einstellung nur ausgewählte Kontext Konsole wird nach dem Schließen und erneuten Öffnen von Entwickler Tools nicht beibehalten | Chrom Fehler"  
[CR1066579]: https://crbug.com/1066579 "DevTools: Anzeigen der ServiceWorkers-Abruf Zeitachse pro Anforderung in der Netzwerksteuerung | Chrom Fehler"  
[CR1071432]: https://crbug.com/1071432 "WASM Basic Developer Experience | Chrom Fehler"  
[CR1073899]: https://crbug.com/1073899 "Die Registerkarte "berechnete Formatvorlage" verschwindet im reaktionsfähigen Modus | Chrom Fehler"  
[CR1073903]: https://crbug.com/1073903 "DevTools: Syntax Hervorhebung funktioniert nicht mit privaten Feldern | Chrom Fehler"  
[CR1082963]: https://crbug.com/1082963 "Das Verhalten der Konsolen Gruppe für ähnliche Nachrichten kann nicht deaktiviert werden | Chrom Fehler"  
[CR1083214]: https://crbug.com/1083214 "Acorn unterstützt keine optionalen Verkettungen | Chrom Fehler"  
[CR1083797]: https://crbug.com/1083797 "Pretty printing Broken für NULL-verschmilzt | Chrom Fehler"  
[CR1096008]: https://crbug.com/1096008 "Entfernen von "aus" | Chrom Fehler"  
[CR1047356]: https://crbug.com/1047356 "CSS Grid/Flexbox/Tabellentools | Chrom Fehler"  
[CR1093687]: https://crbug.com/1093687 "Tool zum Erstellen und Wiedergeben von synthetischen Netzwerkanforderungen | Chrom Fehler"  
[CR1070378]: https://crbug.com/1070378 "Integrieren von webhint in devtools | Chrom Fehler"  
[CR1069404]: https://crbug.com/1069404 "[Dev tools] widget Popups sind zu alle schmal | Chrom Fehler"  
[CR897944]: https://crbug.com/897944 "Verschieb DevTool Panels | Chrom Fehler"

[GithubGoogleChromeLighthouse600]: https://github.com/GoogleChrome/lighthouse/releases/tag/v6.0.0 "v 6.0.0-GoogleChrome/Lighthouse | GitHub"  

[GitHubMicrosoftDocsEdgeDeveloperNewIssue]: https://github.com/MicrosoftDocs/edge-developer/issues/new?title=[DevTools%20Docs%20Feedback] "Neues Problem – MicrosoftDocs/Edge – Entwickler"  

[MdnShadowDom]: https://developer.mozilla.org/docs/Web/Web_Components/Using_shadow_DOM "Verwenden des Schatten-Dom | MDN"

[MicrosoftEdgePreviewChannels]: https://www.microsoftedgeinsider.com/download/ "Microsoft Edge Preview-Kanäle"  

[VS]: https://visualstudio.microsoft.com/ "Visual Studio"
[VSCode]: https://code.visualstudio.com/ "Visual Studio-Code"  

[CsswgDraftsCssom]: https://drafts.csswg.org/cssom "CSS-Objektmodell (CSSOM) | W3C CSS-Arbeitsgruppen-Editor-Entwürfe"  

[PostTweetEdgeDevTools]: https://twitter.com/intent/tweet?text=@EdgeDevTools "@EdgeDevTools | Einen Tweet Posten"  
[EdgeDevToolsTwitterAccount]: https://twitter.com/EdgeDevTools "@EdgeDevTools Twitter-Konto"  

[V8DevClassFieldsPrivate]: https://v8.dev/features/class-fields#private-class-fields "Private Kurs Felder – öffentliche und private Kurs Felder | V8. Dev"  
[V8DevCodeCaching]: https://v8.dev/blog/code-caching-for-devs "Code Zwischenspeicherung für JavaScript-Entwickler | V8. Dev"  
[V8DevNullishCoalescing]: https://v8.dev/features/nullish-coalescing "Ungültiges vereinigen | V8. Dev"  
[V8DevOptionalChaining]: https://v8.dev/features/optional-chaining "Optionale Verkettung | V8. Dev"  

[WebhintMain]: https://webhint.io "webhint"  

[WicgConstructStylesheet]: https://wicg.github.io/construct-stylesheets/ "Konstruktable Stylesheet-Objekte | Web Inkubator CG"

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

[TheWebWeWant]: https://webwewant.fyi/ "Das gewünschte Web"  

> [!NOTE]
> <span data-ttu-id="273e0-319">Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="273e0-319">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="273e0-320">Die ursprüngliche Seite wird [hier](https://developers.google.com/web/updates/2020/06/devtools/index) gefunden und von [Jecelyn Yeen][JecelynYeen] \ (Developer Advocate, Chrome devtools \) erstellt.</span><span class="sxs-lookup"><span data-stu-id="273e0-320">The original page is found [here](https://developers.google.com/web/updates/2020/06/devtools/index) and is authored by [Jecelyn Yeen][JecelynYeen] \(Developer advocate, Chrome DevTools\).</span></span>  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
<span data-ttu-id="273e0-322">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="273e0-322">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[JecelynYeen]: https://developers.google.com/web/resources/contributors/jecelynyeen  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
