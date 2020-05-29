---
description: Erstellt einen booleschen Wert aus einem `bool` Wert.
title: JsBoolToBoolean-Funktion | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsBoolToBoolean
helpviewer_keywords:
- JsBoolToBoolean function
ms.assetid: 24322ea3-0638-40a3-9b4c-fc912ebed3ff
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: f795bdd02a2a21dc4a0c8948a76ef817d6e0fac6
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10567332"
---
# <span data-ttu-id="d9fec-103">JsBoolToBoolean-Funktion</span><span class="sxs-lookup"><span data-stu-id="d9fec-103">JsBoolToBoolean Function</span></span>
<span data-ttu-id="d9fec-104">Erstellt einen booleschen Wert aus einem `bool` Wert.</span><span class="sxs-lookup"><span data-stu-id="d9fec-104">Creates a Boolean value from a `bool` value.</span></span>  
  
## <span data-ttu-id="d9fec-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="d9fec-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode JsBoolToBoolean(  
   _In_ bool value,  
   _Out_ JsValueRef *booleanValue  
);  
```  
  
#### <span data-ttu-id="d9fec-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="d9fec-106">Parameters</span></span>  
 `value`  
 <span data-ttu-id="d9fec-107">Der Wert, der konvertiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="d9fec-107">The value to be converted.</span></span>  
  
 `booleanValue`  
 <span data-ttu-id="d9fec-108">Der konvertierte Wert.</span><span class="sxs-lookup"><span data-stu-id="d9fec-108">The converted value.</span></span>  
  
## <span data-ttu-id="d9fec-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d9fec-109">Return Value</span></span>  
 <span data-ttu-id="d9fec-110">Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="d9fec-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="d9fec-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="d9fec-111">Remarks</span></span>  
 <span data-ttu-id="d9fec-112">Erfordert einen aktiven Skriptkontext.</span><span class="sxs-lookup"><span data-stu-id="d9fec-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="d9fec-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d9fec-113">Requirements</span></span>  
 <span data-ttu-id="d9fec-114">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="d9fec-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="d9fec-115">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="d9fec-115">See Also</span></span>  
 [<span data-ttu-id="d9fec-116">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="d9fec-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)