---
description: Erstellt einen Zahlenwert aus einem Double-Wert.
title: JsDoubleToNumber-Funktion | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsDoubleToNumber
helpviewer_keywords:
- JsDoubleToNumber function
ms.assetid: 43eb2ee1-2789-4302-954e-c4087e1ee786
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: d3385633f41c2e20c43ca865eaeec763b6ff7f43
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233952"
---
# <span data-ttu-id="cc957-103">JsDoubleToNumber Funktion</span><span class="sxs-lookup"><span data-stu-id="cc957-103">JsDoubleToNumber Function</span></span>

<span data-ttu-id="cc957-104">Erstellt einen Zahlenwert aus einem `double` Wert.</span><span class="sxs-lookup"><span data-stu-id="cc957-104">Creates a number value from a `double` value.</span></span>  
  
## <span data-ttu-id="cc957-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="cc957-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsDoubleToNumber(  
   _In_ double doubleValue,  
   _Out_ JsValueRef *value  
);  
```  
  
#### <span data-ttu-id="cc957-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="cc957-106">Parameters</span></span>  
 `doubleValue`  
 <span data-ttu-id="cc957-107">Die `double` Konvertierung in einen Zahlenwert.</span><span class="sxs-lookup"><span data-stu-id="cc957-107">The `double` to convert to a number value.</span></span>  
  
 `value`  
 <span data-ttu-id="cc957-108">Der neue Zahlenwert.</span><span class="sxs-lookup"><span data-stu-id="cc957-108">The new number value.</span></span>  
  
## <span data-ttu-id="cc957-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cc957-109">Return Value</span></span>  
 <span data-ttu-id="cc957-110">Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="cc957-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="cc957-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="cc957-111">Remarks</span></span>  
 <span data-ttu-id="cc957-112">Erfordert einen aktiven Skriptkontext.</span><span class="sxs-lookup"><span data-stu-id="cc957-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="cc957-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cc957-113">Requirements</span></span>  
 <span data-ttu-id="cc957-114">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="cc957-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="cc957-115">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="cc957-115">See Also</span></span>  
 [<span data-ttu-id="cc957-116">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="cc957-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
