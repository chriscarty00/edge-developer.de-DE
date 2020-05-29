---
description: Gibt einen Verweis auf ein Garbage Collection-Objekt frei.
title: JsRelease-Funktion | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsRelease
helpviewer_keywords:
- JsRelease function
ms.assetid: 8714fd0b-5b66-48e0-927e-7b93af6cde7b
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 134ba16509b6c2f0c232214d7efba4d8c8915d43
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10568339"
---
# JsRelease-Funktion
Gibt einen Verweis auf ein Garbage Collection-Objekt frei.  
  
## Syntax  
  
```cpp  
STDAPI_(JsErrorCode) JsRelease(  
   _In_ JsRef ref,  
   _Out_opt_ unsigned int *count  
);  
```  
  
#### Parameter  
 `ref`  
 Das Objekt, auf das ein Verweis hinzugefügt werden soll.  
  
 `count`  
 Der neue Verweiszähler des Objekts (kann NULL übergeben).  
  
## Rückgabewert  
 Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.  
  
## Hinweise  
 Entfernt einen Verweis auf ein `JsRef` handle, das von erstellt wurde `JsAddRef` .  
  
## Anforderungen  
 **Kopfzeile:** jsrt. h  
  
## Weitere Informationen  
 [Referenz (JavaScript-Laufzeit)](../chakra-hosting/reference-javascript-runtime.md)