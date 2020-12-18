---
description: Ruft den `bool` Wert eines booleschen Werts ab.
title: JsBooleanToBool-Funktion | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsBooleanToBool
helpviewer_keywords:
- JsBooleanToBool function
ms.assetid: ab16ac71-fe47-475d-a7ee-46e4643dee60
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 36bf2dc32b94466d8cdea37886e86a42c4ec01d3
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233766"
---
# <span data-ttu-id="72c5b-103">JsBooleanToBool Funktion</span><span class="sxs-lookup"><span data-stu-id="72c5b-103">JsBooleanToBool Function</span></span>

<span data-ttu-id="72c5b-104">Ruft den `bool` Wert eines booleschen Werts ab.</span><span class="sxs-lookup"><span data-stu-id="72c5b-104">Retrieves the `bool` value of a Boolean value.</span></span>  
  
## <span data-ttu-id="72c5b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="72c5b-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsBooleanToBool(  
   _In_ JsValueRef value,  
   _Out_ bool *boolValue  
);  
```  
  
#### <span data-ttu-id="72c5b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="72c5b-106">Parameters</span></span>  
 `value`  
 <span data-ttu-id="72c5b-107">Der Wert, der konvertiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="72c5b-107">The value to be converted.</span></span>  
  
 `boolValue`  
 <span data-ttu-id="72c5b-108">Der konvertierte Wert.</span><span class="sxs-lookup"><span data-stu-id="72c5b-108">The converted value.</span></span>  
  
## <span data-ttu-id="72c5b-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="72c5b-109">Return Value</span></span>  
 <span data-ttu-id="72c5b-110">Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="72c5b-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="72c5b-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="72c5b-111">Remarks</span></span>  
 <span data-ttu-id="72c5b-112">Erfordert einen aktiven Skriptkontext.</span><span class="sxs-lookup"><span data-stu-id="72c5b-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="72c5b-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="72c5b-113">Requirements</span></span>  
 <span data-ttu-id="72c5b-114">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="72c5b-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="72c5b-115">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="72c5b-115">See Also</span></span>  
 [<span data-ttu-id="72c5b-116">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="72c5b-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
