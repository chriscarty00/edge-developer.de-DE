---
description: Ruft die Laufzeit ab, zu der der Kontext gehört.
title: JsGetRuntime-Funktion | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsGetRuntime
helpviewer_keywords:
- JsGetRuntime function
ms.assetid: 5b62e940-a885-405a-9fdd-0495fb391b95
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 6eeb132dd35fcb5104828bef8e8f27334a5f34e4
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10567246"
---
# <span data-ttu-id="7c26d-103">JsGetRuntime-Funktion</span><span class="sxs-lookup"><span data-stu-id="7c26d-103">JsGetRuntime Function</span></span>
<span data-ttu-id="7c26d-104">Ruft die Laufzeit ab, zu der der Kontext gehört.</span><span class="sxs-lookup"><span data-stu-id="7c26d-104">Gets the runtime that the context belongs to.</span></span>  
  
## <span data-ttu-id="7c26d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="7c26d-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetRuntime(  
   _In_ JsContextRef context,  
   _Out_ JsRuntimeHandle *runtime  
);  
```  
  
#### <span data-ttu-id="7c26d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="7c26d-106">Parameters</span></span>  
 `context`  
 <span data-ttu-id="7c26d-107">Der Kontext, aus dem die Laufzeit abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="7c26d-107">The context to get the runtime from.</span></span>  
  
 `runtime`  
 <span data-ttu-id="7c26d-108">Die Laufzeit, zu der der Kontext gehört.</span><span class="sxs-lookup"><span data-stu-id="7c26d-108">The runtime the context belongs to.</span></span>  
  
## <span data-ttu-id="7c26d-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7c26d-109">Return Value</span></span>  
 <span data-ttu-id="7c26d-110">Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="7c26d-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="7c26d-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7c26d-111">Requirements</span></span>  
 <span data-ttu-id="7c26d-112">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="7c26d-112">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="7c26d-113">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="7c26d-113">See Also</span></span>  
 [<span data-ttu-id="7c26d-114">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="7c26d-114">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)