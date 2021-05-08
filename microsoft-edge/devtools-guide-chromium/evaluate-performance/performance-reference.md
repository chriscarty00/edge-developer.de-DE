---
description: Im Zeitachsenereignissemodus werden alle Ereignisse angezeigt, die während der Aufzeichnung ausgelöst werden.  Verwenden Sie den Zeitachsenereignisverweis, um mehr über jeden Zeitachsenereignistyp zu erfahren.
title: Zeitachsenereignisreferenz
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, Entwicklungstools
ms.openlocfilehash: 2a166c9eebc980682fa872e5ee8d213f2058b384
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398665"
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

# <a name="timeline-event-reference"></a><span data-ttu-id="8e0ea-105">Zeitachsenereignisreferenz</span><span class="sxs-lookup"><span data-stu-id="8e0ea-105">Timeline Event reference</span></span>  

<span data-ttu-id="8e0ea-106">Im Zeitachsenereignissemodus werden alle Ereignisse angezeigt, die während der Aufzeichnung ausgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="8e0ea-106">The timeline events mode displays all events triggered while making a recording.</span></span>  <span data-ttu-id="8e0ea-107">Verwenden Sie den Zeitachsenereignisverweis, um mehr über jeden Zeitachsenereignistyp zu erfahren.</span><span class="sxs-lookup"><span data-stu-id="8e0ea-107">Use the timeline event reference to learn more about each timeline event type.</span></span>  

## <a name="common-timeline-event-properties"></a><span data-ttu-id="8e0ea-108">Allgemeine Eigenschaften des Zeitachsenereigniss</span><span class="sxs-lookup"><span data-stu-id="8e0ea-108">Common timeline event properties</span></span>  

<span data-ttu-id="8e0ea-109">Bestimmte Details sind in Ereignissen aller Typen vorhanden, während einige nur für bestimmte Ereignistypen gelten.</span><span class="sxs-lookup"><span data-stu-id="8e0ea-109">Certain details are present in events of all types, while some only apply to certain event types.</span></span>  <span data-ttu-id="8e0ea-110">In diesem Abschnitt werden Eigenschaften aufgeführt, die unterschiedlichen Ereignistypen gemeinsam sind.</span><span class="sxs-lookup"><span data-stu-id="8e0ea-110">This section lists properties common to different event types.</span></span>  <span data-ttu-id="8e0ea-111">Eigenschaften, die für bestimmte Ereignistypen spezifisch sind, werden in den Verweisen für die folgenden Ereignistypen aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="8e0ea-111">Properties specific to certain event types are listed in the references for those event types that follow.</span></span>  

