---
title: Beheben von Speicherproblemen
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/03/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Web-Entwicklung, F12-Tools, devtools
ms.openlocfilehash: 738ef5fe682633f3100345c922ff12c3c27a7166
ms.sourcegitcommit: 50991a04c18283a8890ae33fcc3491c0476c7684
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/30/2020
ms.locfileid: "10611762"
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





# Beheben von Speicherproblemen   



Erfahren Sie, wie Sie Microsoft Edge und DevTools verwenden, um Speicherprobleme zu finden, die sich auf die Seitenleistung auswirken, wie Speicherverluste, aufblasen des Arbeitsspeichers und häufige Garbage Collections.  

### Zusammenfassung  

*   Finden Sie heraus, wie viel Arbeitsspeicher Ihre Seite zurzeit mit dem Task-Manager von Microsoft Edge-Browser verwendet.  
*   Visualisieren Sie die Speichernutzung im Zeitverlauf mit dem **Speicher** Panel.  
*   Identifizieren Sie freigegebene Dom-Bäume \ (eine häufige Ursache für Speicherverluste \) mit **Heap-Snapshots**.  
*   Informieren Sie sich, wann der neue Arbeitsspeicher in Ihrem JavaScript-Heap \ (JS-Heap \) mit **Zuordnungs Instrumentation auf Zeitachse**zugewiesen wird.  

## Übersicht  

Im Sinne des **Rail** -Leistungsmodells sollten Ihre Benutzer den Schwerpunkt ihrer Leistungs Bemühungen haben.  

<!--todo: add RAIL section when available  -->  

Speicherprobleme sind wichtig, da Sie für die Benutzer oft wahrnehmbar sind.  Benutzer können Speicherprobleme wie folgt erkennen:  

*   **Die Leistung einer Seite wird im Laufe der Zeit zunehmend schlechter**.  Dies ist möglicherweise ein Symptom für einen Speicherverlust.  Ein Speicherverlust ist, wenn ein Fehler auf der Seite dazu führt, dass die Seite zunehmend mehr und mehr Arbeitsspeicher im Laufe der Zeit verwendet.  
*   **Die Leistung einer Seite ist durchwegs schlecht**.  Dies ist möglicherweise ein Symptom des Aufblasens des Arbeitsspeichers.  Der Arbeitsspeicher wird aufgebläht, wenn eine Seite mehr Arbeitsspeicher benötigt, als für optimale Seiten Geschwindigkeit erforderlich ist.  
*   **Die Leistung einer Seite wird verzögert oder wird häufig angehalten**.  Dies ist möglicherweise ein Symptom häufiger Garbage Collections.  Die Garbage Collection ist der Fall, wenn der Browser Speicher aufhebt.  Der Browser entscheidet, wann dies geschieht.  Während Auflistungen wird alle ausgeführten Skripts angehalten.  Wenn der Browser also viel Garbage Collection durchläuft, wird die Skriptlaufzeit viel angehalten.  

### Speicher aufblasen: wie viel ist "zu viel"?  

Ein Speicherverlust ist einfach zu definieren.  Wenn eine Website zunehmend mehr und mehr Arbeitsspeicher verwendet, liegt ein Leck vor.  Aber der Speicher aufblasen ist etwas schwieriger zu anheften.  Was qualifiziert als "Verwenden von zu viel Arbeitsspeicher"?  

Hier gibt es keine harten Zahlen, da unterschiedliche Geräte und Browser unterschiedliche Funktionen aufweisen.  Die gleiche Seite, die auf einem Highend-Smartphone problemlos läuft, kann auf einem Low-End-Smartphone abstürzen.  

Der Schlüssel besteht darin, das Schienen Modell zu verwenden und sich auf die Benutzer zu konzentrieren.  Finden Sie heraus, welche Geräte für Ihre Benutzer beliebt sind, und testen Sie dann Ihre Seite auf diesen Geräten.  Wenn die Erfahrung durchweg fehlerhaft ist, kann die Seite die Speicherfunktionen dieser Geräte überschreiten.  

