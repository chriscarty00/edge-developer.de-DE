---
description: Der Kontext, der an Application Callback, JsProjectionEnqueueCallback, von JsRT übergeben und dann zurück an JsRT im bereitgestellten Rückruf, `JsProjectionCallback` von der Anwendung im richtigen Thread übergeben wurde.
title: JsProjectionCallbackContext typedef | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 50c705c5-664f-4a1a-92f6-4882fc718ab1
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 58d4c74da13ae0dd269f3c101bbf3d2b95e77732
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10567212"
---
# JsProjectionCallbackContext typedef
Der Kontext, der an Application Callback, JsProjectionEnqueueCallback, von JsRT übergeben und dann zurück an JsRT im bereitgestellten Rückruf, `JsProjectionCallback` von der Anwendung im richtigen Thread übergeben wurde.  
  
## Syntax  
  
```cpp  
typedef void *JsProjectionCallbackContext;  
```  
  
## Hinweise  
 Erfordert Anrufe `JsSetProjectionEnqueueCallback` , um Rückrufe zu empfangen.  
  
 Diese API wird nur im EdgeHTML-Modus unterstützt.  
  
## Anforderungen  
 jsrt. h  
  
## Weitere Informationen  
 [Referenz (JavaScript-Laufzeit)](../chakra-hosting/reference-javascript-runtime.md)