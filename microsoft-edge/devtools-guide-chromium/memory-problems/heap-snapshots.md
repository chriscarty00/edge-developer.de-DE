---
description: Erfahren Sie, wie Sie Heapmomentaufnahmen mit dem Microsoft Edge DevTools-Heap-Profiler aufzeichnen und Speicherlecks finden.
title: Aufzeichnen von Heapmomentaufnahmen
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, Entwicklungstools
ms.openlocfilehash: 5f097cc45facc7f366a99a9564cf6f3d443f2058
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/13/2021
ms.locfileid: "11565015"
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
# <a name="how-to-record-heap-snapshots"></a>Aufzeichnen von Heapmomentaufnahmen  

Erfahren Sie, wie Sie Heapmomentaufnahmen mit dem Microsoft Edge DevTools-Heap-Profiler aufzeichnen und Speicherlecks finden.  

Der Microsoft Edge DevTools-Heap-Profiler zeigt die Speicherverteilung durch die JavaScript-Objekte und zugehörigen DOM-Knoten Ihrer Seite an.  Verwenden Sie ihn, um JavaScript-Heap-\(JS-Heap\)-Momentaufnahmen zu erstellen, Speicherdiagramme zu analysieren, Momentaufnahmen zu vergleichen und Speicherverluste zu finden.  Navigieren Sie zu [Objekte Aufbewahrungsstruktur][DevtoolsMemoryProblems101ObjectsRetainingTree].  

## <a name="take-a-snapshot"></a>Erstellen einer Momentaufnahme  

Wählen Sie **im Bereich** Arbeitsspeicher die Option **Momentaufnahme erstellen**und dann Start **aus.**  Sie können auch `Ctrl` + `E` \(Windows, Linux\) oder `Cmd` + `E` \(macOS\) auswählen.  

:::image type="complex" source="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots.msft.png" alt-text="Auswählen des Profilerstellungstyps" lightbox="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots.msft.png":::
   Auswählen des Profilerstellungstyps  
:::image-end:::  

**Momentaufnahmen** werden zunächst im Rendererprozessspeicher gespeichert.  Momentaufnahmen werden bei Bedarf an die DevTools übertragen, wenn Sie das Momentaufnahmesymbol zum Anzeigen auswählen.  

Nachdem die Momentaufnahme in DevTools geladen und analysiert wurde, wird die Nummer unter dem Snapshottitel angezeigt und zeigt die Gesamtgröße der erreichbaren [JavaScript-Objekte an.][DevtoolsMemoryProblems101ObjectSizes]  

:::image type="complex" source="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-all.msft.png" alt-text="Gesamtgröße erreichbarer Objekte" lightbox="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-all.msft.png":::
   Gesamtgröße erreichbarer Objekte  
:::image-end:::  

> [!NOTE]
> In Momentaufnahmen sind nur erreichbare Objekte enthalten.  Außerdem beginnt das Erstellen einer Momentaufnahme immer mit einer Garbage Collection.  

## <a name="clear-snapshots"></a>Löschen von Momentaufnahmen  

Wählen **Sie Alle Profile löschen** symbol, um Momentaufnahmen zu entfernen \(sowohl von DevTools als auch von jedem Speicher, der dem Rendererprozess zugeordnet ist\).  

:::image type="complex" source="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-all-hover-clear-all-profiles.msft.png" alt-text="Entfernen von Momentaufnahmen" lightbox="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-all-hover-clear-all-profiles.msft.png":::
   Entfernen von Momentaufnahmen  
:::image-end:::  

Durch das Schließen des DevTools-Fensters werden keine Profile aus dem Speicher gelöscht, der dem Rendererprozess zugeordnet ist.  Beim erneuten Öffnen von DevTools werden alle zuvor aufgenommenen Momentaufnahmen wieder in der Liste der Momentaufnahmen angezeigt.  

> [!NOTE]
> Probieren Sie dieses Beispiel für [gestreute Objekte aus,][GlitchDevtoolsMemoryExample03] und profilieren Sie es mithilfe des Heap-Profilers.  Eine Reihe von \(object\)-Elementzuordnungen werden angezeigt.  

## <a name="view-snapshots"></a>Anzeigen von Momentaufnahmen  

Zeigen Sie Momentaufnahmen aus unterschiedlichen Perspektiven für verschiedene Aufgaben an.  

