---
description: Erstellt eine neue JavaScript-Funktion.
title: JsCreateFunction-Funktion | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsCreateFunction
helpviewer_keywords:
- JsCreateFunction function
ms.assetid: b298a96a-5ef7-4203-a8c8-55f9bfc6d2bb
caps.latest.revision: 13
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: f7e67e86e6d8055664bfb1b58e6d5653f6d75d1b
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11234109"
---
# <span data-ttu-id="4f809-103">JsCreateFunction Funktion</span><span class="sxs-lookup"><span data-stu-id="4f809-103">JsCreateFunction Function</span></span>

<span data-ttu-id="4f809-104">Erstellt eine neue JavaScript-Funktion.</span><span class="sxs-lookup"><span data-stu-id="4f809-104">Creates a new JavaScript function.</span></span>
  
## <span data-ttu-id="4f809-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="4f809-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsCreateFunction(  
   _In_ JsNativeFunction nativeFunction,  
   _In_opt_ void *callbackState,  
   _Out_ JsValueRef *function  
);  
```  
  
#### <span data-ttu-id="4f809-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="4f809-106">Parameters</span></span>  
 `nativeFunction`  
 <span data-ttu-id="4f809-107">Die Methode, die aufgerufen werden soll, wenn die Funktion aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="4f809-107">The method to call when the function is invoked.</span></span>  
  
 `callbackState`  
 <span data-ttu-id="4f809-108">Vom Benutzer bereitgestellter Zustand, der an den Rückruf zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="4f809-108">User-provided state that will be passed back to the callback.</span></span>  
  
 `function`  
 <span data-ttu-id="4f809-109">Das neue Function-Objekt.</span><span class="sxs-lookup"><span data-stu-id="4f809-109">The new function object.</span></span>  
  
## <span data-ttu-id="4f809-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4f809-110">Return Value</span></span>  
 <span data-ttu-id="4f809-111">Das Ergebnis des Anrufs (sofern vorhanden).</span><span class="sxs-lookup"><span data-stu-id="4f809-111">The result of the call, if any.</span></span>  
  
## <span data-ttu-id="4f809-112">Hinweise</span><span class="sxs-lookup"><span data-stu-id="4f809-112">Remarks</span></span>  
 <span data-ttu-id="4f809-113">Erfordert einen aktiven Skriptkontext.</span><span class="sxs-lookup"><span data-stu-id="4f809-113">Requires an active script context.</span></span>  
  
## <span data-ttu-id="4f809-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4f809-114">Requirements</span></span>  
 <span data-ttu-id="4f809-115">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="4f809-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="4f809-116">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="4f809-116">See Also</span></span>  
 [<span data-ttu-id="4f809-117">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="4f809-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
