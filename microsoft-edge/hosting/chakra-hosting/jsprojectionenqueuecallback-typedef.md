---
description: Der Anwendungsrückruf, der von JsRT aufgerufen wird, wenn eine Projektions-API in einem anderen Thread als das Original abgeschlossen ist.
title: JsProjectionEnqueueCallback typedef | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 19c1cefb-a7be-4196-b780-9fe6adf35ba5
caps.latest.revision: 4
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 064a7d1077ae5222e44ab08ebe0592bb97b1f2af
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10567210"
---
# <span data-ttu-id="96c42-103">JsProjectionEnqueueCallback typedef</span><span class="sxs-lookup"><span data-stu-id="96c42-103">JsProjectionEnqueueCallback Typedef</span></span>
<span data-ttu-id="96c42-104">Der Anwendungsrückruf, der von JsRT aufgerufen wird, wenn eine Projektions-API in einem anderen Thread als das Original abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="96c42-104">The application callback which is called by JsRT when a projection API is completed on a different thread than the original.</span></span>  
  
## <span data-ttu-id="96c42-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="96c42-105">Syntax</span></span>  
  
```cpp  
typedef void (CALLBACK *JsProjectionEnqueueCallback)(  
  _In_ JsProjectionCallback jsCallback,  
  _In_ JsProjectionCallbackContext jsContext,  
  _In_opt_ void *callbackState  
);  
```  
  
#### <span data-ttu-id="96c42-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="96c42-106">Parameters</span></span>  
 `jsCallback`  
 <span data-ttu-id="96c42-107">Der Rückruf, der für den ursprünglichen Thread aufgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="96c42-107">The callback to be invoked on the original thread.</span></span>  
  
 `jsContext`  
 <span data-ttu-id="96c42-108">Der Anwendungskontext.</span><span class="sxs-lookup"><span data-stu-id="96c42-108">The applications context.</span></span>  
  
 `callbackState`  
 <span data-ttu-id="96c42-109">Der JsRT-Kontext, an den übergeben werden muss `jsCallback` .</span><span class="sxs-lookup"><span data-stu-id="96c42-109">The JsRT context that must be passed into `jsCallback`.</span></span>  
  
## <span data-ttu-id="96c42-110">Hinweise</span><span class="sxs-lookup"><span data-stu-id="96c42-110">Remarks</span></span>  
 <span data-ttu-id="96c42-111">Erfordert das Aufrufen von JsSetProjectionEnqueueCallback, um Rückrufe zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="96c42-111">Requires calling JsSetProjectionEnqueueCallback to receive callbacks.</span></span>  
  
 <span data-ttu-id="96c42-112">Diese API wird nur im EdgeHTML-Modus unterstützt.</span><span class="sxs-lookup"><span data-stu-id="96c42-112">This API is supported only in EdgeHTML mode.</span></span>  
  
## <span data-ttu-id="96c42-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="96c42-113">Requirements</span></span>  
 <span data-ttu-id="96c42-114">jsrt. h</span><span class="sxs-lookup"><span data-stu-id="96c42-114">jsrt.h</span></span>  
  
## <span data-ttu-id="96c42-115">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="96c42-115">See Also</span></span>  
 [<span data-ttu-id="96c42-116">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="96c42-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)