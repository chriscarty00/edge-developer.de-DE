---
description: DevTools Protocol Version 0,1 (EdgeHTML) Reference für die Runtime-Domäne. Runtime-Domäne macht JavaScript-Runtime mithilfe von Remote Auswertungs-und Spiegel Objekten verfügbar. Evaluierungsergebnisse werden als Spiegelungs Objekt zurückgegeben, die den Objekttyp, die Zeichenfolgendarstellung und den eindeutigen Bezeichner verfügbar machen, die für weitere Objektverweise verwendet werden können. Ursprüngliche Objekte werden im Arbeitsspeicher verwaltet, sofern Sie nicht explizit freigegeben werden.
title: Runtime Domain-devtools Protocol Version 0,1 (EdgeHTML)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: reference
ms.prod: microsoft-edge
ms.custom: seodec18
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 942a105199c8740fb7f7496b2a68e3eb0cc46fb4
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233650"
---
# <span data-ttu-id="f299b-106">Runtime Domain-devtools Protocol Version 0,1 (EdgeHTML)</span><span class="sxs-lookup"><span data-stu-id="f299b-106">Runtime Domain - DevTools Protocol Version 0.1 (EdgeHTML)</span></span>  

<span data-ttu-id="f299b-107">Runtime-Domäne macht JavaScript-Runtime mithilfe von Remote Auswertungs-und Spiegel Objekten verfügbar.</span><span class="sxs-lookup"><span data-stu-id="f299b-107">Runtime domain exposes JavaScript runtime by means of remote evaluation and mirror objects.</span></span> <span data-ttu-id="f299b-108">Evaluierungsergebnisse werden als Spiegelungs Objekt zurückgegeben, die den Objekttyp, die Zeichenfolgendarstellung und den eindeutigen Bezeichner verfügbar machen, die für weitere Objektverweise verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="f299b-108">Evaluation results are returned as mirror object that expose object type, string representation and unique identifier that can be used for further object reference.</span></span> <span data-ttu-id="f299b-109">Ursprüngliche Objekte werden im Arbeitsspeicher verwaltet, sofern Sie nicht explizit freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="f299b-109">Original objects are maintained in memory unless they are either explicitly released.</span></span>

