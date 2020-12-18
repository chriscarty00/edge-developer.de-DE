---
description: Erstellt eine neue JavaScript-Funktion mit dem Namen.
title: JsCreateNamedFunction-Funktion | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 72f40d06-ab82-4fed-a632-68af6b4126c2
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: b54add359422a9312a0ded641051fd04585f3d7e
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233890"
---
# <span data-ttu-id="33bff-103">JsCreateNamedFunction Funktion</span><span class="sxs-lookup"><span data-stu-id="33bff-103">JsCreateNamedFunction Function</span></span>

<span data-ttu-id="33bff-104">Erstellt eine neue JavaScript-Funktion mit dem Namen.</span><span class="sxs-lookup"><span data-stu-id="33bff-104">Creates a new JavaScript function with name.</span></span>
  
## <span data-ttu-id="33bff-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="33bff-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsCreateNamedFunction(  
   _In_ JsValueRef name,  
   _In_ JsNativeFunction nativeFunction,  
   _In_opt_ void *callbackState,  
   _Out_ JsValueRef *function  
);  
```  
  
#### <span data-ttu-id="33bff-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="33bff-106">Parameters</span></span>  
 `name`  
 <span data-ttu-id="33bff-107">Der Name dieser Funktion, die für Diagnose-und stringification Zwecke verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="33bff-107">The name of this function that will be used for diagnostics and stringification purposes.</span></span>  
  
 `nativeFunction`  
 <span data-ttu-id="33bff-108">Die Methode, die aufgerufen werden soll, wenn die Funktion aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="33bff-108">The method to call when the function is invoked.</span></span>  
  
 `callbackState`  
 <span data-ttu-id="33bff-109">Der Benutzer hat den Zustand bereitgestellt, der an den Rückruf zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="33bff-109">User provided state that will be passed back to the callback.</span></span>  
  
 `function`  
 <span data-ttu-id="33bff-110">Das neue Function-Objekt.</span><span class="sxs-lookup"><span data-stu-id="33bff-110">The new function object.</span></span>  
  
## <span data-ttu-id="33bff-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="33bff-111">Return Value</span></span>  
  
## <span data-ttu-id="33bff-112">Hinweise</span><span class="sxs-lookup"><span data-stu-id="33bff-112">Remarks</span></span>  
 <span data-ttu-id="33bff-113">Erfordert einen aktiven Skriptkontext.</span><span class="sxs-lookup"><span data-stu-id="33bff-113">Requires an active script context.</span></span>  
  
 <span data-ttu-id="33bff-114">Diese API wird nur im Microsoft Edge-Modus unterstützt.</span><span class="sxs-lookup"><span data-stu-id="33bff-114">This API is supported only in Microsoft Edge mode.</span></span>  
  
## <span data-ttu-id="33bff-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="33bff-115">Requirements</span></span>  
 <span data-ttu-id="33bff-116">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="33bff-116">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="33bff-117">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="33bff-117">See Also</span></span>  
 [<span data-ttu-id="33bff-118">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="33bff-118">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
