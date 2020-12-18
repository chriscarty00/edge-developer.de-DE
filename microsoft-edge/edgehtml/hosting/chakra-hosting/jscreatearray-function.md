---
description: Erstellt ein JavaScript-Array Objekt.
title: JsCreateArray-Funktion | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsCreateArray
helpviewer_keywords:
- JsCreateArray function
ms.assetid: a119949a-e427-4349-9d00-5ec20fb9319c
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 34ce07055fa3d4d24188d7edbcedc3f08973e233
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233753"
---
# <span data-ttu-id="51478-103">JsCreateArray Funktion</span><span class="sxs-lookup"><span data-stu-id="51478-103">JsCreateArray Function</span></span>

<span data-ttu-id="51478-104">Erstellt ein JavaScript-Array Objekt.</span><span class="sxs-lookup"><span data-stu-id="51478-104">Creates a Javascript array object.</span></span>  
  
## <span data-ttu-id="51478-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="51478-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsCreateArray(  
   _In_ unsigned int length,  
   _Out_ JsValueRef *result  
);  
```  
  
#### <span data-ttu-id="51478-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="51478-106">Parameters</span></span>  
 `length`  
 <span data-ttu-id="51478-107">Die anfängliche Länge des Arrays.</span><span class="sxs-lookup"><span data-stu-id="51478-107">The initial length of the array.</span></span>  
  
 `result`  
 <span data-ttu-id="51478-108">Das neue Array-Objekt.</span><span class="sxs-lookup"><span data-stu-id="51478-108">The new array object.</span></span>  
  
## <span data-ttu-id="51478-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="51478-109">Return Value</span></span>  
 <span data-ttu-id="51478-110">Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="51478-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="51478-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="51478-111">Remarks</span></span>  
 <span data-ttu-id="51478-112">Erfordert einen aktiven Skriptkontext.</span><span class="sxs-lookup"><span data-stu-id="51478-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="51478-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="51478-113">Requirements</span></span>  
 <span data-ttu-id="51478-114">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="51478-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="51478-115">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="51478-115">See Also</span></span>  
 [<span data-ttu-id="51478-116">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="51478-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
