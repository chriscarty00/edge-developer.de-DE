---
title: Aufzeichnen von Heap-Snapshots
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: 183482660ed5fc50862dfd2cce7209384fee93e3
ms.sourcegitcommit: b88d2a55a59db8373ff2bac275d3730977bf19c9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/01/2020
ms.locfileid: "10986171"
---
<!-- Copyright Meggin Kearney 

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->

# Aufzeichnen von Heap-Snapshots  

Erfahren Sie, wie Sie Heap-Snapshots mit dem Microsoft Edge devtools-Heap Profiler aufzeichnen und Speicherverluste finden.  

Der Microsoft Edge devtools-Heap Profiler zeigt die Speicherverteilung nach den JavaScript-Objekten und den zugehörigen DOM-Knoten Ihrer Seite an.  Verwenden Sie es, um Snapshots des JavaScript-Heaps zu erstellen, Speicher Diagramme zu analysieren, Schnappschüsse zu vergleichen und Speicherverluste zu finden.  Siehe auch Objekte, die die [Struktur beibehalten][DevtoolsMemoryProblems101ObjectsRetainingTree].  

## Erstellen einer Momentaufnahme  

Wählen Sie im **Speicher** Panel **Schnappschuss aufnehmen**und dann auf **Start**.  Sie können auch `Ctrl` + `E` \ (Windows \) oder `Cmd` + `E` \ (macOS \) drücken.  

:::image type="complex" source="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots.msft.png" alt-text="Auswählen des Profil Erstellungs Typs" lightbox="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots.msft.png":::
   Auswählen des Profil Erstellungs Typs  
:::image-end:::  

**Snapshots** werden zunächst im Speicher des Renderer-Prozesses gespeichert.  Schnappschüsse werden bei Bedarf an devtools übertragen, wenn Sie auf das Schnappschuss Symbol klicken, um es anzuzeigen.  

Nachdem der Schnappschuss in devtools geladen und analysiert wurde, wird die Zahl unterhalb des Snapshot-Titels angezeigt und zeigt die [Gesamtgröße der erreichbaren JavaScript-Objekte an][DevtoolsMemoryProblems101ObjectSizes].  

:::image type="complex" source="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-all.msft.png" alt-text="Gesamtgröße der erreichbaren Objekte" lightbox="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-all.msft.png":::
   Gesamtgröße der erreichbaren Objekte  
:::image-end:::  

> [!NOTE]
> In Schnappschüssen sind nur erreichbare Objekte enthalten.  Außerdem beginnt das Erstellen eines Snapshots immer mit einer Garbage Collection.  

## Löschen von Schnappschüssen  

Klicken Sie auf Symbol " **alle Profile löschen** ", um Schnappschüsse zu entfernen \ (sowohl aus devtools als auch aus dem Speicher, der dem Renderer-Prozess zugeordnet ist).  

:::image type="complex" source="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-all-hover-clear-all-profiles.msft.png" alt-text="Entfernen von Schnappschüssen" lightbox="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-all-hover-clear-all-profiles.msft.png":::
   Entfernen von Schnappschüssen  
:::image-end:::  

Beim Schließen des devtools-Fensters werden keine Profile aus dem Speicher gelöscht, der dem Renderer-Prozess zugeordnet ist.  Beim erneuten Öffnen von devtools werden alle zuvor aufgenommenen Schnappschüsse wieder in der Liste der Schnappschüsse angezeigt.  

> [!NOTE]
> Probieren Sie dieses Beispiel für [verstreute Objekte][GlitchDevtoolsMemoryExample03] aus, und erstellen Sie ein Profil mit dem Heap Profiler.  Es sollte eine Anzahl von \ (Object \)-Element Zuweisungen angezeigt werden.  

## Anzeigen von Schnappschüssen  

Sie können Schnappschüsse aus unterschiedlichen Perspektiven für verschiedene Aufgaben anzeigen.  

**Zusammenfassungsansicht** zeigt Objekte, die nach dem Namen des Konstruktors gruppiert sind.  Verwenden Sie es, um Objekte \ (und die Speichernutzung \) basierend auf dem Typ nach konstruktornamen gruppiert zu jagen.  Dies ist besonders hilfreich für das **Aufspüren von Dom-Lecks**.

<!--todo: add profile memory problems memory diagnosis (tracking down DOM leaks) section when available  -->  

**Vergleichsansicht**.  Zeigt den Unterschied zwischen zwei Schnappschüssen an.  Verwenden Sie diese Funktion, um zwei \ (oder mehr \) Speicher-Snapshots von vor und nach einem Vorgang zu vergleichen.  Wenn Sie das Delta in freiem Arbeitsspeicher und Verweisanzahl prüfen, können Sie das vorhanden sein und die Ursache für einen Speicherverlust bestätigen.  

