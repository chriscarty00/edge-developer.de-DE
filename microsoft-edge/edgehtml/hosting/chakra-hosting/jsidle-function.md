---
description: Weist die Common Language Runtime an, die erforderliche Leerlaufverarbeitung auszuführen.
title: JsIdle-Funktion | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsIdle
helpviewer_keywords:
- JsIdle function
ms.assetid: 372d1c62-8e19-4886-aa33-364cabc09bba
caps.latest.revision: 13
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: ecba0aafb6b4dcccb4485c2956cae5ce4045355f
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11234263"
---
# JsIdle Funktion

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
