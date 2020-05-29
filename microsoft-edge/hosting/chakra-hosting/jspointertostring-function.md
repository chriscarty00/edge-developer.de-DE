---
description: Erstellt einen Zeichenfolgenwert aus einem Zeichenfolgenzeiger.
title: JsPointerToString-Funktion | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsPointerToString
helpviewer_keywords:
- JsPointerToString function
ms.assetid: c71ce07e-4359-450c-afbf-a6ab7d48dddf
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: b3c5b2d6439244bc9584e15c361412c8a1e87557
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10568348"
---
# <span data-ttu-id="6f1a9-103">JsPointerToString-Funktion</span><span class="sxs-lookup"><span data-stu-id="6f1a9-103">JsPointerToString Function</span></span>
<span data-ttu-id="6f1a9-104">Erstellt einen Zeichenfolgenwert aus einem Zeichenfolgenzeiger.</span><span class="sxs-lookup"><span data-stu-id="6f1a9-104">Creates a string value from a string pointer.</span></span>  
  
## <span data-ttu-id="6f1a9-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="6f1a9-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsPointerToString(  
   _In_reads_(stringLength) const wchar_t *stringValue,  
   _In_ size_t stringLength,  
   _Out_ JsValueRef *value  
);  
```  
  
#### <span data-ttu-id="6f1a9-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="6f1a9-106">Parameters</span></span>  
 `stringValue`  
 <span data-ttu-id="6f1a9-107">Der Zeichenfolgenzeiger, der in einen Zeichenfolgenwert konvertiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="6f1a9-107">The string pointer to convert to a string value.</span></span>  
  
 `stringLength`  
 <span data-ttu-id="6f1a9-108">Die Länge der zu konvertierenden Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="6f1a9-108">The length of the string to convert.</span></span>  
  
 `value`  
 <span data-ttu-id="6f1a9-109">Der neue Zeichenfolgenwert.</span><span class="sxs-lookup"><span data-stu-id="6f1a9-109">The new string value.</span></span>  
  
## <span data-ttu-id="6f1a9-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6f1a9-110">Return Value</span></span>  
 <span data-ttu-id="6f1a9-111">Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="6f1a9-111">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="6f1a9-112">Hinweise</span><span class="sxs-lookup"><span data-stu-id="6f1a9-112">Remarks</span></span>  
 <span data-ttu-id="6f1a9-113">Erfordert einen aktiven Skriptkontext.</span><span class="sxs-lookup"><span data-stu-id="6f1a9-113">Requires an active script context.</span></span>  
  
## <span data-ttu-id="6f1a9-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6f1a9-114">Requirements</span></span>  
 <span data-ttu-id="6f1a9-115">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="6f1a9-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="6f1a9-116">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="6f1a9-116">See Also</span></span>  
 [<span data-ttu-id="6f1a9-117">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="6f1a9-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)