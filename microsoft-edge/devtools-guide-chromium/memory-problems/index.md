---
description: Erfahren Sie, wie Sie Microsoft Edge und DevTools verwenden, um Speicherprobleme zu finden, die sich auf die Seitenleistung auswirken, z. B. Speicherverluste, Speicherbloat und häufige Garbage Collections.
title: Beheben von Speicherproblemen
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, Entwicklungstools
ms.openlocfilehash: afaea8ca561bd975490d9153cda40877786a0f08
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "11397832"
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

# <a name="fix-memory-problems"></a><span data-ttu-id="63a3c-104">Beheben von Speicherproblemen</span><span class="sxs-lookup"><span data-stu-id="63a3c-104">Fix memory problems</span></span>  

<span data-ttu-id="63a3c-105">Erfahren Sie, wie Sie Microsoft Edge und DevTools verwenden, um Speicherprobleme zu finden, die sich auf die Seitenleistung auswirken, z. B. Speicherverluste, Speicherbloat und häufige Garbage Collections.</span><span class="sxs-lookup"><span data-stu-id="63a3c-105">Learn how to use Microsoft Edge and DevTools to find memory issues that affect page performance, including memory leaks, memory bloat, and frequent garbage collections.</span></span>  

### <a name="summary"></a><span data-ttu-id="63a3c-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="63a3c-106">Summary</span></span>  

*   <span data-ttu-id="63a3c-107">Erfahren Sie, wie viel Arbeitsspeicher Ihre Seite derzeit mit dem Microsoft Edge Browser Task Manager verwendet.</span><span class="sxs-lookup"><span data-stu-id="63a3c-107">Find out how much memory your page is currently using with the Microsoft Edge Browser Task Manager.</span></span>  
*   <span data-ttu-id="63a3c-108">Visualisieren Sie die Speichernutzung im Laufe der Zeit mit **dem Speicherbereich.**</span><span class="sxs-lookup"><span data-stu-id="63a3c-108">Visualize memory usage over time with the **Memory** panel.</span></span>  
*   <span data-ttu-id="63a3c-109">Identifizieren von getrennten DOM-Baumstrukturen \(eine häufige Ursache für Speicherverluste\) mit **Heap-Momentaufnahme**.</span><span class="sxs-lookup"><span data-stu-id="63a3c-109">Identify detached DOM trees \(a common cause of memory leaks\) with **Heap snapshot**.</span></span>  
*   <span data-ttu-id="63a3c-110">Erfahren Sie, wann neuer Arbeitsspeicher im JavaScript-Heap \(JS-Heap\) mit **Zuweisungsinstrumentation auf der Zeitachse zugewiesen wird.**</span><span class="sxs-lookup"><span data-stu-id="63a3c-110">Find out when new memory is being allocated in your JavaScript heap \(JS heap\) with **Allocation instrumentation on timeline**.</span></span>  

## <a name="overview"></a><span data-ttu-id="63a3c-111">Übersicht</span><span class="sxs-lookup"><span data-stu-id="63a3c-111">Overview</span></span>  

<span data-ttu-id="63a3c-112">Im Sinne des **RAIL-Leistungsmodells** sollten ihre Benutzer im Mittelpunkt Ihrer Leistungsbemühungen stehen.</span><span class="sxs-lookup"><span data-stu-id="63a3c-112">In the spirit of the **RAIL** performance model, the focus of your performance efforts should be your users.</span></span>  

<!--todo: add RAIL section when available  -->  

<span data-ttu-id="63a3c-113">Speicherprobleme sind wichtig, da sie häufig von Benutzern zu finden sind.</span><span class="sxs-lookup"><span data-stu-id="63a3c-113">Memory issues are important because they are often perceivable by users.</span></span>  <span data-ttu-id="63a3c-114">Benutzer können Speicherprobleme auf folgende Weise wahrnehmen:</span><span class="sxs-lookup"><span data-stu-id="63a3c-114">Users may perceive memory issues in the following ways:</span></span>  

*   <span data-ttu-id="63a3c-115">**Die Leistung einer Seite wird im Laufe der Zeit**immer schlechter.</span><span class="sxs-lookup"><span data-stu-id="63a3c-115">**The performance of a page gets progressively worse over time**.</span></span>  <span data-ttu-id="63a3c-116">Dies ist möglicherweise ein Symptom für einen Speicherverlust.</span><span class="sxs-lookup"><span data-stu-id="63a3c-116">This is possibly a symptom of a memory leak.</span></span>  <span data-ttu-id="63a3c-117">Ein Speicherverlust liegt vor, wenn ein Fehler auf der Seite dazu führt, dass die Seite im Laufe der Zeit immer mehr Arbeitsspeicher verwendet.</span><span class="sxs-lookup"><span data-stu-id="63a3c-117">A memory leak is when a bug in the page causes the page to progressively use more and more memory over time.</span></span>  
*   <span data-ttu-id="63a3c-118">**Die Leistung einer Seite ist konstant schlecht.**</span><span class="sxs-lookup"><span data-stu-id="63a3c-118">**The performance of a page is consistently bad**.</span></span>  <span data-ttu-id="63a3c-119">Dies ist möglicherweise ein Symptom der Speicherbloat.</span><span class="sxs-lookup"><span data-stu-id="63a3c-119">This is possibly a symptom of memory bloat.</span></span>  <span data-ttu-id="63a3c-120">Der Arbeitsspeicher wird aufgebläht, wenn eine Seite mehr Arbeitsspeicher verbraucht, als für eine optimale Seitengeschwindigkeit erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="63a3c-120">Memory bloat is when a page uses more memory than is necessary for optimal page speed.</span></span>  
*   <span data-ttu-id="63a3c-121">**Die Leistung einer Seite wird verzögert oder scheint häufig anzuhalten.**</span><span class="sxs-lookup"><span data-stu-id="63a3c-121">**The performance of a page is delayed or appears to pause frequently**.</span></span>  <span data-ttu-id="63a3c-122">Dies ist möglicherweise ein Symptom für häufige Garbage Collections.</span><span class="sxs-lookup"><span data-stu-id="63a3c-122">This is possibly a symptom of frequent garbage collections.</span></span>  <span data-ttu-id="63a3c-123">Die Garbage Collection wird beim Freigeben des Arbeitsspeichers durch den Browser verwendet.</span><span class="sxs-lookup"><span data-stu-id="63a3c-123">Garbage collection is when the browser reclaims memory.</span></span>  <span data-ttu-id="63a3c-124">Der Browser entscheidet, wann dies geschieht.</span><span class="sxs-lookup"><span data-stu-id="63a3c-124">The browser decides when this happens.</span></span>  <span data-ttu-id="63a3c-125">Während der Auflistungen werden alle ausgeführten Skripts angehalten.</span><span class="sxs-lookup"><span data-stu-id="63a3c-125">During collections, all script running is paused.</span></span>  <span data-ttu-id="63a3c-126">Wenn der Browser also sehr viel Garbage Collection sammelt, wird die Skriptlaufzeit viel angehalten.</span><span class="sxs-lookup"><span data-stu-id="63a3c-126">So if the browser is garbage collecting a lot, script runtime is going to get paused a lot.</span></span>  

