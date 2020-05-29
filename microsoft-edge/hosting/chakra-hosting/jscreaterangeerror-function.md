---
description: Erstellt ein neues JavaScript-RangeError-Fehlerobjekt.
title: JsCreateRangeError-Funktion | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsCreateRangeError
helpviewer_keywords:
- JsCreateRangeError function
ms.assetid: 0ab05de7-57af-4cfd-9aa5-0a69a893cc97
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 3759f1c04a2eb13488f756ae2c135373d9db1f74
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10567293"
---
# <span data-ttu-id="d7052-103">JsCreateRangeError-Funktion</span><span class="sxs-lookup"><span data-stu-id="d7052-103">JsCreateRangeError Function</span></span>
<span data-ttu-id="d7052-104">Erstellt ein neues JavaScript-RangeError-Fehlerobjekt.</span><span class="sxs-lookup"><span data-stu-id="d7052-104">Creates a new JavaScript RangeError error object.</span></span>
  
## <span data-ttu-id="d7052-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="d7052-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsCreateRangeError(  
   _In_ JsValueRef message,  
   _Out_ JsValueRef *error  
);  
```  
  
#### <span data-ttu-id="d7052-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="d7052-106">Parameters</span></span>  
 `message`  
 <span data-ttu-id="d7052-107">Meldung für das Error-Objekt.</span><span class="sxs-lookup"><span data-stu-id="d7052-107">Message for the error object.</span></span>  
  
 `error`  
 <span data-ttu-id="d7052-108">Das neue Error-Objekt.</span><span class="sxs-lookup"><span data-stu-id="d7052-108">The new error object.</span></span>  
  
## <span data-ttu-id="d7052-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d7052-109">Return Value</span></span>  
 <span data-ttu-id="d7052-110">Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="d7052-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="d7052-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="d7052-111">Remarks</span></span>  
 <span data-ttu-id="d7052-112">Erfordert einen aktiven Skriptkontext.</span><span class="sxs-lookup"><span data-stu-id="d7052-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="d7052-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d7052-113">Requirements</span></span>  
 <span data-ttu-id="d7052-114">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="d7052-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="d7052-115">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="d7052-115">See Also</span></span>  
 [<span data-ttu-id="d7052-116">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="d7052-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)