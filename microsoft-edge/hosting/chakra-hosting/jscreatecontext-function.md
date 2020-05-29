---
description: Erstellt einen Skriptkontext zum Ausführen von Skripts.
title: JsCreateContext-Funktion | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsCreateContext
helpviewer_keywords:
- JsCreateContext function
ms.assetid: aceca043-2c73-4029-a06c-8ad6695109cf
caps.latest.revision: 15
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 06bd4c4780a8c7610ebc95cfc0da058306ce5b78
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10567309"
---
# <span data-ttu-id="04c02-103">JsCreateContext-Funktion</span><span class="sxs-lookup"><span data-stu-id="04c02-103">JsCreateContext Function</span></span>
<span data-ttu-id="04c02-104">Erstellt einen Skriptkontext zum Ausführen von Skripts.</span><span class="sxs-lookup"><span data-stu-id="04c02-104">Creates a script context for running scripts.</span></span>  
  
## <span data-ttu-id="04c02-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="04c02-105">Syntax</span></span>  
  
```cpp  
// Microsoft Edge mode signature  
STDAPI_(JsErrorCode) JsCreateContext(  
   _In_ JsRuntimeHandle runtime,  
   _Out_ JsContextRef *newContext);  
  
// Legacy mode signature  
STDAPI_(JsErrorCode) JsCreateContext(  
   _In_ JsRuntimeHandle runtime,  
   _In_ IDebugApplication *debugApplication,  
   _Out_ JsContextRef *newContext  
);  
```  
  
#### <span data-ttu-id="04c02-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="04c02-106">Parameters</span></span>  
 `runtime`  
 <span data-ttu-id="04c02-107">Die Laufzeit, in der der Skriptkontext erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="04c02-107">The runtime the script context is being created in.</span></span>  
  
 `debugApplication`  
 <span data-ttu-id="04c02-108">Die für das Debuggen zu verwendende Debug-Anwendung.</span><span class="sxs-lookup"><span data-stu-id="04c02-108">The debug application to use for debugging.</span></span> <span data-ttu-id="04c02-109">Dieser Parameter kann NULL sein, in diesem Fall ist das Debuggen für den Kontext nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="04c02-109">This parameter can be null, in which case debugging is not enabled for the context.</span></span>  
  
 `newContext`  
 <span data-ttu-id="04c02-110">Der erstellte Skriptkontext.</span><span class="sxs-lookup"><span data-stu-id="04c02-110">The created script context.</span></span>  
  
## <span data-ttu-id="04c02-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="04c02-111">Return Value</span></span>  
 <span data-ttu-id="04c02-112">Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="04c02-112">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="04c02-113">Hinweise</span><span class="sxs-lookup"><span data-stu-id="04c02-113">Remarks</span></span>  
 <span data-ttu-id="04c02-114">Jeder Skriptkontext verfügt über ein eigenes globales Objekt, das von allen anderen Skript Kontexten isoliert ist.</span><span class="sxs-lookup"><span data-stu-id="04c02-114">Each script context has its own global object that is isolated from all other script contexts.</span></span>  
  
 <span data-ttu-id="04c02-115">Der `debugApplication` Parameter wird im Microsoft Edge-Modus nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="04c02-115">The `debugApplication` parameter is not supported in Microsoft Edge mode.</span></span> <span data-ttu-id="04c02-116">Weitere Informationen zur Verwendung dieser API im Microsoft Edge-Modus finden Sie unter [Targeting Microsoft Edge vs. Legacy Engines](../chakra-hosting/targeting-edge-vs-legacy-engines-in-jsrt-apis.md).</span><span class="sxs-lookup"><span data-stu-id="04c02-116">For more information on using this API in Microsoft Edge mode, see [Targeting Microsoft Edge vs. Legacy Engines](../chakra-hosting/targeting-edge-vs-legacy-engines-in-jsrt-apis.md).</span></span>  
  
## <span data-ttu-id="04c02-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="04c02-117">Requirements</span></span>  
 <span data-ttu-id="04c02-118">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="04c02-118">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="04c02-119">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="04c02-119">See Also</span></span>  
 [<span data-ttu-id="04c02-120">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="04c02-120">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)