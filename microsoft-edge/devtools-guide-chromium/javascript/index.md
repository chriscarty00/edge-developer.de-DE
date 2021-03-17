---
description: Erfahren Sie, wie Sie Microsoft Edge DevTools verwenden, um JavaScript-Fehler zu finden und zu beheben.
title: Erste Schritte mit dem Debuggen von JavaScript in Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/08/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, Entwicklungstools
ms.openlocfilehash: bbfb766bcc03e4c4fe0f975f1ecfccbef08084be
ms.sourcegitcommit: 4b9fb5c1176fdaa5e3c60af2b84e38d5bb86cd81
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/16/2021
ms.locfileid: "11439465"
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
# <a name="get-started-with-debugging-javascript-in-microsoft-edge-devtools"></a><span data-ttu-id="12c32-104">Erste Schritte mit dem Debuggen von JavaScript in Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="12c32-104">Get started with debugging JavaScript in Microsoft Edge DevTools</span></span>  

<span data-ttu-id="12c32-105">In diesem Artikel wird der grundlegende Workflow zum Debuggen von JavaScript-Problem in DevTools erläutert.</span><span class="sxs-lookup"><span data-stu-id="12c32-105">This article teaches you the basic workflow for debugging any JavaScript issue in DevTools.</span></span>  

## <a name="step-1-reproduce-the-bug"></a><span data-ttu-id="12c32-106">Schritt 1: Reproduzieren des Fehlers</span><span class="sxs-lookup"><span data-stu-id="12c32-106">Step 1: Reproduce the bug</span></span>  

<span data-ttu-id="12c32-107">Das Suchen einer Reihe von Aktionen, die einen Fehler konsistent reproduzieren, ist immer der erste Schritt zum Debuggen.</span><span class="sxs-lookup"><span data-stu-id="12c32-107">Finding a series of actions that consistently reproduce a bug is always the first step to debugging.</span></span>  

1.  <span data-ttu-id="12c32-108">Wählen **Sie Demo öffnen aus.**</span><span class="sxs-lookup"><span data-stu-id="12c32-108">Choose **Open Demo**.</span></span>  <span data-ttu-id="12c32-109">Halten `Control` Sie \(Windows, Linux\) oder `Command` \(macOS\) fest, und öffnen Sie die Demo auf einer neuen Browserregisterkarte.</span><span class="sxs-lookup"><span data-stu-id="12c32-109">Hold `Control` \(Windows, Linux\) or `Command` \(macOS\) and open the demo in a new browser tab.</span></span>  
    
    [<span data-ttu-id="12c32-110">Demo öffnen</span><span class="sxs-lookup"><span data-stu-id="12c32-110">Open Demo</span></span>][OpenDebugJSDemo]  
    
1.  <span data-ttu-id="12c32-111">Geben `5` Sie in das Textfeld Zahl **1** ein.</span><span class="sxs-lookup"><span data-stu-id="12c32-111">Enter `5` in the **Number 1** text box.</span></span>  
1.  <span data-ttu-id="12c32-112">Geben `1` Sie in das Textfeld Nummer **2** ein.</span><span class="sxs-lookup"><span data-stu-id="12c32-112">Enter `1` in the **Number 2** text box.</span></span>  
1.  <span data-ttu-id="12c32-113">Wählen **Sie Nummer 1 und Nummer 2 hinzufügen aus.**</span><span class="sxs-lookup"><span data-stu-id="12c32-113">Choose **Add Number 1 and Number 2**.</span></span>  <span data-ttu-id="12c32-114">Die Bezeichnung unterhalb der Schaltfläche sagt `5 + 1 = 51` .</span><span class="sxs-lookup"><span data-stu-id="12c32-114">The label below the button says `5 + 1 = 51`.</span></span>  <span data-ttu-id="12c32-115">Das Ergebnis sollte `6` sein.</span><span class="sxs-lookup"><span data-stu-id="12c32-115">The result should be `6`.</span></span>  <span data-ttu-id="12c32-116">Beheben Sie als Nächstes den Additionsfehler, bei dem es sich um den Fehler handelt.</span><span class="sxs-lookup"><span data-stu-id="12c32-116">Next, fix the addition error that is the bug.</span></span>  
    
    :::image type="complex" source="../media/javascript-js-demo-bad.msft.png" alt-text="5 + 1 führt zu 51, sollte aber 6 sein" lightbox="../media/javascript-js-demo-bad.msft.png":::
       `5 + 1` <span data-ttu-id="12c32-118">führt zu `51` , sollte aber</span><span class="sxs-lookup"><span data-stu-id="12c32-118">results in `51`, but should be</span></span> `6`  
    :::image-end:::  
    
## <a name="step-2-get-familiar-with-the-sources-tool-ui"></a><span data-ttu-id="12c32-119">Schritt 2: Machen Sie sich mit der Benutzeroberfläche des Quellentools vertraut</span><span class="sxs-lookup"><span data-stu-id="12c32-119">Step 2: Get familiar with the Sources tool UI</span></span>  

<span data-ttu-id="12c32-120">DevTools bietet viele verschiedene Tools für verschiedene Aufgaben.</span><span class="sxs-lookup"><span data-stu-id="12c32-120">DevTools provides many different tools for different tasks.</span></span>  <span data-ttu-id="12c32-121">Zu den verschiedenen Aufgaben gehören das Ändern von CSS, die Profilerstellung der Seitenladeleistung und die Überwachung von Netzwerkanforderungen.</span><span class="sxs-lookup"><span data-stu-id="12c32-121">Different tasks include changing CSS, profiling page-load performance, and monitoring network requests.</span></span>  <span data-ttu-id="12c32-122">Das **Tool Sources** ist der Ort, an dem Sie JavaScript debuggen.</span><span class="sxs-lookup"><span data-stu-id="12c32-122">The **Sources** tool is where you debug JavaScript.</span></span>  

