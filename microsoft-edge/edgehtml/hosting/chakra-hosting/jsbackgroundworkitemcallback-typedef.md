---
description: Ein Rückruf für einen Arbeitsaufgaben Hintergrund
title: JsBackgroundWorkItemCallback typedef | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: e6db52e1-830c-46a2-b9f9-cc2d450a1da8
caps.latest.revision: 6
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: d69306b334c2e0c9b27b96a5a417739ffdcd7dd7
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233782"
---
# JsBackgroundWorkItemCallback Typedef

Ein Rückruf für einen Arbeitsaufgaben Hintergrund  
  
## Syntax  
  
```cpp  
typedef void (CALLBACK *JsBackgroundWorkItemCallback)(  
   _In_opt_ void *callbackData  
);  
```  
  
#### Parameter  
 callBackData  
 Daten Argument, das an den Thread Dienst übergeben wird.  
  
## Hinweise  
 Diese wird an den Thread Dienst des Hosts übergeben (sofern vorhanden), damit der Host den Arbeitsaufgaben Rückruf im Hintergrundthread seiner Wahl aufrufen kann.  
  
## Anforderungen  
 **Kopfzeile:** jsrt. h  
  
## Weitere Informationen  
 [Referenz (JavaScript-Laufzeit)](../chakra-hosting/reference-javascript-runtime.md)
