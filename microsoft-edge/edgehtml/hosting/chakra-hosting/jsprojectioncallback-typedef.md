---
description: Der JsRT-Rückruf, der aufgerufen werden soll, wobei der Kontext an `JsProjectionEnqueueCallback` den richtigen Thread übergeben wird.
title: JsProjectionCallback typedef | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 32f22d37-e57e-4196-b6cd-a3fc75bd0632
caps.latest.revision: 3
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 211325b536dc84340974b02973f1de9d5749a60a
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11234079"
---
# JsProjectionCallback Typedef

Der JsRT-Rückruf, der aufgerufen werden soll, wobei der Kontext an `JsProjectionEnqueueCallback` den richtigen Thread übergeben wird.  
  
## Syntax  
  
```cpp  
typedef void (CALLBACK *JsProjectionCallback)(  
  _In_ JsProjectionCallbackContext jsContext  
);  
```  
  
#### Parameter  
 `jsContext`  
 Erfordert Anrufe `JsSetProjectionEnqueueCallback` , um Rückrufe zu empfangen.  
  
## Hinweise  
 Diese API wird nur im EdgeHTML-Modus unterstützt.  
  
## Anforderungen  
 jsrt. h  
  
## Weitere Informationen  
 [Referenz (JavaScript-Laufzeit)](../chakra-hosting/reference-javascript-runtime.md)