| <span data-ttu-id="8e0ea-112">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="8e0ea-112">Property</span></span> | <span data-ttu-id="8e0ea-113">Wann wird sie angezeigt?</span><span class="sxs-lookup"><span data-stu-id="8e0ea-113">When is it shown</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="8e0ea-114">Aggregierte Zeit</span><span class="sxs-lookup"><span data-stu-id="8e0ea-114">Aggregated time</span></span> | <span data-ttu-id="8e0ea-115">Bei Ereignissen mit **geschachtelten Ereignissen**die Zeit, die von jeder Kategorie von Ereignissen genommen wird.</span><span class="sxs-lookup"><span data-stu-id="8e0ea-115">For events with **nested events**, the time taken by each category of events.</span></span> |  
| <span data-ttu-id="8e0ea-116">Aufrufliste</span><span class="sxs-lookup"><span data-stu-id="8e0ea-116">Call Stack</span></span> | <span data-ttu-id="8e0ea-117">Für Ereignisse mit **untergeordneten Ereignissen**die Zeit, die von jeder Kategorie von Ereignissen genommen wird.</span><span class="sxs-lookup"><span data-stu-id="8e0ea-117">For events with **child events**, the time taken by each category of events.</span></span> |  
| <span data-ttu-id="8e0ea-118">CPU-Zeit</span><span class="sxs-lookup"><span data-stu-id="8e0ea-118">CPU time</span></span> | <span data-ttu-id="8e0ea-119">Wie viel CPU-Zeit das aufgezeichnete Ereignis in Anspruch nahm.</span><span class="sxs-lookup"><span data-stu-id="8e0ea-119">How much CPU time the recorded event took.</span></span> |  
| <span data-ttu-id="8e0ea-120">Details</span><span class="sxs-lookup"><span data-stu-id="8e0ea-120">Details</span></span> | <span data-ttu-id="8e0ea-121">Weitere Details zum Ereignis.</span><span class="sxs-lookup"><span data-stu-id="8e0ea-121">Other details about the event.</span></span> |  
| <span data-ttu-id="8e0ea-122">Duration \(at time-stamp\)</span><span class="sxs-lookup"><span data-stu-id="8e0ea-122">Duration \(at time-stamp\)</span></span> | <span data-ttu-id="8e0ea-123">Wie lange es ge dauern hat, bis das Ereignis mit allen seinen kindern abgeschlossen wurde; zeitstempel ist der Zeitpunkt, zu dem das Ereignis aufgetreten ist, relativ zum Zeitpunkt des Beginns der Aufzeichnung.</span><span class="sxs-lookup"><span data-stu-id="8e0ea-123">How long it took the event with all of its children to complete; timestamp is the time at which the event occurred, relative to when the recording started.</span></span> |  
| <span data-ttu-id="8e0ea-124">Self time</span><span class="sxs-lookup"><span data-stu-id="8e0ea-124">Self time</span></span> | <span data-ttu-id="8e0ea-125">Die Dauer des Ereignisses ohne seine kinder.</span><span class="sxs-lookup"><span data-stu-id="8e0ea-125">How long the event took without any of its children.</span></span> |  
| <span data-ttu-id="8e0ea-126">Verwendete Heapgröße</span><span class="sxs-lookup"><span data-stu-id="8e0ea-126">Used Heap Size</span></span> | <span data-ttu-id="8e0ea-127">Der von der Anwendung beim Aufzeichnen des Ereignisses verwendete Arbeitsspeicher, und die delta \(+/-\)-Änderung in der verwendeten Heapgröße seit dem letzten Sampling.</span><span class="sxs-lookup"><span data-stu-id="8e0ea-127">Amount of memory being used by the application when the event was recorded, and the delta \(+/-\) change in used heap size since the last sampling.</span></span> |  

<!--todo: add nested and child events (timelinetool) section when available -->  

## <a name="loading-events"></a><span data-ttu-id="8e0ea-128">Laden von Ereignissen</span><span class="sxs-lookup"><span data-stu-id="8e0ea-128">Loading events</span></span>  

<span data-ttu-id="8e0ea-129">In diesem Abschnitt werden Ereignisse aufgeführt, die zur Kategorie Laden und deren Eigenschaften gehören.</span><span class="sxs-lookup"><span data-stu-id="8e0ea-129">This section lists events that belong to Loading category and their properties.</span></span>  

| <span data-ttu-id="8e0ea-130">Ereignis</span><span class="sxs-lookup"><span data-stu-id="8e0ea-130">Event</span></span> | <span data-ttu-id="8e0ea-131">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8e0ea-131">Description</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="8e0ea-132">Analysieren von HTML</span><span class="sxs-lookup"><span data-stu-id="8e0ea-132">Parse HTML</span></span> |  <span data-ttu-id="8e0ea-133">Microsoft Edge den HTML-Analysealgorithmus.</span><span class="sxs-lookup"><span data-stu-id="8e0ea-133">Microsoft Edge ran the HTML parsing algorithm.</span></span> |  
| <span data-ttu-id="8e0ea-134">Beenden des Ladens</span><span class="sxs-lookup"><span data-stu-id="8e0ea-134">Finish Loading</span></span> |  <span data-ttu-id="8e0ea-135">Eine Netzwerkanforderung wurde abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="8e0ea-135">A network request completed.</span></span> |  
| <span data-ttu-id="8e0ea-136">Empfangsdaten</span><span class="sxs-lookup"><span data-stu-id="8e0ea-136">Receive Data</span></span> |  <span data-ttu-id="8e0ea-137">Daten für eine Anforderung wurden empfangen.</span><span class="sxs-lookup"><span data-stu-id="8e0ea-137">Data for a request was received.</span></span>  <span data-ttu-id="8e0ea-138">Es gibt mindestens ein Receive Data-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="8e0ea-138">There are one or more Receive Data events.</span></span> |  
| <span data-ttu-id="8e0ea-139">Antwort empfangen</span><span class="sxs-lookup"><span data-stu-id="8e0ea-139">Receive Response</span></span> |  <span data-ttu-id="8e0ea-140">Die anfängliche HTTP-Antwort einer Anforderung.</span><span class="sxs-lookup"><span data-stu-id="8e0ea-140">The initial HTTP response from a request.</span></span> |  
| <span data-ttu-id="8e0ea-141">Sendeanforderung</span><span class="sxs-lookup"><span data-stu-id="8e0ea-141">Send Request</span></span> |  <span data-ttu-id="8e0ea-142">Eine Netzwerkanforderung wurde gesendet.</span><span class="sxs-lookup"><span data-stu-id="8e0ea-142">A network request has been sent.</span></span> |  

