---
description: Verwenden Sie virtuelle Geräte in Microsoft Edge, um Ihre Website für Dualbildschirme und ausklappbare Geräte zu verbessern.
title: Emulieren von Dualbildschirmen und ausklappbaren Geräten in Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/02/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, f12-Tools, DevTools, Emulation, Gerät, Simulation, mobil, Dual-Screen, ausklappbar, Surface Duo, Samsung Unterdruck Fold
ms.openlocfilehash: bc91c0b7c917d82f169dc7d47e047a587d505353
ms.sourcegitcommit: 12c30ad4ab2664d17c9b7e9d59d7a3cda60ff65c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/04/2021
ms.locfileid: "11313239"
---
# <span data-ttu-id="aceb2-104">Emulieren von Dualbildschirmen und ausklappbaren Geräten in Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="aceb2-104">Emulate dual-screen and foldable devices in Microsoft Edge DevTools</span></span>  

<span data-ttu-id="aceb2-105">In Microsoft Edge, Version 89 oder höher, können Sie die folgenden Dualbildschirme und ausklappbaren Geräte emulieren.</span><span class="sxs-lookup"><span data-stu-id="aceb2-105">In Microsoft Edge version 89 or later, you may emulate the following dual-screen and foldable devices.</span></span>  

*   [<span data-ttu-id="aceb2-106">Surface Duo</span><span class="sxs-lookup"><span data-stu-id="aceb2-106">Surface Duo</span></span>][SurfaceDevicesDuo]  
*   [<span data-ttu-id="aceb2-107">Samsung Verknappung</span><span class="sxs-lookup"><span data-stu-id="aceb2-107">Samsung Galaxy Fold</span></span>][SamsungMobileGalaxyFold]  
    
<span data-ttu-id="aceb2-108">Emulieren Sie die Geräte, und schalten Sie zwischen den folgenden Haltungen um.</span><span class="sxs-lookup"><span data-stu-id="aceb2-108">Emulate the devices and toggle between the following postures.</span></span>  

*   <span data-ttu-id="aceb2-109">Einzelbildschirm oder geklappte Haltung</span><span class="sxs-lookup"><span data-stu-id="aceb2-109">Single-screen or folded posture</span></span>  
*   <span data-ttu-id="aceb2-110">Dualbildschirm oder aufgefunktioniertes Bild</span><span class="sxs-lookup"><span data-stu-id="aceb2-110">Dual-screen or unfolded posture</span></span>  
    
