---
description: Ein Rückruf für einen Arbeitsaufgaben Hintergrund
title: JsBackgroundWorkItemCallback typedef | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: e6db52e1-830c-46a2-b9f9-cc2d450a1da8
caps.latest.revision: 6
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: d69306b334c2e0c9b27b96a5a417739ffdcd7dd7
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233782"
---
# <span data-ttu-id="0854c-103">JsBackgroundWorkItemCallback Typedef</span><span class="sxs-lookup"><span data-stu-id="0854c-103">JsBackgroundWorkItemCallback Typedef</span></span>

<span data-ttu-id="0854c-104">Ein Rückruf für einen Arbeitsaufgaben Hintergrund</span><span class="sxs-lookup"><span data-stu-id="0854c-104">A background work item callback.</span></span>  
  
## <span data-ttu-id="0854c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="0854c-105">Syntax</span></span>  
  
```cpp  
typedef void (CALLBACK *JsBackgroundWorkItemCallback)(  
   _In_opt_ void *callbackData  
);  
```  
  
#### <span data-ttu-id="0854c-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="0854c-106">Parameters</span></span>  
 <span data-ttu-id="0854c-107">callBackData</span><span class="sxs-lookup"><span data-stu-id="0854c-107">callbackData</span></span>  
 <span data-ttu-id="0854c-108">Daten Argument, das an den Thread Dienst übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="0854c-108">Data argument passed to the thread service.</span></span>  
  
## <span data-ttu-id="0854c-109">Hinweise</span><span class="sxs-lookup"><span data-stu-id="0854c-109">Remarks</span></span>  
 <span data-ttu-id="0854c-110">Diese wird an den Thread Dienst des Hosts übergeben (sofern vorhanden), damit der Host den Arbeitsaufgaben Rückruf im Hintergrundthread seiner Wahl aufrufen kann.</span><span class="sxs-lookup"><span data-stu-id="0854c-110">This is passed to the host's thread service (if provided) to allow the host to invoke the work item callback on the background thread of its choice.</span></span>  
  
## <span data-ttu-id="0854c-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0854c-111">Requirements</span></span>  
 <span data-ttu-id="0854c-112">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="0854c-112">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="0854c-113">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="0854c-113">See Also</span></span>  
 [<span data-ttu-id="0854c-114">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="0854c-114">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