### <a name="memory-bloat-how-much-is-too-much"></a><span data-ttu-id="63a3c-127">Speicherbloat: Wie viel ist "zu viel"?</span><span class="sxs-lookup"><span data-stu-id="63a3c-127">Memory bloat: how much is "too much"?</span></span>  

<span data-ttu-id="63a3c-128">Ein Speicherverlust ist einfach zu definieren.</span><span class="sxs-lookup"><span data-stu-id="63a3c-128">A memory leak is easy to define.</span></span>  <span data-ttu-id="63a3c-129">Wenn eine Website zunehmend mehr Arbeitsspeicher verwendet, liegt ein Leck vor.</span><span class="sxs-lookup"><span data-stu-id="63a3c-129">If a site is progressively using more and more memory, then you have a leak.</span></span>  <span data-ttu-id="63a3c-130">Der Speicherbloat ist jedoch etwas schwieriger zu anheften.</span><span class="sxs-lookup"><span data-stu-id="63a3c-130">But memory bloat is a bit harder to pin down.</span></span>  <span data-ttu-id="63a3c-131">Was gilt als "Zu viel Arbeitsspeicher" verwenden?</span><span class="sxs-lookup"><span data-stu-id="63a3c-131">What qualifies as "using too much memory"?</span></span>  

<span data-ttu-id="63a3c-132">Es gibt hier keine schwierigen Zahlen, da unterschiedliche Geräte und Browser unterschiedliche Funktionen haben.</span><span class="sxs-lookup"><span data-stu-id="63a3c-132">There are no hard numbers here, because different devices and browsers have different capabilities.</span></span>  <span data-ttu-id="63a3c-133">Dieselbe Seite, die reibungslos auf einem High-End-Smartphone ausgeführt wird, kann auf einem Low-End-Smartphone abstürzen.</span><span class="sxs-lookup"><span data-stu-id="63a3c-133">The same page that runs smoothly on a high-end smartphone may crash on a low-end smartphone.</span></span>  

<span data-ttu-id="63a3c-134">Der Schlüssel hier ist, das RAIL-Modell zu verwenden und sich auf Ihre Benutzer zu konzentrieren.</span><span class="sxs-lookup"><span data-stu-id="63a3c-134">The key here is to use the RAIL model and focus on your users.</span></span>  <span data-ttu-id="63a3c-135">Erfahren Sie, welche Geräte bei Ihren Benutzern beliebt sind, und testen Sie dann Ihre Seite auf diesen Geräten.</span><span class="sxs-lookup"><span data-stu-id="63a3c-135">Find out what devices are popular with your users, and then test out your page on those devices.</span></span>  <span data-ttu-id="63a3c-136">Wenn die Erfahrung konsistent schlecht ist, übersteigt die Seite möglicherweise die Speicherfunktionen dieser Geräte.</span><span class="sxs-lookup"><span data-stu-id="63a3c-136">If the experience is consistently bad, the page may be exceeding the memory capabilities of those devices.</span></span>  

## <a name="monitor-memory-use-in-realtime-with-the-microsoft-edge-browser-task-manager"></a><span data-ttu-id="63a3c-137">Überwachen der Arbeitsspeichernutzung in Echtzeit mit dem Microsoft Edge Browser Task Manager</span><span class="sxs-lookup"><span data-stu-id="63a3c-137">Monitor memory use in realtime with the Microsoft Edge Browser Task Manager</span></span>  

<span data-ttu-id="63a3c-138">Verwenden Sie den Microsoft Edge Browser Task Manager als Ausgangspunkt für ihre Speicherproblemuntersuchung.</span><span class="sxs-lookup"><span data-stu-id="63a3c-138">Use the Microsoft Edge Browser Task Manager as a starting point to your memory issue investigation.</span></span>  <span data-ttu-id="63a3c-139">Der Microsoft Edge Browser Task Manager ist ein Echtzeitmonitor, der Ihnen mitteilt, wie viel Arbeitsspeicher eine Seite derzeit verwendet.</span><span class="sxs-lookup"><span data-stu-id="63a3c-139">The Microsoft Edge Browser Task Manager is a realtime monitor that tells you how much memory a page is currently using.</span></span>  

