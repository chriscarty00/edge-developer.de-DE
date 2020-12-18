---
description: Ruft den aktuellen Skriptkontext im Thread ab.
title: JsGetCurrentContext-Funktion | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsGetCurrentContext
helpviewer_keywords:
- JsGetCurrentContext function
ms.assetid: dd5fe0fa-d1e5-4af6-809e-e655a27519b5
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: a43b9a6d4413ef1dc1b66321d6078aef84a0645f
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11234002"
---
# <span data-ttu-id="18a1f-103">JsGetCurrentContext Funktion</span><span class="sxs-lookup"><span data-stu-id="18a1f-103">JsGetCurrentContext Function</span></span>

<span data-ttu-id="18a1f-104">Ruft den aktuellen Skriptkontext im Thread ab.</span><span class="sxs-lookup"><span data-stu-id="18a1f-104">Gets the current script context on the thread.</span></span>  
  
## <span data-ttu-id="18a1f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="18a1f-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetCurrentContext(  
   _Out_ JsContextRef *currentContext  
);  
```  
  
#### <span data-ttu-id="18a1f-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="18a1f-106">Parameters</span></span>  
 `currentContext`  
 <span data-ttu-id="18a1f-107">Der aktuelle Skriptkontext im Thread, NULL, wenn kein aktueller Skriptkontext vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="18a1f-107">The current script context on the thread, null if there is no current script context.</span></span>  
  
## <span data-ttu-id="18a1f-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="18a1f-108">Return Value</span></span>  
 <span data-ttu-id="18a1f-109">Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="18a1f-109">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="18a1f-110">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="18a1f-110">Requirements</span></span>  
 <span data-ttu-id="18a1f-111">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="18a1f-111">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="18a1f-112">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="18a1f-112">See Also</span></span>  
 [<span data-ttu-id="18a1f-113">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="18a1f-113">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
