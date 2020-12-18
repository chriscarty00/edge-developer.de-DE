---
description: Ein Handle für eine Chakra-Laufzeit.
title: JsRuntimeHandle typedef | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 69e59bfd-9b0e-4710-9aa8-fbd6844171bc
caps.latest.revision: 6
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: ab08243505b9699fe07ca2e80f7294adf9eb78ad
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233735"
---
# <span data-ttu-id="86100-103">JsRuntimeHandle Typedef</span><span class="sxs-lookup"><span data-stu-id="86100-103">JsRuntimeHandle Typedef</span></span>

<span data-ttu-id="86100-104">Ein Handle für eine Chakra-Laufzeit.</span><span class="sxs-lookup"><span data-stu-id="86100-104">A handle to a Chakra runtime.</span></span>  
  
## <span data-ttu-id="86100-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="86100-105">Syntax</span></span>  
  
```cpp  
typedef void *JsRuntimeHandle;  
```  
  
## <span data-ttu-id="86100-106">Hinweise</span><span class="sxs-lookup"><span data-stu-id="86100-106">Remarks</span></span>  
 <span data-ttu-id="86100-107">Jede Chakra-Laufzeit verfügt über ein eigenes unabhängiges Ausführungsmodul, einen JIT-Compiler und einen Garbage Collector-Heap.</span><span class="sxs-lookup"><span data-stu-id="86100-107">Each Chakra runtime has its own independent execution engine, JIT compiler, and garbage collected heap.</span></span> <span data-ttu-id="86100-108">Daher ist jede Laufzeit vollständig von anderen Laufzeiten isoliert.</span><span class="sxs-lookup"><span data-stu-id="86100-108">As such, each runtime is completely isolated from other runtimes.</span></span>  
  
 <span data-ttu-id="86100-109">Runtimes können für jeden Thread verwendet werden, aber nur ein Thread kann zu einem beliebigen Zeitpunkt eine Laufzeit aufrufen.</span><span class="sxs-lookup"><span data-stu-id="86100-109">Runtimes can be used on any thread, but only one thread can call into a runtime at any time.</span></span>  
  
> [!WARNING]
>  <span data-ttu-id="86100-110">Eine JsRuntimeHandle ist im Gegensatz zu anderen Objekt verweisen in der Chakra-Hosting-API keine Garbage Collection, da Sie den Garbage Collection-Heap selbst enthält.</span><span class="sxs-lookup"><span data-stu-id="86100-110">A JsRuntimeHandle, unlike other object references in the Chakra hosting API, is not garbage collected since it contains the garbage collected heap itself.</span></span> <span data-ttu-id="86100-111">Eine Common Language Runtime wird weiterhin vorhanden sein, bis JsDisposeRuntime aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="86100-111">A runtime will continue to exist until JsDisposeRuntime is called.</span></span>  
  
## <span data-ttu-id="86100-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="86100-112">Requirements</span></span>  
 <span data-ttu-id="86100-113">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="86100-113">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="86100-114">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="86100-114">See Also</span></span>  
 [<span data-ttu-id="86100-115">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="86100-115">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
