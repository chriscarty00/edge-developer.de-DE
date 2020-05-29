---
description: Ein Handle für eine Chakra-Laufzeit.
title: JsRuntimeHandle typedef | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 69e59bfd-9b0e-4710-9aa8-fbd6844171bc
caps.latest.revision: 6
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 4ccdcf39ec6062db47e1b9de249d75c8804de405
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10568323"
---
# <span data-ttu-id="e1fce-103">JsRuntimeHandle typedef</span><span class="sxs-lookup"><span data-stu-id="e1fce-103">JsRuntimeHandle Typedef</span></span>
<span data-ttu-id="e1fce-104">Ein Handle für eine Chakra-Laufzeit.</span><span class="sxs-lookup"><span data-stu-id="e1fce-104">A handle to a Chakra runtime.</span></span>  
  
## <span data-ttu-id="e1fce-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e1fce-105">Syntax</span></span>  
  
```cpp  
typedef void *JsRuntimeHandle;  
```  
  
## <span data-ttu-id="e1fce-106">Hinweise</span><span class="sxs-lookup"><span data-stu-id="e1fce-106">Remarks</span></span>  
 <span data-ttu-id="e1fce-107">Jede Chakra-Laufzeit verfügt über ein eigenes unabhängiges Ausführungsmodul, einen JIT-Compiler und einen Garbage Collector-Heap.</span><span class="sxs-lookup"><span data-stu-id="e1fce-107">Each Chakra runtime has its own independent execution engine, JIT compiler, and garbage collected heap.</span></span> <span data-ttu-id="e1fce-108">Daher ist jede Laufzeit vollständig von anderen Laufzeiten isoliert.</span><span class="sxs-lookup"><span data-stu-id="e1fce-108">As such, each runtime is completely isolated from other runtimes.</span></span>  
  
 <span data-ttu-id="e1fce-109">Runtimes können für jeden Thread verwendet werden, aber nur ein Thread kann zu einem beliebigen Zeitpunkt eine Laufzeit aufrufen.</span><span class="sxs-lookup"><span data-stu-id="e1fce-109">Runtimes can be used on any thread, but only one thread can call into a runtime at any time.</span></span>  
  
> [!WARNING]
>  <span data-ttu-id="e1fce-110">Eine JsRuntimeHandle ist im Gegensatz zu anderen Objekt verweisen in der Chakra-Hosting-API keine Garbage Collection, da Sie den Garbage Collection-Heap selbst enthält.</span><span class="sxs-lookup"><span data-stu-id="e1fce-110">A JsRuntimeHandle, unlike other object references in the Chakra hosting API, is not garbage collected since it contains the garbage collected heap itself.</span></span> <span data-ttu-id="e1fce-111">Eine Common Language Runtime wird weiterhin vorhanden sein, bis JsDisposeRuntime aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="e1fce-111">A runtime will continue to exist until JsDisposeRuntime is called.</span></span>  
  
## <span data-ttu-id="e1fce-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e1fce-112">Requirements</span></span>  
 <span data-ttu-id="e1fce-113">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="e1fce-113">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="e1fce-114">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="e1fce-114">See Also</span></span>  
 [<span data-ttu-id="e1fce-115">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="e1fce-115">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)