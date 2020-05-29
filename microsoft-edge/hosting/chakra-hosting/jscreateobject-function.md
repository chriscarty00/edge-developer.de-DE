---
description: Erstellt ein neues Objekt.
title: JsCreateObject-Funktion | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsCreateObject
helpviewer_keywords:
- JsCreateObject function
ms.assetid: 6c1d01a4-9254-443e-b974-6f0b0c861ca2
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 9ed988aae0921978819d379562d4a966e4a082a0
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10567294"
---
# <span data-ttu-id="ae36c-103">JsCreateObject-Funktion</span><span class="sxs-lookup"><span data-stu-id="ae36c-103">JsCreateObject Function</span></span>
<span data-ttu-id="ae36c-104">Erstellt ein neues Objekt.</span><span class="sxs-lookup"><span data-stu-id="ae36c-104">Creates a new object.</span></span>
  
## <span data-ttu-id="ae36c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ae36c-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsCreateObject(  
   _Out_ JsValueRef *object  
);  
```  
  
#### <span data-ttu-id="ae36c-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ae36c-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="ae36c-107">Das neue Objekt.</span><span class="sxs-lookup"><span data-stu-id="ae36c-107">The new object.</span></span>  
  
## <span data-ttu-id="ae36c-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ae36c-108">Return Value</span></span>  
 <span data-ttu-id="ae36c-109">Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="ae36c-109">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="ae36c-110">Hinweise</span><span class="sxs-lookup"><span data-stu-id="ae36c-110">Remarks</span></span>  
 <span data-ttu-id="ae36c-111">Erfordert einen aktiven Skriptkontext.</span><span class="sxs-lookup"><span data-stu-id="ae36c-111">Requires an active script context.</span></span>  
  
## <span data-ttu-id="ae36c-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ae36c-112">Requirements</span></span>  
 <span data-ttu-id="ae36c-113">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="ae36c-113">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="ae36c-114">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="ae36c-114">See Also</span></span>  
 [<span data-ttu-id="ae36c-115">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="ae36c-115">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)