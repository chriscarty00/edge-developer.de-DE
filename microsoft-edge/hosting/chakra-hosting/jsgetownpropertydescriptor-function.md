---
description: Ruft einen Eigenschaftendeskriptor für die eigene Eigenschaft eines Objekts ab.
title: JsGetOwnPropertyDescriptor-Funktion | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsGetOwnPropertyDescriptor
helpviewer_keywords:
- JsGetOwnPropertyDescriptor function
ms.assetid: 44c417ce-ab63-44eb-a0ab-19838e3ab34f
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 6f500aec8b892cb2ad437bd7159ab14165a8bfb4
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10568390"
---
# <span data-ttu-id="317fb-103">JsGetOwnPropertyDescriptor-Funktion</span><span class="sxs-lookup"><span data-stu-id="317fb-103">JsGetOwnPropertyDescriptor Function</span></span>
<span data-ttu-id="317fb-104">Ruft einen Eigenschaftendeskriptor für die eigene Eigenschaft eines Objekts ab.</span><span class="sxs-lookup"><span data-stu-id="317fb-104">Gets a property descriptor for an object's own property.</span></span>  
  
## <span data-ttu-id="317fb-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="317fb-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetOwnPropertyDescriptor(  
   _In_ JsValueRef object,  
   _In_ JsPropertyIdRef propertyId,  
   _Out_ JsValueRef *propertyDescriptor  
);  
```  
  
#### <span data-ttu-id="317fb-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="317fb-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="317fb-107">Das Objekt, das die Eigenschaft aufweist.</span><span class="sxs-lookup"><span data-stu-id="317fb-107">The object that has the property.</span></span>  
  
 `propertyId`  
 <span data-ttu-id="317fb-108">Die ID der Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="317fb-108">The ID of the property.</span></span>  
  
 `propertyDescriptor`  
 <span data-ttu-id="317fb-109">Der Eigenschaftendeskriptor.</span><span class="sxs-lookup"><span data-stu-id="317fb-109">The property descriptor.</span></span>  
  
## <span data-ttu-id="317fb-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="317fb-110">Return Value</span></span>  
 <span data-ttu-id="317fb-111">Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="317fb-111">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="317fb-112">Hinweise</span><span class="sxs-lookup"><span data-stu-id="317fb-112">Remarks</span></span>  
 <span data-ttu-id="317fb-113">Erfordert einen aktiven Skriptkontext.</span><span class="sxs-lookup"><span data-stu-id="317fb-113">Requires an active script context.</span></span>  
  
## <span data-ttu-id="317fb-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="317fb-114">Requirements</span></span>  
 <span data-ttu-id="317fb-115">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="317fb-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="317fb-116">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="317fb-116">See Also</span></span>  
 [<span data-ttu-id="317fb-117">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="317fb-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)