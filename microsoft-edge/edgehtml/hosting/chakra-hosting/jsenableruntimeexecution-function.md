---
description: 'Aktiviert die Skriptausführung in einer Laufzeit. '
title: JsEnableRuntimeExecution-Funktion | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsEnableRuntimeExecution
helpviewer_keywords:
- JsEnableRuntimeExecution function
ms.assetid: daa2036b-aef6-497d-a8ce-5a006b6ed13f
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: e87191197f70898b2f69d138026edd4e75cd5114
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233950"
---
# <span data-ttu-id="553d0-103">JsEnableRuntimeExecution Funktion</span><span class="sxs-lookup"><span data-stu-id="553d0-103">JsEnableRuntimeExecution Function</span></span>

<span data-ttu-id="553d0-104">Aktiviert die Skriptausführung in einer Laufzeit.</span><span class="sxs-lookup"><span data-stu-id="553d0-104">Enables script execution in a runtime.</span></span>  
  
## <span data-ttu-id="553d0-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="553d0-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsEnableRuntimeExecution(  
   _In_ JsRuntimeHandle runtime  
);  
```  
  
#### <span data-ttu-id="553d0-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="553d0-106">Parameters</span></span>  
 `runtime`  
 <span data-ttu-id="553d0-107">Die Laufzeit, die aktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="553d0-107">The runtime to be enabled.</span></span>  
  
## <span data-ttu-id="553d0-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="553d0-108">Return Value</span></span>  
 <span data-ttu-id="553d0-109">Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="553d0-109">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="553d0-110">Hinweise</span><span class="sxs-lookup"><span data-stu-id="553d0-110">Remarks</span></span>  
 <span data-ttu-id="553d0-111">Das Aktivieren der Skriptausführung in einer Runtime, die bereits die Skriptausführung aktiviert hat, ist ein No-op.</span><span class="sxs-lookup"><span data-stu-id="553d0-111">Enabling script execution in a runtime that already has script execution enabled is a no-op.</span></span>  
  
## <span data-ttu-id="553d0-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="553d0-112">Requirements</span></span>  
 <span data-ttu-id="553d0-113">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="553d0-113">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="553d0-114">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="553d0-114">See Also</span></span>  
 [<span data-ttu-id="553d0-115">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="553d0-115">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
