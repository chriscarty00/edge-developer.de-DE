---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.9.515-Microsoft. Web. WebView2. Core. EdgeNotFoundException
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: fc65d857f11a77a1d3629d40266f0453acadaa7b
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/20/2020
ms.locfileid: "10886311"
---
# 0.9.515-Microsoft. Web. WebView2. Core. EdgeNotFoundException Klasse 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

Namespace: Microsoft. Web. WebView2. Core \
Assembly: Microsoft.Web.WebView2.Core.dll

```
class Microsoft.Web.WebView2.Core.EdgeNotFoundException
  : public Exception
```

Diese Ausnahme wird ausgelöst, wenn eine Edge-Installation fehlt.

## Zusammenfassung

 Member                        | Beschreibungen
--------------------------------|---------------------------------------------
[EdgeNotFoundException](#edgenotfoundexception) | Initialisiert eine neue Instanz der EdgeNotFoundException-Klasse.
[EdgeNotFoundException](#edgenotfoundexception) | Initialisiert eine neue Instanz der EdgeNotFoundException-Klasse mit einem Verweis auf die innere Ausnahme, die diese Ausnahme ausgelöst hat.
[EdgeNotFoundException](#edgenotfoundexception) | Initialisiert eine neue Instanz der EdgeNotFoundException-Klasse mit einer angegebenen Fehlermeldung.
[EdgeNotFoundException](#edgenotfoundexception) | Initialisiert eine neue Instanz der EdgeNotFoundException-Klasse mit einer angegebenen Fehlermeldung und einem Verweis auf die innere Ausnahme, die diese Ausnahme ausgelöst hat.

## Member

#### EdgeNotFoundException 

Initialisiert eine neue Instanz der EdgeNotFoundException-Klasse.

> Public [EdgeNotFoundException](#edgenotfoundexception)()

#### EdgeNotFoundException 

Initialisiert eine neue Instanz der EdgeNotFoundException-Klasse mit einem Verweis auf die innere Ausnahme, die diese Ausnahme ausgelöst hat.

> Public [EdgeNotFoundException](#edgenotfoundexception)(innere Ausnahme)

##### Parameter
* `inner` Die Ausnahme, die die aktuelle Ausnahme verursacht hat.

#### EdgeNotFoundException 

Initialisiert eine neue Instanz der EdgeNotFoundException-Klasse mit einer angegebenen Fehlermeldung.

> öffentliche [EdgeNotFoundException](#edgenotfoundexception)(Zeichenfolgennachricht)

##### Parameter
* `message` Die Fehlermeldung, in der der Grund für die Ausnahme erläutert wird.

#### EdgeNotFoundException 

Initialisiert eine neue Instanz der EdgeNotFoundException-Klasse mit einer angegebenen Fehlermeldung und einem Verweis auf die innere Ausnahme, die diese Ausnahme ausgelöst hat.

> Public [EdgeNotFoundException](#edgenotfoundexception)(String-Nachricht, innere Ausnahme)

##### Parameter
* `message` Die Fehlermeldung, in der der Grund für die Ausnahme erläutert wird. 

* `inner` Die Ausnahme, die die aktuelle Ausnahme verursacht hat.

