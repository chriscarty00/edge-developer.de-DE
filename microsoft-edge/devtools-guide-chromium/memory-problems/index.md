---
description: Erfahren Sie, wie Microsoft Edge und DevTools verwendet werden, um Speicherprobleme zu finden, die sich auf die Seitenleistung auswirken, z. B. Speicherverluste, Speicherbloat und häufige Garbage Collections.
title: Beheben von Arbeitsspeicherproblemen
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, Entwicklungstools
ms.openlocfilehash: 3b2405d23dd6ee349484c9ba66d195e3ed12144b
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/13/2021
ms.locfileid: "11565029"
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
# <a name="fix-memory-problems"></a>Beheben von Arbeitsspeicherproblemen  

Erfahren Sie, wie Microsoft Edge und DevTools verwendet werden, um Speicherprobleme zu finden, die sich auf die Seitenleistung auswirken, z. B. Speicherverluste, Speicherbloat und häufige Garbage Collections.  

### <a name="summary"></a>Zusammenfassung  

*   Erfahren Sie, wie viel Arbeitsspeicher Ihre Seite derzeit mit dem Microsoft Edge-Task-Manager verwendet.  
*   Visualisieren Sie die Speichernutzung im Laufe der Zeit mit **dem Speicherbereich.**  
*   Identifizieren von getrennten DOM-Baumstrukturen \(eine häufige Ursache für Speicherverluste\) mit **Heap-Momentaufnahme**.  
*   Erfahren Sie, wann neuer Arbeitsspeicher im JavaScript-Heap \(JS-Heap\) mit **Zuweisungsinstrumentation auf der Zeitachse zugewiesen wird.**  

## <a name="overview"></a>Übersicht  

Im Sinne des **RAIL-Leistungsmodells** sollten ihre Benutzer im Mittelpunkt Ihrer Leistungsbemühungen stehen.  

<!--todo: add RAIL section when available  -->  

Speicherprobleme sind wichtig, da sie häufig von Benutzern zu finden sind.  Benutzer können Speicherprobleme auf folgende Weise wahrnehmen:  

*   **Die Leistung einer Seite wird im Laufe der Zeit**immer schlechter.  Dies ist möglicherweise ein Symptom für einen Speicherverlust.  Ein Speicherverlust liegt vor, wenn ein Fehler auf der Seite dazu führt, dass die Seite im Laufe der Zeit immer mehr Arbeitsspeicher verwendet.  
*   **Die Leistung einer Seite ist konstant schlecht.**  Dies ist möglicherweise ein Symptom der Speicherbloat.  Der Arbeitsspeicher wird aufgebläht, wenn eine Seite mehr Arbeitsspeicher verbraucht, als für eine optimale Seitengeschwindigkeit erforderlich ist.  
*   **Die Leistung einer Seite wird verzögert oder scheint häufig anzuhalten.**  Dies ist möglicherweise ein Symptom für häufige Garbage Collections.  Die Garbage Collection wird beim Freigeben des Arbeitsspeichers durch den Browser verwendet.  Der Browser entscheidet, wann dies geschieht.  Während der Auflistungen werden alle ausgeführten Skripts angehalten.  Wenn der Browser also sehr viel Garbage Collection sammelt, wird die Skriptlaufzeit viel angehalten.  

### <a name="memory-bloat-how-much-is-too-much"></a>Speicherbloat: Wie viel ist "zu viel"?  

Ein Speicherverlust ist einfach zu definieren.  Wenn eine Website zunehmend mehr Arbeitsspeicher verwendet, liegt ein Leck vor.  Der Speicherbloat ist jedoch etwas schwieriger zu anheften.  Was gilt als "Zu viel Arbeitsspeicher" verwenden?  

Es gibt hier keine schwierigen Zahlen, da unterschiedliche Geräte und Browser unterschiedliche Funktionen haben.  Dieselbe Seite, die reibungslos auf einem High-End-Smartphone ausgeführt wird, kann auf einem Low-End-Smartphone abstürzen.  

