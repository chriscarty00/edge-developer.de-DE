---
description: Macht ein Objekt nicht erweiterbar.
title: JsPreventExtension-Funktion | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsPreventExtension
helpviewer_keywords:
- JsPreventExtension function
ms.assetid: 8da07e20-d076-4ae4-9fb0-3f3c141518c2
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 1904756a932bd581e05ec474004af7107da3f64b
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11234080"
---
# <span data-ttu-id="9776e-103">JsPreventExtension Funktion</span><span class="sxs-lookup"><span data-stu-id="9776e-103">JsPreventExtension Function</span></span>

<span data-ttu-id="9776e-104">Macht ein Objekt nicht erweiterbar.</span><span class="sxs-lookup"><span data-stu-id="9776e-104">Makes an object non-extensible.</span></span>  
  
## <span data-ttu-id="9776e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="9776e-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsPreventExtension(  
   _In_ JsValueRef object  
);  
```  
  
#### <span data-ttu-id="9776e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="9776e-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="9776e-107">Das Objekt, das nicht erweiterbar sein soll.</span><span class="sxs-lookup"><span data-stu-id="9776e-107">The object to make non-extensible.</span></span>  
  
## <span data-ttu-id="9776e-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9776e-108">Return Value</span></span>  
 <span data-ttu-id="9776e-109">Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="9776e-109">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="9776e-110">Hinweise</span><span class="sxs-lookup"><span data-stu-id="9776e-110">Remarks</span></span>  
 <span data-ttu-id="9776e-111">Erfordert einen aktiven Skriptkontext.</span><span class="sxs-lookup"><span data-stu-id="9776e-111">Requires an active script context.</span></span>  
  
## <span data-ttu-id="9776e-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9776e-112">Requirements</span></span>  
 <span data-ttu-id="9776e-113">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="9776e-113">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="9776e-114">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="9776e-114">See Also</span></span>  
 [<span data-ttu-id="9776e-115">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="9776e-115">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
