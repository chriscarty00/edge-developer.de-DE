---
description: Im Modus Zeitachsenereignisse werden alle Ereignisse angezeigt, die während der Aufzeichnung ausgelöst werden.  Verwenden Sie den Zeitachsen-Ereignisverweis, um mehr über die einzelnen Zeitachse-Ereignistypen zu erfahren.
title: Ereignisreferenz der Zeitachse
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: 624035636e2231cf1f3cd1e2ba0fdda7e2e4fa00
ms.sourcegitcommit: 63e6d34ff483f3b419a0e271a3513874e6ce6c79
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/02/2020
ms.locfileid: "10992848"
---
<!-- Copyright Meggin Kearney and Flavio Copes

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->





# <span data-ttu-id="99ab9-105">Ereignisreferenz der Zeitachse</span><span class="sxs-lookup"><span data-stu-id="99ab9-105">Timeline Event Reference</span></span>   




<span data-ttu-id="99ab9-106">Im Modus Zeitachsenereignisse werden alle Ereignisse angezeigt, die während der Aufzeichnung ausgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="99ab9-106">The timeline events mode displays all events triggered while making a recording.</span></span>  <span data-ttu-id="99ab9-107">Verwenden Sie den Zeitachsen-Ereignisverweis, um mehr über die einzelnen Zeitachse-Ereignistypen zu erfahren.</span><span class="sxs-lookup"><span data-stu-id="99ab9-107">Use the timeline event reference to learn more about each timeline event type.</span></span>  

## <span data-ttu-id="99ab9-108">Allgemeine zeitachsenereignis Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="99ab9-108">Common timeline event properties</span></span>  

<span data-ttu-id="99ab9-109">Bestimmte Details sind in Ereignissen aller Typen vorhanden, während einige nur für bestimmte Ereignistypen gelten.</span><span class="sxs-lookup"><span data-stu-id="99ab9-109">Certain details are present in events of all types, while some only apply to certain event types.</span></span>  <span data-ttu-id="99ab9-110">In diesem Abschnitt werden Eigenschaften aufgelistet, die für unterschiedliche Ereignistypen üblich sind.</span><span class="sxs-lookup"><span data-stu-id="99ab9-110">This section lists properties common to different event types.</span></span>  <span data-ttu-id="99ab9-111">Eigenschaften, die für bestimmte Ereignistypen spezifisch sind, werden in den verweisen für die folgenden Ereignistypen aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="99ab9-111">Properties specific to certain event types are listed in the references for those event types that follow.</span></span>  

