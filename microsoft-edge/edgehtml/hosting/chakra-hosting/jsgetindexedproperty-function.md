---
description: Rufen Sie den Wert am angegebenen Index eines Objekts ab.
title: JsGetIndexedProperty-Funktion | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsGetIndexedProperty
helpviewer_keywords:
- JsGetIndexedProperty function
ms.assetid: f61ea388-0ae6-4a19-b3b5-75ed49a3f32d
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: bd0246464d00884ca71fd8d3564ce775415f6267
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233580"
---
# <span data-ttu-id="9f4c6-103">JsGetIndexedProperty Funktion</span><span class="sxs-lookup"><span data-stu-id="9f4c6-103">JsGetIndexedProperty Function</span></span>

<span data-ttu-id="9f4c6-104">Rufen Sie den Wert am angegebenen Index eines Objekts ab.</span><span class="sxs-lookup"><span data-stu-id="9f4c6-104">Retrieve the value at the specified index of an object.</span></span>  
  
## <span data-ttu-id="9f4c6-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="9f4c6-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetIndexedProperty(  
   _In_ JsValueRef object,  
   _In_ JsValueRef index,  
   _Out_ JsValueRef *result  
);  
```  
  
#### <span data-ttu-id="9f4c6-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="9f4c6-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="9f4c6-107">Das Objekt, das ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="9f4c6-107">The object to operate on.</span></span>  
  
 `index`  
 <span data-ttu-id="9f4c6-108">Der abzurufende Index.</span><span class="sxs-lookup"><span data-stu-id="9f4c6-108">The index to retrieve.</span></span>  
  
 `result`  
 <span data-ttu-id="9f4c6-109">Der abgerufene Wert.</span><span class="sxs-lookup"><span data-stu-id="9f4c6-109">The retrieved value.</span></span>  
  
## <span data-ttu-id="9f4c6-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9f4c6-110">Return Value</span></span>  
 <span data-ttu-id="9f4c6-111">Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="9f4c6-111">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="9f4c6-112">Hinweise</span><span class="sxs-lookup"><span data-stu-id="9f4c6-112">Remarks</span></span>  
 <span data-ttu-id="9f4c6-113">Erfordert einen aktiven Skriptkontext.</span><span class="sxs-lookup"><span data-stu-id="9f4c6-113">Requires an active script context.</span></span>  
  
## <span data-ttu-id="9f4c6-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9f4c6-114">Requirements</span></span>  
 <span data-ttu-id="9f4c6-115">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="9f4c6-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="9f4c6-116">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="9f4c6-116">See Also</span></span>  
 [<span data-ttu-id="9f4c6-117">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="9f4c6-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
