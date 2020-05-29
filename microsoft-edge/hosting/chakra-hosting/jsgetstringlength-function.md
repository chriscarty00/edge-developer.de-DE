---
description: Ruft die Länge eines Zeichenfolgenwerts ab.
title: JsGetStringLength-Funktion | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsGetStringLength
helpviewer_keywords:
- JsGetStringLength function
ms.assetid: e9f9f28c-e644-439c-aee5-7ce362f71347
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 6b562b2dc58341523910db41fb8b748453b2a836
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10567242"
---
# <span data-ttu-id="bdb94-103">JsGetStringLength-Funktion</span><span class="sxs-lookup"><span data-stu-id="bdb94-103">JsGetStringLength Function</span></span>
<span data-ttu-id="bdb94-104">Ruft die Länge eines Zeichenfolgenwerts ab.</span><span class="sxs-lookup"><span data-stu-id="bdb94-104">Gets the length of a string value.</span></span>  
  
## <span data-ttu-id="bdb94-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="bdb94-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetStringLength(  
   _In_ JsValueRef stringValue,  
   _Out_ int *length  
);  
```  
  
#### <span data-ttu-id="bdb94-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="bdb94-106">Parameters</span></span>  
 `stringValue`  
 <span data-ttu-id="bdb94-107">Der Zeichenfolgenwert, dessen Länge abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="bdb94-107">The string value to get the length of.</span></span>  
  
 `length`  
 <span data-ttu-id="bdb94-108">Die Länge der Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="bdb94-108">The length of the string.</span></span>  
  
## <span data-ttu-id="bdb94-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bdb94-109">Return Value</span></span>  
 <span data-ttu-id="bdb94-110">Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="bdb94-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="bdb94-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="bdb94-111">Remarks</span></span>  
 <span data-ttu-id="bdb94-112">Erfordert einen aktiven Skriptkontext.</span><span class="sxs-lookup"><span data-stu-id="bdb94-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="bdb94-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bdb94-113">Requirements</span></span>  
 <span data-ttu-id="bdb94-114">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="bdb94-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="bdb94-115">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="bdb94-115">See Also</span></span>  
 [<span data-ttu-id="bdb94-116">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="bdb94-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)