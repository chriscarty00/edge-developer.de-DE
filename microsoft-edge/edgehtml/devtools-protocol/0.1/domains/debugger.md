---
description: DevTools Protocol Version 0,1 (EdgeHTML) Reference für die Debugger-Domäne. Die Debugger-Domäne macht JavaScript-Debugfunktionen verfügbar. Sie ermöglicht das Festlegen und Entfernen von Haltepunkten, durchlaufen der Ausführung, Durchsuchen von Stapelablaufverfolgungen usw.
title: Debugger-Domäne – devtools-Protokoll Version 0,1 (EdgeHTML)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: reference
ms.prod: microsoft-edge
ms.custom: seodec18
ms.date: 12/16/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 5160e6e69ec76f8c584f1bdb969464d805c7afa7
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11234026"
---
# Debugger-Domäne – devtools-Protokoll Version 0,1 (EdgeHTML)  
  
Die Debugger-Domäne macht JavaScript-Debugfunktionen verfügbar. Sie ermöglicht das Festlegen und Entfernen von Haltepunkten, durchlaufen der Ausführung, Durchsuchen von Stapelablaufverfolgungen usw.

| | |
|-|-|
| [**Methoden**](#methods) | [aktivieren](#enable), [Deaktivieren](#disable), [getPossibleBreakpoints](#getpossiblebreakpoints), [setBreakpointsActive](#setbreakpointsactive), [setBreakpointByUrl](#setbreakpointbyurl), [setbreak Point](#setbreakpoint), [removeBreakpoint](#removebreakpoint), [Zustellung](#stepover), [stepInto](#stepinto), [aussteigen](#stepout), [Anhalten](#pause), [fortsetzen](#resume), [getScriptSource](#getscriptsource), [setPauseOnExceptions](#setpauseonexceptions), [evaluateOnCallFrame](#evaluateoncallframe), [setvariablevalue](#setvariablevalue), [setBlackboxPatterns](#setblackboxpatterns), [msSetDebuggerPropertyValue](#mssetdebuggerpropertyvalue) |
| [**Veranstaltungen**](#events) | [scriptParsed](#scriptparsed), [breakpointResolved](#breakpointresolved), [angehalten](#paused), [fortgesetzt](#resumed) |
| [**Typen**](#types) | [Breakpoint](#breakpointid), [CallFrameId](#callframeid), [Location](#location), [BreakLocation](#breaklocation), [CallFrame](#callframe), [Scope](#scope) |
| [**Abhängigkeiten**](#dependencies) | [Laufzeit](runtime.md) |
## Methoden

### Aktivieren
Aktiviert den Debugger für die angegebene Seite. Clients sollten nicht davon ausgehen, dass das Debuggen aktiviert wurde, bis das Ergebnis für diesen Befehl empfangen wurde.


---

### Deaktivieren 
Deaktiviert den Debugger für die angegebene Seite.


---

### getPossibleBreakpoints
Gibt mögliche Speicherorte für Breakpoint zurück. die Skript-Nr in Start-und Endbereich-Speicherorten sollte identisch sein.

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
            <td>start</td>
            <td><a href="#location"><code class="flyout">Location</code></a></td>
            <td>Anfang des Bereichs, in dem mögliche Haltepunkte in der Position durchsucht werden.</td>
        </tr>
        <tr>
            <td>Aufhören</td>
            <td><a href="#location"><code class="flyout">Location</code></a></td>
            <td>Ende des Bereichs, in dem mögliche Haltepunkte in (ohne) durchsucht werden. Wenn keine Angabe erfolgt, wird das Ende von Skripten als Bereichsende verwendet.</td>
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
            <td>Speicherorte</td>
            <td><a href="#breaklocation"><code class="flyout">BreakLocation</code></a></td>
            <td>Liste der möglichen Haltepunkt Positionen</td>
        </tr>
    </tbody>
</table>

---

### setBreakpointsActive
Aktiviert/deaktiviert alle Haltepunkte auf der Seite.

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
            <td>active</td>
            <td><code class="flyout">boolean</code></td>
            <td>Neuer Wert für Haltepunkte für aktiven Zustand.</td>
        </tr>
    </tbody>
</table>

---

### setBreakpointByUrl
Legt den JavaScript-Haltepunkt an einer bestimmten Position fest, die entweder durch URL oder URL Regex angegeben wird. Sobald dieser Befehl ausgegeben wurde, haben alle vorhandenen analysierten Skripts Haltepunkte aufgelöst und werden in der Eigenschaft zurückgegeben <code>locations</code> . Eine weitere übereinstimmende Skript Analyse führt dazu, dass nachfolgende <code>breakpointResolved</code> Ereignisse ausgegeben werden. Dieser logische Haltepunkt überlebt das erneute Laden von Seiten.

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
            <td>LineNumber</td>
            <td><code class="flyout">integer</code></td>
            <td>Die Nummer der Zeile, auf die der Haltepunkt gesetzt werden soll.</td>
        </tr>
        <tr>
            <td>URL <br/> <i>Optional</i></td>
            <td><code class="flyout">string</code></td>
            <td>Die URL der Ressourcen, auf die der Haltepunkt gesetzt werden soll.</td>
        </tr>
        <tr>
            <td>urlRegex <br/> <i>Optional</i></td>
            <td><code class="flyout">string</code></td>
            <td>Regex-Muster für die URLs der Ressourcen zum Festlegen von Haltepunkten. Entweder <code>url</code> oder <code>urlRegex</code> muss angegeben werden.</td>
        </tr>
        <tr>
            <td>ColumnNumber <br/> <i>Optional</i></td>
            <td><code class="flyout">integer</code></td>
            <td>Offset in der Zeile, an der der Haltepunkt gesetzt werden soll.</td>
        </tr>
        <tr>
            <td>Bedingung <br/> <i>Optional</i></td>
            <td><code class="flyout">string</code></td>
            <td>Ausdruck, der als Haltepunktbedingung verwendet werden soll. Wenn angegeben, wird der Debugger nur an dem Haltepunkt angehalten, wenn dieser Ausdruck wahr ausgewertet wird.</td>
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
            <td>Haltepunkt-Nr</td>
            <td><a href="#breakpointid"><code class="flyout">BreakpointId</code></a></td>
            <td>Die ID des erstellten Haltepunkts für Weitere Verweise.</td>
        </tr>
        <tr>
            <td>Speicherorte</td>
            <td><a href="#location"><code class="flyout">Location[]</code></a></td>
            <td>Liste der Speicherorte, in die dieser Haltepunkt nach dem Hinzufügen aufgelöst wurde.</td>
        </tr>
    </tbody>
</table>

---

### setbreaker
Legt den JavaScript-Haltepunkt an einer bestimmten Position fest.

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
            <td>Lage</td>
            <td><a href="#location"><code class="flyout">Location</code></a></td>
            <td>Die Position, an der der Haltepunkt gesetzt werden soll.</td>
        </tr>
        <tr>
            <td>Bedingung <br/> <i>Optional</i></td>
            <td><code class="flyout">string</code></td>
            <td>Ausdruck, der als Haltepunktbedingung verwendet werden soll. Wenn angegeben, wird der Debugger nur an dem Haltepunkt angehalten, wenn dieser Ausdruck wahr ausgewertet wird.</td>
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
            <td>Haltepunkt-Nr</td>
            <td><a href="#breakpointid"><code class="flyout">BreakpointId</code></a></td>
            <td>Die ID des erstellten Haltepunkts für Weitere Verweise.</td>
        </tr>
        <tr>
            <td>actualLocation</td>
            <td><a href="#location"><code class="flyout">Location</code></a></td>
            <td>Ort, in den dieser Haltepunkt aufgelöst wurde.</td>
        </tr>
    </tbody>
</table>

---

### removeBreakpoint
Entfernt den JavaScript-Haltepunkt.

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
            <td>Haltepunkt-Nr</td>
            <td><a href="#breakpointid"><code class="flyout">BreakpointId</code></a></td>
            <td></td>
        </tr>
    </tbody>
</table>

---

### Zustellung
Schritte über die Anweisung.


---

### stepInto
Tritt in den Funktionsaufruf ein.


---

### stepOut
Schritte aus dem Funktionsaufruf.


---

### pause
Stoppt bei der nächsten JavaScript-Anweisung.


---

### resume
Setzt die JavaScript-Ausführung fort.


---

### getScriptSource
Gibt die Quelle für das Skript mit der angegebenen ID zurück.

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
            <td>SkriptID</td>
            <td><a href="runtime.md#scriptid"><code class="flyout">Runtime.ScriptId</code></a></td>
            <td>Die ID des Skripts, für das die Quelle abgerufen werden soll.</td>
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
            <td>scriptSource</td>
            <td><code class="flyout">string</code></td>
            <td>Skript Quelle.</td>
        </tr>
    </tbody>
</table>

---

### setPauseOnExceptions
Definiert die Pause für den Ausnahmezustand. Kann so eingestellt werden, dass bei allen Ausnahmen, nicht abgefangene Ausnahmen oder ohne Ausnahmen, beendet wird. Anfängliche Pause für Ausnahmen Zustand ist <code>none</code> .

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
            <td>Zustand</td>
            <td><code class="flyout">string</code> <br/> <i>Zulässige Werte: keine, nicht abgefangen, alle</i></td>
            <td>Pausieren im Ausnahmen Modus.</td>
        </tr>
    </tbody>
</table>

---

### evaluateOnCallFrame
Wertet den Ausdruck für einen angegebenen Aufruf Frame aus.

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
            <td>callFrameId</td>
            <td><a href="#callframeid"><code class="flyout">CallFrameId</code></a></td>
            <td>Die Frame-ID des Anrufs für die Auswertung.</td>
        </tr>
        <tr>
            <td>Ausdruck</td>
            <td><code class="flyout">string</code></td>
            <td>Ausdruck, der ausgewertet werden soll.</td>
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
            <td><a href="runtime.md#remoteobject"><code class="flyout">Runtime.RemoteObject</code></a></td>
            <td>Objektwrapper für das Auswertungsergebnis</td>
        </tr>
    </tbody>
</table>

---

### setvariablevalue
Ändert den Wert der Variablen in einem callframe. Objektbasierte Bereiche werden nicht unterstützt und müssen manuell mutiert werden.

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
            <td>scopeNumber</td>
            <td><code class="flyout">integer</code></td>
            <td>0-basierte Anzahl des Bereichs, wie er in der Bereichskette aufgeführt ist. Nur "local"-, "Closure"-und "Catch"-Bereichstypen sind zulässig. Andere Bereiche können manuell manipuliert werden.</td>
        </tr>
        <tr>
            <td>variableName</td>
            <td><code class="flyout">string</code></td>
            <td>Name der Variablen.</td>
        </tr>
        <tr>
            <td>NewValue</td>
            <td><a href="runtime.md#callargument"><code class="flyout">Runtime.CallArgument</code></a></td>
            <td>Neuer Variablenwert.</td>
        </tr>
        <tr>
            <td>callFrameId</td>
            <td><a href="#callframeid"><code class="flyout">CallFrameId</code></a></td>
            <td>Die ID der callframe, die Variable enthält.</td>
        </tr>
    </tbody>
</table>

---

### setBlackboxPatterns
<span><b>Experimenteller. </b></span>Ersetzen Sie frühere Blackbox-Muster durch übergebene. Zwingt das Back-End, die Schritt-oder Pausierung in Skripts zu überspringen, wobei die URL einem der Muster entspricht. Der Debugger versucht, das blackboxed-Skript zu verlassen, indem es mehrere Male "Step in" ausführt und schließlich auf "Step out" zurückgegriffen wird, wenn es nicht erfolgreich ist.

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
            <td>Muster</td>
            <td><code class="flyout">string[]</code></td>
            <td>Array von Regexps, die verwendet werden, um die Skript-URL für den Blackbox-Zustand zu überprüfen.</td>
        </tr>
    </tbody>
</table>

---

### msSetDebuggerPropertyValue
<span><b>Experimenteller. </b></span>Microsoft: legt die angegebene Debugger-Eigenschaft auf den angegebenen Wert fest.

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
            <td>debuggerPropertyId</td>
            <td><code class="flyout">string</code></td>
            <td>Microsoft: die Eigenschafts-ID (also msDebuggerPropertyId), die Sie festlegen möchten.</td>
        </tr>
        <tr>
            <td>NewValue</td>
            <td><code class="flyout">string</code></td>
            <td></td>
        </tr>
    </tbody>
</table>

---

## Veranstaltungen

### scriptParsed
Wird ausgelöst, wenn das Skript analysiert wird. Dieses Ereignis wird beim Aktivieren des Debuggers auch für alle bekannten und nicht gesammelten Skripts ausgelöst.

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
            <td>SkriptID</td>
            <td><a href="runtime.md#scriptid"><code class="flyout">Runtime.ScriptId</code></a></td>
            <td>Der Bezeichner des analysierten Skripts.</td>
        </tr>
        <tr>
            <td>URL</td>
            <td><code class="flyout">string</code></td>
            <td>Die URL oder der Name des analysierten Skripts (sofern vorhanden).</td>
        </tr>
        <tr>
            <td>startLine</td>
            <td><code class="flyout">integer</code></td>
            <td>Der Offset des Skripts innerhalb der Ressource mit der angegebenen URL (für Skripttags).</td>
        </tr>
        <tr>
            <td>startColumn</td>
            <td><code class="flyout">integer</code></td>
            <td>Spaltenoffset des Skripts innerhalb der Ressource mit der angegebenen URL.</td>
        </tr>
        <tr>
            <td>endLine</td>
            <td><code class="flyout">integer</code></td>
            <td>Letzte Zeile des Skripts.</td>
        </tr>
        <tr>
            <td>endColumn</td>
            <td><code class="flyout">integer</code></td>
            <td>Die Länge der letzten Zeile des Skripts.</td>
        </tr>
        <tr>
            <td>executionContextId</td>
            <td><a href="runtime.md#executioncontextid"><code class="flyout">Runtime.ExecutionContextId</code></a></td>
            <td>Gibt den Skript Erstellungs Kontext an.</td>
        </tr>
        <tr>
            <td>sourceMapURL <br/> <i>Optional</i></td>
            <td><code class="flyout">string</code></td>
            <td>Die URL der Quell Karte, die dem Skript zugeordnet ist (sofern vorhanden).</td>
        </tr>
        <tr>
            <td>Länge <br/> <i>Optional</i></td>
            <td><code class="flyout">integer</code></td>
            <td><span><b>Experimenteller. </b></span>Diese Skript Länge.</td>
        </tr>
        <tr>
            <td>msParentId <br/> <i>Optional</i></td>
            <td><code class="flyout">string</code></td>
            <td><span><b>Experimenteller. </b></span>Hierbei handelt es sich um die übergeordnete Dokument-ID.</td>
        </tr>
        <tr>
            <td>msMimeType <br/> <i>Optional</i></td>
            <td><code class="flyout">string</code></td>
            <td><span><b>Experimenteller. </b></span>Dies ist der MIME-Typ.</td>
        </tr>
        <tr>
            <td>msIsDynamicCode <br/> <i>Optional</i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span><b>Experimenteller. </b></span>Gibt an, ob es sich um dynamischen Code handelt.</td>
        </tr>
        <tr>
            <td>msLongDocumentId <br/> <i>Optional</i></td>
            <td><code class="flyout">integer</code></td>
            <td><span><b>Experimenteller. </b></span>Dies ist die lange Dokument-ID.</td>
        </tr>
    </tbody>
</table>

---

### breakpointResolved
Wird ausgelöst, wenn der Haltepunkt zu einem tatsächlichen Skript und Speicherort aufgelöst wird.

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
            <td>Haltepunkt-Nr</td>
            <td><a href="#breakpointid"><code class="flyout">BreakpointId</code></a></td>
            <td>Eindeutiger Haltepunktbezeichner.</td>
        </tr>
        <tr>
            <td>Lage</td>
            <td><a href="#location"><code class="flyout">Location</code></a></td>
            <td>Tatsächliche Haltepunktposition.</td>
        </tr>
        <tr>
            <td>msLength <br/> <i>Optional</i></td>
            <td><code class="flyout">integer</code></td>
            <td><span><b>Experimenteller. </b></span>Microsoft: Länge des Codes (also Anzahl der Zeichen) an der Haltepunktposition.</td>
        </tr>
    </tbody>
</table>

---

### angehalten
Wird ausgelöst, wenn die Debugger für einen Haltepunkt oder eine Ausnahme unterbrechen.

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
            <td>callFrames</td>
            <td><a href="#callframe"><code class="flyout">CallFrame[]</code></a></td>
            <td>Aufrufliste der Debugger wurde angehalten.</td>
        </tr>
        <tr>
            <td>Grund</td>
            <td><code class="flyout">string</code> <br/> <i>Zulässige Werte: Haltepunkt, Schritt, Ausnahme, sonstige</i></td>
            <td>Grund für Pause.</td>
        </tr>
        <tr>
            <td>data <br/> <i>Optional</i></td>
            <td><code class="flyout">object</code></td>
            <td>Objekt, das Bruch spezifische Zusatzeigenschaften enthält.</td>
        </tr>
        <tr>
            <td>hitBreakpoints <br/> <i>Optional</i></td>
            <td><code class="flyout">string[]</code></td>
            <td>Treffer Haltepunkte-IDs</td>
        </tr>
    </tbody>
</table>

---

### wieder
Wird ausgelöst, wenn der Debugger die Ausführung fortsetzt.


---

## Typen

### <a name="breakpointid"></a> Haltepunkt-Nr `string`

Haltepunkt-ID.


---

### <a name="callframeid"></a> CallFrameId `string`

Anruf Rahmen-ID.


---

### <a name="location"></a> Pfad `object`

Speicherort im Quellcode.

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
            <td>SkriptID</td>
            <td><a href="runtime.md#scriptid"><code class="flyout">Runtime.ScriptId</code></a></td>
            <td>Skriptbezeichner, wie in <code>Debugger.scriptParsed</code> .</td>
        </tr>
        <tr>
            <td>LineNumber</td>
            <td><code class="flyout">integer</code></td>
            <td>Die Nummer der Zeile im Skript (0-basiert).</td>
        </tr>
        <tr>
            <td>ColumnNumber <br/> <i>Optional</i></td>
            <td><code class="flyout">integer</code></td>
            <td>Spaltennummer im Skript (0-basiert)</td>
        </tr>
        <tr>
            <td>msLength</td>
            <td><code class="flyout">integer</code></td>
            <td>Microsoft: Länge des Codes (also Anzahl der Zeichen) an diesem Aufruf Frame.</td>
        </tr>
    </tbody>
</table>

---

### <a name="breaklocation"></a> BreakLocation `object`

Position im Quellcode unterbrechen.

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
            <td>SkriptID</td>
            <td><a href="runtime.md#scriptid"><code class="flyout">Runtime.ScriptId</code></a></td>
            <td>Skriptbezeichner, wie in <code>Debugger.scriptParsed</code> .</td>
        </tr>
        <tr>
            <td>LineNumber</td>
            <td><code class="flyout">integer</code></td>
            <td>Die Nummer der Zeile im Skript (0-basiert).</td>
        </tr>
        <tr>
            <td>ColumnNumber <br/> <i>Optional</i></td>
            <td><code class="flyout">integer</code></td>
            <td>Spaltennummer im Skript (0-basiert)</td>
        </tr>
        <tr>
            <td>msLength</td>
            <td><code class="flyout">integer</code></td>
            <td>Microsoft: Länge des Codes (also Anzahl der Zeichen) an diesem Aufruf Frame.</td>
        </tr>
        <tr>
            <td>Typ <br/> <i>Optional</i></td>
            <td><code class="flyout">string</code></td>
            <td>Zulässige Werte: debuggerStatement, Aufruf, zurück.</td>
        </tr>
    </tbody>
</table>

---

### <a name="callframe"></a> CallFrame `object`

JavaScript-Anruf Rahmen. Array von Anruf Frames aus der Aufrufliste.

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
            <td>callFrameId</td>
            <td><a href="#callframeid"><code class="flyout">CallFrameId</code></a></td>
            <td>Anruf Rahmen-ID. Dieser Bezeichner ist nur gültig, wenn der Debugger angehalten wurde.</td>
        </tr>
        <tr>
            <td>FunctionName</td>
            <td><code class="flyout">string</code></td>
            <td>Der Name der JavaScript-Funktion, die in diesem Aufruf Frame aufgerufen wird.</td>
        </tr>
        <tr>
            <td>functionLocation <br/> <i>Optional</i></td>
            <td><a href="#location"><code class="flyout">Location</code></a></td>
            <td><span><b>Experimenteller. </b></span>Speicherort im Quellcode.</td>
        </tr>
        <tr>
            <td>Lage</td>
            <td><a href="#location"><code class="flyout">Location</code></a></td>
            <td>Speicherort im Quellcode.</td>
        </tr>
        <tr>
            <td>URL</td>
            <td><code class="flyout">string</code></td>
            <td>JavaScript-Skriptname oder-URL.</td>
        </tr>
        <tr>
            <td>scopeChain</td>
            <td><a href="#scope"><code class="flyout">Scope[]</code></a></td>
            <td>Bereichskette für diesen Aufruf Frame.</td>
        </tr>
        <tr>
            <td>Diese</td>
            <td><a href="runtime.md#remoteobject"><code class="flyout">Runtime.RemoteObject</code></a></td>
            <td><code>this</code> das Objekt für diesen Anruf Frame.</td>
        </tr>
        <tr>
            <td>returnValue <br/> <i>Optional</i></td>
            <td><a href="runtime.md#remoteobject"><code class="flyout">Runtime.RemoteObject</code></a></td>
            <td>Der Wert, der zurückgegeben wird, wenn sich die Funktion am Rückgabe Punkt befindet.</td>
        </tr>
    </tbody>
</table>

---

### <a name="scope"></a> Bereich `object`

Beschreibung des Bereichs

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
            <td><code class="flyout">string</code> <br/> <i>Zulässige Werte: Global, local, with, Closure, catch, Block, Script, eval, Module</i></td>
            <td>Scope-Typ.</td>
        </tr>
        <tr>
            <td>Objekt</td>
            <td><a href="runtime.md#remoteobject"><code class="flyout">Runtime.RemoteObject</code></a></td>
            <td>Das Objekt, das den Bereich darstellt. Für <code>global</code> und <code>with</code> Bereiche stellt es das eigentliche Objekt dar; für die restlichen Bereiche ist es ein künstliches Transienten Objekt, das Bereichsvariablen als Eigenschaften auflistet.</td>
        </tr>
        <tr>
            <td>name <br/> <i>Optional</i></td>
            <td><code class="flyout">string</code></td>
            <td></td>
        </tr>
        <tr>
            <td>StartLocation <br/> <i>Optional</i></td>
            <td><a href="#location"><code class="flyout">Location</code></a></td>
            <td>Speicherort im Quellcode, in dem der Bereich beginnt</td>
        </tr>
        <tr>
            <td>endLocation <br/> <i>Optional</i></td>
            <td><a href="#location"><code class="flyout">Location</code></a></td>
            <td>Speicherort im Quellcode, in dem der Bereich endet</td>
        </tr>
    </tbody>
</table>

---

## Abhängigkeiten

[Laufzeit](runtime.md)
