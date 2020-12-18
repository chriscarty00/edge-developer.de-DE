---
description: DevTools Protocol Version 0,1 (EdgeHTML) Reference für die Debugger-Domäne. Die Debugger-Domäne macht JavaScript-Debugfunktionen verfügbar. Sie ermöglicht das Festlegen und Entfernen von Haltepunkten, durchlaufen der Ausführung, Durchsuchen von Stapelablaufverfolgungen usw.
title: Debugger-Domäne – devtools-Protokoll Version 0,1 (EdgeHTML)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: reference
ms.prod: microsoft-edge
ms.custom: seodec18
ms.date: 12/16/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 5160e6e69ec76f8c584f1bdb969464d805c7afa7
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11234026"
---
# <span data-ttu-id="4d8ce-105">Debugger-Domäne – devtools-Protokoll Version 0,1 (EdgeHTML)</span><span class="sxs-lookup"><span data-stu-id="4d8ce-105">Debugger Domain - DevTools Protocol Version 0.1 (EdgeHTML)</span></span>  
  
<span data-ttu-id="4d8ce-106">Die Debugger-Domäne macht JavaScript-Debugfunktionen verfügbar.</span><span class="sxs-lookup"><span data-stu-id="4d8ce-106">Debugger domain exposes JavaScript debugging capabilities.</span></span> <span data-ttu-id="4d8ce-107">Sie ermöglicht das Festlegen und Entfernen von Haltepunkten, durchlaufen der Ausführung, Durchsuchen von Stapelablaufverfolgungen usw.</span><span class="sxs-lookup"><span data-stu-id="4d8ce-107">It allows setting and removing breakpoints, stepping through execution, exploring stack traces, etc.</span></span>

