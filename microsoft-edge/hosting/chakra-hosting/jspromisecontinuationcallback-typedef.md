---
description: Ein Fortsetzungs Rückruf für Versprechen.
title: JsPromiseContinuationCallback typedef | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 51a3fd02-9668-4cf7-bb0b-e1fd03b2528f
caps.latest.revision: 3
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 023d88af5ff82056d8f57453e0a53b91b34565a6
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10567204"
---
# JsPromiseContinuationCallback typedef
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