---
description: Legt den zu verwendenden Rückruf fest, um einen Projektions Abschluss zurück zum erforderlichen Thread für Aufrufer aufzurufen.
title: JsSetProjectionEnqueueCallback-Funktion | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: c751ccef-20d2-4d41-9568-1c54adf47cdf
caps.latest.revision: 4
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 7dfedfeb1df5a97159a211795a2dd072d239bb35
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233733"
---
# JsSetProjectionEnqueueCallback Funktion

Legt den zu verwendenden Rückruf fest, um einen Projektions Abschluss zurück zum erforderlichen Thread für Aufrufer aufzurufen.  
  
## Syntax  
  
```cpp  
STDAPI_(JsErrorCode) JsSetProjectionEnqueueCallback(  
   _In_ JsProjectionEnqueueCallback projectionEnqueueCallback,  
   _In_opt_ void *projectionEnqueueContext);  
  
```  
  
#### Parameter  
 `projectionEnqueueContext`  
 Der Rückruf, der aufgerufen wird, wenn eine Projektion abgeschlossen wird, wenn ein Hintergrundthread ausgeführt wird.  
  
 `callbackState`  
 Der Anwendungskontext, der bereitgestellt wird `projectionEnqueueContext` .  
  
## Rückgabewert  
 Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.  
  
## Hinweise  
 Erfordert einen aktiven Skriptkontext.  
  
 Der Anruf sollte aus einem anderen com-Apartment oder einem anderen Thread im gleichen MTA erfolgen.  
  
 Diese API wird nur im EdgeHTML-Modus unterstützt.  
  
> [!CAUTION]
>  PInvoke wird derzeit für diese API nicht unterstützt.  
  
## Anforderungen  
 **Kopfzeile:** jsrt. h  
  
## Weitere Informationen  
 [Referenz (JavaScript-Laufzeit)](../chakra-hosting/reference-javascript-runtime.md)
