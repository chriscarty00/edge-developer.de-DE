---
title: Erste Schritte mit Remote Debuggen Surface Duo-Emulatoren
author: zoherghadyali
ms.author: zoghadya
ms.date: 04/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Web-Entwicklung, F12-Tools, devtools, Remote Debugging, Android, Surface Duo
ms.openlocfilehash: af6fa6433b0bc6bba0599e6e9a805235504caadd
ms.sourcegitcommit: 966bfc60040acc794b6ee20eb2084bc8264a4852
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/05/2020
ms.locfileid: "10621502"
---
# <span data-ttu-id="7114b-103">Erste Schritte mit Remote Debuggen Surface Duo-Emulatoren</span><span class="sxs-lookup"><span data-stu-id="7114b-103">Get Started with Remote Debugging Surface Duo emulators</span></span>

<span data-ttu-id="7114b-104">In diesem Artikel durchlaufen Sie den Vorgang des Remotedebuggens von Webinhalten in der [Microsoft Edge-App][AndroidEdge] auf einem [Surface Duo][SurfaceDuo] -Emulator von einer Desktop Instanz von [Microsoft Edge][DesktopEdge].</span><span class="sxs-lookup"><span data-stu-id="7114b-104">In this article, you walk through the process of remotely debugging your web content in the [Microsoft Edge app][AndroidEdge] on a [Surface Duo][SurfaceDuo] emulator from a desktop instance of [Microsoft Edge][DesktopEdge].</span></span> <span data-ttu-id="7114b-105">Informationen zum Debuggen auf einem Surface Duo-Gerät finden Sie im Leitfaden zum [Remotedebuggen von Android-Geräten][RemoteDebuggingAndroid].</span><span class="sxs-lookup"><span data-stu-id="7114b-105">For information on debugging on a Surface Duo device, follow our guide for [remote debugging Android devices][RemoteDebuggingAndroid].</span></span>

## <span data-ttu-id="7114b-106">Bevor Sie beginnen</span><span class="sxs-lookup"><span data-stu-id="7114b-106">Before you Begin</span></span>

<span data-ttu-id="7114b-107">Installieren Sie das [Surface Duo SDK][DuoSdk] , bevor Sie den [Surface Duo-Emulator][DuoEmulator]ausführen.</span><span class="sxs-lookup"><span data-stu-id="7114b-107">Install the [Surface Duo SDK][DuoSdk] before running the [Surface Duo emulator][DuoEmulator].</span></span> <span data-ttu-id="7114b-108">Weitere Informationen finden Sie unter [Abrufen des Surface Duo SDK][DuoSdkdocs].</span><span class="sxs-lookup"><span data-stu-id="7114b-108">For more information, see [Get the Surface Duo SDK][DuoSdkdocs].</span></span>

## <span data-ttu-id="7114b-109">Schritt 1: Navigieren zu Edge://Inspect</span><span class="sxs-lookup"><span data-stu-id="7114b-109">Step 1: Navigate to edge://inspect</span></span>

<span data-ttu-id="7114b-110">Öffnen Sie eine Desktop Instanz von [Microsoft Edge][DesktopEdge], und navigieren Sie zu `edge://inspect` .</span><span class="sxs-lookup"><span data-stu-id="7114b-110">Open a desktop instance of [Microsoft Edge][DesktopEdge], and navigate to `edge://inspect`.</span></span>

