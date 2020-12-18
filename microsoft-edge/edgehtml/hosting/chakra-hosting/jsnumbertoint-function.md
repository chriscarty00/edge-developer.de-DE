---
description: Ruft den `int` Wert eines Zahlenwerts ab.
title: JsNumberToInt-Funktion | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 8b9256d6-76ac-4c74-a97c-fbb16c13f5f5
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 928be9a7cc5cd3e26e8b8df99af1e08a6c50209c
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11234091"
---
# JsNumberToInt Funktion

Ruft den `int` Wert eines Zahlenwerts ab.  
  
## Syntax  
  
```cpp  
STDAPI_(JsErrorCode) JsNumberToInt(  
      _In_ JsValueRef value,  
      _Out_ int *intValue  
);  
```  
  
#### Parameter  
 `value`  
 Der Zahlenwert, der in einen Wert konvertiert werden soll `int` .  
  
 `intValue`  
 Der `int` Wert.  
  
## Rückgabewert  
  
## Hinweise  
 Diese Funktion Ruft den Wert eines Zahlenwerts ab und wandelt ihn in einen `int` Wert um. `JsErrorInvalidArgument`Wenn der Typ des Werts nicht number ist, tritt ein Fehler auf.  
  
 Erfordert einen aktiven Skriptkontext.  
  
 Diese API wird nur im EdgeHTML-Modus unterstützt.  
  
## Anforderungen  
 **Kopfzeile:** jsrt. h  
  
## Weitere Informationen  
 [Referenz (JavaScript-Laufzeit)](../chakra-hosting/reference-javascript-runtime.md)
