---
title: JavaScript-Debug-Referenz
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/18/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Web-Entwicklung, F12-Tools, devtools
ms.openlocfilehash: 1d361bb39523e9b039500f46da54e60b82adbda6
ms.sourcegitcommit: ecdc4287fa25a18cb4ddcaf43fcce3b396c3314c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/17/2020
ms.locfileid: "10581740"
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







# <span data-ttu-id="2ca87-103">JavaScript-Debug-Referenz</span><span class="sxs-lookup"><span data-stu-id="2ca87-103">JavaScript Debugging Reference</span></span>   



<span data-ttu-id="2ca87-104">Entdecken Sie neue Debugging-Workflows mit dieser umfassenden Referenz zu den Microsoft Edge DevTools-Debugging-Features.</span><span class="sxs-lookup"><span data-stu-id="2ca87-104">Discover new debugging workflows with this comprehensive reference of Microsoft Edge DevTools debugging features.</span></span>  

<span data-ttu-id="2ca87-105">Informationen zu den Grundlagen des Debuggens finden Sie unter [Erste Schritte beim Debuggen von JavaScript in Microsoft Edge devtools][DevToolsJavascriptGetStarted] .</span><span class="sxs-lookup"><span data-stu-id="2ca87-105">See [Get Started With Debugging JavaScript In Microsoft Edge DevTools][DevToolsJavascriptGetStarted] to learn the basics of debugging.</span></span>  

## <span data-ttu-id="2ca87-106">Anhalten von Code mit Haltepunkten</span><span class="sxs-lookup"><span data-stu-id="2ca87-106">Pause code with breakpoints</span></span>   

<span data-ttu-id="2ca87-107">Legen Sie einen Haltepunkt fest, damit Sie den Code in der Mitte der Laufzeit anhalten können.</span><span class="sxs-lookup"><span data-stu-id="2ca87-107">Set a breakpoint so that you are able to pause your code in the middle of the runtime.</span></span>  

<span data-ttu-id="2ca87-108">Informationen zum Festlegen von Haltepunkten finden Sie unter [Anhalten des Codes mit Haltepunkten][DevToolsJavascriptBreakpoints] .</span><span class="sxs-lookup"><span data-stu-id="2ca87-108">See [Pause Your Code With Breakpoints][DevToolsJavascriptBreakpoints] to learn how to set breakpoints.</span></span>  

[DevToolsJavascriptBreakpoints]: breakpoints.md "Anhalten des Codes mit Haltepunkten in Microsoft Edge devtools"  

## <span data-ttu-id="2ca87-110">Schritt-für-Schritt-Code</span><span class="sxs-lookup"><span data-stu-id="2ca87-110">Step through code</span></span>   

<span data-ttu-id="2ca87-111">Nachdem der Code angehalten wurde, führen Sie ihn schrittweise durch, und untersuchen Sie die Fluss-und Eigenschaftswerte auf dem Weg.</span><span class="sxs-lookup"><span data-stu-id="2ca87-111">Once your code is paused, step through it, one line at a time, investigating control flow and property values along the way.</span></span>  

### <span data-ttu-id="2ca87-112">Schritt über Codezeile</span><span class="sxs-lookup"><span data-stu-id="2ca87-112">Step over line of code</span></span>   

<span data-ttu-id="2ca87-113">Wenn Sie in einer Codezeile mit einer Funktion angehalten wurden, die für das Problem, das Sie Debuggen, nicht relevant ist, klicken Sie auf das Symbol **Schritt** überschritt, ![ ][ImageStepOverIcon] um die Funktion auszuführen, ohne Sie zu betreten.</span><span class="sxs-lookup"><span data-stu-id="2ca87-113">When paused on a line of code containing a function that is not relevant to the problem you are debugging, click on the **Step over** ![Step over][ImageStepOverIcon] icon to run the function without stepping into it.</span></span>  

> ##### <span data-ttu-id="2ca87-114">Abbildung1</span><span class="sxs-lookup"><span data-stu-id="2ca87-114">Figure 1</span></span>  
> <span data-ttu-id="2ca87-115">Auswählen des **Schritts**</span><span class="sxs-lookup"><span data-stu-id="2ca87-115">Selecting **Step over**</span></span>  
> ![Auswählen des Schritts][ImageSelectingStepOver]  

<span data-ttu-id="2ca87-117">Nehmen wir beispielsweise an, dass Sie den folgenden Code Debuggen:</span><span class="sxs-lookup"><span data-stu-id="2ca87-117">For example, suppose you are debugging the following code:</span></span>  

```javascript
function updateHeader() {
    var day = new Date().getDay();
    var name = getName(); // A
    updateName(name); // D
}
function getName() {
    var name = app.first + ' ' + app.last; // B
    return name; // C
}
```  

<span data-ttu-id="2ca87-118">Sie sind angehalten `A` .</span><span class="sxs-lookup"><span data-stu-id="2ca87-118">You are paused on `A`.</span></span>  <span data-ttu-id="2ca87-119">Wenn Sie den **Schritt über**drücken, führt devtools den gesamten Code in der Funktion aus, die Sie überschreiten, also `B` und `C` .</span><span class="sxs-lookup"><span data-stu-id="2ca87-119">By pressing **Step over**, DevTools runs all the code in the function that you are stepping over, which is `B` and `C`.</span></span>  <span data-ttu-id="2ca87-120">DevTools wird dann angehalten `D` .</span><span class="sxs-lookup"><span data-stu-id="2ca87-120">DevTools then pauses on `D`.</span></span>  

### <span data-ttu-id="2ca87-121">Schritt in Codezeile</span><span class="sxs-lookup"><span data-stu-id="2ca87-121">Step into line of code</span></span>   

