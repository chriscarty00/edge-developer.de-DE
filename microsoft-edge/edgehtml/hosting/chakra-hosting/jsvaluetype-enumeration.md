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
# JsValueType Enumeration

Der JavaScript-Typ eines JsValueRef.  
  
## Syntax  
  
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
  
## Member  
  
### Werte  
  
|Name|Beschreibung|  
|----------|-----------------|  
|`JsUndefined`|Der Wert ist der `undefined` Wert.|  
|`JsNull`|Der Wert ist der `null` Wert.|  
|`JsNumber`|Der Wert ist ein JavaScript-Zahlenwert.|  
|`JsString`|Der Wert ist ein JavaScript-Zeichenfolgenwert.|  
|`JsBoolean`|Der Wert ist ein JavaScript-boolescher Wert.|  
|`JsObject`|Der Wert ist ein JavaScript-Objektwert.|  
|`JsFunction`|Der Wert ist ein JavaScript-Funktionsobjekt Wert.|  
|`JsError`|Der Wert ist ein JavaScript-Fehlerobjekt Wert.|  
|`JsArray`|Der Wert ist ein JavaScript-Array Objektwert.|  
|`JsSymbol`|Der Wert ist ein JavaScript-Symbolwert.<br /><br /> Dieser Enumerationswert wird nur im Microsoft Edge-Modus unterstützt.|  
|`JsArrayBuffer`|Der Wert ist ein JavaScript `ArrayBuffer` -Objektwert.<br /><br /> Dieser Enumerationswert wird nur im Microsoft Edge-Modus unterstützt.|  
|`JsTypedArray`|Der Wert ist ein JavaScript-typisierter Array Objektwert.<br /><br /> Dieser Enumerationswert wird nur im Microsoft Edge-Modus unterstützt.|  
|`JsDataView`|Der Wert ist ein JavaScript `DataView` -Objektwert.<br /><br /> Dieser Enumerationswert wird nur im Microsoft Edge-Modus unterstützt.|  
  
## Anforderungen  
 **Kopfzeile:** jsrt. h  
  
## Weitere Informationen  
 [Referenz (JavaScript-Laufzeit)](../chakra-hosting/reference-javascript-runtime.md)
