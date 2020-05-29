---
description: Ein Verweis auf einen Skriptkontext.
title: JsContextRef typedef | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 8586bfcc-bb24-430d-a6f2-1a3b3e34ec2e
caps.latest.revision: 6
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 80e4b5034079f4f0d26da070bd209aa41bf3475f
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10567323"
---
# JsContextRef typedef
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