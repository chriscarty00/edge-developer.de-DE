---
description: Erfahren Sie mehr über alle Möglichkeiten, wie Sie Ihren Code in devTools Microsoft Edge können.
title: So unterbrechen Sie Ihren Code mit Haltepunkten in Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, Entwicklungstools
ms.openlocfilehash: fda536deb7177b933013120fc11b0896acfbbe5c
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/13/2021
ms.locfileid: "11564175"
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
# <a name="how-to-pause-your-code-with-breakpoints-in-microsoft-edge-devtools"></a><span data-ttu-id="c3cff-104">So unterbrechen Sie Ihren Code mit Haltepunkten in Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="c3cff-104">How to pause your code with breakpoints in Microsoft Edge DevTools</span></span>  

<span data-ttu-id="c3cff-105">Verwenden Sie Haltepunkte, um Ihren JavaScript-Code anzuhalten.</span><span class="sxs-lookup"><span data-stu-id="c3cff-105">Use breakpoints to pause your JavaScript code.</span></span>  <span data-ttu-id="c3cff-106">In diesem Artikel werden die in DevTools verfügbaren Haltepunkttypen sowie die Verwendung und das Festlegen der einzelnen Typen erläutert.</span><span class="sxs-lookup"><span data-stu-id="c3cff-106">This article explains each type of breakpoint available in DevTools, as well as when to use and how to set each type.</span></span>

<span data-ttu-id="c3cff-107">Ein Einführungstutorial mit einer vorhandenen Webseite finden Sie unter Erste Schritte mit dem Debuggen von [JavaScript in Microsoft Edge DevTools][DevtoolsJavascriptIndex].</span><span class="sxs-lookup"><span data-stu-id="c3cff-107">For an introductory tutorial using an existing webpage, navigate to [Get started with debugging JavaScript in Microsoft Edge DevTools][DevtoolsJavascriptIndex].</span></span>

## <a name="overview-of-when-to-use-each-breakpoint-type"></a><span data-ttu-id="c3cff-108">Übersicht über die Verwendung der einzelnen Haltepunkttypen</span><span class="sxs-lookup"><span data-stu-id="c3cff-108">Overview of when to use each breakpoint type</span></span>  

<span data-ttu-id="c3cff-109">Der bekannteste Haltepunkttyp ist die Codezeile.</span><span class="sxs-lookup"><span data-stu-id="c3cff-109">The most well-known type of breakpoint is line-of-code.</span></span>  <span data-ttu-id="c3cff-110">Aber codebasierte Haltepunkte können ineffizient festgelegt werden, insbesondere wenn Sie nicht genau wissen, wo sie aussehen sollen, oder wenn Sie mit einer großen Codebasis arbeiten.</span><span class="sxs-lookup"><span data-stu-id="c3cff-110">But line-of-code breakpoints may be inefficient to set, especially if you do not know exactly where to look, or if you are working with a large codebase.</span></span>  <span data-ttu-id="c3cff-111">Sie können sich beim Debuggen Zeit sparen, indem Sie wissen, wie und wann die anderen Arten von Haltepunkten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c3cff-111">You may save yourself time when debugging by knowing how and when to use the other types of breakpoints.</span></span>  

