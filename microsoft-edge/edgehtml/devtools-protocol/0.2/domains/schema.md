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
# <span data-ttu-id="f6d9d-104">Schema Domain-devtools Protocol Version 0,2 (EdgeHTML)</span><span class="sxs-lookup"><span data-stu-id="f6d9d-104">Schema Domain - DevTools Protocol Version 0.2 (EdgeHTML)</span></span>  

<span data-ttu-id="f6d9d-105">Enthält Informationen zum Protokollschema.</span><span class="sxs-lookup"><span data-stu-id="f6d9d-105">Provides information about the protocol schema.</span></span>

| | |
|-|-|
| [**<span data-ttu-id="f6d9d-106">Methoden</span><span class="sxs-lookup"><span data-stu-id="f6d9d-106">Methods</span></span>**](#methods) | [<span data-ttu-id="f6d9d-107">getdomains</span><span class="sxs-lookup"><span data-stu-id="f6d9d-107">getDomains</span></span>](#getdomains) |
| [**<span data-ttu-id="f6d9d-108">Typen</span><span class="sxs-lookup"><span data-stu-id="f6d9d-108">Types</span></span>**](#types) | [<span data-ttu-id="f6d9d-109">Domäne</span><span class="sxs-lookup"><span data-stu-id="f6d9d-109">Domain</span></span>](#domain) |
## <span data-ttu-id="f6d9d-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="f6d9d-110">Methods</span></span>

### <span data-ttu-id="f6d9d-111">getdomains</span><span class="sxs-lookup"><span data-stu-id="f6d9d-111">getDomains</span></span>
<span data-ttu-id="f6d9d-112">Gibt unterstützte Domänen zurück.</span><span class="sxs-lookup"><span data-stu-id="f6d9d-112">Returns supported domains.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="f6d9d-113">Gibt</span><span class="sxs-lookup"><span data-stu-id="f6d9d-113">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="f6d9d-114">Domänen</span><span class="sxs-lookup"><span data-stu-id="f6d9d-114">domains</span></span></td>
            <td><a href="#domain"><code class="flyout">Domain[]</code></a></td>
            <td><span data-ttu-id="f6d9d-115">Liste der unterstützten Domänen.</span><span class="sxs-lookup"><span data-stu-id="f6d9d-115">List of supported domains.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

## <span data-ttu-id="f6d9d-116">Typen</span><span class="sxs-lookup"><span data-stu-id="f6d9d-116">Types</span></span>

### <a name="domain"></a> <span data-ttu-id="f6d9d-117">Domäne</span><span class="sxs-lookup"><span data-stu-id="f6d9d-117">Domain</span></span> `object`

<span data-ttu-id="f6d9d-118">Beschreibung der Protokoll Domäne.</span><span class="sxs-lookup"><span data-stu-id="f6d9d-118">Description of the protocol domain.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="f6d9d-119">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f6d9d-119">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="f6d9d-120">name</span><span class="sxs-lookup"><span data-stu-id="f6d9d-120">name</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="f6d9d-121">Domänenname.</span><span class="sxs-lookup"><span data-stu-id="f6d9d-121">Domain name.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="f6d9d-122">version</span><span class="sxs-lookup"><span data-stu-id="f6d9d-122">version</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="f6d9d-123">Domänen Version.</span><span class="sxs-lookup"><span data-stu-id="f6d9d-123">Domain version.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---
