---
description: Gibt die Ausnahme zurück, die dazu geführt hat, dass sich die Laufzeit des aktuellen Kontexts im Ausnahmezustand befindet, und setzt den Ausnahmezustand für diese Runtime zurück.
title: JsGetAndClearException-Funktion | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsGetAndClearException
helpviewer_keywords:
- JsGetAndClearException function
ms.assetid: 6aec8a88-41ee-47f6-b5f4-32f3cae6bb7b
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: cb296ea351d0466a856d5ac020550ebacc254ac9
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233876"
---
# <span data-ttu-id="b8aaa-103">JsGetAndClearException Funktion</span><span class="sxs-lookup"><span data-stu-id="b8aaa-103">JsGetAndClearException Function</span></span>

<span data-ttu-id="b8aaa-104">Gibt die Ausnahme zurück, die dazu geführt hat, dass sich die Laufzeit des aktuellen Kontexts im Ausnahmezustand befindet, und setzt den Ausnahmezustand für diese Runtime zurück.</span><span class="sxs-lookup"><span data-stu-id="b8aaa-104">Returns the exception that caused the runtime of the current context to be in the exception state and resets the exception state for that runtime.</span></span>  
  
## <span data-ttu-id="b8aaa-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b8aaa-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetAndClearException(  
   _Out_ JsValueRef *exception  
);  
```  
  
#### <span data-ttu-id="b8aaa-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="b8aaa-106">Parameters</span></span>  
 `exception`  
 <span data-ttu-id="b8aaa-107">Die Ausnahme für die Common Language Runtime des aktuellen Kontexts.</span><span class="sxs-lookup"><span data-stu-id="b8aaa-107">The exception for the runtime of the current context.</span></span>  
  
## <span data-ttu-id="b8aaa-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b8aaa-108">Return Value</span></span>  
 <span data-ttu-id="b8aaa-109">Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="b8aaa-109">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="b8aaa-110">Hinweise</span><span class="sxs-lookup"><span data-stu-id="b8aaa-110">Remarks</span></span>  
 <span data-ttu-id="b8aaa-111">Wenn sich die Laufzeit des aktuellen Kontexts nicht in einem Ausnahmezustand befindet, gibt diese API zurück `JsErrorInvalidArgument` .</span><span class="sxs-lookup"><span data-stu-id="b8aaa-111">If the runtime of the current context is not in an exception state, this API will return `JsErrorInvalidArgument`.</span></span> <span data-ttu-id="b8aaa-112">Wenn die Common Language Runtime deaktiviert ist, wird eine Ausnahme zurückgegeben, die besagt, dass das Skript beendet wurde, aber die Ausnahme wird nicht gelöscht (die Ausnahme wird gelöscht, wenn die Common Language Runtime mithilfe von erneut aktiviert wird `JsEnableRuntimeExecution` ).</span><span class="sxs-lookup"><span data-stu-id="b8aaa-112">If the runtime is disabled, this will return an exception indicating that the script was terminated, but it will not clear the exception (the exception will be cleared if the runtime is re-enabled using `JsEnableRuntimeExecution`).</span></span>  
  
 <span data-ttu-id="b8aaa-113">Erfordert einen aktiven Skriptkontext.</span><span class="sxs-lookup"><span data-stu-id="b8aaa-113">Requires an active script context.</span></span>  
  
## <span data-ttu-id="b8aaa-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b8aaa-114">Requirements</span></span>  
 <span data-ttu-id="b8aaa-115">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="b8aaa-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="b8aaa-116">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="b8aaa-116">See Also</span></span>  
 [<span data-ttu-id="b8aaa-117">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="b8aaa-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
