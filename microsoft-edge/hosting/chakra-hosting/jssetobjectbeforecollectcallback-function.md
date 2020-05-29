---
description: Legt eine Rückruffunktion fest, die von der Laufzeit vor der Garbage Collection eines Objekts aufgerufen wird.
title: JsSetObjectBeforeCollectCallback-Funktion | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: ea2cbd94-d8b0-4fa9-a4a1-c75a4e338eaf
caps.latest.revision: 3
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 77a59c6ace96809c0b232c96aa9639555e7badcd
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10568306"
---
# <span data-ttu-id="174e2-103">JsSetObjectBeforeCollectCallback-Funktion</span><span class="sxs-lookup"><span data-stu-id="174e2-103">JsSetObjectBeforeCollectCallback Function</span></span>
<span data-ttu-id="174e2-104">Legt eine Rückruffunktion fest, die von der Laufzeit vor der Garbage Collection eines Objekts aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="174e2-104">Sets a callback function that is called by the runtime before garbage collection of an object.</span></span>  
  
## <span data-ttu-id="174e2-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="174e2-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsSetObjectBeforeCollectCallback(  
   _In_ JsRef ref,  
   _In_opt_ void *callbackState,  
   _In_ JsObjectBeforeCollectCallback objectBeforeCollectCallback  
);  
```  
  
#### <span data-ttu-id="174e2-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="174e2-106">Parameters</span></span>  
 `ref`  
 <span data-ttu-id="174e2-107">Das Objekt, für das der Rückruf registriert werden soll.</span><span class="sxs-lookup"><span data-stu-id="174e2-107">The object for which to register the callback.</span></span>  
  
 `callbackState`  
 <span data-ttu-id="174e2-108">Vom Benutzer bereitgestellter Zustand, der an den Rückruf zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="174e2-108">User-provided state that will be passed back to the callback.</span></span>  
  
 `objectBeforeCollectCallback`  
 <span data-ttu-id="174e2-109">Die Rückruffunktion, die festzulegen ist.</span><span class="sxs-lookup"><span data-stu-id="174e2-109">The callback function being set.</span></span> <span data-ttu-id="174e2-110">Verwenden Sie NULL, um zuvor registrierten Rückruf zu löschen.</span><span class="sxs-lookup"><span data-stu-id="174e2-110">Use null to clear previously registered callback.</span></span>  
  
## <span data-ttu-id="174e2-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="174e2-111">Return Value</span></span>  
 <span data-ttu-id="174e2-112">Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="174e2-112">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="174e2-113">Hinweise</span><span class="sxs-lookup"><span data-stu-id="174e2-113">Remarks</span></span>  
 <span data-ttu-id="174e2-114">Der Rückruf wird für den aktuellen Runtime-Ausführungsthread aufgerufen, daher wird die Ausführung blockiert, bis der Rückruf abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="174e2-114">The callback is invoked on the current runtime execution thread, therefore execution is blocked until the callback completes.</span></span>  
  
 <span data-ttu-id="174e2-115">Diese API wird nur im EdgeHTML-Modus unterstützt.</span><span class="sxs-lookup"><span data-stu-id="174e2-115">This API is supported only in EdgeHTML mode.</span></span>  
  
## <span data-ttu-id="174e2-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="174e2-116">Requirements</span></span>  
 <span data-ttu-id="174e2-117">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="174e2-117">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="174e2-118">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="174e2-118">See Also</span></span>  
 [<span data-ttu-id="174e2-119">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="174e2-119">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)