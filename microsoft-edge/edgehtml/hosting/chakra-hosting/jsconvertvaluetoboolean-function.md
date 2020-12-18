---
description: Wandelt den Wert mithilfe der JavaScript-Standardsemantik in Boolean um.
title: JsConvertValueToBoolean-Funktion | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsConvertValueToBoolean
helpviewer_keywords:
- JsConvertValueToBoolean function
ms.assetid: 7298ec72-a388-4334-b81b-1691ab4cecf0
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: d2e109690fc8a7a98a1ecb84d6f5abf6a646162b
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233769"
---
# <span data-ttu-id="0fe8e-103">JsConvertValueToBoolean Funktion</span><span class="sxs-lookup"><span data-stu-id="0fe8e-103">JsConvertValueToBoolean Function</span></span>

<span data-ttu-id="0fe8e-104">Wandelt den Wert mithilfe der JavaScript-Standardsemantik in Boolean um.</span><span class="sxs-lookup"><span data-stu-id="0fe8e-104">Converts the value to Boolean using standard JavaScript semantics.</span></span>  
  
## <span data-ttu-id="0fe8e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="0fe8e-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsConvertValueToBoolean(  
   _In_ JsValueRef value,  
   _Out_ JsValueRef *booleanValue  
);  
```  
  
#### <span data-ttu-id="0fe8e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="0fe8e-106">Parameters</span></span>  
 `value`  
 <span data-ttu-id="0fe8e-107">Der Wert, der konvertiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="0fe8e-107">The value to be converted.</span></span>  
  
 `booleanValue`  
 <span data-ttu-id="0fe8e-108">Der konvertierte Wert.</span><span class="sxs-lookup"><span data-stu-id="0fe8e-108">The converted value.</span></span>  
  
## <span data-ttu-id="0fe8e-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0fe8e-109">Return Value</span></span>  
 <span data-ttu-id="0fe8e-110">Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="0fe8e-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="0fe8e-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="0fe8e-111">Remarks</span></span>  
 <span data-ttu-id="0fe8e-112">Erfordert einen aktiven Skriptkontext.</span><span class="sxs-lookup"><span data-stu-id="0fe8e-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="0fe8e-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0fe8e-113">Requirements</span></span>  
 <span data-ttu-id="0fe8e-114">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="0fe8e-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="0fe8e-115">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="0fe8e-115">See Also</span></span>  
 [<span data-ttu-id="0fe8e-116">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="0fe8e-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
