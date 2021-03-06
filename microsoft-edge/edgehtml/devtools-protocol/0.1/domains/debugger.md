---
description: DevTools Protocol Version 0.1 (EdgeHTML)-Referenz für die Debuggerdomäne.  Die Debuggerdomäne macht JavaScript-Debuggingfunktionen verfügbar.  Es ermöglicht das Festlegen und Entfernen von Haltepunkten, das Schrittweise Durchbrechen der Ausführung, das Untersuchen von Stapelverfolgungen usw.
title: Debuggerdomäne – DevTools Protocol Version 0.1 (EdgeHTML)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/03/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.custom: seodec18
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: d63408e23fd8912cf617bfefae2b991387b45a38
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "11397678"
---
# <a name="debugger-domain---devtools-protocol-version-01-edgehtml"></a><span data-ttu-id="16a90-105">Debuggerdomäne – DevTools Protocol Version 0.1 (EdgeHTML)</span><span class="sxs-lookup"><span data-stu-id="16a90-105">Debugger Domain - DevTools Protocol Version 0.1 (EdgeHTML)</span></span>  
  
<span data-ttu-id="16a90-106">Die Debuggerdomäne macht JavaScript-Debuggingfunktionen verfügbar.</span><span class="sxs-lookup"><span data-stu-id="16a90-106">Debugger domain exposes JavaScript debugging capabilities.</span></span>  <span data-ttu-id="16a90-107">Es ermöglicht das Festlegen und Entfernen von Haltepunkten, das Schrittweise Durchbrechen der Ausführung, das Untersuchen von Stapelverfolgungen usw.</span><span class="sxs-lookup"><span data-stu-id="16a90-107">It allows setting and removing breakpoints, stepping through execution, exploring stack traces, etc.</span></span>

