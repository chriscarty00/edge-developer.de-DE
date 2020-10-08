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
# Erste Schritte mit Remote Debuggen Surface Duo-Emulatoren

In diesem Artikel durchlaufen Sie den Vorgang des Remotedebuggens von Webinhalten in der [Microsoft Edge-App][AndroidEdge] auf einem [Surface Duo][SurfaceDuo] -Emulator von einer Desktop Instanz von [Microsoft Edge][DesktopEdge]. Informationen zum Debuggen auf einem Surface Duo-Gerät finden Sie im Leitfaden zum [Remotedebuggen von Android-Geräten][RemoteDebuggingAndroid].

## Bevor Sie beginnen

Installieren Sie das [Surface Duo SDK][DuoSdk] , bevor Sie den [Surface Duo-Emulator][DuoEmulator]ausführen. Weitere Informationen finden Sie unter [Abrufen des Surface Duo SDK][DuoSdkdocs].

## Schritt 1: Navigieren zu Edge://Inspect

Öffnen Sie eine Desktop Instanz von [Microsoft Edge][DesktopEdge], und navigieren Sie zu `edge://inspect` .

> ##### Abbildung1  
> Die `edge://inspect` Seite in Microsoft Edge auf dem Desktop auf der ![ Seite "Edge://Inspect" in Microsoft Edge auf dem Desktop][ImageEdgeInspect]

> [!NOTE]
> Wenn die `edge://inspect` Seite den [Surface Duo-Emulator][DuoEmulator]nicht erkennt, starten Sie den Emulator neu.

## Schritt 2: Starten des Surface Duo-Emulators

Starten Sie den [Surface Duo-Emulator][DuoEmulator]. Beachten Sie, dass der Emulator zwei verschiedene Bildschirme anzeigt, die auf dem Emulator ausgeführt werden.

> ##### Abbildung2
> Der Surface Duo-Emulator ![ der Surface Duo-Emulator][ImageDuoEmulator]  

## Schritt 3: Laden von Webinhalten in Microsoft Edge auf dem Surface Duo-Emulator

Wischen Sie auf einem der beiden Bildschirme auf der Favoritenleiste des [Surface Duo-Emulators][DuoEmulator] nach oben, um die APP-Schublade anzuzeigen. Wählen Sie **Edge** aus, um die [Microsoft Edge-App][AndroidEdge]zu starten.

> ##### Abbildung 3
> Die Microsoft Edge-App auf dem Surface Duo-Emulator ![ die Microsoft Edge-App auf dem Surface Duo-Emulator][ImageDuoEmulatorEdge]  

Navigieren Sie in der [Microsoft Edge-App][AndroidEdge]zu der Website oder App, die Sie debuggen möchten.

## Schritt 4: Debuggen von Webinhalten aus dem Surface Duo-Emulator 

Wechseln Sie zurück zur Desktop Instanz von [Microsoft Edge][DesktopEdge]. `edge://inspect`Auf der Seite wird nun der **SurfaceDuoEmulator** mit einer Liste der geöffneten Registerkarten oder [PWAs][PwaDocs] angezeigt, die auf dem [Surface Duo-Emulator][DuoEmulator]ausgeführt werden.

> ##### Abbildung4
> Auf der `edge://inspect` Seite wird eine Liste der geöffneten Registerkarten in der Microsoft Edge-App angezeigt, die auf dem Emulator ausgeführt wird. auf der Seite "Edge://Inspect" wird ![ eine Liste der geöffneten Registerkarten in der auf dem Emulator ausgeführten Microsoft Edge-App angezeigt.][ImageEdgeInspectTargets]  

> [!NOTE]
> Wenn **SurfaceDuoEmulator** auf der Seite nicht angezeigt `edge://inspect` wird, versuchen Sie, die Registerkarten in der [Microsoft Edge-App][AndroidEdge] auf dem [Surface Duo-Emulator][DuoEmulator]zu öffnen oder zu schließen. Weitere Schritte zur Problembehandlung finden Sie im [Abschnitt Problembehandlung für Android-Geräte][TroubleshootingAndroid].

Wählen Sie in der Liste der geöffneten Registerkarten, die im Emulator ausgeführt werden, auf der Registerkarte über **prüfen** aus, auf der die zu debuggenden Webinhalte enthalten sind. Die [Microsoft Edge-devtools][DevToolsDocs] wird in einem neuen Fenster geöffnet. Wählen Sie **Screencast** umschalten ![ Screencast ][ImageToggleScreencastIcon] aus, um die Webinhalte aus Ihrem [Surface Duo-Emulator][DuoEmulator] im devtools-Fenster anzuzeigen. Sie können jetzt die Microsoft Edge-devtools verwenden, um Ihre Webinhalte auf dem [Surface Duo-Emulator][DuoEmulator]zu debuggen.

> ##### Abbildung5
> Verwenden des Microsoft Edge-devtools zum Debuggen von Bing in der Microsoft Edge-App auf dem Surface Duo-Emulator ![ mithilfe der Microsoft Edge-devtools zum Debuggen von Bing in der Microsoft Edge-App auf dem Surface Duo-Emulator][ImageDevTools]  

> [!NOTE]
> Wenn Sie die [Microsoft Edge-App][AndroidEdge] über beide Bildschirme im Emulator überspannen, gibt der Screencast die neue Größe der APP, aber nicht das Scharnier wieder. Wenn Sie wissen möchten, wie sich das Scharnier auf das Layout Ihres Webinhalts auswirkt, verwenden Sie den [Surface Duo-Emulator][DuoEmulator] anstelle des Screencasts.

## Weitere Ressourcen

Das Web ist eine großartige Plattform für die neue Klasse von faltbaren und Dual-Screen-Geräten, da Sie Ihre HTML-, CSS-und JavaScript-Datei einmal schreiben können und Sie auf Einzelbildschirm-, Dual-Screen-und faltbaren Geräten hervorragend aussehen. Weitere Informationen finden Sie in diesen zusätzlichen Ressourcen, damit Sie mit dem Erstellen von Webinhalten für diese neuen Geräte beginnen können.

- [Dokumentation zum Erstellen von apps auf Dual-Screen-Geräten][DualScreenDocs]
- [Die Microsoft Edge Web Platform-Erläuterung für neue APIs zum Erstellen von Weberfahrungen auf faltbaren und Dual-Screen-Geräten][WebPlatformExplainer]
- [Aufzeichnung der Microsoft 365-Entwicklertag Sitzung: Erstellen von Dual-Screen-Erlebnissen für Websites und Web-Apps][DeveloperDay]

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
