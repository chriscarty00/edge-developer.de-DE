---
description: Referenz für die Overlay-Domäne. Overlay-Domäne macht visuelle Elemente und Interaktion zwischen Knotenauswahl verfügbar
title: Overlay-Domäne – devtools-Protokoll Version 0,2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: reference
ms.prod: microsoft-edge
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: dcf5feff9983aa2e9e61ac0569938988812165f8
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233634"
---
# Überlagerung

Overlay-Domäne macht visuelle Elemente und Interaktion zwischen Knotenauswahl verfügbar

| | |
|-|-|
| [**Methoden**](#methods) | [aktivieren](#enable), [Deaktivieren](#disable), [setInspectMode](#setinspectmode) |
| [**Veranstaltungen**](#events) | [inspectNodeRequested](#inspectnoderequested), [nodeHighlightRequested](#nodehighlightrequested) |
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

## Veranstaltungen

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
