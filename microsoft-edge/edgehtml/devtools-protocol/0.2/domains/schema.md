---
description: DevTools Protocol Version 0,2 (EdgeHTML)-Referenz für die Schema Domäne. Enthält Informationen zum Protokollschema.
title: Schema Domain-devtools Protocol Version 0,2 (EdgeHTML)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: reference
ms.prod: microsoft-edge
ms.date: 12/16/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 53038a02844fafc9550a6ac26303620a1a0183f8
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233630"
---
# Schema Domain-devtools Protocol Version 0,2 (EdgeHTML)  

Enthält Informationen zum Protokollschema.

| | |
|-|-|
| [**Methoden**](#methods) | [getdomains](#getdomains) |
| [**Typen**](#types) | [Domäne](#domain) |
## Methoden

### getdomains
Gibt unterstützte Domänen zurück.

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
            <td>Domänen</td>
            <td><a href="#domain"><code class="flyout">Domain[]</code></a></td>
            <td>Liste der unterstützten Domänen.</td>
        </tr>
    </tbody>
</table>
</p>

---

## Typen

### <a name="domain"></a> Domäne `object`

Beschreibung der Protokoll Domäne.

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
            <td>Domänenname.</td>
        </tr>
        <tr>
            <td>version</td>
            <td><code class="flyout">string</code></td>
            <td>Domänen Version.</td>
        </tr>
    </tbody>
</table>
</p>

---
