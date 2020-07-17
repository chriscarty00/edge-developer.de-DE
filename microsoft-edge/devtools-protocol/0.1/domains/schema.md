---
description: Referenz für die Schema Domäne. Enthält Informationen zum Protokollschema.
title: Schema Domain-devtools Protocol Version 0,1 (EdgeHTML)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/16/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.custom: seodec18
ms.openlocfilehash: a2f679f6f4bf8e82dc7298d96f798507b1338062
ms.sourcegitcommit: a06c86ef7c69e1e400a0be5938449f3c4ba6ec72
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/16/2020
ms.locfileid: "10882926"
---
# <span data-ttu-id="2ed08-104">Schema Domain-devtools Protocol Version 0,1 (EdgeHTML)</span><span class="sxs-lookup"><span data-stu-id="2ed08-104">Schema Domain - DevTools Protocol Version 0.1 (EdgeHTML)</span></span>  

<span data-ttu-id="2ed08-105">Enthält Informationen zum Protokollschema.</span><span class="sxs-lookup"><span data-stu-id="2ed08-105">Provides information about the protocol schema.</span></span>

| | |
|-|-|
| [**<span data-ttu-id="2ed08-106">Methoden</span><span class="sxs-lookup"><span data-stu-id="2ed08-106">Methods</span></span>**](#methods) | [<span data-ttu-id="2ed08-107">getdomains</span><span class="sxs-lookup"><span data-stu-id="2ed08-107">getDomains</span></span>](#getdomains) |
| [**<span data-ttu-id="2ed08-108">Typen</span><span class="sxs-lookup"><span data-stu-id="2ed08-108">Types</span></span>**](#types) | [<span data-ttu-id="2ed08-109">Domäne</span><span class="sxs-lookup"><span data-stu-id="2ed08-109">Domain</span></span>](#domain) |
## <span data-ttu-id="2ed08-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="2ed08-110">Methods</span></span>

### <span data-ttu-id="2ed08-111">getdomains</span><span class="sxs-lookup"><span data-stu-id="2ed08-111">getDomains</span></span>
<span data-ttu-id="2ed08-112">Gibt unterstützte Domänen zurück.</span><span class="sxs-lookup"><span data-stu-id="2ed08-112">Returns supported domains.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="2ed08-113">Gibt</span><span class="sxs-lookup"><span data-stu-id="2ed08-113">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="2ed08-114">Domänen</span><span class="sxs-lookup"><span data-stu-id="2ed08-114">domains</span></span></td>
            <td><a href="#domain"><code class="flyout">Domain[]</code></a></td>
            <td><span data-ttu-id="2ed08-115">Liste der unterstützten Domänen.</span><span class="sxs-lookup"><span data-stu-id="2ed08-115">List of supported domains.</span></span></td>
        </tr>
    </tbody>
</table>

---

## <span data-ttu-id="2ed08-116">Typen</span><span class="sxs-lookup"><span data-stu-id="2ed08-116">Types</span></span>

### <a name="domain"></a> <span data-ttu-id="2ed08-117">Domäne</span><span class="sxs-lookup"><span data-stu-id="2ed08-117">Domain</span></span> `object`

<span data-ttu-id="2ed08-118">Beschreibung der Protokoll Domäne.</span><span class="sxs-lookup"><span data-stu-id="2ed08-118">Description of the protocol domain.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="2ed08-119">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2ed08-119">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="2ed08-120">name</span><span class="sxs-lookup"><span data-stu-id="2ed08-120">name</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="2ed08-121">Domänenname.</span><span class="sxs-lookup"><span data-stu-id="2ed08-121">Domain name.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="2ed08-122">version</span><span class="sxs-lookup"><span data-stu-id="2ed08-122">version</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="2ed08-123">Domänen Version.</span><span class="sxs-lookup"><span data-stu-id="2ed08-123">Domain version.</span></span></td>
        </tr>
    </tbody>
</table>

---
