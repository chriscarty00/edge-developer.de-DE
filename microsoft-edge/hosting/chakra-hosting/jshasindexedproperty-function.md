---
description: Testet, ob ein Objekt am angegebenen Index über einen Wert verfügt.
title: JsHasIndexedProperty-Funktion | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsHasIndexedProperty
helpviewer_keywords:
- JsHasIndexedProperty function
ms.assetid: 30436a3d-fda0-407e-aba2-142be2310372
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 85d9fa12c44bd1d961ec2a7ba494484873635586
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10568361"
---
# <span data-ttu-id="3748a-103">JsHasIndexedProperty-Funktion</span><span class="sxs-lookup"><span data-stu-id="3748a-103">JsHasIndexedProperty Function</span></span>
<span data-ttu-id="3748a-104">Testet, ob ein Objekt am angegebenen Index über einen Wert verfügt.</span><span class="sxs-lookup"><span data-stu-id="3748a-104">Tests whether an object has a value at the specified index.</span></span>  
  
## <span data-ttu-id="3748a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="3748a-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsHasIndexedProperty(  
   _In_ JsValueRef object,  
   _In_ JsValueRef index,  
   _Out_ bool *result  
);  
```  
  
#### <span data-ttu-id="3748a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="3748a-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="3748a-107">Das Objekt, das ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="3748a-107">The object to operate on.</span></span>  
  
 `index`  
 <span data-ttu-id="3748a-108">Der zu testende Index.</span><span class="sxs-lookup"><span data-stu-id="3748a-108">The index to test.</span></span>  
  
 `result`  
 <span data-ttu-id="3748a-109">Gibt an, ob das Objekt am angegebenen Index über einen Wert verfügt.</span><span class="sxs-lookup"><span data-stu-id="3748a-109">Whether the object has an value at the specified index.</span></span>  
  
## <span data-ttu-id="3748a-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3748a-110">Return Value</span></span>  
 <span data-ttu-id="3748a-111">Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="3748a-111">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="3748a-112">Hinweise</span><span class="sxs-lookup"><span data-stu-id="3748a-112">Remarks</span></span>  
 <span data-ttu-id="3748a-113">Erfordert einen aktiven Skriptkontext.</span><span class="sxs-lookup"><span data-stu-id="3748a-113">Requires an active script context.</span></span>  
  
## <span data-ttu-id="3748a-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3748a-114">Requirements</span></span>  
 <span data-ttu-id="3748a-115">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="3748a-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="3748a-116">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="3748a-116">See Also</span></span>  
 [<span data-ttu-id="3748a-117">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="3748a-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)