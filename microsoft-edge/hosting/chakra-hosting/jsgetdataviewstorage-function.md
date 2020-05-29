---
description: Ruft den zugrunde liegenden Speicher Speicher ab, der von einer DataView verwendet wird.
title: JsGetDataViewStorage-Funktion | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 7c2180e0-51d5-4cc8-ad21-8bf29ff7c583
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 54f8a91b6dea1e0997ad31d6585ea741fde8ba99
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10567261"
---
# <span data-ttu-id="f1045-103">JsGetDataViewStorage-Funktion</span><span class="sxs-lookup"><span data-stu-id="f1045-103">JsGetDataViewStorage Function</span></span>
<span data-ttu-id="f1045-104">Ruft den zugrunde liegenden Speicher Speicher ab, der von einem verwendet wird `DataView` .</span><span class="sxs-lookup"><span data-stu-id="f1045-104">Obtains the underlying memory storage used by a `DataView`.</span></span>  
  
## <span data-ttu-id="f1045-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="f1045-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetDataViewStorage(  
   _In_ JsValueRef dataView,  
   _Outptr_result_bytebuffer_(*bufferLength) BYTE **buffer,  
   _Out_ unsigned int *bufferLength  
);  
```  
  
#### <span data-ttu-id="f1045-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="f1045-106">Parameters</span></span>  
 `dataView`  
 <span data-ttu-id="f1045-107">Die DataView-Instanz.</span><span class="sxs-lookup"><span data-stu-id="f1045-107">The DataView instance.</span></span>  
  
 `buffer`  
 <span data-ttu-id="f1045-108">Der DataView-Puffer.</span><span class="sxs-lookup"><span data-stu-id="f1045-108">The DataView's buffer.</span></span> <span data-ttu-id="f1045-109">Die Lebensdauer des zurückgegebenen Puffers entspricht der Lebensdauer von `DataView` .</span><span class="sxs-lookup"><span data-stu-id="f1045-109">The lifetime of the buffer returned is the same as the lifetime of the `DataView`.</span></span> <span data-ttu-id="f1045-110">Der Pufferzeiger zählt nicht als Verweis auf das `DataView` zum Zweck der Garbage Collection.</span><span class="sxs-lookup"><span data-stu-id="f1045-110">The buffer pointer does not count as a reference to the `DataView` for the purpose of garbage collection.</span></span>  
  
 `bufferLength`  
 <span data-ttu-id="f1045-111">Die Anzahl der Bytes im Puffer.</span><span class="sxs-lookup"><span data-stu-id="f1045-111">The number of bytes in the buffer.</span></span>  
  
## <span data-ttu-id="f1045-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f1045-112">Return Value</span></span>  
 <span data-ttu-id="f1045-113">Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="f1045-113">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="f1045-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="f1045-114">Remarks</span></span>  
 <span data-ttu-id="f1045-115">Erfordert einen aktiven Skriptkontext.</span><span class="sxs-lookup"><span data-stu-id="f1045-115">Requires an active script context.</span></span>  
  
 <span data-ttu-id="f1045-116">Diese API wird nur im Microsoft Edge-Modus unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f1045-116">This API is supported only in Microsoft Edge mode.</span></span>  
  
## <span data-ttu-id="f1045-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f1045-117">Requirements</span></span>  
 <span data-ttu-id="f1045-118">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="f1045-118">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="f1045-119">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="f1045-119">See Also</span></span>  
 [<span data-ttu-id="f1045-120">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="f1045-120">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)