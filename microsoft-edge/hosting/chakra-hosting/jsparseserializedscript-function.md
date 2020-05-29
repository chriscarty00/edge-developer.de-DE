---
description: Analysiert ein serialisiertes Skript und gibt eine Funktion zurück, die das Skript darstellt.
title: JsParseSerializedScript-Funktion | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsParseSerializedScript
helpviewer_keywords:
- JsParseSerializedScript function
ms.assetid: 40d0c7c4-fd5b-46ed-9e65-38c2db2fc859
caps.latest.revision: 13
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: a778a007e69f15063d23cc55f999144ab55a306c
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10568350"
---
# <span data-ttu-id="5ce5c-103">JsParseSerializedScript-Funktion</span><span class="sxs-lookup"><span data-stu-id="5ce5c-103">JsParseSerializedScript Function</span></span>
<span data-ttu-id="5ce5c-104">Analysiert ein serialisiertes Skript und gibt eine Funktion zurück, die das Skript darstellt.</span><span class="sxs-lookup"><span data-stu-id="5ce5c-104">Parses a serialized script and returns a function representing the script.</span></span>  
  
## <span data-ttu-id="5ce5c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="5ce5c-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsParseSerializedScript(  
   _In_z_ const wchar_t *script,  
   _In_ BYTE *buffer,  
   _In_ JsSourceContext sourceContext,  
   _In_z_ const wchar_t *sourceUrl,  
   _Out_ JsValueRef *result  
);  
```  
  
#### <span data-ttu-id="5ce5c-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="5ce5c-106">Parameters</span></span>  
 `script`  
 <span data-ttu-id="5ce5c-107">Das zu analysierende Skript.</span><span class="sxs-lookup"><span data-stu-id="5ce5c-107">The script to parse.</span></span>  
  
 `buffer`  
 <span data-ttu-id="5ce5c-108">Das serialisierte Skript.</span><span class="sxs-lookup"><span data-stu-id="5ce5c-108">The serialized script.</span></span>  
  
 `sourceContext`  
 <span data-ttu-id="5ce5c-109">Ein Cookie, das das Skript identifiziert, das von debugfähigen-Skript Kontexten verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="5ce5c-109">A cookie identifying the script that can be used by debuggable script contexts.</span></span>  
  
 `sourceUrl`  
 <span data-ttu-id="5ce5c-110">Der Speicherort, aus dem das Skript kam.</span><span class="sxs-lookup"><span data-stu-id="5ce5c-110">The location the script came from.</span></span>  
  
 `result`  
 <span data-ttu-id="5ce5c-111">Eine Funktion, die den Skriptcode darstellt.</span><span class="sxs-lookup"><span data-stu-id="5ce5c-111">A function representing the script code.</span></span>  
  
## <span data-ttu-id="5ce5c-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5ce5c-112">Return Value</span></span>  
 <span data-ttu-id="5ce5c-113">Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="5ce5c-113">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="5ce5c-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="5ce5c-114">Remarks</span></span>  
 <span data-ttu-id="5ce5c-115">Erfordert einen aktiven Skriptkontext.</span><span class="sxs-lookup"><span data-stu-id="5ce5c-115">Requires an active script context.</span></span>  
  
 <span data-ttu-id="5ce5c-116">Der Puffer wird vom Skriptmodul nicht im Arbeitsspeicher gespeichert, daher muss der Code so lange am Leben bleiben, wie er zum Ausführen von Skripts verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="5ce5c-116">The buffer is not persisted in memory by the scripting engine, so your code must keep it alive for as long as it might be used to execute scripts.</span></span>  
  
## <span data-ttu-id="5ce5c-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5ce5c-117">Requirements</span></span>  
 <span data-ttu-id="5ce5c-118">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="5ce5c-118">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="5ce5c-119">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="5ce5c-119">See Also</span></span>  
 [<span data-ttu-id="5ce5c-120">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="5ce5c-120">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)