---
title: Referenz zur Leistungsanalyse
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/29/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Web-Entwicklung, F12-Tools, devtools
ms.openlocfilehash: acd6e3e68f89096cf80c08f0d0c3430ab31eaec1
ms.sourcegitcommit: 50991a04c18283a8890ae33fcc3491c0476c7684
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/30/2020
ms.locfileid: "10611748"
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

Eine Anleitung zum Analysieren der Leistung einer Seite mit [Microsoft Edge devtools][MicrosoftEdgeDevTools]finden Sie unter [Erste Schritte mit der Analyse der Laufzeitleistung][DevtoolsEvaluatePerformanceGettingStarted] .  

## Aufzeichnen der Leistung   

### Aufzeichnen der Laufzeitleistung   

Zeichnen Sie die Laufzeitleistung auf, wenn Sie die Leistung einer Seite während der Ausführung analysieren möchten, anstatt Sie zu laden.  

1.  Wechseln Sie zu der Seite, die Sie analysieren möchten.  
1.  Klicken Sie in devtools auf die Registerkarte **Leistung** .  
1.  Klicken Sie auf **Datensatz** aufzeichnen ![ ][ImageRecordIcon] .  
    
    > ##### Abbildung1  
    > **Record**  
    > ![Record][ImageRecord]  

1.  Interagieren Sie mit der Seite.  DevTools zeichnet alle Seiten Aktivitäten auf, die durch ihre Interaktionen entstehen.  
1.  Klicken Sie erneut auf **aufzeichnen** , oder klicken Sie auf **Beenden** , um die Aufzeichnung zu beenden.  

### Aufzeichnen der Ladeleistung   

Zeichnen Sie die Ladeleistung auf, wenn Sie die Leistung einer Seite während des Ladens analysieren möchten, anstatt Sie zu starten.  

1.  Wechseln Sie zu der Seite, die Sie analysieren möchten.  
1.  Öffnen Sie das **Leistungs** Panel von devtools.  
1.  Klicken **Sie auf Seite aktualisieren** ![ ][ImageRefreshPageIcon] .  DevTools zeichnet Leistungs Metriken auf, während die Seite aktualisiert wird, und stoppt dann die Aufzeichnung ein paar Sekunden nach Abschluss der Auslastung automatisch.  
    
    > ##### Abbildung2  
    > **Seite aktualisieren**  
    > ![Seite aktualisieren][ImageRefreshPage]  

DevTools zoomt automatisch auf den Teil der Aufzeichnung, in dem die meisten Aktivitäten aufgetreten sind.  

> ##### Abbildung 3  
> Laden einer Seite  
> ![Laden einer Seite][ImageLoadRecording]  

### Aufzeichnen von Screenshots während der Aufzeichnung   

Aktivieren Sie das Kontrollkästchen **Screenshots** , um einen Screenshot jedes Frames während der Aufzeichnung zu erfassen.  

> ##### Abbildung4  
> Das Kontrollkästchen " **Screenshots** "  
> ![Das Kontrollkästchen "Screenshots"][ImageScreenshots]  

