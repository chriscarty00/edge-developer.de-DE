---
description: Vergleichen Sie zwei JavaScript-Werte für Gleichheit.
title: JsEquals-Funktion | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsEquals
helpviewer_keywords:
- JsEquals function
ms.assetid: 8377a7b6-12ff-43e4-8cc8-5a5a198a168b
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 88f906419e73ed0de6ddde0a872becbd18908997
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11234326"
---
# JsEquals Funktion

Vergleichen Sie zwei JavaScript-Werte für Gleichheit.  
  
## Syntax  
  
```cpp  
STDAPI_(JsErrorCode) JsEquals(  
   _In_ JsValueRef object1,  
   _In_ JsValueRef object2,  
   _Out_ bool *result  
);  
```  
  
#### Parameter  
 `object1`  
 Das erste zu vergleichende Objekt.  
  
 `object2`  
 Das zweite zu vergleichende Objekt.  
  
 `result`  
 Gibt an, ob die Werte gleich sind.  
  
## Rückgabewert  
 Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.  
  
## Hinweise  
 Diese Funktion entspricht dem `==` Operator in JavaScript.  
  
 Erfordert einen aktiven Skriptkontext.  
  
## Anforderungen  
 **Kopfzeile:** jsrt. h  
  
## Weitere Informationen  
 [Referenz (JavaScript-Laufzeit)](../chakra-hosting/reference-javascript-runtime.md)
