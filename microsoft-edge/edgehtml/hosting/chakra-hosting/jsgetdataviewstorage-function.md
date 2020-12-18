---
description: Ruft den zugrunde liegenden Speicher Speicher ab, der von einer DataView verwendet wird.
title: JsGetDataViewStorage-Funktion | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 7c2180e0-51d5-4cc8-ad21-8bf29ff7c583
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 55f357e4a94b1edbc417ebb14ab99db11083dff4
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233998"
---
# <span data-ttu-id="a817b-103">JsGetDataViewStorage Funktion</span><span class="sxs-lookup"><span data-stu-id="a817b-103">JsGetDataViewStorage Function</span></span>

<span data-ttu-id="a817b-104">Ruft den zugrunde liegenden Speicher Speicher ab, der von einem verwendet wird `DataView` .</span><span class="sxs-lookup"><span data-stu-id="a817b-104">Obtains the underlying memory storage used by a `DataView`.</span></span>  
  
## <span data-ttu-id="a817b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a817b-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetDataViewStorage(  
   _In_ JsValueRef dataView,  
   _Outptr_result_bytebuffer_(*bufferLength) BYTE **buffer,  
   _Out_ unsigned int *bufferLength  
);  
```  
  
#### <span data-ttu-id="a817b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a817b-106">Parameters</span></span>  
 `dataView`  
 <span data-ttu-id="a817b-107">Die DataView-Instanz.</span><span class="sxs-lookup"><span data-stu-id="a817b-107">The DataView instance.</span></span>  
  
 `buffer`  
 <span data-ttu-id="a817b-108">Der DataView-Puffer.</span><span class="sxs-lookup"><span data-stu-id="a817b-108">The DataView's buffer.</span></span> <span data-ttu-id="a817b-109">Die Lebensdauer des zurückgegebenen Puffers entspricht der Lebensdauer von `DataView` .</span><span class="sxs-lookup"><span data-stu-id="a817b-109">The lifetime of the buffer returned is the same as the lifetime of the `DataView`.</span></span> <span data-ttu-id="a817b-110">Der Pufferzeiger zählt nicht als Verweis auf das `DataView` zum Zweck der Garbage Collection.</span><span class="sxs-lookup"><span data-stu-id="a817b-110">The buffer pointer does not count as a reference to the `DataView` for the purpose of garbage collection.</span></span>  
  
 `bufferLength`  
 <span data-ttu-id="a817b-111">Die Anzahl der Bytes im Puffer.</span><span class="sxs-lookup"><span data-stu-id="a817b-111">The number of bytes in the buffer.</span></span>  
  
## <span data-ttu-id="a817b-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a817b-112">Return Value</span></span>  
 <span data-ttu-id="a817b-113">Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="a817b-113">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="a817b-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="a817b-114">Remarks</span></span>  
 <span data-ttu-id="a817b-115">Erfordert einen aktiven Skriptkontext.</span><span class="sxs-lookup"><span data-stu-id="a817b-115">Requires an active script context.</span></span>  
  
 <span data-ttu-id="a817b-116">Diese API wird nur im Microsoft Edge-Modus unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a817b-116">This API is supported only in Microsoft Edge mode.</span></span>  
  
## <span data-ttu-id="a817b-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a817b-117">Requirements</span></span>  
 <span data-ttu-id="a817b-118">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="a817b-118">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="a817b-119">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="a817b-119">See Also</span></span>  
 [<span data-ttu-id="a817b-120">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="a817b-120">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
