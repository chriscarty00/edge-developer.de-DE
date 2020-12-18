---
description: Ein Handle für eine Chakra-Laufzeit.
title: JsRuntimeHandle typedef | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 69e59bfd-9b0e-4710-9aa8-fbd6844171bc
caps.latest.revision: 6
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: ab08243505b9699fe07ca2e80f7294adf9eb78ad
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233735"
---
# JsRuntimeHandle Typedef

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
