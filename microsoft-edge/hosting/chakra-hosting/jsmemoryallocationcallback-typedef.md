---
description: Benutzer implementierte Rückruf Routine für Speicher Zuordnungs Ereignisse.
title: JsMemoryAllocationCallback typedef | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 511babc7-3caa-4ee5-82a2-943bbd34db8d
caps.latest.revision: 7
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: b11b3d076c01dbfcae190fd665528323d6f8b987
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10567222"
---
# JsMemoryAllocationCallback typedef
Benutzer implementierte Rückruf Routine für Speicher Zuordnungs Ereignisse.  
  
## Syntax  
  
```cpp  
typedef bool (CALLBACK * JsMemoryAllocationCallback)(  
   _In_opt_ void *callbackState,  
   _In_ JsMemoryEventType allocationEvent,  
   _In_ size_t allocationSize  
);  
```  
  
#### Parameter  
 callbackState  
 Der Zustand, der an JsSetRuntimeMemoryAllocationCallback übergeben wurde.  
  
 allocationEvent  
 Der Typ des Typen Zuordnungs Ereignisses.  
  
 verlagern  
 Die Größe der Zuordnung.  
  
## Eigenschaftswert/Rückgabewert  
 Für das JsMemoryAllocate-Ereignis ermöglicht die Rückgabe von true der Laufzeit, die Zuweisung fortzusetzen. Zurückgeben von false gibt an, dass die Zuordnungsanforderung abgelehnt wurde. Der Rückgabewert wird bei anderen Zuordnungs Ereignissen ignoriert.  
  
## Hinweise  
 Verwenden Sie JsSetRuntimeMemoryAllocationCallback, um diesen Rückruf zu registrieren.  
  
## Anforderungen  
 **Kopfzeile:** jsrt. h  
  
## Weitere Informationen  
 [Referenz (JavaScript-Laufzeit)](../chakra-hosting/reference-javascript-runtime.md)