<span data-ttu-id="aceb2-111">Aktivieren Sie [experimentelle Webplattform-APIs,](#turn-on-experimental-apis) und verwenden Sie die [CSS-Medienbildschirm-übergreifende][DualScreenDocsCssMedia] Funktion und [javaScript getWindowSegments-API,][DualScreenDocsJSAPI] um Ihre Website \(oder App\) für Dualbildschirme und ausklappbare Geräte zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="aceb2-111">[Turn on experimental Web Platform APIs](#turn-on-experimental-apis) and use the [CSS media screen-spanning feature][DualScreenDocsCssMedia] and [JavaScript getWindowSegments API][DualScreenDocsJSAPI] to enhance your website \(or app\) for dual-screen and foldable devices.</span></span>  

:::image type="complex" source="../media/experiments-surface-duo-emulation.msft.png" alt-text="Emulieren von Surface Duo in Microsoft Edge" lightbox="../media/experiments-surface-duo-emulation.msft.png":::  
   <span data-ttu-id="aceb2-113">Emulieren von Surface Duo in Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="aceb2-113">Emulate Surface Duo in Microsoft Edge</span></span>  
:::image-end:::  

## <span data-ttu-id="aceb2-114">Aktivieren experimenteller APIs</span><span class="sxs-lookup"><span data-stu-id="aceb2-114">Turn on experimental APIs</span></span>  

<span data-ttu-id="aceb2-115">Aktivieren Sie das Flag in Microsoft Edge, um das Feature für den Bildschirmbereich von [CSS-Medien][DualScreenDocsCssMedia] und die [JavaScript-getWindowSegments-API][DualScreenDocsJSAPI] `Experimental Web Platform features` zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="aceb2-115">To use the [CSS media screen-spanning feature][DualScreenDocsCssMedia] and [JavaScript getWindowSegments API][DualScreenDocsJSAPI], turn on the `Experimental Web Platform features` flag in Microsoft Edge.</span></span>  <span data-ttu-id="aceb2-116">Führen Sie die folgenden Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="aceb2-116">Complete the following steps.</span></span>  

1.  <span data-ttu-id="aceb2-117">Navigieren Sie zu `edge://flags` .</span><span class="sxs-lookup"><span data-stu-id="aceb2-117">Navigate to `edge://flags`.</span></span>  
1.  <span data-ttu-id="aceb2-118">Geben Sie **im Textfeld "Suchkennzeichen"** die Option `Experimental Web Platform features` **"Experimentelle Webplattform-Features"** ein, und ändern Sie **"Deaktiviert"** in **"Aktiviert".**</span><span class="sxs-lookup"><span data-stu-id="aceb2-118">In the **Search flags** textbox, enter `Experimental Web Platform features`, choose the **Experimental Web Platform features** flag, and change **Disabled** to **Enabled**.</span></span>  
1.  <span data-ttu-id="aceb2-119">Starten Sie Microsoft Edge neu.</span><span class="sxs-lookup"><span data-stu-id="aceb2-119">Restart Microsoft Edge.</span></span>  
    
:::image type="complex" source="../media/experiments-dual-screen-emulation-edge-flags.msft.png" alt-text="Aktivieren der Kennzeichnung für experimentelle Webplattformfeatures" lightbox="../media/experiments-dual-screen-emulation.msft.png":::
   <span data-ttu-id="aceb2-121">Aktivieren der **Kennzeichnung für experimentelle Webplattformfeatures**</span><span class="sxs-lookup"><span data-stu-id="aceb2-121">Turn on the **Experimental Web Platform features** flag</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="aceb2-122">Wenn Sie CSS-Medienabfragen oder die [JavaScript-Windows-Segment-Enumerations-API][DualScreenDocsJSAPI] verwenden, um Ihre Website oder App für [Surface Duo][SurfaceDevicesDuo]zu verbessern, müssen Sie auch das Flag **"Experimentelle WebPlattform-Features"** in der [Android Microsoft Edge-App][GooglePlayMicrosoftEdge] auf Ihrem [Surface Duo-Gerät][SurfaceDevicesDuo] aktivieren. [][DualScreenDocsCssMedia]</span><span class="sxs-lookup"><span data-stu-id="aceb2-122">If you are using [CSS media queries][DualScreenDocsCssMedia] or the [JavaScript Windows Segment Enumeration API][DualScreenDocsJSAPI] to enhance your website or app for the [Surface Duo][SurfaceDevicesDuo], you must also turn on the **Experimental Web Platform features** flag in the [Android Microsoft Edge app][GooglePlayMicrosoftEdge] on your [Surface Duo][SurfaceDevicesDuo] device.</span></span>  
> 
> <span data-ttu-id="aceb2-123">Wenn das Flag für experimentelle Webplattformfeatures im Microsoft [Edge][MicrosoftEdge] Desktop aktiviert und in der [Android Microsoft][GooglePlayMicrosoftEdge]Edge-App deaktiviert ist, ist das Verhalten Ihrer Website oder App im Surface Duo-Emulator im Desktop von Microsoft Edge nicht mit der [Android Microsoft Edge-App][GooglePlayMicrosoftEdge] auf [Surface Duo kompatibel.][SurfaceDevicesDuo] </span><span class="sxs-lookup"><span data-stu-id="aceb2-123">If the **Experimental Web Platform features** flag is turned on in [desktop Microsoft Edge][MicrosoftEdge] and turned off in the [Android Microsoft Edge app][GooglePlayMicrosoftEdge], the behavior of your website or app in the Surface Duo emulator in desktop Microsoft Edge does not match with the [Android Microsoft Edge app][GooglePlayMicrosoftEdge] on [Surface Duo][SurfaceDevicesDuo].</span></span>  <span data-ttu-id="aceb2-124">Stellen Sie sicher, dass die Flags in Android- und Desktop-Microsoft Edge übereinstimmen, um den Surface Duo-Emulator im Microsoft Edge [Desktop erfolgreich zu verwenden.][MicrosoftEdge]</span><span class="sxs-lookup"><span data-stu-id="aceb2-124">Ensure that the flags match across Android and desktop Microsoft Edge to successfully use the Surface Duo emulator in [desktop Microsoft Edge][MicrosoftEdge].</span></span>  

## <span data-ttu-id="aceb2-125">Testen auf ausklappbaren und Dualbildschirmgeräten</span><span class="sxs-lookup"><span data-stu-id="aceb2-125">Test on foldable and dual-screen devices</span></span>  

<span data-ttu-id="aceb2-126">Wenn Sie das [Surface Duo][SurfaceDevicesDuo] in einem dualen Bildschirm in Microsoft Edge emulieren, wird die Naht \(der Abstand zwischen den beiden Bildschirmen\) über Ihrer Website oder App gezeichnet.</span><span class="sxs-lookup"><span data-stu-id="aceb2-126">When you emulate the [Surface Duo][SurfaceDevicesDuo] in a dual-screen posture in Microsoft Edge, the seam \(the space between the two screens\) is drawn over your website or app.</span></span>  

<span data-ttu-id="aceb2-127">Die emulierte Anzeige entspricht der Art und Weise, wie Ihre Website \(oder App\) in der [Microsoft Edge -Android-App][GooglePlayMicrosoftEdge] gerendert wird, während sie auf [Surface Duo ausgeführt wird.][SurfaceDevicesDuo]</span><span class="sxs-lookup"><span data-stu-id="aceb2-127">The emulated display matches the way your website \(or app\) renders in the [Microsoft Edge Android app][GooglePlayMicrosoftEdge] while running on [Surface Duo][SurfaceDevicesDuo].</span></span>  <span data-ttu-id="aceb2-128">Möglicherweise müssen Sie Ihre Website \(oder App\) aktualisieren, damit sie am Nahtstrich besser angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="aceb2-128">You may have to update your website \(or app\) to display better along the seam.</span></span>  <span data-ttu-id="aceb2-129">Weitere Informationen zum Anpassen Ihrer Website \(oder app\) an die Naht finden Sie unter "Arbeiten mit [der Naht".][DualScreenIntroductionHowWorkSeam]</span><span class="sxs-lookup"><span data-stu-id="aceb2-129">For more information about adapting your website \(or app\) to the seam, navigate to [How to work with the seam][DualScreenIntroductionHowWorkSeam].</span></span>  

