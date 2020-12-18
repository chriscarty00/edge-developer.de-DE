---
description: Erstellt ein JavaScript `DataView` -Objekt.
title: JsCreateDataView-Funktion | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 161e59eb-d429-46f7-9a38-bbf2149ccf44
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 1d6d170d53f3bfaf885713b6f3abca0b066f8c1d
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233748"
---
# JsCreateDataView Funktion

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
