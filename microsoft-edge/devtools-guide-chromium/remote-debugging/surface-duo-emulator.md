---
description: Erste Schritte mit Remote debugging Surface Duo-Emulatoren.
title: Erste Schritte mit Remotedebu debugging Surface Duo-Emulatoren
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/08/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, web development, f12 tools, devtools, remote debugging, android, surface duo
ms.openlocfilehash: 61f903a5b929b7ee7b924938cf6ddc21a9783ca7
ms.sourcegitcommit: 4b9fb5c1176fdaa5e3c60af2b84e38d5bb86cd81
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/16/2021
ms.locfileid: "11439328"
---
# <a name="get-started-with-remote-debugging-surface-duo-emulators"></a><span data-ttu-id="ffd55-104">Erste Schritte mit Remotedebu debugging Surface Duo-Emulatoren</span><span class="sxs-lookup"><span data-stu-id="ffd55-104">Get started with Remote Debugging Surface Duo emulators</span></span>  

<span data-ttu-id="ffd55-105">In diesem Artikel werden Sie durch den Prozess des Remotedebugierens Ihrer Webinhalte in der [Microsoft Edge-App][GooglePlayStoreAppsComMicrosoftEmmx] auf einem [Surface Duo-Emulator][MicrosoftSurfaceDevicesSurfaceDuo] von einer Desktopinstanz von Microsoft Edge [aus beschrieben.][MicrosoftEdge]</span><span class="sxs-lookup"><span data-stu-id="ffd55-105">In this article, you walk through the process of remotely debugging your web content in the [Microsoft Edge app][GooglePlayStoreAppsComMicrosoftEmmx] on a [Surface Duo][MicrosoftSurfaceDevicesSurfaceDuo] emulator from a desktop instance of [Microsoft Edge][MicrosoftEdge].</span></span>  <span data-ttu-id="ffd55-106">Informationen zum Debuggen auf einem Surface Duo-Gerät finden Sie in unserem Leitfaden zum [Remotedebugen von Android-Geräten.][DevtoolsRemoteDebuggingMain]</span><span class="sxs-lookup"><span data-stu-id="ffd55-106">For information on debugging on a Surface Duo device, follow our guide for [remote debugging Android devices][DevtoolsRemoteDebuggingMain].</span></span>  

## <a name="before-you-begin"></a><span data-ttu-id="ffd55-107">Bevor Sie beginnen</span><span class="sxs-lookup"><span data-stu-id="ffd55-107">Before you Begin</span></span>

<span data-ttu-id="ffd55-108">Installieren Sie [das Surface Duo SDK,][MicrosoftDownload100847] bevor Sie den [Surface Duo-Emulator ausführen.][DualScreenAndroidUseEmulator]</span><span class="sxs-lookup"><span data-stu-id="ffd55-108">Install the [Surface Duo SDK][MicrosoftDownload100847] before running the [Surface Duo emulator][DualScreenAndroidUseEmulator].</span></span>  <span data-ttu-id="ffd55-109">Weitere Informationen finden Sie unter [Get the Surface Duo SDK][DualScreenAndroidGetDuoSdk].</span><span class="sxs-lookup"><span data-stu-id="ffd55-109">For more information, navigate to [Get the Surface Duo SDK][DualScreenAndroidGetDuoSdk].</span></span>  

## <a name="step-1-navigate-to-edgeinspect"></a><span data-ttu-id="ffd55-110">Schritt 1: Navigieren Sie zu edge://inspect</span><span class="sxs-lookup"><span data-stu-id="ffd55-110">Step 1: Navigate to edge://inspect</span></span>  

<span data-ttu-id="ffd55-111">Öffnen Sie eine Desktopinstanz [von Microsoft Edge,][MicrosoftEdge]und navigieren Sie zu `edge://inspect` .</span><span class="sxs-lookup"><span data-stu-id="ffd55-111">Open a desktop instance of [Microsoft Edge][MicrosoftEdge], and navigate to `edge://inspect`.</span></span>  

