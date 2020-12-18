---
description: Löschen Sie den Wert am angegebenen Index eines Objekts.
title: JsDeleteIndexedProperty-Funktion | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsDeleteIndexedProperty
helpviewer_keywords:
- JsDeleteIndexedProperty function
ms.assetid: cc876839-2ecd-41a8-82d0-c19b3de944e3
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 1340b0204d3845d4a9bd3f18a58ec125a82d2bc0
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11234097"
---
# <span data-ttu-id="752ec-103">JsDeleteIndexedProperty Funktion</span><span class="sxs-lookup"><span data-stu-id="752ec-103">JsDeleteIndexedProperty Function</span></span>

<span data-ttu-id="752ec-104">Löschen Sie den Wert am angegebenen Index eines Objekts.</span><span class="sxs-lookup"><span data-stu-id="752ec-104">Delete the value at the specified index of an object.</span></span>  
  
## <span data-ttu-id="752ec-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="752ec-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsDeleteIndexedProperty(  
   _In_ JsValueRef object,  
   _In_ JsValueRef index  
);  
```  
  
#### <span data-ttu-id="752ec-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="752ec-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="752ec-107">Das Objekt, das ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="752ec-107">The object to operate on.</span></span>  
  
 `index`  
 <span data-ttu-id="752ec-108">Der zu löschende Index.</span><span class="sxs-lookup"><span data-stu-id="752ec-108">The index to delete.</span></span>  
  
## <span data-ttu-id="752ec-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="752ec-109">Return Value</span></span>  
 <span data-ttu-id="752ec-110">Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="752ec-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="752ec-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="752ec-111">Remarks</span></span>  
 <span data-ttu-id="752ec-112">Erfordert einen aktiven Skriptkontext.</span><span class="sxs-lookup"><span data-stu-id="752ec-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="752ec-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="752ec-113">Requirements</span></span>  
 <span data-ttu-id="752ec-114">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="752ec-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="752ec-115">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="752ec-115">See Also</span></span>  
 [<span data-ttu-id="752ec-116">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="752ec-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
