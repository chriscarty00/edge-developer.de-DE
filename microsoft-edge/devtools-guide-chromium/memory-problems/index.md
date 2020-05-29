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





# <span data-ttu-id="37857-103">Beheben von Speicherproblemen</span><span class="sxs-lookup"><span data-stu-id="37857-103">Fix Memory Problems</span></span>   



<span data-ttu-id="37857-104">Erfahren Sie, wie Sie Microsoft Edge und DevTools verwenden, um Speicherprobleme zu finden, die sich auf die Seitenleistung auswirken, wie Speicherverluste, aufblasen des Arbeitsspeichers und häufige Garbage Collections.</span><span class="sxs-lookup"><span data-stu-id="37857-104">Learn how to use Microsoft Edge and DevTools to find memory issues that affect page performance, including memory leaks, memory bloat, and frequent garbage collections.</span></span>  

### <span data-ttu-id="37857-105">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="37857-105">Summary</span></span>  

*   <span data-ttu-id="37857-106">Finden Sie heraus, wie viel Arbeitsspeicher Ihre Seite zurzeit mit dem Task-Manager von Microsoft Edge-Browser verwendet.</span><span class="sxs-lookup"><span data-stu-id="37857-106">Find out how much memory your page is currently using with the Microsoft Edge Browser Task Manager.</span></span>  
*   <span data-ttu-id="37857-107">Visualisieren Sie die Speichernutzung im Zeitverlauf mit dem **Speicher** Panel.</span><span class="sxs-lookup"><span data-stu-id="37857-107">Visualize memory usage over time with the **Memory** panel.</span></span>  
*   <span data-ttu-id="37857-108">Identifizieren Sie freigegebene Dom-Bäume \ (eine häufige Ursache für Speicherverluste \) mit **Heap-Snapshots**.</span><span class="sxs-lookup"><span data-stu-id="37857-108">Identify detached DOM trees \(a common cause of memory leaks\) with **Heap snapshot**.</span></span>  
*   <span data-ttu-id="37857-109">Informieren Sie sich, wann der neue Arbeitsspeicher in Ihrem JavaScript-Heap \ (JS-Heap \) mit **Zuordnungs Instrumentation auf Zeitachse**zugewiesen wird.</span><span class="sxs-lookup"><span data-stu-id="37857-109">Find out when new memory is being allocated in your JavaScript heap \(JS heap\) with **Allocation instrumentation on timeline**.</span></span>  

## <span data-ttu-id="37857-110">Übersicht</span><span class="sxs-lookup"><span data-stu-id="37857-110">Overview</span></span>  

<span data-ttu-id="37857-111">Im Sinne des **Rail** -Leistungsmodells sollten Ihre Benutzer den Schwerpunkt ihrer Leistungs Bemühungen haben.</span><span class="sxs-lookup"><span data-stu-id="37857-111">In the spirit of the **RAIL** performance model, the focus of your performance efforts should be your users.</span></span>  

<!--todo: add RAIL section when available  -->  

<span data-ttu-id="37857-112">Speicherprobleme sind wichtig, da Sie für die Benutzer oft wahrnehmbar sind.</span><span class="sxs-lookup"><span data-stu-id="37857-112">Memory issues are important because they are often perceivable by users.</span></span>  <span data-ttu-id="37857-113">Benutzer können Speicherprobleme wie folgt erkennen:</span><span class="sxs-lookup"><span data-stu-id="37857-113">Users may perceive memory issues in the following ways:</span></span>  

*   <span data-ttu-id="37857-114">**Die Leistung einer Seite wird im Laufe der Zeit zunehmend schlechter**.</span><span class="sxs-lookup"><span data-stu-id="37857-114">**The performance of a page gets progressively worse over time**.</span></span>  <span data-ttu-id="37857-115">Dies ist möglicherweise ein Symptom für einen Speicherverlust.</span><span class="sxs-lookup"><span data-stu-id="37857-115">This is possibly a symptom of a memory leak.</span></span>  <span data-ttu-id="37857-116">Ein Speicherverlust ist, wenn ein Fehler auf der Seite dazu führt, dass die Seite zunehmend mehr und mehr Arbeitsspeicher im Laufe der Zeit verwendet.</span><span class="sxs-lookup"><span data-stu-id="37857-116">A memory leak is when a bug in the page causes the page to progressively use more and more memory over time.</span></span>  
*   <span data-ttu-id="37857-117">**Die Leistung einer Seite ist durchwegs schlecht**.</span><span class="sxs-lookup"><span data-stu-id="37857-117">**The performance of a page is consistently bad**.</span></span>  <span data-ttu-id="37857-118">Dies ist möglicherweise ein Symptom des Aufblasens des Arbeitsspeichers.</span><span class="sxs-lookup"><span data-stu-id="37857-118">This is possibly a symptom of memory bloat.</span></span>  <span data-ttu-id="37857-119">Der Arbeitsspeicher wird aufgebläht, wenn eine Seite mehr Arbeitsspeicher benötigt, als für optimale Seiten Geschwindigkeit erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="37857-119">Memory bloat is when a page uses more memory than is necessary for optimal page speed.</span></span>  
*   <span data-ttu-id="37857-120">**Die Leistung einer Seite wird verzögert oder wird häufig angehalten**.</span><span class="sxs-lookup"><span data-stu-id="37857-120">**The performance of a page is delayed or appears to pause frequently**.</span></span>  <span data-ttu-id="37857-121">Dies ist möglicherweise ein Symptom häufiger Garbage Collections.</span><span class="sxs-lookup"><span data-stu-id="37857-121">This is possibly a symptom of frequent garbage collections.</span></span>  <span data-ttu-id="37857-122">Die Garbage Collection ist der Fall, wenn der Browser Speicher aufhebt.</span><span class="sxs-lookup"><span data-stu-id="37857-122">Garbage collection is when the browser reclaims memory.</span></span>  <span data-ttu-id="37857-123">Der Browser entscheidet, wann dies geschieht.</span><span class="sxs-lookup"><span data-stu-id="37857-123">The browser decides when this happens.</span></span>  <span data-ttu-id="37857-124">Während Auflistungen wird alle ausgeführten Skripts angehalten.</span><span class="sxs-lookup"><span data-stu-id="37857-124">During collections, all script running is paused.</span></span>  <span data-ttu-id="37857-125">Wenn der Browser also viel Garbage Collection durchläuft, wird die Skriptlaufzeit viel angehalten.</span><span class="sxs-lookup"><span data-stu-id="37857-125">So if the browser is garbage collecting a lot, script runtime is going to get paused a lot.</span></span>  

