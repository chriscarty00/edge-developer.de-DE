---
description: Gibt eine Laufzeit frei.
title: JsDisposeRuntime-Funktion | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsDisposeRuntime
helpviewer_keywords:
- JsDisposeRuntime function
ms.assetid: 0aefde3f-7250-48be-afc5-53ea85c12f30
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 8cff4578415cdf1aaa01b7203ce734cef9115301
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233954"
---
# JsDisposeRuntime Funktion

Gibt eine Laufzeit frei.  
  
## Syntax  
  
```cpp  
STDAPI_(JsErrorCode) JsDisposeRuntime(  
   _In_ JsRuntimeHandle runtime  
);  
```  
  
#### Parameter  
 `runtime`  
 Die zu entsorgende Laufzeit.  
  
## Rückgabewert  
 Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.  
  
## Hinweise  
 Nachdem eine Laufzeit freigegeben wurde, sind alle von ihr besessenen Ressourcen ungültig und können nicht verwendet werden. Wenn die Common Language Runtime aktiv ist (d. h., dass Sie für einen bestimmten Thread auf Current gesetzt ist), kann Sie nicht freigegeben werden.  
  
## Anforderungen  
 **Kopfzeile:** jsrt. h  
  
## Weitere Informationen  
 [Referenz (JavaScript-Laufzeit)](../chakra-hosting/reference-javascript-runtime.md)
