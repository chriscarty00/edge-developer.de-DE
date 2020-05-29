---
description: 'Legt eine Rückruffunktion fest, die von der Laufzeit vor der Garbage Collection aufgerufen wird. '
title: JsSetRuntimeBeforeCollectCallback-Funktion | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsSetRuntimeBeforeCollectCallback
helpviewer_keywords:
- JsSetRuntimeBeforeCollectCallback function
ms.assetid: 7b2fb911-6007-4ed9-a307-66cefe590ea4
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 31aefd28698c14a6fe17421a990a7c8b120876bf
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10568209"
---
# JsSetRuntimeBeforeCollectCallback-Funktion
Legt eine Rückruffunktion fest, die von der Laufzeit vor der Garbage Collection aufgerufen wird.  
  
## Syntax  
  
```cpp  
STDAPI_(JsErrorCode) JsSetRuntimeBeforeCollectCallback(  
   _In_ JsRuntimeHandle runtime,  
   _In_opt_ void *callbackState,  
   _In_ JsBeforeCollectCallback beforeCollectCallback  
);  
```  
  
#### Parameter  
 `runtime`  
 Die Laufzeit, für die der Zuordnungs Rückruf registriert werden soll.  
  
 `callbackState`  
 Der Benutzer hat den Zustand bereitgestellt, der an den Rückruf zurückgegeben wird.  
  
 `beforeCollectCallback`  
 Die Rückruffunktion, die festzulegen ist.  
  
## Rückgabewert  
 Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.  
  
## Hinweise  
 Der Rückruf wird für den aktuellen Runtime-Ausführungsthread aufgerufen, daher wird die Ausführung blockiert, bis der Rückruf abgeschlossen ist.  
  
 Der Rückruf kann von Hosts verwendet werden, um die Garbage Collection vorzubereiten. Beispielsweisedurch das Freigeben unnötiger Verweise auf Chakra-Objekte.  
  
## Anforderungen  
 **Kopfzeile:** jsrt. h  
  
## Weitere Informationen  
 [Referenz (JavaScript-Laufzeit)](../chakra-hosting/reference-javascript-runtime.md)