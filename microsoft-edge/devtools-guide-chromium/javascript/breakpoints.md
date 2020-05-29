---
title: Anhalten des Codes mit Haltepunkten in Microsoft Edge devtools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/18/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Web-Entwicklung, F12-Tools, devtools
ms.openlocfilehash: 2afa4b7dbe96b65747ec17b147f0a82c16efa288
ms.sourcegitcommit: ecdc4287fa25a18cb4ddcaf43fcce3b396c3314c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/17/2020
ms.locfileid: "10581803"
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







# <span data-ttu-id="dcd08-103">Anhalten des Codes mit Haltepunkten in Microsoft Edge devtools</span><span class="sxs-lookup"><span data-stu-id="dcd08-103">How To Pause Your Code With Breakpoints In Microsoft Edge DevTools</span></span>   



<span data-ttu-id="dcd08-104">Verwenden Sie Haltepunkte, um Ihren JavaScript-Code anzuhalten.</span><span class="sxs-lookup"><span data-stu-id="dcd08-104">Use breakpoints to pause your JavaScript code.</span></span>  <span data-ttu-id="dcd08-105">In diesem Leitfaden werden die einzelnen Typen von Haltepunkten erläutert, die in devtools zur Verfügung stehen, sowie Informationen dazu, wann und wie die einzelnen Typen festzulegen sind.</span><span class="sxs-lookup"><span data-stu-id="dcd08-105">This guide explains each type of breakpoint that is available in DevTools, as well as when to use and how to set each type.</span></span>  <span data-ttu-id="dcd08-106">Eine praktische Einführung in den Debuggingprozess finden Sie unter [Erste Schritte mit dem Debuggen von JavaScript in Microsoft Edge devtools][DevtoolsJavascriptIndex].</span><span class="sxs-lookup"><span data-stu-id="dcd08-106">For a hands-on tutorial of the debugging process, see [Get Started with Debugging JavaScript in Microsoft Edge DevTools][DevtoolsJavascriptIndex].</span></span>  

## <span data-ttu-id="dcd08-107">Übersicht über die Verwendung der einzelnen Haltepunkttypen</span><span class="sxs-lookup"><span data-stu-id="dcd08-107">Overview of when to use each breakpoint type</span></span>   

<span data-ttu-id="dcd08-108">Der bekannteste Breakpoint-Typ ist "Codezeile".</span><span class="sxs-lookup"><span data-stu-id="dcd08-108">The most well-known type of breakpoint is line-of-code.</span></span>  <span data-ttu-id="dcd08-109">Es ist jedoch möglich, dass die festgelegten Code Haltepunkte nicht besonders effizient sind, wenn Sie nicht genau wissen, wo Sie suchen müssen, oder wenn Sie mit einer umfangreichen CodeBase arbeiten.</span><span class="sxs-lookup"><span data-stu-id="dcd08-109">But line-of-code breakpoints may be inefficient to set, especially if you do not know exactly where to look, or if you are working with a large codebase.</span></span>  <span data-ttu-id="dcd08-110">Sie können beim Debuggen Zeit sparen, indem Sie wissen, wie und wann die anderen Arten von Haltepunkten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="dcd08-110">You may save yourself time when debugging by knowing how and when to use the other types of breakpoints.</span></span>  

