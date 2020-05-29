---
description: Definiert die eigene Eigenschaft eines neuen Objekts aus einem Eigenschaftendeskriptor.
title: JsDefineProperty-Funktion | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsDefineProperty
helpviewer_keywords:
- JsDefineProperty function
ms.assetid: b2cf48d6-eb40-457c-aa8b-b16a50dc5d6a
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: b3c9641b4d00540670b44d1718a6aa2aca3b02de
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10567276"
---
# JsDefineProperty-Funktion
Definiert die eigene Eigenschaft eines neuen Objekts aus einem Eigenschaftendeskriptor.  
  
## Syntax  
  
```cpp  
STDAPI_(JsErrorCode) JsDefineProperty(  
   _In_ JsValueRef object,  
   _In_ JsPropertyIdRef propertyId,  
   _In_ JsValueRef propertyDescriptor,  
   _Out_ bool *result  
);  
```  
  
#### Parameter  
 `object`  
 Das Objekt, das die Eigenschaft aufweist.  
  
 `propertyId`  
 Die ID der Eigenschaft.  
  
 `propertyDescriptor`  
 Der Eigenschaftendeskriptor.  
  
 `result`  
 Gibt an, ob die Eigenschaft definiert wurde.  
  
## Rückgabewert  
 Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.  
  
## Hinweise  
 Erfordert einen aktiven Skriptkontext.  
  
## Anforderungen  
 **Kopfzeile:** jsrt. h  
  
## Weitere Informationen  
 [Referenz (JavaScript-Laufzeit)](../chakra-hosting/reference-javascript-runtime.md)