---
description: In den F12-Entwickler Tools erfahren Sie, wie Sie das Hintergrundskript einer Erweiterung, Inhalts Skripts und Erweiterungsseiten Debuggen.
title: Erweiterungen – Debuggen
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/16/2019
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, Web-Entwicklung, HTML, JavaScript, Entwickler, Debuggen, Debuggen
ms.custom: seodec18
ms.openlocfilehash: 34488870cb4e4a92a9d57859509ce7d1176cf284
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10567435"
---
# Debugging von Erweiterungen  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

Sie können Ihre Erweiterungen in Microsoft Edge mithilfe der F12-Entwickler Tools debuggen.

Das folgende Video durchläuft eine fehlerhafte Microsoft-Edge-Erweiterung, wobei jedes Debugging-Szenario durchlaufen und auf dem Weg repariert werden kann. Weitere Informationen finden Sie in den folgenden schrittweisen Anleitungen.

> [!VIDEO https://channel9.msdn.com/Blogs/One-Dev-Minute/Debugging-Microsoft-Edge-Extensions/player]


> [!NOTE]
> Um das Erweiterungs Debuggen mit F12 zu nutzen, müssen Sie zuerst die Entwicklerfeatures in about: Flags aktivieren. Weitere Informationen hierzu finden Sie unter [Hinzufügen und Entfernen von Erweiterungen](./adding-and-removing-extensions.md) .


## Debuggen von Hintergrund Skripten
So beginnen Sie mit dem Debuggen des hintergrundskripts ihrer Erweiterung:

1. Klicken Sie auf **mehr (...)** gefolgt von **Erweiterungen** , um in den Erweiterungsbereich zu wechseln.  
 ![Schaltfläche "Mehr"](./../media/morebutton.png)
2. Klicken Sie auf die Erweiterung, die Sie debuggen möchten.
3. Klicken Sie auf den Link " **Hintergrundseite** ", um F12 für den Hintergrundprozess aufzurufen.  
 ![ausgewählte Erweiterungs Ansicht der Optionen mit dem Link "überprüfen"](./../media/debug-inspect.png)
4. Wählen Sie die Registerkarte **Debugger** in F12 aus.
5. Navigieren Sie zu dem Hintergrundskript ihrer Erweiterung, und wählen Sie es aus.
6. Platzieren Sie Haltepunkte für das Debuggen, indem Sie links neben der Quellcodezeile klicken.  
 ![F12-Konsole mit Hintergrundskript mit Unterbrechungspunkten](./../media/debug-f12-background.png)
7. Wählen Sie die Registerkarte **Konsole** aus, und führen Sie den Befehl " `location.reload()` " aus. Dadurch wird das Hintergrundskript erneut ausgeführt, sodass Sie den Code schrittweise durchlaufen können.  
 ![Konsole mit dem Eintrag "Location. Reload"](./../media/debug-f12-background-console.png)


## Debuggen von Inhalts Skripts
So beginnen Sie mit dem Debuggen des Inhalts Skripts ihrer Erweiterung:

1. Starten Sie F12, indem Sie entweder zur Schaltfläche **mehr (.** ..) navigieren und **"F12-Entwickler Tools"** auswählen oder auf der Tastatur F12 drücken.
2. Navigieren Sie zu dem Inhalts Skript ihrer Erweiterung, und wählen Sie es aus. Inhalts Skripts für zurzeit ausgeführte Erweiterungen werden für jede Erweiterung in einem anderen Ordner dargestellt.

    > [!NOTE]
    > Es werden nur ausgeführte Inhalts Skripts angezeigt.

3. Platzieren Sie Haltepunkte für das Debuggen, indem Sie links neben der Quellcodezeile klicken.  
 ![F12, wenn das Inhalts Skript gedebuggt wird](./../media/debug-content-f12.png)
4. Aktualisieren Sie die Registerkarte Browser, um mit der schrittweisen Ausführung des Codes zu beginnen.




## Debuggen von Erweiterungsseiten

Es gibt zwei Methoden, die für den Zugriff auf den Quellcode der Erweiterungsseite zum Debuggen verwendet werden können. Eine Methode gilt für eine Vielzahl von Seiten, während die andere nur für Popup Seiten verwendet werden kann.

### Debuggen einer beliebigen Erweiterungsseite
Die folgende Methode funktioniert für alle Erweiterungsseiten wie die Seite "Optionen" und Popups:


1. Klicken Sie mit der rechten Maustaste auf den Hintergrund der Seite.
2. Wählen Sie **"Quelle anzeigen"** aus.

   ![Popup Debuggen mit F12](./../media/debug-popup-select.png)

3. Sobald F12 geöffnet wird, platzieren Sie Haltepunkte in der Datei, die Sie debuggen möchten.

   ![Popup Debuggen mit F12](./../media/debug-popup-f12.png)
4. Wählen Sie die Registerkarte **Konsole** aus, und führen Sie den Befehl aus `location.reload()` . Dadurch wird das Seitenskript erneut ausgeführt, sodass Sie den Code schrittweise durchlaufen können.  

   ![Konsole mit dem Eintrag "Location. Reload"](./../media/debug-f12-background-console.png)

### Debuggen einer Popup Erweiterungsseite
Die Methode zum Debuggen von Erweiterungsseiten gilt zwar auch für Popup Erweiterungsseiten, doch mit den folgenden Schritten wird eine weitere Möglichkeit zum Debuggen des Popups skizziert:

1. Klicken Sie mit der rechten Maustaste auf das Symbol der Erweiterung.
2. Wählen Sie **"Popup inspizieren"** aus.

   ![Popup-Debug-Prüfung](./../media/debug-popup-inspect.png)
3. Führen Sie die Schritte 3 und 4 für die Platzierung von Haltepunkten und das erneute Laden des Popups aus.