<span data-ttu-id="2ca87-122">Wenn Sie in einer Codezeile mit einem Funktionsaufruf angehalten haben, der sich auf das Problem bezieht, das Sie Debuggen, klicken Sie auf das Symbol **Schritt** in ![ Schritt, ][ImageStepIntoIcon] um diese Funktion weiter zu untersuchen.</span><span class="sxs-lookup"><span data-stu-id="2ca87-122">When paused on a line of code containing a function call that is related to the problem you are debugging, click on the **Step into** ![Step into][ImageStepIntoIcon] icon to investigate that function further.</span></span>  

> ##### <span data-ttu-id="2ca87-123">Abbildung2</span><span class="sxs-lookup"><span data-stu-id="2ca87-123">Figure 2</span></span>  
> <span data-ttu-id="2ca87-124">Auswählen von **Schritt in**</span><span class="sxs-lookup"><span data-stu-id="2ca87-124">Selecting **Step into**</span></span>  
> ![Auswählen von Schritt in][ImageSelectingStepInto]  

<span data-ttu-id="2ca87-126">Nehmen wir beispielsweise an, dass Sie den folgenden Code Debuggen:</span><span class="sxs-lookup"><span data-stu-id="2ca87-126">For example, suppose you are debugging the following code:</span></span>  

```javascript
function updateHeader() {
    var day = new Date().getDay();
    var name = getName(); // A
    updateName(name);
}
function getName() {
    var name = app.first + ' ' + app.last; // B
    return name;
}
```  

<span data-ttu-id="2ca87-127">Sie sind angehalten `A` .</span><span class="sxs-lookup"><span data-stu-id="2ca87-127">You are paused on `A`.</span></span>  <span data-ttu-id="2ca87-128">Durch Drücken von **Schritt in**führt devtools diese Codezeile aus und hält dann an `B` .</span><span class="sxs-lookup"><span data-stu-id="2ca87-128">By pressing **Step into**, DevTools runs this line of code, then pauses on `B`.</span></span>  

### <span data-ttu-id="2ca87-129">Schritt außerhalb der Codezeile</span><span class="sxs-lookup"><span data-stu-id="2ca87-129">Step out of line of code</span></span>   

<span data-ttu-id="2ca87-130">Wenn Sie innerhalb einer Funktion angehalten haben, die nicht mit dem Problem in Verbindung steht, das Sie Debuggen, klicken Sie auf das Symbol " **Schritt** aus", ![ ][ImageStepOutIcon] um den restlichen Code der Funktion auszuführen.</span><span class="sxs-lookup"><span data-stu-id="2ca87-130">When paused inside of a function that is not related to the problem you are debugging, click on the **Step out** ![Step out][ImageStepOutIcon] icon to run the rest of the code of the function.</span></span>  

> ##### <span data-ttu-id="2ca87-131">Abbildung 3</span><span class="sxs-lookup"><span data-stu-id="2ca87-131">Figure 3</span></span>  
> <span data-ttu-id="2ca87-132">Auswählen **von "Schritt aus** "</span><span class="sxs-lookup"><span data-stu-id="2ca87-132">Selecting **Step out**</span></span>  
> ![Auswählen von "Schritt aus"][ImageSelectingStepOut]  

<span data-ttu-id="2ca87-134">Nehmen wir beispielsweise an, dass Sie den folgenden Code Debuggen:</span><span class="sxs-lookup"><span data-stu-id="2ca87-134">For example, suppose you are debugging the following code:</span></span>  

```javascript
function updateHeader() {
    var day = new Date().getDay();
    var name = getName();
    updateName(name); // C
}
function getName() {
    var name = app.first + ' ' + app.last; // A
    return name; // B
}
```  

<span data-ttu-id="2ca87-135">Sie sind angehalten `A` .</span><span class="sxs-lookup"><span data-stu-id="2ca87-135">You are paused on `A`.</span></span>  <span data-ttu-id="2ca87-136">Durch Drücken von **Step out**führt devtools den restlichen Code in aus `getName()` , der sich nur `B` in diesem Beispiel befindet, und hält dann an `C` .</span><span class="sxs-lookup"><span data-stu-id="2ca87-136">By pressing **Step out**, DevTools runs the rest of the code in `getName()`, which is just `B` in this example, and then pauses on `C`.</span></span>  

### <span data-ttu-id="2ca87-137">Ausführen des gesamten Codes bis zu einer bestimmten Zeile</span><span class="sxs-lookup"><span data-stu-id="2ca87-137">Run all code up to a specific line</span></span>   

<span data-ttu-id="2ca87-138">Wenn Sie eine Long-Funktion Debuggen, gibt es möglicherweise viel Code, der sich nicht auf das zu debuggende Problem bezieht.</span><span class="sxs-lookup"><span data-stu-id="2ca87-138">When debugging a long function, there may be a lot of code that is not related to the problem you are debugging.</span></span>  

<span data-ttu-id="2ca87-139">Sie können alle Zeilen durchlaufen, aber das ist mühsam.</span><span class="sxs-lookup"><span data-stu-id="2ca87-139">You may choose to step through all the lines, but that is tedious.</span></span>  <span data-ttu-id="2ca87-140">Sie können festlegen, dass in der Zeile, in der Sie interessiert sind, ein Haltepunkt für die Codezeile gesetzt wird, und klicken Sie dann auf das Symbol zum Fortsetzen der Skript **Ausführung** ![ fortsetzen ][ImageResumeScriptExecutionIcon] , aber es gibt einen schnelleren Weg.</span><span class="sxs-lookup"><span data-stu-id="2ca87-140">You may choose to set a line-of-code breakpoint on the line in which you are interested and then click on the **Resume Script Execution** ![Resume Script Execution][ImageResumeScriptExecutionIcon] icon, but there is a faster way.</span></span>  