:::image type="complex" source="../media/remote-debugging-surface-duo-inspect-page.msft.png" alt-text="Die edge://inspect in Microsoft Edge auf dem Desktop" lightbox="../media/remote-debugging-surface-duo-inspect-page.msft.png":::
   <span data-ttu-id="ffd55-113">Die `edge://inspect` Seite in Microsoft Edge auf dem Desktop</span><span class="sxs-lookup"><span data-stu-id="ffd55-113">The `edge://inspect` page in Microsoft Edge on the desktop</span></span>  
:::image-end:::

> [!NOTE]
> <span data-ttu-id="ffd55-114">Wenn die `edge://inspect` Seite den Surface [Duo-Emulator][DualScreenAndroidUseEmulator]nicht erkennt, starten Sie den Emulator neu.</span><span class="sxs-lookup"><span data-stu-id="ffd55-114">If the `edge://inspect` page does not recognize the [Surface Duo emulator][DualScreenAndroidUseEmulator], restart the emulator.</span></span>  

## <a name="step-2-launch-the-surface-duo-emulator"></a><span data-ttu-id="ffd55-115">Schritt 2: Starten des Surface Duo-Emulators</span><span class="sxs-lookup"><span data-stu-id="ffd55-115">Step 2: Launch the Surface Duo emulator</span></span>  

<span data-ttu-id="ffd55-116">Starten Sie den [Surface Duo-Emulator.][DualScreenAndroidUseEmulator]</span><span class="sxs-lookup"><span data-stu-id="ffd55-116">Launch the [Surface Duo emulator][DualScreenAndroidUseEmulator].</span></span>  <span data-ttu-id="ffd55-117">Beachten Sie, dass der Emulator zwei verschiedene Bildschirme anzeigt, die auf dem Emulator ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="ffd55-117">Notice that the emulator displays 2 different screens running on the emulator.</span></span>  

:::image type="complex" source="../media/remote-debugging-surface-duo-emulator.msft.png" alt-text="Der Surface Duo-Emulator" lightbox="../media/remote-debugging-surface-duo-emulator.msft.png":::
   <span data-ttu-id="ffd55-119">Der Surface Duo-Emulator</span><span class="sxs-lookup"><span data-stu-id="ffd55-119">The Surface Duo emulator</span></span>  
:::image-end:::  

## <a name="step-3-load-your-web-content-in-microsoft-edge-on-the-surface-duo-emulator"></a><span data-ttu-id="ffd55-120">Schritt 3: Laden von Webinhalten in Microsoft Edge im Surface Duo-Emulator</span><span class="sxs-lookup"><span data-stu-id="ffd55-120">Step 3: Load your web content in Microsoft Edge on the Surface Duo emulator</span></span>  

<span data-ttu-id="ffd55-121">Wischen Sie auf beiden Bildschirmen im Favoritenfach des [Surface Duo-Emulators][DualScreenAndroidUseEmulator] nach oben, um die Apps-Drawer anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="ffd55-121">On either screen, swipe up on the Favorites Tray of the [Surface Duo emulator][DualScreenAndroidUseEmulator] to display the Apps Drawer.</span></span>  <span data-ttu-id="ffd55-122">Wählen **Sie Edge** aus, um die Microsoft [Edge-App zu starten.][GooglePlayStoreAppsComMicrosoftEmmx]</span><span class="sxs-lookup"><span data-stu-id="ffd55-122">Choose **Edge** to launch the [Microsoft Edge app][GooglePlayStoreAppsComMicrosoftEmmx].</span></span>  

:::image type="complex" source="../media/remote-debugging-surface-duo-emulator-edge.msft.png" alt-text="Die Microsoft Edge-App auf dem Surface Duo-Emulator" lightbox="../media/remote-debugging-surface-duo-emulator-edge.msft.png":::
   <span data-ttu-id="ffd55-124">Die Microsoft Edge-App auf dem Surface Duo-Emulator</span><span class="sxs-lookup"><span data-stu-id="ffd55-124">The Microsoft Edge app on the Surface Duo emulator</span></span>  
:::image-end:::  

