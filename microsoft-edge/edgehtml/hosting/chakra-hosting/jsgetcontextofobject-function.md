---
description: Ruft den Skriptkontext ab, zu dem das Objekt gehört.
title: JsGetContextOfObject-Funktion | Microsoft docs
ms.prod: microsoft-edge
ms.topic: article
ms.assetid: cea6cdcd-790f-455c-af04-026af8ae2eb7
caps.latest.revision: 3
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 9085f9156e4e0ca9e952fe51447185239082f975
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11234007"
---
# <span data-ttu-id="eb880-103">JsGetContextOfObject Funktion</span><span class="sxs-lookup"><span data-stu-id="eb880-103">JsGetContextOfObject Function</span></span>

<span data-ttu-id="eb880-104">Ruft den Skriptkontext ab, zu dem das Objekt gehört.</span><span class="sxs-lookup"><span data-stu-id="eb880-104">Gets the script context that the object belongs to.</span></span>  
  
## <span data-ttu-id="eb880-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="eb880-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetContextOfObject(  
  _In_ JsValueRef object,  
  _Out_ JsContextRef *context  
);  
```  
  
#### <span data-ttu-id="eb880-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="eb880-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="eb880-107">Das Objekt, aus dem der Kontext abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="eb880-107">The object to get the context from.</span></span>  
  
 `context`  
 <span data-ttu-id="eb880-108">Der Kontext, zu dem das Objekt gehört.</span><span class="sxs-lookup"><span data-stu-id="eb880-108">The context the object belongs to.</span></span>  
  
## <span data-ttu-id="eb880-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="eb880-109">Return Value</span></span>  
 <span data-ttu-id="eb880-110">Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="eb880-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="eb880-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="eb880-111">Remarks</span></span>  
 <span data-ttu-id="eb880-112">Erfordert einen aktiven Skriptkontext.</span><span class="sxs-lookup"><span data-stu-id="eb880-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="eb880-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="eb880-113">Requirements</span></span>  
 <span data-ttu-id="eb880-114">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="eb880-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="eb880-115">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="eb880-115">See Also</span></span>  
 [<span data-ttu-id="eb880-116">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="eb880-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
