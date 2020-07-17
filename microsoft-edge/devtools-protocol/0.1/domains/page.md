---
description: Verweis auf die Seiten Domäne Aktionen und Ereignisse im Zusammenhang mit der geprüften Seite gehören der Seiten Domäne an.
title: Page Domain-devtools Protocol Version 0,1 (EdgeHTML)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/16/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.custom: seodec18
ms.openlocfilehash: 1602673eae1c04f60046a898dbadeab1b59f9ce5
ms.sourcegitcommit: a06c86ef7c69e1e400a0be5938449f3c4ba6ec72
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/16/2020
ms.locfileid: "10882940"
---
# Page Domain-devtools Protocol Version 0,1 (EdgeHTML)  

Aktionen und Ereignisse im Zusammenhang mit der geprüften Seite gehören der Seiten Domäne an.

| | |
|-|-|
| [**Methoden**](#methods) | [aktivieren](#enable), [Deaktivieren](#disable), [Navigieren](#navigate) |
| [**Typen**](#types) | [Frame-Nr](#frameid) |
## Methoden

### Aktivieren
Aktiviert Seiten Domänen Benachrichtigungen.


---

### Deaktivieren 
Deaktiviert Seiten Domänen Benachrichtigungen.


---

### Navigieren
Navigiert die aktuelle Seite zur angegebenen URL.

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
            <td>URL</td>
            <td><code class="flyout">string</code></td>
            <td>Die URL, zu der die Seite navigiert werden soll.</td>
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
            <td>Frame-Nr</td>
            <td><a href="#frameid"><code class="flyout">FrameId</code></a></td>
            <td><span><b>Experimenteller. </b></span>Die Frame-ID, die navigiert werden soll.</td>
        </tr>
    </tbody>
</table>

---

## Typen

### <a name="frameid"></a> Frame-Nr `string`

Eindeutige Frame-ID.


---
