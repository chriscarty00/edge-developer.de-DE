---
description: DevTools Protocol Version 0.2 (EdgeHTML)-Referenz für die Laufzeitdomäne. Die Laufzeitdomäne macht die JavaScript-Laufzeit über Remoteauswertungs- und Spiegelobjekte verfügbar. Auswertungsergebnisse werden als Spiegelobjekt zurückgegeben, das Objekttyp, Zeichenfolgendarstellung und eindeutigen Bezeichner verfügbar macht, die für weitere Objektverweise verwendet werden können. Originalobjekte werden im Arbeitsspeicher verwaltet, es sei denn, sie werden explizit freigegeben.
title: Runtime Domain - DevTools Protocol Version 0.2 (EdgeHTML)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/03/2020
ms.topic: reference
ms.prod: microsoft-edge
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: afc79a17c5002f60806872a9add57f518ff6cb45
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398140"
---
# <a name="runtime-domain---devtools-protocol-version-02-edgehtml"></a><span data-ttu-id="4cd34-106">Runtime Domain - DevTools Protocol Version 0.2 (EdgeHTML)</span><span class="sxs-lookup"><span data-stu-id="4cd34-106">Runtime Domain - DevTools Protocol Version 0.2 (EdgeHTML)</span></span>  

<span data-ttu-id="4cd34-107">Die Laufzeitdomäne macht die JavaScript-Laufzeit über Remoteauswertungs- und Spiegelobjekte verfügbar.</span><span class="sxs-lookup"><span data-stu-id="4cd34-107">Runtime domain exposes JavaScript runtime by means of remote evaluation and mirror objects.</span></span> <span data-ttu-id="4cd34-108">Auswertungsergebnisse werden als Spiegelobjekt zurückgegeben, das Objekttyp, Zeichenfolgendarstellung und eindeutigen Bezeichner verfügbar macht, die für weitere Objektverweise verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="4cd34-108">Evaluation results are returned as mirror object that expose object type, string representation and unique identifier that can be used for further object reference.</span></span> <span data-ttu-id="4cd34-109">Originalobjekte werden im Arbeitsspeicher verwaltet, es sei denn, sie werden explizit freigegeben.</span><span class="sxs-lookup"><span data-stu-id="4cd34-109">Original objects are maintained in memory unless they are either explicitly released.</span></span>  

