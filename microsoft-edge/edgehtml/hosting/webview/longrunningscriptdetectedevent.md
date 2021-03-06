---
description: LongRunningScriptDetectedEvent-Objekt
title: LongRunningScriptDetectedEvent-Objekt
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/03/2020
ms.topic: reference
ms.prod: microsoft-edge
keywords: Webview, Windows 10-Apps, UWP, Edge
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 5f5eb3230e46ee2cd7926b21f6526e512a7a0322
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "11397941"
---
# <a name="longrunningscriptdetectedevent-object"></a>LongRunningScriptDetectedEvent-Objekt  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

Enthält Informationen für [MSWebViewLongRunningScriptDetected](../webview/index.md#mswebviewlongrunningscriptdetected).  

## <a name="properties"></a>Eigenschaften  

### <a name="executiontime"></a>executionTime  

Ruft die Anzahl von Millisekunden ab, mit der das [Webview-Element](../webview/index.md) ein lange ausgeführtes Skript ausgeführt hat.  

```javascript
var executionTime = LongRunningScriptDetectedEvent.executionTime;
```  

#### <a name="property-value"></a>Eigenschaftenwert  

Typ: **long**  

### <a name="stoppagescriptexecution"></a>stopPageScriptExecution  

Stoppt ein lange ausgeführtes Skript, das im [webview-Element ausgeführt](../webview/index.md) wird.  

```javascript
var stopPageScriptExecution = LongRunningScriptDetectedEvent.stopPageScriptExecution;
```  

#### <a name="property-value"></a>Eigenschaftenwert  

Typ: **Boolean**  
