---
description: Ein Rückruf, der vor dem Sammeln eines Objekts aufgerufen wird.
title: JsObjectBeforeCollectCallback typedef | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: f21a064a-579f-44cb-9d21-76b62e8c18f5
caps.latest.revision: 3
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 27bbd1aed72cc751397ac4e6734f107612653b66
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10567214"
---
# <span data-ttu-id="214ab-103">JsObjectBeforeCollectCallback typedef</span><span class="sxs-lookup"><span data-stu-id="214ab-103">JsObjectBeforeCollectCallback Typedef</span></span>
<span data-ttu-id="214ab-104">Ein Rückruf, der vor dem Sammeln eines Objekts aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="214ab-104">A callback called before collecting an object.</span></span>  
  
## <span data-ttu-id="214ab-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="214ab-105">Syntax</span></span>  
  
```cpp  
typedef void (CALLBACK *JsObjectBeforeCollectCallback)(  
  _In_ JsRef ref,  
  _In_opt_ void *callbackState  
);  
```  
  
#### <span data-ttu-id="214ab-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="214ab-106">Parameters</span></span>  
 `ref`  
 <span data-ttu-id="214ab-107">Das Objekt, das erfasst werden soll.</span><span class="sxs-lookup"><span data-stu-id="214ab-107">The object to be collected.</span></span>  
  
 `callbackState`  
 <span data-ttu-id="214ab-108">Der Zustand, der übergeben wird `JsSetObjectBeforeCollectCallback` .</span><span class="sxs-lookup"><span data-stu-id="214ab-108">The state passed to `JsSetObjectBeforeCollectCallback`.</span></span>  
  
## <span data-ttu-id="214ab-109">Hinweise</span><span class="sxs-lookup"><span data-stu-id="214ab-109">Remarks</span></span>  
 <span data-ttu-id="214ab-110">Diese API wird nur im EdgeHTML-Modus unterstützt.</span><span class="sxs-lookup"><span data-stu-id="214ab-110">This API is supported only in EdgeHTML mode.</span></span>  
  
## <span data-ttu-id="214ab-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="214ab-111">Requirements</span></span>  
 <span data-ttu-id="214ab-112">jsrt. h</span><span class="sxs-lookup"><span data-stu-id="214ab-112">jsrt.h</span></span>  
  
## <span data-ttu-id="214ab-113">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="214ab-113">See Also</span></span>  
 [<span data-ttu-id="214ab-114">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="214ab-114">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)