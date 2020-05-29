---
description: Legt den zu verwendenden Rückruf fest, um einen Projektions Abschluss zurück zum erforderlichen Thread für Aufrufer aufzurufen.
title: JsSetProjectionEnqueueCallback-Funktion | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: c751ccef-20d2-4d41-9568-1c54adf47cdf
caps.latest.revision: 4
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 02da0238360b0dc6fff9bb86c9f5ab04d1ba7112
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10568302"
---
# <span data-ttu-id="ead90-103">JsSetProjectionEnqueueCallback-Funktion</span><span class="sxs-lookup"><span data-stu-id="ead90-103">JsSetProjectionEnqueueCallback Function</span></span>
<span data-ttu-id="ead90-104">Legt den zu verwendenden Rückruf fest, um einen Projektions Abschluss zurück zum erforderlichen Thread für Aufrufer aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="ead90-104">Sets the callback to be used in order to invoke a projection completion back to the callers required thread.</span></span>  
  
## <span data-ttu-id="ead90-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ead90-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsSetProjectionEnqueueCallback(  
   _In_ JsProjectionEnqueueCallback projectionEnqueueCallback,  
   _In_opt_ void *projectionEnqueueContext);  
  
```  
  
#### <span data-ttu-id="ead90-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ead90-106">Parameters</span></span>  
 `projectionEnqueueContext`  
 <span data-ttu-id="ead90-107">Der Rückruf, der aufgerufen wird, wenn eine Projektion abgeschlossen wird, wenn ein Hintergrundthread ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ead90-107">The callback that will be invoked any time a projection completion occurs on a background thread.</span></span>  
  
 `callbackState`  
 <span data-ttu-id="ead90-108">Der Anwendungskontext, der bereitgestellt wird `projectionEnqueueContext` .</span><span class="sxs-lookup"><span data-stu-id="ead90-108">The application context provided to `projectionEnqueueContext`.</span></span>  
  
## <span data-ttu-id="ead90-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ead90-109">Return Value</span></span>  
 <span data-ttu-id="ead90-110">Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="ead90-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="ead90-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="ead90-111">Remarks</span></span>  
 <span data-ttu-id="ead90-112">Erfordert einen aktiven Skriptkontext.</span><span class="sxs-lookup"><span data-stu-id="ead90-112">Requires an active script context.</span></span>  
  
 <span data-ttu-id="ead90-113">Der Anruf sollte aus einem anderen com-Apartment oder einem anderen Thread im gleichen MTA erfolgen.</span><span class="sxs-lookup"><span data-stu-id="ead90-113">The call should be coming from a different COM apartment or from a different thread in the same MTA.</span></span>  
  
 <span data-ttu-id="ead90-114">Diese API wird nur im EdgeHTML-Modus unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ead90-114">This API is supported only in EdgeHTML mode.</span></span>  
  
> [!CAUTION]
>  <span data-ttu-id="ead90-115">PInvoke wird derzeit für diese API nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ead90-115">PInvoke is not currently supported for this API.</span></span>  
  
## <span data-ttu-id="ead90-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ead90-116">Requirements</span></span>  
 <span data-ttu-id="ead90-117">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="ead90-117">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="ead90-118">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="ead90-118">See Also</span></span>  
 [<span data-ttu-id="ead90-119">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="ead90-119">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)