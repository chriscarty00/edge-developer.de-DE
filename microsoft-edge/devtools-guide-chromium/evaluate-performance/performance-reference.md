---
title: Zeitachsenereignis Referenz
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/29/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Web-Entwicklung, F12-Tools, devtools
ms.openlocfilehash: e5f0807204877ce034fd52ea4535795ea80ba394
ms.sourcegitcommit: 50991a04c18283a8890ae33fcc3491c0476c7684
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/30/2020
ms.locfileid: "10611720"
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





# <span data-ttu-id="e75d6-103">Zeitachsenereignis Referenz</span><span class="sxs-lookup"><span data-stu-id="e75d6-103">Timeline Event Reference</span></span>   




<span data-ttu-id="e75d6-104">Im Modus Zeitachsenereignisse werden alle Ereignisse angezeigt, die während der Aufzeichnung ausgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="e75d6-104">The timeline events mode displays all events triggered while making a recording.</span></span>  <span data-ttu-id="e75d6-105">Verwenden Sie den Zeitachsen-Ereignisverweis, um mehr über die einzelnen Zeitachse-Ereignistypen zu erfahren.</span><span class="sxs-lookup"><span data-stu-id="e75d6-105">Use the timeline event reference to learn more about each timeline event type.</span></span>  

## <span data-ttu-id="e75d6-106">Allgemeine zeitachsenereignis Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e75d6-106">Common timeline event properties</span></span>  

<span data-ttu-id="e75d6-107">Bestimmte Details sind in Ereignissen aller Typen vorhanden, während einige nur für bestimmte Ereignistypen gelten.</span><span class="sxs-lookup"><span data-stu-id="e75d6-107">Certain details are present in events of all types, while some only apply to certain event types.</span></span>  <span data-ttu-id="e75d6-108">In diesem Abschnitt werden Eigenschaften aufgelistet, die für unterschiedliche Ereignistypen üblich sind.</span><span class="sxs-lookup"><span data-stu-id="e75d6-108">This section lists properties common to different event types.</span></span>  <span data-ttu-id="e75d6-109">Eigenschaften, die für bestimmte Ereignistypen spezifisch sind, werden in den verweisen für die folgenden Ereignistypen aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="e75d6-109">Properties specific to certain event types are listed in the references for those event types that follow.</span></span>  

