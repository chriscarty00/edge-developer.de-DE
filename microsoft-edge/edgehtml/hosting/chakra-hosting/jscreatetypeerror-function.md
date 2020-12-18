---
description: Erstellt ein neues JavaScript-TypeError-Fehlerobjekt.
title: JsCreateTypeError-Funktion | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsCreateTypeError
helpviewer_keywords:
- JsCreateTypeError function
ms.assetid: 8ef7bb77-2c98-482a-bccb-1f0fe2b826f5
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 627dfdc6f01f0708366720a957b3784fc7bb59a4
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11234101"
---
# <span data-ttu-id="5c2c7-103">JsCreateTypeError Funktion</span><span class="sxs-lookup"><span data-stu-id="5c2c7-103">JsCreateTypeError Function</span></span>

<span data-ttu-id="5c2c7-104">Erstellt ein neues JavaScript-TypeError-Fehlerobjekt.</span><span class="sxs-lookup"><span data-stu-id="5c2c7-104">Creates a new JavaScript TypeError error object.</span></span>  
  
## <span data-ttu-id="5c2c7-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="5c2c7-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsCreateTypeError(  
   _In_ JsValueRef message,  
   _Out_ JsValueRef *error  
);  
```  
  
#### <span data-ttu-id="5c2c7-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="5c2c7-106">Parameters</span></span>  
 `message`  
 <span data-ttu-id="5c2c7-107">Meldung für das Error-Objekt.</span><span class="sxs-lookup"><span data-stu-id="5c2c7-107">Message for the error object.</span></span>  
  
 `error`  
 <span data-ttu-id="5c2c7-108">Das neue Error-Objekt.</span><span class="sxs-lookup"><span data-stu-id="5c2c7-108">The new error object.</span></span>  
  
## <span data-ttu-id="5c2c7-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5c2c7-109">Return Value</span></span>  
 <span data-ttu-id="5c2c7-110">Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="5c2c7-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="5c2c7-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="5c2c7-111">Remarks</span></span>  
 <span data-ttu-id="5c2c7-112">Erfordert einen aktiven Skriptkontext.</span><span class="sxs-lookup"><span data-stu-id="5c2c7-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="5c2c7-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5c2c7-113">Requirements</span></span>  
 <span data-ttu-id="5c2c7-114">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="5c2c7-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="5c2c7-115">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="5c2c7-115">See Also</span></span>  
 [<span data-ttu-id="5c2c7-116">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="5c2c7-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
