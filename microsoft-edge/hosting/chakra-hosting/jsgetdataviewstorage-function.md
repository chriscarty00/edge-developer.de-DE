---
description: Ruft den zugrunde liegenden Speicher Speicher ab, der von einer DataView verwendet wird.
title: JsGetDataViewStorage-Funktion | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 7c2180e0-51d5-4cc8-ad21-8bf29ff7c583
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 54f8a91b6dea1e0997ad31d6585ea741fde8ba99
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10567261"
---
# JsGetDataViewStorage-Funktion
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