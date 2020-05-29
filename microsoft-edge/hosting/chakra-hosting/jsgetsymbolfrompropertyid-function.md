---
description: Ruft das Symbol ab, das der Eigenschafts-ID zugeordnet ist.
title: JsGetSymbolFromPropertyId-Funktion | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 0e822cb4-ba9e-44df-bf3a-fae97c354daa
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 6902384772f29f80751660ce2d4a295d2ea620ab
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10567238"
---
# <span data-ttu-id="b5ea6-103">JsGetSymbolFromPropertyId-Funktion</span><span class="sxs-lookup"><span data-stu-id="b5ea6-103">JsGetSymbolFromPropertyId Function</span></span>
<span data-ttu-id="b5ea6-104">Ruft das Symbol ab, das der Eigenschafts-ID zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="b5ea6-104">Gets the symbol associated with the property ID.</span></span>  
  
## <span data-ttu-id="b5ea6-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b5ea6-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetSymbolFromPropertyId(  
   _In_ JsPropertyIdRef propertyId,  
   _Out_ JsValueRef *symbol  
);  
```  
  
#### <span data-ttu-id="b5ea6-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="b5ea6-106">Parameters</span></span>  
 `propertyId`  
 <span data-ttu-id="b5ea6-107">Die Eigenschafts-ID, deren Symbol abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="b5ea6-107">The property ID to get the symbol of.</span></span>  
  
 `symbol`  
 <span data-ttu-id="b5ea6-108">Das der Eigenschafts-ID zugeordnete Symbol.</span><span class="sxs-lookup"><span data-stu-id="b5ea6-108">The symbol associated with the property ID.</span></span>  
  
## <span data-ttu-id="b5ea6-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b5ea6-109">Return Value</span></span>  
 <span data-ttu-id="b5ea6-110">Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="b5ea6-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="b5ea6-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="b5ea6-111">Remarks</span></span>  
 <span data-ttu-id="b5ea6-112">Erfordert einen aktiven Skriptkontext.</span><span class="sxs-lookup"><span data-stu-id="b5ea6-112">Requires an active script context.</span></span>  
  
 <span data-ttu-id="b5ea6-113">Diese API wird nur im Microsoft Edge-Modus unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b5ea6-113">This API is supported only in Microsoft Edge mode.</span></span>  
  
## <span data-ttu-id="b5ea6-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b5ea6-114">Requirements</span></span>  
 <span data-ttu-id="b5ea6-115">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="b5ea6-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="b5ea6-116">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="b5ea6-116">See Also</span></span>  
 [<span data-ttu-id="b5ea6-117">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="b5ea6-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)