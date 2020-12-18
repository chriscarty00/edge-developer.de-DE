---
description: Ruft den Wert `undefined` im aktuellen Skriptkontext ab.
title: JsGetUndefinedValue-Funktion | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsGetUndefinedValue
helpviewer_keywords:
- JsGetUndefinedValue function
ms.assetid: e118eaf6-452c-42f2-86b8-e63c7d987cba
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 34bfaec4548ee2b77d6d98749c3049bb8f679134
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233613"
---
# <span data-ttu-id="c33bd-103">JsGetUndefinedValue Funktion</span><span class="sxs-lookup"><span data-stu-id="c33bd-103">JsGetUndefinedValue Function</span></span>

<span data-ttu-id="c33bd-104">Ruft den Wert `undefined` im aktuellen Skriptkontext ab.</span><span class="sxs-lookup"><span data-stu-id="c33bd-104">Gets the value of `undefined` in the current script context.</span></span>  
  
## <span data-ttu-id="c33bd-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c33bd-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetUndefinedValue(  
   _Out_ JsValueRef *undefinedValue  
);  
```  
  
#### <span data-ttu-id="c33bd-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c33bd-106">Parameters</span></span>  
 `undefinedValue`  
 <span data-ttu-id="c33bd-107">Der `undefined` Wert.</span><span class="sxs-lookup"><span data-stu-id="c33bd-107">The `undefined` value.</span></span>  
  
## <span data-ttu-id="c33bd-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c33bd-108">Return Value</span></span>  
 <span data-ttu-id="c33bd-109">Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="c33bd-109">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="c33bd-110">Hinweise</span><span class="sxs-lookup"><span data-stu-id="c33bd-110">Remarks</span></span>  
 <span data-ttu-id="c33bd-111">Erfordert einen aktiven Skriptkontext.</span><span class="sxs-lookup"><span data-stu-id="c33bd-111">Requires an active script context.</span></span>  
  
## <span data-ttu-id="c33bd-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c33bd-112">Requirements</span></span>  
 <span data-ttu-id="c33bd-113">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="c33bd-113">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="c33bd-114">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="c33bd-114">See Also</span></span>  
 [<span data-ttu-id="c33bd-115">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="c33bd-115">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
