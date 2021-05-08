---
description: Benutzer erwarten interaktive und flüssige Seiten.  Jede Phase in der Pixelpipeline stellt eine Möglichkeit dar, jank einzuführen.  Erfahren Sie mehr über Tools und Strategien zum Identifizieren und Beheben gängiger Probleme, die die Laufzeitleistung verlangsamen.
title: Analysieren der Laufzeitleistung
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, Entwicklungstools
ms.openlocfilehash: 646db5b2e88e33b109e5eb3ae01a296bf3a4fb46
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398000"
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
   limitations under the License.  -->

# <a name="analyze-runtime-performance"></a>Analysieren der Laufzeitleistung  

Benutzer erwarten interaktive und flüssige Seiten.  Jede Phase in der Pixelpipeline stellt eine Möglichkeit dar, jank einzuführen.  Erfahren Sie mehr über Tools und Strategien zum Identifizieren und Beheben gängiger Probleme, die die Laufzeitleistung verlangsamen.  

### <a name="summary"></a>Zusammenfassung  

*   Schreiben Sie kein JavaScript, das den Browser zwingt, das Layout neu zu berechnen.  Trennen Sie Lese- und Schreibfunktionen, und führen Sie zuerst Lesezugriffe aus.  
*   Komplizieren Sie Ihre CSS nicht überkompliziert.  Verwenden Sie weniger CSS, und halten Sie Ihre CSS-Selektoren einfach.  
*   Vermeiden Sie das Layout so weit wie möglich.  Wählen Sie CSS aus, das das Layout überhaupt nicht auslöst.  
*   Das Malen kann länger dauern als jede andere Renderingaktivität.  Achten Sie auf Farbengpässe.  
    
## <a name="javascript"></a>JavaScript  

JavaScript-Berechnungen, insbesondere diejenigen, die umfangreiche visuelle Änderungen auslösen, können die Anwendungsleistung beeinträchtigen.  Lassen Sie nicht zu, dass sich schlecht zeitgezeitte oder lang ausgeführte JavaScript in Benutzerinteraktionen einmischt.  

### <a name="javascript-tools"></a>JavaScript: Tools  

Nehmen Sie eine Aufzeichnung im **Leistungstool** vor, und suchen Sie nach verdächtig langen `Evaluate Script` Ereignissen.  <!--If you find any, you are able to enable the **JS Profiler** and re-do your recording to get more detailed information about exactly which JavaScript functions were used and how long each took.  -->  

<!--todo: add Recording section when available  -->  
<!--todo: add Profile JavaScript (JS Profiler) section when available  -->  

f Sie in Ihrem JavaScript ein wenig Jank notieren, müssen Sie Ihre Analyse möglicherweise auf die nächste Ebene bringen und ein JavaScript-CPU-Profil sammeln.  CPU-Profile zeigen an, wo die Laufzeit innerhalb der Funktionen Ihrer Seite ausgegeben wird.  Informationen zum Erstellen von CPU-Profilen finden Sie unter [Beschleunigen der JavaScript-Runtime][DevtoolsRenderingToolsJavascriptRuntime].

### <a name="javascript-problems"></a>JavaScript: Probleme  

In der folgenden Tabelle werden einige häufige JavaScript-Probleme und mögliche Lösungen beschrieben.  

