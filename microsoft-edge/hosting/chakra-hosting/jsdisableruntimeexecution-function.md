---
description: Unterbricht die Skriptausführung und beendet alle ausgeführten Skripts in einer Laufzeit.
title: JsDisableRuntimeExecution-Funktion | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsDisableRuntimeExecution
helpviewer_keywords:
- JsDisableRuntimeExecution function
ms.assetid: 4bd4670a-a9da-4f8c-b3fd-1fd366d915c3
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 575947d3038eaa136e9d6ae62507501bc768eabe
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10567272"
---
# JsDisableRuntimeExecution-Funktion
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