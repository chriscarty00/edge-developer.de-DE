---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.8.355-WebView2 Win32 C++ IWebView2WebView5
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge
ms.openlocfilehash: bc48c5d495c2182ba39b867fdb46ce7af503f5ba
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884687"
---
# <span data-ttu-id="647e6-104">0.8.355-Interface-IWebView2WebView5</span><span class="sxs-lookup"><span data-stu-id="647e6-104">0.8.355 - interface IWebView2WebView5</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2WebView5
  : public IWebView2WebView4
```

<span data-ttu-id="647e6-105">Zusätzliche Funktionen, die vom primären WebView-Objekt implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="647e6-105">Additional functionality implemented by the primary WebView object.</span></span>

## <span data-ttu-id="647e6-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="647e6-106">Summary</span></span>

 <span data-ttu-id="647e6-107">Member</span><span class="sxs-lookup"><span data-stu-id="647e6-107">Members</span></span>                        | <span data-ttu-id="647e6-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="647e6-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="647e6-109">add_ContainsFullScreenElementChanged</span><span class="sxs-lookup"><span data-stu-id="647e6-109">add_ContainsFullScreenElementChanged</span></span>](#add_containsfullscreenelementchanged) | <span data-ttu-id="647e6-110">Benachrichtigt, wenn sich die ContainsFullScreenElement-Eigenschaft ändert.</span><span class="sxs-lookup"><span data-stu-id="647e6-110">Notifies when the ContainsFullScreenElement property changes.</span></span>
[<span data-ttu-id="647e6-111">remove_ContainsFullScreenElementChanged</span><span class="sxs-lookup"><span data-stu-id="647e6-111">remove_ContainsFullScreenElementChanged</span></span>](#remove_containsfullscreenelementchanged) | <span data-ttu-id="647e6-112">Entfernen Sie einen Ereignishandler, der zuvor mit der entsprechenden add_-Ereignismethode hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="647e6-112">Remove an event handler previously added with the corresponding add_ event method.</span></span>
[<span data-ttu-id="647e6-113">get_ContainsFullScreenElement</span><span class="sxs-lookup"><span data-stu-id="647e6-113">get_ContainsFullScreenElement</span></span>](#get_containsfullscreenelement) | <span data-ttu-id="647e6-114">Gibt an, ob die WebView ein HTML-Vollbild-Element enthält.</span><span class="sxs-lookup"><span data-stu-id="647e6-114">Indicates if the WebView contains a fullscreen HTML element.</span></span>
[<span data-ttu-id="647e6-115">add_WebResourceRequested</span><span class="sxs-lookup"><span data-stu-id="647e6-115">add_WebResourceRequested</span></span>](#add_webresourcerequested) | <span data-ttu-id="647e6-116">Fügen Sie einen Ereignishandler für das WebResourceRequested-Ereignis hinzu.</span><span class="sxs-lookup"><span data-stu-id="647e6-116">Add an event handler for the WebResourceRequested event.</span></span>
[<span data-ttu-id="647e6-117">AddWebResourceRequestedFilter</span><span class="sxs-lookup"><span data-stu-id="647e6-117">AddWebResourceRequestedFilter</span></span>](#addwebresourcerequestedfilter) | <span data-ttu-id="647e6-118">Fügt dem WebResourceRequested-Ereignis einen URI-und Ressourcenkontext Filter hinzu.</span><span class="sxs-lookup"><span data-stu-id="647e6-118">Adds a URI and resource context filter to the WebResourceRequested event.</span></span>
[<span data-ttu-id="647e6-119">RemoveWebResourceRequestedFilter</span><span class="sxs-lookup"><span data-stu-id="647e6-119">RemoveWebResourceRequestedFilter</span></span>](#removewebresourcerequestedfilter) | <span data-ttu-id="647e6-120">Entfernt einen übereinstimmenden Webressourcen Filter, der zuvor für das WebResourceRequested-Ereignis hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="647e6-120">Removes a matching WebResource filter that was previously added for the WebResourceRequested event.</span></span>

<span data-ttu-id="647e6-121">Sie können QueryInterface für diese Schnittstelle aus dem Objekt, das [IWebView2WebView](IWebView2WebView.md)implementiert.</span><span class="sxs-lookup"><span data-stu-id="647e6-121">You can QueryInterface for this interface from the object that implements [IWebView2WebView](IWebView2WebView.md).</span></span> <span data-ttu-id="647e6-122">Weitere Informationen finden Sie auf der [IWebView2WebView](IWebView2WebView.md) -Benutzeroberfläche.</span><span class="sxs-lookup"><span data-stu-id="647e6-122">See the [IWebView2WebView](IWebView2WebView.md) interface for more details.</span></span>

## <span data-ttu-id="647e6-123">Member</span><span class="sxs-lookup"><span data-stu-id="647e6-123">Members</span></span>

#### <span data-ttu-id="647e6-124">add_ContainsFullScreenElementChanged</span><span class="sxs-lookup"><span data-stu-id="647e6-124">add_ContainsFullScreenElementChanged</span></span> 

<span data-ttu-id="647e6-125">Benachrichtigt, wenn sich die ContainsFullScreenElement-Eigenschaft ändert.</span><span class="sxs-lookup"><span data-stu-id="647e6-125">Notifies when the ContainsFullScreenElement property changes.</span></span>

> <span data-ttu-id="647e6-126">Public HRESULT [add_ContainsFullScreenElementChanged](#add_containsfullscreenelementchanged)([IWebView2ContainsFullScreenElementChangedEventHandler](IWebView2ContainsFullScreenElementChangedEventHandler.md) \* EventHandler, EventRegistrationToken \* Token)</span><span class="sxs-lookup"><span data-stu-id="647e6-126">public HRESULT [add_ContainsFullScreenElementChanged](#add_containsfullscreenelementchanged)([IWebView2ContainsFullScreenElementChangedEventHandler](IWebView2ContainsFullScreenElementChangedEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="647e6-127">Dies bedeutet, dass ein HTML-Element in der WebView Vollbild auf die Größe des WebView-Elements eingibt oder den Fullscreen-Eintrag verlässt.</span><span class="sxs-lookup"><span data-stu-id="647e6-127">This means that an HTML element inside the WebView is entering fullscreen to the size of the WebView or leaving fullscreen.</span></span> <span data-ttu-id="647e6-128">Dieses Ereignis ist nützlich, wenn beispielsweise ein Video Element den Fullscreen-Modus anfordert.</span><span class="sxs-lookup"><span data-stu-id="647e6-128">This event is useful when, for example, a video element requests to go fullscreen.</span></span> <span data-ttu-id="647e6-129">Der Listener von ContainsFullScreenElementChanged kann die WebView-Ansicht dann als Antwort ändern.</span><span class="sxs-lookup"><span data-stu-id="647e6-129">The listener of ContainsFullScreenElementChanged can then resize the WebView in response.</span></span>

```cpp
    // Register a handler for the ContainsFullScreenChanged event.
    CHECK_FAILURE(m_webView->add_ContainsFullScreenElementChanged(
        Callback<IWebView2ContainsFullScreenElementChangedEventHandler>(
            [this](IWebView2WebView5* sender, IUnknown* args) -> HRESULT {
                if (m_fullScreenAllowed)
                {
                    CHECK_FAILURE(sender->get_ContainsFullScreenElement(&m_containsFullscreenElement));
                    if (m_containsFullscreenElement)
                    {
                        EnterFullScreen();
                    }
                    else
                    {
                        ExitFullScreen();
                    }
                }
                return S_OK;
            })
            .Get(),
        nullptr));
