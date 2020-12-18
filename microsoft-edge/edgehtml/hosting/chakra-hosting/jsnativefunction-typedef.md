---
description: Ein Funktions Rückruf.
title: JsNativeFunction typedef | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 56ef6cdf-4ca9-4f7c-b953-e661addb1a8e
caps.latest.revision: 5
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 891fe55f776e8519a5d3c187104b2bc326336482
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233573"
---
# <span data-ttu-id="bba7e-103">JsNativeFunction Typedef</span><span class="sxs-lookup"><span data-stu-id="bba7e-103">JsNativeFunction Typedef</span></span>

<span data-ttu-id="bba7e-104">Ein Funktions Rückruf.</span><span class="sxs-lookup"><span data-stu-id="bba7e-104">A function callback.</span></span>  
  
## <span data-ttu-id="bba7e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="bba7e-105">Syntax</span></span>  
  
```cpp  
typedef _Ret_maybenull_ JsValueRef (CALLBACK * JsNativeFunction)(  
   _In_ JsValueRef callee,  
   _In_ bool isConstructCall,  
   _In_ JsValueRef *arguments,  
   _In_ unsigned short argumentCount  
);  
```  
  
#### <span data-ttu-id="bba7e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="bba7e-106">Parameters</span></span>  
 <span data-ttu-id="bba7e-107">angerufenen</span><span class="sxs-lookup"><span data-stu-id="bba7e-107">callee</span></span>  
 <span data-ttu-id="bba7e-108">Ein `Function` Objekt, das die aufgerufene Funktion darstellt.</span><span class="sxs-lookup"><span data-stu-id="bba7e-108">A `Function` object that represents the function being invoked.</span></span>  
  
 <span data-ttu-id="bba7e-109">isConstructCall</span><span class="sxs-lookup"><span data-stu-id="bba7e-109">isConstructCall</span></span>  
 <span data-ttu-id="bba7e-110">Gibt an, ob es sich um einen regulären Anruf oder einen "neuen" Anruf handelt.</span><span class="sxs-lookup"><span data-stu-id="bba7e-110">Indicates whether this is a regular call or a 'new' call.</span></span>  
  
 <span data-ttu-id="bba7e-111">arguments</span><span class="sxs-lookup"><span data-stu-id="bba7e-111">arguments</span></span>  
 <span data-ttu-id="bba7e-112">Die Argumente für den Anruf.</span><span class="sxs-lookup"><span data-stu-id="bba7e-112">The arguments to the call.</span></span>  
  
 <span data-ttu-id="bba7e-113">argumentCount</span><span class="sxs-lookup"><span data-stu-id="bba7e-113">argumentCount</span></span>  
 <span data-ttu-id="bba7e-114">Die Anzahl von Argumenten.</span><span class="sxs-lookup"><span data-stu-id="bba7e-114">The number of arguments.</span></span>  
  
## <span data-ttu-id="bba7e-115">Eigenschaftswert/Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bba7e-115">Property Value/Return Value</span></span>  
 <span data-ttu-id="bba7e-116">Das Ergebnis des Anrufs (sofern vorhanden).</span><span class="sxs-lookup"><span data-stu-id="bba7e-116">The result of the call, if any.</span></span>  
  
## <span data-ttu-id="bba7e-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bba7e-117">Requirements</span></span>  
 <span data-ttu-id="bba7e-118">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="bba7e-118">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="bba7e-119">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="bba7e-119">See Also</span></span>  
 [<span data-ttu-id="bba7e-120">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="bba7e-120">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
