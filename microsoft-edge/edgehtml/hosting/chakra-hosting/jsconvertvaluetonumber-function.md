---
description: Wandelt den Wert mit der standardmäßigen JavaScript-Semantik in Number um.
title: JsConvertValueToNumber-Funktion | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsConvertValueToNumber
helpviewer_keywords:
- JsConvertValueToNumber function
ms.assetid: c47b8653-0591-4863-b8b5-33187b315816
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 8d00950ef3835c6d75f8f55ffe5002b32c6ee160
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233772"
---
# JsConvertValueToNumber Funktion

Wandelt den Wert mit der standardmäßigen JavaScript-Semantik in Number um.  
  
## Syntax  
  
```cpp  
STDAPI_(JsErrorCode) JsConvertValueToNumber(  
   _In_ JsValueRef value,  
   _Out_ JsValueRef *numberValue  
);  
```  
  
#### Parameter  
 `value`  
 Der Wert, der konvertiert werden soll.  
  
 `numberValue`  
 Der konvertierte Wert.  
  
## Rückgabewert  
 Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.  
  
## Hinweise  
 Erfordert einen aktiven Skriptkontext.  
  
## Anforderungen  
 **Kopfzeile:** jsrt. h  
  
## Weitere Informationen  
 [Referenz (JavaScript-Laufzeit)](../chakra-hosting/reference-javascript-runtime.md)
