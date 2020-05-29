---
description: Ruft die dem Symbol zugeordnete Eigenschafts-ID ab.
title: JsGetPropertyIdFromSymbol-Funktion | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 190fe4b9-352e-4b10-9d0e-6c6bbd6363e8
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 0d11dbaf25b85e2bcd85a0cf2bac1b499fd4fa3e
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10568380"
---
# <span data-ttu-id="4e4e8-103">JsGetPropertyIdFromSymbol-Funktion</span><span class="sxs-lookup"><span data-stu-id="4e4e8-103">JsGetPropertyIdFromSymbol Function</span></span>
<span data-ttu-id="4e4e8-104">Ruft die dem Symbol zugeordnete Eigenschafts-ID ab.</span><span class="sxs-lookup"><span data-stu-id="4e4e8-104">Gets the property ID associated with the symbol.</span></span>  
  
## <span data-ttu-id="4e4e8-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="4e4e8-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetPropertyIdFromSymbol(  
   _In_ JsValueRef symbol,  
   _Out_ JsPropertyIdRef *propertyId  
);  
```  
  
#### <span data-ttu-id="4e4e8-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="4e4e8-106">Parameters</span></span>  
 `symbol`  
 <span data-ttu-id="4e4e8-107">Das Symbol, dessen Eigenschafts-ID abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="4e4e8-107">The symbol whose property ID is being retrieved.</span></span>  
  
 `propertyId`  
 <span data-ttu-id="4e4e8-108">Die Eigenschafts-ID für das angegebene Symbol.</span><span class="sxs-lookup"><span data-stu-id="4e4e8-108">The property ID for the given symbol.</span></span>  
  
## <span data-ttu-id="4e4e8-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4e4e8-109">Return Value</span></span>  
 <span data-ttu-id="4e4e8-110">Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="4e4e8-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="4e4e8-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="4e4e8-111">Remarks</span></span>  
 <span data-ttu-id="4e4e8-112">Eigenschafts-IDs sind für einen kontextspezifisch und können nicht in allen Kontexten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4e4e8-112">Property IDs are specific to a context and cannot be used across contexts.</span></span>  
  
 <span data-ttu-id="4e4e8-113">Erfordert einen aktiven Skriptkontext.</span><span class="sxs-lookup"><span data-stu-id="4e4e8-113">Requires an active script context.</span></span>  
  
 <span data-ttu-id="4e4e8-114">Diese API wird nur im Microsoft Edge-Modus unterstützt.</span><span class="sxs-lookup"><span data-stu-id="4e4e8-114">This API is supported only in Microsoft Edge mode.</span></span>  
  
## <span data-ttu-id="4e4e8-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4e4e8-115">Requirements</span></span>  
 <span data-ttu-id="4e4e8-116">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="4e4e8-116">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="4e4e8-117">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="4e4e8-117">See Also</span></span>  
 [<span data-ttu-id="4e4e8-118">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="4e4e8-118">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)