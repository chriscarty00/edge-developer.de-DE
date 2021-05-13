---
description: Verwenden Sie virtuelle Geräte in Microsoft Edge, um Ihre Website für Dualscreen- und faltbare Geräte zu verbessern.
title: Emulieren von Dualscreen- und faltbaren Geräten in Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, web development, f12 tools, devtools, emulation, device, simulation, mobile, dual-screen, foldable, Surface Duo, Samsung Galaxy Fold
ms.openlocfilehash: c3bd3296afa86d9d2c90c164bc3e9088bc043c3c
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/13/2021
ms.locfileid: "11564343"
---
# <a name="emulate-dual-screen-and-foldable-devices-in-microsoft-edge-devtools"></a><span data-ttu-id="4991f-104">Emulieren von Dualscreen- und faltbaren Geräten in Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="4991f-104">Emulate dual-screen and foldable devices in Microsoft Edge DevTools</span></span>  

<span data-ttu-id="4991f-105">In Microsoft Edge Version 89 oder höher können Sie die folgenden Dualscreen- und faltbaren Geräte emulieren.</span><span class="sxs-lookup"><span data-stu-id="4991f-105">In Microsoft Edge version 89 or later, you may emulate the following dual-screen and foldable devices.</span></span>  

*   [<span data-ttu-id="4991f-106">Surface Duo</span><span class="sxs-lookup"><span data-stu-id="4991f-106">Surface Duo</span></span>][SurfaceDevicesDuo]  
*   [<span data-ttu-id="4991f-107">Samsung Galaxy Fold</span><span class="sxs-lookup"><span data-stu-id="4991f-107">Samsung Galaxy Fold</span></span>][SamsungMobileGalaxyFold]  
    
<span data-ttu-id="4991f-108">Emulieren Sie die Geräte, und schalten Sie zwischen den folgenden Haltungen um.</span><span class="sxs-lookup"><span data-stu-id="4991f-108">Emulate the devices and toggle between the following postures.</span></span>  

*   <span data-ttu-id="4991f-109">Einzelbildschirm- oder geklappte Haltung</span><span class="sxs-lookup"><span data-stu-id="4991f-109">Single-screen or folded posture</span></span>  
*   <span data-ttu-id="4991f-110">Dual-Screen- oder ungefalte Haltung</span><span class="sxs-lookup"><span data-stu-id="4991f-110">Dual-screen or unfolded posture</span></span>  
    