### <span data-ttu-id="37857-126">Speicher aufblasen: wie viel ist "zu viel"?</span><span class="sxs-lookup"><span data-stu-id="37857-126">Memory bloat: how much is "too much"?</span></span>  

<span data-ttu-id="37857-127">Ein Speicherverlust ist einfach zu definieren.</span><span class="sxs-lookup"><span data-stu-id="37857-127">A memory leak is easy to define.</span></span>  <span data-ttu-id="37857-128">Wenn eine Website zunehmend mehr und mehr Arbeitsspeicher verwendet, liegt ein Leck vor.</span><span class="sxs-lookup"><span data-stu-id="37857-128">If a site is progressively using more and more memory, then you have a leak.</span></span>  <span data-ttu-id="37857-129">Aber der Speicher aufblasen ist etwas schwieriger zu anheften.</span><span class="sxs-lookup"><span data-stu-id="37857-129">But memory bloat is a bit harder to pin down.</span></span>  <span data-ttu-id="37857-130">Was qualifiziert als "Verwenden von zu viel Arbeitsspeicher"?</span><span class="sxs-lookup"><span data-stu-id="37857-130">What qualifies as "using too much memory"?</span></span>  

<span data-ttu-id="37857-131">Hier gibt es keine harten Zahlen, da unterschiedliche Geräte und Browser unterschiedliche Funktionen aufweisen.</span><span class="sxs-lookup"><span data-stu-id="37857-131">There are no hard numbers here, because different devices and browsers have different capabilities.</span></span>  <span data-ttu-id="37857-132">Die gleiche Seite, die auf einem Highend-Smartphone problemlos läuft, kann auf einem Low-End-Smartphone abstürzen.</span><span class="sxs-lookup"><span data-stu-id="37857-132">The same page that runs smoothly on a high-end smartphone may crash on a low-end smartphone.</span></span>  

<span data-ttu-id="37857-133">Der Schlüssel besteht darin, das Schienen Modell zu verwenden und sich auf die Benutzer zu konzentrieren.</span><span class="sxs-lookup"><span data-stu-id="37857-133">The key here is to use the RAIL model and focus on your users.</span></span>  <span data-ttu-id="37857-134">Finden Sie heraus, welche Geräte für Ihre Benutzer beliebt sind, und testen Sie dann Ihre Seite auf diesen Geräten.</span><span class="sxs-lookup"><span data-stu-id="37857-134">Find out what devices are popular with your users, and then test out your page on those devices.</span></span>  <span data-ttu-id="37857-135">Wenn die Erfahrung durchweg fehlerhaft ist, kann die Seite die Speicherfunktionen dieser Geräte überschreiten.</span><span class="sxs-lookup"><span data-stu-id="37857-135">If the experience is consistently bad, the page may be exceeding the memory capabilities of those devices.</span></span>  

## <span data-ttu-id="37857-136">Überwachen der Speichernutzung in Echtzeit mit dem Microsoft Edge-Browser-Task-Manager</span><span class="sxs-lookup"><span data-stu-id="37857-136">Monitor memory use in realtime with the Microsoft Edge Browser Task Manager</span></span>  

<span data-ttu-id="37857-137">Verwenden Sie den Microsoft Edge-Browser-Task-Manager als Ausgangspunkt für die Untersuchung des Speicherproblems.</span><span class="sxs-lookup"><span data-stu-id="37857-137">Use the Microsoft Edge Browser Task Manager as a starting point to your memory issue investigation.</span></span>  <span data-ttu-id="37857-138">Der Microsoft Edge-Browser-Task-Manager ist ein Echtzeitmonitor, der Ihnen mitteilt, wie viel Arbeitsspeicher eine Seite zurzeit verwendet.</span><span class="sxs-lookup"><span data-stu-id="37857-138">The Microsoft Edge Browser Task Manager is a realtime monitor that tells you how much memory a page is currently using.</span></span>  

1.  <span data-ttu-id="37857-139">Drücken `Shift` + `Esc` oder wechseln Sie zum Hauptmenü von Microsoft Edge, und wählen Sie **Weitere Tools**  >  **Browser Task-Manager** aus, um den Task-Manager von Microsoft Edge-Browser zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="37857-139">Press `Shift`+`Esc` or go to the Microsoft Edge main menu and select **More tools** > **Browser Task Manager** to open the Microsoft Edge Browser Task Manager.</span></span>  
    
    > ##### <span data-ttu-id="37857-140">Abbildung1</span><span class="sxs-lookup"><span data-stu-id="37857-140">Figure 1</span></span>  
    > <span data-ttu-id="37857-141">Öffnen des Task-Managers des Microsoft Edge-Browsers</span><span class="sxs-lookup"><span data-stu-id="37857-141">Opening the Microsoft Edge Browser Task Manager</span></span>  
    > ![Öffnen des Task-Managers des Microsoft Edge-Browsers][ImageTaskManager]  
    
