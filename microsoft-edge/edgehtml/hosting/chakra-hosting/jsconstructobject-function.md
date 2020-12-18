---
description: Ruft eine Funktion als Konstruktor auf.
title: JsConstructObject-Funktion | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsConstructObject
helpviewer_keywords:
- JsConstructObject function
ms.assetid: b07d2440-db55-4a6a-8376-56b40a8039a1
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 8dbb757456412e50efaf3a026d169e6b3612b6b1
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233765"
---
# <span data-ttu-id="e5e22-103">JsConstructObject Funktion</span><span class="sxs-lookup"><span data-stu-id="e5e22-103">JsConstructObject Function</span></span>

<span data-ttu-id="e5e22-104">Ruft eine Funktion als Konstruktor auf.</span><span class="sxs-lookup"><span data-stu-id="e5e22-104">Invokes a function as a constructor.</span></span>  
  
## <span data-ttu-id="e5e22-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e5e22-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsConstructObject(  
   _In_ JsValueRef function,  
   _In_reads_(argumentCount) JsValueRef *arguments,  
   _In_ unsigned short argumentCount,  
   _Out_opt_ JsValueRef *result  
);  
```  
  
#### <span data-ttu-id="e5e22-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="e5e22-106">Parameters</span></span>  
 `function`  
 <span data-ttu-id="e5e22-107">Die Funktion, die als Konstruktor aufgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="e5e22-107">The function to invoke as a constructor.</span></span>  
  
 `arguments`  
 <span data-ttu-id="e5e22-108">Die Argumente für den Anruf.</span><span class="sxs-lookup"><span data-stu-id="e5e22-108">The arguments to the call.</span></span>  
  
 `argumentCount`  
 <span data-ttu-id="e5e22-109">Die Anzahl von Argumenten, die an die Funktion übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="e5e22-109">The number of arguments being passed in to the function.</span></span>  
  
 `result`  
 <span data-ttu-id="e5e22-110">Der vom Funktionsaufruf zurückgegebene Wert.</span><span class="sxs-lookup"><span data-stu-id="e5e22-110">The value returned from the function invocation.</span></span>  
  
## <span data-ttu-id="e5e22-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e5e22-111">Return Value</span></span>  
 <span data-ttu-id="e5e22-112">Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="e5e22-112">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="e5e22-113">Hinweise</span><span class="sxs-lookup"><span data-stu-id="e5e22-113">Remarks</span></span>  
 <span data-ttu-id="e5e22-114">Erfordert einen aktiven Skriptkontext.</span><span class="sxs-lookup"><span data-stu-id="e5e22-114">Requires an active script context.</span></span>  
  
## <span data-ttu-id="e5e22-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e5e22-115">Requirements</span></span>  
 <span data-ttu-id="e5e22-116">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="e5e22-116">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="e5e22-117">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="e5e22-117">See Also</span></span>  
 [<span data-ttu-id="e5e22-118">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="e5e22-118">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
