---
description: Enthält verweisende Informationen zur Navigation
title: NavigationEventWithReferrer-Objekt
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/10/2020
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, Windows 10-apps, UWP, Edge
ms.openlocfilehash: 72c8a213f632e9e74145de9c34b949adf074cd22
ms.sourcegitcommit: 037a2d62333691104c9accb4862968f80a3465a2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/18/2020
ms.locfileid: "10752127"
---
# NavigationEventWithReferrer-Objekt  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

Ein Objekt, das ein Ereignis darstellt, das ausgelöst wird, wenn die Navigation initiiert wird und die Navigation einen Referer enthält.  

## Eigenschaften  

### Referer

Der URI (Uniform Resource Identifier) der Seite im [WebView](../webview.md) , der die Navigation anfordert.  

Diese Eigenschaft ist schreibgeschützt.  

#### Eigenschaftenwert  

Geben Sie Folgendes ein: **DOM**  

```javascript
var referer = NavigationEventWithReferrer.referer;
```  

### Uri  

Der URI (Uniform Resource Identifier) des Ziels der Navigation.  

Diese Eigenschaft ist schreibgeschützt.  

```javascript
var uri = NavigationEventWithReferrer.uri;
```  

#### Eigenschaftenwert  

Geben Sie Folgendes ein: **DOM**  
