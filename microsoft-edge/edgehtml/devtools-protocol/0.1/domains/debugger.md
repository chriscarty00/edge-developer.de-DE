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
# <a name="debugger-domain---devtools-protocol-version-01-edgehtml"></a>Debuggerdomäne – DevTools Protocol Version 0.1 (EdgeHTML)  
  
Die Debuggerdomäne macht JavaScript-Debuggingfunktionen verfügbar.  Es ermöglicht das Festlegen und Entfernen von Haltepunkten, das Schrittweise Durchbrechen der Ausführung, das Untersuchen von Stapelverfolgungen usw.

| Klassifizierung | Member |  
|:--- |:--- |  
| [Methoden](#methods) | [enable](#enable), [disable](#disable), [getPossibleBreakpoints](#getpossiblebreakpoints), [setBreakpointsActive](#setbreakpointsactive), [setBreakpointByUrl](#setbreakpointbyurl), [setBreakpoint](#setbreakpoint), [removeBreakpoint](#removebreakpoint), [stepOver](#stepover), [stepInto](#stepinto), [stepOut](#stepout), [pause](#pause), [resume](#resume), [getScriptSource](#getscriptsource), [setPauseOnExceptions](#setpauseonexceptions), [evaluateOnCallFrame](#evaluateoncallframe), [setVariableValue](#setvariablevalue), [setBlackboxPatterns](#setblackboxpatterns), [msSetDebuggerPropertyValue](#mssetdebuggerpropertyvalue) |  
| [Veranstaltungen](#events) | [scriptParsed](#scriptparsed), [breakpointResolved](#breakpointresolved), [paused](#paused), [resumed](#resumed) |  
| [Typen](#types) | [BreakpointId](#breakpointid), [CallFrameId](#callframeid), [Location](#location), [BreakLocation](#breaklocation), [CallFrame](#callframe), [Scope](#scope) |  
| [Abhängigkeiten](#dependencies) | [Laufzeit](./runtime.md) |  

## <a name="methods"></a>Methoden  

### <a name="enable"></a>Aktivieren  

Aktiviert den Debugger für die angegebene Seite.  Clients sollten nicht davon ausgehen, dass das Debuggen aktiviert wurde, bis das Ergebnis für diesen Befehl empfangen wurde.  

&nbsp;  

---  

### <a name="disable"></a>Deaktivieren   

Deaktiviert den Debugger für eine bestimmte Seite.  

&nbsp;  

---  

### <a name="getpossiblebreakpoints"></a>getPossibleBreakpoints  

Gibt mögliche Speicherorte für Haltepunkte zurück.  scriptId an Start- und Endbereichspositionen sollte identisch sein.  

| Parameter | Typ | Details |  
|:--- |:--- |:--- |  
| start | [Ort](#location) | Anfang des Bereichs zum Durchsuchen möglicher Haltepunktpositionen in. |  
| Aufhören | [Ort](#location) | Ende des Bereichs, um mögliche Haltepunktpositionen in \(ohne\) zu durchsuchen.  Wenn nicht angegeben, wird das Ende der Skripts als Ende des Bereichs verwendet. |  

| Gibt zurück | Typ | Details |  
|:--- |:--- |:--- |  
| Speicherorte | [BreakLocation](#breaklocation) | Liste der möglichen Haltepunktpositionen. |  

---  

### <a name="setbreakpointsactive"></a>setBreakpointsActive  

Aktiviert/deaktiviert alle Haltepunkte auf der Seite.  

| Parameter | Typ | Details |  
|:--- |:--- |:--- |  
| active | `boolean` | Neuer Wert für den aktiven Zustand der Haltepunkte. |  

---  

### <a name="setbreakpointbyurl"></a>setBreakpointByUrl  

Legt den JavaScript-Haltepunkt an einem bestimmten Speicherort fest, der entweder durch URL oder URL regex angegeben wird.  Sobald dieser Befehl ausgegeben wurde, werden für alle vorhandenen analysierten Skripts Haltepunkte aufgelöst und in der Eigenschaft `locations` zurückgegeben.  Eine weitere übereinstimmende Skript-Analyse führt zu nachfolgenden `breakpointResolved` Ereignissen.  Dieser logische Haltepunkt überdauert seitenladen.  

| Parameter | Typ | Details |  
|:--- |:--- |:--- |  
| lineNumber | `integer` | Zeilennummer zum Festlegen des Haltepunkts. |  
| url \(optional\) | `string` | URL der Ressourcen, auf die der Haltepunkt festgelegt werden soll. |  
| urlRegex \(optional\) | `string` | Regex-Muster für die URLs der Ressourcen zum Festlegen von Haltepunkten.  Entweder `url` oder muss angegeben `urlRegex` werden. |  
| columnNumber \(optional\) | `integer` | Offset in der Linie, um den Haltepunkt zu festlegen. |  
| Bedingung \(optional\) | `string` | Ausdruck, der als Haltepunktbedingung verwendet werden soll.  Wenn angegeben, wird der Debugger nur dann am Haltepunkt beendet, wenn dieser Ausdruck auf true ausgewertet wird. |  

| Gibt zurück | Typ | Details |  
|:--- |:--- |:--- |  
| breakpointId | [BreakpointId](#breakpointid) | ID des erstellten Haltepunkts für weitere Referenz. |  
| Speicherorte | [Location[]](#location) | Liste der Speicherorte, in die dieser Haltepunkt beim Hinzufügen aufgelöst wurde. |  

---  

### <a name="setbreakpoint"></a>setBreakpoint  

Legt den JavaScript-Haltepunkt an einem bestimmten Speicherort fest.  

| Parameter | Typ | Details |  
|:--- |:--- |:--- |  
| location | [Ort](#location) | Speicherort zum Festlegen des Haltepunkts. |  
| Bedingung \(optional\) | `string` | Ausdruck, der als Haltepunktbedingung verwendet werden soll.  Wenn angegeben, wird der Debugger nur dann am Haltepunkt beendet, wenn dieser Ausdruck auf true ausgewertet wird. |  

| Gibt zurück | Typ | Details |  
|:--- |:--- |:--- |  
| breakpointId | [BreakpointId](#breakpointid) | ID des erstellten Haltepunkts für weitere Referenz. |  
| actualLocation | [Ort](#location) | Speicherort, in den dieser Haltepunkt aufgelöst wurde. |  

---  

### <a name="removebreakpoint"></a>removeBreakpoint  

Entfernt den JavaScript-Haltepunkt.  

| Parameter | Typ | Details |  
|:--- |:--- |:--- |  
| breakpointId | [BreakpointId](#breakpointid) | &nbsp; |  

---  

### <a name="stepover"></a>stepOver  

Schritte über die Anweisung.  

&nbsp;  

---  

### <a name="stepinto"></a>stepInto  

Schritte in den Funktionsaufruf.  

&nbsp;  

---  

### <a name="stepout"></a>stepOut  

Tritt aus dem Funktionsaufruf aus.  

&nbsp;  

---  

### <a name="pause"></a>pause  

Stoppt bei der nächsten JavaScript-Anweisung.  

&nbsp;  

---  

### <a name="resume"></a>resume  

Setzt die JavaScript-Ausführung fort.  

&nbsp;  

---  

### <a name="getscriptsource"></a>getScriptSource  

Gibt die Quelle für das Skript mit der angegebenen ID zurück.  

| Parameter | Typ | Details |  
|:--- |:--- |:--- |  
| scriptId | [Runtime.ScriptId](./runtime.md#scriptid) | DIE ID des Skripts, für das Die Quelle erhalten werden soll. |  
| Gibt zurück | Typ | Details |  
|:--- |:--- |:--- |  
| scriptSource | `string` | Skriptquelle. |  

---  

### <a name="setpauseonexceptions"></a>setPauseOnExceptions  

Definiert pause on exceptions state.  Kann so festgelegt werden, dass alle Ausnahmen, nicht abgefangenen Ausnahmen oder keine Ausnahmen beendet werden.  Die anfängliche Pause für den Ausnahmezustand ist `none` .  

| Parameter | Typ | Details |  
|:--- |:--- |:--- |  
| state | `string` | Halten Sie den Ausnahmemodus an.  Zulässige Werte:  `none` `uncaught` , und `all` |  

---  

### <a name="evaluateoncallframe"></a>evaluateOnCallFrame  

Wertet Ausdruck für einen bestimmten Aufrufrahmen aus.  

| Parameter | Typ | Details |  
|:--- |:--- |:--- |  
| callFrameId | [CallFrameId](#callframeid) | Anrufrahmen-ID, die ausgewertet werden soll. |  
| Ausdruck | `string` | Ausdruck, der ausgewertet werden soll. |  
| Gibt zurück | Typ | Details |  
|:--- |:--- |:--- |  
| result | [Runtime.RemoteObject](./runtime.md#remoteobject) | Objektwrapper für das Auswertungsergebnis. |  

---  

### <a name="setvariablevalue"></a>setVariableValue  

Ändert den Wert der Variablen in einem Callframe.  Objektbasierte Bereiche werden nicht unterstützt und müssen manuell mutiert werden.  

| Parameter | Typ | Details |  
|:--- |:--- |:--- |  
| scopeNumber | `integer` | 0-basierte Anzahl des Bereichs, wie in der Bereichskette aufgeführt.  Nur `local` , `closure` und `catch` Bereichstypen sind zulässig.  Andere Bereiche können manuell bearbeitet werden. |  
| variableName | `string` | Variabler Name. |  
| newValue | [Runtime.CallArgument](./runtime.md#callargument) | Neuer Variabler Wert. |  
| callFrameId | [CallFrameId](#callframeid) | ID des Callframes, der eine Variable enthält. |  

---  

### <a name="setblackboxpatterns"></a>setBlackboxPatterns  

**Experimental**.  Ersetzen Sie vorherige Blackboxmuster durch übergebene Muster.  Erzwingt das Back-End, das Schrittweise/Anhalten in Skripts zu überspringen, deren URL mit einem der Muster übereinstimmen.  Der Debugger versucht, das blackboxed-Skript zu verlassen, indem er mehrere Male ausgeführt wird, und schließlich zu einem Fehler `step in` `step out` greifen.  

| Parameter | Typ | Details |  
|:--- |:--- |:--- |  
| Muster | `string[]` | Array von Regexps, das zum Überprüfen der Skript-URL auf den Blackboxstatus verwendet wird. |  

---  

### <a name="mssetdebuggerpropertyvalue"></a>msSetDebuggerPropertyValue  

**Experimental**.  Microsoft: Legt die angegebene Debuggereigenschaft auf den angegebenen Wert fest.  

| Parameter | Typ | Details |  
|:--- |:--- |:--- |  
| debuggerPropertyId | `string` | Microsoft: Die eigenschafts-ID \(d. h. msDebuggerPropertyId\), die festgelegt werden soll. |  
| newValue | `string` | &nbsp; |  

---  

## <a name="events"></a>Veranstaltungen  

### <a name="scriptparsed"></a>scriptParsed  

Wird ausgelöst, wenn das Skript analysiert wird.  Dieses Ereignis wird auch für alle bekannten und nicht abgeholten Skripts beim Aktivieren des Debuggers ausgelöst.  

| Parameter | Typ | Details |  
|:--- |:--- |:--- |  
| scriptId | [Runtime.ScriptId](./runtime.md#scriptid) | Bezeichner des analysierten Skripts. |  
| URL | `string` | URL oder Name des analysierten Skripts \(falls ein\). |  
| startLine | `integer` | Zeilenversatz des Skripts innerhalb der Ressource mit der angegebenen URL \(für Skripttags\). |  
| startColumn | `integer` | Spaltenversatz des Skripts innerhalb der Ressource mit einer angegebenen URL. |  
| endLine | `integer` | Letzte Zeile des Skripts. |  
| endColumn | `integer` | Länge der letzten Zeile des Skripts. |  
| executionContextId | [Runtime.ExecutionContextId](./runtime.md#executioncontextid) | Gibt den Kontext für die Skripterstellung an. |  
| sourceMapURL \(optional\) | `string` | URL der Quellzuordnung, die dem Skript zugeordnet ist (falls eine). |  
| length \(optional\) | `integer` | **Experimental**.  Diese Skriptlänge. |  
| msParentId \(optional\) | `string` | **Experimental**.  Dies ist die übergeordnete Dokument-ID. |  
| msMimeType \(optional\) | `string` | **Experimental**.  Dies ist der Mimetyp. |  
| msIsDynamicCode \(optional\) | `boolean` | **Experimental**.  Dies gibt an, ob es sich um dynamischen Code handelt. |  
| msLongDocumentId \(optional\) | `integer` | **Experimental**.  Dies ist die lange Dokument-ID. |  

---  

### <a name="breakpointresolved"></a>breakpointResolved  

Wird ausgelöst, wenn der Haltepunkt in ein tatsächliches Skript und einen tatsächlichen Speicherort aufgelöst wird.  

| Parameter | Typ | Details |  
|:--- |:--- |:--- |  
| breakpointId | [BreakpointId](#breakpointid) | Eindeutiger Bezeichner des Haltepunkts. |  
| location | [Ort](#location) | Tatsächliche Haltepunktposition. |  
| msLength \(optional\) | `integer` | **Experimental**.  Microsoft: Länge des Codes \(d. h. Anzahl der Zeichen\) am Haltepunktspeicherort. |  

---  

### <a name="paused"></a>angehalten  

Wird ausgelöst, wenn der Debugger für einen Haltepunkt oder eine Ausnahme umbricht.  

| Parameter | Typ | Details |  
|:--- |:--- |:--- |  
| callFrames | [CallFrame[]](#callframe) | Aufrufstapel, auf dem der Debugger beendet wurde. |  
| reason | `string` | Grund anhalten.  Zulässige Werte:  `breakpoint` `step` , , , `exception` und `other` |  
| data \(optional\) | `object` | Objekt mit unterbrechungsspezifischen Hilfseigenschaften. |  
| hitBreakpoints \(optional\) | `string[]` | Hit breakpoints IDs |  

---  

### <a name="resumed"></a>fortgesetzt  

Wird ausgelöst, wenn der Debugger die Ausführung wieder auf sich nimmt.  

&nbsp;  

---  

## <a name="types"></a>Typen  

### <a name="breakpointid-string"></a>BreakpointId-Zeichenfolge  

<a name="breakpointid"></a>  

Haltepunkt-ID.  

&nbsp;  

---  

### <a name="callframeid-string"></a>CallFrameId-Zeichenfolge  

<a name="callframeid"></a>  

Anrufrahmen-ID.  

&nbsp;  

---  

### <a name="location-object"></a>Location-Objekt  

<a name="location"></a>  

Speicherort im Quellcode.  

| Eigenschaften | Typ | Details |  
|:--- |:--- |:--- |  
| scriptId | [Runtime.ScriptId](./runtime.md#scriptid) | Skript-ID, wie in der `Debugger.scriptParsed` angegeben. |  
| lineNumber | `integer` | Zeilennummer im Skript \(0-basiert\). |  
| columnNumber \(optional\) | `integer` | Spaltennummer im Skript \(0-basiert\). |  
| msLength | `integer` | Microsoft: Länge des Codes \(d. h. Anzahl der Zeichen\) in diesem Aufrufrahmen. |  

---  

### <a name="breaklocation-object"></a>BreakLocation-Objekt  

<a name="breaklocation"></a>  

Speicherort im Quellcode umbrechen.  

| Eigenschaften | Typ | Details |  
|:--- |:--- |:--- |  
| scriptId | [Runtime.ScriptId](./runtime.md#scriptid) | Skript-ID, wie in der `Debugger.scriptParsed` angegeben. |  
| lineNumber | `integer` | Zeilennummer im Skript \(0-basiert\). |  
| columnNumber \(optional\) | `integer` | Spaltennummer im Skript \(0-basiert\). |  
| msLength | `integer` | Microsoft: Länge des Codes \(d. h. Anzahl der Zeichen\) in diesem Aufrufrahmen. |  
| Typ \(optional\) | `string` | Zulässige Werte:  `debuggerStatement` `call` , und `return` |  

---  

### <a name="callframe-object"></a>CallFrame-Objekt  

<a name="callframe"></a>  

JavaScript-Aufrufrahmen.  Array von Anrufframes bilden die Aufrufliste.  

| Eigenschaften | Typ | Details |  
|:--- |:--- |:--- |  
| callFrameId | [CallFrameId](#callframeid) | Anrufrahmen-ID.  Dieser Bezeichner ist nur gültig, wenn der Debugger angehalten wird. |  
| functionName | `string` | Name der für diesen Aufrufrahmen aufgerufenen JavaScript-Funktion. |  
| functionLocation \(optional\) | [Ort](#location) | **Experimental**.  Speicherort im Quellcode. |  
| location | [Ort](#location) | Speicherort im Quellcode. |  
| URL | `string` | Name oder URL des JavaScript-Skripts. |  
| scopeChain | [Scope[]](#scope) | Bereichskette für diesen Anrufrahmen. |  
| this | [Runtime.RemoteObject](./runtime.md#remoteobject) | `this` -Objekt für diesen Aufrufrahmen. |  
| returnValue \(optional\) | [Runtime.RemoteObject](./runtime.md#remoteobject) | Der zurückgegebene Wert, wenn sich die Funktion am Rückgabepunkt befindet. |  

---  

### <a name="scope-object"></a>Scope-Objekt  

<a name="scope"></a>  

Bereichsbeschreibung.  

| Eigenschaften | Typ | Details |  
|:--- |:--- |:--- |  
| Typ | `string` | Bereichstyp.  Zulässige Werte:  `global` , , , , , , `local` , `with` `closure` `catch` `block` `script` `eval` und `module` |  
| Objekt | [Runtime.RemoteObject](./runtime.md#remoteobject) | Objekt, das den Bereich darstellt.  Für und Bereiche stellt sie das tatsächliche Objekt dar. Für die restlichen Bereiche ist es ein künstliches transientes Objekt, das Bereichsvariablen als `global` `with` Eigenschaften aufzählt. |  
| Name \(optional\) | `string` | &nbsp; |  
| startLocation \(optional\) | [Ort](#location) | Speicherort im Quellcode, an dem der Bereich beginnt. |  
| endLocation \(optional\) | [Ort](#location) | Speicherort im Quellcode, an dem der Bereich endet. |  

---  

## <a name="dependencies"></a>Abhängigkeiten  

[Laufzeit](./runtime.md)  
