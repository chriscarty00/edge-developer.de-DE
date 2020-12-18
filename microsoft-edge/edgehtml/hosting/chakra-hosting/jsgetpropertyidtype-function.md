---
description: Ruft den Typ der Eigenschaft ab.
title: JsGetPropertyIdType-Funktion | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 2b6e85ad-c630-4a07-a759-3b344d06faaa
caps.latest.revision: 3
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 93ee11bf74014361c89aa93bbb58361b426f573f
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11234135"
---
# <span data-ttu-id="c8556-103">JsGetPropertyIdType Funktion</span><span class="sxs-lookup"><span data-stu-id="c8556-103">JsGetPropertyIdType Function</span></span>

<span data-ttu-id="c8556-104">Ruft den Typ der Eigenschaft ab.</span><span class="sxs-lookup"><span data-stu-id="c8556-104">Gets the type of property.</span></span>  
  
## <span data-ttu-id="c8556-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c8556-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetPropertyIdType(  
   _In_ JsPropertyIdRef propertyId,  
   _Out_ JsPropertyIdType* propertyIdType  
);  
```  
  
#### <span data-ttu-id="c8556-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c8556-106">Parameters</span></span>  
 `propertyId`  
 <span data-ttu-id="c8556-107">Die Eigenschafts-ID, deren Typ abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="c8556-107">The property ID to get the type of.</span></span>  
  
 `propertyIdType`  
 <span data-ttu-id="c8556-108">Die der `JsPropertyIdType` angegebenen Eigenschafts-ID.</span><span class="sxs-lookup"><span data-stu-id="c8556-108">The `JsPropertyIdType` of the given property ID.</span></span>  
  
## <span data-ttu-id="c8556-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c8556-109">Return Value</span></span>  
 <span data-ttu-id="c8556-110">Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="c8556-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="c8556-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="c8556-111">Remarks</span></span>  
 <span data-ttu-id="c8556-112">Erfordert einen aktiven Skriptkontext.</span><span class="sxs-lookup"><span data-stu-id="c8556-112">Requires an active script context.</span></span>  
  
 <span data-ttu-id="c8556-113">Diese API wird nur im Microsoft Edge-Modus unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c8556-113">This API is supported only in Microsoft Edge mode.</span></span>  
  
## <span data-ttu-id="c8556-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c8556-114">Requirements</span></span>  
 <span data-ttu-id="c8556-115">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="c8556-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="c8556-116">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="c8556-116">See Also</span></span>  
 [<span data-ttu-id="c8556-117">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="c8556-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
