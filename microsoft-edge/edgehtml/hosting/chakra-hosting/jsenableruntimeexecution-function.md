---
description: 'Aktiviert die Skriptausführung in einer Laufzeit. '
title: JsEnableRuntimeExecution-Funktion | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsEnableRuntimeExecution
helpviewer_keywords:
- JsEnableRuntimeExecution function
ms.assetid: daa2036b-aef6-497d-a8ce-5a006b6ed13f
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: e87191197f70898b2f69d138026edd4e75cd5114
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233950"
---
# JsEnableRuntimeExecution Funktion

Aktiviert die Skriptausführung in einer Laufzeit.  
  
## Syntax  
  
```cpp  
STDAPI_(JsErrorCode) JsEnableRuntimeExecution(  
   _In_ JsRuntimeHandle runtime  
);  
```  
  
#### Parameter  
 `runtime`  
 Die Laufzeit, die aktiviert werden soll.  
  
## Rückgabewert  
 Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.  
  
## Hinweise  
 Das Aktivieren der Skriptausführung in einer Runtime, die bereits die Skriptausführung aktiviert hat, ist ein No-op.  
  
## Anforderungen  
 **Kopfzeile:** jsrt. h  
  
## Weitere Informationen  
 [Referenz (JavaScript-Laufzeit)](../chakra-hosting/reference-javascript-runtime.md)
