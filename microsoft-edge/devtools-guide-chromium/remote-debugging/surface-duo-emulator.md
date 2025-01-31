---
description: Erste Schritte mit Remote debugging Surface Duo-Emulatoren.
title: Erste Schritte mit Remotedebu debugging Surface Duo-Emulatoren
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/25/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, web development, f12 tools, devtools, remote debugging, android, surface duo
ms.openlocfilehash: 49b16f3c920735b34d44455bae437442cac3bf6e
ms.sourcegitcommit: bff24ab1f0a66aaf4c7f5ff81cea3eb28c6d8380
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/26/2021
ms.locfileid: "11461241"
---
# <a name="get-started-with-remote-debugging-surface-duo-emulators"></a>Erste Schritte mit remote debuggen von Surface Duo-Emulatoren  

In diesem Artikel werden Sie durch den Prozess des Remotedebugierens Ihrer Webinhalte in der [Microsoft Edge-App auf][GooglePlayStoreAppsComMicrosoftEmmx] einem [Surface Duo-Emulator][MicrosoftSurfaceDevicesSurfaceDuo] von einer Desktopinstanz von [Microsoft Edge.][MicrosoftEdge]  Informationen zum Debuggen auf einem Surface Duo-Gerät finden Sie in unserem Leitfaden zum [Remotedebugen von Android-Geräten.][DevtoolsRemoteDebuggingMain]  

## <a name="before-you-begin"></a>Vorbemerkungen

Installieren Sie [das Surface Duo SDK,][MicrosoftDownload100847] bevor Sie den [Surface Duo-Emulator ausführen.][DualScreenAndroidUseEmulator]  Weitere Informationen finden Sie unter [Get the Surface Duo SDK][DualScreenAndroidGetDuoSdk].  

## <a name="step-1-navigate-to-edgeinspect"></a>Schritt 1: Navigieren Sie zu edge://inspect  

Öffnen Sie eine Desktopinstanz [von Microsoft Edge][MicrosoftEdge], und navigieren Sie zu `edge://inspect` .  

:::image type="complex" source="../media/remote-debugging-surface-duo-inspect-page.msft.png" alt-text="Die edge://inspect in Microsoft Edge auf dem Desktop" lightbox="../media/remote-debugging-surface-duo-inspect-page.msft.png":::
   Die `edge://inspect` Seite in Microsoft Edge auf dem Desktop  
:::image-end:::

> [!NOTE]
> Wenn die `edge://inspect` Seite den Surface [Duo-Emulator][DualScreenAndroidUseEmulator]nicht erkennt, starten Sie den Emulator neu.  

## <a name="step-2-launch-the-surface-duo-emulator"></a>Schritt 2: Starten des Surface Duo-Emulators  

Starten Sie den [Surface Duo-Emulator.][DualScreenAndroidUseEmulator]  Beachten Sie, dass der Emulator zwei verschiedene Bildschirme anzeigt, die auf dem Emulator ausgeführt werden.  

:::image type="complex" source="../media/remote-debugging-surface-duo-emulator.msft.png" alt-text="Der Surface Duo-Emulator" lightbox="../media/remote-debugging-surface-duo-emulator.msft.png":::
   Der Surface Duo-Emulator  
:::image-end:::  

## <a name="step-3-load-your-web-content-in-microsoft-edge-on-the-surface-duo-emulator"></a>Schritt 3: Laden von Webinhalten in Microsoft Edge Surface Duo-Emulator  

Wischen Sie auf beiden Bildschirmen im Favoritenfach des [Surface Duo-Emulators][DualScreenAndroidUseEmulator] nach oben, um die Apps-Drawer anzuzeigen.  Wählen **Sie Edge** aus, um die Microsoft Edge [starten.][GooglePlayStoreAppsComMicrosoftEmmx]  

:::image type="complex" source="../media/remote-debugging-surface-duo-emulator-edge.msft.png" alt-text="Die Microsoft Edge-App im Surface Duo-Emulator" lightbox="../media/remote-debugging-surface-duo-emulator-edge.msft.png":::
   Die Microsoft Edge-App im Surface Duo-Emulator  
:::image-end:::  

Navigieren Sie zu der Website oder App, die Sie in der app [debuggen Microsoft Edge möchten.][GooglePlayStoreAppsComMicrosoftEmmx]  

## <a name="step-4-debug-your-web-content-from-the-surface-duo-emulator"></a>Schritt 4: Debuggen Von Webinhalten aus dem Surface Duo-Emulator  

Wechseln Sie zurück zur Desktopinstanz [Microsoft Edge][MicrosoftEdge].  Auf `edge://inspect` der Seite wird nun **surfaceDuoEmulator** mit einer Liste der geöffneten Registerkarten oder [PWAs][ProgressiveWebAppsIndex] angezeigt, die im [Surface Duo-Emulator ausgeführt werden.][DualScreenAndroidUseEmulator]  

:::image type="complex" source="../media/remote-debugging-surface-duo-inspect-page-with-targets.msft.png" alt-text="Auf edge://inspect seite wird eine Liste der geöffneten Registerkarten in der Microsoft Edge app angezeigt, die auf dem Emulator ausgeführt wird" lightbox="../media/remote-debugging-surface-duo-inspect-page-with-targets.msft.png":::
   Auf der Seite wird eine Liste der geöffneten Registerkarten in der Microsoft Edge `edge://inspect` angezeigt, die auf dem Emulator ausgeführt wird.  
:::image-end:::  