| <span data-ttu-id="99ab9-112">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="99ab9-112">Property</span></span> | <span data-ttu-id="99ab9-113">Wann wird angezeigt</span><span class="sxs-lookup"><span data-stu-id="99ab9-113">When is it shown</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="99ab9-114">Aggregierte Zeit</span><span class="sxs-lookup"><span data-stu-id="99ab9-114">Aggregated time</span></span> | <span data-ttu-id="99ab9-115">Für Ereignisse mit **geschachtelten Ereignissen**die Zeit, die für jede Kategorie von Ereignissen übernommen wurde.</span><span class="sxs-lookup"><span data-stu-id="99ab9-115">For events with **nested events**, the time taken by each category of events.</span></span> |  
| <span data-ttu-id="99ab9-116">Aufrufliste</span><span class="sxs-lookup"><span data-stu-id="99ab9-116">Call Stack</span></span> | <span data-ttu-id="99ab9-117">Für Ereignisse mit **untergeordneten Ereignissen**die Zeit, die von jeder Kategorie von Ereignissen genommen wird.</span><span class="sxs-lookup"><span data-stu-id="99ab9-117">For events with **child events**, the time taken by each category of events.</span></span> |  
| <span data-ttu-id="99ab9-118">CPU-Zeit</span><span class="sxs-lookup"><span data-stu-id="99ab9-118">CPU time</span></span> | <span data-ttu-id="99ab9-119">Wie viel CPU-Zeit das aufgezeichnete Ereignis beansprucht hat.</span><span class="sxs-lookup"><span data-stu-id="99ab9-119">How much CPU time the recorded event took.</span></span> |  
| <span data-ttu-id="99ab9-120">Details</span><span class="sxs-lookup"><span data-stu-id="99ab9-120">Details</span></span> | <span data-ttu-id="99ab9-121">Weitere Details zum Ereignis.</span><span class="sxs-lookup"><span data-stu-id="99ab9-121">Other details about the event.</span></span> |  
| <span data-ttu-id="99ab9-122">Dauer \ (zum Zeitstempel \)</span><span class="sxs-lookup"><span data-stu-id="99ab9-122">Duration \(at time-stamp\)</span></span> | <span data-ttu-id="99ab9-123">Wie lange das Ereignis dauerte, bis alle untergeordneten Elemente abgeschlossen waren; timestamp ist der Zeitpunkt, zu dem das Ereignis aufgetreten ist, relativ zu dem Zeitpunkt, zu dem die Aufzeichnung gestartet wurde.</span><span class="sxs-lookup"><span data-stu-id="99ab9-123">How long it took the event with all of its children to complete; timestamp is the time at which the event occurred, relative to when the recording started.</span></span> |  
| <span data-ttu-id="99ab9-124">Selbst Zeit</span><span class="sxs-lookup"><span data-stu-id="99ab9-124">Self time</span></span> | <span data-ttu-id="99ab9-125">Die Dauer des Ereignisses ohne untergeordnete Elemente.</span><span class="sxs-lookup"><span data-stu-id="99ab9-125">How long the event took without any of its children.</span></span> |  
| <span data-ttu-id="99ab9-126">Verwendete Heapgröße</span><span class="sxs-lookup"><span data-stu-id="99ab9-126">Used Heap Size</span></span> | <span data-ttu-id="99ab9-127">Die Menge des Arbeitsspeichers, der von der Anwendung beim Aufzeichnen des Ereignisses verwendet wird, und die Änderung der verwendeten Heapgröße seit dem letzten Sampling in Delta \ (+/-\).</span><span class="sxs-lookup"><span data-stu-id="99ab9-127">Amount of memory being used by the application when the event was recorded, and the delta \(+/-\) change in used heap size since the last sampling.</span></span> |  

<!--todo: add nested and child events (timelinetool) section when available -->  

## <span data-ttu-id="99ab9-128">Laden von Ereignissen</span><span class="sxs-lookup"><span data-stu-id="99ab9-128">Loading events</span></span>  

<span data-ttu-id="99ab9-129">In diesem Abschnitt werden Ereignisse aufgelistet, die zu Lade Kategorie und deren Eigenschaften gehören.</span><span class="sxs-lookup"><span data-stu-id="99ab9-129">This section lists events that belong to Loading category and their properties.</span></span>  

| <span data-ttu-id="99ab9-130">Ereignis</span><span class="sxs-lookup"><span data-stu-id="99ab9-130">Event</span></span> | <span data-ttu-id="99ab9-131">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="99ab9-131">Description</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="99ab9-132">HTML analysieren</span><span class="sxs-lookup"><span data-stu-id="99ab9-132">Parse HTML</span></span> |  <span data-ttu-id="99ab9-133">Microsoft Edge hat den HTML-Analyse Algorithmus ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="99ab9-133">Microsoft Edge ran the HTML parsing algorithm.</span></span> |  
| <span data-ttu-id="99ab9-134">Fertig stellen des Ladens</span><span class="sxs-lookup"><span data-stu-id="99ab9-134">Finish Loading</span></span> |  <span data-ttu-id="99ab9-135">Eine Netzwerkanforderung wurde abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="99ab9-135">A network request completed.</span></span> |  
| <span data-ttu-id="99ab9-136">Empfangen von Daten</span><span class="sxs-lookup"><span data-stu-id="99ab9-136">Receive Data</span></span> |  <span data-ttu-id="99ab9-137">Die Daten für eine Anforderung wurden empfangen.</span><span class="sxs-lookup"><span data-stu-id="99ab9-137">Data for a request was received.</span></span>  <span data-ttu-id="99ab9-138">Es gibt mindestens ein Receive-Datenereignis.</span><span class="sxs-lookup"><span data-stu-id="99ab9-138">There are one or more Receive Data events.</span></span> |  
| <span data-ttu-id="99ab9-139">Antwort empfangen</span><span class="sxs-lookup"><span data-stu-id="99ab9-139">Receive Response</span></span> |  <span data-ttu-id="99ab9-140">Die anfängliche HTTP-Antwort einer Anforderung.</span><span class="sxs-lookup"><span data-stu-id="99ab9-140">The initial HTTP response from a request.</span></span> |  
| <span data-ttu-id="99ab9-141">Anfrage senden</span><span class="sxs-lookup"><span data-stu-id="99ab9-141">Send Request</span></span> |  <span data-ttu-id="99ab9-142">Eine Netzwerkanforderung wurde gesendet.</span><span class="sxs-lookup"><span data-stu-id="99ab9-142">A network request has been sent.</span></span> |  

