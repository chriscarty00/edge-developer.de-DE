---
description: Analysiert ein serialisiertes Skript und gibt eine Funktion zurück, die das Skript darstellt. Bietet die Möglichkeit, die Skript Quelle nur verzögert zu laden, wenn/wann dies erforderlich ist.
title: JsParseSerializedScriptWithCallback-Funktion | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 0a93ecfb-4b82-4a85-b24c-6816db2332ea
caps.latest.revision: 5
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: b145f01a5c3459100d8402beae63b7cff55db7b8
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11234078"
---
# <span data-ttu-id="3946f-104">JsParseSerializedScriptWithCallback Funktion</span><span class="sxs-lookup"><span data-stu-id="3946f-104">JsParseSerializedScriptWithCallback Function</span></span>

<span data-ttu-id="3946f-105">Analysiert ein serialisiertes Skript und gibt eine Funktion zurück, die das Skript darstellt.</span><span class="sxs-lookup"><span data-stu-id="3946f-105">Parses a serialized script and returns a function representing the script.</span></span> <span data-ttu-id="3946f-106">Bietet die Möglichkeit, die Skript Quelle nur verzögert zu laden, wenn/wann dies erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="3946f-106">Provides the ability to lazy load the script source only if/when it is needed.</span></span>  
  
## <span data-ttu-id="3946f-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="3946f-107">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsParseSerializedScriptWithCallback(  
  _In_ JsSerializedScriptLoadSourceCallback scriptLoadCallback,  
  _In_ JsSerializedScriptUnloadCallback scriptUnloadCallback,  
  _In_ BYTE *buffer,  
  _In_ JsSourceContext sourceContext,  
  _In_z_ const wchar_t *sourceUrl,  
  _Out_ JsValueRef * result  
);  
  
```  
  
#### <span data-ttu-id="3946f-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="3946f-108">Parameters</span></span>  
 `scriptLoadCallback`  
 <span data-ttu-id="3946f-109">Der Rückruf wird aufgerufen, wenn der Quellcode des Skripts geladen werden muss.</span><span class="sxs-lookup"><span data-stu-id="3946f-109">Callback called when the source code of the script needs to be loaded.</span></span>  
  
 `scriptUnloadCallback`  
 <span data-ttu-id="3946f-110">Rückruf, der aufgerufen wird, wenn das serialisierte Skript und der Quellcode nicht mehr benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="3946f-110">Callback called when the serialized script and source code are no longer needed.</span></span>  
  
 `buffer`  
 <span data-ttu-id="3946f-111">Das serialisierte Skript.</span><span class="sxs-lookup"><span data-stu-id="3946f-111">The serialized script.</span></span>  
  
 `sourceContext`  
 <span data-ttu-id="3946f-112">Ein Cookie, das das Skript identifiziert, das von debugfähigen-Skript Kontexten verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="3946f-112">A cookie identifying the script that can be used by debuggable script contexts.</span></span>     <span data-ttu-id="3946f-113">Dieser Kontext wird an scriptLoadCallback und scriptUnloadCallback übergeben.</span><span class="sxs-lookup"><span data-stu-id="3946f-113">This context will passed into scriptLoadCallback and scriptUnloadCallback.</span></span>  
  
 `sourceUrl`  
 <span data-ttu-id="3946f-114">Der Speicherort, aus dem das Skript kam.</span><span class="sxs-lookup"><span data-stu-id="3946f-114">The location the script came from.</span></span>  
  
 `result`  
 <span data-ttu-id="3946f-115">Eine Funktion, die den Skriptcode darstellt.</span><span class="sxs-lookup"><span data-stu-id="3946f-115">A function representing the script code.</span></span>  
  
## <span data-ttu-id="3946f-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3946f-116">Return Value</span></span>  
 <span data-ttu-id="3946f-117">Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="3946f-117">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="3946f-118">Hinweise</span><span class="sxs-lookup"><span data-stu-id="3946f-118">Remarks</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="3946f-119">Diese API steht noch nicht für Store-Apps zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="3946f-119">This API is not yet available for Store apps.</span></span>  
  
 <span data-ttu-id="3946f-120">Erfordert einen aktiven Skriptkontext.</span><span class="sxs-lookup"><span data-stu-id="3946f-120">Requires an active script context.</span></span>  
  
 <span data-ttu-id="3946f-121">Die Laufzeit bleibt auf dem Puffer, bis alle Instanzen von Funktionen, die aus dem Puffer erstellt wurden, als Garbage Collection erfasst werden.</span><span class="sxs-lookup"><span data-stu-id="3946f-121">The runtime will hold on to the buffer until all instances of any functions created from     the buffer are garbage collected.</span></span>  <span data-ttu-id="3946f-122">Anschließend wird scriptUnloadCallback aufgerufen, um den Anrufer darüber zu informieren, dass es sicher freigegeben werden kann.</span><span class="sxs-lookup"><span data-stu-id="3946f-122">It will then call scriptUnloadCallback to inform the     caller that it is safe to release.</span></span>  
  
## <span data-ttu-id="3946f-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3946f-123">Requirements</span></span>  
 <span data-ttu-id="3946f-124">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="3946f-124">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="3946f-125">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="3946f-125">See Also</span></span>  
 [<span data-ttu-id="3946f-126">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="3946f-126">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
