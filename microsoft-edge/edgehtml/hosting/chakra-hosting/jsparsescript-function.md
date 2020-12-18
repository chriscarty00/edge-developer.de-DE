---
description: Analysiert ein Skript und gibt eine Funktion zurück, die das Skript darstellt.
title: JsParseScript-Funktion | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsParseScript
helpviewer_keywords:
- JsParseScript function
ms.assetid: e9d0e363-7cbe-43eb-9dc0-1f47e586c9ab
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 656d9a992868a3cb892808775f160092b8eaf069
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11234085"
---
# <span data-ttu-id="700ef-103">JsParseScript Funktion</span><span class="sxs-lookup"><span data-stu-id="700ef-103">JsParseScript Function</span></span>

<span data-ttu-id="700ef-104">Analysiert ein Skript und gibt eine Funktion zurück, die das Skript darstellt.</span><span class="sxs-lookup"><span data-stu-id="700ef-104">Parses a script and returns a function representing the script.</span></span>  
  
## <span data-ttu-id="700ef-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="700ef-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsParseScript(  
   _In_z_ const wchar_t *script,  
   _In_ JsSourceContext sourceContext,  
   _In_z_ const wchar_t *sourceUrl,  
   _Out_ JsValueRef *result  
);  
```  
  
#### <span data-ttu-id="700ef-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="700ef-106">Parameters</span></span>  
 `script`  
 <span data-ttu-id="700ef-107">Das zu analysierende Skript.</span><span class="sxs-lookup"><span data-stu-id="700ef-107">The script to parse.</span></span>  
  
 `sourceContext`  
 <span data-ttu-id="700ef-108">Ein Cookie, das das Skript identifiziert, das von debugfähigen-Skript Kontexten verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="700ef-108">A cookie identifying the script that can be used by debuggable script contexts.</span></span>  
  
 `sourceUrl`  
 <span data-ttu-id="700ef-109">Der Speicherort, aus dem das Skript kam.</span><span class="sxs-lookup"><span data-stu-id="700ef-109">The location the script came from.</span></span>  
  
 `result`  
 <span data-ttu-id="700ef-110">Eine Funktion, die den Skriptcode darstellt.</span><span class="sxs-lookup"><span data-stu-id="700ef-110">A function representing the script code.</span></span>  
  
## <span data-ttu-id="700ef-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="700ef-111">Return Value</span></span>  
 <span data-ttu-id="700ef-112">Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="700ef-112">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="700ef-113">Hinweise</span><span class="sxs-lookup"><span data-stu-id="700ef-113">Remarks</span></span>  
 <span data-ttu-id="700ef-114">Erfordert einen aktiven Skriptkontext.</span><span class="sxs-lookup"><span data-stu-id="700ef-114">Requires an active script context.</span></span>  
  
## <span data-ttu-id="700ef-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="700ef-115">Requirements</span></span>  
 <span data-ttu-id="700ef-116">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="700ef-116">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="700ef-117">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="700ef-117">See Also</span></span>  
 [<span data-ttu-id="700ef-118">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="700ef-118">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
