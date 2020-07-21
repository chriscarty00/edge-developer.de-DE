---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2HistoryChangedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Host, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: e47ca26475ba1b59fa4ea8c87a7aada0d8d6695f
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884134"
---
# 0.9.430-Interface-ICoreWebView2HistoryChangedEventHandler 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2HistoryChangedEventHandler
  : public IUnknown
```

Der Aufrufer implementiert diese Schnittstelle, um das Ereignis "History" zu empfangen.

## Zusammenfassung

 Member                        | Beschreibungen
--------------------------------|---------------------------------------------
[Invoke](#invoke) | Es gibt keine Ereignisargumente, und der args-Parameter ist NULL.

## Member

#### Invoke 

Es gibt keine Ereignisargumente, und der args-Parameter ist NULL.

> öffentlicher HRESULT- [Aufruf](#invoke)([ICoreWebView2](ICoreWebView2.md) * WebView, IUnknown * args)

