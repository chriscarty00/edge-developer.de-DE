---
description: Wandelt den Wert mithilfe der JavaScript-Standardsemantik in Boolean um.
title: JsConvertValueToBoolean-Funktion | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsConvertValueToBoolean
helpviewer_keywords:
- JsConvertValueToBoolean function
ms.assetid: 7298ec72-a388-4334-b81b-1691ab4cecf0
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 861871a030d5a47621ccaf40b6cd332f42a06583
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10567319"
---
# <span data-ttu-id="136d2-103">JsConvertValueToBoolean-Funktion</span><span class="sxs-lookup"><span data-stu-id="136d2-103">JsConvertValueToBoolean Function</span></span>
<span data-ttu-id="136d2-104">Wandelt den Wert mithilfe der JavaScript-Standardsemantik in Boolean um.</span><span class="sxs-lookup"><span data-stu-id="136d2-104">Converts the value to Boolean using standard JavaScript semantics.</span></span>  
  
## <span data-ttu-id="136d2-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="136d2-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsConvertValueToBoolean(  
   _In_ JsValueRef value,  
   _Out_ JsValueRef *booleanValue  
);  
```  
  
#### <span data-ttu-id="136d2-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="136d2-106">Parameters</span></span>  
 `value`  
 <span data-ttu-id="136d2-107">Der Wert, der konvertiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="136d2-107">The value to be converted.</span></span>  
  
 `booleanValue`  
 <span data-ttu-id="136d2-108">Der konvertierte Wert.</span><span class="sxs-lookup"><span data-stu-id="136d2-108">The converted value.</span></span>  
  
## <span data-ttu-id="136d2-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="136d2-109">Return Value</span></span>  
 <span data-ttu-id="136d2-110">Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="136d2-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="136d2-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="136d2-111">Remarks</span></span>  
 <span data-ttu-id="136d2-112">Erfordert einen aktiven Skriptkontext.</span><span class="sxs-lookup"><span data-stu-id="136d2-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="136d2-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="136d2-113">Requirements</span></span>  
 <span data-ttu-id="136d2-114">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="136d2-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="136d2-115">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="136d2-115">See Also</span></span>  
 [<span data-ttu-id="136d2-116">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="136d2-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)