---
description: Ein Rückruf, der vor der Sammlung aufgerufen wird.
title: JsBeforeCollectCallback typedef | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 58bece47-4e6d-49e7-a93d-b6a8f9928b41
caps.latest.revision: 6
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 23ed386a6a28d356aa80cf85650a981d4836a6b6
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233773"
---
# <span data-ttu-id="c4d38-103">JsBeforeCollectCallback Typedef</span><span class="sxs-lookup"><span data-stu-id="c4d38-103">JsBeforeCollectCallback Typedef</span></span>

<span data-ttu-id="c4d38-104">Ein Rückruf, der vor der Sammlung aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="c4d38-104">A callback called before collection.</span></span>  
  
## <span data-ttu-id="c4d38-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c4d38-105">Syntax</span></span>  
  
```cpp  
typedef void (CALLBACK *JsBeforeCollectCallback)(  
_In_opt_ void *callbackState  
);  
```  
  
#### <span data-ttu-id="c4d38-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c4d38-106">Parameters</span></span>  
 <span data-ttu-id="c4d38-107">callbackState</span><span class="sxs-lookup"><span data-stu-id="c4d38-107">callbackState</span></span>  
 <span data-ttu-id="c4d38-108">Der Zustand, der an JsSetBeforeCollectCallback übergeben wurde.</span><span class="sxs-lookup"><span data-stu-id="c4d38-108">The state passed to JsSetBeforeCollectCallback.</span></span>  
  
## <span data-ttu-id="c4d38-109">Hinweise</span><span class="sxs-lookup"><span data-stu-id="c4d38-109">Remarks</span></span>  
 <span data-ttu-id="c4d38-110">Verwenden Sie JsSetBeforeCollectCallback, um diesen Rückruf zu registrieren.</span><span class="sxs-lookup"><span data-stu-id="c4d38-110">Use JsSetBeforeCollectCallback to register this callback.</span></span>  
  
## <span data-ttu-id="c4d38-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c4d38-111">Requirements</span></span>  
 <span data-ttu-id="c4d38-112">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="c4d38-112">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="c4d38-113">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="c4d38-113">See Also</span></span>  
 [<span data-ttu-id="c4d38-114">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="c4d38-114">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
