---
description: Ein Rückruf, der vor dem Sammeln eines Objekts aufgerufen wird.
title: JsObjectBeforeCollectCallback typedef | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: f21a064a-579f-44cb-9d21-76b62e8c18f5
caps.latest.revision: 3
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 27bbd1aed72cc751397ac4e6734f107612653b66
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10567214"
---
# JsObjectBeforeCollectCallback typedef
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