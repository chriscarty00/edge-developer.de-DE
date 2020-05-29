---
description: Ruft die Daten eines externen Objekts ab.
title: JsGetExternalData-Funktion | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsGetExternalData
helpviewer_keywords:
- JsGetExternalData function
ms.assetid: 1919e1da-3ea7-4269-a5fb-a3be06bd029b
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 469d28d47f89b06897e4b72d081baad34eb92a6c
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10567259"
---
# <span data-ttu-id="e6d60-103">JsGetExternalData-Funktion</span><span class="sxs-lookup"><span data-stu-id="e6d60-103">JsGetExternalData Function</span></span>
<span data-ttu-id="e6d60-104">Ruft die Daten eines externen Objekts ab.</span><span class="sxs-lookup"><span data-stu-id="e6d60-104">Retrieves the data from an external object.</span></span>  
  
## <span data-ttu-id="e6d60-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e6d60-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetExternalData(  
   _In_ JsValueRef object,  
   _Out_ void **externalData  
);  
```  
  
#### <span data-ttu-id="e6d60-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="e6d60-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="e6d60-107">Das externe Objekt.</span><span class="sxs-lookup"><span data-stu-id="e6d60-107">The external object.</span></span>  
  
 `externalData`  
 <span data-ttu-id="e6d60-108">Die im Objekt gespeicherten externen Daten.</span><span class="sxs-lookup"><span data-stu-id="e6d60-108">The external data stored in the object.</span></span> <span data-ttu-id="e6d60-109">Kann NULL sein, wenn keine externen Daten im Objekt gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="e6d60-109">Can be null if no external data is stored in the object.</span></span>  
  
## <span data-ttu-id="e6d60-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e6d60-110">Return Value</span></span>  
 <span data-ttu-id="e6d60-111">Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="e6d60-111">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="e6d60-112">Hinweise</span><span class="sxs-lookup"><span data-stu-id="e6d60-112">Remarks</span></span>  
 <span data-ttu-id="e6d60-113">Erfordert einen aktiven Skriptkontext.</span><span class="sxs-lookup"><span data-stu-id="e6d60-113">Requires an active script context.</span></span>  
  
## <span data-ttu-id="e6d60-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e6d60-114">Requirements</span></span>  
 <span data-ttu-id="e6d60-115">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="e6d60-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="e6d60-116">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="e6d60-116">See Also</span></span>  
 [<span data-ttu-id="e6d60-117">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="e6d60-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)