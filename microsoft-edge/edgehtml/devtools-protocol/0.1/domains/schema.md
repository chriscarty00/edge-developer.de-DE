---
description: DevTools Protocol Version 0.1 (EdgeHTML)-Referenz für die Schemadomäne. Stellt Informationen zum Protokollschema zur Verfügung.
title: Schemadomäne – DevTools Protocol Version 0.1 (EdgeHTML)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/03/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.custom: seodec18
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: e89f4269b4984ee49e83a23fcab9679485c49040
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398861"
---
# <a name="schema-domain---devtools-protocol-version-01-edgehtml"></a><span data-ttu-id="459af-104">Schemadomäne – DevTools Protocol Version 0.1 (EdgeHTML)</span><span class="sxs-lookup"><span data-stu-id="459af-104">Schema Domain - DevTools Protocol Version 0.1 (EdgeHTML)</span></span>  

<span data-ttu-id="459af-105">Stellt Informationen zum Protokollschema zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="459af-105">Provides information about the protocol schema.</span></span>  

| <span data-ttu-id="459af-106">Klassifizierung</span><span class="sxs-lookup"><span data-stu-id="459af-106">Classification</span></span> | <span data-ttu-id="459af-107">Member</span><span class="sxs-lookup"><span data-stu-id="459af-107">Members</span></span> |  
|:--- |:--- |  
| [<span data-ttu-id="459af-108">Methoden</span><span class="sxs-lookup"><span data-stu-id="459af-108">Methods</span></span>](#methods) | [<span data-ttu-id="459af-109">getDomains</span><span class="sxs-lookup"><span data-stu-id="459af-109">getDomains</span></span>](#getdomains) |  
| [<span data-ttu-id="459af-110">Typen</span><span class="sxs-lookup"><span data-stu-id="459af-110">Types</span></span>](#types) | [<span data-ttu-id="459af-111">Domäne</span><span class="sxs-lookup"><span data-stu-id="459af-111">Domain</span></span>](#domain) |  

## <a name="methods"></a><span data-ttu-id="459af-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="459af-112">Methods</span></span>  

### <a name="getdomains"></a><span data-ttu-id="459af-113">getDomains</span><span class="sxs-lookup"><span data-stu-id="459af-113">getDomains</span></span>  

<span data-ttu-id="459af-114">Gibt unterstützte Domänen zurück.</span><span class="sxs-lookup"><span data-stu-id="459af-114">Returns supported domains.</span></span>  

| <span data-ttu-id="459af-115">Gibt zurück</span><span class="sxs-lookup"><span data-stu-id="459af-115">Returns</span></span> | <span data-ttu-id="459af-116">Typ</span><span class="sxs-lookup"><span data-stu-id="459af-116">Type</span></span> | <span data-ttu-id="459af-117">Details</span><span class="sxs-lookup"><span data-stu-id="459af-117">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="459af-118">domänen</span><span class="sxs-lookup"><span data-stu-id="459af-118">domains</span></span> | [<span data-ttu-id="459af-119">Domain[]</span><span class="sxs-lookup"><span data-stu-id="459af-119">Domain[]</span></span>](#domain) | <span data-ttu-id="459af-120">Liste der unterstützten Domänen.</span><span class="sxs-lookup"><span data-stu-id="459af-120">List of supported domains.</span></span> |  

---  

## <a name="types"></a><span data-ttu-id="459af-121">Typen</span><span class="sxs-lookup"><span data-stu-id="459af-121">Types</span></span>  

### <a name="domain-object"></a><span data-ttu-id="459af-122">Domänenobjekt</span><span class="sxs-lookup"><span data-stu-id="459af-122">Domain object</span></span>  

<a name="domain"></a>  

<span data-ttu-id="459af-123">Beschreibung der Protokolldomäne.</span><span class="sxs-lookup"><span data-stu-id="459af-123">Description of the protocol domain.</span></span>  

| <span data-ttu-id="459af-124">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="459af-124">Properties</span></span> | <span data-ttu-id="459af-125">Typ</span><span class="sxs-lookup"><span data-stu-id="459af-125">Type</span></span> | <span data-ttu-id="459af-126">Details</span><span class="sxs-lookup"><span data-stu-id="459af-126">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="459af-127">name</span><span class="sxs-lookup"><span data-stu-id="459af-127">name</span></span> | `string` | <span data-ttu-id="459af-128">Domänenname.</span><span class="sxs-lookup"><span data-stu-id="459af-128">Domain name.</span></span> |  
| <span data-ttu-id="459af-129">version</span><span class="sxs-lookup"><span data-stu-id="459af-129">version</span></span> | `string` | <span data-ttu-id="459af-130">Domänenversion.</span><span class="sxs-lookup"><span data-stu-id="459af-130">Domain version.</span></span> |  

---  
