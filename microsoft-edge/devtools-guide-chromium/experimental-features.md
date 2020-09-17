---
description: Die neuesten experimentellen Features in Microsoft Edge devtools
title: Experimentelle Funktionen
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/08/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Web-Entwicklung, F12-Tools, devtools, Experiment
ms.openlocfilehash: ce8388e8065055e6002bd8541101bef658c7a403
ms.sourcegitcommit: 744e2ecf42bcc427ae33e5dadbf6cd48ee0ab6a5
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/17/2020
ms.locfileid: "11016746"
---
# Experimentelle Funktionen  

Microsoft Edge-devtools bieten Zugriff auf experimentelle Features, die sich noch in der Entwicklung befinden.  Sie können testen und p[Feedback geben](#providing-feedback-on-experimental-features) , bevor die einzelnen Funktionen freigegeben werden.  

Während experimentelle Features in allen Kanälen von Microsoft Edge verfügbar sind, erhalten Sie möglicherweise die neuesten experimentellen Features mithilfe des Canary-Kanals von Microsoft Edge.  

## Aktivieren von experimentellen Features  

Führen Sie die folgenden Schritte aus, um die experimentellen Features von \ (oder Off \) in Microsoft Edge zu aktivieren.  

1.  [Öffnen Sie devtools][DevtoolsOpen].  
     *   Wählen Sie `Control` + `Shift` + `I` \ (Windows \) oder `Command` + `Option` + `I` \ (macOS \) aus.  Weitere Informationen finden Sie unter [Tastenkombinationen für Microsoft Edge devtools][DevToolsShortcuts].  
1.  Öffnen Sie den Bereich " [Einstellungen][DevToolsCustomizeSettings] ".  
    *   Wählen Sie aus `Shift` + `?` .  Weitere Informationen finden Sie unter [Tastenkombinationen für Microsoft Edge devtools][DevToolsShortcuts].  
1.  Wählen Sie auf der linken Seite des Bereichs **Einstellungen** den Abschnitt **Experimente** aus.  
    
    :::image type="complex" source="./media/experiments-devtools.msft.png" alt-text="Liste der Experimente in den devtools-Einstellungen" lightbox="./media/experiments-devtools.msft.png":::
       Liste der Experimente in den devtools-Einstellungen  
    :::image-end:::  
    
1.  Scrollen Sie auf der Seite **Experimente** durch die Liste aller verfügbaren experimentellen Features, und aktivieren Sie das Kontrollkästchen neben den einzelnen Features, die Sie testen möchten.  
1.  Schließen Sie die Microsoft Edge-devtools, und öffnen Sie Sie erneut.  

> [!NOTE]
> Experimentelle Features werden ständig aktualisiert, was zu Leistungsproblemen führen kann.  Wenn Sie ein experimentelles Feature deaktivieren möchten, öffnen Sie die Seite **Experimente** , und deaktivieren Sie das Kontrollkästchen des experimentellen Features, das Sie deaktivieren möchten.  

## Hervorgehobene experimentelle Features  

In den folgenden Abschnitten werden die neuen experimentellen Features beschrieben, die in Microsoft Edge zur Verfügung stehen.  

| Experimentelle Funktion | Microsoft Edge-Version |  
|:--- |:--- |  
| [Emulation: Unterstützung des Dual-Screen-Modus](#emulation-support-dual-screen-mode) | 84 oder höher |  
| [Debuggen von neuen CSS-Raster Features aktivieren](#enable-new-css-grid-debugging-features) | 85 oder höher |  
| [Aktivieren der Unterstützung für das Verschieben von Tabstopps zwischen Bereichen](#enable-support-to-move-tabs-between-panels) | 85 oder höher |  
| [Webhint aktivieren](#enable-webhint) | 85 oder höher |  
| [Aktivieren der Netzwerk Konsole](#enable-network-console) | 85 oder höher |  
| [Quellauftrags Anzeige aktivieren](#enable-source-order-viewer) | 86 oder höher |  

### Emulation: Unterstützung des Dual-Screen-Modus  

Bietet zusätzliche Features zum Emulieren von zwei neuen Dual-Screen-und faltbaren Geräten in Microsoft Edge.  

*   [Surface Duo][SurfaceDevicesDuo]  
*   [Samsung Galaxy Fold][SamsungMobileGalaxyFold]  

Emulieren Sie die Geräte, und wechseln Sie zwischen den folgenden Haltungen.  

*   Einzelbild-oder gefaltete Haltung  
*   Dual-Screen-oder entfaltete Haltung  
 
[Aktivieren Sie experimentelle Webplattform-APIs](#enable-experimental-apis) , und verwenden Sie das [Feature "CSS-Medien Bildschirm übergreifend"][DualScreenDocsCssMedia] und die [JavaScript-getWindowSegments-API][DualScreenDocsJSAPI] , um Ihre Website \ (oder App \) für Dual-Screen-und faltbare Geräte zu verbessern.

:::image type="complex" source="./media/experiments-surface-duo-emulation.msft.png" alt-text="Emulieren von Surface Duo in Microsoft Edge" lightbox="./media/experiments-surface-duo-emulation.msft.png":::  
   Emulieren von Surface Duo in Microsoft Edge  
:::image-end:::  

#### Aktivieren von experimentellen APIs  

Aktivieren Sie das Kennzeichen in Microsoft Edge, um das [Feature "CSS-Medien Bildschirm übergreifend"][DualScreenDocsCssMedia] und die [JavaScript-getWindowSegments-API][DualScreenDocsJSAPI]zu verwenden `Experimental Web Platform features` .  Führen Sie die folgenden Schritte aus.

1.  Navigieren Sie zu `edge://flags` .  
1.  Geben Sie im Textfeld **Such Kennzeichnungen** `Experimental Web Platform features` das Flag **experimental Web Platform Features** ein, und ändern Sie **deaktiviert** in **aktiviert**.  
1.  Starten Sie Microsoft Edge neu.  

:::image type="complex" source="./media/experiments-dual-screen-emulation-edge-flags.msft.png" alt-text="Aktivieren des Kennzeichens "experimentelle Webplattform-Features"" lightbox="./media/experiments-dual-screen-emulation.msft.png":::
   Aktivieren des Kennzeichens "experimentelle Webplattform-Features"  
:::image-end:::  

> [!NOTE]
> Wenn Sie CSS- [medienabfragen][DualScreenDocsCssMedia] oder die [JavaScript Windows-Segment Aufzählungs-API][DualScreenDocsJSAPI] verwenden, um Ihre Website oder App für das [Surface Duo][SurfaceDevicesDuo]zu verbessern, müssen Sie auch das Kennzeichen **experimentelle Webplattform-Features** in der [Android-App für Microsoft Edge][GooglePlayMicrosoftEdge] auf Ihrem [Surface Duo][SurfaceDevicesDuo] -Gerät aktivieren.
> 
> Wenn das Flag für **experimentelle Webplattform-Features** in der Microsoft Edge-App für [Desktops][MicrosoftEdge] aktiviert ist und in der [Android-App für Microsoft Edge][GooglePlayMicrosoftEdge]deaktiviert ist, entspricht das Verhalten Ihrer Website oder App im Surface Duo-Emulator auf dem Desktop Microsoft Edge nicht der [Android Microsoft Edge-App][GooglePlayMicrosoftEdge] auf [Surface Duo][SurfaceDevicesDuo].  Stellen Sie sicher, dass die Flags für Android und Desktop Microsoft Edge übereinstimmen, um den Surface Duo-Emulator erfolgreich im [Desktop Microsoft Edge][MicrosoftEdge]zu verwenden.  

#### Testen auf faltbaren und Dual-Screen-Geräten  

Wenn Sie das [Surface Duo][SurfaceDevicesDuo] in einer Haltung mit zwei Bildschirmen in Microsoft Edge emulieren, wird die Naht \ (der Abstand zwischen den beiden Bildschirmen \) über Ihre Website oder App gezeichnet.  

Die emulierte Anzeige entspricht der Art, in der Ihre Website \ (oder App \) in der [Microsoft Edge Android-App][GooglePlayMicrosoftEdge] auf [Surface Duo][SurfaceDevicesDuo]gerendert wird.  Möglicherweise müssen Sie Ihre Website aktualisieren \ (oder App \), damit Sie besser entlang der Naht angezeigt werden.  Weitere Informationen zum Anpassen Ihrer Website \ (oder App \) an die Naht finden Sie unter [Arbeiten mit der Naht][DualScreenIntroductionHowWorkSeam] in der Surface Duo-Dokumentation.  

Die [Gerätesymbolleiste][DevtoolsDeviceModeIndexSimulateMobileViewport] verfügt über zusätzliche Features, die Sie beim Testen Ihrer Website oder app in verschiedenen Haltungen und Ausrichtungen unterstützen.  Wählen Sie **drehen** \ ( ![ drehen ][ImageRotateIcon] \) aus, um das Ansichtsfenster in Querformat zu drehen. Kombinieren Sie das Feature mit **Span** \ ( ![ Span ][ImageSpanIcon] \), um zwischen Einzelbildschirm-oder gefalteten und Dual-Screen-oder entfalteten Haltungen umzuschalten.  Zusammen können die Features das Testen Ihrer Website oder app in allen vier möglichen Haltungen und Ausrichtungen ermöglichen.  

:::image type="complex" source="./media/experiments-dual-screen-emulation-rotate-span.msft.png" alt-text="Matrix von Haltungen und Ausrichtungen für Dual-Screen-und faltbare Geräte" lightbox="./media/experiments-dual-screen-emulation-rotate-span.msft.png":::
   Matrix von Haltungen und Ausrichtungen für Dual-Screen-und faltbare Geräte  
:::image-end:::  

Das **Feature "experimentelle Webplattform-Features** \ ( ![ ExperimentalApis ][ImageExperimentalApisIcon] \)" zeigt den Zustand des Kennzeichens " **experimentelle Web Platform Features** " an.  Wenn die Kennzeichnung aktiviert ist, ist das Symbol hervorgehoben.  Wenn die Kennzeichnung deaktiviert ist, wird das Symbol nicht hervorgehoben.  Um die Kennzeichnung zu aktivieren oder zu deaktivieren, navigieren Sie zu `edge://flags` der Kennzeichnung, und aktivieren Sie Sie.  

<!-- Commenting out until the icon issue is fixed in Edge Canary
The **Experimental Web Platform features** \(![ExperimentalApis][ImageExperimentalApisIcon]\) icon displays the state of the **Experimental Web Platform features** flag.  If the flag is turned on, the icon is highlighted.  If the flag is turned off, the icon is not highlighted.  To turn on \(or off\) the flag, either choose the icon or navigate to `edge://flags` and toggle the flag.   -->

Hier sind weitere Ressourcen, die Ihnen bei der Optimierung Ihrer Website (oder App \) für Dual-Screen-Geräte helfen können:
*   Weitere Informationen zur Web-Entwicklung auf Dual-Screen-Geräten finden Sie unter [Dual-Screen-Web-Erlebnisse][DualScreenWebIndex].  
*   Installieren Sie den [Surface Duo-Emulator][DualScreenAndroidUseEmulator].  Sie unterscheidet sich vom Emulator in Microsoft Edge, emuliert das Surface Duo mit Android und ist in [Android Studio][AndroidDeveloperStudio]integriert.  Wenn Sie weitere Informationen erhalten möchten, navigieren Sie zu [Surface Duo SDK][DualScreenAndroidGetDuoSdk].  

> [!NOTE]
> Die folgende Liste enthält aktuelle bekannte Probleme:
> *   Wenn Sie einen [Microsoft Remote Desktop-Client][RemoteDesktopClientDocs] verwenden, um eine Verbindung mit einem Remote-PC herzustellen und das [Surface Duo][SurfaceDevicesDuo] oder [Samsung Galaxy Fold][SamsungMobileGalaxyFold]zu emulieren, kann der Mauszeiger wackeln oder Stottern.  Wenn Sie dieses Problem vorführen, [Senden Sie uns Feedback](#providing-feedback-on-experimental-features).  

### Debuggen von neuen CSS-Raster Features aktivieren  

Verbessert die on-page-Visualisierungen, wenn Sie Websites mit CSS-Rasterlayouts Debuggen.  Sie können die Overlays in den devtools-Einstellungen weiter anpassen.  

:::image type="complex" source="./media/experiments-grid.msft.png" alt-text="CSS-Raster Debugging-Feature" lightbox="./media/experiments-grid.msft.png":::
   CSS-Raster Debugging-Feature  
:::image-end:::  

Führen Sie die folgenden Aktionen aus, um eine Vorschau der neuesten experimentellen Features anzuzeigen.  

1.  Wählen Sie im Abschnitt **Experimente** das Kontrollkästchen **neue CSS-Raster Debugging-Features aktivieren (Konfigurationsoptionen, die im Bereich Layout-Seitenleiste in Elemente nach dem Neustart verfügbar sind)** .  

<!--Available in Microsoft Edge version 85 and later.  -->  

### Aktivieren der Unterstützung für das Verschieben von Tabstopps zwischen Bereichen  

Normalerweise werden Tools wie **Elemente** und **Netzwerke** nur im Hauptbereich geöffnet, der sich am oberen Rand des devtools befindet.  Tools wie **3D-Ansicht** und **Probleme** , die normalerweise nur in der **Schublade** angezeigt werden, die sich am unteren Rand des devtools befindet.  Nachdem Sie das Experiment ausgewählt haben, können Sie die Tools zwischen dem oberen und unteren Bereich verschieben.  Wenn Sie ein Tool verschieben möchten, zeigen Sie auf die Registerkarte, öffnen Sie das Kontextmenü \ (Klicken Sie mit der rechten Maustaste auf \), und wählen Sie **nach oben** oder **nach unten**verschieben aus.   Mit diesem Experiment können Sie Ihr devtools-Layout anpassen.  Zum ein-oder Ausblenden des **Einschub** Panels wählen Sie `Escape` .  

:::image type="complex" source="./media/experiments-move-panels.msft.png" alt-text="Verschieben von Tabstopps zwischen Bereichen" lightbox="./media/experiments-move-panels.msft.png":::
   Verschieben von Tabstopps zwischen Bereichen  
:::image-end:::  

<!--Available in Microsoft Edge version 85 and later.  -->  

### Webhint aktivieren  

[webhint][WebhintMain] ist ein Open-Source-Tool, das Echtzeitfeedback für Websites und lokale Webseiten bietet.  Der Typ des Feedbacks, das von [webhint][WebhintMain]bereitgestellt wird.  

*   Bedienungshilfen  
*   browserübergreifende Kompatibilität  
*   Sicherheit  
*   Leistung  
*   PWAs  
*   andere häufig auftretende Probleme mit der Web-Entwicklung  

Das [webhint][WebhintMain] -Experiment zeigt das webhint-Feedback im Bereich " [Probleme][DevtoolsIssues] " an.  Wählen Sie ein Problem aus, um die Lösungsdokumentation und eine Liste der betroffenen Ressourcen auf Ihrer Website anzuzeigen.  Wählen Sie einen Ressourcen Link aus, um den entsprechenden Bereich für **Netzwerke**, **Quellen**oder **Elemente** in devtools zu öffnen.  

:::image type="complex" source="./media/experiments-webhint.msft.png" alt-text="webhint-Feedback im Bereich "Probleme"" lightbox="./media/experiments-webhint.msft.png":::
   webhint-Feedback im Bereich " **Probleme** "  
:::image-end:::  

<!--Available in Microsoft Edge version 85 and later.  -->  

### Aktivieren der Netzwerk Konsole  

**Netzwerk Konsole** ist der Arbeitstitel eines Experiments, um synthetische Netzwerkanforderungen über HTTP zu stellen.  Sie können das **Netzwerkkonsolen** Experiment verwenden, um Web-API-Anforderungen zu senden.  

Nachdem Sie das Experiment aktiviert haben, stellen Sie sicher, dass Sie das devtools erneut starten.  Führen Sie die folgenden Schritte aus, um die **Netzwerk Konsole**zu verwenden.    

1.  Öffnen Sie den Bereich **Netzwerk** .  
1.  Suchen Sie die Netzwerkanforderung, die Sie ändern möchten, und senden Sie Sie erneut.  
1.  Öffnen Sie das Kontextmenü \ (Klicken Sie mit der rechten Maustaste auf \), und wählen Sie **Bearbeiten und wiedergeben**aus.  
1.  Wenn die **Netzwerk Konsole** geöffnet wird, bearbeiten Sie die Netzwerk Anforderungsinformationen.  
1.  Wählen Sie **senden**aus.  

:::image type="complex" source="./media/network-network-console.msft.png" alt-text="Netzwerk Konsole im Konsolen Einzug" lightbox="./media/network-network-console.msft.png":::
   **Netzwerk Konsole** im **Konsolen** Einzug  
:::image-end:::  

<!--Available in Microsoft Edge version 85 and later.  -->  

### Quellauftrags Anzeige aktivieren  

Die **Quellauftrags Anzeige** ist ein Experiment, das die Reihenfolge der Elemente in der Seitenquelle anzeigt.  Die Anzeigereihenfolge auf dem Bildschirm kann von der Reihenfolge der Quelle abweichen, die die Bildschirmsprachausgabe und die Tastatur Benutzer verwirrt.  Verwenden Sie das Experiment der **Quellauftrags Anzeige** , um die Unterschiede zwischen der Anzeigereihenfolge auf dem Bildschirm und der Reihenfolge der Quelle zu finden.  

Nachdem Sie das Experiment aktiviert haben, stellen Sie sicher, dass Sie das devtools erneut starten.  So verwenden Sie die Quellauftrags Anzeige:  

1.  Öffnen Sie den Bereich **Elemente** .  
1.  Öffnen Sie den Bereich " **Barrierefreiheit** " im Bereich "Schublade \" (unten).  
1.  Aktivieren Sie im Abschnitt **Quellauftrags Anzeige** das Kontrollkästchen **Quellreihenfolge anzeigen** .  
1.  Markieren Sie ein beliebiges HTML-Element, um ein Overlay anzuzeigen, das die Reihenfolge in der Seitenquelle enthält.  

:::image type="complex" source="./media/experiments-source-order-viewer.msft.png" alt-text="Viewer für Quellreihenfolge im Bereich "Barrierefreiheit"" lightbox="./media/experiments-source-order-viewer.msft.png":::
   **Viewer für Quellreihenfolge** im Bereich " **Barrierefreiheit** "  
:::image-end:::  

<!--Available in Microsoft Edge version 86 and later.  -->  

## Frühere experimentelle Features  

*   die [3D-Ansicht][Devtools3dViewIndex] ist jetzt in Microsoft Edge, Version 83 oder höher, standardmäßig verfügbar und aktiviert.  
*   [Anpassen von Tastenkombinationen][DevtoolsCustomKeyboardShortcuts] ist jetzt in Microsoft Edge, Version 86 oder höher, standardmäßig verfügbar und aktiviert.  

## Bereitstellen von Feedback zu experimentellen Features  

Sie können Feedback zu Microsoft Edge devtools-Experimenten oder zu allem anderen, was mit devtools zu tun hat.  

*   Senden Sie Ihr Feedback über das Symbol " **Feedback senden** " im devtools  
*   Tweet bei [@EdgeDevTools][TwitterEdgedevtools]  

:::image type="complex" source="./media/bing-devtools-send-feedback.msft.png" alt-text="Das Symbol "Feedback senden" in Microsoft Edge devtools" lightbox="./media/bing-devtools-send-feedback.msft.png":::
   Das Symbol " **Feedback senden** " in Microsoft Edge devtools  
:::image-end:::  

<!--  
## Getting in touch with the Microsoft Edge DevTools team  

[!INCLUDE [contact DevTools team note](./includes/contact-devtools-team-note.md)]  
-->  

<!-- image links -->  

[ImageRotateIcon]: ./media/rotate-dark-icon.msft.png  
[ImageSpanIcon]: ./media/span-dark-icon.msft.png  
[ImageExperimentalApisIcon]: ./media/experimental-apis-dark-icon.msft.png  

<!-- links -->  

[Devtools3dViewIndex]: ./3d-view/index.md "3D-Ansicht | Microsoft docs"  
[DevToolsCustomizeSettings]: ./customize/index.md#settings "Einstellungen – anpassen von Microsoft Edge devtools | Microsoft docs"  
[DevtoolsDeviceModeIndexSimulateMobileViewport]: ./device-mode/index.md#simulate-a-mobile-viewport "Simulieren von mobilen Geräten mit dem Gerätemodus in Microsoft Edge devtools | Microsoft Edge"  
[DevtoolsIssues]: ./issues/index.md "Suchen und Beheben von Problemen mit dem Microsoft Edge devtools Issues Tool | Microsoft docs"  
[DevToolsShortcuts]: ./shortcuts.md "Microsoft Edge devtools-Tastenkombinationen | Microsoft docs"  
[DevtoolsOpen]: ./open.md "Öffnen Sie Microsoft Edge devtools | Microsoft docs"  
[DevtoolsCustomKeyboardShortcuts]: ./customize/shortcuts.md "Anpassen von Tastenkombinationen in Microsoft Edge devtools | Microsoft docs"

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
