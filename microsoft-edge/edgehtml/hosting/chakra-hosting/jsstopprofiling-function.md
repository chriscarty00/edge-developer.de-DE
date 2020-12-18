---
description: Beendet die Profilerstellung im aktuellen Kontext.
title: JsStopProfiling-Funktion | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsStopProfiling
helpviewer_keywords:
- JsStopProfiling function
ms.assetid: 3639c04f-a0f9-418b-be39-92f64b4e7ef8
caps.latest.revision: 13
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 02c42afda7e61d71b90a9a1a71aa71cc53584ff8
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233943"
---
# JsStopProfiling Funktion

Beendet die Profilerstellung im aktuellen Kontext.  
  
## Syntax  
  
```cpp  
STDAPI_(JsErrorCode) JsStopProfiling(  
   _In_ HRESULT reason  
);  
```  
  
#### Parameter  
 `reason`  
 Der Grund dafür, dass die Profilerstellung angehalten wird, um an den Profiler Rückruf zu übergeben.  
  
## Rückgabewert  
 Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.  
  
## Hinweise  
 Gibt keinen Fehler zurück, wenn die Profilerstellung nicht gestartet wurde.  
  
 Erfordert einen aktiven Skriptkontext.  
  
 Diese API wird in Desktop-Apps unterstützt, wird aber in Store-Apps nicht unterstützt.  
  
## Anforderungen  
 **Kopfzeile:** jsrt. h  
  
## Weitere Informationen  
 [Referenz (JavaScript-Laufzeit)](../chakra-hosting/reference-javascript-runtime.md)
