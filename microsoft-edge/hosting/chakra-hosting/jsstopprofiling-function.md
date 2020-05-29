---
description: Beendet die Profilerstellung im aktuellen Kontext.
title: JsStopProfiling-Funktion | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsStopProfiling
helpviewer_keywords:
- JsStopProfiling function
ms.assetid: 3639c04f-a0f9-418b-be39-92f64b4e7ef8
caps.latest.revision: 13
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 9d021c7c9849d20283a39d6ecffc89c5b2ea0db0
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10568202"
---
# <span data-ttu-id="68a26-103">JsStopProfiling-Funktion</span><span class="sxs-lookup"><span data-stu-id="68a26-103">JsStopProfiling Function</span></span>
<span data-ttu-id="68a26-104">Beendet die Profilerstellung im aktuellen Kontext.</span><span class="sxs-lookup"><span data-stu-id="68a26-104">Stops profiling in the current context.</span></span>  
  
## <span data-ttu-id="68a26-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="68a26-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsStopProfiling(  
   _In_ HRESULT reason  
);  
```  
  
#### <span data-ttu-id="68a26-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="68a26-106">Parameters</span></span>  
 `reason`  
 <span data-ttu-id="68a26-107">Der Grund dafür, dass die Profilerstellung angehalten wird, um an den Profiler Rückruf zu übergeben.</span><span class="sxs-lookup"><span data-stu-id="68a26-107">The reason for stopping profiling to pass to the profiler callback.</span></span>  
  
## <span data-ttu-id="68a26-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="68a26-108">Return Value</span></span>  
 <span data-ttu-id="68a26-109">Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="68a26-109">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="68a26-110">Hinweise</span><span class="sxs-lookup"><span data-stu-id="68a26-110">Remarks</span></span>  
 <span data-ttu-id="68a26-111">Gibt keinen Fehler zurück, wenn die Profilerstellung nicht gestartet wurde.</span><span class="sxs-lookup"><span data-stu-id="68a26-111">Will not return an error if profiling has not started.</span></span>  
  
 <span data-ttu-id="68a26-112">Erfordert einen aktiven Skriptkontext.</span><span class="sxs-lookup"><span data-stu-id="68a26-112">Requires an active script context.</span></span>  
  
 <span data-ttu-id="68a26-113">Diese API wird in Desktop-Apps unterstützt, wird aber in Store-Apps nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="68a26-113">This API is supported in desktop apps, but is not supported in Store apps.</span></span>  
  
## <span data-ttu-id="68a26-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="68a26-114">Requirements</span></span>  
 <span data-ttu-id="68a26-115">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="68a26-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="68a26-116">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="68a26-116">See Also</span></span>  
 [<span data-ttu-id="68a26-117">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="68a26-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)