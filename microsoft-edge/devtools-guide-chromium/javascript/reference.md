---
description: Entdecken Sie neue Debuggingworkflows in diesem umfassenden Verweis auf Die Debugfeatures von Microsoft Edge DevTools.
title: JavaScript-Debugging-Referenz
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, Entwicklungstools
ms.openlocfilehash: 09a2d61269b2fe3a23a57ce58eb1c89b12a7639c
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398476"
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

# <a name="javascript-debugging-reference"></a><span data-ttu-id="a3424-104">JavaScript-Debugging-Referenz</span><span class="sxs-lookup"><span data-stu-id="a3424-104">JavaScript debugging reference</span></span>  

<span data-ttu-id="a3424-105">Entdecken Sie neue Debugworkflows mit dem folgenden umfassenden Verweis auf Die Debugfeatures von Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="a3424-105">Discover new debugging workflows with the following comprehensive reference of Microsoft Edge DevTools debugging features.</span></span>  

<span data-ttu-id="a3424-106">Um die Grundlagen des Debuggens zu erlernen, navigieren Sie zu Erste Schritte mit dem Debuggen von [JavaScript in Microsoft Edge DevTools][DevToolsJavascriptGetStarted].</span><span class="sxs-lookup"><span data-stu-id="a3424-106">To learn the basics of debugging, navigate to [Get Started With Debugging JavaScript In Microsoft Edge DevTools][DevToolsJavascriptGetStarted].</span></span>  

## <a name="pause-code-with-breakpoints"></a><span data-ttu-id="a3424-107">Anhalten von Code mit Haltepunkten</span><span class="sxs-lookup"><span data-stu-id="a3424-107">Pause code with breakpoints</span></span>  

<span data-ttu-id="a3424-108">Legen Sie einen Haltepunkt fest, damit Sie den Code in der Mitte der Laufzeit anhalten können.</span><span class="sxs-lookup"><span data-stu-id="a3424-108">Set a breakpoint so that you are able to pause your code in the middle of the runtime.</span></span>  

<span data-ttu-id="a3424-109">Informationen zum Festlegen von Haltepunkten finden Sie unter [Pause Your Code With Breakpoints][DevToolsJavascriptBreakpoints].</span><span class="sxs-lookup"><span data-stu-id="a3424-109">To learn how to set breakpoints, navigate to [Pause Your Code With Breakpoints][DevToolsJavascriptBreakpoints].</span></span>  

## <a name="step-through-code"></a><span data-ttu-id="a3424-110">Schritt durch Code</span><span class="sxs-lookup"><span data-stu-id="a3424-110">Step through code</span></span>  

<span data-ttu-id="a3424-111">Sobald Der Code angehalten wurde, durchschritten Sie ihn, eine Zeile nach der anderen, und untersuchen Sie dabei den Steuerungsfluss und die Eigenschaftswerte.</span><span class="sxs-lookup"><span data-stu-id="a3424-111">Once your code is paused, step through it, one line at a time, investigating control flow and property values along the way.</span></span>  

### <a name="step-over-line-of-code"></a><span data-ttu-id="a3424-112">Schritt über Codezeile</span><span class="sxs-lookup"><span data-stu-id="a3424-112">Step over line of code</span></span>  

<span data-ttu-id="a3424-113">Wenn sie in einer Codezeile angehalten wird, die eine Funktion enthält, die für das Problem, das Sie debuggen, nicht relevant ist, wählen Sie die Schaltfläche **Schritt** über \( Schritt über ![ \) aus, um die Funktion auszuführen, ohne sie ][ImageStepOverIcon] auszuführen.</span><span class="sxs-lookup"><span data-stu-id="a3424-113">When paused on a line of code containing a function that is not relevant to the problem you are debugging, choose the **Step over** \(![Step over][ImageStepOverIcon]\) button to run the function without stepping into it.</span></span>  

:::image type="complex" source="../media/javascript-source-page-debugger-step-over-next-function-call.msft.png" alt-text="Wählen Sie Schritt über" lightbox="../media/javascript-source-page-debugger-step-over-next-function-call.msft.png":::
   <span data-ttu-id="a3424-115">Wählen Sie **Schritt über**</span><span class="sxs-lookup"><span data-stu-id="a3424-115">Choose **Step over**</span></span>  
:::image-end:::  

<span data-ttu-id="a3424-116">Angenommen, Sie debuggen den folgenden Codeausschnitt.</span><span class="sxs-lookup"><span data-stu-id="a3424-116">For example, suppose you are debugging the following code snippet.</span></span>  

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

<span data-ttu-id="a3424-117">Sie werden auf `A` angehalten.</span><span class="sxs-lookup"><span data-stu-id="a3424-117">You are paused on `A`.</span></span>  <span data-ttu-id="a3424-118">Nachdem Sie **Schritt über**auswählen, führt DevTools den ganzen Code in der Funktion aus, über die Sie schrittweise gehen, d. h. und `B` `C` .</span><span class="sxs-lookup"><span data-stu-id="a3424-118">After you choose **Step over**, DevTools runs all the code in the function that you are stepping over, which is `B` and `C`.</span></span>  <span data-ttu-id="a3424-119">DevTools hält dann auf `D` an.</span><span class="sxs-lookup"><span data-stu-id="a3424-119">DevTools then pauses on `D`.</span></span>  

