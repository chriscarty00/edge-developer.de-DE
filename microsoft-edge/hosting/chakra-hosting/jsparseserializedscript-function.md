---
description: Analysiert ein serialisiertes Skript und gibt eine Funktion zurück, die das Skript darstellt.
title: JsParseSerializedScript-Funktion | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsParseSerializedScript
helpviewer_keywords:
- JsParseSerializedScript function
ms.assetid: 40d0c7c4-fd5b-46ed-9e65-38c2db2fc859
caps.latest.revision: 13
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: a778a007e69f15063d23cc55f999144ab55a306c
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10568350"
---
# JsParseSerializedScript-Funktion
Analysiert ein serialisiertes Skript und gibt eine Funktion zurück, die das Skript darstellt.  
  
## Syntax  
  
```cpp  
STDAPI_(JsErrorCode) JsParseSerializedScript(  
   _In_z_ const wchar_t *script,  
   _In_ BYTE *buffer,  
   _In_ JsSourceContext sourceContext,  
   _In_z_ const wchar_t *sourceUrl,  
   _Out_ JsValueRef *result  
);  
```  
  
#### Parameter  
 `script`  
 Das zu analysierende Skript.  
  
 `buffer`  
 Das serialisierte Skript.  
  
 `sourceContext`  
 Ein Cookie, das das Skript identifiziert, das von debugfähigen-Skript Kontexten verwendet werden kann.  
  
 `sourceUrl`  
 Der Speicherort, aus dem das Skript kam.  
  
 `result`  
 Eine Funktion, die den Skriptcode darstellt.  
  
## Rückgabewert  
 Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.  
  
## Hinweise  
 Erfordert einen aktiven Skriptkontext.  
  
 Der Puffer wird vom Skriptmodul nicht im Arbeitsspeicher gespeichert, daher muss der Code so lange am Leben bleiben, wie er zum Ausführen von Skripts verwendet werden kann.  
  
## Anforderungen  
 **Kopfzeile:** jsrt. h  
  
## Weitere Informationen  
 [Referenz (JavaScript-Laufzeit)](../chakra-hosting/reference-javascript-runtime.md)