| Problem | Beispiel | Lösung |  
|:--- |:--- |:--- |  
| Teure Eingabehandler, die die Antwort oder Animation beeinflussen.  | Touch- und Parallax-Bildlauf.  | Lassen Sie den Browser Touch- und Bildlauf verarbeiten oder den Listener so spät wie möglich binden.  Navigieren Sie [in der Prüfliste zur][WebPerformanceCalendarRuntimeChecklist]Laufzeitleistung von Paul Lewis zu Teure Eingabehandler.  |  
| Ungültige JavaScript-Zeit, die sich auf Antwort, Animation, Last ausdingt.  | Benutzer scrollt direkt nach Seitenlade, setTimeout /setInterval.  | Optimieren der JavaScript-Laufzeit: `requestAnimationFrame` Verwenden Sie , verteilen Sie die DOM-Manipulation über Frames, verwenden Sie Web [Workers][MDNUsingWebWorkers].  |  
| Lang ausgeführtes JavaScript, das sich auf die Antwort ausdingt.  | Das [DOMContentLoaded-Ereignis][MDNUsingWebWorkers] wird beim Überschwemmen der JS-Arbeit ins Stocken geraten.  | Verschieben Sie reine Rechenarbeit zu [Web Workers][MDNUsingWebWorkers].  Wenn Sie DOM-Zugriff benötigen, verwenden Sie `requestAnimationFrame` .  <!--Navigate to [Optimize JavaScript Execution][WebFundamentalsPerformanceRenderingOptimizeJavascriptRuntime].  -->  |  
| Garbage-y-Skripts, die die Antwort oder Animation beeinflussen.  | Die Garbage Collection kann an einer beliebigen Stelle vorkommen.  | Schreiben Sie weniger Garbage-y-Skripts.  Navigieren Sie [zu Garbage Collection in Animation in Der Prüfliste zur Laufzeitleistung von Paul Lewis][WebPerformanceCalendarRuntimeChecklist].  |  

<!--todo: add Optimize JavaScript runtime section when available  -->  

## <a name="style"></a>Format  

Formatänderungen sind kostspielig, insbesondere wenn sich diese Änderungen auf mehr als ein Element im DOM auswirken.  Jedes Mal, wenn Sie Formatvorlagen auf ein Element anwenden, berechnet der Browser die Auswirkungen auf alle zugehörigen Elemente, berechnet das Layout neu und aktualisiert.  

<!--Related Guides:  

*   [Reduce the Scope and Complexity of Styles Calculations][WebFundamentalsPerformanceRenderingReduceScope]  
-->  

<!--todo: add Reduce the Scope and Complexity of Styles Calculations section when available -->  

### <a name="style-tools"></a>Formatvorlage: Tools  

Nehmen Sie eine Aufzeichnung im **Leistungstool** vor.  Überprüfen Sie die Aufzeichnung auf `Recalculate Style` große Ereignisse \(angezeigt in Lila\).  

<!--todo: add Recording section when available  -->  

Wählen Sie `Recalculate Style` ein Ereignis aus, um weitere Informationen dazu im **Detailbereich anzuzeigen.**  Wenn die Formatvorlageänderungen sehr lange dauern, ist dies ein Leistungstreffer.  Wenn sich die Formatvorlageberechnungen auf eine große Anzahl von Elementen ausdingen, ist dies ein weiterer Bereich mit Verbesserungsmöglichkeiten.  

:::image type="complex" source="../media/rendering-tools-performance-recalculate-style-summary.msft.png" alt-text="Langes Neuberechnungsformat" lightbox="../media/rendering-tools-performance-recalculate-style-summary.msft.png":::
   Langes Neuberechnungsformat  
:::image-end:::  

So reduzieren Sie die Auswirkungen von `Recalculate Style` Ereignissen:  

*   Verwenden Sie die [CSS-Trigger,][CssTriggers] um zu erfahren, welche CSS-Eigenschaften Layout, Paint und Composite auslösen.  Diese Eigenschaften haben die größten Auswirkungen auf die Renderingleistung.  
*   Wechseln Sie zu Eigenschaften, die weniger Auswirkungen haben.  <!--For more guidance, navigate to [Stick to compositor-only properties and manage layer count][WebFundamentalsPerformanceRenderingCompositorOnlyProperties].  -->  
    
<!--todo: add Stick to compositor-only properties and manage layer count section when available -->  

### <a name="style-problems"></a>Formatvorlage: Probleme  

In der folgenden Tabelle werden einige häufige Stilprobleme und mögliche Lösungen beschrieben.  

