---
title: JavaScript-Debugging-Referenz
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: 26f7272534e0834e0fb302a40b7f0ebfc817c88e
ms.sourcegitcommit: 1251c555c6b4db8ef8187ed94d8832fdb89d03b8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/31/2020
ms.locfileid: "10982150"
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







# <span data-ttu-id="a7a81-103">JavaScript-Debug-Referenz</span><span class="sxs-lookup"><span data-stu-id="a7a81-103">JavaScript debugging reference</span></span>   



<span data-ttu-id="a7a81-104">Entdecken Sie neue Debugging-Workflows mit dieser umfassenden Referenz zu den Microsoft Edge DevTools-Debugging-Features.</span><span class="sxs-lookup"><span data-stu-id="a7a81-104">Discover new debugging workflows with this comprehensive reference of Microsoft Edge DevTools debugging features.</span></span>  

<span data-ttu-id="a7a81-105">Informationen zu den Grundlagen des Debuggens finden Sie unter [Erste Schritte beim Debuggen von JavaScript in Microsoft Edge devtools][DevToolsJavascriptGetStarted] .</span><span class="sxs-lookup"><span data-stu-id="a7a81-105">See [Get Started With Debugging JavaScript In Microsoft Edge DevTools][DevToolsJavascriptGetStarted] to learn the basics of debugging.</span></span>  

## <span data-ttu-id="a7a81-106">Anhalten von Code mit Haltepunkten</span><span class="sxs-lookup"><span data-stu-id="a7a81-106">Pause code with breakpoints</span></span>   

<span data-ttu-id="a7a81-107">Legen Sie einen Haltepunkt fest, damit Sie den Code in der Mitte der Laufzeit anhalten können.</span><span class="sxs-lookup"><span data-stu-id="a7a81-107">Set a breakpoint so that you are able to pause your code in the middle of the runtime.</span></span>  

<span data-ttu-id="a7a81-108">Informationen zum Festlegen von Haltepunkten finden Sie unter [Anhalten des Codes mit Haltepunkten][DevToolsJavascriptBreakpoints] .</span><span class="sxs-lookup"><span data-stu-id="a7a81-108">See [Pause Your Code With Breakpoints][DevToolsJavascriptBreakpoints] to learn how to set breakpoints.</span></span>  

[DevToolsJavascriptBreakpoints]: breakpoints.md "Anhalten des Codes mit Haltepunkten in Microsoft Edge devtools"  

## <span data-ttu-id="a7a81-110">Schritt-für-Schritt-Code</span><span class="sxs-lookup"><span data-stu-id="a7a81-110">Step through code</span></span>   

<span data-ttu-id="a7a81-111">Nachdem der Code angehalten wurde, führen Sie ihn schrittweise durch, und untersuchen Sie die Fluss-und Eigenschaftswerte auf dem Weg.</span><span class="sxs-lookup"><span data-stu-id="a7a81-111">Once your code is paused, step through it, one line at a time, investigating control flow and property values along the way.</span></span>  

### <span data-ttu-id="a7a81-112">Schritt über Codezeile</span><span class="sxs-lookup"><span data-stu-id="a7a81-112">Step over line of code</span></span>   

<span data-ttu-id="a7a81-113">Wenn Sie in einer Codezeile mit einer Funktion angehalten wurden, die für das zu debuggende Problem nicht relevant ist, klicken Sie auf das Symbol " **Schritt über** \ ( ![ Schritt über ][ImageStepOverIcon] \)", um die Funktion auszuführen, ohne Sie zu betreten.</span><span class="sxs-lookup"><span data-stu-id="a7a81-113">When paused on a line of code containing a function that is not relevant to the problem you are debugging, click on the **Step over** \(![Step over][ImageStepOverIcon]\) icon to run the function without stepping into it.</span></span>  

:::image type="complex" source="../media/javascript-source-page-debugger-step-over-next-function-call.msft.png" alt-text="Wählen Sie Schritt über" lightbox="../media/javascript-source-page-debugger-step-over-next-function-call.msft.png":::
   <span data-ttu-id="a7a81-115">Wählen Sie **Schritt über**</span><span class="sxs-lookup"><span data-stu-id="a7a81-115">Select **Step over**</span></span>  
:::image-end:::  

<span data-ttu-id="a7a81-116">Nehmen wir beispielsweise an, dass Sie den folgenden Code Debuggen:</span><span class="sxs-lookup"><span data-stu-id="a7a81-116">For example, suppose you are debugging the following code:</span></span>  

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

<span data-ttu-id="a7a81-117">Sie sind angehalten `A` .</span><span class="sxs-lookup"><span data-stu-id="a7a81-117">You are paused on `A`.</span></span>  <span data-ttu-id="a7a81-118">Wenn Sie den **Schritt über**drücken, führt devtools den gesamten Code in der Funktion aus, die Sie überschreiten, also `B` und `C` .</span><span class="sxs-lookup"><span data-stu-id="a7a81-118">By pressing **Step over**, DevTools runs all the code in the function that you are stepping over, which is `B` and `C`.</span></span>  <span data-ttu-id="a7a81-119">DevTools wird dann angehalten `D` .</span><span class="sxs-lookup"><span data-stu-id="a7a81-119">DevTools then pauses on `D`.</span></span>  

