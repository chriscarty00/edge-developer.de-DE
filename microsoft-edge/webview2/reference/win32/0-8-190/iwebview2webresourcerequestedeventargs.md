---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: Microsoft Edge-WebView2 für Win32-apps
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/09/2019
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge
ms.openlocfilehash: 899a6f50db1d77f3f24524c5ccec139dcbdbcaf9
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653777"
---
# Schnittstellen IWebView2WebResourceRequestedEventArgs 

> [!NOTE]
> Diese Schnittstelle kann nach der SDK-Version 0.8.355 geändert oder für Versionen nicht verfügbar sein. Die neueste API-Referenz finden Sie unter [Referenz](../../../webview2-api-reference.md) .

```
interface IWebView2WebResourceRequestedEventArgs
  : public IUnknown
```

Ereignis-args für das WebResourceRequested-Ereignis.

## Zusammenfassung

 Member                        | Beschreibungen
--------------------------------|---------------------------------------------
[get_Request](#get_request) | Die HTTP-Anforderung.
[get_Response](#get_response) | Die HTTP-Antwort.
[put_Response](#put_response) | Festlegen der Response-Eigenschaft
[GetDeferral](#getdeferral) | Rufen Sie ein [IWebView2Deferral](IWebView2Deferral.md) -Objekt ab, und setzen Sie das Ereignis in einen verzögerten Zustand.

## Member

#### get_Request 

Die HTTP-Anforderung.

> öffentliche HRESULT- [get_Request](#get_request)([IWebView2WebResourceRequest](IWebView2WebResourceRequest.md) * * Request)

#### get_Response 

Die HTTP-Antwort.

> öffentliche HRESULT- [get_Response](#get_response)([IWebView2WebResourceResponse](IWebView2WebResourceResponse.md) * * Response)

#### put_Response 

Festlegen der Response-Eigenschaft

> öffentliche HRESULT- [put_Response](#put_response)([IWebView2WebResourceResponse](IWebView2WebResourceResponse.md) * Response)

#### GetDeferral 

Rufen Sie ein [IWebView2Deferral](IWebView2Deferral.md) -Objekt ab, und setzen Sie das Ereignis in einen verzögerten Zustand.

> öffentliche HRESULT [getstundung](#getdeferral)([IWebView2Deferral](IWebView2Deferral.md) * * Stundung)

Sie können das [IWebView2Deferral](IWebView2Deferral.md) -Objekt verwenden, um die Netzwerkanforderung zu einem späteren Zeitpunkt abzuschließen.

