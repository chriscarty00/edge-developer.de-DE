---
description: Gibt an, dass die WebView versucht, eine nicht unterstützte Datei herunterzuladen.
title: UnviewableContentIdentifiedEvent-Objekt
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/25/2018
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, Windows 10-apps, UWP, Edge
ms.openlocfilehash: cec85ca2d5458a05cfd88210907523f25fb4af95
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10566692"
---
# UnviewableContentIdentifiedEvent-Objekt

Gibt an, dass die [WebView](../webview.md) versucht, zu einer Datei mit einem nicht unterstützten Inhaltstyp zu navigieren. 

## Eigenschaften

### MediaType

Ruft den Inhaltstyp des nicht sichtbar-Inhalts ab.

Diese Eigenschaft ist schreibgeschützt

```js
var mediaType = UnviewableContentIdentifiedEvent.mediaType;
```

#### Eigenschaftenwert
Geben Sie Folgendes ein: **DOM**

### Referer

Der URI (Uniform Resource Identifier) der Seite im [WebView](../webview.md) , der die Navigation anfordert.

Diese Eigenschaft ist schreibgeschützt.


```js
var referer = NavigationEventWithReferrer.referer;
```

#### Eigenschaftenwert
Geben Sie Folgendes ein: **DOM**

### Uri

Der URI (Uniform Resource Identifier) des Ziels der Navigation.

Diese Eigenschaft ist schreibgeschützt.

```js
var uri = NavigationEventWithReferrer.uri;
```

#### Eigenschaftenwert
Geben Sie Folgendes ein: **DOM**
