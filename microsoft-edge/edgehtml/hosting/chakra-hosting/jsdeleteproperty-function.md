---
description: Löscht die Eigenschaft eines Objekts.
title: JsDeleteProperty-Funktion | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsDeleteProperty
helpviewer_keywords:
- JsDeleteProperty function
ms.assetid: 0f6ac6a7-3576-42f5-98d0-1c06542c8149
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 55089bd4cff7ef4d58bcce1d7531d4ca1c7381ae
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233583"
---
# <span data-ttu-id="4d9ff-103">JsDeleteProperty Funktion</span><span class="sxs-lookup"><span data-stu-id="4d9ff-103">JsDeleteProperty Function</span></span>

<span data-ttu-id="4d9ff-104">Löscht die Eigenschaft eines Objekts.</span><span class="sxs-lookup"><span data-stu-id="4d9ff-104">Deletes an object's property.</span></span>  
  
## <span data-ttu-id="4d9ff-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="4d9ff-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsDeleteProperty(  
   _In_ JsValueRef object,  
   _In_ JsPropertyIdRef propertyId,  
   _In_ bool useStrictRules,  
   _Out_ JsValueRef *result  
);  
```  
  
#### <span data-ttu-id="4d9ff-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="4d9ff-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="4d9ff-107">Das Objekt, das die Eigenschaft enthält.</span><span class="sxs-lookup"><span data-stu-id="4d9ff-107">The object that contains the property.</span></span>  
  
 `propertyId`  
 <span data-ttu-id="4d9ff-108">Die ID der Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="4d9ff-108">The ID of the property.</span></span>  
  
 `useStrictRules`  
 <span data-ttu-id="4d9ff-109">Der Eigenschaftensatz sollte strikte Regeln für den Modus befolgen.</span><span class="sxs-lookup"><span data-stu-id="4d9ff-109">The property set should follow strict mode rules.</span></span>  
  
 `result`  
 <span data-ttu-id="4d9ff-110">Gibt an, ob die Eigenschaft gelöscht wurde.</span><span class="sxs-lookup"><span data-stu-id="4d9ff-110">Whether the property was deleted.</span></span>  
  
## <span data-ttu-id="4d9ff-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4d9ff-111">Return Value</span></span>  
 <span data-ttu-id="4d9ff-112">Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="4d9ff-112">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="4d9ff-113">Hinweise</span><span class="sxs-lookup"><span data-stu-id="4d9ff-113">Remarks</span></span>  
 <span data-ttu-id="4d9ff-114">Erfordert einen aktiven Skriptkontext.</span><span class="sxs-lookup"><span data-stu-id="4d9ff-114">Requires an active script context.</span></span>  
  
## <span data-ttu-id="4d9ff-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4d9ff-115">Requirements</span></span>  
 <span data-ttu-id="4d9ff-116">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="4d9ff-116">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="4d9ff-117">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="4d9ff-117">See Also</span></span>  
 [<span data-ttu-id="4d9ff-118">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="4d9ff-118">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
