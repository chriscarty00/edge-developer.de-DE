---
description: Ruft den Zeichenfolgenzeiger eines Zeichenfolgenwerts ab.
title: JsStringToPointer-Funktion | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsStringToPointer
helpviewer_keywords:
- JsStringToPointer function
ms.assetid: c7aa7a09-489d-4435-8f8a-aeb62f8875ae
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 1f5997894c4ea479378a323b230492dde28ab177
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10568204"
---
# JsStringToPointer-Funktion
Ruft den Zeichenfolgenzeiger eines Zeichenfolgenwerts ab.  
  
## Syntax  
  
```cpp  
STDAPI_(JsErrorCode) JsStringToPointer(  
   _In_ JsValueRef value,  
   _Outptr_result_buffer_(*stringLength) const wchar_t **stringValue,  
   _Out_ size_t *stringLength  
);  
```  
  
#### Parameter  
 `value`  
 Der Zeichenfolgenwert, der in einen Zeichenfolgenzeiger konvertiert werden soll.  
  
 `stringValue`  
 Der Zeichenfolgenzeiger.  
  
 `stringLength`  
 Die Länge der Zeichenfolge.  
  
## Rückgabewert  
 Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.  
  
## Hinweise  
 Diese Funktion Ruft den Zeichenfolgenzeiger eines Zeichenfolgenwerts ab. `JsErrorInvalidArgument`Wenn der Typ des Werts keine Zeichenfolge ist, tritt ein Fehler auf. Die Lebensdauer der zurückgegebenen Zeichenfolge entspricht der Lebensdauer des Werts, von dem Sie stammen, der Zeichenfolgenzeiger wird jedoch nicht als Verweis auf den Wert betrachtet (und wird daher nicht davon abgeholt).  
  
 Erfordert einen aktiven Skriptkontext.  
  
## Anforderungen  
 **Kopfzeile:** jsrt. h  
  
## Weitere Informationen  
 [Referenz (JavaScript-Laufzeit)](../chakra-hosting/reference-javascript-runtime.md)