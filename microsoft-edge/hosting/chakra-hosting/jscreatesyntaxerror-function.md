---
description: Erstellt ein neues JavaScript-Syntax Error initialisiert-Fehlerobjekt.
title: JsCreateSyntaxError-Funktion | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsCreateSyntaxError
helpviewer_keywords:
- JsCreateSyntaxError function
ms.assetid: 839845fc-60c4-4ffc-bfcc-fd7a8f06126f
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 8f7459e8300df56aa8ccfaa78ef97ce2b6ec6fa0
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10567282"
---
# <span data-ttu-id="8ec97-103">JsCreateSyntaxError-Funktion</span><span class="sxs-lookup"><span data-stu-id="8ec97-103">JsCreateSyntaxError Function</span></span>
<span data-ttu-id="8ec97-104">Erstellt ein neues JavaScript-Syntax Error initialisiert-Fehlerobjekt.</span><span class="sxs-lookup"><span data-stu-id="8ec97-104">Creates a new JavaScript SyntaxError error object.</span></span>  
  
## <span data-ttu-id="8ec97-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="8ec97-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsCreateSyntaxError(  
   _In_ JsValueRef message,  
   _Out_ JsValueRef *error  
);  
```  
  
#### <span data-ttu-id="8ec97-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="8ec97-106">Parameters</span></span>  
 `message`  
 <span data-ttu-id="8ec97-107">Meldung für das Error-Objekt.</span><span class="sxs-lookup"><span data-stu-id="8ec97-107">Message for the error object.</span></span>  
  
 `error`  
 <span data-ttu-id="8ec97-108">Das neue Error-Objekt.</span><span class="sxs-lookup"><span data-stu-id="8ec97-108">The new error object.</span></span>  
  
## <span data-ttu-id="8ec97-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8ec97-109">Return Value</span></span>  
 <span data-ttu-id="8ec97-110">Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="8ec97-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="8ec97-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="8ec97-111">Remarks</span></span>  
 <span data-ttu-id="8ec97-112">Erfordert einen aktiven Skriptkontext.</span><span class="sxs-lookup"><span data-stu-id="8ec97-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="8ec97-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8ec97-113">Requirements</span></span>  
 <span data-ttu-id="8ec97-114">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="8ec97-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="8ec97-115">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="8ec97-115">See Also</span></span>  
 [<span data-ttu-id="8ec97-116">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="8ec97-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)