---
description: Erfahren Sie, wie Sie Microsoft Edge DevTools verwenden, um JavaScript-Fehler zu finden und zu beheben.
title: Erste Schritte mit dem Debuggen von JavaScript in Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/09/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, Entwicklungstools
ms.openlocfilehash: b036fc87149d13446ab1bc05afc8fc8631d27c8d
ms.sourcegitcommit: e737277744dd25a7585c113eef22a2aa4d4c167f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "11325948"
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
# <span data-ttu-id="61639-104">Erste Schritte mit dem Debuggen von JavaScript in Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="61639-104">Get started with debugging JavaScript in Microsoft Edge DevTools</span></span>  

<span data-ttu-id="61639-105">In diesem Artikel lernen Sie den grundlegenden Workflow zum Debuggen von JavaScript-Problem in DevTools.</span><span class="sxs-lookup"><span data-stu-id="61639-105">This article teaches you the basic workflow for debugging any JavaScript issue in DevTools.</span></span>  

## <span data-ttu-id="61639-106">Schritt 1: Reproduzieren des Fehlers</span><span class="sxs-lookup"><span data-stu-id="61639-106">Step 1: Reproduce the bug</span></span>  

<span data-ttu-id="61639-107">Das Suchen einer Reihe von Aktionen, die einen Fehler konsistent reproduzieren, ist immer der erste Schritt beim Debuggen.</span><span class="sxs-lookup"><span data-stu-id="61639-107">Finding a series of actions that consistently reproduce a bug is always the first step to debugging.</span></span>  

1.  <span data-ttu-id="61639-108">Wählen Sie **"Demo öffnen"** aus.</span><span class="sxs-lookup"><span data-stu-id="61639-108">Choose **Open Demo**.</span></span>  <span data-ttu-id="61639-109">Halten `Control` Sie \(Windows, Linux\) oder \(macOS\) fest, und öffnen Sie die Demo `Command` auf einer neuen Browserregisterkarte.</span><span class="sxs-lookup"><span data-stu-id="61639-109">Hold `Control` \(Windows, Linux\) or `Command` \(macOS\) and open the demo in a new browser tab.</span></span>  
    
    [<span data-ttu-id="61639-110">Demo öffnen</span><span class="sxs-lookup"><span data-stu-id="61639-110">Open Demo</span></span>][OpenDebugJSDemo]  
    
1.  <span data-ttu-id="61639-111">Geben `5` Sie in das Textfeld Zahl **1** ein.</span><span class="sxs-lookup"><span data-stu-id="61639-111">Enter `5` in the **Number 1** text box.</span></span>  
1.  <span data-ttu-id="61639-112">Geben `1` Sie in das Textfeld Zahl **2** ein.</span><span class="sxs-lookup"><span data-stu-id="61639-112">Enter `1` in the **Number 2** text box.</span></span>  
1.  <span data-ttu-id="61639-113">Wählen **Sie "Nummer 1 hinzufügen" und "Zahl 2" aus.**</span><span class="sxs-lookup"><span data-stu-id="61639-113">Choose **Add Number 1 and Number 2**.</span></span>  <span data-ttu-id="61639-114">Die Bezeichnung unterhalb der Schaltfläche steht `5 + 1 = 51` für .</span><span class="sxs-lookup"><span data-stu-id="61639-114">The label below the button says `5 + 1 = 51`.</span></span>  <span data-ttu-id="61639-115">Das Ergebnis sollte `6` .</span><span class="sxs-lookup"><span data-stu-id="61639-115">The result should be `6`.</span></span>  <span data-ttu-id="61639-116">Beheben Sie als Nächstes den Fehler beim Hinzuf?en, der der Fehler ist.</span><span class="sxs-lookup"><span data-stu-id="61639-116">Next, fix the addition error that is the bug.</span></span>  
    
    :::image type="complex" source="../media/javascript-js-demo-bad.msft.png" alt-text="5 + 1 ergibt 51, sollte aber 6 sein" lightbox="../media/javascript-js-demo-bad.msft.png":::
       `5 + 1` <span data-ttu-id="61639-118">führt zu `51` , sollte aber</span><span class="sxs-lookup"><span data-stu-id="61639-118">results in `51`, but should be</span></span> `6`  
    :::image-end:::  
    
## <span data-ttu-id="61639-119">Schritt 2: Machen Sie sich mit der Benutzeroberfläche des Quellenbereichs vertraut</span><span class="sxs-lookup"><span data-stu-id="61639-119">Step 2: Get familiar with the Sources panel UI</span></span>  

<span data-ttu-id="61639-120">DevTools bietet viele verschiedene Tools für verschiedene Aufgaben.</span><span class="sxs-lookup"><span data-stu-id="61639-120">DevTools provides many different tools for different tasks.</span></span>  <span data-ttu-id="61639-121">Zu den verschiedenen Aufgaben gehören das Ändern von CSS, das Laden von Profilingseiten und das Überwachen von Netzwerkanforderungen.</span><span class="sxs-lookup"><span data-stu-id="61639-121">Different tasks include changing CSS, profiling page-load performance, and monitoring network requests.</span></span>  <span data-ttu-id="61639-122">Im **Bereich** "Quellen" debuggen Sie JavaScript.</span><span class="sxs-lookup"><span data-stu-id="61639-122">The **Sources** panel is where you debug JavaScript.</span></span>  