### <a name="step-into-line-of-code"></a><span data-ttu-id="a3424-120">Schritt in Codezeile</span><span class="sxs-lookup"><span data-stu-id="a3424-120">Step into line of code</span></span>  

<span data-ttu-id="a3424-121">Wenn sie in einer Codezeile angehalten wird, die einen Funktionsaufruf enthält, der mit dem Problem im Zusammenhang steht, das Sie debuggen, wählen Sie die Schaltfläche **Schritt** in \( Schritt in ![ \) aus, um diese Funktion weiter ][ImageStepIntoIcon] zu untersuchen.</span><span class="sxs-lookup"><span data-stu-id="a3424-121">When paused on a line of code containing a function call that is related to the problem you are debugging, choose the **Step into** \(![Step into][ImageStepIntoIcon]\) button to investigate that function further.</span></span>  

:::image type="complex" source="../media/javascript-source-page-debugger-step-into-next-function-call.msft.png" alt-text="Wählen Sie Schritt in aus." lightbox="../media/javascript-source-page-debugger-step-into-next-function-call.msft.png":::
   <span data-ttu-id="a3424-123">Wählen Sie **Schritt in aus.**</span><span class="sxs-lookup"><span data-stu-id="a3424-123">Choose **Step into**</span></span>  
:::image-end:::  

<span data-ttu-id="a3424-124">Angenommen, Sie debuggen den folgenden Codeausschnitt.</span><span class="sxs-lookup"><span data-stu-id="a3424-124">For example, suppose you are debugging the following code snippet.</span></span>  

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

<span data-ttu-id="a3424-125">Sie werden auf `A` angehalten.</span><span class="sxs-lookup"><span data-stu-id="a3424-125">You are paused on `A`.</span></span>  <span data-ttu-id="a3424-126">Nachdem Sie **Schritt in auswählen,** führt DevTools diese Codezeile aus und hält dann auf `B` an.</span><span class="sxs-lookup"><span data-stu-id="a3424-126">After you choose **Step into**, DevTools runs this line of code, then pauses on `B`.</span></span>  

### <a name="step-out-of-line-of-code"></a><span data-ttu-id="a3424-127">Schritt aus der Codezeile</span><span class="sxs-lookup"><span data-stu-id="a3424-127">Step out of line of code</span></span>  

<span data-ttu-id="a3424-128">Wenn Sie innerhalb einer Funktion angehalten werden, die nicht mit dem Debugproblem im Zusammenhang steht, wählen Sie die Schaltfläche Step **out** \( ![ Step out \) aus, um den Rest des Codes der Funktion ][ImageStepOutIcon] auszuführen.</span><span class="sxs-lookup"><span data-stu-id="a3424-128">When paused inside of a function that is not related to the problem you are debugging, choose the **Step out** \(![Step out][ImageStepOutIcon]\) button to run the rest of the code of the function.</span></span>  

:::image type="complex" source="../media/javascript-source-page-debugger-step-out-of-current-function.msft.png" alt-text="Auswählen von Step out" lightbox="../media/javascript-source-page-debugger-step-out-of-current-function.msft.png":::
   <span data-ttu-id="a3424-130">Auswählen **von Step out**</span><span class="sxs-lookup"><span data-stu-id="a3424-130">Choose **Step out**</span></span>  
:::image-end:::  

<span data-ttu-id="a3424-131">Angenommen, Sie debuggen den folgenden Codeausschnitt.</span><span class="sxs-lookup"><span data-stu-id="a3424-131">For example, suppose you are debugging the following code snippet.</span></span>  

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

<span data-ttu-id="a3424-132">Sie werden auf `A` angehalten.</span><span class="sxs-lookup"><span data-stu-id="a3424-132">You are paused on `A`.</span></span>  <span data-ttu-id="a3424-133">Nachdem Sie **Step out**auswählen, führt DevTools den Rest des Codes in aus, der sich nur in diesem Beispiel befindet, und hält dann auf `getName()` `B` `C` an.</span><span class="sxs-lookup"><span data-stu-id="a3424-133">After you choose **Step out**, DevTools runs the rest of the code in `getName()`, which is just `B` in this example, and then pauses on `C`.</span></span>  

### <a name="run-all-code-up-to-a-specific-line"></a><span data-ttu-id="a3424-134">Ausführen des codes bis zu einer bestimmten Zeile</span><span class="sxs-lookup"><span data-stu-id="a3424-134">Run all code up to a specific line</span></span>  

<span data-ttu-id="a3424-135">Beim Debuggen einer langen Funktion gibt es möglicherweise eine Menge Code, der nicht mit dem Problem im Zusammenhang steht, das Sie debuggen.</span><span class="sxs-lookup"><span data-stu-id="a3424-135">When debugging a long function, there may be a lot of code that is not related to the problem you are debugging.</span></span>  

<span data-ttu-id="a3424-136">Sie können alle Zeilen durchschritten, aber das ist mühsam.</span><span class="sxs-lookup"><span data-stu-id="a3424-136">You may choose to step through all the lines, but that is tedious.</span></span>  <span data-ttu-id="a3424-137">Sie können einen Codepunkt in der Zeile festlegen, an der Sie interessiert sind, und dann die Schaltfläche Skriptausführung fortsetzen **\(** Skriptausführung fortsetzen \) auswählen, aber es gibt eine schnellere ![ ][ImageResumeScriptExecutionIcon] Möglichkeit.</span><span class="sxs-lookup"><span data-stu-id="a3424-137">You may choose to set a line-of-code breakpoint on the line in which you are interested and then choose the **Resume Script Execution** \(![Resume Script Execution][ImageResumeScriptExecutionIcon]\) button, but there is a faster way.</span></span>  

