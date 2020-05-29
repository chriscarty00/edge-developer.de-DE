---
description: Legt eine Fortsetzungs Rückruffunktion für Versprechen fest, die vom Kontext aufgerufen wird, wenn eine Aufgabe zur zukünftigen Ausführung in die Warteschlange gestellt werden soll.
title: JsSetPromiseContinuationCallback-Funktion | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 6ef0faf4-1500-4bd9-aeca-c208492af8ea
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 9438bf05d879b0c2014c0a4d49d374d26eff3fb4
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10568303"
---
# <span data-ttu-id="852b0-103">JsSetPromiseContinuationCallback-Funktion</span><span class="sxs-lookup"><span data-stu-id="852b0-103">JsSetPromiseContinuationCallback Function</span></span>
<span data-ttu-id="852b0-104">Legt eine Fortsetzungs Rückruffunktion für Versprechen fest, die vom Kontext aufgerufen wird, wenn eine Aufgabe zur zukünftigen Ausführung in die Warteschlange gestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="852b0-104">Sets a promise continuation callback function that is called by the context when a task needs to be queued for future execution.</span></span>  
  
## <span data-ttu-id="852b0-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="852b0-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsSetPromiseContinuationCallback(  
   _In_ JsPromiseContinuationCallback promiseContinuationCallback,  
   _In_opt_ void *callbackState  
);  
```  
  
#### <span data-ttu-id="852b0-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="852b0-106">Parameters</span></span>  
 `promiseContinuationCallback`  
 <span data-ttu-id="852b0-107">Die Rückruffunktion, die festzulegen ist.</span><span class="sxs-lookup"><span data-stu-id="852b0-107">The callback function being set.</span></span>  
  
 `callbackState`  
 <span data-ttu-id="852b0-108">Der Benutzer hat den Zustand bereitgestellt, der an den Rückruf zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="852b0-108">User provided state that will be passed back to the callback.</span></span>  
  
## <span data-ttu-id="852b0-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="852b0-109">Return Value</span></span>  
 <span data-ttu-id="852b0-110">Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="852b0-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="852b0-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="852b0-111">Remarks</span></span>  
 <span data-ttu-id="852b0-112">Erfordert einen aktiven Skriptkontext.</span><span class="sxs-lookup"><span data-stu-id="852b0-112">Requires an active script context.</span></span>  
  
 <span data-ttu-id="852b0-113">Diese API wird nur im EdgeHTML-Modus unterstützt.</span><span class="sxs-lookup"><span data-stu-id="852b0-113">This API is supported only in EdgeHTML mode.</span></span>  
  
## <span data-ttu-id="852b0-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="852b0-114">Requirements</span></span>  
 <span data-ttu-id="852b0-115">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="852b0-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="852b0-116">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="852b0-116">See Also</span></span>  
 [<span data-ttu-id="852b0-117">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="852b0-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)