**Einkapselungs Ansicht**.  Ermöglicht das Erforschen von Heap Inhalten.  Die **Einkapselungs Ansicht** bietet eine bessere Sicht auf die Objektstruktur und hilft, Objekte zu analysieren, auf die im globalen Namespace \ (Window \) verwiesen wird, um herauszufinden, welche Objekte in der Nähe sind.  Verwenden Sie es, um Verschlüsse zu analysieren und in Ihre Objekte auf einem niedrigeren Niveau zu tauchen.  

Um zwischen den Ansichten zu wechseln, verwenden Sie die Auswahl oben in der Ansicht.  

:::image type="complex" source="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-view-dropdown.msft.png" alt-text="Wechseln der Ansicht-Auswahl" lightbox="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-view-dropdown.msft.png":::
   Wechseln der Ansicht-Auswahl  
:::image-end:::  

> [!NOTE]
> Nicht alle Eigenschaften werden auf dem JavaScript-Heap gespeichert.  Mit Gettern implementierte Eigenschaften, die systemeigenen Code ausführen, werden nicht erfasst.  Auch nicht-Zeichenfolgenwerte wie Zahlen werden nicht erfasst.  

### Zusammenfassungsansicht  

Zunächst wird in der Zusammenfassungsansicht eine Momentaufnahme geöffnet, in der die Objektergebnisse angezeigt werden, die möglicherweise erweitert werden, um Instanzen anzuzeigen:  

:::image type="complex" source="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-constructor-retainers.msft.png" alt-text="Zusammenfassungsansicht" lightbox="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-constructor-retainers.msft.png":::
   **Zusammenfassungs** Ansicht  
:::image-end:::  

Einträge auf oberster Ebene sind "Total"-Zeilen.  

| Einträge auf oberster Ebene | Beschreibung |  
|:--- |:--- |  
| **Konstruktor** | Stellt alle mit diesem Konstruktor erstellten Objekte dar.  |  
| **Entfernung** | zeigt den Abstand zum Stamm mithilfe des kürzesten einfachen Pfads von Knoten an.  |  
| **Flache Größe** | Zeigt die Summe der flachen Größen aller Objekte an, die von einer bestimmten Konstruktorfunktion erstellt wurden.  Die flache Größe ist die Größe des Speichers, der für ein Objekt reserviert ist \ (im allgemeinen weisen Arrays und Zeichenfolgen größere flache Größen auf \).  Siehe auch [Objektgrößen][DevtoolsMemoryProblems101ObjectSizes].  |  
| **Beibehaltungs Größe** | Zeigt die maximale Beibehaltungs Größe für den gleichen Satz von Objekten an.  Die Größe des Arbeitsspeichers, der nach dem Löschen eines Objekts freigegeben werden kann \ (und die abhängigen Personen sind nicht mehr erreichbar \) wird als Beibehaltungs Größe bezeichnet.  Siehe auch [Objektgrößen][DevtoolsMemoryProblems101ObjectSizes].  |  

<!--| **Number of object instances** | Displayed in the # column.  |  -->  

Nachdem Sie eine Gesamtzeile in der oberen Ansicht erweitert haben, werden alle Instanzen angezeigt.  Für jede Instanz werden die flachen und gespeicherten Größen in den entsprechenden Spalten angezeigt.  Die Zahl hinter dem `@` Zeichen ist die eindeutige ID des Objekts, die es Ihnen ermöglicht, Heap-Schnappschüsse pro Objekt zu vergleichen.  

Beachten Sie, dass gelbe Objekte JavaScript-Bezüge aufweisen und rote Objekte getrennte Knoten sind, auf die von einer mit einem gelben Hintergrund verwiesen wird.  

**Was entsprechen die verschiedenen Konstruktoren \ (Group \)-Einträge im Heap Profiler?**  

:::image type="complex" source="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-constructor-highlight.msft.png" alt-text="Konstruktorgruppen" lightbox="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-constructor-highlight.msft.png":::
   **Konstruktorgruppen**  
:::image-end:::  

