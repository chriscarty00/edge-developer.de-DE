---
description: Einbetten von Webtechnologien (HTML, CSS und JavaScript) in ihre systemeigenen Anwendungen mit dem Microsoft Edge WebView2-Steuerelement
title: 0.9.579-WebView2 Win32 C++ ICoreWebView2Experimental
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML, ICoreWebView2Experimental
ms.openlocfilehash: 01bea6a6f89c61e34fe03af6007bee359770fb54
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011146"
---
# 0.9.579-Interface-ICoreWebView2Experimental 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

```
interface ICoreWebView2Experimental
  : public IUnknown
```

## Zusammenfassung

 Member                        | Beschreibungen
--------------------------------|---------------------------------------------
[add_WebResourceResponseReceived](#add_webresourceresponsereceived) | Fügen Sie einen Ereignishandler für das WebResourceResponseReceived-Ereignis hinzu.
[remove_WebResourceResponseReceived](#remove_webresourceresponsereceived) | Entfernt den zuvor mit add_WebResourceResponseReceived hinzugefügten WebResourceResponseReceived-Ereignishandler.

## Member

#### add_WebResourceResponseReceived 

Fügen Sie einen Ereignishandler für das WebResourceResponseReceived-Ereignis hinzu.

> Public HRESULT [add_WebResourceResponseReceived](#add_webresourceresponsereceived)([ICoreWebView2ExperimentalWebResourceResponseReceivedEventHandler](icorewebview2experimentalwebresourceresponsereceivedeventhandler.md) * EventHandler, EventRegistrationToken * Token)

Das WebResourceResponseReceived-Ereignis wird ausgelöst, nachdem die WebView die Antwort für eine Webressourcen Anforderung empfangen und verarbeitet hat. Zu den Ereignis-args gehören die vom WebResourceRequest gesendeten und empfangenen WebResourceResponse, einschließlich aller zusätzlichen Überschriften, die vom Netzwerkstapel hinzugefügt wurden, die nicht als Teil des zugeordneten WebResourceRequested-Ereignisses, wie etwa Authentifizierungs Kopfzeilen, aufgenommen wurden. 
```cpp
    wil::com_ptr<ICoreWebView2Experimental> webviewExperimental;
    CHECK_FAILURE(m_appWindow->GetWebView()->QueryInterface(IID_PPV_ARGS(&webviewExperimental)));
    CHECK_FAILURE(webviewExperimental->add_WebResourceResponseReceived(
        Callback<ICoreWebView2ExperimentalWebResourceResponseReceivedEventHandler>(
            [this](
                ICoreWebView2Experimental* sender,
                ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgs* args) {           
                wil::com_ptr<ICoreWebView2WebResourceRequest> request;
                CHECK_FAILURE(args->get_Request(&request));
                wil::unique_cotaskmem_string uri;
                CHECK_FAILURE(request->get_Uri(&uri));
                if (wcscmp(uri.get(), L"https://authenticationtest.com/HTTPAuth/") == 0)
                {
                    wil::com_ptr<ICoreWebView2HttpRequestHeaders> requestHeaders;
                    CHECK_FAILURE(request->get_Headers(&requestHeaders));

                    wil::unique_cotaskmem_string authHeaderValue;
                    if (requestHeaders->GetHeader(L"Authorization", &authHeaderValue) == S_OK)
                    {
                        std::wstring message(L"Authorization: ");
                        message += authHeaderValue.get();
                        MessageBox(nullptr, message.c_str(), nullptr, MB_OK);
                        m_appWindow->DeleteComponent(this);
                    }
                }
                
                return S_OK;
            })
            .Get(),
        &m_webResourceResponseReceivedToken));
```

#### remove_WebResourceResponseReceived 

Entfernt den zuvor mit add_WebResourceResponseReceived hinzugefügten WebResourceResponseReceived-Ereignishandler.

> Public HRESULT [remove_WebResourceResponseReceived](#remove_webresourceresponsereceived)(EventRegistrationToken-Token)

