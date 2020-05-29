---
description: Gibt den Prototyp eines Objekts zurück.
title: JsGetPrototype-Funktion | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsGetPrototype
helpviewer_keywords:
- JsGetPrototype function
ms.assetid: 05d743fc-103e-4a92-86f2-a063f39a2a6f
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 12708634fea9e8f9fd1205514845b1cb9760ee9e
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10567249"
---
# <span data-ttu-id="bc08a-103">JsGetPrototype-Funktion</span><span class="sxs-lookup"><span data-stu-id="bc08a-103">JsGetPrototype Function</span></span>
<span data-ttu-id="bc08a-104">Gibt den Prototyp eines Objekts zurück.</span><span class="sxs-lookup"><span data-stu-id="bc08a-104">Returns the prototype of an object.</span></span>  
  
## <span data-ttu-id="bc08a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="bc08a-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetPrototype(  
   _In_ JsValueRef object,  
   _Out_ JsValueRef *prototypeObject  
);  
```  
  
#### <span data-ttu-id="bc08a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="bc08a-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="bc08a-107">Das Objekt, dessen Prototyp zurückgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="bc08a-107">The object whose prototype is to be returned.</span></span>  
  
 `prototypeObject`  
 <span data-ttu-id="bc08a-108">Der Prototyp des Objekts.</span><span class="sxs-lookup"><span data-stu-id="bc08a-108">The object's prototype.</span></span>  
  
## <span data-ttu-id="bc08a-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bc08a-109">Return Value</span></span>  
 <span data-ttu-id="bc08a-110">Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="bc08a-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="bc08a-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="bc08a-111">Remarks</span></span>  
 <span data-ttu-id="bc08a-112">Erfordert einen aktiven Skriptkontext.</span><span class="sxs-lookup"><span data-stu-id="bc08a-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="bc08a-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bc08a-113">Requirements</span></span>  
 <span data-ttu-id="bc08a-114">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="bc08a-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="bc08a-115">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="bc08a-115">See Also</span></span>  
 [<span data-ttu-id="bc08a-116">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="bc08a-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)