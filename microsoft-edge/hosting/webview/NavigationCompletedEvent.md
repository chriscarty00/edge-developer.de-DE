---
description: Enthält Informationen zur abgeschlossenen WebView-Navigation
title: NavigationCompletedEvent-Objekt
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/10/2020
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, Windows 10-apps, UWP, Edge
ms.openlocfilehash: eb5727ab59dbaf056f05ab4b19450c70f85d595f
ms.sourcegitcommit: 037a2d62333691104c9accb4862968f80a3465a2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/18/2020
ms.locfileid: "10752138"
---
# NavigationCompletedEvent-Objekt  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

Ein Objekt, das ein Ereignis darstellt, das ausgelöst wird, wenn die [WebView](../webview.md) das Laden des aktuellen Inhalts durchgeführt hat oder die Navigation fehlgeschlagen ist.  

## Eigenschaften  

### Uri  

Der Uniform Resource Identifier (URI) der Navigation.  

Diese Eigenschaft ist schreibgeschützt.  

```javascript
var uri = NavigationCompletedEvent.uri;
```  

#### Eigenschaftenwert  

Geben Sie Folgendes ein: **DOM**  

### issuccess  

Ruft einen Wert ab, der angibt, ob die Navigation erfolgreich abgeschlossen wurde.  

Diese Eigenschaft ist schreibgeschützt.  

```javascript
var isSuccess = NavigationCompletedEvent.isSuccess;
```  

#### Eigenschaftenwert  

Typ: **boolescher Wert**  

### webErrorStatus  

Wenn die Navigation nicht erfolgreich war, Ruft einen Wert ab, der angibt, warum.  

Diese Eigenschaft ist schreibgeschützt.  

```javascript
var webErrorStatus = NavigationCompletedEvent.webErrorStatus;
```  

#### Eigenschaftenwert  

Typ: **unsigned long**  
