---
description: Ein Fortsetzungs Rückruf für Versprechen.
title: JsPromiseContinuationCallback typedef | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 51a3fd02-9668-4cf7-bb0b-e1fd03b2528f
caps.latest.revision: 3
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: da121d186cd9d0ab1a9770be08c9a92b52cf3366
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11234312"
---
# JsPromiseContinuationCallback Typedef

Ein Fortsetzungs Rückruf für Versprechen.  
  
## Syntax  
  
```cpp  
typedef void (CALLBACK *JsPromiseContinuationCallback)(  
  _In_ JsValueRef task,  
  _In_opt_ void *callbackState  
);  
```  
  
#### Parameter  
 `task`  
  `callbackState`  
  
## Hinweise  
 Der Host kann einen Promise-Fortsetzungs Rückruf in angeben `JsSetPromiseContinuationCallback` . Wenn ein Skript eine Aufgabe erstellt, die später ausgeführt werden soll, wird der Promise-Fortsetzungs Rückruf mit der Aufgabe aufgerufen, und die Aufgabe sollte in eine FIFO-Warteschlange gestellt werden, die ausgeführt werden soll, wenn das aktuelle Skript ausgeführt wird.  
  
 Diese API wird nur im EdgeHTML-Modus unterstützt.  
  
## Anforderungen  
 jsrt. h  
  
## Weitere Informationen  
 [Referenz (JavaScript-Laufzeit)](../chakra-hosting/reference-javascript-runtime.md)
