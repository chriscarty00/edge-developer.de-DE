---
description: Ruft das Symbol ab, das der Eigenschafts-ID zugeordnet ist.
title: JsGetSymbolFromPropertyId-Funktion | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 0e822cb4-ba9e-44df-bf3a-fae97c354daa
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 472253aea228ca0374c42d99710a7a7ab528184c
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11234319"
---
# <span data-ttu-id="9c116-103">JsGetSymbolFromPropertyId Funktion</span><span class="sxs-lookup"><span data-stu-id="9c116-103">JsGetSymbolFromPropertyId Function</span></span>

<span data-ttu-id="9c116-104">Ruft das Symbol ab, das der Eigenschafts-ID zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="9c116-104">Gets the symbol associated with the property ID.</span></span>  
  
## <span data-ttu-id="9c116-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="9c116-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetSymbolFromPropertyId(  
   _In_ JsPropertyIdRef propertyId,  
   _Out_ JsValueRef *symbol  
);  
```  
  
#### <span data-ttu-id="9c116-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="9c116-106">Parameters</span></span>  
 `propertyId`  
 <span data-ttu-id="9c116-107">Die Eigenschafts-ID, deren Symbol abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="9c116-107">The property ID to get the symbol of.</span></span>  
  
 `symbol`  
 <span data-ttu-id="9c116-108">Das der Eigenschafts-ID zugeordnete Symbol.</span><span class="sxs-lookup"><span data-stu-id="9c116-108">The symbol associated with the property ID.</span></span>  
  
## <span data-ttu-id="9c116-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9c116-109">Return Value</span></span>  
 <span data-ttu-id="9c116-110">Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="9c116-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="9c116-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="9c116-111">Remarks</span></span>  
 <span data-ttu-id="9c116-112">Erfordert einen aktiven Skriptkontext.</span><span class="sxs-lookup"><span data-stu-id="9c116-112">Requires an active script context.</span></span>  
  
 <span data-ttu-id="9c116-113">Diese API wird nur im Microsoft Edge-Modus unterstützt.</span><span class="sxs-lookup"><span data-stu-id="9c116-113">This API is supported only in Microsoft Edge mode.</span></span>  
  
## <span data-ttu-id="9c116-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9c116-114">Requirements</span></span>  
 <span data-ttu-id="9c116-115">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="9c116-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="9c116-116">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="9c116-116">See Also</span></span>  
 [<span data-ttu-id="9c116-117">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="9c116-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
