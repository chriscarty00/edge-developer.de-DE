---
description: 'Legt eine Rückruffunktion fest, die von der Laufzeit vor der Garbage Collection aufgerufen wird. '
title: JsSetRuntimeBeforeCollectCallback-Funktion | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsSetRuntimeBeforeCollectCallback
helpviewer_keywords:
- JsSetRuntimeBeforeCollectCallback function
ms.assetid: 7b2fb911-6007-4ed9-a307-66cefe590ea4
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 94ad29fcfb778fc630d70664f917c6b5c2637dde
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233738"
---
# <span data-ttu-id="76419-103">JsSetRuntimeBeforeCollectCallback Funktion</span><span class="sxs-lookup"><span data-stu-id="76419-103">JsSetRuntimeBeforeCollectCallback Function</span></span>

<span data-ttu-id="76419-104">Legt eine Rückruffunktion fest, die von der Laufzeit vor der Garbage Collection aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="76419-104">Sets a callback function that is called by the runtime before garbage collection.</span></span>  
  
## <span data-ttu-id="76419-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="76419-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsSetRuntimeBeforeCollectCallback(  
   _In_ JsRuntimeHandle runtime,  
   _In_opt_ void *callbackState,  
   _In_ JsBeforeCollectCallback beforeCollectCallback  
);  
```  
  
#### <span data-ttu-id="76419-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="76419-106">Parameters</span></span>  
 `runtime`  
 <span data-ttu-id="76419-107">Die Laufzeit, für die der Zuordnungs Rückruf registriert werden soll.</span><span class="sxs-lookup"><span data-stu-id="76419-107">The runtime for which to register the allocation callback.</span></span>  
  
 `callbackState`  
 <span data-ttu-id="76419-108">Der Benutzer hat den Zustand bereitgestellt, der an den Rückruf zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="76419-108">User provided state that will be passed back to the callback.</span></span>  
  
 `beforeCollectCallback`  
 <span data-ttu-id="76419-109">Die Rückruffunktion, die festzulegen ist.</span><span class="sxs-lookup"><span data-stu-id="76419-109">The callback function being set.</span></span>  
  
## <span data-ttu-id="76419-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="76419-110">Return Value</span></span>  
 <span data-ttu-id="76419-111">Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="76419-111">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="76419-112">Hinweise</span><span class="sxs-lookup"><span data-stu-id="76419-112">Remarks</span></span>  
 <span data-ttu-id="76419-113">Der Rückruf wird für den aktuellen Runtime-Ausführungsthread aufgerufen, daher wird die Ausführung blockiert, bis der Rückruf abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="76419-113">The callback is invoked on the current runtime execution thread, therefore execution is blocked until the callback completes.</span></span>  
  
 <span data-ttu-id="76419-114">Der Rückruf kann von Hosts verwendet werden, um die Garbage Collection vorzubereiten.</span><span class="sxs-lookup"><span data-stu-id="76419-114">The callback can be used by hosts to prepare for garbage collection.</span></span> <span data-ttu-id="76419-115">Beispielsweisedurch das Freigeben unnötiger Verweise auf Chakra-Objekte.</span><span class="sxs-lookup"><span data-stu-id="76419-115">For example, by releasing unnecessary references on Chakra objects.</span></span>  
  
## <span data-ttu-id="76419-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="76419-116">Requirements</span></span>  
 <span data-ttu-id="76419-117">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="76419-117">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="76419-118">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="76419-118">See Also</span></span>  
 [<span data-ttu-id="76419-119">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="76419-119">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