1.  <span data-ttu-id="12c32-123">Um das **Konsolentool** in DevTools zu öffnen, wählen `Control` + `Shift` + `J` Sie \(Windows, Linux\) oder `Command` + `Option` + `J` \(macOS\).</span><span class="sxs-lookup"><span data-stu-id="12c32-123">To open the **Console** tool in DevTools, select `Control`+`Shift`+`J` \(Windows, Linux\) or `Command`+`Option`+`J` \(macOS\).</span></span>  
    
    :::image type="complex" source="../media/javascript-console-empty.msft.png" alt-text="Das Konsolentool" lightbox="../media/javascript-console-empty.msft.png":::
       <span data-ttu-id="12c32-125">Das **Konsolentool**</span><span class="sxs-lookup"><span data-stu-id="12c32-125">The **Console** tool</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="12c32-126">Wählen Sie das **Tool Quellen** aus.</span><span class="sxs-lookup"><span data-stu-id="12c32-126">Choose the **Sources** tool.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-sections.msft.png" alt-text="Das Tool "Quellen"" lightbox="../media/javascript-sources-sections.msft.png":::
       <span data-ttu-id="12c32-128">Das **Tool "Quellen"**</span><span class="sxs-lookup"><span data-stu-id="12c32-128">The **Sources** tool</span></span>  
    :::image-end:::  
    
<span data-ttu-id="12c32-129">Die **Benutzeroberfläche** des Quellentools hat drei Teile.</span><span class="sxs-lookup"><span data-stu-id="12c32-129">The **Sources** tool UI has three parts.</span></span>  

:::image type="complex" source="../media/javascript-sources-sections-annotated.msft.png" alt-text="Die 3 Teile der Benutzeroberfläche des Quellentools" lightbox="../media/javascript-sources-sections-annotated.msft.png":::
   <span data-ttu-id="12c32-131">Die 3 Teile der **Benutzeroberfläche des Quellentools**</span><span class="sxs-lookup"><span data-stu-id="12c32-131">The 3 parts of the **Sources** tool UI</span></span>  
:::image-end:::  

1.  <span data-ttu-id="12c32-132">Der **Bereich Dateinavigator** \(Abschnitt 1 in der vorherigen Abbildung\).</span><span class="sxs-lookup"><span data-stu-id="12c32-132">The **File Navigator** panel \(Section 1 in the previous figure\).</span></span>  <span data-ttu-id="12c32-133">Jede Datei, die die Webseite anfordert, wird hier aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="12c32-133">Every file that the webpage requests is listed here.</span></span>  
1.  <span data-ttu-id="12c32-134">Der **Code-Editor-Bereich** \(Abschnitt 2 in der vorherigen Abbildung\).</span><span class="sxs-lookup"><span data-stu-id="12c32-134">The **Code Editor** panel \(Section 2 in the previous figure\).</span></span>  <span data-ttu-id="12c32-135">Nachdem Sie eine Datei im Bereich **Dateinavigator** ausgewählt haben, wird der Inhalt dieser Datei hier angezeigt.</span><span class="sxs-lookup"><span data-stu-id="12c32-135">After selecting a file in the **File Navigator** pane, the contents of that file are displayed here.</span></span>  
1.  <span data-ttu-id="12c32-136">Der **JavaScript-Debugbereich** \(Abschnitt 3 in der vorherigen Abbildung\).</span><span class="sxs-lookup"><span data-stu-id="12c32-136">The **JavaScript Debugging** panel \(Section 3 in the previous figure\).</span></span>  <span data-ttu-id="12c32-137">Verschiedene Tools zum Überprüfen des JavaScript für die Webseite.</span><span class="sxs-lookup"><span data-stu-id="12c32-137">Various tools for inspecting the JavaScript for the webpage.</span></span>  <span data-ttu-id="12c32-138">Wenn Ihr DevTools-Fenster breit ist, wird dieser Bereich rechts neben dem **Code-Editor-Bereich** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="12c32-138">If your DevTools window is wide, this pane is displayed to the right of the **Code Editor** pane.</span></span>  
    
## <a name="step-3-pause-the-code-with-a-breakpoint"></a><span data-ttu-id="12c32-139">Schritt 3: Anhalten des Codes mit einem Haltepunkt</span><span class="sxs-lookup"><span data-stu-id="12c32-139">Step 3: Pause the code with a breakpoint</span></span>  

<span data-ttu-id="12c32-140">Eine gängige Methode zum Debuggen dieser Art von Problem ist das Einfügen mehrerer Anweisungen in den Code und anschließend das Überprüfen von Werten während der Ausführung `console.log()` des Skripts.</span><span class="sxs-lookup"><span data-stu-id="12c32-140">A common method for debugging this type of problem is to insert several `console.log()` statements into the code and then to inspect values as the script runs.</span></span>  <span data-ttu-id="12c32-141">Zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="12c32-141">For example:</span></span>  

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

<span data-ttu-id="12c32-142">Die `console.log()` -Methode kann den Auftrag erledigen, aber **haltepunkte machen** es schneller.</span><span class="sxs-lookup"><span data-stu-id="12c32-142">The `console.log()` method may get the job done, but **breakpoints** get it done faster.</span></span>  <span data-ttu-id="12c32-143">Mit einem Haltepunkt können Sie Ihren Code in der Mitte der Laufzeit anhalten und alle Werte zu diesem Zeitpunkt untersuchen.</span><span class="sxs-lookup"><span data-stu-id="12c32-143">A breakpoint allows you to pause your code in the middle of the runtime, and examine all values at that moment in time.</span></span>  <span data-ttu-id="12c32-144">Haltepunkte haben die folgenden Vorteile gegenüber der `console.log()` Methode.</span><span class="sxs-lookup"><span data-stu-id="12c32-144">Breakpoints have the following advantages over the `console.log()` method.</span></span>  

