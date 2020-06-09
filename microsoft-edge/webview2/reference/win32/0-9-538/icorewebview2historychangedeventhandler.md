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
ms.openlocfilehash: 0f14f8d281d4729d797eb5271a19cff67becafab
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698868"
---
# Schnittstellen ICoreWebView2HistoryChangedEventHandler 

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

> öffentlicher HRESULT- [Aufruf](#invoke)([ICoreWebView2](icorewebview2.md) * WebView, IUnknown * args)

