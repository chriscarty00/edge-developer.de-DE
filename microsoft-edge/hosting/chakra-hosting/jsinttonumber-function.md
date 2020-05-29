---
description: Erstellt einen Zahlenwert aus einem `int` Wert.
title: JsIntToNumber-Funktion | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 1393c4ac-7189-4e9c-8e54-b0e041c22112
caps.latest.revision: 4
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: dd8f51638292346ec3058f9537d72b8fd21bebc6
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10567230"
---
# <span data-ttu-id="d6a29-103">JsIntToNumber-Funktion</span><span class="sxs-lookup"><span data-stu-id="d6a29-103">JsIntToNumber Function</span></span>
<span data-ttu-id="d6a29-104">Erstellt einen Zahlenwert aus einem `int` Wert.</span><span class="sxs-lookup"><span data-stu-id="d6a29-104">Creates a number value from an `int` value.</span></span>  
  
## <span data-ttu-id="d6a29-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="d6a29-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsIntToNumber(  
   _In_ int intValue,  
   _Out_ JsValueRef *value  
);  
```  
  
#### <span data-ttu-id="d6a29-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="d6a29-106">Parameters</span></span>  
 `intValue`  
 <span data-ttu-id="d6a29-107">Die `int` Konvertierung in einen Zahlenwert.</span><span class="sxs-lookup"><span data-stu-id="d6a29-107">The `int` to convert to a number value.</span></span>  
  
 `value`  
 <span data-ttu-id="d6a29-108">Der neue Zahlenwert.</span><span class="sxs-lookup"><span data-stu-id="d6a29-108">The new number value.</span></span>  
  
## <span data-ttu-id="d6a29-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d6a29-109">Return Value</span></span>  
 <span data-ttu-id="d6a29-110">Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="d6a29-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="d6a29-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="d6a29-111">Remarks</span></span>  
 <span data-ttu-id="d6a29-112">Erfordert einen aktiven Skriptkontext.</span><span class="sxs-lookup"><span data-stu-id="d6a29-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="d6a29-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d6a29-113">Requirements</span></span>  
 <span data-ttu-id="d6a29-114">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="d6a29-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="d6a29-115">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="d6a29-115">See Also</span></span>  
 [<span data-ttu-id="d6a29-116">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="d6a29-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)