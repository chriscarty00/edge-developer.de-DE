---
description: Führt eine vollständige Garbage Collection aus.
title: JsCollectGarbage-Funktion | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsCollectGarbage
helpviewer_keywords:
- JsCollectGarbage function
ms.assetid: 995c79a5-6e18-45be-81ff-2a5d3348edb8
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: c551ddf119ec0aa349fcd756f6001d92dbbb0faa
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233768"
---
# <span data-ttu-id="9ca33-103">JsCollectGarbage Funktion</span><span class="sxs-lookup"><span data-stu-id="9ca33-103">JsCollectGarbage Function</span></span>

<span data-ttu-id="9ca33-104">Führt eine vollständige Garbage Collection aus.</span><span class="sxs-lookup"><span data-stu-id="9ca33-104">Performs a full garbage collection.</span></span>  
  
## <span data-ttu-id="9ca33-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="9ca33-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsCollectGarbage(  
   _In_ JsRuntimeHandle runtime  
);  
```  
  
#### <span data-ttu-id="9ca33-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="9ca33-106">Parameters</span></span>  
 `runtime`  
 <span data-ttu-id="9ca33-107">Die Laufzeit, in der die Garbage Collection durchgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9ca33-107">The runtime in which the garbage collection will be performed.</span></span>  
  
## <span data-ttu-id="9ca33-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9ca33-108">Return Value</span></span>  
 <span data-ttu-id="9ca33-109">Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="9ca33-109">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="9ca33-110">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9ca33-110">Requirements</span></span>  
 <span data-ttu-id="9ca33-111">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="9ca33-111">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="9ca33-112">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="9ca33-112">See Also</span></span>  
 [<span data-ttu-id="9ca33-113">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="9ca33-113">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
