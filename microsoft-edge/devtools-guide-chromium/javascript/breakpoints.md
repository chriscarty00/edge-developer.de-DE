---
title: Anhalten des Codes mit Haltepunkten in Microsoft Edge devtools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: 804e864ee3029a49ba1ef2ac1f2deb61c3ba5ec3
ms.sourcegitcommit: 1251c555c6b4db8ef8187ed94d8832fdb89d03b8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/31/2020
ms.locfileid: "10983196"
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







# <span data-ttu-id="4f1f9-103">Anhalten des Codes mit Haltepunkten in Microsoft Edge devtools</span><span class="sxs-lookup"><span data-stu-id="4f1f9-103">How to pause your code with breakpoints in Microsoft Edge DevTools</span></span>   



<span data-ttu-id="4f1f9-104">Verwenden Sie Haltepunkte, um Ihren JavaScript-Code anzuhalten.</span><span class="sxs-lookup"><span data-stu-id="4f1f9-104">Use breakpoints to pause your JavaScript code.</span></span>  <span data-ttu-id="4f1f9-105">In diesem Leitfaden werden die einzelnen Typen von Haltepunkten erläutert, die in devtools zur Verfügung stehen, sowie Informationen dazu, wann und wie die einzelnen Typen festzulegen sind.</span><span class="sxs-lookup"><span data-stu-id="4f1f9-105">This guide explains each type of breakpoint that is available in DevTools, as well as when to use and how to set each type.</span></span>  <span data-ttu-id="4f1f9-106">Eine praktische Einführung in den Debuggingprozess finden Sie unter [Erste Schritte mit dem Debuggen von JavaScript in Microsoft Edge devtools][DevtoolsJavascriptIndex].</span><span class="sxs-lookup"><span data-stu-id="4f1f9-106">For a hands-on tutorial of the debugging process, see [Get started with debugging JavaScript in Microsoft Edge DevTools][DevtoolsJavascriptIndex].</span></span>  

## <span data-ttu-id="4f1f9-107">Übersicht über die Verwendung der einzelnen Haltepunkttypen</span><span class="sxs-lookup"><span data-stu-id="4f1f9-107">Overview of when to use each breakpoint type</span></span>   

<span data-ttu-id="4f1f9-108">Der bekannteste Breakpoint-Typ ist "Codezeile".</span><span class="sxs-lookup"><span data-stu-id="4f1f9-108">The most well-known type of breakpoint is line-of-code.</span></span>  <span data-ttu-id="4f1f9-109">Es ist jedoch möglich, dass die festgelegten Code Haltepunkte nicht besonders effizient sind, wenn Sie nicht genau wissen, wo Sie suchen müssen, oder wenn Sie mit einer umfangreichen CodeBase arbeiten.</span><span class="sxs-lookup"><span data-stu-id="4f1f9-109">But line-of-code breakpoints may be inefficient to set, especially if you do not know exactly where to look, or if you are working with a large codebase.</span></span>  <span data-ttu-id="4f1f9-110">Sie können beim Debuggen Zeit sparen, indem Sie wissen, wie und wann die anderen Arten von Haltepunkten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4f1f9-110">You may save yourself time when debugging by knowing how and when to use the other types of breakpoints.</span></span>  

