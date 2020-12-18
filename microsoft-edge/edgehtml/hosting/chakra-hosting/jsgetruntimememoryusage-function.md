---
description: Ruft die aktuelle Speicherauslastung für eine Laufzeit ab.
title: JsGetRuntimeMemoryUsage-Funktion | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsGetRuntimeMemoryUsage
helpviewer_keywords:
- JsGetRuntimeMemoryUsage function
ms.assetid: b9bd4146-bfbc-4cb1-a0e9-a0ded7fb09bd
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: a9c8d59e8cf73ad178f539f2f9f0ed191ceb47fd
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11234323"
---
# <span data-ttu-id="2c619-103">JsGetRuntimeMemoryUsage Funktion</span><span class="sxs-lookup"><span data-stu-id="2c619-103">JsGetRuntimeMemoryUsage Function</span></span>

<span data-ttu-id="2c619-104">Ruft die aktuelle Speicherauslastung für eine Laufzeit ab.</span><span class="sxs-lookup"><span data-stu-id="2c619-104">Gets the current memory usage for a runtime.</span></span>  
  
## <span data-ttu-id="2c619-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="2c619-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetRuntimeMemoryUsage(  
   _In_ JsRuntimeHandle runtime,  
   _Out_ size_t *memoryUsage  
);  
```  
  
#### <span data-ttu-id="2c619-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="2c619-106">Parameters</span></span>  
 `runtime`  
 <span data-ttu-id="2c619-107">Die Laufzeit, deren Speicherauslastung abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="2c619-107">The runtime whose memory usage is to be retrieved.</span></span>  
  
 `memoryUsage`  
 <span data-ttu-id="2c619-108">Die aktuelle Speicherauslastung der Common Language Runtime in Bytes.</span><span class="sxs-lookup"><span data-stu-id="2c619-108">The runtime's current memory usage, in bytes.</span></span>  
  
## <span data-ttu-id="2c619-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2c619-109">Return Value</span></span>  
 <span data-ttu-id="2c619-110">Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="2c619-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="2c619-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="2c619-111">Remarks</span></span>  
 <span data-ttu-id="2c619-112">Die Speicherauslastung kann immer abgerufen werden, unabhängig davon, ob die Laufzeit in einem anderen Thread aktiv ist oder nicht.</span><span class="sxs-lookup"><span data-stu-id="2c619-112">Memory usage can be always be retrieved, regardless of whether or not the runtime is active on another thread.</span></span>  
  
## <span data-ttu-id="2c619-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2c619-113">Requirements</span></span>  
 <span data-ttu-id="2c619-114">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="2c619-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="2c619-115">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="2c619-115">See Also</span></span>  
 [<span data-ttu-id="2c619-116">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="2c619-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
