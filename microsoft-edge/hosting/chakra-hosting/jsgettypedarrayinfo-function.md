---
description: Ruft häufig verwendete Eigenschaften eines typisierten Arrays ab.
title: JsGetTypedArrayInfo-Funktion | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 992bc4e9-3d06-4ad2-8b6b-88a437360f81
caps.latest.revision: 3
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 24046acc7118cd8f540ba8ceb9976368e93d51ff
ms.sourcegitcommit: 037a2d62333691104c9accb4862968f80a3465a2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/18/2020
ms.locfileid: "10752269"
---
# <span data-ttu-id="a9b41-103">JsGetTypedArrayInfo Funktion</span><span class="sxs-lookup"><span data-stu-id="a9b41-103">JsGetTypedArrayInfo Function</span></span>
<span data-ttu-id="a9b41-104">Ruft häufig verwendete Eigenschaften eines typisierten Arrays ab.</span><span class="sxs-lookup"><span data-stu-id="a9b41-104">Obtains frequently used properties of a typed array.</span></span>  
  
## <span data-ttu-id="a9b41-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a9b41-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetTypedArrayInfo(  
  _In_ JsValueRef typedArray,  
  _Out_opt_ JsTypedArrayType *arrayType,  
  _Out_opt_ JsValueRef *arrayBuffer,  
  _Out_opt_ unsigned int *byteOffset,  
  _Out_opt_ unsigned int *byteLength  
);  
  
```  
  
#### <span data-ttu-id="a9b41-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a9b41-106">Parameters</span></span>  
 `typedArray`  
 <span data-ttu-id="a9b41-107">Die typisierte Arrayinstanz.</span><span class="sxs-lookup"><span data-stu-id="a9b41-107">The typed array instance.</span></span>  
  
 `arrayType`  
 <span data-ttu-id="a9b41-108">Der Typ des Arrays.</span><span class="sxs-lookup"><span data-stu-id="a9b41-108">The type of the array.</span></span>  
  
 `arrayBuffer`  
 <span data-ttu-id="a9b41-109">Der `ArrayBuffer` Backstore des Arrays.</span><span class="sxs-lookup"><span data-stu-id="a9b41-109">The `ArrayBuffer` backstore of the array.</span></span>  
  
 `byteOffset`  
 <span data-ttu-id="a9b41-110">Der Offset in Bytes vom Anfang des arrayBuffer, auf den das Array verweist.</span><span class="sxs-lookup"><span data-stu-id="a9b41-110">The offset in bytes from the start of arrayBuffer referenced by the array.</span></span>  
  
 `byteLength`  
 <span data-ttu-id="a9b41-111">Die Anzahl der Bytes im Array.</span><span class="sxs-lookup"><span data-stu-id="a9b41-111">The number of bytes in the array.</span></span>  
  
## <span data-ttu-id="a9b41-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a9b41-112">Return Value</span></span>  
 <span data-ttu-id="a9b41-113">Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="a9b41-113">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="a9b41-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="a9b41-114">Remarks</span></span>  
 <span data-ttu-id="a9b41-115">Erfordert einen aktiven Skriptkontext.</span><span class="sxs-lookup"><span data-stu-id="a9b41-115">Requires an active script context.</span></span>  
  
## <span data-ttu-id="a9b41-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a9b41-116">Requirements</span></span>  
 <span data-ttu-id="a9b41-117">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="a9b41-117">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="a9b41-118">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="a9b41-118">See Also</span></span>  
 [<span data-ttu-id="a9b41-119">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="a9b41-119">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)