| <span data-ttu-id="4f1f9-111">Breakpoint-Typ</span><span class="sxs-lookup"><span data-stu-id="4f1f9-111">Breakpoint Type</span></span> | <span data-ttu-id="4f1f9-112">Verwenden Sie diese Taste, wenn Sie anhalten möchten...</span><span class="sxs-lookup"><span data-stu-id="4f1f9-112">Use This When You Want To Pause...</span></span>  |  
|:--- |:--- |  
| [<span data-ttu-id="4f1f9-113">Codezeile</span><span class="sxs-lookup"><span data-stu-id="4f1f9-113">Line-of-code</span></span>](#line-of-code-breakpoints) | <span data-ttu-id="4f1f9-114">In einem exakten Codebereich.</span><span class="sxs-lookup"><span data-stu-id="4f1f9-114">On an exact region of code.</span></span>  |  
| [<span data-ttu-id="4f1f9-115">Bedingte Codezeile</span><span class="sxs-lookup"><span data-stu-id="4f1f9-115">Conditional line-of-code</span></span>](#conditional-line-of-code-breakpoints) | <span data-ttu-id="4f1f9-116">In einem exakten Codebereich, aber nur, wenn eine andere Bedingung wahr ist.</span><span class="sxs-lookup"><span data-stu-id="4f1f9-116">On an exact region of code, but only when some other condition is true.</span></span>  |  
| [<span data-ttu-id="4f1f9-117">DOM</span><span class="sxs-lookup"><span data-stu-id="4f1f9-117">DOM</span></span>](#dom-change-breakpoints) | <span data-ttu-id="4f1f9-118">Auf dem Code, der einen bestimmten DOM-Knoten ändert oder entfernt, oder die untergeordneten Elemente.</span><span class="sxs-lookup"><span data-stu-id="4f1f9-118">On the code that changes or removes a specific DOM node, or the children.</span></span>  |  
| [<span data-ttu-id="4f1f9-119">XMLHttpRequest</span><span class="sxs-lookup"><span data-stu-id="4f1f9-119">XHR</span></span>](#xhrfetch-breakpoints) | <span data-ttu-id="4f1f9-120">Wenn eine XMLHttpRequest-URL ein Zeichenfolgenmuster enthält.</span><span class="sxs-lookup"><span data-stu-id="4f1f9-120">When an XHR URL contains a string pattern.</span></span>  |  
| [<span data-ttu-id="4f1f9-121">Ereignis-Listener</span><span class="sxs-lookup"><span data-stu-id="4f1f9-121">Event listener</span></span>](#event-listener-breakpoints) | <span data-ttu-id="4f1f9-122">Auf dem Code, der nach einem Ereignis ausgeführt wird, beispielsweise `click` , wird ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4f1f9-122">On the code that runs after an event, such as `click`, runs.</span></span>  |  
| [<span data-ttu-id="4f1f9-123">Ausnahme</span><span class="sxs-lookup"><span data-stu-id="4f1f9-123">Exception</span></span>](#exception-breakpoints) | <span data-ttu-id="4f1f9-124">In der Codezeile, die eine abgefangene oder nicht abgefangene Ausnahme auslöst.</span><span class="sxs-lookup"><span data-stu-id="4f1f9-124">On the line of code that is throwing a caught or uncaught exception.</span></span>  |  
| [<span data-ttu-id="4f1f9-125">Funktion</span><span class="sxs-lookup"><span data-stu-id="4f1f9-125">Function</span></span>](#function-breakpoints) | <span data-ttu-id="4f1f9-126">Jedes Mal, wenn ein bestimmter Befehl, eine bestimmte Funktion oder Methode ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4f1f9-126">Whenever a specific command, function, or method is run.</span></span>  |  

## <span data-ttu-id="4f1f9-127">Haltepunkte für die Code Zeile</span><span class="sxs-lookup"><span data-stu-id="4f1f9-127">Line-of-code breakpoints</span></span>   

<span data-ttu-id="4f1f9-128">Verwenden Sie einen Haltepunkt für die Codezeile, wenn Sie den genauen Codebereich kennen, den Sie untersuchen müssen.</span><span class="sxs-lookup"><span data-stu-id="4f1f9-128">Use a line-of-code breakpoint when you know the exact region of code that you need to investigate.</span></span>  <span data-ttu-id="4f1f9-129">DevTools wird immer angehalten, bevor diese Codezeile ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4f1f9-129">DevTools always pauses before this line of code is run.</span></span>  

<span data-ttu-id="4f1f9-130">So setzen Sie einen Code Haltepunkt in devtools:</span><span class="sxs-lookup"><span data-stu-id="4f1f9-130">To set a line-of-code breakpoint in DevTools:</span></span>  

1.  <span data-ttu-id="4f1f9-131">Klicken Sie auf die Registerkarte **Quellen** .</span><span class="sxs-lookup"><span data-stu-id="4f1f9-131">Click the **Sources** tab.</span></span>  
1.  <span data-ttu-id="4f1f9-132">Öffnen Sie die Datei, die die Codezeile enthält, für die Sie eine Unterbrechung durchführen möchten.</span><span class="sxs-lookup"><span data-stu-id="4f1f9-132">Open the file containing the line of code on which you want to break.</span></span>  
1.  <span data-ttu-id="4f1f9-133">Wechseln Sie zur Codezeile.</span><span class="sxs-lookup"><span data-stu-id="4f1f9-133">Go the line of code.</span></span>  
1.  <span data-ttu-id="4f1f9-134">Links neben der Codezeile befindet sich die Spalte "Zeile".</span><span class="sxs-lookup"><span data-stu-id="4f1f9-134">To the left of the line of code is the line number column.</span></span>  <span data-ttu-id="4f1f9-135">Klicken Sie darauf.</span><span class="sxs-lookup"><span data-stu-id="4f1f9-135">Click on it.</span></span>  <span data-ttu-id="4f1f9-136">Neben der Spalte "Zeile Nummer" wird ein rotes Symbol angezeigt.</span><span class="sxs-lookup"><span data-stu-id="4f1f9-136">A red icon appears next to the line number column.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-page-js-breakpoint-30.msft.png" alt-text="Ein Haltepunkt für eine Codezeile" lightbox="../media/javascript-sources-page-js-breakpoint-30.msft.png":::
       <span data-ttu-id="4f1f9-138">Ein Haltepunkt für eine Codezeile</span><span class="sxs-lookup"><span data-stu-id="4f1f9-138">A line-of-code breakpoint</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="4f1f9-139">Haltepunkte für die Code Zeile im Code</span><span class="sxs-lookup"><span data-stu-id="4f1f9-139">Line-of-code breakpoints in your code</span></span>   

<span data-ttu-id="4f1f9-140">Führen `debugger` Sie die Methode aus dem Code aus, um in dieser Zeile anzuhalten.</span><span class="sxs-lookup"><span data-stu-id="4f1f9-140">Run the `debugger` method from your code to pause on that line.</span></span>  <span data-ttu-id="4f1f9-141">Dies entspricht einem [Zeile-zu-Code-Haltepunkt](#line-of-code-breakpoints), mit der Ausnahme, dass der Haltepunkt im Code festgesetzt wird, nicht auf der devtools-Benutzeroberfläche.</span><span class="sxs-lookup"><span data-stu-id="4f1f9-141">This is equivalent to a [line-of-code breakpoint](#line-of-code-breakpoints), except that the breakpoint is set in your code, not in the DevTools UI.</span></span>  

```javascript
console.log('a');
console.log('b');
debugger;
console.log('c');
```  

### <span data-ttu-id="4f1f9-142">Bedingte Zeile-für-Code-Haltepunkte</span><span class="sxs-lookup"><span data-stu-id="4f1f9-142">Conditional line-of-code breakpoints</span></span>   

<span data-ttu-id="4f1f9-143">Verwenden Sie einen bedingten Code Haltepunkt, wenn Sie den genauen Codebereich kennen, den Sie untersuchen müssen, aber nur anhalten möchten, wenn eine andere Bedingung wahr ist.</span><span class="sxs-lookup"><span data-stu-id="4f1f9-143">Use a conditional line-of-code breakpoint when you know the exact region of code that you need to investigate, but you want to pause only when some other condition is true.</span></span>  

<span data-ttu-id="4f1f9-144">So setzen Sie einen bedingten Haltepunkt für eine bedingte Codezeile:</span><span class="sxs-lookup"><span data-stu-id="4f1f9-144">To set a conditional line-of-code breakpoint:</span></span>  

1.  <span data-ttu-id="4f1f9-145">Klicken Sie auf die Registerkarte **Quellen** .</span><span class="sxs-lookup"><span data-stu-id="4f1f9-145">Click the **Sources** tab.</span></span>  
1.  <span data-ttu-id="4f1f9-146">Öffnen Sie die Datei, die die Codezeile enthält, für die Sie eine Unterbrechung durchführen möchten.</span><span class="sxs-lookup"><span data-stu-id="4f1f9-146">Open the file containing the line of code on which you want to break.</span></span>  
1.  <span data-ttu-id="4f1f9-147">Wechseln Sie zur Codezeile.</span><span class="sxs-lookup"><span data-stu-id="4f1f9-147">Go the line of code.</span></span>  
1.  <span data-ttu-id="4f1f9-148">Links neben der Codezeile befindet sich die Spalte "Zeile".</span><span class="sxs-lookup"><span data-stu-id="4f1f9-148">To the left of the line of code is the line number column.</span></span>  <span data-ttu-id="4f1f9-149">Klicken Sie mit der rechten Maustaste auf die Leitungsnummer.</span><span class="sxs-lookup"><span data-stu-id="4f1f9-149">Right-click the line number.</span></span>  
1.  <span data-ttu-id="4f1f9-150">Wählen Sie **bedingter Haltepunkt hinzufügen**aus.</span><span class="sxs-lookup"><span data-stu-id="4f1f9-150">Select **Add conditional breakpoint**.</span></span>  <span data-ttu-id="4f1f9-151">Unterhalb der Codezeile wird ein Dialogfeld angezeigt.</span><span class="sxs-lookup"><span data-stu-id="4f1f9-151">A dialog displays underneath the line of code.</span></span>  
1.  <span data-ttu-id="4f1f9-152">Geben Sie Ihre Bedingung in das Dialogfeld ein.</span><span class="sxs-lookup"><span data-stu-id="4f1f9-152">Enter your condition in the dialog.</span></span>  
1.  <span data-ttu-id="4f1f9-153">Drücken Sie `Enter` , um den Haltepunkt zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="4f1f9-153">Press `Enter` to activate the breakpoint.</span></span>  <span data-ttu-id="4f1f9-154">Ein Symbol neben der Spalte "Zeile"</span><span class="sxs-lookup"><span data-stu-id="4f1f9-154">An icon next to the line number column.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-page-js-conditional-breakpoint.msft.png" alt-text="Ein bedingter Zeile-Code-Haltepunkt" lightbox="../media/javascript-sources-page-js-conditional-breakpoint.msft.png":::
       <span data-ttu-id="4f1f9-156">Ein bedingter Zeile-Code-Haltepunkt</span><span class="sxs-lookup"><span data-stu-id="4f1f9-156">A conditional line-of-code breakpoint</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="4f1f9-157">Verwalten von Code Haltepunkten</span><span class="sxs-lookup"><span data-stu-id="4f1f9-157">Manage line-of-code breakpoints</span></span>   

<span data-ttu-id="4f1f9-158">Verwenden Sie den Bereich **Haltepunkte** , um Code Haltepunkte an einer einzelnen Position zu deaktivieren oder zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="4f1f9-158">Use the **Breakpoints** pane to disable or remove line-of-code breakpoints from a single location.</span></span>  

:::image type="complex" source="../media/javascript-sources-page-js-breakpoints-16-33.msft.png" alt-text="Der Haltepunkt-Panel" lightbox="../media/javascript-sources-page-js-breakpoints-16-33.msft.png":::
   <span data-ttu-id="4f1f9-160">Der **Haltepunkt** -Panel</span><span class="sxs-lookup"><span data-stu-id="4f1f9-160">The **Breakpoints** panel</span></span>  
:::image-end:::  

*   <span data-ttu-id="4f1f9-161">Aktivieren Sie das Kontrollkästchen neben einem Eintrag, um diesen Haltepunkt zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="4f1f9-161">Check the checkbox next to an entry to disable that breakpoint.</span></span>  
*   <span data-ttu-id="4f1f9-162">Klicken Sie mit der rechten Maustaste auf einen Eintrag, um diesen Haltepunkt zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="4f1f9-162">Right-click an entry to remove that breakpoint.</span></span>  
*   <span data-ttu-id="4f1f9-163">Klicken Sie mit der rechten Maustaste auf eine beliebige Stelle im Bereich **Haltepunkte** , um alle Haltepunkte zu deaktivieren, alle Haltepunkte zu deaktivieren oder alle Haltepunkte zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="4f1f9-163">Right-click anywhere in the **Breakpoints** pane to deactivate all breakpoints, disable all breakpoints, or remove all breakpoints.</span></span>  <span data-ttu-id="4f1f9-164">Das Deaktivieren aller Haltepunkte entspricht der Deaktivierung der einzelnen Haltepunkte.</span><span class="sxs-lookup"><span data-stu-id="4f1f9-164">Disabling all breakpoints is equivalent to unchecking each one.</span></span>  <span data-ttu-id="4f1f9-165">Durch die Deaktivierung aller Haltepunkte wird devtools angewiesen, alle Zeile-zu-Code-Haltepunkte zu ignorieren, aber auch den aktivierten Zustand beizubehalten, damit sich jeder in demselben Zustand wie zuvor befindet, wenn Sie ihn wieder aktivieren.</span><span class="sxs-lookup"><span data-stu-id="4f1f9-165">Deactivating all breakpoints instructs DevTools to ignore all line-of-code breakpoints, but to also maintain the enabled state so that each are in the same state as before when you reactivate each one.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-page-js-breakpoints-deactivate-breakpoints.msft.png" alt-text="Deaktivierte Haltepunkte im Bereich "Haltepunkte"" lightbox="../media/javascript-sources-page-js-breakpoints-deactivate-breakpoints.msft.png":::
       <span data-ttu-id="4f1f9-167">Deaktivierte Haltepunkte im Bereich " **Haltepunkte** "</span><span class="sxs-lookup"><span data-stu-id="4f1f9-167">Deactivated breakpoints in the **Breakpoints** pane</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="4f1f9-168">Dom-Änderungs Haltepunkte</span><span class="sxs-lookup"><span data-stu-id="4f1f9-168">DOM change breakpoints</span></span>   

<span data-ttu-id="4f1f9-169">Verwenden Sie einen Dom-Änderungs Haltepunkt, wenn Sie den Code anhalten möchten, durch den ein DOM-Knoten oder die untergeordneten Elemente geändert werden.</span><span class="sxs-lookup"><span data-stu-id="4f1f9-169">Use a DOM change breakpoint when you want to pause on the code that changes a DOM node or the children.</span></span>  

<span data-ttu-id="4f1f9-170">So setzen Sie einen Dom-Änderungs Haltepunkt:</span><span class="sxs-lookup"><span data-stu-id="4f1f9-170">To set a DOM change breakpoint:</span></span>  

1.  <span data-ttu-id="4f1f9-171">Klicken Sie auf die Registerkarte **Elemente** .</span><span class="sxs-lookup"><span data-stu-id="4f1f9-171">Click the **Elements** tab.</span></span>  
1.  <span data-ttu-id="4f1f9-172">Wechseln Sie zu dem Element, für das Sie den Haltepunkt festlegen möchten.</span><span class="sxs-lookup"><span data-stu-id="4f1f9-172">Go the element on which you want to set the breakpoint.</span></span>  
1.  <span data-ttu-id="4f1f9-173">Klicken Sie mit der rechten Maustaste auf das Element.</span><span class="sxs-lookup"><span data-stu-id="4f1f9-173">Right-click the element.</span></span>  
1.  <span data-ttu-id="4f1f9-174">Zeigen Sie **mit der Maus auf Umbruch**, und wählen Sie dann **Strukturänderungen**, **Attributänderungen**oder **Knoten Entfernung**aus.</span><span class="sxs-lookup"><span data-stu-id="4f1f9-174">Hover over **Break on**, then select **Subtree modifications**, **Attribute modifications**, or **Node removal**.</span></span>  
    
    :::image type="complex" source="../media/javascript-elements-break-on-subtree-modifications.msft.png" alt-text="Das Kontextmenü zum Erstellen eines DOM-Änderungs Haltepunkts" lightbox="../media/javascript-elements-break-on-subtree-modifications.msft.png":::
       <span data-ttu-id="4f1f9-176">Das Kontextmenü zum Erstellen eines DOM-Änderungs Haltepunkts</span><span class="sxs-lookup"><span data-stu-id="4f1f9-176">The context menu for creating a DOM change breakpoint</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="4f1f9-177">Typen von Dom-Änderungs Haltepunkten</span><span class="sxs-lookup"><span data-stu-id="4f1f9-177">Types of DOM change breakpoints</span></span>   

*   <span data-ttu-id="4f1f9-178">Teil **Strukturänderungen**.</span><span class="sxs-lookup"><span data-stu-id="4f1f9-178">**Subtree modifications**.</span></span>  <span data-ttu-id="4f1f9-179">Wird ausgelöst, wenn ein untergeordnetes Element des aktuell ausgewählten Knotens entfernt oder hinzugefügt oder der Inhalt eines untergeordneten Elements geändert wird.</span><span class="sxs-lookup"><span data-stu-id="4f1f9-179">Triggered when a child of the currently-selected node is removed or added, or the contents of a child are changed.</span></span>  <span data-ttu-id="4f1f9-180">Wird nicht für Änderungen an einem Attribut des untergeordneten Knotens oder für Änderungen am aktuell ausgewählten Knoten ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="4f1f9-180">Not triggered on child node attribute changes, or on any changes to the currently-selected node.</span></span>  
*   <span data-ttu-id="4f1f9-181">Attribut **Änderungen**: wird ausgelöst, wenn ein Attribut auf dem aktuell ausgewählten Knoten hinzugefügt oder entfernt wird oder wenn sich ein Attributwert ändert.</span><span class="sxs-lookup"><span data-stu-id="4f1f9-181">**Attributes modifications**: Triggered when an attribute is added or removed on the currently-selected node, or when an attribute value changes.</span></span>  
*   <span data-ttu-id="4f1f9-182">**Knoten Entfernung**: wird ausgelöst, wenn der aktuell ausgewählte Knoten entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="4f1f9-182">**Node Removal**: Triggered when the currently-selected node is removed.</span></span>  
    
## <span data-ttu-id="4f1f9-183">XMLHttpRequest/FETCH-Haltepunkte</span><span class="sxs-lookup"><span data-stu-id="4f1f9-183">XHR/Fetch breakpoints</span></span>   

<span data-ttu-id="4f1f9-184">Verwenden Sie einen XMLHttpRequest-Haltepunkt, wenn Sie unterbrechen möchten, wenn die Anforderungs-URL eines XMLHttpRequest eine angegebene Zeichenfolge enthält.</span><span class="sxs-lookup"><span data-stu-id="4f1f9-184">Use an XHR breakpoint when you want to break when the request URL of an XHR contains a specified string.</span></span>  <span data-ttu-id="4f1f9-185">DevTools wird in der Codezeile angehalten, in der die XMLHttpRequest die `send()` Methode ausführt.</span><span class="sxs-lookup"><span data-stu-id="4f1f9-185">DevTools pauses on the line of code where the XHR runs the `send()` method.</span></span>  

> [!NOTE]
> <span data-ttu-id="4f1f9-186">Dieses Feature funktioniert auch mit [Fetch-API-][MDNFetchApi] Anforderungen.</span><span class="sxs-lookup"><span data-stu-id="4f1f9-186">This feature also works with [Fetch API][MDNFetchApi] requests.</span></span>  

<span data-ttu-id="4f1f9-187">Wenn dies hilfreich ist, können Sie beispielsweise feststellen, dass die Seite eine falsche URL anfordert, und Sie möchten schnell den AJAX-oder Fetch-Quellcode finden, der die falsche Anforderung verursacht.</span><span class="sxs-lookup"><span data-stu-id="4f1f9-187">One example of when this is helpful is when you see that your page is requesting an incorrect URL, and you want to quickly find the AJAX or Fetch source code that is causing the incorrect request.</span></span>  

<span data-ttu-id="4f1f9-188">So setzen Sie einen XMLHttpRequest-Haltepunkt:</span><span class="sxs-lookup"><span data-stu-id="4f1f9-188">To set an XHR breakpoint:</span></span>  

1.  <span data-ttu-id="4f1f9-189">Klicken Sie auf die Registerkarte **Quellen** .</span><span class="sxs-lookup"><span data-stu-id="4f1f9-189">Click the **Sources** tab.</span></span>  
1.  <span data-ttu-id="4f1f9-190">Erweitern Sie den Bereich **XMLHttpRequest-Haltepunkte** .</span><span class="sxs-lookup"><span data-stu-id="4f1f9-190">Expand the **XHR Breakpoints** pane.</span></span>  
1.  <span data-ttu-id="4f1f9-191">Klicken Sie auf **Haltepunkt hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="4f1f9-191">Click **Add breakpoint**.</span></span>  
1.  <span data-ttu-id="4f1f9-192">Geben Sie die Zeichenfolge ein, die Sie aufheben möchten.</span><span class="sxs-lookup"><span data-stu-id="4f1f9-192">Enter the string which you want to break on.</span></span>  <span data-ttu-id="4f1f9-193">DevTools wird angehalten, wenn diese Zeichenfolge an einer beliebigen Stelle in einer XMLHttpRequest-Anforderungs-URL vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="4f1f9-193">DevTools pauses when this string is present anywhere in an XHR request URL.</span></span>  
1.  <span data-ttu-id="4f1f9-194">Drücken Sie `Enter` , um zu bestätigen.</span><span class="sxs-lookup"><span data-stu-id="4f1f9-194">Press `Enter` to confirm.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-page-js-xhr-fetch-breakpoints-org.msft.png" alt-text="Erstellen eines XMLHttpRequest-Haltepunkts" lightbox="../media/javascript-sources-page-js-xhr-fetch-breakpoints-org.msft.png":::
       <span data-ttu-id="4f1f9-196">Erstellen eines XMLHttpRequest-Haltepunkts</span><span class="sxs-lookup"><span data-stu-id="4f1f9-196">Create an XHR breakpoint</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="4f1f9-197">Ereignis-Listener-Haltepunkte</span><span class="sxs-lookup"><span data-stu-id="4f1f9-197">Event listener breakpoints</span></span> 

<span data-ttu-id="4f1f9-198">Verwenden Sie Ereignis-Listener-Haltepunkte, wenn Sie den Ereignislistener-Code anhalten möchten, der nach dem Auslösen eines Ereignisses ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4f1f9-198">Use event listener breakpoints when you want to pause on the event listener code that runs after an event is fired.</span></span>  <span data-ttu-id="4f1f9-199">Sie können bestimmte Ereignisse, beispielsweise `click` oder Kategorien von Ereignissen, wie alle Mausereignisse auswählen.</span><span class="sxs-lookup"><span data-stu-id="4f1f9-199">You are able to select specific events, such as `click`, or categories of events, such as all mouse events.</span></span>  

1.  <span data-ttu-id="4f1f9-200">Klicken Sie auf die Registerkarte **Quellen** .</span><span class="sxs-lookup"><span data-stu-id="4f1f9-200">Click the **Sources** tab.</span></span>  
1.  <span data-ttu-id="4f1f9-201">Erweitern Sie den Bereich **Ereignislistener-Haltepunkte** .</span><span class="sxs-lookup"><span data-stu-id="4f1f9-201">Expand the **Event Listener Breakpoints** pane.</span></span>  <span data-ttu-id="4f1f9-202">DevTools zeigt eine Liste der Ereigniskategorien, wie etwa **Animationen**, an.</span><span class="sxs-lookup"><span data-stu-id="4f1f9-202">DevTools shows a list of event categories, such as **Animation**.</span></span>  
1.  <span data-ttu-id="4f1f9-203">Überprüfen Sie eine dieser Kategorien, um zu pausieren, wenn ein Ereignis aus dieser Kategorie ausgelöst wird, oder erweitern Sie die Kategorie, und überprüfen Sie ein bestimmtes Ereignis.</span><span class="sxs-lookup"><span data-stu-id="4f1f9-203">Check one of these categories to pause whenever any event from that category is fired, or expand the category and check a specific event.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-page-js-event-listener-breakpoints-device-deviceorientation.msft.png" alt-text="Erstellen eines Ereignis-Listener-Haltepunkts" lightbox="../media/javascript-sources-page-js-event-listener-breakpoints-device-deviceorientation.msft.png":::
       <span data-ttu-id="4f1f9-205">Erstellen eines Ereignis-Listener-Haltepunkts</span><span class="sxs-lookup"><span data-stu-id="4f1f9-205">Create an event listener breakpoint</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="4f1f9-206">Ausnahme Haltepunkte</span><span class="sxs-lookup"><span data-stu-id="4f1f9-206">Exception breakpoints</span></span>   

<span data-ttu-id="4f1f9-207">Verwenden Sie Ausnahme Haltepunkte, wenn Sie in der Codezeile anhalten möchten, die eine abgefangene oder nicht abgefangene Ausnahme auslöst.</span><span class="sxs-lookup"><span data-stu-id="4f1f9-207">Use exception breakpoints when you want to pause on the line of code that is throwing a caught or uncaught exception.</span></span>  

1.  <span data-ttu-id="4f1f9-208">Klicken Sie auf die Registerkarte **Quellen** .</span><span class="sxs-lookup"><span data-stu-id="4f1f9-208">Click the **Sources** tab.</span></span>  
1.  <span data-ttu-id="4f1f9-209">Klicken Sie auf **Ausnahmen anhalten** \ ( ![ bei Ausnahmen anhalten ][ImagePauseOnExceptionsIcon] \).</span><span class="sxs-lookup"><span data-stu-id="4f1f9-209">Click **Pause on exceptions** \(![Pause on exceptions][ImagePauseOnExceptionsIcon]\).</span></span>  <span data-ttu-id="4f1f9-210">Das Symbol wird blau, wenn es aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="4f1f9-210">The icon turns blue when enabled.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-page-js-pause-on-exceptions.msft.png" alt-text="Schaltfläche "auf Ausnahmen pausieren"" lightbox="../media/javascript-sources-page-js-pause-on-exceptions.msft.png":::
       <span data-ttu-id="4f1f9-212">Schaltfläche " **auf Ausnahmen pausieren** "</span><span class="sxs-lookup"><span data-stu-id="4f1f9-212">The **Pause on exceptions** button</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="4f1f9-213">**Optional**.</span><span class="sxs-lookup"><span data-stu-id="4f1f9-213">**Optional**.</span></span>  <span data-ttu-id="4f1f9-214">Aktivieren Sie das Kontrollkästchen **auf abgefangene Ausnahmen anhalten** , wenn Sie zusätzlich zu den nicht abgefangenen Ausnahmen auch auf abgefangene Ausnahmen anhalten möchten.</span><span class="sxs-lookup"><span data-stu-id="4f1f9-214">Check the **Pause On Caught Exceptions** checkbox if you also want to pause on caught exceptions, in addition to uncaught ones.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-page-js-paused-on-exception.msft.png" alt-text="Bei einer nicht abgefangenen Ausnahme angehalten" lightbox="../media/javascript-sources-page-js-paused-on-exception.msft.png":::
       <span data-ttu-id="4f1f9-216">Bei einer nicht abgefangenen Ausnahme angehalten</span><span class="sxs-lookup"><span data-stu-id="4f1f9-216">Paused on an uncaught exception</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="4f1f9-217">Funktionshaltepunkte</span><span class="sxs-lookup"><span data-stu-id="4f1f9-217">Function breakpoints</span></span>   

<span data-ttu-id="4f1f9-218">Führen Sie die Methode aus, `debug(method)` wobei `method` der Befehl, die Funktion oder die Methode, die Sie debuggen möchten, ist, wenn Sie anhalten möchten, wenn eine bestimmte Funktion ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4f1f9-218">Run the `debug(method)` method, where `method` is the command, function, or method you want to debug, when you want to pause whenever a specific function is run.</span></span>  <span data-ttu-id="4f1f9-219">Sie können `debug()` in Ihren Code einfügen (wie eine `console.log()` Anweisung) oder die Methode über die devtools-Konsole ausführen.</span><span class="sxs-lookup"><span data-stu-id="4f1f9-219">You may insert `debug()` into your code (like a `console.log()` statement) or run the method from the DevTools Console.</span></span>  `debug()` <span data-ttu-id="4f1f9-220">entspricht dem Festlegen eines [Haltepunkts für die Code Zeile](#line-of-code-breakpoints) in der ersten Zeile der Funktion.</span><span class="sxs-lookup"><span data-stu-id="4f1f9-220">is equivalent to setting a [line-of-code breakpoint](#line-of-code-breakpoints) on the first line of the function.</span></span>  

```javascript
function sum(a, b) {
    let result = a + b; // DevTools pauses on this line.
    return result;
}
debug(sum); // Pass the function object, not a string.
sum();
```  

### <span data-ttu-id="4f1f9-221">Sicherstellen, dass sich die Zielfunktion im Bereich befindet</span><span class="sxs-lookup"><span data-stu-id="4f1f9-221">Make sure the target function is in scope</span></span>   

<span data-ttu-id="4f1f9-222">DevTools löst a `ReferenceError` aus, wenn sich die zu debuggende Funktion nicht im Bereich befindet.</span><span class="sxs-lookup"><span data-stu-id="4f1f9-222">DevTools throws a `ReferenceError` if the function you want to debug is not in scope.</span></span>  

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

<span data-ttu-id="4f1f9-223">Die Sicherstellung, dass die Zielfunktion im Bereich liegt, ist schwierig, wenn Sie die `debug()` Methode über die devtools-Konsole ausführen.</span><span class="sxs-lookup"><span data-stu-id="4f1f9-223">Ensuring the target function is in scope is tricky if you are running the `debug()` method from the DevTools Console.</span></span>  <span data-ttu-id="4f1f9-224">Hier ist eine Strategie:</span><span class="sxs-lookup"><span data-stu-id="4f1f9-224">Here is one strategy:</span></span>  

1.  <span data-ttu-id="4f1f9-225">Setzen Sie einen [Haltepunkt für die Codezeile](#line-of-code-breakpoints) an einer beliebigen Stelle, an der sich die Funktion im Bereich befindet.</span><span class="sxs-lookup"><span data-stu-id="4f1f9-225">Set a [line-of-code breakpoint](#line-of-code-breakpoints) somewhere where the function is in scope.</span></span>
1.  <span data-ttu-id="4f1f9-226">Auslösen des Haltepunkts</span><span class="sxs-lookup"><span data-stu-id="4f1f9-226">Trigger the breakpoint.</span></span>  
1.  <span data-ttu-id="4f1f9-227">Führen `debug()` Sie die Methode in der devtools-Konsole aus, während der Code weiterhin auf dem Haltepunkt für die Code Zeile angehalten wird.</span><span class="sxs-lookup"><span data-stu-id="4f1f9-227">Run the `debug()` method in the DevTools Console while the code is still paused on your line-of-code breakpoint.</span></span>  
    
<!---  
 


-->  

<!-- image links -->  

[ImagePauseOnExceptionsIcon]: ../media/pause-on-exceptions-icon.msft.png  

<!-- links -->  

[DevtoolsJavascriptIndex]: index.md "Erste Schritte mit dem Debuggen von JavaScript in Microsoft Edge devtools | Microsoft docs"  

[MDNFetchApi]: https://developer.mozilla.org/docs/Web/API/Fetch_API "FETCH-API | MDN"  

> [!NOTE]
> <span data-ttu-id="4f1f9-230">Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4f1f9-230">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="4f1f9-231">Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/javascript/breakpoints) und wird von [Kayce Basken][KayceBasques] (Technical Writer, Chrome devtools & Lighthouse) erstellt.</span><span class="sxs-lookup"><span data-stu-id="4f1f9-231">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/javascript/breakpoints) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools & Lighthouse\).</span></span>  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
<span data-ttu-id="4f1f9-233">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="4f1f9-233">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
