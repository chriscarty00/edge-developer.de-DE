---
description: Legt die internen Daten von JsrtContext fest.
title: JsSetContextData-Funktion | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: be90aa6a-b001-4a6f-90c5-c2135e913be0
caps.latest.revision: 4
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: cac404b9e79bafb5a8eafb47e893dbdf38a02405
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11234071"
---
# JsSetContextData Funktion

Legt die internen Daten von JsrtContext fest.  
  
## Syntax  
  
```cpp  
STDAPI_(JsErrorCode) JsSetContextData(  
  _In_ JsContextRef context,  
  _In_ void *data  
);  
  
```  
  
#### Parameter  
 `context`  
 Der Kontext, auf den die Daten gesetzt werden sollen.  
  
 `data`  
 Der Zeiger auf die Daten, die gesetzt werden sollen.  
  
## Rückgabewert  
 Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.  
  
## Hinweise  
 Erfordert einen aktiven Skriptkontext.  
  
## Anforderungen  
 **Kopfzeile:** jsrt. h  
  
## Weitere Informationen  
 [Referenz (JavaScript-Laufzeit)](../chakra-hosting/reference-javascript-runtime.md)