### <a name="loading-event-properties"></a><span data-ttu-id="8e0ea-143">Laden von Ereigniseigenschaften</span><span class="sxs-lookup"><span data-stu-id="8e0ea-143">Loading event properties</span></span>  

| <span data-ttu-id="8e0ea-144">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="8e0ea-144">Property</span></span> | <span data-ttu-id="8e0ea-145">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8e0ea-145">Description</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="8e0ea-146">Ressource</span><span class="sxs-lookup"><span data-stu-id="8e0ea-146">Resource</span></span> | <span data-ttu-id="8e0ea-147">Die URL der angeforderten Ressource.</span><span class="sxs-lookup"><span data-stu-id="8e0ea-147">The URL of the requested resource.</span></span> |  
| <span data-ttu-id="8e0ea-148">Preview</span><span class="sxs-lookup"><span data-stu-id="8e0ea-148">Preview</span></span> | <span data-ttu-id="8e0ea-149">Vorschau der angeforderten Ressource \(nur Bilder\).</span><span class="sxs-lookup"><span data-stu-id="8e0ea-149">Preview of the requested resource \(images only\).</span></span> |  
| <span data-ttu-id="8e0ea-150">Request-Methode</span><span class="sxs-lookup"><span data-stu-id="8e0ea-150">Request Method</span></span> | <span data-ttu-id="8e0ea-151">DIE HTTP-Methode, die für die Anforderung \( `GET` oder `POST` , z. B. \) verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="8e0ea-151">HTTP method used for the request \(`GET` or `POST`, for example\).</span></span> |  
| <span data-ttu-id="8e0ea-152">Statuscode</span><span class="sxs-lookup"><span data-stu-id="8e0ea-152">Status Code</span></span> | <span data-ttu-id="8e0ea-153">HTTP-Antwortcode.</span><span class="sxs-lookup"><span data-stu-id="8e0ea-153">HTTP response code.</span></span> |  
| <span data-ttu-id="8e0ea-154">MIME-Typ</span><span class="sxs-lookup"><span data-stu-id="8e0ea-154">MIME Type</span></span> | <span data-ttu-id="8e0ea-155">MIME-Typ der angeforderten Ressource.</span><span class="sxs-lookup"><span data-stu-id="8e0ea-155">MIME type of the requested resource.</span></span> |  
| <span data-ttu-id="8e0ea-156">Codierte Datenlänge</span><span class="sxs-lookup"><span data-stu-id="8e0ea-156">Encoded Data Length</span></span> | <span data-ttu-id="8e0ea-157">Länge der angeforderten Ressource in Bytes.</span><span class="sxs-lookup"><span data-stu-id="8e0ea-157">Length of requested resource in bytes.</span></span> |  

## <a name="scripting-events"></a><span data-ttu-id="8e0ea-158">Skriptingereignisse</span><span class="sxs-lookup"><span data-stu-id="8e0ea-158">Scripting events</span></span>  

<span data-ttu-id="8e0ea-159">In diesem Abschnitt werden Ereignisse aufgeführt, die zur Kategorie "Scripting" und deren Eigenschaften gehören.</span><span class="sxs-lookup"><span data-stu-id="8e0ea-159">This section lists events that belong to the Scripting category and their properties.</span></span>  

