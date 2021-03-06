---
description: DevTools Protocol Version 0.1 (EdgeHTML)-Referenz für die Laufzeitdomäne.  Die Laufzeitdomäne macht die JavaScript-Laufzeit über Remoteauswertungs- und Spiegelobjekte verfügbar.  Auswertungsergebnisse werden als Spiegelobjekt zurückgegeben, das Objekttyp, Zeichenfolgendarstellung und eindeutigen Bezeichner verfügbar macht, die für weitere Objektverweise verwendet werden können.  Originalobjekte werden im Arbeitsspeicher verwaltet, es sei denn, sie werden explizit freigegeben.
title: Runtime Domain - DevTools Protocol Version 0.1 (EdgeHTML)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/03/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.custom: seodec18
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: d9aa87c1c289452844ef3442811f84881fc752b4
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "11397692"
---
# <a name="runtime-domain---devtools-protocol-version-01-edgehtml"></a><span data-ttu-id="ee7e1-106">Runtime Domain - DevTools Protocol Version 0.1 (EdgeHTML)</span><span class="sxs-lookup"><span data-stu-id="ee7e1-106">Runtime Domain - DevTools Protocol Version 0.1 (EdgeHTML)</span></span>  

<span data-ttu-id="ee7e1-107">Die Laufzeitdomäne macht die JavaScript-Laufzeit über Remoteauswertungs- und Spiegelobjekte verfügbar.</span><span class="sxs-lookup"><span data-stu-id="ee7e1-107">Runtime domain exposes JavaScript runtime by means of remote evaluation and mirror objects.</span></span>  <span data-ttu-id="ee7e1-108">Auswertungsergebnisse werden als Spiegelobjekt zurückgegeben, das Objekttyp, Zeichenfolgendarstellung und eindeutigen Bezeichner verfügbar macht, die für weitere Objektverweise verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="ee7e1-108">Evaluation results are returned as mirror object that expose object type, string representation and unique identifier that can be used for further object reference.</span></span>  <span data-ttu-id="ee7e1-109">Originalobjekte werden im Arbeitsspeicher verwaltet, es sei denn, sie werden explizit freigegeben.</span><span class="sxs-lookup"><span data-stu-id="ee7e1-109">Original objects are maintained in memory unless they are either explicitly released.</span></span>  

