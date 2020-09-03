---
description: Erfahren Sie, wie Sie Microsoft Edge und DevTools verwenden, um Speicherprobleme zu finden, die sich auf die Seitenleistung auswirken, wie Speicherverluste, aufblasen des Arbeitsspeichers und häufige Garbage Collections.
title: Beheben von Speicherproblemen
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: ef820353f81eb3fd791433e9c53434dff3b10a60
ms.sourcegitcommit: 63e6d34ff483f3b419a0e271a3513874e6ce6c79
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/02/2020
ms.locfileid: "10992778"
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
    
    :::image type="complex" source="../media/memory-problems-bing-settings-more-tools-browser-task-manager.msft.png" alt-text="Öffnen des Task-Managers des Microsoft Edge-Browsers" lightbox="../media/memory-problems-bing-settings-more-tools-browser-task-manager.msft.png":::
       Abbildung 1: Öffnen des Microsoft Edge-Browser-Task-Managers  
    :::image-end:::  
    
1.  Zeigen Sie auf die Tabellenüberschrift des Microsoft Edge-Browser-Task-Managers, öffnen Sie das Kontextmenü \ (Klicken Sie mit der rechten Maustaste auf \), und aktivieren Sie den **JavaScript-Speicher**.  
    
    :::image type="complex" source="../media/memory-problems-bing-browser-task-manager-javascript-memory.msft.png" alt-text="Aktivieren des JavaScript-Speichers" lightbox="../media/memory-problems-bing-browser-task-manager-javascript-memory.msft.png":::
       Abbildung 2: Aktivieren des JavaScript-Speichers  
    :::image-end:::  
    
Diese beiden Spalten geben Ihnen unterschiedliche Informationen dazu, wie Ihre Seite den Arbeitsspeicher verwendet.  

*   Die **Speicher** Spalte stellt den systemeigenen Speicher dar.  DOM-Knoten werden im systemeigenen Speicher gespeichert.  Wenn dieser Wert immer größer wird, werden DOM-Knoten erstellt.  
*   Die **JavaScript-Speicher** Spalte stellt den js-Heap dar.  Diese Spalte enthält zwei Werte.  Der Wert, an dem Sie interessiert sind, ist die Live-Nummer \ (die Zahl in Klammern \).  Die Live-Nummer gibt an, wie viel Arbeitsspeicher die erreichbaren Objekte auf der Seite verwenden.  Wenn diese Zahl zunimmt, werden entweder neue Objekte erstellt, oder die vorhandenen Objekte werden größer.  

<!--*   live number reference: https://groups.google.com/d/msg/google-chrome-developer-tools/aTMVGoNM0VY/bLmf3l2CpJ8J  -->  

## Visualisieren von Speicherverlusten mithilfe des Leistungs Panels  

Sie können das Leistungs Panel auch als weiteren Ausgangspunkt ihrer Untersuchung verwenden.  Der Leistungs Panel hilft Ihnen, die Speichernutzung einer Seite im Laufe der Zeit zu visualisieren.  

1.  Öffnen Sie in devtools das Panel **Leistung** .  
1.  Aktivieren Sie das Kontrollkästchen **Speicher** .  
1.  [Führen Sie eine Aufzeichnung][DevtoolsEvaluatePerformanceReferenceRecord]aus.  

> [!TIP]
> Es empfiehlt sich, die Aufzeichnung mit einer erzwungenen Garbage Collection zu starten und zu beenden.  Wählen Sie **collect garbage** ![ beim Aufzeichnen die Garbage Collection ][ImageForceGarbageCollectionIcon] -Schaltfläche "Garbage Force sammeln" aus, um die Garbage Collection zu erzwingen.  

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

Jedes Mal, wenn die Schaltfläche, auf die im Code verwiesen wird, gedrückt wird, werden 10000- `div` Knoten an den Dokument Text angefügt, und eine Zeichenfolge mit 1 Million `x` Zeichen wird auf das `x` Array verschoben.  Beim Ausführen des vorherigen Codebeispiels wird eine Aufzeichnung im **Leistungs** Panel wie in der folgenden Abbildung erstellt.  

:::image type="complex" source="../media/memory-problems-glitch-example-1-performance-memory.msft.png" alt-text="Einfaches Wachstum" lightbox="../media/memory-problems-glitch-example-1-performance-memory.msft.png":::
   Abbildung 3: einfaches Wachstum  
:::image-end:::  

