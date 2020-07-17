---
description: Verweis auf die Seiten Domäne Aktionen und Ereignisse im Zusammenhang mit der geprüften Seite gehören der Seiten Domäne an.
title: Page Domain-devtools Protocol Version 0,2 (EdgeHTML)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/16/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.openlocfilehash: 864515eefbcb809e280f2ab1d81015018272c398
ms.sourcegitcommit: a06c86ef7c69e1e400a0be5938449f3c4ba6ec72
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/16/2020
ms.locfileid: "10882842"
---
# <span data-ttu-id="73c48-104">Page Domain-devtools Protocol Version 0,2 (EdgeHTML)</span><span class="sxs-lookup"><span data-stu-id="73c48-104">Page Domain - DevTools Protocol Version 0.2 (EdgeHTML)</span></span>  

<span data-ttu-id="73c48-105">Aktionen und Ereignisse im Zusammenhang mit der geprüften Seite gehören der Seiten Domäne an.</span><span class="sxs-lookup"><span data-stu-id="73c48-105">Actions and events related to the inspected page belong to the page domain.</span></span>

| | |
|-|-|
| [**<span data-ttu-id="73c48-106">Methoden</span><span class="sxs-lookup"><span data-stu-id="73c48-106">Methods</span></span>**](#methods) | <span data-ttu-id="73c48-107">[aktivieren](#enable), [Deaktivieren](#disable), [Navigieren](#navigate), [getFrameTree](#getframetree)</span><span class="sxs-lookup"><span data-stu-id="73c48-107">[enable](#enable), [disable](#disable), [navigate](#navigate), [getFrameTree](#getframetree)</span></span> |
| [**<span data-ttu-id="73c48-108">Veranstaltungen</span><span class="sxs-lookup"><span data-stu-id="73c48-108">Events</span></span>**](#events) | <span data-ttu-id="73c48-109">[frameAttached](#frameattached), [frameDetached](#framedetached), [frameNavigated](#framenavigated), [loadEventFired](#loadeventfired), [domContentEventFired](#domcontenteventfired)</span><span class="sxs-lookup"><span data-stu-id="73c48-109">[frameAttached](#frameattached), [frameDetached](#framedetached), [frameNavigated](#framenavigated), [loadEventFired](#loadeventfired), [domContentEventFired](#domcontenteventfired)</span></span> |
| [**<span data-ttu-id="73c48-110">Typen</span><span class="sxs-lookup"><span data-stu-id="73c48-110">Types</span></span>**](#types) | <span data-ttu-id="73c48-111">[Frame](#frameid)-Nr, [Frame](#frame), [FrameTree](#frametree)</span><span class="sxs-lookup"><span data-stu-id="73c48-111">[FrameId](#frameid), [Frame](#frame), [FrameTree](#frametree)</span></span> |
## <span data-ttu-id="73c48-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="73c48-112">Methods</span></span>

### <span data-ttu-id="73c48-113">Aktivieren</span><span class="sxs-lookup"><span data-stu-id="73c48-113">enable</span></span>
<span data-ttu-id="73c48-114">Aktiviert Seiten Domänen Benachrichtigungen.</span><span class="sxs-lookup"><span data-stu-id="73c48-114">Enables page domain notifications.</span></span>

</p>

---

### <span data-ttu-id="73c48-115">Deaktivieren </span><span class="sxs-lookup"><span data-stu-id="73c48-115">disable</span></span>
<span data-ttu-id="73c48-116">Deaktiviert Seiten Domänen Benachrichtigungen.</span><span class="sxs-lookup"><span data-stu-id="73c48-116">Disables page domain notifications.</span></span>

</p>

---

### <span data-ttu-id="73c48-117">Navigieren</span><span class="sxs-lookup"><span data-stu-id="73c48-117">navigate</span></span>
<span data-ttu-id="73c48-118">Navigiert die aktuelle Seite zur angegebenen URL.</span><span class="sxs-lookup"><span data-stu-id="73c48-118">Navigates current page to the given URL.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="73c48-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="73c48-119">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="73c48-120">URL</span><span class="sxs-lookup"><span data-stu-id="73c48-120">url</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="73c48-121">Die URL, zu der die Seite navigiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="73c48-121">URL to navigate the page to.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="73c48-122">Frame-Nr</span><span class="sxs-lookup"><span data-stu-id="73c48-122">frameId</span></span> <br/> <i><span data-ttu-id="73c48-123">Optional</span><span class="sxs-lookup"><span data-stu-id="73c48-123">optional</span></span></i></td>
            <td><a href="#frameid"><code class="flyout">FrameId</code></a></td>
            <td><span data-ttu-id="73c48-124">Die Frame-ID zum Navigieren.</span><span class="sxs-lookup"><span data-stu-id="73c48-124">Frame id to navigate.</span></span> <span data-ttu-id="73c48-125">Wenn keine Angabe erfolgt, navigiert die oberste Seite.</span><span class="sxs-lookup"><span data-stu-id="73c48-125">If not specified, will navigate the top page.</span></span></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="73c48-126">Gibt</span><span class="sxs-lookup"><span data-stu-id="73c48-126">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="73c48-127">Frame-Nr</span><span class="sxs-lookup"><span data-stu-id="73c48-127">frameId</span></span></td>
            <td><a href="#frameid"><code class="flyout">FrameId</code></a></td>
            <td><span data-ttu-id="73c48-128">Die Frame-ID, die navigiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="73c48-128">Frame id that will be navigated.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="73c48-129">getFrameTree</span><span class="sxs-lookup"><span data-stu-id="73c48-129">getFrameTree</span></span>
<span data-ttu-id="73c48-130">Gibt die aktuelle Frame Struktur zurück.</span><span class="sxs-lookup"><span data-stu-id="73c48-130">Returns present frame tree structure.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="73c48-131">Gibt</span><span class="sxs-lookup"><span data-stu-id="73c48-131">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="73c48-132">frameTree</span><span class="sxs-lookup"><span data-stu-id="73c48-132">frameTree</span></span></td>
            <td><a href="#frametree"><code class="flyout">FrameTree</code></a></td>
            <td><span data-ttu-id="73c48-133">Aktuelle Frame Struktur.</span><span class="sxs-lookup"><span data-stu-id="73c48-133">Present frame tree structure.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

## <span data-ttu-id="73c48-134">Veranstaltungen</span><span class="sxs-lookup"><span data-stu-id="73c48-134">Events</span></span>

### <span data-ttu-id="73c48-135">frameAttached</span><span class="sxs-lookup"><span data-stu-id="73c48-135">frameAttached</span></span>
<span data-ttu-id="73c48-136">Wird ausgelöst, wenn Frame dem übergeordneten Element angefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="73c48-136">Fired when frame has been attached to its parent.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="73c48-137">Parameter</span><span class="sxs-lookup"><span data-stu-id="73c48-137">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="73c48-138">Frame-Nr</span><span class="sxs-lookup"><span data-stu-id="73c48-138">frameId</span></span></td>
            <td><a href="#frameid"><code class="flyout">FrameId</code></a></td>
            <td><span data-ttu-id="73c48-139">Die ID des Rahmens, der angefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="73c48-139">Id of the frame that has been attached.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="73c48-140">parentFrameId</span><span class="sxs-lookup"><span data-stu-id="73c48-140">parentFrameId</span></span></td>
            <td><a href="#frameid"><code class="flyout">FrameId</code></a></td>
            <td><span data-ttu-id="73c48-141">Übergeordneter Frame Bezeichner</span><span class="sxs-lookup"><span data-stu-id="73c48-141">Parent frame identifier.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="73c48-142">Stapel</span><span class="sxs-lookup"><span data-stu-id="73c48-142">stack</span></span> <br/> <i><span data-ttu-id="73c48-143">Optional</span><span class="sxs-lookup"><span data-stu-id="73c48-143">optional</span></span></i></td>
            <td><a href="runtime.md#stacktrace"><code class="flyout">Runtime.StackTrace</code></a></td>
            <td><span data-ttu-id="73c48-144">JavaScript-Stapelüberwachung, wenn Frame angefügt wurde, nur festgelegt, wenn Frame vom Skript initiiert wurde.</span><span class="sxs-lookup"><span data-stu-id="73c48-144">JavaScript stack trace of when frame was attached, only set if frame initiated from script.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="73c48-145">frameDetached</span><span class="sxs-lookup"><span data-stu-id="73c48-145">frameDetached</span></span>
<span data-ttu-id="73c48-146">Wird ausgelöst, wenn Frame vom übergeordneten Element abgetrennt wurde.</span><span class="sxs-lookup"><span data-stu-id="73c48-146">Fired when frame has been detached from its parent.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="73c48-147">Parameter</span><span class="sxs-lookup"><span data-stu-id="73c48-147">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="73c48-148">Frame-Nr</span><span class="sxs-lookup"><span data-stu-id="73c48-148">frameId</span></span></td>
            <td><a href="#frameid"><code class="flyout">FrameId</code></a></td>
            <td><span data-ttu-id="73c48-149">Die ID des Frames, der abgetrennt wurde.</span><span class="sxs-lookup"><span data-stu-id="73c48-149">Id of the frame that has been detached.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="73c48-150">frameNavigated</span><span class="sxs-lookup"><span data-stu-id="73c48-150">frameNavigated</span></span>
<span data-ttu-id="73c48-151">Wird ausgelöst, sobald die Navigation des Frames abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="73c48-151">Fired once navigation of the frame has completed.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="73c48-152">Parameter</span><span class="sxs-lookup"><span data-stu-id="73c48-152">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="73c48-153">Frame</span><span class="sxs-lookup"><span data-stu-id="73c48-153">frame</span></span></td>
            <td><a href="#frame"><code class="flyout">Frame</code></a></td>
            <td><span data-ttu-id="73c48-154">Frame-Objekt</span><span class="sxs-lookup"><span data-stu-id="73c48-154">Frame object.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="73c48-155">loadEventFired</span><span class="sxs-lookup"><span data-stu-id="73c48-155">loadEventFired</span></span>
<span data-ttu-id="73c48-156">Entspricht dem Window. OnLoad-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="73c48-156">Corresponds to the window.onload event.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="73c48-157">Parameter</span><span class="sxs-lookup"><span data-stu-id="73c48-157">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="73c48-158">Timestamp</span><span class="sxs-lookup"><span data-stu-id="73c48-158">timestamp</span></span></td>
            <td><code class="flyout">number</code></td>
            <td><span data-ttu-id="73c48-159">Die Anzahl der Millisekunden seit Epoch.</span><span class="sxs-lookup"><span data-stu-id="73c48-159">Number of milliseconds since epoch.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="73c48-160">domContentEventFired</span><span class="sxs-lookup"><span data-stu-id="73c48-160">domContentEventFired</span></span>
<span data-ttu-id="73c48-161">Entspricht dem Document. onDOMContentLoaded-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="73c48-161">Corresponds to the document.onDOMContentLoaded event.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="73c48-162">Parameter</span><span class="sxs-lookup"><span data-stu-id="73c48-162">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="73c48-163">Timestamp</span><span class="sxs-lookup"><span data-stu-id="73c48-163">timestamp</span></span></td>
            <td><code class="flyout">number</code></td>
            <td><span data-ttu-id="73c48-164">Die Anzahl der Millisekunden seit Epoch.</span><span class="sxs-lookup"><span data-stu-id="73c48-164">Number of milliseconds since epoch.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

## <span data-ttu-id="73c48-165">Typen</span><span class="sxs-lookup"><span data-stu-id="73c48-165">Types</span></span>

### <a name="frameid"></a> <span data-ttu-id="73c48-166">Frame-Nr</span><span class="sxs-lookup"><span data-stu-id="73c48-166">FrameId</span></span> `string`

<span data-ttu-id="73c48-167">Eindeutige Frame-ID.</span><span class="sxs-lookup"><span data-stu-id="73c48-167">Unique frame identifier.</span></span>

</p>

---

### <a name="frame"></a> <span data-ttu-id="73c48-168">Frame</span><span class="sxs-lookup"><span data-stu-id="73c48-168">Frame</span></span> `object`

<span data-ttu-id="73c48-169">Informationen zum Frame auf der Seite.</span><span class="sxs-lookup"><span data-stu-id="73c48-169">Information about the Frame on the Page.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="73c48-170">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="73c48-170">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="73c48-171">id</span><span class="sxs-lookup"><span data-stu-id="73c48-171">id</span></span></td>
            <td><a href="#frameid"><code class="flyout">FrameId</code></a></td>
            <td><span data-ttu-id="73c48-172">Frame-eindeutiger Bezeichner</span><span class="sxs-lookup"><span data-stu-id="73c48-172">Frame unique identifier.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="73c48-173">parentID</span><span class="sxs-lookup"><span data-stu-id="73c48-173">parentId</span></span> <br/> <i><span data-ttu-id="73c48-174">Optional</span><span class="sxs-lookup"><span data-stu-id="73c48-174">optional</span></span></i></td>
            <td><a href="#frameid"><code class="flyout">FrameId</code></a></td>
            <td><span data-ttu-id="73c48-175">Eindeutiger Bezeichner des übergeordneten Frames</span><span class="sxs-lookup"><span data-stu-id="73c48-175">Parent frame unique identifier.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="73c48-176">name</span><span class="sxs-lookup"><span data-stu-id="73c48-176">name</span></span> <br/> <i><span data-ttu-id="73c48-177">Optional</span><span class="sxs-lookup"><span data-stu-id="73c48-177">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="73c48-178">Der Name des Frames, wie in der Kategorie angegeben.</span><span class="sxs-lookup"><span data-stu-id="73c48-178">Frame's name as specified in the tag.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="73c48-179">URL</span><span class="sxs-lookup"><span data-stu-id="73c48-179">url</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="73c48-180">Die URL des Frame-Dokuments.</span><span class="sxs-lookup"><span data-stu-id="73c48-180">Frame document's URL.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="73c48-181">securityOrigin</span><span class="sxs-lookup"><span data-stu-id="73c48-181">securityOrigin</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="73c48-182">Sicherheits Ursprung des Frame-Dokuments.</span><span class="sxs-lookup"><span data-stu-id="73c48-182">Frame document's security origin.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="73c48-183">mimeType</span><span class="sxs-lookup"><span data-stu-id="73c48-183">mimeType</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="73c48-184">Das vom Browser festgelegte MimeType-Dateiformat des Dokuments.</span><span class="sxs-lookup"><span data-stu-id="73c48-184">Frame document's mimeType as determined by the browser.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="frametree"></a> <span data-ttu-id="73c48-185">FrameTree</span><span class="sxs-lookup"><span data-stu-id="73c48-185">FrameTree</span></span> `object`

<span data-ttu-id="73c48-186">Informationen zur Frame Hierarchie.</span><span class="sxs-lookup"><span data-stu-id="73c48-186">Information about the Frame hierarchy.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="73c48-187">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="73c48-187">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="73c48-188">Frame</span><span class="sxs-lookup"><span data-stu-id="73c48-188">frame</span></span></td>
            <td><a href="#frame"><code class="flyout">Frame</code></a></td>
            <td><span data-ttu-id="73c48-189">Frame Informationen für dieses Strukturelement</span><span class="sxs-lookup"><span data-stu-id="73c48-189">Frame information for this tree item.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="73c48-190">childFrames</span><span class="sxs-lookup"><span data-stu-id="73c48-190">childFrames</span></span> <br/> <i><span data-ttu-id="73c48-191">Optional</span><span class="sxs-lookup"><span data-stu-id="73c48-191">optional</span></span></i></td>
            <td><a href="#frametree"><code class="flyout">FrameTree[]</code></a></td>
            <td><span data-ttu-id="73c48-192">Untergeordnete Frames</span><span class="sxs-lookup"><span data-stu-id="73c48-192">Child frames.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---
