---
description: Erstellt ein neues Objekt, in dem einige externe Daten gespeichert werden.
title: JsCreateExternalObject-Funktion | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsCreateExternalObject
helpviewer_keywords:
- JsCreateExternalObject function
ms.assetid: 6bcef506-93fb-429b-b06a-a971ff0b71f3
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 9a68f4befea7dc7c3369bcade475e29d53342730
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10567299"
---
# <span data-ttu-id="2f963-103">JsCreateExternalObject-Funktion</span><span class="sxs-lookup"><span data-stu-id="2f963-103">JsCreateExternalObject Function</span></span>
<span data-ttu-id="2f963-104">Erstellt ein neues Objekt, in dem einige externe Daten gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="2f963-104">Creates a new object that stores some external data.</span></span>
  
## <span data-ttu-id="2f963-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="2f963-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsCreateExternalObject(  
   _In_opt_ void *data,  
   _In_opt_ JsFinalizeCallback finalizeCallback,  
   _Out_ JsValueRef *object  
);  
```  
  
#### <span data-ttu-id="2f963-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="2f963-106">Parameters</span></span>  
 `data`  
 <span data-ttu-id="2f963-107">Externe Daten, die das Objekt darstellen soll.</span><span class="sxs-lookup"><span data-stu-id="2f963-107">External data that the object will represent.</span></span> <span data-ttu-id="2f963-108">Kann NULL sein.</span><span class="sxs-lookup"><span data-stu-id="2f963-108">May be null.</span></span>  
  
 `finalizeCallback`  
 <span data-ttu-id="2f963-109">Ein Rückruf für den Zeitpunkt, zu dem das Objekt finalisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="2f963-109">A callback for when the object is finalized.</span></span> <span data-ttu-id="2f963-110">Kann NULL sein.</span><span class="sxs-lookup"><span data-stu-id="2f963-110">May be null.</span></span>  
  
 `object`  
 <span data-ttu-id="2f963-111">Das neue Objekt.</span><span class="sxs-lookup"><span data-stu-id="2f963-111">The new object.</span></span>  
  
## <span data-ttu-id="2f963-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2f963-112">Return Value</span></span>  
 <span data-ttu-id="2f963-113">Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="2f963-113">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="2f963-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="2f963-114">Remarks</span></span>  
 <span data-ttu-id="2f963-115">Erfordert einen aktiven Skriptkontext.</span><span class="sxs-lookup"><span data-stu-id="2f963-115">Requires an active script context.</span></span>  
  
## <span data-ttu-id="2f963-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2f963-116">Requirements</span></span>  
 <span data-ttu-id="2f963-117">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="2f963-117">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="2f963-118">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="2f963-118">See Also</span></span>  
 [<span data-ttu-id="2f963-119">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="2f963-119">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)