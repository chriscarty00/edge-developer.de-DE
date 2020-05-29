---
description: Ruft den Namen ab, der der Eigenschafts-ID zugeordnet ist.
title: JsGetPropertyNameFromId-Funktion | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsGetPropertyNameFromId
helpviewer_keywords:
- JsGetPropertyNameFromId function
ms.assetid: b4ca442c-573d-4bc3-adf7-1b8d48480b3a
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 1e76c69c1d746302bb95cd7229872845c4fbcc88
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10567250"
---
# JsGetPropertyNameFromId-Funktion
Ruft den Namen ab, der der Eigenschafts-ID zugeordnet ist.  
  
## Syntax  
  
```cpp  
STDAPI_(JsErrorCode) JsGetPropertyNameFromId(  
   _In_ JsPropertyIdRef propertyId,  
   _Outptr_result_z_ const wchar_t **name  
);  
```  
  
#### Parameter  
 `propertyId`  
 Die Eigenschafts-ID, deren Name abgerufen werden soll.  
  
 `name`  
 Der Name, der der Eigenschafts-ID zugeordnet ist.  
  
## Rückgabewert  
 Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.  
  
## Hinweise  
 Erfordert einen aktiven Skriptkontext.  
  
 Der zurückgegebene Puffer ist gültig, solange die Laufzeit aktiv ist, und kann nicht verwendet werden, nachdem die Laufzeit freigegeben wurde.  
  
## Anforderungen  
 **Kopfzeile:** jsrt. h  
  
## Weitere Informationen  
 [Referenz (JavaScript-Laufzeit)](../chakra-hosting/reference-javascript-runtime.md)