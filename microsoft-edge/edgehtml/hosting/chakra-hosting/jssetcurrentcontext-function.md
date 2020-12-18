---
description: Legt den aktuellen Skriptkontext für den Thread fest.
title: JsSetCurrentContext-Funktion | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsSetCurrentContext
helpviewer_keywords:
- JsSetCurrentContext function
ms.assetid: 603cc94c-6585-411b-89f9-c6f144e2aa30
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 60ec1760c582f1f6771a5af64f59c4a77b1a43f8
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233910"
---
# <span data-ttu-id="43f93-103">JsSetCurrentContext Funktion</span><span class="sxs-lookup"><span data-stu-id="43f93-103">JsSetCurrentContext Function</span></span>

<span data-ttu-id="43f93-104">Legt den aktuellen Skriptkontext für den Thread fest.</span><span class="sxs-lookup"><span data-stu-id="43f93-104">Sets the current script context on the thread.</span></span>  
  
## <span data-ttu-id="43f93-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="43f93-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsSetCurrentContext(  
   _In_ JsContextRef context  
);  
```  
  
#### <span data-ttu-id="43f93-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="43f93-106">Parameters</span></span>  
 `context`  
 <span data-ttu-id="43f93-107">Der Skriptkontext, um Current zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="43f93-107">The script context to make current.</span></span>  
  
## <span data-ttu-id="43f93-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="43f93-108">Return Value</span></span>  
 <span data-ttu-id="43f93-109">Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="43f93-109">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  

## <span data-ttu-id="43f93-110">Beispiel</span><span class="sxs-lookup"><span data-stu-id="43f93-110">Example</span></span>

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

## <span data-ttu-id="43f93-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="43f93-111">Requirements</span></span>  
 <span data-ttu-id="43f93-112">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="43f93-112">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="43f93-113">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="43f93-113">See Also</span></span>  
 [<span data-ttu-id="43f93-114">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="43f93-114">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
