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
# <span data-ttu-id="8fd9f-104">Schema Domain-devtools Protocol Version 0,2 (EdgeHTML)</span><span class="sxs-lookup"><span data-stu-id="8fd9f-104">Schema Domain - DevTools Protocol Version 0.2 (EdgeHTML)</span></span>  

<span data-ttu-id="8fd9f-105">Enthält Informationen zum Protokollschema.</span><span class="sxs-lookup"><span data-stu-id="8fd9f-105">Provides information about the protocol schema.</span></span>

| | |
|-|-|
| [**<span data-ttu-id="8fd9f-106">Methoden</span><span class="sxs-lookup"><span data-stu-id="8fd9f-106">Methods</span></span>**](#methods) | [<span data-ttu-id="8fd9f-107">getdomains</span><span class="sxs-lookup"><span data-stu-id="8fd9f-107">getDomains</span></span>](#getdomains) |
| [**<span data-ttu-id="8fd9f-108">Typen</span><span class="sxs-lookup"><span data-stu-id="8fd9f-108">Types</span></span>**](#types) | [<span data-ttu-id="8fd9f-109">Domäne</span><span class="sxs-lookup"><span data-stu-id="8fd9f-109">Domain</span></span>](#domain) |
## <span data-ttu-id="8fd9f-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="8fd9f-110">Methods</span></span>

### <span data-ttu-id="8fd9f-111">getdomains</span><span class="sxs-lookup"><span data-stu-id="8fd9f-111">getDomains</span></span>
<span data-ttu-id="8fd9f-112">Gibt unterstützte Domänen zurück.</span><span class="sxs-lookup"><span data-stu-id="8fd9f-112">Returns supported domains.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="8fd9f-113">Gibt</span><span class="sxs-lookup"><span data-stu-id="8fd9f-113">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="8fd9f-114">Domänen</span><span class="sxs-lookup"><span data-stu-id="8fd9f-114">domains</span></span></td>
            <td><a href="#domain"><code class="flyout">Domain[]</code></a></td>
            <td><span data-ttu-id="8fd9f-115">Liste der unterstützten Domänen.</span><span class="sxs-lookup"><span data-stu-id="8fd9f-115">List of supported domains.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

## <span data-ttu-id="8fd9f-116">Typen</span><span class="sxs-lookup"><span data-stu-id="8fd9f-116">Types</span></span>

### <a name="domain"></a> <span data-ttu-id="8fd9f-117">Domäne</span><span class="sxs-lookup"><span data-stu-id="8fd9f-117">Domain</span></span> `object`

<span data-ttu-id="8fd9f-118">Beschreibung der Protokoll Domäne.</span><span class="sxs-lookup"><span data-stu-id="8fd9f-118">Description of the protocol domain.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="8fd9f-119">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="8fd9f-119">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="8fd9f-120">name</span><span class="sxs-lookup"><span data-stu-id="8fd9f-120">name</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="8fd9f-121">Domänenname.</span><span class="sxs-lookup"><span data-stu-id="8fd9f-121">Domain name.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="8fd9f-122">version</span><span class="sxs-lookup"><span data-stu-id="8fd9f-122">version</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="8fd9f-123">Domänen Version.</span><span class="sxs-lookup"><span data-stu-id="8fd9f-123">Domain version.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---
