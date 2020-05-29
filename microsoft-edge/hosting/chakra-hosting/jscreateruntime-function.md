---
description: Erstellt eine neue Laufzeit.
title: JsCreateRuntime-Funktion | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsCreateRuntime
helpviewer_keywords:
- JsCreateRuntime function
ms.assetid: 92d09b89-6593-4d73-a562-88f9fec10228
caps.latest.revision: 15
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: d25c1b46354be1fda0ce906dc68c3643989fe2c6
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10567289"
---
# <span data-ttu-id="bd2f4-103">JsCreateRuntime-Funktion</span><span class="sxs-lookup"><span data-stu-id="bd2f4-103">JsCreateRuntime Function</span></span>
<span data-ttu-id="bd2f4-104">Erstellt eine neue Laufzeit.</span><span class="sxs-lookup"><span data-stu-id="bd2f4-104">Creates a new runtime.</span></span>
  
## <span data-ttu-id="bd2f4-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="bd2f4-105">Syntax</span></span>  
  
```cpp  
// Microsoft Edge mode signature  
STDAPI_(JsErrorCode) JsCreateRuntime(  
   _In_ JsRuntimeAttributes attributes,  
   _In_opt_ JsThreadServiceCallback threadService,  
   _Out_ JsRuntimeHandle *runtime);  
  
// Legacy mode signature  
STDAPI_(JsErrorCode) JsCreateRuntime(  
   _In_ JsRuntimeAttributes attributes,  
   _In_ JsRuntimeVersion version,  
   _In_opt_ JsThreadServiceCallback threadService,  
   _Out_ JsRuntimeHandle *runtime  
);  
```  
  
#### <span data-ttu-id="bd2f4-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="bd2f4-106">Parameters</span></span>  
 `attributes`  
 <span data-ttu-id="bd2f4-107">Die Attribute der zu erstellende Laufzeit.</span><span class="sxs-lookup"><span data-stu-id="bd2f4-107">The attributes of the runtime to be created.</span></span>  
  
 `version`  
 <span data-ttu-id="bd2f4-108">Die Version der zu erstellende Laufzeit.</span><span class="sxs-lookup"><span data-stu-id="bd2f4-108">The version of the runtime to be created.</span></span>  
  
 `threadService`  
 <span data-ttu-id="bd2f4-109">Der Thread Dienst für die Laufzeit.</span><span class="sxs-lookup"><span data-stu-id="bd2f4-109">The thread service for the runtime.</span></span> <span data-ttu-id="bd2f4-110">Kann NULL sein.</span><span class="sxs-lookup"><span data-stu-id="bd2f4-110">Can be null.</span></span>  
  
 `runtime`  
 <span data-ttu-id="bd2f4-111">Die erstellte Laufzeit.</span><span class="sxs-lookup"><span data-stu-id="bd2f4-111">The runtime created.</span></span>  
  
## <span data-ttu-id="bd2f4-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bd2f4-112">Return Value</span></span>  
 <span data-ttu-id="bd2f4-113">Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="bd2f4-113">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="bd2f4-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="bd2f4-114">Remarks</span></span>  
 <span data-ttu-id="bd2f4-115">Der `version` Parameter wird im Microsoft Edge-Modus nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="bd2f4-115">The `version` parameter is not supported in Microsoft Edge mode.</span></span> <span data-ttu-id="bd2f4-116">Weitere Informationen zur Verwendung dieser API im Microsoft Edge-Modus finden Sie unter [Targeting Microsoft Edge vs. Legacy Engines](../chakra-hosting/targeting-edge-vs-legacy-engines-in-jsrt-apis.md).</span><span class="sxs-lookup"><span data-stu-id="bd2f4-116">For more information on using this API in Microsoft Edge mode, see [Targeting Microsoft Edge vs. Legacy Engines](../chakra-hosting/targeting-edge-vs-legacy-engines-in-jsrt-apis.md).</span></span>  
  
## <span data-ttu-id="bd2f4-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bd2f4-117">Requirements</span></span>  
 <span data-ttu-id="bd2f4-118">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="bd2f4-118">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="bd2f4-119">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="bd2f4-119">See Also</span></span>  
 [<span data-ttu-id="bd2f4-120">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="bd2f4-120">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)