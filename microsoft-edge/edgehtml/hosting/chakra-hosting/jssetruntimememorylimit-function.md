---
description: Legt den aktuellen Speichergrenzwert für eine Laufzeit fest.
title: JsSetRuntimeMemoryLimit-Funktion | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsSetRuntimeMemoryLimit
helpviewer_keywords:
- JsSetRuntimeMemoryLimit function
ms.assetid: 74feb31f-19f6-43e3-b117-0694c59ac593
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 1c31d8bbbec4be22fc1af09e546ad4c95f8ec2bd
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233560"
---
# JsSetRuntimeMemoryLimit Funktion

Legt den aktuellen Speichergrenzwert für eine Laufzeit fest.  
  
## Syntax  
  
```cpp  
STDAPI_(JsErrorCode) JsSetRuntimeMemoryLimit(  
   _In_ JsRuntimeHandle runtime,  
   _In_ size_t memoryLimit  
);  
```  
  
#### Parameter  
 `runtime`  
 Die Laufzeit, deren Speichergrenzwert festzulegen ist.  
  
 `memoryLimit`  
 Die neue Obergrenze für den Arbeitsspeicher, in Bytes oder-1 für keinen Speichergrenzwert.  
  
## Rückgabewert  
 Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.  
  
## Hinweise  
 Eine Speichergrenze führt dazu, dass jeder Vorgang, der den Grenzwert überschreitet, mit einem Fehler "nicht genügend Arbeitsspeicher" fehlschlägt. Das Festlegen der Speichergrenze einer Runtime auf-1 bedeutet, dass die Laufzeit keine Speichergrenze aufweist. Für neue Runtimes wird standardmäßig kein Speichergrenzwert festgesetzt. Wenn die neue Arbeitsspeichergrenze die aktuelle Nutzung überschreitet, wird der Aufruf erfolgreich ausgeführt, und alle zukünftigen Zuweisungen in dieser Runtime schlagen fehl, bis die Speicherauslastung der Common Language Runtime unter den Grenzwert fällt.  
  
 Die Speichergrenze einer Common Language Runtime kann immer festgesetzt werden, unabhängig davon, ob die Laufzeit in einem anderen Thread aktiv ist oder nicht.  
  
## Anforderungen  
 **Kopfzeile:** jsrt. h  
  
## Weitere Informationen  
 [Referenz (JavaScript-Laufzeit)](../chakra-hosting/reference-javascript-runtime.md)
