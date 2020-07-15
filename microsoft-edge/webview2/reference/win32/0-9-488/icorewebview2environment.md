---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2Environment
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: 590fb7b93543f6dfe6051c9ede1a1b2ec0dc1467
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/15/2020
ms.locfileid: "10880710"
---
# <span data-ttu-id="978dd-104">0.9.515-Interface-ICoreWebView2Environment</span><span class="sxs-lookup"><span data-stu-id="978dd-104">0.9.515 - interface ICoreWebView2Environment</span></span> 

> [!NOTE]
> <span data-ttu-id="978dd-105">Dieser Verweis kann für Versionen nach der SDK-Version 0.9.515 geändert oder nicht mehr zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="978dd-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="978dd-106">Die neueste API-Referenz finden Sie in der [WebView2-API-Referenz](../../../webview2-api-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="978dd-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2Environment
  : public IUnknown
```

<span data-ttu-id="978dd-107">Dies stellt die WebView2-Umgebung dar.</span><span class="sxs-lookup"><span data-stu-id="978dd-107">This represents the WebView2 Environment.</span></span>

## <span data-ttu-id="978dd-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="978dd-108">Summary</span></span>

 <span data-ttu-id="978dd-109">Member</span><span class="sxs-lookup"><span data-stu-id="978dd-109">Members</span></span>                        | <span data-ttu-id="978dd-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="978dd-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="978dd-111">add_NewBrowserVersionAvailable</span><span class="sxs-lookup"><span data-stu-id="978dd-111">add_NewBrowserVersionAvailable</span></span>](#add_newbrowserversionavailable) | <span data-ttu-id="978dd-112">Das NewBrowserVersionAvailable-Ereignis wird ausgelöst, wenn eine neuere Version des Edge-Browsers installiert ist und über WebView2 zur Verwendung zur Verfügung steht.</span><span class="sxs-lookup"><span data-stu-id="978dd-112">The NewBrowserVersionAvailable event fires when a newer version of the Edge browser is installed and available to use via WebView2.</span></span>
[<span data-ttu-id="978dd-113">CreateCoreWebView2Controller</span><span class="sxs-lookup"><span data-stu-id="978dd-113">CreateCoreWebView2Controller</span></span>](#createcorewebview2controller) | <span data-ttu-id="978dd-114">Erstellen Sie einen neuen WebView asynchron.</span><span class="sxs-lookup"><span data-stu-id="978dd-114">Asynchronously create a new WebView.</span></span>
[<span data-ttu-id="978dd-115">CreateWebResourceResponse</span><span class="sxs-lookup"><span data-stu-id="978dd-115">CreateWebResourceResponse</span></span>](#createwebresourceresponse) | <span data-ttu-id="978dd-116">Erstellen Sie ein neues Webressourcen-Antwortobjekt.</span><span class="sxs-lookup"><span data-stu-id="978dd-116">Create a new web resource response object.</span></span>
[<span data-ttu-id="978dd-117">get_BrowserVersionString</span><span class="sxs-lookup"><span data-stu-id="978dd-117">get_BrowserVersionString</span></span>](#get_browserversionstring) | <span data-ttu-id="978dd-118">Die Browser Versionsinformationen des aktuellen [ICoreWebView2Environment](), einschließlich des Kanal namens, wenn es sich nicht um den stabilen Kanal handelt.</span><span class="sxs-lookup"><span data-stu-id="978dd-118">The browser version info of the current [ICoreWebView2Environment](), including channel name if it is not the stable channel.</span></span>
[<span data-ttu-id="978dd-119">remove_NewBrowserVersionAvailable</span><span class="sxs-lookup"><span data-stu-id="978dd-119">remove_NewBrowserVersionAvailable</span></span>](#remove_newbrowserversionavailable) | <span data-ttu-id="978dd-120">Entfernen Sie einen Ereignishandler, der zuvor mit add_NewBrowserVersionAvailable hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="978dd-120">Remove an event handler previously added with add_NewBrowserVersionAvailable.</span></span>

<span data-ttu-id="978dd-121">Webansichten, die aus einer Umgebung erstellt wurden, die im Browser Prozess ausgeführt wird, der mit Umgebungsparametern und aus einer Umgebung erstellten Objekten erstellt wurde, sollten in derselben Umgebung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="978dd-121">WebViews created from an environment run on the Browser process specified with environment parameters and objects created from an environment should be used in the same environment.</span></span> <span data-ttu-id="978dd-122">Die Verwendung in unterschiedlichen Umgebungen ist nicht garantiert kompatibel und kann fehlerhaft sein.</span><span class="sxs-lookup"><span data-stu-id="978dd-122">Using it in different environments are not guaranteed to be compatible and may fail.</span></span>

## <span data-ttu-id="978dd-123">Member</span><span class="sxs-lookup"><span data-stu-id="978dd-123">Members</span></span>

#### <span data-ttu-id="978dd-124">add_NewBrowserVersionAvailable</span><span class="sxs-lookup"><span data-stu-id="978dd-124">add_NewBrowserVersionAvailable</span></span> 

<span data-ttu-id="978dd-125">Das NewBrowserVersionAvailable-Ereignis wird ausgelöst, wenn eine neuere Version des Edge-Browsers installiert ist und über WebView2 zur Verwendung zur Verfügung steht.</span><span class="sxs-lookup"><span data-stu-id="978dd-125">The NewBrowserVersionAvailable event fires when a newer version of the Edge browser is installed and available to use via WebView2.</span></span>

> <span data-ttu-id="978dd-126">Public HRESULT [add_NewBrowserVersionAvailable](#add_newbrowserversionavailable)([ICoreWebView2NewBrowserVersionAvailableEventHandler](icorewebview2newbrowserversionavailableeventhandler.md) \* EventHandler, EventRegistrationToken \* Token)</span><span class="sxs-lookup"><span data-stu-id="978dd-126">public HRESULT [add_NewBrowserVersionAvailable](#add_newbrowserversionavailable)([ICoreWebView2NewBrowserVersionAvailableEventHandler](icorewebview2newbrowserversionavailableeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="978dd-127">Wenn Sie die neuere Version des Browsers verwenden möchten, müssen Sie eine neue Umgebung und WebView erstellen.</span><span class="sxs-lookup"><span data-stu-id="978dd-127">To use the newer version of the browser you must create a new environment and WebView.</span></span> <span data-ttu-id="978dd-128">Dieses Ereignis wird nur für eine neue Version aus dem gleichen Edge-Kanal ausgelöst, von dem aus der Code ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="978dd-128">This event will only be fired for new version from the same Edge channel that the code is running from.</span></span> <span data-ttu-id="978dd-129">Wenn Sie nicht mit installiertem Edge ausgeführt wird, wird kein Ereignis ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="978dd-129">When not running with installed Edge, no event will be fired.</span></span>

<span data-ttu-id="978dd-130">Da ein benutzerdatenordner nur von einem Browserprozess gleichzeitig verwendet werden kann, wenn Sie denselben benutzerdatenordner in den Webansichten mithilfe der neuen Browserversion verwenden möchten, müssen Sie die Umgebung und Webansichten schließen, die zuerst die ältere Version des Browsers verwenden.</span><span class="sxs-lookup"><span data-stu-id="978dd-130">Because a user data folder can only be used by one browser process at a time, if you want to use the same user data folder in the WebViews using the new version of the browser, you must close the environment and WebViews that are using the older version of the browser first.</span></span> <span data-ttu-id="978dd-131">Oder fordern Sie den Benutzer einfach auf, die APP neu zu starten.</span><span class="sxs-lookup"><span data-stu-id="978dd-131">Or simply prompt the user to restart the app.</span></span>

```cpp
    // After the environment is successfully created,
    // register a handler for the NewBrowserVersionAvailable event.
    // This handler tells when there is a new Edge version available on the machine.
    CHECK_FAILURE(m_webViewEnvironment->add_NewBrowserVersionAvailable(
        Callback<ICoreWebView2NewBrowserVersionAvailableEventHandler>(
            [this](ICoreWebView2Environment* sender, IUnknown* args) -> HRESULT {
                std::wstring message = L"We detected there is a new version for the browser.";
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

#### <span data-ttu-id="978dd-132">CreateCoreWebView2Controller</span><span class="sxs-lookup"><span data-stu-id="978dd-132">CreateCoreWebView2Controller</span></span> 

<span data-ttu-id="978dd-133">Erstellen Sie einen neuen WebView asynchron.</span><span class="sxs-lookup"><span data-stu-id="978dd-133">Asynchronously create a new WebView.</span></span>

> <span data-ttu-id="978dd-134">Public HRESULT [CreateCoreWebView2Controller](#createcorewebview2controller)(HWND ParentWindow, [ICoreWebView2CreateCoreWebView2ControllerCompletedHandler](icorewebview2createcorewebview2controllercompletedhandler.md) \* Handler)</span><span class="sxs-lookup"><span data-stu-id="978dd-134">public HRESULT [CreateCoreWebView2Controller](#createcorewebview2controller)(HWND parentWindow, [ICoreWebView2CreateCoreWebView2ControllerCompletedHandler](icorewebview2createcorewebview2controllercompletedhandler.md) \* handler)</span></span>

<span data-ttu-id="978dd-135">ParentWindow ist das HWND, in dem die WebView-Ansicht angezeigt werden soll und von der die Eingabe empfangen werden soll.</span><span class="sxs-lookup"><span data-stu-id="978dd-135">parentWindow is the HWND in which the WebView should be displayed and from which receive input.</span></span> <span data-ttu-id="978dd-136">Die WebView fügt dem bereitgestellten Fenster während der Erstellung von WebView ein untergeordnetes Fenster hinzu.</span><span class="sxs-lookup"><span data-stu-id="978dd-136">The WebView will add a child window to the provided window during WebView creation.</span></span> <span data-ttu-id="978dd-137">Die Z-Reihenfolge und andere Elemente, die von der Reihenfolge der nebengeordneten Fenster beeinflusst werden, sind dementsprechend betroffen.</span><span class="sxs-lookup"><span data-stu-id="978dd-137">Z-order and other things impacted by sibling window order will be affected accordingly.</span></span>

<span data-ttu-id="978dd-138">Es wird empfohlen, die Anwendungsbenutzer Modell-ID für den Prozess oder das Anwendungsfenster festzulegen.</span><span class="sxs-lookup"><span data-stu-id="978dd-138">It is recommended that the application set Application User Model ID for the process or the application window.</span></span> <span data-ttu-id="978dd-139">Wenn None gesetzt ist, wird bei der Erstellung von WebView eine generierte Anwendungsbenutzer Modell-ID auf das Stammfenster von ParentWindow eingestellt.</span><span class="sxs-lookup"><span data-stu-id="978dd-139">If none is set, during WebView creation a generated Application User Model ID is set to root window of parentWindow.</span></span> 
```cpp
// Create or recreate the WebView and its environment.
void AppWindow::InitializeWebView()
{
    // To ensure browser switches get applied correctly, we need to close
    // the existing WebView. This will result in a new browser process
    // getting created which will apply the browser switches.
    CloseWebView();
    m_dcompDevice = nullptr;
    m_wincompHelper = nullptr;

    LPCWSTR subFolder = nullptr;

    if (m_creationModeId == IDM_CREATION_MODE_VISUAL_DCOMP)
    {
        HRESULT hr = DCompositionCreateDevice2(nullptr, IID_PPV_ARGS(&m_dcompDevice));
        if (!SUCCEEDED(hr))
        {
            MessageBox(
                m_mainWindow,
                L"Attempting to create WebView using DComp Visual is not supported.\r\n"
                "DComp device creation failed.\r\n"
                "Current OS may not support DComp.",
                L"Create with Windowless DComp Visual Failed", MB_OK);
            return;
        }
    }
    else if (m_creationModeId == IDM_CREATION_MODE_VISUAL_WINCOMP)
    {
        HRESULT hr = CreateWinCompCompositor();
        if (!SUCCEEDED(hr))
        {
            MessageBox(
                m_mainWindow,
                L"Attempting to create WebView using WinComp Visual is not supported.\r\n"
                "WinComp compositor creation failed.\r\n"
                "Current OS may not support WinComp.",
                L"Create with Windowless WinComp Visual Failed", MB_OK);
            return;
        }
    }
    auto options = Microsoft::WRL::Make<CoreWebView2EnvironmentOptions>();
    if(!m_language.empty())
        CHECK_FAILURE(options->put_Language(m_language.c_str()));
    HRESULT hr = CreateCoreWebView2EnvironmentWithOptions(
        subFolder, nullptr, options.Get(),
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

// This is the callback passed to CreateWebViewEnvironmentWithOptions.
// Here we simply create the WebView.
HRESULT AppWindow::OnCreateEnvironmentCompleted(
    HRESULT result, ICoreWebView2Environment* environment)
{
    CHECK_FAILURE(result);

    m_webViewEnvironment = environment;

    auto webViewExperimentalEnvironment =
        m_webViewEnvironment.try_query<ICoreWebView2ExperimentalEnvironment>();
    if (webViewExperimentalEnvironment && (m_dcompDevice || m_wincompHelper))
    {
        CHECK_FAILURE(webViewExperimentalEnvironment->CreateCoreWebView2CompositionController(
            m_mainWindow,
            Callback<
                ICoreWebView2ExperimentalCreateCoreWebView2CompositionControllerCompletedHandler>(
                [this](
                    HRESULT result,
                    ICoreWebView2ExperimentalCompositionController* compositionController) -> HRESULT {
                    auto controller =
                        wil::com_ptr<ICoreWebView2ExperimentalCompositionController>(compositionController)
                            .query<ICoreWebView2Controller>();
                    return OnCreateCoreWebView2ControllerCompleted(result, controller.get());
                })
                .Get()));
    }
    else
    {
        CHECK_FAILURE(m_webViewEnvironment->CreateCoreWebView2Controller(
            m_mainWindow, Callback<ICoreWebView2CreateCoreWebView2ControllerCompletedHandler>(
                              this, &AppWindow::OnCreateCoreWebView2ControllerCompleted)
                              .Get()));
    }

    return S_OK;
}
```
 <span data-ttu-id="978dd-140">Es wird empfohlen, dass die Anwendung Neustart-Manager-Nachrichten verarbeitet, damit Sie ordnungsgemäß neu gestartet werden kann, wenn die APP Edge für WebView aus einer bestimmten Installation verwendet und die Installation deinstalliert wird.</span><span class="sxs-lookup"><span data-stu-id="978dd-140">It is recommended that the application handles restart manager messages so that it can be restarted gracefully in the case when the app is using Edge for webview from a certain installation and that installation is being uninstalled.</span></span> <span data-ttu-id="978dd-141">Wenn ein Benutzer beispielsweise Edge from dev Channel installiert und sich entscheidet, Edge aus diesem Kanal zum Testen der APP zu verwenden, und dann Edge aus diesem Kanal deinstalliert, ohne die APP zu schließen, wird die APP neu gestartet, damit die Deinstallation des dev-Kanals erfolgreich ausgeführt werden kann.</span><span class="sxs-lookup"><span data-stu-id="978dd-141">For example, if a user installs Edge from Dev channel and opts to use Edge from that channel for testing the app, and then uninstalls Edge from that channel without closing the app, the app will be restarted to allow uninstallation of the dev channel to succeed.</span></span> 
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
 <span data-ttu-id="978dd-142">Wenn die Anwendung CreateCoreWebView2Controller bei einem Fehler erneut versucht, wird empfohlen, dass die Anwendung neu gestartet wird, indem eine neue WebView2-Umgebung erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="978dd-142">When the application retries CreateCoreWebView2Controller upon failure, it is recommended that the application restarts from creating a new WebView2 Environment.</span></span> <span data-ttu-id="978dd-143">Wenn eine Edge-Aktualisierung durchgeführt wird, könnte die Version, die mit einer WebView2-Umgebung verknüpft ist, entfernt worden sein und dazu führen, dass das Objekt nicht mehr funktioniert.</span><span class="sxs-lookup"><span data-stu-id="978dd-143">If an Edge update happens, the version associated with a WebView2 Environment could have been removed and causing the object to no longer work.</span></span> <span data-ttu-id="978dd-144">Das Erstellen einer neuen WebView2-Umgebung funktioniert bei Verwendung der neuesten Version.</span><span class="sxs-lookup"><span data-stu-id="978dd-144">Creating a new WebView2 Environment will work as it uses the latest version.</span></span>

<span data-ttu-id="978dd-145">Die WebView-Erstellung schlägt fehl, wenn bereits eine ausgeführte Instanz mit dem gleichen benutzerdatenordner vorhanden ist und die Umgebungsobjekte unterschiedliche environmentoptions aufweisen.</span><span class="sxs-lookup"><span data-stu-id="978dd-145">WebView creation will fail if there is already a running instance using the same user data folder, and the Environment objects have different EnvironmentOptions.</span></span> <span data-ttu-id="978dd-146">Wenn beispielsweise bereits eine WebView mit einer Sprache erstellt wurde, schlägt das Erstellen einer WebView mit einer anderen Sprache mithilfe desselben Benutzerdatenordners fehl.</span><span class="sxs-lookup"><span data-stu-id="978dd-146">For example, if there is already a WebView created with one language, trying to create a WebView with a different language using the same user data folder will fail.</span></span>

#### <span data-ttu-id="978dd-147">CreateWebResourceResponse</span><span class="sxs-lookup"><span data-stu-id="978dd-147">CreateWebResourceResponse</span></span> 

<span data-ttu-id="978dd-148">Erstellen Sie ein neues Webressourcen-Antwortobjekt.</span><span class="sxs-lookup"><span data-stu-id="978dd-148">Create a new web resource response object.</span></span>

> <span data-ttu-id="978dd-149">Public HRESULT [CreateWebResourceResponse](#createwebresourceresponse)(IStream \* Content, int Statuscode, LPCWSTR reasonPhrase, LPCWSTR Headers, [ICoreWebView2WebResourceResponse](icorewebview2webresourceresponse.md) \* \* Response)</span><span class="sxs-lookup"><span data-stu-id="978dd-149">public HRESULT [CreateWebResourceResponse](#createwebresourceresponse)(IStream \* content, int statusCode, LPCWSTR reasonPhrase, LPCWSTR headers, [ICoreWebView2WebResourceResponse](icorewebview2webresourceresponse.md) \*\* response)</span></span>

<span data-ttu-id="978dd-150">Die Kopfzeilen ist die unformatierte Antwortheader Zeichenfolge, die durch einen Zeilenumbruch getrennt ist.</span><span class="sxs-lookup"><span data-stu-id="978dd-150">The headers is the raw response header string delimited by newline.</span></span> <span data-ttu-id="978dd-151">Es ist auch möglich, dieses Objekt mit einer leeren Headerzeichenfolge zu erstellen und dann die Kopfzeilen Zeile für Zeile mithilfe der [ICoreWebView2HttpResponseHeaders](icorewebview2httpresponseheaders.md) zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="978dd-151">It's also possible to create this object with empty headers string and then use the [ICoreWebView2HttpResponseHeaders](icorewebview2httpresponseheaders.md) to construct the headers line by line.</span></span> <span data-ttu-id="978dd-152">Informationen zu anderen Parametern finden Sie unter [ICoreWebView2WebResourceResponse](icorewebview2webresourceresponse.md).</span><span class="sxs-lookup"><span data-stu-id="978dd-152">For information on other parameters see [ICoreWebView2WebResourceResponse](icorewebview2webresourceresponse.md).</span></span>

```cpp
        if (m_blockImages)
        {
            m_webView->AddWebResourceRequestedFilter(L"*", COREWEBVIEW2_WEB_RESOURCE_CONTEXT_IMAGE);
            CHECK_FAILURE(m_webView->add_WebResourceRequested(
                Callback<ICoreWebView2WebResourceRequestedEventHandler>(
                    [this](
                        ICoreWebView2* sender,
                        ICoreWebView2WebResourceRequestedEventArgs* args) {
                        COREWEBVIEW2_WEB_RESOURCE_CONTEXT resourceContext;
                        CHECK_FAILURE(
                            args->get_ResourceContext(&resourceContext));
                        // Ensure that the type is image
                        if (resourceContext != COREWEBVIEW2_WEB_RESOURCE_CONTEXT_IMAGE)
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

#### <span data-ttu-id="978dd-153">get_BrowserVersionString</span><span class="sxs-lookup"><span data-stu-id="978dd-153">get_BrowserVersionString</span></span> 

<span data-ttu-id="978dd-154">Die Browser Versionsinformationen des aktuellen [ICoreWebView2Environment](), einschließlich des Kanal namens, wenn es sich nicht um den stabilen Kanal handelt.</span><span class="sxs-lookup"><span data-stu-id="978dd-154">The browser version info of the current [ICoreWebView2Environment](), including channel name if it is not the stable channel.</span></span>

> <span data-ttu-id="978dd-155">Public HRESULT [get_BrowserVersionString](#get_browserversionstring)(LPWSTR \* VERSIONINFO)</span><span class="sxs-lookup"><span data-stu-id="978dd-155">public HRESULT [get_BrowserVersionString](#get_browserversionstring)(LPWSTR \* versionInfo)</span></span>

<span data-ttu-id="978dd-156">Dies entspricht dem Format der GetAvailableCoreWebView2BrowserVersionString-API.</span><span class="sxs-lookup"><span data-stu-id="978dd-156">This matches the format of the GetAvailableCoreWebView2BrowserVersionString API.</span></span> <span data-ttu-id="978dd-157">Kanalnamen sind "Beta", "dev" und "Canary".</span><span class="sxs-lookup"><span data-stu-id="978dd-157">Channel names are 'beta', 'dev', and 'canary'.</span></span>

```cpp
        wil::unique_cotaskmem_string version_info;
        m_webViewEnvironment->get_BrowserVersionString(&version_info);
        MessageBox(
            m_mainWindow, version_info.get(), L"Browser Version Info After WebView Creation",
            MB_OK);
```

#### <span data-ttu-id="978dd-158">remove_NewBrowserVersionAvailable</span><span class="sxs-lookup"><span data-stu-id="978dd-158">remove_NewBrowserVersionAvailable</span></span> 

<span data-ttu-id="978dd-159">Entfernen Sie einen Ereignishandler, der zuvor mit add_NewBrowserVersionAvailable hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="978dd-159">Remove an event handler previously added with add_NewBrowserVersionAvailable.</span></span>

> <span data-ttu-id="978dd-160">Public HRESULT [remove_NewBrowserVersionAvailable](#remove_newbrowserversionavailable)(EventRegistrationToken-Token)</span><span class="sxs-lookup"><span data-stu-id="978dd-160">public HRESULT [remove_NewBrowserVersionAvailable](#remove_newbrowserversionavailable)(EventRegistrationToken token)</span></span>

