---
description: Entdecken Sie neue Debugworkflows in dieser umfassenden Referenz Microsoft Edge DevTools-Debuggingfeatures.
title: Verwenden der Debuggerfeatures
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, Entwicklungstools
ms.openlocfilehash: 6b15d317d4c720ab5ad76b7047532df101f69376
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/13/2021
ms.locfileid: "11564126"
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
# <a name="use-the-debugger-features"></a><span data-ttu-id="89352-104">Verwenden der Debuggerfeatures</span><span class="sxs-lookup"><span data-stu-id="89352-104">Use the debugger features</span></span>

<span data-ttu-id="89352-105">Dieser Artikel behandelt die Verwendung des Debuggers in Microsoft Edge DevTools, einschließlich des Festlegens eines Codezeile-Haltepunkts.</span><span class="sxs-lookup"><span data-stu-id="89352-105">This article covers how to use the debugger in Microsoft Edge DevTools, including how to set a line-of-code breakpoint.</span></span>  <span data-ttu-id="89352-106">Weitere Arten von Haltepunkten finden Sie unter [Pause your code with breakpoints][DevToolsJavascriptBreakpoints].</span><span class="sxs-lookup"><span data-stu-id="89352-106">To set other types of breakpoints, see [Pause your code with breakpoints][DevToolsJavascriptBreakpoints].</span></span>  

<span data-ttu-id="89352-107">Um die Grundlagen des Debuggens zu erlernen, navigieren Sie zu Erste Schritte mit dem Debuggen von [JavaScript in Microsoft Edge DevTools][DevToolsJavascriptGetStarted], einem Lernprogramm, das eine vorhandene, formularbasierte Webseite verwendet.</span><span class="sxs-lookup"><span data-stu-id="89352-107">To learn the basics of debugging, navigate to [Get started with debugging JavaScript in Microsoft Edge DevTools][DevToolsJavascriptGetStarted], which is a tutorial that uses an existing, form-based webpage.</span></span>  <span data-ttu-id="89352-108">Das Lernprogramm verfügt über Bildschirmaufzeichnungen, sodass Sie es überspringen können.</span><span class="sxs-lookup"><span data-stu-id="89352-108">The tutorial has screen captures, so you can skim it.</span></span>  <span data-ttu-id="89352-109">Sie können die Debuggerfeatures ganz einfach auf der Demowebseite ausprobieren.</span><span class="sxs-lookup"><span data-stu-id="89352-109">You can easily try out the debugger features by using the demo webpage.</span></span>

## <a name="view-and-edit-javascript-code"></a><span data-ttu-id="89352-110">Anzeigen und Bearbeiten von JavaScript-Code</span><span class="sxs-lookup"><span data-stu-id="89352-110">View and edit JavaScript code</span></span>

<span data-ttu-id="89352-111">Beim Beheben eines Fehlers möchten Sie häufig einige Änderungen an Ihrem #A0 ausprobieren.</span><span class="sxs-lookup"><span data-stu-id="89352-111">When fixing a bug, you often want to try out some changes to your JavaScript code.</span></span>  <span data-ttu-id="89352-112">Sie müssen die Änderungen nicht in einem externen Editor oder einer externen IDE vornehmen, die Datei erneut auf den Server hochladen und dann die Seite aktualisieren. Zum Testen von Änderungen können Sie stattdessen Ihren JavaScript-Code direkt in DevTools bearbeiten und das Ergebnis sofort anzeigen.</span><span class="sxs-lookup"><span data-stu-id="89352-112">You don't need to make the changes in an external editor or IDE, re-upload the file to the server, and then refresh the page; instead, to test changes, you can edit your JavaScript code directly in DevTools and see the result immediately.</span></span>  

<span data-ttu-id="89352-113">So zeigen Sie eine JavaScript-Datei an und bearbeiten sie:</span><span class="sxs-lookup"><span data-stu-id="89352-113">To view and edit a JavaScript file:</span></span>  

1.  <span data-ttu-id="89352-114">Navigieren Sie zum **Tool Quellen.**</span><span class="sxs-lookup"><span data-stu-id="89352-114">Navigate to the **Sources** tool.</span></span>  
1.  <span data-ttu-id="89352-115">Wählen Sie **im Bereich Navigator** Ihre Datei aus, um sie im **Editorbereich zu** öffnen.</span><span class="sxs-lookup"><span data-stu-id="89352-115">In the **Navigator** pane, select your file, to open it in the **Editor** pane.</span></span>
1.  <span data-ttu-id="89352-116">Bearbeiten Sie **ihre** Datei im Editorbereich.</span><span class="sxs-lookup"><span data-stu-id="89352-116">In the **Editor** pane, edit your file.</span></span>  
1.  <span data-ttu-id="89352-117">Wählen `Ctrl` + `S` Sie \(Windows, Linux\) oder `Command` + `S` \(macOS\) aus, um zu speichern.</span><span class="sxs-lookup"><span data-stu-id="89352-117">Select `Ctrl`+`S` \(Windows, Linux\) or `Command`+`S` \(macOS\) to save.</span></span>  <span data-ttu-id="89352-118">DevTools lädt dann die JavaScript-Datei in das JavaScript-Modul Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="89352-118">DevTools then loads the JavaScript file into the JavaScript engine of Microsoft Edge.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-html-minified.msft.png" alt-text="Der Editorbereich" lightbox="../media/javascript-sources-html-minified.msft.png":::
       <span data-ttu-id="89352-120">Der **Editorbereich**</span><span class="sxs-lookup"><span data-stu-id="89352-120">The **Editor** pane</span></span>  
    :::image-end:::  
     
## <a name="reformat-a-minified-javascript-file-with-pretty-print"></a><span data-ttu-id="89352-121">Neuschreiben einer minifizierten JavaScript-Datei mit Hübschdruck</span><span class="sxs-lookup"><span data-stu-id="89352-121">Reformat a minified JavaScript file with pretty-print</span></span>

