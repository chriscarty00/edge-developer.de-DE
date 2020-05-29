---
description: Gibt einen Verweis auf ein Garbage Collection-Objekt frei.
title: JsRelease-Funktion | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsRelease
helpviewer_keywords:
- JsRelease function
ms.assetid: 8714fd0b-5b66-48e0-927e-7b93af6cde7b
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 134ba16509b6c2f0c232214d7efba4d8c8915d43
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10568339"
---
# <span data-ttu-id="5afcf-103">JsRelease-Funktion</span><span class="sxs-lookup"><span data-stu-id="5afcf-103">JsRelease Function</span></span>
<span data-ttu-id="5afcf-104">Gibt einen Verweis auf ein Garbage Collection-Objekt frei.</span><span class="sxs-lookup"><span data-stu-id="5afcf-104">Releases a reference to a garbage collected object.</span></span>  
  
## <span data-ttu-id="5afcf-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="5afcf-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsRelease(  
   _In_ JsRef ref,  
   _Out_opt_ unsigned int *count  
);  
```  
  
#### <span data-ttu-id="5afcf-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="5afcf-106">Parameters</span></span>  
 `ref`  
 <span data-ttu-id="5afcf-107">Das Objekt, auf das ein Verweis hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="5afcf-107">The object to add a reference to.</span></span>  
  
 `count`  
 <span data-ttu-id="5afcf-108">Der neue Verweiszähler des Objekts (kann NULL übergeben).</span><span class="sxs-lookup"><span data-stu-id="5afcf-108">The object's new reference count (can pass in null).</span></span>  
  
## <span data-ttu-id="5afcf-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5afcf-109">Return Value</span></span>  
 <span data-ttu-id="5afcf-110">Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="5afcf-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="5afcf-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="5afcf-111">Remarks</span></span>  
 <span data-ttu-id="5afcf-112">Entfernt einen Verweis auf ein `JsRef` handle, das von erstellt wurde `JsAddRef` .</span><span class="sxs-lookup"><span data-stu-id="5afcf-112">Removes a reference to a `JsRef` handle that was created by `JsAddRef`.</span></span>  
  
## <span data-ttu-id="5afcf-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5afcf-113">Requirements</span></span>  
 <span data-ttu-id="5afcf-114">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="5afcf-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="5afcf-115">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="5afcf-115">See Also</span></span>  
 [<span data-ttu-id="5afcf-116">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="5afcf-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)