| <span data-ttu-id="e75d6-110">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="e75d6-110">Property</span></span> | <span data-ttu-id="e75d6-111">Wann wird angezeigt</span><span class="sxs-lookup"><span data-stu-id="e75d6-111">When is it shown</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="e75d6-112">Aggregierte Zeit</span><span class="sxs-lookup"><span data-stu-id="e75d6-112">Aggregated time</span></span> | <span data-ttu-id="e75d6-113">Für Ereignisse mit **geschachtelten Ereignissen**die Zeit, die für jede Kategorie von Ereignissen übernommen wurde.</span><span class="sxs-lookup"><span data-stu-id="e75d6-113">For events with **nested events**, the time taken by each category of events.</span></span> |  
| <span data-ttu-id="e75d6-114">Aufrufliste</span><span class="sxs-lookup"><span data-stu-id="e75d6-114">Call Stack</span></span> | <span data-ttu-id="e75d6-115">Für Ereignisse mit **untergeordneten Ereignissen**die Zeit, die von jeder Kategorie von Ereignissen genommen wird.</span><span class="sxs-lookup"><span data-stu-id="e75d6-115">For events with **child events**, the time taken by each category of events.</span></span> |  
| <span data-ttu-id="e75d6-116">CPU-Zeit</span><span class="sxs-lookup"><span data-stu-id="e75d6-116">CPU time</span></span> | <span data-ttu-id="e75d6-117">Wie viel CPU-Zeit das aufgezeichnete Ereignis beansprucht hat.</span><span class="sxs-lookup"><span data-stu-id="e75d6-117">How much CPU time the recorded event took.</span></span> |  
| <span data-ttu-id="e75d6-118">Details</span><span class="sxs-lookup"><span data-stu-id="e75d6-118">Details</span></span> | <span data-ttu-id="e75d6-119">Weitere Details zum Ereignis.</span><span class="sxs-lookup"><span data-stu-id="e75d6-119">Other details about the event.</span></span> |  
| <span data-ttu-id="e75d6-120">Dauer \ (zum Zeitstempel \)</span><span class="sxs-lookup"><span data-stu-id="e75d6-120">Duration \(at time-stamp\)</span></span> | <span data-ttu-id="e75d6-121">Wie lange das Ereignis dauerte, bis alle untergeordneten Elemente abgeschlossen waren; timestamp ist der Zeitpunkt, zu dem das Ereignis aufgetreten ist, relativ zu dem Zeitpunkt, zu dem die Aufzeichnung gestartet wurde.</span><span class="sxs-lookup"><span data-stu-id="e75d6-121">How long it took the event with all of its children to complete; timestamp is the time at which the event occurred, relative to when the recording started.</span></span> |  
| <span data-ttu-id="e75d6-122">Selbst Zeit</span><span class="sxs-lookup"><span data-stu-id="e75d6-122">Self time</span></span> | <span data-ttu-id="e75d6-123">Die Dauer des Ereignisses ohne untergeordnete Elemente.</span><span class="sxs-lookup"><span data-stu-id="e75d6-123">How long the event took without any of its children.</span></span> |  
| <span data-ttu-id="e75d6-124">Verwendete Heapgröße</span><span class="sxs-lookup"><span data-stu-id="e75d6-124">Used Heap Size</span></span> | <span data-ttu-id="e75d6-125">Die Menge des Arbeitsspeichers, der von der Anwendung beim Aufzeichnen des Ereignisses verwendet wird, und die Änderung der verwendeten Heapgröße seit dem letzten Sampling in Delta \ (+/-\).</span><span class="sxs-lookup"><span data-stu-id="e75d6-125">Amount of memory being used by the application when the event was recorded, and the delta \(+/-\) change in used heap size since the last sampling.</span></span> |  

<!--todo: add nested and child events (timelinetool) section when available -->  

## <span data-ttu-id="e75d6-126">Laden von Ereignissen</span><span class="sxs-lookup"><span data-stu-id="e75d6-126">Loading events</span></span>  

<span data-ttu-id="e75d6-127">In diesem Abschnitt werden Ereignisse aufgelistet, die zu Lade Kategorie und deren Eigenschaften gehören.</span><span class="sxs-lookup"><span data-stu-id="e75d6-127">This section lists events that belong to Loading category and their properties.</span></span>  

| <span data-ttu-id="e75d6-128">Ereignis</span><span class="sxs-lookup"><span data-stu-id="e75d6-128">Event</span></span> | <span data-ttu-id="e75d6-129">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e75d6-129">Description</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="e75d6-130">HTML analysieren</span><span class="sxs-lookup"><span data-stu-id="e75d6-130">Parse HTML</span></span> |  <span data-ttu-id="e75d6-131">Microsoft Edge hat den HTML-Analyse Algorithmus ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e75d6-131">Microsoft Edge ran the HTML parsing algorithm.</span></span> |  
| <span data-ttu-id="e75d6-132">Fertig stellen des Ladens</span><span class="sxs-lookup"><span data-stu-id="e75d6-132">Finish Loading</span></span> |  <span data-ttu-id="e75d6-133">Eine Netzwerkanforderung wurde abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="e75d6-133">A network request completed.</span></span> |  
| <span data-ttu-id="e75d6-134">Empfangen von Daten</span><span class="sxs-lookup"><span data-stu-id="e75d6-134">Receive Data</span></span> |  <span data-ttu-id="e75d6-135">Die Daten für eine Anforderung wurden empfangen.</span><span class="sxs-lookup"><span data-stu-id="e75d6-135">Data for a request was received.</span></span>  <span data-ttu-id="e75d6-136">Es gibt mindestens ein Receive-Datenereignis.</span><span class="sxs-lookup"><span data-stu-id="e75d6-136">There are one or more Receive Data events.</span></span> |  
| <span data-ttu-id="e75d6-137">Antwort empfangen</span><span class="sxs-lookup"><span data-stu-id="e75d6-137">Receive Response</span></span> |  <span data-ttu-id="e75d6-138">Die anfängliche HTTP-Antwort einer Anforderung.</span><span class="sxs-lookup"><span data-stu-id="e75d6-138">The initial HTTP response from a request.</span></span> |  
| <span data-ttu-id="e75d6-139">Anfrage senden</span><span class="sxs-lookup"><span data-stu-id="e75d6-139">Send Request</span></span> |  <span data-ttu-id="e75d6-140">Eine Netzwerkanforderung wurde gesendet.</span><span class="sxs-lookup"><span data-stu-id="e75d6-140">A network request has been sent.</span></span> |  