<span data-ttu-id="4991f-111">Aktivieren Sie [experimentelle Webplattform-APIs,](#turn-on-experimental-apis) und verwenden Sie die [CSS-Medienbildschirm-Spannfunktion][DualScreenDocsCssMedia] und die [JavaScript getWindowSegments-API,][DualScreenDocsJSAPI] um Ihre Website \(oder App\) für Dualscreen- und faltbare Geräte zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="4991f-111">[Turn on experimental Web Platform APIs](#turn-on-experimental-apis) and use the [CSS media screen-spanning feature][DualScreenDocsCssMedia] and [JavaScript getWindowSegments API][DualScreenDocsJSAPI] to enhance your website \(or app\) for dual-screen and foldable devices.</span></span>  

:::image type="complex" source="../media/experiments-surface-duo-emulation.msft.png" alt-text="Emulieren von Surface Duo in Microsoft Edge" lightbox="../media/experiments-surface-duo-emulation.msft.png":::  
   <span data-ttu-id="4991f-113">Emulieren von Surface Duo in Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="4991f-113">Emulate Surface Duo in Microsoft Edge</span></span>  
:::image-end:::  

## <a name="turn-on-experimental-apis"></a><span data-ttu-id="4991f-114">Aktivieren von experimentellen APIs</span><span class="sxs-lookup"><span data-stu-id="4991f-114">Turn on experimental APIs</span></span>  

<span data-ttu-id="4991f-115">Aktivieren Sie [][DualScreenDocsCssMedia] das Flag in der Microsoft Edge, um das Feature für die Verwendung des CSS-Medienbildschirmbereichs und der [JavaScript getWindowSegments-API][DualScreenDocsJSAPI] `Experimental Web Platform features` zu Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="4991f-115">To use the [CSS media screen-spanning feature][DualScreenDocsCssMedia] and [JavaScript getWindowSegments API][DualScreenDocsJSAPI], turn on the `Experimental Web Platform features` flag in Microsoft Edge.</span></span>  <span data-ttu-id="4991f-116">Führen Sie die folgenden Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="4991f-116">Complete the following steps.</span></span>  

1.  <span data-ttu-id="4991f-117">Navigieren Sie zu `edge://flags`.</span><span class="sxs-lookup"><span data-stu-id="4991f-117">Navigate to `edge://flags`.</span></span>  
1.  <span data-ttu-id="4991f-118">Geben Sie **im Textfeld Suchkennzeichen** die Option Ein, wählen Sie das `Experimental Web Platform features` Kennzeichen Experimentelle **Webplattformfeatures** aus, und ändern Sie **Deaktiviert** in **Aktiviert**.</span><span class="sxs-lookup"><span data-stu-id="4991f-118">In the **Search flags** textbox, enter `Experimental Web Platform features`, choose the **Experimental Web Platform features** flag, and change **Disabled** to **Enabled**.</span></span>  
1.  <span data-ttu-id="4991f-119">Starten Sie Microsoft Edge neu.</span><span class="sxs-lookup"><span data-stu-id="4991f-119">Restart Microsoft Edge.</span></span>  
    
:::image type="complex" source="../media/experiments-dual-screen-emulation-edge-flags.msft.png" alt-text="Aktivieren des Kennzeichens für Experimentelle Webplattformfeatures" lightbox="../media/experiments-dual-screen-emulation.msft.png":::
   <span data-ttu-id="4991f-121">Aktivieren des **Kennzeichens für Experimentelle Webplattformfeatures**</span><span class="sxs-lookup"><span data-stu-id="4991f-121">Turn on the **Experimental Web Platform features** flag</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="4991f-122">Wenn Sie CSS-Medienabfragen oder die [JavaScript Windows Segment Enumeration API][DualScreenDocsJSAPI] verwenden, um Ihre Website oder App für das Surface [Duo][SurfaceDevicesDuo]zu verbessern, müssen Sie auch das Flag experimentelle Webplattformfeatures in der [Android Microsoft Edge-App][GooglePlayMicrosoftEdge] auf Ihrem Surface [Duo-Gerät][SurfaceDevicesDuo] aktivieren. [][DualScreenDocsCssMedia] \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="4991f-122">If you are using [CSS media queries][DualScreenDocsCssMedia] or the [JavaScript Windows Segment Enumeration API][DualScreenDocsJSAPI] to enhance your website or app for the [Surface Duo][SurfaceDevicesDuo], you must also turn on the **Experimental Web Platform features** flag in the [Android Microsoft Edge app][GooglePlayMicrosoftEdge] on your [Surface Duo][SurfaceDevicesDuo] device.</span></span>  
> 
> <span data-ttu-id="4991f-123">Wenn \*\*\*\* das Flag für experimentelle Webplattformfeatures in desktop [Microsoft Edge][MicrosoftEdge] aktiviert und in der [Android Microsoft Edge-App][GooglePlayMicrosoftEdge]deaktiviert ist, ist das Verhalten Ihrer Website oder App im Surface Duo-Emulator in Desktop Microsoft Edge nicht mit der [Android Microsoft Edge-App][GooglePlayMicrosoftEdge] auf [Surface Duo kompatibel.][SurfaceDevicesDuo]</span><span class="sxs-lookup"><span data-stu-id="4991f-123">If the **Experimental Web Platform features** flag is turned on in [desktop Microsoft Edge][MicrosoftEdge] and turned off in the [Android Microsoft Edge app][GooglePlayMicrosoftEdge], the behavior of your website or app in the Surface Duo emulator in desktop Microsoft Edge does not match with the [Android Microsoft Edge app][GooglePlayMicrosoftEdge] on [Surface Duo][SurfaceDevicesDuo].</span></span>  <span data-ttu-id="4991f-124">Stellen Sie sicher, dass die Flags für Android und desktop-Microsoft Edge, um den Surface Duo-Emulator [in][MicrosoftEdge]Desktop-Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="4991f-124">Ensure that the flags match across Android and desktop Microsoft Edge to successfully use the Surface Duo emulator in [desktop Microsoft Edge][MicrosoftEdge].</span></span>  

## <a name="test-on-foldable-and-dual-screen-devices"></a><span data-ttu-id="4991f-125">Testen auf zusammenklappbaren Und Dualscreen-Geräten</span><span class="sxs-lookup"><span data-stu-id="4991f-125">Test on foldable and dual-screen devices</span></span>  

<span data-ttu-id="4991f-126">Wenn Sie das [Surface Duo][SurfaceDevicesDuo] in einer Dual-Screen-Haltung in Microsoft Edge emulieren, wird die Naht \(der Abstand zwischen den beiden Bildschirmen\) über Ihre Website oder App gezeichnet.</span><span class="sxs-lookup"><span data-stu-id="4991f-126">When you emulate the [Surface Duo][SurfaceDevicesDuo] in a dual-screen posture in Microsoft Edge, the seam \(the space between the two screens\) is drawn over your website or app.</span></span>  

<span data-ttu-id="4991f-127">Die emulierte Anzeige entspricht der Art und [Weise,][GooglePlayMicrosoftEdge] wie Ihre Website \(oder App\) in der Microsoft Edge Android-App gerendert wird, während sie auf [Surface Duo ausgeführt wird.][SurfaceDevicesDuo]</span><span class="sxs-lookup"><span data-stu-id="4991f-127">The emulated display matches the way your website \(or app\) renders in the [Microsoft Edge Android app][GooglePlayMicrosoftEdge] while running on [Surface Duo][SurfaceDevicesDuo].</span></span>  <span data-ttu-id="4991f-128">Möglicherweise müssen Sie Ihre Website \(oder App\) aktualisieren, um entlang der Naht besser angezeigt zu werden.</span><span class="sxs-lookup"><span data-stu-id="4991f-128">You may have to update your website \(or app\) to display better along the seam.</span></span>  <span data-ttu-id="4991f-129">Weitere Informationen zum Anpassen Ihrer Website \(oder App\) an die Naht finden Sie unter [How to work with the seam][DualScreenIntroductionHowWorkSeam].</span><span class="sxs-lookup"><span data-stu-id="4991f-129">For more information about adapting your website \(or app\) to the seam, navigate to [How to work with the seam][DualScreenIntroductionHowWorkSeam].</span></span>  

<span data-ttu-id="4991f-130">Die [Gerätesymbolleiste][DevtoolsDeviceModeIndexSimulateMobileViewport] verfügt über zusätzliche Features, mit deren Hilfe Sie Ihre Website oder App in mehreren Haltungen und Ausrichtungen testen können.</span><span class="sxs-lookup"><span data-stu-id="4991f-130">The [Device Toolbar][DevtoolsDeviceModeIndexSimulateMobileViewport] has additional features to help you test your website or app in multiple postures and orientations.</span></span>  <span data-ttu-id="4991f-131">Wählen **Sie Drehen** \( Drehen ![ ](../media/rotate-dark-icon.msft.png) \) aus, um den Ansichtsfenster in die Querformatausrichtung zu drehen.</span><span class="sxs-lookup"><span data-stu-id="4991f-131">Choose **Rotate** \(![Rotate](../media/rotate-dark-icon.msft.png)\) to rotate the viewport to landscape orientation.</span></span> <span data-ttu-id="4991f-132">Kombinieren Sie das Feature mit **Span** \( Span \), um zwischen einem bildschirm- oder gefalteten und dualen Bildschirm oder aufgeklappten Haltungen ![ ](../media/span-dark-icon.msft.png) umschalten zu können.</span><span class="sxs-lookup"><span data-stu-id="4991f-132">Combine the feature with **Span** \(![Span](../media/span-dark-icon.msft.png)\) to toggle between single-screen or folded and dual-screen or unfolded postures.</span></span>  <span data-ttu-id="4991f-133">Mit den Features können Sie Ihre Website oder App in allen vier möglichen Haltungen und Ausrichtungen testen.</span><span class="sxs-lookup"><span data-stu-id="4991f-133">Together, the features allow you to test your website or app in all four possible postures and orientations.</span></span>  

:::image type="complex" source="../media/experiments-dual-screen-emulation-rotate-span.msft.png" alt-text="Matrix von Haltungen und Ausrichtungen für Dualscreen- und faltbare Geräte" lightbox="../media/experiments-dual-screen-emulation-rotate-span.msft.png":::
   <span data-ttu-id="4991f-135">Matrix von Haltungen und Ausrichtungen für Dualscreen- und faltbare Geräte</span><span class="sxs-lookup"><span data-stu-id="4991f-135">Matrix of postures and orientations for dual-screen and foldable devices</span></span>  
:::image-end:::  

<span data-ttu-id="4991f-136">Das **Symbol Experimental Web Platform features** \( ExperimentalApis \) zeigt den Status des ![ ](../media/experimental-apis-dark-icon.msft.png) **Features-Flag der Experimentellen Webplattform** an.</span><span class="sxs-lookup"><span data-stu-id="4991f-136">The **Experimental Web Platform features** \(![ExperimentalApis](../media/experimental-apis-dark-icon.msft.png)\) icon displays the state of the **Experimental Web Platform features** flag.</span></span>  <span data-ttu-id="4991f-137">Wenn das Flag aktiviert ist, wird das Symbol hervorgehoben.</span><span class="sxs-lookup"><span data-stu-id="4991f-137">If the flag is turned on, the icon is highlighted.</span></span>  <span data-ttu-id="4991f-138">Wenn das Flag deaktiviert ist, wird das Symbol nicht hervorgehoben.</span><span class="sxs-lookup"><span data-stu-id="4991f-138">If the flag is turned off, the icon is not highlighted.</span></span>  <span data-ttu-id="4991f-139">Um das Flag \(oder off\) zu aktivieren, wählen Sie entweder das Symbol aus, oder navigieren Sie zu und schalten `edge://flags` Sie das Flag um.</span><span class="sxs-lookup"><span data-stu-id="4991f-139">To turn on \(or off\) the flag, either choose the icon or navigate to `edge://flags` and toggle the flag.</span></span>  

> [!NOTE]
> <span data-ttu-id="4991f-140">Im Folgenden finden Sie eine Liste der aktuellen bekannten Probleme.</span><span class="sxs-lookup"><span data-stu-id="4991f-140">The following is a list of current known issues.</span></span>  
> 
> *   <span data-ttu-id="4991f-141">Wenn Sie einen [Microsoft-Remotedesktop verwenden,][RemoteDesktopClientDocs] um eine Verbindung mit einem Remote-PC herzustellen und das [Surface Duo][SurfaceDevicesDuo] oder das [Samsung -Galaxis-Fold-Gerät][SamsungMobileGalaxyFold]zu emulieren, kann der Zeiger wackeln oder stottern.</span><span class="sxs-lookup"><span data-stu-id="4991f-141">When you use a [Microsoft Remote Desktop client][RemoteDesktopClientDocs] to connect to a remote PC and emulate the [Surface Duo][SurfaceDevicesDuo] or [Samsung Galaxy Fold][SamsungMobileGalaxyFold], the pointer may shake or stutter.</span></span>  <span data-ttu-id="4991f-142">Wenn Sie das Problem haben, senden [Sie Feedback](#getting-in-touch-with-the-microsoft-edge-devtools-team).</span><span class="sxs-lookup"><span data-stu-id="4991f-142">If you run into the issue, [send feedback](#getting-in-touch-with-the-microsoft-edge-devtools-team).</span></span>  

## <a name="additional-resources"></a><span data-ttu-id="4991f-143">Weitere Ressourcen</span><span class="sxs-lookup"><span data-stu-id="4991f-143">Additional Resources</span></span>  

<span data-ttu-id="4991f-144">Hier finden Sie weitere Ressourcen, die Ihnen bei der Verbesserung Ihrer Website \(oder App\) für Dual-Screen-Geräte helfen können.</span><span class="sxs-lookup"><span data-stu-id="4991f-144">Here are additional resources that may help you enhance your website \(or app\) for dual-screen devices.</span></span>  

*   <span data-ttu-id="4991f-145">Weitere Informationen zur Webentwicklung auf Dual-Screen-Geräten finden Sie unter [Dual-screen web experiences][DualScreenWebIndex].</span><span class="sxs-lookup"><span data-stu-id="4991f-145">For more information about web development on dual-screen devices, navigate to [Dual-screen web experiences][DualScreenWebIndex].</span></span>  
*   <span data-ttu-id="4991f-146">Installieren Sie den [Surface Duo-Emulator][DualScreenAndroidUseEmulator].</span><span class="sxs-lookup"><span data-stu-id="4991f-146">Install the [Surface Duo emulator][DualScreenAndroidUseEmulator].</span></span>  <span data-ttu-id="4991f-147">Der Surface Duo-Emulator ist anders als der Emulator in Microsoft Edge, führt Android aus und integriert sich in [Android Studio.][AndroidDeveloperStudio]</span><span class="sxs-lookup"><span data-stu-id="4991f-147">The Surface Duo emulator is different from the emulator in Microsoft Edge, runs Android, and integrates with [Android Studio][AndroidDeveloperStudio].</span></span>  <span data-ttu-id="4991f-148">Weitere Informationen finden Sie unter [Get the Surface Duo SDK][DualScreenAndroidGetDuoSdk].</span><span class="sxs-lookup"><span data-stu-id="4991f-148">For more information, navigate to [Get the Surface Duo SDK][DualScreenAndroidGetDuoSdk].</span></span>  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="4991f-149">Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen</span><span class="sxs-lookup"><span data-stu-id="4991f-149">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsDeviceModeIndexSimulateMobileViewport]: ../device-mode/index.md#simulate-a-mobile-viewport "Simulieren mobiler Geräte mit gerätemodus in Microsoft Edge DevTools | Microsoft Edge"  

[DualScreenWebIndex]: /dual-screen/web/index "Dualscreen-Weberfahrungen | Microsoft Docs"  
[DualScreenAndroidGetDuoSdk]: /dual-screen/android/get-duo-sdk "Laden Sie den Surface Duo-Emulator | Microsoft Docs"  
[DualScreenIntroductionHowWorkSeam]: /dual-screen/introduction#how-to-work-with-the-seam "Arbeiten mit der Naht – Einführung in Geräten mit dualem Bildschirm | Microsoft Docs"  
[DualScreenAndroidUseEmulator]: /dual-screen/android/use-emulator "Verwenden des Surface Duo-Emulators | Microsoft Docs"  
[DualScreenDocsCssMedia]: /dual-screen/web/css-media-spanning "Feature „CSS-Medienbildschirmaufteilung“ für die Erkennung von dualem Bildschirm | Microsoft Docs"  
[DualScreenDocsJSAPI]: /dual-screen/web/javascript-getwindowsegments "Die API „getWindowSegments JavaScript“ für Geräte mit dualem Bildschirm | Microsoft Docs"  

[RemoteDesktopClientDocs]: /windows-server/remote/remote-desktop-services/clients/remote-desktop-clients "Remotedesktopclients | Microsoft Docs"

[MicrosoftEdge]: https://www.microsoft.com/edge "Microsoft Edge"  

[SurfaceDevicesDuo]: https://www.microsoft.com/surface/devices/surface-duo "Surface Duo | Microsoft Surface"  

[AndroidDeveloperStudio]: https://developer.android.com/studio/ "Android Studio"  

[GooglePlayMicrosoftEdge]: https://play.google.com/store/apps/details?id=com.microsoft.emmx "Microsoft Edge | Google Play"  

[SamsungMobileGalaxyFold]: https://www.samsung.com/global/galaxy/galaxy-fold "Galaxis fold | Samsung"  