<span data-ttu-id="aceb2-130">Die [Gerätesymbolleiste][DevtoolsDeviceModeIndexSimulateMobileViewport] bietet zusätzliche Features, mit deren Hilfe Sie Ihre Website oder App in mehreren Haltungen und Ausrichtungen testen können.</span><span class="sxs-lookup"><span data-stu-id="aceb2-130">The [Device Toolbar][DevtoolsDeviceModeIndexSimulateMobileViewport] has additional features to help you test your website or app in multiple postures and orientations.</span></span>  <span data-ttu-id="aceb2-131">Choose **Rotate** \( ![ Rotate ](../media/rotate-dark-icon.msft.png) \) to rotate the viewport to landscape orientation.</span><span class="sxs-lookup"><span data-stu-id="aceb2-131">Choose **Rotate** \(![Rotate](../media/rotate-dark-icon.msft.png)\) to rotate the viewport to landscape orientation.</span></span> <span data-ttu-id="aceb2-132">Kombinieren Sie das Feature mit **Span** \( Span \), um zwischen einem einzelnen Bildschirm oder gefalteten und dualen Bildschirmen oder aufgeklappten ![ ](../media/span-dark-icon.msft.png) Postures umschalten zu können.</span><span class="sxs-lookup"><span data-stu-id="aceb2-132">Combine the feature with **Span** \(![Span](../media/span-dark-icon.msft.png)\) to toggle between single-screen or folded and dual-screen or unfolded postures.</span></span>  <span data-ttu-id="aceb2-133">Zusammen können Sie mit den Features Ihre Website oder App in allen vier möglichen Haltungen und Ausrichtungen testen.</span><span class="sxs-lookup"><span data-stu-id="aceb2-133">Together, the features allow you to test your website or app in all four possible postures and orientations.</span></span>  

