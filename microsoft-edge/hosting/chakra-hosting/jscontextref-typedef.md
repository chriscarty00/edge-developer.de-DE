---
description: Ein Verweis auf einen Skriptkontext.
title: JsContextRef typedef | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 8586bfcc-bb24-430d-a6f2-1a3b3e34ec2e
caps.latest.revision: 6
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 80e4b5034079f4f0d26da070bd209aa41bf3475f
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10567323"
---
# <span data-ttu-id="e1d92-103">JsContextRef typedef</span><span class="sxs-lookup"><span data-stu-id="e1d92-103">JsContextRef Typedef</span></span>
<span data-ttu-id="e1d92-104">Ein Verweis auf einen Skriptkontext.</span><span class="sxs-lookup"><span data-stu-id="e1d92-104">A reference to a script context.</span></span>  
  
## <span data-ttu-id="e1d92-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e1d92-105">Syntax</span></span>  
  
```cpp  
typedef JsRef JsContextRef;  
```  
  
## <span data-ttu-id="e1d92-106">Hinweise</span><span class="sxs-lookup"><span data-stu-id="e1d92-106">Remarks</span></span>  
 <span data-ttu-id="e1d92-107">Jeder Skriptkontext enthält sein eigenes globales Objekt, das sich vom globalen Objekt in anderen Skript Kontexten unterscheidet.</span><span class="sxs-lookup"><span data-stu-id="e1d92-107">Each script context contains its own global object, distinct from the global object in other script contexts.</span></span>  
  
 <span data-ttu-id="e1d92-108">Viele Chakra-Hosting-APIs erfordern einen "aktiven" Skriptkontext, der mithilfe von verwendet werden kann `JsSetCurrentContext` .</span><span class="sxs-lookup"><span data-stu-id="e1d92-108">Many Chakra hosting APIs require an "active" script context, which can be set using `JsSetCurrentContext`.</span></span> <span data-ttu-id="e1d92-109">Chakra-Host-APIs, für die ein aktueller Kontext festzulegen ist, werden in Ihrer Dokumentation explizit festgestellt.</span><span class="sxs-lookup"><span data-stu-id="e1d92-109">Chakra hosting APIs that require a current context to be set will note that explicitly in their documentation.</span></span>  
  
## <span data-ttu-id="e1d92-110">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e1d92-110">Requirements</span></span>  
 <span data-ttu-id="e1d92-111">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="e1d92-111">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="e1d92-112">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="e1d92-112">See Also</span></span>  
 [<span data-ttu-id="e1d92-113">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="e1d92-113">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)