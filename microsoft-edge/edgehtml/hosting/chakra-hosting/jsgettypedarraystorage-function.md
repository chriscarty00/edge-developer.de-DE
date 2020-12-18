---
description: Ruft den zugrunde liegenden Speicher Speicher ab, der von einem typisierten Array verwendet wird.
title: JsGetTypedArrayStorage-Funktion | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 52e4ac5f-cc71-456d-95de-a48f7327503d
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 442727228433368de14bac528ea416fcc2a95fa8
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233614"
---
# <span data-ttu-id="8d754-103">JsGetTypedArrayStorage Funktion</span><span class="sxs-lookup"><span data-stu-id="8d754-103">JsGetTypedArrayStorage Function</span></span>

<span data-ttu-id="8d754-104">Ruft den zugrunde liegenden Speicher Speicher ab, der von einem typisierten Array verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="8d754-104">Obtains the underlying memory storage used by a typed array.</span></span>  
  
## <span data-ttu-id="8d754-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="8d754-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetTypedArrayStorage(  
   _In_ JsValueRef typedArray,  
   _Outptr_result_bytebuffer_(*bufferLength) BYTE **buffer,  
   _Out_ unsigned int *bufferLength,  
   _Out_opt_ JsTypedArrayType *arrayType,  
   _Out_opt_ int *elementSize  
);  
```  
  
#### <span data-ttu-id="8d754-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="8d754-106">Parameters</span></span>  
 `typedArray`  
 <span data-ttu-id="8d754-107">Die typisierte Arrayinstanz.</span><span class="sxs-lookup"><span data-stu-id="8d754-107">The typed array instance.</span></span>  
  
 `buffer`  
 <span data-ttu-id="8d754-108">Der Puffer des Arrays.</span><span class="sxs-lookup"><span data-stu-id="8d754-108">The array's buffer.</span></span> <span data-ttu-id="8d754-109">Die Lebensdauer des zurückgegebenen Puffers ist mit der Lebensdauer des Arrays identisch.</span><span class="sxs-lookup"><span data-stu-id="8d754-109">The lifetime of the buffer returned is the same as the lifetime of the array.</span></span> <span data-ttu-id="8d754-110">Der Pufferzeiger zählt nicht als Verweis auf das Array zum Zweck der Garbage Collection.</span><span class="sxs-lookup"><span data-stu-id="8d754-110">The buffer pointer does not count as a reference to the array for the purpose of garbage collection.</span></span>  
  
 `bufferLength`  
 <span data-ttu-id="8d754-111">Die Anzahl der Bytes im Puffer.</span><span class="sxs-lookup"><span data-stu-id="8d754-111">The number of bytes in the buffer.</span></span>  
  
 `arrayType`  
 <span data-ttu-id="8d754-112">Der Typ des Arrays.</span><span class="sxs-lookup"><span data-stu-id="8d754-112">The type of the array.</span></span>  
  
 `elementSize`  
 <span data-ttu-id="8d754-113">Die Größe eines Elements des Arrays.</span><span class="sxs-lookup"><span data-stu-id="8d754-113">The size of an element of the array.</span></span>  
  
## <span data-ttu-id="8d754-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8d754-114">Return Value</span></span>  
 <span data-ttu-id="8d754-115">Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="8d754-115">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="8d754-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="8d754-116">Remarks</span></span>  
 <span data-ttu-id="8d754-117">Erfordert einen aktiven Skriptkontext.</span><span class="sxs-lookup"><span data-stu-id="8d754-117">Requires an active script context.</span></span>  
  
 <span data-ttu-id="8d754-118">Diese API wird nur im Microsoft Edge-Modus unterstützt.</span><span class="sxs-lookup"><span data-stu-id="8d754-118">This API is supported only in Microsoft Edge mode.</span></span>  
  
## <span data-ttu-id="8d754-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8d754-119">Requirements</span></span>  
 <span data-ttu-id="8d754-120">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="8d754-120">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="8d754-121">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="8d754-121">See Also</span></span>  
 [<span data-ttu-id="8d754-122">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="8d754-122">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
