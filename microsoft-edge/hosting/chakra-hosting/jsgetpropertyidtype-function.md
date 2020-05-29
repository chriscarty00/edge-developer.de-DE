---
description: Ruft den Typ der Eigenschaft ab.
title: JsGetPropertyIdType-Funktion | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 2b6e85ad-c630-4a07-a759-3b344d06faaa
caps.latest.revision: 3
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: a43cfc2efd69cc14813ad88850afbf602d477d71
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10568378"
---
# <span data-ttu-id="9c70e-103">JsGetPropertyIdType-Funktion</span><span class="sxs-lookup"><span data-stu-id="9c70e-103">JsGetPropertyIdType Function</span></span>
<span data-ttu-id="9c70e-104">Ruft den Typ der Eigenschaft ab.</span><span class="sxs-lookup"><span data-stu-id="9c70e-104">Gets the type of property.</span></span>  
  
## <span data-ttu-id="9c70e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="9c70e-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetPropertyIdType(  
   _In_ JsPropertyIdRef propertyId,  
   _Out_ JsPropertyIdType* propertyIdType  
);  
```  
  
#### <span data-ttu-id="9c70e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="9c70e-106">Parameters</span></span>  
 `propertyId`  
 <span data-ttu-id="9c70e-107">Die Eigenschafts-ID, deren Typ abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="9c70e-107">The property ID to get the type of.</span></span>  
  
 `propertyIdType`  
 <span data-ttu-id="9c70e-108">Die der `JsPropertyIdType` angegebenen Eigenschafts-ID.</span><span class="sxs-lookup"><span data-stu-id="9c70e-108">The `JsPropertyIdType` of the given property ID.</span></span>  
  
## <span data-ttu-id="9c70e-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9c70e-109">Return Value</span></span>  
 <span data-ttu-id="9c70e-110">Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="9c70e-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="9c70e-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="9c70e-111">Remarks</span></span>  
 <span data-ttu-id="9c70e-112">Erfordert einen aktiven Skriptkontext.</span><span class="sxs-lookup"><span data-stu-id="9c70e-112">Requires an active script context.</span></span>  
  
 <span data-ttu-id="9c70e-113">Diese API wird nur im Microsoft Edge-Modus unterstützt.</span><span class="sxs-lookup"><span data-stu-id="9c70e-113">This API is supported only in Microsoft Edge mode.</span></span>  
  
## <span data-ttu-id="9c70e-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9c70e-114">Requirements</span></span>  
 <span data-ttu-id="9c70e-115">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="9c70e-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="9c70e-116">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="9c70e-116">See Also</span></span>  
 [<span data-ttu-id="9c70e-117">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="9c70e-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)