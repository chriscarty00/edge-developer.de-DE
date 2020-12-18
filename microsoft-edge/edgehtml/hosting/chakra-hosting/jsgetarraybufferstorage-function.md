---
description: Ruft den zugrunde liegenden Speicher Speicher ab, der von einem ArrayBuffer verwendet wird.
title: JsGetArrayBufferStorage-Funktion | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 712ae298-36a9-47ef-b089-e51835c056bc
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 64b031a81506e68322759eff49da7467cac6f219
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233877"
---
# <span data-ttu-id="b15fe-103">JsGetArrayBufferStorage Funktion</span><span class="sxs-lookup"><span data-stu-id="b15fe-103">JsGetArrayBufferStorage Function</span></span>

<span data-ttu-id="b15fe-104">Ruft den zugrunde liegenden Speicher Speicher ab, der von einem verwendet wird `ArrayBuffer` .</span><span class="sxs-lookup"><span data-stu-id="b15fe-104">Obtains the underlying memory storage used by an `ArrayBuffer`.</span></span>  
  
## <span data-ttu-id="b15fe-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b15fe-105">Syntax</span></span>  
  
```cpp  
JsErrorCode STDAPI_ JsGetArrayBufferStorage(  
   _In_ JsValueRef arrayBuffer,  
   _Outptr_result_bytebuffer_(*bufferLength) BYTE **buffer,  
   _Out_ unsigned int *bufferLength  
);  
```  
  
#### <span data-ttu-id="b15fe-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="b15fe-106">Parameters</span></span>  
 `arrayBuffer`  
 <span data-ttu-id="b15fe-107">Die ArrayBuffer-Instanz.</span><span class="sxs-lookup"><span data-stu-id="b15fe-107">The ArrayBuffer instance.</span></span>  
  
 `buffer`  
 <span data-ttu-id="b15fe-108">Der ArrayBuffer-Puffer.</span><span class="sxs-lookup"><span data-stu-id="b15fe-108">The ArrayBuffer's buffer.</span></span> <span data-ttu-id="b15fe-109">Die Lebensdauer des zurückgegebenen Puffers entspricht der Lebensdauer von `ArrayBuffer` .</span><span class="sxs-lookup"><span data-stu-id="b15fe-109">The lifetime of the buffer returned is the same as the lifetime of the `ArrayBuffer`.</span></span> <span data-ttu-id="b15fe-110">Der Pufferzeiger zählt nicht als Verweis auf das `ArrayBuffer` zum Zweck der Garbage Collection.</span><span class="sxs-lookup"><span data-stu-id="b15fe-110">The buffer pointer does not count as a reference to the `ArrayBuffer` for the purpose of garbage collection.</span></span>  
  
 `bufferLength`  
 <span data-ttu-id="b15fe-111">Die Anzahl der Bytes im Puffer.</span><span class="sxs-lookup"><span data-stu-id="b15fe-111">The number of bytes in the buffer.</span></span>  
  
## <span data-ttu-id="b15fe-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b15fe-112">Return Value</span></span>  
 <span data-ttu-id="b15fe-113">Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="b15fe-113">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="b15fe-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="b15fe-114">Remarks</span></span>  
 <span data-ttu-id="b15fe-115">Erfordert einen aktiven Skriptkontext.</span><span class="sxs-lookup"><span data-stu-id="b15fe-115">Requires an active script context.</span></span>  
  
 <span data-ttu-id="b15fe-116">Diese API wird nur im Microsoft Edge-Modus unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b15fe-116">This API is supported only in Microsoft Edge mode.</span></span>  
  
## <span data-ttu-id="b15fe-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b15fe-117">Requirements</span></span>  
 <span data-ttu-id="b15fe-118">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="b15fe-118">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="b15fe-119">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="b15fe-119">See Also</span></span>  
 [<span data-ttu-id="b15fe-120">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="b15fe-120">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
