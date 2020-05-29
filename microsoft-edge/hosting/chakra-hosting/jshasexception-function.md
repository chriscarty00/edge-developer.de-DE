---
description: Bestimmt, ob sich die Laufzeit des aktuellen Kontexts in einem Ausnahmezustand befindet.
title: JsHasException-Funktion | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsHasException
helpviewer_keywords:
- JsHasException function
ms.assetid: ac7da3ce-c746-4154-bbb8-bcb0859a8d5b
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 25ddb8f9cc407dd414a6cd2210c315eb4dd7b141
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10568364"
---
# JsHasException-Funktion
Bestimmt, ob sich die Laufzeit des aktuellen Kontexts in einem Ausnahmezustand befindet.  
  
## Syntax  
  
```cpp  
STDAPI_(JsErrorCode) JsHasException(  
   _Out_ bool *hasException  
);  
```  
  
#### Parameter  
 `hasException`  
 Gibt an, ob sich die Laufzeit des aktuellen Kontexts im Ausnahmezustand befindet.  
  
## Rückgabewert  
 Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.  
  
## Hinweise  
 Wenn ein Aufruf der Laufzeit zu einer Ausnahme führt (entweder durch Ausführen eines Skripts oder aufgrund eines Konvertierungs Fehlers), wird die Common Language Runtime in einen "Ausnahmezustand" versetzt. Alle Aufrufe in alle von der Laufzeit erstellten Kontexte (mit Ausnahme der Ausnahme-APIs) können `JsErrorInExceptionState` bis zum Löschen der Ausnahme fehlschlagen.  
  
 Wenn sich die Laufzeit des aktuellen Kontexts im Ausnahmezustand befindet, wenn ein Rückruf in das Modul zurückgegeben wird, löst das Modul automatisch die Ausnahme aus.  
  
 Erfordert einen aktiven Skriptkontext.  
  
## Anforderungen  
 **Kopfzeile:** jsrt. h  
  
## Weitere Informationen  
 [Referenz (JavaScript-Laufzeit)](../chakra-hosting/reference-javascript-runtime.md)