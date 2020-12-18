---
description: Ruft einen Eigenschaftendeskriptor für die eigene Eigenschaft eines Objekts ab.
title: JsGetOwnPropertyDescriptor-Funktion | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsGetOwnPropertyDescriptor
helpviewer_keywords:
- JsGetOwnPropertyDescriptor function
ms.assetid: 44c417ce-ab63-44eb-a0ab-19838e3ab34f
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 05c7a58fa12d7ca8013c512f40031963ebc8ac18
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233947"
---
# <span data-ttu-id="346fc-103">JsGetOwnPropertyDescriptor Funktion</span><span class="sxs-lookup"><span data-stu-id="346fc-103">JsGetOwnPropertyDescriptor Function</span></span>

<span data-ttu-id="346fc-104">Ruft einen Eigenschaftendeskriptor für die eigene Eigenschaft eines Objekts ab.</span><span class="sxs-lookup"><span data-stu-id="346fc-104">Gets a property descriptor for an object's own property.</span></span>  
  
## <span data-ttu-id="346fc-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="346fc-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetOwnPropertyDescriptor(  
   _In_ JsValueRef object,  
   _In_ JsPropertyIdRef propertyId,  
   _Out_ JsValueRef *propertyDescriptor  
);  
```  
  
#### <span data-ttu-id="346fc-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="346fc-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="346fc-107">Das Objekt, das die Eigenschaft aufweist.</span><span class="sxs-lookup"><span data-stu-id="346fc-107">The object that has the property.</span></span>  
  
 `propertyId`  
 <span data-ttu-id="346fc-108">Die ID der Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="346fc-108">The ID of the property.</span></span>  
  
 `propertyDescriptor`  
 <span data-ttu-id="346fc-109">Der Eigenschaftendeskriptor.</span><span class="sxs-lookup"><span data-stu-id="346fc-109">The property descriptor.</span></span>  
  
## <span data-ttu-id="346fc-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="346fc-110">Return Value</span></span>  
 <span data-ttu-id="346fc-111">Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="346fc-111">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="346fc-112">Hinweise</span><span class="sxs-lookup"><span data-stu-id="346fc-112">Remarks</span></span>  
 <span data-ttu-id="346fc-113">Erfordert einen aktiven Skriptkontext.</span><span class="sxs-lookup"><span data-stu-id="346fc-113">Requires an active script context.</span></span>  
  
## <span data-ttu-id="346fc-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="346fc-114">Requirements</span></span>  
 <span data-ttu-id="346fc-115">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="346fc-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="346fc-116">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="346fc-116">See Also</span></span>  
 [<span data-ttu-id="346fc-117">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="346fc-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
