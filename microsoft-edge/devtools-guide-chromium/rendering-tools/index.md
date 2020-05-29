---
title: Analysieren der Laufzeitleistung
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/30/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Web-Entwicklung, F12-Tools, devtools
ms.openlocfilehash: 7705428dba2ca368eb8f61b13bb96901756b081f
ms.sourcegitcommit: 0342d99bf8d3212068890bab0e1e960afa507c02
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/30/2020
ms.locfileid: "10611864"
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





# Analysieren der Laufzeitleistung   




Benutzer erwartet interaktive und glatte Seiten.  Jede Phase in der pixelpipeline stellt eine Möglichkeit dar, Jank einzuführen.  Erfahren Sie mehr über Tools und Strategien, um häufige Probleme zu erkennen und zu beheben, die die Runtime-Leistung verlangsamen.  

### Zusammenfassung  

*   Schreiben Sie keine JavaScript-Daten, die den Browser zwingen, das Layout neu zu berechnen.  Trennen Sie die Lese-und Schreibfunktionen, und führen Sie zuerst Lesevorgänge aus.  
*   Verkomplizieren Sie Ihre CSS nicht.  Verwenden Sie nicht so viel CSS, damit Ihre CSS-Auswahl einfach ist.  
*   Vermeiden Sie das Layout so weit wie möglich.  Wählen Sie CSS aus, das Layout überhaupt nicht auslöst.  
*   Das zeichnen kann mehr Zeit als alle anderen Rendering-Aktivitäten beanspruchen.  Achten Sie auf Farb Engpässe.  

## JavaScript  

JavaScript-Berechnungen, insbesondere diejenigen, die umfangreiche visuelle Änderungen auslösen, können die Anwendungsleistung verzögern.  Lassen Sie nicht zu, dass die Interaktion zwischen unregelmäßigen oder langlebigen JavaScript-Benutzern beeinträchtigt wird.  

### JavaScript: Tools  

Nehmen Sie im **Leistungs** Panel eine Aufzeichnung auf, und suchen Sie nach verdächtig langen `Evaluate Script` Ereignissen.  <!--If you find any, you are able to enable the **JS Profiler** and re-do your recording to get more detailed information about exactly which JavaScript functions were used and how long each took.  -->  

<!--todo: add Recording section when available  -->  
<!--todo: add Profile JavaScript (JS Profiler) section when available  -->  

Wenn Sie einiges an Jank in Ihrem JavaScript bemerken, müssen Sie möglicherweise Ihre Analyse auf die nächste Ebene übertragen und ein JavaScript-CPU-Profil erfassen.  In CPU-Profilen wird angezeigt, wo die Laufzeit innerhalb der Funktionen Ihrer Seite ausgegeben wird.  Erfahren Sie, wie Sie CPU-Profile in der [JavaScript-Laufzeit beschleunigen][DevtoolsRenderingToolsJavascriptRuntime].

### JavaScript: Probleme  

In der folgenden Tabelle werden einige häufige JavaScript-Probleme und mögliche Lösungen beschrieben:  

