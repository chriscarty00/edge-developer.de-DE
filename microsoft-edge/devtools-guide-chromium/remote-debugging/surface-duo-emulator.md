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
# Erste Schritte mit Remote Debuggen Surface Duo-Emulatoren  

In diesem Artikel durchlaufen Sie den Vorgang des Remotedebuggens von Webinhalten in der [Microsoft Edge-App][GooglePlayStoreAppsComMicrosoftEmmx] auf einem [Surface Duo][MicrosoftSurfaceDevicesSurfaceDuo] -Emulator von einer Desktop Instanz von [Microsoft Edge][MicrosoftEdge].  Informationen zum Debuggen auf einem Surface Duo-Gerät finden Sie im Leitfaden zum [Remotedebuggen von Android-Geräten][DevtoolsRemoteDebuggingMain].  

## Bevor Sie beginnen

Installieren Sie das [Surface Duo SDK][MicrosoftDownload100847] , bevor Sie den [Surface Duo-Emulator][DualScreenAndroidUseEmulator]ausführen.  Weitere Informationen finden Sie unter [Abrufen des Surface Duo SDK][DualScreenAndroidGetDuoSdk].  

## Schritt 1: Navigieren zu Edge://Inspect  

Öffnen Sie eine Desktop Instanz von [Microsoft Edge][MicrosoftEdge], und navigieren Sie zu `edge://inspect` .  

:::image type="complex" source="../media/remote-debugging-surface-duo-inspect-page.msft.png" alt-text="Die Seite "Edge://Inspect" in Microsoft Edge auf dem Desktop" lightbox="../media/remote-debugging-surface-duo-inspect-page.msft.png":::
   Die `edge://inspect` Seite in Microsoft Edge auf dem Desktop  
:::image-end:::

> [!NOTE]
> Wenn die `edge://inspect` Seite den [Surface Duo-Emulator][DualScreenAndroidUseEmulator]nicht erkennt, starten Sie den Emulator neu.  

## Schritt 2: Starten des Surface Duo-Emulators  

Starten Sie den [Surface Duo-Emulator][DualScreenAndroidUseEmulator].  Beachten Sie, dass der Emulator zwei verschiedene Bildschirme anzeigt, die auf dem Emulator ausgeführt werden.  

:::image type="complex" source="../media/remote-debugging-surface-duo-emulator.msft.png" alt-text="Der Surface Duo-Emulator" lightbox="../media/remote-debugging-surface-duo-emulator.msft.png":::
   Der Surface Duo-Emulator  
:::image-end:::  

## Schritt 3: Laden von Webinhalten in Microsoft Edge auf dem Surface Duo-Emulator  

Wischen Sie auf einem der beiden Bildschirme auf der Favoritenleiste des [Surface Duo-Emulators][DualScreenAndroidUseEmulator] nach oben, um die APP-Schublade anzuzeigen.  Wählen Sie **Edge** aus, um die [Microsoft Edge-App][GooglePlayStoreAppsComMicrosoftEmmx]zu starten.  

:::image type="complex" source="../media/remote-debugging-surface-duo-emulator-edge.msft.png" alt-text="Die Microsoft Edge-App auf dem Surface Duo-Emulator" lightbox="../media/remote-debugging-surface-duo-emulator-edge.msft.png":::
   Die Microsoft Edge-App auf dem Surface Duo-Emulator  
:::image-end:::  

Navigieren Sie in der [Microsoft Edge-App][GooglePlayStoreAppsComMicrosoftEmmx]zu der Website oder App, die Sie debuggen möchten.  

## Schritt 4: Debuggen von Webinhalten aus dem Surface Duo-Emulator  

Wechseln Sie zurück zur Desktop Instanz von [Microsoft Edge][MicrosoftEdge].  `edge://inspect`Auf der Seite wird nun der **SurfaceDuoEmulator** mit einer Liste der geöffneten Registerkarten oder [PWAs][ProgressiveWebAppsIndex] angezeigt, die auf dem [Surface Duo-Emulator][DualScreenAndroidUseEmulator]ausgeführt werden.  

