---
title: Neuerungen in devtools (Microsoft Edge 85)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/24/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: 7b0193d25fb1d081e5746ec1271ca7b9f4e60c23
ms.sourcegitcommit: ad5eb43172280974b8c063867c2097f7c5c0e77d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/27/2020
ms.locfileid: "10898311"
---
# <span data-ttu-id="890d9-103">Neuerungen in devtools (Microsoft Edge 85)</span><span class="sxs-lookup"><span data-stu-id="890d9-103">What's New In DevTools (Microsoft Edge 85)</span></span>  

## <span data-ttu-id="890d9-104">Ankündigungen des Microsoft Edge devtools-Teams</span><span class="sxs-lookup"><span data-stu-id="890d9-104">Announcements from the Microsoft Edge DevTools team</span></span>  

<span data-ttu-id="890d9-105">In den folgenden Abschnitten finden Sie eine Liste der Ankündigungen, die Sie möglicherweise im Microsoft Edge devtools-Team verpasst haben.</span><span class="sxs-lookup"><span data-stu-id="890d9-105">The following sections are a list of announcements you may have missed from the Microsoft Edge DevTools team.</span></span>  <span data-ttu-id="890d9-106">Schauen Sie sich die Ankündigungen an, um neue Features in den devtools, vs-Code Erweiterungen und vielem mehr auszuprobieren.</span><span class="sxs-lookup"><span data-stu-id="890d9-106">See the announcements to try new features in the DevTools, VS Code extensions, and more.</span></span>  <span data-ttu-id="890d9-107">Wenn Sie über die neuesten und besten Funktionen Ihrer Entwicklertools auf dem Laufenden bleiben möchten, laden Sie die [Microsoft Edge Preview-Kanäle][MicrosoftEdgePreviewChannels] herunter, und [folgen Sie dem Microsoft Edge devtools-Team auf Twitter][EdgeDevToolsTwitterAccount].</span><span class="sxs-lookup"><span data-stu-id="890d9-107">To stay up to date on all the latest and greatest features in your developer tools, download the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] and [follow the Microsoft Edge DevTools team on Twitter][EdgeDevToolsTwitterAccount].</span></span>  

### <span data-ttu-id="890d9-108">Debuggen von CSS-Raster Features</span><span class="sxs-lookup"><span data-stu-id="890d9-108">CSS grid debugging features</span></span>  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Experimentelle Funktion":::
   <span data-ttu-id="890d9-110">Experimentelle Funktion</span><span class="sxs-lookup"><span data-stu-id="890d9-110">Experimental feature</span></span>  
:::image-end:::  

<span data-ttu-id="890d9-111">Das Microsoft Edge devtools-Team kooperiert mit der Chrome-devtools-Team-und Chrom-Community, um neue CSS-Raster Debugging-Features zu devtools hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="890d9-111">The Microsoft Edge DevTools team is collaborating with the Chrome DevTools team and Chromium community to add new CSS grid debugging features to DevTools.</span></span>  <span data-ttu-id="890d9-112">Sie können nun Rasterlinien Nummern, Rasterabstände und erweiterte Rasterlinien als eine auf Seiten Überlagerungen anzeigen.</span><span class="sxs-lookup"><span data-stu-id="890d9-112">You are now able to display grid line numbers, grid gaps, and extended grid lines as an on-page overlay.</span></span>  <span data-ttu-id="890d9-113">Darüber hinaus werden in Kürze weitere Verbesserungen an den Grid-Tools durchkommen.</span><span class="sxs-lookup"><span data-stu-id="890d9-113">Plus, more improvements to the grid tools are coming soon.</span></span>  

:::image type="complex" source="../../media/2020/06/experiments-grid.msft.png" alt-text="Debuggen von CSS-Raster Features" lightbox="../../media/2020/06/experiments-grid.msft.png":::
   <span data-ttu-id="890d9-115">Debuggen von CSS-Raster Features</span><span class="sxs-lookup"><span data-stu-id="890d9-115">CSS grid debugging features</span></span>
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="890d9-116">Wenn Sie das Experiment aktivieren möchten, lesen Sie aktivieren [von experimentellen Features][DevtoolsExperimentalFeaturesTurnOn] , und aktivieren Sie das Kontrollkästchen neben " **neue CSS-Raster Debuggen"-Features aktivieren**.</span><span class="sxs-lookup"><span data-stu-id="890d9-116">To enable the experiment, see [Turn on experimental features][DevtoolsExperimentalFeaturesTurnOn] and select the checkbox next to **Enable new CSS Grid debugging features**.</span></span>  
> 
> <span data-ttu-id="890d9-117">Wenn Sie das Experiment mit einem Beispiel testen möchten, lesen Sie [Beispiel für CSS-Raster Planner][CodepenRachelweilYzwBzKM].</span><span class="sxs-lookup"><span data-stu-id="890d9-117">To try out the experiment with a sample, see [CSS Grid planner example][CodepenRachelweilYzwBzKM].</span></span>  

