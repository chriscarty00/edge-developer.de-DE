---
description: Erstellt ein JavaScript `ArrayBuffer` -Objekt.
title: JsCreateArrayBuffer-Funktion | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: c9e74184-7dd9-41a7-a1fe-9575e1701392
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 3bee44d77f78bd35705211c598db78ab09000c71
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233749"
---
# <span data-ttu-id="14914-103">JsCreateArrayBuffer Funktion</span><span class="sxs-lookup"><span data-stu-id="14914-103">JsCreateArrayBuffer Function</span></span>

<span data-ttu-id="14914-104">Erstellt ein JavaScript `ArrayBuffer` -Objekt.</span><span class="sxs-lookup"><span data-stu-id="14914-104">Creates a JavaScript `ArrayBuffer` object.</span></span>  
  
## <span data-ttu-id="14914-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="14914-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsCreateArrayBuffer(  
   _In_ unsigned int byteLength,  
   _Out_ JsValueRef *result  
);  
```  
  
#### <span data-ttu-id="14914-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="14914-106">Parameters</span></span>  
 `byteLength`  
 <span data-ttu-id="14914-107">Die Anzahl der Bytes in der ArrayBuffer.</span><span class="sxs-lookup"><span data-stu-id="14914-107">The number of bytes in the ArrayBuffer.</span></span>  
  
 `result`  
 <span data-ttu-id="14914-108">Das neue ArrayBuffer-Objekt.</span><span class="sxs-lookup"><span data-stu-id="14914-108">The new ArrayBuffer object.</span></span>  
  
## <span data-ttu-id="14914-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="14914-109">Return Value</span></span>  
 <span data-ttu-id="14914-110">Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="14914-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="14914-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="14914-111">Remarks</span></span>  
 <span data-ttu-id="14914-112">Erfordert einen aktiven Skriptkontext.</span><span class="sxs-lookup"><span data-stu-id="14914-112">Requires an active script context.</span></span>  
  
 <span data-ttu-id="14914-113">Diese API wird nur im Microsoft Edge-Modus unterstützt.</span><span class="sxs-lookup"><span data-stu-id="14914-113">This API is supported only in Microsoft Edge mode.</span></span>  
  
## <span data-ttu-id="14914-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="14914-114">Requirements</span></span>  
 <span data-ttu-id="14914-115">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="14914-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="14914-116">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="14914-116">See Also</span></span>  
 [<span data-ttu-id="14914-117">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="14914-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