*   <span data-ttu-id="12c32-145">Mit müssen Sie den Quellcode manuell öffnen, den relevanten Code suchen, die Anweisungen einfügen und dann die Webseite aktualisieren, um die Nachrichten in der Konsole `console.log()` `console.log()` **anzuzeigen.**</span><span class="sxs-lookup"><span data-stu-id="12c32-145">With `console.log()`, you need to manually open the source code, find the relevant code, insert the `console.log()` statements, and then refresh the webpage to display the messages in the **Console**.</span></span>  <span data-ttu-id="12c32-146">Mit Haltepunkten können Sie den relevanten Code anhalten, ohne zu wissen, wie der Code strukturiert ist.</span><span class="sxs-lookup"><span data-stu-id="12c32-146">With breakpoints, you may pause on the relevant code without even knowing how the code is structured.</span></span>  
*   <span data-ttu-id="12c32-147">In Ihren `console.log()` Anweisungen müssen Sie jeden Wert explizit angeben, den Sie überprüfen möchten.</span><span class="sxs-lookup"><span data-stu-id="12c32-147">In your `console.log()` statements, you need to explicitly specify each value that you want to inspect.</span></span>  <span data-ttu-id="12c32-148">Mit Haltepunkten zeigt DevTools die Werte aller Variablen zu diesem Zeitpunkt an.</span><span class="sxs-lookup"><span data-stu-id="12c32-148">With breakpoints, DevTools shows you the values of all variables at that moment in time.</span></span>  <span data-ttu-id="12c32-149">Manchmal werden Variablen, die sich auf Ihren Code auswirken, ausgeblendet und verschleiert.</span><span class="sxs-lookup"><span data-stu-id="12c32-149">Sometimes variables that affect your code are hidden and obfuscated.</span></span>  
    
<span data-ttu-id="12c32-150">Kurz gesagt, haltepunkte können Ihnen helfen, Fehler schneller zu finden und zu beheben als die `console.log()` Methode.</span><span class="sxs-lookup"><span data-stu-id="12c32-150">In short, breakpoints may help you find and fix bugs faster than the `console.log()` method.</span></span>  

<span data-ttu-id="12c32-151">Wenn Sie zurück treten und überlegen, wie die App funktioniert, können Sie eine gebildete Vermutung treffen, dass die falsche Summe \( \) im Ereignislistener berechnet wird, der der Schaltfläche Nummer 1 und Nummer 2 hinzufügen zugeordnet `5 + 1 = 51` `click` ist. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="12c32-151">If you step back and think about how the app works, you may make an educated guess that the incorrect sum \(`5 + 1 = 51`\) is computed in the `click` event listener associated with the **Add Number 1 and Number 2** button.</span></span>  <span data-ttu-id="12c32-152">Daher möchten Sie den Code wahrscheinlich zu dem Zeitpunkt anhalten, zu dem der `click` Listener ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="12c32-152">So, you probably want to pause the code around the time that the `click` listener runs.</span></span>  <span data-ttu-id="12c32-153">**Mit Ereignislistener-Haltepunkten** können Sie genau dies tun:</span><span class="sxs-lookup"><span data-stu-id="12c32-153">**Event Listener Breakpoints** let you do exactly that:</span></span>  

