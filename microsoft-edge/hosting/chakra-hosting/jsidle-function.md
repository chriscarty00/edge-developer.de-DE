---
description: Weist die Common Language Runtime an, die erforderliche Leerlaufverarbeitung auszuführen.
title: JsIdle-Funktion | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsIdle
helpviewer_keywords:
- JsIdle function
ms.assetid: 372d1c62-8e19-4886-aa33-364cabc09bba
caps.latest.revision: 13
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 4da7148bf7daa3db983ab8f5bba622bfe0b19466
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10568358"
---
# JsIdle-Funktion
Weist die Common Language Runtime an, die erforderliche Leerlaufverarbeitung auszuführen.  
  
## Syntax  
  
```cpp  
STDAPI_(JsErrorCode) JsIdle(  
   _Out_opt_ unsigned int *nextIdleTick  
);  
```  
  
#### Parameter  
 `nextIdleTick`  
 Das nächste System wird angekreuzt, wenn mehr Leerlaufaufgaben ausgeführt werden müssen. Kann NULL sein. Gibt die maximale Anzahl von Ticks zurück, wenn keine bevorstehende Leerlauf Arbeit ausgeführt werden soll.  
  
## Rückgabewert  
 Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.  
  
## Hinweise  
 Wenn die Idle-Verarbeitung für die aktuelle Laufzeit aktiviert wurde, `JsIdle` informiert der Aufruf die aktuelle Laufzeit darüber, dass der Host inaktiv ist und dass die Laufzeit Speicher Bereinigungsaufgaben ausführen kann.  
  
 `JsIdle` kann auch die Anzahl der System Ticks zurückgeben, bis die Laufzeit mehr arbeitslos ist. `JsIdle`Das anrufen, bevor diese Anzahl von Ticks abgelaufen ist, funktioniert nicht.  
  
 Erfordert einen aktiven Skriptkontext.  
  
## Anforderungen  
 **Kopfzeile:** jsrt. h  
  
## Weitere Informationen  
 [Referenz (JavaScript-Laufzeit)](../chakra-hosting/reference-javascript-runtime.md)