---
description: Führt ein serialisiertes Skript aus.
title: JsRunSerializedScript-Funktion | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsRunSerializedScript
helpviewer_keywords:
- JsRunSerializedScript function
ms.assetid: 3fd3f6f1-eb3e-4751-92a5-c93b1035f3b2
caps.latest.revision: 13
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: bc1e2fb7fdc5df52fde3b7cc59cf9173d658782a
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10568336"
---
# <span data-ttu-id="c1160-103">JsRunSerializedScript-Funktion</span><span class="sxs-lookup"><span data-stu-id="c1160-103">JsRunSerializedScript Function</span></span>
<span data-ttu-id="c1160-104">Führt ein serialisiertes Skript aus.</span><span class="sxs-lookup"><span data-stu-id="c1160-104">Runs a serialized script.</span></span>  
  
## <span data-ttu-id="c1160-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c1160-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsRunSerializedScript(  
   _In_z_ const wchar_t *script,  
   _In_ BYTE *buffer,  
   _In_ JsSourceContext sourceContext,  
   _In_z_ const wchar_t *sourceUrl,  
   _Out_ JsValueRef *result  
);  
```  
  
#### <span data-ttu-id="c1160-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c1160-106">Parameters</span></span>  
 `script`  
 <span data-ttu-id="c1160-107">Der Quellcode des serialisierten Skripts.</span><span class="sxs-lookup"><span data-stu-id="c1160-107">The source code of the serialized script.</span></span>  
  
 `buffer`  
 <span data-ttu-id="c1160-108">Das serialisierte Skript.</span><span class="sxs-lookup"><span data-stu-id="c1160-108">The serialized script.</span></span>  
  
 `sourceContext`  
 <span data-ttu-id="c1160-109">Ein Cookie, das das Skript identifiziert, das von debugfähigen-Skript Kontexten verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="c1160-109">A cookie identifying the script that can be used by debuggable script contexts.</span></span>  
  
 `sourceUrl`  
 <span data-ttu-id="c1160-110">Der Speicherort, aus dem das Skript kam.</span><span class="sxs-lookup"><span data-stu-id="c1160-110">The location the script came from.</span></span>  
  
 `result`  
 <span data-ttu-id="c1160-111">Das Ergebnis der Ausführung des Skripts (sofern vorhanden).</span><span class="sxs-lookup"><span data-stu-id="c1160-111">The result of running the script, if any.</span></span> <span data-ttu-id="c1160-112">Dieser Parameter kann NULL sein.</span><span class="sxs-lookup"><span data-stu-id="c1160-112">This parameter can be null.</span></span>  
  
## <span data-ttu-id="c1160-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c1160-113">Return Value</span></span>  
 <span data-ttu-id="c1160-114">Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="c1160-114">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="c1160-115">Hinweise</span><span class="sxs-lookup"><span data-stu-id="c1160-115">Remarks</span></span>  
 <span data-ttu-id="c1160-116">Erfordert einen aktiven Skriptkontext.</span><span class="sxs-lookup"><span data-stu-id="c1160-116">Requires an active script context.</span></span>  
  
 <span data-ttu-id="c1160-117">Der Puffer wird vom Skriptmodul nicht im Arbeitsspeicher gespeichert, daher muss der Code so lange am Leben bleiben, wie er zum Ausführen von Skripts verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="c1160-117">The buffer is not persisted in memory by the scripting engine, so your code must keep it alive for as long as it might be used to execute scripts.</span></span>  
  
## <span data-ttu-id="c1160-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c1160-118">Requirements</span></span>  
 <span data-ttu-id="c1160-119">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="c1160-119">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="c1160-120">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="c1160-120">See Also</span></span>  
 [<span data-ttu-id="c1160-121">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="c1160-121">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)