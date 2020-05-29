---
description: Gibt die Ausnahme zurück, die dazu geführt hat, dass sich die Laufzeit des aktuellen Kontexts im Ausnahmezustand befindet, und setzt den Ausnahmezustand für diese Runtime zurück.
title: JsGetAndClearException-Funktion | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsGetAndClearException
helpviewer_keywords:
- JsGetAndClearException function
ms.assetid: 6aec8a88-41ee-47f6-b5f4-32f3cae6bb7b
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: eb70b4b66b4bb270d9f26487708720efddc2effa
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10568398"
---
# JsGetAndClearException-Funktion
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