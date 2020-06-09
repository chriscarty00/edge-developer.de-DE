---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: Microsoft Edge-WebView2 für Win32-apps
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/05/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: 56f2e59b8f7c19f130bba1e579fac28e4536dd90
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698937"
---
# Schnittstellen ICoreWebView2ExperimentalEnvironment 

> [!NOTE]
> Dies ist eine experimentelle API, die mit unserer Vorabversion SDK-Version 0.9.538 ausgeliefert wird.

```
interface ICoreWebView2ExperimentalEnvironment
  : public IUnknown
```

Diese Schnittstelle ist eine Erweiterung des [ICoreWebView2Environment](icorewebview2environment.md).

## Zusammenfassung

 Member                        | Beschreibungen
--------------------------------|---------------------------------------------
[CreateCoreWebView2CompositionController](#createcorewebview2compositioncontroller) | Erstellen Sie ein neues WebView-Element für die Verwendung mit Visual Hosting asynchron.
[CreateCoreWebView2PointerInfo](#createcorewebview2pointerinfo) | Erstellen Sie ein leeres [ICoreWebView2ExperimentalPointerInfo](icorewebview2experimentalpointerinfo.md).
[GetProviderForHwnd](#getproviderforhwnd) | Gibt den Benutzeroberflächenautomatisierungs-Anbieter für die ICoreWebView2CompositionController zurück, die dem angegebenen HWND entspricht.

Ein Objekt, das die [ICoreWebView2ExperimentalEnvironment]() -Schnittstelle implementiert, implementiert auch [ICoreWebView2Environment](icorewebview2environment.md).

## Member

#### CreateCoreWebView2CompositionController 

Erstellen Sie ein neues WebView-Element für die Verwendung mit Visual Hosting asynchron.

> Public HRESULT [CreateCoreWebView2CompositionController](#createcorewebview2compositioncontroller)(HWND ParentWindow, [ICoreWebView2ExperimentalCreateCoreWebView2CompositionControllerCompletedHandler](icorewebview2experimentalcreatecorewebview2compositioncontrollercompletedhandler.md) * Handler)

ParentWindow ist das HWND, in dem die APP die visuelle Struktur von WebView verbindet. Hierbei handelt es sich um das HWND, in dem die APP Zeiger-und Mauseingaben für die WebView erhält (und SendMouseInput/SendPointerInput für Forward verwenden muss). Wenn die APP die visuelle WebView-Struktur unter einem anderen Fenster verschiebt, muss put_ParentWindow aufgerufen werden, um das neue übergeordnete HWND der visuellen Struktur zu aktualisieren.

Verwenden Sie put_RootVisualTarget auf dem erstellten CoreWebView2CompositionController, um ein visuelles Element bereitzustellen, das die visuelle Struktur des Browsers hostet.

Es wird empfohlen, die Anwendungsbenutzer Modell-ID für den Prozess oder das Anwendungsfenster festzulegen. Wenn None gesetzt ist, wird bei der Erstellung von WebView eine generierte Anwendungsbenutzer Modell-ID auf das Stammfenster von ParentWindow eingestellt. 
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
 Es wird empfohlen, dass die Anwendung Neustart-Manager-Nachrichten verarbeitet, damit Sie ordnungsgemäß neu gestartet werden kann, wenn die APP Edge für WebView aus einer bestimmten Installation verwendet und die Installation deinstalliert wird. Wenn ein Benutzer beispielsweise Edge from dev Channel installiert und sich entscheidet, Edge aus diesem Kanal zum Testen der APP zu verwenden, und dann Edge aus diesem Kanal deinstalliert, ohne die APP zu schließen, wird die APP neu gestartet, damit die Deinstallation des dev-Kanals erfolgreich ausgeführt werden kann. 
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

#### CreateCoreWebView2PointerInfo 

Erstellen Sie ein leeres [ICoreWebView2ExperimentalPointerInfo](icorewebview2experimentalpointerinfo.md).

> Public HRESULT [CreateCoreWebView2PointerInfo](#createcorewebview2pointerinfo)([ICoreWebView2ExperimentalPointerInfo](icorewebview2experimentalpointerinfo.md) * * pointerInfo)

Der zurückgegebene [ICoreWebView2ExperimentalPointerInfo](icorewebview2experimentalpointerinfo.md) muss mit allen relevanten Informationen gefüllt werden, bevor SendPointerInput aufgerufen wird.

#### GetProviderForHwnd 

Gibt den Benutzeroberflächenautomatisierungs-Anbieter für die ICoreWebView2CompositionController zurück, die dem angegebenen HWND entspricht.

> Public HRESULT [GetProviderForHwnd](#getproviderforhwnd)(HWND hWnd, IUnknown * * Provider)

