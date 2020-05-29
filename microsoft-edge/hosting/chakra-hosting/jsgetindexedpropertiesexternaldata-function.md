---
description: Ruft die externen Daten Informationen eines Objekts für indizierte Eigenschaften ab.
title: JsGetIndexedPropertiesExternalData-Funktion | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 2c313163-3462-42fd-8dee-3dfb3ac7f43f
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 96fdcd4b6fe29ffc20a796983cc1de692c80a3f1
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10567253"
---
# JsGetIndexedPropertiesExternalData-Funktion
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