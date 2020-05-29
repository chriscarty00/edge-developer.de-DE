---
description: Erstellt ein neues JavaScript-ReferenceError-Fehlerobjekt.
title: JsCreateReferenceError-Funktion | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsCreateReferenceError
helpviewer_keywords:
- JsCreateReferenceError function
ms.assetid: 1d0b2339-4bea-4dd0-a46a-4dcbf0be3bd8
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 958af7111a233077aa7a2c2391b26666f55c634b
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10567291"
---
# <span data-ttu-id="03fcd-103">JsCreateReferenceError-Funktion</span><span class="sxs-lookup"><span data-stu-id="03fcd-103">JsCreateReferenceError Function</span></span>
<span data-ttu-id="03fcd-104">Erstellt ein neues JavaScript-ReferenceError-Fehlerobjekt.</span><span class="sxs-lookup"><span data-stu-id="03fcd-104">Creates a new JavaScript ReferenceError error object.</span></span>
  
## <span data-ttu-id="03fcd-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="03fcd-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsCreateReferenceError(  
   _In_ JsValueRef message,  
   _Out_ JsValueRef *error  
);  
```  
  
#### <span data-ttu-id="03fcd-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="03fcd-106">Parameters</span></span>  
 `message`  
 <span data-ttu-id="03fcd-107">Meldung für das Error-Objekt.</span><span class="sxs-lookup"><span data-stu-id="03fcd-107">Message for the error object.</span></span>  
  
 `error`  
 <span data-ttu-id="03fcd-108">Das neue Error-Objekt.</span><span class="sxs-lookup"><span data-stu-id="03fcd-108">The new error object.</span></span>  
  
## <span data-ttu-id="03fcd-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="03fcd-109">Return Value</span></span>  
 <span data-ttu-id="03fcd-110">Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="03fcd-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="03fcd-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="03fcd-111">Remarks</span></span>  
 <span data-ttu-id="03fcd-112">Erfordert einen aktiven Skriptkontext.</span><span class="sxs-lookup"><span data-stu-id="03fcd-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="03fcd-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="03fcd-113">Requirements</span></span>  
 <span data-ttu-id="03fcd-114">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="03fcd-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="03fcd-115">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="03fcd-115">See Also</span></span>  
 [<span data-ttu-id="03fcd-116">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="03fcd-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)