| <span data-ttu-id="8e0ea-160">Ereignis</span><span class="sxs-lookup"><span data-stu-id="8e0ea-160">Event</span></span> | <span data-ttu-id="8e0ea-161">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8e0ea-161">Description</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="8e0ea-162">Animationsframe ausgelöst</span><span class="sxs-lookup"><span data-stu-id="8e0ea-162">Animation Frame Fired</span></span> | <span data-ttu-id="8e0ea-163">Ein geplanter Animationsframe wurde ausgelöst, und der Rückrufhandler wird aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="8e0ea-163">A scheduled animation frame fired, and its callback handler invoked.</span></span> |  
| <span data-ttu-id="8e0ea-164">Abbrechen des Animationsframes</span><span class="sxs-lookup"><span data-stu-id="8e0ea-164">Cancel Animation Frame</span></span> |  <span data-ttu-id="8e0ea-165">Ein geplanter Animationsframe wurde abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="8e0ea-165">A scheduled animation frame was canceled.</span></span> |  
| <span data-ttu-id="8e0ea-166">GC-Ereignis</span><span class="sxs-lookup"><span data-stu-id="8e0ea-166">GC Event</span></span> |  <span data-ttu-id="8e0ea-167">Die Garbage Collection ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="8e0ea-167">Garbage collection occurred.</span></span> |  
| <span data-ttu-id="8e0ea-168">DOMContentLoaded</span><span class="sxs-lookup"><span data-stu-id="8e0ea-168">DOMContentLoaded</span></span> |  <span data-ttu-id="8e0ea-169">Das [DOMContentLoaded-Ereignis][MDNWindowDOMContentLoadedEvent] wurde vom Browser ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="8e0ea-169">The [DOMContentLoaded event][MDNWindowDOMContentLoadedEvent] was fired by the browser.</span></span>  <span data-ttu-id="8e0ea-170">Dieses Ereignis wird ausgelöst, wenn der ganze DOM-Inhalt der Seite geladen und analysiert wird.</span><span class="sxs-lookup"><span data-stu-id="8e0ea-170">This event is fired when all of the DOM content of the page is loaded and parsed.</span></span> |  
| <span data-ttu-id="8e0ea-171">Auswerten des Skripts</span><span class="sxs-lookup"><span data-stu-id="8e0ea-171">Evaluate Script</span></span> | <span data-ttu-id="8e0ea-172">Ein Skript wurde ausgewertet.</span><span class="sxs-lookup"><span data-stu-id="8e0ea-172">A script was evaluated.</span></span> |  
| <span data-ttu-id="8e0ea-173">Ereignis</span><span class="sxs-lookup"><span data-stu-id="8e0ea-173">Event</span></span> | <span data-ttu-id="8e0ea-174">Ein JavaScript-Ereignis \(z. B. `mousedown` , oder `key` \).</span><span class="sxs-lookup"><span data-stu-id="8e0ea-174">A JavaScript event \(for example, `mousedown`, or `key`\).</span></span> |  
| <span data-ttu-id="8e0ea-175">Funktionsaufruf</span><span class="sxs-lookup"><span data-stu-id="8e0ea-175">Function Call</span></span> | <span data-ttu-id="8e0ea-176">Ein JavaScript-Funktionsaufruf auf oberster Ebene wurde vorgenommen \(wird nur angezeigt, wenn der Browser das JavaScript-Modul aufruft\).</span><span class="sxs-lookup"><span data-stu-id="8e0ea-176">A top-level JavaScript function call was made \(only appears when browser enters JavaScript engine\).</span></span> |  
| <span data-ttu-id="8e0ea-177">Installieren des Timers</span><span class="sxs-lookup"><span data-stu-id="8e0ea-177">Install Timer</span></span> | <span data-ttu-id="8e0ea-178">Ein Timer wurde mit [setInterval()][MDNWindowOrWorkerGlobalScopeSetInterval] oder [setTimeout() erstellt.][MDNWindowOrWorkerGlobalScopeSetTimeout]</span><span class="sxs-lookup"><span data-stu-id="8e0ea-178">A timer was created with [setInterval()][MDNWindowOrWorkerGlobalScopeSetInterval] or [setTimeout()][MDNWindowOrWorkerGlobalScopeSetTimeout].</span></span> |  
| <span data-ttu-id="8e0ea-179">Animationsframe anfordern</span><span class="sxs-lookup"><span data-stu-id="8e0ea-179">Request Animation Frame</span></span> | <span data-ttu-id="8e0ea-180">Ein `requestAnimationFrame()` Anruf hat einen neuen Frame geplant.</span><span class="sxs-lookup"><span data-stu-id="8e0ea-180">A `requestAnimationFrame()` call scheduled a new frame.</span></span> |  
| <span data-ttu-id="8e0ea-181">Timer entfernen</span><span class="sxs-lookup"><span data-stu-id="8e0ea-181">Remove Timer</span></span> | <span data-ttu-id="8e0ea-182">Ein zuvor erstellter Zeitgeber wurde geräumt.</span><span class="sxs-lookup"><span data-stu-id="8e0ea-182">A previously created timer was cleared.</span></span> |  
| <span data-ttu-id="8e0ea-183">Zeit</span><span class="sxs-lookup"><span data-stu-id="8e0ea-183">Time</span></span> |  <span data-ttu-id="8e0ea-184">Ein Skript mit dem Namen [console.time()][ConsoleApiTime].</span><span class="sxs-lookup"><span data-stu-id="8e0ea-184">A script called [console.time()][ConsoleApiTime].</span></span> |  
| <span data-ttu-id="8e0ea-185">Zeitende</span><span class="sxs-lookup"><span data-stu-id="8e0ea-185">Time End</span></span> | <span data-ttu-id="8e0ea-186">Ein Skript mit dem Namen [console.timeEnd()][ConsoleApiTimeEnd].</span><span class="sxs-lookup"><span data-stu-id="8e0ea-186">A script called [console.timeEnd()][ConsoleApiTimeEnd].</span></span> |  
| <span data-ttu-id="8e0ea-187">Timer Fired</span><span class="sxs-lookup"><span data-stu-id="8e0ea-187">Timer Fired</span></span> | <span data-ttu-id="8e0ea-188">Ein timer fired that was scheduled with `setInterval()` or `setTimeout()` .</span><span class="sxs-lookup"><span data-stu-id="8e0ea-188">A timer fired that was scheduled with `setInterval()` or `setTimeout()`.</span></span> |  
| <span data-ttu-id="8e0ea-189">XHR Ready State Change</span><span class="sxs-lookup"><span data-stu-id="8e0ea-189">XHR Ready State Change</span></span> | <span data-ttu-id="8e0ea-190">Der Bereitzustand einer XMLHTTPRequest wurde geändert.</span><span class="sxs-lookup"><span data-stu-id="8e0ea-190">The ready state of an XMLHTTPRequest changed.</span></span> |  
| <span data-ttu-id="8e0ea-191">XHR Load</span><span class="sxs-lookup"><span data-stu-id="8e0ea-191">XHR Load</span></span> | <span data-ttu-id="8e0ea-192">Ein `XMLHTTPRequest` fertiges Laden.</span><span class="sxs-lookup"><span data-stu-id="8e0ea-192">An `XMLHTTPRequest` finished loading.</span></span> |  

