---
description: Ruft die Eigenschaft eines Objekts ab.
title: JsGetProperty-Funktion | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsGetProperty
helpviewer_keywords:
- JsGetProperty function
ms.assetid: 606bc14f-e849-4f88-a148-6660e923c07b
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: ea0e5a3bad9363800d2b4a3a18ab932ecc384486
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10568381"
---
# <span data-ttu-id="a6a16-103">JsGetProperty-Funktion</span><span class="sxs-lookup"><span data-stu-id="a6a16-103">JsGetProperty Function</span></span>
<span data-ttu-id="a6a16-104">Ruft die Eigenschaft eines Objekts ab.</span><span class="sxs-lookup"><span data-stu-id="a6a16-104">Gets an object's property.</span></span>  
  
## <span data-ttu-id="a6a16-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a6a16-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetProperty(  
   _In_ JsValueRef object,  
   _In_ JsPropertyIdRef propertyId,  
   _Out_ JsValueRef *value  
);  
```  
  
#### <span data-ttu-id="a6a16-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a6a16-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="a6a16-107">Das Objekt, das die Eigenschaft enthält.</span><span class="sxs-lookup"><span data-stu-id="a6a16-107">The object that contains the property.</span></span>  
  
 `propertyId`  
 <span data-ttu-id="a6a16-108">Die ID der Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="a6a16-108">The ID of the property.</span></span>  
  
 `value`  
 <span data-ttu-id="a6a16-109">Der Wert der Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="a6a16-109">The value of the property.</span></span>  
  
## <span data-ttu-id="a6a16-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a6a16-110">Return Value</span></span>  
 <span data-ttu-id="a6a16-111">Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="a6a16-111">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="a6a16-112">Hinweise</span><span class="sxs-lookup"><span data-stu-id="a6a16-112">Remarks</span></span>  
 <span data-ttu-id="a6a16-113">Erfordert einen aktiven Skriptkontext.</span><span class="sxs-lookup"><span data-stu-id="a6a16-113">Requires an active script context.</span></span>  
  
## <span data-ttu-id="a6a16-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a6a16-114">Requirements</span></span>  
 <span data-ttu-id="a6a16-115">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="a6a16-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="a6a16-116">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="a6a16-116">See Also</span></span>  
 [<span data-ttu-id="a6a16-117">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="a6a16-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)