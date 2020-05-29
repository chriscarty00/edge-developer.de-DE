---
description: Referenz für die Overlay-Domäne. Overlay-Domäne macht visuelle Elemente und Interaktion zwischen Knotenauswahl verfügbar
title: Overlay-Domäne – devtools-Protokoll Version 0,2
author: pelavall
ms.author: pelavall
ms.date: 8/17/2018
ms.topic: reference
ms.prod: microsoft-edge
ms.openlocfilehash: a7657e2abc99e45894f19f6557f12f78f8ee9c75
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10567532"
---
# <span data-ttu-id="1e967-104">Überlagerung</span><span class="sxs-lookup"><span data-stu-id="1e967-104">Overlay</span></span>
<span data-ttu-id="1e967-105">Overlay-Domäne macht visuelle Elemente und Interaktion zwischen Knotenauswahl verfügbar</span><span class="sxs-lookup"><span data-stu-id="1e967-105">Overlay domain exposes visual adornments and node selection interaction</span></span>

| | |
|-|-|
| [**<span data-ttu-id="1e967-106">Methoden</span><span class="sxs-lookup"><span data-stu-id="1e967-106">Methods</span></span>**](#methods) | <span data-ttu-id="1e967-107">[aktivieren](#enable), [Deaktivieren](#disable), [setInspectMode](#setinspectmode)</span><span class="sxs-lookup"><span data-stu-id="1e967-107">[enable](#enable), [disable](#disable), [setInspectMode](#setinspectmode)</span></span> |
| [**<span data-ttu-id="1e967-108">Ereignisse</span><span class="sxs-lookup"><span data-stu-id="1e967-108">Events</span></span>**](#events) | <span data-ttu-id="1e967-109">[inspectNodeRequested](#inspectnoderequested), [nodeHighlightRequested](#nodehighlightrequested)</span><span class="sxs-lookup"><span data-stu-id="1e967-109">[inspectNodeRequested](#inspectnoderequested), [nodeHighlightRequested](#nodehighlightrequested)</span></span> |
| [**<span data-ttu-id="1e967-110">Abhängigkeiten</span><span class="sxs-lookup"><span data-stu-id="1e967-110">Dependencies</span></span>**](#dependencies) | [<span data-ttu-id="1e967-111">DOM</span><span class="sxs-lookup"><span data-stu-id="1e967-111">DOM</span></span>](dom.md) |
## <span data-ttu-id="1e967-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="1e967-112">Methods</span></span>

### <span data-ttu-id="1e967-113">Aktivieren</span><span class="sxs-lookup"><span data-stu-id="1e967-113">enable</span></span>
<span data-ttu-id="1e967-114">Ermöglicht das Melden von <code>nodeHighlightRequested</code> und <code>inspectElementRequested</code> Ereignissen</span><span class="sxs-lookup"><span data-stu-id="1e967-114">Enables reporting of <code>nodeHighlightRequested</code> and <code>inspectElementRequested</code> events</span></span>

</p>

---

### <span data-ttu-id="1e967-115">Deaktivieren </span><span class="sxs-lookup"><span data-stu-id="1e967-115">disable</span></span>
<span data-ttu-id="1e967-116">Deaktiviert die Berichterstattung über Overlay-Domänenereignisse</span><span class="sxs-lookup"><span data-stu-id="1e967-116">Disables reporting of Overlay domain events</span></span>

</p>

---

### <span data-ttu-id="1e967-117">setInspectMode</span><span class="sxs-lookup"><span data-stu-id="1e967-117">setInspectMode</span></span>
<span data-ttu-id="1e967-118">Legt den Elementauswahl Modus für den Client fest.</span><span class="sxs-lookup"><span data-stu-id="1e967-118">Sets the element selection mode for the client</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="1e967-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="1e967-119">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="1e967-120">mode</span><span class="sxs-lookup"><span data-stu-id="1e967-120">mode</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="1e967-121">Der Prüfungsmodus.</span><span class="sxs-lookup"><span data-stu-id="1e967-121">The inspection mode.</span></span>  <span data-ttu-id="1e967-122">Gültige Werte sind "searchForNode" und "None".</span><span class="sxs-lookup"><span data-stu-id="1e967-122">Valid values are 'searchForNode' and 'none'.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="1e967-123">highlightConfig</span><span class="sxs-lookup"><span data-stu-id="1e967-123">highlightConfig</span></span> <br/> <i><span data-ttu-id="1e967-124">Optional</span><span class="sxs-lookup"><span data-stu-id="1e967-124">optional</span></span></i></td>
            <td><a href="dom.md#highlightconfig"><code class="flyout">DOM.HighlightConfig</code></a></td>
            <td><span data-ttu-id="1e967-125">Die zu verwendende Hervorhebungs Konfiguration während der Überprüfung</span><span class="sxs-lookup"><span data-stu-id="1e967-125">The highlight configuration to use while inspecting</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

## <span data-ttu-id="1e967-126">Ereignisse</span><span class="sxs-lookup"><span data-stu-id="1e967-126">Events</span></span>

### <span data-ttu-id="1e967-127">inspectNodeRequested</span><span class="sxs-lookup"><span data-stu-id="1e967-127">inspectNodeRequested</span></span>
<span data-ttu-id="1e967-128">Benachrichtigt den Client, dass der Benutzer gebeten hat, einen bestimmten Knoten zu überprüfen</span><span class="sxs-lookup"><span data-stu-id="1e967-128">Notifies the client that the user has asked to inspect a particular node</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="1e967-129">Parameter</span><span class="sxs-lookup"><span data-stu-id="1e967-129">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="1e967-130">backendNodeId</span><span class="sxs-lookup"><span data-stu-id="1e967-130">backendNodeId</span></span></td>
            <td><a href="dom.md#backendnodeid"><code class="flyout">DOM.BackendNodeId</code></a></td>
            <td><span data-ttu-id="1e967-131">Die Back-End-Knoten-ID des angeforderten Knotens</span><span class="sxs-lookup"><span data-stu-id="1e967-131">The backend node ID of node requested</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="1e967-132">nodeHighlightRequested</span><span class="sxs-lookup"><span data-stu-id="1e967-132">nodeHighlightRequested</span></span>
<span data-ttu-id="1e967-133">Gibt an, dass der Benutzer über den Knoten schwebt und den Knoten möglicherweise überprüft.</span><span class="sxs-lookup"><span data-stu-id="1e967-133">Indicates that the user has hovered over the node and may inspect the node</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="1e967-134">Parameter</span><span class="sxs-lookup"><span data-stu-id="1e967-134">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="1e967-135">NodeId</span><span class="sxs-lookup"><span data-stu-id="1e967-135">nodeId</span></span></td>
            <td><a href="dom.md#nodeid"><code class="flyout">DOM.NodeId</code></a></td>
            <td><span data-ttu-id="1e967-136">Die Knoten-ID des betrachteten Knotens</span><span class="sxs-lookup"><span data-stu-id="1e967-136">The node ID of the node being considered</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

## <span data-ttu-id="1e967-137">Abhängigkeiten</span><span class="sxs-lookup"><span data-stu-id="1e967-137">Dependencies</span></span>

[<span data-ttu-id="1e967-138">DOM</span><span class="sxs-lookup"><span data-stu-id="1e967-138">DOM</span></span>](dom.md)