| Problem | Beispiel | Lösung |  
|:--- |:--- |:--- |  
| Teure Formatvorlageberechnungen, die sich auf Die Antwort oder Animation ausdingen.  | Jede CSS-Eigenschaft, die die Geometrie eines Elements ändert, z. B. die Breite, Höhe oder Position; Der Browser überprüft alle anderen Elemente und berechnet das Layout neu.  | Vermeiden von CSS, das Layouts auslöst |  
| Komplexe Selektoren, die die Antwort oder Animation beeinflussen.  | Geschachtelte Selektoren zwingen den Browser, alles über alle anderen Elemente, einschließlich Eltern und Kinder, zu wissen.  | Verweisen Sie auf ein Element in Ihrer CSS mit nur einer Klasse.  |  

<!--todo: add Avoid CSS that triggers layouts section when available -->  
<!--todo: add Reduce the Scope and Complexity of Styles Calculations (Reference an element in your CSS with just a class) section when available -->  

<!--Related Guides:  

*   [Reduce the Scope and Complexity of Styles Calculations][WebFundamentalsPerformanceRenderingReduceScope]  -->  

<!--todo: add Reduce the Scope and Complexity of Styles Calculations section when available -->  

## <a name="layout"></a>Layout  

Layout (oder Reflow in Firefox) ist der Prozess, mit dem der Browser die Positionen und Größen aller Elemente auf einer Seite berechnet.  Das Layoutmodell des Webs bedeutet, dass sich ein Element auf andere auswirken kann. Beispielsweise wirkt sich die Breite des Elements in der Regel auf die Breite aller untergeordneten Elemente aus, und so weiter, bis hin zur `<body>` Struktur nach oben und unten.  Der Prozess kann für den Browser sehr involviert sein.  

Als allgemeine Faustregel gilt: Wenn Sie einen geometrischen Wert aus dem DOM zurück fordern, bevor ein Frame abgeschlossen ist, werden Sie sich mit "erzwungenen synchronen Layouts" befinden. Dies kann ein großer Leistungsengpässe sein, wenn er häufig wiederholt oder für eine große DOM-Struktur ausgeführt wird.  

<!--Related Guides:  

*   [Avoid Layout Thrashing][WebFundamentalsPerformanceRenderingAvoidLargeComplexLayouts]  
*   [Diagnose Forced Synchronous Layouts][DevtoolsRenderingToolsForcedSynchronousLayouts]  -->  

<!--todo: add Avoid CSS that triggers layouts (Avoid Layout Thrashing) section when available -->  
<!--todo: add Diagnose Forced Synchronous Layouts section when available  -->  

### <a name="layout-tools"></a>Layout: Tools  

Der **Bereich Leistung** gibt an, wann eine Seite erzwungene synchrone Layouts verursacht.  Diese `Layout` Ereignisse sind mit roten Balken markiert.  

:::image type="complex" source="../media/rendering-tools-jank-performance-recalculate-style-summary.msft.png" alt-text="Erzwungenes synchrones Layout" lightbox="../media/rendering-tools-jank-performance-recalculate-style-summary.msft.png":::
   Erzwungenes synchrones Layout  
:::image-end:::  

"Layout shing" ist eine Wiederholung erzwungener synchroner Layoutbedingungen.  Dies tritt auf, wenn JavaScript wiederholt aus dem DOM schreibt und liest, was den Browser zwingt, das Layout immer wieder neu zu berechnen.  Suchen Sie zum Identifizieren des Layoutbrands nach einem Muster mehrerer erzwungener synchroner Layoutwarnungen.  Überprüfen Sie die vorherige Abbildung.  

### <a name="layout-problems"></a>Layout: Probleme  

In der folgenden Tabelle werden einige häufige Layoutprobleme und mögliche Lösungen beschrieben.  

| Problem | Beispiel | Lösung |  
|:--- |:--- |:--- |  
| Erzwungenes synchrones Layout, das die Antwort oder Animation beeinflusst.  | Erzwingen, dass der Browser das Layout früher in der Pixelpipeline ausführen muss, was zu wiederholten Schritten im Renderingprozess führt.  | Batch, in dem Ihre Formatvorlage zuerst gelesen wird, und anschließend schreibe.  <!--Navigate to [Avoid large, complex layouts and layout thrashing][WebFundamentalsPerformanceRenderingAvoidLargeComplexLayouts].  -->  |  
| Layoutbrandung, die sich auf Die Antwort oder Animation ausdingt.  | Eine Schleife, die den Browser in einen Lese-/Lese-/Schreibzyklus versetzt und den Browser dazu zwingt, das Layout immer wieder neu zu berechnen.  | Automatische Batch-Lese-/Schreibvorgänge mithilfe der [FastDom-Bibliothek][GitHubWilsonpageFastdom].  |  

