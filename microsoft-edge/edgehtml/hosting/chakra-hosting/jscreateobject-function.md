---
description: Erstellt ein neues Objekt.
title: JsCreateObject-Funktion | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsCreateObject
helpviewer_keywords:
- JsCreateObject function
ms.assetid: 6c1d01a4-9254-443e-b974-6f0b0c861ca2
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: d5effe7ade1679392fcad7f2bb5cea880712ef7f
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233891"
---
# <span data-ttu-id="04a34-103">JsCreateObject Funktion</span><span class="sxs-lookup"><span data-stu-id="04a34-103">JsCreateObject Function</span></span>

<span data-ttu-id="04a34-104">Erstellt ein neues Objekt.</span><span class="sxs-lookup"><span data-stu-id="04a34-104">Creates a new object.</span></span>
  
## <span data-ttu-id="04a34-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="04a34-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsCreateObject(  
   _Out_ JsValueRef *object  
);  
```  
  
#### <span data-ttu-id="04a34-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="04a34-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="04a34-107">Das neue Objekt.</span><span class="sxs-lookup"><span data-stu-id="04a34-107">The new object.</span></span>  
  
## <span data-ttu-id="04a34-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="04a34-108">Return Value</span></span>  
 <span data-ttu-id="04a34-109">Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="04a34-109">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="04a34-110">Hinweise</span><span class="sxs-lookup"><span data-stu-id="04a34-110">Remarks</span></span>  
 <span data-ttu-id="04a34-111">Erfordert einen aktiven Skriptkontext.</span><span class="sxs-lookup"><span data-stu-id="04a34-111">Requires an active script context.</span></span>  
  
## <span data-ttu-id="04a34-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="04a34-112">Requirements</span></span>  
 <span data-ttu-id="04a34-113">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="04a34-113">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="04a34-114">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="04a34-114">See Also</span></span>  
 [<span data-ttu-id="04a34-115">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="04a34-115">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
