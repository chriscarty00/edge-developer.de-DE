---
description: Vergleichen Sie zwei JavaScript-Werte für die strenge Gleichheit.
title: JsStrictEquals-Funktion | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsStrictEquals
helpviewer_keywords:
- JsStrictEquals function
ms.assetid: b35bc655-7ff8-496a-b678-8950bb976047
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 98af1629129986cc21cafe5660d3155e031919dc
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233909"
---
# <span data-ttu-id="baade-103">JsStrictEquals Funktion</span><span class="sxs-lookup"><span data-stu-id="baade-103">JsStrictEquals Function</span></span>

<span data-ttu-id="baade-104">Vergleichen Sie zwei JavaScript-Werte für die strenge Gleichheit.</span><span class="sxs-lookup"><span data-stu-id="baade-104">Compare two JavaScript values for strict equality.</span></span>  
  
## <span data-ttu-id="baade-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="baade-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsStrictEquals(  
   _In_ JsValueRef object1,  
   _In_ JsValueRef object2,  
   _Out_ bool *result  
);  
```  
  
#### <span data-ttu-id="baade-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="baade-106">Parameters</span></span>  
 `object1`  
 <span data-ttu-id="baade-107">Das erste zu vergleichende Objekt.</span><span class="sxs-lookup"><span data-stu-id="baade-107">The first object to compare.</span></span>  
  
 `object2`  
 <span data-ttu-id="baade-108">Das zweite zu vergleichende Objekt.</span><span class="sxs-lookup"><span data-stu-id="baade-108">The second object to compare.</span></span>  
  
 `result`  
 <span data-ttu-id="baade-109">Gibt an, ob die Werte strikt gleich sind.</span><span class="sxs-lookup"><span data-stu-id="baade-109">Whether the values are strictly equal.</span></span>  
  
## <span data-ttu-id="baade-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="baade-110">Return Value</span></span>  
 <span data-ttu-id="baade-111">Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="baade-111">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="baade-112">Hinweise</span><span class="sxs-lookup"><span data-stu-id="baade-112">Remarks</span></span>  
 <span data-ttu-id="baade-113">Diese Funktion entspricht dem `===` Operator in JavaScript.</span><span class="sxs-lookup"><span data-stu-id="baade-113">This function is equivalent to the `===` operator in Javascript.</span></span>  
  
 <span data-ttu-id="baade-114">Erfordert einen aktiven Skriptkontext.</span><span class="sxs-lookup"><span data-stu-id="baade-114">Requires an active script context.</span></span>  
  
## <span data-ttu-id="baade-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="baade-115">Requirements</span></span>  
 <span data-ttu-id="baade-116">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="baade-116">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="baade-117">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="baade-117">See Also</span></span>  
 [<span data-ttu-id="baade-118">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="baade-118">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
