---
description: Ruft den Wert `false` im aktuellen Skriptkontext ab.
title: JsGetFalseValue-Funktion | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsGetFalseValue
helpviewer_keywords:
- JsGetFalseValue function
ms.assetid: 621a584c-4ca8-4ba0-b19a-6cb50cf830b6
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 52e54ad7eb34877c3cb83b06f5aba70edf285bca
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10567256"
---
# <span data-ttu-id="aff9b-103">JsGetFalseValue-Funktion</span><span class="sxs-lookup"><span data-stu-id="aff9b-103">JsGetFalseValue Function</span></span>
<span data-ttu-id="aff9b-104">Ruft den Wert `false` im aktuellen Skriptkontext ab.</span><span class="sxs-lookup"><span data-stu-id="aff9b-104">Gets the value of `false` in the current script context.</span></span>  
  
## <span data-ttu-id="aff9b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="aff9b-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetFalseValue(  
   _Out_ JsValueRef *falseValue  
);  
```  
  
#### <span data-ttu-id="aff9b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="aff9b-106">Parameters</span></span>  
 `falseValue`  
 <span data-ttu-id="aff9b-107">Der `false` Wert.</span><span class="sxs-lookup"><span data-stu-id="aff9b-107">The `false` value.</span></span>  
  
## <span data-ttu-id="aff9b-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="aff9b-108">Return Value</span></span>  
 <span data-ttu-id="aff9b-109">Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="aff9b-109">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="aff9b-110">Hinweise</span><span class="sxs-lookup"><span data-stu-id="aff9b-110">Remarks</span></span>  
 <span data-ttu-id="aff9b-111">Erfordert einen aktiven Skriptkontext.</span><span class="sxs-lookup"><span data-stu-id="aff9b-111">Requires an active script context.</span></span>  
  
## <span data-ttu-id="aff9b-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="aff9b-112">Requirements</span></span>  
 <span data-ttu-id="aff9b-113">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="aff9b-113">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="aff9b-114">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="aff9b-114">See Also</span></span>  
 [<span data-ttu-id="aff9b-115">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="aff9b-115">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)