<span data-ttu-id="2ca87-141">Klicken Sie mit der rechten Maustaste auf die Codezeile, für die Sie sich interessieren, und wählen Sie **hier weiter**.</span><span class="sxs-lookup"><span data-stu-id="2ca87-141">Right-click the line of code in which you are interested, and select **Continue to here**.</span></span>  <span data-ttu-id="2ca87-142">DevTools führt den gesamten Code bis zu diesem Punkt aus und hält dann in dieser Zeile an.</span><span class="sxs-lookup"><span data-stu-id="2ca87-142">DevTools runs all of the code up to that point, and then pauses on that line.</span></span>  

> ##### <span data-ttu-id="2ca87-143">Abbildung4</span><span class="sxs-lookup"><span data-stu-id="2ca87-143">Figure 4</span></span>  
> <span data-ttu-id="2ca87-144">Auswählen **von weiter hier**</span><span class="sxs-lookup"><span data-stu-id="2ca87-144">Selecting **Continue to here**</span></span>  
> ![Auswählen von weiter hier][ImageSelectingContinueToHere]  

### <span data-ttu-id="2ca87-146">Starten der obersten Funktion der Aufrufliste</span><span class="sxs-lookup"><span data-stu-id="2ca87-146">Restart the top function of the call stack</span></span>   

<span data-ttu-id="2ca87-147">Wenn Sie in einer Codezeile angehalten sind, klicken Sie mit der rechten Maustaste auf eine beliebige Stelle im Bereich **Anrufliste** , und wählen Sie **Frame neu starten** aus, um in der ersten Zeile der obersten Funktion in der Aufrufliste zu pausieren.</span><span class="sxs-lookup"><span data-stu-id="2ca87-147">While paused on a line of code, right-click anywhere in the **Call Stack** pane and select **Restart Frame** to pause on the first line of the top function in your call stack.</span></span>  <span data-ttu-id="2ca87-148">Die oberste Funktion ist die letzte aufgerufene Funktion.</span><span class="sxs-lookup"><span data-stu-id="2ca87-148">The top function is the last function that was called.</span></span>  

<span data-ttu-id="2ca87-149">Nehmen wir beispielsweise an, dass Sie den folgenden Code durchlaufen:</span><span class="sxs-lookup"><span data-stu-id="2ca87-149">For example, suppose you are stepping through the following code:</span></span>  

```javascript
function factorial(n) {
    var product = 0; // B
    for (var i = 1; i <= n; i++) {
      product += i;
    }
    return product; // A
}
```  

<span data-ttu-id="2ca87-150">Sie sind angehalten `A` .</span><span class="sxs-lookup"><span data-stu-id="2ca87-150">You are paused on `A`.</span></span>  <span data-ttu-id="2ca87-151">Nachdem Sie auf **Frame neu starten**geklickt haben, sollten Sie angehalten werden `B` , ohne einen Haltepunkt festzulegen oder die **Ausführung von Skript Fortsetzung**zu drücken.</span><span class="sxs-lookup"><span data-stu-id="2ca87-151">After clicking **Restart Frame**, you should be paused on `B`, without ever setting a breakpoint or pressing **Resume script execution**.</span></span>  

> ##### <span data-ttu-id="2ca87-152">Abbildung5</span><span class="sxs-lookup"><span data-stu-id="2ca87-152">Figure 5</span></span>  
> <span data-ttu-id="2ca87-153">Auswählen von " **Frame neu starten** "</span><span class="sxs-lookup"><span data-stu-id="2ca87-153">Selecting **Restart Frame**</span></span>  
> ![Auswählen von "Frame neu starten"][ImageSelectingRestartFrame]  

### <span data-ttu-id="2ca87-155">Fortsetzen der Skriptlaufzeit</span><span class="sxs-lookup"><span data-stu-id="2ca87-155">Resume script runtime</span></span>   

<span data-ttu-id="2ca87-156">Wenn Sie die Laufzeit nach einer Pause Ihres Skripts fortsetzen möchten, klicken Sie auf das Symbol Ausführungsskript **Ausführung fortsetzen** ![ ][ImageResumeScriptExecutionIcon] .</span><span class="sxs-lookup"><span data-stu-id="2ca87-156">To continue the runtime after a pause of your script, click on the **Resume Script Execution** ![Resume Script Execution][ImageResumeScriptExecutionIcon] icon.</span></span>  <span data-ttu-id="2ca87-157">DevTools führt das Skript bis zum nächsten Haltepunkt aus, sofern vorhanden.</span><span class="sxs-lookup"><span data-stu-id="2ca87-157">DevTools runs the script up until the next breakpoint, if any.</span></span>  

> ##### <span data-ttu-id="2ca87-158">Abbildung6</span><span class="sxs-lookup"><span data-stu-id="2ca87-158">Figure 6</span></span>  
> <span data-ttu-id="2ca87-159">Auswählen der **Skriptausführung fortsetzen**</span><span class="sxs-lookup"><span data-stu-id="2ca87-159">Selecting **Resume script execution**</span></span>  
> ![Auswählen der Skriptausführung fortsetzen][ImageSelectingResumeScriptExecution]  

#### <span data-ttu-id="2ca87-161">Erzwingen der Skriptlaufzeit</span><span class="sxs-lookup"><span data-stu-id="2ca87-161">Force script runtime</span></span>   

<span data-ttu-id="2ca87-162">Wenn Sie alle Haltepunkte ignorieren und die Ausführung des Skripts erzwingen möchten, klicken Sie auf **das** Symbol Ausführungsskript Ausführung fortsetzen, und halten Sie es gedrückt, ![ ][ImageResumeScriptExecutionIcon] und wählen Sie dann Skript Ausführungs **Force script execution** ![ Erzwingung erzwingen aus ][ImageForceScriptExecutionIcon] .</span><span class="sxs-lookup"><span data-stu-id="2ca87-162">To ignore all breakpoints and force your script to resume running, click and hold the **Resume Script Execution** ![Resume Script Execution][ImageResumeScriptExecutionIcon] icon and then select **Force script execution** ![Force script execution][ImageForceScriptExecutionIcon].</span></span>  

