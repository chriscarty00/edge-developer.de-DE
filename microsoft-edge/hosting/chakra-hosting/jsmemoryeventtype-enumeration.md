---
description: Zuordnungs Rückruf-Ereignistyp.
title: JsMemoryEventType-Enumeration | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsMemoryEventType
helpviewer_keywords:
- JsMemoryEventType enumeration
ms.assetid: b4b176b6-b536-472e-8999-95b681a1df55
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 1e9833777ed8fe5a19fd2a1487715296279f7351
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10567219"
---
# <span data-ttu-id="43e34-103">JsMemoryEventType-Enumeration</span><span class="sxs-lookup"><span data-stu-id="43e34-103">JsMemoryEventType Enumeration</span></span>
<span data-ttu-id="43e34-104">Zuordnungs Rückruf-Ereignistyp.</span><span class="sxs-lookup"><span data-stu-id="43e34-104">Allocation callback event type.</span></span>  
  
## <span data-ttu-id="43e34-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="43e34-105">Syntax</span></span>  
  
```cpp  
enum JsMemoryEventType;  
```  
  
## <span data-ttu-id="43e34-106">Member</span><span class="sxs-lookup"><span data-stu-id="43e34-106">Members</span></span>  
  
### <span data-ttu-id="43e34-107">Werte</span><span class="sxs-lookup"><span data-stu-id="43e34-107">Values</span></span>  
  
|<span data-ttu-id="43e34-108">Name</span><span class="sxs-lookup"><span data-stu-id="43e34-108">Name</span></span>|<span data-ttu-id="43e34-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="43e34-109">Description</span></span>|  
|----------|-----------------|  
|`JsMemoryAllocate`|<span data-ttu-id="43e34-110">Gibt an, dass eine Speicherzuweisung angefordert wird.</span><span class="sxs-lookup"><span data-stu-id="43e34-110">Indicates a request for memory allocation.</span></span>|  
|`JsMemoryFailure`|<span data-ttu-id="43e34-111">Gibt ein fehlgeschlagenes Zuordnungs Ereignis an.</span><span class="sxs-lookup"><span data-stu-id="43e34-111">Indicates a failed allocation event.</span></span>|  
|`JsMemoryFree`|<span data-ttu-id="43e34-112">Gibt ein Speicher freies Ereignis an.</span><span class="sxs-lookup"><span data-stu-id="43e34-112">Indicates a memory freeing event.</span></span>|  
  
## <span data-ttu-id="43e34-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="43e34-113">Requirements</span></span>  
 <span data-ttu-id="43e34-114">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="43e34-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="43e34-115">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="43e34-115">See Also</span></span>  
 [<span data-ttu-id="43e34-116">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="43e34-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)