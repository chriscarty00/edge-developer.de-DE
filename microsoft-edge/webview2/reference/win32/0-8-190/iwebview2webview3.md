---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.8.355-WebView2 Win32 C++ IWebView2WebView3
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge
ms.openlocfilehash: a095b1ed085cd49a597195e01da21cde53b9095d
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884743"
---
# <span data-ttu-id="31986-104">0.8.355-Interface-IWebView2WebView3</span><span class="sxs-lookup"><span data-stu-id="31986-104">0.8.355 - interface IWebView2WebView3</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2WebView3
  : public IWebView2WebView
```

<span data-ttu-id="31986-105">Zusätzliche Funktionen, die vom primären WebView-Objekt implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="31986-105">Additional functionality implemented by the primary WebView object.</span></span>

## <span data-ttu-id="31986-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="31986-106">Summary</span></span>

 <span data-ttu-id="31986-107">Member</span><span class="sxs-lookup"><span data-stu-id="31986-107">Members</span></span>                        | <span data-ttu-id="31986-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="31986-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="31986-109">Stop</span><span class="sxs-lookup"><span data-stu-id="31986-109">Stop</span></span>](#stop) | <span data-ttu-id="31986-110">Beenden Sie alle Navigations-und ausstehenden Ressourcen Abrufe.</span><span class="sxs-lookup"><span data-stu-id="31986-110">Stop all navigations and pending resource fetches.</span></span>
[<span data-ttu-id="31986-111">add_NewWindowRequested</span><span class="sxs-lookup"><span data-stu-id="31986-111">add_NewWindowRequested</span></span>](#add_newwindowrequested) | <span data-ttu-id="31986-112">Fügen Sie einen Ereignishandler für das mswebviewnewwindowrequested-Ereignis hinzu.</span><span class="sxs-lookup"><span data-stu-id="31986-112">Add an event handler for the NewWindowRequested event.</span></span>
[<span data-ttu-id="31986-113">remove_NewWindowRequested</span><span class="sxs-lookup"><span data-stu-id="31986-113">remove_NewWindowRequested</span></span>](#remove_newwindowrequested) | <span data-ttu-id="31986-114">Entfernen Sie einen Ereignishandler, der zuvor mit add_NewWindowRequested hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="31986-114">Remove an event handler previously added with add_NewWindowRequested.</span></span>
[<span data-ttu-id="31986-115">add_DocumentTitleChanged</span><span class="sxs-lookup"><span data-stu-id="31986-115">add_DocumentTitleChanged</span></span>](#add_documenttitlechanged) | <span data-ttu-id="31986-116">Fügen Sie einen Ereignishandler für das DocumentTitleChanged-Ereignis hinzu.</span><span class="sxs-lookup"><span data-stu-id="31986-116">Add an event handler for the DocumentTitleChanged event.</span></span>
[<span data-ttu-id="31986-117">remove_DocumentTitleChanged</span><span class="sxs-lookup"><span data-stu-id="31986-117">remove_DocumentTitleChanged</span></span>](#remove_documenttitlechanged) | <span data-ttu-id="31986-118">Entfernen Sie einen Ereignishandler, der zuvor mit add_DocumentTitleChanged hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="31986-118">Remove an event handler previously added with add_DocumentTitleChanged.</span></span>
[<span data-ttu-id="31986-119">get_DocumentTitle</span><span class="sxs-lookup"><span data-stu-id="31986-119">get_DocumentTitle</span></span>](#get_documenttitle) | <span data-ttu-id="31986-120">Der Titel für das aktuelle Dokument der obersten Ebene.</span><span class="sxs-lookup"><span data-stu-id="31986-120">The title for the current top level document.</span></span>

<span data-ttu-id="31986-121">Sie können QueryInterface für diese Schnittstelle aus dem Objekt, das [IWebView2WebView](IWebView2WebView.md)implementiert.</span><span class="sxs-lookup"><span data-stu-id="31986-121">You can QueryInterface for this interface from the object that implements [IWebView2WebView](IWebView2WebView.md).</span></span> <span data-ttu-id="31986-122">Weitere Informationen finden Sie auf der [IWebView2WebView](IWebView2WebView.md) -Benutzeroberfläche.</span><span class="sxs-lookup"><span data-stu-id="31986-122">See the [IWebView2WebView](IWebView2WebView.md) interface for more details.</span></span>

## <span data-ttu-id="31986-123">Member</span><span class="sxs-lookup"><span data-stu-id="31986-123">Members</span></span>

#### <span data-ttu-id="31986-124">Stop</span><span class="sxs-lookup"><span data-stu-id="31986-124">Stop</span></span> 

<span data-ttu-id="31986-125">Beenden Sie alle Navigations-und ausstehenden Ressourcen Abrufe.</span><span class="sxs-lookup"><span data-stu-id="31986-125">Stop all navigations and pending resource fetches.</span></span>

> <span data-ttu-id="31986-126">öffentlicher HRESULT- [Stopp](#stop)()</span><span class="sxs-lookup"><span data-stu-id="31986-126">public HRESULT [Stop](#stop)()</span></span>

#### <span data-ttu-id="31986-127">add_NewWindowRequested</span><span class="sxs-lookup"><span data-stu-id="31986-127">add_NewWindowRequested</span></span> 

<span data-ttu-id="31986-128">Fügen Sie einen Ereignishandler für das mswebviewnewwindowrequested-Ereignis hinzu.</span><span class="sxs-lookup"><span data-stu-id="31986-128">Add an event handler for the NewWindowRequested event.</span></span>

> <span data-ttu-id="31986-129">Public HRESULT [add_NewWindowRequested](#add_newwindowrequested)([IWebView2NewWindowRequestedEventHandler](IWebView2NewWindowRequestedEventHandler.md) \* EventHandler, EventRegistrationToken \* Token)</span><span class="sxs-lookup"><span data-stu-id="31986-129">public HRESULT [add_NewWindowRequested](#add_newwindowrequested)([IWebView2NewWindowRequestedEventHandler](IWebView2NewWindowRequestedEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="31986-130">Wird ausgelöst, wenn der Inhalt in der WebView zum Öffnen eines neuen Fensters angefordert wird, beispielsweisedurch Window. Open.</span><span class="sxs-lookup"><span data-stu-id="31986-130">Fires when content inside the WebView requested to open a new window, such as through window.open.</span></span> <span data-ttu-id="31986-131">Die APP kann eine Ziel-WebView übergeben, die als das geöffnete Fenster angesehen wird.</span><span class="sxs-lookup"><span data-stu-id="31986-131">The app can pass a target webview that will be considered the opened window.</span></span>

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

#### <span data-ttu-id="31986-132">remove_NewWindowRequested</span><span class="sxs-lookup"><span data-stu-id="31986-132">remove_NewWindowRequested</span></span> 

<span data-ttu-id="31986-133">Entfernen Sie einen Ereignishandler, der zuvor mit add_NewWindowRequested hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="31986-133">Remove an event handler previously added with add_NewWindowRequested.</span></span>

> <span data-ttu-id="31986-134">Public HRESULT [remove_NewWindowRequested](#remove_newwindowrequested)(EventRegistrationToken-Token)</span><span class="sxs-lookup"><span data-stu-id="31986-134">public HRESULT [remove_NewWindowRequested](#remove_newwindowrequested)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="31986-135">add_DocumentTitleChanged</span><span class="sxs-lookup"><span data-stu-id="31986-135">add_DocumentTitleChanged</span></span> 

<span data-ttu-id="31986-136">Fügen Sie einen Ereignishandler für das DocumentTitleChanged-Ereignis hinzu.</span><span class="sxs-lookup"><span data-stu-id="31986-136">Add an event handler for the DocumentTitleChanged event.</span></span>

> <span data-ttu-id="31986-137">Public HRESULT [add_DocumentTitleChanged](#add_documenttitlechanged)([IWebView2DocumentTitleChangedEventHandler](IWebView2DocumentTitleChangedEventHandler.md) \* EventHandler, EventRegistrationToken \* Token)</span><span class="sxs-lookup"><span data-stu-id="31986-137">public HRESULT [add_DocumentTitleChanged](#add_documenttitlechanged)([IWebView2DocumentTitleChangedEventHandler](IWebView2DocumentTitleChangedEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="31986-138">Das Ereignis wird ausgelöst, wenn die DocumentTitle-Eigenschaft des WebView-Ereignisses geändert wird und möglicherweise vor oder nach dem NavigationCompleted-Ereignis ausgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="31986-138">The event fires when the DocumentTitle property of the WebView changes and may fire before or after the NavigationCompleted event.</span></span>

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

#### <span data-ttu-id="31986-139">remove_DocumentTitleChanged</span><span class="sxs-lookup"><span data-stu-id="31986-139">remove_DocumentTitleChanged</span></span> 

<span data-ttu-id="31986-140">Entfernen Sie einen Ereignishandler, der zuvor mit add_DocumentTitleChanged hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="31986-140">Remove an event handler previously added with add_DocumentTitleChanged.</span></span>

> <span data-ttu-id="31986-141">Public HRESULT [remove_DocumentTitleChanged](#remove_documenttitlechanged)(EventRegistrationToken-Token)</span><span class="sxs-lookup"><span data-stu-id="31986-141">public HRESULT [remove_DocumentTitleChanged](#remove_documenttitlechanged)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="31986-142">get_DocumentTitle</span><span class="sxs-lookup"><span data-stu-id="31986-142">get_DocumentTitle</span></span> 

<span data-ttu-id="31986-143">Der Titel für das aktuelle Dokument der obersten Ebene.</span><span class="sxs-lookup"><span data-stu-id="31986-143">The title for the current top level document.</span></span>

> <span data-ttu-id="31986-144">öffentliche HRESULT- [get_DocumentTitle](#get_documenttitle)(LPWSTR \* Title)</span><span class="sxs-lookup"><span data-stu-id="31986-144">public HRESULT [get_DocumentTitle](#get_documenttitle)(LPWSTR \* title)</span></span>

<span data-ttu-id="31986-145">Wenn das Dokument keinen expliziten Titel hat oder sonst leer ist, wird ein Standardwert verwendet, der möglicherweise nicht mit dem URI des Dokuments übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="31986-145">If the document has no explicit title or is otherwise empty, a default that may or may not match the URI of the document will be used.</span></span>

