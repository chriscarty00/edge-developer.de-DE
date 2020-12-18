---
description: Erstellt eine neue Laufzeit.
title: JsCreateRuntime-Funktion | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsCreateRuntime
helpviewer_keywords:
- JsCreateRuntime function
ms.assetid: 92d09b89-6593-4d73-a562-88f9fec10228
caps.latest.revision: 15
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 3b893bd75725d6d9da56417ba83adfce18d77bac
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233971"
---
# <span data-ttu-id="aed1a-103">JsCreateRuntime Funktion</span><span class="sxs-lookup"><span data-stu-id="aed1a-103">JsCreateRuntime Function</span></span>

<span data-ttu-id="aed1a-104">Erstellt eine neue Laufzeit.</span><span class="sxs-lookup"><span data-stu-id="aed1a-104">Creates a new runtime.</span></span>
  
## <span data-ttu-id="aed1a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="aed1a-105">Syntax</span></span>  
  
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
  
#### <span data-ttu-id="aed1a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="aed1a-106">Parameters</span></span>  
 `attributes`  
 <span data-ttu-id="aed1a-107">Die Attribute der zu erstellende Laufzeit.</span><span class="sxs-lookup"><span data-stu-id="aed1a-107">The attributes of the runtime to be created.</span></span>  
  
 `version`  
 <span data-ttu-id="aed1a-108">Die Version der zu erstellende Laufzeit.</span><span class="sxs-lookup"><span data-stu-id="aed1a-108">The version of the runtime to be created.</span></span>  
  
 `threadService`  
 <span data-ttu-id="aed1a-109">Der Thread Dienst für die Laufzeit.</span><span class="sxs-lookup"><span data-stu-id="aed1a-109">The thread service for the runtime.</span></span> <span data-ttu-id="aed1a-110">Kann NULL sein.</span><span class="sxs-lookup"><span data-stu-id="aed1a-110">Can be null.</span></span>  
  
 `runtime`  
 <span data-ttu-id="aed1a-111">Die erstellte Laufzeit.</span><span class="sxs-lookup"><span data-stu-id="aed1a-111">The runtime created.</span></span>  
  
## <span data-ttu-id="aed1a-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="aed1a-112">Return Value</span></span>  
 <span data-ttu-id="aed1a-113">Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="aed1a-113">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="aed1a-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="aed1a-114">Remarks</span></span>  
 <span data-ttu-id="aed1a-115">Der `version` Parameter wird im Microsoft Edge-Modus nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="aed1a-115">The `version` parameter is not supported in Microsoft Edge mode.</span></span> <span data-ttu-id="aed1a-116">Weitere Informationen zur Verwendung dieser API im Microsoft Edge-Modus finden Sie unter [Targeting Microsoft Edge vs. Legacy Engines](../chakra-hosting/targeting-edge-vs-legacy-engines-in-jsrt-apis.md).</span><span class="sxs-lookup"><span data-stu-id="aed1a-116">For more information on using this API in Microsoft Edge mode, see [Targeting Microsoft Edge vs. Legacy Engines](../chakra-hosting/targeting-edge-vs-legacy-engines-in-jsrt-apis.md).</span></span>  
  
## <span data-ttu-id="aed1a-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="aed1a-117">Requirements</span></span>  
 <span data-ttu-id="aed1a-118">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="aed1a-118">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="aed1a-119">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="aed1a-119">See Also</span></span>  
 [<span data-ttu-id="aed1a-120">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="aed1a-120">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
