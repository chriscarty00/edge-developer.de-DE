---
description: Der JsRT-Rückruf, der aufgerufen werden soll, wobei der Kontext an `JsProjectionEnqueueCallback` den richtigen Thread übergeben wird.
title: JsProjectionCallback typedef | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 32f22d37-e57e-4196-b6cd-a3fc75bd0632
caps.latest.revision: 3
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: b30f9a7dc4671896eeacecbf58ef88f0383e9e7e
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10567211"
---
# <span data-ttu-id="e4a9e-103">JsProjectionCallback typedef</span><span class="sxs-lookup"><span data-stu-id="e4a9e-103">JsProjectionCallback Typedef</span></span>
<span data-ttu-id="e4a9e-104">Der JsRT-Rückruf, der aufgerufen werden soll, wobei der Kontext an `JsProjectionEnqueueCallback` den richtigen Thread übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="e4a9e-104">The JsRT callback which should be called with the context passed to `JsProjectionEnqueueCallback` on the correct thread.</span></span>  
  
## <span data-ttu-id="e4a9e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e4a9e-105">Syntax</span></span>  
  
```cpp  
typedef void (CALLBACK *JsProjectionCallback)(  
  _In_ JsProjectionCallbackContext jsContext  
);  
```  
  
#### <span data-ttu-id="e4a9e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="e4a9e-106">Parameters</span></span>  
 `jsContext`  
 <span data-ttu-id="e4a9e-107">Erfordert Anrufe `JsSetProjectionEnqueueCallback` , um Rückrufe zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="e4a9e-107">Requires calling `JsSetProjectionEnqueueCallback` to receive callbacks.</span></span>  
  
## <span data-ttu-id="e4a9e-108">Hinweise</span><span class="sxs-lookup"><span data-stu-id="e4a9e-108">Remarks</span></span>  
 <span data-ttu-id="e4a9e-109">Diese API wird nur im EdgeHTML-Modus unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e4a9e-109">This API is supported only in EdgeHTML mode.</span></span>  
  
## <span data-ttu-id="e4a9e-110">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e4a9e-110">Requirements</span></span>  
 <span data-ttu-id="e4a9e-111">jsrt. h</span><span class="sxs-lookup"><span data-stu-id="e4a9e-111">jsrt.h</span></span>  
  
## <span data-ttu-id="e4a9e-112">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="e4a9e-112">See Also</span></span>  
 [<span data-ttu-id="e4a9e-113">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="e4a9e-113">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)