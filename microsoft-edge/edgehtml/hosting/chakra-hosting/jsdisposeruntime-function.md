---
description: Gibt eine Laufzeit frei.
title: JsDisposeRuntime-Funktion | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsDisposeRuntime
helpviewer_keywords:
- JsDisposeRuntime function
ms.assetid: 0aefde3f-7250-48be-afc5-53ea85c12f30
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 8cff4578415cdf1aaa01b7203ce734cef9115301
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233954"
---
# <span data-ttu-id="c47e9-103">JsDisposeRuntime Funktion</span><span class="sxs-lookup"><span data-stu-id="c47e9-103">JsDisposeRuntime Function</span></span>

<span data-ttu-id="c47e9-104">Gibt eine Laufzeit frei.</span><span class="sxs-lookup"><span data-stu-id="c47e9-104">Disposes a runtime.</span></span>  
  
## <span data-ttu-id="c47e9-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c47e9-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsDisposeRuntime(  
   _In_ JsRuntimeHandle runtime  
);  
```  
  
#### <span data-ttu-id="c47e9-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c47e9-106">Parameters</span></span>  
 `runtime`  
 <span data-ttu-id="c47e9-107">Die zu entsorgende Laufzeit.</span><span class="sxs-lookup"><span data-stu-id="c47e9-107">The runtime to dispose.</span></span>  
  
## <span data-ttu-id="c47e9-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c47e9-108">Return Value</span></span>  
 <span data-ttu-id="c47e9-109">Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="c47e9-109">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="c47e9-110">Hinweise</span><span class="sxs-lookup"><span data-stu-id="c47e9-110">Remarks</span></span>  
 <span data-ttu-id="c47e9-111">Nachdem eine Laufzeit freigegeben wurde, sind alle von ihr besessenen Ressourcen ungültig und können nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c47e9-111">Once a runtime has been disposed, all resources owned by it are invalid and cannot be used.</span></span> <span data-ttu-id="c47e9-112">Wenn die Common Language Runtime aktiv ist (d. h., dass Sie für einen bestimmten Thread auf Current gesetzt ist), kann Sie nicht freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="c47e9-112">If the runtime is active (i.e. it is set to be current on a particular thread), it cannot be disposed.</span></span>  
  
## <span data-ttu-id="c47e9-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c47e9-113">Requirements</span></span>  
 <span data-ttu-id="c47e9-114">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="c47e9-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="c47e9-115">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="c47e9-115">See Also</span></span>  
 [<span data-ttu-id="c47e9-116">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="c47e9-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