<span data-ttu-id="a3424-138">Zeigen Sie auf die Codezeile, an der Sie interessiert sind, öffnen Sie das Kontextmenü \(rechtsklicken\), und wählen Sie **Weiter zu hier aus.**</span><span class="sxs-lookup"><span data-stu-id="a3424-138">Hover on the line of code in which you are interested, open the contextual menu \(right-click\), and choose **Continue to here**.</span></span>  <span data-ttu-id="a3424-139">DevTools führt bis zu diesem Punkt den ganzen Code aus und hält dann in dieser Zeile an.</span><span class="sxs-lookup"><span data-stu-id="a3424-139">DevTools runs all of the code up to that point, and then pauses on that line.</span></span>  

:::image type="complex" source="../media/javascript-source-page-continue-to-here.msft.png" alt-text="Wählen Sie Weiter zu hier aus." lightbox="../media/javascript-source-page-continue-to-here.msft.png":::
   <span data-ttu-id="a3424-141">Wählen **Sie Weiter zu hier aus.**</span><span class="sxs-lookup"><span data-stu-id="a3424-141">Choose **Continue to here**</span></span>  
:::image-end:::  

### <a name="restart-the-top-function-of-the-call-stack"></a><span data-ttu-id="a3424-142">Starten Sie die oberste Funktion der Aufrufliste neu.</span><span class="sxs-lookup"><span data-stu-id="a3424-142">Restart the top function of the call stack</span></span>  

<span data-ttu-id="a3424-143">Wenn Sie in der ersten Zeile der obersten Funktion in Ihrer Aufrufliste anhalten und \*\*\*\* in einer Codezeile angehalten werden, zeigen Sie auf eine beliebige Stelle im Bereich Anrufliste, öffnen Sie das Kontextmenü \(klicken Sie mit der rechten Maustaste auf\), und wählen Sie Frame neu **starten**aus.</span><span class="sxs-lookup"><span data-stu-id="a3424-143">To pause on the first line of the top function in your call stack, while paused on a line of code, hover anywhere in the **Call Stack** pane, open the contextual menu \(right-click\), and choose **Restart Frame**.</span></span>  <span data-ttu-id="a3424-144">Die top-Funktion ist die letzte ausgeführte Funktion.</span><span class="sxs-lookup"><span data-stu-id="a3424-144">The top function is the last function that was run.</span></span>  

<span data-ttu-id="a3424-145">Der folgende Codeausschnitt ist ein Beispiel für einen schrittweisen Schritt.</span><span class="sxs-lookup"><span data-stu-id="a3424-145">The following code snippet is an example for you to step-through.</span></span>  

```javascript
function factorial(n) {
    var product = 0; // B
    for (var i = 1; i <= n; i++) {
      product += i;
    }
    return product; // A
}
```  

<span data-ttu-id="a3424-146">Sie werden auf `A` angehalten.</span><span class="sxs-lookup"><span data-stu-id="a3424-146">You are paused on `A`.</span></span>  <span data-ttu-id="a3424-147">Nachdem Sie **Frame neu starten**auswählen, sollten Sie auf angehalten werden, ohne jemals einen Haltepunkt festlegen oder `B` **skriptausführung fortsetzen auswählen zu müssen.**</span><span class="sxs-lookup"><span data-stu-id="a3424-147">After choosing **Restart Frame**, you should be paused on `B`, without ever setting a breakpoint or choosing **Resume script execution**.</span></span>  

:::image type="complex" source="../media/javascript-source-page-debugger-restart-frame.msft.png" alt-text="Wählen Sie Frame neu starten aus" lightbox="../media/javascript-source-page-debugger-restart-frame.msft.png":::
   <span data-ttu-id="a3424-149">Wählen **Sie Frame neu starten aus**</span><span class="sxs-lookup"><span data-stu-id="a3424-149">Choose **Restart Frame**</span></span>  
:::image-end:::  

### <a name="resume-script-runtime"></a><span data-ttu-id="a3424-150">Fortsetzen der Skriptlaufzeit</span><span class="sxs-lookup"><span data-stu-id="a3424-150">Resume script runtime</span></span>  

<span data-ttu-id="a3424-151">Wenn Sie die Laufzeit nach einer Pause ihres Skripts fortsetzen möchten, wählen Sie **die** Schaltfläche Skriptausführung fortsetzen \( ![ Skriptausführung fortsetzen ][ImageResumeScriptExecutionIcon] \) aus.</span><span class="sxs-lookup"><span data-stu-id="a3424-151">To continue the runtime after a pause of your script, choose the **Resume Script Execution** \(![Resume Script Execution][ImageResumeScriptExecutionIcon]\) button.</span></span>  <span data-ttu-id="a3424-152">DevTools führt das Skript bis zum nächsten Haltepunkt aus, falls dies der Fall ist.</span><span class="sxs-lookup"><span data-stu-id="a3424-152">DevTools runs the script up until the next breakpoint, if any.</span></span>  

:::image type="complex" source="../media/javascript-sources-get-started-js-resume-script-runtime.msft.png" alt-text="Wählen Sie Skriptausführung fortsetzen aus" lightbox="../media/javascript-sources-get-started-js-resume-script-runtime.msft.png":::
   <span data-ttu-id="a3424-154">Wählen Sie **Skriptausführung fortsetzen aus**</span><span class="sxs-lookup"><span data-stu-id="a3424-154">Choose **Resume script execution**</span></span>  
