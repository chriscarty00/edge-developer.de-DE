---
description: Legt den zu verwendenden Rückruf fest, um einen Projektions Abschluss zurück zum erforderlichen Thread für Aufrufer aufzurufen.
title: JsSetProjectionEnqueueCallback-Funktion | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: c751ccef-20d2-4d41-9568-1c54adf47cdf
caps.latest.revision: 4
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 7dfedfeb1df5a97159a211795a2dd072d239bb35
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233733"
---
# <span data-ttu-id="a6adf-103">JsSetProjectionEnqueueCallback Funktion</span><span class="sxs-lookup"><span data-stu-id="a6adf-103">JsSetProjectionEnqueueCallback Function</span></span>

<span data-ttu-id="a6adf-104">Legt den zu verwendenden Rückruf fest, um einen Projektions Abschluss zurück zum erforderlichen Thread für Aufrufer aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="a6adf-104">Sets the callback to be used in order to invoke a projection completion back to the callers required thread.</span></span>  
  
## <span data-ttu-id="a6adf-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a6adf-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsSetProjectionEnqueueCallback(  
   _In_ JsProjectionEnqueueCallback projectionEnqueueCallback,  
   _In_opt_ void *projectionEnqueueContext);  
  
```  
  
#### <span data-ttu-id="a6adf-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a6adf-106">Parameters</span></span>  
 `projectionEnqueueContext`  
 <span data-ttu-id="a6adf-107">Der Rückruf, der aufgerufen wird, wenn eine Projektion abgeschlossen wird, wenn ein Hintergrundthread ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a6adf-107">The callback that will be invoked any time a projection completion occurs on a background thread.</span></span>  
  
 `callbackState`  
 <span data-ttu-id="a6adf-108">Der Anwendungskontext, der bereitgestellt wird `projectionEnqueueContext` .</span><span class="sxs-lookup"><span data-stu-id="a6adf-108">The application context provided to `projectionEnqueueContext`.</span></span>  
  
## <span data-ttu-id="a6adf-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a6adf-109">Return Value</span></span>  
 <span data-ttu-id="a6adf-110">Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="a6adf-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="a6adf-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="a6adf-111">Remarks</span></span>  
 <span data-ttu-id="a6adf-112">Erfordert einen aktiven Skriptkontext.</span><span class="sxs-lookup"><span data-stu-id="a6adf-112">Requires an active script context.</span></span>  
  
 <span data-ttu-id="a6adf-113">Der Anruf sollte aus einem anderen com-Apartment oder einem anderen Thread im gleichen MTA erfolgen.</span><span class="sxs-lookup"><span data-stu-id="a6adf-113">The call should be coming from a different COM apartment or from a different thread in the same MTA.</span></span>  
  
 <span data-ttu-id="a6adf-114">Diese API wird nur im EdgeHTML-Modus unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a6adf-114">This API is supported only in EdgeHTML mode.</span></span>  
  
> [!CAUTION]
>  <span data-ttu-id="a6adf-115">PInvoke wird derzeit für diese API nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a6adf-115">PInvoke is not currently supported for this API.</span></span>  
  
## <span data-ttu-id="a6adf-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a6adf-116">Requirements</span></span>  
 <span data-ttu-id="a6adf-117">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="a6adf-117">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="a6adf-118">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="a6adf-118">See Also</span></span>  
 [<span data-ttu-id="a6adf-119">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="a6adf-119">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
