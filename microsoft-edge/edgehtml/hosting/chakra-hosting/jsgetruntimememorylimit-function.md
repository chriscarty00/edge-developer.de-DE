---
description: Ruft den aktuellen Speichergrenzwert für eine Laufzeit ab.
title: JsGetRuntimeMemoryLimit-Funktion | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsGetRuntimeMemoryLimit
helpviewer_keywords:
- JsGetRuntimeMemoryLimit function
ms.assetid: ed81ca60-99fd-46b0-89ae-f6ac07926904
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: ed04a0fb921d22eea17eaf86ef7a0152fbf2a1d0
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11234262"
---
# JsGetRuntimeMemoryLimit Funktion

Ruft den aktuellen Speichergrenzwert für eine Laufzeit ab.  
  
## Syntax  
  
```cpp  
STDAPI_(JsErrorCode) JsGetRuntimeMemoryLimit(  
   _In_ JsRuntimeHandle runtime,  
   _Out_ size_t *memoryLimit  
);  
```  
  
#### Parameter  
 `runtime`  
 Die Laufzeit, deren Speichergrenzwert abgerufen werden soll.  
  
 `memoryLimit`  
 Die aktuelle Speichergrenze der Laufzeit in Bytes oder-1, wenn kein Grenzwert festgesetzt wurde.  
  
## Rückgabewert  
 Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.  
  
## Hinweise  
 Die Speichergrenze einer Runtime kann immer abgerufen werden, unabhängig davon, ob die Laufzeit in einem anderen Thread aktiv ist oder nicht.  
  
## Anforderungen  
 **Kopfzeile:** jsrt. h  
  
## Weitere Informationen  
 [Referenz (JavaScript-Laufzeit)](../chakra-hosting/reference-javascript-runtime.md)
