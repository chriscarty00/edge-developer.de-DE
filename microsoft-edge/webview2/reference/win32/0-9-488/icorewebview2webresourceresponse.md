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
ms.openlocfilehash: d6b51600479f47eebb09d5cff8fb096455fb1766
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653758"
---
# Schnittstellen ICoreWebView2WebResourceResponse 

```
interface ICoreWebView2WebResourceResponse
  : public IUnknown
```

Eine HTTP-Antwort, die mit dem WebResourceRequested-Ereignis verwendet wird.

## Zusammenfassung

 Member                        | Beschreibungen
--------------------------------|---------------------------------------------
[get_Content](#get_content) | HTTP-Antwortinhalt als Stream.
[get_Headers](#get_headers) | Überschriebene HTTP-Antwortheader.
[get_ReasonPhrase](#get_reasonphrase) | Der HTTP-Antwort Grund Ausdruck.
[get_StatusCode](#get_statuscode) | Der HTTP-Antwortstatuscode.
[put_Content](#put_content) | Festlegen der Content-Eigenschaft
[put_ReasonPhrase](#put_reasonphrase) | Festlegen der ReasonPhrase-Eigenschaft
[put_StatusCode](#put_statuscode) | Die Statuscode-Eigenschaft festlegen.

## Member

#### get_Content 

HTTP-Antwortinhalt als Stream.

> öffentliche HRESULT- [get_Content](#get_content)(IStream * *-Inhalt)

Datenstrom muss alle Inhaltsdaten zur Verfügung stehen, wenn die WebResourceRequested-Ereignisverzögerung dieser Antwort abgeschlossen ist. Stream sollte agil sein oder aus einem Hintergrundthread erstellt werden, um eine Leistungsbeeinträchtigung des UI-Threads zu verhindern. NULL bedeutet keine Inhaltsdaten. Die IStream-Semantik wird angewendet (Rückgabe S_OK zum Lesen von anrufen, bis alle Daten erschöpft sind)

#### get_Headers 

Überschriebene HTTP-Antwortheader.

> öffentliche HRESULT- [get_Headers](#get_headers)([ICoreWebView2HttpResponseHeaders](icorewebview2httpresponseheaders.md) * *-Header)

#### get_ReasonPhrase 

Der HTTP-Antwort Grund Ausdruck.

> Public HRESULT [get_ReasonPhrase](#get_reasonphrase)(LPWSTR * ReasonPhrase)

#### get_StatusCode 

Der HTTP-Antwortstatuscode.

> Public HRESULT [get_StatusCode](#get_statuscode)(int * Statuscode)

#### put_Content 

Festlegen der Content-Eigenschaft

> öffentliche HRESULT- [put_Content](#put_content)(IStream *-Inhalt)

#### put_ReasonPhrase 

Festlegen der ReasonPhrase-Eigenschaft

> Public HRESULT [put_ReasonPhrase](#put_reasonphrase)(LPCWSTR ReasonPhrase)

#### put_StatusCode 

Die Statuscode-Eigenschaft festlegen.

> Public HRESULT [put_StatusCode](#put_statuscode)(int Statuscode)

