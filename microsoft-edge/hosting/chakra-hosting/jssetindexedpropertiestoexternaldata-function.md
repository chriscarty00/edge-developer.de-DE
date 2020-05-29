---
description: Legt die indizierten Eigenschaften eines Objekts auf externe Daten fest. Die externen Daten werden als Back Store für die indizierten Eigenschaften des Objekts verwendet und auf wie ein typisiertes Array zugegriffen.
title: JsSetIndexedPropertiesToExternalData-Funktion | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: cee2d86d-ed42-4acb-86ef-95a67e63d0d6
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: c1aed6e194b1dc1c35f403626a7b6c02a7752ffb
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10568309"
---
# JsSetIndexedPropertiesToExternalData-Funktion
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