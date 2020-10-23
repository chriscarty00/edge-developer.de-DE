---
description: Die neuesten experimentellen Features in Microsoft Edge devtools
title: Experimentelle Funktionen
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/21/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Web-Entwicklung, F12-Tools, devtools, Experiment
ms.openlocfilehash: b620388df309109e28ab8b9c010dfd448ca906f7
ms.sourcegitcommit: 6e2b26d41a0aa56ac34e6edc7dddd852ddb415b1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/23/2020
ms.locfileid: "11133855"
---
# <span data-ttu-id="a56bf-104">Experimentelle Funktionen</span><span class="sxs-lookup"><span data-stu-id="a56bf-104">Experimental features</span></span>  

<span data-ttu-id="a56bf-105">Microsoft Edge-devtools bieten Zugriff auf experimentelle Features, die sich noch in der Entwicklung befinden.</span><span class="sxs-lookup"><span data-stu-id="a56bf-105">Microsoft Edge DevTools provide access to experimental features that are still in development.</span></span>  <span data-ttu-id="a56bf-106">Sie können testen und [Feedback zur Verfügung stellen](#providing-feedback-on-experimental-features) , bevor die einzelnen Features veröffentlicht werden.</span><span class="sxs-lookup"><span data-stu-id="a56bf-106">You may test and [provide feedback](#providing-feedback-on-experimental-features) before each feature is released.</span></span>  

<span data-ttu-id="a56bf-107">Während experimentelle Features in allen Kanälen von Microsoft Edge verfügbar sind, erhalten Sie möglicherweise die neuesten experimentellen Features mithilfe des Canary-Kanals von Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="a56bf-107">While experimental features are available in all channels of Microsoft Edge, you may get the latest experimental features using the Microsoft Edge Canary channel.</span></span>  

## <span data-ttu-id="a56bf-108">Aktivieren von experimentellen Features</span><span class="sxs-lookup"><span data-stu-id="a56bf-108">Turn on experimental features</span></span>  

<span data-ttu-id="a56bf-109">Führen Sie die folgenden Schritte aus, um die experimentellen Features von \ (oder Off \) in Microsoft Edge zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="a56bf-109">To turn on \(or off\) experimental features in Microsoft Edge, use the following steps.</span></span>  

1.  <span data-ttu-id="a56bf-110">[Öffnen Sie devtools][DevtoolsOpen].</span><span class="sxs-lookup"><span data-stu-id="a56bf-110">[Open DevTools][DevtoolsOpen].</span></span>  
     *   <span data-ttu-id="a56bf-111">Wählen Sie `Control` + `Shift` + `I` \ (Windows, Linux \) oder `Command` + `Option` + `I` \ (macOS \) aus.</span><span class="sxs-lookup"><span data-stu-id="a56bf-111">Select `Control`+`Shift`+`I` \(Windows, Linux\) or `Command`+`Option`+`I` \(macOS\).</span></span>  <span data-ttu-id="a56bf-112">Weitere Informationen finden Sie unter [Tastenkombinationen für Microsoft Edge devtools][DevToolsShortcuts].</span><span class="sxs-lookup"><span data-stu-id="a56bf-112">For more information, navigate to [Microsoft Edge DevTools keyboard shortcuts][DevToolsShortcuts].</span></span>  
1.  <span data-ttu-id="a56bf-113">Öffnen Sie den Bereich " [Einstellungen][DevToolsCustomizeSettings] ".</span><span class="sxs-lookup"><span data-stu-id="a56bf-113">Open the [Settings][DevToolsCustomizeSettings] pane.</span></span>  
    *   <span data-ttu-id="a56bf-114">Wählen Sie aus `Shift` + `?` .</span><span class="sxs-lookup"><span data-stu-id="a56bf-114">Select `Shift`+`?`.</span></span>  <span data-ttu-id="a56bf-115">Weitere Informationen finden Sie unter [Tastenkombinationen für Microsoft Edge devtools][DevToolsShortcuts].</span><span class="sxs-lookup"><span data-stu-id="a56bf-115">For more information, navigate to [Microsoft Edge DevTools keyboard shortcuts][DevToolsShortcuts].</span></span>  
1.  <span data-ttu-id="a56bf-116">Wählen Sie auf der linken Seite des Bereichs **Einstellungen** den Abschnitt **Experimente** aus.</span><span class="sxs-lookup"><span data-stu-id="a56bf-116">On the left side of the **Settings** pane, choose the **Experiments** section.</span></span>  
    
    :::image type="complex" source="./media/experiments-devtools.msft.png" alt-text="Liste der Experimente in den devtools-Einstellungen" lightbox="./media/experiments-devtools.msft.png":::
       <span data-ttu-id="a56bf-118">Liste der Experimente in den devtools- **Einstellungen**</span><span class="sxs-lookup"><span data-stu-id="a56bf-118">List of experiments in DevTools **Settings**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="a56bf-119">Scrollen Sie auf der Seite **Experimente** durch die Liste aller verfügbaren experimentellen Features, und aktivieren Sie das Kontrollkästchen neben den einzelnen Features, die Sie testen möchten.</span><span class="sxs-lookup"><span data-stu-id="a56bf-119">On the **Experiments** page, scroll through the list of all available experimental features and choose the checkbox next to each feature that you want to test.</span></span>  
1.  <span data-ttu-id="a56bf-120">Schließen Sie die Microsoft Edge-devtools, und öffnen Sie Sie erneut.</span><span class="sxs-lookup"><span data-stu-id="a56bf-120">Close and reopen Microsoft Edge DevTools.</span></span>  

> [!NOTE]
> <span data-ttu-id="a56bf-121">Experimentelle Features werden ständig aktualisiert, was zu Leistungsproblemen führen kann.</span><span class="sxs-lookup"><span data-stu-id="a56bf-121">Experimental features are constantly being updated and may cause performance issues.</span></span>  <span data-ttu-id="a56bf-122">Wenn Sie ein experimentelles Feature deaktivieren möchten, öffnen Sie die Seite **Experimente** , und deaktivieren Sie das Kontrollkästchen des experimentellen Features, das Sie deaktivieren möchten.</span><span class="sxs-lookup"><span data-stu-id="a56bf-122">To turn off an experimental feature, open the **Experiments** page and clear the checkbox of the experimental feature that you want to turn off.</span></span>  

## <span data-ttu-id="a56bf-123">Hervorgehobene experimentelle Features</span><span class="sxs-lookup"><span data-stu-id="a56bf-123">Highlighted experimental features</span></span>  

<span data-ttu-id="a56bf-124">In den folgenden Abschnitten werden die neuen experimentellen Features beschrieben, die in Microsoft Edge zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="a56bf-124">The following sections describe the new experimental features that are available in Microsoft Edge.</span></span>  

| <span data-ttu-id="a56bf-125">Experimentelle Funktion</span><span class="sxs-lookup"><span data-stu-id="a56bf-125">Experimental feature</span></span> | <span data-ttu-id="a56bf-126">Microsoft Edge-Version</span><span class="sxs-lookup"><span data-stu-id="a56bf-126">Microsoft Edge version</span></span> |  
|:--- |:--- |  
| [<span data-ttu-id="a56bf-127">Emulation: Unterstützung des Dual-Screen-Modus</span><span class="sxs-lookup"><span data-stu-id="a56bf-127">Emulation: Support dual screen mode</span></span>](#emulation-support-dual-screen-mode) | <span data-ttu-id="a56bf-128">84 oder höher</span><span class="sxs-lookup"><span data-stu-id="a56bf-128">84 or later</span></span> |  
| [<span data-ttu-id="a56bf-129">Debuggen von neuen CSS-Raster Features aktivieren</span><span class="sxs-lookup"><span data-stu-id="a56bf-129">Enable new CSS grid debugging features</span></span>](#enable-new-css-grid-debugging-features) | <span data-ttu-id="a56bf-130">85 oder höher</span><span class="sxs-lookup"><span data-stu-id="a56bf-130">85 or later</span></span> |  
| [<span data-ttu-id="a56bf-131">Aktivieren der Unterstützung für das Verschieben von Tabstopps zwischen Bereichen</span><span class="sxs-lookup"><span data-stu-id="a56bf-131">Enable support to move tabs between panels</span></span>](#enable-support-to-move-tabs-between-panels) | <span data-ttu-id="a56bf-132">85 oder höher</span><span class="sxs-lookup"><span data-stu-id="a56bf-132">85 or later</span></span> |  
| [<span data-ttu-id="a56bf-133">Webhint aktivieren</span><span class="sxs-lookup"><span data-stu-id="a56bf-133">Enable webhint</span></span>](#enable-webhint) | <span data-ttu-id="a56bf-134">85 oder höher</span><span class="sxs-lookup"><span data-stu-id="a56bf-134">85 or later</span></span> |  
| [<span data-ttu-id="a56bf-135">Aktivieren der Netzwerk Konsole</span><span class="sxs-lookup"><span data-stu-id="a56bf-135">Enable Network Console</span></span>](#enable-network-console) | <span data-ttu-id="a56bf-136">85 oder höher</span><span class="sxs-lookup"><span data-stu-id="a56bf-136">85 or later</span></span> |  
| [<span data-ttu-id="a56bf-137">Viewer für Quellreihenfolge</span><span class="sxs-lookup"><span data-stu-id="a56bf-137">Source Order Viewer</span></span>](#source-order-viewer) | <span data-ttu-id="a56bf-138">86 oder höher</span><span class="sxs-lookup"><span data-stu-id="a56bf-138">86 or later</span></span> |  
| [<span data-ttu-id="a56bf-139">Aktivieren des Tasten Kombinations-Editors</span><span class="sxs-lookup"><span data-stu-id="a56bf-139">Enable keyboard shortcut editor</span></span>](#enable-keyboard-shortcut-editor) | <span data-ttu-id="a56bf-140">87 oder höher</span><span class="sxs-lookup"><span data-stu-id="a56bf-140">87 or later</span></span> |  

### <span data-ttu-id="a56bf-141">Emulation: Unterstützung des Dual-Screen-Modus</span><span class="sxs-lookup"><span data-stu-id="a56bf-141">Emulation: Support dual screen mode</span></span>  

<span data-ttu-id="a56bf-142">Bietet zusätzliche Features zum Emulieren von zwei neuen Dual-Screen-und faltbaren Geräten in Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="a56bf-142">Provides additional features for emulating two new dual-screen and foldable devices in Microsoft Edge.</span></span>  

*   [<span data-ttu-id="a56bf-143">Surface Duo</span><span class="sxs-lookup"><span data-stu-id="a56bf-143">Surface Duo</span></span>][SurfaceDevicesDuo]  
*   [<span data-ttu-id="a56bf-144">Samsung Galaxy Fold</span><span class="sxs-lookup"><span data-stu-id="a56bf-144">Samsung Galaxy Fold</span></span>][SamsungMobileGalaxyFold]  

<span data-ttu-id="a56bf-145">Emulieren Sie die Geräte, und wechseln Sie zwischen den folgenden Haltungen.</span><span class="sxs-lookup"><span data-stu-id="a56bf-145">Emulate the devices and toggle between the following postures.</span></span>  

*   <span data-ttu-id="a56bf-146">Einzelbild-oder gefaltete Haltung</span><span class="sxs-lookup"><span data-stu-id="a56bf-146">single-screen or folded posture</span></span>  
*   <span data-ttu-id="a56bf-147">Dual-Screen-oder entfaltete Haltung</span><span class="sxs-lookup"><span data-stu-id="a56bf-147">dual-screen or unfolded posture</span></span>  
    
<span data-ttu-id="a56bf-148">[Aktivieren Sie experimentelle Webplattform-APIs](#enable-experimental-apis) , und verwenden Sie das [Feature "CSS-Medien Bildschirm übergreifend"][DualScreenDocsCssMedia] und die [JavaScript-getWindowSegments-API][DualScreenDocsJSAPI] , um Ihre Website \ (oder App \) für Dual-Screen-und faltbare Geräte zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="a56bf-148">[Enable experimental Web Platform APIs](#enable-experimental-apis) and use the [CSS media screen-spanning feature][DualScreenDocsCssMedia] and [JavaScript getWindowSegments API][DualScreenDocsJSAPI] to enhance your website \(or app\) for dual-screen and foldable devices.</span></span>  

:::image type="complex" source="./media/experiments-surface-duo-emulation.msft.png" alt-text="Liste der Experimente in den devtools-Einstellungen" lightbox="./media/experiments-surface-duo-emulation.msft.png":::  
   <span data-ttu-id="a56bf-150">Emulieren von Surface Duo in Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="a56bf-150">Emulate Surface Duo in Microsoft Edge</span></span>  
:::image-end:::  

#### <span data-ttu-id="a56bf-151">Aktivieren von experimentellen APIs</span><span class="sxs-lookup"><span data-stu-id="a56bf-151">Enable experimental APIs</span></span>  

<span data-ttu-id="a56bf-152">Aktivieren Sie das Kennzeichen in Microsoft Edge, um das [Feature "CSS-Medien Bildschirm übergreifend"][DualScreenDocsCssMedia] und die [JavaScript-getWindowSegments-API][DualScreenDocsJSAPI]zu verwenden `Experimental Web Platform features` .</span><span class="sxs-lookup"><span data-stu-id="a56bf-152">To use the [CSS media screen-spanning feature][DualScreenDocsCssMedia] and [JavaScript getWindowSegments API][DualScreenDocsJSAPI], turn on the `Experimental Web Platform features` flag in Microsoft Edge.</span></span>  <span data-ttu-id="a56bf-153">Führen Sie die folgenden Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="a56bf-153">Complete the following steps.</span></span>  

1.  <span data-ttu-id="a56bf-154">Navigieren Sie zu `edge://flags` .</span><span class="sxs-lookup"><span data-stu-id="a56bf-154">Navigate to `edge://flags`.</span></span>  
1.  <span data-ttu-id="a56bf-155">Geben Sie im Textfeld **Such Kennzeichnungen** `Experimental Web Platform features` das Flag **experimental Web Platform Features** ein, und ändern Sie **deaktiviert** in **aktiviert**.</span><span class="sxs-lookup"><span data-stu-id="a56bf-155">In the **Search flags** textbox, enter `Experimental Web Platform features`, choose the **Experimental Web Platform features** flag, and change **Disabled** to **Enabled**.</span></span>  
1.  <span data-ttu-id="a56bf-156">Starten Sie Microsoft Edge neu.</span><span class="sxs-lookup"><span data-stu-id="a56bf-156">Restart Microsoft Edge.</span></span>  

:::image type="complex" source="./media/experiments-dual-screen-emulation-edge-flags.msft.png" alt-text="Liste der Experimente in den devtools-Einstellungen" lightbox="./media/experiments-dual-screen-emulation.msft.png":::
   <span data-ttu-id="a56bf-158">Aktivieren des Kennzeichens "experimentelle Webplattform-Features"</span><span class="sxs-lookup"><span data-stu-id="a56bf-158">Enable the Experimental Web Platform features flag</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="a56bf-159">Wenn Sie CSS- [medienabfragen][DualScreenDocsCssMedia] oder die [JavaScript Windows-Segment Aufzählungs-API][DualScreenDocsJSAPI] verwenden, um Ihre Website oder App für das [Surface Duo][SurfaceDevicesDuo]zu verbessern, müssen Sie auch das Kennzeichen **experimentelle Webplattform-Features** in der [Android-App für Microsoft Edge][GooglePlayMicrosoftEdge] auf Ihrem [Surface Duo][SurfaceDevicesDuo] -Gerät aktivieren.</span><span class="sxs-lookup"><span data-stu-id="a56bf-159">If you are using [CSS media queries][DualScreenDocsCssMedia] or the [JavaScript Windows Segment Enumeration API][DualScreenDocsJSAPI] to enhance your website or app for the [Surface Duo][SurfaceDevicesDuo], you must also enable the **Experimental Web Platform features** flag in the [Android Microsoft Edge app][GooglePlayMicrosoftEdge] on your [Surface Duo][SurfaceDevicesDuo] device.</span></span>  
> 
> <span data-ttu-id="a56bf-160">Wenn das Flag für **experimentelle Webplattform-Features** in der Microsoft Edge-App für [Desktops][MicrosoftEdge] aktiviert ist und in der [Android-App für Microsoft Edge][GooglePlayMicrosoftEdge]deaktiviert ist, entspricht das Verhalten Ihrer Website oder App im Surface Duo-Emulator in Desktop Microsoft Edge nicht der [Android-App "Microsoft Edge][GooglePlayMicrosoftEdge] " auf [Surface Duo][SurfaceDevicesDuo].</span><span class="sxs-lookup"><span data-stu-id="a56bf-160">If the **Experimental Web Platform features** flag is enabled in [desktop Microsoft Edge][MicrosoftEdge] and disabled in the [Android Microsoft Edge app][GooglePlayMicrosoftEdge], the behavior of your website or app in the Surface Duo emulator in desktop Microsoft Edge does not match with the [Android Microsoft Edge app][GooglePlayMicrosoftEdge] on [Surface Duo][SurfaceDevicesDuo].</span></span>  <span data-ttu-id="a56bf-161">Stellen Sie sicher, dass die Flags für Android und Desktop Microsoft Edge übereinstimmen, um den Surface Duo-Emulator erfolgreich im [Desktop Microsoft Edge][MicrosoftEdge]zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="a56bf-161">Ensure that the flags are matching across Android and desktop Microsoft Edge to successfully use the Surface Duo emulator in [desktop Microsoft Edge][MicrosoftEdge].</span></span>  

#### <span data-ttu-id="a56bf-162">Testen auf faltbaren und Dual-Screen-Geräten</span><span class="sxs-lookup"><span data-stu-id="a56bf-162">Testing on foldable and dual-screen devices</span></span>  

<span data-ttu-id="a56bf-163">Wenn Sie das [Surface Duo][SurfaceDevicesDuo] in einer Haltung mit zwei Bildschirmen in Microsoft Edge emulieren, wird die Naht \ (der Abstand zwischen den beiden Bildschirmen \) über Ihre Website oder App gezeichnet.</span><span class="sxs-lookup"><span data-stu-id="a56bf-163">When you emulate the [Surface Duo][SurfaceDevicesDuo] in a dual-screen posture in Microsoft Edge, the seam \(the space between the two screens\) is drawn over your website or app.</span></span>  

<span data-ttu-id="a56bf-164">Die emulierte Anzeige entspricht der Darstellung Ihrer Website \ (oder App \) in der [Microsoft Edge Android-App][GooglePlayMicrosoftEdge] , die auf [Surface Duo][SurfaceDevicesDuo]ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a56bf-164">The emulated display matches the way your website \(or app\) renders in the [Microsoft Edge Android app][GooglePlayMicrosoftEdge] running on [Surface Duo][SurfaceDevicesDuo].</span></span>  <span data-ttu-id="a56bf-165">Möglicherweise müssen Sie Ihre Website aktualisieren \ (oder App \), damit Sie besser entlang der Naht angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="a56bf-165">You may have to update your website \(or app\) to display better along the seam.</span></span>  <span data-ttu-id="a56bf-166">Weitere Informationen zum Anpassen Ihrer Website \ (oder App \) an die Naht finden Sie unter [Arbeiten mit der Naht][DualScreenIntroductionHowWorkSeam].</span><span class="sxs-lookup"><span data-stu-id="a56bf-166">For more information about adapting your website \(or app\) to the seam, navigate to [How to work with the seam][DualScreenIntroductionHowWorkSeam].</span></span>  

<span data-ttu-id="a56bf-167">Die [Gerätesymbolleiste][DevtoolsDeviceModeIndexSimulateMobileViewport] verfügt über zusätzliche Features, die Sie beim Testen Ihrer Website oder app in verschiedenen Haltungen und Ausrichtungen unterstützen.</span><span class="sxs-lookup"><span data-stu-id="a56bf-167">The [Device Toolbar][DevtoolsDeviceModeIndexSimulateMobileViewport] has additional features to help you test your website or app in multiple postures and orientations.</span></span>  <span data-ttu-id="a56bf-168">Wählen Sie **drehen** \ ( ![ drehen ][ImageRotateIcon] \) aus, um das Ansichtsfenster in Querformat zu drehen.</span><span class="sxs-lookup"><span data-stu-id="a56bf-168">Choose **Rotate** \(![Rotate][ImageRotateIcon]\) to rotate the viewport to landscape orientation.</span></span> <span data-ttu-id="a56bf-169">Kombinieren Sie das Feature mit **Span** \ ( ![ Span ][ImageSpanIcon] \), um zwischen Einzelbildschirm-oder gefalteten und Dual-Screen-oder entfalteten Haltungen umzuschalten.</span><span class="sxs-lookup"><span data-stu-id="a56bf-169">Combine the feature with **Span** \(![Span][ImageSpanIcon]\) to toggle between single-screen or folded and dual-screen or unfolded postures.</span></span>  <span data-ttu-id="a56bf-170">Zusammen können die Features das Testen Ihrer Website oder app in allen vier möglichen Haltungen und Ausrichtungen ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="a56bf-170">Together, the features enable testing your website or app in all four possible postures and orientations.</span></span>  

:::image type="complex" source="./media/experiments-dual-screen-emulation-rotate-span.msft.png" alt-text="Liste der Experimente in den devtools-Einstellungen" lightbox="./media/experiments-dual-screen-emulation-rotate-span.msft.png":::
   <span data-ttu-id="a56bf-172">Matrix von Haltungen und Ausrichtungen für Dual-Screen-und faltbare Geräte</span><span class="sxs-lookup"><span data-stu-id="a56bf-172">Matrix of postures and orientations for dual-screen and foldable devices</span></span>  
:::image-end:::  

<span data-ttu-id="a56bf-173">Das **Feature "experimentelle Webplattform-Features** \ ( ![ ExperimentalApis ][ImageExperimentalApisIcon] \)" zeigt den Zustand des Kennzeichens " **experimentelle Web Platform Features** " an.</span><span class="sxs-lookup"><span data-stu-id="a56bf-173">The **Experimental Web Platform features** \(![ExperimentalApis][ImageExperimentalApisIcon]\) icon displays the state of the **Experimental Web Platform features** flag.</span></span>  <span data-ttu-id="a56bf-174">Wenn die Kennzeichnung aktiviert ist, ist das Symbol hervorgehoben.</span><span class="sxs-lookup"><span data-stu-id="a56bf-174">If the flag is turned on, the icon is highlighted.</span></span>  <span data-ttu-id="a56bf-175">Wenn die Kennzeichnung deaktiviert ist, wird das Symbol nicht hervorgehoben.</span><span class="sxs-lookup"><span data-stu-id="a56bf-175">If the flag is turned off, the icon is not highlighted.</span></span>  <span data-ttu-id="a56bf-176">Um die Kennzeichnung zu aktivieren oder zu deaktivieren, navigieren Sie zu `edge://flags` der Kennzeichnung, und aktivieren Sie Sie.</span><span class="sxs-lookup"><span data-stu-id="a56bf-176">To turn on \(or off\) the flag, navigate to `edge://flags` and toggle the flag.</span></span>  

<!-- Commenting out until the icon issue is fixed in Edge Canary
The **Experimental Web Platform features** \(![ExperimentalApis][ImageExperimentalApisIcon]\) icon displays the state of the **Experimental Web Platform features** flag.  If the flag is turned on, the icon is highlighted.  If the flag is turned off, the icon is not highlighted.  To turn on \(or off\) the flag, either choose the icon or navigate to `edge://flags` and toggle the flag.   -->  

<span data-ttu-id="a56bf-177">Hier sind weitere Ressourcen, die Ihnen bei der Optimierung Ihrer Website (oder App \) für Dual-Screen-Geräte helfen können.</span><span class="sxs-lookup"><span data-stu-id="a56bf-177">Here are additional resources that may help you enhance your website \(or app\) for dual-screen devices.</span></span>  

*   <span data-ttu-id="a56bf-178">Weitere Informationen zur Web-Entwicklung auf Dual-Screen-Geräten finden Sie unter [Dual-Screen-Web-Erlebnisse][DualScreenWebIndex].</span><span class="sxs-lookup"><span data-stu-id="a56bf-178">For more information about web development on dual-screen devices, navigate to [Dual-screen web experiences][DualScreenWebIndex].</span></span>  
*   <span data-ttu-id="a56bf-179">Installieren Sie den [Surface Duo-Emulator][DualScreenAndroidUseEmulator].</span><span class="sxs-lookup"><span data-stu-id="a56bf-179">Install the [Surface Duo emulator][DualScreenAndroidUseEmulator].</span></span>  <span data-ttu-id="a56bf-180">Sie unterscheidet sich vom Emulator in Microsoft Edge, emuliert das Surface Duo mit Android und ist in [Android Studio][AndroidDeveloperStudio]integriert.</span><span class="sxs-lookup"><span data-stu-id="a56bf-180">It is different from the emulator in Microsoft Edge, emulates the Surface Duo running Android, and integrates with [Android Studio][AndroidDeveloperStudio].</span></span>  <span data-ttu-id="a56bf-181">Wenn Sie weitere Informationen erhalten möchten, navigieren Sie zu [Surface Duo SDK][DualScreenAndroidGetDuoSdk].</span><span class="sxs-lookup"><span data-stu-id="a56bf-181">For more information, navigate to [Get the Surface Duo SDK][DualScreenAndroidGetDuoSdk].</span></span>  

> [!NOTE]
> <span data-ttu-id="a56bf-182">Die folgende Liste enthält aktuelle bekannte Probleme.</span><span class="sxs-lookup"><span data-stu-id="a56bf-182">The following is a list of current known issues.</span></span>  
> 
> *   <span data-ttu-id="a56bf-183">Wenn Sie einen [Microsoft Remote Desktop-Client][RemoteDesktopClientDocs] verwenden, um eine Verbindung mit einem Remote-PC herzustellen und das [Surface Duo][SurfaceDevicesDuo] oder [Samsung Galaxy Fold][SamsungMobileGalaxyFold]zu emulieren, kann der Mauszeiger wackeln oder Stottern.</span><span class="sxs-lookup"><span data-stu-id="a56bf-183">When using a [Microsoft Remote Desktop client][RemoteDesktopClientDocs] to connect to a remote PC and emulate the [Surface Duo][SurfaceDevicesDuo] or [Samsung Galaxy Fold][SamsungMobileGalaxyFold], the pointer may shake or stutter.</span></span>  <span data-ttu-id="a56bf-184">Wenn das Problem auftritt, senden Sie [uns Feedback](#providing-feedback-on-experimental-features).</span><span class="sxs-lookup"><span data-stu-id="a56bf-184">If you run into the issue, [send feedback](#providing-feedback-on-experimental-features).</span></span>  

### <span data-ttu-id="a56bf-185">Debuggen von neuen CSS-Raster Features aktivieren</span><span class="sxs-lookup"><span data-stu-id="a56bf-185">Enable new CSS grid debugging features</span></span>  

<span data-ttu-id="a56bf-186">Dieses experimentelle Feature bietet eine Reihe neuer Visualisierungen, die Ihnen beim Debuggen von CSS-Rasterlayouts helfen.</span><span class="sxs-lookup"><span data-stu-id="a56bf-186">This experimental feature provides a number of new visualizations to help you debug CSS grid layouts.</span></span>  <span data-ttu-id="a56bf-187">Wenn Sie eine Vorschau der neuesten experimentellen Features anzeigen möchten, [Aktivieren Sie dieses Experiment](#turn-on-experimental-features) , und laden Sie devtools.</span><span class="sxs-lookup"><span data-stu-id="a56bf-187">To preview the latest experimental features, [enable this experiment](#turn-on-experimental-features) and reload DevTools.</span></span>  <span data-ttu-id="a56bf-188">Dieses Experiment ist in Microsoft Edge, Version 87 oder höher, standardmäßig aktiviert.</span><span class="sxs-lookup"><span data-stu-id="a56bf-188">This experiment is on by default in Microsoft Edge version 87 or later.</span></span>  

#### <span data-ttu-id="a56bf-189">Anzeigen von in-Hover-Raster Überlagerungen mit dem Tool "überprüfen"</span><span class="sxs-lookup"><span data-stu-id="a56bf-189">Viewing on-hover grid overlays with the Inspect tool</span></span>  

<span data-ttu-id="a56bf-190">Das Tool "über **prüfen** " bietet eine schnelle Möglichkeit, CSS-Rasterlayouts in einer Website zu erkennen und zu visualisieren, indem Sie mit der Maus darauf zeigen.</span><span class="sxs-lookup"><span data-stu-id="a56bf-190">The **Inspect** tool provides a quick way to identify and visualize CSS Grid layouts in a website by hovering over them with the mouse.</span></span>  <span data-ttu-id="a56bf-191">Klicken Sie **Inspect** ![ ](./media/inspect-icon.msft.png) in der oberen linken Ecke von devtools auf das Symbol inspizieren \ (Inspect \).</span><span class="sxs-lookup"><span data-stu-id="a56bf-191">Choose the **Inspect** \(![Inspect](./media/inspect-icon.msft.png)\) icon in the top-left corner of DevTools.</span></span>  <span data-ttu-id="a56bf-192">Zeigen Sie dann auf der Website, die Sie Debuggen, auf ein Grid-Element.</span><span class="sxs-lookup"><span data-stu-id="a56bf-192">Then, hover over a Grid element on the website you are debugging.</span></span>  <span data-ttu-id="a56bf-193">Umrisse werden um das Raster herum angezeigt, und Schattierung zeigt die Position von Raster Lücken an, sofern vorhanden.</span><span class="sxs-lookup"><span data-stu-id="a56bf-193">Outlines are displayed around the grid, and shading indicates the location of grid gaps if present.</span></span>  

:::image type="complex" source="./media/grid-inspect.msft.png" alt-text="Liste der Experimente in den devtools-Einstellungen" lightbox="./media/grid-inspect.msft.png":::
   <span data-ttu-id="a56bf-195">Anzeigen von Rastern mit dem Tool "überprüfen"</span><span class="sxs-lookup"><span data-stu-id="a56bf-195">Viewing grids with the Inspect tool</span></span>  
:::image-end:::  

#### <span data-ttu-id="a56bf-196">Anzeigen beständiger Raster Überlagerungen</span><span class="sxs-lookup"><span data-stu-id="a56bf-196">Viewing persistent grid overlays</span></span>  

<span data-ttu-id="a56bf-197">In Microsoft Edge, Version 86 oder höher, bietet das experimentelle CSS-Raster Feature auch die Option zum Aktivieren beständiger Raster Überlagerungen.</span><span class="sxs-lookup"><span data-stu-id="a56bf-197">In Microsoft Edge version 86 or later, the experimental CSS grid feature also offers the option to enable persistent Grid overlays.</span></span>  <span data-ttu-id="a56bf-198">Die persistenten Overlays bieten mehrere Vorteile.</span><span class="sxs-lookup"><span data-stu-id="a56bf-198">The persistent overlays provide several benefits.</span></span>  

*   <span data-ttu-id="a56bf-199">Die beständigen Overlays bleiben auf der Seite sichtbar, während Sie scrollen, die Maus bewegen und andere Features des devtools verwenden.</span><span class="sxs-lookup"><span data-stu-id="a56bf-199">The persistent overlays remain visible on the page as you scroll, move your mouse, and use other features of the DevTools.</span></span>  
*   <span data-ttu-id="a56bf-200">Mehrere persistente Overlays können gleichzeitig aktiviert werden, sodass Sie mehrere Rasterlayouts auf einmal überprüfen können.</span><span class="sxs-lookup"><span data-stu-id="a56bf-200">Multiple persistent overlays can be enabled at the same time, allowing you to review several grid layouts at once.</span></span>  
*   <span data-ttu-id="a56bf-201">Beständige Overlays bieten viele Konfigurationsoptionen, wie das ein-oder Ausblenden von Namen im Rasterbereich, Rasterabstände, nach Titel Größen usw.</span><span class="sxs-lookup"><span data-stu-id="a56bf-201">Persistent overlays offer many configuration options, such as hiding or showing names in the grid area, grid gaps, track sizes, and so on.</span></span>  

<span data-ttu-id="a56bf-202">Zwei Möglichkeiten zum Umschalten einer beständigen Raster Überlagerung</span><span class="sxs-lookup"><span data-stu-id="a56bf-202">The two ways to toggle a persistent grid overlay.</span></span>  

*   <span data-ttu-id="a56bf-203">Wählen Sie das Oval- **Raster** Symbol neben einem Rasterelement aus, das in der DOM-Struktur des **Elements** -Tools angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="a56bf-203">Choose the **Grid** oval icon next to any Grid element shown in the DOM tree of the **Elements** tool.</span></span>  
    
    :::image type="complex" source="./media/grid-adorner.msft.png" alt-text="Liste der Experimente in den devtools-Einstellungen" lightbox="./media/grid-adorner.msft.png":::
       <span data-ttu-id="a56bf-205">Symbol ' Raster Oval ' im Tool ' **Elemente** '</span><span class="sxs-lookup"><span data-stu-id="a56bf-205">Grid oval icon in **Elements** tool</span></span>  
    :::image-end:::  
    
*   <span data-ttu-id="a56bf-206">Öffnen Sie den neuen **LayoutPanel** -Bereich, der sich im Tool Elemente befindet, und aktivieren Sie das Kontrollkästchen neben den einzelnen Rasterelementen, die Sie markieren möchten.</span><span class="sxs-lookup"><span data-stu-id="a56bf-206">Open the new **Layout** panel located in the Elements tool, and choose the checkbox next to each Grid element you want to highlight.</span></span>  
    
    :::image type="complex" source="./media/grid-layout-zoom.msft.png" alt-text="Liste der Experimente in den devtools-Einstellungen" lightbox="./media/grid-layout-zoom.msft.png":::
       <span data-ttu-id="a56bf-208">**LayoutPanel** in devtools</span><span class="sxs-lookup"><span data-stu-id="a56bf-208">**Layout** panel in DevTools</span></span>  
    :::image-end:::  
    
#### <span data-ttu-id="a56bf-209">Konfigurieren von persistenten Overlays</span><span class="sxs-lookup"><span data-stu-id="a56bf-209">Configuring persistent overlays</span></span>  

<span data-ttu-id="a56bf-210">In Microsoft Edge, Version 86 oder höher, befindet sich das neue **LayoutPanel** -Element neben den Registerkarten **"Formatvorlagen** " und " **berechnet** " im Tool " **Elemente** ".</span><span class="sxs-lookup"><span data-stu-id="a56bf-210">In Microsoft Edge version 86 or later, the new **Layout** panel is located in the **Elements** tool alongside the **Styles** and **Computed** tabs.</span></span>  <span data-ttu-id="a56bf-211">Im **LayoutPanel** werden die Konfigurationsoptionen für persistente Overlays Oberflächen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="a56bf-211">The **Layout** panel surfaces configuration options for persistent overlays.</span></span>  

:::image type="complex" source="./media/experiments-grid.msft.png" alt-text="Liste der Experimente in den devtools-Einstellungen" lightbox="./media/experiments-grid.msft.png":::
   <span data-ttu-id="a56bf-213">CSS-Raster Debugging-Feature</span><span class="sxs-lookup"><span data-stu-id="a56bf-213">CSS grid debugging feature</span></span>  
:::image-end:::  

### <span data-ttu-id="a56bf-214">Aktivieren der Unterstützung für das Verschieben von Tabstopps zwischen Bereichen</span><span class="sxs-lookup"><span data-stu-id="a56bf-214">Enable support to move tabs between panels</span></span>  

<span data-ttu-id="a56bf-215">Normalerweise werden Tools wie **Elemente** und **Netzwerke** nur im Hauptbereich geöffnet, der sich am oberen Rand des devtools befindet.</span><span class="sxs-lookup"><span data-stu-id="a56bf-215">Normally, tools such as **Elements** and **Network** may only open in the main panel that is located at the top of the DevTools.</span></span>  <span data-ttu-id="a56bf-216">Tools wie **3D-Ansicht** und **Probleme** , die normalerweise nur in der **Schublade** angezeigt werden, die sich am unteren Rand des devtools befindet.</span><span class="sxs-lookup"><span data-stu-id="a56bf-216">Tools like **3D View** and **Issues** which normally only open in the **Drawer** panel that is located at the bottom of the DevTools.</span></span>  <span data-ttu-id="a56bf-217">Nachdem Sie das Experiment ausgewählt haben, können Sie die Tools zwischen dem oberen und unteren Bereich verschieben.</span><span class="sxs-lookup"><span data-stu-id="a56bf-217">After you choose the experiment, you may move tools between the top and bottom panels.</span></span>  <span data-ttu-id="a56bf-218">Wenn Sie ein Tool verschieben möchten, zeigen Sie auf die Registerkarte, öffnen Sie das Kontextmenü \ (Klicken Sie mit der rechten Maustaste auf \), und wählen Sie **nach oben** oder **nach unten**verschieben aus.</span><span class="sxs-lookup"><span data-stu-id="a56bf-218">To move a tool, hover on the tab, open the contextual menu \(right-click\), and choose **Move to top** or **Move to bottom**.</span></span>   <span data-ttu-id="a56bf-219">Mit diesem Experiment können Sie Ihr devtools-Layout anpassen.</span><span class="sxs-lookup"><span data-stu-id="a56bf-219">This experiment allows you to customize your DevTools layout.</span></span>  <span data-ttu-id="a56bf-220">Zum ein-oder Ausblenden des **Einschub** Panels wählen Sie `Escape` .</span><span class="sxs-lookup"><span data-stu-id="a56bf-220">To show or hide the **Drawer** panel, select `Escape`.</span></span>  

:::image type="complex" source="./media/experiments-move-panels.msft.png" alt-text="Liste der Experimente in den devtools-Einstellungen" lightbox="./media/experiments-move-panels.msft.png":::
   <span data-ttu-id="a56bf-222">Verschieben von Tabstopps zwischen Bereichen</span><span class="sxs-lookup"><span data-stu-id="a56bf-222">Moving tabs between panels</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 85 and later.  -->  

### <span data-ttu-id="a56bf-223">Webhint aktivieren</span><span class="sxs-lookup"><span data-stu-id="a56bf-223">Enable webhint</span></span>  

<span data-ttu-id="a56bf-224">[webhint][WebhintMain] ist ein Open-Source-Tool, das Echtzeitfeedback für Websites und lokale Webseiten bietet.</span><span class="sxs-lookup"><span data-stu-id="a56bf-224">[webhint][WebhintMain] is an open-source tool that provides real-time feedback for websites and local web pages.</span></span>  <span data-ttu-id="a56bf-225">Der Typ des Feedbacks, das von [webhint][WebhintMain]bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="a56bf-225">The type of feedback provided by [webhint][WebhintMain].</span></span>  

*   <span data-ttu-id="a56bf-226">Bedienungshilfen</span><span class="sxs-lookup"><span data-stu-id="a56bf-226">accessibility</span></span>  
*   <span data-ttu-id="a56bf-227">browserübergreifende Kompatibilität</span><span class="sxs-lookup"><span data-stu-id="a56bf-227">cross-browser compatibility</span></span>  
*   <span data-ttu-id="a56bf-228">Sicherheit</span><span class="sxs-lookup"><span data-stu-id="a56bf-228">security</span></span>  
*   <span data-ttu-id="a56bf-229">Leistung</span><span class="sxs-lookup"><span data-stu-id="a56bf-229">performance</span></span>  
*   <span data-ttu-id="a56bf-230">PWAs</span><span class="sxs-lookup"><span data-stu-id="a56bf-230">PWAs</span></span>  
*   <span data-ttu-id="a56bf-231">andere häufig auftretende Probleme mit der Web-Entwicklung</span><span class="sxs-lookup"><span data-stu-id="a56bf-231">other common web development issues</span></span>  

<span data-ttu-id="a56bf-232">Das [webhint][WebhintMain] -Experiment zeigt das webhint-Feedback im Bereich " [Probleme][DevtoolsIssues] " an.</span><span class="sxs-lookup"><span data-stu-id="a56bf-232">The [webhint][WebhintMain] experiment displays the webhint feedback in the [Issues][DevtoolsIssues] panel.</span></span>  <span data-ttu-id="a56bf-233">Wählen Sie ein Problem aus, um die Lösungsdokumentation und eine Liste der betroffenen Ressourcen auf Ihrer Website anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="a56bf-233">Choose an issue to display solution documentation and a list of the affected resources on your website.</span></span>  <span data-ttu-id="a56bf-234">Wählen Sie einen Ressourcen Link aus, um den entsprechenden Bereich für **Netzwerke**, **Quellen**oder **Elemente** in devtools zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="a56bf-234">Choose a resource link to open the relevant **Network**, **Sources**, or **Elements** pane in DevTools.</span></span>  

:::image type="complex" source="./media/experiments-webhint.msft.png" alt-text="Liste der Experimente in den devtools-Einstellungen" lightbox="./media/experiments-webhint.msft.png":::
   <span data-ttu-id="a56bf-236">webhint-Feedback im Bereich " **Probleme** "</span><span class="sxs-lookup"><span data-stu-id="a56bf-236">webhint feedback in the **Issues** panel</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 85 and later.  -->  

### <span data-ttu-id="a56bf-237">Aktivieren der Netzwerk Konsole</span><span class="sxs-lookup"><span data-stu-id="a56bf-237">Enable Network Console</span></span>  

<span data-ttu-id="a56bf-238">**Netzwerk Konsole** ist der Arbeitstitel eines Experiments, um synthetische Netzwerkanforderungen über HTTP zu stellen.</span><span class="sxs-lookup"><span data-stu-id="a56bf-238">**Network Console** is the working title of an experiment to make synthetic network requests over HTTP.</span></span>  <span data-ttu-id="a56bf-239">Sie können das **Netzwerkkonsolen** Experiment verwenden, um Web-API-Anforderungen zu senden.</span><span class="sxs-lookup"><span data-stu-id="a56bf-239">You may use the **Network Console** experiment to send web API requests.</span></span>  

<span data-ttu-id="a56bf-240">Nachdem Sie das Experiment aktiviert haben, stellen Sie sicher, dass Sie das devtools erneut starten.</span><span class="sxs-lookup"><span data-stu-id="a56bf-240">After enabling the experiment, ensure you restart the DevTools.</span></span>  <span data-ttu-id="a56bf-241">Führen Sie die folgenden Schritte aus, um die **Netzwerk Konsole**zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="a56bf-241">To use the **Network Console**, use the following steps.</span></span>  

1.  <span data-ttu-id="a56bf-242">Öffnen Sie den Bereich **Netzwerk** .</span><span class="sxs-lookup"><span data-stu-id="a56bf-242">Open the **Network** pane.</span></span>  
1.  <span data-ttu-id="a56bf-243">Suchen Sie die Netzwerkanforderung, die Sie ändern möchten, und senden Sie Sie erneut.</span><span class="sxs-lookup"><span data-stu-id="a56bf-243">Find the network request that you want to change and resend.</span></span>  
1.  <span data-ttu-id="a56bf-244">Öffnen Sie das Kontextmenü \ (Klicken Sie mit der rechten Maustaste auf \), und wählen Sie **Bearbeiten und wiedergeben**aus.</span><span class="sxs-lookup"><span data-stu-id="a56bf-244">Open the contextual menu \(right-click\), and choose **Edit and Replay**.</span></span>  
1.  <span data-ttu-id="a56bf-245">Wenn die **Netzwerk Konsole** geöffnet wird, bearbeiten Sie die Netzwerk Anforderungsinformationen.</span><span class="sxs-lookup"><span data-stu-id="a56bf-245">When the **Network Console** opens, edit the network request information.</span></span>  
1.  <span data-ttu-id="a56bf-246">Wählen Sie **senden**aus.</span><span class="sxs-lookup"><span data-stu-id="a56bf-246">Choose **Send**.</span></span>  

:::image type="complex" source="./media/network-network-console.msft.png" alt-text="Liste der Experimente in den devtools-Einstellungen" lightbox="./media/network-network-console.msft.png":::
   <span data-ttu-id="a56bf-248">**Netzwerk Konsole** im **Konsolen** Einzug</span><span class="sxs-lookup"><span data-stu-id="a56bf-248">**Network Console** in the **Console** drawer</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 85 and later.  -->  

### <span data-ttu-id="a56bf-249">Viewer für Quellreihenfolge</span><span class="sxs-lookup"><span data-stu-id="a56bf-249">Source Order Viewer</span></span>  

<span data-ttu-id="a56bf-250">Die **Quellauftrags Anzeige** ist ein Experiment, das die Reihenfolge der Elemente in der Seitenquelle anzeigt.</span><span class="sxs-lookup"><span data-stu-id="a56bf-250">**Source Order Viewer** is an experiment that displays the order of elements in the page source.</span></span>  <span data-ttu-id="a56bf-251">Die Anzeigereihenfolge auf dem Bildschirm kann von der Reihenfolge der Quelle abweichen, die die Bildschirmsprachausgabe und die Tastatur Benutzer verwirrt.</span><span class="sxs-lookup"><span data-stu-id="a56bf-251">The on-screen display order may differ from the order of the source, which confuses screen reader and keyboard users.</span></span>  <span data-ttu-id="a56bf-252">Verwenden Sie das Experiment der **Quellauftrags Anzeige** , um die Unterschiede zwischen der Anzeigereihenfolge auf dem Bildschirm und der Reihenfolge der Quelle zu finden.</span><span class="sxs-lookup"><span data-stu-id="a56bf-252">Use the **Source Order Viewer** experiment to find the differences between on-screen display order and the order of the source.</span></span>  

<span data-ttu-id="a56bf-253">Nachdem Sie das Experiment aktiviert haben, stellen Sie sicher, dass Sie das devtools erneut starten.</span><span class="sxs-lookup"><span data-stu-id="a56bf-253">After enabling the experiment, ensure you restart the DevTools.</span></span>  <span data-ttu-id="a56bf-254">Führen Sie die folgenden Schritte aus, um die **Quellauftrags Anzeige**zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="a56bf-254">To use **Source Order Viewer**, use the following steps.</span></span>  

1.  <span data-ttu-id="a56bf-255">Öffnen Sie den Bereich **Elemente** .</span><span class="sxs-lookup"><span data-stu-id="a56bf-255">Open the **Elements** pane.</span></span>  
1.  <span data-ttu-id="a56bf-256">Öffnen Sie den Bereich " **Barrierefreiheit** " im Bereich "Schublade \" (unten).</span><span class="sxs-lookup"><span data-stu-id="a56bf-256">Open the **Accessibility** pane in the drawer \(bottom\) panel.</span></span>  
1.  <span data-ttu-id="a56bf-257">Wählen Sie im Abschnitt **Quellauftrags Anzeige** das Kontrollkästchen **Quellreihenfolge anzeigen** aus.</span><span class="sxs-lookup"><span data-stu-id="a56bf-257">Under the **Source Order Viewer** section, choose the **Show Source Order** checkbox.</span></span>  
1.  <span data-ttu-id="a56bf-258">Markieren Sie ein beliebiges HTML-Element, um ein Overlay anzuzeigen, das die Reihenfolge in der Seitenquelle enthält.</span><span class="sxs-lookup"><span data-stu-id="a56bf-258">Highlight any HTML element to display an overlay that the order in the page source.</span></span>  

:::image type="complex" source="./media/experiments-source-order-viewer.msft.png" alt-text="Liste der Experimente in den devtools-Einstellungen" lightbox="./media/experiments-source-order-viewer.msft.png":::
   <span data-ttu-id="a56bf-260">**Viewer für Quellreihenfolge** im Bereich " **Barrierefreiheit** "</span><span class="sxs-lookup"><span data-stu-id="a56bf-260">**Source Order Viewer** in the **Accessibility** pane</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 86 and later.  -->  

### <span data-ttu-id="a56bf-261">Aktivieren des Tasten Kombinations-Editors</span><span class="sxs-lookup"><span data-stu-id="a56bf-261">Enable keyboard shortcut editor</span></span>

<span data-ttu-id="a56bf-262">Wenn das Experiment " **Tastenkombinationen-Editor aktivieren** " aktiviert ist, können Sie jetzt Tastenkombinationen für jede Aktion im devtools anpassen.</span><span class="sxs-lookup"><span data-stu-id="a56bf-262">With the **Enable keyboard shortcut editor** experiment turned on, you are now able to customize keyboard shortcuts for any action in the DevTools.</span></span>  <span data-ttu-id="a56bf-263">Führen Sie die folgenden Schritte aus, um die Tastenkombination für eine bestimmte Aktion anzupassen.</span><span class="sxs-lookup"><span data-stu-id="a56bf-263">To customize the keyboard shortcut for a specific action, complete the following steps.</span></span>  

1.  <span data-ttu-id="a56bf-264">[Öffnen Sie devtools][DevtoolsOpenMain].</span><span class="sxs-lookup"><span data-stu-id="a56bf-264">[Open DevTools][DevtoolsOpenMain].</span></span>  
1.  <span data-ttu-id="a56bf-265">Öffnen Sie [Einstellungen][DevToolsCustomizeSettings].</span><span class="sxs-lookup"><span data-stu-id="a56bf-265">Open [Settings][DevToolsCustomizeSettings].</span></span>
    *   <span data-ttu-id="a56bf-266">Wählen Sie aus `Shift` + `?` .</span><span class="sxs-lookup"><span data-stu-id="a56bf-266">Select `Shift`+`?`.</span></span>  
1.  <span data-ttu-id="a56bf-267">Navigieren Sie zur Seite **Verknüpfungen** .</span><span class="sxs-lookup"><span data-stu-id="a56bf-267">Navigate to the **Shortcuts** page.</span></span>  
1.  <span data-ttu-id="a56bf-268">Wählen Sie die Aktion aus, die Sie anpassen möchten.</span><span class="sxs-lookup"><span data-stu-id="a56bf-268">Choose the action you want to customize.</span></span>  
1.  <span data-ttu-id="a56bf-269">Wählen Sie das Symbol **Bearbeiten** \ ( ![ EditKeyboardShortcut ][ImageEditKeyboardShortcutIcon] \) aus.</span><span class="sxs-lookup"><span data-stu-id="a56bf-269">Choose the **Edit** \(![EditKeyboardShortcut][ImageEditKeyboardShortcutIcon]\) icon.</span></span>  
    
    :::image type="complex" source="./media/experiments-custom-keyboard-shortcuts-select-action.msft.png" alt-text="Liste der Experimente in den devtools-Einstellungen" lightbox="./media/experiments-custom-keyboard-shortcuts-select-action.msft.png":::
       <span data-ttu-id="a56bf-271">Auswählen der zu anpassenden Aktion auf der Seite " **Verknüpfungen** " in " [Einstellungen][DevToolsCustomizeSettings] "</span><span class="sxs-lookup"><span data-stu-id="a56bf-271">Choose the action to customize from the **Shortcuts** page in [Settings][DevToolsCustomizeSettings]</span></span>
    :::image-end:::  
    
1.  <span data-ttu-id="a56bf-272">Wählen Sie auf der Tastatur die Tasten aus, die Sie an die Aktion binden möchten.</span><span class="sxs-lookup"><span data-stu-id="a56bf-272">On the keyboard, select the keys you want to bind to the action.</span></span>
    
    :::image type="complex" source="./media/experiments-custom-keyboard-shortcuts-enter-key.msft.png" alt-text="Liste der Experimente in den devtools-Einstellungen" lightbox="./media/experiments-custom-keyboard-shortcuts-enter-key.msft.png":::
       <span data-ttu-id="a56bf-274">Wählen Sie die Tasten aus, die Sie der Aktion zuweisen möchten.</span><span class="sxs-lookup"><span data-stu-id="a56bf-274">Select the keys you want to assign to the action</span></span>
    :::image-end:::  
    
1.  <span data-ttu-id="a56bf-275">Wenn Sie die neue Tastenkombination speichern möchten, wählen Sie das Häkchen \ (</span><span class="sxs-lookup"><span data-stu-id="a56bf-275">To save your new keyboard shortcut, choose the checkmark \(</span></span>![CheckmarkKeyboardShortcut][ImageCheckmarkKeyboardShortcutIcon]<span data-ttu-id="a56bf-277">\)-Symbol.</span><span class="sxs-lookup"><span data-stu-id="a56bf-277">\) icon.</span></span>
    
    :::image type="complex" source="./media/experiments-custom-keyboard-shortcuts-save-shortcut.msft.png" alt-text="Liste der Experimente in den devtools-Einstellungen" lightbox="./media/experiments-custom-keyboard-shortcuts-enter-key.msft.png":::
       <span data-ttu-id="a56bf-279">Auswählen des Kontrollkästchen Symbols zum Speichern der neuen Tastenkombination</span><span class="sxs-lookup"><span data-stu-id="a56bf-279">Choose the checkmark icon to save your new keyboard shortcut</span></span>
    :::image-end:::  
    
1.  <span data-ttu-id="a56bf-280">Wählen Sie die neue Tastenkombination aus, um die Aktion im devtools auszulösen.</span><span class="sxs-lookup"><span data-stu-id="a56bf-280">Select your new keyboard shortcut to trigger the action in the DevTools.</span></span>  
    
<span data-ttu-id="a56bf-281">Auf der Seite " **Verknüpfungen** " zeigt das Symbol " **benutzerdefinierte Tastenkombination** \ ( ![ CustomKeyboardShortcut ][ImageCustomKeyboardShortcutIcon] \)" die von Ihnen angepassten Tastenkombinationen an.</span><span class="sxs-lookup"><span data-stu-id="a56bf-281">On the **Shortcuts** page, the **Custom Keyboard Shortcut** \(![CustomKeyboardShortcut][ImageCustomKeyboardShortcutIcon]\) icon displays keyboard shortcuts that you have customized.</span></span>  <span data-ttu-id="a56bf-282">Wenn Sie alle Tastenkombinationen zurücksetzen möchten, wählen Sie **Standardtastenkombinationen wiederherstellen**aus.</span><span class="sxs-lookup"><span data-stu-id="a56bf-282">To reset all shortcuts, choose **Restore default shortcuts**.</span></span>  

<span data-ttu-id="a56bf-283">Wenn Sie die Tastenkombinationen für eine Aktion bearbeiten, um Ihre Änderungen zu verwerfen, wählen Sie das X \ ( ![ XKeyboardShortcut ][ImageXKeyboardShortcutIcon] \)-Symbol aus.</span><span class="sxs-lookup"><span data-stu-id="a56bf-283">When you are editing the keyboard shortcuts for an action, to discard your changes, choose the X \(![XKeyboardShortcut][ImageXKeyboardShortcutIcon]\) icon.</span></span>  <span data-ttu-id="a56bf-284">Wenn Sie Tastenkombinationen für eine bestimmte Aktion entfernen möchten, wählen Sie das Symbol " **Verknüpfung löschen** \ ( ![ DeleteKeyboardShortcut ][ImageDeleteKeyboardShortcutIcon] \)" aus.</span><span class="sxs-lookup"><span data-stu-id="a56bf-284">To remove shortcuts for a specific action, choose the **Delete shortcut** \(![DeleteKeyboardShortcut][ImageDeleteKeyboardShortcutIcon]\) icon.</span></span>  <span data-ttu-id="a56bf-285">Wenn Sie mehrere Tastenkombinationen für eine Aktion hinzufügen möchten, wählen Sie **Verknüpfung hinzufügen**aus.</span><span class="sxs-lookup"><span data-stu-id="a56bf-285">To add multiple shortcuts for an action, choose **Add a shortcut**.</span></span>

> [!NOTE]
> <span data-ttu-id="a56bf-286">Wenn eine Tastenkombination aktuell einer anderen Aktion zugewiesen ist, können Sie Sie nicht für eine neue Aktion speichern.</span><span class="sxs-lookup"><span data-stu-id="a56bf-286">If a keyboard shortcut is currently assigned to another action, you are not able to save it for a new action.</span></span>  <span data-ttu-id="a56bf-287">Sie müssen zuerst die Tastenkombination für die vorherige Aktion löschen und dann der neuen Aktion hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="a56bf-287">You must first delete the keyboard shortcut for the previous action and then add it to the new action.</span></span>  

## <span data-ttu-id="a56bf-288">Frühere experimentelle Features</span><span class="sxs-lookup"><span data-stu-id="a56bf-288">Previous experimental features</span></span>  

*   <span data-ttu-id="a56bf-289">die [3D-Ansicht][Devtools3dViewIndex] ist jetzt in Microsoft Edge, Version 83 oder höher, standardmäßig verfügbar und aktiviert.</span><span class="sxs-lookup"><span data-stu-id="a56bf-289">[3D View][Devtools3dViewIndex] is now available and turned on by default in Microsoft Edge version 83 or later.</span></span>  
*   <span data-ttu-id="a56bf-290">[Anpassen von Tastenkombinationen][DevtoolsCustomKeyboardShortcuts] ist jetzt in Microsoft Edge, Version 86 oder höher, standardmäßig verfügbar und aktiviert.</span><span class="sxs-lookup"><span data-stu-id="a56bf-290">[Customize Keyboard Shortcuts][DevtoolsCustomKeyboardShortcuts] is now available and turned on by default in Microsoft Edge version 86 or later.</span></span>  

## <span data-ttu-id="a56bf-291">Bereitstellen von Feedback zu experimentellen Features</span><span class="sxs-lookup"><span data-stu-id="a56bf-291">Providing feedback on experimental features</span></span>  

<span data-ttu-id="a56bf-292">Sie können Feedback zu Microsoft Edge devtools-Experimenten oder zu allem anderen, was mit devtools zu tun hat.</span><span class="sxs-lookup"><span data-stu-id="a56bf-292">To provide feedback on Microsoft Edge DevTools experiments, or anything else related to DevTools.</span></span>  

*   <span data-ttu-id="a56bf-293">Senden Sie Ihr Feedback über das Symbol " **Feedback senden** " im devtools</span><span class="sxs-lookup"><span data-stu-id="a56bf-293">Send your feedback using the **Send Feedback** icon in the DevTools</span></span>  
*   <span data-ttu-id="a56bf-294">Tweet bei [@EdgeDevTools][TwitterEdgedevtools]</span><span class="sxs-lookup"><span data-stu-id="a56bf-294">Tweet at [@EdgeDevTools][TwitterEdgedevtools]</span></span>  

:::image type="complex" source="./media/bing-devtools-send-feedback.msft.png" alt-text="Liste der Experimente in den devtools-Einstellungen" lightbox="./media/bing-devtools-send-feedback.msft.png":::
   <span data-ttu-id="a56bf-296">Das Symbol " **Feedback senden** " in Microsoft Edge devtools</span><span class="sxs-lookup"><span data-stu-id="a56bf-296">The **Send Feedback** icon in Microsoft Edge DevTools</span></span>  
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