<span data-ttu-id="89352-122">Um eine verminte Datei für den Menschen lesbar zu machen, wählen Sie am unteren Rand des Editorbereichs die Schaltfläche **Format** \( ![ Format ](../media/format-icon.msft.png) \) aus. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="89352-122">To make a minified file human-readable, choose the **Format** \(![Format](../media/format-icon.msft.png)\) button at the bottom of the **Editor** pane.</span></span>

:::image type="complex" source="../media/javascript-sources-html-non-minified.msft.png" alt-text="Die Schaltfläche Format" lightbox="../media/javascript-sources-html-non-minified.msft.png":::
   <span data-ttu-id="89352-124">Die **Schaltfläche Format**</span><span class="sxs-lookup"><span data-stu-id="89352-124">The **Format** button</span></span>  
:::image-end:::  

## <a name="set-a-breakpoint-to-pause-code"></a><span data-ttu-id="89352-125">Festlegen eines Haltepunkts zum Anhalten von Code</span><span class="sxs-lookup"><span data-stu-id="89352-125">Set a breakpoint, to pause code</span></span>

<span data-ttu-id="89352-126">Um den Code in der Mitte der Laufzeit anzuhalten, legen Sie einen Haltepunkt ein.</span><span class="sxs-lookup"><span data-stu-id="89352-126">To pause your code in the middle of the runtime, set a breakpoint.</span></span>  <span data-ttu-id="89352-127">Der grundlegendste und bekannte Typ von Haltepunkt ist ein Code-aus-Code-Haltepunkt.</span><span class="sxs-lookup"><span data-stu-id="89352-127">The most basic and well-known type of breakpoint is a line-of-code breakpoint.</span></span>

<span data-ttu-id="89352-128">Verwenden Sie einen Codezeile-Haltepunkt, wenn Sie den genauen Codebereich kennen, den Sie untersuchen müssen.</span><span class="sxs-lookup"><span data-stu-id="89352-128">Use a line-of-code breakpoint when you know the exact region of code that you need to investigate.</span></span>  <span data-ttu-id="89352-129">DevTools hält immer an der angegebenen Codezeile an, bevor sie ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="89352-129">DevTools always pauses at the specified line of code, before running it.</span></span>

<span data-ttu-id="89352-130">So legen Sie einen Codezeile-Haltepunkt ein:</span><span class="sxs-lookup"><span data-stu-id="89352-130">To set a line-of-code breakpoint:</span></span>  

1.  <span data-ttu-id="89352-131">Navigieren Sie zum **Tool Quellen.**</span><span class="sxs-lookup"><span data-stu-id="89352-131">Navigate to the **Sources** tool.</span></span>  
1.  <span data-ttu-id="89352-132">Öffnen Sie die Datei, die die Codezeile enthält.</span><span class="sxs-lookup"><span data-stu-id="89352-132">Open the file that contains the line of code.</span></span>  
1.  <span data-ttu-id="89352-133">Wählen Sie den Bereich links von der Zeilennummer für die Codezeile aus.</span><span class="sxs-lookup"><span data-stu-id="89352-133">Select the area to the left of the line number for the line of code.</span></span>  <span data-ttu-id="89352-134">Oder klicken Sie mit der rechten Maustaste auf die Zeilennummer, und wählen Sie **dann Haltepunkt hinzufügen aus.**</span><span class="sxs-lookup"><span data-stu-id="89352-134">Or, right-click the line number and then choose **Add breakpoint**.</span></span>  <span data-ttu-id="89352-135">Anschließend wird neben der Zeilennummer ein roter Kreis angezeigt, der einen Haltepunkt angibt.</span><span class="sxs-lookup"><span data-stu-id="89352-135">A red circle then appears next to the line number, indicating a breakpoint.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-page-js-breakpoint-30.msft.png" alt-text="Ein Codezeile-Haltepunkt" lightbox="../media/javascript-sources-page-js-breakpoint-30.msft.png":::
       <span data-ttu-id="89352-137">Ein Codezeile-Haltepunkt</span><span class="sxs-lookup"><span data-stu-id="89352-137">A line-of-code breakpoint</span></span>  
    :::image-end:::  

<span data-ttu-id="89352-138">Zeilen-von-Code-Haltepunkte können ineffizient festgelegt werden, insbesondere wenn Sie nicht genau wissen, wo sie aussehen sollen, oder wenn Ihre Codebasis groß ist.</span><span class="sxs-lookup"><span data-stu-id="89352-138">Line-of-code breakpoints may be inefficient to set, especially if you do not know exactly where to look, or if your codebase is large.</span></span>  <span data-ttu-id="89352-139">Um Beim Debuggen Zeit zu sparen, erfahren Sie, wie und wann die anderen Arten von Haltepunkten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="89352-139">To save time when debugging, learn how and when to use the other types of breakpoints.</span></span>  <span data-ttu-id="89352-140">Weitere Informationen finden Sie unter [Pause your code with breakpoints][DevToolsJavascriptBreakpoints].</span><span class="sxs-lookup"><span data-stu-id="89352-140">For more information, navigate to [Pause your code with breakpoints][DevToolsJavascriptBreakpoints].</span></span>

## <a name="step-through-code"></a><span data-ttu-id="89352-141">Schritt durch Code</span><span class="sxs-lookup"><span data-stu-id="89352-141">Step through code</span></span>  

<span data-ttu-id="89352-142">Nachdem Der Code an einem Haltepunkt angehalten wurde, gehen Sie durch den Code, eine Zeile nach der anderen, und untersuchen Sie dabei den Steuerungsfluss und die Eigenschaftswerte.</span><span class="sxs-lookup"><span data-stu-id="89352-142">After your code is paused at a breakpoint, step through the code, one line at a time, investigating control flow and property values along the way.</span></span>  

### <a name="step-over-line-of-code"></a><span data-ttu-id="89352-143">Schritt über Codezeile</span><span class="sxs-lookup"><span data-stu-id="89352-143">Step over line of code</span></span>  

<span data-ttu-id="89352-144">Wenn sie in einer Codezeile angehalten wird, die eine Funktion enthält, die für das Problem, das Sie debuggen, nicht relevant ist, wählen Sie die Schaltfläche **Schritt** über \( Schritt über ![ \) aus, um die Funktion auszuführen, ohne sie ](../media/step-over-icon.msft.png) auszuführen.</span><span class="sxs-lookup"><span data-stu-id="89352-144">When paused on a line of code containing a function that isn't relevant to the problem you are debugging, choose the **Step over** \(![Step over](../media/step-over-icon.msft.png)\) button to run the function without stepping into it.</span></span>  

