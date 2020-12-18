---
description: Erstellt ein neues JavaScript-Fehlerobjekt.
title: JsCreateError-Funktion | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsCreateError
helpviewer_keywords:
- JsCreateError function
ms.assetid: dadbcac8-c56f-4f30-ba00-2d284daee191
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: cd2fd0172902cc6dc8a4dd169eef5947d0b25256
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233751"
---
# <span data-ttu-id="d5571-103">JsCreateError Funktion</span><span class="sxs-lookup"><span data-stu-id="d5571-103">JsCreateError Function</span></span>

<span data-ttu-id="d5571-104">Erstellt ein neues JavaScript-Fehlerobjekt.</span><span class="sxs-lookup"><span data-stu-id="d5571-104">Creates a new JavaScript error object.</span></span>  
  
## <span data-ttu-id="d5571-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="d5571-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsCreateError(  
   _In_ JsValueRef message,  
   _Out_ JsValueRef *error  
);  
```  
  
#### <span data-ttu-id="d5571-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="d5571-106">Parameters</span></span>  
 `message`  
 <span data-ttu-id="d5571-107">Meldung für das Error-Objekt.</span><span class="sxs-lookup"><span data-stu-id="d5571-107">Message for the error object.</span></span>  
  
 `error`  
 <span data-ttu-id="d5571-108">Das neue Error-Objekt.</span><span class="sxs-lookup"><span data-stu-id="d5571-108">The new error object.</span></span>  
  
## <span data-ttu-id="d5571-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d5571-109">Return Value</span></span>  
 <span data-ttu-id="d5571-110">Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="d5571-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="d5571-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="d5571-111">Remarks</span></span>  
 <span data-ttu-id="d5571-112">Erfordert einen aktiven Skriptkontext.</span><span class="sxs-lookup"><span data-stu-id="d5571-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="d5571-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d5571-113">Requirements</span></span>  
 <span data-ttu-id="d5571-114">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="d5571-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="d5571-115">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="d5571-115">See Also</span></span>  
 [<span data-ttu-id="d5571-116">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="d5571-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
