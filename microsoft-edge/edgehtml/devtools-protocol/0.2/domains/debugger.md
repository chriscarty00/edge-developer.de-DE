---
description: DevTools Protocol Version 0.2 (EdgeHTML)-Referenz für die Debuggerdomäne. Die Debuggerdomäne macht JavaScript-Debuggingfunktionen verfügbar. Es ermöglicht das Festlegen und Entfernen von Haltepunkten, das Schrittweise Durchbrechen der Ausführung, das Untersuchen von Stapelverfolgungen usw.
title: Debuggerdomäne – DevTools Protocol Version 0.2 (EdgeHTML)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/03/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.custom: seodec18
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 00c410812edd4d11e9904a489955e7fd218a7e5d
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398175"
---
# <a name="debugger-domain---devtools-protocol-version-02-edgehtml"></a><span data-ttu-id="51d98-105">Debuggerdomäne – DevTools Protocol Version 0.2 (EdgeHTML)</span><span class="sxs-lookup"><span data-stu-id="51d98-105">Debugger Domain - DevTools Protocol Version 0.2 (EdgeHTML)</span></span>  

<span data-ttu-id="51d98-106">Die Debuggerdomäne macht JavaScript-Debuggingfunktionen verfügbar.</span><span class="sxs-lookup"><span data-stu-id="51d98-106">Debugger domain exposes JavaScript debugging capabilities.</span></span> <span data-ttu-id="51d98-107">Es ermöglicht das Festlegen und Entfernen von Haltepunkten, das Schrittweise Durchbrechen der Ausführung, das Untersuchen von Stapelverfolgungen usw.</span><span class="sxs-lookup"><span data-stu-id="51d98-107">It allows setting and removing breakpoints, stepping through execution, exploring stack traces, etc.</span></span>

