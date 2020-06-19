---
description: Ruft häufig verwendete Eigenschaften eines typisierten Arrays ab.
title: JsGetTypedArrayInfo-Funktion | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 992bc4e9-3d06-4ad2-8b6b-88a437360f81
caps.latest.revision: 3
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 24046acc7118cd8f540ba8ceb9976368e93d51ff
ms.sourcegitcommit: 037a2d62333691104c9accb4862968f80a3465a2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/18/2020
ms.locfileid: "10752269"
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