:::image type="complex" source="../media/javascript-source-page-debugger-step-over-next-function-call.msft.png" alt-text="Wählen Sie Schritt über" lightbox="../media/javascript-source-page-debugger-step-over-next-function-call.msft.png":::
   <span data-ttu-id="89352-146">Wählen Sie **Schritt über**</span><span class="sxs-lookup"><span data-stu-id="89352-146">Choose **Step over**</span></span>  
:::image-end:::  

<span data-ttu-id="89352-147">Angenommen, Sie debuggen den folgenden Codeausschnitt.</span><span class="sxs-lookup"><span data-stu-id="89352-147">For example, suppose you are debugging the following code snippet.</span></span>  

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

<span data-ttu-id="89352-148">Sie werden auf `A` angehalten.</span><span class="sxs-lookup"><span data-stu-id="89352-148">You are paused on `A`.</span></span>  <span data-ttu-id="89352-149">Nachdem Sie **Schritt über**auswählen, führt DevTools den ganzen Code in der Funktion aus, über die Sie schrittweise gehen, d. h. und `B` `C` .</span><span class="sxs-lookup"><span data-stu-id="89352-149">After you choose **Step over**, DevTools runs all the code in the function that you are stepping over, which is `B` and `C`.</span></span>  <span data-ttu-id="89352-150">DevTools hält dann auf `D` an.</span><span class="sxs-lookup"><span data-stu-id="89352-150">DevTools then pauses on `D`.</span></span>  

### <a name="step-into-line-of-code"></a><span data-ttu-id="89352-151">Schritt in Codezeile</span><span class="sxs-lookup"><span data-stu-id="89352-151">Step into line of code</span></span>  

<span data-ttu-id="89352-152">Wenn sie in einer Codezeile angehalten wird, die einen Funktionsaufruf enthält, der mit dem Problem im Zusammenhang steht, das Sie debuggen, wählen Sie die Schaltfläche **Schritt** in \( Schritt in ![ \) aus, um diese Funktion weiter ](../media/step-into-icon.msft.png) zu untersuchen.</span><span class="sxs-lookup"><span data-stu-id="89352-152">When paused on a line of code containing a function call that is related to the problem you are debugging, choose the **Step into** \(![Step into](../media/step-into-icon.msft.png)\) button to investigate that function further.</span></span>  

:::image type="complex" source="../media/javascript-source-page-debugger-step-into-next-function-call.msft.png" alt-text="Wählen Sie Schritt in aus." lightbox="../media/javascript-source-page-debugger-step-into-next-function-call.msft.png":::
   <span data-ttu-id="89352-154">Wählen Sie **Schritt in aus.**</span><span class="sxs-lookup"><span data-stu-id="89352-154">Choose **Step into**</span></span>  
:::image-end:::  

<span data-ttu-id="89352-155">Angenommen, Sie debuggen den folgenden Codeausschnitt.</span><span class="sxs-lookup"><span data-stu-id="89352-155">For example, suppose you are debugging the following code snippet.</span></span>  

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

<span data-ttu-id="89352-156">Sie werden auf `A` angehalten.</span><span class="sxs-lookup"><span data-stu-id="89352-156">You are paused on `A`.</span></span>  <span data-ttu-id="89352-157">Nachdem Sie **Schritt in auswählen,** führt DevTools diese Codezeile aus und hält dann auf `B` an.</span><span class="sxs-lookup"><span data-stu-id="89352-157">After you choose **Step into**, DevTools runs this line of code, then pauses on `B`.</span></span>  

### <a name="step-out-of-line-of-code"></a><span data-ttu-id="89352-158">Schritt aus der Codezeile</span><span class="sxs-lookup"><span data-stu-id="89352-158">Step out of line of code</span></span>  

<span data-ttu-id="89352-159">Wenn Sie innerhalb einer Funktion angehalten werden, die nicht mit dem Problem im Zusammenhang steht, das Sie debuggen, wählen Sie die Schaltfläche Step **out** \( ![ Step out \) aus, um den Rest des Codes der Funktion ](../media/step-out-icon.msft.png) auszuführen.</span><span class="sxs-lookup"><span data-stu-id="89352-159">When paused inside of a function that isn't related to the problem you are debugging, choose the **Step out** \(![Step out](../media/step-out-icon.msft.png)\) button to run the rest of the code of the function.</span></span>  

:::image type="complex" source="../media/javascript-source-page-debugger-step-out-of-current-function.msft.png" alt-text="Auswählen von Step out" lightbox="../media/javascript-source-page-debugger-step-out-of-current-function.msft.png":::
   <span data-ttu-id="89352-161">Auswählen **von Step out**</span><span class="sxs-lookup"><span data-stu-id="89352-161">Choose **Step out**</span></span>  
:::image-end:::  

<span data-ttu-id="89352-162">Angenommen, Sie debuggen den folgenden Codeausschnitt.</span><span class="sxs-lookup"><span data-stu-id="89352-162">For example, suppose you are debugging the following code snippet.</span></span>  

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

<span data-ttu-id="89352-163">Sie werden auf `A` angehalten.</span><span class="sxs-lookup"><span data-stu-id="89352-163">You are paused on `A`.</span></span>  <span data-ttu-id="89352-164">Nachdem Sie **Step out**auswählen, führt DevTools den Rest des Codes in aus, der sich nur in diesem Beispiel befindet, und hält dann auf `getName()` `B` `C` an.</span><span class="sxs-lookup"><span data-stu-id="89352-164">After you choose **Step out**, DevTools runs the rest of the code in `getName()`, which is just `B` in this example, and then pauses on `C`.</span></span>  

### <a name="run-all-code-up-to-a-specific-line"></a><span data-ttu-id="89352-165">Ausführen des codes bis zu einer bestimmten Zeile</span><span class="sxs-lookup"><span data-stu-id="89352-165">Run all code up to a specific line</span></span>  

