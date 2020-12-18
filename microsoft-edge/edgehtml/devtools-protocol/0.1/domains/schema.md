---
description: DevTools Protocol Version 0,1 (EdgeHTML)-Referenz für die Schema Domäne. Enthält Informationen zum Protokollschema.
title: Schema Domain-devtools Protocol Version 0,1 (EdgeHTML)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: reference
ms.prod: microsoft-edge
ms.custom: seodec18
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 7b4ec71b7799ae099c673bd81fa5b15a8ddd5d27
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11234018"
---
# Schema Domain-devtools Protocol Version 0,1 (EdgeHTML)  

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

---