Der Schlüssel hier ist, das RAIL-Modell zu verwenden und sich auf Ihre Benutzer zu konzentrieren.  Erfahren Sie, welche Geräte bei Ihren Benutzern beliebt sind, und testen Sie dann Ihre Seite auf diesen Geräten.  Wenn die Erfahrung konsistent schlecht ist, übersteigt die Seite möglicherweise die Speicherfunktionen dieser Geräte.  

## <a name="monitor-memory-use-in-realtime-with-the-microsoft-edge-browser-task-manager"></a>Überwachen der Speichernutzung in Echtzeit mit dem Microsoft Edge Browser Task Manager  

Verwenden Sie Microsoft Edge Browser Task Manager als Ausgangspunkt für ihre Speicherproblemuntersuchung.  Der Microsoft Edge Browser Task Manager ist ein Echtzeitmonitor, der Ihnen mitteilt, wie viel Arbeitsspeicher eine Seite derzeit verwendet.  

1.  Wählen Oder navigieren Sie zum hauptmenü Microsoft Edge und wählen Sie Weitere Tools Browser Task Manager aus, um den `Shift` + `Esc` ****  >  **** Microsoft Edge-Task-Manager zu öffnen.  
    
    :::image type="complex" source="../media/memory-problems-bing-settings-more-tools-browser-task-manager.msft.png" alt-text="Öffnen des Microsoft Edge Browser Task Manager" lightbox="../media/memory-problems-bing-settings-more-tools-browser-task-manager.msft.png":::
       Abbildung 1: Öffnen Microsoft Edge Browser Task Manager  
    :::image-end:::  
    
1.  Zeigen Sie auf die Tabellenkopfzeile des Microsoft Edge-Browser-Task-Managers, öffnen Sie das Kontextmenü \(klicken Sie mit der rechten Maustaste\), und aktivieren Sie **den JavaScript-Speicher**.  
    
    :::image type="complex" source="../media/memory-problems-bing-browser-task-manager-javascript-memory.msft.png" alt-text="Aktivieren des JavaScript-Speichers" lightbox="../media/memory-problems-bing-browser-task-manager-javascript-memory.msft.png":::
       Abbildung 2: Aktivieren des JavaScript-Speichers  
    :::image-end:::  
    
Diese beiden Spalten geben Ihnen unterschiedliche Informationen dazu, wie Ihre Seite Arbeitsspeicher verwendet.  

*   Die **Spalte Arbeitsspeicher** stellt systemeigenen Arbeitsspeicher dar.  DOM-Knoten werden im systemeigenen Speicher gespeichert.  Wenn dieser Wert zunimmt, werden DOM-Knoten erstellt.  
*   Die **Spalte JavaScript Memory** stellt den JS-Heap dar.  Diese Spalte enthält zwei Werte.  Der Wert, an dem Sie interessiert sind, ist die Livenummer \(die Zahl in Klammern\).  Die Livenummer gibt an, wie viel Arbeitsspeicher die erreichbaren Objekte auf Ihrer Seite verwenden.  Wenn diese Anzahl zunimmt, werden entweder neue Objekte erstellt, oder die vorhandenen Objekte werden größer.  

<!--*   live number reference: https://groups.google.com/d/msg/google-chrome-developer-tools/aTMVGoNM0VY/bLmf3l2CpJ8J  -->  

## <a name="visualize-memory-leaks-with-performance-panel"></a>Visualisieren von Speicherverlusten mit dem Leistungsbereich  

Sie können auch den Bereich "Leistung" als weiteren Ausgangspunkt in Ihrer Untersuchung verwenden.  Der Bereich Leistung hilft Ihnen, die Speichernutzung einer Seite im Laufe der Zeit zu visualisieren.  

