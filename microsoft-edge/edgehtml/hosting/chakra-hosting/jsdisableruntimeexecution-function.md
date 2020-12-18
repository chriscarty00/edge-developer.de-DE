---
description: Unterbricht die Skriptausführung und beendet alle ausgeführten Skripts in einer Laufzeit.
title: JsDisableRuntimeExecution-Funktion | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsDisableRuntimeExecution
helpviewer_keywords:
- JsDisableRuntimeExecution function
ms.assetid: 4bd4670a-a9da-4f8c-b3fd-1fd366d915c3
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 6a08e6a7f89c724f8cf1a73afd97d2cb23c0334e
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233953"
---
# JsDisableRuntimeExecution Funktion

Unterbricht die Skriptausführung und beendet alle ausgeführten Skripts in einer Laufzeit.  
  
## Syntax  
  
```cpp  
STDAPI_(JsErrorCode) JsDisableRuntimeExecution(  
   _In_ JsRuntimeHandle runtime  
);  
```  
  
#### Parameter  
 `runtime`  
 Die Laufzeit, die angehalten werden soll.  
  
## Rückgabewert  
 Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.  
  
## Hinweise  
 Bei Aufrufen einer angehalten-Laufzeit tritt ein Fehler auf, bis `JsEnableRuntimeExecution` aufgerufen wird.  
  
 Diese API muss nicht für den Thread aufgerufen werden, in dem die Laufzeit aktiv ist. Obwohl die Laufzeit in einen angehalten-Zustand gesetzt wird, wird ein ausgeführtes Skript möglicherweise nicht sofort angehalten. ein laufendes Skript wird so schnell wie möglich mit einer nicht abfangbaren Ausnahme beendet.  
  
 Das Anhalten der Ausführung in einer Laufzeit, die bereits angehalten ist, ist ein No-op-Modus.  
  
## Anforderungen  
 **Kopfzeile:** jsrt. h  
  
## Weitere Informationen  
 [Referenz (JavaScript-Laufzeit)](../chakra-hosting/reference-javascript-runtime.md)
