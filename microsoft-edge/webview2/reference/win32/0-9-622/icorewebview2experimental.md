---
description: Einbetten von Webtechnologien (HTML, CSS und JavaScript) in ihre systemeigenen Anwendungen mit dem Microsoft Edge WebView2-Steuerelement
title: WebView2 Win32 C++ ICoreWebView2Experimental
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML, ICoreWebView2Experimental
ms.openlocfilehash: 44795ab425e814054dd3d58cba585f1badfbf431
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/10/2020
ms.locfileid: "11012122"
---
# <span data-ttu-id="30206-104">Schnittstellen ICoreWebView2Experimental</span><span class="sxs-lookup"><span data-stu-id="30206-104">interface ICoreWebView2Experimental</span></span> 

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

```
interface ICoreWebView2Experimental
  : public IUnknown
```

## <span data-ttu-id="30206-105">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="30206-105">Summary</span></span>

 <span data-ttu-id="30206-106">Member</span><span class="sxs-lookup"><span data-stu-id="30206-106">Members</span></span>                        | <span data-ttu-id="30206-107">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="30206-107">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="30206-108">add_WebResourceResponseReceived</span><span class="sxs-lookup"><span data-stu-id="30206-108">add_WebResourceResponseReceived</span></span>](#add_webresourceresponsereceived) | <span data-ttu-id="30206-109">Fügen Sie einen Ereignishandler für das WebResourceResponseReceived-Ereignis hinzu.</span><span class="sxs-lookup"><span data-stu-id="30206-109">Add an event handler for the WebResourceResponseReceived event.</span></span>
[<span data-ttu-id="30206-110">remove_WebResourceResponseReceived</span><span class="sxs-lookup"><span data-stu-id="30206-110">remove_WebResourceResponseReceived</span></span>](#remove_webresourceresponsereceived) | <span data-ttu-id="30206-111">Entfernt den zuvor mit add_WebResourceResponseReceived hinzugefügten WebResourceResponseReceived-Ereignishandler.</span><span class="sxs-lookup"><span data-stu-id="30206-111">Removes the WebResourceResponseReceived event handler previously added with add_WebResourceResponseReceived.</span></span>

## <span data-ttu-id="30206-112">Member</span><span class="sxs-lookup"><span data-stu-id="30206-112">Members</span></span>

#### <span data-ttu-id="30206-113">add_WebResourceResponseReceived</span><span class="sxs-lookup"><span data-stu-id="30206-113">add_WebResourceResponseReceived</span></span> 

<span data-ttu-id="30206-114">Fügen Sie einen Ereignishandler für das WebResourceResponseReceived-Ereignis hinzu.</span><span class="sxs-lookup"><span data-stu-id="30206-114">Add an event handler for the WebResourceResponseReceived event.</span></span>

> <span data-ttu-id="30206-115">Public HRESULT [add_WebResourceResponseReceived](#add_webresourceresponsereceived)([ICoreWebView2ExperimentalWebResourceResponseReceivedEventHandler](icorewebview2experimentalwebresourceresponsereceivedeventhandler.md) \* EventHandler, EventRegistrationToken \* Token)</span><span class="sxs-lookup"><span data-stu-id="30206-115">public HRESULT [add_WebResourceResponseReceived](#add_webresourceresponsereceived)([ICoreWebView2ExperimentalWebResourceResponseReceivedEventHandler](icorewebview2experimentalwebresourceresponsereceivedeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="30206-116">Das WebResourceResponseReceived-Ereignis wird ausgelöst, nachdem die WebView die Antwort für eine Webressourcen Anforderung empfangen und verarbeitet hat.</span><span class="sxs-lookup"><span data-stu-id="30206-116">WebResourceResponseReceived event fires after the WebView has received and processed the response for a WebResource request.</span></span> <span data-ttu-id="30206-117">Zu den Ereignis-args gehören die vom WebResourceRequest gesendeten und empfangenen WebResourceResponse, einschließlich aller zusätzlichen Überschriften, die vom Netzwerkstapel hinzugefügt wurden, die nicht als Teil des zugeordneten WebResourceRequested-Ereignisses, wie etwa Authentifizierungs Kopfzeilen, aufgenommen wurden.</span><span class="sxs-lookup"><span data-stu-id="30206-117">The event args include the WebResourceRequest as sent by the wire and WebResourceResponse received, including any additional headers added by the network stack that were not be included as part of the associated WebResourceRequested event, such as Authentication headers.</span></span> 
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

#### <span data-ttu-id="30206-118">remove_WebResourceResponseReceived</span><span class="sxs-lookup"><span data-stu-id="30206-118">remove_WebResourceResponseReceived</span></span> 

<span data-ttu-id="30206-119">Entfernt den zuvor mit add_WebResourceResponseReceived hinzugefügten WebResourceResponseReceived-Ereignishandler.</span><span class="sxs-lookup"><span data-stu-id="30206-119">Removes the WebResourceResponseReceived event handler previously added with add_WebResourceResponseReceived.</span></span>

> <span data-ttu-id="30206-120">Public HRESULT [remove_WebResourceResponseReceived](#remove_webresourceresponsereceived)(EventRegistrationToken-Token)</span><span class="sxs-lookup"><span data-stu-id="30206-120">public HRESULT [remove_WebResourceResponseReceived](#remove_webresourceresponsereceived)(EventRegistrationToken token)</span></span>

