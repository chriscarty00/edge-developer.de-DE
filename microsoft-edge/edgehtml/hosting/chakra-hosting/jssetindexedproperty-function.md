---
description: Legt den Wert am angegebenen Index eines Objekts fest.
title: JsSetIndexedProperty-Funktion | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsSetIndexedProperty
helpviewer_keywords:
- JsSetIndexedProperty function
ms.assetid: ccbc5bf4-d99b-485c-ab25-d2bd1ed2142e
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 1fa961750fa5db262e1512d8d26572280d5e726c
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233731"
---
# JsSetIndexedProperty Funktion

Legt den Wert am angegebenen Index eines Objekts fest.  
  
## Syntax  
  
```cpp  
STDAPI_(JsErrorCode) JsSetIndexedProperty(  
   _In_ JsValueRef object,  
   _In_ JsValueRef index,  
   _In_ JsValueRef value  
);  
```  
  
#### Parameter  
 `object`  
 Das Objekt, das ausgeführt werden soll.  
  
 `index`  
 Der Index, der gesetzt werden soll.  
  
 `value`  
 Der Wert, der gesetzt werden soll.  
  
## Rückgabewert  
 Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.  
  
## Hinweise  
 Erfordert einen aktiven Skriptkontext.  
  
## Anforderungen  
 **Kopfzeile:** jsrt. h  
  
## Weitere Informationen  
 [Referenz (JavaScript-Laufzeit)](../chakra-hosting/reference-javascript-runtime.md)