<span data-ttu-id="89352-166">Beim Debuggen einer langen Funktion gibt es möglicherweise eine Menge Code, der nicht mit dem Problem im Zusammenhang steht, das Sie debuggen.</span><span class="sxs-lookup"><span data-stu-id="89352-166">When debugging a long function, there may be a lot of code that isn't related to the problem you are debugging.</span></span>  

<span data-ttu-id="89352-167">Sie können alle Zeilen durchschritten, aber das ist mühsam.</span><span class="sxs-lookup"><span data-stu-id="89352-167">You may choose to step through all the lines, but that is tedious.</span></span>  <span data-ttu-id="89352-168">Sie können einen Codepunkt für die Zeile festlegen, an der Sie interessiert sind, und dann die Schaltfläche Skriptausführung fortsetzen **\(** Skriptausführung fortsetzen \) auswählen, aber es gibt eine schnellere ![ ](../media/resume-script-run-icon.msft.png) Möglichkeit.</span><span class="sxs-lookup"><span data-stu-id="89352-168">You may choose to set a line-of-code breakpoint on the line in which you are interested and then choose the **Resume script execution** \(![Resume script execution](../media/resume-script-run-icon.msft.png)\) button, but there is a faster way.</span></span>  

<span data-ttu-id="89352-169">Zeigen Sie auf die Codezeile, an der Sie interessiert sind, öffnen Sie das Kontextmenü \(rechtsklicken\), und wählen Sie **Weiter zu hier aus.**</span><span class="sxs-lookup"><span data-stu-id="89352-169">Hover on the line of code in which you are interested, open the contextual menu \(right-click\), and choose **Continue to here**.</span></span>  <span data-ttu-id="89352-170">DevTools führt bis zu diesem Punkt den ganzen Code aus und hält dann in dieser Zeile an.</span><span class="sxs-lookup"><span data-stu-id="89352-170">DevTools runs all of the code up to that point, and then pauses on that line.</span></span>  

:::image type="complex" source="../media/javascript-source-page-continue-to-here.msft.png" alt-text="Wählen Sie Weiter zu hier aus." lightbox="../media/javascript-source-page-continue-to-here.msft.png":::
   <span data-ttu-id="89352-172">Wählen **Sie Weiter zu hier aus.**</span><span class="sxs-lookup"><span data-stu-id="89352-172">Choose **Continue to here**</span></span>  
:::image-end:::  

### <a name="restart-the-top-function-of-the-call-stack"></a><span data-ttu-id="89352-173">Starten Sie die oberste Funktion der Aufrufliste neu.</span><span class="sxs-lookup"><span data-stu-id="89352-173">Restart the top function of the call stack</span></span>  

<span data-ttu-id="89352-174">Wenn Sie in der ersten Zeile der top-Funktion in Ihrer Aufrufliste anhalten und \*\*\*\* in einer Codezeile angehalten werden, zeigen Sie auf eine beliebige Stelle im Bereich Anrufliste, öffnen Sie das Kontextmenü \(klicken Sie mit der rechten Maustaste\), und wählen Sie Frame neu **starten**aus.</span><span class="sxs-lookup"><span data-stu-id="89352-174">To pause on the first line of the top function in your call stack, while paused on a line of code, hover anywhere in the **Call Stack** pane, open the contextual menu \(right-click\), and choose **Restart frame**.</span></span>  <span data-ttu-id="89352-175">Die top-Funktion ist die letzte ausgeführte Funktion.</span><span class="sxs-lookup"><span data-stu-id="89352-175">The top function is the last function that was run.</span></span>  

<span data-ttu-id="89352-176">Der folgende Codeausschnitt ist ein Beispiel für einen schrittweisen Schritt.</span><span class="sxs-lookup"><span data-stu-id="89352-176">The following code snippet is an example for you to step-through.</span></span>  

```javascript
function factorial(n) {
    var product = 0; // B
    for (var i = 1; i <= n; i++) {
      product += i;
    }
    return product; // A
}
```  

<span data-ttu-id="89352-177">Sie werden auf `A` angehalten.</span><span class="sxs-lookup"><span data-stu-id="89352-177">You are paused on `A`.</span></span>  <span data-ttu-id="89352-178">Nachdem Sie **den Frame Neu starten auswählen,** sollten Sie auf angehalten werden, ohne jemals einen Haltepunkt festlegen oder `B` **skriptausführung fortsetzen auswählen zu müssen.**</span><span class="sxs-lookup"><span data-stu-id="89352-178">After choosing **Restart frame**, you should be paused on `B`, without ever setting a breakpoint or choosing **Resume script execution**.</span></span>  

:::image type="complex" source="../media/javascript-source-page-debugger-restart-frame.msft.png" alt-text="Wählen Sie Frame neu starten aus" lightbox="../media/javascript-source-page-debugger-restart-frame.msft.png":::
   <span data-ttu-id="89352-180">Wählen Sie **Frame neu starten aus**</span><span class="sxs-lookup"><span data-stu-id="89352-180">Choose **Restart frame**</span></span>  
:::image-end:::  

### <a name="resume-script-runtime"></a><span data-ttu-id="89352-181">Fortsetzen der Skriptlaufzeit</span><span class="sxs-lookup"><span data-stu-id="89352-181">Resume script runtime</span></span>  

<span data-ttu-id="89352-182">Wenn Sie die Laufzeit nach einer Pause ihres Skripts fortsetzen möchten, wählen Sie **die** Schaltfläche Skriptausführung fortsetzen \( ![ Skriptausführung fortsetzen ](../media/resume-script-run-icon.msft.png) \) aus.</span><span class="sxs-lookup"><span data-stu-id="89352-182">To continue the runtime after a pause of your script, choose the **Resume script execution** \(![Resume script execution](../media/resume-script-run-icon.msft.png)\) button.</span></span>  <span data-ttu-id="89352-183">DevTools führt das Skript bis zum nächsten Haltepunkt aus, falls dies der Fall ist.</span><span class="sxs-lookup"><span data-stu-id="89352-183">DevTools runs the script up until the next breakpoint, if any.</span></span>  

