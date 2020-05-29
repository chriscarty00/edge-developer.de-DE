---
description: Erstellt ein Array Objekt mit JavaScript-Typisierung.
title: JsCreateTypedArray-Funktion | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 937a2a91-6f5f-4aaa-a018-d3089702bf36
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 57c5d15d76bf8b3ff29d10f7500fe41b3e959f68
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10567281"
---
# <span data-ttu-id="15c4e-103">JsCreateTypedArray-Funktion</span><span class="sxs-lookup"><span data-stu-id="15c4e-103">JsCreateTypedArray Function</span></span>
<span data-ttu-id="15c4e-104">Erstellt ein Array Objekt mit JavaScript-Typisierung.</span><span class="sxs-lookup"><span data-stu-id="15c4e-104">Creates a JavaScript typed array object.</span></span>  
  
## <span data-ttu-id="15c4e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="15c4e-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsCreateTypedArray(  
   _In_ JsTypedArrayType arrayType,  
   _In_ JsValueRef baseArray,  
   _In_ unsigned int byteOffset,  
   _In_ unsigned int elementLength,  
   _Out_ JsValueRef *result  
);  
```  
  
#### <span data-ttu-id="15c4e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="15c4e-106">Parameters</span></span>  
 `arrayType`  
 <span data-ttu-id="15c4e-107">Der Typ des zu erstellenden Array.</span><span class="sxs-lookup"><span data-stu-id="15c4e-107">The type of the array to create.</span></span>  
  
 `baseArray`  
 <span data-ttu-id="15c4e-108">Das Basisarray des neuen Arrays.</span><span class="sxs-lookup"><span data-stu-id="15c4e-108">The base array of the new array.</span></span> <span data-ttu-id="15c4e-109">Verwenden Sie `JS_INVALID_REFERENCE` Wenn kein Basisarray.</span><span class="sxs-lookup"><span data-stu-id="15c4e-109">Use `JS_INVALID_REFERENCE` if no base array.</span></span>  
  
 `byteOffset`  
 <span data-ttu-id="15c4e-110">Der Offset in Bytes ab dem Anfang `baseArray` ( `ArrayBuffer` ) für das Ergebnis typisierte Array, auf das verwiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="15c4e-110">The offset in bytes from the start of `baseArray` (`ArrayBuffer`) for result typed array to reference.</span></span> <span data-ttu-id="15c4e-111">Nur zutreffend `baseArray` , wenn es sich um ein `ArrayBuffer` Objekt handelt.</span><span class="sxs-lookup"><span data-stu-id="15c4e-111">Only applicable when `baseArray` is an `ArrayBuffer` object.</span></span> <span data-ttu-id="15c4e-112">Muss andernfalls 0 sein.</span><span class="sxs-lookup"><span data-stu-id="15c4e-112">Must be 0 otherwise.</span></span>  
  
 `elementLength`  
 <span data-ttu-id="15c4e-113">Die Anzahl der Elemente im Array.</span><span class="sxs-lookup"><span data-stu-id="15c4e-113">The number of elements in the array.</span></span> <span data-ttu-id="15c4e-114">Nur anwendbar beim Erstellen eines neuen typisierten Arrays ohne `baseArray` ( `baseArray` ist `JS_INVALID_REFERENCE` ) oder wenn `baseArray` es sich um ein Objekt handelt `ArrayBuffer` .</span><span class="sxs-lookup"><span data-stu-id="15c4e-114">Only applicable when creating a new typed array without `baseArray` (`baseArray` is `JS_INVALID_REFERENCE`) or when `baseArray` is an `ArrayBuffer` object.</span></span> <span data-ttu-id="15c4e-115">Muss andernfalls 0 sein.</span><span class="sxs-lookup"><span data-stu-id="15c4e-115">Must be 0 otherwise.</span></span>  
  
 `result`  
 <span data-ttu-id="15c4e-116">Das neue typisierte Array Objekt.</span><span class="sxs-lookup"><span data-stu-id="15c4e-116">The new typed array object.</span></span>  
  
## <span data-ttu-id="15c4e-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="15c4e-117">Return Value</span></span>  
 <span data-ttu-id="15c4e-118">Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="15c4e-118">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="15c4e-119">Hinweise</span><span class="sxs-lookup"><span data-stu-id="15c4e-119">Remarks</span></span>  
 <span data-ttu-id="15c4e-120">Das `baseArray` kann ein `ArrayBuffer` , ein weiteres typisiertes Array oder ein JavaScript sein `Array` .</span><span class="sxs-lookup"><span data-stu-id="15c4e-120">The `baseArray` can be an `ArrayBuffer`, another typed array, or a JavaScript `Array`.</span></span> <span data-ttu-id="15c4e-121">Das zurückgegebene typisierte Array verwendet die `baseArray` Wenn es ein ist `ArrayBuffer` , oder auf andere Weise erstellen und verwenden Sie eine Kopie des zugrunde liegenden Quellarrays.</span><span class="sxs-lookup"><span data-stu-id="15c4e-121">The returned typed array will use the `baseArray` if it is an `ArrayBuffer`, or otherwise create and use a copy of the underlying source array.</span></span>  
  
 <span data-ttu-id="15c4e-122">Erfordert einen aktiven Skriptkontext.</span><span class="sxs-lookup"><span data-stu-id="15c4e-122">Requires an active script context.</span></span>  
  
 <span data-ttu-id="15c4e-123">Diese API wird nur im Microsoft Edge-Modus unterstützt.</span><span class="sxs-lookup"><span data-stu-id="15c4e-123">This API is supported only in Microsoft Edge mode.</span></span>  
  
## <span data-ttu-id="15c4e-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="15c4e-124">Requirements</span></span>  
 <span data-ttu-id="15c4e-125">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="15c4e-125">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="15c4e-126">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="15c4e-126">See Also</span></span>  
 [<span data-ttu-id="15c4e-127">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="15c4e-127">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)