---
description: ''
title: LongRunningScriptDetectedEvent-Objekt
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/10/2018
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, Windows 10-apps, UWP, Edge
ms.openlocfilehash: 6cf7af656531eea5046f7af44d4d43ff224d0f08
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10567176"
---
# LongRunningScriptDetectedEvent-Objekt

Enthält Informationen zu [MSWebViewLongRunningScriptDetected](../webview.md#mswebviewlongrunningscriptdetected).

## Eigenschaften

### executionTime

Ruft die Anzahl der Millisekunden ab, die das [WebView](../webview.md) -Element ein Skript mit langer Ausführungsdauer ausführt.

```js
var executionTime = LongRunningScriptDetectedEvent.executionTime;
```

#### Eigenschaftenwert
Typ: **Long**

### stopPageScriptExecution
Beendet ein Skript mit langer Ausführungszeit, das im [WebView](../webview.md) -Element ausgeführt wird.

```js
var stopPageScriptExecution = LongRunningScriptDetectedEvent.stopPageScriptExecution;
```

#### Eigenschaftenwert
Typ: **boolescher Wert**