---
description: Wird von der Common Language Runtime aufgerufen, wenn alle Ressourcen im Zusammenhang mit der Skriptausführung fertig sind. Der Aufrufer sollte die Quelle beim Laden, dem Bytecode und dem Kontext zu diesem Zeitpunkt freigeben.
title: JsSerializedScriptUnloadCallback typedef | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 8d18c392-cca0-411e-9f2b-0d788b16161a
caps.latest.revision: 3
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: c3da27af18ebc7a1913980a865d926bac6a29d11
ms.sourcegitcommit: 037a2d62333691104c9accb4862968f80a3465a2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/18/2020
ms.locfileid: "10751940"
---
# JsSerializedScriptUnloadCallback typedef
Wird von der Common Language Runtime aufgerufen, wenn alle Ressourcen im Zusammenhang mit der Skriptausführung fertig sind. Der Aufrufer sollte die Quelle beim Laden, dem Bytecode und dem Kontext zu diesem Zeitpunkt freigeben.  
  
## Syntax  
  
```cpp  
 typedef void (CALLBACK * JsSerializedScriptUnloadCallback)(  
  _In_ JsSourceContext sourceContext  
);  
```  
  
#### Parameter  
 `sourceContext`  
 Der Kontext, der an oder übergeben wurde `JsParseSerializedScriptWithCallback` `JsRunSerializedScriptWithCallback` .  
  
## Hinweise  
  
> [!WARNING]
## Anforderungen  
 **Kopfzeile:** jsrt. h  
  
## Weitere Informationen  
 [Referenz (JavaScript-Laufzeit)](../chakra-hosting/reference-javascript-runtime.md)