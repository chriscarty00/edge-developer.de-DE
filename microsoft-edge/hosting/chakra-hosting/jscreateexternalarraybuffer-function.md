---
description: Erstellt ein JavaScript `ArrayBuffer` -Objekt für den Zugriff auf externen Speicher.
title: JsCreateExternalArrayBuffer-Funktion | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: 4a02aaec-0f67-4bf9-b37c-71cdb1410ca4
caps.latest.revision: 3
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 376eedda18393436d9dce340753586bf32599b21
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10567300"
---
# JsCreateExternalArrayBuffer-Funktion
Erstellt ein JavaScript `ArrayBuffer` -Objekt für den Zugriff auf externen Speicher.
  
## Syntax  
  
```cpp  
STDAPI_(JsErrorCode) JsCreateExternalArrayBuffer(  
  _Pre_maybenull_ _Pre_writable_byte_size_(byteLength) void *data,  
  _In_ unsigned int byteLength,  
  _In_opt_ JsFinalizeCallback finalizeCallback,  
  _In_opt_ void *callbackState,  
  _Out_ JsValueRef *result  
);  
  
```  
  
#### Parameter  
 `data`  
 Ein Zeiger auf den externen Speicher.  
  
 `byteLength`  
 Die Anzahl der Bytes im externen Speicher.  
  
 `finalizeCallback`  
 Ein Rückruf für den Zeitpunkt, zu dem das Objekt finalisiert wurde. Kann NULL sein.  
  
 `callbackState`  
 Der Benutzer hat den Zustand bereitgestellt, der an finalizeCallback zurückgegeben wird.  
  
 `result`  
 Das neue `ArrayBuffer` Objekt.  
  
## Rückgabewert  
 Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.  
  
## Hinweise  
 Erfordert einen aktiven Skriptkontext.  
  
## Anforderungen  
 **Kopfzeile:** jsrt. h  
  
## Weitere Informationen  
 [Referenz (JavaScript-Laufzeit)](../chakra-hosting/reference-javascript-runtime.md)