### <span data-ttu-id="a7a81-120">Schritt in Codezeile</span><span class="sxs-lookup"><span data-stu-id="a7a81-120">Step into line of code</span></span>   

<span data-ttu-id="a7a81-121">Wenn Sie in einer Codezeile mit einem Funktionsaufruf, der sich auf das zu debuggende Problem bezieht, angehalten haben, klicken Sie auf das Symbol **Schritt in** \ ( ![ Schritt in ][ImageStepIntoIcon] \), um die Funktion weiter zu untersuchen.</span><span class="sxs-lookup"><span data-stu-id="a7a81-121">When paused on a line of code containing a function call that is related to the problem you are debugging, click on the **Step into** \(![Step into][ImageStepIntoIcon]\) icon to investigate that function further.</span></span>  

:::image type="complex" source="../media/javascript-source-page-debugger-step-into-next-function-call.msft.png" alt-text="Schritt in auswählen" lightbox="../media/javascript-source-page-debugger-step-into-next-function-call.msft.png":::
   <span data-ttu-id="a7a81-123">**Schritt in** auswählen</span><span class="sxs-lookup"><span data-stu-id="a7a81-123">Select **Step into**</span></span>  
:::image-end:::  

<span data-ttu-id="a7a81-124">Nehmen wir beispielsweise an, dass Sie den folgenden Code Debuggen:</span><span class="sxs-lookup"><span data-stu-id="a7a81-124">For example, suppose you are debugging the following code:</span></span>  

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

<span data-ttu-id="a7a81-125">Sie sind angehalten `A` .</span><span class="sxs-lookup"><span data-stu-id="a7a81-125">You are paused on `A`.</span></span>  <span data-ttu-id="a7a81-126">Durch Drücken von **Schritt in**führt devtools diese Codezeile aus und hält dann an `B` .</span><span class="sxs-lookup"><span data-stu-id="a7a81-126">By pressing **Step into**, DevTools runs this line of code, then pauses on `B`.</span></span>  

### <span data-ttu-id="a7a81-127">Schritt außerhalb der Codezeile</span><span class="sxs-lookup"><span data-stu-id="a7a81-127">Step out of line of code</span></span>   

<span data-ttu-id="a7a81-128">Wenn Sie innerhalb einer Funktion angehalten haben, die nicht mit dem zu debuggenden Problem in Verbindung steht, klicken Sie auf das Symbol " **Schritt aus** \ ( ![ Schritt aus ][ImageStepOutIcon] \)", um den restlichen Code der Funktion auszuführen.</span><span class="sxs-lookup"><span data-stu-id="a7a81-128">When paused inside of a function that is not related to the problem you are debugging, click on the **Step out** \(![Step out][ImageStepOutIcon]\) icon to run the rest of the code of the function.</span></span>  

:::image type="complex" source="../media/javascript-source-page-debugger-step-out-of-current-function.msft.png" alt-text="Auswählen von "Schritt aus"" lightbox="../media/javascript-source-page-debugger-step-out-of-current-function.msft.png":::
   <span data-ttu-id="a7a81-130">Auswählen **von "Schritt aus** "</span><span class="sxs-lookup"><span data-stu-id="a7a81-130">Select **Step out**</span></span>  
:::image-end:::  

<span data-ttu-id="a7a81-131">Nehmen wir beispielsweise an, dass Sie den folgenden Codeausschnitt Debuggen.</span><span class="sxs-lookup"><span data-stu-id="a7a81-131">For example, suppose you are debugging the following code snippet.</span></span>  

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

<span data-ttu-id="a7a81-132">Sie sind angehalten `A` .</span><span class="sxs-lookup"><span data-stu-id="a7a81-132">You are paused on `A`.</span></span>  <span data-ttu-id="a7a81-133">Durch Drücken von **Step out**führt devtools den restlichen Code in aus `getName()` , der sich nur `B` in diesem Beispiel befindet, und hält dann an `C` .</span><span class="sxs-lookup"><span data-stu-id="a7a81-133">By pressing **Step out**, DevTools runs the rest of the code in `getName()`, which is just `B` in this example, and then pauses on `C`.</span></span>  

### <span data-ttu-id="a7a81-134">Ausführen des gesamten Codes bis zu einer bestimmten Zeile</span><span class="sxs-lookup"><span data-stu-id="a7a81-134">Run all code up to a specific line</span></span>   

<span data-ttu-id="a7a81-135">Wenn Sie eine Long-Funktion Debuggen, gibt es möglicherweise viel Code, der sich nicht auf das zu debuggende Problem bezieht.</span><span class="sxs-lookup"><span data-stu-id="a7a81-135">When debugging a long function, there may be a lot of code that is not related to the problem you are debugging.</span></span>  

<span data-ttu-id="a7a81-136">Sie können alle Zeilen durchlaufen, aber das ist mühsam.</span><span class="sxs-lookup"><span data-stu-id="a7a81-136">You may choose to step through all the lines, but that is tedious.</span></span>  <span data-ttu-id="a7a81-137">Sie können festlegen, dass in der Zeile, in der Sie interessiert sind, ein Haltepunkt für den Code in der Zeile gesetzt wird, und klicken Sie dann auf das Symbol zum **fort** setzen der Skriptausführung \ ( ![ Skriptausführung fortsetzen ][ImageResumeScriptExecutionIcon] \), aber es gibt einen schnelleren Weg.</span><span class="sxs-lookup"><span data-stu-id="a7a81-137">You may choose to set a line-of-code breakpoint on the line in which you are interested and then click on the **Resume Script Execution** \(![Resume Script Execution][ImageResumeScriptExecutionIcon]\) icon, but there is a faster way.</span></span>  