| Konstruktor \ (Gruppe \) Eintrag | Beschreibung |  
|:--- |:--- |  
| **\ (globale Eigenschaft \)** | Die zwischen Objekte zwischen einem globalen Objekt \ (wie `window` \) und einem Objekt, auf das verwiesen wird.  Wenn ein Objekt mit einem Konstruktor erstellt `Person` und von einem globalen Objekt gehalten wird, sieht der Beibehaltungs Pfad wie folgt aus `[global] > \(global property\) > Person` .  Dies steht im Gegensatz zur Norm, bei der sich Objekte direkt gegenseitig referenzieren.  Zwischen Objekte bestehen aus Leistungsgründen.  Globals werden regelmäßig geändert, und Eigenschaftenzugriffs Optimierungen erledigen eine gute Aufgabe für nicht-globale Objekte, die nicht für Globals gelten.  |  
| **\ (Roots \)** | Die Stamm Einträge in der Beibehaltungs Strukturansicht sind die Entitäten, die auf das ausgewählte Objekt verweisen.  Die Einträge können auch Verweise sein, die vom Modul für modulspezifische Zwecke erstellt wurden.  Das Modul hat Zwischenspeicher, die auf Objekte verweisen, aber alle derartigen Bezüge sind schwach und verhindern nicht, dass ein Objekt gesammelt wird, da es keine wirklich starken Bezüge gibt.  |  
| **\ (Closure \)** | Die Anzahl von Verweisen auf eine Gruppe von Objekten über Funktions Closures.  |  
| **\ (Array, Zeichenfolge, Zahl, regexp \)** | Eine Liste von Objekttypen mit Eigenschaften, die auf ein Array, eine Zeichenfolge, eine Zahl oder einen regulären Ausdruck verweisen.  |  
| **\ (kompilierter Code \)** | Alles im Zusammenhang mit kompiliertem Code.  Das Skript ähnelt einer Funktion, entspricht aber einem `<script>` Textkörper.  SharedFunctionInfos \ (SFI \) sind Objekte, die zwischen Funktionen und kompiliertem Code stehen.  Funktionen haben in der Regel einen Kontext, während SFIs nicht.  |  
| **HTMLDivElement**, **HTMLAnchorElement**, **DocumentFragment**usw.  | Verweise auf Elemente oder Dokument Objekte eines bestimmten Typs, auf die der Code verweist.  |  

<!--todo: add heap profiling summary section when available -->  

### Vergleichsansicht  

Suchen Sie durchgesickerte Objekte, indem Sie mehrere Schnappschüsse miteinander vergleichen.  Wenn Sie sicherstellen möchten, dass ein bestimmter Anwendungsvorgang keine Undichtigkeiten verursacht \ (beispielsweise in der Regel ein paar von direkten und umgekehrten Vorgängen, wie das Öffnen eines Dokuments und das anschließende Schließen des Dokuments), sollten Sie die folgenden Schritte ausführen:  

1.  Erstellen Sie einen Heap-Snapshot, bevor Sie einen Vorgang ausführen.  
1.  Durchführen eines Vorgangs \ (Interaktion mit einer Seite auf eine Art und Weise, von der Sie glauben, dass Sie ein Leck verursacht).  
1.  Durchführen eines umgekehrten Vorgangs \ (die entgegengesetzte Interaktion ausführen und einige Male wiederholen \).  
1.  Nehmen Sie einen zweiten Heap-Snapshot auf, und ändern Sie die Ansicht dieser Person in einen **Vergleich**, und vergleichen Sie Sie mit **Snapshot 1**.  
    
In der **Vergleichs** Ansicht wird der Unterschied zwischen zwei Schnappschüssen angezeigt.  Wenn Sie einen Gesamteintrag erweitern, werden hinzugefügte und gelöschte Objektinstanzen angezeigt.  

:::image type="complex" source="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-comparison-dropdown.msft.png" alt-text="Vergleichsansicht" lightbox="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-comparison-dropdown.msft.png":::
   **Vergleichs** Ansicht  
:::image-end:::  

<!--todo: add HeapProfilingComparison section when available  -->  

### Einkapselungs Ansicht  

Die **Einkapselungs** Ansicht ist im Grunde eine "Vogelperspektive" der Objektstruktur Ihrer Anwendung.  Sie ermöglicht es Ihnen, in Funktions Verschlüssen zu spähen, die virtuellen computerinternen Objekte zu beobachten, die zusammen Ihre JavaScript-Objekte bilden, und zu verstehen, wie viel Arbeitsspeicher Ihre Anwendung auf einem sehr geringen Niveau verwendet.  

| Einstiegspunkte für die Eindämmungs Ansicht | Beschreibung |  
|:--- |:--- |  
| **DOMWindow-Objekte** | Globale Objekte für JavaScript-Code.  |  
| **GC-Stämme** | Die tatsächlichen GC-Stämme, die vom Garbage des virtuellen Computers verwendet werden.  GC-Stämme umfassen integrierte Objektzuordnungen, Symboltabellen, VM-Threadstapel, Kompilierungs Caches, handlebereiche und globale Handles.  |  
| **Systemeigene Objekte** | Browser Objekte werden innerhalb des virtuellen JavaScript-Computers "geschoben" \ (JavaScript VM \), um die Automatisierung zu ermöglichen, beispielsweise DOM-Knoten, CSS-Regeln.  |  

