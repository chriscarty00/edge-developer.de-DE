---
description: Startet die Profilerstellung im aktuellen Kontext.
title: JsStartProfiling-Funktion | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsStartProfiling
helpviewer_keywords:
- JsStartProfiling function
ms.assetid: 638da395-42dd-4fc5-b581-819e647e887d
caps.latest.revision: 13
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 891c39305e08d214a8f06b680c7022683a9d6fe4
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10568203"
---
# JsStartProfiling-Funktion
Startet die Profilerstellung im aktuellen Kontext.  
  
## Syntax  
  
```cpp  
STDAPI_(JsErrorCode) JsStartProfiling(  
   _In_ IActiveScriptProfilerCallback *callback,  
   _In_ PROFILER_EVENT_MASK eventMask,  
   _In_ unsigned long context  
);  
```  
  
#### Parameter  
 `callback`  
 Der zu verwendende Profil Erstellungs Rückruf.  
  
 `eventMask`  
 Die Profil Erstellungsereignisse, mit denen Sie eine Rückruffunktion durch.  
  
 `context`  
 Ein Kontext, der an den Profil Erstellungs Rückruf übergeben werden soll.  
  
## Rückgabewert  
 Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.  
  
## Hinweise  
 Erfordert einen aktiven Skriptkontext.  
  
 Diese API wird in Desktop-Apps unterstützt, wird aber in Store-Apps nicht unterstützt.  
  
## Anforderungen  
 **Kopfzeile:** jsrt. h  
  
## Weitere Informationen  
 [Referenz (JavaScript-Laufzeit)](../chakra-hosting/reference-javascript-runtime.md)