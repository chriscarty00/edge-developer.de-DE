---
description: Bestimmt, ob ein Objekt ein externes Objekt ist.
title: JsHasExternalData-Funktion | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsHasExternalData
helpviewer_keywords:
- JsHasExternalData function
ms.assetid: a077e3ac-4f6f-4d94-8398-f1b5cc4c18e0
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 0ca86df09264eb82dac2e928874ca15edd2c8c8e
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10568367"
---
# <span data-ttu-id="04cc6-103">JsHasExternalData-Funktion</span><span class="sxs-lookup"><span data-stu-id="04cc6-103">JsHasExternalData Function</span></span>
<span data-ttu-id="04cc6-104">Bestimmt, ob ein Objekt ein externes Objekt ist.</span><span class="sxs-lookup"><span data-stu-id="04cc6-104">Determines whether an object is an external object.</span></span>  
  
## <span data-ttu-id="04cc6-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="04cc6-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsHasExternalData(  
   _In_ JsValueRef object,  
   _Out_ bool *value  
);  
```  
  
#### <span data-ttu-id="04cc6-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="04cc6-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="04cc6-107">Das Objekt.</span><span class="sxs-lookup"><span data-stu-id="04cc6-107">The object.</span></span>  
  
 `value`  
 <span data-ttu-id="04cc6-108">Gibt an, ob es sich um ein externes Objekt handelt.</span><span class="sxs-lookup"><span data-stu-id="04cc6-108">Whether the object is an external object.</span></span>  
  
## <span data-ttu-id="04cc6-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="04cc6-109">Return Value</span></span>  
 <span data-ttu-id="04cc6-110">Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="04cc6-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="04cc6-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="04cc6-111">Remarks</span></span>  
 <span data-ttu-id="04cc6-112">Erfordert einen aktiven Skriptkontext.</span><span class="sxs-lookup"><span data-stu-id="04cc6-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="04cc6-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="04cc6-113">Requirements</span></span>  
 <span data-ttu-id="04cc6-114">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="04cc6-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="04cc6-115">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="04cc6-115">See Also</span></span>  
 [<span data-ttu-id="04cc6-116">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="04cc6-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)