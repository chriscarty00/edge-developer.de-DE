---
description: Ruft den Skriptkontext ab, zu dem das Objekt gehört.
title: JsGetContextOfObject-Funktion | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: cea6cdcd-790f-455c-af04-026af8ae2eb7
caps.latest.revision: 3
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 4f1b996954e877d9c98ac0caf06f255af629a386
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10567266"
---
# <span data-ttu-id="be838-103">JsGetContextOfObject Funktion</span><span class="sxs-lookup"><span data-stu-id="be838-103">JsGetContextOfObject Function</span></span>
<span data-ttu-id="be838-104">Ruft den Skriptkontext ab, zu dem das Objekt gehört.</span><span class="sxs-lookup"><span data-stu-id="be838-104">Gets the script context that the object belongs to.</span></span>  
  
## <span data-ttu-id="be838-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="be838-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetContextOfObject(  
  _In_ JsValueRef object,  
  _Out_ JsContextRef *context  
);  
```  
  
#### <span data-ttu-id="be838-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="be838-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="be838-107">Das Objekt, aus dem der Kontext abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="be838-107">The object to get the context from.</span></span>  
  
 `context`  
 <span data-ttu-id="be838-108">Der Kontext, zu dem das Objekt gehört.</span><span class="sxs-lookup"><span data-stu-id="be838-108">The context the object belongs to.</span></span>  
  
## <span data-ttu-id="be838-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="be838-109">Return Value</span></span>  
 <span data-ttu-id="be838-110">Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="be838-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="be838-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="be838-111">Remarks</span></span>  
 <span data-ttu-id="be838-112">Erfordert einen aktiven Skriptkontext.</span><span class="sxs-lookup"><span data-stu-id="be838-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="be838-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="be838-113">Requirements</span></span>  
 <span data-ttu-id="be838-114">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="be838-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="be838-115">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="be838-115">See Also</span></span>  
 [<span data-ttu-id="be838-116">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="be838-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)