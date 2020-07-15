---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.9.515-Microsoft. Web. WebView2. Core. EdgeNotFoundException
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: db4a903ca430541fa9edec9d953bf28531f7c0a4
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/15/2020
ms.locfileid: "10879604"
---
# 0.9.515-Microsoft. Web. WebView2. Core. EdgeNotFoundException Klasse 

> [!NOTE]
> Dieser Verweis kann für Versionen nach der SDK-Version 0.9.515 geändert oder nicht mehr zur Verfügung stehen. Die neueste API-Referenz finden Sie in der [WebView2-API-Referenz](../../../webview2-api-reference.md) .

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

