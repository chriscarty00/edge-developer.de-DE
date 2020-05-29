---
description: Referenz für die DOMDebugger-Domäne. Dom-Debuggen ermöglicht das Festlegen von Haltepunkten für bestimmte Dom-Vorgänge und-Ereignisse. Die JavaScript-Ausführung wird bei diesen Vorgängen so beendet, als ob ein regulärer Haltepunkt festgesetzt wurde.
title: DOMDebugger Domain-devtools Protocol Version 0,2
author: pelavall
ms.author: pelavall
ms.date: 8/17/2018
ms.topic: reference
ms.prod: microsoft-edge
ms.openlocfilehash: 437a88ff93bda36d85a8f5632c1a02aa205d049b
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10567533"
---
# <span data-ttu-id="ddd7d-105">DOMDebugger</span><span class="sxs-lookup"><span data-stu-id="ddd7d-105">DOMDebugger</span></span>
<span data-ttu-id="ddd7d-106">Dom-Debuggen ermöglicht das Festlegen von Haltepunkten für bestimmte Dom-Vorgänge und-Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="ddd7d-106">DOM debugging allows setting breakpoints on particular DOM operations and events.</span></span> <span data-ttu-id="ddd7d-107">Die JavaScript-Ausführung wird bei diesen Vorgängen so beendet, als ob ein regulärer Haltepunkt festgesetzt wurde.</span><span class="sxs-lookup"><span data-stu-id="ddd7d-107">JavaScript execution will stop on these operations as if there was a regular breakpoint set.</span></span>

| | |
|-|-|
| [**<span data-ttu-id="ddd7d-108">Methoden</span><span class="sxs-lookup"><span data-stu-id="ddd7d-108">Methods</span></span>**](#methods) | <span data-ttu-id="ddd7d-109">[setInstrumentationBreakpoint](#setinstrumentationbreakpoint), [removeInstrumentationBreakpoint](#removeinstrumentationbreakpoint)</span><span class="sxs-lookup"><span data-stu-id="ddd7d-109">[setInstrumentationBreakpoint](#setinstrumentationbreakpoint), [removeInstrumentationBreakpoint](#removeinstrumentationbreakpoint)</span></span> |
## <span data-ttu-id="ddd7d-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="ddd7d-110">Methods</span></span>

### <span data-ttu-id="ddd7d-111">setInstrumentationBreakpoint</span><span class="sxs-lookup"><span data-stu-id="ddd7d-111">setInstrumentationBreakpoint</span></span>
<span><b><span data-ttu-id="ddd7d-112">Experimenteller.</span><span class="sxs-lookup"><span data-stu-id="ddd7d-112">Experimental.</span></span> </b></span><span data-ttu-id="ddd7d-113">Legt einen Haltepunkt für ein bestimmtes systemeigenes Ereignis fest.</span><span class="sxs-lookup"><span data-stu-id="ddd7d-113">Sets a breakpoint on a particular native event.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="ddd7d-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="ddd7d-114">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="ddd7d-115">EventName</span><span class="sxs-lookup"><span data-stu-id="ddd7d-115">eventName</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="ddd7d-116">Der Name der Instrumentation, auf der angehalten werden soll.</span><span class="sxs-lookup"><span data-stu-id="ddd7d-116">Instrumentation name to stop on.</span></span> <span data-ttu-id="ddd7d-117">Gültige Werte: "scriptFirstStatement".</span><span class="sxs-lookup"><span data-stu-id="ddd7d-117">Valid values: 'scriptFirstStatement'.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="ddd7d-118">removeInstrumentationBreakpoint</span><span class="sxs-lookup"><span data-stu-id="ddd7d-118">removeInstrumentationBreakpoint</span></span>
<span><b><span data-ttu-id="ddd7d-119">Experimenteller.</span><span class="sxs-lookup"><span data-stu-id="ddd7d-119">Experimental.</span></span> </b></span><span data-ttu-id="ddd7d-120">Entfernt einen Haltepunkt für ein bestimmtes systemeigenes Ereignis.</span><span class="sxs-lookup"><span data-stu-id="ddd7d-120">Removes a breakpoint on a particular native event.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="ddd7d-121">Parameter</span><span class="sxs-lookup"><span data-stu-id="ddd7d-121">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="ddd7d-122">EventName</span><span class="sxs-lookup"><span data-stu-id="ddd7d-122">eventName</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="ddd7d-123">Der Name der Instrumentation, auf der angehalten werden soll.</span><span class="sxs-lookup"><span data-stu-id="ddd7d-123">Instrumentation name to stop on.</span></span> <span data-ttu-id="ddd7d-124">Gültige Werte: "scriptFirstStatement".</span><span class="sxs-lookup"><span data-stu-id="ddd7d-124">Valid values: 'scriptFirstStatement'.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---
