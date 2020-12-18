---
description: Legt eine Fortsetzungs Rückruffunktion für Versprechen fest, die vom Kontext aufgerufen wird, wenn eine Aufgabe zur zukünftigen Ausführung in die Warteschlange gestellt werden soll.
title: JsSetPromiseContinuationCallback-Funktion | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 6ef0faf4-1500-4bd9-aeca-c208492af8ea
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: da928431f05831c95d5bc116dbd129de9cb5f3b4
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233988"
---
# JsSetPromiseContinuationCallback Funktion

Legt eine Fortsetzungs Rückruffunktion für Versprechen fest, die vom Kontext aufgerufen wird, wenn eine Aufgabe zur zukünftigen Ausführung in die Warteschlange gestellt werden soll.  
  
## Syntax  
  
```cpp  
STDAPI_(JsErrorCode) JsSetPromiseContinuationCallback(  
   _In_ JsPromiseContinuationCallback promiseContinuationCallback,  
   _In_opt_ void *callbackState  
);  
```  
  
#### Parameter  
 `promiseContinuationCallback`  
 Die Rückruffunktion, die festzulegen ist.  
  
 `callbackState`  
 Der Benutzer hat den Zustand bereitgestellt, der an den Rückruf zurückgegeben wird.  
  
## Rückgabewert  
 Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.  
  
## Hinweise  
 Erfordert einen aktiven Skriptkontext.  
  
 Diese API wird nur im EdgeHTML-Modus unterstützt.  
  
## Anforderungen  
 **Kopfzeile:** jsrt. h  
  
## Weitere Informationen  
 [Referenz (JavaScript-Laufzeit)](../chakra-hosting/reference-javascript-runtime.md)
