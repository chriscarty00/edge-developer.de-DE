---
description: Legt eine Rückruffunktion fest, die von der Laufzeit vor der Garbage Collection eines Objekts aufgerufen wird.
title: JsSetObjectBeforeCollectCallback-Funktion | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: ea2cbd94-d8b0-4fa9-a4a1-c75a4e338eaf
caps.latest.revision: 3
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 77a59c6ace96809c0b232c96aa9639555e7badcd
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10568306"
---
# JsSetObjectBeforeCollectCallback-Funktion
Legt eine Rückruffunktion fest, die von der Laufzeit vor der Garbage Collection eines Objekts aufgerufen wird.  
  
## Syntax  
  
```cpp  
STDAPI_(JsErrorCode) JsSetObjectBeforeCollectCallback(  
   _In_ JsRef ref,  
   _In_opt_ void *callbackState,  
   _In_ JsObjectBeforeCollectCallback objectBeforeCollectCallback  
);  
```  
  
#### Parameter  
 `ref`  
 Das Objekt, für das der Rückruf registriert werden soll.  
  
 `callbackState`  
 Vom Benutzer bereitgestellter Zustand, der an den Rückruf zurückgegeben wird.  
  
 `objectBeforeCollectCallback`  
 Die Rückruffunktion, die festzulegen ist. Verwenden Sie NULL, um zuvor registrierten Rückruf zu löschen.  
  
## Rückgabewert  
 Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.  
  
## Hinweise  
 Der Rückruf wird für den aktuellen Runtime-Ausführungsthread aufgerufen, daher wird die Ausführung blockiert, bis der Rückruf abgeschlossen ist.  
  
 Diese API wird nur im EdgeHTML-Modus unterstützt.  
  
## Anforderungen  
 **Kopfzeile:** jsrt. h  
  
## Weitere Informationen  
 [Referenz (JavaScript-Laufzeit)](../chakra-hosting/reference-javascript-runtime.md)