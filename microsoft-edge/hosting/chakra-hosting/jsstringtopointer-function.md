---
description: Ruft den Zeichenfolgenzeiger eines Zeichenfolgenwerts ab.
title: JsStringToPointer-Funktion | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsStringToPointer
helpviewer_keywords:
- JsStringToPointer function
ms.assetid: c7aa7a09-489d-4435-8f8a-aeb62f8875ae
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 1f5997894c4ea479378a323b230492dde28ab177
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10568204"
---
# <span data-ttu-id="52674-103">JsStringToPointer-Funktion</span><span class="sxs-lookup"><span data-stu-id="52674-103">JsStringToPointer Function</span></span>
<span data-ttu-id="52674-104">Ruft den Zeichenfolgenzeiger eines Zeichenfolgenwerts ab.</span><span class="sxs-lookup"><span data-stu-id="52674-104">Retrieves the string pointer of a string value.</span></span>  
  
## <span data-ttu-id="52674-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="52674-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsStringToPointer(  
   _In_ JsValueRef value,  
   _Outptr_result_buffer_(*stringLength) const wchar_t **stringValue,  
   _Out_ size_t *stringLength  
);  
```  
  
#### <span data-ttu-id="52674-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="52674-106">Parameters</span></span>  
 `value`  
 <span data-ttu-id="52674-107">Der Zeichenfolgenwert, der in einen Zeichenfolgenzeiger konvertiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="52674-107">The string value to convert to a string pointer.</span></span>  
  
 `stringValue`  
 <span data-ttu-id="52674-108">Der Zeichenfolgenzeiger.</span><span class="sxs-lookup"><span data-stu-id="52674-108">The string pointer.</span></span>  
  
 `stringLength`  
 <span data-ttu-id="52674-109">Die Länge der Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="52674-109">The length of the string.</span></span>  
  
## <span data-ttu-id="52674-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="52674-110">Return Value</span></span>  
 <span data-ttu-id="52674-111">Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="52674-111">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="52674-112">Hinweise</span><span class="sxs-lookup"><span data-stu-id="52674-112">Remarks</span></span>  
 <span data-ttu-id="52674-113">Diese Funktion Ruft den Zeichenfolgenzeiger eines Zeichenfolgenwerts ab.</span><span class="sxs-lookup"><span data-stu-id="52674-113">This function retrieves the string pointer of a string value.</span></span> <span data-ttu-id="52674-114">`JsErrorInvalidArgument`Wenn der Typ des Werts keine Zeichenfolge ist, tritt ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="52674-114">It will fail with `JsErrorInvalidArgument` if the type of the value is not string.</span></span> <span data-ttu-id="52674-115">Die Lebensdauer der zurückgegebenen Zeichenfolge entspricht der Lebensdauer des Werts, von dem Sie stammen, der Zeichenfolgenzeiger wird jedoch nicht als Verweis auf den Wert betrachtet (und wird daher nicht davon abgeholt).</span><span class="sxs-lookup"><span data-stu-id="52674-115">The lifetime of the string returned will be the same as the lifetime of the value it came from, however the string pointer is not considered a reference to the value (and so will not keep it from being collected).</span></span>  
  
 <span data-ttu-id="52674-116">Erfordert einen aktiven Skriptkontext.</span><span class="sxs-lookup"><span data-stu-id="52674-116">Requires an active script context.</span></span>  
  
## <span data-ttu-id="52674-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="52674-117">Requirements</span></span>  
 <span data-ttu-id="52674-118">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="52674-118">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="52674-119">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="52674-119">See Also</span></span>  
 [<span data-ttu-id="52674-120">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="52674-120">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)