---
description: Bestimmt, ob sich die Laufzeit des aktuellen Kontexts in einem Ausnahmezustand befindet.
title: JsHasException-Funktion | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsHasException
helpviewer_keywords:
- JsHasException function
ms.assetid: ac7da3ce-c746-4154-bbb8-bcb0859a8d5b
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 4f4abbd6c69a6b2b6414dae2f1de3a2acf21cc32
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233617"
---
# JsHasException Funktion

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
