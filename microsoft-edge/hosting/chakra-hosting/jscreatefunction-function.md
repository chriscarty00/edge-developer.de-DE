---
description: Erstellt eine neue JavaScript-Funktion.
title: JsCreateFunction-Funktion | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsCreateFunction
helpviewer_keywords:
- JsCreateFunction function
ms.assetid: b298a96a-5ef7-4203-a8c8-55f9bfc6d2bb
caps.latest.revision: 13
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 22585afcb379c281eda621c3b233ccf4bc278ad1
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10567298"
---
# JsCreateFunction-Funktion
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