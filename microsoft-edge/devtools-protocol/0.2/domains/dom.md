---
description: Referenz für die DOM-Domäne. Diese Domäne macht Dom-Lese-und Schreibvorgänge verfügbar. Jeder DOM-Knoten wird mit seinem Spiegelungs Objekt dargestellt, das über ein `id` . Damit `id` können zusätzliche Informationen auf dem Knoten abgerufen, in den JavaScript-Objektwrapper aufgelöst werden usw. Es ist wichtig, dass der Client DOM-Ereignisse nur für die Knoten empfängt, die dem Client bekannt sind. Das Back-End verfolgt die Knoten, die an den Client gesendet wurden, und sendet nie denselben Knoten zweimal. Es obliegt dem Kunden, Informationen zu den Knoten zu sammeln, die an den Client gesendet wurden.<p>Beachten Sie, dass `iframe` Besitzer Elemente die entsprechenden Dokumentelemente als untergeordnete Knoten zurückgeben.</p>
title: Dom-Domäne – devtools-Protokoll, Version 0,2
author: pelavall
ms.author: pelavall
ms.date: 8/17/2018
ms.topic: reference
ms.prod: microsoft-edge
ms.custom: seodec18
ms.openlocfilehash: 9ebe5ff709ac2981cb2359b7279c5d4e5d375426
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10567539"
---
# DOM
Diese Domäne macht Dom-Lese-und Schreibvorgänge verfügbar. Jeder DOM-Knoten wird mit seinem Spiegelungs Objekt dargestellt, das über ein `id` . Damit `id` können zusätzliche Informationen auf dem Knoten abgerufen, in den JavaScript-Objektwrapper aufgelöst werden usw. Es ist wichtig, dass der Client DOM-Ereignisse nur für die Knoten empfängt, die dem Client bekannt sind. Das Back-End verfolgt die Knoten, die an den Client gesendet wurden, und sendet nie denselben Knoten zweimal. Es obliegt dem Kunden, Informationen zu den Knoten zu sammeln, die an den Client gesendet wurden.<p>Beachten Sie, dass `iframe` Besitzer Elemente die entsprechenden Dokumentelemente als untergeordnete Knoten zurückgeben.</p>

