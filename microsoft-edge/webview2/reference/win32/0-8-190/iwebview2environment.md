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
ms.openlocfilehash: c3ce6a49be1abf12d66f69da6d2ff6ff9d9f5b68
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/14/2020
ms.locfileid: "10654143"
---
# <span data-ttu-id="acbef-104">Schnittstellen IWebView2Environment</span><span class="sxs-lookup"><span data-stu-id="acbef-104">interface IWebView2Environment</span></span> 

> [!NOTE]
> <span data-ttu-id="acbef-105">Diese Schnittstelle kann nach der SDK-Version 0.8.355 geändert oder für Versionen nicht verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="acbef-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="acbef-106">Die neueste API-Referenz finden Sie unter [Referenz](../../../webview2-api-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="acbef-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2Environment
  : public IUnknown
```

<span data-ttu-id="acbef-107">Dies stellt die WebView2-Umgebung dar.</span><span class="sxs-lookup"><span data-stu-id="acbef-107">This represents the WebView2 Environment.</span></span>

## <span data-ttu-id="acbef-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="acbef-108">Summary</span></span>

 <span data-ttu-id="acbef-109">Member</span><span class="sxs-lookup"><span data-stu-id="acbef-109">Members</span></span>                        | <span data-ttu-id="acbef-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="acbef-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="acbef-111">WebView</span><span class="sxs-lookup"><span data-stu-id="acbef-111">CreateWebView</span></span>](#createwebview) | <span data-ttu-id="acbef-112">Erstellen Sie eine neue [IWebView2WebView](IWebView2WebView.md)asynchron.</span><span class="sxs-lookup"><span data-stu-id="acbef-112">Asynchronously create a new [IWebView2WebView](IWebView2WebView.md).</span></span>
[<span data-ttu-id="acbef-113">CreateWebResourceResponse</span><span class="sxs-lookup"><span data-stu-id="acbef-113">CreateWebResourceResponse</span></span>](#createwebresourceresponse) | <span data-ttu-id="acbef-114">Erstellen Sie ein neues Webressourcen-Antwortobjekt.</span><span class="sxs-lookup"><span data-stu-id="acbef-114">Create a new web resource response object.</span></span>

<span data-ttu-id="acbef-115">Webansichten, die aus einer Umgebung erstellt wurden, die im Browser Prozess ausgeführt wird, der mit Umgebungsparametern und aus einer Umgebung erstellten Objekten erstellt wurde, sollten in derselben Umgebung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="acbef-115">WebViews created from an environment run on the Browser process specified with environment parameters and objects created from an environment should be used in the same environment.</span></span> <span data-ttu-id="acbef-116">Die Verwendung in unterschiedlichen Umgebungen ist nicht garantiert kompatibel und kann fehlerhaft sein.</span><span class="sxs-lookup"><span data-stu-id="acbef-116">Using it in different environments are not guaranteed to be compatible and may fail.</span></span>

## <span data-ttu-id="acbef-117">Member</span><span class="sxs-lookup"><span data-stu-id="acbef-117">Members</span></span>

#### <span data-ttu-id="acbef-118">WebView</span><span class="sxs-lookup"><span data-stu-id="acbef-118">CreateWebView</span></span> 

<span data-ttu-id="acbef-119">Erstellen Sie eine neue [IWebView2WebView](IWebView2WebView.md)asynchron.</span><span class="sxs-lookup"><span data-stu-id="acbef-119">Asynchronously create a new [IWebView2WebView](IWebView2WebView.md).</span></span>

> <span data-ttu-id="acbef-120">öffentliche HRESULT [WebView](#createwebview)(HWND ParentWindow,[IWebView2CreateWebViewCompletedHandler](IWebView2CreateWebViewCompletedHandler.md) \*-Handler)</span><span class="sxs-lookup"><span data-stu-id="acbef-120">public HRESULT [CreateWebView](#createwebview)(HWND parentWindow,[IWebView2CreateWebViewCompletedHandler](IWebView2CreateWebViewCompletedHandler.md) \* handler)</span></span>

<span data-ttu-id="acbef-121">ParentWindow ist das HWND, in dem die WebView-Ansicht angezeigt werden soll und von der die Eingabe empfangen werden soll.</span><span class="sxs-lookup"><span data-stu-id="acbef-121">parentWindow is the HWND in which the WebView should be displayed and from which receive input.</span></span> <span data-ttu-id="acbef-122">Die WebView fügt dem bereitgestellten Fenster während der Erstellung von WebView ein untergeordnetes Fenster hinzu.</span><span class="sxs-lookup"><span data-stu-id="acbef-122">The WebView will add a child window to the provided window during WebView creation.</span></span> <span data-ttu-id="acbef-123">Die Z-Reihenfolge und andere Elemente, die von der Reihenfolge der nebengeordneten Fenster beeinflusst werden, sind dementsprechend betroffen.</span><span class="sxs-lookup"><span data-stu-id="acbef-123">Z-order and other things impacted by sibling window order will be affected accordingly.</span></span>

<span data-ttu-id="acbef-124">Es wird empfohlen, die Anwendungsbenutzer Modell-ID für den Prozess oder das Anwendungsfenster festzulegen.</span><span class="sxs-lookup"><span data-stu-id="acbef-124">It is recommended that the application set Application User Model ID for the process or the application window.</span></span> <span data-ttu-id="acbef-125">Wenn None gesetzt ist, wird bei der Erstellung von WebView eine generierte Anwendungsbenutzer Modell-ID auf das Stammfenster von ParentWindow eingestellt.</span><span class="sxs-lookup"><span data-stu-id="acbef-125">If none is set, during WebView creation a generated Application User Model ID is set to root window of parentWindow.</span></span> 

```cpp
// Create or recreate the WebView and its environment.
void AppWindow::InitializeWebView(InitializeWebViewFlags webviewInitFlags)
{
    m_lastUsedInitFlags = webviewInitFlags;
    // To ensure browser switches get applied correctly, we need to close
    // the existing WebView. This will result in a new browser process
    // getting created which will apply the browser switches.
    CloseWebView();

    LPCWSTR subFolder = nullptr;
    LPCWSTR additionalBrowserSwitches = nullptr;
    HRESULT hr = CreateWebView2EnvironmentWithDetails(
        subFolder, nullptr, additionalBrowserSwitches,
        Callback<IWebView2CreateWebView2EnvironmentCompletedHandler>(
            this, &AppWindow::OnCreateEnvironmentCompleted)
            .Get());
    if (!SUCCEEDED(hr))
    {
        if (hr == HRESULT_FROM_WIN32(ERROR_FILE_NOT_FOUND))
        {
            MessageBox(
                m_mainWindow,
                L"Couldn't find Edge installation. "
                "Do you have a version installed that's compatible with this "
                "WebView2 SDK version?",
                nullptr, MB_OK);
        }
        else
        {
            ShowFailure(hr, L"Failed to create webview environment");
        }
    }
}

