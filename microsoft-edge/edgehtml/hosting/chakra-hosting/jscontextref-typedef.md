---
description: Ein Verweis auf einen Skriptkontext.
title: JsContextRef typedef | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 8586bfcc-bb24-430d-a6f2-1a3b3e34ec2e
caps.latest.revision: 6
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: c8a8fcbd67afb150d682cfc19321f0f13acfe3a6
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233771"
---
# JsContextRef Typedef

Ein Verweis auf einen Skriptkontext.  
  
## Syntax  
  
```cpp  
typedef JsRef JsContextRef;  
```  
  
## Hinweise  
 Jeder Skriptkontext enthält sein eigenes globales Objekt, das sich vom globalen Objekt in anderen Skript Kontexten unterscheidet.  
  
 Viele Chakra-Hosting-APIs erfordern einen "aktiven" Skriptkontext, der mithilfe von verwendet werden kann `JsSetCurrentContext` . Chakra-Host-APIs, für die ein aktueller Kontext festzulegen ist, werden in Ihrer Dokumentation explizit festgestellt.  
  
## Anforderungen  
 **Kopfzeile:** jsrt. h  
  
## Weitere Informationen  
 [Referenz (JavaScript-Laufzeit)](../chakra-hosting/reference-javascript-runtime.md)
