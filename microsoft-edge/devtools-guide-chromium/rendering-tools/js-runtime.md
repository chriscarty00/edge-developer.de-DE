---
title: Beschleunigen der JavaScript-Laufzeit
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/30/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Web-Entwicklung, F12-Tools, devtools
ms.openlocfilehash: 0e198be3e1cef53590a24bfaa2382746ced299ed
ms.sourcegitcommit: 0342d99bf8d3212068890bab0e1e960afa507c02
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/30/2020
ms.locfileid: "10611871"
---
<!-- Copyright Kayce Basques and Meggin Kearney

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License. -->





# Beschleunigen der JavaScript-Laufzeit   




Ermitteln Sie mit dem **Speicher** Panel kostspielige Funktionen.  

> ##### Abbildung1  
> Sampling-profile  
> ![Sampling-profile][ImageCpuProfile]  

### Zusammenfassung  

*   Zeichnen Sie genau auf, welche Funktionen aufgerufen wurden und wie viel Arbeitsspeicher für die Zuweisungs Stichproben im **Speicher** Panel erforderlich ist.  
*   Visualisieren Sie Ihre Profile als Flammen Diagramm.  

## Aufzeichnen eines Stichproben Profils  

Wenn Sie Jank in Ihrem JavaScript bemerken, erfassen Sie ein Sampling-Profil.  Sampling-Profile zeigen an, wo die Laufzeit für Funktionen auf der Seite aufgewendet wird.  

1.  Wechseln Sie zum **Speicher** Panel von devtools.  
1.  Aktivieren Sie das Optionsfeld **Zuweisungs Sampling** .  
1.  Wählen Sie **Start**.  
1.  Je nachdem, was Sie analysieren möchten, können Sie entweder die Seite neu laden, mit der Seite interagieren oder einfach die Seite ausführen lassen.  
1.  Wählen Sie die Schaltfläche **Beenden** aus, wenn Sie den Vorgang beendet haben.  

> [!NOTE]
> Sie können auch die API für die [Konsolen Dienstprogramme][DevtoolsConsoleUtilities] zum Aufzeichnen und Gruppieren von Profilen über die Befehlszeile verwenden.  

## Sampling-Profil anzeigen  

Wenn Sie die Aufzeichnung abgeschlossen haben, füllt devtools den **Speicher** Panel automatisch unter **Sampling-profile** mit den Daten aus ihrer Aufzeichnung auf.  

Die Standardansicht ist **schwer. \ (Bottom up \)**.  In dieser Ansicht können Sie sehen, welche Funktionen die meisten Auswirkungen auf die Leistung haben, und die Aufruf Pfade für diese Funktionen untersuchen.  

### Ändern der Sortierreihenfolge   

Wenn Sie die Sortierreihenfolge ändern möchten, wählen Sie das Dropdownmenü **neben dem Fokus ausgewählte Funktions** Symbol ausgewählte Funktion aus, ![ ][ImageFocusIcon] und wählen Sie dann eine der folgenden Optionen aus.

**Diagramm**aus.  Zeigt ein chronologisches Diagramm der Aufzeichnung an.  

> ##### Abbildung2  
> Flamm Diagramm  
> ![Flamm Diagramm][ImageFlameChart]  

**Heavy \ (Bottom up \)**.  Listet Funktionen nach Auswirkungen auf die Leistung auf und ermöglicht Ihnen, die Aufruf Pfade zu den Funktionen zu untersuchen.  Dies ist die Standardansicht.  

> ##### Abbildung 3  
> Schweres Diagramm  
> ![Schweres Diagramm][ImageHeavyChart]  

**Struktur \ (oben)**  Zeigt ein Gesamtbild der aufrufenden Struktur, beginnend am oberen Rand der Aufrufliste.  

> ##### Abbildung4  
> Strukturdiagramm  
> ![Strukturdiagramm][ImageTreeChart]  

### Ausschließen von Funktionen   