1.  <span data-ttu-id="63a3c-140">Wählen `Shift` + `Esc` Oder navigieren Sie zum Hauptmenü von Microsoft Edge, und wählen Sie **Weitere Tools**Browser Task Manager aus, um  >   den Microsoft Edge Browser Task Manager zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="63a3c-140">Select `Shift`+`Esc` or navigate to the Microsoft Edge main menu and choose **More tools** > **Browser Task Manager** to open the Microsoft Edge Browser Task Manager.</span></span>  
    
    :::image type="complex" source="../media/memory-problems-bing-settings-more-tools-browser-task-manager.msft.png" alt-text="Öffnen des Microsoft Edge-Browser-Task-Managers" lightbox="../media/memory-problems-bing-settings-more-tools-browser-task-manager.msft.png":::
       <span data-ttu-id="63a3c-142">Abbildung 1: Öffnen des Microsoft Edge-Browser-Task-Managers</span><span class="sxs-lookup"><span data-stu-id="63a3c-142">Figure 1:  Opening the Microsoft Edge Browser Task Manager</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="63a3c-143">Zeigen Sie auf die Tabellenkopfzeile des Microsoft Edge-Browser-Task-Managers, öffnen Sie das Kontextmenü \(mit der rechten Maustaste\), und aktivieren Sie **den JavaScript-Speicher.**</span><span class="sxs-lookup"><span data-stu-id="63a3c-143">Hover on the table header of the Microsoft Edge Browser Task Manager, open the contextual menu \(right-click\), and enable **JavaScript memory**.</span></span>  
    
    :::image type="complex" source="../media/memory-problems-bing-browser-task-manager-javascript-memory.msft.png" alt-text="Aktivieren des JavaScript-Speichers" lightbox="../media/memory-problems-bing-browser-task-manager-javascript-memory.msft.png":::
       <span data-ttu-id="63a3c-145">Abbildung 2: Aktivieren des JavaScript-Speichers</span><span class="sxs-lookup"><span data-stu-id="63a3c-145">Figure 2:  Enable JavaScript memory</span></span>  
    :::image-end:::  
    
<span data-ttu-id="63a3c-146">Diese beiden Spalten geben Ihnen unterschiedliche Informationen dazu, wie Ihre Seite Arbeitsspeicher verwendet.</span><span class="sxs-lookup"><span data-stu-id="63a3c-146">These two columns tell you different things about how your page is using memory.</span></span>  

*   <span data-ttu-id="63a3c-147">Die **Spalte Arbeitsspeicher** stellt systemeigenen Arbeitsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="63a3c-147">The **Memory** column represents native memory.</span></span>  <span data-ttu-id="63a3c-148">DOM-Knoten werden im systemeigenen Speicher gespeichert.</span><span class="sxs-lookup"><span data-stu-id="63a3c-148">DOM nodes are stored in native memory.</span></span>  <span data-ttu-id="63a3c-149">Wenn dieser Wert zunimmt, werden DOM-Knoten erstellt.</span><span class="sxs-lookup"><span data-stu-id="63a3c-149">If this value is increasing, DOM nodes are getting created.</span></span>  
*   <span data-ttu-id="63a3c-150">Die **Spalte JavaScript Memory** stellt den JS-Heap dar.</span><span class="sxs-lookup"><span data-stu-id="63a3c-150">The **JavaScript Memory** column represents the JS heap.</span></span>  <span data-ttu-id="63a3c-151">Diese Spalte enthält zwei Werte.</span><span class="sxs-lookup"><span data-stu-id="63a3c-151">This column contains two values.</span></span>  <span data-ttu-id="63a3c-152">Der Wert, an dem Sie interessiert sind, ist die Livenummer \(die Zahl in Klammern\).</span><span class="sxs-lookup"><span data-stu-id="63a3c-152">The value you are interested in is the live number \(the number in parentheses\).</span></span>  <span data-ttu-id="63a3c-153">Die Livenummer gibt an, wie viel Arbeitsspeicher die erreichbaren Objekte auf Ihrer Seite verwenden.</span><span class="sxs-lookup"><span data-stu-id="63a3c-153">The live number represents how much memory the reachable objects on your page are using.</span></span>  <span data-ttu-id="63a3c-154">Wenn diese Anzahl zunimmt, werden entweder neue Objekte erstellt, oder die vorhandenen Objekte werden größer.</span><span class="sxs-lookup"><span data-stu-id="63a3c-154">If this number is increasing, either new objects are being created, or the existing objects are growing.</span></span>  

<!--*   live number reference: https://groups.google.com/d/msg/google-chrome-developer-tools/aTMVGoNM0VY/bLmf3l2CpJ8J  -->  

## <a name="visualize-memory-leaks-with-performance-panel"></a><span data-ttu-id="63a3c-155">Visualisieren von Speicherverlusten mit dem Leistungsbereich</span><span class="sxs-lookup"><span data-stu-id="63a3c-155">Visualize memory leaks with Performance panel</span></span>  

<span data-ttu-id="63a3c-156">Sie können auch den Bereich "Leistung" als weiteren Ausgangspunkt in Ihrer Untersuchung verwenden.</span><span class="sxs-lookup"><span data-stu-id="63a3c-156">You may also use the Performance panel as another starting point in your investigation.</span></span>  <span data-ttu-id="63a3c-157">Der Bereich Leistung hilft Ihnen, die Speichernutzung einer Seite im Laufe der Zeit zu visualisieren.</span><span class="sxs-lookup"><span data-stu-id="63a3c-157">The Performance panel helps you visualize the memory use of a page over time.</span></span>  

1.  <span data-ttu-id="63a3c-158">Öffnen Sie **den Bereich** Leistung auf DevTools.</span><span class="sxs-lookup"><span data-stu-id="63a3c-158">Open the **Performance** panel on DevTools.</span></span>  
1.  <span data-ttu-id="63a3c-159">Aktivieren Sie **das Kontrollkästchen** Speicher.</span><span class="sxs-lookup"><span data-stu-id="63a3c-159">Enable the **Memory** checkbox.</span></span>  
1.  <span data-ttu-id="63a3c-160">[Nehmen Sie eine Aufzeichnung vor.][DevtoolsEvaluatePerformanceReferenceRecord]</span><span class="sxs-lookup"><span data-stu-id="63a3c-160">[Make a recording][DevtoolsEvaluatePerformanceReferenceRecord].</span></span>  

