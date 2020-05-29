---
description: Vergleichen Sie zwei JavaScript-Werte für Gleichheit.
title: JsEquals-Funktion | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsEquals
helpviewer_keywords:
- JsEquals function
ms.assetid: 8377a7b6-12ff-43e4-8cc8-5a5a198a168b
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 84416584a048512ab20754a3b59eb8ec255901c4
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10568401"
---
# <span data-ttu-id="70433-103">JsEquals-Funktion</span><span class="sxs-lookup"><span data-stu-id="70433-103">JsEquals Function</span></span>
<span data-ttu-id="70433-104">Vergleichen Sie zwei JavaScript-Werte für Gleichheit.</span><span class="sxs-lookup"><span data-stu-id="70433-104">Compare two JavaScript values for equality.</span></span>  
  
## <span data-ttu-id="70433-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="70433-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsEquals(  
   _In_ JsValueRef object1,  
   _In_ JsValueRef object2,  
   _Out_ bool *result  
);  
```  
  
#### <span data-ttu-id="70433-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="70433-106">Parameters</span></span>  
 `object1`  
 <span data-ttu-id="70433-107">Das erste zu vergleichende Objekt.</span><span class="sxs-lookup"><span data-stu-id="70433-107">The first object to compare.</span></span>  
  
 `object2`  
 <span data-ttu-id="70433-108">Das zweite zu vergleichende Objekt.</span><span class="sxs-lookup"><span data-stu-id="70433-108">The second object to compare.</span></span>  
  
 `result`  
 <span data-ttu-id="70433-109">Gibt an, ob die Werte gleich sind.</span><span class="sxs-lookup"><span data-stu-id="70433-109">Whether the values are equal.</span></span>  
  
## <span data-ttu-id="70433-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="70433-110">Return Value</span></span>  
 <span data-ttu-id="70433-111">Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="70433-111">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="70433-112">Hinweise</span><span class="sxs-lookup"><span data-stu-id="70433-112">Remarks</span></span>  
 <span data-ttu-id="70433-113">Diese Funktion entspricht dem `==` Operator in JavaScript.</span><span class="sxs-lookup"><span data-stu-id="70433-113">This function is equivalent to the `==` operator in Javascript.</span></span>  
  
 <span data-ttu-id="70433-114">Erfordert einen aktiven Skriptkontext.</span><span class="sxs-lookup"><span data-stu-id="70433-114">Requires an active script context.</span></span>  
  
## <span data-ttu-id="70433-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="70433-115">Requirements</span></span>  
 <span data-ttu-id="70433-116">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="70433-116">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="70433-117">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="70433-117">See Also</span></span>  
 [<span data-ttu-id="70433-118">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="70433-118">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)