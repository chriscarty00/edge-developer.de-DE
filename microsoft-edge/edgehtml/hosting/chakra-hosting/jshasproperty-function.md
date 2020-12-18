---
description: Bestimmt, ob ein Objekt eine Eigenschaft aufweist.
title: JsHasProperty-Funktion | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsHasProperty
helpviewer_keywords:
- JsHasProperty function
ms.assetid: 26c94c3d-aae6-4257-8644-df63c7e714fb
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: e45ecfaafb06c49a6a3773eb798ee93a19fd6d6e
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233961"
---
# <span data-ttu-id="9ddb5-103">JsHasProperty Funktion</span><span class="sxs-lookup"><span data-stu-id="9ddb5-103">JsHasProperty Function</span></span>

<span data-ttu-id="9ddb5-104">Bestimmt, ob ein Objekt eine Eigenschaft aufweist.</span><span class="sxs-lookup"><span data-stu-id="9ddb5-104">Determines whether an object has a property.</span></span>  
  
## <span data-ttu-id="9ddb5-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="9ddb5-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsHasProperty(  
   _In_ JsValueRef object,  
   _In_ JsPropertyIdRef propertyId,  
   _Out_ bool *hasProperty  
);  
```  
  
#### <span data-ttu-id="9ddb5-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="9ddb5-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="9ddb5-107">Das Objekt, das die Eigenschaft enthalten kann.</span><span class="sxs-lookup"><span data-stu-id="9ddb5-107">The object that may contain the property.</span></span>  
  
 `propertyId`  
 <span data-ttu-id="9ddb5-108">Die ID der Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="9ddb5-108">The ID of the property.</span></span>  
  
 `hasProperty`  
 <span data-ttu-id="9ddb5-109">Gibt an, ob das Objekt (oder ein Prototyp) die Eigenschaft aufweist.</span><span class="sxs-lookup"><span data-stu-id="9ddb5-109">Whether the object (or a prototype) has the property.</span></span>  
  
## <span data-ttu-id="9ddb5-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9ddb5-110">Return Value</span></span>  
 <span data-ttu-id="9ddb5-111">Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="9ddb5-111">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="9ddb5-112">Hinweise</span><span class="sxs-lookup"><span data-stu-id="9ddb5-112">Remarks</span></span>  
 <span data-ttu-id="9ddb5-113">Erfordert einen aktiven Skriptkontext.</span><span class="sxs-lookup"><span data-stu-id="9ddb5-113">Requires an active script context.</span></span>  
  
## <span data-ttu-id="9ddb5-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9ddb5-114">Requirements</span></span>  
 <span data-ttu-id="9ddb5-115">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="9ddb5-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="9ddb5-116">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="9ddb5-116">See Also</span></span>  
 [<span data-ttu-id="9ddb5-117">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="9ddb5-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
