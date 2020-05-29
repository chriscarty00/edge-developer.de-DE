---
description: Stellt einen WebView-Prozess dar.
title: MSWebViewProcess-Objekt
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/15/2020
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, Windows 10-apps, UWP, Edge
ms.openlocfilehash: 7581f6da3a23295180c50f6d41cc282ce998b64e
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10567169"
---
# MSWebViewProcess-Objekt

Stellt einen [WebView](../webview.md) -Prozess dar.

```js
var wvprocess = new MSWebViewProcess();
```

## Eigenschaften

### Enterprise-Nr

Die Enterprise-ID des Prozesses.

```js
var enterpriseId = wvprocess.enterpriseId;
```

Diese Eigenschaft ist schreibgeschützt.

#### Eigenschaftenwert
Geben Sie Folgendes ein: **DOM**

### isPrivateNetworkClientServerCapabilityEnabled

Ruft einen Wert ab, der angibt, ob der [WebView](../webview.md) -Prozess im App-Manifest die Funktion für die universelle Windows- [App-Funktionsdeklaration](/windows/uwp/packaging/app-capability-declarations) für *private Netzwerke (Client & Server)* aktiviert hat.

```js
var privateNetwork = wvprocess.isPrivateNetworkClientServerCapabilityEnabled;
```

Diese Eigenschaft ist schreibgeschützt.

#### Eigenschaftenwert
Typ: **boolescher Wert**

## Methoden

### CreateWebViewAsync

Erstellt eine [WebView](../webview.md) in einem bestimmten Prozess.

```js
wvprocess.createWebviewAsync();
```

#### Rückgabewert

Geben**`Promise<MSHTMLWebViewElement>`**

### Webviews

Gibt eine Sequenz von **MSWebViewProcess** -Objekten zurück, die innerhalb des Prozesses gehostet werden.

#### Rückgabewert

Geben**`sequence<MSHTMLWebViewElement>`**

### Beenden

Beendet den Prozess.

```js
wvprocess.terminate();
```

#### Rückgabewert

Diese Methode gibt keinen Wert zurück.
