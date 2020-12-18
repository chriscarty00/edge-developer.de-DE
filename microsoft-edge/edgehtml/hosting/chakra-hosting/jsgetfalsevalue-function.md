---
description: Ruft den Wert `false` im aktuellen Skriptkontext ab.
title: JsGetFalseValue-Funktion | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsGetFalseValue
helpviewer_keywords:
- JsGetFalseValue function
ms.assetid: 621a584c-4ca8-4ba0-b19a-6cb50cf830b6
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: c87ad969fc7547f4d650148005327fb93dce805d
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233995"
---
# <span data-ttu-id="1e1a6-103">JsGetFalseValue Funktion</span><span class="sxs-lookup"><span data-stu-id="1e1a6-103">JsGetFalseValue Function</span></span>

<span data-ttu-id="1e1a6-104">Ruft den Wert `false` im aktuellen Skriptkontext ab.</span><span class="sxs-lookup"><span data-stu-id="1e1a6-104">Gets the value of `false` in the current script context.</span></span>  
  
## <span data-ttu-id="1e1a6-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="1e1a6-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetFalseValue(  
   _Out_ JsValueRef *falseValue  
);  
```  
  
#### <span data-ttu-id="1e1a6-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="1e1a6-106">Parameters</span></span>  
 `falseValue`  
 <span data-ttu-id="1e1a6-107">Der `false` Wert.</span><span class="sxs-lookup"><span data-stu-id="1e1a6-107">The `false` value.</span></span>  
  
## <span data-ttu-id="1e1a6-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1e1a6-108">Return Value</span></span>  
 <span data-ttu-id="1e1a6-109">Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="1e1a6-109">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="1e1a6-110">Hinweise</span><span class="sxs-lookup"><span data-stu-id="1e1a6-110">Remarks</span></span>  
 <span data-ttu-id="1e1a6-111">Erfordert einen aktiven Skriptkontext.</span><span class="sxs-lookup"><span data-stu-id="1e1a6-111">Requires an active script context.</span></span>  
  
## <span data-ttu-id="1e1a6-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1e1a6-112">Requirements</span></span>  
 <span data-ttu-id="1e1a6-113">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="1e1a6-113">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="1e1a6-114">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="1e1a6-114">See Also</span></span>  
 [<span data-ttu-id="1e1a6-115">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="1e1a6-115">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