### <span data-ttu-id="99ab9-143">Laden von Ereigniseigenschaften</span><span class="sxs-lookup"><span data-stu-id="99ab9-143">Loading event properties</span></span>  

| <span data-ttu-id="99ab9-144">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="99ab9-144">Property</span></span> | <span data-ttu-id="99ab9-145">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="99ab9-145">Description</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="99ab9-146">Ressource</span><span class="sxs-lookup"><span data-stu-id="99ab9-146">Resource</span></span> | <span data-ttu-id="99ab9-147">Die URL der angeforderten Ressource.</span><span class="sxs-lookup"><span data-stu-id="99ab9-147">The URL of the requested resource.</span></span> |  
| <span data-ttu-id="99ab9-148">Preview</span><span class="sxs-lookup"><span data-stu-id="99ab9-148">Preview</span></span> | <span data-ttu-id="99ab9-149">Vorschau der angeforderten Ressource \ (nur Bilder \).</span><span class="sxs-lookup"><span data-stu-id="99ab9-149">Preview of the requested resource \(images only\).</span></span> |  
| <span data-ttu-id="99ab9-150">Request-Methode</span><span class="sxs-lookup"><span data-stu-id="99ab9-150">Request Method</span></span> | <span data-ttu-id="99ab9-151">Die für die Anforderung verwendete HTTP-Methode \ ( `GET` oder Beispiels `POST` Weise \).</span><span class="sxs-lookup"><span data-stu-id="99ab9-151">HTTP method used for the request \(`GET` or `POST`, for example\).</span></span> |  
| <span data-ttu-id="99ab9-152">Status Code</span><span class="sxs-lookup"><span data-stu-id="99ab9-152">Status Code</span></span> | <span data-ttu-id="99ab9-153">HTTP-Antwortcode.</span><span class="sxs-lookup"><span data-stu-id="99ab9-153">HTTP response code.</span></span> |  
| <span data-ttu-id="99ab9-154">MIME-Typ</span><span class="sxs-lookup"><span data-stu-id="99ab9-154">MIME Type</span></span> | <span data-ttu-id="99ab9-155">Der MIME-Typ der angeforderten Ressource.</span><span class="sxs-lookup"><span data-stu-id="99ab9-155">MIME type of the requested resource.</span></span> |  
| <span data-ttu-id="99ab9-156">Codierte Datenlänge</span><span class="sxs-lookup"><span data-stu-id="99ab9-156">Encoded Data Length</span></span> | <span data-ttu-id="99ab9-157">Die Länge der angeforderten Ressource in Bytes.</span><span class="sxs-lookup"><span data-stu-id="99ab9-157">Length of requested resource in bytes.</span></span> |  

## <span data-ttu-id="99ab9-158">Skripting-Ereignisse</span><span class="sxs-lookup"><span data-stu-id="99ab9-158">Scripting events</span></span>  

<span data-ttu-id="99ab9-159">In diesem Abschnitt werden Ereignisse aufgelistet, die zu der Kategorie Skripting gehören, und deren Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="99ab9-159">This section lists events that belong to the Scripting category and their properties.</span></span>  

