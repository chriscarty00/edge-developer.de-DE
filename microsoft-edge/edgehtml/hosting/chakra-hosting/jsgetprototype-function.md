---
description: Gibt den Prototyp eines Objekts zurück.
title: JsGetPrototype-Funktion | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsGetPrototype
helpviewer_keywords:
- JsGetPrototype function
ms.assetid: 05d743fc-103e-4a92-86f2-a063f39a2a6f
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: d64e8b090753e5d0627f0d40ee8745eeadd65227
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11234249"
---
# <span data-ttu-id="1ba85-103">JsGetPrototype Funktion</span><span class="sxs-lookup"><span data-stu-id="1ba85-103">JsGetPrototype Function</span></span>

<span data-ttu-id="1ba85-104">Gibt den Prototyp eines Objekts zurück.</span><span class="sxs-lookup"><span data-stu-id="1ba85-104">Returns the prototype of an object.</span></span>  
  
## <span data-ttu-id="1ba85-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="1ba85-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetPrototype(  
   _In_ JsValueRef object,  
   _Out_ JsValueRef *prototypeObject  
);  
```  
  
#### <span data-ttu-id="1ba85-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="1ba85-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="1ba85-107">Das Objekt, dessen Prototyp zurückgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="1ba85-107">The object whose prototype is to be returned.</span></span>  
  
 `prototypeObject`  
 <span data-ttu-id="1ba85-108">Der Prototyp des Objekts.</span><span class="sxs-lookup"><span data-stu-id="1ba85-108">The object's prototype.</span></span>  
  
## <span data-ttu-id="1ba85-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1ba85-109">Return Value</span></span>  
 <span data-ttu-id="1ba85-110">Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="1ba85-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="1ba85-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="1ba85-111">Remarks</span></span>  
 <span data-ttu-id="1ba85-112">Erfordert einen aktiven Skriptkontext.</span><span class="sxs-lookup"><span data-stu-id="1ba85-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="1ba85-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1ba85-113">Requirements</span></span>  
 <span data-ttu-id="1ba85-114">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="1ba85-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="1ba85-115">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="1ba85-115">See Also</span></span>  
 [<span data-ttu-id="1ba85-116">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="1ba85-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
