---
description: Erstellt ein JavaScript-Symbol.
title: JsCreateSymbol-Funktion | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 2fccc5d9-f857-46cd-9aeb-f0a2e7cdee6b
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 6a2f77f477aeebac150635d93cbd0cd043357256
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233967"
---
# <span data-ttu-id="1aba6-103">JsCreateSymbol Funktion</span><span class="sxs-lookup"><span data-stu-id="1aba6-103">JsCreateSymbol Function</span></span>

<span data-ttu-id="1aba6-104">Erstellt ein JavaScript-Symbol.</span><span class="sxs-lookup"><span data-stu-id="1aba6-104">Creates a JavaScript symbol.</span></span>
  
## <span data-ttu-id="1aba6-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="1aba6-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsCreateSymbol(  
   _In_ JsValueRef description,  
   _Out_ JsValueRef *result  
);  
```  
  
#### <span data-ttu-id="1aba6-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="1aba6-106">Parameters</span></span>  
 `description`  
 <span data-ttu-id="1aba6-107">Die Zeichenfolgenbeschreibung für das Symbol.</span><span class="sxs-lookup"><span data-stu-id="1aba6-107">The string description of the symbol.</span></span> <span data-ttu-id="1aba6-108">Kann NULL sein.</span><span class="sxs-lookup"><span data-stu-id="1aba6-108">Can be null.</span></span>  
  
 `result`  
 <span data-ttu-id="1aba6-109">Das neue Symbol.</span><span class="sxs-lookup"><span data-stu-id="1aba6-109">The new symbol.</span></span>  
  
## <span data-ttu-id="1aba6-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1aba6-110">Return Value</span></span>  
 <span data-ttu-id="1aba6-111">Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="1aba6-111">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="1aba6-112">Hinweise</span><span class="sxs-lookup"><span data-stu-id="1aba6-112">Remarks</span></span>  
 <span data-ttu-id="1aba6-113">Erfordert einen aktiven Skriptkontext.</span><span class="sxs-lookup"><span data-stu-id="1aba6-113">Requires an active script context.</span></span>  
  
 <span data-ttu-id="1aba6-114">Diese API wird nur im Microsoft Edge-Modus unterstützt.</span><span class="sxs-lookup"><span data-stu-id="1aba6-114">This API is supported only in Microsoft Edge mode.</span></span>  
  
## <span data-ttu-id="1aba6-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1aba6-115">Requirements</span></span>  
 <span data-ttu-id="1aba6-116">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="1aba6-116">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="1aba6-117">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="1aba6-117">See Also</span></span>  
 [<span data-ttu-id="1aba6-118">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="1aba6-118">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
