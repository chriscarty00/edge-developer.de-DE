---
description: Ruft den Skriptkontext ab, zu dem das Objekt gehört.
title: JsGetContextOfObject-Funktion | Microsoft docs
ms.prod: microsoft-edge
ms.topic: article
ms.assetid: cea6cdcd-790f-455c-af04-026af8ae2eb7
caps.latest.revision: 3
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 9085f9156e4e0ca9e952fe51447185239082f975
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11234007"
---
# JsGetContextOfObject Funktion

Ruft den Skriptkontext ab, zu dem das Objekt gehört.  
  
## Syntax  
  
```cpp  
STDAPI_(JsErrorCode) JsGetContextOfObject(  
  _In_ JsValueRef object,  
  _Out_ JsContextRef *context  
);  
```  
  
#### Parameter  
 `object`  
 Das Objekt, aus dem der Kontext abgerufen werden soll.  
  
 `context`  
 Der Kontext, zu dem das Objekt gehört.  
  
## Rückgabewert  
 Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.  
  
## Hinweise  
 Erfordert einen aktiven Skriptkontext.  
  
## Anforderungen  
 **Kopfzeile:** jsrt. h  
  
## Weitere Informationen  
 [Referenz (JavaScript-Laufzeit)](../chakra-hosting/reference-javascript-runtime.md)