| <span data-ttu-id="4cd34-110">Klassifizierung</span><span class="sxs-lookup"><span data-stu-id="4cd34-110">Classification</span></span> | <span data-ttu-id="4cd34-111">Member</span><span class="sxs-lookup"><span data-stu-id="4cd34-111">Members</span></span> |  
|:--- |:--- |  
| [**<span data-ttu-id="4cd34-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="4cd34-112">Methods</span></span>**](#methods) | <span data-ttu-id="4cd34-113">[enable](#enable), [disable](#disable), [evaluate](#evaluate), [callFunctionOn](#callfunctionon), [awaitPromise](#awaitpromise), [getProperties](#getproperties), [globalLexicalScopeNames](#globallexicalscopenames), [releaseObject](#releaseobject), [releaseObjectGroup](#releaseobjectgroup), [discardConsoleEntries](#discardconsoleentries)</span><span class="sxs-lookup"><span data-stu-id="4cd34-113">[enable](#enable), [disable](#disable), [evaluate](#evaluate), [callFunctionOn](#callfunctionon), [awaitPromise](#awaitpromise), [getProperties](#getproperties), [globalLexicalScopeNames](#globallexicalscopenames), [releaseObject](#releaseobject), [releaseObjectGroup](#releaseobjectgroup), [discardConsoleEntries](#discardconsoleentries)</span></span> |  
| [**<span data-ttu-id="4cd34-114">Veranstaltungen</span><span class="sxs-lookup"><span data-stu-id="4cd34-114">Events</span></span>**](#events) | <span data-ttu-id="4cd34-115">[executionContextCreated](#executioncontextcreated), [executionContextDestroyed](#executioncontextdestroyed), [executionContextsCleared](#executioncontextscleared), [exceptionThrown](#exceptionthrown), [consoleAPICalled](#consoleapicalled)</span><span class="sxs-lookup"><span data-stu-id="4cd34-115">[executionContextCreated](#executioncontextcreated), [executionContextDestroyed](#executioncontextdestroyed), [executionContextsCleared](#executioncontextscleared), [exceptionThrown](#exceptionthrown), [consoleAPICalled](#consoleapicalled)</span></span> |  
| [**<span data-ttu-id="4cd34-116">Typen</span><span class="sxs-lookup"><span data-stu-id="4cd34-116">Types</span></span>**](#types) | <span data-ttu-id="4cd34-117">[ScriptId](#scriptid), [RemoteObjectId](#remoteobjectid), [UnserializableValue](#unserializablevalue), [RemoteObject](#remoteobject), [PropertyDescriptor](#propertydescriptor), [CallArgument](#callargument), [ExecutionContextId](#executioncontextid), [ExecutionContextDescription](#executioncontextdescription), [ExceptionDetails](#exceptiondetails), [Timestamp](#timestamp), [CallFrame](#callframe), [StackTrace](#stacktrace)</span><span class="sxs-lookup"><span data-stu-id="4cd34-117">[ScriptId](#scriptid), [RemoteObjectId](#remoteobjectid), [UnserializableValue](#unserializablevalue), [RemoteObject](#remoteobject), [PropertyDescriptor](#propertydescriptor), [CallArgument](#callargument), [ExecutionContextId](#executioncontextid), [ExecutionContextDescription](#executioncontextdescription), [ExceptionDetails](#exceptiondetails), [Timestamp](#timestamp), [CallFrame](#callframe), [StackTrace](#stacktrace)</span></span> |  

## <a name="methods"></a><span data-ttu-id="4cd34-118">Methoden</span><span class="sxs-lookup"><span data-stu-id="4cd34-118">Methods</span></span>  

### <a name="enable"></a><span data-ttu-id="4cd34-119">Aktivieren</span><span class="sxs-lookup"><span data-stu-id="4cd34-119">enable</span></span>  

<span data-ttu-id="4cd34-120">Ermöglicht die Berichterstellung für `executionContextCreated` `executionContextDestroyed` die Ereignisse , `executionContextsCleared` und.</span><span class="sxs-lookup"><span data-stu-id="4cd34-120">Enables reporting of the `executionContextCreated`, `executionContextDestroyed`, and `executionContextsCleared` events.</span></span>  <span data-ttu-id="4cd34-121">Wenn die Berichterstellung aktiviert wird, `executionContextCreated` wird das Ereignis sofort für jeden vorhandenen Ausführungskontext gesendet.</span><span class="sxs-lookup"><span data-stu-id="4cd34-121">When the reporting gets enabled the `executionContextCreated` event will be sent immediately for each existing execution context.</span></span>  

---  

### <a name="disable"></a><span data-ttu-id="4cd34-122">Deaktivieren </span><span class="sxs-lookup"><span data-stu-id="4cd34-122">disable</span></span>  

<span data-ttu-id="4cd34-123">Deaktiviert die Berichterstellung für `executionContextCreated` die `executionContextDestroyed` Ereignisse , `executionContextsCleared` und.</span><span class="sxs-lookup"><span data-stu-id="4cd34-123">Disables reporting of the `executionContextCreated`, `executionContextDestroyed`, and `executionContextsCleared` events.</span></span>  

---  

### <a name="evaluate"></a><span data-ttu-id="4cd34-124">evaluate</span><span class="sxs-lookup"><span data-stu-id="4cd34-124">evaluate</span></span>  

<span data-ttu-id="4cd34-125">Wertet Ausdruck für globales Objekt aus.</span><span class="sxs-lookup"><span data-stu-id="4cd34-125">Evaluates expression on global object.</span></span>  

| <span data-ttu-id="4cd34-126">Parameter</span><span class="sxs-lookup"><span data-stu-id="4cd34-126">Parameters</span></span> | <span data-ttu-id="4cd34-127">Typ</span><span class="sxs-lookup"><span data-stu-id="4cd34-127">Type</span></span> | <span data-ttu-id="4cd34-128">Details</span><span class="sxs-lookup"><span data-stu-id="4cd34-128">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="4cd34-129">Ausdruck</span><span class="sxs-lookup"><span data-stu-id="4cd34-129">expression</span></span> | `string` | <span data-ttu-id="4cd34-130">Ausdruck, der ausgewertet werden soll.</span><span class="sxs-lookup"><span data-stu-id="4cd34-130">Expression to evaluate.</span></span> |  
| <span data-ttu-id="4cd34-131">includeCommandLineAPI \(optional\)</span><span class="sxs-lookup"><span data-stu-id="4cd34-131">includeCommandLineAPI \(optional\)</span></span> | `boolean` | <span data-ttu-id="4cd34-132">Bestimmt, ob die Befehlszeilen-API während der Auswertung verfügbar sein soll.</span><span class="sxs-lookup"><span data-stu-id="4cd34-132">Determines whether Command Line API should be available during the evaluation.</span></span> |  
| <span data-ttu-id="4cd34-133">objectGroup \(optional\)</span><span class="sxs-lookup"><span data-stu-id="4cd34-133">objectGroup \(optional\)</span></span> | `string` | <span data-ttu-id="4cd34-134">Symbolischer Gruppenname, mit dem mehrere Objekte freigegeben werden können.</span><span class="sxs-lookup"><span data-stu-id="4cd34-134">Symbolic group name that can be used to release multiple objects.</span></span> |  
| <span data-ttu-id="4cd34-135">silent \(optional\)</span><span class="sxs-lookup"><span data-stu-id="4cd34-135">silent \(optional\)</span></span> | `boolean` | <span data-ttu-id="4cd34-136">Im automatischen Modus werden ausnahmen, die während der Auswertung ausgelöst werden, nicht gemeldet und die Ausführung nicht angehalten.</span><span class="sxs-lookup"><span data-stu-id="4cd34-136">In silent mode exceptions thrown during evaluation are not reported and do not pause execution.</span></span>  <span data-ttu-id="4cd34-137">Überschreibt `setPauseOnException` den Status.</span><span class="sxs-lookup"><span data-stu-id="4cd34-137">Overrides `setPauseOnException` state.</span></span> |  
| <span data-ttu-id="4cd34-138">contextId \(optional\)</span><span class="sxs-lookup"><span data-stu-id="4cd34-138">contextId \(optional\)</span></span> | [<span data-ttu-id="4cd34-139">ExecutionContextId</span><span class="sxs-lookup"><span data-stu-id="4cd34-139">ExecutionContextId</span></span>](#executioncontextid) | <span data-ttu-id="4cd34-140">Gibt an, in welchem Ausführungskontext eine Auswertung ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="4cd34-140">Specifies in which execution context to perform evaluation.</span></span>  <span data-ttu-id="4cd34-141">Wenn der Parameter nicht angegeben wird, wird die Auswertung im Kontext der überprüften Seite durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="4cd34-141">If the parameter is omitted the evaluation will be performed in the context of the inspected page.</span></span> |  
| <span data-ttu-id="4cd34-142">returnByValue \(optional\)</span><span class="sxs-lookup"><span data-stu-id="4cd34-142">returnByValue \(optional\)</span></span> | `boolean` | <span data-ttu-id="4cd34-143">Gibt an, ob es sich bei dem Ergebnis um ein JSON-Objekt handelt, das per Wert gesendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="4cd34-143">Whether the result is expected to be a JSON object that should be sent by value.</span></span> |  
| <span data-ttu-id="4cd34-144">awaitPromise \(optional\)</span><span class="sxs-lookup"><span data-stu-id="4cd34-144">awaitPromise \(optional\)</span></span> | `boolean` | <span data-ttu-id="4cd34-145">Ob die Ausführung für den resultierenden Wert und die Rückgabe nach der erwarteten Zusage `await` ausgeführt werden soll, wird aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="4cd34-145">Whether execution should `await` for resulting value and return once awaited promise is resolved.</span></span> |  

| <span data-ttu-id="4cd34-146">Gibt zurück</span><span class="sxs-lookup"><span data-stu-id="4cd34-146">Returns</span></span> | <span data-ttu-id="4cd34-147">Typ</span><span class="sxs-lookup"><span data-stu-id="4cd34-147">Type</span></span> | <span data-ttu-id="4cd34-148">Details</span><span class="sxs-lookup"><span data-stu-id="4cd34-148">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="4cd34-149">result</span><span class="sxs-lookup"><span data-stu-id="4cd34-149">result</span></span> | [<span data-ttu-id="4cd34-150">RemoteObject</span><span class="sxs-lookup"><span data-stu-id="4cd34-150">RemoteObject</span></span>](#remoteobject) | <span data-ttu-id="4cd34-151">Bewertungsergebnis.</span><span class="sxs-lookup"><span data-stu-id="4cd34-151">Evaluation result.</span></span> |  

---  

### <a name="callfunctionon"></a><span data-ttu-id="4cd34-152">callFunctionOn</span><span class="sxs-lookup"><span data-stu-id="4cd34-152">callFunctionOn</span></span>  

<span data-ttu-id="4cd34-153">Aufrufe funktionieren mit einer angegebenen Deklaration für das angegebene Objekt.</span><span class="sxs-lookup"><span data-stu-id="4cd34-153">Calls function with given declaration on the given object.</span></span>  <span data-ttu-id="4cd34-154">Die Objektgruppe des Ergebnisses wird vom Zielobjekt geerbt.</span><span class="sxs-lookup"><span data-stu-id="4cd34-154">Object group of the result is inherited from the target object.</span></span>  

| <span data-ttu-id="4cd34-155">Parameter</span><span class="sxs-lookup"><span data-stu-id="4cd34-155">Parameters</span></span> | <span data-ttu-id="4cd34-156">Typ</span><span class="sxs-lookup"><span data-stu-id="4cd34-156">Type</span></span> | <span data-ttu-id="4cd34-157">Details</span><span class="sxs-lookup"><span data-stu-id="4cd34-157">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="4cd34-158">functionDeclaration</span><span class="sxs-lookup"><span data-stu-id="4cd34-158">functionDeclaration</span></span> | `string` | <span data-ttu-id="4cd34-159">Deklaration der zu aufrufende Funktion.</span><span class="sxs-lookup"><span data-stu-id="4cd34-159">Declaration of the function to call.</span></span> |  
| <span data-ttu-id="4cd34-160">objectId \(optional\)</span><span class="sxs-lookup"><span data-stu-id="4cd34-160">objectId \(optional\)</span></span> | [<span data-ttu-id="4cd34-161">RemoteObjectId</span><span class="sxs-lookup"><span data-stu-id="4cd34-161">RemoteObjectId</span></span>](#remoteobjectid) | <span data-ttu-id="4cd34-162">Bezeichner des Objekts, für das die Funktion aufruft.</span><span class="sxs-lookup"><span data-stu-id="4cd34-162">Identifier of the object to call function on.</span></span>  <span data-ttu-id="4cd34-163">Entweder `objectId` oder sollte angegeben `executionContextId` werden.</span><span class="sxs-lookup"><span data-stu-id="4cd34-163">Either `objectId` or `executionContextId` should be specified.</span></span>  `objectId` <span data-ttu-id="4cd34-164">muss von der Funktion `Runtime.evaluate()` sein.</span><span class="sxs-lookup"><span data-stu-id="4cd34-164">must be from the `Runtime.evaluate()` function.</span></span> |  
| <span data-ttu-id="4cd34-165">Argumente \(optional\)</span><span class="sxs-lookup"><span data-stu-id="4cd34-165">arguments \(optional\)</span></span> | [<span data-ttu-id="4cd34-166">CallArgument[]</span><span class="sxs-lookup"><span data-stu-id="4cd34-166">CallArgument[]</span></span>](#callargument) | <span data-ttu-id="4cd34-167">Aufrufargumente.</span><span class="sxs-lookup"><span data-stu-id="4cd34-167">Call arguments.</span></span>  <span data-ttu-id="4cd34-168">Alle Aufrufargumente müssen zur gleichen JavaScript-Welt wie das Zielobjekt gehören.</span><span class="sxs-lookup"><span data-stu-id="4cd34-168">All call arguments must belong to the same JavaScript world as the target object.</span></span> |  
| <span data-ttu-id="4cd34-169">boolean \(optional\)</span><span class="sxs-lookup"><span data-stu-id="4cd34-169">boolean \(optional\)</span></span> | `boolean` | <span data-ttu-id="4cd34-170">Im automatischen Modus werden ausnahmen, die während der Auswertung ausgelöst werden, nicht gemeldet und die Ausführung nicht angehalten.</span><span class="sxs-lookup"><span data-stu-id="4cd34-170">In silent mode exceptions thrown during evaluation are not reported and do not pause execution.</span></span> <span data-ttu-id="4cd34-171">Überschreibt `setPauseOnException` den Status.</span><span class="sxs-lookup"><span data-stu-id="4cd34-171">Overrides `setPauseOnException` state.</span></span> |  
| <span data-ttu-id="4cd34-172">returnByValue \(optional\)</span><span class="sxs-lookup"><span data-stu-id="4cd34-172">returnByValue \(optional\)</span></span> | `boolean` | <span data-ttu-id="4cd34-173">Gibt an, ob es sich bei dem Ergebnis um ein JSON-Objekt handelt, das per Wert gesendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="4cd34-173">Whether the result is expected to be a JSON object which should be sent by value.</span></span> |  
| <span data-ttu-id="4cd34-174">awaitPromise \(optional\)</span><span class="sxs-lookup"><span data-stu-id="4cd34-174">awaitPromise \(optional\)</span></span> | `boolean` | <span data-ttu-id="4cd34-175">Ob die Ausführung für den resultierenden Wert und die Rückgabe nach der erwarteten Zusage `await` ausgeführt werden soll, wird aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="4cd34-175">Whether execution should `await` for resulting value and return once awaited promise is resolved.</span></span> |  
| <span data-ttu-id="4cd34-176">executionContextId \(optional\)</span><span class="sxs-lookup"><span data-stu-id="4cd34-176">executionContextId \(optional\)</span></span> | [<span data-ttu-id="4cd34-177">ExecutionContextId</span><span class="sxs-lookup"><span data-stu-id="4cd34-177">ExecutionContextId</span></span>](#executioncontextid) | <span data-ttu-id="4cd34-178">Gibt den Ausführungskontext an, für den das globale Objekt zum Aufrufen der Funktion verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="4cd34-178">Specifies execution context which global object will be used to call function on.</span></span>  <span data-ttu-id="4cd34-179">Either</span><span class="sxs-lookup"><span data-stu-id="4cd34-179">Either</span></span>
`executionContextId` <span data-ttu-id="4cd34-180">oder `objectId` muss angegeben werden</span><span class="sxs-lookup"><span data-stu-id="4cd34-180">or `objectId` should be specified</span></span> |  
| <span data-ttu-id="4cd34-181">objectGroup \(optional\)</span><span class="sxs-lookup"><span data-stu-id="4cd34-181">objectGroup \(optional\)</span></span> | `string` | <span data-ttu-id="4cd34-182">Symbolischer Gruppenname, mit dem mehrere Objekte freigegeben werden können.</span><span class="sxs-lookup"><span data-stu-id="4cd34-182">Symbolic group name that can be used to release multiple objects.</span></span>  <span data-ttu-id="4cd34-183">If `objectGroup` is not specified and `objectId` is, will be inherited from `objectGroup` object.</span><span class="sxs-lookup"><span data-stu-id="4cd34-183">If `objectGroup` is not specified and `objectId` is, `objectGroup` will be inherited from object.</span></span> |  

| <span data-ttu-id="4cd34-184">Gibt zurück</span><span class="sxs-lookup"><span data-stu-id="4cd34-184">Returns</span></span> | <span data-ttu-id="4cd34-185">Typ</span><span class="sxs-lookup"><span data-stu-id="4cd34-185">Type</span></span> | <span data-ttu-id="4cd34-186">Details</span><span class="sxs-lookup"><span data-stu-id="4cd34-186">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="4cd34-187">result</span><span class="sxs-lookup"><span data-stu-id="4cd34-187">result</span></span> | [<span data-ttu-id="4cd34-188">RemoteObject</span><span class="sxs-lookup"><span data-stu-id="4cd34-188">RemoteObject</span></span>](#remoteobject) | <span data-ttu-id="4cd34-189">Anrufergebnis.</span><span class="sxs-lookup"><span data-stu-id="4cd34-189">Call result.</span></span> |  

---  

### <a name="awaitpromise"></a><span data-ttu-id="4cd34-190">awaitPromise</span><span class="sxs-lookup"><span data-stu-id="4cd34-190">awaitPromise</span></span>  

<span data-ttu-id="4cd34-191">Fügen Sie handler to promise mit der angegebenen Promise-Objekt-ID hinzu.</span><span class="sxs-lookup"><span data-stu-id="4cd34-191">Add handler to promise with given promise object id.</span></span>  

| <span data-ttu-id="4cd34-192">Parameter</span><span class="sxs-lookup"><span data-stu-id="4cd34-192">Parameters</span></span> | <span data-ttu-id="4cd34-193">Typ</span><span class="sxs-lookup"><span data-stu-id="4cd34-193">Type</span></span> | <span data-ttu-id="4cd34-194">Details</span><span class="sxs-lookup"><span data-stu-id="4cd34-194">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="4cd34-195">promiseObjectId</span><span class="sxs-lookup"><span data-stu-id="4cd34-195">promiseObjectId</span></span> | [<span data-ttu-id="4cd34-196">RemoteObjectId</span><span class="sxs-lookup"><span data-stu-id="4cd34-196">RemoteObjectId</span></span>](#remoteobjectid) | <span data-ttu-id="4cd34-197">Bezeichner der Zusage.</span><span class="sxs-lookup"><span data-stu-id="4cd34-197">Identifier of the promise.</span></span> |  
| <span data-ttu-id="4cd34-198">returnByValue \(optional\)</span><span class="sxs-lookup"><span data-stu-id="4cd34-198">returnByValue \(optional\)</span></span> | <span data-ttu-id="4cd34-199">boolean</span><span class="sxs-lookup"><span data-stu-id="4cd34-199">boolean</span></span> | <span data-ttu-id="4cd34-200">Gibt an, ob es sich bei dem Ergebnis um ein JSON-Objekt handelt, das per Wert gesendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="4cd34-200">Whether the result is expected to be a JSON object that should be sent by value.</span></span> |  

| <span data-ttu-id="4cd34-201">Gibt zurück</span><span class="sxs-lookup"><span data-stu-id="4cd34-201">Returns</span></span> | <span data-ttu-id="4cd34-202">Typ</span><span class="sxs-lookup"><span data-stu-id="4cd34-202">Type</span></span> | <span data-ttu-id="4cd34-203">Details</span><span class="sxs-lookup"><span data-stu-id="4cd34-203">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="4cd34-204">result</span><span class="sxs-lookup"><span data-stu-id="4cd34-204">result</span></span> | [<span data-ttu-id="4cd34-205">RemoteObject</span><span class="sxs-lookup"><span data-stu-id="4cd34-205">RemoteObject</span></span>](#remoteobject) | <span data-ttu-id="4cd34-206">Zusageergebnis.</span><span class="sxs-lookup"><span data-stu-id="4cd34-206">Promise result.</span></span>  <span data-ttu-id="4cd34-207">Enthält abgelehnten Wert, wenn die Zusage abgelehnt wurde.</span><span class="sxs-lookup"><span data-stu-id="4cd34-207">Will contain rejected value if promise was rejected.</span></span> |  

---  

### <a name="getproperties"></a><span data-ttu-id="4cd34-208">getProperties</span><span class="sxs-lookup"><span data-stu-id="4cd34-208">getProperties</span></span>  

<span data-ttu-id="4cd34-209">Gibt Eigenschaften eines bestimmten Objekts zurück.</span><span class="sxs-lookup"><span data-stu-id="4cd34-209">Returns properties of a given object.</span></span> <span data-ttu-id="4cd34-210">Die Objektgruppe des Ergebnisses wird vom Zielobjekt geerbt.</span><span class="sxs-lookup"><span data-stu-id="4cd34-210">Object group of the result is inherited from the target object.</span></span>  

| <span data-ttu-id="4cd34-211">Parameter</span><span class="sxs-lookup"><span data-stu-id="4cd34-211">Parameters</span></span> | <span data-ttu-id="4cd34-212">Typ</span><span class="sxs-lookup"><span data-stu-id="4cd34-212">Type</span></span> | <span data-ttu-id="4cd34-213">Details</span><span class="sxs-lookup"><span data-stu-id="4cd34-213">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="4cd34-214">objectId</span><span class="sxs-lookup"><span data-stu-id="4cd34-214">objectId</span></span> | [<span data-ttu-id="4cd34-215">RemoteObjectId</span><span class="sxs-lookup"><span data-stu-id="4cd34-215">RemoteObjectId</span></span>](#remoteobjectid) | <span data-ttu-id="4cd34-216">Bezeichner des Objekts, für das Eigenschaften zurückgeben werden.</span><span class="sxs-lookup"><span data-stu-id="4cd34-216">Identifier of the object to return properties for.</span></span>  `objectId` <span data-ttu-id="4cd34-217">muss von der Funktion `Debugger.evaluateOnCallFrame()` sein.</span><span class="sxs-lookup"><span data-stu-id="4cd34-217">must be from the `Debugger.evaluateOnCallFrame()` function.</span></span> |  
| <span data-ttu-id="4cd34-218">ownProperties \(optional\)</span><span class="sxs-lookup"><span data-stu-id="4cd34-218">ownProperties \(optional\)</span></span> | `boolean` | <span data-ttu-id="4cd34-219">Wenn `true` , gibt Eigenschaften zurück, die nur zum Element selbst gehören, nicht zu seiner Prototypkette.</span><span class="sxs-lookup"><span data-stu-id="4cd34-219">If `true`, returns properties belonging only to the element itself, not to its prototype chain.</span></span> |  
| <span data-ttu-id="4cd34-220">accessorPropertiesOnly \(optional\)</span><span class="sxs-lookup"><span data-stu-id="4cd34-220">accessorPropertiesOnly \(optional\)</span></span> | `boolean` | <span data-ttu-id="4cd34-221">**Experimental**.</span><span class="sxs-lookup"><span data-stu-id="4cd34-221">**Experimental**.</span></span>  <span data-ttu-id="4cd34-222">Wenn `true` , gibt nur Accessoreigenschaften \(mit Getter/Setter\) zurück; interne Eigenschaften werden auch nicht zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="4cd34-222">If `true`, returns accessor properties \(with getter/setter\) only; internal properties are not returned either.</span></span> |  

| <span data-ttu-id="4cd34-223">Gibt zurück</span><span class="sxs-lookup"><span data-stu-id="4cd34-223">Returns</span></span> | <span data-ttu-id="4cd34-224">Typ</span><span class="sxs-lookup"><span data-stu-id="4cd34-224">Type</span></span> | <span data-ttu-id="4cd34-225">Details</span><span class="sxs-lookup"><span data-stu-id="4cd34-225">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="4cd34-226">result</span><span class="sxs-lookup"><span data-stu-id="4cd34-226">result</span></span> | [<span data-ttu-id="4cd34-227">PropertyDescriptor[]</span><span class="sxs-lookup"><span data-stu-id="4cd34-227">PropertyDescriptor[]</span></span>](#propertydescriptor) | <span data-ttu-id="4cd34-228">Objekteigenschaften.</span><span class="sxs-lookup"><span data-stu-id="4cd34-228">Object properties.</span></span> |  

---  

### <a name="globallexicalscopenames"></a><span data-ttu-id="4cd34-229">globalLexicalScopeNames</span><span class="sxs-lookup"><span data-stu-id="4cd34-229">globalLexicalScopeNames</span></span>  

<span data-ttu-id="4cd34-230">Gibt alle Variablen let, const und class aus dem globalen Konsolenbereich zurück.</span><span class="sxs-lookup"><span data-stu-id="4cd34-230">Returns all let, const, and class variables from the console global scope.</span></span>  

| <span data-ttu-id="4cd34-231">Gibt zurück</span><span class="sxs-lookup"><span data-stu-id="4cd34-231">Returns</span></span> | <span data-ttu-id="4cd34-232">Typ</span><span class="sxs-lookup"><span data-stu-id="4cd34-232">Type</span></span> | <span data-ttu-id="4cd34-233">Details</span><span class="sxs-lookup"><span data-stu-id="4cd34-233">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="4cd34-234">names</span><span class="sxs-lookup"><span data-stu-id="4cd34-234">names</span></span> | `string[]` | &nbsp; |  

---  

### <a name="releaseobject"></a><span data-ttu-id="4cd34-235">releaseObject</span><span class="sxs-lookup"><span data-stu-id="4cd34-235">releaseObject</span></span>  

<span data-ttu-id="4cd34-236">Gibt ein Remoteobjekt mit einer angegebenen ID frei.</span><span class="sxs-lookup"><span data-stu-id="4cd34-236">Releases remote object with given ID.</span></span>  

| <span data-ttu-id="4cd34-237">Parameter</span><span class="sxs-lookup"><span data-stu-id="4cd34-237">Parameters</span></span> | <span data-ttu-id="4cd34-238">Typ</span><span class="sxs-lookup"><span data-stu-id="4cd34-238">Type</span></span> | <span data-ttu-id="4cd34-239">Details</span><span class="sxs-lookup"><span data-stu-id="4cd34-239">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="4cd34-240">objectId</span><span class="sxs-lookup"><span data-stu-id="4cd34-240">objectId</span></span> | [<span data-ttu-id="4cd34-241">RemoteObjectId</span><span class="sxs-lookup"><span data-stu-id="4cd34-241">RemoteObjectId</span></span>](#remoteobjectid) | <span data-ttu-id="4cd34-242">Bezeichner des zu veröffentlichende Objekts.</span><span class="sxs-lookup"><span data-stu-id="4cd34-242">Identifier of the object to release.</span></span> |  

---  

### <a name="releaseobjectgroup"></a><span data-ttu-id="4cd34-243">releaseObjectGroup</span><span class="sxs-lookup"><span data-stu-id="4cd34-243">releaseObjectGroup</span></span>  

<span data-ttu-id="4cd34-244">Gibt alle Remoteobjekte frei, die zu einer bestimmten Gruppe gehören.</span><span class="sxs-lookup"><span data-stu-id="4cd34-244">Releases all remote objects that belong to a given group.</span></span>  

| <span data-ttu-id="4cd34-245">Parameter</span><span class="sxs-lookup"><span data-stu-id="4cd34-245">Parameters</span></span> | <span data-ttu-id="4cd34-246">Typ</span><span class="sxs-lookup"><span data-stu-id="4cd34-246">Type</span></span> | <span data-ttu-id="4cd34-247">Details</span><span class="sxs-lookup"><span data-stu-id="4cd34-247">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="4cd34-248">objectGroup</span><span class="sxs-lookup"><span data-stu-id="4cd34-248">objectGroup</span></span> | `string` | <span data-ttu-id="4cd34-249">Symbolischer Objektgruppenname.</span><span class="sxs-lookup"><span data-stu-id="4cd34-249">Symbolic object group name.</span></span> |  

---  

### <a name="discardconsoleentries"></a><span data-ttu-id="4cd34-250">discardConsoleEntries</span><span class="sxs-lookup"><span data-stu-id="4cd34-250">discardConsoleEntries</span></span>  

<span data-ttu-id="4cd34-251">Verwirft gesammelte Ausnahmen und Konsolen-API-Aufrufe.</span><span class="sxs-lookup"><span data-stu-id="4cd34-251">Discards collected exceptions and console API calls.</span></span>  

---  

## <a name="events"></a><span data-ttu-id="4cd34-252">Veranstaltungen</span><span class="sxs-lookup"><span data-stu-id="4cd34-252">Events</span></span>  

### <a name="executioncontextcreated"></a><span data-ttu-id="4cd34-253">executionContextCreated</span><span class="sxs-lookup"><span data-stu-id="4cd34-253">executionContextCreated</span></span>  

<span data-ttu-id="4cd34-254">Wird ausgegeben, wenn ein neuer Ausführungskontext erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="4cd34-254">Issued when new execution context is created.</span></span>  

| <span data-ttu-id="4cd34-255">Parameter</span><span class="sxs-lookup"><span data-stu-id="4cd34-255">Parameters</span></span> | <span data-ttu-id="4cd34-256">Typ</span><span class="sxs-lookup"><span data-stu-id="4cd34-256">Type</span></span> | <span data-ttu-id="4cd34-257">Details</span><span class="sxs-lookup"><span data-stu-id="4cd34-257">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="4cd34-258">context</span><span class="sxs-lookup"><span data-stu-id="4cd34-258">context</span></span> | [<span data-ttu-id="4cd34-259">ExecutionContextDescription</span><span class="sxs-lookup"><span data-stu-id="4cd34-259">ExecutionContextDescription</span></span>](#executioncontextdescription) | <span data-ttu-id="4cd34-260">Ein neu erstellter Ausführungskontext.</span><span class="sxs-lookup"><span data-stu-id="4cd34-260">A newly created execution context.</span></span> |  

---  

### <a name="executioncontextdestroyed"></a><span data-ttu-id="4cd34-261">executionContextDestroyed</span><span class="sxs-lookup"><span data-stu-id="4cd34-261">executionContextDestroyed</span></span>  

<span data-ttu-id="4cd34-262">Wird ausgegeben, wenn der Ausführungskontext zerstört wird.</span><span class="sxs-lookup"><span data-stu-id="4cd34-262">Issued when execution context is destroyed.</span></span>  

| <span data-ttu-id="4cd34-263">Parameter</span><span class="sxs-lookup"><span data-stu-id="4cd34-263">Parameters</span></span> | <span data-ttu-id="4cd34-264">Typ</span><span class="sxs-lookup"><span data-stu-id="4cd34-264">Type</span></span> | <span data-ttu-id="4cd34-265">Details</span><span class="sxs-lookup"><span data-stu-id="4cd34-265">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="4cd34-266">executionContextId</span><span class="sxs-lookup"><span data-stu-id="4cd34-266">executionContextId</span></span> | [<span data-ttu-id="4cd34-267">ExecutionContextId</span><span class="sxs-lookup"><span data-stu-id="4cd34-267">ExecutionContextId</span></span>](#executioncontextid) | <span data-ttu-id="4cd34-268">ID des zerstörten Kontexts.</span><span class="sxs-lookup"><span data-stu-id="4cd34-268">ID of the destroyed context.</span></span> |  

---  

### <a name="executioncontextscleared"></a><span data-ttu-id="4cd34-269">executionContextsCleared</span><span class="sxs-lookup"><span data-stu-id="4cd34-269">executionContextsCleared</span></span>  

<span data-ttu-id="4cd34-270">Wird ausgegeben, wenn alle executionContexts im Browser gelöscht wurden.</span><span class="sxs-lookup"><span data-stu-id="4cd34-270">Issued when all executionContexts were cleared in browser.</span></span>  

&nbsp;  

---  

### <a name="exceptionthrown"></a><span data-ttu-id="4cd34-271">exceptionThrown</span><span class="sxs-lookup"><span data-stu-id="4cd34-271">exceptionThrown</span></span>  

<span data-ttu-id="4cd34-272">Wird ausgegeben, wenn eine Ausnahme ausgelöst und nicht behandelt wurde.</span><span class="sxs-lookup"><span data-stu-id="4cd34-272">Issued when exception was thrown and unhandled.</span></span>  

| <span data-ttu-id="4cd34-273">Parameter</span><span class="sxs-lookup"><span data-stu-id="4cd34-273">Parameters</span></span> | <span data-ttu-id="4cd34-274">Typ</span><span class="sxs-lookup"><span data-stu-id="4cd34-274">Type</span></span> | <span data-ttu-id="4cd34-275">Details</span><span class="sxs-lookup"><span data-stu-id="4cd34-275">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="4cd34-276">zeitstempel</span><span class="sxs-lookup"><span data-stu-id="4cd34-276">timestamp</span></span> | [<span data-ttu-id="4cd34-277">Zeitstempel</span><span class="sxs-lookup"><span data-stu-id="4cd34-277">Timestamp</span></span>](#timestamp) | <span data-ttu-id="4cd34-278">Zeitstempel der Ausnahme.</span><span class="sxs-lookup"><span data-stu-id="4cd34-278">Timestamp of the exception.</span></span> |  
| <span data-ttu-id="4cd34-279">exceptionDetails</span><span class="sxs-lookup"><span data-stu-id="4cd34-279">exceptionDetails</span></span> | [<span data-ttu-id="4cd34-280">ExceptionDetails</span><span class="sxs-lookup"><span data-stu-id="4cd34-280">ExceptionDetails</span></span>](#exceptiondetails) | &nbsp; |  

---  

### <a name="consoleapicalled"></a><span data-ttu-id="4cd34-281">consoleAPICalled</span><span class="sxs-lookup"><span data-stu-id="4cd34-281">consoleAPICalled</span></span>  

| <span data-ttu-id="4cd34-282">Parameter</span><span class="sxs-lookup"><span data-stu-id="4cd34-282">Parameters</span></span> | <span data-ttu-id="4cd34-283">Typ</span><span class="sxs-lookup"><span data-stu-id="4cd34-283">Type</span></span> | <span data-ttu-id="4cd34-284">Details</span><span class="sxs-lookup"><span data-stu-id="4cd34-284">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="4cd34-285">Typ</span><span class="sxs-lookup"><span data-stu-id="4cd34-285">type</span></span> | `string` | <span data-ttu-id="4cd34-286">Typ des Anrufs.</span><span class="sxs-lookup"><span data-stu-id="4cd34-286">Type of the call.</span></span>  <span data-ttu-id="4cd34-287">Zulässige Werte:  `log` , , , , , , , , `info` , , `warning` , , , , `error` , `debug` , , , , `assert` , , `table` `trace` , `dir` `dirxml` `clear` `select` `count` `countReset` `timeEnd` `timeStamp` `startGroup` `startGroupCollapsed` und</span><span class="sxs-lookup"><span data-stu-id="4cd34-287">Allowed values:  `log`, `info`, `warning`, `error`, `debug`, `assert`, `table`, `trace`, `dir`, `dirxml`, `clear`, `select`, `count`, `countReset`, `timeEnd`, `timeStamp`, `startGroup`, `startGroupCollapsed`, and</span></span> `endGroup` |  
| <span data-ttu-id="4cd34-288">args</span><span class="sxs-lookup"><span data-stu-id="4cd34-288">args</span></span> | <span data-ttu-id="4cd34-289">[RemoteObject[]] (#remoteobject</span><span class="sxs-lookup"><span data-stu-id="4cd34-289">[RemoteObject[]](#remoteobject</span></span> | <span data-ttu-id="4cd34-290">Aufrufargumente.</span><span class="sxs-lookup"><span data-stu-id="4cd34-290">Call arguments.</span></span> |  
| <span data-ttu-id="4cd34-291">executionContextId</span><span class="sxs-lookup"><span data-stu-id="4cd34-291">executionContextId</span></span> | [<span data-ttu-id="4cd34-292">ExecutionContextId</span><span class="sxs-lookup"><span data-stu-id="4cd34-292">ExecutionContextId</span></span>](#executioncontextid) | <span data-ttu-id="4cd34-293">Bezeichner des Kontexts, in dem Konsolenaufrufe vorgenommen wurden.</span><span class="sxs-lookup"><span data-stu-id="4cd34-293">Identifier of the context where console call was made.</span></span> |  
| <span data-ttu-id="4cd34-294">zeitstempel \(optional\)</span><span class="sxs-lookup"><span data-stu-id="4cd34-294">timestamp \(optional\)</span></span> | [<span data-ttu-id="4cd34-295">Zeitstempel</span><span class="sxs-lookup"><span data-stu-id="4cd34-295">Timestamp</span></span>](#timestamp) | <span data-ttu-id="4cd34-296">Zeitstempel aufrufen.</span><span class="sxs-lookup"><span data-stu-id="4cd34-296">Call timestamp.</span></span> |  
| <span data-ttu-id="4cd34-297">stackTrace \(optional\)</span><span class="sxs-lookup"><span data-stu-id="4cd34-297">stackTrace \(optional\)</span></span> | [<span data-ttu-id="4cd34-298">StackTrace</span><span class="sxs-lookup"><span data-stu-id="4cd34-298">StackTrace</span></span>](#stacktrace) | <span data-ttu-id="4cd34-299">Stapelverfolgung, sofern verfügbar.</span><span class="sxs-lookup"><span data-stu-id="4cd34-299">Stack trace captured if available.</span></span> |  

---  

## <a name="types"></a><span data-ttu-id="4cd34-300">Typen</span><span class="sxs-lookup"><span data-stu-id="4cd34-300">Types</span></span>  

### <a name="scriptid-string"></a><span data-ttu-id="4cd34-301">ScriptId-Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="4cd34-301">ScriptId string</span></span>  

<a name="scriptid"></a>

<span data-ttu-id="4cd34-302">Eindeutige Skript-ID.</span><span class="sxs-lookup"><span data-stu-id="4cd34-302">Unique script identifier.</span></span>  

&nbsp;  

---  

### <a name="remoteobjectid-string"></a><span data-ttu-id="4cd34-303">RemoteObjectId-Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="4cd34-303">RemoteObjectId string</span></span>  

<a name="remoteobjectid"></a>

<span data-ttu-id="4cd34-304">Eindeutiger Objektbezeichner.</span><span class="sxs-lookup"><span data-stu-id="4cd34-304">Unique object identifier.</span></span>  

&nbsp;  

---  

### <a name="unserializablevalue-string"></a><span data-ttu-id="4cd34-305">Zeichenfolge UnserializableValue</span><span class="sxs-lookup"><span data-stu-id="4cd34-305">UnserializableValue string</span></span>  

<a name="unserializablevalue"></a>  

<span data-ttu-id="4cd34-306">Grundtypwert, der nicht JSON-stringified sein kann.</span><span class="sxs-lookup"><span data-stu-id="4cd34-306">Primitive value which cannot be JSON-stringified.</span></span>  

##### <a name="allowed-values"></a><span data-ttu-id="4cd34-307">Zulässige Werte</span><span class="sxs-lookup"><span data-stu-id="4cd34-307">Allowed Values</span></span>  

`Infinity`<span data-ttu-id="4cd34-308">, `NaN`, `-Infinity`,</span><span class="sxs-lookup"><span data-stu-id="4cd34-308">, `NaN`, `-Infinity`,</span></span> `-0`  

---  

### <a name="remoteobject-object"></a><span data-ttu-id="4cd34-309">RemoteObject-Objekt</span><span class="sxs-lookup"><span data-stu-id="4cd34-309">RemoteObject object</span></span>  

<a name="remoteobject"></a>  

<span data-ttu-id="4cd34-310">Mirror-Objekt, das auf das ursprüngliche JavaScript-Objekt referenziert.</span><span class="sxs-lookup"><span data-stu-id="4cd34-310">Mirror object referencing original JavaScript object.</span></span>  

| <span data-ttu-id="4cd34-311">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="4cd34-311">Properties</span></span> | <span data-ttu-id="4cd34-312">Typ</span><span class="sxs-lookup"><span data-stu-id="4cd34-312">Type</span></span> | <span data-ttu-id="4cd34-313">Details</span><span class="sxs-lookup"><span data-stu-id="4cd34-313">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="4cd34-314">Typ</span><span class="sxs-lookup"><span data-stu-id="4cd34-314">type</span></span> | `string` | <span data-ttu-id="4cd34-315">Objekttyp.</span><span class="sxs-lookup"><span data-stu-id="4cd34-315">Object type.</span></span>  <span data-ttu-id="4cd34-316">Zulässige Werte:  `object` , , , , , `function` `undefined` `string` `number` `boolean` und</span><span class="sxs-lookup"><span data-stu-id="4cd34-316">Allowed values:  `object`, `function`, `undefined`, `string`, `number`, `boolean`, and</span></span> `symbol` |  
| <span data-ttu-id="4cd34-317">subtype \(optional\)</span><span class="sxs-lookup"><span data-stu-id="4cd34-317">subtype \(optional\)</span></span> | `string` | <span data-ttu-id="4cd34-318">Objektuntertyphinweis.</span><span class="sxs-lookup"><span data-stu-id="4cd34-318">Object subtype hint.</span></span>  <span data-ttu-id="4cd34-319">Nur für `object` Typwerte angegeben.</span><span class="sxs-lookup"><span data-stu-id="4cd34-319">Specified for `object` type values only.</span></span>  <span data-ttu-id="4cd34-320">Zulässige Werte:  `null` `error` , , , `promise` und</span><span class="sxs-lookup"><span data-stu-id="4cd34-320">Allowed values:  `null`, `error`, `promise`, and</span></span> `node` |  
| <span data-ttu-id="4cd34-321">className \(optional\)</span><span class="sxs-lookup"><span data-stu-id="4cd34-321">className \(optional\)</span></span> | `string` | <span data-ttu-id="4cd34-322">Objektklasse \(constructor\) name.</span><span class="sxs-lookup"><span data-stu-id="4cd34-322">Object class \(constructor\) name.</span></span>  <span data-ttu-id="4cd34-323">Nur für `object` Typwerte angegeben.</span><span class="sxs-lookup"><span data-stu-id="4cd34-323">Specified for `object` type values only.</span></span> |  
| <span data-ttu-id="4cd34-324">Wert \(optional\)</span><span class="sxs-lookup"><span data-stu-id="4cd34-324">value \(optional\)</span></span> | `any` | <span data-ttu-id="4cd34-325">Remoteobjektwert bei Grundwerten oder JSON-Werten \(wenn er angefordert wurde\).</span><span class="sxs-lookup"><span data-stu-id="4cd34-325">Remote object value in case of primitive values or JSON values \(if it was requested\).</span></span> |  
| <span data-ttu-id="4cd34-326">unserializableValue \(optional\)</span><span class="sxs-lookup"><span data-stu-id="4cd34-326">unserializableValue \(optional\)</span></span> | [<span data-ttu-id="4cd34-327">UnserializableValue</span><span class="sxs-lookup"><span data-stu-id="4cd34-327">UnserializableValue</span></span>](#unserializablevalue) | <span data-ttu-id="4cd34-328">Primitiver Wert, der nicht JSON-stringified sein kann, verfügt nicht `value` über , ruft aber diese Eigenschaft ab.</span><span class="sxs-lookup"><span data-stu-id="4cd34-328">Primitive value which can not be JSON-stringified does not have `value`, but gets this property.</span></span> |  
| <span data-ttu-id="4cd34-329">beschreibung \(optional\)</span><span class="sxs-lookup"><span data-stu-id="4cd34-329">description \(optional\)</span></span> | `string` | <span data-ttu-id="4cd34-330">Zeichenfolgendarstellung des Objekts.</span><span class="sxs-lookup"><span data-stu-id="4cd34-330">String representation of the object.</span></span> |  
| <span data-ttu-id="4cd34-331">objectId \(optional\)</span><span class="sxs-lookup"><span data-stu-id="4cd34-331">objectId \(optional\)</span></span> | [<span data-ttu-id="4cd34-332">RemoteObjectId</span><span class="sxs-lookup"><span data-stu-id="4cd34-332">RemoteObjectId</span></span>](#remoteobjectid) | <span data-ttu-id="4cd34-333">Eindeutiger Objektbezeichner \(für nicht primitive Werte\).</span><span class="sxs-lookup"><span data-stu-id="4cd34-333">Unique object identifier \(for non-primitive values\).</span></span> |  
| <span data-ttu-id="4cd34-334">msDebuggerPropertyId \(optional\)</span><span class="sxs-lookup"><span data-stu-id="4cd34-334">msDebuggerPropertyId \(optional\)</span></span> | `string` | <span data-ttu-id="4cd34-335">**Experimental**.</span><span class="sxs-lookup"><span data-stu-id="4cd34-335">**Experimental**.</span></span>  <span data-ttu-id="4cd34-336">Microsoft: Die zugeordnete Debuggereigenschafts-ID für dieses Objekt.</span><span class="sxs-lookup"><span data-stu-id="4cd34-336">Microsoft:  The associated debugger property ID for this object.</span></span> |  

---  

### <a name="propertydescriptor-object"></a><span data-ttu-id="4cd34-337">PropertyDescriptor-Objekt</span><span class="sxs-lookup"><span data-stu-id="4cd34-337">PropertyDescriptor object</span></span>  

<a name="propertydescriptor"></a>  

<span data-ttu-id="4cd34-338">Objekteigenschaftsdeskriptor.</span><span class="sxs-lookup"><span data-stu-id="4cd34-338">Object property descriptor.</span></span>  

| <span data-ttu-id="4cd34-339">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="4cd34-339">Properties</span></span> | <span data-ttu-id="4cd34-340">Typ</span><span class="sxs-lookup"><span data-stu-id="4cd34-340">Type</span></span> | <span data-ttu-id="4cd34-341">Details</span><span class="sxs-lookup"><span data-stu-id="4cd34-341">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="4cd34-342">name</span><span class="sxs-lookup"><span data-stu-id="4cd34-342">name</span></span> | `string` | <span data-ttu-id="4cd34-343">Eigenschaftenname oder Symbolbeschreibung.</span><span class="sxs-lookup"><span data-stu-id="4cd34-343">Property name or symbol description.</span></span> |  
| <span data-ttu-id="4cd34-344">Wert \(optional\)</span><span class="sxs-lookup"><span data-stu-id="4cd34-344">value \(optional\)</span></span> | [<span data-ttu-id="4cd34-345">RemoteObject</span><span class="sxs-lookup"><span data-stu-id="4cd34-345">RemoteObject</span></span>](#remoteobject) | <span data-ttu-id="4cd34-346">Der Wert, der der Eigenschaft zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="4cd34-346">The value associated with the property.</span></span> |  
| <span data-ttu-id="4cd34-347">Schreibbar \(optional\)</span><span class="sxs-lookup"><span data-stu-id="4cd34-347">writable \(optional\)</span></span> | `boolean` | `True` <span data-ttu-id="4cd34-348">wenn der der Eigenschaft zugeordnete Wert geändert werden kann \(nur Datendeskriptoren\).</span><span class="sxs-lookup"><span data-stu-id="4cd34-348">if the value associated with the property may be changed \(data descriptors only\).</span></span> |  
| <span data-ttu-id="4cd34-349">get \(optional\)</span><span class="sxs-lookup"><span data-stu-id="4cd34-349">get \(optional\)</span></span> | [<span data-ttu-id="4cd34-350">RemoteObject</span><span class="sxs-lookup"><span data-stu-id="4cd34-350">RemoteObject</span></span>](#remoteobject) | <span data-ttu-id="4cd34-351">Eine Funktion, die als Getter für die Eigenschaft dient, oder wenn kein `undefined` Getter \(accessor descriptors only\) vorkommt.</span><span class="sxs-lookup"><span data-stu-id="4cd34-351">A function which serves as a getter for the property, or `undefined` if there is no getter \(accessor descriptors only\).</span></span> |  
| <span data-ttu-id="4cd34-352">set \(optional\)</span><span class="sxs-lookup"><span data-stu-id="4cd34-352">set \(optional\)</span></span> | [<span data-ttu-id="4cd34-353">RemoteObject</span><span class="sxs-lookup"><span data-stu-id="4cd34-353">RemoteObject</span></span>](#remoteobject) | <span data-ttu-id="4cd34-354">Eine Funktion, die als Setter für die Eigenschaft dient, oder wenn kein `undefined` Setter \(accessor descriptors only\) enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="4cd34-354">A function which serves as a setter for the property, or `undefined` if there is no setter \(accessor descriptors only\).</span></span> |  
| <span data-ttu-id="4cd34-355">konfigurierbar</span><span class="sxs-lookup"><span data-stu-id="4cd34-355">configurable</span></span> | `boolean` | `True` <span data-ttu-id="4cd34-356">wenn der Typ dieses Eigenschaftendeskriptors geändert werden kann und ob die Eigenschaft aus dem entsprechenden Objekt gelöscht werden kann.</span><span class="sxs-lookup"><span data-stu-id="4cd34-356">if the type of this property descriptor may be changed and if the property may be deleted from the corresponding object.</span></span> |  
| <span data-ttu-id="4cd34-357">enumerable</span><span class="sxs-lookup"><span data-stu-id="4cd34-357">enumerable</span></span> | `boolean` | `True` <span data-ttu-id="4cd34-358">wenn diese Eigenschaft während der Aufzählung der Eigenschaften des entsprechenden Objekts angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="4cd34-358">if this property shows up during enumeration of the properties on the corresponding object.</span></span> |  
| <span data-ttu-id="4cd34-359">wasThrown \(optional\)</span><span class="sxs-lookup"><span data-stu-id="4cd34-359">wasThrown \(optional\)</span></span> | `boolean` | `True` <span data-ttu-id="4cd34-360">wenn das Ergebnis während der Auswertung ausgelöst wurde.</span><span class="sxs-lookup"><span data-stu-id="4cd34-360">if the result was thrown during the evaluation.</span></span> |  
| <span data-ttu-id="4cd34-361">isOwn \(optional\)</span><span class="sxs-lookup"><span data-stu-id="4cd34-361">isOwn \(optional\)</span></span> | `boolean` | `True` <span data-ttu-id="4cd34-362">wenn sich die Eigenschaft im Besitz des Objekts befindet.</span><span class="sxs-lookup"><span data-stu-id="4cd34-362">if the property is owned for the object.</span></span> |  
| <span data-ttu-id="4cd34-363">msReturnValue \(optional\)</span><span class="sxs-lookup"><span data-stu-id="4cd34-363">msReturnValue \(optional\)</span></span> | `boolean` | <span data-ttu-id="4cd34-364">**Experimental**.</span><span class="sxs-lookup"><span data-stu-id="4cd34-364">**Experimental**.</span></span>  <span data-ttu-id="4cd34-365">Microsoft:  `True` Wenn es sich bei der Eigenschaft um einen Rückgabewert handelt.</span><span class="sxs-lookup"><span data-stu-id="4cd34-365">Microsoft:  `True` if the property is a return value.</span></span> |  
| <span data-ttu-id="4cd34-366">Symbol \(optional\)</span><span class="sxs-lookup"><span data-stu-id="4cd34-366">symbol \(optional\)</span></span> | [<span data-ttu-id="4cd34-367">RemoteObject</span><span class="sxs-lookup"><span data-stu-id="4cd34-367">RemoteObject</span></span>](#remoteobject) | <span data-ttu-id="4cd34-368">Eigenschaftssymbolobjekt, wenn die Eigenschaft vom Typ `symbol` ist.</span><span class="sxs-lookup"><span data-stu-id="4cd34-368">Property symbol object, if the property is of the `symbol` type.</span></span> |  

---  

### <a name="callargument-object"></a><span data-ttu-id="4cd34-369">CallArgument-Objekt</span><span class="sxs-lookup"><span data-stu-id="4cd34-369">CallArgument object</span></span>  

<a name="callargument"></a>  

<span data-ttu-id="4cd34-370">Represents function call argument.</span><span class="sxs-lookup"><span data-stu-id="4cd34-370">Represents function call argument.</span></span>  <span data-ttu-id="4cd34-371">Die Remoteobjekt-ID , der Grundtyp , der grundtypielle Grundwert oder kein `objectId` `value` \(für undefined\) sollte angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="4cd34-371">Either remote object ID `objectId`, primitive `value`, unserializable primitive value, or neither of \(for undefined\) them should be specified.</span></span>  

| <span data-ttu-id="4cd34-372">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="4cd34-372">Properties</span></span> | <span data-ttu-id="4cd34-373">Typ</span><span class="sxs-lookup"><span data-stu-id="4cd34-373">Type</span></span> | <span data-ttu-id="4cd34-374">Details</span><span class="sxs-lookup"><span data-stu-id="4cd34-374">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="4cd34-375">Wert \(optional\)</span><span class="sxs-lookup"><span data-stu-id="4cd34-375">value \(optional\)</span></span> | `any` | <span data-ttu-id="4cd34-376">Grundtypwert oder serialisierbares javascript-Objekt.</span><span class="sxs-lookup"><span data-stu-id="4cd34-376">Primitive value or serializable javascript object.</span></span> |  
| <span data-ttu-id="4cd34-377">unserializableValue \(optional\)</span><span class="sxs-lookup"><span data-stu-id="4cd34-377">unserializableValue \(optional\)</span></span> | [<span data-ttu-id="4cd34-378">UnserializableValue</span><span class="sxs-lookup"><span data-stu-id="4cd34-378">UnserializableValue</span></span>](#unserializablevalue) | <span data-ttu-id="4cd34-379">Grundtypwert, der nicht JSON-stringified sein kann.</span><span class="sxs-lookup"><span data-stu-id="4cd34-379">Primitive value which can not be JSON-stringified.</span></span> |  
| <span data-ttu-id="4cd34-380">objectId \(optional\)</span><span class="sxs-lookup"><span data-stu-id="4cd34-380">objectId \(optional\)</span></span> | <span data-ttu-id="4cd34-381">[RemoteObjectId](#remoteobjectid)]</span><span class="sxs-lookup"><span data-stu-id="4cd34-381">[RemoteObjectId](#remoteobjectid)]</span></span> | <span data-ttu-id="4cd34-382">Remoteobjekthandle.</span><span class="sxs-lookup"><span data-stu-id="4cd34-382">Remote object handle.</span></span> |  

---  

### <a name="executioncontextid-integer"></a><span data-ttu-id="4cd34-383">ExecutionContextId ganzzahlig</span><span class="sxs-lookup"><span data-stu-id="4cd34-383">ExecutionContextId integer</span></span>  

<a name="executioncontextid"></a>  

<span data-ttu-id="4cd34-384">ID eines Ausführungskontexts.</span><span class="sxs-lookup"><span data-stu-id="4cd34-384">ID of an execution context.</span></span>  

&nbsp;  

---  

### <a name="executioncontextdescription-object"></a><span data-ttu-id="4cd34-385">ExecutionContextDescription-Objekt</span><span class="sxs-lookup"><span data-stu-id="4cd34-385">ExecutionContextDescription object</span></span>  

<a name="executioncontextdescription"></a>  

<span data-ttu-id="4cd34-386">Beschreibung einer isolierten Welt.</span><span class="sxs-lookup"><span data-stu-id="4cd34-386">Description of an isolated world.</span></span>  

| <span data-ttu-id="4cd34-387">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="4cd34-387">Properties</span></span> | <span data-ttu-id="4cd34-388">Typ</span><span class="sxs-lookup"><span data-stu-id="4cd34-388">Type</span></span> | <span data-ttu-id="4cd34-389">Details</span><span class="sxs-lookup"><span data-stu-id="4cd34-389">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="4cd34-390">id</span><span class="sxs-lookup"><span data-stu-id="4cd34-390">id</span></span> | [<span data-ttu-id="4cd34-391">ExecutionContextId</span><span class="sxs-lookup"><span data-stu-id="4cd34-391">ExecutionContextId</span></span>](#executioncontextid) | <span data-ttu-id="4cd34-392">Eindeutige ID des Ausführungskontexts.</span><span class="sxs-lookup"><span data-stu-id="4cd34-392">Unique ID of the execution context.</span></span>  <span data-ttu-id="4cd34-393">Sie kann verwendet werden, um anzugeben, in welchem Ausführungskontext</span><span class="sxs-lookup"><span data-stu-id="4cd34-393">It can be used to specify in which execution context</span></span>
<span data-ttu-id="4cd34-394">Die Skriptauswertung sollte durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="4cd34-394">script evaluation should be performed.</span></span> |  
| <span data-ttu-id="4cd34-395">Ursprung</span><span class="sxs-lookup"><span data-stu-id="4cd34-395">origin</span></span> | `string` | <span data-ttu-id="4cd34-396">Ausführungskontextherkunft.</span><span class="sxs-lookup"><span data-stu-id="4cd34-396">Execution context origin.</span></span> |  
| <span data-ttu-id="4cd34-397">name</span><span class="sxs-lookup"><span data-stu-id="4cd34-397">name</span></span> | `string` | <span data-ttu-id="4cd34-398">Vom Menschen lesbarer Name, der den angegebenen Kontext beschreibt.</span><span class="sxs-lookup"><span data-stu-id="4cd34-398">Human readable name describing given context.</span></span> |  

---  

### <a name="exceptiondetails-object"></a><span data-ttu-id="4cd34-399">ExceptionDetails-Objekt</span><span class="sxs-lookup"><span data-stu-id="4cd34-399">ExceptionDetails object</span></span>  

<a name="exceptiondetails"></a>  

<span data-ttu-id="4cd34-400">Ausführliche Informationen zu Ausnahme (oder Fehler), die während der Skriptkompilierung oder -ausführung ausgelöst wurde.</span><span class="sxs-lookup"><span data-stu-id="4cd34-400">Detailed information about exception (or error) that was thrown during script compilation or execution.</span></span>  

| <span data-ttu-id="4cd34-401">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="4cd34-401">Properties</span></span> | <span data-ttu-id="4cd34-402">Typ</span><span class="sxs-lookup"><span data-stu-id="4cd34-402">Type</span></span> | <span data-ttu-id="4cd34-403">Details</span><span class="sxs-lookup"><span data-stu-id="4cd34-403">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="4cd34-404">exceptionId</span><span class="sxs-lookup"><span data-stu-id="4cd34-404">exceptionId</span></span> | `integer` | <span data-ttu-id="4cd34-405">Ausnahme-ID.</span><span class="sxs-lookup"><span data-stu-id="4cd34-405">Exception ID.</span></span> |  
| <span data-ttu-id="4cd34-406">Text</span><span class="sxs-lookup"><span data-stu-id="4cd34-406">text</span></span> | `string` | <span data-ttu-id="4cd34-407">Ausnahmetext, der zusammen mit dem Ausnahmeobjekt verwendet werden sollte, wenn verfügbar.</span><span class="sxs-lookup"><span data-stu-id="4cd34-407">Exception text, which should be used together with exception object when available.</span></span> |  
| <span data-ttu-id="4cd34-408">lineNumber</span><span class="sxs-lookup"><span data-stu-id="4cd34-408">lineNumber</span></span> | `integer` | <span data-ttu-id="4cd34-409">Zeilennummer des Ausnahmespeicherorts \(0-basiert\).</span><span class="sxs-lookup"><span data-stu-id="4cd34-409">Line number of the exception location \(0-based\).</span></span> |  
| <span data-ttu-id="4cd34-410">columnNumber</span><span class="sxs-lookup"><span data-stu-id="4cd34-410">columnNumber</span></span> | `integer` | <span data-ttu-id="4cd34-411">Spaltennummer des Ausnahmespeicherorts \(0-basiert\).</span><span class="sxs-lookup"><span data-stu-id="4cd34-411">Column number of the exception location \(0-based\).</span></span> |  
| <span data-ttu-id="4cd34-412">scriptId \(optional\)</span><span class="sxs-lookup"><span data-stu-id="4cd34-412">scriptId \(optional\)</span></span> | [<span data-ttu-id="4cd34-413">ScriptId</span><span class="sxs-lookup"><span data-stu-id="4cd34-413">ScriptId</span></span>](#scriptid) | <span data-ttu-id="4cd34-414">Skript-ID des Ausnahmespeicherorts.</span><span class="sxs-lookup"><span data-stu-id="4cd34-414">Script ID of the exception location.</span></span> |  
| <span data-ttu-id="4cd34-415">url \(optional\)</span><span class="sxs-lookup"><span data-stu-id="4cd34-415">url \(optional\)</span></span> | `string` | <span data-ttu-id="4cd34-416">URL des Ausnahmespeicherorts, der verwendet werden soll, wenn das Skript nicht gemeldet wurde.</span><span class="sxs-lookup"><span data-stu-id="4cd34-416">URL of the exception location, to be used when the script was not reported.</span></span> |  
| <span data-ttu-id="4cd34-417">stackTrace \(optional\)</span><span class="sxs-lookup"><span data-stu-id="4cd34-417">stackTrace \(optional\)</span></span> | [<span data-ttu-id="4cd34-418">StackTrace</span><span class="sxs-lookup"><span data-stu-id="4cd34-418">StackTrace</span></span>](#stacktrace) | <span data-ttu-id="4cd34-419">JavaScript-Stapelverfolgung, sofern verfügbar.</span><span class="sxs-lookup"><span data-stu-id="4cd34-419">JavaScript stack trace if available.</span></span> |  
| <span data-ttu-id="4cd34-420">Ausnahme \(optional\)</span><span class="sxs-lookup"><span data-stu-id="4cd34-420">exception \(optional\)</span></span> | [<span data-ttu-id="4cd34-421">RemoteObject</span><span class="sxs-lookup"><span data-stu-id="4cd34-421">RemoteObject</span></span>](#remoteobject) | <span data-ttu-id="4cd34-422">Exception-Objekt, sofern verfügbar.</span><span class="sxs-lookup"><span data-stu-id="4cd34-422">Exception object if available.</span></span> |  
| <span data-ttu-id="4cd34-423">executionContextId \(optional\)</span><span class="sxs-lookup"><span data-stu-id="4cd34-423">executionContextId \(optional\)</span></span> | [<span data-ttu-id="4cd34-424">ExecutionContextId</span><span class="sxs-lookup"><span data-stu-id="4cd34-424">ExecutionContextId</span></span>](#executioncontextid) | <span data-ttu-id="4cd34-425">Bezeichner des Kontexts, in dem eine Ausnahme eingetreten ist.</span><span class="sxs-lookup"><span data-stu-id="4cd34-425">Identifier of the context where exception happened.</span></span> |  

---  

### <a name="timestamp-integer"></a><span data-ttu-id="4cd34-426">Ganze Zeitstempel</span><span class="sxs-lookup"><span data-stu-id="4cd34-426">Timestamp integer</span></span>  

<a name="timestamp"></a>  

<span data-ttu-id="4cd34-427">Anzahl der Millisekunden seit der Epoche.</span><span class="sxs-lookup"><span data-stu-id="4cd34-427">Number of milliseconds since epoch.</span></span>  

&nbsp;  

---  

### <a name="callframe-object"></a><span data-ttu-id="4cd34-428">CallFrame-Objekt</span><span class="sxs-lookup"><span data-stu-id="4cd34-428">CallFrame object</span></span>  

<a name="callframe"></a>  

<span data-ttu-id="4cd34-429">Stapeleintrag für Laufzeitfehler und -assertionen.</span><span class="sxs-lookup"><span data-stu-id="4cd34-429">Stack entry for runtime errors and assertions.</span></span>  

| <span data-ttu-id="4cd34-430">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="4cd34-430">Properties</span></span> | <span data-ttu-id="4cd34-431">Typ</span><span class="sxs-lookup"><span data-stu-id="4cd34-431">Type</span></span> | <span data-ttu-id="4cd34-432">Details</span><span class="sxs-lookup"><span data-stu-id="4cd34-432">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="4cd34-433">functionName</span><span class="sxs-lookup"><span data-stu-id="4cd34-433">functionName</span></span> | `string` | <span data-ttu-id="4cd34-434">JavaScript-Funktionsname.</span><span class="sxs-lookup"><span data-stu-id="4cd34-434">JavaScript function name.</span></span> |  
| <span data-ttu-id="4cd34-435">scriptId</span><span class="sxs-lookup"><span data-stu-id="4cd34-435">scriptId</span></span> | [<span data-ttu-id="4cd34-436">ScriptId</span><span class="sxs-lookup"><span data-stu-id="4cd34-436">ScriptId</span></span>](#scriptid) | <span data-ttu-id="4cd34-437">JavaScript-Skript-ID. ScriptId ist leer, wenn der Debugger nicht aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="4cd34-437">JavaScript script id. ScriptId will be empty if debugger is not enabled.</span></span> |  
| <span data-ttu-id="4cd34-438">URL</span><span class="sxs-lookup"><span data-stu-id="4cd34-438">url</span></span> | `string` | <span data-ttu-id="4cd34-439">Name oder URL des JavaScript-Skripts.</span><span class="sxs-lookup"><span data-stu-id="4cd34-439">JavaScript script name or url.</span></span> |  
| <span data-ttu-id="4cd34-440">lineNumber</span><span class="sxs-lookup"><span data-stu-id="4cd34-440">lineNumber</span></span> | `integer` | <span data-ttu-id="4cd34-441">JavaScript-Skript-Zeilennummer \(0-basiert\).</span><span class="sxs-lookup"><span data-stu-id="4cd34-441">JavaScript script line number \(0-based\).</span></span> |  
| <span data-ttu-id="4cd34-442">columnNumber</span><span class="sxs-lookup"><span data-stu-id="4cd34-442">columnNumber</span></span> | <span data-ttu-id="4cd34-443">Ganzzahl</span><span class="sxs-lookup"><span data-stu-id="4cd34-443">integer</span></span> | <span data-ttu-id="4cd34-444">JavaScript-Skriptspaltennummer \(0-basiert\).</span><span class="sxs-lookup"><span data-stu-id="4cd34-444">JavaScript script column number \(0-based\).</span></span> |  

---  

### <a name="stacktrace-object"></a><span data-ttu-id="4cd34-445">StackTrace-Objekt</span><span class="sxs-lookup"><span data-stu-id="4cd34-445">StackTrace object</span></span>  

<a name="stacktrace"></a>  

<span data-ttu-id="4cd34-446">Aufrufframes für Assertionen oder Fehlermeldungen.</span><span class="sxs-lookup"><span data-stu-id="4cd34-446">Call frames for assertions or error messages.</span></span>  

| <span data-ttu-id="4cd34-447">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="4cd34-447">Properties</span></span> | <span data-ttu-id="4cd34-448">Typ</span><span class="sxs-lookup"><span data-stu-id="4cd34-448">Type</span></span> | <span data-ttu-id="4cd34-449">Details</span><span class="sxs-lookup"><span data-stu-id="4cd34-449">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="4cd34-450">beschreibung \(optional\)</span><span class="sxs-lookup"><span data-stu-id="4cd34-450">description \(optional\)</span></span> | `string` | <span data-ttu-id="4cd34-451">Zeichenfolgenbeschriftung dieser Stapelverfolgung.</span><span class="sxs-lookup"><span data-stu-id="4cd34-451">String label of this stack trace.</span></span>  <span data-ttu-id="4cd34-452">Bei asynchronen Ablaufverfolgungen kann dies ein Name der Funktion sein, die den asynchronen Aufruf initiiert hat.</span><span class="sxs-lookup"><span data-stu-id="4cd34-452">For async traces this may be a name of the function that initiated the async call.</span></span> |  
| <span data-ttu-id="4cd34-453">callFrames</span><span class="sxs-lookup"><span data-stu-id="4cd34-453">callFrames</span></span> | [<span data-ttu-id="4cd34-454">CallFrame[]</span><span class="sxs-lookup"><span data-stu-id="4cd34-454">CallFrame[]</span></span>](#callframe) | <span data-ttu-id="4cd34-455">JavaScript-Funktionsname.</span><span class="sxs-lookup"><span data-stu-id="4cd34-455">JavaScript function name.</span></span> |  
| <span data-ttu-id="4cd34-456">übergeordnetes Element \(optional\)</span><span class="sxs-lookup"><span data-stu-id="4cd34-456">parent \(optional\)</span></span> | [<span data-ttu-id="4cd34-457">StackTrace</span><span class="sxs-lookup"><span data-stu-id="4cd34-457">StackTrace</span></span>](#stacktrace) | <span data-ttu-id="4cd34-458">Asynchrone JavaScript-Stapelverfolgung, die diesem Stapel vorausgegangen ist, sofern verfügbar.</span><span class="sxs-lookup"><span data-stu-id="4cd34-458">Asynchronous JavaScript stack trace that preceded this stack, if available.</span></span> |  

---  
