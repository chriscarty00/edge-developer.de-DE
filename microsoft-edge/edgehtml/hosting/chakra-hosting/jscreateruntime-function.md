---
description: Erstellt eine neue Laufzeit.
title: JsCreateRuntime-Funktion | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsCreateRuntime
helpviewer_keywords:
- JsCreateRuntime function
ms.assetid: 92d09b89-6593-4d73-a562-88f9fec10228
caps.latest.revision: 15
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 3b893bd75725d6d9da56417ba83adfce18d77bac
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233971"
---
# JsCreateRuntime Funktion

Erstellt eine neue Laufzeit.
  
## Syntax  
  
```cpp  
// Microsoft Edge mode signature  
STDAPI_(JsErrorCode) JsCreateRuntime(  
   _In_ JsRuntimeAttributes attributes,  
   _In_opt_ JsThreadServiceCallback threadService,  
   _Out_ JsRuntimeHandle *runtime);  
  
// Legacy mode signature  
STDAPI_(JsErrorCode) JsCreateRuntime(  
   _In_ JsRuntimeAttributes attributes,  
   _In_ JsRuntimeVersion version,  
   _In_opt_ JsThreadServiceCallback threadService,  
   _Out_ JsRuntimeHandle *runtime  
);  
```  
  
#### Parameter  
 `attributes`  
 Die Attribute der zu erstellende Laufzeit.  
  
 `version`  
 Die Version der zu erstellende Laufzeit.  
  
 `threadService`  
 Der Thread Dienst für die Laufzeit. Kann NULL sein.  
  
 `runtime`  
 Die erstellte Laufzeit.  
  
## Rückgabewert  
 Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.  
  
## Hinweise  
 Der `version` Parameter wird im Microsoft Edge-Modus nicht unterstützt. Weitere Informationen zur Verwendung dieser API im Microsoft Edge-Modus finden Sie unter [Targeting Microsoft Edge vs. Legacy Engines](../chakra-hosting/targeting-edge-vs-legacy-engines-in-jsrt-apis.md).  
  
## Anforderungen  
 **Kopfzeile:** jsrt. h  
  
## Weitere Informationen  
 [Referenz (JavaScript-Laufzeit)](../chakra-hosting/reference-javascript-runtime.md)