> [!TIP]
> <span data-ttu-id="63a3c-161">Es ist eine bewährte Methode, ihre Aufzeichnung mit einer erzwungenen Garbage Collection zu starten und zu beenden.</span><span class="sxs-lookup"><span data-stu-id="63a3c-161">It is a good practice to start and end your recording with a forced garbage collection.</span></span>  <span data-ttu-id="63a3c-162">Um die Garbage Collection zu erzwingen, wählen **Sie** während der Aufzeichnung die Schaltfläche Garbage Force Garbage Collection ![ sammeln ][ImageForceGarbageCollectionIcon] aus.</span><span class="sxs-lookup"><span data-stu-id="63a3c-162">To force garbage collection, choose the **collect garbage** ![force garbage collection][ImageForceGarbageCollectionIcon] button while recording.</span></span>  

<span data-ttu-id="63a3c-163">Um Speicheraufzeichnungen zu veranschaulichen, berücksichtigen Sie den folgenden Code:</span><span class="sxs-lookup"><span data-stu-id="63a3c-163">To demonstrate memory recordings, consider the code below:</span></span>  

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

<span data-ttu-id="63a3c-164">Jedes Mal, wenn die Schaltfläche ausgewählt wird, auf die im Code verwiesen wird, werden zehntausend Knoten an den Dokumenttext angefügt, und eine Zeichenfolge von einer Million Zeichen wird auf das `div` `x` Array `x` gedrückt.</span><span class="sxs-lookup"><span data-stu-id="63a3c-164">Every time that the button referenced in the code is chosen, ten thousand `div` nodes are appended to the document body, and a string of one million `x` characters is pushed onto the `x` array.</span></span>  <span data-ttu-id="63a3c-165">Beim Ausführen des vorherigen Codebeispiels wird eine Aufzeichnung im **Leistungsbereich** wie in der folgenden Abbildung erstellt.</span><span class="sxs-lookup"><span data-stu-id="63a3c-165">Running the previous code sample produces a recording in the **Performance** panel like the following figure.</span></span>  

:::image type="complex" source="../media/memory-problems-glitch-example-1-performance-memory.msft.png" alt-text="Einfaches Wachstum" lightbox="../media/memory-problems-glitch-example-1-performance-memory.msft.png":::
   <span data-ttu-id="63a3c-167">Abbildung 3: Einfaches Wachstum</span><span class="sxs-lookup"><span data-stu-id="63a3c-167">Figure 3:  Simple growth</span></span>  
:::image-end:::  

<span data-ttu-id="63a3c-168">Zunächst eine Erläuterung der Benutzeroberfläche.</span><span class="sxs-lookup"><span data-stu-id="63a3c-168">First, an explanation of the user interface.</span></span>  <span data-ttu-id="63a3c-169">Das **HEAP-Diagramm** im **Übersichtsbereich** \(unter **NET**\) stellt den JS-Heap dar.</span><span class="sxs-lookup"><span data-stu-id="63a3c-169">The **HEAP** graph in the **Overview** pane \(below **NET**\) represents the JS heap.</span></span>  <span data-ttu-id="63a3c-170">Unterhalb des **Bereichs Übersicht** befindet sich der **Bereich Counter.**</span><span class="sxs-lookup"><span data-stu-id="63a3c-170">Below the **Overview** pane is the **Counter** pane.</span></span>  <span data-ttu-id="63a3c-171">Die Speicherauslastung wird nach JS-Heap \(identisch  mit **HEAP-Diagramm** im Übersichtsbereich\), Dokumenten, DOM-Knoten, Listenern und GPU-Speicher aufgeschlüsselt.</span><span class="sxs-lookup"><span data-stu-id="63a3c-171">The memory usage is broken down by JS heap \(same as **HEAP** graph in the **Overview** pane\), documents, DOM nodes, listeners, and GPU memory.</span></span>  <span data-ttu-id="63a3c-172">Deaktivieren Sie ein Kontrollkästchen, um es aus dem Diagramm auszublenden.</span><span class="sxs-lookup"><span data-stu-id="63a3c-172">Turn off a checkbox to hide it from the graph.</span></span>  

<span data-ttu-id="63a3c-173">Nun eine Analyse des Codes im Vergleich zur vorherigen Abbildung.</span><span class="sxs-lookup"><span data-stu-id="63a3c-173">Now, an analysis of the code compared with the previous figure.</span></span>  <span data-ttu-id="63a3c-174">Wenn Sie den Knotenzähler \(das grüne Diagramm\) überprüfen, wird er mit dem Code sauber nachgeschlagen.</span><span class="sxs-lookup"><span data-stu-id="63a3c-174">If you review the node counter \(the green graph\), it matches up cleanly with the code.</span></span>  <span data-ttu-id="63a3c-175">Die Knotenanzahl nimmt in separaten Schritten zu.</span><span class="sxs-lookup"><span data-stu-id="63a3c-175">The node count increases in discrete steps.</span></span>  <span data-ttu-id="63a3c-176">Sie können davon ausgehen, dass jede Erhöhung der Knotenanzahl ein Aufruf von `grow()` ist.</span><span class="sxs-lookup"><span data-stu-id="63a3c-176">You may presume that each increase in the node count is a call to `grow()`.</span></span>  <span data-ttu-id="63a3c-177">Das JS-Heapdiagramm \(das blaue Diagramm\) ist nicht so einfach.</span><span class="sxs-lookup"><span data-stu-id="63a3c-177">The JS heap graph \(the blue graph\) is not as straightforward.</span></span>  <span data-ttu-id="63a3c-178">In Einklang mit bewährten Methoden ist der erste Dip  tatsächlich eine erzwungene Garbage Collection \(Wählen Sie die Schaltfläche Garbage ![ Force Garbage Collection ][ImageForceGarbageCollectionIcon] sammeln\).</span><span class="sxs-lookup"><span data-stu-id="63a3c-178">In keeping with best practices, the first dip is actually a forced garbage collection \(choose the  **collect garbage** ![force garbage collection][ImageForceGarbageCollectionIcon] button\).</span></span>  <span data-ttu-id="63a3c-179">Im Verlauf der Aufzeichnung werden die Spikes der JS-Heapgröße angezeigt.</span><span class="sxs-lookup"><span data-stu-id="63a3c-179">As the recording progresses, the JS heap size spikes are displayed.</span></span>  <span data-ttu-id="63a3c-180">Dies ist natürlich und erwartet: Der JavaScript-Code erstellt die DOM-Knoten auf jeder schaltfläche, die Sie auswählen, und macht viel Arbeit, wenn die Zeichenfolge von einer Million Zeichen erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="63a3c-180">This is natural and expected:  the JavaScript code is creating the DOM nodes on every button you choose and doing a lot of work when it creates the string of one million characters.</span></span>  <span data-ttu-id="63a3c-181">Der Schlüssel hier ist die Tatsache, dass der JS-Heap höher endet, als er begonnen hat \(der "Anfang" hier ist der Punkt nach der erzwungenen Garbage Collection\).</span><span class="sxs-lookup"><span data-stu-id="63a3c-181">The key thing here is the fact that the JS heap ends higher than it began \(the "beginning" here being the point after the forced garbage collection\).</span></span>  <span data-ttu-id="63a3c-182">Wenn Sie in der realen Welt dieses Muster der Zunehmenden Größe des JS-Heaps oder der Knotengröße gesehen haben, kann dies potenziell einen Speicherverlust definieren.</span><span class="sxs-lookup"><span data-stu-id="63a3c-182">In the real world, if you saw this pattern of increasing JS heap size or node size, it may potentially define a memory leak.</span></span>  

