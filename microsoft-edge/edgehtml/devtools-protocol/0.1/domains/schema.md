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
# <span data-ttu-id="78452-104">Schema Domain-devtools Protocol Version 0,1 (EdgeHTML)</span><span class="sxs-lookup"><span data-stu-id="78452-104">Schema Domain - DevTools Protocol Version 0.1 (EdgeHTML)</span></span>  

<span data-ttu-id="78452-105">Enthält Informationen zum Protokollschema.</span><span class="sxs-lookup"><span data-stu-id="78452-105">Provides information about the protocol schema.</span></span>

| | |
|-|-|
| [**<span data-ttu-id="78452-106">Methoden</span><span class="sxs-lookup"><span data-stu-id="78452-106">Methods</span></span>**](#methods) | [<span data-ttu-id="78452-107">getdomains</span><span class="sxs-lookup"><span data-stu-id="78452-107">getDomains</span></span>](#getdomains) |
| [**<span data-ttu-id="78452-108">Typen</span><span class="sxs-lookup"><span data-stu-id="78452-108">Types</span></span>**](#types) | [<span data-ttu-id="78452-109">Domäne</span><span class="sxs-lookup"><span data-stu-id="78452-109">Domain</span></span>](#domain) |
## <span data-ttu-id="78452-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="78452-110">Methods</span></span>

### <span data-ttu-id="78452-111">getdomains</span><span class="sxs-lookup"><span data-stu-id="78452-111">getDomains</span></span>
<span data-ttu-id="78452-112">Gibt unterstützte Domänen zurück.</span><span class="sxs-lookup"><span data-stu-id="78452-112">Returns supported domains.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="78452-113">Gibt</span><span class="sxs-lookup"><span data-stu-id="78452-113">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="78452-114">Domänen</span><span class="sxs-lookup"><span data-stu-id="78452-114">domains</span></span></td>
            <td><a href="#domain"><code class="flyout">Domain[]</code></a></td>
            <td><span data-ttu-id="78452-115">Liste der unterstützten Domänen.</span><span class="sxs-lookup"><span data-stu-id="78452-115">List of supported domains.</span></span></td>
        </tr>
    </tbody>
</table>

---

## <span data-ttu-id="78452-116">Typen</span><span class="sxs-lookup"><span data-stu-id="78452-116">Types</span></span>

### <a name="domain"></a> <span data-ttu-id="78452-117">Domäne</span><span class="sxs-lookup"><span data-stu-id="78452-117">Domain</span></span> `object`

<span data-ttu-id="78452-118">Beschreibung der Protokoll Domäne.</span><span class="sxs-lookup"><span data-stu-id="78452-118">Description of the protocol domain.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="78452-119">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="78452-119">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="78452-120">name</span><span class="sxs-lookup"><span data-stu-id="78452-120">name</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="78452-121">Domänenname.</span><span class="sxs-lookup"><span data-stu-id="78452-121">Domain name.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="78452-122">version</span><span class="sxs-lookup"><span data-stu-id="78452-122">version</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="78452-123">Domänen Version.</span><span class="sxs-lookup"><span data-stu-id="78452-123">Domain version.</span></span></td>
        </tr>
    </tbody>
</table>

---
