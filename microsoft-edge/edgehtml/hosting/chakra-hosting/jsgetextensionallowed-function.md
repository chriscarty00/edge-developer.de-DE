---
description: Gibt einen Wert zurück, der angibt, ob ein Objekt erweiterbar ist oder nicht.
title: JsGetExtensionAllowed-Funktion | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsGetExtensionAllowed
helpviewer_keywords:
- JsGetExtensionAllowed function
ms.assetid: 839054a1-d643-47d9-89db-6a015bba0d91
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 7bc9e3265b48a27d0da4bc4646b2b5e3b1765b86
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233997"
---
# JsGetExtensionAllowed Funktion

Gibt einen Wert zurück, der angibt, ob ein Objekt erweiterbar ist oder nicht.  
  
## Syntax  
  
```cpp  
STDAPI_(JsErrorCode) JsGetExtensionAllowed(  
   _In_ JsValueRef object,  
   _Out_ bool *value  
);  
```  
  
#### Parameter  
 `object`  
 Das zu testende Objekt.  
  
 `value`  
 Gibt an, ob das Objekt erweiterbar ist oder nicht.  
  
## Rückgabewert  
 Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.  
  
## Hinweise  
 Erfordert einen aktiven Skriptkontext.  
  
## Anforderungen  
 **Kopfzeile:** jsrt. h  
  
## Weitere Informationen  
 [Referenz (JavaScript-Laufzeit)](../chakra-hosting/reference-javascript-runtime.md)
