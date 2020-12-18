---
description: Der Anwendungsrückruf, der von JsRT aufgerufen wird, wenn eine Projektions-API in einem anderen Thread als das Original abgeschlossen ist.
title: JsProjectionEnqueueCallback typedef | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 19c1cefb-a7be-4196-b780-9fe6adf35ba5
caps.latest.revision: 4
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 47527d5e32076e40a82ab5452c2e0f624e8a2818
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11234314"
---
# JsProjectionEnqueueCallback Typedef

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
