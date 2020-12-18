---
description: Gibt einen Wert zurück, der angibt, ob die Skriptausführung in der Laufzeit deaktiviert ist.
title: JsIsRuntimeExecutionDisabled-Funktion | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsIsRuntimeExecutionDisabled
helpviewer_keywords:
- JsIsRuntimeExecutionDisabled function
ms.assetid: 77490280-fb84-4614-a1f0-6ac31e3bd607
caps.latest.revision: 5
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 0ce59c77525abdb2dd6cac71dde1378264395e79
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233574"
---
# JsIsRuntimeExecutionDisabled Funktion

Gibt einen Wert zurück, der angibt, ob die Skriptausführung in der Laufzeit deaktiviert ist.  
  
## Syntax  
  
```cpp  
STDAPI_(JsErrorCode) JsIsRuntimeExecutionDisabled(    _In_ JsRuntimeHandle runtime,    _Out_ bool *isDisabled);  
```  
  
#### Parameter  
 `runtime`  
 Gibt die Laufzeit an, um zu überprüfen, ob die Ausführung deaktiviert ist.  
  
 `isDisabled`  
 `true` Wenn die Ausführung deaktiviert ist, `false` andernfalls.  
  
## Rückgabewert  
 `JsNoError` Wenn der Vorgang erfolgreich war, wird andernfalls ein Fehlercode ausgeführt.  
  
## Anforderungen  
 **Kopfzeile:** jsrt. h  
  
## Weitere Informationen  
 [Referenz (JavaScript-Laufzeit)](../chakra-hosting/reference-javascript-runtime.md)