1.  Öffnen Sie **den Bereich** Leistung auf DevTools.  
1.  Aktivieren Sie **das Kontrollkästchen** Speicher.  
1.  [Nehmen Sie eine Aufzeichnung vor.][DevtoolsEvaluatePerformanceReferenceRecord]  

> [!TIP]
> Es ist eine bewährte Methode, ihre Aufzeichnung mit einer erzwungenen Garbage Collection zu starten und zu beenden.  Um die Garbage Collection zu erzwingen, wählen **Sie** während der Aufzeichnung die Schaltfläche Garbage Force Garbage Collection ![ sammeln ][ImageForceGarbageCollectionIcon] aus.  

Um Speicheraufzeichnungen zu veranschaulichen, berücksichtigen Sie den folgenden Code:  

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

Jedes Mal, wenn die Schaltfläche ausgewählt wird, auf die im Code verwiesen wird, werden zehntausend Knoten an den Dokumenttext angefügt, und eine Zeichenfolge von einer Million Zeichen wird auf das `div` `x` Array `x` gedrückt.  Beim Ausführen des vorherigen Codebeispiels wird eine Aufzeichnung im **Leistungsbereich** wie in der folgenden Abbildung erstellt.  

:::image type="complex" source="../media/memory-problems-glitch-example-1-performance-memory.msft.png" alt-text="Einfaches Wachstum" lightbox="../media/memory-problems-glitch-example-1-performance-memory.msft.png":::
   Abbildung 3: Einfaches Wachstum  
:::image-end:::  

Zunächst eine Erläuterung der Benutzeroberfläche.  Das **HEAP-Diagramm** im **Übersichtsbereich** \(unter **NET**\) stellt den JS-Heap dar.  Unterhalb des **Bereichs Übersicht** befindet sich der **Bereich Counter.**  Die Speicherauslastung wird nach JS-Heap \(identisch **** mit **HEAP-Diagramm** im Übersichtsbereich\), Dokumenten, DOM-Knoten, Listenern und GPU-Speicher aufgeschlüsselt.  Deaktivieren Sie ein Kontrollkästchen, um es aus dem Diagramm auszublenden.  

Nun eine Analyse des Codes im Vergleich zur vorherigen Abbildung.  Wenn Sie den Knotenzähler \(das grüne Diagramm\) überprüfen, wird er mit dem Code sauber nachgeschlagen.  Die Knotenanzahl nimmt in separaten Schritten zu.  Sie können davon ausgehen, dass jede Erhöhung der Knotenanzahl ein Aufruf von `grow()` ist.  Das JS-Heapdiagramm \(das blaue Diagramm\) ist nicht so einfach.  In Einklang mit bewährten Methoden ist der erste Dip **** tatsächlich eine erzwungene Garbage Collection \(Wählen Sie die Schaltfläche Garbage ![ Force Garbage Collection ][ImageForceGarbageCollectionIcon] sammeln\).  Im Verlauf der Aufzeichnung werden die Spikes der JS-Heapgröße angezeigt.  Dies ist natürlich und erwartet: Der JavaScript-Code erstellt die DOM-Knoten auf jeder schaltfläche, die Sie auswählen, und macht viel Arbeit, wenn die Zeichenfolge von einer Million Zeichen erstellt wird.  Der Schlüssel hier ist die Tatsache, dass der JS-Heap höher endet, als er begonnen hat \(der "Anfang" hier ist der Punkt nach der erzwungenen Garbage Collection\).  Wenn Sie in der realen Welt dieses Muster der Zunehmenden Größe des JS-Heaps oder der Knotengröße gesehen haben, kann dies potenziell einen Speicherverlust definieren.  

<!--todo: the Heap snapshots and Profiles panel are not found in Edge  -->  

## <a name="discover-detached-dom-tree-memory-leaks-with-heap-snapshots"></a>Ermitteln getrennter Speicherverluste der DOM-Struktur mit Heap-Momentaufnahmen  

