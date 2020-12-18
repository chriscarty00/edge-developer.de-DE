---
description: Legt die internen Daten von JsrtContext fest.
title: JsSetContextData-Funktion | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: be90aa6a-b001-4a6f-90c5-c2135e913be0
caps.latest.revision: 4
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: cac404b9e79bafb5a8eafb47e893dbdf38a02405
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11234071"
---
# <span data-ttu-id="21340-103">JsSetContextData Funktion</span><span class="sxs-lookup"><span data-stu-id="21340-103">JsSetContextData Function</span></span>

<span data-ttu-id="21340-104">Legt die internen Daten von JsrtContext fest.</span><span class="sxs-lookup"><span data-stu-id="21340-104">Sets the internal data of JsrtContext.</span></span>  
  
## <span data-ttu-id="21340-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="21340-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsSetContextData(  
  _In_ JsContextRef context,  
  _In_ void *data  
);  
  
```  
  
#### <span data-ttu-id="21340-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="21340-106">Parameters</span></span>  
 `context`  
 <span data-ttu-id="21340-107">Der Kontext, auf den die Daten gesetzt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="21340-107">The context to set the data to.</span></span>  
  
 `data`  
 <span data-ttu-id="21340-108">Der Zeiger auf die Daten, die gesetzt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="21340-108">The pointer to the data to be set.</span></span>  
  
## <span data-ttu-id="21340-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="21340-109">Return Value</span></span>  
 <span data-ttu-id="21340-110">Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="21340-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="21340-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="21340-111">Remarks</span></span>  
 <span data-ttu-id="21340-112">Erfordert einen aktiven Skriptkontext.</span><span class="sxs-lookup"><span data-stu-id="21340-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="21340-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="21340-113">Requirements</span></span>  
 <span data-ttu-id="21340-114">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="21340-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="21340-115">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="21340-115">See Also</span></span>  
 [<span data-ttu-id="21340-116">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="21340-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
