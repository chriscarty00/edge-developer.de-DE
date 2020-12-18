---
description: Wandelt den Wert mithilfe der JavaScript-Standardsemantik in eine Zeichenfolge um.
title: JsConvertValueToString-Funktion | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsConvertValueToString
helpviewer_keywords:
- JsConvertValueToString function
ms.assetid: a97aca04-b2ce-446a-acf4-49cd6777a85c
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 499f9555f6385b8458524fb4e14b92339c0aa478
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233754"
---
# JsConvertValueToString Funktion

Wandelt den Wert mithilfe der JavaScript-Standardsemantik in eine Zeichenfolge um.  
  
## Syntax  
  
```cpp  
STDAPI_(JsErrorCode) JsConvertValueToString(  
   _In_ JsValueRef value,  
   _Out_ JsValueRef *stringValue  
);  
```  
  
#### Parameter  
 `value`  
 Der Wert, der konvertiert werden soll.  
  
 `stringValue`  
 Der konvertierte Wert.  
  
## Rückgabewert  
 Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.  
  
## Hinweise  
 Erfordert einen aktiven Skriptkontext.  
  
## Anforderungen  
 **Kopfzeile:** jsrt. h  
  
## Weitere Informationen  
 [Referenz (JavaScript-Laufzeit)](../chakra-hosting/reference-javascript-runtime.md)
