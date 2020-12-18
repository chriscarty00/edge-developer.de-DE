---
description: Referenz für die DOMDebugger-Domäne. Dom-Debuggen ermöglicht das Festlegen von Haltepunkten für bestimmte Dom-Vorgänge und-Ereignisse. Die JavaScript-Ausführung wird bei diesen Vorgängen so beendet, als ob ein regulärer Haltepunkt festgesetzt wurde.
title: DOMDebugger Domain-devtools Protocol Version 0,2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: reference
ms.prod: microsoft-edge
ms.date: 12/02/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: d97a9a8f2d0e49166f5f081e8bb0c0d5d3cdd93f
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233636"
---
# <span data-ttu-id="e30c1-105">DOMDebugger</span><span class="sxs-lookup"><span data-stu-id="e30c1-105">DOMDebugger</span></span>

<span data-ttu-id="e30c1-106">Dom-Debuggen ermöglicht das Festlegen von Haltepunkten für bestimmte Dom-Vorgänge und-Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="e30c1-106">DOM debugging allows setting breakpoints on particular DOM operations and events.</span></span> <span data-ttu-id="e30c1-107">Die JavaScript-Ausführung wird bei diesen Vorgängen so beendet, als ob ein regulärer Haltepunkt festgesetzt wurde.</span><span class="sxs-lookup"><span data-stu-id="e30c1-107">JavaScript execution will stop on these operations as if there was a regular breakpoint set.</span></span>

| | |
|-|-|
| [**<span data-ttu-id="e30c1-108">Methoden</span><span class="sxs-lookup"><span data-stu-id="e30c1-108">Methods</span></span>**](#methods) | <span data-ttu-id="e30c1-109">[setInstrumentationBreakpoint](#setinstrumentationbreakpoint), [removeInstrumentationBreakpoint](#removeinstrumentationbreakpoint)</span><span class="sxs-lookup"><span data-stu-id="e30c1-109">[setInstrumentationBreakpoint](#setinstrumentationbreakpoint), [removeInstrumentationBreakpoint](#removeinstrumentationbreakpoint)</span></span> |
## <span data-ttu-id="e30c1-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="e30c1-110">Methods</span></span>

### <span data-ttu-id="e30c1-111">setInstrumentationBreakpoint</span><span class="sxs-lookup"><span data-stu-id="e30c1-111">setInstrumentationBreakpoint</span></span>
<span><b><span data-ttu-id="e30c1-112">Experimenteller.</span><span class="sxs-lookup"><span data-stu-id="e30c1-112">Experimental.</span></span> </b></span><span data-ttu-id="e30c1-113">Legt einen Haltepunkt für ein bestimmtes systemeigenes Ereignis fest.</span><span class="sxs-lookup"><span data-stu-id="e30c1-113">Sets a breakpoint on a particular native event.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="e30c1-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="e30c1-114">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="e30c1-115">EventName</span><span class="sxs-lookup"><span data-stu-id="e30c1-115">eventName</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="e30c1-116">Der Name der Instrumentation, auf der angehalten werden soll.</span><span class="sxs-lookup"><span data-stu-id="e30c1-116">Instrumentation name to stop on.</span></span> <span data-ttu-id="e30c1-117">Gültige Werte: "scriptFirstStatement".</span><span class="sxs-lookup"><span data-stu-id="e30c1-117">Valid values: 'scriptFirstStatement'.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="e30c1-118">removeInstrumentationBreakpoint</span><span class="sxs-lookup"><span data-stu-id="e30c1-118">removeInstrumentationBreakpoint</span></span>
<span><b><span data-ttu-id="e30c1-119">Experimenteller.</span><span class="sxs-lookup"><span data-stu-id="e30c1-119">Experimental.</span></span> </b></span><span data-ttu-id="e30c1-120">Entfernt einen Haltepunkt für ein bestimmtes systemeigenes Ereignis.</span><span class="sxs-lookup"><span data-stu-id="e30c1-120">Removes a breakpoint on a particular native event.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="e30c1-121">Parameter</span><span class="sxs-lookup"><span data-stu-id="e30c1-121">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="e30c1-122">EventName</span><span class="sxs-lookup"><span data-stu-id="e30c1-122">eventName</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="e30c1-123">Der Name der Instrumentation, auf der angehalten werden soll.</span><span class="sxs-lookup"><span data-stu-id="e30c1-123">Instrumentation name to stop on.</span></span> <span data-ttu-id="e30c1-124">Gültige Werte: "scriptFirstStatement".</span><span class="sxs-lookup"><span data-stu-id="e30c1-124">Valid values: 'scriptFirstStatement'.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---
