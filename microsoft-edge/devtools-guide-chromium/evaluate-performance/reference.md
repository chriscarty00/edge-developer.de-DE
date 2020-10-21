---
description: Ein Verweis auf alle Möglichkeiten zum Aufzeichnen und Analysieren der Leistung in Microsoft Edge devtools
title: Referenz zur Leistungsanalyse
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/19/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: d135f83273842a1e128df0bb346f0f126e2fbe8d
ms.sourcegitcommit: 99eee78698dc95b2a3fa638a5b063ef449899cda
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/20/2020
ms.locfileid: "11125139"
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

# Referenz zur Leistungsanalyse  

Diese Seite ist eine umfassende Referenz zu den Microsoft Edge devtools-Features, die sich auf die Leistungsanalyse beziehen.  

Navigieren Sie zu den [ersten Schritten mit der Analyse der Laufzeitleistung][DevtoolsEvaluatePerformanceGettingStarted] für ein geführtes Lernprogramm zum Analysieren der Leistung einer Seite mit [Microsoft Edge devtools][MicrosoftEdgeDevTools].  

## Aufzeichnen der Leistung  

### Aufzeichnen der Laufzeitleistung  

Zeichnen Sie die Laufzeitleistung auf, wenn Sie die Leistung einer Seite während der Ausführung analysieren möchten, anstatt Sie zu laden.  

1.  Wechseln Sie zu der Seite, die Sie analysieren möchten.  
1.  Klicken Sie in devtools auf die Registerkarte **Leistung** .  
1.  Wählen Sie **Datensatz** \ ( ![ Eintrags Symbol ][ImageRecordIcon] \) aus.  
    
    :::image type="complex" source="../media/evaluate-performance-performance-record-highlight.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-performance-record-highlight.msft.png":::
       **Record**  
    :::image-end:::  
    
1.  Interagieren Sie mit der Seite.  DevTools zeichnet alle Seiten Aktivitäten auf, die durch ihre Interaktionen entstehen.  
1.  Wählen Sie erneut **aufzeichnen** aus, oder klicken Sie auf **Beenden** , um die Aufzeichnung zu beenden.  
    
### Aufzeichnen der Ladeleistung  

Zeichnen Sie die Ladeleistung auf, wenn Sie die Leistung einer Seite während des Ladens analysieren möchten, anstatt Sie zu starten.  

1.  Wechseln Sie zu der Seite, die Sie analysieren möchten.  
1.  Öffnen Sie das **Leistungs** Panel von devtools.  
1.  Wählen Sie **Seite aktualisieren** \ ( ![ Seite aktualisieren ][ImageRefreshPageIcon] \) aus.  DevTools zeichnet Leistungs Metriken auf, während die Seite aktualisiert wird, und stoppt dann die Aufzeichnung ein paar Sekunden nach Abschluss der Auslastung automatisch.  
    
    :::image type="complex" source="../media/evaluate-performance-performance-refresh-button.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-performance-refresh-button.msft.png":::
       **Seite aktualisieren**  
    :::image-end:::  
    
DevTools zoomt automatisch auf den Teil der Aufzeichnung, in dem die meisten Aktivitäten aufgetreten sind.  

:::image type="complex" source="../media/evaluate-performance-performance-refreshed.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-performance-refreshed.msft.png":::
   Laden einer Seite  
:::image-end:::  

### Aufzeichnen von Screenshots während der Aufzeichnung  

Aktivieren Sie das Kontrollkästchen **Screenshots** , um einen Screenshot jedes Frames während der Aufzeichnung zu erfassen.  

:::image type="complex" source="../media/evaluate-performance-performance-capture-screenshots-checkbox.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-performance-capture-screenshots-checkbox.msft.png":::
   Das Kontrollkästchen " **Screenshots** "  
:::image-end:::  

