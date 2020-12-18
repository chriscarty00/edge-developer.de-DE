---
description: Initialisiert die übergebene `VARIANT` als Projektion eines JavaScript-Werts.
title: JsValueToVariant-Funktion | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsValueToVariant
helpviewer_keywords:
- JsValueToVariant function
ms.assetid: 070244be-a69d-4b78-971b-69c0579c03cf
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: f383f2d8bc3aab70b4a361b370698cd71cb714d3
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233902"
---
# JsValueToVariant Funktion

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
