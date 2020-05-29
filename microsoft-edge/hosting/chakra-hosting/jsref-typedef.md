---
description: Ein Verweis auf ein Objekt, das dem Chakra Garbage Collector gehört.
title: JsRef typedef | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 6aafc39f-6b9c-457f-8bf0-48831bffe9b8
caps.latest.revision: 6
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: f5ce1ada67a4530ba57345b90c0b7deba6954c7c
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10568340"
---
# JsRef typedef
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