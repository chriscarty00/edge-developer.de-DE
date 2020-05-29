---
description: Löschen Sie den Wert am angegebenen Index eines Objekts.
title: JsDeleteIndexedProperty-Funktion | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsDeleteIndexedProperty
helpviewer_keywords:
- JsDeleteIndexedProperty function
ms.assetid: cc876839-2ecd-41a8-82d0-c19b3de944e3
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 6148a9c59105749a78ece73578d4b840501c6ecc
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10567273"
---
# <span data-ttu-id="1815c-103">JsDeleteIndexedProperty-Funktion</span><span class="sxs-lookup"><span data-stu-id="1815c-103">JsDeleteIndexedProperty Function</span></span>
<span data-ttu-id="1815c-104">Löschen Sie den Wert am angegebenen Index eines Objekts.</span><span class="sxs-lookup"><span data-stu-id="1815c-104">Delete the value at the specified index of an object.</span></span>  
  
## <span data-ttu-id="1815c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="1815c-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsDeleteIndexedProperty(  
   _In_ JsValueRef object,  
   _In_ JsValueRef index  
);  
```  
  
#### <span data-ttu-id="1815c-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="1815c-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="1815c-107">Das Objekt, das ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="1815c-107">The object to operate on.</span></span>  
  
 `index`  
 <span data-ttu-id="1815c-108">Der zu löschende Index.</span><span class="sxs-lookup"><span data-stu-id="1815c-108">The index to delete.</span></span>  
  
## <span data-ttu-id="1815c-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1815c-109">Return Value</span></span>  
 <span data-ttu-id="1815c-110">Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="1815c-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="1815c-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="1815c-111">Remarks</span></span>  
 <span data-ttu-id="1815c-112">Erfordert einen aktiven Skriptkontext.</span><span class="sxs-lookup"><span data-stu-id="1815c-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="1815c-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1815c-113">Requirements</span></span>  
 <span data-ttu-id="1815c-114">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="1815c-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="1815c-115">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="1815c-115">See Also</span></span>  
 [<span data-ttu-id="1815c-116">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="1815c-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)