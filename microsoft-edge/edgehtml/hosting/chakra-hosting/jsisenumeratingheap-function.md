---
description: Gibt einen Wert zurück, der angibt, ob der Heap des aktuellen Kontexts aufgelistet wird.
title: JsIsEnumeratingHeap-Funktion | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsIsEnumeratingHeap
helpviewer_keywords:
- JsIsEnumeratingHeap function
ms.assetid: 5d14518e-3153-43f2-9a9c-068580cbd54f
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 5b66fc70ea79d78029f6bc0c900ade1aae38e604
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11234125"
---
# <span data-ttu-id="dce87-103">JsIsEnumeratingHeap Funktion</span><span class="sxs-lookup"><span data-stu-id="dce87-103">JsIsEnumeratingHeap Function</span></span>

<span data-ttu-id="dce87-104">Gibt einen Wert zurück, der angibt, ob der Heap des aktuellen Kontexts aufgelistet wird.</span><span class="sxs-lookup"><span data-stu-id="dce87-104">Returns a value that indicates whether the heap of the current context is being enumerated.</span></span>  
  
## <span data-ttu-id="dce87-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="dce87-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsIsEnumeratingHeap(  
   _Out_ bool *isEnumeratingHeap  
);  
```  
  
#### <span data-ttu-id="dce87-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="dce87-106">Parameters</span></span>  
 `isEnumeratingHeap`  
 <span data-ttu-id="dce87-107">Gibt an, ob der Heap aufgelistet wird.</span><span class="sxs-lookup"><span data-stu-id="dce87-107">Whether the heap is being enumerated.</span></span>  
  
## <span data-ttu-id="dce87-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="dce87-108">Return Value</span></span>  
 <span data-ttu-id="dce87-109">Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="dce87-109">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="dce87-110">Hinweise</span><span class="sxs-lookup"><span data-stu-id="dce87-110">Remarks</span></span>  
 <span data-ttu-id="dce87-111">Erfordert einen aktiven Skriptkontext.</span><span class="sxs-lookup"><span data-stu-id="dce87-111">Requires an active script context.</span></span>  
  
 <span data-ttu-id="dce87-112">Diese API wird in Desktop-Apps unterstützt, wird aber in Store-Apps nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="dce87-112">This API is supported in desktop apps, but is not supported in Store apps.</span></span>  
  
## <span data-ttu-id="dce87-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="dce87-113">Requirements</span></span>  
 <span data-ttu-id="dce87-114">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="dce87-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="dce87-115">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="dce87-115">See Also</span></span>  
 [<span data-ttu-id="dce87-116">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="dce87-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
