---
description: Legt den Prototyp eines Objekts fest.
title: JsSetPrototype-Funktion | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 88e1e421-4ae5-4e3b-b377-19256cc80e9f
caps.latest.revision: 4
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 860a7b8d85e043c87d554e09de50d0cb642b273a
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233734"
---
# <span data-ttu-id="9a2d4-103">JsSetPrototype Funktion</span><span class="sxs-lookup"><span data-stu-id="9a2d4-103">JsSetPrototype Function</span></span>

<span data-ttu-id="9a2d4-104">Legt den Prototyp eines Objekts fest.</span><span class="sxs-lookup"><span data-stu-id="9a2d4-104">Sets the prototype of an object.</span></span>  
  
## <span data-ttu-id="9a2d4-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="9a2d4-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsSetPrototype(  
   _In_ JsValueRef object,  
   _In_ JsValueRef prototypeObject  
);  
```  
  
#### <span data-ttu-id="9a2d4-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="9a2d4-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="9a2d4-107">Das Objekt, dessen Prototyp geändert werden soll.</span><span class="sxs-lookup"><span data-stu-id="9a2d4-107">The object whose prototype is to be changed.</span></span>  
  
 `prototypeObject`  
 <span data-ttu-id="9a2d4-108">Der neue Prototyp des Objekts.</span><span class="sxs-lookup"><span data-stu-id="9a2d4-108">The object's new prototype.</span></span>  
  
## <span data-ttu-id="9a2d4-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9a2d4-109">Return Value</span></span>  
 <span data-ttu-id="9a2d4-110">Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="9a2d4-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="9a2d4-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="9a2d4-111">Remarks</span></span>  
 <span data-ttu-id="9a2d4-112">Erfordert einen aktiven Skriptkontext.</span><span class="sxs-lookup"><span data-stu-id="9a2d4-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="9a2d4-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9a2d4-113">Requirements</span></span>  
 <span data-ttu-id="9a2d4-114">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="9a2d4-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="9a2d4-115">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="9a2d4-115">See Also</span></span>  
 [<span data-ttu-id="9a2d4-116">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="9a2d4-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
