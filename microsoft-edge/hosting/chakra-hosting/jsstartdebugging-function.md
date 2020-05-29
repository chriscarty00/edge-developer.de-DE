---
description: Startet das Debuggen im aktuellen Kontext.
title: JsStartDebugging-Funktion | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsStartDebugging
helpviewer_keywords:
- JsStartDebugging function
ms.assetid: c48ba02d-6d47-466f-a970-02f087d525f3
caps.latest.revision: 15
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 2c94a6f36ad72bfb9354c85d98ae0b5b4e9c77fb
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10568206"
---
# <span data-ttu-id="156e4-103">JsStartDebugging-Funktion</span><span class="sxs-lookup"><span data-stu-id="156e4-103">JsStartDebugging Function</span></span>
<span data-ttu-id="156e4-104">Startet das Debuggen im aktuellen Kontext.</span><span class="sxs-lookup"><span data-stu-id="156e4-104">Starts debugging in the current context.</span></span>  
  
## <span data-ttu-id="156e4-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="156e4-105">Syntax</span></span>  
  
```cpp  
// Microsoft Edge mode signature  
STDAPI_(JsErrorCode) JsStartDebugging();  
  
// Legacy mode signature  
STDAPI_(JsErrorCode)  JsStartDebugging(  
   _In_ IDebugApplication *debugApplication  
);  
```  
  
#### <span data-ttu-id="156e4-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="156e4-106">Parameters</span></span>  
 `debugApplication`  
 <span data-ttu-id="156e4-107">Die für das Debuggen zu verwendende Debug-Anwendung.</span><span class="sxs-lookup"><span data-stu-id="156e4-107">The debug application to use for debugging.</span></span>  
  
## <span data-ttu-id="156e4-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="156e4-108">Return Value</span></span>  
 <span data-ttu-id="156e4-109">Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="156e4-109">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="156e4-110">Hinweise</span><span class="sxs-lookup"><span data-stu-id="156e4-110">Remarks</span></span>  
 <span data-ttu-id="156e4-111">Der Host sollte sicherstellen, dass `CoInitializeEx` mit `COINIT_MULTITHREADED` oder mindestens `COINIT_APARTMENTTHREADED` einmal vor der Verwendung dieser API aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="156e4-111">The host should make sure that `CoInitializeEx` is called with `COINIT_MULTITHREADED` or `COINIT_APARTMENTTHREADED` at least once before using this API</span></span>  
  
 <span data-ttu-id="156e4-112">Der `debugApplication` Parameter wird im Microsoft Edge-Modus nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="156e4-112">The `debugApplication` parameter is not supported in Microsoft Edge mode.</span></span> <span data-ttu-id="156e4-113">Weitere Informationen zur Verwendung dieser API im Microsoft Edge-Modus finden Sie unter [Targeting Microsoft Edge vs. Legacy Engines](../chakra-hosting/targeting-edge-vs-legacy-engines-in-jsrt-apis.md).</span><span class="sxs-lookup"><span data-stu-id="156e4-113">For more information on using this API in Microsoft Edge mode, see [Targeting Microsoft Edge vs. Legacy Engines](../chakra-hosting/targeting-edge-vs-legacy-engines-in-jsrt-apis.md).</span></span>  
  
## <span data-ttu-id="156e4-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="156e4-114">Requirements</span></span>  
 <span data-ttu-id="156e4-115">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="156e4-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="156e4-116">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="156e4-116">See Also</span></span>  
 [<span data-ttu-id="156e4-117">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="156e4-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)