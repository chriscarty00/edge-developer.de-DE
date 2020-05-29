---
description: Erstellt einen Zahlenwert aus einem Double-Wert.
title: JsDoubleToNumber-Funktion | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsDoubleToNumber
helpviewer_keywords:
- JsDoubleToNumber function
ms.assetid: 43eb2ee1-2789-4302-954e-c4087e1ee786
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: c33adbe217f27f77e348fc56e87c4587c6a6ec4c
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10568405"
---
# <span data-ttu-id="4a4a5-103">JsDoubleToNumber-Funktion</span><span class="sxs-lookup"><span data-stu-id="4a4a5-103">JsDoubleToNumber Function</span></span>
<span data-ttu-id="4a4a5-104">Erstellt einen Zahlenwert aus einem `double` Wert.</span><span class="sxs-lookup"><span data-stu-id="4a4a5-104">Creates a number value from a `double` value.</span></span>  
  
## <span data-ttu-id="4a4a5-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="4a4a5-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsDoubleToNumber(  
   _In_ double doubleValue,  
   _Out_ JsValueRef *value  
);  
```  
  
#### <span data-ttu-id="4a4a5-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="4a4a5-106">Parameters</span></span>  
 `doubleValue`  
 <span data-ttu-id="4a4a5-107">Die `double` Konvertierung in einen Zahlenwert.</span><span class="sxs-lookup"><span data-stu-id="4a4a5-107">The `double` to convert to a number value.</span></span>  
  
 `value`  
 <span data-ttu-id="4a4a5-108">Der neue Zahlenwert.</span><span class="sxs-lookup"><span data-stu-id="4a4a5-108">The new number value.</span></span>  
  
## <span data-ttu-id="4a4a5-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4a4a5-109">Return Value</span></span>  
 <span data-ttu-id="4a4a5-110">Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="4a4a5-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="4a4a5-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="4a4a5-111">Remarks</span></span>  
 <span data-ttu-id="4a4a5-112">Erfordert einen aktiven Skriptkontext.</span><span class="sxs-lookup"><span data-stu-id="4a4a5-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="4a4a5-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4a4a5-113">Requirements</span></span>  
 <span data-ttu-id="4a4a5-114">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="4a4a5-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="4a4a5-115">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="4a4a5-115">See Also</span></span>  
 [<span data-ttu-id="4a4a5-116">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="4a4a5-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)