---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.8.355-WebView2 Win32 C++ IWebView2WebView3
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge
ms.openlocfilehash: cfb99be772170ee458fa252133f90240d75af3db
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878050"
---
# <span data-ttu-id="f5d78-104">0.8.355-Interface-IWebView2WebView3</span><span class="sxs-lookup"><span data-stu-id="f5d78-104">0.8.355 - interface IWebView2WebView3</span></span> 

> [!NOTE]
> <span data-ttu-id="f5d78-105">Diese Schnittstelle kann nach der SDK-Version 0.8.355 geändert oder für Versionen nicht verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="f5d78-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="f5d78-106">Die neueste API-Referenz finden Sie unter [Referenz](../../../webview2-api-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="f5d78-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2WebView3
  : public IWebView2WebView
```

<span data-ttu-id="f5d78-107">Zusätzliche Funktionen, die vom primären WebView-Objekt implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="f5d78-107">Additional functionality implemented by the primary WebView object.</span></span>

## <span data-ttu-id="f5d78-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="f5d78-108">Summary</span></span>

 <span data-ttu-id="f5d78-109">Member</span><span class="sxs-lookup"><span data-stu-id="f5d78-109">Members</span></span>                        | <span data-ttu-id="f5d78-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="f5d78-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="f5d78-111">Stop</span><span class="sxs-lookup"><span data-stu-id="f5d78-111">Stop</span></span>](#stop) | <span data-ttu-id="f5d78-112">Beenden Sie alle Navigations-und ausstehenden Ressourcen Abrufe.</span><span class="sxs-lookup"><span data-stu-id="f5d78-112">Stop all navigations and pending resource fetches.</span></span>
[<span data-ttu-id="f5d78-113">add_NewWindowRequested</span><span class="sxs-lookup"><span data-stu-id="f5d78-113">add_NewWindowRequested</span></span>](#add_newwindowrequested) | <span data-ttu-id="f5d78-114">Fügen Sie einen Ereignishandler für das mswebviewnewwindowrequested-Ereignis hinzu.</span><span class="sxs-lookup"><span data-stu-id="f5d78-114">Add an event handler for the NewWindowRequested event.</span></span>
[<span data-ttu-id="f5d78-115">remove_NewWindowRequested</span><span class="sxs-lookup"><span data-stu-id="f5d78-115">remove_NewWindowRequested</span></span>](#remove_newwindowrequested) | <span data-ttu-id="f5d78-116">Entfernen Sie einen Ereignishandler, der zuvor mit add_NewWindowRequested hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="f5d78-116">Remove an event handler previously added with add_NewWindowRequested.</span></span>
[<span data-ttu-id="f5d78-117">add_DocumentTitleChanged</span><span class="sxs-lookup"><span data-stu-id="f5d78-117">add_DocumentTitleChanged</span></span>](#add_documenttitlechanged) | <span data-ttu-id="f5d78-118">Fügen Sie einen Ereignishandler für das DocumentTitleChanged-Ereignis hinzu.</span><span class="sxs-lookup"><span data-stu-id="f5d78-118">Add an event handler for the DocumentTitleChanged event.</span></span>
[<span data-ttu-id="f5d78-119">remove_DocumentTitleChanged</span><span class="sxs-lookup"><span data-stu-id="f5d78-119">remove_DocumentTitleChanged</span></span>](#remove_documenttitlechanged) | <span data-ttu-id="f5d78-120">Entfernen Sie einen Ereignishandler, der zuvor mit add_DocumentTitleChanged hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="f5d78-120">Remove an event handler previously added with add_DocumentTitleChanged.</span></span>
[<span data-ttu-id="f5d78-121">get_DocumentTitle</span><span class="sxs-lookup"><span data-stu-id="f5d78-121">get_DocumentTitle</span></span>](#get_documenttitle) | <span data-ttu-id="f5d78-122">Der Titel für das aktuelle Dokument der obersten Ebene.</span><span class="sxs-lookup"><span data-stu-id="f5d78-122">The title for the current top level document.</span></span>

<span data-ttu-id="f5d78-123">Sie können QueryInterface für diese Schnittstelle aus dem Objekt, das [IWebView2WebView](IWebView2WebView.md)implementiert.</span><span class="sxs-lookup"><span data-stu-id="f5d78-123">You can QueryInterface for this interface from the object that implements [IWebView2WebView](IWebView2WebView.md).</span></span> <span data-ttu-id="f5d78-124">Weitere Informationen finden Sie auf der [IWebView2WebView](IWebView2WebView.md) -Benutzeroberfläche.</span><span class="sxs-lookup"><span data-stu-id="f5d78-124">See the [IWebView2WebView](IWebView2WebView.md) interface for more details.</span></span>

## <span data-ttu-id="f5d78-125">Member</span><span class="sxs-lookup"><span data-stu-id="f5d78-125">Members</span></span>

#### <span data-ttu-id="f5d78-126">Stop</span><span class="sxs-lookup"><span data-stu-id="f5d78-126">Stop</span></span> 

<span data-ttu-id="f5d78-127">Beenden Sie alle Navigations-und ausstehenden Ressourcen Abrufe.</span><span class="sxs-lookup"><span data-stu-id="f5d78-127">Stop all navigations and pending resource fetches.</span></span>

> <span data-ttu-id="f5d78-128">öffentlicher HRESULT- [Stopp](#stop)()</span><span class="sxs-lookup"><span data-stu-id="f5d78-128">public HRESULT [Stop](#stop)()</span></span>

#### <span data-ttu-id="f5d78-129">add_NewWindowRequested</span><span class="sxs-lookup"><span data-stu-id="f5d78-129">add_NewWindowRequested</span></span> 

<span data-ttu-id="f5d78-130">Fügen Sie einen Ereignishandler für das mswebviewnewwindowrequested-Ereignis hinzu.</span><span class="sxs-lookup"><span data-stu-id="f5d78-130">Add an event handler for the NewWindowRequested event.</span></span>

> <span data-ttu-id="f5d78-131">Public HRESULT [add_NewWindowRequested](#add_newwindowrequested)([IWebView2NewWindowRequestedEventHandler](IWebView2NewWindowRequestedEventHandler.md) \* EventHandler, EventRegistrationToken \* Token)</span><span class="sxs-lookup"><span data-stu-id="f5d78-131">public HRESULT [add_NewWindowRequested](#add_newwindowrequested)([IWebView2NewWindowRequestedEventHandler](IWebView2NewWindowRequestedEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="f5d78-132">Wird ausgelöst, wenn der Inhalt in der WebView zum Öffnen eines neuen Fensters angefordert wird, beispielsweisedurch Window. Open.</span><span class="sxs-lookup"><span data-stu-id="f5d78-132">Fires when content inside the WebView requested to open a new window, such as through window.open.</span></span> <span data-ttu-id="f5d78-133">Die APP kann eine Ziel-WebView übergeben, die als das geöffnete Fenster angesehen wird.</span><span class="sxs-lookup"><span data-stu-id="f5d78-133">The app can pass a target webview that will be considered the opened window.</span></span>

```cpp
    // Register a handler for the NewWindowRequested event.
    // This handler will defer the event, create a new app window, and then once the
    // new window is ready, it'll provide that new window's WebView as the response to
    // the request.
    CHECK_FAILURE(m_webView->add_NewWindowRequested(
        Callback<IWebView2NewWindowRequestedEventHandler>(
            [this](IWebView2WebView* sender, IWebView2NewWindowRequestedEventArgs* args) {
                wil::com_ptr<IWebView2Deferral> deferral;
                CHECK_FAILURE(args->GetDeferral(&deferral));

                auto newAppWindow = new AppWindow(L"");
                newAppWindow->m_onWebViewFirstInitialized = [args, deferral, newAppWindow]() {
                    CHECK_FAILURE(args->put_NewWindow(newAppWindow->m_webView.get()));
                    CHECK_FAILURE(args->put_Handled(TRUE));
                    CHECK_FAILURE(deferral->Complete());
                };

                return S_OK;
            })
            .Get(),
        nullptr));
