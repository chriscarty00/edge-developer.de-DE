---
description: Die neuesten experimentellen Features in Microsoft Edge devtools
title: Experimentelle Funktionen
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/07/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Web-Entwicklung, F12-Tools, devtools, Experiment
ms.openlocfilehash: b2b2e591834f1c75d51ec98523e2752d67a2d354
ms.sourcegitcommit: 6571bcc0b7f1c4c9d6ead65081374bab87cd4469
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "11203899"
---
# <span data-ttu-id="8d497-104">Experimentelle Funktionen</span><span class="sxs-lookup"><span data-stu-id="8d497-104">Experimental features</span></span>  

<span data-ttu-id="8d497-105">Microsoft Edge-devtools bieten Zugriff auf experimentelle Features, die sich noch in der Entwicklung befinden.</span><span class="sxs-lookup"><span data-stu-id="8d497-105">Microsoft Edge DevTools provide access to experimental features that are still in development.</span></span>  <span data-ttu-id="8d497-106">Sie können testen und [Feedback zur Verfügung stellen](#providing-feedback-on-experimental-features) , bevor die einzelnen Features veröffentlicht werden.</span><span class="sxs-lookup"><span data-stu-id="8d497-106">You may test and [provide feedback](#providing-feedback-on-experimental-features) before each feature is released.</span></span>  

<span data-ttu-id="8d497-107">Während experimentelle Features in allen Kanälen von Microsoft Edge verfügbar sind, erhalten Sie möglicherweise die neuesten experimentellen Features mithilfe des Canary-Kanals von Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="8d497-107">While experimental features are available in all channels of Microsoft Edge, you may get the latest experimental features using the Microsoft Edge Canary channel.</span></span>  

## <span data-ttu-id="8d497-108">Aktivieren von experimentellen Features</span><span class="sxs-lookup"><span data-stu-id="8d497-108">Turn on experimental features</span></span>  

<span data-ttu-id="8d497-109">Führen Sie die folgenden Schritte aus, um die experimentellen Features in Microsoft Edge zu aktivieren oder zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="8d497-109">To turn on \(or off\) experimental features in Microsoft Edge, complete the following steps.</span></span>  

1.  <span data-ttu-id="8d497-110">[Öffnen Sie devtools][DevtoolsOpen].</span><span class="sxs-lookup"><span data-stu-id="8d497-110">[Open DevTools][DevtoolsOpen].</span></span>  
    *   <span data-ttu-id="8d497-111">Wählen Sie `Control` + `Shift` + `I` \ (Windows, Linux \) oder `Command` + `Option` + `I` \ (macOS \) aus.</span><span class="sxs-lookup"><span data-stu-id="8d497-111">Select `Control`+`Shift`+`I` \(Windows, Linux\) or `Command`+`Option`+`I` \(macOS\).</span></span>  <span data-ttu-id="8d497-112">Weitere Informationen finden Sie unter [Tastenkombinationen für Microsoft Edge devtools][DevToolsShortcuts].</span><span class="sxs-lookup"><span data-stu-id="8d497-112">For more information, navigate to [Microsoft Edge DevTools keyboard shortcuts][DevToolsShortcuts].</span></span>  
1.  <span data-ttu-id="8d497-113">Öffnen Sie den Bereich " [Einstellungen][DevToolsCustomizeSettings] ".</span><span class="sxs-lookup"><span data-stu-id="8d497-113">Open the [Settings][DevToolsCustomizeSettings] pane.</span></span>  
    *   <span data-ttu-id="8d497-114">Wählen Sie aus `Shift` + `?` .</span><span class="sxs-lookup"><span data-stu-id="8d497-114">Select `Shift`+`?`.</span></span>  <span data-ttu-id="8d497-115">Weitere Informationen finden Sie unter [Tastenkombinationen für Microsoft Edge devtools][DevToolsShortcuts].</span><span class="sxs-lookup"><span data-stu-id="8d497-115">For more information, navigate to [Microsoft Edge DevTools keyboard shortcuts][DevToolsShortcuts].</span></span>  
1.  <span data-ttu-id="8d497-116">Wählen Sie auf der linken Seite des Bereichs **Einstellungen** den Abschnitt **Experimente** aus.</span><span class="sxs-lookup"><span data-stu-id="8d497-116">On the left side of the **Settings** pane, choose the **Experiments** section.</span></span>  
    
    :::image type="complex" source="./media/experiments-devtools.msft.png" alt-text="Liste der Experimente in den devtools-Einstellungen" lightbox="./media/experiments-devtools.msft.png":::
       <span data-ttu-id="8d497-118">Liste der Experimente in den devtools- **Einstellungen**</span><span class="sxs-lookup"><span data-stu-id="8d497-118">List of experiments in DevTools **Settings**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="8d497-119">Scrollen Sie auf der Seite **Experimente** durch die Liste aller verfügbaren experimentellen Features, und aktivieren Sie das Kontrollkästchen neben den einzelnen Features, die Sie testen möchten.</span><span class="sxs-lookup"><span data-stu-id="8d497-119">On the **Experiments** page, scroll through the list of all available experimental features and choose the checkbox next to each feature that you want to test.</span></span>  
1.  <span data-ttu-id="8d497-120">Schließen Sie die Microsoft Edge-devtools, und öffnen Sie Sie erneut.</span><span class="sxs-lookup"><span data-stu-id="8d497-120">Close and reopen Microsoft Edge DevTools.</span></span>  
    
> [!NOTE]
> <span data-ttu-id="8d497-121">Experimentelle Features werden ständig aktualisiert, was zu Leistungsproblemen führen kann.</span><span class="sxs-lookup"><span data-stu-id="8d497-121">Experimental features are constantly being updated and may cause performance issues.</span></span>  <span data-ttu-id="8d497-122">Wenn Sie ein experimentelles Feature deaktivieren möchten, öffnen Sie die Seite **Experimente** , und deaktivieren Sie das Kontrollkästchen des experimentellen Features, das Sie deaktivieren möchten.</span><span class="sxs-lookup"><span data-stu-id="8d497-122">To turn off an experimental feature, open the **Experiments** page and clear the checkbox of the experimental feature that you want to turn off.</span></span>  

## <span data-ttu-id="8d497-123">Hervorgehobene experimentelle Features</span><span class="sxs-lookup"><span data-stu-id="8d497-123">Highlighted experimental features</span></span>  

<span data-ttu-id="8d497-124">In den folgenden Abschnitten werden die neuen experimentellen Features beschrieben, die in Microsoft Edge zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="8d497-124">The following sections describe the new experimental features that are available in Microsoft Edge.</span></span>  

| <span data-ttu-id="8d497-125">Experimentelle Funktion</span><span class="sxs-lookup"><span data-stu-id="8d497-125">Experimental feature</span></span> | <span data-ttu-id="8d497-126">Microsoft Edge-Version</span><span class="sxs-lookup"><span data-stu-id="8d497-126">Microsoft Edge version</span></span> |  
|:--- |:--- |  
| [<span data-ttu-id="8d497-127">Emulation: Unterstützung des Dual-Screen-Modus</span><span class="sxs-lookup"><span data-stu-id="8d497-127">Emulation: Support dual screen mode</span></span>](#emulation-support-dual-screen-mode) | <span data-ttu-id="8d497-128">84 oder höher</span><span class="sxs-lookup"><span data-stu-id="8d497-128">84 or later</span></span> |  
| [<span data-ttu-id="8d497-129">Debuggen von neuen CSS-Raster Features aktivieren</span><span class="sxs-lookup"><span data-stu-id="8d497-129">Enable new CSS grid debugging features</span></span>](#enable-new-css-grid-debugging-features) | <span data-ttu-id="8d497-130">85 oder höher</span><span class="sxs-lookup"><span data-stu-id="8d497-130">85 or later</span></span> |  
| [<span data-ttu-id="8d497-131">Aktivieren der Unterstützung für das Verschieben von Tabstopps zwischen Bereichen</span><span class="sxs-lookup"><span data-stu-id="8d497-131">Enable support to move tabs between panels</span></span>](#enable-support-to-move-tabs-between-panels) | <span data-ttu-id="8d497-132">85 oder höher</span><span class="sxs-lookup"><span data-stu-id="8d497-132">85 or later</span></span> |  
| [<span data-ttu-id="8d497-133">Webhint aktivieren</span><span class="sxs-lookup"><span data-stu-id="8d497-133">Enable webhint</span></span>](#enable-webhint) | <span data-ttu-id="8d497-134">85 oder höher</span><span class="sxs-lookup"><span data-stu-id="8d497-134">85 or later</span></span> |  
| [<span data-ttu-id="8d497-135">Aktivieren der Netzwerk Konsole</span><span class="sxs-lookup"><span data-stu-id="8d497-135">Enable Network Console</span></span>](#enable-network-console) | <span data-ttu-id="8d497-136">85 oder höher</span><span class="sxs-lookup"><span data-stu-id="8d497-136">85 or later</span></span> |  
| [<span data-ttu-id="8d497-137">Viewer für Quellreihenfolge</span><span class="sxs-lookup"><span data-stu-id="8d497-137">Source Order Viewer</span></span>](#source-order-viewer) | <span data-ttu-id="8d497-138">86 oder höher</span><span class="sxs-lookup"><span data-stu-id="8d497-138">86 or later</span></span> |  
| [<span data-ttu-id="8d497-139">Aktivieren des Tasten Kombinations-Editors</span><span class="sxs-lookup"><span data-stu-id="8d497-139">Enable keyboard shortcut editor</span></span>](#enable-keyboard-shortcut-editor) | <span data-ttu-id="8d497-140">87 oder höher</span><span class="sxs-lookup"><span data-stu-id="8d497-140">87 or later</span></span> |  
| [<span data-ttu-id="8d497-141">Aktivieren von zusammengesetzten Layern in der 3D-Ansicht</span><span class="sxs-lookup"><span data-stu-id="8d497-141">Turn on Composited Layers in 3D View</span></span>](#turn-on-composited-layers-in-3d-view) | <span data-ttu-id="8d497-142">87 oder höher</span><span class="sxs-lookup"><span data-stu-id="8d497-142">87 or later</span></span> |  

### <span data-ttu-id="8d497-143">Emulation: Unterstützung des Dual-Screen-Modus</span><span class="sxs-lookup"><span data-stu-id="8d497-143">Emulation: Support dual screen mode</span></span>  

<span data-ttu-id="8d497-144">Bietet zusätzliche Features zum Emulieren von zwei neuen Dual-Screen-und faltbaren Geräten in Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="8d497-144">Provides additional features for emulating two new dual-screen and foldable devices in Microsoft Edge.</span></span>  

*   [<span data-ttu-id="8d497-145">Surface Duo</span><span class="sxs-lookup"><span data-stu-id="8d497-145">Surface Duo</span></span>][SurfaceDevicesDuo]  
*   [<span data-ttu-id="8d497-146">Samsung Galaxy Fold</span><span class="sxs-lookup"><span data-stu-id="8d497-146">Samsung Galaxy Fold</span></span>][SamsungMobileGalaxyFold]  
    
<span data-ttu-id="8d497-147">Emulieren Sie die Geräte, und wechseln Sie zwischen den folgenden Haltungen.</span><span class="sxs-lookup"><span data-stu-id="8d497-147">Emulate the devices and toggle between the following postures.</span></span>  

*   <span data-ttu-id="8d497-148">Einzelbild-oder gefaltete Haltung</span><span class="sxs-lookup"><span data-stu-id="8d497-148">single-screen or folded posture</span></span>  
*   <span data-ttu-id="8d497-149">Dual-Screen-oder entfaltete Haltung</span><span class="sxs-lookup"><span data-stu-id="8d497-149">dual-screen or unfolded posture</span></span>  
    
<span data-ttu-id="8d497-150">[Aktivieren Sie experimentelle Webplattform-APIs](#enable-experimental-apis) , und verwenden Sie das [Feature "CSS-Medien Bildschirm übergreifend"][DualScreenDocsCssMedia] und die [JavaScript-getWindowSegments-API][DualScreenDocsJSAPI] , um Ihre Website \ (oder App \) für Dual-Screen-und faltbare Geräte zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="8d497-150">[Enable experimental Web Platform APIs](#enable-experimental-apis) and use the [CSS media screen-spanning feature][DualScreenDocsCssMedia] and [JavaScript getWindowSegments API][DualScreenDocsJSAPI] to enhance your website \(or app\) for dual-screen and foldable devices.</span></span>  

:::image type="complex" source="./media/experiments-surface-duo-emulation.msft.png" alt-text="Emulieren von Surface Duo in Microsoft Edge" lightbox="./media/experiments-surface-duo-emulation.msft.png":::  
   <span data-ttu-id="8d497-152">Emulieren von Surface Duo in Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="8d497-152">Emulate Surface Duo in Microsoft Edge</span></span>  
:::image-end:::  

#### <span data-ttu-id="8d497-153">Aktivieren von experimentellen APIs</span><span class="sxs-lookup"><span data-stu-id="8d497-153">Enable experimental APIs</span></span>  

<span data-ttu-id="8d497-154">Aktivieren Sie das Kennzeichen in Microsoft Edge, um das [Feature "CSS-Medien Bildschirm übergreifend"][DualScreenDocsCssMedia] und die [JavaScript-getWindowSegments-API][DualScreenDocsJSAPI]zu verwenden `Experimental Web Platform features` .</span><span class="sxs-lookup"><span data-stu-id="8d497-154">To use the [CSS media screen-spanning feature][DualScreenDocsCssMedia] and [JavaScript getWindowSegments API][DualScreenDocsJSAPI], turn on the `Experimental Web Platform features` flag in Microsoft Edge.</span></span>  <span data-ttu-id="8d497-155">Führen Sie die folgenden Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="8d497-155">Complete the following steps.</span></span>  

1.  <span data-ttu-id="8d497-156">Navigieren Sie zu `edge://flags` .</span><span class="sxs-lookup"><span data-stu-id="8d497-156">Navigate to `edge://flags`.</span></span>  
1.  <span data-ttu-id="8d497-157">Geben Sie im Textfeld **Such Kennzeichnungen** `Experimental Web Platform features` das Flag **experimental Web Platform Features** ein, und ändern Sie **deaktiviert** in **aktiviert**.</span><span class="sxs-lookup"><span data-stu-id="8d497-157">In the **Search flags** textbox, enter `Experimental Web Platform features`, choose the **Experimental Web Platform features** flag, and change **Disabled** to **Enabled**.</span></span>  
1.  <span data-ttu-id="8d497-158">Starten Sie Microsoft Edge neu.</span><span class="sxs-lookup"><span data-stu-id="8d497-158">Restart Microsoft Edge.</span></span>  
    
:::image type="complex" source="./media/experiments-dual-screen-emulation-edge-flags.msft.png" alt-text="Aktivieren des Kennzeichens "experimentelle Webplattform-Features"" lightbox="./media/experiments-dual-screen-emulation.msft.png":::
   <span data-ttu-id="8d497-160">Aktivieren des Kennzeichens "experimentelle Webplattform-Features"</span><span class="sxs-lookup"><span data-stu-id="8d497-160">Enable the Experimental Web Platform features flag</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="8d497-161">Wenn Sie CSS- [medienabfragen][DualScreenDocsCssMedia] oder die [JavaScript Windows-Segment Aufzählungs-API][DualScreenDocsJSAPI] verwenden, um Ihre Website oder App für das [Surface Duo][SurfaceDevicesDuo]zu verbessern, müssen Sie auch das Kennzeichen **experimentelle Webplattform-Features** in der [Android-App für Microsoft Edge][GooglePlayMicrosoftEdge] auf Ihrem [Surface Duo][SurfaceDevicesDuo] -Gerät aktivieren.</span><span class="sxs-lookup"><span data-stu-id="8d497-161">If you are using [CSS media queries][DualScreenDocsCssMedia] or the [JavaScript Windows Segment Enumeration API][DualScreenDocsJSAPI] to enhance your website or app for the [Surface Duo][SurfaceDevicesDuo], you must also enable the **Experimental Web Platform features** flag in the [Android Microsoft Edge app][GooglePlayMicrosoftEdge] on your [Surface Duo][SurfaceDevicesDuo] device.</span></span>  
> 
> <span data-ttu-id="8d497-162">Wenn das Flag für **experimentelle Webplattform-Features** in der Microsoft Edge-App für [Desktops][MicrosoftEdge] aktiviert ist und in der [Android-App für Microsoft Edge][GooglePlayMicrosoftEdge]deaktiviert ist, entspricht das Verhalten Ihrer Website oder App im Surface Duo-Emulator in Desktop Microsoft Edge nicht der [Android-App "Microsoft Edge][GooglePlayMicrosoftEdge] " auf [Surface Duo][SurfaceDevicesDuo].</span><span class="sxs-lookup"><span data-stu-id="8d497-162">If the **Experimental Web Platform features** flag is enabled in [desktop Microsoft Edge][MicrosoftEdge] and disabled in the [Android Microsoft Edge app][GooglePlayMicrosoftEdge], the behavior of your website or app in the Surface Duo emulator in desktop Microsoft Edge does not match with the [Android Microsoft Edge app][GooglePlayMicrosoftEdge] on [Surface Duo][SurfaceDevicesDuo].</span></span>  <span data-ttu-id="8d497-163">Stellen Sie sicher, dass die Flags für Android und Desktop Microsoft Edge übereinstimmen, um den Surface Duo-Emulator erfolgreich im [Desktop Microsoft Edge][MicrosoftEdge]zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="8d497-163">Ensure that the flags are matching across Android and desktop Microsoft Edge to successfully use the Surface Duo emulator in [desktop Microsoft Edge][MicrosoftEdge].</span></span>  

#### <span data-ttu-id="8d497-164">Testen auf faltbaren und Dual-Screen-Geräten</span><span class="sxs-lookup"><span data-stu-id="8d497-164">Testing on foldable and dual-screen devices</span></span>  

<span data-ttu-id="8d497-165">Wenn Sie das [Surface Duo][SurfaceDevicesDuo] in einer Haltung mit zwei Bildschirmen in Microsoft Edge emulieren, wird die Naht \ (der Abstand zwischen den beiden Bildschirmen \) über Ihre Website oder App gezeichnet.</span><span class="sxs-lookup"><span data-stu-id="8d497-165">When you emulate the [Surface Duo][SurfaceDevicesDuo] in a dual-screen posture in Microsoft Edge, the seam \(the space between the two screens\) is drawn over your website or app.</span></span>  

<span data-ttu-id="8d497-166">Die emulierte Anzeige entspricht der Darstellung Ihrer Website \ (oder App \) in der [Microsoft Edge Android-App][GooglePlayMicrosoftEdge] , die auf [Surface Duo][SurfaceDevicesDuo]ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8d497-166">The emulated display matches the way your website \(or app\) renders in the [Microsoft Edge Android app][GooglePlayMicrosoftEdge] running on [Surface Duo][SurfaceDevicesDuo].</span></span>  <span data-ttu-id="8d497-167">Möglicherweise müssen Sie Ihre Website aktualisieren \ (oder App \), damit Sie besser entlang der Naht angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="8d497-167">You may have to update your website \(or app\) to display better along the seam.</span></span>  <span data-ttu-id="8d497-168">Weitere Informationen zum Anpassen Ihrer Website \ (oder App \) an die Naht finden Sie unter [Arbeiten mit der Naht][DualScreenIntroductionHowWorkSeam].</span><span class="sxs-lookup"><span data-stu-id="8d497-168">For more information about adapting your website \(or app\) to the seam, navigate to [How to work with the seam][DualScreenIntroductionHowWorkSeam].</span></span>  

<span data-ttu-id="8d497-169">Die [Gerätesymbolleiste][DevtoolsDeviceModeIndexSimulateMobileViewport] verfügt über zusätzliche Features, die Sie beim Testen Ihrer Website oder app in verschiedenen Haltungen und Ausrichtungen unterstützen.</span><span class="sxs-lookup"><span data-stu-id="8d497-169">The [Device Toolbar][DevtoolsDeviceModeIndexSimulateMobileViewport] has additional features to help you test your website or app in multiple postures and orientations.</span></span>  <span data-ttu-id="8d497-170">Wählen Sie **drehen** \ ( ![ drehen ][ImageRotateIcon] \) aus, um das Ansichtsfenster in Querformat zu drehen.</span><span class="sxs-lookup"><span data-stu-id="8d497-170">Choose **Rotate** \(![Rotate][ImageRotateIcon]\) to rotate the viewport to landscape orientation.</span></span> <span data-ttu-id="8d497-171">Kombinieren Sie das Feature mit **Span** \ ( ![ Span ][ImageSpanIcon] \), um zwischen Einzelbildschirm-oder gefalteten und Dual-Screen-oder entfalteten Haltungen umzuschalten.</span><span class="sxs-lookup"><span data-stu-id="8d497-171">Combine the feature with **Span** \(![Span][ImageSpanIcon]\) to toggle between single-screen or folded and dual-screen or unfolded postures.</span></span>  <span data-ttu-id="8d497-172">Zusammen können die Features das Testen Ihrer Website oder app in allen vier möglichen Haltungen und Ausrichtungen ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="8d497-172">Together, the features enable testing your website or app in all four possible postures and orientations.</span></span>  

:::image type="complex" source="./media/experiments-dual-screen-emulation-rotate-span.msft.png" alt-text="Matrix von Haltungen und Ausrichtungen für Dual-Screen-und faltbare Geräte" lightbox="./media/experiments-dual-screen-emulation-rotate-span.msft.png":::
   <span data-ttu-id="8d497-174">Matrix von Haltungen und Ausrichtungen für Dual-Screen-und faltbare Geräte</span><span class="sxs-lookup"><span data-stu-id="8d497-174">Matrix of postures and orientations for dual-screen and foldable devices</span></span>  
:::image-end:::  

<span data-ttu-id="8d497-175">Das **Feature "experimentelle Webplattform-Features** \ ( ![ ExperimentalApis ][ImageExperimentalApisIcon] \)" zeigt den Zustand des Kennzeichens " **experimentelle Web Platform Features** " an.</span><span class="sxs-lookup"><span data-stu-id="8d497-175">The **Experimental Web Platform features** \(![ExperimentalApis][ImageExperimentalApisIcon]\) icon displays the state of the **Experimental Web Platform features** flag.</span></span>  <span data-ttu-id="8d497-176">Wenn die Kennzeichnung aktiviert ist, ist das Symbol hervorgehoben.</span><span class="sxs-lookup"><span data-stu-id="8d497-176">If the flag is turned on, the icon is highlighted.</span></span>  <span data-ttu-id="8d497-177">Wenn die Kennzeichnung deaktiviert ist, wird das Symbol nicht hervorgehoben.</span><span class="sxs-lookup"><span data-stu-id="8d497-177">If the flag is turned off, the icon is not highlighted.</span></span>  <span data-ttu-id="8d497-178">Um die Kennzeichnung zu aktivieren oder zu deaktivieren, navigieren Sie zu `edge://flags` der Kennzeichnung, und aktivieren Sie Sie.</span><span class="sxs-lookup"><span data-stu-id="8d497-178">To turn on \(or off\) the flag, navigate to `edge://flags` and toggle the flag.</span></span>  

<!-- Commenting out until the icon issue is fixed in Edge Canary
The **Experimental Web Platform features** \(![ExperimentalApis][ImageExperimentalApisIcon]\) icon displays the state of the **Experimental Web Platform features** flag.  If the flag is turned on, the icon is highlighted.  If the flag is turned off, the icon is not highlighted.  To turn on \(or off\) the flag, either choose the icon or navigate to `edge://flags` and toggle the flag.   -->  

<span data-ttu-id="8d497-179">Hier sind weitere Ressourcen, die Ihnen bei der Optimierung Ihrer Website (oder App \) für Dual-Screen-Geräte helfen können.</span><span class="sxs-lookup"><span data-stu-id="8d497-179">Here are additional resources that may help you enhance your website \(or app\) for dual-screen devices.</span></span>  

*   <span data-ttu-id="8d497-180">Weitere Informationen zur Web-Entwicklung auf Dual-Screen-Geräten finden Sie unter [Dual-Screen-Web-Erlebnisse][DualScreenWebIndex].</span><span class="sxs-lookup"><span data-stu-id="8d497-180">For more information about web development on dual-screen devices, navigate to [Dual-screen web experiences][DualScreenWebIndex].</span></span>  
*   <span data-ttu-id="8d497-181">Installieren Sie den [Surface Duo-Emulator][DualScreenAndroidUseEmulator].</span><span class="sxs-lookup"><span data-stu-id="8d497-181">Install the [Surface Duo emulator][DualScreenAndroidUseEmulator].</span></span>  <span data-ttu-id="8d497-182">Sie unterscheidet sich vom Emulator in Microsoft Edge, emuliert das Surface Duo mit Android und ist in [Android Studio][AndroidDeveloperStudio]integriert.</span><span class="sxs-lookup"><span data-stu-id="8d497-182">It is different from the emulator in Microsoft Edge, emulates the Surface Duo running Android, and integrates with [Android Studio][AndroidDeveloperStudio].</span></span>  <span data-ttu-id="8d497-183">Wenn Sie weitere Informationen erhalten möchten, navigieren Sie zu [Surface Duo SDK][DualScreenAndroidGetDuoSdk].</span><span class="sxs-lookup"><span data-stu-id="8d497-183">For more information, navigate to [Get the Surface Duo SDK][DualScreenAndroidGetDuoSdk].</span></span>  
    
> [!NOTE]
> <span data-ttu-id="8d497-184">Die folgende Liste enthält aktuelle bekannte Probleme.</span><span class="sxs-lookup"><span data-stu-id="8d497-184">The following is a list of current known issues.</span></span>  
> 
> *   <span data-ttu-id="8d497-185">Wenn Sie einen [Microsoft Remote Desktop-Client][RemoteDesktopClientDocs] verwenden, um eine Verbindung mit einem Remote-PC herzustellen und das [Surface Duo][SurfaceDevicesDuo] oder [Samsung Galaxy Fold][SamsungMobileGalaxyFold]zu emulieren, kann der Mauszeiger wackeln oder Stottern.</span><span class="sxs-lookup"><span data-stu-id="8d497-185">When using a [Microsoft Remote Desktop client][RemoteDesktopClientDocs] to connect to a remote PC and emulate the [Surface Duo][SurfaceDevicesDuo] or [Samsung Galaxy Fold][SamsungMobileGalaxyFold], the pointer may shake or stutter.</span></span>  <span data-ttu-id="8d497-186">Wenn das Problem auftritt, senden Sie [uns Feedback](#providing-feedback-on-experimental-features).</span><span class="sxs-lookup"><span data-stu-id="8d497-186">If you run into the issue, [send feedback](#providing-feedback-on-experimental-features).</span></span>  

### <span data-ttu-id="8d497-187">Debuggen von neuen CSS-Raster Features aktivieren</span><span class="sxs-lookup"><span data-stu-id="8d497-187">Enable new CSS grid debugging features</span></span>  

<span data-ttu-id="8d497-188">Dieses experimentelle Feature bietet eine Reihe neuer Visualisierungen, die Ihnen beim Debuggen von CSS-Rasterlayouts helfen.</span><span class="sxs-lookup"><span data-stu-id="8d497-188">This experimental feature provides a number of new visualizations to help you debug CSS grid layouts.</span></span>  <span data-ttu-id="8d497-189">Wenn Sie eine Vorschau der neuesten experimentellen Features anzeigen möchten, [Aktivieren Sie dieses Experiment](#turn-on-experimental-features) , und laden Sie devtools.</span><span class="sxs-lookup"><span data-stu-id="8d497-189">To preview the latest experimental features, [enable this experiment](#turn-on-experimental-features) and reload DevTools.</span></span>  <span data-ttu-id="8d497-190">Dieses Experiment ist in Microsoft Edge, Version 87 oder höher, standardmäßig aktiviert.</span><span class="sxs-lookup"><span data-stu-id="8d497-190">This experiment is on by default in Microsoft Edge version 87 or later.</span></span>  

#### <span data-ttu-id="8d497-191">Anzeigen von in-Hover-Raster Überlagerungen mit dem Tool "überprüfen"</span><span class="sxs-lookup"><span data-stu-id="8d497-191">Viewing on-hover grid overlays with the Inspect tool</span></span>  

<span data-ttu-id="8d497-192">Das Tool "über **prüfen** " bietet eine schnelle Möglichkeit, CSS-Rasterlayouts in einer Website zu erkennen und zu visualisieren, indem Sie mit der Maus darauf zeigen.</span><span class="sxs-lookup"><span data-stu-id="8d497-192">The **Inspect** tool provides a quick way to identify and visualize CSS Grid layouts in a website by hovering over them with the mouse.</span></span>  <span data-ttu-id="8d497-193">Klicken Sie **Inspect** ![ ](./media/inspect-icon.msft.png) in der oberen linken Ecke von devtools auf das Symbol inspizieren \ (Inspect \).</span><span class="sxs-lookup"><span data-stu-id="8d497-193">Choose the **Inspect** \(![Inspect](./media/inspect-icon.msft.png)\) icon in the top-left corner of DevTools.</span></span>  <span data-ttu-id="8d497-194">Zeigen Sie dann auf der Website, die Sie Debuggen, auf ein Grid-Element.</span><span class="sxs-lookup"><span data-stu-id="8d497-194">Then, hover over a Grid element on the website you are debugging.</span></span>  <span data-ttu-id="8d497-195">Umrisse werden um das Raster herum angezeigt, und Schattierung zeigt die Position von Raster Lücken an, sofern vorhanden.</span><span class="sxs-lookup"><span data-stu-id="8d497-195">Outlines are displayed around the grid, and shading indicates the location of grid gaps if present.</span></span>  

:::image type="complex" source="./media/grid-inspect.msft.png" alt-text="Anzeigen von Rastern mit dem Tool "überprüfen"" lightbox="./media/grid-inspect.msft.png":::
   <span data-ttu-id="8d497-197">Anzeigen von Rastern mit dem Tool "überprüfen"</span><span class="sxs-lookup"><span data-stu-id="8d497-197">Viewing grids with the Inspect tool</span></span>  
:::image-end:::  

#### <span data-ttu-id="8d497-198">Anzeigen beständiger Raster Überlagerungen</span><span class="sxs-lookup"><span data-stu-id="8d497-198">Viewing persistent grid overlays</span></span>  

<span data-ttu-id="8d497-199">In Microsoft Edge, Version 86 oder höher, bietet das experimentelle CSS-Raster Feature auch die Option zum Aktivieren beständiger Raster Überlagerungen.</span><span class="sxs-lookup"><span data-stu-id="8d497-199">In Microsoft Edge version 86 or later, the experimental CSS grid feature also offers the option to enable persistent Grid overlays.</span></span>  <span data-ttu-id="8d497-200">Die persistenten Overlays bieten mehrere Vorteile.</span><span class="sxs-lookup"><span data-stu-id="8d497-200">The persistent overlays provide several benefits.</span></span>  

*   <span data-ttu-id="8d497-201">Die beständigen Overlays bleiben auf der Seite sichtbar, während Sie scrollen, die Maus bewegen und andere Features des devtools verwenden.</span><span class="sxs-lookup"><span data-stu-id="8d497-201">The persistent overlays remain visible on the page as you scroll, move your mouse, and use other features of the DevTools.</span></span>  
*   <span data-ttu-id="8d497-202">Mehrere persistente Overlays können gleichzeitig aktiviert werden, sodass Sie mehrere Rasterlayouts auf einmal überprüfen können.</span><span class="sxs-lookup"><span data-stu-id="8d497-202">Multiple persistent overlays can be enabled at the same time, allowing you to review several grid layouts at once.</span></span>  
*   <span data-ttu-id="8d497-203">Beständige Overlays bieten viele Konfigurationsoptionen, wie das ein-oder Ausblenden von Namen im Rasterbereich, Rasterabstände, nach Titel Größen usw.</span><span class="sxs-lookup"><span data-stu-id="8d497-203">Persistent overlays offer many configuration options, such as hiding or showing names in the grid area, grid gaps, track sizes, and so on.</span></span>  
    
<span data-ttu-id="8d497-204">Zwei Möglichkeiten zum Umschalten einer beständigen Raster Überlagerung</span><span class="sxs-lookup"><span data-stu-id="8d497-204">The two ways to toggle a persistent grid overlay.</span></span>  

*   <span data-ttu-id="8d497-205">Wählen Sie das Oval- **Raster** Symbol neben einem Rasterelement aus, das in der DOM-Struktur des **Elements** -Tools angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="8d497-205">Choose the **Grid** oval icon next to any Grid element shown in the DOM tree of the **Elements** tool.</span></span>  
    
    :::image type="complex" source="./media/grid-adorner.msft.png" alt-text="Symbol ' Raster Oval ' im Tool ' Elemente '" lightbox="./media/grid-adorner.msft.png":::
       <span data-ttu-id="8d497-207">Symbol ' Raster Oval ' im Tool ' **Elemente** '</span><span class="sxs-lookup"><span data-stu-id="8d497-207">Grid oval icon in **Elements** tool</span></span>  
    :::image-end:::  
    
*   <span data-ttu-id="8d497-208">Öffnen Sie den neuen **LayoutPanel** -Bereich, der sich im Tool Elemente befindet, und aktivieren Sie das Kontrollkästchen neben den einzelnen Rasterelementen, die Sie markieren möchten.</span><span class="sxs-lookup"><span data-stu-id="8d497-208">Open the new **Layout** panel located in the Elements tool, and choose the checkbox next to each Grid element you want to highlight.</span></span>  
    
    :::image type="complex" source="./media/grid-layout-zoom.msft.png" alt-text="Layoutpanel in devtools" lightbox="./media/grid-layout-zoom.msft.png":::
       <span data-ttu-id="8d497-210">**LayoutPanel** in devtools</span><span class="sxs-lookup"><span data-stu-id="8d497-210">**Layout** panel in DevTools</span></span>  
    :::image-end:::  
    
#### <span data-ttu-id="8d497-211">Konfigurieren von persistenten Overlays</span><span class="sxs-lookup"><span data-stu-id="8d497-211">Configuring persistent overlays</span></span>  

<span data-ttu-id="8d497-212">In Microsoft Edge, Version 86 oder höher, befindet sich das neue **LayoutPanel** -Element neben den Registerkarten **"Formatvorlagen** " und " **berechnet** " im Tool " **Elemente** ".</span><span class="sxs-lookup"><span data-stu-id="8d497-212">In Microsoft Edge version 86 or later, the new **Layout** panel is located in the **Elements** tool alongside the **Styles** and **Computed** tabs.</span></span>  <span data-ttu-id="8d497-213">Im **LayoutPanel** werden die Konfigurationsoptionen für persistente Overlays Oberflächen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="8d497-213">The **Layout** panel surfaces configuration options for persistent overlays.</span></span>  

:::image type="complex" source="./media/experiments-grid.msft.png" alt-text="CSS-Raster Debugging-Feature" lightbox="./media/experiments-grid.msft.png":::
   <span data-ttu-id="8d497-215">CSS-Raster Debugging-Feature</span><span class="sxs-lookup"><span data-stu-id="8d497-215">CSS grid debugging feature</span></span>  
:::image-end:::  

### <span data-ttu-id="8d497-216">Aktivieren der Unterstützung für das Verschieben von Tabstopps zwischen Bereichen</span><span class="sxs-lookup"><span data-stu-id="8d497-216">Enable support to move tabs between panels</span></span>  

<span data-ttu-id="8d497-217">Normalerweise werden Tools wie **Elemente** und **Netzwerke** nur im Hauptbereich geöffnet, der sich am oberen Rand des devtools befindet.</span><span class="sxs-lookup"><span data-stu-id="8d497-217">Normally, tools such as **Elements** and **Network** may only open in the main panel that is located at the top of the DevTools.</span></span>  <span data-ttu-id="8d497-218">Tools wie **3D-Ansicht** und **Probleme** , die normalerweise nur in der **Schublade** angezeigt werden, die sich am unteren Rand des devtools befindet.</span><span class="sxs-lookup"><span data-stu-id="8d497-218">Tools like **3D View** and **Issues** which normally only open in the **Drawer** panel that is located at the bottom of the DevTools.</span></span>  <span data-ttu-id="8d497-219">Nachdem Sie das Experiment ausgewählt haben, können Sie die Tools zwischen dem oberen und unteren Bereich verschieben.</span><span class="sxs-lookup"><span data-stu-id="8d497-219">After you choose the experiment, you may move tools between the top and bottom panels.</span></span>  <span data-ttu-id="8d497-220">Wenn Sie ein Tool verschieben möchten, zeigen Sie auf die Registerkarte, öffnen Sie das Kontextmenü \ (Klicken Sie mit der rechten Maustaste auf \), und wählen Sie **nach oben** oder **nach unten**verschieben aus.</span><span class="sxs-lookup"><span data-stu-id="8d497-220">To move a tool, hover on the tab, open the contextual menu \(right-click\), and choose **Move to top** or **Move to bottom**.</span></span>   <span data-ttu-id="8d497-221">Mit diesem Experiment können Sie Ihr devtools-Layout anpassen.</span><span class="sxs-lookup"><span data-stu-id="8d497-221">This experiment allows you to customize your DevTools layout.</span></span>  <span data-ttu-id="8d497-222">Zum ein-oder Ausblenden des **Einschub** Panels wählen Sie `Escape` .</span><span class="sxs-lookup"><span data-stu-id="8d497-222">To show or hide the **Drawer** panel, select `Escape`.</span></span>  

:::image type="complex" source="./media/experiments-move-panels.msft.png" alt-text="Verschieben von Tabstopps zwischen Bereichen" lightbox="./media/experiments-move-panels.msft.png":::
   <span data-ttu-id="8d497-224">Verschieben von Tabstopps zwischen Bereichen</span><span class="sxs-lookup"><span data-stu-id="8d497-224">Moving tabs between panels</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 85 and later.  -->  

### <span data-ttu-id="8d497-225">Webhint aktivieren</span><span class="sxs-lookup"><span data-stu-id="8d497-225">Enable webhint</span></span>  

<span data-ttu-id="8d497-226">[webhint][WebhintMain] ist ein Open-Source-Tool, das Echtzeitfeedback für Websites und lokale Webseiten bietet.</span><span class="sxs-lookup"><span data-stu-id="8d497-226">[webhint][WebhintMain] is an open-source tool that provides real-time feedback for websites and local web pages.</span></span>  <span data-ttu-id="8d497-227">Der Typ des Feedbacks, das von [webhint][WebhintMain]bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="8d497-227">The type of feedback provided by [webhint][WebhintMain].</span></span>  

*   <span data-ttu-id="8d497-228">Bedienungshilfen</span><span class="sxs-lookup"><span data-stu-id="8d497-228">accessibility</span></span>  
*   <span data-ttu-id="8d497-229">browserübergreifende Kompatibilität</span><span class="sxs-lookup"><span data-stu-id="8d497-229">cross-browser compatibility</span></span>  
*   <span data-ttu-id="8d497-230">Sicherheit</span><span class="sxs-lookup"><span data-stu-id="8d497-230">security</span></span>  
*   <span data-ttu-id="8d497-231">Leistung</span><span class="sxs-lookup"><span data-stu-id="8d497-231">performance</span></span>  
*   <span data-ttu-id="8d497-232">Progressive Web-Apps (PWAs)</span><span class="sxs-lookup"><span data-stu-id="8d497-232">Progressive Web Apps (PWAs)</span></span>  
*   <span data-ttu-id="8d497-233">andere häufig auftretende Probleme mit der Web-Entwicklung</span><span class="sxs-lookup"><span data-stu-id="8d497-233">other common web development issues</span></span>  
    
<span data-ttu-id="8d497-234">Das [webhint][WebhintMain] -Experiment zeigt das webhint-Feedback im Bereich " [Probleme][DevtoolsIssues] " an.</span><span class="sxs-lookup"><span data-stu-id="8d497-234">The [webhint][WebhintMain] experiment displays the webhint feedback in the [Issues][DevtoolsIssues] panel.</span></span>  <span data-ttu-id="8d497-235">Wählen Sie ein Problem aus, um die Lösungsdokumentation und eine Liste der betroffenen Ressourcen auf Ihrer Website anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="8d497-235">Choose an issue to display solution documentation and a list of the affected resources on your website.</span></span>  <span data-ttu-id="8d497-236">Wählen Sie einen Ressourcen Link aus, um den entsprechenden Bereich für **Netzwerke**, **Quellen**oder **Elemente** in devtools zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="8d497-236">Choose a resource link to open the relevant **Network**, **Sources**, or **Elements** pane in DevTools.</span></span>  

:::image type="complex" source="./media/experiments-webhint.msft.png" alt-text="webhint-Feedback im Bereich "Probleme"" lightbox="./media/experiments-webhint.msft.png":::
   <span data-ttu-id="8d497-238">webhint-Feedback im Bereich " **Probleme** "</span><span class="sxs-lookup"><span data-stu-id="8d497-238">webhint feedback in the **Issues** panel</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 85 and later.  -->  

### <span data-ttu-id="8d497-239">Aktivieren der Netzwerk Konsole</span><span class="sxs-lookup"><span data-stu-id="8d497-239">Enable Network Console</span></span>  

<span data-ttu-id="8d497-240">**Netzwerk Konsole** ist der Arbeitstitel eines Experiments, um synthetische Netzwerkanforderungen über HTTP zu stellen.</span><span class="sxs-lookup"><span data-stu-id="8d497-240">**Network Console** is the working title of an experiment to make synthetic network requests over HTTP.</span></span>  <span data-ttu-id="8d497-241">Sie können das **Netzwerkkonsolen** Experiment verwenden, um Web-API-Anforderungen zu senden.</span><span class="sxs-lookup"><span data-stu-id="8d497-241">You may use the **Network Console** experiment to send web API requests.</span></span>  

<span data-ttu-id="8d497-242">Nachdem Sie das Experiment aktiviert haben, stellen Sie sicher, dass Sie das devtools erneut starten.</span><span class="sxs-lookup"><span data-stu-id="8d497-242">After enabling the experiment, ensure you restart the DevTools.</span></span>  <span data-ttu-id="8d497-243">Führen Sie die folgenden Schritte aus, um die **Netzwerk Konsole**zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="8d497-243">To use the **Network Console**, complete the following steps.</span></span>  

1.  <span data-ttu-id="8d497-244">Öffnen Sie den Bereich **Netzwerk** .</span><span class="sxs-lookup"><span data-stu-id="8d497-244">Open the **Network** pane.</span></span>  
1.  <span data-ttu-id="8d497-245">Suchen Sie die Netzwerkanforderung, die Sie ändern möchten, und senden Sie Sie erneut.</span><span class="sxs-lookup"><span data-stu-id="8d497-245">Find the network request that you want to change and resend.</span></span>  
1.  <span data-ttu-id="8d497-246">Öffnen Sie das Kontextmenü \ (Klicken Sie mit der rechten Maustaste auf \), und wählen Sie **Bearbeiten und wiedergeben**aus.</span><span class="sxs-lookup"><span data-stu-id="8d497-246">Open the contextual menu \(right-click\), and choose **Edit and Replay**.</span></span>  
1.  <span data-ttu-id="8d497-247">Wenn die **Netzwerk Konsole** geöffnet wird, bearbeiten Sie die Netzwerk Anforderungsinformationen.</span><span class="sxs-lookup"><span data-stu-id="8d497-247">When the **Network Console** opens, edit the network request information.</span></span>  
1.  <span data-ttu-id="8d497-248">Wählen Sie **senden**aus.</span><span class="sxs-lookup"><span data-stu-id="8d497-248">Choose **Send**.</span></span>  
    
:::image type="complex" source="./media/network-network-console.msft.png" alt-text="Netzwerk Konsole im Konsolen Einzug" lightbox="./media/network-network-console.msft.png":::
   <span data-ttu-id="8d497-250">**Netzwerk Konsole** im **Konsolen** Einzug</span><span class="sxs-lookup"><span data-stu-id="8d497-250">**Network Console** in the **Console** drawer</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 85 and later.  -->  

### <span data-ttu-id="8d497-251">Viewer für Quellreihenfolge</span><span class="sxs-lookup"><span data-stu-id="8d497-251">Source Order Viewer</span></span>  

<span data-ttu-id="8d497-252">Die **Quellauftrags Anzeige** ist ein Experiment, das die Reihenfolge der Elemente in der Seitenquelle anzeigt.</span><span class="sxs-lookup"><span data-stu-id="8d497-252">**Source Order Viewer** is an experiment that displays the order of elements in the page source.</span></span>  <span data-ttu-id="8d497-253">Die Anzeigereihenfolge auf dem Bildschirm kann von der Reihenfolge der Quelle abweichen, die die Bildschirmsprachausgabe und die Tastatur Benutzer verwirrt.</span><span class="sxs-lookup"><span data-stu-id="8d497-253">The on-screen display order may differ from the order of the source, which confuses screen reader and keyboard users.</span></span>  <span data-ttu-id="8d497-254">Verwenden Sie das Experiment der **Quellauftrags Anzeige** , um die Unterschiede zwischen der Anzeigereihenfolge auf dem Bildschirm und der Reihenfolge der Quelle zu finden.</span><span class="sxs-lookup"><span data-stu-id="8d497-254">Use the **Source Order Viewer** experiment to find the differences between on-screen display order and the order of the source.</span></span>  

<span data-ttu-id="8d497-255">Nachdem Sie das Experiment aktiviert haben, stellen Sie sicher, dass Sie das devtools erneut starten.</span><span class="sxs-lookup"><span data-stu-id="8d497-255">After enabling the experiment, ensure you restart the DevTools.</span></span>  <span data-ttu-id="8d497-256">Führen Sie die folgenden Schritte aus, um die **Quellauftrags Anzeige**zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="8d497-256">To use **Source Order Viewer**, complete the following steps.</span></span>  

1.  <span data-ttu-id="8d497-257">Öffnen Sie den Bereich **Elemente** .</span><span class="sxs-lookup"><span data-stu-id="8d497-257">Open the **Elements** pane.</span></span>  
1.  <span data-ttu-id="8d497-258">Öffnen Sie den Bereich " **Barrierefreiheit** " im Bereich "Schublade \" (unten).</span><span class="sxs-lookup"><span data-stu-id="8d497-258">Open the **Accessibility** pane in the drawer \(bottom\) panel.</span></span>  
1.  <span data-ttu-id="8d497-259">Wählen Sie im Abschnitt **Quellauftrags Anzeige** das Kontrollkästchen **Quellreihenfolge anzeigen** aus.</span><span class="sxs-lookup"><span data-stu-id="8d497-259">Under the **Source Order Viewer** section, choose the **Show Source Order** checkbox.</span></span>  
1.  <span data-ttu-id="8d497-260">Markieren Sie ein beliebiges HTML-Element, um ein Overlay anzuzeigen, das die Reihenfolge in der Seitenquelle enthält.</span><span class="sxs-lookup"><span data-stu-id="8d497-260">Highlight any HTML element to display an overlay that the order in the page source.</span></span>  
    
:::image type="complex" source="./media/experiments-source-order-viewer.msft.png" alt-text="Viewer für Quellreihenfolge im Bereich "Barrierefreiheit"" lightbox="./media/experiments-source-order-viewer.msft.png":::
   <span data-ttu-id="8d497-262">**Viewer für Quellreihenfolge** im Bereich " **Barrierefreiheit** "</span><span class="sxs-lookup"><span data-stu-id="8d497-262">**Source Order Viewer** in the **Accessibility** pane</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 86 and later.  -->  

### <span data-ttu-id="8d497-263">Aktivieren des Tasten Kombinations-Editors</span><span class="sxs-lookup"><span data-stu-id="8d497-263">Enable keyboard shortcut editor</span></span>

<span data-ttu-id="8d497-264">Wenn das Experiment " **Tastenkombinationen-Editor aktivieren** " aktiviert ist, können Sie jetzt Tastenkombinationen für jede Aktion im devtools anpassen.</span><span class="sxs-lookup"><span data-stu-id="8d497-264">With the **Enable keyboard shortcut editor** experiment turned on, you are now able to customize keyboard shortcuts for any action in the DevTools.</span></span>  <span data-ttu-id="8d497-265">Führen Sie die folgenden Schritte aus, um die Tastenkombination für eine bestimmte Aktion anzupassen.</span><span class="sxs-lookup"><span data-stu-id="8d497-265">To customize the keyboard shortcut for a specific action, complete the following steps.</span></span>  

1.  <span data-ttu-id="8d497-266">[Öffnen Sie devtools][DevtoolsOpenMain].</span><span class="sxs-lookup"><span data-stu-id="8d497-266">[Open DevTools][DevtoolsOpenMain].</span></span>  
1.  <span data-ttu-id="8d497-267">Öffnen Sie [Einstellungen][DevToolsCustomizeSettings].</span><span class="sxs-lookup"><span data-stu-id="8d497-267">Open [Settings][DevToolsCustomizeSettings].</span></span>
    *   <span data-ttu-id="8d497-268">Wählen Sie aus `Shift` + `?` .</span><span class="sxs-lookup"><span data-stu-id="8d497-268">Select `Shift`+`?`.</span></span>  
1.  <span data-ttu-id="8d497-269">Navigieren Sie zur Seite **Verknüpfungen** .</span><span class="sxs-lookup"><span data-stu-id="8d497-269">Navigate to the **Shortcuts** page.</span></span>  
1.  <span data-ttu-id="8d497-270">Wählen Sie die Aktion aus, die Sie anpassen möchten.</span><span class="sxs-lookup"><span data-stu-id="8d497-270">Choose the action you want to customize.</span></span>  
1.  <span data-ttu-id="8d497-271">Wählen Sie das Symbol **Bearbeiten** \ ( ![ EditKeyboardShortcut ][ImageEditKeyboardShortcutIcon] \) aus.</span><span class="sxs-lookup"><span data-stu-id="8d497-271">Choose the **Edit** \(![EditKeyboardShortcut][ImageEditKeyboardShortcutIcon]\) icon.</span></span>  
    
    :::image type="complex" source="./media/experiments-custom-keyboard-shortcuts-select-action.msft.png" alt-text="Auswählen der zu anpassenden Aktion auf der Seite "Verknüpfungen" in "Einstellungen"" lightbox="./media/experiments-custom-keyboard-shortcuts-select-action.msft.png":::
       <span data-ttu-id="8d497-273">Auswählen der zu anpassenden Aktion auf der Seite " **Verknüpfungen** " in " [Einstellungen][DevToolsCustomizeSettings] "</span><span class="sxs-lookup"><span data-stu-id="8d497-273">Choose the action to customize from the **Shortcuts** page in [Settings][DevToolsCustomizeSettings]</span></span>
    :::image-end:::  
    
1.  <span data-ttu-id="8d497-274">Wählen Sie auf der Tastatur die Tasten aus, die Sie an die Aktion binden möchten.</span><span class="sxs-lookup"><span data-stu-id="8d497-274">On the keyboard, select the keys you want to bind to the action.</span></span>
    
    :::image type="complex" source="./media/experiments-custom-keyboard-shortcuts-enter-key.msft.png" alt-text="Wählen Sie die Tasten aus, die Sie der Aktion zuweisen möchten." lightbox="./media/experiments-custom-keyboard-shortcuts-enter-key.msft.png":::
       <span data-ttu-id="8d497-276">Wählen Sie die Tasten aus, die Sie der Aktion zuweisen möchten.</span><span class="sxs-lookup"><span data-stu-id="8d497-276">Select the keys you want to assign to the action</span></span>
    :::image-end:::  
    
1.  <span data-ttu-id="8d497-277">Wenn Sie die neue Tastenkombination speichern möchten, wählen Sie das Häkchen \ (</span><span class="sxs-lookup"><span data-stu-id="8d497-277">To save your new keyboard shortcut, choose the checkmark \(</span></span>![CheckmarkKeyboardShortcut][ImageCheckmarkKeyboardShortcutIcon]<span data-ttu-id="8d497-279">\)-Symbol.</span><span class="sxs-lookup"><span data-stu-id="8d497-279">\) icon.</span></span>
    
    :::image type="complex" source="./media/experiments-custom-keyboard-shortcuts-save-shortcut.msft.png" alt-text="Auswählen des Kontrollkästchen Symbols zum Speichern der neuen Tastenkombination" lightbox="./media/experiments-custom-keyboard-shortcuts-enter-key.msft.png":::
       <span data-ttu-id="8d497-281">Auswählen des Kontrollkästchen Symbols zum Speichern der neuen Tastenkombination</span><span class="sxs-lookup"><span data-stu-id="8d497-281">Choose the checkmark icon to save your new keyboard shortcut</span></span>
    :::image-end:::  
    
1.  <span data-ttu-id="8d497-282">Wählen Sie die neue Tastenkombination aus, um die Aktion im devtools auszulösen.</span><span class="sxs-lookup"><span data-stu-id="8d497-282">Select your new keyboard shortcut to trigger the action in the DevTools.</span></span>  
    
<span data-ttu-id="8d497-283">Auf der Seite " **Verknüpfungen** " zeigt das Symbol " **benutzerdefinierte Tastenkombination** \ ( ![ CustomKeyboardShortcut ][ImageCustomKeyboardShortcutIcon] \)" die von Ihnen angepassten Tastenkombinationen an.</span><span class="sxs-lookup"><span data-stu-id="8d497-283">On the **Shortcuts** page, the **Custom Keyboard Shortcut** \(![CustomKeyboardShortcut][ImageCustomKeyboardShortcutIcon]\) icon displays keyboard shortcuts that you have customized.</span></span>  <span data-ttu-id="8d497-284">Wenn Sie alle Tastenkombinationen zurücksetzen möchten, wählen Sie **Standardtastenkombinationen wiederherstellen**aus.</span><span class="sxs-lookup"><span data-stu-id="8d497-284">To reset all shortcuts, choose **Restore default shortcuts**.</span></span>  

<span data-ttu-id="8d497-285">Wenn Sie die Tastenkombinationen für eine Aktion bearbeiten, um Ihre Änderungen zu verwerfen, wählen Sie das X \ ( ![ XKeyboardShortcut ][ImageXKeyboardShortcutIcon] \)-Symbol aus.</span><span class="sxs-lookup"><span data-stu-id="8d497-285">When you are editing the keyboard shortcuts for an action, to discard your changes, choose the X \(![XKeyboardShortcut][ImageXKeyboardShortcutIcon]\) icon.</span></span>  <span data-ttu-id="8d497-286">Wenn Sie Tastenkombinationen für eine bestimmte Aktion entfernen möchten, wählen Sie das Symbol " **Verknüpfung löschen** \ ( ![ DeleteKeyboardShortcut ][ImageDeleteKeyboardShortcutIcon] \)" aus.</span><span class="sxs-lookup"><span data-stu-id="8d497-286">To remove shortcuts for a specific action, choose the **Delete shortcut** \(![DeleteKeyboardShortcut][ImageDeleteKeyboardShortcutIcon]\) icon.</span></span>  <span data-ttu-id="8d497-287">Wenn Sie mehrere Tastenkombinationen für eine Aktion hinzufügen möchten, wählen Sie **Verknüpfung hinzufügen**aus.</span><span class="sxs-lookup"><span data-stu-id="8d497-287">To add multiple shortcuts for an action, choose **Add a shortcut**.</span></span>

> [!NOTE]
> <span data-ttu-id="8d497-288">Wenn eine Tastenkombination aktuell einer anderen Aktion zugewiesen ist, können Sie Sie nicht für eine neue Aktion speichern.</span><span class="sxs-lookup"><span data-stu-id="8d497-288">If a keyboard shortcut is currently assigned to another action, you are not able to save it for a new action.</span></span>  <span data-ttu-id="8d497-289">Sie müssen zuerst die Tastenkombination für die vorherige Aktion löschen und dann der neuen Aktion hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="8d497-289">You must first delete the keyboard shortcut for the previous action and then add it to the new action.</span></span>  

<!--Available in Microsoft Edge version 87 and later.  -->

### <span data-ttu-id="8d497-290">Aktivieren von zusammengesetzten Layern in der 3D-Ansicht</span><span class="sxs-lookup"><span data-stu-id="8d497-290">Turn on Composited Layers in 3D View</span></span>

<span data-ttu-id="8d497-291">Sie können nun Ebenen neben z-Indizes und dem Dokumentobjektmodell \ (DOM \) visualisieren.</span><span class="sxs-lookup"><span data-stu-id="8d497-291">You may now visualize Layers alongside z-indexes and the Document Object Model \(DOM\).</span></span>  <span data-ttu-id="8d497-292">Mit diesem Feature können Sie Debuggen, ohne die Kontexte so häufig zu wechseln.</span><span class="sxs-lookup"><span data-stu-id="8d497-292">This feature helps you debug without switching contexts as often.</span></span>  <span data-ttu-id="8d497-293">Sie haben festgestellt, dass die Verringerung des Kontextwechsels ein wichtiger Problempunkt war.</span><span class="sxs-lookup"><span data-stu-id="8d497-293">You identified that reducing context-switching was a major pain point.</span></span>  <span data-ttu-id="8d497-294">Es ist nicht immer klar, wie sich der Code, den Sie schreiben, auf Ihre Web-App auswirkt.</span><span class="sxs-lookup"><span data-stu-id="8d497-294">It is not always clear how the code you write affects your web app.</span></span>  <span data-ttu-id="8d497-295">Für ein umfassendes visuelles Debugging werden jetzt die 3D-Ansicht und die zusammengesetzten Ebenen kombiniert.</span><span class="sxs-lookup"><span data-stu-id="8d497-295">For a comprehensive visual debugging experience, the 3D View and Composited Layers are now combined.</span></span>  <span data-ttu-id="8d497-296">Nachdem Sie das Experiment aktiviert haben, stellen Sie sicher, dass Sie das devtools erneut starten.</span><span class="sxs-lookup"><span data-stu-id="8d497-296">After enabling the experiment, ensure you restart the DevTools.</span></span>  <span data-ttu-id="8d497-297">Führen Sie die folgenden Schritte aus, um **zusammengesetzte Layer**zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="8d497-297">To use **Composited Layers**, complete the following steps.</span></span>  

1.  <span data-ttu-id="8d497-298">Wählen Sie auf der Schublade das Tool **3D-Ansicht** aus.</span><span class="sxs-lookup"><span data-stu-id="8d497-298">On the drawer, choose the **3D View** tool.</span></span>  
1.  <span data-ttu-id="8d497-299">Öffnen Sie den Bereich **zusammengesetzte Ebenen** .</span><span class="sxs-lookup"><span data-stu-id="8d497-299">Open the **Composited Layers** pane.</span></span>  
1.  <span data-ttu-id="8d497-300">Alle gemalten Ebenen der App werden angezeigt.</span><span class="sxs-lookup"><span data-stu-id="8d497-300">All of the painted layers of the app are displayed.</span></span>  <span data-ttu-id="8d497-301">Testen Sie diese Funktion mit ihren eigenen Web-Apps.</span><span class="sxs-lookup"><span data-stu-id="8d497-301">Try this feature with your own web apps.</span></span>  
    
:::image type="complex" source="./media/experiments-layers.msft.png" alt-text="Bereich ' zusammengesetzte Ebenen '" lightbox="./media/experiments-layers.msft.png":::
   <span data-ttu-id="8d497-303">Bereich ' **zusammengesetzte Ebenen** '</span><span class="sxs-lookup"><span data-stu-id="8d497-303">**Composited Layers** pane</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 87 and later.  -->  

## <span data-ttu-id="8d497-304">Frühere experimentelle Features</span><span class="sxs-lookup"><span data-stu-id="8d497-304">Previous experimental features</span></span>  

*   <span data-ttu-id="8d497-305">die [3D-Ansicht][Devtools3dViewIndex] ist jetzt in Microsoft Edge, Version 83 oder höher, standardmäßig verfügbar und aktiviert.</span><span class="sxs-lookup"><span data-stu-id="8d497-305">[3D View][Devtools3dViewIndex] is now available and turned on by default in Microsoft Edge version 83 or later.</span></span>  
*   <span data-ttu-id="8d497-306">[Anpassen von Tastenkombinationen][DevtoolsCustomKeyboardShortcuts] ist jetzt in Microsoft Edge, Version 86 oder höher, standardmäßig verfügbar und aktiviert.</span><span class="sxs-lookup"><span data-stu-id="8d497-306">[Customize Keyboard Shortcuts][DevtoolsCustomKeyboardShortcuts] is now available and turned on by default in Microsoft Edge version 86 or later.</span></span>  

## <span data-ttu-id="8d497-307">Bereitstellen von Feedback zu experimentellen Features</span><span class="sxs-lookup"><span data-stu-id="8d497-307">Providing feedback on experimental features</span></span>  

<span data-ttu-id="8d497-308">Sie können Feedback zu Microsoft Edge devtools-Experimenten oder zu allem anderen, was mit devtools zu tun hat.</span><span class="sxs-lookup"><span data-stu-id="8d497-308">To provide feedback on Microsoft Edge DevTools experiments, or anything else related to DevTools.</span></span>  

*   <span data-ttu-id="8d497-309">Senden Sie Ihr Feedback über das Symbol " **Feedback senden** " im devtools</span><span class="sxs-lookup"><span data-stu-id="8d497-309">Send your feedback using the **Send Feedback** icon in the DevTools</span></span>  
*   <span data-ttu-id="8d497-310">Tweet bei [@EdgeDevTools][TwitterEdgedevtools]</span><span class="sxs-lookup"><span data-stu-id="8d497-310">Tweet at [@EdgeDevTools][TwitterEdgedevtools]</span></span>  

:::image type="complex" source="./media/bing-devtools-send-feedback.msft.png" alt-text="Das Symbol "Feedback senden" in Microsoft Edge devtools" lightbox="./media/bing-devtools-send-feedback.msft.png":::
   <span data-ttu-id="8d497-312">Das Symbol " **Feedback senden** " in Microsoft Edge devtools</span><span class="sxs-lookup"><span data-stu-id="8d497-312">The **Send Feedback** icon in Microsoft Edge DevTools</span></span>  
:::image-end:::  

<!--  
## Getting in touch with the Microsoft Edge DevTools team  

[!INCLUDE [contact DevTools team note](./includes/contact-devtools-team-note.md)]  
-->  

<!-- image links -->  

[ImageRotateIcon]: ./media/rotate-dark-icon.msft.png  
[ImageSpanIcon]: ./media/span-dark-icon.msft.png  
[ImageExperimentalApisIcon]: ./media/experimental-apis-dark-icon.msft.png  
[ImageEditKeyboardShortcutIcon]: ./media/edit-keyboard-shortcut-icon.msft.png  
[ImageCheckmarkKeyboardShortcutIcon]: ./media/checkmark-keyboard-shortcut-icon.msft.png  
[ImageCustomKeyboardShortcutIcon]: ./media/custom-keyboard-shortcut-icon.msft.png  
[ImageDeleteKeyboardShortcutIcon]: ./media/delete-keyboard-shortcut-icon.msft.png  
[ImageXKeyboardShortcutIcon]: ./media/discard-changes-keyboard-shortcut-icon.msft.png  

<!-- links -->  

[Devtools3dViewIndex]: ./3d-view/index.md "3D-Ansicht | Microsoft docs"  
[DevToolsCustomizeSettings]: ./customize/index.md#settings "Einstellungen – anpassen von Microsoft Edge devtools | Microsoft docs"  
[DevtoolsDeviceModeIndexSimulateMobileViewport]: ./device-mode/index.md#simulate-a-mobile-viewport "Simulieren von mobilen Geräten mit dem Gerätemodus in Microsoft Edge devtools | Microsoft Edge"  
[DevtoolsIssues]: ./issues/index.md "Suchen und Beheben von Problemen mit dem Microsoft Edge devtools Issues Tool | Microsoft docs"  
[DevToolsShortcuts]: ./shortcuts.md "Microsoft Edge devtools-Tastenkombinationen | Microsoft docs"  
[DevtoolsOpen]: ./open.md "Öffnen Sie Microsoft Edge devtools | Microsoft docs"  
[DevtoolsCustomKeyboardShortcuts]: ./customize/shortcuts.md "Anpassen von Tastenkombinationen in Microsoft Edge devtools | Microsoft docs"  
[DevtoolsOpenMain]: ./open.md "Öffnen Sie Microsoft Edge devtools | Microsoft docs"  

[DualScreenWebIndex]: /dual-screen/web/index "Dual-Screen Web Experiences | Microsoft docs"  
[DualScreenAndroidGetDuoSdk]: /dual-screen/android/get-duo-sdk "Abrufen des Surface Duo-Emulators | Microsoft docs"  
[DualScreenIntroductionHowWorkSeam]: /dual-screen/introduction#how-to-work-with-the-seam "Arbeiten mit der Naht – Einführung in Dual-Screen-Geräte | Microsoft docs"  
[DualScreenAndroidUseEmulator]: /dual-screen/android/use-emulator "Verwenden des Surface Duo-Emulators | Microsoft docs"  
[DualScreenDocsCssMedia]: /dual-screen/web/css-media-spanning "CSS mediascreen-Spanning-Funktion für Dual-Screen-Erkennung | Microsoft docs"  
[DualScreenDocsJSAPI]: /dual-screen/web/javascript-getwindowsegments "Die getWindowSegments-JavaScript-API für Dual-Screen-Geräte | Microsoft docs"  

[RemoteDesktopClientDocs]: /windows-server/remote/remote-desktop-services/clients/remote-desktop-clients "Remote Desktop-Clients | Microsoft docs"

[MicrosoftEdge]: https://www.microsoft.com/edge "Microsoft Edge"  

[SurfaceDevicesDuo]: https://www.microsoft.com/surface/devices/surface-duo "Surface Duo | Microsoft Surface"  

[AndroidDeveloperStudio]: https://developer.android.com/studio/ "Android Studio"  

[GooglePlayMicrosoftEdge]: https://play.google.com/store/apps/details?id=com.microsoft.emmx "Microsoft Edge | Google Play"  

[SamsungMobileGalaxyFold]: https://www.samsung.com/mobile/galaxy-fold/ "Galaxy Fold | Samsung"  

[TwitterEdgedevtools]: https://www.twitter.com/EdgeDevTools "Microsoft Edge-devtools | Twitter"  

[WebhintMain]: https://webhint.io "webhint"  
