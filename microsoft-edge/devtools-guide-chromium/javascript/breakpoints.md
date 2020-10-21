---
description: Informieren Sie sich über alle Möglichkeiten, wie Sie Ihren Code in Microsoft Edge devtools anhalten können.
title: Anhalten des Codes mit Haltepunkten in Microsoft Edge devtools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/19/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: 98c0e42657d9b0900d3eaca8af69f1c17abfcf06
ms.sourcegitcommit: 99eee78698dc95b2a3fa638a5b063ef449899cda
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/20/2020
ms.locfileid: "11124810"
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

# <span data-ttu-id="32147-104">Anhalten des Codes mit Haltepunkten in Microsoft Edge devtools</span><span class="sxs-lookup"><span data-stu-id="32147-104">How to pause your code with breakpoints in Microsoft Edge DevTools</span></span>  

<span data-ttu-id="32147-105">Verwenden Sie Haltepunkte, um Ihren JavaScript-Code anzuhalten.</span><span class="sxs-lookup"><span data-stu-id="32147-105">Use breakpoints to pause your JavaScript code.</span></span>  <span data-ttu-id="32147-106">In diesem Leitfaden werden die einzelnen Typen von Haltepunkten erläutert, die in devtools zur Verfügung stehen, sowie Informationen dazu, wann und wie die einzelnen Typen festzulegen sind.</span><span class="sxs-lookup"><span data-stu-id="32147-106">This guide explains each type of breakpoint that is available in DevTools, as well as when to use and how to set each type.</span></span>  <span data-ttu-id="32147-107">Wenn Sie ein praktisches Lernprogramm für den Debuggingprozess durchführen möchten, navigieren Sie zu den [ersten Schritten beim Debuggen von JavaScript in Microsoft Edge devtools][DevtoolsJavascriptIndex].</span><span class="sxs-lookup"><span data-stu-id="32147-107">For a hands-on tutorial of the debugging process, navigate to [Get started with debugging JavaScript in Microsoft Edge DevTools][DevtoolsJavascriptIndex].</span></span>  

## <span data-ttu-id="32147-108">Übersicht über die Verwendung der einzelnen Haltepunkttypen</span><span class="sxs-lookup"><span data-stu-id="32147-108">Overview of when to use each breakpoint type</span></span>  

<span data-ttu-id="32147-109">Der bekannteste Breakpoint-Typ ist "Codezeile".</span><span class="sxs-lookup"><span data-stu-id="32147-109">The most well-known type of breakpoint is line-of-code.</span></span>  <span data-ttu-id="32147-110">Es ist jedoch möglich, dass die festgelegten Code Haltepunkte nicht besonders effizient sind, wenn Sie nicht genau wissen, wo Sie suchen müssen, oder wenn Sie mit einer umfangreichen CodeBase arbeiten.</span><span class="sxs-lookup"><span data-stu-id="32147-110">But line-of-code breakpoints may be inefficient to set, especially if you do not know exactly where to look, or if you are working with a large codebase.</span></span>  <span data-ttu-id="32147-111">Sie können beim Debuggen Zeit sparen, indem Sie wissen, wie und wann die anderen Arten von Haltepunkten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="32147-111">You may save yourself time when debugging by knowing how and when to use the other types of breakpoints.</span></span>  

