---
description: Legt den zu verwendenden Rückruf fest, um einen Projektions Abschluss zurück zum erforderlichen Thread für Aufrufer aufzurufen.
title: JsSetProjectionEnqueueCallback-Funktion | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: c751ccef-20d2-4d41-9568-1c54adf47cdf
caps.latest.revision: 4
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 02da0238360b0dc6fff9bb86c9f5ab04d1ba7112
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10568302"
---
# JsSetProjectionEnqueueCallback-Funktion
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