1.  <span data-ttu-id="61639-123">Öffnen Sie DevTools, indem `Control` + `Shift` + `J` Sie \(Windows, Linux\) oder `Command` + `Option` + `J` \(macOS\) drücken.</span><span class="sxs-lookup"><span data-stu-id="61639-123">Open DevTools by pressing `Control`+`Shift`+`J` \(Windows, Linux\) or `Command`+`Option`+`J` \(macOS\).</span></span>  <span data-ttu-id="61639-124">Mit dieser Verknüpfung wird der **Konsolenbereich** geöffnet.</span><span class="sxs-lookup"><span data-stu-id="61639-124">This shortcut opens the **Console** panel.</span></span>  
    
    :::image type="complex" source="../media/javascript-console-empty.msft.png" alt-text="Konsolenbereich" lightbox="../media/javascript-console-empty.msft.png":::
       <span data-ttu-id="61639-126">Das **Konsolentool**</span><span class="sxs-lookup"><span data-stu-id="61639-126">The **Console** tool</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="61639-127">Wählen Sie das **Quellentool** aus.</span><span class="sxs-lookup"><span data-stu-id="61639-127">Choose the **Sources** tool.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-sections.msft.png" alt-text="Bereich "Quellen"" lightbox="../media/javascript-sources-sections.msft.png":::
       <span data-ttu-id="61639-129">Bereich **"Quellen"**</span><span class="sxs-lookup"><span data-stu-id="61639-129">The **Sources** panel</span></span>  
    :::image-end:::  
    
<span data-ttu-id="61639-130">Die **Benutzeroberfläche** des Quellenbereichs hat drei Teile.</span><span class="sxs-lookup"><span data-stu-id="61639-130">The **Sources** panel UI has three parts.</span></span>  

:::image type="complex" source="../media/javascript-sources-sections-annotated.msft.png" alt-text="Die drei Teile der Benutzeroberfläche des Quellenbereichs" lightbox="../media/javascript-sources-sections-annotated.msft.png":::
   <span data-ttu-id="61639-132">Die drei Teile der **Benutzeroberfläche** des Quellenbereichs</span><span class="sxs-lookup"><span data-stu-id="61639-132">The 3 parts of the **Sources** panel UI</span></span>  
:::image-end:::  

1.  <span data-ttu-id="61639-133">Der **Dateinavigatorbereich** \(Abschnitt 1 in der vorherigen Abbildung\).</span><span class="sxs-lookup"><span data-stu-id="61639-133">The **File Navigator** pane \(Section 1 in the previous figure\).</span></span>  <span data-ttu-id="61639-134">Jede Datei, die die Webseite anfordert, wird hier aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="61639-134">Every file that the webpage requests is listed here.</span></span>  
1.  <span data-ttu-id="61639-135">Der **Code-Editor-Bereich** \(Abschnitt 2 in der vorherigen Abbildung\).</span><span class="sxs-lookup"><span data-stu-id="61639-135">The **Code Editor** pane \(Section 2 in the previous figure\).</span></span>  <span data-ttu-id="61639-136">Nachdem Sie eine Datei im **Bereich "Dateinavigator"** ausgewählt haben, wird der Inhalt dieser Datei hier angezeigt.</span><span class="sxs-lookup"><span data-stu-id="61639-136">After selecting a file in the **File Navigator** pane, the contents of that file are displayed here.</span></span>  
1.  <span data-ttu-id="61639-137">Der **JavaScript-Debugbereich** \(Abschnitt 3 in der vorherigen Abbildung\).</span><span class="sxs-lookup"><span data-stu-id="61639-137">The **JavaScript Debugging** pane \(Section 3 in the previous figure\).</span></span>  <span data-ttu-id="61639-138">Verschiedene Tools zum Überprüfen des JavaScript für die Webseite.</span><span class="sxs-lookup"><span data-stu-id="61639-138">Various tools for inspecting the JavaScript for the webpage.</span></span>  <span data-ttu-id="61639-139">Wenn ihr DevTools-Fenster breit ist, wird dieser Bereich rechts vom **Code-Editor-Bereich** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="61639-139">If your DevTools window is wide, this pane is displayed to the right of the **Code Editor** pane.</span></span>  
    
## <span data-ttu-id="61639-140">Schritt 3: Anhalten des Codes mit einem Haltepunkt</span><span class="sxs-lookup"><span data-stu-id="61639-140">Step 3: Pause the code with a breakpoint</span></span>  

<span data-ttu-id="61639-141">Eine gängige Methode zum Debuggen dieser Art von Problem ist das Einfügen mehrerer Anweisungen in den Code und das anschließende Überprüfen von Werten während der Ausführung `console.log()` des Skripts.</span><span class="sxs-lookup"><span data-stu-id="61639-141">A common method for debugging this type of problem is to insert several `console.log()` statements into the code and then to inspect values as the script runs.</span></span>  <span data-ttu-id="61639-142">Zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="61639-142">For example:</span></span>  

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

<span data-ttu-id="61639-143">Die `console.log()` Methode kann die Aufgabe erledigen, **haltepunkte können** sie jedoch schneller erledigen.</span><span class="sxs-lookup"><span data-stu-id="61639-143">The `console.log()` method may get the job done, but **breakpoints** get it done faster.</span></span>  <span data-ttu-id="61639-144">Mit einem Haltepunkt können Sie Ihren Code in der Mitte der Laufzeit anhalten und alle Werte zu diesem Zeitpunkt untersuchen.</span><span class="sxs-lookup"><span data-stu-id="61639-144">A breakpoint lets you pause your code in the middle of the runtime, and examine all values at that moment in time.</span></span>  <span data-ttu-id="61639-145">Haltepunkte haben gegenüber der Methode einige `console.log()` Vorteile:</span><span class="sxs-lookup"><span data-stu-id="61639-145">Breakpoints have a few advantages over the `console.log()` method:</span></span>  

