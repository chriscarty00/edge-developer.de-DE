---
description: Gibt einen Wert zurück, der angibt, ob der Heap des aktuellen Kontexts aufgelistet wird.
title: JsIsEnumeratingHeap-Funktion | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsIsEnumeratingHeap
helpviewer_keywords:
- JsIsEnumeratingHeap function
ms.assetid: 5d14518e-3153-43f2-9a9c-068580cbd54f
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 79f263547ef5812d905103d09ede7499d56c5dfb
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10567226"
---
# <span data-ttu-id="e438e-103">JsIsEnumeratingHeap-Funktion</span><span class="sxs-lookup"><span data-stu-id="e438e-103">JsIsEnumeratingHeap Function</span></span>
<span data-ttu-id="e438e-104">Gibt einen Wert zurück, der angibt, ob der Heap des aktuellen Kontexts aufgelistet wird.</span><span class="sxs-lookup"><span data-stu-id="e438e-104">Returns a value that indicates whether the heap of the current context is being enumerated.</span></span>  
  
## <span data-ttu-id="e438e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e438e-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsIsEnumeratingHeap(  
   _Out_ bool *isEnumeratingHeap  
);  
```  
  
#### <span data-ttu-id="e438e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="e438e-106">Parameters</span></span>  
 `isEnumeratingHeap`  
 <span data-ttu-id="e438e-107">Gibt an, ob der Heap aufgelistet wird.</span><span class="sxs-lookup"><span data-stu-id="e438e-107">Whether the heap is being enumerated.</span></span>  
  
## <span data-ttu-id="e438e-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e438e-108">Return Value</span></span>  
 <span data-ttu-id="e438e-109">Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="e438e-109">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="e438e-110">Hinweise</span><span class="sxs-lookup"><span data-stu-id="e438e-110">Remarks</span></span>  
 <span data-ttu-id="e438e-111">Erfordert einen aktiven Skriptkontext.</span><span class="sxs-lookup"><span data-stu-id="e438e-111">Requires an active script context.</span></span>  
  
 <span data-ttu-id="e438e-112">Diese API wird in Desktop-Apps unterstützt, wird aber in Store-Apps nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e438e-112">This API is supported in desktop apps, but is not supported in Store apps.</span></span>  
  
## <span data-ttu-id="e438e-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e438e-113">Requirements</span></span>  
 <span data-ttu-id="e438e-114">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="e438e-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="e438e-115">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="e438e-115">See Also</span></span>  
 [<span data-ttu-id="e438e-116">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="e438e-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)