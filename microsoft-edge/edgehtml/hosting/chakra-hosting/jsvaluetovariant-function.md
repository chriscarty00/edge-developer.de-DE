---
description: Initialisiert die übergebene `VARIANT` als Projektion eines JavaScript-Werts.
title: JsValueToVariant-Funktion | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsValueToVariant
helpviewer_keywords:
- JsValueToVariant function
ms.assetid: 070244be-a69d-4b78-971b-69c0579c03cf
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: f383f2d8bc3aab70b4a361b370698cd71cb714d3
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233902"
---
# <span data-ttu-id="b6221-103">JsValueToVariant Funktion</span><span class="sxs-lookup"><span data-stu-id="b6221-103">JsValueToVariant Function</span></span>

<span data-ttu-id="b6221-104">Initialisiert die übergebene `VARIANT` als Projektion eines JavaScript-Werts.</span><span class="sxs-lookup"><span data-stu-id="b6221-104">Initializes the passed in `VARIANT` as a projection of a JavaScript value.</span></span>  
  
## <span data-ttu-id="b6221-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b6221-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsValueToVariant(  
   _In_ JsValueRef object,  
   _Out_ VARIANT *variant  
);  
```  
  
#### <span data-ttu-id="b6221-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="b6221-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="b6221-107">Ein JavaScript-Wert für Project als `VARIANT` .</span><span class="sxs-lookup"><span data-stu-id="b6221-107">A JavaScript value to project as a `VARIANT`.</span></span>  
  
 `variant`  
 <span data-ttu-id="b6221-108">Ein Zeiger auf eine `VARIANT` Struktur, die als Projektion initialisiert wird.</span><span class="sxs-lookup"><span data-stu-id="b6221-108">A pointer to a `VARIANT` struct that will be initialized as a projection.</span></span>  
  
## <span data-ttu-id="b6221-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b6221-109">Return Value</span></span>  
  
## <span data-ttu-id="b6221-110">Hinweise</span><span class="sxs-lookup"><span data-stu-id="b6221-110">Remarks</span></span>  
 <span data-ttu-id="b6221-111">Die Projektion `VARIANT` kann von com-Automatisierungsclients verwendet werden, um das projizierte JavaScript-Objekt aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="b6221-111">The projection `VARIANT` can be used by COM automation clients to call into the projected JavaScript object.</span></span>  
  
 <span data-ttu-id="b6221-112">Erfordert einen aktiven Skriptkontext.</span><span class="sxs-lookup"><span data-stu-id="b6221-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="b6221-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b6221-113">Requirements</span></span>  
 <span data-ttu-id="b6221-114">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="b6221-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="b6221-115">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="b6221-115">See Also</span></span>  
 [<span data-ttu-id="b6221-116">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="b6221-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
