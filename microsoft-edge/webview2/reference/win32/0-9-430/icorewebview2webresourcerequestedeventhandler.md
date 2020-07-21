---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2WebResourceRequestedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Host, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: d35e21fde7788b1df5b201f8690196ecd0d82a34
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884092"
---
# 0.9.430-Interface-ICoreWebView2WebResourceRequestedEventHandler 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2WebResourceRequestedEventHandler
  : public IUnknown
```

Wird ausgelöst, wenn eine HTTP-Anforderung in der WebView erstellt wird.

## Zusammenfassung

 Member                        | Beschreibungen
--------------------------------|---------------------------------------------
[Invoke](#invoke) | Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.

Der Host kann Anforderung, Antwortheader und Antwortinhalt außer Kraft setzen.

## Member

#### Invoke 

Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.

> Public HRESULT [Invoke](#invoke)([ICoreWebView2](ICoreWebView2.md) * Sender;[ICoreWebView2WebResourceRequestedEventArgs](ICoreWebView2WebResourceRequestedEventArgs.md) * args)

