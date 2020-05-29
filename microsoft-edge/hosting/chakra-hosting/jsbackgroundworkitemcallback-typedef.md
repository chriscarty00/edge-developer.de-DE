---
description: Ein Rückruf für einen Arbeitsaufgaben Hintergrund
title: JsBackgroundWorkItemCallback typedef | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: e6db52e1-830c-46a2-b9f9-cc2d450a1da8
caps.latest.revision: 6
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 9bc1e5687d92d7286e1e6d4387bd6b69d95ceb68
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10567336"
---
# <span data-ttu-id="a872f-103">JsBackgroundWorkItemCallback typedef</span><span class="sxs-lookup"><span data-stu-id="a872f-103">JsBackgroundWorkItemCallback Typedef</span></span>
<span data-ttu-id="a872f-104">Ein Rückruf für einen Arbeitsaufgaben Hintergrund</span><span class="sxs-lookup"><span data-stu-id="a872f-104">A background work item callback.</span></span>  
  
## <span data-ttu-id="a872f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a872f-105">Syntax</span></span>  
  
```cpp  
typedef void (CALLBACK *JsBackgroundWorkItemCallback)(  
   _In_opt_ void *callbackData  
);  
```  
  
#### <span data-ttu-id="a872f-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a872f-106">Parameters</span></span>  
 <span data-ttu-id="a872f-107">callBackData</span><span class="sxs-lookup"><span data-stu-id="a872f-107">callbackData</span></span>  
 <span data-ttu-id="a872f-108">Daten Argument, das an den Thread Dienst übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="a872f-108">Data argument passed to the thread service.</span></span>  
  
## <span data-ttu-id="a872f-109">Hinweise</span><span class="sxs-lookup"><span data-stu-id="a872f-109">Remarks</span></span>  
 <span data-ttu-id="a872f-110">Diese wird an den Thread Dienst des Hosts übergeben (sofern vorhanden), damit der Host den Arbeitsaufgaben Rückruf im Hintergrundthread seiner Wahl aufrufen kann.</span><span class="sxs-lookup"><span data-stu-id="a872f-110">This is passed to the host's thread service (if provided) to allow the host to invoke the work item callback on the background thread of its choice.</span></span>  
  
## <span data-ttu-id="a872f-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a872f-111">Requirements</span></span>  
 <span data-ttu-id="a872f-112">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="a872f-112">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="a872f-113">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="a872f-113">See Also</span></span>  
 [<span data-ttu-id="a872f-114">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="a872f-114">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)