```

#### <span data-ttu-id="647e6-130">remove_ContainsFullScreenElementChanged</span><span class="sxs-lookup"><span data-stu-id="647e6-130">remove_ContainsFullScreenElementChanged</span></span> 

<span data-ttu-id="647e6-131">Entfernen Sie einen Ereignishandler, der zuvor mit der entsprechenden add_-Ereignismethode hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="647e6-131">Remove an event handler previously added with the corresponding add_ event method.</span></span>

> <span data-ttu-id="647e6-132">Public HRESULT [remove_ContainsFullScreenElementChanged](#remove_containsfullscreenelementchanged)(EventRegistrationToken-Token)</span><span class="sxs-lookup"><span data-stu-id="647e6-132">public HRESULT [remove_ContainsFullScreenElementChanged](#remove_containsfullscreenelementchanged)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="647e6-133">get_ContainsFullScreenElement</span><span class="sxs-lookup"><span data-stu-id="647e6-133">get_ContainsFullScreenElement</span></span> 

<span data-ttu-id="647e6-134">Gibt an, ob die WebView ein HTML-Vollbild-Element enthält.</span><span class="sxs-lookup"><span data-stu-id="647e6-134">Indicates if the WebView contains a fullscreen HTML element.</span></span>

> <span data-ttu-id="647e6-135">Public HRESULT [get_ContainsFullScreenElement](#get_containsfullscreenelement)(bool \* ContainsFullScreenElement)</span><span class="sxs-lookup"><span data-stu-id="647e6-135">public HRESULT [get_ContainsFullScreenElement](#get_containsfullscreenelement)(BOOL \* containsFullScreenElement)</span></span>

#### <span data-ttu-id="647e6-136">add_WebResourceRequested</span><span class="sxs-lookup"><span data-stu-id="647e6-136">add_WebResourceRequested</span></span> 

<span data-ttu-id="647e6-137">Fügen Sie einen Ereignishandler für das WebResourceRequested-Ereignis hinzu.</span><span class="sxs-lookup"><span data-stu-id="647e6-137">Add an event handler for the WebResourceRequested event.</span></span>

> <span data-ttu-id="647e6-138">Public HRESULT [add_WebResourceRequested](#add_webresourcerequested)([IWebView2WebResourceRequestedEventHandler](IWebView2WebResourceRequestedEventHandler.md) \* EventHandler, EventRegistrationToken \* Token)</span><span class="sxs-lookup"><span data-stu-id="647e6-138">public HRESULT [add_WebResourceRequested](#add_webresourcerequested)([IWebView2WebResourceRequestedEventHandler](IWebView2WebResourceRequestedEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="647e6-139">Wird ausgelöst, wenn die WebView eine HTTP-Anforderung an einen übereinstimmenden URL-und Ressourcenkontext Filter ausführt, der mit AddWebResourceRequestedFilter hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="647e6-139">Fires when the WebView is performing an HTTP request to a matching URL and resource context filter that was added with AddWebResourceRequestedFilter.</span></span> <span data-ttu-id="647e6-140">Es muss mindestens ein Filter hinzugefügt werden, damit das Ereignis ausgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="647e6-140">At least one filter must be added for the event to fire.</span></span>

```cpp
        if (m_blockImages)
        {
            m_webView->AddWebResourceRequestedFilter(L"*", WEBVIEW2_WEB_RESOURCE_CONTEXT_IMAGE);
            CHECK_FAILURE(m_webView->add_WebResourceRequested(
                Callback<IWebView2WebResourceRequestedEventHandler>(
                    [this](
                        IWebView2WebView* sender,
                        IWebView2WebResourceRequestedEventArgs* args) {
                        wil::com_ptr<IWebView2WebResourceRequestedEventArgs2>
                            webResourceEventArgs2;
                        args->QueryInterface(IID_PPV_ARGS(&webResourceEventArgs2));
                        WEBVIEW2_WEB_RESOURCE_CONTEXT resourceContext;
                        CHECK_FAILURE(
                            webResourceEventArgs2->get_ResourceContext(&resourceContext));
                        // Ensure that the type is image
                        if (resourceContext != WEBVIEW2_WEB_RESOURCE_CONTEXT_IMAGE)
                        {
                            return E_INVALIDARG;
                        }
                        // Override the response with an empty one to block the image.
                        // If put_Response is not called, the request will continue as normal.
                        wil::com_ptr<IWebView2WebResourceResponse> response;
                        CHECK_FAILURE(m_webViewEnvironment->CreateWebResourceResponse(
                            nullptr, 403 /*NoContent*/, L"Blocked", L"", &response));
                        CHECK_FAILURE(args->put_Response(response.get()));
                        return S_OK;
                    })
                    .Get(),
                &m_webResourceRequestedTokenForImageBlocking));
        }
        else
        {
            CHECK_FAILURE(m_webView->remove_WebResourceRequested(
                m_webResourceRequestedTokenForImageBlocking));
        }
