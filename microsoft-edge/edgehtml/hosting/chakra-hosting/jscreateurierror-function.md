---
description: Erstellt ein neues JavaScript-URIError-Fehlerobjekt.
title: JsCreateURIError-Funktion | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsCreateURIError
helpviewer_keywords:
- JsCreateURIError function
ms.assetid: 711fd237-12a2-4ff0-b58a-ad74c91e79fb
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 88e6c1fc04607b3be088e297d1fa86f9374bcb03
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233889"
---
# <span data-ttu-id="a7de5-103">JsCreateURIError Funktion</span><span class="sxs-lookup"><span data-stu-id="a7de5-103">JsCreateURIError Function</span></span>

<span data-ttu-id="a7de5-104">Erstellt ein neues JavaScript-URIError-Fehlerobjekt.</span><span class="sxs-lookup"><span data-stu-id="a7de5-104">Creates a new JavaScript URIError error object.</span></span>  
  
## <span data-ttu-id="a7de5-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a7de5-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsCreateURIError(  
   _In_ JsValueRef message,  
   _Out_ JsValueRef *error  
);  
```  
  
#### <span data-ttu-id="a7de5-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a7de5-106">Parameters</span></span>  
 `message`  
 <span data-ttu-id="a7de5-107">Meldung für das Error-Objekt.</span><span class="sxs-lookup"><span data-stu-id="a7de5-107">Message for the error object.</span></span>  
  
 `error`  
 <span data-ttu-id="a7de5-108">Das neue Error-Objekt.</span><span class="sxs-lookup"><span data-stu-id="a7de5-108">The new error object.</span></span>  
  
## <span data-ttu-id="a7de5-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a7de5-109">Return Value</span></span>  
 <span data-ttu-id="a7de5-110">Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="a7de5-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="a7de5-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="a7de5-111">Remarks</span></span>  
 <span data-ttu-id="a7de5-112">Erfordert einen aktiven Skriptkontext.</span><span class="sxs-lookup"><span data-stu-id="a7de5-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="a7de5-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a7de5-113">Requirements</span></span>  
 <span data-ttu-id="a7de5-114">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="a7de5-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="a7de5-115">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="a7de5-115">See Also</span></span>  
 [<span data-ttu-id="a7de5-116">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="a7de5-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