| <span data-ttu-id="99ab9-160">Ereignis</span><span class="sxs-lookup"><span data-stu-id="99ab9-160">Event</span></span> | <span data-ttu-id="99ab9-161">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="99ab9-161">Description</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="99ab9-162">Animations Frame gebrannt</span><span class="sxs-lookup"><span data-stu-id="99ab9-162">Animation Frame Fired</span></span> | <span data-ttu-id="99ab9-163">Ein geplanter Animationsframe wird ausgelöst, und der zugehörige Rückrufhandler wird aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="99ab9-163">A scheduled animation frame fired, and its callback handler invoked.</span></span> |  
| <span data-ttu-id="99ab9-164">Animations Frame Abbrechen</span><span class="sxs-lookup"><span data-stu-id="99ab9-164">Cancel Animation Frame</span></span> |  <span data-ttu-id="99ab9-165">Ein geplanter Animationsframe wurde abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="99ab9-165">A scheduled animation frame was canceled.</span></span> |  
| <span data-ttu-id="99ab9-166">GC-Ereignis</span><span class="sxs-lookup"><span data-stu-id="99ab9-166">GC Event</span></span> |  <span data-ttu-id="99ab9-167">Garbage Collection ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="99ab9-167">Garbage collection occurred.</span></span> |  
| <span data-ttu-id="99ab9-168">DOMContentLoaded</span><span class="sxs-lookup"><span data-stu-id="99ab9-168">DOMContentLoaded</span></span> |  <span data-ttu-id="99ab9-169">Das [DOMContentLoaded-Ereignis][MDNWindowDOMContentLoadedEvent] wurde vom Browser ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="99ab9-169">The [DOMContentLoaded event][MDNWindowDOMContentLoadedEvent] was fired by the browser.</span></span>  <span data-ttu-id="99ab9-170">Dieses Ereignis wird ausgelöst, wenn der gesamte Dom-Inhalt der Seite geladen und analysiert wurde.</span><span class="sxs-lookup"><span data-stu-id="99ab9-170">This event is fired when all of the page's DOM content has been loaded and parsed.</span></span> |  
| <span data-ttu-id="99ab9-171">Auswerten des Skripts</span><span class="sxs-lookup"><span data-stu-id="99ab9-171">Evaluate Script</span></span> | <span data-ttu-id="99ab9-172">Ein Skript wurde ausgewertet.</span><span class="sxs-lookup"><span data-stu-id="99ab9-172">A script was evaluated.</span></span> |  
| <span data-ttu-id="99ab9-173">Ereignis</span><span class="sxs-lookup"><span data-stu-id="99ab9-173">Event</span></span> | <span data-ttu-id="99ab9-174">Ein JavaScript-Ereignis \ (Beispiel: `mousedown` oder `key` \).</span><span class="sxs-lookup"><span data-stu-id="99ab9-174">A JavaScript event \(for example, `mousedown`, or `key`\).</span></span> |  
| <span data-ttu-id="99ab9-175">Funktionsaufruf</span><span class="sxs-lookup"><span data-stu-id="99ab9-175">Function Call</span></span> | <span data-ttu-id="99ab9-176">Es wurde ein JavaScript-Funktionsaufruf der obersten Ebene durchgeführt \ (wird nur angezeigt, wenn der Browser JavaScript-Modul wechselt).</span><span class="sxs-lookup"><span data-stu-id="99ab9-176">A top-level JavaScript function call was made \(only appears when browser enters JavaScript engine\).</span></span> |  
| <span data-ttu-id="99ab9-177">Timer installieren</span><span class="sxs-lookup"><span data-stu-id="99ab9-177">Install Timer</span></span> | <span data-ttu-id="99ab9-178">Ein Zeitgeber wurde mit [setInterval ()][MDNWindowOrWorkerGlobalScopeSetInterval] oder [setTimeout ()][MDNWindowOrWorkerGlobalScopeSetTimeout]erstellt.</span><span class="sxs-lookup"><span data-stu-id="99ab9-178">A timer was created with [setInterval()][MDNWindowOrWorkerGlobalScopeSetInterval] or [setTimeout()][MDNWindowOrWorkerGlobalScopeSetTimeout].</span></span> |  
| <span data-ttu-id="99ab9-179">Animationsrahmen anfordern</span><span class="sxs-lookup"><span data-stu-id="99ab9-179">Request Animation Frame</span></span> | <span data-ttu-id="99ab9-180">Ein `requestAnimationFrame()` Anruf hat einen neuen Frame geplant.</span><span class="sxs-lookup"><span data-stu-id="99ab9-180">A `requestAnimationFrame()` call scheduled a new frame.</span></span> |  
| <span data-ttu-id="99ab9-181">Timer entfernen</span><span class="sxs-lookup"><span data-stu-id="99ab9-181">Remove Timer</span></span> | <span data-ttu-id="99ab9-182">Ein zuvor erstellter Zeitgeber wurde gelöscht.</span><span class="sxs-lookup"><span data-stu-id="99ab9-182">A previously created timer was cleared.</span></span> |  
| <span data-ttu-id="99ab9-183">Zeit</span><span class="sxs-lookup"><span data-stu-id="99ab9-183">Time</span></span> |  <span data-ttu-id="99ab9-184">Ein Skript mit dem Namen [Console. time ()][ConsoleApiTime].</span><span class="sxs-lookup"><span data-stu-id="99ab9-184">A script called [console.time()][ConsoleApiTime].</span></span> |  
| <span data-ttu-id="99ab9-185">Endzeit</span><span class="sxs-lookup"><span data-stu-id="99ab9-185">Time End</span></span> | <span data-ttu-id="99ab9-186">Ein Skript mit dem Namen [Console. timeEnd ()][ConsoleApiTimeEnd].</span><span class="sxs-lookup"><span data-stu-id="99ab9-186">A script called [console.timeEnd()][ConsoleApiTimeEnd].</span></span> |  
| <span data-ttu-id="99ab9-187">Timer ausgelöst</span><span class="sxs-lookup"><span data-stu-id="99ab9-187">Timer Fired</span></span> | <span data-ttu-id="99ab9-188">Ein Timer, der mit oder geplant `setInterval()` wurde `setTimeout()` .</span><span class="sxs-lookup"><span data-stu-id="99ab9-188">A timer fired that was scheduled with `setInterval()` or `setTimeout()`.</span></span> |  
| <span data-ttu-id="99ab9-189">XMLHttpRequest Ready-Statusänderung</span><span class="sxs-lookup"><span data-stu-id="99ab9-189">XHR Ready State Change</span></span> | <span data-ttu-id="99ab9-190">Der Zustand "Ready" eines XMLHttpRequest wurde geändert.</span><span class="sxs-lookup"><span data-stu-id="99ab9-190">The ready state of an XMLHTTPRequest changed.</span></span> |  
| <span data-ttu-id="99ab9-191">XMLHttpRequest Load</span><span class="sxs-lookup"><span data-stu-id="99ab9-191">XHR Load</span></span> | <span data-ttu-id="99ab9-192">Ein `XMLHTTPRequest` beendeten Ladevorgang.</span><span class="sxs-lookup"><span data-stu-id="99ab9-192">An `XMLHTTPRequest` finished loading.</span></span> |  

