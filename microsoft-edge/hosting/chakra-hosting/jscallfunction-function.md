---
description: Ruft eine Funktion auf.
title: JsCallFunction-Funktion | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsCallFunction
helpviewer_keywords:
- JsCallFunction function
ms.assetid: 8a1dca72-d720-4a28-a86e-6809465006fe
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: f242ccef71d8a2b361dbe2d1a299728f5551f5d3
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10567329"
---
# <span data-ttu-id="2083d-103">JsCallFunction-Funktion</span><span class="sxs-lookup"><span data-stu-id="2083d-103">JsCallFunction Function</span></span>
<span data-ttu-id="2083d-104">Ruft eine Funktion auf.</span><span class="sxs-lookup"><span data-stu-id="2083d-104">Invokes a function.</span></span>  
  
## <span data-ttu-id="2083d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="2083d-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsCallFunction(  
   _In_ JsValueRef function,  
   _In_reads_(argumentCount) JsValueRef *arguments,  
   _In_ unsigned short argumentCount,  
   _Out_opt_ JsValueRef *result  
);  
```  
  
#### <span data-ttu-id="2083d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="2083d-106">Parameters</span></span>  
 `function`  
 <span data-ttu-id="2083d-107">Die aufzurufende Funktion.</span><span class="sxs-lookup"><span data-stu-id="2083d-107">The function to invoke.</span></span>  
  
 `arguments`  
 <span data-ttu-id="2083d-108">Die Argumente für den Anruf.</span><span class="sxs-lookup"><span data-stu-id="2083d-108">The arguments to the call.</span></span>  
  
 `argumentCount`  
 <span data-ttu-id="2083d-109">Die Anzahl von Argumenten, die an die Funktion übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="2083d-109">The number of arguments being passed in to the function.</span></span>  
  
 `result`  
 <span data-ttu-id="2083d-110">Der vom Funktionsaufruf zurückgegebene Wert (sofern vorhanden).</span><span class="sxs-lookup"><span data-stu-id="2083d-110">The value returned from the function invocation, if any.</span></span>  
  
## <span data-ttu-id="2083d-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2083d-111">Return Value</span></span>  
 <span data-ttu-id="2083d-112">Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="2083d-112">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="2083d-113">Hinweise</span><span class="sxs-lookup"><span data-stu-id="2083d-113">Remarks</span></span>  
 <span data-ttu-id="2083d-114">Erfordert einen aktiven Skriptkontext.</span><span class="sxs-lookup"><span data-stu-id="2083d-114">Requires an active script context.</span></span>  
  
## <span data-ttu-id="2083d-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2083d-115">Requirements</span></span>  
 <span data-ttu-id="2083d-116">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="2083d-116">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="2083d-117">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="2083d-117">See Also</span></span>  
 [<span data-ttu-id="2083d-118">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="2083d-118">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)