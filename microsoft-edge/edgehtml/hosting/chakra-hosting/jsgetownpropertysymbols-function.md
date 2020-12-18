---
description: Ruft die Liste aller Symbol Eigenschaften für das Objekt ab.
title: JsGetOwnPropertySymbols-Funktion | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 57c431e3-de0b-4ed0-b750-87a86448daff
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: d44da140f61a17d4cdc3a959c8fa7d017cbab1cc
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11234118"
---
# <span data-ttu-id="21a30-103">JsGetOwnPropertySymbols Funktion</span><span class="sxs-lookup"><span data-stu-id="21a30-103">JsGetOwnPropertySymbols Function</span></span>

<span data-ttu-id="21a30-104">Ruft die Liste aller Symbol Eigenschaften für das Objekt ab.</span><span class="sxs-lookup"><span data-stu-id="21a30-104">Gets the list of all symbol properties on the object.</span></span>  
  
## <span data-ttu-id="21a30-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="21a30-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetOwnPropertySymbols(  
   _In_ JsValueRef object,  
   _Out_ JsValueRef *propertySymbols  
);  
```  
  
#### <span data-ttu-id="21a30-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="21a30-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="21a30-107">Das Objekt, aus dem die Eigenschaften Symbole abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="21a30-107">The object from which to get the property symbols.</span></span>  
  
 `propertySymbols`  
 <span data-ttu-id="21a30-108">Ein Array von Eigenschafts Symbolen.</span><span class="sxs-lookup"><span data-stu-id="21a30-108">An array of property symbols.</span></span>  
  
## <span data-ttu-id="21a30-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="21a30-109">Return Value</span></span>  
 <span data-ttu-id="21a30-110">Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="21a30-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="21a30-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="21a30-111">Remarks</span></span>  
 <span data-ttu-id="21a30-112">Erfordert einen aktiven Skriptkontext.</span><span class="sxs-lookup"><span data-stu-id="21a30-112">Requires an active script context.</span></span>  
  
 <span data-ttu-id="21a30-113">Diese API wird nur im Microsoft Edge-Modus unterstützt.</span><span class="sxs-lookup"><span data-stu-id="21a30-113">This API is supported only in Microsoft Edge mode.</span></span>  
  
## <span data-ttu-id="21a30-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="21a30-114">Requirements</span></span>  
 <span data-ttu-id="21a30-115">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="21a30-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="21a30-116">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="21a30-116">See Also</span></span>  
 [<span data-ttu-id="21a30-117">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="21a30-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
