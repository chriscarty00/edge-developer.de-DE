---
description: Wird von der Common Language Runtime aufgerufen, wenn alle Ressourcen im Zusammenhang mit der Skriptausführung fertig sind. Der Aufrufer sollte die Quelle beim Laden, dem Bytecode und dem Kontext zu diesem Zeitpunkt freigeben.
title: JsSerializedScriptUnloadCallback typedef | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 8d18c392-cca0-411e-9f2b-0d788b16161a
caps.latest.revision: 3
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 5c63f2ff3faf21a19e31f2f6fd1692e21d59fc0b
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11234261"
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
