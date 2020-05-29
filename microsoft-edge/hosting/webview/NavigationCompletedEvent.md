---
description: Enthält Informationen zur abgeschlossenen WebView-Navigation
title: NavigationCompletedEvent-Objekt
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/26/2018
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, Windows 10-apps, UWP, Edge
ms.openlocfilehash: 11974f0c66d48569ee63c592bdd3b0153db075b1
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10567166"
---
# NavigationCompletedEvent-Objekt

Ein Objekt, das ein Ereignis darstellt, das ausgelöst wird, wenn die [WebView](../webview.md) das Laden des aktuellen Inhalts durchgeführt hat oder die Navigation fehlgeschlagen ist.

## Eigenschaften
    
### Uri

Der Uniform Resource Identifier (URI) der Navigation.

Diese Eigenschaft ist schreibgeschützt.

```js
var uri = NavigationCompletedEvent.uri;
```

#### Eigenschaftenwert
Geben Sie Folgendes ein: **DOM**

### issuccess

Ruft einen Wert ab, der angibt, ob die Navigation erfolgreich abgeschlossen wurde.

Diese Eigenschaft ist schreibgeschützt

```js
var isSuccess = NavigationCompletedEvent.isSuccess;
```

#### Eigenschaftenwert
Typ: **boolescher Wert**

### webErrorStatus

Wenn die Navigation nicht erfolgreich war, Ruft einen Wert ab, der angibt, warum.

Diese Eigenschaft ist schreibgeschützt

```js
var webErrorStatus = NavigationCompletedEvent.webErrorStatus;
```

#### Eigenschaftenwert
Typ: **unsigned long**
