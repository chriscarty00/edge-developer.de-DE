---
description: Benutzer implementierte Rückruf Routine für Speicher Zuordnungs Ereignisse.
title: JsMemoryAllocationCallback typedef | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 511babc7-3caa-4ee5-82a2-943bbd34db8d
caps.latest.revision: 7
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: b11b3d076c01dbfcae190fd665528323d6f8b987
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10567222"
---
# <span data-ttu-id="10fc7-103">JsMemoryAllocationCallback typedef</span><span class="sxs-lookup"><span data-stu-id="10fc7-103">JsMemoryAllocationCallback Typedef</span></span>
<span data-ttu-id="10fc7-104">Benutzer implementierte Rückruf Routine für Speicher Zuordnungs Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="10fc7-104">User implemented callback routine for memory allocation events.</span></span>  
  
## <span data-ttu-id="10fc7-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="10fc7-105">Syntax</span></span>  
  
```cpp  
typedef bool (CALLBACK * JsMemoryAllocationCallback)(  
   _In_opt_ void *callbackState,  
   _In_ JsMemoryEventType allocationEvent,  
   _In_ size_t allocationSize  
);  
```  
  
#### <span data-ttu-id="10fc7-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="10fc7-106">Parameters</span></span>  
 <span data-ttu-id="10fc7-107">callbackState</span><span class="sxs-lookup"><span data-stu-id="10fc7-107">callbackState</span></span>  
 <span data-ttu-id="10fc7-108">Der Zustand, der an JsSetRuntimeMemoryAllocationCallback übergeben wurde.</span><span class="sxs-lookup"><span data-stu-id="10fc7-108">The state passed to JsSetRuntimeMemoryAllocationCallback.</span></span>  
  
 <span data-ttu-id="10fc7-109">allocationEvent</span><span class="sxs-lookup"><span data-stu-id="10fc7-109">allocationEvent</span></span>  
 <span data-ttu-id="10fc7-110">Der Typ des Typen Zuordnungs Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="10fc7-110">The type of type allocation event.</span></span>  
  
 <span data-ttu-id="10fc7-111">verlagern</span><span class="sxs-lookup"><span data-stu-id="10fc7-111">allocationSize</span></span>  
 <span data-ttu-id="10fc7-112">Die Größe der Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="10fc7-112">The size of the allocation.</span></span>  
  
## <span data-ttu-id="10fc7-113">Eigenschaftswert/Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="10fc7-113">Property Value/Return Value</span></span>  
 <span data-ttu-id="10fc7-114">Für das JsMemoryAllocate-Ereignis ermöglicht die Rückgabe von true der Laufzeit, die Zuweisung fortzusetzen.</span><span class="sxs-lookup"><span data-stu-id="10fc7-114">For the JsMemoryAllocate event, returning true allows the runtime to continue with allocation.</span></span> <span data-ttu-id="10fc7-115">Zurückgeben von false gibt an, dass die Zuordnungsanforderung abgelehnt wurde.</span><span class="sxs-lookup"><span data-stu-id="10fc7-115">Returning false indicates the allocation request is rejected.</span></span> <span data-ttu-id="10fc7-116">Der Rückgabewert wird bei anderen Zuordnungs Ereignissen ignoriert.</span><span class="sxs-lookup"><span data-stu-id="10fc7-116">The return value is ignored for other allocation events.</span></span>  
  
## <span data-ttu-id="10fc7-117">Hinweise</span><span class="sxs-lookup"><span data-stu-id="10fc7-117">Remarks</span></span>  
 <span data-ttu-id="10fc7-118">Verwenden Sie JsSetRuntimeMemoryAllocationCallback, um diesen Rückruf zu registrieren.</span><span class="sxs-lookup"><span data-stu-id="10fc7-118">Use JsSetRuntimeMemoryAllocationCallback to register this callback.</span></span>  
  
## <span data-ttu-id="10fc7-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="10fc7-119">Requirements</span></span>  
 <span data-ttu-id="10fc7-120">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="10fc7-120">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="10fc7-121">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="10fc7-121">See Also</span></span>  
 [<span data-ttu-id="10fc7-122">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="10fc7-122">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)