**Die Zusammenfassungsansicht** zeigt Objekte, die nach dem Konstruktornamen zusammengefasst sind.  Verwenden Sie es, um Objekte \(und die Speichernutzung\) basierend auf dem Typ nach Konstruktornamen zu erstellen.  Es ist besonders hilfreich, um **DOM-Lecks nachverfolgung zu verfolgen.**

<!--todo: add profile memory problems memory diagnosis (tracking down DOM leaks) section when available  -->  

**Vergleichsansicht**.  Zeigt den Unterschied zwischen zwei Momentaufnahmen an.  Verwenden Sie sie, um zwei \(oder mehr\) Speichermomentaufnahmen vor und nach einem Vorgang zu vergleichen.  Wenn Sie das Delta im frei werdenden Speicher und in der Referenzanzahl überprüfen, können Sie das Vorhandensein und die Ursache eines Speicherverlusts bestätigen.  

**Containment-Ansicht**.  Ermöglicht die Untersuchung von Heapinhalten.  **Die Eindämmungsansicht** bietet eine bessere Ansicht der Objektstruktur und hilft dabei, Objekte zu analysieren, auf die im globalen Namespace \(window\) verwiesen wird, um herauszufinden, was Objekte um sich herum hält.  Verwenden Sie sie, um Verschlüsse zu analysieren und sich auf niedriger Ebene mit Ihren Objekten zu begnnen.  

Um zwischen Ansichten zu wechseln, verwenden Sie die Auswahl oben in der Ansicht.  

:::image type="complex" source="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-view-dropdown.msft.png" alt-text="Auswahl für Switchansichten" lightbox="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-view-dropdown.msft.png":::
   Auswahl für Switchansichten  
:::image-end:::  

> [!NOTE]
> Nicht alle Eigenschaften werden im JavaScript-Heap gespeichert.  Eigenschaften, die mithilfe von Getters implementiert werden, die systemeigenen Code ausführen, werden nicht erfasst.  Außerdem werden werte, die keine Zeichenfolgen sind, z. B. Zahlen, nicht erfasst.  

### <a name="summary-view"></a>Zusammenfassungsansicht  

Zunächst wird in der Zusammenfassungsansicht eine Momentaufnahme geöffnet, in der Objektsummen angezeigt werden, die erweitert werden können, um Instanzen zu zeigen:  

:::image type="complex" source="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-constructor-retainers.msft.png" alt-text="Zusammenfassungsansicht" lightbox="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-constructor-retainers.msft.png":::
   **Zusammenfassungsansicht**  
:::image-end:::  

Einträge auf oberster Ebene sind "Gesamtlinien".  

| Einträge auf oberster Ebene | Beschreibung |  
|:--- |:--- |  
| **Konstruktor** | Stellt alle Objekte dar, die mit diesem Konstruktor erstellt wurden.  |  
| **Entfernung** | zeigt den Abstand zum Stamm mithilfe des kürzesten einfachen Pfads von Knoten an.  |  
| **Flache Größe** | Zeigt die Summe der flachen Größen aller Objekte an, die von einer bestimmten Konstruktorfunktion erstellt werden.  Die flache Größe ist die Größe des Arbeitsspeichers, der von einem Objekt gehalten wird \(im Allgemeinen haben Arrays und Zeichenfolgen größere flache Größen\).  Navigieren Sie zu [Objektgrößen][DevtoolsMemoryProblems101ObjectSizes].  |  
| **Beibehaltene Größe** | Zeigt die maximale beibehaltene Größe zwischen denselben Objekten an.  Die Größe des Arbeitsspeichers, den Sie frei machen können, nachdem ein Objekt gelöscht wurde \(und die Abhängigen werden nicht mehr erreichbar\) wird als beibehaltene Größe bezeichnet.  Navigieren Sie zu [Objektgrößen][DevtoolsMemoryProblems101ObjectSizes].  |  

<!--| **Number of object instances** | Displayed in the # column.  |  -->  

Nach dem Erweitern einer Gesamtlinie in der oberen Ansicht werden alle Instanzen angezeigt.  Für jede Instanz werden die flachen und beibehaltenen Größen in den entsprechenden Spalten angezeigt.  Die Zahl nach dem Zeichen ist die eindeutige ID des Objekts, sodass Sie Heapmomentaufnahmen auf `@` Objektbasis vergleichen können.  

Denken Sie daran, dass gelbe Objekte JavaScript-Verweise und rote Objekte getrennte Knoten sind, auf die von einem mit einem gelben Hintergrund verwiesen wird.  

