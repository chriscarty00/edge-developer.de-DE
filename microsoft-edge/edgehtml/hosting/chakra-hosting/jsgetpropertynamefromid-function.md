---
description: Ruft den Namen ab, der der Eigenschafts-ID zugeordnet ist.
title: JsGetPropertyNameFromId-Funktion | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsGetPropertyNameFromId
helpviewer_keywords:
- JsGetPropertyNameFromId function
ms.assetid: b4ca442c-573d-4bc3-adf7-1b8d48480b3a
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 42061ab54a70fed571740961a909a6da17fb0733
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233964"
---
# JsGetPropertyNameFromId Funktion

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