### <a name="scripting-event-properties"></a><span data-ttu-id="8e0ea-193">Eigenschaften des Skriptereigniss</span><span class="sxs-lookup"><span data-stu-id="8e0ea-193">Scripting event properties</span></span>  

| <span data-ttu-id="8e0ea-194">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="8e0ea-194">Property</span></span> | <span data-ttu-id="8e0ea-195">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8e0ea-195">Description</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="8e0ea-196">Zeitgeber-ID</span><span class="sxs-lookup"><span data-stu-id="8e0ea-196">Timer ID</span></span> | <span data-ttu-id="8e0ea-197">Die Zeitgeber-ID.</span><span class="sxs-lookup"><span data-stu-id="8e0ea-197">The timer ID.</span></span> |  
| <span data-ttu-id="8e0ea-198">Timeout</span><span class="sxs-lookup"><span data-stu-id="8e0ea-198">Timeout</span></span> | <span data-ttu-id="8e0ea-199">Das vom Timer angegebene Timeout.</span><span class="sxs-lookup"><span data-stu-id="8e0ea-199">The timeout specified by the timer.</span></span> |  
| <span data-ttu-id="8e0ea-200">Wiederholungen</span><span class="sxs-lookup"><span data-stu-id="8e0ea-200">Repeats</span></span> | <span data-ttu-id="8e0ea-201">Boolean, der angibt, ob der Timer wiederholt wird.</span><span class="sxs-lookup"><span data-stu-id="8e0ea-201">Boolean that specifies if the timer repeats.</span></span> |  
| <span data-ttu-id="8e0ea-202">Funktionsaufruf</span><span class="sxs-lookup"><span data-stu-id="8e0ea-202">Function Call</span></span> | <span data-ttu-id="8e0ea-203">Eine Funktion, die aufgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="8e0ea-203">A function that was invoked.</span></span> |  