<span data-ttu-id="a7a81-138">Klicken Sie mit der rechten Maustaste auf die Codezeile, für die Sie sich interessieren, und wählen Sie **hier weiter**.</span><span class="sxs-lookup"><span data-stu-id="a7a81-138">Right-click the line of code in which you are interested, and select **Continue to here**.</span></span>  <span data-ttu-id="a7a81-139">DevTools führt den gesamten Code bis zu diesem Punkt aus und hält dann in dieser Zeile an.</span><span class="sxs-lookup"><span data-stu-id="a7a81-139">DevTools runs all of the code up to that point, and then pauses on that line.</span></span>  

:::image type="complex" source="../media/javascript-source-page-continue-to-here.msft.png" alt-text="Wählen Sie hier weiter" lightbox="../media/javascript-source-page-continue-to-here.msft.png":::
   <span data-ttu-id="a7a81-141">Wählen Sie **hier weiter**</span><span class="sxs-lookup"><span data-stu-id="a7a81-141">Select **Continue to here**</span></span>  
:::image-end:::  

### <span data-ttu-id="a7a81-142">Starten der obersten Funktion der Aufrufliste</span><span class="sxs-lookup"><span data-stu-id="a7a81-142">Restart the top function of the call stack</span></span>   

<span data-ttu-id="a7a81-143">Wenn Sie in einer Codezeile angehalten sind, klicken Sie mit der rechten Maustaste auf eine beliebige Stelle im Bereich **Anrufliste** , und wählen Sie **Frame neu starten** aus, um in der ersten Zeile der obersten Funktion in der Aufrufliste zu pausieren.</span><span class="sxs-lookup"><span data-stu-id="a7a81-143">While paused on a line of code, right-click anywhere in the **Call Stack** pane and select **Restart Frame** to pause on the first line of the top function in your call stack.</span></span>  <span data-ttu-id="a7a81-144">Die oberste Funktion ist die letzte Funktion, die ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="a7a81-144">The top function is the last function that was run.</span></span>  

<span data-ttu-id="a7a81-145">Nehmen wir beispielsweise an, dass Sie den folgenden Codeausschnitt durchlaufen haben.</span><span class="sxs-lookup"><span data-stu-id="a7a81-145">For example, suppose you are stepping through the following code snippet.</span></span>  

```javascript
function factorial(n) {
    var product = 0; // B
    for (var i = 1; i <= n; i++) {
      product += i;
    }
    return product; // A
}
```  

<span data-ttu-id="a7a81-146">Sie sind angehalten `A` .</span><span class="sxs-lookup"><span data-stu-id="a7a81-146">You are paused on `A`.</span></span>  <span data-ttu-id="a7a81-147">Nachdem Sie auf **Frame neu starten**geklickt haben, sollten Sie angehalten werden `B` , ohne einen Haltepunkt festzulegen oder die **Ausführung von Skript Fortsetzung**zu drücken.</span><span class="sxs-lookup"><span data-stu-id="a7a81-147">After clicking **Restart Frame**, you should be paused on `B`, without ever setting a breakpoint or pressing **Resume script execution**.</span></span>  

:::image type="complex" source="../media/javascript-source-page-debugger-restart-frame.msft.png" alt-text="Wählen Sie Frame neu starten aus." lightbox="../media/javascript-source-page-debugger-restart-frame.msft.png":::
   <span data-ttu-id="a7a81-149">Wählen Sie **Frame neu starten** aus.</span><span class="sxs-lookup"><span data-stu-id="a7a81-149">Select **Restart Frame**</span></span>  
:::image-end:::  

### <span data-ttu-id="a7a81-150">Fortsetzen der Skriptlaufzeit</span><span class="sxs-lookup"><span data-stu-id="a7a81-150">Resume script runtime</span></span>   

<span data-ttu-id="a7a81-151">Wenn Sie die Laufzeit nach einer Pause Ihres Skripts fortsetzen möchten, klicken Sie auf das Symbol zum Fortsetzen der \**Skriptausführung \** ( ![ Fortsetzungs Skriptausführung ][ImageResumeScriptExecutionIcon] \).</span><span class="sxs-lookup"><span data-stu-id="a7a81-151">To continue the runtime after a pause of your script, click on the **Resume Script Execution** \(![Resume Script Execution][ImageResumeScriptExecutionIcon]\) icon.</span></span>  <span data-ttu-id="a7a81-152">DevTools führt das Skript bis zum nächsten Haltepunkt aus, sofern vorhanden.</span><span class="sxs-lookup"><span data-stu-id="a7a81-152">DevTools runs the script up until the next breakpoint, if any.</span></span>  

:::image type="complex" source="../media/javascript-sources-get-started-js-resume-script-runtime.msft.png" alt-text="Auswählen der Skriptausführung fortsetzen" lightbox="../media/javascript-sources-get-started-js-resume-script-runtime.msft.png":::
   <span data-ttu-id="a7a81-154">Auswählen der **Skriptausführung fortsetzen**</span><span class="sxs-lookup"><span data-stu-id="a7a81-154">Select **Resume script execution**</span></span>  
