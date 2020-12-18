---
description: 'Attribute einer Laufzeit. '
title: JsRuntimeAttributes-Enumeration | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsRuntimeAttributes
helpviewer_keywords:
- JsRuntimeAttributes enumeration
ms.assetid: f76d82e9-a695-4d6a-96c1-b3a4d27fed68
caps.latest.revision: 14
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: bbc5341c3214d9796278d334507e284989ff45dd
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233874"
---
# JsRuntimeAttributes Enumeration

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
