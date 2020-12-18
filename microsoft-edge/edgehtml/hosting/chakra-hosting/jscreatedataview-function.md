---
description: Erstellt ein JavaScript `DataView` -Objekt.
title: JsCreateDataView-Funktion | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 161e59eb-d429-46f7-9a38-bbf2149ccf44
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 1d6d170d53f3bfaf885713b6f3abca0b066f8c1d
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233748"
---
# <span data-ttu-id="4d324-103">JsCreateDataView Funktion</span><span class="sxs-lookup"><span data-stu-id="4d324-103">JsCreateDataView Function</span></span>

<span data-ttu-id="4d324-104">Erstellt ein JavaScript `DataView` -Objekt.</span><span class="sxs-lookup"><span data-stu-id="4d324-104">Creates a Javascript `DataView` object.</span></span>  
  
## <span data-ttu-id="4d324-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="4d324-105">Syntax</span></span>  
  
```cpp  
JsErrorCode  JsCreateDataView(  
   _In_ JsValueRef arrayBuffer,  
   _In_ unsigned int byteOffset,  
   _In_ unsigned int byteLength,  
   _Out_ JsValueRef *result  
);  
```  
  
#### <span data-ttu-id="4d324-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="4d324-106">Parameters</span></span>  
 `arrayBuffer`  
 <span data-ttu-id="4d324-107">Ein vorhandenes `ArrayBuffer` Objekt, das als Speicher für das Result-Objekt verwendet werden soll `DataView` .</span><span class="sxs-lookup"><span data-stu-id="4d324-107">An existing `ArrayBuffer` object to use as the storage for the result `DataView` object.</span></span>  
  
 `byteOffset`  
 <span data-ttu-id="4d324-108">Der Offset in Bytes vom Anfang des zu vergleichenden `arrayBuffer` Ergebnisses `DataView` .</span><span class="sxs-lookup"><span data-stu-id="4d324-108">The offset in bytes from the start of `arrayBuffer` for result `DataView` to reference.</span></span>  
  
 `byteLength`  
 <span data-ttu-id="4d324-109">Die Anzahl der Bytes in der ArrayBuffer für das Ergebnis DataView, auf die verwiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="4d324-109">The number of bytes in the ArrayBuffer for result DataView to reference.</span></span>  
  
 `result`  
 <span data-ttu-id="4d324-110">Das neue DataView-Objekt.</span><span class="sxs-lookup"><span data-stu-id="4d324-110">The new DataView object.</span></span>  
  
## <span data-ttu-id="4d324-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4d324-111">Return Value</span></span>  
 <span data-ttu-id="4d324-112">Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="4d324-112">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="4d324-113">Hinweise</span><span class="sxs-lookup"><span data-stu-id="4d324-113">Remarks</span></span>  
 <span data-ttu-id="4d324-114">Erfordert einen aktiven Skriptkontext.</span><span class="sxs-lookup"><span data-stu-id="4d324-114">Requires an active script context.</span></span>  
  
 <span data-ttu-id="4d324-115">Diese API wird nur im Microsoft Edge-Modus unterstützt.</span><span class="sxs-lookup"><span data-stu-id="4d324-115">This API is supported only in Microsoft Edge mode.</span></span>  
  
## <span data-ttu-id="4d324-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4d324-116">Requirements</span></span>  
 <span data-ttu-id="4d324-117">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="4d324-117">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="4d324-118">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="4d324-118">See Also</span></span>  
 [<span data-ttu-id="4d324-119">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="4d324-119">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