*   <span data-ttu-id="61639-146">With `console.log()` , you need to manually open the source code, find the relevant code, insert the `console.log()` statements, and then refresh the webpage to display the messages in the **Console**.</span><span class="sxs-lookup"><span data-stu-id="61639-146">With `console.log()`, you need to manually open the source code, find the relevant code, insert the `console.log()` statements, and then refresh the webpage to display the messages in the **Console**.</span></span>  <span data-ttu-id="61639-147">Bei Haltepunkten können Sie den relevanten Code unterbrechen, ohne zu wissen, wie der Code strukturiert ist.</span><span class="sxs-lookup"><span data-stu-id="61639-147">With breakpoints, you may pause on the relevant code without even knowing how the code is structured.</span></span>  
*   <span data-ttu-id="61639-148">In Ihren Anweisungen müssen Sie explizit jeden `console.log()` Wert angeben, den Sie überprüfen möchten.</span><span class="sxs-lookup"><span data-stu-id="61639-148">In your `console.log()` statements, you need to explicitly specify each value that you want to inspect.</span></span>  <span data-ttu-id="61639-149">Mit Haltepunkten zeigt DevTools die Werte aller Variablen zu diesem Zeitpunkt an.</span><span class="sxs-lookup"><span data-stu-id="61639-149">With breakpoints, DevTools shows you the values of all variables at that moment in time.</span></span>  <span data-ttu-id="61639-150">Manchmal werden Variablen, die sich auf Ihren Code auswirken, ausgeblendet und verschleiert.</span><span class="sxs-lookup"><span data-stu-id="61639-150">Sometimes variables that affect your code are hidden and obfuscated.</span></span>  
    
<span data-ttu-id="61639-151">Kurz gesagt, können Haltepunkte Ihnen helfen, Fehler schneller zu finden und zu beheben als die `console.log()` Methode.</span><span class="sxs-lookup"><span data-stu-id="61639-151">In short, breakpoints may help you find and fix bugs faster than the `console.log()` method.</span></span>  

<span data-ttu-id="61639-152">Wenn Sie einen Schritt zurück gehen und sich Gedanken über die Funktionsweise der App machen, können Sie eine gebildete Ermutung treffen, dass die falsche Summe \( \) im Ereignislistener berechnet wird, der der Schaltfläche "Nummer 1 hinzufügen" und "Nummer `5 + 1 = 51` `click` **2"** zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="61639-152">If you step back and think about how the app works, you may make an educated guess that the incorrect sum \(`5 + 1 = 51`\) is computed in the `click` event listener associated with the **Add Number 1 and Number 2** button.</span></span>  <span data-ttu-id="61639-153">Daher möchten Sie den Code wahrscheinlich zu dem Zeitpunkt anhalten, zu dem der `click` Listener ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="61639-153">So, you probably want to pause the code around the time that the `click` listener runs.</span></span>  <span data-ttu-id="61639-154">**Mit Ereignislistener-Haltepunkten** können Sie genau dies tun:</span><span class="sxs-lookup"><span data-stu-id="61639-154">**Event Listener Breakpoints** let you do exactly that:</span></span>  

1.  <span data-ttu-id="61639-155">Wählen Sie **im Bereich "JavaScript-Debuggen"** die **Option "Ereignislistener-Haltepunkte"** aus, um den Abschnitt zu erweitern.</span><span class="sxs-lookup"><span data-stu-id="61639-155">In the **JavaScript Debugging** pane, choose **Event Listener Breakpoints** to expand the section.</span></span>  <span data-ttu-id="61639-156">DevTools zeigt eine Liste erweiterbarer Ereigniskategorien an, z. B. **Animation** und **Zwischenablage.**</span><span class="sxs-lookup"><span data-stu-id="61639-156">DevTools reveals a list of expandable event categories, such as **Animation** and **Clipboard**.</span></span>  
1.  <span data-ttu-id="61639-157">Wählen Sie neben der **Kategorie "Mausereignis"** **"Erweitern** \( ![ Symbol "Erweitern" ][ImageExpandIcon] \) aus.</span><span class="sxs-lookup"><span data-stu-id="61639-157">Next to the **Mouse** event category, choose **Expand** \(![Expand icon][ImageExpandIcon]\).</span></span>  <span data-ttu-id="61639-158">DevTools zeigt eine Liste von Mausereignissen an, z. B. **Klicken** **und Mousedown.**</span><span class="sxs-lookup"><span data-stu-id="61639-158">DevTools reveals a list of mouse events, such as **click** and **mousedown**.</span></span>  <span data-ttu-id="61639-159">Jedes Ereignis verfügt über ein Kontrollkästchen daneben.</span><span class="sxs-lookup"><span data-stu-id="61639-159">Each event has a checkbox next to it.</span></span>  
1.  <span data-ttu-id="61639-160">Aktivieren Sie das Kontrollkästchen neben dem **Klicken.**</span><span class="sxs-lookup"><span data-stu-id="61639-160">Choose the checkbox next to **click**.</span></span>  <span data-ttu-id="61639-161">DevTools ist jetzt so eingerichtet, dass es automatisch angehalten wird, wenn ein `click` Ereignislistener ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="61639-161">DevTools is now set up to automatically pause when any `click` event listener runs.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-event-listener-breakpoint-mouse-click.msft.png" alt-text="Aktivieren Sie das Kontrollkästchen neben dem Klicken." lightbox="../media/javascript-sources-event-listener-breakpoint-mouse-click.msft.png":::
       <span data-ttu-id="61639-163">Aktivieren Sie das Kontrollkästchen neben dem **Klicken.**</span><span class="sxs-lookup"><span data-stu-id="61639-163">Choose the checkbox next to **click**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="61639-164">Wählen Sie wieder auf der Demo **"Nummer 1" und "Nummer 2"** aus.</span><span class="sxs-lookup"><span data-stu-id="61639-164">Back on the demo, choose **Add Number 1 and Number 2** again.</span></span>  <span data-ttu-id="61639-165">DevTools hält die Demo an und hebt eine Codezeile im **Quellenbereich** hervor.</span><span class="sxs-lookup"><span data-stu-id="61639-165">DevTools pauses the demo and highlights a line of code in the **Sources** panel.</span></span>  <span data-ttu-id="61639-166">DevTools sollten in Zeile 16 in angehalten `get-started.js` werden.</span><span class="sxs-lookup"><span data-stu-id="61639-166">DevTools should pause on line 16 in `get-started.js`.</span></span>  
    
    ```javascript
    if (inputsAreEmpty()) {
    ```  
    
    <span data-ttu-id="61639-167">Wenn Sie in einer anderen Codezeile anhalten, drücken Sie **"Skriptausführung** fortsetzen\( Skriptausführung fortsetzen \) bis Sie in der richtigen ![ ][ImageResumeIcon] Zeile anhalten.</span><span class="sxs-lookup"><span data-stu-id="61639-167">If you pause on a different line of code, press **Resume Script Execution** \(![Resume Script Execution][ImageResumeIcon]\) until you pause on the correct line.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="61639-168">Wenn Sie in einer anderen Zeile angehalten haben, verfügen Sie über eine Browsererweiterung, die einen Ereignislistener auf jeder besuchten `click` Webseite registriert.</span><span class="sxs-lookup"><span data-stu-id="61639-168">If you paused on a different line, you have a browser extension that registers a `click` event listener on every webpage that you visit.</span></span>  <span data-ttu-id="61639-169">Sie wurden im Listener der Erweiterung `click` angehalten.</span><span class="sxs-lookup"><span data-stu-id="61639-169">You were paused in the `click` listener of the extension.</span></span>  <span data-ttu-id="61639-170">Wenn Sie den InPrivate-Modus verwenden, um **im privaten**Modus zu navigieren, wodurch alle Erweiterungen deaktiviert werden, sehen Sie möglicherweise, dass Sie jedes Mal in der gewünschten Codezeile anhalten.</span><span class="sxs-lookup"><span data-stu-id="61639-170">If you use InPrivate Mode to **browse in private**, which disables all extensions, you may see that you pause on the desired line of code every time.</span></span>  