<span data-ttu-id="890d9-118">Chrom Problem [#1047356][CR1047356]</span><span class="sxs-lookup"><span data-stu-id="890d9-118">Chromium issue [#1047356][CR1047356]</span></span>  

### <span data-ttu-id="890d9-119">Bearbeiten und Wiedergeben von Anforderungen mit der Netzwerk Konsole</span><span class="sxs-lookup"><span data-stu-id="890d9-119">Edit and Replay requests with the Network Console</span></span>  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Experimentelle Funktion":::
   <span data-ttu-id="890d9-121">Experimentelle Funktion</span><span class="sxs-lookup"><span data-stu-id="890d9-121">Experimental feature</span></span>  
:::image-end:::  

<span data-ttu-id="890d9-122">Sie können jetzt die **Bearbeitung und Wiedergabe** von Anforderungen im [Netzwerkprotokoll][DevtoolsNetworkIndexLogActivity] über die **Netzwerk Konsole**verwenden.</span><span class="sxs-lookup"><span data-stu-id="890d9-122">You are now able to use **Edit and Replay** on requests in the [Network Log][DevtoolsNetworkIndexLogActivity] using the **Network Console**.</span></span>  

:::image type="complex" source="../../media/2020/06/experiments-network-console-edit-and-replay.msft.png" alt-text="Bearbeiten und Wiedergeben einer Anforderung im NetworkLog mit der Netzwerk Konsole" lightbox="../../media/2020/06/experiments-network-console-edit-and-replay.msft.png":::
   <span data-ttu-id="890d9-124">Bearbeiten und Wiedergeben einer Anforderung im [NetworkLog][DevtoolsNetworkIndexLogActivity] mit der **Netzwerk Konsole**</span><span class="sxs-lookup"><span data-stu-id="890d9-124">Edit and Replay a request in the [NetworkLog][DevtoolsNetworkIndexLogActivity] with the **Network Console**</span></span>  
:::image-end:::  

<span data-ttu-id="890d9-125">Ein neues Panel, die **Netzwerk Konsole** wird im [devtools-Einzug][DevtoolsCustomizeIndexDrawer] geöffnet und füllt automatisch Informationen für die HTTP-Anforderung auf.</span><span class="sxs-lookup"><span data-stu-id="890d9-125">A new panel, the **Network Console** opens in the [DevTools Drawer][DevtoolsCustomizeIndexDrawer] and automatically populates with information for the HTTP request.</span></span>  <span data-ttu-id="890d9-126">Um die vom Server zurückgegebene Antwort anzuzeigen, bearbeiten Sie die Anforderung \ (falls erforderlich \), und wählen Sie **senden**aus.</span><span class="sxs-lookup"><span data-stu-id="890d9-126">To see the response returned from the server, edit the request \(if needed\) and select **Send**.</span></span>  

<span data-ttu-id="890d9-127">Sie können auch die **Netzwerk Konsole** verwenden, um HTTP-Anforderungen direkt aus dem devtools zu erstellen und zu senden.</span><span class="sxs-lookup"><span data-stu-id="890d9-127">You may also use the **Network Console** to create and send HTTP requests directly from the DevTools.</span></span>  

:::image type="complex" source="../../media/2020/06/experiments-network-console.msft.png" alt-text="Das Netzwerkkonsolen Panel" lightbox="../../media/2020/06/experiments-network-console.msft.png":::
   <span data-ttu-id="890d9-129">Das **Netzwerkkonsolen** Panel</span><span class="sxs-lookup"><span data-stu-id="890d9-129">The **Network Console** panel</span></span>  
:::image-end:::  

> [!TIP]
> <span data-ttu-id="890d9-130">Informationen zum Anzeigen der **Netzwerk Konsole** im Hauptbereich \ (oben \) anstelle der [devtools-Schublade][DevtoolsCustomizeIndexDrawer]finden Sie unter [Verschieben von Tools zwischen Bereichen](#move-tools-between-panels).</span><span class="sxs-lookup"><span data-stu-id="890d9-130">To see **Network Console** in the main \(top\) panel instead of the [DevTools Drawer][DevtoolsCustomizeIndexDrawer], see [moving tools between panels](#move-tools-between-panels).</span></span>  

> [!NOTE]
> <span data-ttu-id="890d9-131">Wenn Sie das Experiment aktivieren möchten, lesen Sie aktivieren [von experimentellen Features][DevtoolsExperimentalFeaturesTurnOn] , und aktivieren Sie das Kontrollkästchen neben **Netzwerk Konsole aktivieren**.</span><span class="sxs-lookup"><span data-stu-id="890d9-131">To enable the experiment, see [Turn on experimental features][DevtoolsExperimentalFeaturesTurnOn] and select the checkbox next to **Enable Network Console**.</span></span>  
> 
> <span data-ttu-id="890d9-132">Öffnen Sie das [Netzwerkprotokoll][DevtoolsNetworkIndexLogActivity], öffnen Sie das Kontextmenü \ (Klicken Sie mit der rechten Maustaste auf \), und wählen Sie **Bearbeiten und wiedergeben**aus.</span><span class="sxs-lookup"><span data-stu-id="890d9-132">Open the [Network Log][DevtoolsNetworkIndexLogActivity], open the contextual menu \(right-click\), and select **Edit and Replay**.</span></span>  

<span data-ttu-id="890d9-133">Chrom Problem [#1093687][CR1093687]</span><span class="sxs-lookup"><span data-stu-id="890d9-133">Chromium issue [#1093687][CR1093687]</span></span>  

### <span data-ttu-id="890d9-134">Service Worker-respondWith-Ereignisse auf der Registerkarte "Anzeigedauer"</span><span class="sxs-lookup"><span data-stu-id="890d9-134">Service worker respondWith events in the Timing tab</span></span>  

<span data-ttu-id="890d9-135">Die Registerkarte " **Anzeige** Dauer" des **Netzwerk** Panels enthält jetzt `respondWith` Service Worker-Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="890d9-135">The **Timing** tab of the **Network** panel now includes `respondWith` service worker events.</span></span>  <span data-ttu-id="890d9-136">Das `respondWith` Dienst Arbeitskraft-Ereignis zeigt die Dauer ab dem Zeitpunkt an, zu dem der Service Worker- `fetch` Ereignishandler mit dem Zeitpunkt beginnt, zu dem das `respondWith` Versprechen des `fetch` Handlers abgerechnet wird.</span><span class="sxs-lookup"><span data-stu-id="890d9-136">The `respondWith` service worker event shows the duration from the time immediately before the service worker `fetch` event handler starts running to the time when the `respondWith` promise of the `fetch` handler is settled.</span></span>  

:::image type="complex" source="../../media/2020/06/timing-tab.msft.png" alt-text="Das respondWith-Dienst Arbeitskraft Ereignis auf der Registerkarte "Anzeigedauer" des Netzwerk Panels" lightbox="../../media/2020/06/timing-tab.msft.png":::
   <span data-ttu-id="890d9-138">Das `respondWith` Service Worker-Ereignis auf der Registerkarte " **Anzeige** Dauer" des **Netzwerk** Panels</span><span class="sxs-lookup"><span data-stu-id="890d9-138">The `respondWith` service worker event in the **Timing** tab of the **Network** panel</span></span>  
:::image-end:::  

<span data-ttu-id="890d9-139">Erweitern der **empfangenen Antwort** , um weitere Informationen aus der `fetch` Antwort wie `CacheStorageCacheName` , `serviceWorkerResponseSource` und anzuzeigen `ResponseTime` .</span><span class="sxs-lookup"><span data-stu-id="890d9-139">Expand **Response received** to see additional information from the `fetch` response like `CacheStorageCacheName`, `serviceWorkerResponseSource`, and `ResponseTime`.</span></span>  

:::image type="complex" source="../../media/2020/06/timing-tab2.msft.png" alt-text="Erweitern der empfangenen Antwort, um weitere Informationen aus der Abruf Antwort anzuzeigen" lightbox="../../media/2020/06/timing-tab2.msft.png":::
   <span data-ttu-id="890d9-141">Erweitern der **empfangenen Antwort** , um weitere Informationen aus der `fetch` Antwort anzuzeigen</span><span class="sxs-lookup"><span data-stu-id="890d9-141">Expand **Response received** to see additional information from the `fetch` response</span></span>  
:::image-end:::  

<span data-ttu-id="890d9-142">Chrom Problem [#1066579][CR1066579]</span><span class="sxs-lookup"><span data-stu-id="890d9-142">Chromium issue [#1066579][CR1066579]</span></span>  

### <span data-ttu-id="890d9-143">webhint-Feedback im Bereich "Probleme"</span><span class="sxs-lookup"><span data-stu-id="890d9-143">webhint feedback in the Issues panel</span></span>  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Experimentelle Funktion":::
   <span data-ttu-id="890d9-145">Experimentelle Funktion</span><span class="sxs-lookup"><span data-stu-id="890d9-145">Experimental feature</span></span>  
:::image-end:::  

<span data-ttu-id="890d9-146">[webhint][WebhintMain] ist ein Open-Source-Tool, das in Echtzeit Feedback zur Barrierefreiheit, browserübergreifenden Kompatibilität, Sicherheit, Leistung, PWAs und anderen gängigen Webentwicklungs Problemen von Websites bietet.</span><span class="sxs-lookup"><span data-stu-id="890d9-146">[webhint][WebhintMain] is an open-source tool that provides real-time feedback on the accessibility, cross-browser compatibility, security, performance, PWAs, and other common web development issues of websites.</span></span>  <span data-ttu-id="890d9-147">Sie können jetzt webhint-Feedback im [Problem][DevtoolsIssues] Bereich anzeigen.</span><span class="sxs-lookup"><span data-stu-id="890d9-147">You are now able to see webhint feedback in the [Issues][DevtoolsIssues] panel.</span></span>  

:::image type="complex" source="../../media/2020/06/experiments-webhint.msft.png" alt-text="webhint-Feedback im Bereich "Probleme"" lightbox="../../media/2020/06/experiments-webhint.msft.png":::
   <span data-ttu-id="890d9-149">webhint-Feedback im Bereich "Probleme"</span><span class="sxs-lookup"><span data-stu-id="890d9-149">webhint feedback in the Issues panel</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="890d9-150">Wenn Sie das Experiment aktivieren möchten, lesen Sie aktivieren [von experimentellen Features][DevtoolsExperimentalFeaturesTurnOn] , und aktivieren Sie das Kontrollkästchen neben **webhint aktivieren**.</span><span class="sxs-lookup"><span data-stu-id="890d9-150">To enable the experiment, see [Turn on experimental features][DevtoolsExperimentalFeaturesTurnOn] and select the checkbox next to **Enable webhint**.</span></span>  
> 
> <span data-ttu-id="890d9-151">Öffnen Sie den Bereich [Probleme][DevtoolsIssues] , um Feedback von webhint anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="890d9-151">Open the [Issues][DevtoolsIssues] panel to see feedback from webhint.</span></span>  

<span data-ttu-id="890d9-152">Chrom Problem [#1070378][CR1070378]</span><span class="sxs-lookup"><span data-stu-id="890d9-152">Chromium issue [#1070378][CR1070378]</span></span>  

### <span data-ttu-id="890d9-153">Verschieben von Tools zwischen Bereichen</span><span class="sxs-lookup"><span data-stu-id="890d9-153">Move tools between panels</span></span>  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Experimentelle Funktion":::
   <span data-ttu-id="890d9-155">Experimentelle Funktion</span><span class="sxs-lookup"><span data-stu-id="890d9-155">Experimental feature</span></span>  
:::image-end:::  

<span data-ttu-id="890d9-156">In der Regel können Tools, wie **Elemente** und **Netzwerke** , nur im Hauptbereich \ (oben \) von devtools geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="890d9-156">Normally, tools such as **Elements** and **Network** may only be opened in the main \(top\) panel of DevTools.</span></span>  <span data-ttu-id="890d9-157">Auf ähnliche Weise können Tools wie **3D-Ansicht** und **Probleme** nur im Bereich "drawer \ (unten \)" von devtools geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="890d9-157">Similarly, tools such as **3D View** and **Issues** may only be opened in the drawer \(bottom\) panel of DevTools.</span></span>  <span data-ttu-id="890d9-158">Sie können jetzt Ihr devtools-Layout anpassen, indem Sie die Tools zwischen dem oberen und unteren Bereich verschieben.</span><span class="sxs-lookup"><span data-stu-id="890d9-158">You are now able to customize your DevTools layout by moving tools between the top and bottom panels.</span></span>  

:::image type="complex" source="../../media/2020/06/experiments-move-panels.msft.png" alt-text="Verschieben von Tabstopps zwischen Bereichen" lightbox="../../media/2020/06/experiments-move-panels.msft.png":::
   <span data-ttu-id="890d9-160">Verschieben von Tabstopps zwischen Bereichen</span><span class="sxs-lookup"><span data-stu-id="890d9-160">Moving tabs between panels</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="890d9-161">Wenn Sie das Experiment aktivieren möchten, lesen Sie aktivieren [von experimentellen Features][DevtoolsExperimentalFeaturesTurnOn] , und aktivieren Sie das Kontrollkästchen neben **Unterstützung aktivieren, um Tabstopps zwischen Bereichen zu verschieben**.</span><span class="sxs-lookup"><span data-stu-id="890d9-161">To enable the experiment, see [Turn on experimental features][DevtoolsExperimentalFeaturesTurnOn] and select the checkbox next to **Enable support to move tabs between panels**.</span></span>  

<span data-ttu-id="890d9-162">Chrom Problem [#897944][CR897944]</span><span class="sxs-lookup"><span data-stu-id="890d9-162">Chromium issue [#897944][CR897944]</span></span>  

### <span data-ttu-id="890d9-163">Verbesserte QuickInfo des Initiators im Netzwerk Panel</span><span class="sxs-lookup"><span data-stu-id="890d9-163">Improved Initiator tooltip in the Network panel</span></span>  

<span data-ttu-id="890d9-164">In Microsoft Edge 83 und 84 werden QuickInfos für die Initiator-Spalte, die die Ursache der Ressourcenanforderung zeigt, im [Netzwerkprotokoll][DevtoolsNetworkIndexLogActivity] mit einer horizontalen Bildlaufleiste angezeigt.</span><span class="sxs-lookup"><span data-stu-id="890d9-164">In Microsoft Edge 83 and 84, tooltips for the Initiator column, which shows the cause of the resource request, in the [Network Log][DevtoolsNetworkIndexLogActivity] displayed with a horizontal scrollbar.</span></span>  <span data-ttu-id="890d9-165">Sie konnten nur den Aufruf Stapel sehen, der die Anforderung initiiert hat, indem Sie in der QuickInfo horizontal scrollen.</span><span class="sxs-lookup"><span data-stu-id="890d9-165">You were only able to see the call stack that initiated the request by scrolling horizontally in the tooltip.</span></span>  

:::image type="complex" source="../../media/2020/06/initiator-tooltip-84.msft.png" alt-text="Die QuickInfo des Initiators in Microsoft Edge 84" lightbox="../../media/2020/06/initiator-tooltip-84.msft.png":::
   <span data-ttu-id="890d9-167">Die QuickInfo des Initiators in Microsoft Edge 84</span><span class="sxs-lookup"><span data-stu-id="890d9-167">The Initiator tooltip in Microsoft Edge 84</span></span>  
:::image-end:::  

<span data-ttu-id="890d9-168">Ab Microsoft Edge 85 können Sie jetzt den Initiator-Aufruf Stapel in der QuickInfo anzeigen, ohne horizontal scrollen zu müssen.</span><span class="sxs-lookup"><span data-stu-id="890d9-168">Starting with Microsoft Edge 85, you are now able to see the Initiator call stack in the tooltip without scrolling horizontally.</span></span>  

:::image type="complex" source="../../media/2020/06/initiator-tooltip-85.msft.png" alt-text="Die QuickInfo des Initiators in Microsoft Edge 85" lightbox="../../media/2020/06/initiator-tooltip-85.msft.png":::
   <span data-ttu-id="890d9-170">Die QuickInfo des Initiators in Microsoft Edge 85</span><span class="sxs-lookup"><span data-stu-id="890d9-170">The Initiator tooltip in Microsoft Edge 85</span></span>
:::image-end:::  

<span data-ttu-id="890d9-171">Chrom Problem [#1069404][CR1069404]</span><span class="sxs-lookup"><span data-stu-id="890d9-171">Chromium issue [#1069404][CR1069404]</span></span>  

## <span data-ttu-id="890d9-172">Ankündigungen aus dem Chromium-Projekt</span><span class="sxs-lookup"><span data-stu-id="890d9-172">Announcements from the Chromium project</span></span>  

<span data-ttu-id="890d9-173">In den folgenden Abschnitten werden weitere in Microsoft Edge 85 verfügbare Features angekündigt, die zum Open-Source-Projekt Chromium beigetragen haben.</span><span class="sxs-lookup"><span data-stu-id="890d9-173">The following sections announce additional features available in Microsoft Edge 85 that were contributed to the open source Chromium project.</span></span>  

### <span data-ttu-id="890d9-174">Format Bearbeitung für CSS-in-JS-Frameworks</span><span class="sxs-lookup"><span data-stu-id="890d9-174">Style editing for CSS-in-JS frameworks</span></span>  

<span data-ttu-id="890d9-175">Der Bereich " **Formatvorlagen** " bietet nun eine bessere Unterstützung für die Bearbeitung von Formatvorlagen, die mit den [CSSOM-APIs (CSS Object Model)][CsswgDraftsCssom] erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="890d9-175">The **Styles** pane now has better support for editing styles that were created with the [CSS Object Model (CSSOM)][CsswgDraftsCssom] APIs.</span></span>  <span data-ttu-id="890d9-176">Viele CSS-in-JS-Frameworks und-Bibliotheken verwenden die CSSOM-APIs unter der Haube zum Erstellen von Formatvorlagen.</span><span class="sxs-lookup"><span data-stu-id="890d9-176">Many CSS-in-JS frameworks and libraries use the CSSOM APIs under the hood to construct styles.</span></span>  

<span data-ttu-id="890d9-177">Sie können jetzt in JavaScript hinzugefügte Formatvorlagen mithilfe von Konstruktions fähigen [Stylesheets][WicgConstructStylesheet]bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="890d9-177">You are now able to edit styles added in JavaScript using [Constructable Stylesheets][WicgConstructStylesheet].</span></span>  <span data-ttu-id="890d9-178">Konstruktable-Stylesheets sind eine neue Möglichkeit zum Erstellen und Verteilen von wiederverwendbaren Formatvorlagen bei Verwendung des [Schatten-Dom][MdnShadowDom].</span><span class="sxs-lookup"><span data-stu-id="890d9-178">Constructable Stylesheets are a new way to create and distribute reusable styles when using [Shadow DOM][MdnShadowDom].</span></span>  

<span data-ttu-id="890d9-179">Beispielsweise wurden die `h1` mit `CSSStyleSheet` \ (CSSOM-APIs \) hinzugefügten Formatvorlagen zuvor nicht bearbeitet.</span><span class="sxs-lookup"><span data-stu-id="890d9-179">For example, the `h1` styles added with `CSSStyleSheet` \(CSSOM APIs\) were not editable previously.</span></span>  <span data-ttu-id="890d9-180">Die Formatvorlagen können jetzt im Bereich " **Formatvorlagen** " bearbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="890d9-180">The styles are editable now in the **Styles** pane.</span></span>  

:::image type="complex" source="../../media/2020/06/css-in-js.msft.png" alt-text="Ändern der Background-Eigenschaft der H1-Formate, die mit CSSStyleSheet von Pink zu Hellblau hinzugefügt wurden" lightbox="../../media/2020/06/css-in-js.msft.png":::
   <span data-ttu-id="890d9-182">Ändern der `background` Eigenschaft der `h1` mit `CSSStyleSheet` from `pink` to hinzugefügten Formatvorlagen `lightblue`</span><span class="sxs-lookup"><span data-stu-id="890d9-182">Changing the `background` property of the `h1` styles added with `CSSStyleSheet` from `pink` to `lightblue`.</span></span>
:::image-end:::  

<span data-ttu-id="890d9-183">Geben Sie diesem Feature einen Versuch mit einem [Beispiel, in dem CSS-in-JS verwendet wird][CodepenZoherghadyaliAbdgrpz].</span><span class="sxs-lookup"><span data-stu-id="890d9-183">Give this feature a try with a [sample that uses CSS-in-JS][CodepenZoherghadyaliAbdgrpz].</span></span>

<span data-ttu-id="890d9-184">Chrom Problem [#946975][CR946975]</span><span class="sxs-lookup"><span data-stu-id="890d9-184">Chromium issue [#946975][CR946975]</span></span>  

### <span data-ttu-id="890d9-185">Leuchtturm 6 im Leuchtturm-Panel</span><span class="sxs-lookup"><span data-stu-id="890d9-185">Lighthouse 6 in the Lighthouse panel</span></span>  

<span data-ttu-id="890d9-186">Auf dem **Leuchtturm** -Panel läuft nun Lighthouse 6.</span><span class="sxs-lookup"><span data-stu-id="890d9-186">The **Lighthouse** panel is now running Lighthouse 6.</span></span>  <span data-ttu-id="890d9-187">Eine vollständige Liste aller Änderungen finden Sie unter [v 6.0.0-Versionshinweise][GithubGoogleChromeLighthouse600].</span><span class="sxs-lookup"><span data-stu-id="890d9-187">For a full list of all changes, see [v6.0.0 release notes][GithubGoogleChromeLighthouse600].</span></span>  

<span data-ttu-id="890d9-188">Lighthouse 6,0 führt drei neue Metriken in den Bericht ein: größter Content-Paint \ (LCP \), kumulative Layout-UMSCHALT \ (CLS \) und Gesamt Blockierungszeit \ (TBT \).</span><span class="sxs-lookup"><span data-stu-id="890d9-188">Lighthouse 6.0 introduces three new metrics to the report:  Largest Contentful Paint \(LCP\), Cumulative Layout Shift \(CLS\), and Total Blocking Time \(TBT\).</span></span>  

<span data-ttu-id="890d9-189">Die Formel für die Leistungsbewertung wurde ebenfalls umgewichtet, um die Lade Erfahrung des Benutzers besser wiederzugeben.</span><span class="sxs-lookup"><span data-stu-id="890d9-189">The performance score formula has also been reweighted to better reflect the loading experience of the user.</span></span>  

<span data-ttu-id="890d9-190">Chrom Problem [#772558][CR772558]</span><span class="sxs-lookup"><span data-stu-id="890d9-190">Chromium issue [#772558][CR772558]</span></span>  

#### <span data-ttu-id="890d9-191">Erste aussagekräftige Paint-Missbilligung</span><span class="sxs-lookup"><span data-stu-id="890d9-191">First Meaningful Paint deprecation</span></span>  

<span data-ttu-id="890d9-192">Die erste aussagekräftige Farbe \ (Unterstützung \) ist in Lighthouse 6,0 veraltet.</span><span class="sxs-lookup"><span data-stu-id="890d9-192">First Meaningful Paint \(FMP\) is deprecated in Lighthouse 6.0.</span></span>  <span data-ttu-id="890d9-193">In der **Leistungs** Palette wurde auch das Unternehmen entfernt.</span><span class="sxs-lookup"><span data-stu-id="890d9-193">FMP has also been removed from the **Performance** panel.</span></span>  <span data-ttu-id="890d9-194">Der **größte zufriedene Anstrich** ist der empfohlene Ersatz für die Verwendung von "mehr".</span><span class="sxs-lookup"><span data-stu-id="890d9-194">**Largest Contentful Paint** is the recommended replacement for FMP.</span></span>  <!--See [First Meaningful Paint][WebDevFirstMeaningfulPaint] for an explanation of why it was deprecated.  -->  

<!--todo: add Largest Contentful Paint when section available  -->  
<!--todo: add First Meaningful Paint link and note when available  -->  

<span data-ttu-id="890d9-195">Chrom Problem [#1096008][CR1096008]</span><span class="sxs-lookup"><span data-stu-id="890d9-195">Chromium issue [#1096008][CR1096008]</span></span>  

### <span data-ttu-id="890d9-196">Unterstützung für neue JavaScript-Features</span><span class="sxs-lookup"><span data-stu-id="890d9-196">Support for new JavaScript features</span></span>  

<span data-ttu-id="890d9-197">DevTools bietet nun eine bessere Unterstützung für einige der neuesten JavaScript-Sprachfeatures.</span><span class="sxs-lookup"><span data-stu-id="890d9-197">DevTools now has better support for some of the latest JavaScript language features.</span></span>  

:::row:::
   :::column span="1":::
      <span data-ttu-id="890d9-198">[Optionale Verkettungs][V8DevOptionalChaining] Syntax Autovervollständigung</span><span class="sxs-lookup"><span data-stu-id="890d9-198">[Optional chaining][V8DevOptionalChaining] syntax autocompletion</span></span>  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="890d9-199">Die automatische Vervollständigung von Eigenschaften in der **Konsole** unterstützt jetzt optionale Verkettungs Syntax, beispielsweise `name?.` jetzt zusätzlich zu `name.` und `name[` .</span><span class="sxs-lookup"><span data-stu-id="890d9-199">Property auto-completion in the **Console** now supports optional chaining syntax, for example,  `name?.` now works in addition to `name.` and `name[`.</span></span>  
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="1":::
      <span data-ttu-id="890d9-200">Syntax Hervorhebung für [private Felder][V8DevClassFieldsPrivate]</span><span class="sxs-lookup"><span data-stu-id="890d9-200">Syntax highlighting for [private fields][V8DevClassFieldsPrivate]</span></span>  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="890d9-201">Private Kurs Felder werden jetzt ordnungsgemäß in der Syntax hervorgehoben und im **Quellen** Panel hübsch gedruckt.</span><span class="sxs-lookup"><span data-stu-id="890d9-201">private class fields are now properly syntax-highlighted and pretty-printed in the **Sources** panel.</span></span>  
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="1":::
      <span data-ttu-id="890d9-202">Syntax Hervorhebung für [ungültigen][V8DevNullishCoalescing] Vereinigungsoperator</span><span class="sxs-lookup"><span data-stu-id="890d9-202">Syntax highlighting for [Nullish coalescing operator][V8DevNullishCoalescing]</span></span>
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="890d9-203">DevTools nun richtig hübsch – druckt den ungültigen Vereinigungsoperator im **Quellen** Panel.</span><span class="sxs-lookup"><span data-stu-id="890d9-203">DevTools now properly pretty-prints the nullish coalescing operator in the **Sources** panel.</span></span>  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="890d9-204">Chrom Probleme [#1073903][CR1073903], [#1083214][CR1083214], [#1083797][CR1083797]</span><span class="sxs-lookup"><span data-stu-id="890d9-204">Chromium issues [#1073903][CR1073903], [#1083214][CR1083214], [#1083797][CR1083797]</span></span>  

### <span data-ttu-id="890d9-205">Neue APP-Verknüpfungs Warnungen im Bereich "Manifest"</span><span class="sxs-lookup"><span data-stu-id="890d9-205">New app shortcut warnings in the Manifest pane</span></span>  

<span data-ttu-id="890d9-206">**App-Tastenkombinationen** helfen Benutzern, häufige oder empfohlene Aufgaben in einer Web-App schnell zu starten.</span><span class="sxs-lookup"><span data-stu-id="890d9-206">**App shortcuts** help users quickly start common or recommended tasks within a web app.</span></span>  

<!--todo: add App shortcuts when section is live  -->  

<span data-ttu-id="890d9-207">Der Bereich **Manifest** zeigt nun Warnungen für die folgenden Bedingungen an.</span><span class="sxs-lookup"><span data-stu-id="890d9-207">The **Manifest** pane now shows warnings for the following conditions.</span></span>  

* <span data-ttu-id="890d9-208">Die APP-Verknüpfungssymbole sind kleiner als 96x96 Pixel</span><span class="sxs-lookup"><span data-stu-id="890d9-208">The app shortcut icons are smaller than 96x96 pixels</span></span>  
* <span data-ttu-id="890d9-209">Die APP-Verknüpfungssymbole und Manifest-Symbole sind nicht quadratisch \ (da die Symbole ignoriert werden \)</span><span class="sxs-lookup"><span data-stu-id="890d9-209">The app shortcut icons and manifest icons are not square \(since the icons are ignored\)</span></span>  

:::image type="complex" source="../../media/2020/06/app-shortcut-warnings.msft.png" alt-text="App-Verknüpfungs Warnungen" lightbox="../../media/2020/06/app-shortcut-warnings.msft.png":::
   <span data-ttu-id="890d9-211">App-Verknüpfungs Warnungen</span><span class="sxs-lookup"><span data-stu-id="890d9-211">App shortcut warnings</span></span>  
:::image-end:::  

<span data-ttu-id="890d9-212">Chrom Problem [#955497][CR955497]</span><span class="sxs-lookup"><span data-stu-id="890d9-212">Chromium issue [#955497][CR955497]</span></span>  

### <span data-ttu-id="890d9-213">Konsistente Anzeige des berechneten Bereichs</span><span class="sxs-lookup"><span data-stu-id="890d9-213">Consistent display of the Computed pane</span></span>  

<span data-ttu-id="890d9-214">Der **berechnete** Bereich im **Element** Bereich wird nun einheitlich als Bereich für alle Ansichtsfenster Größen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="890d9-214">The **Computed** pane in the **Elements** panel now displays consistently as a pane across all viewport sizes.</span></span>  <span data-ttu-id="890d9-215">Zuvor wurde der **berechnete** Bereich im Bereich " **Formatvorlagen** " zusammengeführt, wenn die Breite des devtools-Viewports schmal war.</span><span class="sxs-lookup"><span data-stu-id="890d9-215">Previously the **Computed** pane merged inside the **Styles** pane when the width of the DevTools viewport was narrow.</span></span>  

:::image type="complex" source="../../media/2020/06/computed-pane.msft.png" alt-text="Der berechnete Bereich wird konsistent als separater Bereich angezeigt, auch wenn die devtools schmal sind." lightbox="../../media/2020/06/computed-pane.msft.png":::
   <span data-ttu-id="890d9-217">Der **berechnete** Bereich wird konsistent als separater Bereich angezeigt, auch wenn die devtools schmal sind.</span><span class="sxs-lookup"><span data-stu-id="890d9-217">The **Computed** pane consistently displays as a separate pane even when the DevTools are narrow.</span></span>
:::image-end:::  

<span data-ttu-id="890d9-218">Chrom Problem [#1073899][CR1073899]</span><span class="sxs-lookup"><span data-stu-id="890d9-218">Chromium issue [#1073899][CR1073899]</span></span>  

### <span data-ttu-id="890d9-219">Bytecode-Offsets für webassemblydateien</span><span class="sxs-lookup"><span data-stu-id="890d9-219">Bytecode offsets for WebAssembly files</span></span>  

<span data-ttu-id="890d9-220">DevTools verwendet jetzt Bytecode-Offsets zum Anzeigen von WASM-Disassembly-Nummern.</span><span class="sxs-lookup"><span data-stu-id="890d9-220">DevTools now uses bytecode offsets for displaying line numbers of Wasm disassembly.</span></span>  
<span data-ttu-id="890d9-221">Durch die Zahlen in der Zeile wird deutlicher, dass Sie Binärdaten suchen, und es ist konsistenter, wie die WASM-Laufzeit auf Speicherorte verweist.</span><span class="sxs-lookup"><span data-stu-id="890d9-221">The line numbers make it clearer that you are looking at binary data, and is more consistent with how the Wasm runtime references locations.</span></span>  

<span data-ttu-id="890d9-222">Chrom Problem [#1071432][CR1071432]</span><span class="sxs-lookup"><span data-stu-id="890d9-222">Chromium issue [#1071432][CR1071432]</span></span>  

### <span data-ttu-id="890d9-223">Kopieren und Ausschneiden der Zeile im Quellen Panel</span><span class="sxs-lookup"><span data-stu-id="890d9-223">Line-wise copy and cut in Sources Panel</span></span>  

<span data-ttu-id="890d9-224">Beim Ausführen von kopieren oder Ausschneiden ohne Auswahl im [Quellcode-Panel-Editor][DevtoolsSourcesEditCssJavascript]kopiert devtools die aktuelle Inhaltszeile oder schneidet sie aus.</span><span class="sxs-lookup"><span data-stu-id="890d9-224">When performing copy or cut with no selection in the [Sources panel editor][DevtoolsSourcesEditCssJavascript], DevTools copies or cuts the current line of content.</span></span>  

:::image type="complex" source="../../media/2020/06/line-wise-cut.msft.png" alt-text="Mit dem Cursor am Ende der Zeile 5, Kopieren der gesamten Zeile aus pen.js im devtools und Einfügen in vs-Code" lightbox="../../media/2020/06/line-wise-cut.msft.png":::
   <span data-ttu-id="890d9-226">Mit dem Cursor am Ende der Zeile 5, kopieren Sie die gesamte Zeile aus **pen.js** im devtools, und fügen Sie Sie in [vs-Code][VSCode]ein.</span><span class="sxs-lookup"><span data-stu-id="890d9-226">With the cursor at the end of Line 5, copying the whole line from **pen.js** in the DevTools and pasting in [VS Code][VSCode].</span></span>
:::image-end:::  

<span data-ttu-id="890d9-227">Chrom Problem [#800028][CR800028]</span><span class="sxs-lookup"><span data-stu-id="890d9-227">Chromium issue [#800028][CR800028]</span></span>

### <span data-ttu-id="890d9-228">Updates für Konsoleneinstellungen</span><span class="sxs-lookup"><span data-stu-id="890d9-228">Console Settings updates</span></span>  

#### <span data-ttu-id="890d9-229">Aufheben der Gruppierung derselben Konsolen Nachrichten</span><span class="sxs-lookup"><span data-stu-id="890d9-229">Ungroup same console messages</span></span>  

<span data-ttu-id="890d9-230">Die **Gruppe ähnliche** Umschalter in den Konsoleneinstellungen gilt jetzt für doppelte Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="890d9-230">The **Group similar** toggle in Console Settings now applies to duplicate messages.</span></span>  <span data-ttu-id="890d9-231">Zuvor hat es gerade auf ähnliche Nachrichten angewendet.</span><span class="sxs-lookup"><span data-stu-id="890d9-231">Previously it just applied to similar messages.</span></span>  

<span data-ttu-id="890d9-232">Zuvor hat devtools die Gruppierung der Nachrichten nicht aufheben, obwohl `hello` **Gruppe ähnlich** deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="890d9-232">For example, previously, DevTools did not ungroup the `hello` messages even though **Group similar** is unchecked.</span></span>  <span data-ttu-id="890d9-233">Nun werden die `hello` Nachrichten nicht gruppiert.</span><span class="sxs-lookup"><span data-stu-id="890d9-233">Now, the `hello` messages are ungrouped.</span></span>  

:::image type="complex" source="../../media/2020/06/ungroup-similar.msft.png" alt-text="Wenn Gruppe ähnlich deaktiviert ist, werden die Hello-Nachrichten nicht gruppiert" lightbox="../../media/2020/06/ungroup-similar.msft.png":::
   <span data-ttu-id="890d9-235">Wenn **Gruppe ähnlich** deaktiviert ist, `hello` werden die Nachrichten nicht gruppiert.</span><span class="sxs-lookup"><span data-stu-id="890d9-235">When **Group similar** is unchecked, the `hello` messages are ungrouped.</span></span>
:::image-end:::  

<span data-ttu-id="890d9-236">Geben Sie diesem Feature einen Versuch mit einem [Beispiel, mit dem doppelte Nachrichten an die Konsole gesendet werden][CodepenZoherghadyaliZyrjgdJ].</span><span class="sxs-lookup"><span data-stu-id="890d9-236">Give this feature a try with a [sample that sends duplicate messages to the Console][CodepenZoherghadyaliZyrjgdJ].</span></span>  

<span data-ttu-id="890d9-237">Chrom Problem [#1082963][CR1082963]</span><span class="sxs-lookup"><span data-stu-id="890d9-237">Chromium issue [#1082963][CR1082963]</span></span>  

### <span data-ttu-id="890d9-238">Nur ausgewählte Kontext Einstellungen beibehalten</span><span class="sxs-lookup"><span data-stu-id="890d9-238">Persisting Selected context only settings</span></span>  

<span data-ttu-id="890d9-239">Die Einstellungen für den **ausgewählten Kontext nur** in den Konsoleneinstellungen werden nun beibehalten.</span><span class="sxs-lookup"><span data-stu-id="890d9-239">The **Selected context only** settings in Console Settings is now persisted.</span></span>  <span data-ttu-id="890d9-240">Zuvor wurden die Einstellungen jedes Mal zurückgesetzt, wenn Sie devtools geschlossen und wieder geöffnet haben.</span><span class="sxs-lookup"><span data-stu-id="890d9-240">Previously the settings were reset every time you closed and reopened DevTools.</span></span>  <span data-ttu-id="890d9-241">Durch die Änderung wird das Einstellungsverhalten mit anderen Optionen für Konsoleneinstellungen konsistent.</span><span class="sxs-lookup"><span data-stu-id="890d9-241">The change makes the setting behavior consistent with other Console Settings options.</span></span>  

:::image type="complex" source="../../media/2020/06/selected-context.msft.png" alt-text="Nur ausgewählte Kontext Einstellung" lightbox="../../media/2020/06/selected-context.msft.png":::
   <span data-ttu-id="890d9-243">**Nur ausgewählte Kontext** Einstellung</span><span class="sxs-lookup"><span data-stu-id="890d9-243">**Selected context only** setting</span></span>  
:::image-end:::  

<span data-ttu-id="890d9-244">Chrom Problem [#1055875][CR1055875]</span><span class="sxs-lookup"><span data-stu-id="890d9-244">Chromium issue [#1055875][CR1055875]</span></span>  

### <span data-ttu-id="890d9-245">Updates für das Leistungs Panel</span><span class="sxs-lookup"><span data-stu-id="890d9-245">Performance panel updates</span></span>  

#### <span data-ttu-id="890d9-246">Informationen zum Cache für JavaScript-Kompilierung im Leistungs Panel</span><span class="sxs-lookup"><span data-stu-id="890d9-246">JavaScript compilation cache information in Performance panel</span></span>  

<span data-ttu-id="890d9-247">Die [Informationen im JavaScript-Kompilierungs Cache][V8DevCodeCaching] werden jetzt immer auf der Registerkarte "Zusammenfassung" im Leistungsfenster angezeigt.</span><span class="sxs-lookup"><span data-stu-id="890d9-247">[JavaScript compilation cache information][V8DevCodeCaching] is now always displayed in the Summary tab of the Performance panel.</span></span>  <span data-ttu-id="890d9-248">Zuvor zeigten devtools nichts im Zusammenhang mit der Code Zwischenspeicherung an, wenn die Code Zwischenspeicherung nicht statt fand.</span><span class="sxs-lookup"><span data-stu-id="890d9-248">Previously, DevTools did not show anything related to code caching if code caching did not happen.</span></span>  

:::image type="complex" source="../../media/2020/06/js-compilation-cache.msft.png" alt-text="Informationen zum Cache für JavaScript-Kompilierung" lightbox="../../media/2020/06/js-compilation-cache.msft.png":::
   <span data-ttu-id="890d9-250">Informationen zum Cache für JavaScript-Kompilierung</span><span class="sxs-lookup"><span data-stu-id="890d9-250">JavaScript compilation cache information</span></span>  
:::image-end:::  

<span data-ttu-id="890d9-251">Chrom Problem [#912581][CR912581]</span><span class="sxs-lookup"><span data-stu-id="890d9-251">Chromium issue [#912581][CR912581]</span></span>  

#### <span data-ttu-id="890d9-252">Ausrichtung der Navigationsanzeige im Leistungsbereich</span><span class="sxs-lookup"><span data-stu-id="890d9-252">Navigation timing alignment in the Performance panel</span></span>  

<span data-ttu-id="890d9-253">Im **Leistungs** Panel werden die Zeiten in den Linealen basierend auf dem Beginn der Aufzeichnung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="890d9-253">The **Performance** panel used to show times in the rulers based on when the recording started.</span></span>  <span data-ttu-id="890d9-254">Die Anzeigedauer wurde für Aufzeichnungen geändert, in denen der Benutzer navigiert, wobei in devtools nun stattdessen die linealzeiten relativ zur Navigation angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="890d9-254">The timing has now changed for recordings where the user navigates, where DevTools now shows ruler times relative to the navigation instead.</span></span>  

:::image type="complex" source="../../media/2020/06/nav-timing.msft.png" alt-text="Ausrichten der Navigationsanzeige im Leistungsbereich" lightbox="../../media/2020/06/nav-timing.msft.png":::
   <span data-ttu-id="890d9-256">Ausrichten der Navigationsanzeige im **Leistungs** Bereich</span><span class="sxs-lookup"><span data-stu-id="890d9-256">Align navigation timing in **Performance** panel</span></span>  
:::image-end:::  

<span data-ttu-id="890d9-257">Die Zeiten für `DOMContentLoaded` , erster Anstrich, erster Inhaltsbezogener Paint und die größten inhaltsabhängigen Paint-Ereignisse werden relativ zum Anfang der Navigation aktualisiert, was bedeutet, dass die Anzeigedauer den angegebenen Anzeigedauern entspricht `PerformanceObserver` .</span><span class="sxs-lookup"><span data-stu-id="890d9-257">The times for `DOMContentLoaded`, First Paint, First Contentful Paint, and Largest Contentful Paint events are updated to be relative to the start of the navigation, which means the timing matches the timings reported by `PerformanceObserver`.</span></span>  

<span data-ttu-id="890d9-258">Chrom Problem [#974550][CR974550]</span><span class="sxs-lookup"><span data-stu-id="890d9-258">Chromium issue [#974550][CR974550]</span></span>  

### <span data-ttu-id="890d9-259">Neue Symbole für Haltepunkte, bedingte Haltepunkte und logpoints</span><span class="sxs-lookup"><span data-stu-id="890d9-259">New icons for breakpoints, conditional breakpoints, and logpoints</span></span>  

<span data-ttu-id="890d9-260">Das **Quellen** Panel enthält neue Designs für Haltepunkte, bedingte Haltepunkte und logpoints.</span><span class="sxs-lookup"><span data-stu-id="890d9-260">The **Sources** panel has new designs for breakpoints, conditional breakpoints, and logpoints.</span></span>  <span data-ttu-id="890d9-261">Haltepunkte werden durch einen roten Kreis dargestellt, genau wie [vs-Code][VSCode] und [Visual Studio][VS].</span><span class="sxs-lookup"><span data-stu-id="890d9-261">Breakpoints are represented by a red circle, just like [VS Code][VSCode] and [Visual Studio][VS].</span></span>  <span data-ttu-id="890d9-262">Symbole werden hinzugefügt, um bedingte Haltepunkte und logpoints zu unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="890d9-262">Icons are added to differentiate conditional breakpoints and logpoints.</span></span>  

:::image type="complex" source="../../media/2020/06/breakpoints.msft.png" alt-text="Breakpoints" lightbox="../../media/2020/06/breakpoints.msft.png":::
   <span data-ttu-id="890d9-264">Breakpoints</span><span class="sxs-lookup"><span data-stu-id="890d9-264">Breakpoints</span></span>  
:::image-end:::  

<span data-ttu-id="890d9-265">Chrom Problem [#1041830][CR1041830]</span><span class="sxs-lookup"><span data-stu-id="890d9-265">Chromium issue [#1041830][CR1041830]</span></span>  

## <span data-ttu-id="890d9-266">Herunterladen der Microsoft Edge Preview-Kanäle</span><span class="sxs-lookup"><span data-stu-id="890d9-266">Download the Microsoft Edge preview channels</span></span>  

<span data-ttu-id="890d9-267">Wenn Sie unter Windows oder macOS arbeiten, sollten Sie die [Microsoft Edge Preview-Kanäle][MicrosoftEdgePreviewChannels] als Standard Entwicklungsbrowser verwenden.</span><span class="sxs-lookup"><span data-stu-id="890d9-267">If you are on Windows or macOS, consider using the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] as your default development browser.</span></span>  <span data-ttu-id="890d9-268">Über die Vorschau Kanäle erhalten Sie Zugriff auf die neuesten devtools-Funktionen.</span><span class="sxs-lookup"><span data-stu-id="890d9-268">The preview channels give you access to the latest DevTools features.</span></span>  

## <span data-ttu-id="890d9-269">Kontakt mit dem Microsoft Edge devtools-Team</span><span class="sxs-lookup"><span data-stu-id="890d9-269">Getting in touch with Microsoft Edge DevTools team</span></span>  

<span data-ttu-id="890d9-270">Verwenden Sie die folgenden Optionen, um die neuen Features und Änderungen im Beitrag zu besprechen, oder alles, was mit devtools zu tun hat.</span><span class="sxs-lookup"><span data-stu-id="890d9-270">Use the following options to discuss the new features and changes in the post, or anything else related to DevTools.</span></span>  

* <span data-ttu-id="890d9-271">Senden Sie Ihr Feedback über das **Feedback** -Symbol im devtools</span><span class="sxs-lookup"><span data-stu-id="890d9-271">Send your feedback using the **Feedback** icon in the DevTools</span></span>  
* <span data-ttu-id="890d9-272">Tweet bei [@EdgeDevTools][PostTweetEdgeDevTools]</span><span class="sxs-lookup"><span data-stu-id="890d9-272">Tweet at [@EdgeDevTools][PostTweetEdgeDevTools]</span></span>  
* <span data-ttu-id="890d9-273">Einen Vorschlag an [das gewünschte Web][TheWebWeWant] senden</span><span class="sxs-lookup"><span data-stu-id="890d9-273">Submit a suggestion to [The Web We Want][TheWebWeWant]</span></span>  
* <span data-ttu-id="890d9-274">Datei Fehler auf dieser Seite im [Edge-Entwickler-][GitHubMicrosoftDocsEdgeDeveloperNewIssue] Repository</span><span class="sxs-lookup"><span data-stu-id="890d9-274">File bugs on this page in the [edge-developer][GitHubMicrosoftDocsEdgeDeveloperNewIssue] repository</span></span>  

:::image type="complex" source="../../media/2020/05/feedback-icon.msft.png" alt-text="Das Feedback Symbol in der Microsoft Edge-devtools" lightbox="../../media/2020/05/feedback-icon.msft.png":::
  <span data-ttu-id="890d9-276">Das **Feedback** Symbol in der Microsoft Edge-devtools</span><span class="sxs-lookup"><span data-stu-id="890d9-276">The **Feedback** icon in the Microsoft Edge DevTools</span></span>  
:::image-end:::  

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
> <span data-ttu-id="890d9-325">Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="890d9-325">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="890d9-326">Die ursprüngliche Seite wird [hier](https://developers.google.com/web/updates/2020/06/devtools/index) gefunden und von [Jecelyn Yeen][JecelynYeen] \ (Developer Advocate, Chrome devtools \) erstellt.</span><span class="sxs-lookup"><span data-stu-id="890d9-326">The original page is found [here](https://developers.google.com/web/updates/2020/06/devtools/index) and is authored by [Jecelyn Yeen][JecelynYeen] \(Developer advocate, Chrome DevTools\).</span></span>  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
<span data-ttu-id="890d9-328">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="890d9-328">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[JecelynYeen]: https://developers.google.com/web/resources/contributors/jecelynyeen  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
