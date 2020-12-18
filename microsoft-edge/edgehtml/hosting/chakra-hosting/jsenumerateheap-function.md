---
description: Listet den Heap des aktuellen Kontexts auf.
title: JsEnumerateHeap-Funktion | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsEnumerateHeap
helpviewer_keywords:
- JsEnumerateHeap function
ms.assetid: 3e518e0b-b959-4686-899c-83e6b1946c9d
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: bb76b28f24b769f71827e59be691188e34e9e1a3
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11234099"
---
# <span data-ttu-id="a3867-103">JsEnumerateHeap Funktion</span><span class="sxs-lookup"><span data-stu-id="a3867-103">JsEnumerateHeap Function</span></span>

<span data-ttu-id="a3867-104">Listet den Heap des aktuellen Kontexts auf.</span><span class="sxs-lookup"><span data-stu-id="a3867-104">Enumerates the heap of the current context.</span></span>  
  
## <span data-ttu-id="a3867-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a3867-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsEnumerateHeap(  
   _Out_ IActiveScriptProfilerHeapEnum **enumerator  
);  
```  
  
#### <span data-ttu-id="a3867-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a3867-106">Parameters</span></span>  
 `enumerator`  
 <span data-ttu-id="a3867-107">Der Heap-Enumerator.</span><span class="sxs-lookup"><span data-stu-id="a3867-107">The heap enumerator.</span></span>  
  
## <span data-ttu-id="a3867-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a3867-108">Return Value</span></span>  
 <span data-ttu-id="a3867-109">Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="a3867-109">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="a3867-110">Hinweise</span><span class="sxs-lookup"><span data-stu-id="a3867-110">Remarks</span></span>  
 <span data-ttu-id="a3867-111">Während der Enumeration des Heaps wird der aktuelle Kontext nicht entfernt, und alle Aufrufe zum Ändern des Zustands des Kontexts schlagen fehl, bis der Heap Enumerator freigegeben wird.</span><span class="sxs-lookup"><span data-stu-id="a3867-111">While the heap is being enumerated, the current context cannot be removed, and all calls to modify the state of the context will fail until the heap enumerator is released.</span></span>  
  
 <span data-ttu-id="a3867-112">Erfordert einen aktiven Skriptkontext.</span><span class="sxs-lookup"><span data-stu-id="a3867-112">Requires an active script context.</span></span>  
  
 <span data-ttu-id="a3867-113">Diese API wird in Desktop-Apps unterstützt, wird aber in Store-Apps nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a3867-113">This API is supported in desktop apps, but is not supported in Store apps.</span></span>  
  
## <span data-ttu-id="a3867-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a3867-114">Requirements</span></span>  
 <span data-ttu-id="a3867-115">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="a3867-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="a3867-116">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="a3867-116">See Also</span></span>  
 [<span data-ttu-id="a3867-117">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="a3867-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
