---
description: Führt JavaScript `instanceof` -Operator Test aus.
title: JsInstanceOf-Funktion | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: 94399a62-b996-4fd2-82ce-1c26e7a4da08
caps.latest.revision: 6
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 3a7e2397abe5dcb25346e583a0fdab301b8b45f4
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10567231"
---
# <span data-ttu-id="4217c-103">JsInstanceOf-Funktion</span><span class="sxs-lookup"><span data-stu-id="4217c-103">JsInstanceOf Function</span></span>
<span data-ttu-id="4217c-104">Führt JavaScript `instanceof` -Operator Test aus.</span><span class="sxs-lookup"><span data-stu-id="4217c-104">Performs JavaScript `instanceof` operator test.</span></span>  
  
## <span data-ttu-id="4217c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="4217c-105">Syntax</span></span>  
  
```cpp  
JsInstanceOf(   
  _In_ JsValueRef object,  
  _In_ JsValueRef constructor,  
  _Out_ bool *result  
);  
  
```  
  
#### <span data-ttu-id="4217c-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="4217c-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="4217c-107">Das zu testende Objekt.</span><span class="sxs-lookup"><span data-stu-id="4217c-107">The object to test.</span></span>  
  
 `constructor`  
 <span data-ttu-id="4217c-108">Die Konstruktorfunktion, die getestet werden soll.</span><span class="sxs-lookup"><span data-stu-id="4217c-108">The constructor function to test against.</span></span>  
  
 `result`  
 <span data-ttu-id="4217c-109">Gibt an, ob der "Object instanceof-Konstruktor" wahr ist.</span><span class="sxs-lookup"><span data-stu-id="4217c-109">Whether the "object instanceof constructor" is true.</span></span>  
  
## <span data-ttu-id="4217c-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4217c-110">Return Value</span></span>  
 <span data-ttu-id="4217c-111">Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="4217c-111">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="4217c-112">Hinweise</span><span class="sxs-lookup"><span data-stu-id="4217c-112">Remarks</span></span>  
 <span data-ttu-id="4217c-113">Erfordert einen aktiven Skriptkontext.</span><span class="sxs-lookup"><span data-stu-id="4217c-113">Requires an active script context.</span></span>  
  
## <span data-ttu-id="4217c-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4217c-114">Requirements</span></span>  
 <span data-ttu-id="4217c-115">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="4217c-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="4217c-116">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="4217c-116">See Also</span></span>  
 [<span data-ttu-id="4217c-117">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="4217c-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)