:::image-end:::  

#### <a name="force-script-runtime"></a><span data-ttu-id="a3424-155">Erzwingen der Skriptlaufzeit</span><span class="sxs-lookup"><span data-stu-id="a3424-155">Force script runtime</span></span>  

<span data-ttu-id="a3424-156">Um alle Haltepunkte zu ignorieren und die Fortsetzung der Ausführung des Skripts zu erzwingen, wählen Sie die Schaltfläche Skriptausführung fortsetzen **\(** Skriptausführung fortsetzen \) aus, und wählen Sie dann die Schaltfläche Skriptausführung erzwingen \( Skriptausführung erzwingen ![ ][ImageResumeScriptExecutionIcon] \*\*\*\* ![ ][ImageForceScriptExecutionIcon] \) aus.</span><span class="sxs-lookup"><span data-stu-id="a3424-156">To ignore all breakpoints and force your script to resume running, choose and hold the **Resume Script Execution** \(![Resume Script Execution][ImageResumeScriptExecutionIcon]\) button and then choose the **Force script execution** \(![Force script execution][ImageForceScriptExecutionIcon]\) button.</span></span>  

:::image type="complex" source="../media/javascript-sources-get-started-js-force-script-runtime.msft.png" alt-text="Auswählen der Skriptausführung erzwingen" lightbox="../media/javascript-sources-get-started-js-force-script-runtime.msft.png":::
   <span data-ttu-id="a3424-158">Auswählen **der Skriptausführung erzwingen**</span><span class="sxs-lookup"><span data-stu-id="a3424-158">Choose **Force script execution**</span></span>  
:::image-end:::  

### <a name="change-thread-context"></a><span data-ttu-id="a3424-159">Ändern des Threadkontexts</span><span class="sxs-lookup"><span data-stu-id="a3424-159">Change thread context</span></span>  

<span data-ttu-id="a3424-160">Wählen Sie bei der Arbeit mit Webmitarbeitern oder Servicemitarbeitern einen Kontext aus, der im **Bereich Threads** aufgeführt ist, um zu diesem Kontext zu wechseln.</span><span class="sxs-lookup"><span data-stu-id="a3424-160">When working with web workers or service workers, choose on a context listed in the **Threads** pane to switch to that context.</span></span>  <span data-ttu-id="a3424-161">Das blaue Pfeilsymbol gibt an, welcher Kontext aktuell ausgewählt ist.</span><span class="sxs-lookup"><span data-stu-id="a3424-161">The blue arrow icon represents which context is currently selected.</span></span>  

:::image type="complex" source="../media/javascript-sources-main-min-js-threads.msft.png" alt-text="Der Bereich Threads" lightbox="../media/javascript-sources-main-min-js-threads.msft.png":::
   <span data-ttu-id="a3424-163">Der **Bereich Threads**</span><span class="sxs-lookup"><span data-stu-id="a3424-163">The **Threads** pane</span></span>  
:::image-end:::  

<span data-ttu-id="a3424-164">Angenommen, Sie werden sowohl im Hauptskript als auch im Dienstarbeitsskript an einem Haltepunkt angehalten.</span><span class="sxs-lookup"><span data-stu-id="a3424-164">For example, suppose that you are paused on a breakpoint in both your main script and your service worker script.</span></span>  <span data-ttu-id="a3424-165">Sie möchten die lokalen und globalen Eigenschaften für den Dienstarbeitskontext anzeigen, aber im **Bereich Quellen** wird der Hauptskriptkontext angezeigt.</span><span class="sxs-lookup"><span data-stu-id="a3424-165">You want to view the local and global properties for the service worker context, but the **Sources** panel is showing the main script context.</span></span>  <span data-ttu-id="a3424-166">Durch Auswählen des Dienstarbeitseintrags im **Bereich Threads** sollten Sie in der Lage sein, zu diesem Kontext zu wechseln.</span><span class="sxs-lookup"><span data-stu-id="a3424-166">By choosing on the service worker entry in the **Threads** pane, you should be able to switch to that context.</span></span>  

## <a name="view-and-edit-local-closure-and-global-properties"></a><span data-ttu-id="a3424-167">Anzeigen und Bearbeiten lokaler, geschlossener und globaler Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a3424-167">View and edit local, closure, and global properties</span></span>  

<span data-ttu-id="a3424-168">Verwenden Sie den Bereich Bereich, \*\*\*\* um die Werte von Eigenschaften und Variablen in den lokalen, Schließ- und globalen Bereich anzuzeigen und zu bearbeiten, während sie in einer Codezeile angehalten werden.</span><span class="sxs-lookup"><span data-stu-id="a3424-168">While paused on a line of code, use the **Scope** pane to view and edit the values of properties and variables in the local, closure, and global scopes.</span></span>  

*   <span data-ttu-id="a3424-169">Doppelklicken Sie auf einen Eigenschaftswert, um ihn zu ändern.</span><span class="sxs-lookup"><span data-stu-id="a3424-169">Double-click a property value to change it.</span></span>  
*   <span data-ttu-id="a3424-170">Nicht aufzählbare Eigenschaften sind ausgegraut.</span><span class="sxs-lookup"><span data-stu-id="a3424-170">Non-enumerable properties are greyed out.</span></span>  

