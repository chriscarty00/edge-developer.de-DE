---
description: Benutzer erwarten interaktive und flüssige Seiten.  Jede Phase in der Pixelpipeline stellt eine Möglichkeit dar, jank einzuführen.  Erfahren Sie mehr über Tools und Strategien zum Identifizieren und Beheben gängiger Probleme, die die Laufzeitleistung verlangsamen.
title: Analysieren der Laufzeitleistung
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, Entwicklungstools
ms.openlocfilehash: d5c37c188ae9038a7baafc936d2a02299def6366
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/13/2021
ms.locfileid: "11564707"
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
# <a name="analyze-runtime-performance"></a><span data-ttu-id="a3af9-106">Analysieren der Laufzeitleistung</span><span class="sxs-lookup"><span data-stu-id="a3af9-106">Analyze runtime performance</span></span>  

<span data-ttu-id="a3af9-107">Benutzer erwarten interaktive und flüssige Seiten.</span><span class="sxs-lookup"><span data-stu-id="a3af9-107">Users expects interactive and smooth pages.</span></span>  <span data-ttu-id="a3af9-108">Jede Phase in der Pixelpipeline stellt eine Möglichkeit dar, jank einzuführen.</span><span class="sxs-lookup"><span data-stu-id="a3af9-108">Each stage in the pixel pipeline represents an opportunity to introduce jank.</span></span>  <span data-ttu-id="a3af9-109">Erfahren Sie mehr über Tools und Strategien zum Identifizieren und Beheben gängiger Probleme, die die Laufzeitleistung verlangsamen.</span><span class="sxs-lookup"><span data-stu-id="a3af9-109">Learn about tools and strategies to identify and fix common problems that slow down runtime performance.</span></span>  

### <a name="summary"></a><span data-ttu-id="a3af9-110">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="a3af9-110">Summary</span></span>  

*   <span data-ttu-id="a3af9-111">Schreiben Sie kein JavaScript, das den Browser zwingt, das Layout neu zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="a3af9-111">Do not write JavaScript that forces the browser to recalculate layout.</span></span>  <span data-ttu-id="a3af9-112">Trennen Sie Lese- und Schreibfunktionen, und führen Sie zuerst Lesezugriffe aus.</span><span class="sxs-lookup"><span data-stu-id="a3af9-112">Separate read and write functions, and perform reads first.</span></span>  
*   <span data-ttu-id="a3af9-113">Komplizieren Sie Ihre CSS nicht überkompliziert.</span><span class="sxs-lookup"><span data-stu-id="a3af9-113">Do not over-complicate your CSS.</span></span>  <span data-ttu-id="a3af9-114">Verwenden Sie weniger CSS, und halten Sie Ihre CSS-Selektoren einfach.</span><span class="sxs-lookup"><span data-stu-id="a3af9-114">Use less CSS and keep your CSS selectors simple.</span></span>  
*   <span data-ttu-id="a3af9-115">Vermeiden Sie das Layout so weit wie möglich.</span><span class="sxs-lookup"><span data-stu-id="a3af9-115">Avoid layout as much as possible.</span></span>  <span data-ttu-id="a3af9-116">Wählen Sie CSS aus, das das Layout überhaupt nicht auslöst.</span><span class="sxs-lookup"><span data-stu-id="a3af9-116">Choose CSS that does not trigger layout at all.</span></span>  
*   <span data-ttu-id="a3af9-117">Das Malen kann länger dauern als jede andere Renderingaktivität.</span><span class="sxs-lookup"><span data-stu-id="a3af9-117">Painting may take up more time than any other rendering activity.</span></span>  <span data-ttu-id="a3af9-118">Achten Sie auf Farbengpässe.</span><span class="sxs-lookup"><span data-stu-id="a3af9-118">Watch out for paint bottlenecks.</span></span>  
    
## <a name="javascript"></a><span data-ttu-id="a3af9-119">JavaScript</span><span class="sxs-lookup"><span data-stu-id="a3af9-119">JavaScript</span></span>  

<span data-ttu-id="a3af9-120">JavaScript-Berechnungen, insbesondere diejenigen, die umfangreiche visuelle Änderungen auslösen, können die Anwendungsleistung beeinträchtigen.</span><span class="sxs-lookup"><span data-stu-id="a3af9-120">JavaScript calculations, especially ones that trigger extensive visual changes, may stall application performance.</span></span>  <span data-ttu-id="a3af9-121">Lassen Sie nicht zu, dass sich schlecht zeitgezeitte oder lang ausgeführte JavaScript in Benutzerinteraktionen einmischt.</span><span class="sxs-lookup"><span data-stu-id="a3af9-121">Do not let badly-timed or long-running JavaScript interfere with user interactions.</span></span>  

