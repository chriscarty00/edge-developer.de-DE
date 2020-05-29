---
description: Definiert Eigenschaften, die WebView-Features aktivieren oder deaktivieren.
title: MSWebViewSettings-Objekt
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/10/2018
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, Windows 10-apps, UWP, Edge
ms.openlocfilehash: 0e164e7eb44edc636201f283ec4bbe866a122b8e
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10567167"
---
# MSWebViewSettings-Objekt

Definiert Eigenschaften, die [WebView](../webview.md) -Features aktivieren oder deaktivieren.

## Eigenschaften

### isIndexedDBEnabled

Ruft einen Wert ab, der angibt, ob die Verwendung von IndexedDB in der [WebView](../webview.md)zulässig ist, oder legt diesen fest.

```js
var isIndexedDBEnabled = MSWebViewSettings.isIndexedDBEnabled;
MSWebViewSettings.isIndexedDBEnabled = isIndexedDBEnabled;
```

#### Eigenschaftenwert
Typ: **boolescher Wert**

**True** , wenn IndexedDB in der **WebView**zulässig ist, andernfalls false. andernfalls **false**. 

### isJavaScriptEnabled

Ruft einen Wert ab, der angibt, ob die Verwendung von JavaScript in der [WebView](../webview.md)zulässig ist, oder legt diesen fest.

```js
var isJavaScriptEnabled = MSWebViewSettings.isJavaScriptEnabled;
MSWebViewSettings.isJavaScriptEnabled = isJavaScriptEnabled;
```

#### Eigenschaftenwert
Typ: **boolescher Wert**

**True** JavaScript ist in der [WebView](../webview.md)zulässig; andernfalls **false**. 

### isScriptNotifyAllowed

Ruft einen Wert ab, der angibt, ob die Verwendung von [ScriptNotifyEvent](ScriptNotifyEvent.md) in der [WebView](../webview.md)zulässig ist, oder legt diesen fest.

```js
var isScriptNotifyAllowed = MSWebViewSettings.isScriptNotifyAllowed;
MSWebViewSettings.isScriptNotifyAllowed = isScriptNotifyAllowed;
```

#### Eigenschaftenwert
Typ: **boolescher Wert**

**True** [ScriptNotifyEvent](ScriptNotifyEvent.md) ist in der [WebView](../webview.md)zulässig; andernfalls **false**. 
