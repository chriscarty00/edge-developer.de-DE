---
description: Erste Schritte mit Remote Debuggen Surface Duo-Emulatoren.
title: Erste Schritte mit Remote Debuggen Surface Duo-Emulatoren
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/17/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Web-Entwicklung, F12-Tools, devtools, Remote Debugging, Android, Surface Duo
ms.openlocfilehash: f44c85c468de3bdd7727695e3f33269584966231
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11230641"
---
# <span data-ttu-id="16d55-104">Erste Schritte mit Remote Debuggen Surface Duo-Emulatoren</span><span class="sxs-lookup"><span data-stu-id="16d55-104">Get Started with Remote Debugging Surface Duo emulators</span></span>  

<span data-ttu-id="16d55-105">In diesem Artikel durchlaufen Sie den Vorgang des Remotedebuggens von Webinhalten in der [Microsoft Edge-App][GooglePlayStoreAppsComMicrosoftEmmx] auf einem [Surface Duo][MicrosoftSurfaceDevicesSurfaceDuo] -Emulator von einer Desktop Instanz von [Microsoft Edge][MicrosoftEdge].</span><span class="sxs-lookup"><span data-stu-id="16d55-105">In this article, you walk through the process of remotely debugging your web content in the [Microsoft Edge app][GooglePlayStoreAppsComMicrosoftEmmx] on a [Surface Duo][MicrosoftSurfaceDevicesSurfaceDuo] emulator from a desktop instance of [Microsoft Edge][MicrosoftEdge].</span></span>  <span data-ttu-id="16d55-106">Informationen zum Debuggen auf einem Surface Duo-Gerät finden Sie im Leitfaden zum [Remotedebuggen von Android-Geräten][DevtoolsRemoteDebuggingMain].</span><span class="sxs-lookup"><span data-stu-id="16d55-106">For information on debugging on a Surface Duo device, follow our guide for [remote debugging Android devices][DevtoolsRemoteDebuggingMain].</span></span>  

## <span data-ttu-id="16d55-107">Bevor Sie beginnen</span><span class="sxs-lookup"><span data-stu-id="16d55-107">Before you Begin</span></span>

<span data-ttu-id="16d55-108">Installieren Sie das [Surface Duo SDK][MicrosoftDownload100847] , bevor Sie den [Surface Duo-Emulator][DualScreenAndroidUseEmulator]ausführen.</span><span class="sxs-lookup"><span data-stu-id="16d55-108">Install the [Surface Duo SDK][MicrosoftDownload100847] before running the [Surface Duo emulator][DualScreenAndroidUseEmulator].</span></span>  <span data-ttu-id="16d55-109">Weitere Informationen finden Sie unter [Abrufen des Surface Duo SDK][DualScreenAndroidGetDuoSdk].</span><span class="sxs-lookup"><span data-stu-id="16d55-109">For more information, see [Get the Surface Duo SDK][DualScreenAndroidGetDuoSdk].</span></span>  

## <span data-ttu-id="16d55-110">Schritt 1: Navigieren zu Edge://Inspect</span><span class="sxs-lookup"><span data-stu-id="16d55-110">Step 1: Navigate to edge://inspect</span></span>  

<span data-ttu-id="16d55-111">Öffnen Sie eine Desktop Instanz von [Microsoft Edge][MicrosoftEdge], und navigieren Sie zu `edge://inspect` .</span><span class="sxs-lookup"><span data-stu-id="16d55-111">Open a desktop instance of [Microsoft Edge][MicrosoftEdge], and navigate to `edge://inspect`.</span></span>  

:::image type="complex" source="../media/remote-debugging-surface-duo-inspect-page.msft.png" alt-text="Die Seite "Edge://Inspect" in Microsoft Edge auf dem Desktop" lightbox="../media/remote-debugging-surface-duo-inspect-page.msft.png":::
   <span data-ttu-id="16d55-113">Die `edge://inspect` Seite in Microsoft Edge auf dem Desktop</span><span class="sxs-lookup"><span data-stu-id="16d55-113">The `edge://inspect` page in Microsoft Edge on the desktop</span></span>  
