---
description: Ruft den JavaScript-Typ eines JsValueRef ab.
title: JsGetValueType-Funktion | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsGetValueType
helpviewer_keywords:
- JsGetValueType function
ms.assetid: f403cf7c-c8c0-4a17-bfa9-0302d00e760e
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: b2e9937ca13bf2a680a4a33c07020d06c53efdf3
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233618"
---
# <span data-ttu-id="97978-103">JsGetValueType Funktion</span><span class="sxs-lookup"><span data-stu-id="97978-103">JsGetValueType Function</span></span>

<span data-ttu-id="97978-104">Ruft den JavaScript-Typ eines JsValueRef ab.</span><span class="sxs-lookup"><span data-stu-id="97978-104">Gets the JavaScript type of a JsValueRef.</span></span>  
  
## <span data-ttu-id="97978-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="97978-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetValueType(  
   _In_ JsValueRef value,  
   _Out_ JsValueType *type  
);  
```  
  
#### <span data-ttu-id="97978-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="97978-106">Parameters</span></span>  
 `value`  
 <span data-ttu-id="97978-107">Der Wert, dessen Typ zurückgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="97978-107">The value whose type is to be returned.</span></span>  
  
 `type`  
 <span data-ttu-id="97978-108">Der Typ des Werts.</span><span class="sxs-lookup"><span data-stu-id="97978-108">The type of the value.</span></span>  
  
## <span data-ttu-id="97978-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="97978-109">Return Value</span></span>  
 <span data-ttu-id="97978-110">Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="97978-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="97978-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="97978-111">Remarks</span></span>  
 <span data-ttu-id="97978-112">Erfordert einen aktiven Skriptkontext.</span><span class="sxs-lookup"><span data-stu-id="97978-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="97978-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="97978-113">Requirements</span></span>  
 <span data-ttu-id="97978-114">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="97978-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="97978-115">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="97978-115">See Also</span></span>  
 [<span data-ttu-id="97978-116">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="97978-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
