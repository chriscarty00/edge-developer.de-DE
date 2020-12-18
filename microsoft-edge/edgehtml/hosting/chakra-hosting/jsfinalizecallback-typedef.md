---
description: Ein Finalizer-Rückruf.
title: JsFinalizeCallback typedef | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: aa7a0269-b9d4-4717-97ac-8da7eb6ced15
caps.latest.revision: 6
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 794edbb3a61c8c213c0908740ed0a867488a2c6d
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233883"
---
# JsFinalizeCallback Typedef

Ein Finalizer-Rückruf.  
  
## Syntax  
  
```cpp  
typedef void (CALLBACK *JsFinalizeCallback)(  
   _In_opt_ void *data  
);  
```  
  
#### Parameter  
 data  
 Die externen Daten, die beim Erstellen des finalisierten Objekts übergeben wurden.  
  
## Anforderungen  
 **Kopfzeile:** jsrt. h  
  
## Weitere Informationen  
 [Referenz (JavaScript-Laufzeit)](../chakra-hosting/reference-javascript-runtime.md)
