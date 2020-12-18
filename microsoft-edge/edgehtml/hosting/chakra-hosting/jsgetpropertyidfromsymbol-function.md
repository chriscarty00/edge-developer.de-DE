---
description: Ruft die dem Symbol zugeordnete Eigenschafts-ID ab.
title: JsGetPropertyIdFromSymbol-Funktion | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 190fe4b9-352e-4b10-9d0e-6c6bbd6363e8
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: d97f1fb517164d692cdd010f899dc40d2e3596ed
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11234136"
---
# <span data-ttu-id="85044-103">JsGetPropertyIdFromSymbol Funktion</span><span class="sxs-lookup"><span data-stu-id="85044-103">JsGetPropertyIdFromSymbol Function</span></span>

<span data-ttu-id="85044-104">Ruft die dem Symbol zugeordnete Eigenschafts-ID ab.</span><span class="sxs-lookup"><span data-stu-id="85044-104">Gets the property ID associated with the symbol.</span></span>  
  
## <span data-ttu-id="85044-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="85044-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetPropertyIdFromSymbol(  
   _In_ JsValueRef symbol,  
   _Out_ JsPropertyIdRef *propertyId  
);  
```  
  
#### <span data-ttu-id="85044-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="85044-106">Parameters</span></span>  
 `symbol`  
 <span data-ttu-id="85044-107">Das Symbol, dessen Eigenschafts-ID abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="85044-107">The symbol whose property ID is being retrieved.</span></span>  
  
 `propertyId`  
 <span data-ttu-id="85044-108">Die Eigenschafts-ID für das angegebene Symbol.</span><span class="sxs-lookup"><span data-stu-id="85044-108">The property ID for the given symbol.</span></span>  
  
## <span data-ttu-id="85044-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="85044-109">Return Value</span></span>  
 <span data-ttu-id="85044-110">Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="85044-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="85044-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="85044-111">Remarks</span></span>  
 <span data-ttu-id="85044-112">Eigenschafts-IDs sind für einen kontextspezifisch und können nicht in allen Kontexten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="85044-112">Property IDs are specific to a context and cannot be used across contexts.</span></span>  
  
 <span data-ttu-id="85044-113">Erfordert einen aktiven Skriptkontext.</span><span class="sxs-lookup"><span data-stu-id="85044-113">Requires an active script context.</span></span>  
  
 <span data-ttu-id="85044-114">Diese API wird nur im Microsoft Edge-Modus unterstützt.</span><span class="sxs-lookup"><span data-stu-id="85044-114">This API is supported only in Microsoft Edge mode.</span></span>  
  
## <span data-ttu-id="85044-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="85044-115">Requirements</span></span>  
 <span data-ttu-id="85044-116">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="85044-116">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="85044-117">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="85044-117">See Also</span></span>  
 [<span data-ttu-id="85044-118">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="85044-118">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
