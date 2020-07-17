---
description: Referenz für die Schema Domäne. Enthält Informationen zum Protokollschema.
title: Schema Domain-devtools Protocol Version 0,2 (EdgeHTML)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/16/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.openlocfilehash: d0fbe9cde742d255797a2460b940732ffa5b8f27
ms.sourcegitcommit: a06c86ef7c69e1e400a0be5938449f3c4ba6ec72
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/16/2020
ms.locfileid: "10882877"
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
