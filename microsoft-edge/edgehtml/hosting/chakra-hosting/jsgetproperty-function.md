---
description: Ruft die Eigenschaft eines Objekts ab.
title: JsGetProperty-Funktion | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsGetProperty
helpviewer_keywords:
- JsGetProperty function
ms.assetid: 606bc14f-e849-4f88-a148-6660e923c07b
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: e5731fa3f889fc1b182f88e37ae90c96d3825402
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233556"
---
# <span data-ttu-id="ed577-103">JsGetProperty Funktion</span><span class="sxs-lookup"><span data-stu-id="ed577-103">JsGetProperty Function</span></span>

<span data-ttu-id="ed577-104">Ruft die Eigenschaft eines Objekts ab.</span><span class="sxs-lookup"><span data-stu-id="ed577-104">Gets an object's property.</span></span>  
  
## <span data-ttu-id="ed577-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ed577-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetProperty(  
   _In_ JsValueRef object,  
   _In_ JsPropertyIdRef propertyId,  
   _Out_ JsValueRef *value  
);  
```  
  
#### <span data-ttu-id="ed577-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ed577-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="ed577-107">Das Objekt, das die Eigenschaft enthält.</span><span class="sxs-lookup"><span data-stu-id="ed577-107">The object that contains the property.</span></span>  
  
 `propertyId`  
 <span data-ttu-id="ed577-108">Die ID der Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="ed577-108">The ID of the property.</span></span>  
  
 `value`  
 <span data-ttu-id="ed577-109">Der Wert der Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="ed577-109">The value of the property.</span></span>  
  
## <span data-ttu-id="ed577-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ed577-110">Return Value</span></span>  
 <span data-ttu-id="ed577-111">Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="ed577-111">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="ed577-112">Hinweise</span><span class="sxs-lookup"><span data-stu-id="ed577-112">Remarks</span></span>  
 <span data-ttu-id="ed577-113">Erfordert einen aktiven Skriptkontext.</span><span class="sxs-lookup"><span data-stu-id="ed577-113">Requires an active script context.</span></span>  
  
## <span data-ttu-id="ed577-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ed577-114">Requirements</span></span>  
 <span data-ttu-id="ed577-115">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="ed577-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="ed577-116">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="ed577-116">See Also</span></span>  
 [<span data-ttu-id="ed577-117">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="ed577-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
