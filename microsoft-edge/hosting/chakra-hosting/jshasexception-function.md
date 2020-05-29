---
description: Bestimmt, ob sich die Laufzeit des aktuellen Kontexts in einem Ausnahmezustand befindet.
title: JsHasException-Funktion | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsHasException
helpviewer_keywords:
- JsHasException function
ms.assetid: ac7da3ce-c746-4154-bbb8-bcb0859a8d5b
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 25ddb8f9cc407dd414a6cd2210c315eb4dd7b141
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10568364"
---
# <span data-ttu-id="e4ea5-103">JsHasException-Funktion</span><span class="sxs-lookup"><span data-stu-id="e4ea5-103">JsHasException Function</span></span>
<span data-ttu-id="e4ea5-104">Bestimmt, ob sich die Laufzeit des aktuellen Kontexts in einem Ausnahmezustand befindet.</span><span class="sxs-lookup"><span data-stu-id="e4ea5-104">Determines whether the runtime of the current context is in an exception state.</span></span>  
  
## <span data-ttu-id="e4ea5-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e4ea5-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsHasException(  
   _Out_ bool *hasException  
);  
```  
  
#### <span data-ttu-id="e4ea5-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="e4ea5-106">Parameters</span></span>  
 `hasException`  
 <span data-ttu-id="e4ea5-107">Gibt an, ob sich die Laufzeit des aktuellen Kontexts im Ausnahmezustand befindet.</span><span class="sxs-lookup"><span data-stu-id="e4ea5-107">Whether the runtime of the current context is in the exception state.</span></span>  
  
## <span data-ttu-id="e4ea5-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e4ea5-108">Return Value</span></span>  
 <span data-ttu-id="e4ea5-109">Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="e4ea5-109">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="e4ea5-110">Hinweise</span><span class="sxs-lookup"><span data-stu-id="e4ea5-110">Remarks</span></span>  
 <span data-ttu-id="e4ea5-111">Wenn ein Aufruf der Laufzeit zu einer Ausnahme führt (entweder durch Ausführen eines Skripts oder aufgrund eines Konvertierungs Fehlers), wird die Common Language Runtime in einen "Ausnahmezustand" versetzt.</span><span class="sxs-lookup"><span data-stu-id="e4ea5-111">If a call into the runtime results in an exception (either as the result of running a script or due to something like a conversion failure), the runtime is placed into an "exception state."</span></span> <span data-ttu-id="e4ea5-112">Alle Aufrufe in alle von der Laufzeit erstellten Kontexte (mit Ausnahme der Ausnahme-APIs) können `JsErrorInExceptionState` bis zum Löschen der Ausnahme fehlschlagen.</span><span class="sxs-lookup"><span data-stu-id="e4ea5-112">All calls into any context created by the runtime (except for the exception APIs) will fail with `JsErrorInExceptionState` until the exception is cleared.</span></span>  
  
 <span data-ttu-id="e4ea5-113">Wenn sich die Laufzeit des aktuellen Kontexts im Ausnahmezustand befindet, wenn ein Rückruf in das Modul zurückgegeben wird, löst das Modul automatisch die Ausnahme aus.</span><span class="sxs-lookup"><span data-stu-id="e4ea5-113">If the runtime of the current context is in the exception state when a callback returns into the engine, the engine will automatically rethrow the exception.</span></span>  
  
 <span data-ttu-id="e4ea5-114">Erfordert einen aktiven Skriptkontext.</span><span class="sxs-lookup"><span data-stu-id="e4ea5-114">Requires an active script context.</span></span>  
  
## <span data-ttu-id="e4ea5-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e4ea5-115">Requirements</span></span>  
 <span data-ttu-id="e4ea5-116">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="e4ea5-116">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="e4ea5-117">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="e4ea5-117">See Also</span></span>  
 [<span data-ttu-id="e4ea5-118">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="e4ea5-118">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)