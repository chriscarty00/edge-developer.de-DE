---
description: Ruft die Länge eines Zeichenfolgenwerts ab.
title: JsGetStringLength-Funktion | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsGetStringLength
helpviewer_keywords:
- JsGetStringLength function
ms.assetid: e9f9f28c-e644-439c-aee5-7ce362f71347
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 10fd6be4bb839ccb9eb64c99931cdb474e3aa7a2
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11234320"
---
# <span data-ttu-id="9ecab-103">JsGetStringLength Funktion</span><span class="sxs-lookup"><span data-stu-id="9ecab-103">JsGetStringLength Function</span></span>

<span data-ttu-id="9ecab-104">Ruft die Länge eines Zeichenfolgenwerts ab.</span><span class="sxs-lookup"><span data-stu-id="9ecab-104">Gets the length of a string value.</span></span>  
  
## <span data-ttu-id="9ecab-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="9ecab-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetStringLength(  
   _In_ JsValueRef stringValue,  
   _Out_ int *length  
);  
```  
  
#### <span data-ttu-id="9ecab-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="9ecab-106">Parameters</span></span>  
 `stringValue`  
 <span data-ttu-id="9ecab-107">Der Zeichenfolgenwert, dessen Länge abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="9ecab-107">The string value to get the length of.</span></span>  
  
 `length`  
 <span data-ttu-id="9ecab-108">Die Länge der Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="9ecab-108">The length of the string.</span></span>  
  
## <span data-ttu-id="9ecab-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9ecab-109">Return Value</span></span>  
 <span data-ttu-id="9ecab-110">Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="9ecab-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="9ecab-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="9ecab-111">Remarks</span></span>  
 <span data-ttu-id="9ecab-112">Erfordert einen aktiven Skriptkontext.</span><span class="sxs-lookup"><span data-stu-id="9ecab-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="9ecab-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9ecab-113">Requirements</span></span>  
 <span data-ttu-id="9ecab-114">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="9ecab-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="9ecab-115">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="9ecab-115">See Also</span></span>  
 [<span data-ttu-id="9ecab-116">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="9ecab-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
