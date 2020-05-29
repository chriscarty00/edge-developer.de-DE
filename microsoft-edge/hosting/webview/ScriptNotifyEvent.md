---
description: Stellt eine Benachrichtigungs Zeichenfolge dar, die von WebView-Inhalt an die Anwendung übergeben wird.
title: ScriptNotifyEvent-Objekt
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2018
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, Windows 10-apps, UWP, Edge
ms.openlocfilehash: 22313f2d96ca2c5d4d3554ca40589b9a583c89cd
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10566693"
---
# ScriptNotifyEvent-Objekt

Ein Objekt, das ein Ereignis darstellt, das ausgelöst wird, wenn der Inhalt in der [WebView](../webview.md) eine Zeichenfolge mit JavaScript an die Anwendung übergibt.

## Eigenschaften
    
### callingUri

Ruft den Uniform Resource Identifier (URI) der Seite ab, die das Skript enthält, das das **ScriptNotifyEvent**ausgelöst hat.

Diese Eigenschaft ist schreibgeschützt.

```js
var callingUri = ScriptNotifyEvent.callingUri;
```

#### Eigenschaftenwert
Geben Sie Folgendes ein: **DOM**

### value

Der Methodenname, der an die Anwendung übergeben wird.

Diese Eigenschaft ist schreibgeschützt.

```js
var value = ScriptNotifyEvent.value;
```

#### Eigenschaftenwert
Geben Sie Folgendes ein: **DOM**