### <span data-ttu-id="e75d6-141">Laden von Ereigniseigenschaften</span><span class="sxs-lookup"><span data-stu-id="e75d6-141">Loading event properties</span></span>  

| <span data-ttu-id="e75d6-142">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="e75d6-142">Property</span></span> | <span data-ttu-id="e75d6-143">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e75d6-143">Description</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="e75d6-144">Ressource</span><span class="sxs-lookup"><span data-stu-id="e75d6-144">Resource</span></span> | <span data-ttu-id="e75d6-145">Die URL der angeforderten Ressource.</span><span class="sxs-lookup"><span data-stu-id="e75d6-145">The URL of the requested resource.</span></span> |  
| <span data-ttu-id="e75d6-146">Preview</span><span class="sxs-lookup"><span data-stu-id="e75d6-146">Preview</span></span> | <span data-ttu-id="e75d6-147">Vorschau der angeforderten Ressource \ (nur Bilder \).</span><span class="sxs-lookup"><span data-stu-id="e75d6-147">Preview of the requested resource \(images only\).</span></span> |  
| <span data-ttu-id="e75d6-148">Request-Methode</span><span class="sxs-lookup"><span data-stu-id="e75d6-148">Request Method</span></span> | <span data-ttu-id="e75d6-149">Die für die Anforderung verwendete HTTP-Methode \ ( `GET` oder Beispiels `POST` Weise \).</span><span class="sxs-lookup"><span data-stu-id="e75d6-149">HTTP method used for the request \(`GET` or `POST`, for example\).</span></span> |  
| <span data-ttu-id="e75d6-150">Status Code</span><span class="sxs-lookup"><span data-stu-id="e75d6-150">Status Code</span></span> | <span data-ttu-id="e75d6-151">HTTP-Antwortcode.</span><span class="sxs-lookup"><span data-stu-id="e75d6-151">HTTP response code.</span></span> |  
| <span data-ttu-id="e75d6-152">MIME-Typ</span><span class="sxs-lookup"><span data-stu-id="e75d6-152">MIME Type</span></span> | <span data-ttu-id="e75d6-153">Der MIME-Typ der angeforderten Ressource.</span><span class="sxs-lookup"><span data-stu-id="e75d6-153">MIME type of the requested resource.</span></span> |  
| <span data-ttu-id="e75d6-154">Codierte Datenlänge</span><span class="sxs-lookup"><span data-stu-id="e75d6-154">Encoded Data Length</span></span> | <span data-ttu-id="e75d6-155">Die Länge der angeforderten Ressource in Bytes.</span><span class="sxs-lookup"><span data-stu-id="e75d6-155">Length of requested resource in bytes.</span></span> |  

## <span data-ttu-id="e75d6-156">Skripting-Ereignisse</span><span class="sxs-lookup"><span data-stu-id="e75d6-156">Scripting events</span></span>  

<span data-ttu-id="e75d6-157">In diesem Abschnitt werden Ereignisse aufgelistet, die zu der Kategorie Skripting gehören, und deren Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="e75d6-157">This section lists events that belong to the Scripting category and their properties.</span></span>  