<!--todo: add Avoid CSS that triggers layouts (Avoid large, complex layouts and layout thrashing) section when available -->  

## <a name="paint-and-composite"></a>Paint und zusammengesetzt  

Paint ist der Vorgang des Ausfüllens von Pixeln.  Dies ist häufig der kostspieligste Teil des Renderingprozesses.  Wenn Sie feststellen, dass Ihre Seite nicht so funktioniert, wie sie entworfen wurde, ist es wahrscheinlich, dass Sie Farbprobleme haben.  

Beim Compositing werden die dargestellten Teile der Seite für die Anzeige auf dem Bildschirm gegliedert.  Wenn Sie sich in den meisten Punkten nur an die Eigenschaften des Kompositors halten und die Farbe ganz vermeiden, sollten Sie eine wesentliche Leistungsverbesserung feststellen, sie müssen jedoch auf übermäßig hohe Ebenenanzahl achten.  <!--Navigate to [Stick to compositor-only properties and manage layer count][WebFundamentalsPerformanceRenderingCompositorOnlyProperties].  -->  

<!--todo: add Stick to compositor-only properties and manage layer count section when available  -->  

### <a name="paint-and-composite-tools"></a>Paint and composite: Tools  

Möchten Sie wissen, wie lange das Malen dauert oder wie oft das Malen stattfindet?  Überprüfen Sie [die Einstellung Erweiterte Farbinstrumentierung aktivieren][DevtoolsChromiumEvaluatePerformanceReferenceEnableadvancedpaintinstrumentation] im Bereich **Leistung,** und nehmen Sie dann eine Aufzeichnung vor.  Wenn die meiste Renderzeit mit dem Malen verbracht wird, haben Sie Farbprobleme.  

<!--
:::image type="complex" source="../media/rendering-tools-jank-performance-advanced-paint-instrumentation-summary.msft.png" alt-text="Long paint times in timeline recording" lightbox="../media/rendering-tools-jank-performance-advanced-paint-instrumentation-summary.msft.png":::
   Long paint times in timeline recording  
:::image-end:::  
-->  

<!--
Check out the **Rendering** panel for further configurations that are able to help you diagnose paint problems.  -->  

<!--todo: link Rendering panel in ../evaluate-performance/timeline-tool  sub-section when live  -->  

### <a name="paint-and-composite-problems"></a>Farbe und Zusammengesetzt: Probleme  

In der folgenden Tabelle werden einige häufige Farb- und Verbundprobleme sowie mögliche Lösungen beschrieben.  

| Problem | Beispiel | Lösung |  
|:--- |:--- |:--- |  
| Farbstürmchen, die sich auf die Reaktion oder Animation ausdingen.  | Große Farbbereiche oder teure Farben, die die Reaktion oder Animation beeinflussen.  | Vermeiden Sie Farbe, fördern Sie Elemente, die sich auf ihre eigene Ebene verschieben, verwenden Sie Transformationen und Deckkraft.  <!--Navigate to [Simplify paint complexity and reduce paint areas][WebFundamentalsPerformanceRenderingSimplifyPaintComplexity].  -->  |  
| Ebenenexplosionen, die Animationen beeinflussen.  | Überpromotion von zu vielen Elementen mit `translateZ(0)` erheblichen Auswirkungen auf die Animationsleistung.  | Bewerben Sie sich sparsam auf Ebenen, und nur, wenn Sie wissen, dass es greifbare Verbesserungen bietet.  <!--Navigate to [Stick to composite-only properties and manage layer count][WebFundamentalsPerformanceRenderingCompositorOnlyProperties].  -->  |  