:::image-end:::

> [!NOTE]
> <span data-ttu-id="16d55-114">Wenn die `edge://inspect` Seite den [Surface Duo-Emulator][DualScreenAndroidUseEmulator]nicht erkennt, starten Sie den Emulator neu.</span><span class="sxs-lookup"><span data-stu-id="16d55-114">If the `edge://inspect` page does not recognize the [Surface Duo emulator][DualScreenAndroidUseEmulator], restart the emulator.</span></span>  

## <span data-ttu-id="16d55-115">Schritt 2: Starten des Surface Duo-Emulators</span><span class="sxs-lookup"><span data-stu-id="16d55-115">Step 2: Launch the Surface Duo emulator</span></span>  

<span data-ttu-id="16d55-116">Starten Sie den [Surface Duo-Emulator][DualScreenAndroidUseEmulator].</span><span class="sxs-lookup"><span data-stu-id="16d55-116">Launch the [Surface Duo emulator][DualScreenAndroidUseEmulator].</span></span>  <span data-ttu-id="16d55-117">Beachten Sie, dass der Emulator zwei verschiedene Bildschirme anzeigt, die auf dem Emulator ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="16d55-117">Notice that the emulator displays 2 different screens running on the emulator.</span></span>  

:::image type="complex" source="../media/remote-debugging-surface-duo-emulator.msft.png" alt-text="Der Surface Duo-Emulator" lightbox="../media/remote-debugging-surface-duo-emulator.msft.png":::
   <span data-ttu-id="16d55-119">Der Surface Duo-Emulator</span><span class="sxs-lookup"><span data-stu-id="16d55-119">The Surface Duo emulator</span></span>  
:::image-end:::  

## <span data-ttu-id="16d55-120">Schritt 3: Laden von Webinhalten in Microsoft Edge auf dem Surface Duo-Emulator</span><span class="sxs-lookup"><span data-stu-id="16d55-120">Step 3: Load your web content in Microsoft Edge on the Surface Duo emulator</span></span>  

<span data-ttu-id="16d55-121">Wischen Sie auf einem der beiden Bildschirme auf der Favoritenleiste des [Surface Duo-Emulators][DualScreenAndroidUseEmulator] nach oben, um die APP-Schublade anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="16d55-121">On either screen, swipe up on the Favorites Tray of the [Surface Duo emulator][DualScreenAndroidUseEmulator] to display the Apps Drawer.</span></span>  <span data-ttu-id="16d55-122">Wählen Sie **Edge** aus, um die [Microsoft Edge-App][GooglePlayStoreAppsComMicrosoftEmmx]zu starten.</span><span class="sxs-lookup"><span data-stu-id="16d55-122">Choose **Edge** to launch the [Microsoft Edge app][GooglePlayStoreAppsComMicrosoftEmmx].</span></span>  

:::image type="complex" source="../media/remote-debugging-surface-duo-emulator-edge.msft.png" alt-text="Die Microsoft Edge-App auf dem Surface Duo-Emulator" lightbox="../media/remote-debugging-surface-duo-emulator-edge.msft.png":::
   <span data-ttu-id="16d55-124">Die Microsoft Edge-App auf dem Surface Duo-Emulator</span><span class="sxs-lookup"><span data-stu-id="16d55-124">The Microsoft Edge app on the Surface Duo emulator</span></span>  
:::image-end:::  

<span data-ttu-id="16d55-125">Navigieren Sie in der [Microsoft Edge-App][GooglePlayStoreAppsComMicrosoftEmmx]zu der Website oder App, die Sie debuggen möchten.</span><span class="sxs-lookup"><span data-stu-id="16d55-125">Navigate to the website or app that you want to debug in the [Microsoft Edge app][GooglePlayStoreAppsComMicrosoftEmmx].</span></span>  

