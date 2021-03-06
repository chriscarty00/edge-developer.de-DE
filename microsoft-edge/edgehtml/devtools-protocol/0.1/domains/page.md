---
description: DevTools Protocol Version 0.1 (EdgeHTML)-Referenz für die Seitendomäne. Aktionen und Ereignisse im Zusammenhang mit der überprüften Seite gehören zur Seitendomäne.
title: Page Domain - DevTools Protocol Version 0.1 (EdgeHTML)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/03/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.custom: seodec18
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: b04b0685a6b465d40e999a2a48d370573a3058d8
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "11399148"
---
# <a name="page-domain---devtools-protocol-version-01-edgehtml"></a><span data-ttu-id="d85ae-104">Page Domain - DevTools Protocol Version 0.1 (EdgeHTML)</span><span class="sxs-lookup"><span data-stu-id="d85ae-104">Page Domain - DevTools Protocol Version 0.1 (EdgeHTML)</span></span>  

<span data-ttu-id="d85ae-105">Aktionen und Ereignisse im Zusammenhang mit der überprüften Seite gehören zur Seitendomäne.</span><span class="sxs-lookup"><span data-stu-id="d85ae-105">Actions and events related to the inspected page belong to the page domain.</span></span>  

| <span data-ttu-id="d85ae-106">Klassifizierung</span><span class="sxs-lookup"><span data-stu-id="d85ae-106">Classification</span></span> | <span data-ttu-id="d85ae-107">Member</span><span class="sxs-lookup"><span data-stu-id="d85ae-107">Members</span></span> |  
|:--- |:--- |  
| [**<span data-ttu-id="d85ae-108">Methoden</span><span class="sxs-lookup"><span data-stu-id="d85ae-108">Methods</span></span>**](#methods) | <span data-ttu-id="d85ae-109">[aktivieren](#enable), [deaktivieren](#disable), [navigieren](#navigate)</span><span class="sxs-lookup"><span data-stu-id="d85ae-109">[enable](#enable), [disable](#disable), [navigate](#navigate)</span></span> |  
| [**<span data-ttu-id="d85ae-110">Typen</span><span class="sxs-lookup"><span data-stu-id="d85ae-110">Types</span></span>**](#types) | [<span data-ttu-id="d85ae-111">FrameId</span><span class="sxs-lookup"><span data-stu-id="d85ae-111">FrameId</span></span>](#frameid) |  

## <a name="methods"></a><span data-ttu-id="d85ae-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="d85ae-112">Methods</span></span>  

### <a name="enable"></a><span data-ttu-id="d85ae-113">Aktivieren</span><span class="sxs-lookup"><span data-stu-id="d85ae-113">enable</span></span>  

<span data-ttu-id="d85ae-114">Aktiviert Seitendomänenbenachrichtigungen.</span><span class="sxs-lookup"><span data-stu-id="d85ae-114">Enables page domain notifications.</span></span>  

&nbsp;  

---  

### <a name="disable"></a><span data-ttu-id="d85ae-115">Deaktivieren </span><span class="sxs-lookup"><span data-stu-id="d85ae-115">disable</span></span>  

<span data-ttu-id="d85ae-116">Deaktiviert Seitendomänenbenachrichtigungen.</span><span class="sxs-lookup"><span data-stu-id="d85ae-116">Disables page domain notifications.</span></span>  

&nbsp;  

---  

### <a name="navigate"></a><span data-ttu-id="d85ae-117">Navigieren</span><span class="sxs-lookup"><span data-stu-id="d85ae-117">navigate</span></span>  

<span data-ttu-id="d85ae-118">Navigiert die aktuelle Seite zur angegebenen URL.</span><span class="sxs-lookup"><span data-stu-id="d85ae-118">Navigates current page to the given URL.</span></span>  

| <span data-ttu-id="d85ae-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="d85ae-119">Parameters</span></span> | <span data-ttu-id="d85ae-120">Typ</span><span class="sxs-lookup"><span data-stu-id="d85ae-120">Type</span></span> | <span data-ttu-id="d85ae-121">Details</span><span class="sxs-lookup"><span data-stu-id="d85ae-121">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="d85ae-122">URL</span><span class="sxs-lookup"><span data-stu-id="d85ae-122">url</span></span> | `string` | <span data-ttu-id="d85ae-123">URL, zu der die Seite navigiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="d85ae-123">URL to navigate the page to.</span></span> |  

| <span data-ttu-id="d85ae-124">Gibt zurück</span><span class="sxs-lookup"><span data-stu-id="d85ae-124">Returns</span></span> | <span data-ttu-id="d85ae-125">Typ</span><span class="sxs-lookup"><span data-stu-id="d85ae-125">Type</span></span> | <span data-ttu-id="d85ae-126">Details</span><span class="sxs-lookup"><span data-stu-id="d85ae-126">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="d85ae-127">frameId</span><span class="sxs-lookup"><span data-stu-id="d85ae-127">frameId</span></span> | [<span data-ttu-id="d85ae-128">FrameId</span><span class="sxs-lookup"><span data-stu-id="d85ae-128">FrameId</span></span>](#frameid) | <span data-ttu-id="d85ae-129">**Experimental**.</span><span class="sxs-lookup"><span data-stu-id="d85ae-129">**Experimental**.</span></span>  <span data-ttu-id="d85ae-130">Frame-ID, die navigiert wird.</span><span class="sxs-lookup"><span data-stu-id="d85ae-130">Frame ID that will be navigated.</span></span> |  

---  

## <a name="types"></a><span data-ttu-id="d85ae-131">Typen</span><span class="sxs-lookup"><span data-stu-id="d85ae-131">Types</span></span>  

### <a name="frameid-string"></a><span data-ttu-id="d85ae-132">FrameId-Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="d85ae-132">FrameId string</span></span>  

<a name="frameid"></a>  

<span data-ttu-id="d85ae-133">Eindeutige Frame-ID.</span><span class="sxs-lookup"><span data-stu-id="d85ae-133">Unique frame identifier.</span></span>  

&nbsp;  

---  
