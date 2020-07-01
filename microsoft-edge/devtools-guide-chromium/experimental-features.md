---
description: Die neuesten experimentellen Features in Microsoft Edge devtools
title: Experimentelle Features
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/26/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Web-Entwicklung, F12-Tools, devtools, Experiment
ms.openlocfilehash: 731a289f555870eeff9cdc160965b59925b70c4d
ms.sourcegitcommit: 0048eb692d49eab4755c0c3ef6866e6a9122d579
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/01/2020
ms.locfileid: "10843950"
---
# <span data-ttu-id="d9b07-104">Experimentelle Features</span><span class="sxs-lookup"><span data-stu-id="d9b07-104">Experimental features</span></span>  

<span data-ttu-id="d9b07-105">Sie können die experimentellen Features, die noch in der Entwicklung sind, in der Microsoft Edge-devtools verwenden, um zu testen und [Feedback bereitzustellen](#providing-feedback-on-experimental-features) , bevor diese im allgemeinen veröffentlicht werden.</span><span class="sxs-lookup"><span data-stu-id="d9b07-105">You may use the experimental features that are still under development in the Microsoft Edge DevTools to test and [provide feedback](#providing-feedback-on-experimental-features) before each is released broadly.</span></span>  

<span data-ttu-id="d9b07-106">Während experimentelle Features in allen Kanälen von Microsoft Edge verfügbar sind, erhalten Sie möglicherweise die neuesten experimentellen Features mithilfe des Canary-Kanals von Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="d9b07-106">While experimental features are available in all channels of Microsoft Edge, you may get the latest experimental features using the Microsoft Edge Canary channel.</span></span>  

## <span data-ttu-id="d9b07-107">Aktivieren von experimentellen Features</span><span class="sxs-lookup"><span data-stu-id="d9b07-107">Turn on experimental features</span></span>  

<span data-ttu-id="d9b07-108">Führen Sie die folgenden Schritte aus, um die experimentellen Features von \ (oder Off \) in Microsoft Edge zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="d9b07-108">Use the following steps to turn on \(or off\) experimental features in Microsoft Edge.</span></span>  

1.  <span data-ttu-id="d9b07-109">[Öffnen Sie devtools][DevtoolsOpen].</span><span class="sxs-lookup"><span data-stu-id="d9b07-109">[Open DevTools][DevtoolsOpen].</span></span>  
     *   <span data-ttu-id="d9b07-110">Drücken Sie `Control` + `Shift` + `I` \ (Windows \) oder `Command` + `Option` + `I` \ (macOS \).</span><span class="sxs-lookup"><span data-stu-id="d9b07-110">Press `Control`+`Shift`+`I` \(Windows\) or `Command`+`Option`+`I` \(macOS\).</span></span>  <span data-ttu-id="d9b07-111">Weitere Informationen finden Sie unter [Tastenkombinationen für Microsoft Edge devtools][DevToolsShortcuts].</span><span class="sxs-lookup"><span data-stu-id="d9b07-111">For more information, see [Microsoft Edge DevTools keyboard shortcuts][DevToolsShortcuts].</span></span>  
1.  <span data-ttu-id="d9b07-112">Öffnen Sie den Bereich " **Einstellungen** ".</span><span class="sxs-lookup"><span data-stu-id="d9b07-112">Open the **Settings** pane.</span></span>  
    *   <span data-ttu-id="d9b07-113">Drücken Sie `Shift` + `?` .</span><span class="sxs-lookup"><span data-stu-id="d9b07-113">Press `Shift`+`?`.</span></span>  <span data-ttu-id="d9b07-114">Weitere Informationen finden Sie unter [Tastenkombinationen für Microsoft Edge devtools][DevToolsShortcuts].</span><span class="sxs-lookup"><span data-stu-id="d9b07-114">For more information, see [Microsoft Edge DevTools keyboard shortcuts][DevToolsShortcuts].</span></span>  
1.  <span data-ttu-id="d9b07-115">Wählen Sie auf der linken Seite des Bereichs **Einstellungen** den Abschnitt **Experimente** aus.</span><span class="sxs-lookup"><span data-stu-id="d9b07-115">On the left side of the **Settings** pane, select the **Experiments** section.</span></span>  
    
    :::image type="complex" source="./media/experiments-devtools.png" alt-text="Liste der Experimente in den devtools-Einstellungen" lightbox="./media/experiments-devtools.png":::
       <span data-ttu-id="d9b07-117">Liste der Experimente in den devtools-Einstellungen</span><span class="sxs-lookup"><span data-stu-id="d9b07-117">List of experiments in DevTools Settings</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="d9b07-118">Scrollen Sie auf der Seite **Experimente** durch die Liste aller verfügbaren experimentellen Features, und aktivieren Sie das Kontrollkästchen neben den einzelnen Features, die Sie testen möchten.</span><span class="sxs-lookup"><span data-stu-id="d9b07-118">On the **Experiments** page, scroll through the list of all available experimental features and select the checkbox next to each features that you want to test.</span></span>  
1.  <span data-ttu-id="d9b07-119">Schließen Sie die Microsoft Edge-devtools, und öffnen Sie Sie erneut.</span><span class="sxs-lookup"><span data-stu-id="d9b07-119">Close and reopen Microsoft Edge DevTools.</span></span>  

> [!NOTE]
> <span data-ttu-id="d9b07-120">Experimentelle Features werden ständig aktualisiert, was zu Leistungsproblemen führen kann.</span><span class="sxs-lookup"><span data-stu-id="d9b07-120">Experimental features are constantly being updated and may cause performance issues.</span></span>  <span data-ttu-id="d9b07-121">Wenn Sie ein experimentelles Feature deaktivieren möchten, öffnen Sie die Seite **Experimente** , und deaktivieren Sie das Kontrollkästchen des experimentellen Features, das Sie deaktivieren möchten.</span><span class="sxs-lookup"><span data-stu-id="d9b07-121">To turn off an experimental feature, open the **Experiments** page and clear the checkbox of the experimental feature that you want to turn off.</span></span>  

## <span data-ttu-id="d9b07-122">Hervorgehobene experimentelle Features</span><span class="sxs-lookup"><span data-stu-id="d9b07-122">Highlighted experimental features</span></span>  

<span data-ttu-id="d9b07-123">In den folgenden Abschnitten werden die neuen experimentellen Features beschrieben, die in Microsoft Edge zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="d9b07-123">The following sections describe the new experimental features that are available in Microsoft Edge.</span></span>  

| <span data-ttu-id="d9b07-124">Experimentelle Funktion</span><span class="sxs-lookup"><span data-stu-id="d9b07-124">Experimental feature</span></span> | <span data-ttu-id="d9b07-125">Microsoft Edge-Version</span><span class="sxs-lookup"><span data-stu-id="d9b07-125">Microsoft Edge version</span></span> |  
|:--- |:--- |  
| [<span data-ttu-id="d9b07-126">Debuggen von neuen CSS-Raster Features aktivieren</span><span class="sxs-lookup"><span data-stu-id="d9b07-126">Enable new CSS grid debugging features</span></span>](#enable-new-css-grid-debugging-features) | <span data-ttu-id="d9b07-127">85 oder höher</span><span class="sxs-lookup"><span data-stu-id="d9b07-127">85 or later</span></span> |  
| [<span data-ttu-id="d9b07-128">Aktivieren der Unterstützung für das Verschieben von Tabstopps zwischen Bereichen</span><span class="sxs-lookup"><span data-stu-id="d9b07-128">Enable support to move tabs between panels</span></span>](#enable-support-to-move-tabs-between-panels) | <span data-ttu-id="d9b07-129">85 oder höher</span><span class="sxs-lookup"><span data-stu-id="d9b07-129">85 or later</span></span> |  
| [<span data-ttu-id="d9b07-130">Webhint aktivieren</span><span class="sxs-lookup"><span data-stu-id="d9b07-130">Enable webhint</span></span>](#enable-webhint) | <span data-ttu-id="d9b07-131">85 oder höher</span><span class="sxs-lookup"><span data-stu-id="d9b07-131">85 or later</span></span> |  

### <span data-ttu-id="d9b07-132">Debuggen von neuen CSS-Raster Features aktivieren</span><span class="sxs-lookup"><span data-stu-id="d9b07-132">Enable new CSS grid debugging features</span></span>  

<span data-ttu-id="d9b07-133">Verbessert die on-page-Visualisierungen, wenn Sie Websites mit CSS-Rasterlayouts Debuggen.</span><span class="sxs-lookup"><span data-stu-id="d9b07-133">Improves on-page visualizations when you debug websites that have CSS grid layouts.</span></span>  <span data-ttu-id="d9b07-134">Sie können die Overlays in den devtools-Einstellungen weiter anpassen.</span><span class="sxs-lookup"><span data-stu-id="d9b07-134">You may further customize the overlays in DevTools Settings.</span></span>  

:::image type="complex" source="./media/experiments-grid.png" alt-text="CSS-Raster Debugging-Feature" lightbox="./media/experiments-grid.png":::
   <span data-ttu-id="d9b07-136">CSS-Raster Debugging-Feature</span><span class="sxs-lookup"><span data-stu-id="d9b07-136">CSS grid debugging feature</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 85 and later.  -->  

### <span data-ttu-id="d9b07-137">Aktivieren der Unterstützung für das Verschieben von Tabstopps zwischen Bereichen</span><span class="sxs-lookup"><span data-stu-id="d9b07-137">Enable support to move tabs between panels</span></span>  

<span data-ttu-id="d9b07-138">In der Regel können Tools, wie **Elemente** und **Netzwerke** , nur im Hauptbereich \ (oben \) von devtools geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="d9b07-138">Normally, tools such as **Elements** and **Network** may only be opened in the main \(top\) panel of DevTools.</span></span>  <span data-ttu-id="d9b07-139">Auf ähnliche Weise können Tools wie **3D-Ansicht** und **Probleme** nur im Bereich "drawer \ (unten \)" von devtools geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="d9b07-139">Similarly, tools such as **3D View** and **Issues** may only be opened in the drawer \(bottom\) panel of DevTools.</span></span>  <span data-ttu-id="d9b07-140">Wenn dieses Experiment ausgewählt ist, können Sie die Tools zwischen dem oberen und unteren Bereich verschieben, indem Sie auf die Registerkarte zeigen, das Kontextmenü öffnen (Klicken Sie mit der rechten Maustaste auf \), und wählen Sie **nach oben** oder **nach unten**verschieben aus.</span><span class="sxs-lookup"><span data-stu-id="d9b07-140">When this experiment is selected, you may move tools between the top and bottom panels by hovering on the tab, opening the contextual menu \(right-click\), and selecting **Move to top** or **Move to bottom**.</span></span>   <span data-ttu-id="d9b07-141">Mit diesem Experiment können Sie Ihr devtools-Layout anpassen.</span><span class="sxs-lookup"><span data-stu-id="d9b07-141">This experiment allows you to customize your DevTools layout.</span></span>  <span data-ttu-id="d9b07-142">Wenn Sie den unteren Bereich ein-oder ausblenden möchten, drücken Sie `Escape` .</span><span class="sxs-lookup"><span data-stu-id="d9b07-142">To show or hide the bottom panel, press `Escape`.</span></span>  

:::image type="complex" source="./media/experiments-move-panels.png" alt-text="Verschieben von Tabstopps zwischen Bereichen" lightbox="./media/experiments-move-panels.png":::
   <span data-ttu-id="d9b07-144">Verschieben von Tabstopps zwischen Bereichen</span><span class="sxs-lookup"><span data-stu-id="d9b07-144">Moving tabs between panels</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 85 and later.  -->  

### <span data-ttu-id="d9b07-145">Webhint aktivieren</span><span class="sxs-lookup"><span data-stu-id="d9b07-145">Enable webhint</span></span>  

<span data-ttu-id="d9b07-146">[webhint][WebhintMain] ist ein Open-Source-Tool, das in Echtzeit Feedback zur Barrierefreiheit, browserübergreifenden Kompatibilität, Sicherheit, Leistung, PWAs und anderen gängigen Webentwicklungs Problemen von Websites bietet.</span><span class="sxs-lookup"><span data-stu-id="d9b07-146">[webhint][WebhintMain] is an open-source tool that provides real-time feedback on the accessibility, cross-browser compatibility, security, performance, PWAs, and other common web development issues of websites.</span></span>  <span data-ttu-id="d9b07-147">Dieses Experiment führt das webhint-Feedback in devtools im Bereich [Probleme][DevtoolsIssues] .</span><span class="sxs-lookup"><span data-stu-id="d9b07-147">This experiment brings the webhint feedback into DevTools in the [Issues][DevtoolsIssues] panel.</span></span>  <span data-ttu-id="d9b07-148">Sie können das Problem auswählen, um die Dokumentation zur Behebung des Problems und eine Liste der betroffenen Ressourcen auf Ihrer Website anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="d9b07-148">You may select the issue to see documentation on how to fix the issue and a list of the affected resources on your website.</span></span>  <span data-ttu-id="d9b07-149">Wählen Sie einen Ressourcen Link aus, um den entsprechenden Bereich für **Netzwerke**, **Quellen**oder **Elemente** in devtools zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="d9b07-149">Select a resource link to open the relevant **Network**, **Sources**, or **Elements** pane in DevTools.</span></span>  

:::image type="complex" source="./media/experiments-webhint.png" alt-text="webhint-Feedback im Bereich "Probleme"" lightbox="./media/experiments-webhint.png":::
   <span data-ttu-id="d9b07-151">webhint-Feedback im Bereich "Probleme"</span><span class="sxs-lookup"><span data-stu-id="d9b07-151">webhint feedback in the Issues panel</span></span>  
:::image-end:::      

<!--Available in Microsoft Edge version 85 and later.  -->  

## <span data-ttu-id="d9b07-152">Frühere experimentelle Features</span><span class="sxs-lookup"><span data-stu-id="d9b07-152">Previous experimental features</span></span>  

*   <span data-ttu-id="d9b07-153">die [3D-Ansicht][Devtools3DView] ist jetzt in Microsoft Edge, Version 83 oder höher, standardmäßig verfügbar und aktiviert.</span><span class="sxs-lookup"><span data-stu-id="d9b07-153">[3D View][Devtools3DView] is now available and turned on by default in Microsoft Edge version 83 or later.</span></span>  

## <span data-ttu-id="d9b07-154">Bereitstellen von Feedback zu experimentellen Features</span><span class="sxs-lookup"><span data-stu-id="d9b07-154">Providing feedback on experimental features</span></span>  

<span data-ttu-id="d9b07-155">So geben Sie Feedback zu Microsoft Edge devtools-Experimenten oder zu allem anderen devtools:</span><span class="sxs-lookup"><span data-stu-id="d9b07-155">To provide feedback on Microsoft Edge DevTools experiments, or anything else related to DevTools:</span></span>  

*   <span data-ttu-id="d9b07-156">Senden Sie Ihr Feedback über das Feedback-Symbol im devtools</span><span class="sxs-lookup"><span data-stu-id="d9b07-156">Send your feedback using the Feedback icon in the DevTools</span></span>  
*   <span data-ttu-id="d9b07-157">Tweet bei [@EdgeDevTools][TwitterEdgedevtools]</span><span class="sxs-lookup"><span data-stu-id="d9b07-157">Tweet at [@EdgeDevTools][TwitterEdgedevtools]</span></span>  

:::image type="complex" source="./media/devtools-feedback.png" alt-text="Symbol "Feedback" im Microsoft Edge-devtools" lightbox="./media/devtools-feedback.png":::
   <span data-ttu-id="d9b07-159">Symbol "Feedback" im Microsoft Edge-devtools</span><span class="sxs-lookup"><span data-stu-id="d9b07-159">Feedback icon in the Microsoft Edge DevTools</span></span>  
:::image-end:::  

<!-- links -->  

[Devtools3DView]: ./3D-view.md "3D-Ansicht | Microsoft docs"  
[DevtoolsIssues]: ./issues/index.md "Suchen und Beheben von Problemen mit dem Microsoft Edge devtools Issues Tool | Microsoft docs"  
[DevToolsShortcuts]: ./shortcuts.md "Microsoft Edge devtools-Tastenkombinationen – Microsoft docs"  
[DevtoolsOpen]: ./open.md "Öffnen Sie Microsoft Edge devtools | Microsoft docs"  

[TwitterEdgedevtools]: https://www.twitter.com/EdgeDevTools "Microsoft Edge-devtools | Twitter"  

[WebhintMain]: https://webhint.io "webhint" 