## <span data-ttu-id="16d55-126">Schritt 4: Debuggen von Webinhalten aus dem Surface Duo-Emulator</span><span class="sxs-lookup"><span data-stu-id="16d55-126">Step 4: Debug your web content from the Surface Duo emulator</span></span>  

<span data-ttu-id="16d55-127">Wechseln Sie zurück zur Desktop Instanz von [Microsoft Edge][MicrosoftEdge].</span><span class="sxs-lookup"><span data-stu-id="16d55-127">Switch back to the desktop instance of [Microsoft Edge][MicrosoftEdge].</span></span>  <span data-ttu-id="16d55-128">`edge://inspect`Auf der Seite wird nun der **SurfaceDuoEmulator** mit einer Liste der geöffneten Registerkarten oder [PWAs][ProgressiveWebAppsIndex] angezeigt, die auf dem [Surface Duo-Emulator][DualScreenAndroidUseEmulator]ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="16d55-128">The `edge://inspect` page now shows the **SurfaceDuoEmulator** with a list of the open tabs or [PWAs][ProgressiveWebAppsIndex] that are running on the [Surface Duo emulator][DualScreenAndroidUseEmulator].</span></span>  

:::image type="complex" source="../media/remote-debugging-surface-duo-inspect-page-with-targets.msft.png" alt-text="Auf der Seite "Edge://Inspect" wird eine Liste der geöffneten Registerkarten in der Microsoft Edge-App angezeigt, die auf dem Emulator ausgeführt wird." lightbox="../media/remote-debugging-surface-duo-inspect-page-with-targets.msft.png":::
   <span data-ttu-id="16d55-130">`edge://inspect`Auf der Seite wird eine Liste der geöffneten Registerkarten in der Microsoft Edge-App angezeigt, die auf dem Emulator ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="16d55-130">The `edge://inspect` page displays a list of the open tabs in the Microsoft Edge app running on the emulator</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="16d55-131">Wenn **SurfaceDuoEmulator** auf der Seite nicht angezeigt `edge://inspect` wird, versuchen Sie, die Registerkarten in der [Microsoft Edge-App][GooglePlayStoreAppsComMicrosoftEmmx] auf dem [Surface Duo-Emulator][DualScreenAndroidUseEmulator]zu öffnen oder zu schließen.</span><span class="sxs-lookup"><span data-stu-id="16d55-131">If you do not see **SurfaceDuoEmulator** on the `edge://inspect` page, try opening or closing tabs in the [Microsoft Edge app][GooglePlayStoreAppsComMicrosoftEmmx] on the [Surface Duo Emulator][DualScreenAndroidUseEmulator].</span></span>  <span data-ttu-id="16d55-132">Weitere Schritte zur Problembehandlung finden Sie im [Abschnitt Problembehandlung für Android-Geräte][DevtoolsRemoteDebuggingIndexTroubleshootingDevtoolsIsNotDetectingAndroidDevice].</span><span class="sxs-lookup"><span data-stu-id="16d55-132">For additional troubleshooting steps, see the [troubleshooting section for Android devices][DevtoolsRemoteDebuggingIndexTroubleshootingDevtoolsIsNotDetectingAndroidDevice].</span></span>  

