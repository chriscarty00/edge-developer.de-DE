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
# JsMemoryEventType-Enumeration
Zuordnungs Rückruf-Ereignistyp.  
  
## Syntax  
  
```cpp  
enum JsMemoryEventType;  
```  
  
## Member  
  
### Werte  
  
|Name|Beschreibung|  
|----------|-----------------|  
|`JsMemoryAllocate`|Gibt an, dass eine Speicherzuweisung angefordert wird.|  
|`JsMemoryFailure`|Gibt ein fehlgeschlagenes Zuordnungs Ereignis an.|  
|`JsMemoryFree`|Gibt ein Speicher freies Ereignis an.|  
  
## Anforderungen  
 **Kopfzeile:** jsrt. h  
  
## Weitere Informationen  
 [Referenz (JavaScript-Laufzeit)](../chakra-hosting/reference-javascript-runtime.md)