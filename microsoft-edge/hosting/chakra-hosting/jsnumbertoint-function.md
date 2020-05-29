---
description: Ruft den `int` Wert eines Zahlenwerts ab.
title: JsNumberToInt-Funktion | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 8b9256d6-76ac-4c74-a97c-fbb16c13f5f5
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: cf4c8cb42c737cfb9efee5422fe6bb3c1389cbfd
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10568356"
---
# <span data-ttu-id="a29f3-103">JsNumberToInt-Funktion</span><span class="sxs-lookup"><span data-stu-id="a29f3-103">JsNumberToInt Function</span></span>
<span data-ttu-id="a29f3-104">Ruft den `int` Wert eines Zahlenwerts ab.</span><span class="sxs-lookup"><span data-stu-id="a29f3-104">Retrieves the `int` value of a number value.</span></span>  
  
## <span data-ttu-id="a29f3-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a29f3-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsNumberToInt(  
      _In_ JsValueRef value,  
      _Out_ int *intValue  
);  
```  
  
#### <span data-ttu-id="a29f3-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a29f3-106">Parameters</span></span>  
 `value`  
 <span data-ttu-id="a29f3-107">Der Zahlenwert, der in einen Wert konvertiert werden soll `int` .</span><span class="sxs-lookup"><span data-stu-id="a29f3-107">The number value to convert to an `int` value.</span></span>  
  
 `intValue`  
 <span data-ttu-id="a29f3-108">Der `int` Wert.</span><span class="sxs-lookup"><span data-stu-id="a29f3-108">The `int` value.</span></span>  
  
## <span data-ttu-id="a29f3-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a29f3-109">Return Value</span></span>  
  
## <span data-ttu-id="a29f3-110">Hinweise</span><span class="sxs-lookup"><span data-stu-id="a29f3-110">Remarks</span></span>  
 <span data-ttu-id="a29f3-111">Diese Funktion Ruft den Wert eines Zahlenwerts ab und wandelt ihn in einen `int` Wert um.</span><span class="sxs-lookup"><span data-stu-id="a29f3-111">This function retrieves the value of a number value and converts to an `int` value.</span></span> <span data-ttu-id="a29f3-112">`JsErrorInvalidArgument`Wenn der Typ des Werts nicht number ist, tritt ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="a29f3-112">It will fail with `JsErrorInvalidArgument` if the type of the value is not number.</span></span>  
  
 <span data-ttu-id="a29f3-113">Erfordert einen aktiven Skriptkontext.</span><span class="sxs-lookup"><span data-stu-id="a29f3-113">Requires an active script context.</span></span>  
  
 <span data-ttu-id="a29f3-114">Diese API wird nur im EdgeHTML-Modus unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a29f3-114">This API is supported only in EdgeHTML mode.</span></span>  
  
## <span data-ttu-id="a29f3-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a29f3-115">Requirements</span></span>  
 <span data-ttu-id="a29f3-116">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="a29f3-116">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="a29f3-117">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="a29f3-117">See Also</span></span>  
 [<span data-ttu-id="a29f3-118">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="a29f3-118">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)