<!--todo: add inprivate section when available -->  

<span data-ttu-id="61639-171">**Ereignislistener-Haltepunkte** sind nur einer von vielen Arten von Haltepunkten, die in DevTools verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="61639-171">**Event Listener Breakpoints** are just one of many types of breakpoints available in DevTools.</span></span>  <span data-ttu-id="61639-172">Merken Sie sich alle verschiedenen Typen, damit Sie unterschiedliche Szenarien so schnell wie möglich debuggen können.</span><span class="sxs-lookup"><span data-stu-id="61639-172">Memorize all the different types to help you debug different scenarios as quickly as possible.</span></span>  <!--See [Pause Your Code With Breakpoints][JSBreakpoints] to learn when and how to use each type.  -->  

## <span data-ttu-id="61639-173">Schritt 4: Schrittweises Durchschritten des Codes</span><span class="sxs-lookup"><span data-stu-id="61639-173">Step 4: Step through the code</span></span>  

<span data-ttu-id="61639-174">Eine häufige Ursache für Fehler ist, wenn ein Skript in der falschen Reihenfolge ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="61639-174">One common cause of bugs is when a script runs in the wrong order.</span></span>  <span data-ttu-id="61639-175">Schrittweises Durchschritten des Codes ermöglicht Es Ihnen, die Laufzeit ihres Codes zu durchschritten.</span><span class="sxs-lookup"><span data-stu-id="61639-175">Stepping through your code allows you to walk through the runtime of your code.</span></span>  <span data-ttu-id="61639-176">Sie werden durch eine Zeile nach der anderen gehen, um herauszufinden, wo Ihr Code in einer anderen Reihenfolge als erwartet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="61639-176">You walk through one line at a time to help you figure out exactly where your code is running in a different order than you expect.</span></span>  <span data-ttu-id="61639-177">Probieren Sie es jetzt aus:</span><span class="sxs-lookup"><span data-stu-id="61639-177">Try it now:</span></span>  

1.  <span data-ttu-id="61639-178">Choose **Step over next function call** \( Step over next function call ![ ][ImageOverIcon] \).</span><span class="sxs-lookup"><span data-stu-id="61639-178">Choose **Step over next function call** \(![Step over next function call][ImageOverIcon]\).</span></span>  <span data-ttu-id="61639-179">DevTools führt den folgenden Code aus, ohne ihn schrittweise zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="61639-179">DevTools runs the following code without stepping into it.</span></span>  
    
    ```javascript
    if (inputsAreEmpty()) {
    ```  
    
    > [!NOTE]
    > <span data-ttu-id="61639-180">DevTools überspringt einige Codezeilen.</span><span class="sxs-lookup"><span data-stu-id="61639-180">DevTools skips a few lines of code.</span></span>  <span data-ttu-id="61639-181">Dies liegt daran, dass der Codeblock für die Anweisung nicht als `inputsAreEmpty()` falsch `if` ausgewertet wird.</span><span class="sxs-lookup"><span data-stu-id="61639-181">This is because `inputsAreEmpty()` evaluates as false, so the block of code for the `if` statement does not run.</span></span>  
    
1.  <span data-ttu-id="61639-182">On the **Sources** panel of DevTools, choose **Step into next function call** \( Step into next function call ![ ][ImageIntoIcon] \) to step through the runtime of the `updateLabel()` function, one line at a time.</span><span class="sxs-lookup"><span data-stu-id="61639-182">On the **Sources** panel of DevTools, choose **Step into next function call** \(![Step into next function call][ImageIntoIcon]\) to step through the runtime of the `updateLabel()` function, one line at a time.</span></span>  
    
<span data-ttu-id="61639-183">Das Überprüfen einer Zeile nach der anderen ist die grundidee Idee, codeschritten zu werden.</span><span class="sxs-lookup"><span data-stu-id="61639-183">Reviewing one line at a time is the basic idea of stepping through code.</span></span>  <span data-ttu-id="61639-184">Wenn Sie den Code in betrachten, sehen Sie, dass sich der Fehler wahrscheinlich an `get-started.js` einer anderen Stelle in der Funktion `updateLabel()` befindet.</span><span class="sxs-lookup"><span data-stu-id="61639-184">If you look at the code in `get-started.js`, you see that the bug is probably somewhere in the `updateLabel()` function.</span></span>  <span data-ttu-id="61639-185">Anstatt jede Codezeile zu durchschritten, können Sie einen anderen Haltepunkttyp verwenden, um den Code näher an der voraussichtlichen Stelle des Fehlers anzuhalten.</span><span class="sxs-lookup"><span data-stu-id="61639-185">Rather than stepping through every line of code, you may use another type of breakpoint to pause the code closer to the probable location of the bug.</span></span>  