Zunächst eine Erläuterung der Benutzeroberfläche.  Das **Heap** Diagramm im Übersichts **Bereich \** (unter **net**\) stellt den js-Heap dar.  Unter dem Übersichtsbereich befindet sich **der Bereich** **Zähler** .  Hier können **Sie die Speicher** Auslastung nach js-Heap (wie **Heap** Diagramm im Übersichtsbereich \), Dokumente, DOM-Knoten, Listener und GPU-Speicher unterteilt sehen.  Wenn Sie ein Kontrollkästchen deaktivieren, wird es aus dem Diagramm ausgeblendet.  

Nun eine Analyse des Codes im Vergleich zur vorherigen Zahl.  Wenn Sie sich den Knoten Zähler \ (das grüne Diagramm \) ansehen, können Sie sehen, dass er mit dem Code sauber übereinstimmt.  Die Anzahl der Knoten nimmt in diskreten Schritten zu.  Sie können davon ausgehen, dass jede Erhöhung der Knotenanzahl ein Aufruf von ist `grow()` .  Das js-Heap Diagramm \ (das blaue Diagramm \) ist nicht so einfach.  In Übereinstimmung mit den bewährten Methoden ist der erste DIP eine erzwungene Garbage Collection \ (erreicht durch **collect garbage** Drücken der ![ Schaltfläche Garbage Force Garbage Collection sammeln ][ImageForceGarbageCollectionIcon] ).  Während die Aufzeichnung fortschreitet, können Sie sehen, dass die JS-Heapgröße Spikes.  Dies ist natürlich und erwartet: der JavaScript-Code erstellt die DOM-Knoten auf jeder Schaltfläche und macht viel Arbeit, wenn die Zeichenfolge von 1 Million-Zeichen erstellt wird.  Der wichtigste Punkt hierbei ist die Tatsache, dass der JS-Heap höher als gestartet ist \ (der "Anfang" hier ist der Punkt nach der erzwungenen Garbage Collection \).  Wenn Sie in der realen Welt dieses Muster mit einer zunehmenden js-Heapgröße oder Knoten Größe gesehen haben, kann dies potenziell einen Speicherverlust definieren.  

<!--todo: the Heap snapshots and Profiles panel are not found in Edge  -->  

## Entdecken von frei gelösten Dom-Strukturspeicher Lecks mit Heap-Schnappschüssen  

Ein DOM-Knoten ist nur Garbage Collection, wenn keine Verweise auf den Knoten aus der DOM-Struktur oder dem auf der Seite ausgeführten JavaScript-Code vorhanden sind.  Ein Knoten wird als "losgelöst" bezeichnet, wenn er aus der DOM-Struktur entfernt wird, aber einige JavaScript-Objekte verweisen weiterhin auf ihn.  Getrennte DOM-Knoten sind eine häufige Ursache für Speicherverluste.  In diesem Abschnitt erfahren Sie, wie Sie die Heap-Profiler in devtools verwenden, um getrennte Knoten zu identifizieren.  

Es folgt ein einfaches Beispiel für getrennte DOM-Knoten.  

```javascript
var detachedTree;

function create() {
    var ul = document.createElement('ul');
    for (var i = 0; i < 10; i++) {
        var li = document.createElement('li');
        ul.appendChild(li);
    }
    detachedTree = ul;
}
document.getElementById('create').addEventListener('click', create);
```  

Wenn Sie im Code auf die Schaltfläche klicken `ul` , wird ein Knoten mit zehn unter `li` geordneten Elementen erstellt.  Auf die Knoten wird vom Code verwiesen, aber Sie sind nicht in der DOM-Struktur vorhanden, daher wird jeder getrennt.  

Heap-Schnappschüsse sind eine Möglichkeit, getrennte Knoten zu identifizieren.  Wie der Name schon sagt, zeigen Heap-Schnappschüsse an, wie der Speicher zwischen den js-Objekten und DOM-Knoten für Ihre Seite zum Zeitpunkt des Schnappschusses verteilt wird.  

Wenn Sie einen Schnappschuss erstellen möchten, öffnen Sie devtools, und wechseln Sie zum **Speicher** Panel, wählen Sie das Optionsfeld **Heap-Snapshot** aus, und drücken Sie dann die Schaltfläche **Schnappschuss aufnehmen** .  

:::image type="complex" source="../media/memory-problems-glitch-example-12-memory-heap-snapshot.msft.png" alt-text="Snapshot des Heaps aufnehmen" lightbox="../media/memory-problems-glitch-example-12-memory-heap-snapshot.msft.png":::
   Abbildung 4: Erstellen eines Heap-Snapshots  
:::image-end:::  

