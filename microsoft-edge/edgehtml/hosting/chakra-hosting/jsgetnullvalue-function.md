---
description: Ruft den Wert `null` im aktuellen Skriptkontext ab.
title: JsGetNullValue-Funktion | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsGetNullValue
helpviewer_keywords:
- JsGetNullValue function
ms.assetid: 132a1496-8dfe-4d3c-a8f8-389f5b0b50d2
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 31e1ba19f9f27e75f0166238d98390e2c4a26c24
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233579"
---
# <span data-ttu-id="59425-103">JsGetNullValue Funktion</span><span class="sxs-lookup"><span data-stu-id="59425-103">JsGetNullValue Function</span></span>

<span data-ttu-id="59425-104">Ruft den Wert `null` im aktuellen Skriptkontext ab.</span><span class="sxs-lookup"><span data-stu-id="59425-104">Gets the value of `null` in the current script context.</span></span>  
  
## <span data-ttu-id="59425-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="59425-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetNullValue(  
   _Out_ JsValueRef *nullValue  
);  
```  
  
#### <span data-ttu-id="59425-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="59425-106">Parameters</span></span>  
 `nullValue`  
 <span data-ttu-id="59425-107">Der `null` Wert.</span><span class="sxs-lookup"><span data-stu-id="59425-107">The `null` value.</span></span>  
  
## <span data-ttu-id="59425-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="59425-108">Return Value</span></span>  
 <span data-ttu-id="59425-109">Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="59425-109">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="59425-110">Hinweise</span><span class="sxs-lookup"><span data-stu-id="59425-110">Remarks</span></span>  
 <span data-ttu-id="59425-111">Erfordert einen aktiven Skriptkontext.</span><span class="sxs-lookup"><span data-stu-id="59425-111">Requires an active script context.</span></span>  
  
## <span data-ttu-id="59425-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="59425-112">Requirements</span></span>  
 <span data-ttu-id="59425-113">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="59425-113">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="59425-114">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="59425-114">See Also</span></span>  
 [<span data-ttu-id="59425-115">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="59425-115">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