:::image type="complex" source="../media/javascript-sources-get-started-js-resume-script-runtime.msft.png" alt-text="Wählen Sie Skriptausführung fortsetzen aus" lightbox="../media/javascript-sources-get-started-js-resume-script-runtime.msft.png":::
   <span data-ttu-id="89352-185">Wählen Sie **Skriptausführung fortsetzen aus**</span><span class="sxs-lookup"><span data-stu-id="89352-185">Choose **Resume script execution**</span></span>  
:::image-end:::  

#### <a name="force-script-runtime"></a><span data-ttu-id="89352-186">Erzwingen der Skriptlaufzeit</span><span class="sxs-lookup"><span data-stu-id="89352-186">Force script runtime</span></span>  

<span data-ttu-id="89352-187">Um alle Haltepunkte zu ignorieren und die Ausführung des Skripts zu erzwingen, klicken Sie auf die Schaltfläche Skriptausführung fortsetzen **\(** Skriptausführung fortsetzen \) und wählen Sie dann die Schaltfläche Skriptausführung erzwingen \( Skriptausführung erzwingen ![ ](../media/resume-script-run-icon.msft.png) \*\*\*\* ![ ](../media/force-script-run-icon.msft.png) \) aus.</span><span class="sxs-lookup"><span data-stu-id="89352-187">To ignore all breakpoints and force your script to continue to run, choose and hold the **Resume script execution** \(![Resume script execution](../media/resume-script-run-icon.msft.png)\) button and then choose the **Force script execution** \(![Force script execution](../media/force-script-run-icon.msft.png)\) button.</span></span>  

:::image type="complex" source="../media/javascript-sources-get-started-js-force-script-runtime.msft.png" alt-text="Auswählen der Skriptausführung erzwingen" lightbox="../media/javascript-sources-get-started-js-force-script-runtime.msft.png":::
   <span data-ttu-id="89352-189">Auswählen **der Skriptausführung erzwingen**</span><span class="sxs-lookup"><span data-stu-id="89352-189">Choose **Force script execution**</span></span>  
:::image-end:::  

### <a name="change-thread-context"></a><span data-ttu-id="89352-190">Ändern des Threadkontexts</span><span class="sxs-lookup"><span data-stu-id="89352-190">Change thread context</span></span>  

<span data-ttu-id="89352-191">Wählen Sie bei der Arbeit mit Webmitarbeitern oder Servicemitarbeitern einen Kontext aus, der im **Bereich Threads** aufgeführt ist, um zu diesem Kontext zu wechseln.</span><span class="sxs-lookup"><span data-stu-id="89352-191">When working with web workers or service workers, choose on a context listed in the **Threads** pane to switch to that context.</span></span>  <span data-ttu-id="89352-192">Das blaue Pfeilsymbol gibt an, welcher Kontext aktuell ausgewählt ist.</span><span class="sxs-lookup"><span data-stu-id="89352-192">The blue arrow icon represents which context is currently selected.</span></span>  

:::image type="complex" source="../media/javascript-sources-main-min-js-threads.msft.png" alt-text="Der Bereich Threads" lightbox="../media/javascript-sources-main-min-js-threads.msft.png":::
   <span data-ttu-id="89352-194">Der **Bereich Threads**</span><span class="sxs-lookup"><span data-stu-id="89352-194">The **Threads** pane</span></span>  
:::image-end:::  

<span data-ttu-id="89352-195">Angenommen, Sie werden sowohl im Hauptskript als auch im Dienstarbeitsskript an einem Haltepunkt angehalten.</span><span class="sxs-lookup"><span data-stu-id="89352-195">For example, suppose that you are paused on a breakpoint in both your main script and your service worker script.</span></span>  <span data-ttu-id="89352-196">Sie möchten die lokalen und globalen Eigenschaften für den Dienstarbeitskontext anzeigen, aber das **Tool Sources** zeigt den Hauptskriptkontext an.</span><span class="sxs-lookup"><span data-stu-id="89352-196">You want to view the local and global properties for the service worker context, but the **Sources** tool is showing the main script context.</span></span>  <span data-ttu-id="89352-197">Um zum Kontext der Dienstarbeitskraft zu wechseln, wählen Sie im **Bereich Threads** den Eintrag Service worker aus.</span><span class="sxs-lookup"><span data-stu-id="89352-197">To switch to the service worker context, in the **Threads** pane, choose the service worker entry.</span></span>  

## <a name="view-and-edit-properties-and-variables"></a><span data-ttu-id="89352-198">Anzeigen und Bearbeiten von Eigenschaften und Variablen</span><span class="sxs-lookup"><span data-stu-id="89352-198">View and edit properties and variables</span></span>

<span data-ttu-id="89352-199">Verwenden Sie den Bereich Bereich, \*\*\*\* um die Werte von Eigenschaften und Variablen in den lokalen, Schließ- und globalen Bereich anzuzeigen und zu bearbeiten, während sie in einer Codezeile angehalten werden.</span><span class="sxs-lookup"><span data-stu-id="89352-199">While paused on a line of code, use the **Scope** pane to view and edit the values of properties and variables in the local, closure, and global scopes.</span></span>  

*   <span data-ttu-id="89352-200">Doppelklicken Sie auf einen Eigenschaftswert, um ihn zu ändern.</span><span class="sxs-lookup"><span data-stu-id="89352-200">Double-click a property value to change it.</span></span>  
*   <span data-ttu-id="89352-201">Nicht aufzählbare Eigenschaften sind ausgegraut.</span><span class="sxs-lookup"><span data-stu-id="89352-201">Non-enumerable properties are greyed out.</span></span>  

:::image type="complex" source="../media/javascript-sources-get-started-js-scope.msft.png" alt-text="Der Bereich Bereich" lightbox="../media/javascript-sources-get-started-js-scope.msft.png":::
   <span data-ttu-id="89352-203">Der **Bereich Bereich**</span><span class="sxs-lookup"><span data-stu-id="89352-203">The **Scope** pane</span></span>  
:::image-end:::  

## <a name="watch-the-values-of-javascript-expressions"></a><span data-ttu-id="89352-204">Beobachten der Werte von JavaScript-Ausdrücken</span><span class="sxs-lookup"><span data-stu-id="89352-204">Watch the values of JavaScript expressions</span></span>  

