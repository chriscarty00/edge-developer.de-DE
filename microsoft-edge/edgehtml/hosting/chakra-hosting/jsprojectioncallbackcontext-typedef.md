---
description: Der Kontext, der an Application Callback, JsProjectionEnqueueCallback, von JsRT übergeben und dann zurück an JsRT im bereitgestellten Rückruf, `JsProjectionCallback` von der Anwendung im richtigen Thread übergeben wurde.
title: JsProjectionCallbackContext typedef | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 50c705c5-664f-4a1a-92f6-4882fc718ab1
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 7742b0186a49e99f2738b81357b9e55cfe00042b
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11234075"
---
# <span data-ttu-id="da0ab-103">JsProjectionCallbackContext Typedef</span><span class="sxs-lookup"><span data-stu-id="da0ab-103">JsProjectionCallbackContext Typedef</span></span>

<span data-ttu-id="da0ab-104">Der Kontext, der an Application Callback, JsProjectionEnqueueCallback, von JsRT übergeben und dann zurück an JsRT im bereitgestellten Rückruf, `JsProjectionCallback` von der Anwendung im richtigen Thread übergeben wurde.</span><span class="sxs-lookup"><span data-stu-id="da0ab-104">The context passed into application callback, JsProjectionEnqueueCallback, from JsRT and then passed back to JsRT in the provided callback, `JsProjectionCallback`, by the application on the correct thread.</span></span>  
  
## <span data-ttu-id="da0ab-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="da0ab-105">Syntax</span></span>  
  
```cpp  
typedef void *JsProjectionCallbackContext;  
```  
  
## <span data-ttu-id="da0ab-106">Hinweise</span><span class="sxs-lookup"><span data-stu-id="da0ab-106">Remarks</span></span>  
 <span data-ttu-id="da0ab-107">Erfordert Anrufe `JsSetProjectionEnqueueCallback` , um Rückrufe zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="da0ab-107">Requires calling `JsSetProjectionEnqueueCallback` to receive callbacks.</span></span>  
  
 <span data-ttu-id="da0ab-108">Diese API wird nur im EdgeHTML-Modus unterstützt.</span><span class="sxs-lookup"><span data-stu-id="da0ab-108">This API is supported only in EdgeHTML mode.</span></span>  
  
## <span data-ttu-id="da0ab-109">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="da0ab-109">Requirements</span></span>  
 <span data-ttu-id="da0ab-110">jsrt. h</span><span class="sxs-lookup"><span data-stu-id="da0ab-110">jsrt.h</span></span>  
  
## <span data-ttu-id="da0ab-111">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="da0ab-111">See Also</span></span>  
 [<span data-ttu-id="da0ab-112">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="da0ab-112">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