| <span data-ttu-id="e75d6-158">Ereignis</span><span class="sxs-lookup"><span data-stu-id="e75d6-158">Event</span></span> | <span data-ttu-id="e75d6-159">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e75d6-159">Description</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="e75d6-160">Animations Frame gebrannt</span><span class="sxs-lookup"><span data-stu-id="e75d6-160">Animation Frame Fired</span></span> | <span data-ttu-id="e75d6-161">Ein geplanter Animationsframe wird ausgelöst, und der zugehörige Rückrufhandler wird aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="e75d6-161">A scheduled animation frame fired, and its callback handler invoked.</span></span> |  
| <span data-ttu-id="e75d6-162">Animations Frame Abbrechen</span><span class="sxs-lookup"><span data-stu-id="e75d6-162">Cancel Animation Frame</span></span> |  <span data-ttu-id="e75d6-163">Ein geplanter Animationsframe wurde abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="e75d6-163">A scheduled animation frame was canceled.</span></span> |  
| <span data-ttu-id="e75d6-164">GC-Ereignis</span><span class="sxs-lookup"><span data-stu-id="e75d6-164">GC Event</span></span> |  <span data-ttu-id="e75d6-165">Garbage Collection ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="e75d6-165">Garbage collection occurred.</span></span> |  
| <span data-ttu-id="e75d6-166">DOMContentLoaded</span><span class="sxs-lookup"><span data-stu-id="e75d6-166">DOMContentLoaded</span></span> |  <span data-ttu-id="e75d6-167">Das [DOMContentLoaded-Ereignis][MDNWindowDOMContentLoadedEvent] wurde vom Browser ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="e75d6-167">The [DOMContentLoaded event][MDNWindowDOMContentLoadedEvent] was fired by the browser.</span></span>  <span data-ttu-id="e75d6-168">Dieses Ereignis wird ausgelöst, wenn der gesamte Dom-Inhalt der Seite geladen und analysiert wurde.</span><span class="sxs-lookup"><span data-stu-id="e75d6-168">This event is fired when all of the page's DOM content has been loaded and parsed.</span></span> |  
| <span data-ttu-id="e75d6-169">Auswerten des Skripts</span><span class="sxs-lookup"><span data-stu-id="e75d6-169">Evaluate Script</span></span> | <span data-ttu-id="e75d6-170">Ein Skript wurde ausgewertet.</span><span class="sxs-lookup"><span data-stu-id="e75d6-170">A script was evaluated.</span></span> |  
| <span data-ttu-id="e75d6-171">Ereignis</span><span class="sxs-lookup"><span data-stu-id="e75d6-171">Event</span></span> | <span data-ttu-id="e75d6-172">Ein JavaScript-Ereignis \ (Beispiel: `mousedown` oder `key` \).</span><span class="sxs-lookup"><span data-stu-id="e75d6-172">A JavaScript event \(for example, `mousedown`, or `key`\).</span></span> |  
| <span data-ttu-id="e75d6-173">Funktionsaufruf</span><span class="sxs-lookup"><span data-stu-id="e75d6-173">Function Call</span></span> | <span data-ttu-id="e75d6-174">Es wurde ein JavaScript-Funktionsaufruf der obersten Ebene durchgeführt \ (wird nur angezeigt, wenn der Browser JavaScript-Modul wechselt).</span><span class="sxs-lookup"><span data-stu-id="e75d6-174">A top-level JavaScript function call was made \(only appears when browser enters JavaScript engine\).</span></span> |  
| <span data-ttu-id="e75d6-175">Timer installieren</span><span class="sxs-lookup"><span data-stu-id="e75d6-175">Install Timer</span></span> | <span data-ttu-id="e75d6-176">Ein Zeitgeber wurde mit [setInterval ()][MDNWindowOrWorkerGlobalScopeSetInterval] oder [setTimeout ()][MDNWindowOrWorkerGlobalScopeSetTimeout]erstellt.</span><span class="sxs-lookup"><span data-stu-id="e75d6-176">A timer was created with [setInterval()][MDNWindowOrWorkerGlobalScopeSetInterval] or [setTimeout()][MDNWindowOrWorkerGlobalScopeSetTimeout].</span></span> |  
| <span data-ttu-id="e75d6-177">Animationsrahmen anfordern</span><span class="sxs-lookup"><span data-stu-id="e75d6-177">Request Animation Frame</span></span> | <span data-ttu-id="e75d6-178">Ein `requestAnimationFrame()` Anruf hat einen neuen Frame geplant.</span><span class="sxs-lookup"><span data-stu-id="e75d6-178">A `requestAnimationFrame()` call scheduled a new frame.</span></span> |  
| <span data-ttu-id="e75d6-179">Timer entfernen</span><span class="sxs-lookup"><span data-stu-id="e75d6-179">Remove Timer</span></span> | <span data-ttu-id="e75d6-180">Ein zuvor erstellter Zeitgeber wurde gelöscht.</span><span class="sxs-lookup"><span data-stu-id="e75d6-180">A previously created timer was cleared.</span></span> |  
| <span data-ttu-id="e75d6-181">Zeit</span><span class="sxs-lookup"><span data-stu-id="e75d6-181">Time</span></span> |  <span data-ttu-id="e75d6-182">Ein Skript mit dem Namen [Console. time ()][ConsoleApiTime].</span><span class="sxs-lookup"><span data-stu-id="e75d6-182">A script called [console.time()][ConsoleApiTime].</span></span> |  
| <span data-ttu-id="e75d6-183">Endzeit</span><span class="sxs-lookup"><span data-stu-id="e75d6-183">Time End</span></span> | <span data-ttu-id="e75d6-184">Ein Skript mit dem Namen [Console. timeEnd ()][ConsoleApiTimeEnd].</span><span class="sxs-lookup"><span data-stu-id="e75d6-184">A script called [console.timeEnd()][ConsoleApiTimeEnd].</span></span> |  
| <span data-ttu-id="e75d6-185">Timer ausgelöst</span><span class="sxs-lookup"><span data-stu-id="e75d6-185">Timer Fired</span></span> | <span data-ttu-id="e75d6-186">Ein Timer, der mit oder geplant `setInterval()` wurde `setTimeout()` .</span><span class="sxs-lookup"><span data-stu-id="e75d6-186">A timer fired that was scheduled with `setInterval()` or `setTimeout()`.</span></span> |  
| <span data-ttu-id="e75d6-187">XMLHttpRequest Ready-Statusänderung</span><span class="sxs-lookup"><span data-stu-id="e75d6-187">XHR Ready State Change</span></span> | <span data-ttu-id="e75d6-188">Der Zustand "Ready" eines XMLHttpRequest wurde geändert.</span><span class="sxs-lookup"><span data-stu-id="e75d6-188">The ready state of an XMLHTTPRequest changed.</span></span> |  
| <span data-ttu-id="e75d6-189">XMLHttpRequest Load</span><span class="sxs-lookup"><span data-stu-id="e75d6-189">XHR Load</span></span> | <span data-ttu-id="e75d6-190">Ein `XMLHTTPRequest` beendeten Ladevorgang.</span><span class="sxs-lookup"><span data-stu-id="e75d6-190">An `XMLHTTPRequest` finished loading.</span></span> |  

