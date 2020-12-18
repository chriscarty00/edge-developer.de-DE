---
description: Ruft den Zeichenfolgenzeiger eines Zeichenfolgenwerts ab.
title: JsStringToPointer-Funktion | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsStringToPointer
helpviewer_keywords:
- JsStringToPointer function
ms.assetid: c7aa7a09-489d-4435-8f8a-aeb62f8875ae
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 77b8e16be41d8b5541129b50fa200b947f566342
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233906"
---
# JsStringToPointer Funktion

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
