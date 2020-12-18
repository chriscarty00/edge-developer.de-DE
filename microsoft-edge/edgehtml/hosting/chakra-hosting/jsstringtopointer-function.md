---
description: Ruft den Zeichenfolgenzeiger eines Zeichenfolgenwerts ab.
title: JsStringToPointer-Funktion | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsStringToPointer
helpviewer_keywords:
- JsStringToPointer function
ms.assetid: c7aa7a09-489d-4435-8f8a-aeb62f8875ae
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 77b8e16be41d8b5541129b50fa200b947f566342
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233906"
---
# <span data-ttu-id="60467-103">JsStringToPointer Funktion</span><span class="sxs-lookup"><span data-stu-id="60467-103">JsStringToPointer Function</span></span>

<span data-ttu-id="60467-104">Ruft den Zeichenfolgenzeiger eines Zeichenfolgenwerts ab.</span><span class="sxs-lookup"><span data-stu-id="60467-104">Retrieves the string pointer of a string value.</span></span>  
  
## <span data-ttu-id="60467-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="60467-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsStringToPointer(  
   _In_ JsValueRef value,  
   _Outptr_result_buffer_(*stringLength) const wchar_t **stringValue,  
   _Out_ size_t *stringLength  
);  
```  
  
#### <span data-ttu-id="60467-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="60467-106">Parameters</span></span>  
 `value`  
 <span data-ttu-id="60467-107">Der Zeichenfolgenwert, der in einen Zeichenfolgenzeiger konvertiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="60467-107">The string value to convert to a string pointer.</span></span>  
  
 `stringValue`  
 <span data-ttu-id="60467-108">Der Zeichenfolgenzeiger.</span><span class="sxs-lookup"><span data-stu-id="60467-108">The string pointer.</span></span>  
  
 `stringLength`  
 <span data-ttu-id="60467-109">Die Länge der Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="60467-109">The length of the string.</span></span>  
  
## <span data-ttu-id="60467-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="60467-110">Return Value</span></span>  
 <span data-ttu-id="60467-111">Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="60467-111">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="60467-112">Hinweise</span><span class="sxs-lookup"><span data-stu-id="60467-112">Remarks</span></span>  
 <span data-ttu-id="60467-113">Diese Funktion Ruft den Zeichenfolgenzeiger eines Zeichenfolgenwerts ab.</span><span class="sxs-lookup"><span data-stu-id="60467-113">This function retrieves the string pointer of a string value.</span></span> <span data-ttu-id="60467-114">`JsErrorInvalidArgument`Wenn der Typ des Werts keine Zeichenfolge ist, tritt ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="60467-114">It will fail with `JsErrorInvalidArgument` if the type of the value is not string.</span></span> <span data-ttu-id="60467-115">Die Lebensdauer der zurückgegebenen Zeichenfolge entspricht der Lebensdauer des Werts, von dem Sie stammen, der Zeichenfolgenzeiger wird jedoch nicht als Verweis auf den Wert betrachtet (und wird daher nicht davon abgeholt).</span><span class="sxs-lookup"><span data-stu-id="60467-115">The lifetime of the string returned will be the same as the lifetime of the value it came from, however the string pointer is not considered a reference to the value (and so will not keep it from being collected).</span></span>  
  
 <span data-ttu-id="60467-116">Erfordert einen aktiven Skriptkontext.</span><span class="sxs-lookup"><span data-stu-id="60467-116">Requires an active script context.</span></span>  
  
## <span data-ttu-id="60467-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="60467-117">Requirements</span></span>  
 <span data-ttu-id="60467-118">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="60467-118">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="60467-119">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="60467-119">See Also</span></span>  
 [<span data-ttu-id="60467-120">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="60467-120">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
