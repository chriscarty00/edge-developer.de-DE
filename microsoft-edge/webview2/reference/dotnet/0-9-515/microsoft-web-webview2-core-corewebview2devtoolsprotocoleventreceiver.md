---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2DevToolsProtocolEventReceiver
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: 1982c6926d2ed8805433efc4d46ff6f3cac691ce
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885058"
---
# 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2DevToolsProtocolEventReceiver Klasse 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

Namespace: Microsoft. Web. WebView2. Core \
Assembly: Microsoft.Web.WebView2.Core.dll

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

