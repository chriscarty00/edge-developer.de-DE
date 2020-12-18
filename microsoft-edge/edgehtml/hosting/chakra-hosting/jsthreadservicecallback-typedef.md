---
description: Ein Rückruf des Thread Diensts.
title: JsThreadServiceCallback typedef | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: dbe67be5-418a-4f66-8b68-b38078a6d140
caps.latest.revision: 6
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: a5f1fe416e158e9524bdd1caab847977a5dd21b8
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233904"
---
# <span data-ttu-id="58df7-103">JsThreadServiceCallback Typedef</span><span class="sxs-lookup"><span data-stu-id="58df7-103">JsThreadServiceCallback Typedef</span></span>

<span data-ttu-id="58df7-104">Ein Rückruf des Thread Diensts.</span><span class="sxs-lookup"><span data-stu-id="58df7-104">A thread service callback.</span></span>  
  
## <span data-ttu-id="58df7-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="58df7-105">Syntax</span></span>  
  
```cpp  
typedef bool (CALLBACK *JsThreadServiceCallback)(  
   _In_ JsBackgroundWorkItemCallback callback,  
   _In_opt_ void *callbackData  
);  
```  
  
#### <span data-ttu-id="58df7-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="58df7-106">Parameters</span></span>  
 <span data-ttu-id="58df7-107">Rückruf</span><span class="sxs-lookup"><span data-stu-id="58df7-107">callback</span></span>  
 <span data-ttu-id="58df7-108">Der Rückruf für die Hintergrund Arbeitsaufgabe.</span><span class="sxs-lookup"><span data-stu-id="58df7-108">The callback for the background work item.</span></span>  
  
 <span data-ttu-id="58df7-109">callBackData</span><span class="sxs-lookup"><span data-stu-id="58df7-109">callbackData</span></span>  
 <span data-ttu-id="58df7-110">Das Daten Argument, das an den Rückruf übergeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="58df7-110">The data argument to be passed to the callback.</span></span>  
  
## <span data-ttu-id="58df7-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="58df7-111">Remarks</span></span>  
 <span data-ttu-id="58df7-112">Der Host kann einen Hintergrundthread Dienst angeben, wenn JsCreateRuntime aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="58df7-112">The host can specify a background thread service when calling JsCreateRuntime.</span></span> <span data-ttu-id="58df7-113">Wenn angegeben, werden Hintergrund Arbeitsaufgaben mithilfe dieses Rückrufs an den Host übergeben.</span><span class="sxs-lookup"><span data-stu-id="58df7-113">If specified, then background work items will be passed to the host using this callback.</span></span> <span data-ttu-id="58df7-114">Es wird erwartet, dass der Host die Hintergrund Arbeitsaufgabe sofort ausführt und "true" zurückgibt oder "false" zurückgibt und die Laufzeit die Arbeitsaufgabe in Thread behandelt.</span><span class="sxs-lookup"><span data-stu-id="58df7-114">The host is expected to either begin executing the background work item immediately and return true or return false and the runtime will handle the work item in-thread.</span></span>  
  
## <span data-ttu-id="58df7-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="58df7-115">Requirements</span></span>  
 <span data-ttu-id="58df7-116">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="58df7-116">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="58df7-117">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="58df7-117">See Also</span></span>  
 [<span data-ttu-id="58df7-118">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="58df7-118">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
