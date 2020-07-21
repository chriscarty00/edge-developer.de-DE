---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.8.355-WebView2 Win32 C++ IWebView2WebResourceResponse
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge
ms.openlocfilehash: 82c94869a84165de4c3b8d09937d6ea5d1f79256
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885688"
---
# 0.8.355-Interface-IWebView2WebResourceResponse 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2WebResourceResponse
  : public IUnknown
```

Eine HTTP-Antwort, die mit dem WebResourceRequested-Ereignis verwendet wird.

## Zusammenfassung

 Member                        | Beschreibungen
--------------------------------|---------------------------------------------
[get_Content](#get_content) | HTTP-Antwortinhalt als Stream.
[put_Content](#put_content) | Festlegen der Content-Eigenschaft
[get_Headers](#get_headers) | Überschriebene HTTP-Antwortheader.
[get_StatusCode](#get_statuscode) | Der HTTP-Antwortstatuscode.
[put_StatusCode](#put_statuscode) | Die Statuscode-Eigenschaft festlegen.
[get_ReasonPhrase](#get_reasonphrase) | Der HTTP-Antwort Grund Ausdruck.
[put_ReasonPhrase](#put_reasonphrase) | Festlegen der ReasonPhrase-Eigenschaft

## Member

#### get_Content 

HTTP-Antwortinhalt als Stream.

> öffentliche HRESULT- [get_Content](#get_content)(IStream * *-Inhalt)

Datenstrom muss alle Inhaltsdaten zur Verfügung stehen, wenn die WebResourceRequested-Ereignisverzögerung dieser Antwort abgeschlossen ist. Stream sollte agil sein oder aus einem Hintergrundthread erstellt werden, um eine Leistungsbeeinträchtigung des UI-Threads zu verhindern. NULL bedeutet keine Inhaltsdaten. Die IStream-Semantik wird angewendet (Rückgabe S_OK zum Lesen von anrufen, bis alle Daten erschöpft sind)

#### put_Content 

Festlegen der Content-Eigenschaft

> öffentliche HRESULT- [put_Content](#put_content)(IStream *-Inhalt)

#### get_Headers 

Überschriebene HTTP-Antwortheader.

> öffentliche HRESULT- [get_Headers](#get_headers)([IWebView2HttpResponseHeaders](IWebView2HttpResponseHeaders.md) * *-Header)

#### get_StatusCode 

Der HTTP-Antwortstatuscode.

> Public HRESULT [get_StatusCode](#get_statuscode)(int * Statuscode)

#### put_StatusCode 

Die Statuscode-Eigenschaft festlegen.

> Public HRESULT [put_StatusCode](#put_statuscode)(int Statuscode)

#### get_ReasonPhrase 

Der HTTP-Antwort Grund Ausdruck.

> Public HRESULT [get_ReasonPhrase](#get_reasonphrase)(LPWSTR * ReasonPhrase)

#### put_ReasonPhrase 

Festlegen der ReasonPhrase-Eigenschaft

> Public HRESULT [put_ReasonPhrase](#put_reasonphrase)(LPCWSTR ReasonPhrase)

