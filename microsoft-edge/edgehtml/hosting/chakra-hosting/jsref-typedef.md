---
description: Ein Verweis auf ein Objekt, das dem Chakra Garbage Collector gehört.
title: JsRef typedef | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 6aafc39f-6b9c-457f-8bf0-48831bffe9b8
caps.latest.revision: 6
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 69d13472b15b5d448908b5dafb2e3d7dc0ace7e4
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233576"
---
# <span data-ttu-id="5d763-103">JsRef Typedef</span><span class="sxs-lookup"><span data-stu-id="5d763-103">JsRef Typedef</span></span>

<span data-ttu-id="5d763-104">Ein Verweis auf ein Objekt, das dem Chakra Garbage Collector gehört.</span><span class="sxs-lookup"><span data-stu-id="5d763-104">A reference to an object owned by the Chakra garbage collector.</span></span>  
  
## <span data-ttu-id="5d763-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="5d763-105">Syntax</span></span>  
  
```cpp  
typedef void *JsRef;  
```  
  
## <span data-ttu-id="5d763-106">Hinweise</span><span class="sxs-lookup"><span data-stu-id="5d763-106">Remarks</span></span>  
 <span data-ttu-id="5d763-107">Eine Chakra-Laufzeit erfasst JsRef-Verweise automatisch, solange Sie in lokalen Variablen oder in Parametern (also auf dem Stapel) gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="5d763-107">A Chakra runtime will automatically track JsRef references as long as they are on stored in local variables or in parameters (i.e. on the stack).</span></span> <span data-ttu-id="5d763-108">Das Speichern eines JsRef an einer anderen Stelle als auf dem Stapel erfordert das Aufrufen von JsAddRef und JsRelease, um die Lebensdauer des Objekts zu verwalten, andernfalls kann der Garbage Collector das Objekt freigeben, während es noch verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="5d763-108">Storing a JsRef somewhere other than on the stack requires calling JsAddRef and JsRelease to manage the lifetime of the object, otherwise the garbage collector may free the object while it is still in use.</span></span>  
  
## <span data-ttu-id="5d763-109">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5d763-109">Requirements</span></span>  
 <span data-ttu-id="5d763-110">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="5d763-110">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="5d763-111">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="5d763-111">See Also</span></span>  
 [<span data-ttu-id="5d763-112">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="5d763-112">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
