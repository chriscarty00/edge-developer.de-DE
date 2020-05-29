---
description: Ein Handle für eine Chakra-Laufzeit.
title: JsRuntimeHandle typedef | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 69e59bfd-9b0e-4710-9aa8-fbd6844171bc
caps.latest.revision: 6
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 4ccdcf39ec6062db47e1b9de249d75c8804de405
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10568323"
---
# JsRuntimeHandle typedef
Ein Handle für eine Chakra-Laufzeit.  
  
## Syntax  
  
```cpp  
typedef void *JsRuntimeHandle;  
```  
  
## Hinweise  
 Jede Chakra-Laufzeit verfügt über ein eigenes unabhängiges Ausführungsmodul, einen JIT-Compiler und einen Garbage Collector-Heap. Daher ist jede Laufzeit vollständig von anderen Laufzeiten isoliert.  
  
 Runtimes können für jeden Thread verwendet werden, aber nur ein Thread kann zu einem beliebigen Zeitpunkt eine Laufzeit aufrufen.  
  
> [!WARNING]
>  Eine JsRuntimeHandle ist im Gegensatz zu anderen Objekt verweisen in der Chakra-Hosting-API keine Garbage Collection, da Sie den Garbage Collection-Heap selbst enthält. Eine Common Language Runtime wird weiterhin vorhanden sein, bis JsDisposeRuntime aufgerufen wird.  
  
## Anforderungen  
 **Kopfzeile:** jsrt. h  
  
## Weitere Informationen  
 [Referenz (JavaScript-Laufzeit)](../chakra-hosting/reference-javascript-runtime.md)