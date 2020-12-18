---
description: Der JsRT-Rückruf, der aufgerufen werden soll, wobei der Kontext an `JsProjectionEnqueueCallback` den richtigen Thread übergeben wird.
title: JsProjectionCallback typedef | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 32f22d37-e57e-4196-b6cd-a3fc75bd0632
caps.latest.revision: 3
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 211325b536dc84340974b02973f1de9d5749a60a
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11234079"
---
# <span data-ttu-id="390f0-103">JsProjectionCallback Typedef</span><span class="sxs-lookup"><span data-stu-id="390f0-103">JsProjectionCallback Typedef</span></span>

<span data-ttu-id="390f0-104">Der JsRT-Rückruf, der aufgerufen werden soll, wobei der Kontext an `JsProjectionEnqueueCallback` den richtigen Thread übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="390f0-104">The JsRT callback which should be called with the context passed to `JsProjectionEnqueueCallback` on the correct thread.</span></span>  
  
## <span data-ttu-id="390f0-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="390f0-105">Syntax</span></span>  
  
```cpp  
typedef void (CALLBACK *JsProjectionCallback)(  
  _In_ JsProjectionCallbackContext jsContext  
);  
```  
  
#### <span data-ttu-id="390f0-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="390f0-106">Parameters</span></span>  
 `jsContext`  
 <span data-ttu-id="390f0-107">Erfordert Anrufe `JsSetProjectionEnqueueCallback` , um Rückrufe zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="390f0-107">Requires calling `JsSetProjectionEnqueueCallback` to receive callbacks.</span></span>  
  
## <span data-ttu-id="390f0-108">Hinweise</span><span class="sxs-lookup"><span data-stu-id="390f0-108">Remarks</span></span>  
 <span data-ttu-id="390f0-109">Diese API wird nur im EdgeHTML-Modus unterstützt.</span><span class="sxs-lookup"><span data-stu-id="390f0-109">This API is supported only in EdgeHTML mode.</span></span>  
  
## <span data-ttu-id="390f0-110">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="390f0-110">Requirements</span></span>  
 <span data-ttu-id="390f0-111">jsrt. h</span><span class="sxs-lookup"><span data-stu-id="390f0-111">jsrt.h</span></span>  
  
## <span data-ttu-id="390f0-112">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="390f0-112">See Also</span></span>  
 [<span data-ttu-id="390f0-113">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="390f0-113">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
