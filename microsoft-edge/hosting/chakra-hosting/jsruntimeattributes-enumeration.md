---
description: 'Attribute einer Laufzeit. '
title: JsRuntimeAttributes-Enumeration | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsRuntimeAttributes
helpviewer_keywords:
- JsRuntimeAttributes enumeration
ms.assetid: f76d82e9-a695-4d6a-96c1-b3a4d27fed68
caps.latest.revision: 14
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 9b8f6788f1de4988e3936701cfc742a564c92cfd
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10568325"
---
# JsRuntimeAttributes-Enumeration
Attribute einer Laufzeit.  
  
## Syntax  
  
```cpp  
enum JsRuntimeAttributes;  
```  
  
## Member  
  
### Werte  
  
|Name|Beschreibung|  
|----------|-----------------|  
|`JsRuntimeAttributeAllowScriptInterrupt`|Die Laufzeit sollte eine zuverlässige Skript Unterbrechung unterstützen. Dies erhöht die Anzahl der stellen, an denen die Laufzeit auf eine Skript Unterbrechungsanforderung überprüft, und zwar zu Lasten einer geringen Laufzeit.|  
|`JsRuntimeAttributeDisableBackgroundWork`|Die Laufzeit führt keine Arbeit (wie Garbage Collection) für Hintergrund-Threads aus.|  
|`JsRuntimeAttributeDisableEval`|Mit `eval` oder `function` -Konstruktor wird eine Ausnahme ausgelöst.|  
|`JsRuntimeAttributeDisableNativeCodeGeneration`|Die Laufzeit generiert keinen systemeigenen Code.|  
|`JsRuntimeAttributeEnableExperimentalFeatures`|Die Laufzeit ermöglicht alle experimentellen Funktionen.|  
|`JsRuntimeAttributeEnableIdleProcessing`|Host ruft an `JsIdle` , also aktivieren Sie die Leerlaufverarbeitung. Andernfalls verwaltet die Laufzeit den Arbeitsspeicher etwas aggressiver.|  
|`JsRuntimeAttributeDispatchSetExceptionsToDebugger`|Durch das Aufrufen `JsSetException` wird auch die Ausnahme an den Skriptdebugger gesendet (sofern vorhanden), der dem Debugger die Möglichkeit gibt, die Ausnahme zu unterbrechen.|  
|`JsRuntimeAttributeNone`|Keine besonderen Attribute.|  
  
## Anforderungen  
 **Kopfzeile:** jsrt. h  
  
## Weitere Informationen  
 [Referenz (JavaScript-Laufzeit)](../chakra-hosting/reference-javascript-runtime.md)