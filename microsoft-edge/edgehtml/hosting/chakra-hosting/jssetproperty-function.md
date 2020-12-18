---
description: Fügt die Eigenschaft eines Objekts ein.
title: JsSetProperty-Funktion | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsSetProperty
helpviewer_keywords:
- JsSetProperty function
ms.assetid: 2c36bebf-ec86-425c-8131-2dd75fd30f40
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 29c3e04fc240bd63fc755c6727752d053b94484d
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233962"
---
# <span data-ttu-id="2d787-103">JsSetProperty Funktion</span><span class="sxs-lookup"><span data-stu-id="2d787-103">JsSetProperty Function</span></span>

<span data-ttu-id="2d787-104">Fügt die Eigenschaft eines Objekts ein.</span><span class="sxs-lookup"><span data-stu-id="2d787-104">Puts an object's property.</span></span>  
  
## <span data-ttu-id="2d787-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="2d787-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsSetProperty(  
   _In_ JsValueRef object,  
   _In_ JsPropertyIdRef propertyId,  
   _In_ JsValueRef value,  
   _In_ bool useStrictRules  
);  
```  
  
#### <span data-ttu-id="2d787-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="2d787-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="2d787-107">Das Objekt, das die Eigenschaft enthält.</span><span class="sxs-lookup"><span data-stu-id="2d787-107">The object that contains the property.</span></span>  
  
 `propertyId`  
 <span data-ttu-id="2d787-108">Die ID der Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="2d787-108">The ID of the property.</span></span>  
  
 `value`  
 <span data-ttu-id="2d787-109">Der neue Wert der Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="2d787-109">The new value of the property.</span></span>  
  
 `useStrictRules`  
 <span data-ttu-id="2d787-110">Der Eigenschaftensatz sollte strikte Regeln für den Modus befolgen.</span><span class="sxs-lookup"><span data-stu-id="2d787-110">The property set should follow strict mode rules.</span></span>  
  
## <span data-ttu-id="2d787-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2d787-111">Return Value</span></span>  
 <span data-ttu-id="2d787-112">Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="2d787-112">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="2d787-113">Hinweise</span><span class="sxs-lookup"><span data-stu-id="2d787-113">Remarks</span></span>  
 <span data-ttu-id="2d787-114">Erfordert einen aktiven Skriptkontext.</span><span class="sxs-lookup"><span data-stu-id="2d787-114">Requires an active script context.</span></span>  
  
## <span data-ttu-id="2d787-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2d787-115">Requirements</span></span>  
 <span data-ttu-id="2d787-116">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="2d787-116">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="2d787-117">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="2d787-117">See Also</span></span>  
 [<span data-ttu-id="2d787-118">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="2d787-118">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
