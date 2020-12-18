---
description: Fügt einen Verweis auf ein Garbage Collected-Objekt hinzu.
title: JsAddRef-Funktion | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsAddRef
helpviewer_keywords:
- JsAddRef function
ms.assetid: a7f3ed49-6a86-489a-abdf-c99428e79cae
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: fd397dbfeacafdf12728ef0ca2a98d97405f6592
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233784"
---
# JsAddRef Funktion

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
