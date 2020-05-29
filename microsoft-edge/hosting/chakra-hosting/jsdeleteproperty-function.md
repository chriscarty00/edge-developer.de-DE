---
description: Löscht die Eigenschaft eines Objekts.
title: JsDeleteProperty-Funktion | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsDeleteProperty
helpviewer_keywords:
- JsDeleteProperty function
ms.assetid: 0f6ac6a7-3576-42f5-98d0-1c06542c8149
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: c5539238324d59126b45f19fa9a6f8facc0f2ee3
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10567274"
---
# <span data-ttu-id="ee400-103">JsDeleteProperty-Funktion</span><span class="sxs-lookup"><span data-stu-id="ee400-103">JsDeleteProperty Function</span></span>
<span data-ttu-id="ee400-104">Löscht die Eigenschaft eines Objekts.</span><span class="sxs-lookup"><span data-stu-id="ee400-104">Deletes an object's property.</span></span>  
  
## <span data-ttu-id="ee400-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ee400-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsDeleteProperty(  
   _In_ JsValueRef object,  
   _In_ JsPropertyIdRef propertyId,  
   _In_ bool useStrictRules,  
   _Out_ JsValueRef *result  
);  
```  
  
#### <span data-ttu-id="ee400-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ee400-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="ee400-107">Das Objekt, das die Eigenschaft enthält.</span><span class="sxs-lookup"><span data-stu-id="ee400-107">The object that contains the property.</span></span>  
  
 `propertyId`  
 <span data-ttu-id="ee400-108">Die ID der Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="ee400-108">The ID of the property.</span></span>  
  
 `useStrictRules`  
 <span data-ttu-id="ee400-109">Der Eigenschaftensatz sollte strikte Regeln für den Modus befolgen.</span><span class="sxs-lookup"><span data-stu-id="ee400-109">The property set should follow strict mode rules.</span></span>  
  
 `result`  
 <span data-ttu-id="ee400-110">Gibt an, ob die Eigenschaft gelöscht wurde.</span><span class="sxs-lookup"><span data-stu-id="ee400-110">Whether the property was deleted.</span></span>  
  
## <span data-ttu-id="ee400-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ee400-111">Return Value</span></span>  
 <span data-ttu-id="ee400-112">Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="ee400-112">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="ee400-113">Hinweise</span><span class="sxs-lookup"><span data-stu-id="ee400-113">Remarks</span></span>  
 <span data-ttu-id="ee400-114">Erfordert einen aktiven Skriptkontext.</span><span class="sxs-lookup"><span data-stu-id="ee400-114">Requires an active script context.</span></span>  
  
## <span data-ttu-id="ee400-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ee400-115">Requirements</span></span>  
 <span data-ttu-id="ee400-116">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="ee400-116">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="ee400-117">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="ee400-117">See Also</span></span>  
 [<span data-ttu-id="ee400-118">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="ee400-118">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)