---
description: Ruft die Laufzeit ab, zu der der Kontext gehört.
title: JsGetRuntime-Funktion | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsGetRuntime
helpviewer_keywords:
- JsGetRuntime function
ms.assetid: 5b62e940-a885-405a-9fdd-0495fb391b95
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 49739f0cf3675a44b9fc328e3eaa7d49c6282e53
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233965"
---
# JsGetRuntime Funktion

Ruft die Laufzeit ab, zu der der Kontext gehört.  
  
## Syntax  
  
```cpp  
STDAPI_(JsErrorCode) JsGetRuntime(  
   _In_ JsContextRef context,  
   _Out_ JsRuntimeHandle *runtime  
);  
```  
  
#### Parameter  
 `context`  
 Der Kontext, aus dem die Laufzeit abgerufen werden soll.  
  
 `runtime`  
 Die Laufzeit, zu der der Kontext gehört.  
  
## Rückgabewert  
 Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.  
  
## Anforderungen  
 **Kopfzeile:** jsrt. h  
  
## Weitere Informationen  
 [Referenz (JavaScript-Laufzeit)](../chakra-hosting/reference-javascript-runtime.md)
