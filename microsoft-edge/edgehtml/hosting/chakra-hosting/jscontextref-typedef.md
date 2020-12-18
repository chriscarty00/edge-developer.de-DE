---
description: Ein Verweis auf einen Skriptkontext.
title: JsContextRef typedef | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 8586bfcc-bb24-430d-a6f2-1a3b3e34ec2e
caps.latest.revision: 6
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: c8a8fcbd67afb150d682cfc19321f0f13acfe3a6
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233771"
---
# <span data-ttu-id="8124e-103">JsContextRef Typedef</span><span class="sxs-lookup"><span data-stu-id="8124e-103">JsContextRef Typedef</span></span>

<span data-ttu-id="8124e-104">Ein Verweis auf einen Skriptkontext.</span><span class="sxs-lookup"><span data-stu-id="8124e-104">A reference to a script context.</span></span>  
  
## <span data-ttu-id="8124e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="8124e-105">Syntax</span></span>  
  
```cpp  
typedef JsRef JsContextRef;  
```  
  
## <span data-ttu-id="8124e-106">Hinweise</span><span class="sxs-lookup"><span data-stu-id="8124e-106">Remarks</span></span>  
 <span data-ttu-id="8124e-107">Jeder Skriptkontext enthält sein eigenes globales Objekt, das sich vom globalen Objekt in anderen Skript Kontexten unterscheidet.</span><span class="sxs-lookup"><span data-stu-id="8124e-107">Each script context contains its own global object, distinct from the global object in other script contexts.</span></span>  
  
 <span data-ttu-id="8124e-108">Viele Chakra-Hosting-APIs erfordern einen "aktiven" Skriptkontext, der mithilfe von verwendet werden kann `JsSetCurrentContext` .</span><span class="sxs-lookup"><span data-stu-id="8124e-108">Many Chakra hosting APIs require an "active" script context, which can be set using `JsSetCurrentContext`.</span></span> <span data-ttu-id="8124e-109">Chakra-Host-APIs, für die ein aktueller Kontext festzulegen ist, werden in Ihrer Dokumentation explizit festgestellt.</span><span class="sxs-lookup"><span data-stu-id="8124e-109">Chakra hosting APIs that require a current context to be set will note that explicitly in their documentation.</span></span>  
  
## <span data-ttu-id="8124e-110">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8124e-110">Requirements</span></span>  
 <span data-ttu-id="8124e-111">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="8124e-111">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="8124e-112">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="8124e-112">See Also</span></span>  
 [<span data-ttu-id="8124e-113">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="8124e-113">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
