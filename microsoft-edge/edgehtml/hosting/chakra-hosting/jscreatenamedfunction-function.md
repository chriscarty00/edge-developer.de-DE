---
description: Erstellt eine neue JavaScript-Funktion mit dem Namen.
title: JsCreateNamedFunction-Funktion | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 72f40d06-ab82-4fed-a632-68af6b4126c2
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: b54add359422a9312a0ded641051fd04585f3d7e
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233890"
---
# JsCreateNamedFunction Funktion

Erstellt eine neue JavaScript-Funktion mit dem Namen.
  
## Syntax  
  
```cpp  
STDAPI_(JsErrorCode) JsCreateNamedFunction(  
   _In_ JsValueRef name,  
   _In_ JsNativeFunction nativeFunction,  
   _In_opt_ void *callbackState,  
   _Out_ JsValueRef *function  
);  
```  
  
#### Parameter  
 `name`  
 Der Name dieser Funktion, die für Diagnose-und stringification Zwecke verwendet wird.  
  
 `nativeFunction`  
 Die Methode, die aufgerufen werden soll, wenn die Funktion aufgerufen wird.  
  
 `callbackState`  
 Der Benutzer hat den Zustand bereitgestellt, der an den Rückruf zurückgegeben wird.  
  
 `function`  
 Das neue Function-Objekt.  
  
## Rückgabewert  
  
## Hinweise  
 Erfordert einen aktiven Skriptkontext.  
  
 Diese API wird nur im Microsoft Edge-Modus unterstützt.  
  
## Anforderungen  
 **Kopfzeile:** jsrt. h  
  
## Weitere Informationen  
 [Referenz (JavaScript-Laufzeit)](../chakra-hosting/reference-javascript-runtime.md)
