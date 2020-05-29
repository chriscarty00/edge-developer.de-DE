---
description: Ruft den Wert `true` im aktuellen Skriptkontext ab.
title: JsGetTrueValue-Funktion | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsGetTrueValue
helpviewer_keywords:
- JsGetTrueValue function
ms.assetid: c2a56d48-344b-492b-90b8-f570710f8310
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 620ed775947db9d7156d61df1cfdf974a46baec2
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10567236"
---
# <span data-ttu-id="fb779-103">JsGetTrueValue-Funktion</span><span class="sxs-lookup"><span data-stu-id="fb779-103">JsGetTrueValue Function</span></span>
<span data-ttu-id="fb779-104">Ruft den Wert `true` im aktuellen Skriptkontext ab.</span><span class="sxs-lookup"><span data-stu-id="fb779-104">Gets the value of `true` in the current script context.</span></span>  
  
## <span data-ttu-id="fb779-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="fb779-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetTrueValue(  
   _Out_ JsValueRef *trueValue  
);  
```  
  
#### <span data-ttu-id="fb779-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="fb779-106">Parameters</span></span>  
 `trueValue`  
 <span data-ttu-id="fb779-107">Der `true` Wert.</span><span class="sxs-lookup"><span data-stu-id="fb779-107">The `true` value.</span></span>  
  
## <span data-ttu-id="fb779-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fb779-108">Return Value</span></span>  
 <span data-ttu-id="fb779-109">Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="fb779-109">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="fb779-110">Hinweise</span><span class="sxs-lookup"><span data-stu-id="fb779-110">Remarks</span></span>  
 <span data-ttu-id="fb779-111">Erfordert einen aktiven Skriptkontext.</span><span class="sxs-lookup"><span data-stu-id="fb779-111">Requires an active script context.</span></span>  
  
## <span data-ttu-id="fb779-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fb779-112">Requirements</span></span>  
 <span data-ttu-id="fb779-113">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="fb779-113">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="fb779-114">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="fb779-114">See Also</span></span>  
 [<span data-ttu-id="fb779-115">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="fb779-115">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)