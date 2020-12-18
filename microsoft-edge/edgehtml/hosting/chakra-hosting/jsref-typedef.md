---
description: Ein Verweis auf ein Objekt, das dem Chakra Garbage Collector gehört.
title: JsRef typedef | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 6aafc39f-6b9c-457f-8bf0-48831bffe9b8
caps.latest.revision: 6
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 69d13472b15b5d448908b5dafb2e3d7dc0ace7e4
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233576"
---
# JsRef Typedef

Ein Verweis auf ein Objekt, das dem Chakra Garbage Collector gehört.  
  
## Syntax  
  
```cpp  
typedef void *JsRef;  
```  
  
## Hinweise  
 Eine Chakra-Laufzeit erfasst JsRef-Verweise automatisch, solange Sie in lokalen Variablen oder in Parametern (also auf dem Stapel) gespeichert sind. Das Speichern eines JsRef an einer anderen Stelle als auf dem Stapel erfordert das Aufrufen von JsAddRef und JsRelease, um die Lebensdauer des Objekts zu verwalten, andernfalls kann der Garbage Collector das Objekt freigeben, während es noch verwendet wird.  
  
## Anforderungen  
 **Kopfzeile:** jsrt. h  
  
## Weitere Informationen  
 [Referenz (JavaScript-Laufzeit)](../chakra-hosting/reference-javascript-runtime.md)
