---
description: Der Kontext, der an Application Callback, JsProjectionEnqueueCallback, von JsRT übergeben und dann zurück an JsRT im bereitgestellten Rückruf, `JsProjectionCallback` von der Anwendung im richtigen Thread übergeben wurde.
title: JsProjectionCallbackContext typedef | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 50c705c5-664f-4a1a-92f6-4882fc718ab1
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 58d4c74da13ae0dd269f3c101bbf3d2b95e77732
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10567212"
---
# <span data-ttu-id="553e9-103">JsProjectionCallbackContext typedef</span><span class="sxs-lookup"><span data-stu-id="553e9-103">JsProjectionCallbackContext Typedef</span></span>
<span data-ttu-id="553e9-104">Der Kontext, der an Application Callback, JsProjectionEnqueueCallback, von JsRT übergeben und dann zurück an JsRT im bereitgestellten Rückruf, `JsProjectionCallback` von der Anwendung im richtigen Thread übergeben wurde.</span><span class="sxs-lookup"><span data-stu-id="553e9-104">The context passed into application callback, JsProjectionEnqueueCallback, from JsRT and then passed back to JsRT in the provided callback, `JsProjectionCallback`, by the application on the correct thread.</span></span>  
  
## <span data-ttu-id="553e9-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="553e9-105">Syntax</span></span>  
  
```cpp  
typedef void *JsProjectionCallbackContext;  
```  
  
## <span data-ttu-id="553e9-106">Hinweise</span><span class="sxs-lookup"><span data-stu-id="553e9-106">Remarks</span></span>  
 <span data-ttu-id="553e9-107">Erfordert Anrufe `JsSetProjectionEnqueueCallback` , um Rückrufe zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="553e9-107">Requires calling `JsSetProjectionEnqueueCallback` to receive callbacks.</span></span>  
  
 <span data-ttu-id="553e9-108">Diese API wird nur im EdgeHTML-Modus unterstützt.</span><span class="sxs-lookup"><span data-stu-id="553e9-108">This API is supported only in EdgeHTML mode.</span></span>  
  
## <span data-ttu-id="553e9-109">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="553e9-109">Requirements</span></span>  
 <span data-ttu-id="553e9-110">jsrt. h</span><span class="sxs-lookup"><span data-stu-id="553e9-110">jsrt.h</span></span>  
  
## <span data-ttu-id="553e9-111">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="553e9-111">See Also</span></span>  
 [<span data-ttu-id="553e9-112">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="553e9-112">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)