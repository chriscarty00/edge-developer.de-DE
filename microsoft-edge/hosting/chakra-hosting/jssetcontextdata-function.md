---
description: Legt die internen Daten von JsrtContext fest.
title: JsSetContextData-Funktion | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: be90aa6a-b001-4a6f-90c5-c2135e913be0
caps.latest.revision: 4
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 00521bafdaf6125dd15746de8a1d403eaf03b4a0
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10568318"
---
# <span data-ttu-id="dd843-103">JsSetContextData-Funktion</span><span class="sxs-lookup"><span data-stu-id="dd843-103">JsSetContextData Function</span></span>
<span data-ttu-id="dd843-104">Legt die internen Daten von JsrtContext fest.</span><span class="sxs-lookup"><span data-stu-id="dd843-104">Sets the internal data of JsrtContext.</span></span>  
  
## <span data-ttu-id="dd843-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="dd843-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsSetContextData(  
  _In_ JsContextRef context,  
  _In_ void *data  
);  
  
```  
  
#### <span data-ttu-id="dd843-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="dd843-106">Parameters</span></span>  
 `context`  
 <span data-ttu-id="dd843-107">Der Kontext, auf den die Daten gesetzt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="dd843-107">The context to set the data to.</span></span>  
  
 `data`  
 <span data-ttu-id="dd843-108">Der Zeiger auf die Daten, die gesetzt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="dd843-108">The pointer to the data to be set.</span></span>  
  
## <span data-ttu-id="dd843-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="dd843-109">Return Value</span></span>  
 <span data-ttu-id="dd843-110">Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="dd843-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="dd843-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="dd843-111">Remarks</span></span>  
 <span data-ttu-id="dd843-112">Erfordert einen aktiven Skriptkontext.</span><span class="sxs-lookup"><span data-stu-id="dd843-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="dd843-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="dd843-113">Requirements</span></span>  
 <span data-ttu-id="dd843-114">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="dd843-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="dd843-115">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="dd843-115">See Also</span></span>  
 [<span data-ttu-id="dd843-116">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="dd843-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)