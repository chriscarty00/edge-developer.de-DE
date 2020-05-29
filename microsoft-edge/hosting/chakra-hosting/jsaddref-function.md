---
description: Fügt einen Verweis auf ein Garbage Collected-Objekt hinzu.
title: JsAddRef-Funktion | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsAddRef
helpviewer_keywords:
- JsAddRef function
ms.assetid: a7f3ed49-6a86-489a-abdf-c99428e79cae
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: bd02dded6dc2877228f22b4d2800e41a78163467
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10567337"
---
# <span data-ttu-id="4369b-103">JsAddRef-Funktion</span><span class="sxs-lookup"><span data-stu-id="4369b-103">JsAddRef Function</span></span>
<span data-ttu-id="4369b-104">Fügt einen Verweis auf ein Garbage Collected-Objekt hinzu.</span><span class="sxs-lookup"><span data-stu-id="4369b-104">Adds a reference to a garbage collected object.</span></span>  
  
## <span data-ttu-id="4369b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="4369b-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsAddRef(  
   _In_ JsRef ref,  
   _Out_opt_ unsigned int *count  
);  
```  
  
#### <span data-ttu-id="4369b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="4369b-106">Parameters</span></span>  
 `ref`  
 <span data-ttu-id="4369b-107">Das Objekt, auf das ein Verweis hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="4369b-107">The object to add a reference to.</span></span>  
  
 `count`  
 <span data-ttu-id="4369b-108">Der neue Verweiszähler des Objekts (kann NULL übergeben).</span><span class="sxs-lookup"><span data-stu-id="4369b-108">The object's new reference count (can pass in null).</span></span>  
  
## <span data-ttu-id="4369b-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4369b-109">Return Value</span></span>  
 <span data-ttu-id="4369b-110">Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="4369b-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="4369b-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="4369b-111">Remarks</span></span>  
 <span data-ttu-id="4369b-112">Dies muss nur für `JsRef` Handles aufgerufen werden, die nicht irgendwo auf dem Stapel gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="4369b-112">This only needs to be called on `JsRef` handles that are not going to be stored somewhere on the stack.</span></span> <span data-ttu-id="4369b-113">Durch das Aufrufen wird `JsAddRef` sichergestellt, dass das Objekt `JsRef` , auf das verwiesen wird, erst `JsRelease` aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="4369b-113">Calling `JsAddRef` ensures that the object the `JsRef` refers to will not be freed until `JsRelease` is called.</span></span>  
  
## <span data-ttu-id="4369b-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4369b-114">Requirements</span></span>  
 <span data-ttu-id="4369b-115">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="4369b-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="4369b-116">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="4369b-116">See Also</span></span>  
 [<span data-ttu-id="4369b-117">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="4369b-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)