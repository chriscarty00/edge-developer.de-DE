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
# Runtime
Runtime-Domäne macht JavaScript-Runtime mithilfe von Remote Auswertungs-und Spiegel Objekten verfügbar. Evaluierungsergebnisse werden als Spiegelungs Objekt zurückgegeben, die den Objekttyp, die Zeichenfolgendarstellung und den eindeutigen Bezeichner verfügbar machen, die für weitere Objektverweise verwendet werden können. Ursprüngliche Objekte werden im Arbeitsspeicher verwaltet, sofern Sie nicht explizit freigegeben werden.

| | |
|-|-|
| [**Methoden**](#methods) | [aktivieren](#enable), [Deaktivieren](#disable), [Auswerten](#evaluate), [callFunctionOn](#callfunctionon), [awaitPromise](#awaitpromise), [GetProperties](#getproperties), [globalLexicalScopeNames](#globallexicalscopenames), [ReleaseObject](#releaseobject), [releaseObjectGroup](#releaseobjectgroup), [discardConsoleEntries](#discardconsoleentries) |
| [**Ereignisse**](#events) | [executionContextCreated](#executioncontextcreated), [executionContextDestroyed](#executioncontextdestroyed), [executionContextsCleared](#executioncontextscleared), [exceptionThrown](#exceptionthrown), [consoleAPICalled](#consoleapicalled) |
| [**Typen**](#types) | [Skript](#scriptid)- [RemoteObjectId](#remoteobjectid), [unserializablevalue](#unserializablevalue), [,](#remoteobject) [PropertyDescriptor](#propertydescriptor), [CallArgument](#callargument), [ExecutionContextId](#executioncontextid), [ExecutionContextDescription](#executioncontextdescription), [ExceptionDetails](#exceptiondetails), [timestamp](#timestamp), [CallFrame](#callframe), [StackTrace](#stacktrace) |
## Methoden

### Aktivieren
Ermöglicht die Berichterstellung <code>executionContextCreated</code> <code>executionContextDestroyed</code> und die <code>executionContextsCleared</code> Ereignisse. Wenn die Berichterstellung aktiviert wird <code>executionContextCreated</code> , wird das Ereignis für jeden vorhandenen Ausführungskontext sofort gesendet.

</p>

---

### Deaktivieren 
Deaktiviert die Berichterstellung und die <code>executionContextCreated</code> <code>executionContextDestroyed</code> <code>executionContextsCleared</code> Ereignisse.

</p>

---

### bewerten
Wertet Ausdruck für globales Objekt aus.

<table>
    <thead>
        <tr>
            <th>Parameter</th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>Ausdruck</td>
            <td><code class="flyout">string</code></td>
            <td>Ausdruck, der ausgewertet werden soll.</td>
        </tr>
        <tr>
            <td>includeCommandLineAPI <br/> <i>Optional</i></td>
            <td><code class="flyout">boolean</code></td>
            <td>Bestimmt, ob die Befehlszeilen-API während der Auswertung verfügbar sein soll.</td>
        </tr>
        <tr>
            <td>objectGroup <br/> <i>Optional</i></td>
            <td><code class="flyout">string</code></td>
            <td>Symbolischer Gruppenname, der zum Freigeben mehrerer Objekte verwendet werden kann.</td>
        </tr>
        <tr>
            <td>lautlos <br/> <i>Optional</i></td>
            <td><code class="flyout">boolean</code></td>
            <td>Im unbeaufsichtigten Modus werden während der Auswertung ausgelöste Ausnahmen nicht gemeldet, und die Ausführung wird nicht angehalten. Überschreibt den <code>setPauseOnException</code> Zustand.</td>
        </tr>
        <tr>
            <td>ContextId <br/> <i>Optional</i></td>
            <td><a href="#executioncontextid"><code class="flyout">ExecutionContextId</code></a></td>
            <td>Gibt an, in welchem Ausführungskontext die Auswertung durchgeführt werden soll. Wenn der Parameter ausgelassen wird, wird die Auswertung im Kontext der geprüften Seite durchgeführt.</td>
        </tr>
        <tr>
            <td>returnByValue <br/> <i>Optional</i></td>
            <td><code class="flyout">boolean</code></td>
            <td>Gibt an, ob es sich bei dem Ergebnis um ein JSON-Objekt handelt, das als Wert gesendet werden soll.</td>
        </tr>
        <tr>
            <td>awaitPromise <br/> <i>Optional</i></td>
            <td><code class="flyout">boolean</code></td>
            <td>Ob die Ausführung <code>await</code> für den resultierenden Wert und die Rückgabe nach dem erwarteten Versprechen aufgelöst werden soll.</td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th>Gibt</th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>Ergebnis</td>
            <td><a href="#remoteobject"><code class="flyout">RemoteObject</code></a></td>
            <td>Auswertungsergebnis.</td>
        </tr>
    </tbody>
</table>
</p>

---

### callFunctionOn
Calls-Funktion mit einer angegebenen Deklaration für das angegebene Objekt. Die Objektgruppe des Ergebnisses wird vom Zielobjekt geerbt.

<table>
    <thead>
        <tr>
            <th>Parameter</th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>functionDeclaration</td>
            <td><code class="flyout">string</code></td>
            <td>Die Deklaration der Funktion, die aufgerufen werden soll.</td>
        </tr>
        <tr>
            <td>ObjectID <br/> <i>Optional</i></td>
            <td><a href="#remoteobjectid"><code class="flyout">RemoteObjectId</code></a></td>
            <td>Der Bezeichner des Objekts, für das die Funktion aufgerufen werden soll. Es sollten entweder ObjectID oder executionContextId angegeben werden.  ObjectID muss aus der Runtime. Evaluate ()-Funktion sein.</td>
        </tr>
        <tr>
            <td>arguments <br/> <i>Optional</i></td>
            <td><a href="#callargument"><code class="flyout">CallArgument[]</code></a></td>
            <td>Rufen Sie Argumente auf. Alle Anruf Argumente müssen zur gleichen JavaScript-Welt gehören wie das Zielobjekt.</td>
        </tr>
        <tr>
            <td>lautlos <br/> <i>Optional</i></td>
            <td><code class="flyout">boolean</code></td>
            <td>Im unbeaufsichtigten Modus werden während der Auswertung ausgelöste Ausnahmen nicht gemeldet, und die Ausführung wird nicht angehalten. Überschreibt den <code>setPauseOnException</code> Zustand.</td>
        </tr>
        <tr>
            <td>returnByValue <br/> <i>Optional</i></td>
            <td><code class="flyout">boolean</code></td>
            <td>Gibt an, ob es sich bei dem Ergebnis um ein JSON-Objekt handelt, das als Wert gesendet werden soll.</td>
        </tr>
        <tr>
            <td>awaitPromise <br/> <i>Optional</i></td>
            <td><code class="flyout">boolean</code></td>
            <td>Ob die Ausführung <code>await</code> für den resultierenden Wert und die Rückgabe nach dem erwarteten Versprechen aufgelöst werden soll.</td>
        </tr>
        <tr>
            <td>executionContextId <br/> <i>Optional</i></td>
            <td><a href="#executioncontextid"><code class="flyout">ExecutionContextId</code></a></td>
            <td>Gibt den Ausführungskontext an, auf dem das globale Objekt zum Aufrufen von Funktion verwendet wird. Entweder executionContextId oder ObjectID sollte angegeben werden.</td>
        </tr>
        <tr>
            <td>objectGroup <br/> <i>Optional</i></td>
            <td><code class="flyout">string</code></td>
            <td>Symbolischer Gruppenname, der zum Freigeben mehrerer Objekte verwendet werden kann. Wenn objectgroup nicht angegeben ist und ObjectID ist, wird objectgroup von Object geerbt.</td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th>Gibt</th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>Ergebnis</td>
            <td><a href="#remoteobject"><code class="flyout">RemoteObject</code></a></td>
            <td>Ergebnis des Anrufs.</td>
        </tr>
    </tbody>
</table>
</p>

---

### awaitPromise
Hinzufügen eines Handlers zum Versprechen mit der angegebenen Promise-Objekt-ID.

<table>
    <thead>
        <tr>
            <th>Parameter</th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>promiseObjectId</td>
            <td><a href="#remoteobjectid"><code class="flyout">RemoteObjectId</code></a></td>
            <td>Bezeichner des Versprechens.</td>
        </tr>
        <tr>
            <td>returnByValue <br/> <i>Optional</i></td>
            <td><code class="flyout">boolean</code></td>
            <td>Gibt an, ob es sich bei dem Ergebnis um ein JSON-Objekt handelt, das als Wert gesendet werden soll.</td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th>Gibt</th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>Ergebnis</td>
            <td><a href="#remoteobject"><code class="flyout">RemoteObject</code></a></td>
            <td>Ergebnis versprechen.  Enthält einen abgelehnten Wert, wenn Promise abgelehnt wurde.</td>
        </tr>
    </tbody>
</table>
</p>

---

### GetProperties
Gibt Eigenschaften eines angegebenen Objekts zurück. Die Objektgruppe des Ergebnisses wird vom Zielobjekt geerbt.

<table>
    <thead>
        <tr>
            <th>Parameter</th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>ObjectID</td>
            <td><a href="#remoteobjectid"><code class="flyout">RemoteObjectId</code></a></td>
            <td>Der Bezeichner des Objekts, für das Eigenschaften zurückgegeben werden sollen. ObjectID muss aus der Debugger. evaluateOnCallFrame ()-Funktion sein.</td>
        </tr>
        <tr>
            <td>ownProperties <br/> <i>Optional</i></td>
            <td><code class="flyout">boolean</code></td>
            <td>Ist "true", gibt Eigenschaften zurück, die nur dem Element selbst und nicht der zugehörigen Prototypkette gehören.</td>
        </tr>
        <tr>
            <td>accessorPropertiesOnly <br/> <i>Optional</i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span><b>Experimenteller. </b></span>Ist "true", gibt nur Accessor-Eigenschaften (mit Getter/Setter) zurück. interne Eigenschaften werden auch nicht zurückgegeben.</td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th>Gibt</th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>Ergebnis</td>
            <td><a href="#propertydescriptor"><code class="flyout">PropertyDescriptor[]</code></a></td>
            <td>Objekteigenschaften.</td>
        </tr>
    </tbody>
</table>
</p>

---

### globalLexicalScopeNames
Gibt alle Let-, const-und Class-Variablen aus dem globalen Bereich der Konsole zurück.

<table>
    <thead>
        <tr>
            <th>Gibt</th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>Namen</td>
            <td><code class="flyout">string[]</code></td>
            <td></td>
        </tr>
    </tbody>
</table>
</p>

---

### ReleaseObject
Gibt das Remoteobjekt mit der angegebenen ID frei.

<table>
    <thead>
        <tr>
            <th>Parameter</th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>ObjectID</td>
            <td><a href="#remoteobjectid"><code class="flyout">RemoteObjectId</code></a></td>
            <td>Der Bezeichner des freizugebenden Objekts. </td>
        </tr>
    </tbody>
</table>
</p>

---

### releaseObjectGroup
Gibt alle Remoteobjekte frei, die zu einer bestimmten Gruppe gehören.

<table>
    <thead>
        <tr>
            <th>Parameter</th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>objectGroup</td>
            <td><code class="flyout">string</code></td>
            <td>Name der symbolischen Objektgruppe. </td>
        </tr>
    </tbody>
</table>
</p>

---

### discardConsoleEntries
Verwirft gesammelte Ausnahmen und Konsolen-API-Aufrufe.

</p>

---

## Ereignisse

### executionContextCreated
Wird ausgegeben, wenn ein neuer Ausführungskontext erstellt wird.

<table>
    <thead>
        <tr>
            <th>Parameter</th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>Kontext</td>
            <td><a href="#executioncontextdescription"><code class="flyout">ExecutionContextDescription</code></a></td>
            <td>Ein neu erstellter Ausführungskontext.</td>
        </tr>
    </tbody>
</table>
</p>

---

### executionContextDestroyed
Wird ausgegeben, wenn der Ausführungskontext zerstört wurde.

<table>
    <thead>
        <tr>
            <th>Parameter</th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>executionContextId</td>
            <td><a href="#executioncontextid"><code class="flyout">ExecutionContextId</code></a></td>
            <td>ID des zerstörten Kontexts</td>
        </tr>
    </tbody>
</table>
</p>

---

### executionContextsCleared
Wird ausgegeben, wenn alle executionContexts im Browser gelöscht wurden

</p>

---

### exceptionThrown
Wird ausgegeben, wenn eine Ausnahme ausgelöst und nicht behandelt wurde.

<table>
    <thead>
        <tr>
            <th>Parameter</th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>Timestamp</td>
            <td><a href="#timestamp"><code class="flyout">Timestamp</code></a></td>
            <td>Der Zeitstempel der Ausnahme.</td>
        </tr>
        <tr>
            <td>exceptionDetails</td>
            <td><a href="#exceptiondetails"><code class="flyout">ExceptionDetails</code></a></td>
            <td></td>
        </tr>
    </tbody>
</table>
</p>

---

### consoleAPICalled


<table>
    <thead>
        <tr>
            <th>Parameter</th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>Typ</td>
            <td><code class="flyout">string</code> <br/> <i>Zulässige Werte: Protokoll, Info, Warnung, Fehler, Debuggen, Assert, Tabelle, Ablaufverfolgung, dir, DirXML, Clear, SELECT, count, countReset, timeEnd, timestamp, startGroup, startGroupCollapsed, endGroup</i></td>
            <td>Der Typ des Anrufs. Dazu gehören Protokoll, Informationen, Warnung, Fehler, Debuggen, Assert, Tabelle, Ablaufverfolgung, dir, DirXML, Clear, SELECT, count, countReset, timeEnd, Exception, timestamp, Group, groupCollapsed, groupEnd.</td>
        </tr>
        <tr>
            <td>args</td>
            <td><a href="#remoteobject"><code class="flyout">RemoteObject[]</code></a></td>
            <td>Rufen Sie Argumente auf.</td>
        </tr>
        <tr>
            <td>executionContextId</td>
            <td><a href="#executioncontextid"><code class="flyout">ExecutionContextId</code></a></td>
            <td>Bezeichner des Kontexts, in dem der Konsolen Aufruf durchgeführt wurde</td>
        </tr>
        <tr>
            <td>Timestamp <br/> <i>Optional</i></td>
            <td><a href="#timestamp"><code class="flyout">Timestamp</code></a></td>
            <td>Anruf Zeitstempel.</td>
        </tr>
        <tr>
            <td>StackTrace <br/> <i>Optional</i></td>
            <td><a href="#stacktrace"><code class="flyout">StackTrace</code></a></td>
            <td>Aufgezeichnete Stapelüberwachung, falls verfügbar</td>
        </tr>
    </tbody>
</table>
</p>

---

## Typen

### <a name="scriptid"></a> SkriptID `string`

Eindeutiger Skriptbezeichner.

</p>

---

### <a name="remoteobjectid"></a> RemoteObjectId `string`

Eindeutige Objekt-ID.

</p>

---

### <a name="unserializablevalue"></a> Unserializablevalue `string`

Primitiver Wert, der nicht JSON-stringified sein kann.

##### Zulässige Werte
Unendlichkeit, Nan,-Unendlichkeit,-0
</p>

---

### <a name="remoteobject"></a> RemoteObject `object`

Spiegelungs Objekt, das auf das ursprüngliche JavaScript-Objekt verweist

<table>
    <thead>
        <tr>
            <th>Eigenschaften</th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>Typ</td>
            <td><code class="flyout">string</code> <br/> <i>Zulässige Werte: Objekt, Funktion, undefined, Zeichenfolge, Zahl, boolescher Wert, Symbol</i></td>
            <td>Objekttyp.</td>
        </tr>
        <tr>
            <td>Untertyp <br/> <i>Optional</i></td>
            <td><code class="flyout">string</code> <br/> <i>Zulässige Werte: NULL, Fehler, Promise, Knoten</i></td>
            <td>Hinweis für den Untertyp des Objekts. Nur für <code>object</code> Typwerte angegeben.</td>
        </tr>
        <tr>
            <td>ClassName <br/> <i>Optional</i></td>
            <td><code class="flyout">string</code></td>
            <td>Name der Objektklasse (Konstruktor). Nur für <code>object</code> Typwerte angegeben.</td>
        </tr>
        <tr>
            <td>value <br/> <i>Optional</i></td>
            <td><code class="flyout">any</code></td>
            <td>Remote Objektwert im Fall von primitiven Werten oder JSON-Werten (sofern angefordert).</td>
        </tr>
        <tr>
            <td>unserializablevalue <br/> <i>Optional</i></td>
            <td><a href="#unserializablevalue"><code class="flyout">UnserializableValue</code></a></td>
            <td>Primitiver Wert, der nicht JSON-stringified sein kann <code>value</code>, aber ruft diese Eigenschaft ab.</td>
        </tr>
        <tr>
            <td>description <br/> <i>Optional</i></td>
            <td><code class="flyout">string</code></td>
            <td>Zeichenfolgendarstellung des Objekts.</td>
        </tr>
        <tr>
            <td>ObjectID <br/> <i>Optional</i></td>
            <td><a href="#remoteobjectid"><code class="flyout">RemoteObjectId</code></a></td>
            <td>Eindeutige Objekt-ID (für nicht primitive Werte).</td>
        </tr>
        <tr>
            <td>msDebuggerPropertyId <br/> <i>Optional</i></td>
            <td><code class="flyout">string</code></td>
            <td><span><b>Experimenteller. </b></span>Microsoft: die zugeordnete Debugger-Eigenschafts-ID für dieses Objekt.</td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="propertydescriptor"></a> PropertyDescriptor `object`

Objekteigenschaften Deskriptor

<table>
    <thead>
        <tr>
            <th>Eigenschaften</th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>name</td>
            <td><code class="flyout">string</code></td>
            <td>Eigenschaftsname oder Symbol Beschreibung.</td>
        </tr>
        <tr>
            <td>value <br/> <i>Optional</i></td>
            <td><a href="#remoteobject"><code class="flyout">RemoteObject</code></a></td>
            <td>Der Wert, der der Eigenschaft zugeordnet ist.</td>
        </tr>
        <tr>
            <td>beschreibbar <br/> <i>Optional</i></td>
            <td><code class="flyout">boolean</code></td>
            <td>"True", wenn der Wert, der der Eigenschaft zugeordnet ist, geändert werden kann (nur Daten Deskriptoren).</td>
        </tr>
        <tr>
            <td>Abrufen <br/> <i>Optional</i></td>
            <td><a href="#remoteobject"><code class="flyout">RemoteObject</code></a></td>
            <td>Eine Funktion, die als Getter für die Eigenschaft dient, oder <code>undefined</code> Wenn kein Getter vorhanden ist (nur Accessor-Deskriptoren).</td>
        </tr>
        <tr>
            <td>set <br/> <i>Optional</i></td>
            <td><a href="#remoteobject"><code class="flyout">RemoteObject</code></a></td>
            <td>Eine Funktion, die als Setter für die Eigenschaft dient, oder <code>undefined</code> Wenn kein Setter vorhanden ist (nur Accessor-Deskriptoren).</td>
        </tr>
        <tr>
            <td>konfigurierbar</td>
            <td><code class="flyout">boolean</code></td>
            <td>"True", wenn der Typ dieses Eigenschaftendeskriptors geändert werden kann und die Eigenschaft aus dem entsprechenden Objekt gelöscht werden kann.</td>
        </tr>
        <tr>
            <td>Enumerable</td>
            <td><code class="flyout">boolean</code></td>
            <td>"True", wenn diese Eigenschaft während der Enumeration der Eigenschaften des entsprechenden Objekts angezeigt wird.</td>
        </tr>
        <tr>
            <td>wasThrown <br/> <i>Optional</i></td>
            <td><code class="flyout">boolean</code></td>
            <td>"True", wenn das Ergebnis während der Auswertung ausgelöst wurde.</td>
        </tr>
        <tr>
            <td>isOwn <br/> <i>Optional</i></td>
            <td><code class="flyout">boolean</code></td>
            <td>"True", wenn die Eigenschaft für das Objekt gehört.</td>
        </tr>
        <tr>
            <td>msReturnValue <br/> <i>Optional</i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span><b>Experimenteller. </b></span>Microsoft: true, wenn die Eigenschaft ein Rückgabewert ist.</td>
        </tr>
        <tr>
            <td>symbol <br/> <i>Optional</i></td>
            <td><a href="#remoteobject"><code class="flyout">RemoteObject</code></a></td>
            <td>Eigenschafts Symbol Objekt, wenn die Eigenschaft vom `symbol` Typ ist. </td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="callargument"></a> CallArgument `object`

Steht für Funktionsaufruf Argument. Es sollten entweder die Remoteobjekt-ID <code>objectId</code> , der primitive <code>value</code> , der unserialisierbare primitive Wert oder keines der (für undefined) angegeben werden.

<table>
    <thead>
        <tr>
            <th>Eigenschaften</th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>value <br/> <i>Optional</i></td>
            <td><code class="flyout">any</code></td>
            <td>Primitiver Wert oder serialisierbares JavaScript-Objekt.</td>
        </tr>
        <tr>
            <td>unserializablevalue <br/> <i>Optional</i></td>
            <td><a href="#unserializablevalue"><code class="flyout">UnserializableValue</code></a></td>
            <td>Primitiver Wert, der nicht JSON-stringified sein kann.</td>
        </tr>
        <tr>
            <td>ObjectID <br/> <i>Optional</i></td>
            <td><a href="#remoteobjectid"><code class="flyout">RemoteObjectId</code></a></td>
            <td>Remote Objekthandle.</td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="executioncontextid"></a> ExecutionContextId `integer`

Die ID eines Ausführungskontexts.

</p>

---

### <a name="executioncontextdescription"></a> ExecutionContextDescription `object`

Beschreibung einer isolierten Welt.

<table>
    <thead>
        <tr>
            <th>Eigenschaften</th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>id</td>
            <td><a href="#executioncontextid"><code class="flyout">ExecutionContextId</code></a></td>
            <td>Eindeutige ID des Ausführungskontexts. Sie kann verwendet werden, um anzugeben, in welcher Ausführungskontext Skript Auswertung durchgeführt werden soll.</td>
        </tr>
        <tr>
            <td>Ursprung</td>
            <td><code class="flyout">string</code></td>
            <td>Ursprung des Ausführungskontexts.</td>
        </tr>
        <tr>
            <td>name</td>
            <td><code class="flyout">string</code></td>
            <td>Menschlicher lesbarer Name, der den angegebenen Kontext beschreibt.</td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="exceptiondetails"></a> ExceptionDetails `object`

Detaillierte Informationen zu Ausnahmen (oder Fehlern), die während der Skriptkompilierung oder-Ausführung ausgelöst wurden.

<table>
    <thead>
        <tr>
            <th>Eigenschaften</th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>Ausnahme-Nr</td>
            <td><code class="flyout">integer</code></td>
            <td>Ausnahme-ID.</td>
        </tr>
        <tr>
            <td>Text</td>
            <td><code class="flyout">string</code></td>
            <td>Ausnahmetext, der bei Verfügbarkeit zusammen mit Ausnahmeobjekt verwendet werden soll.</td>
        </tr>
        <tr>
            <td>LineNumber</td>
            <td><code class="flyout">integer</code></td>
            <td>Die Leitungsnummer des Ausnahme Speicherorts (0-basiert).</td>
        </tr>
        <tr>
            <td>ColumnNumber</td>
            <td><code class="flyout">integer</code></td>
            <td>Spaltennummer des Ausnahme Speicherorts (0-basiert).</td>
        </tr>
        <tr>
            <td>SkriptID <br/> <i>Optional</i></td>
            <td><a href="#scriptid"><code class="flyout">ScriptId</code></a></td>
            <td>Skript-ID des Ausnahme Speicherorts.</td>
        </tr>
        <tr>
            <td>URL <br/> <i>Optional</i></td>
            <td><code class="flyout">string</code></td>
            <td>Die URL des Ausnahme Speicherorts, die verwendet werden soll, wenn das Skript nicht gemeldet wurde.</td>
        </tr>
        <tr>
            <td>StackTrace <br/> <i>Optional</i></td>
            <td><a href="#stacktrace"><code class="flyout">StackTrace</code></a></td>
            <td>JavaScript-Stapelüberwachung, falls verfügbar.</td>
        </tr>
        <tr>
            <td>Ausnahme <br/> <i>Optional</i></td>
            <td><a href="#remoteobject"><code class="flyout">RemoteObject</code></a></td>
            <td>Exception-Objekt, falls verfügbar.</td>
        </tr>
        <tr>
            <td>executionContextId <br/> <i>Optional</i></td>
            <td><a href="#executioncontextid"><code class="flyout">ExecutionContextId</code></a></td>
            <td>Der Bezeichner des Kontexts, in dem die Ausnahme aufgetreten ist.</td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="timestamp"></a> Zeitstempel `integer`

Die Anzahl der Millisekunden seit Epoch.

</p>

---

### <a name="callframe"></a> CallFrame `object`

Stapel Eintrag für Runtime-Fehler und Assertionen

<table>
    <thead>
        <tr>
            <th>Eigenschaften</th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>FunctionName</td>
            <td><code class="flyout">string</code></td>
            <td>JavaScript-Funktionsname.</td>
        </tr>
        <tr>
            <td>SkriptID</td>
            <td><a href="#scriptid"><code class="flyout">ScriptId</code></a></td>
            <td>JavaScript-Skript-ID. Die Skript-Nr ist leer, wenn der Debugger nicht aktiviert ist.</td>
        </tr>
        <tr>
            <td>URL</td>
            <td><code class="flyout">string</code></td>
            <td>JavaScript-Skriptname oder-URL.</td>
        </tr>
        <tr>
            <td>LineNumber</td>
            <td><code class="flyout">integer</code></td>
            <td>JavaScript-Skript-Leitungsnummer (0-basiert).</td>
        </tr>
        <tr>
            <td>ColumnNumber</td>
            <td><code class="flyout">integer</code></td>
            <td>JavaScript-Skript-Spaltennummer (0-basiert)</td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="stacktrace"></a> StackTrace `object`

Anruf Rahmen für Assertionen oder Fehlermeldungen.

<table>
    <thead>
        <tr>
            <th>Eigenschaften</th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>description <br/> <i>Optional</i></td>
            <td><code class="flyout">string</code></td>
            <td>Zeichenfolgenbeschriftung dieser Stapelüberwachung. Bei asynchronen Ablaufverfolgungen kann dies ein Name der Funktion sein, die den asynchronen Aufruf initiiert hat.</td>
        </tr>
        <tr>
            <td>callFrames</td>
            <td><a href="#callframe"><code class="flyout">CallFrame[]</code></a></td>
            <td>JavaScript-Funktionsname.</td>
        </tr>
        <tr>
            <td>Eltern <br/> <i>Optional</i></td>
            <td><a href="#stacktrace"><code class="flyout">StackTrace</code></a></td>
            <td>Asynchrone JavaScript-Stapelüberwachung, die diesem Stapel vorausging (sofern verfügbar).</td>
        </tr>
    </tbody>
</table>
</p>

---
