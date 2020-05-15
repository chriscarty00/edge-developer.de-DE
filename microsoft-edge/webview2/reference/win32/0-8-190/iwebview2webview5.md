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
ms.openlocfilehash: 3c32cd59e75eb81bf69661d01f6044a0628ba35d
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653705"
---
# <span data-ttu-id="3a03f-104">Schnittstellen IWebView2WebView5</span><span class="sxs-lookup"><span data-stu-id="3a03f-104">interface IWebView2WebView5</span></span> 

> [!NOTE]
> <span data-ttu-id="3a03f-105">Diese Schnittstelle kann nach der SDK-Version 0.8.355 geändert oder für Versionen nicht verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="3a03f-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="3a03f-106">Die neueste API-Referenz finden Sie unter [Referenz](../../../webview2-api-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="3a03f-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2WebView5
  : public IWebView2WebView4
```

<span data-ttu-id="3a03f-107">Zusätzliche Funktionen, die vom primären WebView-Objekt implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="3a03f-107">Additional functionality implemented by the primary WebView object.</span></span>

## <span data-ttu-id="3a03f-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="3a03f-108">Summary</span></span>

 <span data-ttu-id="3a03f-109">Member</span><span class="sxs-lookup"><span data-stu-id="3a03f-109">Members</span></span>                        | <span data-ttu-id="3a03f-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="3a03f-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="3a03f-111">add_ContainsFullScreenElementChanged</span><span class="sxs-lookup"><span data-stu-id="3a03f-111">add_ContainsFullScreenElementChanged</span></span>](#add_containsfullscreenelementchanged) | <span data-ttu-id="3a03f-112">Benachrichtigt, wenn sich die ContainsFullScreenElement-Eigenschaft ändert.</span><span class="sxs-lookup"><span data-stu-id="3a03f-112">Notifies when the ContainsFullScreenElement property changes.</span></span>
[<span data-ttu-id="3a03f-113">remove_ContainsFullScreenElementChanged</span><span class="sxs-lookup"><span data-stu-id="3a03f-113">remove_ContainsFullScreenElementChanged</span></span>](#remove_containsfullscreenelementchanged) | <span data-ttu-id="3a03f-114">Entfernen Sie einen Ereignishandler, der zuvor mit der entsprechenden add_-Ereignismethode hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="3a03f-114">Remove an event handler previously added with the corresponding add_ event method.</span></span>
[<span data-ttu-id="3a03f-115">get_ContainsFullScreenElement</span><span class="sxs-lookup"><span data-stu-id="3a03f-115">get_ContainsFullScreenElement</span></span>](#get_containsfullscreenelement) | <span data-ttu-id="3a03f-116">Gibt an, ob die WebView ein HTML-Vollbild-Element enthält.</span><span class="sxs-lookup"><span data-stu-id="3a03f-116">Indicates if the WebView contains a fullscreen HTML element.</span></span>
[<span data-ttu-id="3a03f-117">add_WebResourceRequested</span><span class="sxs-lookup"><span data-stu-id="3a03f-117">add_WebResourceRequested</span></span>](#add_webresourcerequested) | <span data-ttu-id="3a03f-118">Fügen Sie einen Ereignishandler für das WebResourceRequested-Ereignis hinzu.</span><span class="sxs-lookup"><span data-stu-id="3a03f-118">Add an event handler for the WebResourceRequested event.</span></span>
[<span data-ttu-id="3a03f-119">AddWebResourceRequestedFilter</span><span class="sxs-lookup"><span data-stu-id="3a03f-119">AddWebResourceRequestedFilter</span></span>](#addwebresourcerequestedfilter) | <span data-ttu-id="3a03f-120">Fügt dem WebResourceRequested-Ereignis einen URI-und Ressourcenkontext Filter hinzu.</span><span class="sxs-lookup"><span data-stu-id="3a03f-120">Adds a URI and resource context filter to the WebResourceRequested event.</span></span>
[<span data-ttu-id="3a03f-121">RemoveWebResourceRequestedFilter</span><span class="sxs-lookup"><span data-stu-id="3a03f-121">RemoveWebResourceRequestedFilter</span></span>](#removewebresourcerequestedfilter) | <span data-ttu-id="3a03f-122">Entfernt einen übereinstimmenden Webressourcen Filter, der zuvor für das WebResourceRequested-Ereignis hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="3a03f-122">Removes a matching WebResource filter that was previously added for the WebResourceRequested event.</span></span>

<span data-ttu-id="3a03f-123">Sie können QueryInterface für diese Schnittstelle aus dem Objekt, das [IWebView2WebView](IWebView2WebView.md)implementiert.</span><span class="sxs-lookup"><span data-stu-id="3a03f-123">You can QueryInterface for this interface from the object that implements [IWebView2WebView](IWebView2WebView.md).</span></span> <span data-ttu-id="3a03f-124">Weitere Informationen finden Sie auf der [IWebView2WebView](IWebView2WebView.md) -Benutzeroberfläche.</span><span class="sxs-lookup"><span data-stu-id="3a03f-124">See the [IWebView2WebView](IWebView2WebView.md) interface for more details.</span></span>

## <span data-ttu-id="3a03f-125">Member</span><span class="sxs-lookup"><span data-stu-id="3a03f-125">Members</span></span>

#### <span data-ttu-id="3a03f-126">add_ContainsFullScreenElementChanged</span><span class="sxs-lookup"><span data-stu-id="3a03f-126">add_ContainsFullScreenElementChanged</span></span> 

<span data-ttu-id="3a03f-127">Benachrichtigt, wenn sich die ContainsFullScreenElement-Eigenschaft ändert.</span><span class="sxs-lookup"><span data-stu-id="3a03f-127">Notifies when the ContainsFullScreenElement property changes.</span></span>

> <span data-ttu-id="3a03f-128">Public HRESULT [add_ContainsFullScreenElementChanged](#add_containsfullscreenelementchanged)([IWebView2ContainsFullScreenElementChangedEventHandler](IWebView2ContainsFullScreenElementChangedEventHandler.md) \* EventHandler, EventRegistrationToken \* Token)</span><span class="sxs-lookup"><span data-stu-id="3a03f-128">public HRESULT [add_ContainsFullScreenElementChanged](#add_containsfullscreenelementchanged)([IWebView2ContainsFullScreenElementChangedEventHandler](IWebView2ContainsFullScreenElementChangedEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="3a03f-129">Dies bedeutet, dass ein HTML-Element in der WebView Vollbild auf die Größe des WebView-Elements eingibt oder den Fullscreen-Eintrag verlässt.</span><span class="sxs-lookup"><span data-stu-id="3a03f-129">This means that an HTML element inside the WebView is entering fullscreen to the size of the WebView or leaving fullscreen.</span></span> <span data-ttu-id="3a03f-130">Dieses Ereignis ist nützlich, wenn beispielsweise ein Video Element den Fullscreen-Modus anfordert.</span><span class="sxs-lookup"><span data-stu-id="3a03f-130">This event is useful when, for example, a video element requests to go fullscreen.</span></span> <span data-ttu-id="3a03f-131">Der Listener von ContainsFullScreenElementChanged kann die WebView-Ansicht dann als Antwort ändern.</span><span class="sxs-lookup"><span data-stu-id="3a03f-131">The listener of ContainsFullScreenElementChanged can then resize the WebView in response.</span></span>

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

#### <span data-ttu-id="3a03f-132">remove_ContainsFullScreenElementChanged</span><span class="sxs-lookup"><span data-stu-id="3a03f-132">remove_ContainsFullScreenElementChanged</span></span> 

<span data-ttu-id="3a03f-133">Entfernen Sie einen Ereignishandler, der zuvor mit der entsprechenden add_-Ereignismethode hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="3a03f-133">Remove an event handler previously added with the corresponding add_ event method.</span></span>

> <span data-ttu-id="3a03f-134">Public HRESULT [remove_ContainsFullScreenElementChanged](#remove_containsfullscreenelementchanged)(EventRegistrationToken-Token)</span><span class="sxs-lookup"><span data-stu-id="3a03f-134">public HRESULT [remove_ContainsFullScreenElementChanged](#remove_containsfullscreenelementchanged)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="3a03f-135">get_ContainsFullScreenElement</span><span class="sxs-lookup"><span data-stu-id="3a03f-135">get_ContainsFullScreenElement</span></span> 

<span data-ttu-id="3a03f-136">Gibt an, ob die WebView ein HTML-Vollbild-Element enthält.</span><span class="sxs-lookup"><span data-stu-id="3a03f-136">Indicates if the WebView contains a fullscreen HTML element.</span></span>

> <span data-ttu-id="3a03f-137">Public HRESULT [get_ContainsFullScreenElement](#get_containsfullscreenelement)(bool \* ContainsFullScreenElement)</span><span class="sxs-lookup"><span data-stu-id="3a03f-137">public HRESULT [get_ContainsFullScreenElement](#get_containsfullscreenelement)(BOOL \* containsFullScreenElement)</span></span>

#### <span data-ttu-id="3a03f-138">add_WebResourceRequested</span><span class="sxs-lookup"><span data-stu-id="3a03f-138">add_WebResourceRequested</span></span> 

<span data-ttu-id="3a03f-139">Fügen Sie einen Ereignishandler für das WebResourceRequested-Ereignis hinzu.</span><span class="sxs-lookup"><span data-stu-id="3a03f-139">Add an event handler for the WebResourceRequested event.</span></span>

> <span data-ttu-id="3a03f-140">Public HRESULT [add_WebResourceRequested](#add_webresourcerequested)([IWebView2WebResourceRequestedEventHandler](IWebView2WebResourceRequestedEventHandler.md) \* EventHandler, EventRegistrationToken \* Token)</span><span class="sxs-lookup"><span data-stu-id="3a03f-140">public HRESULT [add_WebResourceRequested](#add_webresourcerequested)([IWebView2WebResourceRequestedEventHandler](IWebView2WebResourceRequestedEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="3a03f-141">Wird ausgelöst, wenn die WebView eine HTTP-Anforderung an einen übereinstimmenden URL-und Ressourcenkontext Filter ausführt, der mit AddWebResourceRequestedFilter hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="3a03f-141">Fires when the WebView is performing an HTTP request to a matching URL and resource context filter that was added with AddWebResourceRequestedFilter.</span></span> <span data-ttu-id="3a03f-142">Es muss mindestens ein Filter hinzugefügt werden, damit das Ereignis ausgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="3a03f-142">At least one filter must be added for the event to fire.</span></span>

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

#### <span data-ttu-id="3a03f-143">AddWebResourceRequestedFilter</span><span class="sxs-lookup"><span data-stu-id="3a03f-143">AddWebResourceRequestedFilter</span></span> 

<span data-ttu-id="3a03f-144">Fügt dem WebResourceRequested-Ereignis einen URI-und Ressourcenkontext Filter hinzu.</span><span class="sxs-lookup"><span data-stu-id="3a03f-144">Adds a URI and resource context filter to the WebResourceRequested event.</span></span>

> <span data-ttu-id="3a03f-145">Public HRESULT [AddWebResourceRequestedFilter](#addwebresourcerequestedfilter)(LPCWSTR const URI,[WEBVIEW2_WEB_RESOURCE_CONTEXT](IWebView2WebView.md#webview2_web_resource_context) const resourcecontext)</span><span class="sxs-lookup"><span data-stu-id="3a03f-145">public HRESULT [AddWebResourceRequestedFilter](#addwebresourcerequestedfilter)(LPCWSTR const uri,[WEBVIEW2_WEB_RESOURCE_CONTEXT](IWebView2WebView.md#webview2_web_resource_context) const resourceContext)</span></span>

<span data-ttu-id="3a03f-146">Der URI-Parameter kann eine Platzhalterzeichenfolge (' ': 0 oder mehr; '? ': genau eins) sein.</span><span class="sxs-lookup"><span data-stu-id="3a03f-146">URI parameter can be a wildcard string ('': zero or more, '?': exactly one).</span></span> <span data-ttu-id="3a03f-147">nullptr entspricht L "".</span><span class="sxs-lookup"><span data-stu-id="3a03f-147">nullptr is equivalent to L"".</span></span> <span data-ttu-id="3a03f-148">Eine Beschreibung der Ressourcenkontext Filter finden Sie unter WEBVIEW2_WEB_RESOURCE_CONTEXT Enum.</span><span class="sxs-lookup"><span data-stu-id="3a03f-148">See WEBVIEW2_WEB_RESOURCE_CONTEXT enum for description of resource context filters.</span></span>

#### <span data-ttu-id="3a03f-149">RemoveWebResourceRequestedFilter</span><span class="sxs-lookup"><span data-stu-id="3a03f-149">RemoveWebResourceRequestedFilter</span></span> 

<span data-ttu-id="3a03f-150">Entfernt einen übereinstimmenden Webressourcen Filter, der zuvor für das WebResourceRequested-Ereignis hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="3a03f-150">Removes a matching WebResource filter that was previously added for the WebResourceRequested event.</span></span>

> <span data-ttu-id="3a03f-151">Public HRESULT [RemoveWebResourceRequestedFilter](#removewebresourcerequestedfilter)(LPCWSTR const URI,[WEBVIEW2_WEB_RESOURCE_CONTEXT](IWebView2WebView.md#webview2_web_resource_context) const resourcecontext)</span><span class="sxs-lookup"><span data-stu-id="3a03f-151">public HRESULT [RemoveWebResourceRequestedFilter](#removewebresourcerequestedfilter)(LPCWSTR const uri,[WEBVIEW2_WEB_RESOURCE_CONTEXT](IWebView2WebView.md#webview2_web_resource_context) const resourceContext)</span></span>

<span data-ttu-id="3a03f-152">Wenn derselbe Filter mehrmals hinzugefügt wurde, muss er so oft entfernt werden, wie er hinzugefügt wurde, damit er wirksam wird.</span><span class="sxs-lookup"><span data-stu-id="3a03f-152">If the same filter was added multiple times, then it will need to be removed as many times as it was added for the removal to be effective.</span></span> <span data-ttu-id="3a03f-153">Gibt E_INVALIDARG für einen Filter zurück, der nie hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="3a03f-153">Returns E_INVALIDARG for a filter that was never added.</span></span>

