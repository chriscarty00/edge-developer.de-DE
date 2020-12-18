---
description: Ruft den `double` Wert eines Zahlenwerts ab.
title: JsNumberToDouble-Funktion | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsNumberToDouble
helpviewer_keywords:
- JsNumberToDouble function
ms.assetid: 5f52e8b6-2b70-49a3-879a-bd83ebf2ac33
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: e4ae744f091045116a639aff619c475c7c7025f3
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11234093"
---
# <span data-ttu-id="f0f1b-103">JsNumberToDouble Funktion</span><span class="sxs-lookup"><span data-stu-id="f0f1b-103">JsNumberToDouble Function</span></span>

<span data-ttu-id="f0f1b-104">Ruft den `double` Wert eines Zahlenwerts ab.</span><span class="sxs-lookup"><span data-stu-id="f0f1b-104">Retrieves the `double` value of a number value.</span></span>  
  
## <span data-ttu-id="f0f1b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="f0f1b-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsNumberToDouble(  
   _In_ JsValueRef value,  
   _Out_ double *doubleValue  
);  
```  
  
#### <span data-ttu-id="f0f1b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="f0f1b-106">Parameters</span></span>  
 `value`  
 <span data-ttu-id="f0f1b-107">Der Zahlenwert, der in einen Wert konvertiert werden soll `double` .</span><span class="sxs-lookup"><span data-stu-id="f0f1b-107">The number value to convert to a `double` value.</span></span>  
  
 `doubleValue`  
 <span data-ttu-id="f0f1b-108">Der `double` Wert.</span><span class="sxs-lookup"><span data-stu-id="f0f1b-108">The `double` value.</span></span>  
  
## <span data-ttu-id="f0f1b-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f0f1b-109">Return Value</span></span>  
 <span data-ttu-id="f0f1b-110">Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="f0f1b-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="f0f1b-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="f0f1b-111">Remarks</span></span>  
 <span data-ttu-id="f0f1b-112">Diese Funktion Ruft den Wert eines Zahlenwerts ab.</span><span class="sxs-lookup"><span data-stu-id="f0f1b-112">This function retrieves the value of a number value.</span></span> <span data-ttu-id="f0f1b-113">`JsErrorInvalidArgument`Wenn der Typ des Werts nicht number ist, tritt ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="f0f1b-113">It will fail with `JsErrorInvalidArgument` if the type of the value is not number.</span></span>  
  
 <span data-ttu-id="f0f1b-114">Erfordert einen aktiven Skriptkontext.</span><span class="sxs-lookup"><span data-stu-id="f0f1b-114">Requires an active script context.</span></span>  
  
## <span data-ttu-id="f0f1b-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f0f1b-115">Requirements</span></span>  
 <span data-ttu-id="f0f1b-116">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="f0f1b-116">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="f0f1b-117">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="f0f1b-117">See Also</span></span>  
 [<span data-ttu-id="f0f1b-118">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="f0f1b-118">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
