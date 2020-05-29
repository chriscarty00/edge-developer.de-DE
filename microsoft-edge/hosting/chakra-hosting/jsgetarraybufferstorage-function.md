---
description: Ruft den zugrunde liegenden Speicher Speicher ab, der von einem ArrayBuffer verwendet wird.
title: JsGetArrayBufferStorage-Funktion | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 712ae298-36a9-47ef-b089-e51835c056bc
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 1e8d265f3e81015ba9f5d0547b6b1c7246c23ce5
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10568397"
---
# JsGetArrayBufferStorage-Funktion
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