```

#### <span data-ttu-id="f5d78-134">remove_NewWindowRequested</span><span class="sxs-lookup"><span data-stu-id="f5d78-134">remove_NewWindowRequested</span></span> 

<span data-ttu-id="f5d78-135">Entfernen Sie einen Ereignishandler, der zuvor mit add_NewWindowRequested hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="f5d78-135">Remove an event handler previously added with add_NewWindowRequested.</span></span>

> <span data-ttu-id="f5d78-136">Public HRESULT [remove_NewWindowRequested](#remove_newwindowrequested)(EventRegistrationToken-Token)</span><span class="sxs-lookup"><span data-stu-id="f5d78-136">public HRESULT [remove_NewWindowRequested](#remove_newwindowrequested)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="f5d78-137">add_DocumentTitleChanged</span><span class="sxs-lookup"><span data-stu-id="f5d78-137">add_DocumentTitleChanged</span></span> 

<span data-ttu-id="f5d78-138">Fügen Sie einen Ereignishandler für das DocumentTitleChanged-Ereignis hinzu.</span><span class="sxs-lookup"><span data-stu-id="f5d78-138">Add an event handler for the DocumentTitleChanged event.</span></span>

> <span data-ttu-id="f5d78-139">Public HRESULT [add_DocumentTitleChanged](#add_documenttitlechanged)([IWebView2DocumentTitleChangedEventHandler](IWebView2DocumentTitleChangedEventHandler.md) \* EventHandler, EventRegistrationToken \* Token)</span><span class="sxs-lookup"><span data-stu-id="f5d78-139">public HRESULT [add_DocumentTitleChanged](#add_documenttitlechanged)([IWebView2DocumentTitleChangedEventHandler](IWebView2DocumentTitleChangedEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="f5d78-140">Das Ereignis wird ausgelöst, wenn die DocumentTitle-Eigenschaft des WebView-Ereignisses geändert wird und möglicherweise vor oder nach dem NavigationCompleted-Ereignis ausgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="f5d78-140">The event fires when the DocumentTitle property of the WebView changes and may fire before or after the NavigationCompleted event.</span></span>

```cpp
    // Register a handler for the DocumentTitleChanged event.
    // This handler just announces the new title on the window's title bar.
    CHECK_FAILURE(m_webView->add_DocumentTitleChanged(
        Callback<IWebView2DocumentTitleChangedEventHandler>(
            [this](IWebView2WebView3* sender, IUnknown* args) -> HRESULT {
                wil::unique_cotaskmem_string title;
                CHECK_FAILURE(sender->get_DocumentTitle(&title));
                SetWindowText(m_appWindow->GetMainWindow(), title.get());
                return S_OK;
            })
            .Get(),
        &m_documentTitleChangedToken));
