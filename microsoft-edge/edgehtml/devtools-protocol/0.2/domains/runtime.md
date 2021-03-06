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
# <a name="runtime-domain---devtools-protocol-version-02-edgehtml"></a>Runtime Domain - DevTools Protocol Version 0.2 (EdgeHTML)  

Die Laufzeitdomäne macht die JavaScript-Laufzeit über Remoteauswertungs- und Spiegelobjekte verfügbar. Auswertungsergebnisse werden als Spiegelobjekt zurückgegeben, das Objekttyp, Zeichenfolgendarstellung und eindeutigen Bezeichner verfügbar macht, die für weitere Objektverweise verwendet werden können. Originalobjekte werden im Arbeitsspeicher verwaltet, es sei denn, sie werden explizit freigegeben.  

| Klassifizierung | Member |  
|:--- |:--- |  
| [**Methoden**](#methods) | [enable](#enable), [disable](#disable), [evaluate](#evaluate), [callFunctionOn](#callfunctionon), [awaitPromise](#awaitpromise), [getProperties](#getproperties), [globalLexicalScopeNames](#globallexicalscopenames), [releaseObject](#releaseobject), [releaseObjectGroup](#releaseobjectgroup), [discardConsoleEntries](#discardconsoleentries) |  
| [**Veranstaltungen**](#events) | [executionContextCreated](#executioncontextcreated), [executionContextDestroyed](#executioncontextdestroyed), [executionContextsCleared](#executioncontextscleared), [exceptionThrown](#exceptionthrown), [consoleAPICalled](#consoleapicalled) |  
| [**Typen**](#types) | [ScriptId](#scriptid), [RemoteObjectId](#remoteobjectid), [UnserializableValue](#unserializablevalue), [RemoteObject](#remoteobject), [PropertyDescriptor](#propertydescriptor), [CallArgument](#callargument), [ExecutionContextId](#executioncontextid), [ExecutionContextDescription](#executioncontextdescription), [ExceptionDetails](#exceptiondetails), [Timestamp](#timestamp), [CallFrame](#callframe), [StackTrace](#stacktrace) |  

## <a name="methods"></a>Methoden  

### <a name="enable"></a>Aktivieren  

Ermöglicht die Berichterstellung für `executionContextCreated` `executionContextDestroyed` die Ereignisse , `executionContextsCleared` und.  Wenn die Berichterstellung aktiviert wird, `executionContextCreated` wird das Ereignis sofort für jeden vorhandenen Ausführungskontext gesendet.  

---  

### <a name="disable"></a>Deaktivieren   

Deaktiviert die Berichterstellung für `executionContextCreated` die `executionContextDestroyed` Ereignisse , `executionContextsCleared` und.  

---  

### <a name="evaluate"></a>evaluate  

Wertet Ausdruck für globales Objekt aus.  

| Parameter | Typ | Details |  
|:--- |:--- |:--- |  
| Ausdruck | `string` | Ausdruck, der ausgewertet werden soll. |  
| includeCommandLineAPI \(optional\) | `boolean` | Bestimmt, ob die Befehlszeilen-API während der Auswertung verfügbar sein soll. |  
| objectGroup \(optional\) | `string` | Symbolischer Gruppenname, mit dem mehrere Objekte freigegeben werden können. |  
| silent \(optional\) | `boolean` | Im automatischen Modus werden ausnahmen, die während der Auswertung ausgelöst werden, nicht gemeldet und die Ausführung nicht angehalten.  Überschreibt `setPauseOnException` den Status. |  
| contextId \(optional\) | [ExecutionContextId](#executioncontextid) | Gibt an, in welchem Ausführungskontext eine Auswertung ausgeführt werden soll.  Wenn der Parameter nicht angegeben wird, wird die Auswertung im Kontext der überprüften Seite durchgeführt. |  
| returnByValue \(optional\) | `boolean` | Gibt an, ob es sich bei dem Ergebnis um ein JSON-Objekt handelt, das per Wert gesendet werden soll. |  
| awaitPromise \(optional\) | `boolean` | Ob die Ausführung für den resultierenden Wert und die Rückgabe nach der erwarteten Zusage `await` ausgeführt werden soll, wird aufgelöst. |  

| Gibt zurück | Typ | Details |  
|:--- |:--- |:--- |  
| result | [RemoteObject](#remoteobject) | Bewertungsergebnis. |  

---  

### <a name="callfunctionon"></a>callFunctionOn  

Aufrufe funktionieren mit einer angegebenen Deklaration für das angegebene Objekt.  Die Objektgruppe des Ergebnisses wird vom Zielobjekt geerbt.  

| Parameter | Typ | Details |  
|:--- |:--- |:--- |  
| functionDeclaration | `string` | Deklaration der zu aufrufende Funktion. |  
| objectId \(optional\) | [RemoteObjectId](#remoteobjectid) | Bezeichner des Objekts, für das die Funktion aufruft.  Entweder `objectId` oder sollte angegeben `executionContextId` werden.  `objectId` muss von der Funktion `Runtime.evaluate()` sein. |  
| Argumente \(optional\) | [CallArgument[]](#callargument) | Aufrufargumente.  Alle Aufrufargumente müssen zur gleichen JavaScript-Welt wie das Zielobjekt gehören. |  
| boolean \(optional\) | `boolean` | Im automatischen Modus werden ausnahmen, die während der Auswertung ausgelöst werden, nicht gemeldet und die Ausführung nicht angehalten. Überschreibt `setPauseOnException` den Status. |  
| returnByValue \(optional\) | `boolean` | Gibt an, ob es sich bei dem Ergebnis um ein JSON-Objekt handelt, das per Wert gesendet werden soll. |  
| awaitPromise \(optional\) | `boolean` | Ob die Ausführung für den resultierenden Wert und die Rückgabe nach der erwarteten Zusage `await` ausgeführt werden soll, wird aufgelöst. |  
| executionContextId \(optional\) | [ExecutionContextId](#executioncontextid) | Gibt den Ausführungskontext an, für den das globale Objekt zum Aufrufen der Funktion verwendet wird.  Either
`executionContextId` oder `objectId` muss angegeben werden |  
| objectGroup \(optional\) | `string` | Symbolischer Gruppenname, mit dem mehrere Objekte freigegeben werden können.  If `objectGroup` is not specified and `objectId` is, will be inherited from `objectGroup` object. |  

| Gibt zurück | Typ | Details |  
|:--- |:--- |:--- |  
| result | [RemoteObject](#remoteobject) | Anrufergebnis. |  

---  

### <a name="awaitpromise"></a>awaitPromise  

Fügen Sie handler to promise mit der angegebenen Promise-Objekt-ID hinzu.  

| Parameter | Typ | Details |  
|:--- |:--- |:--- |  
| promiseObjectId | [RemoteObjectId](#remoteobjectid) | Bezeichner der Zusage. |  
| returnByValue \(optional\) | boolean | Gibt an, ob es sich bei dem Ergebnis um ein JSON-Objekt handelt, das per Wert gesendet werden soll. |  

| Gibt zurück | Typ | Details |  
|:--- |:--- |:--- |  
| result | [RemoteObject](#remoteobject) | Zusageergebnis.  Enthält abgelehnten Wert, wenn die Zusage abgelehnt wurde. |  

---  

### <a name="getproperties"></a>getProperties  

Gibt Eigenschaften eines bestimmten Objekts zurück. Die Objektgruppe des Ergebnisses wird vom Zielobjekt geerbt.  

| Parameter | Typ | Details |  
|:--- |:--- |:--- |  
| objectId | [RemoteObjectId](#remoteobjectid) | Bezeichner des Objekts, für das Eigenschaften zurückgeben werden.  `objectId` muss von der Funktion `Debugger.evaluateOnCallFrame()` sein. |  
| ownProperties \(optional\) | `boolean` | Wenn `true` , gibt Eigenschaften zurück, die nur zum Element selbst gehören, nicht zu seiner Prototypkette. |  
| accessorPropertiesOnly \(optional\) | `boolean` | **Experimental**.  Wenn `true` , gibt nur Accessoreigenschaften \(mit Getter/Setter\) zurück; interne Eigenschaften werden auch nicht zurückgegeben. |  

| Gibt zurück | Typ | Details |  
|:--- |:--- |:--- |  
| result | [PropertyDescriptor[]](#propertydescriptor) | Objekteigenschaften. |  

---  

### <a name="globallexicalscopenames"></a>globalLexicalScopeNames  

Gibt alle Variablen let, const und class aus dem globalen Konsolenbereich zurück.  

| Gibt zurück | Typ | Details |  
|:--- |:--- |:--- |  
| names | `string[]` | &nbsp; |  

---  

### <a name="releaseobject"></a>releaseObject  

Gibt ein Remoteobjekt mit einer angegebenen ID frei.  

| Parameter | Typ | Details |  
|:--- |:--- |:--- |  
| objectId | [RemoteObjectId](#remoteobjectid) | Bezeichner des zu veröffentlichende Objekts. |  

---  

### <a name="releaseobjectgroup"></a>releaseObjectGroup  

Gibt alle Remoteobjekte frei, die zu einer bestimmten Gruppe gehören.  

| Parameter | Typ | Details |  
|:--- |:--- |:--- |  
| objectGroup | `string` | Symbolischer Objektgruppenname. |  

---  

### <a name="discardconsoleentries"></a>discardConsoleEntries  

Verwirft gesammelte Ausnahmen und Konsolen-API-Aufrufe.  

---  

## <a name="events"></a>Veranstaltungen  

### <a name="executioncontextcreated"></a>executionContextCreated  

Wird ausgegeben, wenn ein neuer Ausführungskontext erstellt wird.  

| Parameter | Typ | Details |  
|:--- |:--- |:--- |  
| context | [ExecutionContextDescription](#executioncontextdescription) | Ein neu erstellter Ausführungskontext. |  

---  

### <a name="executioncontextdestroyed"></a>executionContextDestroyed  

Wird ausgegeben, wenn der Ausführungskontext zerstört wird.  

| Parameter | Typ | Details |  
|:--- |:--- |:--- |  
| executionContextId | [ExecutionContextId](#executioncontextid) | ID des zerstörten Kontexts. |  

---  

### <a name="executioncontextscleared"></a>executionContextsCleared  

Wird ausgegeben, wenn alle executionContexts im Browser gelöscht wurden.  

&nbsp;  

---  

### <a name="exceptionthrown"></a>exceptionThrown  

Wird ausgegeben, wenn eine Ausnahme ausgelöst und nicht behandelt wurde.  

| Parameter | Typ | Details |  
|:--- |:--- |:--- |  
| zeitstempel | [Zeitstempel](#timestamp) | Zeitstempel der Ausnahme. |  
| exceptionDetails | [ExceptionDetails](#exceptiondetails) | &nbsp; |  

---  

### <a name="consoleapicalled"></a>consoleAPICalled  

| Parameter | Typ | Details |  
|:--- |:--- |:--- |  
| Typ | `string` | Typ des Anrufs.  Zulässige Werte:  `log` , , , , , , , , `info` , , `warning` , , , , `error` , `debug` , , , , `assert` , , `table` `trace` , `dir` `dirxml` `clear` `select` `count` `countReset` `timeEnd` `timeStamp` `startGroup` `startGroupCollapsed` und `endGroup` |  
| args | [RemoteObject[]] (#remoteobject | Aufrufargumente. |  
| executionContextId | [ExecutionContextId](#executioncontextid) | Bezeichner des Kontexts, in dem Konsolenaufrufe vorgenommen wurden. |  
| zeitstempel \(optional\) | [Zeitstempel](#timestamp) | Zeitstempel aufrufen. |  
| stackTrace \(optional\) | [StackTrace](#stacktrace) | Stapelverfolgung, sofern verfügbar. |  

---  

## <a name="types"></a>Typen  

### <a name="scriptid-string"></a>ScriptId-Zeichenfolge  

<a name="scriptid"></a>

Eindeutige Skript-ID.  

&nbsp;  

---  

### <a name="remoteobjectid-string"></a>RemoteObjectId-Zeichenfolge  

<a name="remoteobjectid"></a>

Eindeutiger Objektbezeichner.  

&nbsp;  

---  

### <a name="unserializablevalue-string"></a>Zeichenfolge UnserializableValue  

<a name="unserializablevalue"></a>  

Grundtypwert, der nicht JSON-stringified sein kann.  

##### <a name="allowed-values"></a>Zulässige Werte  

`Infinity`, `NaN`, `-Infinity`, `-0`  

---  

### <a name="remoteobject-object"></a>RemoteObject-Objekt  

<a name="remoteobject"></a>  

Mirror-Objekt, das auf das ursprüngliche JavaScript-Objekt referenziert.  

| Eigenschaften | Typ | Details |  
|:--- |:--- |:--- |  
| Typ | `string` | Objekttyp.  Zulässige Werte:  `object` , , , , , `function` `undefined` `string` `number` `boolean` und `symbol` |  
| subtype \(optional\) | `string` | Objektuntertyphinweis.  Nur für `object` Typwerte angegeben.  Zulässige Werte:  `null` `error` , , , `promise` und `node` |  
| className \(optional\) | `string` | Objektklasse \(constructor\) name.  Nur für `object` Typwerte angegeben. |  
| Wert \(optional\) | `any` | Remoteobjektwert bei Grundwerten oder JSON-Werten \(wenn er angefordert wurde\). |  
| unserializableValue \(optional\) | [UnserializableValue](#unserializablevalue) | Primitiver Wert, der nicht JSON-stringified sein kann, verfügt nicht `value` über , ruft aber diese Eigenschaft ab. |  
| beschreibung \(optional\) | `string` | Zeichenfolgendarstellung des Objekts. |  
| objectId \(optional\) | [RemoteObjectId](#remoteobjectid) | Eindeutiger Objektbezeichner \(für nicht primitive Werte\). |  
| msDebuggerPropertyId \(optional\) | `string` | **Experimental**.  Microsoft: Die zugeordnete Debuggereigenschafts-ID für dieses Objekt. |  

---  

### <a name="propertydescriptor-object"></a>PropertyDescriptor-Objekt  

<a name="propertydescriptor"></a>  

Objekteigenschaftsdeskriptor.  

| Eigenschaften | Typ | Details |  
|:--- |:--- |:--- |  
| name | `string` | Eigenschaftenname oder Symbolbeschreibung. |  
| Wert \(optional\) | [RemoteObject](#remoteobject) | Der Wert, der der Eigenschaft zugeordnet ist. |  
| Schreibbar \(optional\) | `boolean` | `True` wenn der der Eigenschaft zugeordnete Wert geändert werden kann \(nur Datendeskriptoren\). |  
| get \(optional\) | [RemoteObject](#remoteobject) | Eine Funktion, die als Getter für die Eigenschaft dient, oder wenn kein `undefined` Getter \(accessor descriptors only\) vorkommt. |  
| set \(optional\) | [RemoteObject](#remoteobject) | Eine Funktion, die als Setter für die Eigenschaft dient, oder wenn kein `undefined` Setter \(accessor descriptors only\) enthalten ist. |  
| konfigurierbar | `boolean` | `True` wenn der Typ dieses Eigenschaftendeskriptors geändert werden kann und ob die Eigenschaft aus dem entsprechenden Objekt gelöscht werden kann. |  
| enumerable | `boolean` | `True` wenn diese Eigenschaft während der Aufzählung der Eigenschaften des entsprechenden Objekts angezeigt wird. |  
| wasThrown \(optional\) | `boolean` | `True` wenn das Ergebnis während der Auswertung ausgelöst wurde. |  
| isOwn \(optional\) | `boolean` | `True` wenn sich die Eigenschaft im Besitz des Objekts befindet. |  
| msReturnValue \(optional\) | `boolean` | **Experimental**.  Microsoft:  `True` Wenn es sich bei der Eigenschaft um einen Rückgabewert handelt. |  
| Symbol \(optional\) | [RemoteObject](#remoteobject) | Eigenschaftssymbolobjekt, wenn die Eigenschaft vom Typ `symbol` ist. |  

---  

### <a name="callargument-object"></a>CallArgument-Objekt  

<a name="callargument"></a>  

Represents function call argument.  Die Remoteobjekt-ID , der Grundtyp , der grundtypielle Grundwert oder kein `objectId` `value` \(für undefined\) sollte angegeben werden.  

| Eigenschaften | Typ | Details |  
|:--- |:--- |:--- |  
| Wert \(optional\) | `any` | Grundtypwert oder serialisierbares javascript-Objekt. |  
| unserializableValue \(optional\) | [UnserializableValue](#unserializablevalue) | Grundtypwert, der nicht JSON-stringified sein kann. |  
| objectId \(optional\) | [RemoteObjectId](#remoteobjectid)] | Remoteobjekthandle. |  

---  

### <a name="executioncontextid-integer"></a>ExecutionContextId ganzzahlig  

<a name="executioncontextid"></a>  

ID eines Ausführungskontexts.  

&nbsp;  

---  

### <a name="executioncontextdescription-object"></a>ExecutionContextDescription-Objekt  

<a name="executioncontextdescription"></a>  

Beschreibung einer isolierten Welt.  

| Eigenschaften | Typ | Details |  
|:--- |:--- |:--- |  
| id | [ExecutionContextId](#executioncontextid) | Eindeutige ID des Ausführungskontexts.  Sie kann verwendet werden, um anzugeben, in welchem Ausführungskontext
Die Skriptauswertung sollte durchgeführt werden. |  
| Ursprung | `string` | Ausführungskontextherkunft. |  
| name | `string` | Vom Menschen lesbarer Name, der den angegebenen Kontext beschreibt. |  

---  

### <a name="exceptiondetails-object"></a>ExceptionDetails-Objekt  

<a name="exceptiondetails"></a>  

Ausführliche Informationen zu Ausnahme (oder Fehler), die während der Skriptkompilierung oder -ausführung ausgelöst wurde.  

| Eigenschaften | Typ | Details |  
|:--- |:--- |:--- |  
| exceptionId | `integer` | Ausnahme-ID. |  
| Text | `string` | Ausnahmetext, der zusammen mit dem Ausnahmeobjekt verwendet werden sollte, wenn verfügbar. |  
| lineNumber | `integer` | Zeilennummer des Ausnahmespeicherorts \(0-basiert\). |  
| columnNumber | `integer` | Spaltennummer des Ausnahmespeicherorts \(0-basiert\). |  
| scriptId \(optional\) | [ScriptId](#scriptid) | Skript-ID des Ausnahmespeicherorts. |  
| url \(optional\) | `string` | URL des Ausnahmespeicherorts, der verwendet werden soll, wenn das Skript nicht gemeldet wurde. |  
| stackTrace \(optional\) | [StackTrace](#stacktrace) | JavaScript-Stapelverfolgung, sofern verfügbar. |  
| Ausnahme \(optional\) | [RemoteObject](#remoteobject) | Exception-Objekt, sofern verfügbar. |  
| executionContextId \(optional\) | [ExecutionContextId](#executioncontextid) | Bezeichner des Kontexts, in dem eine Ausnahme eingetreten ist. |  

---  

### <a name="timestamp-integer"></a>Ganze Zeitstempel  

<a name="timestamp"></a>  

Anzahl der Millisekunden seit der Epoche.  

&nbsp;  

---  

### <a name="callframe-object"></a>CallFrame-Objekt  

<a name="callframe"></a>  

Stapeleintrag für Laufzeitfehler und -assertionen.  

| Eigenschaften | Typ | Details |  
|:--- |:--- |:--- |  
| functionName | `string` | JavaScript-Funktionsname. |  
| scriptId | [ScriptId](#scriptid) | JavaScript-Skript-ID. ScriptId ist leer, wenn der Debugger nicht aktiviert ist. |  
| URL | `string` | Name oder URL des JavaScript-Skripts. |  
| lineNumber | `integer` | JavaScript-Skript-Zeilennummer \(0-basiert\). |  
| columnNumber | Ganzzahl | JavaScript-Skriptspaltennummer \(0-basiert\). |  

---  

### <a name="stacktrace-object"></a>StackTrace-Objekt  

<a name="stacktrace"></a>  

Aufrufframes für Assertionen oder Fehlermeldungen.  

| Eigenschaften | Typ | Details |  
|:--- |:--- |:--- |  
| beschreibung \(optional\) | `string` | Zeichenfolgenbeschriftung dieser Stapelverfolgung.  Bei asynchronen Ablaufverfolgungen kann dies ein Name der Funktion sein, die den asynchronen Aufruf initiiert hat. |  
| callFrames | [CallFrame[]](#callframe) | JavaScript-Funktionsname. |  
| übergeordnetes Element \(optional\) | [StackTrace](#stacktrace) | Asynchrone JavaScript-Stapelverfolgung, die diesem Stapel vorausgegangen ist, sofern verfügbar. |  

---  
