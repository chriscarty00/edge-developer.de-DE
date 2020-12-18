---
description: Löscht die Eigenschaft eines Objekts.
title: JsDeleteProperty-Funktion | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsDeleteProperty
helpviewer_keywords:
- JsDeleteProperty function
ms.assetid: 0f6ac6a7-3576-42f5-98d0-1c06542c8149
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 55089bd4cff7ef4d58bcce1d7531d4ca1c7381ae
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233583"
---
# JsDeleteProperty Funktion

Löscht die Eigenschaft eines Objekts.  
  
## Syntax  
  
```cpp  
STDAPI_(JsErrorCode) JsDeleteProperty(  
   _In_ JsValueRef object,  
   _In_ JsPropertyIdRef propertyId,  
   _In_ bool useStrictRules,  
   _Out_ JsValueRef *result  
);  
```  
  
#### Parameter  
 `object`  
 Das Objekt, das die Eigenschaft enthält.  
  
 `propertyId`  
 Die ID der Eigenschaft.  
  
 `useStrictRules`  
 Der Eigenschaftensatz sollte strikte Regeln für den Modus befolgen.  
  
 `result`  
 Gibt an, ob die Eigenschaft gelöscht wurde.  
  
## Rückgabewert  
 Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.  
  
## Hinweise  
 Erfordert einen aktiven Skriptkontext.  
  
## Anforderungen  
 **Kopfzeile:** jsrt. h  
  
## Weitere Informationen  
 [Referenz (JavaScript-Laufzeit)](../chakra-hosting/reference-javascript-runtime.md)