| Problem | Beispiel | Lösung |  
|:--- |:--- |:--- |  
| Kostspielige Eingabehandler, die die Antwort oder Animation beeinflussen.  | Tippen Sie auf, um den Bildschirm zu scrollen.  | Lassen Sie den Browser Fingereingabe und scrollen, oder binden Sie den Listener so spät wie möglich.  Informationen [zu kostspieligen Eingabe Handlern finden Sie in der Checkliste zur Leistungsfähigkeit von Paul Lewis][WebPerformanceCalendarRuntimeChecklist].  |  
| JavaScript mit starkem Zeitlimit, das die Antwort, Animation, Auslastung beeinflusst.  | Der Benutzer scrollt direkt nach dem Laden der Seite, setTimeout/setInterval.  | JavaScript-Laufzeit optimieren: Verwenden Sie `requestAnimationFrame` , verbreiten Sie DOM-Manipulation über Frames, verwenden Sie [Web-Worker][MDNUsingWebWorkers].  |  
| JavaScript mit langer Laufzeit, das die Antwort beeinflusst.  | Das [DOMContentLoaded-Ereignis][MDNUsingWebWorkers] wird angehalten, da es mit js work überschwemmt wird.  | Verschieben Sie reine Rechenarbeit auf [web work worker][MDNUsingWebWorkers].  Wenn Sie DOM-Zugriff benötigen, verwenden Sie `requestAnimationFrame` .  <!--See also [Optimize JavaScript Execution][WebFundamentalsPerformanceRenderingOptimizeJavascriptRuntime].  -->  |  
| Garbage-y-Skripte, die die Antwort oder Animation beeinflussen.  | Die Garbage Collection kann überall vorkommen.  | Schreiben Sie geringere Garbage-y-Skripte.  Informationen dazu finden Sie unter [Garbage Collection in Animation in Paul Lewis ' Runtime Performance Checkliste][WebPerformanceCalendarRuntimeChecklist].  |  

<!--todo: add Optimize JavaScript runtime section when available  -->  

## Format  

Formatänderungen sind kostspielig, insbesondere dann, wenn sich diese Änderungen auf mehr als ein Element im Dom auswirken.  Jedes Mal, wenn Sie Formatvorlagen auf ein Element anwenden, wird der Browser die Auswirkungen auf alle zugehörigen Elemente ermitteln, das Layout neu berechnen und neu zeichnen.  

<!--Related Guides:  

*   [Reduce the Scope and Complexity of Styles Calculations][WebFundamentalsPerformanceRenderingReduceScope]  
-->  

<!--todo: add Reduce the Scope and Complexity of Styles Calculations section when available -->  

### Formatvorlage: Tools  

Führen Sie eine Aufzeichnung im **Leistungs** Panel aus.  Überprüfen Sie die Aufzeichnung auf große `Recalculate Style` Ereignisse \ (in Lila angezeigt).  

<!--todo: add Recording section when available  -->  

Klicken Sie auf ein `Recalculate Style` Ereignis, um weitere Informationen dazu im **Detail** Bereich anzuzeigen.  Wenn die Formatänderungen sehr lange dauern, handelt es sich um einen leistungserfolg.  Wenn sich die Format Berechnungen auf eine große Anzahl von Elementen auswirken, handelt es sich um einen anderen Bereich mit Raum für Verbesserungen.  

> ##### Abbildung1  
> Formatvorlage ' lange neu berechnen '  
> ![Formatvorlage ' lange neu berechnen '][ImageLongRecalculateStyle]

So verringern Sie die Auswirkungen von `Recalculate Style` Ereignissen:  

*   Verwenden Sie die [CSS-Trigger][CssTriggers] , um zu erfahren, welche CSS-Eigenschaften Layout, Paint und Composite auslösen.  Diese Eigenschaften haben die größten Auswirkungen auf die Leistung des Renderings.  
*   Wechseln Sie zu Eigenschaften, die geringere Auswirkungen haben.  <!--See [Stick to compositor-only properties and manage layer count][WebFundamentalsPerformanceRenderingCompositorOnlyProperties] for more guidance.  -->  

<!--todo: add Stick to compositor-only properties and manage layer count section when available -->  

### Formatvorlage: Probleme  

In der folgenden Tabelle werden einige allgemeine Stil Probleme und mögliche Lösungen beschrieben:  

| Problem | Beispiel | Lösung |  
|:--- |:--- |:--- |  
| Kostspielige Formatvorlagen Berechnungen, die die Antwort oder Animation beeinflussen.  | Eine beliebige CSS-Eigenschaft, die die Geometrie eines Elements ändert, wie Breite, Höhe oder Position; der Browser überprüft alle anderen Elemente und berechnet das Layout neu.  | Vermeiden von CSS, das Layouts auslöst |  
| Komplexe Auswahlen, die die Antwort oder Animation beeinflussen.  | Geschachtelte Auswahlen zwingen den Browser, alles über alle anderen Elemente zu erfahren, einschließlich Eltern und untergeordneten Elementen.  | Verweisen Sie mit nur einer Klasse auf ein Element in Ihrem CSS.  |  

<!--todo: add Avoid CSS that triggers layouts section when available -->  
<!--todo: add Reduce the Scope and Complexity of Styles Calculations (Reference an element in your CSS with just a class) section when available -->  

<!--Related Guides:  

*   [Reduce the Scope and Complexity of Styles Calculations][WebFundamentalsPerformanceRenderingReduceScope]  -->  

<!--todo: add Reduce the Scope and Complexity of Styles Calculations section when available -->  

## Layout  

Layout (oder Reflow in Firefox) ist der Prozess, bei dem der Browser die Positionen und Größen aller Elemente auf einer Seite berechnet.  Das Layout-Modell des Webs bedeutet, dass ein Element andere beeinflussen kann. beispielsweise wirkt sich die Breite des `<body>` Elements in der Regel auf die Breite aller untergeordneten Elemente und so weiter auf die gesamte Struktur nach oben und unten aus.  Der Vorgang ist möglicherweise für den Browser ziemlich kompliziert.  

Als Faustregelgilt: Wenn Sie einen geometrischen Wert zurück aus dem Dom anfordern, bevor ein Frame abgeschlossen ist, werden Sie sich mit "erzwungenen synchronen Layouts" befunden, was ein großer Leistungsengpass sein kann, wenn Sie häufig wiederholt werden oder für eine große DOM-Struktur ausgeführt werden.  

<!--Related Guides:  

*   [Avoid Layout Thrashing][WebFundamentalsPerformanceRenderingAvoidLargeComplexLayouts]  
*   [Diagnose Forced Synchronous Layouts][DevtoolsRenderingToolsForcedSynchronousLayouts]  -->  

<!--todo: add Avoid CSS that triggers layouts (Avoid Layout Thrashing) section when available -->  
<!--todo: add Diagnose Forced Synchronous Layouts section when available  -->  

### Layout: Tools  

Der Bereich " **Leistung** " gibt an, wann eine Seite erzwungene synchrone Layouts verursacht.  Diese `Layout` Ereignisse sind mit roten Balken gekennzeichnet.  

> ##### Abbildung2  
> Erzwungenes synchrones Layout  
> ![Erzwungenes synchrones Layout][ImageForcedSynchronousLayout]  

"Layout-Thrashing" ist eine Wiederholung erzwungener synchroner layoutbedingungen.  Dies tritt auf, wenn JavaScript wiederholt vom Dom geschrieben und gelesen wird, wodurch der Browser die Neuberechnung des Layouts erzwungen.  Suchen Sie nach einem Muster mehrerer erzwungener synchroner Layout-Warnungen, um das verprügeln des Layouts zu erkennen.  Siehe [Abbildung 2](#figure-2).  

### Layout: Probleme  

In der folgenden Tabelle werden einige häufige Probleme beim Layout und mögliche Lösungen beschrieben:  

| Problem | Beispiel | Lösung |  
|:--- |:--- |:--- |  
| Erzwungenes synchrones Layout, das die Antwort oder Animation beeinflusst.  | Erzwingen, dass der Browser das Layout zuvor in der pixelpipeline ausführt, wodurch sich wieder holende Schritte im Renderingprozess ergeben.  | Stapeln Sie Ihre Formatvorlage zuerst, und führen Sie dann alle Schreibvorgänge aus.  <!--See also [Avoid large, complex layouts and layout thrashing][WebFundamentalsPerformanceRenderingAvoidLargeComplexLayouts].  -->  |  
| Das Layout verprügelt Auswirkungen auf die Antwort oder Animation.  | Eine Schleife, die den Browser in einen Lese-Schreib-Lese-/Schreibzugriff.-Zyklus versetzt, wodurch der Browser das Layout immer wieder neu berechnet.  | Automatisches Stapeln von Lese-und Schreibvorgängen mithilfe der [FastDom-Bibliothek][GitHubWilsonpageFastdom]  |  

<!--todo: add Avoid CSS that triggers layouts (Avoid large, complex layouts and layout thrashing) section when available -->  

## Malen und Composite  

Paint ist der Vorgang des Füllens von Pixeln.  Es ist oft der kostspieligste Teil des Rendering-Prozesses.  Wenn Sie festgestellt haben, dass Ihre Seite in irgendeiner Weise Janky ist, haben Sie wahrscheinlich Probleme mit Paint.  

Compositing ist der Ort, an dem die gemalten Teile der Seite für die Anzeige auf dem Bildschirm zusammengestellt werden.  In den meisten Fällen sollten Sie, wenn Sie sich an nur für Compositor-Eigenschaften halten und die Farbe ganz vermeiden, eine deutliche Verbesserung der Leistung festzustellen, doch müssen Sie auf eine übermäßige Anzahl von Ebenen achten.  <!--See also [Stick to compositor-only properties and manage layer count][WebFundamentalsPerformanceRenderingCompositorOnlyProperties].  -->  

<!--todo: add Stick to compositor-only properties and manage layer count section when available  -->  

### Paint und Composite: Tools  

Möchten Sie wissen, wie lange das Malen dauert oder wie oft gemalt wird?  Aktivieren Sie das Kontrollkästchen [Erweiterte Farben Instrumentation aktivieren][DevtoolsChromiumEvaluatePerformanceReferenceEnableadvancedpaintinstrumentation] im **Leistungs** Panel, und nehmen Sie dann eine Aufzeichnung vor.  Wenn die meiste Zeit für das Rendern von Bildern verwendet wird, gibt es Probleme mit der Farbwiedergabe.  

<!--
> ##### Old Figure 3  
> Long paint times in timeline recording  
> ![Long paint times in timeline recording][ImageLongPaintTimes]  
-->  

<!--
Check out the **Rendering** panel for further configurations that are able to help you diagnose paint problems.  -->  

<!--todo: link Rendering panel in ../evaluate-performance/timeline-tool  sub-section when live  -->  

### Paint und Composite: Probleme  

In der folgenden Tabelle werden einige häufige Probleme bei der Farb-und Zusammensetzung und mögliche Lösungen beschrieben:  

| Problem | Beispiel | Lösung |  
|:--- |:--- |:--- |  
| Malen Sie Stürme, die die Antwort oder Animation beeinflussen.  | Große Farbbereiche oder kostspielige Farben, die die Antwort oder Animation beeinflussen.  | Vermeiden Sie Paint, fördern Sie Elemente, die in eine eigene Ebene verschoben werden, und verwenden Sie Transformationen und Deckkraft.  <!--See [Simplify paint complexity and reduce paint areas][WebFundamentalsPerformanceRenderingSimplifyPaintComplexity].  -->  |  
| Layer-Explosionen, die Animationen beeinflussen  | Die über Förderung von zu vielen Elementen mit `translateZ(0)` starkem Einfluss auf die animationsleistung.  | Werben Sie auf Ebenen sparsam, und nur, wenn Sie wissen, dass es greifbare Verbesserungen bietet.  <!--See [Stick to composite-only properties and manage layer count][WebFundamentalsPerformanceRenderingCompositorOnlyProperties].  -->  |  

<!--todo: add Simplify paint complexity and reduce paint areas section when available  -->  
<!--todo: add Stick to compositor-only properties and manage layer count section when available  -->  

<!--## Feedback   -->  



<!-- image links -->  

[ImageLongRecalculateStyle]: /microsoft-edge/devtools-guide-chromium/media/rendering-tools-performance-recalculate-style-summary.msft.png "Abbildung 1: langes Neuberechnen des Formats"  
[ImageForcedSynchronousLayout]: /microsoft-edge/devtools-guide-chromium/media/rendering-tools-jank-performance-recalculate-style-summary.msft.png "Abbildung 2: Erzwungenes synchrones Layout"  
<!--[ImageLongPaintTimes]: /microsoft-edge/devtools-guide-chromium/media/rendering-tools-jank-performance-advanced-paint-instrumentation-summary.msft.png "Old Figure 3: Long paint times in timeline recording"  -->  

<!-- links -->  

[DevtoolsRenderingToolsJavascriptRuntime]: /microsoft-edge/devtools-guide-chromium/rendering-tools/js-runtime "Beschleunigen der JavaScript-Laufzeit"  

[DevtoolsChromiumEvaluatePerformanceReferenceEnableadvancedpaintinstrumentation]: /microsoft-edge/devtools-guide-chromium/evaluate-performance/reference#enable-advanced-paint-instrumentation "Aktivieren von Advanced Paint Instrumentation – Referenz zur Leistungsanalyse"

<!--[DevtoolsRenderingToolsForcedSynchronousLayouts]: /microsoft-edge/devtools-guide-chromium/rendering-tools/forced-synchronous-layouts "Diagnose Forced Synchronous Layouts"  -->  

<!-- The Timeline Tool page is deprecated  -->  
<!--[DevtoolsEvaluatePerformanceTimelineToolProfileJavascript]: /microsoft-edge/devtools-guide-chromium/evaluate-performance/timeline-tool#profile-javascript "Profile JavaScript - How to Use the Timeline Tool"  -->  
<!--[DevtoolsEvaluatePerformanceTimelineToolProfilePainting]: /microsoft-edge/devtools-guide-chromium/evaluate-performance/timeline-tool#profile-painting "Profile painting - How to Use the Timeline Tool"  -->  
<!--[DevtoolsEvaluatePerformanceTimelineToolRecording]: /microsoft-edge/devtools-guide-chromium/evaluate-performance/timeline-tool#make-a-recording "Make a recording - How to Use the Timeline Tool"  -->  
<!--[DevtoolsEvaluatePerformanceTimelineToolRenderingSettings]: /microsoft-edge/devtools-guide-chromium/evaluate-performance/timeline-tool#rendering-settings "Rendering settings - How to Use the Timeline Tool"  -->  

<!--[WebFundamentalsPerformanceRenderingAvoidLargeComplexLayouts]: /web/fundamentals/performance/rendering/avoid-large-complex-layouts-and-layout-thrashing "Avoid Large, Complex Layouts, and Layout Thrashing"  -->  
<!--[WebFundamentalsPerformanceRenderingOptimizeJavascriptRuntime]: /web/fundamentals/performance/rendering/optimize-javascript-execution "Optimize JavaScript Runtime"  -->  
<!--[WebFundamentalsPerformanceRenderingReduceScope]: /web/fundamentals/performance/rendering/reduce-the-scope-and-complexity-of-style-calculations "Reduce the Scope and Complexity of Style Calculations"  -->  
<!--[WebFundamentalsPerformanceRenderingSimplifyPaintComplexity]: /web/fundamentals/performance/rendering/simplify-paint-complexity-and-reduce-paint-areas "Simplify Paint Complexity and Reduce Paint Areas"  -->  
<!--[WebFundamentalsPerformanceRenderingCompositorOnlyProperties]: /web/fundamentals/performance/rendering/stick-to-compositor-only-properties-and-manage-layer-count "Stick to Compositor-Only Properties and Manage Layer Count"  -->  

[CssTriggers]: https://csstriggers.com "CSS-Trigger"  

[MDNUsingWebWorkers]: https://developer.mozilla.org/docs/Web/API/Web_Workers_API/Using_web_workers "Verwenden von Web Workers | MDN"  

[WebPerformanceCalendarRuntimeChecklist]: https://calendar.perfplanet.com/2013/the-runtime-performance-checklist/ "Die Checkliste für die Laufzeitleistung – webleistungs Kalender"  

[GitHubWilsonpageFastdom]: https://github.com/wilsonpage/fastdom "wilsonpage/fastdom | GitHub"  

> [!NOTE]
> Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.  
> Die ursprüngliche Seite wird [hier](https://developers.google.com/web/tools/chrome-devtools/rendering-tools/index) gefunden und von [Kayce Basken][KayceBasques] (Technical Writer, Chrome devtools \ & Lighthouse \) und [Meggin Kearney][MegginKearney] \ (Tech Writer \) erstellt.  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[MegginKearney]: https://developers.google.com/web/resources/contributors/megginkearney  
