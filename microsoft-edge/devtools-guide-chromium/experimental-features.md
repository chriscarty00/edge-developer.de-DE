---
description: Die neuesten experimentellen Features in Microsoft Edge devtools
title: Experimentelle Funktionen
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/25/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Web-Entwicklung, F12-Tools, devtools, Experiment
ms.openlocfilehash: 4915c909921bb4c5eaa8d727ab7a08493b941445
ms.sourcegitcommit: b88d2a55a59db8373ff2bac275d3730977bf19c9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/01/2020
ms.locfileid: "10986122"
---
# Experimentelle Funktionen  

Sie können die experimentellen Features, die noch in der Entwicklung sind, in der Microsoft Edge-devtools verwenden, um zu testen und [Feedback bereitzustellen](#providing-feedback-on-experimental-features) , bevor diese im allgemeinen veröffentlicht werden.  

Während experimentelle Features in allen Kanälen von Microsoft Edge verfügbar sind, erhalten Sie möglicherweise die neuesten experimentellen Features mithilfe des Canary-Kanals von Microsoft Edge.  

## Aktivieren von experimentellen Features  

Führen Sie die folgenden Schritte aus, um die experimentellen Features von \ (oder Off \) in Microsoft Edge zu aktivieren.  

1.  [Öffnen Sie devtools][DevtoolsOpen].  
     *   Wählen Sie `Control` + `Shift` + `I` \ (Windows \) oder `Command` + `Option` + `I` \ (macOS \) aus.  Weitere Informationen finden Sie unter [Tastenkombinationen für Microsoft Edge devtools][DevToolsShortcuts].  
1.  Öffnen Sie den Bereich " [Einstellungen][DevToolsCustomizeSettings] ".  
    *   Wählen Sie aus `Shift` + `?` .  Weitere Informationen finden Sie unter [Tastenkombinationen für Microsoft Edge devtools][DevToolsShortcuts].  
1.  Wählen Sie auf der linken Seite des Bereichs **Einstellungen** den Abschnitt **Experimente** aus.  
    
    :::image type="complex" source="./media/experiments-devtools.png" alt-text="Liste der Experimente in den devtools-Einstellungen" lightbox="./media/experiments-devtools.png":::
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
| [Aktivieren der Registerkarte "Benutzerdefinierte Tastenkombinationen"](#enable-custom-keyboard-shortcuts-settings-tab) | 84 oder höher |
| [Debuggen von neuen CSS-Raster Features aktivieren](#enable-new-css-grid-debugging-features) | 85 oder höher |  
| [Aktivieren der Unterstützung für das Verschieben von Tabstopps zwischen Bereichen](#enable-support-to-move-tabs-between-panels) | 85 oder höher |  
| [Webhint aktivieren](#enable-webhint) | 85 oder höher |  
| [Aktivieren der Netzwerk Konsole](#enable-network-console) | 85 oder höher |  
| [Quellauftrags Anzeige aktivieren](#enable-source-order-viewer) | 86 oder höher |  

### Aktivieren der Registerkarte "Benutzerdefinierte Tastenkombinationen"  

Stellt eine neue **Verknüpfungs** Seite in [devtools-Einstellungen][DevToolsCustomizeSettings] bereit, die das Zuordnen von [Tastenkombinationen][DevToolsShortcuts] im devtools zu [Microsoft Visual Studio-Code][VisualstudioCode]ermöglicht.  

Nachdem Sie das Experiment aktiviert haben, öffnen Sie die [devtools-Einstellungen][DevToolsCustomizeSettings] mithilfe von SELECT erneut `Shift` + `?` .  Navigieren Sie zur Seite neue **Verknüpfungen** .  Wählen Sie im Dropdownmenü **Tastenkombinationen von Voreinstellungen** **devtools (Standard)** aus, und wählen Sie **Visual Studio-Code**aus.  Die Tastenkombinationen im devtools entsprechen nun den Tastenkombinationen für entsprechende Aktionen in Visual Studio-Code.  

:::image type="complex" source="./media/experiments-keyboard-shortcut.png" alt-text="Zuordnen von Tastenkombinationen im devtools zu Visual Studio-Code" lightbox="./media/experiments-keyboard-shortcut.png":::
   Zuordnen von Tastenkombinationen im devtools zu Visual Studio-Code  
:::image-end:::  

Unter Windows wird beispielsweise die Tastenkombination zum Anhalten oder Fortsetzen der Ausführung eines Skripts in [Visual Studio-Code][VisualstudioCodeShortcutsKeyboardWindows] bereitgestellt `F5` .  Mit der **devtools (Standardeinstellung)** ist die gleiche Verknüpfung in der devtools `F8` .  Mit der **Visual Studio-Code** Vorgabe ist auch die Verknüpfung `F5` .  

### Debuggen von neuen CSS-Raster Features aktivieren  

Verbessert die on-page-Visualisierungen, wenn Sie Websites mit CSS-Rasterlayouts Debuggen.  Sie können die Overlays in den devtools-Einstellungen weiter anpassen.  

:::image type="complex" source="./media/experiments-grid.png" alt-text="CSS-Raster Debugging-Feature" lightbox="./media/experiments-grid.png":::
   CSS-Raster Debugging-Feature  
:::image-end:::  

<!--Available in Microsoft Edge version 85 and later.  -->  

### Aktivieren der Unterstützung für das Verschieben von Tabstopps zwischen Bereichen  

In der Regel können Tools, wie **Elemente** und **Netzwerke** , nur im Hauptbereich \ (oben \) von devtools geöffnet werden.  Auf ähnliche Weise können Tools wie **3D-Ansicht** und **Probleme** nur im Bereich "drawer \ (unten \)" von devtools geöffnet werden.  Wenn Sie das Experiment auswählen, können Sie die Tools zwischen dem oberen und unteren Bereich verschieben, indem Sie auf die Registerkarte zeigen, das Kontextmenü öffnen (Klicken Sie mit der rechten Maustaste auf \), und wählen Sie **nach oben** oder **nach unten**verschieben aus.   Mit diesem Experiment können Sie Ihr devtools-Layout anpassen.  Wenn Sie den unteren Bereich ein-oder ausblenden möchten, wählen Sie aus `Escape` .  

:::image type="complex" source="./media/experiments-move-panels.png" alt-text="Verschieben von Tabstopps zwischen Bereichen" lightbox="./media/experiments-move-panels.png":::
   Verschieben von Tabstopps zwischen Bereichen  
:::image-end:::  

<!--Available in Microsoft Edge version 85 and later.  -->  

### Webhint aktivieren  

[webhint][WebhintMain] ist ein Open-Source-Tool, das in Echtzeit Feedback zur Barrierefreiheit, browserübergreifenden Kompatibilität, Sicherheit, Leistung, PWAs und anderen gängigen Webentwicklungs Problemen von Websites bietet.  Das [webhint-Experiment führt][WebhintMain] das webhint-Feedback in devtools im Bereich [Probleme][DevtoolsIssues] .  Sie können das Problem auswählen, um die Dokumentation zur Behebung des Problems und eine Liste der betroffenen Ressourcen auf Ihrer Website anzuzeigen.  Wählen Sie einen Ressourcen Link aus, um den entsprechenden Bereich für **Netzwerke**, **Quellen**oder **Elemente** in devtools zu öffnen.  

:::image type="complex" source="./media/experiments-webhint.png" alt-text="webhint-Feedback im Bereich "Probleme"" lightbox="./media/experiments-webhint.png":::
   webhint-Feedback im Bereich " **Probleme** "  
:::image-end:::  

<!--Available in Microsoft Edge version 85 and later.  -->  

### Aktivieren der Netzwerk Konsole  

**Netzwerk Konsole** ist der Arbeitstitel eines Experiments, um synthetische Netzwerkanforderungen über HTTP zu stellen.  Sie können das **Netzwerkkonsolen** Experiment verwenden, um Web-API-Anforderungen zu senden.  

Nachdem Sie das Experiment aktiviert haben, stellen Sie sicher, dass Sie das devtools erneut starten.  So verwenden Sie die Netzwerk Konsole:  

1.  Öffnen Sie den Bereich **Netzwerk** .  
1.  Suchen Sie die Netzwerkanforderung, die Sie ändern möchten, und senden Sie Sie erneut.  
1.  Öffnen Sie das Kontextmenü \ (Klicken Sie mit der rechten Maustaste auf \), und wählen Sie **Bearbeiten und wiedergeben**aus.  
1.  Wenn die **Netzwerk Konsole** geöffnet wird, bearbeiten Sie die Netzwerk Anforderungsinformationen.  
1.  Wählen Sie **senden**aus.  

:::image type="complex" source="./media/network-network-console.png" alt-text="Netzwerk Konsole im Konsolen Einzug" lightbox="./media/network-network-console.png":::
   **Netzwerk Konsole** im **Konsolen** Einzug  
:::image-end:::  

<!--Available in Microsoft Edge version 85 and later.  --> 

### Quellauftrags Anzeige aktivieren  

Die **Ansicht "Quellreihenfolge** " ist der Arbeitstitel eines Experiments, um die Reihenfolge der Elemente in der Seitenquelle anzuzeigen.  Sie können das Experiment der **Quellauftrags Anzeige** verwenden, um Barrierefreiheitsprobleme in Ihren Seiten zu finden, da sich die Anzeigereihenfolge auf dem Bildschirm von der Reihenfolge der Quelle unterscheiden kann, die die Benutzer der Bildschirmsprachausgabe verwirrt.  

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

## Bereitstellen von Feedback zu experimentellen Features  

Sie können Feedback zu Microsoft Edge devtools-Experimenten oder zu allem anderen, was mit devtools zu tun hat.  

*   Senden Sie Ihr Feedback über das Symbol " **Feedback senden** " im devtools  
*   Tweet bei [@EdgeDevTools][TwitterEdgedevtools]   

:::image type="complex" source="./media/bing-devtools-send-feedback.msft.png" alt-text="Das Symbol "Feedback senden" im Microsoft Edge-devtools" lightbox="./media/bing-devtools-send-feedback.msft.png":::
   Das Symbol " **Feedback senden** " in Microsoft Edge devtools  
:::image-end:::  

<!-- links -->  

[Devtools3dViewIndex]: ./3d-view/index.md "3D-Ansicht | Microsoft docs"  
[DevtoolsIssues]: ./issues/index.md "Suchen und Beheben von Problemen mit dem Microsoft Edge devtools Issues Tool | Microsoft docs"  
[DevToolsCustomizeSettings]: ./customize/index.md#settings "Einstellungen – anpassen von Microsoft Edge devtools | Microsoft docs"  
[DevToolsShortcuts]: ./shortcuts.md "Microsoft Edge devtools-Tastenkombinationen | Microsoft docs"  
[DevtoolsOpen]: ./open.md "Öffnen Sie Microsoft Edge devtools | Microsoft docs"  

[TwitterEdgedevtools]: https://www.twitter.com/EdgeDevTools "Microsoft Edge-devtools | Twitter"  

[VisualstudioCode]: https://code.visualstudio.com "Microsoft Visual Studio-Code"  
[VisualstudioCodeShortcutsKeyboardWindows]: https://code.visualstudio.com/shortcuts/keyboard-shortcuts-windows.pdf "Visual Studio-Code Tastenkombinationen für Windows | Microsoft Visual Studio-Code"  

[WebhintMain]: https://webhint.io "webhint" 
