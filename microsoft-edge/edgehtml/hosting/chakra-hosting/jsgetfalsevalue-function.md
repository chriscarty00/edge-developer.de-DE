---
description: Ruft den Wert `false` im aktuellen Skriptkontext ab.
title: JsGetFalseValue-Funktion | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsGetFalseValue
helpviewer_keywords:
- JsGetFalseValue function
ms.assetid: 621a584c-4ca8-4ba0-b19a-6cb50cf830b6
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: c87ad969fc7547f4d650148005327fb93dce805d
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233995"
---
# JsGetFalseValue Funktion

Ruft den Wert `false` im aktuellen Skriptkontext ab.  
  
## Syntax  
  
```cpp  
STDAPI_(JsErrorCode) JsGetFalseValue(  
   _Out_ JsValueRef *falseValue  
);  
```  
  
#### Parameter  
 `falseValue`  
 Der `false` Wert.  
  
## Rückgabewert  
 Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.  
  
## Hinweise  
 Erfordert einen aktiven Skriptkontext.  
  
## Anforderungen  
 **Kopfzeile:** jsrt. h  
  
## Weitere Informationen  
 [Referenz (JavaScript-Laufzeit)](../chakra-hosting/reference-javascript-runtime.md)
