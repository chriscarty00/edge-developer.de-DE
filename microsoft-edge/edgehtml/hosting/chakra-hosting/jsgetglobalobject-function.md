---
description: Ruft das globale Objekt im aktuellen Skriptkontext ab.
title: JsGetGlobalObject-Funktion | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsGetGlobalObject
helpviewer_keywords:
- JsGetGlobalObject function
ms.assetid: d3e91e64-1ca3-4d2b-aada-725ded0fd0b1
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: cda960710180c135b99abd359d0cc76776ff0225
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233994"
---
# <span data-ttu-id="e83d7-103">JsGetGlobalObject Funktion</span><span class="sxs-lookup"><span data-stu-id="e83d7-103">JsGetGlobalObject Function</span></span>

<span data-ttu-id="e83d7-104">Ruft das globale Objekt im aktuellen Skriptkontext ab.</span><span class="sxs-lookup"><span data-stu-id="e83d7-104">Gets the global object in the current script context.</span></span>  
  
## <span data-ttu-id="e83d7-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e83d7-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetGlobalObject(  
   _Out_ JsValueRef *globalObject  
);  
```  
  
#### <span data-ttu-id="e83d7-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="e83d7-106">Parameters</span></span>  
 `globalObject`  
 <span data-ttu-id="e83d7-107">Das globale Objekt.</span><span class="sxs-lookup"><span data-stu-id="e83d7-107">The global object.</span></span>  
  
## <span data-ttu-id="e83d7-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e83d7-108">Return Value</span></span>  
 <span data-ttu-id="e83d7-109">Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="e83d7-109">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="e83d7-110">Hinweise</span><span class="sxs-lookup"><span data-stu-id="e83d7-110">Remarks</span></span>  
 <span data-ttu-id="e83d7-111">Erfordert einen aktiven Skriptkontext.</span><span class="sxs-lookup"><span data-stu-id="e83d7-111">Requires an active script context.</span></span>  
  
## <span data-ttu-id="e83d7-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e83d7-112">Requirements</span></span>  
 <span data-ttu-id="e83d7-113">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="e83d7-113">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="e83d7-114">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="e83d7-114">See Also</span></span>  
 [<span data-ttu-id="e83d7-115">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="e83d7-115">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
