---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: Microsoft Edge-WebView2 für Win32-apps
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/12/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: 23ee363fd90416d07c76644879a5f4b6cc2acabe
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/14/2020
ms.locfileid: "10654027"
---
# Microsoft. Web. WebView2. Core. CoreWebView2DevToolsProtocolEventReceiver Klasse 

Namespace: Microsoft. Web. WebView2. Core \
Assembly: Microsoft. Web. WebView2. Core. dll

Ein Empfänger wird für ein bestimmtes devtools-Protokollereignis erstellt und ermöglicht Ihnen, dieses Ereignis zu abonnieren und abzubestellen.

## Zusammenfassung

 Member                        | Beschreibungen
--------------------------------|---------------------------------------------
[DevToolsProtocolEventReceived](#devtoolsprotocoleventreceived) | Abonnieren eines DevToolsProtocol-Ereignisses

Abgerufen aus dem WebView-Objekt über GetDevToolsProtocolEventReceiver.

## Member

#### DevToolsProtocolEventReceived 

Abonnieren eines DevToolsProtocol-Ereignisses

> public event EventHandler< [CoreWebView2DevToolsProtocolEventReceivedEventArgs](microsoft-web-webview2-core-corewebview2devtoolsprotocoleventreceivedeventargs.md)  >  [DevToolsProtocolEventReceived](#devtoolsprotocoleventreceived)

Die Invoke-Methode des Handlers wird aufgerufen, wenn das entsprechende DevToolsProtocol-Ereignis ausgelöst wird. Invoke wird mit dem Ereignis args-Objekt aufgerufen, das das Parameter Objekt des devtools-Protokollereignisses als JSON-Zeichenfolge enthält.