:::image type="complex" source="../media/remote-debugging-surface-duo-inspect-page-with-targets.msft.png" alt-text="Auf der Seite "Edge://Inspect" wird eine Liste der geöffneten Registerkarten in der Microsoft Edge-App angezeigt, die auf dem Emulator ausgeführt wird." lightbox="../media/remote-debugging-surface-duo-inspect-page-with-targets.msft.png":::
   `edge://inspect`Auf der Seite wird eine Liste der geöffneten Registerkarten in der Microsoft Edge-App angezeigt, die auf dem Emulator ausgeführt wird.  
:::image-end:::  

> [!NOTE]
> Wenn **SurfaceDuoEmulator** auf der Seite nicht angezeigt `edge://inspect` wird, versuchen Sie, die Registerkarten in der [Microsoft Edge-App][GooglePlayStoreAppsComMicrosoftEmmx] auf dem [Surface Duo-Emulator][DualScreenAndroidUseEmulator]zu öffnen oder zu schließen.  Weitere Schritte zur Problembehandlung finden Sie im [Abschnitt Problembehandlung für Android-Geräte][DevtoolsRemoteDebuggingIndexTroubleshootingDevtoolsIsNotDetectingAndroidDevice].  

Wählen Sie in der Liste der geöffneten Registerkarten, die im Emulator ausgeführt werden, auf der Registerkarte über **prüfen** aus, auf der die zu debuggenden Webinhalte enthalten sind.  Die [Microsoft Edge-devtools][DevtoolsIndex] wird in einem neuen Fenster geöffnet.  Wählen Sie **Screencast umschalten** \ ( ![ Screencast wechseln ][ImageToggleScreencastIcon] \) aus, um die Webinhalte aus Ihrem [Surface Duo-Emulator][DualScreenAndroidUseEmulator] im devtools-Fenster anzuzeigen.  Sie können jetzt die Microsoft Edge-devtools verwenden, um Ihre Webinhalte auf dem [Surface Duo-Emulator][DualScreenAndroidUseEmulator]zu debuggen.  

:::image type="complex" source="../media/remote-debugging-surface-duo-devtools.msft.png" alt-text="Verwenden des Microsoft Edge-devtools zum Debuggen von Bing in der Microsoft Edge-App auf dem Surface Duo-Emulator" lightbox="../media/remote-debugging-surface-duo-devtools.msft.png":::
   Verwenden des Microsoft Edge-devtools zum Debuggen von Bing in der Microsoft Edge-App auf dem Surface Duo-Emulator  
:::image-end:::  

> [!NOTE]
> Wenn Sie die [Microsoft Edge-App][GooglePlayStoreAppsComMicrosoftEmmx] über beide Bildschirme im Emulator überspannen, gibt der Screencast die neue Größe der APP, aber nicht das Scharnier wieder.  Wenn Sie wissen möchten, wie sich das Scharnier auf das Layout Ihres Webinhalts auswirkt, verwenden Sie den [Surface Duo-Emulator][DualScreenAndroidUseEmulator] anstelle des Screencasts.  

## Weitere Ressourcen  

Das Web ist eine großartige Plattform für die neue Klasse von faltbaren und Dual-Screen-Geräten, da Sie Ihre HTML-, CSS-und JavaScript-Datei einmal schreiben können und Sie auf Einzelbildschirm-, Dual-Screen-und faltbaren Geräten hervorragend aussehen.  Weitere Informationen finden Sie in diesen zusätzlichen Ressourcen, damit Sie mit dem Erstellen von Webinhalten für diese neuen Geräte beginnen können.  

*   [Dokumentation zum Erstellen von apps auf Dual-Screen-Geräten][DualScreenIndex]  
*   [Die Microsoft Edge Web Platform-Erläuterung für neue APIs zum Erstellen von Weberfahrungen auf faltbaren und Dual-Screen-Geräten][GithubMicrosoftedgeMsedgeexplainersFoldablesExplainer]  
*   [Aufzeichnung der Microsoft 365-Entwicklertag Sitzung: Erstellen von Dual-Screen-Erlebnissen für Websites und Web-Apps][YoutubeDxrzwsqxpvc]  

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