| <span data-ttu-id="c3cff-112">Haltepunkttyp</span><span class="sxs-lookup"><span data-stu-id="c3cff-112">Breakpoint Type</span></span> | <span data-ttu-id="c3cff-113">Verwenden Sie dies, wenn Sie anhalten möchten...</span><span class="sxs-lookup"><span data-stu-id="c3cff-113">Use This When You Want To Pause...</span></span> |  
|:--- |:--- |  
| [<span data-ttu-id="c3cff-114">Codezeile</span><span class="sxs-lookup"><span data-stu-id="c3cff-114">Line-of-code</span></span>](#line-of-code-breakpoints) | <span data-ttu-id="c3cff-115">Für einen genauen Codebereich.</span><span class="sxs-lookup"><span data-stu-id="c3cff-115">On an exact region of code.</span></span>  |  
| [<span data-ttu-id="c3cff-116">Bedingte Codezeile</span><span class="sxs-lookup"><span data-stu-id="c3cff-116">Conditional line-of-code</span></span>](#conditional-line-of-code-breakpoints) | <span data-ttu-id="c3cff-117">Für einen genauen Codebereich, jedoch nur, wenn eine andere Bedingung true ist.</span><span class="sxs-lookup"><span data-stu-id="c3cff-117">On an exact region of code, but only when some other condition is true.</span></span>  |  
| [<span data-ttu-id="c3cff-118">DOM</span><span class="sxs-lookup"><span data-stu-id="c3cff-118">DOM</span></span>](#dom-change-breakpoints) | <span data-ttu-id="c3cff-119">Auf dem Code, der einen bestimmten DOM-Knoten ändert oder entfernt, oder die unteren Knoten.</span><span class="sxs-lookup"><span data-stu-id="c3cff-119">On the code that changes or removes a specific DOM node, or the children.</span></span>  |  
| [<span data-ttu-id="c3cff-120">XHR</span><span class="sxs-lookup"><span data-stu-id="c3cff-120">XHR</span></span>](#xhrfetch-breakpoints) | <span data-ttu-id="c3cff-121">Wenn eine XHR-URL ein Zeichenfolgenmuster enthält.</span><span class="sxs-lookup"><span data-stu-id="c3cff-121">When an XHR URL contains a string pattern.</span></span>  |  
| [<span data-ttu-id="c3cff-122">Ereignislistener</span><span class="sxs-lookup"><span data-stu-id="c3cff-122">Event listener</span></span>](#event-listener-breakpoints) | <span data-ttu-id="c3cff-123">Auf dem Code, der nach einem Ereignis ausgeführt wird, z. B. `click` , wird ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c3cff-123">On the code that runs after an event, such as `click`, runs.</span></span>  |  
| [<span data-ttu-id="c3cff-124">Ausnahme</span><span class="sxs-lookup"><span data-stu-id="c3cff-124">Exception</span></span>](#exception-breakpoints) | <span data-ttu-id="c3cff-125">In der Codezeile, die eine Ausnahme beim Abfangen oder Nichtfangen auslöst.</span><span class="sxs-lookup"><span data-stu-id="c3cff-125">On the line of code that is throwing a caught or uncaught exception.</span></span>  |  
| [<span data-ttu-id="c3cff-126">Funktion</span><span class="sxs-lookup"><span data-stu-id="c3cff-126">Function</span></span>](#function-breakpoints) | <span data-ttu-id="c3cff-127">Jedes Mal, wenn ein bestimmter Befehl, eine bestimmte Funktion oder methode ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c3cff-127">Whenever a specific command, function, or method is run.</span></span>  |  

## <a name="line-of-code-breakpoints"></a><span data-ttu-id="c3cff-128">Zeilen-von-Code-Haltepunkte</span><span class="sxs-lookup"><span data-stu-id="c3cff-128">Line-of-code breakpoints</span></span>  

<span data-ttu-id="c3cff-129">Verwenden Sie einen Codezeile-Haltepunkt, wenn Sie den genauen Codebereich kennen, den Sie untersuchen müssen.</span><span class="sxs-lookup"><span data-stu-id="c3cff-129">Use a line-of-code breakpoint when you know the exact region of code that you need to investigate.</span></span>  <span data-ttu-id="c3cff-130">DevTools hält immer an, bevor diese Codezeile ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c3cff-130">DevTools always pauses before this line of code is run.</span></span>  

<span data-ttu-id="c3cff-131">So legen Sie einen Codezeile-Haltepunkt in DevTools ein:</span><span class="sxs-lookup"><span data-stu-id="c3cff-131">To set a line-of-code breakpoint in DevTools:</span></span>  

1.  <span data-ttu-id="c3cff-132">Wählen Sie das **Tool Quellen** aus.</span><span class="sxs-lookup"><span data-stu-id="c3cff-132">Choose the **Sources** tool.</span></span>  
1.  <span data-ttu-id="c3cff-133">Öffnen Sie die Datei, die die Codezeile enthält, in der Sie die Datei umbrechen möchten.</span><span class="sxs-lookup"><span data-stu-id="c3cff-133">Open the file containing the line of code on which you want to break.</span></span>  
1.  <span data-ttu-id="c3cff-134">Wechseln Sie zur Codezeile.</span><span class="sxs-lookup"><span data-stu-id="c3cff-134">Go the line of code.</span></span>  
1.  <span data-ttu-id="c3cff-135">Links von der Codezeile befindet sich die Zeilennummerspalte.</span><span class="sxs-lookup"><span data-stu-id="c3cff-135">To the left of the line of code is the line number column.</span></span>  <span data-ttu-id="c3cff-136">Wählen Sie sie aus.</span><span class="sxs-lookup"><span data-stu-id="c3cff-136">Choose it.</span></span>  <span data-ttu-id="c3cff-137">Neben der Zeilennummerspalte wird ein rotes Symbol angezeigt.</span><span class="sxs-lookup"><span data-stu-id="c3cff-137">A red icon appears next to the line number column.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-page-js-breakpoint-30.msft.png" alt-text="Ein Codezeile-Haltepunkt" lightbox="../media/javascript-sources-page-js-breakpoint-30.msft.png":::
       <span data-ttu-id="c3cff-139">Ein Codezeile-Haltepunkt</span><span class="sxs-lookup"><span data-stu-id="c3cff-139">A line-of-code breakpoint</span></span>  
    :::image-end:::  
    
### <a name="line-of-code-breakpoints-in-your-code"></a><span data-ttu-id="c3cff-140">Zeilen-von-Code-Haltepunkte in Ihrem Code</span><span class="sxs-lookup"><span data-stu-id="c3cff-140">Line-of-code breakpoints in your code</span></span>  

<span data-ttu-id="c3cff-141">Führen Sie `debugger` die -Methode aus Ihrem Code aus, um diese Zeile anzuhalten.</span><span class="sxs-lookup"><span data-stu-id="c3cff-141">Run the `debugger` method from your code to pause on that line.</span></span>  <span data-ttu-id="c3cff-142">Dies entspricht einem [Zeilen-von-Code-Haltepunkt,](#line-of-code-breakpoints)mit der Ausnahme, dass der Haltepunkt in Ihrem Code festgelegt ist, nicht in der DevTools-Benutzeroberfläche.</span><span class="sxs-lookup"><span data-stu-id="c3cff-142">This is equivalent to a [line-of-code breakpoint](#line-of-code-breakpoints), except that the breakpoint is set in your code, not in the DevTools UI.</span></span>  

```javascript
console.log('a');
console.log('b');
debugger;
console.log('c');
```  

### <a name="conditional-line-of-code-breakpoints"></a><span data-ttu-id="c3cff-143">Bedingte Zeilen-von-Code-Haltepunkte</span><span class="sxs-lookup"><span data-stu-id="c3cff-143">Conditional line-of-code breakpoints</span></span>  

<span data-ttu-id="c3cff-144">Verwenden Sie einen bedingten Zeilen-von-Code-Haltepunkt, wenn Sie den genauen Codebereich kennen, den Sie untersuchen müssen, aber Sie möchten nur anhalten, wenn eine andere Bedingung wahr ist.</span><span class="sxs-lookup"><span data-stu-id="c3cff-144">Use a conditional line-of-code breakpoint when you know the exact region of code that you need to investigate, but you want to pause only when some other condition is true.</span></span>  

<span data-ttu-id="c3cff-145">So legen Sie einen bedingten Codelinien-Haltepunkt ein:</span><span class="sxs-lookup"><span data-stu-id="c3cff-145">To set a conditional line-of-code breakpoint:</span></span>  

1.  <span data-ttu-id="c3cff-146">Wählen Sie das **Tool Quellen** aus.</span><span class="sxs-lookup"><span data-stu-id="c3cff-146">Choose the **Sources** tool.</span></span>  
1.  <span data-ttu-id="c3cff-147">Öffnen Sie die Datei, die die Codezeile enthält, in der Sie die Datei umbrechen möchten.</span><span class="sxs-lookup"><span data-stu-id="c3cff-147">Open the file containing the line of code on which you want to break.</span></span>  
1.  <span data-ttu-id="c3cff-148">Wechseln Sie zur Codezeile.</span><span class="sxs-lookup"><span data-stu-id="c3cff-148">Go the line of code.</span></span>  
1.  <span data-ttu-id="c3cff-149">Links von der Codezeile befindet sich die Zeilennummerspalte.</span><span class="sxs-lookup"><span data-stu-id="c3cff-149">To the left of the line of code is the line number column.</span></span>  <span data-ttu-id="c3cff-150">Zeigen Sie auf die Zeilennummer, und öffnen Sie das Kontextmenü \(klicken Sie mit der rechten Maustaste\).</span><span class="sxs-lookup"><span data-stu-id="c3cff-150">Hover on the line number and open the contextual menu \(right-click\).</span></span>  
1.  <span data-ttu-id="c3cff-151">Wählen **Sie Bedingten Haltepunkt hinzufügen aus.**</span><span class="sxs-lookup"><span data-stu-id="c3cff-151">Choose **Add conditional breakpoint**.</span></span>  <span data-ttu-id="c3cff-152">Unterhalb der Codezeile wird ein Dialogfeld angezeigt.</span><span class="sxs-lookup"><span data-stu-id="c3cff-152">A dialog displays underneath the line of code.</span></span>  
1.  <span data-ttu-id="c3cff-153">Geben Sie Ihre Bedingung in das Dialogfeld ein.</span><span class="sxs-lookup"><span data-stu-id="c3cff-153">Enter your condition in the dialog.</span></span>  
1.  <span data-ttu-id="c3cff-154">Wählen `Enter` Sie diese Option aus, um den Haltepunkt zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="c3cff-154">Select `Enter` to activate the breakpoint.</span></span>  <span data-ttu-id="c3cff-155">Ein Symbol neben der Zeilennummerspalte.</span><span class="sxs-lookup"><span data-stu-id="c3cff-155">An icon next to the line number column.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-page-js-conditional-breakpoint.msft.png" alt-text="Ein bedingter Zeilen-von-Code-Haltepunkt" lightbox="../media/javascript-sources-page-js-conditional-breakpoint.msft.png":::
       <span data-ttu-id="c3cff-157">Ein bedingter Zeilen-von-Code-Haltepunkt</span><span class="sxs-lookup"><span data-stu-id="c3cff-157">A conditional line-of-code breakpoint</span></span>  
    :::image-end:::  
    
### <a name="manage-line-of-code-breakpoints"></a><span data-ttu-id="c3cff-158">Verwalten von Zeilen-von-Code-Haltepunkten</span><span class="sxs-lookup"><span data-stu-id="c3cff-158">Manage line-of-code breakpoints</span></span>  

<span data-ttu-id="c3cff-159">Verwenden Sie **den Bereich Haltepunkte,** um Codelinien-Haltepunkte an einem einzigen Speicherort zu deaktivieren oder zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="c3cff-159">Use the **Breakpoints** pane to disable or remove line-of-code breakpoints from a single location.</span></span>  

:::image type="complex" source="../media/javascript-sources-page-js-breakpoints-16-33.msft.png" alt-text="The Breakpoints panel" lightbox="../media/javascript-sources-page-js-breakpoints-16-33.msft.png":::
   <span data-ttu-id="c3cff-161">The **Breakpoints** panel</span><span class="sxs-lookup"><span data-stu-id="c3cff-161">The **Breakpoints** panel</span></span>  
:::image-end:::  

*   <span data-ttu-id="c3cff-162">Aktivieren Sie das Kontrollkästchen neben einem Eintrag, um diesen Haltepunkt zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="c3cff-162">Check the checkbox next to an entry to disable that breakpoint.</span></span>  
*   <span data-ttu-id="c3cff-163">Zeigen Sie auf einen Eintrag, und öffnen Sie das Kontextmenü \(klicken Sie mit der rechten Maustaste\), um diesen Haltepunkt zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="c3cff-163">Hover on an entry and open the contextual menu \(right-click\) to remove that breakpoint.</span></span>  
*   <span data-ttu-id="c3cff-164">Zeigen Sie \*\*\*\* auf eine beliebige Stelle im Bereich Haltepunkte, und öffnen Sie das Kontextmenü \(mit der rechten Maustaste\), um alle Haltepunkte zu deaktivieren, alle Haltepunkte zu deaktivieren oder alle Haltepunkte zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="c3cff-164">Hover anywhere in the **Breakpoints** pane and open the contextual menu \(right-click\) to deactivate all breakpoints, disable all breakpoints, or remove all breakpoints.</span></span>  <span data-ttu-id="c3cff-165">Das Deaktivieren aller Haltepunkte entspricht dem Deaktivieren der einzelnen Haltepunkte.</span><span class="sxs-lookup"><span data-stu-id="c3cff-165">Disabling all breakpoints is equivalent to unchecking each one.</span></span>  <span data-ttu-id="c3cff-166">Durch das Deaktivieren aller Haltepunkte wird DevTools angewiesen, alle Zeilen-von-Code-Haltepunkte zu ignorieren, aber auch den aktivierten Zustand so zu verwalten, dass sich alle im gleichen Zustand befinden wie zuvor, wenn Sie die einzelnen Haltepunkte reaktivieren.</span><span class="sxs-lookup"><span data-stu-id="c3cff-166">Deactivating all breakpoints instructs DevTools to ignore all line-of-code breakpoints, but to also maintain the enabled state so that each are in the same state as before when you reactivate each one.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-page-js-breakpoints-deactivate-breakpoints.msft.png" alt-text="Deaktivierte Haltepunkte im Bereich Haltepunkte" lightbox="../media/javascript-sources-page-js-breakpoints-deactivate-breakpoints.msft.png":::
       <span data-ttu-id="c3cff-168">Deaktivierte Haltepunkte im **Bereich Haltepunkte**</span><span class="sxs-lookup"><span data-stu-id="c3cff-168">Deactivated breakpoints in the **Breakpoints** pane</span></span>  
    :::image-end:::  
    
## <a name="dom-change-breakpoints"></a><span data-ttu-id="c3cff-169">DOM-Änderungs-Haltepunkte</span><span class="sxs-lookup"><span data-stu-id="c3cff-169">DOM change breakpoints</span></span>  

<span data-ttu-id="c3cff-170">Verwenden Sie einen DOM-Änderungsbruchpunkt, wenn Sie den Code anhalten möchten, der einen DOM-Knoten oder die unteren Knoten ändert.</span><span class="sxs-lookup"><span data-stu-id="c3cff-170">Use a DOM change breakpoint when you want to pause on the code that changes a DOM node or the children.</span></span>  

<span data-ttu-id="c3cff-171">So legen Sie einen DOM-Änderungs-Haltepunkt ein:</span><span class="sxs-lookup"><span data-stu-id="c3cff-171">To set a DOM change breakpoint:</span></span>  

1.  <span data-ttu-id="c3cff-172">Wählen Sie das **Elementtool** aus.</span><span class="sxs-lookup"><span data-stu-id="c3cff-172">Choose the **Elements** tool.</span></span>  
1.  <span data-ttu-id="c3cff-173">Wechseln Sie zum Element, für das Sie den Haltepunkt festlegen möchten.</span><span class="sxs-lookup"><span data-stu-id="c3cff-173">Go the element on which you want to set the breakpoint.</span></span>  
1.  <span data-ttu-id="c3cff-174">Zeigen Sie auf das Element, und öffnen Sie das Kontextmenü \(klicken Sie mit der rechten Maustaste\).</span><span class="sxs-lookup"><span data-stu-id="c3cff-174">Hover on the element and open the contextual menu \(right-click\).</span></span>  
1.  <span data-ttu-id="c3cff-175">Zeigen Sie **auf Unterbrechung auf**, und wählen Sie dann **Subtree-Änderungen,** **Attributänderungen**oder **Knotenentfernung aus.**</span><span class="sxs-lookup"><span data-stu-id="c3cff-175">Hover on **Break on**, then choose **Subtree modifications**, **Attribute modifications**, or **Node removal**.</span></span>  
    
    :::image type="complex" source="../media/javascript-elements-break-on-subtree-modifications.msft.png" alt-text="Das Kontextmenü zum Erstellen eines DOM-Änderungs-Haltepunkts" lightbox="../media/javascript-elements-break-on-subtree-modifications.msft.png":::
       <span data-ttu-id="c3cff-177">Das Kontextmenü zum Erstellen eines DOM-Änderungs-Haltepunkts</span><span class="sxs-lookup"><span data-stu-id="c3cff-177">The context menu for creating a DOM change breakpoint</span></span>  
    :::image-end:::  
    
### <a name="types-of-dom-change-breakpoints"></a><span data-ttu-id="c3cff-178">Typen von DOM-Änderungs-Haltepunkten</span><span class="sxs-lookup"><span data-stu-id="c3cff-178">Types of DOM change breakpoints</span></span>  

*   <span data-ttu-id="c3cff-179">**Änderungen an der Unterstruktur**.</span><span class="sxs-lookup"><span data-stu-id="c3cff-179">**Subtree modifications**.</span></span>  <span data-ttu-id="c3cff-180">Wird ausgelöst, wenn ein untergeordnetes Element des aktuell ausgewählten Knotens entfernt oder hinzugefügt wird oder der Inhalt eines untergeordneten Knotens geändert wird.</span><span class="sxs-lookup"><span data-stu-id="c3cff-180">Triggered when a child of the currently-selected node is removed or added, or the contents of a child are changed.</span></span>  <span data-ttu-id="c3cff-181">Wird nicht bei Änderungen des untergeordneten Knotenattributs oder bei Änderungen am aktuell ausgewählten Knoten ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="c3cff-181">Not triggered on child node attribute changes, or on any changes to the currently-selected node.</span></span>  
*   <span data-ttu-id="c3cff-182">**Attributeänderungen:** Wird ausgelöst, wenn ein Attribut auf dem aktuell ausgewählten Knoten hinzugefügt oder entfernt wird oder wenn sich ein Attributwert ändert.</span><span class="sxs-lookup"><span data-stu-id="c3cff-182">**Attributes modifications**: Triggered when an attribute is added or removed on the currently-selected node, or when an attribute value changes.</span></span>  
*   <span data-ttu-id="c3cff-183">**Knotenentfernung**: Wird ausgelöst, wenn der aktuell ausgewählte Knoten entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="c3cff-183">**Node Removal**: Triggered when the currently-selected node is removed.</span></span>  
    
## <a name="xhrfetch-breakpoints"></a><span data-ttu-id="c3cff-184">XHR/Fetch-Haltepunkte</span><span class="sxs-lookup"><span data-stu-id="c3cff-184">XHR/Fetch breakpoints</span></span>  

<span data-ttu-id="c3cff-185">Verwenden Sie einen XHR-Haltepunkt, wenn Sie den Wert ändern möchten, wenn die Anforderungs-URL einer XHR eine angegebene Zeichenfolge enthält.</span><span class="sxs-lookup"><span data-stu-id="c3cff-185">Use an XHR breakpoint when you want to break when the request URL of an XHR contains a specified string.</span></span>  <span data-ttu-id="c3cff-186">DevTools hält in der Codezeile an, in der die XHR die Methode `send()` ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c3cff-186">DevTools pauses on the line of code where the XHR runs the `send()` method.</span></span>  

> [!NOTE]
> <span data-ttu-id="c3cff-187">Dieses Feature funktioniert auch mit [Fetch-API-Anforderungen.][MDNFetchApi]</span><span class="sxs-lookup"><span data-stu-id="c3cff-187">This feature also works with [Fetch API][MDNFetchApi] requests.</span></span>  

<span data-ttu-id="c3cff-188">Ein Beispiel dafür, wann dies hilfreich ist, ist, wenn Ihre Webseite eine falsche URL anfordert und Sie schnell den AJAX- oder Fetch-Quellcode finden möchten, der die falsche Anforderung verursacht.</span><span class="sxs-lookup"><span data-stu-id="c3cff-188">One example of when this is helpful is when your webpage is requesting an incorrect URL, and you want to quickly find the AJAX or Fetch source code that is causing the incorrect request.</span></span>  

<span data-ttu-id="c3cff-189">So legen Sie einen XHR-Haltepunkt ein:</span><span class="sxs-lookup"><span data-stu-id="c3cff-189">To set an XHR breakpoint:</span></span>  

1.  <span data-ttu-id="c3cff-190">Wählen Sie das **Tool Quellen** aus.</span><span class="sxs-lookup"><span data-stu-id="c3cff-190">Choose the **Sources** tool.</span></span>  
1.  <span data-ttu-id="c3cff-191">Erweitern Sie **den XHR-Haltepunktbereich.**</span><span class="sxs-lookup"><span data-stu-id="c3cff-191">Expand the **XHR Breakpoints** panel.</span></span>  
1.  <span data-ttu-id="c3cff-192">Wählen **Sie Haltepunkt hinzufügen aus.**</span><span class="sxs-lookup"><span data-stu-id="c3cff-192">Choose **Add breakpoint**.</span></span>  
1.  <span data-ttu-id="c3cff-193">Geben Sie die Zeichenfolge ein, die Sie umbrechen möchten.</span><span class="sxs-lookup"><span data-stu-id="c3cff-193">Enter the string which you want to break on.</span></span>  <span data-ttu-id="c3cff-194">DevTools hält an, wenn diese Zeichenfolge an einer beliebigen Stelle in einer XHR-Anforderungs-URL vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="c3cff-194">DevTools pauses when this string is present anywhere in an XHR request URL.</span></span>  
1.  <span data-ttu-id="c3cff-195">Wählen `Enter` Sie aus, um dies zu bestätigen.</span><span class="sxs-lookup"><span data-stu-id="c3cff-195">Select `Enter` to confirm.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-page-js-xhr-fetch-breakpoints-org.msft.png" alt-text="Erstellen eines XHR-Haltepunkts" lightbox="../media/javascript-sources-page-js-xhr-fetch-breakpoints-org.msft.png":::
       <span data-ttu-id="c3cff-197">Erstellen eines XHR-Haltepunkts</span><span class="sxs-lookup"><span data-stu-id="c3cff-197">Create an XHR breakpoint</span></span>  
    :::image-end:::  
    
## <a name="event-listener-breakpoints"></a><span data-ttu-id="c3cff-198">Haltepunkte für Ereignislistener</span><span class="sxs-lookup"><span data-stu-id="c3cff-198">Event listener breakpoints</span></span>  

<span data-ttu-id="c3cff-199">Verwenden Sie Ereignislistener-Haltepunkte, wenn Sie den Ereignislistenercode anhalten möchten, der nach dem Ausgelöst eines Ereignisses ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c3cff-199">Use event listener breakpoints when you want to pause on the event listener code that runs after an event is fired.</span></span>  <span data-ttu-id="c3cff-200">Sie können bestimmte Ereignisse auswählen, z. B. , oder Kategorien von Ereignissen, z. B. `click` alle Mausereignisse.</span><span class="sxs-lookup"><span data-stu-id="c3cff-200">You are able to select specific events, such as `click`, or categories of events, such as all mouse events.</span></span>  

1.  <span data-ttu-id="c3cff-201">Wählen Sie das **Tool Quellen** aus.</span><span class="sxs-lookup"><span data-stu-id="c3cff-201">Choose the **Sources** tool.</span></span>  
1.  <span data-ttu-id="c3cff-202">Erweitern Sie **den Bereich Ereignislistener-Haltepunkte.**</span><span class="sxs-lookup"><span data-stu-id="c3cff-202">Expand the **Event Listener Breakpoints** panel.</span></span>  <span data-ttu-id="c3cff-203">DevTools zeigt eine Liste der Ereigniskategorien an, z. B. **Animation**.</span><span class="sxs-lookup"><span data-stu-id="c3cff-203">DevTools shows a list of event categories, such as **Animation**.</span></span>  
1.  <span data-ttu-id="c3cff-204">Überprüfen Sie eine dieser Kategorien, um zu unterbrechen, wenn ein Ereignis aus dieser Kategorie ausgelöst wird, oder erweitern Sie die Kategorie, und überprüfen Sie ein bestimmtes Ereignis.</span><span class="sxs-lookup"><span data-stu-id="c3cff-204">Check one of these categories to pause whenever any event from that category is fired, or expand the category and check a specific event.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-page-js-event-listener-breakpoints-device-deviceorientation.msft.png" alt-text="Erstellen eines Haltepunkts für Ereignislistener" lightbox="../media/javascript-sources-page-js-event-listener-breakpoints-device-deviceorientation.msft.png":::
       <span data-ttu-id="c3cff-206">Erstellen eines Haltepunkts für Ereignislistener</span><span class="sxs-lookup"><span data-stu-id="c3cff-206">Create an event listener breakpoint</span></span>  
    :::image-end:::  
    
## <a name="exception-breakpoints"></a><span data-ttu-id="c3cff-207">Ausnahme-Haltepunkte</span><span class="sxs-lookup"><span data-stu-id="c3cff-207">Exception breakpoints</span></span>  

<span data-ttu-id="c3cff-208">Verwenden Sie Ausnahme-Haltepunkte, wenn Sie die Codezeile anhalten möchten, die eine Ausnahme beim Abfangen oder Nichtfangen auslöst.</span><span class="sxs-lookup"><span data-stu-id="c3cff-208">Use exception breakpoints when you want to pause on the line of code that is throwing a caught or uncaught exception.</span></span>  

1.  <span data-ttu-id="c3cff-209">Wählen Sie das **Tool Quellen** aus.</span><span class="sxs-lookup"><span data-stu-id="c3cff-209">Choose the **Sources** tool.</span></span>  
1.  <span data-ttu-id="c3cff-210">Wählen **Sie Pause für Ausnahmen** \( Pause für Ausnahmen ![ ](../media/pause-on-exceptions-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="c3cff-210">Choose **Pause on exceptions** \(![Pause on exceptions](../media/pause-on-exceptions-icon.msft.png)\).</span></span>  <span data-ttu-id="c3cff-211">Das Symbol wird blau, wenn es aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="c3cff-211">The icon turns blue when enabled.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-page-js-pause-on-exceptions.msft.png" alt-text="Die Schaltfläche Für Ausnahmen anhalten" lightbox="../media/javascript-sources-page-js-pause-on-exceptions.msft.png":::
       <span data-ttu-id="c3cff-213">Die **Schaltfläche Für Ausnahmen anhalten**</span><span class="sxs-lookup"><span data-stu-id="c3cff-213">The **Pause on exceptions** button</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="c3cff-214">**Optional**.</span><span class="sxs-lookup"><span data-stu-id="c3cff-214">**Optional**.</span></span>  <span data-ttu-id="c3cff-215">Aktivieren Sie das Kontrollkästchen Bei **erwischten Ausnahmen** anhalten, wenn Sie zusätzlich zu nicht abgefangenen Ausnahmen auch bei abgefangenen Ausnahmen anhalten möchten.</span><span class="sxs-lookup"><span data-stu-id="c3cff-215">Check the **Pause On Caught Exceptions** checkbox if you also want to pause on caught exceptions, in addition to uncaught ones.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-page-js-paused-on-exception.msft.png" alt-text="Angehalten für eine nicht abgefangene Ausnahme" lightbox="../media/javascript-sources-page-js-paused-on-exception.msft.png":::
       <span data-ttu-id="c3cff-217">Angehalten für eine nicht abgefangene Ausnahme</span><span class="sxs-lookup"><span data-stu-id="c3cff-217">Paused on an uncaught exception</span></span>  
    :::image-end:::  
    
## <a name="function-breakpoints"></a><span data-ttu-id="c3cff-218">Haltepunkte für Funktionen</span><span class="sxs-lookup"><span data-stu-id="c3cff-218">Function breakpoints</span></span>  

<span data-ttu-id="c3cff-219">Führen Sie die -Methode aus, wobei der Befehl, die Funktion oder die Methode ist, die Sie debuggen möchten, wenn Sie anhalten möchten, wenn eine bestimmte `debug(method)` `method` Funktion ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c3cff-219">Run the `debug(method)` method, where `method` is the command, function, or method you want to debug, when you want to pause whenever a specific function is run.</span></span>  <span data-ttu-id="c3cff-220">Sie können in Ihren Code (wie eine Anweisung) einfügen oder die Methode über die `debug()` `console.log()` DevTools-Konsole ausführen.</span><span class="sxs-lookup"><span data-stu-id="c3cff-220">You may insert `debug()` into your code (like a `console.log()` statement) or run the method from the DevTools Console.</span></span>  `debug()` <span data-ttu-id="c3cff-221">entspricht dem Festlegen eines [Codepunkts](#line-of-code-breakpoints) in der ersten Zeile der Funktion.</span><span class="sxs-lookup"><span data-stu-id="c3cff-221">is equivalent to setting a [line-of-code breakpoint](#line-of-code-breakpoints) on the first line of the function.</span></span>  

```javascript
function sum(a, b) {
    let result = a + b; // DevTools pauses on this line.
    return result;
}
debug(sum); // Pass the function object, not a string.
sum();
```  

### <a name="make-sure-the-target-function-is-in-scope"></a><span data-ttu-id="c3cff-222">Sicherstellen, dass sich die Zielfunktion im Bereich befindet</span><span class="sxs-lookup"><span data-stu-id="c3cff-222">Make sure the target function is in scope</span></span>  

<span data-ttu-id="c3cff-223">DevTools gibt eine `ReferenceError` aus, wenn sich die funktion, die Sie debuggen möchten, nicht im Bereich befindet.</span><span class="sxs-lookup"><span data-stu-id="c3cff-223">DevTools throws a `ReferenceError` if the function you want to debug is not in scope.</span></span>  

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

<span data-ttu-id="c3cff-224">Wenn Sie die Methode über die DevTools-Konsole ausführen, ist es schwierig sicherzustellen, dass sich die Zielfunktion im Bereich `debug()` befindet.</span><span class="sxs-lookup"><span data-stu-id="c3cff-224">Ensuring the target function is in scope is tricky if you are running the `debug()` method from the DevTools Console.</span></span>  <span data-ttu-id="c3cff-225">Hier ist eine Strategie:</span><span class="sxs-lookup"><span data-stu-id="c3cff-225">Here is one strategy:</span></span>  

1.  <span data-ttu-id="c3cff-226">Legen Sie [einen Codezeile-Haltepunkt](#line-of-code-breakpoints) an einer Stelle an, an der sich die Funktion im Bereich befindet.</span><span class="sxs-lookup"><span data-stu-id="c3cff-226">Set a [line-of-code breakpoint](#line-of-code-breakpoints) somewhere where the function is in scope.</span></span>
1.  <span data-ttu-id="c3cff-227">Lösen Sie den Haltepunkt aus.</span><span class="sxs-lookup"><span data-stu-id="c3cff-227">Trigger the breakpoint.</span></span>  
1.  <span data-ttu-id="c3cff-228">Führen Sie die Methode in der DevTools-Konsole aus, während der Code weiterhin an Ihrem `debug()` Codezeile-Haltepunkt angehalten wird.</span><span class="sxs-lookup"><span data-stu-id="c3cff-228">Run the `debug()` method in the DevTools Console while the code is still paused on your line-of-code breakpoint.</span></span>  
    
## <a name="related-articles"></a><span data-ttu-id="c3cff-229">Verwandte Artikel</span><span class="sxs-lookup"><span data-stu-id="c3cff-229">Related articles</span></span>

*   <span data-ttu-id="c3cff-230">[Verwenden der Debuggerfeatures][DevtoolsJavascriptReference] – Verwenden der Benutzeroberfläche des Debuggers im **Tool Sources.**</span><span class="sxs-lookup"><span data-stu-id="c3cff-230">[Use the debugger features][DevtoolsJavascriptReference] - Using the UI of the debugger in the **Sources** tool.</span></span>
*   <span data-ttu-id="c3cff-231">[Erste Schritte mit dem Debuggen von JavaScript in Microsoft Edge DevTools][DevtoolsJavascriptIndex] – Ein einführungstutorial mit einer vorhandenen Webseite.</span><span class="sxs-lookup"><span data-stu-id="c3cff-231">[Get started with debugging JavaScript in Microsoft Edge DevTools][DevtoolsJavascriptIndex] - An introductory tutorial using an existing webpage.</span></span>
*   <span data-ttu-id="c3cff-232">[Übersicht über das][DevtoolsSourcesIndex] Quellentool – Der Debugger ist Teil des **Sources-Tools,** das einen JavaScript-Editor enthält.</span><span class="sxs-lookup"><span data-stu-id="c3cff-232">[Sources tool overview][DevtoolsSourcesIndex] - The debugger is part of the **Sources** tool, which includes a JavaScript editor.</span></span>

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="c3cff-233">Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen</span><span class="sxs-lookup"><span data-stu-id="c3cff-233">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsJavascriptReference]: ./reference.md "Verwenden der Debuggerfeatures | Microsoft Docs"  

[DevtoolsJavascriptIndex]: index.md "Erste Schritte mit dem Debuggen von JavaScript in Microsoft Edge DevTools | Microsoft Docs"  

[DevtoolsSourcesIndex]: ../sources/index.md "Übersicht über das | Microsoft Docs"  

[MDNFetchApi]: https://developer.mozilla.org/docs/Web/API/Fetch_API "Abrufen von API-| MDN"  

> [!NOTE]
> <span data-ttu-id="c3cff-238">Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c3cff-238">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="c3cff-239">Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/javascript/breakpoints) und wird von [Kayce Basken][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\) verfasst.</span><span class="sxs-lookup"><span data-stu-id="c3cff-239">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/javascript/breakpoints) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="c3cff-241">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="c3cff-241">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  