:::image-end:::  

#### <span data-ttu-id="a7a81-155">Erzwingen der Skriptlaufzeit</span><span class="sxs-lookup"><span data-stu-id="a7a81-155">Force script runtime</span></span>   

<span data-ttu-id="a7a81-156">Wenn Sie alle Haltepunkte ignorieren und die Fortsetzung des Skripts erzwingen möchten, klicken Sie **auf das** Symbol zum Fortsetzen der Skriptausführung \ ( ![ Fortsetzen der Skriptausführung ][ImageResumeScriptExecutionIcon] \), und wählen Sie dann Skriptausführung **erzwingen** \ ( ![ erzwingen der Skriptausführung ][ImageForceScriptExecutionIcon] \) aus.</span><span class="sxs-lookup"><span data-stu-id="a7a81-156">To ignore all breakpoints and force your script to resume running, click and hold the **Resume Script Execution** \(![Resume Script Execution][ImageResumeScriptExecutionIcon]\) icon and then select **Force script execution** \(![Force script execution][ImageForceScriptExecutionIcon]\).</span></span>  

:::image type="complex" source="../media/javascript-sources-get-started-js-force-script-runtime.msft.png" alt-text="Auswählen der Erzwingung der Skriptausführung" lightbox="../media/javascript-sources-get-started-js-force-script-runtime.msft.png":::
   <span data-ttu-id="a7a81-158">Auswählen der **Erzwingung der Skriptausführung**</span><span class="sxs-lookup"><span data-stu-id="a7a81-158">Select **Force script execution**</span></span>  
:::image-end:::  

### <span data-ttu-id="a7a81-159">Ändern des Thread Kontexts</span><span class="sxs-lookup"><span data-stu-id="a7a81-159">Change thread context</span></span>   

<span data-ttu-id="a7a81-160">Wenn Sie mit webarbeitern oder Dienst Mitarbeitern arbeiten, klicken Sie auf einen im Bereich **Threads** aufgelisteten Kontext, um zu diesem Kontext zu wechseln.</span><span class="sxs-lookup"><span data-stu-id="a7a81-160">When working with web workers or service workers, click on a context listed in the **Threads** pane to switch to that context.</span></span>  <span data-ttu-id="a7a81-161">Das blaue Pfeilsymbol steht für den aktuell ausgewählten Kontext.</span><span class="sxs-lookup"><span data-stu-id="a7a81-161">The blue arrow icon represents which context is currently selected.</span></span>  

:::image type="complex" source="../media/javascript-sources-main-min-js-threads.msft.png" alt-text="Der Bereich "Threads"" lightbox="../media/javascript-sources-main-min-js-threads.msft.png":::
   <span data-ttu-id="a7a81-163">Der Bereich " **Threads** "</span><span class="sxs-lookup"><span data-stu-id="a7a81-163">The **Threads** pane</span></span>  
:::image-end:::  

<span data-ttu-id="a7a81-164">Nehmen wir beispielsweise an, dass Sie sowohl in Ihrem Hauptskript als auch in Ihrem Dienstmitarbeiter Skript an einem Haltepunkt angehalten werden.</span><span class="sxs-lookup"><span data-stu-id="a7a81-164">For example, suppose that you are paused on a breakpoint in both your main script and your service worker script.</span></span>  <span data-ttu-id="a7a81-165">Sie möchten die lokalen und globalen Eigenschaften für den Service Worker-Kontext anzeigen, aber der Bereich " **Quellen** " zeigt den Hauptskript Kontext an.</span><span class="sxs-lookup"><span data-stu-id="a7a81-165">You want to view the local and global properties for the service worker context, but the **Sources** panel is showing the main script context.</span></span>  <span data-ttu-id="a7a81-166">Durch Klicken auf den Eintrag Service Worker im Bereich **Threads** sollten Sie in der Lage sein, zu diesem Kontext zu wechseln.</span><span class="sxs-lookup"><span data-stu-id="a7a81-166">By clicking on the service worker entry in the **Threads** pane, you should be able to switch to that context.</span></span>  

## <span data-ttu-id="a7a81-167">Anzeigen und Bearbeiten von lokalen, Closure-und globalen Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a7a81-167">View and edit local, closure, and global properties</span></span>   

<span data-ttu-id="a7a81-168">Wenn Sie in einer Codezeile angehalten wurden, verwenden Sie **den Bereich Bereich,** um die Werte von Eigenschaften und Variablen in den Bereichen lokal, Closure und Global anzuzeigen und zu bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="a7a81-168">While paused on a line of code, use the **Scope** pane to view and edit the values of properties and variables in the local, closure, and global scopes.</span></span>  

*   <span data-ttu-id="a7a81-169">Doppelklicken Sie auf einen Eigenschaftswert, um ihn zu ändern.</span><span class="sxs-lookup"><span data-stu-id="a7a81-169">Double-click a property value to change it.</span></span>  
*   <span data-ttu-id="a7a81-170">Nicht aufzählbare Eigenschaften werden abgeblendet dargestellt.</span><span class="sxs-lookup"><span data-stu-id="a7a81-170">Non-enumerable properties are greyed out.</span></span>  