> ##### <span data-ttu-id="2ca87-163">Abbildung7</span><span class="sxs-lookup"><span data-stu-id="2ca87-163">Figure 7</span></span>  
> <span data-ttu-id="2ca87-164">Auswählen der **Erzwingung der Skriptausführung**</span><span class="sxs-lookup"><span data-stu-id="2ca87-164">Selecting **Force script execution**</span></span>  
> ![Auswählen der Erzwingung der Skriptausführung][ImageSelectingForceScriptExecution]  

### <span data-ttu-id="2ca87-166">Ändern des Thread Kontexts</span><span class="sxs-lookup"><span data-stu-id="2ca87-166">Change thread context</span></span>   

<span data-ttu-id="2ca87-167">Wenn Sie mit webarbeitern oder Dienst Mitarbeitern arbeiten, klicken Sie auf einen im Bereich **Threads** aufgelisteten Kontext, um zu diesem Kontext zu wechseln.</span><span class="sxs-lookup"><span data-stu-id="2ca87-167">When working with web workers or service workers, click on a context listed in the **Threads** pane to switch to that context.</span></span>  <span data-ttu-id="2ca87-168">Das blaue Pfeilsymbol steht für den aktuell ausgewählten Kontext.</span><span class="sxs-lookup"><span data-stu-id="2ca87-168">The blue arrow icon represents which context is currently selected.</span></span>  

> ##### <span data-ttu-id="2ca87-169">Abbildung8</span><span class="sxs-lookup"><span data-stu-id="2ca87-169">Figure 8</span></span>  
> <span data-ttu-id="2ca87-170">Der Bereich " **Threads** "</span><span class="sxs-lookup"><span data-stu-id="2ca87-170">The **Threads** pane</span></span>  
> ![Der Bereich "Threads"][ImageThreadsPane]  

<span data-ttu-id="2ca87-172">Nehmen wir beispielsweise an, dass Sie sowohl in Ihrem Hauptskript als auch in Ihrem Dienstmitarbeiter Skript an einem Haltepunkt angehalten werden.</span><span class="sxs-lookup"><span data-stu-id="2ca87-172">For example, suppose that you are paused on a breakpoint in both your main script and your service worker script.</span></span>  <span data-ttu-id="2ca87-173">Sie möchten die lokalen und globalen Eigenschaften für den Service Worker-Kontext anzeigen, aber der Bereich " **Quellen** " zeigt den Hauptskript Kontext an.</span><span class="sxs-lookup"><span data-stu-id="2ca87-173">You want to view the local and global properties for the service worker context, but the **Sources** panel is showing the main script context.</span></span>  <span data-ttu-id="2ca87-174">Durch Klicken auf den Eintrag Service Worker im Bereich **Threads** sollten Sie in der Lage sein, zu diesem Kontext zu wechseln.</span><span class="sxs-lookup"><span data-stu-id="2ca87-174">By clicking on the service worker entry in the **Threads** pane, you should be able to switch to that context.</span></span>  

## <span data-ttu-id="2ca87-175">Anzeigen und Bearbeiten von lokalen, Closure-und globalen Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2ca87-175">View and edit local, closure, and global properties</span></span>   

<span data-ttu-id="2ca87-176">Wenn Sie in einer Codezeile angehalten wurden, verwenden Sie **den Bereich Bereich,** um die Werte von Eigenschaften und Variablen in den Bereichen lokal, Closure und Global anzuzeigen und zu bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="2ca87-176">While paused on a line of code, use the **Scope** pane to view and edit the values of properties and variables in the local, closure, and global scopes.</span></span>  

*   <span data-ttu-id="2ca87-177">Doppelklicken Sie auf einen Eigenschaftswert, um ihn zu ändern.</span><span class="sxs-lookup"><span data-stu-id="2ca87-177">Double-click a property value to change it.</span></span>  
*   <span data-ttu-id="2ca87-178">Nicht aufzählbare Eigenschaften werden abgeblendet dargestellt.</span><span class="sxs-lookup"><span data-stu-id="2ca87-178">Non-enumerable properties are greyed out.</span></span>  

> ##### <span data-ttu-id="2ca87-179">Abbildung 9</span><span class="sxs-lookup"><span data-stu-id="2ca87-179">Figure 9</span></span>  
> <span data-ttu-id="2ca87-180">**Bereichs** Bereich</span><span class="sxs-lookup"><span data-stu-id="2ca87-180">The **Scope** pane</span></span>  
> ![Bereichs Bereich][ImageScopePane]  

## <span data-ttu-id="2ca87-182">Anzeigen der aktuellen Anrufliste</span><span class="sxs-lookup"><span data-stu-id="2ca87-182">View the current call stack</span></span>   

<span data-ttu-id="2ca87-183">Wenn Sie in einer Codezeile angehalten wurden, verwenden Sie den Bereich **Anrufliste** , um die Anrufliste anzuzeigen, die Sie zu diesem Punkt erhalten hat.</span><span class="sxs-lookup"><span data-stu-id="2ca87-183">While paused on a line of code, use the **Call Stack** pane to view the call stack that got you to this point.</span></span>  

<!--If you are working with async code, check the **Async** checkbox to enable async call stacks.  -->  

<span data-ttu-id="2ca87-184">Klicken Sie auf einen Eintrag, um zu der Codezeile zu springen, in der die Funktion aufgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="2ca87-184">Click on an entry to jump to the line of code where that function was called.</span></span>  <span data-ttu-id="2ca87-185">Das blaue Pfeilsymbol stellt dar, welche Funktion devtools derzeit markiert.</span><span class="sxs-lookup"><span data-stu-id="2ca87-185">The blue arrow icon represents which function DevTools is currently highlighting.</span></span>  

