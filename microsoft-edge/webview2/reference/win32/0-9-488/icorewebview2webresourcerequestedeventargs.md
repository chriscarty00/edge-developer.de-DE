---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2WebResourceRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: dec8bfb2927e823c85f472bd2cab0800ff5f00c7
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/20/2020
ms.locfileid: "10883749"
---
# 0.9.515-Interface-ICoreWebView2WebResourceRequestedEventArgs 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2WebResourceRequestedEventArgs
  : public IUnknown
```

Ereignis-args für das WebResourceRequested-Ereignis.

## Zusammenfassung

 Member                        | Beschreibungen
--------------------------------|---------------------------------------------
[get_Request](#get_request) | Die HTTP-Anforderung.
[get_ResourceContext](#get_resourcecontext) | Der Webressource-Anforderungskontext.
[get_Response](#get_response) | Die HTTP-Antwort.
[GetDeferral](#getdeferral) | Rufen Sie ein [ICoreWebView2Deferral](icorewebview2deferral.md) -Objekt ab, und setzen Sie das Ereignis in einen verzögerten Zustand.
[put_Response](#put_response) | Festlegen der Response-Eigenschaft

## Member

#### get_Request 

Die HTTP-Anforderung.

> öffentliche HRESULT- [get_Request](#get_request)([ICoreWebView2WebResourceRequest](icorewebview2webresourcerequest.md) * * Request)

#### get_ResourceContext 

Der Webressource-Anforderungskontext.

> öffentliche HRESULT- [get_ResourceContext](#get_resourcecontext)(COREWEBVIEW2_WEB_RESOURCE_CONTEXT *-Kontext)

#### get_Response 

Die HTTP-Antwort.

> öffentliche HRESULT- [get_Response](#get_response)([ICoreWebView2WebResourceResponse](icorewebview2webresourceresponse.md) * * Response)

#### GetDeferral 

Rufen Sie ein [ICoreWebView2Deferral](icorewebview2deferral.md) -Objekt ab, und setzen Sie das Ereignis in einen verzögerten Zustand.

> öffentliche HRESULT [getstundung](#getdeferral)([ICoreWebView2Deferral](icorewebview2deferral.md) * * Stundung)

Sie können das [ICoreWebView2Deferral](icorewebview2deferral.md) -Objekt verwenden, um die Netzwerkanforderung zu einem späteren Zeitpunkt abzuschließen.

#### put_Response 

Festlegen der Response-Eigenschaft

> öffentliche HRESULT- [put_Response](#put_response)([ICoreWebView2WebResourceResponse](icorewebview2webresourceresponse.md) * Response)

