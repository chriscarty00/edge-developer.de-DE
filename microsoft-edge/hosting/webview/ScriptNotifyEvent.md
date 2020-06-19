---
description: Stellt eine Benachrichtigungs Zeichenfolge dar, die von WebView-Inhalt an die Anwendung übergeben wird.
title: ScriptNotifyEvent-Objekt
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/10/2020
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, Windows 10-apps, UWP, Edge
ms.openlocfilehash: 164bfa7228b1f4ccf9817e4b7231361d090f1394
ms.sourcegitcommit: 037a2d62333691104c9accb4862968f80a3465a2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/18/2020
ms.locfileid: "10752024"
---
# ScriptNotifyEvent-Objekt  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

Ein Objekt, das ein Ereignis darstellt, das ausgelöst wird, wenn der Inhalt in der [WebView](../webview.md) eine Zeichenfolge mit JavaScript an die Anwendung übergibt.  

## Eigenschaften  

### callingUri  

Ruft den Uniform Resource Identifier (URI) der Seite ab, die das Skript enthält, das das **ScriptNotifyEvent**ausgelöst hat.  

Diese Eigenschaft ist schreibgeschützt.  

```javascript
var callingUri = ScriptNotifyEvent.callingUri;
```  

#### Eigenschaftenwert  

Geben Sie Folgendes ein: **DOM**  

### value  

Der Methodenname, der an die Anwendung übergeben wird.  

Diese Eigenschaft ist schreibgeschützt.  

```javascript
var value = ScriptNotifyEvent.value;
```  

#### Eigenschaftenwert  

Geben Sie Folgendes ein: **DOM**  