:::image type="complex" source="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-containment-dropdown.msft.png" alt-text="Einkapselungs Ansicht" lightbox="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-containment-dropdown.msft.png":::
   **Einkapselungs** Ansicht  
:::image-end:::  

<!--todo: add heap profiling containment section when available  -->  

> [!TIP]
> Ein Tipp zu Closures.  Benennen Sie die Funktionen, damit Sie problemlos zwischen den Closures im Schnappschuss unterscheiden können.  In diesem Beispiel werden beispielsweise keine benannten Funktionen verwendet.  
> 
> ```javascript
> function createLargeClosure() {
>     var largeStr = new Array(1000000).join('x');
>     var lC = function() { // this is NOT a named function
>         return largeStr;
>     };
>     return lC;
> }
> ```  
> 
> Das followingcode-Snippet verwendet benannte Funktionen.  
> 
> ```javascript
> function createLargeClosure() {
>     var largeStr = new Array(1000000).join('x');
>     var lC = function lC() { // this IS a named function
>         return largeStr;
>     };
>     return lC;
> }
> ```  
> 
> <!--  
> :::image type="complex" source="../media/memory-problems-domleaks.msft.png" alt-text="Name functions to distinguish between closures" lightbox="../media/memory-problems-domleaks.msft.png":::
>    Name functions to distinguish between closures  
> :::image-end:::  
> -->  
> 
> > [!NOTE]
> > Probieren Sie dieses Beispiel aus, [warum das `eval` böse ist][GlitchDevtoolsMemoryExample07] , um die Auswirkungen von Closures auf den Arbeitsspeicher zu analysieren.  Möglicherweise sind Sie auch daran interessiert, es mit diesem Beispiel zu befolgen, das Sie durch das Aufzeichnen von [Heapzuweisungen][GlitchDevtoolsMemoryExample08]führt.  
> 

## Nachschlagen der Farbcodierung  

Eigenschaften und Eigenschaftswerte von Objekten haben unterschiedliche Typen und werden entsprechend eingefärbt.  Jede Eigenschaft hat einen von vier Typen.  

| Eigenschaftstyp | Beschreibung |  
|:--- |:--- |  
| **a: Eigenschaft** | Eine reguläre Eigenschaft mit einem Namen, auf den über den `.` \ (dot \)-Operator zugegriffen wird, `[` `]` beispielsweise über die Notation \ (Brackets \) `["foo bar"]` .  |  
| **0: Element** | Eine reguläre Eigenschaft mit einem numerischen Index, auf die über `[` `]` \ (eckige Klammern \)-Notation zugegriffen wird.  |  
| **a: Kontext var** |  Eine Variable in einem Funktionskontext, auf die über den Variablennamen in einem Funktions Abschluss zugegriffen werden kann.  |  
| **a: System Prop** | Eine von der JavaScript-VM hinzugefügte Eigenschaft, auf die über JavaScript-Code nicht zugegriffen werden kann.  |  

Objekte, `System` die als kein entsprechender JavaScript-Typ gekennzeichnet sind.  Jede ist Teil der Objekt Systemimplementierung der JavaScript-VM.  V8 ordnet die meisten internen Objekte im gleichen Heap wie die JS-Objekte des Benutzers an.  Das sind also nur V8-Interna.  

## Suchen nach einem bestimmten Objekt  

Wenn Sie ein Objekt im gesammelten Heap suchen möchten, können Sie `Ctrl` + `F` die Objekt-ID verwenden und angeben.  

## Aufdecken von Dom-Lecks  

Der Heap-Profiler hat die Möglichkeit, bidirektionale Abhängigkeiten zwischen Browser systemeigenen Objekten \ (DOM-Knoten, CSS-Regeln \) und JavaScript-Objekten wiederzugeben.
Dies hilft bei der Ermittlung von ansonsten unsichtbaren Lecks, die durch vergessene, freigegebene Dom-unter Bäume entstehen.  

Dom-Lecks können größer sein, als Sie denken.  Sehen Sie sich das folgende Beispiel an:  Wann ist der #Tree GC?  

