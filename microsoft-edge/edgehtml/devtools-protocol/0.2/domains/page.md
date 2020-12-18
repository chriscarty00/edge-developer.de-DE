---
description: DevTools Protocol Version 0,2 (EdgeHTML)-Referenz für die Seiten Domäne. Aktionen und Ereignisse im Zusammenhang mit der geprüften Seite gehören der Seiten Domäne an.
title: Page Domain-devtools Protocol Version 0,2 (EdgeHTML)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: reference
ms.prod: microsoft-edge
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 2f1849a2e2aa2f53cef9dff5d03ac991d368a6f3
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233635"
---
# <span data-ttu-id="aa2e5-104">Page Domain-devtools Protocol Version 0,2 (EdgeHTML)</span><span class="sxs-lookup"><span data-stu-id="aa2e5-104">Page Domain - DevTools Protocol Version 0.2 (EdgeHTML)</span></span>  

<span data-ttu-id="aa2e5-105">Aktionen und Ereignisse im Zusammenhang mit der geprüften Seite gehören der Seiten Domäne an.</span><span class="sxs-lookup"><span data-stu-id="aa2e5-105">Actions and events related to the inspected page belong to the page domain.</span></span>

| | |
|-|-|
| [**<span data-ttu-id="aa2e5-106">Methoden</span><span class="sxs-lookup"><span data-stu-id="aa2e5-106">Methods</span></span>**](#methods) | <span data-ttu-id="aa2e5-107">[aktivieren](#enable), [Deaktivieren](#disable), [Navigieren](#navigate), [getFrameTree](#getframetree)</span><span class="sxs-lookup"><span data-stu-id="aa2e5-107">[enable](#enable), [disable](#disable), [navigate](#navigate), [getFrameTree](#getframetree)</span></span> |
| [**<span data-ttu-id="aa2e5-108">Veranstaltungen</span><span class="sxs-lookup"><span data-stu-id="aa2e5-108">Events</span></span>**](#events) | <span data-ttu-id="aa2e5-109">[frameAttached](#frameattached), [frameDetached](#framedetached), [frameNavigated](#framenavigated), [loadEventFired](#loadeventfired), [domContentEventFired](#domcontenteventfired)</span><span class="sxs-lookup"><span data-stu-id="aa2e5-109">[frameAttached](#frameattached), [frameDetached](#framedetached), [frameNavigated](#framenavigated), [loadEventFired](#loadeventfired), [domContentEventFired](#domcontenteventfired)</span></span> |
| [**<span data-ttu-id="aa2e5-110">Typen</span><span class="sxs-lookup"><span data-stu-id="aa2e5-110">Types</span></span>**](#types) | <span data-ttu-id="aa2e5-111">[Frame](#frameid)-Nr, [Frame](#frame), [FrameTree](#frametree)</span><span class="sxs-lookup"><span data-stu-id="aa2e5-111">[FrameId](#frameid), [Frame](#frame), [FrameTree](#frametree)</span></span> |
## <span data-ttu-id="aa2e5-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="aa2e5-112">Methods</span></span>

### <span data-ttu-id="aa2e5-113">Aktivieren</span><span class="sxs-lookup"><span data-stu-id="aa2e5-113">enable</span></span>
<span data-ttu-id="aa2e5-114">Aktiviert Seiten Domänen Benachrichtigungen.</span><span class="sxs-lookup"><span data-stu-id="aa2e5-114">Enables page domain notifications.</span></span>

</p>

---

### <span data-ttu-id="aa2e5-115">Deaktivieren </span><span class="sxs-lookup"><span data-stu-id="aa2e5-115">disable</span></span>
<span data-ttu-id="aa2e5-116">Deaktiviert Seiten Domänen Benachrichtigungen.</span><span class="sxs-lookup"><span data-stu-id="aa2e5-116">Disables page domain notifications.</span></span>

</p>

---

### <span data-ttu-id="aa2e5-117">Navigieren</span><span class="sxs-lookup"><span data-stu-id="aa2e5-117">navigate</span></span>
<span data-ttu-id="aa2e5-118">Navigiert die aktuelle Seite zur angegebenen URL.</span><span class="sxs-lookup"><span data-stu-id="aa2e5-118">Navigates current page to the given URL.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="aa2e5-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="aa2e5-119">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="aa2e5-120">URL</span><span class="sxs-lookup"><span data-stu-id="aa2e5-120">url</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="aa2e5-121">Die URL, zu der die Seite navigiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="aa2e5-121">URL to navigate the page to.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="aa2e5-122">Frame-Nr</span><span class="sxs-lookup"><span data-stu-id="aa2e5-122">frameId</span></span> <br/> <i><span data-ttu-id="aa2e5-123">Optional</span><span class="sxs-lookup"><span data-stu-id="aa2e5-123">optional</span></span></i></td>
            <td><a href="#frameid"><code class="flyout">FrameId</code></a></td>
            <td><span data-ttu-id="aa2e5-124">Die Frame-ID zum Navigieren.</span><span class="sxs-lookup"><span data-stu-id="aa2e5-124">Frame id to navigate.</span></span> <span data-ttu-id="aa2e5-125">Wenn keine Angabe erfolgt, navigiert die oberste Seite.</span><span class="sxs-lookup"><span data-stu-id="aa2e5-125">If not specified, will navigate the top page.</span></span></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="aa2e5-126">Gibt</span><span class="sxs-lookup"><span data-stu-id="aa2e5-126">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="aa2e5-127">Frame-Nr</span><span class="sxs-lookup"><span data-stu-id="aa2e5-127">frameId</span></span></td>
            <td><a href="#frameid"><code class="flyout">FrameId</code></a></td>
            <td><span data-ttu-id="aa2e5-128">Die Frame-ID, die navigiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="aa2e5-128">Frame id that will be navigated.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="aa2e5-129">getFrameTree</span><span class="sxs-lookup"><span data-stu-id="aa2e5-129">getFrameTree</span></span>
<span data-ttu-id="aa2e5-130">Gibt die aktuelle Frame Struktur zurück.</span><span class="sxs-lookup"><span data-stu-id="aa2e5-130">Returns present frame tree structure.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="aa2e5-131">Gibt</span><span class="sxs-lookup"><span data-stu-id="aa2e5-131">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="aa2e5-132">frameTree</span><span class="sxs-lookup"><span data-stu-id="aa2e5-132">frameTree</span></span></td>
            <td><a href="#frametree"><code class="flyout">FrameTree</code></a></td>
            <td><span data-ttu-id="aa2e5-133">Aktuelle Frame Struktur.</span><span class="sxs-lookup"><span data-stu-id="aa2e5-133">Present frame tree structure.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

## <span data-ttu-id="aa2e5-134">Veranstaltungen</span><span class="sxs-lookup"><span data-stu-id="aa2e5-134">Events</span></span>

### <span data-ttu-id="aa2e5-135">frameAttached</span><span class="sxs-lookup"><span data-stu-id="aa2e5-135">frameAttached</span></span>
<span data-ttu-id="aa2e5-136">Wird ausgelöst, wenn Frame dem übergeordneten Element angefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="aa2e5-136">Fired when frame has been attached to its parent.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="aa2e5-137">Parameter</span><span class="sxs-lookup"><span data-stu-id="aa2e5-137">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="aa2e5-138">Frame-Nr</span><span class="sxs-lookup"><span data-stu-id="aa2e5-138">frameId</span></span></td>
            <td><a href="#frameid"><code class="flyout">FrameId</code></a></td>
            <td><span data-ttu-id="aa2e5-139">Die ID des Rahmens, der angefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="aa2e5-139">Id of the frame that has been attached.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="aa2e5-140">parentFrameId</span><span class="sxs-lookup"><span data-stu-id="aa2e5-140">parentFrameId</span></span></td>
            <td><a href="#frameid"><code class="flyout">FrameId</code></a></td>
            <td><span data-ttu-id="aa2e5-141">Übergeordneter Frame Bezeichner</span><span class="sxs-lookup"><span data-stu-id="aa2e5-141">Parent frame identifier.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="aa2e5-142">Stapel</span><span class="sxs-lookup"><span data-stu-id="aa2e5-142">stack</span></span> <br/> <i><span data-ttu-id="aa2e5-143">Optional</span><span class="sxs-lookup"><span data-stu-id="aa2e5-143">optional</span></span></i></td>
            <td><a href="runtime.md#stacktrace"><code class="flyout">Runtime.StackTrace</code></a></td>
            <td><span data-ttu-id="aa2e5-144">JavaScript-Stapelüberwachung, wenn Frame angefügt wurde, nur festgelegt, wenn Frame vom Skript initiiert wurde.</span><span class="sxs-lookup"><span data-stu-id="aa2e5-144">JavaScript stack trace of when frame was attached, only set if frame initiated from script.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="aa2e5-145">frameDetached</span><span class="sxs-lookup"><span data-stu-id="aa2e5-145">frameDetached</span></span>
<span data-ttu-id="aa2e5-146">Wird ausgelöst, wenn Frame vom übergeordneten Element abgetrennt wurde.</span><span class="sxs-lookup"><span data-stu-id="aa2e5-146">Fired when frame has been detached from its parent.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="aa2e5-147">Parameter</span><span class="sxs-lookup"><span data-stu-id="aa2e5-147">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="aa2e5-148">Frame-Nr</span><span class="sxs-lookup"><span data-stu-id="aa2e5-148">frameId</span></span></td>
            <td><a href="#frameid"><code class="flyout">FrameId</code></a></td>
            <td><span data-ttu-id="aa2e5-149">Die ID des Frames, der abgetrennt wurde.</span><span class="sxs-lookup"><span data-stu-id="aa2e5-149">Id of the frame that has been detached.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="aa2e5-150">frameNavigated</span><span class="sxs-lookup"><span data-stu-id="aa2e5-150">frameNavigated</span></span>
<span data-ttu-id="aa2e5-151">Wird ausgelöst, sobald die Navigation des Frames abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="aa2e5-151">Fired once navigation of the frame has completed.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="aa2e5-152">Parameter</span><span class="sxs-lookup"><span data-stu-id="aa2e5-152">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="aa2e5-153">Frame</span><span class="sxs-lookup"><span data-stu-id="aa2e5-153">frame</span></span></td>
            <td><a href="#frame"><code class="flyout">Frame</code></a></td>
            <td><span data-ttu-id="aa2e5-154">Frame-Objekt</span><span class="sxs-lookup"><span data-stu-id="aa2e5-154">Frame object.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="aa2e5-155">loadEventFired</span><span class="sxs-lookup"><span data-stu-id="aa2e5-155">loadEventFired</span></span>
<span data-ttu-id="aa2e5-156">Entspricht dem Window. OnLoad-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="aa2e5-156">Corresponds to the window.onload event.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="aa2e5-157">Parameter</span><span class="sxs-lookup"><span data-stu-id="aa2e5-157">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="aa2e5-158">Timestamp</span><span class="sxs-lookup"><span data-stu-id="aa2e5-158">timestamp</span></span></td>
            <td><code class="flyout">number</code></td>
            <td><span data-ttu-id="aa2e5-159">Die Anzahl der Millisekunden seit Epoch.</span><span class="sxs-lookup"><span data-stu-id="aa2e5-159">Number of milliseconds since epoch.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="aa2e5-160">domContentEventFired</span><span class="sxs-lookup"><span data-stu-id="aa2e5-160">domContentEventFired</span></span>
<span data-ttu-id="aa2e5-161">Entspricht dem Document. onDOMContentLoaded-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="aa2e5-161">Corresponds to the document.onDOMContentLoaded event.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="aa2e5-162">Parameter</span><span class="sxs-lookup"><span data-stu-id="aa2e5-162">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="aa2e5-163">Timestamp</span><span class="sxs-lookup"><span data-stu-id="aa2e5-163">timestamp</span></span></td>
            <td><code class="flyout">number</code></td>
            <td><span data-ttu-id="aa2e5-164">Die Anzahl der Millisekunden seit Epoch.</span><span class="sxs-lookup"><span data-stu-id="aa2e5-164">Number of milliseconds since epoch.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

## <span data-ttu-id="aa2e5-165">Typen</span><span class="sxs-lookup"><span data-stu-id="aa2e5-165">Types</span></span>

### <a name="frameid"></a> <span data-ttu-id="aa2e5-166">Frame-Nr</span><span class="sxs-lookup"><span data-stu-id="aa2e5-166">FrameId</span></span> `string`

<span data-ttu-id="aa2e5-167">Eindeutige Frame-ID.</span><span class="sxs-lookup"><span data-stu-id="aa2e5-167">Unique frame identifier.</span></span>

</p>

---

### <a name="frame"></a> <span data-ttu-id="aa2e5-168">Frame</span><span class="sxs-lookup"><span data-stu-id="aa2e5-168">Frame</span></span> `object`

<span data-ttu-id="aa2e5-169">Informationen zum Frame auf der Seite.</span><span class="sxs-lookup"><span data-stu-id="aa2e5-169">Information about the Frame on the Page.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="aa2e5-170">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="aa2e5-170">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="aa2e5-171">id</span><span class="sxs-lookup"><span data-stu-id="aa2e5-171">id</span></span></td>
            <td><a href="#frameid"><code class="flyout">FrameId</code></a></td>
            <td><span data-ttu-id="aa2e5-172">Frame-eindeutiger Bezeichner</span><span class="sxs-lookup"><span data-stu-id="aa2e5-172">Frame unique identifier.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="aa2e5-173">parentID</span><span class="sxs-lookup"><span data-stu-id="aa2e5-173">parentId</span></span> <br/> <i><span data-ttu-id="aa2e5-174">Optional</span><span class="sxs-lookup"><span data-stu-id="aa2e5-174">optional</span></span></i></td>
            <td><a href="#frameid"><code class="flyout">FrameId</code></a></td>
            <td><span data-ttu-id="aa2e5-175">Eindeutiger Bezeichner des übergeordneten Frames</span><span class="sxs-lookup"><span data-stu-id="aa2e5-175">Parent frame unique identifier.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="aa2e5-176">name</span><span class="sxs-lookup"><span data-stu-id="aa2e5-176">name</span></span> <br/> <i><span data-ttu-id="aa2e5-177">Optional</span><span class="sxs-lookup"><span data-stu-id="aa2e5-177">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="aa2e5-178">Der Name des Frames, wie in der Kategorie angegeben.</span><span class="sxs-lookup"><span data-stu-id="aa2e5-178">Frame's name as specified in the tag.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="aa2e5-179">URL</span><span class="sxs-lookup"><span data-stu-id="aa2e5-179">url</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="aa2e5-180">Die URL des Frame-Dokuments.</span><span class="sxs-lookup"><span data-stu-id="aa2e5-180">Frame document's URL.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="aa2e5-181">securityOrigin</span><span class="sxs-lookup"><span data-stu-id="aa2e5-181">securityOrigin</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="aa2e5-182">Sicherheits Ursprung des Frame-Dokuments.</span><span class="sxs-lookup"><span data-stu-id="aa2e5-182">Frame document's security origin.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="aa2e5-183">mimeType</span><span class="sxs-lookup"><span data-stu-id="aa2e5-183">mimeType</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="aa2e5-184">Das vom Browser festgelegte MimeType-Dateiformat des Dokuments.</span><span class="sxs-lookup"><span data-stu-id="aa2e5-184">Frame document's mimeType as determined by the browser.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="frametree"></a> <span data-ttu-id="aa2e5-185">FrameTree</span><span class="sxs-lookup"><span data-stu-id="aa2e5-185">FrameTree</span></span> `object`

<span data-ttu-id="aa2e5-186">Informationen zur Frame Hierarchie.</span><span class="sxs-lookup"><span data-stu-id="aa2e5-186">Information about the Frame hierarchy.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="aa2e5-187">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="aa2e5-187">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="aa2e5-188">Frame</span><span class="sxs-lookup"><span data-stu-id="aa2e5-188">frame</span></span></td>
            <td><a href="#frame"><code class="flyout">Frame</code></a></td>
            <td><span data-ttu-id="aa2e5-189">Frame Informationen für dieses Strukturelement</span><span class="sxs-lookup"><span data-stu-id="aa2e5-189">Frame information for this tree item.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="aa2e5-190">childFrames</span><span class="sxs-lookup"><span data-stu-id="aa2e5-190">childFrames</span></span> <br/> <i><span data-ttu-id="aa2e5-191">Optional</span><span class="sxs-lookup"><span data-stu-id="aa2e5-191">optional</span></span></i></td>
            <td><a href="#frametree"><code class="flyout">FrameTree[]</code></a></td>
            <td><span data-ttu-id="aa2e5-192">Untergeordnete Frames</span><span class="sxs-lookup"><span data-stu-id="aa2e5-192">Child frames.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---