## <span data-ttu-id="61639-186">Schritt 5: Festlegen eines Codezeile-Haltepunkts</span><span class="sxs-lookup"><span data-stu-id="61639-186">Step 5: Set a line-of-code breakpoint</span></span>  

<span data-ttu-id="61639-187">Codelinien-Haltepunkte sind der am häufigsten verwendeten Haltepunkttyp.</span><span class="sxs-lookup"><span data-stu-id="61639-187">Line-of-code breakpoints are the most common type of breakpoint.</span></span>  <span data-ttu-id="61639-188">Wenn Sie zu der bestimmten Codezeile kommen, die Sie anhalten möchten, verwenden Sie einen Codezeile-Haltepunkt.</span><span class="sxs-lookup"><span data-stu-id="61639-188">When you get to the specific line of code you want to pause, use a line-of-code breakpoint.</span></span>  

1.  <span data-ttu-id="61639-189">Sehen Sie sich die letzte Codezeile `updateLabel()` in:</span><span class="sxs-lookup"><span data-stu-id="61639-189">Look at the last line of code in `updateLabel()`:</span></span>  
    
    ```javascript
    label.textContent = addend1 + ' + ' + addend2 + ' = ' + sum;
    ```  
    
1.  <span data-ttu-id="61639-190">Auf der linken Seite wird die Nummer dieser bestimmten Codezeile als **34 angezeigt.**</span><span class="sxs-lookup"><span data-stu-id="61639-190">On the left, the number of this particular line of code is displayed as **34**.</span></span>  <span data-ttu-id="61639-191">Wählen Sie Zeile **34 aus.**</span><span class="sxs-lookup"><span data-stu-id="61639-191">Choose line **34**.</span></span>  <span data-ttu-id="61639-192">DevTools setzt links von **34**ein rotes Symbol.</span><span class="sxs-lookup"><span data-stu-id="61639-192">DevTools puts a red icon to the left of **34**.</span></span>  <span data-ttu-id="61639-193">Das rote Symbol gibt an, dass sich in dieser Zeile ein Codezeile-Haltepunkt befindet.</span><span class="sxs-lookup"><span data-stu-id="61639-193">The red icon indicates that a line-of-code breakpoint is on this line.</span></span>  <span data-ttu-id="61639-194">DevTools hält immer an, bevor diese Codezeile ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="61639-194">DevTools always pauses before this line of code is run.</span></span>  
1.  <span data-ttu-id="61639-195">Choose **Resume script execution** \( Resume script execution ![ ][ImageResumeIcon] \).</span><span class="sxs-lookup"><span data-stu-id="61639-195">Choose **Resume script execution** \(![Resume script execution][ImageResumeIcon]\).</span></span>  <span data-ttu-id="61639-196">Das Skript wird weiterhin ausgeführt, bis es Die Zeile 33 erreicht.</span><span class="sxs-lookup"><span data-stu-id="61639-196">The script continues running until it reaches line 33.</span></span>  <span data-ttu-id="61639-197">In den Zeilen 31, 32 und 33 druckt DevTools die Werte von , und rechts neben dem `addend1` `addend2` `sum` Semikolon in jeder Zeile.</span><span class="sxs-lookup"><span data-stu-id="61639-197">On lines 31, 32, and 33, DevTools prints the values of `addend1`, `addend2`, and `sum` to the right of the semi-colon on each line.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-breakpoint-paused.msft.png" alt-text="DevTools hält am Codelinien-Haltepunkt in Zeile 34 an." lightbox="../media/javascript-sources-breakpoint-paused.msft.png":::
       <span data-ttu-id="61639-199">DevTools hält am Codelinien-Haltepunkt in Zeile 34 an.</span><span class="sxs-lookup"><span data-stu-id="61639-199">DevTools pauses on the line-of-code breakpoint on line 34</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="61639-200">Schritt 6: Überprüfen von Variablenwerten</span><span class="sxs-lookup"><span data-stu-id="61639-200">Step 6: Check variable values</span></span>  

<span data-ttu-id="61639-201">Die Werte von `addend1` , `addend2` und sehen `sum` verdächtig aus.</span><span class="sxs-lookup"><span data-stu-id="61639-201">The values of `addend1`, `addend2`, and `sum` look suspicious.</span></span>  <span data-ttu-id="61639-202">Die Werte sind in Anführungszeichen eingeschlossen.</span><span class="sxs-lookup"><span data-stu-id="61639-202">The values are wrapped in quotes.</span></span>  <span data-ttu-id="61639-203">Die Anführungszeichen bedeuten, dass der Wert eine Zeichenfolge ist. Dies ist eine gute Hypothese, um die Ursache des Fehlers zu erläutern.</span><span class="sxs-lookup"><span data-stu-id="61639-203">The quotations mean that the value is a string, which is a good hypothesis to explain the cause of the bug.</span></span>  <span data-ttu-id="61639-204">Sammeln Sie weitere Informationen zur Situation.</span><span class="sxs-lookup"><span data-stu-id="61639-204">Gather more information about the situation.</span></span>  <span data-ttu-id="61639-205">DevTools bietet viele Tools zum Untersuchen von Variablenwerten.</span><span class="sxs-lookup"><span data-stu-id="61639-205">DevTools provides many tools for examining variable values.</span></span>  

### <span data-ttu-id="61639-206">Methode 1: Bereichsbereich</span><span class="sxs-lookup"><span data-stu-id="61639-206">Method 1: The Scope pane</span></span>  

