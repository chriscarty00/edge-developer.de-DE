---
description: Gibt einen Wert zurück, der angibt, ob die Skriptausführung in der Laufzeit deaktiviert ist.
title: JsIsRuntimeExecutionDisabled-Funktion | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsIsRuntimeExecutionDisabled
helpviewer_keywords:
- JsIsRuntimeExecutionDisabled function
ms.assetid: 77490280-fb84-4614-a1f0-6ac31e3bd607
caps.latest.revision: 5
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 0ce59c77525abdb2dd6cac71dde1378264395e79
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233574"
---
# <span data-ttu-id="c6928-103">JsIsRuntimeExecutionDisabled Funktion</span><span class="sxs-lookup"><span data-stu-id="c6928-103">JsIsRuntimeExecutionDisabled Function</span></span>

<span data-ttu-id="c6928-104">Gibt einen Wert zurück, der angibt, ob die Skriptausführung in der Laufzeit deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="c6928-104">Returns a value that indicates whether script execution is disabled in the runtime.</span></span>  
  
## <span data-ttu-id="c6928-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c6928-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsIsRuntimeExecutionDisabled(    _In_ JsRuntimeHandle runtime,    _Out_ bool *isDisabled);  
```  
  
#### <span data-ttu-id="c6928-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c6928-106">Parameters</span></span>  
 `runtime`  
 <span data-ttu-id="c6928-107">Gibt die Laufzeit an, um zu überprüfen, ob die Ausführung deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="c6928-107">Specifies the runtime to check if execution is disabled.</span></span>  
  
 `isDisabled`  
 `true` <span data-ttu-id="c6928-108">Wenn die Ausführung deaktiviert ist, `false` andernfalls.</span><span class="sxs-lookup"><span data-stu-id="c6928-108">if execution is disabled, `false` otherwise.</span></span>  
  
## <span data-ttu-id="c6928-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c6928-109">Return Value</span></span>  
 `JsNoError` <span data-ttu-id="c6928-110">Wenn der Vorgang erfolgreich war, wird andernfalls ein Fehlercode ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c6928-110">if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="c6928-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c6928-111">Requirements</span></span>  
 <span data-ttu-id="c6928-112">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="c6928-112">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="c6928-113">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="c6928-113">See Also</span></span>  
 [<span data-ttu-id="c6928-114">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="c6928-114">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
