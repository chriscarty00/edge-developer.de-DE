---
description: Zuordnungs Rückruf-Ereignistyp.
title: JsMemoryEventType-Enumeration | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsMemoryEventType
helpviewer_keywords:
- JsMemoryEventType enumeration
ms.assetid: b4b176b6-b536-472e-8999-95b681a1df55
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: a28010f908285098cf652b497b6d6c272bc763fc
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233559"
---
# <span data-ttu-id="21813-103">JsMemoryEventType Enumeration</span><span class="sxs-lookup"><span data-stu-id="21813-103">JsMemoryEventType Enumeration</span></span>

<span data-ttu-id="21813-104">Zuordnungs Rückruf-Ereignistyp.</span><span class="sxs-lookup"><span data-stu-id="21813-104">Allocation callback event type.</span></span>  
  
## <span data-ttu-id="21813-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="21813-105">Syntax</span></span>  
  
```cpp  
enum JsMemoryEventType;  
```  
  
## <span data-ttu-id="21813-106">Member</span><span class="sxs-lookup"><span data-stu-id="21813-106">Members</span></span>  
  
### <span data-ttu-id="21813-107">Werte</span><span class="sxs-lookup"><span data-stu-id="21813-107">Values</span></span>  
  
|<span data-ttu-id="21813-108">Name</span><span class="sxs-lookup"><span data-stu-id="21813-108">Name</span></span>|<span data-ttu-id="21813-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="21813-109">Description</span></span>|  
|----------|-----------------|  
|`JsMemoryAllocate`|<span data-ttu-id="21813-110">Gibt an, dass eine Speicherzuweisung angefordert wird.</span><span class="sxs-lookup"><span data-stu-id="21813-110">Indicates a request for memory allocation.</span></span>|  
|`JsMemoryFailure`|<span data-ttu-id="21813-111">Gibt ein fehlgeschlagenes Zuordnungs Ereignis an.</span><span class="sxs-lookup"><span data-stu-id="21813-111">Indicates a failed allocation event.</span></span>|  
|`JsMemoryFree`|<span data-ttu-id="21813-112">Gibt ein Speicher freies Ereignis an.</span><span class="sxs-lookup"><span data-stu-id="21813-112">Indicates a memory freeing event.</span></span>|  
  
## <span data-ttu-id="21813-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="21813-113">Requirements</span></span>  
 <span data-ttu-id="21813-114">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="21813-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="21813-115">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="21813-115">See Also</span></span>  
 [<span data-ttu-id="21813-116">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="21813-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
