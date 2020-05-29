---
description: Verweis auf die Seiten Domäne Aktionen und Ereignisse im Zusammenhang mit der geprüften Seite gehören der Seiten Domäne an.
title: Page Domain-devtools Protocol Version 0,1
author: pelavall
ms.author: pelavall
ms.date: 12/15/2017
ms.topic: reference
ms.prod: microsoft-edge
ms.custom: seodec18
ms.openlocfilehash: a1cd094baef4571240881a86ecccfdb319fef61b
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10567558"
---
# <span data-ttu-id="80c02-104">Seite</span><span class="sxs-lookup"><span data-stu-id="80c02-104">Page</span></span>
<span data-ttu-id="80c02-105">Aktionen und Ereignisse im Zusammenhang mit der geprüften Seite gehören der Seiten Domäne an.</span><span class="sxs-lookup"><span data-stu-id="80c02-105">Actions and events related to the inspected page belong to the page domain.</span></span>

| | |
|-|-|
| [**<span data-ttu-id="80c02-106">Methoden</span><span class="sxs-lookup"><span data-stu-id="80c02-106">Methods</span></span>**](#methods) | <span data-ttu-id="80c02-107">[aktivieren](#enable), [Deaktivieren](#disable), [Navigieren](#navigate)</span><span class="sxs-lookup"><span data-stu-id="80c02-107">[enable](#enable), [disable](#disable), [navigate](#navigate)</span></span> |
| [**<span data-ttu-id="80c02-108">Typen</span><span class="sxs-lookup"><span data-stu-id="80c02-108">Types</span></span>**](#types) | [<span data-ttu-id="80c02-109">Frame-Nr</span><span class="sxs-lookup"><span data-stu-id="80c02-109">FrameId</span></span>](#frameid) |
## <span data-ttu-id="80c02-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="80c02-110">Methods</span></span>

### <span data-ttu-id="80c02-111">Aktivieren</span><span class="sxs-lookup"><span data-stu-id="80c02-111">enable</span></span>
<span data-ttu-id="80c02-112">Aktiviert Seiten Domänen Benachrichtigungen.</span><span class="sxs-lookup"><span data-stu-id="80c02-112">Enables page domain notifications.</span></span>


---

### <span data-ttu-id="80c02-113">Deaktivieren </span><span class="sxs-lookup"><span data-stu-id="80c02-113">disable</span></span>
<span data-ttu-id="80c02-114">Deaktiviert Seiten Domänen Benachrichtigungen.</span><span class="sxs-lookup"><span data-stu-id="80c02-114">Disables page domain notifications.</span></span>


---

### <span data-ttu-id="80c02-115">Navigieren</span><span class="sxs-lookup"><span data-stu-id="80c02-115">navigate</span></span>
<span data-ttu-id="80c02-116">Navigiert die aktuelle Seite zur angegebenen URL.</span><span class="sxs-lookup"><span data-stu-id="80c02-116">Navigates current page to the given URL.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="80c02-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="80c02-117">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="80c02-118">URL</span><span class="sxs-lookup"><span data-stu-id="80c02-118">url</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="80c02-119">Die URL, zu der die Seite navigiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="80c02-119">URL to navigate the page to.</span></span></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="80c02-120">Gibt</span><span class="sxs-lookup"><span data-stu-id="80c02-120">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="80c02-121">Frame-Nr</span><span class="sxs-lookup"><span data-stu-id="80c02-121">frameId</span></span></td>
            <td><a href="#frameid"><code class="flyout">FrameId</code></a></td>
            <td><span><b><span data-ttu-id="80c02-122">Experimenteller.</span><span class="sxs-lookup"><span data-stu-id="80c02-122">Experimental.</span></span> </b></span><span data-ttu-id="80c02-123">Die Frame-ID, die navigiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="80c02-123">Frame id that will be navigated.</span></span></td>
        </tr>
    </tbody>
</table>

---

## <span data-ttu-id="80c02-124">Typen</span><span class="sxs-lookup"><span data-stu-id="80c02-124">Types</span></span>

### <a name="frameid"></a> <span data-ttu-id="80c02-125">Frame-Nr</span><span class="sxs-lookup"><span data-stu-id="80c02-125">FrameId</span></span> `string`

<span data-ttu-id="80c02-126">Eindeutige Frame-ID.</span><span class="sxs-lookup"><span data-stu-id="80c02-126">Unique frame identifier.</span></span>


---
