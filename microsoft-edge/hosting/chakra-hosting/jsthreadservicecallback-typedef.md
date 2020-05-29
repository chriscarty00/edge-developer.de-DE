---
description: Ein Rückruf des Thread Diensts.
title: JsThreadServiceCallback typedef | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: dbe67be5-418a-4f66-8b68-b38078a6d140
caps.latest.revision: 6
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 5eb9f2986c79db024f01f4d22050f79c9689400c
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10567202"
---
# JsThreadServiceCallback typedef
Ein Rückruf des Thread Diensts.  
  
## Syntax  
  
```cpp  
typedef bool (CALLBACK *JsThreadServiceCallback)(  
   _In_ JsBackgroundWorkItemCallback callback,  
   _In_opt_ void *callbackData  
);  
```  
  
#### Parameter  
 Rückruf  
 Der Rückruf für die Hintergrund Arbeitsaufgabe.  
  
 callBackData  
 Das Daten Argument, das an den Rückruf übergeben werden soll.  
  
## Hinweise  
 Der Host kann einen Hintergrundthread Dienst angeben, wenn JsCreateRuntime aufgerufen wird. Wenn angegeben, werden Hintergrund Arbeitsaufgaben mithilfe dieses Rückrufs an den Host übergeben. Es wird erwartet, dass der Host die Hintergrund Arbeitsaufgabe sofort ausführt und "true" zurückgibt oder "false" zurückgibt und die Laufzeit die Arbeitsaufgabe in Thread behandelt.  
  
## Anforderungen  
 **Kopfzeile:** jsrt. h  
  
## Weitere Informationen  
 [Referenz (JavaScript-Laufzeit)](../chakra-hosting/reference-javascript-runtime.md)