## <a name="rendering-events"></a><span data-ttu-id="8e0ea-204">Renderingereignisse</span><span class="sxs-lookup"><span data-stu-id="8e0ea-204">Rendering events</span></span>  

<span data-ttu-id="8e0ea-205">In diesem Abschnitt werden Ereignisse aufgeführt, die zur Kategorie Rendering und deren Eigenschaften gehören.</span><span class="sxs-lookup"><span data-stu-id="8e0ea-205">This section lists events that belong to Rendering category and their properties.</span></span>  

| <span data-ttu-id="8e0ea-206">Ereignis</span><span class="sxs-lookup"><span data-stu-id="8e0ea-206">Event</span></span> | <span data-ttu-id="8e0ea-207">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8e0ea-207">Description</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="8e0ea-208">Ungültiges Layout</span><span class="sxs-lookup"><span data-stu-id="8e0ea-208">Invalidate layout</span></span> | <span data-ttu-id="8e0ea-209">Das Seitenlayout wurde durch eine DOM-Änderung ungültig.</span><span class="sxs-lookup"><span data-stu-id="8e0ea-209">The page layout was invalidated by a DOM change.</span></span> |  
| <span data-ttu-id="8e0ea-210">Layout</span><span class="sxs-lookup"><span data-stu-id="8e0ea-210">Layout</span></span> | <span data-ttu-id="8e0ea-211">Ein Seitenlayout wurde abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="8e0ea-211">A page layout was completed.</span></span> |  
| <span data-ttu-id="8e0ea-212">Formatvorlage neu berechnen</span><span class="sxs-lookup"><span data-stu-id="8e0ea-212">Recalculate style</span></span> | <span data-ttu-id="8e0ea-213">Microsoft Edge hat Elementformatvorlagen neu berechnet.</span><span class="sxs-lookup"><span data-stu-id="8e0ea-213">Microsoft Edge recalculated element styles.</span></span> |  
| <span data-ttu-id="8e0ea-214">Scroll</span><span class="sxs-lookup"><span data-stu-id="8e0ea-214">Scroll</span></span> | <span data-ttu-id="8e0ea-215">Der Inhalt der geschachtelten Ansicht wurde geschachtelt.</span><span class="sxs-lookup"><span data-stu-id="8e0ea-215">The content of nested view was scrolled.</span></span> |  

### <a name="rendering-event-properties"></a><span data-ttu-id="8e0ea-216">Renderingereigniseigenschaften</span><span class="sxs-lookup"><span data-stu-id="8e0ea-216">Rendering event properties</span></span>  