> ##### <span data-ttu-id="7114b-111">Abbildung1</span><span class="sxs-lookup"><span data-stu-id="7114b-111">Figure 1</span></span>  
> <span data-ttu-id="7114b-112">Die `edge://inspect` Seite in Microsoft Edge auf dem Desktop auf der ![ Seite "Edge://Inspect" in Microsoft Edge auf dem Desktop][ImageEdgeInspect]</span><span class="sxs-lookup"><span data-stu-id="7114b-112">The `edge://inspect` page in Microsoft Edge on the desktop ![The edge://inspect page in Microsoft Edge on the desktop][ImageEdgeInspect]</span></span>

> [!NOTE]
> <span data-ttu-id="7114b-113">Wenn die `edge://inspect` Seite den [Surface Duo-Emulator][DuoEmulator]nicht erkennt, starten Sie den Emulator neu.</span><span class="sxs-lookup"><span data-stu-id="7114b-113">If the `edge://inspect` page does not recognize the [Surface Duo emulator][DuoEmulator], restart the emulator.</span></span>

## <span data-ttu-id="7114b-114">Schritt 2: Starten des Surface Duo-Emulators</span><span class="sxs-lookup"><span data-stu-id="7114b-114">Step 2: Launch the Surface Duo emulator</span></span>

<span data-ttu-id="7114b-115">Starten Sie den [Surface Duo-Emulator][DuoEmulator].</span><span class="sxs-lookup"><span data-stu-id="7114b-115">Launch the [Surface Duo emulator][DuoEmulator].</span></span> <span data-ttu-id="7114b-116">Beachten Sie, dass der Emulator zwei verschiedene Bildschirme anzeigt, die auf dem Emulator ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="7114b-116">Notice that the emulator displays 2 different screens running on the emulator.</span></span>

> ##### <span data-ttu-id="7114b-117">Abbildung2</span><span class="sxs-lookup"><span data-stu-id="7114b-117">Figure 2</span></span>
> <span data-ttu-id="7114b-118">Der Surface Duo-Emulator ![ der Surface Duo-Emulator][ImageDuoEmulator]</span><span class="sxs-lookup"><span data-stu-id="7114b-118">The Surface Duo emulator ![The Surface Duo emulator][ImageDuoEmulator]</span></span>  

## <span data-ttu-id="7114b-119">Schritt 3: Laden von Webinhalten in Microsoft Edge auf dem Surface Duo-Emulator</span><span class="sxs-lookup"><span data-stu-id="7114b-119">Step 3: Load your web content in Microsoft Edge on the Surface Duo emulator</span></span>

<span data-ttu-id="7114b-120">Wischen Sie auf einem der beiden Bildschirme auf der Favoritenleiste des [Surface Duo-Emulators][DuoEmulator] nach oben, um die APP-Schublade anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="7114b-120">On either screen, swipe up on the Favorites Tray of the [Surface Duo emulator][DuoEmulator] to display the Apps Drawer.</span></span> <span data-ttu-id="7114b-121">Wählen Sie **Edge** aus, um die [Microsoft Edge-App][AndroidEdge]zu starten.</span><span class="sxs-lookup"><span data-stu-id="7114b-121">Choose **Edge** to launch the [Microsoft Edge app][AndroidEdge].</span></span>

> ##### <span data-ttu-id="7114b-122">Abbildung 3</span><span class="sxs-lookup"><span data-stu-id="7114b-122">Figure 3</span></span>
> <span data-ttu-id="7114b-123">Die Microsoft Edge-App auf dem Surface Duo-Emulator ![ die Microsoft Edge-App auf dem Surface Duo-Emulator][ImageDuoEmulatorEdge]</span><span class="sxs-lookup"><span data-stu-id="7114b-123">The Microsoft Edge app on the Surface Duo emulator ![The Microsoft Edge app on the Surface Duo emulator][ImageDuoEmulatorEdge]</span></span>  

<span data-ttu-id="7114b-124">Navigieren Sie in der [Microsoft Edge-App][AndroidEdge]zu der Website oder App, die Sie debuggen möchten.</span><span class="sxs-lookup"><span data-stu-id="7114b-124">Navigate to the website or app that you want to debug in the [Microsoft Edge app][AndroidEdge].</span></span>

## <span data-ttu-id="7114b-125">Schritt 4: Debuggen von Webinhalten aus dem Surface Duo-Emulator</span><span class="sxs-lookup"><span data-stu-id="7114b-125">Step 4: Debug your web content from the Surface Duo emulator</span></span> 

<span data-ttu-id="7114b-126">Wechseln Sie zurück zur Desktop Instanz von [Microsoft Edge][DesktopEdge].</span><span class="sxs-lookup"><span data-stu-id="7114b-126">Switch back to the desktop instance of [Microsoft Edge][DesktopEdge].</span></span> <span data-ttu-id="7114b-127">`edge://inspect`Auf der Seite wird nun der **SurfaceDuoEmulator** mit einer Liste der geöffneten Registerkarten oder [PWAs][PwaDocs] angezeigt, die auf dem [Surface Duo-Emulator][DuoEmulator]ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="7114b-127">The `edge://inspect` page now shows the **SurfaceDuoEmulator** with a list of the open tabs or [PWAs][PwaDocs] that are running on the [Surface Duo emulator][DuoEmulator].</span></span>

> ##### <span data-ttu-id="7114b-128">Abbildung4</span><span class="sxs-lookup"><span data-stu-id="7114b-128">Figure 4</span></span>
> <span data-ttu-id="7114b-129">Auf der `edge://inspect` Seite wird eine Liste der geöffneten Registerkarten in der Microsoft Edge-App angezeigt, die auf dem Emulator ausgeführt wird. auf der Seite "Edge://Inspect" wird ![ eine Liste der geöffneten Registerkarten in der auf dem Emulator ausgeführten Microsoft Edge-App angezeigt.][ImageEdgeInspectTargets]</span><span class="sxs-lookup"><span data-stu-id="7114b-129">The `edge://inspect` page displays a list of the open tabs in the Microsoft Edge app running on the emulator ![The edge://inspect page displays a list of the open tabs in the Microsoft Edge app running on the emulator][ImageEdgeInspectTargets]</span></span>  

> [!NOTE]
> <span data-ttu-id="7114b-130">Wenn **SurfaceDuoEmulator** auf der Seite nicht angezeigt `edge://inspect` wird, versuchen Sie, die Registerkarten in der [Microsoft Edge-App][AndroidEdge] auf dem [Surface Duo-Emulator][DuoEmulator]zu öffnen oder zu schließen.</span><span class="sxs-lookup"><span data-stu-id="7114b-130">If you do not see **SurfaceDuoEmulator** on the `edge://inspect` page, try opening or closing tabs in the [Microsoft Edge app][AndroidEdge] on the [Surface Duo Emulator][DuoEmulator].</span></span> <span data-ttu-id="7114b-131">Weitere Schritte zur Problembehandlung finden Sie im [Abschnitt Problembehandlung für Android-Geräte][TroubleshootingAndroid].</span><span class="sxs-lookup"><span data-stu-id="7114b-131">For additional troubleshooting steps, see the [troubleshooting section for Android devices][TroubleshootingAndroid].</span></span>

<span data-ttu-id="7114b-132">Wählen Sie in der Liste der geöffneten Registerkarten, die im Emulator ausgeführt werden, auf der Registerkarte über **prüfen** aus, auf der die zu debuggenden Webinhalte enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="7114b-132">From the list of open tabs running on the emulator, choose **inspect** on the tab that has the web content to be debugged.</span></span> <span data-ttu-id="7114b-133">Die [Microsoft Edge-devtools][DevToolsDocs] wird in einem neuen Fenster geöffnet.</span><span class="sxs-lookup"><span data-stu-id="7114b-133">The [Microsoft Edge DevTools][DevToolsDocs] will open in a new window.</span></span> <span data-ttu-id="7114b-134">Wählen Sie **Screencast** umschalten ![ Screencast ][ImageToggleScreencastIcon] aus, um die Webinhalte aus Ihrem [Surface Duo-Emulator][DuoEmulator] im devtools-Fenster anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="7114b-134">Choose **Toggle Screencast** ![Toggle Screencast][ImageToggleScreencastIcon] to view the web content from your [Surface Duo emulator][DuoEmulator] in the DevTools window.</span></span> <span data-ttu-id="7114b-135">Sie können jetzt die Microsoft Edge-devtools verwenden, um Ihre Webinhalte auf dem [Surface Duo-Emulator][DuoEmulator]zu debuggen.</span><span class="sxs-lookup"><span data-stu-id="7114b-135">You are now able to use the Microsoft Edge DevTools to debug your web content on the [Surface Duo emulator][DuoEmulator].</span></span>

> ##### <span data-ttu-id="7114b-136">Abbildung5</span><span class="sxs-lookup"><span data-stu-id="7114b-136">Figure 5</span></span>
> <span data-ttu-id="7114b-137">Verwenden des Microsoft Edge-devtools zum Debuggen von Bing in der Microsoft Edge-App auf dem Surface Duo-Emulator ![ mithilfe der Microsoft Edge-devtools zum Debuggen von Bing in der Microsoft Edge-App auf dem Surface Duo-Emulator][ImageDevTools]</span><span class="sxs-lookup"><span data-stu-id="7114b-137">Using the Microsoft Edge DevTools to debug Bing in the Microsoft Edge app on the Surface Duo emulator ![Using the Microsoft Edge DevTools to debug Bing in the Microsoft Edge app on the Surface Duo emulator][ImageDevTools]</span></span>  

> [!NOTE]
> <span data-ttu-id="7114b-138">Wenn Sie die [Microsoft Edge-App][AndroidEdge] über beide Bildschirme im Emulator überspannen, gibt der Screencast die neue Größe der APP, aber nicht das Scharnier wieder.</span><span class="sxs-lookup"><span data-stu-id="7114b-138">If you span the [Microsoft Edge app][AndroidEdge] across both screens in the emulator, the screencast will reflect the new size of the app but not the hinge.</span></span> <span data-ttu-id="7114b-139">Wenn Sie wissen möchten, wie sich das Scharnier auf das Layout Ihres Webinhalts auswirkt, verwenden Sie den [Surface Duo-Emulator][DuoEmulator] anstelle des Screencasts.</span><span class="sxs-lookup"><span data-stu-id="7114b-139">To understand how the hinge impacts the layout of your web content, use the [Surface Duo emulator][DuoEmulator] instead of the screencast.</span></span>

## <span data-ttu-id="7114b-140">Weitere Ressourcen</span><span class="sxs-lookup"><span data-stu-id="7114b-140">Additional Resources</span></span>

<span data-ttu-id="7114b-141">Das Web ist eine großartige Plattform für die neue Klasse von faltbaren und Dual-Screen-Geräten, da Sie Ihre HTML-, CSS-und JavaScript-Datei einmal schreiben können und Sie auf Einzelbildschirm-, Dual-Screen-und faltbaren Geräten hervorragend aussehen.</span><span class="sxs-lookup"><span data-stu-id="7114b-141">The web is a great platform for the new class of foldable and dual-screen devices because you can write your HTML, CSS, and JavaScript once and have it look great across single-screen, dual-screen, and foldable devices.</span></span> <span data-ttu-id="7114b-142">Weitere Informationen finden Sie in diesen zusätzlichen Ressourcen, damit Sie mit dem Erstellen von Webinhalten für diese neuen Geräte beginnen können.</span><span class="sxs-lookup"><span data-stu-id="7114b-142">For more information, see these additional resources to get started building web content for these new devices.</span></span>

- [<span data-ttu-id="7114b-143">Dokumentation zum Erstellen von apps auf Dual-Screen-Geräten</span><span class="sxs-lookup"><span data-stu-id="7114b-143">Documentation for creating apps on dual-screen devices</span></span>][DualScreenDocs]
- [<span data-ttu-id="7114b-144">Die Microsoft Edge Web Platform-Erläuterung für neue APIs zum Erstellen von Weberfahrungen auf faltbaren und Dual-Screen-Geräten</span><span class="sxs-lookup"><span data-stu-id="7114b-144">The Microsoft Edge web platform explainer for new APIs to build web experiences on foldable and dual-screen devices</span></span>][WebPlatformExplainer]
- [<span data-ttu-id="7114b-145">Aufzeichnung der Microsoft 365-Entwicklertag Sitzung: Erstellen von Dual-Screen-Erlebnissen für Websites und Web-Apps</span><span class="sxs-lookup"><span data-stu-id="7114b-145">Recording of Microsoft 365 Developer Day session: How to build dual-screen experiences for websites and web apps</span></span>][DeveloperDay]

<!-- image links -->  
[ImageEdgeInspect]: /microsoft-edge/devtools-guide-chromium/media/remote-debugging-surface-duo-inspect-page.msft.png "Abbildung 1: die Seite "Edge://Inspect" in Microsoft Edge auf dem Desktop"
[ImageDuoEmulator]: /microsoft-edge/devtools-guide-chromium/media/remote-debugging-surface-duo-emulator.msft.png "Abbildung 2: der Surface Duo-Emulator"
[ImageDuoEmulatorEdge]: /microsoft-edge/devtools-guide-chromium/media/remote-debugging-surface-duo-emulator-edge.msft.png "Abbildung 3: die Microsoft Edge-App auf dem Surface Duo-Emulator"
[ImageEdgeInspectTargets]: /microsoft-edge/devtools-guide-chromium/media/remote-debugging-surface-duo-inspect-page-with-targets.msft.png "Abbildung 4: die Seite "Edge://Inspect" zeigt eine Liste der geöffneten Registerkarten in der auf dem Emulator ausgeführten Microsoft Edge-APP an."
[ImageToggleScreencastIcon]: images/toggle-screencast-icon.msft.png
[ImageDevTools]: /microsoft-edge/devtools-guide-chromium/media/remote-debugging-surface-duo-devtools.msft.png "Abbildung 5: Verwenden des Microsoft Edge-devtools zum Debuggen von Bing in der Microsoft Edge-App auf dem Surface Duo-Emulator"

<!-- links -->  
[RemoteDebuggingAndroid]: /microsoft-edge/devtools-guide-chromium/remote-debugging/index "Erste Schritte mit dem Remote Debuggen von Android-Geräten"
[PwaDocs]: /microsoft-edge/progressive-web-apps-chromium/index "Progressive Web-Apps unter Windows"
[DevToolsDocs]: /microsoft-edge/devtools-guide-chromium "Microsoft Edge (Chrom)-Entwickler Tools"
[TroubleshootingAndroid]: /microsoft-edge/devtools-guide-chromium/remote-debugging/index#troubleshooting-devtools-is-not-detecting-the-android-device "Problembehandlung: devtools erkennt das Android-Gerät nicht."

[AndroidEdge]: https://play.google.com/store/apps/details?id=com.microsoft.emmx "Microsoft Edge Android-App"
[SurfaceDuo]: https://www.microsoft.com/surface/devices/surface-duo "Einführung in Surface Duo"
[DesktopEdge]: https://www.microsoft.com/edge/ "Einführung in das neue Microsoft Edge"
[DuoEmulator]: https://docs.microsoft.com/dual-screen/android/use-emulator "Verwenden des Surface DUo-Emulators"
[DuoSdk]: https://www.microsoft.com/download/details.aspx?id=100847 "Surface Duo SDK Preview-Version"
[DuoSdkDocs]: https://docs.microsoft.com/dual-screen/android/get-duo-sdk "Abrufen des Surface Duo SDK"
[DualScreenDocs]: https://docs.microsoft.com/dual-screen/ "Erstellen von Apps für Dual-Screen-Geräte"
[WebPlatformExplainer]: https://github.com/MicrosoftEdge/MSEdgeExplainers/blob/master/Foldables/explainer.md "Webplattform-Grundtypen für aufgeklärte Erfahrungen auf faltbaren Geräten"
[DeveloperDay]: https://youtu.be/DXrZWsqXPVc "Erstellen von Dual-Screen-Erlebnissen für die Website und Web-Apps"
