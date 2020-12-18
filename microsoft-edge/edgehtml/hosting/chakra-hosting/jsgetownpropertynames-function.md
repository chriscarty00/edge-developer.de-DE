---
description: Ruft die Liste aller Eigenschaften des Objekts ab.
title: JsGetOwnPropertyNames-Funktion | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsGetOwnPropertyNames
helpviewer_keywords:
- JsGetOwnPropertyNames function
ms.assetid: 0c17ea06-b17f-4ea3-ad04-1259a4d1b6de
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 4d00788b6ef581b923413e5c71a63bb27398a326
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233557"
---
# <span data-ttu-id="e7c6f-103">JsGetOwnPropertyNames Funktion</span><span class="sxs-lookup"><span data-stu-id="e7c6f-103">JsGetOwnPropertyNames Function</span></span>

<span data-ttu-id="e7c6f-104">Ruft die Liste aller Eigenschaften des Objekts ab.</span><span class="sxs-lookup"><span data-stu-id="e7c6f-104">Gets the list of all properties on the object.</span></span>  
  
## <span data-ttu-id="e7c6f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e7c6f-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetOwnPropertyNames(  
   _In_ JsValueRef object,  
   _Out_ JsValueRef *propertyNames  
);  
```  
  
#### <span data-ttu-id="e7c6f-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="e7c6f-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="e7c6f-107">Das Objekt, aus dem die Eigenschaftennamen abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="e7c6f-107">The object from which to get the property names.</span></span>  
  
 `propertyNames`  
 <span data-ttu-id="e7c6f-108">Ein Array von Eigenschaftennamen.</span><span class="sxs-lookup"><span data-stu-id="e7c6f-108">An array of property names.</span></span>  
  
## <span data-ttu-id="e7c6f-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e7c6f-109">Return Value</span></span>  
 <span data-ttu-id="e7c6f-110">Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="e7c6f-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="e7c6f-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="e7c6f-111">Remarks</span></span>  
 <span data-ttu-id="e7c6f-112">Erfordert einen aktiven Skriptkontext.</span><span class="sxs-lookup"><span data-stu-id="e7c6f-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="e7c6f-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e7c6f-113">Requirements</span></span>  
 <span data-ttu-id="e7c6f-114">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="e7c6f-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="e7c6f-115">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="e7c6f-115">See Also</span></span>  
 [<span data-ttu-id="e7c6f-116">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="e7c6f-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
