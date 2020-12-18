---
description: Ruft den `int` Wert eines Zahlenwerts ab.
title: JsNumberToInt-Funktion | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 8b9256d6-76ac-4c74-a97c-fbb16c13f5f5
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 928be9a7cc5cd3e26e8b8df99af1e08a6c50209c
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11234091"
---
# <span data-ttu-id="820fb-103">JsNumberToInt Funktion</span><span class="sxs-lookup"><span data-stu-id="820fb-103">JsNumberToInt Function</span></span>

<span data-ttu-id="820fb-104">Ruft den `int` Wert eines Zahlenwerts ab.</span><span class="sxs-lookup"><span data-stu-id="820fb-104">Retrieves the `int` value of a number value.</span></span>  
  
## <span data-ttu-id="820fb-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="820fb-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsNumberToInt(  
      _In_ JsValueRef value,  
      _Out_ int *intValue  
);  
```  
  
#### <span data-ttu-id="820fb-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="820fb-106">Parameters</span></span>  
 `value`  
 <span data-ttu-id="820fb-107">Der Zahlenwert, der in einen Wert konvertiert werden soll `int` .</span><span class="sxs-lookup"><span data-stu-id="820fb-107">The number value to convert to an `int` value.</span></span>  
  
 `intValue`  
 <span data-ttu-id="820fb-108">Der `int` Wert.</span><span class="sxs-lookup"><span data-stu-id="820fb-108">The `int` value.</span></span>  
  
## <span data-ttu-id="820fb-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="820fb-109">Return Value</span></span>  
  
## <span data-ttu-id="820fb-110">Hinweise</span><span class="sxs-lookup"><span data-stu-id="820fb-110">Remarks</span></span>  
 <span data-ttu-id="820fb-111">Diese Funktion Ruft den Wert eines Zahlenwerts ab und wandelt ihn in einen `int` Wert um.</span><span class="sxs-lookup"><span data-stu-id="820fb-111">This function retrieves the value of a number value and converts to an `int` value.</span></span> <span data-ttu-id="820fb-112">`JsErrorInvalidArgument`Wenn der Typ des Werts nicht number ist, tritt ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="820fb-112">It will fail with `JsErrorInvalidArgument` if the type of the value is not number.</span></span>  
  
 <span data-ttu-id="820fb-113">Erfordert einen aktiven Skriptkontext.</span><span class="sxs-lookup"><span data-stu-id="820fb-113">Requires an active script context.</span></span>  
  
 <span data-ttu-id="820fb-114">Diese API wird nur im EdgeHTML-Modus unterstützt.</span><span class="sxs-lookup"><span data-stu-id="820fb-114">This API is supported only in EdgeHTML mode.</span></span>  
  
## <span data-ttu-id="820fb-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="820fb-115">Requirements</span></span>  
 <span data-ttu-id="820fb-116">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="820fb-116">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="820fb-117">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="820fb-117">See Also</span></span>  
 [<span data-ttu-id="820fb-118">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="820fb-118">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
