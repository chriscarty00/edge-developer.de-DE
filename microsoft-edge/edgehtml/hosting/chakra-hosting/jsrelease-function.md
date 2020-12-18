---
description: Gibt einen Verweis auf ein Garbage Collection-Objekt frei.
title: JsRelease-Funktion | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsRelease
helpviewer_keywords:
- JsRelease function
ms.assetid: 8714fd0b-5b66-48e0-927e-7b93af6cde7b
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 46552a03dc56a10b1d258d8c33da1c533f38464a
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233732"
---
# <span data-ttu-id="e94e8-103">JsRelease Funktion</span><span class="sxs-lookup"><span data-stu-id="e94e8-103">JsRelease Function</span></span>

<span data-ttu-id="e94e8-104">Gibt einen Verweis auf ein Garbage Collection-Objekt frei.</span><span class="sxs-lookup"><span data-stu-id="e94e8-104">Releases a reference to a garbage collected object.</span></span>  
  
## <span data-ttu-id="e94e8-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e94e8-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsRelease(  
   _In_ JsRef ref,  
   _Out_opt_ unsigned int *count  
);  
```  
  
#### <span data-ttu-id="e94e8-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="e94e8-106">Parameters</span></span>  
 `ref`  
 <span data-ttu-id="e94e8-107">Das Objekt, auf das ein Verweis hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="e94e8-107">The object to add a reference to.</span></span>  
  
 `count`  
 <span data-ttu-id="e94e8-108">Der neue Verweiszähler des Objekts (kann NULL übergeben).</span><span class="sxs-lookup"><span data-stu-id="e94e8-108">The object's new reference count (can pass in null).</span></span>  
  
## <span data-ttu-id="e94e8-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e94e8-109">Return Value</span></span>  
 <span data-ttu-id="e94e8-110">Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="e94e8-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="e94e8-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="e94e8-111">Remarks</span></span>  
 <span data-ttu-id="e94e8-112">Entfernt einen Verweis auf ein `JsRef` handle, das von erstellt wurde `JsAddRef` .</span><span class="sxs-lookup"><span data-stu-id="e94e8-112">Removes a reference to a `JsRef` handle that was created by `JsAddRef`.</span></span>  
  
## <span data-ttu-id="e94e8-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e94e8-113">Requirements</span></span>  
 <span data-ttu-id="e94e8-114">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="e94e8-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="e94e8-115">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="e94e8-115">See Also</span></span>  
 [<span data-ttu-id="e94e8-116">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="e94e8-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
