---
description: Ein Funktions Rückruf.
title: JsNativeFunction typedef | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 56ef6cdf-4ca9-4f7c-b953-e661addb1a8e
caps.latest.revision: 5
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: c0b73a11d3a0b2ed0867ef001f3c29c5643132a0
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10567220"
---
# <span data-ttu-id="7455b-103">JsNativeFunction typedef</span><span class="sxs-lookup"><span data-stu-id="7455b-103">JsNativeFunction Typedef</span></span>
<span data-ttu-id="7455b-104">Ein Funktions Rückruf.</span><span class="sxs-lookup"><span data-stu-id="7455b-104">A function callback.</span></span>  
  
## <span data-ttu-id="7455b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="7455b-105">Syntax</span></span>  
  
```cpp  
typedef _Ret_maybenull_ JsValueRef (CALLBACK * JsNativeFunction)(  
   _In_ JsValueRef callee,  
   _In_ bool isConstructCall,  
   _In_ JsValueRef *arguments,  
   _In_ unsigned short argumentCount  
);  
```  
  
#### <span data-ttu-id="7455b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="7455b-106">Parameters</span></span>  
 <span data-ttu-id="7455b-107">angerufenen</span><span class="sxs-lookup"><span data-stu-id="7455b-107">callee</span></span>  
 <span data-ttu-id="7455b-108">Ein `Function` Objekt, das die aufgerufene Funktion darstellt.</span><span class="sxs-lookup"><span data-stu-id="7455b-108">A `Function` object that represents the function being invoked.</span></span>  
  
 <span data-ttu-id="7455b-109">isConstructCall</span><span class="sxs-lookup"><span data-stu-id="7455b-109">isConstructCall</span></span>  
 <span data-ttu-id="7455b-110">Gibt an, ob es sich um einen regulären Anruf oder einen "neuen" Anruf handelt.</span><span class="sxs-lookup"><span data-stu-id="7455b-110">Indicates whether this is a regular call or a 'new' call.</span></span>  
  
 <span data-ttu-id="7455b-111">arguments</span><span class="sxs-lookup"><span data-stu-id="7455b-111">arguments</span></span>  
 <span data-ttu-id="7455b-112">Die Argumente für den Anruf.</span><span class="sxs-lookup"><span data-stu-id="7455b-112">The arguments to the call.</span></span>  
  
 <span data-ttu-id="7455b-113">argumentCount</span><span class="sxs-lookup"><span data-stu-id="7455b-113">argumentCount</span></span>  
 <span data-ttu-id="7455b-114">Die Anzahl von Argumenten.</span><span class="sxs-lookup"><span data-stu-id="7455b-114">The number of arguments.</span></span>  
  
## <span data-ttu-id="7455b-115">Eigenschaftswert/Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7455b-115">Property Value/Return Value</span></span>  
 <span data-ttu-id="7455b-116">Das Ergebnis des Anrufs (sofern vorhanden).</span><span class="sxs-lookup"><span data-stu-id="7455b-116">The result of the call, if any.</span></span>  
  
## <span data-ttu-id="7455b-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7455b-117">Requirements</span></span>  
 <span data-ttu-id="7455b-118">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="7455b-118">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="7455b-119">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="7455b-119">See Also</span></span>  
 [<span data-ttu-id="7455b-120">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="7455b-120">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)