<span data-ttu-id="89352-205">Verwenden Sie den **Bereich "Watch",** um die Werte benutzerdefinierter Ausdrücke zu beobachten.</span><span class="sxs-lookup"><span data-stu-id="89352-205">Use the **Watch** pane to watch the values of custom expressions.</span></span>  <span data-ttu-id="89352-206">Sie können einen beliebigen gültigen JavaScript-Ausdruck ansehen.</span><span class="sxs-lookup"><span data-stu-id="89352-206">You can watch any valid JavaScript expression.</span></span>  

:::image type="complex" source="../media/javascript-sources-get-started-js-watch.msft.png" alt-text="Der Bereich "Watch"" lightbox="../media/javascript-sources-get-started-js-watch.msft.png":::
   <span data-ttu-id="89352-208">Der **Bereich "Watch"**</span><span class="sxs-lookup"><span data-stu-id="89352-208">The **Watch** pane</span></span>  
:::image-end:::  

*   <span data-ttu-id="89352-209">Wählen Sie zum Erstellen eines neuen Watchausdrucks die Schaltfläche **Uhrausdruck** hinzufügen \( ![ Uhrausdruck ](../media/add-expression-icon.msft.png) hinzufügen \) aus.</span><span class="sxs-lookup"><span data-stu-id="89352-209">To create a new watch expression, select the **Add watch expression** \(![Add watch expression](../media/add-expression-icon.msft.png)\) button.</span></span>  
*   <span data-ttu-id="89352-210">Um die Werte aller vorhandenen Ausdrücke zu aktualisieren, wählen Sie die **Schaltfläche Aktualisieren** \( ![ Aktualisieren ](../media/refresh-icon.msft.png) \) aus.</span><span class="sxs-lookup"><span data-stu-id="89352-210">To refresh the values of all existing expressions, select the **Refresh** \(![Refresh](../media/refresh-icon.msft.png)\) button.</span></span>  <span data-ttu-id="89352-211">Werte werden automatisch aktualisiert, während Code schrittweise durchschritten wird.</span><span class="sxs-lookup"><span data-stu-id="89352-211">Values automatically refresh while stepping through code.</span></span>  
*   <span data-ttu-id="89352-212">Klicken Sie zum Löschen eines Uhrausdrucks mit der rechten Maustaste auf den Ausdruck, und wählen Sie dann **Watchausdruck** löschen \( ![ Watchausdruck ](../media/delete-expression-icon.msft.png) löschen \) aus.</span><span class="sxs-lookup"><span data-stu-id="89352-212">To delete a watch expression, right-click the expression and then select **Delete watch expression** \(![Delete watch expression](../media/delete-expression-icon.msft.png)\).</span></span>  

## <a name="view-the-call-stack"></a><span data-ttu-id="89352-213">Anzeigen der Aufrufliste</span><span class="sxs-lookup"><span data-stu-id="89352-213">View the call stack</span></span>  

<span data-ttu-id="89352-214">Während Sie in einer Codezeile \*\*\*\* angehalten werden, verwenden Sie den Bereich Anrufliste, um die Aufrufliste anzuzeigen, die Sie zu diesem Punkt enstanden hat.</span><span class="sxs-lookup"><span data-stu-id="89352-214">While paused on a line of code, use the **Call Stack** pane to view the call stack that got you to this point.</span></span>  

<!--If you are working with async code, check the **Async** checkbox to enable async call stacks.  -->  

<span data-ttu-id="89352-215">Wählen Sie einen Eintrag aus, um zur Codezeile zu springen, in der diese Funktion aufgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="89352-215">Choose an entry to jump to the line of code where that function was called.</span></span>  <span data-ttu-id="89352-216">Das blaue Pfeilsymbol stellt dar, welche Funktion DevTools derzeit hervorhebt.</span><span class="sxs-lookup"><span data-stu-id="89352-216">The blue arrow icon represents which function DevTools is currently highlighting.</span></span>  

:::image type="complex" source="../media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty.msft.png" alt-text="Der Bereich "Anrufliste"" lightbox="../media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty.msft.png":::
   <span data-ttu-id="89352-218">Der **Bereich "Anrufliste"**</span><span class="sxs-lookup"><span data-stu-id="89352-218">The **Call Stack** pane</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="89352-219">Wenn sie in einer Codezeile nicht angehalten wird, ist der Bereich **Anrufliste** leer.</span><span class="sxs-lookup"><span data-stu-id="89352-219">When not paused on a line of code, the **Call Stack** pane is empty.</span></span>  

### <a name="copy-stack-trace"></a><span data-ttu-id="89352-220">Kopieren der Stapelverfolgung</span><span class="sxs-lookup"><span data-stu-id="89352-220">Copy stack trace</span></span>  

<!--
This should be moved to an "Export debug data" H2 section when there is enough content for that, but there is not right now, so it is here.
-->

<span data-ttu-id="89352-221">Wenn Sie den aktuellen Aufrufstapel in die \*\*\*\* Zwischenablage kopieren möchten, zeigen Sie auf eine beliebige Stelle im Bereich Anrufliste, öffnen Sie das Kontextmenü \(rechtsklicken\), und wählen Sie Stapelverfolgung kopieren **aus.**</span><span class="sxs-lookup"><span data-stu-id="89352-221">To copy the current call stack to the clipboard, hover anywhere in the **Call Stack** pane, open the contextual menu \(right-click\), and choose **Copy stack trace**.</span></span>  

:::image type="complex" source="../media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty-copy-stack-trace.msft.png" alt-text="Wählen Sie Stapelverfolgung kopieren aus" lightbox="../media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty-copy-stack-trace.msft.png":::
   <span data-ttu-id="89352-223">Wählen **Sie Stapelverfolgung kopieren aus**</span><span class="sxs-lookup"><span data-stu-id="89352-223">Choose **Copy Stack Trace**</span></span>  
:::image-end:::  

<span data-ttu-id="89352-224">Der folgende Codeausschnitt ist ein Beispiel für die Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="89352-224">The following code snippet is an example of the output.</span></span>  

