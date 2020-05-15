---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: Microsoft Edge-WebView2 für Win32-apps
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/26/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Host, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: 2f376cdd7098c512a8c7a0a3a463f5302f0bfbd7
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/14/2020
ms.locfileid: "10654144"
---
# <span data-ttu-id="fc077-104">Schnittstellen ICoreWebView2Environment</span><span class="sxs-lookup"><span data-stu-id="fc077-104">interface ICoreWebView2Environment</span></span> 

> [!NOTE]
> <span data-ttu-id="fc077-105">Diese Schnittstelle kann nach der SDK-Version 0.9.430 geändert oder für Versionen nicht verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="fc077-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="fc077-106">Die neueste API-Referenz finden Sie unter [Referenz](../../../webview2-api-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="fc077-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2Environment
  : public IUnknown
```

<span data-ttu-id="fc077-107">Dies stellt die WebView2-Umgebung dar.</span><span class="sxs-lookup"><span data-stu-id="fc077-107">This represents the WebView2 Environment.</span></span>

## <span data-ttu-id="fc077-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="fc077-108">Summary</span></span>

 <span data-ttu-id="fc077-109">Member</span><span class="sxs-lookup"><span data-stu-id="fc077-109">Members</span></span>                        | <span data-ttu-id="fc077-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="fc077-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="fc077-111">CreateCoreWebView2Host</span><span class="sxs-lookup"><span data-stu-id="fc077-111">CreateCoreWebView2Host</span></span>](#createcorewebview2host) | <span data-ttu-id="fc077-112">Erstellen Sie einen neuen WebView asynchron.</span><span class="sxs-lookup"><span data-stu-id="fc077-112">Asynchronously create a new WebView.</span></span>
[<span data-ttu-id="fc077-113">CreateWebResourceResponse</span><span class="sxs-lookup"><span data-stu-id="fc077-113">CreateWebResourceResponse</span></span>](#createwebresourceresponse) | <span data-ttu-id="fc077-114">Erstellen Sie ein neues Webressourcen-Antwortobjekt.</span><span class="sxs-lookup"><span data-stu-id="fc077-114">Create a new web resource response object.</span></span>
[<span data-ttu-id="fc077-115">get_BrowserVersionInfo</span><span class="sxs-lookup"><span data-stu-id="fc077-115">get_BrowserVersionInfo</span></span>](#get_browserversioninfo) | <span data-ttu-id="fc077-116">Die Browser Versionsinformationen des aktuellen [ICoreWebView2Environment](), einschließlich des Kanal namens, wenn es sich nicht um den stabilen Kanal handelt.</span><span class="sxs-lookup"><span data-stu-id="fc077-116">The browser version info of the current [ICoreWebView2Environment](), including channel name if it is not the stable channel.</span></span>
[<span data-ttu-id="fc077-117">add_NewBrowserVersionAvailable</span><span class="sxs-lookup"><span data-stu-id="fc077-117">add_NewBrowserVersionAvailable</span></span>](#add_newbrowserversionavailable) | <span data-ttu-id="fc077-118">Das NewBrowserVersionAvailable-Ereignis wird ausgelöst, wenn eine neuere Version des Edge-Browsers installiert ist und über WebView2 zur Verwendung zur Verfügung steht.</span><span class="sxs-lookup"><span data-stu-id="fc077-118">The NewBrowserVersionAvailable event fires when a newer version of the Edge browser is installed and available to use via WebView2.</span></span>
[<span data-ttu-id="fc077-119">remove_NewBrowserVersionAvailable</span><span class="sxs-lookup"><span data-stu-id="fc077-119">remove_NewBrowserVersionAvailable</span></span>](#remove_newbrowserversionavailable) | <span data-ttu-id="fc077-120">Entfernen Sie einen Ereignishandler, der zuvor mit add_NewBrowserVersionAvailable hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="fc077-120">Remove an event handler previously added with add_NewBrowserVersionAvailable.</span></span>

<span data-ttu-id="fc077-121">Webansichten, die aus einer Umgebung erstellt wurden, die im Browser Prozess ausgeführt wird, der mit Umgebungsparametern und aus einer Umgebung erstellten Objekten erstellt wurde, sollten in derselben Umgebung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="fc077-121">WebViews created from an environment run on the Browser process specified with environment parameters and objects created from an environment should be used in the same environment.</span></span> <span data-ttu-id="fc077-122">Die Verwendung in unterschiedlichen Umgebungen ist nicht garantiert kompatibel und kann fehlerhaft sein.</span><span class="sxs-lookup"><span data-stu-id="fc077-122">Using it in different environments are not guaranteed to be compatible and may fail.</span></span>

## <span data-ttu-id="fc077-123">Member</span><span class="sxs-lookup"><span data-stu-id="fc077-123">Members</span></span>

#### <span data-ttu-id="fc077-124">CreateCoreWebView2Host</span><span class="sxs-lookup"><span data-stu-id="fc077-124">CreateCoreWebView2Host</span></span> 

<span data-ttu-id="fc077-125">Erstellen Sie einen neuen WebView asynchron.</span><span class="sxs-lookup"><span data-stu-id="fc077-125">Asynchronously create a new WebView.</span></span>

> <span data-ttu-id="fc077-126">Public HRESULT [CreateCoreWebView2Host](#createcorewebview2host)(HWND ParentWindow,[ICoreWebView2CreateCoreWebView2HostCompletedHandler](ICoreWebView2CreateCoreWebView2HostCompletedHandler.md) \* Handler)</span><span class="sxs-lookup"><span data-stu-id="fc077-126">public HRESULT [CreateCoreWebView2Host](#createcorewebview2host)(HWND parentWindow,[ICoreWebView2CreateCoreWebView2HostCompletedHandler](ICoreWebView2CreateCoreWebView2HostCompletedHandler.md) \* handler)</span></span>

<span data-ttu-id="fc077-127">ParentWindow ist das HWND, in dem die WebView-Ansicht angezeigt werden soll und von der die Eingabe empfangen werden soll.</span><span class="sxs-lookup"><span data-stu-id="fc077-127">parentWindow is the HWND in which the WebView should be displayed and from which receive input.</span></span> <span data-ttu-id="fc077-128">Die WebView fügt dem bereitgestellten Fenster während der Erstellung von WebView ein untergeordnetes Fenster hinzu.</span><span class="sxs-lookup"><span data-stu-id="fc077-128">The WebView will add a child window to the provided window during WebView creation.</span></span> <span data-ttu-id="fc077-129">Die Z-Reihenfolge und andere Elemente, die von der Reihenfolge der nebengeordneten Fenster beeinflusst werden, sind dementsprechend betroffen.</span><span class="sxs-lookup"><span data-stu-id="fc077-129">Z-order and other things impacted by sibling window order will be affected accordingly.</span></span>

<span data-ttu-id="fc077-130">Es wird empfohlen, die Anwendungsbenutzer Modell-ID für den Prozess oder das Anwendungsfenster festzulegen.</span><span class="sxs-lookup"><span data-stu-id="fc077-130">It is recommended that the application set Application User Model ID for the process or the application window.</span></span> <span data-ttu-id="fc077-131">Wenn None gesetzt ist, wird bei der Erstellung von WebView eine generierte Anwendungsbenutzer Modell-ID auf das Stammfenster von ParentWindow eingestellt.</span><span class="sxs-lookup"><span data-stu-id="fc077-131">If none is set, during WebView creation a generated Application User Model ID is set to root window of parentWindow.</span></span> 

```cpp
// Create or recreate the WebView and its environment.
void AppWindow::InitializeWebView()
{
    // To ensure browser switches get applied correctly, we need to close
    // the existing WebView. This will result in a new browser process
    // getting created which will apply the browser switches.
    CloseWebView();

    LPCWSTR subFolder = nullptr;
    LPCWSTR additionalBrowserSwitches = nullptr;
    HRESULT hr = CreateCoreWebView2EnvironmentWithDetails(
        subFolder, nullptr, additionalBrowserSwitches,
        Callback<ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler>(
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
    HRESULT result, ICoreWebView2Environment* environment)
{
    CHECK_FAILURE(result);

    CHECK_FAILURE(environment->QueryInterface(IID_PPV_ARGS(&m_webViewEnvironment)));
        CHECK_FAILURE(m_webViewEnvironment->CreateCoreWebView2Host(
            m_mainWindow, Callback<ICoreWebView2CreateCoreWebView2HostCompletedHandler>(
                              this, &AppWindow::OnCreateCoreWebView2HostCompleted)
                              .Get()));
    return S_OK;
}
```

 <span data-ttu-id="fc077-132">Es wird empfohlen, dass die Anwendung Neustart-Manager-Nachrichten verarbeitet, damit Sie ordnungsgemäß neu gestartet werden kann, wenn die APP Edge für WebView aus einer bestimmten Installation verwendet und die Installation deinstalliert wird.</span><span class="sxs-lookup"><span data-stu-id="fc077-132">It is recommended that the application handles restart manager messages so that it can be restarted gracefully in the case when the app is using Edge for webview from a certain installation and that installation is being uninstalled.</span></span> <span data-ttu-id="fc077-133">Wenn ein Benutzer beispielsweise Edge from dev Channel installiert und sich entscheidet, Edge aus diesem Kanal zum Testen der APP zu verwenden, und dann Edge aus diesem Kanal deinstalliert, ohne die APP zu schließen, wird die APP neu gestartet, damit die Deinstallation des dev-Kanals erfolgreich ausgeführt werden kann.</span><span class="sxs-lookup"><span data-stu-id="fc077-133">For example, if a user installs Edge from Dev channel and opts to use Edge from that channel for testing the app, and then uninstalls Edge from that channel without closing the app, the app will be restarted to allow uninstallation of the dev channel to succeed.</span></span> 

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

#### <span data-ttu-id="fc077-134">CreateWebResourceResponse</span><span class="sxs-lookup"><span data-stu-id="fc077-134">CreateWebResourceResponse</span></span> 

<span data-ttu-id="fc077-135">Erstellen Sie ein neues Webressourcen-Antwortobjekt.</span><span class="sxs-lookup"><span data-stu-id="fc077-135">Create a new web resource response object.</span></span>

> <span data-ttu-id="fc077-136">Public HRESULT [CreateWebResourceResponse](#createwebresourceresponse)(IStream \* Content, int Statuscode, LPCWSTR reasonPhrase, LPCWSTR Headers,[ICoreWebView2WebResourceResponse](ICoreWebView2WebResourceResponse.md) \* \* Response)</span><span class="sxs-lookup"><span data-stu-id="fc077-136">public HRESULT [CreateWebResourceResponse](#createwebresourceresponse)(IStream \* content,int statusCode,LPCWSTR reasonPhrase,LPCWSTR headers,[ICoreWebView2WebResourceResponse](ICoreWebView2WebResourceResponse.md) \*\* response)</span></span>

<span data-ttu-id="fc077-137">Die Kopfzeilen ist die unformatierte Antwortheader Zeichenfolge, die durch einen Zeilenumbruch getrennt ist.</span><span class="sxs-lookup"><span data-stu-id="fc077-137">The headers is the raw response header string delimited by newline.</span></span> <span data-ttu-id="fc077-138">Es ist auch möglich, dieses Objekt mit einer leeren Headerzeichenfolge zu erstellen und dann die Kopfzeilen Zeile für Zeile mithilfe der [ICoreWebView2HttpResponseHeaders](ICoreWebView2HttpResponseHeaders.md) zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="fc077-138">It's also possible to create this object with empty headers string and then use the [ICoreWebView2HttpResponseHeaders](ICoreWebView2HttpResponseHeaders.md) to construct the headers line by line.</span></span> <span data-ttu-id="fc077-139">Informationen zu anderen Parametern finden Sie unter [ICoreWebView2WebResourceResponse](ICoreWebView2WebResourceResponse.md).</span><span class="sxs-lookup"><span data-stu-id="fc077-139">For information on other parameters see [ICoreWebView2WebResourceResponse](ICoreWebView2WebResourceResponse.md).</span></span>

```cpp
        if (m_blockImages)
        {
            m_webView->AddWebResourceRequestedFilter(L"*", CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_IMAGE);
            CHECK_FAILURE(m_webView->add_WebResourceRequested(
                Callback<ICoreWebView2WebResourceRequestedEventHandler>(
                    [this](
                        ICoreWebView2* sender,
                        ICoreWebView2WebResourceRequestedEventArgs* args) {
                        CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT resourceContext;
                        CHECK_FAILURE(
                            args->get_ResourceContext(&resourceContext));
                        // Ensure that the type is image
                        if (resourceContext != CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_IMAGE)
                        {
                            return E_INVALIDARG;
                        }
                        // Override the response with an empty one to block the image.
                        // If put_Response is not called, the request will continue as normal.
                        wil::com_ptr<ICoreWebView2WebResourceResponse> response;
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

#### <span data-ttu-id="fc077-140">get_BrowserVersionInfo</span><span class="sxs-lookup"><span data-stu-id="fc077-140">get_BrowserVersionInfo</span></span> 

<span data-ttu-id="fc077-141">Die Browser Versionsinformationen des aktuellen [ICoreWebView2Environment](), einschließlich des Kanal namens, wenn es sich nicht um den stabilen Kanal handelt.</span><span class="sxs-lookup"><span data-stu-id="fc077-141">The browser version info of the current [ICoreWebView2Environment](), including channel name if it is not the stable channel.</span></span>

> <span data-ttu-id="fc077-142">Public HRESULT [get_BrowserVersionInfo](#get_browserversioninfo)(LPWSTR \* VERSIONINFO)</span><span class="sxs-lookup"><span data-stu-id="fc077-142">public HRESULT [get_BrowserVersionInfo](#get_browserversioninfo)(LPWSTR \* versionInfo)</span></span>

<span data-ttu-id="fc077-143">Dies entspricht dem Format der GetCoreWebView2BrowserVersionInfo-API.</span><span class="sxs-lookup"><span data-stu-id="fc077-143">This matches the format of the GetCoreWebView2BrowserVersionInfo API.</span></span> <span data-ttu-id="fc077-144">Kanalnamen sind "Beta", "dev" und "Canary".</span><span class="sxs-lookup"><span data-stu-id="fc077-144">Channel names are 'beta', 'dev', and 'canary'.</span></span>

```cpp
        wil::unique_cotaskmem_string version_info;
        m_webViewEnvironment->get_BrowserVersionInfo(&version_info);
        MessageBox(
            m_mainWindow, version_info.get(), L"Browser Version Info After WebView Creation",
            MB_OK);
```

#### <span data-ttu-id="fc077-145">add_NewBrowserVersionAvailable</span><span class="sxs-lookup"><span data-stu-id="fc077-145">add_NewBrowserVersionAvailable</span></span> 

<span data-ttu-id="fc077-146">Das NewBrowserVersionAvailable-Ereignis wird ausgelöst, wenn eine neuere Version des Edge-Browsers installiert ist und über WebView2 zur Verwendung zur Verfügung steht.</span><span class="sxs-lookup"><span data-stu-id="fc077-146">The NewBrowserVersionAvailable event fires when a newer version of the Edge browser is installed and available to use via WebView2.</span></span>

> <span data-ttu-id="fc077-147">Public HRESULT [add_NewBrowserVersionAvailable](#add_newbrowserversionavailable)([ICoreWebView2NewBrowserVersionAvailableEventHandler](ICoreWebView2NewBrowserVersionAvailableEventHandler.md) \* EventHandler, EventRegistrationToken \* Token)</span><span class="sxs-lookup"><span data-stu-id="fc077-147">public HRESULT [add_NewBrowserVersionAvailable](#add_newbrowserversionavailable)([ICoreWebView2NewBrowserVersionAvailableEventHandler](ICoreWebView2NewBrowserVersionAvailableEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="fc077-148">Wenn Sie die neuere Version des Browsers verwenden möchten, müssen Sie eine neue Umgebung und WebView erstellen.</span><span class="sxs-lookup"><span data-stu-id="fc077-148">To use the newer version of the browser you must create a new environment and WebView.</span></span> <span data-ttu-id="fc077-149">Dieses Ereignis wird nur für eine neue Version aus dem gleichen Edge-Kanal ausgelöst, von dem aus der Code ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="fc077-149">This event will only be fired for new version from the same Edge channel that the code is running from.</span></span> <span data-ttu-id="fc077-150">Wenn Sie nicht mit installiertem Edge ausgeführt wird, wird kein Ereignis ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="fc077-150">When not running with installed Edge, no event will be fired.</span></span>

<span data-ttu-id="fc077-151">Da ein benutzerdatenordner nur von einem Browserprozess gleichzeitig verwendet werden kann, wenn Sie denselben benutzerdatenordner in den Webansichten mithilfe der neuen Browserversion verwenden möchten, müssen Sie die Umgebung und Webansichten schließen, die zuerst die ältere Version des Browsers verwenden.</span><span class="sxs-lookup"><span data-stu-id="fc077-151">Because a user data folder can only be used by one browser process at a time, if you want to use the same user data folder in the WebViews using the new version of the browser, you must close the environment and WebViews that are using the older version of the browser first.</span></span> <span data-ttu-id="fc077-152">Oder fordern Sie den Benutzer einfach auf, die APP neu zu starten.</span><span class="sxs-lookup"><span data-stu-id="fc077-152">Or simply prompt the user to restart the app.</span></span>

```cpp
    // After the environment is successfully created,
    // register a handler for the NewBrowserVersionAvailable event.
    // This handler tells when there is a new Edge version available on the machine.
    CHECK_FAILURE(m_webViewEnvironment->add_NewBrowserVersionAvailable(
        Callback<ICoreWebView2NewBrowserVersionAvailableEventHandler>(
            [this](
                ICoreWebView2Environment* sender,
                ICoreWebView2NewBrowserVersionAvailableEventArgs* args) -> HRESULT {
                // Get the version value from args
                wil::unique_cotaskmem_string newVersion;
                CHECK_FAILURE(args->get_NewVersion(&newVersion));
                std::wstring message = L"We detected there is a new version for the browser.";
                message += L"\n\nVersion number: ";
                message += newVersion.get();
                message += L"\n\n";
                if (m_webView)
                {
                    message += L"Do you want to restart the app? \n\n";
                    message += L"Click No if you only want to re-create the webviews. \n";
                    message += L"Click Cancel for no action. \n";
                }
                int response = MessageBox(
                    m_mainWindow, message.c_str(), L"New available version",
                    m_webView ? MB_YESNOCANCEL : MB_OK);

                if (response == IDYES)
                {
                    RestartApp();
                }
                else if (response == IDNO)
                {
                    ReinitializeWebViewWithNewBrowser();
                }
                else
                {
                    // do nothing
                }

                return S_OK;
            })
            .Get(),
        nullptr));
```

#### <span data-ttu-id="fc077-153">remove_NewBrowserVersionAvailable</span><span class="sxs-lookup"><span data-stu-id="fc077-153">remove_NewBrowserVersionAvailable</span></span> 

<span data-ttu-id="fc077-154">Entfernen Sie einen Ereignishandler, der zuvor mit add_NewBrowserVersionAvailable hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="fc077-154">Remove an event handler previously added with add_NewBrowserVersionAvailable.</span></span>

> <span data-ttu-id="fc077-155">Public HRESULT [remove_NewBrowserVersionAvailable](#remove_newbrowserversionavailable)(EventRegistrationToken-Token)</span><span class="sxs-lookup"><span data-stu-id="fc077-155">public HRESULT [remove_NewBrowserVersionAvailable](#remove_newbrowserversionavailable)(EventRegistrationToken token)</span></span>

