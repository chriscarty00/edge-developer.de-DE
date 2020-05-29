---
description: Wird von der Common Language Runtime aufgerufen, wenn alle Ressourcen im Zusammenhang mit der Skriptausführung fertig sind. Der Aufrufer sollte die Quelle beim Laden, dem Bytecode und dem Kontext zu diesem Zeitpunkt freigeben.
title: JsSerializedScriptUnloadCallback typedef | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: 8d18c392-cca0-411e-9f2b-0d788b16161a
caps.latest.revision: 3
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 9555b3fd8c14c9629d17c13592e3c78a78be150e
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10568321"
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