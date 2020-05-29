---
description: Legt die externen Daten für ein externes Objekt fest.
title: JsSetExternalData-Funktion | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsSetExternalData
helpviewer_keywords:
- JsSetExternalData function
ms.assetid: 94e0ad34-67d7-4f7f-88a3-3b057ef5e4b9
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: cc638905786a1baa0a3d5f79bfa3792a764f358f
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10568312"
---
# <span data-ttu-id="3880c-103">JsSetExternalData-Funktion</span><span class="sxs-lookup"><span data-stu-id="3880c-103">JsSetExternalData Function</span></span>
<span data-ttu-id="3880c-104">Legt die externen Daten für ein externes Objekt fest.</span><span class="sxs-lookup"><span data-stu-id="3880c-104">Sets the external data on an external object.</span></span>  
  
## <span data-ttu-id="3880c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="3880c-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsSetExternalData(  
   _In_ JsValueRef object,  
   _In_opt_ void *externalData  
);  
```  
  
#### <span data-ttu-id="3880c-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="3880c-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="3880c-107">Das externe Objekt.</span><span class="sxs-lookup"><span data-stu-id="3880c-107">The external object.</span></span>  
  
 `externalData`  
 <span data-ttu-id="3880c-108">Die im Objekt gespeicherten externen Daten.</span><span class="sxs-lookup"><span data-stu-id="3880c-108">The external data stored in the object.</span></span> <span data-ttu-id="3880c-109">Kann NULL sein, wenn keine externen Daten im Objekt gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="3880c-109">Can be null if no external data is stored in the object.</span></span>  
  
## <span data-ttu-id="3880c-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3880c-110">Return Value</span></span>  
 <span data-ttu-id="3880c-111">Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="3880c-111">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="3880c-112">Hinweise</span><span class="sxs-lookup"><span data-stu-id="3880c-112">Remarks</span></span>  
 <span data-ttu-id="3880c-113">Erfordert einen aktiven Skriptkontext.</span><span class="sxs-lookup"><span data-stu-id="3880c-113">Requires an active script context.</span></span>  
  
## <span data-ttu-id="3880c-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3880c-114">Requirements</span></span>  
 <span data-ttu-id="3880c-115">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="3880c-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="3880c-116">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="3880c-116">See Also</span></span>  
 [<span data-ttu-id="3880c-117">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="3880c-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)