---
description: Verweis auf die Seiten Domäne Aktionen und Ereignisse im Zusammenhang mit der geprüften Seite gehören der Seiten Domäne an.
title: Page Domain-devtools Protocol Version 0,2 (EdgeHTML)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/16/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.openlocfilehash: 864515eefbcb809e280f2ab1d81015018272c398
ms.sourcegitcommit: a06c86ef7c69e1e400a0be5938449f3c4ba6ec72
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/16/2020
ms.locfileid: "10882842"
---
# Page Domain-devtools Protocol Version 0,2 (EdgeHTML)  

Aktionen und Ereignisse im Zusammenhang mit der geprüften Seite gehören der Seiten Domäne an.

| | |
|-|-|
| [**Methoden**](#methods) | [aktivieren](#enable), [Deaktivieren](#disable), [Navigieren](#navigate), [getFrameTree](#getframetree) |
| [**Veranstaltungen**](#events) | [frameAttached](#frameattached), [frameDetached](#framedetached), [frameNavigated](#framenavigated), [loadEventFired](#loadeventfired), [domContentEventFired](#domcontenteventfired) |
| [**Typen**](#types) | [Frame](#frameid)-Nr, [Frame](#frame), [FrameTree](#frametree) |
## Methoden

### Aktivieren
Aktiviert Seiten Domänen Benachrichtigungen.

</p>

---

### Deaktivieren 
Deaktiviert Seiten Domänen Benachrichtigungen.

</p>

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
        <tr>
            <td>Frame-Nr <br/> <i>Optional</i></td>
            <td><a href="#frameid"><code class="flyout">FrameId</code></a></td>
            <td>Die Frame-ID zum Navigieren. Wenn keine Angabe erfolgt, navigiert die oberste Seite.</td>
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
            <td>Die Frame-ID, die navigiert werden soll.</td>
        </tr>
    </tbody>
</table>
</p>

---

### getFrameTree
Gibt die aktuelle Frame Struktur zurück.

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
            <td>frameTree</td>
            <td><a href="#frametree"><code class="flyout">FrameTree</code></a></td>
            <td>Aktuelle Frame Struktur.</td>
        </tr>
    </tbody>
</table>
</p>

---

## Veranstaltungen

### frameAttached
Wird ausgelöst, wenn Frame dem übergeordneten Element angefügt wurde.

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
            <td>Frame-Nr</td>
            <td><a href="#frameid"><code class="flyout">FrameId</code></a></td>
            <td>Die ID des Rahmens, der angefügt wurde.</td>
        </tr>
        <tr>
            <td>parentFrameId</td>
            <td><a href="#frameid"><code class="flyout">FrameId</code></a></td>
            <td>Übergeordneter Frame Bezeichner</td>
        </tr>
        <tr>
            <td>Stapel <br/> <i>Optional</i></td>
            <td><a href="runtime.md#stacktrace"><code class="flyout">Runtime.StackTrace</code></a></td>
            <td>JavaScript-Stapelüberwachung, wenn Frame angefügt wurde, nur festgelegt, wenn Frame vom Skript initiiert wurde.</td>
        </tr>
    </tbody>
</table>
</p>

---

### frameDetached
Wird ausgelöst, wenn Frame vom übergeordneten Element abgetrennt wurde.

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
            <td>Frame-Nr</td>
            <td><a href="#frameid"><code class="flyout">FrameId</code></a></td>
            <td>Die ID des Frames, der abgetrennt wurde.</td>
        </tr>
    </tbody>
</table>
</p>

---

### frameNavigated
Wird ausgelöst, sobald die Navigation des Frames abgeschlossen ist.

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
            <td>Frame</td>
            <td><a href="#frame"><code class="flyout">Frame</code></a></td>
            <td>Frame-Objekt</td>
        </tr>
    </tbody>
</table>
</p>

---

### loadEventFired
Entspricht dem Window. OnLoad-Ereignis.

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
            <td><code class="flyout">number</code></td>
            <td>Die Anzahl der Millisekunden seit Epoch.</td>
        </tr>
    </tbody>
</table>
</p>

---

### domContentEventFired
Entspricht dem Document. onDOMContentLoaded-Ereignis.

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
            <td><code class="flyout">number</code></td>
            <td>Die Anzahl der Millisekunden seit Epoch.</td>
        </tr>
    </tbody>
</table>
</p>

---

## Typen

### <a name="frameid"></a> Frame-Nr `string`

Eindeutige Frame-ID.

</p>

---

### <a name="frame"></a> Frame `object`

Informationen zum Frame auf der Seite.

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
            <td><a href="#frameid"><code class="flyout">FrameId</code></a></td>
            <td>Frame-eindeutiger Bezeichner</td>
        </tr>
        <tr>
            <td>parentID <br/> <i>Optional</i></td>
            <td><a href="#frameid"><code class="flyout">FrameId</code></a></td>
            <td>Eindeutiger Bezeichner des übergeordneten Frames</td>
        </tr>
        <tr>
            <td>name <br/> <i>Optional</i></td>
            <td><code class="flyout">string</code></td>
            <td>Der Name des Frames, wie in der Kategorie angegeben.</td>
        </tr>
        <tr>
            <td>URL</td>
            <td><code class="flyout">string</code></td>
            <td>Die URL des Frame-Dokuments.</td>
        </tr>
        <tr>
            <td>securityOrigin</td>
            <td><code class="flyout">string</code></td>
            <td>Sicherheits Ursprung des Frame-Dokuments.</td>
        </tr>
        <tr>
            <td>mimeType</td>
            <td><code class="flyout">string</code></td>
            <td>Das vom Browser festgelegte MimeType-Dateiformat des Dokuments.</td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="frametree"></a> FrameTree `object`

Informationen zur Frame Hierarchie.

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
            <td>Frame</td>
            <td><a href="#frame"><code class="flyout">Frame</code></a></td>
            <td>Frame Informationen für dieses Strukturelement</td>
        </tr>
        <tr>
            <td>childFrames <br/> <i>Optional</i></td>
            <td><a href="#frametree"><code class="flyout">FrameTree[]</code></a></td>
            <td>Untergeordnete Frames</td>
        </tr>
    </tbody>
</table>
</p>

---
