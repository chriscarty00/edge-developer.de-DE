---
description: Erstellt ein JavaScript-Symbol.
title: JsCreateSymbol-Funktion | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 2fccc5d9-f857-46cd-9aeb-f0a2e7cdee6b
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: a4e634e6f0726ca32ad1056129186ce941edb77b
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10567285"
---
# <span data-ttu-id="50e34-103">JsCreateSymbol-Funktion</span><span class="sxs-lookup"><span data-stu-id="50e34-103">JsCreateSymbol Function</span></span>
<span data-ttu-id="50e34-104">Erstellt ein JavaScript-Symbol.</span><span class="sxs-lookup"><span data-stu-id="50e34-104">Creates a JavaScript symbol.</span></span>
  
## <span data-ttu-id="50e34-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="50e34-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsCreateSymbol(  
   _In_ JsValueRef description,  
   _Out_ JsValueRef *result  
);  
```  
  
#### <span data-ttu-id="50e34-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="50e34-106">Parameters</span></span>  
 `description`  
 <span data-ttu-id="50e34-107">Die Zeichenfolgenbeschreibung für das Symbol.</span><span class="sxs-lookup"><span data-stu-id="50e34-107">The string description of the symbol.</span></span> <span data-ttu-id="50e34-108">Kann NULL sein.</span><span class="sxs-lookup"><span data-stu-id="50e34-108">Can be null.</span></span>  
  
 `result`  
 <span data-ttu-id="50e34-109">Das neue Symbol.</span><span class="sxs-lookup"><span data-stu-id="50e34-109">The new symbol.</span></span>  
  
## <span data-ttu-id="50e34-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="50e34-110">Return Value</span></span>  
 <span data-ttu-id="50e34-111">Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="50e34-111">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="50e34-112">Hinweise</span><span class="sxs-lookup"><span data-stu-id="50e34-112">Remarks</span></span>  
 <span data-ttu-id="50e34-113">Erfordert einen aktiven Skriptkontext.</span><span class="sxs-lookup"><span data-stu-id="50e34-113">Requires an active script context.</span></span>  
  
 <span data-ttu-id="50e34-114">Diese API wird nur im Microsoft Edge-Modus unterstützt.</span><span class="sxs-lookup"><span data-stu-id="50e34-114">This API is supported only in Microsoft Edge mode.</span></span>  
  
## <span data-ttu-id="50e34-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="50e34-115">Requirements</span></span>  
 <span data-ttu-id="50e34-116">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="50e34-116">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="50e34-117">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="50e34-117">See Also</span></span>  
 [<span data-ttu-id="50e34-118">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="50e34-118">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)