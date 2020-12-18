---
description: Konvertiert den Wert mit der standardmäßigen JavaScript-Semantik in Object.
title: JsConvertValueToObject-Funktion | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsConvertValueToObject
helpviewer_keywords:
- JsConvertValueToObject function
ms.assetid: 6528b28a-1d2b-417f-bf78-bf05547c52e1
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 6f3676b512585b0750c994bcfcdf9d2e6e4e1cc3
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233755"
---
# <span data-ttu-id="01aba-103">JsConvertValueToObject Funktion</span><span class="sxs-lookup"><span data-stu-id="01aba-103">JsConvertValueToObject Function</span></span>

<span data-ttu-id="01aba-104">Konvertiert den Wert mit der standardmäßigen JavaScript-Semantik in Object.</span><span class="sxs-lookup"><span data-stu-id="01aba-104">Converts the value to object using standard JavaScript semantics.</span></span>  
  
## <span data-ttu-id="01aba-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="01aba-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsConvertValueToObject(  
   _In_ JsValueRef value,  
   _Out_ JsValueRef *object  
);  
```  
  
#### <span data-ttu-id="01aba-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="01aba-106">Parameters</span></span>  
 `value`  
 <span data-ttu-id="01aba-107">Der Wert, der konvertiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="01aba-107">The value to be converted.</span></span>  
  
 `object`  
 <span data-ttu-id="01aba-108">Der konvertierte Wert.</span><span class="sxs-lookup"><span data-stu-id="01aba-108">The converted value.</span></span>  
  
## <span data-ttu-id="01aba-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="01aba-109">Return Value</span></span>  
 <span data-ttu-id="01aba-110">Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="01aba-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="01aba-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="01aba-111">Remarks</span></span>  
 <span data-ttu-id="01aba-112">Erfordert einen aktiven Skriptkontext.</span><span class="sxs-lookup"><span data-stu-id="01aba-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="01aba-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="01aba-113">Requirements</span></span>  
 <span data-ttu-id="01aba-114">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="01aba-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="01aba-115">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="01aba-115">See Also</span></span>  
 [<span data-ttu-id="01aba-116">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="01aba-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
