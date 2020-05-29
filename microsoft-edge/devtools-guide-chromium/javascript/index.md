---
title: Erste Schritte mit dem Debuggen von JavaScript in Microsoft Edge devtools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/18/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Web-Entwicklung, F12-Tools, devtools
ms.openlocfilehash: 06df1fd4d6457a3f02be85b95959bdc353865495
ms.sourcegitcommit: ecdc4287fa25a18cb4ddcaf43fcce3b396c3314c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/17/2020
ms.locfileid: "10581824"
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







# <span data-ttu-id="cea04-103">Erste Schritte mit dem Debuggen von JavaScript in Microsoft Edge devtools</span><span class="sxs-lookup"><span data-stu-id="cea04-103">Get Started with Debugging JavaScript in Microsoft Edge DevTools</span></span>   



<span data-ttu-id="cea04-104">In diesem Lernprogramm lernen Sie den grundlegenden Workflow zum Debuggen von JavaScript-Problemen in devtools.</span><span class="sxs-lookup"><span data-stu-id="cea04-104">This tutorial teaches you the basic workflow for debugging any JavaScript issue in DevTools.</span></span>  

## <span data-ttu-id="cea04-105">Schritt 1: reproduzieren des Fehlers</span><span class="sxs-lookup"><span data-stu-id="cea04-105">Step 1: Reproduce the bug</span></span>   

<span data-ttu-id="cea04-106">Das Suchen nach einer Reihe von Aktionen, die einen Fehler konsistent reproduzieren, ist immer der erste Schritt zum Debuggen.</span><span class="sxs-lookup"><span data-stu-id="cea04-106">Finding a series of actions that consistently reproduces a bug is always the first step to debugging.</span></span>  

1.  <span data-ttu-id="cea04-107">Klicken Sie auf **Demo öffnen**.</span><span class="sxs-lookup"><span data-stu-id="cea04-107">Click **Open Demo**.</span></span>  <span data-ttu-id="cea04-108">Halten Sie `Control` \ (Windows \) oder `Command` \ (macOS \) gedrückt, und öffnen Sie die Demo auf einer neuen Registerkarte.</span><span class="sxs-lookup"><span data-stu-id="cea04-108">Hold `Control` \(Windows\) or `Command` \(macOS\) and open the demo in a new tab.</span></span>  

    <span data-ttu-id="cea04-109">[Demo öffnen] [OpenDebugJSDemo]</span><span class="sxs-lookup"><span data-stu-id="cea04-109">[Open Demo][OpenDebugJSDemo]</span></span>  

1.  <span data-ttu-id="cea04-110">Geben Sie `5` den Text in das Textfeld **Zahl 1** ein.</span><span class="sxs-lookup"><span data-stu-id="cea04-110">Enter `5` in the **Number 1** text box.</span></span>  
1.  <span data-ttu-id="cea04-111">Geben Sie `1` den Text in das Textfeld **Zahl 2** ein.</span><span class="sxs-lookup"><span data-stu-id="cea04-111">Enter `1` in the **Number 2** text box.</span></span>  
1.  <span data-ttu-id="cea04-112">Klicken Sie auf **Add Number 1 und Number 2**.</span><span class="sxs-lookup"><span data-stu-id="cea04-112">Click **Add Number 1 and Number 2**.</span></span>  <span data-ttu-id="cea04-113">Die Beschriftung unter der Schaltfläche steht `5 + 1 = 51` .</span><span class="sxs-lookup"><span data-stu-id="cea04-113">The label below the button says `5 + 1 = 51`.</span></span>  <span data-ttu-id="cea04-114">Das Ergebnis sollte sein `6` .</span><span class="sxs-lookup"><span data-stu-id="cea04-114">The result should be `6`.</span></span>  <span data-ttu-id="cea04-115">Dies ist der Fehler, den Sie beheben werden.</span><span class="sxs-lookup"><span data-stu-id="cea04-115">This is the bug you are going to fix.</span></span>  
    
    > ##### <span data-ttu-id="cea04-116">Abbildung1</span><span class="sxs-lookup"><span data-stu-id="cea04-116">Figure 1</span></span>  
    > <span data-ttu-id="cea04-117">Das Ergebnis `5 + 1` ist `51`</span><span class="sxs-lookup"><span data-stu-id="cea04-117">The result of `5 + 1` is `51`, but should be</span></span> `6`  
    > ![Das Ergebnis von 5 + 1 ist 51, sollte aber 6 sein.][ImageJSBugs]  

## <span data-ttu-id="cea04-119">Schritt 2: Kennenlernen der Benutzeroberfläche des Quellbereichs</span><span class="sxs-lookup"><span data-stu-id="cea04-119">Step 2: Get familiar with the Sources panel UI</span></span>   

<span data-ttu-id="cea04-120">DevTools bietet eine Vielzahl unterschiedlicher Tools für verschiedene Aufgaben, wie beispielsweise das Ändern von CSS, die Leistung der Profilerstellung für Seiten und das Überwachen von Netzwerkanforderungen.</span><span class="sxs-lookup"><span data-stu-id="cea04-120">DevTools provides a lot of different tools for different tasks, such as changing CSS, profiling page load performance, and monitoring network requests.</span></span>  <span data-ttu-id="cea04-121">Im **Quellen** Bereich können Sie JavaScript Debuggen.</span><span class="sxs-lookup"><span data-stu-id="cea04-121">The **Sources** panel is where you debug JavaScript.</span></span>  

1.  <span data-ttu-id="cea04-122">Öffnen Sie devtools, indem Sie `Control` + `Shift` + `J` \ (Windows \) oder `Command` + `Option` + `J` \ (macOS \) drücken.</span><span class="sxs-lookup"><span data-stu-id="cea04-122">Open DevTools by pressing `Control`+`Shift`+`J` \(Windows\) or `Command`+`Option`+`J` \(macOS\) .</span></span>  <span data-ttu-id="cea04-123">Mit dieser Tastenkombination wird die **Konsolen** Leiste geöffnet.</span><span class="sxs-lookup"><span data-stu-id="cea04-123">This shortcut opens the **Console** panel.</span></span>  
    
    > ##### <span data-ttu-id="cea04-124">Abbildung2</span><span class="sxs-lookup"><span data-stu-id="cea04-124">Figure 2</span></span>  
    > <span data-ttu-id="cea04-125">Die **Konsolen** Leiste</span><span class="sxs-lookup"><span data-stu-id="cea04-125">The **Console** panel</span></span>  
    > ![Die Konsolen Leiste][ImageJSConsole]  

