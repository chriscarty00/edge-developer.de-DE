---
description: Erstellt einen Zeichenfolgenwert aus einem Zeichenfolgenzeiger.
title: JsPointerToString-Funktion | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsPointerToString
helpviewer_keywords:
- JsPointerToString function
ms.assetid: c71ce07e-4359-450c-afbf-a6ab7d48dddf
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: c00a060098f0b021afca27b300f3e0578e992cb9
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11234082"
---
# <span data-ttu-id="ef4f8-103">JsPointerToString Funktion</span><span class="sxs-lookup"><span data-stu-id="ef4f8-103">JsPointerToString Function</span></span>

<span data-ttu-id="ef4f8-104">Erstellt einen Zeichenfolgenwert aus einem Zeichenfolgenzeiger.</span><span class="sxs-lookup"><span data-stu-id="ef4f8-104">Creates a string value from a string pointer.</span></span>  
  
## <span data-ttu-id="ef4f8-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ef4f8-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsPointerToString(  
   _In_reads_(stringLength) const wchar_t *stringValue,  
   _In_ size_t stringLength,  
   _Out_ JsValueRef *value  
);  
```  
  
#### <span data-ttu-id="ef4f8-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ef4f8-106">Parameters</span></span>  
 `stringValue`  
 <span data-ttu-id="ef4f8-107">Der Zeichenfolgenzeiger, der in einen Zeichenfolgenwert konvertiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="ef4f8-107">The string pointer to convert to a string value.</span></span>  
  
 `stringLength`  
 <span data-ttu-id="ef4f8-108">Die Länge der zu konvertierenden Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="ef4f8-108">The length of the string to convert.</span></span>  
  
 `value`  
 <span data-ttu-id="ef4f8-109">Der neue Zeichenfolgenwert.</span><span class="sxs-lookup"><span data-stu-id="ef4f8-109">The new string value.</span></span>  
  
## <span data-ttu-id="ef4f8-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ef4f8-110">Return Value</span></span>  
 <span data-ttu-id="ef4f8-111">Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="ef4f8-111">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="ef4f8-112">Hinweise</span><span class="sxs-lookup"><span data-stu-id="ef4f8-112">Remarks</span></span>  
 <span data-ttu-id="ef4f8-113">Erfordert einen aktiven Skriptkontext.</span><span class="sxs-lookup"><span data-stu-id="ef4f8-113">Requires an active script context.</span></span>  
  
## <span data-ttu-id="ef4f8-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ef4f8-114">Requirements</span></span>  
 <span data-ttu-id="ef4f8-115">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="ef4f8-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="ef4f8-116">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="ef4f8-116">See Also</span></span>  
 [<span data-ttu-id="ef4f8-117">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="ef4f8-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
