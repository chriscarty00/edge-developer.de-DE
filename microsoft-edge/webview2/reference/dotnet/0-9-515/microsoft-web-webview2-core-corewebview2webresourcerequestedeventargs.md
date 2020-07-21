---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2WebResourceRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: 656510998879e77c2e7797c700dacc5966299210
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884652"
---
# 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2WebResourceRequestedEventArgs Klasse 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

Namespace: Microsoft. Web. WebView2. Core \
Assembly: Microsoft.Web.WebView2.Core.dll

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