// This is the callback passed to CreateWebViewEnvironmnetWithDetails.
// Here we simply create the WebView.
HRESULT AppWindow::OnCreateEnvironmentCompleted(
    HRESULT result, IWebView2Environment* environment)
{
    CHECK_FAILURE(result);

    CHECK_FAILURE(environment->QueryInterface(IID_PPV_ARGS(&m_webViewEnvironment)));
        CHECK_FAILURE(m_webViewEnvironment->CreateWebView(
            m_mainWindow, Callback<IWebView2CreateWebViewCompletedHandler>(
                              this, &AppWindow::OnCreateWebViewCompleted)
                              .Get()));
    return S_OK;
}
```

 <span data-ttu-id="acbef-126">Es wird empfohlen, dass die Anwendung Neustart-Manager-Nachrichten verarbeitet, damit Sie ordnungsgemäß neu gestartet werden kann, wenn die APP Edge für WebView aus einer bestimmten Installation verwendet und die Installation deinstalliert wird.</span><span class="sxs-lookup"><span data-stu-id="acbef-126">It is recommended that the application handles restart manager messages so that it can be restarted gracefully in the case when the app is using Edge for webview from a certain installation and that installation is being uninstalled.</span></span> <span data-ttu-id="acbef-127">Wenn ein Benutzer beispielsweise Edge from dev Channel installiert und sich entscheidet, Edge aus diesem Kanal zum Testen der APP zu verwenden, und dann Edge aus diesem Kanal deinstalliert, ohne die APP zu schließen, wird die APP neu gestartet, damit die Deinstallation des dev-Kanals erfolgreich ausgeführt werden kann.</span><span class="sxs-lookup"><span data-stu-id="acbef-127">For example, if a user installs Edge from Dev channel and opts to use Edge from that channel for testing the app, and then uninstalls Edge from that channel without closing the app, the app will be restarted to allow uninstallation of the dev channel to succeed.</span></span> 

```cpp
    case WM_QUERYENDSESSION:
    {
        // yes, we can shut down
        // Register how we might be restarted
        RegisterApplicationRestart(L"--restore", RESTART_NO_CRASH | RESTART_NO_HANG);
        *result = TRUE;
        return true;
    }
    break;
    case WM_ENDSESSION:
    {
        if (wParam == TRUE)
        {
            // save app state and exit.
            PostQuitMessage(0);
            return true;
        }
    }
    break;
