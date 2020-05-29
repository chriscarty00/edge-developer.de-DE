---
description: Erstellt ein neues JavaScript-Fehlerobjekt.
title: JsCreateError-Funktion | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsCreateError
helpviewer_keywords:
- JsCreateError function
ms.assetid: dadbcac8-c56f-4f30-ba00-2d284daee191
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 33d70e3f077b085ccb4ab541d3246d777ea68978
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10567304"
---
# <span data-ttu-id="cdfed-103">JsCreateError-Funktion</span><span class="sxs-lookup"><span data-stu-id="cdfed-103">JsCreateError Function</span></span>
<span data-ttu-id="cdfed-104">Erstellt ein neues JavaScript-Fehlerobjekt.</span><span class="sxs-lookup"><span data-stu-id="cdfed-104">Creates a new JavaScript error object.</span></span>  
  
## <span data-ttu-id="cdfed-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="cdfed-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsCreateError(  
   _In_ JsValueRef message,  
   _Out_ JsValueRef *error  
);  
```  
  
#### <span data-ttu-id="cdfed-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="cdfed-106">Parameters</span></span>  
 `message`  
 <span data-ttu-id="cdfed-107">Meldung für das Error-Objekt.</span><span class="sxs-lookup"><span data-stu-id="cdfed-107">Message for the error object.</span></span>  
  
 `error`  
 <span data-ttu-id="cdfed-108">Das neue Error-Objekt.</span><span class="sxs-lookup"><span data-stu-id="cdfed-108">The new error object.</span></span>  
  
## <span data-ttu-id="cdfed-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cdfed-109">Return Value</span></span>  
 <span data-ttu-id="cdfed-110">Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="cdfed-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="cdfed-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="cdfed-111">Remarks</span></span>  
 <span data-ttu-id="cdfed-112">Erfordert einen aktiven Skriptkontext.</span><span class="sxs-lookup"><span data-stu-id="cdfed-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="cdfed-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cdfed-113">Requirements</span></span>  
 <span data-ttu-id="cdfed-114">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="cdfed-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="cdfed-115">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="cdfed-115">See Also</span></span>  
 [<span data-ttu-id="cdfed-116">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="cdfed-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)