:::image type="complex" source="../media/javascript-sources-get-started-js-scope.msft.png" alt-text="Der Bereich Bereich" lightbox="../media/javascript-sources-get-started-js-scope.msft.png":::
   <span data-ttu-id="a3424-172">Der **Bereich Bereich**</span><span class="sxs-lookup"><span data-stu-id="a3424-172">The **Scope** pane</span></span>  
:::image-end:::  

## <a name="view-the-current-call-stack"></a><span data-ttu-id="a3424-173">Anzeigen der aktuellen Aufrufliste</span><span class="sxs-lookup"><span data-stu-id="a3424-173">View the current call stack</span></span>  

<span data-ttu-id="a3424-174">Während Sie in einer Codezeile \*\*\*\* angehalten werden, verwenden Sie den Bereich Anrufliste, um die Aufrufliste anzuzeigen, die Sie zu diesem Punkt enstanden hat.</span><span class="sxs-lookup"><span data-stu-id="a3424-174">While paused on a line of code, use the **Call Stack** pane to view the call stack that got you to this point.</span></span>  

<!--If you are working with async code, check the **Async** checkbox to enable async call stacks.  -->  

<span data-ttu-id="a3424-175">Wählen Sie einen Eintrag aus, um zur Codezeile zu springen, in der diese Funktion aufgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="a3424-175">Choose an entry to jump to the line of code where that function was called.</span></span>  <span data-ttu-id="a3424-176">Das blaue Pfeilsymbol stellt dar, welche Funktion DevTools derzeit hervorhebt.</span><span class="sxs-lookup"><span data-stu-id="a3424-176">The blue arrow icon represents which function DevTools is currently highlighting.</span></span>  

:::image type="complex" source="../media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty.msft.png" alt-text="Der Bereich "Anrufliste"" lightbox="../media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty.msft.png":::
   <span data-ttu-id="a3424-178">Der **Bereich "Anrufliste"**</span><span class="sxs-lookup"><span data-stu-id="a3424-178">The **Call Stack** pane</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="a3424-179">Wenn sie in einer Codezeile nicht angehalten wird, ist der Bereich **Anrufliste** leer.</span><span class="sxs-lookup"><span data-stu-id="a3424-179">When not paused on a line of code, the **Call Stack** pane is empty.</span></span>  

### <a name="copy-stack-trace"></a><span data-ttu-id="a3424-180">Kopieren der Stapelverfolgung</span><span class="sxs-lookup"><span data-stu-id="a3424-180">Copy stack trace</span></span>  

<!--
This should be moved to an "Export debug data" H2 section when there is enough content for that, but there is not right now, so it is here.
-->

<span data-ttu-id="a3424-181">Um die aktuelle Aufrufliste in die Zwischenablage zu kopieren, zeigen Sie auf eine beliebige Stelle im Bereich Anrufliste, öffnen Sie das Kontextmenü \(rechtsklicken\), und wählen Sie Stapelverfolgung kopieren **aus.** \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="a3424-181">to copy the current call stack to the clipboard, hover anywhere in the **Call Stack** pane, open the contextual menu \(right-click\), and choose **Copy stack trace**.</span></span>  

:::image type="complex" source="../media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty-copy-stack-trace.msft.png" alt-text="Wählen Sie Stapelverfolgung kopieren aus" lightbox="../media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty-copy-stack-trace.msft.png":::
   <span data-ttu-id="a3424-183">Wählen **Sie Stapelverfolgung kopieren aus**</span><span class="sxs-lookup"><span data-stu-id="a3424-183">Choose **Copy Stack Trace**</span></span>  
:::image-end:::  

<span data-ttu-id="a3424-184">Der folgende Codeausschnitt ist ein Beispiel für die Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="a3424-184">The following code snippet is an example of the output.</span></span>  

```javascript
getNumber1 (get-started.js:35)
inputsAreEmpty (get-started.js:22)
onChoose (get-started.js:15)
```  

## <a name="ignore-a-script-or-pattern-of-scripts"></a><span data-ttu-id="a3424-185">Ignorieren eines Skripts oder Skriptmusters</span><span class="sxs-lookup"><span data-stu-id="a3424-185">Ignore a script or pattern of scripts</span></span>  

<span data-ttu-id="a3424-186">Markieren Sie ein Skript als Bibliothekscode, wenn Sie dieses Skript beim Debuggen ignorieren möchten.</span><span class="sxs-lookup"><span data-stu-id="a3424-186">Mark a script as Library code when you want to ignore that script while debugging.</span></span>  <span data-ttu-id="a3424-187">Wenn sie als Bibliothekscode markiert sind, \*\*\*\* wird ein Skript im Bereich Aufrufliste verdeckt, und Sie treten niemals in die Funktionen des Skripts ein, wenn Sie den Code durchschritten.</span><span class="sxs-lookup"><span data-stu-id="a3424-187">When marked as Library code, a script is obscured in the **Call Stack** pane, and you never step into the functions of the script when you step through your code.</span></span>  

<span data-ttu-id="a3424-188">Der folgende Codeausschnitt ist ein Beispiel für einen schrittweisen Schritt.</span><span class="sxs-lookup"><span data-stu-id="a3424-188">The following code snippet is an example for you to step-through.</span></span>  

```javascript
function animate() {
    prepare();
    lib.doFancyStuff(); // A
    render();
}
```  

