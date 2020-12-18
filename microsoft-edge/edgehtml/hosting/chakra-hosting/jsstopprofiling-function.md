---
description: Beendet die Profilerstellung im aktuellen Kontext.
title: JsStopProfiling-Funktion | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsStopProfiling
helpviewer_keywords:
- JsStopProfiling function
ms.assetid: 3639c04f-a0f9-418b-be39-92f64b4e7ef8
caps.latest.revision: 13
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 02c42afda7e61d71b90a9a1a71aa71cc53584ff8
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233943"
---
# <span data-ttu-id="00854-103">JsStopProfiling Funktion</span><span class="sxs-lookup"><span data-stu-id="00854-103">JsStopProfiling Function</span></span>

<span data-ttu-id="00854-104">Beendet die Profilerstellung im aktuellen Kontext.</span><span class="sxs-lookup"><span data-stu-id="00854-104">Stops profiling in the current context.</span></span>  
  
## <span data-ttu-id="00854-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="00854-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsStopProfiling(  
   _In_ HRESULT reason  
);  
```  
  
#### <span data-ttu-id="00854-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="00854-106">Parameters</span></span>  
 `reason`  
 <span data-ttu-id="00854-107">Der Grund dafür, dass die Profilerstellung angehalten wird, um an den Profiler Rückruf zu übergeben.</span><span class="sxs-lookup"><span data-stu-id="00854-107">The reason for stopping profiling to pass to the profiler callback.</span></span>  
  
## <span data-ttu-id="00854-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="00854-108">Return Value</span></span>  
 <span data-ttu-id="00854-109">Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="00854-109">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="00854-110">Hinweise</span><span class="sxs-lookup"><span data-stu-id="00854-110">Remarks</span></span>  
 <span data-ttu-id="00854-111">Gibt keinen Fehler zurück, wenn die Profilerstellung nicht gestartet wurde.</span><span class="sxs-lookup"><span data-stu-id="00854-111">Will not return an error if profiling has not started.</span></span>  
  
 <span data-ttu-id="00854-112">Erfordert einen aktiven Skriptkontext.</span><span class="sxs-lookup"><span data-stu-id="00854-112">Requires an active script context.</span></span>  
  
 <span data-ttu-id="00854-113">Diese API wird in Desktop-Apps unterstützt, wird aber in Store-Apps nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="00854-113">This API is supported in desktop apps, but is not supported in Store apps.</span></span>  
  
## <span data-ttu-id="00854-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="00854-114">Requirements</span></span>  
 <span data-ttu-id="00854-115">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="00854-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="00854-116">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="00854-116">See Also</span></span>  
 [<span data-ttu-id="00854-117">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="00854-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
