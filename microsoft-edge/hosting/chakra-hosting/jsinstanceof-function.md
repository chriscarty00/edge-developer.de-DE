---
description: Führt JavaScript `instanceof` -Operator Test aus.
title: JsInstanceOf-Funktion | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 94399a62-b996-4fd2-82ce-1c26e7a4da08
caps.latest.revision: 6
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 4d9bf2e4c3da9f83fdf7c0ef4e2c31df04670420
ms.sourcegitcommit: 037a2d62333691104c9accb4862968f80a3465a2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/18/2020
ms.locfileid: "10751975"
---
# <span data-ttu-id="554dc-103">JsInstanceOf Funktion</span><span class="sxs-lookup"><span data-stu-id="554dc-103">JsInstanceOf Function</span></span>
<span data-ttu-id="554dc-104">Führt JavaScript `instanceof` -Operator Test aus.</span><span class="sxs-lookup"><span data-stu-id="554dc-104">Performs JavaScript `instanceof` operator test.</span></span>  
  
## <span data-ttu-id="554dc-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="554dc-105">Syntax</span></span>  
  
```cpp  
JsInstanceOf(   
  _In_ JsValueRef object,  
  _In_ JsValueRef constructor,  
  _Out_ bool *result  
);  
  
```  
  
#### <span data-ttu-id="554dc-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="554dc-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="554dc-107">Das zu testende Objekt.</span><span class="sxs-lookup"><span data-stu-id="554dc-107">The object to test.</span></span>  
  
 `constructor`  
 <span data-ttu-id="554dc-108">Die Konstruktorfunktion, die getestet werden soll.</span><span class="sxs-lookup"><span data-stu-id="554dc-108">The constructor function to test against.</span></span>  
  
 `result`  
 <span data-ttu-id="554dc-109">Gibt an, ob der "Object instanceof-Konstruktor" wahr ist.</span><span class="sxs-lookup"><span data-stu-id="554dc-109">Whether the "object instanceof constructor" is true.</span></span>  
  
## <span data-ttu-id="554dc-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="554dc-110">Return Value</span></span>  
 <span data-ttu-id="554dc-111">Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="554dc-111">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="554dc-112">Hinweise</span><span class="sxs-lookup"><span data-stu-id="554dc-112">Remarks</span></span>  
 <span data-ttu-id="554dc-113">Erfordert einen aktiven Skriptkontext.</span><span class="sxs-lookup"><span data-stu-id="554dc-113">Requires an active script context.</span></span>  
  
## <span data-ttu-id="554dc-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="554dc-114">Requirements</span></span>  
 <span data-ttu-id="554dc-115">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="554dc-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="554dc-116">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="554dc-116">See Also</span></span>  
 [<span data-ttu-id="554dc-117">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="554dc-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)