---
description: Vergleichen Sie zwei JavaScript-Werte für die strenge Gleichheit.
title: JsStrictEquals-Funktion | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsStrictEquals
helpviewer_keywords:
- JsStrictEquals function
ms.assetid: b35bc655-7ff8-496a-b678-8950bb976047
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: b7f2b7a66c32428100f0c0d0f9db6150559ed7a2
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10568300"
---
# <span data-ttu-id="cd296-103">JsStrictEquals-Funktion</span><span class="sxs-lookup"><span data-stu-id="cd296-103">JsStrictEquals Function</span></span>
<span data-ttu-id="cd296-104">Vergleichen Sie zwei JavaScript-Werte für die strenge Gleichheit.</span><span class="sxs-lookup"><span data-stu-id="cd296-104">Compare two JavaScript values for strict equality.</span></span>  
  
## <span data-ttu-id="cd296-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="cd296-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsStrictEquals(  
   _In_ JsValueRef object1,  
   _In_ JsValueRef object2,  
   _Out_ bool *result  
);  
```  
  
#### <span data-ttu-id="cd296-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="cd296-106">Parameters</span></span>  
 `object1`  
 <span data-ttu-id="cd296-107">Das erste zu vergleichende Objekt.</span><span class="sxs-lookup"><span data-stu-id="cd296-107">The first object to compare.</span></span>  
  
 `object2`  
 <span data-ttu-id="cd296-108">Das zweite zu vergleichende Objekt.</span><span class="sxs-lookup"><span data-stu-id="cd296-108">The second object to compare.</span></span>  
  
 `result`  
 <span data-ttu-id="cd296-109">Gibt an, ob die Werte strikt gleich sind.</span><span class="sxs-lookup"><span data-stu-id="cd296-109">Whether the values are strictly equal.</span></span>  
  
## <span data-ttu-id="cd296-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cd296-110">Return Value</span></span>  
 <span data-ttu-id="cd296-111">Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="cd296-111">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="cd296-112">Hinweise</span><span class="sxs-lookup"><span data-stu-id="cd296-112">Remarks</span></span>  
 <span data-ttu-id="cd296-113">Diese Funktion entspricht dem `===` Operator in JavaScript.</span><span class="sxs-lookup"><span data-stu-id="cd296-113">This function is equivalent to the `===` operator in Javascript.</span></span>  
  
 <span data-ttu-id="cd296-114">Erfordert einen aktiven Skriptkontext.</span><span class="sxs-lookup"><span data-stu-id="cd296-114">Requires an active script context.</span></span>  
  
## <span data-ttu-id="cd296-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cd296-115">Requirements</span></span>  
 <span data-ttu-id="cd296-116">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="cd296-116">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="cd296-117">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="cd296-117">See Also</span></span>  
 [<span data-ttu-id="cd296-118">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="cd296-118">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)