<span data-ttu-id="16d55-133">Wählen Sie in der Liste der geöffneten Registerkarten, die im Emulator ausgeführt werden, auf der Registerkarte über **prüfen** aus, auf der die zu debuggenden Webinhalte enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="16d55-133">From the list of open tabs running on the emulator, choose **inspect** on the tab that has the web content to be debugged.</span></span>  <span data-ttu-id="16d55-134">Die [Microsoft Edge-devtools][DevtoolsIndex] wird in einem neuen Fenster geöffnet.</span><span class="sxs-lookup"><span data-stu-id="16d55-134">The [Microsoft Edge DevTools][DevtoolsIndex] will open in a new window.</span></span>  <span data-ttu-id="16d55-135">Wählen Sie **Screencast umschalten** \ ( ![ Screencast wechseln ][ImageToggleScreencastIcon] \) aus, um die Webinhalte aus Ihrem [Surface Duo-Emulator][DualScreenAndroidUseEmulator] im devtools-Fenster anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="16d55-135">Choose **Toggle Screencast** \(![Toggle Screencast][ImageToggleScreencastIcon]\) to view the web content from your [Surface Duo emulator][DualScreenAndroidUseEmulator] in the DevTools window.</span></span>  <span data-ttu-id="16d55-136">Sie können jetzt die Microsoft Edge-devtools verwenden, um Ihre Webinhalte auf dem [Surface Duo-Emulator][DualScreenAndroidUseEmulator]zu debuggen.</span><span class="sxs-lookup"><span data-stu-id="16d55-136">You are now able to use the Microsoft Edge DevTools to debug your web content on the [Surface Duo emulator][DualScreenAndroidUseEmulator].</span></span>  

:::image type="complex" source="../media/remote-debugging-surface-duo-devtools.msft.png" alt-text="Verwenden des Microsoft Edge-devtools zum Debuggen von Bing in der Microsoft Edge-App auf dem Surface Duo-Emulator" lightbox="../media/remote-debugging-surface-duo-devtools.msft.png":::
   <span data-ttu-id="16d55-138">Verwenden des Microsoft Edge-devtools zum Debuggen von Bing in der Microsoft Edge-App auf dem Surface Duo-Emulator</span><span class="sxs-lookup"><span data-stu-id="16d55-138">Using the Microsoft Edge DevTools to debug Bing in the Microsoft Edge app on the Surface Duo emulator</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="16d55-139">Wenn Sie die [Microsoft Edge-App][GooglePlayStoreAppsComMicrosoftEmmx] über beide Bildschirme im Emulator überspannen, gibt der Screencast die neue Größe der APP, aber nicht das Scharnier wieder.</span><span class="sxs-lookup"><span data-stu-id="16d55-139">If you span the [Microsoft Edge app][GooglePlayStoreAppsComMicrosoftEmmx] across both screens in the emulator, the screencast will reflect the new size of the app but not the hinge.</span></span>  <span data-ttu-id="16d55-140">Wenn Sie wissen möchten, wie sich das Scharnier auf das Layout Ihres Webinhalts auswirkt, verwenden Sie den [Surface Duo-Emulator][DualScreenAndroidUseEmulator] anstelle des Screencasts.</span><span class="sxs-lookup"><span data-stu-id="16d55-140">To understand how the hinge impacts the layout of your web content, use the [Surface Duo emulator][DualScreenAndroidUseEmulator] instead of the screencast.</span></span>  

## <span data-ttu-id="16d55-141">Weitere Ressourcen</span><span class="sxs-lookup"><span data-stu-id="16d55-141">Additional Resources</span></span>  

<span data-ttu-id="16d55-142">Das Web ist eine großartige Plattform für die neue Klasse von faltbaren und Dual-Screen-Geräten, da Sie Ihre HTML-, CSS-und JavaScript-Datei einmal schreiben können und Sie auf Einzelbildschirm-, Dual-Screen-und faltbaren Geräten hervorragend aussehen.</span><span class="sxs-lookup"><span data-stu-id="16d55-142">The web is a great platform for the new class of foldable and dual-screen devices because you can write your HTML, CSS, and JavaScript once and have it look great across single-screen, dual-screen, and foldable devices.</span></span>  <span data-ttu-id="16d55-143">Weitere Informationen finden Sie in diesen zusätzlichen Ressourcen, damit Sie mit dem Erstellen von Webinhalten für diese neuen Geräte beginnen können.</span><span class="sxs-lookup"><span data-stu-id="16d55-143">For more information, see these additional resources to get started building web content for these new devices.</span></span>  

