---
description: Ein Rückruf, der vor dem Sammeln eines Objekts aufgerufen wird.
title: JsObjectBeforeCollectCallback typedef | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: f21a064a-579f-44cb-9d21-76b62e8c18f5
caps.latest.revision: 3
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 4c24385ec5e15919719ffb0ae71c8adf39c1724c
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11234089"
---
# JsObjectBeforeCollectCallback Typedef

Ein Rückruf, der vor dem Sammeln eines Objekts aufgerufen wird.  
  
## Syntax  
  
```cpp  
typedef void (CALLBACK *JsObjectBeforeCollectCallback)(  
  _In_ JsRef ref,  
  _In_opt_ void *callbackState  
);  
```  
  
#### Parameter  
 `ref`  
 Das Objekt, das erfasst werden soll.  
  
 `callbackState`  
 Der Zustand, der übergeben wird `JsSetObjectBeforeCollectCallback` .  
  
## Hinweise  
 Diese API wird nur im EdgeHTML-Modus unterstützt.  
  
## Anforderungen  
 jsrt. h  
  
## Weitere Informationen  
 [Referenz (JavaScript-Laufzeit)](../chakra-hosting/reference-javascript-runtime.md)