```javascript
var select = document.querySelector;
var treeRef = select("#tree");
var leafRef = select("#leaf");
var body = select("body");
body.removeChild(treeRef);
//#tree in not GC yet due to treeRef
treeRef = null;
//#tree is not GC yet due to indirect
//reference from leafRef
leafRef = null;
//#NOW able to be #tree GC
```  

Der `#leaf` verwaltet einen Verweis auf das relevante übergeordnete Element \ (parentNode \) und rekursiv bis zu `#tree` , sodass nur dann, wenn leafRef ungültig ist, die gesamte Struktur unter `#tree` einem Kandidaten für GC verfügbar ist.  

:::image type="complex" source="../media/memory-problems-tree-gc.msft.png" alt-text="Dom-Teilbäume" lightbox="../media/memory-problems-tree-gc.msft.png":::
   Dom-Teilbäume  
:::image-end:::  

> [!NOTE]
> Beispiele: Probieren Sie dieses Beispiel eines [undichten DOM-Knotens][GlitchDevtoolsMemoryExample06] aus, um zu verstehen, wo er undicht sein kann und wie er erkannt wird.  Sie können sich auch dieses Beispiel für [Undichtigkeiten von Dom anschauen, die größer als erwartet sind][GlitchDevtoolsMemoryExample09].  

Weitere Informationen zu Dom-Lecks und Grundlagen der Speicheranalyse finden Sie unter Auschecken von [Speicherlecks bei der Suche nach dem Microsoft Edge-devtools][GonzaloRuizdeVillaMemory] von Gonzalo Ruiz de Villa.  

<!--  
> [!NOTE]
> Example: Try this **demo** to play with detached DOM trees.  
-->  

<!--todo: add heap profiling dom leaks section when available  -->  

## Kontakt mit dem Microsoft Edge devtools-Team  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsMemoryProblems101ObjectSizes]: ./memory-101.md#object-sizes "Objektgrößen – Speicher Terminologie | Microsoft docs"  
[DevtoolsMemoryProblems101ObjectsRetainingTree]: ./memory-101.md#objects-retaining-tree "Objekte, die die Struktur des Arbeitsspeichers beibehalten | Microsoft docs"  

<!--[DevToolsHeapProfilingComparison]: https://developer.alphabet.com/devtools/docs/heap-profiling-comparison ""  -->  
<!--[DevToolsHeapProfilingContainment]: https://developer.alphabet.com/devtools/docs/heap-profiling-containment ""  -->  
<!--[DevtoolsHeapProfilingDomLeaks]: https://developer.alphabet.com/devtools/docs/heap-profiling-dom-leaks ""  -->  
<!--[DevToolsHeapProfilingSummary]: https://developer.alphabet.com/devtools/docs/heap-profiling-summary ""  -->  
<!--[DevtoolsProfileMemoryProblemsDiagnosisCausesMemoryLeaks]: ../profile/memory-problems/memory-diagnosis#narrow-down-causes-of-memory-leaks ""  -->  

[GlitchDevtoolsMemoryExample03]: https://microsoft-edge-chromium-devtools.glitch.me/static/memory/example-03.html "example-03.html-Microsoft Edge (Chrom) devtools | Glitch"  
[GlitchDevtoolsMemoryExample06]: https://microsoft-edge-chromium-devtools.glitch.me/static/memory/example-06.html "example-06.html-Microsoft Edge (Chrom) devtools | Glitch"  
[GlitchDevtoolsMemoryExample07]: https://microsoft-edge-chromium-devtools.glitch.me/static/memory/example-07.html "example-07.html-Microsoft Edge (Chrom) devtools | Glitch"  
[GlitchDevtoolsMemoryExample08]: https://microsoft-edge-chromium-devtools.glitch.me/static/memory/example-08.html "example-08.html-Microsoft Edge (Chrom) devtools | Glitch"  
[GlitchDevtoolsMemoryExample09]: https://microsoft-edge-chromium-devtools.glitch.me/static/memory/example-09.html "example-09.html-Microsoft Edge (Chrom) devtools | Glitch"  
[GlitchDevtoolsMemoryExample10]: https://microsoft-edge-chromium-devtools.glitch.me/static/memory/example-10.html "example-10.html-Microsoft Edge (Chrom) devtools | Glitch"  

[GonzaloRuizdeVillaMemory]: https://slid.es/gruizdevilla/memory "Arbeitsspeicher | Folien"  

> [!NOTE]
> Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.  
> Die ursprüngliche Seite wird [hier](https://developers.google.com/web/tools/chrome-devtools/memory-problems/heap-snapshots) gefunden und von [Meggin Kearney][MegginKearney] (Technical Writer \) erstellt.  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[MegginKearney]: https://developers.google.com/web/resources/contributors/megginkearney  