| <span data-ttu-id="51d98-108">Klassifizierung</span><span class="sxs-lookup"><span data-stu-id="51d98-108">Classification</span></span> | <span data-ttu-id="51d98-109">Member</span><span class="sxs-lookup"><span data-stu-id="51d98-109">Members</span></span> |  
|:--- |:--- |  
| [**<span data-ttu-id="51d98-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="51d98-110">Methods</span></span>**](#methods) | <span data-ttu-id="51d98-111">[enable](#enable), [disable](#disable), [getPossibleBreakpoints](#getpossiblebreakpoints), [setBreakpointsActive](#setbreakpointsactive), [setBreakpointByUrl](#setbreakpointbyurl), [setBreakpoint](#setbreakpoint), [removeBreakpoint](#removebreakpoint), [stepOver](#stepover), [stepInto](#stepinto), [stepOut](#stepout), [pause](#pause), [resume](#resume), [getScriptSource](#getscriptsource), [setPauseOnExceptions](#setpauseonexceptions), [evaluateOnCallFrame](#evaluateoncallframe), [setVariableValue](#setvariablevalue), [setBlackboxPatterns](#setblackboxpatterns), [msSetDebuggerPropertyValue](#mssetdebuggerpropertyvalue)</span><span class="sxs-lookup"><span data-stu-id="51d98-111">[enable](#enable), [disable](#disable), [getPossibleBreakpoints](#getpossiblebreakpoints), [setBreakpointsActive](#setbreakpointsactive), [setBreakpointByUrl](#setbreakpointbyurl), [setBreakpoint](#setbreakpoint), [removeBreakpoint](#removebreakpoint), [stepOver](#stepover), [stepInto](#stepinto), [stepOut](#stepout), [pause](#pause), [resume](#resume), [getScriptSource](#getscriptsource), [setPauseOnExceptions](#setpauseonexceptions), [evaluateOnCallFrame](#evaluateoncallframe), [setVariableValue](#setvariablevalue), [setBlackboxPatterns](#setblackboxpatterns), [msSetDebuggerPropertyValue](#mssetdebuggerpropertyvalue)</span></span> |  
| [**<span data-ttu-id="51d98-112">Veranstaltungen</span><span class="sxs-lookup"><span data-stu-id="51d98-112">Events</span></span>**](#events) | <span data-ttu-id="51d98-113">[scriptParsed](#scriptparsed), [breakpointResolved](#breakpointresolved), [paused](#paused), [resumed](#resumed)</span><span class="sxs-lookup"><span data-stu-id="51d98-113">[scriptParsed](#scriptparsed), [breakpointResolved](#breakpointresolved), [paused](#paused), [resumed](#resumed)</span></span> |  
| [**<span data-ttu-id="51d98-114">Typen</span><span class="sxs-lookup"><span data-stu-id="51d98-114">Types</span></span>**](#types) | <span data-ttu-id="51d98-115">[BreakpointId](#breakpointid), [CallFrameId](#callframeid), [Location](#location), [BreakLocation](#breaklocation), [CallFrame](#callframe), [Scope](#scope)</span><span class="sxs-lookup"><span data-stu-id="51d98-115">[BreakpointId](#breakpointid), [CallFrameId](#callframeid), [Location](#location), [BreakLocation](#breaklocation), [CallFrame](#callframe), [Scope](#scope)</span></span> |  
| [**<span data-ttu-id="51d98-116">Abhängigkeiten</span><span class="sxs-lookup"><span data-stu-id="51d98-116">Dependencies</span></span>**](#dependencies) | [<span data-ttu-id="51d98-117">Laufzeit</span><span class="sxs-lookup"><span data-stu-id="51d98-117">Runtime</span></span>](./runtime.md) |  

## <a name="methods"></a><span data-ttu-id="51d98-118">Methoden</span><span class="sxs-lookup"><span data-stu-id="51d98-118">Methods</span></span>  

### <a name="enable"></a><span data-ttu-id="51d98-119">Aktivieren</span><span class="sxs-lookup"><span data-stu-id="51d98-119">enable</span></span>  

<span data-ttu-id="51d98-120">Aktiviert den Debugger für die angegebene Seite.</span><span class="sxs-lookup"><span data-stu-id="51d98-120">Enables debugger for the given page.</span></span> <span data-ttu-id="51d98-121">Clients sollten nicht davon ausgehen, dass das Debuggen aktiviert wurde, bis das Ergebnis für diesen Befehl empfangen wurde.</span><span class="sxs-lookup"><span data-stu-id="51d98-121">Clients should not assume that the debugging has been enabled until the result for this command is received.</span></span>  

&nbsp;  

---  

### <a name="disable"></a><span data-ttu-id="51d98-122">Deaktivieren </span><span class="sxs-lookup"><span data-stu-id="51d98-122">disable</span></span>  

<span data-ttu-id="51d98-123">Deaktiviert den Debugger für eine bestimmte Seite.</span><span class="sxs-lookup"><span data-stu-id="51d98-123">Disables debugger for given page.</span></span>  

&nbsp;  

---  

### <a name="getpossiblebreakpoints"></a><span data-ttu-id="51d98-124">getPossibleBreakpoints</span><span class="sxs-lookup"><span data-stu-id="51d98-124">getPossibleBreakpoints</span></span>  

<span data-ttu-id="51d98-125">Gibt mögliche Speicherorte für Haltepunkte zurück.</span><span class="sxs-lookup"><span data-stu-id="51d98-125">Returns possible locations for breakpoint.</span></span> <span data-ttu-id="51d98-126">scriptId an Start- und Endbereichspositionen sollte identisch sein.</span><span class="sxs-lookup"><span data-stu-id="51d98-126">scriptId in start and end range locations should be the same.</span></span>  

| <span data-ttu-id="51d98-127">Parameter</span><span class="sxs-lookup"><span data-stu-id="51d98-127">Parameters</span></span> | <span data-ttu-id="51d98-128">Typ</span><span class="sxs-lookup"><span data-stu-id="51d98-128">Type</span></span> | <span data-ttu-id="51d98-129">Details</span><span class="sxs-lookup"><span data-stu-id="51d98-129">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="51d98-130">start</span><span class="sxs-lookup"><span data-stu-id="51d98-130">start</span></span> | [<span data-ttu-id="51d98-131">Ort</span><span class="sxs-lookup"><span data-stu-id="51d98-131">Location</span></span>](#location) | <span data-ttu-id="51d98-132">Anfang des Bereichs zum Durchsuchen möglicher Haltepunktpositionen in.</span><span class="sxs-lookup"><span data-stu-id="51d98-132">Start of range to search possible breakpoint locations in.</span></span> |  
| <span data-ttu-id="51d98-133">Aufhören</span><span class="sxs-lookup"><span data-stu-id="51d98-133">end</span></span> | [<span data-ttu-id="51d98-134">Ort</span><span class="sxs-lookup"><span data-stu-id="51d98-134">Location</span></span>](#location) | <span data-ttu-id="51d98-135">Ende des Bereichs, um mögliche Haltepunktpositionen in \(ohne\) zu durchsuchen.</span><span class="sxs-lookup"><span data-stu-id="51d98-135">End of range to search possible breakpoint locations in \(excluding\).</span></span>  <span data-ttu-id="51d98-136">Wenn nicht angegeben, wird das Ende der Skripts als Ende des Bereichs verwendet.</span><span class="sxs-lookup"><span data-stu-id="51d98-136">When not specified, end of scripts is used as end of range.</span></span> |  

| <span data-ttu-id="51d98-137">Gibt zurück</span><span class="sxs-lookup"><span data-stu-id="51d98-137">Returns</span></span> | <span data-ttu-id="51d98-138">Typ</span><span class="sxs-lookup"><span data-stu-id="51d98-138">Type</span></span> | <span data-ttu-id="51d98-139">Details</span><span class="sxs-lookup"><span data-stu-id="51d98-139">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="51d98-140">Speicherorte</span><span class="sxs-lookup"><span data-stu-id="51d98-140">locations</span></span> | [<span data-ttu-id="51d98-141">BreakLocation</span><span class="sxs-lookup"><span data-stu-id="51d98-141">BreakLocation</span></span>](#breaklocation) | <span data-ttu-id="51d98-142">Liste der möglichen Haltepunktpositionen.</span><span class="sxs-lookup"><span data-stu-id="51d98-142">List of the possible breakpoint locations.</span></span> |  

---  

### <a name="setbreakpointsactive"></a><span data-ttu-id="51d98-143">setBreakpointsActive</span><span class="sxs-lookup"><span data-stu-id="51d98-143">setBreakpointsActive</span></span>  

<span data-ttu-id="51d98-144">Aktiviert/deaktiviert alle Haltepunkte auf der Seite.</span><span class="sxs-lookup"><span data-stu-id="51d98-144">Activates / deactivates all breakpoints on the page.</span></span>  

| <span data-ttu-id="51d98-145">Parameter</span><span class="sxs-lookup"><span data-stu-id="51d98-145">Parameters</span></span> | <span data-ttu-id="51d98-146">Typ</span><span class="sxs-lookup"><span data-stu-id="51d98-146">Type</span></span> | <span data-ttu-id="51d98-147">Details</span><span class="sxs-lookup"><span data-stu-id="51d98-147">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="51d98-148">active</span><span class="sxs-lookup"><span data-stu-id="51d98-148">active</span></span> | `boolean` | <span data-ttu-id="51d98-149">Neuer Wert für den aktiven Zustand der Haltepunkte.</span><span class="sxs-lookup"><span data-stu-id="51d98-149">New value for breakpoints active state.</span></span> | 

---  

### <a name="setbreakpointbyurl"></a><span data-ttu-id="51d98-150">setBreakpointByUrl</span><span class="sxs-lookup"><span data-stu-id="51d98-150">setBreakpointByUrl</span></span>  

<span data-ttu-id="51d98-151">Legt den JavaScript-Haltepunkt an einem bestimmten Speicherort fest, der entweder durch URL oder URL regex angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="51d98-151">Sets JavaScript breakpoint at given location specified either by URL or URL regex.</span></span>  <span data-ttu-id="51d98-152">Sobald dieser Befehl ausgegeben wurde, werden für alle vorhandenen analysierten Skripts Haltepunkte aufgelöst und in der Eigenschaft `locations` zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="51d98-152">Once this command is issued, all existing parsed scripts will have breakpoints resolved and returned in `locations` property.</span></span>  <span data-ttu-id="51d98-153">Eine weitere übereinstimmende Skript-Analyse führt zu nachfolgenden `breakpointResolved` Ereignissen.</span><span class="sxs-lookup"><span data-stu-id="51d98-153">Further matching script parsing will result in subsequent `breakpointResolved` events issued.</span></span>  <span data-ttu-id="51d98-154">Dieser logische Haltepunkt überdauert seitenladen.</span><span class="sxs-lookup"><span data-stu-id="51d98-154">This logical breakpoint will survive page reloads.</span></span>  

| <span data-ttu-id="51d98-155">Parameter</span><span class="sxs-lookup"><span data-stu-id="51d98-155">Parameters</span></span> | <span data-ttu-id="51d98-156">Typ</span><span class="sxs-lookup"><span data-stu-id="51d98-156">Type</span></span> | <span data-ttu-id="51d98-157">Details</span><span class="sxs-lookup"><span data-stu-id="51d98-157">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="51d98-158">lineNumber</span><span class="sxs-lookup"><span data-stu-id="51d98-158">lineNumber</span></span> | `integer` | <span data-ttu-id="51d98-159">Zeilennummer zum Festlegen des Haltepunkts.</span><span class="sxs-lookup"><span data-stu-id="51d98-159">Line number to set breakpoint at.</span></span> | 
| <span data-ttu-id="51d98-160">url \(optional\)</span><span class="sxs-lookup"><span data-stu-id="51d98-160">url \(optional\)</span></span> | `string` | <span data-ttu-id="51d98-161">URL der Ressourcen, auf die der Haltepunkt festgelegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="51d98-161">URL of the resources to set breakpoint on.</span></span> |  
| <span data-ttu-id="51d98-162">urlRegex \(optional\)</span><span class="sxs-lookup"><span data-stu-id="51d98-162">urlRegex \(optional\)</span></span> | `string` | <span data-ttu-id="51d98-163">Regex-Muster für die URLs der Ressourcen zum Festlegen von Haltepunkten.</span><span class="sxs-lookup"><span data-stu-id="51d98-163">Regex pattern for the URLs of the resources to set breakpoints on.</span></span>  <span data-ttu-id="51d98-164">Entweder `url` oder muss angegeben `urlRegex` werden.</span><span class="sxs-lookup"><span data-stu-id="51d98-164">Either `url` or `urlRegex` must be specified.</span></span> |  
| <span data-ttu-id="51d98-165">columnNumber \(optional\)</span><span class="sxs-lookup"><span data-stu-id="51d98-165">columnNumber \(optional\)</span></span> | `integer` | <span data-ttu-id="51d98-166">Offset in der Linie, um den Haltepunkt zu festlegen.</span><span class="sxs-lookup"><span data-stu-id="51d98-166">Offset in the line to set breakpoint at.</span></span> |  
| <span data-ttu-id="51d98-167">Bedingung \(optional\)</span><span class="sxs-lookup"><span data-stu-id="51d98-167">condition \(optional\)</span></span> | `string` | <span data-ttu-id="51d98-168">Ausdruck, der als Haltepunktbedingung verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="51d98-168">Expression to use as a breakpoint condition.</span></span> <span data-ttu-id="51d98-169">Wenn angegeben, wird der Debugger nur dann am Haltepunkt beendet, wenn dieser Ausdruck auf true ausgewertet wird.</span><span class="sxs-lookup"><span data-stu-id="51d98-169">When specified, debugger will only stop on the breakpoint if this expression evaluates to true.</span></span> |  

| <span data-ttu-id="51d98-170">Gibt zurück</span><span class="sxs-lookup"><span data-stu-id="51d98-170">Returns</span></span> | <span data-ttu-id="51d98-171">Typ</span><span class="sxs-lookup"><span data-stu-id="51d98-171">Type</span></span> | <span data-ttu-id="51d98-172">Details</span><span class="sxs-lookup"><span data-stu-id="51d98-172">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="51d98-173">breakpointId</span><span class="sxs-lookup"><span data-stu-id="51d98-173">breakpointId</span></span> | [<span data-ttu-id="51d98-174">BreakpointId</span><span class="sxs-lookup"><span data-stu-id="51d98-174">BreakpointId</span></span>](#breakpointid) | <span data-ttu-id="51d98-175">ID des erstellten Haltepunkts für weitere Referenz.</span><span class="sxs-lookup"><span data-stu-id="51d98-175">ID of the created breakpoint for further reference.</span></span> |  
| <span data-ttu-id="51d98-176">Speicherorte</span><span class="sxs-lookup"><span data-stu-id="51d98-176">locations</span></span> | [<span data-ttu-id="51d98-177">Location[]</span><span class="sxs-lookup"><span data-stu-id="51d98-177">Location[]</span></span>](#location) | <span data-ttu-id="51d98-178">Liste der Speicherorte, in die dieser Haltepunkt beim Hinzufügen aufgelöst wurde.</span><span class="sxs-lookup"><span data-stu-id="51d98-178">List of the locations this breakpoint resolved into upon addition.</span></span> |  

---  

### <a name="setbreakpoint"></a><span data-ttu-id="51d98-179">setBreakpoint</span><span class="sxs-lookup"><span data-stu-id="51d98-179">setBreakpoint</span></span>  

<span data-ttu-id="51d98-180">Legt den JavaScript-Haltepunkt an einem bestimmten Speicherort fest.</span><span class="sxs-lookup"><span data-stu-id="51d98-180">Sets JavaScript breakpoint at a given location.</span></span>  

| <span data-ttu-id="51d98-181">Parameter</span><span class="sxs-lookup"><span data-stu-id="51d98-181">Parameters</span></span> | <span data-ttu-id="51d98-182">Typ</span><span class="sxs-lookup"><span data-stu-id="51d98-182">Type</span></span> | <span data-ttu-id="51d98-183">Details</span><span class="sxs-lookup"><span data-stu-id="51d98-183">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="51d98-184">location</span><span class="sxs-lookup"><span data-stu-id="51d98-184">location</span></span> | [<span data-ttu-id="51d98-185">Ort</span><span class="sxs-lookup"><span data-stu-id="51d98-185">Location</span></span>](#location) | <span data-ttu-id="51d98-186">Speicherort zum Festlegen des Haltepunkts.</span><span class="sxs-lookup"><span data-stu-id="51d98-186">Location to set breakpoint in.</span></span> |  
| <span data-ttu-id="51d98-187">Bedingung \(optional\)</span><span class="sxs-lookup"><span data-stu-id="51d98-187">condition \(optional\)</span></span> | `string` | <span data-ttu-id="51d98-188">Ausdruck, der als Haltepunktbedingung verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="51d98-188">Expression to use as a breakpoint condition.</span></span>  <span data-ttu-id="51d98-189">Wenn angegeben, wird der Debugger nur dann am Haltepunkt beendet, wenn dieser Ausdruck auf true ausgewertet wird.</span><span class="sxs-lookup"><span data-stu-id="51d98-189">When specified, debugger will only stop on the breakpoint if this expression evaluates to true.</span></span> |  

| <span data-ttu-id="51d98-190">Gibt zurück</span><span class="sxs-lookup"><span data-stu-id="51d98-190">Returns</span></span> | <span data-ttu-id="51d98-191">Typ</span><span class="sxs-lookup"><span data-stu-id="51d98-191">Type</span></span> | <span data-ttu-id="51d98-192">Details</span><span class="sxs-lookup"><span data-stu-id="51d98-192">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="51d98-193">breakpointId</span><span class="sxs-lookup"><span data-stu-id="51d98-193">breakpointId</span></span> | [<span data-ttu-id="51d98-194">BreakpointId</span><span class="sxs-lookup"><span data-stu-id="51d98-194">BreakpointId</span></span>](#breakpointid) | <span data-ttu-id="51d98-195">ID des erstellten Haltepunkts für weitere Referenz.</span><span class="sxs-lookup"><span data-stu-id="51d98-195">ID of the created breakpoint for further reference.</span></span> |  
| <span data-ttu-id="51d98-196">actualLocation</span><span class="sxs-lookup"><span data-stu-id="51d98-196">actualLocation</span></span> | [<span data-ttu-id="51d98-197">Ort</span><span class="sxs-lookup"><span data-stu-id="51d98-197">Location</span></span>](#location) | <span data-ttu-id="51d98-198">Speicherort, in den dieser Haltepunkt aufgelöst wurde.</span><span class="sxs-lookup"><span data-stu-id="51d98-198">Location this breakpoint resolved into.</span></span> |  

---  

### <a name="removebreakpoint"></a><span data-ttu-id="51d98-199">removeBreakpoint</span><span class="sxs-lookup"><span data-stu-id="51d98-199">removeBreakpoint</span></span>  

<span data-ttu-id="51d98-200">Entfernt den JavaScript-Haltepunkt.</span><span class="sxs-lookup"><span data-stu-id="51d98-200">Removes JavaScript breakpoint.</span></span>  

| <span data-ttu-id="51d98-201">Parameter</span><span class="sxs-lookup"><span data-stu-id="51d98-201">Parameters</span></span> | <span data-ttu-id="51d98-202">Typ</span><span class="sxs-lookup"><span data-stu-id="51d98-202">Type</span></span> | <span data-ttu-id="51d98-203">Details</span><span class="sxs-lookup"><span data-stu-id="51d98-203">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="51d98-204">breakpointId</span><span class="sxs-lookup"><span data-stu-id="51d98-204">breakpointId</span></span> | [<span data-ttu-id="51d98-205">BreakpointId</span><span class="sxs-lookup"><span data-stu-id="51d98-205">BreakpointId</span></span>](#breakpointid) | &nbsp; |  

---  

### <a name="stepover"></a><span data-ttu-id="51d98-206">stepOver</span><span class="sxs-lookup"><span data-stu-id="51d98-206">stepOver</span></span>  

<span data-ttu-id="51d98-207">Schritte über die Anweisung.</span><span class="sxs-lookup"><span data-stu-id="51d98-207">Steps over the statement.</span></span>  

&nbsp;  

---  

### <a name="stepinto"></a><span data-ttu-id="51d98-208">stepInto</span><span class="sxs-lookup"><span data-stu-id="51d98-208">stepInto</span></span>  

<span data-ttu-id="51d98-209">Schritte in den Funktionsaufruf.</span><span class="sxs-lookup"><span data-stu-id="51d98-209">Steps into the function call.</span></span>  

&nbsp;  

---  

### <a name="stepout"></a><span data-ttu-id="51d98-210">stepOut</span><span class="sxs-lookup"><span data-stu-id="51d98-210">stepOut</span></span>  

<span data-ttu-id="51d98-211">Tritt aus dem Funktionsaufruf aus.</span><span class="sxs-lookup"><span data-stu-id="51d98-211">Steps out of the function call.</span></span>  

&nbsp;  

---  

### <a name="pause"></a><span data-ttu-id="51d98-212">pause</span><span class="sxs-lookup"><span data-stu-id="51d98-212">pause</span></span>  

<span data-ttu-id="51d98-213">Stoppt bei der nächsten JavaScript-Anweisung.</span><span class="sxs-lookup"><span data-stu-id="51d98-213">Stops on the next JavaScript statement.</span></span>  

&nbsp;  

---  

### <a name="resume"></a><span data-ttu-id="51d98-214">resume</span><span class="sxs-lookup"><span data-stu-id="51d98-214">resume</span></span>  

<span data-ttu-id="51d98-215">Setzt die JavaScript-Ausführung fort.</span><span class="sxs-lookup"><span data-stu-id="51d98-215">Resumes JavaScript execution.</span></span>  

&nbsp;  

---  

### <a name="getscriptsource"></a><span data-ttu-id="51d98-216">getScriptSource</span><span class="sxs-lookup"><span data-stu-id="51d98-216">getScriptSource</span></span>  

<span data-ttu-id="51d98-217">Gibt die Quelle für das Skript mit der angegebenen ID zurück.</span><span class="sxs-lookup"><span data-stu-id="51d98-217">Returns source for the script with given id.</span></span>  

| <span data-ttu-id="51d98-218">Parameter</span><span class="sxs-lookup"><span data-stu-id="51d98-218">Parameters</span></span> | <span data-ttu-id="51d98-219">Typ</span><span class="sxs-lookup"><span data-stu-id="51d98-219">Type</span></span> | <span data-ttu-id="51d98-220">Details</span><span class="sxs-lookup"><span data-stu-id="51d98-220">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="51d98-221">scriptId</span><span class="sxs-lookup"><span data-stu-id="51d98-221">scriptId</span></span> | [<span data-ttu-id="51d98-222">Runtime.ScriptId</span><span class="sxs-lookup"><span data-stu-id="51d98-222">Runtime.ScriptId</span></span>](./runtime.md#scriptid) | <span data-ttu-id="51d98-223">DIE ID des Skripts, für das Die Quelle erhalten werden soll.</span><span class="sxs-lookup"><span data-stu-id="51d98-223">ID of the script to get source for.</span></span> |  

| <span data-ttu-id="51d98-224">Gibt zurück</span><span class="sxs-lookup"><span data-stu-id="51d98-224">Returns</span></span> | <span data-ttu-id="51d98-225">Typ</span><span class="sxs-lookup"><span data-stu-id="51d98-225">Type</span></span> | <span data-ttu-id="51d98-226">Details</span><span class="sxs-lookup"><span data-stu-id="51d98-226">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="51d98-227">scriptSource</span><span class="sxs-lookup"><span data-stu-id="51d98-227">scriptSource</span></span> | `string` | <span data-ttu-id="51d98-228">Skriptquelle.</span><span class="sxs-lookup"><span data-stu-id="51d98-228">Script source.</span></span> | 

---  

### <a name="setpauseonexceptions"></a><span data-ttu-id="51d98-229">setPauseOnExceptions</span><span class="sxs-lookup"><span data-stu-id="51d98-229">setPauseOnExceptions</span></span>  

<span data-ttu-id="51d98-230">Definiert pause on exceptions state.</span><span class="sxs-lookup"><span data-stu-id="51d98-230">Defines pause on exceptions state.</span></span>  <span data-ttu-id="51d98-231">Kann so festgelegt werden, dass alle Ausnahmen, nicht abgefangenen Ausnahmen oder keine Ausnahmen beendet werden.</span><span class="sxs-lookup"><span data-stu-id="51d98-231">Can be set to stop on all exceptions, uncaught exceptions or no exceptions.</span></span>  <span data-ttu-id="51d98-232">Die anfängliche Pause für den Ausnahmezustand ist `none` .</span><span class="sxs-lookup"><span data-stu-id="51d98-232">Initial pause on exceptions state is `none`.</span></span>  

| <span data-ttu-id="51d98-233">Parameter</span><span class="sxs-lookup"><span data-stu-id="51d98-233">Parameters</span></span> | <span data-ttu-id="51d98-234">Typ</span><span class="sxs-lookup"><span data-stu-id="51d98-234">Type</span></span> | <span data-ttu-id="51d98-235">Details</span><span class="sxs-lookup"><span data-stu-id="51d98-235">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="51d98-236">state</span><span class="sxs-lookup"><span data-stu-id="51d98-236">state</span></span> | `string` | <span data-ttu-id="51d98-237">Halten Sie den Ausnahmemodus an.</span><span class="sxs-lookup"><span data-stu-id="51d98-237">Pause on exceptions mode.</span></span>  <span data-ttu-id="51d98-238">Zulässige Werte:  `none` `uncaught` , ,</span><span class="sxs-lookup"><span data-stu-id="51d98-238">Allowed values:  `none`, `uncaught`,</span></span> `all` |  

---  

### <a name="evaluateoncallframe"></a><span data-ttu-id="51d98-239">evaluateOnCallFrame</span><span class="sxs-lookup"><span data-stu-id="51d98-239">evaluateOnCallFrame</span></span>  

<span data-ttu-id="51d98-240">Wertet Ausdruck für einen bestimmten Aufrufrahmen aus.</span><span class="sxs-lookup"><span data-stu-id="51d98-240">Evaluates expression on a given call frame.</span></span>  

| <span data-ttu-id="51d98-241">Parameter</span><span class="sxs-lookup"><span data-stu-id="51d98-241">Parameters</span></span> | <span data-ttu-id="51d98-242">Typ</span><span class="sxs-lookup"><span data-stu-id="51d98-242">Type</span></span> | <span data-ttu-id="51d98-243">Details</span><span class="sxs-lookup"><span data-stu-id="51d98-243">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="51d98-244">callFrameId</span><span class="sxs-lookup"><span data-stu-id="51d98-244">callFrameId</span></span> | [<span data-ttu-id="51d98-245">CallFrameId</span><span class="sxs-lookup"><span data-stu-id="51d98-245">CallFrameId</span></span>](#callframeid) | <span data-ttu-id="51d98-246">Anrufrahmen-ID, die ausgewertet werden soll.</span><span class="sxs-lookup"><span data-stu-id="51d98-246">Call frame identifier to evaluate on.</span></span> |  
| <span data-ttu-id="51d98-247">Ausdruck</span><span class="sxs-lookup"><span data-stu-id="51d98-247">expression</span></span> | `string` | <span data-ttu-id="51d98-248">Ausdruck, der ausgewertet werden soll.</span><span class="sxs-lookup"><span data-stu-id="51d98-248">Expression to evaluate.</span></span> | 

| <span data-ttu-id="51d98-249">Gibt zurück</span><span class="sxs-lookup"><span data-stu-id="51d98-249">Returns</span></span> | <span data-ttu-id="51d98-250">Typ</span><span class="sxs-lookup"><span data-stu-id="51d98-250">Type</span></span> | <span data-ttu-id="51d98-251">Details</span><span class="sxs-lookup"><span data-stu-id="51d98-251">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="51d98-252">result</span><span class="sxs-lookup"><span data-stu-id="51d98-252">result</span></span> | [<span data-ttu-id="51d98-253">Runtime.RemoteObject</span><span class="sxs-lookup"><span data-stu-id="51d98-253">Runtime.RemoteObject</span></span>](./runtime.md#remoteobject) | <span data-ttu-id="51d98-254">Objektwrapper für das Auswertungsergebnis.</span><span class="sxs-lookup"><span data-stu-id="51d98-254">Object wrapper for the evaluation result.</span></span> |  

---  

### <a name="setvariablevalue"></a><span data-ttu-id="51d98-255">setVariableValue</span><span class="sxs-lookup"><span data-stu-id="51d98-255">setVariableValue</span></span>  

<span data-ttu-id="51d98-256">Ändert den Wert der Variablen in einem Callframe.</span><span class="sxs-lookup"><span data-stu-id="51d98-256">Changes value of variable in a callframe.</span></span>  <span data-ttu-id="51d98-257">Objektbasierte Bereiche werden nicht unterstützt und müssen manuell mutiert werden.</span><span class="sxs-lookup"><span data-stu-id="51d98-257">Object-based scopes are not supported and must be mutated manually.</span></span>  

| <span data-ttu-id="51d98-258">Parameter</span><span class="sxs-lookup"><span data-stu-id="51d98-258">Parameters</span></span> | <span data-ttu-id="51d98-259">Typ</span><span class="sxs-lookup"><span data-stu-id="51d98-259">Type</span></span> | <span data-ttu-id="51d98-260">Details</span><span class="sxs-lookup"><span data-stu-id="51d98-260">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="51d98-261">scopeNumber</span><span class="sxs-lookup"><span data-stu-id="51d98-261">scopeNumber</span></span> | `integer` | <span data-ttu-id="51d98-262">0-basierte Anzahl des Bereichs, wie in der Bereichskette aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="51d98-262">0-based number of scope as was listed in scope chain.</span></span>  <span data-ttu-id="51d98-263">Nur `local` , `closure` und `catch` Bereichstypen sind zulässig.</span><span class="sxs-lookup"><span data-stu-id="51d98-263">Only `local`, `closure`, and `catch` scope types are allowed.</span></span>  <span data-ttu-id="51d98-264">Andere Bereiche können manuell bearbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="51d98-264">Other scopes could be manipulated manually.</span></span> | 
| <span data-ttu-id="51d98-265">variableName</span><span class="sxs-lookup"><span data-stu-id="51d98-265">variableName</span></span> | `string` | <span data-ttu-id="51d98-266">Variabler Name.</span><span class="sxs-lookup"><span data-stu-id="51d98-266">Variable name.</span></span> | 
| <span data-ttu-id="51d98-267">newValue</span><span class="sxs-lookup"><span data-stu-id="51d98-267">newValue</span></span> | [<span data-ttu-id="51d98-268">Runtime.CallArgument</span><span class="sxs-lookup"><span data-stu-id="51d98-268">Runtime.CallArgument</span></span>](./runtime.md#callargument) | <span data-ttu-id="51d98-269">Neuer Variabler Wert.</span><span class="sxs-lookup"><span data-stu-id="51d98-269">New variable value.</span></span> |  
| <span data-ttu-id="51d98-270">callFrameId</span><span class="sxs-lookup"><span data-stu-id="51d98-270">callFrameId</span></span> | [<span data-ttu-id="51d98-271">CallFrameId</span><span class="sxs-lookup"><span data-stu-id="51d98-271">CallFrameId</span></span>](#callframeid) | <span data-ttu-id="51d98-272">ID des Callframes, der eine Variable enthält.</span><span class="sxs-lookup"><span data-stu-id="51d98-272">ID of callframe that holds variable.</span></span> |  

---  

### <a name="setblackboxpatterns"></a><span data-ttu-id="51d98-273">setBlackboxPatterns</span><span class="sxs-lookup"><span data-stu-id="51d98-273">setBlackboxPatterns</span></span>  

<span data-ttu-id="51d98-274">**Experimental**.</span><span class="sxs-lookup"><span data-stu-id="51d98-274">**Experimental**.</span></span>  <span data-ttu-id="51d98-275">Ersetzen Sie vorherige Blackboxmuster durch übergebene Muster.</span><span class="sxs-lookup"><span data-stu-id="51d98-275">Replace previous blackbox patterns with passed ones.</span></span>  <span data-ttu-id="51d98-276">Erzwingt das Back-End, das Schrittweise/Anhalten in Skripts zu überspringen, deren URL mit einem der Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="51d98-276">Forces backend to skip stepping/pausing in scripts with url matching one of the patterns.</span></span>  <span data-ttu-id="51d98-277">Der Debugger versucht, das blackboxed-Skript zu verlassen, indem er mehrmals "Einschritt" ausgeführt hat, und schließlich zu "Step out" greifen, wenn dies nicht erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="51d98-277">The debugger will try to leave blackboxed script by performing 'step in' several times, finally resorting to 'step out' if unsuccessful.</span></span>  


| <span data-ttu-id="51d98-278">Parameter</span><span class="sxs-lookup"><span data-stu-id="51d98-278">Parameters</span></span> | <span data-ttu-id="51d98-279">Typ</span><span class="sxs-lookup"><span data-stu-id="51d98-279">Type</span></span> | <span data-ttu-id="51d98-280">Details</span><span class="sxs-lookup"><span data-stu-id="51d98-280">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="51d98-281">Muster</span><span class="sxs-lookup"><span data-stu-id="51d98-281">patterns</span></span> | `string[]` | <span data-ttu-id="51d98-282">Array von Regexps, das zum Überprüfen der Skript-URL auf den Blackboxstatus verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="51d98-282">Array of regexps that will be used to check script url for blackbox state.</span></span> | 

---  

### <a name="mssetdebuggerpropertyvalue"></a><span data-ttu-id="51d98-283">msSetDebuggerPropertyValue</span><span class="sxs-lookup"><span data-stu-id="51d98-283">msSetDebuggerPropertyValue</span></span>  

<span data-ttu-id="51d98-284">**Experimental**.</span><span class="sxs-lookup"><span data-stu-id="51d98-284">**Experimental**.</span></span>  <span data-ttu-id="51d98-285">Microsoft: Legt die angegebene Debuggereigenschaft auf den angegebenen Wert fest.</span><span class="sxs-lookup"><span data-stu-id="51d98-285">Microsoft: Sets the specified debugger property to the specified value.</span></span>  

| <span data-ttu-id="51d98-286">Parameter</span><span class="sxs-lookup"><span data-stu-id="51d98-286">Parameters</span></span> | <span data-ttu-id="51d98-287">Typ</span><span class="sxs-lookup"><span data-stu-id="51d98-287">Type</span></span> | <span data-ttu-id="51d98-288">Details</span><span class="sxs-lookup"><span data-stu-id="51d98-288">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="51d98-289">debuggerPropertyId</span><span class="sxs-lookup"><span data-stu-id="51d98-289">debuggerPropertyId</span></span> | <span data-ttu-id="51d98-290">string</span><span class="sxs-lookup"><span data-stu-id="51d98-290">string</span></span> | <span data-ttu-id="51d98-291">Microsoft: Die eigenschafts-ID \(d. h. `msDebuggerPropertyId` \), die festgelegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="51d98-291">Microsoft:  The property id \(i.e. `msDebuggerPropertyId`\) to set.</span></span> | 
| <span data-ttu-id="51d98-292">newValue</span><span class="sxs-lookup"><span data-stu-id="51d98-292">newValue</span></span> | `string` | &nbsp; |  

---  

## <a name="events"></a><span data-ttu-id="51d98-293">Veranstaltungen</span><span class="sxs-lookup"><span data-stu-id="51d98-293">Events</span></span>  

### <a name="scriptparsed"></a><span data-ttu-id="51d98-294">scriptParsed</span><span class="sxs-lookup"><span data-stu-id="51d98-294">scriptParsed</span></span>  

<span data-ttu-id="51d98-295">Wird ausgelöst, wenn das Skript analysiert wird.</span><span class="sxs-lookup"><span data-stu-id="51d98-295">Fired when the script is parsed.</span></span> <span data-ttu-id="51d98-296">Dieses Ereignis wird auch für alle bekannten und nicht abgeholten Skripts beim Aktivieren des Debuggers ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="51d98-296">This event is also fired for all known and uncollected scripts upon enabling debugger.</span></span>  

| <span data-ttu-id="51d98-297">Parameter</span><span class="sxs-lookup"><span data-stu-id="51d98-297">Parameters</span></span> | <span data-ttu-id="51d98-298">Typ</span><span class="sxs-lookup"><span data-stu-id="51d98-298">Type</span></span> | <span data-ttu-id="51d98-299">Details</span><span class="sxs-lookup"><span data-stu-id="51d98-299">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="51d98-300">scriptId</span><span class="sxs-lookup"><span data-stu-id="51d98-300">scriptId</span></span> | [<span data-ttu-id="51d98-301">Runtime.ScriptId</span><span class="sxs-lookup"><span data-stu-id="51d98-301">Runtime.ScriptId</span></span>](./runtime.md#scriptid) | <span data-ttu-id="51d98-302">Bezeichner des analysierten Skripts.</span><span class="sxs-lookup"><span data-stu-id="51d98-302">Identifier of the script parsed.</span></span> |  
| <span data-ttu-id="51d98-303">URL</span><span class="sxs-lookup"><span data-stu-id="51d98-303">url</span></span> | `string` | <span data-ttu-id="51d98-304">URL oder Name des analysierten Skripts \(falls ein\).</span><span class="sxs-lookup"><span data-stu-id="51d98-304">URL or name of the script parsed \(if any\).</span></span> | 
| <span data-ttu-id="51d98-305">startLine</span><span class="sxs-lookup"><span data-stu-id="51d98-305">startLine</span></span> | `integer` | <span data-ttu-id="51d98-306">Zeilenversatz des Skripts innerhalb der Ressource mit der angegebenen URL \(für Skripttags\).</span><span class="sxs-lookup"><span data-stu-id="51d98-306">Line offset of the script within the resource with given URL \(for script tags\).</span></span> | 
| <span data-ttu-id="51d98-307">startColumn</span><span class="sxs-lookup"><span data-stu-id="51d98-307">startColumn</span></span> | `integer` | <span data-ttu-id="51d98-308">Spaltenversatz des Skripts innerhalb der Ressource mit einer angegebenen URL.</span><span class="sxs-lookup"><span data-stu-id="51d98-308">Column offset of the script within the resource with given URL.</span></span> | 
| <span data-ttu-id="51d98-309">endLine</span><span class="sxs-lookup"><span data-stu-id="51d98-309">endLine</span></span> | `integer` | <span data-ttu-id="51d98-310">Letzte Zeile des Skripts.</span><span class="sxs-lookup"><span data-stu-id="51d98-310">Last line of the script.</span></span> | 
| <span data-ttu-id="51d98-311">endColumn</span><span class="sxs-lookup"><span data-stu-id="51d98-311">endColumn</span></span> | `integer` | <span data-ttu-id="51d98-312">Länge der letzten Zeile des Skripts.</span><span class="sxs-lookup"><span data-stu-id="51d98-312">Length of the last line of the script.</span></span> | 
| <span data-ttu-id="51d98-313">executionContextId</span><span class="sxs-lookup"><span data-stu-id="51d98-313">executionContextId</span></span> | [<span data-ttu-id="51d98-314">Runtime.ExecutionContextId</span><span class="sxs-lookup"><span data-stu-id="51d98-314">Runtime.ExecutionContextId</span></span>](./runtime.md#executioncontextid) | <span data-ttu-id="51d98-315">Gibt den Kontext für die Skripterstellung an.</span><span class="sxs-lookup"><span data-stu-id="51d98-315">Specifies script creation context.</span></span> |  
| <span data-ttu-id="51d98-316">sourceMapURL \(optional\)</span><span class="sxs-lookup"><span data-stu-id="51d98-316">sourceMapURL \(optional\)</span></span> | `string` | <span data-ttu-id="51d98-317">URL der Quellzuordnung, die dem Skript zugeordnet ist (falls eine).</span><span class="sxs-lookup"><span data-stu-id="51d98-317">URL of source map associated with script (if any).</span></span> |  
| <span data-ttu-id="51d98-318">length \(optional\)</span><span class="sxs-lookup"><span data-stu-id="51d98-318">length \(optional\)</span></span> | `integer` | <span data-ttu-id="51d98-319">**Experimental**.</span><span class="sxs-lookup"><span data-stu-id="51d98-319">**Experimental**.</span></span>  <span data-ttu-id="51d98-320">Diese Skriptlänge.</span><span class="sxs-lookup"><span data-stu-id="51d98-320">This script length.</span></span> |  
| <span data-ttu-id="51d98-321">msParentId \(optional\)</span><span class="sxs-lookup"><span data-stu-id="51d98-321">msParentId \(optional\)</span></span> | `string` | <span data-ttu-id="51d98-322">**Experimental**.</span><span class="sxs-lookup"><span data-stu-id="51d98-322">**Experimental**.</span></span>  <span data-ttu-id="51d98-323">Dies ist die übergeordnete Dokument-ID.</span><span class="sxs-lookup"><span data-stu-id="51d98-323">This is the parent document ID.</span></span> |  
| <span data-ttu-id="51d98-324">msMimeType \(optional\)</span><span class="sxs-lookup"><span data-stu-id="51d98-324">msMimeType \(optional\)</span></span> | `string` | <span data-ttu-id="51d98-325">**Experimental**.</span><span class="sxs-lookup"><span data-stu-id="51d98-325">**Experimental**.</span></span>  <span data-ttu-id="51d98-326">Dies ist der Mimetyp.</span><span class="sxs-lookup"><span data-stu-id="51d98-326">This is the mime type.</span></span> |  
| <span data-ttu-id="51d98-327">msIsDynamicCode \(optional\)</span><span class="sxs-lookup"><span data-stu-id="51d98-327">msIsDynamicCode \(optional\)</span></span> | `boolean` | <span data-ttu-id="51d98-328">**Experimental**.</span><span class="sxs-lookup"><span data-stu-id="51d98-328">**Experimental**.</span></span>  <span data-ttu-id="51d98-329">Dies gibt an, ob es sich um dynamischen Code handelt.</span><span class="sxs-lookup"><span data-stu-id="51d98-329">This indicates whether it is dynamic code.</span></span> |  
| <span data-ttu-id="51d98-330">msLongDocumentId \(optional\)</span><span class="sxs-lookup"><span data-stu-id="51d98-330">msLongDocumentId \(optional\)</span></span> | `integer` | <span data-ttu-id="51d98-331">**Experimental**.</span><span class="sxs-lookup"><span data-stu-id="51d98-331">**Experimental**.</span></span>  <span data-ttu-id="51d98-332">Dies ist die lange Dokument-ID.</span><span class="sxs-lookup"><span data-stu-id="51d98-332">This is the long document ID.</span></span> |  

---  

### <a name="breakpointresolved"></a><span data-ttu-id="51d98-333">breakpointResolved</span><span class="sxs-lookup"><span data-stu-id="51d98-333">breakpointResolved</span></span>  

<span data-ttu-id="51d98-334">Wird ausgelöst, wenn der Haltepunkt in ein tatsächliches Skript und einen tatsächlichen Speicherort aufgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="51d98-334">Fired when breakpoint is resolved to an actual script and location.</span></span>  

| <span data-ttu-id="51d98-335">Parameter</span><span class="sxs-lookup"><span data-stu-id="51d98-335">Parameters</span></span> | <span data-ttu-id="51d98-336">Typ</span><span class="sxs-lookup"><span data-stu-id="51d98-336">Type</span></span> | <span data-ttu-id="51d98-337">Details</span><span class="sxs-lookup"><span data-stu-id="51d98-337">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="51d98-338">breakpointId</span><span class="sxs-lookup"><span data-stu-id="51d98-338">breakpointId</span></span> | [<span data-ttu-id="51d98-339">BreakpointId</span><span class="sxs-lookup"><span data-stu-id="51d98-339">BreakpointId</span></span>](#breakpointid) | <span data-ttu-id="51d98-340">Eindeutiger Bezeichner des Haltepunkts.</span><span class="sxs-lookup"><span data-stu-id="51d98-340">Breakpoint unique identifier.</span></span> |  
| <span data-ttu-id="51d98-341">location</span><span class="sxs-lookup"><span data-stu-id="51d98-341">location</span></span> | [<span data-ttu-id="51d98-342">Ort</span><span class="sxs-lookup"><span data-stu-id="51d98-342">Location</span></span>](#location) | <span data-ttu-id="51d98-343">Tatsächliche Haltepunktposition.</span><span class="sxs-lookup"><span data-stu-id="51d98-343">Actual breakpoint location.</span></span> |  
| <span data-ttu-id="51d98-344">msLength \(optional\)</span><span class="sxs-lookup"><span data-stu-id="51d98-344">msLength \(optional\)</span></span> | `integer` | <span data-ttu-id="51d98-345">**Experimental**.</span><span class="sxs-lookup"><span data-stu-id="51d98-345">**Experimental**.</span></span>  <span data-ttu-id="51d98-346">Microsoft: Länge des Codes \(d. h. Anzahl der Zeichen\) am Haltepunktspeicherort.</span><span class="sxs-lookup"><span data-stu-id="51d98-346">Microsoft:  Length of code \(i.e. number of characters\) at the breakpoint location.</span></span> |  

---  

### <a name="paused"></a><span data-ttu-id="51d98-347">angehalten</span><span class="sxs-lookup"><span data-stu-id="51d98-347">paused</span></span>  

<span data-ttu-id="51d98-348">Wird ausgelöst, wenn der Debugger für einen Haltepunkt oder eine Ausnahme umbricht.</span><span class="sxs-lookup"><span data-stu-id="51d98-348">Fired when the debuggers breaks for a breakpoint or exception.</span></span>  

| <span data-ttu-id="51d98-349">Parameter</span><span class="sxs-lookup"><span data-stu-id="51d98-349">Parameters</span></span> | <span data-ttu-id="51d98-350">Typ</span><span class="sxs-lookup"><span data-stu-id="51d98-350">Type</span></span> | <span data-ttu-id="51d98-351">Details</span><span class="sxs-lookup"><span data-stu-id="51d98-351">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="51d98-352">callFrames</span><span class="sxs-lookup"><span data-stu-id="51d98-352">callFrames</span></span> | [<span data-ttu-id="51d98-353">CallFrame[]</span><span class="sxs-lookup"><span data-stu-id="51d98-353">CallFrame[]</span></span>](#callframe) | <span data-ttu-id="51d98-354">Aufrufstapel, auf dem der Debugger beendet wurde.</span><span class="sxs-lookup"><span data-stu-id="51d98-354">Call stack the debugger stopped on.</span></span> |  
| <span data-ttu-id="51d98-355">reason</span><span class="sxs-lookup"><span data-stu-id="51d98-355">reason</span></span> | `string` |  <span data-ttu-id="51d98-356">Grund anhalten.</span><span class="sxs-lookup"><span data-stu-id="51d98-356">Pause reason.</span></span>  <span data-ttu-id="51d98-357">Zulässige Werte:  `breakpoint` , , , , `step` `exception` `other` und</span><span class="sxs-lookup"><span data-stu-id="51d98-357">Allowed values:  `breakpoint`, `step`, `exception`, `other`, and</span></span> `EventListener` |  
| <span data-ttu-id="51d98-358">data \(optional\)</span><span class="sxs-lookup"><span data-stu-id="51d98-358">data \(optional\)</span></span> | `object` | <span data-ttu-id="51d98-359">Objekt mit unterbrechungsspezifischen Hilfseigenschaften.</span><span class="sxs-lookup"><span data-stu-id="51d98-359">Object containing break-specific auxiliary properties.</span></span> |  
| <span data-ttu-id="51d98-360">hitBreakpoints \(optional\)</span><span class="sxs-lookup"><span data-stu-id="51d98-360">hitBreakpoints \(optional\)</span></span> | `string[]` | <span data-ttu-id="51d98-361">Hit breakpoints IDs</span><span class="sxs-lookup"><span data-stu-id="51d98-361">Hit breakpoints IDs</span></span> |  
| <span data-ttu-id="51d98-362">asyncStackTrace \(optional\)</span><span class="sxs-lookup"><span data-stu-id="51d98-362">asyncStackTrace \(optional\)</span></span> | `StackTrace` | <span data-ttu-id="51d98-363">JavaScript async stack trace.</span><span class="sxs-lookup"><span data-stu-id="51d98-363">JavaScript async stack trace.</span></span> |  

---  

### <a name="resumed"></a><span data-ttu-id="51d98-364">fortgesetzt</span><span class="sxs-lookup"><span data-stu-id="51d98-364">resumed</span></span>  

<span data-ttu-id="51d98-365">Wird ausgelöst, wenn der Debugger die Ausführung wieder auf sich nimmt.</span><span class="sxs-lookup"><span data-stu-id="51d98-365">Fired when the debugger resumes execution.</span></span>  

&nbsp;  

---  

## <a name="types"></a><span data-ttu-id="51d98-366">Typen</span><span class="sxs-lookup"><span data-stu-id="51d98-366">Types</span></span>  

### <a name="breakpointid-string"></a><span data-ttu-id="51d98-367">BreakpointId-Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="51d98-367">BreakpointId string</span></span>  

<a name="breakpointid"></a>  

<span data-ttu-id="51d98-368">Haltepunkt-ID.</span><span class="sxs-lookup"><span data-stu-id="51d98-368">Breakpoint identifier.</span></span>  

&nbsp;  

---  

### <a name="callframeid-string"></a><span data-ttu-id="51d98-369">CallFrameId-Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="51d98-369">CallFrameId string</span></span>  

<a name="callframeid"></a>  

<span data-ttu-id="51d98-370">Anrufrahmen-ID.</span><span class="sxs-lookup"><span data-stu-id="51d98-370">Call frame identifier.</span></span>  

&nbsp;  

---  

### <a name="location-object"></a><span data-ttu-id="51d98-371">Location-Objekt</span><span class="sxs-lookup"><span data-stu-id="51d98-371">Location object</span></span>  

<a name="location"></a>  

<span data-ttu-id="51d98-372">Speicherort im Quellcode.</span><span class="sxs-lookup"><span data-stu-id="51d98-372">Location in the source code.</span></span>  

| <span data-ttu-id="51d98-373">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="51d98-373">Properties</span></span> | <span data-ttu-id="51d98-374">Typ</span><span class="sxs-lookup"><span data-stu-id="51d98-374">Type</span></span> | <span data-ttu-id="51d98-375">Details</span><span class="sxs-lookup"><span data-stu-id="51d98-375">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="51d98-376">scriptId</span><span class="sxs-lookup"><span data-stu-id="51d98-376">scriptId</span></span> | [<span data-ttu-id="51d98-377">Runtime.ScriptId</span><span class="sxs-lookup"><span data-stu-id="51d98-377">Runtime.ScriptId</span></span>](./runtime.md#scriptid) | <span data-ttu-id="51d98-378">Skript-ID, wie in der `Debugger.scriptParsed` angegeben.</span><span class="sxs-lookup"><span data-stu-id="51d98-378">Script identifier as reported in the `Debugger.scriptParsed`.</span></span> |  
| <span data-ttu-id="51d98-379">lineNumber</span><span class="sxs-lookup"><span data-stu-id="51d98-379">lineNumber</span></span> | `integer` | <span data-ttu-id="51d98-380">Zeilennummer im Skript \(0-basiert\).</span><span class="sxs-lookup"><span data-stu-id="51d98-380">Line number in the script \(0-based\).</span></span> |  
| <span data-ttu-id="51d98-381">columnNumber \(optional\)</span><span class="sxs-lookup"><span data-stu-id="51d98-381">columnNumber \(optional\)</span></span> | `integer` | <span data-ttu-id="51d98-382">Spaltennummer im Skript \(0-basiert\).</span><span class="sxs-lookup"><span data-stu-id="51d98-382">Column number in the script \(0-based\).</span></span> |  
| <span data-ttu-id="51d98-383">msLength</span><span class="sxs-lookup"><span data-stu-id="51d98-383">msLength</span></span> | `integer` | <span data-ttu-id="51d98-384">Microsoft: Länge des Codes \(d. h. Anzahl der Zeichen\) in diesem Aufrufrahmen.</span><span class="sxs-lookup"><span data-stu-id="51d98-384">Microsoft:  Length of code \(i.e. number of characters\) at this call frame.</span></span> |  

---  

### <a name="breaklocation-object"></a><span data-ttu-id="51d98-385">BreakLocation-Objekt</span><span class="sxs-lookup"><span data-stu-id="51d98-385">BreakLocation object</span></span>  

<a name="breaklocation"></a>  

<span data-ttu-id="51d98-386">Speicherort im Quellcode umbrechen.</span><span class="sxs-lookup"><span data-stu-id="51d98-386">Break location in the source code.</span></span>  

| <span data-ttu-id="51d98-387">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="51d98-387">Properties</span></span> | <span data-ttu-id="51d98-388">Typ</span><span class="sxs-lookup"><span data-stu-id="51d98-388">Type</span></span> | <span data-ttu-id="51d98-389">Details</span><span class="sxs-lookup"><span data-stu-id="51d98-389">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="51d98-390">scriptId</span><span class="sxs-lookup"><span data-stu-id="51d98-390">scriptId</span></span> | [<span data-ttu-id="51d98-391">Runtime.ScriptId</span><span class="sxs-lookup"><span data-stu-id="51d98-391">Runtime.ScriptId</span></span>](./runtime.md#scriptid) | <span data-ttu-id="51d98-392">Skript-ID, wie in der `Debugger.scriptParsed` angegeben.</span><span class="sxs-lookup"><span data-stu-id="51d98-392">Script identifier as reported in the `Debugger.scriptParsed`.</span></span> |  
| <span data-ttu-id="51d98-393">lineNumber</span><span class="sxs-lookup"><span data-stu-id="51d98-393">lineNumber</span></span> | `integer` | <span data-ttu-id="51d98-394">Zeilennummer im Skript \(0-basiert\).</span><span class="sxs-lookup"><span data-stu-id="51d98-394">Line number in the script \(0-based\).</span></span> |  
| <span data-ttu-id="51d98-395">columnNumber \(optional\)</span><span class="sxs-lookup"><span data-stu-id="51d98-395">columnNumber \(optional\)</span></span> | `integer` | <span data-ttu-id="51d98-396">Spaltennummer im Skript \(0-basiert\).</span><span class="sxs-lookup"><span data-stu-id="51d98-396">Column number in the script \(0-based\).</span></span> |  
| <span data-ttu-id="51d98-397">msLength</span><span class="sxs-lookup"><span data-stu-id="51d98-397">msLength</span></span> | `integer` | <span data-ttu-id="51d98-398">Microsoft: Länge des Codes \(d. h. Anzahl der Zeichen\) in diesem Aufrufrahmen.</span><span class="sxs-lookup"><span data-stu-id="51d98-398">Microsoft:  Length of code \(i.e. number of characters\) at this call frame.</span></span> |  
| <span data-ttu-id="51d98-399">Typ \(optional\)</span><span class="sxs-lookup"><span data-stu-id="51d98-399">type \(optional\)</span></span> | `string` | <span data-ttu-id="51d98-400">Zulässige Werte: debuggerStatement, call, return.</span><span class="sxs-lookup"><span data-stu-id="51d98-400">Allowed values: debuggerStatement, call, return.</span></span> |  

---  

### <a name="callframe-object"></a><span data-ttu-id="51d98-401">CallFrame-Objekt</span><span class="sxs-lookup"><span data-stu-id="51d98-401">CallFrame object</span></span>  

<a name="callframe"></a>  

<span data-ttu-id="51d98-402">JavaScript-Aufrufrahmen.</span><span class="sxs-lookup"><span data-stu-id="51d98-402">JavaScript call frame.</span></span> <span data-ttu-id="51d98-403">Array von Anrufframes bilden die Aufrufliste.</span><span class="sxs-lookup"><span data-stu-id="51d98-403">Array of call frames form the call stack.</span></span>  

| <span data-ttu-id="51d98-404">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="51d98-404">Properties</span></span> | <span data-ttu-id="51d98-405">Typ</span><span class="sxs-lookup"><span data-stu-id="51d98-405">Type</span></span> | <span data-ttu-id="51d98-406">Details</span><span class="sxs-lookup"><span data-stu-id="51d98-406">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="51d98-407">callFrameId</span><span class="sxs-lookup"><span data-stu-id="51d98-407">callFrameId</span></span> | [<span data-ttu-id="51d98-408">CallFrameId</span><span class="sxs-lookup"><span data-stu-id="51d98-408">CallFrameId</span></span>](#callframeid) | <span data-ttu-id="51d98-409">Anrufrahmen-ID.</span><span class="sxs-lookup"><span data-stu-id="51d98-409">Call frame identifier.</span></span>  <span data-ttu-id="51d98-410">Dieser Bezeichner ist nur gültig, wenn der Debugger angehalten wird.</span><span class="sxs-lookup"><span data-stu-id="51d98-410">This identifier is only valid while the debugger is paused.</span></span> |  
| <span data-ttu-id="51d98-411">functionName</span><span class="sxs-lookup"><span data-stu-id="51d98-411">functionName</span></span> | `string` | <span data-ttu-id="51d98-412">Name der für diesen Aufrufrahmen aufgerufenen JavaScript-Funktion.</span><span class="sxs-lookup"><span data-stu-id="51d98-412">Name of the JavaScript function called on this call frame.</span></span> |  
| <span data-ttu-id="51d98-413">functionLocation \(optional\)</span><span class="sxs-lookup"><span data-stu-id="51d98-413">functionLocation \(optional\)</span></span> | [<span data-ttu-id="51d98-414">Ort</span><span class="sxs-lookup"><span data-stu-id="51d98-414">Location</span></span>](#location) | <span data-ttu-id="51d98-415">**Experimental**.</span><span class="sxs-lookup"><span data-stu-id="51d98-415">**Experimental**.</span></span>  <span data-ttu-id="51d98-416">Speicherort im Quellcode.</span><span class="sxs-lookup"><span data-stu-id="51d98-416">Location in the source code.</span></span> |  
| <span data-ttu-id="51d98-417">location</span><span class="sxs-lookup"><span data-stu-id="51d98-417">location</span></span> | [<span data-ttu-id="51d98-418">Ort</span><span class="sxs-lookup"><span data-stu-id="51d98-418">Location</span></span>](#location) | <span data-ttu-id="51d98-419">Speicherort im Quellcode.</span><span class="sxs-lookup"><span data-stu-id="51d98-419">Location in the source code.</span></span> |  
| <span data-ttu-id="51d98-420">URL</span><span class="sxs-lookup"><span data-stu-id="51d98-420">url</span></span> | `string` | <span data-ttu-id="51d98-421">Name oder URL des JavaScript-Skripts.</span><span class="sxs-lookup"><span data-stu-id="51d98-421">JavaScript script name or url.</span></span> |  
| <span data-ttu-id="51d98-422">scopeChain</span><span class="sxs-lookup"><span data-stu-id="51d98-422">scopeChain</span></span> | [<span data-ttu-id="51d98-423">Scope[]</span><span class="sxs-lookup"><span data-stu-id="51d98-423">Scope[]</span></span>](#scope) | <span data-ttu-id="51d98-424">Bereichskette für diesen Anrufrahmen.</span><span class="sxs-lookup"><span data-stu-id="51d98-424">Scope chain for this call frame.</span></span> |  
| <span data-ttu-id="51d98-425">this</span><span class="sxs-lookup"><span data-stu-id="51d98-425">this</span></span> | [<span data-ttu-id="51d98-426">Runtime.RemoteObject</span><span class="sxs-lookup"><span data-stu-id="51d98-426">Runtime.RemoteObject</span></span>](./runtime.md#remoteobject) | `this` <span data-ttu-id="51d98-427">-Objekt für diesen Aufrufrahmen.</span><span class="sxs-lookup"><span data-stu-id="51d98-427">object for this call frame.</span></span> |  
| <span data-ttu-id="51d98-428">returnValue \(optional\)</span><span class="sxs-lookup"><span data-stu-id="51d98-428">returnValue \(optional\)</span></span> | [<span data-ttu-id="51d98-429">Runtime.RemoteObject</span><span class="sxs-lookup"><span data-stu-id="51d98-429">Runtime.RemoteObject</span></span>](./runtime.md#remoteobject) | <span data-ttu-id="51d98-430">Der zurückgegebene Wert, wenn sich die Funktion am Rückgabepunkt befindet.</span><span class="sxs-lookup"><span data-stu-id="51d98-430">The value being returned, if the function is at return point.</span></span> |  

---  

### <a name="scope-object"></a><span data-ttu-id="51d98-431">Scope-Objekt</span><span class="sxs-lookup"><span data-stu-id="51d98-431">Scope object</span></span>  

<a name="scope"></a>  

<span data-ttu-id="51d98-432">Bereichsbeschreibung.</span><span class="sxs-lookup"><span data-stu-id="51d98-432">Scope description.</span></span>  

| <span data-ttu-id="51d98-433">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="51d98-433">Properties</span></span> | <span data-ttu-id="51d98-434">Typ</span><span class="sxs-lookup"><span data-stu-id="51d98-434">Type</span></span> | <span data-ttu-id="51d98-435">Details</span><span class="sxs-lookup"><span data-stu-id="51d98-435">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="51d98-436">Typ</span><span class="sxs-lookup"><span data-stu-id="51d98-436">type</span></span> | `string` | <span data-ttu-id="51d98-437">Bereichstyp.</span><span class="sxs-lookup"><span data-stu-id="51d98-437">Scope type.</span></span>  <span data-ttu-id="51d98-438">Zulässige Werte:  `global` , , , , , , , , `local` , `with` `closure` `catch` `block` `script` `eval` `module` und</span><span class="sxs-lookup"><span data-stu-id="51d98-438">Allowed values:  `global`, `local`, `with`, `closure`, `catch`, `block`, `script`, `eval`, `module`, and</span></span> `return` |  
| <span data-ttu-id="51d98-439">Objekt</span><span class="sxs-lookup"><span data-stu-id="51d98-439">object</span></span> | [<span data-ttu-id="51d98-440">Runtime.RemoteObject</span><span class="sxs-lookup"><span data-stu-id="51d98-440">Runtime.RemoteObject</span></span>](./runtime.md#remoteobject) | <span data-ttu-id="51d98-441">Objekt, das den Bereich darstellt.</span><span class="sxs-lookup"><span data-stu-id="51d98-441">Object representing the scope.</span></span>  <span data-ttu-id="51d98-442">Für und Bereiche stellt sie das tatsächliche Objekt dar. Für die restlichen Bereiche ist es ein künstliches transientes Objekt, das Bereichsvariablen als `global` `with` Eigenschaften aufzählt.</span><span class="sxs-lookup"><span data-stu-id="51d98-442">For `global` and `with` scopes it represents the actual object; for the rest of the scopes, it is artificial transient object enumerating scope variables as its properties.</span></span> |  
| <span data-ttu-id="51d98-443">Name \(optional\)</span><span class="sxs-lookup"><span data-stu-id="51d98-443">name \(optional\)</span></span> | `string` | &nbsp; |  
| <span data-ttu-id="51d98-444">startLocation \(optional\)</span><span class="sxs-lookup"><span data-stu-id="51d98-444">startLocation \(optional\)</span></span> | [<span data-ttu-id="51d98-445">Ort</span><span class="sxs-lookup"><span data-stu-id="51d98-445">Location</span></span>](#location) | <span data-ttu-id="51d98-446">Speicherort im Quellcode, an dem der Bereich beginnt.</span><span class="sxs-lookup"><span data-stu-id="51d98-446">Location in the source code where scope starts.</span></span> |  
| <span data-ttu-id="51d98-447">endLocation \(optional\)</span><span class="sxs-lookup"><span data-stu-id="51d98-447">endLocation \(optional\)</span></span> | [<span data-ttu-id="51d98-448">Ort</span><span class="sxs-lookup"><span data-stu-id="51d98-448">Location</span></span>](#location) | <span data-ttu-id="51d98-449">Speicherort im Quellcode, an dem der Bereich endet.</span><span class="sxs-lookup"><span data-stu-id="51d98-449">Location in the source code where scope ends.</span></span> |  

---  

## <a name="dependencies"></a><span data-ttu-id="51d98-450">Abhängigkeiten</span><span class="sxs-lookup"><span data-stu-id="51d98-450">Dependencies</span></span>  

[<span data-ttu-id="51d98-451">Laufzeit</span><span class="sxs-lookup"><span data-stu-id="51d98-451">Runtime</span></span>](./runtime.md)  