Informationen zum interagieren mit Screenshots finden Sie unter [Anzeigen eines](#view-a-screenshot) Screenshots.  

### Erzwingen der Garbage Collection während der Aufzeichnung   

Klicken Sie während der Aufzeichnung einer Seite auf Garbage Collect Garbage Collection **sammeln** , ![ ][ImageCollectGarbageIcon] um die Garbage Collection zu erzwingen.  

> ##### Abbildung5  
> Garbage Collection  
> ![Garbage Collection][ImageCollectGarbage]  

### Aufzeichnungseinstellungen anzeigen   

Klicken Sie auf Einstellungen für Aufnahme **Einstellungen** ![ ][ImageCaptureSettingsIcon] , um weitere Einstellungen anzuzeigen, die sich auf die Darstellung von Leistungs Aufzeichnungen in devtools beziehen.  

> ##### Abbildung6  
> Abschnitt " **aufnahmeeinstellungen** "  
> ![Abschnitt "Aufnahmeeinstellungen"][ImageCaptureSettings]  

### Deaktivieren von JavaScript-Beispielen   

Standardmäßig werden im **Haupt** Abschnitt einer Aufzeichnung detaillierte Aufruflisten von JavaScript-Funktionen angezeigt, die während der Aufzeichnung aufgerufen wurden.  So deaktivieren Sie diese Anruflisten:  

1.  Öffnen Sie das Menü " **aufnahmeeinstellungen** ".  Weitere Informationen finden Sie unter [Anzeigen von aufnahmeeinstellungen](#show-recording-settings).  
1.  Aktivieren Sie das Kontrollkästchen **JavaScript-Beispiele deaktivieren** .  
1.  Nehmen Sie eine Aufzeichnung der Seite auf.  

[Abbildung 7](#figure-7) und [Abbildung 8](#figure-8) zeigen den Unterschied zwischen dem deaktivieren und Aktivieren von JavaScript-Beispielen.  Der **Haupt** Abschnitt der Aufzeichnung ist viel kürzer, wenn Sampling deaktiviert ist, da alle JavaScript-Aufruflisten ausgelassen werden.  

> ##### Abbildung7  
> Beispiel für eine Aufzeichnung, wenn JS-Beispiele deaktiviert sind  
> ![Beispiel für eine Aufzeichnung, wenn JS-Beispiele deaktiviert sind][ImageJSSamplesDisabled]  

> ##### Abbildung8  
> Beispiel für eine Aufzeichnung, wenn JS-Beispiele aktiviert sind  
> ![Beispiel für eine Aufzeichnung, wenn JS-Beispiele aktiviert sind][ImageJSSamplesEnabled]  

### Drosseln des Netzwerks während der Aufzeichnung   

So Drosseln Sie das Netzwerk während der Aufzeichnung:  

1.  Öffnen Sie das Menü " **aufnahmeeinstellungen** ".  Weitere Informationen finden Sie unter [Anzeigen von aufnahmeeinstellungen](#show-recording-settings).  
1.  Stellen Sie **Network** auf die gewünschte drosselungsebene ein.  

### Drosseln der CPU während der Aufzeichnung   

So Drosseln Sie die CPU während der Aufzeichnung:  

1.  Öffnen Sie das Menü " **aufnahmeeinstellungen** ".  Weitere Informationen finden Sie unter [Anzeigen von aufnahmeeinstellungen](#show-recording-settings).  
1.  Setzen Sie die **CPU** auf das gewünschte Drosselungs Niveau.  

Die Drosselung ist relativ zu den Funktionen Ihres Computers.  Mit der Option " **2X verlangsamen** " wird beispielsweise die CPU zwei Mal langsamer als normal ausgeführt.  DevTools simulieren die CPUs von mobilen Geräten nicht wirklich, da sich die Architektur von mobilen Geräten stark von der von Desktops und Laptops unterscheidet.  

### Erweiterte Paint-Instrumentation aktivieren   

So zeigen Sie die detaillierte Farb Instrumentation an:  

1.  Öffnen Sie das Menü " **aufnahmeeinstellungen** ".  Weitere Informationen finden Sie unter [Anzeigen von aufnahmeeinstellungen](#show-recording-settings).  
1.  Aktivieren Sie das Kontrollkästchen **Erweiterte Farb Instrumentation (langsam) aktivieren** .  

Informationen zur Interaktion mit den Malfarbe-Informationen finden Sie unter [Anzeigen von Ebenen](#view-layers-information) und [Anzeigen von Paint Profiler](#view-paint-profiler).  

## Speichern einer Aufzeichnung   

Wenn Sie eine Aufzeichnung speichern möchten, klicken Sie mit der rechten Maustaste, und wählen Sie **Profil speichern**aus.  

> ##### Abbildung 9  
> **Profil speichern**  
> ![Profil speichern][ImageSaveProfile]  

## Laden einer Aufzeichnung   

Wenn Sie eine Aufzeichnung laden möchten, klicken Sie mit der rechten Maustaste, und wählen Sie **Profil laden**aus.  

> ##### Abbildung 10  
> **Profil laden**  
> ![Profil laden][ImageLoadProfile]  

## Löschen der vorherigen Aufzeichnung   

Nachdem **Sie eine** Aufzeichnung gemacht haben, drücken Sie die Aufzeichnung löschen, um die Aufzeichnung ![ ][ImageClearRecordingIcon] aus dem **Leistungs** Panel zu löschen.  

> ##### Abbildung 11  
> Aufzeichnen löschen  
> ![Aufzeichnen löschen][ImageClearRecording]  

## Analysieren einer Leistungsaufzeichnung   

Nachdem Sie die Leistung der [Lauf Zeitaufzeichnung](#record-runtime-performance) oder die [Daten Satz Auslastung](#record-load-performance)aufgezeichnet haben, bietet der **Leistungs** Bereich viele Daten für die Analyse der Leistung von dem, was gerade geschehen ist.  

### Auswählen eines Teils einer Aufzeichnung   

Ziehen Sie den Mauszeiger über die **Übersicht** nach links oder rechts, um einen Teil der Aufzeichnung auszuwählen.  Die **Übersicht** ist der Abschnitt, in dem die **fps**-, **CPU**-und **net** -Diagramme enthalten sind.  

> ##### Abbildung 12  
> Ziehen der Maus über die Übersicht zum Zoomen  
> ![Ziehen der Maus über die Übersicht zum Zoomen][ImageZoom]  

So wählen Sie einen Teil über die Tastatur aus:  

1.  Klicken Sie auf den Hintergrund des **Haupt** Abschnitts oder eines der Abschnitte daneben, wie **Interaktionen**, **Netzwerk**oder **GPU**.  Dieser Tastatur Workflow funktioniert nur, wenn einer dieser Abschnitte den Fokus hat.  
1.  Verwenden Sie `W` die `A` Tasten,, `S` , `D` um Sie zu vergrößern, nach Links zu verschieben, zu verkleinern und nach rechts zu verschieben.  

So wählen Sie einen Teil mithilfe eines Trackpads aus:  

1.  Zeigen Sie mit der Maus auf den Abschnitt " **Übersicht** " oder den Abschnitt " **Details** ".  Der Abschnitt " **Übersicht** " ist der Bereich, in dem die **fps**-, **CPU**-und **net** -Diagramme enthalten sind.  Der Abschnitt **Details** ist der Bereich, der den **Haupt** Abschnitt, den Abschnitt **Interaktionen** und so weiter enthält.  
1.  Wischen Sie mit zwei Fingern nach oben, um es zu verkleinern, wischen Sie nach links, wischen Sie nach unten, um die Ansicht zu vergrößern, und wischen Sie nach rechts, um nach rechts zu wechseln  

Wenn Sie im **Haupt** Abschnitt oder in einem der Nachbarn in einem langen Flammen Diagramm Scrollen möchten, klicken und halten Sie beim Ziehen nach oben und unten.  Ziehen Sie nach links und rechts, um zu verschieben, welcher Teil der Aufzeichnung markiert ist.  

### Suchaktivitäten   

Drücken Sie `Control` + `F` \ (Windows \) oder `Command` + `F` \ (macOS \), um das Suchfeld unten im **Leistungs** Bereich zu öffnen.  

> ##### Abbildung 13  
> Verwenden von Regex im Suchfeld am unteren Rand des Fensters, um alle Aktivitäten zu finden, die mit beginnen `E`  
> ![Suchfeld][ImageSearch]  

So navigieren Sie in Aktivitäten, die Ihrer Abfrage entsprechen:  

*   Verwenden Sie die Schaltflächen **vorheriger** ![ ][ImagePreviousIcon] und **Nächster** ![ Nächster Schritt ][ImageNextIcon] .  
*   Drücken Sie `Shift` + `Enter` , um die vorherige oder `Enter` die nächste auszuwählen.  

So ändern Sie die Abfrageeinstellungen:  

*   Drücken **Sie** ![ die Groß-/Kleinschreibung von Groß-/Kleinschreibung ][ImageSearchCaseIcon] , damit die Abfrage Groß-/Kleinschreibung beachtet.  
*   Drücken Sie **Regex** ![ Regex ][ImageSearchRegexIcon] , um einen regulären Ausdruck in Ihrer Abfrage zu verwenden.  

Wenn Sie das Suchfeld ausblenden möchten, drücken Sie **Abbrechen**.  

### Hauptthread Aktivität anzeigen   

Verwenden Sie den **Haupt** Abschnitt, um die Aktivitäten anzuzeigen, die im Hauptthread der Seite aufgetreten sind.  

> ##### Abbildung 14  
> Der **Haupt** Abschnitt  
> ![Der Hauptabschnitt][ImageMain]  

Klicken Sie auf ein Ereignis, um weitere Informationen dazu auf der Registerkarte " **Zusammenfassung** " anzuzeigen.  DevTools skizziert das ausgewählte Ereignis.  

> ##### Abbildung 15  
> Weitere Informationen zur `anonymous` Funktion auf der Registerkarte " **Zusammenfassung** "  
> ![Weitere Informationen zur anonymen Funktion auf der Registerkarte "Zusammenfassung"][ImageMainEventSummary]  

DevTools stellt die Hauptthread Aktivität mit einem Flammen Diagramm dar.  Die x-Achse stellt die Aufzeichnung über einen Zeitraum dar.  Die y-Achse steht für die Aufrufliste.  Die Ereignisse im Vordergrund führen zu den darunter liegenden Ereignissen.  

> ##### Abbildung 16  
> Ein Flammen Diagramm im **Haupt** Abschnitt  
> ![Ein Flammen Diagramm][ImageFlameChart]  

In [Abbildung 16](#figure-16)hat ein `click` Ereignis eine `Function Call` in `activitytabs.js` on Zeile 53 verursacht.  Unten `Function Call` sehen Sie, dass eine anonyme Funktion aufgerufen wurde.  Die anonyme Funktion mit dem Namen, die aufgerufen `a` `wait` wird `Minor GC` .  

DevTools weist Skripten zufällige Farben zu.  In [Abbildung 16](#figure-16)sind Funktionsaufrufe eines Skripts farbig hellgrün.  Anrufe von einem anderen Skript sind farbig beige.  Das dunklere Gelb steht für Skriptaktivitäten, und das Purple-Ereignis stellt die Rendering-Aktivität dar.  Diese dunkelgelben und violetten Ereignisse sind für alle Aufzeichnungen konsistent.  

Weitere Informationen finden Sie unter [Deaktivieren von JavaScript-Beispielen](#disable-javascript-samples) , wenn Sie den detaillierten Flammen Diagramm von JavaScript-anrufen ausblenden möchten.  Wenn js-Beispiele deaktiviert sind, werden nur Ereignisse auf höherer Ebene angezeigt, `Event: click` wie `Function Call` in [Abbildung 16](#figure-16).  

### Anzeigen von Aktivitäten in einer Tabelle   

Nach dem Aufzeichnen einer Seite müssen Sie sich nicht nur auf den **Haupt** Abschnitt verlassen, um Aktivitäten zu analysieren.  DevTools stellt auch drei tabellarische Ansichten zum Analysieren von Aktivitäten bereit.  Jede Ansicht gibt Ihnen eine andere Perspektive auf die Aktivitäten:  

*   Wenn Sie die Stammaktivitäten anzeigen möchten, die die meiste Arbeit verursachen, verwenden Sie [die Registerkarte **anrufstruktur** ](#the-call-tree-tab).  
*   Wenn Sie die Aktivitäten anzeigen möchten, bei denen die meiste Zeit direkt ausgegeben wurde, verwenden Sie [die Registerkarte **unten nach oben** ](#the-bottom-up-tab).  
*   Wenn Sie die Aktivitäten in der Reihenfolge anzeigen möchten, in der Sie während der Aufzeichnung aufgetreten sind, verwenden Sie [die Registerkarte **Ereignisprotokoll** ](#the-event-log-tab).  

> [!NOTE]
> Die nächsten drei Abschnitte beziehen sich alle auf die gleiche Demo.  Führen Sie die Demo selbst auf der [Registerkarte Activity Tabs][ActivityTabsDemo]aus.  

#### Stammaktivitäten   

Im folgenden finden Sie eine Erläuterung des Konzepts der **Stammaktivitäten** , das auf der Registerkarte " **anrufstruktur** ", " **Bottom-up-** Registerkarte" und " **Ereignisprotokoll** Abschnitte" erwähnt wird.  

Stammaktivitäten sind solche, die dazu führen, dass der Browser einige Aufgaben ausführen kann.  Wenn Sie beispielsweise auf eine Seite klicken, löst der Browser eine `Event` Aktivität als Stammaktivität aus.  , Die `Event` dazu führen können, dass ein Handler ausgeführt wird usw.  

Im Flammen Diagramm des **Haupt** Abschnitts befinden sich die Stammaktivitäten am oberen Rand des Diagramms.  In den Registerkarten " **anrufstruktur** " und " **Ereignisprotokoll** " sind Stammaktivitäten die Elemente der obersten Ebene.  

Ein Beispiel für Stammaktivitäten finden Sie auf [der Registerkarte anrufstruktur](#the-call-tree-tab) .  

#### Die Registerkarte "anrufstruktur"   

Verwenden Sie die Registerkarte **anrufstruktur** , um anzuzeigen, welche [Stammaktivitäten](#root-activities) die meiste Arbeit verursachen.  

Die Registerkarte " **anrufstruktur** " zeigt nur Aktivitäten während des ausgewählten Teils der Aufzeichnung an.  Informationen zum Auswählen von Teilen finden Sie unter [Auswählen eines Teils einer Aufzeichnung](#select-a-portion-of-a-recording) .  

> ##### Abbildung 17  
> Die Registerkarte " **anrufstruktur** "  
> ![Die Registerkarte "anrufstruktur"][ImageCallTree]  

In [Abbildung 17](#figure-17)ist die oberste Ebene der Elemente in der Spalte **Aktivität** , wie `Evaluate Script` und `Parse HTML` sind Stammaktivitäten.  Die Schachtelung stellt die Aufrufliste dar.  Beispielsweise in [Abbildung 17](#figure-17), `Parse HTML` die verursacht hat, `Evaluate Script` `Compile Script` und `(anonymous)` .  

**Self time** steht für die in dieser Aktivität direkt verbrachte Zeit.  **Gesamtzeit** stellt die Zeit dar, die in dieser Aktivität oder einem der untergeordneten Elemente aufgewendet wurde.  

Klicken Sie auf **selbst Zeit**, **Gesamtzeit**oder **Aktivität** , um die Tabelle nach dieser Spalte zu sortieren.  

Verwenden Sie das Textfeld **Filtern** , um Ereignisse nach Aktivitätsname zu filtern.  

Standardmäßig ist das Menü **Gruppierung** auf **keine Gruppierung**eingestellt.  Verwenden Sie das Menü **Gruppierung** , um die aktivitätstabelle auf der Grundlage verschiedener Kriterien zu sortieren.  

Klicken Sie auf **schwerste** Stapel ![ anzeigen ][ImageShowHeaviestStackIcon] , um eine andere Tabelle rechts neben der **Aktivitäts** Tabelle anzuzeigen.  Klicken Sie auf eine Aktivität, um die **schwerste Stapel** Tabelle aufzufüllen.  Die **schwerste Stapel** Tabelle zeigt, welche untergeordneten Elemente der ausgewählten Aktivität am längsten ausgeführt wurden.  

#### Die Registerkarte "Bottom-up"   

Verwenden Sie die Registerkarte " **Bottom-up** ", um anzuzeigen, welche Aktivitäten die meiste Zeit im Aggregat Direktaufnahmen.  

Auf der Registerkarte **Bottom-up** werden nur Aktivitäten während des ausgewählten Teils der Aufzeichnung angezeigt.  Informationen zum Auswählen von Teilen finden Sie unter [Auswählen eines Teils einer Aufzeichnung](#select-a-portion-of-a-recording) .  

> ##### Abbildung 18  
> Die Registerkarte " **Bottom-up** "  
> ![Die Registerkarte "Bottom-up"][ImageBottomUp]  

Sehen Sie im **Haupt** Abschnitt Flammen Diagramm in [Abbildung 18](#figure-18), dass fast die ganze Zeit ausgeführt wurde `Parse HTML` .  Die oberste Aktivität auf der Registerkarte " **Bottom-up** " in [Abbildung 18](#figure-18) ist `Parse HTML` .  <!--In the flame chart of [Figure 18](#figure-18), the yellow below the calls to `wait` are actually thousands of `Minor GC` calls.  -->  Informationen dazu finden Sie auf der Registerkarte " **Bottom-up** " `Layout` .  

Die Spalte **selbst Zeit** stellt die aggregierte Zeit dar, die direkt in dieser Aktivität für alle Vorkommen aufgewendet wurde.  

Die Spalte " **Gesamtzeit** " stellt die aggregierte Zeit dar, die in dieser Aktivität oder einem der untergeordneten Elemente aufgewendet wurde.  

#### Die Registerkarte "Ereignisprotokoll"   

Verwenden Sie die Registerkarte **Ereignisprotokoll** , um Aktivitäten in der Reihenfolge anzuzeigen, in der Sie während der Aufzeichnung aufgetreten sind.  

Die Registerkarte **Ereignisprotokoll** zeigt nur Aktivitäten während des ausgewählten Teils der Aufzeichnung an.  Informationen zum Auswählen von Teilen finden Sie unter [Auswählen eines Teils einer Aufzeichnung](#select-a-portion-of-a-recording) .  

> ##### Abbildung 19  
> Die Registerkarte " **Ereignisprotokoll** "  
> ![Die Registerkarte "Ereignisprotokoll"][ImageEventLog]  

Die Spalte **Anfangszeit** steht für den Punkt, an dem die Aktivität gestartet wurde, relativ zum Anfang der Aufzeichnung.  Beispielsweise bedeutet die Startzeit `175.7 ms` für das ausgewählte Element in [Abbildung 19](#figure-19) , dass die Aktivität nach Beginn der Aufzeichnung 175,7 ms gestartet hat.  

Die Spalte **selbst Zeit** stellt die Zeit dar, die direkt in dieser Aktivität verbracht wurde.  

Die Spalten **Gesamtzeit** stellt die Zeit dar, die direkt in dieser Aktivität oder in einem der untergeordneten Elemente aufgewendet wurde.  

Klicken Sie auf **Startzeit**, **selbst Zeit**oder **Gesamtzeit** , um die Tabelle nach dieser Spalte zu sortieren.

Verwenden Sie das Textfeld **Filtern** , um Aktivitäten nach Namen zu filtern.  

Verwenden Sie das Menü " **Dauer** ", um alle Aktivitäten zu filtern, die weniger als 1 MS oder 15 MS dauerte.  Standardmäßig ist das Menü **Dauer** auf **alle**eingestellt, was bedeutet, dass alle Aktivitäten angezeigt werden.  

Deaktivieren Sie die Kontrollkästchen **Lade**-, **Skripting**-, **Rendering**-oder **Painting** , um alle Aktivitäten aus diesen Kategorien zu filtern.  

### Anzeigen der GPU-Aktivität   

Zeigen Sie die GPU-Aktivität im Abschnitt **GPU** an.  

> ##### Abbildung 20  
> Der **GPU** -Abschnitt  
> ![Der GPU-Abschnitt][ImageGpu]  

### Raster Aktivität anzeigen   

Raster Aktivitäten im **Raster** Abschnitt anzeigen  

> ##### Abbildung 21  
> Der **Raster** Abschnitt  
> ![Der Raster Abschnitt][ImageRaster]  

### Anzeigen von Interaktionen   

Verwenden Sie den Abschnitt **Interaktionen** , um Benutzerinteraktionen zu suchen und zu analysieren, die während der Aufzeichnung aufgetreten sind.  

> ##### Abbildung 22  
> Abschnitt " **Interaktionen** "  
> ![Abschnitt "Interaktionen"][ImageInteractions]  

Eine rote Zeile am unteren Rand einer Interaktion stellt die Zeit dar, die auf den Hauptthread wartet.  

Klicken Sie auf eine Interaktion, um weitere Informationen dazu auf der Registerkarte **Zusammenfassung** anzuzeigen.  

### Analysieren von Frames pro Sekunde (fps)   

DevTools bietet zahlreiche Möglichkeiten zum Analysieren von Frames pro Sekunde:  

*   Verwenden Sie [das **fps** -Diagramm](#the-fps-chart) , um einen Überblick über fps über die Dauer der Aufzeichnung zu erhalten.  
*   Verwenden Sie [den Abschnitt **Frames** ](#the-frames-section) , um anzuzeigen, wie lange ein bestimmter Frame aufgenommen wurde.  
*   Verwenden Sie das **fps-Messgerät** für eine echt Zeitschätzung von fps während der Ausführung der Seite.  Informationen dazu finden Sie unter [Anzeigen von Frames pro Sekunde in Echtzeit mit dem FPS-Meter](#view-frames-per-second-in-realtime-with-the-fps-meter).  

#### Das fps-Diagramm   

Das **fps** -Diagramm bietet eine Übersicht über die Framerate für die Dauer einer Aufzeichnung.  Je höher die grüne Leiste, desto besser die Framerate.  

Eine rote Leiste oberhalb des **fps** -Diagramms ist eine Warnung, dass die Framerate so gering war, dass Sie möglicherweise die Benutzererfahrung beeinträchtigte.  

> ##### Abbildung 23  
> Das fps-Diagramm  
> ![Das fps-Diagramm][ImageFpsChart]  

#### Der Abschnitt "Frames"   

Im Abschnitt **Frames** erfahren Sie genau, wie lange ein bestimmter Frame aufgenommen wurde.  

Zeigen Sie mit der Maus auf einen Frame, um eine QuickInfo mit weiteren Informationen dazu anzuzeigen.  

> ##### Abbildung 24  
> Bewegen des Mauszeigers über einen Frame  
> ![Bewegen des Mauszeigers über einen Frame][ImageFramesSection]  

Klicken Sie auf einen Frame, um auf der Registerkarte **Zusammenfassung** noch weitere Informationen zu dem Frame anzuzeigen.  DevTools konturiert den markierten Frame in blau.  

> ##### Abbildung 25  
> Anzeigen eines Frames auf der Registerkarte " **Zusammenfassung** "  
> ![Anzeigen eines Frames auf der Registerkarte "Zusammenfassung"][ImageFrameSummary]  

### Anzeigen von Netzwerkanforderungen   

Erweitern Sie den Abschnitt **Netzwerk** , um einen Wasserfall von Netzwerkanforderungen anzuzeigen, die während der Aufzeichnung aufgetreten sind.  

> ##### Abbildung 26  
> Der Abschnitt " **Netzwerk** "  
> ![Der Abschnitt "Netzwerk"][ImageNetworkRequest]  

Anforderungen werden wie folgt farblich gekennzeichnet:  

*   HTML: blau  
*   CSS: lila  
*   JS: gelb  
*   Bilder: grün  

Klicken Sie auf eine Anfrage, um weitere Informationen dazu auf der Registerkarte " **Zusammenfassung** " anzuzeigen.  So zeigt beispielsweise in [Abbildung 26](#figure-26) auf der Registerkarte " **Zusammenfassung** " Weitere Informationen zur blauen Anforderung an, die im Abschnitt " **Netzwerk** " ausgewählt ist.  

Ein dunkelblaues Quadrat in der oberen linken Ecke einer Anforderung bedeutet, dass es sich um eine Anforderung mit höherer Priorität handelt.  Ein helleres blaues Quadrat bedeutet niedrigere Priorität.  In [Abbildung 26](#figure-26) ist beispielsweise die blaue, ausgewählte Anforderung mit höherer Priorität markiert, und die grüne darunter hat eine niedrigere Priorität.  

In [Abbildung 27](#figure-27)wird die Anforderung `www.bing.com` durch eine Zeile auf der linken Seite, eine Leiste in der Mitte mit einem dunklen Teil und einem hellen Teil sowie eine Zeile auf der rechten Seite dargestellt.  [Abbildung 28](#figure-28) zeigt die entsprechende Darstellung der gleichen Anforderung auf der Registerkarte **Anzeige** Dauer des **Netzwerk** Panels.  Hier sehen Sie, wie diese beiden Darstellungen einander zugeordnet sind:

*   Die linke Zeile ist alles bis zur `Connection Start` Gruppe von Ereignissen inklusive.  Mit anderen Worten: Es ist alles vor `Request Sent` , exklusiv.  
*   Der helle Bereich der Leiste ist `Request Sent` und `Waiting (TTFB)` .  
*   Der dunkle Teil der Leiste ist `Content Download` .  
*   Die richtige Zeile ist im Wesentlichen die Zeit, die auf den Hauptthread wartet.  Diese wird auf der Registerkarte **Anzeige** Dauer nicht dargestellt.  

> ##### Abbildung 27  
> Die Zeile-Balken-Darstellung der `www.bing.com` Anforderung  
> ![Die Zeile-Balken-Darstellung der www.Bing.com-Anforderung][ImageLineBar]  

> ##### Abbildung 28  
> Die Darstellung der Anforderung auf der Registerkarte " **Anzeige** Dauer" `www.bing.com`  
> ![Der Abschnitt "Netzwerk"][ImageTiming]  

### Anzeigen von Speicher Metriken   

Aktivieren Sie das Kontrollkästchen **Speicher** , um Speicher Metriken aus der letzten Aufzeichnung anzuzeigen.  

> ##### Abbildung 29  
> Das Kontrollkästchen " **Speicher** "  
> ![Das Kontrollkästchen "Speicher"][ImageMemory]  

DevTools zeigt ein neues **Speicher** Diagramm über der Registerkarte " **Zusammenfassung** " an.  Es gibt auch ein neues Diagramm unter dem **Netz** Diagramm, das als **Heap**bezeichnet wird.  Das **Heap** Diagramm bietet dieselben Informationen wie die **js-heaplinie** im **Speicher** Diagramm.  

> ##### Abbildung 30  
> Speicher Metriken oberhalb der Registerkarte " **Zusammenfassung** "  
> ![Speicher Metriken][ImageMemoryMetrics]  

Die farbigen Linien auf dem Diagramm werden den farbigen Kontrollkästchen oberhalb des Diagramms zugeordnet.  
Deaktivieren Sie ein Kontrollkästchen, um diese Kategorie aus dem Diagramm auszublenden.  

Das Diagramm zeigt nur den Bereich der Aufzeichnung an, der aktuell markiert ist.  In [Abbildung 30](#figure-30)zeigt das **Speicher** Diagramm beispielsweise nur die Speicherauslastung von der 400 MS-Marke bis zum 1750 MS Mark.  

### Anzeigen der Dauer eines Teils einer Aufzeichnung   

Wenn Sie einen Abschnitt wie " **Netzwerk** " oder " **Main**" analysieren, benötigen Sie manchmal eine genauere Einschätzung, wie lange bestimmte Ereignisse dauerte.  Halten `Shift` , klicken und halten Sie, und ziehen Sie nach links oder rechts, um einen Teil der Aufzeichnung auszuwählen.  Am unteren Rand Ihrer Auswahl zeigt devtools an, wie lange dieser Teil dauerte.  

> ##### Abbildung 31  
> Der `9.47ms` Zeitstempel am unteren Rand des markierten Abschnitts gibt an, wie lange dieser Teil dauerte  
> ![Anzeigen der Dauer eines Teils einer Aufzeichnung][ImageDuration]  

### Anzeigen eines Screenshots   

Informationen zum Aktivieren von Screenshots finden Sie unter [Aufzeichnen von Screenshots während der Aufzeichnung](#capture-screenshots-while-recording) .  

Zeigen Sie mit der Maus auf die **Übersicht** , um einen Screenshot zu sehen, wie die Seite während dieses Moments der Aufzeichnung aussah.  Die **Übersicht** ist der Abschnitt mit den Diagrammen **CPU**, **fps**und **net** .  

> ##### Abbildung 32  
> Anzeigen eines Screenshots  
> ![Anzeigen eines Screenshots][ImageViewScreenshot]  

Sie können Screenshots auch anzeigen, indem Sie im Abschnitt **Frames** auf einen Frame klicken.  DevTools zeigt eine kleine Version des Screenshots auf der Registerkarte " **Zusammenfassung** " an.  

> ##### Abbildung 33  
> Nachdem Sie auf den `233.9ms` Frame im Abschnitt **Frames** geklickt haben, wird der Screenshot für diesen Frame auf der Registerkarte **Zusammenfassung** angezeigt.  
> ![Anzeigen eines Screenshots auf der Registerkarte "Zusammenfassung"][ImageFrameScreenshotSummary]  

Klicken Sie auf der Registerkarte **Zusammenfassung** auf die Miniaturansicht, um den Screenshot zu vergrößern.  

> ##### Abbildung 34  
> Nachdem Sie auf der Registerkarte " **Zusammenfassung** " auf die Miniaturansicht geklickt haben, vergrößert devtools den Screenshot.  
> ![Vergrößern eines Screenshots über die Registerkarte "Zusammenfassung"][ImageFrameScreenshotZoom]  

### Informationen zu Layern anzeigen   

So zeigen Sie erweiterte Folieninformationen zu einem Frame an:  

1.  [Aktivieren der erweiterten Farb Instrumentation](#enable-advanced-paint-instrumentation)  
1.  Wählen Sie im Abschnitt **Frames** einen Frame aus.  DevTools zeigt Informationen zu den Ebenen auf der Registerkarte "neue **Ebenen** " neben der Registerkarte " **Ereignisprotokoll** " an.  
    
    > ##### Abbildung 35  
    > Der Bereich " **Ebenen** "  
    > ![Der Bereich "Ebenen"][ImageLayers]  
    
Zeigen Sie mit der Maus auf eine Ebene, um Sie im Diagramm hervorzuheben.  

> ##### Abbildung 36  
> Highlighting Layer **#39**  
> ![Markieren eines Layers][ImageLayerHover]  

So verschieben Sie das Diagramm:  

*   Klicken **Sie auf Schwenkmodus** ![ ][ImagePanModeIcon] , um entlang der X-und Y-Achse zu navigieren.  
*   Klicken **Sie auf** Rotationsmodus drehen ![ ][ImageRotateModeIcon] , um entlang der Z-Achse zu drehen.  
*   Klicken Sie auf **Transform** ![ -Transformation zurücksetzen ][ImageResetTransformIcon] , um das Diagramm auf die ursprüngliche Position zurückzusetzen.  

### Anzeigen des Paint-Profilers   

So zeigen Sie erweiterte Informationen zu einem Paint-Ereignis an:  

1.  [Aktivieren der erweiterten Farb Instrumentation](#enable-advanced-paint-instrumentation)  
1.  Wählen Sie im **Haupt** Abschnitt ein **Paint** -Ereignis aus.  
    
    > ##### Abbildung 37  
    > Die Registerkarte " **Paint-Profiler** "  
    > ![Die Registerkarte "Paint-Profiler"][ImagePaintProfiler]  
    
## Analysieren der Renderingleistung mit der Registerkarte "Rendern"   

Verwenden Sie die Features der Registerkarte " **Rendern** ", um die Renderingleistung Ihrer Seite zu visualisieren.  

So öffnen Sie die Registerkarte " **Rendering** ":  

1.  [Öffnen des Befehlsmenüs][DevToolsCommandMenu]  
1.  Beginnen `Rendering` Sie mit der Eingabe, und wählen Sie aus `Show Rendering` .  DevTools zeigt die Registerkarte " **Rendering** " am unteren Rand des devtools-Fensters an.  
    
    > ##### Abbildung 38  
    > Die Registerkarte " **Rendern** "  
    > ![Die Registerkarte "Rendern"][ImageRenderingTab]  
    
### Anzeigen von Frames pro Sekunde in Echtzeit mit dem fps-Messgerät   

Das **fps-Messgerät** ist ein Overlay, das in der oberen rechten Ecke des Viewports angezeigt wird.  Bei der Ausführung der Seite wird eine Echtzeit-Schätzung von fps bereitgestellt.  So öffnen Sie das **fps-Messgerät**:  

1.  Öffnen Sie die Registerkarte **Rendering** .  Weitere Informationen finden Sie unter [Analysieren der Renderingleistung mithilfe der Registerkarte Rendern](#analyze-rendering-performance-with-the-rendering-tab).  
1.  Aktivieren Sie das Kontrollkästchen **FPS-Meter** .  
    
    > ##### Abbildung 39  
    > Das fps-Messgerät  
    > ![Das fps-Messgerät][ImageFpsMeter]  
    
### Anzeigen von Zeichnungs Ereignissen in Echtzeit mit Farb blinken   

Verwenden Sie das Farb blinken, um eine Echtzeitansicht aller Paint-Ereignisse auf der Seite zu erhalten.  Jedes Mal, wenn ein Teil der Seite neu gestrichen wird, wird der Abschnitt in devtools in grün umrissen.  

So aktivieren Sie die Farb Blinkfunktion:  

1.  Öffnen Sie die Registerkarte **Rendering** .  Weitere Informationen finden Sie unter [Analysieren der Renderingleistung mithilfe der Registerkarte Rendern](#analyze-rendering-performance-with-the-rendering-tab).  
1.  Aktivieren Sie das Kontrollkästchen " **Farbe blinkt** ".  
    
    > ##### Abbildung 40  
    > **Malen blinkt**  
    > ![Malen blinkt][ImagePaintFlashing]  
    
### Anzeigen einer Überlagerung von Ebenen mit Ebenen Rändern   

Verwenden Sie **Layer-Rahmen** , um eine Überlagerung von Layer-Rändern und Kacheln oben auf der Seite anzuzeigen.  

So aktivieren Sie Layer-Rahmen:  

1.  Öffnen Sie die Registerkarte **Rendering** .  Weitere Informationen finden Sie unter [Analysieren der Renderingleistung mithilfe der Registerkarte Rendern](#analyze-rendering-performance-with-the-rendering-tab).  
1.  Aktivieren Sie das Kontrollkästchen **Layer-Rahmen** .  
    
    > ##### Abbildung 41  
    > **Folienrahmen**  
    > ![Folienrahmen][ImageLayerBorders]  
    
[`debug_colors.cc`][ChromiumDebugColors]Eine Erläuterung der Farbcodierungen finden Sie in den Kommentaren in.  

### Suchen von Scroll-Leistungsproblemen in Echtzeit   

Verwenden Sie Leistungsprobleme beim Scrollen, um Elemente der Seite zu identifizieren, die Ereignislistener in Bezug auf den Bildlauf aufweisen, die die Leistung der Seite beeinträchtigen können.  
DevTools beschreibt die potenziell problematischen Elemente in Teal.  

So zeigen Sie Bild Lauf Leistungsprobleme an:  

1.  Öffnen Sie die Registerkarte **Rendering** .  Weitere Informationen finden Sie unter [Analysieren der Renderingleistung mithilfe der Registerkarte Rendern](#analyze-rendering-performance-with-the-rendering-tab).  
1.  Aktivieren Sie das Kontrollkästchen **Scrolling Performance Issues** .  
 
    > ##### Abbildung 42  
    > **Probleme mit der Bildlaufleistung** deuten darauf hin, dass nicht-Layer-Viewport-abhängige Objekte die Bildlaufleistung beeinträchtigen können.  
    > ![Probleme mit der Bildlaufleistung deuten darauf hin, dass nicht-Layer-Viewport-abhängige Objekte die Bildlaufleistung beeinträchtigen können.][ImageScrollingPerformanceIssues]  
    

<!--    -->  



<!-- image links -->  

[ImageCaptureSettingsIcon]: /microsoft-edge/devtools-guide-chromium/media/capture-settings-icon.msft.png  
[ImageClearRecordingIcon]: /microsoft-edge/devtools-guide-chromium/media/clear-recording-icon.msft.png  
[ImageCollectGarbageIcon]: /microsoft-edge/devtools-guide-chromium/media/collect-garbage-icon.msft.png  
[ImageNextIcon]: /microsoft-edge/devtools-guide-chromium/media/next-icon.msft.png  
[ImagePanModeIcon]: /microsoft-edge/devtools-guide-chromium/media/pan-mode-icon.msft.png  
[ImagePreviousIcon]: /microsoft-edge/devtools-guide-chromium/media/previous-icon.msft.png  
[ImageRecordIcon]: /microsoft-edge/devtools-guide-chromium/media/record-icon.msft.png
[ImageRefreshPageIcon]: /microsoft-edge/devtools-guide-chromium/media/refresh-page-icon.msft.png  
[ImageResetTransformIcon]: /microsoft-edge/devtools-guide-chromium/media/reset-transform-icon.msft.png  
[ImageRotateModeIcon]: /microsoft-edge/devtools-guide-chromium/media/rotate-mode-icon.msft.png  
[ImageSearchCaseIcon]: /microsoft-edge/devtools-guide-chromium/media/search-case-icon.msft.png  
[ImageSearchRegexIcon]: /microsoft-edge/devtools-guide-chromium/media/search-regex-icon.msft.png  
[ImageShowHeaviestStackIcon]: /microsoft-edge/devtools-guide-chromium/media/show-heaviest-stack-icon.msft.png  

[ImageRecord]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-record-highlight.msft.png "Abbildung 1: aufzeichnen"  
[ImageRefreshPage]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-refresh-button.msft.png "Abbildung 2: Seite "Aktualisieren""  
[ImageLoadRecording]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-refreshed.msft.png "Abbildung 3: Laden einer Seiten Aufzeichnung"  
[ImageScreenshots]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-capture-screenshots-checkbox.msft.png "Abbildung 4: das Kontrollkästchen "Screenshots""  
[ImageCollectGarbage]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-collect-garbage-button.msft.png "Abbildung 5: Sammeln von Garbage"  
[ImageCaptureSettings]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-capture-settings-button-open-drawer.msft.png "Abbildung 6: Abschnitt "Aufnahmeeinstellungen""  
[ImageJSSamplesDisabled]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-on.msft.png "Abbildung 7: ein Beispiel für eine Aufzeichnung, wenn JS-Beispiele deaktiviert sind"  
[ImageJSSamplesEnabled]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off.msft.png "Abbildung 8: ein Beispiel für eine Aufzeichnung, wenn JS-Beispiele aktiviert sind"  
[ImageSaveProfile]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off-save-profile.msft.png "Abbildung 9: Speichern des Profils"  
[ImageLoadProfile]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off-load-profile.msft.png "Abbildung 10: Laden eines Profils"  
[ImageClearRecording]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off-clear-button.msft.png "Abbildung 11: Löschen der Aufzeichnung"  
[ImageZoom]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-zoom-highlighted.msft.png "Abbildung 12: Ziehen des Mauszeigers über die Übersicht zum Zoomen"  
[ImageSearch]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-search-regex.msft.png "Abbildung 13: Suchfeld"  
[ImageMain]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-main-zoomed.msft.png "Abbildung 14: der Hauptabschnitt"  
[ImageMainEventSummary]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-summary-me.msft.png "Abbildung 15: Weitere Informationen zur anonymen Funktion auf der Registerkarte "Zusammenfassung""  
[ImageFlameChart]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-main-flame-chart.msft.png "Abbildung 16: ein Flammen Diagramm"  
[ImageCallTree]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-call-tree.msft.png "Abbildung 17: die Registerkarte "anrufstruktur""  
[ImageBottomUp]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-bottoms-up.msft.png "Abbildung 18: die Registerkarte "Bottom-up""  
[ImageEventLog]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-event-log.msft.png "Abbildung 19: Registerkarte "Ereignisprotokoll""  
[ImageGpu]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-gpu-zoomed.msft.png "Abbildung 20: der GPU-Abschnitt"  
[ImageRaster]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-raster.msft.png "Abbildung 21: der Raster Abschnitt"  
[ImageInteractions]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-interactions-animation.msft.png "Abbildung 22: Abschnitt "Interaktionen""  
[ImageFpsChart]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-fps-highlight.msft.png "Abbildung 23: das FPS-Diagramm"  
[ImageFramesSection]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-frames-hover.msft.png "Abbildung 24: Bewegen des Mauszeigers über einen Frame"  
[ImageFrameSummary]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-frames-summary.msft.png "Abbildung 25: Anzeigen eines Frames auf der Registerkarte "Zusammenfassung""  
[ImageNetworkRequest]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-network.msft.png "Abbildung 26: der Abschnitt "Netzwerk""  
[ImageLineBar]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-bing-performance-network.msft.png "Abbildung 27: die Linien leisten Darstellung der www.Bing.com-Anforderung"  
[ImageTiming]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-bing-network-timing.msft.png "Abbildung 28: der Abschnitt "Netzwerk""  
[ImageMemory]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-memory-highlight.msft.png "Abbildung 29: das Kontrollkästchen "Speicher""  
[ImageMemoryMetrics]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-memory-chart.msft.png "Abbildung 30: Speicher Metriken"  
[ImageDuration]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-main-duration.msft.png "Abbildung 31: Anzeigen der Dauer eines Teils einer Aufzeichnung"  
[ImageViewScreenshot]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-screenshots-hover.msft.png "Abbildung 32: Anzeigen eines Screenshots"  
[ImageFrameScreenshotSummary]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-summary-preview.msft.png "Abbildung 33: Anzeigen eines Screenshots auf der Registerkarte "Zusammenfassung""  
[ImageFrameScreenshotZoom]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-summary-preview-select.msft.png "Abbildung 34: Vergrößern eines Screenshots über die Registerkarte "Zusammenfassung""  
[ImageLayers]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-layers-all.msft.png "Abbildung 35: der Bereich "Ebenen""  
[ImageLayerHover]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-frames-document-nav-bar-highlighted.msft.png "Abbildung 36: Markieren eines Layers"  
[ImagePaintProfiler]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-paint-profiler.msft.png "Abbildung 37: die Registerkarte "Paint-Profiler""  
[ImageRenderingTab]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-console-drawer-rendering.msft.png "Abbildung 38: die Registerkarte "Rendern""  
[ImageFpsMeter]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-jank-console-rendering-frame-rate.msft.png "Abbildung 39: das FPS-Messgerät"  
[ImagePaintFlashing]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-jank-console-rendering-paint-flashing.msft.png "Abbildung 40: Farbe blinkt"  
[ImageLayerBorders]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-devtools-console-rendering-layer-borders.msft.png "Abbildung 41: Ebenen Ränder"  
[ImageScrollingPerformanceIssues]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-bing-console-drawer-rendering-scrolling-performance-issues.msft.png "Abbildung 42: Leistungsprobleme beim Scrollen deuten darauf hin, dass nicht-Layer-Viewport-abhängige Objekte die Bildlaufleistung beeinträchtigen können."  

<!-- links -->  

[MicrosoftEdgeDevTools]: /microsoft-edge/devtools-guide-chromium "Microsoft Edge (Chrom)-Entwickler Tools"  
[DevToolsCommandMenu]: /microsoft-edge/devtools-guide-chromium/command-menu/index#open-the-command-menu "Öffnen des Befehlsmenüs – Ausführen von Befehlen mit dem Befehlsmenü von Microsoft Edge devtools"  
[DevtoolsEvaluatePerformanceGettingStarted]: /microsoft-edge/devtools-guide-chromium/evaluate-performance/index "Erste Schritte mit der Analyse der Laufzeitleistung"  

[ActivityTabsDemo]: https://microsoft-edge-chromium-devtools.glitch.me/perf/activitytabs.html "Demo zu Aktivitäts Registerkarten"  

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
