---
description: Ruft den aktuellen Speichergrenzwert für eine Laufzeit ab.
title: JsGetRuntimeMemoryLimit-Funktion | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsGetRuntimeMemoryLimit
helpviewer_keywords:
- JsGetRuntimeMemoryLimit function
ms.assetid: ed81ca60-99fd-46b0-89ae-f6ac07926904
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: ed04a0fb921d22eea17eaf86ef7a0152fbf2a1d0
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11234262"
---
# <span data-ttu-id="825d2-103">JsGetRuntimeMemoryLimit Funktion</span><span class="sxs-lookup"><span data-stu-id="825d2-103">JsGetRuntimeMemoryLimit Function</span></span>

<span data-ttu-id="825d2-104">Ruft den aktuellen Speichergrenzwert für eine Laufzeit ab.</span><span class="sxs-lookup"><span data-stu-id="825d2-104">Gets the current memory limit for a runtime.</span></span>  
  
## <span data-ttu-id="825d2-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="825d2-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetRuntimeMemoryLimit(  
   _In_ JsRuntimeHandle runtime,  
   _Out_ size_t *memoryLimit  
);  
```  
  
#### <span data-ttu-id="825d2-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="825d2-106">Parameters</span></span>  
 `runtime`  
 <span data-ttu-id="825d2-107">Die Laufzeit, deren Speichergrenzwert abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="825d2-107">The runtime whose memory limit is to be retrieved.</span></span>  
  
 `memoryLimit`  
 <span data-ttu-id="825d2-108">Die aktuelle Speichergrenze der Laufzeit in Bytes oder-1, wenn kein Grenzwert festgesetzt wurde.</span><span class="sxs-lookup"><span data-stu-id="825d2-108">The runtime's current memory limit, in bytes, or -1 if no limit has been set.</span></span>  
  
## <span data-ttu-id="825d2-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="825d2-109">Return Value</span></span>  
 <span data-ttu-id="825d2-110">Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="825d2-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="825d2-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="825d2-111">Remarks</span></span>  
 <span data-ttu-id="825d2-112">Die Speichergrenze einer Runtime kann immer abgerufen werden, unabhängig davon, ob die Laufzeit in einem anderen Thread aktiv ist oder nicht.</span><span class="sxs-lookup"><span data-stu-id="825d2-112">The memory limit of a runtime can be always be retrieved, regardless of whether or not the runtime is active on another thread.</span></span>  
  
## <span data-ttu-id="825d2-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="825d2-113">Requirements</span></span>  
 <span data-ttu-id="825d2-114">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="825d2-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="825d2-115">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="825d2-115">See Also</span></span>  
 [<span data-ttu-id="825d2-116">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="825d2-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
