---
description: Analysiert ein Skript und gibt eine Funktion zurück, die das Skript darstellt.
title: JsParseScript-Funktion | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsParseScript
helpviewer_keywords:
- JsParseScript function
ms.assetid: e9d0e363-7cbe-43eb-9dc0-1f47e586c9ab
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: dd224ef0e800f05e6e07580f545bc4af218b3498
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10568351"
---
# <span data-ttu-id="a77f6-103">JsParseScript-Funktion</span><span class="sxs-lookup"><span data-stu-id="a77f6-103">JsParseScript Function</span></span>
<span data-ttu-id="a77f6-104">Analysiert ein Skript und gibt eine Funktion zurück, die das Skript darstellt.</span><span class="sxs-lookup"><span data-stu-id="a77f6-104">Parses a script and returns a function representing the script.</span></span>  
  
## <span data-ttu-id="a77f6-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a77f6-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsParseScript(  
   _In_z_ const wchar_t *script,  
   _In_ JsSourceContext sourceContext,  
   _In_z_ const wchar_t *sourceUrl,  
   _Out_ JsValueRef *result  
);  
```  
  
#### <span data-ttu-id="a77f6-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a77f6-106">Parameters</span></span>  
 `script`  
 <span data-ttu-id="a77f6-107">Das zu analysierende Skript.</span><span class="sxs-lookup"><span data-stu-id="a77f6-107">The script to parse.</span></span>  
  
 `sourceContext`  
 <span data-ttu-id="a77f6-108">Ein Cookie, das das Skript identifiziert, das von debugfähigen-Skript Kontexten verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="a77f6-108">A cookie identifying the script that can be used by debuggable script contexts.</span></span>  
  
 `sourceUrl`  
 <span data-ttu-id="a77f6-109">Der Speicherort, aus dem das Skript kam.</span><span class="sxs-lookup"><span data-stu-id="a77f6-109">The location the script came from.</span></span>  
  
 `result`  
 <span data-ttu-id="a77f6-110">Eine Funktion, die den Skriptcode darstellt.</span><span class="sxs-lookup"><span data-stu-id="a77f6-110">A function representing the script code.</span></span>  
  
## <span data-ttu-id="a77f6-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a77f6-111">Return Value</span></span>  
 <span data-ttu-id="a77f6-112">Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="a77f6-112">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="a77f6-113">Hinweise</span><span class="sxs-lookup"><span data-stu-id="a77f6-113">Remarks</span></span>  
 <span data-ttu-id="a77f6-114">Erfordert einen aktiven Skriptkontext.</span><span class="sxs-lookup"><span data-stu-id="a77f6-114">Requires an active script context.</span></span>  
  
## <span data-ttu-id="a77f6-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a77f6-115">Requirements</span></span>  
 <span data-ttu-id="a77f6-116">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="a77f6-116">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="a77f6-117">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="a77f6-117">See Also</span></span>  
 [<span data-ttu-id="a77f6-118">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="a77f6-118">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)