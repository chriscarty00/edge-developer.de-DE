---
description: Ruft den `double` Wert eines Zahlenwerts ab.
title: JsNumberToDouble-Funktion | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsNumberToDouble
helpviewer_keywords:
- JsNumberToDouble function
ms.assetid: 5f52e8b6-2b70-49a3-879a-bd83ebf2ac33
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: fc99e02aa0376bb100b4e1302c29532a57bd539f
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10567216"
---
# <span data-ttu-id="0724e-103">JsNumberToDouble-Funktion</span><span class="sxs-lookup"><span data-stu-id="0724e-103">JsNumberToDouble Function</span></span>
<span data-ttu-id="0724e-104">Ruft den `double` Wert eines Zahlenwerts ab.</span><span class="sxs-lookup"><span data-stu-id="0724e-104">Retrieves the `double` value of a number value.</span></span>  
  
## <span data-ttu-id="0724e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="0724e-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsNumberToDouble(  
   _In_ JsValueRef value,  
   _Out_ double *doubleValue  
);  
```  
  
#### <span data-ttu-id="0724e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="0724e-106">Parameters</span></span>  
 `value`  
 <span data-ttu-id="0724e-107">Der Zahlenwert, der in einen Wert konvertiert werden soll `double` .</span><span class="sxs-lookup"><span data-stu-id="0724e-107">The number value to convert to a `double` value.</span></span>  
  
 `doubleValue`  
 <span data-ttu-id="0724e-108">Der `double` Wert.</span><span class="sxs-lookup"><span data-stu-id="0724e-108">The `double` value.</span></span>  
  
## <span data-ttu-id="0724e-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0724e-109">Return Value</span></span>  
 <span data-ttu-id="0724e-110">Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="0724e-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="0724e-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="0724e-111">Remarks</span></span>  
 <span data-ttu-id="0724e-112">Diese Funktion Ruft den Wert eines Zahlenwerts ab.</span><span class="sxs-lookup"><span data-stu-id="0724e-112">This function retrieves the value of a number value.</span></span> <span data-ttu-id="0724e-113">`JsErrorInvalidArgument`Wenn der Typ des Werts nicht number ist, tritt ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="0724e-113">It will fail with `JsErrorInvalidArgument` if the type of the value is not number.</span></span>  
  
 <span data-ttu-id="0724e-114">Erfordert einen aktiven Skriptkontext.</span><span class="sxs-lookup"><span data-stu-id="0724e-114">Requires an active script context.</span></span>  
  
## <span data-ttu-id="0724e-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0724e-115">Requirements</span></span>  
 <span data-ttu-id="0724e-116">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="0724e-116">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="0724e-117">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="0724e-117">See Also</span></span>  
 [<span data-ttu-id="0724e-118">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="0724e-118">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)