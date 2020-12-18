---
description: Konvertiert den Wert mit der standardmäßigen JavaScript-Semantik in Object.
title: JsConvertValueToObject-Funktion | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsConvertValueToObject
helpviewer_keywords:
- JsConvertValueToObject function
ms.assetid: 6528b28a-1d2b-417f-bf78-bf05547c52e1
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 6f3676b512585b0750c994bcfcdf9d2e6e4e1cc3
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233755"
---
# JsConvertValueToObject Funktion

Konvertiert den Wert mit der standardmäßigen JavaScript-Semantik in Object.  
  
## Syntax  
  
```cpp  
STDAPI_(JsErrorCode) JsConvertValueToObject(  
   _In_ JsValueRef value,  
   _Out_ JsValueRef *object  
);  
```  
  
#### Parameter  
 `value`  
 Der Wert, der konvertiert werden soll.  
  
 `object`  
 Der konvertierte Wert.  
  
## Rückgabewert  
 Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.  
  
## Hinweise  
 Erfordert einen aktiven Skriptkontext.  
  
## Anforderungen  
 **Kopfzeile:** jsrt. h  
  
## Weitere Informationen  
 [Referenz (JavaScript-Laufzeit)](../chakra-hosting/reference-javascript-runtime.md)
