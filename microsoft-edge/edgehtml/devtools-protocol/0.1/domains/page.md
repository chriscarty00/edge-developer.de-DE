---
description: DevTools Protocol Version 0,1 (EdgeHTML)-Referenz für die Seiten Domäne. Aktionen und Ereignisse im Zusammenhang mit der geprüften Seite gehören der Seiten Domäne an.
title: Page Domain-devtools Protocol Version 0,1 (EdgeHTML)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: reference
ms.prod: microsoft-edge
ms.custom: seodec18
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 55575e54b9125d7ff544c23c81da4b15d3b56fb1
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11234025"
---
# <span data-ttu-id="a3e49-104">Page Domain-devtools Protocol Version 0,1 (EdgeHTML)</span><span class="sxs-lookup"><span data-stu-id="a3e49-104">Page Domain - DevTools Protocol Version 0.1 (EdgeHTML)</span></span>  

<span data-ttu-id="a3e49-105">Aktionen und Ereignisse im Zusammenhang mit der geprüften Seite gehören der Seiten Domäne an.</span><span class="sxs-lookup"><span data-stu-id="a3e49-105">Actions and events related to the inspected page belong to the page domain.</span></span>

| | |
|-|-|
| [**<span data-ttu-id="a3e49-106">Methoden</span><span class="sxs-lookup"><span data-stu-id="a3e49-106">Methods</span></span>**](#methods) | <span data-ttu-id="a3e49-107">[aktivieren](#enable), [Deaktivieren](#disable), [Navigieren](#navigate)</span><span class="sxs-lookup"><span data-stu-id="a3e49-107">[enable](#enable), [disable](#disable), [navigate](#navigate)</span></span> |
| [**<span data-ttu-id="a3e49-108">Typen</span><span class="sxs-lookup"><span data-stu-id="a3e49-108">Types</span></span>**](#types) | [<span data-ttu-id="a3e49-109">Frame-Nr</span><span class="sxs-lookup"><span data-stu-id="a3e49-109">FrameId</span></span>](#frameid) |
## <span data-ttu-id="a3e49-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="a3e49-110">Methods</span></span>

### <span data-ttu-id="a3e49-111">Aktivieren</span><span class="sxs-lookup"><span data-stu-id="a3e49-111">enable</span></span>
<span data-ttu-id="a3e49-112">Aktiviert Seiten Domänen Benachrichtigungen.</span><span class="sxs-lookup"><span data-stu-id="a3e49-112">Enables page domain notifications.</span></span>


---

### <span data-ttu-id="a3e49-113">Deaktivieren </span><span class="sxs-lookup"><span data-stu-id="a3e49-113">disable</span></span>
<span data-ttu-id="a3e49-114">Deaktiviert Seiten Domänen Benachrichtigungen.</span><span class="sxs-lookup"><span data-stu-id="a3e49-114">Disables page domain notifications.</span></span>


---

### <span data-ttu-id="a3e49-115">Navigieren</span><span class="sxs-lookup"><span data-stu-id="a3e49-115">navigate</span></span>
<span data-ttu-id="a3e49-116">Navigiert die aktuelle Seite zur angegebenen URL.</span><span class="sxs-lookup"><span data-stu-id="a3e49-116">Navigates current page to the given URL.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="a3e49-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="a3e49-117">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="a3e49-118">URL</span><span class="sxs-lookup"><span data-stu-id="a3e49-118">url</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="a3e49-119">Die URL, zu der die Seite navigiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="a3e49-119">URL to navigate the page to.</span></span></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="a3e49-120">Gibt</span><span class="sxs-lookup"><span data-stu-id="a3e49-120">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="a3e49-121">Frame-Nr</span><span class="sxs-lookup"><span data-stu-id="a3e49-121">frameId</span></span></td>
            <td><a href="#frameid"><code class="flyout">FrameId</code></a></td>
            <td><span><b><span data-ttu-id="a3e49-122">Experimenteller.</span><span class="sxs-lookup"><span data-stu-id="a3e49-122">Experimental.</span></span> </b></span><span data-ttu-id="a3e49-123">Die Frame-ID, die navigiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="a3e49-123">Frame id that will be navigated.</span></span></td>
        </tr>
    </tbody>
</table>

---

## <span data-ttu-id="a3e49-124">Typen</span><span class="sxs-lookup"><span data-stu-id="a3e49-124">Types</span></span>

### <a name="frameid"></a> <span data-ttu-id="a3e49-125">Frame-Nr</span><span class="sxs-lookup"><span data-stu-id="a3e49-125">FrameId</span></span> `string`

<span data-ttu-id="a3e49-126">Eindeutige Frame-ID.</span><span class="sxs-lookup"><span data-stu-id="a3e49-126">Unique frame identifier.</span></span>


---
