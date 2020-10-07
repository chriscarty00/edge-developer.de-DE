---
description: Creates a Javascript `ArrayBuffer` object to access external memory.
title: JsCreateExternalArrayBuffer Function | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: 4a02aaec-0f67-4bf9-b37c-71cdb1410ca4
caps.latest.revision: 3
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 376eedda18393436d9dce340753586bf32599b21
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10567300"
---
# <span data-ttu-id="04876-103">JsCreateExternalArrayBuffer Function</span><span class="sxs-lookup"><span data-stu-id="04876-103">JsCreateExternalArrayBuffer Function</span></span>
<span data-ttu-id="04876-104">Creates a Javascript `ArrayBuffer` object to access external memory.</span><span class="sxs-lookup"><span data-stu-id="04876-104">Creates a Javascript `ArrayBuffer` object to access external memory.</span></span>
  
## <span data-ttu-id="04876-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="04876-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsCreateExternalArrayBuffer(  
  _Pre_maybenull_ _Pre_writable_byte_size_(byteLength) void *data,  
  _In_ unsigned int byteLength,  
  _In_opt_ JsFinalizeCallback finalizeCallback,  
  _In_opt_ void *callbackState,  
  _Out_ JsValueRef *result  
);  
  
```  
  
#### <span data-ttu-id="04876-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="04876-106">Parameters</span></span>  
 `data`  
 <span data-ttu-id="04876-107">A pointer to the external memory.</span><span class="sxs-lookup"><span data-stu-id="04876-107">A pointer to the external memory.</span></span>  
  
 `byteLength`  
 <span data-ttu-id="04876-108">The number of bytes in the external memory.</span><span class="sxs-lookup"><span data-stu-id="04876-108">The number of bytes in the external memory.</span></span>  
  
 `finalizeCallback`  
 <span data-ttu-id="04876-109">A callback for when the object is finalized.</span><span class="sxs-lookup"><span data-stu-id="04876-109">A callback for when the object is finalized.</span></span> <span data-ttu-id="04876-110">May be null.</span><span class="sxs-lookup"><span data-stu-id="04876-110">May be null.</span></span>  
  
 `callbackState`  
 <span data-ttu-id="04876-111">User provided state that will be passed back to finalizeCallback.</span><span class="sxs-lookup"><span data-stu-id="04876-111">User provided state that will be passed back to finalizeCallback.</span></span>  
  
 `result`  
 <span data-ttu-id="04876-112">The new `ArrayBuffer` object.</span><span class="sxs-lookup"><span data-stu-id="04876-112">The new `ArrayBuffer` object.</span></span>  
  
## <span data-ttu-id="04876-113">Return Value</span><span class="sxs-lookup"><span data-stu-id="04876-113">Return Value</span></span>  
 <span data-ttu-id="04876-114">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span><span class="sxs-lookup"><span data-stu-id="04876-114">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="04876-115">Remarks</span><span class="sxs-lookup"><span data-stu-id="04876-115">Remarks</span></span>  
 <span data-ttu-id="04876-116">Requires an active script context.</span><span class="sxs-lookup"><span data-stu-id="04876-116">Requires an active script context.</span></span>  
  
## <span data-ttu-id="04876-117">Requirements</span><span class="sxs-lookup"><span data-stu-id="04876-117">Requirements</span></span>  
 <span data-ttu-id="04876-118">**Header:** jsrt.h</span><span class="sxs-lookup"><span data-stu-id="04876-118">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="04876-119">See Also</span><span class="sxs-lookup"><span data-stu-id="04876-119">See Also</span></span>  
 [<span data-ttu-id="04876-120">Reference (JavaScript Runtime)</span><span class="sxs-lookup"><span data-stu-id="04876-120">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)