Der Snapshot kann einige Zeit dauern, bis er verarbeitet und geladen wurde.  Wenn Sie den Vorgang beenden, wählen Sie ihn im linken Panel aus. \ (benannte **Heap-Schnappschüsse**\).  

Geben `Detached` Sie in das Textfeld **Klassenfilter** ein, um nach frei gelösten Dom-Strukturen zu suchen.  

:::image type="complex" source="../media/memory-problems-glitch-example-12-memory-heap-snapshot-filter-detached.msft.png" alt-text="Filtern für getrennte Knoten" lightbox="../media/memory-problems-glitch-example-12-memory-heap-snapshot-filter-detached.msft.png":::
   Abbildung 5: Filtern nach getrennten Knoten  
:::image-end:::  

Erweitern Sie die Karat, um eine frei gelöste Struktur zu untersuchen.  

:::image type="complex" source="../media/memory-problems-glitch-example-12-memory-heap-snapshot-filter-detached-expanded.msft.png" alt-text="Untersuchen von getrennten Strukturen" lightbox="../media/memory-problems-glitch-example-12-memory-heap-snapshot-filter-detached-expanded.msft.png":::
   Abbildung 6: untersuchen einer getrennten Struktur  
:::image-end:::  

<!--Nodes highlighted yellow have direct references to them from the JavaScript code.  Nodes highlighted red do not have direct references.  They are only alive because they are part of the tree for the yellow node.  In general, you want to focus on the yellow nodes.  Fix your code so that the yellow node is not alive for longer than it needs to be, and you also get rid of the red nodes that are part of the tree for the yellow node.  -->

Wählen Sie einen Knoten aus, um ihn weiter zu untersuchen.  Im **Objekt** Bereich können Sie weitere Informationen zu dem Code anzeigen, der darauf verweist.  In der folgenden Abbildung können Sie beispielsweise feststellen, dass die `detachedNodes` Variable auf den Knoten verweist.  Um diesen bestimmten Speicherverlust zu beheben, sollten Sie den Code untersuchen, der die Variable verwendet, `detachedUNode` und sicherstellen, dass der Verweis auf den Knoten entfernt wird, wenn er nicht mehr benötigt wird.  

:::image type="complex" source="../media/memory-problems-glitch-example-12-memory-heap-snapshot-filter-detached-expanded-selected.msft.png" alt-text="Untersuchen eines Knotens" lightbox="../media/memory-problems-glitch-example-12-memory-heap-snapshot-filter-detached-expanded-selected.msft.png":::
   Abbildung 7: Untersuchen eines Knotens  
:::image-end:::  

<!--todo: the allocation timeline does not appear in the DevTools in Edge  -->  

## Ermitteln von JS-Heapspeicher Lecks mit Zuordnungs Instrumentation auf Zeitachse  

Die **Zuweisungs Instrumentation auf der Zeitachse** ist ein weiteres Tool, mit dem Sie möglicherweise Speicherverluste in Ihrem js-Heap ermitteln können.  

Demonstrieren Sie die **Zuweisungs Instrumentation auf Zeitachse**  mithilfe des folgenden Codes.  

```javascript
var x = [];
function grow() {
    x.push(new Array(1000000).join('x'));
}
document.getElementById('grow').addEventListener('click', grow);
```  

Jedes Mal, wenn die Schaltfläche, auf die im Code verwiesen wird, gedrückt wird, wird dem Array eine Zeichenfolge von 1 Million-Zeichen hinzugefügt `x` .  

Wenn Sie eine Zuordnungs Instrumentation auf der Zeitachse aufzeichnen möchten, öffnen Sie devtools, wechseln Sie zur Register **Karte Speicher** , wählen Sie das Optionsfeld **Zuweisungs Instrumentation auf Zeitachse** aus, drücken Sie die Schaltfläche **Start** , führen Sie die Aktion aus, die Sie vermuten, dass der Speicherverlust verursacht wird, und drücken Sie dann die Schaltfläche **Aufzeichnung** Beenden der Aufzeichnung beenden, ![ ][ImageStopRecordingIcon] Wenn Sie fertig sind.  

Beachten Sie während der Aufzeichnung, ob blaue Balken in der Zuordnungs Instrumentation auf der Zeitachse angezeigt werden, wie in der folgenden Abbildung dargestellt.  

:::image type="complex" source="../media/memory-problems-glitch-example-13-allocation-timeline-snapshot-all.msft.png" alt-text="Neue Zuweisungen" lightbox="../media/memory-problems-glitch-example-13-allocation-timeline-snapshot-all.msft.png":::
   Abbildung 8: neue Zuweisungen  
