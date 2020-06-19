---
description: Ein Ereignis, das ausgelöst wird, wenn eine HTTP-Anforderung durchgeführt wird.
title: WebResourceRequestedEvent-Objekt
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/10/2020
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, Windows 10-apps, UWP, Edge
ms.openlocfilehash: 3d2bb54cc5d60aec5391f0e3fdd427c8ba8a3dab
ms.sourcegitcommit: 037a2d62333691104c9accb4862968f80a3465a2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/18/2020
ms.locfileid: "10751982"
---
# WebResourceRequestedEvent-Objekt  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

Ein Ereignis, das ausgelöst wird, wenn eine HTTP-Anforderung durchgeführt wird.  

## Eigenschaften  

### args  

Informationen zur Ressourcenanforderung.  Dies ist ein [Windows. Web. UI. WebViewControlWebResourceRequestedEventArgs](/uwp/api/windows.web.ui.webviewcontrolwebresourcerequestedeventargs).  

Diese Eigenschaft ist schreibgeschützt.  

```javascript
var args = webResourceRequestedEventArgs.args;
var request = args.request;
```  

#### Eigenschaftenwert  

Geben Sie Folgendes **ein** :  
