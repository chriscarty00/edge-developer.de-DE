---
description: Gibt einen Wert zurück, der angibt, ob ein Objekt erweiterbar ist oder nicht.
title: JsGetExtensionAllowed-Funktion | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsGetExtensionAllowed
helpviewer_keywords:
- JsGetExtensionAllowed function
ms.assetid: 839054a1-d643-47d9-89db-6a015bba0d91
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 7bc9e3265b48a27d0da4bc4646b2b5e3b1765b86
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233997"
---
# <span data-ttu-id="9cfcb-103">JsGetExtensionAllowed Funktion</span><span class="sxs-lookup"><span data-stu-id="9cfcb-103">JsGetExtensionAllowed Function</span></span>

<span data-ttu-id="9cfcb-104">Gibt einen Wert zurück, der angibt, ob ein Objekt erweiterbar ist oder nicht.</span><span class="sxs-lookup"><span data-stu-id="9cfcb-104">Returns a value that indicates whether an object is extensible or not.</span></span>  
  
## <span data-ttu-id="9cfcb-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="9cfcb-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetExtensionAllowed(  
   _In_ JsValueRef object,  
   _Out_ bool *value  
);  
```  
  
#### <span data-ttu-id="9cfcb-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="9cfcb-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="9cfcb-107">Das zu testende Objekt.</span><span class="sxs-lookup"><span data-stu-id="9cfcb-107">The object to test.</span></span>  
  
 `value`  
 <span data-ttu-id="9cfcb-108">Gibt an, ob das Objekt erweiterbar ist oder nicht.</span><span class="sxs-lookup"><span data-stu-id="9cfcb-108">Whether the object is extensible or not.</span></span>  
  
## <span data-ttu-id="9cfcb-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9cfcb-109">Return Value</span></span>  
 <span data-ttu-id="9cfcb-110">Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="9cfcb-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="9cfcb-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="9cfcb-111">Remarks</span></span>  
 <span data-ttu-id="9cfcb-112">Erfordert einen aktiven Skriptkontext.</span><span class="sxs-lookup"><span data-stu-id="9cfcb-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="9cfcb-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9cfcb-113">Requirements</span></span>  
 <span data-ttu-id="9cfcb-114">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="9cfcb-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="9cfcb-115">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="9cfcb-115">See Also</span></span>  
 [<span data-ttu-id="9cfcb-116">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="9cfcb-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
