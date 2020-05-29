---
description: Ein Rückruf des Thread Diensts.
title: JsThreadServiceCallback typedef | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: dbe67be5-418a-4f66-8b68-b38078a6d140
caps.latest.revision: 6
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 5eb9f2986c79db024f01f4d22050f79c9689400c
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10567202"
---
# <span data-ttu-id="d6feb-103">JsThreadServiceCallback typedef</span><span class="sxs-lookup"><span data-stu-id="d6feb-103">JsThreadServiceCallback Typedef</span></span>
<span data-ttu-id="d6feb-104">Ein Rückruf des Thread Diensts.</span><span class="sxs-lookup"><span data-stu-id="d6feb-104">A thread service callback.</span></span>  
  
## <span data-ttu-id="d6feb-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="d6feb-105">Syntax</span></span>  
  
```cpp  
typedef bool (CALLBACK *JsThreadServiceCallback)(  
   _In_ JsBackgroundWorkItemCallback callback,  
   _In_opt_ void *callbackData  
);  
```  
  
#### <span data-ttu-id="d6feb-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="d6feb-106">Parameters</span></span>  
 <span data-ttu-id="d6feb-107">Rückruf</span><span class="sxs-lookup"><span data-stu-id="d6feb-107">callback</span></span>  
 <span data-ttu-id="d6feb-108">Der Rückruf für die Hintergrund Arbeitsaufgabe.</span><span class="sxs-lookup"><span data-stu-id="d6feb-108">The callback for the background work item.</span></span>  
  
 <span data-ttu-id="d6feb-109">callBackData</span><span class="sxs-lookup"><span data-stu-id="d6feb-109">callbackData</span></span>  
 <span data-ttu-id="d6feb-110">Das Daten Argument, das an den Rückruf übergeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="d6feb-110">The data argument to be passed to the callback.</span></span>  
  
## <span data-ttu-id="d6feb-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="d6feb-111">Remarks</span></span>  
 <span data-ttu-id="d6feb-112">Der Host kann einen Hintergrundthread Dienst angeben, wenn JsCreateRuntime aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="d6feb-112">The host can specify a background thread service when calling JsCreateRuntime.</span></span> <span data-ttu-id="d6feb-113">Wenn angegeben, werden Hintergrund Arbeitsaufgaben mithilfe dieses Rückrufs an den Host übergeben.</span><span class="sxs-lookup"><span data-stu-id="d6feb-113">If specified, then background work items will be passed to the host using this callback.</span></span> <span data-ttu-id="d6feb-114">Es wird erwartet, dass der Host die Hintergrund Arbeitsaufgabe sofort ausführt und "true" zurückgibt oder "false" zurückgibt und die Laufzeit die Arbeitsaufgabe in Thread behandelt.</span><span class="sxs-lookup"><span data-stu-id="d6feb-114">The host is expected to either begin executing the background work item immediately and return true or return false and the runtime will handle the work item in-thread.</span></span>  
  
## <span data-ttu-id="d6feb-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d6feb-115">Requirements</span></span>  
 <span data-ttu-id="d6feb-116">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="d6feb-116">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="d6feb-117">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="d6feb-117">See Also</span></span>  
 [<span data-ttu-id="d6feb-118">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="d6feb-118">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)