> ##### <span data-ttu-id="2ca87-186">Abbildung 10</span><span class="sxs-lookup"><span data-stu-id="2ca87-186">Figure 10</span></span>  
> <span data-ttu-id="2ca87-187">Der Bereich " **Anrufliste** "</span><span class="sxs-lookup"><span data-stu-id="2ca87-187">The **Call Stack** pane</span></span>  
> ![Der Bereich "Anrufliste"][ImageCallStackPane]  

> [!NOTE]
> <span data-ttu-id="2ca87-189">Wenn Sie nicht in einer Codezeile angehalten wurden, ist der Bereich **Aufrufliste** leer.</span><span class="sxs-lookup"><span data-stu-id="2ca87-189">When not paused on a line of code, the **Call Stack** pane is empty.</span></span>  

### <span data-ttu-id="2ca87-190">Kopieren einer Stapelüberwachung</span><span class="sxs-lookup"><span data-stu-id="2ca87-190">Copy stack trace</span></span>   

<!--
This should be moved to an "Export debug data" H2 section when there is enough content for that, but there is not right now, so it is here.
-->

<span data-ttu-id="2ca87-191">Klicken Sie mit der rechten Maustaste auf eine beliebige Stelle im Bereich **Anrufliste** , und wählen Sie **Stapelüberwachung kopieren** aus, um die aktuelle Aufrufliste in die Zwischenablage zu kopieren.</span><span class="sxs-lookup"><span data-stu-id="2ca87-191">Right-click anywhere in the **Call Stack** pane and select **Copy stack trace** to copy the current call stack to the clipboard.</span></span>  

> ##### <span data-ttu-id="2ca87-192">Abbildung 11</span><span class="sxs-lookup"><span data-stu-id="2ca87-192">Figure 11</span></span>  
> <span data-ttu-id="2ca87-193">Auswählen der **Stapelüberwachung kopieren**</span><span class="sxs-lookup"><span data-stu-id="2ca87-193">Selecting **Copy Stack Trace**</span></span>  
> ![Auswählen der Stapelüberwachung kopieren][ImageSelectingCopyStackTrace]  

<span data-ttu-id="2ca87-195">Nachfolgend finden Sie ein Beispiel für die Ausgabe:</span><span class="sxs-lookup"><span data-stu-id="2ca87-195">Below is an example of the output:</span></span>  

```javascript
getNumber1 (get-started.js:35)
inputsAreEmpty (get-started.js:22)
onClick (get-started.js:15)
```  

## <span data-ttu-id="2ca87-196">Ignorieren eines Skripts oder Musters von Skripts</span><span class="sxs-lookup"><span data-stu-id="2ca87-196">Ignore a script or pattern of scripts</span></span>  

<span data-ttu-id="2ca87-197">Markieren Sie ein Skript als Bibliothekscode, wenn Sie dieses Skript beim Debuggen ignorieren möchten.</span><span class="sxs-lookup"><span data-stu-id="2ca87-197">Mark a script as Library code when you want to ignore that script while debugging.</span></span>  <span data-ttu-id="2ca87-198">Wenn es sich um einen Bibliothekscode handelt, wird ein Skript im Bereich " **Aufrufliste** " verdeckt, und Sie gehen nie in die Funktionen des Skripts ein, wenn Sie den Code schrittweise durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="2ca87-198">When marked as Library code, a script is obscured in the **Call Stack** pane, and you never step into the functions of the script when you step through your code.</span></span>  

<span data-ttu-id="2ca87-199">Nehmen wir beispielsweise an, dass Sie diesen Code durchlaufen:</span><span class="sxs-lookup"><span data-stu-id="2ca87-199">For example, suppose you are stepping through this code:</span></span>  

```javascript
function animate() {
    prepare();
    lib.doFancyStuff(); // A
    render();
}
```  

`A` <span data-ttu-id="2ca87-200">ist eine drittanbieterbibliothek, der Sie vertrauen.</span><span class="sxs-lookup"><span data-stu-id="2ca87-200">is a third-party library that you trust.</span></span>  <span data-ttu-id="2ca87-201">Wenn Sie sicher sind, dass das Problem, das Sie Debuggen, nicht mit der Bibliothek von Drittanbietern verknüpft ist, ist es sinnvoll, das Skript als **Bibliothekscode**zu kennzeichnen.</span><span class="sxs-lookup"><span data-stu-id="2ca87-201">If you are confident that the problem you are debugging is not related to the third-party library, then it makes sense to mark the script as **Library code**.</span></span>  

### <span data-ttu-id="2ca87-202">Markieren eines Skripts als Bibliothekscode im Bereich "Editor"</span><span class="sxs-lookup"><span data-stu-id="2ca87-202">Mark a script as Library code from the Editor pane</span></span>  

<span data-ttu-id="2ca87-203">So markieren Sie ein Skript im **Editor** Bereich als **Bibliothekscode** :</span><span class="sxs-lookup"><span data-stu-id="2ca87-203">To mark a script as **Library code** from the **Editor** pane:</span></span>  

1.  <span data-ttu-id="2ca87-204">Öffnen Sie die Datei.</span><span class="sxs-lookup"><span data-stu-id="2ca87-204">Open the file.</span></span>  
1.  <span data-ttu-id="2ca87-205">Klicken Sie mit der rechten Maustaste auf eine beliebige Stelle.</span><span class="sxs-lookup"><span data-stu-id="2ca87-205">Right-click anywhere.</span></span>  
1.  <span data-ttu-id="2ca87-206">Wählen Sie **als Bibliothekscode markieren**aus.</span><span class="sxs-lookup"><span data-stu-id="2ca87-206">Select **Mark as Library code**.</span></span>  

> ##### <span data-ttu-id="2ca87-207">Abbildung 12</span><span class="sxs-lookup"><span data-stu-id="2ca87-207">Figure 12</span></span>  
> <span data-ttu-id="2ca87-208">Markieren eines Skripts als **Bibliothekscode** über den Bereich " **Editor** "</span><span class="sxs-lookup"><span data-stu-id="2ca87-208">Marking a script as **Library code** from the **Editor** pane</span></span>  
> ![Markieren eines Skripts als Bibliothekscode über den Bereich "Editor"][ImageMarkEditorPane]  

