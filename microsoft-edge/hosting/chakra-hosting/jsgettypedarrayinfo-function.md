---
description: Ruft häufig verwendete Eigenschaften eines typisierten Arrays ab.
title: JsGetTypedArrayInfo-Funktion | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: 992bc4e9-3d06-4ad2-8b6b-88a437360f81
caps.latest.revision: 3
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: b33b0c515733864c1849a08aa2f8dc6e884c22ad
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10567234"
---
# <span data-ttu-id="9a48d-103">JsGetTypedArrayInfo-Funktion</span><span class="sxs-lookup"><span data-stu-id="9a48d-103">JsGetTypedArrayInfo Function</span></span>
<span data-ttu-id="9a48d-104">Ruft häufig verwendete Eigenschaften eines typisierten Arrays ab.</span><span class="sxs-lookup"><span data-stu-id="9a48d-104">Obtains frequently used properties of a typed array.</span></span>  
  
## <span data-ttu-id="9a48d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="9a48d-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetTypedArrayInfo(  
  _In_ JsValueRef typedArray,  
  _Out_opt_ JsTypedArrayType *arrayType,  
  _Out_opt_ JsValueRef *arrayBuffer,  
  _Out_opt_ unsigned int *byteOffset,  
  _Out_opt_ unsigned int *byteLength  
);  
  
```  
  
#### <span data-ttu-id="9a48d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="9a48d-106">Parameters</span></span>  
 `typedArray`  
 <span data-ttu-id="9a48d-107">Die typisierte Arrayinstanz.</span><span class="sxs-lookup"><span data-stu-id="9a48d-107">The typed array instance.</span></span>  
  
 `arrayType`  
 <span data-ttu-id="9a48d-108">Der Typ des Arrays.</span><span class="sxs-lookup"><span data-stu-id="9a48d-108">The type of the array.</span></span>  
  
 `arrayBuffer`  
 <span data-ttu-id="9a48d-109">Der `ArrayBuffer` Backstore des Arrays.</span><span class="sxs-lookup"><span data-stu-id="9a48d-109">The `ArrayBuffer` backstore of the array.</span></span>  
  
 `byteOffset`  
 <span data-ttu-id="9a48d-110">Der Offset in Bytes vom Anfang des arrayBuffer, auf den das Array verweist.</span><span class="sxs-lookup"><span data-stu-id="9a48d-110">The offset in bytes from the start of arrayBuffer referenced by the array.</span></span>  
  
 `byteLength`  
 <span data-ttu-id="9a48d-111">Die Anzahl der Bytes im Array.</span><span class="sxs-lookup"><span data-stu-id="9a48d-111">The number of bytes in the array.</span></span>  
  
## <span data-ttu-id="9a48d-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9a48d-112">Return Value</span></span>  
 <span data-ttu-id="9a48d-113">Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="9a48d-113">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="9a48d-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="9a48d-114">Remarks</span></span>  
 <span data-ttu-id="9a48d-115">Erfordert einen aktiven Skriptkontext.</span><span class="sxs-lookup"><span data-stu-id="9a48d-115">Requires an active script context.</span></span>  
  
## <span data-ttu-id="9a48d-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9a48d-116">Requirements</span></span>  
 <span data-ttu-id="9a48d-117">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="9a48d-117">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="9a48d-118">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="9a48d-118">See Also</span></span>  
 [<span data-ttu-id="9a48d-119">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="9a48d-119">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)