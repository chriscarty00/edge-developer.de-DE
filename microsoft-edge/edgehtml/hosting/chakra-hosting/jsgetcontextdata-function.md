---
description: Ruft die interne Datengruppe in JsrtContext ab.
title: JsGetContextData-Funktion | Microsoft docs
ms.prod: microsoft-edge
ms.topic: article
ms.assetid: f5d7e446-267a-4a80-a427-6e1b95a3391b
caps.latest.revision: 4
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 8f5f70a9c36fea355792050c1a2a810bca2d07b3
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233875"
---
# <span data-ttu-id="8f0d6-103">JsGetContextData Funktion</span><span class="sxs-lookup"><span data-stu-id="8f0d6-103">JsGetContextData Function</span></span>

<span data-ttu-id="8f0d6-104">Ruft die interne Datengruppe in JsrtContext ab.</span><span class="sxs-lookup"><span data-stu-id="8f0d6-104">Gets the internal data set on JsrtContext.</span></span>  
  
## <span data-ttu-id="8f0d6-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="8f0d6-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetContextData(  
  _In_ JsContextRef context,  
  _Out_ void **data  
);  
```  
  
#### <span data-ttu-id="8f0d6-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="8f0d6-106">Parameters</span></span>  
 `context`  
 <span data-ttu-id="8f0d6-107">Der Kontext, aus dem die Daten abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="8f0d6-107">The context to get the data from.</span></span>  
  
 `data`  
 <span data-ttu-id="8f0d6-108">Der Zeiger auf die Daten, in die Daten zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="8f0d6-108">The pointer to the data where data will be returned.</span></span>  
  
## <span data-ttu-id="8f0d6-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8f0d6-109">Return Value</span></span>  
 <span data-ttu-id="8f0d6-110">Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="8f0d6-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="8f0d6-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="8f0d6-111">Remarks</span></span>  
 <span data-ttu-id="8f0d6-112">Erfordert einen aktiven Skriptkontext.</span><span class="sxs-lookup"><span data-stu-id="8f0d6-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="8f0d6-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8f0d6-113">Requirements</span></span>  
 <span data-ttu-id="8f0d6-114">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="8f0d6-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="8f0d6-115">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="8f0d6-115">See Also</span></span>  
 [<span data-ttu-id="8f0d6-116">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="8f0d6-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