Navigieren Sie zu [einem Screenshot](#view-a-screenshot) , um zu erfahren, wie Sie mit Screenshots interagieren können.  

### Erzwingen der Garbage Collection während der Aufzeichnung  

Wenn Sie eine Seite aufzeichnen, wählen Sie **Garbage** Collection durchführen aus, ![ ][ImageCollectGarbageIcon] um die Garbage Collection zu erzwingen.  

:::image type="complex" source="../media/evaluate-performance-performance-collect-garbage-button.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-performance-collect-garbage-button.msft.png":::
   Garbage Collection  
:::image-end:::  

### Aufzeichnungseinstellungen anzeigen  

Wählen Sie **aufnahmeeinstellungen** \ ( ![ Aufnahmeeinstellungen ][ImageCaptureSettingsIcon] \) aus, um weitere Einstellungen anzuzeigen, die sich darauf beziehen, wie devtools Leistungs Aufzeichnungen erfasst.  

:::image type="complex" source="../media/evaluate-performance-performance-capture-settings-button-open-drawer.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-performance-capture-settings-button-open-drawer.msft.png":::
   Abschnitt " **aufnahmeeinstellungen** "  
:::image-end:::  

### Deaktivieren von JavaScript-Beispielen  

Standardmäßig werden im **Haupt** Abschnitt einer Aufzeichnung detaillierte Aufruflisten von JavaScript-Funktionen angezeigt, die während der Aufzeichnung aufgerufen wurden.  So deaktivieren Sie diese Anruflisten:  

1.  Öffnen Sie das Menü " **aufnahmeeinstellungen** ".  Navigieren Sie zu [Aufzeichnung Einstellungen anzeigen](#show-recording-settings).  
1.  Aktivieren Sie das Kontrollkästchen **JavaScript-Beispiele deaktivieren** .  
1.  Nehmen Sie eine Aufzeichnung der Seite auf.  
    
Die folgenden zwei Abbildungen zeigen den Unterschied zwischen dem deaktivieren und Aktivieren von JavaScript-Beispielen.  Der **Haupt** Abschnitt der Aufzeichnung ist viel kürzer, wenn Sampling deaktiviert ist, da alle JavaScript-Aufruflisten ausgelassen werden.  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-on.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-on.msft.png":::
         Beispiel für eine Aufzeichnung, wenn JS-Beispiele deaktiviert sind  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off.msft.png":::
         Beispiel für eine Aufzeichnung, wenn JS-Beispiele aktiviert sind  
      :::image-end:::  
   :::column-end:::
:::row-end:::

### Drosseln des Netzwerks während der Aufzeichnung  

So Drosseln Sie das Netzwerk während der Aufzeichnung:  

1.  Öffnen Sie das Menü " **aufnahmeeinstellungen** ".  Navigieren Sie zu [Aufzeichnung Einstellungen anzeigen](#show-recording-settings).  
1.  Stellen Sie **Network** auf die gewünschte drosselungsebene ein.  
    
### Drosseln der CPU während der Aufzeichnung  

So Drosseln Sie die CPU während der Aufzeichnung:  

1.  Öffnen Sie das Menü " **aufnahmeeinstellungen** ".  Navigieren Sie zu [Aufzeichnung Einstellungen anzeigen](#show-recording-settings).  
1.  Setzen Sie die **CPU** auf das gewünschte Drosselungs Niveau.  
    
Die Drosselung ist relativ zu den Funktionen Ihres Computers.  Mit der Option " **2X verlangsamen** " wird beispielsweise die CPU zwei Mal langsamer als normal ausgeführt.  DevTools simulieren die CPUs von mobilen Geräten nicht wirklich, da sich die Architektur von mobilen Geräten stark von der von Desktops und Laptops unterscheidet.  

### Erweiterte Paint-Instrumentation aktivieren  

So zeigen Sie die detaillierte Farb Instrumentation an:  

1.  Öffnen Sie das Menü " **aufnahmeeinstellungen** ".  Navigieren Sie zu [Aufzeichnung Einstellungen anzeigen](#show-recording-settings).  
1.  Aktivieren Sie das Kontrollkästchen **Erweiterte Farb Instrumentation (langsam) aktivieren** .  

Wenn Sie wissen möchten, wie Sie mit den Paint-Informationen interagieren, navigieren Sie zu [Ansichtsebenen](#view-layers-information) , und [zeigen Sie Paint Profiler](#view-paint-profiler)an.  

## Speichern einer Aufzeichnung  

Wenn Sie eine Aufzeichnung speichern möchten, klicken Sie mit der rechten Maustaste, und wählen Sie **Profil speichern**aus.  

:::image type="complex" source="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off-save-profile.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off-save-profile.msft.png":::
   **Profil speichern**  
:::image-end:::  

## Laden einer Aufzeichnung  

Wenn Sie eine Aufzeichnung laden möchten, klicken Sie mit der rechten Maustaste, und wählen Sie **Profil laden**aus.  

:::image type="complex" source="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off-load-profile.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off-load-profile.msft.png":::
   **Profil laden**  
:::image-end:::  

## Löschen der vorherigen Aufzeichnung  

Nachdem Sie eine Aufzeichnung durchführen, drücken Sie die **Aufzeichnung löschen** \ ( ![ Symbol ' Aufzeichnung löschen ][ImageClearRecordingIcon] \), um die Aufzeichnung aus dem **Leistungs** Panel zu löschen.  

:::image type="complex" source="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off-clear-button.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off-clear-button.msft.png":::
   **Aufzeichnen löschen**  
:::image-end:::  

## Analysieren einer Leistungsaufzeichnung  

Nachdem Sie die Leistung der [Lauf Zeitaufzeichnung](#record-runtime-performance) oder die [Daten Satz Auslastung](#record-load-performance)aufgezeichnet haben, bietet der **Leistungs** Bereich viele Daten für die Analyse der Leistung von dem, was gerade geschehen ist.  

### Auswählen eines Teils einer Aufzeichnung  

Ziehen Sie den Mauszeiger über die **Übersicht** nach links oder rechts, um einen Teil der Aufzeichnung auszuwählen.  Die **Übersicht** ist der Abschnitt, in dem die **fps**-, **CPU**-und **net** -Diagramme enthalten sind.  

:::image type="complex" source="../media/evaluate-performance-performance-zoom-highlighted.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-performance-zoom-highlighted.msft.png":::
   Ziehen Sie den Mauszeiger über die **Übersicht** , um die Ansicht zu vergrößern  
:::image-end:::  

So wählen Sie einen Teil über die Tastatur aus:  

1.  Klicken Sie auf den Hintergrund des **Haupt** Abschnitts oder eines der Abschnitte daneben, wie **Interaktionen**, **Netzwerk**oder **GPU**.  Dieser Tastatur Workflow funktioniert nur, wenn einer dieser Abschnitte den Fokus hat.  
1.  Verwenden Sie `W` die `A` Tasten,, `S` , `D` um Sie zu vergrößern, nach Links zu verschieben, zu verkleinern und nach rechts zu verschieben.  

So wählen Sie einen Teil mithilfe eines Trackpads aus:  

1.  Zeigen Sie mit der Maus auf den Abschnitt " **Übersicht** " oder den Abschnitt " **Details** ".  Der Abschnitt " **Übersicht** " ist der Bereich, in dem die **fps**-, **CPU**-und **net** -Diagramme enthalten sind.  Der Abschnitt **Details** ist der Bereich, der den **Haupt** Abschnitt, den Abschnitt **Interaktionen** und so weiter enthält.  
1.  Wischen Sie mit zwei Fingern nach oben, um es zu verkleinern, wischen Sie nach links, wischen Sie nach unten, um die Ansicht zu vergrößern, und wischen Sie nach rechts, um nach rechts zu wechseln  

Wenn Sie im **Haupt** Abschnitt oder in einem der Nachbarn in einem langen Flammen Diagramm Scrollen möchten, klicken und halten Sie beim Ziehen nach oben und unten.  Ziehen Sie nach links und rechts, um zu verschieben, welcher Teil der Aufzeichnung markiert ist.  

### Suchaktivitäten  

Wählen Sie `Control` + `F` \ (Windows, Linux \) oder `Command` + `F` \ (macOS \) aus, um das Suchfeld unten im **Leistungs** Bereich zu öffnen.  

:::image type="complex" source="../media/evaluate-performance-performance-search-regex.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-performance-search-regex.msft.png":::
   Suchfeld  
:::image-end:::  

So navigieren Sie in Aktivitäten, die Ihrer Abfrage entsprechen:  

*   Verwenden Sie die Schaltflächen **vorherige** \ ( ![ vorherige ][ImagePreviousIcon] \) und **nächste** \ ( ![ weiter \ ][ImageNextIcon] ).  
*   Wählen Sie aus `Shift` + `Enter` , um das vorherige auszuwählen, oder `Enter` Wählen Sie das nächste aus.  

So ändern Sie die Abfrageeinstellungen:  

*   Drücken Sie **groß** -/Kleinschreibung ![ beachten \ (Groß-/Kleinschreibung ][ImageSearchCaseIcon] beachten \), damit die Abfrage Groß-/Kleinschreibung berücksichtigt.  
*   Drücken Sie **Regex** \ ( ![ Regex ][ImageSearchRegexIcon] \), um einen regulären Ausdruck in Ihrer Abfrage zu verwenden.  

Wenn Sie das Suchfeld ausblenden möchten, drücken Sie **Abbrechen**.  

### Hauptthread Aktivität anzeigen  

Verwenden Sie den **Haupt** Abschnitt, um die Aktivitäten anzuzeigen, die im Hauptthread der Seite aufgetreten sind.  

:::image type="complex" source="../media/evaluate-performance-performance-main-zoomed.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-performance-main-zoomed.msft.png":::
   Der **Haupt** Abschnitt  
:::image-end:::  

Klicken Sie auf ein Ereignis, um weitere Informationen dazu auf der Registerkarte " **Zusammenfassung** " anzuzeigen.  DevTools skizziert das ausgewählte Ereignis.  

:::image type="complex" source="../media/evaluate-performance-performance-summary-me.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-performance-summary-me.msft.png":::
   Weitere Informationen zur `anonymous` Funktion auf der Registerkarte " **Zusammenfassung** "  
:::image-end:::  

DevTools stellt die Hauptthread Aktivität mit einem Flammen Diagramm dar.  Die x-Achse stellt die Aufzeichnung über einen Zeitraum dar.  Die y-Achse steht für die Aufrufliste.  Die Ereignisse im Vordergrund führen zu den darunter liegenden Ereignissen.  

:::image type="complex" source="../media/evaluate-performance-performance-main-flame-chart.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-performance-main-flame-chart.msft.png":::
   Ein Flammen Diagramm  
:::image-end:::  

In der vorherigen Abbildung hat ein `click` Ereignis eine `Function Call` in `activitytabs.js` on Zeile 53 verursacht.  Unten `Function Call` sehen Sie, dass eine anonyme Funktion aufgerufen wurde.  Die anonyme Funktion mit dem Namen, die aufgerufen `a` `wait` wird `Minor GC` .  

DevTools weist Skripten zufällige Farben zu.  In der vorhergehenden Abbildung sind Funktionsaufrufe eines Skripts farbig hellgrün.  Anrufe von einem anderen Skript sind farbig beige.  Das dunklere Gelb steht für Skriptaktivitäten, und das Purple-Ereignis stellt die Rendering-Aktivität dar.  Diese dunkelgelben und violetten Ereignisse sind für alle Aufzeichnungen konsistent.  

Navigieren Sie zum [Deaktivieren von JavaScript-Beispielen](#disable-javascript-samples) , wenn Sie den detaillierten Flammen Diagramm von JavaScript-anrufen ausblenden möchten.  Wenn js-Beispiele deaktiviert sind, sehen Sie nur Ereignisse auf höherer Ebene, wie `Event: click` und `Function Call` aus der vorherigen Abbildung.  

### Anzeigen von Aktivitäten in einer Tabelle  

Nach dem Aufzeichnen einer Seite müssen Sie sich nicht nur auf den **Haupt** Abschnitt verlassen, um Aktivitäten zu analysieren.  DevTools stellt auch drei tabellarische Ansichten zum Analysieren von Aktivitäten bereit.  Jede Ansicht gibt Ihnen eine andere Perspektive auf die Aktivitäten:  

*   Wenn Sie die Stammaktivitäten anzeigen möchten, die die meiste Arbeit verursachen, verwenden Sie [die Registerkarte anrufstruktur](#the-call-tree-tab).  
*   Wenn Sie die Aktivitäten anzeigen möchten, bei denen die meiste Zeit direkt ausgegeben wurde, verwenden Sie [die Registerkarte Bottom-Up](#the-bottom-up-tab).  
*   Wenn Sie die Aktivitäten in der Reihenfolge anzeigen möchten, in der Sie während der Aufzeichnung aufgetreten sind, verwenden Sie [die Registerkarte Ereignisprotokoll](#the-event-log-tab).  
    
> [!NOTE]
> Die nächsten drei Abschnitte beziehen sich alle auf die gleiche Demo.  Führen Sie die Demo selbst auf der [Registerkarte Activity Tabs][ActivityTabsDemo]aus.  

#### Stammaktivitäten  

Im folgenden finden Sie eine Erläuterung des Konzepts der **Stammaktivitäten** , das auf der Registerkarte " **anrufstruktur** ", " **Bottom-up-** Registerkarte" und " **Ereignisprotokoll** Abschnitte" erwähnt wird.  

Stammaktivitäten sind solche, die dazu führen, dass der Browser einige Aufgaben ausführen kann.  Wenn Sie beispielsweise auf eine Seite klicken, löst der Browser eine `Event` Aktivität als Stammaktivität aus.  , Die `Event` dazu führen können, dass ein Handler ausgeführt wird usw.  

Im Flammen Diagramm des **Haupt** Abschnitts befinden sich die Stammaktivitäten am oberen Rand des Diagramms.  In den Registerkarten " **anrufstruktur** " und " **Ereignisprotokoll** " sind Stammaktivitäten die Elemente der obersten Ebene.  

Navigieren Sie zur [Registerkarte anrufstruktur](#the-call-tree-tab) , um ein Beispiel für Stammaktivitäten anzuzeigen.  

#### Die Registerkarte "anrufstruktur"  

Verwenden Sie die Registerkarte **anrufstruktur** , um anzuzeigen, welche [Stammaktivitäten](#root-activities) die meiste Arbeit verursachen.  

Die Registerkarte " **anrufstruktur** " zeigt nur Aktivitäten während des ausgewählten Teils der Aufzeichnung an.  Navigieren [Sie zum Auswählen eines Teils einer Aufzeichnung](#select-a-portion-of-a-recording) , um zu erfahren, wie Sie Abschnitte auswählen.  

:::image type="complex" source="../media/evaluate-performance-performance-call-tree.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-performance-call-tree.msft.png":::
   Die Registerkarte " **anrufstruktur** "  
:::image-end:::  

In der vorhergehenden Abbildung sind die Elemente der obersten Ebene in der Spalte **Aktivität** , beispielsweise `Evaluate Script` und Stammaktivitäten, zu finden `Parse HTML` .  Die Schachtelung stellt die Aufrufliste dar.  Beispielsweise in der vorherigen Abbildung, die `Parse HTML` verursacht hat, `Evaluate Script` `Compile Script` und `(anonymous)` .  

**Self time** steht für die in dieser Aktivität direkt verbrachte Zeit.  **Gesamtzeit** stellt die Zeit dar, die in dieser Aktivität oder einem der untergeordneten Elemente aufgewendet wurde.  

Wählen Sie **selbst Zeit**, **Gesamtzeit**oder **Aktivität** aus, um die Tabelle nach dieser Spalte zu sortieren.  

Verwenden Sie das Textfeld **Filtern** , um Ereignisse nach Aktivitätsname zu filtern.  

Standardmäßig ist das Menü **Gruppierung** auf **keine Gruppierung**eingestellt.  Verwenden Sie das Menü **Gruppierung** , um die aktivitätstabelle auf der Grundlage verschiedener Kriterien zu sortieren.  

Wählen Sie den **schwersten Stapel anzeigen** aus ![ , um ][ImageShowHeaviestStackIcon] eine andere Tabelle rechts neben der **Aktivitäts** Tabelle anzuzeigen.  Klicken Sie auf eine Aktivität, um die **schwerste Stapel** Tabelle aufzufüllen.  Die **schwerste Stapel** Tabelle zeigt, welche untergeordneten Elemente der ausgewählten Aktivität am längsten ausgeführt wurden.  

#### Die Registerkarte "Bottom-Up"  

Verwenden Sie die Registerkarte " **Bottom-up** ", um anzuzeigen, welche Aktivitäten die meiste Zeit im Aggregat Direktaufnahmen.  

Auf der Registerkarte **Bottom-up** werden nur Aktivitäten während des ausgewählten Teils der Aufzeichnung angezeigt.  Navigieren [Sie zum Auswählen eines Teils einer Aufzeichnung](#select-a-portion-of-a-recording) , um zu erfahren, wie Sie Abschnitte auswählen.  

:::image type="complex" source="../media/evaluate-performance-performance-bottoms-up.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-performance-bottoms-up.msft.png":::
   Die Registerkarte " **Bottom-up** "  
:::image-end:::  

Navigieren Sie im **Haupt** Abschnitt Flammen Diagramm der vorhergehenden Abbildung zu dieser fast nahezu alle Zeit verbrachte Ausführung `Parse HTML` .  Die oberste Aktivität auf der Registerkarte " **Bottom-up** " der vorherigen Abbildung ist `Parse HTML` .  <!--In the flame chart of the previous figure, the yellow below the calls to `wait` are actually thousands of `Minor GC` calls.  -->  Navigieren Sie auf der Registerkarte **Bottom-up** wird die nächst teuerste Aktivität `Layout` angezeigt.  

Die Spalte **selbst Zeit** stellt die aggregierte Zeit dar, die direkt in dieser Aktivität für alle Vorkommen aufgewendet wurde.  

Die Spalte " **Gesamtzeit** " stellt die aggregierte Zeit dar, die in dieser Aktivität oder einem der untergeordneten Elemente aufgewendet wurde.  

#### Die Registerkarte "Ereignisprotokoll"  

Verwenden Sie die Registerkarte **Ereignisprotokoll** , um Aktivitäten in der Reihenfolge anzuzeigen, in der Sie während der Aufzeichnung aufgetreten sind.  

Die Registerkarte **Ereignisprotokoll** zeigt nur Aktivitäten während des ausgewählten Teils der Aufzeichnung an.  Navigieren [Sie zum Auswählen eines Teils einer Aufzeichnung](#select-a-portion-of-a-recording) , um zu erfahren, wie Sie Abschnitte auswählen.  

:::image type="complex" source="../media/evaluate-performance-performance-event-log.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-performance-event-log.msft.png":::
   Die Registerkarte " **Ereignisprotokoll** "  
:::image-end:::  

Die Spalte **Anfangszeit** steht für den Punkt, an dem die Aktivität gestartet wurde, relativ zum Anfang der Aufzeichnung.  Beispielsweise bedeutet die Startzeit `175.7 ms` für das ausgewählte Element in der vorherigen Abbildung, dass die Aktivität nach Beginn der Aufzeichnung 175,7 ms gestartet hat.  

Die Spalte **selbst Zeit** stellt die Zeit dar, die direkt in dieser Aktivität verbracht wurde.  

Die Spalten **Gesamtzeit** stellt die Zeit dar, die direkt in dieser Aktivität oder in einem der untergeordneten Elemente aufgewendet wurde.  

Wählen Sie **Start Zeit**, **selbst Zeit**oder **Gesamtzeit** aus, um die Tabelle nach dieser Spalte zu sortieren.

Verwenden Sie das Textfeld **Filtern** , um Aktivitäten nach Namen zu filtern.  

Verwenden Sie das Menü " **Dauer** ", um alle Aktivitäten zu filtern, die weniger als 1 MS oder 15 MS dauerte.  Standardmäßig ist das Menü **Dauer** auf **alle**eingestellt, was bedeutet, dass alle Aktivitäten angezeigt werden.  

Deaktivieren Sie die Kontrollkästchen **Lade**-, **Skripting**-, **Rendering**-oder **Painting** , um alle Aktivitäten aus diesen Kategorien zu filtern.  

### Anzeigen der GPU-Aktivität  

Zeigen Sie die GPU-Aktivität im Abschnitt **GPU** an.  

:::image type="complex" source="../media/evaluate-performance-performance-gpu-zoomed.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-performance-gpu-zoomed.msft.png":::
   Der **GPU** -Abschnitt  
:::image-end:::  

### Raster Aktivität anzeigen  

Raster Aktivitäten im **Raster** Abschnitt anzeigen  

:::image type="complex" source="../media/evaluate-performance-performance-raster.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-performance-raster.msft.png":::
   Der **Raster** Abschnitt  
:::image-end:::  

### Anzeigen von Interaktionen  

Verwenden Sie den Abschnitt **Interaktionen** , um Benutzerinteraktionen zu suchen und zu analysieren, die während der Aufzeichnung aufgetreten sind.  

:::image type="complex" source="../media/evaluate-performance-performance-interactions-animation.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-performance-interactions-animation.msft.png":::
   Abschnitt " **Interaktionen** "  
:::image-end:::  

Eine rote Zeile am unteren Rand einer Interaktion stellt die Zeit dar, die auf den Hauptthread wartet.  

Klicken Sie auf eine Interaktion, um weitere Informationen dazu auf der Registerkarte **Zusammenfassung** anzuzeigen.  

### Analysieren von Frames pro Sekunde (fps)  

DevTools bietet zahlreiche Möglichkeiten zum Analysieren von Frames pro Sekunde:  

*   Verwenden Sie [das FPS-Diagramm](#the-fps-chart) , um einen Überblick über fps über die Dauer der Aufzeichnung zu erhalten.  
*   Verwenden Sie [den Abschnitt Frames](#the-frames-section) , um anzuzeigen, wie lange ein bestimmter Frame aufgenommen wurde.  
*   Verwenden Sie das **fps-Messgerät** für eine echt Zeitschätzung von fps während der Ausführung der Seite.  Navigieren Sie [in Echtzeit mit dem fps-Messgerät zu Anzeige Frames pro Sekunde](#view-frames-per-second-in-realtime-with-the-fps-meter).  
    
#### Das fps-Diagramm  

Das **fps** -Diagramm bietet eine Übersicht über die Framerate für die Dauer einer Aufzeichnung.  Je höher die grüne Leiste, desto besser die Framerate.  

Eine rote Leiste oberhalb des **fps** -Diagramms ist eine Warnung, dass die Framerate so gering war, dass Sie möglicherweise die Benutzererfahrung beeinträchtigte.  

:::image type="complex" source="../media/evaluate-performance-performance-fps-highlight.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-performance-fps-highlight.msft.png":::
   Das **fps** -Diagramm  
:::image-end:::  

#### Der Abschnitt "Frames"  

Im Abschnitt **Frames** erfahren Sie genau, wie lange ein bestimmter Frame aufgenommen wurde.  

Zeigen Sie mit der Maus auf einen Frame, um eine QuickInfo mit weiteren Informationen dazu anzuzeigen.  

:::image type="complex" source="../media/evaluate-performance-performance-frames-hover.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-performance-frames-hover.msft.png":::
   Zeigen Sie mit der Maus auf einen Frame  
:::image-end:::  

Klicken Sie auf einen Frame, um auf der Registerkarte **Zusammenfassung** noch weitere Informationen zu dem Frame anzuzeigen.  DevTools konturiert den markierten Frame in blau.  

:::image type="complex" source="../media/evaluate-performance-performance-frames-summary.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-performance-frames-summary.msft.png":::
   Anzeigen eines Frames auf der Registerkarte " **Zusammenfassung** "  
:::image-end:::  

### Anzeigen von Netzwerkanforderungen  

Erweitern Sie den Abschnitt **Netzwerk** , um einen Wasserfall von Netzwerkanforderungen anzuzeigen, die während der Aufzeichnung aufgetreten sind.  

:::image type="complex" source="../media/evaluate-performance-performance-network.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-performance-network.msft.png":::
   Der Abschnitt " **Netzwerk** "  
:::image-end:::  

Anforderungen werden wie folgt farblich gekennzeichnet:  

*   HTML: blau  
*   CSS: lila  
*   JS: gelb  
*   Bilder: grün  
    
Klicken Sie auf eine Anfrage, um weitere Informationen dazu auf der Registerkarte " **Zusammenfassung** " anzuzeigen.  In der vorhergehenden Abbildung werden beispielsweise auf der Registerkarte **Zusammenfassung** Weitere Informationen zu der im Abschnitt **Netzwerk** ausgewählten blauen Anforderung angezeigt.  

Ein dunkelblaues Quadrat in der oberen linken Ecke einer Anforderung bedeutet, dass es sich um eine Anforderung mit höherer Priorität handelt.  Ein helleres blaues Quadrat bedeutet niedrigere Priorität.  In der vorhergehenden Abbildung ist beispielsweise die blaue, ausgewählte Anforderung eine höhere Priorität, und die grüne darunter hat eine niedrigere Priorität.  

In der ersten der folgenden Zahlen wird die Anforderung für `www.bing.com` durch eine Zeile auf der linken Seite, eine Leiste in der Mitte mit einem dunklen Teil und einem hellen Teil sowie eine Zeile auf der rechten Seite dargestellt.  In der zweiten der folgenden Abbildungen wird die entsprechende Darstellung der gleichen Anforderung auf der Registerkarte **Anzeige** Dauer im **Netzwerk** Fenster angezeigt.  Hier sehen Sie, wie diese beiden Darstellungen einander zugeordnet sind:

*   Die linke Zeile ist alles bis zur `Connection Start` Gruppe von Ereignissen inklusive.  Mit anderen Worten: Es ist alles vor `Request Sent` , exklusiv.  
*   Der helle Bereich der Leiste ist `Request Sent` und `Waiting (TTFB)` .  
*   Der dunkle Teil der Leiste ist `Content Download` .  
*   Die richtige Zeile ist im Wesentlichen die Zeit, die auf den Hauptthread wartet.  Diese wird auf der Registerkarte **Anzeige** Dauer nicht dargestellt.  
    
:::row:::
   :::column span="":::
      :::image type="complex" source="../media/evaluate-performance-bing-performance-network.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-bing-performance-network.msft.png":::
         Die Zeile-Balken-Darstellung der `www.bing.com` Anforderung  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/evaluate-performance-bing-network-timing.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-bing-network-timing.msft.png":::
         Das **Netzwerk** Tool  
::: Image-End:::  
   :::column-end:::
:::row-end:::

### Anzeigen von Speicher Metriken  

Aktivieren Sie das Kontrollkästchen **Speicher** , um Speicher Metriken aus der letzten Aufzeichnung anzuzeigen.  

:::image type="complex" source="../media/evaluate-performance-performance-memory-highlight.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-performance-memory-highlight.msft.png":::
   Das Kontrollkästchen " **Speicher** "  
:::image-end:::  

DevTools zeigt ein neues **Speicher** Diagramm über der Registerkarte " **Zusammenfassung** " an.  Es gibt auch ein neues Diagramm unter dem **Netz** Diagramm, das als **Heap**bezeichnet wird.  Das **Heap** Diagramm bietet dieselben Informationen wie die **js-heaplinie** im **Speicher** Diagramm.  

:::image type="complex" source="../media/evaluate-performance-performance-memory-chart.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-performance-memory-chart.msft.png":::
   Speicher Metriken  
:::image-end:::  

Die farbigen Linien auf dem Diagramm werden den farbigen Kontrollkästchen oberhalb des Diagramms zugeordnet.  
Deaktivieren Sie ein Kontrollkästchen, um diese Kategorie aus dem Diagramm auszublenden.  

Das Diagramm zeigt nur den Bereich der Aufzeichnung an, der aktuell markiert ist.  In der vorhergehenden Abbildung zeigt das **Speicher** Diagramm beispielsweise nur die Speicherauslastung von der 400 MS-Marke bis zum 1750 MS Mark.  

### Anzeigen der Dauer eines Teils einer Aufzeichnung  

Wenn Sie einen Abschnitt wie " **Netzwerk** " oder " **Main**" analysieren, benötigen Sie manchmal eine genauere Einschätzung, wie lange bestimmte Ereignisse dauerte.  Halten `Shift` , klicken und halten Sie, und ziehen Sie nach links oder rechts, um einen Teil der Aufzeichnung auszuwählen.  Am unteren Rand Ihrer Auswahl zeigt devtools an, wie lange dieser Teil dauerte.  

:::image type="complex" source="../media/evaluate-performance-performance-main-duration.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-performance-main-duration.msft.png":::
   Anzeigen der Dauer eines Teils einer Aufzeichnung  
:::image-end:::  

### Anzeigen eines Screenshots  

Navigieren Sie zu [Capture Screenshots während der Aufzeichnung](#capture-screenshots-while-recording) , um zu erfahren, wie Screenshots aktiviert werden.  

Zeigen Sie mit der Maus auf die **Übersicht** , um einen Screenshot zu sehen, wie die Seite während dieses Moments der Aufzeichnung aussah.  Die **Übersicht** ist der Abschnitt mit den Diagrammen **CPU**, **fps**und **net** .  

:::image type="complex" source="../media/evaluate-performance-performance-screenshots-hover.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-performance-screenshots-hover.msft.png":::
   Anzeigen eines Screenshots  
:::image-end:::  

Sie können Screenshots auch anzeigen, indem Sie im Abschnitt **Frames** auf einen Frame klicken.  DevTools zeigt eine kleine Version des Screenshots auf der Registerkarte " **Zusammenfassung** " an.  

:::image type="complex" source="../media/evaluate-performance-performance-summary-preview.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-performance-summary-preview.msft.png":::
   Anzeigen eines Screenshots auf der Registerkarte " **Zusammenfassung** "  
:::image-end:::  

Klicken Sie auf der Registerkarte **Zusammenfassung** auf die Miniaturansicht, um den Screenshot zu vergrößern.  

:::image type="complex" source="../media/evaluate-performance-performance-summary-preview-select.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-performance-summary-preview-select.msft.png":::
   Vergrößern eines Screenshots über die Registerkarte " **Zusammenfassung** "  
:::image-end:::  

### Informationen zu Layern anzeigen  

So zeigen Sie erweiterte Folieninformationen zu einem Frame an:  

1.  [Aktivieren der erweiterten Farb Instrumentation](#enable-advanced-paint-instrumentation)  
1.  Wählen Sie im Abschnitt **Frames** einen Frame aus.  DevTools zeigt Informationen zu den Ebenen auf der Registerkarte "neue **Ebenen** " neben der Registerkarte " **Ereignisprotokoll** " an.  
    
    :::image type="complex" source="../media/evaluate-performance-layers-all.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-layers-all.msft.png":::
       Der Bereich " **Ebenen** "  
    :::image-end:::  
    
Zeigen Sie mit der Maus auf eine Ebene, um Sie im Diagramm hervorzuheben.  

:::image type="complex" source="../media/evaluate-performance-performance-frames-document-nav-bar-highlighted.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-performance-frames-document-nav-bar-highlighted.msft.png":::
   Markieren eines Layers  
:::image-end:::  

So verschieben Sie das Diagramm:  

*   Wählen Sie **Schwenkmodus** \ ( ![ Schwenkmodus ][ImagePanModeIcon] \) aus, um entlang der X-und Y-Achse zu navigieren.  
*   Wählen Sie **Rotationsmodus** \ ( ![ Rotate Mode ][ImageRotateModeIcon] \) aus, um sich entlang der Z-Achse zu drehen.  
*   Wählen Sie **Transform zurück** setzen \ ( ![ Transform zurücksetzen ][ImageResetTransformIcon] \) aus, um das Diagramm auf die ursprüngliche Position zurückzusetzen.  
    
### Anzeigen des Paint-Profilers  

So zeigen Sie erweiterte Informationen zu einem Paint-Ereignis an:  

1.  [Aktivieren der erweiterten Farb Instrumentation](#enable-advanced-paint-instrumentation)  
1.  Wählen Sie im **Haupt** Abschnitt ein **Paint** -Ereignis aus.  
    
    :::image type="complex" source="../media/evaluate-performance-paint-profiler.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-paint-profiler.msft.png":::
       Die Registerkarte " **Paint-Profiler** "  
    :::image-end:::  
    
## Analysieren der Renderingleistung mit der Registerkarte "Rendern"  

Verwenden Sie die Features der Registerkarte " **Rendern** ", um die Renderingleistung Ihrer Seite zu visualisieren.  

So öffnen Sie die Registerkarte " **Rendering** ":  

1.  [Öffnen des Befehlsmenüs][DevToolsCommandMenu]  
1.  Beginnen `Rendering` Sie mit der Eingabe, und wählen Sie aus `Show Rendering` .  DevTools zeigt die Registerkarte " **Rendering** " am unteren Rand des devtools-Fensters an.  
    
    :::image type="complex" source="../media/evaluate-performance-console-drawer-rendering.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-console-drawer-rendering.msft.png":::
       Die Registerkarte " **Rendern** "  
    :::image-end:::  
    
### Anzeigen von Frames pro Sekunde in Echtzeit mit dem fps-Messgerät  

Das **fps-Messgerät** ist ein Overlay, das in der oberen rechten Ecke des Viewports angezeigt wird.  Bei der Ausführung der Seite wird eine Echtzeit-Schätzung von fps bereitgestellt.  So öffnen Sie das **fps-Messgerät**:  

1.  Öffnen Sie die Registerkarte **Rendering** .  Na [Analysieren Sie die Renderingleistung mit der Registerkarte "Rendering"](#analyze-rendering-performance-with-the-rendering-tab).  
1.  Aktivieren Sie das Kontrollkästchen **FPS-Meter** .  
    
    :::image type="complex" source="../media/evaluate-performance-jank-console-rendering-frame-rate.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-jank-console-rendering-frame-rate.msft.png":::
       Das **fps-Messgerät**  
    :::image-end:::  
    
### Anzeigen von Zeichnungs Ereignissen in Echtzeit mit Farb blinken  

Verwenden Sie das Farb blinken, um eine Echtzeitansicht aller Paint-Ereignisse auf der Seite zu erhalten.  Jedes Mal, wenn ein Teil der Seite neu gestrichen wird, wird der Abschnitt in devtools in grün umrissen.  

So aktivieren Sie die Farb Blinkfunktion:  

1.  Öffnen Sie die Registerkarte **Rendering** .  Navigieren Sie zur [Analyse der Renderingleistung mithilfe der Registerkarte Rendern](#analyze-rendering-performance-with-the-rendering-tab).  
1.  Aktivieren Sie das Kontrollkästchen " **Farbe blinkt** ".  
    
    :::image type="complex" source="../media/evaluate-performance-jank-console-rendering-paint-flashing.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-jank-console-rendering-paint-flashing.msft.png":::
       **Malen blinkt**  
    :::image-end:::  
    
### Anzeigen einer Überlagerung von Ebenen mit Ebenen Rändern  

Verwenden Sie **Layer-Rahmen** , um eine Überlagerung von Layer-Rändern und Kacheln oben auf der Seite anzuzeigen.  

So aktivieren Sie Layer-Rahmen:  

1.  Öffnen Sie die Registerkarte **Rendering** .  Navigieren Sie zur [Analyse der Renderingleistung mithilfe der Registerkarte Rendern](#analyze-rendering-performance-with-the-rendering-tab).  
1.  Aktivieren Sie das Kontrollkästchen **Layer-Rahmen** .  
    
    :::image type="complex" source="../media/evaluate-performance-devtools-console-rendering-layer-borders.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-devtools-console-rendering-layer-borders.msft.png":::
       **Folienrahmen**  
    :::image-end:::  
    
Navigieren Sie zu den Kommentaren in [debug_colors. CC][ChromiumDebugColors] , um eine Erläuterung der Farbcodierungen anzuzeigen.  

### Suchen von Scroll-Leistungsproblemen in Echtzeit  

Verwenden Sie Leistungsprobleme beim Scrollen, um Elemente der Seite zu identifizieren, die Ereignislistener in Bezug auf den Bildlauf aufweisen, die die Leistung der Seite beeinträchtigen können.  
DevTools beschreibt die potenziell problematischen Elemente in Teal.  

So zeigen Sie Bild Lauf Leistungsprobleme an:  

1.  Öffnen Sie die Registerkarte **Rendering** .  Navigieren Sie zur [Analyse der Renderingleistung mithilfe der Registerkarte Rendern](#analyze-rendering-performance-with-the-rendering-tab).  
1.  Aktivieren Sie das Kontrollkästchen **Scrolling Performance Issues** .  
    
    :::image type="complex" source="../media/evaluate-performance-bing-console-drawer-rendering-scrolling-performance-issues.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-bing-console-drawer-rendering-scrolling-performance-issues.msft.png":::
       **Probleme mit der Bildlaufleistung** deuten darauf hin, dass nicht-Layer-Viewport-abhängige Objekte die Bildlaufleistung beeinträchtigen können.  
    :::image-end:::  
    
## Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageCaptureSettingsIcon]: ../media/capture-settings-icon.msft.png  
[ImageClearRecordingIcon]: ../media/clear-recording-icon.msft.png  
[ImageCollectGarbageIcon]: ../media/collect-garbage-icon.msft.png  
[ImageNextIcon]: ../media/next-icon.msft.png  
[ImagePanModeIcon]: ../media/pan-mode-icon.msft.png  
[ImagePreviousIcon]: ../media/previous-icon.msft.png  
[ImageRecordIcon]: ../media/record-icon.msft.png
[ImageRefreshPageIcon]: ../media/refresh-page-icon.msft.png  
[ImageResetTransformIcon]: ../media/reset-transform-icon.msft.png  
[ImageRotateModeIcon]: ../media/rotate-mode-icon.msft.png  
[ImageSearchCaseIcon]: ../media/search-case-icon.msft.png  
[ImageSearchRegexIcon]: ../media/search-regex-icon.msft.png  
[ImageShowHeaviestStackIcon]: ../media/show-heaviest-stack-icon.msft.png  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium.md "Microsoft Edge (Chrom)-Entwicklertools | Microsoft docs"  
[DevToolsCommandMenu]: ../command-menu/index.md#open-the-command-menu "Öffnen des Befehlsmenüs – Ausführen von Befehlen mit dem Befehlsmenü von Microsoft Edge devtools | Microsoft docs"  
[DevtoolsEvaluatePerformanceGettingStarted]: ./index.md "Erste Schritte mit der Analyse der Laufzeitleistung | Microsoft docs"  

[ActivityTabsDemo]: https://microsoft-edge-chromium-devtools.glitch.me/perf/activitytabs.html "Demo für Aktivitäts Registerkarten | Glitch"  

[ChromiumDebugColors]: https://cs.chromium.org/chromium/src/cc/debug/debug_colors.cc "debug_colors. CC-Code Suche"  

> [!NOTE]
> Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.  
> Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/evaluate-performance/reference) und wird von [Kayce Basken][KayceBasques] (Technical Writer, Chrome devtools \ & Lighthouse \) erstellt.  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
