---
description: Ruft den Wert `true` im aktuellen Skriptkontext ab.
title: JsGetTrueValue-Funktion | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsGetTrueValue
helpviewer_keywords:
- JsGetTrueValue function
ms.assetid: c2a56d48-344b-492b-90b8-f570710f8310
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 58798e1e8aab57d626be0c8c878f9be39d0af942
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11234315"
---
# <span data-ttu-id="9ee99-103">JsGetTrueValue Funktion</span><span class="sxs-lookup"><span data-stu-id="9ee99-103">JsGetTrueValue Function</span></span>

<span data-ttu-id="9ee99-104">Ruft den Wert `true` im aktuellen Skriptkontext ab.</span><span class="sxs-lookup"><span data-stu-id="9ee99-104">Gets the value of `true` in the current script context.</span></span>  
  
## <span data-ttu-id="9ee99-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="9ee99-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetTrueValue(  
   _Out_ JsValueRef *trueValue  
);  
```  
  
#### <span data-ttu-id="9ee99-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="9ee99-106">Parameters</span></span>  
 `trueValue`  
 <span data-ttu-id="9ee99-107">Der `true` Wert.</span><span class="sxs-lookup"><span data-stu-id="9ee99-107">The `true` value.</span></span>  
  
## <span data-ttu-id="9ee99-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9ee99-108">Return Value</span></span>  
 <span data-ttu-id="9ee99-109">Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="9ee99-109">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="9ee99-110">Hinweise</span><span class="sxs-lookup"><span data-stu-id="9ee99-110">Remarks</span></span>  
 <span data-ttu-id="9ee99-111">Erfordert einen aktiven Skriptkontext.</span><span class="sxs-lookup"><span data-stu-id="9ee99-111">Requires an active script context.</span></span>  
  
## <span data-ttu-id="9ee99-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9ee99-112">Requirements</span></span>  
 <span data-ttu-id="9ee99-113">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="9ee99-113">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="9ee99-114">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="9ee99-114">See Also</span></span>  
 [<span data-ttu-id="9ee99-115">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="9ee99-115">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