`A` <span data-ttu-id="a3424-189">ist eine Bibliothek eines Drittanbieters, der Sie vertrauen.</span><span class="sxs-lookup"><span data-stu-id="a3424-189">is a third-party library that you trust.</span></span>  <span data-ttu-id="a3424-190">Wenn Sie sicher sind, dass das Problem, das Sie debuggen, nicht mit der Bibliothek eines Drittanbieters in Zusammenhang steht, ist es sinnvoll, das Skript als **Bibliothekscode zu kennzeichnen.**</span><span class="sxs-lookup"><span data-stu-id="a3424-190">If you are confident that the problem you are debugging is not related to the third-party library, then it makes sense to mark the script as **Library code**.</span></span>  

### <a name="mark-a-script-as-library-code-from-the-editor-pane"></a><span data-ttu-id="a3424-191">Markieren eines Skripts als Bibliothekscode aus dem Editorbereich</span><span class="sxs-lookup"><span data-stu-id="a3424-191">Mark a script as Library code from the Editor pane</span></span>  

<span data-ttu-id="a3424-192">Führen Sie die folgenden Aktionen aus, um ein Skript **im** Editorbereich als **Bibliothekscode zu** markieren.</span><span class="sxs-lookup"><span data-stu-id="a3424-192">Complete the following actions to mark a script as **Library code** from the **Editor** pane.</span></span>  

1.  <span data-ttu-id="a3424-193">Öffnen Sie die Datei.</span><span class="sxs-lookup"><span data-stu-id="a3424-193">Open the file.</span></span>  
1.  <span data-ttu-id="a3424-194">Zeigen Sie auf eine beliebige Stelle, und öffnen Sie das Kontextmenü \(klicken Sie mit der rechten Maustaste\).</span><span class="sxs-lookup"><span data-stu-id="a3424-194">Hover anywhere and open the contextual menu \(right-click\).</span></span>  
1.  <span data-ttu-id="a3424-195">Wählen **Sie Als Bibliothekscode markieren aus.**</span><span class="sxs-lookup"><span data-stu-id="a3424-195">Choose **Mark as Library code**.</span></span>  
    
    :::image type="complex" source="../media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty-editor-mark-as-library-code.msft.png" alt-text="Markieren eines Skripts als Bibliothekscode aus dem Editorbereich" lightbox="../media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty-editor-mark-as-library-code.msft.png":::
       <span data-ttu-id="a3424-197">Markieren eines Skripts **als Bibliothekscode** aus dem **Editorbereich**</span><span class="sxs-lookup"><span data-stu-id="a3424-197">Mark a script as **Library code** from the **Editor** pane</span></span>  
    :::image-end:::  
    
### <a name="mark-a-script-as-library-code-from-the-call-stack-pane"></a><span data-ttu-id="a3424-198">Markieren eines Skripts als Bibliothekscode aus dem Bereich "Aufrufliste"</span><span class="sxs-lookup"><span data-stu-id="a3424-198">Mark a script as Library code from the Call Stack pane</span></span>  

<span data-ttu-id="a3424-199">Führen Sie die folgenden Aktionen aus, um ein Skript **im** Bereich Aufrufliste als **Bibliothekscode zu** markieren.</span><span class="sxs-lookup"><span data-stu-id="a3424-199">Complete the following actions to mark a script as **Library code** from the **Call Stack** pane.</span></span>  

1.  <span data-ttu-id="a3424-200">Zeigen Sie auf eine Funktion aus dem Skript, und öffnen Sie das Kontextmenü \(klicken Sie mit der rechten Maustaste\).</span><span class="sxs-lookup"><span data-stu-id="a3424-200">Hover on a function from the script and open the contextual menu \(right-click\).</span></span>  
1.  <span data-ttu-id="a3424-201">Wählen **Sie Als Bibliothekscode markieren aus.**</span><span class="sxs-lookup"><span data-stu-id="a3424-201">Choose **Mark as Library code**.</span></span>  
    
    :::image type="complex" source="../media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty-call-stack-mark-as-library-code.msft.png" alt-text="Markieren eines Skripts als Bibliothekscode aus dem Bereich "Aufrufliste"" lightbox="../media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty-call-stack-mark-as-library-code.msft.png":::
       <span data-ttu-id="a3424-203">Markieren eines Skripts **als Bibliothekscode** aus dem **Bereich "Aufrufliste"**</span><span class="sxs-lookup"><span data-stu-id="a3424-203">Mark a script as **Library code** from the **Call Stack** pane</span></span>  
    :::image-end:::  
    
### <a name="mark-a-script-as-library-code-from-settings"></a><span data-ttu-id="a3424-204">Markieren eines Skripts als Bibliothekscode in den Einstellungen</span><span class="sxs-lookup"><span data-stu-id="a3424-204">Mark a script as Library code from Settings</span></span>  

<span data-ttu-id="a3424-205">Führen Sie die folgenden Aktionen aus, um ein einzelnes Skript oder Muster von Skripts aus Einstellungen **zu markieren.**</span><span class="sxs-lookup"><span data-stu-id="a3424-205">Complete the following actions to mark a single script or pattern of scripts from **Settings**.</span></span>  

