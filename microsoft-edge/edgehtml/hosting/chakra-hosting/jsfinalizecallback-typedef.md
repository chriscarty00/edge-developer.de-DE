---
description: Ein Finalizer-Rückruf.
title: JsFinalizeCallback typedef | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: aa7a0269-b9d4-4717-97ac-8da7eb6ced15
caps.latest.revision: 6
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 794edbb3a61c8c213c0908740ed0a867488a2c6d
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233883"
---
# <span data-ttu-id="22fdd-103">JsFinalizeCallback Typedef</span><span class="sxs-lookup"><span data-stu-id="22fdd-103">JsFinalizeCallback Typedef</span></span>

<span data-ttu-id="22fdd-104">Ein Finalizer-Rückruf.</span><span class="sxs-lookup"><span data-stu-id="22fdd-104">A finalizer callback.</span></span>  
  
## <span data-ttu-id="22fdd-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="22fdd-105">Syntax</span></span>  
  
```cpp  
typedef void (CALLBACK *JsFinalizeCallback)(  
   _In_opt_ void *data  
);  
```  
  
#### <span data-ttu-id="22fdd-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="22fdd-106">Parameters</span></span>  
 <span data-ttu-id="22fdd-107">data</span><span class="sxs-lookup"><span data-stu-id="22fdd-107">data</span></span>  
 <span data-ttu-id="22fdd-108">Die externen Daten, die beim Erstellen des finalisierten Objekts übergeben wurden.</span><span class="sxs-lookup"><span data-stu-id="22fdd-108">The external data that was passed in when creating the object being finalized.</span></span>  
  
## <span data-ttu-id="22fdd-109">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="22fdd-109">Requirements</span></span>  
 <span data-ttu-id="22fdd-110">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="22fdd-110">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="22fdd-111">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="22fdd-111">See Also</span></span>  
 [<span data-ttu-id="22fdd-112">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="22fdd-112">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
