---
description: Legt den Wert am angegebenen Index eines Objekts fest.
title: JsSetIndexedProperty-Funktion | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsSetIndexedProperty
helpviewer_keywords:
- JsSetIndexedProperty function
ms.assetid: ccbc5bf4-d99b-485c-ab25-d2bd1ed2142e
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 893849c42d9cbf0de160846d3397fcd5d7c77b7b
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10568308"
---
# <span data-ttu-id="e853e-103">JsSetIndexedProperty-Funktion</span><span class="sxs-lookup"><span data-stu-id="e853e-103">JsSetIndexedProperty Function</span></span>
<span data-ttu-id="e853e-104">Legt den Wert am angegebenen Index eines Objekts fest.</span><span class="sxs-lookup"><span data-stu-id="e853e-104">Set the value at the specified index of an object.</span></span>  
  
## <span data-ttu-id="e853e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e853e-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsSetIndexedProperty(  
   _In_ JsValueRef object,  
   _In_ JsValueRef index,  
   _In_ JsValueRef value  
);  
```  
  
#### <span data-ttu-id="e853e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="e853e-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="e853e-107">Das Objekt, das ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="e853e-107">The object to operate on.</span></span>  
  
 `index`  
 <span data-ttu-id="e853e-108">Der Index, der gesetzt werden soll.</span><span class="sxs-lookup"><span data-stu-id="e853e-108">The index to set.</span></span>  
  
 `value`  
 <span data-ttu-id="e853e-109">Der Wert, der gesetzt werden soll.</span><span class="sxs-lookup"><span data-stu-id="e853e-109">The value to set.</span></span>  
  
## <span data-ttu-id="e853e-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e853e-110">Return Value</span></span>  
 <span data-ttu-id="e853e-111">Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="e853e-111">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="e853e-112">Hinweise</span><span class="sxs-lookup"><span data-stu-id="e853e-112">Remarks</span></span>  
 <span data-ttu-id="e853e-113">Erfordert einen aktiven Skriptkontext.</span><span class="sxs-lookup"><span data-stu-id="e853e-113">Requires an active script context.</span></span>  
  
## <span data-ttu-id="e853e-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e853e-114">Requirements</span></span>  
 <span data-ttu-id="e853e-115">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="e853e-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="e853e-116">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="e853e-116">See Also</span></span>  
 [<span data-ttu-id="e853e-117">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="e853e-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)