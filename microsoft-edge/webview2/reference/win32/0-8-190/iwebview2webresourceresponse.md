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
ms.openlocfilehash: ad3f4e5e95b0309628644f17e5d647ab6d4af658
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653766"
---
# Schnittstellen IWebView2WebResourceResponse 

> [!NOTE]
> Diese Schnittstelle kann nach der SDK-Version 0.8.355 geändert oder für Versionen nicht verfügbar sein. Die neueste API-Referenz finden Sie unter [Referenz](../../../webview2-api-reference.md) .

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

