---
description: Der Anwendungsrückruf, der von JsRT aufgerufen wird, wenn eine Projektions-API in einem anderen Thread als das Original abgeschlossen ist.
title: JsProjectionEnqueueCallback typedef | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 19c1cefb-a7be-4196-b780-9fe6adf35ba5
caps.latest.revision: 4
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 47527d5e32076e40a82ab5452c2e0f624e8a2818
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11234314"
---
# <span data-ttu-id="45907-103">JsProjectionEnqueueCallback Typedef</span><span class="sxs-lookup"><span data-stu-id="45907-103">JsProjectionEnqueueCallback Typedef</span></span>

<span data-ttu-id="45907-104">Der Anwendungsrückruf, der von JsRT aufgerufen wird, wenn eine Projektions-API in einem anderen Thread als das Original abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="45907-104">The application callback which is called by JsRT when a projection API is completed on a different thread than the original.</span></span>  
  
## <span data-ttu-id="45907-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="45907-105">Syntax</span></span>  
  
```cpp  
typedef void (CALLBACK *JsProjectionEnqueueCallback)(  
  _In_ JsProjectionCallback jsCallback,  
  _In_ JsProjectionCallbackContext jsContext,  
  _In_opt_ void *callbackState  
);  
```  
  
#### <span data-ttu-id="45907-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="45907-106">Parameters</span></span>  
 `jsCallback`  
 <span data-ttu-id="45907-107">Der Rückruf, der für den ursprünglichen Thread aufgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="45907-107">The callback to be invoked on the original thread.</span></span>  
  
 `jsContext`  
 <span data-ttu-id="45907-108">Der Anwendungskontext.</span><span class="sxs-lookup"><span data-stu-id="45907-108">The applications context.</span></span>  
  
 `callbackState`  
 <span data-ttu-id="45907-109">Der JsRT-Kontext, an den übergeben werden muss `jsCallback` .</span><span class="sxs-lookup"><span data-stu-id="45907-109">The JsRT context that must be passed into `jsCallback`.</span></span>  
  
## <span data-ttu-id="45907-110">Hinweise</span><span class="sxs-lookup"><span data-stu-id="45907-110">Remarks</span></span>  
 <span data-ttu-id="45907-111">Erfordert das Aufrufen von JsSetProjectionEnqueueCallback, um Rückrufe zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="45907-111">Requires calling JsSetProjectionEnqueueCallback to receive callbacks.</span></span>  
  
 <span data-ttu-id="45907-112">Diese API wird nur im EdgeHTML-Modus unterstützt.</span><span class="sxs-lookup"><span data-stu-id="45907-112">This API is supported only in EdgeHTML mode.</span></span>  
  
## <span data-ttu-id="45907-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="45907-113">Requirements</span></span>  
 <span data-ttu-id="45907-114">jsrt. h</span><span class="sxs-lookup"><span data-stu-id="45907-114">jsrt.h</span></span>  
  
## <span data-ttu-id="45907-115">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="45907-115">See Also</span></span>  
 [<span data-ttu-id="45907-116">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="45907-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