```javascript
getNumber1 (get-started.js:35)
inputsAreEmpty (get-started.js:22)
onChoose (get-started.js:15)
```  

## <a name="ignore-a-script-or-pattern-of-scripts"></a><span data-ttu-id="89352-225">Ignorieren eines Skripts oder Skriptmusters</span><span class="sxs-lookup"><span data-stu-id="89352-225">Ignore a script or pattern of scripts</span></span>  

<span data-ttu-id="89352-226">Markieren Sie ein Skript als Bibliothekscode, wenn Sie dieses Skript beim Debuggen ignorieren möchten.</span><span class="sxs-lookup"><span data-stu-id="89352-226">Mark a script as Library code when you want to ignore that script while debugging.</span></span>  <span data-ttu-id="89352-227">Wenn sie als Bibliothekscode markiert sind, \*\*\*\* wird ein Skript im Bereich Aufrufliste verdeckt, und Sie treten niemals in die Funktionen des Skripts ein, wenn Sie den Code durchschritten.</span><span class="sxs-lookup"><span data-stu-id="89352-227">When marked as Library code, a script is obscured in the **Call Stack** pane, and you never step into the functions of the script when you step through your code.</span></span>  

<span data-ttu-id="89352-228">Im folgenden Codeausschnitt wird in zeile beispielsweise verwendet , bei dem es sich um eine `A` `lib` Drittanbieterbibliothek handelt.</span><span class="sxs-lookup"><span data-stu-id="89352-228">For example, in the following code snippet, line `A` uses `lib`, which is a third-party library.</span></span>  <span data-ttu-id="89352-229">Wenn Sie sicher sind, dass das Problem, das Sie debuggen, nicht mit dieser Drittanbieterbibliothek in Zusammenhang steht, ist es sinnvoll, das Skript als **Bibliothekscode zu kennzeichnen.**</span><span class="sxs-lookup"><span data-stu-id="89352-229">If you are confident that the problem you are debugging is not related to that third-party library, then it makes sense to mark the script as **Library code**.</span></span>  

```javascript
function animate() {
    prepare();
    lib.doFancyStuff(); // A
    render();
}
```  

### <a name="mark-a-script-as-library-code-from-the-editor-pane"></a><span data-ttu-id="89352-230">Markieren eines Skripts als Bibliothekscode aus dem Editorbereich</span><span class="sxs-lookup"><span data-stu-id="89352-230">Mark a script as Library code from the Editor pane</span></span>  

<span data-ttu-id="89352-231">So markieren Sie ein Skript **im** Editorbereich als **Bibliothekscode:**</span><span class="sxs-lookup"><span data-stu-id="89352-231">To mark a script as **Library code** from the **Editor** pane:</span></span>  

1.  <span data-ttu-id="89352-232">Öffnen Sie die Datei.</span><span class="sxs-lookup"><span data-stu-id="89352-232">Open the file.</span></span>  
1.  <span data-ttu-id="89352-233">Zeigen Sie auf eine beliebige Stelle, und öffnen Sie das Kontextmenü \(klicken Sie mit der rechten Maustaste\).</span><span class="sxs-lookup"><span data-stu-id="89352-233">Hover anywhere and open the contextual menu \(right-click\).</span></span>  
1.  <span data-ttu-id="89352-234">Wählen **Sie Skript hinzufügen aus, um die Liste** zu ignorieren **(zuvor als Als Bibliothekscode markieren angezeigt).**</span><span class="sxs-lookup"><span data-stu-id="89352-234">Choose **Add script to ignore list** (previously shown as **Mark as Library code**).</span></span>  
    
    :::image type="complex" source="../media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty-editor-mark-as-library-code.msft.png" alt-text="Markieren eines Skripts als Bibliothekscode aus dem Editorbereich" lightbox="../media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty-editor-mark-as-library-code.msft.png":::
       <span data-ttu-id="89352-236">Markieren eines Skripts **als Bibliothekscode** aus dem **Editorbereich**</span><span class="sxs-lookup"><span data-stu-id="89352-236">Mark a script as **Library code** from the **Editor** pane</span></span>  
    :::image-end:::  
    
### <a name="mark-a-script-as-library-code-from-the-call-stack-pane"></a><span data-ttu-id="89352-237">Markieren eines Skripts als Bibliothekscode aus dem Bereich "Aufrufliste"</span><span class="sxs-lookup"><span data-stu-id="89352-237">Mark a script as Library code from the Call Stack pane</span></span>  

<span data-ttu-id="89352-238">So markieren Sie ein Skript als **Bibliothekscode** aus dem **Bereich "Aufrufliste":**</span><span class="sxs-lookup"><span data-stu-id="89352-238">To mark a script as **Library code** from the **Call Stack** pane:</span></span>  

1.  <span data-ttu-id="89352-239">Zeigen Sie auf eine Funktion aus dem Skript, und öffnen Sie das Kontextmenü \(klicken Sie mit der rechten Maustaste\).</span><span class="sxs-lookup"><span data-stu-id="89352-239">Hover on a function from the script and open the contextual menu \(right-click\).</span></span>  
1.  <span data-ttu-id="89352-240">Wählen **Sie Skript hinzufügen aus, um die Liste** zu ignorieren **(zuvor als Als Bibliothekscode markieren angezeigt).**</span><span class="sxs-lookup"><span data-stu-id="89352-240">Choose **Add script to ignore list** (previously shown as **Mark as Library code**).</span></span>  
    
    :::image type="complex" source="../media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty-call-stack-mark-as-library-code.msft.png" alt-text="Markieren eines Skripts als Bibliothekscode aus dem Bereich "Aufrufliste"" lightbox="../media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty-call-stack-mark-as-library-code.msft.png":::
       <span data-ttu-id="89352-242">Markieren eines Skripts **als Bibliothekscode** aus dem **Bereich "Aufrufliste"**</span><span class="sxs-lookup"><span data-stu-id="89352-242">Mark a script as **Library code** from the **Call Stack** pane</span></span>  
    :::image-end:::  
    
