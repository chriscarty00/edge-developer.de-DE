---
description: Bestimmt, ob ein Objekt ein externes Objekt ist.
title: JsHasExternalData-Funktion | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsHasExternalData
helpviewer_keywords:
- JsHasExternalData function
ms.assetid: a077e3ac-4f6f-4d94-8398-f1b5cc4c18e0
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: d73333215a33fc409190a0e33fa616b6350fb2a3
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233612"
---
# <span data-ttu-id="6432d-103">JsHasExternalData Funktion</span><span class="sxs-lookup"><span data-stu-id="6432d-103">JsHasExternalData Function</span></span>

<span data-ttu-id="6432d-104">Bestimmt, ob ein Objekt ein externes Objekt ist.</span><span class="sxs-lookup"><span data-stu-id="6432d-104">Determines whether an object is an external object.</span></span>  
  
## <span data-ttu-id="6432d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="6432d-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsHasExternalData(  
   _In_ JsValueRef object,  
   _Out_ bool *value  
);  
```  
  
#### <span data-ttu-id="6432d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="6432d-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="6432d-107">Das Objekt.</span><span class="sxs-lookup"><span data-stu-id="6432d-107">The object.</span></span>  
  
 `value`  
 <span data-ttu-id="6432d-108">Gibt an, ob es sich um ein externes Objekt handelt.</span><span class="sxs-lookup"><span data-stu-id="6432d-108">Whether the object is an external object.</span></span>  
  
## <span data-ttu-id="6432d-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6432d-109">Return Value</span></span>  
 <span data-ttu-id="6432d-110">Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="6432d-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="6432d-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="6432d-111">Remarks</span></span>  
 <span data-ttu-id="6432d-112">Erfordert einen aktiven Skriptkontext.</span><span class="sxs-lookup"><span data-stu-id="6432d-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="6432d-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6432d-113">Requirements</span></span>  
 <span data-ttu-id="6432d-114">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="6432d-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="6432d-115">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="6432d-115">See Also</span></span>  
 [<span data-ttu-id="6432d-116">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="6432d-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
