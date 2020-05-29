---
description: Erstellt ein JavaScript `ArrayBuffer` -Objekt.
title: JsCreateArrayBuffer-Funktion | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: c9e74184-7dd9-41a7-a1fe-9575e1701392
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 7e81c50317de5243fbcdf761c09c084f97a8e1e0
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10567313"
---
# <span data-ttu-id="cdd2c-103">JsCreateArrayBuffer-Funktion</span><span class="sxs-lookup"><span data-stu-id="cdd2c-103">JsCreateArrayBuffer Function</span></span>
<span data-ttu-id="cdd2c-104">Erstellt ein JavaScript `ArrayBuffer` -Objekt.</span><span class="sxs-lookup"><span data-stu-id="cdd2c-104">Creates a JavaScript `ArrayBuffer` object.</span></span>  
  
## <span data-ttu-id="cdd2c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="cdd2c-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsCreateArrayBuffer(  
   _In_ unsigned int byteLength,  
   _Out_ JsValueRef *result  
);  
```  
  
#### <span data-ttu-id="cdd2c-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="cdd2c-106">Parameters</span></span>  
 `byteLength`  
 <span data-ttu-id="cdd2c-107">Die Anzahl der Bytes in der ArrayBuffer.</span><span class="sxs-lookup"><span data-stu-id="cdd2c-107">The number of bytes in the ArrayBuffer.</span></span>  
  
 `result`  
 <span data-ttu-id="cdd2c-108">Das neue ArrayBuffer-Objekt.</span><span class="sxs-lookup"><span data-stu-id="cdd2c-108">The new ArrayBuffer object.</span></span>  
  
## <span data-ttu-id="cdd2c-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cdd2c-109">Return Value</span></span>  
 <span data-ttu-id="cdd2c-110">Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="cdd2c-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="cdd2c-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="cdd2c-111">Remarks</span></span>  
 <span data-ttu-id="cdd2c-112">Erfordert einen aktiven Skriptkontext.</span><span class="sxs-lookup"><span data-stu-id="cdd2c-112">Requires an active script context.</span></span>  
  
 <span data-ttu-id="cdd2c-113">Diese API wird nur im Microsoft Edge-Modus unterstützt.</span><span class="sxs-lookup"><span data-stu-id="cdd2c-113">This API is supported only in Microsoft Edge mode.</span></span>  
  
## <span data-ttu-id="cdd2c-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cdd2c-114">Requirements</span></span>  
 <span data-ttu-id="cdd2c-115">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="cdd2c-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="cdd2c-116">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="cdd2c-116">See Also</span></span>  
 [<span data-ttu-id="cdd2c-117">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="cdd2c-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)