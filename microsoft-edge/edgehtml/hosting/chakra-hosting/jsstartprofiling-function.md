---
description: Startet die Profilerstellung im aktuellen Kontext.
title: JsStartProfiling-Funktion | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsStartProfiling
helpviewer_keywords:
- JsStartProfiling function
ms.assetid: 638da395-42dd-4fc5-b581-819e647e887d
caps.latest.revision: 13
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 332ff04a987e6e7ae5030983af96dd48249e58e2
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233942"
---
# <span data-ttu-id="4f3ca-103">JsStartProfiling Funktion</span><span class="sxs-lookup"><span data-stu-id="4f3ca-103">JsStartProfiling Function</span></span>

<span data-ttu-id="4f3ca-104">Startet die Profilerstellung im aktuellen Kontext.</span><span class="sxs-lookup"><span data-stu-id="4f3ca-104">Starts profiling in the current context.</span></span>  
  
## <span data-ttu-id="4f3ca-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="4f3ca-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsStartProfiling(  
   _In_ IActiveScriptProfilerCallback *callback,  
   _In_ PROFILER_EVENT_MASK eventMask,  
   _In_ unsigned long context  
);  
```  
  
#### <span data-ttu-id="4f3ca-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="4f3ca-106">Parameters</span></span>  
 `callback`  
 <span data-ttu-id="4f3ca-107">Der zu verwendende Profil Erstellungs Rückruf.</span><span class="sxs-lookup"><span data-stu-id="4f3ca-107">The profiling callback to use.</span></span>  
  
 `eventMask`  
 <span data-ttu-id="4f3ca-108">Die Profil Erstellungsereignisse, mit denen Sie eine Rückruffunktion durch.</span><span class="sxs-lookup"><span data-stu-id="4f3ca-108">The profiling events to callback with.</span></span>  
  
 `context`  
 <span data-ttu-id="4f3ca-109">Ein Kontext, der an den Profil Erstellungs Rückruf übergeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="4f3ca-109">A context to pass to the profiling callback.</span></span>  
  
## <span data-ttu-id="4f3ca-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4f3ca-110">Return Value</span></span>  
 <span data-ttu-id="4f3ca-111">Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="4f3ca-111">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="4f3ca-112">Hinweise</span><span class="sxs-lookup"><span data-stu-id="4f3ca-112">Remarks</span></span>  
 <span data-ttu-id="4f3ca-113">Erfordert einen aktiven Skriptkontext.</span><span class="sxs-lookup"><span data-stu-id="4f3ca-113">Requires an active script context.</span></span>  
  
 <span data-ttu-id="4f3ca-114">Diese API wird in Desktop-Apps unterstützt, wird aber in Store-Apps nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="4f3ca-114">This API is supported in desktop apps, but is not supported in Store apps.</span></span>  
  
## <span data-ttu-id="4f3ca-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4f3ca-115">Requirements</span></span>  
 <span data-ttu-id="4f3ca-116">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="4f3ca-116">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="4f3ca-117">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="4f3ca-117">See Also</span></span>  
 [<span data-ttu-id="4f3ca-118">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="4f3ca-118">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