### <span data-ttu-id="e75d6-191">Skripting-Ereigniseigenschaften</span><span class="sxs-lookup"><span data-stu-id="e75d6-191">Scripting event properties</span></span>  

| <span data-ttu-id="e75d6-192">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="e75d6-192">Property</span></span> | <span data-ttu-id="e75d6-193">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e75d6-193">Description</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="e75d6-194">Timer-ID</span><span class="sxs-lookup"><span data-stu-id="e75d6-194">Timer ID</span></span> | <span data-ttu-id="e75d6-195">Die Timer-ID.</span><span class="sxs-lookup"><span data-stu-id="e75d6-195">The timer ID.</span></span> |  
| <span data-ttu-id="e75d6-196">Timeout</span><span class="sxs-lookup"><span data-stu-id="e75d6-196">Timeout</span></span> | <span data-ttu-id="e75d6-197">Das vom Zeitgeber angegebene Timeout.</span><span class="sxs-lookup"><span data-stu-id="e75d6-197">The timeout specified by the timer.</span></span> |  
| <span data-ttu-id="e75d6-198">Wiederholt</span><span class="sxs-lookup"><span data-stu-id="e75d6-198">Repeats</span></span> | <span data-ttu-id="e75d6-199">Boolescher Wert, der angibt, ob der Zeitgeber wiederholt wird.</span><span class="sxs-lookup"><span data-stu-id="e75d6-199">Boolean that specifies if the timer repeats.</span></span> |  
| <span data-ttu-id="e75d6-200">Funktionsaufruf</span><span class="sxs-lookup"><span data-stu-id="e75d6-200">Function Call</span></span> | <span data-ttu-id="e75d6-201">Eine Funktion, die aufgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="e75d6-201">A function that was invoked.</span></span> |  