| | |
|-|-|
| [**Methoden**](#methods) | [aktivieren](#enable), [Deaktivieren](#disable), [GetDocument](#getdocument), [highlightNode](#highlightnode), [hideHighlight](#hidehighlight), [requestChildNodes](#requestchildnodes), [GetAttributes](#getattributes), [getOuterHTML](#getouterhtml), [pushNodesByBackendIdsToFrontend](#pushnodesbybackendidstofrontend), [querySelector](#queryselector), [querySelectorAll](#queryselectorall), [requestNode](#requestnode), [resolveNode](#resolvenode), [setInspectedNode](#setinspectednode) |
| [**Ereignisse**](#events) | [setChildNodes](#setchildnodes), [attributeModified](#attributemodified), [attributeRemoved](#attributeremoved), [characterDataModified](#characterdatamodified), [childNodeInserted](#childnodeinserted), [childNodeRemoved](#childnoderemoved), [documentUpdated](#documentupdated) |
| [**Typen**](#types) | [RGBA](#rgba), [HighlightConfig](#highlightconfig), [Knoten](#nodeid)-Nr, [Knoten](#node), [BackendNodeId](#backendnodeid), [Pseudotyp](#pseudotype) |
| [**Abhängigkeiten**](#dependencies) | [Runtime](runtime.md) |
## Methoden

### Aktivieren
Aktiviert den Dom-Agent für die angegebene Seite.

</p>

---

### Deaktivieren 
Deaktiviert den Dom-Agent für die angegebene Seite. Durch das Deaktivieren des DOM werden alle zuvor gültigen nodeIds ungültig.

</p>

---

### getDocument
Gibt den Dom-Stammknoten (und optional die Unterstruktur) für den Aufrufer zurück. Durch das Aufrufen `getDocument` werden alle zuvor gültigen nodeIds ungültig.

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
            <td>Tiefe</td>
            <td><code class="flyout">integer</code></td>
            <td>Die maximale Tiefe, mit der untergeordnete Elemente abgerufen werden sollen, standardmäßig 2. Verwenden Sie-1 für die gesamte Unterstruktur.</td>
        </tr>
        <tr>
            <td>Pierce</td>
            <td><code class="flyout">boolean</code></td>
            <td>Ob iframes durchlaufen werden sollen, wenn die Teilstruktur zurückgegeben wird (Standard ist falsch).</td>
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
            <td>Stamm</td>
            <td><a href="#node"><code class="flyout">Node</code></a></td>
            <td>Resultierender Knoten</td>
        </tr>
    </tbody>
</table>
</p>

---

### highlightNode
Higlights-DOM-Knoten mit angegebener ID oder Objektwrapper. Knoten-backendNodeId oder ObjectID muss angegeben werden.

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
            <td>NodeId <br/> <i>Optional</i></td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td>Der Bezeichner des Knotens, der markiert werden soll.</td>
        </tr>
        <tr>
            <td>backendNodeId <br/> <i>Optional</i></td>
            <td><a href="#backendnodeid"><code class="flyout">BackendNodeId</code></a></td>
            <td>Der Bezeichner des zu markierenden Back-End-Knotens.</td>
        </tr>
        <tr>
            <td>ObjectID <br/> <i>Optional</i></td>
            <td><a href="runtime.md#remoteobjectid"><code class="flyout">Runtime.RemoteObjectId</code></a></td>
            <td>JavaScript-Objekt-ID des Knotens, der hervorgehoben werden soll.</td>
        </tr>
        <tr>
            <td>higlightConfig</td>
            <td><a href="#highlightconfig"><code class="flyout">HighlightConfig</code></a></td>
            <td>Deskriptor der Hervorhebungs Darstellung</td>
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
            <td>Stamm</td>
            <td><a href="#node"><code class="flyout">Node</code></a></td>
            <td>Resultierender Knoten</td>
        </tr>
    </tbody>
</table>
</p>

---

### hideHighlight
Blendet jede aktuelle DOM-Knoten Hervorhebung aus.

</p>

---

### requestChildNodes
Fordert an, dass untergeordnete Elemente des Knotens mit der angegebenen ID in Form von Ereignissen an den Anrufer zurückgegeben werden `setChildNodes` . `setChildNodes` wird für jeden Knoten ausgelöst, dessen untergeordnete Elemente zuvor nicht zurückgegeben wurden, beginnend mit dem angeforderten Knoten bis zur angegebenen Tiefe.

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
            <td>NodeId</td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td>Die ID des Knotens, von dem untergeordnete Elemente abgerufen werden sollen.</td>
        </tr>
        <tr>
            <td>Tiefe</td>
            <td><code class="flyout">integer</code></td>
            <td>Die maximale Tiefe, mit der untergeordnete Elemente abgerufen werden sollen, wird standardmäßig auf 1 festgesetzt. Verwenden Sie-1 für die gesamte Unterstruktur.</td>
        </tr>
        <tr>
            <td>Pierce</td>
            <td><code class="flyout">boolean</code></td>
            <td>Ob iframes durchlaufen werden sollen, wenn die Teilstruktur zurückgegeben wird (Standard ist falsch).</td>
        </tr>
    </tbody>
</table>
</p>

---

### GetAttributes
Gibt Attribute für den angegebenen Knoten zurück.

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
            <td>NodeId</td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td>Die ID des Knotens, für den attibutes abgerufen werden soll.</td>
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
            <td>Attribute</td>
            <td><code class="flyout">string[]</code></td>
            <td>Ein Interleaved-Array mit Namen und Werten von Knoten Attributen.</td>
        </tr>
    </tbody>
</table>
</p>

---

### getOuterHTML
Gibt das HTML-Markup des Knotens zurück.

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
            <td>NodeId <br/> <i>Optional</i></td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td>Der Bezeichner des Knotens.</td>
        </tr>
        <tr>
            <td>backendNodeId <br/> <i>Optional</i></td>
            <td><a href="#backendnodeid"><code class="flyout">BackendNodeId</code></a></td>
            <td>Der Bezeichner des Back-End-Knotens.</td>
        </tr>
        <tr>
            <td>ObjectID <br/> <i>Optional</i></td>
            <td><a href="runtime.md#remoteobjectid"><code class="flyout">Runtime.RemoteObjectId</code></a></td>
            <td>JavaScript-Objekt-ID des Knoten Wrappers.</td>
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
            <td>outerHTML</td>
            <td><code class="flyout">string</code></td>
            <td>Äußeres HTML-Markup.</td>
        </tr>
    </tbody>
</table>
</p>

---

### pushNodesByBackendIdsToFrontend
Sucht nach Knoten-IDs und löst alle übergeordneten Elemente für die angegebenen Back-End-Knoten-IDs auf

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
            <td>backendNodeIds</td>
            <td><a href="#backendnodeid"><code class="flyout">BackendNodeId[]</code></a></td>
            <td>Back-End-Knoten-IDs der zu lösenden Knoten</td>
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
            <td>nodeIds</td>
            <td><a href="#node"><code class="flyout">Node[]</code></a></td>
            <td>Knoten-IDs der aufgelösten Knoten</td>
        </tr>
    </tbody>
</table>
</p>

---

### querySelector
Wird `querySelector` für einen bestimmten Knoten ausgeführt.

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
            <td>NodeId</td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td>Die ID des Knotens, nach dem abgefragt werden soll.</td>
        </tr>
        <tr>
            <td>Auswahl</td>
            <td><code class="flyout">string</code></td>
            <td>Die Auswahlzeichenfolge.</td>
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
            <td>NodeId</td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td>Abfrageauswahl Ergebnis.</td>
        </tr>
    </tbody>
</table>
</p>

---

### querySelectorAll
Wird `querySelectorAll` für einen bestimmten Knoten ausgeführt.

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
            <td>NodeId</td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td>Die ID des Knotens, nach dem abgefragt werden soll.</td>
        </tr>
        <tr>
            <td>Auswahl</td>
            <td><code class="flyout">string</code></td>
            <td>Die Auswahlzeichenfolge.</td>
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
            <td>nodeIds</td>
            <td><a href="#nodeid"><code class="flyout">NodeId[]</code></a></td>
            <td>Abfrageauswahl Ergebnisse.</td>
        </tr>
    </tbody>
</table>
</p>

---

### requestNode
Fordert an, dass der Knoten mit der angegebenen Remoteobjekt-ID an den Anrufer gesendet wird. Alle Knoten, die den Pfad vom Knoten zum Stamm bilden, werden auch als eine Reihe von Benachrichtigungen an den Client gesendet `setChildNodes` . gibt 0 zurück, wenn das Dokument, das den angeforderten Knoten enthält, nicht zuvor vom Client angefordert wurde.

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
            <td><a href="runtime.md#remoteobjectid"><code class="flyout">Runtime.RemoteObjectId</code></a></td>
            <td>JavaScript-Objekt-ID, die in Knoten konvertiert werden soll.</td>
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
            <td>NodeId</td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td>Knoten-ID für das angegebene Objekt.</td>
        </tr>
    </tbody>
</table>
</p>

---

### resolveNode
Löst das JavaScript-Knotenobjekt für eine angegebene Knoten-oder BackendNodeId auf.

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
            <td>NodeId <br/> <i>Optional</i></td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td>Die ID des zu lösenden Knotens.</td>
        </tr>
        <tr>
            <td>backendNodeId <br/> <i>Optional</i></td>
            <td><a href="#backendnodeid"><code class="flyout">BackendNodeId</code></a></td>
            <td>Die Back-End-Knoten-ID des zu lösenden Knotens.</td>
        </tr>
        <tr>
            <td>objectGroup</td>
            <td><code class="flyout">string</code></td>
            <td>Symbolischer Gruppenname, der zum Freigeben mehrerer Objekte verwendet werden kann.</td>
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
            <td>Objekt</td>
            <td><a href="runtime.md#remoteobject"><code class="flyout">Runtime.RemoteObject</code></a></td>
            <td>JavaScript-Objektwrapper für gegebenen Knoten</td>
        </tr>
    </tbody>
</table>
</p>

---

### setInspectedNode
<span><b>Experimenteller. </b></span>Ermöglicht es Console, auf den vorherigen überprüften Knoten mit der angegebenen ID über $0-$ 4 zu verweisen.

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
            <td>NodeId</td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td>DOM-Knoten-ID, auf die mithilfe von $0-$ 4 in der Befehlszeilen-API zugegriffen werden kann.</td>
        </tr>
    </tbody>
</table>
</p>

---

## Ereignisse

### setChildNodes
Wird ausgelöst, wenn das Back-End dem Client eine fehlende DOM-Struktur bereitstellen möchte. Dies geschieht bei den meisten anrufen, die nodeIds anfordern.

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
            <td>parentID</td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td>Übergeordneter Knoten für poplate mit untergeordneten Elementen.</td>
        </tr>
        <tr>
            <td>Knoten</td>
            <td><a href="#nodeid"><code class="flyout">NodeId[]</code></a></td>
            <td>Array für untergeordnete Knoten</td>
        </tr>
    </tbody>
</table>
</p>

---

### attributeModified
Wird ausgelöst `Element` , wenn das Attribut geändert wird.

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
            <td>NodeId</td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td>Die ID des Knotens, der sich geändert hat.</td>
        </tr>
        <tr>
            <td>name</td>
            <td><code class="flyout">string</code></td>
            <td>Attribut Name.</td>
        </tr>
        <tr>
            <td>value</td>
            <td><code class="flyout">string</code></td>
            <td>Attributwert.</td>
        </tr>
    </tbody>
</table>
</p>

---

### attributeRemoved
Wird ausgelöst `Element` , wenn das Attribut entfernt wurde.

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
            <td>NodeId</td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td>Die ID des Knotens, der sich geändert hat.</td>
        </tr>
        <tr>
            <td>name</td>
            <td><code class="flyout">string</code></td>
            <td>Attribut Name.</td>
        </tr>
    </tbody>
</table>
</p>

---

### characterDataModified
Mirrors `DOMCharacterDataModified` -Ereignis.

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
            <td>NodeId</td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td>Die ID des Knotens, der sich geändert hat.</td>
        </tr>
        <tr>
            <td>charcterData</td>
            <td><code class="flyout">string</code></td>
            <td>Neuer Textwert.</td>
        </tr>
    </tbody>
</table>
</p>

---

### childNodeInserted
Mirrors `DOMNodeInserted` -Ereignis.

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
            <td>parentNodeId</td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td>Die ID des Knotens, der sich geändert hat.</td>
        </tr>
        <tr>
            <td>previousNodeId</td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td>Die ID des vorherigen gleichgeordneten Elements des eingefügten Knotens.</td>
        </tr>
        <tr>
            <td>Knoten</td>
            <td><a href="#node"><code class="flyout">Node</code></a></td>
            <td>Eingefügte Knoten Daten.</td>
        </tr>
    </tbody>
</table>
</p>

---

### childNodeRemoved
Mirrors `DOMNodeRemoved` -Ereignis.

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
            <td>parentNodeId</td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td>Die ID des Knotens, der sich geändert hat.</td>
        </tr>
        <tr>
            <td>NodeId</td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td>Die ID des Knotens, der entfernt wurde.</td>
        </tr>
    </tbody>
</table>
</p>

---

### documentUpdated
Wird ausgelöst `Document` , wenn die vollständige Aktualisierung durchgeführt wurde. Knoten-IDs sind nicht mehr gültig.

</p>

---

## Typen

### <a name="rgba"></a> RGBA `object`

Eine Struktur mit einer RGBA-Farbe.

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
            <td>r</td>
            <td><code class="flyout">integer</code></td>
            <td>Die rote Komponente im Bereich [0-255].</td>
        </tr>
        <tr>
            <td>g</td>
            <td><code class="flyout">integer</code></td>
            <td>Die grüne Komponente im Bereich [0-255].</td>
        </tr>
        <tr>
            <td>b</td>
            <td><code class="flyout">integer</code></td>
            <td>Die blaue Komponente im Bereich [0-255].</td>
        </tr>
        <tr>
            <td>a <br/> <i>Optional</i></td>
            <td><code class="flyout">number</code></td>
            <td>Die Alpha-Komponente im Bereich [0-1]. Der Standardwert ist 1.</td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="highlightconfig"></a> HighlightConfig `object`

Konfigurationsdaten zum Markieren von Seitenelementen.

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
            <td>contentColor <br/> <i>Optional</i></td>
            <td><a href="#rgba"><code class="flyout">RGBA</code></a></td>
            <td>Das Feld "Inhalt" hebt die Füllfarbe auf. Standard ist transparent.</td>
        </tr>
        <tr>
            <td>paddingColor <br/> <i>Optional</i></td>
            <td><a href="#rgba"><code class="flyout">RGBA</code></a></td>
            <td>Die Füllfarbe des Füllbereichs wird markiert. Standard ist transparent.</td>
        </tr>
        <tr>
            <td>BorderColor <br/> <i>Optional</i></td>
            <td><a href="#rgba"><code class="flyout">RGBA</code></a></td>
            <td>Die Rahmen Hervorhebungsfarbe. Standard ist transparent.</td>
        </tr>
        <tr>
            <td>marginColor <br/> <i>Optional</i></td>
            <td><a href="#rgba"><code class="flyout">RGBA</code></a></td>
            <td>Die Füllfarbe des Rands. Standard ist transparent.</td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="nodeid"></a> NodeId `integer`

Eindeutige DOM-Knoten-ID

</p>

---

### <a name="node"></a> Knoten `object`

Mirror-Objekt, das die eigentlichen DOM-Knoten darstellt.

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
            <td>NodeId</td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td>Knoten Bezeichner, der für den Verweis auf diesen Knoten verwendet wird. Das Back-End löst DOM-Ereignisse für Knoten aus, die über eine Knoten-Nr verfügen, die dem Client bekannt ist.</td>
        </tr>
        <tr>
            <td>parentID <br/> <i>Optional</i></td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td>Knoten Bezeichner des übergeordneten Knotens (sofern vorhanden).</td>
        </tr>
        <tr>
            <td>backendNodeId</td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td>Back-End-Knoten Bezeichner des Knotens. BackendNodeIds-Verweisknoten, die dem Client bekannt sein können, jedoch keine DOM-Ereignisse über diesen Knoten pushen.</td>
        </tr>
        <tr>
            <td>NodeType</td>
            <td><code class="flyout">integer</code></td>
            <td>`Node`-NodeType.</td>
        </tr>
        <tr>
            <td>nodeName</td>
            <td><code class="flyout">string</code></td>
            <td>`Node`Knoten-Nr.</td>
        </tr>
        <tr>
            <td>localName</td>
            <td><code class="flyout">string</code></td>
            <td>`Node`es LocalName</td>
        </tr>
        <tr>
            <td>nodeValue</td>
            <td><code class="flyout">string</code></td>
            <td>`Node`es nodeValue</td>
        </tr>
        <tr>
            <td>childNodeCount <br/> <i>Optional</i></td>
            <td><code class="flyout">integer</code></td>
            <td>Untergeordnete Anzahl für `Container` Knoten.</td>
        </tr>
        <tr>
            <td>Kinder <br/> <i>Optional</i></td>
            <td><a href="#node"><code class="flyout">Node[]</code></a></td>
            <td>Untergeordnete Knoten dieses Knotens, wenn Sie mit untergeordneten Elementen angefordert werden.</td>
        </tr>
        <tr>
            <td>Attribute <br/> <i>Optional</i></td>
            <td><code class="flyout">string[]</code></td>
            <td>Attribute von `Element` Knoten in Form einer flachen Matrix ' [name1, value1, name2, Value2]</td>
        </tr>
        <tr>
            <td>documentURL <br/> <i>Optional</i></td>
            <td><code class="flyout">string</code></td>
            <td>Dokument-URL, auf die die `Document` Knoten verweisen.</td>
        </tr>
        <tr>
            <td>baseURL <br/> <i>Optional</i></td>
            <td><code class="flyout">string</code></td>
            <td>Dokument-URL, die `Document` Knoten für die URL-Vervollständigung verwenden</td>
        </tr>
        <tr>
            <td>PublicId <br/> <i>Optional</i></td>
            <td><code class="flyout">string</code></td>
            <td>`DocumentType` Public-Nr des Knotens.</td>
        </tr>
        <tr>
            <td>SystemId <br/> <i>Optional</i></td>
            <td><code class="flyout">string</code></td>
            <td>`DocumentType` Die System-Nr des Knotens.</td>
        </tr>
        <tr>
            <td>InternalSubset <br/> <i>Optional</i></td>
            <td><code class="flyout">string</code></td>
            <td>`DocumentType` InternalSubset des Knotens.</td>
        </tr>
        <tr>
            <td>xmlversion <br/> <i>Optional</i></td>
            <td><code class="flyout">string</code></td>
            <td>`Document` XML-Version des Knotens im Fall von XML-Dokumenten</td>
        </tr>
        <tr>
            <td>name <br/> <i>Optional</i></td>
            <td><code class="flyout">string</code></td>
            <td>`Attr` Der Name des Knotens.</td>
        </tr>
        <tr>
            <td>value <br/> <i>Optional</i></td>
            <td><code class="flyout">string</code></td>
            <td>`Attr` Der Wert des Knotens.</td>
        </tr>
        <tr>
            <td>Frame-Nr <br/> <i>Optional</i></td>
            <td><a href="page.md#frameid"><code class="flyout">Page.FrameId</code></a></td>
            <td>Frame-ID für die Elemente des Frame-Besitzers.</td>
        </tr>
        <tr>
            <td>contentDocument <br/> <i>Optional</i></td>
            <td><a href="#node"><code class="flyout">Node</code></a></td>
            <td>Inhaltsdokument für Elemente des Frame-Besitzers.</td>
        </tr>
        <tr>
            <td>isSVG <br/> <i>Optional</i></td>
            <td><code class="flyout">boolean</code></td>
            <td>"True", wenn der Knoten SVG ist.</td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="backendnodeid"></a> BackendNodeId `integer`

Eindeutiger DOM-Knoten Bezeichner, der zum Verweisen auf einen Knoten verwendet wird, der möglicherweise nicht in das Front-End verschoben wurde.

</p>

---

### <a name="pseudotype"></a> Pseudotyp `string`

Pseudo Elementtyp.

##### Zulässige Werte
erste Zeile, erster Buchstabe, vorher, nachher, Auswahl
</p>

---

## Abhängigkeiten

[Runtime](runtime.md)