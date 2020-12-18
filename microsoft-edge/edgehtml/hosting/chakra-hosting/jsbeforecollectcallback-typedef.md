---
description: Ein Rückruf, der vor der Sammlung aufgerufen wird.
title: JsBeforeCollectCallback typedef | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 58bece47-4e6d-49e7-a93d-b6a8f9928b41
caps.latest.revision: 6
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 23ed386a6a28d356aa80cf85650a981d4836a6b6
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233773"
---
# JsBeforeCollectCallback Typedef

Ein Rückruf, der vor der Sammlung aufgerufen wird.  
  
## Syntax  
  
```cpp  
typedef void (CALLBACK *JsBeforeCollectCallback)(  
_In_opt_ void *callbackState  
);  
```  
  
#### Parameter  
 callbackState  
 Der Zustand, der an JsSetBeforeCollectCallback übergeben wurde.  
  
## Hinweise  
 Verwenden Sie JsSetBeforeCollectCallback, um diesen Rückruf zu registrieren.  
  
## Anforderungen  
 **Kopfzeile:** jsrt. h  
  
## Weitere Informationen  
 [Referenz (JavaScript-Laufzeit)](../chakra-hosting/reference-javascript-runtime.md)
