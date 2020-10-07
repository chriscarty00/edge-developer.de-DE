---
description: Gets the script context that the object belongs to.
title: JsGetContextOfObject Function | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: cea6cdcd-790f-455c-af04-026af8ae2eb7
caps.latest.revision: 3
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 4f1b996954e877d9c98ac0caf06f255af629a386
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10567266"
---
# <span data-ttu-id="d3d96-103">JsGetContextOfObject Function</span><span class="sxs-lookup"><span data-stu-id="d3d96-103">JsGetContextOfObject Function</span></span>
<span data-ttu-id="d3d96-104">Gets the script context that the object belongs to.</span><span class="sxs-lookup"><span data-stu-id="d3d96-104">Gets the script context that the object belongs to.</span></span>  
  
## <span data-ttu-id="d3d96-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="d3d96-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetContextOfObject(  
  _In_ JsValueRef object,  
  _Out_ JsContextRef *context  
);  
```  
  
#### <span data-ttu-id="d3d96-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="d3d96-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="d3d96-107">The object to get the context from.</span><span class="sxs-lookup"><span data-stu-id="d3d96-107">The object to get the context from.</span></span>  
  
 `context`  
 <span data-ttu-id="d3d96-108">The context the object belongs to.</span><span class="sxs-lookup"><span data-stu-id="d3d96-108">The context the object belongs to.</span></span>  
  
## <span data-ttu-id="d3d96-109">Return Value</span><span class="sxs-lookup"><span data-stu-id="d3d96-109">Return Value</span></span>  
 <span data-ttu-id="d3d96-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span><span class="sxs-lookup"><span data-stu-id="d3d96-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="d3d96-111">Remarks</span><span class="sxs-lookup"><span data-stu-id="d3d96-111">Remarks</span></span>  
 <span data-ttu-id="d3d96-112">Requires an active script context.</span><span class="sxs-lookup"><span data-stu-id="d3d96-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="d3d96-113">Requirements</span><span class="sxs-lookup"><span data-stu-id="d3d96-113">Requirements</span></span>  
 <span data-ttu-id="d3d96-114">**Header:** jsrt.h</span><span class="sxs-lookup"><span data-stu-id="d3d96-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="d3d96-115">See Also</span><span class="sxs-lookup"><span data-stu-id="d3d96-115">See Also</span></span>  
 [<span data-ttu-id="d3d96-116">Reference (JavaScript Runtime)</span><span class="sxs-lookup"><span data-stu-id="d3d96-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)