:::image type="complex" source="../media/javascript-sources-get-started-js-scope.msft.png" alt-text="Bereichs Bereich" lightbox="../media/javascript-sources-get-started-js-scope.msft.png":::
   <span data-ttu-id="a7a81-172">**Bereichs** Bereich</span><span class="sxs-lookup"><span data-stu-id="a7a81-172">The **Scope** pane</span></span>  
:::image-end:::  

## <span data-ttu-id="a7a81-173">Anzeigen der aktuellen Anrufliste</span><span class="sxs-lookup"><span data-stu-id="a7a81-173">View the current call stack</span></span>   

<span data-ttu-id="a7a81-174">Wenn Sie in einer Codezeile angehalten wurden, verwenden Sie den Bereich **Anrufliste** , um die Anrufliste anzuzeigen, die Sie zu diesem Punkt erhalten hat.</span><span class="sxs-lookup"><span data-stu-id="a7a81-174">While paused on a line of code, use the **Call Stack** pane to view the call stack that got you to this point.</span></span>  

<!--If you are working with async code, check the **Async** checkbox to enable async call stacks.  -->  

<span data-ttu-id="a7a81-175">Klicken Sie auf einen Eintrag, um zu der Codezeile zu springen, in der die Funktion aufgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="a7a81-175">Click on an entry to jump to the line of code where that function was called.</span></span>  <span data-ttu-id="a7a81-176">Das blaue Pfeilsymbol stellt dar, welche Funktion devtools derzeit markiert.</span><span class="sxs-lookup"><span data-stu-id="a7a81-176">The blue arrow icon represents which function DevTools is currently highlighting.</span></span>  

:::image type="complex" source="../media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty.msft.png" alt-text="Der Bereich "Anrufliste"" lightbox="../media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty.msft.png":::
   <span data-ttu-id="a7a81-178">Der Bereich " **Anrufliste** "</span><span class="sxs-lookup"><span data-stu-id="a7a81-178">The **Call Stack** pane</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="a7a81-179">Wenn Sie nicht in einer Codezeile angehalten wurden, ist der Bereich **Aufrufliste** leer.</span><span class="sxs-lookup"><span data-stu-id="a7a81-179">When not paused on a line of code, the **Call Stack** pane is empty.</span></span>  

### <span data-ttu-id="a7a81-180">Kopieren einer Stapelüberwachung</span><span class="sxs-lookup"><span data-stu-id="a7a81-180">Copy stack trace</span></span>   

<!--
This should be moved to an "Export debug data" H2 section when there is enough content for that, but there is not right now, so it is here.
-->

<span data-ttu-id="a7a81-181">Klicken Sie mit der rechten Maustaste auf eine beliebige Stelle im Bereich **Anrufliste** , und wählen Sie **Stapelüberwachung kopieren** aus, um die aktuelle Aufrufliste in die Zwischenablage zu kopieren.</span><span class="sxs-lookup"><span data-stu-id="a7a81-181">Right-click anywhere in the **Call Stack** pane and select **Copy stack trace** to copy the current call stack to the clipboard.</span></span>  

:::image type="complex" source="../media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty-copy-stack-trace.msft.png" alt-text="Wählen Sie Stapelüberwachung kopieren aus." lightbox="../media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty-copy-stack-trace.msft.png":::
   <span data-ttu-id="a7a81-183">Wählen Sie **Stapelüberwachung kopieren** aus.</span><span class="sxs-lookup"><span data-stu-id="a7a81-183">Select **Copy Stack Trace**</span></span>  
:::image-end:::  

<span data-ttu-id="a7a81-184">Nachfolgend finden Sie ein Beispiel für die Ausgabe:</span><span class="sxs-lookup"><span data-stu-id="a7a81-184">Below is an example of the output:</span></span>  

```javascript
getNumber1 (get-started.js:35)
inputsAreEmpty (get-started.js:22)
onClick (get-started.js:15)
```  

## <span data-ttu-id="a7a81-185">Ignorieren eines Skripts oder Musters von Skripts</span><span class="sxs-lookup"><span data-stu-id="a7a81-185">Ignore a script or pattern of scripts</span></span>  

<span data-ttu-id="a7a81-186">Markieren Sie ein Skript als Bibliothekscode, wenn Sie dieses Skript beim Debuggen ignorieren möchten.</span><span class="sxs-lookup"><span data-stu-id="a7a81-186">Mark a script as Library code when you want to ignore that script while debugging.</span></span>  <span data-ttu-id="a7a81-187">Wenn es sich um einen Bibliothekscode handelt, wird ein Skript im Bereich " **Aufrufliste** " verdeckt, und Sie gehen nie in die Funktionen des Skripts ein, wenn Sie den Code schrittweise durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="a7a81-187">When marked as Library code, a script is obscured in the **Call Stack** pane, and you never step into the functions of the script when you step through your code.</span></span>  

<span data-ttu-id="a7a81-188">Nehmen wir beispielsweise an, dass Sie den folgenden Codeausschnitt durchlaufen haben.</span><span class="sxs-lookup"><span data-stu-id="a7a81-188">For example, suppose you are stepping through the following code snippet.</span></span>  

```javascript
function animate() {
    prepare();
    lib.doFancyStuff(); // A
    render();
}
```  

