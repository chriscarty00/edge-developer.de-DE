---
description: Ruft den JavaScript-Typ eines JsValueRef ab.
title: JsGetValueType-Funktion | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsGetValueType
helpviewer_keywords:
- JsGetValueType function
ms.assetid: f403cf7c-c8c0-4a17-bfa9-0302d00e760e
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 85dc6644e26017c6085ab64d914a86196cca8080
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10568365"
---
# <span data-ttu-id="9f976-103">JsGetValueType-Funktion</span><span class="sxs-lookup"><span data-stu-id="9f976-103">JsGetValueType Function</span></span>
<span data-ttu-id="9f976-104">Ruft den JavaScript-Typ eines JsValueRef ab.</span><span class="sxs-lookup"><span data-stu-id="9f976-104">Gets the JavaScript type of a JsValueRef.</span></span>  
  
## <span data-ttu-id="9f976-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="9f976-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetValueType(  
   _In_ JsValueRef value,  
   _Out_ JsValueType *type  
);  
```  
  
#### <span data-ttu-id="9f976-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="9f976-106">Parameters</span></span>  
 `value`  
 <span data-ttu-id="9f976-107">Der Wert, dessen Typ zurückgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="9f976-107">The value whose type is to be returned.</span></span>  
  
 `type`  
 <span data-ttu-id="9f976-108">Der Typ des Werts.</span><span class="sxs-lookup"><span data-stu-id="9f976-108">The type of the value.</span></span>  
  
## <span data-ttu-id="9f976-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9f976-109">Return Value</span></span>  
 <span data-ttu-id="9f976-110">Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="9f976-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="9f976-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="9f976-111">Remarks</span></span>  
 <span data-ttu-id="9f976-112">Erfordert einen aktiven Skriptkontext.</span><span class="sxs-lookup"><span data-stu-id="9f976-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="9f976-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9f976-113">Requirements</span></span>  
 <span data-ttu-id="9f976-114">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="9f976-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="9f976-115">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="9f976-115">See Also</span></span>  
 [<span data-ttu-id="9f976-116">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="9f976-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)