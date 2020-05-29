---
description: Ruft den aktuellen Speichergrenzwert für eine Laufzeit ab.
title: JsGetRuntimeMemoryLimit-Funktion | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsGetRuntimeMemoryLimit
helpviewer_keywords:
- JsGetRuntimeMemoryLimit function
ms.assetid: ed81ca60-99fd-46b0-89ae-f6ac07926904
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: e6b44bb1dc8ad5fb8c07248a225c10682f96c86a
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10567243"
---
# <span data-ttu-id="1861b-103">JsGetRuntimeMemoryLimit-Funktion</span><span class="sxs-lookup"><span data-stu-id="1861b-103">JsGetRuntimeMemoryLimit Function</span></span>
<span data-ttu-id="1861b-104">Ruft den aktuellen Speichergrenzwert für eine Laufzeit ab.</span><span class="sxs-lookup"><span data-stu-id="1861b-104">Gets the current memory limit for a runtime.</span></span>  
  
## <span data-ttu-id="1861b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="1861b-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetRuntimeMemoryLimit(  
   _In_ JsRuntimeHandle runtime,  
   _Out_ size_t *memoryLimit  
);  
```  
  
#### <span data-ttu-id="1861b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="1861b-106">Parameters</span></span>  
 `runtime`  
 <span data-ttu-id="1861b-107">Die Laufzeit, deren Speichergrenzwert abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="1861b-107">The runtime whose memory limit is to be retrieved.</span></span>  
  
 `memoryLimit`  
 <span data-ttu-id="1861b-108">Die aktuelle Speichergrenze der Laufzeit in Bytes oder-1, wenn kein Grenzwert festgesetzt wurde.</span><span class="sxs-lookup"><span data-stu-id="1861b-108">The runtime's current memory limit, in bytes, or -1 if no limit has been set.</span></span>  
  
## <span data-ttu-id="1861b-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1861b-109">Return Value</span></span>  
 <span data-ttu-id="1861b-110">Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="1861b-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="1861b-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="1861b-111">Remarks</span></span>  
 <span data-ttu-id="1861b-112">Die Speichergrenze einer Runtime kann immer abgerufen werden, unabhängig davon, ob die Laufzeit in einem anderen Thread aktiv ist oder nicht.</span><span class="sxs-lookup"><span data-stu-id="1861b-112">The memory limit of a runtime can be always be retrieved, regardless of whether or not the runtime is active on another thread.</span></span>  
  
## <span data-ttu-id="1861b-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1861b-113">Requirements</span></span>  
 <span data-ttu-id="1861b-114">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="1861b-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="1861b-115">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="1861b-115">See Also</span></span>  
 [<span data-ttu-id="1861b-116">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="1861b-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)