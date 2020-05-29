---
description: Wandelt den Wert mithilfe der JavaScript-Standardsemantik in eine Zeichenfolge um.
title: JsConvertValueToString-Funktion | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsConvertValueToString
helpviewer_keywords:
- JsConvertValueToString function
ms.assetid: a97aca04-b2ce-446a-acf4-49cd6777a85c
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 21c77ca3050773c07572665c6d58e0ebc05d8ee9
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10567314"
---
# <span data-ttu-id="20934-103">JsConvertValueToString-Funktion</span><span class="sxs-lookup"><span data-stu-id="20934-103">JsConvertValueToString Function</span></span>
<span data-ttu-id="20934-104">Wandelt den Wert mithilfe der JavaScript-Standardsemantik in eine Zeichenfolge um.</span><span class="sxs-lookup"><span data-stu-id="20934-104">Converts the value to string using standard JavaScript semantics.</span></span>  
  
## <span data-ttu-id="20934-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="20934-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsConvertValueToString(  
   _In_ JsValueRef value,  
   _Out_ JsValueRef *stringValue  
);  
```  
  
#### <span data-ttu-id="20934-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="20934-106">Parameters</span></span>  
 `value`  
 <span data-ttu-id="20934-107">Der Wert, der konvertiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="20934-107">The value to be converted.</span></span>  
  
 `stringValue`  
 <span data-ttu-id="20934-108">Der konvertierte Wert.</span><span class="sxs-lookup"><span data-stu-id="20934-108">The converted value.</span></span>  
  
## <span data-ttu-id="20934-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="20934-109">Return Value</span></span>  
 <span data-ttu-id="20934-110">Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="20934-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="20934-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="20934-111">Remarks</span></span>  
 <span data-ttu-id="20934-112">Erfordert einen aktiven Skriptkontext.</span><span class="sxs-lookup"><span data-stu-id="20934-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="20934-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="20934-113">Requirements</span></span>  
 <span data-ttu-id="20934-114">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="20934-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="20934-115">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="20934-115">See Also</span></span>  
 [<span data-ttu-id="20934-116">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="20934-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)