| <span data-ttu-id="dcd08-111">Breakpoint-Typ</span><span class="sxs-lookup"><span data-stu-id="dcd08-111">Breakpoint Type</span></span> | <span data-ttu-id="dcd08-112">Verwenden Sie diese Taste, wenn Sie anhalten möchten...</span><span class="sxs-lookup"><span data-stu-id="dcd08-112">Use This When You Want To Pause...</span></span>  |  
|:--- |:--- |  
| [<span data-ttu-id="dcd08-113">Codezeile</span><span class="sxs-lookup"><span data-stu-id="dcd08-113">Line-of-code</span></span>](#line-of-code-breakpoints) | <span data-ttu-id="dcd08-114">In einem exakten Codebereich.</span><span class="sxs-lookup"><span data-stu-id="dcd08-114">On an exact region of code.</span></span>  |  
| [<span data-ttu-id="dcd08-115">Bedingte Codezeile</span><span class="sxs-lookup"><span data-stu-id="dcd08-115">Conditional line-of-code</span></span>](#conditional-line-of-code-breakpoints) | <span data-ttu-id="dcd08-116">In einem exakten Codebereich, aber nur, wenn eine andere Bedingung wahr ist.</span><span class="sxs-lookup"><span data-stu-id="dcd08-116">On an exact region of code, but only when some other condition is true.</span></span>  |  
| [<span data-ttu-id="dcd08-117">DOM</span><span class="sxs-lookup"><span data-stu-id="dcd08-117">DOM</span></span>](#dom-change-breakpoints) | <span data-ttu-id="dcd08-118">Auf dem Code, der einen bestimmten DOM-Knoten ändert oder entfernt, oder die untergeordneten Elemente.</span><span class="sxs-lookup"><span data-stu-id="dcd08-118">On the code that changes or removes a specific DOM node, or the children.</span></span>  |  
| [<span data-ttu-id="dcd08-119">XMLHttpRequest</span><span class="sxs-lookup"><span data-stu-id="dcd08-119">XHR</span></span>](#xhrfetch-breakpoints) | <span data-ttu-id="dcd08-120">Wenn eine XMLHttpRequest-URL ein Zeichenfolgenmuster enthält.</span><span class="sxs-lookup"><span data-stu-id="dcd08-120">When an XHR URL contains a string pattern.</span></span>  |  
| [<span data-ttu-id="dcd08-121">Ereignis-Listener</span><span class="sxs-lookup"><span data-stu-id="dcd08-121">Event listener</span></span>](#event-listener-breakpoints) | <span data-ttu-id="dcd08-122">Auf dem Code, der nach einem Ereignis ausgeführt wird, beispielsweise `click` , wird ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="dcd08-122">On the code that runs after an event, such as `click`, runs.</span></span>  |  
| [<span data-ttu-id="dcd08-123">Ausnahme</span><span class="sxs-lookup"><span data-stu-id="dcd08-123">Exception</span></span>](#exception-breakpoints) | <span data-ttu-id="dcd08-124">In der Codezeile, die eine abgefangene oder nicht abgefangene Ausnahme auslöst.</span><span class="sxs-lookup"><span data-stu-id="dcd08-124">On the line of code that is throwing a caught or uncaught exception.</span></span>  |  
| [<span data-ttu-id="dcd08-125">Funktion</span><span class="sxs-lookup"><span data-stu-id="dcd08-125">Function</span></span>](#function-breakpoints) | <span data-ttu-id="dcd08-126">Jedes Mal, wenn ein bestimmter Befehl, eine bestimmte Funktion oder Methode ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="dcd08-126">Whenever a specific command, function, or method is run.</span></span>  |  

## <span data-ttu-id="dcd08-127">Haltepunkte für die Code Zeile</span><span class="sxs-lookup"><span data-stu-id="dcd08-127">Line-of-code breakpoints</span></span>   

<span data-ttu-id="dcd08-128">Verwenden Sie einen Haltepunkt für die Codezeile, wenn Sie den genauen Codebereich kennen, den Sie untersuchen müssen.</span><span class="sxs-lookup"><span data-stu-id="dcd08-128">Use a line-of-code breakpoint when you know the exact region of code that you need to investigate.</span></span>  <span data-ttu-id="dcd08-129">DevTools wird **immer** angehalten, bevor diese Codezeile ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="dcd08-129">DevTools **always** pauses before this line of code is run.</span></span>  

<span data-ttu-id="dcd08-130">So setzen Sie einen Code Haltepunkt in devtools:</span><span class="sxs-lookup"><span data-stu-id="dcd08-130">To set a line-of-code breakpoint in DevTools:</span></span>  

1.  <span data-ttu-id="dcd08-131">Klicken Sie auf die Registerkarte **Quellen** .</span><span class="sxs-lookup"><span data-stu-id="dcd08-131">Click the **Sources** tab.</span></span>  
1.  <span data-ttu-id="dcd08-132">Öffnen Sie die Datei, die die Codezeile enthält, für die Sie eine Unterbrechung durchführen möchten.</span><span class="sxs-lookup"><span data-stu-id="dcd08-132">Open the file containing the line of code on which you want to break.</span></span>  
1.  <span data-ttu-id="dcd08-133">Wechseln Sie zur Codezeile.</span><span class="sxs-lookup"><span data-stu-id="dcd08-133">Go the line of code.</span></span>  
1.  <span data-ttu-id="dcd08-134">Links neben der Codezeile befindet sich die Spalte "Zeile".</span><span class="sxs-lookup"><span data-stu-id="dcd08-134">To the left of the line of code is the line number column.</span></span>  <span data-ttu-id="dcd08-135">Klicken Sie darauf.</span><span class="sxs-lookup"><span data-stu-id="dcd08-135">Click on it.</span></span>  <span data-ttu-id="dcd08-136">Neben der Spalte "Zeile Nummer" wird ein rotes Symbol angezeigt.</span><span class="sxs-lookup"><span data-stu-id="dcd08-136">A red icon appears next to the line number column.</span></span>  

> ##### <span data-ttu-id="dcd08-137">Abbildung1</span><span class="sxs-lookup"><span data-stu-id="dcd08-137">Figure 1</span></span>  
> <span data-ttu-id="dcd08-138">Ein in Zeile 30 eingestellter Haltepunkt für den Code</span><span class="sxs-lookup"><span data-stu-id="dcd08-138">A line-of-code breakpoint set on line 30</span></span>  
> ![Ein Haltepunkt für eine Codezeile][ImageLocBreakpoint]  

### <span data-ttu-id="dcd08-140">Haltepunkte für die Code Zeile im Code</span><span class="sxs-lookup"><span data-stu-id="dcd08-140">Line-of-code breakpoints in your code</span></span>   

<span data-ttu-id="dcd08-141">Führen `debugger` Sie die Methode aus dem Code aus, um in dieser Zeile anzuhalten.</span><span class="sxs-lookup"><span data-stu-id="dcd08-141">Run the `debugger` method from your code to pause on that line.</span></span>  <span data-ttu-id="dcd08-142">Dies entspricht einem [Zeile-zu-Code-Haltepunkt](#line-of-code-breakpoints), mit der Ausnahme, dass der Haltepunkt im Code festgesetzt wird, nicht auf der devtools-Benutzeroberfläche.</span><span class="sxs-lookup"><span data-stu-id="dcd08-142">This is equivalent to a [line-of-code breakpoint](#line-of-code-breakpoints), except that the breakpoint is set in your code, not in the DevTools UI.</span></span>  

```javascript
console.log('a');
console.log('b');
debugger;
console.log('c');
```  

### <span data-ttu-id="dcd08-143">Bedingte Zeile-für-Code-Haltepunkte</span><span class="sxs-lookup"><span data-stu-id="dcd08-143">Conditional line-of-code breakpoints</span></span>   

<span data-ttu-id="dcd08-144">Verwenden Sie einen bedingten Code Haltepunkt, wenn Sie den genauen Codebereich kennen, den Sie untersuchen müssen, aber nur anhalten möchten, wenn eine andere Bedingung wahr ist.</span><span class="sxs-lookup"><span data-stu-id="dcd08-144">Use a conditional line-of-code breakpoint when you know the exact region of code that you need to investigate, but you want to pause only when some other condition is true.</span></span>  

<span data-ttu-id="dcd08-145">So setzen Sie einen bedingten Haltepunkt für eine bedingte Codezeile:</span><span class="sxs-lookup"><span data-stu-id="dcd08-145">To set a conditional line-of-code breakpoint:</span></span>  

1.  <span data-ttu-id="dcd08-146">Klicken Sie auf die Registerkarte **Quellen** .</span><span class="sxs-lookup"><span data-stu-id="dcd08-146">Click the **Sources** tab.</span></span>  
1.  <span data-ttu-id="dcd08-147">Öffnen Sie die Datei, die die Codezeile enthält, für die Sie eine Unterbrechung durchführen möchten.</span><span class="sxs-lookup"><span data-stu-id="dcd08-147">Open the file containing the line of code on which you want to break.</span></span>  
1.  <span data-ttu-id="dcd08-148">Wechseln Sie zur Codezeile.</span><span class="sxs-lookup"><span data-stu-id="dcd08-148">Go the line of code.</span></span>  
1.  <span data-ttu-id="dcd08-149">Links neben der Codezeile befindet sich die Spalte "Zeile".</span><span class="sxs-lookup"><span data-stu-id="dcd08-149">To the left of the line of code is the line number column.</span></span>  <span data-ttu-id="dcd08-150">Klicken Sie mit der rechten Maustaste auf die Leitungsnummer.</span><span class="sxs-lookup"><span data-stu-id="dcd08-150">Right-click the line number.</span></span>  
1.  <span data-ttu-id="dcd08-151">Wählen Sie **bedingter Haltepunkt hinzufügen**aus.</span><span class="sxs-lookup"><span data-stu-id="dcd08-151">Select **Add conditional breakpoint**.</span></span>  <span data-ttu-id="dcd08-152">Unterhalb der Codezeile wird ein Dialogfeld angezeigt.</span><span class="sxs-lookup"><span data-stu-id="dcd08-152">A dialog displays underneath the line of code.</span></span>  
1.  <span data-ttu-id="dcd08-153">Geben Sie Ihre Bedingung in das Dialogfeld ein.</span><span class="sxs-lookup"><span data-stu-id="dcd08-153">Enter your condition in the dialog.</span></span>  
1.  <span data-ttu-id="dcd08-154">Drücken Sie `Enter` , um den Haltepunkt zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="dcd08-154">Press `Enter` to activate the breakpoint.</span></span>  <span data-ttu-id="dcd08-155">Ein Symbol neben der Spalte "Zeile"</span><span class="sxs-lookup"><span data-stu-id="dcd08-155">An icon next to the line number column.</span></span>  

> ##### <span data-ttu-id="dcd08-156">Abbildung2</span><span class="sxs-lookup"><span data-stu-id="dcd08-156">Figure 2</span></span>  
> <span data-ttu-id="dcd08-157">Ein bedingter Zeile-Code-Haltepunkt, der auf Zeile 34 gesetzt ist</span><span class="sxs-lookup"><span data-stu-id="dcd08-157">A conditional line-of-code breakpoint set on line 34</span></span>  
> ![Ein bedingter Zeile-Code-Haltepunkt][ImageConditionalLocBreakpoint]  

### <span data-ttu-id="dcd08-159">Verwalten von Code Haltepunkten</span><span class="sxs-lookup"><span data-stu-id="dcd08-159">Manage line-of-code breakpoints</span></span>   

<span data-ttu-id="dcd08-160">Verwenden Sie den Bereich **Haltepunkte** , um Code Haltepunkte an einer einzelnen Position zu deaktivieren oder zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="dcd08-160">Use the **Breakpoints** pane to disable or remove line-of-code breakpoints from a single location.</span></span>  

> ##### <span data-ttu-id="dcd08-161">Abbildung 3</span><span class="sxs-lookup"><span data-stu-id="dcd08-161">Figure 3</span></span>  
> <span data-ttu-id="dcd08-162">Der **Haltepunkt** -Panel mit zwei Zeile-zu-Code-Haltepunkten: eine Zeile mit einem `16` `get-started.js` anderen Online</span><span class="sxs-lookup"><span data-stu-id="dcd08-162">The **Breakpoints** panel showing two line-of-code breakpoints: one on line `16` of `get-started.js`, another on line</span></span> `33`  
> ![Der Haltepunkt-Panel][ImageBreakpointsPanel]  

*   <span data-ttu-id="dcd08-164">Aktivieren Sie das Kontrollkästchen neben einem Eintrag, um diesen Haltepunkt zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="dcd08-164">Check the checkbox next to an entry to disable that breakpoint.</span></span>  
*   <span data-ttu-id="dcd08-165">Klicken Sie mit der rechten Maustaste auf einen Eintrag, um diesen Haltepunkt zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="dcd08-165">Right-click an entry to remove that breakpoint.</span></span>  
*   <span data-ttu-id="dcd08-166">Klicken Sie mit der rechten Maustaste auf eine beliebige Stelle im Bereich **Haltepunkte** , um alle Haltepunkte zu deaktivieren, alle Haltepunkte zu deaktivieren oder alle Haltepunkte zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="dcd08-166">Right-click anywhere in the **Breakpoints** pane to deactivate all breakpoints, disable all breakpoints, or remove all breakpoints.</span></span>  <span data-ttu-id="dcd08-167">Das Deaktivieren aller Haltepunkte entspricht der Deaktivierung der einzelnen Haltepunkte.</span><span class="sxs-lookup"><span data-stu-id="dcd08-167">Disabling all breakpoints is equivalent to unchecking each one.</span></span>  <span data-ttu-id="dcd08-168">Durch die Deaktivierung aller Haltepunkte wird devtools angewiesen, alle Zeile-zu-Code-Haltepunkte zu ignorieren, aber auch den aktivierten Zustand beizubehalten, damit sich jeder in demselben Zustand wie zuvor befindet, wenn Sie ihn wieder aktivieren.</span><span class="sxs-lookup"><span data-stu-id="dcd08-168">Deactivating all breakpoints instructs DevTools to ignore all line-of-code breakpoints, but to also maintain the enabled state so that each are in the same state as before when you reactivate each one.</span></span>  

> ##### <span data-ttu-id="dcd08-169">Abbildung4</span><span class="sxs-lookup"><span data-stu-id="dcd08-169">Figure 4</span></span>  
> <span data-ttu-id="dcd08-170">Deaktivierte Haltepunkte im Bereich " **Haltepunkte** " sind deaktiviert und transparent.</span><span class="sxs-lookup"><span data-stu-id="dcd08-170">Deactivated breakpoints in the **Breakpoints** pane are disabled and transparent</span></span>  
> ![Deaktivierte Haltepunkte im Bereich "Haltepunkte"][ImageDeactivatedBreakpoints]  

## <span data-ttu-id="dcd08-172">Dom-Änderungs Haltepunkte</span><span class="sxs-lookup"><span data-stu-id="dcd08-172">DOM change breakpoints</span></span>   

<span data-ttu-id="dcd08-173">Verwenden Sie einen Dom-Änderungs Haltepunkt, wenn Sie den Code anhalten möchten, durch den ein DOM-Knoten oder die untergeordneten Elemente geändert werden.</span><span class="sxs-lookup"><span data-stu-id="dcd08-173">Use a DOM change breakpoint when you want to pause on the code that changes a DOM node or the children.</span></span>  

<span data-ttu-id="dcd08-174">So setzen Sie einen Dom-Änderungs Haltepunkt:</span><span class="sxs-lookup"><span data-stu-id="dcd08-174">To set a DOM change breakpoint:</span></span>  

1.  <span data-ttu-id="dcd08-175">Klicken Sie auf die Registerkarte **Elemente** .</span><span class="sxs-lookup"><span data-stu-id="dcd08-175">Click the **Elements** tab.</span></span>  
1.  <span data-ttu-id="dcd08-176">Wechseln Sie zu dem Element, für das Sie den Haltepunkt festlegen möchten.</span><span class="sxs-lookup"><span data-stu-id="dcd08-176">Go the element on which you want to set the breakpoint.</span></span>  
1.  <span data-ttu-id="dcd08-177">Klicken Sie mit der rechten Maustaste auf das Element.</span><span class="sxs-lookup"><span data-stu-id="dcd08-177">Right-click the element.</span></span>  
1.  <span data-ttu-id="dcd08-178">Zeigen Sie **mit der Maus auf Umbruch**, und wählen Sie dann **Strukturänderungen**, **Attributänderungen**oder **Knoten Entfernung**aus.</span><span class="sxs-lookup"><span data-stu-id="dcd08-178">Hover over **Break on**, then select **Subtree modifications**, **Attribute modifications**, or **Node removal**.</span></span>  

> ##### <span data-ttu-id="dcd08-179">Abbildung5</span><span class="sxs-lookup"><span data-stu-id="dcd08-179">Figure 5</span></span>  
> <span data-ttu-id="dcd08-180">Das Kontextmenü zum Erstellen eines DOM-Änderungs Haltepunkts</span><span class="sxs-lookup"><span data-stu-id="dcd08-180">The context menu for creating a DOM change breakpoint</span></span>  
> ![Das Kontextmenü zum Erstellen eines DOM-Änderungs Haltepunkts][ImageDomChangeBreakpoint]  

### <span data-ttu-id="dcd08-182">Typen von Dom-Änderungs Haltepunkten</span><span class="sxs-lookup"><span data-stu-id="dcd08-182">Types of DOM change breakpoints</span></span>   

*   <span data-ttu-id="dcd08-183">Teil **Strukturänderungen**.</span><span class="sxs-lookup"><span data-stu-id="dcd08-183">**Subtree modifications**.</span></span>  <span data-ttu-id="dcd08-184">Wird ausgelöst, wenn ein untergeordnetes Element des aktuell ausgewählten Knotens entfernt oder hinzugefügt oder der Inhalt eines untergeordneten Elements geändert wird.</span><span class="sxs-lookup"><span data-stu-id="dcd08-184">Triggered when a child of the currently-selected node is removed or added, or the contents of a child are changed.</span></span>  <span data-ttu-id="dcd08-185">Wird nicht für Änderungen an einem Attribut des untergeordneten Knotens oder für Änderungen am aktuell ausgewählten Knoten ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="dcd08-185">Not triggered on child node attribute changes, or on any changes to the currently-selected node.</span></span>  

*   <span data-ttu-id="dcd08-186">Attribut **Änderungen**: wird ausgelöst, wenn ein Attribut auf dem aktuell ausgewählten Knoten hinzugefügt oder entfernt wird oder wenn sich ein Attributwert ändert.</span><span class="sxs-lookup"><span data-stu-id="dcd08-186">**Attributes modifications**: Triggered when an attribute is added or removed on the currently-selected node, or when an attribute value changes.</span></span>  

*   <span data-ttu-id="dcd08-187">**Knoten Entfernung**: wird ausgelöst, wenn der aktuell ausgewählte Knoten entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="dcd08-187">**Node Removal**: Triggered when the currently-selected node is removed.</span></span>  

## <span data-ttu-id="dcd08-188">XMLHttpRequest/FETCH-Haltepunkte</span><span class="sxs-lookup"><span data-stu-id="dcd08-188">XHR/Fetch breakpoints</span></span>   

<span data-ttu-id="dcd08-189">Verwenden Sie einen XMLHttpRequest-Haltepunkt, wenn Sie unterbrechen möchten, wenn die Anforderungs-URL eines XMLHttpRequest eine angegebene Zeichenfolge enthält.</span><span class="sxs-lookup"><span data-stu-id="dcd08-189">Use an XHR breakpoint when you want to break when the request URL of an XHR contains a specified string.</span></span>  <span data-ttu-id="dcd08-190">DevTools wird in der Codezeile angehalten, in der die XMLHttpRequest die `send()` Methode ausführt.</span><span class="sxs-lookup"><span data-stu-id="dcd08-190">DevTools pauses on the line of code where the XHR runs the `send()` method.</span></span>  

> [!NOTE]
> <span data-ttu-id="dcd08-191">Dieses Feature funktioniert auch mit [Fetch-API-][MDNFetchApi] Anforderungen.</span><span class="sxs-lookup"><span data-stu-id="dcd08-191">This feature also works with [Fetch API][MDNFetchApi] requests.</span></span>  

<span data-ttu-id="dcd08-192">Wenn dies hilfreich ist, können Sie beispielsweise feststellen, dass die Seite eine falsche URL anfordert, und Sie möchten schnell den AJAX-oder Fetch-Quellcode finden, der die falsche Anforderung verursacht.</span><span class="sxs-lookup"><span data-stu-id="dcd08-192">One example of when this is helpful is when you see that your page is requesting an incorrect URL, and you want to quickly find the AJAX or Fetch source code that is causing the incorrect request.</span></span>  

<span data-ttu-id="dcd08-193">So setzen Sie einen XMLHttpRequest-Haltepunkt:</span><span class="sxs-lookup"><span data-stu-id="dcd08-193">To set an XHR breakpoint:</span></span>  

1.  <span data-ttu-id="dcd08-194">Klicken Sie auf die Registerkarte **Quellen** .</span><span class="sxs-lookup"><span data-stu-id="dcd08-194">Click the **Sources** tab.</span></span>  
1.  <span data-ttu-id="dcd08-195">Erweitern Sie den Bereich **XMLHttpRequest-Haltepunkte** .</span><span class="sxs-lookup"><span data-stu-id="dcd08-195">Expand the **XHR Breakpoints** pane.</span></span>  
1.  <span data-ttu-id="dcd08-196">Klicken Sie auf **Haltepunkt hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="dcd08-196">Click **Add breakpoint**.</span></span>  
1.  <span data-ttu-id="dcd08-197">Geben Sie die Zeichenfolge ein, die Sie aufheben möchten.</span><span class="sxs-lookup"><span data-stu-id="dcd08-197">Enter the string which you want to break on.</span></span>  <span data-ttu-id="dcd08-198">DevTools wird angehalten, wenn diese Zeichenfolge an einer beliebigen Stelle in einer XMLHttpRequest-Anforderungs-URL vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="dcd08-198">DevTools pauses when this string is present anywhere in an XHR request URL.</span></span>  
1.  <span data-ttu-id="dcd08-199">Drücken Sie `Enter` , um zu bestätigen.</span><span class="sxs-lookup"><span data-stu-id="dcd08-199">Press `Enter` to confirm.</span></span>  

> ##### <span data-ttu-id="dcd08-200">Abbildung6</span><span class="sxs-lookup"><span data-stu-id="dcd08-200">Figure 6</span></span>  
> <span data-ttu-id="dcd08-201">Erstellen eines XMLHttpRequest-Haltepunkts in den **XMLHttpRequest-Haltepunkten** für jede Anforderung, die `org` in der URL enthalten ist</span><span class="sxs-lookup"><span data-stu-id="dcd08-201">Creating an XHR breakpoint in the **XHR Breakpoints** for any request that contains `org` in the URL</span></span>  
> ![Erstellen eines XMLHttpRequest-Haltepunkts][ImageXhrBreakpoint]  

## <span data-ttu-id="dcd08-203">Ereignis-Listener-Haltepunkte</span><span class="sxs-lookup"><span data-stu-id="dcd08-203">Event listener breakpoints</span></span> 

<span data-ttu-id="dcd08-204">Verwenden Sie Ereignis-Listener-Haltepunkte, wenn Sie den Ereignislistener-Code anhalten möchten, der nach dem Auslösen eines Ereignisses ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="dcd08-204">Use event listener breakpoints when you want to pause on the event listener code that runs after an event is fired.</span></span>  <span data-ttu-id="dcd08-205">Sie können bestimmte Ereignisse, beispielsweise `click` oder Kategorien von Ereignissen, wie alle Mausereignisse auswählen.</span><span class="sxs-lookup"><span data-stu-id="dcd08-205">You are able to select specific events, such as `click`, or categories of events, such as all mouse events.</span></span>  

1.  <span data-ttu-id="dcd08-206">Klicken Sie auf die Registerkarte **Quellen** .</span><span class="sxs-lookup"><span data-stu-id="dcd08-206">Click the **Sources** tab.</span></span>  
1.  <span data-ttu-id="dcd08-207">Erweitern Sie den Bereich **Ereignislistener-Haltepunkte** .</span><span class="sxs-lookup"><span data-stu-id="dcd08-207">Expand the **Event Listener Breakpoints** pane.</span></span>  <span data-ttu-id="dcd08-208">DevTools zeigt eine Liste der Ereigniskategorien, wie etwa **Animationen**, an.</span><span class="sxs-lookup"><span data-stu-id="dcd08-208">DevTools shows a list of event categories, such as **Animation**.</span></span>  
1.  <span data-ttu-id="dcd08-209">Überprüfen Sie eine dieser Kategorien, um zu pausieren, wenn ein Ereignis aus dieser Kategorie ausgelöst wird, oder erweitern Sie die Kategorie, und überprüfen Sie ein bestimmtes Ereignis.</span><span class="sxs-lookup"><span data-stu-id="dcd08-209">Check one of these categories to pause whenever any event from that category is fired, or expand the category and check a specific event.</span></span>  

> ##### <span data-ttu-id="dcd08-210">Abbildung7</span><span class="sxs-lookup"><span data-stu-id="dcd08-210">Figure 7</span></span>  
> <span data-ttu-id="dcd08-211">Erstellen eines Ereignis-Listener-Haltepunkts für</span><span class="sxs-lookup"><span data-stu-id="dcd08-211">Creating an event listener breakpoint for</span></span> `deviceorientation`  
> ![Erstellen eines Ereignis-Listener-Haltepunkts][ImageEventListenerBreakpoint]  

## <span data-ttu-id="dcd08-213">Ausnahme Haltepunkte</span><span class="sxs-lookup"><span data-stu-id="dcd08-213">Exception breakpoints</span></span>   

<span data-ttu-id="dcd08-214">Verwenden Sie Ausnahme Haltepunkte, wenn Sie in der Codezeile anhalten möchten, die eine abgefangene oder nicht abgefangene Ausnahme auslöst.</span><span class="sxs-lookup"><span data-stu-id="dcd08-214">Use exception breakpoints when you want to pause on the line of code that is throwing a caught or uncaught exception.</span></span>  

1.  <span data-ttu-id="dcd08-215">Klicken Sie auf die Registerkarte **Quellen** .</span><span class="sxs-lookup"><span data-stu-id="dcd08-215">Click the **Sources** tab.</span></span>  
1.  <span data-ttu-id="dcd08-216">Klicken Sie auf **bei** Ausnahmen anhalten ![ für Ausnahmen anhalten ][ImagePauseOnExceptionsIcon] .</span><span class="sxs-lookup"><span data-stu-id="dcd08-216">Click **Pause on exceptions** ![Pause on exceptions][ImagePauseOnExceptionsIcon].</span></span>  <span data-ttu-id="dcd08-217">Das Symbol wird blau, wenn es aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="dcd08-217">The icon turns blue when enabled.</span></span>  
    
    > ##### <span data-ttu-id="dcd08-218">Abbildung8</span><span class="sxs-lookup"><span data-stu-id="dcd08-218">Figure 8</span></span>  
    > <span data-ttu-id="dcd08-219">Schaltfläche " **auf Ausnahmen pausieren** "</span><span class="sxs-lookup"><span data-stu-id="dcd08-219">The **Pause on exceptions** button</span></span>  
    > ![Schaltfläche "auf Ausnahmen pausieren"][ImagePauseExceptionsHighlight]  

1.  <span data-ttu-id="dcd08-221">**Optional**.</span><span class="sxs-lookup"><span data-stu-id="dcd08-221">**Optional**.</span></span> <span data-ttu-id="dcd08-222">Aktivieren Sie das Kontrollkästchen **auf abgefangene Ausnahmen anhalten** , wenn Sie zusätzlich zu den nicht abgefangenen Ausnahmen auch auf abgefangene Ausnahmen anhalten möchten.</span><span class="sxs-lookup"><span data-stu-id="dcd08-222">Check the **Pause On Caught Exceptions** checkbox if you also want to pause on caught exceptions, in addition to uncaught ones.</span></span>  

> ##### <span data-ttu-id="dcd08-223">Abbildung 9</span><span class="sxs-lookup"><span data-stu-id="dcd08-223">Figure 9</span></span>  
> <span data-ttu-id="dcd08-224">Bei einer nicht abgefangenen Ausnahme angehalten</span><span class="sxs-lookup"><span data-stu-id="dcd08-224">Paused on an uncaught exception</span></span>  
> ![Bei einer nicht abgefangenen Ausnahme angehalten][ImageUncaughtException]  

## <span data-ttu-id="dcd08-226">Funktionshaltepunkte</span><span class="sxs-lookup"><span data-stu-id="dcd08-226">Function breakpoints</span></span>   

<span data-ttu-id="dcd08-227">Führen Sie die Methode aus, `debug(method)` wobei `method` der Befehl, die Funktion oder die Methode, die Sie debuggen möchten, ist, wenn Sie anhalten möchten, wenn eine bestimmte Funktion ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="dcd08-227">Run the `debug(method)` method, where `method` is the command, function, or method you want to debug, when you want to pause whenever a specific function is run.</span></span>  <span data-ttu-id="dcd08-228">Sie können `debug()` in Ihren Code einfügen (wie eine `console.log()` Anweisung) oder die Methode über die devtools-Konsole ausführen.</span><span class="sxs-lookup"><span data-stu-id="dcd08-228">You may insert `debug()` into your code (like a `console.log()` statement) or run the method from the DevTools Console.</span></span>  `debug()` <span data-ttu-id="dcd08-229">entspricht dem Festlegen eines [Haltepunkts für die Code Zeile](#line-of-code-breakpoints) in der ersten Zeile der Funktion.</span><span class="sxs-lookup"><span data-stu-id="dcd08-229">is equivalent to setting a [line-of-code breakpoint](#line-of-code-breakpoints) on the first line of the function.</span></span>  

```javascript
function sum(a, b) {
    let result = a + b; // DevTools pauses on this line.
    return result;
}
debug(sum); // Pass the function object, not a string.
sum();
```  

### <span data-ttu-id="dcd08-230">Sicherstellen, dass sich die Zielfunktion im Bereich befindet</span><span class="sxs-lookup"><span data-stu-id="dcd08-230">Make sure the target function is in scope</span></span>   

<span data-ttu-id="dcd08-231">DevTools löst a `ReferenceError` aus, wenn sich die zu debuggende Funktion nicht im Bereich befindet.</span><span class="sxs-lookup"><span data-stu-id="dcd08-231">DevTools throws a `ReferenceError` if the function you want to debug is not in scope.</span></span>  

```javascript
(function () {
    function hey() {
        console.log('hey');
    }
    function yo() {
        console.log('yo');
    }
    debug(yo); // This works.
    yo();
})();
debug(hey); // This does not work.  hey() is out of scope.
```  

<span data-ttu-id="dcd08-232">Die Sicherstellung, dass die Zielfunktion im Bereich liegt, ist schwierig, wenn Sie die `debug()` Methode über die devtools-Konsole ausführen.</span><span class="sxs-lookup"><span data-stu-id="dcd08-232">Ensuring the target function is in scope is tricky if you are running the `debug()` method from the DevTools Console.</span></span>  <span data-ttu-id="dcd08-233">Hier ist eine Strategie:</span><span class="sxs-lookup"><span data-stu-id="dcd08-233">Here is one strategy:</span></span>  

1.  <span data-ttu-id="dcd08-234">Setzen Sie einen [Haltepunkt für die Codezeile](#line-of-code-breakpoints) an einer beliebigen Stelle, an der sich die Funktion im Bereich befindet.</span><span class="sxs-lookup"><span data-stu-id="dcd08-234">Set a [line-of-code breakpoint](#line-of-code-breakpoints) somewhere where the function is in scope.</span></span>
1.  <span data-ttu-id="dcd08-235">Auslösen des Haltepunkts</span><span class="sxs-lookup"><span data-stu-id="dcd08-235">Trigger the breakpoint.</span></span>  
1.  <span data-ttu-id="dcd08-236">Führen `debug()` Sie die Methode in der devtools-Konsole aus, während der Code weiterhin auf dem Haltepunkt für die Code Zeile angehalten wird.</span><span class="sxs-lookup"><span data-stu-id="dcd08-236">Run the `debug()` method in the DevTools Console while the code is still paused on your line-of-code breakpoint.</span></span>  

 



<!-- image links -->  

[ImagePauseOnExceptionsIcon]: /microsoft-edge/devtools-guide-chromium/media/pause-on-exceptions-icon.msft.png  

[ImageLocBreakpoint]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-page-js-breakpoint-30.msft.png "Abbildung 1: ein Haltepunkt für eine Codezeile"  
[ImageConditionalLocBreakpoint]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-page-js-conditional-breakpoint.msft.png "Abbildung 2: ein bedingter Zeile-Code-Haltepunkt"  
[ImageBreakpointsPanel]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-page-js-breakpoints-16-33.msft.png "Abbildung 3: der Abschnitt "Haltepunkte""  
[ImageDeactivatedBreakpoints]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-page-js-breakpoints-deactivate-breakpoints.msft.png "Abbildung 4: deaktivierte Haltepunkte im Bereich "Haltepunkte""  
[ImageDomChangeBreakpoint]: /microsoft-edge/devtools-guide-chromium/media/javascript-elements-break-on-subtree-modifications.msft.png "Abbildung 5: Kontextmenü zum Erstellen eines DOM-Änderungs Haltepunkts"  
[ImageXhrBreakpoint]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-page-js-xhr-fetch-breakpoints-org.msft.png "Abbildung 6: Erstellen eines XMLHttpRequest-Haltepunkts"  
[ImageEventListenerBreakpoint]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-page-js-event-listener-breakpoints-device-deviceorientation.msft.png "Abbildung 7: Erstellen eines Ereignis-Listener-Haltepunkts"  
[ImagePauseExceptionsHighlight]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-page-js-pause-on-exceptions.msft.png "Abbildung 8: Schaltfläche "auf Ausnahmen pausieren""  
[ImageUncaughtException]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-page-js-paused-on-exception.msft.png "Abbildung 9: angehalten für eine nicht abgefangene Ausnahme"  

<!-- links -->  

[DevtoolsJavascriptIndex]: index.md "Erste Schritte mit dem Debuggen von JavaScript in Microsoft Edge devtools"  

[MDNFetchApi]: https://developer.mozilla.org/docs/Web/API/Fetch_API "FETCH-API | MDN"  

> [!NOTE]
> <span data-ttu-id="dcd08-248">Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="dcd08-248">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="dcd08-249">Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/javascript/breakpoints) und wird von [Kayce Basken][KayceBasques] (Technical Writer, Chrome devtools & Lighthouse) erstellt.</span><span class="sxs-lookup"><span data-stu-id="dcd08-249">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/javascript/breakpoints) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools & Lighthouse\).</span></span>  
[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
<span data-ttu-id="dcd08-251">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="dcd08-251">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