1.  <span data-ttu-id="a3424-206">Öffnen [Sie Einstellungen][DevToolsCustomize].</span><span class="sxs-lookup"><span data-stu-id="a3424-206">Open [Settings][DevToolsCustomize].</span></span>  
1.  <span data-ttu-id="a3424-207">Navigieren Sie zur **Codeeinstellung Bibliothek.**</span><span class="sxs-lookup"><span data-stu-id="a3424-207">Navigate to the **Library code** setting.</span></span>  
1.  <span data-ttu-id="a3424-208">Wählen **Sie Muster hinzufügen aus.**</span><span class="sxs-lookup"><span data-stu-id="a3424-208">Choose **Add pattern**.</span></span>  
1.  <span data-ttu-id="a3424-209">Geben Sie den Skriptnamen oder ein Regexmuster von Skriptnamen ein, die als **Bibliothekscode zu markieren sind.**</span><span class="sxs-lookup"><span data-stu-id="a3424-209">Enter the script name or a regex pattern of script names to mark as **Library code**.</span></span>  
1.  <span data-ttu-id="a3424-210">Wählen Sie **Hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="a3424-210">Choose **Add**.</span></span>  
    
    :::image type="complex" source="../media/javascript-framework-library-code.msft.png" alt-text="Markieren eines Skripts als Bibliothekscode in den Einstellungen" lightbox="../media/javascript-framework-library-code.msft.png":::
       <span data-ttu-id="a3424-212">Markieren eines Skripts **als Bibliothekscode in** **den Einstellungen**</span><span class="sxs-lookup"><span data-stu-id="a3424-212">Mark a script as **Library code** from **Settings**</span></span>  
    :::image-end:::  
    
## <a name="run-snippets-of-debug-code-from-any-page"></a><span data-ttu-id="a3424-213">Ausführen von Codeausschnitten für debuggen von einer beliebigen Seite</span><span class="sxs-lookup"><span data-stu-id="a3424-213">Run snippets of debug code from any page</span></span>  

<span data-ttu-id="a3424-214">Wenn Sie immer wieder denselben Debugcode in der Konsole ausführen, sollten Sie Codeausschnitte in Betracht ziehen.</span><span class="sxs-lookup"><span data-stu-id="a3424-214">If you find yourself running the same debug code in the Console over and over, consider Snippets.</span></span>  <span data-ttu-id="a3424-215">Codeausschnitte sind Laufzeitskripts, die Sie in DevTools erstellen, speichern und ausführen.</span><span class="sxs-lookup"><span data-stu-id="a3424-215">Snippets are runtime scripts that you author, store, and run within DevTools.</span></span>  

<span data-ttu-id="a3424-216">Weitere Informationen finden Sie unter [Ausführen von Codeausschnitten von beliebigen Seiten][DevToolsJavascriptSnippets].</span><span class="sxs-lookup"><span data-stu-id="a3424-216">To learn more, navigate to [Run Snippets of Code From Any Page][DevToolsJavascriptSnippets].</span></span>  

## <a name="watch-the-values-of-custom-javascript-expressions"></a><span data-ttu-id="a3424-217">Beobachten der Werte benutzerdefinierter JavaScript-Ausdrücke</span><span class="sxs-lookup"><span data-stu-id="a3424-217">Watch the values of custom JavaScript expressions</span></span>  

<span data-ttu-id="a3424-218">Verwenden Sie den **Bereich "Watch",** um die Werte benutzerdefinierter Ausdrücke zu beobachten.</span><span class="sxs-lookup"><span data-stu-id="a3424-218">Use the **Watch** pane to watch the values of custom expressions.</span></span>  <span data-ttu-id="a3424-219">Sie können einen beliebigen gültigen JavaScript-Ausdruck ansehen.</span><span class="sxs-lookup"><span data-stu-id="a3424-219">You may watch any valid JavaScript expression.</span></span>  

:::image type="complex" source="../media/javascript-sources-get-started-js-watch.msft.png" alt-text="Der Bereich "Watch"" lightbox="../media/javascript-sources-get-started-js-watch.msft.png":::
   <span data-ttu-id="a3424-221">Der **Bereich "Watch"**</span><span class="sxs-lookup"><span data-stu-id="a3424-221">The **Watch** pane</span></span>  
:::image-end:::  

*   <span data-ttu-id="a3424-222">Wählen Sie **die Schaltfläche Ausdruck** hinzufügen \( Ausdruck hinzufügen ![ ][ImageAddExpressionIcon] \) aus, um einen neuen Watchausdruck zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="a3424-222">Choose the **Add Expression** \(![Add Expression][ImageAddExpressionIcon]\) button to create a new watch expression.</span></span>  
*   <span data-ttu-id="a3424-223">Wählen Sie die **Schaltfläche Aktualisieren** \( ![ Aktualisieren ][ImageRefreshIcon] \) aus, um die Werte aller vorhandenen Ausdrücke zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="a3424-223">Choose the **Refresh** \(![Refresh][ImageRefreshIcon]\) button to refresh the values of all existing expressions.</span></span>  <span data-ttu-id="a3424-224">Werte werden automatisch aktualisiert, während Code schrittweise durchschritten wird.</span><span class="sxs-lookup"><span data-stu-id="a3424-224">Values automatically refresh while stepping through code.</span></span>  
*   <span data-ttu-id="a3424-225">Zeigen Sie auf einen Ausdruck, und wählen Sie die Schaltfläche **Ausdruck** löschen \( ![ Ausdruck löschen ][ImageDeleteExpressionIcon] \) aus, um ihn zu löschen.</span><span class="sxs-lookup"><span data-stu-id="a3424-225">Hover on an expression and choose the **Delete Expression** \(![Delete Expression][ImageDeleteExpressionIcon]\) button to delete it.</span></span>  