## <span data-ttu-id="e75d6-202">Rendern von Ereignissen</span><span class="sxs-lookup"><span data-stu-id="e75d6-202">Rendering events</span></span>  

<span data-ttu-id="e75d6-203">In diesem Abschnitt werden Ereignisse aufgelistet, die zu einer Rendering-Kategorie und deren Eigenschaften gehören.</span><span class="sxs-lookup"><span data-stu-id="e75d6-203">This section lists events that belong to Rendering category and their properties.</span></span>  

| <span data-ttu-id="e75d6-204">Ereignis</span><span class="sxs-lookup"><span data-stu-id="e75d6-204">Event</span></span> | <span data-ttu-id="e75d6-205">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e75d6-205">Description</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="e75d6-206">Ungültiges Layout</span><span class="sxs-lookup"><span data-stu-id="e75d6-206">Invalidate layout</span></span> | <span data-ttu-id="e75d6-207">Das Seitenlayout wurde durch eine DOM-Änderung ungültig.</span><span class="sxs-lookup"><span data-stu-id="e75d6-207">The page layout was invalidated by a DOM change.</span></span> |  
| <span data-ttu-id="e75d6-208">Layout</span><span class="sxs-lookup"><span data-stu-id="e75d6-208">Layout</span></span> | <span data-ttu-id="e75d6-209">Ein Seitenlayout wurde abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="e75d6-209">A page layout was completed.</span></span> |  
| <span data-ttu-id="e75d6-210">Neuberechnen des Formats</span><span class="sxs-lookup"><span data-stu-id="e75d6-210">Recalculate style</span></span> | <span data-ttu-id="e75d6-211">Neu berechnete Microsoft Edge-Element Formatvorlagen</span><span class="sxs-lookup"><span data-stu-id="e75d6-211">Microsoft Edge recalculated element styles.</span></span> |  
| <span data-ttu-id="e75d6-212">Scroll</span><span class="sxs-lookup"><span data-stu-id="e75d6-212">Scroll</span></span> | <span data-ttu-id="e75d6-213">Der Inhalt der geschachtelten Ansicht wurde gescrollt.</span><span class="sxs-lookup"><span data-stu-id="e75d6-213">The content of nested view was scrolled.</span></span> |  

### <span data-ttu-id="e75d6-214">Rendern von Ereigniseigenschaften</span><span class="sxs-lookup"><span data-stu-id="e75d6-214">Rendering event properties</span></span>  

