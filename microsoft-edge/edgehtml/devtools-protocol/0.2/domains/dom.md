---
description: Referenz für die DOM-Domäne. Diese Domäne macht Dom-Lese-und Schreibvorgänge verfügbar. Jeder DOM-Knoten wird mit seinem Spiegelungs Objekt dargestellt, das über ein `id` . Damit `id` können zusätzliche Informationen auf dem Knoten abgerufen, in den JavaScript-Objektwrapper aufgelöst werden usw. Es ist wichtig, dass der Client DOM-Ereignisse nur für die Knoten empfängt, die dem Client bekannt sind. Das Back-End verfolgt die Knoten, die an den Client gesendet wurden, und sendet nie denselben Knoten zweimal. Es obliegt dem Kunden, Informationen zu den Knoten zu sammeln, die an den Client gesendet wurden.<p>Beachten Sie, dass `iframe` Besitzer Elemente die entsprechenden Dokumentelemente als untergeordnete Knoten zurückgeben.</p>
title: Dom-Domäne – devtools-Protokoll, Version 0,2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: reference
ms.prod: microsoft-edge
ms.custom: seodec18
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 7d9861a2395f7b24142a41efea9ac599907dec27
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11234014"
---
# <span data-ttu-id="e00ee-109">DOM</span><span class="sxs-lookup"><span data-stu-id="e00ee-109">DOM</span></span>

<span data-ttu-id="e00ee-110">Diese Domäne macht Dom-Lese-und Schreibvorgänge verfügbar.</span><span class="sxs-lookup"><span data-stu-id="e00ee-110">This domain exposes DOM read/write operations.</span></span> <span data-ttu-id="e00ee-111">Jeder DOM-Knoten wird mit seinem Spiegelungs Objekt dargestellt, das über ein `id` .</span><span class="sxs-lookup"><span data-stu-id="e00ee-111">Each DOM Node is represented with its mirror object that has an `id`.</span></span> <span data-ttu-id="e00ee-112">Damit `id` können zusätzliche Informationen auf dem Knoten abgerufen, in den JavaScript-Objektwrapper aufgelöst werden usw. Es ist wichtig, dass der Client DOM-Ereignisse nur für die Knoten empfängt, die dem Client bekannt sind.</span><span class="sxs-lookup"><span data-stu-id="e00ee-112">This `id` can be used to get additional information on the Node, resolve it into the JavaScript object wrapper, etc. It is important that client receives DOM events only for the nodes that are known to the client.</span></span> <span data-ttu-id="e00ee-113">Das Back-End verfolgt die Knoten, die an den Client gesendet wurden, und sendet nie denselben Knoten zweimal.</span><span class="sxs-lookup"><span data-stu-id="e00ee-113">Backend keeps track of the nodes that were sent to the client and never sends the same node twice.</span></span> <span data-ttu-id="e00ee-114">Es obliegt dem Kunden, Informationen zu den Knoten zu sammeln, die an den Client gesendet wurden.</span><span class="sxs-lookup"><span data-stu-id="e00ee-114">It is client's responsibility to collect information about the nodes that were sent to the client.</span></span><p><span data-ttu-id="e00ee-115">Beachten Sie, dass `iframe` Besitzer Elemente die entsprechenden Dokumentelemente als untergeordnete Knoten zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="e00ee-115">Note that `iframe` owner elements will return corresponding document elements as their child nodes.</span></span></p>

