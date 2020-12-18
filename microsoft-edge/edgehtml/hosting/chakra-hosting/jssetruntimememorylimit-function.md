---
description: Legt den aktuellen Speichergrenzwert für eine Laufzeit fest.
title: JsSetRuntimeMemoryLimit-Funktion | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsSetRuntimeMemoryLimit
helpviewer_keywords:
- JsSetRuntimeMemoryLimit function
ms.assetid: 74feb31f-19f6-43e3-b117-0694c59ac593
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 1c31d8bbbec4be22fc1af09e546ad4c95f8ec2bd
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233560"
---
# <span data-ttu-id="50baa-103">JsSetRuntimeMemoryLimit Funktion</span><span class="sxs-lookup"><span data-stu-id="50baa-103">JsSetRuntimeMemoryLimit Function</span></span>

<span data-ttu-id="50baa-104">Legt den aktuellen Speichergrenzwert für eine Laufzeit fest.</span><span class="sxs-lookup"><span data-stu-id="50baa-104">Sets the current memory limit for a runtime.</span></span>  
  
## <span data-ttu-id="50baa-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="50baa-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsSetRuntimeMemoryLimit(  
   _In_ JsRuntimeHandle runtime,  
   _In_ size_t memoryLimit  
);  
```  
  
#### <span data-ttu-id="50baa-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="50baa-106">Parameters</span></span>  
 `runtime`  
 <span data-ttu-id="50baa-107">Die Laufzeit, deren Speichergrenzwert festzulegen ist.</span><span class="sxs-lookup"><span data-stu-id="50baa-107">The runtime whose memory limit is to be set.</span></span>  
  
 `memoryLimit`  
 <span data-ttu-id="50baa-108">Die neue Obergrenze für den Arbeitsspeicher, in Bytes oder-1 für keinen Speichergrenzwert.</span><span class="sxs-lookup"><span data-stu-id="50baa-108">The new runtime memory limit, in bytes, or -1 for no memory limit.</span></span>  
  
## <span data-ttu-id="50baa-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="50baa-109">Return Value</span></span>  
 <span data-ttu-id="50baa-110">Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="50baa-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="50baa-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="50baa-111">Remarks</span></span>  
 <span data-ttu-id="50baa-112">Eine Speichergrenze führt dazu, dass jeder Vorgang, der den Grenzwert überschreitet, mit einem Fehler "nicht genügend Arbeitsspeicher" fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="50baa-112">A memory limit will cause any operation which exceeds the limit to fail with an "out of memory" error.</span></span> <span data-ttu-id="50baa-113">Das Festlegen der Speichergrenze einer Runtime auf-1 bedeutet, dass die Laufzeit keine Speichergrenze aufweist.</span><span class="sxs-lookup"><span data-stu-id="50baa-113">Setting a runtime's memory limit to -1 means that the runtime has no memory limit.</span></span> <span data-ttu-id="50baa-114">Für neue Runtimes wird standardmäßig kein Speichergrenzwert festgesetzt.</span><span class="sxs-lookup"><span data-stu-id="50baa-114">New runtimes default to having no memory limit.</span></span> <span data-ttu-id="50baa-115">Wenn die neue Arbeitsspeichergrenze die aktuelle Nutzung überschreitet, wird der Aufruf erfolgreich ausgeführt, und alle zukünftigen Zuweisungen in dieser Runtime schlagen fehl, bis die Speicherauslastung der Common Language Runtime unter den Grenzwert fällt.</span><span class="sxs-lookup"><span data-stu-id="50baa-115">If the new memory limit exceeds current usage, the call will succeed and any future allocations in this runtime will fail until the runtime's memory usage drops below the limit.</span></span>  
  
 <span data-ttu-id="50baa-116">Die Speichergrenze einer Common Language Runtime kann immer festgesetzt werden, unabhängig davon, ob die Laufzeit in einem anderen Thread aktiv ist oder nicht.</span><span class="sxs-lookup"><span data-stu-id="50baa-116">A runtime's memory limit can be always be set, regardless of whether or not the runtime is active on another thread.</span></span>  
  
## <span data-ttu-id="50baa-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="50baa-117">Requirements</span></span>  
 <span data-ttu-id="50baa-118">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="50baa-118">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="50baa-119">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="50baa-119">See Also</span></span>  
 [<span data-ttu-id="50baa-120">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="50baa-120">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