Wenn Sie eine Funktion aus Ihrem Stichproben Profil ausschließen möchten, wählen Sie Sie aus, um Sie zu markieren, und wählen Sie dann das Symbol ausgewählte **Funktion ausschließen aus** ![ ][ImageExcludeIcon] .  Die anfordernde Funktion \ (übergeordnete \) der ausgeschlossenen Funktion \ (untergeordnete \) wird mit dem zugewiesenen Arbeitsspeicher belastet, der der ausgeschlossenen Funktion zugeordnet ist (untergeordnete \).  

Wählen Sie **das Symbol alle Funktionen** wiederherstellen alle Funktionen wiederherstellen aus ![ ][ImageRestoreIcon] , um alle ausgeschlossenen Funktionen wieder in die Aufzeichnung zurückzusetzen.  

## Sampling-Profil als Diagramm anzeigen   

Die Diagrammansicht bietet eine visuelle Darstellung des Sampling-Profils über einen Zeitraum.  

Nachdem Sie [ein Stichproben Profil aufgezeichnet](#record-a-sampling-profile)haben, zeigen Sie die Aufzeichnung als Flammen Diagramm an, indem Sie [die Sortierreihenfolge](#change-sort-order) in **Diagramm**ändern.  

> ##### Abbildung5  
> Ansicht "Flammen Diagramm"  
> ![Ansicht "Flammen Diagramm"][ImageFlameChartView]  

Das Flammen Diagramm ist in zwei Teile aufgeteilt.  

| | Bestandteil | Beschreibung |  
| --- |:--- |:--- |  
| 1 | Übersicht | Eine Vogelperspektive der gesamten Aufzeichnung  Die Höhe der Balken entspricht der Tiefe der Aufrufliste.  Je höher die Leiste, desto tiefer die Aufrufliste.  |  
| 2 | Anruflisten | Hierbei handelt es sich um eine detaillierte Ansicht der Funktionen, die während der Aufzeichnung aufgerufen wurden.  Die horizontale Achse ist Zeit, und die vertikale Achse ist die Aufrufliste.  Die Stapel werden oben nach unten angeordnet.  So nennt sich die Funktion oben die untere und so weiter.  |  

Funktionen werden nach dem Zufallsprinzip eingefärbt.  Es gibt keine Korrelation zu den in den anderen Bereichen verwendeten Farben.  Funktionen werden allerdings immer gleich über Aufrufe eingefärbt, sodass Sie in jeder Laufzeit Muster sehen können.  

> ##### Abbildung6  
> Flamm Diagramm mit Anmerkungen  
> ![Flamm Diagramm mit Anmerkungen][ImageAnnotatedFlameChart]  

Eine hohe Aufrufliste ist nicht unbedingt wichtig, Sie bedeutet nur, dass viele Funktionen aufgerufen wurden.  Eine breite Leiste bedeutet aber, dass eine Funktion lange Zeit in Anspruch genommen hat.  Diese sind Kandidaten für die Optimierung.  

### Vergrößern bestimmter Teile der Aufzeichnung   

Wählen, halten und ziehen Sie die Maus nach links und rechts über die Übersicht, um bestimmte Teile der Anrufliste zu vergrößern.  Nachdem Sie die Ansicht gezoomt haben, wird in der Aufrufliste automatisch der Teil der Aufzeichnung angezeigt, den Sie ausgewählt haben.  

> ##### Abbildung7  
> Diagramm vergrößert  
> ![Diagramm vergrößert][ImageFlameChartZoomed]  

### Anzeigen von Funktionsdetails   

Wählen Sie eine Funktion aus, um die Definition im **Quellen** Panel anzuzeigen.  

Zeigen Sie mit der Maus auf eine Funktion, um die Namen-und Anzeigedauer Daten anzuzeigen.  Die folgenden Informationen werden bereitgestellt.  

| Detail | Beschreibung |  
|:--- |:--- |  
| **Name** | Der Name der Funktion.  |  
| **Selbst Größe** | Die Größe des aktuellen Aufrufs der Funktion, einschließlich nur der Anweisungen in der Funktion.  |  
| **Gesamtgröße** | Die Größe des aktuellen Aufrufs dieser Funktion und der von ihr aufgerufenen Funktionen.  |  
| **URL** | Die Position der Funktionsdefinition in Form von `base.js:261` Where `base.js` ist der Name der Datei, in der die Funktion definiert ist, und `261` die Nummer der Zeile der Definition.  |  
<!--*   **Aggregated self time**.  Aggregate time for all invocations of the function across the recording, not including functions called by this function.  -->  
<!--*   **Aggregated total time**.  Aggregate total time for all invocations of the function, including functions called by this function.  -->  
<!--*   **Not optimized**.  If the profiler has detected a potential optimization for the function it lists it here.  -->  

> ##### Abbildung8  
> Anzeigen von Funktionsdetails in einem Diagramm  
> ![Anzeigen von Funktionsdetails in einem Diagramm][ImageFunctionsDetails]  

<!--## Feedback   -->  



<!-- image links -->  

[ImageExcludeIcon]: /microsoft-edge/devtools-guide-chromium/media/exclude-icon.msft.png  
[ImageFocusIcon]: /microsoft-edge/devtools-guide-chromium/media/images/focus-icon.msft.png  
[ImageRestoreIcon]: /microsoft-edge/devtools-guide-chromium/media/images/restore-icon.msft.png  

[ImageCpuProfile]: /microsoft-edge/devtools-guide-chromium/media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-heavy-bottom-up.msft.png "Abbildung 1: Sampling-profile"  
[ImageFlameChart]: /microsoft-edge/devtools-guide-chromium/media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart.msft.png "Abbildung 2: Flammen Diagramm"  
[ImageHeavyChart]: /microsoft-edge/devtools-guide-chromium/media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-heavy-bottom-up.msft.png "Abbildung 3: schweres Diagramm"  
[ImageTreeChart]: /microsoft-edge/devtools-guide-chromium/media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-tree-top-down.msft.png "Abbildung 4: Strukturdiagramm"  
[ImageFlameChartView]: /microsoft-edge/devtools-guide-chromium/media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart.msft.png "Abbildung 5: Ansicht "Flammen Diagramm""  
[ImageAnnotatedFlameChart]: /microsoft-edge/devtools-guide-chromium/media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart-highlighted.msft.png "Abbildung 6: kommentiertes Flammen Diagramm"  
[ImageFlameChartZoomed]: /microsoft-edge/devtools-guide-chromium/media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart-zoomed.msft.png "Abbildung 7: Diagramm vergrößert"  
[ImageFunctionsDetails]: /microsoft-edge/devtools-guide-chromium/media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart-hover.msft.png "Abbildung 8: Anzeigen von Funktionsdetails in einem Diagramm"  

<!-- links -->  

[DevtoolsConsoleUtilities]: /microsoft-edge/devtools-guide-chromium/console/utilities "API-Referenz für Konsolen Dienstprogramme"  
[DevtoolsConsoleUtilitiesProfile]: /microsoft-edge/devtools-guide-chromium/console/utilities#profile "API-Referenz für Profil-Console-Utilities"  
[DevtoolsConsoleUtilitiesProfileEnd]: /microsoft-edge/devtools-guide-chromium/console/utilities#profileend "API-Referenz zu profileEnd-Console Utilities"  

> [!NOTE]
> Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.  
> Die ursprüngliche Seite wird [hier](https://developers.google.com/web/tools/chrome-devtools/rendering-tools/js-execution) gefunden und von [Kayce Basken][KayceBasques] (Technical Writer, Chrome devtools & Lighthouse \) und [Meggin Kearney][MegginKearney] \ (Tech Writer \) erstellt.  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[MegginKearney]: https://developers.google.com/web/resources/contributors/megginkearney  
