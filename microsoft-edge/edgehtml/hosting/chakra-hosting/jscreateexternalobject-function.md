---
description: Erstellt ein neues Objekt, in dem einige externe Daten gespeichert werden.
title: JsCreateExternalObject-Funktion | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsCreateExternalObject
helpviewer_keywords:
- JsCreateExternalObject function
ms.assetid: 6bcef506-93fb-429b-b06a-a971ff0b71f3
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 4d402c3d379a16186daaba601c7f830c53a9a953
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11234264"
---
# <span data-ttu-id="86406-103">JsCreateExternalObject Funktion</span><span class="sxs-lookup"><span data-stu-id="86406-103">JsCreateExternalObject Function</span></span>

<span data-ttu-id="86406-104">Erstellt ein neues Objekt, in dem einige externe Daten gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="86406-104">Creates a new object that stores some external data.</span></span>
  
## <span data-ttu-id="86406-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="86406-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsCreateExternalObject(  
   _In_opt_ void *data,  
   _In_opt_ JsFinalizeCallback finalizeCallback,  
   _Out_ JsValueRef *object  
);  
```  
  
#### <span data-ttu-id="86406-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="86406-106">Parameters</span></span>  
 `data`  
 <span data-ttu-id="86406-107">Externe Daten, die das Objekt darstellen soll.</span><span class="sxs-lookup"><span data-stu-id="86406-107">External data that the object will represent.</span></span> <span data-ttu-id="86406-108">Kann NULL sein.</span><span class="sxs-lookup"><span data-stu-id="86406-108">May be null.</span></span>  
  
 `finalizeCallback`  
 <span data-ttu-id="86406-109">Ein Rückruf für den Zeitpunkt, zu dem das Objekt finalisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="86406-109">A callback for when the object is finalized.</span></span> <span data-ttu-id="86406-110">Kann NULL sein.</span><span class="sxs-lookup"><span data-stu-id="86406-110">May be null.</span></span>  
  
 `object`  
 <span data-ttu-id="86406-111">Das neue Objekt.</span><span class="sxs-lookup"><span data-stu-id="86406-111">The new object.</span></span>  
  
## <span data-ttu-id="86406-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="86406-112">Return Value</span></span>  
 <span data-ttu-id="86406-113">Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="86406-113">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="86406-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="86406-114">Remarks</span></span>  
 <span data-ttu-id="86406-115">Erfordert einen aktiven Skriptkontext.</span><span class="sxs-lookup"><span data-stu-id="86406-115">Requires an active script context.</span></span>  
  
## <span data-ttu-id="86406-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="86406-116">Requirements</span></span>  
 <span data-ttu-id="86406-117">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="86406-117">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="86406-118">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="86406-118">See Also</span></span>  
 [<span data-ttu-id="86406-119">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="86406-119">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