1.  <span data-ttu-id="cea04-127">Klicken Sie auf die Registerkarte **Quellen** .</span><span class="sxs-lookup"><span data-stu-id="cea04-127">Click the **Sources** tab.</span></span>  
    
    > ##### <span data-ttu-id="cea04-128">Abbildung 3</span><span class="sxs-lookup"><span data-stu-id="cea04-128">Figure 3</span></span>  
    > <span data-ttu-id="cea04-129">Das **Quellen** Panel</span><span class="sxs-lookup"><span data-stu-id="cea04-129">The **Sources** panel</span></span>  
    > ![Das Quellen Panel][ImageJSSources]  

<span data-ttu-id="cea04-131">Die UI des **Quellen** Panels besteht aus drei Teilen:</span><span class="sxs-lookup"><span data-stu-id="cea04-131">The **Sources** panel UI has 3 parts:</span></span>  

> ##### <span data-ttu-id="cea04-132">Abbildung4</span><span class="sxs-lookup"><span data-stu-id="cea04-132">Figure 4</span></span>  
> <span data-ttu-id="cea04-133">Die drei Teile der Benutzeroberfläche des **Quellen** Panels</span><span class="sxs-lookup"><span data-stu-id="cea04-133">The 3 parts of the **Sources** panel UI</span></span>  
> ![Die drei Teile der Benutzeroberfläche des Quellen Panels][ImageJSSourcesAnnotated]  

