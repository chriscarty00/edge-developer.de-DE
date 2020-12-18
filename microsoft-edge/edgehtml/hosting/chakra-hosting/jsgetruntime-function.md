---
description: Ruft die Laufzeit ab, zu der der Kontext gehört.
title: JsGetRuntime-Funktion | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsGetRuntime
helpviewer_keywords:
- JsGetRuntime function
ms.assetid: 5b62e940-a885-405a-9fdd-0495fb391b95
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 49739f0cf3675a44b9fc328e3eaa7d49c6282e53
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233965"
---
# <span data-ttu-id="51509-103">JsGetRuntime Funktion</span><span class="sxs-lookup"><span data-stu-id="51509-103">JsGetRuntime Function</span></span>

<span data-ttu-id="51509-104">Ruft die Laufzeit ab, zu der der Kontext gehört.</span><span class="sxs-lookup"><span data-stu-id="51509-104">Gets the runtime that the context belongs to.</span></span>  
  
## <span data-ttu-id="51509-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="51509-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetRuntime(  
   _In_ JsContextRef context,  
   _Out_ JsRuntimeHandle *runtime  
);  
```  
  
#### <span data-ttu-id="51509-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="51509-106">Parameters</span></span>  
 `context`  
 <span data-ttu-id="51509-107">Der Kontext, aus dem die Laufzeit abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="51509-107">The context to get the runtime from.</span></span>  
  
 `runtime`  
 <span data-ttu-id="51509-108">Die Laufzeit, zu der der Kontext gehört.</span><span class="sxs-lookup"><span data-stu-id="51509-108">The runtime the context belongs to.</span></span>  
  
## <span data-ttu-id="51509-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="51509-109">Return Value</span></span>  
 <span data-ttu-id="51509-110">Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="51509-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="51509-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="51509-111">Requirements</span></span>  
 <span data-ttu-id="51509-112">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="51509-112">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="51509-113">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="51509-113">See Also</span></span>  
 [<span data-ttu-id="51509-114">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="51509-114">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