### <span data-ttu-id="2ca87-210">Markieren eines Skripts als Bibliothekscode aus dem Bereich "Anrufliste"</span><span class="sxs-lookup"><span data-stu-id="2ca87-210">Mark a script as Library code from the Call Stack pane</span></span>  

<span data-ttu-id="2ca87-211">So markieren Sie ein Skript aus dem Bereich " **Anrufliste** " als **Bibliothekscode** :</span><span class="sxs-lookup"><span data-stu-id="2ca87-211">To mark a script as **Library code** from the **Call Stack** pane:</span></span>  

1.  <span data-ttu-id="2ca87-212">Klicken Sie mit der rechten Maustaste auf eine Funktion aus dem Skript.</span><span class="sxs-lookup"><span data-stu-id="2ca87-212">Right-click on a function from the script.</span></span>  
1.  <span data-ttu-id="2ca87-213">Wählen Sie **als Bibliothekscode markieren**aus.</span><span class="sxs-lookup"><span data-stu-id="2ca87-213">Select **Mark as Library code**.</span></span>  

> ##### <span data-ttu-id="2ca87-214">Abbildung 13</span><span class="sxs-lookup"><span data-stu-id="2ca87-214">Figure 13</span></span>  
> <span data-ttu-id="2ca87-215">Markieren eines Skripts als **Bibliothekscode** aus dem Bereich " **Anrufliste** "</span><span class="sxs-lookup"><span data-stu-id="2ca87-215">Marking a script as **Library code** from the **Call Stack** pane</span></span>  
> ![Markieren eines Skripts als Bibliothekscode aus dem Bereich "Anrufliste"][ImageMarkCallStackPane]  

### <span data-ttu-id="2ca87-217">Markieren eines Skripts als Bibliothekscode aus Einstellungen</span><span class="sxs-lookup"><span data-stu-id="2ca87-217">Mark a script as Library code from Settings</span></span>  

<span data-ttu-id="2ca87-218">So markieren Sie ein einzelnes Skript oder Skript Muster aus den Einstellungen:</span><span class="sxs-lookup"><span data-stu-id="2ca87-218">To mark a single script or pattern of scripts from Settings:</span></span>  

1.  <span data-ttu-id="2ca87-219">Öffnen Sie [Einstellungen][DevToolsCustomize].</span><span class="sxs-lookup"><span data-stu-id="2ca87-219">Open [Settings][DevToolsCustomize].</span></span>  
1.  <span data-ttu-id="2ca87-220">Wechseln Sie zur Registerkarte **Bibliothekscode** .</span><span class="sxs-lookup"><span data-stu-id="2ca87-220">Go to the **Library code** tab.</span></span>  
1.  <span data-ttu-id="2ca87-221">Klicken Sie auf **Muster hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="2ca87-221">Click **Add pattern**.</span></span>  
1.  <span data-ttu-id="2ca87-222">Geben Sie den Skriptnamen oder ein Regex-Muster von Skriptnamen ein, das als **Bibliothekscode**markiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="2ca87-222">Enter the script name or a regex pattern of script names to mark as **Library code**.</span></span>  
1.  <span data-ttu-id="2ca87-223">Klicken Sie auf **Hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="2ca87-223">Click **Add**.</span></span>  

> ##### <span data-ttu-id="2ca87-224">Abbildung 14</span><span class="sxs-lookup"><span data-stu-id="2ca87-224">Figure 14</span></span>  
> <span data-ttu-id="2ca87-225">Markieren eines Skripts als **Bibliothekscode** aus Einstellungen</span><span class="sxs-lookup"><span data-stu-id="2ca87-225">Marking a script as **Library code** from Settings</span></span>  
> ![Markieren eines Skripts als Bibliothekscode aus Einstellungen][ImageMarkScriptSettings]  

## <span data-ttu-id="2ca87-227">Ausführen von Codeausschnitten von Debugcode auf jeder Seite</span><span class="sxs-lookup"><span data-stu-id="2ca87-227">Run snippets of debug code from any page</span></span>   

<span data-ttu-id="2ca87-228">Wenn Sie immer wieder denselben Debugcode in der Konsole ausführen, sollten Sie Snippets in Betracht gezogen sehen.</span><span class="sxs-lookup"><span data-stu-id="2ca87-228">If you find yourself running the same debug code in the Console over and over, consider Snippets.</span></span>  <span data-ttu-id="2ca87-229">Ausschnitte sind Lauf Zeit Skripte, die Sie in devtools erstellen, speichern und ausführen.</span><span class="sxs-lookup"><span data-stu-id="2ca87-229">Snippets are runtime scripts that you author, store, and run within DevTools.</span></span>  

<span data-ttu-id="2ca87-230">Weitere Informationen finden Sie unter [Ausführen von Codeausschnitten auf jeder Seite][DevToolsJavascriptSnippets] .</span><span class="sxs-lookup"><span data-stu-id="2ca87-230">See [Run Snippets of Code From Any Page][DevToolsJavascriptSnippets] to learn more.</span></span>  

## <span data-ttu-id="2ca87-231">Sehen Sie sich die Werte benutzerdefinierter JavaScript-Ausdrücke an</span><span class="sxs-lookup"><span data-stu-id="2ca87-231">Watch the values of custom JavaScript expressions</span></span>   

<span data-ttu-id="2ca87-232">Verwenden Sie den **Überwachungs** Bereich, um die Werte benutzerdefinierter Ausdrücke zu überwachen.</span><span class="sxs-lookup"><span data-stu-id="2ca87-232">Use the **Watch** pane to watch the values of custom expressions.</span></span>  <span data-ttu-id="2ca87-233">Sie können jeden gültigen JavaScript-Ausdruck sehen.</span><span class="sxs-lookup"><span data-stu-id="2ca87-233">You may watch any valid JavaScript expression.</span></span>  