```

#### <span data-ttu-id="647e6-141">AddWebResourceRequestedFilter</span><span class="sxs-lookup"><span data-stu-id="647e6-141">AddWebResourceRequestedFilter</span></span> 

<span data-ttu-id="647e6-142">Fügt dem WebResourceRequested-Ereignis einen URI-und Ressourcenkontext Filter hinzu.</span><span class="sxs-lookup"><span data-stu-id="647e6-142">Adds a URI and resource context filter to the WebResourceRequested event.</span></span>

> <span data-ttu-id="647e6-143">Public HRESULT [AddWebResourceRequestedFilter](#addwebresourcerequestedfilter)(LPCWSTR const URI,[WEBVIEW2_WEB_RESOURCE_CONTEXT](IWebView2WebView.md#webview2_web_resource_context) const resourcecontext)</span><span class="sxs-lookup"><span data-stu-id="647e6-143">public HRESULT [AddWebResourceRequestedFilter](#addwebresourcerequestedfilter)(LPCWSTR const uri,[WEBVIEW2_WEB_RESOURCE_CONTEXT](IWebView2WebView.md#webview2_web_resource_context) const resourceContext)</span></span>

<span data-ttu-id="647e6-144">Der URI-Parameter kann eine Platzhalterzeichenfolge (' ': 0 oder mehr; '? ': genau eins) sein.</span><span class="sxs-lookup"><span data-stu-id="647e6-144">URI parameter can be a wildcard string ('': zero or more, '?': exactly one).</span></span> <span data-ttu-id="647e6-145">nullptr entspricht L "".</span><span class="sxs-lookup"><span data-stu-id="647e6-145">nullptr is equivalent to L"".</span></span> <span data-ttu-id="647e6-146">Eine Beschreibung der Ressourcenkontext Filter finden Sie unter WEBVIEW2_WEB_RESOURCE_CONTEXT Enum.</span><span class="sxs-lookup"><span data-stu-id="647e6-146">See WEBVIEW2_WEB_RESOURCE_CONTEXT enum for description of resource context filters.</span></span>

#### <span data-ttu-id="647e6-147">RemoveWebResourceRequestedFilter</span><span class="sxs-lookup"><span data-stu-id="647e6-147">RemoveWebResourceRequestedFilter</span></span> 

<span data-ttu-id="647e6-148">Entfernt einen übereinstimmenden Webressourcen Filter, der zuvor für das WebResourceRequested-Ereignis hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="647e6-148">Removes a matching WebResource filter that was previously added for the WebResourceRequested event.</span></span>

> <span data-ttu-id="647e6-149">Public HRESULT [RemoveWebResourceRequestedFilter](#removewebresourcerequestedfilter)(LPCWSTR const URI,[WEBVIEW2_WEB_RESOURCE_CONTEXT](IWebView2WebView.md#webview2_web_resource_context) const resourcecontext)</span><span class="sxs-lookup"><span data-stu-id="647e6-149">public HRESULT [RemoveWebResourceRequestedFilter](#removewebresourcerequestedfilter)(LPCWSTR const uri,[WEBVIEW2_WEB_RESOURCE_CONTEXT](IWebView2WebView.md#webview2_web_resource_context) const resourceContext)</span></span>

<span data-ttu-id="647e6-150">Wenn derselbe Filter mehrmals hinzugefügt wurde, muss er so oft entfernt werden, wie er hinzugefügt wurde, damit er wirksam wird.</span><span class="sxs-lookup"><span data-stu-id="647e6-150">If the same filter was added multiple times, then it will need to be removed as many times as it was added for the removal to be effective.</span></span> <span data-ttu-id="647e6-151">Gibt E_INVALIDARG für einen Filter zurück, der nie hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="647e6-151">Returns E_INVALIDARG for a filter that was never added.</span></span>

