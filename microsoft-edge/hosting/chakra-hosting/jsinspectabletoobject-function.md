---
description: Erstellt einen JavaScript-Wert, bei dem es sich um eine Projektion des übergebenen `IInspectable` Zeigers handelt.
title: JsInspectableToObject-Funktion | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: dd0ad567-2ba8-4a63-bee4-2c6ff5ce9fa9
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 26ce17eb3abcefcf9a1f0cc773e9fe4c3aaf05cd
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10567233"
---
# JsInspectableToObject-Funktion
Erstellt einen JavaScript-Wert, bei dem es sich um eine Projektion des übergebenen `IInspectable` Zeigers handelt.  
  
## Syntax  
  
```cpp  
STDAPI_(JsErrorCode) JsInspectableToObject(  
        _In_ IInspectable  *inspectable,  
        _Out_ JsValueRef *value  
);  
```  
  
#### Parameter  
 `inspectable`  
 A `IInspectable` , das projiziert werden soll.  
  
 `value`  
 Ein JavaScript-Wert, bei dem es sich um eine Projektion von `IInspectable` .  
  
## Rückgabewert  
 Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.  
  
## Hinweise  
 Der projizierte Wert kann vom Skript verwendet werden, um ein WinRT-Objekt aufzurufen. Hosts sind für das Erzwingen von COM-Threading Regeln verantwortlich.  
  
 Erfordert einen aktiven Skriptkontext.  
  
 Diese API wird nur im EdgeHTML-Modus unterstützt.  
  
## Anforderungen  
 **Kopfzeile:** jsrt. h  
  
## Weitere Informationen  
 [Referenz (JavaScript-Laufzeit)](../chakra-hosting/reference-javascript-runtime.md)