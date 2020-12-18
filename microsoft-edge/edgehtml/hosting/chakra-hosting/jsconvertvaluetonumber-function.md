---
description: Wandelt den Wert mit der standardmäßigen JavaScript-Semantik in Number um.
title: JsConvertValueToNumber-Funktion | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsConvertValueToNumber
helpviewer_keywords:
- JsConvertValueToNumber function
ms.assetid: c47b8653-0591-4863-b8b5-33187b315816
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 8d00950ef3835c6d75f8f55ffe5002b32c6ee160
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233772"
---
# <span data-ttu-id="da48d-103">JsConvertValueToNumber Funktion</span><span class="sxs-lookup"><span data-stu-id="da48d-103">JsConvertValueToNumber Function</span></span>

<span data-ttu-id="da48d-104">Wandelt den Wert mit der standardmäßigen JavaScript-Semantik in Number um.</span><span class="sxs-lookup"><span data-stu-id="da48d-104">Converts the value to number using standard JavaScript semantics.</span></span>  
  
## <span data-ttu-id="da48d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="da48d-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsConvertValueToNumber(  
   _In_ JsValueRef value,  
   _Out_ JsValueRef *numberValue  
);  
```  
  
#### <span data-ttu-id="da48d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="da48d-106">Parameters</span></span>  
 `value`  
 <span data-ttu-id="da48d-107">Der Wert, der konvertiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="da48d-107">The value to be converted.</span></span>  
  
 `numberValue`  
 <span data-ttu-id="da48d-108">Der konvertierte Wert.</span><span class="sxs-lookup"><span data-stu-id="da48d-108">The converted value.</span></span>  
  
## <span data-ttu-id="da48d-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="da48d-109">Return Value</span></span>  
 <span data-ttu-id="da48d-110">Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="da48d-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="da48d-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="da48d-111">Remarks</span></span>  
 <span data-ttu-id="da48d-112">Erfordert einen aktiven Skriptkontext.</span><span class="sxs-lookup"><span data-stu-id="da48d-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="da48d-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="da48d-113">Requirements</span></span>  
 <span data-ttu-id="da48d-114">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="da48d-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="da48d-115">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="da48d-115">See Also</span></span>  
 [<span data-ttu-id="da48d-116">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="da48d-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
