---
description: Führt ein serialisiertes Skript aus.
title: JsRunSerializedScript-Funktion | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsRunSerializedScript
helpviewer_keywords:
- JsRunSerializedScript function
ms.assetid: 3fd3f6f1-eb3e-4751-92a5-c93b1035f3b2
caps.latest.revision: 13
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 46f293d76bf0944c1cdedae917735c505798f4ad
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11234247"
---
# <span data-ttu-id="63ed7-103">JsRunSerializedScript Funktion</span><span class="sxs-lookup"><span data-stu-id="63ed7-103">JsRunSerializedScript Function</span></span>

<span data-ttu-id="63ed7-104">Führt ein serialisiertes Skript aus.</span><span class="sxs-lookup"><span data-stu-id="63ed7-104">Runs a serialized script.</span></span>  
  
## <span data-ttu-id="63ed7-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="63ed7-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsRunSerializedScript(  
   _In_z_ const wchar_t *script,  
   _In_ BYTE *buffer,  
   _In_ JsSourceContext sourceContext,  
   _In_z_ const wchar_t *sourceUrl,  
   _Out_ JsValueRef *result  
);  
```  
  
#### <span data-ttu-id="63ed7-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="63ed7-106">Parameters</span></span>  
 `script`  
 <span data-ttu-id="63ed7-107">Der Quellcode des serialisierten Skripts.</span><span class="sxs-lookup"><span data-stu-id="63ed7-107">The source code of the serialized script.</span></span>  
  
 `buffer`  
 <span data-ttu-id="63ed7-108">Das serialisierte Skript.</span><span class="sxs-lookup"><span data-stu-id="63ed7-108">The serialized script.</span></span>  
  
 `sourceContext`  
 <span data-ttu-id="63ed7-109">Ein Cookie, das das Skript identifiziert, das von debugfähigen-Skript Kontexten verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="63ed7-109">A cookie identifying the script that can be used by debuggable script contexts.</span></span>  
  
 `sourceUrl`  
 <span data-ttu-id="63ed7-110">Der Speicherort, aus dem das Skript kam.</span><span class="sxs-lookup"><span data-stu-id="63ed7-110">The location the script came from.</span></span>  
  
 `result`  
 <span data-ttu-id="63ed7-111">Das Ergebnis der Ausführung des Skripts (sofern vorhanden).</span><span class="sxs-lookup"><span data-stu-id="63ed7-111">The result of running the script, if any.</span></span> <span data-ttu-id="63ed7-112">Dieser Parameter kann NULL sein.</span><span class="sxs-lookup"><span data-stu-id="63ed7-112">This parameter can be null.</span></span>  
  
## <span data-ttu-id="63ed7-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="63ed7-113">Return Value</span></span>  
 <span data-ttu-id="63ed7-114">Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="63ed7-114">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="63ed7-115">Hinweise</span><span class="sxs-lookup"><span data-stu-id="63ed7-115">Remarks</span></span>  
 <span data-ttu-id="63ed7-116">Erfordert einen aktiven Skriptkontext.</span><span class="sxs-lookup"><span data-stu-id="63ed7-116">Requires an active script context.</span></span>  
  
 <span data-ttu-id="63ed7-117">Der Puffer wird vom Skriptmodul nicht im Arbeitsspeicher gespeichert, daher muss der Code so lange am Leben bleiben, wie er zum Ausführen von Skripts verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="63ed7-117">The buffer is not persisted in memory by the scripting engine, so your code must keep it alive for as long as it might be used to execute scripts.</span></span>  
  
## <span data-ttu-id="63ed7-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="63ed7-118">Requirements</span></span>  
 <span data-ttu-id="63ed7-119">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="63ed7-119">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="63ed7-120">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="63ed7-120">See Also</span></span>  
 [<span data-ttu-id="63ed7-121">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="63ed7-121">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