Ein DOM-Knoten wird nur dann gesammelt, wenn es keine Verweise auf den Knoten aus der DOM-Struktur oder dem JavaScript-Code gibt, der auf der Seite ausgeführt wird.  Ein Knoten wird als "getrennt" bezeichnet, wenn er aus der DOM-Struktur entfernt wird, aber einige JavaScript-Elemente verweisen weiterhin auf ihn.  Getrennte DOM-Knoten sind eine häufige Ursache für Speicherverluste.  In diesem Abschnitt erfahren Sie, wie Sie die Heapprofiler in DevTools verwenden, um getrennte Knoten zu identifizieren.  

Hier ist ein einfaches Beispiel für getrennte DOM-Knoten.  

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

Wenn Sie die Schaltfläche auswählen, auf die im Code verwiesen wird, wird `ul` ein Knoten mit zehn untergingen Knoten `li` erstellt.  Auf die Knoten wird durch den Code verwiesen, sie sind jedoch nicht in der DOM-Struktur vorhanden, sodass jede getrennt ist.  

Heapmomentaufnahmen sind eine Möglichkeit, getrennte Knoten zu identifizieren.  Wie der Name schon sagt, zeigen Heapmomentaufnahmen, wie der Arbeitsspeicher zum Zeitpunkt der Momentaufnahme auf die JS-Objekte und DOM-Knoten für Ihre Seite verteilt wird.  

Um eine Momentaufnahme zu erstellen, **** öffnen Sie DevTools, und navigieren Sie zum Speicherbereich, wählen Sie das Optionsfeld Heap-Momentaufnahme aus, > **Momentaufnahme erstellen.** ****  

:::image type="complex" source="../media/memory-problems-glitch-example-12-memory-heap-snapshot.msft.png" alt-text="Erstellen einer Heapmomentaufnahme" lightbox="../media/memory-problems-glitch-example-12-memory-heap-snapshot.msft.png":::
   Abbildung 4: Erstellen einer Heapmomentaufnahme  
:::image-end:::  

Die Momentaufnahme kann einige Zeit zum Verarbeiten und Laden dauern.  Nachdem sie abgeschlossen ist, wählen Sie sie im linken Bereich \(benannte **HEAP-MOMENTAUFNAHMEN**\) aus.  

Geben `Detached` Sie in das Textfeld **Klassenfilter** ein, um nach getrennten DOM-Baumstrukturen zu suchen.  

:::image type="complex" source="../media/memory-problems-glitch-example-12-memory-heap-snapshot-filter-detached.msft.png" alt-text="Filtern nach getrennten Knoten" lightbox="../media/memory-problems-glitch-example-12-memory-heap-snapshot-filter-detached.msft.png":::
   Abbildung 5: Filtern nach getrennten Knoten  
:::image-end:::  

Erweitern Sie die Karate, um eine getrennte Struktur zu untersuchen.  

:::image type="complex" source="../media/memory-problems-glitch-example-12-memory-heap-snapshot-filter-detached-expanded.msft.png" alt-text="Untersuchen der getrennten Struktur" lightbox="../media/memory-problems-glitch-example-12-memory-heap-snapshot-filter-detached-expanded.msft.png":::
   Abbildung 6: Untersuchen der getrennten Struktur  
:::image-end:::  

<!--Nodes highlighted yellow have direct references to them from the JavaScript code.  Nodes highlighted red do not have direct references.  They are only alive because they are part of the tree for the yellow node.  In general, you want to focus on the yellow nodes.  Fix your code so that the yellow node is not alive for longer than it needs to be, and you also get rid of the red nodes that are part of the tree for the yellow node.  -->

Wählen Sie einen Knoten aus, um ihn weiter zu untersuchen.  Im Bereich **Objekte** können Sie weitere Informationen zu dem Code überprüfen, auf den sie verweisen.  In der folgenden Abbildung bezieht sich die Variable `detachedNodes` beispielsweise auf den Knoten.  Zum Beheben des speicherlecks sollten Sie den Code untersuchen, der die Variable verwendet, und sicherstellen, dass der Verweis auf den Knoten entfernt wird, wenn er `detachedUNode` nicht mehr benötigt wird.  

