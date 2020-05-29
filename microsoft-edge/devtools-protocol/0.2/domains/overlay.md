---
description: Referenz für die Overlay-Domäne. Overlay-Domäne macht visuelle Elemente und Interaktion zwischen Knotenauswahl verfügbar
title: Overlay-Domäne – devtools-Protokoll Version 0,2
author: pelavall
ms.author: pelavall
ms.date: 8/17/2018
ms.topic: reference
ms.prod: microsoft-edge
ms.openlocfilehash: a7657e2abc99e45894f19f6557f12f78f8ee9c75
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10567532"
---
# Überlagerung
Overlay-Domäne macht visuelle Elemente und Interaktion zwischen Knotenauswahl verfügbar

| | |
|-|-|
| [**Methoden**](#methods) | [aktivieren](#enable), [Deaktivieren](#disable), [setInspectMode](#setinspectmode) |
| [**Ereignisse**](#events) | [inspectNodeRequested](#inspectnoderequested), [nodeHighlightRequested](#nodehighlightrequested) |
| [**Abhängigkeiten**](#dependencies) | [DOM](dom.md) |
## Methoden

### Aktivieren
Ermöglicht das Melden von <code>nodeHighlightRequested</code> und <code>inspectElementRequested</code> Ereignissen

</p>

---

### Deaktivieren 
Deaktiviert die Berichterstattung über Overlay-Domänenereignisse

</p>

---

### setInspectMode
Legt den Elementauswahl Modus für den Client fest.

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
            <td>mode</td>
            <td><code class="flyout">string</code></td>
            <td>Der Prüfungsmodus.  Gültige Werte sind "searchForNode" und "None".</td>
        </tr>
        <tr>
            <td>highlightConfig <br/> <i>Optional</i></td>
            <td><a href="dom.md#highlightconfig"><code class="flyout">DOM.HighlightConfig</code></a></td>
            <td>Die zu verwendende Hervorhebungs Konfiguration während der Überprüfung</td>
        </tr>
    </tbody>
</table>
</p>

---

## Ereignisse

### inspectNodeRequested
Benachrichtigt den Client, dass der Benutzer gebeten hat, einen bestimmten Knoten zu überprüfen

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
            <td>backendNodeId</td>
            <td><a href="dom.md#backendnodeid"><code class="flyout">DOM.BackendNodeId</code></a></td>
            <td>Die Back-End-Knoten-ID des angeforderten Knotens</td>
        </tr>
    </tbody>
</table>
</p>

---

### nodeHighlightRequested
Gibt an, dass der Benutzer über den Knoten schwebt und den Knoten möglicherweise überprüft.

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
            <td><a href="dom.md#nodeid"><code class="flyout">DOM.NodeId</code></a></td>
            <td>Die Knoten-ID des betrachteten Knotens</td>
        </tr>
    </tbody>
</table>
</p>

---

## Abhängigkeiten

[DOM](dom.md)