### <a name="javascript-tools"></a><span data-ttu-id="a3af9-122">JavaScript: Tools</span><span class="sxs-lookup"><span data-stu-id="a3af9-122">JavaScript: Tools</span></span>  

<span data-ttu-id="a3af9-123">Nehmen Sie eine Aufzeichnung im **Leistungstool** vor, und suchen Sie nach verdächtig langen `Evaluate Script` Ereignissen.</span><span class="sxs-lookup"><span data-stu-id="a3af9-123">Take a recording in the **Performance** tool and look for suspiciously long `Evaluate Script` events.</span></span>  <!--If you find any, you are able to enable the **JS Profiler** and re-do your recording to get more detailed information about exactly which JavaScript functions were used and how long each took.  -->  

<!--todo: add Recording section when available  -->  
<!--todo: add Profile JavaScript (JS Profiler) section when available  -->  

<span data-ttu-id="a3af9-124">f Sie in Ihrem JavaScript ein wenig Jank notieren, müssen Sie Ihre Analyse möglicherweise auf die nächste Ebene bringen und ein JavaScript-CPU-Profil sammeln.</span><span class="sxs-lookup"><span data-stu-id="a3af9-124">f you noticing quite a bit of jank in your JavaScript, you may need to take your analysis to the next level and collect a JavaScript CPU profile.</span></span>  <span data-ttu-id="a3af9-125">CPU-Profile zeigen an, wo die Laufzeit innerhalb der Funktionen Ihrer Seite ausgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="a3af9-125">CPU profiles show where runtime is spent within the functions of your page.</span></span>  <span data-ttu-id="a3af9-126">Informationen zum Erstellen von CPU-Profilen finden Sie unter [Beschleunigen der JavaScript-Runtime][DevtoolsRenderingToolsJavascriptRuntime].</span><span class="sxs-lookup"><span data-stu-id="a3af9-126">Learn how to create CPU profiles in [Speed Up JavaScript Runtime][DevtoolsRenderingToolsJavascriptRuntime].</span></span>

### <a name="javascript-problems"></a><span data-ttu-id="a3af9-127">JavaScript: Probleme</span><span class="sxs-lookup"><span data-stu-id="a3af9-127">JavaScript: Problems</span></span>  

<span data-ttu-id="a3af9-128">In der folgenden Tabelle werden einige häufige JavaScript-Probleme und mögliche Lösungen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="a3af9-128">The following table describes some common JavaScript problems and potential solutions.</span></span>  

