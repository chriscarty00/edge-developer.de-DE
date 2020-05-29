---
description: Referenz für die DOMDebugger-Domäne. Dom-Debuggen ermöglicht das Festlegen von Haltepunkten für bestimmte Dom-Vorgänge und-Ereignisse. Die JavaScript-Ausführung wird bei diesen Vorgängen so beendet, als ob ein regulärer Haltepunkt festgesetzt wurde.
title: DOMDebugger Domain-devtools Protocol Version 0,2
author: pelavall
ms.author: pelavall
ms.date: 8/17/2018
ms.topic: reference
ms.prod: microsoft-edge
ms.openlocfilehash: 437a88ff93bda36d85a8f5632c1a02aa205d049b
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10567533"
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
