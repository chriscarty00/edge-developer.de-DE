---
description: Erstellt ein JavaScript-Array Objekt.
title: JsCreateArray-Funktion | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsCreateArray
helpviewer_keywords:
- JsCreateArray function
ms.assetid: a119949a-e427-4349-9d00-5ec20fb9319c
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: fb6a65df1484eb308224a42bb5a65443855c6215
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10567312"
---
# <span data-ttu-id="24773-103">JsCreateArray-Funktion</span><span class="sxs-lookup"><span data-stu-id="24773-103">JsCreateArray Function</span></span>
<span data-ttu-id="24773-104">Erstellt ein JavaScript-Array Objekt.</span><span class="sxs-lookup"><span data-stu-id="24773-104">Creates a Javascript array object.</span></span>  
  
## <span data-ttu-id="24773-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="24773-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsCreateArray(  
   _In_ unsigned int length,  
   _Out_ JsValueRef *result  
);  
```  
  
#### <span data-ttu-id="24773-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="24773-106">Parameters</span></span>  
 `length`  
 <span data-ttu-id="24773-107">Die anfängliche Länge des Arrays.</span><span class="sxs-lookup"><span data-stu-id="24773-107">The initial length of the array.</span></span>  
  
 `result`  
 <span data-ttu-id="24773-108">Das neue Array-Objekt.</span><span class="sxs-lookup"><span data-stu-id="24773-108">The new array object.</span></span>  
  
## <span data-ttu-id="24773-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="24773-109">Return Value</span></span>  
 <span data-ttu-id="24773-110">Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="24773-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="24773-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="24773-111">Remarks</span></span>  
 <span data-ttu-id="24773-112">Erfordert einen aktiven Skriptkontext.</span><span class="sxs-lookup"><span data-stu-id="24773-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="24773-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="24773-113">Requirements</span></span>  
 <span data-ttu-id="24773-114">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="24773-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="24773-115">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="24773-115">See Also</span></span>  
 [<span data-ttu-id="24773-116">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="24773-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)