---
description: Der Kontext, der an Application Callback, JsProjectionEnqueueCallback, von JsRT übergeben und dann zurück an JsRT im bereitgestellten Rückruf, `JsProjectionCallback` von der Anwendung im richtigen Thread übergeben wurde.
title: JsProjectionCallbackContext typedef | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 50c705c5-664f-4a1a-92f6-4882fc718ab1
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 7742b0186a49e99f2738b81357b9e55cfe00042b
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11234075"
---
# JsProjectionCallbackContext Typedef

Der Kontext, der an Application Callback, JsProjectionEnqueueCallback, von JsRT übergeben und dann zurück an JsRT im bereitgestellten Rückruf, `JsProjectionCallback` von der Anwendung im richtigen Thread übergeben wurde.  
  
## Syntax  
  
```cpp  
typedef void *JsProjectionCallbackContext;  
```  
  
## Hinweise  
 Erfordert Anrufe `JsSetProjectionEnqueueCallback` , um Rückrufe zu empfangen.  
  
 Diese API wird nur im EdgeHTML-Modus unterstützt.  
  
## Anforderungen  
 jsrt. h  
  
## Weitere Informationen  
 [Referenz (JavaScript-Laufzeit)](../chakra-hosting/reference-javascript-runtime.md)
