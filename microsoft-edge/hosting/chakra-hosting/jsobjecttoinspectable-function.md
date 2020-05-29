---
description: Entbindet ein JavaScript-Objekt auf einen `IInspectable` Zeiger.
title: JsObjectToInspectable-Funktion | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 1d15b0b8-516f-4fc6-95aa-2ddd65f8ab75
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: c7127e1cf1372020e0df00b81ed172739379426f
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10568355"
---
# <span data-ttu-id="34ba9-103">JsObjectToInspectable-Funktion</span><span class="sxs-lookup"><span data-stu-id="34ba9-103">JsObjectToInspectable Function</span></span>
<span data-ttu-id="34ba9-104">Entbindet ein JavaScript-Objekt auf einen `IInspectable` Zeiger.</span><span class="sxs-lookup"><span data-stu-id="34ba9-104">Unwraps a JavaScript object to an `IInspectable` pointer.</span></span>  
  
## <span data-ttu-id="34ba9-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="34ba9-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsObjectToInspectable(  
   _In_ JsValueRef value,  
   _Out_ IInspectable  **inspectable  
);  
```  
  
#### <span data-ttu-id="34ba9-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="34ba9-106">Parameters</span></span>  
 `value`  
 <span data-ttu-id="34ba9-107">Ein JavaScript-Wert, auf den projiziert werden soll `IInspectable` .</span><span class="sxs-lookup"><span data-stu-id="34ba9-107">A JavaScript value that should be projected to `IInspectable`.</span></span>  
  
 `inspectable`  
 <span data-ttu-id="34ba9-108">Ein `IInspectable` Wert des Objekts.</span><span class="sxs-lookup"><span data-stu-id="34ba9-108">An `IInspectable` value of the object.</span></span>  
  
## <span data-ttu-id="34ba9-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="34ba9-109">Return Value</span></span>  
 <span data-ttu-id="34ba9-110">Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="34ba9-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="34ba9-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="34ba9-111">Remarks</span></span>  
 <span data-ttu-id="34ba9-112">Hosts sind für das Erzwingen von COM-Threading Regeln verantwortlich.</span><span class="sxs-lookup"><span data-stu-id="34ba9-112">Hosts are responsible for enforcing COM threading rules.</span></span>  
  
 <span data-ttu-id="34ba9-113">Erfordert einen aktiven Skriptkontext.</span><span class="sxs-lookup"><span data-stu-id="34ba9-113">Requires an active script context.</span></span>  
  
 <span data-ttu-id="34ba9-114">Diese API wird nur im EdgeHTML-Modus unterstützt.</span><span class="sxs-lookup"><span data-stu-id="34ba9-114">This API is supported only in EdgeHTML mode.</span></span>  
  
## <span data-ttu-id="34ba9-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="34ba9-115">Requirements</span></span>  
 <span data-ttu-id="34ba9-116">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="34ba9-116">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="34ba9-117">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="34ba9-117">See Also</span></span>  
 [<span data-ttu-id="34ba9-118">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="34ba9-118">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)