:::image type="complex" source="../media/experiments-dual-screen-emulation-rotate-span.msft.png" alt-text="Matrix der Haltungen und Ausrichtungen für Dualbildschirme und ausklappbare Geräte" lightbox="../media/experiments-dual-screen-emulation-rotate-span.msft.png":::
   <span data-ttu-id="aceb2-135">Matrix der Haltungen und Ausrichtungen für Dualbildschirme und ausklappbare Geräte</span><span class="sxs-lookup"><span data-stu-id="aceb2-135">Matrix of postures and orientations for dual-screen and foldable devices</span></span>  
:::image-end:::  

<span data-ttu-id="aceb2-136">Das **Symbol für experimentelle Webplattformfeatures** \( ExperimentalApis \) zeigt den Status des Features der ![ ](../media/experimental-apis-dark-icon.msft.png) **experimentellen Webplattform** an.</span><span class="sxs-lookup"><span data-stu-id="aceb2-136">The **Experimental Web Platform features** \(![ExperimentalApis](../media/experimental-apis-dark-icon.msft.png)\) icon displays the state of the **Experimental Web Platform features** flag.</span></span>  <span data-ttu-id="aceb2-137">Wenn das Flag aktiviert ist, wird das Symbol hervorgehoben.</span><span class="sxs-lookup"><span data-stu-id="aceb2-137">If the flag is turned on, the icon is highlighted.</span></span>  <span data-ttu-id="aceb2-138">Wenn das Flag deaktiviert ist, wird das Symbol nicht hervorgehoben.</span><span class="sxs-lookup"><span data-stu-id="aceb2-138">If the flag is turned off, the icon is not highlighted.</span></span>  <span data-ttu-id="aceb2-139">Um das Flag zu aktivieren (oder zu deaktivieren), wählen Sie entweder das Symbol aus, oder navigieren Sie zu dem Flag, und schalten `edge://flags` Sie es um.</span><span class="sxs-lookup"><span data-stu-id="aceb2-139">To turn on \(or off\) the flag, either choose the icon or navigate to `edge://flags` and toggle the flag.</span></span>  

