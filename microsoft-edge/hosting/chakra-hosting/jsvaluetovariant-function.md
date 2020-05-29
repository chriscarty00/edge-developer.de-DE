---
description: Initialisiert die übergebene `VARIANT` als Projektion eines JavaScript-Werts.
title: JsValueToVariant-Funktion | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsValueToVariant
helpviewer_keywords:
- JsValueToVariant function
ms.assetid: 070244be-a69d-4b78-971b-69c0579c03cf
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: d8748fddcc149cf09fbd46ad3ad489cd66200b71
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10567195"
---
# JsValueToVariant-Funktion
Initialisiert die übergebene `VARIANT` als Projektion eines JavaScript-Werts.  
  
## Syntax  
  
```cpp  
STDAPI_(JsErrorCode) JsValueToVariant(  
   _In_ JsValueRef object,  
   _Out_ VARIANT *variant  
);  
```  
  
#### Parameter  
 `object`  
 Ein JavaScript-Wert für Project als `VARIANT` .  
  
 `variant`  
 Ein Zeiger auf eine `VARIANT` Struktur, die als Projektion initialisiert wird.  
  
## Rückgabewert  
  
## Hinweise  
 Die Projektion `VARIANT` kann von com-Automatisierungsclients verwendet werden, um das projizierte JavaScript-Objekt aufzurufen.  
  
 Erfordert einen aktiven Skriptkontext.  
  
## Anforderungen  
 **Kopfzeile:** jsrt. h  
  
## Weitere Informationen  
 [Referenz (JavaScript-Laufzeit)](../chakra-hosting/reference-javascript-runtime.md)