<span data-ttu-id="61639-207">Wenn Sie in einer Codezeile \*\*\*\* anhalten, werden im Bereichsbereich die lokalen und globalen Variablen angezeigt, die derzeit definiert sind, zusammen mit dem Wert jeder Variablen.</span><span class="sxs-lookup"><span data-stu-id="61639-207">If you pause on a line of code, the **Scope** pane displays the local and global variables that are currently defined, along with the value of each variable.</span></span>  <span data-ttu-id="61639-208">Außerdem werden ggf. Schließvariablen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="61639-208">It also displays closure variables, as applicable.</span></span>  <span data-ttu-id="61639-209">Doppelklicken Sie auf einen Variablenwert, um ihn zu bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="61639-209">Double-click a variable value to edit it.</span></span>  <span data-ttu-id="61639-210">Wenn Sie in einer Codezeile nicht anhalten, **ist** der Bereich leer.</span><span class="sxs-lookup"><span data-stu-id="61639-210">If you don't pause on a line of code, the **Scope** pane is empty.</span></span>  

:::image type="complex" source="../media/javascript-sources-breakpoint-paused-scope.msft.png" alt-text="Bereichsbereich" lightbox="../media/javascript-sources-breakpoint-paused-scope.msft.png":::
   <span data-ttu-id="61639-212">**Bereichsbereich**</span><span class="sxs-lookup"><span data-stu-id="61639-212">The **Scope** pane</span></span>  
:::image-end:::  

### <span data-ttu-id="61639-213">Methode 2: Ausdrücke ansehen</span><span class="sxs-lookup"><span data-stu-id="61639-213">Method 2: Watch Expressions</span></span>  

<span data-ttu-id="61639-214">Im **Bereich "Überwachungsausdrücke"** können Sie die Werte von Variablen im Laufe der Zeit überwachen.</span><span class="sxs-lookup"><span data-stu-id="61639-214">The **Watch Expressions** pane lets you monitor the values of variables over time.</span></span>  <span data-ttu-id="61639-215">Wie der Name schon sagt, sind **Watch Expressions** nicht auf Variablen beschränkt.</span><span class="sxs-lookup"><span data-stu-id="61639-215">As the name implies, **Watch Expressions** aren't limited to variables.</span></span>  <span data-ttu-id="61639-216">Sie können jeden gültigen JavaScript-Ausdruck in einem **Watch-Ausdruck speichern.**</span><span class="sxs-lookup"><span data-stu-id="61639-216">You may store any valid JavaScript expression in a **Watch Expression**.</span></span>  <span data-ttu-id="61639-217">Versuchen Sie es jetzt.</span><span class="sxs-lookup"><span data-stu-id="61639-217">Try it now.</span></span>  

1.  <span data-ttu-id="61639-218">Wählen Sie den **Bereich "Watch"** aus.</span><span class="sxs-lookup"><span data-stu-id="61639-218">Choose the **Watch** pane.</span></span>  
1.  <span data-ttu-id="61639-219">Choose **Add Expression** \( Add Expression ![ ][ImageAddIcon] \).</span><span class="sxs-lookup"><span data-stu-id="61639-219">Choose **Add Expression** \(![Add Expression][ImageAddIcon]\).</span></span>  
1.  <span data-ttu-id="61639-220">Geben Sie `typeof sum` ein.</span><span class="sxs-lookup"><span data-stu-id="61639-220">Type `typeof sum`.</span></span>  
1.  <span data-ttu-id="61639-221">Wählen Sie `Enter` .</span><span class="sxs-lookup"><span data-stu-id="61639-221">Select `Enter`.</span></span>  <span data-ttu-id="61639-222">DevTools zeigt `typeof sum: "string"` .</span><span class="sxs-lookup"><span data-stu-id="61639-222">DevTools shows `typeof sum: "string"`.</span></span>  <span data-ttu-id="61639-223">Der Wert rechts neben dem Doppelpunkt ist das Ergebnis des Watch-Ausdrucks.</span><span class="sxs-lookup"><span data-stu-id="61639-223">The value to the right of the colon is the result of your Watch Expression.</span></span>  
    
> [!NOTE]
> <span data-ttu-id="61639-224">Im Bereich **"Watch Expression"** (unten rechts\) in der folgenden Abbildung wird der Watch `typeof sum` Expression angezeigt.</span><span class="sxs-lookup"><span data-stu-id="61639-224">In the **Watch Expression** pane \(bottom-right\) in the following figure, the `typeof sum` Watch Expression is displayed.</span></span>  <span data-ttu-id="61639-225">Wenn ihr DevTools-Fenster groß ist, befindet sich der Bereich "Watch **Expression"** auf der rechten Seite über dem Bereich "Haltepunkte des Ereignislisteners". \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="61639-225">If your DevTools window is large, the **Watch Expression** pane is on the right above the **Event Listener Breakpoints** pane.</span></span>  

:::image type="complex" source="../media/javascript-sources-breakpoint-paused-watch.msft.png" alt-text="Der Bereich "Watch Expression"" lightbox="../media/javascript-sources-breakpoint-paused-watch.msft.png":::
   <span data-ttu-id="61639-227">Der **Bereich "Watch Expression"**</span><span class="sxs-lookup"><span data-stu-id="61639-227">The **Watch Expression** pane</span></span>  
:::image-end:::  

<span data-ttu-id="61639-228">Wie verdächtig, `sum` wird sie als Zeichenfolge ausgewertet, wenn es sich um eine Zahl handelt.</span><span class="sxs-lookup"><span data-stu-id="61639-228">As suspected, `sum` is being evaluated as a string, when it should be a number.</span></span>  <span data-ttu-id="61639-229">Sie haben nun bestätigt, dass der Werttyp die Ursache des Fehlers ist.</span><span class="sxs-lookup"><span data-stu-id="61639-229">You now confirmed value type is the cause of the bug.</span></span>  

### <span data-ttu-id="61639-230">Methode 3: Die Konsole</span><span class="sxs-lookup"><span data-stu-id="61639-230">Method 3: The Console</span></span>  

