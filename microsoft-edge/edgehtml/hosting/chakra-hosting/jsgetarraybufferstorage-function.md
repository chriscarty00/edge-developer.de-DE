---
description: Ruft den zugrunde liegenden Speicher Speicher ab, der von einem ArrayBuffer verwendet wird.
title: JsGetArrayBufferStorage-Funktion | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 712ae298-36a9-47ef-b089-e51835c056bc
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 64b031a81506e68322759eff49da7467cac6f219
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233877"
---
# JsGetArrayBufferStorage Funktion

Ruft den zugrunde liegenden Speicher Speicher ab, der von einem verwendet wird `ArrayBuffer` .  
  
## Syntax  
  
```cpp  
JsErrorCode STDAPI_ JsGetArrayBufferStorage(  
   _In_ JsValueRef arrayBuffer,  
   _Outptr_result_bytebuffer_(*bufferLength) BYTE **buffer,  
   _Out_ unsigned int *bufferLength  
);  
```  
  
#### Parameter  
 `arrayBuffer`  
 Die ArrayBuffer-Instanz.  
  
 `buffer`  
 Der ArrayBuffer-Puffer. Die Lebensdauer des zurückgegebenen Puffers entspricht der Lebensdauer von `ArrayBuffer` . Der Pufferzeiger zählt nicht als Verweis auf das `ArrayBuffer` zum Zweck der Garbage Collection.  
  
 `bufferLength`  
 Die Anzahl der Bytes im Puffer.  
  
## Rückgabewert  
 Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.  
  
## Hinweise  
 Erfordert einen aktiven Skriptkontext.  
  
 Diese API wird nur im Microsoft Edge-Modus unterstützt.  
  
## Anforderungen  
 **Kopfzeile:** jsrt. h  
  
## Weitere Informationen  
 [Referenz (JavaScript-Laufzeit)](../chakra-hosting/reference-javascript-runtime.md)
