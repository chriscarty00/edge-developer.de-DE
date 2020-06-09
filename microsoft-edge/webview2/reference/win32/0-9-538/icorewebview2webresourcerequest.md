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
ms.openlocfilehash: c715a195a52d95e91095e006c71e50de46dc05e4
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698860"
---
# Schnittstellen ICoreWebView2WebResourceRequest 

```
interface ICoreWebView2WebResourceRequest
  : public IUnknown
```

Eine HTTP-Anforderung für das WebResourceRequested-Ereignis.

## Zusammenfassung

 Member                        | Beschreibungen
--------------------------------|---------------------------------------------
[get_Content](#get_content) | Der HTTP-Request-Nachrichtentext als Stream.
[get_Headers](#get_headers) | Die änderbaren HTTP-Anforderungsheader.
[get_Method](#get_method) | Die http-Anforderungsmethode.
[get_Uri](#get_uri) | Der Anforderungs-URI.
[put_Content](#put_content) | Festlegen der Content-Eigenschaft
[put_Method](#put_method) | Festlegen der Method-Eigenschaft
[put_Uri](#put_uri) | Die URI-Eigenschaft festlegen.

## Member

#### get_Content 

Der HTTP-Request-Nachrichtentext als Stream.

> öffentliche HRESULT- [get_Content](#get_content)(IStream * *-Inhalt)

Post-Daten wären hier. Wenn ein Datenstrom festgesetzt wird, der den Nachrichtentext überschreibt, muss der Datenstrom alle Inhaltsdaten aufweisen, bis die WebResourceRequested-Ereignisverzögerung dieser Antwort abgeschlossen ist. Stream sollte agil sein oder aus einem background-STA erstellt werden, um eine Leistungsbeeinträchtigung des UI-Threads zu verhindern. NULL bedeutet keine Inhaltsdaten. Die IStream-Semantik wird angewendet (Rückgabe S_OK zum Lesen von anrufen, bis alle Daten erschöpft sind)

#### get_Headers 

Die änderbaren HTTP-Anforderungsheader.

> öffentliche HRESULT- [get_Headers](#get_headers)([ICoreWebView2HttpRequestHeaders](icorewebview2httprequestheaders.md) * *-Header)

#### get_Method 

Die http-Anforderungsmethode.

> öffentliche HRESULT- [get_Method](#get_method)(LPWSTR *-Methode)

#### get_Uri 

Der Anforderungs-URI.

> Public HRESULT [get_Uri](#get_uri)(LPWSTR * URI)

#### put_Content 

Festlegen der Content-Eigenschaft

> öffentliche HRESULT- [put_Content](#put_content)(IStream *-Inhalt)

#### put_Method 

Festlegen der Method-Eigenschaft

> Public HRESULT [put_Method](#put_method)(LPCWSTR-Methode)

#### put_Uri 

Die URI-Eigenschaft festlegen.

> öffentliche HRESULT- [put_Uri](#put_uri)(LPCWSTR-URI)