```

#### <span data-ttu-id="acbef-128">CreateWebResourceResponse</span><span class="sxs-lookup"><span data-stu-id="acbef-128">CreateWebResourceResponse</span></span> 

<span data-ttu-id="acbef-129">Erstellen Sie ein neues Webressourcen-Antwortobjekt.</span><span class="sxs-lookup"><span data-stu-id="acbef-129">Create a new web resource response object.</span></span>

> <span data-ttu-id="acbef-130">Public HRESULT [CreateWebResourceResponse](#createwebresourceresponse)(IStream \* Content, int Statuscode, LPCWSTR reasonPhrase, LPCWSTR Headers,[IWebView2WebResourceResponse](IWebView2WebResourceResponse.md) \* \* Response)</span><span class="sxs-lookup"><span data-stu-id="acbef-130">public HRESULT [CreateWebResourceResponse](#createwebresourceresponse)(IStream \* content,int statusCode,LPCWSTR reasonPhrase,LPCWSTR headers,[IWebView2WebResourceResponse](IWebView2WebResourceResponse.md) \*\* response)</span></span>

<span data-ttu-id="acbef-131">Die Kopfzeilen ist die unformatierte Antwortheader Zeichenfolge, die durch einen Zeilenumbruch getrennt ist.</span><span class="sxs-lookup"><span data-stu-id="acbef-131">The headers is the raw response header string delimited by newline.</span></span> <span data-ttu-id="acbef-132">Es ist auch möglich, dieses Objekt mit einer leeren Headerzeichenfolge zu erstellen und dann die Kopfzeilen Zeile für Zeile mithilfe der [IWebView2HttpResponseHeaders](IWebView2HttpResponseHeaders.md) zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="acbef-132">It's also possible to create this object with empty headers string and then use the [IWebView2HttpResponseHeaders](IWebView2HttpResponseHeaders.md) to construct the headers line by line.</span></span> <span data-ttu-id="acbef-133">Informationen zu anderen Parametern finden Sie unter [IWebView2WebResourceResponse](IWebView2WebResourceResponse.md).</span><span class="sxs-lookup"><span data-stu-id="acbef-133">For information on other parameters see [IWebView2WebResourceResponse](IWebView2WebResourceResponse.md).</span></span>

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

