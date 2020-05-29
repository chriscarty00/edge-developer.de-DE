---
description: Verwenden Sie das Konsolen Tool für interaktives Debuggen und Ad-hoc-Tests.
title: DevTools-Console
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/15/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Web Development, F12 Tools, devtools, Console
ms.custom: seodec18
ms.openlocfilehash: f2733cac57ed5f2364747ee64e669fa83aae41f4
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10567646"
---
# Console

Das Konsolen Entwicklertool in Microsoft Edge protokolliert Informationen, die einer Webseite zugeordnet sind, wie JavaScript, Netzwerkanforderungen und Sicherheitsfehler. Sie können die Konsole für interaktives Debuggen und Ad-hoc-Tests verwenden. 

Zum Öffnen des Konsolentools in Microsoft Edge drücken Sie die Taste F12, um auf das Entwicklertool Fenster zuzugreifen (oder klicken Sie mit der rechten Maustaste auf die Seite, und wählen Sie dann **Element überprüfen**aus) aus. Wählen Sie dann oben im Fenster die Registerkarte **Konsole** aus. 

Sie können auch das Konsolen Tool verwenden, um zu und von einer ausgeführten Webseite zu kommunizieren. Sie können die Konsole für folgende Zwecke verwenden:

- Posten Sie Standard [Fehler-und Statuscodes](./console/error-and-status-codes.md) sowie Informationsmeldungen, während der Code ausgeführt wird.
- Generieren Sie benutzerdefinierte Debug-Protokolle über die [Konsolen-API-](./console/console-api.md) Aufrufe, die Sie in Ihren Code einbeziehen.
- Stellen Sie eine [Befehlszeile](./console/command-line.md) und eine interaktive Strukturansicht zum Überprüfen der aktuellen Rückgabewerte von Schlüsselvariablen und Funktionen bereit.

## Teile der Konsole

Die folgende Abbildung zeigt die wichtigsten Elemente der Konsole:

![Die Microsoft Edge devtools-Konsole](./media/console.png)

1. **Fehlermeldungen**  /  **Warnungen**  /  Weitere **Informationen**  /  Schaltflächen für **Protokolle** : Filtern der Konsolenausgabe nach dem angegebenen Typ Sie können Schaltflächen mehrfach auswählen, indem Sie die **STRG** -Taste gedrückt halten. Die Schaltfläche **alle** löscht alle Filter.

2. Schaltfläche " **Löschen** " (**STRG + L**): die Schaltfläche " **Löschen** " löscht die aktuelle Konsolenanzeige.

3. Kontrollkästchen " **Protokoll beibehalten** ": durch Aktivieren des Kontrollkästchens **Protokoll beibehalten** wird die Konsolenausgabe während der Seitenaktualisierung und dem Schließen und erneuten Öffnen von devtools beibehalten. Der Konsolen Verlauf wird nur gelöscht, wenn die Registerkarte geschlossen ist, oder Sie können die Konsole manuell löschen.

4. **Ziel**: Verwenden Sie das Dropdownmenü **Ziel** , um zu einem anderen Ausführungskontext zu wechseln, beispielsweise `<iframe>` in einer Seite oder in einer ausgeführten Erweiterung. Standardmäßig ist der Frame auf oberster Ebene der Seite ausgewählt. Wenn Sie auf einen markierten Frame zeigen, wird eine QuickInfo mit der vollständigen URL für diese Ressource angezeigt.

5. **Konsole anzeigen**  /  Schaltfläche " **Konsole ausblenden** " (**STRG** +  **&grave;** ): Zusätzlich zum Konsolenbereich können Sie die Konsole vom unteren Rand eines anderen devtools-Panels aus verwenden, **Show Console**indem Sie die  /  Schaltfläche Konsole**Ausblenden** Console anzeigen drücken. Die Schaltfläche hat keine Auswirkungen, wenn devtools im Konsolen Panel geöffnet ist.
 
6. **Filter Protokolle** (**STRG + F**): Sie können auch Protokolle filtern, indem Sie eine bestimmte Textzeichenfolge im Suchfeld verwenden.

7. **Debugger**: Wählen Sie einen beliebigen blauen Quell Link aus, um den devtools-Debugger für diese bestimmte Codezeile zu öffnen, um Sie zu überprüfen.

## Kombinationen

Aktion                                            | Tastenkombination               
:-------------------------------------------------| :----------------------
Starten von devtools mit Konsole im Fokus             | **STRG**  +  **UMSCHALT**  +  **J** 
Wechseln zur Konsole                                 | **STRG**  +  **2**           
Anzeigen/Ausblenden der Konsole auf einer anderen devtools-Registerkarte       | **Ctrl**  +  STRG **&grave;** (zurück markieren)  
Ausführen (Befehl mit einer Zeile)                     | **Eingabe**                
Zeilenumbruch ohne Ausführung (mehrzeiligen Befehl) | **UMSCHALT**  +  **EINGABETASTE oder** **STRG**  +  **Enter** -Taste      
Deaktivieren der Konsole aller Nachrichten                 | **STRG**  +  **L**           
Filtern von Protokollen (Fokus auf Suchfeld setzen)             | **STRG**  +  **F**           
Vorschlag zur automatischen Vervollständigung annehmen (im Fokus) | **EINGABETASTE** oder **Tab**       
Vorheriger/Nächster Vorschlag zur automatischen Vervollständigung          | Nach- **oben-Taste** / **Nach-unten-Taste**   


