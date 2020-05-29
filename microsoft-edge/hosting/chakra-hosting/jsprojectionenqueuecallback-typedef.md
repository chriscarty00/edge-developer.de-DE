---
description: Der Anwendungsrückruf, der von JsRT aufgerufen wird, wenn eine Projektions-API in einem anderen Thread als das Original abgeschlossen ist.
title: JsProjectionEnqueueCallback typedef | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 19c1cefb-a7be-4196-b780-9fe6adf35ba5
caps.latest.revision: 4
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 064a7d1077ae5222e44ab08ebe0592bb97b1f2af
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10567210"
---
# JsProjectionEnqueueCallback typedef
Der Anwendungsrückruf, der von JsRT aufgerufen wird, wenn eine Projektions-API in einem anderen Thread als das Original abgeschlossen ist.  
  
## Syntax  
  
```cpp  
typedef void (CALLBACK *JsProjectionEnqueueCallback)(  
  _In_ JsProjectionCallback jsCallback,  
  _In_ JsProjectionCallbackContext jsContext,  
  _In_opt_ void *callbackState  
);  
```  
  
#### Parameter  
 `jsCallback`  
 Der Rückruf, der für den ursprünglichen Thread aufgerufen werden soll.  
  
 `jsContext`  
 Der Anwendungskontext.  
  
 `callbackState`  
 Der JsRT-Kontext, an den übergeben werden muss `jsCallback` .  
  
## Hinweise  
 Erfordert das Aufrufen von JsSetProjectionEnqueueCallback, um Rückrufe zu empfangen.  
  
 Diese API wird nur im EdgeHTML-Modus unterstützt.  
  
## Anforderungen  
 jsrt. h  
  
## Weitere Informationen  
 [Referenz (JavaScript-Laufzeit)](../chakra-hosting/reference-javascript-runtime.md)