> [!NOTE]
> <span data-ttu-id="aceb2-140">Im Folgenden finden Sie eine Liste der aktuellen bekannten Probleme.</span><span class="sxs-lookup"><span data-stu-id="aceb2-140">The following is a list of current known issues.</span></span>  
> 
> *   <span data-ttu-id="aceb2-141">Wenn Sie einen [Microsoft Remote Desktop Client][RemoteDesktopClientDocs] verwenden, um eine Verbindung mit einem Remote-PC herzustellen und das Surface [Duo][SurfaceDevicesDuo] oder [Das Unterflag von Samsung zu][SamsungMobileGalaxyFold]emulieren, kann der Zeiger wackeln oder unübersichtlich werden.</span><span class="sxs-lookup"><span data-stu-id="aceb2-141">When you use a [Microsoft Remote Desktop client][RemoteDesktopClientDocs] to connect to a remote PC and emulate the [Surface Duo][SurfaceDevicesDuo] or [Samsung Galaxy Fold][SamsungMobileGalaxyFold], the pointer may shake or stutter.</span></span>  <span data-ttu-id="aceb2-142">Wenn das Problem vor sich geht, senden [Sie Feedback.](#getting-in-touch-with-the-microsoft-edge-devtools-team)</span><span class="sxs-lookup"><span data-stu-id="aceb2-142">If you run into the issue, [send feedback](#getting-in-touch-with-the-microsoft-edge-devtools-team).</span></span>  

## <span data-ttu-id="aceb2-143">Weitere Ressourcen</span><span class="sxs-lookup"><span data-stu-id="aceb2-143">Additional Resources</span></span>  

<span data-ttu-id="aceb2-144">Hier finden Sie weitere Ressourcen, die Sie bei der Verbesserung Ihrer Website \(oder App\) für Dual-Screen-Geräte unterstützen können.</span><span class="sxs-lookup"><span data-stu-id="aceb2-144">Here are additional resources that may help you enhance your website \(or app\) for dual-screen devices.</span></span>  

*   <span data-ttu-id="aceb2-145">Weitere Informationen zur Webentwicklung auf Dual-Screen-Geräten finden Sie unter ["Dual-screen web experiences".][DualScreenWebIndex]</span><span class="sxs-lookup"><span data-stu-id="aceb2-145">For more information about web development on dual-screen devices, navigate to [Dual-screen web experiences][DualScreenWebIndex].</span></span>  
*   <span data-ttu-id="aceb2-146">Installieren Sie den [Surface Duo-Emulator.][DualScreenAndroidUseEmulator]</span><span class="sxs-lookup"><span data-stu-id="aceb2-146">Install the [Surface Duo emulator][DualScreenAndroidUseEmulator].</span></span>  <span data-ttu-id="aceb2-147">Der Surface Duo Emulator ist anders als der Emulator in Microsoft Edge, führt Android aus und kann in [Android Studio integriert werden.][AndroidDeveloperStudio]</span><span class="sxs-lookup"><span data-stu-id="aceb2-147">The Surface Duo emulator is different from the emulator in Microsoft Edge, runs Android, and integrates with [Android Studio][AndroidDeveloperStudio].</span></span>  <span data-ttu-id="aceb2-148">Weitere Informationen finden Sie unter ["Surface Duo SDK erhalten".][DualScreenAndroidGetDuoSdk]</span><span class="sxs-lookup"><span data-stu-id="aceb2-148">For more information, navigate to [Get the Surface Duo SDK][DualScreenAndroidGetDuoSdk].</span></span>  

## <span data-ttu-id="aceb2-149">Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen</span><span class="sxs-lookup"><span data-stu-id="aceb2-149">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsDeviceModeIndexSimulateMobileViewport]: ../device-mode/index.md#simulate-a-mobile-viewport "Simulieren mobiler Geräte mit dem Gerätemodus in Microsoft Edge DevTools | Microsoft Edge"  

[DualScreenWebIndex]: /dual-screen/web/index "Weberfahrungen auf zwei | Microsoft Docs"  
[DualScreenAndroidGetDuoSdk]: /dual-screen/android/get-duo-sdk "Surface Duo-Emulator-| Microsoft Docs"  
[DualScreenIntroductionHowWorkSeam]: /dual-screen/introduction#how-to-work-with-the-seam "So arbeiten Sie mit der Naht – Einführung in duale Bildschirmgeräte | Microsoft Docs"  
[DualScreenAndroidUseEmulator]: /dual-screen/android/use-emulator "Verwenden der Surface Duo-Emulator-| Microsoft Docs"  
[DualScreenDocsCssMedia]: /dual-screen/web/css-media-spanning "Feature für bildschirmübergreifende CSS-Medien für die Erkennung von | Microsoft Docs"  
[DualScreenDocsJSAPI]: /dual-screen/web/javascript-getwindowsegments "Die getWindowSegments-JavaScript-API für Dualbildschirmgeräte | Microsoft Docs"  

[RemoteDesktopClientDocs]: /windows-server/remote/remote-desktop-services/clients/remote-desktop-clients "Remotedesktopclients | Microsoft Docs"

[MicrosoftEdge]: https://www.microsoft.com/edge "Microsoft Edge"  

[SurfaceDevicesDuo]: https://www.microsoft.com/surface/devices/surface-duo "Surface Duo | Microsoft Surface"  

[AndroidDeveloperStudio]: https://developer.android.com/studio/ "Android Studio"  

[GooglePlayMicrosoftEdge]: https://play.google.com/store/apps/details?id=com.microsoft.emmx "Microsoft Edge | Google Play"  

[SamsungMobileGalaxyFold]: https://www.samsung.com/mobile/galaxy-fold/ "1-1-| Samsung"  
