---
description: Erstellt einen JavaScript-Wert, bei dem es sich um eine Projektion des übergebenen `IInspectable` Zeigers handelt.
title: JsInspectableToObject-Funktion | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: dd0ad567-2ba8-4a63-bee4-2c6ff5ce9fa9
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: a5d3d91b38c9db5de2eb8fb02526f6072f0f5147
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11234134"
---
# JsInspectableToObject Funktion

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
