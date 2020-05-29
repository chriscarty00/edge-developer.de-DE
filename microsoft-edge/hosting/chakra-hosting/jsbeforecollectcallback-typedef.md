---
description: Ein Rückruf, der vor der Sammlung aufgerufen wird.
title: JsBeforeCollectCallback typedef | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 58bece47-4e6d-49e7-a93d-b6a8f9928b41
caps.latest.revision: 6
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 17f279c2d2ffcc8d02819994dddebfc22baa4cab
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10567333"
---
# <span data-ttu-id="8652a-103">JsBeforeCollectCallback typedef</span><span class="sxs-lookup"><span data-stu-id="8652a-103">JsBeforeCollectCallback Typedef</span></span>
<span data-ttu-id="8652a-104">Ein Rückruf, der vor der Sammlung aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="8652a-104">A callback called before collection.</span></span>  
  
## <span data-ttu-id="8652a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="8652a-105">Syntax</span></span>  
  
```cpp  
typedef void (CALLBACK *JsBeforeCollectCallback)(  
_In_opt_ void *callbackState  
);  
```  
  
#### <span data-ttu-id="8652a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="8652a-106">Parameters</span></span>  
 <span data-ttu-id="8652a-107">callbackState</span><span class="sxs-lookup"><span data-stu-id="8652a-107">callbackState</span></span>  
 <span data-ttu-id="8652a-108">Der Zustand, der an JsSetBeforeCollectCallback übergeben wurde.</span><span class="sxs-lookup"><span data-stu-id="8652a-108">The state passed to JsSetBeforeCollectCallback.</span></span>  
  
## <span data-ttu-id="8652a-109">Hinweise</span><span class="sxs-lookup"><span data-stu-id="8652a-109">Remarks</span></span>  
 <span data-ttu-id="8652a-110">Verwenden Sie JsSetBeforeCollectCallback, um diesen Rückruf zu registrieren.</span><span class="sxs-lookup"><span data-stu-id="8652a-110">Use JsSetBeforeCollectCallback to register this callback.</span></span>  
  
## <span data-ttu-id="8652a-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8652a-111">Requirements</span></span>  
 <span data-ttu-id="8652a-112">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="8652a-112">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="8652a-113">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="8652a-113">See Also</span></span>  
 [<span data-ttu-id="8652a-114">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="8652a-114">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)