---
description: Einbetten von Webtechnologien (HTML, CSS und JavaScript) in ihre systemeigenen Anwendungen mit dem Microsoft Edge WebView2-Steuerelement
title: WebView2 Win32 C++ ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML, ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgs
ms.openlocfilehash: 056667b4ee1995763fee81c8d7a9be31496f7f3e
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/20/2020
ms.locfileid: "10886533"
---
# Schnittstellen ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgs 

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

```
interface ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgs
  : public IUnknown
```

Ereignis-args für das WebResourceResponseReceived-Ereignis.

## Zusammenfassung

 Member                        | Beschreibungen
--------------------------------|---------------------------------------------
[get_Request](#get_request) | Web-Ressourcen Anforderungsobjekt Alle Änderungen an diesem Objekt werden ignoriert.
[get_Response](#get_response) | Webressourcen-Antwortobjekt
[PopulateResponseContent](#populateresponsecontent) | Async-Methode, um den Inhaltsdatenstrom der Antwort anzufordern.

Enthält die Anforderung, während Sie gesendet wurde, und die Antwort, wie Sie empfangen wurde. Hinweis: um den Antwort Inhaltsdatenstrom abzurufen, rufen Sie zunächst PopulateResponseContent auf, und warten Sie, bis der asynchrone Aufruf abgeschlossen ist, da andernfalls das zurückgegebene Inhaltsdatenstrom-Objekt NULL ist.

## Member

#### get_Request 

Web-Ressourcen Anforderungsobjekt Alle Änderungen an diesem Objekt werden ignoriert.

> öffentliche HRESULT- [get_Request](#get_request)(ICoreWebView2WebResourceRequest * * Request)

#### get_Response 

Webressourcen-Antwortobjekt

> öffentliche HRESULT- [get_Response](#get_response)(ICoreWebView2WebResourceResponse * * Response)

Alle Änderungen an diesem Objekt werden ignoriert.

#### PopulateResponseContent 

Async-Methode, um den Inhaltsdatenstrom der Antwort anzufordern.

> Public HRESULT [PopulateResponseContent](#populateresponsecontent)([ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgsPopulateResponseContentCompletedHandler](icorewebview2experimentalwebresourceresponsereceivedeventargspopulateresponsecontentcompletedhandler.md) *-Handler)

```cpp
                    args->PopulateResponseContent(
                        Callback<
                            ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgsPopulateResponseContentCompletedHandler>(
                            [this, webResourceRequest, webResourceResponse](HRESULT result) {
                                std::wstring message =
                                    L"{ \"kind\": \"event\", \"name\": "
                                    L"\"WebResourceResponseReceived\", \"args\": {"
                                    L"\"request\": " +
                                    RequestToJsonString(webResourceRequest.get()) +
                                    L", "
                                    L"\"response\": " +
                                    ResponseToJsonString(webResourceResponse.get()) + L"}";

                                message +=
                                    WebViewPropertiesToJsonString(m_webviewEventSource.get());
                                message += L"}";
                                PostEventMessage(message);
                                return S_OK;
                            })
                            .Get());
```