| <span data-ttu-id="8e0ea-217">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="8e0ea-217">Property</span></span> | <span data-ttu-id="8e0ea-218">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8e0ea-218">Description</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="8e0ea-219">Layout ungültig</span><span class="sxs-lookup"><span data-stu-id="8e0ea-219">Layout invalidated</span></span> | <span data-ttu-id="8e0ea-220">Bei Layoutdatensätzen die Stapelverfolgung des Codes, der dazu führte, dass das Layout ungültig wurde.</span><span class="sxs-lookup"><span data-stu-id="8e0ea-220">For Layout records, the stack trace of the code that caused the layout to be invalidated.</span></span> |  
| <span data-ttu-id="8e0ea-221">Knoten, die Layout benötigen</span><span class="sxs-lookup"><span data-stu-id="8e0ea-221">Nodes that need layout</span></span> | <span data-ttu-id="8e0ea-222">Für Layoutdatensätze die Anzahl der Knoten, die vor dem Neulayout als layout erforderlich gekennzeichnet wurden.</span><span class="sxs-lookup"><span data-stu-id="8e0ea-222">For Layout records, the number of nodes that were marked as needing layout before the relayout started.</span></span>  <span data-ttu-id="8e0ea-223">Dies sind normalerweise die Knoten, die durch Entwicklercode ungültig wurden, sowie ein Pfad nach oben zum Neulayout des Stamms.</span><span class="sxs-lookup"><span data-stu-id="8e0ea-223">These are normally those nodes that were invalidated by developer code, plus a path upward to relayout root.</span></span> |  
| <span data-ttu-id="8e0ea-224">Layoutstrukturgröße</span><span class="sxs-lookup"><span data-stu-id="8e0ea-224">Layout tree size</span></span> | <span data-ttu-id="8e0ea-225">Für Layoutdatensätze die Gesamtanzahl der Knoten unter dem Neulayoutstamm \(der Knoten, von dem Microsoft Edge das Neulayout startet\).</span><span class="sxs-lookup"><span data-stu-id="8e0ea-225">For Layout records, the total number of nodes under the relayout root \(the node that Microsoft Edge starts the relayout\).</span></span> |  
| <span data-ttu-id="8e0ea-226">Layoutbereich</span><span class="sxs-lookup"><span data-stu-id="8e0ea-226">Layout scope</span></span> | <span data-ttu-id="8e0ea-227">Mögliche Werte sind `Partial` \(die Neulayoutgrenze ist ein Teil des DOM\) oder `Whole document` .</span><span class="sxs-lookup"><span data-stu-id="8e0ea-227">Possible values are `Partial` \(the re-layout boundary is a portion of the DOM\) or `Whole document`.</span></span> |  
| <span data-ttu-id="8e0ea-228">Betroffene Elemente</span><span class="sxs-lookup"><span data-stu-id="8e0ea-228">Elements affected</span></span> | <span data-ttu-id="8e0ea-229">Bei Neuberechnung von Formatvorlagedatensätzen die Anzahl der Elemente, die von einer Formatvorlage neu berechnet werden.</span><span class="sxs-lookup"><span data-stu-id="8e0ea-229">For Recalculate style records, the number of elements affected by a style recalculation.</span></span> |  
| <span data-ttu-id="8e0ea-230">Formatvorlagen ungültig</span><span class="sxs-lookup"><span data-stu-id="8e0ea-230">Styles invalidated</span></span> | <span data-ttu-id="8e0ea-231">Stellt für Die Neuberechnung von Formatvorlagedatensätzen die Stapelverfolgung des Codes zur Ursache der Format ungültigen Formatvorlage.</span><span class="sxs-lookup"><span data-stu-id="8e0ea-231">For Recalculate style records, provides the stack trace of the code that caused the style invalidation.</span></span> |  

## <a name="painting-events"></a><span data-ttu-id="8e0ea-232">Malereignisse</span><span class="sxs-lookup"><span data-stu-id="8e0ea-232">Painting events</span></span>  

<span data-ttu-id="8e0ea-233">In diesem Abschnitt werden Ereignisse aufgeführt, die zur Kategorie "Malen" und deren Eigenschaften gehören.</span><span class="sxs-lookup"><span data-stu-id="8e0ea-233">This section lists events that belong to Painting category and their properties.</span></span>  

| <span data-ttu-id="8e0ea-234">Ereignis</span><span class="sxs-lookup"><span data-stu-id="8e0ea-234">Event</span></span> | <span data-ttu-id="8e0ea-235">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8e0ea-235">Description</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="8e0ea-236">Zusammengesetzte Ebenen</span><span class="sxs-lookup"><span data-stu-id="8e0ea-236">Composite Layers</span></span> | <span data-ttu-id="8e0ea-237">Die zusammengesetzten Bildebenen für das Microsoft Edge-Renderingmodul.</span><span class="sxs-lookup"><span data-stu-id="8e0ea-237">The composited image layers for the Microsoft Edge rendering engine.</span></span> |  
| <span data-ttu-id="8e0ea-238">Bilddecode</span><span class="sxs-lookup"><span data-stu-id="8e0ea-238">Image Decode</span></span> | <span data-ttu-id="8e0ea-239">Eine Bildressource wurde decodiert.</span><span class="sxs-lookup"><span data-stu-id="8e0ea-239">An image resource was decoded.</span></span> |  
| <span data-ttu-id="8e0ea-240">Bildgröße</span><span class="sxs-lookup"><span data-stu-id="8e0ea-240">Image Resize</span></span> | <span data-ttu-id="8e0ea-241">Die Größe eines Bilds wurde von den systemeigenen Dimensionen angepasst.</span><span class="sxs-lookup"><span data-stu-id="8e0ea-241">An image was resized from its native dimensions.</span></span> |  
| <span data-ttu-id="8e0ea-242">Paint</span><span class="sxs-lookup"><span data-stu-id="8e0ea-242">Paint</span></span> | <span data-ttu-id="8e0ea-243">Zusammengesetzte Ebenen wurden in einen Bereich der Anzeige dargestellt.</span><span class="sxs-lookup"><span data-stu-id="8e0ea-243">Composited layers were painted to a region of the display.</span></span>  <span data-ttu-id="8e0ea-244">Wenn Sie mit der Maus auf einen Paint-Datensatz zeigen, wird der Bereich der aktualisierten Anzeige hervorgehoben.</span><span class="sxs-lookup"><span data-stu-id="8e0ea-244">Hovering over a Paint record highlights the region of the display that was updated.</span></span> |  

