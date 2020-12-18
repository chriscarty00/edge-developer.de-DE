---
description: Gibt die Ausnahme zurück, die dazu geführt hat, dass sich die Laufzeit des aktuellen Kontexts im Ausnahmezustand befindet, und setzt den Ausnahmezustand für diese Runtime zurück.
title: JsGetAndClearException-Funktion | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsGetAndClearException
helpviewer_keywords:
- JsGetAndClearException function
ms.assetid: 6aec8a88-41ee-47f6-b5f4-32f3cae6bb7b
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: cb296ea351d0466a856d5ac020550ebacc254ac9
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233876"
---
# JsGetAndClearException Funktion

Gibt die Ausnahme zurück, die dazu geführt hat, dass sich die Laufzeit des aktuellen Kontexts im Ausnahmezustand befindet, und setzt den Ausnahmezustand für diese Runtime zurück.  
  
## Syntax  
  
```cpp  
STDAPI_(JsErrorCode) JsGetAndClearException(  
   _Out_ JsValueRef *exception  
);  
```  
  
#### Parameter  
 `exception`  
 Die Ausnahme für die Common Language Runtime des aktuellen Kontexts.  
  
## Rückgabewert  
 Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.  
  
## Hinweise  
 Wenn sich die Laufzeit des aktuellen Kontexts nicht in einem Ausnahmezustand befindet, gibt diese API zurück `JsErrorInvalidArgument` . Wenn die Common Language Runtime deaktiviert ist, wird eine Ausnahme zurückgegeben, die besagt, dass das Skript beendet wurde, aber die Ausnahme wird nicht gelöscht (die Ausnahme wird gelöscht, wenn die Common Language Runtime mithilfe von erneut aktiviert wird `JsEnableRuntimeExecution` ).  
  
 Erfordert einen aktiven Skriptkontext.  
  
## Anforderungen  
 **Kopfzeile:** jsrt. h  
  
## Weitere Informationen  
 [Referenz (JavaScript-Laufzeit)](../chakra-hosting/reference-javascript-runtime.md)
