---
description: Ruft den JavaScript-Typ eines JsValueRef ab.
title: JsGetValueType-Funktion | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsGetValueType
helpviewer_keywords:
- JsGetValueType function
ms.assetid: f403cf7c-c8c0-4a17-bfa9-0302d00e760e
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: b2e9937ca13bf2a680a4a33c07020d06c53efdf3
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233618"
---
# JsGetValueType Funktion

Ruft den JavaScript-Typ eines JsValueRef ab.  
  
## Syntax  
  
```cpp  
STDAPI_(JsErrorCode) JsGetValueType(  
   _In_ JsValueRef value,  
   _Out_ JsValueType *type  
);  
```  
  
#### Parameter  
 `value`  
 Der Wert, dessen Typ zurückgegeben werden soll.  
  
 `type`  
 Der Typ des Werts.  
  
## Rückgabewert  
 Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.  
  
## Hinweise  
 Erfordert einen aktiven Skriptkontext.  
  
## Anforderungen  
 **Kopfzeile:** jsrt. h  
  
## Weitere Informationen  
 [Referenz (JavaScript-Laufzeit)](../chakra-hosting/reference-javascript-runtime.md)
