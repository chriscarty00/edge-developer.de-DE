---
description: Legt die internen Daten von JsrtContext fest.
title: JsSetContextData-Funktion | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: be90aa6a-b001-4a6f-90c5-c2135e913be0
caps.latest.revision: 4
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: e874f500ca82328dddeaaa03a0b78a188b8fd241
ms.sourcegitcommit: 037a2d62333691104c9accb4862968f80a3465a2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/18/2020
ms.locfileid: "10751933"
---
# <span data-ttu-id="5853e-103">JsSetContextData Funktion</span><span class="sxs-lookup"><span data-stu-id="5853e-103">JsSetContextData Function</span></span>
<span data-ttu-id="5853e-104">Legt die internen Daten von JsrtContext fest.</span><span class="sxs-lookup"><span data-stu-id="5853e-104">Sets the internal data of JsrtContext.</span></span>  
  
## <span data-ttu-id="5853e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="5853e-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsSetContextData(  
  _In_ JsContextRef context,  
  _In_ void *data  
);  
  
```  
  
#### <span data-ttu-id="5853e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="5853e-106">Parameters</span></span>  
 `context`  
 <span data-ttu-id="5853e-107">Der Kontext, auf den die Daten gesetzt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="5853e-107">The context to set the data to.</span></span>  
  
 `data`  
 <span data-ttu-id="5853e-108">Der Zeiger auf die Daten, die gesetzt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="5853e-108">The pointer to the data to be set.</span></span>  
  
## <span data-ttu-id="5853e-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5853e-109">Return Value</span></span>  
 <span data-ttu-id="5853e-110">Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="5853e-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="5853e-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="5853e-111">Remarks</span></span>  
 <span data-ttu-id="5853e-112">Erfordert einen aktiven Skriptkontext.</span><span class="sxs-lookup"><span data-stu-id="5853e-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="5853e-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5853e-113">Requirements</span></span>  
 <span data-ttu-id="5853e-114">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="5853e-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="5853e-115">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="5853e-115">See Also</span></span>  
 [<span data-ttu-id="5853e-116">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="5853e-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)