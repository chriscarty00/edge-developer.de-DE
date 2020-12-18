---
description: Projizieren Sie einen WinRT-Namespace.
title: JsProjectWinRTNamespace-Funktion | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 8a23c154-df4b-4ce3-9fef-f41f90acdb87
caps.latest.revision: 5
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: f781cf90aaec68b2bd305bf34c453fc663ad0187
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11234317"
---
# JsProjectWinRTNamespace Funktion

Projizieren Sie einen WinRT-Namespace.  
  
## Syntax  
  
```cpp  
STDAPI_(JsErrorCode)  
   JsProjectWinRTNamespace(  
   _In_z_ const wchar_t *namespaceName  
);  
```  
  
#### Parameter  
 `namespaceName`  
 Der WinRT-Namespace, der projiziert werden soll.  
  
## Rückgabewert  
 Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.  
  
## Hinweise  
 Erfordert einen aktiven Skriptkontext.  
  
 Diese API wird nur im EdgeHTML-Modus unterstützt.  
  
> [!NOTE]
>  WinRT war der Platt Form Name vor der universellen Windows-Plattform (UWP).  
  
## Anforderungen  
 **Kopfzeile:** jsrt. h  
  
## Weitere Informationen  
 [Referenz (JavaScript-Laufzeit)](../chakra-hosting/reference-javascript-runtime.md)