## Überwachen der Speichernutzung in Echtzeit mit dem Microsoft Edge-Browser-Task-Manager  

Verwenden Sie den Microsoft Edge-Browser-Task-Manager als Ausgangspunkt für die Untersuchung des Speicherproblems.  Der Microsoft Edge-Browser-Task-Manager ist ein Echtzeitmonitor, der Ihnen mitteilt, wie viel Arbeitsspeicher eine Seite zurzeit verwendet.  

1.  Drücken `Shift` + `Esc` oder wechseln Sie zum Hauptmenü von Microsoft Edge, und wählen Sie **Weitere Tools**  >  **Browser Task-Manager** aus, um den Task-Manager von Microsoft Edge-Browser zu öffnen.  
    
    > ##### Abbildung1  
    > Öffnen des Task-Managers des Microsoft Edge-Browsers  
    > ![Öffnen des Task-Managers des Microsoft Edge-Browsers][ImageTaskManager]  
    
1.  Klicken Sie mit der rechten Maustaste auf die Tabellenüberschrift des Task-Managers von Microsoft Edge-Browser, und aktivieren Sie **JavaScript-Speicher**.  
    
    > ##### Abbildung2  
    > Aktivieren des JavaScript-Speichers  
    > ![Aktivieren des JavaScript-Speichers][ImageJavascriptMemory]  
    
Diese beiden Spalten geben Ihnen unterschiedliche Informationen dazu, wie Ihre Seite den Arbeitsspeicher verwendet:  

*   Die **Speicher** Spalte stellt den systemeigenen Speicher dar.  DOM-Knoten werden im systemeigenen Speicher gespeichert.  Wenn dieser Wert immer größer wird, werden DOM-Knoten erstellt.  
*   Die **JavaScript-Speicher** Spalte stellt den js-Heap dar.  Diese Spalte enthält zwei Werte.  Der Wert, an dem Sie interessiert sind, ist die Live-Nummer \ (die Zahl in Klammern \).  Die Live-Nummer gibt an, wie viel Arbeitsspeicher die erreichbaren Objekte auf der Seite verwenden.  Wenn diese Zahl zunimmt, werden entweder neue Objekte erstellt, oder die vorhandenen Objekte werden größer.  

<!--*   live number reference: https://groups.google.com/d/msg/google-chrome-developer-tools/aTMVGoNM0VY/bLmf3l2CpJ8J  -->  

## Visualisieren von Speicherverlusten mithilfe des Leistungs Panels  

Sie können das Leistungs Panel auch als weiteren Ausgangspunkt ihrer Untersuchung verwenden.  Der Leistungs Panel hilft Ihnen, die Speichernutzung einer Seite im Laufe der Zeit zu visualisieren.  

1.  Öffnen Sie in devtools das Panel **Leistung** .  
1.  Aktivieren Sie das Kontrollkästchen **Speicher** .  
1.  [Führen Sie eine Aufzeichnung][DevtoolsEvaluatePerformanceReferenceRecord]aus.  

> [!TIP]
> Es empfiehlt sich, die Aufzeichnung mit einer erzwungenen Garbage Collection zu starten und zu beenden.  Klicken Sie **collect garbage** ![ während der Aufzeichnung auf die Schaltfläche Garbage Collection sammeln, um die Garbage ][ImageForceGarbageCollectionIcon] Collection zu erzwingen.  

Wenn Sie Speicher Aufzeichnungen demonstrieren möchten, sollten Sie den folgenden Code verwenden:  

```javascript
var x = [];
function grow() {
    for (var i = 0; i < 10000; i++) {
        document.body.appendChild(document.createElement('div'));
    }
    x.push(new Array(1000000).join('x'));
}
document.getElementById('grow').addEventListener('click', grow);
```  

