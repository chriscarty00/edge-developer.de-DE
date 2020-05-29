---
description: Erstellt einen JavaScript-Wert, bei dem es sich um eine Projektion des übergebenen `IInspectable` Zeigers handelt.
title: JsInspectableToObject-Funktion | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: dd0ad567-2ba8-4a63-bee4-2c6ff5ce9fa9
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 26ce17eb3abcefcf9a1f0cc773e9fe4c3aaf05cd
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10567233"
---
# <span data-ttu-id="94e5b-103">JsInspectableToObject-Funktion</span><span class="sxs-lookup"><span data-stu-id="94e5b-103">JsInspectableToObject Function</span></span>
<span data-ttu-id="94e5b-104">Erstellt einen JavaScript-Wert, bei dem es sich um eine Projektion des übergebenen `IInspectable` Zeigers handelt.</span><span class="sxs-lookup"><span data-stu-id="94e5b-104">Creates a JavaScript value that is a projection of the passed in `IInspectable` pointer.</span></span>  
  
## <span data-ttu-id="94e5b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="94e5b-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsInspectableToObject(  
        _In_ IInspectable  *inspectable,  
        _Out_ JsValueRef *value  
);  
```  
  
#### <span data-ttu-id="94e5b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="94e5b-106">Parameters</span></span>  
 `inspectable`  
 <span data-ttu-id="94e5b-107">A `IInspectable` , das projiziert werden soll.</span><span class="sxs-lookup"><span data-stu-id="94e5b-107">A `IInspectable` to be projected.</span></span>  
  
 `value`  
 <span data-ttu-id="94e5b-108">Ein JavaScript-Wert, bei dem es sich um eine Projektion von `IInspectable` .</span><span class="sxs-lookup"><span data-stu-id="94e5b-108">A JavaScript value that is a projection of the `IInspectable`.</span></span>  
  
## <span data-ttu-id="94e5b-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="94e5b-109">Return Value</span></span>  
 <span data-ttu-id="94e5b-110">Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="94e5b-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="94e5b-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="94e5b-111">Remarks</span></span>  
 <span data-ttu-id="94e5b-112">Der projizierte Wert kann vom Skript verwendet werden, um ein WinRT-Objekt aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="94e5b-112">The projected value can be used by script to call a WinRT object.</span></span> <span data-ttu-id="94e5b-113">Hosts sind für das Erzwingen von COM-Threading Regeln verantwortlich.</span><span class="sxs-lookup"><span data-stu-id="94e5b-113">Hosts are responsible for enforcing COM threading rules.</span></span>  
  
 <span data-ttu-id="94e5b-114">Erfordert einen aktiven Skriptkontext.</span><span class="sxs-lookup"><span data-stu-id="94e5b-114">Requires an active script context.</span></span>  
  
 <span data-ttu-id="94e5b-115">Diese API wird nur im EdgeHTML-Modus unterstützt.</span><span class="sxs-lookup"><span data-stu-id="94e5b-115">This API is supported only in EdgeHTML mode.</span></span>  
  
## <span data-ttu-id="94e5b-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="94e5b-116">Requirements</span></span>  
 <span data-ttu-id="94e5b-117">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="94e5b-117">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="94e5b-118">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="94e5b-118">See Also</span></span>  
 [<span data-ttu-id="94e5b-119">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="94e5b-119">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)