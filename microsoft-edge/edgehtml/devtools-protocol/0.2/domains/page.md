---
description: DevTools Protocol Version 0.2 (EdgeHTML)-Referenz für die Seitendomäne. Aktionen und Ereignisse im Zusammenhang mit der überprüften Seite gehören zur Seitendomäne.
title: Page Domain - DevTools Protocol Version 0.2 (EdgeHTML)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/03/2020
ms.topic: reference
ms.prod: microsoft-edge
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: d969dd100164ace61445a4618174cfa943dcfd2b
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398847"
---
# <a name="page-domain---devtools-protocol-version-02-edgehtml"></a><span data-ttu-id="a4a91-104">Page Domain - DevTools Protocol Version 0.2 (EdgeHTML)</span><span class="sxs-lookup"><span data-stu-id="a4a91-104">Page Domain - DevTools Protocol Version 0.2 (EdgeHTML)</span></span>  

<span data-ttu-id="a4a91-105">Aktionen und Ereignisse im Zusammenhang mit der überprüften Seite gehören zur Seitendomäne.</span><span class="sxs-lookup"><span data-stu-id="a4a91-105">Actions and events related to the inspected page belong to the page domain.</span></span>  

| <span data-ttu-id="a4a91-106">Klassifizierung</span><span class="sxs-lookup"><span data-stu-id="a4a91-106">Classification</span></span> | <span data-ttu-id="a4a91-107">Member</span><span class="sxs-lookup"><span data-stu-id="a4a91-107">Members</span></span> |  
|:--- |:--- |  
| [<span data-ttu-id="a4a91-108">Methoden</span><span class="sxs-lookup"><span data-stu-id="a4a91-108">Methods</span></span>](#methods) | <span data-ttu-id="a4a91-109">[aktivieren](#enable), [deaktivieren](#disable), [navigieren](#navigate), [getFrameTree](#getframetree)</span><span class="sxs-lookup"><span data-stu-id="a4a91-109">[enable](#enable), [disable](#disable), [navigate](#navigate), [getFrameTree](#getframetree)</span></span> |  
| [<span data-ttu-id="a4a91-110">Veranstaltungen</span><span class="sxs-lookup"><span data-stu-id="a4a91-110">Events</span></span>](#events) | <span data-ttu-id="a4a91-111">[frameAttached](#frameattached), [frameDetached](#framedetached), [frameNavigated](#framenavigated), [loadEventFired](#loadeventfired), [domContentEventFired](#domcontenteventfired)</span><span class="sxs-lookup"><span data-stu-id="a4a91-111">[frameAttached](#frameattached), [frameDetached](#framedetached), [frameNavigated](#framenavigated), [loadEventFired](#loadeventfired), [domContentEventFired](#domcontenteventfired)</span></span> |  
| [<span data-ttu-id="a4a91-112">Typen</span><span class="sxs-lookup"><span data-stu-id="a4a91-112">Types</span></span>](#types) | <span data-ttu-id="a4a91-113">[FrameId](#frameid), [Frame](#frame), [FrameTree](#frametree)</span><span class="sxs-lookup"><span data-stu-id="a4a91-113">[FrameId](#frameid), [Frame](#frame), [FrameTree](#frametree)</span></span> |  

## <a name="methods"></a><span data-ttu-id="a4a91-114">Methoden</span><span class="sxs-lookup"><span data-stu-id="a4a91-114">Methods</span></span>  

### <a name="enable"></a><span data-ttu-id="a4a91-115">Aktivieren</span><span class="sxs-lookup"><span data-stu-id="a4a91-115">enable</span></span>  

<span data-ttu-id="a4a91-116">Aktiviert Seitendomänenbenachrichtigungen.</span><span class="sxs-lookup"><span data-stu-id="a4a91-116">Enables page domain notifications.</span></span>  

&nbsp;  

---  

### <a name="disable"></a><span data-ttu-id="a4a91-117">Deaktivieren </span><span class="sxs-lookup"><span data-stu-id="a4a91-117">disable</span></span>  

<span data-ttu-id="a4a91-118">Deaktiviert Seitendomänenbenachrichtigungen.</span><span class="sxs-lookup"><span data-stu-id="a4a91-118">Disables page domain notifications.</span></span>  

&nbsp;  

---  

### <a name="navigate"></a><span data-ttu-id="a4a91-119">Navigieren</span><span class="sxs-lookup"><span data-stu-id="a4a91-119">navigate</span></span>  

<span data-ttu-id="a4a91-120">Navigiert die aktuelle Seite zur angegebenen URL.</span><span class="sxs-lookup"><span data-stu-id="a4a91-120">Navigates current page to the given URL.</span></span>  

| <span data-ttu-id="a4a91-121">Parameter</span><span class="sxs-lookup"><span data-stu-id="a4a91-121">Parameters</span></span> | <span data-ttu-id="a4a91-122">Typ</span><span class="sxs-lookup"><span data-stu-id="a4a91-122">Type</span></span> | <span data-ttu-id="a4a91-123">Details</span><span class="sxs-lookup"><span data-stu-id="a4a91-123">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="a4a91-124">URL</span><span class="sxs-lookup"><span data-stu-id="a4a91-124">url</span></span> | `string` | <span data-ttu-id="a4a91-125">URL, zu der die Seite navigiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="a4a91-125">URL to navigate the page to.</span></span> |  
| <span data-ttu-id="a4a91-126">frameId \(optional\)</span><span class="sxs-lookup"><span data-stu-id="a4a91-126">frameId \(optional\)</span></span> | [<span data-ttu-id="a4a91-127">FrameId</span><span class="sxs-lookup"><span data-stu-id="a4a91-127">FrameId</span></span>](#frameid) | <span data-ttu-id="a4a91-128">Frame-ID zum Navigieren.</span><span class="sxs-lookup"><span data-stu-id="a4a91-128">Frame id to navigate.</span></span>  <span data-ttu-id="a4a91-129">Wenn dieser Wert nicht angegeben ist, navigiert er auf der oberen Seite.</span><span class="sxs-lookup"><span data-stu-id="a4a91-129">If not specified, will navigate the top page.</span></span> |  

| <span data-ttu-id="a4a91-130">Gibt zurück</span><span class="sxs-lookup"><span data-stu-id="a4a91-130">Returns</span></span> | <span data-ttu-id="a4a91-131">Typ</span><span class="sxs-lookup"><span data-stu-id="a4a91-131">Type</span></span> | <span data-ttu-id="a4a91-132">Details</span><span class="sxs-lookup"><span data-stu-id="a4a91-132">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="a4a91-133">frameId</span><span class="sxs-lookup"><span data-stu-id="a4a91-133">frameId</span></span> | [<span data-ttu-id="a4a91-134">FrameId</span><span class="sxs-lookup"><span data-stu-id="a4a91-134">FrameId</span></span>](#frameid) | <span data-ttu-id="a4a91-135">Frame-ID, die navigiert wird.</span><span class="sxs-lookup"><span data-stu-id="a4a91-135">Frame id that will be navigated.</span></span> |  

---  

### <a name="getframetree"></a><span data-ttu-id="a4a91-136">getFrameTree</span><span class="sxs-lookup"><span data-stu-id="a4a91-136">getFrameTree</span></span>  

<span data-ttu-id="a4a91-137">Gibt die aktuelle Struktur der Framestruktur zurück.</span><span class="sxs-lookup"><span data-stu-id="a4a91-137">Returns present frame tree structure.</span></span>  

| <span data-ttu-id="a4a91-138">Gibt zurück</span><span class="sxs-lookup"><span data-stu-id="a4a91-138">Returns</span></span> | <span data-ttu-id="a4a91-139">Typ</span><span class="sxs-lookup"><span data-stu-id="a4a91-139">Type</span></span> | <span data-ttu-id="a4a91-140">Details</span><span class="sxs-lookup"><span data-stu-id="a4a91-140">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="a4a91-141">frameTree</span><span class="sxs-lookup"><span data-stu-id="a4a91-141">frameTree</span></span> | [<span data-ttu-id="a4a91-142">FrameTree</span><span class="sxs-lookup"><span data-stu-id="a4a91-142">FrameTree</span></span>](#frametree) | <span data-ttu-id="a4a91-143">Präsentieren der Struktur der Framestruktur.</span><span class="sxs-lookup"><span data-stu-id="a4a91-143">Present frame tree structure.</span></span> |  

---  

## <a name="events"></a><span data-ttu-id="a4a91-144">Veranstaltungen</span><span class="sxs-lookup"><span data-stu-id="a4a91-144">Events</span></span>  

### <a name="frameattached"></a><span data-ttu-id="a4a91-145">frameAttached</span><span class="sxs-lookup"><span data-stu-id="a4a91-145">frameAttached</span></span>  

<span data-ttu-id="a4a91-146">Wird ausgelöst, wenn frame an das übergeordnete Element angefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="a4a91-146">Fired when frame has been attached to its parent.</span></span>  

| <span data-ttu-id="a4a91-147">Parameter</span><span class="sxs-lookup"><span data-stu-id="a4a91-147">Parameters</span></span> | <span data-ttu-id="a4a91-148">Typ</span><span class="sxs-lookup"><span data-stu-id="a4a91-148">Type</span></span> | <span data-ttu-id="a4a91-149">Details</span><span class="sxs-lookup"><span data-stu-id="a4a91-149">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="a4a91-150">frameId</span><span class="sxs-lookup"><span data-stu-id="a4a91-150">frameId</span></span> | [<span data-ttu-id="a4a91-151">FrameId</span><span class="sxs-lookup"><span data-stu-id="a4a91-151">FrameId</span></span>](#frameid) | <span data-ttu-id="a4a91-152">ID des angefügten Frames.</span><span class="sxs-lookup"><span data-stu-id="a4a91-152">Id of the frame that has been attached.</span></span> |  
| <span data-ttu-id="a4a91-153">parentFrameId</span><span class="sxs-lookup"><span data-stu-id="a4a91-153">parentFrameId</span></span> | [<span data-ttu-id="a4a91-154">FrameId</span><span class="sxs-lookup"><span data-stu-id="a4a91-154">FrameId</span></span>](#frameid) | <span data-ttu-id="a4a91-155">Übergeordneter Framebezeichner.</span><span class="sxs-lookup"><span data-stu-id="a4a91-155">Parent frame identifier.</span></span> |  
| <span data-ttu-id="a4a91-156">stack \(optional\)</span><span class="sxs-lookup"><span data-stu-id="a4a91-156">stack \(optional\)</span></span> | [<span data-ttu-id="a4a91-157">Runtime.StackTrace</span><span class="sxs-lookup"><span data-stu-id="a4a91-157">Runtime.StackTrace</span></span>](./runtime.md#stacktrace) | <span data-ttu-id="a4a91-158">JavaScript stack trace of when frame was attached, only set if frame initiated from script.</span><span class="sxs-lookup"><span data-stu-id="a4a91-158">JavaScript stack trace of when frame was attached, only set if frame initiated from script.</span></span> |  

---  

### <a name="framedetached"></a><span data-ttu-id="a4a91-159">frameDetached</span><span class="sxs-lookup"><span data-stu-id="a4a91-159">frameDetached</span></span>  

<span data-ttu-id="a4a91-160">Wird ausgelöst, wenn der Frame vom übergeordneten Element getrennt wurde.</span><span class="sxs-lookup"><span data-stu-id="a4a91-160">Fired when frame has been detached from its parent.</span></span>  

| <span data-ttu-id="a4a91-161">Parameter</span><span class="sxs-lookup"><span data-stu-id="a4a91-161">Parameters</span></span> | <span data-ttu-id="a4a91-162">Typ</span><span class="sxs-lookup"><span data-stu-id="a4a91-162">Type</span></span> | <span data-ttu-id="a4a91-163">Details</span><span class="sxs-lookup"><span data-stu-id="a4a91-163">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="a4a91-164">frameId</span><span class="sxs-lookup"><span data-stu-id="a4a91-164">frameId</span></span> | [<span data-ttu-id="a4a91-165">FrameId</span><span class="sxs-lookup"><span data-stu-id="a4a91-165">FrameId</span></span>](#frameid) | <span data-ttu-id="a4a91-166">ID des getrennten Frames.</span><span class="sxs-lookup"><span data-stu-id="a4a91-166">ID of the frame that has been detached.</span></span> |  

---  

### <a name="framenavigated"></a><span data-ttu-id="a4a91-167">frameNavigated</span><span class="sxs-lookup"><span data-stu-id="a4a91-167">frameNavigated</span></span>  

<span data-ttu-id="a4a91-168">Wird ausgelöst, nachdem die Navigation des Frames abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="a4a91-168">Fired once navigation of the frame has completed.</span></span>  

| <span data-ttu-id="a4a91-169">Parameter</span><span class="sxs-lookup"><span data-stu-id="a4a91-169">Parameters</span></span> | <span data-ttu-id="a4a91-170">Typ</span><span class="sxs-lookup"><span data-stu-id="a4a91-170">Type</span></span> | <span data-ttu-id="a4a91-171">Details</span><span class="sxs-lookup"><span data-stu-id="a4a91-171">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="a4a91-172">frame</span><span class="sxs-lookup"><span data-stu-id="a4a91-172">frame</span></span> | [<span data-ttu-id="a4a91-173">Frame</span><span class="sxs-lookup"><span data-stu-id="a4a91-173">Frame</span></span>](#frame) | <span data-ttu-id="a4a91-174">Frame-Objekt.</span><span class="sxs-lookup"><span data-stu-id="a4a91-174">Frame object.</span></span> |  

---  

### <a name="loadeventfired"></a><span data-ttu-id="a4a91-175">loadEventFired</span><span class="sxs-lookup"><span data-stu-id="a4a91-175">loadEventFired</span></span>  

<span data-ttu-id="a4a91-176">Entspricht dem `window.onload` Ereignis.</span><span class="sxs-lookup"><span data-stu-id="a4a91-176">Corresponds to the `window.onload` event.</span></span>  

| <span data-ttu-id="a4a91-177">Parameter</span><span class="sxs-lookup"><span data-stu-id="a4a91-177">Parameters</span></span> | <span data-ttu-id="a4a91-178">Typ</span><span class="sxs-lookup"><span data-stu-id="a4a91-178">Type</span></span> | <span data-ttu-id="a4a91-179">Details</span><span class="sxs-lookup"><span data-stu-id="a4a91-179">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="a4a91-180">zeitstempel</span><span class="sxs-lookup"><span data-stu-id="a4a91-180">timestamp</span></span> | `number` | <span data-ttu-id="a4a91-181">Anzahl der Millisekunden seit der Epoche.</span><span class="sxs-lookup"><span data-stu-id="a4a91-181">Number of milliseconds since epoch.</span></span> |  

---  

### <a name="domcontenteventfired"></a><span data-ttu-id="a4a91-182">domContentEventFired</span><span class="sxs-lookup"><span data-stu-id="a4a91-182">domContentEventFired</span></span>  

<span data-ttu-id="a4a91-183">Entspricht dem `document.onDOMContentLoaded` Ereignis.</span><span class="sxs-lookup"><span data-stu-id="a4a91-183">Corresponds to the `document.onDOMContentLoaded` event.</span></span>  

| <span data-ttu-id="a4a91-184">Parameter</span><span class="sxs-lookup"><span data-stu-id="a4a91-184">Parameters</span></span> | <span data-ttu-id="a4a91-185">Typ</span><span class="sxs-lookup"><span data-stu-id="a4a91-185">Type</span></span> | <span data-ttu-id="a4a91-186">Details</span><span class="sxs-lookup"><span data-stu-id="a4a91-186">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="a4a91-187">zeitstempel</span><span class="sxs-lookup"><span data-stu-id="a4a91-187">timestamp</span></span> | `number` | <span data-ttu-id="a4a91-188">Anzahl der Millisekunden seit der Epoche.</span><span class="sxs-lookup"><span data-stu-id="a4a91-188">Number of milliseconds since epoch.</span></span> |  

---  

## <a name="types"></a><span data-ttu-id="a4a91-189">Typen</span><span class="sxs-lookup"><span data-stu-id="a4a91-189">Types</span></span>  

### <a name="frameid-string"></a><span data-ttu-id="a4a91-190">FrameId-Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="a4a91-190">FrameId string</span></span>  

<a name="frameid"></a>  

<span data-ttu-id="a4a91-191">Eindeutige Frame-ID.</span><span class="sxs-lookup"><span data-stu-id="a4a91-191">Unique frame identifier.</span></span>  

&nbsp;  

---  

### <a name="frame-object"></a><span data-ttu-id="a4a91-192">Frame-Objekt</span><span class="sxs-lookup"><span data-stu-id="a4a91-192">Frame object</span></span>  

<a name="frame"></a>  

<span data-ttu-id="a4a91-193">Informationen zum Frame auf der Seite.</span><span class="sxs-lookup"><span data-stu-id="a4a91-193">Information about the Frame on the Page.</span></span>  

| <span data-ttu-id="a4a91-194">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a4a91-194">Properties</span></span> | <span data-ttu-id="a4a91-195">Typ</span><span class="sxs-lookup"><span data-stu-id="a4a91-195">Type</span></span> | <span data-ttu-id="a4a91-196">Details</span><span class="sxs-lookup"><span data-stu-id="a4a91-196">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="a4a91-197">id</span><span class="sxs-lookup"><span data-stu-id="a4a91-197">id</span></span> | [<span data-ttu-id="a4a91-198">FrameId</span><span class="sxs-lookup"><span data-stu-id="a4a91-198">FrameId</span></span>](#frameid) | <span data-ttu-id="a4a91-199">Frame eindeutiger Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="a4a91-199">Frame unique identifier.</span></span> |  
| <span data-ttu-id="a4a91-200">parentId \(optional\)</span><span class="sxs-lookup"><span data-stu-id="a4a91-200">parentId \(optional\)</span></span> | [<span data-ttu-id="a4a91-201">FrameId</span><span class="sxs-lookup"><span data-stu-id="a4a91-201">FrameId</span></span>](#frameid) | <span data-ttu-id="a4a91-202">Eindeutiger Bezeichner des übergeordneten Frames.</span><span class="sxs-lookup"><span data-stu-id="a4a91-202">Parent frame unique identifier.</span></span> |  
| <span data-ttu-id="a4a91-203">Name \(optional\)</span><span class="sxs-lookup"><span data-stu-id="a4a91-203">name \(optional\)</span></span> | `string` | <span data-ttu-id="a4a91-204">Framename, wie im Tag angegeben.</span><span class="sxs-lookup"><span data-stu-id="a4a91-204">Frame's name as specified in the tag.</span></span> |  
| <span data-ttu-id="a4a91-205">URL</span><span class="sxs-lookup"><span data-stu-id="a4a91-205">url</span></span> | `string` | <span data-ttu-id="a4a91-206">Die URL des Framedokuments.</span><span class="sxs-lookup"><span data-stu-id="a4a91-206">Frame document's URL.</span></span> |  
| <span data-ttu-id="a4a91-207">securityOrigin</span><span class="sxs-lookup"><span data-stu-id="a4a91-207">securityOrigin</span></span> | `string` | <span data-ttu-id="a4a91-208">Der Sicherheitsherkunft des Framedokuments.</span><span class="sxs-lookup"><span data-stu-id="a4a91-208">Frame document's security origin.</span></span> |  
| <span data-ttu-id="a4a91-209">mimeType</span><span class="sxs-lookup"><span data-stu-id="a4a91-209">mimeType</span></span> | `string` | <span data-ttu-id="a4a91-210">Der mimeType des Framedokuments, wie vom Browser bestimmt.</span><span class="sxs-lookup"><span data-stu-id="a4a91-210">Frame document's mimeType as determined by the browser.</span></span> |  

---  

### <a name="frametree-object"></a><span data-ttu-id="a4a91-211">FrameTree-Objekt</span><span class="sxs-lookup"><span data-stu-id="a4a91-211">FrameTree object</span></span>  

<a name="frametree"></a>  

<span data-ttu-id="a4a91-212">Informationen zur Framehierarchie.</span><span class="sxs-lookup"><span data-stu-id="a4a91-212">Information about the Frame hierarchy.</span></span>  

| <span data-ttu-id="a4a91-213">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a4a91-213">Properties</span></span> | <span data-ttu-id="a4a91-214">Typ</span><span class="sxs-lookup"><span data-stu-id="a4a91-214">Type</span></span> | <span data-ttu-id="a4a91-215">Details</span><span class="sxs-lookup"><span data-stu-id="a4a91-215">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="a4a91-216">frame</span><span class="sxs-lookup"><span data-stu-id="a4a91-216">frame</span></span> | [<span data-ttu-id="a4a91-217">Frame</span><span class="sxs-lookup"><span data-stu-id="a4a91-217">Frame</span></span>](#frame) | <span data-ttu-id="a4a91-218">Frameinformationen für dieses Strukturelement.</span><span class="sxs-lookup"><span data-stu-id="a4a91-218">Frame information for this tree item.</span></span> |  
| <span data-ttu-id="a4a91-219">childFrames \(optional\)</span><span class="sxs-lookup"><span data-stu-id="a4a91-219">childFrames \(optional\)</span></span> | [<span data-ttu-id="a4a91-220">FrameTree[]</span><span class="sxs-lookup"><span data-stu-id="a4a91-220">FrameTree[]</span></span>](#frametree) | <span data-ttu-id="a4a91-221">Untergeordnete Frames.</span><span class="sxs-lookup"><span data-stu-id="a4a91-221">Child frames.</span></span> |  

---  
