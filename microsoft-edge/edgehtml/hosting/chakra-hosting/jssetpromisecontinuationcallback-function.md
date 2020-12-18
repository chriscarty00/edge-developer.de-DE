---
description: Legt eine Fortsetzungs Rückruffunktion für Versprechen fest, die vom Kontext aufgerufen wird, wenn eine Aufgabe zur zukünftigen Ausführung in die Warteschlange gestellt werden soll.
title: JsSetPromiseContinuationCallback-Funktion | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 6ef0faf4-1500-4bd9-aeca-c208492af8ea
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: da928431f05831c95d5bc116dbd129de9cb5f3b4
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233988"
---
# <span data-ttu-id="92665-103">JsSetPromiseContinuationCallback Funktion</span><span class="sxs-lookup"><span data-stu-id="92665-103">JsSetPromiseContinuationCallback Function</span></span>

<span data-ttu-id="92665-104">Legt eine Fortsetzungs Rückruffunktion für Versprechen fest, die vom Kontext aufgerufen wird, wenn eine Aufgabe zur zukünftigen Ausführung in die Warteschlange gestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="92665-104">Sets a promise continuation callback function that is called by the context when a task needs to be queued for future execution.</span></span>  
  
## <span data-ttu-id="92665-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="92665-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsSetPromiseContinuationCallback(  
   _In_ JsPromiseContinuationCallback promiseContinuationCallback,  
   _In_opt_ void *callbackState  
);  
```  
  
#### <span data-ttu-id="92665-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="92665-106">Parameters</span></span>  
 `promiseContinuationCallback`  
 <span data-ttu-id="92665-107">Die Rückruffunktion, die festzulegen ist.</span><span class="sxs-lookup"><span data-stu-id="92665-107">The callback function being set.</span></span>  
  
 `callbackState`  
 <span data-ttu-id="92665-108">Der Benutzer hat den Zustand bereitgestellt, der an den Rückruf zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="92665-108">User provided state that will be passed back to the callback.</span></span>  
  
## <span data-ttu-id="92665-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="92665-109">Return Value</span></span>  
 <span data-ttu-id="92665-110">Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="92665-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="92665-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="92665-111">Remarks</span></span>  
 <span data-ttu-id="92665-112">Erfordert einen aktiven Skriptkontext.</span><span class="sxs-lookup"><span data-stu-id="92665-112">Requires an active script context.</span></span>  
  
 <span data-ttu-id="92665-113">Diese API wird nur im EdgeHTML-Modus unterstützt.</span><span class="sxs-lookup"><span data-stu-id="92665-113">This API is supported only in EdgeHTML mode.</span></span>  
  
## <span data-ttu-id="92665-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="92665-114">Requirements</span></span>  
 <span data-ttu-id="92665-115">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="92665-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="92665-116">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="92665-116">See Also</span></span>  
 [<span data-ttu-id="92665-117">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="92665-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
