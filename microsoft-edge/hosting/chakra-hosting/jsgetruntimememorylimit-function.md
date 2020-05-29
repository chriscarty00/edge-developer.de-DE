---
description: Ruft den aktuellen Speichergrenzwert für eine Laufzeit ab.
title: JsGetRuntimeMemoryLimit-Funktion | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsGetRuntimeMemoryLimit
helpviewer_keywords:
- JsGetRuntimeMemoryLimit function
ms.assetid: ed81ca60-99fd-46b0-89ae-f6ac07926904
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: e6b44bb1dc8ad5fb8c07248a225c10682f96c86a
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10567243"
---
# JsGetRuntimeMemoryLimit-Funktion
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