| <span data-ttu-id="e75d6-215">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="e75d6-215">Property</span></span> | <span data-ttu-id="e75d6-216">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e75d6-216">Description</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="e75d6-217">Layout ungültig</span><span class="sxs-lookup"><span data-stu-id="e75d6-217">Layout invalidated</span></span> | <span data-ttu-id="e75d6-218">Bei Layout-Datensätzen ist die Stapelüberwachung des Codes, der das Layout verursacht hat, ungültig.</span><span class="sxs-lookup"><span data-stu-id="e75d6-218">For Layout records, the stack trace of the code that caused the layout to be invalidated.</span></span> |  
| <span data-ttu-id="e75d6-219">Knoten, die Layout benötigen</span><span class="sxs-lookup"><span data-stu-id="e75d6-219">Nodes that need layout</span></span> | <span data-ttu-id="e75d6-220">Bei Layout-Datensätzen wird die Anzahl der Knoten, die vor dem Neulayout als Layout erforderlich markiert wurden, gestartet.</span><span class="sxs-lookup"><span data-stu-id="e75d6-220">For Layout records, the number of nodes that were marked as needing layout before the relayout started.</span></span>  <span data-ttu-id="e75d6-221">In der Regel handelt es sich um die Knoten, die vom Entwickler Code für ungültig erklärt wurden, sowie einen Pfad aufwärts zum Neulayout-Stamm.</span><span class="sxs-lookup"><span data-stu-id="e75d6-221">These are normally those nodes that were invalidated by developer code, plus a path upward to relayout root.</span></span> |  
| <span data-ttu-id="e75d6-222">Layout-Strukturgröße</span><span class="sxs-lookup"><span data-stu-id="e75d6-222">Layout tree size</span></span> | <span data-ttu-id="e75d6-223">Bei Layout-Datensätzen die Gesamtzahl der Knoten unter dem umlayout-Stamm \ (der Knoten, mit dem Microsoft Edge das Neulayout startet \).</span><span class="sxs-lookup"><span data-stu-id="e75d6-223">For Layout records, the total number of nodes under the relayout root \(the node that Microsoft Edge starts the relayout\).</span></span> |  
| <span data-ttu-id="e75d6-224">Bereich ' Layout '</span><span class="sxs-lookup"><span data-stu-id="e75d6-224">Layout scope</span></span> | <span data-ttu-id="e75d6-225">Mögliche Werte sind `Partial` \ (die Umgrenzung des Re-Layouts ist ein Teil des DOM \) oder `Whole document` .</span><span class="sxs-lookup"><span data-stu-id="e75d6-225">Possible values are `Partial` \(the re-layout boundary is a portion of the DOM\) or `Whole document`.</span></span> |  
| <span data-ttu-id="e75d6-226">Betroffene Elemente</span><span class="sxs-lookup"><span data-stu-id="e75d6-226">Elements affected</span></span> | <span data-ttu-id="e75d6-227">Zum Neuberechnen von Formatvorlagen Datensätzen die Anzahl der Elemente, die von einer Neuberechnung des Formats betroffen sind.</span><span class="sxs-lookup"><span data-stu-id="e75d6-227">For Recalculate style records, the number of elements affected by a style recalculation.</span></span> |  
| <span data-ttu-id="e75d6-228">Formatvorlagen ungültig</span><span class="sxs-lookup"><span data-stu-id="e75d6-228">Styles invalidated</span></span> | <span data-ttu-id="e75d6-229">Zum Neuberechnen von Formatvorlagen Datensätzen wird die Stapelüberwachung des Codes bereitgestellt, der die Formatvorlage ungültig wurde.</span><span class="sxs-lookup"><span data-stu-id="e75d6-229">For Recalculate style records, provides the stack trace of the code that caused the style invalidation.</span></span> |  

## <span data-ttu-id="e75d6-230">Malen von Ereignissen</span><span class="sxs-lookup"><span data-stu-id="e75d6-230">Painting events</span></span>  

<span data-ttu-id="e75d6-231">In diesem Abschnitt werden Ereignisse aufgelistet, die zur Kategorie "Malerei" und deren Eigenschaften gehören.</span><span class="sxs-lookup"><span data-stu-id="e75d6-231">This section lists events that belong to Painting category and their properties.</span></span>  

| <span data-ttu-id="e75d6-232">Ereignis</span><span class="sxs-lookup"><span data-stu-id="e75d6-232">Event</span></span> | <span data-ttu-id="e75d6-233">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e75d6-233">Description</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="e75d6-234">Composite-Layer</span><span class="sxs-lookup"><span data-stu-id="e75d6-234">Composite Layers</span></span> | <span data-ttu-id="e75d6-235">Die zusammengesetzten Bildebenen für das Microsoft-Edge-Rendering-Modul</span><span class="sxs-lookup"><span data-stu-id="e75d6-235">The composited image layers for the Microsoft Edge rendering engine.</span></span> |  
| <span data-ttu-id="e75d6-236">Bild decodieren</span><span class="sxs-lookup"><span data-stu-id="e75d6-236">Image Decode</span></span> | <span data-ttu-id="e75d6-237">Eine Bildressource wurde dekodiert.</span><span class="sxs-lookup"><span data-stu-id="e75d6-237">An image resource was decoded.</span></span> |  
| <span data-ttu-id="e75d6-238">Bildgröße</span><span class="sxs-lookup"><span data-stu-id="e75d6-238">Image Resize</span></span> | <span data-ttu-id="e75d6-239">Die Größe eines Bilds wurde aus den systemeigenen Dimensionen geändert.</span><span class="sxs-lookup"><span data-stu-id="e75d6-239">An image was resized from its native dimensions.</span></span> |  
| <span data-ttu-id="e75d6-240">Paint</span><span class="sxs-lookup"><span data-stu-id="e75d6-240">Paint</span></span> | <span data-ttu-id="e75d6-241">Zusammengesetzte Ebenen wurden in einen Bereich der Anzeige gemalt.</span><span class="sxs-lookup"><span data-stu-id="e75d6-241">Composited layers were painted to a region of the display.</span></span>  <span data-ttu-id="e75d6-242">Wenn Sie den Mauszeiger über einen Paint-Eintrag bewegen, wird der Bereich der Anzeige, der aktualisiert wurde, hervorgehoben.</span><span class="sxs-lookup"><span data-stu-id="e75d6-242">Hovering over a Paint record highlights the region of the display that was updated.</span></span> |  

