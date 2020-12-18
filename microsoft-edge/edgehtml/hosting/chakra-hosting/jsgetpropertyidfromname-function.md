---
description: Ruft die dem Namen zugeordnete Eigenschafts-ID ab.
title: JsGetPropertyIdFromName-Funktion | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsGetPropertyIdFromName
helpviewer_keywords:
- JsGetPropertyIdFromName function
ms.assetid: 1674906f-746a-4c62-99cd-023276683a86
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: adc8de4d55fa0c74ad191b4621ceb3a54026d02d
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11234102"
---
# <span data-ttu-id="9c323-103">JsGetPropertyIdFromName Funktion</span><span class="sxs-lookup"><span data-stu-id="9c323-103">JsGetPropertyIdFromName Function</span></span>

<span data-ttu-id="9c323-104">Ruft die dem Namen zugeordnete Eigenschafts-ID ab.</span><span class="sxs-lookup"><span data-stu-id="9c323-104">Gets the property ID associated with the name.</span></span>  
  
## <span data-ttu-id="9c323-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="9c323-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetPropertyIdFromName(  
   _In_z_ const wchar_t *name,  
   _Out_ JsPropertyIdRef *propertyId  
);  
```  
  
#### <span data-ttu-id="9c323-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="9c323-106">Parameters</span></span>  
 `name`  
 <span data-ttu-id="9c323-107">Der Name der Eigenschafts-ID, die abgerufen oder erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="9c323-107">The name of the property ID to get or create.</span></span> <span data-ttu-id="9c323-108">Der Name kann nur aus Ziffern bestehen.</span><span class="sxs-lookup"><span data-stu-id="9c323-108">The name may consist of only digits.</span></span>  
  
 `propertyId`  
 <span data-ttu-id="9c323-109">Die Eigenschafts-ID in dieser Runtime für den angegebenen Namen.</span><span class="sxs-lookup"><span data-stu-id="9c323-109">The property ID in this runtime for the given name.</span></span>  
  
## <span data-ttu-id="9c323-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9c323-110">Return Value</span></span>  
 <span data-ttu-id="9c323-111">Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="9c323-111">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="9c323-112">Hinweise</span><span class="sxs-lookup"><span data-stu-id="9c323-112">Remarks</span></span>  
 <span data-ttu-id="9c323-113">Eigenschafts-IDs sind für einen kontextspezifisch und können nicht in allen Kontexten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9c323-113">Property IDs are specific to a context and cannot be used across contexts.</span></span>  
  
 <span data-ttu-id="9c323-114">Erfordert einen aktiven Skriptkontext.</span><span class="sxs-lookup"><span data-stu-id="9c323-114">Requires an active script context.</span></span>  
  
## <span data-ttu-id="9c323-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9c323-115">Requirements</span></span>  
 <span data-ttu-id="9c323-116">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="9c323-116">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="9c323-117">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="9c323-117">See Also</span></span>  
 [<span data-ttu-id="9c323-118">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="9c323-118">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