<span data-ttu-id="ffd55-125">Navigieren Sie zu der Website oder App, die Sie in der [Microsoft Edge-App debuggen möchten.][GooglePlayStoreAppsComMicrosoftEmmx]</span><span class="sxs-lookup"><span data-stu-id="ffd55-125">Navigate to the website or app that you want to debug in the [Microsoft Edge app][GooglePlayStoreAppsComMicrosoftEmmx].</span></span>  

## <a name="step-4-debug-your-web-content-from-the-surface-duo-emulator"></a><span data-ttu-id="ffd55-126">Schritt 4: Debuggen Von Webinhalten aus dem Surface Duo-Emulator</span><span class="sxs-lookup"><span data-stu-id="ffd55-126">Step 4: Debug your web content from the Surface Duo emulator</span></span>  

<span data-ttu-id="ffd55-127">Wechseln Sie zurück zur Desktopinstanz von [Microsoft Edge][MicrosoftEdge].</span><span class="sxs-lookup"><span data-stu-id="ffd55-127">Switch back to the desktop instance of [Microsoft Edge][MicrosoftEdge].</span></span>  <span data-ttu-id="ffd55-128">Auf `edge://inspect` der Seite wird nun **surfaceDuoEmulator** mit einer Liste der geöffneten Registerkarten oder [PWAs][ProgressiveWebAppsIndex] angezeigt, die im [Surface Duo-Emulator ausgeführt werden.][DualScreenAndroidUseEmulator]</span><span class="sxs-lookup"><span data-stu-id="ffd55-128">The `edge://inspect` page now shows the **SurfaceDuoEmulator** with a list of the open tabs or [PWAs][ProgressiveWebAppsIndex] that are running on the [Surface Duo emulator][DualScreenAndroidUseEmulator].</span></span>  

:::image type="complex" source="../media/remote-debugging-surface-duo-inspect-page-with-targets.msft.png" alt-text="Auf edge://inspect wird eine Liste der geöffneten Registerkarten in der Microsoft Edge-App angezeigt, die auf dem Emulator ausgeführt wird." lightbox="../media/remote-debugging-surface-duo-inspect-page-with-targets.msft.png":::
   <span data-ttu-id="ffd55-130">Auf `edge://inspect` der Seite wird eine Liste der geöffneten Registerkarten in der Microsoft Edge-App angezeigt, die auf dem Emulator ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ffd55-130">The `edge://inspect` page displays a list of the open tabs in the Microsoft Edge app running on the emulator</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="ffd55-131">Wenn **SurfaceDuoEmulator** nicht auf der Seite angezeigt wird, versuchen Sie, Registerkarten in der Microsoft Edge-App im `edge://inspect` Surface [Duo-Emulator][DualScreenAndroidUseEmulator]zu öffnen oder zu schließen. [][GooglePlayStoreAppsComMicrosoftEmmx]</span><span class="sxs-lookup"><span data-stu-id="ffd55-131">If **SurfaceDuoEmulator** is not displayed on the `edge://inspect` page, try opening or closing tabs in the [Microsoft Edge app][GooglePlayStoreAppsComMicrosoftEmmx] on the [Surface Duo Emulator][DualScreenAndroidUseEmulator].</span></span>  <span data-ttu-id="ffd55-132">Weitere Schritte zur Problembehandlung finden Sie im [Abschnitt Problembehandlung für Android-Geräte.][DevtoolsRemoteDebuggingIndexTroubleshootingDevtoolsIsNotDetectingAndroidDevice]</span><span class="sxs-lookup"><span data-stu-id="ffd55-132">For additional troubleshooting steps, navigate to [troubleshooting section for Android devices][DevtoolsRemoteDebuggingIndexTroubleshootingDevtoolsIsNotDetectingAndroidDevice].</span></span>  

