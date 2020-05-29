---
description: Erstellt ein neues JavaScript-TypeError-Fehlerobjekt.
title: JsCreateTypeError-Funktion | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsCreateTypeError
helpviewer_keywords:
- JsCreateTypeError function
ms.assetid: 8ef7bb77-2c98-482a-bccb-1f0fe2b826f5
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 302bf75af3668dfdd0b40336e940e3eef3a74bce
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10567279"
---
# <span data-ttu-id="999ce-103">JsCreateTypeError-Funktion</span><span class="sxs-lookup"><span data-stu-id="999ce-103">JsCreateTypeError Function</span></span>
<span data-ttu-id="999ce-104">Erstellt ein neues JavaScript-TypeError-Fehlerobjekt.</span><span class="sxs-lookup"><span data-stu-id="999ce-104">Creates a new JavaScript TypeError error object.</span></span>  
  
## <span data-ttu-id="999ce-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="999ce-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsCreateTypeError(  
   _In_ JsValueRef message,  
   _Out_ JsValueRef *error  
);  
```  
  
#### <span data-ttu-id="999ce-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="999ce-106">Parameters</span></span>  
 `message`  
 <span data-ttu-id="999ce-107">Meldung für das Error-Objekt.</span><span class="sxs-lookup"><span data-stu-id="999ce-107">Message for the error object.</span></span>  
  
 `error`  
 <span data-ttu-id="999ce-108">Das neue Error-Objekt.</span><span class="sxs-lookup"><span data-stu-id="999ce-108">The new error object.</span></span>  
  
## <span data-ttu-id="999ce-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="999ce-109">Return Value</span></span>  
 <span data-ttu-id="999ce-110">Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="999ce-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="999ce-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="999ce-111">Remarks</span></span>  
 <span data-ttu-id="999ce-112">Erfordert einen aktiven Skriptkontext.</span><span class="sxs-lookup"><span data-stu-id="999ce-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="999ce-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="999ce-113">Requirements</span></span>  
 <span data-ttu-id="999ce-114">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="999ce-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="999ce-115">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="999ce-115">See Also</span></span>  
 [<span data-ttu-id="999ce-116">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="999ce-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)