---
description: Ruft den aktuellen Skriptkontext im Thread ab.
title: JsGetCurrentContext-Funktion | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsGetCurrentContext
helpviewer_keywords:
- JsGetCurrentContext function
ms.assetid: dd5fe0fa-d1e5-4af6-809e-e655a27519b5
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 78f04674aab8783c43f22516903669e0f9b7543b
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10567262"
---
# <span data-ttu-id="af643-103">JsGetCurrentContext-Funktion</span><span class="sxs-lookup"><span data-stu-id="af643-103">JsGetCurrentContext Function</span></span>
<span data-ttu-id="af643-104">Ruft den aktuellen Skriptkontext im Thread ab.</span><span class="sxs-lookup"><span data-stu-id="af643-104">Gets the current script context on the thread.</span></span>  
  
## <span data-ttu-id="af643-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="af643-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetCurrentContext(  
   _Out_ JsContextRef *currentContext  
);  
```  
  
#### <span data-ttu-id="af643-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="af643-106">Parameters</span></span>  
 `currentContext`  
 <span data-ttu-id="af643-107">Der aktuelle Skriptkontext im Thread, NULL, wenn kein aktueller Skriptkontext vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="af643-107">The current script context on the thread, null if there is no current script context.</span></span>  
  
## <span data-ttu-id="af643-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="af643-108">Return Value</span></span>  
 <span data-ttu-id="af643-109">Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="af643-109">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="af643-110">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="af643-110">Requirements</span></span>  
 <span data-ttu-id="af643-111">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="af643-111">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="af643-112">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="af643-112">See Also</span></span>  
 [<span data-ttu-id="af643-113">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="af643-113">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)