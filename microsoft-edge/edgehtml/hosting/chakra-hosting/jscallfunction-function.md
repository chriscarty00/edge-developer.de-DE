---
description: Ruft eine Funktion auf.
title: JsCallFunction-Funktion | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsCallFunction
helpviewer_keywords:
- JsCallFunction function
ms.assetid: 8a1dca72-d720-4a28-a86e-6809465006fe
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: dc26f66cb7deae0857ce34cbd4d83ee26046b3c8
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233767"
---
# <span data-ttu-id="a5ee3-103">JsCallFunction Funktion</span><span class="sxs-lookup"><span data-stu-id="a5ee3-103">JsCallFunction Function</span></span>

<span data-ttu-id="a5ee3-104">Ruft eine Funktion auf.</span><span class="sxs-lookup"><span data-stu-id="a5ee3-104">Invokes a function.</span></span>  
  
## <span data-ttu-id="a5ee3-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a5ee3-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsCallFunction(  
   _In_ JsValueRef function,  
   _In_reads_(argumentCount) JsValueRef *arguments,  
   _In_ unsigned short argumentCount,  
   _Out_opt_ JsValueRef *result  
);  
```  
  
#### <span data-ttu-id="a5ee3-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a5ee3-106">Parameters</span></span>  
 `function`  
 <span data-ttu-id="a5ee3-107">Die aufzurufende Funktion.</span><span class="sxs-lookup"><span data-stu-id="a5ee3-107">The function to invoke.</span></span>  
  
 `arguments`  
 <span data-ttu-id="a5ee3-108">Die Argumente für den Anruf.</span><span class="sxs-lookup"><span data-stu-id="a5ee3-108">The arguments to the call.</span></span>  
  
 `argumentCount`  
 <span data-ttu-id="a5ee3-109">Die Anzahl von Argumenten, die an die Funktion übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="a5ee3-109">The number of arguments being passed in to the function.</span></span>  
  
 `result`  
 <span data-ttu-id="a5ee3-110">Der vom Funktionsaufruf zurückgegebene Wert (sofern vorhanden).</span><span class="sxs-lookup"><span data-stu-id="a5ee3-110">The value returned from the function invocation, if any.</span></span>  
  
## <span data-ttu-id="a5ee3-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a5ee3-111">Return Value</span></span>  
 <span data-ttu-id="a5ee3-112">Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="a5ee3-112">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="a5ee3-113">Hinweise</span><span class="sxs-lookup"><span data-stu-id="a5ee3-113">Remarks</span></span>  
 <span data-ttu-id="a5ee3-114">Erfordert einen aktiven Skriptkontext.</span><span class="sxs-lookup"><span data-stu-id="a5ee3-114">Requires an active script context.</span></span>  
  
## <span data-ttu-id="a5ee3-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a5ee3-115">Requirements</span></span>  
 <span data-ttu-id="a5ee3-116">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="a5ee3-116">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="a5ee3-117">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="a5ee3-117">See Also</span></span>  
 [<span data-ttu-id="a5ee3-118">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="a5ee3-118">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
