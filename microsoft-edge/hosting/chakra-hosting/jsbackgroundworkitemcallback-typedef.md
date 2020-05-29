---
description: Ein Rückruf für einen Arbeitsaufgaben Hintergrund
title: JsBackgroundWorkItemCallback typedef | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: e6db52e1-830c-46a2-b9f9-cc2d450a1da8
caps.latest.revision: 6
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 9bc1e5687d92d7286e1e6d4387bd6b69d95ceb68
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10567336"
---
# JsBackgroundWorkItemCallback typedef
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