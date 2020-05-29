---
description: 'Aktiviert die Skriptausführung in einer Laufzeit. '
title: JsEnableRuntimeExecution-Funktion | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsEnableRuntimeExecution
helpviewer_keywords:
- JsEnableRuntimeExecution function
ms.assetid: daa2036b-aef6-497d-a8ce-5a006b6ed13f
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: dd8071fd3c120d1c2029a3c7a3d9c39e68c4cfd2
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10568407"
---
# <span data-ttu-id="49971-103">JsEnableRuntimeExecution-Funktion</span><span class="sxs-lookup"><span data-stu-id="49971-103">JsEnableRuntimeExecution Function</span></span>
<span data-ttu-id="49971-104">Aktiviert die Skriptausführung in einer Laufzeit.</span><span class="sxs-lookup"><span data-stu-id="49971-104">Enables script execution in a runtime.</span></span>  
  
## <span data-ttu-id="49971-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="49971-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsEnableRuntimeExecution(  
   _In_ JsRuntimeHandle runtime  
);  
```  
  
#### <span data-ttu-id="49971-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="49971-106">Parameters</span></span>  
 `runtime`  
 <span data-ttu-id="49971-107">Die Laufzeit, die aktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="49971-107">The runtime to be enabled.</span></span>  
  
## <span data-ttu-id="49971-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="49971-108">Return Value</span></span>  
 <span data-ttu-id="49971-109">Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="49971-109">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="49971-110">Hinweise</span><span class="sxs-lookup"><span data-stu-id="49971-110">Remarks</span></span>  
 <span data-ttu-id="49971-111">Das Aktivieren der Skriptausführung in einer Runtime, die bereits die Skriptausführung aktiviert hat, ist ein No-op.</span><span class="sxs-lookup"><span data-stu-id="49971-111">Enabling script execution in a runtime that already has script execution enabled is a no-op.</span></span>  
  
## <span data-ttu-id="49971-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="49971-112">Requirements</span></span>  
 <span data-ttu-id="49971-113">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="49971-113">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="49971-114">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="49971-114">See Also</span></span>  
 [<span data-ttu-id="49971-115">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="49971-115">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)