:::image type="complex" source="../media/memory-problems-glitch-example-12-memory-heap-snapshot-filter-detached-expanded-selected.msft.png" alt-text="Untersuchen eines Knotens" lightbox="../media/memory-problems-glitch-example-12-memory-heap-snapshot-filter-detached-expanded-selected.msft.png":::
   Abbildung 7: Untersuchen eines Knotens  
:::image-end:::  

<!--todo: the allocation timeline does not appear in the DevTools in Edge  -->  

## <a name="identify-js-heap-memory-leaks-with-allocation-instrumentation-on-timeline"></a>Identifizieren von JS-Heapspeicherlecks mit Zuweisungsinstrumentation auf der Zeitachse  

**Die Zuordnungsinstrumentation auf der Zeitachse** ist ein weiteres Tool, mit dem Sie Speicherverluste im JS-Heap nachverfolgen können.  

Demonstrieren **Sie die Zuordnungsinstrumentation auf der Zeitachse**  mithilfe des folgenden Codes.  

```javascript
var x = [];
function grow() {
    x.push(new Array(1000000).join('x'));
}
document.getElementById('grow').addEventListener('click', grow);
```  

Jedes Mal, wenn die Schaltfläche, auf die im Code verwiesen wird, gedrückt wird, wird dem Array eine Zeichenfolge von einer Million Zeichen `x` hinzugefügt.  

Wenn Sie eine Zuordnungsinstrumentation auf der Zeitachse aufzeichnen möchten, öffnen Sie DevTools, navigieren Sie zum Speicherbereich, wählen Sie die Option **Zuordnungsinstrumentation** auf der Zeitachse aus, klicken Sie auf die **Schaltfläche Start,** führen Sie die Aktion aus, von der Sie vermuten, dass der Speicherverlust verursacht wird, und wählen Sie dann die Schaltfläche Aufzeichnungsstopp des Heapprofils beenden aus, sobald Sie fertig **** **** ![ ][ImageStopRecordingIcon] sind.  

Beachten Sie bei der Aufzeichnung, ob blaue Balken auf der Zuordnungsinstrumentation auf der Zeitachse angezeigt werden, wie in der folgenden Abbildung dargestellt.  

:::image type="complex" source="../media/memory-problems-glitch-example-13-allocation-timeline-snapshot-all.msft.png" alt-text="Neue Zuordnungen" lightbox="../media/memory-problems-glitch-example-13-allocation-timeline-snapshot-all.msft.png":::
   Abbildung 8: Neue Zuordnungen  
:::image-end:::  

Diese blauen Balken stellen neue Speicherzuweisungen dar.  Diese neuen Speicherzuweisungen sind Ihre Kandidaten für Speicherverluste.  Sie können eine Leiste vergrößern, **** um den Konstruktorbereich so zu filtern, dass nur Objekte angezeigt werden, die während des angegebenen Zeitrahmens zugewiesen wurden.  

:::image type="complex" source="../media/memory-problems-glitch-example-13-allocation-timeline-snapshot-focused.msft.png" alt-text="Zeitachse für die verkleinerte Zuweisung" lightbox="../media/memory-problems-glitch-example-13-allocation-timeline-snapshot-focused.msft.png":::
   Abbildung 9: Zeitachse der verkleinerten Zuweisung  
:::image-end:::  

Erweitern Sie das Objekt, und wählen Sie den Wert aus, um weitere Details im **Objektbereich anzuzeigen.**  In der folgenden Abbildung wird beispielsweise in den Details des neu zugeordneten Objekts angegeben, dass es der Variablen im `x` Bereich zugeordnet `Window` wurde.  

