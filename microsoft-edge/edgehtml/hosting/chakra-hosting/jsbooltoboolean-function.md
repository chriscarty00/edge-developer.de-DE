---
description: Erstellt einen booleschen Wert aus einem `bool` Wert.
title: JsBoolToBoolean-Funktion | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsBoolToBoolean
helpviewer_keywords:
- JsBoolToBoolean function
ms.assetid: 24322ea3-0638-40a3-9b4c-fc912ebed3ff
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 3d6ec9f85d53e0d78c6bbe1c7d3282971831717b
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233770"
---
# <span data-ttu-id="9a4b4-103">JsBoolToBoolean Funktion</span><span class="sxs-lookup"><span data-stu-id="9a4b4-103">JsBoolToBoolean Function</span></span>

<span data-ttu-id="9a4b4-104">Erstellt einen booleschen Wert aus einem `bool` Wert.</span><span class="sxs-lookup"><span data-stu-id="9a4b4-104">Creates a Boolean value from a `bool` value.</span></span>  
  
## <span data-ttu-id="9a4b4-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="9a4b4-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode JsBoolToBoolean(  
   _In_ bool value,  
   _Out_ JsValueRef *booleanValue  
);  
```  
  
#### <span data-ttu-id="9a4b4-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="9a4b4-106">Parameters</span></span>  
 `value`  
 <span data-ttu-id="9a4b4-107">Der Wert, der konvertiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="9a4b4-107">The value to be converted.</span></span>  
  
 `booleanValue`  
 <span data-ttu-id="9a4b4-108">Der konvertierte Wert.</span><span class="sxs-lookup"><span data-stu-id="9a4b4-108">The converted value.</span></span>  
  
## <span data-ttu-id="9a4b4-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9a4b4-109">Return Value</span></span>  
 <span data-ttu-id="9a4b4-110">Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="9a4b4-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="9a4b4-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="9a4b4-111">Remarks</span></span>  
 <span data-ttu-id="9a4b4-112">Erfordert einen aktiven Skriptkontext.</span><span class="sxs-lookup"><span data-stu-id="9a4b4-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="9a4b4-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9a4b4-113">Requirements</span></span>  
 <span data-ttu-id="9a4b4-114">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="9a4b4-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="9a4b4-115">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="9a4b4-115">See Also</span></span>  
 [<span data-ttu-id="9a4b4-116">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="9a4b4-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
