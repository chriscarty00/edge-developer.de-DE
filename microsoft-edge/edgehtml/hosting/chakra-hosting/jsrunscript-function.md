---
description: Führt ein Skript aus.
title: JsRunScript-Funktion | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsRunScript
helpviewer_keywords:
- JsRunScript function
ms.assetid: 8d6b8c9a-af3a-4e21-a330-5a6b535423a3
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: d61771991e1d22a9d71a928d785390b814a992a8
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11234248"
---
# <span data-ttu-id="dab07-103">JsRunScript Funktion</span><span class="sxs-lookup"><span data-stu-id="dab07-103">JsRunScript Function</span></span>

<span data-ttu-id="dab07-104">Führt ein Skript aus.</span><span class="sxs-lookup"><span data-stu-id="dab07-104">Executes a script.</span></span>  
  
## <span data-ttu-id="dab07-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="dab07-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsRunScript(  
   _In_z_ const wchar_t *script,  
   _In_ JsSourceContext sourceContext,  
   _In_z_ const wchar_t *sourceUrl,  
   _Out_ JsValueRef *result  
);  
```  
  
#### <span data-ttu-id="dab07-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="dab07-106">Parameters</span></span>  
 `script`  
 <span data-ttu-id="dab07-107">Das auszuführende Skript.</span><span class="sxs-lookup"><span data-stu-id="dab07-107">The script to run.</span></span>  
  
 `sourceContext`  
 <span data-ttu-id="dab07-108">Ein Cookie, das das Skript identifiziert, das von debugfähigen-Skript Kontexten verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="dab07-108">A cookie identifying the script that can be used by debuggable script contexts.</span></span>  
  
 `sourceUrl`  
 <span data-ttu-id="dab07-109">Der Speicherort, aus dem das Skript kam.</span><span class="sxs-lookup"><span data-stu-id="dab07-109">The location the script came from.</span></span>  
  
 `result`  
 <span data-ttu-id="dab07-110">Das Ergebnis des Skripts (sofern vorhanden).</span><span class="sxs-lookup"><span data-stu-id="dab07-110">The result of the script, if any.</span></span> <span data-ttu-id="dab07-111">Dieser Parameter kann NULL sein.</span><span class="sxs-lookup"><span data-stu-id="dab07-111">This parameter can be null.</span></span>  
  
## <span data-ttu-id="dab07-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="dab07-112">Return Value</span></span>  
 <span data-ttu-id="dab07-113">Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="dab07-113">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="dab07-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="dab07-114">Remarks</span></span>  
 <span data-ttu-id="dab07-115">Erfordert einen aktiven Skriptkontext.</span><span class="sxs-lookup"><span data-stu-id="dab07-115">Requires an active script context.</span></span>  
  
## <span data-ttu-id="dab07-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="dab07-116">Requirements</span></span>  
 <span data-ttu-id="dab07-117">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="dab07-117">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="dab07-118">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="dab07-118">See Also</span></span>  
 [<span data-ttu-id="dab07-119">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="dab07-119">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
