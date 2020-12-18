---
description: Legt den Prototyp eines Objekts fest.
title: JsSetPrototype-Funktion | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 88e1e421-4ae5-4e3b-b377-19256cc80e9f
caps.latest.revision: 4
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 860a7b8d85e043c87d554e09de50d0cb642b273a
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233734"
---
# JsSetPrototype Funktion

Legt den Prototyp eines Objekts fest.  
  
## Syntax  
  
```cpp  
STDAPI_(JsErrorCode) JsSetPrototype(  
   _In_ JsValueRef object,  
   _In_ JsValueRef prototypeObject  
);  
```  
  
#### Parameter  
 `object`  
 Das Objekt, dessen Prototyp geändert werden soll.  
  
 `prototypeObject`  
 Der neue Prototyp des Objekts.  
  
## Rückgabewert  
 Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.  
  
## Hinweise  
 Erfordert einen aktiven Skriptkontext.  
  
## Anforderungen  
 **Kopfzeile:** jsrt. h  
  
## Weitere Informationen  
 [Referenz (JavaScript-Laufzeit)](../chakra-hosting/reference-javascript-runtime.md)
