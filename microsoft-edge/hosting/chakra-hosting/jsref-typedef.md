---
description: Ein Verweis auf ein Objekt, das dem Chakra Garbage Collector gehört.
title: JsRef typedef | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 6aafc39f-6b9c-457f-8bf0-48831bffe9b8
caps.latest.revision: 6
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: f5ce1ada67a4530ba57345b90c0b7deba6954c7c
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10568340"
---
# <span data-ttu-id="094c6-103">JsRef typedef</span><span class="sxs-lookup"><span data-stu-id="094c6-103">JsRef Typedef</span></span>
<span data-ttu-id="094c6-104">Ein Verweis auf ein Objekt, das dem Chakra Garbage Collector gehört.</span><span class="sxs-lookup"><span data-stu-id="094c6-104">A reference to an object owned by the Chakra garbage collector.</span></span>  
  
## <span data-ttu-id="094c6-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="094c6-105">Syntax</span></span>  
  
```cpp  
typedef void *JsRef;  
```  
  
## <span data-ttu-id="094c6-106">Hinweise</span><span class="sxs-lookup"><span data-stu-id="094c6-106">Remarks</span></span>  
 <span data-ttu-id="094c6-107">Eine Chakra-Laufzeit erfasst JsRef-Verweise automatisch, solange Sie in lokalen Variablen oder in Parametern (also auf dem Stapel) gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="094c6-107">A Chakra runtime will automatically track JsRef references as long as they are on stored in local variables or in parameters (i.e. on the stack).</span></span> <span data-ttu-id="094c6-108">Das Speichern eines JsRef an einer anderen Stelle als auf dem Stapel erfordert das Aufrufen von JsAddRef und JsRelease, um die Lebensdauer des Objekts zu verwalten, andernfalls kann der Garbage Collector das Objekt freigeben, während es noch verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="094c6-108">Storing a JsRef somewhere other than on the stack requires calling JsAddRef and JsRelease to manage the lifetime of the object, otherwise the garbage collector may free the object while it is still in use.</span></span>  
  
## <span data-ttu-id="094c6-109">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="094c6-109">Requirements</span></span>  
 <span data-ttu-id="094c6-110">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="094c6-110">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="094c6-111">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="094c6-111">See Also</span></span>  
 [<span data-ttu-id="094c6-112">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="094c6-112">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)