---
description: Erstellt einen Zeichenfolgenwert aus einem Zeichenfolgenzeiger.
title: JsPointerToString-Funktion | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsPointerToString
helpviewer_keywords:
- JsPointerToString function
ms.assetid: c71ce07e-4359-450c-afbf-a6ab7d48dddf
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: b3c5b2d6439244bc9584e15c361412c8a1e87557
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10568348"
---
# JsPointerToString-Funktion
Erstellt einen Zeichenfolgenwert aus einem Zeichenfolgenzeiger.  
  
## Syntax  
  
```cpp  
STDAPI_(JsErrorCode) JsPointerToString(  
   _In_reads_(stringLength) const wchar_t *stringValue,  
   _In_ size_t stringLength,  
   _Out_ JsValueRef *value  
);  
```  
  
#### Parameter  
 `stringValue`  
 Der Zeichenfolgenzeiger, der in einen Zeichenfolgenwert konvertiert werden soll.  
  
 `stringLength`  
 Die Länge der zu konvertierenden Zeichenfolge.  
  
 `value`  
 Der neue Zeichenfolgenwert.  
  
## Rückgabewert  
 Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.  
  
## Hinweise  
 Erfordert einen aktiven Skriptkontext.  
  
## Anforderungen  
 **Kopfzeile:** jsrt. h  
  
## Weitere Informationen  
 [Referenz (JavaScript-Laufzeit)](../chakra-hosting/reference-javascript-runtime.md)