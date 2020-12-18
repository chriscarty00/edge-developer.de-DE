---
description: Bestimmt, ob ein Objekt seine indizierten Eigenschaften in externen Daten aufweist.
title: JsHasIndexedPropertiesExternalData-Funktion | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: c676db20-3ef1-4f84-8b26-3e06fe0ab2bf
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: e6395bacb15904bc3f2e74d22959844e8e0af373
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11234250"
---
# <span data-ttu-id="1ed67-103">JsHasIndexedPropertiesExternalData Funktion</span><span class="sxs-lookup"><span data-stu-id="1ed67-103">JsHasIndexedPropertiesExternalData Function</span></span>

<span data-ttu-id="1ed67-104">Bestimmt, ob ein Objekt seine indizierten Eigenschaften in externen Daten aufweist.</span><span class="sxs-lookup"><span data-stu-id="1ed67-104">Determines whether an object has its indexed properties in external data.</span></span>  
  
## <span data-ttu-id="1ed67-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="1ed67-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsHasIndexedPropertiesExternalData(  
   _In_ JsValueRef object,  
   _Out_ bool* value  
);  
```  
  
#### <span data-ttu-id="1ed67-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="1ed67-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="1ed67-107">Das Objekt.</span><span class="sxs-lookup"><span data-stu-id="1ed67-107">The object.</span></span>  
  
 `value`  
 <span data-ttu-id="1ed67-108">Gibt an, ob das Objekt seine indizierten Eigenschaften in externen Daten hat.</span><span class="sxs-lookup"><span data-stu-id="1ed67-108">Whether the object has its indexed properties in external data.</span></span>  
  
## <span data-ttu-id="1ed67-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1ed67-109">Return Value</span></span>  
 <span data-ttu-id="1ed67-110">Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="1ed67-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="1ed67-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="1ed67-111">Remarks</span></span>  
 <span data-ttu-id="1ed67-112">Diese API wird nur im Microsoft Edge-Modus unterstützt.</span><span class="sxs-lookup"><span data-stu-id="1ed67-112">This API is supported only in Microsoft Edge mode.</span></span>  
  
## <span data-ttu-id="1ed67-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1ed67-113">Requirements</span></span>  
 <span data-ttu-id="1ed67-114">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="1ed67-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="1ed67-115">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="1ed67-115">See Also</span></span>  
 [<span data-ttu-id="1ed67-116">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="1ed67-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
