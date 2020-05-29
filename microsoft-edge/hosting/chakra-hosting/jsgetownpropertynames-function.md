---
description: Ruft die Liste aller Eigenschaften des Objekts ab.
title: JsGetOwnPropertyNames-Funktion | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsGetOwnPropertyNames
helpviewer_keywords:
- JsGetOwnPropertyNames function
ms.assetid: 0c17ea06-b17f-4ea3-ad04-1259a4d1b6de
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 5355caab864724d72fdb2c7abb3dc70e39662b55
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10568383"
---
# <span data-ttu-id="efc2b-103">JsGetOwnPropertyNames-Funktion</span><span class="sxs-lookup"><span data-stu-id="efc2b-103">JsGetOwnPropertyNames Function</span></span>
<span data-ttu-id="efc2b-104">Ruft die Liste aller Eigenschaften des Objekts ab.</span><span class="sxs-lookup"><span data-stu-id="efc2b-104">Gets the list of all properties on the object.</span></span>  
  
## <span data-ttu-id="efc2b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="efc2b-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetOwnPropertyNames(  
   _In_ JsValueRef object,  
   _Out_ JsValueRef *propertyNames  
);  
```  
  
#### <span data-ttu-id="efc2b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="efc2b-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="efc2b-107">Das Objekt, aus dem die Eigenschaftennamen abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="efc2b-107">The object from which to get the property names.</span></span>  
  
 `propertyNames`  
 <span data-ttu-id="efc2b-108">Ein Array von Eigenschaftennamen.</span><span class="sxs-lookup"><span data-stu-id="efc2b-108">An array of property names.</span></span>  
  
## <span data-ttu-id="efc2b-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="efc2b-109">Return Value</span></span>  
 <span data-ttu-id="efc2b-110">Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="efc2b-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="efc2b-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="efc2b-111">Remarks</span></span>  
 <span data-ttu-id="efc2b-112">Erfordert einen aktiven Skriptkontext.</span><span class="sxs-lookup"><span data-stu-id="efc2b-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="efc2b-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="efc2b-113">Requirements</span></span>  
 <span data-ttu-id="efc2b-114">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="efc2b-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="efc2b-115">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="efc2b-115">See Also</span></span>  
 [<span data-ttu-id="efc2b-116">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="efc2b-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)