| <span data-ttu-id="16a90-108">Klassifizierung</span><span class="sxs-lookup"><span data-stu-id="16a90-108">Classification</span></span> | <span data-ttu-id="16a90-109">Member</span><span class="sxs-lookup"><span data-stu-id="16a90-109">Members</span></span> |  
|:--- |:--- |  
| [<span data-ttu-id="16a90-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="16a90-110">Methods</span></span>](#methods) | <span data-ttu-id="16a90-111">[enable](#enable), [disable](#disable), [getPossibleBreakpoints](#getpossiblebreakpoints), [setBreakpointsActive](#setbreakpointsactive), [setBreakpointByUrl](#setbreakpointbyurl), [setBreakpoint](#setbreakpoint), [removeBreakpoint](#removebreakpoint), [stepOver](#stepover), [stepInto](#stepinto), [stepOut](#stepout), [pause](#pause), [resume](#resume), [getScriptSource](#getscriptsource), [setPauseOnExceptions](#setpauseonexceptions), [evaluateOnCallFrame](#evaluateoncallframe), [setVariableValue](#setvariablevalue), [setBlackboxPatterns](#setblackboxpatterns), [msSetDebuggerPropertyValue](#mssetdebuggerpropertyvalue)</span><span class="sxs-lookup"><span data-stu-id="16a90-111">[enable](#enable), [disable](#disable), [getPossibleBreakpoints](#getpossiblebreakpoints), [setBreakpointsActive](#setbreakpointsactive), [setBreakpointByUrl](#setbreakpointbyurl), [setBreakpoint](#setbreakpoint), [removeBreakpoint](#removebreakpoint), [stepOver](#stepover), [stepInto](#stepinto), [stepOut](#stepout), [pause](#pause), [resume](#resume), [getScriptSource](#getscriptsource), [setPauseOnExceptions](#setpauseonexceptions), [evaluateOnCallFrame](#evaluateoncallframe), [setVariableValue](#setvariablevalue), [setBlackboxPatterns](#setblackboxpatterns), [msSetDebuggerPropertyValue](#mssetdebuggerpropertyvalue)</span></span> |  
| [<span data-ttu-id="16a90-112">Veranstaltungen</span><span class="sxs-lookup"><span data-stu-id="16a90-112">Events</span></span>](#events) | <span data-ttu-id="16a90-113">[scriptParsed](#scriptparsed), [breakpointResolved](#breakpointresolved), [paused](#paused), [resumed](#resumed)</span><span class="sxs-lookup"><span data-stu-id="16a90-113">[scriptParsed](#scriptparsed), [breakpointResolved](#breakpointresolved), [paused](#paused), [resumed](#resumed)</span></span> |  
| [<span data-ttu-id="16a90-114">Typen</span><span class="sxs-lookup"><span data-stu-id="16a90-114">Types</span></span>](#types) | <span data-ttu-id="16a90-115">[BreakpointId](#breakpointid), [CallFrameId](#callframeid), [Location](#location), [BreakLocation](#breaklocation), [CallFrame](#callframe), [Scope](#scope)</span><span class="sxs-lookup"><span data-stu-id="16a90-115">[BreakpointId](#breakpointid), [CallFrameId](#callframeid), [Location](#location), [BreakLocation](#breaklocation), [CallFrame](#callframe), [Scope](#scope)</span></span> |  
| [<span data-ttu-id="16a90-116">Abhängigkeiten</span><span class="sxs-lookup"><span data-stu-id="16a90-116">Dependencies</span></span>](#dependencies) | [<span data-ttu-id="16a90-117">Laufzeit</span><span class="sxs-lookup"><span data-stu-id="16a90-117">Runtime</span></span>](./runtime.md) |  

## <a name="methods"></a><span data-ttu-id="16a90-118">Methoden</span><span class="sxs-lookup"><span data-stu-id="16a90-118">Methods</span></span>  

### <a name="enable"></a><span data-ttu-id="16a90-119">Aktivieren</span><span class="sxs-lookup"><span data-stu-id="16a90-119">enable</span></span>  

<span data-ttu-id="16a90-120">Aktiviert den Debugger für die angegebene Seite.</span><span class="sxs-lookup"><span data-stu-id="16a90-120">Enables debugger for the given page.</span></span>  <span data-ttu-id="16a90-121">Clients sollten nicht davon ausgehen, dass das Debuggen aktiviert wurde, bis das Ergebnis für diesen Befehl empfangen wurde.</span><span class="sxs-lookup"><span data-stu-id="16a90-121">Clients should not assume that the debugging has been enabled until the result for this command is received.</span></span>  

&nbsp;  

---  

### <a name="disable"></a><span data-ttu-id="16a90-122">Deaktivieren </span><span class="sxs-lookup"><span data-stu-id="16a90-122">disable</span></span>  

<span data-ttu-id="16a90-123">Deaktiviert den Debugger für eine bestimmte Seite.</span><span class="sxs-lookup"><span data-stu-id="16a90-123">Disables debugger for given page.</span></span>  

&nbsp;  

---  

### <a name="getpossiblebreakpoints"></a><span data-ttu-id="16a90-124">getPossibleBreakpoints</span><span class="sxs-lookup"><span data-stu-id="16a90-124">getPossibleBreakpoints</span></span>  

<span data-ttu-id="16a90-125">Gibt mögliche Speicherorte für Haltepunkte zurück.</span><span class="sxs-lookup"><span data-stu-id="16a90-125">Returns possible locations for breakpoint.</span></span>  <span data-ttu-id="16a90-126">scriptId an Start- und Endbereichspositionen sollte identisch sein.</span><span class="sxs-lookup"><span data-stu-id="16a90-126">scriptId in start and end range locations should be the same.</span></span>  

| <span data-ttu-id="16a90-127">Parameter</span><span class="sxs-lookup"><span data-stu-id="16a90-127">Parameters</span></span> | <span data-ttu-id="16a90-128">Typ</span><span class="sxs-lookup"><span data-stu-id="16a90-128">Type</span></span> | <span data-ttu-id="16a90-129">Details</span><span class="sxs-lookup"><span data-stu-id="16a90-129">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="16a90-130">start</span><span class="sxs-lookup"><span data-stu-id="16a90-130">start</span></span> | [<span data-ttu-id="16a90-131">Ort</span><span class="sxs-lookup"><span data-stu-id="16a90-131">Location</span></span>](#location) | <span data-ttu-id="16a90-132">Anfang des Bereichs zum Durchsuchen möglicher Haltepunktpositionen in.</span><span class="sxs-lookup"><span data-stu-id="16a90-132">Start of range to search possible breakpoint locations in.</span></span> |  
| <span data-ttu-id="16a90-133">Aufhören</span><span class="sxs-lookup"><span data-stu-id="16a90-133">end</span></span> | [<span data-ttu-id="16a90-134">Ort</span><span class="sxs-lookup"><span data-stu-id="16a90-134">Location</span></span>](#location) | <span data-ttu-id="16a90-135">Ende des Bereichs, um mögliche Haltepunktpositionen in \(ohne\) zu durchsuchen.</span><span class="sxs-lookup"><span data-stu-id="16a90-135">End of range to search possible breakpoint locations in \(excluding\).</span></span>  <span data-ttu-id="16a90-136">Wenn nicht angegeben, wird das Ende der Skripts als Ende des Bereichs verwendet.</span><span class="sxs-lookup"><span data-stu-id="16a90-136">When not specified, end of scripts is used as end of range.</span></span> |  

| <span data-ttu-id="16a90-137">Gibt zurück</span><span class="sxs-lookup"><span data-stu-id="16a90-137">Returns</span></span> | <span data-ttu-id="16a90-138">Typ</span><span class="sxs-lookup"><span data-stu-id="16a90-138">Type</span></span> | <span data-ttu-id="16a90-139">Details</span><span class="sxs-lookup"><span data-stu-id="16a90-139">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="16a90-140">Speicherorte</span><span class="sxs-lookup"><span data-stu-id="16a90-140">locations</span></span> | [<span data-ttu-id="16a90-141">BreakLocation</span><span class="sxs-lookup"><span data-stu-id="16a90-141">BreakLocation</span></span>](#breaklocation) | <span data-ttu-id="16a90-142">Liste der möglichen Haltepunktpositionen.</span><span class="sxs-lookup"><span data-stu-id="16a90-142">List of the possible breakpoint locations.</span></span> |  

---  

### <a name="setbreakpointsactive"></a><span data-ttu-id="16a90-143">setBreakpointsActive</span><span class="sxs-lookup"><span data-stu-id="16a90-143">setBreakpointsActive</span></span>  

<span data-ttu-id="16a90-144">Aktiviert/deaktiviert alle Haltepunkte auf der Seite.</span><span class="sxs-lookup"><span data-stu-id="16a90-144">Activates / deactivates all breakpoints on the page.</span></span>  

| <span data-ttu-id="16a90-145">Parameter</span><span class="sxs-lookup"><span data-stu-id="16a90-145">Parameters</span></span> | <span data-ttu-id="16a90-146">Typ</span><span class="sxs-lookup"><span data-stu-id="16a90-146">Type</span></span> | <span data-ttu-id="16a90-147">Details</span><span class="sxs-lookup"><span data-stu-id="16a90-147">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="16a90-148">active</span><span class="sxs-lookup"><span data-stu-id="16a90-148">active</span></span> | `boolean` | <span data-ttu-id="16a90-149">Neuer Wert für den aktiven Zustand der Haltepunkte.</span><span class="sxs-lookup"><span data-stu-id="16a90-149">New value for breakpoints active state.</span></span> |  

---  

### <a name="setbreakpointbyurl"></a><span data-ttu-id="16a90-150">setBreakpointByUrl</span><span class="sxs-lookup"><span data-stu-id="16a90-150">setBreakpointByUrl</span></span>  

<span data-ttu-id="16a90-151">Legt den JavaScript-Haltepunkt an einem bestimmten Speicherort fest, der entweder durch URL oder URL regex angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="16a90-151">Sets JavaScript breakpoint at given location specified either by URL or URL regex.</span></span>  <span data-ttu-id="16a90-152">Sobald dieser Befehl ausgegeben wurde, werden für alle vorhandenen analysierten Skripts Haltepunkte aufgelöst und in der Eigenschaft `locations` zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="16a90-152">Once this command is issued, all existing parsed scripts will have breakpoints resolved and returned in `locations` property.</span></span>  <span data-ttu-id="16a90-153">Eine weitere übereinstimmende Skript-Analyse führt zu nachfolgenden `breakpointResolved` Ereignissen.</span><span class="sxs-lookup"><span data-stu-id="16a90-153">Further matching script parsing will result in subsequent `breakpointResolved` events issued.</span></span>  <span data-ttu-id="16a90-154">Dieser logische Haltepunkt überdauert seitenladen.</span><span class="sxs-lookup"><span data-stu-id="16a90-154">This logical breakpoint will survive page reloads.</span></span>  

| <span data-ttu-id="16a90-155">Parameter</span><span class="sxs-lookup"><span data-stu-id="16a90-155">Parameters</span></span> | <span data-ttu-id="16a90-156">Typ</span><span class="sxs-lookup"><span data-stu-id="16a90-156">Type</span></span> | <span data-ttu-id="16a90-157">Details</span><span class="sxs-lookup"><span data-stu-id="16a90-157">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="16a90-158">lineNumber</span><span class="sxs-lookup"><span data-stu-id="16a90-158">lineNumber</span></span> | `integer` | <span data-ttu-id="16a90-159">Zeilennummer zum Festlegen des Haltepunkts.</span><span class="sxs-lookup"><span data-stu-id="16a90-159">Line number to set breakpoint at.</span></span> |  
| <span data-ttu-id="16a90-160">url \(optional\)</span><span class="sxs-lookup"><span data-stu-id="16a90-160">url  \(optional\)</span></span> | `string` | <span data-ttu-id="16a90-161">URL der Ressourcen, auf die der Haltepunkt festgelegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="16a90-161">URL of the resources to set breakpoint on.</span></span> |  
| <span data-ttu-id="16a90-162">urlRegex \(optional\)</span><span class="sxs-lookup"><span data-stu-id="16a90-162">urlRegex  \(optional\)</span></span> | `string` | <span data-ttu-id="16a90-163">Regex-Muster für die URLs der Ressourcen zum Festlegen von Haltepunkten.</span><span class="sxs-lookup"><span data-stu-id="16a90-163">Regex pattern for the URLs of the resources to set breakpoints on.</span></span>  <span data-ttu-id="16a90-164">Entweder `url` oder muss angegeben `urlRegex` werden.</span><span class="sxs-lookup"><span data-stu-id="16a90-164">Either `url` or `urlRegex` must be specified.</span></span> |  
| <span data-ttu-id="16a90-165">columnNumber \(optional\)</span><span class="sxs-lookup"><span data-stu-id="16a90-165">columnNumber  \(optional\)</span></span> | `integer` | <span data-ttu-id="16a90-166">Offset in der Linie, um den Haltepunkt zu festlegen.</span><span class="sxs-lookup"><span data-stu-id="16a90-166">Offset in the line to set breakpoint at.</span></span> |  
| <span data-ttu-id="16a90-167">Bedingung \(optional\)</span><span class="sxs-lookup"><span data-stu-id="16a90-167">condition  \(optional\)</span></span> | `string` | <span data-ttu-id="16a90-168">Ausdruck, der als Haltepunktbedingung verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="16a90-168">Expression to use as a breakpoint condition.</span></span>  <span data-ttu-id="16a90-169">Wenn angegeben, wird der Debugger nur dann am Haltepunkt beendet, wenn dieser Ausdruck auf true ausgewertet wird.</span><span class="sxs-lookup"><span data-stu-id="16a90-169">When specified, debugger will only stop on the breakpoint if this expression evaluates to true.</span></span> |  

| <span data-ttu-id="16a90-170">Gibt zurück</span><span class="sxs-lookup"><span data-stu-id="16a90-170">Returns</span></span> | <span data-ttu-id="16a90-171">Typ</span><span class="sxs-lookup"><span data-stu-id="16a90-171">Type</span></span> | <span data-ttu-id="16a90-172">Details</span><span class="sxs-lookup"><span data-stu-id="16a90-172">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="16a90-173">breakpointId</span><span class="sxs-lookup"><span data-stu-id="16a90-173">breakpointId</span></span> | [<span data-ttu-id="16a90-174">BreakpointId</span><span class="sxs-lookup"><span data-stu-id="16a90-174">BreakpointId</span></span>](#breakpointid) | <span data-ttu-id="16a90-175">ID des erstellten Haltepunkts für weitere Referenz.</span><span class="sxs-lookup"><span data-stu-id="16a90-175">ID of the created breakpoint for further reference.</span></span> |  
| <span data-ttu-id="16a90-176">Speicherorte</span><span class="sxs-lookup"><span data-stu-id="16a90-176">locations</span></span> | [<span data-ttu-id="16a90-177">Location[]</span><span class="sxs-lookup"><span data-stu-id="16a90-177">Location[]</span></span>](#location) | <span data-ttu-id="16a90-178">Liste der Speicherorte, in die dieser Haltepunkt beim Hinzufügen aufgelöst wurde.</span><span class="sxs-lookup"><span data-stu-id="16a90-178">List of the locations this breakpoint resolved into upon addition.</span></span> |  

---  

### <a name="setbreakpoint"></a><span data-ttu-id="16a90-179">setBreakpoint</span><span class="sxs-lookup"><span data-stu-id="16a90-179">setBreakpoint</span></span>  

<span data-ttu-id="16a90-180">Legt den JavaScript-Haltepunkt an einem bestimmten Speicherort fest.</span><span class="sxs-lookup"><span data-stu-id="16a90-180">Sets JavaScript breakpoint at a given location.</span></span>  

| <span data-ttu-id="16a90-181">Parameter</span><span class="sxs-lookup"><span data-stu-id="16a90-181">Parameters</span></span> | <span data-ttu-id="16a90-182">Typ</span><span class="sxs-lookup"><span data-stu-id="16a90-182">Type</span></span> | <span data-ttu-id="16a90-183">Details</span><span class="sxs-lookup"><span data-stu-id="16a90-183">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="16a90-184">location</span><span class="sxs-lookup"><span data-stu-id="16a90-184">location</span></span> | [<span data-ttu-id="16a90-185">Ort</span><span class="sxs-lookup"><span data-stu-id="16a90-185">Location</span></span>](#location) | <span data-ttu-id="16a90-186">Speicherort zum Festlegen des Haltepunkts.</span><span class="sxs-lookup"><span data-stu-id="16a90-186">Location to set breakpoint in.</span></span> |  
| <span data-ttu-id="16a90-187">Bedingung \(optional\)</span><span class="sxs-lookup"><span data-stu-id="16a90-187">condition  \(optional\)</span></span> | `string` | <span data-ttu-id="16a90-188">Ausdruck, der als Haltepunktbedingung verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="16a90-188">Expression to use as a breakpoint condition.</span></span>  <span data-ttu-id="16a90-189">Wenn angegeben, wird der Debugger nur dann am Haltepunkt beendet, wenn dieser Ausdruck auf true ausgewertet wird.</span><span class="sxs-lookup"><span data-stu-id="16a90-189">When specified, debugger will only stop on the breakpoint if this expression evaluates to true.</span></span> |  

| <span data-ttu-id="16a90-190">Gibt zurück</span><span class="sxs-lookup"><span data-stu-id="16a90-190">Returns</span></span> | <span data-ttu-id="16a90-191">Typ</span><span class="sxs-lookup"><span data-stu-id="16a90-191">Type</span></span> | <span data-ttu-id="16a90-192">Details</span><span class="sxs-lookup"><span data-stu-id="16a90-192">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="16a90-193">breakpointId</span><span class="sxs-lookup"><span data-stu-id="16a90-193">breakpointId</span></span> | [<span data-ttu-id="16a90-194">BreakpointId</span><span class="sxs-lookup"><span data-stu-id="16a90-194">BreakpointId</span></span>](#breakpointid) | <span data-ttu-id="16a90-195">ID des erstellten Haltepunkts für weitere Referenz.</span><span class="sxs-lookup"><span data-stu-id="16a90-195">ID of the created breakpoint for further reference.</span></span> |  
| <span data-ttu-id="16a90-196">actualLocation</span><span class="sxs-lookup"><span data-stu-id="16a90-196">actualLocation</span></span> | [<span data-ttu-id="16a90-197">Ort</span><span class="sxs-lookup"><span data-stu-id="16a90-197">Location</span></span>](#location) | <span data-ttu-id="16a90-198">Speicherort, in den dieser Haltepunkt aufgelöst wurde.</span><span class="sxs-lookup"><span data-stu-id="16a90-198">Location this breakpoint resolved into.</span></span> |  

---  

### <a name="removebreakpoint"></a><span data-ttu-id="16a90-199">removeBreakpoint</span><span class="sxs-lookup"><span data-stu-id="16a90-199">removeBreakpoint</span></span>  

<span data-ttu-id="16a90-200">Entfernt den JavaScript-Haltepunkt.</span><span class="sxs-lookup"><span data-stu-id="16a90-200">Removes JavaScript breakpoint.</span></span>  

| <span data-ttu-id="16a90-201">Parameter</span><span class="sxs-lookup"><span data-stu-id="16a90-201">Parameters</span></span> | <span data-ttu-id="16a90-202">Typ</span><span class="sxs-lookup"><span data-stu-id="16a90-202">Type</span></span> | <span data-ttu-id="16a90-203">Details</span><span class="sxs-lookup"><span data-stu-id="16a90-203">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="16a90-204">breakpointId</span><span class="sxs-lookup"><span data-stu-id="16a90-204">breakpointId</span></span> | [<span data-ttu-id="16a90-205">BreakpointId</span><span class="sxs-lookup"><span data-stu-id="16a90-205">BreakpointId</span></span>](#breakpointid) | &nbsp; |  

---  

### <a name="stepover"></a><span data-ttu-id="16a90-206">stepOver</span><span class="sxs-lookup"><span data-stu-id="16a90-206">stepOver</span></span>  

<span data-ttu-id="16a90-207">Schritte über die Anweisung.</span><span class="sxs-lookup"><span data-stu-id="16a90-207">Steps over the statement.</span></span>  

&nbsp;  

---  

### <a name="stepinto"></a><span data-ttu-id="16a90-208">stepInto</span><span class="sxs-lookup"><span data-stu-id="16a90-208">stepInto</span></span>  

<span data-ttu-id="16a90-209">Schritte in den Funktionsaufruf.</span><span class="sxs-lookup"><span data-stu-id="16a90-209">Steps into the function call.</span></span>  

&nbsp;  

---  

### <a name="stepout"></a><span data-ttu-id="16a90-210">stepOut</span><span class="sxs-lookup"><span data-stu-id="16a90-210">stepOut</span></span>  

<span data-ttu-id="16a90-211">Tritt aus dem Funktionsaufruf aus.</span><span class="sxs-lookup"><span data-stu-id="16a90-211">Steps out of the function call.</span></span>  

&nbsp;  

---  

### <a name="pause"></a><span data-ttu-id="16a90-212">pause</span><span class="sxs-lookup"><span data-stu-id="16a90-212">pause</span></span>  

<span data-ttu-id="16a90-213">Stoppt bei der nächsten JavaScript-Anweisung.</span><span class="sxs-lookup"><span data-stu-id="16a90-213">Stops on the next JavaScript statement.</span></span>  

&nbsp;  

---  

### <a name="resume"></a><span data-ttu-id="16a90-214">resume</span><span class="sxs-lookup"><span data-stu-id="16a90-214">resume</span></span>  

<span data-ttu-id="16a90-215">Setzt die JavaScript-Ausführung fort.</span><span class="sxs-lookup"><span data-stu-id="16a90-215">Resumes JavaScript execution.</span></span>  

&nbsp;  

---  

### <a name="getscriptsource"></a><span data-ttu-id="16a90-216">getScriptSource</span><span class="sxs-lookup"><span data-stu-id="16a90-216">getScriptSource</span></span>  

<span data-ttu-id="16a90-217">Gibt die Quelle für das Skript mit der angegebenen ID zurück.</span><span class="sxs-lookup"><span data-stu-id="16a90-217">Returns source for the script with given ID.</span></span>  

| <span data-ttu-id="16a90-218">Parameter</span><span class="sxs-lookup"><span data-stu-id="16a90-218">Parameters</span></span> | <span data-ttu-id="16a90-219">Typ</span><span class="sxs-lookup"><span data-stu-id="16a90-219">Type</span></span> | <span data-ttu-id="16a90-220">Details</span><span class="sxs-lookup"><span data-stu-id="16a90-220">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="16a90-221">scriptId</span><span class="sxs-lookup"><span data-stu-id="16a90-221">scriptId</span></span> | [<span data-ttu-id="16a90-222">Runtime.ScriptId</span><span class="sxs-lookup"><span data-stu-id="16a90-222">Runtime.ScriptId</span></span>](./runtime.md#scriptid) | <span data-ttu-id="16a90-223">DIE ID des Skripts, für das Die Quelle erhalten werden soll.</span><span class="sxs-lookup"><span data-stu-id="16a90-223">ID of the script to get source for.</span></span> |  
| <span data-ttu-id="16a90-224">Gibt zurück</span><span class="sxs-lookup"><span data-stu-id="16a90-224">Returns</span></span> | <span data-ttu-id="16a90-225">Typ</span><span class="sxs-lookup"><span data-stu-id="16a90-225">Type</span></span> | <span data-ttu-id="16a90-226">Details</span><span class="sxs-lookup"><span data-stu-id="16a90-226">Details</span></span> |  
|<span data-ttu-id="16a90-227">:---</span><span class="sxs-lookup"><span data-stu-id="16a90-227">:---</span></span> |<span data-ttu-id="16a90-228">:---</span><span class="sxs-lookup"><span data-stu-id="16a90-228">:---</span></span> |<span data-ttu-id="16a90-229">:---</span><span class="sxs-lookup"><span data-stu-id="16a90-229">:---</span></span> |  
| <span data-ttu-id="16a90-230">scriptSource</span><span class="sxs-lookup"><span data-stu-id="16a90-230">scriptSource</span></span> | `string` | <span data-ttu-id="16a90-231">Skriptquelle.</span><span class="sxs-lookup"><span data-stu-id="16a90-231">Script source.</span></span> |  

---  

### <a name="setpauseonexceptions"></a><span data-ttu-id="16a90-232">setPauseOnExceptions</span><span class="sxs-lookup"><span data-stu-id="16a90-232">setPauseOnExceptions</span></span>  

<span data-ttu-id="16a90-233">Definiert pause on exceptions state.</span><span class="sxs-lookup"><span data-stu-id="16a90-233">Defines pause on exceptions state.</span></span>  <span data-ttu-id="16a90-234">Kann so festgelegt werden, dass alle Ausnahmen, nicht abgefangenen Ausnahmen oder keine Ausnahmen beendet werden.</span><span class="sxs-lookup"><span data-stu-id="16a90-234">Can be set to stop on all exceptions, uncaught exceptions or no exceptions.</span></span>  <span data-ttu-id="16a90-235">Die anfängliche Pause für den Ausnahmezustand ist `none` .</span><span class="sxs-lookup"><span data-stu-id="16a90-235">Initial pause on exceptions state is `none`.</span></span>  

| <span data-ttu-id="16a90-236">Parameter</span><span class="sxs-lookup"><span data-stu-id="16a90-236">Parameters</span></span> | <span data-ttu-id="16a90-237">Typ</span><span class="sxs-lookup"><span data-stu-id="16a90-237">Type</span></span> | <span data-ttu-id="16a90-238">Details</span><span class="sxs-lookup"><span data-stu-id="16a90-238">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="16a90-239">state</span><span class="sxs-lookup"><span data-stu-id="16a90-239">state</span></span> | `string` | <span data-ttu-id="16a90-240">Halten Sie den Ausnahmemodus an.</span><span class="sxs-lookup"><span data-stu-id="16a90-240">Pause on exceptions mode.</span></span>  <span data-ttu-id="16a90-241">Zulässige Werte:  `none` `uncaught` , und</span><span class="sxs-lookup"><span data-stu-id="16a90-241">Allowed values:  `none`, `uncaught`, and</span></span> `all` |  

---  

### <a name="evaluateoncallframe"></a><span data-ttu-id="16a90-242">evaluateOnCallFrame</span><span class="sxs-lookup"><span data-stu-id="16a90-242">evaluateOnCallFrame</span></span>  

<span data-ttu-id="16a90-243">Wertet Ausdruck für einen bestimmten Aufrufrahmen aus.</span><span class="sxs-lookup"><span data-stu-id="16a90-243">Evaluates expression on a given call frame.</span></span>  

| <span data-ttu-id="16a90-244">Parameter</span><span class="sxs-lookup"><span data-stu-id="16a90-244">Parameters</span></span> | <span data-ttu-id="16a90-245">Typ</span><span class="sxs-lookup"><span data-stu-id="16a90-245">Type</span></span> | <span data-ttu-id="16a90-246">Details</span><span class="sxs-lookup"><span data-stu-id="16a90-246">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="16a90-247">callFrameId</span><span class="sxs-lookup"><span data-stu-id="16a90-247">callFrameId</span></span> | [<span data-ttu-id="16a90-248">CallFrameId</span><span class="sxs-lookup"><span data-stu-id="16a90-248">CallFrameId</span></span>](#callframeid) | <span data-ttu-id="16a90-249">Anrufrahmen-ID, die ausgewertet werden soll.</span><span class="sxs-lookup"><span data-stu-id="16a90-249">Call frame identifier to evaluate on.</span></span> |  
| <span data-ttu-id="16a90-250">Ausdruck</span><span class="sxs-lookup"><span data-stu-id="16a90-250">expression</span></span> | `string` | <span data-ttu-id="16a90-251">Ausdruck, der ausgewertet werden soll.</span><span class="sxs-lookup"><span data-stu-id="16a90-251">Expression to evaluate.</span></span> |  
| <span data-ttu-id="16a90-252">Gibt zurück</span><span class="sxs-lookup"><span data-stu-id="16a90-252">Returns</span></span> | <span data-ttu-id="16a90-253">Typ</span><span class="sxs-lookup"><span data-stu-id="16a90-253">Type</span></span> | <span data-ttu-id="16a90-254">Details</span><span class="sxs-lookup"><span data-stu-id="16a90-254">Details</span></span> |  
|<span data-ttu-id="16a90-255">:---</span><span class="sxs-lookup"><span data-stu-id="16a90-255">:---</span></span> |<span data-ttu-id="16a90-256">:---</span><span class="sxs-lookup"><span data-stu-id="16a90-256">:---</span></span> |<span data-ttu-id="16a90-257">:---</span><span class="sxs-lookup"><span data-stu-id="16a90-257">:---</span></span> |  
| <span data-ttu-id="16a90-258">result</span><span class="sxs-lookup"><span data-stu-id="16a90-258">result</span></span> | [<span data-ttu-id="16a90-259">Runtime.RemoteObject</span><span class="sxs-lookup"><span data-stu-id="16a90-259">Runtime.RemoteObject</span></span>](./runtime.md#remoteobject) | <span data-ttu-id="16a90-260">Objektwrapper für das Auswertungsergebnis.</span><span class="sxs-lookup"><span data-stu-id="16a90-260">Object wrapper for the evaluation result.</span></span> |  

---  

### <a name="setvariablevalue"></a><span data-ttu-id="16a90-261">setVariableValue</span><span class="sxs-lookup"><span data-stu-id="16a90-261">setVariableValue</span></span>  

<span data-ttu-id="16a90-262">Ändert den Wert der Variablen in einem Callframe.</span><span class="sxs-lookup"><span data-stu-id="16a90-262">Changes value of variable in a callframe.</span></span>  <span data-ttu-id="16a90-263">Objektbasierte Bereiche werden nicht unterstützt und müssen manuell mutiert werden.</span><span class="sxs-lookup"><span data-stu-id="16a90-263">Object-based scopes are not supported and must be mutated manually.</span></span>  

| <span data-ttu-id="16a90-264">Parameter</span><span class="sxs-lookup"><span data-stu-id="16a90-264">Parameters</span></span> | <span data-ttu-id="16a90-265">Typ</span><span class="sxs-lookup"><span data-stu-id="16a90-265">Type</span></span> | <span data-ttu-id="16a90-266">Details</span><span class="sxs-lookup"><span data-stu-id="16a90-266">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="16a90-267">scopeNumber</span><span class="sxs-lookup"><span data-stu-id="16a90-267">scopeNumber</span></span> | `integer` | <span data-ttu-id="16a90-268">0-basierte Anzahl des Bereichs, wie in der Bereichskette aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="16a90-268">0-based number of scope as was listed in scope chain.</span></span>  <span data-ttu-id="16a90-269">Nur `local` , `closure` und `catch` Bereichstypen sind zulässig.</span><span class="sxs-lookup"><span data-stu-id="16a90-269">Only `local`, `closure`, and `catch` scope types are allowed.</span></span>  <span data-ttu-id="16a90-270">Andere Bereiche können manuell bearbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="16a90-270">Other scopes could be manipulated manually.</span></span> |  
| <span data-ttu-id="16a90-271">variableName</span><span class="sxs-lookup"><span data-stu-id="16a90-271">variableName</span></span> | `string` | <span data-ttu-id="16a90-272">Variabler Name.</span><span class="sxs-lookup"><span data-stu-id="16a90-272">Variable name.</span></span> |  
| <span data-ttu-id="16a90-273">newValue</span><span class="sxs-lookup"><span data-stu-id="16a90-273">newValue</span></span> | [<span data-ttu-id="16a90-274">Runtime.CallArgument</span><span class="sxs-lookup"><span data-stu-id="16a90-274">Runtime.CallArgument</span></span>](./runtime.md#callargument) | <span data-ttu-id="16a90-275">Neuer Variabler Wert.</span><span class="sxs-lookup"><span data-stu-id="16a90-275">New variable value.</span></span> |  
| <span data-ttu-id="16a90-276">callFrameId</span><span class="sxs-lookup"><span data-stu-id="16a90-276">callFrameId</span></span> | [<span data-ttu-id="16a90-277">CallFrameId</span><span class="sxs-lookup"><span data-stu-id="16a90-277">CallFrameId</span></span>](#callframeid) | <span data-ttu-id="16a90-278">ID des Callframes, der eine Variable enthält.</span><span class="sxs-lookup"><span data-stu-id="16a90-278">ID of callframe that holds variable.</span></span> |  

---  

### <a name="setblackboxpatterns"></a><span data-ttu-id="16a90-279">setBlackboxPatterns</span><span class="sxs-lookup"><span data-stu-id="16a90-279">setBlackboxPatterns</span></span>  

<span data-ttu-id="16a90-280">**Experimental**.</span><span class="sxs-lookup"><span data-stu-id="16a90-280">**Experimental**.</span></span>  <span data-ttu-id="16a90-281">Ersetzen Sie vorherige Blackboxmuster durch übergebene Muster.</span><span class="sxs-lookup"><span data-stu-id="16a90-281">Replace previous blackbox patterns with passed ones.</span></span>  <span data-ttu-id="16a90-282">Erzwingt das Back-End, das Schrittweise/Anhalten in Skripts zu überspringen, deren URL mit einem der Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="16a90-282">Forces backend to skip stepping/pausing in scripts with url matching one of the patterns.</span></span>  <span data-ttu-id="16a90-283">Der Debugger versucht, das blackboxed-Skript zu verlassen, indem er mehrere Male ausgeführt wird, und schließlich zu einem Fehler `step in` `step out` greifen.</span><span class="sxs-lookup"><span data-stu-id="16a90-283">The debugger will try to leave blackboxed script by performing `step in` several times, finally resorting to `step out` if unsuccessful.</span></span>  

| <span data-ttu-id="16a90-284">Parameter</span><span class="sxs-lookup"><span data-stu-id="16a90-284">Parameters</span></span> | <span data-ttu-id="16a90-285">Typ</span><span class="sxs-lookup"><span data-stu-id="16a90-285">Type</span></span> | <span data-ttu-id="16a90-286">Details</span><span class="sxs-lookup"><span data-stu-id="16a90-286">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="16a90-287">Muster</span><span class="sxs-lookup"><span data-stu-id="16a90-287">patterns</span></span> | `string[]` | <span data-ttu-id="16a90-288">Array von Regexps, das zum Überprüfen der Skript-URL auf den Blackboxstatus verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="16a90-288">Array of regexps that will be used to check script url for blackbox state.</span></span> |  

---  

### <a name="mssetdebuggerpropertyvalue"></a><span data-ttu-id="16a90-289">msSetDebuggerPropertyValue</span><span class="sxs-lookup"><span data-stu-id="16a90-289">msSetDebuggerPropertyValue</span></span>  

<span data-ttu-id="16a90-290">**Experimental**.</span><span class="sxs-lookup"><span data-stu-id="16a90-290">**Experimental**.</span></span>  <span data-ttu-id="16a90-291">Microsoft: Legt die angegebene Debuggereigenschaft auf den angegebenen Wert fest.</span><span class="sxs-lookup"><span data-stu-id="16a90-291">Microsoft:  Sets the specified debugger property to the specified value.</span></span>  

| <span data-ttu-id="16a90-292">Parameter</span><span class="sxs-lookup"><span data-stu-id="16a90-292">Parameters</span></span> | <span data-ttu-id="16a90-293">Typ</span><span class="sxs-lookup"><span data-stu-id="16a90-293">Type</span></span> | <span data-ttu-id="16a90-294">Details</span><span class="sxs-lookup"><span data-stu-id="16a90-294">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="16a90-295">debuggerPropertyId</span><span class="sxs-lookup"><span data-stu-id="16a90-295">debuggerPropertyId</span></span> | `string` | <span data-ttu-id="16a90-296">Microsoft: Die eigenschafts-ID \(d. h. msDebuggerPropertyId\), die festgelegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="16a90-296">Microsoft: The property ID \(i.e. msDebuggerPropertyId\) to set.</span></span> |  
| <span data-ttu-id="16a90-297">newValue</span><span class="sxs-lookup"><span data-stu-id="16a90-297">newValue</span></span> | `string` | &nbsp; |  

---  

## <a name="events"></a><span data-ttu-id="16a90-298">Veranstaltungen</span><span class="sxs-lookup"><span data-stu-id="16a90-298">Events</span></span>  

### <a name="scriptparsed"></a><span data-ttu-id="16a90-299">scriptParsed</span><span class="sxs-lookup"><span data-stu-id="16a90-299">scriptParsed</span></span>  

<span data-ttu-id="16a90-300">Wird ausgelöst, wenn das Skript analysiert wird.</span><span class="sxs-lookup"><span data-stu-id="16a90-300">Fired when the script is parsed.</span></span>  <span data-ttu-id="16a90-301">Dieses Ereignis wird auch für alle bekannten und nicht abgeholten Skripts beim Aktivieren des Debuggers ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="16a90-301">This event is also fired for all known and uncollected scripts upon enabling debugger.</span></span>  

| <span data-ttu-id="16a90-302">Parameter</span><span class="sxs-lookup"><span data-stu-id="16a90-302">Parameters</span></span> | <span data-ttu-id="16a90-303">Typ</span><span class="sxs-lookup"><span data-stu-id="16a90-303">Type</span></span> | <span data-ttu-id="16a90-304">Details</span><span class="sxs-lookup"><span data-stu-id="16a90-304">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="16a90-305">scriptId</span><span class="sxs-lookup"><span data-stu-id="16a90-305">scriptId</span></span> | [<span data-ttu-id="16a90-306">Runtime.ScriptId</span><span class="sxs-lookup"><span data-stu-id="16a90-306">Runtime.ScriptId</span></span>](./runtime.md#scriptid) | <span data-ttu-id="16a90-307">Bezeichner des analysierten Skripts.</span><span class="sxs-lookup"><span data-stu-id="16a90-307">Identifier of the script parsed.</span></span> |  
| <span data-ttu-id="16a90-308">URL</span><span class="sxs-lookup"><span data-stu-id="16a90-308">url</span></span> | `string` | <span data-ttu-id="16a90-309">URL oder Name des analysierten Skripts \(falls ein\).</span><span class="sxs-lookup"><span data-stu-id="16a90-309">URL or name of the script parsed \(if any\).</span></span> |  
| <span data-ttu-id="16a90-310">startLine</span><span class="sxs-lookup"><span data-stu-id="16a90-310">startLine</span></span> | `integer` | <span data-ttu-id="16a90-311">Zeilenversatz des Skripts innerhalb der Ressource mit der angegebenen URL \(für Skripttags\).</span><span class="sxs-lookup"><span data-stu-id="16a90-311">Line offset of the script within the resource with given URL \(for script tags\).</span></span> |  
| <span data-ttu-id="16a90-312">startColumn</span><span class="sxs-lookup"><span data-stu-id="16a90-312">startColumn</span></span> | `integer` | <span data-ttu-id="16a90-313">Spaltenversatz des Skripts innerhalb der Ressource mit einer angegebenen URL.</span><span class="sxs-lookup"><span data-stu-id="16a90-313">Column offset of the script within the resource with given URL.</span></span> |  
| <span data-ttu-id="16a90-314">endLine</span><span class="sxs-lookup"><span data-stu-id="16a90-314">endLine</span></span> | `integer` | <span data-ttu-id="16a90-315">Letzte Zeile des Skripts.</span><span class="sxs-lookup"><span data-stu-id="16a90-315">Last line of the script.</span></span> |  
| <span data-ttu-id="16a90-316">endColumn</span><span class="sxs-lookup"><span data-stu-id="16a90-316">endColumn</span></span> | `integer` | <span data-ttu-id="16a90-317">Länge der letzten Zeile des Skripts.</span><span class="sxs-lookup"><span data-stu-id="16a90-317">Length of the last line of the script.</span></span> |  
| <span data-ttu-id="16a90-318">executionContextId</span><span class="sxs-lookup"><span data-stu-id="16a90-318">executionContextId</span></span> | [<span data-ttu-id="16a90-319">Runtime.ExecutionContextId</span><span class="sxs-lookup"><span data-stu-id="16a90-319">Runtime.ExecutionContextId</span></span>](./runtime.md#executioncontextid) | <span data-ttu-id="16a90-320">Gibt den Kontext für die Skripterstellung an.</span><span class="sxs-lookup"><span data-stu-id="16a90-320">Specifies script creation context.</span></span> |  
| <span data-ttu-id="16a90-321">sourceMapURL \(optional\)</span><span class="sxs-lookup"><span data-stu-id="16a90-321">sourceMapURL  \(optional\)</span></span> | `string` | <span data-ttu-id="16a90-322">URL der Quellzuordnung, die dem Skript zugeordnet ist (falls eine).</span><span class="sxs-lookup"><span data-stu-id="16a90-322">URL of source map associated with script (if any).</span></span> |  
| <span data-ttu-id="16a90-323">length \(optional\)</span><span class="sxs-lookup"><span data-stu-id="16a90-323">length  \(optional\)</span></span> | `integer` | <span data-ttu-id="16a90-324">**Experimental**.</span><span class="sxs-lookup"><span data-stu-id="16a90-324">**Experimental**.</span></span>  <span data-ttu-id="16a90-325">Diese Skriptlänge.</span><span class="sxs-lookup"><span data-stu-id="16a90-325">This script length.</span></span> |  
| <span data-ttu-id="16a90-326">msParentId \(optional\)</span><span class="sxs-lookup"><span data-stu-id="16a90-326">msParentId  \(optional\)</span></span> | `string` | <span data-ttu-id="16a90-327">**Experimental**.</span><span class="sxs-lookup"><span data-stu-id="16a90-327">**Experimental**.</span></span>  <span data-ttu-id="16a90-328">Dies ist die übergeordnete Dokument-ID.</span><span class="sxs-lookup"><span data-stu-id="16a90-328">This is the parent document ID.</span></span> |  
| <span data-ttu-id="16a90-329">msMimeType \(optional\)</span><span class="sxs-lookup"><span data-stu-id="16a90-329">msMimeType  \(optional\)</span></span> | `string` | <span data-ttu-id="16a90-330">**Experimental**.</span><span class="sxs-lookup"><span data-stu-id="16a90-330">**Experimental**.</span></span>  <span data-ttu-id="16a90-331">Dies ist der Mimetyp.</span><span class="sxs-lookup"><span data-stu-id="16a90-331">This is the mime type.</span></span> |  
| <span data-ttu-id="16a90-332">msIsDynamicCode \(optional\)</span><span class="sxs-lookup"><span data-stu-id="16a90-332">msIsDynamicCode  \(optional\)</span></span> | `boolean` | <span data-ttu-id="16a90-333">**Experimental**.</span><span class="sxs-lookup"><span data-stu-id="16a90-333">**Experimental**.</span></span>  <span data-ttu-id="16a90-334">Dies gibt an, ob es sich um dynamischen Code handelt.</span><span class="sxs-lookup"><span data-stu-id="16a90-334">This indicates whether it is dynamic code.</span></span> |  
| <span data-ttu-id="16a90-335">msLongDocumentId \(optional\)</span><span class="sxs-lookup"><span data-stu-id="16a90-335">msLongDocumentId  \(optional\)</span></span> | `integer` | <span data-ttu-id="16a90-336">**Experimental**.</span><span class="sxs-lookup"><span data-stu-id="16a90-336">**Experimental**.</span></span>  <span data-ttu-id="16a90-337">Dies ist die lange Dokument-ID.</span><span class="sxs-lookup"><span data-stu-id="16a90-337">This is the long document ID.</span></span> |  

---  

### <a name="breakpointresolved"></a><span data-ttu-id="16a90-338">breakpointResolved</span><span class="sxs-lookup"><span data-stu-id="16a90-338">breakpointResolved</span></span>  

<span data-ttu-id="16a90-339">Wird ausgelöst, wenn der Haltepunkt in ein tatsächliches Skript und einen tatsächlichen Speicherort aufgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="16a90-339">Fired when breakpoint is resolved to an actual script and location.</span></span>  

| <span data-ttu-id="16a90-340">Parameter</span><span class="sxs-lookup"><span data-stu-id="16a90-340">Parameters</span></span> | <span data-ttu-id="16a90-341">Typ</span><span class="sxs-lookup"><span data-stu-id="16a90-341">Type</span></span> | <span data-ttu-id="16a90-342">Details</span><span class="sxs-lookup"><span data-stu-id="16a90-342">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="16a90-343">breakpointId</span><span class="sxs-lookup"><span data-stu-id="16a90-343">breakpointId</span></span> | [<span data-ttu-id="16a90-344">BreakpointId</span><span class="sxs-lookup"><span data-stu-id="16a90-344">BreakpointId</span></span>](#breakpointid) | <span data-ttu-id="16a90-345">Eindeutiger Bezeichner des Haltepunkts.</span><span class="sxs-lookup"><span data-stu-id="16a90-345">Breakpoint unique identifier.</span></span> |  
| <span data-ttu-id="16a90-346">location</span><span class="sxs-lookup"><span data-stu-id="16a90-346">location</span></span> | [<span data-ttu-id="16a90-347">Ort</span><span class="sxs-lookup"><span data-stu-id="16a90-347">Location</span></span>](#location) | <span data-ttu-id="16a90-348">Tatsächliche Haltepunktposition.</span><span class="sxs-lookup"><span data-stu-id="16a90-348">Actual breakpoint location.</span></span> |  
| <span data-ttu-id="16a90-349">msLength \(optional\)</span><span class="sxs-lookup"><span data-stu-id="16a90-349">msLength  \(optional\)</span></span> | `integer` | <span data-ttu-id="16a90-350">**Experimental**.</span><span class="sxs-lookup"><span data-stu-id="16a90-350">**Experimental**.</span></span>  <span data-ttu-id="16a90-351">Microsoft: Länge des Codes \(d. h. Anzahl der Zeichen\) am Haltepunktspeicherort.</span><span class="sxs-lookup"><span data-stu-id="16a90-351">Microsoft:  Length of code \(i.e. number of characters\) at the breakpoint location.</span></span> |  

---  

### <a name="paused"></a><span data-ttu-id="16a90-352">angehalten</span><span class="sxs-lookup"><span data-stu-id="16a90-352">paused</span></span>  

<span data-ttu-id="16a90-353">Wird ausgelöst, wenn der Debugger für einen Haltepunkt oder eine Ausnahme umbricht.</span><span class="sxs-lookup"><span data-stu-id="16a90-353">Fired when the debuggers breaks for a breakpoint or exception.</span></span>  

| <span data-ttu-id="16a90-354">Parameter</span><span class="sxs-lookup"><span data-stu-id="16a90-354">Parameters</span></span> | <span data-ttu-id="16a90-355">Typ</span><span class="sxs-lookup"><span data-stu-id="16a90-355">Type</span></span> | <span data-ttu-id="16a90-356">Details</span><span class="sxs-lookup"><span data-stu-id="16a90-356">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="16a90-357">callFrames</span><span class="sxs-lookup"><span data-stu-id="16a90-357">callFrames</span></span> | [<span data-ttu-id="16a90-358">CallFrame[]</span><span class="sxs-lookup"><span data-stu-id="16a90-358">CallFrame[]</span></span>](#callframe) | <span data-ttu-id="16a90-359">Aufrufstapel, auf dem der Debugger beendet wurde.</span><span class="sxs-lookup"><span data-stu-id="16a90-359">Call stack the debugger stopped on.</span></span> |  
| <span data-ttu-id="16a90-360">reason</span><span class="sxs-lookup"><span data-stu-id="16a90-360">reason</span></span> | `string` | <span data-ttu-id="16a90-361">Grund anhalten.</span><span class="sxs-lookup"><span data-stu-id="16a90-361">Pause reason.</span></span>  <span data-ttu-id="16a90-362">Zulässige Werte:  `breakpoint` `step` , , , `exception` und</span><span class="sxs-lookup"><span data-stu-id="16a90-362">Allowed values:  `breakpoint`, `step`, `exception`, and</span></span> `other` |  
| <span data-ttu-id="16a90-363">data \(optional\)</span><span class="sxs-lookup"><span data-stu-id="16a90-363">data  \(optional\)</span></span> | `object` | <span data-ttu-id="16a90-364">Objekt mit unterbrechungsspezifischen Hilfseigenschaften.</span><span class="sxs-lookup"><span data-stu-id="16a90-364">Object containing break-specific auxiliary properties.</span></span> |  
| <span data-ttu-id="16a90-365">hitBreakpoints \(optional\)</span><span class="sxs-lookup"><span data-stu-id="16a90-365">hitBreakpoints  \(optional\)</span></span> | `string[]` | <span data-ttu-id="16a90-366">Hit breakpoints IDs</span><span class="sxs-lookup"><span data-stu-id="16a90-366">Hit breakpoints IDs</span></span> |  

---  

### <a name="resumed"></a><span data-ttu-id="16a90-367">fortgesetzt</span><span class="sxs-lookup"><span data-stu-id="16a90-367">resumed</span></span>  

<span data-ttu-id="16a90-368">Wird ausgelöst, wenn der Debugger die Ausführung wieder auf sich nimmt.</span><span class="sxs-lookup"><span data-stu-id="16a90-368">Fired when the debugger resumes execution.</span></span>  

&nbsp;  

---  

## <a name="types"></a><span data-ttu-id="16a90-369">Typen</span><span class="sxs-lookup"><span data-stu-id="16a90-369">Types</span></span>  

### <a name="breakpointid-string"></a><span data-ttu-id="16a90-370">BreakpointId-Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="16a90-370">BreakpointId string</span></span>  

<a name="breakpointid"></a>  

<span data-ttu-id="16a90-371">Haltepunkt-ID.</span><span class="sxs-lookup"><span data-stu-id="16a90-371">Breakpoint identifier.</span></span>  

&nbsp;  

---  

### <a name="callframeid-string"></a><span data-ttu-id="16a90-372">CallFrameId-Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="16a90-372">CallFrameId string</span></span>  

<a name="callframeid"></a>  

<span data-ttu-id="16a90-373">Anrufrahmen-ID.</span><span class="sxs-lookup"><span data-stu-id="16a90-373">Call frame identifier.</span></span>  

&nbsp;  

---  

### <a name="location-object"></a><span data-ttu-id="16a90-374">Location-Objekt</span><span class="sxs-lookup"><span data-stu-id="16a90-374">Location object</span></span>  

<a name="location"></a>  

<span data-ttu-id="16a90-375">Speicherort im Quellcode.</span><span class="sxs-lookup"><span data-stu-id="16a90-375">Location in the source code.</span></span>  

| <span data-ttu-id="16a90-376">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="16a90-376">Properties</span></span> | <span data-ttu-id="16a90-377">Typ</span><span class="sxs-lookup"><span data-stu-id="16a90-377">Type</span></span> | <span data-ttu-id="16a90-378">Details</span><span class="sxs-lookup"><span data-stu-id="16a90-378">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="16a90-379">scriptId</span><span class="sxs-lookup"><span data-stu-id="16a90-379">scriptId</span></span> | [<span data-ttu-id="16a90-380">Runtime.ScriptId</span><span class="sxs-lookup"><span data-stu-id="16a90-380">Runtime.ScriptId</span></span>](./runtime.md#scriptid) | <span data-ttu-id="16a90-381">Skript-ID, wie in der `Debugger.scriptParsed` angegeben.</span><span class="sxs-lookup"><span data-stu-id="16a90-381">Script identifier as reported in the `Debugger.scriptParsed`.</span></span> |  
| <span data-ttu-id="16a90-382">lineNumber</span><span class="sxs-lookup"><span data-stu-id="16a90-382">lineNumber</span></span> | `integer` | <span data-ttu-id="16a90-383">Zeilennummer im Skript \(0-basiert\).</span><span class="sxs-lookup"><span data-stu-id="16a90-383">Line number in the script \(0-based\).</span></span> |  
| <span data-ttu-id="16a90-384">columnNumber \(optional\)</span><span class="sxs-lookup"><span data-stu-id="16a90-384">columnNumber  \(optional\)</span></span> | `integer` | <span data-ttu-id="16a90-385">Spaltennummer im Skript \(0-basiert\).</span><span class="sxs-lookup"><span data-stu-id="16a90-385">Column number in the script \(0-based\).</span></span> |  
| <span data-ttu-id="16a90-386">msLength</span><span class="sxs-lookup"><span data-stu-id="16a90-386">msLength</span></span> | `integer` | <span data-ttu-id="16a90-387">Microsoft: Länge des Codes \(d. h. Anzahl der Zeichen\) in diesem Aufrufrahmen.</span><span class="sxs-lookup"><span data-stu-id="16a90-387">Microsoft: Length of code \(i.e. number of characters\) at this call frame.</span></span> |  

---  

### <a name="breaklocation-object"></a><span data-ttu-id="16a90-388">BreakLocation-Objekt</span><span class="sxs-lookup"><span data-stu-id="16a90-388">BreakLocation object</span></span>  

<a name="breaklocation"></a>  

<span data-ttu-id="16a90-389">Speicherort im Quellcode umbrechen.</span><span class="sxs-lookup"><span data-stu-id="16a90-389">Break location in the source code.</span></span>  

| <span data-ttu-id="16a90-390">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="16a90-390">Properties</span></span> | <span data-ttu-id="16a90-391">Typ</span><span class="sxs-lookup"><span data-stu-id="16a90-391">Type</span></span> | <span data-ttu-id="16a90-392">Details</span><span class="sxs-lookup"><span data-stu-id="16a90-392">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="16a90-393">scriptId</span><span class="sxs-lookup"><span data-stu-id="16a90-393">scriptId</span></span> | [<span data-ttu-id="16a90-394">Runtime.ScriptId</span><span class="sxs-lookup"><span data-stu-id="16a90-394">Runtime.ScriptId</span></span>](./runtime.md#scriptid) | <span data-ttu-id="16a90-395">Skript-ID, wie in der `Debugger.scriptParsed` angegeben.</span><span class="sxs-lookup"><span data-stu-id="16a90-395">Script identifier as reported in the `Debugger.scriptParsed`.</span></span> |  
| <span data-ttu-id="16a90-396">lineNumber</span><span class="sxs-lookup"><span data-stu-id="16a90-396">lineNumber</span></span> | `integer` | <span data-ttu-id="16a90-397">Zeilennummer im Skript \(0-basiert\).</span><span class="sxs-lookup"><span data-stu-id="16a90-397">Line number in the script \(0-based\).</span></span> |  
| <span data-ttu-id="16a90-398">columnNumber \(optional\)</span><span class="sxs-lookup"><span data-stu-id="16a90-398">columnNumber  \(optional\)</span></span> | `integer` | <span data-ttu-id="16a90-399">Spaltennummer im Skript \(0-basiert\).</span><span class="sxs-lookup"><span data-stu-id="16a90-399">Column number in the script \(0-based\).</span></span> |  
| <span data-ttu-id="16a90-400">msLength</span><span class="sxs-lookup"><span data-stu-id="16a90-400">msLength</span></span> | `integer` | <span data-ttu-id="16a90-401">Microsoft: Länge des Codes \(d. h. Anzahl der Zeichen\) in diesem Aufrufrahmen.</span><span class="sxs-lookup"><span data-stu-id="16a90-401">Microsoft:  Length of code \(i.e. number of characters\) at this call frame.</span></span> |  
| <span data-ttu-id="16a90-402">Typ \(optional\)</span><span class="sxs-lookup"><span data-stu-id="16a90-402">type  \(optional\)</span></span> | `string` | <span data-ttu-id="16a90-403">Zulässige Werte:  `debuggerStatement` `call` , und</span><span class="sxs-lookup"><span data-stu-id="16a90-403">Allowed values:  `debuggerStatement`, `call`, and</span></span> `return` |  

---  

### <a name="callframe-object"></a><span data-ttu-id="16a90-404">CallFrame-Objekt</span><span class="sxs-lookup"><span data-stu-id="16a90-404">CallFrame object</span></span>  

<a name="callframe"></a>  

<span data-ttu-id="16a90-405">JavaScript-Aufrufrahmen.</span><span class="sxs-lookup"><span data-stu-id="16a90-405">JavaScript call frame.</span></span>  <span data-ttu-id="16a90-406">Array von Anrufframes bilden die Aufrufliste.</span><span class="sxs-lookup"><span data-stu-id="16a90-406">Array of call frames form the call stack.</span></span>  

| <span data-ttu-id="16a90-407">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="16a90-407">Properties</span></span> | <span data-ttu-id="16a90-408">Typ</span><span class="sxs-lookup"><span data-stu-id="16a90-408">Type</span></span> | <span data-ttu-id="16a90-409">Details</span><span class="sxs-lookup"><span data-stu-id="16a90-409">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="16a90-410">callFrameId</span><span class="sxs-lookup"><span data-stu-id="16a90-410">callFrameId</span></span> | [<span data-ttu-id="16a90-411">CallFrameId</span><span class="sxs-lookup"><span data-stu-id="16a90-411">CallFrameId</span></span>](#callframeid) | <span data-ttu-id="16a90-412">Anrufrahmen-ID.</span><span class="sxs-lookup"><span data-stu-id="16a90-412">Call frame identifier.</span></span>  <span data-ttu-id="16a90-413">Dieser Bezeichner ist nur gültig, wenn der Debugger angehalten wird.</span><span class="sxs-lookup"><span data-stu-id="16a90-413">This identifier is only valid while the debugger is paused.</span></span> |  
| <span data-ttu-id="16a90-414">functionName</span><span class="sxs-lookup"><span data-stu-id="16a90-414">functionName</span></span> | `string` | <span data-ttu-id="16a90-415">Name der für diesen Aufrufrahmen aufgerufenen JavaScript-Funktion.</span><span class="sxs-lookup"><span data-stu-id="16a90-415">Name of the JavaScript function called on this call frame.</span></span> |  
| <span data-ttu-id="16a90-416">functionLocation \(optional\)</span><span class="sxs-lookup"><span data-stu-id="16a90-416">functionLocation  \(optional\)</span></span> | [<span data-ttu-id="16a90-417">Ort</span><span class="sxs-lookup"><span data-stu-id="16a90-417">Location</span></span>](#location) | <span data-ttu-id="16a90-418">**Experimental**.</span><span class="sxs-lookup"><span data-stu-id="16a90-418">**Experimental**.</span></span>  <span data-ttu-id="16a90-419">Speicherort im Quellcode.</span><span class="sxs-lookup"><span data-stu-id="16a90-419">Location in the source code.</span></span> |  
| <span data-ttu-id="16a90-420">location</span><span class="sxs-lookup"><span data-stu-id="16a90-420">location</span></span> | [<span data-ttu-id="16a90-421">Ort</span><span class="sxs-lookup"><span data-stu-id="16a90-421">Location</span></span>](#location) | <span data-ttu-id="16a90-422">Speicherort im Quellcode.</span><span class="sxs-lookup"><span data-stu-id="16a90-422">Location in the source code.</span></span> |  
| <span data-ttu-id="16a90-423">URL</span><span class="sxs-lookup"><span data-stu-id="16a90-423">url</span></span> | `string` | <span data-ttu-id="16a90-424">Name oder URL des JavaScript-Skripts.</span><span class="sxs-lookup"><span data-stu-id="16a90-424">JavaScript script name or url.</span></span> |  
| <span data-ttu-id="16a90-425">scopeChain</span><span class="sxs-lookup"><span data-stu-id="16a90-425">scopeChain</span></span> | [<span data-ttu-id="16a90-426">Scope[]</span><span class="sxs-lookup"><span data-stu-id="16a90-426">Scope[]</span></span>](#scope) | <span data-ttu-id="16a90-427">Bereichskette für diesen Anrufrahmen.</span><span class="sxs-lookup"><span data-stu-id="16a90-427">Scope chain for this call frame.</span></span> |  
| <span data-ttu-id="16a90-428">this</span><span class="sxs-lookup"><span data-stu-id="16a90-428">this</span></span> | [<span data-ttu-id="16a90-429">Runtime.RemoteObject</span><span class="sxs-lookup"><span data-stu-id="16a90-429">Runtime.RemoteObject</span></span>](./runtime.md#remoteobject) | `this` <span data-ttu-id="16a90-430">-Objekt für diesen Aufrufrahmen.</span><span class="sxs-lookup"><span data-stu-id="16a90-430">object for this call frame.</span></span> |  
| <span data-ttu-id="16a90-431">returnValue \(optional\)</span><span class="sxs-lookup"><span data-stu-id="16a90-431">returnValue  \(optional\)</span></span> | [<span data-ttu-id="16a90-432">Runtime.RemoteObject</span><span class="sxs-lookup"><span data-stu-id="16a90-432">Runtime.RemoteObject</span></span>](./runtime.md#remoteobject) | <span data-ttu-id="16a90-433">Der zurückgegebene Wert, wenn sich die Funktion am Rückgabepunkt befindet.</span><span class="sxs-lookup"><span data-stu-id="16a90-433">The value being returned, if the function is at return point.</span></span> |  

---  

### <a name="scope-object"></a><span data-ttu-id="16a90-434">Scope-Objekt</span><span class="sxs-lookup"><span data-stu-id="16a90-434">Scope object</span></span>  

<a name="scope"></a>  

<span data-ttu-id="16a90-435">Bereichsbeschreibung.</span><span class="sxs-lookup"><span data-stu-id="16a90-435">Scope description.</span></span>  

| <span data-ttu-id="16a90-436">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="16a90-436">Properties</span></span> | <span data-ttu-id="16a90-437">Typ</span><span class="sxs-lookup"><span data-stu-id="16a90-437">Type</span></span> | <span data-ttu-id="16a90-438">Details</span><span class="sxs-lookup"><span data-stu-id="16a90-438">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="16a90-439">Typ</span><span class="sxs-lookup"><span data-stu-id="16a90-439">type</span></span> | `string` | <span data-ttu-id="16a90-440">Bereichstyp.</span><span class="sxs-lookup"><span data-stu-id="16a90-440">Scope type.</span></span>  <span data-ttu-id="16a90-441">Zulässige Werte:  `global` , , , , , , `local` , `with` `closure` `catch` `block` `script` `eval` und</span><span class="sxs-lookup"><span data-stu-id="16a90-441">Allowed values:  `global`, `local`, `with`, `closure`, `catch`, `block`, `script`, `eval`, and</span></span> `module` |  
| <span data-ttu-id="16a90-442">Objekt</span><span class="sxs-lookup"><span data-stu-id="16a90-442">object</span></span> | [<span data-ttu-id="16a90-443">Runtime.RemoteObject</span><span class="sxs-lookup"><span data-stu-id="16a90-443">Runtime.RemoteObject</span></span>](./runtime.md#remoteobject) | <span data-ttu-id="16a90-444">Objekt, das den Bereich darstellt.</span><span class="sxs-lookup"><span data-stu-id="16a90-444">Object representing the scope.</span></span>  <span data-ttu-id="16a90-445">Für und Bereiche stellt sie das tatsächliche Objekt dar. Für die restlichen Bereiche ist es ein künstliches transientes Objekt, das Bereichsvariablen als `global` `with` Eigenschaften aufzählt.</span><span class="sxs-lookup"><span data-stu-id="16a90-445">For `global` and `with` scopes it represents the actual object; for the rest of the scopes, it is artificial transient object enumerating scope variables as its properties.</span></span> |  
| <span data-ttu-id="16a90-446">Name \(optional\)</span><span class="sxs-lookup"><span data-stu-id="16a90-446">name  \(optional\)</span></span> | `string` | &nbsp; |  
| <span data-ttu-id="16a90-447">startLocation \(optional\)</span><span class="sxs-lookup"><span data-stu-id="16a90-447">startLocation  \(optional\)</span></span> | [<span data-ttu-id="16a90-448">Ort</span><span class="sxs-lookup"><span data-stu-id="16a90-448">Location</span></span>](#location) | <span data-ttu-id="16a90-449">Speicherort im Quellcode, an dem der Bereich beginnt.</span><span class="sxs-lookup"><span data-stu-id="16a90-449">Location in the source code where scope starts.</span></span> |  
| <span data-ttu-id="16a90-450">endLocation \(optional\)</span><span class="sxs-lookup"><span data-stu-id="16a90-450">endLocation  \(optional\)</span></span> | [<span data-ttu-id="16a90-451">Ort</span><span class="sxs-lookup"><span data-stu-id="16a90-451">Location</span></span>](#location) | <span data-ttu-id="16a90-452">Speicherort im Quellcode, an dem der Bereich endet.</span><span class="sxs-lookup"><span data-stu-id="16a90-452">Location in the source code where scope ends.</span></span> |  

---  

## <a name="dependencies"></a><span data-ttu-id="16a90-453">Abhängigkeiten</span><span class="sxs-lookup"><span data-stu-id="16a90-453">Dependencies</span></span>  

[<span data-ttu-id="16a90-454">Laufzeit</span><span class="sxs-lookup"><span data-stu-id="16a90-454">Runtime</span></span>](./runtime.md)  
