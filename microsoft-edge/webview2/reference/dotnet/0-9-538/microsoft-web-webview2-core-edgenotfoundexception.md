---
description: Einbetten von Webtechnologien (HTML, CSS und JavaScript) in ihre systemeigenen Anwendungen mit dem Microsoft Edge WebView2-Steuerelement
title: 0.9.579-Microsoft. Web. WebView2. Core. EdgeNotFoundException
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, DotNet, WPF, WinForms, APP, Edge, CoreWebView2, CoreWebView2Controller, Browser Control, Edge HTML, Microsoft. Web. WebView2. Core. EdgeNotFoundException
ms.openlocfilehash: b4dc30ff741702d03796cb40e6ea6367ffdd0fc0
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/10/2020
ms.locfileid: "11010103"
---
# 0.9.579-Microsoft. Web. WebView2. Core. EdgeNotFoundException Klasse 

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

