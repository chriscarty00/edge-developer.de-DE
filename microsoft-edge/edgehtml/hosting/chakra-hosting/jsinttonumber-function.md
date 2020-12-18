---
description: Erstellt einen Zahlenwert aus einem `int` Wert.
title: JsIntToNumber-Funktion | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 1393c4ac-7189-4e9c-8e54-b0e041c22112
caps.latest.revision: 4
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 24e861d1535ae79843fb35de8a047031a479fe16
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11234133"
---
# <span data-ttu-id="70b89-103">JsIntToNumber Funktion</span><span class="sxs-lookup"><span data-stu-id="70b89-103">JsIntToNumber Function</span></span>

<span data-ttu-id="70b89-104">Erstellt einen Zahlenwert aus einem `int` Wert.</span><span class="sxs-lookup"><span data-stu-id="70b89-104">Creates a number value from an `int` value.</span></span>  
  
## <span data-ttu-id="70b89-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="70b89-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsIntToNumber(  
   _In_ int intValue,  
   _Out_ JsValueRef *value  
);  
```  
  
#### <span data-ttu-id="70b89-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="70b89-106">Parameters</span></span>  
 `intValue`  
 <span data-ttu-id="70b89-107">Die `int` Konvertierung in einen Zahlenwert.</span><span class="sxs-lookup"><span data-stu-id="70b89-107">The `int` to convert to a number value.</span></span>  
  
 `value`  
 <span data-ttu-id="70b89-108">Der neue Zahlenwert.</span><span class="sxs-lookup"><span data-stu-id="70b89-108">The new number value.</span></span>  
  
## <span data-ttu-id="70b89-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="70b89-109">Return Value</span></span>  
 <span data-ttu-id="70b89-110">Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="70b89-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="70b89-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="70b89-111">Remarks</span></span>  
 <span data-ttu-id="70b89-112">Erfordert einen aktiven Skriptkontext.</span><span class="sxs-lookup"><span data-stu-id="70b89-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="70b89-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="70b89-113">Requirements</span></span>  
 <span data-ttu-id="70b89-114">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="70b89-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="70b89-115">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="70b89-115">See Also</span></span>  
 [<span data-ttu-id="70b89-116">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="70b89-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
