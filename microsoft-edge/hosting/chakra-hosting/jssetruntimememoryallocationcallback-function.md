---
description: Legt einen Speicher Zuordnungs Rückruf für die angegebene Laufzeit fest.
title: JsSetRuntimeMemoryAllocationCallback-Funktion | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsSetRuntimeMemoryAllocationCallback
helpviewer_keywords:
- JsSetRuntimeMemoryAllocationCallback function
ms.assetid: 6aa7d58d-6456-4df1-815f-1ba36fb4ae14
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 5c648761473023f00e894fbf75c794cfcc9422c5
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10568208"
---
# <span data-ttu-id="5c5e1-103">JsSetRuntimeMemoryAllocationCallback-Funktion</span><span class="sxs-lookup"><span data-stu-id="5c5e1-103">JsSetRuntimeMemoryAllocationCallback Function</span></span>
<span data-ttu-id="5c5e1-104">Legt einen Speicher Zuordnungs Rückruf für die angegebene Laufzeit fest.</span><span class="sxs-lookup"><span data-stu-id="5c5e1-104">Sets a memory allocation callback for specified runtime.</span></span>  
  
## <span data-ttu-id="5c5e1-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="5c5e1-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsSetRuntimeMemoryAllocationCallback(  
   _In_ JsRuntimeHandle runtime,  
   _In_opt_ void *callbackState,  
   _In_ JsMemoryAllocationCallback allocationCallback  
);  
```  
  
#### <span data-ttu-id="5c5e1-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="5c5e1-106">Parameters</span></span>  
 `runtime`  
 <span data-ttu-id="5c5e1-107">Die Laufzeit, für die der Zuordnungs Rückruf registriert werden soll.</span><span class="sxs-lookup"><span data-stu-id="5c5e1-107">The runtime for which to register the allocation callback.</span></span>  
  
 `callbackState`  
 <span data-ttu-id="5c5e1-108">Der Benutzer hat den Zustand bereitgestellt, der an den Rückruf zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="5c5e1-108">User provided state that will be passed back to the callback.</span></span>  
  
 `allocationCallback`  
 <span data-ttu-id="5c5e1-109">Speicher Zuordnungs Rückruf, der für Speicher Zuordnungs Ereignisse aufgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="5c5e1-109">Memory allocation callback to be called for memory allocation events.</span></span>  
  
## <span data-ttu-id="5c5e1-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5c5e1-110">Return Value</span></span>  
 <span data-ttu-id="5c5e1-111">Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="5c5e1-111">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="5c5e1-112">Hinweise</span><span class="sxs-lookup"><span data-stu-id="5c5e1-112">Remarks</span></span>  
 <span data-ttu-id="5c5e1-113">Wenn Sie einen Speicher Zuordnungs Rückruf registrieren, ruft die Common Language Runtime zurück an den Host, wenn dieser Speicher aus dem Betriebssystem abruft oder Speicher freigibt.</span><span class="sxs-lookup"><span data-stu-id="5c5e1-113">Registering a memory allocation callback will cause the runtime to call back to the host whenever it acquires memory from, or releases memory to, the OS.</span></span> <span data-ttu-id="5c5e1-114">Die Rückruf Routine wird aufgerufen, bevor der Laufzeitspeicher-Manager einen Speicherblock reserviert.</span><span class="sxs-lookup"><span data-stu-id="5c5e1-114">The callback routine is called before the runtime memory manager allocates a block of memory.</span></span> <span data-ttu-id="5c5e1-115">Die Zuweisung wird zurückgewiesen, wenn der Rückruf false zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="5c5e1-115">The allocation will be rejected if the callback returns false.</span></span> <span data-ttu-id="5c5e1-116">Der Laufzeitspeicher-Manager ruft auch nach dem Freigeben eines Speicherblocks sowie nach Zuordnungsfehlern die Rückruf Routine auf.</span><span class="sxs-lookup"><span data-stu-id="5c5e1-116">The runtime memory manager will also invoke the callback routine after freeing a block of memory, as well as after allocation failures.</span></span>  
  
 <span data-ttu-id="5c5e1-117">Der Rückruf wird für den aktuellen Runtime-Ausführungsthread aufgerufen, daher wird die Ausführung blockiert, bis der Rückruf abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="5c5e1-117">The callback is invoked on the current runtime execution thread, therefore execution is blocked until the callback completes.</span></span>  
  
 <span data-ttu-id="5c5e1-118">Der Rückgabewert des Rückrufs wird nicht gespeichert; zuvor abgelehnte Zuweisungen verhindern nicht, dass die Common Language Runtime den Rückruf später für neue Speicherzuweisungen erneut aufruft.</span><span class="sxs-lookup"><span data-stu-id="5c5e1-118">The return value of the callback is not stored; previously rejected allocations will not prevent the runtime from invoking the callback again later for new memory allocations.</span></span>  
  
## <span data-ttu-id="5c5e1-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5c5e1-119">Requirements</span></span>  
 <span data-ttu-id="5c5e1-120">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="5c5e1-120">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="5c5e1-121">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="5c5e1-121">See Also</span></span>  
 [<span data-ttu-id="5c5e1-122">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="5c5e1-122">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)