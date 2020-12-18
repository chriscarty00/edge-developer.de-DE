---
description: Legt die indizierten Eigenschaften eines Objekts auf externe Daten fest. Die externen Daten werden als Back Store für die indizierten Eigenschaften des Objekts verwendet und auf wie ein typisiertes Array zugegriffen.
title: JsSetIndexedPropertiesToExternalData-Funktion | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: cee2d86d-ed42-4acb-86ef-95a67e63d0d6
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: fa0eba3659c20066913cd42a0a18dd5ffe5f857f
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233736"
---
# JsSetIndexedPropertiesToExternalData Funktion

Legt die indizierten Eigenschaften eines Objekts auf externe Daten fest. Die externen Daten werden als Back Store für die indizierten Eigenschaften des Objekts verwendet und auf wie ein typisiertes Array zugegriffen.  
  
## Syntax  
  
```cpp  
STDAPI_(JsErrorCode) JsSetIndexedPropertiesToExternalData(  
   _In_ JsValueRef object,  
   _In_ void* data,  
   _In_ JsTypedArrayType arrayType,  
   _In_ unsigned int elementLength  
);  
```  
  
#### Parameter  
 `object`  
 Das Objekt, das ausgeführt werden soll.  
  
 `data`  
 Die externen Daten, die als Back Store für die indizierten Eigenschaften des Objekts verwendet werden sollen.  
  
 `arrayType`  
 Der Arrayelementtyp in externen Daten.  
  
 `elementLength`  
 Die Anzahl der Arrayelemente in externen Daten.  
  
## Rückgabewert  
 Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.  
  
## Hinweise  
 Erfordert einen aktiven Skriptkontext.  
  
 Diese API wird nur im EdgeHTML-Modus unterstützt.  
  
## Anforderungen  
 **Kopfzeile:** jsrt. h  
  
## Weitere Informationen  
 [Referenz (JavaScript-Laufzeit)](../chakra-hosting/reference-javascript-runtime.md)
