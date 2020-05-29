---
description: Serialisiert ein analysiertes Skript in einen Puffer, als wieder verwendet werden kann.
title: JsSerializeScript-Funktion | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsSerializeScript
helpviewer_keywords:
- JsSerializeScript function
ms.assetid: ca42c194-e1c1-407d-b542-b9d494e3ac4e
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 1b45067fddb7ea4dff02e527e460db1270011c61
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10568319"
---
# JsSerializeScript-Funktion
Serialisiert ein analysiertes Skript in einen Puffer, als wieder verwendet werden kann.  
  
## Syntax  
  
```cpp  
STDAPI_(JsErrorCode) JsSerializeScript(  
   _In_z_ const wchar_t *script,  
   _Out_writes_to_opt_(*bufferSize,  
   *bufferSize) BYTE *buffer,  
   _Inout_ unsigned long *bufferSize  
);  
```  
  
#### Parameter  
 `script`  
 Das zu serialisierende Skript.  
  
 `buffer`  
 Der Puffer, in den das serialisierte Skript eingefügt werden soll. Kann NULL sein.  
  
 `bufferSize`  
 Beim Eintrag die Größe des Puffers in Bytes; beim Beenden muss die Größe des Puffers in Byte für das serialisierte Skript angegeben werden.  
  
## Rückgabewert  
 Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.  
  
## Hinweise  
 `JsSerializeScript` analysiert ein Skript und speichert dann die analysierte Form des Skripts in einem Laufzeit-unabhängigen Format. Das serialisierte Skript kann dann in einer beliebigen Laufzeit deserialisiert werden, ohne dass das Skript erneut analysiert werden muss.  
  
 Erfordert einen aktiven Skriptkontext.  
  
## Anforderungen  
 **Kopfzeile:** jsrt. h  
  
## Weitere Informationen  
 [Referenz (JavaScript-Laufzeit)](../chakra-hosting/reference-javascript-runtime.md)