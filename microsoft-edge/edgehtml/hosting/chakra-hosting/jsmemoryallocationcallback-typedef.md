---
description: Benutzer implementierte Rückruf Routine für Speicher Zuordnungs Ereignisse.
title: JsMemoryAllocationCallback typedef | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 511babc7-3caa-4ee5-82a2-943bbd34db8d
caps.latest.revision: 7
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 22b5cc0fe5a2c8b49f71c91d28f95ba29af37849
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233750"
---
# <span data-ttu-id="cf232-103">JsMemoryAllocationCallback Typedef</span><span class="sxs-lookup"><span data-stu-id="cf232-103">JsMemoryAllocationCallback Typedef</span></span>

<span data-ttu-id="cf232-104">Benutzer implementierte Rückruf Routine für Speicher Zuordnungs Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="cf232-104">User implemented callback routine for memory allocation events.</span></span>  
  
## <span data-ttu-id="cf232-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="cf232-105">Syntax</span></span>  
  
```cpp  
typedef bool (CALLBACK * JsMemoryAllocationCallback)(  
   _In_opt_ void *callbackState,  
   _In_ JsMemoryEventType allocationEvent,  
   _In_ size_t allocationSize  
);  
```  
  
#### <span data-ttu-id="cf232-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="cf232-106">Parameters</span></span>  
 <span data-ttu-id="cf232-107">callbackState</span><span class="sxs-lookup"><span data-stu-id="cf232-107">callbackState</span></span>  
 <span data-ttu-id="cf232-108">Der Zustand, der an JsSetRuntimeMemoryAllocationCallback übergeben wurde.</span><span class="sxs-lookup"><span data-stu-id="cf232-108">The state passed to JsSetRuntimeMemoryAllocationCallback.</span></span>  
  
 <span data-ttu-id="cf232-109">allocationEvent</span><span class="sxs-lookup"><span data-stu-id="cf232-109">allocationEvent</span></span>  
 <span data-ttu-id="cf232-110">Der Typ des Typen Zuordnungs Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="cf232-110">The type of type allocation event.</span></span>  
  
 <span data-ttu-id="cf232-111">verlagern</span><span class="sxs-lookup"><span data-stu-id="cf232-111">allocationSize</span></span>  
 <span data-ttu-id="cf232-112">Die Größe der Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="cf232-112">The size of the allocation.</span></span>  
  
## <span data-ttu-id="cf232-113">Eigenschaftswert/Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cf232-113">Property Value/Return Value</span></span>  
 <span data-ttu-id="cf232-114">Für das JsMemoryAllocate-Ereignis ermöglicht die Rückgabe von true der Laufzeit, die Zuweisung fortzusetzen.</span><span class="sxs-lookup"><span data-stu-id="cf232-114">For the JsMemoryAllocate event, returning true allows the runtime to continue with allocation.</span></span> <span data-ttu-id="cf232-115">Zurückgeben von false gibt an, dass die Zuordnungsanforderung abgelehnt wurde.</span><span class="sxs-lookup"><span data-stu-id="cf232-115">Returning false indicates the allocation request is rejected.</span></span> <span data-ttu-id="cf232-116">Der Rückgabewert wird bei anderen Zuordnungs Ereignissen ignoriert.</span><span class="sxs-lookup"><span data-stu-id="cf232-116">The return value is ignored for other allocation events.</span></span>  
  
## <span data-ttu-id="cf232-117">Hinweise</span><span class="sxs-lookup"><span data-stu-id="cf232-117">Remarks</span></span>  
 <span data-ttu-id="cf232-118">Verwenden Sie JsSetRuntimeMemoryAllocationCallback, um diesen Rückruf zu registrieren.</span><span class="sxs-lookup"><span data-stu-id="cf232-118">Use JsSetRuntimeMemoryAllocationCallback to register this callback.</span></span>  
  
## <span data-ttu-id="cf232-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cf232-119">Requirements</span></span>  
 <span data-ttu-id="cf232-120">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="cf232-120">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="cf232-121">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="cf232-121">See Also</span></span>  
 [<span data-ttu-id="cf232-122">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="cf232-122">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
