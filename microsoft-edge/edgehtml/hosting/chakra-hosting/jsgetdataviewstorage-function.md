---
description: Ruft den zugrunde liegenden Speicher Speicher ab, der von einer DataView verwendet wird.
title: JsGetDataViewStorage-Funktion | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 7c2180e0-51d5-4cc8-ad21-8bf29ff7c583
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 55f357e4a94b1edbc417ebb14ab99db11083dff4
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233998"
---
# JsGetDataViewStorage Funktion

Ruft den zugrunde liegenden Speicher Speicher ab, der von einem verwendet wird `DataView` .  
  
## Syntax  
  
```cpp  
STDAPI_(JsErrorCode) JsGetDataViewStorage(  
   _In_ JsValueRef dataView,  
   _Outptr_result_bytebuffer_(*bufferLength) BYTE **buffer,  
   _Out_ unsigned int *bufferLength  
);  
```  
  
#### Parameter  
 `dataView`  
 Die DataView-Instanz.  
  
 `buffer`  
 Der DataView-Puffer. Die Lebensdauer des zurückgegebenen Puffers entspricht der Lebensdauer von `DataView` . Der Pufferzeiger zählt nicht als Verweis auf das `DataView` zum Zweck der Garbage Collection.  
  
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
