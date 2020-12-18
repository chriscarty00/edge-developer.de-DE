---
description: Ruft den zugrunde liegenden Speicher Speicher ab, der von einem typisierten Array verwendet wird.
title: JsGetTypedArrayStorage-Funktion | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 52e4ac5f-cc71-456d-95de-a48f7327503d
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 442727228433368de14bac528ea416fcc2a95fa8
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233614"
---
# JsGetTypedArrayStorage Funktion

Ruft den zugrunde liegenden Speicher Speicher ab, der von einem typisierten Array verwendet wird.  
  
## Syntax  
  
```cpp  
STDAPI_(JsErrorCode) JsGetTypedArrayStorage(  
   _In_ JsValueRef typedArray,  
   _Outptr_result_bytebuffer_(*bufferLength) BYTE **buffer,  
   _Out_ unsigned int *bufferLength,  
   _Out_opt_ JsTypedArrayType *arrayType,  
   _Out_opt_ int *elementSize  
);  
```  
  
#### Parameter  
 `typedArray`  
 Die typisierte Arrayinstanz.  
  
 `buffer`  
 Der Puffer des Arrays. Die Lebensdauer des zurückgegebenen Puffers ist mit der Lebensdauer des Arrays identisch. Der Pufferzeiger zählt nicht als Verweis auf das Array zum Zweck der Garbage Collection.  
  
 `bufferLength`  
 Die Anzahl der Bytes im Puffer.  
  
 `arrayType`  
 Der Typ des Arrays.  
  
 `elementSize`  
 Die Größe eines Elements des Arrays.  
  
## Rückgabewert  
 Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.  
  
## Hinweise  
 Erfordert einen aktiven Skriptkontext.  
  
 Diese API wird nur im Microsoft Edge-Modus unterstützt.  
  
## Anforderungen  
 **Kopfzeile:** jsrt. h  
  
## Weitere Informationen  
 [Referenz (JavaScript-Laufzeit)](../chakra-hosting/reference-javascript-runtime.md)