### <span data-ttu-id="99ab9-193">Skripting-Ereigniseigenschaften</span><span class="sxs-lookup"><span data-stu-id="99ab9-193">Scripting event properties</span></span>  

| <span data-ttu-id="99ab9-194">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="99ab9-194">Property</span></span> | <span data-ttu-id="99ab9-195">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="99ab9-195">Description</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="99ab9-196">Timer-ID</span><span class="sxs-lookup"><span data-stu-id="99ab9-196">Timer ID</span></span> | <span data-ttu-id="99ab9-197">Die Timer-ID.</span><span class="sxs-lookup"><span data-stu-id="99ab9-197">The timer ID.</span></span> |  
| <span data-ttu-id="99ab9-198">Timeout</span><span class="sxs-lookup"><span data-stu-id="99ab9-198">Timeout</span></span> | <span data-ttu-id="99ab9-199">Das vom Zeitgeber angegebene Timeout.</span><span class="sxs-lookup"><span data-stu-id="99ab9-199">The timeout specified by the timer.</span></span> |  
| <span data-ttu-id="99ab9-200">Wiederholt</span><span class="sxs-lookup"><span data-stu-id="99ab9-200">Repeats</span></span> | <span data-ttu-id="99ab9-201">Boolescher Wert, der angibt, ob der Zeitgeber wiederholt wird.</span><span class="sxs-lookup"><span data-stu-id="99ab9-201">Boolean that specifies if the timer repeats.</span></span> |  
| <span data-ttu-id="99ab9-202">Funktionsaufruf</span><span class="sxs-lookup"><span data-stu-id="99ab9-202">Function Call</span></span> | <span data-ttu-id="99ab9-203">Eine Funktion, die aufgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="99ab9-203">A function that was invoked.</span></span> |  

