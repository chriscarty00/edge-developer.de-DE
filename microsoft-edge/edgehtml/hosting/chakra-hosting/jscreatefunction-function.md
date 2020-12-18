---
description: Erstellt eine neue JavaScript-Funktion.
title: JsCreateFunction-Funktion | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsCreateFunction
helpviewer_keywords:
- JsCreateFunction function
ms.assetid: b298a96a-5ef7-4203-a8c8-55f9bfc6d2bb
caps.latest.revision: 13
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: f7e67e86e6d8055664bfb1b58e6d5653f6d75d1b
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11234109"
---
# JsCreateFunction Funktion

Erstellt eine neue JavaScript-Funktion.
  
## Syntax  
  
```cpp  
STDAPI_(JsErrorCode) JsCreateFunction(  
   _In_ JsNativeFunction nativeFunction,  
   _In_opt_ void *callbackState,  
   _Out_ JsValueRef *function  
);  
```  
  
#### Parameter  
 `nativeFunction`  
 Die Methode, die aufgerufen werden soll, wenn die Funktion aufgerufen wird.  
  
 `callbackState`  
 Vom Benutzer bereitgestellter Zustand, der an den Rückruf zurückgegeben wird.  
  
 `function`  
 Das neue Function-Objekt.  
  
## Rückgabewert  
 Das Ergebnis des Anrufs (sofern vorhanden).  
  
## Hinweise  
 Erfordert einen aktiven Skriptkontext.  
  
## Anforderungen  
 **Kopfzeile:** jsrt. h  
  
## Weitere Informationen  
 [Referenz (JavaScript-Laufzeit)](../chakra-hosting/reference-javascript-runtime.md)
