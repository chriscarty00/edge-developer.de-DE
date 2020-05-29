---
description: Bestimmt, ob ein Objekt eine Eigenschaft aufweist.
title: JsHasProperty-Funktion | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsHasProperty
helpviewer_keywords:
- JsHasProperty function
ms.assetid: 26c94c3d-aae6-4257-8644-df63c7e714fb
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: c6cc195ae02c28500f0a018256d24278ad4b47d8
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10568360"
---
# <span data-ttu-id="96e46-103">JsHasProperty-Funktion</span><span class="sxs-lookup"><span data-stu-id="96e46-103">JsHasProperty Function</span></span>
<span data-ttu-id="96e46-104">Bestimmt, ob ein Objekt eine Eigenschaft aufweist.</span><span class="sxs-lookup"><span data-stu-id="96e46-104">Determines whether an object has a property.</span></span>  
  
## <span data-ttu-id="96e46-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="96e46-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsHasProperty(  
   _In_ JsValueRef object,  
   _In_ JsPropertyIdRef propertyId,  
   _Out_ bool *hasProperty  
);  
```  
  
#### <span data-ttu-id="96e46-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="96e46-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="96e46-107">Das Objekt, das die Eigenschaft enthalten kann.</span><span class="sxs-lookup"><span data-stu-id="96e46-107">The object that may contain the property.</span></span>  
  
 `propertyId`  
 <span data-ttu-id="96e46-108">Die ID der Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="96e46-108">The ID of the property.</span></span>  
  
 `hasProperty`  
 <span data-ttu-id="96e46-109">Gibt an, ob das Objekt (oder ein Prototyp) die Eigenschaft aufweist.</span><span class="sxs-lookup"><span data-stu-id="96e46-109">Whether the object (or a prototype) has the property.</span></span>  
  
## <span data-ttu-id="96e46-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="96e46-110">Return Value</span></span>  
 <span data-ttu-id="96e46-111">Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="96e46-111">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="96e46-112">Hinweise</span><span class="sxs-lookup"><span data-stu-id="96e46-112">Remarks</span></span>  
 <span data-ttu-id="96e46-113">Erfordert einen aktiven Skriptkontext.</span><span class="sxs-lookup"><span data-stu-id="96e46-113">Requires an active script context.</span></span>  
  
## <span data-ttu-id="96e46-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="96e46-114">Requirements</span></span>  
 <span data-ttu-id="96e46-115">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="96e46-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="96e46-116">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="96e46-116">See Also</span></span>  
 [<span data-ttu-id="96e46-117">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="96e46-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)