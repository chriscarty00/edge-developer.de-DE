---
description: Testet, ob ein Objekt am angegebenen Index über einen Wert verfügt.
title: JsHasIndexedProperty-Funktion | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsHasIndexedProperty
helpviewer_keywords:
- JsHasIndexedProperty function
ms.assetid: 30436a3d-fda0-407e-aba2-142be2310372
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 9eb1794c465b4b116978a2150285e2fed3ae1d9b
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233963"
---
# <span data-ttu-id="7a108-103">JsHasIndexedProperty Funktion</span><span class="sxs-lookup"><span data-stu-id="7a108-103">JsHasIndexedProperty Function</span></span>

<span data-ttu-id="7a108-104">Testet, ob ein Objekt am angegebenen Index über einen Wert verfügt.</span><span class="sxs-lookup"><span data-stu-id="7a108-104">Tests whether an object has a value at the specified index.</span></span>  
  
## <span data-ttu-id="7a108-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="7a108-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsHasIndexedProperty(  
   _In_ JsValueRef object,  
   _In_ JsValueRef index,  
   _Out_ bool *result  
);  
```  
  
#### <span data-ttu-id="7a108-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="7a108-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="7a108-107">Das Objekt, das ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="7a108-107">The object to operate on.</span></span>  
  
 `index`  
 <span data-ttu-id="7a108-108">Der zu testende Index.</span><span class="sxs-lookup"><span data-stu-id="7a108-108">The index to test.</span></span>  
  
 `result`  
 <span data-ttu-id="7a108-109">Gibt an, ob das Objekt am angegebenen Index über einen Wert verfügt.</span><span class="sxs-lookup"><span data-stu-id="7a108-109">Whether the object has an value at the specified index.</span></span>  
  
## <span data-ttu-id="7a108-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7a108-110">Return Value</span></span>  
 <span data-ttu-id="7a108-111">Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="7a108-111">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="7a108-112">Hinweise</span><span class="sxs-lookup"><span data-stu-id="7a108-112">Remarks</span></span>  
 <span data-ttu-id="7a108-113">Erfordert einen aktiven Skriptkontext.</span><span class="sxs-lookup"><span data-stu-id="7a108-113">Requires an active script context.</span></span>  
  
## <span data-ttu-id="7a108-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7a108-114">Requirements</span></span>  
 <span data-ttu-id="7a108-115">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="7a108-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="7a108-116">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="7a108-116">See Also</span></span>  
 [<span data-ttu-id="7a108-117">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="7a108-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
