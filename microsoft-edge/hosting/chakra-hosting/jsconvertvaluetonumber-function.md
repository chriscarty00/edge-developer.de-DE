---
description: Wandelt den Wert mit der standardmäßigen JavaScript-Semantik in Number um.
title: JsConvertValueToNumber-Funktion | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsConvertValueToNumber
helpviewer_keywords:
- JsConvertValueToNumber function
ms.assetid: c47b8653-0591-4863-b8b5-33187b315816
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 3b3f450a58aaf1c434e1d34cd51577e3a5a9ee31
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10567317"
---
# <span data-ttu-id="fb9b8-103">JsConvertValueToNumber-Funktion</span><span class="sxs-lookup"><span data-stu-id="fb9b8-103">JsConvertValueToNumber Function</span></span>
<span data-ttu-id="fb9b8-104">Wandelt den Wert mit der standardmäßigen JavaScript-Semantik in Number um.</span><span class="sxs-lookup"><span data-stu-id="fb9b8-104">Converts the value to number using standard JavaScript semantics.</span></span>  
  
## <span data-ttu-id="fb9b8-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="fb9b8-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsConvertValueToNumber(  
   _In_ JsValueRef value,  
   _Out_ JsValueRef *numberValue  
);  
```  
  
#### <span data-ttu-id="fb9b8-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="fb9b8-106">Parameters</span></span>  
 `value`  
 <span data-ttu-id="fb9b8-107">Der Wert, der konvertiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="fb9b8-107">The value to be converted.</span></span>  
  
 `numberValue`  
 <span data-ttu-id="fb9b8-108">Der konvertierte Wert.</span><span class="sxs-lookup"><span data-stu-id="fb9b8-108">The converted value.</span></span>  
  
## <span data-ttu-id="fb9b8-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fb9b8-109">Return Value</span></span>  
 <span data-ttu-id="fb9b8-110">Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="fb9b8-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="fb9b8-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="fb9b8-111">Remarks</span></span>  
 <span data-ttu-id="fb9b8-112">Erfordert einen aktiven Skriptkontext.</span><span class="sxs-lookup"><span data-stu-id="fb9b8-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="fb9b8-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fb9b8-113">Requirements</span></span>  
 <span data-ttu-id="fb9b8-114">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="fb9b8-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="fb9b8-115">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="fb9b8-115">See Also</span></span>  
 [<span data-ttu-id="fb9b8-116">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="fb9b8-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)