<!--todo: the Heap snapshots and Profiles panel are not found in Edge  -->  

## <a name="discover-detached-dom-tree-memory-leaks-with-heap-snapshots"></a><span data-ttu-id="63a3c-183">Ermitteln getrennter Speicherverluste der DOM-Struktur mit Heap-Momentaufnahmen</span><span class="sxs-lookup"><span data-stu-id="63a3c-183">Discover detached DOM tree memory leaks with Heap Snapshots</span></span>  

<span data-ttu-id="63a3c-184">Ein DOM-Knoten wird nur dann gesammelt, wenn es keine Verweise auf den Knoten aus der DOM-Struktur oder dem JavaScript-Code gibt, der auf der Seite ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="63a3c-184">A DOM node is only garbage collected when there are no references to the node from either the DOM tree or JavaScript code running on the page.</span></span>  <span data-ttu-id="63a3c-185">Ein Knoten wird als "getrennt" bezeichnet, wenn er aus der DOM-Struktur entfernt wird, aber einige JavaScript-Elemente verweisen weiterhin auf ihn.</span><span class="sxs-lookup"><span data-stu-id="63a3c-185">A node is said to be "detached" when it is removed from the DOM tree but some JavaScript still references it.</span></span>  <span data-ttu-id="63a3c-186">Getrennte DOM-Knoten sind eine häufige Ursache für Speicherverluste.</span><span class="sxs-lookup"><span data-stu-id="63a3c-186">Detached DOM nodes are a common cause of memory leaks.</span></span>  <span data-ttu-id="63a3c-187">In diesem Abschnitt erfahren Sie, wie Sie die Heapprofiler in DevTools verwenden, um getrennte Knoten zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="63a3c-187">This section teaches you how to use the heap profilers in DevTools to identify detached nodes.</span></span>  

<span data-ttu-id="63a3c-188">Hier ist ein einfaches Beispiel für getrennte DOM-Knoten.</span><span class="sxs-lookup"><span data-stu-id="63a3c-188">Here is a simple example of detached DOM nodes.</span></span>  

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

<span data-ttu-id="63a3c-189">Wenn Sie die Schaltfläche auswählen, auf die im Code verwiesen wird, wird `ul` ein Knoten mit zehn untergingen Knoten `li` erstellt.</span><span class="sxs-lookup"><span data-stu-id="63a3c-189">Choosing the button referenced in the code creates a `ul` node with ten `li` children.</span></span>  <span data-ttu-id="63a3c-190">Auf die Knoten wird durch den Code verwiesen, sie sind jedoch nicht in der DOM-Struktur vorhanden, sodass jede getrennt ist.</span><span class="sxs-lookup"><span data-stu-id="63a3c-190">The nodes are referenced by the code but do not exist in the DOM tree, so each is detached.</span></span>  

<span data-ttu-id="63a3c-191">Heapmomentaufnahmen sind eine Möglichkeit, getrennte Knoten zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="63a3c-191">Heap snapshots are one way to identify detached nodes.</span></span>  <span data-ttu-id="63a3c-192">Wie der Name schon sagt, zeigen Heapmomentaufnahmen, wie der Arbeitsspeicher zum Zeitpunkt der Momentaufnahme auf die JS-Objekte und DOM-Knoten für Ihre Seite verteilt wird.</span><span class="sxs-lookup"><span data-stu-id="63a3c-192">As the name implies, heap snapshots show you how memory is distributed among the JS objects and DOM nodes for your page at the point of time of the snapshot.</span></span>  

<span data-ttu-id="63a3c-193">Um eine Momentaufnahme zu erstellen,  öffnen Sie DevTools, und navigieren Sie zum Speicherbereich, wählen Sie das Optionsfeld Heap-Momentaufnahme aus, > **Momentaufnahme erstellen.** </span><span class="sxs-lookup"><span data-stu-id="63a3c-193">To create a snapshot, open DevTools and navigate to the **Memory** panel, choose the **Heap snapshot** radio button > **Take snapshot** button.</span></span>  

:::image type="complex" source="../media/memory-problems-glitch-example-12-memory-heap-snapshot.msft.png" alt-text="Erstellen einer Heapmomentaufnahme" lightbox="../media/memory-problems-glitch-example-12-memory-heap-snapshot.msft.png":::
   <span data-ttu-id="63a3c-195">Abbildung 4: Erstellen einer Heapmomentaufnahme</span><span class="sxs-lookup"><span data-stu-id="63a3c-195">Figure 4:  Take heap snapshot</span></span>  
