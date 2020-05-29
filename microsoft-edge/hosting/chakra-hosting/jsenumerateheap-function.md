---
description: Listet den Heap des aktuellen Kontexts auf.
title: JsEnumerateHeap-Funktion | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsEnumerateHeap
helpviewer_keywords:
- JsEnumerateHeap function
ms.assetid: 3e518e0b-b959-4686-899c-83e6b1946c9d
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: f1c2590388fcc09b641e3908d45eef7271bcb1ad
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10568406"
---
# <span data-ttu-id="21948-103">JsEnumerateHeap-Funktion</span><span class="sxs-lookup"><span data-stu-id="21948-103">JsEnumerateHeap Function</span></span>
<span data-ttu-id="21948-104">Listet den Heap des aktuellen Kontexts auf.</span><span class="sxs-lookup"><span data-stu-id="21948-104">Enumerates the heap of the current context.</span></span>  
  
## <span data-ttu-id="21948-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="21948-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsEnumerateHeap(  
   _Out_ IActiveScriptProfilerHeapEnum **enumerator  
);  
```  
  
#### <span data-ttu-id="21948-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="21948-106">Parameters</span></span>  
 `enumerator`  
 <span data-ttu-id="21948-107">Der Heap-Enumerator.</span><span class="sxs-lookup"><span data-stu-id="21948-107">The heap enumerator.</span></span>  
  
## <span data-ttu-id="21948-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="21948-108">Return Value</span></span>  
 <span data-ttu-id="21948-109">Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="21948-109">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="21948-110">Hinweise</span><span class="sxs-lookup"><span data-stu-id="21948-110">Remarks</span></span>  
 <span data-ttu-id="21948-111">Während der Enumeration des Heaps wird der aktuelle Kontext nicht entfernt, und alle Aufrufe zum Ändern des Zustands des Kontexts schlagen fehl, bis der Heap Enumerator freigegeben wird.</span><span class="sxs-lookup"><span data-stu-id="21948-111">While the heap is being enumerated, the current context cannot be removed, and all calls to modify the state of the context will fail until the heap enumerator is released.</span></span>  
  
 <span data-ttu-id="21948-112">Erfordert einen aktiven Skriptkontext.</span><span class="sxs-lookup"><span data-stu-id="21948-112">Requires an active script context.</span></span>  
  
 <span data-ttu-id="21948-113">Diese API wird in Desktop-Apps unterstützt, wird aber in Store-Apps nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="21948-113">This API is supported in desktop apps, but is not supported in Store apps.</span></span>  
  
## <span data-ttu-id="21948-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="21948-114">Requirements</span></span>  
 <span data-ttu-id="21948-115">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="21948-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="21948-116">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="21948-116">See Also</span></span>  
 [<span data-ttu-id="21948-117">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="21948-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)