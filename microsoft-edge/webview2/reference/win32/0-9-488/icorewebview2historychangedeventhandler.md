---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: Microsoft Edge-WebView2 für Win32-apps
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/07/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: 42e3767ad2a42a1d9e9931efa8a4fe844ea80dba
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653764"
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

