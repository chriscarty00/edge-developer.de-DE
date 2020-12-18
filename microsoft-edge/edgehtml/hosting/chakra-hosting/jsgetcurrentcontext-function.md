---
description: Ruft den aktuellen Skriptkontext im Thread ab.
title: JsGetCurrentContext-Funktion | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsGetCurrentContext
helpviewer_keywords:
- JsGetCurrentContext function
ms.assetid: dd5fe0fa-d1e5-4af6-809e-e655a27519b5
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: a43b9a6d4413ef1dc1b66321d6078aef84a0645f
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11234002"
---
# JsGetCurrentContext Funktion

Ruft den aktuellen Skriptkontext im Thread ab.  
  
## Syntax  
  
```cpp  
STDAPI_(JsErrorCode) JsGetCurrentContext(  
   _Out_ JsContextRef *currentContext  
);  
```  
  
#### Parameter  
 `currentContext`  
 Der aktuelle Skriptkontext im Thread, NULL, wenn kein aktueller Skriptkontext vorhanden ist.  
  
## Rückgabewert  
 Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.  
  
## Anforderungen  
 **Kopfzeile:** jsrt. h  
  
## Weitere Informationen  
 [Referenz (JavaScript-Laufzeit)](../chakra-hosting/reference-javascript-runtime.md)
