---
description: Ruft den Wert `null` im aktuellen Skriptkontext ab.
title: JsGetNullValue-Funktion | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsGetNullValue
helpviewer_keywords:
- JsGetNullValue function
ms.assetid: 132a1496-8dfe-4d3c-a8f8-389f5b0b50d2
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 84164aa9ce5d522b0933d928d85b26c652be066f
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10568389"
---
# <span data-ttu-id="0e3f5-103">JsGetNullValue-Funktion</span><span class="sxs-lookup"><span data-stu-id="0e3f5-103">JsGetNullValue Function</span></span>
<span data-ttu-id="0e3f5-104">Ruft den Wert `null` im aktuellen Skriptkontext ab.</span><span class="sxs-lookup"><span data-stu-id="0e3f5-104">Gets the value of `null` in the current script context.</span></span>  
  
## <span data-ttu-id="0e3f5-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="0e3f5-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetNullValue(  
   _Out_ JsValueRef *nullValue  
);  
```  
  
#### <span data-ttu-id="0e3f5-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="0e3f5-106">Parameters</span></span>  
 `nullValue`  
 <span data-ttu-id="0e3f5-107">Der `null` Wert.</span><span class="sxs-lookup"><span data-stu-id="0e3f5-107">The `null` value.</span></span>  
  
## <span data-ttu-id="0e3f5-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0e3f5-108">Return Value</span></span>  
 <span data-ttu-id="0e3f5-109">Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="0e3f5-109">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="0e3f5-110">Hinweise</span><span class="sxs-lookup"><span data-stu-id="0e3f5-110">Remarks</span></span>  
 <span data-ttu-id="0e3f5-111">Erfordert einen aktiven Skriptkontext.</span><span class="sxs-lookup"><span data-stu-id="0e3f5-111">Requires an active script context.</span></span>  
  
## <span data-ttu-id="0e3f5-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0e3f5-112">Requirements</span></span>  
 <span data-ttu-id="0e3f5-113">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="0e3f5-113">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="0e3f5-114">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="0e3f5-114">See Also</span></span>  
 [<span data-ttu-id="0e3f5-115">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="0e3f5-115">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)