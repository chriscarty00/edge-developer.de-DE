---
description: Ruft die dem Symbol zugeordnete Eigenschafts-ID ab.
title: JsGetPropertyIdFromSymbol-Funktion | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 190fe4b9-352e-4b10-9d0e-6c6bbd6363e8
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 0d11dbaf25b85e2bcd85a0cf2bac1b499fd4fa3e
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10568380"
---
# JsGetPropertyIdFromSymbol-Funktion
Ruft die dem Symbol zugeordnete Eigenschafts-ID ab.  
  
## Syntax  
  
```cpp  
STDAPI_(JsErrorCode) JsGetPropertyIdFromSymbol(  
   _In_ JsValueRef symbol,  
   _Out_ JsPropertyIdRef *propertyId  
);  
```  
  
#### Parameter  
 `symbol`  
 Das Symbol, dessen Eigenschafts-ID abgerufen wird.  
  
 `propertyId`  
 Die Eigenschafts-ID für das angegebene Symbol.  
  
## Rückgabewert  
 Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.  
  
## Hinweise  
 Eigenschafts-IDs sind für einen kontextspezifisch und können nicht in allen Kontexten verwendet werden.  
  
 Erfordert einen aktiven Skriptkontext.  
  
 Diese API wird nur im Microsoft Edge-Modus unterstützt.  
  
## Anforderungen  
 **Kopfzeile:** jsrt. h  
  
## Weitere Informationen  
 [Referenz (JavaScript-Laufzeit)](../chakra-hosting/reference-javascript-runtime.md)