<span data-ttu-id="61639-231">Mit **der Konsole** können Sie Nachrichten anzeigen und sie auch zum `console.log()` Auswerten beliebiger JavaScript-Anweisungen verwenden.</span><span class="sxs-lookup"><span data-stu-id="61639-231">The **Console** allows you to view `console.log()` messages and you may also use it to evaluate arbitrary JavaScript statements.</span></span>  <span data-ttu-id="61639-232">Zum Debuggen können Sie die **Konsole** verwenden, um potenzielle Fehlerbehebungen zu testen.</span><span class="sxs-lookup"><span data-stu-id="61639-232">For debugging, you may use the **Console** to test potential fixes for bugs.</span></span>  <span data-ttu-id="61639-233">Versuchen Sie es jetzt.</span><span class="sxs-lookup"><span data-stu-id="61639-233">Try it now.</span></span>  

1.  <span data-ttu-id="61639-234">Wenn die **Konsolenschubschubte** geschlossen ist, wählen Sie `Escape` sie aus, um sie zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="61639-234">If the **Console** drawer is closed, select `Escape` to open it.</span></span>  <span data-ttu-id="61639-235">Die \*\*\*\* Konsolenschubschubleiste wird im unteren Bereich des Fensters DevTools geöffnet.</span><span class="sxs-lookup"><span data-stu-id="61639-235">The **Console** drawer opens in the lower panel of the DevTools window.</span></span>  
1.  <span data-ttu-id="61639-236">Geben Sie in **der Konsole**den Text `parseInt(addend1) + parseInt(addend2)` ein.</span><span class="sxs-lookup"><span data-stu-id="61639-236">In the **Console**, type `parseInt(addend1) + parseInt(addend2)`.</span></span>  <span data-ttu-id="61639-237">Die Anweisung, mit der das Tool in einer Codezeile angehalten wird, in der sich der Bereich `addend1` `addend2` befindet.</span><span class="sxs-lookup"><span data-stu-id="61639-237">The statement the tool is paused on a line of code where `addend1` and `addend2` are in scope.</span></span>  
1.  <span data-ttu-id="61639-238">Wählen Sie `Enter` .</span><span class="sxs-lookup"><span data-stu-id="61639-238">Select `Enter`.</span></span>  <span data-ttu-id="61639-239">DevTools wertet die Anweisung aus und druckt , was das Ergebnis ist, das Sie von `6` der Demo erwarten.</span><span class="sxs-lookup"><span data-stu-id="61639-239">DevTools evaluates the statement and prints `6`, which is the result you expect the demo to produce.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-breakpoint-paused-console.msft.png" alt-text="Die Konsolenschubschubte nach der Auswertung von parseInt(addend1) + parseInt(addend2)" lightbox="../media/javascript-sources-breakpoint-paused-console.msft.png":::
       <span data-ttu-id="61639-241">Die **Konsolenschubschubte** nach der Auswertung</span><span class="sxs-lookup"><span data-stu-id="61639-241">The **Console** drawer, after evaluating</span></span> `parseInt(addend1) + parseInt(addend2)`  
    :::image-end:::  
    
## <span data-ttu-id="61639-242">Schritt 7: Anwenden eines Fixs</span><span class="sxs-lookup"><span data-stu-id="61639-242">Step 7: Apply a fix</span></span>  

<span data-ttu-id="61639-243">Wenn Sie einen Fix für den Fehler finden, probieren Sie Ihre Korrektur aus, indem Sie den Code bearbeiten und die Demo erneut ausführen.</span><span class="sxs-lookup"><span data-stu-id="61639-243">If you find a fix for the bug, try out your fix by editing the code and rerunning the demo.</span></span>  <span data-ttu-id="61639-244">Sie können JavaScript-Code direkt in der DevTools-Benutzeroberfläche bearbeiten und den Fix anwenden.</span><span class="sxs-lookup"><span data-stu-id="61639-244">You may edit JavaScript code directly within the DevTools UI and apply the fix.</span></span>  <span data-ttu-id="61639-245">Versuchen Sie es jetzt.</span><span class="sxs-lookup"><span data-stu-id="61639-245">Try it now.</span></span>  

1.  <span data-ttu-id="61639-246">Choose **Resume script execution** \( Resume script execution ![ ][ImageResumeIcon] \).</span><span class="sxs-lookup"><span data-stu-id="61639-246">Choose **Resume script execution** \(![Resume script execution][ImageResumeIcon]\).</span></span>  
1.  <span data-ttu-id="61639-247">Ersetzen Sie **im Code-Editor**Zeile 32 `var sum = addend1 + addend2` durch `var sum = parseInt(addend1) + parseInt(addend2)` .</span><span class="sxs-lookup"><span data-stu-id="61639-247">In the **Code Editor**, replace line 32, `var sum = addend1 + addend2`, with `var sum = parseInt(addend1) + parseInt(addend2)`.</span></span>  
1.  <span data-ttu-id="61639-248">Wählen `Control` + `S` Sie \(Windows, Linux\) oder `Command` + `S` \(macOS\) aus, um Ihre Änderung zu speichern.</span><span class="sxs-lookup"><span data-stu-id="61639-248">Select `Control`+`S` \(Windows, Linux\) or `Command`+`S` \(macOS\) to save your change.</span></span>  
1.  <span data-ttu-id="61639-249">Choose **Deactivate breakpoints** \( ![ Deactivate breakpoints ][ImageDeactivateIcon] \).</span><span class="sxs-lookup"><span data-stu-id="61639-249">Choose **Deactivate breakpoints** \(![Deactivate breakpoints][ImageDeactivateIcon]\).</span></span>  <span data-ttu-id="61639-250">Es ändert sich blau, um anzugeben, dass die Option aktiv ist.</span><span class="sxs-lookup"><span data-stu-id="61639-250">It changes blue to indicate the option is active.</span></span>  <span data-ttu-id="61639-251">Während **Haltepunkte deaktiviert sind,** ignoriert DevTools alle von Ihnen festgelegten Haltepunkte.</span><span class="sxs-lookup"><span data-stu-id="61639-251">While **Deactivate breakpoints** is set, DevTools ignores any breakpoints you set.</span></span>  
1.  <span data-ttu-id="61639-252">Testen Sie die Demo mit unterschiedlichen Werten.</span><span class="sxs-lookup"><span data-stu-id="61639-252">Try out the demo with different values.</span></span>  <span data-ttu-id="61639-253">Die Demo wird nun korrekt berechnet.</span><span class="sxs-lookup"><span data-stu-id="61639-253">The demo now calculates correctly.</span></span>  
    
