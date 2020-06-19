---
description: ''
title: LongRunningScriptDetectedEvent-Objekt
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/10/2020
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, Windows 10-apps, UWP, Edge
ms.openlocfilehash: 5fe90495b83ab8f95ee594d3400c8c1a26f0547e
ms.sourcegitcommit: 037a2d62333691104c9accb4862968f80a3465a2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/18/2020
ms.locfileid: "10752151"
---
# LongRunningScriptDetectedEvent-Objekt  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

Enthält Informationen zu [MSWebViewLongRunningScriptDetected](../webview.md#mswebviewlongrunningscriptdetected).  

## Eigenschaften  

### executionTime  

Ruft die Anzahl der Millisekunden ab, die das [WebView](../webview.md) -Element ein Skript mit langer Ausführungsdauer ausführt.  

```javascript
var executionTime = LongRunningScriptDetectedEvent.executionTime;
```  

#### Eigenschaftenwert  

Typ: **Long**  

### stopPageScriptExecution  

Beendet ein Skript mit langer Ausführungszeit, das im [WebView](../webview.md) -Element ausgeführt wird.  

```javascript
var stopPageScriptExecution = LongRunningScriptDetectedEvent.stopPageScriptExecution;
```  

#### Eigenschaftenwert  

Typ: **boolescher Wert**  
