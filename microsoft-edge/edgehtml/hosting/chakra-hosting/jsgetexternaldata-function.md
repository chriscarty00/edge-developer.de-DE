---
description: Ruft die Daten eines externen Objekts ab.
title: JsGetExternalData-Funktion | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsGetExternalData
helpviewer_keywords:
- JsGetExternalData function
ms.assetid: 1919e1da-3ea7-4269-a5fb-a3be06bd029b
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: d046b5c515b1a688cd527fdc0eb9cd173eb47570
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233996"
---
# <span data-ttu-id="8e202-103">JsGetExternalData Funktion</span><span class="sxs-lookup"><span data-stu-id="8e202-103">JsGetExternalData Function</span></span>

<span data-ttu-id="8e202-104">Ruft die Daten eines externen Objekts ab.</span><span class="sxs-lookup"><span data-stu-id="8e202-104">Retrieves the data from an external object.</span></span>  
  
## <span data-ttu-id="8e202-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="8e202-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetExternalData(  
   _In_ JsValueRef object,  
   _Out_ void **externalData  
);  
```  
  
#### <span data-ttu-id="8e202-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="8e202-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="8e202-107">Das externe Objekt.</span><span class="sxs-lookup"><span data-stu-id="8e202-107">The external object.</span></span>  
  
 `externalData`  
 <span data-ttu-id="8e202-108">Die im Objekt gespeicherten externen Daten.</span><span class="sxs-lookup"><span data-stu-id="8e202-108">The external data stored in the object.</span></span> <span data-ttu-id="8e202-109">Kann NULL sein, wenn keine externen Daten im Objekt gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="8e202-109">Can be null if no external data is stored in the object.</span></span>  
  
## <span data-ttu-id="8e202-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8e202-110">Return Value</span></span>  
 <span data-ttu-id="8e202-111">Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="8e202-111">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="8e202-112">Hinweise</span><span class="sxs-lookup"><span data-stu-id="8e202-112">Remarks</span></span>  
 <span data-ttu-id="8e202-113">Erfordert einen aktiven Skriptkontext.</span><span class="sxs-lookup"><span data-stu-id="8e202-113">Requires an active script context.</span></span>  
  
## <span data-ttu-id="8e202-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8e202-114">Requirements</span></span>  
 <span data-ttu-id="8e202-115">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="8e202-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="8e202-116">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="8e202-116">See Also</span></span>  
 [<span data-ttu-id="8e202-117">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="8e202-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
