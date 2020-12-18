---
description: Wird von der Common Language Runtime aufgerufen, wenn alle Ressourcen im Zusammenhang mit der Skriptausführung fertig sind. Der Aufrufer sollte die Quelle beim Laden, dem Bytecode und dem Kontext zu diesem Zeitpunkt freigeben.
title: JsSerializedScriptUnloadCallback typedef | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 8d18c392-cca0-411e-9f2b-0d788b16161a
caps.latest.revision: 3
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 5c63f2ff3faf21a19e31f2f6fd1692e21d59fc0b
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11234261"
---
# <span data-ttu-id="f17d1-104">JsSerializedScriptUnloadCallback typedef</span><span class="sxs-lookup"><span data-stu-id="f17d1-104">JsSerializedScriptUnloadCallback typedef</span></span>

<span data-ttu-id="f17d1-105">Wird von der Common Language Runtime aufgerufen, wenn alle Ressourcen im Zusammenhang mit der Skriptausführung fertig sind.</span><span class="sxs-lookup"><span data-stu-id="f17d1-105">Called by the runtime when it is finished with all resources related to the script execution.</span></span> <span data-ttu-id="f17d1-106">Der Aufrufer sollte die Quelle beim Laden, dem Bytecode und dem Kontext zu diesem Zeitpunkt freigeben.</span><span class="sxs-lookup"><span data-stu-id="f17d1-106">The caller should free the source if loaded, the byte code, and the context at this time.</span></span>  
  
## <span data-ttu-id="f17d1-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="f17d1-107">Syntax</span></span>  
  
```cpp  
 typedef void (CALLBACK * JsSerializedScriptUnloadCallback)(  
  _In_ JsSourceContext sourceContext  
);  
```  
  
#### <span data-ttu-id="f17d1-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="f17d1-108">Parameters</span></span>  
 `sourceContext`  
 <span data-ttu-id="f17d1-109">Der Kontext, der an oder übergeben wurde `JsParseSerializedScriptWithCallback` `JsRunSerializedScriptWithCallback` .</span><span class="sxs-lookup"><span data-stu-id="f17d1-109">The context passed to `JsParseSerializedScriptWithCallback` or `JsRunSerializedScriptWithCallback`.</span></span>  
  
## <span data-ttu-id="f17d1-110">Hinweise</span><span class="sxs-lookup"><span data-stu-id="f17d1-110">Remarks</span></span>  
  
> [!WARNING]
## <span data-ttu-id="f17d1-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f17d1-111">Requirements</span></span>  
 <span data-ttu-id="f17d1-112">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="f17d1-112">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="f17d1-113">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="f17d1-113">See Also</span></span>  
 [<span data-ttu-id="f17d1-114">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="f17d1-114">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
