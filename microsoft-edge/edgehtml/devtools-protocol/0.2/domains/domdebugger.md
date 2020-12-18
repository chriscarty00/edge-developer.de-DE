---
description: Referenz für die DOMDebugger-Domäne. Dom-Debuggen ermöglicht das Festlegen von Haltepunkten für bestimmte Dom-Vorgänge und-Ereignisse. Die JavaScript-Ausführung wird bei diesen Vorgängen so beendet, als ob ein regulärer Haltepunkt festgesetzt wurde.
title: DOMDebugger Domain-devtools Protocol Version 0,2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: reference
ms.prod: microsoft-edge
ms.date: 12/02/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: d97a9a8f2d0e49166f5f081e8bb0c0d5d3cdd93f
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233636"
---
# DOMDebugger

Dom-Debuggen ermöglicht das Festlegen von Haltepunkten für bestimmte Dom-Vorgänge und-Ereignisse. Die JavaScript-Ausführung wird bei diesen Vorgängen so beendet, als ob ein regulärer Haltepunkt festgesetzt wurde.

| | |
|-|-|
| [**Methoden**](#methods) | [setInstrumentationBreakpoint](#setinstrumentationbreakpoint), [removeInstrumentationBreakpoint](#removeinstrumentationbreakpoint) |
## Methoden

### setInstrumentationBreakpoint
<span><b>Experimenteller. </b></span>Legt einen Haltepunkt für ein bestimmtes systemeigenes Ereignis fest.

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
            <td>EventName</td>
            <td><code class="flyout">string</code></td>
            <td>Der Name der Instrumentation, auf der angehalten werden soll. Gültige Werte: "scriptFirstStatement".</td>
        </tr>
    </tbody>
</table>
</p>

---

### removeInstrumentationBreakpoint
<span><b>Experimenteller. </b></span>Entfernt einen Haltepunkt für ein bestimmtes systemeigenes Ereignis.

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
            <td>EventName</td>
            <td><code class="flyout">string</code></td>
            <td>Der Name der Instrumentation, auf der angehalten werden soll. Gültige Werte: "scriptFirstStatement".</td>
        </tr>
    </tbody>
</table>
</p>

---
