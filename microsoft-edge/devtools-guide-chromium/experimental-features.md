---
description: Die neuesten experimentellen Features in Microsoft Edge devtools
title: Experimentelle Funktionen
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/07/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Web-Entwicklung, F12-Tools, devtools, Experiment
ms.openlocfilehash: 6824b09ffc3c1f00c4a2f3000d84bf2c1be743d0
ms.sourcegitcommit: 1e33cd41e5afb2e6dbdc19353011ff6c2b019f9c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/13/2020
ms.locfileid: "10866043"
---
# <span data-ttu-id="d057f-104">Experimentelle Funktionen</span><span class="sxs-lookup"><span data-stu-id="d057f-104">Experimental features</span></span>  

<span data-ttu-id="d057f-105">Sie können die experimentellen Features, die noch in der Entwicklung sind, in der Microsoft Edge-devtools verwenden, um zu testen und [Feedback bereitzustellen](#providing-feedback-on-experimental-features) , bevor diese im allgemeinen veröffentlicht werden.</span><span class="sxs-lookup"><span data-stu-id="d057f-105">You may use the experimental features that are still under development in the Microsoft Edge DevTools to test and [provide feedback](#providing-feedback-on-experimental-features) before each is released broadly.</span></span>  

<span data-ttu-id="d057f-106">Während experimentelle Features in allen Kanälen von Microsoft Edge verfügbar sind, erhalten Sie möglicherweise die neuesten experimentellen Features mithilfe des Canary-Kanals von Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="d057f-106">While experimental features are available in all channels of Microsoft Edge, you may get the latest experimental features using the Microsoft Edge Canary channel.</span></span>  

## <span data-ttu-id="d057f-107">Aktivieren von experimentellen Features</span><span class="sxs-lookup"><span data-stu-id="d057f-107">Turn on experimental features</span></span>  

<span data-ttu-id="d057f-108">Führen Sie die folgenden Schritte aus, um die experimentellen Features von \ (oder Off \) in Microsoft Edge zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="d057f-108">Use the following steps to turn on \(or off\) experimental features in Microsoft Edge.</span></span>  

1.  <span data-ttu-id="d057f-109">[Öffnen Sie devtools][DevtoolsOpen].</span><span class="sxs-lookup"><span data-stu-id="d057f-109">[Open DevTools][DevtoolsOpen].</span></span>  
     *   <span data-ttu-id="d057f-110">Drücken Sie `Control` + `Shift` + `I` \ (Windows \) oder `Command` + `Option` + `I` \ (macOS \).</span><span class="sxs-lookup"><span data-stu-id="d057f-110">Press `Control`+`Shift`+`I` \(Windows\) or `Command`+`Option`+`I` \(macOS\).</span></span>  <span data-ttu-id="d057f-111">Weitere Informationen finden Sie unter [Tastenkombinationen für Microsoft Edge devtools][DevToolsShortcuts].</span><span class="sxs-lookup"><span data-stu-id="d057f-111">For more information, see [Microsoft Edge DevTools keyboard shortcuts][DevToolsShortcuts].</span></span>  
1.  <span data-ttu-id="d057f-112">Öffnen Sie den Bereich " [Einstellungen][DevToolsCustomizeSettings] ".</span><span class="sxs-lookup"><span data-stu-id="d057f-112">Open the [Settings][DevToolsCustomizeSettings] pane.</span></span>  
    *   <span data-ttu-id="d057f-113">Drücken Sie `Shift` + `?` .</span><span class="sxs-lookup"><span data-stu-id="d057f-113">Press `Shift`+`?`.</span></span>  <span data-ttu-id="d057f-114">Weitere Informationen finden Sie unter [Tastenkombinationen für Microsoft Edge devtools][DevToolsShortcuts].</span><span class="sxs-lookup"><span data-stu-id="d057f-114">For more information, see [Microsoft Edge DevTools keyboard shortcuts][DevToolsShortcuts].</span></span>  
1.  <span data-ttu-id="d057f-115">Wählen Sie auf der linken Seite des Bereichs **Einstellungen** den Abschnitt **Experimente** aus.</span><span class="sxs-lookup"><span data-stu-id="d057f-115">On the left side of the **Settings** pane, select the **Experiments** section.</span></span>  
    
    :::image type="complex" source="./media/experiments-devtools.png" alt-text="Liste der Experimente in den devtools-Einstellungen" lightbox="./media/experiments-devtools.png":::
       <span data-ttu-id="d057f-117">Liste der Experimente in den devtools-Einstellungen</span><span class="sxs-lookup"><span data-stu-id="d057f-117">List of experiments in DevTools Settings</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="d057f-118">Scrollen Sie auf der Seite **Experimente** durch die Liste aller verfügbaren experimentellen Features, und aktivieren Sie das Kontrollkästchen neben den einzelnen Features, die Sie testen möchten.</span><span class="sxs-lookup"><span data-stu-id="d057f-118">On the **Experiments** page, scroll through the list of all available experimental features and select the checkbox next to each features that you want to test.</span></span>  
1.  <span data-ttu-id="d057f-119">Schließen Sie die Microsoft Edge-devtools, und öffnen Sie Sie erneut.</span><span class="sxs-lookup"><span data-stu-id="d057f-119">Close and reopen Microsoft Edge DevTools.</span></span>  

> [!NOTE]
> <span data-ttu-id="d057f-120">Experimentelle Features werden ständig aktualisiert, was zu Leistungsproblemen führen kann.</span><span class="sxs-lookup"><span data-stu-id="d057f-120">Experimental features are constantly being updated and may cause performance issues.</span></span>  <span data-ttu-id="d057f-121">Wenn Sie ein experimentelles Feature deaktivieren möchten, öffnen Sie die Seite **Experimente** , und deaktivieren Sie das Kontrollkästchen des experimentellen Features, das Sie deaktivieren möchten.</span><span class="sxs-lookup"><span data-stu-id="d057f-121">To turn off an experimental feature, open the **Experiments** page and clear the checkbox of the experimental feature that you want to turn off.</span></span>  

## <span data-ttu-id="d057f-122">Hervorgehobene experimentelle Features</span><span class="sxs-lookup"><span data-stu-id="d057f-122">Highlighted experimental features</span></span>  

<span data-ttu-id="d057f-123">In den folgenden Abschnitten werden die neuen experimentellen Features beschrieben, die in Microsoft Edge zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="d057f-123">The following sections describe the new experimental features that are available in Microsoft Edge.</span></span>  

| <span data-ttu-id="d057f-124">Experimentelle Funktion</span><span class="sxs-lookup"><span data-stu-id="d057f-124">Experimental feature</span></span> | <span data-ttu-id="d057f-125">Microsoft Edge-Version</span><span class="sxs-lookup"><span data-stu-id="d057f-125">Microsoft Edge version</span></span> |  
|:--- |:--- |  
| [<span data-ttu-id="d057f-126">Aktivieren der Registerkarte "Benutzerdefinierte Tastenkombinationen"</span><span class="sxs-lookup"><span data-stu-id="d057f-126">Enable custom keyboard shortcuts settings tab</span></span>](#enable-custom-keyboard-shortcuts-settings-tab) | <span data-ttu-id="d057f-127">84 oder höher</span><span class="sxs-lookup"><span data-stu-id="d057f-127">84 or later</span></span> |
| [<span data-ttu-id="d057f-128">Debuggen von neuen CSS-Raster Features aktivieren</span><span class="sxs-lookup"><span data-stu-id="d057f-128">Enable new CSS grid debugging features</span></span>](#enable-new-css-grid-debugging-features) | <span data-ttu-id="d057f-129">85 oder höher</span><span class="sxs-lookup"><span data-stu-id="d057f-129">85 or later</span></span> |  
| [<span data-ttu-id="d057f-130">Aktivieren der Unterstützung für das Verschieben von Tabstopps zwischen Bereichen</span><span class="sxs-lookup"><span data-stu-id="d057f-130">Enable support to move tabs between panels</span></span>](#enable-support-to-move-tabs-between-panels) | <span data-ttu-id="d057f-131">85 oder höher</span><span class="sxs-lookup"><span data-stu-id="d057f-131">85 or later</span></span> |  
| [<span data-ttu-id="d057f-132">Webhint aktivieren</span><span class="sxs-lookup"><span data-stu-id="d057f-132">Enable webhint</span></span>](#enable-webhint) | <span data-ttu-id="d057f-133">85 oder höher</span><span class="sxs-lookup"><span data-stu-id="d057f-133">85 or later</span></span> | 

### <span data-ttu-id="d057f-134">Aktivieren der Registerkarte "Benutzerdefinierte Tastenkombinationen"</span><span class="sxs-lookup"><span data-stu-id="d057f-134">Enable custom keyboard shortcuts settings tab</span></span>

<span data-ttu-id="d057f-135">Enthält eine neue **Verknüpfungs** Seite in [devtools-Einstellungen][DevToolsCustomizeSettings] , die das Zuordnen von [Tastenkombinationen][DevToolsShortcuts] im devtools zu [vs-Code][VisualstudioCode]ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="d057f-135">Provides a new **Shortcuts** page in [DevTools Settings][DevToolsCustomizeSettings] that enables matching [keyboard shortcuts][DevToolsShortcuts] in the DevTools to [VS Code][VisualstudioCode].</span></span>  

<span data-ttu-id="d057f-136">Nachdem Sie dieses Experiment aktiviert haben, öffnen Sie die [devtools-Einstellungen][DevToolsCustomizeSettings] erneut, indem Sie auf klicken `Shift` + `?` .</span><span class="sxs-lookup"><span data-stu-id="d057f-136">Once you have enabled this experiment, open [DevTools Settings][DevToolsCustomizeSettings] again by pressing `Shift`+`?`.</span></span>  <span data-ttu-id="d057f-137">Navigieren Sie zur Seite neue **Verknüpfungen** .</span><span class="sxs-lookup"><span data-stu-id="d057f-137">Navigate to the new **Shortcuts** page.</span></span>  <span data-ttu-id="d057f-138">Wählen Sie im Dropdownmenü **Tastenkombinationen von Voreinstellungen** **devtools (Standard)** aus, und wählen Sie **Visual Studio-Code**aus.</span><span class="sxs-lookup"><span data-stu-id="d057f-138">Select **DevTools (Default)** in the **Match shortcuts from preset** dropdown and select **Visual Studio Code**.</span></span>  <span data-ttu-id="d057f-139">Die Tastenkombinationen im devtools entsprechen nun den Tastenkombinationen für äquivalente Aktionen in vs-Code.</span><span class="sxs-lookup"><span data-stu-id="d057f-139">The keyboard shortcuts in the DevTools now match the shortcuts for equivalent actions in VS Code.</span></span>  

:::image type="complex" source="./media/experiments-keyboard-shortcut.png" alt-text="Anpassen von Tastenkombinationen im devtools an vs-Code" lightbox="./media/experiments-keyboard-shortcut.png":::
   <span data-ttu-id="d057f-141">Anpassen von Tastenkombinationen im devtools an vs-Code</span><span class="sxs-lookup"><span data-stu-id="d057f-141">Match keyboard shortcuts in the DevTools to VS Code</span></span>
:::image-end:::  

<span data-ttu-id="d057f-142">Beispielsweise ist unter Windows die Tastenkombination zum Anhalten oder Fortsetzen der Ausführung eines Skripts im [vs-Code][VisualstudioCodeShortcutsKeyboardWindows] `F5` .</span><span class="sxs-lookup"><span data-stu-id="d057f-142">For example, on Windows the keyboard shortcut for pausing or continuing running a script in [VS Code][VisualstudioCodeShortcutsKeyboardWindows] is `F5`.</span></span>  <span data-ttu-id="d057f-143">Wenn die **devtools (Standardeinstellung)** voreingestellt ist, ist die gleiche Verknüpfung in der devtools, `F8` aber mit der **Visual Studio-Code** Vorgabe, diese Verknüpfung nun auch `F5` .</span><span class="sxs-lookup"><span data-stu-id="d057f-143">With the **DevTools (Default)** preset, that same shortcut in the DevTools is `F8` but with the **Visual Studio Code** preset, that shortcut is now also `F5`.</span></span>  

### <span data-ttu-id="d057f-144">Debuggen von neuen CSS-Raster Features aktivieren</span><span class="sxs-lookup"><span data-stu-id="d057f-144">Enable new CSS grid debugging features</span></span>  

<span data-ttu-id="d057f-145">Verbessert die on-page-Visualisierungen, wenn Sie Websites mit CSS-Rasterlayouts Debuggen.</span><span class="sxs-lookup"><span data-stu-id="d057f-145">Improves on-page visualizations when you debug websites that have CSS grid layouts.</span></span>  <span data-ttu-id="d057f-146">Sie können die Overlays in den devtools-Einstellungen weiter anpassen.</span><span class="sxs-lookup"><span data-stu-id="d057f-146">You may further customize the overlays in DevTools Settings.</span></span>  

:::image type="complex" source="./media/experiments-grid.png" alt-text="CSS-Raster Debugging-Feature" lightbox="./media/experiments-grid.png":::
   <span data-ttu-id="d057f-148">CSS-Raster Debugging-Feature</span><span class="sxs-lookup"><span data-stu-id="d057f-148">CSS grid debugging feature</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 85 and later.  -->  

### <span data-ttu-id="d057f-149">Aktivieren der Unterstützung für das Verschieben von Tabstopps zwischen Bereichen</span><span class="sxs-lookup"><span data-stu-id="d057f-149">Enable support to move tabs between panels</span></span>  

<span data-ttu-id="d057f-150">In der Regel können Tools, wie **Elemente** und **Netzwerke** , nur im Hauptbereich \ (oben \) von devtools geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="d057f-150">Normally, tools such as **Elements** and **Network** may only be opened in the main \(top\) panel of DevTools.</span></span>  <span data-ttu-id="d057f-151">Auf ähnliche Weise können Tools wie **3D-Ansicht** und **Probleme** nur im Bereich "drawer \ (unten \)" von devtools geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="d057f-151">Similarly, tools such as **3D View** and **Issues** may only be opened in the drawer \(bottom\) panel of DevTools.</span></span>  <span data-ttu-id="d057f-152">Wenn dieses Experiment ausgewählt ist, können Sie die Tools zwischen dem oberen und unteren Bereich verschieben, indem Sie auf die Registerkarte zeigen, das Kontextmenü öffnen (Klicken Sie mit der rechten Maustaste auf \), und wählen Sie **nach oben** oder **nach unten**verschieben aus.</span><span class="sxs-lookup"><span data-stu-id="d057f-152">When this experiment is selected, you may move tools between the top and bottom panels by hovering on the tab, opening the contextual menu \(right-click\), and selecting **Move to top** or **Move to bottom**.</span></span>   <span data-ttu-id="d057f-153">Mit diesem Experiment können Sie Ihr devtools-Layout anpassen.</span><span class="sxs-lookup"><span data-stu-id="d057f-153">This experiment allows you to customize your DevTools layout.</span></span>  <span data-ttu-id="d057f-154">Wenn Sie den unteren Bereich ein-oder ausblenden möchten, drücken Sie `Escape` .</span><span class="sxs-lookup"><span data-stu-id="d057f-154">To show or hide the bottom panel, press `Escape`.</span></span>  

:::image type="complex" source="./media/experiments-move-panels.png" alt-text="Verschieben von Tabstopps zwischen Bereichen" lightbox="./media/experiments-move-panels.png":::
   <span data-ttu-id="d057f-156">Verschieben von Tabstopps zwischen Bereichen</span><span class="sxs-lookup"><span data-stu-id="d057f-156">Moving tabs between panels</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 85 and later.  -->  

### <span data-ttu-id="d057f-157">Webhint aktivieren</span><span class="sxs-lookup"><span data-stu-id="d057f-157">Enable webhint</span></span>  

<span data-ttu-id="d057f-158">[webhint][WebhintMain] ist ein Open-Source-Tool, das in Echtzeit Feedback zur Barrierefreiheit, browserübergreifenden Kompatibilität, Sicherheit, Leistung, PWAs und anderen gängigen Webentwicklungs Problemen von Websites bietet.</span><span class="sxs-lookup"><span data-stu-id="d057f-158">[webhint][WebhintMain] is an open-source tool that provides real-time feedback on the accessibility, cross-browser compatibility, security, performance, PWAs, and other common web development issues of websites.</span></span>  <span data-ttu-id="d057f-159">Dieses Experiment führt das webhint-Feedback in devtools im Bereich [Probleme][DevtoolsIssues] .</span><span class="sxs-lookup"><span data-stu-id="d057f-159">This experiment brings the webhint feedback into DevTools in the [Issues][DevtoolsIssues] panel.</span></span>  <span data-ttu-id="d057f-160">Sie können das Problem auswählen, um die Dokumentation zur Behebung des Problems und eine Liste der betroffenen Ressourcen auf Ihrer Website anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="d057f-160">You may select the issue to see documentation on how to fix the issue and a list of the affected resources on your website.</span></span>  <span data-ttu-id="d057f-161">Wählen Sie einen Ressourcen Link aus, um den entsprechenden Bereich für **Netzwerke**, **Quellen**oder **Elemente** in devtools zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="d057f-161">Select a resource link to open the relevant **Network**, **Sources**, or **Elements** pane in DevTools.</span></span>  

:::image type="complex" source="./media/experiments-webhint.png" alt-text="webhint-Feedback im Bereich "Probleme"" lightbox="./media/experiments-webhint.png":::
   <span data-ttu-id="d057f-163">webhint-Feedback im Bereich "Probleme"</span><span class="sxs-lookup"><span data-stu-id="d057f-163">webhint feedback in the Issues panel</span></span>  
:::image-end:::      

<!--Available in Microsoft Edge version 85 and later.  -->  

## <span data-ttu-id="d057f-164">Frühere experimentelle Features</span><span class="sxs-lookup"><span data-stu-id="d057f-164">Previous experimental features</span></span>  

*   <span data-ttu-id="d057f-165">die [3D-Ansicht][Devtools3dViewIndex] ist jetzt in Microsoft Edge, Version 83 oder höher, standardmäßig verfügbar und aktiviert.</span><span class="sxs-lookup"><span data-stu-id="d057f-165">[3D View][Devtools3dViewIndex] is now available and turned on by default in Microsoft Edge version 83 or later.</span></span>  

## <span data-ttu-id="d057f-166">Bereitstellen von Feedback zu experimentellen Features</span><span class="sxs-lookup"><span data-stu-id="d057f-166">Providing feedback on experimental features</span></span>  

<span data-ttu-id="d057f-167">Sie können Feedback zu Microsoft Edge devtools-Experimenten oder zu allem anderen, was mit devtools zu tun hat.</span><span class="sxs-lookup"><span data-stu-id="d057f-167">To provide feedback on Microsoft Edge DevTools experiments, or anything else related to DevTools.</span></span>  

*   <span data-ttu-id="d057f-168">Senden Sie Ihr Feedback über das Feedback-Symbol im devtools</span><span class="sxs-lookup"><span data-stu-id="d057f-168">Send your feedback using the Feedback icon in the DevTools</span></span>  
*   <span data-ttu-id="d057f-169">Tweet bei [@EdgeDevTools][TwitterEdgedevtools]</span><span class="sxs-lookup"><span data-stu-id="d057f-169">Tweet at [@EdgeDevTools][TwitterEdgedevtools]</span></span>  

:::image type="complex" source="./media/devtools-feedback.png" alt-text="Symbol "Feedback" im Microsoft Edge-devtools" lightbox="./media/devtools-feedback.png":::
   <span data-ttu-id="d057f-171">Symbol "Feedback" im Microsoft Edge-devtools</span><span class="sxs-lookup"><span data-stu-id="d057f-171">Feedback icon in the Microsoft Edge DevTools</span></span>  
:::image-end:::  

<!-- links -->  

[Devtools3dViewIndex]: ./3d-view/index.md "3D-Ansicht | Microsoft docs"  
[DevtoolsIssues]: ./issues/index.md "Suchen und Beheben von Problemen mit dem Microsoft Edge devtools Issues Tool | Microsoft docs"  
[DevToolsCustomizeSettings]: ./customize/index.md#settings "Einstellungen – anpassen von Microsoft Edge devtools | Microsoft docs"  
[DevToolsShortcuts]: ./shortcuts.md "Microsoft Edge devtools-Tastenkombinationen | Microsoft docs"  
[DevtoolsOpen]: ./open.md "Öffnen Sie Microsoft Edge devtools | Microsoft docs"  

[TwitterEdgedevtools]: https://www.twitter.com/EdgeDevTools "Microsoft Edge-devtools | Twitter"  

[VisualstudioCode]: https://code.visualstudio.com "Visual Studio-Code"  
[VisualstudioCodeShortcutsKeyboardWindows]: https://code.visualstudio.com/shortcuts/keyboard-shortcuts-windows.pdf "Visual Studio-Code Tastenkombinationen für Windows | Visual Studio-Code"  

[WebhintMain]: https://webhint.io "webhint" 
