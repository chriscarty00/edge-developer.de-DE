---
description: Ein Verweis auf alle Möglichkeiten zum Aufzeichnen und Analysieren der Leistung in Microsoft Edge DevTools.
title: Referenz zur Leistungsanalyse
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/08/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, Entwicklungstools
ms.openlocfilehash: e7774dc0aab647b8cf2bf47699368fafe6c21d70
ms.sourcegitcommit: 4b9fb5c1176fdaa5e3c60af2b84e38d5bb86cd81
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/16/2021
ms.locfileid: "11439689"
---
<!-- Copyright Kayce Basques 

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->  

# <a name="performance-analysis-reference"></a>Referenz zur Leistungsanalyse  

Diese Seite ist eine umfassende Referenz zu Microsoft Edge DevTools-Features im Zusammenhang mit der Leistungsanalyse.  

Navigieren Sie [zu Erste Schritte mit der Analyse der Laufzeitleistung][DevtoolsEvaluatePerformanceGettingStarted] für ein geführtes Lernprogramm zum Analysieren der Leistung einer Seite mithilfe von Microsoft Edge [DevTools][MicrosoftEdgeDevTools].  

## <a name="record-performance"></a>Aufzeichnen der Leistung  

### <a name="record-runtime-performance"></a>Aufzeichnen der Laufzeitleistung  

Zeichnen Sie die Laufzeitleistung auf, wenn Sie die Leistung einer Seite während der Ausführung analysieren möchten, statt zu laden.  

1.  Navigieren Sie zu der Seite, die Sie analysieren möchten.  
1.  Öffnen Sie **das Tool Leistung** in DevTools.  
1.  Wählen **Sie Datensatz** \( ![ Datensatzsymbol ](../media/record-icon.msft.png) \).  
    
    :::image type="complex" source="../media/evaluate-performance-performance-record-highlight.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-performance-record-highlight.msft.png":::
       **Record**  
    :::image-end:::  
    
1.  Interagieren mit der Seite.  DevTools zeichnet alle Seitenaktivitäten auf, die als Ergebnis Ihrer Interaktionen auftreten.  
1.  Wählen **Sie erneut Aufzeichnen** aus, oder wählen Sie Beenden **aus,** um die Aufzeichnung zu beenden.  
    
### <a name="record-load-performance"></a>Aufzeichnen der Lastleistung  

Zeichnen Sie die Lastleistung auf, wenn Sie die Leistung einer Seite beim Laden analysieren möchten, statt sie zu ausführen.  

1.  Navigieren Sie zu der Seite, die Sie analysieren möchten.  
1.  Öffnen Sie **den Bereich** Leistung von DevTools.  
1.  Wählen **Sie Seite aktualisieren** \( Seite aktualisieren ![ ](../media/refresh-page-icon.msft.png) \).  DevTools zeichnet Leistungsmetriken auf, während die Seite aktualisiert wird, und beendet dann die Aufzeichnung ein paar Sekunden nach Abschluss der Last automatisch.  
    
    :::image type="complex" source="../media/evaluate-performance-performance-refresh-button.msft.png" alt-text="Seite aktualisieren" lightbox="../media/evaluate-performance-performance-refresh-button.msft.png":::
       **Seite aktualisieren**  
    :::image-end:::  
    
DevTools vergrößert automatisch den Teil der Aufzeichnung, in dem der Großteil der Aktivität aufgetreten ist.  

:::image type="complex" source="../media/evaluate-performance-performance-refreshed.msft.png" alt-text="Eine Aufzeichnung zum Laden von Seiten" lightbox="../media/evaluate-performance-performance-refreshed.msft.png":::
   Eine Aufzeichnung zum Laden von Seiten  
:::image-end:::  

### <a name="capture-screenshots-while-recording"></a>Aufnehmen von Screenshots während der Aufzeichnung  

Aktivieren Sie das **Kontrollkästchen Screenshots,** um einen Screenshot jedes Frames während der Aufzeichnung zu erfassen.  

:::image type="complex" source="../media/evaluate-performance-performance-capture-screenshots-checkbox.msft.png" alt-text="Das Kontrollkästchen Screenshots" lightbox="../media/evaluate-performance-performance-capture-screenshots-checkbox.msft.png":::
   Das **Kontrollkästchen Screenshots**  
:::image-end:::  