| | |
|-|-|
| [**<span data-ttu-id="f299b-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="f299b-110">Methods</span></span>**](#methods) | <span data-ttu-id="f299b-111">[aktivieren](#enable), [Deaktivieren](#disable), [Auswerten](#evaluate), [callFunctionOn](#callfunctionon), [GetProperties](#getproperties)</span><span class="sxs-lookup"><span data-stu-id="f299b-111">[enable](#enable), [disable](#disable), [evaluate](#evaluate), [callFunctionOn](#callfunctionon), [getProperties](#getproperties)</span></span> |
| [**<span data-ttu-id="f299b-112">Veranstaltungen</span><span class="sxs-lookup"><span data-stu-id="f299b-112">Events</span></span>**](#events) | <span data-ttu-id="f299b-113">[executionContextsCleared](#executioncontextscleared), [exceptionThrown](#exceptionthrown)</span><span class="sxs-lookup"><span data-stu-id="f299b-113">[executionContextsCleared](#executioncontextscleared), [exceptionThrown](#exceptionthrown)</span></span> |
| [**<span data-ttu-id="f299b-114">Typen</span><span class="sxs-lookup"><span data-stu-id="f299b-114">Types</span></span>**](#types) | <span data-ttu-id="f299b-115">[Skript](#scriptid)- [RemoteObjectId](#remoteobjectid), [unserializablevalue](#unserializablevalue), [RemoteObject](#remoteobject), [PropertyDescriptor](#propertydescriptor), [CallArgument](#callargument), [ExecutionContextId](#executioncontextid), [ExceptionDetails](#exceptiondetails), [timestamp](#timestamp), [CallFrame](#callframe), [StackTrace](#stacktrace)</span><span class="sxs-lookup"><span data-stu-id="f299b-115">[ScriptId](#scriptid), [RemoteObjectId](#remoteobjectid), [UnserializableValue](#unserializablevalue), [RemoteObject](#remoteobject), [PropertyDescriptor](#propertydescriptor), [CallArgument](#callargument), [ExecutionContextId](#executioncontextid), [ExceptionDetails](#exceptiondetails), [Timestamp](#timestamp), [CallFrame](#callframe), [StackTrace](#stacktrace)</span></span> |
## <span data-ttu-id="f299b-116">Methoden</span><span class="sxs-lookup"><span data-stu-id="f299b-116">Methods</span></span>

### <span data-ttu-id="f299b-117">Aktivieren</span><span class="sxs-lookup"><span data-stu-id="f299b-117">enable</span></span>
<span data-ttu-id="f299b-118">Ermöglicht die Berichterstattung über das <code>executionContextsCleared</code> Ereignis.</span><span class="sxs-lookup"><span data-stu-id="f299b-118">Enables reporting of the <code>executionContextsCleared</code> event.</span></span>


---

### <span data-ttu-id="f299b-119">Deaktivieren </span><span class="sxs-lookup"><span data-stu-id="f299b-119">disable</span></span>
<span data-ttu-id="f299b-120">Deaktiviert die Berichterstattung über das <code>executionContextsCleared</code> Ereignis.</span><span class="sxs-lookup"><span data-stu-id="f299b-120">Disables reporting of the <code>executionContextsCleared</code> event.</span></span>


---

### <span data-ttu-id="f299b-121">bewerten</span><span class="sxs-lookup"><span data-stu-id="f299b-121">evaluate</span></span>
<span data-ttu-id="f299b-122">Wertet Ausdruck für globales Objekt aus.</span><span class="sxs-lookup"><span data-stu-id="f299b-122">Evaluates expression on global object.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="f299b-123">Parameter</span><span class="sxs-lookup"><span data-stu-id="f299b-123">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="f299b-124">Ausdruck</span><span class="sxs-lookup"><span data-stu-id="f299b-124">expression</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="f299b-125">Ausdruck, der ausgewertet werden soll.</span><span class="sxs-lookup"><span data-stu-id="f299b-125">Expression to evaluate.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="f299b-126">lautlos</span><span class="sxs-lookup"><span data-stu-id="f299b-126">silent</span></span> <br/> <i><span data-ttu-id="f299b-127">Optional</span><span class="sxs-lookup"><span data-stu-id="f299b-127">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="f299b-128">Im unbeaufsichtigten Modus werden während der Auswertung ausgelöste Ausnahmen nicht gemeldet, und die Ausführung wird nicht angehalten.</span><span class="sxs-lookup"><span data-stu-id="f299b-128">In silent mode exceptions thrown during evaluation are not reported and do not pause execution.</span></span> <span data-ttu-id="f299b-129">Überschreibt den <code>setPauseOnException</code> Zustand.</span><span class="sxs-lookup"><span data-stu-id="f299b-129">Overrides <code>setPauseOnException</code> state.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="f299b-130">ContextId</span><span class="sxs-lookup"><span data-stu-id="f299b-130">contextId</span></span> <br/> <i><span data-ttu-id="f299b-131">Optional</span><span class="sxs-lookup"><span data-stu-id="f299b-131">optional</span></span></i></td>
            <td><a href="#executioncontextid"><code class="flyout">ExecutionContextId</code></a></td>
            <td><span data-ttu-id="f299b-132">Gibt an, in welchem Ausführungskontext die Auswertung durchgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="f299b-132">Specifies in which execution context to perform evaluation.</span></span> <span data-ttu-id="f299b-133">Wenn der Parameter ausgelassen wird, wird die Auswertung im Kontext der geprüften Seite durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="f299b-133">If the parameter is omitted the evaluation will be performed in the context of the inspected page.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="f299b-134">returnByValue</span><span class="sxs-lookup"><span data-stu-id="f299b-134">returnByValue</span></span> <br/> <i><span data-ttu-id="f299b-135">Optional</span><span class="sxs-lookup"><span data-stu-id="f299b-135">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="f299b-136">Gibt an, ob es sich bei dem Ergebnis um ein JSON-Objekt handelt, das als Wert gesendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="f299b-136">Whether the result is expected to be a JSON object that should be sent by value.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="f299b-137">awaitPromise</span><span class="sxs-lookup"><span data-stu-id="f299b-137">awaitPromise</span></span> <br/> <i><span data-ttu-id="f299b-138">Optional</span><span class="sxs-lookup"><span data-stu-id="f299b-138">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="f299b-139">Ob die Ausführung <code>await</code> für den resultierenden Wert und die Rückgabe nach dem erwarteten Versprechen aufgelöst werden soll.</span><span class="sxs-lookup"><span data-stu-id="f299b-139">Whether execution should <code>await</code> for resulting value and return once awaited promise is resolved.</span></span></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="f299b-140">Gibt</span><span class="sxs-lookup"><span data-stu-id="f299b-140">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="f299b-141">Ergebnis</span><span class="sxs-lookup"><span data-stu-id="f299b-141">result</span></span></td>
            <td><a href="#remoteobject"><code class="flyout">RemoteObject</code></a></td>
            <td><span data-ttu-id="f299b-142">Auswertungsergebnis.</span><span class="sxs-lookup"><span data-stu-id="f299b-142">Evaluation result.</span></span></td>
        </tr>
    </tbody>
</table>

---

### <span data-ttu-id="f299b-143">callFunctionOn</span><span class="sxs-lookup"><span data-stu-id="f299b-143">callFunctionOn</span></span>
<span data-ttu-id="f299b-144">Calls-Funktion mit einer angegebenen Deklaration für das angegebene Objekt.</span><span class="sxs-lookup"><span data-stu-id="f299b-144">Calls function with given declaration on the given object.</span></span> <span data-ttu-id="f299b-145">Die Objektgruppe des Ergebnisses wird vom Zielobjekt geerbt.</span><span class="sxs-lookup"><span data-stu-id="f299b-145">Object group of the result is inherited from the target object.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="f299b-146">Parameter</span><span class="sxs-lookup"><span data-stu-id="f299b-146">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="f299b-147">functionDeclaration</span><span class="sxs-lookup"><span data-stu-id="f299b-147">functionDeclaration</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="f299b-148">Die Deklaration der Funktion, die aufgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="f299b-148">Declaration of the function to call.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="f299b-149">ObjectID</span><span class="sxs-lookup"><span data-stu-id="f299b-149">objectId</span></span> <br/> <i><span data-ttu-id="f299b-150">Optional</span><span class="sxs-lookup"><span data-stu-id="f299b-150">optional</span></span></i></td>
            <td><a href="#remoteobjectid"><code class="flyout">RemoteObjectId</code></a></td>
            <td><span data-ttu-id="f299b-151">Der Bezeichner des Objekts, für das die Funktion aufgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="f299b-151">Identifier of the object to call function on.</span></span> <span data-ttu-id="f299b-152">Es sollten entweder ObjectID oder executionContextId angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="f299b-152">Either objectId or executionContextId should be specified.</span></span>  <span data-ttu-id="f299b-153">ObjectID muss aus der Runtime. Evaluate ()-Funktion sein.</span><span class="sxs-lookup"><span data-stu-id="f299b-153">objectId must be from the Runtime.evaluate() function.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="f299b-154">arguments</span><span class="sxs-lookup"><span data-stu-id="f299b-154">arguments</span></span> <br/> <i><span data-ttu-id="f299b-155">Optional</span><span class="sxs-lookup"><span data-stu-id="f299b-155">optional</span></span></i></td>
            <td><a href="#callargument"><code class="flyout">CallArgument[]</code></a></td>
            <td><span data-ttu-id="f299b-156">Rufen Sie Argumente auf.</span><span class="sxs-lookup"><span data-stu-id="f299b-156">Call arguments.</span></span> <span data-ttu-id="f299b-157">Alle Anruf Argumente müssen zur gleichen JavaScript-Welt gehören wie das Zielobjekt.</span><span class="sxs-lookup"><span data-stu-id="f299b-157">All call arguments must belong to the same JavaScript world as the target object.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="f299b-158">lautlos</span><span class="sxs-lookup"><span data-stu-id="f299b-158">silent</span></span> <br/> <i><span data-ttu-id="f299b-159">Optional</span><span class="sxs-lookup"><span data-stu-id="f299b-159">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="f299b-160">Im unbeaufsichtigten Modus werden während der Auswertung ausgelöste Ausnahmen nicht gemeldet, und die Ausführung wird nicht angehalten.</span><span class="sxs-lookup"><span data-stu-id="f299b-160">In silent mode exceptions thrown during evaluation are not reported and do not pause execution.</span></span> <span data-ttu-id="f299b-161">Überschreibt den <code>setPauseOnException</code> Zustand.</span><span class="sxs-lookup"><span data-stu-id="f299b-161">Overrides <code>setPauseOnException</code> state.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="f299b-162">returnByValue</span><span class="sxs-lookup"><span data-stu-id="f299b-162">returnByValue</span></span> <br/> <i><span data-ttu-id="f299b-163">Optional</span><span class="sxs-lookup"><span data-stu-id="f299b-163">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="f299b-164">Gibt an, ob es sich bei dem Ergebnis um ein JSON-Objekt handelt, das als Wert gesendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="f299b-164">Whether the result is expected to be a JSON object which should be sent by value.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="f299b-165">awaitPromise</span><span class="sxs-lookup"><span data-stu-id="f299b-165">awaitPromise</span></span> <br/> <i><span data-ttu-id="f299b-166">Optional</span><span class="sxs-lookup"><span data-stu-id="f299b-166">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="f299b-167">Ob die Ausführung <code>await</code> für den resultierenden Wert und die Rückgabe nach dem erwarteten Versprechen aufgelöst werden soll.</span><span class="sxs-lookup"><span data-stu-id="f299b-167">Whether execution should <code>await</code> for resulting value and return once awaited promise is resolved.</span></span></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="f299b-168">Gibt</span><span class="sxs-lookup"><span data-stu-id="f299b-168">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="f299b-169">Ergebnis</span><span class="sxs-lookup"><span data-stu-id="f299b-169">result</span></span></td>
            <td><a href="#remoteobject"><code class="flyout">RemoteObject</code></a></td>
            <td><span data-ttu-id="f299b-170">Ergebnis des Anrufs.</span><span class="sxs-lookup"><span data-stu-id="f299b-170">Call result.</span></span></td>
        </tr>
    </tbody>
</table>

---

### <span data-ttu-id="f299b-171">GetProperties</span><span class="sxs-lookup"><span data-stu-id="f299b-171">getProperties</span></span>
<span data-ttu-id="f299b-172">Gibt Eigenschaften eines angegebenen Objekts zurück.</span><span class="sxs-lookup"><span data-stu-id="f299b-172">Returns properties of a given object.</span></span> <span data-ttu-id="f299b-173">Die Objektgruppe des Ergebnisses wird vom Zielobjekt geerbt.</span><span class="sxs-lookup"><span data-stu-id="f299b-173">Object group of the result is inherited from the target object.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="f299b-174">Parameter</span><span class="sxs-lookup"><span data-stu-id="f299b-174">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="f299b-175">ObjectID</span><span class="sxs-lookup"><span data-stu-id="f299b-175">objectId</span></span></td>
            <td><a href="#remoteobjectid"><code class="flyout">RemoteObjectId</code></a></td>
            <td><span data-ttu-id="f299b-176">Der Bezeichner des Objekts, für das Eigenschaften zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="f299b-176">Identifier of the object to return properties for.</span></span>  <span data-ttu-id="f299b-177">ObjectID muss aus der Debugger. evaluateOnCallFrame ()-Funktion sein.</span><span class="sxs-lookup"><span data-stu-id="f299b-177">objectId must be from the Debugger.evaluateOnCallFrame() function.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="f299b-178">ownProperties</span><span class="sxs-lookup"><span data-stu-id="f299b-178">ownProperties</span></span> <br/> <i><span data-ttu-id="f299b-179">Optional</span><span class="sxs-lookup"><span data-stu-id="f299b-179">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="f299b-180">Ist "true", gibt Eigenschaften zurück, die nur dem Element selbst und nicht der zugehörigen Prototypkette gehören.</span><span class="sxs-lookup"><span data-stu-id="f299b-180">If true, returns properties belonging only to the element itself, not to its prototype chain.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="f299b-181">accessorPropertiesOnly</span><span class="sxs-lookup"><span data-stu-id="f299b-181">accessorPropertiesOnly</span></span> <br/> <i><span data-ttu-id="f299b-182">Optional</span><span class="sxs-lookup"><span data-stu-id="f299b-182">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span><b><span data-ttu-id="f299b-183">Experimenteller.</span><span class="sxs-lookup"><span data-stu-id="f299b-183">Experimental.</span></span> </b></span><span data-ttu-id="f299b-184">Ist "true", gibt nur Accessor-Eigenschaften (mit Getter/Setter) zurück. interne Eigenschaften werden auch nicht zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="f299b-184">If true, returns accessor properties (with getter/setter) only; internal properties are not returned either.</span></span></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="f299b-185">Gibt</span><span class="sxs-lookup"><span data-stu-id="f299b-185">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="f299b-186">Ergebnis</span><span class="sxs-lookup"><span data-stu-id="f299b-186">result</span></span></td>
            <td><a href="#propertydescriptor"><code class="flyout">PropertyDescriptor[]</code></a></td>
            <td><span data-ttu-id="f299b-187">Objekteigenschaften.</span><span class="sxs-lookup"><span data-stu-id="f299b-187">Object properties.</span></span></td>
        </tr>
    </tbody>
</table>

---

## <span data-ttu-id="f299b-188">Veranstaltungen</span><span class="sxs-lookup"><span data-stu-id="f299b-188">Events</span></span>

### <span data-ttu-id="f299b-189">executionContextsCleared</span><span class="sxs-lookup"><span data-stu-id="f299b-189">executionContextsCleared</span></span>
<span data-ttu-id="f299b-190">Wird ausgegeben, wenn alle executionContexts im Browser gelöscht wurden</span><span class="sxs-lookup"><span data-stu-id="f299b-190">Issued when all executionContexts were cleared in browser</span></span>


---

### <span data-ttu-id="f299b-191">exceptionThrown</span><span class="sxs-lookup"><span data-stu-id="f299b-191">exceptionThrown</span></span>
<span data-ttu-id="f299b-192">Wird ausgegeben, wenn eine Ausnahme ausgelöst und nicht behandelt wurde.</span><span class="sxs-lookup"><span data-stu-id="f299b-192">Issued when exception was thrown and unhandled.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="f299b-193">Parameter</span><span class="sxs-lookup"><span data-stu-id="f299b-193">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="f299b-194">Timestamp</span><span class="sxs-lookup"><span data-stu-id="f299b-194">timestamp</span></span></td>
            <td><a href="#timestamp"><code class="flyout">Timestamp</code></a></td>
            <td><span data-ttu-id="f299b-195">Der Zeitstempel der Ausnahme.</span><span class="sxs-lookup"><span data-stu-id="f299b-195">Timestamp of the exception.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="f299b-196">exceptionDetails</span><span class="sxs-lookup"><span data-stu-id="f299b-196">exceptionDetails</span></span></td>
            <td><a href="#exceptiondetails"><code class="flyout">ExceptionDetails</code></a></td>
            <td></td>
        </tr>
    </tbody>
</table>

---

## <span data-ttu-id="f299b-197">Typen</span><span class="sxs-lookup"><span data-stu-id="f299b-197">Types</span></span>

### <a name="scriptid"></a> <span data-ttu-id="f299b-198">SkriptID</span><span class="sxs-lookup"><span data-stu-id="f299b-198">ScriptId</span></span> `string`

<span data-ttu-id="f299b-199">Eindeutiger Skriptbezeichner.</span><span class="sxs-lookup"><span data-stu-id="f299b-199">Unique script identifier.</span></span>


---

### <a name="remoteobjectid"></a> <span data-ttu-id="f299b-200">RemoteObjectId</span><span class="sxs-lookup"><span data-stu-id="f299b-200">RemoteObjectId</span></span> `string`

<span data-ttu-id="f299b-201">Eindeutige Objekt-ID.</span><span class="sxs-lookup"><span data-stu-id="f299b-201">Unique object identifier.</span></span>


---

### <a name="unserializablevalue"></a> <span data-ttu-id="f299b-202">Unserializablevalue</span><span class="sxs-lookup"><span data-stu-id="f299b-202">UnserializableValue</span></span> `string`

<span data-ttu-id="f299b-203">Primitiver Wert, der nicht JSON-stringified sein kann.</span><span class="sxs-lookup"><span data-stu-id="f299b-203">Primitive value which cannot be JSON-stringified.</span></span>

##### <span data-ttu-id="f299b-204">Zulässige Werte</span><span class="sxs-lookup"><span data-stu-id="f299b-204">Allowed Values</span></span>
<span data-ttu-id="f299b-205">Unendlichkeit, Nan,-Unendlichkeit,-0</span><span class="sxs-lookup"><span data-stu-id="f299b-205">Infinity, NaN, -Infinity, -0</span></span>

---

### <a name="remoteobject"></a> <span data-ttu-id="f299b-206">RemoteObject</span><span class="sxs-lookup"><span data-stu-id="f299b-206">RemoteObject</span></span> `object`

<span data-ttu-id="f299b-207">Spiegelungs Objekt, das auf das ursprüngliche JavaScript-Objekt verweist</span><span class="sxs-lookup"><span data-stu-id="f299b-207">Mirror object referencing original JavaScript object.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="f299b-208">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f299b-208">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="f299b-209">Typ</span><span class="sxs-lookup"><span data-stu-id="f299b-209">type</span></span></td>
            <td><code class="flyout">string</code> <br/> <i><span data-ttu-id="f299b-210">Zulässige Werte: Objekt, Funktion, undefined, Zeichenfolge, Zahl, boolescher Wert, Symbol</span><span class="sxs-lookup"><span data-stu-id="f299b-210">Allowed values: object, function, undefined, string, number, boolean, symbol</span></span></i></td>
            <td><span data-ttu-id="f299b-211">Objekttyp.</span><span class="sxs-lookup"><span data-stu-id="f299b-211">Object type.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="f299b-212">Untertyp</span><span class="sxs-lookup"><span data-stu-id="f299b-212">subtype</span></span> <br/> <i><span data-ttu-id="f299b-213">Optional</span><span class="sxs-lookup"><span data-stu-id="f299b-213">optional</span></span></i></td>
            <td><code class="flyout">string</code> <br/> <i><span data-ttu-id="f299b-214">Zulässige Werte: NULL, Fehler, Versprechung</span><span class="sxs-lookup"><span data-stu-id="f299b-214">Allowed values: null, error, promise</span></span></i></td>
            <td><span data-ttu-id="f299b-215">Hinweis für den Untertyp des Objekts.</span><span class="sxs-lookup"><span data-stu-id="f299b-215">Object subtype hint.</span></span> <span data-ttu-id="f299b-216">Nur für <code>object</code> Typwerte angegeben.</span><span class="sxs-lookup"><span data-stu-id="f299b-216">Specified for <code>object</code> type values only.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="f299b-217">ClassName</span><span class="sxs-lookup"><span data-stu-id="f299b-217">className</span></span> <br/> <i><span data-ttu-id="f299b-218">Optional</span><span class="sxs-lookup"><span data-stu-id="f299b-218">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="f299b-219">Name der Objektklasse (Konstruktor).</span><span class="sxs-lookup"><span data-stu-id="f299b-219">Object class (constructor) name.</span></span> <span data-ttu-id="f299b-220">Nur für <code>object</code> Typwerte angegeben.</span><span class="sxs-lookup"><span data-stu-id="f299b-220">Specified for <code>object</code> type values only.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="f299b-221">value</span><span class="sxs-lookup"><span data-stu-id="f299b-221">value</span></span> <br/> <i><span data-ttu-id="f299b-222">Optional</span><span class="sxs-lookup"><span data-stu-id="f299b-222">optional</span></span></i></td>
            <td><code class="flyout">any</code></td>
            <td><span data-ttu-id="f299b-223">Remote Objektwert im Fall von primitiven Werten oder JSON-Werten (sofern angefordert).</span><span class="sxs-lookup"><span data-stu-id="f299b-223">Remote object value in case of primitive values or JSON values (if it was requested).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="f299b-224">unserializablevalue</span><span class="sxs-lookup"><span data-stu-id="f299b-224">unserializableValue</span></span> <br/> <i><span data-ttu-id="f299b-225">Optional</span><span class="sxs-lookup"><span data-stu-id="f299b-225">optional</span></span></i></td>
            <td><a href="#unserializablevalue"><code class="flyout">UnserializableValue</code></a></td>
            <td><span data-ttu-id="f299b-226">Primitiver Wert, der nicht JSON-stringified sein kann</span><span class="sxs-lookup"><span data-stu-id="f299b-226">Primitive value which can not be JSON-stringified does not have</span></span> <code>value</code><span data-ttu-id="f299b-227">, aber ruft diese Eigenschaft ab.</span><span class="sxs-lookup"><span data-stu-id="f299b-227">, but gets this property.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="f299b-228">description</span><span class="sxs-lookup"><span data-stu-id="f299b-228">description</span></span> <br/> <i><span data-ttu-id="f299b-229">Optional</span><span class="sxs-lookup"><span data-stu-id="f299b-229">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="f299b-230">Zeichenfolgendarstellung des Objekts.</span><span class="sxs-lookup"><span data-stu-id="f299b-230">String representation of the object.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="f299b-231">ObjectID</span><span class="sxs-lookup"><span data-stu-id="f299b-231">objectId</span></span> <br/> <i><span data-ttu-id="f299b-232">Optional</span><span class="sxs-lookup"><span data-stu-id="f299b-232">optional</span></span></i></td>
            <td><a href="#remoteobjectid"><code class="flyout">RemoteObjectId</code></a></td>
            <td><span data-ttu-id="f299b-233">Eindeutige Objekt-ID (für nicht primitive Werte).</span><span class="sxs-lookup"><span data-stu-id="f299b-233">Unique object identifier (for non-primitive values).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="f299b-234">msDebuggerPropertyId</span><span class="sxs-lookup"><span data-stu-id="f299b-234">msDebuggerPropertyId</span></span> <br/> <i><span data-ttu-id="f299b-235">Optional</span><span class="sxs-lookup"><span data-stu-id="f299b-235">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span><b><span data-ttu-id="f299b-236">Experimenteller.</span><span class="sxs-lookup"><span data-stu-id="f299b-236">Experimental.</span></span> </b></span><span data-ttu-id="f299b-237">Microsoft: die zugeordnete Debugger-Eigenschafts-ID für dieses Objekt.</span><span class="sxs-lookup"><span data-stu-id="f299b-237">Microsoft: The associated debugger property id for this object.</span></span></td>
        </tr>
    </tbody>
</table>

---

### <a name="propertydescriptor"></a> <span data-ttu-id="f299b-238">PropertyDescriptor</span><span class="sxs-lookup"><span data-stu-id="f299b-238">PropertyDescriptor</span></span> `object`

<span data-ttu-id="f299b-239">Objekteigenschaften Deskriptor</span><span class="sxs-lookup"><span data-stu-id="f299b-239">Object property descriptor.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="f299b-240">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f299b-240">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="f299b-241">name</span><span class="sxs-lookup"><span data-stu-id="f299b-241">name</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="f299b-242">Eigenschaftsname oder Symbol Beschreibung.</span><span class="sxs-lookup"><span data-stu-id="f299b-242">Property name or symbol description.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="f299b-243">value</span><span class="sxs-lookup"><span data-stu-id="f299b-243">value</span></span> <br/> <i><span data-ttu-id="f299b-244">Optional</span><span class="sxs-lookup"><span data-stu-id="f299b-244">optional</span></span></i></td>
            <td><a href="#remoteobject"><code class="flyout">RemoteObject</code></a></td>
            <td><span data-ttu-id="f299b-245">Der Wert, der der Eigenschaft zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="f299b-245">The value associated with the property.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="f299b-246">beschreibbar</span><span class="sxs-lookup"><span data-stu-id="f299b-246">writable</span></span> <br/> <i><span data-ttu-id="f299b-247">Optional</span><span class="sxs-lookup"><span data-stu-id="f299b-247">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="f299b-248">"True", wenn der Wert, der der Eigenschaft zugeordnet ist, geändert werden kann (nur Daten Deskriptoren).</span><span class="sxs-lookup"><span data-stu-id="f299b-248">True if the value associated with the property may be changed (data descriptors only).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="f299b-249">Abrufen</span><span class="sxs-lookup"><span data-stu-id="f299b-249">get</span></span> <br/> <i><span data-ttu-id="f299b-250">Optional</span><span class="sxs-lookup"><span data-stu-id="f299b-250">optional</span></span></i></td>
            <td><a href="#remoteobject"><code class="flyout">RemoteObject</code></a></td>
            <td><span data-ttu-id="f299b-251">Eine Funktion, die als Getter für die Eigenschaft dient, oder <code>undefined</code> Wenn kein Getter vorhanden ist (nur Accessor-Deskriptoren).</span><span class="sxs-lookup"><span data-stu-id="f299b-251">A function which serves as a getter for the property, or <code>undefined</code> if there is no getter (accessor descriptors only).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="f299b-252">set</span><span class="sxs-lookup"><span data-stu-id="f299b-252">set</span></span> <br/> <i><span data-ttu-id="f299b-253">Optional</span><span class="sxs-lookup"><span data-stu-id="f299b-253">optional</span></span></i></td>
            <td><a href="#remoteobject"><code class="flyout">RemoteObject</code></a></td>
            <td><span data-ttu-id="f299b-254">Eine Funktion, die als Setter für die Eigenschaft dient, oder <code>undefined</code> Wenn kein Setter vorhanden ist (nur Accessor-Deskriptoren).</span><span class="sxs-lookup"><span data-stu-id="f299b-254">A function which serves as a setter for the property, or <code>undefined</code> if there is no setter (accessor descriptors only).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="f299b-255">konfigurierbar</span><span class="sxs-lookup"><span data-stu-id="f299b-255">configurable</span></span></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="f299b-256">"True", wenn der Typ dieses Eigenschaftendeskriptors geändert werden kann und die Eigenschaft aus dem entsprechenden Objekt gelöscht werden kann.</span><span class="sxs-lookup"><span data-stu-id="f299b-256">True if the type of this property descriptor may be changed and if the property may be deleted from the corresponding object.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="f299b-257">Enumerable</span><span class="sxs-lookup"><span data-stu-id="f299b-257">enumerable</span></span></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="f299b-258">"True", wenn diese Eigenschaft während der Enumeration der Eigenschaften des entsprechenden Objekts angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="f299b-258">True if this property shows up during enumeration of the properties on the corresponding object.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="f299b-259">wasThrown</span><span class="sxs-lookup"><span data-stu-id="f299b-259">wasThrown</span></span> <br/> <i><span data-ttu-id="f299b-260">Optional</span><span class="sxs-lookup"><span data-stu-id="f299b-260">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="f299b-261">"True", wenn das Ergebnis während der Auswertung ausgelöst wurde.</span><span class="sxs-lookup"><span data-stu-id="f299b-261">True if the result was thrown during the evaluation.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="f299b-262">isOwn</span><span class="sxs-lookup"><span data-stu-id="f299b-262">isOwn</span></span> <br/> <i><span data-ttu-id="f299b-263">Optional</span><span class="sxs-lookup"><span data-stu-id="f299b-263">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="f299b-264">"True", wenn die Eigenschaft für das Objekt gehört.</span><span class="sxs-lookup"><span data-stu-id="f299b-264">True if the property is owned for the object.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="f299b-265">msReturnValue</span><span class="sxs-lookup"><span data-stu-id="f299b-265">msReturnValue</span></span> <br/> <i><span data-ttu-id="f299b-266">Optional</span><span class="sxs-lookup"><span data-stu-id="f299b-266">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span><b><span data-ttu-id="f299b-267">Experimenteller.</span><span class="sxs-lookup"><span data-stu-id="f299b-267">Experimental.</span></span> </b></span><span data-ttu-id="f299b-268">Microsoft: true, wenn die Eigenschaft ein Rückgabewert ist.</span><span class="sxs-lookup"><span data-stu-id="f299b-268">Microsoft: True if the property is a return value.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="f299b-269">symbol</span><span class="sxs-lookup"><span data-stu-id="f299b-269">symbol</span></span> <br/> <i><span data-ttu-id="f299b-270">Optional</span><span class="sxs-lookup"><span data-stu-id="f299b-270">optional</span></span></i></td>
            <td><a href="#remoteobject"><code class="flyout">RemoteObject</code></a></td>
            <td><span data-ttu-id="f299b-271">Eigenschafts Symbol Objekt, wenn die Eigenschaft vom `symbol` Typ ist.</span><span class="sxs-lookup"><span data-stu-id="f299b-271">Property symbol object, if the property is of the `symbol` type.</span></span> </td>
        </tr>
    </tbody>
</table>

---

### <a name="callargument"></a> <span data-ttu-id="f299b-272">CallArgument</span><span class="sxs-lookup"><span data-stu-id="f299b-272">CallArgument</span></span> `object`

<span data-ttu-id="f299b-273">Steht für Funktionsaufruf Argument.</span><span class="sxs-lookup"><span data-stu-id="f299b-273">Represents function call argument.</span></span> <span data-ttu-id="f299b-274">Es sollten entweder die Remoteobjekt-ID <code>objectId</code> , der primitive <code>value</code> , der unserialisierbare primitive Wert oder keines der (für undefined) angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="f299b-274">Either remote object id <code>objectId</code>, primitive <code>value</code>, unserializable primitive value or neither of (for undefined) them should be specified.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="f299b-275">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f299b-275">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="f299b-276">value</span><span class="sxs-lookup"><span data-stu-id="f299b-276">value</span></span> <br/> <i><span data-ttu-id="f299b-277">Optional</span><span class="sxs-lookup"><span data-stu-id="f299b-277">optional</span></span></i></td>
            <td><code class="flyout">any</code></td>
            <td><span data-ttu-id="f299b-278">Primitiver Wert oder serialisierbares JavaScript-Objekt.</span><span class="sxs-lookup"><span data-stu-id="f299b-278">Primitive value or serializable javascript object.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="f299b-279">unserializablevalue</span><span class="sxs-lookup"><span data-stu-id="f299b-279">unserializableValue</span></span> <br/> <i><span data-ttu-id="f299b-280">Optional</span><span class="sxs-lookup"><span data-stu-id="f299b-280">optional</span></span></i></td>
            <td><a href="#unserializablevalue"><code class="flyout">UnserializableValue</code></a></td>
            <td><span data-ttu-id="f299b-281">Primitiver Wert, der nicht JSON-stringified sein kann.</span><span class="sxs-lookup"><span data-stu-id="f299b-281">Primitive value which can not be JSON-stringified.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="f299b-282">ObjectID</span><span class="sxs-lookup"><span data-stu-id="f299b-282">objectId</span></span> <br/> <i><span data-ttu-id="f299b-283">Optional</span><span class="sxs-lookup"><span data-stu-id="f299b-283">optional</span></span></i></td>
            <td><a href="#remoteobjectid"><code class="flyout">RemoteObjectId</code></a></td>
            <td><span data-ttu-id="f299b-284">Remote Objekthandle.</span><span class="sxs-lookup"><span data-stu-id="f299b-284">Remote object handle.</span></span></td>
        </tr>
    </tbody>
</table>

---

### <a name="executioncontextid"></a> <span data-ttu-id="f299b-285">ExecutionContextId</span><span class="sxs-lookup"><span data-stu-id="f299b-285">ExecutionContextId</span></span> `integer`

<span data-ttu-id="f299b-286">Die ID eines Ausführungskontexts.</span><span class="sxs-lookup"><span data-stu-id="f299b-286">Id of an execution context.</span></span>


---

### <a name="exceptiondetails"></a> <span data-ttu-id="f299b-287">ExceptionDetails</span><span class="sxs-lookup"><span data-stu-id="f299b-287">ExceptionDetails</span></span> `object`

<span data-ttu-id="f299b-288">Detaillierte Informationen zu Ausnahmen (oder Fehlern), die während der Skriptkompilierung oder-Ausführung ausgelöst wurden.</span><span class="sxs-lookup"><span data-stu-id="f299b-288">Detailed information about exception (or error) that was thrown during script compilation or execution.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="f299b-289">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f299b-289">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="f299b-290">Ausnahme-Nr</span><span class="sxs-lookup"><span data-stu-id="f299b-290">exceptionId</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="f299b-291">Ausnahme-ID.</span><span class="sxs-lookup"><span data-stu-id="f299b-291">Exception id.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="f299b-292">Text</span><span class="sxs-lookup"><span data-stu-id="f299b-292">text</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="f299b-293">Ausnahmetext, der bei Verfügbarkeit zusammen mit Ausnahmeobjekt verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="f299b-293">Exception text, which should be used together with exception object when available.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="f299b-294">LineNumber</span><span class="sxs-lookup"><span data-stu-id="f299b-294">lineNumber</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="f299b-295">Die Leitungsnummer des Ausnahme Speicherorts (0-basiert).</span><span class="sxs-lookup"><span data-stu-id="f299b-295">Line number of the exception location (0-based).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="f299b-296">ColumnNumber</span><span class="sxs-lookup"><span data-stu-id="f299b-296">columnNumber</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="f299b-297">Spaltennummer des Ausnahme Speicherorts (0-basiert).</span><span class="sxs-lookup"><span data-stu-id="f299b-297">Column number of the exception location (0-based).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="f299b-298">SkriptID</span><span class="sxs-lookup"><span data-stu-id="f299b-298">scriptId</span></span> <br/> <i><span data-ttu-id="f299b-299">Optional</span><span class="sxs-lookup"><span data-stu-id="f299b-299">optional</span></span></i></td>
            <td><a href="#scriptid"><code class="flyout">ScriptId</code></a></td>
            <td><span data-ttu-id="f299b-300">Skript-ID des Ausnahme Speicherorts.</span><span class="sxs-lookup"><span data-stu-id="f299b-300">Script ID of the exception location.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="f299b-301">URL</span><span class="sxs-lookup"><span data-stu-id="f299b-301">url</span></span> <br/> <i><span data-ttu-id="f299b-302">Optional</span><span class="sxs-lookup"><span data-stu-id="f299b-302">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="f299b-303">Die URL des Ausnahme Speicherorts, die verwendet werden soll, wenn das Skript nicht gemeldet wurde.</span><span class="sxs-lookup"><span data-stu-id="f299b-303">URL of the exception location, to be used when the script was not reported.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="f299b-304">StackTrace</span><span class="sxs-lookup"><span data-stu-id="f299b-304">stackTrace</span></span> <br/> <i><span data-ttu-id="f299b-305">Optional</span><span class="sxs-lookup"><span data-stu-id="f299b-305">optional</span></span></i></td>
            <td><a href="#stacktrace"><code class="flyout">StackTrace</code></a></td>
            <td><span data-ttu-id="f299b-306">JavaScript-Stapelüberwachung, falls verfügbar.</span><span class="sxs-lookup"><span data-stu-id="f299b-306">JavaScript stack trace if available.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="f299b-307">Ausnahme</span><span class="sxs-lookup"><span data-stu-id="f299b-307">exception</span></span> <br/> <i><span data-ttu-id="f299b-308">Optional</span><span class="sxs-lookup"><span data-stu-id="f299b-308">optional</span></span></i></td>
            <td><a href="#remoteobject"><code class="flyout">RemoteObject</code></a></td>
            <td><span data-ttu-id="f299b-309">Exception-Objekt, falls verfügbar.</span><span class="sxs-lookup"><span data-stu-id="f299b-309">Exception object if available.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="f299b-310">executionContextId</span><span class="sxs-lookup"><span data-stu-id="f299b-310">executionContextId</span></span> <br/> <i><span data-ttu-id="f299b-311">Optional</span><span class="sxs-lookup"><span data-stu-id="f299b-311">optional</span></span></i></td>
            <td><a href="#executioncontextid"><code class="flyout">ExecutionContextId</code></a></td>
            <td><span data-ttu-id="f299b-312">Der Bezeichner des Kontexts, in dem die Ausnahme aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="f299b-312">Identifier of the context where exception happened.</span></span></td>
        </tr>
    </tbody>
</table>

---

### <a name="timestamp"></a> <span data-ttu-id="f299b-313">Zeitstempel</span><span class="sxs-lookup"><span data-stu-id="f299b-313">Timestamp</span></span> `integer`

<span data-ttu-id="f299b-314">Die Anzahl der Millisekunden seit Epoch.</span><span class="sxs-lookup"><span data-stu-id="f299b-314">Number of milliseconds since epoch.</span></span>


---

### <a name="callframe"></a> <span data-ttu-id="f299b-315">CallFrame</span><span class="sxs-lookup"><span data-stu-id="f299b-315">CallFrame</span></span> `object`

<span data-ttu-id="f299b-316">Stapel Eintrag für Runtime-Fehler und Assertionen</span><span class="sxs-lookup"><span data-stu-id="f299b-316">Stack entry for runtime errors and assertions.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="f299b-317">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f299b-317">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="f299b-318">FunctionName</span><span class="sxs-lookup"><span data-stu-id="f299b-318">functionName</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="f299b-319">JavaScript-Funktionsname.</span><span class="sxs-lookup"><span data-stu-id="f299b-319">JavaScript function name.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="f299b-320">SkriptID</span><span class="sxs-lookup"><span data-stu-id="f299b-320">scriptId</span></span></td>
            <td><a href="#scriptid"><code class="flyout">ScriptId</code></a></td>
            <td><span data-ttu-id="f299b-321">JavaScript-Skript-ID.</span><span class="sxs-lookup"><span data-stu-id="f299b-321">JavaScript script id.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="f299b-322">URL</span><span class="sxs-lookup"><span data-stu-id="f299b-322">url</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="f299b-323">JavaScript-Skriptname oder-URL.</span><span class="sxs-lookup"><span data-stu-id="f299b-323">JavaScript script name or url.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="f299b-324">LineNumber</span><span class="sxs-lookup"><span data-stu-id="f299b-324">lineNumber</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="f299b-325">JavaScript-Skript-Leitungsnummer (0-basiert).</span><span class="sxs-lookup"><span data-stu-id="f299b-325">JavaScript script line number (0-based).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="f299b-326">ColumnNumber</span><span class="sxs-lookup"><span data-stu-id="f299b-326">columnNumber</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="f299b-327">JavaScript-Skript-Spaltennummer (0-basiert)</span><span class="sxs-lookup"><span data-stu-id="f299b-327">JavaScript script column number (0-based).</span></span></td>
        </tr>
    </tbody>
</table>

---

### <a name="stacktrace"></a> <span data-ttu-id="f299b-328">StackTrace</span><span class="sxs-lookup"><span data-stu-id="f299b-328">StackTrace</span></span> `object`

<span data-ttu-id="f299b-329">Anruf Rahmen für Assertionen oder Fehlermeldungen.</span><span class="sxs-lookup"><span data-stu-id="f299b-329">Call frames for assertions or error messages.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="f299b-330">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f299b-330">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="f299b-331">description</span><span class="sxs-lookup"><span data-stu-id="f299b-331">description</span></span> <br/> <i><span data-ttu-id="f299b-332">Optional</span><span class="sxs-lookup"><span data-stu-id="f299b-332">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="f299b-333">Zeichenfolgenbeschriftung dieser Stapelüberwachung.</span><span class="sxs-lookup"><span data-stu-id="f299b-333">String label of this stack trace.</span></span> <span data-ttu-id="f299b-334">Bei asynchronen Ablaufverfolgungen kann dies ein Name der Funktion sein, die den asynchronen Aufruf initiiert hat.</span><span class="sxs-lookup"><span data-stu-id="f299b-334">For async traces this may be a name of the function that initiated the async call.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="f299b-335">callFrames</span><span class="sxs-lookup"><span data-stu-id="f299b-335">callFrames</span></span></td>
            <td><a href="#callframe"><code class="flyout">CallFrame[]</code></a></td>
            <td><span data-ttu-id="f299b-336">JavaScript-Funktionsname.</span><span class="sxs-lookup"><span data-stu-id="f299b-336">JavaScript function name.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="f299b-337">Eltern</span><span class="sxs-lookup"><span data-stu-id="f299b-337">parent</span></span> <br/> <i><span data-ttu-id="f299b-338">Optional</span><span class="sxs-lookup"><span data-stu-id="f299b-338">optional</span></span></i></td>
            <td><a href="#stacktrace"><code class="flyout">StackTrace</code></a></td>
            <td><span data-ttu-id="f299b-339">Asynchrone JavaScript-Stapelüberwachung, die diesem Stapel vorausging (sofern verfügbar).</span><span class="sxs-lookup"><span data-stu-id="f299b-339">Asynchronous JavaScript stack trace that preceded this stack, if available.</span></span></td>
        </tr>
    </tbody>
</table>

---