| <span data-ttu-id="ee7e1-110">Klassifizierung</span><span class="sxs-lookup"><span data-stu-id="ee7e1-110">Classification</span></span> | <span data-ttu-id="ee7e1-111">Member</span><span class="sxs-lookup"><span data-stu-id="ee7e1-111">Members</span></span> |  
|:--- |:--- |  
| [<span data-ttu-id="ee7e1-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="ee7e1-112">Methods</span></span>](#methods) | <span data-ttu-id="ee7e1-113">[enable](#enable), [disable](#disable), [evaluate](#evaluate), [callFunctionOn](#callfunctionon), [getProperties](#getproperties)</span><span class="sxs-lookup"><span data-stu-id="ee7e1-113">[enable](#enable), [disable](#disable), [evaluate](#evaluate), [callFunctionOn](#callfunctionon), [getProperties](#getproperties)</span></span> |  
| [<span data-ttu-id="ee7e1-114">Veranstaltungen</span><span class="sxs-lookup"><span data-stu-id="ee7e1-114">Events</span></span>](#events) | <span data-ttu-id="ee7e1-115">[executionContextsCleared](#executioncontextscleared), [exceptionThrown](#exceptionthrown)</span><span class="sxs-lookup"><span data-stu-id="ee7e1-115">[executionContextsCleared](#executioncontextscleared), [exceptionThrown](#exceptionthrown)</span></span> |  
| [<span data-ttu-id="ee7e1-116">Typen</span><span class="sxs-lookup"><span data-stu-id="ee7e1-116">Types</span></span>](#types) | <span data-ttu-id="ee7e1-117">[ScriptId](#scriptid), [RemoteObjectId](#remoteobjectid), [UnserializableValue](#unserializablevalue), [RemoteObject](#remoteobject), [PropertyDescriptor](#propertydescriptor), [CallArgument](#callargument), [ExecutionContextId](#executioncontextid), [ExceptionDetails](#exceptiondetails), [Timestamp](#timestamp), [CallFrame](#callframe), [StackTrace](#stacktrace)</span><span class="sxs-lookup"><span data-stu-id="ee7e1-117">[ScriptId](#scriptid), [RemoteObjectId](#remoteobjectid), [UnserializableValue](#unserializablevalue), [RemoteObject](#remoteobject), [PropertyDescriptor](#propertydescriptor), [CallArgument](#callargument), [ExecutionContextId](#executioncontextid), [ExceptionDetails](#exceptiondetails), [Timestamp](#timestamp), [CallFrame](#callframe), [StackTrace](#stacktrace)</span></span> |  

## <a name="methods"></a><span data-ttu-id="ee7e1-118">Methoden</span><span class="sxs-lookup"><span data-stu-id="ee7e1-118">Methods</span></span>  

### <a name="enable"></a><span data-ttu-id="ee7e1-119">Aktivieren</span><span class="sxs-lookup"><span data-stu-id="ee7e1-119">enable</span></span>  

<span data-ttu-id="ee7e1-120">Aktiviert die Berichterstellung des `executionContextsCleared` Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="ee7e1-120">Enables reporting of the `executionContextsCleared` event.</span></span>  

&nbsp;  

---  

### <a name="disable"></a><span data-ttu-id="ee7e1-121">Deaktivieren </span><span class="sxs-lookup"><span data-stu-id="ee7e1-121">disable</span></span>  

<span data-ttu-id="ee7e1-122">Deaktiviert die Berichterstellung für das `executionContextsCleared` Ereignis.</span><span class="sxs-lookup"><span data-stu-id="ee7e1-122">Disables reporting of the `executionContextsCleared` event.</span></span>  

&nbsp;  

---  

### <a name="evaluate"></a><span data-ttu-id="ee7e1-123">evaluate</span><span class="sxs-lookup"><span data-stu-id="ee7e1-123">evaluate</span></span>  

<span data-ttu-id="ee7e1-124">Wertet Ausdruck für globales Objekt aus.</span><span class="sxs-lookup"><span data-stu-id="ee7e1-124">Evaluates expression on global object.</span></span>  

| <span data-ttu-id="ee7e1-125">Parameter</span><span class="sxs-lookup"><span data-stu-id="ee7e1-125">Parameters</span></span> | <span data-ttu-id="ee7e1-126">Typ</span><span class="sxs-lookup"><span data-stu-id="ee7e1-126">Type</span></span> | <span data-ttu-id="ee7e1-127">Details</span><span class="sxs-lookup"><span data-stu-id="ee7e1-127">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="ee7e1-128">Ausdruck</span><span class="sxs-lookup"><span data-stu-id="ee7e1-128">expression</span></span> | `string` | <span data-ttu-id="ee7e1-129">Ausdruck, der ausgewertet werden soll.</span><span class="sxs-lookup"><span data-stu-id="ee7e1-129">Expression to evaluate.</span></span> |  
| <span data-ttu-id="ee7e1-130">silent \(optional\)</span><span class="sxs-lookup"><span data-stu-id="ee7e1-130">silent \(optional\)</span></span> | `boolean` | <span data-ttu-id="ee7e1-131">Im automatischen Modus werden ausnahmen, die während der Auswertung ausgelöst werden, nicht gemeldet und die Ausführung nicht angehalten.</span><span class="sxs-lookup"><span data-stu-id="ee7e1-131">In silent mode exceptions thrown during evaluation are not reported and do not pause execution.</span></span>  <span data-ttu-id="ee7e1-132">Überschreibt `setPauseOnException` den Status.</span><span class="sxs-lookup"><span data-stu-id="ee7e1-132">Overrides `setPauseOnException` state.</span></span> |  
| <span data-ttu-id="ee7e1-133">contextId \(optional\)</span><span class="sxs-lookup"><span data-stu-id="ee7e1-133">contextId \(optional\)</span></span> | [<span data-ttu-id="ee7e1-134">ExecutionContextId</span><span class="sxs-lookup"><span data-stu-id="ee7e1-134">ExecutionContextId</span></span>](#executioncontextid) | <span data-ttu-id="ee7e1-135">Gibt an, in welchem Ausführungskontext eine Auswertung ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="ee7e1-135">Specifies in which execution context to perform evaluation.</span></span>  <span data-ttu-id="ee7e1-136">Wenn der Parameter nicht angegeben wird, wird die Auswertung im Kontext der überprüften Seite durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="ee7e1-136">If the parameter is omitted the evaluation will be performed in the context of the inspected page.</span></span> |  
| <span data-ttu-id="ee7e1-137">returnByValue \(optional\)</span><span class="sxs-lookup"><span data-stu-id="ee7e1-137">returnByValue \(optional\)</span></span> | `boolean` | <span data-ttu-id="ee7e1-138">Gibt an, ob es sich bei dem Ergebnis um ein JSON-Objekt handelt, das per Wert gesendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="ee7e1-138">Whether the result is expected to be a JSON object that should be sent by value.</span></span> |  
| <span data-ttu-id="ee7e1-139">awaitPromise \(optional\)</span><span class="sxs-lookup"><span data-stu-id="ee7e1-139">awaitPromise \(optional\)</span></span> | `boolean` | <span data-ttu-id="ee7e1-140">Ob die Ausführung für den resultierenden Wert und die Rückgabe nach der erwarteten Zusage `await` ausgeführt werden soll, wird aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="ee7e1-140">Whether execution should `await` for resulting value and return once awaited promise is resolved.</span></span> |  

| <span data-ttu-id="ee7e1-141">Gibt zurück</span><span class="sxs-lookup"><span data-stu-id="ee7e1-141">Returns</span></span> | <span data-ttu-id="ee7e1-142">Typ</span><span class="sxs-lookup"><span data-stu-id="ee7e1-142">Type</span></span> | <span data-ttu-id="ee7e1-143">Details</span><span class="sxs-lookup"><span data-stu-id="ee7e1-143">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="ee7e1-144">result</span><span class="sxs-lookup"><span data-stu-id="ee7e1-144">result</span></span> | [<span data-ttu-id="ee7e1-145">RemoteObject</span><span class="sxs-lookup"><span data-stu-id="ee7e1-145">RemoteObject</span></span>](#remoteobject) | <span data-ttu-id="ee7e1-146">Bewertungsergebnis.</span><span class="sxs-lookup"><span data-stu-id="ee7e1-146">Evaluation result.</span></span> |  

---  

### <a name="callfunctionon"></a><span data-ttu-id="ee7e1-147">callFunctionOn</span><span class="sxs-lookup"><span data-stu-id="ee7e1-147">callFunctionOn</span></span>  

<span data-ttu-id="ee7e1-148">Aufrufe funktionieren mit einer angegebenen Deklaration für das angegebene Objekt.</span><span class="sxs-lookup"><span data-stu-id="ee7e1-148">Calls function with given declaration on the given object.</span></span>  <span data-ttu-id="ee7e1-149">Die Objektgruppe des Ergebnisses wird vom Zielobjekt geerbt.</span><span class="sxs-lookup"><span data-stu-id="ee7e1-149">Object group of the result is inherited from the target object.</span></span>  

| <span data-ttu-id="ee7e1-150">Parameter</span><span class="sxs-lookup"><span data-stu-id="ee7e1-150">Parameters</span></span> | <span data-ttu-id="ee7e1-151">Typ</span><span class="sxs-lookup"><span data-stu-id="ee7e1-151">Type</span></span> | <span data-ttu-id="ee7e1-152">Details</span><span class="sxs-lookup"><span data-stu-id="ee7e1-152">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="ee7e1-153">functionDeclaration</span><span class="sxs-lookup"><span data-stu-id="ee7e1-153">functionDeclaration</span></span> | `string` | <span data-ttu-id="ee7e1-154">Deklaration der zu aufrufende Funktion.</span><span class="sxs-lookup"><span data-stu-id="ee7e1-154">Declaration of the function to call.</span></span> |  
| <span data-ttu-id="ee7e1-155">objectId \(optional\)</span><span class="sxs-lookup"><span data-stu-id="ee7e1-155">objectId \(optional\)</span></span> | [<span data-ttu-id="ee7e1-156">RemoteObjectId</span><span class="sxs-lookup"><span data-stu-id="ee7e1-156">RemoteObjectId</span></span>](#remoteobjectid) | <span data-ttu-id="ee7e1-157">Bezeichner des Objekts, für das die Funktion aufruft.</span><span class="sxs-lookup"><span data-stu-id="ee7e1-157">Identifier of the object to call function on.</span></span>  <span data-ttu-id="ee7e1-158">Entweder `objectId` oder sollte angegeben `executionContextId` werden.</span><span class="sxs-lookup"><span data-stu-id="ee7e1-158">Either `objectId` or `executionContextId` should be specified.</span></span>  <span data-ttu-id="ee7e1-159">objectId muss aus der Runtime.evaluate()-Funktion kommen.</span><span class="sxs-lookup"><span data-stu-id="ee7e1-159">objectId must be from the Runtime.evaluate() function.</span></span> |  
| <span data-ttu-id="ee7e1-160">Argumente \(optional\)</span><span class="sxs-lookup"><span data-stu-id="ee7e1-160">arguments \(optional\)</span></span> | [<span data-ttu-id="ee7e1-161">CallArgument[]</span><span class="sxs-lookup"><span data-stu-id="ee7e1-161">CallArgument[]</span></span>](#callargument) | <span data-ttu-id="ee7e1-162">Aufrufargumente.</span><span class="sxs-lookup"><span data-stu-id="ee7e1-162">Call arguments.</span></span>  <span data-ttu-id="ee7e1-163">Alle Aufrufargumente müssen zur gleichen JavaScript-Welt wie das Zielobjekt gehören.</span><span class="sxs-lookup"><span data-stu-id="ee7e1-163">All call arguments must belong to the same JavaScript world as the target object.</span></span> |  
| <span data-ttu-id="ee7e1-164">silent \(optional\)</span><span class="sxs-lookup"><span data-stu-id="ee7e1-164">silent \(optional\)</span></span> | `boolean` | <span data-ttu-id="ee7e1-165">Im automatischen Modus werden ausnahmen, die während der Auswertung ausgelöst werden, nicht gemeldet und die Ausführung nicht angehalten.</span><span class="sxs-lookup"><span data-stu-id="ee7e1-165">In silent mode exceptions thrown during evaluation are not reported and do not pause execution.</span></span>  <span data-ttu-id="ee7e1-166">Überschreibt `setPauseOnException` den Status.</span><span class="sxs-lookup"><span data-stu-id="ee7e1-166">Overrides `setPauseOnException` state.</span></span> |  
| <span data-ttu-id="ee7e1-167">returnByValue \(optional\)</span><span class="sxs-lookup"><span data-stu-id="ee7e1-167">returnByValue \(optional\)</span></span> | `boolean` | <span data-ttu-id="ee7e1-168">Gibt an, ob es sich bei dem Ergebnis um ein JSON-Objekt handelt, das per Wert gesendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="ee7e1-168">Whether the result is expected to be a JSON object which should be sent by value.</span></span> |  
| <span data-ttu-id="ee7e1-169">awaitPromise \(optional\)</span><span class="sxs-lookup"><span data-stu-id="ee7e1-169">awaitPromise \(optional\)</span></span> | `boolean` | <span data-ttu-id="ee7e1-170">Ob die Ausführung für den resultierenden Wert und die Rückgabe nach der erwarteten Zusage `await` ausgeführt werden soll, wird aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="ee7e1-170">Whether execution should `await` for resulting value and return once awaited promise is resolved.</span></span> |  

| <span data-ttu-id="ee7e1-171">Gibt zurück</span><span class="sxs-lookup"><span data-stu-id="ee7e1-171">Returns</span></span> | <span data-ttu-id="ee7e1-172">Typ</span><span class="sxs-lookup"><span data-stu-id="ee7e1-172">Type</span></span> | <span data-ttu-id="ee7e1-173">Details</span><span class="sxs-lookup"><span data-stu-id="ee7e1-173">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="ee7e1-174">result</span><span class="sxs-lookup"><span data-stu-id="ee7e1-174">result</span></span> | [<span data-ttu-id="ee7e1-175">RemoteObject</span><span class="sxs-lookup"><span data-stu-id="ee7e1-175">RemoteObject</span></span>](#remoteobject) | <span data-ttu-id="ee7e1-176">Anrufergebnis.</span><span class="sxs-lookup"><span data-stu-id="ee7e1-176">Call result.</span></span> |  

---  

### <a name="getproperties"></a><span data-ttu-id="ee7e1-177">getProperties</span><span class="sxs-lookup"><span data-stu-id="ee7e1-177">getProperties</span></span>  

<span data-ttu-id="ee7e1-178">Gibt Eigenschaften eines bestimmten Objekts zurück.</span><span class="sxs-lookup"><span data-stu-id="ee7e1-178">Returns properties of a given object.</span></span>  <span data-ttu-id="ee7e1-179">Die Objektgruppe des Ergebnisses wird vom Zielobjekt geerbt.</span><span class="sxs-lookup"><span data-stu-id="ee7e1-179">Object group of the result is inherited from the target object.</span></span>  

| <span data-ttu-id="ee7e1-180">Parameter</span><span class="sxs-lookup"><span data-stu-id="ee7e1-180">Parameters</span></span> | <span data-ttu-id="ee7e1-181">Typ</span><span class="sxs-lookup"><span data-stu-id="ee7e1-181">Type</span></span> | <span data-ttu-id="ee7e1-182">Details</span><span class="sxs-lookup"><span data-stu-id="ee7e1-182">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="ee7e1-183">objectId</span><span class="sxs-lookup"><span data-stu-id="ee7e1-183">objectId</span></span> | [<span data-ttu-id="ee7e1-184">RemoteObjectId</span><span class="sxs-lookup"><span data-stu-id="ee7e1-184">RemoteObjectId</span></span>](#remoteobjectid) | <span data-ttu-id="ee7e1-185">Bezeichner des Objekts, für das Eigenschaften zurückgeben werden.</span><span class="sxs-lookup"><span data-stu-id="ee7e1-185">Identifier of the object to return properties for.</span></span>  `objectId` <span data-ttu-id="ee7e1-186">muss von der Funktion `Debugger.evaluateOnCallFrame()` sein.</span><span class="sxs-lookup"><span data-stu-id="ee7e1-186">must be from the `Debugger.evaluateOnCallFrame()` function.</span></span> |  
| <span data-ttu-id="ee7e1-187">ownProperties \(optional\)</span><span class="sxs-lookup"><span data-stu-id="ee7e1-187">ownProperties \(optional\)</span></span> | `boolean` | <span data-ttu-id="ee7e1-188">Wenn `true` , gibt Eigenschaften zurück, die nur zum Element selbst gehören, nicht zu seiner Prototypkette.</span><span class="sxs-lookup"><span data-stu-id="ee7e1-188">If `true`, returns properties belonging only to the element itself, not to its prototype chain.</span></span> |  
| <span data-ttu-id="ee7e1-189">accessorPropertiesOnly \(optional\)</span><span class="sxs-lookup"><span data-stu-id="ee7e1-189">accessorPropertiesOnly \(optional\)</span></span> | `boolean` | <span data-ttu-id="ee7e1-190">**Experimental**.</span><span class="sxs-lookup"><span data-stu-id="ee7e1-190">**Experimental**.</span></span>  <span data-ttu-id="ee7e1-191">Wenn `true` , gibt nur Accessoreigenschaften \(mit Getter/Setter\) zurück; interne Eigenschaften werden auch nicht zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="ee7e1-191">If `true`, returns accessor properties \(with getter/setter\) only; internal properties are not returned either.</span></span> |  

| <span data-ttu-id="ee7e1-192">Gibt zurück</span><span class="sxs-lookup"><span data-stu-id="ee7e1-192">Returns</span></span> | <span data-ttu-id="ee7e1-193">Typ</span><span class="sxs-lookup"><span data-stu-id="ee7e1-193">Type</span></span> | <span data-ttu-id="ee7e1-194">Details</span><span class="sxs-lookup"><span data-stu-id="ee7e1-194">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="ee7e1-195">result</span><span class="sxs-lookup"><span data-stu-id="ee7e1-195">result</span></span> | [<span data-ttu-id="ee7e1-196">PropertyDescriptor[]</span><span class="sxs-lookup"><span data-stu-id="ee7e1-196">PropertyDescriptor[]</span></span>](#propertydescriptor) | <span data-ttu-id="ee7e1-197">Objekteigenschaften.</span><span class="sxs-lookup"><span data-stu-id="ee7e1-197">Object properties.</span></span> |  

---  

## <a name="events"></a><span data-ttu-id="ee7e1-198">Veranstaltungen</span><span class="sxs-lookup"><span data-stu-id="ee7e1-198">Events</span></span>  

### <a name="executioncontextscleared"></a><span data-ttu-id="ee7e1-199">executionContextsCleared</span><span class="sxs-lookup"><span data-stu-id="ee7e1-199">executionContextsCleared</span></span>  

<span data-ttu-id="ee7e1-200">Wird ausgegeben, wenn alle executionContexts im Browser gelöscht wurden.</span><span class="sxs-lookup"><span data-stu-id="ee7e1-200">Issued when all executionContexts were cleared in browser.</span></span>  

&nbsp;  

---  

### <a name="exceptionthrown"></a><span data-ttu-id="ee7e1-201">exceptionThrown</span><span class="sxs-lookup"><span data-stu-id="ee7e1-201">exceptionThrown</span></span>  

<span data-ttu-id="ee7e1-202">Wird ausgegeben, wenn eine Ausnahme ausgelöst und nicht behandelt wurde.</span><span class="sxs-lookup"><span data-stu-id="ee7e1-202">Issued when exception was thrown and unhandled.</span></span>  

| <span data-ttu-id="ee7e1-203">Parameter</span><span class="sxs-lookup"><span data-stu-id="ee7e1-203">Parameters</span></span> | <span data-ttu-id="ee7e1-204">Typ</span><span class="sxs-lookup"><span data-stu-id="ee7e1-204">Type</span></span> | <span data-ttu-id="ee7e1-205">Details</span><span class="sxs-lookup"><span data-stu-id="ee7e1-205">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="ee7e1-206">zeitstempel</span><span class="sxs-lookup"><span data-stu-id="ee7e1-206">timestamp</span></span> | [<span data-ttu-id="ee7e1-207">Zeitstempel</span><span class="sxs-lookup"><span data-stu-id="ee7e1-207">Timestamp</span></span>](#timestamp) | <span data-ttu-id="ee7e1-208">Zeitstempel der Ausnahme.</span><span class="sxs-lookup"><span data-stu-id="ee7e1-208">Timestamp of the exception.</span></span> |  
| <span data-ttu-id="ee7e1-209">exceptionDetails</span><span class="sxs-lookup"><span data-stu-id="ee7e1-209">exceptionDetails</span></span> | [<span data-ttu-id="ee7e1-210">ExceptionDetails</span><span class="sxs-lookup"><span data-stu-id="ee7e1-210">ExceptionDetails</span></span>](#exceptiondetails) | &nbsp; |  

---  

## <a name="types"></a><span data-ttu-id="ee7e1-211">Typen</span><span class="sxs-lookup"><span data-stu-id="ee7e1-211">Types</span></span>  

### <a name="scriptid-string"></a><span data-ttu-id="ee7e1-212">ScriptId-Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="ee7e1-212">ScriptId string</span></span>  

<a name="scriptid"></a>  

<span data-ttu-id="ee7e1-213">Eindeutige Skript-ID.</span><span class="sxs-lookup"><span data-stu-id="ee7e1-213">Unique script identifier.</span></span>  

&nbsp;  

---  

### <a name="remoteobjectid-string"></a><span data-ttu-id="ee7e1-214">RemoteObjectId-Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="ee7e1-214">RemoteObjectId string</span></span>  

<a name="remoteobjectid"></a>  

<span data-ttu-id="ee7e1-215">Eindeutiger Objektbezeichner.</span><span class="sxs-lookup"><span data-stu-id="ee7e1-215">Unique object identifier.</span></span>  

&nbsp;  

---  

### <a name="unserializablevalue-string"></a><span data-ttu-id="ee7e1-216">Zeichenfolge UnserializableValue</span><span class="sxs-lookup"><span data-stu-id="ee7e1-216">UnserializableValue string</span></span>  

<a name="unserializablevalue"></a>  

<span data-ttu-id="ee7e1-217">Grundtypwert, der nicht JSON-stringified sein kann.</span><span class="sxs-lookup"><span data-stu-id="ee7e1-217">Primitive value which cannot be JSON-stringified.</span></span>  

##### <a name="allowed-values"></a><span data-ttu-id="ee7e1-218">Zulässige Werte</span><span class="sxs-lookup"><span data-stu-id="ee7e1-218">Allowed Values</span></span>  

`Infinity`<span data-ttu-id="ee7e1-219">, `NaN`, `-Infinity`,</span><span class="sxs-lookup"><span data-stu-id="ee7e1-219">, `NaN`, `-Infinity`,</span></span> `-0`  

---  

### <a name="remoteobject-object"></a><span data-ttu-id="ee7e1-220">RemoteObject-Objekt</span><span class="sxs-lookup"><span data-stu-id="ee7e1-220">RemoteObject object</span></span>  

<a name="remoteobject"></a>  

<span data-ttu-id="ee7e1-221">Mirror-Objekt, das auf das ursprüngliche JavaScript-Objekt referenziert.</span><span class="sxs-lookup"><span data-stu-id="ee7e1-221">Mirror object referencing original JavaScript object.</span></span>  

| <span data-ttu-id="ee7e1-222">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ee7e1-222">Properties</span></span> | <span data-ttu-id="ee7e1-223">Typ</span><span class="sxs-lookup"><span data-stu-id="ee7e1-223">Type</span></span> | <span data-ttu-id="ee7e1-224">Details</span><span class="sxs-lookup"><span data-stu-id="ee7e1-224">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="ee7e1-225">Typ</span><span class="sxs-lookup"><span data-stu-id="ee7e1-225">type</span></span> | `string` | <span data-ttu-id="ee7e1-226">Objekttyp.</span><span class="sxs-lookup"><span data-stu-id="ee7e1-226">Object type.</span></span>  <span data-ttu-id="ee7e1-227">Zulässige Werte:  `object` , , , , , `function` `undefined` `string` `number` `boolean` und</span><span class="sxs-lookup"><span data-stu-id="ee7e1-227">Allowed values:  `object`, `function`, `undefined`, `string`, `number`, `boolean`, and</span></span> `symbol` |  
| <span data-ttu-id="ee7e1-228">subtype \(optional\)</span><span class="sxs-lookup"><span data-stu-id="ee7e1-228">subtype \(optional\)</span></span> | `string` | <span data-ttu-id="ee7e1-229">Objektuntertyphinweis.</span><span class="sxs-lookup"><span data-stu-id="ee7e1-229">Object subtype hint.</span></span>  <span data-ttu-id="ee7e1-230">Nur für `object` Typwerte angegeben.</span><span class="sxs-lookup"><span data-stu-id="ee7e1-230">Specified for `object` type values only.</span></span>  <span data-ttu-id="ee7e1-231">Zulässige Werte:  `null` `error` , und</span><span class="sxs-lookup"><span data-stu-id="ee7e1-231">Allowed values:  `null`, `error`, and</span></span> `promise` |  
| <span data-ttu-id="ee7e1-232">className \(optional\)</span><span class="sxs-lookup"><span data-stu-id="ee7e1-232">className \(optional\)</span></span> | `string` | <span data-ttu-id="ee7e1-233">Objektklasse \(constructor\) name.</span><span class="sxs-lookup"><span data-stu-id="ee7e1-233">Object class \(constructor\) name.</span></span>  <span data-ttu-id="ee7e1-234">Nur für `object` Typwerte angegeben.</span><span class="sxs-lookup"><span data-stu-id="ee7e1-234">Specified for `object` type values only.</span></span> |  
| <span data-ttu-id="ee7e1-235">Wert \(optional\)</span><span class="sxs-lookup"><span data-stu-id="ee7e1-235">value \(optional\)</span></span> | `any` | <span data-ttu-id="ee7e1-236">Remoteobjektwert bei Grundwerten oder JSON-Werten \(wenn er angefordert wurde\).</span><span class="sxs-lookup"><span data-stu-id="ee7e1-236">Remote object value in case of primitive values or JSON values \(if it was requested\).</span></span> |  
| <span data-ttu-id="ee7e1-237">unserializableValue \(optional\)</span><span class="sxs-lookup"><span data-stu-id="ee7e1-237">unserializableValue \(optional\)</span></span> | [<span data-ttu-id="ee7e1-238">UnserializableValue</span><span class="sxs-lookup"><span data-stu-id="ee7e1-238">UnserializableValue</span></span>](#unserializablevalue) | <span data-ttu-id="ee7e1-239">Primitiver Wert, der nicht JSON-stringified sein kann, verfügt nicht `value` über , ruft aber diese Eigenschaft ab.</span><span class="sxs-lookup"><span data-stu-id="ee7e1-239">Primitive value which can not be JSON-stringified does not have `value`, but gets this property.</span></span> |  
| <span data-ttu-id="ee7e1-240">beschreibung \(optional\)</span><span class="sxs-lookup"><span data-stu-id="ee7e1-240">description \(optional\)</span></span> | `string` | <span data-ttu-id="ee7e1-241">Zeichenfolgendarstellung des Objekts.</span><span class="sxs-lookup"><span data-stu-id="ee7e1-241">String representation of the object.</span></span> |  
| <span data-ttu-id="ee7e1-242">objectId \(optional\)</span><span class="sxs-lookup"><span data-stu-id="ee7e1-242">objectId \(optional\)</span></span> | [<span data-ttu-id="ee7e1-243">RemoteObjectId</span><span class="sxs-lookup"><span data-stu-id="ee7e1-243">RemoteObjectId</span></span>](#remoteobjectid) | <span data-ttu-id="ee7e1-244">Eindeutiger Objektbezeichner \(für nicht primitive Werte\).</span><span class="sxs-lookup"><span data-stu-id="ee7e1-244">Unique object identifier \(for non-primitive values\).</span></span> |  
| <span data-ttu-id="ee7e1-245">msDebuggerPropertyId \(optional\)</span><span class="sxs-lookup"><span data-stu-id="ee7e1-245">msDebuggerPropertyId \(optional\)</span></span> | `string` | <span data-ttu-id="ee7e1-246">**Experimental**.</span><span class="sxs-lookup"><span data-stu-id="ee7e1-246">**Experimental**.</span></span>  <span data-ttu-id="ee7e1-247">Microsoft: Die zugeordnete Debuggereigenschafts-ID für dieses Objekt.</span><span class="sxs-lookup"><span data-stu-id="ee7e1-247">Microsoft:  The associated debugger property ID for this object.</span></span> |  

---  

### <a name="propertydescriptor-object"></a><span data-ttu-id="ee7e1-248">PropertyDescriptor-Objekt</span><span class="sxs-lookup"><span data-stu-id="ee7e1-248">PropertyDescriptor object</span></span>  

<a name="propertydescriptor"></a>  

<span data-ttu-id="ee7e1-249">Objekteigenschaftsdeskriptor.</span><span class="sxs-lookup"><span data-stu-id="ee7e1-249">Object property descriptor.</span></span>  

| <span data-ttu-id="ee7e1-250">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ee7e1-250">Properties</span></span> | <span data-ttu-id="ee7e1-251">Typ</span><span class="sxs-lookup"><span data-stu-id="ee7e1-251">Type</span></span> | <span data-ttu-id="ee7e1-252">Details</span><span class="sxs-lookup"><span data-stu-id="ee7e1-252">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="ee7e1-253">name</span><span class="sxs-lookup"><span data-stu-id="ee7e1-253">name</span></span> | `string` | <span data-ttu-id="ee7e1-254">Eigenschaftenname oder Symbolbeschreibung.</span><span class="sxs-lookup"><span data-stu-id="ee7e1-254">Property name or symbol description.</span></span> |  
| <span data-ttu-id="ee7e1-255">Wert \(optional\)</span><span class="sxs-lookup"><span data-stu-id="ee7e1-255">value \(optional\)</span></span> | [<span data-ttu-id="ee7e1-256">RemoteObject</span><span class="sxs-lookup"><span data-stu-id="ee7e1-256">RemoteObject</span></span>](#remoteobject) | <span data-ttu-id="ee7e1-257">Der Wert, der der Eigenschaft zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="ee7e1-257">The value associated with the property.</span></span> |  
| <span data-ttu-id="ee7e1-258">Schreibbar \(optional\)</span><span class="sxs-lookup"><span data-stu-id="ee7e1-258">writable \(optional\)</span></span> | `boolean` | `True` <span data-ttu-id="ee7e1-259">wenn der der Eigenschaft zugeordnete Wert geändert werden kann \(nur Datendeskriptoren\).</span><span class="sxs-lookup"><span data-stu-id="ee7e1-259">if the value associated with the property may be changed \(data descriptors only\).</span></span> |  
| <span data-ttu-id="ee7e1-260">get \(optional\)</span><span class="sxs-lookup"><span data-stu-id="ee7e1-260">get \(optional\)</span></span> | [<span data-ttu-id="ee7e1-261">RemoteObject</span><span class="sxs-lookup"><span data-stu-id="ee7e1-261">RemoteObject</span></span>](#remoteobject) | <span data-ttu-id="ee7e1-262">Eine Funktion, die als Getter für die Eigenschaft dient, oder wenn kein `undefined` Getter \(accessor descriptors only\) vorkommt.</span><span class="sxs-lookup"><span data-stu-id="ee7e1-262">A function which serves as a getter for the property, or `undefined` if there is no getter \(accessor descriptors only\).</span></span> |  
| <span data-ttu-id="ee7e1-263">set \(optional\)</span><span class="sxs-lookup"><span data-stu-id="ee7e1-263">set \(optional\)</span></span> | [<span data-ttu-id="ee7e1-264">RemoteObject</span><span class="sxs-lookup"><span data-stu-id="ee7e1-264">RemoteObject</span></span>](#remoteobject) | <span data-ttu-id="ee7e1-265">Eine Funktion, die als Setter für die Eigenschaft dient, oder wenn kein `undefined` Setter \(accessor descriptors only\) enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="ee7e1-265">A function which serves as a setter for the property, or `undefined` if there is no setter \(accessor descriptors only\).</span></span> |  
| <span data-ttu-id="ee7e1-266">konfigurierbar</span><span class="sxs-lookup"><span data-stu-id="ee7e1-266">configurable</span></span> | `boolean` | `True` <span data-ttu-id="ee7e1-267">wenn der Typ dieses Eigenschaftendeskriptors geändert werden kann und ob die Eigenschaft aus dem entsprechenden Objekt gelöscht werden kann.</span><span class="sxs-lookup"><span data-stu-id="ee7e1-267">if the type of this property descriptor may be changed and if the property may be deleted from the corresponding object.</span></span> |  
| <span data-ttu-id="ee7e1-268">enumerable</span><span class="sxs-lookup"><span data-stu-id="ee7e1-268">enumerable</span></span> | `boolean` | `True` <span data-ttu-id="ee7e1-269">wenn diese Eigenschaft während der Aufzählung der Eigenschaften des entsprechenden Objekts angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="ee7e1-269">if this property shows up during enumeration of the properties on the corresponding object.</span></span> |  
| <span data-ttu-id="ee7e1-270">wasThrown \(optional\)</span><span class="sxs-lookup"><span data-stu-id="ee7e1-270">wasThrown \(optional\)</span></span> | `boolean` | `True` <span data-ttu-id="ee7e1-271">wenn das Ergebnis während der Auswertung ausgelöst wurde.</span><span class="sxs-lookup"><span data-stu-id="ee7e1-271">if the result was thrown during the evaluation.</span></span> |  
| <span data-ttu-id="ee7e1-272">isOwn \(optional\)</span><span class="sxs-lookup"><span data-stu-id="ee7e1-272">isOwn \(optional\)</span></span> | `boolean` | `True` <span data-ttu-id="ee7e1-273">wenn sich die Eigenschaft im Besitz des Objekts befindet.</span><span class="sxs-lookup"><span data-stu-id="ee7e1-273">if the property is owned for the object.</span></span> |  
| <span data-ttu-id="ee7e1-274">msReturnValue \(optional\)</span><span class="sxs-lookup"><span data-stu-id="ee7e1-274">msReturnValue \(optional\)</span></span> | `boolean` | <span data-ttu-id="ee7e1-275">**Experimental**.</span><span class="sxs-lookup"><span data-stu-id="ee7e1-275">**Experimental**.</span></span>  <span data-ttu-id="ee7e1-276">Microsoft:  `True` Wenn es sich bei der Eigenschaft um einen Rückgabewert handelt.</span><span class="sxs-lookup"><span data-stu-id="ee7e1-276">Microsoft:  `True` if the property is a return value.</span></span> |  
| <span data-ttu-id="ee7e1-277">Symbol \(optional\)</span><span class="sxs-lookup"><span data-stu-id="ee7e1-277">symbol \(optional\)</span></span> | [<span data-ttu-id="ee7e1-278">RemoteObject</span><span class="sxs-lookup"><span data-stu-id="ee7e1-278">RemoteObject</span></span>](#remoteobject) | <span data-ttu-id="ee7e1-279">Eigenschaftssymbolobjekt, wenn die Eigenschaft vom Typ `symbol` ist.</span><span class="sxs-lookup"><span data-stu-id="ee7e1-279">Property symbol object, if the property is of the `symbol` type.</span></span> |  

---  

### <a name="callargument-object"></a><span data-ttu-id="ee7e1-280">CallArgument-Objekt</span><span class="sxs-lookup"><span data-stu-id="ee7e1-280">CallArgument object</span></span>  

<a name="callargument"></a>  

<span data-ttu-id="ee7e1-281">Represents function call argument.</span><span class="sxs-lookup"><span data-stu-id="ee7e1-281">Represents function call argument.</span></span>  <span data-ttu-id="ee7e1-282">Entweder Remoteobjekt-ID, unserialisierbarer Grundtypwert oder keiner von `value` \(für nicht definiert\) sollte angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="ee7e1-282">Either remote object ID `value`, unserializable primitive value or neither of \(for undefined\) them should be specified.</span></span>  

| <span data-ttu-id="ee7e1-283">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ee7e1-283">Properties</span></span> | <span data-ttu-id="ee7e1-284">Typ</span><span class="sxs-lookup"><span data-stu-id="ee7e1-284">Type</span></span> | <span data-ttu-id="ee7e1-285">Details</span><span class="sxs-lookup"><span data-stu-id="ee7e1-285">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="ee7e1-286">Wert \(optional\)</span><span class="sxs-lookup"><span data-stu-id="ee7e1-286">value \(optional\)</span></span> | `any` | <span data-ttu-id="ee7e1-287">Grundtypwert oder serialisierbares javascript-Objekt.</span><span class="sxs-lookup"><span data-stu-id="ee7e1-287">Primitive value or serializable javascript object.</span></span> |  
| <span data-ttu-id="ee7e1-288">unserializableValue \(optional\)</span><span class="sxs-lookup"><span data-stu-id="ee7e1-288">unserializableValue \(optional\)</span></span> | [<span data-ttu-id="ee7e1-289">UnserializableValue</span><span class="sxs-lookup"><span data-stu-id="ee7e1-289">UnserializableValue</span></span>](#unserializablevalue) | <span data-ttu-id="ee7e1-290">Grundtypwert, der nicht JSON-stringified sein kann.</span><span class="sxs-lookup"><span data-stu-id="ee7e1-290">Primitive value which can not be JSON-stringified.</span></span> |  
| <span data-ttu-id="ee7e1-291">objectId \(optional\)</span><span class="sxs-lookup"><span data-stu-id="ee7e1-291">objectId \(optional\)</span></span> | [<span data-ttu-id="ee7e1-292">RemoteObjectId</span><span class="sxs-lookup"><span data-stu-id="ee7e1-292">RemoteObjectId</span></span>](#remoteobjectid) | <span data-ttu-id="ee7e1-293">Remoteobjekthandle.</span><span class="sxs-lookup"><span data-stu-id="ee7e1-293">Remote object handle.</span></span> |  

---  

### <a name="executioncontextid-integer"></a><span data-ttu-id="ee7e1-294">ExecutionContextId ganzzahlig</span><span class="sxs-lookup"><span data-stu-id="ee7e1-294">ExecutionContextId integer</span></span>  

<a name="executioncontextid"></a>  

<span data-ttu-id="ee7e1-295">ID eines Ausführungskontexts.</span><span class="sxs-lookup"><span data-stu-id="ee7e1-295">ID of an execution context.</span></span>  

&nbsp;  

---  

### <a name="exceptiondetails-object"></a><span data-ttu-id="ee7e1-296">ExceptionDetails-Objekt</span><span class="sxs-lookup"><span data-stu-id="ee7e1-296">ExceptionDetails object</span></span>  

<a name="exceptiondetails"></a>  

<span data-ttu-id="ee7e1-297">Ausführliche Informationen zu Ausnahme \(oder Fehler\), die während der Skriptkompilierung oder -ausführung ausgelöst wurde.</span><span class="sxs-lookup"><span data-stu-id="ee7e1-297">Detailed information about exception \(or error\) that was thrown during script compilation or execution.</span></span>  

| <span data-ttu-id="ee7e1-298">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ee7e1-298">Properties</span></span> | <span data-ttu-id="ee7e1-299">Typ</span><span class="sxs-lookup"><span data-stu-id="ee7e1-299">Type</span></span> | <span data-ttu-id="ee7e1-300">Details</span><span class="sxs-lookup"><span data-stu-id="ee7e1-300">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="ee7e1-301">exceptionId</span><span class="sxs-lookup"><span data-stu-id="ee7e1-301">exceptionId</span></span> | `integer` | <span data-ttu-id="ee7e1-302">Ausnahme-ID.</span><span class="sxs-lookup"><span data-stu-id="ee7e1-302">Exception ID.</span></span> |  
| <span data-ttu-id="ee7e1-303">Text</span><span class="sxs-lookup"><span data-stu-id="ee7e1-303">text</span></span> | `string` | <span data-ttu-id="ee7e1-304">Ausnahmetext, der zusammen mit dem Ausnahmeobjekt verwendet werden sollte, wenn verfügbar.</span><span class="sxs-lookup"><span data-stu-id="ee7e1-304">Exception text, which should be used together with exception object when available.</span></span> |  
| <span data-ttu-id="ee7e1-305">lineNumber</span><span class="sxs-lookup"><span data-stu-id="ee7e1-305">lineNumber</span></span> | `integer` | <span data-ttu-id="ee7e1-306">Zeilennummer des Ausnahmespeicherorts \(0-basiert\).</span><span class="sxs-lookup"><span data-stu-id="ee7e1-306">Line number of the exception location \(0-based\).</span></span> |  
| <span data-ttu-id="ee7e1-307">columnNumber</span><span class="sxs-lookup"><span data-stu-id="ee7e1-307">columnNumber</span></span> | `integer` | <span data-ttu-id="ee7e1-308">Spaltennummer des Ausnahmespeicherorts \(0-basiert\).</span><span class="sxs-lookup"><span data-stu-id="ee7e1-308">Column number of the exception location \(0-based\).</span></span> |  
| <span data-ttu-id="ee7e1-309">scriptId \(optional\)</span><span class="sxs-lookup"><span data-stu-id="ee7e1-309">scriptId \(optional\)</span></span> | [<span data-ttu-id="ee7e1-310">ScriptId</span><span class="sxs-lookup"><span data-stu-id="ee7e1-310">ScriptId</span></span>](#scriptid) | <span data-ttu-id="ee7e1-311">Skript-ID des Ausnahmespeicherorts.</span><span class="sxs-lookup"><span data-stu-id="ee7e1-311">Script ID of the exception location.</span></span> |  
| <span data-ttu-id="ee7e1-312">url \(optional\)</span><span class="sxs-lookup"><span data-stu-id="ee7e1-312">url \(optional\)</span></span> | `string` | <span data-ttu-id="ee7e1-313">URL des Ausnahmespeicherorts, der verwendet werden soll, wenn das Skript nicht gemeldet wurde.</span><span class="sxs-lookup"><span data-stu-id="ee7e1-313">URL of the exception location, to be used when the script was not reported.</span></span> |  
| <span data-ttu-id="ee7e1-314">stackTrace \(optional\)</span><span class="sxs-lookup"><span data-stu-id="ee7e1-314">stackTrace \(optional\)</span></span> | [<span data-ttu-id="ee7e1-315">StackTrace</span><span class="sxs-lookup"><span data-stu-id="ee7e1-315">StackTrace</span></span>](#stacktrace) | <span data-ttu-id="ee7e1-316">JavaScript-Stapelverfolgung, sofern verfügbar.</span><span class="sxs-lookup"><span data-stu-id="ee7e1-316">JavaScript stack trace if available.</span></span> |  
| <span data-ttu-id="ee7e1-317">Ausnahme \(optional\)</span><span class="sxs-lookup"><span data-stu-id="ee7e1-317">exception \(optional\)</span></span> | [<span data-ttu-id="ee7e1-318">RemoteObject</span><span class="sxs-lookup"><span data-stu-id="ee7e1-318">RemoteObject</span></span>](#remoteobject) | <span data-ttu-id="ee7e1-319">Exception-Objekt, sofern verfügbar.</span><span class="sxs-lookup"><span data-stu-id="ee7e1-319">Exception object if available.</span></span> |  
| <span data-ttu-id="ee7e1-320">executionContextId \(optional\)</span><span class="sxs-lookup"><span data-stu-id="ee7e1-320">executionContextId \(optional\)</span></span> | [<span data-ttu-id="ee7e1-321">ExecutionContextId</span><span class="sxs-lookup"><span data-stu-id="ee7e1-321">ExecutionContextId</span></span>](#executioncontextid) | <span data-ttu-id="ee7e1-322">Bezeichner des Kontexts, in dem eine Ausnahme eingetreten ist.</span><span class="sxs-lookup"><span data-stu-id="ee7e1-322">Identifier of the context where exception happened.</span></span> |  

---  

### <a name="timestamp-integer"></a><span data-ttu-id="ee7e1-323">Ganze Zeitstempel</span><span class="sxs-lookup"><span data-stu-id="ee7e1-323">Timestamp integer</span></span>  

<a name="timestamp"></a>  

<span data-ttu-id="ee7e1-324">Anzahl der Millisekunden seit der Epoche.</span><span class="sxs-lookup"><span data-stu-id="ee7e1-324">Number of milliseconds since epoch.</span></span>  

&nbsp;  

---  

### <a name="callframe-object"></a><span data-ttu-id="ee7e1-325">CallFrame-Objekt</span><span class="sxs-lookup"><span data-stu-id="ee7e1-325">CallFrame object</span></span>  

<a name="callframe"></a>  

<span data-ttu-id="ee7e1-326">Stapeleintrag für Laufzeitfehler und -assertionen.</span><span class="sxs-lookup"><span data-stu-id="ee7e1-326">Stack entry for runtime errors and assertions.</span></span>  

| <span data-ttu-id="ee7e1-327">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ee7e1-327">Properties</span></span> | <span data-ttu-id="ee7e1-328">Typ</span><span class="sxs-lookup"><span data-stu-id="ee7e1-328">Type</span></span> | <span data-ttu-id="ee7e1-329">Details</span><span class="sxs-lookup"><span data-stu-id="ee7e1-329">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="ee7e1-330">functionName</span><span class="sxs-lookup"><span data-stu-id="ee7e1-330">functionName</span></span> | `string` | <span data-ttu-id="ee7e1-331">JavaScript-Funktionsname.</span><span class="sxs-lookup"><span data-stu-id="ee7e1-331">JavaScript function name.</span></span> |  
| <span data-ttu-id="ee7e1-332">scriptId</span><span class="sxs-lookup"><span data-stu-id="ee7e1-332">scriptId</span></span> | [<span data-ttu-id="ee7e1-333">ScriptId</span><span class="sxs-lookup"><span data-stu-id="ee7e1-333">ScriptId</span></span>](#scriptid) | <span data-ttu-id="ee7e1-334">JavaScript-Skript-ID.</span><span class="sxs-lookup"><span data-stu-id="ee7e1-334">JavaScript script ID.</span></span> |  
| <span data-ttu-id="ee7e1-335">URL</span><span class="sxs-lookup"><span data-stu-id="ee7e1-335">url</span></span> | `string` | <span data-ttu-id="ee7e1-336">Name oder URL des JavaScript-Skripts.</span><span class="sxs-lookup"><span data-stu-id="ee7e1-336">JavaScript script name or url.</span></span> |  
| <span data-ttu-id="ee7e1-337">lineNumber</span><span class="sxs-lookup"><span data-stu-id="ee7e1-337">lineNumber</span></span> | `integer` | <span data-ttu-id="ee7e1-338">JavaScript-Skript-Zeilennummer \(0-basiert\).</span><span class="sxs-lookup"><span data-stu-id="ee7e1-338">JavaScript script line number \(0-based\).</span></span> |  
| <span data-ttu-id="ee7e1-339">columnNumber</span><span class="sxs-lookup"><span data-stu-id="ee7e1-339">columnNumber</span></span> | `integer` | <span data-ttu-id="ee7e1-340">JavaScript-Skriptspaltennummer \(0-basiert\).</span><span class="sxs-lookup"><span data-stu-id="ee7e1-340">JavaScript script column number \(0-based\).</span></span> |  

---  

### <a name="stacktrace-object"></a><span data-ttu-id="ee7e1-341">StackTrace-Objekt</span><span class="sxs-lookup"><span data-stu-id="ee7e1-341">StackTrace object</span></span>  

<a name="stacktrace"></a>  

<span data-ttu-id="ee7e1-342">Aufrufframes für Assertionen oder Fehlermeldungen.</span><span class="sxs-lookup"><span data-stu-id="ee7e1-342">Call frames for assertions or error messages.</span></span>  

| <span data-ttu-id="ee7e1-343">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ee7e1-343">Properties</span></span> | <span data-ttu-id="ee7e1-344">Typ</span><span class="sxs-lookup"><span data-stu-id="ee7e1-344">Type</span></span> | <span data-ttu-id="ee7e1-345">Details</span><span class="sxs-lookup"><span data-stu-id="ee7e1-345">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="ee7e1-346">beschreibung \(optional\)</span><span class="sxs-lookup"><span data-stu-id="ee7e1-346">description \(optional\)</span></span> | `string` | <span data-ttu-id="ee7e1-347">Zeichenfolgenbeschriftung dieser Stapelverfolgung.</span><span class="sxs-lookup"><span data-stu-id="ee7e1-347">String label of this stack trace.</span></span>  <span data-ttu-id="ee7e1-348">Bei asynchronen Ablaufverfolgungen kann dies ein Name der Funktion sein, die den asynchronen Aufruf initiiert hat.</span><span class="sxs-lookup"><span data-stu-id="ee7e1-348">For async traces this may be a name of the function that initiated the async call.</span></span> |  
| <span data-ttu-id="ee7e1-349">callFrames</span><span class="sxs-lookup"><span data-stu-id="ee7e1-349">callFrames</span></span> | [<span data-ttu-id="ee7e1-350">CallFrame[]</span><span class="sxs-lookup"><span data-stu-id="ee7e1-350">CallFrame[]</span></span>](#callframe) | <span data-ttu-id="ee7e1-351">JavaScript-Funktionsname.</span><span class="sxs-lookup"><span data-stu-id="ee7e1-351">JavaScript function name.</span></span> |  
| <span data-ttu-id="ee7e1-352">übergeordnetes Element \(optional\)</span><span class="sxs-lookup"><span data-stu-id="ee7e1-352">parent \(optional\)</span></span> | [<span data-ttu-id="ee7e1-353">StackTrace</span><span class="sxs-lookup"><span data-stu-id="ee7e1-353">StackTrace</span></span>](#stacktrace) | <span data-ttu-id="ee7e1-354">Asynchrone JavaScript-Stapelverfolgung, die diesem Stapel vorausgegangen ist, sofern verfügbar.</span><span class="sxs-lookup"><span data-stu-id="ee7e1-354">Asynchronous JavaScript stack trace that preceded this stack, if available.</span></span> |  

---  
