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
ms.openlocfilehash: 69bf9eeae4b6736ac6df6ddaa9594b7438cbf58c
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653778"
---
# Schnittstellen IWebView2WebResourceRequest 

> [!NOTE]
> Diese Schnittstelle kann nach der SDK-Version 0.8.355 geändert oder für Versionen nicht verfügbar sein. Die neueste API-Referenz finden Sie unter [Referenz](../../../webview2-api-reference.md) .

```
interface IWebView2WebResourceRequest
  : public IUnknown
```

Eine HTTP-Anforderung für das WebResourceRequested-Ereignis.

## Zusammenfassung

 Member                        | Beschreibungen
--------------------------------|---------------------------------------------
[get_Uri](#get_uri) | Der Anforderungs-URI.
[put_Uri](#put_uri) | Die URI-Eigenschaft festlegen.
[get_Method](#get_method) | Die http-Anforderungsmethode.
[put_Method](#put_method) | Festlegen der Method-Eigenschaft
[get_Content](#get_content) | Der HTTP-Request-Nachrichtentext als Stream.
[put_Content](#put_content) | Festlegen der Content-Eigenschaft
[get_Headers](#get_headers) | Die änderbaren HTTP-Anforderungsheader.

## Member

#### get_Uri 

Der Anforderungs-URI.

> Public HRESULT [get_Uri](#get_uri)(LPWSTR * URI)

#### put_Uri 

Die URI-Eigenschaft festlegen.

> öffentliche HRESULT- [put_Uri](#put_uri)(LPCWSTR-URI)

#### get_Method 

Die http-Anforderungsmethode.

> öffentliche HRESULT- [get_Method](#get_method)(LPWSTR *-Methode)

#### put_Method 

Festlegen der Method-Eigenschaft

> Public HRESULT [put_Method](#put_method)(LPCWSTR-Methode)

#### get_Content 

Der HTTP-Request-Nachrichtentext als Stream.

> öffentliche HRESULT- [get_Content](#get_content)(IStream * *-Inhalt)

Post-Daten wären hier. Wenn ein Datenstrom festgesetzt wird, der den Nachrichtentext überschreibt, muss der Datenstrom alle Inhaltsdaten aufweisen, bis die WebResourceRequested-Ereignisverzögerung dieser Antwort abgeschlossen ist. Stream sollte agil sein oder aus einem background-STA erstellt werden, um eine Leistungsbeeinträchtigung des UI-Threads zu verhindern. NULL bedeutet keine Inhaltsdaten. Die IStream-Semantik wird angewendet (Rückgabe S_OK zum Lesen von anrufen, bis alle Daten erschöpft sind)

#### put_Content 

Festlegen der Content-Eigenschaft

> öffentliche HRESULT- [put_Content](#put_content)(IStream *-Inhalt)

#### get_Headers 

Die änderbaren HTTP-Anforderungsheader.

> öffentliche HRESULT- [get_Headers](#get_headers)([IWebView2HttpRequestHeaders](IWebView2HttpRequestHeaders.md) * *-Header)

