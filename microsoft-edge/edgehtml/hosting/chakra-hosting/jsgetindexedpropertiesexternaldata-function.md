---
description: Ruft die externen Daten Informationen eines Objekts für indizierte Eigenschaften ab.
title: JsGetIndexedPropertiesExternalData-Funktion | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 2c313163-3462-42fd-8dee-3dfb3ac7f43f
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 627aaef48def2e042927467e1cbb6d6b7c06a525
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233582"
---
# JsGetIndexedPropertiesExternalData Funktion

Ruft die externen Daten Informationen eines Objekts für indizierte Eigenschaften ab.  
  
## Syntax  
  
```cpp  
STDAPI_(JsErrorCode) JsGetIndexedPropertiesExternalData(  
   _In_ JsValueRef object,  
   _Out_ void** data,  
   _Out_ JsTypedArrayType* arrayType,  
   _Out_ unsigned int* elementLength  
);  
```  
  
#### Parameter  
 `object`  
 Das Objekt.  
  
 `data`  
 Der externe Datenspeicher für die indizierten Eigenschaften des Objekts.  
  
 `arrayType`  
 Der Arrayelementtyp in externen Daten.  
  
 `elementLength`  
 Die Anzahl der Arrayelemente in externen Daten.  
  
## Rückgabewert  
 Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.  
  
## Hinweise  
 Diese API wird nur im Microsoft Edge-Modus unterstützt.  
  
## Anforderungen  
 **Kopfzeile:** jsrt. h  
  
## Weitere Informationen  
 [Referenz (JavaScript-Laufzeit)](../chakra-hosting/reference-javascript-runtime.md)