:::image-end:::  

<span data-ttu-id="63a3c-196">Die Momentaufnahme kann einige Zeit zum Verarbeiten und Laden dauern.</span><span class="sxs-lookup"><span data-stu-id="63a3c-196">The snapshot may take some time to process and load.</span></span>  <span data-ttu-id="63a3c-197">Nachdem sie abgeschlossen ist, wählen Sie sie im linken Bereich \(benannte **HEAP-MOMENTAUFNAHMEN**\) aus.</span><span class="sxs-lookup"><span data-stu-id="63a3c-197">After it is finished, select it from the left-hand panel \(named **HEAP SNAPSHOTS**\).</span></span>  

<span data-ttu-id="63a3c-198">Geben `Detached` Sie in das Textfeld **Klassenfilter** ein, um nach getrennten DOM-Baumstrukturen zu suchen.</span><span class="sxs-lookup"><span data-stu-id="63a3c-198">Type `Detached` in the **Class filter** textbox to search for detached DOM trees.</span></span>  

:::image type="complex" source="../media/memory-problems-glitch-example-12-memory-heap-snapshot-filter-detached.msft.png" alt-text="Filtern nach getrennten Knoten" lightbox="../media/memory-problems-glitch-example-12-memory-heap-snapshot-filter-detached.msft.png":::
   <span data-ttu-id="63a3c-200">Abbildung 5: Filtern nach getrennten Knoten</span><span class="sxs-lookup"><span data-stu-id="63a3c-200">Figure 5:  Filtering for detached nodes</span></span>  
:::image-end:::  

<span data-ttu-id="63a3c-201">Erweitern Sie die Karate, um eine getrennte Struktur zu untersuchen.</span><span class="sxs-lookup"><span data-stu-id="63a3c-201">Expand the carats to investigate a detached tree.</span></span>  

:::image type="complex" source="../media/memory-problems-glitch-example-12-memory-heap-snapshot-filter-detached-expanded.msft.png" alt-text="Untersuchen der getrennten Struktur" lightbox="../media/memory-problems-glitch-example-12-memory-heap-snapshot-filter-detached-expanded.msft.png":::
   <span data-ttu-id="63a3c-203">Abbildung 6: Untersuchen der getrennten Struktur</span><span class="sxs-lookup"><span data-stu-id="63a3c-203">Figure 6:  Investigating detached tree</span></span>  
:::image-end:::  

<!--Nodes highlighted yellow have direct references to them from the JavaScript code.  Nodes highlighted red do not have direct references.  They are only alive because they are part of the tree for the yellow node.  In general, you want to focus on the yellow nodes.  Fix your code so that the yellow node is not alive for longer than it needs to be, and you also get rid of the red nodes that are part of the tree for the yellow node.  -->

<span data-ttu-id="63a3c-204">Wählen Sie einen Knoten aus, um ihn weiter zu untersuchen.</span><span class="sxs-lookup"><span data-stu-id="63a3c-204">Choose a node to investigate it further.</span></span>  <span data-ttu-id="63a3c-205">Im Bereich **Objekte** können Sie weitere Informationen zu dem Code überprüfen, auf den sie verweisen.</span><span class="sxs-lookup"><span data-stu-id="63a3c-205">In the **Objects** pane, you may review more information about the code that is referencing it.</span></span>  <span data-ttu-id="63a3c-206">In der folgenden Abbildung bezieht sich die Variable `detachedNodes` beispielsweise auf den Knoten.</span><span class="sxs-lookup"><span data-stu-id="63a3c-206">For example, in the following figure, the `detachedNodes` variable is referencing the node.</span></span>  <span data-ttu-id="63a3c-207">Zum Beheben des speicherlecks sollten Sie den Code untersuchen, der die Variable verwendet, und sicherstellen, dass der Verweis auf den Knoten entfernt wird, wenn er `detachedUNode` nicht mehr benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="63a3c-207">To fix the particular memory leak, you should study the code that uses the `detachedUNode` variable and ensure that the reference to the node is removed when it is no longer needed.</span></span>  

:::image type="complex" source="../media/memory-problems-glitch-example-12-memory-heap-snapshot-filter-detached-expanded-selected.msft.png" alt-text="Untersuchen eines Knotens" lightbox="../media/memory-problems-glitch-example-12-memory-heap-snapshot-filter-detached-expanded-selected.msft.png":::
   <span data-ttu-id="63a3c-209">Abbildung 7: Untersuchen eines Knotens</span><span class="sxs-lookup"><span data-stu-id="63a3c-209">Figure 7:  Investigating a node</span></span>  
:::image-end:::  

<!--todo: the allocation timeline does not appear in the DevTools in Edge  -->  

## <a name="identify-js-heap-memory-leaks-with-allocation-instrumentation-on-timeline"></a><span data-ttu-id="63a3c-210">Identifizieren von JS-Heapspeicherlecks mit Zuweisungsinstrumentation auf der Zeitachse</span><span class="sxs-lookup"><span data-stu-id="63a3c-210">Identify JS heap memory leaks with Allocation instrumentation on timeline</span></span>  

<span data-ttu-id="63a3c-211">**Die Zuordnungsinstrumentation auf der Zeitachse** ist ein weiteres Tool, mit dem Sie Speicherverluste im JS-Heap nachverfolgen können.</span><span class="sxs-lookup"><span data-stu-id="63a3c-211">**Allocation instrumentation on timeline** is another tool that may help you track down memory leaks in your JS heap.</span></span>  

<span data-ttu-id="63a3c-212">Demonstrieren **Sie die Zuordnungsinstrumentation auf der Zeitachse**  mithilfe des folgenden Codes.</span><span class="sxs-lookup"><span data-stu-id="63a3c-212">Demonstrate **Allocation instrumentation on timeline**  using the following code.</span></span>  

