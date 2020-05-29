---
description: Initialisiert die übergebene `VARIANT` als Projektion eines JavaScript-Werts.
title: JsValueToVariant-Funktion | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsValueToVariant
helpviewer_keywords:
- JsValueToVariant function
ms.assetid: 070244be-a69d-4b78-971b-69c0579c03cf
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: d8748fddcc149cf09fbd46ad3ad489cd66200b71
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10567195"
---
# <span data-ttu-id="daaab-103">JsValueToVariant-Funktion</span><span class="sxs-lookup"><span data-stu-id="daaab-103">JsValueToVariant Function</span></span>
<span data-ttu-id="daaab-104">Initialisiert die übergebene `VARIANT` als Projektion eines JavaScript-Werts.</span><span class="sxs-lookup"><span data-stu-id="daaab-104">Initializes the passed in `VARIANT` as a projection of a JavaScript value.</span></span>  
  
## <span data-ttu-id="daaab-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="daaab-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsValueToVariant(  
   _In_ JsValueRef object,  
   _Out_ VARIANT *variant  
);  
```  
  
#### <span data-ttu-id="daaab-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="daaab-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="daaab-107">Ein JavaScript-Wert für Project als `VARIANT` .</span><span class="sxs-lookup"><span data-stu-id="daaab-107">A JavaScript value to project as a `VARIANT`.</span></span>  
  
 `variant`  
 <span data-ttu-id="daaab-108">Ein Zeiger auf eine `VARIANT` Struktur, die als Projektion initialisiert wird.</span><span class="sxs-lookup"><span data-stu-id="daaab-108">A pointer to a `VARIANT` struct that will be initialized as a projection.</span></span>  
  
## <span data-ttu-id="daaab-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="daaab-109">Return Value</span></span>  
  
## <span data-ttu-id="daaab-110">Hinweise</span><span class="sxs-lookup"><span data-stu-id="daaab-110">Remarks</span></span>  
 <span data-ttu-id="daaab-111">Die Projektion `VARIANT` kann von com-Automatisierungsclients verwendet werden, um das projizierte JavaScript-Objekt aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="daaab-111">The projection `VARIANT` can be used by COM automation clients to call into the projected JavaScript object.</span></span>  
  
 <span data-ttu-id="daaab-112">Erfordert einen aktiven Skriptkontext.</span><span class="sxs-lookup"><span data-stu-id="daaab-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="daaab-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="daaab-113">Requirements</span></span>  
 <span data-ttu-id="daaab-114">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="daaab-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="daaab-115">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="daaab-115">See Also</span></span>  
 [<span data-ttu-id="daaab-116">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="daaab-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)