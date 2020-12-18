---
description: Bestimmt, ob ein Objekt seine indizierten Eigenschaften in externen Daten aufweist.
title: JsHasIndexedPropertiesExternalData-Funktion | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: c676db20-3ef1-4f84-8b26-3e06fe0ab2bf
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: e6395bacb15904bc3f2e74d22959844e8e0af373
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11234250"
---
# JsHasIndexedPropertiesExternalData Funktion

Bestimmt, ob ein Objekt seine indizierten Eigenschaften in externen Daten aufweist.  
  
## Syntax  
  
```cpp  
STDAPI_(JsErrorCode) JsHasIndexedPropertiesExternalData(  
   _In_ JsValueRef object,  
   _Out_ bool* value  
);  
```  
  
#### Parameter  
 `object`  
 Das Objekt.  
  
 `value`  
 Gibt an, ob das Objekt seine indizierten Eigenschaften in externen Daten hat.  
  
## Rückgabewert  
 Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.  
  
## Hinweise  
 Diese API wird nur im Microsoft Edge-Modus unterstützt.  
  
## Anforderungen  
 **Kopfzeile:** jsrt. h  
  
## Weitere Informationen  
 [Referenz (JavaScript-Laufzeit)](../chakra-hosting/reference-javascript-runtime.md)
