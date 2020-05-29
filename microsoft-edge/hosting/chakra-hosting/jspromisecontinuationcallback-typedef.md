---
description: Ein Fortsetzungs Rückruf für Versprechen.
title: JsPromiseContinuationCallback typedef | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 51a3fd02-9668-4cf7-bb0b-e1fd03b2528f
caps.latest.revision: 3
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 023d88af5ff82056d8f57453e0a53b91b34565a6
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10567204"
---
# <span data-ttu-id="40e8d-103">JsPromiseContinuationCallback typedef</span><span class="sxs-lookup"><span data-stu-id="40e8d-103">JsPromiseContinuationCallback Typedef</span></span>
<span data-ttu-id="40e8d-104">Ein Fortsetzungs Rückruf für Versprechen.</span><span class="sxs-lookup"><span data-stu-id="40e8d-104">A promise continuation callback.</span></span>  
  
## <span data-ttu-id="40e8d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="40e8d-105">Syntax</span></span>  
  
```cpp  
typedef void (CALLBACK *JsPromiseContinuationCallback)(  
  _In_ JsValueRef task,  
  _In_opt_ void *callbackState  
);  
```  
  
#### <span data-ttu-id="40e8d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="40e8d-106">Parameters</span></span>  
 `task`  
  `callbackState`  
  
## <span data-ttu-id="40e8d-107">Hinweise</span><span class="sxs-lookup"><span data-stu-id="40e8d-107">Remarks</span></span>  
 <span data-ttu-id="40e8d-108">Der Host kann einen Promise-Fortsetzungs Rückruf in angeben `JsSetPromiseContinuationCallback` .</span><span class="sxs-lookup"><span data-stu-id="40e8d-108">The host can specify a promise continuation callback in `JsSetPromiseContinuationCallback`.</span></span> <span data-ttu-id="40e8d-109">Wenn ein Skript eine Aufgabe erstellt, die später ausgeführt werden soll, wird der Promise-Fortsetzungs Rückruf mit der Aufgabe aufgerufen, und die Aufgabe sollte in eine FIFO-Warteschlange gestellt werden, die ausgeführt werden soll, wenn das aktuelle Skript ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="40e8d-109">If a script creates a task to be run later, then the promise continuation callback will be called with the task and the task should be put in a FIFO queue, to be run when the current script is done executing.</span></span>  
  
 <span data-ttu-id="40e8d-110">Diese API wird nur im EdgeHTML-Modus unterstützt.</span><span class="sxs-lookup"><span data-stu-id="40e8d-110">This API is supported only in EdgeHTML mode.</span></span>  
  
## <span data-ttu-id="40e8d-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="40e8d-111">Requirements</span></span>  
 <span data-ttu-id="40e8d-112">jsrt. h</span><span class="sxs-lookup"><span data-stu-id="40e8d-112">jsrt.h</span></span>  
  
## <span data-ttu-id="40e8d-113">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="40e8d-113">See Also</span></span>  
 [<span data-ttu-id="40e8d-114">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="40e8d-114">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)