<span data-ttu-id="ffd55-133">Wählen Sie in der Liste der geöffneten Registerkarten, die auf dem Emulator ausgeführt werden, auf der Registerkarte überprüfen aus, auf der die zu debuggenden Webinhalte enthalten sind. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="ffd55-133">From the list of open tabs running on the emulator, choose **inspect** on the tab that has the web content to be debugged.</span></span>  <span data-ttu-id="ffd55-134">Die [Microsoft Edge DevTools][DevtoolsIndex] werden in einem neuen Fenster geöffnet.</span><span class="sxs-lookup"><span data-stu-id="ffd55-134">The [Microsoft Edge DevTools][DevtoolsIndex] will open in a new window.</span></span>  <span data-ttu-id="ffd55-135">Wählen **Sie Screencast umschalten** \( Screencast umschalten \), um den Webinhalt aus dem Surface Duo-Emulator im ![ ](../media/toggle-screencast-icon.msft.png) DevTools-Fenster anzuzeigen. [][DualScreenAndroidUseEmulator]</span><span class="sxs-lookup"><span data-stu-id="ffd55-135">Choose **Toggle Screencast** \(![Toggle Screencast](../media/toggle-screencast-icon.msft.png)\) to view the web content from your [Surface Duo emulator][DualScreenAndroidUseEmulator] in the DevTools window.</span></span>  <span data-ttu-id="ffd55-136">Sie können jetzt die Microsoft Edge DevTools verwenden, um Ihre Webinhalte im [Surface Duo-Emulator zu debuggen.][DualScreenAndroidUseEmulator]</span><span class="sxs-lookup"><span data-stu-id="ffd55-136">You are now able to use the Microsoft Edge DevTools to debug your web content on the [Surface Duo emulator][DualScreenAndroidUseEmulator].</span></span>  

:::image type="complex" source="../media/remote-debugging-surface-duo-devtools.msft.png" alt-text="Verwenden der Microsoft Edge DevTools zum Debuggen von Bing in der Microsoft Edge-App auf dem Surface Duo-Emulator" lightbox="../media/remote-debugging-surface-duo-devtools.msft.png":::
   <span data-ttu-id="ffd55-138">Verwenden der Microsoft Edge DevTools zum Debuggen von Bing in der Microsoft Edge-App auf dem Surface Duo-Emulator</span><span class="sxs-lookup"><span data-stu-id="ffd55-138">Using the Microsoft Edge DevTools to debug Bing in the Microsoft Edge app on the Surface Duo emulator</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="ffd55-139">Wenn Sie die [Microsoft Edge-App][GooglePlayStoreAppsComMicrosoftEmmx] auf beiden Bildschirmen im Emulator überspannen, spiegelt der Screencast die neue Größe der App wider, aber nicht das Scharnier.</span><span class="sxs-lookup"><span data-stu-id="ffd55-139">If you span the [Microsoft Edge app][GooglePlayStoreAppsComMicrosoftEmmx] across both screens in the emulator, the screencast will reflect the new size of the app but not the hinge.</span></span>  <span data-ttu-id="ffd55-140">Um zu verstehen, wie sich das Scharnier auf das Layout Ihrer Webinhalte aus wirkt, verwenden Sie den [Surface Duo-Emulator][DualScreenAndroidUseEmulator] anstelle des Screencasts.</span><span class="sxs-lookup"><span data-stu-id="ffd55-140">To understand how the hinge impacts the layout of your web content, use the [Surface Duo emulator][DualScreenAndroidUseEmulator] instead of the screencast.</span></span>  

## <a name="additional-resources"></a><span data-ttu-id="ffd55-141">Weitere Ressourcen</span><span class="sxs-lookup"><span data-stu-id="ffd55-141">Additional Resources</span></span>  

<span data-ttu-id="ffd55-142">Das Web ist eine großartige Plattform für die neue Klasse von zusammenklappbaren Und Dual-Screen-Geräten, da Sie Ihre HTML, CSS und JavaScript einmal schreiben können und es auf einzelnen Bildschirmen, dualen Bildschirmen und faltbaren Geräten großartig aussehen lässt.</span><span class="sxs-lookup"><span data-stu-id="ffd55-142">The web is a great platform for the new class of foldable and dual-screen devices because you may write your HTML, CSS, and JavaScript once and have it look great across single-screen, dual-screen, and foldable devices.</span></span>  <span data-ttu-id="ffd55-143">Weitere Informationen finden Sie in den folgenden zusätzlichen Ressourcen, um mit dem Erstellen von Webinhalten für diese neuen Geräte zu beginnen.</span><span class="sxs-lookup"><span data-stu-id="ffd55-143">For more information, navigate to the following additional resources to get started building web content for these new devices.</span></span>  

