---
description: Referenz für die Runtime-Domäne. Runtime-Domäne macht JavaScript-Runtime mithilfe von Remote Auswertungs-und Spiegel Objekten verfügbar. Evaluierungsergebnisse werden als Spiegelungs Objekt zurückgegeben, die den Objekttyp, die Zeichenfolgendarstellung und den eindeutigen Bezeichner verfügbar machen, die für weitere Objektverweise verwendet werden können. Ursprüngliche Objekte werden im Arbeitsspeicher verwaltet, sofern Sie nicht explizit freigegeben werden.
title: Runtime Domain-devtools Protocol Version 0,2
author: pelavall
ms.author: pelavall
ms.date: 8/17/2018
ms.topic: reference
ms.prod: microsoft-edge
ms.openlocfilehash: 504f944f7a8389450685b40cdd010b54c3a7ba4e
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10567529"
---
# <span data-ttu-id="b2d9a-106">Runtime</span><span class="sxs-lookup"><span data-stu-id="b2d9a-106">Runtime</span></span>
<span data-ttu-id="b2d9a-107">Runtime-Domäne macht JavaScript-Runtime mithilfe von Remote Auswertungs-und Spiegel Objekten verfügbar.</span><span class="sxs-lookup"><span data-stu-id="b2d9a-107">Runtime domain exposes JavaScript runtime by means of remote evaluation and mirror objects.</span></span> <span data-ttu-id="b2d9a-108">Evaluierungsergebnisse werden als Spiegelungs Objekt zurückgegeben, die den Objekttyp, die Zeichenfolgendarstellung und den eindeutigen Bezeichner verfügbar machen, die für weitere Objektverweise verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="b2d9a-108">Evaluation results are returned as mirror object that expose object type, string representation and unique identifier that can be used for further object reference.</span></span> <span data-ttu-id="b2d9a-109">Ursprüngliche Objekte werden im Arbeitsspeicher verwaltet, sofern Sie nicht explizit freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="b2d9a-109">Original objects are maintained in memory unless they are either explicitly released.</span></span>