> ##### <span data-ttu-id="2ca87-234">Abbildung 15</span><span class="sxs-lookup"><span data-stu-id="2ca87-234">Figure 15</span></span>  
> <span data-ttu-id="2ca87-235">Der **Überwachungs** Bereich</span><span class="sxs-lookup"><span data-stu-id="2ca87-235">The **Watch** pane</span></span>  
> ![Der Überwachungsbereich][ImageWatchPane]  

*   <span data-ttu-id="2ca87-237">Klicken Sie auf **Add Expression** das ![ Symbol zum Hinzufügen eines Ausdrucks hinzufügen ][ImageAddExpressionIcon] , um einen neuen Überwachungsausdruck zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="2ca87-237">Click on the **Add Expression** ![Add Expression][ImageAddExpressionIcon] icon to create a new watch expression.</span></span>  
*   <span data-ttu-id="2ca87-238">Klicken Sie auf **das Aktualisierungs** ![ Symbol Aktualisieren ][ImageRefreshIcon] , um die Werte aller vorhandenen Ausdrücke zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="2ca87-238">Click on the **Refresh** ![Refresh][ImageRefreshIcon] icon to refresh the values of all existing expressions.</span></span>  <span data-ttu-id="2ca87-239">Werte werden beim Durchlaufen des Codes automatisch aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="2ca87-239">Values automatically refresh while stepping through code.</span></span>  
*   <span data-ttu-id="2ca87-240">Zeigen Sie mit der Maus auf einen Ausdruck, und klicken Sie **auf das** Symbol Ausdrucks löschen Ausdruck löschen ![ ][ImageDeleteExpressionIcon] , um es zu löschen.</span><span class="sxs-lookup"><span data-stu-id="2ca87-240">Hover over an expression and click on the **Delete Expression** ![Delete Expression][ImageDeleteExpressionIcon] icon to delete it.</span></span>  

## <span data-ttu-id="2ca87-241">Erstellen einer lesbaren minimierte-Datei</span><span class="sxs-lookup"><span data-stu-id="2ca87-241">Make a minified file readable</span></span>   

<span data-ttu-id="2ca87-242">Klicken Sie auf das Symbol **Format** formatieren ![ ][ImageFormatIcon] , um eine minimierte-Datei menschlich lesbar zu machen.</span><span class="sxs-lookup"><span data-stu-id="2ca87-242">Click on the **Format** ![Format][ImageFormatIcon] icon to make a minified file human-readable.</span></span>  

> ##### <span data-ttu-id="2ca87-243">Abbildung 16</span><span class="sxs-lookup"><span data-stu-id="2ca87-243">Figure 16</span></span>  
> <span data-ttu-id="2ca87-244">Schaltfläche " **Format** "</span><span class="sxs-lookup"><span data-stu-id="2ca87-244">The **Format** button</span></span>  
> ![Schaltfläche "Format"][ImageFormat]  

## <span data-ttu-id="2ca87-246">Bearbeiten eines Skripts</span><span class="sxs-lookup"><span data-stu-id="2ca87-246">Edit a script</span></span>   

<span data-ttu-id="2ca87-247">Wenn Sie einen Fehler beheben, möchten Sie häufig einige Änderungen an Ihrem JavaScript-Code testen.</span><span class="sxs-lookup"><span data-stu-id="2ca87-247">When fixing a bug, you often want to test out some changes to your JavaScript code.</span></span>  <span data-ttu-id="2ca87-248">Sie müssen die Änderungen nicht in einem externen Editor oder in einer IDE vornehmen und die Seite dann erneut laden.</span><span class="sxs-lookup"><span data-stu-id="2ca87-248">You do not need to make the changes in an external editor or IDE and then reload the page.</span></span>  <span data-ttu-id="2ca87-249">Sie können Ihr Skript in devtools bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="2ca87-249">You may edit your script in DevTools.</span></span>  

<span data-ttu-id="2ca87-250">So bearbeiten Sie ein Skript:</span><span class="sxs-lookup"><span data-stu-id="2ca87-250">To edit a script:</span></span>  

1.  <span data-ttu-id="2ca87-251">Öffnen Sie die Datei im Bereich " **Editor** " des Bereichs " **Quellen** ".</span><span class="sxs-lookup"><span data-stu-id="2ca87-251">Open the file in the **Editor** pane of the **Sources** panel.</span></span>  
1.  <span data-ttu-id="2ca87-252">Nehmen Sie die gewünschten Änderungen im Bereich " **Editor** " vor.</span><span class="sxs-lookup"><span data-stu-id="2ca87-252">Make your changes in the **Editor** pane.</span></span>  
1.  <span data-ttu-id="2ca87-253">Drücken Sie `Ctrl` + `S` \ (Windows \) oder `Command` + `S` \ (macOS \), um zu speichern.</span><span class="sxs-lookup"><span data-stu-id="2ca87-253">Press `Ctrl`+`S` \(Windows\) or `Command`+`S` \(macOS\) to save.</span></span>  <span data-ttu-id="2ca87-254">DevTools-Patches die gesamte JS-Datei in das JavaScript-Modul von Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="2ca87-254">DevTools patches the entire JS file into the JavaScript engine of Microsoft Edge.</span></span>  

> ##### <span data-ttu-id="2ca87-255">Abbildung 17</span><span class="sxs-lookup"><span data-stu-id="2ca87-255">Figure 17</span></span>  
> <span data-ttu-id="2ca87-256">Der Bereich " **Editor** "</span><span class="sxs-lookup"><span data-stu-id="2ca87-256">The **Editor** pane</span></span>  
> ![Der Bereich "Editor"][ImageEditorPane]  

