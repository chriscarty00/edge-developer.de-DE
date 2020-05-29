---
description: Beendet die Profilerstellung im aktuellen Kontext.
title: JsStopProfiling-Funktion | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsStopProfiling
helpviewer_keywords:
- JsStopProfiling function
ms.assetid: 3639c04f-a0f9-418b-be39-92f64b4e7ef8
caps.latest.revision: 13
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 9d021c7c9849d20283a39d6ecffc89c5b2ea0db0
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10568202"
---
# JsStopProfiling-Funktion
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