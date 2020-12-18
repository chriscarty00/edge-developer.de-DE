---
description: Wird von der Common Language Runtime aufgerufen, um den Quellcode des serialisierten Skripts zu laden. Der Aufrufer muss den skriptpuffer gültig halten, bis `JsSerializedScriptUnloadCallback` .
title: JsSerializedScriptLoadSourceCallback typedef | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 9406c488-76ac-49e5-b305-39751f3412ea
caps.latest.revision: 3
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 2bb30befc61003d20cdeaa293fd1fdfdc95b36f7
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11234311"
---
# JsSerializedScriptLoadSourceCallback Typedef

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
