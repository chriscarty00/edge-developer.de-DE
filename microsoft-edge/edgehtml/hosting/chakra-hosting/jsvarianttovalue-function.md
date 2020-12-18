---
description: Erstellt einen JavaScript-Wert, bei dem es sich um eine Projektion des übergebenen Werts handelt `VARIANT` .
title: JsVariantToValue-Funktion | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsVariantToValue
helpviewer_keywords:
- JsVariantToValue function
ms.assetid: e8f9eb8b-55b3-4b65-927e-cad5b482edee
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 58c928b519b5a9a678b6cd6ad367e1db2332f021
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233899"
---
# JsVariantToValue Funktion

Erstellt einen JavaScript-Wert, bei dem es sich um eine Projektion des übergebenen Werts handelt `VARIANT` .  
  
## Syntax  
  
```cpp  
STDAPI_(JsErrorCode) JsVariantToValue(  
   _In_ VARIANT *variant,  
   _Out_ JsValueRef *value  
);  
```  
  
#### Parameter  
 `variant`  
 A `VARIANT` , das projiziert werden soll.  
  
 `value`  
 Ein JavaScript-Wert, bei dem es sich um eine Projektion von `VARIANT` .  
  
## Rückgabewert  
 Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.  
  
## Hinweise  
 Der projizierte Wert kann vom Skript verwendet werden, um ein COM-Automatisierungsobjekt aus einem Skript aufzurufen. Hosts sind für das Erzwingen von COM-Threading Regeln verantwortlich.  
  
 Erfordert einen aktiven Skriptkontext.  
  
## Anforderungen  
 **Kopfzeile:** jsrt. h  
  
## Weitere Informationen  
 [Referenz (JavaScript-Laufzeit)](../chakra-hosting/reference-javascript-runtime.md)
