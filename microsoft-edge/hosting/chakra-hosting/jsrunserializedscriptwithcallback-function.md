---
description: Führt ein serialisiertes Skript aus. Bietet die Möglichkeit, die Skript Quelle nur verzögert zu laden, wenn/wann dies erforderlich ist.
title: JsRunSerializedScriptWithCallback-Funktion | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: 0608d778-f65b-4dc5-a745-364aac57ef59
caps.latest.revision: 4
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 31669615d5e00cb2dbe3730ed20e24d904161f8b
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10568331"
---
# <span data-ttu-id="ae76d-104">JsRunSerializedScriptWithCallback-Funktion</span><span class="sxs-lookup"><span data-stu-id="ae76d-104">JsRunSerializedScriptWithCallback Function</span></span>
<span data-ttu-id="ae76d-105">Führt ein serialisiertes Skript aus.</span><span class="sxs-lookup"><span data-stu-id="ae76d-105">Runs a serialized script.</span></span> <span data-ttu-id="ae76d-106">Bietet die Möglichkeit, die Skript Quelle nur verzögert zu laden, wenn/wann dies erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="ae76d-106">Provides the ability to lazy load the script source only if/when it is needed.</span></span>  
  
## <span data-ttu-id="ae76d-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="ae76d-107">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsRunSerializedScriptWithCallback(  
  _In_ JsSerializedScriptLoadSourceCallback scriptLoadCallback,  
  _In_ JsSerializedScriptUnloadCallback scriptUnloadCallback,  
  _In_ BYTE *buffer,  
  _In_ JsSourceContext sourceContext,  
  _In_z_ const wchar_t *sourceUrl,  
  _Out_opt_ JsValueRef *result  
);  
  
```  
  
#### <span data-ttu-id="ae76d-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="ae76d-108">Parameters</span></span>  
 `scriptLoadCallback`  
 <span data-ttu-id="ae76d-109">Der Rückruf wird aufgerufen, wenn der Quellcode des Skripts geladen werden muss.</span><span class="sxs-lookup"><span data-stu-id="ae76d-109">Callback called when the source code of the script needs to be loaded.</span></span>  
  
 `scriptUnloadCallback`  
 <span data-ttu-id="ae76d-110">Rückruf, der aufgerufen wird, wenn das serialisierte Skript und der Quellcode nicht mehr benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="ae76d-110">Callback called when the serialized script and source code are no longer needed.</span></span>  
  
 `buffer`  
 <span data-ttu-id="ae76d-111">Das serialisierte Skript.</span><span class="sxs-lookup"><span data-stu-id="ae76d-111">The serialized script.</span></span>  
  
 `sourceContext`  
 <span data-ttu-id="ae76d-112">Ein Cookie, das das Skript identifiziert, das von debugfähigen-Skript Kontexten verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="ae76d-112">A cookie identifying the script that can be used by debuggable script contexts.</span></span>     <span data-ttu-id="ae76d-113">Dieser Kontext wird an scriptLoadCallback und scriptUnloadCallback übergeben.</span><span class="sxs-lookup"><span data-stu-id="ae76d-113">This context will passed into scriptLoadCallback and scriptUnloadCallback.</span></span>  
  
 `sourceUrl`  
 <span data-ttu-id="ae76d-114">Der Speicherort, aus dem das Skript kam.</span><span class="sxs-lookup"><span data-stu-id="ae76d-114">The location the script came from.</span></span>  
  
 `result`  
 <span data-ttu-id="ae76d-115">Das Ergebnis der Ausführung des Skripts (sofern vorhanden).</span><span class="sxs-lookup"><span data-stu-id="ae76d-115">The result of running the script, if any.</span></span> <span data-ttu-id="ae76d-116">Dieser Parameter kann NULL sein.</span><span class="sxs-lookup"><span data-stu-id="ae76d-116">This parameter can be null.</span></span>  
  
## <span data-ttu-id="ae76d-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ae76d-117">Return Value</span></span>  
 <span data-ttu-id="ae76d-118">Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="ae76d-118">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="ae76d-119">Hinweise</span><span class="sxs-lookup"><span data-stu-id="ae76d-119">Remarks</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="ae76d-120">Diese API steht noch nicht für Store-Apps zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="ae76d-120">This API is not yet available for Store apps.</span></span>  
  
 <span data-ttu-id="ae76d-121">Erfordert einen aktiven Skriptkontext.</span><span class="sxs-lookup"><span data-stu-id="ae76d-121">Requires an active script context.</span></span>  
  
 <span data-ttu-id="ae76d-122">Die Laufzeit bleibt auf dem Puffer, bis alle Instanzen von Funktionen, die aus dem Puffer erstellt wurden, als Garbage Collection erfasst werden.</span><span class="sxs-lookup"><span data-stu-id="ae76d-122">The runtime will hold on to the buffer until all instances of any functions created from     the buffer are garbage collected.</span></span>  <span data-ttu-id="ae76d-123">Anschließend wird scriptUnloadCallback aufgerufen, um den Anrufer darüber zu informieren, dass es sicher freigegeben werden kann.</span><span class="sxs-lookup"><span data-stu-id="ae76d-123">It will then call scriptUnloadCallback to inform the     caller that it is safe to release.</span></span>  
  
## <span data-ttu-id="ae76d-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ae76d-124">Requirements</span></span>  
 <span data-ttu-id="ae76d-125">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="ae76d-125">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="ae76d-126">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="ae76d-126">See Also</span></span>  
 [<span data-ttu-id="ae76d-127">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="ae76d-127">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)