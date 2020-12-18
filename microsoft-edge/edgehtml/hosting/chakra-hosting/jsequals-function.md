---
description: Vergleichen Sie zwei JavaScript-Werte für Gleichheit.
title: JsEquals-Funktion | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsEquals
helpviewer_keywords:
- JsEquals function
ms.assetid: 8377a7b6-12ff-43e4-8cc8-5a5a198a168b
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 88f906419e73ed0de6ddde0a872becbd18908997
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11234326"
---
# <span data-ttu-id="9eed9-103">JsEquals Funktion</span><span class="sxs-lookup"><span data-stu-id="9eed9-103">JsEquals Function</span></span>

<span data-ttu-id="9eed9-104">Vergleichen Sie zwei JavaScript-Werte für Gleichheit.</span><span class="sxs-lookup"><span data-stu-id="9eed9-104">Compare two JavaScript values for equality.</span></span>  
  
## <span data-ttu-id="9eed9-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="9eed9-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsEquals(  
   _In_ JsValueRef object1,  
   _In_ JsValueRef object2,  
   _Out_ bool *result  
);  
```  
  
#### <span data-ttu-id="9eed9-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="9eed9-106">Parameters</span></span>  
 `object1`  
 <span data-ttu-id="9eed9-107">Das erste zu vergleichende Objekt.</span><span class="sxs-lookup"><span data-stu-id="9eed9-107">The first object to compare.</span></span>  
  
 `object2`  
 <span data-ttu-id="9eed9-108">Das zweite zu vergleichende Objekt.</span><span class="sxs-lookup"><span data-stu-id="9eed9-108">The second object to compare.</span></span>  
  
 `result`  
 <span data-ttu-id="9eed9-109">Gibt an, ob die Werte gleich sind.</span><span class="sxs-lookup"><span data-stu-id="9eed9-109">Whether the values are equal.</span></span>  
  
## <span data-ttu-id="9eed9-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9eed9-110">Return Value</span></span>  
 <span data-ttu-id="9eed9-111">Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="9eed9-111">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="9eed9-112">Hinweise</span><span class="sxs-lookup"><span data-stu-id="9eed9-112">Remarks</span></span>  
 <span data-ttu-id="9eed9-113">Diese Funktion entspricht dem `==` Operator in JavaScript.</span><span class="sxs-lookup"><span data-stu-id="9eed9-113">This function is equivalent to the `==` operator in Javascript.</span></span>  
  
 <span data-ttu-id="9eed9-114">Erfordert einen aktiven Skriptkontext.</span><span class="sxs-lookup"><span data-stu-id="9eed9-114">Requires an active script context.</span></span>  
  
## <span data-ttu-id="9eed9-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9eed9-115">Requirements</span></span>  
 <span data-ttu-id="9eed9-116">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="9eed9-116">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="9eed9-117">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="9eed9-117">See Also</span></span>  
 [<span data-ttu-id="9eed9-118">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="9eed9-118">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