1.  <span data-ttu-id="12c32-154">Wählen Sie **im Bereich JavaScript-Debugging** die **Option Ereignislistener-Haltepunkte** aus, um den Abschnitt zu erweitern.</span><span class="sxs-lookup"><span data-stu-id="12c32-154">In the **JavaScript Debugging** pane, choose **Event Listener Breakpoints** to expand the section.</span></span>  <span data-ttu-id="12c32-155">DevTools zeigt eine Liste erweiterbarer Ereigniskategorien an, z. B. **Animation** und **Zwischenablage.**</span><span class="sxs-lookup"><span data-stu-id="12c32-155">DevTools reveals a list of expandable event categories, such as **Animation** and **Clipboard**.</span></span>  
1.  <span data-ttu-id="12c32-156">Wählen Sie neben **der Kategorie Mouse-Ereignis** **die Option Erweitern** \( Symbol erweitern ![ ](../media/expand-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="12c32-156">Next to the **Mouse** event category, choose **Expand** \(![Expand icon](../media/expand-icon.msft.png)\).</span></span>  <span data-ttu-id="12c32-157">DevTools zeigt eine Liste von Mausereignissen an, z. B. **Klicken** **und Mousedown**.</span><span class="sxs-lookup"><span data-stu-id="12c32-157">DevTools reveals a list of mouse events, such as **click** and **mousedown**.</span></span>  <span data-ttu-id="12c32-158">Jedes Ereignis hat ein Kontrollkästchen daneben.</span><span class="sxs-lookup"><span data-stu-id="12c32-158">Each event has a checkbox next to it.</span></span>  
1.  <span data-ttu-id="12c32-159">Aktivieren Sie das Kontrollkästchen neben , um **auf zu klicken.**</span><span class="sxs-lookup"><span data-stu-id="12c32-159">Choose the checkbox next to **click**.</span></span>  <span data-ttu-id="12c32-160">DevTools ist jetzt so eingerichtet, dass es automatisch angehalten wird, wenn ein `click` Ereignislistener ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="12c32-160">DevTools is now set up to automatically pause when any `click` event listener runs.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-event-listener-breakpoint-mouse-click.msft.png" alt-text="Aktivieren Sie das Kontrollkästchen neben dem Klicken." lightbox="../media/javascript-sources-event-listener-breakpoint-mouse-click.msft.png":::
       <span data-ttu-id="12c32-162">Aktivieren Sie das Kontrollkästchen neben **dem Klicken.**</span><span class="sxs-lookup"><span data-stu-id="12c32-162">Choose the checkbox next to **click**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="12c32-163">Wählen Sie wieder auf der Demo **die Option Nummer 1 und Nummer 2** hinzufügen aus.</span><span class="sxs-lookup"><span data-stu-id="12c32-163">Back on the demo, choose **Add Number 1 and Number 2** again.</span></span>  <span data-ttu-id="12c32-164">DevTools hält die Demo an und hebt eine Codezeile im **Tool Quellen** hervor.</span><span class="sxs-lookup"><span data-stu-id="12c32-164">DevTools pauses the demo and highlights a line of code in the **Sources** tool.</span></span>  <span data-ttu-id="12c32-165">DevTools sollte in Zeile 16 in `get-started.js` anhalten.</span><span class="sxs-lookup"><span data-stu-id="12c32-165">DevTools should pause on line 16 in `get-started.js`.</span></span>  
    
    ```javascript
    if (inputsAreEmpty()) {
    ```  
    
    <span data-ttu-id="12c32-166">Wenn Sie in einer anderen Codezeile anhalten, wählen Sie **Skriptausführung** fortsetzen \( Skriptausführung fortsetzen \) aus, bis Sie in der richtigen ![ ](../media/resume-script-run-icon.msft.png) Zeile anhalten.</span><span class="sxs-lookup"><span data-stu-id="12c32-166">If you pause on a different line of code, choose **Resume Script Execution** \(![Resume Script Execution](../media/resume-script-run-icon.msft.png)\) until you pause on the correct line.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="12c32-167">Wenn Sie in einer anderen Zeile angehalten haben, verfügen Sie über eine Browsererweiterung, die einen Ereignislistener auf jeder besuchten `click` Webseite registriert.</span><span class="sxs-lookup"><span data-stu-id="12c32-167">If you paused on a different line, you have a browser extension that registers a `click` event listener on every webpage that you visit.</span></span>  <span data-ttu-id="12c32-168">Sie werden im Listener der `click` Erweiterung angehalten.</span><span class="sxs-lookup"><span data-stu-id="12c32-168">You are paused in the `click` listener of the extension.</span></span>  <span data-ttu-id="12c32-169">Wenn Sie den InPrivate-Modus verwenden, um **im**privaten Modus zu navigieren, wodurch alle Erweiterungen deaktiviert werden, wird möglicherweise jedes Mal angezeigt, dass Sie in der gewünschten Codezeile anhalten.</span><span class="sxs-lookup"><span data-stu-id="12c32-169">If you use InPrivate Mode to **browse in private**, which disables all extensions, you may see that you pause on the desired line of code every time.</span></span>  

<!--todo: add inprivate section when available -->  

<span data-ttu-id="12c32-170">**Ereignislistener-Haltepunkte** sind nur einer von vielen Arten von Haltepunkten, die in DevTools verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="12c32-170">**Event Listener Breakpoints** are just one of many types of breakpoints available in DevTools.</span></span>  <span data-ttu-id="12c32-171">Merken Sie sich alle verschiedenen Typen, um unterschiedliche Szenarien so schnell wie möglich zu debuggen.</span><span class="sxs-lookup"><span data-stu-id="12c32-171">Memorize all the different types to help you debug different scenarios as quickly as possible.</span></span>  <!--See [Pause Your Code With Breakpoints][JSBreakpoints] to learn when and how to use each type.  -->  

## <a name="step-4-step-through-the-code"></a><span data-ttu-id="12c32-172">Schritt 4: Schritt durch den Code</span><span class="sxs-lookup"><span data-stu-id="12c32-172">Step 4: Step through the code</span></span>  

<span data-ttu-id="12c32-173">Eine häufige Ursache für Fehler ist, wenn ein Skript in der falschen Reihenfolge ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="12c32-173">One common cause of bugs is when a script runs in the wrong order.</span></span>  <span data-ttu-id="12c32-174">Wenn Sie den Code schrittweise durchschritten haben, können Sie die Laufzeit Ihres Codes durchfingen.</span><span class="sxs-lookup"><span data-stu-id="12c32-174">Stepping through your code allows you to walk through the runtime of your code.</span></span>  <span data-ttu-id="12c32-175">Sie gehen eine Zeile gleichzeitig durch, um herauszufinden, wo Ihr Code in einer anderen Reihenfolge ausgeführt wird als erwartet.</span><span class="sxs-lookup"><span data-stu-id="12c32-175">You walk through one line at a time to help you figure out exactly where your code is running in a different order than you expect.</span></span>  <span data-ttu-id="12c32-176">Probieren Sie es jetzt aus:</span><span class="sxs-lookup"><span data-stu-id="12c32-176">Try it now:</span></span>  

1.  <span data-ttu-id="12c32-177">Wählen **Sie Schritt über nächsten Funktionsaufruf** \( Schritt über nächsten ![ Funktionsaufruf ](../media/step-over-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="12c32-177">Choose **Step over next function call** \(![Step over next function call](../media/step-over-icon.msft.png)\).</span></span>  <span data-ttu-id="12c32-178">DevTools führt den folgenden Code aus, ohne ihn zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="12c32-178">DevTools runs the following code without stepping into it.</span></span>  
    
    ```javascript
    if (inputsAreEmpty()) {
    ```  
    
    > [!NOTE]
    > <span data-ttu-id="12c32-179">DevTools überspringt einige Codezeilen.</span><span class="sxs-lookup"><span data-stu-id="12c32-179">DevTools skips a few lines of code.</span></span>  <span data-ttu-id="12c32-180">Dies liegt `inputsAreEmpty()` daran, dass false ausgewertet wird, sodass der Codeblock für die Anweisung `if` nicht ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="12c32-180">This is because `inputsAreEmpty()` evaluates as false, so the block of code for the `if` statement does not run.</span></span>  
    
1.  <span data-ttu-id="12c32-181">Wählen Sie **im Tool** Quellen von DevTools Schritt **in** nächsten Funktionsaufruf \( Schritt in nächsten Funktionsaufruf \) aus, um die Laufzeit der Funktion zu durchschritten, eine Zeile ![ ](../media/step-into-icon.msft.png) nach der `updateLabel()` anderen.</span><span class="sxs-lookup"><span data-stu-id="12c32-181">On the **Sources** tool of DevTools, choose **Step into next function call** \(![Step into next function call](../media/step-into-icon.msft.png)\) to step through the runtime of the `updateLabel()` function, one line at a time.</span></span>  
    
<span data-ttu-id="12c32-182">Das Überprüfen einer Zeile nach dem anderen ist die grundlegende Idee des Schrittweisen Durcharbeitens von Code.</span><span class="sxs-lookup"><span data-stu-id="12c32-182">Reviewing one line at a time is the basic idea of stepping through code.</span></span>  <span data-ttu-id="12c32-183">Wenn Sie den Code in `get-started.js` überprüfen, befindet sich der Fehler wahrscheinlich irgendwo in der `updateLabel()` Funktion.</span><span class="sxs-lookup"><span data-stu-id="12c32-183">If you review the code in `get-started.js`, the bug is probably somewhere in the `updateLabel()` function.</span></span>  <span data-ttu-id="12c32-184">Anstatt jede Codezeile zu durchbrechen, können Sie eine andere Art von Haltepunkt verwenden, um den Code näher am wahrscheinlichen Speicherort des Fehlers anzuhalten.</span><span class="sxs-lookup"><span data-stu-id="12c32-184">Rather than stepping through every line of code, you may use another type of breakpoint to pause the code closer to the probable location of the bug.</span></span>  

## <a name="step-5-set-a-line-of-code-breakpoint"></a><span data-ttu-id="12c32-185">Schritt 5: Festlegen eines Codezeile-Haltepunkts</span><span class="sxs-lookup"><span data-stu-id="12c32-185">Step 5: Set a line-of-code breakpoint</span></span>  

<span data-ttu-id="12c32-186">Codelinien-Haltepunkte sind die am häufigsten verwendeten Haltepunkte.</span><span class="sxs-lookup"><span data-stu-id="12c32-186">Line-of-code breakpoints are the most common type of breakpoint.</span></span>  <span data-ttu-id="12c32-187">Wenn Sie zu der bestimmten Codezeile kommen, die Sie anhalten möchten, verwenden Sie einen Codezeile-Haltepunkt.</span><span class="sxs-lookup"><span data-stu-id="12c32-187">When you get to the specific line of code you want to pause, use a line-of-code breakpoint.</span></span>  

1.  <span data-ttu-id="12c32-188">Sehen Sie sich die letzte Codezeile in `updateLabel()` an:</span><span class="sxs-lookup"><span data-stu-id="12c32-188">Look at the last line of code in `updateLabel()`:</span></span>  
    
    ```javascript
    label.textContent = addend1 + ' + ' + addend2 + ' = ' + sum;
    ```  
    
1.  <span data-ttu-id="12c32-189">Auf der linken Seite wird die Nummer dieser bestimmten Codezeile als **34 angezeigt.**</span><span class="sxs-lookup"><span data-stu-id="12c32-189">On the left, the number of this particular line of code is displayed as **34**.</span></span>  <span data-ttu-id="12c32-190">Wählen Sie Zeile **34 aus.**</span><span class="sxs-lookup"><span data-stu-id="12c32-190">Choose line **34**.</span></span>  <span data-ttu-id="12c32-191">DevTools zeigt links von **34**ein rotes Symbol an.</span><span class="sxs-lookup"><span data-stu-id="12c32-191">DevTools displays a red icon to the left of **34**.</span></span>  <span data-ttu-id="12c32-192">Das rote Symbol gibt an, dass sich ein Codepunkt in dieser Zeile befindet.</span><span class="sxs-lookup"><span data-stu-id="12c32-192">The red icon indicates that a line-of-code breakpoint is on this line.</span></span>  <span data-ttu-id="12c32-193">DevTools hält immer an, bevor diese Codezeile ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="12c32-193">DevTools always pauses before this line of code is run.</span></span>  
1.  <span data-ttu-id="12c32-194">Wählen **Sie Skriptausführung fortsetzen** \( ![ Skriptausführung fortsetzen ](../media/resume-script-run-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="12c32-194">Choose **Resume script execution** \(![Resume script execution](../media/resume-script-run-icon.msft.png)\).</span></span>  <span data-ttu-id="12c32-195">Das Skript wird weiterhin ausgeführt, bis Zeile 33 erreicht ist.</span><span class="sxs-lookup"><span data-stu-id="12c32-195">The script continues to run until it reaches line 33.</span></span>  <span data-ttu-id="12c32-196">In den Zeilen 31, 32 und 33 druckt DevTools die Werte von , und rechts neben dem `addend1` `addend2` `sum` Semikolon in jeder Zeile.</span><span class="sxs-lookup"><span data-stu-id="12c32-196">On lines 31, 32, and 33, DevTools prints the values of `addend1`, `addend2`, and `sum` to the right of the semi-colon on each line.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-breakpoint-paused.msft.png" alt-text="DevTools hält am Zeilen-of-Code-Haltepunkt in Zeile 34 an" lightbox="../media/javascript-sources-breakpoint-paused.msft.png":::
       <span data-ttu-id="12c32-198">DevTools hält am Zeilen-of-Code-Haltepunkt in Zeile 34 an</span><span class="sxs-lookup"><span data-stu-id="12c32-198">DevTools pauses on the line-of-code breakpoint on line 34</span></span>  
    :::image-end:::  
    
## <a name="step-6-check-variable-values"></a><span data-ttu-id="12c32-199">Schritt 6: Überprüfen von Variablenwerten</span><span class="sxs-lookup"><span data-stu-id="12c32-199">Step 6: Check variable values</span></span>  

<span data-ttu-id="12c32-200">Die Werte `addend1` von , und sehen `addend2` `sum` verdächtig aus.</span><span class="sxs-lookup"><span data-stu-id="12c32-200">The values of `addend1`, `addend2`, and `sum` look suspicious.</span></span>  <span data-ttu-id="12c32-201">Die Werte werden in Anführungszeichen eingeschlossen.</span><span class="sxs-lookup"><span data-stu-id="12c32-201">The values are wrapped in quotes.</span></span>  <span data-ttu-id="12c32-202">Die Anführungszeichen bedeuten, dass der Wert eine Zeichenfolge ist. Dies ist eine gute Hypothese, um die Ursache des Fehlers zu erläutern.</span><span class="sxs-lookup"><span data-stu-id="12c32-202">The quotations mean that the value is a string, which is a good hypothesis to explain the cause of the bug.</span></span>  <span data-ttu-id="12c32-203">Sammeln Sie weitere Informationen zur Situation.</span><span class="sxs-lookup"><span data-stu-id="12c32-203">Gather more information about the situation.</span></span>  <span data-ttu-id="12c32-204">DevTools bietet viele Tools zum Untersuchen von Variablenwerten.</span><span class="sxs-lookup"><span data-stu-id="12c32-204">DevTools provides many tools for examining variable values.</span></span>  

### <a name="method-1-the-scope-panel"></a><span data-ttu-id="12c32-205">Methode 1: Bereich</span><span class="sxs-lookup"><span data-stu-id="12c32-205">Method 1: The Scope panel</span></span>  

<span data-ttu-id="12c32-206">Wenn Sie in einer Codezeile \*\*\*\* anhalten, werden im Bereich Bereich die lokalen und globalen Variablen angezeigt, die derzeit definiert sind, zusammen mit dem Wert der einzelnen Variablen.</span><span class="sxs-lookup"><span data-stu-id="12c32-206">If you pause on a line of code, the **Scope** panel displays the local and global variables that are currently defined, along with the value of each variable.</span></span>  <span data-ttu-id="12c32-207">Außerdem werden ggf. Schließvariablen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="12c32-207">It also displays closure variables, as applicable.</span></span>  <span data-ttu-id="12c32-208">Doppelklicken Sie auf einen Variablenwert, um ihn zu bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="12c32-208">Double-click a variable value to edit it.</span></span>  <span data-ttu-id="12c32-209">Wenn Sie in einer Codezeile nicht anhalten, ist der **Bereich** Bereich leer.</span><span class="sxs-lookup"><span data-stu-id="12c32-209">If you don't pause on a line of code, the **Scope** panel is empty.</span></span>  

:::image type="complex" source="../media/javascript-sources-breakpoint-paused-scope.msft.png" alt-text="Der Bereich Bereich" lightbox="../media/javascript-sources-breakpoint-paused-scope.msft.png":::
   <span data-ttu-id="12c32-211">Der **Bereich Bereich**</span><span class="sxs-lookup"><span data-stu-id="12c32-211">The **Scope** pane</span></span>  
:::image-end:::  

### <a name="method-2-watch-expressions"></a><span data-ttu-id="12c32-212">Methode 2: Watch Expressions</span><span class="sxs-lookup"><span data-stu-id="12c32-212">Method 2: Watch Expressions</span></span>  

<span data-ttu-id="12c32-213">Im **Bereich Überwachungsausdrücke** können Sie die Werte von Variablen im Laufe der Zeit überwachen.</span><span class="sxs-lookup"><span data-stu-id="12c32-213">The **Watch Expressions** panel lets you monitor the values of variables over time.</span></span>  <span data-ttu-id="12c32-214">Wie der Name schon sagt, **sind Watch Expressions** nicht auf Variablen beschränkt.</span><span class="sxs-lookup"><span data-stu-id="12c32-214">As the name implies, **Watch Expressions** aren't limited to variables.</span></span>  <span data-ttu-id="12c32-215">Sie können einen beliebigen gültigen JavaScript-Ausdruck in einem **Watch Expression speichern.**</span><span class="sxs-lookup"><span data-stu-id="12c32-215">You may store any valid JavaScript expression in a **Watch Expression**.</span></span>  <span data-ttu-id="12c32-216">Versuchen Sie es jetzt.</span><span class="sxs-lookup"><span data-stu-id="12c32-216">Try it now.</span></span>  

1.  <span data-ttu-id="12c32-217">Wählen Sie den **Bereich "Beobachten"** aus.</span><span class="sxs-lookup"><span data-stu-id="12c32-217">Choose the **Watch** panel.</span></span>  
1.  <span data-ttu-id="12c32-218">Wählen **Sie Ausdruck hinzufügen** \( Ausdruck hinzufügen ![ ](../media/add-expression-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="12c32-218">Choose **Add Expression** \(![Add Expression](../media/add-expression-icon.msft.png)\).</span></span>  
1.  <span data-ttu-id="12c32-219">Geben Sie `typeof sum` ein.</span><span class="sxs-lookup"><span data-stu-id="12c32-219">Type `typeof sum`.</span></span>  
1.  <span data-ttu-id="12c32-220">Wählen Sie `Enter` aus.</span><span class="sxs-lookup"><span data-stu-id="12c32-220">Select `Enter`.</span></span>  <span data-ttu-id="12c32-221">DevTools zeigt `typeof sum: "string"` .</span><span class="sxs-lookup"><span data-stu-id="12c32-221">DevTools shows `typeof sum: "string"`.</span></span>  <span data-ttu-id="12c32-222">Der Wert rechts neben dem Doppelpunkt ist das Ergebnis Ihres Watch Expression.</span><span class="sxs-lookup"><span data-stu-id="12c32-222">The value to the right of the colon is the result of your Watch Expression.</span></span>  
    
> [!NOTE]
> <span data-ttu-id="12c32-223">Im Bereich **"Uhrausdruck"** \(unten rechts\) in der folgenden Abbildung wird der `typeof sum` Watch Expression angezeigt.</span><span class="sxs-lookup"><span data-stu-id="12c32-223">In the **Watch Expression** pane \(bottom-right\) in the following figure, the `typeof sum` Watch Expression is displayed.</span></span>  <span data-ttu-id="12c32-224">Wenn Ihr DevTools-Fenster groß ist, befindet sich der Bereich **"Watch Expression"** rechts über dem **Bereich Ereignislistener-Haltepunkte.**</span><span class="sxs-lookup"><span data-stu-id="12c32-224">If your DevTools window is large, the **Watch Expression** pane is on the right above the **Event Listener Breakpoints** pane.</span></span>  

:::image type="complex" source="../media/javascript-sources-breakpoint-paused-watch.msft.png" alt-text="Der Bereich "Watch Expression"" lightbox="../media/javascript-sources-breakpoint-paused-watch.msft.png":::
   <span data-ttu-id="12c32-226">Der **Bereich "Watch Expression"**</span><span class="sxs-lookup"><span data-stu-id="12c32-226">The **Watch Expression** panel</span></span>  
:::image-end:::  

<span data-ttu-id="12c32-227">Wie verdächtig, `sum` wird als Zeichenfolge ausgewertet, wenn es sich um eine Zahl handelt.</span><span class="sxs-lookup"><span data-stu-id="12c32-227">As suspected, `sum` is being evaluated as a string, when it should be a number.</span></span>  <span data-ttu-id="12c32-228">Sie haben nun bestätigt, dass der Werttyp die Ursache des Fehlers ist.</span><span class="sxs-lookup"><span data-stu-id="12c32-228">You now confirmed value type is the cause of the bug.</span></span>  

### <a name="method-3-the-console"></a><span data-ttu-id="12c32-229">Methode 3: Die Konsole</span><span class="sxs-lookup"><span data-stu-id="12c32-229">Method 3: The Console</span></span>  

<span data-ttu-id="12c32-230">Mit **der Konsole** können Sie Nachrichten anzeigen und sie auch verwenden, um beliebige `console.log()` JavaScript-Anweisungen auszuwerten.</span><span class="sxs-lookup"><span data-stu-id="12c32-230">The **Console** allows you to view `console.log()` messages and you may also use it to evaluate arbitrary JavaScript statements.</span></span>  <span data-ttu-id="12c32-231">Zum Debuggen können Sie die **Konsole** verwenden, um potenzielle Fehlerbehebungen auf Fehler zu testen.</span><span class="sxs-lookup"><span data-stu-id="12c32-231">For debugging, you may use the **Console** to test potential fixes for bugs.</span></span>  <span data-ttu-id="12c32-232">Versuchen Sie es jetzt.</span><span class="sxs-lookup"><span data-stu-id="12c32-232">Try it now.</span></span>  

1.  <span data-ttu-id="12c32-233">Wenn das **Konsolentool** geschlossen ist, wählen Sie `Escape` es aus, um es zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="12c32-233">If the **Console** tool is closed, select `Escape` to open it.</span></span>  <span data-ttu-id="12c32-234">Das **Konsolentool** wird im unteren Bereich des DevTools-Fensters geöffnet.</span><span class="sxs-lookup"><span data-stu-id="12c32-234">The **Console** tool opens in the lower panel of the DevTools window.</span></span>  
1.  <span data-ttu-id="12c32-235">Geben Sie **in der Konsole** `parseInt(addend1) + parseInt(addend2)` ein.</span><span class="sxs-lookup"><span data-stu-id="12c32-235">In the **Console**, type `parseInt(addend1) + parseInt(addend2)`.</span></span>  <span data-ttu-id="12c32-236">Die Anweisung, mit der das Tool in einer Codezeile angehalten wird, in `addend1` der sich der Bereich `addend2` befindet.</span><span class="sxs-lookup"><span data-stu-id="12c32-236">The statement the tool is paused on a line of code where `addend1` and `addend2` are in scope.</span></span>  
1.  <span data-ttu-id="12c32-237">Wählen Sie `Enter` aus.</span><span class="sxs-lookup"><span data-stu-id="12c32-237">Select `Enter`.</span></span>  <span data-ttu-id="12c32-238">DevTools wertet die Anweisung aus und druckt , was das Ergebnis ist, das Sie von `6` der Demo erwarten.</span><span class="sxs-lookup"><span data-stu-id="12c32-238">DevTools evaluates the statement and prints `6`, which is the result you expect the demo to produce.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-breakpoint-paused-console.msft.png" alt-text="Das Konsolentool nach der Auswertung von parseInt(addend1) + parseInt(addend2)" lightbox="../media/javascript-sources-breakpoint-paused-console.msft.png":::
       <span data-ttu-id="12c32-240">Das **Konsolentool** nach der Auswertung</span><span class="sxs-lookup"><span data-stu-id="12c32-240">The **Console** tool, after evaluating</span></span> `parseInt(addend1) + parseInt(addend2)`  
    :::image-end:::  
    
## <a name="step-7-apply-a-fix"></a><span data-ttu-id="12c32-241">Schritt 7: Anwenden einer Korrektur</span><span class="sxs-lookup"><span data-stu-id="12c32-241">Step 7: Apply a fix</span></span>  

<span data-ttu-id="12c32-242">Wenn Sie eine Fehlerbehebung für den Fehler finden, versuchen Sie es, indem Sie den Code bearbeiten und die Demo erneut ausführen.</span><span class="sxs-lookup"><span data-stu-id="12c32-242">If you find a fix for the bug, try out your fix by editing the code and rerunning the demo.</span></span>  <span data-ttu-id="12c32-243">Sie können JavaScript-Code direkt in der DevTools-Benutzeroberfläche bearbeiten und die Korrektur anwenden.</span><span class="sxs-lookup"><span data-stu-id="12c32-243">You may edit JavaScript code directly within the DevTools UI and apply the fix.</span></span>  <span data-ttu-id="12c32-244">Versuchen Sie es jetzt.</span><span class="sxs-lookup"><span data-stu-id="12c32-244">Try it now.</span></span>  

1.  <span data-ttu-id="12c32-245">Wählen **Sie Skriptausführung fortsetzen** \( ![ Skriptausführung fortsetzen ](../media/resume-script-run-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="12c32-245">Choose **Resume script execution** \(![Resume script execution](../media/resume-script-run-icon.msft.png)\).</span></span>  
1.  <span data-ttu-id="12c32-246">Ersetzen Sie **im Code-Editor**Zeile 32 durch `var sum = addend1 + addend2` `var sum = parseInt(addend1) + parseInt(addend2)` .</span><span class="sxs-lookup"><span data-stu-id="12c32-246">In the **Code Editor**, replace line 32, `var sum = addend1 + addend2`, with `var sum = parseInt(addend1) + parseInt(addend2)`.</span></span>  
1.  <span data-ttu-id="12c32-247">Wählen `Control` + `S` Sie \(Windows, Linux\) oder `Command` + `S` \(macOS\) aus, um Ihre Änderung zu speichern.</span><span class="sxs-lookup"><span data-stu-id="12c32-247">Select `Control`+`S` \(Windows, Linux\) or `Command`+`S` \(macOS\) to save your change.</span></span>  
1.  <span data-ttu-id="12c32-248">Wählen **Sie Haltepunkte deaktivieren** \( ![ Haltepunkte deaktivieren ](../media/deactivate-breakpoints-button-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="12c32-248">Choose **Deactivate breakpoints** \(![Deactivate breakpoints](../media/deactivate-breakpoints-button-icon.msft.png)\).</span></span>  <span data-ttu-id="12c32-249">Es ändert sich blau, um anzugeben, dass die Option aktiv ist.</span><span class="sxs-lookup"><span data-stu-id="12c32-249">It changes blue to indicate the option is active.</span></span>  <span data-ttu-id="12c32-250">Während **Die Haltepunkte deaktivieren** festgelegt ist, ignoriert DevTools alle von Ihnen festgelegten Haltepunkte.</span><span class="sxs-lookup"><span data-stu-id="12c32-250">While **Deactivate breakpoints** is set, DevTools ignores any breakpoints you set.</span></span>  
1.  <span data-ttu-id="12c32-251">Testen Sie die Demo mit unterschiedlichen Werten.</span><span class="sxs-lookup"><span data-stu-id="12c32-251">Try out the demo with different values.</span></span>  <span data-ttu-id="12c32-252">Die Demo wird nun korrekt berechnet.</span><span class="sxs-lookup"><span data-stu-id="12c32-252">The demo now calculates correctly.</span></span>  
    
> [!CAUTION]
> <span data-ttu-id="12c32-253">Dieser Workflow wendet nur eine Korrektur auf den Code an, der in Ihrem Browser ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="12c32-253">This workflow only applies a fix to the code that is running in your browser.</span></span>  <span data-ttu-id="12c32-254">Der Code für alle Benutzer, die Ihre Webseite besuchen, wird nicht behoben.</span><span class="sxs-lookup"><span data-stu-id="12c32-254">It does not fix the code for all users that visit your webpage.</span></span>  <span data-ttu-id="12c32-255">Dazu müssen Sie den Code auf Ihren Servern beheben.</span><span class="sxs-lookup"><span data-stu-id="12c32-255">To do that, you need to fix the code that is on your servers.</span></span>  

## <a name="next-steps"></a><span data-ttu-id="12c32-256">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="12c32-256">Next steps</span></span>  

<span data-ttu-id="12c32-257">Herzlichen Glückwunsch!</span><span class="sxs-lookup"><span data-stu-id="12c32-257">Congratulations!</span></span>  <span data-ttu-id="12c32-258">Sie wissen nun, wie Sie Microsoft Edge DevTools beim Debuggen von JavaScript nutzen können.</span><span class="sxs-lookup"><span data-stu-id="12c32-258">You now know how to make the most of Microsoft Edge DevTools when debugging JavaScript.</span></span>  <span data-ttu-id="12c32-259">Die Tools und Methoden, die Sie in diesem Artikel gelernt haben, können Ihnen unzählige Stunden sparen.</span><span class="sxs-lookup"><span data-stu-id="12c32-259">The tools and methods you learned in this article may save you countless hours.</span></span>  

<span data-ttu-id="12c32-260">In diesem Artikel wurden Ihnen nur zwei Methoden zum Festlegen von Haltepunkten erläutert.</span><span class="sxs-lookup"><span data-stu-id="12c32-260">This article only taught you two ways to set breakpoints.</span></span>  <span data-ttu-id="12c32-261">DevTools bietet viele andere Möglichkeiten, einschließlich der folgenden Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="12c32-261">DevTools offers many other ways including the following settings.</span></span>  

*   <span data-ttu-id="12c32-262">Bedingte Haltepunkte, die nur ausgelöst werden, wenn die bedingung, die Sie bereitstellen, true ist.</span><span class="sxs-lookup"><span data-stu-id="12c32-262">Conditional breakpoints that are only triggered when the condition that you provide is true.</span></span>  
*   <span data-ttu-id="12c32-263">Haltepunkte für abgefangene oder nicht abgefangene Ausnahmen.</span><span class="sxs-lookup"><span data-stu-id="12c32-263">Breakpoints on caught or uncaught exceptions.</span></span>  
*   <span data-ttu-id="12c32-264">XHR-Haltepunkte, die ausgelöst werden, wenn die angeforderte URL einer von Ihnen angegebenen Teilzeichenfolge entspricht.</span><span class="sxs-lookup"><span data-stu-id="12c32-264">XHR breakpoints that are triggered when the requested URL matches a substring that you provide.</span></span>  
    
<span data-ttu-id="12c32-265">Weitere Informationen zur Verwendung der einzelnen Typen finden Sie unter [Pause Your Code With Breakpoints][DevtoolsJavscriptBreakpoints].</span><span class="sxs-lookup"><span data-stu-id="12c32-265">For more information about when and how to use each type, navigate to [Pause Your Code With Breakpoints][DevtoolsJavscriptBreakpoints].</span></span>  

<span data-ttu-id="12c32-266">Einige Codeschrittsteuerelemente werden in diesem Artikel nicht erläutert.</span><span class="sxs-lookup"><span data-stu-id="12c32-266">A couple of code stepping controls aren't explained in this article.</span></span>  <span data-ttu-id="12c32-267">Weitere Informationen finden Sie unter [Step over line of code][DevtoolsJavascriptReferenceStepThroughCode].</span><span class="sxs-lookup"><span data-stu-id="12c32-267">For more information, navigate to [Step over line of code][DevtoolsJavascriptReferenceStepThroughCode].</span></span>  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="12c32-268">Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen</span><span class="sxs-lookup"><span data-stu-id="12c32-268">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsJavscriptBreakpoints]: ./breakpoints.md "So halten Sie Ihren Code mit Haltepunkten in Microsoft Edge DevTools | Microsoft Docs"
[DevtoolsJavascriptReferenceStepThroughCode]: ./reference.md#step-through-code "Schritt durch Code – JavaScript-Debugreferenz | Microsoft Docs"

<!--[inPrivate]: https://support.alphabet.com/alphabet-browser/answer/95464  -->  

[OpenDebugJSDemo]: https://microsoft-edge-chromium-devtools.glitch.me/debug-js/get-started.html "Öffnen sie demo | Glitch"  

> [!NOTE]
> <span data-ttu-id="12c32-272">Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="12c32-272">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="12c32-273">Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/javascript/index) und wird von [Kayce Basken][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\) verfasst.</span><span class="sxs-lookup"><span data-stu-id="12c32-273">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/javascript/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="12c32-275">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="12c32-275">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
