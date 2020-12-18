---
description: Projizieren Sie einen WinRT-Namespace.
title: JsProjectWinRTNamespace-Funktion | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 8a23c154-df4b-4ce3-9fef-f41f90acdb87
caps.latest.revision: 5
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: f781cf90aaec68b2bd305bf34c453fc663ad0187
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11234317"
---
# <span data-ttu-id="31256-103">JsProjectWinRTNamespace Funktion</span><span class="sxs-lookup"><span data-stu-id="31256-103">JsProjectWinRTNamespace Function</span></span>

<span data-ttu-id="31256-104">Projizieren Sie einen WinRT-Namespace.</span><span class="sxs-lookup"><span data-stu-id="31256-104">Project a WinRT namespace.</span></span>  
  
## <span data-ttu-id="31256-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="31256-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode)  
   JsProjectWinRTNamespace(  
   _In_z_ const wchar_t *namespaceName  
);  
```  
  
#### <span data-ttu-id="31256-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="31256-106">Parameters</span></span>  
 `namespaceName`  
 <span data-ttu-id="31256-107">Der WinRT-Namespace, der projiziert werden soll.</span><span class="sxs-lookup"><span data-stu-id="31256-107">The WinRT namespace to be projected.</span></span>  
  
## <span data-ttu-id="31256-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="31256-108">Return Value</span></span>  
 <span data-ttu-id="31256-109">Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="31256-109">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="31256-110">Hinweise</span><span class="sxs-lookup"><span data-stu-id="31256-110">Remarks</span></span>  
 <span data-ttu-id="31256-111">Erfordert einen aktiven Skriptkontext.</span><span class="sxs-lookup"><span data-stu-id="31256-111">Requires an active script context.</span></span>  
  
 <span data-ttu-id="31256-112">Diese API wird nur im EdgeHTML-Modus unterstützt.</span><span class="sxs-lookup"><span data-stu-id="31256-112">This API is supported only in EdgeHTML mode.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="31256-113">WinRT war der Platt Form Name vor der universellen Windows-Plattform (UWP).</span><span class="sxs-lookup"><span data-stu-id="31256-113">WinRT was the platform name before Universal Windows Platform (UWP).</span></span>  
  
## <span data-ttu-id="31256-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="31256-114">Requirements</span></span>  
 <span data-ttu-id="31256-115">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="31256-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="31256-116">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="31256-116">See Also</span></span>  
 [<span data-ttu-id="31256-117">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="31256-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
