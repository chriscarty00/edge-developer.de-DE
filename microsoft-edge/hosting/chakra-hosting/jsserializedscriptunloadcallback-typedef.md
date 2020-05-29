---
description: Wird von der Common Language Runtime aufgerufen, wenn alle Ressourcen im Zusammenhang mit der Skriptausführung fertig sind. Der Aufrufer sollte die Quelle beim Laden, dem Bytecode und dem Kontext zu diesem Zeitpunkt freigeben.
title: JsSerializedScriptUnloadCallback typedef | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: 8d18c392-cca0-411e-9f2b-0d788b16161a
caps.latest.revision: 3
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 9555b3fd8c14c9629d17c13592e3c78a78be150e
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10568321"
---
# <span data-ttu-id="e4f07-104">JsSerializedScriptUnloadCallback typedef</span><span class="sxs-lookup"><span data-stu-id="e4f07-104">JsSerializedScriptUnloadCallback typedef</span></span>
<span data-ttu-id="e4f07-105">Wird von der Common Language Runtime aufgerufen, wenn alle Ressourcen im Zusammenhang mit der Skriptausführung fertig sind.</span><span class="sxs-lookup"><span data-stu-id="e4f07-105">Called by the runtime when it is finished with all resources related to the script execution.</span></span> <span data-ttu-id="e4f07-106">Der Aufrufer sollte die Quelle beim Laden, dem Bytecode und dem Kontext zu diesem Zeitpunkt freigeben.</span><span class="sxs-lookup"><span data-stu-id="e4f07-106">The caller should free the source if loaded, the byte code, and the context at this time.</span></span>  
  
## <span data-ttu-id="e4f07-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="e4f07-107">Syntax</span></span>  
  
```cpp  
 typedef void (CALLBACK * JsSerializedScriptUnloadCallback)(  
  _In_ JsSourceContext sourceContext  
);  
```  
  
#### <span data-ttu-id="e4f07-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="e4f07-108">Parameters</span></span>  
 `sourceContext`  
 <span data-ttu-id="e4f07-109">Der Kontext, der an oder übergeben wurde `JsParseSerializedScriptWithCallback` `JsRunSerializedScriptWithCallback` .</span><span class="sxs-lookup"><span data-stu-id="e4f07-109">The context passed to `JsParseSerializedScriptWithCallback` or `JsRunSerializedScriptWithCallback`.</span></span>  
  
## <span data-ttu-id="e4f07-110">Hinweise</span><span class="sxs-lookup"><span data-stu-id="e4f07-110">Remarks</span></span>  
  
> [!WARNING]
## <span data-ttu-id="e4f07-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e4f07-111">Requirements</span></span>  
 <span data-ttu-id="e4f07-112">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="e4f07-112">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="e4f07-113">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="e4f07-113">See Also</span></span>  
 [<span data-ttu-id="e4f07-114">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="e4f07-114">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)