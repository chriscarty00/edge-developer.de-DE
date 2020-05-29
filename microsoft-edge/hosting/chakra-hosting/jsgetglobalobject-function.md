---
description: Ruft das globale Objekt im aktuellen Skriptkontext ab.
title: JsGetGlobalObject-Funktion | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsGetGlobalObject
helpviewer_keywords:
- JsGetGlobalObject function
ms.assetid: d3e91e64-1ca3-4d2b-aada-725ded0fd0b1
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 9f8b540485e75ef80d42ba66f031b3e827b475fa
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10567254"
---
# <span data-ttu-id="642f1-103">JsGetGlobalObject-Funktion</span><span class="sxs-lookup"><span data-stu-id="642f1-103">JsGetGlobalObject Function</span></span>
<span data-ttu-id="642f1-104">Ruft das globale Objekt im aktuellen Skriptkontext ab.</span><span class="sxs-lookup"><span data-stu-id="642f1-104">Gets the global object in the current script context.</span></span>  
  
## <span data-ttu-id="642f1-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="642f1-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetGlobalObject(  
   _Out_ JsValueRef *globalObject  
);  
```  
  
#### <span data-ttu-id="642f1-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="642f1-106">Parameters</span></span>  
 `globalObject`  
 <span data-ttu-id="642f1-107">Das globale Objekt.</span><span class="sxs-lookup"><span data-stu-id="642f1-107">The global object.</span></span>  
  
## <span data-ttu-id="642f1-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="642f1-108">Return Value</span></span>  
 <span data-ttu-id="642f1-109">Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="642f1-109">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="642f1-110">Hinweise</span><span class="sxs-lookup"><span data-stu-id="642f1-110">Remarks</span></span>  
 <span data-ttu-id="642f1-111">Erfordert einen aktiven Skriptkontext.</span><span class="sxs-lookup"><span data-stu-id="642f1-111">Requires an active script context.</span></span>  
  
## <span data-ttu-id="642f1-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="642f1-112">Requirements</span></span>  
 <span data-ttu-id="642f1-113">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="642f1-113">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="642f1-114">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="642f1-114">See Also</span></span>  
 [<span data-ttu-id="642f1-115">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="642f1-115">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)