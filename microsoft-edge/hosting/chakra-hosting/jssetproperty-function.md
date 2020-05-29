---
description: Fügt die Eigenschaft eines Objekts ein.
title: JsSetProperty-Funktion | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsSetProperty
helpviewer_keywords:
- JsSetProperty function
ms.assetid: 2c36bebf-ec86-425c-8131-2dd75fd30f40
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 2aba03a73f35284f79355a7d93161d9a9518012c
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10568301"
---
# <span data-ttu-id="87632-103">JsSetProperty-Funktion</span><span class="sxs-lookup"><span data-stu-id="87632-103">JsSetProperty Function</span></span>
<span data-ttu-id="87632-104">Fügt die Eigenschaft eines Objekts ein.</span><span class="sxs-lookup"><span data-stu-id="87632-104">Puts an object's property.</span></span>  
  
## <span data-ttu-id="87632-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="87632-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsSetProperty(  
   _In_ JsValueRef object,  
   _In_ JsPropertyIdRef propertyId,  
   _In_ JsValueRef value,  
   _In_ bool useStrictRules  
);  
```  
  
#### <span data-ttu-id="87632-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="87632-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="87632-107">Das Objekt, das die Eigenschaft enthält.</span><span class="sxs-lookup"><span data-stu-id="87632-107">The object that contains the property.</span></span>  
  
 `propertyId`  
 <span data-ttu-id="87632-108">Die ID der Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="87632-108">The ID of the property.</span></span>  
  
 `value`  
 <span data-ttu-id="87632-109">Der neue Wert der Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="87632-109">The new value of the property.</span></span>  
  
 `useStrictRules`  
 <span data-ttu-id="87632-110">Der Eigenschaftensatz sollte strikte Regeln für den Modus befolgen.</span><span class="sxs-lookup"><span data-stu-id="87632-110">The property set should follow strict mode rules.</span></span>  
  
## <span data-ttu-id="87632-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="87632-111">Return Value</span></span>  
 <span data-ttu-id="87632-112">Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="87632-112">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="87632-113">Hinweise</span><span class="sxs-lookup"><span data-stu-id="87632-113">Remarks</span></span>  
 <span data-ttu-id="87632-114">Erfordert einen aktiven Skriptkontext.</span><span class="sxs-lookup"><span data-stu-id="87632-114">Requires an active script context.</span></span>  
  
## <span data-ttu-id="87632-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="87632-115">Requirements</span></span>  
 <span data-ttu-id="87632-116">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="87632-116">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="87632-117">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="87632-117">See Also</span></span>  
 [<span data-ttu-id="87632-118">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="87632-118">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)