### <span data-ttu-id="e75d6-243">Zeichnen von Ereigniseigenschaften</span><span class="sxs-lookup"><span data-stu-id="e75d6-243">Painting event properties</span></span>  

| <span data-ttu-id="e75d6-244">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="e75d6-244">Property</span></span> | <span data-ttu-id="e75d6-245">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e75d6-245">Description</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="e75d6-246">Speicherort</span><span class="sxs-lookup"><span data-stu-id="e75d6-246">Location</span></span> | <span data-ttu-id="e75d6-247">Für Paint-Ereignisse die x-und y-Koordinaten des Paint-Rechtecks.</span><span class="sxs-lookup"><span data-stu-id="e75d6-247">For Paint events, the x and y coordinates of the paint rectangle.</span></span> |  
| <span data-ttu-id="e75d6-248">Dimensionen</span><span class="sxs-lookup"><span data-stu-id="e75d6-248">Dimensions</span></span> | <span data-ttu-id="e75d6-249">Für Paint-Ereignisse die Höhe und Breite des bemalten Bereichs.</span><span class="sxs-lookup"><span data-stu-id="e75d6-249">For Paint events, the height and width of the painted region.</span></span> |  

 



<!-- image links -->  

<!-- links -->

[ConsoleApiTime]: /microsoft-edge/devtools-guide-chromium/console/api#time "Referenz zur Zeit Konsolen-API"  
[ConsoleApiTimeEnd]: /microsoft-edge/devtools-guide-chromium/console/api#timeend "timeEnd-API-Referenz"  
<!--[EvaluatePerformanceTimelineTool]: timeline-tool "How to Use the Timeline Tool"  -->

[MDNWindowDOMContentLoadedEvent]: https://developer.mozilla.org/docs/Web/Events/DOMContentLoaded "Fenster: DOMContentLoaded-Ereignis | MDN"  
[MDNWindowOrWorkerGlobalScopeSetInterval]: https://developer.mozilla.org/docs/Web/API/WindowTimers/setInterval "WindowOrWorkerGlobalScope. setInterval () | MDN"  
[MDNWindowOrWorkerGlobalScopeSetTimeout]: https://developer.mozilla.org/docs/Web/API/WindowTimers/setTimeout "WindowOrWorkerGlobalScope. setTimeout () | MDN"  

> [!NOTE]
> <span data-ttu-id="e75d6-255">Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e75d6-255">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="e75d6-256">Die ursprüngliche Seite wird [hier](https://developers.google.com/web/tools/chrome-devtools/evaluate-performance/performance-reference) gefunden und von [Meggin Kearney][MegginKearney] (Tech Writer \) und [Flavio Copes][FlavioCopes] \ (vollständiger Stack-Entwickler \) erstellt.</span><span class="sxs-lookup"><span data-stu-id="e75d6-256">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/evaluate-performance/performance-reference) and is authored by [Meggin Kearney][MegginKearney] \(Tech Writer\) and [Flavio Copes][FlavioCopes] \(Full Stack Developer\).</span></span>  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
<span data-ttu-id="e75d6-258">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="e75d6-258">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[MegginKearney]: https://developers.google.com/web/resources/contributors/megginkearney  
[FlavioCopes]: https://developers.google.com/web/resources/contributors/flaviocopes  
