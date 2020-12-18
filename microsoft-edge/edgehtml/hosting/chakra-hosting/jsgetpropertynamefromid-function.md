---
description: Ruft den Namen ab, der der Eigenschafts-ID zugeordnet ist.
title: JsGetPropertyNameFromId-Funktion | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsGetPropertyNameFromId
helpviewer_keywords:
- JsGetPropertyNameFromId function
ms.assetid: b4ca442c-573d-4bc3-adf7-1b8d48480b3a
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 42061ab54a70fed571740961a909a6da17fb0733
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233964"
---
# <span data-ttu-id="4a6b1-103">JsGetPropertyNameFromId Funktion</span><span class="sxs-lookup"><span data-stu-id="4a6b1-103">JsGetPropertyNameFromId Function</span></span>

<span data-ttu-id="4a6b1-104">Ruft den Namen ab, der der Eigenschafts-ID zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="4a6b1-104">Gets the name associated with the property ID.</span></span>  
  
## <span data-ttu-id="4a6b1-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="4a6b1-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetPropertyNameFromId(  
   _In_ JsPropertyIdRef propertyId,  
   _Outptr_result_z_ const wchar_t **name  
);  
```  
  
#### <span data-ttu-id="4a6b1-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="4a6b1-106">Parameters</span></span>  
 `propertyId`  
 <span data-ttu-id="4a6b1-107">Die Eigenschafts-ID, deren Name abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="4a6b1-107">The property ID to get the name of.</span></span>  
  
 `name`  
 <span data-ttu-id="4a6b1-108">Der Name, der der Eigenschafts-ID zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="4a6b1-108">The name associated with the property ID.</span></span>  
  
## <span data-ttu-id="4a6b1-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4a6b1-109">Return Value</span></span>  
 <span data-ttu-id="4a6b1-110">Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="4a6b1-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="4a6b1-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="4a6b1-111">Remarks</span></span>  
 <span data-ttu-id="4a6b1-112">Erfordert einen aktiven Skriptkontext.</span><span class="sxs-lookup"><span data-stu-id="4a6b1-112">Requires an active script context.</span></span>  
  
 <span data-ttu-id="4a6b1-113">Der zurückgegebene Puffer ist gültig, solange die Laufzeit aktiv ist, und kann nicht verwendet werden, nachdem die Laufzeit freigegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="4a6b1-113">The returned buffer is valid as long as the runtime is alive and cannot be used once the runtime has been disposed.</span></span>  
  
## <span data-ttu-id="4a6b1-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4a6b1-114">Requirements</span></span>  
 <span data-ttu-id="4a6b1-115">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="4a6b1-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="4a6b1-116">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="4a6b1-116">See Also</span></span>  
 [<span data-ttu-id="4a6b1-117">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="4a6b1-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