Jedes Mal, wenn die Schaltfläche, auf die im Code verwiesen wird, gedrückt wird, werden 10000- `div` Knoten an den Dokument Text angefügt, und eine Zeichenfolge mit 1 Million `x` Zeichen wird auf das `x` Array verschoben.  Durch Ausführen dieses Codes wird eine Aufzeichnung im **Leistungs** Panel wie [Abbildung 3](#figure-3)erstellt.  

> ##### Abbildung 3  
> Einfaches Wachstum  
> ![Einfaches Wachstum][ImageSimpleGrowth]  

Zunächst eine Erläuterung der Benutzeroberfläche.  Das **Heap** Diagramm im Übersichts **Bereich \** (unter **net**\) stellt den js-Heap dar.  Unter dem Übersichtsbereich befindet sich **der Bereich** **Zähler** .  Hier können **Sie die Speicher** Auslastung nach js-Heap (wie **Heap** Diagramm im Übersichtsbereich \), Dokumente, DOM-Knoten, Listener und GPU-Speicher unterteilt sehen.  Wenn Sie ein Kontrollkästchen deaktivieren, wird es aus dem Diagramm ausgeblendet.  

Nun eine Analyse des Codes im Vergleich zu [Abbildung 3](#figure-3).  Wenn Sie sich den Knoten Zähler \ (das grüne Diagramm \) ansehen, können Sie sehen, dass er mit dem Code sauber übereinstimmt.  Die Anzahl der Knoten nimmt in diskreten Schritten zu.  Sie können davon ausgehen, dass jede Erhöhung der Knotenanzahl ein Aufruf von ist `grow()` .  Das js-Heap Diagramm \ (das blaue Diagramm \) ist nicht so einfach.  In Übereinstimmung mit den bewährten Methoden ist der erste DIP eine erzwungene Garbage Collection \ (erreicht durch **collect garbage** Drücken der ![ Schaltfläche Garbage Force Garbage Collection sammeln ][ImageForceGarbageCollectionIcon] ).  Während die Aufzeichnung fortschreitet, können Sie sehen, dass die JS-Heapgröße Spikes.  Dies ist natürlich und erwartet: der JavaScript-Code erstellt die DOM-Knoten auf jedem Schaltflächenklick und macht viel Arbeit, wenn die Zeichenfolge von 1 Million-Zeichen erstellt wird.  Der wichtigste Punkt hierbei ist die Tatsache, dass der JS-Heap höher als gestartet ist \ (der "Anfang" hier ist der Punkt nach der erzwungenen Garbage Collection \).  Wenn Sie in der realen Welt dieses Muster mit einer zunehmenden js-Heapgröße oder Knoten Größe gesehen haben, kann dies potenziell einen Speicherverlust definieren.  

<!--todo: the Heap snapshots and Profiles panel are not found in Edge  -->  

## Entdecken von frei gelösten Dom-Strukturspeicher Lecks mit Heap-Schnappschüssen  

Ein DOM-Knoten ist nur Garbage Collection, wenn keine Verweise auf den Knoten aus der DOM-Struktur oder dem auf der Seite ausgeführten JavaScript-Code vorhanden sind.  Ein Knoten wird als "losgelöst" bezeichnet, wenn er aus der DOM-Struktur entfernt wird, aber einige JavaScript-Objekte verweisen weiterhin auf ihn.  Getrennte DOM-Knoten sind eine häufige Ursache für Speicherverluste.  In diesem Abschnitt erfahren Sie, wie Sie die Heap-Profiler in devtools verwenden, um getrennte Knoten zu identifizieren.  

Es folgt ein einfaches Beispiel für getrennte DOM-Knoten.  

```javascript
var detachedNodes;
function create() {
    var ul = document.createElement('ul');
    for (var i = 0; i < 10; i++) {
        var li = document.createElement('li');
        ul.appendChild(li);
    }
    detachedNodes = ul;
}
document.getElementById('create').addEventListener('click', create);
```  

Durch Klicken auf die Schaltfläche im Code wird ein `ul` Knoten mit zehn unter `li` geordneten Elementen erstellt.  Auf diese Knoten wird vom Code verwiesen, aber Sie sind nicht in der DOM-Struktur vorhanden, daher wird jeder getrennt.  

Heap-Schnappschüsse sind eine Möglichkeit, getrennte Knoten zu identifizieren.  Wie der Name schon sagt, zeigen Heap-Schnappschüsse an, wie der Speicher zwischen den js-Objekten und DOM-Knoten für Ihre Seite zum Zeitpunkt des Schnappschusses verteilt wird.  

Wenn Sie einen Schnappschuss erstellen möchten, öffnen Sie devtools, und wechseln Sie zum **Speicher** Panel, wählen Sie das Optionsfeld **Heap-Snapshot** aus, und drücken Sie dann die Schaltfläche **Schnappschuss aufnehmen** .  

> ##### Abbildung4  
> Snapshot des Heaps aufnehmen  
> ![Snapshot des Heaps aufnehmen][ImageTakeHeapSnapshot]  

Der Snapshot kann einige Zeit dauern, bis er verarbeitet und geladen wurde.  Wenn Sie den Vorgang beenden, wählen Sie ihn im linken Panel aus. \ (benannte **Heap-Schnappschüsse**\).  

Geben `Detached` Sie in das Textfeld **Klassenfilter** ein, um nach frei gelösten Dom-Strukturen zu suchen.  

> ##### Abbildung5  
> Filtern für getrennte Knoten  
> ![Filtern für getrennte Knoten][ImageFilteringForDetachedNodes]  

Erweitern Sie die Karat, um eine frei gelöste Struktur zu untersuchen.  

> ##### Abbildung6  
> Untersuchen von getrennten Strukturen  
> ![Untersuchen von getrennten Strukturen][ImageInvestigatingDetachedTree]  

<!--Nodes highlighted yellow have direct references to them from the JavaScript code.  Nodes highlighted red do not have direct references.  They are only alive because they are part of the tree for the yellow node.  In general, you want to focus on the yellow nodes.  Fix your code so that the yellow node is not alive for longer than it needs to be, and you also get rid of the red nodes that are part of the tree for the yellow node.  -->

Klicken Sie auf einen Knoten, um ihn weiter zu untersuchen.  Im **Objekt** Bereich können Sie weitere Informationen zu dem Code anzeigen, der darauf verweist.  In [Abbildung 7](#figure-7) können Sie beispielsweise feststellen, dass die `detachedNodes` Variable auf den Knoten verweist.  Um diesen bestimmten Speicherverlust zu beheben, sollten Sie den Code untersuchen, der die Variable verwendet, `detachedUNode` und sicherstellen, dass der Verweis auf den Knoten entfernt wird, wenn er nicht mehr benötigt wird.

> ##### Abbildung7  
> Untersuchen eines Knotens  
> ![Untersuchen eines Knotens][ImageInvestigatingNode]  

<!--todo: the allocation timeline does not appear in the DevTools in Edge  -->  

## Ermitteln von JS-Heapspeicher Lecks mit Zuordnungs Instrumentation auf Zeitachse  

Die **Zuweisungs Instrumentation auf der Zeitachse** ist ein weiteres Tool, mit dem Sie möglicherweise Speicherverluste in Ihrem js-Heap ermitteln können.  

Demonstrieren Sie die **Zuweisungs Instrumentation auf Zeitachse** mithilfe des folgenden Codes.  

```javascript
var x = [];
function grow() {
    x.push(new Array(1000000).join('x'));
}
document.getElementById('grow').addEventListener('click', grow);
```  

Jedes Mal, wenn die Schaltfläche, auf die im Code verwiesen wird, gedrückt wird, wird dem Array eine Zeichenfolge von 1 Million-Zeichen hinzugefügt `x` .  

Wenn Sie eine Zuordnungs Instrumentation auf der Zeitachse aufzeichnen möchten, öffnen Sie devtools, wechseln Sie zur Register **Karte Speicher** , wählen Sie das Optionsfeld **Zuweisungs Instrumentation auf Zeitachse** aus, drücken Sie die Schaltfläche **Start** , führen Sie die Aktion aus, die Sie vermuten, dass der Speicherverlust verursacht wird, und drücken Sie dann die Schaltfläche **Aufzeichnung** Beenden der Aufzeichnung beenden, ![ ][ImageStopRecordingIcon] Wenn Sie fertig sind.  

Beachten Sie während der Aufzeichnung, ob blaue Balken in der Zuordnungs Instrumentation auf der Zeitachse angezeigt werden, wie in [Abbildung 8](#figure-8).  

> ##### Abbildung8  
> Neue Zuweisungen  
> ![Neue Zuweisungen][ImageNewAllocations]  

Diese blauen Balken stellen neue Speicherzuweisungen dar.  Diese neuen Speicherzuweisungen sind ihre Kandidaten für Speicherverluste.  Sie können auf eine Leiste Zoomen, um den Bereich " **Konstruktor** " zu filtern, sodass nur Objekte angezeigt werden, die während des angegebenen Zeitrahmens reserviert wurden.  

> ##### Abbildung 9  
> Verkleinerte Zuordnungs Zeitachse  
> ![Verkleinerte Zuordnungs Zeitachse][ImageZoomedAllocationTimeline]  

Erweitern Sie das Objekt, und klicken Sie auf den Wert, um weitere Details im **Objekt** Bereich anzuzeigen.  Wenn Sie beispielsweise in [Abbildung 10](#figure-10)die Details des neu zugewiesenen Objekts anzeigen, sollten Sie sehen können, dass es der `x` Variablen im Bereich zugeordnet wurde `Window` .  

> ##### Abbildung 10 
> Objektdetails  
> ![Objektdetails][ImageObjectDetail]  

## Untersuchen der Speicherzuweisung nach Funktion   

Verwenden Sie den Profilerstellungs-Typ der **Zuordnungs Stichprobe** , um die Speicherzuweisung nach JavaScript-Funktion anzuzeigen.  

> ##### Abbildung 11  
> Sampling für Daten Satz Zuteilung  
> ![Sampling für Daten Satz Zuteilung][ImageRecordAllocationSampling]  

1.  Aktivieren Sie das Optionsfeld **Zuweisungs Sampling** .  Wenn auf der Seite eine Arbeitskraft vorhanden ist, können Sie diese über das Dropdownmenü neben der Schaltfläche **Start** als Profil Ziel auswählen.  
1.  Drücken Sie die Schaltfläche **Start** .  
1.  Führen Sie die Aktionen auf der Seite aus, die Sie untersuchen möchten.  
1.  Drücken Sie die **Stopp** -Taste, wenn Sie alle Ihre Aktionen beendet haben.  

DevTools zeigt eine Aufschlüsselung der Speicherzuweisung nach Funktion.  Die Standardansicht ist **schwer (unten nach oben)**, in der die Funktionen angezeigt werden, die den größten Arbeitsspeicher oben zugewiesen haben.  

> ##### Abbildung 12  
> Zuordnungs Stichproben  
>![Zuordnungs Stichproben][ImageAllocationSampling]  

## Häufige Garbage Collections erkennen  

Wenn Ihre Seite häufig angehalten wird, haben Sie möglicherweise Probleme mit der Garbage Collection.  

Sie können entweder den Microsoft Edge-Browser-Task-Manager oder Leistungs Speicher Aufzeichnungen verwenden, um häufige Garbage Collection zu erkennen.  Im Microsoft Edge-Browser Task-Manager stellen häufig steigende und fallende **Speicher** -oder **JavaScript-Speicher** Werte häufige Garbage Collection dar.  In Leistungs Aufzeichnungen deuten häufige Änderungen (steigende und fallende) auf die JS-Heap-oder Knotenanzahl-Diagramme auf häufige Garbage Collection hin.  

Nachdem Sie das Problem identifiziert haben, können Sie eine **Zuordnungs Instrumentation für die Zeitachsen** Aufzeichnung verwenden, um herauszufinden, wo Speicher reserviert wird und welche Funktionen die Zuweisungen verursachen.  

<!--## Feedback   -->  



<!-- image links -->  

[ImageForceGarbageCollectionIcon]: /microsoft-edge/devtools-guide-chromium/media/collect-garbage-icon.msft.png  
[ImageStopRecordingIcon]: /microsoft-edge/devtools-guide-chromium/media/stop-recording-icon.msft.png  

[ImageTaskManager]: /microsoft-edge/devtools-guide-chromium/media/memory-problems-bing-settings-more-tools-browser-task-manager.msft.png "Abbildung 1: Öffnen des Microsoft Edge-Browser-Task-Managers"  
[ImageJavascriptMemory]: /microsoft-edge/devtools-guide-chromium/media/memory-problems-bing-browser-task-manager-javascript-memory.msft.png "Abbildung 2: Aktivieren des JavaScript-Speichers"  
[ImageSimpleGrowth]: /microsoft-edge/devtools-guide-chromium/media/memory-problems-glitch-example-1-performance-memory.msft.png "Abbildung 3: einfaches Wachstum"  
[ImageTakeHeapSnapshot]: /microsoft-edge/devtools-guide-chromium/media/memory-problems-glitch-example-12-memory-heap-snapshot.msft.png "Abbildung 4: Erstellen eines Heap-Snapshots"  
[ImageFilteringForDetachedNodes]: /microsoft-edge/devtools-guide-chromium/media/memory-problems-glitch-example-12-memory-heap-snapshot-filter-detached.msft.png "Abbildung 5: Filtern nach getrennten Knoten"  
[ImageInvestigatingDetachedTree]: /microsoft-edge/devtools-guide-chromium/media/memory-problems-glitch-example-12-memory-heap-snapshot-filter-detached-expanded.msft.png "Abbildung 6: untersuchen einer getrennten Struktur"  
[ImageInvestigatingNode]: /microsoft-edge/devtools-guide-chromium/media/memory-problems-glitch-example-12-memory-heap-snapshot-filter-detached-expanded-selected.msft.png "Abbildung 7: Untersuchen eines Knotens"  
[ImageNewAllocations]: /microsoft-edge/devtools-guide-chromium/media/memory-problems-glitch-example-13-allocation-timeline-snapshot-all.msft.png "Abbildung 8: neue Zuweisungen"  
[ImageZoomedAllocationTimeline]: /microsoft-edge/devtools-guide-chromium/media/memory-problems-glitch-example-13-allocation-timeline-snapshot-focused.msft.png "Abbildung 9: Zeitachse mit vergrößerten Zuordnungen"  
[ImageObjectDetail]: /microsoft-edge/devtools-guide-chromium/media/memory-problems-glitch-example-13-allocation-timeline-snapshot-focused-constructor-expanded.msft.png "Abbildung 10: Objektdetails"  
[ImageRecordAllocationSampling]: /microsoft-edge/devtools-guide-chromium/media/memory-problems-glitch-example-05-memory-allocation-sampling.msft.png "Abbildung 11: Sampling zur Daten Satz Zuteilung"  
[ImageAllocationSampling]: /microsoft-edge/devtools-guide-chromium/media/memory-problems-glitch-example-05-memory-allocation-sampling-heavy-bottom-up.msft.png "Abbildung 12: Zuordnungs Stichproben"  

<!-- links -->  

[DevtoolsEvaluatePerformanceReferenceRecord]: /microsoft-edge/devtools-guide-chromium/evaluate-performance/reference#record-performance "Aufzeichnen einer Leistungsanalyse Referenz"  

<!--[RAIL]: /profile/evaluate-performance/rail  -->
<!--[recording]: /profile/evaluate-performance/timeline-tool#make-a-recording ""  -->  

<!--[hngd]: https://jsfiddle.net/kaycebasques/tmtbw8ef/  -->  

> [!NOTE]
> Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.  
> Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/memory-problems/index) und wird von [Kayce Basken][KayceBasques] (Technical Writer, Chrome devtools \ & Lighthouse \) erstellt.  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
