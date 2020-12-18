---
description: Verwenden Sie den Speicher-Panel, um
title: DevTools – Arbeitsspeicher
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Web-Entwicklung, F12-Tools, devtools, Arbeitsspeicher, Heap, GC, Garbage Collection, Aufbewahrungs Größe, dominierer
ms.custom: seodec18
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 5ad284f8072cc296743299ec9c4fb2037f8fd883
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233676"
---
# Arbeitsspeicher

Verwenden Sie den **Speicher** Panel, um ihre Verwendung von Systemressourcen zu messen und Heap-Snapshots in verschiedenen Zuständen der Codeausführung zu vergleichen. Damit haben Sie folgende Möglichkeiten:

- Zeichnen Sie [den Speicherverbrauch Ihrer Seite in Echtzeit ab](#memory-usage-timeline) , und nehmen Sie Schnappschüsse des Heaps auf
- [Ermitteln potenzieller Arbeitsspeicherprobleme](#snapshot-summary) in Ihrem Code, beispielsweise aufbewahrte Objekte, die nicht an das DOM angefügt sind
- [Überprüfen von Speicher Nutzungsdaten](#snapshot-details) nach Objekttyp, instanzenanzahl, Größe und verweisen, um Probleme zu isolieren
- [Anwenden von Snapshot-Daten filtern](#filters) , um das Rauschen nicht umsetzbar Informationen zu verringern
- [Ermitteln der Speicherkosten für ein bestimmtes Objekt](#object-references) und die Verweise, die es beibehalten
- Untersuchen Sie [den Heap in verschiedenen Phasen der Untersuchung](#snapshot-comparison) , um die Quelle von Speicherverlusten und anderen Problemen zu ermitteln.

![Der Microsoft Edge devtools-Speicher Panel](./media/memory.png)


## Symbolleiste

1. **Starten/Beenden der Profilerstellungssitzung (STRG + E)**: Wenn Sie den Profiler aktivieren, können Sie die Speicherauslastung nachvollziehen und Snapshots des Heaps aufnehmen.
2. **Profilerstellungssitzung importieren (STRG + O)**: Laden Sie eine gespeicherte devtools-Speicherdiagnose Sitzung.
3. **Profilerstellungssitzung exportieren (STRG + S)**: Speichern Sie die aktuelle Diagnosesitzung auf dem Datenträger.
4. Erstellen eines **Heap-Snapshots (STRG + UMSCHALT + T)**: Aufzeichnen der aktuellen Speicherzuweisungen für einen bestimmten Zeitpunkt.


## Speicher Auslastungs Zeitachse

Speicherprobleme können ein Hauptverursacher von Leistungsproblemen sein, was dazu führt, dass Ihre Seite zunehmend nicht mehr reagiert und im Laufe der zeitverzögert wird.

Der erste Schritt bei der Analyse der Speichernutzung Ihrer Seite besteht darin, [eine Profilerstellungssitzung zu starten](#toolbar) , um vor/nach-Snapshots des Heaps zu erstellen, während Sie die Schritte zum Aufblasen des Arbeitsspeichers oder einen vermuteten Speicherverlust durchführen.

Wenn Sie den Speicher Profiler starten, wird ein Prozess Speicher Diagramm angezeigt, in dem Sie den gesamten privaten Arbeitssatz (die Menge des von der Seite verbrauchten Arbeitsspeichers) über einen Zeitraum beobachten können. Im Arbeitsspeicher Diagramm wird eine Live Ansicht des Arbeitsspeichers der Registerkarte angezeigt, die private Bytes, systemeigenen Speicher und den JavaScript-Heap umfasst. 

![Speicher Auslastungs Zeitachse](./media/memory_timeline.png)

 Das Diagramm zeigt den speichertrend für die Seite an, mit dem Sie beurteilen können, wann [ein Heap-Schnappschuss für einen](#toolbar) späteren Vergleich geeignet ist, beispielsweise wenn Sie Zeiträume mit unerwarteter Speicher Aufbewahrung sehen.

### Performance. Mark ()

Sie können der Zeitachse benutzerdefinierte **Benutzermarkierungen** hinzufügen, um wichtige Ereignisse im Verlauf der Analysesitzung zu identifizieren, indem Sie die [`Performance.mark()`](https://developer.mozilla.org/docs/Web/API/Performance/mark) Methode im Code oder in der devtools- [**Konsole**](./console.md)aufrufen.

### Console. takeheapSnapshot ()

Manchmal müssen Sie Schnappschüsse zu sehr bestimmten Zeitpunkten aufnehmen, beispielsweise unmittelbar vor einer großen Mutation des DOM. In diesen Fällen können Sie Schnappschüsse programmgesteuert mit ausführen [`Console.takeHeapSnapshot()`](./console/console-api.md#taking-heap-snapshots) .

## Zusammenfassung der Momentaufnahme

Wenn Sie [einen Schnappschuss](#toolbar) erstellen, wird eine Zusammenfassungs Kachel generiert, die die Größe des JavaScript-Heaps zum Zeitpunkt des Schnappschusses sowie die Anzahl der zugewiesenen Objekte und einen Screenshot der Seite angibt. Sie können jederzeit während der Ausführung des Benutzerszenarios, in dem eine Analyse erforderlich ist, Snapshots aufnehmen. Die Snapshots generieren zusätzliche Kacheln, die jeweils den Unterschied im JavaScript-Speicher aus dem vorherigen Snapshot angeben.

![Heap-Snapshot](./media/memory_snapshot.png)

Durch Klicken auf die Werte in der Zusammenfassungs Kachel wechseln Sie zu dem Bereich, in dem [Details zu den Momentaufnahme Daten](#snapshot-details)angezeigt werden. Potenzielle [Speicherprobleme werden](#snapshot-details) mit einem blauen Informationssymbol ("i") angezeigt.

## Details zur Momentaufnahme

Die Daten im *Momentaufnahme* Bereich zeigen die von Ihrer Seite erstellten Objekte zusammen mit allen von JavaScript-Frameworks zugewiesenen Arbeitsspeichers, die Sie möglicherweise verwenden.

![Snapshot-Detailtabelle](./media/memory_details.png)

Die drei Registerkarten stellen unterschiedliche Ansichten der Daten dar:

#### Typen

Zeigt die Anzahl der Instanzen und die Gesamtgröße von Objekten im Heap, gruppiert nach Objekttyp. Standardmäßig werden diese nach instanzenanzahl sortiert.

Wenn Sie ein Objekt im Bereich obere *Typen* auswählen, werden in der Tabelle [Objektverweise](#object-references) im unteren Bereich alle Objekte aufgelistet, die auf das Objekt verweisen.

#### Wurzeln

Zeigt eine hierarchische Ansicht der untergeordneten Bezüge an, um zu beschreiben, wie Objekte zum globalen Objekt verwurzelt sind, wodurch verhindert wird, dass Sie von der Garbage Collection erfasst werden.

Standardmäßig werden die untergeordneten Knoten nach der Spalte mit der Beibehaltungs Größe sortiert, wobei der größte oben ist.

#### Dominators

Zeigt eine Liste der Objekte auf dem Heap, die exklusive Bezüge zu anderen Objekten aufweisen. Die dominierer werden nach Beibehaltungs Größe sortiert, um die Objekte anzugeben, die den meisten Speicher verbrauchen, die möglicherweise am einfachsten zu befreien sind.

Hier erfahren Sie, wie Sie die Spalten in den Ansichten *Typen, Stämme* und *Dominanzen* interpretieren:

Spalte | Beschreibung
:------------ | :-------------
Kennung (en) | Der Name, der das Objekt am besten identifiziert. Bei HTML-Elementen zeigt die momentaufnahmedetails beispielsweise den ID-Attributwert an, wenn eine verwendet wird.
Typ | Objekttyp (beispielsweise *HTMLDivElement*).
Size | Objektgröße, ohne die Größe von referenzierten Objekten.
Beibehaltungs Größe | Objektgröße plus die Größe aller untergeordneten Objekte, die keine anderen übergeordneten Elemente aufweisen. Für praktische Zwecke ist dies die Größe des vom Objekt aufbewahrten Arbeitsspeichers, wenn Sie also das Objekt löschen, wird die angegebene Speichermenge zurückgefordert.
Anzahl | Die Anzahl der Objektinstanzen. Dieser Wert wird nur in der Ansicht Typen angezeigt.

Wenn Sie ein Objekt im Bereich obere *Dominanz* auswählen, werden in der Tabelle [Objektverweise](#object-references) im unteren Bereich alle Objekte aufgelistet, die auf das Objekt verweisen.

### Filter

Sie können die Daten in der Tabelle mit den folgenden Schritten weiter anpassen:

![Filtern nach integrierten und Objekt-IDs](./media/memory_filter.png)

1. **Kennzeichnungs Filter**: Filtern von Daten durchsuchen nach einer bestimmten Objektkennung
2. **Gruppieren nach Dominator**: nur Objekte mit *exklusiven* Bezügen auf andere Objekte werden in der Ansicht der obersten Ebene der Objekte angezeigt (Dies ist die Standardansicht auf der Registerkarte " *Herrscher* ").
3. **Integrierter/IDs-Filter**: Standardmäßig sind [JavaScript-integrierte Objekte](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects) in der Liste enthalten. Das Auflisten von Objekt-IDs kann hilfreich sein, wenn mehrere anonyme Objekte unterschieden werden müssen.

Die Ansichten *Typen, Stämme* und *Dominanzen* verfügen jeweils über einen eigenen Filter, sodass der Filter nicht beibehalten wird, wenn Sie zu einer anderen Ansicht wechseln.

### Objekt Bezüge

In den Ansichten [**Typen**](#types) und [**Dominanzen**](#dominators) enthält der untere Bereich eine **Objektverweis** Liste, in der freigegebene Verweise angezeigt werden. Wenn Sie ein Objekt im oberen Bereich auswählen, werden in dieser Liste alle Objekte angezeigt, die auf das Objekt verweisen, also die Objekte, die das ausgewählte Objekt am Leben erhalten.

Zirkelbezüge werden mit einem Sternchen (*) und Informations ToolTip angezeigt und können nicht erweitert werden. Andernfalls verhindern Sie, dass Sie die Referenzstruktur hinauflaufen und Objekte identifizieren, die Speicher erhalten.

Um gleichwertige Objekte schnell zu identifizieren, markieren Sie die Option " [*Objekt-IDs anzeigen*](#filters) ", um Objekt-IDs neben Objektnamen in der Spalte " *Identifier (s)* " anzuzeigen. Objekte mit der gleichen ID sind freigegebene Verweise.

### Snapshot-Vergleich

Durch Klicken auf die [Registerkarte "Snapshot-Vergleich"](#snapshot-details) oder den Vergleichs Link auf der [Kachel "Snapshot-Zusammenfassung](#snapshot-summary)  " wird ein Unterschied zwischen den beiden Schnappschüssen angezeigt. Im Vergleichsbereich bieten die Vorwahlen *, Typen* und *Stamm* Ansichten dieselben Snapshot- [*Details*](#snapshot-details) , die Sie für einzelne Schnappschüsse sehen würden, mit den folgenden zusätzlichen Werten:

Spalte | Beschreibung
:------------ | :-------------
Größenunterschied. | Unterschied zwischen der Größe des Objekts im aktuellen Snapshot und seiner Größe im vorherigen Snapshot, ohne die Größe von referenzierten Objekten.
Unterschiede bei der Beibehaltungs Größe | Unterschied zwischen der aufbewahrten Größe des Objekts im aktuellen Snapshot und der Beibehaltungs Größe im vorherigen Schnappschuss. Die Beibehaltungs Größe umfasst die Objektgröße plus die Größe aller untergeordneten Objekte, die keine anderen übergeordneten Elemente aufweisen. Für praktische Zwecke ist die Größe des Speichers, der vom Objekt aufbewahrt wird, also, wenn Sie das Objekt löschen, das Sie den angegebenen Arbeitsspeicher zurückfordern.

Sie können die Dropdownliste **Bereichs** verwenden, um differenzielle Informationen zwischen Snapshots zu filtern:

![Bereichsfilter für Snapshot-Vergleiche](./media/memory_comparison_scope_filter.png)

- <strong>Objekte, die von "Snapshot #" übrig <number></strong> sind, zeigt die Differenz zwischen den Objekten, die dem Heap hinzugefügt wurden, und aus dem Heap vom Basisplan zum vorherigen Snapshot entfernt. Wenn beispielsweise in der Zusammenfassung der Momentaufnahme <em> + 205/-195 </em> in der Objektanzahl angezeigt wird, werden in diesem Filter die zehn Objekte angezeigt, die hinzugefügt, aber nicht entfernt wurden.

- <strong>Zwischen Snapshot # und #: hinzugefügte Objekte <number> <number></strong> zeigt alle Objekte, die dem Heap aus dem vorherigen Snapshot hinzugefügt wurden.

- <strong>Alle Objekte in Snapshot # <number></strong> : zeigt alle Objekte auf dem Heap an (also eine <em> ungefilterte </em> Ansicht).

Standardmäßig wird der Filter *nicht übereinstimmende Bezüge anzeigen* auf die Vergleichsansicht angewendet, um Objekt Bezüge anzugeben, die dem aktuellen Bereichsfilter nicht entsprechen. Sie können es über das Dropdown-Menü deaktivieren:

![Filter für nicht übereinstimmende Bezüge für Snapshot-Vergleiche](./media/memory_comparison_matching_filter.png)


## Tastenkombinationen

 Aktion | Tastenkombination
:------------ | :-------------
Starten/Beenden der Profilerstellungssitzung  | `Ctrl` + `E`
Profilerstellungssitzung importieren | `Ctrl` + `O`
Profilerstellungssitzung exportieren | `Ctrl` + `S`
Snapshot des Heaps aufnehmen | `Ctrl` + `Shift` + `T`

## Bekannte Probleme

### Beim Starten der Profilerstellungssitzung ist ein Fehler aufgetreten.

Wenn diese Fehlermeldung angezeigt wird: **beim Starten der Profilerstellungssitzung im Speicher Tool ist ein Fehler aufgetreten** , führen Sie die folgenden Schritte aus, um eine Problemumgehung zu erhalten.

1. Drücken Sie `Windows Key`  +  `R` .

2. Geben Sie im Dialogfeld Ausführen den **Dienst "Services. msc**" ein.
![Bekannte Probleme-1](./media/known_issues_1.PNG)

3. Suchen Sie den **Microsoft (R) Diagnostics Hub Standard-Kollektor Dienst** , und klicken Sie mit der rechten Maustaste darauf.
![Bekannte Probleme-2](./media/known_issues_2.PNG)

4. Starten Sie den **Microsoft (R) Diagnostics Hub Standard-Kollektor Dienst**erneut.
![Bekannte Probleme-3](./media/known_issues_3.PNG)

5. Schließen Sie die Microsoft Edge-Entwickler Tools und die Registerkarte. Öffnen Sie eine neue Registerkarte, navigieren Sie zu Ihrer Seite, und drücken Sie `F12` .

6. Sie sollten jetzt in der Lage sein, mit der Profilerstellung zu beginnen. 
![Bekannte Probleme-4](./media/known_issues_4-memory.PNG)

Gibt es immer noch Probleme? Senden Sie uns Ihr Feedback über das Symbol **Feedback senden** ! 

![Bekannte Probleme-5](./media/known_issues_5.PNG)
