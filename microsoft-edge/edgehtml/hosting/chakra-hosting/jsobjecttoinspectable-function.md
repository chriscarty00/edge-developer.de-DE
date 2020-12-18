---
description: Entbindet ein JavaScript-Objekt auf einen `IInspectable` Zeiger.
title: JsObjectToInspectable-Funktion | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 1d15b0b8-516f-4fc6-95aa-2ddd65f8ab75
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 0d818f798805e2afad4dc87b308258464d31bf92
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11234081"
---
# <span data-ttu-id="680f4-103">JsObjectToInspectable Funktion</span><span class="sxs-lookup"><span data-stu-id="680f4-103">JsObjectToInspectable Function</span></span>

<span data-ttu-id="680f4-104">Entbindet ein JavaScript-Objekt auf einen `IInspectable` Zeiger.</span><span class="sxs-lookup"><span data-stu-id="680f4-104">Unwraps a JavaScript object to an `IInspectable` pointer.</span></span>  
  
## <span data-ttu-id="680f4-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="680f4-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsObjectToInspectable(  
   _In_ JsValueRef value,  
   _Out_ IInspectable  **inspectable  
);  
```  
  
#### <span data-ttu-id="680f4-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="680f4-106">Parameters</span></span>  
 `value`  
 <span data-ttu-id="680f4-107">Ein JavaScript-Wert, auf den projiziert werden soll `IInspectable` .</span><span class="sxs-lookup"><span data-stu-id="680f4-107">A JavaScript value that should be projected to `IInspectable`.</span></span>  
  
 `inspectable`  
 <span data-ttu-id="680f4-108">Ein `IInspectable` Wert des Objekts.</span><span class="sxs-lookup"><span data-stu-id="680f4-108">An `IInspectable` value of the object.</span></span>  
  
## <span data-ttu-id="680f4-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="680f4-109">Return Value</span></span>  
 <span data-ttu-id="680f4-110">Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="680f4-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="680f4-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="680f4-111">Remarks</span></span>  
 <span data-ttu-id="680f4-112">Hosts sind für das Erzwingen von COM-Threading Regeln verantwortlich.</span><span class="sxs-lookup"><span data-stu-id="680f4-112">Hosts are responsible for enforcing COM threading rules.</span></span>  
  
 <span data-ttu-id="680f4-113">Erfordert einen aktiven Skriptkontext.</span><span class="sxs-lookup"><span data-stu-id="680f4-113">Requires an active script context.</span></span>  
  
 <span data-ttu-id="680f4-114">Diese API wird nur im EdgeHTML-Modus unterstützt.</span><span class="sxs-lookup"><span data-stu-id="680f4-114">This API is supported only in EdgeHTML mode.</span></span>  
  
## <span data-ttu-id="680f4-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="680f4-115">Requirements</span></span>  
 <span data-ttu-id="680f4-116">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="680f4-116">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="680f4-117">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="680f4-117">See Also</span></span>  
 [<span data-ttu-id="680f4-118">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="680f4-118">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
