---
description: Der JavaScript-Typ eines JsValueRef.
title: JsValueType-Enumeration | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsValueType
helpviewer_keywords:
- JsValueType enumeration
ms.assetid: 6645e723-e554-41fc-b622-ab54ee044b3d
caps.latest.revision: 16
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 840afcde86d4df80490d463921a74c73e42ddfc2
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233900"
---
# <span data-ttu-id="b23ea-103">JsValueType Enumeration</span><span class="sxs-lookup"><span data-stu-id="b23ea-103">JsValueType Enumeration</span></span>

<span data-ttu-id="b23ea-104">Der JavaScript-Typ eines JsValueRef.</span><span class="sxs-lookup"><span data-stu-id="b23ea-104">The JavaScript type of a JsValueRef.</span></span>  
  
## <span data-ttu-id="b23ea-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b23ea-105">Syntax</span></span>  
  
```cpp  
enum JsValueType {  
    JsUndefined      = 0,  
    JsNull           = 1,  
    JsNumber         = 2,  
    JsString         = 3,  
    JsBoolean        = 4,  
    JsObject         = 5,  
    JsFunction       = 6,  
    JsError          = 7,  
    JsArray          = 8,  
    JsSymbol         = 9,  
    JsArrayBuffer    = 10,  
    JsTypedArray     = 11,  
    JsDataView       = 12,  
};  
```  
  
## <span data-ttu-id="b23ea-106">Member</span><span class="sxs-lookup"><span data-stu-id="b23ea-106">Members</span></span>  
  
### <span data-ttu-id="b23ea-107">Werte</span><span class="sxs-lookup"><span data-stu-id="b23ea-107">Values</span></span>  
  
|<span data-ttu-id="b23ea-108">Name</span><span class="sxs-lookup"><span data-stu-id="b23ea-108">Name</span></span>|<span data-ttu-id="b23ea-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b23ea-109">Description</span></span>|  
|----------|-----------------|  
|`JsUndefined`|<span data-ttu-id="b23ea-110">Der Wert ist der `undefined` Wert.</span><span class="sxs-lookup"><span data-stu-id="b23ea-110">The value is the `undefined` value.</span></span>|  
|`JsNull`|<span data-ttu-id="b23ea-111">Der Wert ist der `null` Wert.</span><span class="sxs-lookup"><span data-stu-id="b23ea-111">The value is the `null` value.</span></span>|  
|`JsNumber`|<span data-ttu-id="b23ea-112">Der Wert ist ein JavaScript-Zahlenwert.</span><span class="sxs-lookup"><span data-stu-id="b23ea-112">The value is a JavaScript number value.</span></span>|  
|`JsString`|<span data-ttu-id="b23ea-113">Der Wert ist ein JavaScript-Zeichenfolgenwert.</span><span class="sxs-lookup"><span data-stu-id="b23ea-113">The value is a JavaScript string value.</span></span>|  
|`JsBoolean`|<span data-ttu-id="b23ea-114">Der Wert ist ein JavaScript-boolescher Wert.</span><span class="sxs-lookup"><span data-stu-id="b23ea-114">The value is a JavaScript Boolean value.</span></span>|  
|`JsObject`|<span data-ttu-id="b23ea-115">Der Wert ist ein JavaScript-Objektwert.</span><span class="sxs-lookup"><span data-stu-id="b23ea-115">The value is a JavaScript object value.</span></span>|  
|`JsFunction`|<span data-ttu-id="b23ea-116">Der Wert ist ein JavaScript-Funktionsobjekt Wert.</span><span class="sxs-lookup"><span data-stu-id="b23ea-116">The value is a JavaScript function object value.</span></span>|  
|`JsError`|<span data-ttu-id="b23ea-117">Der Wert ist ein JavaScript-Fehlerobjekt Wert.</span><span class="sxs-lookup"><span data-stu-id="b23ea-117">The value is a JavaScript error object value.</span></span>|  
|`JsArray`|<span data-ttu-id="b23ea-118">Der Wert ist ein JavaScript-Array Objektwert.</span><span class="sxs-lookup"><span data-stu-id="b23ea-118">The value is a JavaScript array object value.</span></span>|  
|`JsSymbol`|<span data-ttu-id="b23ea-119">Der Wert ist ein JavaScript-Symbolwert.</span><span class="sxs-lookup"><span data-stu-id="b23ea-119">The value is a JavaScript symbol value.</span></span><br /><br /> <span data-ttu-id="b23ea-120">Dieser Enumerationswert wird nur im Microsoft Edge-Modus unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b23ea-120">This enumeration value is supported only in Microsoft Edge mode.</span></span>|  
|`JsArrayBuffer`|<span data-ttu-id="b23ea-121">Der Wert ist ein JavaScript `ArrayBuffer` -Objektwert.</span><span class="sxs-lookup"><span data-stu-id="b23ea-121">The value is a JavaScript `ArrayBuffer` object value.</span></span><br /><br /> <span data-ttu-id="b23ea-122">Dieser Enumerationswert wird nur im Microsoft Edge-Modus unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b23ea-122">This enumeration value is supported only in Microsoft Edge mode.</span></span>|  
|`JsTypedArray`|<span data-ttu-id="b23ea-123">Der Wert ist ein JavaScript-typisierter Array Objektwert.</span><span class="sxs-lookup"><span data-stu-id="b23ea-123">The value is a JavaScript typed array object value.</span></span><br /><br /> <span data-ttu-id="b23ea-124">Dieser Enumerationswert wird nur im Microsoft Edge-Modus unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b23ea-124">This enumeration value is supported only in Microsoft Edge mode.</span></span>|  
|`JsDataView`|<span data-ttu-id="b23ea-125">Der Wert ist ein JavaScript `DataView` -Objektwert.</span><span class="sxs-lookup"><span data-stu-id="b23ea-125">The value is a JavaScript `DataView` object value.</span></span><br /><br /> <span data-ttu-id="b23ea-126">Dieser Enumerationswert wird nur im Microsoft Edge-Modus unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b23ea-126">This enumeration value is supported only in Microsoft Edge mode.</span></span>|  
  
## <span data-ttu-id="b23ea-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b23ea-127">Requirements</span></span>  
 <span data-ttu-id="b23ea-128">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="b23ea-128">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="b23ea-129">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="b23ea-129">See Also</span></span>  
 [<span data-ttu-id="b23ea-130">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="b23ea-130">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
