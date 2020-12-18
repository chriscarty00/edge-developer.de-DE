---
description: Ruft den Wert `null` im aktuellen Skriptkontext ab.
title: JsGetNullValue-Funktion | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsGetNullValue
helpviewer_keywords:
- JsGetNullValue function
ms.assetid: 132a1496-8dfe-4d3c-a8f8-389f5b0b50d2
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 31e1ba19f9f27e75f0166238d98390e2c4a26c24
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233579"
---
# JsGetNullValue Funktion

Ruft den Wert `null` im aktuellen Skriptkontext ab.  
  
## Syntax  
  
```cpp  
STDAPI_(JsErrorCode) JsGetNullValue(  
   _Out_ JsValueRef *nullValue  
);  
```  
  
#### Parameter  
 `nullValue`  
 Der `null` Wert.  
  
## Rückgabewert  
 Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.  
  
## Hinweise  
 Erfordert einen aktiven Skriptkontext.  
  
## Anforderungen  
 **Kopfzeile:** jsrt. h  
  
## Weitere Informationen  
 [Referenz (JavaScript-Laufzeit)](../chakra-hosting/reference-javascript-runtime.md)