## <span data-ttu-id="2ca87-258">JavaScript deaktivieren</span><span class="sxs-lookup"><span data-stu-id="2ca87-258">Disable JavaScript</span></span>   

<span data-ttu-id="2ca87-259">Weitere Informationen finden Sie unter [Deaktivieren von JavaScript mit Microsoft Edge devtools][DevToolsJavascriptDisable].</span><span class="sxs-lookup"><span data-stu-id="2ca87-259">See [Disable JavaScript With Microsoft Edge DevTools][DevToolsJavascriptDisable].</span></span>  

<!--## Feedback   -->  



<!-- image links -->  

[ImageStepOverIcon]: /microsoft-edge/devtools-guide-chromium/media/step-over-icon.msft.png  
[ImageStepIntoIcon]: /microsoft-edge/devtools-guide-chromium/media/step-into-icon.msft.png  
[ImageStepOutIcon]: /microsoft-edge/devtools-guide-chromium/media/step-out-icon.msft.png  
[ImageResumeScriptExecutionIcon]: /microsoft-edge/devtools-guide-chromium/media/resume-script-run-icon.msft.png  
[ImageForceScriptExecutionIcon]: /microsoft-edge/devtools-guide-chromium/media/force-script-run-icon.msft.png  
[ImageAddExpressionIcon]: /microsoft-edge/devtools-guide-chromium/media/add-expression-icon.msft.png  
[ImageRefreshIcon]: /microsoft-edge/devtools-guide-chromium/media/refresh-icon.msft.png  
[ImageDeleteExpressionIcon]: /microsoft-edge/devtools-guide-chromium/media/delete-expression-icon.msft.png  
[ImageFormatIcon]: /microsoft-edge/devtools-guide-chromium/media/format-icon.msft.png  

[ImageSelectingStepOver]: /microsoft-edge/devtools-guide-chromium/media/javascript-source-page-debugger-step-over-next-function-call.msft.png "Abbildung 1: Auswählen des Schritts"  
[ImageSelectingStepInto]: /microsoft-edge/devtools-guide-chromium/media/javascript-source-page-debugger-step-into-next-function-call.msft.png "Abbildung 2: Auswählen von "Schritt in""  
[ImageSelectingStepOut]: /microsoft-edge/devtools-guide-chromium/media/javascript-source-page-debugger-step-out-of-current-function.msft.png "Abbildung 3: Auswählen von "Schritt aus""  
[ImageSelectingContinueToHere]: /microsoft-edge/devtools-guide-chromium/media/javascript-source-page-continue-to-here.msft.png "Abbildung 4: Auswählen von "weiter hier""  
[ImageSelectingRestartFrame]: /microsoft-edge/devtools-guide-chromium/media/javascript-source-page-debugger-restart-frame.msft.png "Abbildung 5: Auswählen von "Frame neu starten""  
[ImageSelectingResumeScriptExecution]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-get-started-js-resume-script-runtime.msft.png "Abbildung 6: Auswählen der Skriptausführung fortsetzen"  
[ImageSelectingForceScriptExecution]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-get-started-js-force-script-runtime.msft.png "Abbildung 7: Auswählen der Erzwingung der Skriptausführung"  
[ImageThreadsPane]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-main-min-js-threads.msft.png "Abbildung 8: der Bereich "Threads""  
[ImageScopePane]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-get-started-js-scope.msft.png "Abbildung 9: Bereichs Bereich"  
[ImageCallStackPane]: /microsoft-edge/devtools-guide-chromium/media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty.msft.png "Abbildung 10: der Bereich "Anrufliste""  
[ImageSelectingCopyStackTrace]: /microsoft-edge/devtools-guide-chromium/media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty-copy-stack-trace.msft.png "Abbildung 11: Auswählen der Stapelüberwachung kopieren"  
[ImageMarkEditorPane]: /microsoft-edge/devtools-guide-chromium/media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty-editor-mark-as-library-code.msft.png "Abbildung 12: Kennzeichnen eines Skripts als Bibliothekscode im Bereich "Editor""  
[ImageMarkCallStackPane]: /microsoft-edge/devtools-guide-chromium/media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty-call-stack-mark-as-library-code.msft.png "Abbildung 13: Kennzeichnen eines Skripts als Bibliothekscode aus dem Bereich "Anrufliste""  
[ImageMarkScriptSettings]: /microsoft-edge/devtools-guide-chromium/media/javascript-framework-library-code.msft.png "Abbildung 14: Kennzeichnen eines Skripts als Bibliothekscode aus Einstellungen"  
[ImageWatchPane]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-get-started-js-watch.msft.png "Abbildung 15: Überwachungsbereich"  
[ImageFormat]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-html-non-minified.msft.png "Abbildung 16: die Schaltfläche "Format""  
[ImageEditorPane]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-html-minified.msft.png "Abbildung 17: der Bereich "Editor""  

<!-- links -->  

[DevToolsJavascriptDisable]: disable.md "Deaktivieren von JavaScript mit Microsoft Edge devtools"  
[DevToolsJavascriptGetStarted]: index.md "Erste Schritte mit dem Debuggen von JavaScript in Microsoft Edge devtools"  
[DevToolsJavascriptSnippets]: snippets.md "Ausführen von JavaScript-Codeausschnitten auf einer beliebigen Seite mit Microsoft Edge devtools"  

[DevToolsCustomize]: ../customize/index.md "Anpassen von Microsoft Edge devtools"  

> [!NOTE]
> <span data-ttu-id="2ca87-281">Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2ca87-281">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="2ca87-282">Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/javascript/reference) und wird von [Kayce Basken][KayceBasques] (Technical Writer, Chrome devtools \ & Lighthouse \) erstellt.</span><span class="sxs-lookup"><span data-stu-id="2ca87-282">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/javascript/reference) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
<span data-ttu-id="2ca87-284">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="2ca87-284">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
