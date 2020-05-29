---
description: Führt eine vollständige Garbage Collection aus.
title: JsCollectGarbage-Funktion | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsCollectGarbage
helpviewer_keywords:
- JsCollectGarbage function
ms.assetid: 995c79a5-6e18-45be-81ff-2a5d3348edb8
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 1702ad960a0a2f366e97b8a994abd0700cec50e7
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10567326"
---
# <span data-ttu-id="6114d-103">JsCollectGarbage-Funktion</span><span class="sxs-lookup"><span data-stu-id="6114d-103">JsCollectGarbage Function</span></span>
<span data-ttu-id="6114d-104">Führt eine vollständige Garbage Collection aus.</span><span class="sxs-lookup"><span data-stu-id="6114d-104">Performs a full garbage collection.</span></span>  
  
## <span data-ttu-id="6114d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="6114d-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsCollectGarbage(  
   _In_ JsRuntimeHandle runtime  
);  
```  
  
#### <span data-ttu-id="6114d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="6114d-106">Parameters</span></span>  
 `runtime`  
 <span data-ttu-id="6114d-107">Die Laufzeit, in der die Garbage Collection durchgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6114d-107">The runtime in which the garbage collection will be performed.</span></span>  
  
## <span data-ttu-id="6114d-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6114d-108">Return Value</span></span>  
 <span data-ttu-id="6114d-109">Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="6114d-109">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="6114d-110">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6114d-110">Requirements</span></span>  
 <span data-ttu-id="6114d-111">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="6114d-111">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="6114d-112">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="6114d-112">See Also</span></span>  
 [<span data-ttu-id="6114d-113">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="6114d-113">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)