## <span data-ttu-id="99ab9-204">Rendern von Ereignissen</span><span class="sxs-lookup"><span data-stu-id="99ab9-204">Rendering events</span></span>  

<span data-ttu-id="99ab9-205">In diesem Abschnitt werden Ereignisse aufgelistet, die zu einer Rendering-Kategorie und deren Eigenschaften gehören.</span><span class="sxs-lookup"><span data-stu-id="99ab9-205">This section lists events that belong to Rendering category and their properties.</span></span>  

| <span data-ttu-id="99ab9-206">Ereignis</span><span class="sxs-lookup"><span data-stu-id="99ab9-206">Event</span></span> | <span data-ttu-id="99ab9-207">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="99ab9-207">Description</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="99ab9-208">Ungültiges Layout</span><span class="sxs-lookup"><span data-stu-id="99ab9-208">Invalidate layout</span></span> | <span data-ttu-id="99ab9-209">Das Seitenlayout wurde durch eine DOM-Änderung ungültig.</span><span class="sxs-lookup"><span data-stu-id="99ab9-209">The page layout was invalidated by a DOM change.</span></span> |  
| <span data-ttu-id="99ab9-210">Layout</span><span class="sxs-lookup"><span data-stu-id="99ab9-210">Layout</span></span> | <span data-ttu-id="99ab9-211">Ein Seitenlayout wurde abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="99ab9-211">A page layout was completed.</span></span> |  
| <span data-ttu-id="99ab9-212">Neuberechnen des Formats</span><span class="sxs-lookup"><span data-stu-id="99ab9-212">Recalculate style</span></span> | <span data-ttu-id="99ab9-213">Neu berechnete Microsoft Edge-Element Formatvorlagen</span><span class="sxs-lookup"><span data-stu-id="99ab9-213">Microsoft Edge recalculated element styles.</span></span> |  
| <span data-ttu-id="99ab9-214">Scroll</span><span class="sxs-lookup"><span data-stu-id="99ab9-214">Scroll</span></span> | <span data-ttu-id="99ab9-215">Der Inhalt der geschachtelten Ansicht wurde gescrollt.</span><span class="sxs-lookup"><span data-stu-id="99ab9-215">The content of nested view was scrolled.</span></span> |  

### <span data-ttu-id="99ab9-216">Rendern von Ereigniseigenschaften</span><span class="sxs-lookup"><span data-stu-id="99ab9-216">Rendering event properties</span></span>  

