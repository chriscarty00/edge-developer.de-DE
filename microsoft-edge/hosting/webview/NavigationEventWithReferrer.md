---
description: Enthält verweisende Informationen zur Navigation
title: NavigationEventWithReferrer-Objekt
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/22/2018
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, Windows 10-apps, UWP, Edge
ms.openlocfilehash: b11f60724387d996d0a730965602b5ead6a84145
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10567160"
---
# NavigationEventWithReferrer-Objekt

Ein Objekt, das ein Ereignis darstellt, das ausgelöst wird, wenn die Navigation initiiert wird und die Navigation einen Referer enthält.

## Eigenschaften

### Referer

Der URI (Uniform Resource Identifier) der Seite im [WebView](../webview.md) , der die Navigation anfordert.

Diese Eigenschaft ist schreibgeschützt.

#### Eigenschaftenwert
Geben Sie Folgendes ein: **DOM**


```js
var referer = NavigationEventWithReferrer.referer;
```

### Uri

Der URI (Uniform Resource Identifier) des Ziels der Navigation.

Diese Eigenschaft ist schreibgeschützt.

```js
var uri = NavigationEventWithReferrer.uri;
```

#### Eigenschaftenwert
Geben Sie Folgendes ein: **DOM**
