---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: Microsoft Edge-WebView2 für Win32-apps
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/05/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: 7f30bda4deb0811748c65880fcc49c21bc39a732
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/08/2020
ms.locfileid: "10697294"
---
# Microsoft. Web. WebView2. Core. EdgeNotFoundException Klasse 

> [!NOTE]
> Dieser Verweis kann für Versionen nach der SDK-Version 0.9.515 geändert oder nicht mehr zur Verfügung stehen. Die neueste API-Referenz finden Sie in der [WebView2-API-Referenz](../../../webview2-api-reference.md) .

Namespace: Microsoft. Web. WebView2. Core \
Assembly: Microsoft. Web. WebView2. Core. dll

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

