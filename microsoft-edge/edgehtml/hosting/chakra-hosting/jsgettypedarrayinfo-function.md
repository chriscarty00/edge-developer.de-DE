---
description: Ruft häufig verwendete Eigenschaften eines typisierten Arrays ab.
title: JsGetTypedArrayInfo-Funktion | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 992bc4e9-3d06-4ad2-8b6b-88a437360f81
caps.latest.revision: 3
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: fdc9a05a2aebdabfd0c8e95c848d3bd5f97e580a
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11234117"
---
# JsGetTypedArrayInfo Funktion

Ruft häufig verwendete Eigenschaften eines typisierten Arrays ab.  
  
## Syntax  
  
```cpp  
STDAPI_(JsErrorCode) JsGetTypedArrayInfo(  
  _In_ JsValueRef typedArray,  
  _Out_opt_ JsTypedArrayType *arrayType,  
  _Out_opt_ JsValueRef *arrayBuffer,  
  _Out_opt_ unsigned int *byteOffset,  
  _Out_opt_ unsigned int *byteLength  
);  
  
```  
  
#### Parameter  
 `typedArray`  
 Die typisierte Arrayinstanz.  
  
 `arrayType`  
 Der Typ des Arrays.  
  
 `arrayBuffer`  
 Der `ArrayBuffer` Backstore des Arrays.  
  
 `byteOffset`  
 Der Offset in Bytes vom Anfang des arrayBuffer, auf den das Array verweist.  
  
 `byteLength`  
 Die Anzahl der Bytes im Array.  
  
## Rückgabewert  
 Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.  
  
## Hinweise  
 Erfordert einen aktiven Skriptkontext.  
  
## Anforderungen  
 **Kopfzeile:** jsrt. h  
  
## Weitere Informationen  
 [Referenz (JavaScript-Laufzeit)](../chakra-hosting/reference-javascript-runtime.md)