## <a name="make-a-minified-file-readable"></a><span data-ttu-id="a3424-226">Lesen einer verminten Datei</span><span class="sxs-lookup"><span data-stu-id="a3424-226">Make a minified file readable</span></span>  

<span data-ttu-id="a3424-227">Wählen Sie **die Schaltfläche Format** \( Format ![ \) aus, um eine verminte Datei lesbar ][ImageFormatIcon] zu machen.</span><span class="sxs-lookup"><span data-stu-id="a3424-227">Choose the **Format** \(![Format][ImageFormatIcon]\) button to make a minified file human-readable.</span></span>  

:::image type="complex" source="../media/javascript-sources-html-non-minified.msft.png" alt-text="Die Schaltfläche Format" lightbox="../media/javascript-sources-html-non-minified.msft.png":::
   <span data-ttu-id="a3424-229">Die **Schaltfläche Format**</span><span class="sxs-lookup"><span data-stu-id="a3424-229">The **Format** button</span></span>  
:::image-end:::  

## <a name="edit-a-script"></a><span data-ttu-id="a3424-230">Bearbeiten eines Skripts</span><span class="sxs-lookup"><span data-stu-id="a3424-230">Edit a script</span></span>  

<span data-ttu-id="a3424-231">Beim Beheben eines Fehlers möchten Sie häufig einige Änderungen an Ihrem #A0 testen.</span><span class="sxs-lookup"><span data-stu-id="a3424-231">When fixing a bug, you often want to test out some changes to your JavaScript code.</span></span>  <span data-ttu-id="a3424-232">Sie müssen die Änderungen nicht in einem externen Editor oder einer IDE vornehmen und dann die Seite aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="a3424-232">You do not need to make the changes in an external editor or IDE and then refresh the page.</span></span>  <span data-ttu-id="a3424-233">Sie können Ihr Skript in DevTools bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="a3424-233">You may edit your script in DevTools.</span></span>  

<span data-ttu-id="a3424-234">Führen Sie die folgenden Aktionen aus, um ein Skript zu bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="a3424-234">Complete the following actions to edit a script.</span></span>  

1.  <span data-ttu-id="a3424-235">Öffnen Sie die Datei im **Editorbereich** des **Bereichs Quellen.**</span><span class="sxs-lookup"><span data-stu-id="a3424-235">Open the file in the **Editor** pane of the **Sources** panel.</span></span>  
1.  <span data-ttu-id="a3424-236">Nehmen Sie Ihre Änderungen im **Editorbereich** vor.</span><span class="sxs-lookup"><span data-stu-id="a3424-236">Make your changes in the **Editor** pane.</span></span>  
1.  <span data-ttu-id="a3424-237">Wählen `Ctrl` + `S` Sie \(Windows, Linux\) oder `Command` + `S` \(macOS\) aus, um zu speichern.</span><span class="sxs-lookup"><span data-stu-id="a3424-237">Select `Ctrl`+`S` \(Windows, Linux\) or `Command`+`S` \(macOS\) to save.</span></span>  <span data-ttu-id="a3424-238">DevTools patches the entire JS file into the JavaScript engine of Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="a3424-238">DevTools patches the entire JS file into the JavaScript engine of Microsoft Edge.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-html-minified.msft.png" alt-text="Der Editorbereich" lightbox="../media/javascript-sources-html-minified.msft.png":::
       <span data-ttu-id="a3424-240">Der **Editorbereich**</span><span class="sxs-lookup"><span data-stu-id="a3424-240">The **Editor** pane</span></span>  
    :::image-end:::  
     
## <a name="disable-javascript"></a><span data-ttu-id="a3424-241">JavaScript deaktivieren</span><span class="sxs-lookup"><span data-stu-id="a3424-241">Disable JavaScript</span></span>  

<span data-ttu-id="a3424-242">Navigieren Sie [zu Deaktivieren von JavaScript mit Microsoft Edge DevTools][DevToolsJavascriptDisable].</span><span class="sxs-lookup"><span data-stu-id="a3424-242">Navigate to [Disable JavaScript with Microsoft Edge DevTools][DevToolsJavascriptDisable].</span></span>  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="a3424-243">Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen</span><span class="sxs-lookup"><span data-stu-id="a3424-243">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

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

[DevToolsJavascriptBreakpoints]: ./breakpoints.md "So halten Sie Ihren Code mit Haltepunkten in Microsoft Edge DevTools | Microsoft Docs"  
[DevToolsJavascriptDisable]: ./disable.md "Deaktivieren von JavaScript mit Microsoft Edge DevTools | Microsoft Docs"  
[DevToolsJavascriptGetStarted]: ./index.md "Erste Schritte mit dem Debuggen von JavaScript in Microsoft Edge DevTools | Microsoft Docs"  
[DevToolsJavascriptSnippets]: ./snippets.md "Ausführen von Codeausschnitten von JavaScript auf jeder Seite mit Microsoft Edge DevTools | Microsoft Docs"  
[DevToolsCustomize]: ../customize/index.md "Anpassen von Microsoft Edge DevTools | Microsoft Docs"  

> [!NOTE]
> <span data-ttu-id="a3424-249">Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a3424-249">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="a3424-250">Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/javascript/reference) und wird von [Kayce Basken][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\) verfasst.</span><span class="sxs-lookup"><span data-stu-id="a3424-250">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/javascript/reference) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="a3424-252">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="a3424-252">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
