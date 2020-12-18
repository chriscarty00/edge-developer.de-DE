---
description: DevTools Protocol Version 0,1 (EdgeHTML)-Referenz für die Seiten Domäne. Aktionen und Ereignisse im Zusammenhang mit der geprüften Seite gehören der Seiten Domäne an.
title: Page Domain-devtools Protocol Version 0,1 (EdgeHTML)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: reference
ms.prod: microsoft-edge
ms.custom: seodec18
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 55575e54b9125d7ff544c23c81da4b15d3b56fb1
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11234025"
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
