---
description: Legt einen Speicher Zuordnungs Rückruf für die angegebene Laufzeit fest.
title: JsSetRuntimeMemoryAllocationCallback-Funktion | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsSetRuntimeMemoryAllocationCallback
helpviewer_keywords:
- JsSetRuntimeMemoryAllocationCallback function
ms.assetid: 6aa7d58d-6456-4df1-815f-1ba36fb4ae14
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 5c648761473023f00e894fbf75c794cfcc9422c5
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10568208"
---
# JsSetRuntimeMemoryAllocationCallback-Funktion
Legt einen Speicher Zuordnungs Rückruf für die angegebene Laufzeit fest.  
  
## Syntax  
  
```cpp  
STDAPI_(JsErrorCode) JsSetRuntimeMemoryAllocationCallback(  
   _In_ JsRuntimeHandle runtime,  
   _In_opt_ void *callbackState,  
   _In_ JsMemoryAllocationCallback allocationCallback  
);  
```  
  
#### Parameter  
 `runtime`  
 Die Laufzeit, für die der Zuordnungs Rückruf registriert werden soll.  
  
 `callbackState`  
 Der Benutzer hat den Zustand bereitgestellt, der an den Rückruf zurückgegeben wird.  
  
 `allocationCallback`  
 Speicher Zuordnungs Rückruf, der für Speicher Zuordnungs Ereignisse aufgerufen werden soll.  
  
## Rückgabewert  
 Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.  
  
## Hinweise  
 Wenn Sie einen Speicher Zuordnungs Rückruf registrieren, ruft die Common Language Runtime zurück an den Host, wenn dieser Speicher aus dem Betriebssystem abruft oder Speicher freigibt. Die Rückruf Routine wird aufgerufen, bevor der Laufzeitspeicher-Manager einen Speicherblock reserviert. Die Zuweisung wird zurückgewiesen, wenn der Rückruf false zurückgibt. Der Laufzeitspeicher-Manager ruft auch nach dem Freigeben eines Speicherblocks sowie nach Zuordnungsfehlern die Rückruf Routine auf.  
  
 Der Rückruf wird für den aktuellen Runtime-Ausführungsthread aufgerufen, daher wird die Ausführung blockiert, bis der Rückruf abgeschlossen ist.  
  
 Der Rückgabewert des Rückrufs wird nicht gespeichert; zuvor abgelehnte Zuweisungen verhindern nicht, dass die Common Language Runtime den Rückruf später für neue Speicherzuweisungen erneut aufruft.  
  
## Anforderungen  
 **Kopfzeile:** jsrt. h  
  
## Weitere Informationen  
 [Referenz (JavaScript-Laufzeit)](../chakra-hosting/reference-javascript-runtime.md)