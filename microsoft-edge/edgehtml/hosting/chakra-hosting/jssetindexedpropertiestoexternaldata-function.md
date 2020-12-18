---
description: Legt die indizierten Eigenschaften eines Objekts auf externe Daten fest. Die externen Daten werden als Back Store für die indizierten Eigenschaften des Objekts verwendet und auf wie ein typisiertes Array zugegriffen.
title: JsSetIndexedPropertiesToExternalData-Funktion | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: cee2d86d-ed42-4acb-86ef-95a67e63d0d6
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: fa0eba3659c20066913cd42a0a18dd5ffe5f857f
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233736"
---
# <span data-ttu-id="830f8-104">JsSetIndexedPropertiesToExternalData Funktion</span><span class="sxs-lookup"><span data-stu-id="830f8-104">JsSetIndexedPropertiesToExternalData Function</span></span>

<span data-ttu-id="830f8-105">Legt die indizierten Eigenschaften eines Objekts auf externe Daten fest.</span><span class="sxs-lookup"><span data-stu-id="830f8-105">Sets an object's indexed properties to external data.</span></span> <span data-ttu-id="830f8-106">Die externen Daten werden als Back Store für die indizierten Eigenschaften des Objekts verwendet und auf wie ein typisiertes Array zugegriffen.</span><span class="sxs-lookup"><span data-stu-id="830f8-106">The external data will be used as back store for the object's indexed properties and accessed like a typed array.</span></span>  
  
## <span data-ttu-id="830f8-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="830f8-107">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsSetIndexedPropertiesToExternalData(  
   _In_ JsValueRef object,  
   _In_ void* data,  
   _In_ JsTypedArrayType arrayType,  
   _In_ unsigned int elementLength  
);  
```  
  
#### <span data-ttu-id="830f8-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="830f8-108">Parameters</span></span>  
 `object`  
 <span data-ttu-id="830f8-109">Das Objekt, das ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="830f8-109">The object to operate on.</span></span>  
  
 `data`  
 <span data-ttu-id="830f8-110">Die externen Daten, die als Back Store für die indizierten Eigenschaften des Objekts verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="830f8-110">The external data to be used as back store for the object's indexed properties.</span></span>  
  
 `arrayType`  
 <span data-ttu-id="830f8-111">Der Arrayelementtyp in externen Daten.</span><span class="sxs-lookup"><span data-stu-id="830f8-111">The array element type in external data.</span></span>  
  
 `elementLength`  
 <span data-ttu-id="830f8-112">Die Anzahl der Arrayelemente in externen Daten.</span><span class="sxs-lookup"><span data-stu-id="830f8-112">The number of array elements in external data.</span></span>  
  
## <span data-ttu-id="830f8-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="830f8-113">Return Value</span></span>  
 <span data-ttu-id="830f8-114">Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="830f8-114">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="830f8-115">Hinweise</span><span class="sxs-lookup"><span data-stu-id="830f8-115">Remarks</span></span>  
 <span data-ttu-id="830f8-116">Erfordert einen aktiven Skriptkontext.</span><span class="sxs-lookup"><span data-stu-id="830f8-116">Requires an active script context.</span></span>  
  
 <span data-ttu-id="830f8-117">Diese API wird nur im EdgeHTML-Modus unterstützt.</span><span class="sxs-lookup"><span data-stu-id="830f8-117">This API is supported only in EdgeHTML mode.</span></span>  
  
## <span data-ttu-id="830f8-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="830f8-118">Requirements</span></span>  
 <span data-ttu-id="830f8-119">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="830f8-119">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="830f8-120">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="830f8-120">See Also</span></span>  
 [<span data-ttu-id="830f8-121">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="830f8-121">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