```javascript
var x = [];
function grow() {
    x.push(new Array(1000000).join('x'));
}
document.getElementById('grow').addEventListener('click', grow);
```  

<span data-ttu-id="63a3c-213">Jedes Mal, wenn die Schaltfläche, auf die im Code verwiesen wird, gedrückt wird, wird dem Array eine Zeichenfolge von einer Million Zeichen `x` hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="63a3c-213">Every time that the button referenced in the code is pushed, a string of one million characters is added to the `x` array.</span></span>  

<span data-ttu-id="63a3c-214">Wenn Sie eine Zuordnungsinstrumentation auf der Zeitachse aufzeichnen möchten, öffnen Sie DevTools, navigieren Sie zum Speicherbereich, wählen Sie die Option **Zuordnungsinstrumentation** auf der Zeitachse aus, klicken Sie auf die **Schaltfläche Start,** führen Sie die Aktion aus, von der Sie vermuten, dass der Speicherverlust verursacht wird, und wählen Sie dann die Schaltfläche Aufzeichnungsstopp des Heapprofils beenden aus, sobald Sie fertig   ![ ][ImageStopRecordingIcon] sind.</span><span class="sxs-lookup"><span data-stu-id="63a3c-214">To record an Allocation instrumentation on timeline, open DevTools, navigate to the **Memory** panel, choose the **Allocation instrumentation on timeline** radio button, choose the **Start** button, perform the action that you suspect is causing the memory leak, and then choose the **Stop recording heap profile** ![stop recording][ImageStopRecordingIcon] button when you are done.</span></span>  

<span data-ttu-id="63a3c-215">Beachten Sie bei der Aufzeichnung, ob blaue Balken auf der Zuordnungsinstrumentation auf der Zeitachse angezeigt werden, wie in der folgenden Abbildung dargestellt.</span><span class="sxs-lookup"><span data-stu-id="63a3c-215">As you are recording, notice if any blue bars show up on the Allocation instrumentation on timeline, like in the following figure.</span></span>  

:::image type="complex" source="../media/memory-problems-glitch-example-13-allocation-timeline-snapshot-all.msft.png" alt-text="Neue Zuordnungen" lightbox="../media/memory-problems-glitch-example-13-allocation-timeline-snapshot-all.msft.png":::
   <span data-ttu-id="63a3c-217">Abbildung 8: Neue Zuordnungen</span><span class="sxs-lookup"><span data-stu-id="63a3c-217">Figure 8:  New allocations</span></span>  
:::image-end:::  

<span data-ttu-id="63a3c-218">Diese blauen Balken stellen neue Speicherzuweisungen dar.</span><span class="sxs-lookup"><span data-stu-id="63a3c-218">Those blue bars represent new memory allocations.</span></span>  <span data-ttu-id="63a3c-219">Diese neuen Speicherzuweisungen sind Ihre Kandidaten für Speicherverluste.</span><span class="sxs-lookup"><span data-stu-id="63a3c-219">Those new memory allocations are your candidates for memory leaks.</span></span>  <span data-ttu-id="63a3c-220">Sie können eine Leiste vergrößern,  um den Konstruktorbereich so zu filtern, dass nur Objekte angezeigt werden, die während des angegebenen Zeitrahmens zugewiesen wurden.</span><span class="sxs-lookup"><span data-stu-id="63a3c-220">You are able to zoom on a bar to filter the **Constructor** pane to only show objects that were allocated during the specified timeframe.</span></span>  

:::image type="complex" source="../media/memory-problems-glitch-example-13-allocation-timeline-snapshot-focused.msft.png" alt-text="Zeitachse für die verkleinerte Zuweisung" lightbox="../media/memory-problems-glitch-example-13-allocation-timeline-snapshot-focused.msft.png":::
   <span data-ttu-id="63a3c-222">Abbildung 9: Zeitachse der verkleinerten Zuweisung</span><span class="sxs-lookup"><span data-stu-id="63a3c-222">Figure 9:  Zoomed allocation timeline</span></span>  
:::image-end:::  

<span data-ttu-id="63a3c-223">Erweitern Sie das Objekt, und wählen Sie den Wert aus, um weitere Details im **Objektbereich anzuzeigen.**</span><span class="sxs-lookup"><span data-stu-id="63a3c-223">Expand the object and select the value to view more details in the **Object** pane.</span></span>  <span data-ttu-id="63a3c-224">In der folgenden Abbildung wird beispielsweise in den Details des neu zugeordneten Objekts angegeben, dass es der Variablen im `x` Bereich zugeordnet `Window` wurde.</span><span class="sxs-lookup"><span data-stu-id="63a3c-224">For example, in the following figure, in the details of the newly allocated object indicates that it was allocated to the `x` variable in the `Window` scope.</span></span>  

:::image type="complex" source="../media/memory-problems-glitch-example-13-allocation-timeline-snapshot-focused-constructor-expanded.msft.png" alt-text="Objektdetails" lightbox="../media/memory-problems-glitch-example-13-allocation-timeline-snapshot-focused-constructor-expanded.msft.png":::
   <span data-ttu-id="63a3c-226">Abbildung 10: Objektdetails</span><span class="sxs-lookup"><span data-stu-id="63a3c-226">Figure 10:  Object details</span></span>  
:::image-end:::  

## <a name="investigate-memory-allocation-by-function"></a><span data-ttu-id="63a3c-227">Untersuchen der Speicherzuweisung nach Funktion</span><span class="sxs-lookup"><span data-stu-id="63a3c-227">Investigate memory allocation by function</span></span>  

<span data-ttu-id="63a3c-228">Verwenden Sie den **Zuweisungsstichprobeprofiltyp,** um die Speicherzuweisung nach JavaScript-Funktion anzeigen zu können.</span><span class="sxs-lookup"><span data-stu-id="63a3c-228">Use the **Allocation sampling** profiling type to view memory allocation by JavaScript function.</span></span>  

