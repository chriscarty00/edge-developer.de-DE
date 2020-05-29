---
description: Ein Fehlercode, der von einer Chakra-Hosting-API zurückgegeben wird.
title: JsErrorCode-Enumeration | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsErrorCode
helpviewer_keywords:
- JsErrorCode enumeration
ms.assetid: 4902f3f3-47a5-4e74-9c29-f96eeecbcda9
caps.latest.revision: 15
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: e3d1a319872ac69b2acaf19997f3c38f9c04597b
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10568400"
---
# JsErrorCode-Enumeration
Ein Fehlercode, der von einer Chakra-Hosting-API zurückgegeben wird.  
  
## Syntax  
  
```cpp  
enum JsErrorCode : unsigned int;  
```  
  
## Member  
  
### Werte  
  
|Name|Beschreibung|  
|----------|-----------------|  
|`JsErrorAlreadyDebuggingContext`|Der Kontext kann nicht in einen Debug-Zustand versetzt werden, da er sich bereits in einem Debugstatus befindet.|  
|`JsErrorAlreadyProfilingContext`|Der Kontext kann die Profilerstellung nicht starten, da er bereits Profilerstellung ist.|  
|`JsErrorArgumentNotObject`|Eine Hosting-API, die für Objektwerte verwendet wird, wurde mit einem nicht-Objekt-Wert aufgerufen.|  
|`JsErrorBadSerializedScript`|Es wurde ein fehlerhaftes serialisiertes Skript verwendet, oder das serialisierte Skript wurde von einer anderen Version des Chakra-Moduls serialisiert.|  
|`JsErrorCannotDisableExecution`|Runtime unterstützt keine zuverlässige Skript Unterbrechung.|  
|`JsErrorCannotSerializeDebugScript`|Skripts können nicht in Debug-Kontexten serialisiert werden.|  
|`JsErrorCategoryEngine`|Fehlerkategorie, die sich auf Fehler im Modul selbst bezieht.|  
|`JsErrorCategoryFatal`|Kategorie der Fehler, die fatal sind und einen Fehler des Moduls signalisieren.|  
|`JsErrorCategoryScript`|Fehlerkategorie, die sich auf Fehler in einem Skript bezieht.|  
|`JsErrorCategoryUsage`|Fehlerkategorie, die sich auf eine falsche Verwendung der API selbst bezieht.|  
|`JsErrorFatal`|Ein schwerwiegender Fehler im Modul ist aufgetreten.|  
|`JsErrorHeapEnumInProgress`|Im Skriptkontext läuft derzeit eine Heap-Enumeration.|  
|`JsErrorIdleNotEnabled`|Leerlauf Benachrichtigung, wenn der Host die Leerlaufverarbeitung nicht aktiviert hat.|  
|`JsErrorInDisabledState`|Die Laufzeit befindet sich in einem deaktivierten Zustand.|  
|`JsErrorInExceptionState`|Das Modul befindet sich in einem Ausnahmezustand, und es können keine APIs aufgerufen werden, bis die Ausnahme gelöscht wurde.|  
|`JsErrorInObjectBeforeCollectCallback`|Der Vorgang wird in einem Objekt vor dem Collect-Rückruf nicht unterstützt.<br /><br /> Dieser Enumerationswert wird nur im Microsoft Edge-Modus unterstützt.|  
|`JsErrorInProfileCallback`|Ein Skriptkontext befindet sich in der Mitte eines Profil Rückrufs.|  
|`JsErrorInThreadServiceCallback`|Ein Thread Dienst Rückruf ist derzeit im Gange.|  
|`JsErrorInvalidArgument`|Ein Argument für eine Hosting-API war ungültig.|  
|`JsErrorNoCurrentContext`|Die Hosting-API setzt voraus, dass ein Kontext aktuell ist, aber es gibt keinen aktuellen Kontext.|  
|`JsErrorNotImplemented`|Eine Hosting-API ist noch nicht implementiert.|  
|`JsErrorNullArgument`|Ein Argument für eine Hosting-API war NULL in einem Kontext, in dem NULL nicht zulässig ist.|  
|`JsErrorObjectNotInspectable`|Das Objekt kann nicht in den Zeiger umgebrochen werden `IInspectable` .<br /><br /> Dieser Enumerationswert wird nur im Microsoft Edge-Modus unterstützt.|  
|`JsErrorOutOfMemory`|Das Chakra-Modul hat keinen Arbeitsspeicher mehr.|  
|`JsErrorPropertyNotSymbol`|Eine Hosting-API, die für Symbol Eigenschafts-IDs verwendet wird, aber mit einer nicht-Symbol-Eigenschafts-ID aufgerufen wurde. Der Fehlercode wird von zurückgegeben, `JsGetSymbolFromPropertyId` Wenn die Funktion mit einer nicht-Symbol-Eigenschafts-ID aufgerufen wird.<br /><br /> Dieser Enumerationswert wird nur im Microsoft Edge-Modus unterstützt.|  
|`JsErrorPropertyNotString`|Eine Hosting-API, die für Zeichenfolgeneigenschaften-IDs verwendet wird, aber mit einer Eigenschafts-ID ohne Zeichenfolge aufgerufen wurde. Der Fehlercode wird von vorhanden zurückgegeben, `JsGetPropertyNamefromId` Wenn die Funktion mit einer nicht-Zeichenfolgen-Eigenschafts-ID aufgerufen wird.<br /><br /> Dieser Enumerationswert wird nur im Microsoft Edge-Modus unterstützt.|  
|`JsErrorRuntimeInUse`|Eine noch verwendete Laufzeit kann nicht freigegeben werden.|  
|`JsErrorScriptCompile`|JavaScript konnte nicht kompiliert werden.|  
|`JsErrorScriptEvalDisabled`|Ein Skript wurde beendet, weil es versucht hat, zu verwenden, `eval` oder `function` und eval wurde deaktiviert.|  
|`JsErrorScriptException`|Beim Ausführen eines Skripts ist eine JavaScript-Ausnahme aufgetreten.|  
|`JsErrorScriptTerminated`|Ein Skript wurde aufgrund einer Anforderung zum Anhalten einer Laufzeit beendet.|  
|`JsErrorWrongRuntime`|Eine Hosting-API wurde mit einem Objekt aufgerufen, das unter einer anderen JavaScript-Laufzeit erstellt wurde.|  
|`JsErrorWrongThread`|Eine Hosting-API wurde im falschen Thread aufgerufen.|  
|`JsNoError`|Erfolgs Fehlercode.|  
  
## Anforderungen  
 **Kopfzeile:** jsrt. h  
  
## Weitere Informationen  
 [Referenz (JavaScript-Laufzeit)](../chakra-hosting/reference-javascript-runtime.md)