---
description: Erstellt einen Skriptkontext zum Ausführen von Skripts.
title: JsCreateContext-Funktion | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsCreateContext
helpviewer_keywords:
- JsCreateContext function
ms.assetid: aceca043-2c73-4029-a06c-8ad6695109cf
caps.latest.revision: 15
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 5d6c8149b8a5e5fee7cbc8dac821713b1d9649ee
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233752"
---
# JsCreateContext Funktion

Erstellt einen Skriptkontext zum Ausführen von Skripts.  
  
## Syntax  
  
```cpp  
// Microsoft Edge mode signature  
STDAPI_(JsErrorCode) JsCreateContext(  
   _In_ JsRuntimeHandle runtime,  
   _Out_ JsContextRef *newContext);  
  
// Legacy mode signature  
STDAPI_(JsErrorCode) JsCreateContext(  
   _In_ JsRuntimeHandle runtime,  
   _In_ IDebugApplication *debugApplication,  
   _Out_ JsContextRef *newContext  
);  
```  
  
#### Parameter  
 `runtime`  
 Die Laufzeit, in der der Skriptkontext erstellt wird.  
  
 `debugApplication`  
 Die für das Debuggen zu verwendende Debug-Anwendung. Dieser Parameter kann NULL sein, in diesem Fall ist das Debuggen für den Kontext nicht aktiviert.  
  
 `newContext`  
 Der erstellte Skriptkontext.  
  
## Rückgabewert  
 Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.  
  
## Hinweise  
 Jeder Skriptkontext verfügt über ein eigenes globales Objekt, das von allen anderen Skript Kontexten isoliert ist.  
  
 Der `debugApplication` Parameter wird im Microsoft Edge-Modus nicht unterstützt. Weitere Informationen zur Verwendung dieser API im Microsoft Edge-Modus finden Sie unter [Targeting Microsoft Edge vs. Legacy Engines](../chakra-hosting/targeting-edge-vs-legacy-engines-in-jsrt-apis.md).  
  
## Anforderungen  
 **Kopfzeile:** jsrt. h  
  
## Weitere Informationen  
 [Referenz (JavaScript-Laufzeit)](../chakra-hosting/reference-javascript-runtime.md)