### <a name="painting-event-properties"></a><span data-ttu-id="8e0ea-245">Eigenschaften des Painting-Ereignisses</span><span class="sxs-lookup"><span data-stu-id="8e0ea-245">Painting event properties</span></span>  

| <span data-ttu-id="8e0ea-246">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="8e0ea-246">Property</span></span> | <span data-ttu-id="8e0ea-247">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8e0ea-247">Description</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="8e0ea-248">Pfad</span><span class="sxs-lookup"><span data-stu-id="8e0ea-248">Location</span></span> | <span data-ttu-id="8e0ea-249">Bei Paint-Ereignissen werden die x- und y-Koordinaten des Farbrechtecks angezeigt.</span><span class="sxs-lookup"><span data-stu-id="8e0ea-249">For Paint events, the x and y coordinates of the paint rectangle.</span></span> |  
| <span data-ttu-id="8e0ea-250">Dimensionen</span><span class="sxs-lookup"><span data-stu-id="8e0ea-250">Dimensions</span></span> | <span data-ttu-id="8e0ea-251">Bei Paint-Ereignissen die Höhe und Breite des gefärbten Bereich.</span><span class="sxs-lookup"><span data-stu-id="8e0ea-251">For Paint events, the height and width of the painted region.</span></span> |  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="8e0ea-252">Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen</span><span class="sxs-lookup"><span data-stu-id="8e0ea-252">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->

[ConsoleApiTime]: /microsoft-edge/devtools-guide-chromium/console/api#time "time – Konsolen-API-Referenz"  
[ConsoleApiTimeEnd]: /microsoft-edge/devtools-guide-chromium/console/api#timeend "timeEnd – Konsolen-API-Referenz"  
<!--[EvaluatePerformanceTimelineTool]: timeline-tool "How to Use the Timeline Tool"  -->

[MDNWindowDOMContentLoadedEvent]: https://developer.mozilla.org/docs/Web/Events/DOMContentLoaded "Fenster: DOMContentLoaded-Ereignis | MDN"  
[MDNWindowOrWorkerGlobalScopeSetInterval]: https://developer.mozilla.org/docs/Web/API/WindowTimers/setInterval "WindowOrWorkerGlobalScope.setInterval() | MDN"  
[MDNWindowOrWorkerGlobalScopeSetTimeout]: https://developer.mozilla.org/docs/Web/API/WindowTimers/setTimeout "WindowOrWorkerGlobalScope.setTimeout() | MDN"  

> [!NOTE]
> <span data-ttu-id="8e0ea-258">Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8e0ea-258">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="8e0ea-259">Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/evaluate-performance/performance-reference) und wird von [Meggin Kearney][MegginKearney] \(Tech Writer\) und [Flavio Copes][FlavioCopes] \(Full Stack Developer\) verfasst.</span><span class="sxs-lookup"><span data-stu-id="8e0ea-259">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/evaluate-performance/performance-reference) and is authored by [Meggin Kearney][MegginKearney] \(Tech Writer\) and [Flavio Copes][FlavioCopes] \(Full Stack Developer\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="8e0ea-261">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="8e0ea-261">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[MegginKearney]: https://developers.google.com/web/resources/contributors/megginkearney  
[FlavioCopes]: https://developers.google.com/web/resources/contributors/flaviocopes  
