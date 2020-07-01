---
description: Die neuesten experimentellen Features in Microsoft Edge devtools
title: Experimentelle Features
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/26/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Web-Entwicklung, F12-Tools, devtools, Experiment
ms.openlocfilehash: 731a289f555870eeff9cdc160965b59925b70c4d
ms.sourcegitcommit: 0048eb692d49eab4755c0c3ef6866e6a9122d579
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/01/2020
ms.locfileid: "10843950"
---
# Experimentelle Features  

Sie können die experimentellen Features, die noch in der Entwicklung sind, in der Microsoft Edge-devtools verwenden, um zu testen und [Feedback bereitzustellen](#providing-feedback-on-experimental-features) , bevor diese im allgemeinen veröffentlicht werden.  

Während experimentelle Features in allen Kanälen von Microsoft Edge verfügbar sind, erhalten Sie möglicherweise die neuesten experimentellen Features mithilfe des Canary-Kanals von Microsoft Edge.  

## Aktivieren von experimentellen Features  

Führen Sie die folgenden Schritte aus, um die experimentellen Features von \ (oder Off \) in Microsoft Edge zu aktivieren.  

1.  [Öffnen Sie devtools][DevtoolsOpen].  
     *   Drücken Sie `Control` + `Shift` + `I` \ (Windows \) oder `Command` + `Option` + `I` \ (macOS \).  Weitere Informationen finden Sie unter [Tastenkombinationen für Microsoft Edge devtools][DevToolsShortcuts].  
1.  Öffnen Sie den Bereich " **Einstellungen** ".  
    *   Drücken Sie `Shift` + `?` .  Weitere Informationen finden Sie unter [Tastenkombinationen für Microsoft Edge devtools][DevToolsShortcuts].  
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
| [Debuggen von neuen CSS-Raster Features aktivieren](#enable-new-css-grid-debugging-features) | 85 oder höher |  
| [Aktivieren der Unterstützung für das Verschieben von Tabstopps zwischen Bereichen](#enable-support-to-move-tabs-between-panels) | 85 oder höher |  
| [Webhint aktivieren](#enable-webhint) | 85 oder höher |  

### Debuggen von neuen CSS-Raster Features aktivieren  

Verbessert die on-page-Visualisierungen, wenn Sie Websites mit CSS-Rasterlayouts Debuggen.  Sie können die Overlays in den devtools-Einstellungen weiter anpassen.  

:::image type="complex" source="./media/experiments-grid.png" alt-text="CSS-Raster Debugging-Feature" lightbox="./media/experiments-grid.png":::
   CSS-Raster Debugging-Feature  
:::image-end:::  

<!--Available in Microsoft Edge version 85 and later.  -->  

### Aktivieren der Unterstützung für das Verschieben von Tabstopps zwischen Bereichen  

In der Regel können Tools, wie **Elemente** und **Netzwerke** , nur im Hauptbereich \ (oben \) von devtools geöffnet werden.  Auf ähnliche Weise können Tools wie **3D-Ansicht** und **Probleme** nur im Bereich "drawer \ (unten \)" von devtools geöffnet werden.  Wenn dieses Experiment ausgewählt ist, können Sie die Tools zwischen dem oberen und unteren Bereich verschieben, indem Sie auf die Registerkarte zeigen, das Kontextmenü öffnen (Klicken Sie mit der rechten Maustaste auf \), und wählen Sie **nach oben** oder **nach unten**verschieben aus.   Mit diesem Experiment können Sie Ihr devtools-Layout anpassen.  Wenn Sie den unteren Bereich ein-oder ausblenden möchten, drücken Sie `Escape` .  

:::image type="complex" source="./media/experiments-move-panels.png" alt-text="Verschieben von Tabstopps zwischen Bereichen" lightbox="./media/experiments-move-panels.png":::
   Verschieben von Tabstopps zwischen Bereichen  
:::image-end:::  

<!--Available in Microsoft Edge version 85 and later.  -->  

### Webhint aktivieren  

[webhint][WebhintMain] ist ein Open-Source-Tool, das in Echtzeit Feedback zur Barrierefreiheit, browserübergreifenden Kompatibilität, Sicherheit, Leistung, PWAs und anderen gängigen Webentwicklungs Problemen von Websites bietet.  Dieses Experiment führt das webhint-Feedback in devtools im Bereich [Probleme][DevtoolsIssues] .  Sie können das Problem auswählen, um die Dokumentation zur Behebung des Problems und eine Liste der betroffenen Ressourcen auf Ihrer Website anzuzeigen.  Wählen Sie einen Ressourcen Link aus, um den entsprechenden Bereich für **Netzwerke**, **Quellen**oder **Elemente** in devtools zu öffnen.  

:::image type="complex" source="./media/experiments-webhint.png" alt-text="webhint-Feedback im Bereich "Probleme"" lightbox="./media/experiments-webhint.png":::
   webhint-Feedback im Bereich "Probleme"  
:::image-end:::      

<!--Available in Microsoft Edge version 85 and later.  -->  

## Frühere experimentelle Features  

*   die [3D-Ansicht][Devtools3DView] ist jetzt in Microsoft Edge, Version 83 oder höher, standardmäßig verfügbar und aktiviert.  

## Bereitstellen von Feedback zu experimentellen Features  

So geben Sie Feedback zu Microsoft Edge devtools-Experimenten oder zu allem anderen devtools:  

*   Senden Sie Ihr Feedback über das Feedback-Symbol im devtools  
*   Tweet bei [@EdgeDevTools][TwitterEdgedevtools]  

:::image type="complex" source="./media/devtools-feedback.png" alt-text="Symbol "Feedback" im Microsoft Edge-devtools" lightbox="./media/devtools-feedback.png":::
   Symbol "Feedback" im Microsoft Edge-devtools  
:::image-end:::  

<!-- links -->  

[Devtools3DView]: ./3D-view.md "3D-Ansicht | Microsoft docs"  
[DevtoolsIssues]: ./issues/index.md "Suchen und Beheben von Problemen mit dem Microsoft Edge devtools Issues Tool | Microsoft docs"  
[DevToolsShortcuts]: ./shortcuts.md "Microsoft Edge devtools-Tastenkombinationen – Microsoft docs"  
[DevtoolsOpen]: ./open.md "Öffnen Sie Microsoft Edge devtools | Microsoft docs"  

[TwitterEdgedevtools]: https://www.twitter.com/EdgeDevTools "Microsoft Edge-devtools | Twitter"  

[WebhintMain]: https://webhint.io "webhint" 
