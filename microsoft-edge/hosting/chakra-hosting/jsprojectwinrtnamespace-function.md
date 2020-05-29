---
description: Projizieren Sie einen WinRT-Namespace.
title: JsProjectWinRTNamespace-Funktion | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 8a23c154-df4b-4ce3-9fef-f41f90acdb87
caps.latest.revision: 5
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: c4d63727b3d25bbb346fee7179ae0d942ae37008
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10567206"
---
# <span data-ttu-id="690da-103">JsProjectWinRTNamespace-Funktion</span><span class="sxs-lookup"><span data-stu-id="690da-103">JsProjectWinRTNamespace Function</span></span>
<span data-ttu-id="690da-104">Projizieren Sie einen WinRT-Namespace.</span><span class="sxs-lookup"><span data-stu-id="690da-104">Project a WinRT namespace.</span></span>  
  
## <span data-ttu-id="690da-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="690da-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode)  
   JsProjectWinRTNamespace(  
   _In_z_ const wchar_t *namespaceName  
);  
```  
  
#### <span data-ttu-id="690da-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="690da-106">Parameters</span></span>  
 `namespaceName`  
 <span data-ttu-id="690da-107">Der WinRT-Namespace, der projiziert werden soll.</span><span class="sxs-lookup"><span data-stu-id="690da-107">The WinRT namespace to be projected.</span></span>  
  
## <span data-ttu-id="690da-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="690da-108">Return Value</span></span>  
 <span data-ttu-id="690da-109">Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="690da-109">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="690da-110">Hinweise</span><span class="sxs-lookup"><span data-stu-id="690da-110">Remarks</span></span>  
 <span data-ttu-id="690da-111">Erfordert einen aktiven Skriptkontext.</span><span class="sxs-lookup"><span data-stu-id="690da-111">Requires an active script context.</span></span>  
  
 <span data-ttu-id="690da-112">Diese API wird nur im EdgeHTML-Modus unterstützt.</span><span class="sxs-lookup"><span data-stu-id="690da-112">This API is supported only in EdgeHTML mode.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="690da-113">WinRT war der Platt Form Name vor der universellen Windows-Plattform (UWP).</span><span class="sxs-lookup"><span data-stu-id="690da-113">WinRT was the platform name before Universal Windows Platform (UWP).</span></span>  
  
## <span data-ttu-id="690da-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="690da-114">Requirements</span></span>  
 <span data-ttu-id="690da-115">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="690da-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="690da-116">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="690da-116">See Also</span></span>  
 [<span data-ttu-id="690da-117">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="690da-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)