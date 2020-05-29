---
description: Referenz für die Schema Domäne. Enthält Informationen zum Protokollschema.
title: Schema Domäne – devtools-Protokoll Version 0,2
author: pelavall
ms.author: pelavall
ms.date: 8/17/2018
ms.topic: reference
ms.prod: microsoft-edge
ms.openlocfilehash: df86e6669956c14b7c905514fc44376f71eaa993
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10567527"
---
# Schema
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
