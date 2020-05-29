---
description: Gibt einen Wert zurück, der angibt, ob ein Objekt erweiterbar ist oder nicht.
title: JsGetExtensionAllowed-Funktion | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsGetExtensionAllowed
helpviewer_keywords:
- JsGetExtensionAllowed function
ms.assetid: 839054a1-d643-47d9-89db-6a015bba0d91
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: e3baa6449294f7b055251d861a32095deb1bdfe9
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10567258"
---
# <span data-ttu-id="78fa3-103">JsGetExtensionAllowed-Funktion</span><span class="sxs-lookup"><span data-stu-id="78fa3-103">JsGetExtensionAllowed Function</span></span>
<span data-ttu-id="78fa3-104">Gibt einen Wert zurück, der angibt, ob ein Objekt erweiterbar ist oder nicht.</span><span class="sxs-lookup"><span data-stu-id="78fa3-104">Returns a value that indicates whether an object is extensible or not.</span></span>  
  
## <span data-ttu-id="78fa3-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="78fa3-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetExtensionAllowed(  
   _In_ JsValueRef object,  
   _Out_ bool *value  
);  
```  
  
#### <span data-ttu-id="78fa3-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="78fa3-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="78fa3-107">Das zu testende Objekt.</span><span class="sxs-lookup"><span data-stu-id="78fa3-107">The object to test.</span></span>  
  
 `value`  
 <span data-ttu-id="78fa3-108">Gibt an, ob das Objekt erweiterbar ist oder nicht.</span><span class="sxs-lookup"><span data-stu-id="78fa3-108">Whether the object is extensible or not.</span></span>  
  
## <span data-ttu-id="78fa3-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="78fa3-109">Return Value</span></span>  
 <span data-ttu-id="78fa3-110">Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="78fa3-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="78fa3-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="78fa3-111">Remarks</span></span>  
 <span data-ttu-id="78fa3-112">Erfordert einen aktiven Skriptkontext.</span><span class="sxs-lookup"><span data-stu-id="78fa3-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="78fa3-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="78fa3-113">Requirements</span></span>  
 <span data-ttu-id="78fa3-114">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="78fa3-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="78fa3-115">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="78fa3-115">See Also</span></span>  
 [<span data-ttu-id="78fa3-116">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="78fa3-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)