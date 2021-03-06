---
description: Erfahren Sie mit den F12 Developer Tools, wie Sie das Hintergrundskript, Inhaltsskripts und Erweiterungsseiten einer Erweiterung debuggen.
title: Debuggen | Erweiterungen
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/03/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: edge, web development, html, javascript, developer, debug, debugging
ms.custom: seodec18
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: a23c7558080cca7671cdfc9790705a8d8c9ed705
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "11399365"
---
# <a name="debugging-extensions"></a>Debugging von Erweiterungen  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

Sie können Ihre Erweiterungen in Microsoft Edge mithilfe von F12 Developer Tools debuggen.  

Im folgenden Video wird eine fehlerhafte Microsoft Edge-Erweiterung durch die einzelnen Debuggingszenarien gestreamt und auf dem Weg nach oben gefixt.  Weitere Informationen finden Sie in den schrittweisen Anweisungen unten.  

> [!VIDEO https://channel9.msdn.com/Blogs/One-Dev-Minute/Debugging-Microsoft-Edge-Extensions/player]  

> [!NOTE]
> Um das Erweiterungsdebuggen mit F12 nutzen zu können, müssen Sie zuerst Entwicklerfeatures in "about:flags" aktivieren.  Weitere [Informationen dazu finden Sie unter](./adding-and-removing-extensions.md) Hinzufügen und Entfernen von Erweiterungen.  

## <a name="background-script-debugging"></a>Debuggen von Hintergrundskripts  

So starten Sie das Debuggen des Hintergrundskripts Ihrer Erweiterung:  

1.  Klicken Sie auf **Weitere (...)** gefolgt von **Erweiterungen,** um in den Erweiterungsbereich zu wechseln.  
    
    ![Schaltfläche "Mehr"](../media/morebutton.png)  
    
1.  Klicken Sie auf die Erweiterung, die Sie debuggen möchten.  
1.  Klicken Sie auf den **Link Hintergrundseite,** um F12 für den Hintergrundprozess zu öffnen.  
    
    ![Ausgewählte Erweiterungsansicht von Optionen mit Link "Überprüfen"](../media/debug-inspect.png)  
    
1.  Wählen Sie **die Registerkarte Debugger** in F12 aus.  
1.  Navigieren Sie zum Hintergrundskript Ihrer Erweiterung, und wählen Sie es aus.  
1.  Platzieren Sie Haltepunkte für das Debuggen, indem Sie links von der Quellcodezeile klicken.  
    
    ![f12-Konsole mit Hintergrundskript mit Unterbrechungspunkten](../media/debug-f12-background.png)  
    
1.  Wählen Sie die **Registerkarte Konsole** aus, und führen Sie den Befehl `location.reload()` aus.  Dadurch wird das Hintergrundskript erneut ausgeführt, sodass Sie ihren Code schrittweise ausführen können.  
    
    ![Konsole mit eingegebener location.reload](../media/debug-f12-background-console.png)  
    
## <a name="content-script-debugging"></a>Debuggen von Inhaltsskripts  

So starten Sie das Debuggen des Inhaltsskripts Ihrer Erweiterung:  

1.  Starten Sie F12, indem Sie entweder zur Schaltfläche **Mehr (...)** navigieren und **F12 Developer Tools** auswählen oder die Tastatur `F12` drücken.  
1.  Navigieren Sie zum Inhaltsskript Ihrer Erweiterung, und wählen Sie es aus.  Inhaltsskripts für derzeit ausgeführte Erweiterungen werden von einem anderen Ordner für jede Erweiterung dargestellt.  
    
    > [!NOTE]
    > Es werden nur ausgeführte Inhaltsskripts angezeigt.  
    
1.  Platzieren Sie Haltepunkte für das Debuggen, indem Sie links von der Quellcodezeile klicken.  
    
    ![f12 mit Debuggen des Inhaltsskripts](../media/debug-content-f12.png)  
    
1.  Aktualisieren Sie die Browserregisterkarte, um mit dem Schritt durch den Code zu beginnen.  
    
## <a name="extension-page-debugging"></a>Debuggen von Erweiterungsseiten  

Es gibt zwei Methoden, die für den Zugriff auf den Quellcode Ihrer Erweiterungsseite zum Debuggen verwendet werden können.  Eine Methode gilt für eine Vielzahl von Seiten, die andere nur für Popupseiten.  

### <a name="debugging-any-extension-page"></a>Debuggen einer beliebigen Erweiterungsseite  

Die folgende Methode funktioniert für alle Erweiterungsseiten wie die Optionsseite und Popups:  

1.  Klicken Sie mit der rechten Maustaste auf den Hintergrund Ihrer Seite.  
1.  Wählen **Sie Quelle anzeigen aus.**  
    
    ![Öffnen des Popupdebu debuggings mit f12](../media/debug-popup-select.png)  
    
1.  Nachdem F12 geöffnet wurde, platzieren Sie Haltepunkte in der Datei, die Sie debuggen möchten.  
    
    ![Popupdebu debugging mit f12](../media/debug-popup-f12.png)  
    
1.  Wählen Sie die **Registerkarte Konsole** aus, und führen Sie den Befehl `location.reload()` aus.  Dadurch wird das Seitenskript erneut ausgeführt, sodass Sie ihren Code schrittweise ausführen können.  
    
    ![Konsole mit eingegebener location.reload](../media/debug-f12-background-console.png)  
    
### <a name="debugging-a-popup-extension-page"></a>Debuggen einer Popuperweiterungsseite  

Die Methode zum Debuggen von Erweiterungsseiten gilt zwar auch für Popuperweiterungsseiten, die folgenden Schritte beschreiben jedoch eine weitere Möglichkeit zum Debuggen Ihres Popups:  

1.  Klicken Sie mit der rechten Maustaste auf das Symbol Ihrer Erweiterung.  
1.  Wählen **Sie Popup überprüfen aus.**  
    
    ![Überprüfen des Popupdebuggers](../media/debug-popup-inspect.png)  
    
1.  Führen Sie die Schritte 3 und 4 oben aus, um Haltepunkte zu platzieren und das Popup neu zu laden.  
    