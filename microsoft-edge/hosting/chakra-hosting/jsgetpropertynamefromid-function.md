---
description: Ruft den Namen ab, der der Eigenschafts-ID zugeordnet ist.
title: JsGetPropertyNameFromId-Funktion | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsGetPropertyNameFromId
helpviewer_keywords:
- JsGetPropertyNameFromId function
ms.assetid: b4ca442c-573d-4bc3-adf7-1b8d48480b3a
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 1e76c69c1d746302bb95cd7229872845c4fbcc88
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10567250"
---
# <span data-ttu-id="b42f4-103">JsGetPropertyNameFromId-Funktion</span><span class="sxs-lookup"><span data-stu-id="b42f4-103">JsGetPropertyNameFromId Function</span></span>
<span data-ttu-id="b42f4-104">Ruft den Namen ab, der der Eigenschafts-ID zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="b42f4-104">Gets the name associated with the property ID.</span></span>  
  
## <span data-ttu-id="b42f4-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b42f4-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetPropertyNameFromId(  
   _In_ JsPropertyIdRef propertyId,  
   _Outptr_result_z_ const wchar_t **name  
);  
```  
  
#### <span data-ttu-id="b42f4-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="b42f4-106">Parameters</span></span>  
 `propertyId`  
 <span data-ttu-id="b42f4-107">Die Eigenschafts-ID, deren Name abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="b42f4-107">The property ID to get the name of.</span></span>  
  
 `name`  
 <span data-ttu-id="b42f4-108">Der Name, der der Eigenschafts-ID zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="b42f4-108">The name associated with the property ID.</span></span>  
  
## <span data-ttu-id="b42f4-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b42f4-109">Return Value</span></span>  
 <span data-ttu-id="b42f4-110">Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="b42f4-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="b42f4-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="b42f4-111">Remarks</span></span>  
 <span data-ttu-id="b42f4-112">Erfordert einen aktiven Skriptkontext.</span><span class="sxs-lookup"><span data-stu-id="b42f4-112">Requires an active script context.</span></span>  
  
 <span data-ttu-id="b42f4-113">Der zurückgegebene Puffer ist gültig, solange die Laufzeit aktiv ist, und kann nicht verwendet werden, nachdem die Laufzeit freigegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="b42f4-113">The returned buffer is valid as long as the runtime is alive and cannot be used once the runtime has been disposed.</span></span>  
  
## <span data-ttu-id="b42f4-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b42f4-114">Requirements</span></span>  
 <span data-ttu-id="b42f4-115">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="b42f4-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="b42f4-116">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="b42f4-116">See Also</span></span>  
 [<span data-ttu-id="b42f4-117">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="b42f4-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)