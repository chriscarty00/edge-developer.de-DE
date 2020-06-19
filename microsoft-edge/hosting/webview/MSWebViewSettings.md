---
description: Definiert Eigenschaften, die WebView-Features aktivieren oder deaktivieren.
title: MSWebViewSettings-Objekt
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/10/2020
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, Windows 10-apps, UWP, Edge
ms.openlocfilehash: 147f852f8fbcb2a748c00b472814e9cc45b9c9da
ms.sourcegitcommit: 037a2d62333691104c9accb4862968f80a3465a2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/18/2020
ms.locfileid: "10752178"
---
# MSWebViewSettings-Objekt  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

Definiert Eigenschaften, die [WebView](../webview.md) -Features aktivieren oder deaktivieren.  

## Eigenschaften  

### isIndexedDBEnabled  

Ruft einen Wert ab, der angibt, ob die Verwendung von IndexedDB in der [WebView](../webview.md)zulässig ist, oder legt diesen fest.  

```javascript
var isIndexedDBEnabled = MSWebViewSettings.isIndexedDBEnabled;
MSWebViewSettings.isIndexedDBEnabled = isIndexedDBEnabled;
```  

#### Eigenschaftenwert  

Typ: **boolescher Wert**  

**True** , wenn IndexedDB in der **WebView**zulässig ist, andernfalls false. andernfalls **false**.  

### isJavaScriptEnabled  

Ruft einen Wert ab, der angibt, ob die Verwendung von JavaScript in der [WebView](../webview.md)zulässig ist, oder legt diesen fest.  

```javascript
var isJavaScriptEnabled = MSWebViewSettings.isJavaScriptEnabled;
MSWebViewSettings.isJavaScriptEnabled = isJavaScriptEnabled;
```  

#### Eigenschaftenwert  

Typ: **boolescher Wert**  

**True** JavaScript ist in der [WebView](../webview.md)zulässig; andernfalls **false**.  

### isScriptNotifyAllowed  

Ruft einen Wert ab, der angibt, ob die Verwendung von [ScriptNotifyEvent](ScriptNotifyEvent.md) in der [WebView](../webview.md)zulässig ist, oder legt diesen fest.  

```javascript
var isScriptNotifyAllowed = MSWebViewSettings.isScriptNotifyAllowed;
MSWebViewSettings.isScriptNotifyAllowed = isScriptNotifyAllowed;
```  

#### Eigenschaftenwert  

Typ: **boolescher Wert**  

**True** [ScriptNotifyEvent](ScriptNotifyEvent.md) ist in der [WebView](../webview.md)zulässig; andernfalls **false**.  