1.  <span data-ttu-id="37857-143">Klicken Sie mit der rechten Maustaste auf die Tabellenüberschrift des Task-Managers von Microsoft Edge-Browser, und aktivieren Sie **JavaScript-Speicher**.</span><span class="sxs-lookup"><span data-stu-id="37857-143">Right-click on the table header of the Microsoft Edge Browser Task Manager and enable **JavaScript memory**.</span></span>  
    
    > ##### <span data-ttu-id="37857-144">Abbildung2</span><span class="sxs-lookup"><span data-stu-id="37857-144">Figure 2</span></span>  
    > <span data-ttu-id="37857-145">Aktivieren des JavaScript-Speichers</span><span class="sxs-lookup"><span data-stu-id="37857-145">Enable JavaScript memory</span></span>  
    > ![Aktivieren des JavaScript-Speichers][ImageJavascriptMemory]  
    
<span data-ttu-id="37857-147">Diese beiden Spalten geben Ihnen unterschiedliche Informationen dazu, wie Ihre Seite den Arbeitsspeicher verwendet:</span><span class="sxs-lookup"><span data-stu-id="37857-147">These two columns tell you different things about how your page is using memory:</span></span>  

*   <span data-ttu-id="37857-148">Die **Speicher** Spalte stellt den systemeigenen Speicher dar.</span><span class="sxs-lookup"><span data-stu-id="37857-148">The **Memory** column represents native memory.</span></span>  <span data-ttu-id="37857-149">DOM-Knoten werden im systemeigenen Speicher gespeichert.</span><span class="sxs-lookup"><span data-stu-id="37857-149">DOM nodes are stored in native memory.</span></span>  <span data-ttu-id="37857-150">Wenn dieser Wert immer größer wird, werden DOM-Knoten erstellt.</span><span class="sxs-lookup"><span data-stu-id="37857-150">If this value is increasing, DOM nodes are getting created.</span></span>  
*   <span data-ttu-id="37857-151">Die **JavaScript-Speicher** Spalte stellt den js-Heap dar.</span><span class="sxs-lookup"><span data-stu-id="37857-151">The **JavaScript Memory** column represents the JS heap.</span></span>  <span data-ttu-id="37857-152">Diese Spalte enthält zwei Werte.</span><span class="sxs-lookup"><span data-stu-id="37857-152">This column contains two values.</span></span>  <span data-ttu-id="37857-153">Der Wert, an dem Sie interessiert sind, ist die Live-Nummer \ (die Zahl in Klammern \).</span><span class="sxs-lookup"><span data-stu-id="37857-153">The value you are interested in is the live number \(the number in parentheses\).</span></span>  <span data-ttu-id="37857-154">Die Live-Nummer gibt an, wie viel Arbeitsspeicher die erreichbaren Objekte auf der Seite verwenden.</span><span class="sxs-lookup"><span data-stu-id="37857-154">The live number represents how much memory the reachable objects on your page are using.</span></span>  <span data-ttu-id="37857-155">Wenn diese Zahl zunimmt, werden entweder neue Objekte erstellt, oder die vorhandenen Objekte werden größer.</span><span class="sxs-lookup"><span data-stu-id="37857-155">If this number is increasing, either new objects are being created, or the existing objects are growing.</span></span>  

<!--*   live number reference: https://groups.google.com/d/msg/google-chrome-developer-tools/aTMVGoNM0VY/bLmf3l2CpJ8J  -->  

## <span data-ttu-id="37857-156">Visualisieren von Speicherverlusten mithilfe des Leistungs Panels</span><span class="sxs-lookup"><span data-stu-id="37857-156">Visualize memory leaks with Performance panel</span></span>  

<span data-ttu-id="37857-157">Sie können das Leistungs Panel auch als weiteren Ausgangspunkt ihrer Untersuchung verwenden.</span><span class="sxs-lookup"><span data-stu-id="37857-157">You may also use the Performance panel as another starting point in your investigation.</span></span>  <span data-ttu-id="37857-158">Der Leistungs Panel hilft Ihnen, die Speichernutzung einer Seite im Laufe der Zeit zu visualisieren.</span><span class="sxs-lookup"><span data-stu-id="37857-158">The Performance panel helps you visualize the memory use of a page over time.</span></span>  

1.  <span data-ttu-id="37857-159">Öffnen Sie in devtools das Panel **Leistung** .</span><span class="sxs-lookup"><span data-stu-id="37857-159">Open the **Performance** panel on DevTools.</span></span>  
1.  <span data-ttu-id="37857-160">Aktivieren Sie das Kontrollkästchen **Speicher** .</span><span class="sxs-lookup"><span data-stu-id="37857-160">Enable the **Memory** checkbox.</span></span>  
1.  <span data-ttu-id="37857-161">[Führen Sie eine Aufzeichnung][DevtoolsEvaluatePerformanceReferenceRecord]aus.</span><span class="sxs-lookup"><span data-stu-id="37857-161">[Make a recording][DevtoolsEvaluatePerformanceReferenceRecord].</span></span>  

