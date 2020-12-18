---
description: Benutzer implementierte Rückruf Routine für Speicher Zuordnungs Ereignisse.
title: JsMemoryAllocationCallback typedef | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 511babc7-3caa-4ee5-82a2-943bbd34db8d
caps.latest.revision: 7
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 22b5cc0fe5a2c8b49f71c91d28f95ba29af37849
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233750"
---
# JsMemoryAllocationCallback Typedef

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
