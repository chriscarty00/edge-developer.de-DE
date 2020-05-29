---
description: Der JavaScript-Typ eines JsValueRef.
title: JsValueType-Enumeration | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsValueType
helpviewer_keywords:
- JsValueType enumeration
ms.assetid: 6645e723-e554-41fc-b622-ab54ee044b3d
caps.latest.revision: 16
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: c42231525b55b49f0931a2ace33b373e0d4ae441
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10567194"
---
# JsValueType-Enumeration
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