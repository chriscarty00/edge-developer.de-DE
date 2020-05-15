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
ms.openlocfilehash: 9210a4b70d0e2edf30cbaad906f57b360688dfe8
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653795"
---
# Microsoft. Web. WebView2. Core. CoreWebView2WebResourceRequestedEventArgs Klasse 

Namespace: Microsoft. Web. WebView2. Core \
Assembly: Microsoft. Web. WebView2. Core. dll

Ereignis-args für das WebResourceRequested-Ereignis.

## Zusammenfassung

 Member                        | Beschreibungen
--------------------------------|---------------------------------------------
[Anforderung](#request) | Die HTTP-Anforderung.
[ResourceContext](#resourcecontext) | Der Webressource-Anforderungskontext.
[Antwort](#response) | Die HTTP-Antwort.
[GetDeferral](#getdeferral) | Rufen Sie ein CoreWebView2Deferral-Objekt ab, und setzen Sie das Ereignis in einen verzögerten Zustand.

## Member

#### Anforderung 

Die HTTP-Anforderung.

> öffentliche HttpRequestMessage- [Anforderung](#request)

#### ResourceContext 

Der Webressource-Anforderungskontext.

> Public [CoreWebView2WebResourceContext](./namespace-microsoft-web-webview2-core.md) - [resourcecontext](#resourcecontext)

#### Antwort 

Die HTTP-Antwort.

> öffentliche HttpResponseMessage- [Antwort](#response)

#### GetDeferral 

Rufen Sie ein CoreWebView2Deferral-Objekt ab, und setzen Sie das Ereignis in einen verzögerten Zustand.

> Public [CoreWebView2Deferral](microsoft-web-webview2-core-corewebview2deferral.md) [getstundungal](#getdeferral)()

Sie können das CoreWebView2Deferral-Objekt verwenden, um die Netzwerkanforderung zu einem späteren Zeitpunkt abzuschließen.

