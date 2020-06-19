---
description: Gibt an, dass die WebView versucht, eine nicht unterstützte Datei herunterzuladen.
title: UnviewableContentIdentifiedEvent-Objekt
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/10/2020
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, Windows 10-apps, UWP, Edge
ms.openlocfilehash: 0179522f3eaf0813531084eb996ee9d392e8249d
ms.sourcegitcommit: 037a2d62333691104c9accb4862968f80a3465a2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/18/2020
ms.locfileid: "10752013"
---
# UnviewableContentIdentifiedEvent-Objekt  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

Gibt an, dass die [WebView](../webview.md) versucht, zu einer Datei mit einem nicht unterstützten Inhaltstyp zu navigieren.  

## Eigenschaften  

### MediaType  

Ruft den Inhaltstyp des nicht sichtbar-Inhalts ab.  

Diese Eigenschaft ist schreibgeschützt  

```javascript
var mediaType = UnviewableContentIdentifiedEvent.mediaType;
```  

#### Eigenschaftenwert  

Geben Sie Folgendes ein: **DOM**  

### Referer  

Der URI (Uniform Resource Identifier) der Seite im [WebView](../webview.md) , der die Navigation anfordert.  

Diese Eigenschaft ist schreibgeschützt.  

```javascript
var referer = NavigationEventWithReferrer.referer;
```  

#### Eigenschaftenwert  

Geben Sie Folgendes ein: **DOM**  

### Uri  

Der URI (Uniform Resource Identifier) des Ziels der Navigation.  

Diese Eigenschaft ist schreibgeschützt.  

```javascript
var uri = NavigationEventWithReferrer.uri;
```  

#### Eigenschaftenwert  

Geben Sie Folgendes ein: **DOM**  
