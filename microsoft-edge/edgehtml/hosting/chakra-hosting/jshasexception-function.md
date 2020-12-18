---
description: Bestimmt, ob sich die Laufzeit des aktuellen Kontexts in einem Ausnahmezustand befindet.
title: JsHasException-Funktion | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsHasException
helpviewer_keywords:
- JsHasException function
ms.assetid: ac7da3ce-c746-4154-bbb8-bcb0859a8d5b
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 4f4abbd6c69a6b2b6414dae2f1de3a2acf21cc32
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233617"
---
# <span data-ttu-id="5546f-103">JsHasException Funktion</span><span class="sxs-lookup"><span data-stu-id="5546f-103">JsHasException Function</span></span>

<span data-ttu-id="5546f-104">Bestimmt, ob sich die Laufzeit des aktuellen Kontexts in einem Ausnahmezustand befindet.</span><span class="sxs-lookup"><span data-stu-id="5546f-104">Determines whether the runtime of the current context is in an exception state.</span></span>  
  
## <span data-ttu-id="5546f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="5546f-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsHasException(  
   _Out_ bool *hasException  
);  
```  
  
#### <span data-ttu-id="5546f-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="5546f-106">Parameters</span></span>  
 `hasException`  
 <span data-ttu-id="5546f-107">Gibt an, ob sich die Laufzeit des aktuellen Kontexts im Ausnahmezustand befindet.</span><span class="sxs-lookup"><span data-stu-id="5546f-107">Whether the runtime of the current context is in the exception state.</span></span>  
  
## <span data-ttu-id="5546f-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5546f-108">Return Value</span></span>  
 <span data-ttu-id="5546f-109">Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="5546f-109">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="5546f-110">Hinweise</span><span class="sxs-lookup"><span data-stu-id="5546f-110">Remarks</span></span>  
 <span data-ttu-id="5546f-111">Wenn ein Aufruf der Laufzeit zu einer Ausnahme führt (entweder durch Ausführen eines Skripts oder aufgrund eines Konvertierungs Fehlers), wird die Common Language Runtime in einen "Ausnahmezustand" versetzt.</span><span class="sxs-lookup"><span data-stu-id="5546f-111">If a call into the runtime results in an exception (either as the result of running a script or due to something like a conversion failure), the runtime is placed into an "exception state."</span></span> <span data-ttu-id="5546f-112">Alle Aufrufe in alle von der Laufzeit erstellten Kontexte (mit Ausnahme der Ausnahme-APIs) können `JsErrorInExceptionState` bis zum Löschen der Ausnahme fehlschlagen.</span><span class="sxs-lookup"><span data-stu-id="5546f-112">All calls into any context created by the runtime (except for the exception APIs) will fail with `JsErrorInExceptionState` until the exception is cleared.</span></span>  
  
 <span data-ttu-id="5546f-113">Wenn sich die Laufzeit des aktuellen Kontexts im Ausnahmezustand befindet, wenn ein Rückruf in das Modul zurückgegeben wird, löst das Modul automatisch die Ausnahme aus.</span><span class="sxs-lookup"><span data-stu-id="5546f-113">If the runtime of the current context is in the exception state when a callback returns into the engine, the engine will automatically rethrow the exception.</span></span>  
  
 <span data-ttu-id="5546f-114">Erfordert einen aktiven Skriptkontext.</span><span class="sxs-lookup"><span data-stu-id="5546f-114">Requires an active script context.</span></span>  
  
## <span data-ttu-id="5546f-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5546f-115">Requirements</span></span>  
 <span data-ttu-id="5546f-116">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="5546f-116">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="5546f-117">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="5546f-117">See Also</span></span>  
 [<span data-ttu-id="5546f-118">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="5546f-118">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
