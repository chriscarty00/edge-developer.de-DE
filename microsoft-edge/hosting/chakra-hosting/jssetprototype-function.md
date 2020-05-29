---
description: Legt den Prototyp eines Objekts fest.
title: JsSetPrototype-Funktion | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 88e1e421-4ae5-4e3b-b377-19256cc80e9f
caps.latest.revision: 4
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 625269c5f9f459a5c7eecb6cfc31cb85fc24214b
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10568221"
---
# <span data-ttu-id="c5aaa-103">JsSetPrototype-Funktion</span><span class="sxs-lookup"><span data-stu-id="c5aaa-103">JsSetPrototype Function</span></span>
<span data-ttu-id="c5aaa-104">Legt den Prototyp eines Objekts fest.</span><span class="sxs-lookup"><span data-stu-id="c5aaa-104">Sets the prototype of an object.</span></span>  
  
## <span data-ttu-id="c5aaa-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c5aaa-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsSetPrototype(  
   _In_ JsValueRef object,  
   _In_ JsValueRef prototypeObject  
);  
```  
  
#### <span data-ttu-id="c5aaa-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c5aaa-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="c5aaa-107">Das Objekt, dessen Prototyp geändert werden soll.</span><span class="sxs-lookup"><span data-stu-id="c5aaa-107">The object whose prototype is to be changed.</span></span>  
  
 `prototypeObject`  
 <span data-ttu-id="c5aaa-108">Der neue Prototyp des Objekts.</span><span class="sxs-lookup"><span data-stu-id="c5aaa-108">The object's new prototype.</span></span>  
  
## <span data-ttu-id="c5aaa-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c5aaa-109">Return Value</span></span>  
 <span data-ttu-id="c5aaa-110">Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="c5aaa-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="c5aaa-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="c5aaa-111">Remarks</span></span>  
 <span data-ttu-id="c5aaa-112">Erfordert einen aktiven Skriptkontext.</span><span class="sxs-lookup"><span data-stu-id="c5aaa-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="c5aaa-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c5aaa-113">Requirements</span></span>  
 <span data-ttu-id="c5aaa-114">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="c5aaa-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="c5aaa-115">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="c5aaa-115">See Also</span></span>  
 [<span data-ttu-id="c5aaa-116">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="c5aaa-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)