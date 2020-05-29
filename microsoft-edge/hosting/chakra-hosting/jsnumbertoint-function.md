---
description: Ruft den `int` Wert eines Zahlenwerts ab.
title: JsNumberToInt-Funktion | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 8b9256d6-76ac-4c74-a97c-fbb16c13f5f5
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: cf4c8cb42c737cfb9efee5422fe6bb3c1389cbfd
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10568356"
---
# JsNumberToInt-Funktion
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