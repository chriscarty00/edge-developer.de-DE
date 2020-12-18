---
description: Legt die Laufzeit des aktuellen Kontexts auf einen Ausnahmezustand fest.
title: JsSetException-Funktion | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsSetException
helpviewer_keywords:
- JsSetException function
ms.assetid: c528793a-2e1b-4ee1-bd2e-e63fd547dc40
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 2c2e3840d2a831db23a525c5d8854b9b2fcfb8c9
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233949"
---
# JsSetException Funktion

Legt die Laufzeit des aktuellen Kontexts auf einen Ausnahmezustand fest.  
  
## Syntax  
  
```cpp  
STDAPI_(JsErrorCode) JsSetException(  
   _In_ JsValueRef exception  
);  
```  
  
#### Parameter  
 `exception`  
 Die JavaScript-Ausnahme, die für die Laufzeit des aktuellen Kontexts gesetzt werden soll.  
  
## Rückgabewert  
 `JsNoError` Wenn das Modul in einen Ausnahmezustand gesetzt wurde, wird andernfalls ein Fehlercode ausgelöst.  
  
## Hinweise  
 Wenn sich die Laufzeit des aktuellen Kontexts bereits in einem Ausnahmezustand befindet, gibt diese API zurück `JsErrorInExceptionState` .  
  
 Erfordert einen aktiven Skriptkontext.  
  
## Anforderungen  
 **Kopfzeile:** jsrt. h  
  
## Weitere Informationen  
 [Referenz (JavaScript-Laufzeit)](../chakra-hosting/reference-javascript-runtime.md)