> [!NOTE]
> Wenn **SurfaceDuoEmulator** nicht auf der Seite angezeigt wird, versuchen Sie, Registerkarten in der `edge://inspect` Microsoft Edge-App im Surface [Duo-Emulator][GooglePlayStoreAppsComMicrosoftEmmx] zu öffnen oder [zu schließen.][DualScreenAndroidUseEmulator]  Weitere Schritte zur Problembehandlung finden Sie im [Abschnitt Problembehandlung für Android-Geräte.][DevtoolsRemoteDebuggingIndexTroubleshootingDevtoolsIsNotDetectingAndroidDevice]  

Wählen Sie in der Liste der geöffneten Registerkarten, die auf dem Emulator ausgeführt werden, auf der Registerkarte überprüfen aus, auf der die zu debuggenden Webinhalte enthalten sind. ****  Die [Microsoft Edge DevTools][DevtoolsIndex] wird in einem neuen Fenster geöffnet.  Wählen **Sie Screencast umschalten** \( Screencast umschalten \), um den Webinhalt aus dem Surface Duo-Emulator im ![ ](../media/toggle-screencast-icon.msft.png) DevTools-Fenster anzuzeigen. [][DualScreenAndroidUseEmulator]  Sie können jetzt die DevTools-Microsoft Edge verwenden, um Ihre Webinhalte im [Surface Duo-Emulator zu debuggen.][DualScreenAndroidUseEmulator]  

:::image type="complex" source="../media/remote-debugging-surface-duo-devtools.msft.png" alt-text="Verwenden der Microsoft Edge DevTools zum Debuggen Bing in der Microsoft Edge-App im Surface Duo-Emulator" lightbox="../media/remote-debugging-surface-duo-devtools.msft.png":::
   Verwenden der Microsoft Edge DevTools zum Debuggen Bing in der Microsoft Edge-App im Surface Duo-Emulator  
:::image-end:::  

> [!NOTE]
> Wenn Sie die [Microsoft Edge-App][GooglePlayStoreAppsComMicrosoftEmmx] auf beiden Bildschirmen im Emulator überspannen, spiegelt das Screencast die neue Größe der App wider, aber nicht das Scharnier.  Um zu verstehen, wie sich das Scharnier auf das Layout Ihrer Webinhalte aus wirkt, verwenden Sie den [Surface Duo-Emulator][DualScreenAndroidUseEmulator] anstelle des Screencasts.  

## <a name="additional-resources"></a>Weitere Ressourcen  

Das Web ist eine großartige Plattform für die neue Klasse von zusammenklappbaren Und Dual-Screen-Geräten, da Sie Ihre HTML, CSS und JavaScript einmal schreiben können und es auf einzelnen Bildschirmen, dualen Bildschirmen und faltbaren Geräten großartig aussehen lässt.  Weitere Informationen finden Sie in den folgenden zusätzlichen Ressourcen, um mit dem Erstellen von Webinhalten für diese neuen Geräte zu beginnen.  

*   [Dokumentation zum Erstellen von Apps auf Dual-Screen-Geräten][DualScreenIndex]  
*   [Die Microsoft Edge web platform explainer for new APIs to build web experiences on foldable and dual-screen devices][GithubMicrosoftedgeMsedgeexplainersFoldablesExplainer]  
*   [Aufzeichnung Microsoft 365 Developer Day-Sitzung: Erstellen von Dualscreen-Erfahrungen für Websites und Web-Apps][YoutubeDxrzwsqxpvc]  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsIndex]: ../index.md "Microsoft Edge (Chromium) -Entwicklertools | Microsoft Docs"  
[ProgressiveWebAppsIndex]: ../../progressive-web-apps-chromium/index.md "Progressive Web Apps auf Windows | Microsoft Docs"  
[DevtoolsRemoteDebuggingMain]: ./index.md "Erste Schritte mit remote debuggen von Android-Geräten | Microsoft Docs"  
[DevtoolsRemoteDebuggingIndexTroubleshootingDevtoolsIsNotDetectingAndroidDevice]: ./index.md#troubleshooting-devtools-is-not-detecting-the-android-device "Problembehandlung: DevTools erkennt das Android-Gerät nicht – Erste Schritte mit dem Remotedebugieren von Android-Geräten | Microsoft Docs"  

[DualScreenIndex]: /dual-screen/index "Erstellen von Apps für Zwei-Bildschirm-| Microsoft Docs"  
[DualScreenAndroidUseEmulator]: /dual-screen/android/use-emulator "Verwenden des Surface DUo-Emulators | Microsoft Docs"  
[DualScreenAndroidGetDuoSdk]: /dual-screen/android/get-duo-sdk "Get the Surface Duo SDK | Microsoft Docs"  

[MicrosoftEdge]: https://www.microsoft.com/edge "Einführung in die Microsoft Edge"  
[MicrosoftSurfaceDevicesSurfaceDuo]: https://www.microsoft.com/surface/devices/surface-duo "Das neue Surface Duo-| Microsoft Surface"  
[MicrosoftDownload100847]: https://www.microsoft.com/download/details.aspx?id=100847 "Surface Duo SDK Preview Release | Microsoft Download Center"  

[GooglePlayStoreAppsComMicrosoftEmmx]: https://play.google.com/store/apps/details?id=com.microsoft.emmx "Microsoft Edge: Webbrowser | GooglePlay"  

[GithubMicrosoftedgeMsedgeexplainersFoldablesExplainer]: https://github.com/MicrosoftEdge/MSEdgeExplainers/blob/master/Foldables/explainer.md "Webplattformgrundtypen für aufklappbare Geräte – MicrosoftEdge/MSEdgeExplainers | GitHub"  

[YoutubeDxrzwsqxpvc]: https://youtu.be/DXrZWsqXPVc "Erstellen von dualen Bildschirmen für die Website- und Web-Apps-| YouTube"  
