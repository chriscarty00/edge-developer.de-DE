---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2CreateCoreWebView2HostCompletedHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Host, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: 9c2b5568e6a276b07dc91bd639c730b2009aa9e5
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884281"
---
# 0.9.430-Interface-ICoreWebView2CreateCoreWebView2HostCompletedHandler 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2CreateCoreWebView2HostCompletedHandler
  : public IUnknown
```

Der Aufrufer implementiert diese Schnittstelle, um die über CreateCoreWebView2Host erstellte CoreWebView2Host zu empfangen.

## Zusammenfassung

 Member                        | Beschreibungen
--------------------------------|---------------------------------------------
[Invoke](#invoke) | Wird aufgerufen, um dem Implementierer den Fertigstellungsstatus und das Ergebnis des entsprechenden asynchronen Methodenaufrufs bereitzustellen.

## Member

#### Invoke 

Wird aufgerufen, um dem Implementierer den Fertigstellungsstatus und das Ergebnis des entsprechenden asynchronen Methodenaufrufs bereitzustellen.

> öffentlicher HRESULT- [Aufruf](#invoke)(HRESULT-Ergebnis,[ICoreWebView2Host](ICoreWebView2Host.md) * created_host)

