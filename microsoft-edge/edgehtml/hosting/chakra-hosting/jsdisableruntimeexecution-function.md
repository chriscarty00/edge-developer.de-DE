---
description: Unterbricht die Skriptausführung und beendet alle ausgeführten Skripts in einer Laufzeit.
title: JsDisableRuntimeExecution-Funktion | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsDisableRuntimeExecution
helpviewer_keywords:
- JsDisableRuntimeExecution function
ms.assetid: 4bd4670a-a9da-4f8c-b3fd-1fd366d915c3
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 6a08e6a7f89c724f8cf1a73afd97d2cb23c0334e
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233953"
---
# <span data-ttu-id="c9423-103">JsDisableRuntimeExecution Funktion</span><span class="sxs-lookup"><span data-stu-id="c9423-103">JsDisableRuntimeExecution Function</span></span>

<span data-ttu-id="c9423-104">Unterbricht die Skriptausführung und beendet alle ausgeführten Skripts in einer Laufzeit.</span><span class="sxs-lookup"><span data-stu-id="c9423-104">Suspends script execution and terminates any running scripts in a runtime.</span></span>  
  
## <span data-ttu-id="c9423-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c9423-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsDisableRuntimeExecution(  
   _In_ JsRuntimeHandle runtime  
);  
```  
  
#### <span data-ttu-id="c9423-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c9423-106">Parameters</span></span>  
 `runtime`  
 <span data-ttu-id="c9423-107">Die Laufzeit, die angehalten werden soll.</span><span class="sxs-lookup"><span data-stu-id="c9423-107">The runtime to be suspended.</span></span>  
  
## <span data-ttu-id="c9423-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c9423-108">Return Value</span></span>  
 <span data-ttu-id="c9423-109">Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="c9423-109">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="c9423-110">Hinweise</span><span class="sxs-lookup"><span data-stu-id="c9423-110">Remarks</span></span>  
 <span data-ttu-id="c9423-111">Bei Aufrufen einer angehalten-Laufzeit tritt ein Fehler auf, bis `JsEnableRuntimeExecution` aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="c9423-111">Calls to a suspended runtime will fail until `JsEnableRuntimeExecution` is called.</span></span>  
  
 <span data-ttu-id="c9423-112">Diese API muss nicht für den Thread aufgerufen werden, in dem die Laufzeit aktiv ist.</span><span class="sxs-lookup"><span data-stu-id="c9423-112">This API does not have to be called on the thread the runtime is active on.</span></span> <span data-ttu-id="c9423-113">Obwohl die Laufzeit in einen angehalten-Zustand gesetzt wird, wird ein ausgeführtes Skript möglicherweise nicht sofort angehalten. ein laufendes Skript wird so schnell wie möglich mit einer nicht abfangbaren Ausnahme beendet.</span><span class="sxs-lookup"><span data-stu-id="c9423-113">Although the runtime will be set into a suspended state, an executing script may not be suspended immediately; a running script will be terminated with an uncatchable exception as soon as possible.</span></span>  
  
 <span data-ttu-id="c9423-114">Das Anhalten der Ausführung in einer Laufzeit, die bereits angehalten ist, ist ein No-op-Modus.</span><span class="sxs-lookup"><span data-stu-id="c9423-114">Suspending execution in a runtime that is already suspended is a no-op.</span></span>  
  
## <span data-ttu-id="c9423-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c9423-115">Requirements</span></span>  
 <span data-ttu-id="c9423-116">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="c9423-116">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="c9423-117">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="c9423-117">See Also</span></span>  
 [<span data-ttu-id="c9423-118">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="c9423-118">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
