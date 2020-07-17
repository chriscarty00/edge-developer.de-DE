---
description: Verweis auf die Seiten Domäne Aktionen und Ereignisse im Zusammenhang mit der geprüften Seite gehören der Seiten Domäne an.
title: Page Domain-devtools Protocol Version 0,1 (EdgeHTML)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/16/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.custom: seodec18
ms.openlocfilehash: 1602673eae1c04f60046a898dbadeab1b59f9ce5
ms.sourcegitcommit: a06c86ef7c69e1e400a0be5938449f3c4ba6ec72
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/16/2020
ms.locfileid: "10882940"
---
# <span data-ttu-id="af212-104">Page Domain-devtools Protocol Version 0,1 (EdgeHTML)</span><span class="sxs-lookup"><span data-stu-id="af212-104">Page Domain - DevTools Protocol Version 0.1 (EdgeHTML)</span></span>  

<span data-ttu-id="af212-105">Aktionen und Ereignisse im Zusammenhang mit der geprüften Seite gehören der Seiten Domäne an.</span><span class="sxs-lookup"><span data-stu-id="af212-105">Actions and events related to the inspected page belong to the page domain.</span></span>

| | |
|-|-|
| [**<span data-ttu-id="af212-106">Methoden</span><span class="sxs-lookup"><span data-stu-id="af212-106">Methods</span></span>**](#methods) | <span data-ttu-id="af212-107">[aktivieren](#enable), [Deaktivieren](#disable), [Navigieren](#navigate)</span><span class="sxs-lookup"><span data-stu-id="af212-107">[enable](#enable), [disable](#disable), [navigate](#navigate)</span></span> |
| [**<span data-ttu-id="af212-108">Typen</span><span class="sxs-lookup"><span data-stu-id="af212-108">Types</span></span>**](#types) | [<span data-ttu-id="af212-109">Frame-Nr</span><span class="sxs-lookup"><span data-stu-id="af212-109">FrameId</span></span>](#frameid) |
## <span data-ttu-id="af212-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="af212-110">Methods</span></span>

### <span data-ttu-id="af212-111">Aktivieren</span><span class="sxs-lookup"><span data-stu-id="af212-111">enable</span></span>
<span data-ttu-id="af212-112">Aktiviert Seiten Domänen Benachrichtigungen.</span><span class="sxs-lookup"><span data-stu-id="af212-112">Enables page domain notifications.</span></span>


---

### <span data-ttu-id="af212-113">Deaktivieren </span><span class="sxs-lookup"><span data-stu-id="af212-113">disable</span></span>
<span data-ttu-id="af212-114">Deaktiviert Seiten Domänen Benachrichtigungen.</span><span class="sxs-lookup"><span data-stu-id="af212-114">Disables page domain notifications.</span></span>


---

### <span data-ttu-id="af212-115">Navigieren</span><span class="sxs-lookup"><span data-stu-id="af212-115">navigate</span></span>
<span data-ttu-id="af212-116">Navigiert die aktuelle Seite zur angegebenen URL.</span><span class="sxs-lookup"><span data-stu-id="af212-116">Navigates current page to the given URL.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="af212-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="af212-117">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="af212-118">URL</span><span class="sxs-lookup"><span data-stu-id="af212-118">url</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="af212-119">Die URL, zu der die Seite navigiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="af212-119">URL to navigate the page to.</span></span></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="af212-120">Gibt</span><span class="sxs-lookup"><span data-stu-id="af212-120">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="af212-121">Frame-Nr</span><span class="sxs-lookup"><span data-stu-id="af212-121">frameId</span></span></td>
            <td><a href="#frameid"><code class="flyout">FrameId</code></a></td>
            <td><span><b><span data-ttu-id="af212-122">Experimenteller.</span><span class="sxs-lookup"><span data-stu-id="af212-122">Experimental.</span></span> </b></span><span data-ttu-id="af212-123">Die Frame-ID, die navigiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="af212-123">Frame id that will be navigated.</span></span></td>
        </tr>
    </tbody>
</table>

---

## <span data-ttu-id="af212-124">Typen</span><span class="sxs-lookup"><span data-stu-id="af212-124">Types</span></span>

### <a name="frameid"></a> <span data-ttu-id="af212-125">Frame-Nr</span><span class="sxs-lookup"><span data-stu-id="af212-125">FrameId</span></span> `string`

<span data-ttu-id="af212-126">Eindeutige Frame-ID.</span><span class="sxs-lookup"><span data-stu-id="af212-126">Unique frame identifier.</span></span>


---
