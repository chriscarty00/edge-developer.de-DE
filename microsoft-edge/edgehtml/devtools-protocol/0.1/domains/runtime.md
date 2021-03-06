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
# <a name="runtime-domain---devtools-protocol-version-01-edgehtml"></a>Runtime Domain - DevTools Protocol Version 0.1 (EdgeHTML)  

Die Laufzeitdomäne macht die JavaScript-Laufzeit über Remoteauswertungs- und Spiegelobjekte verfügbar.  Auswertungsergebnisse werden als Spiegelobjekt zurückgegeben, das Objekttyp, Zeichenfolgendarstellung und eindeutigen Bezeichner verfügbar macht, die für weitere Objektverweise verwendet werden können.  Originalobjekte werden im Arbeitsspeicher verwaltet, es sei denn, sie werden explizit freigegeben.  

| Klassifizierung | Member |  
|:--- |:--- |  
| [Methoden](#methods) | [enable](#enable), [disable](#disable), [evaluate](#evaluate), [callFunctionOn](#callfunctionon), [getProperties](#getproperties) |  
| [Veranstaltungen](#events) | [executionContextsCleared](#executioncontextscleared), [exceptionThrown](#exceptionthrown) |  
| [Typen](#types) | [ScriptId](#scriptid), [RemoteObjectId](#remoteobjectid), [UnserializableValue](#unserializablevalue), [RemoteObject](#remoteobject), [PropertyDescriptor](#propertydescriptor), [CallArgument](#callargument), [ExecutionContextId](#executioncontextid), [ExceptionDetails](#exceptiondetails), [Timestamp](#timestamp), [CallFrame](#callframe), [StackTrace](#stacktrace) |  

## <a name="methods"></a>Methoden  

### <a name="enable"></a>Aktivieren  

Aktiviert die Berichterstellung des `executionContextsCleared` Ereignisses.  

&nbsp;  

---  

### <a name="disable"></a>Deaktivieren   

Deaktiviert die Berichterstellung für das `executionContextsCleared` Ereignis.  

&nbsp;  

---  

### <a name="evaluate"></a>evaluate  

Wertet Ausdruck für globales Objekt aus.  

| Parameter | Typ | Details |  
|:--- |:--- |:--- |  
| Ausdruck | `string` | Ausdruck, der ausgewertet werden soll. |  
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
| objectId \(optional\) | [RemoteObjectId](#remoteobjectid) | Bezeichner des Objekts, für das die Funktion aufruft.  Entweder `objectId` oder sollte angegeben `executionContextId` werden.  objectId muss aus der Runtime.evaluate()-Funktion kommen. |  
| Argumente \(optional\) | [CallArgument[]](#callargument) | Aufrufargumente.  Alle Aufrufargumente müssen zur gleichen JavaScript-Welt wie das Zielobjekt gehören. |  
| silent \(optional\) | `boolean` | Im automatischen Modus werden ausnahmen, die während der Auswertung ausgelöst werden, nicht gemeldet und die Ausführung nicht angehalten.  Überschreibt `setPauseOnException` den Status. |  
| returnByValue \(optional\) | `boolean` | Gibt an, ob es sich bei dem Ergebnis um ein JSON-Objekt handelt, das per Wert gesendet werden soll. |  
| awaitPromise \(optional\) | `boolean` | Ob die Ausführung für den resultierenden Wert und die Rückgabe nach der erwarteten Zusage `await` ausgeführt werden soll, wird aufgelöst. |  

| Gibt zurück | Typ | Details |  
|:--- |:--- |:--- |  
| result | [RemoteObject](#remoteobject) | Anrufergebnis. |  

---  

### <a name="getproperties"></a>getProperties  

Gibt Eigenschaften eines bestimmten Objekts zurück.  Die Objektgruppe des Ergebnisses wird vom Zielobjekt geerbt.  

| Parameter | Typ | Details |  
|:--- |:--- |:--- |  
| objectId | [RemoteObjectId](#remoteobjectid) | Bezeichner des Objekts, für das Eigenschaften zurückgeben werden.  `objectId` muss von der Funktion `Debugger.evaluateOnCallFrame()` sein. |  
| ownProperties \(optional\) | `boolean` | Wenn `true` , gibt Eigenschaften zurück, die nur zum Element selbst gehören, nicht zu seiner Prototypkette. |  
| accessorPropertiesOnly \(optional\) | `boolean` | **Experimental**.  Wenn `true` , gibt nur Accessoreigenschaften \(mit Getter/Setter\) zurück; interne Eigenschaften werden auch nicht zurückgegeben. |  

| Gibt zurück | Typ | Details |  
|:--- |:--- |:--- |  
| result | [PropertyDescriptor[]](#propertydescriptor) | Objekteigenschaften. |  

---  

## <a name="events"></a>Veranstaltungen  

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
| subtype \(optional\) | `string` | Objektuntertyphinweis.  Nur für `object` Typwerte angegeben.  Zulässige Werte:  `null` `error` , und `promise` |  
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

Represents function call argument.  Entweder Remoteobjekt-ID, unserialisierbarer Grundtypwert oder keiner von `value` \(für nicht definiert\) sollte angegeben werden.  

| Eigenschaften | Typ | Details |  
|:--- |:--- |:--- |  
| Wert \(optional\) | `any` | Grundtypwert oder serialisierbares javascript-Objekt. |  
| unserializableValue \(optional\) | [UnserializableValue](#unserializablevalue) | Grundtypwert, der nicht JSON-stringified sein kann. |  
| objectId \(optional\) | [RemoteObjectId](#remoteobjectid) | Remoteobjekthandle. |  

---  

### <a name="executioncontextid-integer"></a>ExecutionContextId ganzzahlig  

<a name="executioncontextid"></a>  

ID eines Ausführungskontexts.  

&nbsp;  

---  

### <a name="exceptiondetails-object"></a>ExceptionDetails-Objekt  

<a name="exceptiondetails"></a>  

Ausführliche Informationen zu Ausnahme \(oder Fehler\), die während der Skriptkompilierung oder -ausführung ausgelöst wurde.  

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
| scriptId | [ScriptId](#scriptid) | JavaScript-Skript-ID. |  
| URL | `string` | Name oder URL des JavaScript-Skripts. |  
| lineNumber | `integer` | JavaScript-Skript-Zeilennummer \(0-basiert\). |  
| columnNumber | `integer` | JavaScript-Skriptspaltennummer \(0-basiert\). |  

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
