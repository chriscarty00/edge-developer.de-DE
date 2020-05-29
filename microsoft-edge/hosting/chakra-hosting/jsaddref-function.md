---
description: Fügt einen Verweis auf ein Garbage Collected-Objekt hinzu.
title: JsAddRef-Funktion | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsAddRef
helpviewer_keywords:
- JsAddRef function
ms.assetid: a7f3ed49-6a86-489a-abdf-c99428e79cae
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: bd02dded6dc2877228f22b4d2800e41a78163467
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10567337"
---
# JsAddRef-Funktion
Fügt einen Verweis auf ein Garbage Collected-Objekt hinzu.  
  
## Syntax  
  
```cpp  
STDAPI_(JsErrorCode) JsAddRef(  
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
 Dies muss nur für `JsRef` Handles aufgerufen werden, die nicht irgendwo auf dem Stapel gespeichert werden. Durch das Aufrufen wird `JsAddRef` sichergestellt, dass das Objekt `JsRef` , auf das verwiesen wird, erst `JsRelease` aufgerufen wird.  
  
## Anforderungen  
 **Kopfzeile:** jsrt. h  
  
## Weitere Informationen  
 [Referenz (JavaScript-Laufzeit)](../chakra-hosting/reference-javascript-runtime.md)