`A` <span data-ttu-id="a7a81-189">ist eine drittanbieterbibliothek, der Sie vertrauen.</span><span class="sxs-lookup"><span data-stu-id="a7a81-189">is a third-party library that you trust.</span></span>  <span data-ttu-id="a7a81-190">Wenn Sie sicher sind, dass das Problem, das Sie Debuggen, nicht mit der Bibliothek von Drittanbietern verknüpft ist, ist es sinnvoll, das Skript als **Bibliothekscode**zu kennzeichnen.</span><span class="sxs-lookup"><span data-stu-id="a7a81-190">If you are confident that the problem you are debugging is not related to the third-party library, then it makes sense to mark the script as **Library code**.</span></span>  

### <span data-ttu-id="a7a81-191">Markieren eines Skripts als Bibliothekscode im Bereich "Editor"</span><span class="sxs-lookup"><span data-stu-id="a7a81-191">Mark a script as Library code from the Editor pane</span></span>  

<span data-ttu-id="a7a81-192">So markieren Sie ein Skript im **Editor** Bereich als **Bibliothekscode** :</span><span class="sxs-lookup"><span data-stu-id="a7a81-192">To mark a script as **Library code** from the **Editor** pane:</span></span>  

1.  <span data-ttu-id="a7a81-193">Öffnen Sie die Datei.</span><span class="sxs-lookup"><span data-stu-id="a7a81-193">Open the file.</span></span>  
1.  <span data-ttu-id="a7a81-194">Klicken Sie mit der rechten Maustaste auf eine beliebige Stelle.</span><span class="sxs-lookup"><span data-stu-id="a7a81-194">Right-click anywhere.</span></span>  
1.  <span data-ttu-id="a7a81-195">Wählen Sie **als Bibliothekscode markieren**aus.</span><span class="sxs-lookup"><span data-stu-id="a7a81-195">Select **Mark as Library code**.</span></span>  
    
    :::image type="complex" source="../media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty-editor-mark-as-library-code.msft.png" alt-text="Markieren eines Skripts als Bibliothekscode über den Bereich "Editor"" lightbox="../media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty-editor-mark-as-library-code.msft.png":::
       <span data-ttu-id="a7a81-197">Markieren eines Skripts als **Bibliothekscode** über den Bereich " **Editor** "</span><span class="sxs-lookup"><span data-stu-id="a7a81-197">Marking a script as **Library code** from the **Editor** pane</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="a7a81-198">Markieren eines Skripts als Bibliothekscode aus dem Bereich "Anrufliste"</span><span class="sxs-lookup"><span data-stu-id="a7a81-198">Mark a script as Library code from the Call Stack pane</span></span>  

<span data-ttu-id="a7a81-199">So markieren Sie ein Skript aus dem Bereich " **Anrufliste** " als **Bibliothekscode** :</span><span class="sxs-lookup"><span data-stu-id="a7a81-199">To mark a script as **Library code** from the **Call Stack** pane:</span></span>  

1.  <span data-ttu-id="a7a81-200">Klicken Sie mit der rechten Maustaste auf eine Funktion aus dem Skript.</span><span class="sxs-lookup"><span data-stu-id="a7a81-200">Right-click on a function from the script.</span></span>  
1.  <span data-ttu-id="a7a81-201">Wählen Sie **als Bibliothekscode markieren**aus.</span><span class="sxs-lookup"><span data-stu-id="a7a81-201">Select **Mark as Library code**.</span></span>  
    
    :::image type="complex" source="../media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty-call-stack-mark-as-library-code.msft.png" alt-text="Markieren eines Skripts als Bibliothekscode aus dem Bereich "Anrufliste"" lightbox="../media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty-call-stack-mark-as-library-code.msft.png":::
       <span data-ttu-id="a7a81-203">Markieren eines Skripts als **Bibliothekscode** aus dem Bereich " **Anrufliste** "</span><span class="sxs-lookup"><span data-stu-id="a7a81-203">Marking a script as **Library code** from the **Call Stack** pane</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="a7a81-204">Markieren eines Skripts als Bibliothekscode aus Einstellungen</span><span class="sxs-lookup"><span data-stu-id="a7a81-204">Mark a script as Library code from Settings</span></span>  

<span data-ttu-id="a7a81-205">So markieren Sie ein einzelnes Skript oder Skript Muster aus den Einstellungen:</span><span class="sxs-lookup"><span data-stu-id="a7a81-205">To mark a single script or pattern of scripts from Settings:</span></span>  

1.  <span data-ttu-id="a7a81-206">Öffnen Sie [Einstellungen][DevToolsCustomize].</span><span class="sxs-lookup"><span data-stu-id="a7a81-206">Open [Settings][DevToolsCustomize].</span></span>  
1.  <span data-ttu-id="a7a81-207">Wechseln Sie zur Registerkarte **Bibliothekscode** .</span><span class="sxs-lookup"><span data-stu-id="a7a81-207">Go to the **Library code** tab.</span></span>  
1.  <span data-ttu-id="a7a81-208">Klicken Sie auf **Muster hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="a7a81-208">Click **Add pattern**.</span></span>  
1.  <span data-ttu-id="a7a81-209">Geben Sie den Skriptnamen oder ein Regex-Muster von Skriptnamen ein, das als **Bibliothekscode**markiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="a7a81-209">Enter the script name or a regex pattern of script names to mark as **Library code**.</span></span>  
1.  <span data-ttu-id="a7a81-210">Klicken Sie auf **Hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="a7a81-210">Click **Add**.</span></span>  
    
    :::image type="complex" source="../media/javascript-framework-library-code.msft.png" alt-text="Markieren eines Skripts als Bibliothekscode aus Einstellungen" lightbox="../media/javascript-framework-library-code.msft.png":::
       <span data-ttu-id="a7a81-212">Markieren eines Skripts als **Bibliothekscode** aus **Einstellungen**</span><span class="sxs-lookup"><span data-stu-id="a7a81-212">Marking a script as **Library code** from **Settings**</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="a7a81-213">Ausführen von Codeausschnitten von Debugcode auf jeder Seite</span><span class="sxs-lookup"><span data-stu-id="a7a81-213">Run snippets of debug code from any page</span></span>   