| <span data-ttu-id="32147-112">Breakpoint-Typ</span><span class="sxs-lookup"><span data-stu-id="32147-112">Breakpoint Type</span></span> | <span data-ttu-id="32147-113">Verwenden Sie diese Taste, wenn Sie anhalten möchten...</span><span class="sxs-lookup"><span data-stu-id="32147-113">Use This When You Want To Pause...</span></span>  |  
|:--- |:--- |  
| [<span data-ttu-id="32147-114">Codezeile</span><span class="sxs-lookup"><span data-stu-id="32147-114">Line-of-code</span></span>](#line-of-code-breakpoints) | <span data-ttu-id="32147-115">In einem exakten Codebereich.</span><span class="sxs-lookup"><span data-stu-id="32147-115">On an exact region of code.</span></span>  |  
| [<span data-ttu-id="32147-116">Bedingte Codezeile</span><span class="sxs-lookup"><span data-stu-id="32147-116">Conditional line-of-code</span></span>](#conditional-line-of-code-breakpoints) | <span data-ttu-id="32147-117">In einem exakten Codebereich, aber nur, wenn eine andere Bedingung wahr ist.</span><span class="sxs-lookup"><span data-stu-id="32147-117">On an exact region of code, but only when some other condition is true.</span></span>  |  
| [<span data-ttu-id="32147-118">DOM</span><span class="sxs-lookup"><span data-stu-id="32147-118">DOM</span></span>](#dom-change-breakpoints) | <span data-ttu-id="32147-119">Auf dem Code, der einen bestimmten DOM-Knoten ändert oder entfernt, oder die untergeordneten Elemente.</span><span class="sxs-lookup"><span data-stu-id="32147-119">On the code that changes or removes a specific DOM node, or the children.</span></span>  |  
| [<span data-ttu-id="32147-120">XMLHttpRequest</span><span class="sxs-lookup"><span data-stu-id="32147-120">XHR</span></span>](#xhrfetch-breakpoints) | <span data-ttu-id="32147-121">Wenn eine XMLHttpRequest-URL ein Zeichenfolgenmuster enthält.</span><span class="sxs-lookup"><span data-stu-id="32147-121">When an XHR URL contains a string pattern.</span></span>  |  
| [<span data-ttu-id="32147-122">Ereignis-Listener</span><span class="sxs-lookup"><span data-stu-id="32147-122">Event listener</span></span>](#event-listener-breakpoints) | <span data-ttu-id="32147-123">Auf dem Code, der nach einem Ereignis ausgeführt wird, beispielsweise `click` , wird ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="32147-123">On the code that runs after an event, such as `click`, runs.</span></span>  |  
| [<span data-ttu-id="32147-124">Ausnahme</span><span class="sxs-lookup"><span data-stu-id="32147-124">Exception</span></span>](#exception-breakpoints) | <span data-ttu-id="32147-125">In der Codezeile, die eine abgefangene oder nicht abgefangene Ausnahme auslöst.</span><span class="sxs-lookup"><span data-stu-id="32147-125">On the line of code that is throwing a caught or uncaught exception.</span></span>  |  
| [<span data-ttu-id="32147-126">Funktion</span><span class="sxs-lookup"><span data-stu-id="32147-126">Function</span></span>](#function-breakpoints) | <span data-ttu-id="32147-127">Jedes Mal, wenn ein bestimmter Befehl, eine bestimmte Funktion oder Methode ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="32147-127">Whenever a specific command, function, or method is run.</span></span>  |  

## <span data-ttu-id="32147-128">Haltepunkte für die Code Zeile</span><span class="sxs-lookup"><span data-stu-id="32147-128">Line-of-code breakpoints</span></span>  

<span data-ttu-id="32147-129">Verwenden Sie einen Haltepunkt für die Codezeile, wenn Sie den genauen Codebereich kennen, den Sie untersuchen müssen.</span><span class="sxs-lookup"><span data-stu-id="32147-129">Use a line-of-code breakpoint when you know the exact region of code that you need to investigate.</span></span>  <span data-ttu-id="32147-130">DevTools wird immer angehalten, bevor diese Codezeile ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="32147-130">DevTools always pauses before this line of code is run.</span></span>  

<span data-ttu-id="32147-131">So setzen Sie einen Code Haltepunkt in devtools:</span><span class="sxs-lookup"><span data-stu-id="32147-131">To set a line-of-code breakpoint in DevTools:</span></span>  

1.  <span data-ttu-id="32147-132">Klicken Sie auf die Registerkarte **Quellen** .</span><span class="sxs-lookup"><span data-stu-id="32147-132">Click the **Sources** tab.</span></span>  
1.  <span data-ttu-id="32147-133">Öffnen Sie die Datei, die die Codezeile enthält, für die Sie eine Unterbrechung durchführen möchten.</span><span class="sxs-lookup"><span data-stu-id="32147-133">Open the file containing the line of code on which you want to break.</span></span>  
1.  <span data-ttu-id="32147-134">Wechseln Sie zur Codezeile.</span><span class="sxs-lookup"><span data-stu-id="32147-134">Go the line of code.</span></span>  
1.  <span data-ttu-id="32147-135">Links neben der Codezeile befindet sich die Spalte "Zeile".</span><span class="sxs-lookup"><span data-stu-id="32147-135">To the left of the line of code is the line number column.</span></span>  <span data-ttu-id="32147-136">Klicken Sie darauf.</span><span class="sxs-lookup"><span data-stu-id="32147-136">Click on it.</span></span>  <span data-ttu-id="32147-137">Neben der Spalte "Zeile Nummer" wird ein rotes Symbol angezeigt.</span><span class="sxs-lookup"><span data-stu-id="32147-137">A red icon appears next to the line number column.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-page-js-breakpoint-30.msft.png" alt-text="Ein Haltepunkt für eine Codezeile" lightbox="../media/javascript-sources-page-js-breakpoint-30.msft.png":::
       <span data-ttu-id="32147-139">Ein Haltepunkt für eine Codezeile</span><span class="sxs-lookup"><span data-stu-id="32147-139">A line-of-code breakpoint</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="32147-140">Haltepunkte für die Code Zeile im Code</span><span class="sxs-lookup"><span data-stu-id="32147-140">Line-of-code breakpoints in your code</span></span>  

<span data-ttu-id="32147-141">Führen `debugger` Sie die Methode aus dem Code aus, um in dieser Zeile anzuhalten.</span><span class="sxs-lookup"><span data-stu-id="32147-141">Run the `debugger` method from your code to pause on that line.</span></span>  <span data-ttu-id="32147-142">Dies entspricht einem [Zeile-zu-Code-Haltepunkt](#line-of-code-breakpoints), mit der Ausnahme, dass der Haltepunkt im Code festgesetzt wird, nicht auf der devtools-Benutzeroberfläche.</span><span class="sxs-lookup"><span data-stu-id="32147-142">This is equivalent to a [line-of-code breakpoint](#line-of-code-breakpoints), except that the breakpoint is set in your code, not in the DevTools UI.</span></span>  

```javascript
console.log('a');
console.log('b');
debugger;
console.log('c');
```  

### <span data-ttu-id="32147-143">Bedingte Zeile-für-Code-Haltepunkte</span><span class="sxs-lookup"><span data-stu-id="32147-143">Conditional line-of-code breakpoints</span></span>  

<span data-ttu-id="32147-144">Verwenden Sie einen bedingten Code Haltepunkt, wenn Sie den genauen Codebereich kennen, den Sie untersuchen müssen, aber nur anhalten möchten, wenn eine andere Bedingung wahr ist.</span><span class="sxs-lookup"><span data-stu-id="32147-144">Use a conditional line-of-code breakpoint when you know the exact region of code that you need to investigate, but you want to pause only when some other condition is true.</span></span>  

<span data-ttu-id="32147-145">So setzen Sie einen bedingten Haltepunkt für eine bedingte Codezeile:</span><span class="sxs-lookup"><span data-stu-id="32147-145">To set a conditional line-of-code breakpoint:</span></span>  

1.  <span data-ttu-id="32147-146">Klicken Sie auf die Registerkarte **Quellen** .</span><span class="sxs-lookup"><span data-stu-id="32147-146">Click the **Sources** tab.</span></span>  
1.  <span data-ttu-id="32147-147">Öffnen Sie die Datei, die die Codezeile enthält, für die Sie eine Unterbrechung durchführen möchten.</span><span class="sxs-lookup"><span data-stu-id="32147-147">Open the file containing the line of code on which you want to break.</span></span>  
1.  <span data-ttu-id="32147-148">Wechseln Sie zur Codezeile.</span><span class="sxs-lookup"><span data-stu-id="32147-148">Go the line of code.</span></span>  
1.  <span data-ttu-id="32147-149">Links neben der Codezeile befindet sich die Spalte "Zeile".</span><span class="sxs-lookup"><span data-stu-id="32147-149">To the left of the line of code is the line number column.</span></span>  <span data-ttu-id="32147-150">Klicken Sie mit der rechten Maustaste auf die Leitungsnummer.</span><span class="sxs-lookup"><span data-stu-id="32147-150">Right-click the line number.</span></span>  
1.  <span data-ttu-id="32147-151">Wählen Sie **bedingter Haltepunkt hinzufügen**aus.</span><span class="sxs-lookup"><span data-stu-id="32147-151">Choose **Add conditional breakpoint**.</span></span>  <span data-ttu-id="32147-152">Unterhalb der Codezeile wird ein Dialogfeld angezeigt.</span><span class="sxs-lookup"><span data-stu-id="32147-152">A dialog displays underneath the line of code.</span></span>  
1.  <span data-ttu-id="32147-153">Geben Sie Ihre Bedingung in das Dialogfeld ein.</span><span class="sxs-lookup"><span data-stu-id="32147-153">Enter your condition in the dialog.</span></span>  
1.  <span data-ttu-id="32147-154">Wählen Sie aus `Enter` , um den Haltepunkt zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="32147-154">Select `Enter` to activate the breakpoint.</span></span>  <span data-ttu-id="32147-155">Ein Symbol neben der Spalte "Zeile"</span><span class="sxs-lookup"><span data-stu-id="32147-155">An icon next to the line number column.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-page-js-conditional-breakpoint.msft.png" alt-text="Ein Haltepunkt für eine Codezeile" lightbox="../media/javascript-sources-page-js-conditional-breakpoint.msft.png":::
       <span data-ttu-id="32147-157">Ein bedingter Zeile-Code-Haltepunkt</span><span class="sxs-lookup"><span data-stu-id="32147-157">A conditional line-of-code breakpoint</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="32147-158">Verwalten von Code Haltepunkten</span><span class="sxs-lookup"><span data-stu-id="32147-158">Manage line-of-code breakpoints</span></span>  

<span data-ttu-id="32147-159">Verwenden Sie den Bereich **Haltepunkte** , um Code Haltepunkte an einer einzelnen Position zu deaktivieren oder zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="32147-159">Use the **Breakpoints** pane to disable or remove line-of-code breakpoints from a single location.</span></span>  

:::image type="complex" source="../media/javascript-sources-page-js-breakpoints-16-33.msft.png" alt-text="Ein Haltepunkt für eine Codezeile" lightbox="../media/javascript-sources-page-js-breakpoints-16-33.msft.png":::
   <span data-ttu-id="32147-161">Der **Haltepunkt** -Panel</span><span class="sxs-lookup"><span data-stu-id="32147-161">The **Breakpoints** panel</span></span>  
:::image-end:::  

*   <span data-ttu-id="32147-162">Aktivieren Sie das Kontrollkästchen neben einem Eintrag, um diesen Haltepunkt zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="32147-162">Check the checkbox next to an entry to disable that breakpoint.</span></span>  
*   <span data-ttu-id="32147-163">Klicken Sie mit der rechten Maustaste auf einen Eintrag, um diesen Haltepunkt zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="32147-163">Right-click an entry to remove that breakpoint.</span></span>  
*   <span data-ttu-id="32147-164">Klicken Sie mit der rechten Maustaste auf eine beliebige Stelle im Bereich **Haltepunkte** , um alle Haltepunkte zu deaktivieren, alle Haltepunkte zu deaktivieren oder alle Haltepunkte zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="32147-164">Right-click anywhere in the **Breakpoints** pane to deactivate all breakpoints, disable all breakpoints, or remove all breakpoints.</span></span>  <span data-ttu-id="32147-165">Das Deaktivieren aller Haltepunkte entspricht der Deaktivierung der einzelnen Haltepunkte.</span><span class="sxs-lookup"><span data-stu-id="32147-165">Disabling all breakpoints is equivalent to unchecking each one.</span></span>  <span data-ttu-id="32147-166">Durch die Deaktivierung aller Haltepunkte wird devtools angewiesen, alle Zeile-zu-Code-Haltepunkte zu ignorieren, aber auch den aktivierten Zustand beizubehalten, damit sich jeder in demselben Zustand wie zuvor befindet, wenn Sie ihn wieder aktivieren.</span><span class="sxs-lookup"><span data-stu-id="32147-166">Deactivating all breakpoints instructs DevTools to ignore all line-of-code breakpoints, but to also maintain the enabled state so that each are in the same state as before when you reactivate each one.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-page-js-breakpoints-deactivate-breakpoints.msft.png" alt-text="Ein Haltepunkt für eine Codezeile" lightbox="../media/javascript-sources-page-js-breakpoints-deactivate-breakpoints.msft.png":::
       <span data-ttu-id="32147-168">Deaktivierte Haltepunkte im Bereich " **Haltepunkte** "</span><span class="sxs-lookup"><span data-stu-id="32147-168">Deactivated breakpoints in the **Breakpoints** pane</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="32147-169">Dom-Änderungs Haltepunkte</span><span class="sxs-lookup"><span data-stu-id="32147-169">DOM change breakpoints</span></span>  

<span data-ttu-id="32147-170">Verwenden Sie einen Dom-Änderungs Haltepunkt, wenn Sie den Code anhalten möchten, durch den ein DOM-Knoten oder die untergeordneten Elemente geändert werden.</span><span class="sxs-lookup"><span data-stu-id="32147-170">Use a DOM change breakpoint when you want to pause on the code that changes a DOM node or the children.</span></span>  

<span data-ttu-id="32147-171">So setzen Sie einen Dom-Änderungs Haltepunkt:</span><span class="sxs-lookup"><span data-stu-id="32147-171">To set a DOM change breakpoint:</span></span>  

1.  <span data-ttu-id="32147-172">Klicken Sie auf die Registerkarte **Elemente** .</span><span class="sxs-lookup"><span data-stu-id="32147-172">Click the **Elements** tab.</span></span>  
1.  <span data-ttu-id="32147-173">Wechseln Sie zu dem Element, für das Sie den Haltepunkt festlegen möchten.</span><span class="sxs-lookup"><span data-stu-id="32147-173">Go the element on which you want to set the breakpoint.</span></span>  
1.  <span data-ttu-id="32147-174">Klicken Sie mit der rechten Maustaste auf das Element.</span><span class="sxs-lookup"><span data-stu-id="32147-174">Right-click the element.</span></span>  
1.  <span data-ttu-id="32147-175">Zeigen Sie **mit der Maus auf Umbruch**, und wählen Sie dann **Strukturänderungen**, **Attributänderungen**oder **Knoten Entfernung**aus.</span><span class="sxs-lookup"><span data-stu-id="32147-175">Hover over **Break on**, then choose **Subtree modifications**, **Attribute modifications**, or **Node removal**.</span></span>  
    
    :::image type="complex" source="../media/javascript-elements-break-on-subtree-modifications.msft.png" alt-text="Ein Haltepunkt für eine Codezeile" lightbox="../media/javascript-elements-break-on-subtree-modifications.msft.png":::
       <span data-ttu-id="32147-177">Das Kontextmenü zum Erstellen eines DOM-Änderungs Haltepunkts</span><span class="sxs-lookup"><span data-stu-id="32147-177">The context menu for creating a DOM change breakpoint</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="32147-178">Typen von Dom-Änderungs Haltepunkten</span><span class="sxs-lookup"><span data-stu-id="32147-178">Types of DOM change breakpoints</span></span>  

*   <span data-ttu-id="32147-179">Teil **Strukturänderungen**.</span><span class="sxs-lookup"><span data-stu-id="32147-179">**Subtree modifications**.</span></span>  <span data-ttu-id="32147-180">Wird ausgelöst, wenn ein untergeordnetes Element des aktuell ausgewählten Knotens entfernt oder hinzugefügt oder der Inhalt eines untergeordneten Elements geändert wird.</span><span class="sxs-lookup"><span data-stu-id="32147-180">Triggered when a child of the currently-selected node is removed or added, or the contents of a child are changed.</span></span>  <span data-ttu-id="32147-181">Wird nicht für Änderungen an einem Attribut des untergeordneten Knotens oder für Änderungen am aktuell ausgewählten Knoten ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="32147-181">Not triggered on child node attribute changes, or on any changes to the currently-selected node.</span></span>  
*   <span data-ttu-id="32147-182">Attribut **Änderungen**: wird ausgelöst, wenn ein Attribut auf dem aktuell ausgewählten Knoten hinzugefügt oder entfernt wird oder wenn sich ein Attributwert ändert.</span><span class="sxs-lookup"><span data-stu-id="32147-182">**Attributes modifications**: Triggered when an attribute is added or removed on the currently-selected node, or when an attribute value changes.</span></span>  
*   <span data-ttu-id="32147-183">**Knoten Entfernung**: wird ausgelöst, wenn der aktuell ausgewählte Knoten entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="32147-183">**Node Removal**: Triggered when the currently-selected node is removed.</span></span>  
    
## <span data-ttu-id="32147-184">XMLHttpRequest/FETCH-Haltepunkte</span><span class="sxs-lookup"><span data-stu-id="32147-184">XHR/Fetch breakpoints</span></span>  

<span data-ttu-id="32147-185">Verwenden Sie einen XMLHttpRequest-Haltepunkt, wenn Sie unterbrechen möchten, wenn die Anforderungs-URL eines XMLHttpRequest eine angegebene Zeichenfolge enthält.</span><span class="sxs-lookup"><span data-stu-id="32147-185">Use an XHR breakpoint when you want to break when the request URL of an XHR contains a specified string.</span></span>  <span data-ttu-id="32147-186">DevTools wird in der Codezeile angehalten, in der die XMLHttpRequest die `send()` Methode ausführt.</span><span class="sxs-lookup"><span data-stu-id="32147-186">DevTools pauses on the line of code where the XHR runs the `send()` method.</span></span>  

> [!NOTE]
> <span data-ttu-id="32147-187">Dieses Feature funktioniert auch mit [Fetch-API-][MDNFetchApi] Anforderungen.</span><span class="sxs-lookup"><span data-stu-id="32147-187">This feature also works with [Fetch API][MDNFetchApi] requests.</span></span>  

<span data-ttu-id="32147-188">Wenn dies hilfreich ist, können Sie beispielsweise feststellen, dass die Seite eine falsche URL anfordert, und Sie möchten schnell den AJAX-oder Fetch-Quellcode finden, der die falsche Anforderung verursacht.</span><span class="sxs-lookup"><span data-stu-id="32147-188">One example of when this is helpful is when you see that your page is requesting an incorrect URL, and you want to quickly find the AJAX or Fetch source code that is causing the incorrect request.</span></span>  

<span data-ttu-id="32147-189">So setzen Sie einen XMLHttpRequest-Haltepunkt:</span><span class="sxs-lookup"><span data-stu-id="32147-189">To set an XHR breakpoint:</span></span>  

1.  <span data-ttu-id="32147-190">Klicken Sie auf die Registerkarte **Quellen** .</span><span class="sxs-lookup"><span data-stu-id="32147-190">Click the **Sources** tab.</span></span>  
1.  <span data-ttu-id="32147-191">Erweitern Sie den Bereich **XMLHttpRequest-Haltepunkte** .</span><span class="sxs-lookup"><span data-stu-id="32147-191">Expand the **XHR Breakpoints** pane.</span></span>  
1.  <span data-ttu-id="32147-192">Wählen Sie **Haltepunkt hinzufügen**aus.</span><span class="sxs-lookup"><span data-stu-id="32147-192">Choose **Add breakpoint**.</span></span>  
1.  <span data-ttu-id="32147-193">Geben Sie die Zeichenfolge ein, die Sie aufheben möchten.</span><span class="sxs-lookup"><span data-stu-id="32147-193">Enter the string which you want to break on.</span></span>  <span data-ttu-id="32147-194">DevTools wird angehalten, wenn diese Zeichenfolge an einer beliebigen Stelle in einer XMLHttpRequest-Anforderungs-URL vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="32147-194">DevTools pauses when this string is present anywhere in an XHR request URL.</span></span>  
1.  <span data-ttu-id="32147-195">Wählen Sie aus `Enter` , um zu bestätigen.</span><span class="sxs-lookup"><span data-stu-id="32147-195">Select `Enter` to confirm.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-page-js-xhr-fetch-breakpoints-org.msft.png" alt-text="Ein Haltepunkt für eine Codezeile" lightbox="../media/javascript-sources-page-js-xhr-fetch-breakpoints-org.msft.png":::
       <span data-ttu-id="32147-197">Erstellen eines XMLHttpRequest-Haltepunkts</span><span class="sxs-lookup"><span data-stu-id="32147-197">Create an XHR breakpoint</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="32147-198">Ereignis-Listener-Haltepunkte</span><span class="sxs-lookup"><span data-stu-id="32147-198">Event listener breakpoints</span></span>   

<span data-ttu-id="32147-199">Verwenden Sie Ereignis-Listener-Haltepunkte, wenn Sie den Ereignislistener-Code anhalten möchten, der nach dem Auslösen eines Ereignisses ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="32147-199">Use event listener breakpoints when you want to pause on the event listener code that runs after an event is fired.</span></span>  <span data-ttu-id="32147-200">Sie können bestimmte Ereignisse, beispielsweise `click` oder Kategorien von Ereignissen, wie alle Mausereignisse auswählen.</span><span class="sxs-lookup"><span data-stu-id="32147-200">You are able to select specific events, such as `click`, or categories of events, such as all mouse events.</span></span>  

1.  <span data-ttu-id="32147-201">Klicken Sie auf die Registerkarte **Quellen** .</span><span class="sxs-lookup"><span data-stu-id="32147-201">Click the **Sources** tab.</span></span>  
1.  <span data-ttu-id="32147-202">Erweitern Sie den Bereich **Ereignislistener-Haltepunkte** .</span><span class="sxs-lookup"><span data-stu-id="32147-202">Expand the **Event Listener Breakpoints** pane.</span></span>  <span data-ttu-id="32147-203">DevTools zeigt eine Liste der Ereigniskategorien, wie etwa **Animationen**, an.</span><span class="sxs-lookup"><span data-stu-id="32147-203">DevTools shows a list of event categories, such as **Animation**.</span></span>  
1.  <span data-ttu-id="32147-204">Überprüfen Sie eine dieser Kategorien, um zu pausieren, wenn ein Ereignis aus dieser Kategorie ausgelöst wird, oder erweitern Sie die Kategorie, und überprüfen Sie ein bestimmtes Ereignis.</span><span class="sxs-lookup"><span data-stu-id="32147-204">Check one of these categories to pause whenever any event from that category is fired, or expand the category and check a specific event.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-page-js-event-listener-breakpoints-device-deviceorientation.msft.png" alt-text="Ein Haltepunkt für eine Codezeile" lightbox="../media/javascript-sources-page-js-event-listener-breakpoints-device-deviceorientation.msft.png":::
       <span data-ttu-id="32147-206">Erstellen eines Ereignis-Listener-Haltepunkts</span><span class="sxs-lookup"><span data-stu-id="32147-206">Create an event listener breakpoint</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="32147-207">Ausnahme Haltepunkte</span><span class="sxs-lookup"><span data-stu-id="32147-207">Exception breakpoints</span></span>  

<span data-ttu-id="32147-208">Verwenden Sie Ausnahme Haltepunkte, wenn Sie in der Codezeile anhalten möchten, die eine abgefangene oder nicht abgefangene Ausnahme auslöst.</span><span class="sxs-lookup"><span data-stu-id="32147-208">Use exception breakpoints when you want to pause on the line of code that is throwing a caught or uncaught exception.</span></span>  

1.  <span data-ttu-id="32147-209">Klicken Sie auf die Registerkarte **Quellen** .</span><span class="sxs-lookup"><span data-stu-id="32147-209">Click the **Sources** tab.</span></span>  
1.  <span data-ttu-id="32147-210">Wählen Sie **bei Ausnahmen anhalten** \ ( ![ bei Ausnahmen anhalten ][ImagePauseOnExceptionsIcon] \) aus.</span><span class="sxs-lookup"><span data-stu-id="32147-210">Choose **Pause on exceptions** \(![Pause on exceptions][ImagePauseOnExceptionsIcon]\).</span></span>  <span data-ttu-id="32147-211">Das Symbol wird blau, wenn es aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="32147-211">The icon turns blue when enabled.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-page-js-pause-on-exceptions.msft.png" alt-text="Ein Haltepunkt für eine Codezeile" lightbox="../media/javascript-sources-page-js-pause-on-exceptions.msft.png":::
       <span data-ttu-id="32147-213">Schaltfläche " **auf Ausnahmen pausieren** "</span><span class="sxs-lookup"><span data-stu-id="32147-213">The **Pause on exceptions** button</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="32147-214">**Optional**.</span><span class="sxs-lookup"><span data-stu-id="32147-214">**Optional**.</span></span>  <span data-ttu-id="32147-215">Aktivieren Sie das Kontrollkästchen **auf abgefangene Ausnahmen anhalten** , wenn Sie zusätzlich zu den nicht abgefangenen Ausnahmen auch auf abgefangene Ausnahmen anhalten möchten.</span><span class="sxs-lookup"><span data-stu-id="32147-215">Check the **Pause On Caught Exceptions** checkbox if you also want to pause on caught exceptions, in addition to uncaught ones.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-page-js-paused-on-exception.msft.png" alt-text="Ein Haltepunkt für eine Codezeile" lightbox="../media/javascript-sources-page-js-paused-on-exception.msft.png":::
       <span data-ttu-id="32147-217">Bei einer nicht abgefangenen Ausnahme angehalten</span><span class="sxs-lookup"><span data-stu-id="32147-217">Paused on an uncaught exception</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="32147-218">Funktionshaltepunkte</span><span class="sxs-lookup"><span data-stu-id="32147-218">Function breakpoints</span></span>  

<span data-ttu-id="32147-219">Führen Sie die Methode aus, `debug(method)` wobei `method` der Befehl, die Funktion oder die Methode, die Sie debuggen möchten, ist, wenn Sie anhalten möchten, wenn eine bestimmte Funktion ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="32147-219">Run the `debug(method)` method, where `method` is the command, function, or method you want to debug, when you want to pause whenever a specific function is run.</span></span>  <span data-ttu-id="32147-220">Sie können `debug()` in Ihren Code einfügen (wie eine `console.log()` Anweisung) oder die Methode über die devtools-Konsole ausführen.</span><span class="sxs-lookup"><span data-stu-id="32147-220">You may insert `debug()` into your code (like a `console.log()` statement) or run the method from the DevTools Console.</span></span>  `debug()` <span data-ttu-id="32147-221">entspricht dem Festlegen eines [Haltepunkts für die Code Zeile](#line-of-code-breakpoints) in der ersten Zeile der Funktion.</span><span class="sxs-lookup"><span data-stu-id="32147-221">is equivalent to setting a [line-of-code breakpoint](#line-of-code-breakpoints) on the first line of the function.</span></span>  

```javascript
function sum(a, b) {
    let result = a + b; // DevTools pauses on this line.
    return result;
}
debug(sum); // Pass the function object, not a string.
sum();
```  

### <span data-ttu-id="32147-222">Sicherstellen, dass sich die Zielfunktion im Bereich befindet</span><span class="sxs-lookup"><span data-stu-id="32147-222">Make sure the target function is in scope</span></span>  

<span data-ttu-id="32147-223">DevTools löst a `ReferenceError` aus, wenn sich die zu debuggende Funktion nicht im Bereich befindet.</span><span class="sxs-lookup"><span data-stu-id="32147-223">DevTools throws a `ReferenceError` if the function you want to debug is not in scope.</span></span>  

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

<span data-ttu-id="32147-224">Die Sicherstellung, dass die Zielfunktion im Bereich liegt, ist schwierig, wenn Sie die `debug()` Methode über die devtools-Konsole ausführen.</span><span class="sxs-lookup"><span data-stu-id="32147-224">Ensuring the target function is in scope is tricky if you are running the `debug()` method from the DevTools Console.</span></span>  <span data-ttu-id="32147-225">Hier ist eine Strategie:</span><span class="sxs-lookup"><span data-stu-id="32147-225">Here is one strategy:</span></span>  

1.  <span data-ttu-id="32147-226">Setzen Sie einen [Haltepunkt für die Codezeile](#line-of-code-breakpoints) an einer beliebigen Stelle, an der sich die Funktion im Bereich befindet.</span><span class="sxs-lookup"><span data-stu-id="32147-226">Set a [line-of-code breakpoint](#line-of-code-breakpoints) somewhere where the function is in scope.</span></span>
1.  <span data-ttu-id="32147-227">Auslösen des Haltepunkts</span><span class="sxs-lookup"><span data-stu-id="32147-227">Trigger the breakpoint.</span></span>  
1.  <span data-ttu-id="32147-228">Führen `debug()` Sie die Methode in der devtools-Konsole aus, während der Code weiterhin auf dem Haltepunkt für die Code Zeile angehalten wird.</span><span class="sxs-lookup"><span data-stu-id="32147-228">Run the `debug()` method in the DevTools Console while the code is still paused on your line-of-code breakpoint.</span></span>  
    
## <span data-ttu-id="32147-229">Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen</span><span class="sxs-lookup"><span data-stu-id="32147-229">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImagePauseOnExceptionsIcon]: ../media/pause-on-exceptions-icon.msft.png  

<!-- links -->  

[DevtoolsJavascriptIndex]: index.md "Erste Schritte mit dem Debuggen von JavaScript in Microsoft Edge devtools | Microsoft docs"  

[MDNFetchApi]: https://developer.mozilla.org/docs/Web/API/Fetch_API "FETCH-API | MDN"  

> [!NOTE]
> <span data-ttu-id="32147-232">Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="32147-232">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="32147-233">Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/javascript/breakpoints) und wird von [Kayce Basken][KayceBasques] (Technical Writer, Chrome devtools \ & Lighthouse \) erstellt.</span><span class="sxs-lookup"><span data-stu-id="32147-233">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/javascript/breakpoints) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
<span data-ttu-id="32147-235">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="32147-235">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