> [!TIP]
> <span data-ttu-id="37857-162">Es empfiehlt sich, die Aufzeichnung mit einer erzwungenen Garbage Collection zu starten und zu beenden.</span><span class="sxs-lookup"><span data-stu-id="37857-162">It is a good practice to start and end your recording with a forced garbage collection.</span></span>  <span data-ttu-id="37857-163">Klicken Sie **collect garbage** ![ während der Aufzeichnung auf die Schaltfläche Garbage Collection sammeln, um die Garbage ][ImageForceGarbageCollectionIcon] Collection zu erzwingen.</span><span class="sxs-lookup"><span data-stu-id="37857-163">Click the **collect garbage** ![force garbage collection][ImageForceGarbageCollectionIcon] button while recording to force garbage collection.</span></span>  

<span data-ttu-id="37857-164">Wenn Sie Speicher Aufzeichnungen demonstrieren möchten, sollten Sie den folgenden Code verwenden:</span><span class="sxs-lookup"><span data-stu-id="37857-164">To demonstrate memory recordings, consider the code below:</span></span>  

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

<span data-ttu-id="37857-165">Jedes Mal, wenn die Schaltfläche, auf die im Code verwiesen wird, gedrückt wird, werden 10000- `div` Knoten an den Dokument Text angefügt, und eine Zeichenfolge mit 1 Million `x` Zeichen wird auf das `x` Array verschoben.</span><span class="sxs-lookup"><span data-stu-id="37857-165">Every time that the button referenced in the code is pressed, ten thousand `div` nodes are appended to the document body, and a string of one million `x` characters is pushed onto the `x` array.</span></span>  <span data-ttu-id="37857-166">Durch Ausführen dieses Codes wird eine Aufzeichnung im **Leistungs** Panel wie [Abbildung 3](#figure-3)erstellt.</span><span class="sxs-lookup"><span data-stu-id="37857-166">Running this code produces a recording in the **Performance** panel like [Figure 3](#figure-3).</span></span>  

> ##### <span data-ttu-id="37857-167">Abbildung 3</span><span class="sxs-lookup"><span data-stu-id="37857-167">Figure 3</span></span>  
> <span data-ttu-id="37857-168">Einfaches Wachstum</span><span class="sxs-lookup"><span data-stu-id="37857-168">Simple growth</span></span>  
> ![Einfaches Wachstum][ImageSimpleGrowth]  

<span data-ttu-id="37857-170">Zunächst eine Erläuterung der Benutzeroberfläche.</span><span class="sxs-lookup"><span data-stu-id="37857-170">First, an explanation of the user interface.</span></span>  <span data-ttu-id="37857-171">Das **Heap** Diagramm im Übersichts \**Bereich \** (unter **net**\) stellt den js-Heap dar.</span><span class="sxs-lookup"><span data-stu-id="37857-171">The **HEAP** graph in the **Overview** pane \(below **NET**\) represents the JS heap.</span></span>  <span data-ttu-id="37857-172">Unter dem Übersichtsbereich befindet sich **der Bereich** **Zähler** .</span><span class="sxs-lookup"><span data-stu-id="37857-172">Below the **Overview** pane is the **Counter** pane.</span></span>  <span data-ttu-id="37857-173">Hier können **Sie die Speicher** Auslastung nach js-Heap (wie **Heap** Diagramm im Übersichtsbereich \), Dokumente, DOM-Knoten, Listener und GPU-Speicher unterteilt sehen.</span><span class="sxs-lookup"><span data-stu-id="37857-173">Here you are able to see memory usage broken down by JS heap \(same as **HEAP** graph in the **Overview** pane\), documents, DOM nodes, listeners, and GPU memory.</span></span>  <span data-ttu-id="37857-174">Wenn Sie ein Kontrollkästchen deaktivieren, wird es aus dem Diagramm ausgeblendet.</span><span class="sxs-lookup"><span data-stu-id="37857-174">Disabling a checkbox hides it from the graph.</span></span>  

<span data-ttu-id="37857-175">Nun eine Analyse des Codes im Vergleich zu [Abbildung 3](#figure-3).</span><span class="sxs-lookup"><span data-stu-id="37857-175">Now, an analysis of the code compared with [Figure 3](#figure-3).</span></span>  <span data-ttu-id="37857-176">Wenn Sie sich den Knoten Zähler \ (das grüne Diagramm \) ansehen, können Sie sehen, dass er mit dem Code sauber übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="37857-176">If you look at the node counter \(the green graph\) you are able to see that it matches up cleanly with the code.</span></span>  <span data-ttu-id="37857-177">Die Anzahl der Knoten nimmt in diskreten Schritten zu.</span><span class="sxs-lookup"><span data-stu-id="37857-177">The node count increases in discrete steps.</span></span>  <span data-ttu-id="37857-178">Sie können davon ausgehen, dass jede Erhöhung der Knotenanzahl ein Aufruf von ist `grow()` .</span><span class="sxs-lookup"><span data-stu-id="37857-178">You may presume that each increase in the node count is a call to `grow()`.</span></span>  <span data-ttu-id="37857-179">Das js-Heap Diagramm \ (das blaue Diagramm \) ist nicht so einfach.</span><span class="sxs-lookup"><span data-stu-id="37857-179">The JS heap graph \(the blue graph\) is not as straightforward.</span></span>  <span data-ttu-id="37857-180">In Übereinstimmung mit den bewährten Methoden ist der erste DIP eine erzwungene Garbage Collection \ (erreicht durch **collect garbage** Drücken der ![ Schaltfläche Garbage Force Garbage Collection sammeln ][ImageForceGarbageCollectionIcon] ).</span><span class="sxs-lookup"><span data-stu-id="37857-180">In keeping with best practices, the first dip is actually a forced garbage collection \(achieved by pressing the  **collect garbage** ![force garbage collection][ImageForceGarbageCollectionIcon] button\).</span></span>  <span data-ttu-id="37857-181">Während die Aufzeichnung fortschreitet, können Sie sehen, dass die JS-Heapgröße Spikes.</span><span class="sxs-lookup"><span data-stu-id="37857-181">As the recording progresses you are able to see that the JS heap size spikes.</span></span>  <span data-ttu-id="37857-182">Dies ist natürlich und erwartet: der JavaScript-Code erstellt die DOM-Knoten auf jedem Schaltflächenklick und macht viel Arbeit, wenn die Zeichenfolge von 1 Million-Zeichen erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="37857-182">This is natural and expected:  the JavaScript code is creating the DOM nodes on every button click and doing a lot of work when it creates the string of one million characters.</span></span>  <span data-ttu-id="37857-183">Der wichtigste Punkt hierbei ist die Tatsache, dass der JS-Heap höher als gestartet ist \ (der "Anfang" hier ist der Punkt nach der erzwungenen Garbage Collection \).</span><span class="sxs-lookup"><span data-stu-id="37857-183">The key thing here is the fact that the JS heap ends higher than it began \(the "beginning" here being the point after the forced garbage collection\).</span></span>  <span data-ttu-id="37857-184">Wenn Sie in der realen Welt dieses Muster mit einer zunehmenden js-Heapgröße oder Knoten Größe gesehen haben, kann dies potenziell einen Speicherverlust definieren.</span><span class="sxs-lookup"><span data-stu-id="37857-184">In the real world, if you saw this pattern of increasing JS heap size or node size, it may potentially define a memory leak.</span></span>  

<!--todo: the Heap snapshots and Profiles panel are not found in Edge  -->  

## <span data-ttu-id="37857-185">Entdecken von frei gelösten Dom-Strukturspeicher Lecks mit Heap-Schnappschüssen</span><span class="sxs-lookup"><span data-stu-id="37857-185">Discover detached DOM tree memory leaks with Heap Snapshots</span></span>  

<span data-ttu-id="37857-186">Ein DOM-Knoten ist nur Garbage Collection, wenn keine Verweise auf den Knoten aus der DOM-Struktur oder dem auf der Seite ausgeführten JavaScript-Code vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="37857-186">A DOM node is only garbage collected when there are no references to the node from either the DOM tree or JavaScript code running on the page.</span></span>  <span data-ttu-id="37857-187">Ein Knoten wird als "losgelöst" bezeichnet, wenn er aus der DOM-Struktur entfernt wird, aber einige JavaScript-Objekte verweisen weiterhin auf ihn.</span><span class="sxs-lookup"><span data-stu-id="37857-187">A node is said to be "detached" when it is removed from the DOM tree but some JavaScript still references it.</span></span>  <span data-ttu-id="37857-188">Getrennte DOM-Knoten sind eine häufige Ursache für Speicherverluste.</span><span class="sxs-lookup"><span data-stu-id="37857-188">Detached DOM nodes are a common cause of memory leaks.</span></span>  <span data-ttu-id="37857-189">In diesem Abschnitt erfahren Sie, wie Sie die Heap-Profiler in devtools verwenden, um getrennte Knoten zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="37857-189">This section teaches you how to use the heap profilers in DevTools to identify detached nodes.</span></span>  

<span data-ttu-id="37857-190">Es folgt ein einfaches Beispiel für getrennte DOM-Knoten.</span><span class="sxs-lookup"><span data-stu-id="37857-190">Here is a simple example of detached DOM nodes.</span></span>  

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

<span data-ttu-id="37857-191">Durch Klicken auf die Schaltfläche im Code wird ein `ul` Knoten mit zehn unter `li` geordneten Elementen erstellt.</span><span class="sxs-lookup"><span data-stu-id="37857-191">Clicking the button referenced in the code creates a `ul` node with ten `li` children.</span></span>  <span data-ttu-id="37857-192">Auf diese Knoten wird vom Code verwiesen, aber Sie sind nicht in der DOM-Struktur vorhanden, daher wird jeder getrennt.</span><span class="sxs-lookup"><span data-stu-id="37857-192">These nodes are referenced by the code but do not exist in the DOM tree, so each is detached.</span></span>  

<span data-ttu-id="37857-193">Heap-Schnappschüsse sind eine Möglichkeit, getrennte Knoten zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="37857-193">Heap snapshots are one way to identify detached nodes.</span></span>  <span data-ttu-id="37857-194">Wie der Name schon sagt, zeigen Heap-Schnappschüsse an, wie der Speicher zwischen den js-Objekten und DOM-Knoten für Ihre Seite zum Zeitpunkt des Schnappschusses verteilt wird.</span><span class="sxs-lookup"><span data-stu-id="37857-194">As the name implies, heap snapshots show you how memory is distributed among the JS objects and DOM nodes for your page at the point of time of the snapshot.</span></span>  

<span data-ttu-id="37857-195">Wenn Sie einen Schnappschuss erstellen möchten, öffnen Sie devtools, und wechseln Sie zum **Speicher** Panel, wählen Sie das Optionsfeld **Heap-Snapshot** aus, und drücken Sie dann die Schaltfläche **Schnappschuss aufnehmen** .</span><span class="sxs-lookup"><span data-stu-id="37857-195">To create a snapshot, open DevTools and go to the **Memory** panel, select the **Heap snapshot** radio button, and then press the **Take snapshot** button.</span></span>  

> ##### <span data-ttu-id="37857-196">Abbildung4</span><span class="sxs-lookup"><span data-stu-id="37857-196">Figure 4</span></span>  
> <span data-ttu-id="37857-197">Snapshot des Heaps aufnehmen</span><span class="sxs-lookup"><span data-stu-id="37857-197">Take heap snapshot</span></span>  
> ![Snapshot des Heaps aufnehmen][ImageTakeHeapSnapshot]  

<span data-ttu-id="37857-199">Der Snapshot kann einige Zeit dauern, bis er verarbeitet und geladen wurde.</span><span class="sxs-lookup"><span data-stu-id="37857-199">The snapshot may take some time to process and load.</span></span>  <span data-ttu-id="37857-200">Wenn Sie den Vorgang beenden, wählen Sie ihn im linken Panel aus. \ (benannte **Heap-Schnappschüsse**\).</span><span class="sxs-lookup"><span data-stu-id="37857-200">After it is finished, select it from the left-hand panel \(named **HEAP SNAPSHOTS**\).</span></span>  

<span data-ttu-id="37857-201">Geben `Detached` Sie in das Textfeld **Klassenfilter** ein, um nach frei gelösten Dom-Strukturen zu suchen.</span><span class="sxs-lookup"><span data-stu-id="37857-201">Type `Detached` in the **Class filter** textbox to search for detached DOM trees.</span></span>  

> ##### <span data-ttu-id="37857-202">Abbildung5</span><span class="sxs-lookup"><span data-stu-id="37857-202">Figure 5</span></span>  
> <span data-ttu-id="37857-203">Filtern für getrennte Knoten</span><span class="sxs-lookup"><span data-stu-id="37857-203">Filtering for detached nodes</span></span>  
> ![Filtern für getrennte Knoten][ImageFilteringForDetachedNodes]  

<span data-ttu-id="37857-205">Erweitern Sie die Karat, um eine frei gelöste Struktur zu untersuchen.</span><span class="sxs-lookup"><span data-stu-id="37857-205">Expand the carats to investigate a detached tree.</span></span>  

> ##### <span data-ttu-id="37857-206">Abbildung6</span><span class="sxs-lookup"><span data-stu-id="37857-206">Figure 6</span></span>  
> <span data-ttu-id="37857-207">Untersuchen von getrennten Strukturen</span><span class="sxs-lookup"><span data-stu-id="37857-207">Investigating detached tree</span></span>  
> ![Untersuchen von getrennten Strukturen][ImageInvestigatingDetachedTree]  

<!--Nodes highlighted yellow have direct references to them from the JavaScript code.  Nodes highlighted red do not have direct references.  They are only alive because they are part of the tree for the yellow node.  In general, you want to focus on the yellow nodes.  Fix your code so that the yellow node is not alive for longer than it needs to be, and you also get rid of the red nodes that are part of the tree for the yellow node.  -->

<span data-ttu-id="37857-209">Klicken Sie auf einen Knoten, um ihn weiter zu untersuchen.</span><span class="sxs-lookup"><span data-stu-id="37857-209">Click on a node to investigate it further.</span></span>  <span data-ttu-id="37857-210">Im **Objekt** Bereich können Sie weitere Informationen zu dem Code anzeigen, der darauf verweist.</span><span class="sxs-lookup"><span data-stu-id="37857-210">In the **Objects** pane you are able to see more information about the code that is referencing it.</span></span>  <span data-ttu-id="37857-211">In [Abbildung 7](#figure-7) können Sie beispielsweise feststellen, dass die `detachedNodes` Variable auf den Knoten verweist.</span><span class="sxs-lookup"><span data-stu-id="37857-211">For example, in [Figure 7](#figure-7) you are able to see that the `detachedNodes` variable is referencing the node.</span></span>  <span data-ttu-id="37857-212">Um diesen bestimmten Speicherverlust zu beheben, sollten Sie den Code untersuchen, der die Variable verwendet, `detachedUNode` und sicherstellen, dass der Verweis auf den Knoten entfernt wird, wenn er nicht mehr benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="37857-212">To fix this particular memory leak, you should study the code that uses the `detachedUNode` variable and ensure that the reference to the node is removed when it is no longer needed.</span></span>

> ##### <span data-ttu-id="37857-213">Abbildung7</span><span class="sxs-lookup"><span data-stu-id="37857-213">Figure 7</span></span>  
> <span data-ttu-id="37857-214">Untersuchen eines Knotens</span><span class="sxs-lookup"><span data-stu-id="37857-214">Investigating a node</span></span>  
> ![Untersuchen eines Knotens][ImageInvestigatingNode]  

<!--todo: the allocation timeline does not appear in the DevTools in Edge  -->  

## <span data-ttu-id="37857-216">Ermitteln von JS-Heapspeicher Lecks mit Zuordnungs Instrumentation auf Zeitachse</span><span class="sxs-lookup"><span data-stu-id="37857-216">Identify JS heap memory leaks with Allocation instrumentation on timeline</span></span>  

<span data-ttu-id="37857-217">Die **Zuweisungs Instrumentation auf der Zeitachse** ist ein weiteres Tool, mit dem Sie möglicherweise Speicherverluste in Ihrem js-Heap ermitteln können.</span><span class="sxs-lookup"><span data-stu-id="37857-217">**Allocation instrumentation on timeline** is another tool that may help you track down memory leaks in your JS heap.</span></span>  

<span data-ttu-id="37857-218">Demonstrieren Sie die **Zuweisungs Instrumentation auf Zeitachse** mithilfe des folgenden Codes.</span><span class="sxs-lookup"><span data-stu-id="37857-218">Demonstrate **Allocation instrumentation on timeline**  using the following code.</span></span>  

```javascript
var x = [];
function grow() {
    x.push(new Array(1000000).join('x'));
}
document.getElementById('grow').addEventListener('click', grow);
```  

<span data-ttu-id="37857-219">Jedes Mal, wenn die Schaltfläche, auf die im Code verwiesen wird, gedrückt wird, wird dem Array eine Zeichenfolge von 1 Million-Zeichen hinzugefügt `x` .</span><span class="sxs-lookup"><span data-stu-id="37857-219">Every time that the button referenced in the code is pushed, a string of one million characters is added to the `x` array.</span></span>  

<span data-ttu-id="37857-220">Wenn Sie eine Zuordnungs Instrumentation auf der Zeitachse aufzeichnen möchten, öffnen Sie devtools, wechseln Sie zur Register **Karte Speicher** , wählen Sie das Optionsfeld **Zuweisungs Instrumentation auf Zeitachse** aus, drücken Sie die Schaltfläche **Start** , führen Sie die Aktion aus, die Sie vermuten, dass der Speicherverlust verursacht wird, und drücken Sie dann die Schaltfläche **Aufzeichnung** Beenden der Aufzeichnung beenden, ![ ][ImageStopRecordingIcon] Wenn Sie fertig sind.</span><span class="sxs-lookup"><span data-stu-id="37857-220">To record an Allocation instrumentation on timeline, open DevTools, go to the **Memory** panel, select the **Allocation instrumentation on timeline** radio button, press the **Start** button, perform the action that you suspect is causing the memory leak, and then press the **Stop recording heap profile** ![stop recording][ImageStopRecordingIcon] button when you are done.</span></span>  

<span data-ttu-id="37857-221">Beachten Sie während der Aufzeichnung, ob blaue Balken in der Zuordnungs Instrumentation auf der Zeitachse angezeigt werden, wie in [Abbildung 8](#figure-8).</span><span class="sxs-lookup"><span data-stu-id="37857-221">As you are recording, notice if any blue bars show up on the Allocation instrumentation on timeline, like in [Figure 8](#figure-8).</span></span>  

> ##### <span data-ttu-id="37857-222">Abbildung8</span><span class="sxs-lookup"><span data-stu-id="37857-222">Figure 8</span></span>  
> <span data-ttu-id="37857-223">Neue Zuweisungen</span><span class="sxs-lookup"><span data-stu-id="37857-223">New allocations</span></span>  
> ![Neue Zuweisungen][ImageNewAllocations]  

<span data-ttu-id="37857-225">Diese blauen Balken stellen neue Speicherzuweisungen dar.</span><span class="sxs-lookup"><span data-stu-id="37857-225">Those blue bars represent new memory allocations.</span></span>  <span data-ttu-id="37857-226">Diese neuen Speicherzuweisungen sind ihre Kandidaten für Speicherverluste.</span><span class="sxs-lookup"><span data-stu-id="37857-226">Those new memory allocations are your candidates for memory leaks.</span></span>  <span data-ttu-id="37857-227">Sie können auf eine Leiste Zoomen, um den Bereich " **Konstruktor** " zu filtern, sodass nur Objekte angezeigt werden, die während des angegebenen Zeitrahmens reserviert wurden.</span><span class="sxs-lookup"><span data-stu-id="37857-227">You are able to zoom on a bar to filter the **Constructor** pane to only show objects that were allocated during the specified timeframe.</span></span>  

> ##### <span data-ttu-id="37857-228">Abbildung 9</span><span class="sxs-lookup"><span data-stu-id="37857-228">Figure 9</span></span>  
> <span data-ttu-id="37857-229">Verkleinerte Zuordnungs Zeitachse</span><span class="sxs-lookup"><span data-stu-id="37857-229">Zoomed allocation timeline</span></span>  
> ![Verkleinerte Zuordnungs Zeitachse][ImageZoomedAllocationTimeline]  

<span data-ttu-id="37857-231">Erweitern Sie das Objekt, und klicken Sie auf den Wert, um weitere Details im **Objekt** Bereich anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="37857-231">Expand the object and click on the value to view more details in the **Object** pane.</span></span>  <span data-ttu-id="37857-232">Wenn Sie beispielsweise in [Abbildung 10](#figure-10)die Details des neu zugewiesenen Objekts anzeigen, sollten Sie sehen können, dass es der `x` Variablen im Bereich zugeordnet wurde `Window` .</span><span class="sxs-lookup"><span data-stu-id="37857-232">For example, in [Figure 10](#figure-10), by viewing the details of the object that was newly allocated, you should be able to see that it was allocated to the `x` variable in the `Window` scope.</span></span>  

> ##### <span data-ttu-id="37857-233">Abbildung 10</span><span class="sxs-lookup"><span data-stu-id="37857-233">Figure 10</span></span> 
> <span data-ttu-id="37857-234">Objektdetails</span><span class="sxs-lookup"><span data-stu-id="37857-234">Object details</span></span>  
> ![Objektdetails][ImageObjectDetail]  

## <span data-ttu-id="37857-236">Untersuchen der Speicherzuweisung nach Funktion</span><span class="sxs-lookup"><span data-stu-id="37857-236">Investigate memory allocation by function</span></span>   

<span data-ttu-id="37857-237">Verwenden Sie den Profilerstellungs-Typ der **Zuordnungs Stichprobe** , um die Speicherzuweisung nach JavaScript-Funktion anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="37857-237">Use the **Allocation sampling** profiling type to view memory allocation by JavaScript function.</span></span>  

> ##### <span data-ttu-id="37857-238">Abbildung 11</span><span class="sxs-lookup"><span data-stu-id="37857-238">Figure 11</span></span>  
> <span data-ttu-id="37857-239">Sampling für Daten Satz Zuteilung</span><span class="sxs-lookup"><span data-stu-id="37857-239">Record Allocation sampling</span></span>  
> ![Sampling für Daten Satz Zuteilung][ImageRecordAllocationSampling]  

1.  <span data-ttu-id="37857-241">Aktivieren Sie das Optionsfeld **Zuweisungs Sampling** .</span><span class="sxs-lookup"><span data-stu-id="37857-241">Select the **Allocation sampling** radio button.</span></span>  <span data-ttu-id="37857-242">Wenn auf der Seite eine Arbeitskraft vorhanden ist, können Sie diese über das Dropdownmenü neben der Schaltfläche **Start** als Profil Ziel auswählen.</span><span class="sxs-lookup"><span data-stu-id="37857-242">If there is a worker on the page, you are able to select that as the profiling target using the dropdown menu next to the **Start** button.</span></span>  
1.  <span data-ttu-id="37857-243">Drücken Sie die Schaltfläche **Start** .</span><span class="sxs-lookup"><span data-stu-id="37857-243">Press the **Start** button.</span></span>  
1.  <span data-ttu-id="37857-244">Führen Sie die Aktionen auf der Seite aus, die Sie untersuchen möchten.</span><span class="sxs-lookup"><span data-stu-id="37857-244">Perform the actions on the page which you want to investigate.</span></span>  
1.  <span data-ttu-id="37857-245">Drücken Sie die **Stopp** -Taste, wenn Sie alle Ihre Aktionen beendet haben.</span><span class="sxs-lookup"><span data-stu-id="37857-245">Press the **Stop** button when you have finished all of your actions.</span></span>  

<span data-ttu-id="37857-246">DevTools zeigt eine Aufschlüsselung der Speicherzuweisung nach Funktion.</span><span class="sxs-lookup"><span data-stu-id="37857-246">DevTools shows you a breakdown of memory allocation by function.</span></span>  <span data-ttu-id="37857-247">Die Standardansicht ist **schwer (unten nach oben)**, in der die Funktionen angezeigt werden, die den größten Arbeitsspeicher oben zugewiesen haben.</span><span class="sxs-lookup"><span data-stu-id="37857-247">The default view is **Heavy (Bottom Up)**, which displays the functions that allocated the most memory at the top.</span></span>  

> ##### <span data-ttu-id="37857-248">Abbildung 12</span><span class="sxs-lookup"><span data-stu-id="37857-248">Figure 12</span></span>  
> <span data-ttu-id="37857-249">Zuordnungs Stichproben</span><span class="sxs-lookup"><span data-stu-id="37857-249">Allocation sampling</span></span>  
>![Zuordnungs Stichproben][ImageAllocationSampling]  

## <span data-ttu-id="37857-251">Häufige Garbage Collections erkennen</span><span class="sxs-lookup"><span data-stu-id="37857-251">Spot frequent garbage collections</span></span>  

<span data-ttu-id="37857-252">Wenn Ihre Seite häufig angehalten wird, haben Sie möglicherweise Probleme mit der Garbage Collection.</span><span class="sxs-lookup"><span data-stu-id="37857-252">If your page appears to pause frequently, then you may have garbage collection issues.</span></span>  

<span data-ttu-id="37857-253">Sie können entweder den Microsoft Edge-Browser-Task-Manager oder Leistungs Speicher Aufzeichnungen verwenden, um häufige Garbage Collection zu erkennen.</span><span class="sxs-lookup"><span data-stu-id="37857-253">You are able to use either the Microsoft Edge Browser Task Manager or Performance memory recordings to spot frequent garbage collection.</span></span>  <span data-ttu-id="37857-254">Im Microsoft Edge-Browser Task-Manager stellen häufig steigende und fallende **Speicher** -oder **JavaScript-Speicher** Werte häufige Garbage Collection dar.</span><span class="sxs-lookup"><span data-stu-id="37857-254">In the Microsoft Edge Browser Task Manager, frequently rising and falling **Memory** or **JavaScript Memory** values represent frequent garbage collection.</span></span>  <span data-ttu-id="37857-255">In Leistungs Aufzeichnungen deuten häufige Änderungen (steigende und fallende) auf die JS-Heap-oder Knotenanzahl-Diagramme auf häufige Garbage Collection hin.</span><span class="sxs-lookup"><span data-stu-id="37857-255">In Performance recordings, frequent changes (rising and falling) to the JS heap or node count graphs indicate frequent garbage collection.</span></span>  

<span data-ttu-id="37857-256">Nachdem Sie das Problem identifiziert haben, können Sie eine **Zuordnungs Instrumentation für die Zeitachsen** Aufzeichnung verwenden, um herauszufinden, wo Speicher reserviert wird und welche Funktionen die Zuweisungen verursachen.</span><span class="sxs-lookup"><span data-stu-id="37857-256">After you have identified the problem, you are able to use an **Allocation instrumentation on timeline** recording to find out where memory is being allocated and which functions are causing the allocations.</span></span>  

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
> <span data-ttu-id="37857-270">Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="37857-270">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="37857-271">Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/memory-problems/index) und wird von [Kayce Basken][KayceBasques] (Technical Writer, Chrome devtools \ & Lighthouse \) erstellt.</span><span class="sxs-lookup"><span data-stu-id="37857-271">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/memory-problems/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
<span data-ttu-id="37857-273">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="37857-273">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
