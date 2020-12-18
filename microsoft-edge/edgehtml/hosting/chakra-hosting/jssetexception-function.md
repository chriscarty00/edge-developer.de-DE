---
description: Legt die Laufzeit des aktuellen Kontexts auf einen Ausnahmezustand fest.
title: JsSetException-Funktion | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsSetException
helpviewer_keywords:
- JsSetException function
ms.assetid: c528793a-2e1b-4ee1-bd2e-e63fd547dc40
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 2c2e3840d2a831db23a525c5d8854b9b2fcfb8c9
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233949"
---
# <span data-ttu-id="6d43e-103">JsSetException Funktion</span><span class="sxs-lookup"><span data-stu-id="6d43e-103">JsSetException Function</span></span>

<span data-ttu-id="6d43e-104">Legt die Laufzeit des aktuellen Kontexts auf einen Ausnahmezustand fest.</span><span class="sxs-lookup"><span data-stu-id="6d43e-104">Sets the runtime of the current context to an exception state.</span></span>  
  
## <span data-ttu-id="6d43e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="6d43e-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsSetException(  
   _In_ JsValueRef exception  
);  
```  
  
#### <span data-ttu-id="6d43e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="6d43e-106">Parameters</span></span>  
 `exception`  
 <span data-ttu-id="6d43e-107">Die JavaScript-Ausnahme, die für die Laufzeit des aktuellen Kontexts gesetzt werden soll.</span><span class="sxs-lookup"><span data-stu-id="6d43e-107">The JavaScript exception to set for the runtime of the current context.</span></span>  
  
## <span data-ttu-id="6d43e-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6d43e-108">Return Value</span></span>  
 `JsNoError` <span data-ttu-id="6d43e-109">Wenn das Modul in einen Ausnahmezustand gesetzt wurde, wird andernfalls ein Fehlercode ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="6d43e-109">if the engine was set into an exception state, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="6d43e-110">Hinweise</span><span class="sxs-lookup"><span data-stu-id="6d43e-110">Remarks</span></span>  
 <span data-ttu-id="6d43e-111">Wenn sich die Laufzeit des aktuellen Kontexts bereits in einem Ausnahmezustand befindet, gibt diese API zurück `JsErrorInExceptionState` .</span><span class="sxs-lookup"><span data-stu-id="6d43e-111">If the runtime of the current context is already in an exception state, this API will return `JsErrorInExceptionState`.</span></span>  
  
 <span data-ttu-id="6d43e-112">Erfordert einen aktiven Skriptkontext.</span><span class="sxs-lookup"><span data-stu-id="6d43e-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="6d43e-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6d43e-113">Requirements</span></span>  
 <span data-ttu-id="6d43e-114">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="6d43e-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="6d43e-115">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="6d43e-115">See Also</span></span>  
 [<span data-ttu-id="6d43e-116">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="6d43e-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