<span data-ttu-id="a7a81-214">Wenn Sie immer wieder denselben Debugcode in der Konsole ausführen, sollten Sie Snippets in Betracht gezogen sehen.</span><span class="sxs-lookup"><span data-stu-id="a7a81-214">If you find yourself running the same debug code in the Console over and over, consider Snippets.</span></span>  <span data-ttu-id="a7a81-215">Ausschnitte sind Lauf Zeit Skripte, die Sie in devtools erstellen, speichern und ausführen.</span><span class="sxs-lookup"><span data-stu-id="a7a81-215">Snippets are runtime scripts that you author, store, and run within DevTools.</span></span>  

<span data-ttu-id="a7a81-216">Weitere Informationen finden Sie unter [Ausführen von Codeausschnitten auf jeder Seite][DevToolsJavascriptSnippets] .</span><span class="sxs-lookup"><span data-stu-id="a7a81-216">See [Run Snippets of Code From Any Page][DevToolsJavascriptSnippets] to learn more.</span></span>  

## <span data-ttu-id="a7a81-217">Sehen Sie sich die Werte benutzerdefinierter JavaScript-Ausdrücke an</span><span class="sxs-lookup"><span data-stu-id="a7a81-217">Watch the values of custom JavaScript expressions</span></span>   

<span data-ttu-id="a7a81-218">Verwenden Sie den **Überwachungs** Bereich, um die Werte benutzerdefinierter Ausdrücke zu überwachen.</span><span class="sxs-lookup"><span data-stu-id="a7a81-218">Use the **Watch** pane to watch the values of custom expressions.</span></span>  <span data-ttu-id="a7a81-219">Sie können jeden gültigen JavaScript-Ausdruck sehen.</span><span class="sxs-lookup"><span data-stu-id="a7a81-219">You may watch any valid JavaScript expression.</span></span>  

:::image type="complex" source="../media/javascript-sources-get-started-js-watch.msft.png" alt-text="Der Überwachungsbereich" lightbox="../media/javascript-sources-get-started-js-watch.msft.png":::
   <span data-ttu-id="a7a81-221">Der **Überwachungs** Bereich</span><span class="sxs-lookup"><span data-stu-id="a7a81-221">The **Watch** pane</span></span>  
:::image-end:::  

*   <span data-ttu-id="a7a81-222">Klicken Sie auf das Symbol **Ausdruck hinzufügen** \ ( ![ Ausdruck hinzufügen ][ImageAddExpressionIcon] \), um einen neuen Überwachungsausdruck zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="a7a81-222">Click on the **Add Expression** \(![Add Expression][ImageAddExpressionIcon]\) icon to create a new watch expression.</span></span>  
*   <span data-ttu-id="a7a81-223">Klicken Sie auf das Symbol **Aktualisieren** \ ( ![ aktualisieren ][ImageRefreshIcon] \), um die Werte aller vorhandenen Ausdrücke zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="a7a81-223">Click on the **Refresh** \(![Refresh][ImageRefreshIcon]\) icon to refresh the values of all existing expressions.</span></span>  <span data-ttu-id="a7a81-224">Werte werden beim Durchlaufen des Codes automatisch aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="a7a81-224">Values automatically refresh while stepping through code.</span></span>  
*   <span data-ttu-id="a7a81-225">Zeigen Sie mit der Maus auf einen Ausdruck, und klicken Sie auf das Symbol zum **Löschen** des Ausdrucks \ ( ![ Ausdruck löschen ][ImageDeleteExpressionIcon] \), um es zu löschen.</span><span class="sxs-lookup"><span data-stu-id="a7a81-225">Hover over an expression and click on the **Delete Expression** \(![Delete Expression][ImageDeleteExpressionIcon]\) icon to delete it.</span></span>  
    
## <span data-ttu-id="a7a81-226">Erstellen einer lesbaren minimierte-Datei</span><span class="sxs-lookup"><span data-stu-id="a7a81-226">Make a minified file readable</span></span>   

<span data-ttu-id="a7a81-227">Klicken Sie auf das Symbol **Format** \ ( ![ Format ][ImageFormatIcon] \), um eine minimierte-Datei menschlich lesbar zu machen.</span><span class="sxs-lookup"><span data-stu-id="a7a81-227">Click on the **Format** \(![Format][ImageFormatIcon]\) icon to make a minified file human-readable.</span></span>  

:::image type="complex" source="../media/javascript-sources-html-non-minified.msft.png" alt-text="Schaltfläche "Format"" lightbox="../media/javascript-sources-html-non-minified.msft.png":::
   <span data-ttu-id="a7a81-229">Schaltfläche " **Format** "</span><span class="sxs-lookup"><span data-stu-id="a7a81-229">The **Format** button</span></span>  
