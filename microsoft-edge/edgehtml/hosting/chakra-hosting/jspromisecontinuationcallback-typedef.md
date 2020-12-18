---
description: Ein Fortsetzungs Rückruf für Versprechen.
title: JsPromiseContinuationCallback typedef | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 51a3fd02-9668-4cf7-bb0b-e1fd03b2528f
caps.latest.revision: 3
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: da121d186cd9d0ab1a9770be08c9a92b52cf3366
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11234312"
---
# <span data-ttu-id="4f521-103">JsPromiseContinuationCallback Typedef</span><span class="sxs-lookup"><span data-stu-id="4f521-103">JsPromiseContinuationCallback Typedef</span></span>

<span data-ttu-id="4f521-104">Ein Fortsetzungs Rückruf für Versprechen.</span><span class="sxs-lookup"><span data-stu-id="4f521-104">A promise continuation callback.</span></span>  
  
## <span data-ttu-id="4f521-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="4f521-105">Syntax</span></span>  
  
```cpp  
typedef void (CALLBACK *JsPromiseContinuationCallback)(  
  _In_ JsValueRef task,  
  _In_opt_ void *callbackState  
);  
```  
  
#### <span data-ttu-id="4f521-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="4f521-106">Parameters</span></span>  
 `task`  
  `callbackState`  
  
## <span data-ttu-id="4f521-107">Hinweise</span><span class="sxs-lookup"><span data-stu-id="4f521-107">Remarks</span></span>  
 <span data-ttu-id="4f521-108">Der Host kann einen Promise-Fortsetzungs Rückruf in angeben `JsSetPromiseContinuationCallback` .</span><span class="sxs-lookup"><span data-stu-id="4f521-108">The host can specify a promise continuation callback in `JsSetPromiseContinuationCallback`.</span></span> <span data-ttu-id="4f521-109">Wenn ein Skript eine Aufgabe erstellt, die später ausgeführt werden soll, wird der Promise-Fortsetzungs Rückruf mit der Aufgabe aufgerufen, und die Aufgabe sollte in eine FIFO-Warteschlange gestellt werden, die ausgeführt werden soll, wenn das aktuelle Skript ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4f521-109">If a script creates a task to be run later, then the promise continuation callback will be called with the task and the task should be put in a FIFO queue, to be run when the current script is done executing.</span></span>  
  
 <span data-ttu-id="4f521-110">Diese API wird nur im EdgeHTML-Modus unterstützt.</span><span class="sxs-lookup"><span data-stu-id="4f521-110">This API is supported only in EdgeHTML mode.</span></span>  
  
## <span data-ttu-id="4f521-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4f521-111">Requirements</span></span>  
 <span data-ttu-id="4f521-112">jsrt. h</span><span class="sxs-lookup"><span data-stu-id="4f521-112">jsrt.h</span></span>  
  
## <span data-ttu-id="4f521-113">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="4f521-113">See Also</span></span>  
 [<span data-ttu-id="4f521-114">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="4f521-114">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
