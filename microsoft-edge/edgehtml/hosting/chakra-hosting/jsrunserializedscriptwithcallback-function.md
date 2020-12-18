---
description: Führt ein serialisiertes Skript aus. Bietet die Möglichkeit, die Skript Quelle nur verzögert zu laden, wenn/wann dies erforderlich ist.
title: JsRunSerializedScriptWithCallback-Funktion | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 0608d778-f65b-4dc5-a745-364aac57ef59
caps.latest.revision: 4
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: ac9ac08357cd479f78e3500bc5eef151fb8e4e6c
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11234246"
---
# <span data-ttu-id="cacff-104">JsRunSerializedScriptWithCallback Funktion</span><span class="sxs-lookup"><span data-stu-id="cacff-104">JsRunSerializedScriptWithCallback Function</span></span>

<span data-ttu-id="cacff-105">Führt ein serialisiertes Skript aus.</span><span class="sxs-lookup"><span data-stu-id="cacff-105">Runs a serialized script.</span></span> <span data-ttu-id="cacff-106">Bietet die Möglichkeit, die Skript Quelle nur verzögert zu laden, wenn/wann dies erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="cacff-106">Provides the ability to lazy load the script source only if/when it is needed.</span></span>  
  
## <span data-ttu-id="cacff-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="cacff-107">Syntax</span></span>  
  
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
  
#### <span data-ttu-id="cacff-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="cacff-108">Parameters</span></span>  
 `scriptLoadCallback`  
 <span data-ttu-id="cacff-109">Der Rückruf wird aufgerufen, wenn der Quellcode des Skripts geladen werden muss.</span><span class="sxs-lookup"><span data-stu-id="cacff-109">Callback called when the source code of the script needs to be loaded.</span></span>  
  
 `scriptUnloadCallback`  
 <span data-ttu-id="cacff-110">Rückruf, der aufgerufen wird, wenn das serialisierte Skript und der Quellcode nicht mehr benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="cacff-110">Callback called when the serialized script and source code are no longer needed.</span></span>  
  
 `buffer`  
 <span data-ttu-id="cacff-111">Das serialisierte Skript.</span><span class="sxs-lookup"><span data-stu-id="cacff-111">The serialized script.</span></span>  
  
 `sourceContext`  
 <span data-ttu-id="cacff-112">Ein Cookie, das das Skript identifiziert, das von debugfähigen-Skript Kontexten verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="cacff-112">A cookie identifying the script that can be used by debuggable script contexts.</span></span>     <span data-ttu-id="cacff-113">Dieser Kontext wird an scriptLoadCallback und scriptUnloadCallback übergeben.</span><span class="sxs-lookup"><span data-stu-id="cacff-113">This context will passed into scriptLoadCallback and scriptUnloadCallback.</span></span>  
  
 `sourceUrl`  
 <span data-ttu-id="cacff-114">Der Speicherort, aus dem das Skript kam.</span><span class="sxs-lookup"><span data-stu-id="cacff-114">The location the script came from.</span></span>  
  
 `result`  
 <span data-ttu-id="cacff-115">Das Ergebnis der Ausführung des Skripts (sofern vorhanden).</span><span class="sxs-lookup"><span data-stu-id="cacff-115">The result of running the script, if any.</span></span> <span data-ttu-id="cacff-116">Dieser Parameter kann NULL sein.</span><span class="sxs-lookup"><span data-stu-id="cacff-116">This parameter can be null.</span></span>  
  
## <span data-ttu-id="cacff-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cacff-117">Return Value</span></span>  
 <span data-ttu-id="cacff-118">Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="cacff-118">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="cacff-119">Hinweise</span><span class="sxs-lookup"><span data-stu-id="cacff-119">Remarks</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="cacff-120">Diese API steht noch nicht für Store-Apps zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="cacff-120">This API is not yet available for Store apps.</span></span>  
  
 <span data-ttu-id="cacff-121">Erfordert einen aktiven Skriptkontext.</span><span class="sxs-lookup"><span data-stu-id="cacff-121">Requires an active script context.</span></span>  
  
 <span data-ttu-id="cacff-122">Die Laufzeit bleibt auf dem Puffer, bis alle Instanzen von Funktionen, die aus dem Puffer erstellt wurden, als Garbage Collection erfasst werden.</span><span class="sxs-lookup"><span data-stu-id="cacff-122">The runtime will hold on to the buffer until all instances of any functions created from     the buffer are garbage collected.</span></span>  <span data-ttu-id="cacff-123">Anschließend wird scriptUnloadCallback aufgerufen, um den Anrufer darüber zu informieren, dass es sicher freigegeben werden kann.</span><span class="sxs-lookup"><span data-stu-id="cacff-123">It will then call scriptUnloadCallback to inform the     caller that it is safe to release.</span></span>  
  
## <span data-ttu-id="cacff-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cacff-124">Requirements</span></span>  
 <span data-ttu-id="cacff-125">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="cacff-125">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="cacff-126">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="cacff-126">See Also</span></span>  
 [<span data-ttu-id="cacff-127">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="cacff-127">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
