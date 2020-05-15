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
ms.openlocfilehash: 436e0e33180c65afcce0487fffeff5f168dceab7
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653710"
---
# <span data-ttu-id="f91c8-104">Schnittstellen IWebView2WebView3</span><span class="sxs-lookup"><span data-stu-id="f91c8-104">interface IWebView2WebView3</span></span> 

> [!NOTE]
> <span data-ttu-id="f91c8-105">Diese Schnittstelle kann nach der SDK-Version 0.8.355 geändert oder für Versionen nicht verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="f91c8-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="f91c8-106">Die neueste API-Referenz finden Sie unter [Referenz](../../../webview2-api-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="f91c8-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2WebView3
  : public IWebView2WebView
```

<span data-ttu-id="f91c8-107">Zusätzliche Funktionen, die vom primären WebView-Objekt implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="f91c8-107">Additional functionality implemented by the primary WebView object.</span></span>

## <span data-ttu-id="f91c8-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="f91c8-108">Summary</span></span>

 <span data-ttu-id="f91c8-109">Member</span><span class="sxs-lookup"><span data-stu-id="f91c8-109">Members</span></span>                        | <span data-ttu-id="f91c8-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="f91c8-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="f91c8-111">Stop</span><span class="sxs-lookup"><span data-stu-id="f91c8-111">Stop</span></span>](#stop) | <span data-ttu-id="f91c8-112">Beenden Sie alle Navigations-und ausstehenden Ressourcen Abrufe.</span><span class="sxs-lookup"><span data-stu-id="f91c8-112">Stop all navigations and pending resource fetches.</span></span>
[<span data-ttu-id="f91c8-113">add_NewWindowRequested</span><span class="sxs-lookup"><span data-stu-id="f91c8-113">add_NewWindowRequested</span></span>](#add_newwindowrequested) | <span data-ttu-id="f91c8-114">Fügen Sie einen Ereignishandler für das mswebviewnewwindowrequested-Ereignis hinzu.</span><span class="sxs-lookup"><span data-stu-id="f91c8-114">Add an event handler for the NewWindowRequested event.</span></span>
[<span data-ttu-id="f91c8-115">remove_NewWindowRequested</span><span class="sxs-lookup"><span data-stu-id="f91c8-115">remove_NewWindowRequested</span></span>](#remove_newwindowrequested) | <span data-ttu-id="f91c8-116">Entfernen Sie einen Ereignishandler, der zuvor mit add_NewWindowRequested hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="f91c8-116">Remove an event handler previously added with add_NewWindowRequested.</span></span>
[<span data-ttu-id="f91c8-117">add_DocumentTitleChanged</span><span class="sxs-lookup"><span data-stu-id="f91c8-117">add_DocumentTitleChanged</span></span>](#add_documenttitlechanged) | <span data-ttu-id="f91c8-118">Fügen Sie einen Ereignishandler für das DocumentTitleChanged-Ereignis hinzu.</span><span class="sxs-lookup"><span data-stu-id="f91c8-118">Add an event handler for the DocumentTitleChanged event.</span></span>
[<span data-ttu-id="f91c8-119">remove_DocumentTitleChanged</span><span class="sxs-lookup"><span data-stu-id="f91c8-119">remove_DocumentTitleChanged</span></span>](#remove_documenttitlechanged) | <span data-ttu-id="f91c8-120">Entfernen Sie einen Ereignishandler, der zuvor mit add_DocumentTitleChanged hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="f91c8-120">Remove an event handler previously added with add_DocumentTitleChanged.</span></span>
[<span data-ttu-id="f91c8-121">get_DocumentTitle</span><span class="sxs-lookup"><span data-stu-id="f91c8-121">get_DocumentTitle</span></span>](#get_documenttitle) | <span data-ttu-id="f91c8-122">Der Titel für das aktuelle Dokument der obersten Ebene.</span><span class="sxs-lookup"><span data-stu-id="f91c8-122">The title for the current top level document.</span></span>

<span data-ttu-id="f91c8-123">Sie können QueryInterface für diese Schnittstelle aus dem Objekt, das [IWebView2WebView](IWebView2WebView.md)implementiert.</span><span class="sxs-lookup"><span data-stu-id="f91c8-123">You can QueryInterface for this interface from the object that implements [IWebView2WebView](IWebView2WebView.md).</span></span> <span data-ttu-id="f91c8-124">Weitere Informationen finden Sie auf der [IWebView2WebView](IWebView2WebView.md) -Benutzeroberfläche.</span><span class="sxs-lookup"><span data-stu-id="f91c8-124">See the [IWebView2WebView](IWebView2WebView.md) interface for more details.</span></span>

## <span data-ttu-id="f91c8-125">Member</span><span class="sxs-lookup"><span data-stu-id="f91c8-125">Members</span></span>

#### <span data-ttu-id="f91c8-126">Stop</span><span class="sxs-lookup"><span data-stu-id="f91c8-126">Stop</span></span> 

<span data-ttu-id="f91c8-127">Beenden Sie alle Navigations-und ausstehenden Ressourcen Abrufe.</span><span class="sxs-lookup"><span data-stu-id="f91c8-127">Stop all navigations and pending resource fetches.</span></span>

> <span data-ttu-id="f91c8-128">öffentlicher HRESULT- [Stopp](#stop)()</span><span class="sxs-lookup"><span data-stu-id="f91c8-128">public HRESULT [Stop](#stop)()</span></span>

#### <span data-ttu-id="f91c8-129">add_NewWindowRequested</span><span class="sxs-lookup"><span data-stu-id="f91c8-129">add_NewWindowRequested</span></span> 

<span data-ttu-id="f91c8-130">Fügen Sie einen Ereignishandler für das mswebviewnewwindowrequested-Ereignis hinzu.</span><span class="sxs-lookup"><span data-stu-id="f91c8-130">Add an event handler for the NewWindowRequested event.</span></span>

> <span data-ttu-id="f91c8-131">Public HRESULT [add_NewWindowRequested](#add_newwindowrequested)([IWebView2NewWindowRequestedEventHandler](IWebView2NewWindowRequestedEventHandler.md) \* EventHandler, EventRegistrationToken \* Token)</span><span class="sxs-lookup"><span data-stu-id="f91c8-131">public HRESULT [add_NewWindowRequested](#add_newwindowrequested)([IWebView2NewWindowRequestedEventHandler](IWebView2NewWindowRequestedEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="f91c8-132">Wird ausgelöst, wenn der Inhalt in der WebView zum Öffnen eines neuen Fensters angefordert wird, beispielsweisedurch Window. Open.</span><span class="sxs-lookup"><span data-stu-id="f91c8-132">Fires when content inside the WebView requested to open a new window, such as through window.open.</span></span> <span data-ttu-id="f91c8-133">Die APP kann eine Ziel-WebView übergeben, die als das geöffnete Fenster angesehen wird.</span><span class="sxs-lookup"><span data-stu-id="f91c8-133">The app can pass a target webview that will be considered the opened window.</span></span>

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

#### <span data-ttu-id="f91c8-134">remove_NewWindowRequested</span><span class="sxs-lookup"><span data-stu-id="f91c8-134">remove_NewWindowRequested</span></span> 

<span data-ttu-id="f91c8-135">Entfernen Sie einen Ereignishandler, der zuvor mit add_NewWindowRequested hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="f91c8-135">Remove an event handler previously added with add_NewWindowRequested.</span></span>

> <span data-ttu-id="f91c8-136">Public HRESULT [remove_NewWindowRequested](#remove_newwindowrequested)(EventRegistrationToken-Token)</span><span class="sxs-lookup"><span data-stu-id="f91c8-136">public HRESULT [remove_NewWindowRequested](#remove_newwindowrequested)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="f91c8-137">add_DocumentTitleChanged</span><span class="sxs-lookup"><span data-stu-id="f91c8-137">add_DocumentTitleChanged</span></span> 

<span data-ttu-id="f91c8-138">Fügen Sie einen Ereignishandler für das DocumentTitleChanged-Ereignis hinzu.</span><span class="sxs-lookup"><span data-stu-id="f91c8-138">Add an event handler for the DocumentTitleChanged event.</span></span>

> <span data-ttu-id="f91c8-139">Public HRESULT [add_DocumentTitleChanged](#add_documenttitlechanged)([IWebView2DocumentTitleChangedEventHandler](IWebView2DocumentTitleChangedEventHandler.md) \* EventHandler, EventRegistrationToken \* Token)</span><span class="sxs-lookup"><span data-stu-id="f91c8-139">public HRESULT [add_DocumentTitleChanged](#add_documenttitlechanged)([IWebView2DocumentTitleChangedEventHandler](IWebView2DocumentTitleChangedEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="f91c8-140">Das Ereignis wird ausgelöst, wenn die DocumentTitle-Eigenschaft des WebView-Ereignisses geändert wird und möglicherweise vor oder nach dem NavigationCompleted-Ereignis ausgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="f91c8-140">The event fires when the DocumentTitle property of the WebView changes and may fire before or after the NavigationCompleted event.</span></span>

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

#### <span data-ttu-id="f91c8-141">remove_DocumentTitleChanged</span><span class="sxs-lookup"><span data-stu-id="f91c8-141">remove_DocumentTitleChanged</span></span> 

<span data-ttu-id="f91c8-142">Entfernen Sie einen Ereignishandler, der zuvor mit add_DocumentTitleChanged hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="f91c8-142">Remove an event handler previously added with add_DocumentTitleChanged.</span></span>

> <span data-ttu-id="f91c8-143">Public HRESULT [remove_DocumentTitleChanged](#remove_documenttitlechanged)(EventRegistrationToken-Token)</span><span class="sxs-lookup"><span data-stu-id="f91c8-143">public HRESULT [remove_DocumentTitleChanged](#remove_documenttitlechanged)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="f91c8-144">get_DocumentTitle</span><span class="sxs-lookup"><span data-stu-id="f91c8-144">get_DocumentTitle</span></span> 

<span data-ttu-id="f91c8-145">Der Titel für das aktuelle Dokument der obersten Ebene.</span><span class="sxs-lookup"><span data-stu-id="f91c8-145">The title for the current top level document.</span></span>

> <span data-ttu-id="f91c8-146">öffentliche HRESULT- [get_DocumentTitle](#get_documenttitle)(LPWSTR \* Title)</span><span class="sxs-lookup"><span data-stu-id="f91c8-146">public HRESULT [get_DocumentTitle](#get_documenttitle)(LPWSTR \* title)</span></span>

<span data-ttu-id="f91c8-147">Wenn das Dokument keinen expliziten Titel hat oder sonst leer ist, wird ein Standardwert verwendet, der möglicherweise nicht mit dem URI des Dokuments übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="f91c8-147">If the document has no explicit title or is otherwise empty, a default that may or may not match the URI of the document will be used.</span></span>