```

#### <span data-ttu-id="f5d78-141">remove_DocumentTitleChanged</span><span class="sxs-lookup"><span data-stu-id="f5d78-141">remove_DocumentTitleChanged</span></span> 

<span data-ttu-id="f5d78-142">Entfernen Sie einen Ereignishandler, der zuvor mit add_DocumentTitleChanged hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="f5d78-142">Remove an event handler previously added with add_DocumentTitleChanged.</span></span>

> <span data-ttu-id="f5d78-143">Public HRESULT [remove_DocumentTitleChanged](#remove_documenttitlechanged)(EventRegistrationToken-Token)</span><span class="sxs-lookup"><span data-stu-id="f5d78-143">public HRESULT [remove_DocumentTitleChanged](#remove_documenttitlechanged)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="f5d78-144">get_DocumentTitle</span><span class="sxs-lookup"><span data-stu-id="f5d78-144">get_DocumentTitle</span></span> 

<span data-ttu-id="f5d78-145">Der Titel für das aktuelle Dokument der obersten Ebene.</span><span class="sxs-lookup"><span data-stu-id="f5d78-145">The title for the current top level document.</span></span>

> <span data-ttu-id="f5d78-146">öffentliche HRESULT- [get_DocumentTitle](#get_documenttitle)(LPWSTR \* Title)</span><span class="sxs-lookup"><span data-stu-id="f5d78-146">public HRESULT [get_DocumentTitle](#get_documenttitle)(LPWSTR \* title)</span></span>

<span data-ttu-id="f5d78-147">Wenn das Dokument keinen expliziten Titel hat oder sonst leer ist, wird ein Standardwert verwendet, der möglicherweise nicht mit dem URI des Dokuments übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="f5d78-147">If the document has no explicit title or is otherwise empty, a default that may or may not match the URI of the document will be used.</span></span>

