---
description: Erstellt einen JavaScript-Wert, bei dem es sich um eine Projektion des übergebenen Werts handelt `VARIANT` .
title: JsVariantToValue-Funktion | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsVariantToValue
helpviewer_keywords:
- JsVariantToValue function
ms.assetid: e8f9eb8b-55b3-4b65-927e-cad5b482edee
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 01796bc38548cf56b500731d899541ef214ec4e3
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10567191"
---
# JsVariantToValue-Funktion
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