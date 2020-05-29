---
description: Ruft den Wert `undefined` im aktuellen Skriptkontext ab.
title: JsGetUndefinedValue-Funktion | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsGetUndefinedValue
helpviewer_keywords:
- JsGetUndefinedValue function
ms.assetid: e118eaf6-452c-42f2-86b8-e63c7d987cba
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 5edd536a29f5003591de476cb5d21ddb64f48c0b
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10568370"
---
# <span data-ttu-id="cf06a-103">JsGetUndefinedValue-Funktion</span><span class="sxs-lookup"><span data-stu-id="cf06a-103">JsGetUndefinedValue Function</span></span>
<span data-ttu-id="cf06a-104">Ruft den Wert `undefined` im aktuellen Skriptkontext ab.</span><span class="sxs-lookup"><span data-stu-id="cf06a-104">Gets the value of `undefined` in the current script context.</span></span>  
  
## <span data-ttu-id="cf06a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="cf06a-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetUndefinedValue(  
   _Out_ JsValueRef *undefinedValue  
);  
```  
  
#### <span data-ttu-id="cf06a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="cf06a-106">Parameters</span></span>  
 `undefinedValue`  
 <span data-ttu-id="cf06a-107">Der `undefined` Wert.</span><span class="sxs-lookup"><span data-stu-id="cf06a-107">The `undefined` value.</span></span>  
  
## <span data-ttu-id="cf06a-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cf06a-108">Return Value</span></span>  
 <span data-ttu-id="cf06a-109">Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="cf06a-109">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="cf06a-110">Hinweise</span><span class="sxs-lookup"><span data-stu-id="cf06a-110">Remarks</span></span>  
 <span data-ttu-id="cf06a-111">Erfordert einen aktiven Skriptkontext.</span><span class="sxs-lookup"><span data-stu-id="cf06a-111">Requires an active script context.</span></span>  
  
## <span data-ttu-id="cf06a-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cf06a-112">Requirements</span></span>  
 <span data-ttu-id="cf06a-113">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="cf06a-113">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="cf06a-114">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="cf06a-114">See Also</span></span>  
 [<span data-ttu-id="cf06a-115">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="cf06a-115">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)