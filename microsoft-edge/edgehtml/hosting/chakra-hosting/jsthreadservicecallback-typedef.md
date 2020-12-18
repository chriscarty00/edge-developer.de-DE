---
description: Ein Rückruf des Thread Diensts.
title: JsThreadServiceCallback typedef | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: dbe67be5-418a-4f66-8b68-b38078a6d140
caps.latest.revision: 6
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: a5f1fe416e158e9524bdd1caab847977a5dd21b8
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233904"
---
# JsThreadServiceCallback Typedef

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
