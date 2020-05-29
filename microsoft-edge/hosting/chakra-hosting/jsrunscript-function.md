---
description: Führt ein Skript aus.
title: JsRunScript-Funktion | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsRunScript
helpviewer_keywords:
- JsRunScript function
ms.assetid: 8d6b8c9a-af3a-4e21-a330-5a6b535423a3
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 49a06e4e6ad0c04e124b76f31d38b2e362e03f99
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10568337"
---
# <span data-ttu-id="90c13-103">JsRunScript-Funktion</span><span class="sxs-lookup"><span data-stu-id="90c13-103">JsRunScript Function</span></span>
<span data-ttu-id="90c13-104">Führt ein Skript aus.</span><span class="sxs-lookup"><span data-stu-id="90c13-104">Executes a script.</span></span>  
  
## <span data-ttu-id="90c13-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="90c13-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsRunScript(  
   _In_z_ const wchar_t *script,  
   _In_ JsSourceContext sourceContext,  
   _In_z_ const wchar_t *sourceUrl,  
   _Out_ JsValueRef *result  
);  
```  
  
#### <span data-ttu-id="90c13-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="90c13-106">Parameters</span></span>  
 `script`  
 <span data-ttu-id="90c13-107">Das auszuführende Skript.</span><span class="sxs-lookup"><span data-stu-id="90c13-107">The script to run.</span></span>  
  
 `sourceContext`  
 <span data-ttu-id="90c13-108">Ein Cookie, das das Skript identifiziert, das von debugfähigen-Skript Kontexten verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="90c13-108">A cookie identifying the script that can be used by debuggable script contexts.</span></span>  
  
 `sourceUrl`  
 <span data-ttu-id="90c13-109">Der Speicherort, aus dem das Skript kam.</span><span class="sxs-lookup"><span data-stu-id="90c13-109">The location the script came from.</span></span>  
  
 `result`  
 <span data-ttu-id="90c13-110">Das Ergebnis des Skripts (sofern vorhanden).</span><span class="sxs-lookup"><span data-stu-id="90c13-110">The result of the script, if any.</span></span> <span data-ttu-id="90c13-111">Dieser Parameter kann NULL sein.</span><span class="sxs-lookup"><span data-stu-id="90c13-111">This parameter can be null.</span></span>  
  
## <span data-ttu-id="90c13-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="90c13-112">Return Value</span></span>  
 <span data-ttu-id="90c13-113">Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="90c13-113">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="90c13-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="90c13-114">Remarks</span></span>  
 <span data-ttu-id="90c13-115">Erfordert einen aktiven Skriptkontext.</span><span class="sxs-lookup"><span data-stu-id="90c13-115">Requires an active script context.</span></span>  
  
## <span data-ttu-id="90c13-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="90c13-116">Requirements</span></span>  
 <span data-ttu-id="90c13-117">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="90c13-117">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="90c13-118">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="90c13-118">See Also</span></span>  
 [<span data-ttu-id="90c13-119">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="90c13-119">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)