| | |
|-|-|
| [**<span data-ttu-id="4d8ce-108">Methoden</span><span class="sxs-lookup"><span data-stu-id="4d8ce-108">Methods</span></span>**](#methods) | <span data-ttu-id="4d8ce-109">[aktivieren](#enable), [Deaktivieren](#disable), [getPossibleBreakpoints](#getpossiblebreakpoints), [setBreakpointsActive](#setbreakpointsactive), [setBreakpointByUrl](#setbreakpointbyurl), [setbreak Point](#setbreakpoint), [removeBreakpoint](#removebreakpoint), [Zustellung](#stepover), [stepInto](#stepinto), [aussteigen](#stepout), [Anhalten](#pause), [fortsetzen](#resume), [getScriptSource](#getscriptsource), [setPauseOnExceptions](#setpauseonexceptions), [evaluateOnCallFrame](#evaluateoncallframe), [setvariablevalue](#setvariablevalue), [setBlackboxPatterns](#setblackboxpatterns), [msSetDebuggerPropertyValue](#mssetdebuggerpropertyvalue)</span><span class="sxs-lookup"><span data-stu-id="4d8ce-109">[enable](#enable), [disable](#disable), [getPossibleBreakpoints](#getpossiblebreakpoints), [setBreakpointsActive](#setbreakpointsactive), [setBreakpointByUrl](#setbreakpointbyurl), [setBreakpoint](#setbreakpoint), [removeBreakpoint](#removebreakpoint), [stepOver](#stepover), [stepInto](#stepinto), [stepOut](#stepout), [pause](#pause), [resume](#resume), [getScriptSource](#getscriptsource), [setPauseOnExceptions](#setpauseonexceptions), [evaluateOnCallFrame](#evaluateoncallframe), [setVariableValue](#setvariablevalue), [setBlackboxPatterns](#setblackboxpatterns), [msSetDebuggerPropertyValue](#mssetdebuggerpropertyvalue)</span></span> |
| [**<span data-ttu-id="4d8ce-110">Veranstaltungen</span><span class="sxs-lookup"><span data-stu-id="4d8ce-110">Events</span></span>**](#events) | <span data-ttu-id="4d8ce-111">[scriptParsed](#scriptparsed), [breakpointResolved](#breakpointresolved), [angehalten](#paused), [fortgesetzt](#resumed)</span><span class="sxs-lookup"><span data-stu-id="4d8ce-111">[scriptParsed](#scriptparsed), [breakpointResolved](#breakpointresolved), [paused](#paused), [resumed](#resumed)</span></span> |
| [**<span data-ttu-id="4d8ce-112">Typen</span><span class="sxs-lookup"><span data-stu-id="4d8ce-112">Types</span></span>**](#types) | <span data-ttu-id="4d8ce-113">[Breakpoint](#breakpointid), [CallFrameId](#callframeid), [Location](#location), [BreakLocation](#breaklocation), [CallFrame](#callframe), [Scope](#scope)</span><span class="sxs-lookup"><span data-stu-id="4d8ce-113">[BreakpointId](#breakpointid), [CallFrameId](#callframeid), [Location](#location), [BreakLocation](#breaklocation), [CallFrame](#callframe), [Scope](#scope)</span></span> |
| [**<span data-ttu-id="4d8ce-114">Abhängigkeiten</span><span class="sxs-lookup"><span data-stu-id="4d8ce-114">Dependencies</span></span>**](#dependencies) | [<span data-ttu-id="4d8ce-115">Laufzeit</span><span class="sxs-lookup"><span data-stu-id="4d8ce-115">Runtime</span></span>](runtime.md) |
## <span data-ttu-id="4d8ce-116">Methoden</span><span class="sxs-lookup"><span data-stu-id="4d8ce-116">Methods</span></span>

### <span data-ttu-id="4d8ce-117">Aktivieren</span><span class="sxs-lookup"><span data-stu-id="4d8ce-117">enable</span></span>
<span data-ttu-id="4d8ce-118">Aktiviert den Debugger für die angegebene Seite.</span><span class="sxs-lookup"><span data-stu-id="4d8ce-118">Enables debugger for the given page.</span></span> <span data-ttu-id="4d8ce-119">Clients sollten nicht davon ausgehen, dass das Debuggen aktiviert wurde, bis das Ergebnis für diesen Befehl empfangen wurde.</span><span class="sxs-lookup"><span data-stu-id="4d8ce-119">Clients should not assume that the debugging has been enabled until the result for this command is received.</span></span>


---

### <span data-ttu-id="4d8ce-120">Deaktivieren </span><span class="sxs-lookup"><span data-stu-id="4d8ce-120">disable</span></span>
<span data-ttu-id="4d8ce-121">Deaktiviert den Debugger für die angegebene Seite.</span><span class="sxs-lookup"><span data-stu-id="4d8ce-121">Disables debugger for given page.</span></span>


---

### <span data-ttu-id="4d8ce-122">getPossibleBreakpoints</span><span class="sxs-lookup"><span data-stu-id="4d8ce-122">getPossibleBreakpoints</span></span>
<span data-ttu-id="4d8ce-123">Gibt mögliche Speicherorte für Breakpoint zurück.</span><span class="sxs-lookup"><span data-stu-id="4d8ce-123">Returns possible locations for breakpoint.</span></span> <span data-ttu-id="4d8ce-124">die Skript-Nr in Start-und Endbereich-Speicherorten sollte identisch sein.</span><span class="sxs-lookup"><span data-stu-id="4d8ce-124">scriptId in start and end range locations should be the same.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="4d8ce-125">Parameter</span><span class="sxs-lookup"><span data-stu-id="4d8ce-125">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="4d8ce-126">start</span><span class="sxs-lookup"><span data-stu-id="4d8ce-126">start</span></span></td>
            <td><a href="#location"><code class="flyout">Location</code></a></td>
            <td><span data-ttu-id="4d8ce-127">Anfang des Bereichs, in dem mögliche Haltepunkte in der Position durchsucht werden.</span><span class="sxs-lookup"><span data-stu-id="4d8ce-127">Start of range to search possible breakpoint locations in.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="4d8ce-128">Aufhören</span><span class="sxs-lookup"><span data-stu-id="4d8ce-128">end</span></span></td>
            <td><a href="#location"><code class="flyout">Location</code></a></td>
            <td><span data-ttu-id="4d8ce-129">Ende des Bereichs, in dem mögliche Haltepunkte in (ohne) durchsucht werden.</span><span class="sxs-lookup"><span data-stu-id="4d8ce-129">End of range to search possible breakpoint locations in (excluding).</span></span> <span data-ttu-id="4d8ce-130">Wenn keine Angabe erfolgt, wird das Ende von Skripten als Bereichsende verwendet.</span><span class="sxs-lookup"><span data-stu-id="4d8ce-130">When not specified, end of scripts is used as end of range.</span></span></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="4d8ce-131">Gibt</span><span class="sxs-lookup"><span data-stu-id="4d8ce-131">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="4d8ce-132">Speicherorte</span><span class="sxs-lookup"><span data-stu-id="4d8ce-132">locations</span></span></td>
            <td><a href="#breaklocation"><code class="flyout">BreakLocation</code></a></td>
            <td><span data-ttu-id="4d8ce-133">Liste der möglichen Haltepunkt Positionen</span><span class="sxs-lookup"><span data-stu-id="4d8ce-133">List of the possible breakpoint locations.</span></span></td>
        </tr>
    </tbody>
</table>

---

### <span data-ttu-id="4d8ce-134">setBreakpointsActive</span><span class="sxs-lookup"><span data-stu-id="4d8ce-134">setBreakpointsActive</span></span>
<span data-ttu-id="4d8ce-135">Aktiviert/deaktiviert alle Haltepunkte auf der Seite.</span><span class="sxs-lookup"><span data-stu-id="4d8ce-135">Activates / deactivates all breakpoints on the page.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="4d8ce-136">Parameter</span><span class="sxs-lookup"><span data-stu-id="4d8ce-136">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="4d8ce-137">active</span><span class="sxs-lookup"><span data-stu-id="4d8ce-137">active</span></span></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="4d8ce-138">Neuer Wert für Haltepunkte für aktiven Zustand.</span><span class="sxs-lookup"><span data-stu-id="4d8ce-138">New value for breakpoints active state.</span></span></td>
        </tr>
    </tbody>
</table>

---

### <span data-ttu-id="4d8ce-139">setBreakpointByUrl</span><span class="sxs-lookup"><span data-stu-id="4d8ce-139">setBreakpointByUrl</span></span>
<span data-ttu-id="4d8ce-140">Legt den JavaScript-Haltepunkt an einer bestimmten Position fest, die entweder durch URL oder URL Regex angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="4d8ce-140">Sets JavaScript breakpoint at given location specified either by URL or URL regex.</span></span> <span data-ttu-id="4d8ce-141">Sobald dieser Befehl ausgegeben wurde, haben alle vorhandenen analysierten Skripts Haltepunkte aufgelöst und werden in der Eigenschaft zurückgegeben <code>locations</code> .</span><span class="sxs-lookup"><span data-stu-id="4d8ce-141">Once this command is issued, all existing parsed scripts will have breakpoints resolved and returned in <code>locations</code> property.</span></span> <span data-ttu-id="4d8ce-142">Eine weitere übereinstimmende Skript Analyse führt dazu, dass nachfolgende <code>breakpointResolved</code> Ereignisse ausgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="4d8ce-142">Further matching script parsing will result in subsequent <code>breakpointResolved</code> events issued.</span></span> <span data-ttu-id="4d8ce-143">Dieser logische Haltepunkt überlebt das erneute Laden von Seiten.</span><span class="sxs-lookup"><span data-stu-id="4d8ce-143">This logical breakpoint will survive page reloads.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="4d8ce-144">Parameter</span><span class="sxs-lookup"><span data-stu-id="4d8ce-144">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="4d8ce-145">LineNumber</span><span class="sxs-lookup"><span data-stu-id="4d8ce-145">lineNumber</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="4d8ce-146">Die Nummer der Zeile, auf die der Haltepunkt gesetzt werden soll.</span><span class="sxs-lookup"><span data-stu-id="4d8ce-146">Line number to set breakpoint at.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="4d8ce-147">URL</span><span class="sxs-lookup"><span data-stu-id="4d8ce-147">url</span></span> <br/> <i><span data-ttu-id="4d8ce-148">Optional</span><span class="sxs-lookup"><span data-stu-id="4d8ce-148">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="4d8ce-149">Die URL der Ressourcen, auf die der Haltepunkt gesetzt werden soll.</span><span class="sxs-lookup"><span data-stu-id="4d8ce-149">URL of the resources to set breakpoint on.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="4d8ce-150">urlRegex</span><span class="sxs-lookup"><span data-stu-id="4d8ce-150">urlRegex</span></span> <br/> <i><span data-ttu-id="4d8ce-151">Optional</span><span class="sxs-lookup"><span data-stu-id="4d8ce-151">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="4d8ce-152">Regex-Muster für die URLs der Ressourcen zum Festlegen von Haltepunkten.</span><span class="sxs-lookup"><span data-stu-id="4d8ce-152">Regex pattern for the URLs of the resources to set breakpoints on.</span></span> <span data-ttu-id="4d8ce-153">Entweder <code>url</code> oder <code>urlRegex</code> muss angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="4d8ce-153">Either <code>url</code> or <code>urlRegex</code> must be specified.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="4d8ce-154">ColumnNumber</span><span class="sxs-lookup"><span data-stu-id="4d8ce-154">columnNumber</span></span> <br/> <i><span data-ttu-id="4d8ce-155">Optional</span><span class="sxs-lookup"><span data-stu-id="4d8ce-155">optional</span></span></i></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="4d8ce-156">Offset in der Zeile, an der der Haltepunkt gesetzt werden soll.</span><span class="sxs-lookup"><span data-stu-id="4d8ce-156">Offset in the line to set breakpoint at.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="4d8ce-157">Bedingung</span><span class="sxs-lookup"><span data-stu-id="4d8ce-157">condition</span></span> <br/> <i><span data-ttu-id="4d8ce-158">Optional</span><span class="sxs-lookup"><span data-stu-id="4d8ce-158">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="4d8ce-159">Ausdruck, der als Haltepunktbedingung verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="4d8ce-159">Expression to use as a breakpoint condition.</span></span> <span data-ttu-id="4d8ce-160">Wenn angegeben, wird der Debugger nur an dem Haltepunkt angehalten, wenn dieser Ausdruck wahr ausgewertet wird.</span><span class="sxs-lookup"><span data-stu-id="4d8ce-160">When specified, debugger will only stop on the breakpoint if this expression evaluates to true.</span></span></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="4d8ce-161">Gibt</span><span class="sxs-lookup"><span data-stu-id="4d8ce-161">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="4d8ce-162">Haltepunkt-Nr</span><span class="sxs-lookup"><span data-stu-id="4d8ce-162">breakpointId</span></span></td>
            <td><a href="#breakpointid"><code class="flyout">BreakpointId</code></a></td>
            <td><span data-ttu-id="4d8ce-163">Die ID des erstellten Haltepunkts für Weitere Verweise.</span><span class="sxs-lookup"><span data-stu-id="4d8ce-163">Id of the created breakpoint for further reference.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="4d8ce-164">Speicherorte</span><span class="sxs-lookup"><span data-stu-id="4d8ce-164">locations</span></span></td>
            <td><a href="#location"><code class="flyout">Location[]</code></a></td>
            <td><span data-ttu-id="4d8ce-165">Liste der Speicherorte, in die dieser Haltepunkt nach dem Hinzufügen aufgelöst wurde.</span><span class="sxs-lookup"><span data-stu-id="4d8ce-165">List of the locations this breakpoint resolved into upon addition.</span></span></td>
        </tr>
    </tbody>
</table>

---

### <span data-ttu-id="4d8ce-166">setbreaker</span><span class="sxs-lookup"><span data-stu-id="4d8ce-166">setBreakpoint</span></span>
<span data-ttu-id="4d8ce-167">Legt den JavaScript-Haltepunkt an einer bestimmten Position fest.</span><span class="sxs-lookup"><span data-stu-id="4d8ce-167">Sets JavaScript breakpoint at a given location.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="4d8ce-168">Parameter</span><span class="sxs-lookup"><span data-stu-id="4d8ce-168">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="4d8ce-169">Lage</span><span class="sxs-lookup"><span data-stu-id="4d8ce-169">location</span></span></td>
            <td><a href="#location"><code class="flyout">Location</code></a></td>
            <td><span data-ttu-id="4d8ce-170">Die Position, an der der Haltepunkt gesetzt werden soll.</span><span class="sxs-lookup"><span data-stu-id="4d8ce-170">Location to set breakpoint in.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="4d8ce-171">Bedingung</span><span class="sxs-lookup"><span data-stu-id="4d8ce-171">condition</span></span> <br/> <i><span data-ttu-id="4d8ce-172">Optional</span><span class="sxs-lookup"><span data-stu-id="4d8ce-172">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="4d8ce-173">Ausdruck, der als Haltepunktbedingung verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="4d8ce-173">Expression to use as a breakpoint condition.</span></span> <span data-ttu-id="4d8ce-174">Wenn angegeben, wird der Debugger nur an dem Haltepunkt angehalten, wenn dieser Ausdruck wahr ausgewertet wird.</span><span class="sxs-lookup"><span data-stu-id="4d8ce-174">When specified, debugger will only stop on the breakpoint if this expression evaluates to true.</span></span></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="4d8ce-175">Gibt</span><span class="sxs-lookup"><span data-stu-id="4d8ce-175">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="4d8ce-176">Haltepunkt-Nr</span><span class="sxs-lookup"><span data-stu-id="4d8ce-176">breakpointId</span></span></td>
            <td><a href="#breakpointid"><code class="flyout">BreakpointId</code></a></td>
            <td><span data-ttu-id="4d8ce-177">Die ID des erstellten Haltepunkts für Weitere Verweise.</span><span class="sxs-lookup"><span data-stu-id="4d8ce-177">Id of the created breakpoint for further reference.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="4d8ce-178">actualLocation</span><span class="sxs-lookup"><span data-stu-id="4d8ce-178">actualLocation</span></span></td>
            <td><a href="#location"><code class="flyout">Location</code></a></td>
            <td><span data-ttu-id="4d8ce-179">Ort, in den dieser Haltepunkt aufgelöst wurde.</span><span class="sxs-lookup"><span data-stu-id="4d8ce-179">Location this breakpoint resolved into.</span></span></td>
        </tr>
    </tbody>
</table>

---

### <span data-ttu-id="4d8ce-180">removeBreakpoint</span><span class="sxs-lookup"><span data-stu-id="4d8ce-180">removeBreakpoint</span></span>
<span data-ttu-id="4d8ce-181">Entfernt den JavaScript-Haltepunkt.</span><span class="sxs-lookup"><span data-stu-id="4d8ce-181">Removes JavaScript breakpoint.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="4d8ce-182">Parameter</span><span class="sxs-lookup"><span data-stu-id="4d8ce-182">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="4d8ce-183">Haltepunkt-Nr</span><span class="sxs-lookup"><span data-stu-id="4d8ce-183">breakpointId</span></span></td>
            <td><a href="#breakpointid"><code class="flyout">BreakpointId</code></a></td>
            <td></td>
        </tr>
    </tbody>
</table>

---

### <span data-ttu-id="4d8ce-184">Zustellung</span><span class="sxs-lookup"><span data-stu-id="4d8ce-184">stepOver</span></span>
<span data-ttu-id="4d8ce-185">Schritte über die Anweisung.</span><span class="sxs-lookup"><span data-stu-id="4d8ce-185">Steps over the statement.</span></span>


---

### <span data-ttu-id="4d8ce-186">stepInto</span><span class="sxs-lookup"><span data-stu-id="4d8ce-186">stepInto</span></span>
<span data-ttu-id="4d8ce-187">Tritt in den Funktionsaufruf ein.</span><span class="sxs-lookup"><span data-stu-id="4d8ce-187">Steps into the function call.</span></span>


---

### <span data-ttu-id="4d8ce-188">stepOut</span><span class="sxs-lookup"><span data-stu-id="4d8ce-188">stepOut</span></span>
<span data-ttu-id="4d8ce-189">Schritte aus dem Funktionsaufruf.</span><span class="sxs-lookup"><span data-stu-id="4d8ce-189">Steps out of the function call.</span></span>


---

### <span data-ttu-id="4d8ce-190">pause</span><span class="sxs-lookup"><span data-stu-id="4d8ce-190">pause</span></span>
<span data-ttu-id="4d8ce-191">Stoppt bei der nächsten JavaScript-Anweisung.</span><span class="sxs-lookup"><span data-stu-id="4d8ce-191">Stops on the next JavaScript statement.</span></span>


---

### <span data-ttu-id="4d8ce-192">resume</span><span class="sxs-lookup"><span data-stu-id="4d8ce-192">resume</span></span>
<span data-ttu-id="4d8ce-193">Setzt die JavaScript-Ausführung fort.</span><span class="sxs-lookup"><span data-stu-id="4d8ce-193">Resumes JavaScript execution.</span></span>


---

### <span data-ttu-id="4d8ce-194">getScriptSource</span><span class="sxs-lookup"><span data-stu-id="4d8ce-194">getScriptSource</span></span>
<span data-ttu-id="4d8ce-195">Gibt die Quelle für das Skript mit der angegebenen ID zurück.</span><span class="sxs-lookup"><span data-stu-id="4d8ce-195">Returns source for the script with given id.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="4d8ce-196">Parameter</span><span class="sxs-lookup"><span data-stu-id="4d8ce-196">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="4d8ce-197">SkriptID</span><span class="sxs-lookup"><span data-stu-id="4d8ce-197">scriptId</span></span></td>
            <td><a href="runtime.md#scriptid"><code class="flyout">Runtime.ScriptId</code></a></td>
            <td><span data-ttu-id="4d8ce-198">Die ID des Skripts, für das die Quelle abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="4d8ce-198">Id of the script to get source for.</span></span></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="4d8ce-199">Gibt</span><span class="sxs-lookup"><span data-stu-id="4d8ce-199">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="4d8ce-200">scriptSource</span><span class="sxs-lookup"><span data-stu-id="4d8ce-200">scriptSource</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="4d8ce-201">Skript Quelle.</span><span class="sxs-lookup"><span data-stu-id="4d8ce-201">Script source.</span></span></td>
        </tr>
    </tbody>
</table>

---

### <span data-ttu-id="4d8ce-202">setPauseOnExceptions</span><span class="sxs-lookup"><span data-stu-id="4d8ce-202">setPauseOnExceptions</span></span>
<span data-ttu-id="4d8ce-203">Definiert die Pause für den Ausnahmezustand.</span><span class="sxs-lookup"><span data-stu-id="4d8ce-203">Defines pause on exceptions state.</span></span> <span data-ttu-id="4d8ce-204">Kann so eingestellt werden, dass bei allen Ausnahmen, nicht abgefangene Ausnahmen oder ohne Ausnahmen, beendet wird.</span><span class="sxs-lookup"><span data-stu-id="4d8ce-204">Can be set to stop on all exceptions, uncaught exceptions or no exceptions.</span></span> <span data-ttu-id="4d8ce-205">Anfängliche Pause für Ausnahmen Zustand ist <code>none</code> .</span><span class="sxs-lookup"><span data-stu-id="4d8ce-205">Initial pause on exceptions state is <code>none</code>.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="4d8ce-206">Parameter</span><span class="sxs-lookup"><span data-stu-id="4d8ce-206">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="4d8ce-207">Zustand</span><span class="sxs-lookup"><span data-stu-id="4d8ce-207">state</span></span></td>
            <td><code class="flyout">string</code> <br/> <i><span data-ttu-id="4d8ce-208">Zulässige Werte: keine, nicht abgefangen, alle</span><span class="sxs-lookup"><span data-stu-id="4d8ce-208">Allowed values: none, uncaught, all</span></span></i></td>
            <td><span data-ttu-id="4d8ce-209">Pausieren im Ausnahmen Modus.</span><span class="sxs-lookup"><span data-stu-id="4d8ce-209">Pause on exceptions mode.</span></span></td>
        </tr>
    </tbody>
</table>

---

### <span data-ttu-id="4d8ce-210">evaluateOnCallFrame</span><span class="sxs-lookup"><span data-stu-id="4d8ce-210">evaluateOnCallFrame</span></span>
<span data-ttu-id="4d8ce-211">Wertet den Ausdruck für einen angegebenen Aufruf Frame aus.</span><span class="sxs-lookup"><span data-stu-id="4d8ce-211">Evaluates expression on a given call frame.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="4d8ce-212">Parameter</span><span class="sxs-lookup"><span data-stu-id="4d8ce-212">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="4d8ce-213">callFrameId</span><span class="sxs-lookup"><span data-stu-id="4d8ce-213">callFrameId</span></span></td>
            <td><a href="#callframeid"><code class="flyout">CallFrameId</code></a></td>
            <td><span data-ttu-id="4d8ce-214">Die Frame-ID des Anrufs für die Auswertung.</span><span class="sxs-lookup"><span data-stu-id="4d8ce-214">Call frame identifier to evaluate on.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="4d8ce-215">Ausdruck</span><span class="sxs-lookup"><span data-stu-id="4d8ce-215">expression</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="4d8ce-216">Ausdruck, der ausgewertet werden soll.</span><span class="sxs-lookup"><span data-stu-id="4d8ce-216">Expression to evaluate.</span></span></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="4d8ce-217">Gibt</span><span class="sxs-lookup"><span data-stu-id="4d8ce-217">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="4d8ce-218">Ergebnis</span><span class="sxs-lookup"><span data-stu-id="4d8ce-218">result</span></span></td>
            <td><a href="runtime.md#remoteobject"><code class="flyout">Runtime.RemoteObject</code></a></td>
            <td><span data-ttu-id="4d8ce-219">Objektwrapper für das Auswertungsergebnis</span><span class="sxs-lookup"><span data-stu-id="4d8ce-219">Object wrapper for the evaluation result.</span></span></td>
        </tr>
    </tbody>
</table>

---

### <span data-ttu-id="4d8ce-220">setvariablevalue</span><span class="sxs-lookup"><span data-stu-id="4d8ce-220">setVariableValue</span></span>
<span data-ttu-id="4d8ce-221">Ändert den Wert der Variablen in einem callframe.</span><span class="sxs-lookup"><span data-stu-id="4d8ce-221">Changes value of variable in a callframe.</span></span> <span data-ttu-id="4d8ce-222">Objektbasierte Bereiche werden nicht unterstützt und müssen manuell mutiert werden.</span><span class="sxs-lookup"><span data-stu-id="4d8ce-222">Object-based scopes are not supported and must be mutated manually.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="4d8ce-223">Parameter</span><span class="sxs-lookup"><span data-stu-id="4d8ce-223">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="4d8ce-224">scopeNumber</span><span class="sxs-lookup"><span data-stu-id="4d8ce-224">scopeNumber</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="4d8ce-225">0-basierte Anzahl des Bereichs, wie er in der Bereichskette aufgeführt ist.</span><span class="sxs-lookup"><span data-stu-id="4d8ce-225">0-based number of scope as was listed in scope chain.</span></span> <span data-ttu-id="4d8ce-226">Nur "local"-, "Closure"-und "Catch"-Bereichstypen sind zulässig.</span><span class="sxs-lookup"><span data-stu-id="4d8ce-226">Only 'local', 'closure' and 'catch' scope types are allowed.</span></span> <span data-ttu-id="4d8ce-227">Andere Bereiche können manuell manipuliert werden.</span><span class="sxs-lookup"><span data-stu-id="4d8ce-227">Other scopes could be manipulated manually.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="4d8ce-228">variableName</span><span class="sxs-lookup"><span data-stu-id="4d8ce-228">variableName</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="4d8ce-229">Name der Variablen.</span><span class="sxs-lookup"><span data-stu-id="4d8ce-229">Variable name.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="4d8ce-230">NewValue</span><span class="sxs-lookup"><span data-stu-id="4d8ce-230">newValue</span></span></td>
            <td><a href="runtime.md#callargument"><code class="flyout">Runtime.CallArgument</code></a></td>
            <td><span data-ttu-id="4d8ce-231">Neuer Variablenwert.</span><span class="sxs-lookup"><span data-stu-id="4d8ce-231">New variable value.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="4d8ce-232">callFrameId</span><span class="sxs-lookup"><span data-stu-id="4d8ce-232">callFrameId</span></span></td>
            <td><a href="#callframeid"><code class="flyout">CallFrameId</code></a></td>
            <td><span data-ttu-id="4d8ce-233">Die ID der callframe, die Variable enthält.</span><span class="sxs-lookup"><span data-stu-id="4d8ce-233">Id of callframe that holds variable.</span></span></td>
        </tr>
    </tbody>
</table>

---

### <span data-ttu-id="4d8ce-234">setBlackboxPatterns</span><span class="sxs-lookup"><span data-stu-id="4d8ce-234">setBlackboxPatterns</span></span>
<span><b><span data-ttu-id="4d8ce-235">Experimenteller.</span><span class="sxs-lookup"><span data-stu-id="4d8ce-235">Experimental.</span></span> </b></span><span data-ttu-id="4d8ce-236">Ersetzen Sie frühere Blackbox-Muster durch übergebene.</span><span class="sxs-lookup"><span data-stu-id="4d8ce-236">Replace previous blackbox patterns with passed ones.</span></span> <span data-ttu-id="4d8ce-237">Zwingt das Back-End, die Schritt-oder Pausierung in Skripts zu überspringen, wobei die URL einem der Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="4d8ce-237">Forces backend to skip stepping/pausing in scripts with url matching one of the patterns.</span></span> <span data-ttu-id="4d8ce-238">Der Debugger versucht, das blackboxed-Skript zu verlassen, indem es mehrere Male "Step in" ausführt und schließlich auf "Step out" zurückgegriffen wird, wenn es nicht erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="4d8ce-238">The debugger will try to leave blackboxed script by performing 'step in' several times, finally resorting to 'step out' if unsuccessful.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="4d8ce-239">Parameter</span><span class="sxs-lookup"><span data-stu-id="4d8ce-239">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="4d8ce-240">Muster</span><span class="sxs-lookup"><span data-stu-id="4d8ce-240">patterns</span></span></td>
            <td><code class="flyout">string[]</code></td>
            <td><span data-ttu-id="4d8ce-241">Array von Regexps, die verwendet werden, um die Skript-URL für den Blackbox-Zustand zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="4d8ce-241">Array of regexps that will be used to check script url for blackbox state.</span></span></td>
        </tr>
    </tbody>
</table>

---

### <span data-ttu-id="4d8ce-242">msSetDebuggerPropertyValue</span><span class="sxs-lookup"><span data-stu-id="4d8ce-242">msSetDebuggerPropertyValue</span></span>
<span><b><span data-ttu-id="4d8ce-243">Experimenteller.</span><span class="sxs-lookup"><span data-stu-id="4d8ce-243">Experimental.</span></span> </b></span><span data-ttu-id="4d8ce-244">Microsoft: legt die angegebene Debugger-Eigenschaft auf den angegebenen Wert fest.</span><span class="sxs-lookup"><span data-stu-id="4d8ce-244">Microsoft: Sets the specified debugger property to the specified value.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="4d8ce-245">Parameter</span><span class="sxs-lookup"><span data-stu-id="4d8ce-245">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="4d8ce-246">debuggerPropertyId</span><span class="sxs-lookup"><span data-stu-id="4d8ce-246">debuggerPropertyId</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="4d8ce-247">Microsoft: die Eigenschafts-ID (also msDebuggerPropertyId), die Sie festlegen möchten.</span><span class="sxs-lookup"><span data-stu-id="4d8ce-247">Microsoft: The property id (i.e. msDebuggerPropertyId) to set.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="4d8ce-248">NewValue</span><span class="sxs-lookup"><span data-stu-id="4d8ce-248">newValue</span></span></td>
            <td><code class="flyout">string</code></td>
            <td></td>
        </tr>
    </tbody>
</table>

---

## <span data-ttu-id="4d8ce-249">Veranstaltungen</span><span class="sxs-lookup"><span data-stu-id="4d8ce-249">Events</span></span>

### <span data-ttu-id="4d8ce-250">scriptParsed</span><span class="sxs-lookup"><span data-stu-id="4d8ce-250">scriptParsed</span></span>
<span data-ttu-id="4d8ce-251">Wird ausgelöst, wenn das Skript analysiert wird.</span><span class="sxs-lookup"><span data-stu-id="4d8ce-251">Fired when the script is parsed.</span></span> <span data-ttu-id="4d8ce-252">Dieses Ereignis wird beim Aktivieren des Debuggers auch für alle bekannten und nicht gesammelten Skripts ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="4d8ce-252">This event is also fired for all known and uncollected scripts upon enabling debugger.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="4d8ce-253">Parameter</span><span class="sxs-lookup"><span data-stu-id="4d8ce-253">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="4d8ce-254">SkriptID</span><span class="sxs-lookup"><span data-stu-id="4d8ce-254">scriptId</span></span></td>
            <td><a href="runtime.md#scriptid"><code class="flyout">Runtime.ScriptId</code></a></td>
            <td><span data-ttu-id="4d8ce-255">Der Bezeichner des analysierten Skripts.</span><span class="sxs-lookup"><span data-stu-id="4d8ce-255">Identifier of the script parsed.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="4d8ce-256">URL</span><span class="sxs-lookup"><span data-stu-id="4d8ce-256">url</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="4d8ce-257">Die URL oder der Name des analysierten Skripts (sofern vorhanden).</span><span class="sxs-lookup"><span data-stu-id="4d8ce-257">URL or name of the script parsed (if any).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="4d8ce-258">startLine</span><span class="sxs-lookup"><span data-stu-id="4d8ce-258">startLine</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="4d8ce-259">Der Offset des Skripts innerhalb der Ressource mit der angegebenen URL (für Skripttags).</span><span class="sxs-lookup"><span data-stu-id="4d8ce-259">Line offset of the script within the resource with given URL (for script tags).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="4d8ce-260">startColumn</span><span class="sxs-lookup"><span data-stu-id="4d8ce-260">startColumn</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="4d8ce-261">Spaltenoffset des Skripts innerhalb der Ressource mit der angegebenen URL.</span><span class="sxs-lookup"><span data-stu-id="4d8ce-261">Column offset of the script within the resource with given URL.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="4d8ce-262">endLine</span><span class="sxs-lookup"><span data-stu-id="4d8ce-262">endLine</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="4d8ce-263">Letzte Zeile des Skripts.</span><span class="sxs-lookup"><span data-stu-id="4d8ce-263">Last line of the script.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="4d8ce-264">endColumn</span><span class="sxs-lookup"><span data-stu-id="4d8ce-264">endColumn</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="4d8ce-265">Die Länge der letzten Zeile des Skripts.</span><span class="sxs-lookup"><span data-stu-id="4d8ce-265">Length of the last line of the script.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="4d8ce-266">executionContextId</span><span class="sxs-lookup"><span data-stu-id="4d8ce-266">executionContextId</span></span></td>
            <td><a href="runtime.md#executioncontextid"><code class="flyout">Runtime.ExecutionContextId</code></a></td>
            <td><span data-ttu-id="4d8ce-267">Gibt den Skript Erstellungs Kontext an.</span><span class="sxs-lookup"><span data-stu-id="4d8ce-267">Specifies script creation context.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="4d8ce-268">sourceMapURL</span><span class="sxs-lookup"><span data-stu-id="4d8ce-268">sourceMapURL</span></span> <br/> <i><span data-ttu-id="4d8ce-269">Optional</span><span class="sxs-lookup"><span data-stu-id="4d8ce-269">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="4d8ce-270">Die URL der Quell Karte, die dem Skript zugeordnet ist (sofern vorhanden).</span><span class="sxs-lookup"><span data-stu-id="4d8ce-270">URL of source map associated with script (if any).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="4d8ce-271">Länge</span><span class="sxs-lookup"><span data-stu-id="4d8ce-271">length</span></span> <br/> <i><span data-ttu-id="4d8ce-272">Optional</span><span class="sxs-lookup"><span data-stu-id="4d8ce-272">optional</span></span></i></td>
            <td><code class="flyout">integer</code></td>
            <td><span><b><span data-ttu-id="4d8ce-273">Experimenteller.</span><span class="sxs-lookup"><span data-stu-id="4d8ce-273">Experimental.</span></span> </b></span><span data-ttu-id="4d8ce-274">Diese Skript Länge.</span><span class="sxs-lookup"><span data-stu-id="4d8ce-274">This script length.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="4d8ce-275">msParentId</span><span class="sxs-lookup"><span data-stu-id="4d8ce-275">msParentId</span></span> <br/> <i><span data-ttu-id="4d8ce-276">Optional</span><span class="sxs-lookup"><span data-stu-id="4d8ce-276">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span><b><span data-ttu-id="4d8ce-277">Experimenteller.</span><span class="sxs-lookup"><span data-stu-id="4d8ce-277">Experimental.</span></span> </b></span><span data-ttu-id="4d8ce-278">Hierbei handelt es sich um die übergeordnete Dokument-ID.</span><span class="sxs-lookup"><span data-stu-id="4d8ce-278">This is the parent document ID.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="4d8ce-279">msMimeType</span><span class="sxs-lookup"><span data-stu-id="4d8ce-279">msMimeType</span></span> <br/> <i><span data-ttu-id="4d8ce-280">Optional</span><span class="sxs-lookup"><span data-stu-id="4d8ce-280">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span><b><span data-ttu-id="4d8ce-281">Experimenteller.</span><span class="sxs-lookup"><span data-stu-id="4d8ce-281">Experimental.</span></span> </b></span><span data-ttu-id="4d8ce-282">Dies ist der MIME-Typ.</span><span class="sxs-lookup"><span data-stu-id="4d8ce-282">This is the mime type.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="4d8ce-283">msIsDynamicCode</span><span class="sxs-lookup"><span data-stu-id="4d8ce-283">msIsDynamicCode</span></span> <br/> <i><span data-ttu-id="4d8ce-284">Optional</span><span class="sxs-lookup"><span data-stu-id="4d8ce-284">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span><b><span data-ttu-id="4d8ce-285">Experimenteller.</span><span class="sxs-lookup"><span data-stu-id="4d8ce-285">Experimental.</span></span> </b></span><span data-ttu-id="4d8ce-286">Gibt an, ob es sich um dynamischen Code handelt.</span><span class="sxs-lookup"><span data-stu-id="4d8ce-286">This indicates whether it is dynamic code.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="4d8ce-287">msLongDocumentId</span><span class="sxs-lookup"><span data-stu-id="4d8ce-287">msLongDocumentId</span></span> <br/> <i><span data-ttu-id="4d8ce-288">Optional</span><span class="sxs-lookup"><span data-stu-id="4d8ce-288">optional</span></span></i></td>
            <td><code class="flyout">integer</code></td>
            <td><span><b><span data-ttu-id="4d8ce-289">Experimenteller.</span><span class="sxs-lookup"><span data-stu-id="4d8ce-289">Experimental.</span></span> </b></span><span data-ttu-id="4d8ce-290">Dies ist die lange Dokument-ID.</span><span class="sxs-lookup"><span data-stu-id="4d8ce-290">This is the long document ID.</span></span></td>
        </tr>
    </tbody>
</table>

---

### <span data-ttu-id="4d8ce-291">breakpointResolved</span><span class="sxs-lookup"><span data-stu-id="4d8ce-291">breakpointResolved</span></span>
<span data-ttu-id="4d8ce-292">Wird ausgelöst, wenn der Haltepunkt zu einem tatsächlichen Skript und Speicherort aufgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="4d8ce-292">Fired when breakpoint is resolved to an actual script and location.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="4d8ce-293">Parameter</span><span class="sxs-lookup"><span data-stu-id="4d8ce-293">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="4d8ce-294">Haltepunkt-Nr</span><span class="sxs-lookup"><span data-stu-id="4d8ce-294">breakpointId</span></span></td>
            <td><a href="#breakpointid"><code class="flyout">BreakpointId</code></a></td>
            <td><span data-ttu-id="4d8ce-295">Eindeutiger Haltepunktbezeichner.</span><span class="sxs-lookup"><span data-stu-id="4d8ce-295">Breakpoint unique identifier.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="4d8ce-296">Lage</span><span class="sxs-lookup"><span data-stu-id="4d8ce-296">location</span></span></td>
            <td><a href="#location"><code class="flyout">Location</code></a></td>
            <td><span data-ttu-id="4d8ce-297">Tatsächliche Haltepunktposition.</span><span class="sxs-lookup"><span data-stu-id="4d8ce-297">Actual breakpoint location.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="4d8ce-298">msLength</span><span class="sxs-lookup"><span data-stu-id="4d8ce-298">msLength</span></span> <br/> <i><span data-ttu-id="4d8ce-299">Optional</span><span class="sxs-lookup"><span data-stu-id="4d8ce-299">optional</span></span></i></td>
            <td><code class="flyout">integer</code></td>
            <td><span><b><span data-ttu-id="4d8ce-300">Experimenteller.</span><span class="sxs-lookup"><span data-stu-id="4d8ce-300">Experimental.</span></span> </b></span><span data-ttu-id="4d8ce-301">Microsoft: Länge des Codes (also Anzahl der Zeichen) an der Haltepunktposition.</span><span class="sxs-lookup"><span data-stu-id="4d8ce-301">Microsoft: Length of code (i.e. number of characters) at the breakpoint location.</span></span></td>
        </tr>
    </tbody>
</table>

---

### <span data-ttu-id="4d8ce-302">angehalten</span><span class="sxs-lookup"><span data-stu-id="4d8ce-302">paused</span></span>
<span data-ttu-id="4d8ce-303">Wird ausgelöst, wenn die Debugger für einen Haltepunkt oder eine Ausnahme unterbrechen.</span><span class="sxs-lookup"><span data-stu-id="4d8ce-303">Fired when the debuggers breaks for a breakpoint or exception.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="4d8ce-304">Parameter</span><span class="sxs-lookup"><span data-stu-id="4d8ce-304">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="4d8ce-305">callFrames</span><span class="sxs-lookup"><span data-stu-id="4d8ce-305">callFrames</span></span></td>
            <td><a href="#callframe"><code class="flyout">CallFrame[]</code></a></td>
            <td><span data-ttu-id="4d8ce-306">Aufrufliste der Debugger wurde angehalten.</span><span class="sxs-lookup"><span data-stu-id="4d8ce-306">Call stack the debugger stopped on.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="4d8ce-307">Grund</span><span class="sxs-lookup"><span data-stu-id="4d8ce-307">reason</span></span></td>
            <td><code class="flyout">string</code> <br/> <i><span data-ttu-id="4d8ce-308">Zulässige Werte: Haltepunkt, Schritt, Ausnahme, sonstige</span><span class="sxs-lookup"><span data-stu-id="4d8ce-308">Allowed values: breakpoint, step, exception, other</span></span></i></td>
            <td><span data-ttu-id="4d8ce-309">Grund für Pause.</span><span class="sxs-lookup"><span data-stu-id="4d8ce-309">Pause reason.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="4d8ce-310">data</span><span class="sxs-lookup"><span data-stu-id="4d8ce-310">data</span></span> <br/> <i><span data-ttu-id="4d8ce-311">Optional</span><span class="sxs-lookup"><span data-stu-id="4d8ce-311">optional</span></span></i></td>
            <td><code class="flyout">object</code></td>
            <td><span data-ttu-id="4d8ce-312">Objekt, das Bruch spezifische Zusatzeigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="4d8ce-312">Object containing break-specific auxiliary properties.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="4d8ce-313">hitBreakpoints</span><span class="sxs-lookup"><span data-stu-id="4d8ce-313">hitBreakpoints</span></span> <br/> <i><span data-ttu-id="4d8ce-314">Optional</span><span class="sxs-lookup"><span data-stu-id="4d8ce-314">optional</span></span></i></td>
            <td><code class="flyout">string[]</code></td>
            <td><span data-ttu-id="4d8ce-315">Treffer Haltepunkte-IDs</span><span class="sxs-lookup"><span data-stu-id="4d8ce-315">Hit breakpoints IDs</span></span></td>
        </tr>
    </tbody>
</table>

---

### <span data-ttu-id="4d8ce-316">wieder</span><span class="sxs-lookup"><span data-stu-id="4d8ce-316">resumed</span></span>
<span data-ttu-id="4d8ce-317">Wird ausgelöst, wenn der Debugger die Ausführung fortsetzt.</span><span class="sxs-lookup"><span data-stu-id="4d8ce-317">Fired when the debugger resumes execution.</span></span>


---

## <span data-ttu-id="4d8ce-318">Typen</span><span class="sxs-lookup"><span data-stu-id="4d8ce-318">Types</span></span>

### <a name="breakpointid"></a> <span data-ttu-id="4d8ce-319">Haltepunkt-Nr</span><span class="sxs-lookup"><span data-stu-id="4d8ce-319">BreakpointId</span></span> `string`

<span data-ttu-id="4d8ce-320">Haltepunkt-ID.</span><span class="sxs-lookup"><span data-stu-id="4d8ce-320">Breakpoint identifier.</span></span>


---

### <a name="callframeid"></a> <span data-ttu-id="4d8ce-321">CallFrameId</span><span class="sxs-lookup"><span data-stu-id="4d8ce-321">CallFrameId</span></span> `string`

<span data-ttu-id="4d8ce-322">Anruf Rahmen-ID.</span><span class="sxs-lookup"><span data-stu-id="4d8ce-322">Call frame identifier.</span></span>


---

### <a name="location"></a> <span data-ttu-id="4d8ce-323">Pfad</span><span class="sxs-lookup"><span data-stu-id="4d8ce-323">Location</span></span> `object`

<span data-ttu-id="4d8ce-324">Speicherort im Quellcode.</span><span class="sxs-lookup"><span data-stu-id="4d8ce-324">Location in the source code.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="4d8ce-325">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="4d8ce-325">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="4d8ce-326">SkriptID</span><span class="sxs-lookup"><span data-stu-id="4d8ce-326">scriptId</span></span></td>
            <td><a href="runtime.md#scriptid"><code class="flyout">Runtime.ScriptId</code></a></td>
            <td><span data-ttu-id="4d8ce-327">Skriptbezeichner, wie in <code>Debugger.scriptParsed</code> .</span><span class="sxs-lookup"><span data-stu-id="4d8ce-327">Script identifier as reported in the <code>Debugger.scriptParsed</code>.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="4d8ce-328">LineNumber</span><span class="sxs-lookup"><span data-stu-id="4d8ce-328">lineNumber</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="4d8ce-329">Die Nummer der Zeile im Skript (0-basiert).</span><span class="sxs-lookup"><span data-stu-id="4d8ce-329">Line number in the script (0-based).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="4d8ce-330">ColumnNumber</span><span class="sxs-lookup"><span data-stu-id="4d8ce-330">columnNumber</span></span> <br/> <i><span data-ttu-id="4d8ce-331">Optional</span><span class="sxs-lookup"><span data-stu-id="4d8ce-331">optional</span></span></i></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="4d8ce-332">Spaltennummer im Skript (0-basiert)</span><span class="sxs-lookup"><span data-stu-id="4d8ce-332">Column number in the script (0-based).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="4d8ce-333">msLength</span><span class="sxs-lookup"><span data-stu-id="4d8ce-333">msLength</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="4d8ce-334">Microsoft: Länge des Codes (also Anzahl der Zeichen) an diesem Aufruf Frame.</span><span class="sxs-lookup"><span data-stu-id="4d8ce-334">Microsoft: Length of code (i.e. number of characters) at this call frame.</span></span></td>
        </tr>
    </tbody>
</table>

---

### <a name="breaklocation"></a> <span data-ttu-id="4d8ce-335">BreakLocation</span><span class="sxs-lookup"><span data-stu-id="4d8ce-335">BreakLocation</span></span> `object`

<span data-ttu-id="4d8ce-336">Position im Quellcode unterbrechen.</span><span class="sxs-lookup"><span data-stu-id="4d8ce-336">Break location in the source code.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="4d8ce-337">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="4d8ce-337">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="4d8ce-338">SkriptID</span><span class="sxs-lookup"><span data-stu-id="4d8ce-338">scriptId</span></span></td>
            <td><a href="runtime.md#scriptid"><code class="flyout">Runtime.ScriptId</code></a></td>
            <td><span data-ttu-id="4d8ce-339">Skriptbezeichner, wie in <code>Debugger.scriptParsed</code> .</span><span class="sxs-lookup"><span data-stu-id="4d8ce-339">Script identifier as reported in the <code>Debugger.scriptParsed</code>.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="4d8ce-340">LineNumber</span><span class="sxs-lookup"><span data-stu-id="4d8ce-340">lineNumber</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="4d8ce-341">Die Nummer der Zeile im Skript (0-basiert).</span><span class="sxs-lookup"><span data-stu-id="4d8ce-341">Line number in the script (0-based).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="4d8ce-342">ColumnNumber</span><span class="sxs-lookup"><span data-stu-id="4d8ce-342">columnNumber</span></span> <br/> <i><span data-ttu-id="4d8ce-343">Optional</span><span class="sxs-lookup"><span data-stu-id="4d8ce-343">optional</span></span></i></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="4d8ce-344">Spaltennummer im Skript (0-basiert)</span><span class="sxs-lookup"><span data-stu-id="4d8ce-344">Column number in the script (0-based).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="4d8ce-345">msLength</span><span class="sxs-lookup"><span data-stu-id="4d8ce-345">msLength</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="4d8ce-346">Microsoft: Länge des Codes (also Anzahl der Zeichen) an diesem Aufruf Frame.</span><span class="sxs-lookup"><span data-stu-id="4d8ce-346">Microsoft: Length of code (i.e. number of characters) at this call frame.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="4d8ce-347">Typ</span><span class="sxs-lookup"><span data-stu-id="4d8ce-347">type</span></span> <br/> <i><span data-ttu-id="4d8ce-348">Optional</span><span class="sxs-lookup"><span data-stu-id="4d8ce-348">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="4d8ce-349">Zulässige Werte: debuggerStatement, Aufruf, zurück.</span><span class="sxs-lookup"><span data-stu-id="4d8ce-349">Allowed values: debuggerStatement, call, return.</span></span></td>
        </tr>
    </tbody>
</table>

---

### <a name="callframe"></a> <span data-ttu-id="4d8ce-350">CallFrame</span><span class="sxs-lookup"><span data-stu-id="4d8ce-350">CallFrame</span></span> `object`

<span data-ttu-id="4d8ce-351">JavaScript-Anruf Rahmen.</span><span class="sxs-lookup"><span data-stu-id="4d8ce-351">JavaScript call frame.</span></span> <span data-ttu-id="4d8ce-352">Array von Anruf Frames aus der Aufrufliste.</span><span class="sxs-lookup"><span data-stu-id="4d8ce-352">Array of call frames form the call stack.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="4d8ce-353">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="4d8ce-353">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="4d8ce-354">callFrameId</span><span class="sxs-lookup"><span data-stu-id="4d8ce-354">callFrameId</span></span></td>
            <td><a href="#callframeid"><code class="flyout">CallFrameId</code></a></td>
            <td><span data-ttu-id="4d8ce-355">Anruf Rahmen-ID.</span><span class="sxs-lookup"><span data-stu-id="4d8ce-355">Call frame identifier.</span></span> <span data-ttu-id="4d8ce-356">Dieser Bezeichner ist nur gültig, wenn der Debugger angehalten wurde.</span><span class="sxs-lookup"><span data-stu-id="4d8ce-356">This identifier is only valid while the debugger is paused.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="4d8ce-357">FunctionName</span><span class="sxs-lookup"><span data-stu-id="4d8ce-357">functionName</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="4d8ce-358">Der Name der JavaScript-Funktion, die in diesem Aufruf Frame aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="4d8ce-358">Name of the JavaScript function called on this call frame.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="4d8ce-359">functionLocation</span><span class="sxs-lookup"><span data-stu-id="4d8ce-359">functionLocation</span></span> <br/> <i><span data-ttu-id="4d8ce-360">Optional</span><span class="sxs-lookup"><span data-stu-id="4d8ce-360">optional</span></span></i></td>
            <td><a href="#location"><code class="flyout">Location</code></a></td>
            <td><span><b><span data-ttu-id="4d8ce-361">Experimenteller.</span><span class="sxs-lookup"><span data-stu-id="4d8ce-361">Experimental.</span></span> </b></span><span data-ttu-id="4d8ce-362">Speicherort im Quellcode.</span><span class="sxs-lookup"><span data-stu-id="4d8ce-362">Location in the source code.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="4d8ce-363">Lage</span><span class="sxs-lookup"><span data-stu-id="4d8ce-363">location</span></span></td>
            <td><a href="#location"><code class="flyout">Location</code></a></td>
            <td><span data-ttu-id="4d8ce-364">Speicherort im Quellcode.</span><span class="sxs-lookup"><span data-stu-id="4d8ce-364">Location in the source code.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="4d8ce-365">URL</span><span class="sxs-lookup"><span data-stu-id="4d8ce-365">url</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="4d8ce-366">JavaScript-Skriptname oder-URL.</span><span class="sxs-lookup"><span data-stu-id="4d8ce-366">JavaScript script name or url.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="4d8ce-367">scopeChain</span><span class="sxs-lookup"><span data-stu-id="4d8ce-367">scopeChain</span></span></td>
            <td><a href="#scope"><code class="flyout">Scope[]</code></a></td>
            <td><span data-ttu-id="4d8ce-368">Bereichskette für diesen Aufruf Frame.</span><span class="sxs-lookup"><span data-stu-id="4d8ce-368">Scope chain for this call frame.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="4d8ce-369">Diese</span><span class="sxs-lookup"><span data-stu-id="4d8ce-369">this</span></span></td>
            <td><a href="runtime.md#remoteobject"><code class="flyout">Runtime.RemoteObject</code></a></td>
            <td><code>this</code> <span data-ttu-id="4d8ce-370">das Objekt für diesen Anruf Frame.</span><span class="sxs-lookup"><span data-stu-id="4d8ce-370">object for this call frame.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="4d8ce-371">returnValue</span><span class="sxs-lookup"><span data-stu-id="4d8ce-371">returnValue</span></span> <br/> <i><span data-ttu-id="4d8ce-372">Optional</span><span class="sxs-lookup"><span data-stu-id="4d8ce-372">optional</span></span></i></td>
            <td><a href="runtime.md#remoteobject"><code class="flyout">Runtime.RemoteObject</code></a></td>
            <td><span data-ttu-id="4d8ce-373">Der Wert, der zurückgegeben wird, wenn sich die Funktion am Rückgabe Punkt befindet.</span><span class="sxs-lookup"><span data-stu-id="4d8ce-373">The value being returned, if the function is at return point.</span></span></td>
        </tr>
    </tbody>
</table>

---

### <a name="scope"></a> <span data-ttu-id="4d8ce-374">Bereich</span><span class="sxs-lookup"><span data-stu-id="4d8ce-374">Scope</span></span> `object`

<span data-ttu-id="4d8ce-375">Beschreibung des Bereichs</span><span class="sxs-lookup"><span data-stu-id="4d8ce-375">Scope description.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="4d8ce-376">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="4d8ce-376">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="4d8ce-377">Typ</span><span class="sxs-lookup"><span data-stu-id="4d8ce-377">type</span></span></td>
            <td><code class="flyout">string</code> <br/> <i><span data-ttu-id="4d8ce-378">Zulässige Werte: Global, local, with, Closure, catch, Block, Script, eval, Module</span><span class="sxs-lookup"><span data-stu-id="4d8ce-378">Allowed values: global, local, with, closure, catch, block, script, eval, module</span></span></i></td>
            <td><span data-ttu-id="4d8ce-379">Scope-Typ.</span><span class="sxs-lookup"><span data-stu-id="4d8ce-379">Scope type.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="4d8ce-380">Objekt</span><span class="sxs-lookup"><span data-stu-id="4d8ce-380">object</span></span></td>
            <td><a href="runtime.md#remoteobject"><code class="flyout">Runtime.RemoteObject</code></a></td>
            <td><span data-ttu-id="4d8ce-381">Das Objekt, das den Bereich darstellt.</span><span class="sxs-lookup"><span data-stu-id="4d8ce-381">Object representing the scope.</span></span> <span data-ttu-id="4d8ce-382">Für <code>global</code> und <code>with</code> Bereiche stellt es das eigentliche Objekt dar; für die restlichen Bereiche ist es ein künstliches Transienten Objekt, das Bereichsvariablen als Eigenschaften auflistet.</span><span class="sxs-lookup"><span data-stu-id="4d8ce-382">For <code>global</code> and <code>with</code> scopes it represents the actual object; for the rest of the scopes, it is artificial transient object enumerating scope variables as its properties.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="4d8ce-383">name</span><span class="sxs-lookup"><span data-stu-id="4d8ce-383">name</span></span> <br/> <i><span data-ttu-id="4d8ce-384">Optional</span><span class="sxs-lookup"><span data-stu-id="4d8ce-384">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td></td>
        </tr>
        <tr>
            <td><span data-ttu-id="4d8ce-385">StartLocation</span><span class="sxs-lookup"><span data-stu-id="4d8ce-385">startLocation</span></span> <br/> <i><span data-ttu-id="4d8ce-386">Optional</span><span class="sxs-lookup"><span data-stu-id="4d8ce-386">optional</span></span></i></td>
            <td><a href="#location"><code class="flyout">Location</code></a></td>
            <td><span data-ttu-id="4d8ce-387">Speicherort im Quellcode, in dem der Bereich beginnt</span><span class="sxs-lookup"><span data-stu-id="4d8ce-387">Location in the source code where scope starts</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="4d8ce-388">endLocation</span><span class="sxs-lookup"><span data-stu-id="4d8ce-388">endLocation</span></span> <br/> <i><span data-ttu-id="4d8ce-389">Optional</span><span class="sxs-lookup"><span data-stu-id="4d8ce-389">optional</span></span></i></td>
            <td><a href="#location"><code class="flyout">Location</code></a></td>
            <td><span data-ttu-id="4d8ce-390">Speicherort im Quellcode, in dem der Bereich endet</span><span class="sxs-lookup"><span data-stu-id="4d8ce-390">Location in the source code where scope ends</span></span></td>
        </tr>
    </tbody>
</table>

---

## <span data-ttu-id="4d8ce-391">Abhängigkeiten</span><span class="sxs-lookup"><span data-stu-id="4d8ce-391">Dependencies</span></span>

[<span data-ttu-id="4d8ce-392">Laufzeit</span><span class="sxs-lookup"><span data-stu-id="4d8ce-392">Runtime</span></span>](runtime.md)