1.  <span data-ttu-id="cea04-135">Der Bereich " **Datei-Navigator** " \ (Abschnitt 1 in [Abbildung 4](#figure-4)\).</span><span class="sxs-lookup"><span data-stu-id="cea04-135">The **File Navigator** pane \(Section 1 in [Figure 4](#figure-4)\).</span></span>  <span data-ttu-id="cea04-136">Jede Datei, die die Seite anfordert, wird hier aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="cea04-136">Every file that the page requests is listed here.</span></span>  
1.  <span data-ttu-id="cea04-137">Der Bereich " **Code-Editor** " \ (Abschnitt 2 in [Abbildung 4](#figure-4)\).</span><span class="sxs-lookup"><span data-stu-id="cea04-137">The **Code Editor** pane \(Section 2 in [Figure 4](#figure-4)\).</span></span>  <span data-ttu-id="cea04-138">Nachdem Sie eine Datei im Bereich " **Datei-Navigator** " ausgewählt haben, wird hier der Inhalt der Datei angezeigt.</span><span class="sxs-lookup"><span data-stu-id="cea04-138">After selecting a file in the **File Navigator** pane, the contents of that file are displayed here.</span></span>  
1.  <span data-ttu-id="cea04-139">Der **JavaScript-Debugbereich** \ (Abschnitt 3 in [Abbildung 4](#figure-4)\).</span><span class="sxs-lookup"><span data-stu-id="cea04-139">The **JavaScript Debugging** pane \(Section 3 in [Figure 4](#figure-4)\).</span></span>  <span data-ttu-id="cea04-140">Verschiedene Tools zum Überprüfen des Javascripts für die Seite.</span><span class="sxs-lookup"><span data-stu-id="cea04-140">Various tools for inspecting the JavaScript for the page.</span></span>  <span data-ttu-id="cea04-141">Wenn Ihr devtools-Fenster breit ist, wird dieser Bereich rechts neben dem **Code-Editor-** Bereich angezeigt.</span><span class="sxs-lookup"><span data-stu-id="cea04-141">If your DevTools window is wide, this pane is displayed to the right of the **Code Editor** pane.</span></span>  

## <span data-ttu-id="cea04-142">Schritt 3: Anhalten des Codes mit einem Haltepunkt</span><span class="sxs-lookup"><span data-stu-id="cea04-142">Step 3: Pause the code with a breakpoint</span></span>   

<span data-ttu-id="cea04-143">Eine gängige Methode zum Debuggen eines Problems wie dieses besteht darin, viele `console.log()` Anweisungen in den Code einzufügen, um Werte während der Ausführung des Skripts zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="cea04-143">A common method for debugging a problem like this is to insert a lot of `console.log()` statements into the code, in order to inspect values as the script runs.</span></span>  <span data-ttu-id="cea04-144">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="cea04-144">For example:</span></span>  

```javascript
function updateLabel() {
    var addend1 = getNumber1();
    console.log('addend1:', addend1);
    var addend2 = getNumber2();
    console.log('addend2:', addend2);
    var sum = addend1 + addend2;
    console.log('sum:', sum);
    label.textContent = addend1 + ' + ' + addend2 + ' = ' + sum;
}
```  

<span data-ttu-id="cea04-145">Die `console.log()` Methode erhält möglicherweise die Aufgabe erledigt, aber **Haltepunkte** können Sie schneller erledigen.</span><span class="sxs-lookup"><span data-stu-id="cea04-145">The `console.log()` method may get the job done, but **breakpoints** are able to get it done faster.</span></span>  <span data-ttu-id="cea04-146">Mit einem Haltepunkt können Sie Ihren Code in der Mitte der Laufzeit anhalten und alle Werte zu diesem Zeitpunkt untersuchen.</span><span class="sxs-lookup"><span data-stu-id="cea04-146">A breakpoint lets you pause your code in the middle of the runtime, and examine all values at that moment in time.</span></span>  <span data-ttu-id="cea04-147">Haltepunkte weisen gegenüber der Methode einige Vorteile auf `console.log()` :</span><span class="sxs-lookup"><span data-stu-id="cea04-147">Breakpoints have a few advantages over the `console.log()` method:</span></span>  

*   <span data-ttu-id="cea04-148">Mit `console.log()` müssen Sie den Quellcode manuell öffnen, den relevanten Code suchen, die Anweisungen einfügen und die `console.log()` Seite dann erneut laden, um die Nachrichten in der Konsole anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="cea04-148">With `console.log()`, you need to manually open the source code, find the relevant code, insert the `console.log()` statements, and then reload the page in order to see the messages in the Console.</span></span>  <span data-ttu-id="cea04-149">Mit Haltepunkten können Sie den relevanten Code anhalten, ohne zu wissen, wie der Code strukturiert ist.</span><span class="sxs-lookup"><span data-stu-id="cea04-149">With breakpoints, you may pause on the relevant code without even knowing how the code is structured.</span></span>  
*   <span data-ttu-id="cea04-150">In Ihren `console.log()` Anweisungen müssen Sie jeden Wert, den Sie überprüfen möchten, explizit angeben.</span><span class="sxs-lookup"><span data-stu-id="cea04-150">In your `console.log()` statements you need to explicitly specify each value that you want to inspect.</span></span>  <span data-ttu-id="cea04-151">Mit Haltepunkten zeigt devtools die Werte aller Variablen zu diesem Zeitpunkt an.</span><span class="sxs-lookup"><span data-stu-id="cea04-151">With breakpoints, DevTools shows you the values of all variables at that moment in time.</span></span>  <span data-ttu-id="cea04-152">Manchmal gibt es Variablen, die Ihren Code beeinflussen, den Sie nicht einmal kennen.</span><span class="sxs-lookup"><span data-stu-id="cea04-152">Sometimes there are variables affecting your code that you are not even aware of.</span></span>  

<span data-ttu-id="cea04-153">Kurz gesagt: Haltepunkte können Ihnen helfen, Fehler schneller zu finden und zu beheben als die `console.log()` Methode.</span><span class="sxs-lookup"><span data-stu-id="cea04-153">In short, breakpoints may help you find and fix bugs faster than the `console.log()` method.</span></span>  

<span data-ttu-id="cea04-154">Wenn Sie einen Schritt zurückgehen und darüber nachdenken, wie die APP funktioniert, können Sie eine fundierte Vermutung anstellen, dass die falsche Summe ( `5 + 1 = 51` ) im `click` Ereignislistener berechnet wird, der der Schaltfläche " **Zahl 1" und "Zahl 2** " zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="cea04-154">If you take a step back and think about how the app works, you are able to make an educated guess that the incorrect sum (`5 + 1 = 51`) gets computed in the `click` event listener that is associated to the **Add Number 1 and Number 2** button.</span></span>  <span data-ttu-id="cea04-155">Daher möchten Sie den Code wahrscheinlich um die Zeit anhalten, zu der der `click` Listener ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="cea04-155">Therefore, you probably want to pause the code around the time that the `click` listener runs.</span></span>  <span data-ttu-id="cea04-156">Mit **Ereignis-Listener-Haltepunkten** können Sie genau das ausführen:</span><span class="sxs-lookup"><span data-stu-id="cea04-156">**Event Listener Breakpoints** let you do exactly that:</span></span>  

1.  <span data-ttu-id="cea04-157">Klicken Sie im Bereich **JavaScript-Debuggen** auf **Ereignislistener-Haltepunkte** , um den Abschnitt zu erweitern.</span><span class="sxs-lookup"><span data-stu-id="cea04-157">In the **JavaScript Debugging** pane, click **Event Listener Breakpoints** to expand the section.</span></span>  <span data-ttu-id="cea04-158">DevTools zeigt eine Liste erweiterbarer Ereigniskategorien wie **Animation** und **Zwischenablage**an.</span><span class="sxs-lookup"><span data-stu-id="cea04-158">DevTools reveals a list of expandable event categories, such as **Animation** and **Clipboard**.</span></span>  
1.  <span data-ttu-id="cea04-159">Klicken Sie neben der **Maus** Ereigniskategorie auf Erweiterungssymbol **erweitern** ![ ][ImageExpandIcon] .</span><span class="sxs-lookup"><span data-stu-id="cea04-159">Next to the **Mouse** event category, click **Expand** ![Expand icon][ImageExpandIcon].</span></span>  <span data-ttu-id="cea04-160">DevTools zeigt eine Liste von Mausereignissen wie **Click** und **MouseDown**an.</span><span class="sxs-lookup"><span data-stu-id="cea04-160">DevTools reveals a list of mouse events, such as **click** and **mousedown**.</span></span>  <span data-ttu-id="cea04-161">Neben jedem Ereignis ist ein Kontrollkästchen markiert.</span><span class="sxs-lookup"><span data-stu-id="cea04-161">Each event has a checkbox next to it.</span></span>  
1.  <span data-ttu-id="cea04-162">Aktivieren Sie das Kontrollkästchen **Klicken** .</span><span class="sxs-lookup"><span data-stu-id="cea04-162">Check the **click** checkbox.</span></span>  <span data-ttu-id="cea04-163">DevTools ist jetzt so eingerichtet, dass automatisch angehalten wird, wenn *ein* `click` Ereignis-Listener ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="cea04-163">DevTools is now set up to automatically pause when *any* `click` event listener runs.</span></span>  
    
    > ##### <span data-ttu-id="cea04-164">Abbildung5</span><span class="sxs-lookup"><span data-stu-id="cea04-164">Figure 5</span></span>  
    > <span data-ttu-id="cea04-165">Das Kontrollkästchen **"klicken"** ist aktiviert.</span><span class="sxs-lookup"><span data-stu-id="cea04-165">The **click** checkbox is enabled</span></span>  
    > ![Das Kontrollkästchen "klicken" ist aktiviert.][ImageJSClickCheckbox]  
    
1.  <span data-ttu-id="cea04-167">Klicken Sie wieder auf die Demo und dann erneut auf **Nummer 1 und 2** .</span><span class="sxs-lookup"><span data-stu-id="cea04-167">Back on the demo, click **Add Number 1 and Number 2** again.</span></span>  <span data-ttu-id="cea04-168">DevTools hält die Demo an und hebt eine Codezeile im **Quellen** Panel hervor.</span><span class="sxs-lookup"><span data-stu-id="cea04-168">DevTools pauses the demo and highlights a line of code in the **Sources** panel.</span></span>  <span data-ttu-id="cea04-169">DevTools sollte auf Zeile 16 anhalten `get-started.js` .</span><span class="sxs-lookup"><span data-stu-id="cea04-169">DevTools should pause on line 16 in `get-started.js`.</span></span>  
    
    ```javascript
    if (inputsAreEmpty()) {
    ```  
    
    <span data-ttu-id="cea04-170">Wenn Sie in einer anderen Codezeile anhalten, drücken Sie die Skriptausführung fort **setzen,** ![ ][ImageResumeIcon] bis Sie die richtige Zeile angehalten haben.</span><span class="sxs-lookup"><span data-stu-id="cea04-170">If you pause on a different line of code, press **Resume Script Execution** ![Resume Script Execution][ImageResumeIcon] until you pause on the correct line.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="cea04-171">Wenn Sie in einer anderen Zeile angehalten haben, verfügen Sie über eine Browser Erweiterung, die einen `click` Ereignis-Listener auf jeder besuchten Seite registriert.</span><span class="sxs-lookup"><span data-stu-id="cea04-171">If you paused on a different line, you have a browser extension that registers a `click` event listener on every page that you visit.</span></span>  <span data-ttu-id="cea04-172">Sie wurden im `click` Listener der Erweiterung angehalten.</span><span class="sxs-lookup"><span data-stu-id="cea04-172">You were paused in the `click` listener of the extension.</span></span>  <span data-ttu-id="cea04-173">Wenn Sie den InPrivate-Modus verwenden, um **private zu durchsuchen**, wodurch alle Erweiterungen deaktiviert werden, sehen Sie möglicherweise, dass Sie jedes Mal in der gewünschten Codezeile anhalten.</span><span class="sxs-lookup"><span data-stu-id="cea04-173">If you use InPrivate Mode to **browse in private**, which disables all extensions, you may see that you pause on the desired line of code every time.</span></span>  

<!--todo: add inprivate section when available -->  

<span data-ttu-id="cea04-174">**Ereignis-Listener-Haltepunkte** sind nur eine von vielen Arten von Haltepunkten, die in devtools verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="cea04-174">**Event Listener Breakpoints** are just one of many types of breakpoints available in DevTools.</span></span>  <span data-ttu-id="cea04-175">Es lohnt sich, alle unterschiedlichen Typen zu merken, denn jeder Typ hilft Ihnen letztendlich dabei, verschiedene Szenarien so schnell wie möglich zu debuggen.</span><span class="sxs-lookup"><span data-stu-id="cea04-175">It is worth memorizing all the different types, because each type ultimately helps you debug different scenarios as quickly as possible.</span></span>  <!--See [Pause Your Code With Breakpoints][JSBreakpoints] to learn when and how to use each type.  -->  

## <span data-ttu-id="cea04-176">Schritt 4: Durchlaufen des Codes</span><span class="sxs-lookup"><span data-stu-id="cea04-176">Step 4: Step through the code</span></span>   

<span data-ttu-id="cea04-177">Eine häufige Ursache für Fehler ist, wenn ein Skript in der falschen Reihenfolge ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="cea04-177">One common cause of bugs is when a script runs in the wrong order.</span></span>  <span data-ttu-id="cea04-178">Wenn Sie den Code schrittweise durchlaufen, können Sie die Laufzeit des Codes, jeweils eine Zeile, durchlaufen und genau ermitteln, wo er in einer anderen Reihenfolge als erwartet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="cea04-178">Stepping through your code enables you to walk through the runtime of your code, one line at a time, and figure out exactly where it is running in a different order than you expected.</span></span>  <span data-ttu-id="cea04-179">Probieren Sie es jetzt aus:</span><span class="sxs-lookup"><span data-stu-id="cea04-179">Try it now:</span></span>  

1.  <span data-ttu-id="cea04-180">Klicken Sie auf Schritt **übernächsten** Funktionsaufruf ![ Schritt übernächsten Funktionsaufruf ][ImageOverIcon] .</span><span class="sxs-lookup"><span data-stu-id="cea04-180">Click **Step over next function call** ![Step over next function call][ImageOverIcon].</span></span>  <span data-ttu-id="cea04-181">DevTools führt den folgenden Code aus, ohne ihn zu betreten.</span><span class="sxs-lookup"><span data-stu-id="cea04-181">DevTools runs the following code without stepping into it.</span></span>  
    
    ```javascript
    if (inputsAreEmpty()) {
    ```  

    > [!NOTE]
    > <span data-ttu-id="cea04-182">DevTools überspringt einige Codezeilen.</span><span class="sxs-lookup"><span data-stu-id="cea04-182">DevTools skips a few lines of code.</span></span>  <span data-ttu-id="cea04-183">Dies liegt daran `inputsAreEmpty()` , dass die Auswertung als falsch ausgewertet wird, damit der Codeblock für die `if` Anweisung nicht ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="cea04-183">This is because `inputsAreEmpty()` evaluates as false, so the block of code for the `if` statement does not run.</span></span>  

1.  <span data-ttu-id="cea04-184">Klicken Sie im **Quellen** Panel von devtools auf **Schritt in nächster Funktionsaufruf** ![ Schritt in nächster Funktionsaufruf, ][ImageIntoIcon] um die Laufzeit der Funktion jeweils um eine Zeile zu durchlaufen `updateLabel()` .</span><span class="sxs-lookup"><span data-stu-id="cea04-184">On the **Sources** panel of DevTools, click **Step into next function call** ![Step into next function call][ImageIntoIcon] to step through the runtime of the `updateLabel()` function, one line at a time.</span></span>  

<span data-ttu-id="cea04-185">Das ist die grundlegende Idee, Code zu durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="cea04-185">That is the basic idea of stepping through code.</span></span>  <span data-ttu-id="cea04-186">Wenn Sie sich den Code in ansehen `get-started.js` , sehen Sie, dass der Fehler wahrscheinlich irgendwo in der `updateLabel()` Funktion enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="cea04-186">If you look at the code in `get-started.js`, you see that the bug is probably somewhere in the `updateLabel()` function.</span></span>  <span data-ttu-id="cea04-187">Anstatt jede Codezeile zu durchlaufen, können Sie eine andere Art von Haltepunkt verwenden, um den Code näher an der wahrscheinlichen Position des Fehlers anzuhalten.</span><span class="sxs-lookup"><span data-stu-id="cea04-187">Rather than stepping through every line of code, you may use another type of breakpoint to pause the code closer to the probable location of the bug.</span></span>  

## <span data-ttu-id="cea04-188">Schritt 5: Festlegen eines Haltepunkts für die Code Zeile</span><span class="sxs-lookup"><span data-stu-id="cea04-188">Step 5: Set a line-of-code breakpoint</span></span>   

<span data-ttu-id="cea04-189">Die am häufigsten verwendeten Haltepunkte sind die Code Haltepunkte.</span><span class="sxs-lookup"><span data-stu-id="cea04-189">Line-of-code breakpoints are the most common type of breakpoint.</span></span>  <span data-ttu-id="cea04-190">Wenn Sie die spezifische Codezeile erhalten, die Sie anhalten möchten, verwenden Sie einen Haltepunkt für die Code Zeile:</span><span class="sxs-lookup"><span data-stu-id="cea04-190">When you get the specific line of code that you want to pause on, use a line-of-code breakpoint:</span></span>  

1.  <span data-ttu-id="cea04-191">Sehen Sie sich die letzte Codezeile in an `updateLabel()` :</span><span class="sxs-lookup"><span data-stu-id="cea04-191">Look at the last line of code in `updateLabel()`:</span></span>  
    
    ```javascript
    label.textContent = addend1 + ' + ' + addend2 + ' = ' + sum;
    ```  
    
1.  <span data-ttu-id="cea04-192">Auf der linken Seite des Codes sehen Sie die Nummer der Zeile dieser bestimmten Codezeile, die **33**ist.</span><span class="sxs-lookup"><span data-stu-id="cea04-192">To the left of the code you see the line number of this particular line of code, which is **33**.</span></span>  <span data-ttu-id="cea04-193">Klicken Sie auf **33**.</span><span class="sxs-lookup"><span data-stu-id="cea04-193">Click on **33**.</span></span>  <span data-ttu-id="cea04-194">DevTools platziert ein rotes Symbol links von **33**.</span><span class="sxs-lookup"><span data-stu-id="cea04-194">DevTools puts a red icon to the left of **33**.</span></span>  <span data-ttu-id="cea04-195">Dies bedeutet, dass in dieser Zeile ein Haltepunkt für eine Codezeile vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="cea04-195">This means that there is a line-of-code breakpoint on this line.</span></span>  <span data-ttu-id="cea04-196">DevTools wird nun immer angehalten, bevor diese Codezeile ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="cea04-196">DevTools now always pauses before this line of code is run.</span></span>  
1.  <span data-ttu-id="cea04-197">Klicken Sie auf **Skript** Ausführung fortsetzen ![ ][ImageResumeIcon] .</span><span class="sxs-lookup"><span data-stu-id="cea04-197">Click **Resume script execution** ![Resume script execution][ImageResumeIcon].</span></span>  <span data-ttu-id="cea04-198">Das Skript wird weiterhin ausgeführt, bis es die Zeile 33 erreicht hat.</span><span class="sxs-lookup"><span data-stu-id="cea04-198">The script continues running until it reaches line 33.</span></span>  <span data-ttu-id="cea04-199">In den Zeilen 30, 31 und 32 druckt devtools die Werte von `addend1` , `addend2` und `sum` rechts neben dem Semikolon auf jeder Zeile aus.</span><span class="sxs-lookup"><span data-stu-id="cea04-199">On lines 30, 31, and 32, DevTools prints out the values of `addend1`, `addend2`, and `sum` to the right of the semi-colon on each line.</span></span>  
    
    > ##### <span data-ttu-id="cea04-200">Abbildung6</span><span class="sxs-lookup"><span data-stu-id="cea04-200">Figure 6</span></span>  
    > <span data-ttu-id="cea04-201">DevTools hält auf dem Zeile-zu-Code-Haltepunkt in Zeile 32</span><span class="sxs-lookup"><span data-stu-id="cea04-201">DevTools pauses on the line-of-code breakpoint on line 32</span></span>  
    > ![DevTools hält auf dem Zeile-zu-Code-Haltepunkt in Zeile 32][ImageJSLineOfCodeBreakpoint]  

## <span data-ttu-id="cea04-203">Schritt 6: Überprüfen von Variablenwerten</span><span class="sxs-lookup"><span data-stu-id="cea04-203">Step 6: Check variable values</span></span>   

<span data-ttu-id="cea04-204">Die Werte von `addend1` , `addend2` und `sum` verdächtig aussehen.</span><span class="sxs-lookup"><span data-stu-id="cea04-204">The values of `addend1`, `addend2`, and `sum` look suspicious.</span></span>  <span data-ttu-id="cea04-205">Sie werden in Anführungszeichen eingeschlossen, was bedeutet, dass es sich um Zeichenfolgen handelt.</span><span class="sxs-lookup"><span data-stu-id="cea04-205">They are wrapped in quotes, which means that they are strings.</span></span>  <span data-ttu-id="cea04-206">Dies ist eine gute Hypothese, in der die Ursache des Fehlers erläutert wird.</span><span class="sxs-lookup"><span data-stu-id="cea04-206">This is a good hypothesis for the explaining the cause of the bug.</span></span>  <span data-ttu-id="cea04-207">Jetzt ist es an der Zeit, weitere Informationen zu sammeln.</span><span class="sxs-lookup"><span data-stu-id="cea04-207">Now it is time to gather more information.</span></span>  <span data-ttu-id="cea04-208">DevTools bietet eine Vielzahl von Tools für die Untersuchung von Variablenwerten.</span><span class="sxs-lookup"><span data-stu-id="cea04-208">DevTools provides a lot of tools for examining variable values.</span></span>  

### <span data-ttu-id="cea04-209">Methode 1: Bereichs Bereich</span><span class="sxs-lookup"><span data-stu-id="cea04-209">Method 1: The Scope pane</span></span>   

<span data-ttu-id="cea04-210">Wenn Sie in einer Codezeile anhalten, zeigt der **Bereich** Bereich an, welche lokalen und globalen Variablen aktuell definiert sind, zusammen mit dem Wert der einzelnen Variablen.</span><span class="sxs-lookup"><span data-stu-id="cea04-210">When you pause on a line of code, the **Scope** pane shows you what local and global variables are currently defined, along with the value of each variable.</span></span>  <span data-ttu-id="cea04-211">Darüber hinaus werden ggf. Schließ Variablen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="cea04-211">It also shows closure variables, when applicable.</span></span>  <span data-ttu-id="cea04-212">Doppelklicken Sie auf einen Variablenwert, um ihn zu bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="cea04-212">Double-click a variable value to edit it.</span></span>  <span data-ttu-id="cea04-213">Wenn Sie nicht in einer Codezeile angehalten werden, ist der **Bereich** Bereich leer.</span><span class="sxs-lookup"><span data-stu-id="cea04-213">When you are not paused on a line of code, the **Scope** pane is empty.</span></span>  

> ##### <span data-ttu-id="cea04-214">Abbildung7</span><span class="sxs-lookup"><span data-stu-id="cea04-214">Figure 7</span></span>  
> <span data-ttu-id="cea04-215">**Bereichs** Bereich</span><span class="sxs-lookup"><span data-stu-id="cea04-215">The **Scope** pane</span></span>  
> ![Bereichs Bereich][ImageJSScope]  

### <span data-ttu-id="cea04-217">Methode 2: Überwachen von Ausdrücken</span><span class="sxs-lookup"><span data-stu-id="cea04-217">Method 2: Watch Expressions</span></span>   

<span data-ttu-id="cea04-218">Auf der Registerkarte " **Überwachungsausdrücke** " können Sie die Werte von Variablen über einen Zeitraum überwachen.</span><span class="sxs-lookup"><span data-stu-id="cea04-218">The **Watch Expressions** tab lets you monitor the values of variables over time.</span></span>  <span data-ttu-id="cea04-219">Wie der Name schon sagt, sind Watch-Ausdrücke nicht nur auf Variablen limitiert.</span><span class="sxs-lookup"><span data-stu-id="cea04-219">As the name implies, Watch Expressions are not just limited to variables.</span></span>  <span data-ttu-id="cea04-220">Sie können jeden gültigen JavaScript-Ausdruck in einem Überwachungsausdruck speichern.</span><span class="sxs-lookup"><span data-stu-id="cea04-220">You are able to store any valid JavaScript expression in a Watch Expression.</span></span>  <span data-ttu-id="cea04-221">Probieren Sie es jetzt aus:</span><span class="sxs-lookup"><span data-stu-id="cea04-221">Try it now:</span></span>  

1.  <span data-ttu-id="cea04-222">Klicken Sie auf die Registerkarte über **Wachen** .</span><span class="sxs-lookup"><span data-stu-id="cea04-222">Click the **Watch** tab.</span></span>  
1.  <span data-ttu-id="cea04-223">Klicken Sie auf **Ausdrucks** Ausdruck ![ Hinzufügen ][ImageAddIcon] .</span><span class="sxs-lookup"><span data-stu-id="cea04-223">Click **Add Expression** ![Add Expression][ImageAddIcon].</span></span>  
1.  <span data-ttu-id="cea04-224">Geben Sie `typeof sum` ein.</span><span class="sxs-lookup"><span data-stu-id="cea04-224">Type `typeof sum`.</span></span>  
1.  <span data-ttu-id="cea04-225">Drücken Sie `Enter` .</span><span class="sxs-lookup"><span data-stu-id="cea04-225">Press `Enter`.</span></span>  <span data-ttu-id="cea04-226">DevTools wird angezeigt `typeof sum: "string"` .</span><span class="sxs-lookup"><span data-stu-id="cea04-226">DevTools shows `typeof sum: "string"`.</span></span>  <span data-ttu-id="cea04-227">Der Wert rechts neben dem Doppelpunkt ist das Ergebnis des Überwachungsausdrucks.</span><span class="sxs-lookup"><span data-stu-id="cea04-227">The value to the right of the colon is the result of your Watch Expression.</span></span>  

> [!NOTE]
> <span data-ttu-id="cea04-228">Im Bereich "Überwachungsausdruck" \ (unten rechts \) in [Abbildung 8](#figure-8)wird der `typeof sum` Überwachungsausdruck angezeigt.</span><span class="sxs-lookup"><span data-stu-id="cea04-228">In the Watch Expression pane \(bottom-right\) in [Figure 8](#figure-8), the `typeof sum` Watch Expression is displayed.</span></span>  <span data-ttu-id="cea04-229">Wenn Ihr devtools-Fenster groß ist, befindet sich der Bereich "Überwachungsausdruck" auf der rechten Seite oberhalb des Bereichs " **Ereignis-Listener-Haltepunkte** ".</span><span class="sxs-lookup"><span data-stu-id="cea04-229">If your DevTools window is large, the Watch Expression pane is on the right above the **Event Listener Breakpoints** pane.</span></span>  

> ##### <span data-ttu-id="cea04-230">Abbildung8</span><span class="sxs-lookup"><span data-stu-id="cea04-230">Figure 8</span></span>  
> <span data-ttu-id="cea04-231">Der Bereich "Überwachungsausdruck"</span><span class="sxs-lookup"><span data-stu-id="cea04-231">The Watch Expression pane</span></span>  
> ![Der Bereich "Überwachungsausdruck"][ImageJSWatchExpression]  

<span data-ttu-id="cea04-233">Wie vermutet, `sum` wird als Zeichenfolge ausgewertet, wenn es sich um eine Zahl handelt.</span><span class="sxs-lookup"><span data-stu-id="cea04-233">As suspected, `sum` is being evaluated as a string, when it should be a number.</span></span>  <span data-ttu-id="cea04-234">Sie haben nun bestätigt, dass dies die Ursache des Fehlers ist.</span><span class="sxs-lookup"><span data-stu-id="cea04-234">You have now confirmed that this is the cause of the bug.</span></span>  

### <span data-ttu-id="cea04-235">Methode 3: die Konsole</span><span class="sxs-lookup"><span data-stu-id="cea04-235">Method 3: The Console</span></span>   

<span data-ttu-id="cea04-236">Neben der Anzeige von `console.log()` Nachrichten können Sie auch die Konsole verwenden, um willkürliche JavaScript-Anweisungen auszuwerten.</span><span class="sxs-lookup"><span data-stu-id="cea04-236">In addition to viewing `console.log()` messages, you may also use the Console to evaluate arbitrary JavaScript statements.</span></span>  <span data-ttu-id="cea04-237">Im Hinblick auf das Debuggen können Sie die Konsole verwenden, um mögliche Fehlerkorrekturen zu testen.</span><span class="sxs-lookup"><span data-stu-id="cea04-237">In terms of debugging, you may use the Console to test out potential fixes for bugs.</span></span>  <span data-ttu-id="cea04-238">Probieren Sie es jetzt aus:</span><span class="sxs-lookup"><span data-stu-id="cea04-238">Try it now:</span></span>  

1.  <span data-ttu-id="cea04-239">Wenn das Konsolen Fach nicht geöffnet ist, drücken Sie, `Escape` um es zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="cea04-239">If you do not have the Console drawer open, press `Escape` to open it.</span></span>  <span data-ttu-id="cea04-240">Sie wird unten im devtools-Fenster geöffnet.</span><span class="sxs-lookup"><span data-stu-id="cea04-240">It opens at the bottom of your DevTools window.</span></span>  
1.  <span data-ttu-id="cea04-241">Geben Sie in der Konsole `parseInt(addend1) + parseInt(addend2)` .</span><span class="sxs-lookup"><span data-stu-id="cea04-241">In the Console, type `parseInt(addend1) + parseInt(addend2)`.</span></span>  <span data-ttu-id="cea04-242">Diese Anweisung funktioniert, weil Sie in einer Codezeile angehalten werden `addend1` und `addend2` sich im Bereich befinden.</span><span class="sxs-lookup"><span data-stu-id="cea04-242">This statement works because you are paused on a line of code where `addend1` and `addend2` are in scope.</span></span>  
1.  <span data-ttu-id="cea04-243">Drücken Sie `Enter` .</span><span class="sxs-lookup"><span data-stu-id="cea04-243">Press `Enter`.</span></span>  <span data-ttu-id="cea04-244">DevTools wertet die Anweisung aus und gibt das `6` Ergebnis aus, das Sie erwarten, dass die Demo erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="cea04-244">DevTools evaluates the statement and prints out `6`, which is the result you expect the demo to produce.</span></span>  

> ##### <span data-ttu-id="cea04-245">Abbildung 9</span><span class="sxs-lookup"><span data-stu-id="cea04-245">Figure 9</span></span>  
> <span data-ttu-id="cea04-246">Der Konsolen Einzug nach der Auswertung</span><span class="sxs-lookup"><span data-stu-id="cea04-246">The Console drawer, after evaluating</span></span> `parseInt(addend1) + parseInt(addend2)`  
> ![Der Konsolen Einzug nach der Auswertung von parseInt (addend1) + parseInt (addend2)][ImageJSConsoleEvaluated]  

## <span data-ttu-id="cea04-248">Schritt 7: Anwenden einer Korrektur</span><span class="sxs-lookup"><span data-stu-id="cea04-248">Step 7: Apply a fix</span></span>   

<span data-ttu-id="cea04-249">Wenn Sie eine Lösung für den Fehler gefunden haben, versuchen Sie, Ihr Problem zu beheben, indem Sie den Code bearbeiten und die Demo erneut ausführen.</span><span class="sxs-lookup"><span data-stu-id="cea04-249">If you find a fix for the bug, try out your fix by editing the code and re-running the demo.</span></span>  <span data-ttu-id="cea04-250">Sie müssen devtools nicht mehr belassen, um den Fix anzuwenden.</span><span class="sxs-lookup"><span data-stu-id="cea04-250">You do not need to leave DevTools to apply the fix.</span></span>  <span data-ttu-id="cea04-251">Sie können JavaScript-Code direkt in der devtools-Benutzeroberfläche bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="cea04-251">You are able to edit JavaScript code directly within the DevTools UI.</span></span>  <span data-ttu-id="cea04-252">Probieren Sie es jetzt aus:</span><span class="sxs-lookup"><span data-stu-id="cea04-252">Try it now:</span></span>  

1.  <span data-ttu-id="cea04-253">Klicken Sie auf **Skript** Ausführung fortsetzen ![ ][ImageResumeIcon] .</span><span class="sxs-lookup"><span data-stu-id="cea04-253">Click **Resume script execution** ![Resume script execution][ImageResumeIcon].</span></span>  
1.  <span data-ttu-id="cea04-254">Ersetzen Sie im **Code-Editor**Zeile 32, `var sum = addend1 + addend2` mit `var sum = parseInt(addend1) + parseInt(addend2)` .</span><span class="sxs-lookup"><span data-stu-id="cea04-254">In the **Code Editor**, replace line 32, `var sum = addend1 + addend2`, with `var sum = parseInt(addend1) + parseInt(addend2)`.</span></span>  
1.  <span data-ttu-id="cea04-255">Drücken Sie `Control` + `S` \ (Windows \) oder `Command` + `S` \ (macOS \), um die Änderung zu speichern.</span><span class="sxs-lookup"><span data-stu-id="cea04-255">Press `Control`+`S` \(Windows\) or `Command`+`S` \(macOS\) to save your change.</span></span>  
1.  <span data-ttu-id="cea04-256">Klicken Sie auf **Haltepunkte deaktivieren** ![ , um Haltepunkte zu deaktivieren ][ImageDeactivateIcon] .</span><span class="sxs-lookup"><span data-stu-id="cea04-256">Click **Deactivate breakpoints** ![Deactivate breakpoints][ImageDeactivateIcon].</span></span>  <span data-ttu-id="cea04-257">Es wechselt blau, um anzuzeigen, dass es aktiv ist.</span><span class="sxs-lookup"><span data-stu-id="cea04-257">It changes blue to indicate that it is active.</span></span>  <span data-ttu-id="cea04-258">Während dies eingestellt ist, ignoriert devtools alle von Ihnen gesetzten Haltepunkte.</span><span class="sxs-lookup"><span data-stu-id="cea04-258">While this is set, DevTools ignores any breakpoints you set.</span></span>  
1.  <span data-ttu-id="cea04-259">Probieren Sie die Demo mit unterschiedlichen Werten aus.</span><span class="sxs-lookup"><span data-stu-id="cea04-259">Try out the demo with different values.</span></span>  <span data-ttu-id="cea04-260">Die Demo wird nun korrekt berechnet.</span><span class="sxs-lookup"><span data-stu-id="cea04-260">The demo now calculates correctly.</span></span>  

> [!CAUTION]
> <span data-ttu-id="cea04-261">Dieser Workflow wendet nur einen Fix auf den Code an, der im Browser ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="cea04-261">This workflow only applies a fix to the code that is running in your browser.</span></span>  <span data-ttu-id="cea04-262">Der Code für alle Benutzer, die Ihre Seite besuchen, wird dadurch nicht behoben.</span><span class="sxs-lookup"><span data-stu-id="cea04-262">It does not fix the code for all users that visit your page.</span></span>  <span data-ttu-id="cea04-263">Dazu müssen Sie den Code korrigieren, der sich auf Ihren Servern befindet.</span><span class="sxs-lookup"><span data-stu-id="cea04-263">To do that, you need to fix the code that is on your servers.</span></span>  

## <span data-ttu-id="cea04-264">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="cea04-264">Next steps</span></span>   

<span data-ttu-id="cea04-265">Herzlichen Glückwunsch!</span><span class="sxs-lookup"><span data-stu-id="cea04-265">Congratulations!</span></span>  <span data-ttu-id="cea04-266">Sie wissen jetzt, wie Sie Microsoft Edge devtools beim Debuggen von JavaScript optimal nutzen können.</span><span class="sxs-lookup"><span data-stu-id="cea04-266">You now know how to make the most of Microsoft Edge DevTools when debugging JavaScript.</span></span>  <span data-ttu-id="cea04-267">Die Tools und Methoden, die Sie in diesem Lernprogramm gelernt haben, können Ihnen unzählige Stunden sparen.</span><span class="sxs-lookup"><span data-stu-id="cea04-267">The tools and methods you learned in this tutorial may save you countless hours.</span></span>  

<span data-ttu-id="cea04-268">In diesem Lernprogramm wurden nur zwei Möglichkeiten zum Festlegen von Haltepunkten gezeigt.</span><span class="sxs-lookup"><span data-stu-id="cea04-268">This tutorial only showed you two ways to set breakpoints.</span></span>  <span data-ttu-id="cea04-269">DevTools bietet viele weitere Möglichkeiten, einschließlich:</span><span class="sxs-lookup"><span data-stu-id="cea04-269">DevTools offers many other ways, including:</span></span>  

*   <span data-ttu-id="cea04-270">Bedingte Haltepunkte, die nur ausgelöst werden, wenn die von Ihnen bereitgestellte Bedingung wahr ist.</span><span class="sxs-lookup"><span data-stu-id="cea04-270">Conditional breakpoints that are only triggered when the condition that you provide is true.</span></span>  
*   <span data-ttu-id="cea04-271">Haltepunkte für abgefangene oder nicht abgefangene Ausnahmen</span><span class="sxs-lookup"><span data-stu-id="cea04-271">Breakpoints on caught or uncaught exceptions.</span></span>  
*   <span data-ttu-id="cea04-272">XMLHttpRequest-Haltepunkte, die ausgelöst werden, wenn die angeforderte URL einer von Ihnen bereitgestellten Teilzeichenfolge entspricht.</span><span class="sxs-lookup"><span data-stu-id="cea04-272">XHR breakpoints that are triggered when the requested URL matches a substring that you provide.</span></span>  

<!-- See [Pause Your Code With Breakpoints][JSBreakpoints] to learn when and how to use each type.  -->  

<!--There are a couple of code stepping controls that were not explained in this tutorial.  See [Step over line of code][JSReferenceStepping] to learn more.  -->  

 



<!-- image links -->  

[ImageAddIcon]: /microsoft-edge/devtools-guide-chromium/media/add-expression-icon.msft.png  
[ImageDeactivateIcon]: /microsoft-edge/devtools-guide-chromium/media/deactivate-breakpoints-button-icon.msft.png  
[ImageExpandIcon]: /microsoft-edge/devtools-guide-chromium/media/expand-icon.msft.png  
[ImageIntoIcon]: /microsoft-edge/devtools-guide-chromium/media/step-into-icon.msft.png  
[ImageOverIcon]: /microsoft-edge/devtools-guide-chromium/media/step-over-icon.msft.png  
[ImageResumeIcon]: /microsoft-edge/devtools-guide-chromium/media/resume-script-run-icon.msft.png  

[ImageJSBugs]: /microsoft-edge/devtools-guide-chromium/media/javascript-js-demo-bad.msft.png "Abbildung 1: das Ergebnis von 5 + 1 ist 51, sollte aber 6 sein."  
[ImageJSConsole]: /microsoft-edge/devtools-guide-chromium/media/javascript-console-empty.msft.png "Abbildung 2: die Konsolen Leiste"  
[ImageJSSources]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-sections.msft.png "Abbildung 3: das Quellen Panel"  
[ImageJSSourcesAnnotated]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-sections-annotated.msft.png "Abbildung 4: die drei Teile der Benutzeroberfläche des Quellen Panels"  
[ImageJSClickCheckbox]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-event-listener-breakpoint-mouse-click.msft.png "Abbildung 5: das Kontrollkästchen "klicken" ist aktiviert"  
[ImageJSLineOfCodeBreakpoint]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-breakpoint-paused.msft.png "Abbildung 6: devtools-Pausen auf dem Zeile-zu-Code-Haltepunkt in Zeile 32"  
[ImageJSScope]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-breakpoint-paused-scope.msft.png "Abbildung 7: Bereichs Bereich"  
[ImageJSWatchExpression]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-breakpoint-paused-watch.msft.png "Abbildung 8: der Bereich "Überwachungsausdruck""  
[ImageJSConsoleEvaluated]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-breakpoint-paused-console.msft.png "Der Konsolen Einzug nach der Auswertung von parseInt (addend1) + parseInt (addend2)"  

<!-- links -->  

<!--[JSBreakpoints]: breakpoints.md "JavaScript Breakpoints"  -->  
<!--[inPrivate]: https://support.alphabet.com/alphabet-browser/answer/95464  -->
[OpenDebugJSDemo]: https://microsoft-edge-chromium-devtools.glitch.me/debug-js/get-started.html "Demo öffnen"  
<!--[JSReferenceStepping]: reference.md#stepping "Reference Stepping"  -->

> [!NOTE]
> <span data-ttu-id="cea04-283">Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="cea04-283">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="cea04-284">Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/javascript/index) und wird von [Kayce Basken][KayceBasques] (Technical Writer, Chrome devtools \ & Lighthouse \) erstellt.</span><span class="sxs-lookup"><span data-stu-id="cea04-284">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/javascript/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
<span data-ttu-id="cea04-286">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="cea04-286">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
