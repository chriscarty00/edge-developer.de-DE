---
description: Erstellt einen JavaScript-Wert, bei dem es sich um eine Projektion des übergebenen Werts handelt `VARIANT` .
title: JsVariantToValue-Funktion | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsVariantToValue
helpviewer_keywords:
- JsVariantToValue function
ms.assetid: e8f9eb8b-55b3-4b65-927e-cad5b482edee
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 01796bc38548cf56b500731d899541ef214ec4e3
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10567191"
---
# <span data-ttu-id="b77de-103">JsVariantToValue-Funktion</span><span class="sxs-lookup"><span data-stu-id="b77de-103">JsVariantToValue Function</span></span>
<span data-ttu-id="b77de-104">Erstellt einen JavaScript-Wert, bei dem es sich um eine Projektion des übergebenen Werts handelt `VARIANT` .</span><span class="sxs-lookup"><span data-stu-id="b77de-104">Creates a JavaScript value that is a projection of the passed in `VARIANT`.</span></span>  
  
## <span data-ttu-id="b77de-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b77de-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsVariantToValue(  
   _In_ VARIANT *variant,  
   _Out_ JsValueRef *value  
);  
```  
  
#### <span data-ttu-id="b77de-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="b77de-106">Parameters</span></span>  
 `variant`  
 <span data-ttu-id="b77de-107">A `VARIANT` , das projiziert werden soll.</span><span class="sxs-lookup"><span data-stu-id="b77de-107">A `VARIANT` to be projected.</span></span>  
  
 `value`  
 <span data-ttu-id="b77de-108">Ein JavaScript-Wert, bei dem es sich um eine Projektion von `VARIANT` .</span><span class="sxs-lookup"><span data-stu-id="b77de-108">A JavaScript value that is a projection of the `VARIANT`.</span></span>  
  
## <span data-ttu-id="b77de-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b77de-109">Return Value</span></span>  
 <span data-ttu-id="b77de-110">Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="b77de-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="b77de-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="b77de-111">Remarks</span></span>  
 <span data-ttu-id="b77de-112">Der projizierte Wert kann vom Skript verwendet werden, um ein COM-Automatisierungsobjekt aus einem Skript aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="b77de-112">The projected value can be used by script to call a COM automation object from script.</span></span> <span data-ttu-id="b77de-113">Hosts sind für das Erzwingen von COM-Threading Regeln verantwortlich.</span><span class="sxs-lookup"><span data-stu-id="b77de-113">Hosts are responsible for enforcing COM threading rules.</span></span>  
  
 <span data-ttu-id="b77de-114">Erfordert einen aktiven Skriptkontext.</span><span class="sxs-lookup"><span data-stu-id="b77de-114">Requires an active script context.</span></span>  
  
## <span data-ttu-id="b77de-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b77de-115">Requirements</span></span>  
 <span data-ttu-id="b77de-116">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="b77de-116">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="b77de-117">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="b77de-117">See Also</span></span>  
 [<span data-ttu-id="b77de-118">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="b77de-118">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)