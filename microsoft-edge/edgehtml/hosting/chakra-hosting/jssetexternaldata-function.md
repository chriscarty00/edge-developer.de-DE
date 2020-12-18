---
description: Legt die externen Daten für ein externes Objekt fest.
title: JsSetExternalData-Funktion | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsSetExternalData
helpviewer_keywords:
- JsSetExternalData function
ms.assetid: 94e0ad34-67d7-4f7f-88a3-3b057ef5e4b9
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: f2ebdce4448a14f145ce5aafe6ba412f7db26c17
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11234066"
---
# JsSetExternalData Funktion

Legt die externen Daten für ein externes Objekt fest.  
  
## Syntax  
  
```cpp  
STDAPI_(JsErrorCode) JsSetExternalData(  
   _In_ JsValueRef object,  
   _In_opt_ void *externalData  
);  
```  
  
#### Parameter  
 `object`  
 Das externe Objekt.  
  
 `externalData`  
 Die im Objekt gespeicherten externen Daten. Kann NULL sein, wenn keine externen Daten im Objekt gespeichert sind.  
  
## Rückgabewert  
 Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.  
  
## Hinweise  
 Erfordert einen aktiven Skriptkontext.  
  
## Anforderungen  
 **Kopfzeile:** jsrt. h  
  
## Weitere Informationen  
 [Referenz (JavaScript-Laufzeit)](../chakra-hosting/reference-javascript-runtime.md)
