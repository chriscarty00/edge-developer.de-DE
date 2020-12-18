---
description: Legt die externen Daten für ein externes Objekt fest.
title: JsSetExternalData-Funktion | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsSetExternalData
helpviewer_keywords:
- JsSetExternalData function
ms.assetid: 94e0ad34-67d7-4f7f-88a3-3b057ef5e4b9
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: f2ebdce4448a14f145ce5aafe6ba412f7db26c17
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11234066"
---
# <span data-ttu-id="d0ac3-103">JsSetExternalData Funktion</span><span class="sxs-lookup"><span data-stu-id="d0ac3-103">JsSetExternalData Function</span></span>

<span data-ttu-id="d0ac3-104">Legt die externen Daten für ein externes Objekt fest.</span><span class="sxs-lookup"><span data-stu-id="d0ac3-104">Sets the external data on an external object.</span></span>  
  
## <span data-ttu-id="d0ac3-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="d0ac3-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsSetExternalData(  
   _In_ JsValueRef object,  
   _In_opt_ void *externalData  
);  
```  
  
#### <span data-ttu-id="d0ac3-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="d0ac3-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="d0ac3-107">Das externe Objekt.</span><span class="sxs-lookup"><span data-stu-id="d0ac3-107">The external object.</span></span>  
  
 `externalData`  
 <span data-ttu-id="d0ac3-108">Die im Objekt gespeicherten externen Daten.</span><span class="sxs-lookup"><span data-stu-id="d0ac3-108">The external data stored in the object.</span></span> <span data-ttu-id="d0ac3-109">Kann NULL sein, wenn keine externen Daten im Objekt gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="d0ac3-109">Can be null if no external data is stored in the object.</span></span>  
  
## <span data-ttu-id="d0ac3-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d0ac3-110">Return Value</span></span>  
 <span data-ttu-id="d0ac3-111">Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="d0ac3-111">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="d0ac3-112">Hinweise</span><span class="sxs-lookup"><span data-stu-id="d0ac3-112">Remarks</span></span>  
 <span data-ttu-id="d0ac3-113">Erfordert einen aktiven Skriptkontext.</span><span class="sxs-lookup"><span data-stu-id="d0ac3-113">Requires an active script context.</span></span>  
  
## <span data-ttu-id="d0ac3-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d0ac3-114">Requirements</span></span>  
 <span data-ttu-id="d0ac3-115">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="d0ac3-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="d0ac3-116">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="d0ac3-116">See Also</span></span>  
 [<span data-ttu-id="d0ac3-117">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="d0ac3-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
