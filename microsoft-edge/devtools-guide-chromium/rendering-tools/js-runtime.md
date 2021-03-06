---
description: Identifizieren Sie teure Funktionen mithilfe des Microsoft Edge DevTools-Speicherbereichs.
title: Beschleunigen der JavaScript-Laufzeit
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, Entwicklungstools
ms.openlocfilehash: 682001ae8d265b342e5d6e0725f9f8ac4e298cf8
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "11397601"
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

# <a name="speed-up-javascript-runtime"></a>Beschleunigen der JavaScript-Laufzeit  

Identifizieren Sie teure Funktionen mithilfe des **Speicherbereichs.**  

:::image type="complex" source="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-heavy-bottom-up.msft.png" alt-text="Beispielprofile" lightbox="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-heavy-bottom-up.msft.png":::
   Beispielprofile  
:::image-end:::  

### <a name="summary"></a>Zusammenfassung  

*   Zeichnen Sie genau auf, welche Funktionen aufgerufen wurden und wie viel Arbeitsspeicher die einzelnen Funktionen mit Demokation Sampling im **Speicherbereich** benötigen.  
*   Visualisieren Sie Ihre Profile als Flammendiagramm.  
    
## <a name="record-a-sampling-profile"></a>Aufzeichnen eines Samplingprofils  

Wenn Sie jank in Ihrem JavaScript bemerken, erfassen Sie ein Samplingprofil.  Samplingprofile zeigen an, wo die Laufzeit für Funktionen auf Ihrer Seite verwendet wird.  

1.  Navigieren Sie zum **Speicherbereich** von DevTools.  
1.  Wählen Sie das **Optionsfeld Zuweisungsstichprobe** aus.  
1.  Wählen Sie **Start**aus.  
1.  Je nachdem, was Sie analysieren möchten, können Sie entweder die Seite aktualisieren, mit der Seite interagieren oder einfach die Seite ausführen lassen.  
1.  Wählen Sie die **Schaltfläche** Beenden aus, wenn Sie fertig sind.  
    
> [!NOTE]
> Sie können auch die [Console Utilities-API verwenden,][DevtoolsConsoleUtilities] um Profile über die Befehlszeile zu aufzeichnen und zu gruppieren.  

## <a name="view-sampling-profile"></a>Anzeigen des Samplingprofils  

Wenn Sie die Aufzeichnung abgeschlossen haben, **** füllt DevTools automatisch den Speicherbereich unter **SAMPLING PROFILES** mit den Daten aus Ihrer Aufzeichnung auf.  

Die Standardansicht ist **Heavy \(Bottom Up\)**.  In dieser Ansicht können Sie überprüfen, welche Funktionen die Leistung am stärksten beeinträchtigen, und den anfordernden Pfad für jede Funktion untersuchen.  

### <a name="change-sort-order"></a>Sortierreihenfolge ändern  

Wenn Sie die Sortierreihenfolge ändern möchten, wählen Sie das Dropdownmenü neben dem Symbol für ausgewählte Fokusfunktion **\(** ausgewählte Funktion im Fokus \) aus, und wählen Sie dann eine der ![ ][ImageFocusIcon] folgenden Optionen aus.

**Diagramm**.  Zeigt ein chronologisches Diagramm der Aufzeichnung an.  

:::image type="complex" source="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart.msft.png" alt-text="Flammendiagramm" lightbox="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart.msft.png":::
   Flammendiagramm  
:::image-end:::  

**Heavy \(Bottom Up\)**.  Listet Funktionen nach Auswirkungen auf die Leistung auf und ermöglicht es Ihnen, die aufrufenden Pfade zu den Funktionen zu untersuchen.  Dies ist die Standardansicht.  

:::image type="complex" source="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-heavy-bottom-up.msft.png" alt-text="Schweres Diagramm" lightbox="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-heavy-bottom-up.msft.png":::
   Schweres Diagramm  
:::image-end:::  

**Struktur \(Top Down\)**.  Zeigt ein Gesamtbild der Anrufstruktur, beginnend am oberen Rand der Aufrufliste.  

:::image type="complex" source="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-tree-top-down.msft.png" alt-text="Strukturdiagramm" lightbox="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-tree-top-down.msft.png":::
   Strukturdiagramm  
:::image-end:::  

### <a name="exclude-functions"></a>Ausschließen von Funktionen  

Um eine Funktion aus Dem Samplingprofil auszuschließen, wählen Sie sie aus, und wählen Sie dann die Schaltfläche ausgewählte Funktion **ausschließen** \( ausgewählte Funktion ![ ausschließen ][ImageExcludeIcon] \) aus.  Die anfordernde Funktion \(parent\) der ausgeschlossenen Funktion \(child\) wird mit dem zugewiesenen Arbeitsspeicher belastet, der der ausgeschlossenen Funktion \(child\) zugewiesen ist.  

Wählen Sie **die Schaltfläche Alle Funktionen wiederherstellen** \( Alle Funktionen ![ wiederherstellen \) aus, um alle ausgeschlossenen Funktionen wieder in der ][ImageRestoreIcon] Aufzeichnung wiederherzustellen.  

## <a name="view-sampling-profile-as-chart"></a>Anzeigen des Samplingprofils als Diagramm  

Die Diagrammansicht bietet eine visuelle Darstellung des Samplingprofils im Laufe der Zeit.  

