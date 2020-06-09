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
ms.openlocfilehash: 072ce10e7ac1f34238278366c3e8799a3268cb0b
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/08/2020
ms.locfileid: "10697532"
---
# Microsoft. Web. WebView2. Core. CoreWebView2WebResourceRequestedEventArgs Klasse 

> [!NOTE]
> Dieser Verweis kann für Versionen nach der SDK-Version 0.9.515 geändert oder nicht mehr zur Verfügung stehen. Die neueste API-Referenz finden Sie in der [WebView2-API-Referenz](../../../webview2-api-reference.md) .

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