| <span data-ttu-id="99ab9-217">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="99ab9-217">Property</span></span> | <span data-ttu-id="99ab9-218">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="99ab9-218">Description</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="99ab9-219">Layout ungültig</span><span class="sxs-lookup"><span data-stu-id="99ab9-219">Layout invalidated</span></span> | <span data-ttu-id="99ab9-220">Bei Layout-Datensätzen ist die Stapelüberwachung des Codes, der das Layout verursacht hat, ungültig.</span><span class="sxs-lookup"><span data-stu-id="99ab9-220">For Layout records, the stack trace of the code that caused the layout to be invalidated.</span></span> |  
| <span data-ttu-id="99ab9-221">Knoten, die Layout benötigen</span><span class="sxs-lookup"><span data-stu-id="99ab9-221">Nodes that need layout</span></span> | <span data-ttu-id="99ab9-222">Bei Layout-Datensätzen wird die Anzahl der Knoten, die vor dem Neulayout als Layout erforderlich markiert wurden, gestartet.</span><span class="sxs-lookup"><span data-stu-id="99ab9-222">For Layout records, the number of nodes that were marked as needing layout before the relayout started.</span></span>  <span data-ttu-id="99ab9-223">In der Regel handelt es sich um die Knoten, die vom Entwickler Code für ungültig erklärt wurden, sowie einen Pfad aufwärts zum Neulayout-Stamm.</span><span class="sxs-lookup"><span data-stu-id="99ab9-223">These are normally those nodes that were invalidated by developer code, plus a path upward to relayout root.</span></span> |  
| <span data-ttu-id="99ab9-224">Layout-Strukturgröße</span><span class="sxs-lookup"><span data-stu-id="99ab9-224">Layout tree size</span></span> | <span data-ttu-id="99ab9-225">Bei Layout-Datensätzen die Gesamtzahl der Knoten unter dem umlayout-Stamm \ (der Knoten, mit dem Microsoft Edge das Neulayout startet \).</span><span class="sxs-lookup"><span data-stu-id="99ab9-225">For Layout records, the total number of nodes under the relayout root \(the node that Microsoft Edge starts the relayout\).</span></span> |  
| <span data-ttu-id="99ab9-226">Bereich ' Layout '</span><span class="sxs-lookup"><span data-stu-id="99ab9-226">Layout scope</span></span> | <span data-ttu-id="99ab9-227">Mögliche Werte sind `Partial` \ (die Umgrenzung des Re-Layouts ist ein Teil des DOM \) oder `Whole document` .</span><span class="sxs-lookup"><span data-stu-id="99ab9-227">Possible values are `Partial` \(the re-layout boundary is a portion of the DOM\) or `Whole document`.</span></span> |  
| <span data-ttu-id="99ab9-228">Betroffene Elemente</span><span class="sxs-lookup"><span data-stu-id="99ab9-228">Elements affected</span></span> | <span data-ttu-id="99ab9-229">Zum Neuberechnen von Formatvorlagen Datensätzen die Anzahl der Elemente, die von einer Neuberechnung des Formats betroffen sind.</span><span class="sxs-lookup"><span data-stu-id="99ab9-229">For Recalculate style records, the number of elements affected by a style recalculation.</span></span> |  
| <span data-ttu-id="99ab9-230">Formatvorlagen ungültig</span><span class="sxs-lookup"><span data-stu-id="99ab9-230">Styles invalidated</span></span> | <span data-ttu-id="99ab9-231">Zum Neuberechnen von Formatvorlagen Datensätzen wird die Stapelüberwachung des Codes bereitgestellt, der die Formatvorlage ungültig wurde.</span><span class="sxs-lookup"><span data-stu-id="99ab9-231">For Recalculate style records, provides the stack trace of the code that caused the style invalidation.</span></span> |  

## <span data-ttu-id="99ab9-232">Malen von Ereignissen</span><span class="sxs-lookup"><span data-stu-id="99ab9-232">Painting events</span></span>  

<span data-ttu-id="99ab9-233">In diesem Abschnitt werden Ereignisse aufgelistet, die zur Kategorie "Malerei" und deren Eigenschaften gehören.</span><span class="sxs-lookup"><span data-stu-id="99ab9-233">This section lists events that belong to Painting category and their properties.</span></span>  

| <span data-ttu-id="99ab9-234">Ereignis</span><span class="sxs-lookup"><span data-stu-id="99ab9-234">Event</span></span> | <span data-ttu-id="99ab9-235">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="99ab9-235">Description</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="99ab9-236">Composite-Layer</span><span class="sxs-lookup"><span data-stu-id="99ab9-236">Composite Layers</span></span> | <span data-ttu-id="99ab9-237">Die zusammengesetzten Bildebenen für das Microsoft-Edge-Rendering-Modul</span><span class="sxs-lookup"><span data-stu-id="99ab9-237">The composited image layers for the Microsoft Edge rendering engine.</span></span> |  
| <span data-ttu-id="99ab9-238">Bild decodieren</span><span class="sxs-lookup"><span data-stu-id="99ab9-238">Image Decode</span></span> | <span data-ttu-id="99ab9-239">Eine Bildressource wurde dekodiert.</span><span class="sxs-lookup"><span data-stu-id="99ab9-239">An image resource was decoded.</span></span> |  
| <span data-ttu-id="99ab9-240">Bildgröße</span><span class="sxs-lookup"><span data-stu-id="99ab9-240">Image Resize</span></span> | <span data-ttu-id="99ab9-241">Die Größe eines Bilds wurde aus den systemeigenen Dimensionen geändert.</span><span class="sxs-lookup"><span data-stu-id="99ab9-241">An image was resized from its native dimensions.</span></span> |  
| <span data-ttu-id="99ab9-242">Paint</span><span class="sxs-lookup"><span data-stu-id="99ab9-242">Paint</span></span> | <span data-ttu-id="99ab9-243">Zusammengesetzte Ebenen wurden in einen Bereich der Anzeige gemalt.</span><span class="sxs-lookup"><span data-stu-id="99ab9-243">Composited layers were painted to a region of the display.</span></span>  <span data-ttu-id="99ab9-244">Wenn Sie den Mauszeiger über einen Paint-Eintrag bewegen, wird der Bereich der Anzeige, der aktualisiert wurde, hervorgehoben.</span><span class="sxs-lookup"><span data-stu-id="99ab9-244">Hovering over a Paint record highlights the region of the display that was updated.</span></span> |  

