---
description: Stellt einen WebView-Prozess dar.
title: MSWebViewProcess-Objekt
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/10/2020
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, Windows 10-apps, UWP, Edge
ms.openlocfilehash: bb70b0e8eb12c7a7c23d71f01ea24e9084caa156
ms.sourcegitcommit: 037a2d62333691104c9accb4862968f80a3465a2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/18/2020
ms.locfileid: "10752156"
---
# MSWebViewProcess-Objekt  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

Stellt einen [WebView](../webview.md) -Prozess dar.  

```javascript
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

```javascript
var privateNetwork = wvprocess.isPrivateNetworkClientServerCapabilityEnabled;
```  

Diese Eigenschaft ist schreibgeschützt.  

#### Eigenschaftenwert  

Typ: **boolescher Wert**  

## Methoden  

### CreateWebViewAsync  

Erstellt eine [WebView](../webview.md) in einem bestimmten Prozess.  

```javascript
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

```javascript
wvprocess.terminate();
```  

#### Rückgabewert  

Diese Methode gibt keinen Wert zurück.  