### <a name="mark-a-script-as-library-code-from-settings"></a><span data-ttu-id="89352-243">Markieren eines Skripts als Bibliothekscode aus Einstellungen</span><span class="sxs-lookup"><span data-stu-id="89352-243">Mark a script as Library code from Settings</span></span>  

<span data-ttu-id="89352-244">So markieren Sie ein einzelnes Skript oder Skriptmuster aus **Einstellungen:**</span><span class="sxs-lookup"><span data-stu-id="89352-244">To mark a single script or pattern of scripts from **Settings**:</span></span>  

1.  <span data-ttu-id="89352-245">Öffnen [Einstellungen][DevToolsCustomize].</span><span class="sxs-lookup"><span data-stu-id="89352-245">Open [Settings][DevToolsCustomize].</span></span>  
1.  <span data-ttu-id="89352-246">Navigieren Sie zur **Codeeinstellung Bibliothek.**</span><span class="sxs-lookup"><span data-stu-id="89352-246">Navigate to the **Library code** setting.</span></span>  
1.  <span data-ttu-id="89352-247">Wählen **Sie Muster hinzufügen aus.**</span><span class="sxs-lookup"><span data-stu-id="89352-247">Choose **Add pattern**.</span></span>  
1.  <span data-ttu-id="89352-248">Geben Sie den Skriptnamen oder ein Regexmuster von Skriptnamen ein, die als **Bibliothekscode zu markieren sind.**</span><span class="sxs-lookup"><span data-stu-id="89352-248">Enter the script name or a regex pattern of script names to mark as **Library code**.</span></span>  
1.  <span data-ttu-id="89352-249">Wählen Sie **Hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="89352-249">Choose **Add**.</span></span>  
    
    :::image type="complex" source="../media/javascript-framework-library-code.msft.png" alt-text="Markieren eines Skripts als Bibliothekscode aus Einstellungen" lightbox="../media/javascript-framework-library-code.msft.png":::
       <span data-ttu-id="89352-251">Markieren eines Skripts **als Bibliothekscode aus** **Einstellungen**</span><span class="sxs-lookup"><span data-stu-id="89352-251">Mark a script as **Library code** from **Settings**</span></span>  
    :::image-end:::  
    
## <a name="run-snippets-of-debug-code-from-any-page"></a><span data-ttu-id="89352-252">Ausführen von Codeausschnitten für debuggen von einer beliebigen Seite</span><span class="sxs-lookup"><span data-stu-id="89352-252">Run snippets of debug code from any page</span></span>  

<span data-ttu-id="89352-253">Wenn Sie immer wieder denselben Debugcode in der Konsole ausführen, sollten Sie Codeausschnitte in Betracht ziehen.</span><span class="sxs-lookup"><span data-stu-id="89352-253">If you find yourself running the same debug code in the Console over and over, consider Snippets.</span></span>  <span data-ttu-id="89352-254">Codeausschnitte sind Laufzeitskripts, die Sie in DevTools erstellen, speichern und ausführen.</span><span class="sxs-lookup"><span data-stu-id="89352-254">Snippets are runtime scripts that you author, store, and run within DevTools.</span></span>  

<span data-ttu-id="89352-255">Weitere [Informationen finden Sie unter Ausführen von Codeausschnitten von JavaScript auf einer beliebigen Webseite.][DevToolsJavascriptSnippets]</span><span class="sxs-lookup"><span data-stu-id="89352-255">See [Run snippets of JavaScript on any webpage][DevToolsJavascriptSnippets].</span></span>  

## <a name="see-also"></a><span data-ttu-id="89352-256">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="89352-256">See also</span></span>  

*   <span data-ttu-id="89352-257">[Erste Schritte Mit Debuggen von JavaScript in Microsoft Edge DevTools][DevToolsJavascriptGetStarted] – Ein einfaches, kurzes Lernprogramm mit vorhandenem Code mit Bildschirmaufzeichnungen.</span><span class="sxs-lookup"><span data-stu-id="89352-257">[Get Started With Debugging JavaScript In Microsoft Edge DevTools][DevToolsJavascriptGetStarted] - A simple, short tutorial using existing code, with screen captures.</span></span>
*   <span data-ttu-id="89352-258">[Übersicht über das Quellentool][DevToolsSourcesIndex] – Das **Tool Sources** enthält den JavaScript-Debugger und -Editor.</span><span class="sxs-lookup"><span data-stu-id="89352-258">[Sources tool overview][DevToolsSourcesIndex] - The **Sources** tool includes the JavaScript debugger and editor.</span></span>
*   <span data-ttu-id="89352-259">[Deaktivieren Sie JavaScript mit Microsoft Edge DevTools][DevToolsJavascriptDisable].</span><span class="sxs-lookup"><span data-stu-id="89352-259">[Disable JavaScript with Microsoft Edge DevTools][DevToolsJavascriptDisable].</span></span>

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="89352-260">Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen</span><span class="sxs-lookup"><span data-stu-id="89352-260">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevToolsJavascriptBreakpoints]: ./breakpoints.md "So halten Sie Ihren Code mit Haltepunkten in Microsoft Edge DevTools | Microsoft Docs"  
[DevToolsJavascriptDisable]: ./disable.md "Deaktivieren von JavaScript mit Microsoft Edge DevTools | Microsoft Docs"  
[DevToolsJavascriptGetStarted]: ./index.md "Erste Schritte mit dem Debuggen von JavaScript in Microsoft Edge DevTools | Microsoft Docs"  
[DevToolsJavascriptSnippets]: ./snippets.md "Führen Sie Codeausschnitte von JavaScript auf jeder Seite mit Microsoft Edge DevTools | Microsoft Docs"  
[DevToolsSourcesIndex]: ../sources/index.md "Übersicht über das | Microsoft Docs"  
[DevToolsCustomize]: ../customize/index.md "Anpassen Microsoft Edge DevTools | Microsoft Docs"  

> [!NOTE]
> <span data-ttu-id="89352-267">Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="89352-267">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="89352-268">Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/javascript/reference) und wird von [Kayce Basken][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\) verfasst.</span><span class="sxs-lookup"><span data-stu-id="89352-268">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/javascript/reference) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="89352-270">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="89352-270">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  
