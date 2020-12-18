---
description: Referenz für die Overlay-Domäne. Overlay-Domäne macht visuelle Elemente und Interaktion zwischen Knotenauswahl verfügbar
title: Overlay-Domäne – devtools-Protokoll Version 0,2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: reference
ms.prod: microsoft-edge
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: dcf5feff9983aa2e9e61ac0569938988812165f8
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233634"
---
# <span data-ttu-id="bc6af-104">Überlagerung</span><span class="sxs-lookup"><span data-stu-id="bc6af-104">Overlay</span></span>

<span data-ttu-id="bc6af-105">Overlay-Domäne macht visuelle Elemente und Interaktion zwischen Knotenauswahl verfügbar</span><span class="sxs-lookup"><span data-stu-id="bc6af-105">Overlay domain exposes visual adornments and node selection interaction</span></span>

| | |
|-|-|
| [**<span data-ttu-id="bc6af-106">Methoden</span><span class="sxs-lookup"><span data-stu-id="bc6af-106">Methods</span></span>**](#methods) | <span data-ttu-id="bc6af-107">[aktivieren](#enable), [Deaktivieren](#disable), [setInspectMode](#setinspectmode)</span><span class="sxs-lookup"><span data-stu-id="bc6af-107">[enable](#enable), [disable](#disable), [setInspectMode](#setinspectmode)</span></span> |
| [**<span data-ttu-id="bc6af-108">Veranstaltungen</span><span class="sxs-lookup"><span data-stu-id="bc6af-108">Events</span></span>**](#events) | <span data-ttu-id="bc6af-109">[inspectNodeRequested](#inspectnoderequested), [nodeHighlightRequested](#nodehighlightrequested)</span><span class="sxs-lookup"><span data-stu-id="bc6af-109">[inspectNodeRequested](#inspectnoderequested), [nodeHighlightRequested](#nodehighlightrequested)</span></span> |
| [**<span data-ttu-id="bc6af-110">Abhängigkeiten</span><span class="sxs-lookup"><span data-stu-id="bc6af-110">Dependencies</span></span>**](#dependencies) | [<span data-ttu-id="bc6af-111">DOM</span><span class="sxs-lookup"><span data-stu-id="bc6af-111">DOM</span></span>](dom.md) |
## <span data-ttu-id="bc6af-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="bc6af-112">Methods</span></span>

### <span data-ttu-id="bc6af-113">Aktivieren</span><span class="sxs-lookup"><span data-stu-id="bc6af-113">enable</span></span>
<span data-ttu-id="bc6af-114">Ermöglicht das Melden von <code>nodeHighlightRequested</code> und <code>inspectElementRequested</code> Ereignissen</span><span class="sxs-lookup"><span data-stu-id="bc6af-114">Enables reporting of <code>nodeHighlightRequested</code> and <code>inspectElementRequested</code> events</span></span>

</p>

---

### <span data-ttu-id="bc6af-115">Deaktivieren </span><span class="sxs-lookup"><span data-stu-id="bc6af-115">disable</span></span>
<span data-ttu-id="bc6af-116">Deaktiviert die Berichterstattung über Overlay-Domänenereignisse</span><span class="sxs-lookup"><span data-stu-id="bc6af-116">Disables reporting of Overlay domain events</span></span>

</p>

---

### <span data-ttu-id="bc6af-117">setInspectMode</span><span class="sxs-lookup"><span data-stu-id="bc6af-117">setInspectMode</span></span>
<span data-ttu-id="bc6af-118">Legt den Elementauswahl Modus für den Client fest.</span><span class="sxs-lookup"><span data-stu-id="bc6af-118">Sets the element selection mode for the client</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="bc6af-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="bc6af-119">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="bc6af-120">mode</span><span class="sxs-lookup"><span data-stu-id="bc6af-120">mode</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="bc6af-121">Der Prüfungsmodus.</span><span class="sxs-lookup"><span data-stu-id="bc6af-121">The inspection mode.</span></span>  <span data-ttu-id="bc6af-122">Gültige Werte sind "searchForNode" und "None".</span><span class="sxs-lookup"><span data-stu-id="bc6af-122">Valid values are 'searchForNode' and 'none'.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="bc6af-123">highlightConfig</span><span class="sxs-lookup"><span data-stu-id="bc6af-123">highlightConfig</span></span> <br/> <i><span data-ttu-id="bc6af-124">Optional</span><span class="sxs-lookup"><span data-stu-id="bc6af-124">optional</span></span></i></td>
            <td><a href="dom.md#highlightconfig"><code class="flyout">DOM.HighlightConfig</code></a></td>
            <td><span data-ttu-id="bc6af-125">Die zu verwendende Hervorhebungs Konfiguration während der Überprüfung</span><span class="sxs-lookup"><span data-stu-id="bc6af-125">The highlight configuration to use while inspecting</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

## <span data-ttu-id="bc6af-126">Veranstaltungen</span><span class="sxs-lookup"><span data-stu-id="bc6af-126">Events</span></span>

### <span data-ttu-id="bc6af-127">inspectNodeRequested</span><span class="sxs-lookup"><span data-stu-id="bc6af-127">inspectNodeRequested</span></span>
<span data-ttu-id="bc6af-128">Benachrichtigt den Client, dass der Benutzer gebeten hat, einen bestimmten Knoten zu überprüfen</span><span class="sxs-lookup"><span data-stu-id="bc6af-128">Notifies the client that the user has asked to inspect a particular node</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="bc6af-129">Parameter</span><span class="sxs-lookup"><span data-stu-id="bc6af-129">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="bc6af-130">backendNodeId</span><span class="sxs-lookup"><span data-stu-id="bc6af-130">backendNodeId</span></span></td>
            <td><a href="dom.md#backendnodeid"><code class="flyout">DOM.BackendNodeId</code></a></td>
            <td><span data-ttu-id="bc6af-131">Die Back-End-Knoten-ID des angeforderten Knotens</span><span class="sxs-lookup"><span data-stu-id="bc6af-131">The backend node ID of node requested</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="bc6af-132">nodeHighlightRequested</span><span class="sxs-lookup"><span data-stu-id="bc6af-132">nodeHighlightRequested</span></span>
<span data-ttu-id="bc6af-133">Gibt an, dass der Benutzer über den Knoten schwebt und den Knoten möglicherweise überprüft.</span><span class="sxs-lookup"><span data-stu-id="bc6af-133">Indicates that the user has hovered over the node and may inspect the node</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="bc6af-134">Parameter</span><span class="sxs-lookup"><span data-stu-id="bc6af-134">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="bc6af-135">NodeId</span><span class="sxs-lookup"><span data-stu-id="bc6af-135">nodeId</span></span></td>
            <td><a href="dom.md#nodeid"><code class="flyout">DOM.NodeId</code></a></td>
            <td><span data-ttu-id="bc6af-136">Die Knoten-ID des betrachteten Knotens</span><span class="sxs-lookup"><span data-stu-id="bc6af-136">The node ID of the node being considered</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

## <span data-ttu-id="bc6af-137">Abhängigkeiten</span><span class="sxs-lookup"><span data-stu-id="bc6af-137">Dependencies</span></span>

[<span data-ttu-id="bc6af-138">DOM</span><span class="sxs-lookup"><span data-stu-id="bc6af-138">DOM</span></span>](dom.md)
