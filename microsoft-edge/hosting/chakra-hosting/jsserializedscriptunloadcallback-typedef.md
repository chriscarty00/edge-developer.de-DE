---
description: Wird von der Common Language Runtime aufgerufen, wenn alle Ressourcen im Zusammenhang mit der Skriptausführung fertig sind. Der Aufrufer sollte die Quelle beim Laden, dem Bytecode und dem Kontext zu diesem Zeitpunkt freigeben.
title: JsSerializedScriptUnloadCallback typedef | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 8d18c392-cca0-411e-9f2b-0d788b16161a
caps.latest.revision: 3
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: c3da27af18ebc7a1913980a865d926bac6a29d11
ms.sourcegitcommit: 037a2d62333691104c9accb4862968f80a3465a2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/18/2020
ms.locfileid: "10751940"
---
# <span data-ttu-id="50c01-104">JsSerializedScriptUnloadCallback typedef</span><span class="sxs-lookup"><span data-stu-id="50c01-104">JsSerializedScriptUnloadCallback typedef</span></span>
<span data-ttu-id="50c01-105">Wird von der Common Language Runtime aufgerufen, wenn alle Ressourcen im Zusammenhang mit der Skriptausführung fertig sind.</span><span class="sxs-lookup"><span data-stu-id="50c01-105">Called by the runtime when it is finished with all resources related to the script execution.</span></span> <span data-ttu-id="50c01-106">Der Aufrufer sollte die Quelle beim Laden, dem Bytecode und dem Kontext zu diesem Zeitpunkt freigeben.</span><span class="sxs-lookup"><span data-stu-id="50c01-106">The caller should free the source if loaded, the byte code, and the context at this time.</span></span>  
  
## <span data-ttu-id="50c01-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="50c01-107">Syntax</span></span>  
  
```cpp  
 typedef void (CALLBACK * JsSerializedScriptUnloadCallback)(  
  _In_ JsSourceContext sourceContext  
);  
```  
  
#### <span data-ttu-id="50c01-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="50c01-108">Parameters</span></span>  
 `sourceContext`  
 <span data-ttu-id="50c01-109">Der Kontext, der an oder übergeben wurde `JsParseSerializedScriptWithCallback` `JsRunSerializedScriptWithCallback` .</span><span class="sxs-lookup"><span data-stu-id="50c01-109">The context passed to `JsParseSerializedScriptWithCallback` or `JsRunSerializedScriptWithCallback`.</span></span>  
  
## <span data-ttu-id="50c01-110">Hinweise</span><span class="sxs-lookup"><span data-stu-id="50c01-110">Remarks</span></span>  
  
> [!WARNING]
## <span data-ttu-id="50c01-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="50c01-111">Requirements</span></span>  
 <span data-ttu-id="50c01-112">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="50c01-112">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="50c01-113">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="50c01-113">See Also</span></span>  
 [<span data-ttu-id="50c01-114">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="50c01-114">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)