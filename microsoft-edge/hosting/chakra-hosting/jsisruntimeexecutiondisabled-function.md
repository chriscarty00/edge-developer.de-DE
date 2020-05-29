---
description: Gibt einen Wert zurück, der angibt, ob die Skriptausführung in der Laufzeit deaktiviert ist.
title: JsIsRuntimeExecutionDisabled-Funktion | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsIsRuntimeExecutionDisabled
helpviewer_keywords:
- JsIsRuntimeExecutionDisabled function
ms.assetid: 77490280-fb84-4614-a1f0-6ac31e3bd607
caps.latest.revision: 5
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 6968a31c9acab70589fe58c86cc566e631778c3c
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10567223"
---
# <span data-ttu-id="2e025-103">JsIsRuntimeExecutionDisabled-Funktion</span><span class="sxs-lookup"><span data-stu-id="2e025-103">JsIsRuntimeExecutionDisabled Function</span></span>
<span data-ttu-id="2e025-104">Gibt einen Wert zurück, der angibt, ob die Skriptausführung in der Laufzeit deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="2e025-104">Returns a value that indicates whether script execution is disabled in the runtime.</span></span>  
  
## <span data-ttu-id="2e025-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="2e025-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsIsRuntimeExecutionDisabled(    _In_ JsRuntimeHandle runtime,    _Out_ bool *isDisabled);  
```  
  
#### <span data-ttu-id="2e025-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="2e025-106">Parameters</span></span>  
 `runtime`  
 <span data-ttu-id="2e025-107">Gibt die Laufzeit an, um zu überprüfen, ob die Ausführung deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="2e025-107">Specifies the runtime to check if execution is disabled.</span></span>  
  
 `isDisabled`  
 `true` <span data-ttu-id="2e025-108">Wenn die Ausführung deaktiviert ist, `false` andernfalls.</span><span class="sxs-lookup"><span data-stu-id="2e025-108">if execution is disabled, `false` otherwise.</span></span>  
  
## <span data-ttu-id="2e025-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2e025-109">Return Value</span></span>  
 `JsNoError` <span data-ttu-id="2e025-110">Wenn der Vorgang erfolgreich war, wird andernfalls ein Fehlercode ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2e025-110">if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="2e025-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2e025-111">Requirements</span></span>  
 <span data-ttu-id="2e025-112">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="2e025-112">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="2e025-113">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="2e025-113">See Also</span></span>  
 [<span data-ttu-id="2e025-114">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="2e025-114">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)