:::image type="complex" source="../media/memory-problems-glitch-example-05-memory-allocation-sampling.msft.png" alt-text="Sampling der Datensatzzuweisung" lightbox="../media/memory-problems-glitch-example-05-memory-allocation-sampling.msft.png":::
   <span data-ttu-id="63a3c-230">Abbildung 11: Sampling der Datensatzzuweisung</span><span class="sxs-lookup"><span data-stu-id="63a3c-230">Figure 11:  Record Allocation sampling</span></span>  
:::image-end:::  

1.  <span data-ttu-id="63a3c-231">Wählen Sie das **Optionsfeld Zuweisungsstichprobe** aus.</span><span class="sxs-lookup"><span data-stu-id="63a3c-231">Choose the **Allocation sampling** radio button.</span></span>  <span data-ttu-id="63a3c-232">Wenn sich auf der Seite ein Mitarbeiter befindet, können Sie dies über das Dropdownmenü neben der Schaltfläche Start als **Profilerstellungsziel** auswählen.</span><span class="sxs-lookup"><span data-stu-id="63a3c-232">If there is a worker on the page, you are able to select that as the profiling target using the dropdown menu next to the **Start** button.</span></span>  
1.  <span data-ttu-id="63a3c-233">Wählen Sie die **Schaltfläche Start** aus.</span><span class="sxs-lookup"><span data-stu-id="63a3c-233">Choose the **Start** button.</span></span>  
1.  <span data-ttu-id="63a3c-234">Führen Sie die Aktionen auf der Webseite aus, die Sie untersuchen möchten.</span><span class="sxs-lookup"><span data-stu-id="63a3c-234">Complete the actions on the webpage which you want to investigate.</span></span>  
1.  <span data-ttu-id="63a3c-235">Wählen Sie **die Schaltfläche** Beenden aus, wenn Sie alle Aktionen abgeschlossen haben.</span><span class="sxs-lookup"><span data-stu-id="63a3c-235">Choose the **Stop** button when you have finished all of your actions.</span></span>  

<span data-ttu-id="63a3c-236">DevTools zeigt eine Aufschlüsselung der Speicherzuweisung nach Funktion.</span><span class="sxs-lookup"><span data-stu-id="63a3c-236">DevTools shows you a breakdown of memory allocation by function.</span></span>  <span data-ttu-id="63a3c-237">Die Standardansicht ist **Heavy (Bottom Up),** die die Funktionen anzeigt, die den größten Arbeitsspeicher oben zugewiesen haben.</span><span class="sxs-lookup"><span data-stu-id="63a3c-237">The default view is **Heavy (Bottom Up)**, which displays the functions that allocated the most memory at the top.</span></span>  

:::image type="complex" source="../media/memory-problems-glitch-example-05-memory-allocation-sampling-heavy-bottom-up.msft.png" alt-text="Zuweisungss sampling" lightbox="../media/memory-problems-glitch-example-05-memory-allocation-sampling-heavy-bottom-up.msft.png":::
   <span data-ttu-id="63a3c-239">Abbildung 12: Zuweisungsstichprobe</span><span class="sxs-lookup"><span data-stu-id="63a3c-239">Figure 12:  Allocation sampling</span></span>  
:::image-end:::  

## <a name="spot-frequent-garbage-collections"></a><span data-ttu-id="63a3c-240">Häufige Garbage Collections erkennen</span><span class="sxs-lookup"><span data-stu-id="63a3c-240">Spot frequent garbage collections</span></span>  

<span data-ttu-id="63a3c-241">Wenn Ihre Seite häufig angehalten wird, können Probleme mit der Garbage Collection auftreten.</span><span class="sxs-lookup"><span data-stu-id="63a3c-241">If your page appears to pause frequently, then you may have garbage collection issues.</span></span>  

<span data-ttu-id="63a3c-242">Sie können entweder den Microsoft Edge Browser Task Manager oder Leistungsspeicheraufzeichnungen verwenden, um häufige Garbage Collection zu erkennen.</span><span class="sxs-lookup"><span data-stu-id="63a3c-242">You are able to use either the Microsoft Edge Browser Task Manager or Performance memory recordings to spot frequent garbage collection.</span></span>  <span data-ttu-id="63a3c-243">Im Microsoft Edge Browser Task Manager stellen häufig steigende und absteigende **Speicher-** oder **JavaScript-Speicherwerte** eine häufige Garbage Collection dar.</span><span class="sxs-lookup"><span data-stu-id="63a3c-243">In the Microsoft Edge Browser Task Manager, frequently rising and falling **Memory** or **JavaScript Memory** values represent frequent garbage collection.</span></span>  <span data-ttu-id="63a3c-244">In Leistungsaufzeichnungen deuten häufige Änderungen \(aufsteigend und fallend\) an den JS-Heap- oder Knotenanzahldiagrammen auf häufige Garbage Collection hin.</span><span class="sxs-lookup"><span data-stu-id="63a3c-244">In Performance recordings, frequent changes \(rising and falling\) to the JS heap or node count graphs indicate frequent garbage collection.</span></span>  

<span data-ttu-id="63a3c-245">Nachdem Sie das Problem erkannt haben,  können Sie eine Allocation-Instrumentierung für die Zeitachsenaufzeichnung verwenden, um herauszufinden, wo Speicher zugewiesen wird und welche Funktionen die Zuweisungen verursachen.</span><span class="sxs-lookup"><span data-stu-id="63a3c-245">After you have identified the problem, you are able to use an **Allocation instrumentation on timeline** recording to find out where memory is being allocated and which functions are causing the allocations.</span></span>  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="63a3c-246">Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen</span><span class="sxs-lookup"><span data-stu-id="63a3c-246">Getting in touch with the Microsoft Edge DevTools team</span></span>  

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
> <span data-ttu-id="63a3c-248">Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="63a3c-248">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="63a3c-249">Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/memory-problems/index) und wird von [Kayce Basken][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\) verfasst.</span><span class="sxs-lookup"><span data-stu-id="63a3c-249">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/memory-problems/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="63a3c-251">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="63a3c-251">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
