---
description: Legt den aktuellen Skriptkontext für den Thread fest.
title: JsSetCurrentContext-Funktion | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsSetCurrentContext
helpviewer_keywords:
- JsSetCurrentContext function
ms.assetid: 603cc94c-6585-411b-89f9-c6f144e2aa30
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 57620ad0e986034791ec07765d7cc115b958d661
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10568317"
---
# <span data-ttu-id="fe986-103">JsSetCurrentContext-Funktion</span><span class="sxs-lookup"><span data-stu-id="fe986-103">JsSetCurrentContext Function</span></span>
<span data-ttu-id="fe986-104">Legt den aktuellen Skriptkontext für den Thread fest.</span><span class="sxs-lookup"><span data-stu-id="fe986-104">Sets the current script context on the thread.</span></span>  
  
## <span data-ttu-id="fe986-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="fe986-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsSetCurrentContext(  
   _In_ JsContextRef context  
);  
```  
  
#### <span data-ttu-id="fe986-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="fe986-106">Parameters</span></span>  
 `context`  
 <span data-ttu-id="fe986-107">Der Skriptkontext, um Current zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="fe986-107">The script context to make current.</span></span>  
  
## <span data-ttu-id="fe986-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fe986-108">Return Value</span></span>  
 <span data-ttu-id="fe986-109">Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="fe986-109">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  

## <span data-ttu-id="fe986-110">Beispiel</span><span class="sxs-lookup"><span data-stu-id="fe986-110">Example</span></span>

```cpp
JsRuntimeHandle runtime;
JsContextRef context;

// Create a runtime.
JsCreateRuntime(JsRuntimeAttributeNone, nullptr, &runtime);

// Create an execution context.
JsCreateContext(runtime, &context);

// Now set the current execution context.
JsSetCurrentContext(context);
```

## <span data-ttu-id="fe986-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fe986-111">Requirements</span></span>  
 <span data-ttu-id="fe986-112">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="fe986-112">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="fe986-113">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="fe986-113">See Also</span></span>  
 [<span data-ttu-id="fe986-114">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="fe986-114">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)