Navigieren Sie zu [Screenshot anzeigen,](#view-a-screenshot) um zu erfahren, wie Sie mit Screenshots interagieren.  

### <a name="force-garbage-collection-while-recording"></a>Erzwingen der Garbage Collection während der Aufzeichnung  

Wählen Sie beim Aufzeichnen einer Seite die Option Garbage **sammeln** \( Garbage Icon sammeln \) aus, ![ um die Garbage Collection zu ](../media/collect-garbage-icon.msft.png) erzwingen.  

:::image type="complex" source="../media/evaluate-performance-performance-collect-garbage-button.msft.png" alt-text="Sammeln von Garbage" lightbox="../media/evaluate-performance-performance-collect-garbage-button.msft.png":::
   Sammeln von Garbage  
:::image-end:::  

### <a name="show-recording-settings"></a>Anzeigen von Aufzeichnungseinstellungen  

Wählen **Sie Aufnahmeeinstellungen** \( Aufnahmeeinstellungen \) aus, um weitere Einstellungen im Zusammenhang mit der Erfassung von Leistungsaufzeichnungen durch ![ ](../media/capture-settings-icon.msft.png) DevTools verfügbar zu machen.  

:::image type="complex" source="../media/evaluate-performance-performance-capture-settings-button-open-drawer.msft.png" alt-text="Abschnitt "Aufnahmeeinstellungen"" lightbox="../media/evaluate-performance-performance-capture-settings-button-open-drawer.msft.png":::
   Abschnitt **"Aufnahmeeinstellungen"**  
:::image-end:::  

### <a name="disable-javascript-samples"></a>Deaktivieren von JavaScript-Beispielen  

Standardmäßig werden im **Hauptabschnitt** einer Aufzeichnung detaillierte Aufrufstapel von JavaScript-Funktionen angezeigt, die während der Aufzeichnung aufgerufen wurden.  So deaktivieren Sie diese Aufrufstapel:  

1.  Öffnen Sie **das Menü Einstellungen erfassen.**  Navigieren Sie zu [Aufzeichnungseinstellungen anzeigen.](#show-recording-settings)  
1.  Aktivieren Sie das **Kontrollkästchen JavaScript-Beispiele** deaktivieren.  
1.  Nehmen Sie eine Aufzeichnung der Seite vor.  
    
Die folgenden beiden Abbildungen zeigen den Unterschied zwischen dem Deaktivieren und Aktivieren von JavaScript-Beispielen.  Der **Abschnitt "Main"** der Aufzeichnung ist wesentlich kürzer, wenn das Sampling deaktiviert ist, da alle JavaScript-Aufrufstapel nicht verwendet werden.  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-on.msft.png" alt-text="Ein Beispiel für eine Aufzeichnung, wenn JS-Beispiele deaktiviert sind" lightbox="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-on.msft.png":::
         Ein Beispiel für eine Aufzeichnung, wenn JS-Beispiele deaktiviert sind  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off.msft.png" alt-text="Ein Beispiel für eine Aufzeichnung, wenn JS-Beispiele aktiviert sind" lightbox="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off.msft.png":::
         Ein Beispiel für eine Aufzeichnung, wenn JS-Beispiele aktiviert sind  
      :::image-end:::  
   :::column-end:::
:::row-end:::

### <a name="throttle-the-network-while-recording"></a>Drosseln des Netzwerks während der Aufzeichnung  

So drosseln Sie das Netzwerk während der Aufzeichnung:  

1.  Öffnen Sie **das Menü Einstellungen erfassen.**  Navigieren Sie zu [Aufzeichnungseinstellungen anzeigen.](#show-recording-settings)  
1.  Legen **Sie Netzwerk** auf die gewünschte Drosselungsstufe.  
    
### <a name="throttle-the-cpu-while-recording"></a>Drosseln der CPU während der Aufzeichnung  

So drosseln Sie die CPU während der Aufzeichnung:  

1.  Öffnen Sie **das Menü Einstellungen erfassen.**  Navigieren Sie zu [Aufzeichnungseinstellungen anzeigen.](#show-recording-settings)  
1.  Legen **Sie die CPU** auf die gewünschte Drosselungsstufe.  
    
Die Einschränkung ist relativ zu den Funktionen Ihres Computers.  Die **2x-Verlangsamungsoption** z. B. macht ihre CPU zwei Mal langsamer als normal.  DevTools simulieren nicht wirklich die CPUs mobiler Geräte, da sich die Architektur mobiler Geräte stark von der architektur von Desktops und Laptops unterscheiden.  

### <a name="turn-on-advanced-paint-instrumentation"></a>Aktivieren der erweiterten Farbinstrumentierung  

So zeigen Sie die detaillierte Farbinstrumentierung an:  

1.  Öffnen Sie **das Menü Einstellungen erfassen.**  Navigieren Sie zu [Aufzeichnungseinstellungen anzeigen.](#show-recording-settings)  
1.  Aktivieren Sie **das Kontrollkästchen Erweiterte Farbinstrumentierung aktivieren (langsam).**  

Um zu erfahren, wie Sie mit den Farbinformationen interagieren, navigieren Sie zu [Ebenen anzeigen](#view-layers-information) und [Lackprofiler anzeigen.](#view-paint-profiler)  

## <a name="save-a-recording"></a>Speichern einer Aufzeichnung  

Öffnen Sie zum Speichern einer Aufzeichnung das Kontextmenü \(klicken Sie mit der rechten Maustaste auf\), und wählen Sie **Profil speichern aus.**  

:::image type="complex" source="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off-save-profile.msft.png" alt-text="Profil speichern" lightbox="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off-save-profile.msft.png":::
   **Profil speichern**  
:::image-end:::  

## <a name="load-a-recording"></a>Laden einer Aufzeichnung  

Öffnen Sie zum Laden einer Aufzeichnung das Kontextmenü \(klicken Sie mit der rechten Maustaste\), und wählen Sie **Profil laden aus.**  

:::image type="complex" source="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off-load-profile.msft.png" alt-text="Lastenprofil" lightbox="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off-load-profile.msft.png":::
   **Lastenprofil**  
:::image-end:::  

## <a name="clear-the-previous-recording"></a>Löschen der vorherigen Aufzeichnung  

Nachdem Sie eine Aufzeichnung gemacht haben, **wählen** Sie Aufzeichnung löschen \( Aufzeichnungssymbol löschen \) aus, um diese Aufzeichnung im ![ ](../media/clear-recording-icon.msft.png) Leistungsbereich **zu** löschen.  

:::image type="complex" source="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off-clear-button.msft.png" alt-text="Löschen der Aufzeichnung" lightbox="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off-clear-button.msft.png":::
   **Löschen der Aufzeichnung**  
:::image-end:::  

## <a name="analyze-a-performance-recording"></a>Analysieren einer Leistungsaufzeichnung  

Nachdem Sie [die Laufzeitleistung oder](#record-runtime-performance) **** die Ladeleistung aufgezeichnet [haben,](#record-load-performance)stellt der Bereich Leistung eine Menge Daten für die Analyse der Leistung der gerade geschehenen Daten zur Wahl.  

### <a name="select-a-portion-of-a-recording"></a>Auswählen eines Teils einer Aufzeichnung  

Ziehen Sie die Maus nach links oder rechts über die **Übersicht,** um einen Teil einer Aufzeichnung auszuwählen.  Der **Abschnitt Übersicht** enthält die Diagramme **FPS,** **CPU**und **NET.**  

:::image type="complex" source="../media/evaluate-performance-performance-zoom-highlighted.msft.png" alt-text="Ziehen Sie die Maus über die Übersicht, um zu zoomen" lightbox="../media/evaluate-performance-performance-zoom-highlighted.msft.png":::
   Ziehen Sie die Maus über die **Übersicht,** um zu zoomen  
:::image-end:::  

So wählen Sie einen Teil mithilfe der Tastatur aus:  

1.  Wählen Sie den Hintergrund des **Abschnitts Main** oder einen der abschnitte daneben aus, z. B. **Interaktionen,** **Netzwerk**oder **GPU**.  Dieser Tastaturworkflow funktioniert nur, wenn sich einer dieser Abschnitte im Fokus befindet.  
1.  Verwenden Sie die Tasten , , , um `W` `A` zu `S` zoomen, nach links zu verschieben, zu verkleinern und nach rechts `D` zu verschieben.  

Führen Sie die folgenden Aktionen aus, um einen Teil mithilfe eines Trackpads auszuwählen.  

1.  Zeigen Sie mit der Maus auf den **Abschnitt Übersicht** oder den **Abschnitt Details.**  Der **Abschnitt Übersicht** ist der Bereich, der die **FPS-,** **CPU-** und **#A0** enthält.  Der **Abschnitt Details** ist der Bereich, der den Abschnitt **Main,** den Abschnitt **Interaktionen** und so weiter enthält.  
1.  Wischen Sie mit zwei Fingern nach oben, um sie zu verkleinern, wischen Sie nach links, wischen Sie nach unten, um zu vergrößern, und wischen Sie nach rechts, um nach rechts zu wechseln.  

Wenn Sie ein langes Flammendiagramm im **Abschnitt "Main"** oder einen der Benachbarten scrollen möchten, wählen Sie beim Ziehen nach oben und unten die Option und halten sie gedrückt.  Ziehen Sie nach links und rechts, um den ausgewählten Teil der Aufzeichnung zu verschieben.  

### <a name="search-activities"></a>Suchaktivitäten  

Wählen `Control` + `F` Sie \(Windows, Linux\) oder `Command` + `F` \(macOS\) **** aus, um das Suchfeld am unteren Rand des Leistungsbereichs zu öffnen.  

:::image type="complex" source="../media/evaluate-performance-performance-search-regex.msft.png" alt-text="Suchfeld" lightbox="../media/evaluate-performance-performance-search-regex.msft.png":::
   Suchfeld  
:::image-end:::  

So navigieren Sie zu Aktivitäten, die mit Ihrer Abfrage übereinstimmen:  

*   Verwenden Sie **die Schaltflächen** Previous \( ![ Previous ](../media/previous-icon.msft.png) \) und **Next** \( ![ Next ](../media/next-icon.msft.png) \).  
*   Wählen `Shift` + `Enter` Sie diese Option aus, um den `Enter` vorherigen oder den nächsten auszuwählen.  

So ändern Sie Abfrageeinstellungen:  

*   Wählen **Sie Zwischen- und** ![ Kleinschreibung \( Zwischenfall ](../media/search-case-icon.msft.png) und \) aus, um die Abfragefalle vertraulich zu machen.  
*   Wählen **Sie Regex** \( ![ Regex ](../media/search-regex-icon.msft.png) \) aus, um einen regulären Ausdruck in Ihrer Abfrage zu verwenden.  

Wählen Sie Abbrechen aus, um das Suchfeld **auszublenden.**  

### <a name="view-main-thread-activity"></a>Anzeigen der Hauptthreadaktivität  

Verwenden Sie **den Abschnitt Main,** um Aktivitäten im Hauptthread der Seite zu anzeigen.  

:::image type="complex" source="../media/evaluate-performance-performance-main-zoomed.msft.png" alt-text="Der Abschnitt "Main"" lightbox="../media/evaluate-performance-performance-main-zoomed.msft.png":::
   Der **Abschnitt "Main"**  
:::image-end:::  

Wählen Sie ein Ereignis aus, um weitere Informationen zu diesem Ereignis im **Zusammenfassungsfenster anzeigen** zu können.  DevTools umreißt das ausgewählte Ereignis.  

:::image type="complex" source="../media/evaluate-performance-performance-summary-me.msft.png" alt-text="Weitere Informationen zur anonymen Funktion im Zusammenfassungsfenster" lightbox="../media/evaluate-performance-performance-summary-me.msft.png":::
   Weitere Informationen zur `anonymous` Funktion im **Zusammenfassungsfenster**  
:::image-end:::  

DevTools stellt die Hauptthreadaktivität mit einem Flammendiagramm dar.  Die x-Achse stellt die Aufzeichnung im Laufe der Zeit dar.  Die y-Achse stellt die Aufrufliste dar.  Die Ereignisse oben verursachen die Ereignisse darunter.  

:::image type="complex" source="../media/evaluate-performance-performance-main-flame-chart.msft.png" alt-text="Ein Flammendiagramm" lightbox="../media/evaluate-performance-performance-main-flame-chart.msft.png":::
   Ein Flammendiagramm  
:::image-end:::  

In der vorherigen Abbildung hat ein `click` Ereignis ein In in zeile `Function Call` `activitytabs.js` 53 verursacht.  Überprüfen `Function Call` Sie unten, ob eine anonyme Funktion ausgeführt wurde.  Die anonyme Funktion angefordert `a` , die angefordert hat , die angefordert `wait` `Minor GC` hat.  

DevTools weist Skripts zufällige Farben zu.  In der vorherigen Abbildung sind Funktionsanforderungen von einem Skript hellgrün gefärbt.  Anforderungen von einem anderen Skript sind gefärbtes Grau.  Das dunklere Gelb stellt die Skriptaktivität dar, und das violette Ereignis stellt die Renderingaktivität dar.  Diese dunkleren gelben und violetten Ereignisse sind für alle Aufzeichnungen konsistent.  

Navigieren Sie [zu Deaktivieren von JavaScript-Beispielen,](#disable-javascript-samples) wenn Sie das detaillierte Flammendiagramm von JavaScript-Anforderungen ausblenden möchten.  Wenn JS-Beispiele deaktiviert sind, werden nur Ereignisse auf hoher Ebene wie und aus der `Event: choose` `Function Call` vorherigen Abbildung `str` angezeigt.  

### <a name="view-activities-in-a-table"></a>Anzeigen von Aktivitäten in einer Tabelle  

Nach dem Aufzeichnen einer Seite müssen Sie sich nicht nur auf den **Abschnitt "Main"** verlassen, um Aktivitäten zu analysieren.  DevTools bietet außerdem drei Tabellenansichten für die Analyse von Aktivitäten.  Jede Ansicht bietet Ihnen eine andere Perspektive für die Aktivitäten:  

*   Wenn Sie die Stammaktivitäten anzeigen möchten, die am meisten Arbeit verursachen, verwenden Sie den [Anrufstrukturbereich.](#the-call-tree-panel)  
*   Wenn Sie die Aktivitäten anzeigen möchten, in denen die meiste Zeit direkt verbracht wurde, verwenden Sie den [Bottom-Up-Bereich.](#the-bottom-up-panel)  
*   Wenn Sie die Aktivitäten in der Reihenfolge anzeigen möchten, in der sie während der Aufzeichnung aufgetreten sind, verwenden Sie den [Ereignisprotokollbereich.](#the-event-log-panel)  
    
> [!NOTE]
> Die nächsten drei Abschnitte beziehen sich alle auf die gleiche Demo.  Führen Sie die Demo selbst unter [Activity Tabs Demo aus.][ActivityTabsDemo]  

#### <a name="root-activities"></a>Stammaktivitäten  

Hier finden Sie **** eine Erläuterung des Konzepts **** der Stammaktivitäten, das im Bereich Anrufstruktur, **Bottom-Up-Bereich** und **Ereignisprotokoll erwähnt** wird.  

Stammaktivitäten sind diejenigen, die dazu führen, dass der Browser einige Arbeit macht.  Wenn Sie beispielsweise eine Webseite auswählen, führt der Browser eine `Event` Aktivität als Stammaktivität aus.  Dies `Event` kann dazu führen, dass ein Handler ausgeführt wird, und so weiter.  

Im Flammendiagramm des **Abschnitts Main** befinden sich die Stammaktivitäten am oberen Rand des Diagramms.  In den **Feldern Anrufstruktur** **und Ereignisprotokoll** sind Stammaktivitäten die Elemente auf oberster Ebene.  

Navigieren Sie zum [Bereich Anrufstruktur,](#the-call-tree-panel) um ein Beispiel für Stammaktivitäten zu finden.  

#### <a name="the-call-tree-panel"></a>Der Bereich "Anrufstruktur"  

Verwenden Sie **den Anrufstrukturbereich,** um zu sehen, [welche Stammaktivitäten](#root-activities) am meisten Arbeit verursachen.  

Im **Bereich Anrufstruktur** werden nur Aktivitäten während des ausgewählten Abschnitts der Aufzeichnung angezeigt.  Navigieren Sie [zu Wählen Sie einen Teil einer Aufzeichnung aus,](#select-a-portion-of-a-recording) um zu erfahren, wie Sie Teile auswählen.  

:::image type="complex" source="../media/evaluate-performance-performance-call-tree.msft.png" alt-text="Der Bereich "Anrufstruktur"" lightbox="../media/evaluate-performance-performance-call-tree.msft.png":::
   Der **Bereich "Anrufstruktur"**  
:::image-end:::  

In der vorherigen Abbildung ist die oberste Ebene der Elemente in der Spalte **Aktivität,** z. B. Und `Evaluate Script` sind `Parse HTML` Stammaktivitäten.  Die Verschachtelung stellt die Aufrufliste dar.  Beispiel: in der vorherigen Abbildung, `Parse HTML` die verursacht hat, `Evaluate Script` und `Compile Script` `(anonymous)` .  

**Self Time stellt** die Zeit dar, die direkt in dieser Aktivität verbracht wird.  **Die Gesamtzeit** stellt die Zeit dar, die in dieser Aktivität oder einem der kinder verbracht wird.  

Wählen **Sie Self Time**, Total **Time**oder **Activity** aus, um die Tabelle nach dieser Spalte zu sortieren.  

Verwenden Sie das **Textfeld Filter,** um Ereignisse nach Aktivitätsnamen zu filtern.  

Standardmäßig ist **das Menü Gruppierung** auf Keine Gruppierung **festgelegt.**  Verwenden Sie **das Menü** Gruppierung, um die Aktivitätstabelle nach verschiedenen Kriterien zu sortieren.  

Wählen **Sie Schwerer Stapel** anzeigen \( Schwerer Stapel anzeigen \) aus, um eine weitere Tabelle rechts neben der ![ ](../media/show-heaviest-stack-icon.msft.png) **Aktivitätstabelle zu** zeigen.  Wählen Sie eine Aktivität aus, um die **Tabelle "Schwerster Stapel" auffüllen** zu können.  In **der Tabelle "Schwerster Stapel"** wird angezeigt, welche Kinder der ausgewählten Aktivität am längsten ausgeführt wurden.  

#### <a name="the-bottom-up-panel"></a>The Bottom-Up panel  

Verwenden Sie **den Bottom-Up-Bereich,** um zu sehen, welche Aktivitäten am häufigsten zusammengefasst verwendet wurden.  

Im **Bottom-Up-Bereich** werden nur Aktivitäten während des ausgewählten Teils der Aufzeichnung angezeigt.  Navigieren Sie [zu Wählen Sie einen Teil einer Aufzeichnung aus,](#select-a-portion-of-a-recording) um zu erfahren, wie Sie Teile auswählen.  

:::image type="complex" source="../media/evaluate-performance-performance-bottoms-up.msft.png" alt-text="The Bottom-Up panel" lightbox="../media/evaluate-performance-performance-bottoms-up.msft.png":::
   The **Bottom-Up** panel  
:::image-end:::  

Navigieren Sie **im Diagramm Hauptabschnitt** Flammen der vorherigen Abbildung zu dem fast die ganze Zeit, die für die Ausführung auf sich `Parse HTML` hatte.  Die oberste Aktivität im **Bottom-Up-Bereich** der vorherigen Abbildung ist `Parse HTML` .  <!--In the flame chart of the previous figure, the yellow below the calls to `wait` are actually thousands of `Minor GC` calls.  -->  Navigieren Sie zum **Bottom-Up-Bereich,** die nächste teuerste Aktivität ist `Layout` .  

Die **Spalte Self Time** stellt die aggregierte Zeit dar, die direkt in dieser Aktivität über alle Vorkommen hinweg verbracht wird.  

Die **Spalte Gesamtzeit** stellt die aggregierte Zeit dar, die in dieser Aktivität oder in einem der unterg nen Aktivitäten verbracht wird.  

#### <a name="the-event-log-panel"></a>Ereignisprotokollbereich  

Verwenden Sie **den Ereignisprotokollbereich,** um Aktivitäten in der Reihenfolge zu anzeigen, in der sie während der Aufzeichnung aufgetreten sind.  

Im **Ereignisprotokollbereich** werden nur Aktivitäten während des ausgewählten Abschnitts der Aufzeichnung angezeigt.  Navigieren Sie [zu Wählen Sie einen Teil einer Aufzeichnung aus,](#select-a-portion-of-a-recording) um zu erfahren, wie Sie Teile auswählen.  

:::image type="complex" source="../media/evaluate-performance-performance-event-log.msft.png" alt-text="Ereignisprotokollbereich" lightbox="../media/evaluate-performance-performance-event-log.msft.png":::
   **Ereignisprotokollbereich**  
:::image-end:::  

Die **Spalte Startzeit** stellt den Zeitpunkt dar, an dem diese Aktivität gestartet wurde, relativ zum Beginn der Aufzeichnung.  Beispielsweise bedeutet die Startzeit für das ausgewählte Element in der vorherigen Abbildung, dass die Aktivität `175.7 ms` 175,7 ms nach Beginn der Aufzeichnung gestartet wurde.  

Die **Spalte Self Time** stellt die Zeit dar, die direkt in dieser Aktivität verbracht wird.  

Die **Spalten Gesamtzeit** stellen die Zeit dar, die direkt in dieser Aktivität oder in einem der unterg nen Aktivitäten verbracht wird.  

Wählen **Sie Startzeit,** **Selbstzeit**oder **Gesamtzeit aus,** um die Tabelle nach dieser Spalte zu sortieren.

Verwenden Sie das **Textfeld Filter,** um Aktivitäten nach Namen zu filtern.  

Verwenden Sie **das Menü Dauer,** um aktivitäten herausfiltern, die weniger als 1 ms oder 15 ms dauerten.  Standardmäßig ist das **Menü Dauer** auf **Alle festgelegt,** d. h. alle Aktivitäten werden angezeigt.  

Deaktivieren Sie **die Kontrollkästchen Laden,** **** **Skripten,** **Rendern**oder Malen, um alle Aktivitäten aus diesen Kategorien heraus zu filtern.  

### <a name="view-gpu-activity"></a>Anzeigen der GPU-Aktivität  

Anzeigen der GPU-Aktivität im **Abschnitt GPU.**  

:::image type="complex" source="../media/evaluate-performance-performance-gpu-zoomed.msft.png" alt-text="Der Abschnitt "GPU"" lightbox="../media/evaluate-performance-performance-gpu-zoomed.msft.png":::
   Der **Abschnitt "GPU"**  
:::image-end:::  

### <a name="view-raster-activity"></a>Anzeigen der Rasteraktivität  

Anzeigen der Rasteraktivität im **Abschnitt Raster.**  

:::image type="complex" source="../media/evaluate-performance-performance-raster.msft.png" alt-text="Der Abschnitt Raster" lightbox="../media/evaluate-performance-performance-raster.msft.png":::
   Der **Abschnitt Raster**  
:::image-end:::  

### <a name="view-interactions"></a>Anzeigen von Interaktionen  

Verwenden Sie **den Abschnitt Interaktionen,** um Benutzerinteraktionen zu suchen und zu analysieren, die während der Aufzeichnung passiert sind.  

:::image type="complex" source="../media/evaluate-performance-performance-interactions-animation.msft.png" alt-text="Der Abschnitt Interaktionen" lightbox="../media/evaluate-performance-performance-interactions-animation.msft.png":::
   Der **Abschnitt Interaktionen**  
:::image-end:::  

Eine rote Linie am unteren Rand einer Interaktion stellt die Wartezeit auf den Hauptthread dar.  

Wählen Sie eine Interaktion aus, um weitere Informationen dazu im **Zusammenfassungsfenster einblenden** zu können.  

### <a name="analyze-frames-per-second-fps"></a>Analysieren von Frames pro Sekunde (FPS)  

DevTools bietet zahlreiche Möglichkeiten zum Analysieren von Frames pro Sekunde:  

*   Verwenden [Sie das FPS-Diagramm,](#the-fps-chart) um eine Übersicht über FPS über die Dauer der Aufzeichnung zu erhalten.  
*   Verwenden [Sie den Abschnitt Frames,](#the-frames-section) um die Dauer eines bestimmten Frames zu sehen.  
*   Verwenden Sie **das #A0** für eine Echtzeitschätzung von FPS, während die Seite ausgeführt wird.  Navigieren Sie [mit dem FPS-Meter zu](#view-frames-per-second-in-realtime-with-the-fps-meter)Frames pro Sekunde in Echtzeit anzeigen.  
    
#### <a name="the-fps-chart"></a>Das #A0  

Das **#A0** bietet eine Übersicht über die Framerate während der Dauer einer Aufzeichnung.  Im Allgemeinen gilt: Je höher der grüne Balken, desto besser ist die Framerate.  

Ein roter Balken über dem **#A0** ist eine Warnung, dass die Framerate so niedrig gefallen ist, dass sie wahrscheinlich die Benutzererfahrung geschädigt hat.  

:::image type="complex" source="../media/evaluate-performance-performance-fps-highlight.msft.png" alt-text="Das #A0" lightbox="../media/evaluate-performance-performance-fps-highlight.msft.png":::
   Das **#A0**  
:::image-end:::  

#### <a name="the-frames-section"></a>Der Abschnitt Frames  

Im **Abschnitt Frames** erfahren Sie genau, wie lange ein bestimmter Frame ge dauern hat.  

Zeigen Sie auf einen Frame, um eine QuickInfo mit weiteren Informationen dazu zu sehen.  

:::image type="complex" source="../media/evaluate-performance-performance-frames-hover.msft.png" alt-text="Zeigen auf einen Frame" lightbox="../media/evaluate-performance-performance-frames-hover.msft.png":::
   Zeigen auf einen Frame  
:::image-end:::  

Wählen Sie einen Frame aus, um weitere Informationen zum Frame im **Zusammenfassungsbereich anzeigen zu** können.  DevTools umreißt den ausgewählten Frame in Blau.  

:::image type="complex" source="../media/evaluate-performance-performance-frames-summary.msft.png" alt-text="Anzeigen eines Frames im Zusammenfassungsfenster" lightbox="../media/evaluate-performance-performance-frames-summary.msft.png":::
   Anzeigen eines Frames im **Zusammenfassungsfenster**  
:::image-end:::  

### <a name="view-network-requests"></a>Anzeigen von Netzwerkanforderungen  

Erweitern Sie den **Abschnitt Netzwerk,** um einen Wasserfall mit Netzwerkanforderungen zu sehen, die während der Aufzeichnung aufgetreten sind.  

:::image type="complex" source="../media/evaluate-performance-performance-network.msft.png" alt-text="Der Abschnitt "Netzwerk"" lightbox="../media/evaluate-performance-performance-network.msft.png":::
   Der **Abschnitt "Netzwerk"**  
:::image-end:::  

Anforderungen sind wie folgt farblich codiert:  

*   HTML: Blau  
*   CSS: Lila  
*   JS: Gelb  
*   Bilder: Grün  
    
Wählen Sie eine Anforderung aus, um weitere Informationen dazu im **Zusammenfassungsfenster anzeigen** zu können.  In der vorherigen Abbildung **** zeigt der Zusammenfassungsbereich beispielsweise weitere Informationen zur blauen Anforderung an, die im Abschnitt **Netzwerk ausgewählt** ist.  

Ein dunkelblaues Quadrat oben links einer Anforderung bedeutet, dass es sich um eine Anforderung mit höherer Priorität handelt.  Ein heller-blaues Quadrat bedeutet niedrigere Priorität.  In der vorherigen Abbildung hat die blaue, ausgewählte Anforderung beispielsweise eine höhere Priorität, und die grüne Anforderung darunter hat eine niedrigere Priorität.  

In der 1. der folgenden Abbildungen wird die Anforderung durch eine Linie auf der linken Seite, eine Leiste in der Mitte mit einem dunklen Und einem hellen Teil und einer Linie auf der rechten Seite `www.bing.com` dargestellt.  Im 2. der folgenden Abbildungen ist die entsprechende Darstellung derselben Anforderung im **Zeitfenster** des **Netzwerktools** angezeigt.  So ordnen sich diese beiden Darstellungen zu:

*   Die linke Linie ist alles bis zur `Connection Start` Gruppe von Ereignissen, einschließlich.  Mit anderen Worten, es ist alles vor `Request Sent` , exklusiv.  
*   Der helle Teil der Leiste ist `Request Sent` und `Waiting (TTFB)` .  
*   Der dunkle Teil der Leiste ist `Content Download` .  
*   Die rechte Linie ist im Wesentlichen eine Zeit, die auf das Warten auf den Hauptthread wartet.  Dies wird im **Zeitsteuerungsfenster nicht** dargestellt.  
    
:::row:::
   :::column span="":::
      :::image type="complex" source="../media/evaluate-performance-bing-performance-network.msft.png" alt-text="Die Zeilenleistendarstellung der www.bing.com Anforderung" lightbox="../media/evaluate-performance-bing-performance-network.msft.png":::
         Die Zeilenleistendarstellung der `www.bing.com` Anforderung  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/evaluate-performance-bing-network-timing.msft.png" alt-text="Das Netzwerktool" lightbox="../media/evaluate-performance-bing-network-timing.msft.png":::
         Das **Netzwerktool**  
: ::image-end:::  
   :::column-end:::
:::row-end:::

### <a name="view-memory-metrics"></a>Anzeigen von Speichermetriken  

Aktivieren Sie das **Kontrollkästchen Speicher,** um Speichermetriken aus der letzten Aufzeichnung anzuzeigen.  

:::image type="complex" source="../media/evaluate-performance-performance-memory-highlight.msft.png" alt-text="Das Kontrollkästchen Speicher" lightbox="../media/evaluate-performance-performance-memory-highlight.msft.png":::
   Das **Kontrollkästchen Speicher**  
:::image-end:::  

DevTools zeigt ein neues **Arbeitsspeicherdiagramm** über dem **Zusammenfassungsfenster** an.  Es gibt auch ein neues Diagramm unterhalb des **NET-Diagramms** mit dem Namen **HEAP**.  Das **HEAP-Diagramm** enthält die gleichen Informationen wie die **JS-Heap-Zeile** im **Arbeitsspeicherdiagramm.**  

:::image type="complex" source="../media/evaluate-performance-performance-memory-chart.msft.png" alt-text="Speichermetriken" lightbox="../media/evaluate-performance-performance-memory-chart.msft.png":::
   Speichermetriken  
:::image-end:::  

Die farbigen Linien im Diagramm werden den farbigen Kontrollkästchen oberhalb des Diagramms angezeigt.  
Deaktivieren Sie ein Kontrollkästchen, um diese Kategorie im Diagramm auszublenden.  

Das Diagramm zeigt nur den Bereich der aktuell ausgewählten Aufzeichnung an.  In der vorherigen Abbildung **** zeigt das Diagramm Arbeitsspeicher beispielsweise nur die Speicherauslastung zwischen 400 ms und 1750 ms an.  

### <a name="view-the-duration-of-a-portion-of-a-recording"></a>Anzeigen der Dauer eines Teils einer Aufzeichnung  

Bei der Analyse eines Abschnitts wie **"Netzwerk"** oder **"Main"** benötigen Sie manchmal eine genauere Schätzung der Dauer bestimmter Ereignisse.  Halten, auswählen und halten Sie, und ziehen Sie nach links oder rechts, um `Shift` einen Teil der Aufzeichnung auszuwählen.  Am unteren Rand Ihrer Auswahl zeigt DevTools, wie lange dieser Teil ge dauern hat.  

:::image type="complex" source="../media/evaluate-performance-performance-main-duration.msft.png" alt-text="Anzeigen der Dauer eines Teils einer Aufzeichnung" lightbox="../media/evaluate-performance-performance-main-duration.msft.png":::
   Anzeigen der Dauer eines Teils einer Aufzeichnung  
:::image-end:::  

### <a name="view-a-screenshot"></a>Screenshot anzeigen  

Navigieren Sie während der Aufzeichnung zu Screenshots [aufnehmen,](#capture-screenshots-while-recording) um zu erfahren, wie Sie Screenshots aktivieren.  

Zeigen Sie auf **die Übersicht,** um einen Screenshot zu sehen, wie die Seite in diesem Moment der Aufzeichnung aussah.  Der **Abschnitt Übersicht** enthält die Diagramme **CPU,** **FPS**und **NET.**  

:::image type="complex" source="../media/evaluate-performance-performance-screenshots-hover.msft.png" alt-text="Screenshot anzeigen" lightbox="../media/evaluate-performance-performance-screenshots-hover.msft.png":::
   Screenshot anzeigen  
:::image-end:::  

Sie können auch Screenshots anzeigen, indem Sie im Abschnitt Frames einen **Frame** auswählen.  DevTools zeigt eine kleine Version des Screenshots im **Zusammenfassungsbereich** an.  

:::image type="complex" source="../media/evaluate-performance-performance-summary-preview.msft.png" alt-text="Anzeigen eines Screenshots im Zusammenfassungsfenster" lightbox="../media/evaluate-performance-performance-summary-preview.msft.png":::
   Anzeigen eines Screenshots im **Zusammenfassungsfenster**  
:::image-end:::  

Wählen Sie die Miniaturansicht im **Zusammenfassungsfenster aus,** um den Screenshot zu vergrößern.  

:::image type="complex" source="../media/evaluate-performance-performance-summary-preview-select.msft.png" alt-text="Vergrößern eines Screenshots aus dem Zusammenfassungsfenster" lightbox="../media/evaluate-performance-performance-summary-preview-select.msft.png":::
   Vergrößern eines Screenshots aus dem **Zusammenfassungsfenster**  
:::image-end:::  

### <a name="view-layers-information"></a>Anzeigen von Layerinformationen  

So zeigen Sie erweiterte Layerinformationen zu einem Frame an:  

1.  [Aktivieren Sie die erweiterte Malinstrumentierung.](#turn-on-advanced-paint-instrumentation)  
1.  Wählen Sie im Abschnitt **Frames einen Frame** aus.  DevTools zeigt Informationen zu den Ebenen im neuen **Ebenenbereich** neben dem **Ereignisprotokollbereich** an.  
    
    :::image type="complex" source="../media/evaluate-performance-layers-all.msft.png" alt-text="Der Bereich Ebenen" lightbox="../media/evaluate-performance-layers-all.msft.png":::
       Der **Bereich Ebenen**  
    :::image-end:::  
    
Zeigen Sie auf eine Ebene, um sie im Diagramm zu markieren.  

:::image type="complex" source="../media/evaluate-performance-performance-frames-document-nav-bar-highlighted.msft.png" alt-text="Hervorheben einer Ebene" lightbox="../media/evaluate-performance-performance-frames-document-nav-bar-highlighted.msft.png":::
   Hervorheben einer Ebene  
:::image-end:::  

So verschieben Sie das Diagramm:  

*   Wählen **Sie Schwenkmodus** \( ![ Schwenkmodus ](../media/pan-mode-icon.msft.png) \), um sich entlang der X- und Y-Achsen zu bewegen.  
*   Wählen **Sie Drehmodus** \( ![ Drehmodus ](../media/rotate-mode-icon.msft.png) \) aus, um sich entlang der Z-Achse zu drehen.  
*   Wählen **Sie Transform zurücksetzen** \( Transform zurücksetzen ![ ](../media/reset-transform-icon.msft.png) \), um das Diagramm an die ursprüngliche Position zurückzusetzen.  
    
### <a name="view-paint-profiler"></a>Anzeigen von Farbprofiler  

So zeigen Sie erweiterte Informationen zu einem Paint-Ereignis an:  

1.  [Aktivieren Sie](#turn-on-advanced-paint-instrumentation).  
1.  Wählen Sie im **Abschnitt** Main ein **Paint-Ereignis** aus.  
    
    :::image type="complex" source="../media/evaluate-performance-paint-profiler.msft.png" alt-text="Der Bereich "Paint Profiler"" lightbox="../media/evaluate-performance-paint-profiler.msft.png":::
       Der **Bereich "Paint Profiler"**  
    :::image-end:::  
    
## <a name="analyze-rendering-performance-with-the-rendering-tool"></a>Analysieren der Renderingleistung mit dem Renderingtool  

Verwenden Sie die **** Features des Renderingbereichs, um die Renderingleistung Ihrer Seite zu visualisieren.  

So öffnen Sie das **Renderingtool:**  

1.  [Öffnen Sie das Befehlsmenü][DevToolsCommandMenu].  
1.  Beginnen Sie mit der `Rendering` Eingabe und wählen Sie `Show Rendering` aus.  DevTools zeigt das **Renderingtool** am unteren Rand des DevTools-Fensters an.  
    
    :::image type="complex" source="../media/evaluate-performance-console-drawer-rendering.msft.png" alt-text="Das Renderingtool" lightbox="../media/evaluate-performance-console-drawer-rendering.msft.png":::
       Das **Renderingtool**  
    :::image-end:::  
    
### <a name="view-frames-per-second-in-realtime-with-the-fps-meter"></a>Anzeigen von Frames pro Sekunde in Echtzeit mit dem #A0  

Die **#A0 ist** eine Überlagerung, die in der oberen rechten Ecke Des Viewports angezeigt wird.  Es bietet eine Echtzeitschätzung von FPS, während die Seite ausgeführt wird.  So öffnen Sie das **FPS-Zähler:**  

1.  Öffnen Sie das **Renderingtool.**  [Analysieren Sie die Renderingleistung mit dem Renderingtool](#analyze-rendering-performance-with-the-rendering-tool).  
1.  Aktivieren Sie das **Kontrollkästchen FPS Meter.**  
    
    :::image type="complex" source="../media/evaluate-performance-jank-console-rendering-frame-rate.msft.png" alt-text="Das #A0" lightbox="../media/evaluate-performance-jank-console-rendering-frame-rate.msft.png":::
       Das **#A0**  
    :::image-end:::  
    
### <a name="view-painting-events-in-realtime-with-paint-flashing"></a>Anzeigen von Malereignissen in Echtzeit mit Paint Flashing  

Verwenden Sie Paint Flashing, um eine Echtzeitansicht aller Malereignisse auf der Seite zu erhalten.  Jedes Mal, wenn ein Teil der Seite neu angestrichen wird, umreißt DevTools diesen Abschnitt grün.  

Führen Sie die folgenden Aktionen aus, um das Blinken von Farben zu aktivieren.  

1.  Öffnen Sie das **Renderingtool.**  Navigieren Sie zu [Renderleistung mit dem Renderingtool analysieren.](#analyze-rendering-performance-with-the-rendering-tool)  
1.  Aktivieren Sie das **Kontrollkästchen Farbenblitzen.**  
    
    :::image type="complex" source="../media/evaluate-performance-jank-console-rendering-paint-flashing.msft.png" alt-text="Blinken von Farben" lightbox="../media/evaluate-performance-jank-console-rendering-paint-flashing.msft.png":::
       **Blinken von Farben**  
    :::image-end:::  
    
### <a name="view-an-overlay-of-layers-with-layer-borders"></a>Anzeigen einer Überlagerung von Ebenen mit Ebenenrändern  

Verwenden **Sie Ebenenränder,** um eine Überlagerung von Ebenenrändern und Kacheln oben auf der Seite zu sehen.  

Führen Sie zum Aktivieren von Ebenenrändern die folgenden Aktionen aus:  

1.  Öffnen Sie das **Renderingtool.**  Navigieren Sie zu [Renderleistung mit dem Renderingtool analysieren.](#analyze-rendering-performance-with-the-rendering-tool)  
1.  Aktivieren Sie das **Kontrollkästchen Ebenenränder.**  
    
    :::image type="complex" source="../media/evaluate-performance-devtools-console-rendering-layer-borders.msft.png" alt-text="Ebenenränder" lightbox="../media/evaluate-performance-devtools-console-rendering-layer-borders.msft.png":::
       **Ebenenränder**  
    :::image-end:::  
    
Navigieren Sie zu den Kommentaren in [debug_colors.cc,][ChromiumDebugColors] um eine Erläuterung der Farbcodierungen zu erhalten.  

### <a name="find-scroll-performance-issues-in-realtime"></a>Suchen von Problemen mit der Bildlaufleistung in Echtzeit  

Verwenden Sie Bildlaufleistungsprobleme, um Elemente der Seite zu identifizieren, die Ereignislistener im Zusammenhang mit einem Bildlauf haben, die die Leistung der Seite beeinträchtigen können.  
DevTools skizziert die potenziell problematischen Elemente in Teal.  

Führen Sie die folgenden Aktionen aus, um Probleme mit der Bildlaufleistung zu sehen. 

1.  Öffnen Sie das **Renderingtool.**  Navigieren Sie zu [Renderleistung mit dem Renderingtool analysieren.](#analyze-rendering-performance-with-the-rendering-tool)  
1.  Aktivieren Sie das **Kontrollkästchen Leistungsprobleme** beim Bildlauf.  
    
    :::image type="complex" source="../media/evaluate-performance-bing-console-drawer-rendering-scrolling-performance-issues.msft.png" alt-text="Scrolling Performance Issues gibt an, dass objekte, die nicht mit viewport eingeschränkt sind, die Bildlaufleistung beeinträchtigen können." lightbox="../media/evaluate-performance-bing-console-drawer-rendering-scrolling-performance-issues.msft.png":::
       **Scrolling Performance Issues** gibt an, dass objekte, die nicht mit viewport eingeschränkt sind, die Bildlaufleistung beeinträchtigen können.  
    :::image-end:::  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium/index.md "Microsoft Edge (Chromium) Entwicklertools | Microsoft Docs"  
[DevToolsCommandMenu]: ../command-menu/index.md#open-the-command-menu "Öffnen Sie das Befehlsmenü - Befehle ausführen mit dem Microsoft Edge DevTools-Befehlsmenü | Microsoft Docs"  
[DevtoolsEvaluatePerformanceGettingStarted]: ./index.md "Erste Schritte mit der Analyse der Laufzeitleistung | Microsoft Docs"  

[ActivityTabsDemo]: https://microsoft-edge-chromium-devtools.glitch.me/perf/activitytabs.html "Aktivitätsregisterkarten Demo | glitch"  

[ChromiumDebugColors]: https://cs.chromium.org/chromium/src/cc/debug/debug_colors.cc "debug_colors.cc – Codesuche"  

> [!NOTE]
> Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.  
> Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/evaluate-performance/reference) und wird von [Kayce Basken][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\) verfasst.  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
