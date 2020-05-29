---
description: Erstellt eine neue JavaScript-Funktion.
title: JsCreateFunction-Funktion | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsCreateFunction
helpviewer_keywords:
- JsCreateFunction function
ms.assetid: b298a96a-5ef7-4203-a8c8-55f9bfc6d2bb
caps.latest.revision: 13
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 22585afcb379c281eda621c3b233ccf4bc278ad1
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10567298"
---
# <span data-ttu-id="ee273-103">JsCreateFunction-Funktion</span><span class="sxs-lookup"><span data-stu-id="ee273-103">JsCreateFunction Function</span></span>
<span data-ttu-id="ee273-104">Erstellt eine neue JavaScript-Funktion.</span><span class="sxs-lookup"><span data-stu-id="ee273-104">Creates a new JavaScript function.</span></span>
  
## <span data-ttu-id="ee273-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ee273-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsCreateFunction(  
   _In_ JsNativeFunction nativeFunction,  
   _In_opt_ void *callbackState,  
   _Out_ JsValueRef *function  
);  
```  
  
#### <span data-ttu-id="ee273-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ee273-106">Parameters</span></span>  
 `nativeFunction`  
 <span data-ttu-id="ee273-107">Die Methode, die aufgerufen werden soll, wenn die Funktion aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="ee273-107">The method to call when the function is invoked.</span></span>  
  
 `callbackState`  
 <span data-ttu-id="ee273-108">Vom Benutzer bereitgestellter Zustand, der an den Rückruf zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="ee273-108">User-provided state that will be passed back to the callback.</span></span>  
  
 `function`  
 <span data-ttu-id="ee273-109">Das neue Function-Objekt.</span><span class="sxs-lookup"><span data-stu-id="ee273-109">The new function object.</span></span>  
  
## <span data-ttu-id="ee273-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ee273-110">Return Value</span></span>  
 <span data-ttu-id="ee273-111">Das Ergebnis des Anrufs (sofern vorhanden).</span><span class="sxs-lookup"><span data-stu-id="ee273-111">The result of the call, if any.</span></span>  
  
## <span data-ttu-id="ee273-112">Hinweise</span><span class="sxs-lookup"><span data-stu-id="ee273-112">Remarks</span></span>  
 <span data-ttu-id="ee273-113">Erfordert einen aktiven Skriptkontext.</span><span class="sxs-lookup"><span data-stu-id="ee273-113">Requires an active script context.</span></span>  
  
## <span data-ttu-id="ee273-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ee273-114">Requirements</span></span>  
 <span data-ttu-id="ee273-115">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="ee273-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="ee273-116">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="ee273-116">See Also</span></span>  
 [<span data-ttu-id="ee273-117">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="ee273-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)