**Was entsprechen die verschiedenen Konstruktoreinträge \(Group\) im Heap-Profiler?**  

:::image type="complex" source="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-constructor-highlight.msft.png" alt-text="Konstruktorgruppen" lightbox="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-constructor-highlight.msft.png":::
   **Konstruktorgruppen**  
:::image-end:::  

| Konstruktor \(Group\)-Eintrag | Beschreibung |  
|:--- |:--- |  
| **\(global property\)** | Die Zwischenobjekte zwischen einem globalen Objekt \(z. B. \) und einem Objekt, auf das `window` verwiesen wird.  Wenn ein Objekt mithilfe eines Konstruktors erstellt wird und von einem globalen Objekt gehalten wird, kann der `Person` Aufbewahrungspfad als dargestellt `[global] > \(global property\) > Person` werden.  Dies steht im Gegensatz zur Norm, bei der Objekte direkt aufeinander verweisen.  Zwischenobjekte sind aus Leistungsgründen vorhanden.  Globals werden regelmäßig geändert, und Eigenschaftenzugriffsoptimierungen sind für nicht-globale Objekte nicht anwendbar.  |  
| **\(roots\)** | Die Stammeinträge in der Aufbewahrungsstrukturansicht sind die Entitäten, die Verweise auf das ausgewählte Objekt haben.  Die Einträge können auch Verweise sein, die vom Modul zu modulspezifischen Zwecken erstellt werden.  Das Modul verfügt über Caches, die auf Objekte verweisen, aber alle diese Verweise sind schwach und verhindern nicht, dass ein Objekt gesammelt wird, da keine wirklich starken Verweise vorhanden sind.  |  
| **\(closure\)** | Eine Anzahl von Verweisen auf eine Gruppe von Objekten über Funktionsschließungen.  |  
| **\(array, string, number, regexp\)** | Eine Liste von Objekttypen mit Eigenschaften, die auf ein Array, eine Zeichenfolge, eine Zahl oder einen regulären Ausdruck verweisen.  |  
| **\(kompilierter Code\)** | Alles im Zusammenhang mit kompilierten Code.  Skript ähnelt einer Funktion, entspricht jedoch einem `<script>` Textkörper.  SharedFunctionInfos \(SFI\) sind Objekte, die zwischen Funktionen und kompilierten Code stehen.  Funktionen haben in der Regel einen Kontext, sfIs nicht.  |  
| **HTMLDivElement**, **HTMLAnchorElement**, **DocumentFragment**und so weiter.  | Verweise auf Elemente oder Dokumentobjekte eines bestimmten Typs, auf die ihr Code verweist.  |  

<!--todo: add heap profiling summary section when available -->  

### <a name="comparison-view"></a>Vergleichsansicht  

Suchen Sie nach undichten Objekten, indem Sie mehrere Momentaufnahmen miteinander vergleichen.  Um zu überprüfen, ob ein bestimmter Anwendungsvorgang keine Lecks \(z. B. ein Paar direkter und umgekehrter Vorgänge, z. B. das Öffnen eines Dokuments und das anschließende Schließen, keine Undichte hinterlassen sollte\), können Sie das folgende Szenario befolgen:  

1.  Erstellen Sie eine Heapmomentaufnahme, bevor Sie einen Vorgang ausführen.  
1.  Führen Sie einen Vorgang \(interagieren Sie mit einer Seite in einer Weise aus, von der Sie glauben, dass ein Leck verursacht wird\).  
1.  Führen Sie einen umgekehrten Vorgang aus \(Führen Sie die entgegengesetzte Interaktion aus, und wiederholen Sie sie ein paar Mal\).  
1.  Erstellen Sie einen zweiten Heapsnapshot, und ändern Sie die Ansicht dieser in **Vergleich**, und vergleichen Sie sie mit **Snapshot 1**.  
    
In der **Vergleichsansicht** wird der Unterschied zwischen zwei Momentaufnahmen angezeigt.  Beim Erweitern eines Gesamteintrags werden hinzugefügte und gelöschte Objektinstanzen angezeigt.  

:::image type="complex" source="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-comparison-dropdown.msft.png" alt-text="Vergleichsansicht" lightbox="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-comparison-dropdown.msft.png":::
   **Vergleichsansicht**  
:::image-end:::  

<!--todo: add HeapProfilingComparison section when available  -->  

### <a name="containment-view"></a>Containment-Ansicht  

