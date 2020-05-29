---
description: Ruft den `bool` Wert eines booleschen Werts ab.
title: JsBooleanToBool-Funktion | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsBooleanToBool
helpviewer_keywords:
- JsBooleanToBool function
ms.assetid: ab16ac71-fe47-475d-a7ee-46e4643dee60
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 55b0ef1278cbc73652fc8427e004cab002d76e5b
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10567334"
---
# <span data-ttu-id="5d1e6-103">JsBooleanToBool-Funktion</span><span class="sxs-lookup"><span data-stu-id="5d1e6-103">JsBooleanToBool Function</span></span>
<span data-ttu-id="5d1e6-104">Ruft den `bool` Wert eines booleschen Werts ab.</span><span class="sxs-lookup"><span data-stu-id="5d1e6-104">Retrieves the `bool` value of a Boolean value.</span></span>  
  
## <span data-ttu-id="5d1e6-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="5d1e6-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsBooleanToBool(  
   _In_ JsValueRef value,  
   _Out_ bool *boolValue  
);  
```  
  
#### <span data-ttu-id="5d1e6-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="5d1e6-106">Parameters</span></span>  
 `value`  
 <span data-ttu-id="5d1e6-107">Der Wert, der konvertiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="5d1e6-107">The value to be converted.</span></span>  
  
 `boolValue`  
 <span data-ttu-id="5d1e6-108">Der konvertierte Wert.</span><span class="sxs-lookup"><span data-stu-id="5d1e6-108">The converted value.</span></span>  
  
## <span data-ttu-id="5d1e6-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5d1e6-109">Return Value</span></span>  
 <span data-ttu-id="5d1e6-110">Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="5d1e6-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="5d1e6-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="5d1e6-111">Remarks</span></span>  
 <span data-ttu-id="5d1e6-112">Erfordert einen aktiven Skriptkontext.</span><span class="sxs-lookup"><span data-stu-id="5d1e6-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="5d1e6-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5d1e6-113">Requirements</span></span>  
 <span data-ttu-id="5d1e6-114">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="5d1e6-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="5d1e6-115">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="5d1e6-115">See Also</span></span>  
 [<span data-ttu-id="5d1e6-116">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="5d1e6-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)