### <span data-ttu-id="99ab9-245">Zeichnen von Ereigniseigenschaften</span><span class="sxs-lookup"><span data-stu-id="99ab9-245">Painting event properties</span></span>  

| <span data-ttu-id="99ab9-246">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="99ab9-246">Property</span></span> | <span data-ttu-id="99ab9-247">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="99ab9-247">Description</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="99ab9-248">Pfad</span><span class="sxs-lookup"><span data-stu-id="99ab9-248">Location</span></span> | <span data-ttu-id="99ab9-249">Für Paint-Ereignisse die x-und y-Koordinaten des Paint-Rechtecks.</span><span class="sxs-lookup"><span data-stu-id="99ab9-249">For Paint events, the x and y coordinates of the paint rectangle.</span></span> |  
| <span data-ttu-id="99ab9-250">Dimensionen</span><span class="sxs-lookup"><span data-stu-id="99ab9-250">Dimensions</span></span> | <span data-ttu-id="99ab9-251">Für Paint-Ereignisse die Höhe und Breite des bemalten Bereichs.</span><span class="sxs-lookup"><span data-stu-id="99ab9-251">For Paint events, the height and width of the painted region.</span></span> |  

 



<!-- image links -->  

<!-- links -->

[ConsoleApiTime]: /microsoft-edge/devtools-guide-chromium/console/api#time "Referenz zur Zeit Konsolen-API"  
[ConsoleApiTimeEnd]: /microsoft-edge/devtools-guide-chromium/console/api#timeend "timeEnd-API-Referenz"  
<!--[EvaluatePerformanceTimelineTool]: timeline-tool "How to Use the Timeline Tool"  -->

[MDNWindowDOMContentLoadedEvent]: https://developer.mozilla.org/docs/Web/Events/DOMContentLoaded "Fenster: DOMContentLoaded-Ereignis | MDN"  
[MDNWindowOrWorkerGlobalScopeSetInterval]: https://developer.mozilla.org/docs/Web/API/WindowTimers/setInterval "WindowOrWorkerGlobalScope. setInterval () | MDN"  
[MDNWindowOrWorkerGlobalScopeSetTimeout]: https://developer.mozilla.org/docs/Web/API/WindowTimers/setTimeout "WindowOrWorkerGlobalScope. setTimeout () | MDN"  

> [!NOTE]
> <span data-ttu-id="99ab9-257">Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="99ab9-257">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="99ab9-258">Die ursprüngliche Seite wird [hier](https://developers.google.com/web/tools/chrome-devtools/evaluate-performance/performance-reference) gefunden und von [Meggin Kearney][MegginKearney] (Tech Writer \) und [Flavio Copes][FlavioCopes] \ (vollständiger Stack-Entwickler \) erstellt.</span><span class="sxs-lookup"><span data-stu-id="99ab9-258">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/evaluate-performance/performance-reference) and is authored by [Meggin Kearney][MegginKearney] \(Tech Writer\) and [Flavio Copes][FlavioCopes] \(Full Stack Developer\).</span></span>  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
<span data-ttu-id="99ab9-260">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="99ab9-260">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[MegginKearney]: https://developers.google.com/web/resources/contributors/megginkearney  
[FlavioCopes]: https://developers.google.com/web/resources/contributors/flaviocopes  
