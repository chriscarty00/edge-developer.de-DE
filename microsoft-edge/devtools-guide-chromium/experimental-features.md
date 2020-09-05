---
description: Die neuesten experimentellen Features in Microsoft Edge devtools
title: Experimentelle Funktionen
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/25/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Web-Entwicklung, F12-Tools, devtools, Experiment
ms.openlocfilehash: a5793b6f4b67add313958ad4b8cee01cb7b09dbf
ms.sourcegitcommit: 7e3644e6b1d568ab795168e421c013814efa0073
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/04/2020
ms.locfileid: "10996159"
---
# <span data-ttu-id="6c319-104">Experimentelle Funktionen</span><span class="sxs-lookup"><span data-stu-id="6c319-104">Experimental features</span></span>  

<span data-ttu-id="6c319-105">Sie können die experimentellen Features, die noch in der Entwicklung sind, in der Microsoft Edge-devtools verwenden, um zu testen und [Feedback bereitzustellen](#providing-feedback-on-experimental-features) , bevor diese im allgemeinen veröffentlicht werden.</span><span class="sxs-lookup"><span data-stu-id="6c319-105">You may use the experimental features that are still under development in the Microsoft Edge DevTools to test and [provide feedback](#providing-feedback-on-experimental-features) before each is released broadly.</span></span>  

<span data-ttu-id="6c319-106">Während experimentelle Features in allen Kanälen von Microsoft Edge verfügbar sind, erhalten Sie möglicherweise die neuesten experimentellen Features mithilfe des Canary-Kanals von Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="6c319-106">While experimental features are available in all channels of Microsoft Edge, you may get the latest experimental features using the Microsoft Edge Canary channel.</span></span>  

## <span data-ttu-id="6c319-107">Aktivieren von experimentellen Features</span><span class="sxs-lookup"><span data-stu-id="6c319-107">Turn on experimental features</span></span>  

<span data-ttu-id="6c319-108">Führen Sie die folgenden Schritte aus, um die experimentellen Features von \ (oder Off \) in Microsoft Edge zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="6c319-108">Use the following steps to turn on \(or off\) experimental features in Microsoft Edge.</span></span>  

1.  <span data-ttu-id="6c319-109">[Öffnen Sie devtools][DevtoolsOpen].</span><span class="sxs-lookup"><span data-stu-id="6c319-109">[Open DevTools][DevtoolsOpen].</span></span>  
     *   <span data-ttu-id="6c319-110">Wählen Sie `Control` + `Shift` + `I` \ (Windows \) oder `Command` + `Option` + `I` \ (macOS \) aus.</span><span class="sxs-lookup"><span data-stu-id="6c319-110">Select `Control`+`Shift`+`I` \(Windows\) or `Command`+`Option`+`I` \(macOS\).</span></span>  <span data-ttu-id="6c319-111">Weitere Informationen finden Sie unter [Tastenkombinationen für Microsoft Edge devtools][DevToolsShortcuts].</span><span class="sxs-lookup"><span data-stu-id="6c319-111">For more information, see [Microsoft Edge DevTools keyboard shortcuts][DevToolsShortcuts].</span></span>  
1.  <span data-ttu-id="6c319-112">Öffnen Sie den Bereich " [Einstellungen][DevToolsCustomizeSettings] ".</span><span class="sxs-lookup"><span data-stu-id="6c319-112">Open the [Settings][DevToolsCustomizeSettings] pane.</span></span>  
    *   <span data-ttu-id="6c319-113">Wählen Sie aus `Shift` + `?` .</span><span class="sxs-lookup"><span data-stu-id="6c319-113">Select `Shift`+`?`.</span></span>  <span data-ttu-id="6c319-114">Weitere Informationen finden Sie unter [Tastenkombinationen für Microsoft Edge devtools][DevToolsShortcuts].</span><span class="sxs-lookup"><span data-stu-id="6c319-114">For more information, see [Microsoft Edge DevTools keyboard shortcuts][DevToolsShortcuts].</span></span>  
1.  <span data-ttu-id="6c319-115">Wählen Sie auf der linken Seite des Bereichs **Einstellungen** den Abschnitt **Experimente** aus.</span><span class="sxs-lookup"><span data-stu-id="6c319-115">On the left side of the **Settings** pane, select the **Experiments** section.</span></span>  
    
    :::image type="complex" source="./media/experiments-devtools.png" alt-text="Liste der Experimente in den devtools-Einstellungen" lightbox="./media/experiments-devtools.png":::
       <span data-ttu-id="6c319-117">Liste der Experimente in den devtools-Einstellungen</span><span class="sxs-lookup"><span data-stu-id="6c319-117">List of experiments in DevTools Settings</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="6c319-118">Scrollen Sie auf der Seite **Experimente** durch die Liste aller verfügbaren experimentellen Features, und aktivieren Sie das Kontrollkästchen neben den einzelnen Features, die Sie testen möchten.</span><span class="sxs-lookup"><span data-stu-id="6c319-118">On the **Experiments** page, scroll through the list of all available experimental features and select the checkbox next to each features that you want to test.</span></span>  
1.  <span data-ttu-id="6c319-119">Schließen Sie die Microsoft Edge-devtools, und öffnen Sie Sie erneut.</span><span class="sxs-lookup"><span data-stu-id="6c319-119">Close and reopen Microsoft Edge DevTools.</span></span>  

> [!NOTE]
> <span data-ttu-id="6c319-120">Experimentelle Features werden ständig aktualisiert, was zu Leistungsproblemen führen kann.</span><span class="sxs-lookup"><span data-stu-id="6c319-120">Experimental features are constantly being updated and may cause performance issues.</span></span>  <span data-ttu-id="6c319-121">Wenn Sie ein experimentelles Feature deaktivieren möchten, öffnen Sie die Seite **Experimente** , und deaktivieren Sie das Kontrollkästchen des experimentellen Features, das Sie deaktivieren möchten.</span><span class="sxs-lookup"><span data-stu-id="6c319-121">To turn off an experimental feature, open the **Experiments** page and clear the checkbox of the experimental feature that you want to turn off.</span></span>  

## <span data-ttu-id="6c319-122">Hervorgehobene experimentelle Features</span><span class="sxs-lookup"><span data-stu-id="6c319-122">Highlighted experimental features</span></span>  

<span data-ttu-id="6c319-123">In den folgenden Abschnitten werden die neuen experimentellen Features beschrieben, die in Microsoft Edge zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="6c319-123">The following sections describe the new experimental features that are available in Microsoft Edge.</span></span>  

| <span data-ttu-id="6c319-124">Experimentelle Funktion</span><span class="sxs-lookup"><span data-stu-id="6c319-124">Experimental feature</span></span> | <span data-ttu-id="6c319-125">Microsoft Edge-Version</span><span class="sxs-lookup"><span data-stu-id="6c319-125">Microsoft Edge version</span></span> |  
|:--- |:--- |  
| [<span data-ttu-id="6c319-126">Debuggen von neuen CSS-Raster Features aktivieren</span><span class="sxs-lookup"><span data-stu-id="6c319-126">Enable new CSS grid debugging features</span></span>](#enable-new-css-grid-debugging-features) | <span data-ttu-id="6c319-127">85 oder höher</span><span class="sxs-lookup"><span data-stu-id="6c319-127">85 or later</span></span> |  
| [<span data-ttu-id="6c319-128">Aktivieren der Unterstützung für das Verschieben von Tabstopps zwischen Bereichen</span><span class="sxs-lookup"><span data-stu-id="6c319-128">Enable support to move tabs between panels</span></span>](#enable-support-to-move-tabs-between-panels) | <span data-ttu-id="6c319-129">85 oder höher</span><span class="sxs-lookup"><span data-stu-id="6c319-129">85 or later</span></span> |  
| [<span data-ttu-id="6c319-130">Webhint aktivieren</span><span class="sxs-lookup"><span data-stu-id="6c319-130">Enable webhint</span></span>](#enable-webhint) | <span data-ttu-id="6c319-131">85 oder höher</span><span class="sxs-lookup"><span data-stu-id="6c319-131">85 or later</span></span> |  
| [<span data-ttu-id="6c319-132">Aktivieren der Netzwerk Konsole</span><span class="sxs-lookup"><span data-stu-id="6c319-132">Enable Network Console</span></span>](#enable-network-console) | <span data-ttu-id="6c319-133">85 oder höher</span><span class="sxs-lookup"><span data-stu-id="6c319-133">85 or later</span></span> |  
| [<span data-ttu-id="6c319-134">Quellauftrags Anzeige aktivieren</span><span class="sxs-lookup"><span data-stu-id="6c319-134">Enable Source Order Viewer</span></span>](#enable-source-order-viewer) | <span data-ttu-id="6c319-135">86 oder höher</span><span class="sxs-lookup"><span data-stu-id="6c319-135">86 or later</span></span> |  

### <span data-ttu-id="6c319-136">Debuggen von neuen CSS-Raster Features aktivieren</span><span class="sxs-lookup"><span data-stu-id="6c319-136">Enable new CSS grid debugging features</span></span>  

<span data-ttu-id="6c319-137">Verbessert die on-page-Visualisierungen, wenn Sie Websites mit CSS-Rasterlayouts Debuggen.</span><span class="sxs-lookup"><span data-stu-id="6c319-137">Improves on-page visualizations when you debug websites that have CSS grid layouts.</span></span>  <span data-ttu-id="6c319-138">Sie können die Overlays in den devtools-Einstellungen weiter anpassen.</span><span class="sxs-lookup"><span data-stu-id="6c319-138">You may further customize the overlays in DevTools Settings.</span></span>  

:::image type="complex" source="./media/experiments-grid.png" alt-text="CSS-Raster Debugging-Feature" lightbox="./media/experiments-grid.png":::
   <span data-ttu-id="6c319-140">CSS-Raster Debugging-Feature</span><span class="sxs-lookup"><span data-stu-id="6c319-140">CSS grid debugging feature</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 85 and later.  -->  

### <span data-ttu-id="6c319-141">Aktivieren der Unterstützung für das Verschieben von Tabstopps zwischen Bereichen</span><span class="sxs-lookup"><span data-stu-id="6c319-141">Enable support to move tabs between panels</span></span>  

<span data-ttu-id="6c319-142">In der Regel können Tools, wie **Elemente** und **Netzwerke** , nur im Hauptbereich \ (oben \) von devtools geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="6c319-142">Normally, tools such as **Elements** and **Network** may only be opened in the main \(top\) panel of DevTools.</span></span>  <span data-ttu-id="6c319-143">Auf ähnliche Weise können Tools wie **3D-Ansicht** und **Probleme** nur im Bereich "drawer \ (unten \)" von devtools geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="6c319-143">Similarly, tools such as **3D View** and **Issues** may only be opened in the drawer \(bottom\) panel of DevTools.</span></span>  <span data-ttu-id="6c319-144">Wenn Sie das Experiment auswählen, können Sie die Tools zwischen dem oberen und unteren Bereich verschieben, indem Sie auf die Registerkarte zeigen, das Kontextmenü öffnen (Klicken Sie mit der rechten Maustaste auf \), und wählen Sie **nach oben** oder **nach unten**verschieben aus.</span><span class="sxs-lookup"><span data-stu-id="6c319-144">When you choose the experiment, you may move tools between the top and bottom panels by hovering on the tab, opening the contextual menu \(right-click\), and choose **Move to top** or **Move to bottom**.</span></span>   <span data-ttu-id="6c319-145">Mit diesem Experiment können Sie Ihr devtools-Layout anpassen.</span><span class="sxs-lookup"><span data-stu-id="6c319-145">This experiment allows you to customize your DevTools layout.</span></span>  <span data-ttu-id="6c319-146">Wenn Sie den unteren Bereich ein-oder ausblenden möchten, wählen Sie aus `Escape` .</span><span class="sxs-lookup"><span data-stu-id="6c319-146">To show or hide the bottom panel, select `Escape`.</span></span>  

:::image type="complex" source="./media/experiments-move-panels.png" alt-text="Verschieben von Tabstopps zwischen Bereichen" lightbox="./media/experiments-move-panels.png":::
   <span data-ttu-id="6c319-148">Verschieben von Tabstopps zwischen Bereichen</span><span class="sxs-lookup"><span data-stu-id="6c319-148">Moving tabs between panels</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 85 and later.  -->  

### <span data-ttu-id="6c319-149">Webhint aktivieren</span><span class="sxs-lookup"><span data-stu-id="6c319-149">Enable webhint</span></span>  

<span data-ttu-id="6c319-150">[webhint][WebhintMain] ist ein Open-Source-Tool, das in Echtzeit Feedback zur Barrierefreiheit, browserübergreifenden Kompatibilität, Sicherheit, Leistung, PWAs und anderen gängigen Webentwicklungs Problemen von Websites bietet.</span><span class="sxs-lookup"><span data-stu-id="6c319-150">[webhint][WebhintMain] is an open-source tool that provides real-time feedback on the accessibility, cross-browser compatibility, security, performance, PWAs, and other common web development issues of websites.</span></span>  <span data-ttu-id="6c319-151">Das [webhint-Experiment führt][WebhintMain] das webhint-Feedback in devtools im Bereich [Probleme][DevtoolsIssues] .</span><span class="sxs-lookup"><span data-stu-id="6c319-151">The [webhint][WebhintMain] experiment brings the webhint feedback into DevTools in the [Issues][DevtoolsIssues] panel.</span></span>  <span data-ttu-id="6c319-152">Sie können das Problem auswählen, um die Dokumentation zur Behebung des Problems und eine Liste der betroffenen Ressourcen auf Ihrer Website anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="6c319-152">You may select the issue to see documentation on how to fix the issue and a list of the affected resources on your website.</span></span>  <span data-ttu-id="6c319-153">Wählen Sie einen Ressourcen Link aus, um den entsprechenden Bereich für **Netzwerke**, **Quellen**oder **Elemente** in devtools zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="6c319-153">Select a resource link to open the relevant **Network**, **Sources**, or **Elements** pane in DevTools.</span></span>  

:::image type="complex" source="./media/experiments-webhint.png" alt-text="webhint-Feedback im Bereich "Probleme"" lightbox="./media/experiments-webhint.png":::
   <span data-ttu-id="6c319-155">webhint-Feedback im Bereich " **Probleme** "</span><span class="sxs-lookup"><span data-stu-id="6c319-155">webhint feedback in the **Issues** panel</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 85 and later.  -->  

### <span data-ttu-id="6c319-156">Aktivieren der Netzwerk Konsole</span><span class="sxs-lookup"><span data-stu-id="6c319-156">Enable Network Console</span></span>  

<span data-ttu-id="6c319-157">**Netzwerk Konsole** ist der Arbeitstitel eines Experiments, um synthetische Netzwerkanforderungen über HTTP zu stellen.</span><span class="sxs-lookup"><span data-stu-id="6c319-157">**Network Console** is the working title of an experiment to make synthetic network requests over HTTP.</span></span>  <span data-ttu-id="6c319-158">Sie können das **Netzwerkkonsolen** Experiment verwenden, um Web-API-Anforderungen zu senden.</span><span class="sxs-lookup"><span data-stu-id="6c319-158">You may use the **Network Console** experiment to send web API requests.</span></span>  

<span data-ttu-id="6c319-159">Nachdem Sie das Experiment aktiviert haben, stellen Sie sicher, dass Sie das devtools erneut starten.</span><span class="sxs-lookup"><span data-stu-id="6c319-159">After enabling the experiment, ensure you restart the DevTools.</span></span>  <span data-ttu-id="6c319-160">So verwenden Sie die Netzwerk Konsole:</span><span class="sxs-lookup"><span data-stu-id="6c319-160">To use the Network Console:</span></span>  

1.  <span data-ttu-id="6c319-161">Öffnen Sie den Bereich **Netzwerk** .</span><span class="sxs-lookup"><span data-stu-id="6c319-161">Open the **Network** pane.</span></span>  
1.  <span data-ttu-id="6c319-162">Suchen Sie die Netzwerkanforderung, die Sie ändern möchten, und senden Sie Sie erneut.</span><span class="sxs-lookup"><span data-stu-id="6c319-162">Find the network request that you want to change and resend.</span></span>  
1.  <span data-ttu-id="6c319-163">Öffnen Sie das Kontextmenü \ (Klicken Sie mit der rechten Maustaste auf \), und wählen Sie **Bearbeiten und wiedergeben**aus.</span><span class="sxs-lookup"><span data-stu-id="6c319-163">Open the contextual menu \(right-click\), and choose **Edit and Replay**.</span></span>  
1.  <span data-ttu-id="6c319-164">Wenn die **Netzwerk Konsole** geöffnet wird, bearbeiten Sie die Netzwerk Anforderungsinformationen.</span><span class="sxs-lookup"><span data-stu-id="6c319-164">When the **Network Console** opens, edit the network request information.</span></span>  
1.  <span data-ttu-id="6c319-165">Wählen Sie **senden**aus.</span><span class="sxs-lookup"><span data-stu-id="6c319-165">Select **Send**.</span></span>  

:::image type="complex" source="./media/network-network-console.png" alt-text="Netzwerk Konsole im Konsolen Einzug" lightbox="./media/network-network-console.png":::
   <span data-ttu-id="6c319-167">**Netzwerk Konsole** im **Konsolen** Einzug</span><span class="sxs-lookup"><span data-stu-id="6c319-167">**Network Console** in the **Console** drawer</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 85 and later.  --> 

### <span data-ttu-id="6c319-168">Quellauftrags Anzeige aktivieren</span><span class="sxs-lookup"><span data-stu-id="6c319-168">Enable Source Order Viewer</span></span>  

<span data-ttu-id="6c319-169">Die **Ansicht "Quellreihenfolge** " ist der Arbeitstitel eines Experiments, um die Reihenfolge der Elemente in der Seitenquelle anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="6c319-169">**Source Order Viewer** is the working title of an experiment to display the order of elements in the page source.</span></span>  <span data-ttu-id="6c319-170">Sie können das Experiment der **Quellauftrags Anzeige** verwenden, um Barrierefreiheitsprobleme in Ihren Seiten zu finden, da sich die Anzeigereihenfolge auf dem Bildschirm von der Reihenfolge der Quelle unterscheiden kann, die die Benutzer der Bildschirmsprachausgabe verwirrt.</span><span class="sxs-lookup"><span data-stu-id="6c319-170">You may use the **Source Order Viewer** experiment to find accessibility issues in your pages since the display order on-screen may differ from the order of the source, which confuses screen reader users.</span></span>  

<span data-ttu-id="6c319-171">Nachdem Sie das Experiment aktiviert haben, stellen Sie sicher, dass Sie das devtools erneut starten.</span><span class="sxs-lookup"><span data-stu-id="6c319-171">After enabling the experiment, ensure you restart the DevTools.</span></span>  <span data-ttu-id="6c319-172">So verwenden Sie die Quellauftrags Anzeige:</span><span class="sxs-lookup"><span data-stu-id="6c319-172">To use Source Order Viewer:</span></span>  

1.  <span data-ttu-id="6c319-173">Öffnen Sie den Bereich **Elemente** .</span><span class="sxs-lookup"><span data-stu-id="6c319-173">Open the **Elements** pane.</span></span>  
1.  <span data-ttu-id="6c319-174">Öffnen Sie den Bereich " **Barrierefreiheit** " im Bereich "Schublade \" (unten).</span><span class="sxs-lookup"><span data-stu-id="6c319-174">Open the **Accessibility** pane in the drawer \(bottom\) panel.</span></span>  
1.  <span data-ttu-id="6c319-175">Aktivieren Sie im Abschnitt **Quellauftrags Anzeige** das Kontrollkästchen **Quellreihenfolge anzeigen** .</span><span class="sxs-lookup"><span data-stu-id="6c319-175">Under the **Source Order Viewer** section, select the **Show Source Order** checkbox.</span></span>  
1.  <span data-ttu-id="6c319-176">Markieren Sie ein beliebiges HTML-Element, um ein Overlay anzuzeigen, das die Reihenfolge in der Seitenquelle enthält.</span><span class="sxs-lookup"><span data-stu-id="6c319-176">Highlight any HTML element to display an overlay that the order in the page source.</span></span>  

:::image type="complex" source="./media/experiments-source-order-viewer.msft.png" alt-text="Viewer für Quellreihenfolge im Bereich "Barrierefreiheit"" lightbox="./media/experiments-source-order-viewer.msft.png":::
   <span data-ttu-id="6c319-178">**Viewer für Quellreihenfolge** im Bereich " **Barrierefreiheit** "</span><span class="sxs-lookup"><span data-stu-id="6c319-178">**Source Order Viewer** in the **Accessibility** pane</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 86 and later.  -->  

## <span data-ttu-id="6c319-179">Frühere experimentelle Features</span><span class="sxs-lookup"><span data-stu-id="6c319-179">Previous experimental features</span></span>  

*   <span data-ttu-id="6c319-180">die [3D-Ansicht][Devtools3dViewIndex] ist jetzt in Microsoft Edge, Version 83 oder höher, standardmäßig verfügbar und aktiviert.</span><span class="sxs-lookup"><span data-stu-id="6c319-180">[3D View][Devtools3dViewIndex] is now available and turned on by default in Microsoft Edge version 83 or later.</span></span>  
*   <span data-ttu-id="6c319-181">[Anpassen von Tastenkombinationen][DevtoolsCustomKeyboardShortcuts] ist jetzt in Microsoft Edge, Version 86 oder höher, standardmäßig verfügbar und aktiviert.</span><span class="sxs-lookup"><span data-stu-id="6c319-181">[Customize Keyboard Shortcuts][DevtoolsCustomKeyboardShortcuts] is now available and turned on by default in Microsoft Edge version 86 or later.</span></span>
## <span data-ttu-id="6c319-182">Bereitstellen von Feedback zu experimentellen Features</span><span class="sxs-lookup"><span data-stu-id="6c319-182">Providing feedback on experimental features</span></span>  

<span data-ttu-id="6c319-183">Sie können Feedback zu Microsoft Edge devtools-Experimenten oder zu allem anderen, was mit devtools zu tun hat.</span><span class="sxs-lookup"><span data-stu-id="6c319-183">To provide feedback on Microsoft Edge DevTools experiments, or anything else related to DevTools.</span></span>  

*   <span data-ttu-id="6c319-184">Senden Sie Ihr Feedback über das Symbol " **Feedback senden** " im devtools</span><span class="sxs-lookup"><span data-stu-id="6c319-184">Send your feedback using the **Send Feedback** icon in the DevTools</span></span>  
*   <span data-ttu-id="6c319-185">Tweet bei [@EdgeDevTools][TwitterEdgedevtools]</span><span class="sxs-lookup"><span data-stu-id="6c319-185">Tweet at [@EdgeDevTools][TwitterEdgedevtools]</span></span>   

:::image type="complex" source="./media/bing-devtools-send-feedback.msft.png" alt-text="Das Symbol "Feedback senden" im Microsoft Edge-devtools" lightbox="./media/bing-devtools-send-feedback.msft.png":::
   <span data-ttu-id="6c319-187">Das Symbol " **Feedback senden** " in Microsoft Edge devtools</span><span class="sxs-lookup"><span data-stu-id="6c319-187">The **Send Feedback** icon in Microsoft Edge DevTools</span></span>  
:::image-end:::  

<!-- links -->  

[Devtools3dViewIndex]: ./3d-view/index.md "3D-Ansicht | Microsoft docs"  
[DevtoolsIssues]: ./issues/index.md "Suchen und Beheben von Problemen mit dem Microsoft Edge devtools Issues Tool | Microsoft docs"  
[DevToolsCustomizeSettings]: ./customize/index.md#settings "Einstellungen – anpassen von Microsoft Edge devtools | Microsoft docs"  
[DevToolsShortcuts]: ./shortcuts.md "Microsoft Edge devtools-Tastenkombinationen | Microsoft docs"  
[DevtoolsOpen]: ./open.md "Öffnen Sie Microsoft Edge devtools | Microsoft docs"  
[DevtoolsCustomKeyboardShortcuts]: ./customize/shortcuts.md "Anpassen von Tastenkombinationen in Microsoft Edge devtools | Microsoft docs"

[TwitterEdgedevtools]: https://www.twitter.com/EdgeDevTools "Microsoft Edge-devtools | Twitter"  

[WebhintMain]: https://webhint.io "webhint" 
