---
description: Ruft die Liste aller Symbol Eigenschaften für das Objekt ab.
title: JsGetOwnPropertySymbols-Funktion | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 57c431e3-de0b-4ed0-b750-87a86448daff
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: c7a7f4e88986a45fbccfae0c53e92ff2e5313991
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10568384"
---
# <span data-ttu-id="2b76f-103">JsGetOwnPropertySymbols-Funktion</span><span class="sxs-lookup"><span data-stu-id="2b76f-103">JsGetOwnPropertySymbols Function</span></span>
<span data-ttu-id="2b76f-104">Ruft die Liste aller Symbol Eigenschaften für das Objekt ab.</span><span class="sxs-lookup"><span data-stu-id="2b76f-104">Gets the list of all symbol properties on the object.</span></span>  
  
## <span data-ttu-id="2b76f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="2b76f-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetOwnPropertySymbols(  
   _In_ JsValueRef object,  
   _Out_ JsValueRef *propertySymbols  
);  
```  
  
#### <span data-ttu-id="2b76f-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="2b76f-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="2b76f-107">Das Objekt, aus dem die Eigenschaften Symbole abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="2b76f-107">The object from which to get the property symbols.</span></span>  
  
 `propertySymbols`  
 <span data-ttu-id="2b76f-108">Ein Array von Eigenschafts Symbolen.</span><span class="sxs-lookup"><span data-stu-id="2b76f-108">An array of property symbols.</span></span>  
  
## <span data-ttu-id="2b76f-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2b76f-109">Return Value</span></span>  
 <span data-ttu-id="2b76f-110">Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="2b76f-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="2b76f-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="2b76f-111">Remarks</span></span>  
 <span data-ttu-id="2b76f-112">Erfordert einen aktiven Skriptkontext.</span><span class="sxs-lookup"><span data-stu-id="2b76f-112">Requires an active script context.</span></span>  
  
 <span data-ttu-id="2b76f-113">Diese API wird nur im Microsoft Edge-Modus unterstützt.</span><span class="sxs-lookup"><span data-stu-id="2b76f-113">This API is supported only in Microsoft Edge mode.</span></span>  
  
## <span data-ttu-id="2b76f-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2b76f-114">Requirements</span></span>  
 <span data-ttu-id="2b76f-115">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="2b76f-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="2b76f-116">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="2b76f-116">See Also</span></span>  
 [<span data-ttu-id="2b76f-117">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="2b76f-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)