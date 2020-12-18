---
description: Erstellt ein neues JavaScript-RangeError-Fehlerobjekt.
title: JsCreateRangeError-Funktion | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsCreateRangeError
helpviewer_keywords:
- JsCreateRangeError function
ms.assetid: 0ab05de7-57af-4cfd-9aa5-0a69a893cc97
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 72cf882d5f9517f0f05d9e3367283f5f531dbdb3
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233916"
---
# <span data-ttu-id="db3e9-103">JsCreateRangeError Funktion</span><span class="sxs-lookup"><span data-stu-id="db3e9-103">JsCreateRangeError Function</span></span>

<span data-ttu-id="db3e9-104">Erstellt ein neues JavaScript-RangeError-Fehlerobjekt.</span><span class="sxs-lookup"><span data-stu-id="db3e9-104">Creates a new JavaScript RangeError error object.</span></span>
  
## <span data-ttu-id="db3e9-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="db3e9-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsCreateRangeError(  
   _In_ JsValueRef message,  
   _Out_ JsValueRef *error  
);  
```  
  
#### <span data-ttu-id="db3e9-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="db3e9-106">Parameters</span></span>  
 `message`  
 <span data-ttu-id="db3e9-107">Meldung für das Error-Objekt.</span><span class="sxs-lookup"><span data-stu-id="db3e9-107">Message for the error object.</span></span>  
  
 `error`  
 <span data-ttu-id="db3e9-108">Das neue Error-Objekt.</span><span class="sxs-lookup"><span data-stu-id="db3e9-108">The new error object.</span></span>  
  
## <span data-ttu-id="db3e9-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="db3e9-109">Return Value</span></span>  
 <span data-ttu-id="db3e9-110">Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="db3e9-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="db3e9-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="db3e9-111">Remarks</span></span>  
 <span data-ttu-id="db3e9-112">Erfordert einen aktiven Skriptkontext.</span><span class="sxs-lookup"><span data-stu-id="db3e9-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="db3e9-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="db3e9-113">Requirements</span></span>  
 <span data-ttu-id="db3e9-114">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="db3e9-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="db3e9-115">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="db3e9-115">See Also</span></span>  
 [<span data-ttu-id="db3e9-116">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="db3e9-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