Die **Containment-Ansicht** ist im Wesentlichen eine "Vogelperspektive" der Objektstruktur Ihrer Anwendung.  Es ermöglicht Ihnen, einen Blick in Funktionsschließungen zu werfen, interne Objekte des virtuellen Computers \(VM\) zu beobachten, die ihre JavaScript-Objekte zusammen stellen, und zu verstehen, wie viel Arbeitsspeicher Ihre Anwendung auf sehr niedriger Ebene verwendet.  

| Einstiegspunkte für die Eindämmungsansicht | Beschreibung |  
|:--- |:--- |  
| **DOMWindow-Objekte** | Globale Objekte für JavaScript-Code.  |  
| **GC-Stamm** | Die tatsächlichen GC-Stammwurzeln, die vom Garbage of the VM verwendet werden.  GC-Stammpunkte bestehen aus integrierten Objektzuordnungen, Symboltabellen, VM-Threadstapeln, Kompilierungscaches, Handlebereiche und globalen Handles.  |  
| **Systemeigene Objekte** | Browserobjekte werden innerhalb des virtuellen JavaScript-Computers \(JavaScript VM\) "pushed", um Automatisierung zu ermöglichen, z. B. DOM-Knoten, CSS-Regeln.  |  

:::image type="complex" source="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-containment-dropdown.msft.png" alt-text="Containment-Ansicht" lightbox="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-containment-dropdown.msft.png":::
   **Containment-Ansicht**  
:::image-end:::  

<!--todo: add heap profiling containment section when available  -->  

> [!TIP]
> Ein Tipp zu Verschlüssen.  Benennen Sie die Funktionen so, dass Sie problemlos zwischen Verschlüssen in der Momentaufnahme unterscheiden können.  In diesem Beispiel werden beispielsweise keine benannten Funktionen verwendet.  
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
> Der folgende Codeausschnitt verwendet benannte Funktionen.  
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
> > Probieren Sie dieses Beispiel [aus, warum `eval` es übl ist,][GlitchDevtoolsMemoryExample07] die Auswirkungen von Sperrungen auf den Speicher zu analysieren.  Sie können auch daran interessiert sein, diesem Beispiel nachzu folgen, das Sie durch die Aufzeichnung von [Heapzuordnungen führt.][GlitchDevtoolsMemoryExample08]  
> 

## <a name="look-up-color-coding"></a>Suchen nach Farbcodierung  

Eigenschaften und Eigenschaftswerte von Objekten haben unterschiedliche Typen und werden entsprechend gefärbt.  Jede Eigenschaft hat einen von vier Typen.  

| Eigenschaftstyp | Beschreibung |  
|:--- |:--- |  
| **a: property** | Eine reguläre Eigenschaft mit einem Namen, auf die über den `.` \(dot\)-Operator zugegriffen wird, oder über `[` `]` \(brackets\)-Notation, z. B. `["foo bar"]` .  |  
| **0: Element** | Eine reguläre Eigenschaft mit einem numerischen Index, auf die über `[` `]` die Notation \(brackets\) zugegriffen wird.  |  
| **a: context var** |  Eine Variable in einem Funktionskontext, auf die über den Variablennamen innerhalb einer Funktionsschließung zugegriffen werden kann.  |  
| **a: System-Prop** | Eine Eigenschaft, die von der JavaScript-VM hinzugefügt wurde und nicht über JavaScript-Code zugänglich ist.  |  

Objekte, die `System` nicht über einen entsprechenden JavaScript-Typ verfügen.  Jeder ist Teil der Objektsystemimplementierung der Javascript-VM.  V8 weist die meisten internen Objekte im gleichen Heap wie die JS-Objekte des Benutzers zu.  Dies sind also nur V8-Interne.  

## <a name="find-a-specific-object"></a>Suchen eines bestimmten Objekts  

Um ein Objekt im gesammelten Heap zu finden, können Sie die Objekt-ID verwenden `Ctrl` + `F` und geben.  

## <a name="uncover-dom-leaks"></a>Aufdecken von DOM-Lecks  

Der Heapprofiler kann bidirektionale Abhängigkeiten zwischen browsereigenen Objekten \(DOM-Knoten, CSS-Regeln\) und JavaScript-Objekten widerspiegeln.
Dies hilft, ansonsten unsichtbare Lecks zu erkennen, die aufgrund vergessener getrennter DOM-Unterstrukturen passieren, die herumschlaufen.  