Nachdem Sie [ein Samplingprofil aufgezeichnet haben,](#record-a-sampling-profile)zeigen Sie die Aufzeichnung als Flammendiagramm an, indem Sie [die Sortierreihenfolge in](#change-sort-order) Diagramm **ändern.**  

:::image type="complex" source="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart.msft.png" alt-text="Flammendiagrammansicht" lightbox="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart.msft.png":::
   Flammendiagrammansicht  
:::image-end:::  

Das Flammendiagramm ist in zwei Teile unterteilt.  

| index | Bestandteil | Beschreibung |  
| --- |:--- |:--- |  
| 1 | Übersicht | Eine Vogel-Augen-Ansicht der gesamten Aufzeichnung.  Die Höhe der Balken entspricht der Tiefe der Aufrufliste.  Je höher die Leiste, desto tiefer die Aufrufliste.  |  
| 2 | Anrufstapel | Dies ist eine detaillierte Ansicht der Funktionen, die während der Aufzeichnung aufgerufen wurden.  Die horizontale Achse ist Zeit und vertikale Achse ist die Aufrufliste.  Die Stapel sind von oben nach unten organisiert.  Die Funktion oben hat also die darunter genannte aufgerufen, und so weiter.  |  

Funktionen werden nach dem Zufallsprinzip gefärbt.  Es besteht keine Korrelation mit den Farben, die in den anderen Panels verwendet werden.  Funktionen sind jedoch bei Aufrufen immer gleich gefärbt, sodass Sie Muster in jeder Laufzeit beobachten können.  

:::image type="complex" source="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart-highlighted.msft.png" alt-text="Mit Anmerkungen versehenes Flammendiagramm" lightbox="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart-highlighted.msft.png":::
   Mit Anmerkungen versehenes Flammendiagramm  
:::image-end:::  

Eine hohe Aufrufliste ist nicht unbedingt wichtig, sondern bedeutet lediglich, dass viele Funktionen aufgerufen wurden.  Ein breiter Balken bedeutet jedoch, dass eine Funktion lange ge dauern hat, bis sie abgeschlossen wurde.  Dies sind Kandidaten für die Optimierung.  

### <a name="zoom-in-on-specific-parts-of-recording"></a>Vergrößern bestimmter Teile der Aufzeichnung  

Wählen, halten und ziehen Sie die Maus nach links und rechts über die Übersicht, um bestimmte Teile der Anrufliste zu vergrößern.  Nach dem Zoomen zeigt die Aufrufliste automatisch den von Ihnen ausgewählten Teil der Aufzeichnung an.  

:::image type="complex" source="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart-zoomed.msft.png" alt-text="Diagramm verkleinert" lightbox="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart-zoomed.msft.png":::
   Diagramm verkleinert  
:::image-end:::  

### <a name="view-function-details"></a>Anzeigen von Funktionsdetails  

Wählen Sie eine Funktion aus, um die Definition im Bereich **Quellen anzeigen** zu können.  

Zeigen Sie auf eine Funktion, um den Namen und die Zeitdaten anzeigen.  Die folgenden Informationen werden bereitgestellt.  

| Detail | Beschreibung |  
|:--- |:--- |  
| **Name** | Der Name der Funktion.  |  
| **Self size** | Die Größe des aktuellen Aufrufs der Funktion, einschließlich nur der Anweisungen in der Funktion.  |  
| **Gesamtgröße** | Die Größe des aktuellen Aufrufs dieser Funktion und aller von ihr aufgerufenen Funktionen.  |  
| **URL** | Die Position der Funktionsdefinition in Form von where ist der Name der Datei, in der die Funktion definiert ist, und die `base.js:261` `base.js` `261` Zeilennummer der Definition.  |  
<!--*   **Aggregated self time**.  Aggregate time for all invocations of the function across the recording, not including functions called by this function.  -->  
<!--*   **Aggregated total time**.  Aggregate total time for all invocations of the function, including functions called by this function.  -->  
<!--*   **Not optimized**.  If the profiler has detected a potential optimization for the function it lists it here.  -->  

:::image type="complex" source="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart-hover.msft.png" alt-text="Anzeigen von Funktionsdetails im Diagramm" lightbox="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart-hover.msft.png":::
   Anzeigen von Funktionsdetails im Diagramm  
:::image-end:::  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageExcludeIcon]: ../media/exclude-icon.msft.png  
[ImageFocusIcon]: ../media/focus-icon.msft.png  
[ImageRestoreIcon]: ../media/restore-icon.msft.png  

<!-- links -->  

[DevtoolsConsoleUtilities]: ../console/utilities.md "Api-Referenz für Konsolenprogramme | Microsoft Docs"  
[DevtoolsConsoleUtilitiesProfile]: ../console/utilities.md#profile "profile – Apireferenz für Konsolenprogramme | Microsoft Docs"  
[DevtoolsConsoleUtilitiesProfileEnd]: ../console/utilities.md#profileend "profileEnd – Api-Referenz für Konsolenprogramme | Microsoft Docs"  

> [!NOTE]
> Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.  
> Die ursprüngliche Seite [](https://developers.google.com/web/tools/chrome-devtools/rendering-tools/js-execution) befindet sich hier und wird von [Kayce Basken][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\) und [Meggin Kearney][MegginKearney] \(Tech Writer\) verfasst.  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[MegginKearney]: https://developers.google.com/web/resources/contributors/megginkearney  