| | |
|-|-|
| [**<span data-ttu-id="e00ee-116">Methoden</span><span class="sxs-lookup"><span data-stu-id="e00ee-116">Methods</span></span>**](#methods) | <span data-ttu-id="e00ee-117">[aktivieren](#enable), [Deaktivieren](#disable), [GetDocument](#getdocument), [highlightNode](#highlightnode), [hideHighlight](#hidehighlight), [requestChildNodes](#requestchildnodes), [GetAttributes](#getattributes), [getOuterHTML](#getouterhtml), [pushNodesByBackendIdsToFrontend](#pushnodesbybackendidstofrontend), [querySelector](#queryselector), [querySelectorAll](#queryselectorall), [requestNode](#requestnode), [resolveNode](#resolvenode), [setInspectedNode](#setinspectednode)</span><span class="sxs-lookup"><span data-stu-id="e00ee-117">[enable](#enable), [disable](#disable), [getDocument](#getdocument), [highlightNode](#highlightnode), [hideHighlight](#hidehighlight), [requestChildNodes](#requestchildnodes), [getAttributes](#getattributes), [getOuterHTML](#getouterhtml), [pushNodesByBackendIdsToFrontend](#pushnodesbybackendidstofrontend), [querySelector](#queryselector), [querySelectorAll](#queryselectorall), [requestNode](#requestnode), [resolveNode](#resolvenode), [setInspectedNode](#setinspectednode)</span></span> |
| [**<span data-ttu-id="e00ee-118">Veranstaltungen</span><span class="sxs-lookup"><span data-stu-id="e00ee-118">Events</span></span>**](#events) | <span data-ttu-id="e00ee-119">[setChildNodes](#setchildnodes), [attributeModified](#attributemodified), [attributeRemoved](#attributeremoved), [characterDataModified](#characterdatamodified), [childNodeInserted](#childnodeinserted), [childNodeRemoved](#childnoderemoved), [documentUpdated](#documentupdated)</span><span class="sxs-lookup"><span data-stu-id="e00ee-119">[setChildNodes](#setchildnodes), [attributeModified](#attributemodified), [attributeRemoved](#attributeremoved), [characterDataModified](#characterdatamodified), [childNodeInserted](#childnodeinserted), [childNodeRemoved](#childnoderemoved), [documentUpdated](#documentupdated)</span></span> |
| [**<span data-ttu-id="e00ee-120">Typen</span><span class="sxs-lookup"><span data-stu-id="e00ee-120">Types</span></span>**](#types) | <span data-ttu-id="e00ee-121">[RGBA](#rgba), [HighlightConfig](#highlightconfig), [Knoten](#nodeid)-Nr, [Knoten](#node), [BackendNodeId](#backendnodeid), [Pseudotyp](#pseudotype)</span><span class="sxs-lookup"><span data-stu-id="e00ee-121">[RGBA](#rgba), [HighlightConfig](#highlightconfig), [NodeId](#nodeid), [Node](#node), [BackendNodeId](#backendnodeid), [PseudoType](#pseudotype)</span></span> |
| [**<span data-ttu-id="e00ee-122">Abhängigkeiten</span><span class="sxs-lookup"><span data-stu-id="e00ee-122">Dependencies</span></span>**](#dependencies) | [<span data-ttu-id="e00ee-123">Laufzeit</span><span class="sxs-lookup"><span data-stu-id="e00ee-123">Runtime</span></span>](runtime.md) |
## <span data-ttu-id="e00ee-124">Methoden</span><span class="sxs-lookup"><span data-stu-id="e00ee-124">Methods</span></span>

### <span data-ttu-id="e00ee-125">Aktivieren</span><span class="sxs-lookup"><span data-stu-id="e00ee-125">enable</span></span>
<span data-ttu-id="e00ee-126">Aktiviert den Dom-Agent für die angegebene Seite.</span><span class="sxs-lookup"><span data-stu-id="e00ee-126">Enables DOM agent for the given page.</span></span>

</p>

---

### <span data-ttu-id="e00ee-127">Deaktivieren </span><span class="sxs-lookup"><span data-stu-id="e00ee-127">disable</span></span>
<span data-ttu-id="e00ee-128">Deaktiviert den Dom-Agent für die angegebene Seite.</span><span class="sxs-lookup"><span data-stu-id="e00ee-128">Disables DOM agent for the given page.</span></span> <span data-ttu-id="e00ee-129">Durch das Deaktivieren des DOM werden alle zuvor gültigen nodeIds ungültig.</span><span class="sxs-lookup"><span data-stu-id="e00ee-129">Disabling the DOM will invalidate any previously valid nodeIds.</span></span>

</p>

---

### <span data-ttu-id="e00ee-130">getDocument</span><span class="sxs-lookup"><span data-stu-id="e00ee-130">getDocument</span></span>
<span data-ttu-id="e00ee-131">Gibt den Dom-Stammknoten (und optional die Unterstruktur) für den Aufrufer zurück.</span><span class="sxs-lookup"><span data-stu-id="e00ee-131">Returns the root DOM node (and optionally the subtree) to the caller.</span></span> <span data-ttu-id="e00ee-132">Durch das Aufrufen `getDocument` werden alle zuvor gültigen nodeIds ungültig.</span><span class="sxs-lookup"><span data-stu-id="e00ee-132">Calling `getDocument` will invalidate any previously valid nodeIds</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="e00ee-133">Parameter</span><span class="sxs-lookup"><span data-stu-id="e00ee-133">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="e00ee-134">Tiefe</span><span class="sxs-lookup"><span data-stu-id="e00ee-134">depth</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="e00ee-135">Die maximale Tiefe, mit der untergeordnete Elemente abgerufen werden sollen, standardmäßig 2.</span><span class="sxs-lookup"><span data-stu-id="e00ee-135">The maximum depth at which children should be retrieved, defaults to 2.</span></span> <span data-ttu-id="e00ee-136">Verwenden Sie-1 für die gesamte Unterstruktur.</span><span class="sxs-lookup"><span data-stu-id="e00ee-136">Use -1 for entire subtree.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e00ee-137">Pierce</span><span class="sxs-lookup"><span data-stu-id="e00ee-137">pierce</span></span></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="e00ee-138">Ob iframes durchlaufen werden sollen, wenn die Teilstruktur zurückgegeben wird (Standard ist falsch).</span><span class="sxs-lookup"><span data-stu-id="e00ee-138">Whether or not iframes should be traversed when returning the subtree (default is false).</span></span></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="e00ee-139">Gibt</span><span class="sxs-lookup"><span data-stu-id="e00ee-139">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="e00ee-140">Stamm</span><span class="sxs-lookup"><span data-stu-id="e00ee-140">root</span></span></td>
            <td><a href="#node"><code class="flyout">Node</code></a></td>
            <td><span data-ttu-id="e00ee-141">Resultierender Knoten</span><span class="sxs-lookup"><span data-stu-id="e00ee-141">Resulting Node.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="e00ee-142">highlightNode</span><span class="sxs-lookup"><span data-stu-id="e00ee-142">highlightNode</span></span>
<span data-ttu-id="e00ee-143">Higlights-DOM-Knoten mit angegebener ID oder Objektwrapper.</span><span class="sxs-lookup"><span data-stu-id="e00ee-143">Higlights DOM node with given id or object wrapper.</span></span> <span data-ttu-id="e00ee-144">Knoten-backendNodeId oder ObjectID muss angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="e00ee-144">nodeId, backendNodeId, or objectId must be specified.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="e00ee-145">Parameter</span><span class="sxs-lookup"><span data-stu-id="e00ee-145">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="e00ee-146">NodeId</span><span class="sxs-lookup"><span data-stu-id="e00ee-146">nodeId</span></span> <br/> <i><span data-ttu-id="e00ee-147">Optional</span><span class="sxs-lookup"><span data-stu-id="e00ee-147">optional</span></span></i></td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td><span data-ttu-id="e00ee-148">Der Bezeichner des Knotens, der markiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="e00ee-148">Identifier of the node to highlight.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e00ee-149">backendNodeId</span><span class="sxs-lookup"><span data-stu-id="e00ee-149">backendNodeId</span></span> <br/> <i><span data-ttu-id="e00ee-150">Optional</span><span class="sxs-lookup"><span data-stu-id="e00ee-150">optional</span></span></i></td>
            <td><a href="#backendnodeid"><code class="flyout">BackendNodeId</code></a></td>
            <td><span data-ttu-id="e00ee-151">Der Bezeichner des zu markierenden Back-End-Knotens.</span><span class="sxs-lookup"><span data-stu-id="e00ee-151">Identifier of the backend node to highlight.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e00ee-152">ObjectID</span><span class="sxs-lookup"><span data-stu-id="e00ee-152">objectId</span></span> <br/> <i><span data-ttu-id="e00ee-153">Optional</span><span class="sxs-lookup"><span data-stu-id="e00ee-153">optional</span></span></i></td>
            <td><a href="runtime.md#remoteobjectid"><code class="flyout">Runtime.RemoteObjectId</code></a></td>
            <td><span data-ttu-id="e00ee-154">JavaScript-Objekt-ID des Knotens, der hervorgehoben werden soll.</span><span class="sxs-lookup"><span data-stu-id="e00ee-154">JavaScript object id of the node to be highlighted.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e00ee-155">higlightConfig</span><span class="sxs-lookup"><span data-stu-id="e00ee-155">higlightConfig</span></span></td>
            <td><a href="#highlightconfig"><code class="flyout">HighlightConfig</code></a></td>
            <td><span data-ttu-id="e00ee-156">Deskriptor der Hervorhebungs Darstellung</span><span class="sxs-lookup"><span data-stu-id="e00ee-156">Descriptor of the highlight appearance.</span></span></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="e00ee-157">Gibt</span><span class="sxs-lookup"><span data-stu-id="e00ee-157">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="e00ee-158">Stamm</span><span class="sxs-lookup"><span data-stu-id="e00ee-158">root</span></span></td>
            <td><a href="#node"><code class="flyout">Node</code></a></td>
            <td><span data-ttu-id="e00ee-159">Resultierender Knoten</span><span class="sxs-lookup"><span data-stu-id="e00ee-159">Resulting Node.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="e00ee-160">hideHighlight</span><span class="sxs-lookup"><span data-stu-id="e00ee-160">hideHighlight</span></span>
<span data-ttu-id="e00ee-161">Blendet jede aktuelle DOM-Knoten Hervorhebung aus.</span><span class="sxs-lookup"><span data-stu-id="e00ee-161">Hides any current DOM node highlight.</span></span>

</p>

---

### <span data-ttu-id="e00ee-162">requestChildNodes</span><span class="sxs-lookup"><span data-stu-id="e00ee-162">requestChildNodes</span></span>
<span data-ttu-id="e00ee-163">Fordert an, dass untergeordnete Elemente des Knotens mit der angegebenen ID in Form von Ereignissen an den Anrufer zurückgegeben werden `setChildNodes` .</span><span class="sxs-lookup"><span data-stu-id="e00ee-163">Requests that children of the node with given id are returned to ghe caller in the form of `setChildNodes` events.</span></span> `setChildNodes` <span data-ttu-id="e00ee-164">wird für jeden Knoten ausgelöst, dessen untergeordnete Elemente zuvor nicht zurückgegeben wurden, beginnend mit dem angeforderten Knoten bis zur angegebenen Tiefe.</span><span class="sxs-lookup"><span data-stu-id="e00ee-164">will be fired for each node that has not previously returned it's children, starting from the requested node down to the specified depth.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="e00ee-165">Parameter</span><span class="sxs-lookup"><span data-stu-id="e00ee-165">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="e00ee-166">NodeId</span><span class="sxs-lookup"><span data-stu-id="e00ee-166">nodeId</span></span></td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td><span data-ttu-id="e00ee-167">Die ID des Knotens, von dem untergeordnete Elemente abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="e00ee-167">Id of the node to get children from.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e00ee-168">Tiefe</span><span class="sxs-lookup"><span data-stu-id="e00ee-168">depth</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="e00ee-169">Die maximale Tiefe, mit der untergeordnete Elemente abgerufen werden sollen, wird standardmäßig auf 1 festgesetzt.</span><span class="sxs-lookup"><span data-stu-id="e00ee-169">The maximum depth at which children should be retrieved, defaults to 1.</span></span> <span data-ttu-id="e00ee-170">Verwenden Sie-1 für die gesamte Unterstruktur.</span><span class="sxs-lookup"><span data-stu-id="e00ee-170">Use -1 for entire subtree.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e00ee-171">Pierce</span><span class="sxs-lookup"><span data-stu-id="e00ee-171">pierce</span></span></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="e00ee-172">Ob iframes durchlaufen werden sollen, wenn die Teilstruktur zurückgegeben wird (Standard ist falsch).</span><span class="sxs-lookup"><span data-stu-id="e00ee-172">Whether or not iframes should be traversed when returning the subtree (default is false).</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="e00ee-173">GetAttributes</span><span class="sxs-lookup"><span data-stu-id="e00ee-173">getAttributes</span></span>
<span data-ttu-id="e00ee-174">Gibt Attribute für den angegebenen Knoten zurück.</span><span class="sxs-lookup"><span data-stu-id="e00ee-174">Returns attributes for the specified node.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="e00ee-175">Parameter</span><span class="sxs-lookup"><span data-stu-id="e00ee-175">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="e00ee-176">NodeId</span><span class="sxs-lookup"><span data-stu-id="e00ee-176">nodeId</span></span></td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td><span data-ttu-id="e00ee-177">Die ID des Knotens, für den attibutes abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="e00ee-177">Id of the node to retrieve attibutes for.</span></span></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="e00ee-178">Gibt</span><span class="sxs-lookup"><span data-stu-id="e00ee-178">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="e00ee-179">Attribute</span><span class="sxs-lookup"><span data-stu-id="e00ee-179">attributes</span></span></td>
            <td><code class="flyout">string[]</code></td>
            <td><span data-ttu-id="e00ee-180">Ein Interleaved-Array mit Namen und Werten von Knoten Attributen.</span><span class="sxs-lookup"><span data-stu-id="e00ee-180">An interleaved array of node attribute names and values.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="e00ee-181">getOuterHTML</span><span class="sxs-lookup"><span data-stu-id="e00ee-181">getOuterHTML</span></span>
<span data-ttu-id="e00ee-182">Gibt das HTML-Markup des Knotens zurück.</span><span class="sxs-lookup"><span data-stu-id="e00ee-182">Returns node's HTML markup.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="e00ee-183">Parameter</span><span class="sxs-lookup"><span data-stu-id="e00ee-183">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="e00ee-184">NodeId</span><span class="sxs-lookup"><span data-stu-id="e00ee-184">nodeId</span></span> <br/> <i><span data-ttu-id="e00ee-185">Optional</span><span class="sxs-lookup"><span data-stu-id="e00ee-185">optional</span></span></i></td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td><span data-ttu-id="e00ee-186">Der Bezeichner des Knotens.</span><span class="sxs-lookup"><span data-stu-id="e00ee-186">Identifier of the node.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e00ee-187">backendNodeId</span><span class="sxs-lookup"><span data-stu-id="e00ee-187">backendNodeId</span></span> <br/> <i><span data-ttu-id="e00ee-188">Optional</span><span class="sxs-lookup"><span data-stu-id="e00ee-188">optional</span></span></i></td>
            <td><a href="#backendnodeid"><code class="flyout">BackendNodeId</code></a></td>
            <td><span data-ttu-id="e00ee-189">Der Bezeichner des Back-End-Knotens.</span><span class="sxs-lookup"><span data-stu-id="e00ee-189">Identifier of the backend node.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e00ee-190">ObjectID</span><span class="sxs-lookup"><span data-stu-id="e00ee-190">objectId</span></span> <br/> <i><span data-ttu-id="e00ee-191">Optional</span><span class="sxs-lookup"><span data-stu-id="e00ee-191">optional</span></span></i></td>
            <td><a href="runtime.md#remoteobjectid"><code class="flyout">Runtime.RemoteObjectId</code></a></td>
            <td><span data-ttu-id="e00ee-192">JavaScript-Objekt-ID des Knoten Wrappers.</span><span class="sxs-lookup"><span data-stu-id="e00ee-192">JavaScript object id of the node wrapper.</span></span></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="e00ee-193">Gibt</span><span class="sxs-lookup"><span data-stu-id="e00ee-193">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="e00ee-194">outerHTML</span><span class="sxs-lookup"><span data-stu-id="e00ee-194">outerHTML</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="e00ee-195">Äußeres HTML-Markup.</span><span class="sxs-lookup"><span data-stu-id="e00ee-195">Outer HTML markup.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="e00ee-196">pushNodesByBackendIdsToFrontend</span><span class="sxs-lookup"><span data-stu-id="e00ee-196">pushNodesByBackendIdsToFrontend</span></span>
<span data-ttu-id="e00ee-197">Sucht nach Knoten-IDs und löst alle übergeordneten Elemente für die angegebenen Back-End-Knoten-IDs auf</span><span class="sxs-lookup"><span data-stu-id="e00ee-197">Looks up Node Ids and resolves all parents for the specified Backend Node Ids</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="e00ee-198">Parameter</span><span class="sxs-lookup"><span data-stu-id="e00ee-198">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="e00ee-199">backendNodeIds</span><span class="sxs-lookup"><span data-stu-id="e00ee-199">backendNodeIds</span></span></td>
            <td><a href="#backendnodeid"><code class="flyout">BackendNodeId[]</code></a></td>
            <td><span data-ttu-id="e00ee-200">Back-End-Knoten-IDs der zu lösenden Knoten</span><span class="sxs-lookup"><span data-stu-id="e00ee-200">Backend Node IDs of the nodes to resolve</span></span></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="e00ee-201">Gibt</span><span class="sxs-lookup"><span data-stu-id="e00ee-201">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="e00ee-202">nodeIds</span><span class="sxs-lookup"><span data-stu-id="e00ee-202">nodeIds</span></span></td>
            <td><a href="#node"><code class="flyout">Node[]</code></a></td>
            <td><span data-ttu-id="e00ee-203">Knoten-IDs der aufgelösten Knoten</span><span class="sxs-lookup"><span data-stu-id="e00ee-203">Node Ids of the resolved nodes</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="e00ee-204">querySelector</span><span class="sxs-lookup"><span data-stu-id="e00ee-204">querySelector</span></span>
<span data-ttu-id="e00ee-205">Wird `querySelector` für einen bestimmten Knoten ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e00ee-205">Executes `querySelector` on a given node.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="e00ee-206">Parameter</span><span class="sxs-lookup"><span data-stu-id="e00ee-206">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="e00ee-207">NodeId</span><span class="sxs-lookup"><span data-stu-id="e00ee-207">nodeId</span></span></td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td><span data-ttu-id="e00ee-208">Die ID des Knotens, nach dem abgefragt werden soll.</span><span class="sxs-lookup"><span data-stu-id="e00ee-208">Id of the node to query upon.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e00ee-209">Auswahl</span><span class="sxs-lookup"><span data-stu-id="e00ee-209">selector</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="e00ee-210">Die Auswahlzeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="e00ee-210">The selector string.</span></span></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="e00ee-211">Gibt</span><span class="sxs-lookup"><span data-stu-id="e00ee-211">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="e00ee-212">NodeId</span><span class="sxs-lookup"><span data-stu-id="e00ee-212">nodeId</span></span></td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td><span data-ttu-id="e00ee-213">Abfrageauswahl Ergebnis.</span><span class="sxs-lookup"><span data-stu-id="e00ee-213">Query selector result.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="e00ee-214">querySelectorAll</span><span class="sxs-lookup"><span data-stu-id="e00ee-214">querySelectorAll</span></span>
<span data-ttu-id="e00ee-215">Wird `querySelectorAll` für einen bestimmten Knoten ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e00ee-215">Executes `querySelectorAll` on a given node.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="e00ee-216">Parameter</span><span class="sxs-lookup"><span data-stu-id="e00ee-216">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="e00ee-217">NodeId</span><span class="sxs-lookup"><span data-stu-id="e00ee-217">nodeId</span></span></td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td><span data-ttu-id="e00ee-218">Die ID des Knotens, nach dem abgefragt werden soll.</span><span class="sxs-lookup"><span data-stu-id="e00ee-218">Id of the node to query upon.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e00ee-219">Auswahl</span><span class="sxs-lookup"><span data-stu-id="e00ee-219">selector</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="e00ee-220">Die Auswahlzeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="e00ee-220">The selector string.</span></span></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="e00ee-221">Gibt</span><span class="sxs-lookup"><span data-stu-id="e00ee-221">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="e00ee-222">nodeIds</span><span class="sxs-lookup"><span data-stu-id="e00ee-222">nodeIds</span></span></td>
            <td><a href="#nodeid"><code class="flyout">NodeId[]</code></a></td>
            <td><span data-ttu-id="e00ee-223">Abfrageauswahl Ergebnisse.</span><span class="sxs-lookup"><span data-stu-id="e00ee-223">Query selector results.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="e00ee-224">requestNode</span><span class="sxs-lookup"><span data-stu-id="e00ee-224">requestNode</span></span>
<span data-ttu-id="e00ee-225">Fordert an, dass der Knoten mit der angegebenen Remoteobjekt-ID an den Anrufer gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="e00ee-225">Requests that the node with given remote object Id is sent to caller.</span></span> <span data-ttu-id="e00ee-226">Alle Knoten, die den Pfad vom Knoten zum Stamm bilden, werden auch als eine Reihe von Benachrichtigungen an den Client gesendet `setChildNodes` .</span><span class="sxs-lookup"><span data-stu-id="e00ee-226">All nodes that form the path from the node to the root are also sent to the client as a series of `setChildNodes` notifications.</span></span> <span data-ttu-id="e00ee-227">gibt 0 zurück, wenn das Dokument, das den angeforderten Knoten enthält, nicht zuvor vom Client angefordert wurde.</span><span class="sxs-lookup"><span data-stu-id="e00ee-227">returns 0 if the document containing the requested node has not previously been requested by the client.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="e00ee-228">Parameter</span><span class="sxs-lookup"><span data-stu-id="e00ee-228">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="e00ee-229">ObjectID</span><span class="sxs-lookup"><span data-stu-id="e00ee-229">objectId</span></span></td>
            <td><a href="runtime.md#remoteobjectid"><code class="flyout">Runtime.RemoteObjectId</code></a></td>
            <td><span data-ttu-id="e00ee-230">JavaScript-Objekt-ID, die in Knoten konvertiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="e00ee-230">JavaScript object Id to convert into node.</span></span></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="e00ee-231">Gibt</span><span class="sxs-lookup"><span data-stu-id="e00ee-231">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="e00ee-232">NodeId</span><span class="sxs-lookup"><span data-stu-id="e00ee-232">nodeId</span></span></td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td><span data-ttu-id="e00ee-233">Knoten-ID für das angegebene Objekt.</span><span class="sxs-lookup"><span data-stu-id="e00ee-233">Node Id for given object.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="e00ee-234">resolveNode</span><span class="sxs-lookup"><span data-stu-id="e00ee-234">resolveNode</span></span>
<span data-ttu-id="e00ee-235">Löst das JavaScript-Knotenobjekt für eine angegebene Knoten-oder BackendNodeId auf.</span><span class="sxs-lookup"><span data-stu-id="e00ee-235">Resolves the JavaScript node object for a given NodeId or BackendNodeId.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="e00ee-236">Parameter</span><span class="sxs-lookup"><span data-stu-id="e00ee-236">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="e00ee-237">NodeId</span><span class="sxs-lookup"><span data-stu-id="e00ee-237">nodeId</span></span> <br/> <i><span data-ttu-id="e00ee-238">Optional</span><span class="sxs-lookup"><span data-stu-id="e00ee-238">optional</span></span></i></td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td><span data-ttu-id="e00ee-239">Die ID des zu lösenden Knotens.</span><span class="sxs-lookup"><span data-stu-id="e00ee-239">Id of the node to resolve.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e00ee-240">backendNodeId</span><span class="sxs-lookup"><span data-stu-id="e00ee-240">backendNodeId</span></span> <br/> <i><span data-ttu-id="e00ee-241">Optional</span><span class="sxs-lookup"><span data-stu-id="e00ee-241">optional</span></span></i></td>
            <td><a href="#backendnodeid"><code class="flyout">BackendNodeId</code></a></td>
            <td><span data-ttu-id="e00ee-242">Die Back-End-Knoten-ID des zu lösenden Knotens.</span><span class="sxs-lookup"><span data-stu-id="e00ee-242">Backend Node Id of the node to resolve.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e00ee-243">objectGroup</span><span class="sxs-lookup"><span data-stu-id="e00ee-243">objectGroup</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="e00ee-244">Symbolischer Gruppenname, der zum Freigeben mehrerer Objekte verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="e00ee-244">Symbolic group name that can be used to release multiple objects.</span></span></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="e00ee-245">Gibt</span><span class="sxs-lookup"><span data-stu-id="e00ee-245">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="e00ee-246">Objekt</span><span class="sxs-lookup"><span data-stu-id="e00ee-246">object</span></span></td>
            <td><a href="runtime.md#remoteobject"><code class="flyout">Runtime.RemoteObject</code></a></td>
            <td><span data-ttu-id="e00ee-247">JavaScript-Objektwrapper für gegebenen Knoten</span><span class="sxs-lookup"><span data-stu-id="e00ee-247">JavaScript object wrapper for given node.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="e00ee-248">setInspectedNode</span><span class="sxs-lookup"><span data-stu-id="e00ee-248">setInspectedNode</span></span>
<span><b><span data-ttu-id="e00ee-249">Experimenteller.</span><span class="sxs-lookup"><span data-stu-id="e00ee-249">Experimental.</span></span> </b></span><span data-ttu-id="e00ee-250">Ermöglicht es Console, auf den vorherigen überprüften Knoten mit der angegebenen ID über $0-$ 4 zu verweisen.</span><span class="sxs-lookup"><span data-stu-id="e00ee-250">Enables console to refer to the previous inspected node with given id via $0-$4.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="e00ee-251">Parameter</span><span class="sxs-lookup"><span data-stu-id="e00ee-251">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="e00ee-252">NodeId</span><span class="sxs-lookup"><span data-stu-id="e00ee-252">nodeId</span></span></td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td><span data-ttu-id="e00ee-253">DOM-Knoten-ID, auf die mithilfe von $0-$ 4 in der Befehlszeilen-API zugegriffen werden kann.</span><span class="sxs-lookup"><span data-stu-id="e00ee-253">DOM node id to be accessible by means of $0-$4 in command line API.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

## <span data-ttu-id="e00ee-254">Veranstaltungen</span><span class="sxs-lookup"><span data-stu-id="e00ee-254">Events</span></span>

### <span data-ttu-id="e00ee-255">setChildNodes</span><span class="sxs-lookup"><span data-stu-id="e00ee-255">setChildNodes</span></span>
<span data-ttu-id="e00ee-256">Wird ausgelöst, wenn das Back-End dem Client eine fehlende DOM-Struktur bereitstellen möchte.</span><span class="sxs-lookup"><span data-stu-id="e00ee-256">Fired when the backend wishes to provide client with missing DOM structure.</span></span> <span data-ttu-id="e00ee-257">Dies geschieht bei den meisten anrufen, die nodeIds anfordern.</span><span class="sxs-lookup"><span data-stu-id="e00ee-257">This happens upon most calls requesting nodeIds</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="e00ee-258">Parameter</span><span class="sxs-lookup"><span data-stu-id="e00ee-258">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="e00ee-259">parentID</span><span class="sxs-lookup"><span data-stu-id="e00ee-259">parentId</span></span></td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td><span data-ttu-id="e00ee-260">Übergeordneter Knoten für poplate mit untergeordneten Elementen.</span><span class="sxs-lookup"><span data-stu-id="e00ee-260">Parent node to poplate with children.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e00ee-261">Knoten</span><span class="sxs-lookup"><span data-stu-id="e00ee-261">nodes</span></span></td>
            <td><a href="#nodeid"><code class="flyout">NodeId[]</code></a></td>
            <td><span data-ttu-id="e00ee-262">Array für untergeordnete Knoten</span><span class="sxs-lookup"><span data-stu-id="e00ee-262">Child nodes array.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="e00ee-263">attributeModified</span><span class="sxs-lookup"><span data-stu-id="e00ee-263">attributeModified</span></span>
<span data-ttu-id="e00ee-264">Wird ausgelöst `Element` , wenn das Attribut geändert wird.</span><span class="sxs-lookup"><span data-stu-id="e00ee-264">Fired when `Element`'s attribute is modified.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="e00ee-265">Parameter</span><span class="sxs-lookup"><span data-stu-id="e00ee-265">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="e00ee-266">NodeId</span><span class="sxs-lookup"><span data-stu-id="e00ee-266">nodeId</span></span></td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td><span data-ttu-id="e00ee-267">Die ID des Knotens, der sich geändert hat.</span><span class="sxs-lookup"><span data-stu-id="e00ee-267">Id of the node that has changed.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e00ee-268">name</span><span class="sxs-lookup"><span data-stu-id="e00ee-268">name</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="e00ee-269">Attribut Name.</span><span class="sxs-lookup"><span data-stu-id="e00ee-269">Attribute name.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e00ee-270">value</span><span class="sxs-lookup"><span data-stu-id="e00ee-270">value</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="e00ee-271">Attributwert.</span><span class="sxs-lookup"><span data-stu-id="e00ee-271">Attribute value.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="e00ee-272">attributeRemoved</span><span class="sxs-lookup"><span data-stu-id="e00ee-272">attributeRemoved</span></span>
<span data-ttu-id="e00ee-273">Wird ausgelöst `Element` , wenn das Attribut entfernt wurde.</span><span class="sxs-lookup"><span data-stu-id="e00ee-273">Fired when `Element`'s attribute is removed.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="e00ee-274">Parameter</span><span class="sxs-lookup"><span data-stu-id="e00ee-274">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="e00ee-275">NodeId</span><span class="sxs-lookup"><span data-stu-id="e00ee-275">nodeId</span></span></td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td><span data-ttu-id="e00ee-276">Die ID des Knotens, der sich geändert hat.</span><span class="sxs-lookup"><span data-stu-id="e00ee-276">Id of the node that has changed.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e00ee-277">name</span><span class="sxs-lookup"><span data-stu-id="e00ee-277">name</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="e00ee-278">Attribut Name.</span><span class="sxs-lookup"><span data-stu-id="e00ee-278">Attribute name.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="e00ee-279">characterDataModified</span><span class="sxs-lookup"><span data-stu-id="e00ee-279">characterDataModified</span></span>
<span data-ttu-id="e00ee-280">Mirrors `DOMCharacterDataModified` -Ereignis.</span><span class="sxs-lookup"><span data-stu-id="e00ee-280">Mirrors `DOMCharacterDataModified` event.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="e00ee-281">Parameter</span><span class="sxs-lookup"><span data-stu-id="e00ee-281">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="e00ee-282">NodeId</span><span class="sxs-lookup"><span data-stu-id="e00ee-282">nodeId</span></span></td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td><span data-ttu-id="e00ee-283">Die ID des Knotens, der sich geändert hat.</span><span class="sxs-lookup"><span data-stu-id="e00ee-283">Id of the node that has changed.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e00ee-284">charcterData</span><span class="sxs-lookup"><span data-stu-id="e00ee-284">charcterData</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="e00ee-285">Neuer Textwert.</span><span class="sxs-lookup"><span data-stu-id="e00ee-285">New text value.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="e00ee-286">childNodeInserted</span><span class="sxs-lookup"><span data-stu-id="e00ee-286">childNodeInserted</span></span>
<span data-ttu-id="e00ee-287">Mirrors `DOMNodeInserted` -Ereignis.</span><span class="sxs-lookup"><span data-stu-id="e00ee-287">Mirrors `DOMNodeInserted` event.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="e00ee-288">Parameter</span><span class="sxs-lookup"><span data-stu-id="e00ee-288">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="e00ee-289">parentNodeId</span><span class="sxs-lookup"><span data-stu-id="e00ee-289">parentNodeId</span></span></td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td><span data-ttu-id="e00ee-290">Die ID des Knotens, der sich geändert hat.</span><span class="sxs-lookup"><span data-stu-id="e00ee-290">Id of the node that has changed.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e00ee-291">previousNodeId</span><span class="sxs-lookup"><span data-stu-id="e00ee-291">previousNodeId</span></span></td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td><span data-ttu-id="e00ee-292">Die ID des vorherigen gleichgeordneten Elements des eingefügten Knotens.</span><span class="sxs-lookup"><span data-stu-id="e00ee-292">Id of the inserted node's previous sibling.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e00ee-293">Knoten</span><span class="sxs-lookup"><span data-stu-id="e00ee-293">node</span></span></td>
            <td><a href="#node"><code class="flyout">Node</code></a></td>
            <td><span data-ttu-id="e00ee-294">Eingefügte Knoten Daten.</span><span class="sxs-lookup"><span data-stu-id="e00ee-294">Inserted node data.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="e00ee-295">childNodeRemoved</span><span class="sxs-lookup"><span data-stu-id="e00ee-295">childNodeRemoved</span></span>
<span data-ttu-id="e00ee-296">Mirrors `DOMNodeRemoved` -Ereignis.</span><span class="sxs-lookup"><span data-stu-id="e00ee-296">Mirrors `DOMNodeRemoved` event.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="e00ee-297">Parameter</span><span class="sxs-lookup"><span data-stu-id="e00ee-297">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="e00ee-298">parentNodeId</span><span class="sxs-lookup"><span data-stu-id="e00ee-298">parentNodeId</span></span></td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td><span data-ttu-id="e00ee-299">Die ID des Knotens, der sich geändert hat.</span><span class="sxs-lookup"><span data-stu-id="e00ee-299">Id of the node that has changed.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e00ee-300">NodeId</span><span class="sxs-lookup"><span data-stu-id="e00ee-300">nodeId</span></span></td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td><span data-ttu-id="e00ee-301">Die ID des Knotens, der entfernt wurde.</span><span class="sxs-lookup"><span data-stu-id="e00ee-301">Id of the node that has been removed.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="e00ee-302">documentUpdated</span><span class="sxs-lookup"><span data-stu-id="e00ee-302">documentUpdated</span></span>
<span data-ttu-id="e00ee-303">Wird ausgelöst `Document` , wenn die vollständige Aktualisierung durchgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="e00ee-303">Fired when `Document` has been totally updated.</span></span> <span data-ttu-id="e00ee-304">Knoten-IDs sind nicht mehr gültig.</span><span class="sxs-lookup"><span data-stu-id="e00ee-304">Node ids are no longer valid.</span></span>

</p>

---

## <span data-ttu-id="e00ee-305">Typen</span><span class="sxs-lookup"><span data-stu-id="e00ee-305">Types</span></span>

### <a name="rgba"></a> <span data-ttu-id="e00ee-306">RGBA</span><span class="sxs-lookup"><span data-stu-id="e00ee-306">RGBA</span></span> `object`

<span data-ttu-id="e00ee-307">Eine Struktur mit einer RGBA-Farbe.</span><span class="sxs-lookup"><span data-stu-id="e00ee-307">A Structure holding an RGBA color.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="e00ee-308">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e00ee-308">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="e00ee-309">r</span><span class="sxs-lookup"><span data-stu-id="e00ee-309">r</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="e00ee-310">Die rote Komponente im Bereich [0-255].</span><span class="sxs-lookup"><span data-stu-id="e00ee-310">The red component, in the [0-255] range.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e00ee-311">g</span><span class="sxs-lookup"><span data-stu-id="e00ee-311">g</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="e00ee-312">Die grüne Komponente im Bereich [0-255].</span><span class="sxs-lookup"><span data-stu-id="e00ee-312">The green component, in the [0-255] range.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e00ee-313">b</span><span class="sxs-lookup"><span data-stu-id="e00ee-313">b</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="e00ee-314">Die blaue Komponente im Bereich [0-255].</span><span class="sxs-lookup"><span data-stu-id="e00ee-314">The blue component, in the [0-255] range.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e00ee-315">a</span><span class="sxs-lookup"><span data-stu-id="e00ee-315">a</span></span> <br/> <i><span data-ttu-id="e00ee-316">Optional</span><span class="sxs-lookup"><span data-stu-id="e00ee-316">optional</span></span></i></td>
            <td><code class="flyout">number</code></td>
            <td><span data-ttu-id="e00ee-317">Die Alpha-Komponente im Bereich [0-1].</span><span class="sxs-lookup"><span data-stu-id="e00ee-317">The alpha component, in the [0-1] range.</span></span> <span data-ttu-id="e00ee-318">Der Standardwert ist 1.</span><span class="sxs-lookup"><span data-stu-id="e00ee-318">Default is 1.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="highlightconfig"></a> <span data-ttu-id="e00ee-319">HighlightConfig</span><span class="sxs-lookup"><span data-stu-id="e00ee-319">HighlightConfig</span></span> `object`

<span data-ttu-id="e00ee-320">Konfigurationsdaten zum Markieren von Seitenelementen.</span><span class="sxs-lookup"><span data-stu-id="e00ee-320">Configuration data for highlighting of page elements.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="e00ee-321">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e00ee-321">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="e00ee-322">contentColor</span><span class="sxs-lookup"><span data-stu-id="e00ee-322">contentColor</span></span> <br/> <i><span data-ttu-id="e00ee-323">Optional</span><span class="sxs-lookup"><span data-stu-id="e00ee-323">optional</span></span></i></td>
            <td><a href="#rgba"><code class="flyout">RGBA</code></a></td>
            <td><span data-ttu-id="e00ee-324">Das Feld "Inhalt" hebt die Füllfarbe auf.</span><span class="sxs-lookup"><span data-stu-id="e00ee-324">The content box highlight fill color.</span></span> <span data-ttu-id="e00ee-325">Standard ist transparent.</span><span class="sxs-lookup"><span data-stu-id="e00ee-325">Default is transparent.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e00ee-326">paddingColor</span><span class="sxs-lookup"><span data-stu-id="e00ee-326">paddingColor</span></span> <br/> <i><span data-ttu-id="e00ee-327">Optional</span><span class="sxs-lookup"><span data-stu-id="e00ee-327">optional</span></span></i></td>
            <td><a href="#rgba"><code class="flyout">RGBA</code></a></td>
            <td><span data-ttu-id="e00ee-328">Die Füllfarbe des Füllbereichs wird markiert.</span><span class="sxs-lookup"><span data-stu-id="e00ee-328">The padding highlight fill color.</span></span> <span data-ttu-id="e00ee-329">Standard ist transparent.</span><span class="sxs-lookup"><span data-stu-id="e00ee-329">Default is transparent.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e00ee-330">BorderColor</span><span class="sxs-lookup"><span data-stu-id="e00ee-330">borderColor</span></span> <br/> <i><span data-ttu-id="e00ee-331">Optional</span><span class="sxs-lookup"><span data-stu-id="e00ee-331">optional</span></span></i></td>
            <td><a href="#rgba"><code class="flyout">RGBA</code></a></td>
            <td><span data-ttu-id="e00ee-332">Die Rahmen Hervorhebungsfarbe.</span><span class="sxs-lookup"><span data-stu-id="e00ee-332">The border highlight fill color.</span></span> <span data-ttu-id="e00ee-333">Standard ist transparent.</span><span class="sxs-lookup"><span data-stu-id="e00ee-333">Default is transparent.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e00ee-334">marginColor</span><span class="sxs-lookup"><span data-stu-id="e00ee-334">marginColor</span></span> <br/> <i><span data-ttu-id="e00ee-335">Optional</span><span class="sxs-lookup"><span data-stu-id="e00ee-335">optional</span></span></i></td>
            <td><a href="#rgba"><code class="flyout">RGBA</code></a></td>
            <td><span data-ttu-id="e00ee-336">Die Füllfarbe des Rands.</span><span class="sxs-lookup"><span data-stu-id="e00ee-336">The margin highlight fill color.</span></span> <span data-ttu-id="e00ee-337">Standard ist transparent.</span><span class="sxs-lookup"><span data-stu-id="e00ee-337">Default is transparent.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="nodeid"></a> <span data-ttu-id="e00ee-338">NodeId</span><span class="sxs-lookup"><span data-stu-id="e00ee-338">NodeId</span></span> `integer`

<span data-ttu-id="e00ee-339">Eindeutige DOM-Knoten-ID</span><span class="sxs-lookup"><span data-stu-id="e00ee-339">Unique DOM node identifier</span></span>

</p>

---

### <a name="node"></a> <span data-ttu-id="e00ee-340">Knoten</span><span class="sxs-lookup"><span data-stu-id="e00ee-340">Node</span></span> `object`

<span data-ttu-id="e00ee-341">Mirror-Objekt, das die eigentlichen DOM-Knoten darstellt.</span><span class="sxs-lookup"><span data-stu-id="e00ee-341">Mirror object that represents the actual DOM nodes.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="e00ee-342">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e00ee-342">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="e00ee-343">NodeId</span><span class="sxs-lookup"><span data-stu-id="e00ee-343">nodeId</span></span></td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td><span data-ttu-id="e00ee-344">Knoten Bezeichner, der für den Verweis auf diesen Knoten verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="e00ee-344">Node Identifier used to reference this node.</span></span> <span data-ttu-id="e00ee-345">Das Back-End löst DOM-Ereignisse für Knoten aus, die über eine Knoten-Nr verfügen, die dem Client bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="e00ee-345">Backend will fire DOM events for nodes that have a nodeId that is known to the client</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e00ee-346">parentID</span><span class="sxs-lookup"><span data-stu-id="e00ee-346">parentId</span></span> <br/> <i><span data-ttu-id="e00ee-347">Optional</span><span class="sxs-lookup"><span data-stu-id="e00ee-347">optional</span></span></i></td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td><span data-ttu-id="e00ee-348">Knoten Bezeichner des übergeordneten Knotens (sofern vorhanden).</span><span class="sxs-lookup"><span data-stu-id="e00ee-348">Node Identifier of the parent Node, if any.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e00ee-349">backendNodeId</span><span class="sxs-lookup"><span data-stu-id="e00ee-349">backendNodeId</span></span></td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td><span data-ttu-id="e00ee-350">Back-End-Knoten Bezeichner des Knotens.</span><span class="sxs-lookup"><span data-stu-id="e00ee-350">Backend Node identifier of the node.</span></span> <span data-ttu-id="e00ee-351">BackendNodeIds-Verweisknoten, die dem Client bekannt sein können, jedoch keine DOM-Ereignisse über diesen Knoten pushen.</span><span class="sxs-lookup"><span data-stu-id="e00ee-351">BackendNodeIds reference Nodes that can be known to the client, but do not push DOM events about this node.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e00ee-352">NodeType</span><span class="sxs-lookup"><span data-stu-id="e00ee-352">nodeType</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td>`Node`<span data-ttu-id="e00ee-353">-NodeType.</span><span class="sxs-lookup"><span data-stu-id="e00ee-353">'s nodeType.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e00ee-354">nodeName</span><span class="sxs-lookup"><span data-stu-id="e00ee-354">nodeName</span></span></td>
            <td><code class="flyout">string</code></td>
            <td>`Node`<span data-ttu-id="e00ee-355">Knoten-Nr.</span><span class="sxs-lookup"><span data-stu-id="e00ee-355">'s nodeName.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e00ee-356">localName</span><span class="sxs-lookup"><span data-stu-id="e00ee-356">localName</span></span></td>
            <td><code class="flyout">string</code></td>
            <td>`Node`<span data-ttu-id="e00ee-357">es LocalName</span><span class="sxs-lookup"><span data-stu-id="e00ee-357">'s localName</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e00ee-358">nodeValue</span><span class="sxs-lookup"><span data-stu-id="e00ee-358">nodeValue</span></span></td>
            <td><code class="flyout">string</code></td>
            <td>`Node`<span data-ttu-id="e00ee-359">es nodeValue</span><span class="sxs-lookup"><span data-stu-id="e00ee-359">'s nodeValue</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e00ee-360">childNodeCount</span><span class="sxs-lookup"><span data-stu-id="e00ee-360">childNodeCount</span></span> <br/> <i><span data-ttu-id="e00ee-361">Optional</span><span class="sxs-lookup"><span data-stu-id="e00ee-361">optional</span></span></i></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="e00ee-362">Untergeordnete Anzahl für `Container` Knoten.</span><span class="sxs-lookup"><span data-stu-id="e00ee-362">Child count for `Container` nodes.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e00ee-363">Kinder</span><span class="sxs-lookup"><span data-stu-id="e00ee-363">children</span></span> <br/> <i><span data-ttu-id="e00ee-364">Optional</span><span class="sxs-lookup"><span data-stu-id="e00ee-364">optional</span></span></i></td>
            <td><a href="#node"><code class="flyout">Node[]</code></a></td>
            <td><span data-ttu-id="e00ee-365">Untergeordnete Knoten dieses Knotens, wenn Sie mit untergeordneten Elementen angefordert werden.</span><span class="sxs-lookup"><span data-stu-id="e00ee-365">Child nodes of this node when requested with children.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e00ee-366">Attribute</span><span class="sxs-lookup"><span data-stu-id="e00ee-366">attributes</span></span> <br/> <i><span data-ttu-id="e00ee-367">Optional</span><span class="sxs-lookup"><span data-stu-id="e00ee-367">optional</span></span></i></td>
            <td><code class="flyout">string[]</code></td>
            <td><span data-ttu-id="e00ee-368">Attribute von `Element` Knoten in Form einer flachen Matrix ' [name1, value1, name2, Value2]</span><span class="sxs-lookup"><span data-stu-id="e00ee-368">Attributes of `Element` nodes in the form of a flat array \`[name1, value1, name2, value2]</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e00ee-369">documentURL</span><span class="sxs-lookup"><span data-stu-id="e00ee-369">documentURL</span></span> <br/> <i><span data-ttu-id="e00ee-370">Optional</span><span class="sxs-lookup"><span data-stu-id="e00ee-370">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="e00ee-371">Dokument-URL, auf die die `Document` Knoten verweisen.</span><span class="sxs-lookup"><span data-stu-id="e00ee-371">Document URL that `Document` nodes point to.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e00ee-372">baseURL</span><span class="sxs-lookup"><span data-stu-id="e00ee-372">baseURL</span></span> <br/> <i><span data-ttu-id="e00ee-373">Optional</span><span class="sxs-lookup"><span data-stu-id="e00ee-373">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="e00ee-374">Dokument-URL, die `Document` Knoten für die URL-Vervollständigung verwenden</span><span class="sxs-lookup"><span data-stu-id="e00ee-374">Document URL that `Document` nodes use for URL completion.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e00ee-375">PublicId</span><span class="sxs-lookup"><span data-stu-id="e00ee-375">publicId</span></span> <br/> <i><span data-ttu-id="e00ee-376">Optional</span><span class="sxs-lookup"><span data-stu-id="e00ee-376">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td>`DocumentType` <span data-ttu-id="e00ee-377">Public-Nr des Knotens.</span><span class="sxs-lookup"><span data-stu-id="e00ee-377">Node's publicId.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e00ee-378">SystemId</span><span class="sxs-lookup"><span data-stu-id="e00ee-378">systemId</span></span> <br/> <i><span data-ttu-id="e00ee-379">Optional</span><span class="sxs-lookup"><span data-stu-id="e00ee-379">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td>`DocumentType` <span data-ttu-id="e00ee-380">Die System-Nr des Knotens.</span><span class="sxs-lookup"><span data-stu-id="e00ee-380">Node's systemId.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e00ee-381">InternalSubset</span><span class="sxs-lookup"><span data-stu-id="e00ee-381">internalSubset</span></span> <br/> <i><span data-ttu-id="e00ee-382">Optional</span><span class="sxs-lookup"><span data-stu-id="e00ee-382">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td>`DocumentType` <span data-ttu-id="e00ee-383">InternalSubset des Knotens.</span><span class="sxs-lookup"><span data-stu-id="e00ee-383">Node's internalSubset.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e00ee-384">xmlversion</span><span class="sxs-lookup"><span data-stu-id="e00ee-384">xmlVersion</span></span> <br/> <i><span data-ttu-id="e00ee-385">Optional</span><span class="sxs-lookup"><span data-stu-id="e00ee-385">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td>`Document` <span data-ttu-id="e00ee-386">XML-Version des Knotens im Fall von XML-Dokumenten</span><span class="sxs-lookup"><span data-stu-id="e00ee-386">Node's xml version in the case of XML documents.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e00ee-387">name</span><span class="sxs-lookup"><span data-stu-id="e00ee-387">name</span></span> <br/> <i><span data-ttu-id="e00ee-388">Optional</span><span class="sxs-lookup"><span data-stu-id="e00ee-388">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td>`Attr` <span data-ttu-id="e00ee-389">Der Name des Knotens.</span><span class="sxs-lookup"><span data-stu-id="e00ee-389">Node's name.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e00ee-390">value</span><span class="sxs-lookup"><span data-stu-id="e00ee-390">value</span></span> <br/> <i><span data-ttu-id="e00ee-391">Optional</span><span class="sxs-lookup"><span data-stu-id="e00ee-391">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td>`Attr` <span data-ttu-id="e00ee-392">Der Wert des Knotens.</span><span class="sxs-lookup"><span data-stu-id="e00ee-392">Node's value.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e00ee-393">Frame-Nr</span><span class="sxs-lookup"><span data-stu-id="e00ee-393">frameId</span></span> <br/> <i><span data-ttu-id="e00ee-394">Optional</span><span class="sxs-lookup"><span data-stu-id="e00ee-394">optional</span></span></i></td>
            <td><a href="page.md#frameid"><code class="flyout">Page.FrameId</code></a></td>
            <td><span data-ttu-id="e00ee-395">Frame-ID für die Elemente des Frame-Besitzers.</span><span class="sxs-lookup"><span data-stu-id="e00ee-395">Frame ID for frame owner elements.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e00ee-396">contentDocument</span><span class="sxs-lookup"><span data-stu-id="e00ee-396">contentDocument</span></span> <br/> <i><span data-ttu-id="e00ee-397">Optional</span><span class="sxs-lookup"><span data-stu-id="e00ee-397">optional</span></span></i></td>
            <td><a href="#node"><code class="flyout">Node</code></a></td>
            <td><span data-ttu-id="e00ee-398">Inhaltsdokument für Elemente des Frame-Besitzers.</span><span class="sxs-lookup"><span data-stu-id="e00ee-398">Content document for frame owner elements.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e00ee-399">isSVG</span><span class="sxs-lookup"><span data-stu-id="e00ee-399">isSVG</span></span> <br/> <i><span data-ttu-id="e00ee-400">Optional</span><span class="sxs-lookup"><span data-stu-id="e00ee-400">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="e00ee-401">"True", wenn der Knoten SVG ist.</span><span class="sxs-lookup"><span data-stu-id="e00ee-401">True if the node is SVG.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="backendnodeid"></a> <span data-ttu-id="e00ee-402">BackendNodeId</span><span class="sxs-lookup"><span data-stu-id="e00ee-402">BackendNodeId</span></span> `integer`

<span data-ttu-id="e00ee-403">Eindeutiger DOM-Knoten Bezeichner, der zum Verweisen auf einen Knoten verwendet wird, der möglicherweise nicht in das Front-End verschoben wurde.</span><span class="sxs-lookup"><span data-stu-id="e00ee-403">Unique DOM node identifier used to reference a node that may not have been pushed to the front-end.</span></span>

</p>

---

### <a name="pseudotype"></a> <span data-ttu-id="e00ee-404">Pseudotyp</span><span class="sxs-lookup"><span data-stu-id="e00ee-404">PseudoType</span></span> `string`

<span data-ttu-id="e00ee-405">Pseudo Elementtyp.</span><span class="sxs-lookup"><span data-stu-id="e00ee-405">Pseudo element type.</span></span>

##### <span data-ttu-id="e00ee-406">Zulässige Werte</span><span class="sxs-lookup"><span data-stu-id="e00ee-406">Allowed Values</span></span>
<span data-ttu-id="e00ee-407">erste Zeile, erster Buchstabe, vorher, nachher, Auswahl</span><span class="sxs-lookup"><span data-stu-id="e00ee-407">first-line, first-letter, before, after, selection</span></span>
</p>

---

## <span data-ttu-id="e00ee-408">Abhängigkeiten</span><span class="sxs-lookup"><span data-stu-id="e00ee-408">Dependencies</span></span>

[<span data-ttu-id="e00ee-409">Laufzeit</span><span class="sxs-lookup"><span data-stu-id="e00ee-409">Runtime</span></span>](runtime.md)
