---
description: Erstellt einen Zahlenwert aus einem `int` Wert.
title: JsIntToNumber-Funktion | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 1393c4ac-7189-4e9c-8e54-b0e041c22112
caps.latest.revision: 4
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 24e861d1535ae79843fb35de8a047031a479fe16
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11234133"
---
# JsIntToNumber Funktion

Erstellt einen Zahlenwert aus einem `int` Wert.  
  
## Syntax  
  
```cpp  
STDAPI_(JsErrorCode) JsIntToNumber(  
   _In_ int intValue,  
   _Out_ JsValueRef *value  
);  
```  
  
#### Parameter  
 `intValue`  
 Die `int` Konvertierung in einen Zahlenwert.  
  
 `value`  
 Der neue Zahlenwert.  
  
## Rückgabewert  
 Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.  
  
## Hinweise  
 Erfordert einen aktiven Skriptkontext.  
  
## Anforderungen  
 **Kopfzeile:** jsrt. h  
  
## Weitere Informationen  
 [Referenz (JavaScript-Laufzeit)](../chakra-hosting/reference-javascript-runtime.md)
