---
description: Gibt einen Wert zurück, der angibt, ob die Skriptausführung in der Laufzeit deaktiviert ist.
title: JsIsRuntimeExecutionDisabled-Funktion | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsIsRuntimeExecutionDisabled
helpviewer_keywords:
- JsIsRuntimeExecutionDisabled function
ms.assetid: 77490280-fb84-4614-a1f0-6ac31e3bd607
caps.latest.revision: 5
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 6968a31c9acab70589fe58c86cc566e631778c3c
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10567223"
---
# JsIsRuntimeExecutionDisabled-Funktion
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