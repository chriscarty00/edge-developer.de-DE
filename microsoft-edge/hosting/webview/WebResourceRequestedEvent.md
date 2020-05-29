---
description: Ein Ereignis, das ausgelöst wird, wenn eine HTTP-Anforderung durchgeführt wird.
title: WebResourceRequestedEvent-Objekt
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/15/2020
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, Windows 10-apps, UWP, Edge
ms.openlocfilehash: 79cff0d8fd68e3b5747008f343b5b46fb8093013
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10566689"
---
# WebResourceRequestedEvent-Objekt

Ein Ereignis, das ausgelöst wird, wenn eine HTTP-Anforderung durchgeführt wird.

## Eigenschaften

### args

Informationen zur Ressourcenanforderung. Dies ist ein [Windows. Web. UI. WebViewControlWebResourceRequestedEventArgs](/uwp/api/windows.web.ui.webviewcontrolwebresourcerequestedeventargs).

Diese Eigenschaft ist schreibgeschützt.

```js
var args = webResourceRequestedEventArgs.args;
var request = args.request;
```

#### Eigenschaftenwert
Geben Sie Folgendes **ein** :

