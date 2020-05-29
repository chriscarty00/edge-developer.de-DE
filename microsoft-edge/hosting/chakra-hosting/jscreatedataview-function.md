---
description: Erstellt ein JavaScript `DataView` -Objekt.
title: JsCreateDataView-Funktion | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 161e59eb-d429-46f7-9a38-bbf2149ccf44
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 1bf237458e8561b7070e4f3f0d4a14050f028375
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10567306"
---
# <span data-ttu-id="fbd78-103">JsCreateDataView-Funktion</span><span class="sxs-lookup"><span data-stu-id="fbd78-103">JsCreateDataView Function</span></span>
<span data-ttu-id="fbd78-104">Erstellt ein JavaScript `DataView` -Objekt.</span><span class="sxs-lookup"><span data-stu-id="fbd78-104">Creates a Javascript `DataView` object.</span></span>  
  
## <span data-ttu-id="fbd78-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="fbd78-105">Syntax</span></span>  
  
```cpp  
JsErrorCode  JsCreateDataView(  
   _In_ JsValueRef arrayBuffer,  
   _In_ unsigned int byteOffset,  
   _In_ unsigned int byteLength,  
   _Out_ JsValueRef *result  
);  
```  
  
#### <span data-ttu-id="fbd78-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="fbd78-106">Parameters</span></span>  
 `arrayBuffer`  
 <span data-ttu-id="fbd78-107">Ein vorhandenes `ArrayBuffer` Objekt, das als Speicher für das Result-Objekt verwendet werden soll `DataView` .</span><span class="sxs-lookup"><span data-stu-id="fbd78-107">An existing `ArrayBuffer` object to use as the storage for the result `DataView` object.</span></span>  
  
 `byteOffset`  
 <span data-ttu-id="fbd78-108">Der Offset in Bytes vom Anfang des zu vergleichenden `arrayBuffer` Ergebnisses `DataView` .</span><span class="sxs-lookup"><span data-stu-id="fbd78-108">The offset in bytes from the start of `arrayBuffer` for result `DataView` to reference.</span></span>  
  
 `byteLength`  
 <span data-ttu-id="fbd78-109">Die Anzahl der Bytes in der ArrayBuffer für das Ergebnis DataView, auf die verwiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="fbd78-109">The number of bytes in the ArrayBuffer for result DataView to reference.</span></span>  
  
 `result`  
 <span data-ttu-id="fbd78-110">Das neue DataView-Objekt.</span><span class="sxs-lookup"><span data-stu-id="fbd78-110">The new DataView object.</span></span>  
  
## <span data-ttu-id="fbd78-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fbd78-111">Return Value</span></span>  
 <span data-ttu-id="fbd78-112">Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="fbd78-112">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="fbd78-113">Hinweise</span><span class="sxs-lookup"><span data-stu-id="fbd78-113">Remarks</span></span>  
 <span data-ttu-id="fbd78-114">Erfordert einen aktiven Skriptkontext.</span><span class="sxs-lookup"><span data-stu-id="fbd78-114">Requires an active script context.</span></span>  
  
 <span data-ttu-id="fbd78-115">Diese API wird nur im Microsoft Edge-Modus unterstützt.</span><span class="sxs-lookup"><span data-stu-id="fbd78-115">This API is supported only in Microsoft Edge mode.</span></span>  
  
## <span data-ttu-id="fbd78-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fbd78-116">Requirements</span></span>  
 <span data-ttu-id="fbd78-117">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="fbd78-117">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="fbd78-118">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="fbd78-118">See Also</span></span>  
 [<span data-ttu-id="fbd78-119">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="fbd78-119">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)