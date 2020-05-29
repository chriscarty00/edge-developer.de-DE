---
description: Macht ein Objekt nicht erweiterbar.
title: JsPreventExtension-Funktion | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsPreventExtension
helpviewer_keywords:
- JsPreventExtension function
ms.assetid: 8da07e20-d076-4ae4-9fb0-3f3c141518c2
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: baa001b2fd26133ef3a20c88213ac6aaf34a2e0d
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10568342"
---
# <span data-ttu-id="de75e-103">JsPreventExtension-Funktion</span><span class="sxs-lookup"><span data-stu-id="de75e-103">JsPreventExtension Function</span></span>
<span data-ttu-id="de75e-104">Macht ein Objekt nicht erweiterbar.</span><span class="sxs-lookup"><span data-stu-id="de75e-104">Makes an object non-extensible.</span></span>  
  
## <span data-ttu-id="de75e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="de75e-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsPreventExtension(  
   _In_ JsValueRef object  
);  
```  
  
#### <span data-ttu-id="de75e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="de75e-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="de75e-107">Das Objekt, das nicht erweiterbar sein soll.</span><span class="sxs-lookup"><span data-stu-id="de75e-107">The object to make non-extensible.</span></span>  
  
## <span data-ttu-id="de75e-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="de75e-108">Return Value</span></span>  
 <span data-ttu-id="de75e-109">Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="de75e-109">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="de75e-110">Hinweise</span><span class="sxs-lookup"><span data-stu-id="de75e-110">Remarks</span></span>  
 <span data-ttu-id="de75e-111">Erfordert einen aktiven Skriptkontext.</span><span class="sxs-lookup"><span data-stu-id="de75e-111">Requires an active script context.</span></span>  
  
## <span data-ttu-id="de75e-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="de75e-112">Requirements</span></span>  
 <span data-ttu-id="de75e-113">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="de75e-113">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="de75e-114">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="de75e-114">See Also</span></span>  
 [<span data-ttu-id="de75e-115">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="de75e-115">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)