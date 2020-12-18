---
description: Ruft die Liste aller Symbol Eigenschaften für das Objekt ab.
title: JsGetOwnPropertySymbols-Funktion | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 57c431e3-de0b-4ed0-b750-87a86448daff
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: d44da140f61a17d4cdc3a959c8fa7d017cbab1cc
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11234118"
---
# JsGetOwnPropertySymbols Funktion

Ruft die Liste aller Symbol Eigenschaften für das Objekt ab.  
  
## Syntax  
  
```cpp  
STDAPI_(JsErrorCode) JsGetOwnPropertySymbols(  
   _In_ JsValueRef object,  
   _Out_ JsValueRef *propertySymbols  
);  
```  
  
#### Parameter  
 `object`  
 Das Objekt, aus dem die Eigenschaften Symbole abgerufen werden sollen.  
  
 `propertySymbols`  
 Ein Array von Eigenschafts Symbolen.  
  
## Rückgabewert  
 Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.  
  
## Hinweise  
 Erfordert einen aktiven Skriptkontext.  
  
 Diese API wird nur im Microsoft Edge-Modus unterstützt.  
  
## Anforderungen  
 **Kopfzeile:** jsrt. h  
  
## Weitere Informationen  
 [Referenz (JavaScript-Laufzeit)](../chakra-hosting/reference-javascript-runtime.md)