| <span data-ttu-id="a3af9-129">Problem</span><span class="sxs-lookup"><span data-stu-id="a3af9-129">Problem</span></span> | <span data-ttu-id="a3af9-130">Beispiel</span><span class="sxs-lookup"><span data-stu-id="a3af9-130">Example</span></span> | <span data-ttu-id="a3af9-131">Lösung</span><span class="sxs-lookup"><span data-stu-id="a3af9-131">Solution</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="a3af9-132">Teure Eingabehandler, die die Antwort oder Animation beeinflussen.</span><span class="sxs-lookup"><span data-stu-id="a3af9-132">Expensive input handlers affecting response or animation.</span></span>  | <span data-ttu-id="a3af9-133">Touch- und Parallax-Bildlauf.</span><span class="sxs-lookup"><span data-stu-id="a3af9-133">Touch, parallax scrolling.</span></span>  | <span data-ttu-id="a3af9-134">Lassen Sie den Browser Touch- und Bildlauf verarbeiten oder den Listener so spät wie möglich binden.</span><span class="sxs-lookup"><span data-stu-id="a3af9-134">Let the browser handle touch and scrolls, or bind the listener as late as possible.</span></span>  <span data-ttu-id="a3af9-135">Navigieren Sie [in der Prüfliste zur][WebPerformanceCalendarRuntimeChecklist]Laufzeitleistung von Paul Lewis zu Teure Eingabehandler.</span><span class="sxs-lookup"><span data-stu-id="a3af9-135">Navigate to [Expensive Input Handlers in Paul Lewis' runtime performance checklist][WebPerformanceCalendarRuntimeChecklist].</span></span>  |  
| <span data-ttu-id="a3af9-136">Ungültige JavaScript-Zeit, die sich auf Antwort, Animation, Last ausdingt.</span><span class="sxs-lookup"><span data-stu-id="a3af9-136">Badly-timed JavaScript affecting response, animation, load.</span></span>  | <span data-ttu-id="a3af9-137">Benutzer scrollt direkt nach Seitenlade, setTimeout /setInterval.</span><span class="sxs-lookup"><span data-stu-id="a3af9-137">User scrolls right after page load, setTimeout / setInterval.</span></span>  | <span data-ttu-id="a3af9-138">Optimieren der JavaScript-Laufzeit: `requestAnimationFrame` Verwenden Sie , verteilen Sie die DOM-Manipulation über Frames, verwenden Sie Web [Workers][MDNUsingWebWorkers].</span><span class="sxs-lookup"><span data-stu-id="a3af9-138">Optimize JavaScript runtime: use `requestAnimationFrame`, spread DOM manipulation over frames, use [Web Workers][MDNUsingWebWorkers].</span></span>  |  
| <span data-ttu-id="a3af9-139">Lang ausgeführtes JavaScript, das sich auf die Antwort ausdingt.</span><span class="sxs-lookup"><span data-stu-id="a3af9-139">Long-running JavaScript affecting response.</span></span>  | <span data-ttu-id="a3af9-140">Das [DOMContentLoaded-Ereignis][MDNUsingWebWorkers] wird beim Überschwemmen der JS-Arbeit ins Stocken geraten.</span><span class="sxs-lookup"><span data-stu-id="a3af9-140">The [DOMContentLoaded event][MDNUsingWebWorkers] stalls as it is swamped with JS work.</span></span>  | <span data-ttu-id="a3af9-141">Verschieben Sie reine Rechenarbeit zu [Web Workers][MDNUsingWebWorkers].</span><span class="sxs-lookup"><span data-stu-id="a3af9-141">Move pure computational work to [Web Workers][MDNUsingWebWorkers].</span></span>  <span data-ttu-id="a3af9-142">Wenn Sie DOM-Zugriff benötigen, verwenden Sie `requestAnimationFrame` .</span><span class="sxs-lookup"><span data-stu-id="a3af9-142">If you need DOM access, use `requestAnimationFrame`.</span></span>  <!--Navigate to [Optimize JavaScript Execution][WebFundamentalsPerformanceRenderingOptimizeJavascriptRuntime].  -->  |  
| <span data-ttu-id="a3af9-143">Garbage-y-Skripts, die die Antwort oder Animation beeinflussen.</span><span class="sxs-lookup"><span data-stu-id="a3af9-143">Garbage-y scripts affecting response or animation.</span></span>  | <span data-ttu-id="a3af9-144">Die Garbage Collection kann an einer beliebigen Stelle vorkommen.</span><span class="sxs-lookup"><span data-stu-id="a3af9-144">Garbage collection may happen anywhere.</span></span>  | <span data-ttu-id="a3af9-145">Schreiben Sie weniger Garbage-y-Skripts.</span><span class="sxs-lookup"><span data-stu-id="a3af9-145">Write less garbage-y scripts.</span></span>  <span data-ttu-id="a3af9-146">Navigieren Sie [zu Garbage Collection in Animation in Der Prüfliste zur Laufzeitleistung von Paul Lewis][WebPerformanceCalendarRuntimeChecklist].</span><span class="sxs-lookup"><span data-stu-id="a3af9-146">Navigate to [Garbage Collection in Animation in Paul Lewis' runtime performance checklist][WebPerformanceCalendarRuntimeChecklist].</span></span>  |  

<!--todo: add Optimize JavaScript runtime section when available  -->  

## <a name="style"></a><span data-ttu-id="a3af9-147">Format</span><span class="sxs-lookup"><span data-stu-id="a3af9-147">Style</span></span>  

<span data-ttu-id="a3af9-148">Formatänderungen sind kostspielig, insbesondere wenn sich diese Änderungen auf mehr als ein Element im DOM auswirken.</span><span class="sxs-lookup"><span data-stu-id="a3af9-148">Style changes are costly, especially if those changes affect more than one element in the DOM.</span></span>  <span data-ttu-id="a3af9-149">Jedes Mal, wenn Sie Formatvorlagen auf ein Element anwenden, berechnet der Browser die Auswirkungen auf alle zugehörigen Elemente, berechnet das Layout neu und aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="a3af9-149">Any time you apply styles to an element, the browser figures out the impact on all related elements, recalculates the layout, and repaints.</span></span>  

<!--Related Guides:  

*   [Reduce the Scope and Complexity of Styles Calculations][WebFundamentalsPerformanceRenderingReduceScope]  
-->  

<!--todo: add Reduce the Scope and Complexity of Styles Calculations section when available -->  

### <a name="style-tools"></a><span data-ttu-id="a3af9-150">Formatvorlage: Tools</span><span class="sxs-lookup"><span data-stu-id="a3af9-150">Style: Tools</span></span>  

<span data-ttu-id="a3af9-151">Nehmen Sie eine Aufzeichnung im **Leistungstool** vor.</span><span class="sxs-lookup"><span data-stu-id="a3af9-151">Take a recording in the **Performance** tool.</span></span>  <span data-ttu-id="a3af9-152">Überprüfen Sie die Aufzeichnung auf `Recalculate Style` große Ereignisse \(angezeigt in Lila\).</span><span class="sxs-lookup"><span data-stu-id="a3af9-152">Check the recording for large `Recalculate Style` events \(displayed in purple\).</span></span>  

<!--todo: add Recording section when available  -->  

<span data-ttu-id="a3af9-153">Wählen Sie `Recalculate Style` ein Ereignis aus, um weitere Informationen dazu im **Detailbereich anzuzeigen.**</span><span class="sxs-lookup"><span data-stu-id="a3af9-153">Choose a `Recalculate Style` event to view more information about it in the **Details** pane.</span></span>  <span data-ttu-id="a3af9-154">Wenn die Formatvorlageänderungen sehr lange dauern, ist dies ein Leistungstreffer.</span><span class="sxs-lookup"><span data-stu-id="a3af9-154">If the style changes are taking a long time, that is a performance hit.</span></span>  <span data-ttu-id="a3af9-155">Wenn sich die Formatvorlageberechnungen auf eine große Anzahl von Elementen ausdingen, ist dies ein weiterer Bereich mit Verbesserungsmöglichkeiten.</span><span class="sxs-lookup"><span data-stu-id="a3af9-155">If the style calculations are affecting a large number of elements, that is another area with room for improvement.</span></span>  

:::image type="complex" source="../media/rendering-tools-performance-recalculate-style-summary.msft.png" alt-text="Langes Neuberechnungsformat" lightbox="../media/rendering-tools-performance-recalculate-style-summary.msft.png":::
   <span data-ttu-id="a3af9-157">Langes Neuberechnungsformat</span><span class="sxs-lookup"><span data-stu-id="a3af9-157">Long recalculate style</span></span>  
:::image-end:::  

<span data-ttu-id="a3af9-158">So reduzieren Sie die Auswirkungen von `Recalculate Style` Ereignissen:</span><span class="sxs-lookup"><span data-stu-id="a3af9-158">To reduce the impact of `Recalculate Style` events:</span></span>  

*   <span data-ttu-id="a3af9-159">Verwenden Sie die [CSS-Trigger,][CssTriggers] um zu erfahren, welche CSS-Eigenschaften Layout, Paint und Composite auslösen.</span><span class="sxs-lookup"><span data-stu-id="a3af9-159">Use the [CSS Triggers][CssTriggers] to learn which CSS properties trigger layout, paint, and composite.</span></span>  <span data-ttu-id="a3af9-160">Diese Eigenschaften haben die größten Auswirkungen auf die Renderingleistung.</span><span class="sxs-lookup"><span data-stu-id="a3af9-160">These properties have the worst impact on rendering performance.</span></span>  
*   <span data-ttu-id="a3af9-161">Wechseln Sie zu Eigenschaften, die weniger Auswirkungen haben.</span><span class="sxs-lookup"><span data-stu-id="a3af9-161">Switch to properties that have less impact.</span></span>  <!--For more guidance, navigate to [Stick to compositor-only properties and manage layer count][WebFundamentalsPerformanceRenderingCompositorOnlyProperties].  -->  
    
<!--todo: add Stick to compositor-only properties and manage layer count section when available -->  

### <a name="style-problems"></a><span data-ttu-id="a3af9-162">Formatvorlage: Probleme</span><span class="sxs-lookup"><span data-stu-id="a3af9-162">Style: Problems</span></span>  

<span data-ttu-id="a3af9-163">In der folgenden Tabelle werden einige häufige Stilprobleme und mögliche Lösungen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="a3af9-163">The following table describes some common style problems and potential solutions.</span></span>  

| <span data-ttu-id="a3af9-164">Problem</span><span class="sxs-lookup"><span data-stu-id="a3af9-164">Problem</span></span> | <span data-ttu-id="a3af9-165">Beispiel</span><span class="sxs-lookup"><span data-stu-id="a3af9-165">Example</span></span> | <span data-ttu-id="a3af9-166">Lösung</span><span class="sxs-lookup"><span data-stu-id="a3af9-166">Solution</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="a3af9-167">Teure Formatvorlageberechnungen, die sich auf Die Antwort oder Animation ausdingen.</span><span class="sxs-lookup"><span data-stu-id="a3af9-167">Expensive style calculations affecting response or animation.</span></span>  | <span data-ttu-id="a3af9-168">Jede CSS-Eigenschaft, die die Geometrie eines Elements ändert, z. B. die Breite, Höhe oder Position; Der Browser überprüft alle anderen Elemente und berechnet das Layout neu.</span><span class="sxs-lookup"><span data-stu-id="a3af9-168">Any CSS property that changes the geometry of an element, like the width, height, or position; the browser checks all other elements and recalculates the layout.</span></span>  | <span data-ttu-id="a3af9-169">Vermeiden von CSS, das Layouts auslöst</span><span class="sxs-lookup"><span data-stu-id="a3af9-169">Avoid CSS that triggers layouts</span></span> |  
| <span data-ttu-id="a3af9-170">Komplexe Selektoren, die die Antwort oder Animation beeinflussen.</span><span class="sxs-lookup"><span data-stu-id="a3af9-170">Complex selectors affecting response or animation.</span></span>  | <span data-ttu-id="a3af9-171">Geschachtelte Selektoren zwingen den Browser, alles über alle anderen Elemente, einschließlich Eltern und Kinder, zu wissen.</span><span class="sxs-lookup"><span data-stu-id="a3af9-171">Nested selectors force the browser to know everything about all the other elements, including parents and children.</span></span>  | <span data-ttu-id="a3af9-172">Verweisen Sie auf ein Element in Ihrer CSS mit nur einer Klasse.</span><span class="sxs-lookup"><span data-stu-id="a3af9-172">Reference an element in your CSS with just a class.</span></span>  |  

<!--todo: add Avoid CSS that triggers layouts section when available -->  
<!--todo: add Reduce the Scope and Complexity of Styles Calculations (Reference an element in your CSS with just a class) section when available -->  

<!--Related Guides:  

*   [Reduce the Scope and Complexity of Styles Calculations][WebFundamentalsPerformanceRenderingReduceScope]  -->  

<!--todo: add Reduce the Scope and Complexity of Styles Calculations section when available -->  

## <a name="layout"></a><span data-ttu-id="a3af9-173">Layout</span><span class="sxs-lookup"><span data-stu-id="a3af9-173">Layout</span></span>  

<span data-ttu-id="a3af9-174">Layout (oder Reflow in Firefox) ist der Prozess, mit dem der Browser die Positionen und Größen aller Elemente auf einer Seite berechnet.</span><span class="sxs-lookup"><span data-stu-id="a3af9-174">Layout (or reflow in Firefox) is the process by which the browser calculates the positions and sizes of all the elements on a page.</span></span>  <span data-ttu-id="a3af9-175">Das Layoutmodell des Webs bedeutet, dass sich ein Element auf andere auswirken kann. Beispielsweise wirkt sich die Breite des Elements in der Regel auf die Breite aller untergeordneten Elemente aus, und so weiter, bis hin zur `<body>` Struktur nach oben und unten.</span><span class="sxs-lookup"><span data-stu-id="a3af9-175">The layout model of the web means that one element may affect others; for example, the width of the `<body>` element typically affects the widths of any child elements, and so on, all the way up and down the tree.</span></span>  <span data-ttu-id="a3af9-176">Der Prozess kann für den Browser sehr involviert sein.</span><span class="sxs-lookup"><span data-stu-id="a3af9-176">The process may be quite involved for the browser.</span></span>  

<span data-ttu-id="a3af9-177">Als allgemeine Faustregel gilt: Wenn Sie einen geometrischen Wert aus dem DOM zurück fordern, bevor ein Frame abgeschlossen ist, werden Sie sich mit "erzwungenen synchronen Layouts" befinden. Dies kann ein großer Leistungsengpässe sein, wenn er häufig wiederholt oder für eine große DOM-Struktur ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a3af9-177">As a general rule of thumb, if you ask for a geometric value back from the DOM before a frame is complete, you are going to find yourself with "forced synchronous layouts", which may be a big performance bottleneck if repeated frequently or performed for a large DOM tree.</span></span>  

<!--Related Guides:  

*   [Avoid Layout Thrashing][WebFundamentalsPerformanceRenderingAvoidLargeComplexLayouts]  
*   [Diagnose Forced Synchronous Layouts][DevtoolsRenderingToolsForcedSynchronousLayouts]  -->  

<!--todo: add Avoid CSS that triggers layouts (Avoid Layout Thrashing) section when available -->  
<!--todo: add Diagnose Forced Synchronous Layouts section when available  -->  

### <a name="layout-tools"></a><span data-ttu-id="a3af9-178">Layout: Tools</span><span class="sxs-lookup"><span data-stu-id="a3af9-178">Layout: Tools</span></span>  

<span data-ttu-id="a3af9-179">Der **Bereich Leistung** gibt an, wann eine Seite erzwungene synchrone Layouts verursacht.</span><span class="sxs-lookup"><span data-stu-id="a3af9-179">The **Performance** pane identifies when a page causes forced synchronous layouts.</span></span>  <span data-ttu-id="a3af9-180">Diese `Layout` Ereignisse sind mit roten Balken markiert.</span><span class="sxs-lookup"><span data-stu-id="a3af9-180">These `Layout` events are marked with red bars.</span></span>  

:::image type="complex" source="../media/rendering-tools-jank-performance-recalculate-style-summary.msft.png" alt-text="Erzwungenes synchrones Layout" lightbox="../media/rendering-tools-jank-performance-recalculate-style-summary.msft.png":::
   <span data-ttu-id="a3af9-182">Erzwungenes synchrones Layout</span><span class="sxs-lookup"><span data-stu-id="a3af9-182">Forced synchronous layout</span></span>  
:::image-end:::  

<span data-ttu-id="a3af9-183">"Layout shing" ist eine Wiederholung erzwungener synchroner Layoutbedingungen.</span><span class="sxs-lookup"><span data-stu-id="a3af9-183">"Layout thrashing" is a repetition of forced synchronous layout conditions.</span></span>  <span data-ttu-id="a3af9-184">Dies tritt auf, wenn JavaScript wiederholt aus dem DOM schreibt und liest, was den Browser zwingt, das Layout immer wieder neu zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="a3af9-184">This occurs when JavaScript writes and reads from the DOM repeatedly, which forces the browser to recalculate the layout over and over.</span></span>  <span data-ttu-id="a3af9-185">Suchen Sie zum Identifizieren des Layoutbrands nach einem Muster mehrerer erzwungener synchroner Layoutwarnungen.</span><span class="sxs-lookup"><span data-stu-id="a3af9-185">To identify layout thrashing, look for a pattern of multiple forced synchronous layout warnings.</span></span>  <span data-ttu-id="a3af9-186">Überprüfen Sie die vorherige Abbildung.</span><span class="sxs-lookup"><span data-stu-id="a3af9-186">Review the previous figure.</span></span>  

### <a name="layout-problems"></a><span data-ttu-id="a3af9-187">Layout: Probleme</span><span class="sxs-lookup"><span data-stu-id="a3af9-187">Layout: Problems</span></span>  

<span data-ttu-id="a3af9-188">In der folgenden Tabelle werden einige häufige Layoutprobleme und mögliche Lösungen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="a3af9-188">The following table describes some common layout problems and potential solutions.</span></span>  

| <span data-ttu-id="a3af9-189">Problem</span><span class="sxs-lookup"><span data-stu-id="a3af9-189">Problem</span></span> | <span data-ttu-id="a3af9-190">Beispiel</span><span class="sxs-lookup"><span data-stu-id="a3af9-190">Example</span></span> | <span data-ttu-id="a3af9-191">Lösung</span><span class="sxs-lookup"><span data-stu-id="a3af9-191">Solution</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="a3af9-192">Erzwungenes synchrones Layout, das die Antwort oder Animation beeinflusst.</span><span class="sxs-lookup"><span data-stu-id="a3af9-192">Forced synchronous layout affecting response or animation.</span></span>  | <span data-ttu-id="a3af9-193">Erzwingen, dass der Browser das Layout früher in der Pixelpipeline ausführen muss, was zu wiederholten Schritten im Renderingprozess führt.</span><span class="sxs-lookup"><span data-stu-id="a3af9-193">Forcing the browser to perform layout earlier in the pixel pipeline, resulting in repeating steps in the rendering process.</span></span>  | <span data-ttu-id="a3af9-194">Batch, in dem Ihre Formatvorlage zuerst gelesen wird, und anschließend schreibe.</span><span class="sxs-lookup"><span data-stu-id="a3af9-194">Batch your style reads first, then do any writes.</span></span>  <!--Navigate to [Avoid large, complex layouts and layout thrashing][WebFundamentalsPerformanceRenderingAvoidLargeComplexLayouts].  -->  |  
| <span data-ttu-id="a3af9-195">Layoutbrandung, die sich auf Die Antwort oder Animation ausdingt.</span><span class="sxs-lookup"><span data-stu-id="a3af9-195">Layout thrashing affecting response or animation.</span></span>  | <span data-ttu-id="a3af9-196">Eine Schleife, die den Browser in einen Lese-/Lese-/Schreibzyklus versetzt und den Browser dazu zwingt, das Layout immer wieder neu zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="a3af9-196">A loop that puts the browser into a read-write-read-write cycle, forcing the browser to recalculate layout over and over again.</span></span>  | <span data-ttu-id="a3af9-197">Automatische Batch-Lese-/Schreibvorgänge mithilfe der [FastDom-Bibliothek][GitHubWilsonpageFastdom].</span><span class="sxs-lookup"><span data-stu-id="a3af9-197">Automatically batch read-write operations using [FastDom library][GitHubWilsonpageFastdom].</span></span>  |  

<!--todo: add Avoid CSS that triggers layouts (Avoid large, complex layouts and layout thrashing) section when available -->  

## <a name="paint-and-composite"></a><span data-ttu-id="a3af9-198">Paint und zusammengesetzt</span><span class="sxs-lookup"><span data-stu-id="a3af9-198">Paint and composite</span></span>  

<span data-ttu-id="a3af9-199">Paint ist der Vorgang des Ausfüllens von Pixeln.</span><span class="sxs-lookup"><span data-stu-id="a3af9-199">Paint is the process of filling in pixels.</span></span>  <span data-ttu-id="a3af9-200">Dies ist häufig der kostspieligste Teil des Renderingprozesses.</span><span class="sxs-lookup"><span data-stu-id="a3af9-200">It is often the most costly part of the rendering process.</span></span>  <span data-ttu-id="a3af9-201">Wenn Sie feststellen, dass Ihre Seite nicht so funktioniert, wie sie entworfen wurde, ist es wahrscheinlich, dass Sie Farbprobleme haben.</span><span class="sxs-lookup"><span data-stu-id="a3af9-201">If you noticed that your page is not working as designed in any way, it is likely that you have paint problems.</span></span>  

<span data-ttu-id="a3af9-202">Beim Compositing werden die dargestellten Teile der Seite für die Anzeige auf dem Bildschirm gegliedert.</span><span class="sxs-lookup"><span data-stu-id="a3af9-202">Compositing is where the painted parts of the page are put together for displaying on screen.</span></span>  <span data-ttu-id="a3af9-203">Wenn Sie sich in den meisten Punkten nur an die Eigenschaften des Kompositors halten und die Farbe ganz vermeiden, sollten Sie eine wesentliche Leistungsverbesserung feststellen, sie müssen jedoch auf übermäßig hohe Ebenenanzahl achten.</span><span class="sxs-lookup"><span data-stu-id="a3af9-203">For the most part, if you stick to compositor-only properties and avoid paint altogether, you should notice a major improvement in performance, but you need to watch out for excessive layer counts.</span></span>  <!--Navigate to [Stick to compositor-only properties and manage layer count][WebFundamentalsPerformanceRenderingCompositorOnlyProperties].  -->  

<!--todo: add Stick to compositor-only properties and manage layer count section when available  -->  

### <a name="paint-and-composite-tools"></a><span data-ttu-id="a3af9-204">Paint und zusammengesetzt: Tools</span><span class="sxs-lookup"><span data-stu-id="a3af9-204">Paint and composite: Tools</span></span>  

<span data-ttu-id="a3af9-205">Möchten Sie wissen, wie lange das Malen dauert oder wie oft das Malen stattfindet?</span><span class="sxs-lookup"><span data-stu-id="a3af9-205">Want to know how long painting takes or how often painting occurs?</span></span>  <span data-ttu-id="a3af9-206">Überprüfen Sie [die Einstellung Erweiterte Farbinstrumentierung aktivieren][DevtoolsChromiumEvaluatePerformanceReferenceEnableadvancedpaintinstrumentation] im Bereich **Leistung,** und nehmen Sie dann eine Aufzeichnung vor.</span><span class="sxs-lookup"><span data-stu-id="a3af9-206">Check the [Enable advanced paint instrumentation][DevtoolsChromiumEvaluatePerformanceReferenceEnableadvancedpaintinstrumentation] setting in the **Performance** panel and then take a recording.</span></span>  <span data-ttu-id="a3af9-207">Wenn die meiste Renderzeit mit dem Malen verbracht wird, haben Sie Farbprobleme.</span><span class="sxs-lookup"><span data-stu-id="a3af9-207">If most of your rendering time is spent painting, you have paint problems.</span></span>  

<!--
:::image type="complex" source="../media/rendering-tools-jank-performance-advanced-paint-instrumentation-summary.msft.png" alt-text="Long paint times in timeline recording" lightbox="../media/rendering-tools-jank-performance-advanced-paint-instrumentation-summary.msft.png":::
   Long paint times in timeline recording  
:::image-end:::  
-->  

<!--
Check out the **Rendering** panel for further configurations that are able to help you diagnose paint problems.  -->  

<!--todo: link Rendering panel in ../evaluate-performance/timeline-tool  sub-section when live  -->  

### <a name="paint-and-composite-problems"></a><span data-ttu-id="a3af9-208">Paint und zusammengesetzt: Probleme</span><span class="sxs-lookup"><span data-stu-id="a3af9-208">Paint and composite: Problems</span></span>  

<span data-ttu-id="a3af9-209">In der folgenden Tabelle werden einige häufige Farb- und Verbundprobleme sowie mögliche Lösungen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="a3af9-209">The following table describes some common paint and composite problems and potential solutions.</span></span>  

| <span data-ttu-id="a3af9-210">Problem</span><span class="sxs-lookup"><span data-stu-id="a3af9-210">Problem</span></span> | <span data-ttu-id="a3af9-211">Beispiel</span><span class="sxs-lookup"><span data-stu-id="a3af9-211">Example</span></span> | <span data-ttu-id="a3af9-212">Lösung</span><span class="sxs-lookup"><span data-stu-id="a3af9-212">Solution</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="a3af9-213">Paint, die sich auf die Reaktion oder Animation ausdingen.</span><span class="sxs-lookup"><span data-stu-id="a3af9-213">Paint storms affecting response or animation.</span></span>  | <span data-ttu-id="a3af9-214">Große Farbbereiche oder teure Farben, die die Reaktion oder Animation beeinflussen.</span><span class="sxs-lookup"><span data-stu-id="a3af9-214">Big paint areas or expensive paints affecting response or animation.</span></span>  | <span data-ttu-id="a3af9-215">Vermeiden Sie Farbe, fördern Sie Elemente, die sich auf ihre eigene Ebene verschieben, verwenden Sie Transformationen und Deckkraft.</span><span class="sxs-lookup"><span data-stu-id="a3af9-215">Avoid paint, promote elements that are moving to their own layer, use transforms and opacity.</span></span>  <!--Navigate to [Simplify paint complexity and reduce paint areas][WebFundamentalsPerformanceRenderingSimplifyPaintComplexity].  -->  |  
| <span data-ttu-id="a3af9-216">Ebenenexplosionen, die Animationen beeinflussen.</span><span class="sxs-lookup"><span data-stu-id="a3af9-216">Layer explosions affecting animations.</span></span>  | <span data-ttu-id="a3af9-217">Überpromotion von zu vielen Elementen mit `translateZ(0)` erheblichen Auswirkungen auf die Animationsleistung.</span><span class="sxs-lookup"><span data-stu-id="a3af9-217">Overpromotion of too many elements with `translateZ(0)` greatly affects animation performance.</span></span>  | <span data-ttu-id="a3af9-218">Bewerben Sie sich sparsam auf Ebenen, und nur, wenn Sie wissen, dass es greifbare Verbesserungen bietet.</span><span class="sxs-lookup"><span data-stu-id="a3af9-218">Promote to layers sparingly, and only when you know it offers tangible improvements.</span></span>  <!--Navigate to [Stick to composite-only properties and manage layer count][WebFundamentalsPerformanceRenderingCompositorOnlyProperties].  -->  |  

<!--todo: add Simplify paint complexity and reduce paint areas section when available  -->  
<!--todo: add Stick to compositor-only properties and manage layer count section when available  -->  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="a3af9-219">Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen</span><span class="sxs-lookup"><span data-stu-id="a3af9-219">Getting in touch with the Microsoft Edge DevTools team</span></span>  

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
> <span data-ttu-id="a3af9-226">Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a3af9-226">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="a3af9-227">Die ursprüngliche Seite [](https://developers.google.com/web/tools/chrome-devtools/rendering-tools/index) befindet sich hier und wird von [Kayce Basken][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\) und [Meggin Kearney][MegginKearney] \(Tech Writer\) verfasst.</span><span class="sxs-lookup"><span data-stu-id="a3af9-227">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/rendering-tools/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\) and [Meggin Kearney][MegginKearney] \(Tech Writer\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="a3af9-229">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="a3af9-229">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  
[MegginKearney]: https://developers.google.com/web/resources/contributors#meggin-kearney  
