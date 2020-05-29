---
description: Erstellt eine neue JavaScript-Funktion mit dem Namen.
title: JsCreateNamedFunction-Funktion | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 72f40d06-ab82-4fed-a632-68af6b4126c2
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: d963fe196b8e56394e22501ed3898a0d887a3d3b
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10567296"
---
# <span data-ttu-id="4783b-103">JsCreateNamedFunction-Funktion</span><span class="sxs-lookup"><span data-stu-id="4783b-103">JsCreateNamedFunction Function</span></span>
<span data-ttu-id="4783b-104">Erstellt eine neue JavaScript-Funktion mit dem Namen.</span><span class="sxs-lookup"><span data-stu-id="4783b-104">Creates a new JavaScript function with name.</span></span>
  
## <span data-ttu-id="4783b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="4783b-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsCreateNamedFunction(  
   _In_ JsValueRef name,  
   _In_ JsNativeFunction nativeFunction,  
   _In_opt_ void *callbackState,  
   _Out_ JsValueRef *function  
);  
```  
  
#### <span data-ttu-id="4783b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="4783b-106">Parameters</span></span>  
 `name`  
 <span data-ttu-id="4783b-107">Der Name dieser Funktion, die für Diagnose-und stringification Zwecke verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="4783b-107">The name of this function that will be used for diagnostics and stringification purposes.</span></span>  
  
 `nativeFunction`  
 <span data-ttu-id="4783b-108">Die Methode, die aufgerufen werden soll, wenn die Funktion aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="4783b-108">The method to call when the function is invoked.</span></span>  
  
 `callbackState`  
 <span data-ttu-id="4783b-109">Der Benutzer hat den Zustand bereitgestellt, der an den Rückruf zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="4783b-109">User provided state that will be passed back to the callback.</span></span>  
  
 `function`  
 <span data-ttu-id="4783b-110">Das neue Function-Objekt.</span><span class="sxs-lookup"><span data-stu-id="4783b-110">The new function object.</span></span>  
  
## <span data-ttu-id="4783b-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4783b-111">Return Value</span></span>  
  
## <span data-ttu-id="4783b-112">Hinweise</span><span class="sxs-lookup"><span data-stu-id="4783b-112">Remarks</span></span>  
 <span data-ttu-id="4783b-113">Erfordert einen aktiven Skriptkontext.</span><span class="sxs-lookup"><span data-stu-id="4783b-113">Requires an active script context.</span></span>  
  
 <span data-ttu-id="4783b-114">Diese API wird nur im Microsoft Edge-Modus unterstützt.</span><span class="sxs-lookup"><span data-stu-id="4783b-114">This API is supported only in Microsoft Edge mode.</span></span>  
  
## <span data-ttu-id="4783b-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4783b-115">Requirements</span></span>  
 <span data-ttu-id="4783b-116">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="4783b-116">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="4783b-117">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="4783b-117">See Also</span></span>  
 [<span data-ttu-id="4783b-118">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="4783b-118">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)