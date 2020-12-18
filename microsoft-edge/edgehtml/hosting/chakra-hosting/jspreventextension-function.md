---
description: Macht ein Objekt nicht erweiterbar.
title: JsPreventExtension-Funktion | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsPreventExtension
helpviewer_keywords:
- JsPreventExtension function
ms.assetid: 8da07e20-d076-4ae4-9fb0-3f3c141518c2
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 1904756a932bd581e05ec474004af7107da3f64b
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11234080"
---
# JsPreventExtension Funktion

Macht ein Objekt nicht erweiterbar.  
  
## Syntax  
  
```cpp  
STDAPI_(JsErrorCode) JsPreventExtension(  
   _In_ JsValueRef object  
);  
```  
  
#### Parameter  
 `object`  
 Das Objekt, das nicht erweiterbar sein soll.  
  
## Rückgabewert  
 Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.  
  
## Hinweise  
 Erfordert einen aktiven Skriptkontext.  
  
## Anforderungen  
 **Kopfzeile:** jsrt. h  
  
## Weitere Informationen  
 [Referenz (JavaScript-Laufzeit)](../chakra-hosting/reference-javascript-runtime.md)
