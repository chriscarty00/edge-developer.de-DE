---
description: Führt JavaScript `instanceof` -Operator Test aus.
title: JsInstanceOf-Funktion | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 94399a62-b996-4fd2-82ce-1c26e7a4da08
caps.latest.revision: 6
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: d8aec1d4512fe937d1fd48aa6f3e88294bf9850c
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11234132"
---
# <span data-ttu-id="eb17e-103">JsInstanceOf Funktion</span><span class="sxs-lookup"><span data-stu-id="eb17e-103">JsInstanceOf Function</span></span>

<span data-ttu-id="eb17e-104">Führt JavaScript `instanceof` -Operator Test aus.</span><span class="sxs-lookup"><span data-stu-id="eb17e-104">Performs JavaScript `instanceof` operator test.</span></span>  
  
## <span data-ttu-id="eb17e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="eb17e-105">Syntax</span></span>  
  
```cpp  
JsInstanceOf(   
  _In_ JsValueRef object,  
  _In_ JsValueRef constructor,  
  _Out_ bool *result  
);  
  
```  
  
#### <span data-ttu-id="eb17e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="eb17e-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="eb17e-107">Das zu testende Objekt.</span><span class="sxs-lookup"><span data-stu-id="eb17e-107">The object to test.</span></span>  
  
 `constructor`  
 <span data-ttu-id="eb17e-108">Die Konstruktorfunktion, die getestet werden soll.</span><span class="sxs-lookup"><span data-stu-id="eb17e-108">The constructor function to test against.</span></span>  
  
 `result`  
 <span data-ttu-id="eb17e-109">Gibt an, ob der "Object instanceof-Konstruktor" wahr ist.</span><span class="sxs-lookup"><span data-stu-id="eb17e-109">Whether the "object instanceof constructor" is true.</span></span>  
  
## <span data-ttu-id="eb17e-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="eb17e-110">Return Value</span></span>  
 <span data-ttu-id="eb17e-111">Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="eb17e-111">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="eb17e-112">Hinweise</span><span class="sxs-lookup"><span data-stu-id="eb17e-112">Remarks</span></span>  
 <span data-ttu-id="eb17e-113">Erfordert einen aktiven Skriptkontext.</span><span class="sxs-lookup"><span data-stu-id="eb17e-113">Requires an active script context.</span></span>  
  
## <span data-ttu-id="eb17e-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="eb17e-114">Requirements</span></span>  
 <span data-ttu-id="eb17e-115">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="eb17e-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="eb17e-116">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="eb17e-116">See Also</span></span>  
 [<span data-ttu-id="eb17e-117">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="eb17e-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