*   [<span data-ttu-id="ffd55-144">Dokumentation zum Erstellen von Apps auf Dual-Screen-Geräten</span><span class="sxs-lookup"><span data-stu-id="ffd55-144">Documentation for creating apps on dual-screen devices</span></span>][DualScreenIndex]  
*   [<span data-ttu-id="ffd55-145">Der Microsoft Edge-Webplattform-Erklärer für neue APIs zum Erstellen von Weberfahrungen auf zusammenklappbaren Und Dual-Screen-Geräten</span><span class="sxs-lookup"><span data-stu-id="ffd55-145">The Microsoft Edge web platform explainer for new APIs to build web experiences on foldable and dual-screen devices</span></span>][GithubMicrosoftedgeMsedgeexplainersFoldablesExplainer]  
*   [<span data-ttu-id="ffd55-146">Aufzeichnung der Microsoft 365 Developer Day-Sitzung: Erstellen von Dualscreen-Erfahrungen für Websites und Web-Apps</span><span class="sxs-lookup"><span data-stu-id="ffd55-146">Recording of Microsoft 365 Developer Day session: How to build dual-screen experiences for websites and web apps</span></span>][YoutubeDxrzwsqxpvc]  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="ffd55-147">Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen</span><span class="sxs-lookup"><span data-stu-id="ffd55-147">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsIndex]: ../index.md "Microsoft Edge (Chromium) -Entwicklertools | Microsoft Docs"  
[ProgressiveWebAppsIndex]: ../../progressive-web-apps-chromium/index.md "Progressive Web Apps unter Windows | Microsoft Docs"  
[DevtoolsRemoteDebuggingMain]: ./index.md "Erste Schritte mit remote debuggen von Android-Geräten | Microsoft Docs"  
[DevtoolsRemoteDebuggingIndexTroubleshootingDevtoolsIsNotDetectingAndroidDevice]: ./index.md#troubleshooting-devtools-is-not-detecting-the-android-device "Problembehandlung: DevTools erkennt das Android-Gerät nicht – Erste Schritte mit dem Remotedebugieren von Android-Geräten | Microsoft Docs"  

[DualScreenIndex]: /dual-screen/index "Erstellen von Apps für Zwei-Bildschirm-| Microsoft Docs"  
[DualScreenAndroidUseEmulator]: /dual-screen/android/use-emulator "Verwenden des Surface DUo-Emulators | Microsoft Docs"  
[DualScreenAndroidGetDuoSdk]: /dual-screen/android/get-duo-sdk "Get the Surface Duo SDK | Microsoft Docs"  

[MicrosoftEdge]: https://www.microsoft.com/edge "Einführung in das neue Microsoft Edge"  
[MicrosoftSurfaceDevicesSurfaceDuo]: https://www.microsoft.com/surface/devices/surface-duo "Das neue Surface Duo-| Microsoft Surface"  
[MicrosoftDownload100847]: https://www.microsoft.com/download/details.aspx?id=100847 "Surface Duo SDK Preview Release | Microsoft Download Center"  

[GooglePlayStoreAppsComMicrosoftEmmx]: https://play.google.com/store/apps/details?id=com.microsoft.emmx "Microsoft Edge: Webbrowser | GooglePlay"  

[GithubMicrosoftedgeMsedgeexplainersFoldablesExplainer]: https://github.com/MicrosoftEdge/MSEdgeExplainers/blob/master/Foldables/explainer.md "Webplattformgrundtypen für aufklappbare Geräte – MicrosoftEdge/MSEdgeExplainers | GitHub"  

[YoutubeDxrzwsqxpvc]: https://youtu.be/DXrZWsqXPVc "Erstellen von dualen Bildschirmen für die Website- und Web-Apps-| YouTube"  