:::image-end:::  

Diese blauen Balken stellen neue Speicherzuweisungen dar.  Diese neuen Speicherzuweisungen sind ihre Kandidaten für Speicherverluste.  Sie können auf eine Leiste Zoomen, um den Bereich " **Konstruktor** " zu filtern, sodass nur Objekte angezeigt werden, die während des angegebenen Zeitrahmens reserviert wurden.  

:::image type="complex" source="../media/memory-problems-glitch-example-13-allocation-timeline-snapshot-focused.msft.png" alt-text="Verkleinerte Zuordnungs Zeitachse" lightbox="../media/memory-problems-glitch-example-13-allocation-timeline-snapshot-focused.msft.png":::
   Abbildung 9: Zeitachse mit vergrößerten Zuordnungen  
:::image-end:::  

Erweitern Sie das Objekt, und wählen Sie den Wert aus, um weitere Details im **Objekt** Bereich anzuzeigen.  In der folgenden Abbildung können Sie beispielsweisedurch Anzeigen der Details des Objekts, das neu zugeordnet wurde, sehen, dass es der `x` Variablen im Bereich zugeordnet wurde `Window` .  

:::image type="complex" source="../media/memory-problems-glitch-example-13-allocation-timeline-snapshot-focused-constructor-expanded.msft.png" alt-text="Objektdetails" lightbox="../media/memory-problems-glitch-example-13-allocation-timeline-snapshot-focused-constructor-expanded.msft.png":::
   Abbildung 10: Objektdetails  
:::image-end:::  

## Untersuchen der Speicherzuweisung nach Funktion  

Verwenden Sie den Profilerstellungs-Typ der **Zuordnungs Stichprobe** , um die Speicherzuweisung nach JavaScript-Funktion anzuzeigen.  

:::image type="complex" source="../media/memory-problems-glitch-example-05-memory-allocation-sampling.msft.png" alt-text="Sampling für Daten Satz Zuteilung" lightbox="../media/memory-problems-glitch-example-05-memory-allocation-sampling.msft.png":::
   Abbildung 11: Sampling zur Daten Satz Zuteilung  
:::image-end:::  

1.  Aktivieren Sie das Optionsfeld **Zuweisungs Sampling** .  Wenn auf der Seite eine Arbeitskraft vorhanden ist, können Sie diese über das Dropdownmenü neben der Schaltfläche **Start** als Profil Ziel auswählen.  
1.  Drücken Sie die Schaltfläche **Start** .  
1.  Führen Sie die Aktionen auf der Seite aus, die Sie untersuchen möchten.  
1.  Drücken Sie die **Stopp** -Taste, wenn Sie alle Ihre Aktionen beendet haben.  

DevTools zeigt eine Aufschlüsselung der Speicherzuweisung nach Funktion.  Die Standardansicht ist **schwer (unten nach oben)**, in der die Funktionen angezeigt werden, die den größten Arbeitsspeicher oben zugewiesen haben.  

:::image type="complex" source="../media/memory-problems-glitch-example-05-memory-allocation-sampling-heavy-bottom-up.msft.png" alt-text="Zuordnungs Stichproben" lightbox="../media/memory-problems-glitch-example-05-memory-allocation-sampling-heavy-bottom-up.msft.png":::
   Abbildung 12: Zuordnungs Stichproben  
:::image-end:::  

## Häufige Garbage Collections erkennen  

Wenn Ihre Seite häufig angehalten wird, haben Sie möglicherweise Probleme mit der Garbage Collection.  

Sie können entweder den Microsoft Edge-Browser-Task-Manager oder Leistungs Speicher Aufzeichnungen verwenden, um häufige Garbage Collection zu erkennen.  Im Microsoft Edge-Browser Task-Manager stellen häufig steigende und fallende **Speicher** -oder **JavaScript-Speicher** Werte häufige Garbage Collection dar.  In Leistungs Aufzeichnungen zeigen häufige Änderungen \ (steigende und fallende \) zu den js-Heap-oder Knotenanzahl-Diagrammen auf häufige Garbage Collection.  

Nachdem Sie das Problem identifiziert haben, können Sie eine **Zuordnungs Instrumentation für die Zeitachsen** Aufzeichnung verwenden, um herauszufinden, wo Speicher reserviert wird und welche Funktionen die Zuweisungen verursachen.  

<!-- image links -->  

[ImageForceGarbageCollectionIcon]: ../media/collect-garbage-icon.msft.png  
[ImageStopRecordingIcon]: ../media/stop-recording-icon.msft.png  

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