<!--todo: add Simplify paint complexity and reduce paint areas section when available  -->  
<!--todo: add Stick to compositor-only properties and manage layer count section when available  -->  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsRenderingToolsJavascriptRuntime]: ./js-runtime.md "Beschleunigen sie die JavaScript-Laufzeit | Microsoft Docs"  
[DevtoolsChromiumEvaluatePerformanceReferenceEnableadvancedpaintinstrumentation]: ../evaluate-performance/reference.md#turn-on-advanced-paint-instrumentation "Aktivieren der erweiterten Farbinstrumentierung – Leistungsanalysereferenz | Microsoft Docs"

<!--[DevtoolsRenderingToolsForcedSynchronousLayouts]: ./rendering-tools/forced-synchronous-layouts.md "Diagnose Forced Synchronous Layouts | Microsoft Docs"  -->  

<!-- The Timeline Tool page is deprecated  -->  
<!--[DevtoolsEvaluatePerformanceTimelineToolProfileJavascript]: ../evaluate-performance/timeline-tool#profile-javascript "Profile JavaScript - How to Use the Timeline Tool | Microsoft Docs"  -->  
<!--[DevtoolsEvaluatePerformanceTimelineToolProfilePainting]: ../evaluate-performance/timeline-tool#profile-painting "Profile painting - How to Use the Timeline Tool | Microsoft Docs"  -->  
<!--[DevtoolsEvaluatePerformanceTimelineToolRecording]: ../evaluate-performance/timeline-tool#make-a-recording "Make a recording - How to Use the Timeline Tool | Microsoft Docs"  -->  
<!--[DevtoolsEvaluatePerformanceTimelineToolRenderingSettings]: ../evaluate-performance/timeline-tool#rendering-settings "Rendering settings - How to Use the Timeline Tool | Microsoft Docs"  -->  

<!--[WebFundamentalsPerformanceRenderingAvoidLargeComplexLayouts]: /web/fundamentals/performance/rendering/avoid-large-complex-layouts-and-layout-thrashing "Avoid Large, Complex Layouts, and Layout Thrashing"  -->  
<!--[WebFundamentalsPerformanceRenderingOptimizeJavascriptRuntime]: /web/fundamentals/performance/rendering/optimize-javascript-execution "Optimize JavaScript Runtime"  -->  
<!--[WebFundamentalsPerformanceRenderingReduceScope]: /web/fundamentals/performance/rendering/reduce-the-scope-and-complexity-of-style-calculations "Reduce the Scope and Complexity of Style Calculations"  -->  
<!--[WebFundamentalsPerformanceRenderingSimplifyPaintComplexity]: /web/fundamentals/performance/rendering/simplify-paint-complexity-and-reduce-paint-areas "Simplify Paint Complexity and Reduce Paint Areas"  -->  
<!--[WebFundamentalsPerformanceRenderingCompositorOnlyProperties]: /web/fundamentals/performance/rendering/stick-to-compositor-only-properties-and-manage-layer-count "Stick to Compositor-Only Properties and Manage Layer Count"  -->  

[CssTriggers]: https://csstriggers.com "CSS-Trigger"  

[MDNUsingWebWorkers]: https://developer.mozilla.org/docs/Web/API/Web_Workers_API/Using_web_workers "Verwenden von Web Workers | MDN"  

[WebPerformanceCalendarRuntimeChecklist]: https://calendar.perfplanet.com/2013/the-runtime-performance-checklist/ "Prüfliste zur Laufzeitleistung – Webleistungskalender"  

[GitHubWilsonpageFastdom]: https://github.com/wilsonpage/fastdom "wilsonpage/fastdom | GitHub"  

> [!NOTE]
> Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.  
> Die ursprüngliche Seite [](https://developers.google.com/web/tools/chrome-devtools/rendering-tools/index) befindet sich hier und wird von [Kayce Basken][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\) und [Meggin Kearney][MegginKearney] \(Tech Writer\) verfasst.  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[MegginKearney]: https://developers.google.com/web/resources/contributors/megginkearney  