:::image-end:::  

## <span data-ttu-id="a7a81-230">Bearbeiten eines Skripts</span><span class="sxs-lookup"><span data-stu-id="a7a81-230">Edit a script</span></span>   

<span data-ttu-id="a7a81-231">Wenn Sie einen Fehler beheben, möchten Sie häufig einige Änderungen an Ihrem JavaScript-Code testen.</span><span class="sxs-lookup"><span data-stu-id="a7a81-231">When fixing a bug, you often want to test out some changes to your JavaScript code.</span></span>  <span data-ttu-id="a7a81-232">Sie müssen die Änderungen nicht in einem externen Editor oder in einer IDE vornehmen und die Seite dann erneut laden.</span><span class="sxs-lookup"><span data-stu-id="a7a81-232">You do not need to make the changes in an external editor or IDE and then reload the page.</span></span>  <span data-ttu-id="a7a81-233">Sie können Ihr Skript in devtools bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="a7a81-233">You may edit your script in DevTools.</span></span>  

<span data-ttu-id="a7a81-234">So bearbeiten Sie ein Skript:</span><span class="sxs-lookup"><span data-stu-id="a7a81-234">To edit a script:</span></span>  

1.  <span data-ttu-id="a7a81-235">Öffnen Sie die Datei im Bereich " **Editor** " des Bereichs " **Quellen** ".</span><span class="sxs-lookup"><span data-stu-id="a7a81-235">Open the file in the **Editor** pane of the **Sources** panel.</span></span>  
1.  <span data-ttu-id="a7a81-236">Nehmen Sie die gewünschten Änderungen im Bereich " **Editor** " vor.</span><span class="sxs-lookup"><span data-stu-id="a7a81-236">Make your changes in the **Editor** pane.</span></span>  
1.  <span data-ttu-id="a7a81-237">Drücken Sie `Ctrl` + `S` \ (Windows \) oder `Command` + `S` \ (macOS \), um zu speichern.</span><span class="sxs-lookup"><span data-stu-id="a7a81-237">Press `Ctrl`+`S` \(Windows\) or `Command`+`S` \(macOS\) to save.</span></span>  <span data-ttu-id="a7a81-238">DevTools-Patches die gesamte JS-Datei in das JavaScript-Modul von Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="a7a81-238">DevTools patches the entire JS file into the JavaScript engine of Microsoft Edge.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-html-minified.msft.png" alt-text="Der Bereich "Editor"" lightbox="../media/javascript-sources-html-minified.msft.png":::
       <span data-ttu-id="a7a81-240">Der Bereich " **Editor** "</span><span class="sxs-lookup"><span data-stu-id="a7a81-240">The **Editor** pane</span></span>  
    :::image-end:::  
     
## <span data-ttu-id="a7a81-241">JavaScript deaktivieren</span><span class="sxs-lookup"><span data-stu-id="a7a81-241">Disable JavaScript</span></span>   

<span data-ttu-id="a7a81-242">Weitere Informationen finden Sie unter [Deaktivieren von JavaScript mit Microsoft Edge devtools][DevToolsJavascriptDisable].</span><span class="sxs-lookup"><span data-stu-id="a7a81-242">See [Disable JavaScript with Microsoft Edge DevTools][DevToolsJavascriptDisable].</span></span>  

<!--## Feedback   -->  



<!-- image links -->  

[ImageStepOverIcon]: ../media/step-over-icon.msft.png  
[ImageStepIntoIcon]: ../media/step-into-icon.msft.png  
[ImageStepOutIcon]: ../media/step-out-icon.msft.png  
[ImageResumeScriptExecutionIcon]: ../media/resume-script-run-icon.msft.png  
[ImageForceScriptExecutionIcon]: ../media/force-script-run-icon.msft.png  
[ImageAddExpressionIcon]: ../media/add-expression-icon.msft.png  
[ImageRefreshIcon]: ../media/refresh-icon.msft.png  
[ImageDeleteExpressionIcon]: ../media/delete-expression-icon.msft.png  
[ImageFormatIcon]: ../media/format-icon.msft.png  

<!-- links -->  

[DevToolsJavascriptDisable]: ./disable.md "Deaktivieren von JavaScript mit Microsoft Edge devtools | Microsoft docs"  
[DevToolsJavascriptGetStarted]: ./index.md "Erste Schritte mit dem Debuggen von JavaScript in Microsoft Edge devtools | Microsoft docs"  
[DevToolsJavascriptSnippets]: ./snippets.md "Ausführen von JavaScript-Codeausschnitten auf einer beliebigen Seite mit Microsoft Edge devtools | Microsoft docs"  
[DevToolsCustomize]: ../customize/index.md "Anpassen von Microsoft Edge devtools | Microsoft docs"  

> [!NOTE]
> <span data-ttu-id="a7a81-247">Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a7a81-247">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="a7a81-248">Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/javascript/reference) und wird von [Kayce Basken][KayceBasques] (Technical Writer, Chrome devtools \ & Lighthouse \) erstellt.</span><span class="sxs-lookup"><span data-stu-id="a7a81-248">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/javascript/reference) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
<span data-ttu-id="a7a81-250">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="a7a81-250">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