:::image type="complex" source="../media/memory-problems-glitch-example-13-allocation-timeline-snapshot-focused-constructor-expanded.msft.png" alt-text="Objektdetails" lightbox="../media/memory-problems-glitch-example-13-allocation-timeline-snapshot-focused-constructor-expanded.msft.png":::
   Abbildung 10: Objektdetails  
:::image-end:::  

## <a name="investigate-memory-allocation-by-function"></a>Untersuchen der Speicherzuweisung nach Funktion  

Verwenden Sie den **Zuweisungsstichprobeprofiltyp,** um die Speicherzuweisung nach JavaScript-Funktion anzeigen zu können.  

:::image type="complex" source="../media/memory-problems-glitch-example-05-memory-allocation-sampling.msft.png" alt-text="Sampling der Datensatzzuweisung" lightbox="../media/memory-problems-glitch-example-05-memory-allocation-sampling.msft.png":::
   Abbildung 11: Sampling der Datensatzzuweisung  
:::image-end:::  

1.  Wählen Sie das **Optionsfeld Zuweisungsstichprobe** aus.  Wenn sich auf der Seite ein Mitarbeiter befindet, können Sie dies über das Dropdownmenü neben der Schaltfläche Start als **Profilerstellungsziel** auswählen.  
1.  Wählen Sie die **Schaltfläche Start** aus.  
1.  Führen Sie die Aktionen auf der Webseite aus, die Sie untersuchen möchten.  
1.  Wählen Sie **die Schaltfläche** Beenden aus, wenn Sie alle Aktionen abgeschlossen haben.  

DevTools zeigt eine Aufschlüsselung der Speicherzuweisung nach Funktion.  Die Standardansicht ist **Heavy (Bottom Up),** die die Funktionen anzeigt, die den größten Arbeitsspeicher oben zugewiesen haben.  

:::image type="complex" source="../media/memory-problems-glitch-example-05-memory-allocation-sampling-heavy-bottom-up.msft.png" alt-text="Zuweisungss sampling" lightbox="../media/memory-problems-glitch-example-05-memory-allocation-sampling-heavy-bottom-up.msft.png":::
   Abbildung 12: Zuweisungsstichprobe  
:::image-end:::  

## <a name="spot-frequent-garbage-collections"></a>Häufige Garbage Collections erkennen  

Wenn Ihre Seite häufig angehalten wird, können Probleme mit der Garbage Collection auftreten.  

Sie können entweder den Microsoft Edge-Task-Manager oder Leistungsspeicheraufzeichnungen verwenden, um häufige Garbage Collection zu erkennen.  Im Microsoft Edge Browser Task Manager stellen häufig steigende und absteigende **Speicher-** oder **JavaScript-Speicherwerte** eine häufige Garbage Collection dar.  In Leistungsaufzeichnungen deuten häufige Änderungen \(aufsteigend und fallend\) an den JS-Heap- oder Knotenanzahldiagrammen auf häufige Garbage Collection hin.  

Nachdem Sie das Problem erkannt haben, **** können Sie eine Allocation-Instrumentierung für die Zeitachsenaufzeichnung verwenden, um herauszufinden, wo Speicher zugewiesen wird und welche Funktionen die Zuweisungen verursachen.  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageForceGarbageCollectionIcon]: ../media/collect-garbage-icon.msft.png  
[ImageStopRecordingIcon]: ../media/stop-recording-icon.msft.png  

<!-- links -->  

[DevtoolsEvaluatePerformanceReferenceRecord]: /microsoft-edge/devtools-guide-chromium/evaluate-performance/reference#record-performance "Datensatzleistung – Referenz zur Leistungsanalyse"  

<!--[RAIL]: /profile/evaluate-performance/rail  -->
<!--[recording]: /profile/evaluate-performance/timeline-tool#make-a-recording ""  -->  

<!--[hngd]: https://jsfiddle.net/kaycebasques/tmtbw8ef/  -->  

> [!NOTE]
> Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.  
> Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/memory-problems/index) und wird von [Kayce Basken][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\) verfasst.  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  
