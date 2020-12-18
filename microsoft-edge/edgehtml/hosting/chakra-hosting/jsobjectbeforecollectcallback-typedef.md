---
description: Ein Rückruf, der vor dem Sammeln eines Objekts aufgerufen wird.
title: JsObjectBeforeCollectCallback typedef | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: f21a064a-579f-44cb-9d21-76b62e8c18f5
caps.latest.revision: 3
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 4c24385ec5e15919719ffb0ae71c8adf39c1724c
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11234089"
---
# <span data-ttu-id="56526-103">JsObjectBeforeCollectCallback Typedef</span><span class="sxs-lookup"><span data-stu-id="56526-103">JsObjectBeforeCollectCallback Typedef</span></span>

<span data-ttu-id="56526-104">Ein Rückruf, der vor dem Sammeln eines Objekts aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="56526-104">A callback called before collecting an object.</span></span>  
  
## <span data-ttu-id="56526-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="56526-105">Syntax</span></span>  
  
```cpp  
typedef void (CALLBACK *JsObjectBeforeCollectCallback)(  
  _In_ JsRef ref,  
  _In_opt_ void *callbackState  
);  
```  
  
#### <span data-ttu-id="56526-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="56526-106">Parameters</span></span>  
 `ref`  
 <span data-ttu-id="56526-107">Das Objekt, das erfasst werden soll.</span><span class="sxs-lookup"><span data-stu-id="56526-107">The object to be collected.</span></span>  
  
 `callbackState`  
 <span data-ttu-id="56526-108">Der Zustand, der übergeben wird `JsSetObjectBeforeCollectCallback` .</span><span class="sxs-lookup"><span data-stu-id="56526-108">The state passed to `JsSetObjectBeforeCollectCallback`.</span></span>  
  
## <span data-ttu-id="56526-109">Hinweise</span><span class="sxs-lookup"><span data-stu-id="56526-109">Remarks</span></span>  
 <span data-ttu-id="56526-110">Diese API wird nur im EdgeHTML-Modus unterstützt.</span><span class="sxs-lookup"><span data-stu-id="56526-110">This API is supported only in EdgeHTML mode.</span></span>  
  
## <span data-ttu-id="56526-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="56526-111">Requirements</span></span>  
 <span data-ttu-id="56526-112">jsrt. h</span><span class="sxs-lookup"><span data-stu-id="56526-112">jsrt.h</span></span>  
  
## <span data-ttu-id="56526-113">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="56526-113">See Also</span></span>  
 [<span data-ttu-id="56526-114">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="56526-114">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