*   [<span data-ttu-id="16d55-144">Dokumentation zum Erstellen von apps auf Dual-Screen-Geräten</span><span class="sxs-lookup"><span data-stu-id="16d55-144">Documentation for creating apps on dual-screen devices</span></span>][DualScreenIndex]  
*   [<span data-ttu-id="16d55-145">Die Microsoft Edge Web Platform-Erläuterung für neue APIs zum Erstellen von Weberfahrungen auf faltbaren und Dual-Screen-Geräten</span><span class="sxs-lookup"><span data-stu-id="16d55-145">The Microsoft Edge web platform explainer for new APIs to build web experiences on foldable and dual-screen devices</span></span>][GithubMicrosoftedgeMsedgeexplainersFoldablesExplainer]  
*   [<span data-ttu-id="16d55-146">Aufzeichnung der Microsoft 365-Entwicklertag Sitzung: Erstellen von Dual-Screen-Erlebnissen für Websites und Web-Apps</span><span class="sxs-lookup"><span data-stu-id="16d55-146">Recording of Microsoft 365 Developer Day session: How to build dual-screen experiences for websites and web apps</span></span>][YoutubeDxrzwsqxpvc]  

<!-- image links -->  

[ImageToggleScreencastIcon]: images/toggle-screencast-icon.msft.png  

<!-- links -->  

[DevtoolsIndex]: ../index.md "Microsoft Edge (Chrom)-Entwickler Tools | Microsoft docs"  
[ProgressiveWebAppsIndex]: ../../progressive-web-apps-chromium/index.md "Progressive Web-Apps unter Windows | Microsoft docs"  
[DevtoolsRemoteDebuggingMain]: ./index.md "Erste Schritte mit dem Remotedebuggen von Android-Geräten | Microsoft docs"  
[DevtoolsRemoteDebuggingIndexTroubleshootingDevtoolsIsNotDetectingAndroidDevice]: ./index.md#troubleshooting-devtools-is-not-detecting-the-android-device "Problembehandlung: devtools erkennt das Android-Gerät nicht – erste Schritte mit dem Remotedebuggen von Android-Geräten | Microsoft docs"  

[DualScreenIndex]: /dual-screen/index "Erstellen von Apps für Dual-Screen-Geräte | Microsoft docs"  
[DualScreenAndroidUseEmulator]: /dual-screen/android/use-emulator "Verwenden des Surface DUo-Emulators | Microsoft docs"  
[DualScreenAndroidGetDuoSdk]: /dual-screen/android/get-duo-sdk "Besorgen Sie sich das Surface Duo SDK | Microsoft docs"  

[MicrosoftEdge]: https://www.microsoft.com/edge "Einführung in das neue Microsoft Edge"  
[MicrosoftSurfaceDevicesSurfaceDuo]: https://www.microsoft.com/surface/devices/surface-duo "Das neue Surface Duo | Microsoft Surface"  
[MicrosoftDownload100847]: https://www.microsoft.com/download/details.aspx?id=100847 "Surface Duo SDK Preview-Version herunterladen | Microsoft Download Center"  

[GooglePlayStoreAppsComMicrosoftEmmx]: https://play.google.com/store/apps/details?id=com.microsoft.emmx "Microsoft Edge: Webbrowser | GooglePlay"  

[GithubMicrosoftedgeMsedgeexplainersFoldablesExplainer]: https://github.com/MicrosoftEdge/MSEdgeExplainers/blob/master/Foldables/explainer.md "Webplattform-Grundtypen für erleuchtete Erfahrungen auf faltbaren Geräten-MicrosoftEdge/MSEdgeExplainers | GitHub"  

[YoutubeDxrzwsqxpvc]: https://youtu.be/DXrZWsqXPVc "Erstellen von Dual-Screen-Erlebnissen für die Website und Web-Apps | YouTube"  
