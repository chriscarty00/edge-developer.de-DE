---
description: Erstellt ein JavaScript `DataView` -Objekt.
title: JsCreateDataView-Funktion | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 161e59eb-d429-46f7-9a38-bbf2149ccf44
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 1bf237458e8561b7070e4f3f0d4a14050f028375
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10567306"
---
# JsCreateDataView-Funktion
Erstellt ein JavaScript `DataView` -Objekt.  
  
## Syntax  
  
```cpp  
JsErrorCode  JsCreateDataView(  
   _In_ JsValueRef arrayBuffer,  
   _In_ unsigned int byteOffset,  
   _In_ unsigned int byteLength,  
   _Out_ JsValueRef *result  
);  
```  
  
#### Parameter  
 `arrayBuffer`  
 Ein vorhandenes `ArrayBuffer` Objekt, das als Speicher für das Result-Objekt verwendet werden soll `DataView` .  
  
 `byteOffset`  
 Der Offset in Bytes vom Anfang des zu vergleichenden `arrayBuffer` Ergebnisses `DataView` .  
  
 `byteLength`  
 Die Anzahl der Bytes in der ArrayBuffer für das Ergebnis DataView, auf die verwiesen werden soll.  
  
 `result`  
 Das neue DataView-Objekt.  
  
## Rückgabewert  
 Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.  
  
## Hinweise  
 Erfordert einen aktiven Skriptkontext.  
  
 Diese API wird nur im Microsoft Edge-Modus unterstützt.  
  
## Anforderungen  
 **Kopfzeile:** jsrt. h  
  
## Weitere Informationen  
 [Referenz (JavaScript-Laufzeit)](../chakra-hosting/reference-javascript-runtime.md)