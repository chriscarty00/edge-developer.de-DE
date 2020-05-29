---
description: Ruft eine Funktion als Konstruktor auf.
title: JsConstructObject-Funktion | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsConstructObject
helpviewer_keywords:
- JsConstructObject function
ms.assetid: b07d2440-db55-4a6a-8376-56b40a8039a1
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 6fb9654b5c7321d6c6b0b255ec897fb30a114041
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10567324"
---
# <span data-ttu-id="9a254-103">JsConstructObject-Funktion</span><span class="sxs-lookup"><span data-stu-id="9a254-103">JsConstructObject Function</span></span>
<span data-ttu-id="9a254-104">Ruft eine Funktion als Konstruktor auf.</span><span class="sxs-lookup"><span data-stu-id="9a254-104">Invokes a function as a constructor.</span></span>  
  
## <span data-ttu-id="9a254-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="9a254-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsConstructObject(  
   _In_ JsValueRef function,  
   _In_reads_(argumentCount) JsValueRef *arguments,  
   _In_ unsigned short argumentCount,  
   _Out_opt_ JsValueRef *result  
);  
```  
  
#### <span data-ttu-id="9a254-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="9a254-106">Parameters</span></span>  
 `function`  
 <span data-ttu-id="9a254-107">Die Funktion, die als Konstruktor aufgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="9a254-107">The function to invoke as a constructor.</span></span>  
  
 `arguments`  
 <span data-ttu-id="9a254-108">Die Argumente für den Anruf.</span><span class="sxs-lookup"><span data-stu-id="9a254-108">The arguments to the call.</span></span>  
  
 `argumentCount`  
 <span data-ttu-id="9a254-109">Die Anzahl von Argumenten, die an die Funktion übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="9a254-109">The number of arguments being passed in to the function.</span></span>  
  
 `result`  
 <span data-ttu-id="9a254-110">Der vom Funktionsaufruf zurückgegebene Wert.</span><span class="sxs-lookup"><span data-stu-id="9a254-110">The value returned from the function invocation.</span></span>  
  
## <span data-ttu-id="9a254-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9a254-111">Return Value</span></span>  
 <span data-ttu-id="9a254-112">Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="9a254-112">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="9a254-113">Hinweise</span><span class="sxs-lookup"><span data-stu-id="9a254-113">Remarks</span></span>  
 <span data-ttu-id="9a254-114">Erfordert einen aktiven Skriptkontext.</span><span class="sxs-lookup"><span data-stu-id="9a254-114">Requires an active script context.</span></span>  
  
## <span data-ttu-id="9a254-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9a254-115">Requirements</span></span>  
 <span data-ttu-id="9a254-116">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="9a254-116">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="9a254-117">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="9a254-117">See Also</span></span>  
 [<span data-ttu-id="9a254-118">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="9a254-118">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)