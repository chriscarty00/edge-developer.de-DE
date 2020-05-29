---
description: Erstellt ein Array Objekt mit JavaScript-Typisierung.
title: JsCreateTypedArray-Funktion | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 937a2a91-6f5f-4aaa-a018-d3089702bf36
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 57c5d15d76bf8b3ff29d10f7500fe41b3e959f68
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10567281"
---
# JsCreateTypedArray-Funktion
Erstellt ein Array Objekt mit JavaScript-Typisierung.  
  
## Syntax  
  
```cpp  
STDAPI_(JsErrorCode) JsCreateTypedArray(  
   _In_ JsTypedArrayType arrayType,  
   _In_ JsValueRef baseArray,  
   _In_ unsigned int byteOffset,  
   _In_ unsigned int elementLength,  
   _Out_ JsValueRef *result  
);  
```  
  
#### Parameter  
 `arrayType`  
 Der Typ des zu erstellenden Array.  
  
 `baseArray`  
 Das Basisarray des neuen Arrays. Verwenden Sie `JS_INVALID_REFERENCE` Wenn kein Basisarray.  
  
 `byteOffset`  
 Der Offset in Bytes ab dem Anfang `baseArray` ( `ArrayBuffer` ) für das Ergebnis typisierte Array, auf das verwiesen werden soll. Nur zutreffend `baseArray` , wenn es sich um ein `ArrayBuffer` Objekt handelt. Muss andernfalls 0 sein.  
  
 `elementLength`  
 Die Anzahl der Elemente im Array. Nur anwendbar beim Erstellen eines neuen typisierten Arrays ohne `baseArray` ( `baseArray` ist `JS_INVALID_REFERENCE` ) oder wenn `baseArray` es sich um ein Objekt handelt `ArrayBuffer` . Muss andernfalls 0 sein.  
  
 `result`  
 Das neue typisierte Array Objekt.  
  
## Rückgabewert  
 Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.  
  
## Hinweise  
 Das `baseArray` kann ein `ArrayBuffer` , ein weiteres typisiertes Array oder ein JavaScript sein `Array` . Das zurückgegebene typisierte Array verwendet die `baseArray` Wenn es ein ist `ArrayBuffer` , oder auf andere Weise erstellen und verwenden Sie eine Kopie des zugrunde liegenden Quellarrays.  
  
 Erfordert einen aktiven Skriptkontext.  
  
 Diese API wird nur im Microsoft Edge-Modus unterstützt.  
  
## Anforderungen  
 **Kopfzeile:** jsrt. h  
  
## Weitere Informationen  
 [Referenz (JavaScript-Laufzeit)](../chakra-hosting/reference-javascript-runtime.md)