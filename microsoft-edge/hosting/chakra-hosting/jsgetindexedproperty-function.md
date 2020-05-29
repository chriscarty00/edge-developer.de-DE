---
description: Rufen Sie den Wert am angegebenen Index eines Objekts ab.
title: JsGetIndexedProperty-Funktion | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsGetIndexedProperty
helpviewer_keywords:
- JsGetIndexedProperty function
ms.assetid: f61ea388-0ae6-4a19-b3b5-75ed49a3f32d
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 7bb048b841462e27604ab169c69e4c051209a67d
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10568386"
---
# <span data-ttu-id="b3ad3-103">JsGetIndexedProperty-Funktion</span><span class="sxs-lookup"><span data-stu-id="b3ad3-103">JsGetIndexedProperty Function</span></span>
<span data-ttu-id="b3ad3-104">Rufen Sie den Wert am angegebenen Index eines Objekts ab.</span><span class="sxs-lookup"><span data-stu-id="b3ad3-104">Retrieve the value at the specified index of an object.</span></span>  
  
## <span data-ttu-id="b3ad3-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b3ad3-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetIndexedProperty(  
   _In_ JsValueRef object,  
   _In_ JsValueRef index,  
   _Out_ JsValueRef *result  
);  
```  
  
#### <span data-ttu-id="b3ad3-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="b3ad3-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="b3ad3-107">Das Objekt, das ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="b3ad3-107">The object to operate on.</span></span>  
  
 `index`  
 <span data-ttu-id="b3ad3-108">Der abzurufende Index.</span><span class="sxs-lookup"><span data-stu-id="b3ad3-108">The index to retrieve.</span></span>  
  
 `result`  
 <span data-ttu-id="b3ad3-109">Der abgerufene Wert.</span><span class="sxs-lookup"><span data-stu-id="b3ad3-109">The retrieved value.</span></span>  
  
## <span data-ttu-id="b3ad3-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b3ad3-110">Return Value</span></span>  
 <span data-ttu-id="b3ad3-111">Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="b3ad3-111">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="b3ad3-112">Hinweise</span><span class="sxs-lookup"><span data-stu-id="b3ad3-112">Remarks</span></span>  
 <span data-ttu-id="b3ad3-113">Erfordert einen aktiven Skriptkontext.</span><span class="sxs-lookup"><span data-stu-id="b3ad3-113">Requires an active script context.</span></span>  
  
## <span data-ttu-id="b3ad3-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b3ad3-114">Requirements</span></span>  
 <span data-ttu-id="b3ad3-115">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="b3ad3-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="b3ad3-116">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="b3ad3-116">See Also</span></span>  
 [<span data-ttu-id="b3ad3-117">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="b3ad3-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)