| | |
|-|-|
| [**<span data-ttu-id="b2d9a-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="b2d9a-110">Methods</span></span>**](#methods) | <span data-ttu-id="b2d9a-111">[aktivieren](#enable), [Deaktivieren](#disable), [Auswerten](#evaluate), [callFunctionOn](#callfunctionon), [awaitPromise](#awaitpromise), [GetProperties](#getproperties), [globalLexicalScopeNames](#globallexicalscopenames), [ReleaseObject](#releaseobject), [releaseObjectGroup](#releaseobjectgroup), [discardConsoleEntries](#discardconsoleentries)</span><span class="sxs-lookup"><span data-stu-id="b2d9a-111">[enable](#enable), [disable](#disable), [evaluate](#evaluate), [callFunctionOn](#callfunctionon), [awaitPromise](#awaitpromise), [getProperties](#getproperties), [globalLexicalScopeNames](#globallexicalscopenames), [releaseObject](#releaseobject), [releaseObjectGroup](#releaseobjectgroup), [discardConsoleEntries](#discardconsoleentries)</span></span> |
| [**<span data-ttu-id="b2d9a-112">Ereignisse</span><span class="sxs-lookup"><span data-stu-id="b2d9a-112">Events</span></span>**](#events) | <span data-ttu-id="b2d9a-113">[executionContextCreated](#executioncontextcreated), [executionContextDestroyed](#executioncontextdestroyed), [executionContextsCleared](#executioncontextscleared), [exceptionThrown](#exceptionthrown), [consoleAPICalled](#consoleapicalled)</span><span class="sxs-lookup"><span data-stu-id="b2d9a-113">[executionContextCreated](#executioncontextcreated), [executionContextDestroyed](#executioncontextdestroyed), [executionContextsCleared](#executioncontextscleared), [exceptionThrown](#exceptionthrown), [consoleAPICalled](#consoleapicalled)</span></span> |
| [**<span data-ttu-id="b2d9a-114">Typen</span><span class="sxs-lookup"><span data-stu-id="b2d9a-114">Types</span></span>**](#types) | <span data-ttu-id="b2d9a-115">[Skript](#scriptid)- [RemoteObjectId](#remoteobjectid), [unserializablevalue](#unserializablevalue), [,](#remoteobject) [PropertyDescriptor](#propertydescriptor), [CallArgument](#callargument), [ExecutionContextId](#executioncontextid), [ExecutionContextDescription](#executioncontextdescription), [ExceptionDetails](#exceptiondetails), [timestamp](#timestamp), [CallFrame](#callframe), [StackTrace](#stacktrace)</span><span class="sxs-lookup"><span data-stu-id="b2d9a-115">[ScriptId](#scriptid), [RemoteObjectId](#remoteobjectid), [UnserializableValue](#unserializablevalue), [RemoteObject](#remoteobject), [PropertyDescriptor](#propertydescriptor), [CallArgument](#callargument), [ExecutionContextId](#executioncontextid), [ExecutionContextDescription](#executioncontextdescription), [ExceptionDetails](#exceptiondetails), [Timestamp](#timestamp), [CallFrame](#callframe), [StackTrace](#stacktrace)</span></span> |
## <span data-ttu-id="b2d9a-116">Methoden</span><span class="sxs-lookup"><span data-stu-id="b2d9a-116">Methods</span></span>

### <span data-ttu-id="b2d9a-117">Aktivieren</span><span class="sxs-lookup"><span data-stu-id="b2d9a-117">enable</span></span>
<span data-ttu-id="b2d9a-118">Ermöglicht die Berichterstellung <code>executionContextCreated</code> <code>executionContextDestroyed</code> und die <code>executionContextsCleared</code> Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="b2d9a-118">Enables reporting of the <code>executionContextCreated</code>, <code>executionContextDestroyed</code> and <code>executionContextsCleared</code> events.</span></span> <span data-ttu-id="b2d9a-119">Wenn die Berichterstellung aktiviert wird <code>executionContextCreated</code> , wird das Ereignis für jeden vorhandenen Ausführungskontext sofort gesendet.</span><span class="sxs-lookup"><span data-stu-id="b2d9a-119">When the reporting gets enabled the <code>executionContextCreated</code> event will be sent immediately for each existing execution context.</span></span>

</p>

---

### <span data-ttu-id="b2d9a-120">Deaktivieren </span><span class="sxs-lookup"><span data-stu-id="b2d9a-120">disable</span></span>
<span data-ttu-id="b2d9a-121">Deaktiviert die Berichterstellung und die <code>executionContextCreated</code> <code>executionContextDestroyed</code> <code>executionContextsCleared</code> Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="b2d9a-121">Disables reporting of the <code>executionContextCreated</code>, <code>executionContextDestroyed</code> and <code>executionContextsCleared</code> events.</span></span>

</p>

---

### <span data-ttu-id="b2d9a-122">bewerten</span><span class="sxs-lookup"><span data-stu-id="b2d9a-122">evaluate</span></span>
<span data-ttu-id="b2d9a-123">Wertet Ausdruck für globales Objekt aus.</span><span class="sxs-lookup"><span data-stu-id="b2d9a-123">Evaluates expression on global object.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="b2d9a-124">Parameter</span><span class="sxs-lookup"><span data-stu-id="b2d9a-124">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="b2d9a-125">Ausdruck</span><span class="sxs-lookup"><span data-stu-id="b2d9a-125">expression</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="b2d9a-126">Ausdruck, der ausgewertet werden soll.</span><span class="sxs-lookup"><span data-stu-id="b2d9a-126">Expression to evaluate.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="b2d9a-127">includeCommandLineAPI</span><span class="sxs-lookup"><span data-stu-id="b2d9a-127">includeCommandLineAPI</span></span> <br/> <i><span data-ttu-id="b2d9a-128">Optional</span><span class="sxs-lookup"><span data-stu-id="b2d9a-128">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="b2d9a-129">Bestimmt, ob die Befehlszeilen-API während der Auswertung verfügbar sein soll.</span><span class="sxs-lookup"><span data-stu-id="b2d9a-129">Determines whether Command Line API should be available during the evaluation.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="b2d9a-130">objectGroup</span><span class="sxs-lookup"><span data-stu-id="b2d9a-130">objectGroup</span></span> <br/> <i><span data-ttu-id="b2d9a-131">Optional</span><span class="sxs-lookup"><span data-stu-id="b2d9a-131">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="b2d9a-132">Symbolischer Gruppenname, der zum Freigeben mehrerer Objekte verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="b2d9a-132">Symbolic group name that can be used to release multiple objects.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="b2d9a-133">lautlos</span><span class="sxs-lookup"><span data-stu-id="b2d9a-133">silent</span></span> <br/> <i><span data-ttu-id="b2d9a-134">Optional</span><span class="sxs-lookup"><span data-stu-id="b2d9a-134">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="b2d9a-135">Im unbeaufsichtigten Modus werden während der Auswertung ausgelöste Ausnahmen nicht gemeldet, und die Ausführung wird nicht angehalten.</span><span class="sxs-lookup"><span data-stu-id="b2d9a-135">In silent mode exceptions thrown during evaluation are not reported and do not pause execution.</span></span> <span data-ttu-id="b2d9a-136">Überschreibt den <code>setPauseOnException</code> Zustand.</span><span class="sxs-lookup"><span data-stu-id="b2d9a-136">Overrides <code>setPauseOnException</code> state.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="b2d9a-137">ContextId</span><span class="sxs-lookup"><span data-stu-id="b2d9a-137">contextId</span></span> <br/> <i><span data-ttu-id="b2d9a-138">Optional</span><span class="sxs-lookup"><span data-stu-id="b2d9a-138">optional</span></span></i></td>
            <td><a href="#executioncontextid"><code class="flyout">ExecutionContextId</code></a></td>
            <td><span data-ttu-id="b2d9a-139">Gibt an, in welchem Ausführungskontext die Auswertung durchgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="b2d9a-139">Specifies in which execution context to perform evaluation.</span></span> <span data-ttu-id="b2d9a-140">Wenn der Parameter ausgelassen wird, wird die Auswertung im Kontext der geprüften Seite durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="b2d9a-140">If the parameter is omitted the evaluation will be performed in the context of the inspected page.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="b2d9a-141">returnByValue</span><span class="sxs-lookup"><span data-stu-id="b2d9a-141">returnByValue</span></span> <br/> <i><span data-ttu-id="b2d9a-142">Optional</span><span class="sxs-lookup"><span data-stu-id="b2d9a-142">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="b2d9a-143">Gibt an, ob es sich bei dem Ergebnis um ein JSON-Objekt handelt, das als Wert gesendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="b2d9a-143">Whether the result is expected to be a JSON object that should be sent by value.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="b2d9a-144">awaitPromise</span><span class="sxs-lookup"><span data-stu-id="b2d9a-144">awaitPromise</span></span> <br/> <i><span data-ttu-id="b2d9a-145">Optional</span><span class="sxs-lookup"><span data-stu-id="b2d9a-145">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="b2d9a-146">Ob die Ausführung <code>await</code> für den resultierenden Wert und die Rückgabe nach dem erwarteten Versprechen aufgelöst werden soll.</span><span class="sxs-lookup"><span data-stu-id="b2d9a-146">Whether execution should <code>await</code> for resulting value and return once awaited promise is resolved.</span></span></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="b2d9a-147">Gibt</span><span class="sxs-lookup"><span data-stu-id="b2d9a-147">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="b2d9a-148">Ergebnis</span><span class="sxs-lookup"><span data-stu-id="b2d9a-148">result</span></span></td>
            <td><a href="#remoteobject"><code class="flyout">RemoteObject</code></a></td>
            <td><span data-ttu-id="b2d9a-149">Auswertungsergebnis.</span><span class="sxs-lookup"><span data-stu-id="b2d9a-149">Evaluation result.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="b2d9a-150">callFunctionOn</span><span class="sxs-lookup"><span data-stu-id="b2d9a-150">callFunctionOn</span></span>
<span data-ttu-id="b2d9a-151">Calls-Funktion mit einer angegebenen Deklaration für das angegebene Objekt.</span><span class="sxs-lookup"><span data-stu-id="b2d9a-151">Calls function with given declaration on the given object.</span></span> <span data-ttu-id="b2d9a-152">Die Objektgruppe des Ergebnisses wird vom Zielobjekt geerbt.</span><span class="sxs-lookup"><span data-stu-id="b2d9a-152">Object group of the result is inherited from the target object.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="b2d9a-153">Parameter</span><span class="sxs-lookup"><span data-stu-id="b2d9a-153">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="b2d9a-154">functionDeclaration</span><span class="sxs-lookup"><span data-stu-id="b2d9a-154">functionDeclaration</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="b2d9a-155">Die Deklaration der Funktion, die aufgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="b2d9a-155">Declaration of the function to call.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="b2d9a-156">ObjectID</span><span class="sxs-lookup"><span data-stu-id="b2d9a-156">objectId</span></span> <br/> <i><span data-ttu-id="b2d9a-157">Optional</span><span class="sxs-lookup"><span data-stu-id="b2d9a-157">optional</span></span></i></td>
            <td><a href="#remoteobjectid"><code class="flyout">RemoteObjectId</code></a></td>
            <td><span data-ttu-id="b2d9a-158">Der Bezeichner des Objekts, für das die Funktion aufgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="b2d9a-158">Identifier of the object to call function on.</span></span> <span data-ttu-id="b2d9a-159">Es sollten entweder ObjectID oder executionContextId angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="b2d9a-159">Either objectId or executionContextId should be specified.</span></span>  <span data-ttu-id="b2d9a-160">ObjectID muss aus der Runtime. Evaluate ()-Funktion sein.</span><span class="sxs-lookup"><span data-stu-id="b2d9a-160">objectId must be from the Runtime.evaluate() function.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="b2d9a-161">arguments</span><span class="sxs-lookup"><span data-stu-id="b2d9a-161">arguments</span></span> <br/> <i><span data-ttu-id="b2d9a-162">Optional</span><span class="sxs-lookup"><span data-stu-id="b2d9a-162">optional</span></span></i></td>
            <td><a href="#callargument"><code class="flyout">CallArgument[]</code></a></td>
            <td><span data-ttu-id="b2d9a-163">Rufen Sie Argumente auf.</span><span class="sxs-lookup"><span data-stu-id="b2d9a-163">Call arguments.</span></span> <span data-ttu-id="b2d9a-164">Alle Anruf Argumente müssen zur gleichen JavaScript-Welt gehören wie das Zielobjekt.</span><span class="sxs-lookup"><span data-stu-id="b2d9a-164">All call arguments must belong to the same JavaScript world as the target object.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="b2d9a-165">lautlos</span><span class="sxs-lookup"><span data-stu-id="b2d9a-165">silent</span></span> <br/> <i><span data-ttu-id="b2d9a-166">Optional</span><span class="sxs-lookup"><span data-stu-id="b2d9a-166">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="b2d9a-167">Im unbeaufsichtigten Modus werden während der Auswertung ausgelöste Ausnahmen nicht gemeldet, und die Ausführung wird nicht angehalten.</span><span class="sxs-lookup"><span data-stu-id="b2d9a-167">In silent mode exceptions thrown during evaluation are not reported and do not pause execution.</span></span> <span data-ttu-id="b2d9a-168">Überschreibt den <code>setPauseOnException</code> Zustand.</span><span class="sxs-lookup"><span data-stu-id="b2d9a-168">Overrides <code>setPauseOnException</code> state.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="b2d9a-169">returnByValue</span><span class="sxs-lookup"><span data-stu-id="b2d9a-169">returnByValue</span></span> <br/> <i><span data-ttu-id="b2d9a-170">Optional</span><span class="sxs-lookup"><span data-stu-id="b2d9a-170">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="b2d9a-171">Gibt an, ob es sich bei dem Ergebnis um ein JSON-Objekt handelt, das als Wert gesendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="b2d9a-171">Whether the result is expected to be a JSON object which should be sent by value.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="b2d9a-172">awaitPromise</span><span class="sxs-lookup"><span data-stu-id="b2d9a-172">awaitPromise</span></span> <br/> <i><span data-ttu-id="b2d9a-173">Optional</span><span class="sxs-lookup"><span data-stu-id="b2d9a-173">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="b2d9a-174">Ob die Ausführung <code>await</code> für den resultierenden Wert und die Rückgabe nach dem erwarteten Versprechen aufgelöst werden soll.</span><span class="sxs-lookup"><span data-stu-id="b2d9a-174">Whether execution should <code>await</code> for resulting value and return once awaited promise is resolved.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="b2d9a-175">executionContextId</span><span class="sxs-lookup"><span data-stu-id="b2d9a-175">executionContextId</span></span> <br/> <i><span data-ttu-id="b2d9a-176">Optional</span><span class="sxs-lookup"><span data-stu-id="b2d9a-176">optional</span></span></i></td>
            <td><a href="#executioncontextid"><code class="flyout">ExecutionContextId</code></a></td>
            <td><span data-ttu-id="b2d9a-177">Gibt den Ausführungskontext an, auf dem das globale Objekt zum Aufrufen von Funktion verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="b2d9a-177">Specifies execution context which global object will be used to call function on.</span></span> <span data-ttu-id="b2d9a-178">Entweder executionContextId oder ObjectID sollte angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="b2d9a-178">Either executionContextId or objectId should be specified.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="b2d9a-179">objectGroup</span><span class="sxs-lookup"><span data-stu-id="b2d9a-179">objectGroup</span></span> <br/> <i><span data-ttu-id="b2d9a-180">Optional</span><span class="sxs-lookup"><span data-stu-id="b2d9a-180">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="b2d9a-181">Symbolischer Gruppenname, der zum Freigeben mehrerer Objekte verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="b2d9a-181">Symbolic group name that can be used to release multiple objects.</span></span> <span data-ttu-id="b2d9a-182">Wenn objectgroup nicht angegeben ist und ObjectID ist, wird objectgroup von Object geerbt.</span><span class="sxs-lookup"><span data-stu-id="b2d9a-182">If objectGroup is not specified and objectId is, objectGroup will be inherited from object.</span></span></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="b2d9a-183">Gibt</span><span class="sxs-lookup"><span data-stu-id="b2d9a-183">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="b2d9a-184">Ergebnis</span><span class="sxs-lookup"><span data-stu-id="b2d9a-184">result</span></span></td>
            <td><a href="#remoteobject"><code class="flyout">RemoteObject</code></a></td>
            <td><span data-ttu-id="b2d9a-185">Ergebnis des Anrufs.</span><span class="sxs-lookup"><span data-stu-id="b2d9a-185">Call result.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="b2d9a-186">awaitPromise</span><span class="sxs-lookup"><span data-stu-id="b2d9a-186">awaitPromise</span></span>
<span data-ttu-id="b2d9a-187">Hinzufügen eines Handlers zum Versprechen mit der angegebenen Promise-Objekt-ID.</span><span class="sxs-lookup"><span data-stu-id="b2d9a-187">Add handler to promise with given promise object id.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="b2d9a-188">Parameter</span><span class="sxs-lookup"><span data-stu-id="b2d9a-188">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="b2d9a-189">promiseObjectId</span><span class="sxs-lookup"><span data-stu-id="b2d9a-189">promiseObjectId</span></span></td>
            <td><a href="#remoteobjectid"><code class="flyout">RemoteObjectId</code></a></td>
            <td><span data-ttu-id="b2d9a-190">Bezeichner des Versprechens.</span><span class="sxs-lookup"><span data-stu-id="b2d9a-190">Identifier of the promise.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="b2d9a-191">returnByValue</span><span class="sxs-lookup"><span data-stu-id="b2d9a-191">returnByValue</span></span> <br/> <i><span data-ttu-id="b2d9a-192">Optional</span><span class="sxs-lookup"><span data-stu-id="b2d9a-192">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="b2d9a-193">Gibt an, ob es sich bei dem Ergebnis um ein JSON-Objekt handelt, das als Wert gesendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="b2d9a-193">Whether the result is expected to be a JSON object that should be sent by value.</span></span></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="b2d9a-194">Gibt</span><span class="sxs-lookup"><span data-stu-id="b2d9a-194">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="b2d9a-195">Ergebnis</span><span class="sxs-lookup"><span data-stu-id="b2d9a-195">result</span></span></td>
            <td><a href="#remoteobject"><code class="flyout">RemoteObject</code></a></td>
            <td><span data-ttu-id="b2d9a-196">Ergebnis versprechen.</span><span class="sxs-lookup"><span data-stu-id="b2d9a-196">Promise result.</span></span>  <span data-ttu-id="b2d9a-197">Enthält einen abgelehnten Wert, wenn Promise abgelehnt wurde.</span><span class="sxs-lookup"><span data-stu-id="b2d9a-197">Will contain rejected value if promise was rejected.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="b2d9a-198">GetProperties</span><span class="sxs-lookup"><span data-stu-id="b2d9a-198">getProperties</span></span>
<span data-ttu-id="b2d9a-199">Gibt Eigenschaften eines angegebenen Objekts zurück.</span><span class="sxs-lookup"><span data-stu-id="b2d9a-199">Returns properties of a given object.</span></span> <span data-ttu-id="b2d9a-200">Die Objektgruppe des Ergebnisses wird vom Zielobjekt geerbt.</span><span class="sxs-lookup"><span data-stu-id="b2d9a-200">Object group of the result is inherited from the target object.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="b2d9a-201">Parameter</span><span class="sxs-lookup"><span data-stu-id="b2d9a-201">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="b2d9a-202">ObjectID</span><span class="sxs-lookup"><span data-stu-id="b2d9a-202">objectId</span></span></td>
            <td><a href="#remoteobjectid"><code class="flyout">RemoteObjectId</code></a></td>
            <td><span data-ttu-id="b2d9a-203">Der Bezeichner des Objekts, für das Eigenschaften zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="b2d9a-203">Identifier of the object to return properties for.</span></span> <span data-ttu-id="b2d9a-204">ObjectID muss aus der Debugger. evaluateOnCallFrame ()-Funktion sein.</span><span class="sxs-lookup"><span data-stu-id="b2d9a-204">objectId must be from the Debugger.evaluateOnCallFrame() function.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="b2d9a-205">ownProperties</span><span class="sxs-lookup"><span data-stu-id="b2d9a-205">ownProperties</span></span> <br/> <i><span data-ttu-id="b2d9a-206">Optional</span><span class="sxs-lookup"><span data-stu-id="b2d9a-206">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="b2d9a-207">Ist "true", gibt Eigenschaften zurück, die nur dem Element selbst und nicht der zugehörigen Prototypkette gehören.</span><span class="sxs-lookup"><span data-stu-id="b2d9a-207">If true, returns properties belonging only to the element itself, not to its prototype chain.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="b2d9a-208">accessorPropertiesOnly</span><span class="sxs-lookup"><span data-stu-id="b2d9a-208">accessorPropertiesOnly</span></span> <br/> <i><span data-ttu-id="b2d9a-209">Optional</span><span class="sxs-lookup"><span data-stu-id="b2d9a-209">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span><b><span data-ttu-id="b2d9a-210">Experimenteller.</span><span class="sxs-lookup"><span data-stu-id="b2d9a-210">Experimental.</span></span> </b></span><span data-ttu-id="b2d9a-211">Ist "true", gibt nur Accessor-Eigenschaften (mit Getter/Setter) zurück. interne Eigenschaften werden auch nicht zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="b2d9a-211">If true, returns accessor properties (with getter/setter) only; internal properties are not returned either.</span></span></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="b2d9a-212">Gibt</span><span class="sxs-lookup"><span data-stu-id="b2d9a-212">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="b2d9a-213">Ergebnis</span><span class="sxs-lookup"><span data-stu-id="b2d9a-213">result</span></span></td>
            <td><a href="#propertydescriptor"><code class="flyout">PropertyDescriptor[]</code></a></td>
            <td><span data-ttu-id="b2d9a-214">Objekteigenschaften.</span><span class="sxs-lookup"><span data-stu-id="b2d9a-214">Object properties.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="b2d9a-215">globalLexicalScopeNames</span><span class="sxs-lookup"><span data-stu-id="b2d9a-215">globalLexicalScopeNames</span></span>
<span data-ttu-id="b2d9a-216">Gibt alle Let-, const-und Class-Variablen aus dem globalen Bereich der Konsole zurück.</span><span class="sxs-lookup"><span data-stu-id="b2d9a-216">Returns all let, const, and class variables from the console global scope.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="b2d9a-217">Gibt</span><span class="sxs-lookup"><span data-stu-id="b2d9a-217">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="b2d9a-218">Namen</span><span class="sxs-lookup"><span data-stu-id="b2d9a-218">names</span></span></td>
            <td><code class="flyout">string[]</code></td>
            <td></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="b2d9a-219">ReleaseObject</span><span class="sxs-lookup"><span data-stu-id="b2d9a-219">releaseObject</span></span>
<span data-ttu-id="b2d9a-220">Gibt das Remoteobjekt mit der angegebenen ID frei.</span><span class="sxs-lookup"><span data-stu-id="b2d9a-220">Releases remote object with given id.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="b2d9a-221">Parameter</span><span class="sxs-lookup"><span data-stu-id="b2d9a-221">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="b2d9a-222">ObjectID</span><span class="sxs-lookup"><span data-stu-id="b2d9a-222">objectId</span></span></td>
            <td><a href="#remoteobjectid"><code class="flyout">RemoteObjectId</code></a></td>
            <td><span data-ttu-id="b2d9a-223">Der Bezeichner des freizugebenden Objekts.</span><span class="sxs-lookup"><span data-stu-id="b2d9a-223">Identifier of the object to release.</span></span> </td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="b2d9a-224">releaseObjectGroup</span><span class="sxs-lookup"><span data-stu-id="b2d9a-224">releaseObjectGroup</span></span>
<span data-ttu-id="b2d9a-225">Gibt alle Remoteobjekte frei, die zu einer bestimmten Gruppe gehören.</span><span class="sxs-lookup"><span data-stu-id="b2d9a-225">Releases all remote objects that belong to a given group.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="b2d9a-226">Parameter</span><span class="sxs-lookup"><span data-stu-id="b2d9a-226">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="b2d9a-227">objectGroup</span><span class="sxs-lookup"><span data-stu-id="b2d9a-227">objectGroup</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="b2d9a-228">Name der symbolischen Objektgruppe.</span><span class="sxs-lookup"><span data-stu-id="b2d9a-228">Symbolic object group name.</span></span> </td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="b2d9a-229">discardConsoleEntries</span><span class="sxs-lookup"><span data-stu-id="b2d9a-229">discardConsoleEntries</span></span>
<span data-ttu-id="b2d9a-230">Verwirft gesammelte Ausnahmen und Konsolen-API-Aufrufe.</span><span class="sxs-lookup"><span data-stu-id="b2d9a-230">Discards collected exceptions and console API calls.</span></span>

</p>

---

## <span data-ttu-id="b2d9a-231">Ereignisse</span><span class="sxs-lookup"><span data-stu-id="b2d9a-231">Events</span></span>

### <span data-ttu-id="b2d9a-232">executionContextCreated</span><span class="sxs-lookup"><span data-stu-id="b2d9a-232">executionContextCreated</span></span>
<span data-ttu-id="b2d9a-233">Wird ausgegeben, wenn ein neuer Ausführungskontext erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="b2d9a-233">Issued when new execution context is created.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="b2d9a-234">Parameter</span><span class="sxs-lookup"><span data-stu-id="b2d9a-234">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="b2d9a-235">Kontext</span><span class="sxs-lookup"><span data-stu-id="b2d9a-235">context</span></span></td>
            <td><a href="#executioncontextdescription"><code class="flyout">ExecutionContextDescription</code></a></td>
            <td><span data-ttu-id="b2d9a-236">Ein neu erstellter Ausführungskontext.</span><span class="sxs-lookup"><span data-stu-id="b2d9a-236">A newly created execution context.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="b2d9a-237">executionContextDestroyed</span><span class="sxs-lookup"><span data-stu-id="b2d9a-237">executionContextDestroyed</span></span>
<span data-ttu-id="b2d9a-238">Wird ausgegeben, wenn der Ausführungskontext zerstört wurde.</span><span class="sxs-lookup"><span data-stu-id="b2d9a-238">Issued when execution context is destroyed.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="b2d9a-239">Parameter</span><span class="sxs-lookup"><span data-stu-id="b2d9a-239">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="b2d9a-240">executionContextId</span><span class="sxs-lookup"><span data-stu-id="b2d9a-240">executionContextId</span></span></td>
            <td><a href="#executioncontextid"><code class="flyout">ExecutionContextId</code></a></td>
            <td><span data-ttu-id="b2d9a-241">ID des zerstörten Kontexts</span><span class="sxs-lookup"><span data-stu-id="b2d9a-241">Id of the destroyed context</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="b2d9a-242">executionContextsCleared</span><span class="sxs-lookup"><span data-stu-id="b2d9a-242">executionContextsCleared</span></span>
<span data-ttu-id="b2d9a-243">Wird ausgegeben, wenn alle executionContexts im Browser gelöscht wurden</span><span class="sxs-lookup"><span data-stu-id="b2d9a-243">Issued when all executionContexts were cleared in browser</span></span>

</p>

---

### <span data-ttu-id="b2d9a-244">exceptionThrown</span><span class="sxs-lookup"><span data-stu-id="b2d9a-244">exceptionThrown</span></span>
<span data-ttu-id="b2d9a-245">Wird ausgegeben, wenn eine Ausnahme ausgelöst und nicht behandelt wurde.</span><span class="sxs-lookup"><span data-stu-id="b2d9a-245">Issued when exception was thrown and unhandled.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="b2d9a-246">Parameter</span><span class="sxs-lookup"><span data-stu-id="b2d9a-246">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="b2d9a-247">Timestamp</span><span class="sxs-lookup"><span data-stu-id="b2d9a-247">timestamp</span></span></td>
            <td><a href="#timestamp"><code class="flyout">Timestamp</code></a></td>
            <td><span data-ttu-id="b2d9a-248">Der Zeitstempel der Ausnahme.</span><span class="sxs-lookup"><span data-stu-id="b2d9a-248">Timestamp of the exception.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="b2d9a-249">exceptionDetails</span><span class="sxs-lookup"><span data-stu-id="b2d9a-249">exceptionDetails</span></span></td>
            <td><a href="#exceptiondetails"><code class="flyout">ExceptionDetails</code></a></td>
            <td></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="b2d9a-250">consoleAPICalled</span><span class="sxs-lookup"><span data-stu-id="b2d9a-250">consoleAPICalled</span></span>


<table>
    <thead>
        <tr>
            <th><span data-ttu-id="b2d9a-251">Parameter</span><span class="sxs-lookup"><span data-stu-id="b2d9a-251">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="b2d9a-252">Typ</span><span class="sxs-lookup"><span data-stu-id="b2d9a-252">type</span></span></td>
            <td><code class="flyout">string</code> <br/> <i><span data-ttu-id="b2d9a-253">Zulässige Werte: Protokoll, Info, Warnung, Fehler, Debuggen, Assert, Tabelle, Ablaufverfolgung, dir, DirXML, Clear, SELECT, count, countReset, timeEnd, timestamp, startGroup, startGroupCollapsed, endGroup</span><span class="sxs-lookup"><span data-stu-id="b2d9a-253">Allowed values: log, info, warning, error, debug, assert, table, trace, dir, dirxml, clear, select, count, countReset, timeEnd, timeStamp, startGroup, startGroupCollapsed, endGroup</span></span></i></td>
            <td><span data-ttu-id="b2d9a-254">Der Typ des Anrufs.</span><span class="sxs-lookup"><span data-stu-id="b2d9a-254">Type of the call.</span></span> <span data-ttu-id="b2d9a-255">Dazu gehören Protokoll, Informationen, Warnung, Fehler, Debuggen, Assert, Tabelle, Ablaufverfolgung, dir, DirXML, Clear, SELECT, count, countReset, timeEnd, Exception, timestamp, Group, groupCollapsed, groupEnd.</span><span class="sxs-lookup"><span data-stu-id="b2d9a-255">This includes log, info, warn, error, debug, assert, table, trace, dir, dirxml, clear, select, count, countReset, timeEnd, exception, timeStamp, group, groupCollapsed, groupEnd.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="b2d9a-256">args</span><span class="sxs-lookup"><span data-stu-id="b2d9a-256">args</span></span></td>
            <td><a href="#remoteobject"><code class="flyout">RemoteObject[]</code></a></td>
            <td><span data-ttu-id="b2d9a-257">Rufen Sie Argumente auf.</span><span class="sxs-lookup"><span data-stu-id="b2d9a-257">Call arguments.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="b2d9a-258">executionContextId</span><span class="sxs-lookup"><span data-stu-id="b2d9a-258">executionContextId</span></span></td>
            <td><a href="#executioncontextid"><code class="flyout">ExecutionContextId</code></a></td>
            <td><span data-ttu-id="b2d9a-259">Bezeichner des Kontexts, in dem der Konsolen Aufruf durchgeführt wurde</span><span class="sxs-lookup"><span data-stu-id="b2d9a-259">Identifier of the context where console call was made</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="b2d9a-260">Timestamp</span><span class="sxs-lookup"><span data-stu-id="b2d9a-260">timestamp</span></span> <br/> <i><span data-ttu-id="b2d9a-261">Optional</span><span class="sxs-lookup"><span data-stu-id="b2d9a-261">optional</span></span></i></td>
            <td><a href="#timestamp"><code class="flyout">Timestamp</code></a></td>
            <td><span data-ttu-id="b2d9a-262">Anruf Zeitstempel.</span><span class="sxs-lookup"><span data-stu-id="b2d9a-262">Call timestamp.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="b2d9a-263">StackTrace</span><span class="sxs-lookup"><span data-stu-id="b2d9a-263">stackTrace</span></span> <br/> <i><span data-ttu-id="b2d9a-264">Optional</span><span class="sxs-lookup"><span data-stu-id="b2d9a-264">optional</span></span></i></td>
            <td><a href="#stacktrace"><code class="flyout">StackTrace</code></a></td>
            <td><span data-ttu-id="b2d9a-265">Aufgezeichnete Stapelüberwachung, falls verfügbar</span><span class="sxs-lookup"><span data-stu-id="b2d9a-265">Stack trace captured if available</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

## <span data-ttu-id="b2d9a-266">Typen</span><span class="sxs-lookup"><span data-stu-id="b2d9a-266">Types</span></span>

### <a name="scriptid"></a> <span data-ttu-id="b2d9a-267">SkriptID</span><span class="sxs-lookup"><span data-stu-id="b2d9a-267">ScriptId</span></span> `string`

<span data-ttu-id="b2d9a-268">Eindeutiger Skriptbezeichner.</span><span class="sxs-lookup"><span data-stu-id="b2d9a-268">Unique script identifier.</span></span>

</p>

---

### <a name="remoteobjectid"></a> <span data-ttu-id="b2d9a-269">RemoteObjectId</span><span class="sxs-lookup"><span data-stu-id="b2d9a-269">RemoteObjectId</span></span> `string`

<span data-ttu-id="b2d9a-270">Eindeutige Objekt-ID.</span><span class="sxs-lookup"><span data-stu-id="b2d9a-270">Unique object identifier.</span></span>

</p>

---

### <a name="unserializablevalue"></a> <span data-ttu-id="b2d9a-271">Unserializablevalue</span><span class="sxs-lookup"><span data-stu-id="b2d9a-271">UnserializableValue</span></span> `string`

<span data-ttu-id="b2d9a-272">Primitiver Wert, der nicht JSON-stringified sein kann.</span><span class="sxs-lookup"><span data-stu-id="b2d9a-272">Primitive value which cannot be JSON-stringified.</span></span>

##### <span data-ttu-id="b2d9a-273">Zulässige Werte</span><span class="sxs-lookup"><span data-stu-id="b2d9a-273">Allowed Values</span></span>
<span data-ttu-id="b2d9a-274">Unendlichkeit, Nan,-Unendlichkeit,-0</span><span class="sxs-lookup"><span data-stu-id="b2d9a-274">Infinity, NaN, -Infinity, -0</span></span>
</p>

---

### <a name="remoteobject"></a> <span data-ttu-id="b2d9a-275">RemoteObject</span><span class="sxs-lookup"><span data-stu-id="b2d9a-275">RemoteObject</span></span> `object`

<span data-ttu-id="b2d9a-276">Spiegelungs Objekt, das auf das ursprüngliche JavaScript-Objekt verweist</span><span class="sxs-lookup"><span data-stu-id="b2d9a-276">Mirror object referencing original JavaScript object.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="b2d9a-277">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b2d9a-277">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="b2d9a-278">Typ</span><span class="sxs-lookup"><span data-stu-id="b2d9a-278">type</span></span></td>
            <td><code class="flyout">string</code> <br/> <i><span data-ttu-id="b2d9a-279">Zulässige Werte: Objekt, Funktion, undefined, Zeichenfolge, Zahl, boolescher Wert, Symbol</span><span class="sxs-lookup"><span data-stu-id="b2d9a-279">Allowed values: object, function, undefined, string, number, boolean, symbol</span></span></i></td>
            <td><span data-ttu-id="b2d9a-280">Objekttyp.</span><span class="sxs-lookup"><span data-stu-id="b2d9a-280">Object type.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="b2d9a-281">Untertyp</span><span class="sxs-lookup"><span data-stu-id="b2d9a-281">subtype</span></span> <br/> <i><span data-ttu-id="b2d9a-282">Optional</span><span class="sxs-lookup"><span data-stu-id="b2d9a-282">optional</span></span></i></td>
            <td><code class="flyout">string</code> <br/> <i><span data-ttu-id="b2d9a-283">Zulässige Werte: NULL, Fehler, Promise, Knoten</span><span class="sxs-lookup"><span data-stu-id="b2d9a-283">Allowed values: null, error, promise, node</span></span></i></td>
            <td><span data-ttu-id="b2d9a-284">Hinweis für den Untertyp des Objekts.</span><span class="sxs-lookup"><span data-stu-id="b2d9a-284">Object subtype hint.</span></span> <span data-ttu-id="b2d9a-285">Nur für <code>object</code> Typwerte angegeben.</span><span class="sxs-lookup"><span data-stu-id="b2d9a-285">Specified for <code>object</code> type values only.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="b2d9a-286">ClassName</span><span class="sxs-lookup"><span data-stu-id="b2d9a-286">className</span></span> <br/> <i><span data-ttu-id="b2d9a-287">Optional</span><span class="sxs-lookup"><span data-stu-id="b2d9a-287">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="b2d9a-288">Name der Objektklasse (Konstruktor).</span><span class="sxs-lookup"><span data-stu-id="b2d9a-288">Object class (constructor) name.</span></span> <span data-ttu-id="b2d9a-289">Nur für <code>object</code> Typwerte angegeben.</span><span class="sxs-lookup"><span data-stu-id="b2d9a-289">Specified for <code>object</code> type values only.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="b2d9a-290">value</span><span class="sxs-lookup"><span data-stu-id="b2d9a-290">value</span></span> <br/> <i><span data-ttu-id="b2d9a-291">Optional</span><span class="sxs-lookup"><span data-stu-id="b2d9a-291">optional</span></span></i></td>
            <td><code class="flyout">any</code></td>
            <td><span data-ttu-id="b2d9a-292">Remote Objektwert im Fall von primitiven Werten oder JSON-Werten (sofern angefordert).</span><span class="sxs-lookup"><span data-stu-id="b2d9a-292">Remote object value in case of primitive values or JSON values (if it was requested).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="b2d9a-293">unserializablevalue</span><span class="sxs-lookup"><span data-stu-id="b2d9a-293">unserializableValue</span></span> <br/> <i><span data-ttu-id="b2d9a-294">Optional</span><span class="sxs-lookup"><span data-stu-id="b2d9a-294">optional</span></span></i></td>
            <td><a href="#unserializablevalue"><code class="flyout">UnserializableValue</code></a></td>
            <td><span data-ttu-id="b2d9a-295">Primitiver Wert, der nicht JSON-stringified sein kann</span><span class="sxs-lookup"><span data-stu-id="b2d9a-295">Primitive value which can not be JSON-stringified does not have</span></span> <code>value</code><span data-ttu-id="b2d9a-296">, aber ruft diese Eigenschaft ab.</span><span class="sxs-lookup"><span data-stu-id="b2d9a-296">, but gets this property.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="b2d9a-297">description</span><span class="sxs-lookup"><span data-stu-id="b2d9a-297">description</span></span> <br/> <i><span data-ttu-id="b2d9a-298">Optional</span><span class="sxs-lookup"><span data-stu-id="b2d9a-298">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="b2d9a-299">Zeichenfolgendarstellung des Objekts.</span><span class="sxs-lookup"><span data-stu-id="b2d9a-299">String representation of the object.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="b2d9a-300">ObjectID</span><span class="sxs-lookup"><span data-stu-id="b2d9a-300">objectId</span></span> <br/> <i><span data-ttu-id="b2d9a-301">Optional</span><span class="sxs-lookup"><span data-stu-id="b2d9a-301">optional</span></span></i></td>
            <td><a href="#remoteobjectid"><code class="flyout">RemoteObjectId</code></a></td>
            <td><span data-ttu-id="b2d9a-302">Eindeutige Objekt-ID (für nicht primitive Werte).</span><span class="sxs-lookup"><span data-stu-id="b2d9a-302">Unique object identifier (for non-primitive values).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="b2d9a-303">msDebuggerPropertyId</span><span class="sxs-lookup"><span data-stu-id="b2d9a-303">msDebuggerPropertyId</span></span> <br/> <i><span data-ttu-id="b2d9a-304">Optional</span><span class="sxs-lookup"><span data-stu-id="b2d9a-304">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span><b><span data-ttu-id="b2d9a-305">Experimenteller.</span><span class="sxs-lookup"><span data-stu-id="b2d9a-305">Experimental.</span></span> </b></span><span data-ttu-id="b2d9a-306">Microsoft: die zugeordnete Debugger-Eigenschafts-ID für dieses Objekt.</span><span class="sxs-lookup"><span data-stu-id="b2d9a-306">Microsoft: The associated debugger property id for this object.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="propertydescriptor"></a> <span data-ttu-id="b2d9a-307">PropertyDescriptor</span><span class="sxs-lookup"><span data-stu-id="b2d9a-307">PropertyDescriptor</span></span> `object`

<span data-ttu-id="b2d9a-308">Objekteigenschaften Deskriptor</span><span class="sxs-lookup"><span data-stu-id="b2d9a-308">Object property descriptor.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="b2d9a-309">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b2d9a-309">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="b2d9a-310">name</span><span class="sxs-lookup"><span data-stu-id="b2d9a-310">name</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="b2d9a-311">Eigenschaftsname oder Symbol Beschreibung.</span><span class="sxs-lookup"><span data-stu-id="b2d9a-311">Property name or symbol description.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="b2d9a-312">value</span><span class="sxs-lookup"><span data-stu-id="b2d9a-312">value</span></span> <br/> <i><span data-ttu-id="b2d9a-313">Optional</span><span class="sxs-lookup"><span data-stu-id="b2d9a-313">optional</span></span></i></td>
            <td><a href="#remoteobject"><code class="flyout">RemoteObject</code></a></td>
            <td><span data-ttu-id="b2d9a-314">Der Wert, der der Eigenschaft zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="b2d9a-314">The value associated with the property.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="b2d9a-315">beschreibbar</span><span class="sxs-lookup"><span data-stu-id="b2d9a-315">writable</span></span> <br/> <i><span data-ttu-id="b2d9a-316">Optional</span><span class="sxs-lookup"><span data-stu-id="b2d9a-316">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="b2d9a-317">"True", wenn der Wert, der der Eigenschaft zugeordnet ist, geändert werden kann (nur Daten Deskriptoren).</span><span class="sxs-lookup"><span data-stu-id="b2d9a-317">True if the value associated with the property may be changed (data descriptors only).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="b2d9a-318">Abrufen</span><span class="sxs-lookup"><span data-stu-id="b2d9a-318">get</span></span> <br/> <i><span data-ttu-id="b2d9a-319">Optional</span><span class="sxs-lookup"><span data-stu-id="b2d9a-319">optional</span></span></i></td>
            <td><a href="#remoteobject"><code class="flyout">RemoteObject</code></a></td>
            <td><span data-ttu-id="b2d9a-320">Eine Funktion, die als Getter für die Eigenschaft dient, oder <code>undefined</code> Wenn kein Getter vorhanden ist (nur Accessor-Deskriptoren).</span><span class="sxs-lookup"><span data-stu-id="b2d9a-320">A function which serves as a getter for the property, or <code>undefined</code> if there is no getter (accessor descriptors only).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="b2d9a-321">set</span><span class="sxs-lookup"><span data-stu-id="b2d9a-321">set</span></span> <br/> <i><span data-ttu-id="b2d9a-322">Optional</span><span class="sxs-lookup"><span data-stu-id="b2d9a-322">optional</span></span></i></td>
            <td><a href="#remoteobject"><code class="flyout">RemoteObject</code></a></td>
            <td><span data-ttu-id="b2d9a-323">Eine Funktion, die als Setter für die Eigenschaft dient, oder <code>undefined</code> Wenn kein Setter vorhanden ist (nur Accessor-Deskriptoren).</span><span class="sxs-lookup"><span data-stu-id="b2d9a-323">A function which serves as a setter for the property, or <code>undefined</code> if there is no setter (accessor descriptors only).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="b2d9a-324">konfigurierbar</span><span class="sxs-lookup"><span data-stu-id="b2d9a-324">configurable</span></span></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="b2d9a-325">"True", wenn der Typ dieses Eigenschaftendeskriptors geändert werden kann und die Eigenschaft aus dem entsprechenden Objekt gelöscht werden kann.</span><span class="sxs-lookup"><span data-stu-id="b2d9a-325">True if the type of this property descriptor may be changed and if the property may be deleted from the corresponding object.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="b2d9a-326">Enumerable</span><span class="sxs-lookup"><span data-stu-id="b2d9a-326">enumerable</span></span></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="b2d9a-327">"True", wenn diese Eigenschaft während der Enumeration der Eigenschaften des entsprechenden Objekts angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="b2d9a-327">True if this property shows up during enumeration of the properties on the corresponding object.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="b2d9a-328">wasThrown</span><span class="sxs-lookup"><span data-stu-id="b2d9a-328">wasThrown</span></span> <br/> <i><span data-ttu-id="b2d9a-329">Optional</span><span class="sxs-lookup"><span data-stu-id="b2d9a-329">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="b2d9a-330">"True", wenn das Ergebnis während der Auswertung ausgelöst wurde.</span><span class="sxs-lookup"><span data-stu-id="b2d9a-330">True if the result was thrown during the evaluation.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="b2d9a-331">isOwn</span><span class="sxs-lookup"><span data-stu-id="b2d9a-331">isOwn</span></span> <br/> <i><span data-ttu-id="b2d9a-332">Optional</span><span class="sxs-lookup"><span data-stu-id="b2d9a-332">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="b2d9a-333">"True", wenn die Eigenschaft für das Objekt gehört.</span><span class="sxs-lookup"><span data-stu-id="b2d9a-333">True if the property is owned for the object.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="b2d9a-334">msReturnValue</span><span class="sxs-lookup"><span data-stu-id="b2d9a-334">msReturnValue</span></span> <br/> <i><span data-ttu-id="b2d9a-335">Optional</span><span class="sxs-lookup"><span data-stu-id="b2d9a-335">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span><b><span data-ttu-id="b2d9a-336">Experimenteller.</span><span class="sxs-lookup"><span data-stu-id="b2d9a-336">Experimental.</span></span> </b></span><span data-ttu-id="b2d9a-337">Microsoft: true, wenn die Eigenschaft ein Rückgabewert ist.</span><span class="sxs-lookup"><span data-stu-id="b2d9a-337">Microsoft: True if the property is a return value.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="b2d9a-338">symbol</span><span class="sxs-lookup"><span data-stu-id="b2d9a-338">symbol</span></span> <br/> <i><span data-ttu-id="b2d9a-339">Optional</span><span class="sxs-lookup"><span data-stu-id="b2d9a-339">optional</span></span></i></td>
            <td><a href="#remoteobject"><code class="flyout">RemoteObject</code></a></td>
            <td><span data-ttu-id="b2d9a-340">Eigenschafts Symbol Objekt, wenn die Eigenschaft vom `symbol` Typ ist.</span><span class="sxs-lookup"><span data-stu-id="b2d9a-340">Property symbol object, if the property is of the `symbol` type.</span></span> </td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="callargument"></a> <span data-ttu-id="b2d9a-341">CallArgument</span><span class="sxs-lookup"><span data-stu-id="b2d9a-341">CallArgument</span></span> `object`

<span data-ttu-id="b2d9a-342">Steht für Funktionsaufruf Argument.</span><span class="sxs-lookup"><span data-stu-id="b2d9a-342">Represents function call argument.</span></span> <span data-ttu-id="b2d9a-343">Es sollten entweder die Remoteobjekt-ID <code>objectId</code> , der primitive <code>value</code> , der unserialisierbare primitive Wert oder keines der (für undefined) angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="b2d9a-343">Either remote object id <code>objectId</code>, primitive <code>value</code>, unserializable primitive value or neither of (for undefined) them should be specified.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="b2d9a-344">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b2d9a-344">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="b2d9a-345">value</span><span class="sxs-lookup"><span data-stu-id="b2d9a-345">value</span></span> <br/> <i><span data-ttu-id="b2d9a-346">Optional</span><span class="sxs-lookup"><span data-stu-id="b2d9a-346">optional</span></span></i></td>
            <td><code class="flyout">any</code></td>
            <td><span data-ttu-id="b2d9a-347">Primitiver Wert oder serialisierbares JavaScript-Objekt.</span><span class="sxs-lookup"><span data-stu-id="b2d9a-347">Primitive value or serializable javascript object.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="b2d9a-348">unserializablevalue</span><span class="sxs-lookup"><span data-stu-id="b2d9a-348">unserializableValue</span></span> <br/> <i><span data-ttu-id="b2d9a-349">Optional</span><span class="sxs-lookup"><span data-stu-id="b2d9a-349">optional</span></span></i></td>
            <td><a href="#unserializablevalue"><code class="flyout">UnserializableValue</code></a></td>
            <td><span data-ttu-id="b2d9a-350">Primitiver Wert, der nicht JSON-stringified sein kann.</span><span class="sxs-lookup"><span data-stu-id="b2d9a-350">Primitive value which can not be JSON-stringified.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="b2d9a-351">ObjectID</span><span class="sxs-lookup"><span data-stu-id="b2d9a-351">objectId</span></span> <br/> <i><span data-ttu-id="b2d9a-352">Optional</span><span class="sxs-lookup"><span data-stu-id="b2d9a-352">optional</span></span></i></td>
            <td><a href="#remoteobjectid"><code class="flyout">RemoteObjectId</code></a></td>
            <td><span data-ttu-id="b2d9a-353">Remote Objekthandle.</span><span class="sxs-lookup"><span data-stu-id="b2d9a-353">Remote object handle.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="executioncontextid"></a> <span data-ttu-id="b2d9a-354">ExecutionContextId</span><span class="sxs-lookup"><span data-stu-id="b2d9a-354">ExecutionContextId</span></span> `integer`

<span data-ttu-id="b2d9a-355">Die ID eines Ausführungskontexts.</span><span class="sxs-lookup"><span data-stu-id="b2d9a-355">Id of an execution context.</span></span>

</p>

---

### <a name="executioncontextdescription"></a> <span data-ttu-id="b2d9a-356">ExecutionContextDescription</span><span class="sxs-lookup"><span data-stu-id="b2d9a-356">ExecutionContextDescription</span></span> `object`

<span data-ttu-id="b2d9a-357">Beschreibung einer isolierten Welt.</span><span class="sxs-lookup"><span data-stu-id="b2d9a-357">Description of an isolated world.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="b2d9a-358">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b2d9a-358">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="b2d9a-359">id</span><span class="sxs-lookup"><span data-stu-id="b2d9a-359">id</span></span></td>
            <td><a href="#executioncontextid"><code class="flyout">ExecutionContextId</code></a></td>
            <td><span data-ttu-id="b2d9a-360">Eindeutige ID des Ausführungskontexts.</span><span class="sxs-lookup"><span data-stu-id="b2d9a-360">Unique id of the execution context.</span></span> <span data-ttu-id="b2d9a-361">Sie kann verwendet werden, um anzugeben, in welcher Ausführungskontext Skript Auswertung durchgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="b2d9a-361">It can be used to specify in which execution context script evaluation should be performed.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="b2d9a-362">Ursprung</span><span class="sxs-lookup"><span data-stu-id="b2d9a-362">origin</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="b2d9a-363">Ursprung des Ausführungskontexts.</span><span class="sxs-lookup"><span data-stu-id="b2d9a-363">Execution context origin.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="b2d9a-364">name</span><span class="sxs-lookup"><span data-stu-id="b2d9a-364">name</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="b2d9a-365">Menschlicher lesbarer Name, der den angegebenen Kontext beschreibt.</span><span class="sxs-lookup"><span data-stu-id="b2d9a-365">Human readable name describing given context.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="exceptiondetails"></a> <span data-ttu-id="b2d9a-366">ExceptionDetails</span><span class="sxs-lookup"><span data-stu-id="b2d9a-366">ExceptionDetails</span></span> `object`

<span data-ttu-id="b2d9a-367">Detaillierte Informationen zu Ausnahmen (oder Fehlern), die während der Skriptkompilierung oder-Ausführung ausgelöst wurden.</span><span class="sxs-lookup"><span data-stu-id="b2d9a-367">Detailed information about exception (or error) that was thrown during script compilation or execution.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="b2d9a-368">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b2d9a-368">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="b2d9a-369">Ausnahme-Nr</span><span class="sxs-lookup"><span data-stu-id="b2d9a-369">exceptionId</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="b2d9a-370">Ausnahme-ID.</span><span class="sxs-lookup"><span data-stu-id="b2d9a-370">Exception id.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="b2d9a-371">Text</span><span class="sxs-lookup"><span data-stu-id="b2d9a-371">text</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="b2d9a-372">Ausnahmetext, der bei Verfügbarkeit zusammen mit Ausnahmeobjekt verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="b2d9a-372">Exception text, which should be used together with exception object when available.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="b2d9a-373">LineNumber</span><span class="sxs-lookup"><span data-stu-id="b2d9a-373">lineNumber</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="b2d9a-374">Die Leitungsnummer des Ausnahme Speicherorts (0-basiert).</span><span class="sxs-lookup"><span data-stu-id="b2d9a-374">Line number of the exception location (0-based).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="b2d9a-375">ColumnNumber</span><span class="sxs-lookup"><span data-stu-id="b2d9a-375">columnNumber</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="b2d9a-376">Spaltennummer des Ausnahme Speicherorts (0-basiert).</span><span class="sxs-lookup"><span data-stu-id="b2d9a-376">Column number of the exception location (0-based).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="b2d9a-377">SkriptID</span><span class="sxs-lookup"><span data-stu-id="b2d9a-377">scriptId</span></span> <br/> <i><span data-ttu-id="b2d9a-378">Optional</span><span class="sxs-lookup"><span data-stu-id="b2d9a-378">optional</span></span></i></td>
            <td><a href="#scriptid"><code class="flyout">ScriptId</code></a></td>
            <td><span data-ttu-id="b2d9a-379">Skript-ID des Ausnahme Speicherorts.</span><span class="sxs-lookup"><span data-stu-id="b2d9a-379">Script ID of the exception location.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="b2d9a-380">URL</span><span class="sxs-lookup"><span data-stu-id="b2d9a-380">url</span></span> <br/> <i><span data-ttu-id="b2d9a-381">Optional</span><span class="sxs-lookup"><span data-stu-id="b2d9a-381">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="b2d9a-382">Die URL des Ausnahme Speicherorts, die verwendet werden soll, wenn das Skript nicht gemeldet wurde.</span><span class="sxs-lookup"><span data-stu-id="b2d9a-382">URL of the exception location, to be used when the script was not reported.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="b2d9a-383">StackTrace</span><span class="sxs-lookup"><span data-stu-id="b2d9a-383">stackTrace</span></span> <br/> <i><span data-ttu-id="b2d9a-384">Optional</span><span class="sxs-lookup"><span data-stu-id="b2d9a-384">optional</span></span></i></td>
            <td><a href="#stacktrace"><code class="flyout">StackTrace</code></a></td>
            <td><span data-ttu-id="b2d9a-385">JavaScript-Stapelüberwachung, falls verfügbar.</span><span class="sxs-lookup"><span data-stu-id="b2d9a-385">JavaScript stack trace if available.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="b2d9a-386">Ausnahme</span><span class="sxs-lookup"><span data-stu-id="b2d9a-386">exception</span></span> <br/> <i><span data-ttu-id="b2d9a-387">Optional</span><span class="sxs-lookup"><span data-stu-id="b2d9a-387">optional</span></span></i></td>
            <td><a href="#remoteobject"><code class="flyout">RemoteObject</code></a></td>
            <td><span data-ttu-id="b2d9a-388">Exception-Objekt, falls verfügbar.</span><span class="sxs-lookup"><span data-stu-id="b2d9a-388">Exception object if available.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="b2d9a-389">executionContextId</span><span class="sxs-lookup"><span data-stu-id="b2d9a-389">executionContextId</span></span> <br/> <i><span data-ttu-id="b2d9a-390">Optional</span><span class="sxs-lookup"><span data-stu-id="b2d9a-390">optional</span></span></i></td>
            <td><a href="#executioncontextid"><code class="flyout">ExecutionContextId</code></a></td>
            <td><span data-ttu-id="b2d9a-391">Der Bezeichner des Kontexts, in dem die Ausnahme aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="b2d9a-391">Identifier of the context where exception happened.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="timestamp"></a> <span data-ttu-id="b2d9a-392">Zeitstempel</span><span class="sxs-lookup"><span data-stu-id="b2d9a-392">Timestamp</span></span> `integer`

<span data-ttu-id="b2d9a-393">Die Anzahl der Millisekunden seit Epoch.</span><span class="sxs-lookup"><span data-stu-id="b2d9a-393">Number of milliseconds since epoch.</span></span>

</p>

---

### <a name="callframe"></a> <span data-ttu-id="b2d9a-394">CallFrame</span><span class="sxs-lookup"><span data-stu-id="b2d9a-394">CallFrame</span></span> `object`

<span data-ttu-id="b2d9a-395">Stapel Eintrag für Runtime-Fehler und Assertionen</span><span class="sxs-lookup"><span data-stu-id="b2d9a-395">Stack entry for runtime errors and assertions.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="b2d9a-396">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b2d9a-396">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="b2d9a-397">FunctionName</span><span class="sxs-lookup"><span data-stu-id="b2d9a-397">functionName</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="b2d9a-398">JavaScript-Funktionsname.</span><span class="sxs-lookup"><span data-stu-id="b2d9a-398">JavaScript function name.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="b2d9a-399">SkriptID</span><span class="sxs-lookup"><span data-stu-id="b2d9a-399">scriptId</span></span></td>
            <td><a href="#scriptid"><code class="flyout">ScriptId</code></a></td>
            <td><span data-ttu-id="b2d9a-400">JavaScript-Skript-ID. Die Skript-Nr ist leer, wenn der Debugger nicht aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="b2d9a-400">JavaScript script id. ScriptId will be empty if debugger is not enabled.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="b2d9a-401">URL</span><span class="sxs-lookup"><span data-stu-id="b2d9a-401">url</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="b2d9a-402">JavaScript-Skriptname oder-URL.</span><span class="sxs-lookup"><span data-stu-id="b2d9a-402">JavaScript script name or url.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="b2d9a-403">LineNumber</span><span class="sxs-lookup"><span data-stu-id="b2d9a-403">lineNumber</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="b2d9a-404">JavaScript-Skript-Leitungsnummer (0-basiert).</span><span class="sxs-lookup"><span data-stu-id="b2d9a-404">JavaScript script line number (0-based).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="b2d9a-405">ColumnNumber</span><span class="sxs-lookup"><span data-stu-id="b2d9a-405">columnNumber</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="b2d9a-406">JavaScript-Skript-Spaltennummer (0-basiert)</span><span class="sxs-lookup"><span data-stu-id="b2d9a-406">JavaScript script column number (0-based).</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="stacktrace"></a> <span data-ttu-id="b2d9a-407">StackTrace</span><span class="sxs-lookup"><span data-stu-id="b2d9a-407">StackTrace</span></span> `object`

<span data-ttu-id="b2d9a-408">Anruf Rahmen für Assertionen oder Fehlermeldungen.</span><span class="sxs-lookup"><span data-stu-id="b2d9a-408">Call frames for assertions or error messages.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="b2d9a-409">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b2d9a-409">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="b2d9a-410">description</span><span class="sxs-lookup"><span data-stu-id="b2d9a-410">description</span></span> <br/> <i><span data-ttu-id="b2d9a-411">Optional</span><span class="sxs-lookup"><span data-stu-id="b2d9a-411">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="b2d9a-412">Zeichenfolgenbeschriftung dieser Stapelüberwachung.</span><span class="sxs-lookup"><span data-stu-id="b2d9a-412">String label of this stack trace.</span></span> <span data-ttu-id="b2d9a-413">Bei asynchronen Ablaufverfolgungen kann dies ein Name der Funktion sein, die den asynchronen Aufruf initiiert hat.</span><span class="sxs-lookup"><span data-stu-id="b2d9a-413">For async traces this may be a name of the function that initiated the async call.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="b2d9a-414">callFrames</span><span class="sxs-lookup"><span data-stu-id="b2d9a-414">callFrames</span></span></td>
            <td><a href="#callframe"><code class="flyout">CallFrame[]</code></a></td>
            <td><span data-ttu-id="b2d9a-415">JavaScript-Funktionsname.</span><span class="sxs-lookup"><span data-stu-id="b2d9a-415">JavaScript function name.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="b2d9a-416">Eltern</span><span class="sxs-lookup"><span data-stu-id="b2d9a-416">parent</span></span> <br/> <i><span data-ttu-id="b2d9a-417">Optional</span><span class="sxs-lookup"><span data-stu-id="b2d9a-417">optional</span></span></i></td>
            <td><a href="#stacktrace"><code class="flyout">StackTrace</code></a></td>
            <td><span data-ttu-id="b2d9a-418">Asynchrone JavaScript-Stapelüberwachung, die diesem Stapel vorausging (sofern verfügbar).</span><span class="sxs-lookup"><span data-stu-id="b2d9a-418">Asynchronous JavaScript stack trace that preceded this stack, if available.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---
