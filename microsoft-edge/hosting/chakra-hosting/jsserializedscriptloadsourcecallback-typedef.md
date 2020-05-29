---
description: Wird von der Common Language Runtime aufgerufen, um den Quellcode des serialisierten Skripts zu laden. Der Aufrufer muss den skriptpuffer gültig halten, bis `JsSerializedScriptUnloadCallback` .
title: JsSerializedScriptLoadSourceCallback typedef | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: 9406c488-76ac-49e5-b305-39751f3412ea
caps.latest.revision: 3
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: bc1264bdc77da10cadb44a570ae37e7f3cd9ce6b
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10568322"
---
# JsSerializedScriptLoadSourceCallback typedef
Wird von der Common Language Runtime aufgerufen, um den Quellcode des serialisierten Skripts zu laden. Der Aufrufer muss den skriptpuffer gültig halten, bis `JsSerializedScriptUnloadCallback` .  
  
## Syntax  
  
```cpp  
typedef bool (CALLBACK * JsSerializedScriptLoadSourceCallback)(  
  _In_ JsSourceContextsourceContext,  
  _Outptr_result_z_ const wchar_t** scriptBuffer  
);  
```  
  
#### Parameter  
 `sourceContext`  
 Der Kontext, der an oder übergeben wurde `JsParseSerializedScriptWithCallback` `JsRunSerializedScriptWithCallback` .  
  
 `scriptBuffer`  
 Das Skript wurde zurückgegeben.  
  
## Hinweise  
  
> [!WARNING]
## Anforderungen  
 **Kopfzeile:** jsrt. h  
  
## Weitere Informationen  
 [Referenz (JavaScript-Laufzeit)](../chakra-hosting/reference-javascript-runtime.md)