> [!CAUTION]
> <span data-ttu-id="61639-254">Dieser Workflow wendet nur eine Korrektur auf den Code an, der in Ihrem Browser ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="61639-254">This workflow only applies a fix to the code that is running in your browser.</span></span>  <span data-ttu-id="61639-255">Der Code für alle Benutzer, die Ihre Webseite besuchen, wird nicht korrigiert.</span><span class="sxs-lookup"><span data-stu-id="61639-255">It does not fix the code for all users that visit your webpage.</span></span>  <span data-ttu-id="61639-256">Dazu müssen Sie den Code auf den Servern korrigieren.</span><span class="sxs-lookup"><span data-stu-id="61639-256">To do that, you need to fix the code that is on your servers.</span></span>  

## <span data-ttu-id="61639-257">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="61639-257">Next steps</span></span>  

<span data-ttu-id="61639-258">Herzlichen Glückwunsch!</span><span class="sxs-lookup"><span data-stu-id="61639-258">Congratulations!</span></span>  <span data-ttu-id="61639-259">Sie wissen nun, wie Sie Microsoft Edge DevTools beim Debuggen von JavaScript nutzen.</span><span class="sxs-lookup"><span data-stu-id="61639-259">You now know how to make the most of Microsoft Edge DevTools when debugging JavaScript.</span></span>  <span data-ttu-id="61639-260">Die Tools und Methoden, die Sie in diesem Artikel gelernt haben, können Stunden sparen.</span><span class="sxs-lookup"><span data-stu-id="61639-260">The tools and methods you learned in this article may save you countless hours.</span></span>  

<span data-ttu-id="61639-261">In diesem Artikel wurden ihnen nur zwei Methoden zum Festlegen von Haltepunkten erläutert.</span><span class="sxs-lookup"><span data-stu-id="61639-261">This article only taught you two ways to set breakpoints.</span></span>  <span data-ttu-id="61639-262">DevTools bietet viele weitere Möglichkeiten, einschließlich der folgenden Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="61639-262">DevTools offers many other ways including the following settings.</span></span>  

*   <span data-ttu-id="61639-263">Bedingte Haltepunkte, die nur ausgelöst werden, wenn die bedingung, die Sie bereitstellen, wahr ist.</span><span class="sxs-lookup"><span data-stu-id="61639-263">Conditional breakpoints that are only triggered when the condition that you provide is true.</span></span>  
*   <span data-ttu-id="61639-264">Haltepunkte für abgefangene oder nicht abgefangene Ausnahmen.</span><span class="sxs-lookup"><span data-stu-id="61639-264">Breakpoints on caught or uncaught exceptions.</span></span>  
*   <span data-ttu-id="61639-265">XHR-Haltepunkte, die ausgelöst werden, wenn die angeforderte URL einer von Ihnen angegebenen Teilzeichenfolge entspricht.</span><span class="sxs-lookup"><span data-stu-id="61639-265">XHR breakpoints that are triggered when the requested URL matches a substring that you provide.</span></span>  
    
<span data-ttu-id="61639-266">Weitere Informationen dazu, wann und wie Sie die einzelnen Typen verwenden, finden Sie unter ["Ihren Code mit Haltepunkten anhalten".][DevtoolsJavscriptBreakpoints]</span><span class="sxs-lookup"><span data-stu-id="61639-266">For more information about when and how to use each type, navigate to [Pause Your Code With Breakpoints][DevtoolsJavscriptBreakpoints].</span></span>  

<span data-ttu-id="61639-267">Einige Steuerelemente für die Codeschritte werden in diesem Artikel nicht erläutert.</span><span class="sxs-lookup"><span data-stu-id="61639-267">A couple of code stepping controls aren't explained in this article.</span></span>  <span data-ttu-id="61639-268">Weitere Informationen finden Sie unter ["Schritt über Codezeile".][DevtoolsJavascriptReferenceStepThroughCode]</span><span class="sxs-lookup"><span data-stu-id="61639-268">For more information, navigate to [Step over line of code][DevtoolsJavascriptReferenceStepThroughCode].</span></span>  

## <span data-ttu-id="61639-269">Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen</span><span class="sxs-lookup"><span data-stu-id="61639-269">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageAddIcon]: ../media/add-expression-icon.msft.png  
[ImageDeactivateIcon]: ../media/deactivate-breakpoints-button-icon.msft.png  
[ImageExpandIcon]: ../media/expand-icon.msft.png  
[ImageIntoIcon]: ../media/step-into-icon.msft.png  
[ImageOverIcon]: ../media/step-over-icon.msft.png  
[ImageResumeIcon]: ../media/resume-script-run-icon.msft.png  

<!-- links -->  

[DevtoolsJavscriptBreakpoints]: ./breakpoints.md "So unterbrechen Sie Ihren Code mit Haltepunkten in Microsoft Edge DevTools | Microsoft Docs"
[DevtoolsJavascriptReferenceStepThroughCode]: ./reference.md#step-through-code "Schritt-für-Schritt-Code – JavaScript-Debugreferenz-| Microsoft Docs"

<!--[inPrivate]: https://support.alphabet.com/alphabet-browser/answer/95464  -->  

[OpenDebugJSDemo]: https://microsoft-edge-chromium-devtools.glitch.me/debug-js/get-started.html "Öffnen der Demo-| Glitch"  

> [!NOTE]
> <span data-ttu-id="61639-273">Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="61639-273">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="61639-274">Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/javascript/index) und wird von [Kayce Baskisch][KayceBasques] \(Technical Writer, Chrome DevTools \& Vorsteller\) verfasst.</span><span class="sxs-lookup"><span data-stu-id="61639-274">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/javascript/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="61639-276">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="61639-276">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