DOM-Lecks können größer sein, als Sie denken.  Ziehen Sie das folgende Beispiel in Betracht.  Wann ist die #tree GC?  

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

Der behält einen Verweis auf das relevante übergeordnete Objekt \(parentNode\) bei und rekursiv bis , also nur, wenn leafRef nullifiziert wird, ist die GESAMTE Struktur unter einem Kandidaten für `#leaf` `#tree` `#tree` GC.  

:::image type="complex" source="../media/memory-problems-tree-gc.msft.png" alt-text="DOM-Unterstrukturen" lightbox="../media/memory-problems-tree-gc.msft.png":::
   DOM-Unterstrukturen  
:::image-end:::  

> [!NOTE]
> Beispiele: Probieren Sie dieses Beispiel für einen nicht mehr vorhandenen [DOM-Knoten][GlitchDevtoolsMemoryExample06] aus, um zu verstehen, wo und wie sie erkannt werden können.  Sie können sich auch dieses Beispiel dafür anschauen, dass [DOM-Lecks größer als erwartet sind.][GlitchDevtoolsMemoryExample09]  

Weitere Informationen zu DOM leaks and memory analysis fundamentals checkout [Finding and debugging memory leaks with the Microsoft Edge DevTools][GonzaloRuizdeVillaMemory] by Gonzalo Ruiz de Villa.  

<!--  
> [!NOTE]
> Example: Try this **demo** to play with detached DOM trees.  
-->  

<!--todo: add heap profiling dom leaks section when available  -->  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsMemoryProblems101ObjectSizes]: ./memory-101.md#object-sizes "Objektgrößen – Speicherterminologie | Microsoft Docs"  
[DevtoolsMemoryProblems101ObjectsRetainingTree]: ./memory-101.md#objects-retaining-tree "Struktur der Aufbewahrung von Objekten – Speicherterminologie | Microsoft Docs"  

<!--[DevToolsHeapProfilingComparison]: https://developer.alphabet.com/devtools/docs/heap-profiling-comparison ""  -->  
<!--[DevToolsHeapProfilingContainment]: https://developer.alphabet.com/devtools/docs/heap-profiling-containment ""  -->  
<!--[DevtoolsHeapProfilingDomLeaks]: https://developer.alphabet.com/devtools/docs/heap-profiling-dom-leaks ""  -->  
<!--[DevToolsHeapProfilingSummary]: https://developer.alphabet.com/devtools/docs/heap-profiling-summary ""  -->  
<!--[DevtoolsProfileMemoryProblemsDiagnosisCausesMemoryLeaks]: ../profile/memory-problems/memory-diagnosis#narrow-down-causes-of-memory-leaks ""  -->  

[GlitchDevtoolsMemoryExample03]: https://microsoft-edge-chromium-devtools.glitch.me/static/memory/example-03.html "example-03.html - Microsoft Edge (Chromium) DevTools | Glitch"  
[GlitchDevtoolsMemoryExample06]: https://microsoft-edge-chromium-devtools.glitch.me/static/memory/example-06.html "example-06.html - Microsoft Edge (Chromium) DevTools | Glitch"  
[GlitchDevtoolsMemoryExample07]: https://microsoft-edge-chromium-devtools.glitch.me/static/memory/example-07.html "example-07.html - Microsoft Edge (Chromium) DevTools | Glitch"  
[GlitchDevtoolsMemoryExample08]: https://microsoft-edge-chromium-devtools.glitch.me/static/memory/example-08.html "example-08.html - Microsoft Edge (Chromium) DevTools | Glitch"  
[GlitchDevtoolsMemoryExample09]: https://microsoft-edge-chromium-devtools.glitch.me/static/memory/example-09.html "example-09.html - Microsoft Edge (Chromium) DevTools | Glitch"  
[GlitchDevtoolsMemoryExample10]: https://microsoft-edge-chromium-devtools.glitch.me/static/memory/example-10.html "example-10.html - Microsoft Edge (Chromium) DevTools | Glitch"  

[GonzaloRuizdeVillaMemory]: https://slid.es/gruizdevilla/memory "Speicher | Folien"  

> [!NOTE]
> Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.  
> Die ursprüngliche Seite befindet sich [hier und](https://developers.google.com/web/tools/chrome-devtools/memory-problems/heap-snapshots) wird von [Meggin Kearney][MegginKearney] \(Technical Writer\) verfasst.  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  
[MegginKearney]: https://developers.google.com/web/resources/contributors#meggin-kearney  
