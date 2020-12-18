---
description: Weist die Common Language Runtime an, die erforderliche Leerlaufverarbeitung auszuführen.
title: JsIdle-Funktion | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsIdle
helpviewer_keywords:
- JsIdle function
ms.assetid: 372d1c62-8e19-4886-aa33-364cabc09bba
caps.latest.revision: 13
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: ecba0aafb6b4dcccb4485c2956cae5ce4045355f
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11234263"
---
# <span data-ttu-id="ffb77-103">JsIdle Funktion</span><span class="sxs-lookup"><span data-stu-id="ffb77-103">JsIdle Function</span></span>

<span data-ttu-id="ffb77-104">Weist die Common Language Runtime an, die erforderliche Leerlaufverarbeitung auszuführen.</span><span class="sxs-lookup"><span data-stu-id="ffb77-104">Tells the runtime to do any idle processing it need to do.</span></span>  
  
## <span data-ttu-id="ffb77-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ffb77-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsIdle(  
   _Out_opt_ unsigned int *nextIdleTick  
);  
```  
  
#### <span data-ttu-id="ffb77-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ffb77-106">Parameters</span></span>  
 `nextIdleTick`  
 <span data-ttu-id="ffb77-107">Das nächste System wird angekreuzt, wenn mehr Leerlaufaufgaben ausgeführt werden müssen.</span><span class="sxs-lookup"><span data-stu-id="ffb77-107">The next system tick when there will be more idle work to do.</span></span> <span data-ttu-id="ffb77-108">Kann NULL sein.</span><span class="sxs-lookup"><span data-stu-id="ffb77-108">Can be null.</span></span> <span data-ttu-id="ffb77-109">Gibt die maximale Anzahl von Ticks zurück, wenn keine bevorstehende Leerlauf Arbeit ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="ffb77-109">Returns the maximum number of ticks if there no upcoming idle work to do.</span></span>  
  
## <span data-ttu-id="ffb77-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ffb77-110">Return Value</span></span>  
 <span data-ttu-id="ffb77-111">Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="ffb77-111">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="ffb77-112">Hinweise</span><span class="sxs-lookup"><span data-stu-id="ffb77-112">Remarks</span></span>  
 <span data-ttu-id="ffb77-113">Wenn die Idle-Verarbeitung für die aktuelle Laufzeit aktiviert wurde, `JsIdle` informiert der Aufruf die aktuelle Laufzeit darüber, dass der Host inaktiv ist und dass die Laufzeit Speicher Bereinigungsaufgaben ausführen kann.</span><span class="sxs-lookup"><span data-stu-id="ffb77-113">If idle processing has been enabled for the current runtime, calling `JsIdle` will inform the current runtime that the host is idle and that the runtime can perform memory cleanup tasks.</span></span>  
  
 `JsIdle` <span data-ttu-id="ffb77-114">kann auch die Anzahl der System Ticks zurückgeben, bis die Laufzeit mehr arbeitslos ist.</span><span class="sxs-lookup"><span data-stu-id="ffb77-114">can also return the number of system ticks until there will be more idle work for the runtime to do.</span></span> <span data-ttu-id="ffb77-115">`JsIdle`Das anrufen, bevor diese Anzahl von Ticks abgelaufen ist, funktioniert nicht.</span><span class="sxs-lookup"><span data-stu-id="ffb77-115">Calling `JsIdle` before this number of ticks has passed will do no work.</span></span>  
  
 <span data-ttu-id="ffb77-116">Erfordert einen aktiven Skriptkontext.</span><span class="sxs-lookup"><span data-stu-id="ffb77-116">Requires an active script context.</span></span>  
  
## <span data-ttu-id="ffb77-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ffb77-117">Requirements</span></span>  
 <span data-ttu-id="ffb77-118">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="ffb77-118">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="ffb77-119">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="ffb77-119">See Also</span></span>  
 [<span data-ttu-id="ffb77-120">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="ffb77-120">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
