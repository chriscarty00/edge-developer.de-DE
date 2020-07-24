---
description: Einbetten von Webtechnologien (HTML, CSS und JavaScript) in ihre systemeigenen Anwendungen mit dem Microsoft Edge WebView2-Steuerelement
title: WebView2 Win32 C++ ICoreWebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/23/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML, ICoreWebView2
ms.openlocfilehash: a1da6789027234130c58078871d7da23b4e285ba
ms.sourcegitcommit: 553957c101f83681b363103cb6af56bf20173f23
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/24/2020
ms.locfileid: "10895497"
---
# Schnittstellen ICoreWebView2 

```
interface ICoreWebView2
  : public IUnknown
```

WebView2 ermöglicht Ihnen das Hosten von Webinhalten mithilfe der neuesten Edge-Webbrowser Technologie.

## Zusammenfassung

 Member                        | Beschreibungen
--------------------------------|---------------------------------------------
[add_ContainsFullScreenElementChanged](#add_containsfullscreenelementchanged) | Benachrichtigt, wenn sich die ContainsFullScreenElement-Eigenschaft ändert.
[add_ContentLoading](#add_contentloading) | Fügen Sie einen Ereignishandler für das ContentLoading-Ereignis hinzu.
[add_DocumentTitleChanged](#add_documenttitlechanged) | Fügen Sie einen Ereignishandler für das DocumentTitleChanged-Ereignis hinzu.
[add_FrameNavigationCompleted](#add_framenavigationcompleted) | Fügen Sie einen Ereignishandler für das FrameNavigationCompleted-Ereignis hinzu.
[add_FrameNavigationStarting](#add_framenavigationstarting) | Fügen Sie einen Ereignishandler für das FrameNavigationStarting-Ereignis hinzu.
[add_HistoryChanged](#add_historychanged) | Abrechnungshistorieändern hören Sie sich die Änderung des Navigationsverlaufs für das Dokument der obersten Ebene an.
[add_NavigationCompleted](#add_navigationcompleted) | Fügen Sie einen Ereignishandler für das NavigationCompleted-Ereignis hinzu.
[add_NavigationStarting](#add_navigationstarting) | Fügen Sie einen Ereignishandler für das NavigationStarting-Ereignis hinzu.
[add_NewWindowRequested](#add_newwindowrequested) | Fügen Sie einen Ereignishandler für das mswebviewnewwindowrequested-Ereignis hinzu.
[add_PermissionRequested](#add_permissionrequested) | Fügen Sie einen Ereignishandler für das PermissionRequested-Ereignis hinzu.
[add_ProcessFailed](#add_processfailed) | Fügen Sie einen Ereignishandler für das ProcessFailed-Ereignis hinzu.
[add_ScriptDialogOpening](#add_scriptdialogopening) | Fügen Sie einen Ereignishandler für das ScriptDialogOpening-Ereignis hinzu.
[add_SourceChanged](#add_sourcechanged) | Die Quelle wird ausgelöst, wenn die Quelleigenschaft geändert wird.
[add_WebMessageReceived](#add_webmessagereceived) | Dieses Ereignis wird ausgelöst, wenn die IsWebMessageEnabled-Einstellung festgelegt ist, und das Dokument auf oberster Ebene des WebView-Anrufs `window.chrome.webview.postMessage` .
[add_WebResourceRequested](#add_webresourcerequested) | Fügen Sie einen Ereignishandler für das WebResourceRequested-Ereignis hinzu.
[add_WindowCloseRequested](#add_windowcloserequested) | Fügen Sie einen Ereignishandler für das WindowCloseRequested-Ereignis hinzu.
[AddHostObjectToScript](#addhostobjecttoscript) | Fügen Sie das bereitgestellte Hostobjekt zu Skript hinzu, das in der WebView mit dem angegebenen Namen ausgeführt wird.
[AddScriptToExecuteOnDocumentCreated](#addscripttoexecuteondocumentcreated) | Fügen Sie das bereitgestellte JavaScript einer Liste von Skripts hinzu, die ausgeführt werden sollen, nachdem das globale Objekt erstellt wurde, aber bevor das HTML-Dokument analysiert wurde und bevor ein anderes Skript ausgeführt wird, das vom HTML-Dokument eingeschlossen ist.
[AddWebResourceRequestedFilter](#addwebresourcerequestedfilter) | Fügt dem WebResourceRequested-Ereignis einen URI-und Ressourcenkontext Filter hinzu.
[CallDevToolsProtocolMethod](#calldevtoolsprotocolmethod) | Rufen Sie eine asynchrone DevToolsProtocol-Methode auf.
[CapturePreview](#capturepreview) | Erfassen Sie ein Bild von der Anzeige von WebView.
[ExecuteScript](#executescript) | Führen Sie JavaScript-Code aus dem JavaScript-Parameter im aktuellen Dokument der obersten Ebene aus, das in der WebView gerendert wird.
[get_BrowserProcessId](#get_browserprocessid) | Die Prozess-ID des Browser Prozesses, der die WebView hostet.
[get_CanGoBack](#get_cangoback) | Gibt "true" zurück, wenn die WebView zu einer vorherigen Seite im Navigationsverlauf navigieren kann.
[get_CanGoForward](#get_cangoforward) | Gibt "true" zurück, wenn die WebView zu einer nächsten Seite im Navigationsverlauf navigieren kann.
[get_ContainsFullScreenElement](#get_containsfullscreenelement) | Gibt an, ob die WebView ein HTML-Vollbild-Element enthält.
[get_DocumentTitle](#get_documenttitle) | Der Titel für das aktuelle Dokument der obersten Ebene.
[get_Settings](#get_settings) | Das [ICoreWebView2Settings](icorewebview2settings.md) -Objekt enthält verschiedene änderbare Einstellungen für den ausgeführten WebView.
[get_Source](#get_source) | Der URI des aktuellen Dokuments auf oberster Ebene.
[GetDevToolsProtocolEventReceiver](#getdevtoolsprotocoleventreceiver) | Rufen Sie einen devtools-Protokollereignis Empfänger ab, mit dem Sie ein devtools-Protokollereignis abonnieren können.
[GoBack](#goback) | Navigiert die WebView zur vorherigen Seite im Navigationsverlauf.
[GoForward](#goforward) | Navigiert die WebView zur nächsten Seite im Navigationsverlauf.
[%%amp;quot;Navigate%%amp;quot;
](#navigate) | Führen Sie eine Navigation des Dokuments auf oberster Ebene zum angegebenen URI.
[NavigateToString](#navigatetostring) | Initiiert eine Navigation zu htmlContent als HTML-Code für ein neues Dokument.
[OpenDevToolsWindow](#opendevtoolswindow) | Öffnet das devtools-Fenster für das aktuelle Dokument in der WebView.
[PostWebMessageAsJson](#postwebmessageasjson) | Posten Sie die angegebene Webnachricht im Dokument der obersten Ebene in dieser WebView.
[PostWebMessageAsString](#postwebmessageasstring) | Dies ist ein Helfer zum Posten einer Nachricht, bei der es sich um eine einfache Zeichenfolge und nicht um eine JSON-Zeichenfolgendarstellung eines JavaScript-Objekts handelt.
[Laden](#reload) | Laden Sie die aktuelle Seite neu.
[remove_ContainsFullScreenElementChanged](#remove_containsfullscreenelementchanged) | Entfernen Sie einen Ereignishandler, der zuvor mit der entsprechenden add_-Ereignismethode hinzugefügt wurde.
[remove_ContentLoading](#remove_contentloading) | Entfernen Sie einen Ereignishandler, der zuvor mit add_ContentLoading hinzugefügt wurde.
[remove_DocumentTitleChanged](#remove_documenttitlechanged) | Entfernen Sie einen Ereignishandler, der zuvor mit add_DocumentTitleChanged hinzugefügt wurde.
[remove_FrameNavigationCompleted](#remove_framenavigationcompleted) | Entfernen Sie einen Ereignishandler, der zuvor mit add_FrameNavigationCompleted hinzugefügt wurde.
[remove_FrameNavigationStarting](#remove_framenavigationstarting) | Entfernen Sie einen Ereignishandler, der zuvor mit add_FrameNavigationStarting hinzugefügt wurde.
[remove_HistoryChanged](#remove_historychanged) | Entfernen Sie einen Ereignishandler, der zuvor mit add_HistoryChanged hinzugefügt wurde.
[remove_NavigationCompleted](#remove_navigationcompleted) | Entfernen Sie einen Ereignishandler, der zuvor mit add_NavigationCompleted hinzugefügt wurde.
[remove_NavigationStarting](#remove_navigationstarting) | Entfernen Sie einen Ereignishandler, der zuvor mit add_NavigationStarting hinzugefügt wurde.
[remove_NewWindowRequested](#remove_newwindowrequested) | Entfernen Sie einen Ereignishandler, der zuvor mit add_NewWindowRequested hinzugefügt wurde.
[remove_PermissionRequested](#remove_permissionrequested) | Entfernen Sie einen Ereignishandler, der zuvor mit add_PermissionRequested hinzugefügt wurde.
[remove_ProcessFailed](#remove_processfailed) | Entfernen Sie einen Ereignishandler, der zuvor mit add_ProcessFailed hinzugefügt wurde.
[remove_ScriptDialogOpening](#remove_scriptdialogopening) | Entfernen Sie einen Ereignishandler, der zuvor mit add_ScriptDialogOpening hinzugefügt wurde.
[remove_SourceChanged](#remove_sourcechanged) | Entfernen Sie einen Ereignishandler, der zuvor mit add_SourceChanged hinzugefügt wurde.
[remove_WebMessageReceived](#remove_webmessagereceived) | Entfernen Sie einen Ereignishandler, der zuvor mit add_WebMessageReceived hinzugefügt wurde.
[remove_WebResourceRequested](#remove_webresourcerequested) | Entfernen Sie einen Ereignishandler, der zuvor mit add_WebResourceRequested hinzugefügt wurde.
[remove_WindowCloseRequested](#remove_windowcloserequested) | Entfernen Sie einen Ereignishandler, der zuvor mit add_WindowCloseRequested hinzugefügt wurde.
[RemoveHostObjectFromScript](#removehostobjectfromscript) | Entfernen Sie das vom Namen angegebene Hostobjekt, damit es nicht mehr über JavaScript-Code in der WebView zugänglich ist.
[RemoveScriptToExecuteOnDocumentCreated](#removescripttoexecuteondocumentcreated) | Entfernen Sie das entsprechende JavaScript `AddScriptToExecuteOnDocumentCreated` , das mit der angegebenen Skript-ID hinzugefügt wurde.
[RemoveWebResourceRequestedFilter](#removewebresourcerequestedfilter) | Entfernt einen übereinstimmenden Webressourcen Filter, der zuvor für das WebResourceRequested-Ereignis hinzugefügt wurde.
[Stop](#stop) | Beenden Sie alle Navigations-und ausstehenden Ressourcen Abrufe.
[COREWEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT](#corewebview2_capture_preview_image_format) | Bildformat, das von der ICoreWebView2:: CapturePreview-Methode verwendet wird.
[COREWEBVIEW2_KEY_EVENT_KIND](#corewebview2_key_event_kind) | Der Typ des Schlüssel Ereignisses, das ein AcceleratorKeyPressed-Ereignis ausgelöst hat.
[COREWEBVIEW2_MOVE_FOCUS_REASON](#corewebview2_move_focus_reason) | Grund für das Verschieben des Fokus
[COREWEBVIEW2_PERMISSION_KIND](#corewebview2_permission_kind) | Der Typ einer Berechtigungsanforderung.
[COREWEBVIEW2_PERMISSION_STATE](#corewebview2_permission_state) | Antwort auf eine Berechtigungsanforderung.
[COREWEBVIEW2_PHYSICAL_KEY_STATUS](#corewebview2_physical_key_status) | Eine Struktur, die die Informationen darstellt, die in lParam verpackt sind, die einem Win32-Schlüsselereignis zugewiesen wurden.
[COREWEBVIEW2_PROCESS_FAILED_KIND](#corewebview2_process_failed_kind) | Art des in der ICoreWebView2ProcessFailedEventHandler-Schnittstelle verwendeten Prozess Fehlers.
[COREWEBVIEW2_SCRIPT_DIALOG_KIND](#corewebview2_script_dialog_kind) | Art des in der ICoreWebView2ScriptDialogOpeningEventHandler-Schnittstelle verwendeten JavaScript-Dialogfelds.
[COREWEBVIEW2_WEB_ERROR_STATUS](#corewebview2_web_error_status) | Fehlerstatus Werte für Web-Navigationselemente.
[COREWEBVIEW2_WEB_RESOURCE_CONTEXT](#corewebview2_web_resource_context) | Enum für Webressourcen-anforderungskontexte.

## Member

#### add_ContainsFullScreenElementChanged 

Benachrichtigt, wenn sich die ContainsFullScreenElement-Eigenschaft ändert.

> Public HRESULT [add_ContainsFullScreenElementChanged](#add_containsfullscreenelementchanged)([ICoreWebView2ContainsFullScreenElementChangedEventHandler](icorewebview2containsfullscreenelementchangedeventhandler.md) * EventHandler, EventRegistrationToken * Token)

Dies bedeutet, dass ein HTML-Element in der WebView Vollbild auf die Größe des WebView-Elements eingibt oder den Fullscreen-Eintrag verlässt. Dieses Ereignis ist nützlich, wenn beispielsweise ein Video Element den Fullscreen-Modus anfordert. Der Listener von ContainsFullScreenElementChanged kann die WebView-Ansicht dann als Antwort ändern.

```cpp
    // Register a handler for the ContainsFullScreenChanged event.
    CHECK_FAILURE(m_webView->add_ContainsFullScreenElementChanged(
        Callback<ICoreWebView2ContainsFullScreenElementChangedEventHandler>(
            [this](ICoreWebView2* sender, IUnknown* args) -> HRESULT {
                if (m_fullScreenAllowed)
                {
                    CHECK_FAILURE(
                        sender->get_ContainsFullScreenElement(&m_containsFullscreenElement));
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

#### add_ContentLoading 

Fügen Sie einen Ereignishandler für das ContentLoading-Ereignis hinzu.

> Public HRESULT [add_ContentLoading](#add_contentloading)([ICoreWebView2ContentLoadingEventHandler](icorewebview2contentloadingeventhandler.md) * EventHandler, EventRegistrationToken * Token)

ContentLoading wird ausgelöst, bevor Inhalte geladen werden, einschließlich Skripten, die mit AddScriptToExecuteOnDocumentCreated hinzugefügt wurden ContentLoading werden nicht ausgelöst, wenn dieselbe Seitennavigation erfolgt (beispielsweisedurch Fragment-Navigation oder History. pushState-Navigation). Dies folgt auf das NavigationStarting-Ereignis und das Source-Ereignis und steht vor den Ereignissen "History" und "NavigationCompleted".

#### add_DocumentTitleChanged 

Fügen Sie einen Ereignishandler für das DocumentTitleChanged-Ereignis hinzu.

> Public HRESULT [add_DocumentTitleChanged](#add_documenttitlechanged)([ICoreWebView2DocumentTitleChangedEventHandler](icorewebview2documenttitlechangedeventhandler.md) * EventHandler, EventRegistrationToken * Token)

Das Ereignis wird ausgelöst, wenn die DocumentTitle-Eigenschaft des WebView-Ereignisses geändert wird und möglicherweise vor oder nach dem NavigationCompleted-Ereignis ausgelöst wird.

```cpp
    // Register a handler for the DocumentTitleChanged event.
    // This handler just announces the new title on the window's title bar.
    CHECK_FAILURE(m_webView->add_DocumentTitleChanged(
        Callback<ICoreWebView2DocumentTitleChangedEventHandler>(
            [this](ICoreWebView2* sender, IUnknown* args) -> HRESULT {
                wil::unique_cotaskmem_string title;
                CHECK_FAILURE(sender->get_DocumentTitle(&title));
                SetWindowText(m_appWindow->GetMainWindow(), title.get());
                return S_OK;
            })
            .Get(),
        &m_documentTitleChangedToken));
```

#### add_FrameNavigationCompleted 

Fügen Sie einen Ereignishandler für das FrameNavigationCompleted-Ereignis hinzu.

> Public HRESULT [add_FrameNavigationCompleted](#add_framenavigationcompleted)([ICoreWebView2NavigationCompletedEventHandler](icorewebview2navigationcompletedeventhandler.md) * EventHandler, EventRegistrationToken * Token)

Das FrameNavigationCompleted-Ereignis wird ausgelöst, wenn ein untergeordneter Frame vollständig geladen wurde (Body. OnLoad wurde ausgelöst) oder das Laden mit einem Fehler beendet wurde.

```cpp
    // Register a handler for the FrameNavigationCompleted event.
    // Check whether the navigation succeeded, and if not, do something.
    CHECK_FAILURE(m_webView->add_FrameNavigationCompleted(
        Callback<ICoreWebView2NavigationCompletedEventHandler>(
            [this](ICoreWebView2* sender, ICoreWebView2NavigationCompletedEventArgs* args)
                -> HRESULT {
                BOOL success;
                CHECK_FAILURE(args->get_IsSuccess(&success));
                if (!success)
                {
                    COREWEBVIEW2_WEB_ERROR_STATUS webErrorStatus;
                    CHECK_FAILURE(args->get_WebErrorStatus(&webErrorStatus));
                    std::wstring error_msg = WebErrorStatusToString(webErrorStatus);
                    MessageBox(nullptr,
                       (std::wstring(L"IFrame navigation failed with the ") +
                         L"give in error " + error_msg).c_str(),
                       L"Navigation Failure", MB_OK);
                    if (webErrorStatus == COREWEBVIEW2_WEB_ERROR_STATUS_DISCONNECTED)
                    {
                        // Do something here if you want to handle a specific error case.
                        // In most cases this isn't necessary, because the WebView will
                        // display its own error page automatically.
                    }
                }
                return S_OK;
            })
            .Get(),
        &m_frameNavigationCompletedToken));
```

#### add_FrameNavigationStarting 

Fügen Sie einen Ereignishandler für das FrameNavigationStarting-Ereignis hinzu.

> Public HRESULT [add_FrameNavigationStarting](#add_framenavigationstarting)([ICoreWebView2NavigationStartingEventHandler](icorewebview2navigationstartingeventhandler.md) * EventHandler, EventRegistrationToken * Token)

FrameNavigationStarting wird ausgelöst, wenn ein untergeordneter Frame in der WebView die Berechtigung zum Navigieren zu einem anderen URI anfordert. Dies wird auch für Umleitungen ausgelöst.

```cpp
    // Register a handler for the FrameNavigationStarting event.
    // This handler will prevent a frame from navigating to a blocked domain.
    CHECK_FAILURE(m_webView->add_FrameNavigationStarting(
        Callback<ICoreWebView2NavigationStartingEventHandler>(
            [this](ICoreWebView2* sender,
                   ICoreWebView2NavigationStartingEventArgs* args) -> HRESULT
    {
        wil::unique_cotaskmem_string uri;
        CHECK_FAILURE(args->get_Uri(&uri));

        if (ShouldBlockUri(uri.get()))
        {
            CHECK_FAILURE(args->put_Cancel(true));
        }
        return S_OK;
    }).Get(), &m_frameNavigationStartingToken));
```

#### add_HistoryChanged 

Abrechnungshistorieändern hören Sie sich die Änderung des Navigationsverlaufs für das Dokument der obersten Ebene an.

> Public HRESULT [add_HistoryChanged](#add_historychanged)([ICoreWebView2HistoryChangedEventHandler](icorewebview2historychangedeventhandler.md) * EventHandler, EventRegistrationToken * Token)

Verwenden Sie abrechnungshistorieändern, um zu überprüfen, ob sich CanGoBack/CanGoForward-Wert geändert hat. "History" wird auch für die Verwendung von GoBack/GoForward ausgelöst. "History" wird nach "sourcely" und "ContentLoading" ausgelöst. Fügen Sie einen Ereignishandler für das History-Ereignis hinzu. 
```cpp
    // Register a handler for the HistoryChanged event.
    // Update the Back, Forward buttons.
    CHECK_FAILURE(m_webView->add_HistoryChanged(
        Callback<ICoreWebView2HistoryChangedEventHandler>(
            [this](ICoreWebView2* sender, IUnknown* args) -> HRESULT {
                BOOL canGoBack;
                BOOL canGoForward;
                sender->get_CanGoBack(&canGoBack);
                sender->get_CanGoForward(&canGoForward);
                m_toolbar->SetItemEnabled(Toolbar::Item_BackButton, canGoBack);
                m_toolbar->SetItemEnabled(Toolbar::Item_ForwardButton, canGoForward);

                return S_OK;
            })
            .Get(),
        &m_historyChangedToken));
```

#### add_NavigationCompleted 

Fügen Sie einen Ereignishandler für das NavigationCompleted-Ereignis hinzu.

> Public HRESULT [add_NavigationCompleted](#add_navigationcompleted)([ICoreWebView2NavigationCompletedEventHandler](icorewebview2navigationcompletedeventhandler.md) * EventHandler, EventRegistrationToken * Token)

Das NavigationCompleted-Ereignis wird ausgelöst, wenn die WebView vollständig geladen wurde (Body. OnLoad wurde ausgelöst) oder das Laden mit einem Fehler beendet wurde.

```cpp
    // Register a handler for the NavigationCompleted event.
    // Check whether the navigation succeeded, and if not, do something.
    // Also update the Cancel buttons.
    CHECK_FAILURE(m_webView->add_NavigationCompleted(
        Callback<ICoreWebView2NavigationCompletedEventHandler>(
            [this](ICoreWebView2* sender, ICoreWebView2NavigationCompletedEventArgs* args)
                -> HRESULT {
                BOOL success;
                CHECK_FAILURE(args->get_IsSuccess(&success));
                if (!success)
                {
                    COREWEBVIEW2_WEB_ERROR_STATUS webErrorStatus;
                    CHECK_FAILURE(args->get_WebErrorStatus(&webErrorStatus));
                    if (webErrorStatus == COREWEBVIEW2_WEB_ERROR_STATUS_DISCONNECTED)
                    {
                        // Do something here if you want to handle a specific error case.
                        // In most cases this isn't necessary, because the WebView will
                        // display its own error page automatically.
                    }
                }
                m_toolbar->SetItemEnabled(Toolbar::Item_CancelButton, false);
                m_toolbar->SetItemEnabled(Toolbar::Item_ReloadButton, true);
                return S_OK;
            })
            .Get(),
        &m_navigationCompletedToken));
```

#### add_NavigationStarting 

Fügen Sie einen Ereignishandler für das NavigationStarting-Ereignis hinzu.

> Public HRESULT [add_NavigationStarting](#add_navigationstarting)([ICoreWebView2NavigationStartingEventHandler](icorewebview2navigationstartingeventhandler.md) * EventHandler, EventRegistrationToken * Token)

NavigationStarting wird ausgelöst, wenn der WebView-Hauptframe die Berechtigung zum Navigieren zu einem anderen URI anfordert. Dies wird auch für Umleitungen ausgelöst.

```cpp
    // Register a handler for the NavigationStarting event.
    // This handler will check the domain being navigated to, and if the domain
    // matches a list of blocked sites, it will cancel the navigation and
    // possibly display a warning page.  It will also disable JavaScript on
    // selected websites.
    CHECK_FAILURE(m_webView->add_NavigationStarting(
        Callback<ICoreWebView2NavigationStartingEventHandler>(
            [this](ICoreWebView2* sender,
                   ICoreWebView2NavigationStartingEventArgs* args) -> HRESULT
    {
        wil::unique_cotaskmem_string uri;
        CHECK_FAILURE(args->get_Uri(&uri));

        if (ShouldBlockUri(uri.get()))
        {
            CHECK_FAILURE(args->put_Cancel(true));

            // If the user clicked a link to navigate, show a warning page.
            BOOL userInitiated;
            CHECK_FAILURE(args->get_IsUserInitiated(&userInitiated));
            static const PCWSTR htmlContent =
              L"<h1>Domain Blocked</h1>"
              L"<p>You've attempted to navigate to a domain in the blocked "
              L"sites list. Press back to return to the previous page.</p>";
            CHECK_FAILURE(sender->NavigateToString(htmlContent));
        }
        // Changes to settings will apply at the next navigation, which includes the
        // navigation after a NavigationStarting event.  We can use this to change
        // settings according to what site we're visiting.
        if (ShouldBlockScriptForUri(uri.get()))
        {
            m_settings->put_IsScriptEnabled(FALSE);
        }
        else
        {
            m_settings->put_IsScriptEnabled(m_isScriptEnabled);
        }
        return S_OK;
    }).Get(), &m_navigationStartingToken));
```

#### add_NewWindowRequested 

Fügen Sie einen Ereignishandler für das mswebviewnewwindowrequested-Ereignis hinzu.

> Public HRESULT [add_NewWindowRequested](#add_newwindowrequested)([ICoreWebView2NewWindowRequestedEventHandler](icorewebview2newwindowrequestedeventhandler.md) * EventHandler, EventRegistrationToken * Token)

Wird ausgelöst, wenn der Inhalt in der WebView zum Öffnen eines neuen Fensters angefordert wird, beispielsweisedurch Window. Open. Die APP kann eine Ziel-WebView übergeben, die als das geöffnete Fenster angesehen wird.

```cpp
    // Register a handler for the NewWindowRequested event.
    // This handler will defer the event, create a new app window, and then once the
    // new window is ready, it'll provide that new window's WebView as the response to
    // the request.
    CHECK_FAILURE(m_webView->add_NewWindowRequested(
        Callback<ICoreWebView2NewWindowRequestedEventHandler>(
            [this](ICoreWebView2* sender, ICoreWebView2NewWindowRequestedEventArgs* args) {
                wil::com_ptr<ICoreWebView2Deferral> deferral;
                CHECK_FAILURE(args->GetDeferral(&deferral));
                AppWindow* newAppWindow;

                wil::com_ptr<ICoreWebView2ExperimentalNewWindowRequestedEventArgs>
                    experimentalArgs;
                CHECK_FAILURE(args->QueryInterface(IID_PPV_ARGS(&experimentalArgs)));
                wil::com_ptr<ICoreWebView2ExperimentalWindowFeatures> windowFeatures;
                CHECK_FAILURE(experimentalArgs->get_WindowFeatures(&windowFeatures));

                RECT windowRect = {0};
                UINT32 left = 0;
                UINT32 top = 0;
                UINT32 height = 0;
                UINT32 width = 0;
                BOOL shouldHaveToolbar = true;

                BOOL hasPosition = FALSE;
                BOOL hasSize = FALSE;
                CHECK_FAILURE(windowFeatures->HasPosition(&hasPosition));
                CHECK_FAILURE(windowFeatures->HasSize(&hasSize));

                bool useDefaultWindow = true;

                if (!!hasPosition && !!hasSize)
                {
                    CHECK_FAILURE(windowFeatures->get_Left(&left));
                    CHECK_FAILURE(windowFeatures->get_Top(&top));
                    CHECK_FAILURE(windowFeatures->get_Height(&height));
                    CHECK_FAILURE(windowFeatures->get_Width(&width));
                    useDefaultWindow = false;
                }
                CHECK_FAILURE(windowFeatures->get_Toolbar(&shouldHaveToolbar));

                windowRect.left = left;
                windowRect.right = left + (width < s_minNewWindowSize ? s_minNewWindowSize : width);
                windowRect.top = top;
                windowRect.bottom = top + (height < s_minNewWindowSize ? s_minNewWindowSize : height);

                if (!useDefaultWindow)
                {
                  newAppWindow = new AppWindow(m_creationModeId, L"", nullptr, true, windowRect, !!shouldHaveToolbar);
                }
                else
                {
                  newAppWindow = new AppWindow(m_creationModeId, L"");
                }
                newAppWindow->m_isPopupWindow = true;
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

#### add_PermissionRequested 

Fügen Sie einen Ereignishandler für das PermissionRequested-Ereignis hinzu.

> Public HRESULT [add_PermissionRequested](#add_permissionrequested)([ICoreWebView2PermissionRequestedEventHandler](icorewebview2permissionrequestedeventhandler.md) * EventHandler, EventRegistrationToken * Token)

Wird ausgelöst, wenn Inhalt in einer WebView-Anforderung die Berechtigung für den Zugriff auf einige Privilegierte Ressourcen anfordert.

```cpp
    // Register a handler for the PermissionRequested event.
    // This handler prompts the user to allow or deny the request.
    CHECK_FAILURE(m_webView->add_PermissionRequested(
        Callback<ICoreWebView2PermissionRequestedEventHandler>(
            [this](
                ICoreWebView2* sender,
                ICoreWebView2PermissionRequestedEventArgs* args) -> HRESULT
    {
        wil::unique_cotaskmem_string uri;
        COREWEBVIEW2_PERMISSION_KIND kind = COREWEBVIEW2_PERMISSION_KIND_UNKNOWN_PERMISSION;
        BOOL userInitiated = FALSE;

        CHECK_FAILURE(args->get_Uri(&uri));
        CHECK_FAILURE(args->get_PermissionKind(&kind));
        CHECK_FAILURE(args->get_IsUserInitiated(&userInitiated));

        std::wstring message = L"Do you want to grant permission for ";
        message += NameOfPermissionKind(kind);
        message += L" to the website at ";
        message += uri.get();
        message += L"?\n\n";
        message += (userInitiated
            ? L"This request came from a user gesture."
            : L"This request did not come from a user gesture.");

        int response = MessageBox(nullptr, message.c_str(), L"Permission Request",
                                   MB_YESNOCANCEL | MB_ICONWARNING);

        COREWEBVIEW2_PERMISSION_STATE state =
              response == IDYES ? COREWEBVIEW2_PERMISSION_STATE_ALLOW
            : response == IDNO  ? COREWEBVIEW2_PERMISSION_STATE_DENY
            :                     COREWEBVIEW2_PERMISSION_STATE_DEFAULT;
        CHECK_FAILURE(args->put_State(state));

        return S_OK;
    }).Get(), &m_permissionRequestedToken));
```

#### add_ProcessFailed 

Fügen Sie einen Ereignishandler für das ProcessFailed-Ereignis hinzu.

> Public HRESULT [add_ProcessFailed](#add_processfailed)([ICoreWebView2ProcessFailedEventHandler](icorewebview2processfailedeventhandler.md) * EventHandler, EventRegistrationToken * Token)

Wird ausgelöst, wenn ein WebView-Prozess unerwartet beendet wird oder nicht mehr reagiert.

```cpp
    // Register a handler for the ProcessFailed event.
    // This handler checks if the browser process failed, and asks the user if
    // they want to recreate the webview.
    CHECK_FAILURE(m_webView->add_ProcessFailed(
        Callback<ICoreWebView2ProcessFailedEventHandler>(
            [this](ICoreWebView2* sender,
                ICoreWebView2ProcessFailedEventArgs* args) -> HRESULT
    {
        COREWEBVIEW2_PROCESS_FAILED_KIND failureType;
        CHECK_FAILURE(args->get_ProcessFailedKind(&failureType));
        if (failureType == COREWEBVIEW2_PROCESS_FAILED_KIND_BROWSER_PROCESS_EXITED)
        {
            int button = MessageBox(
                m_appWindow->GetMainWindow(),
                L"Browser process exited unexpectedly.  Recreate webview?",
                L"Browser process exited",
                MB_YESNO);
            if (button == IDYES)
            {
                m_appWindow->ReinitializeWebView();
            }
        }
        else if (failureType == COREWEBVIEW2_PROCESS_FAILED_KIND_RENDER_PROCESS_UNRESPONSIVE)
        {
            int button = MessageBox(
                m_appWindow->GetMainWindow(),
                L"Browser render process has stopped responding.  Recreate webview?",
                L"Web page unresponsive", MB_YESNO);
            if (button == IDYES)
            {
                m_appWindow->ReinitializeWebView();
            }
        }
        else if (failureType == COREWEBVIEW2_PROCESS_FAILED_KIND_RENDER_PROCESS_EXITED)
        {
            int button = MessageBox(
                m_appWindow->GetMainWindow(),
                L"Browser render process exited unexpectedly. Reload page?",
                L"Web page unresponsive", MB_YESNO);
            if (button == IDYES)
            {
                CHECK_FAILURE(m_webView->Reload());
            }
        }
        return S_OK;
    }).Get(), &m_processFailedToken));
```

#### add_ScriptDialogOpening 

Fügen Sie einen Ereignishandler für das ScriptDialogOpening-Ereignis hinzu.

> Public HRESULT [add_ScriptDialogOpening](#add_scriptdialogopening)([ICoreWebView2ScriptDialogOpeningEventHandler](icorewebview2scriptdialogopeningeventhandler.md) * EventHandler, EventRegistrationToken * Token)

Das Ereignis wird ausgelöst, wenn ein JavaScript-Dialogfeld (Benachrichtigung, Bestätigung oder Eingabeaufforderung) für die WebView angezeigt wird. Dieses Ereignis wird nur ausgelöst, wenn die ICoreWebView2Settings:: AreDefaultScriptDialogsEnabled-Eigenschaft auf false festgelegt ist. Das ScriptDialogOpening-Ereignis kann verwendet werden, um Dialogfelder zu unterdrücken oder Standarddialogfelder durch benutzerdefinierte Dialogfelder zu ersetzen.

```cpp
    // Register a handler for the ScriptDialogOpening event.
    // This handler will set up a custom prompt dialog for the user,
    // and may defer the event if the setting to defer dialogs is enabled.
    CHECK_FAILURE(m_webView->add_ScriptDialogOpening(
        Callback<ICoreWebView2ScriptDialogOpeningEventHandler>(
            [this](
                ICoreWebView2* sender,
                ICoreWebView2ScriptDialogOpeningEventArgs* args) -> HRESULT
    {
        wil::com_ptr<ICoreWebView2ScriptDialogOpeningEventArgs> eventArgs = args;
        auto showDialog = [this, eventArgs]
        {
            wil::unique_cotaskmem_string uri;
            COREWEBVIEW2_SCRIPT_DIALOG_KIND type;
            wil::unique_cotaskmem_string message;
            wil::unique_cotaskmem_string defaultText;

            CHECK_FAILURE(eventArgs->get_Uri(&uri));
            CHECK_FAILURE(eventArgs->get_Kind(&type));
            CHECK_FAILURE(eventArgs->get_Message(&message));
            CHECK_FAILURE(eventArgs->get_DefaultText(&defaultText));

            std::wstring promptString = std::wstring(L"The page at '")
                + uri.get() + L"' says:";
            TextInputDialog dialog(
                m_appWindow->GetMainWindow(),
                L"Script Dialog",
                promptString.c_str(),
                message.get(),
                defaultText.get(),
                /* readonly */ type != COREWEBVIEW2_SCRIPT_DIALOG_KIND_PROMPT);
            if (dialog.confirmed)
            {
                CHECK_FAILURE(eventArgs->put_ResultText(dialog.input.c_str()));
                CHECK_FAILURE(eventArgs->Accept());
            }
        };

        if (m_deferScriptDialogs)
        {
            wil::com_ptr<ICoreWebView2Deferral> deferral;
            CHECK_FAILURE(args->GetDeferral(&deferral));
            m_completeDeferredDialog = [showDialog, deferral]
            {
                showDialog();
                CHECK_FAILURE(deferral->Complete());
            };
        }
        else
        {
            showDialog();
        }

        return S_OK;
    }).Get(), &m_scriptDialogOpeningToken));
```

#### add_SourceChanged 

Die Quelle wird ausgelöst, wenn die Quelleigenschaft geändert wird.

> Public HRESULT [add_SourceChanged](#add_sourcechanged)([ICoreWebView2SourceChangedEventHandler](icorewebview2sourcechangedeventhandler.md) * EventHandler, EventRegistrationToken * Token)

Die Quelle wird ausgelöst, um zu einer anderen Website oder zu einer anderen Fragment-Navigation zu navigieren. Sie wird nicht für andere Navigations Typen wie "Seiten-Reload" oder "History. pushState" mit der gleichen URL wie die aktuelle Seite ausgelöst. Die Quelle wird vor ContentLoading für die Navigation zu einem neuen Dokument ausgelöst. Fügen Sie einen Ereignishandler für das Quellpfad-Ereignis hinzu. 
```cpp
    // Register a handler for the SourceChanged event.
    // This handler will read the webview's source URI and update
    // the app's address bar.
    CHECK_FAILURE(m_webView->add_SourceChanged(
        Callback<ICoreWebView2SourceChangedEventHandler>(
            [this](ICoreWebView2* sender, ICoreWebView2SourceChangedEventArgs* args)
                -> HRESULT {
                wil::unique_cotaskmem_string uri;
                sender->get_Source(&uri);
                if (wcscmp(uri.get(), L"about:blank") == 0)
                {
                    uri = wil::make_cotaskmem_string(L"");
                }
                SetWindowText(GetAddressBar(), uri.get());

                return S_OK;
            })
            .Get(),
        &m_sourceChangedToken));
```

#### add_WebMessageReceived 

Dieses Ereignis wird ausgelöst, wenn die IsWebMessageEnabled-Einstellung festgelegt ist, und das Dokument auf oberster Ebene des WebView-Anrufs `window.chrome.webview.postMessage` .

> öffentliche HRESULT- [add_WebMessageReceived](#add_webmessagereceived)([ICoreWebView2WebMessageReceivedEventHandler](icorewebview2webmessagereceivedeventhandler.md) *-Handler, EventRegistrationToken *-Token)

Bei der Funktion PostMessage handelt es sich um `void postMessage(object)` ein Objekt, das von der JSON-Konvertierung unterstützt wird.

```html
        window.chrome.webview.addEventListener('message', arg => {
            if ("SetColor" in arg.data) {
                document.getElementById("colorable").style.color = arg.data.SetColor;
            }
            if ("WindowBounds" in arg.data) {
                document.getElementById("window-bounds").value = arg.data.WindowBounds;
            }
        });

        function SetTitleText() {
            let titleText = document.getElementById("title-text");
            window.chrome.webview.postMessage(`SetTitleText ${titleText.value}`);
        }
        function GetWindowBounds() {
            window.chrome.webview.postMessage("GetWindowBounds");
        }
```
 Wenn PostMessage aufgerufen wird, wird der [ICoreWebView2WebMessageReceivedEventHandler](icorewebview2webmessagereceivedeventhandler.md) -Satz über diese SetWebMessageReceivedEventHandler-Methode aufgerufen, wobei der Objektparameter der PostMessage in eine JSON-Zeichenfolge konvertiert wird.

```cpp
    // Setup the web message received event handler before navigating to
    // ensure we don't miss any messages.
    CHECK_FAILURE(m_webView->add_WebMessageReceived(
        Microsoft::WRL::Callback<ICoreWebView2WebMessageReceivedEventHandler>(
            [this](ICoreWebView2* sender, ICoreWebView2WebMessageReceivedEventArgs* args)
    {
        wil::unique_cotaskmem_string uri;
        CHECK_FAILURE(args->get_Source(&uri));

        // Always validate that the origin of the message is what you expect.
        if (uri.get() != m_sampleUri)
        {
            return S_OK;
        }
        wil::unique_cotaskmem_string messageRaw;
        CHECK_FAILURE(args->TryGetWebMessageAsString(&messageRaw));
        std::wstring message = messageRaw.get();

        if (message.compare(0, 13, L"SetTitleText ") == 0)
        {
            m_appWindow->SetTitleText(message.substr(13).c_str());
        }
        else if (message.compare(L"GetWindowBounds") == 0)
        {
            RECT bounds = m_appWindow->GetWindowBounds();
            std::wstring reply =
                L"{\"WindowBounds\":\"Left:" + std::to_wstring(bounds.left)
                + L"\\nTop:" + std::to_wstring(bounds.top)
                + L"\\nRight:" + std::to_wstring(bounds.right)
                + L"\\nBottom:" + std::to_wstring(bounds.bottom)
                + L"\"}";
            CHECK_FAILURE(sender->PostWebMessageAsJson(reply.c_str()));
        }
        return S_OK;
    }).Get(), &m_webMessageReceivedToken));
```

#### add_WebResourceRequested 

Fügen Sie einen Ereignishandler für das WebResourceRequested-Ereignis hinzu.

> Public HRESULT [add_WebResourceRequested](#add_webresourcerequested)([ICoreWebView2WebResourceRequestedEventHandler](icorewebview2webresourcerequestedeventhandler.md) * EventHandler, EventRegistrationToken * Token)

Wird ausgelöst, wenn die WebView eine URL-Anforderung für einen übereinstimmenden URL-und Ressourcenkontext Filter ausführt, der mit AddWebResourceRequestedFilter hinzugefügt wurde. Es muss mindestens ein Filter hinzugefügt werden, damit das Ereignis ausgelöst wird.

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

#### add_WindowCloseRequested 

Fügen Sie einen Ereignishandler für das WindowCloseRequested-Ereignis hinzu.

> Public HRESULT [add_WindowCloseRequested](#add_windowcloserequested)([ICoreWebView2WindowCloseRequestedEventHandler](icorewebview2windowcloserequestedeventhandler.md) * EventHandler, EventRegistrationToken * Token)

Wird ausgelöst, wenn der Inhalt in der WebView zum Schließen des Fensters angefordert wird, beispielsweise nach dem Aufruf von Window. Close. Die APP sollte das Fenster WebView und verwandte APP schließen, wenn dies für die APP sinnvoll ist.

```cpp
    // Register a handler for the WindowCloseRequested event.
    // This handler will close the app window if it is not the main window.
    CHECK_FAILURE(m_webView->add_WindowCloseRequested(
        Callback<ICoreWebView2WindowCloseRequestedEventHandler>([this](
                                                                    ICoreWebView2* sender,
                                                                    IUnknown* args) {
            if (m_isPopupWindow)
            {
                CloseAppWindow();
            }
            return S_OK;
        }).Get(),
        nullptr));
```

#### AddHostObjectToScript 

Fügen Sie das bereitgestellte Hostobjekt zu Skript hinzu, das in der WebView mit dem angegebenen Namen ausgeführt wird.

> Public HRESULT [AddHostObjectToScript](#addhostobjecttoscript)(LPCWSTR-Name; Variant *-Objekt)

Hostobjekte werden als Hostobjekt Proxys über `window.chrome.webview.hostObjects.<name>` . Hostobjekt Proxys sind Versprechungen und werden in ein Objekt aufgelöst, das das Hostobjekt darstellt. Das Versprechen wird abgelehnt, wenn die APP kein Objekt mit dem Namen hinzugefügt hat. Wenn JavaScript-Code auf eine Eigenschaft oder Methode des Objekts zugreift, wird eine Zusage zurückgegeben, die in den Wert aufgelöst wird, der vom Host für die Eigenschaft oder Methode zurückgegeben wird, oder im Fall eines Fehlers abgelehnt wird, beispielsweise wenn keine solche Eigenschaft oder Methode für das Objekt vorhanden ist oder Parameter ungültig sind. Wenn der Anwendungscode beispielsweise Folgendes durchführt:

```
VARIANT object;
object.vt = VT_DISPATCH;
object.pdispVal = appObject;
webview->AddHostObjectToScript(L"host_object", &host);
```

JavaScript-Code in der WebView kann auf appObject wie folgt zugreifen und dann auf Attribute und Methoden von appObject zugreifen:

```
let app_object = await window.chrome.webview.hostObjects.host_object;
let attr1 = await app_object.attr1;
let result = await app_object.method1(parameters);
```

Beachten Sie, dass einfache Typen, IDispatch und Array unterstützt werden, generische IUnknown, VT_DECIMAL oder VT_RECORD Variant nicht unterstützt werden. Remote-JavaScript-Objekte wie Rückruffunktionen werden als VT_DISPATCH Variante mit dem Object-Implementierungs-IDispatch dargestellt. Die JavaScript-Rückrufmethode kann mit DISPID_VALUE für die DISPID aufgerufen werden. Geschachtelte Arrays werden bis zu einer Tiefe von 3 unterstützt. Arrays von nach Verweistypen werden nicht unterstützt. VT_EMPTY und VT_NULL werden JavaScript als NULL zugeordnet. In JavaScript werden NULL und undefined VT_EMPTY zugeordnet.

Darüber hinaus werden alle Hostobjekte als verfügbar gemacht `window.chrome.webview.hostObjects.sync.<name>` . Hier werden die Hostobjekte als synchrone Hostobjekt Proxys verfügbar gemacht. Hierbei handelt es sich nicht um Versprechungen und Aufrufe von Funktionen oder des Eigenschafts Zugriffs, die ein synchrones Blockieren des ausgeführten Skripts warten, um die Ausführung des Host Codes zu kommunizieren. Dementsprechend kann dies zu Zuverlässigkeitsproblemen führen, und es wird empfohlen, dass Sie die oben beschriebene Versprechen-basierte asynchrone `window.chrome.webview.hostObjects.<name>` API verwenden.

Synchrone Hostobjekt Proxys und asynchrone Hostobjekt Proxys können beide Proxys für dasselbe Hostobjekt bereithalten. Remote Änderungen, die von einem Proxy durchgeführt werden, werden in jedem anderen Proxy desselben Hostobjekts widergespiegelt, unabhängig davon, ob die anderen Proxys synchron oder asynchron sind.

Während JavaScript bei einem synchronen Aufruf von systemeigenem Code blockiert wird, kann dieser systemeigene Code nicht mehr in JavaScript zurückrufen. Der Versuch, dies zu tun, schlägt mit HRESULT_FROM_WIN32 (ERROR_POSSIBLE_DEADLOCK) fehl.

Host Objektproxys sind JavaScript-Proxy Objekte, die alle Eigenschaften abrufen, Eigenschaftensätze und Methodenaufrufe abfangen. Eigenschaften oder Methoden, die Teil des Funktions-oder Objekt Prototyps sind, werden lokal ausgeführt. Darüber hinaus werden alle Eigenschaften oder Methoden im Array `chrome.webview.hostObjects.options.forceLocalProperties` lokal ausgeführt. Diese Option enthält standardmäßig optionale Methoden, die in JavaScript wie und in Bedeutung sind `toJSON` `Symbol.toPrimitive` . Sie können diesem Array nach Bedarf weitere hinzufügen.

Es gibt eine Methode `chrome.webview.hostObjects.cleanupSome` , mit der die Garbage Collection von Hostobjekt Proxys am besten abläuft.

Host Objektproxys verfügen zusätzlich über die folgenden Methoden, die lokal ausgeführt werden:

* applyHostFunction, gethostproperty, sethostproperty: führen Sie einen Methodenaufruf, eine Eigenschaft Get oder einen Eigenschaftssatz für das Hostobjekt aus. Mit diesen können Sie explizit erzwingen, dass eine Methode oder Eigenschaft Remote ausgeführt wird, wenn eine in Konflikt stehende lokale Methode oder Eigenschaft vorhanden ist. Beispielsweise führt `proxy.toString()` die lokale ToString-Methode für das Proxyobjekt aus. `proxy.applyHostFunction('toString')`Wird aber `toString` stattdessen auf dem Host Proxyobjekt ausgeführt.

* getlocalproperty, setlocalproperty: Ausführen von Eigenschaften abrufen oder Eigenschaftssatz lokal. Sie können diese Methoden verwenden, um das Abrufen oder Festlegen einer Eigenschaft für den Hostobjekt Proxy selbst zu erzwingen, anstatt auf das Hostobjekt, das es darstellt. Beispielsweise `proxy.unknownProperty` wird die Eigenschaft abgerufen, die `unknownProperty` aus dem Host Proxyobjekt benannt wurde. `proxy.getLocalProperty('unknownProperty')`Der Wert der Eigenschaft wird jedoch `unknownProperty` für das Proxyobjekt selbst abgerufen.

* Synchronisierung: asynchrone Hostobjekt Proxys machen eine Synchronisierungsmethode verfügbar, die eine Versprechung für einen synchronen Hostobjekt Proxy für dasselbe Hostobjekt zurückgibt. Gibt beispielsweise `chrome.webview.hostObjects.sample.methodCall()` einen asynchronen Hostobjekt Proxy zurück. Stattdessen können Sie die `sync` Methode zum Abrufen eines synchronen Hostobjekt Proxys verwenden: `const syncProxy = await chrome.webview.hostObjects.sample.methodCall().sync()`

* Async: synchrone Hostobjekt Proxys machen eine asynchrone Methode verfügbar, die einen asynchronen Hostobjekt Proxy für dasselbe Hostobjekt blockiert und zurückgibt. Gibt beispielsweise `chrome.webview.hostObjects.sync.sample.methodCall()` einen synchronen Hostobjekt Proxy zurück. Aufruf der `async` Methode für diesen Block und anschließendes zurückgeben eines asynchronen Hostobjekt Proxys für dasselbe Hostobjekt: `const asyncProxy = chrome.webview.hostObjects.sync.sample.methodCall().async()`

* dann: asynchrone Hostobjekt Proxys verfügen über eine then-Methode. Auf diese Weise können Sie warten. `then` gibt eine Verheißung zurück, die mit einer Darstellung des Hostobjekts aufgelöst wird. Wenn der Proxy ein JavaScript-Literal darstellt, wird eine Kopie davon lokal zurückgegeben. Wenn der Proxy eine Funktion darstellt, wird ein nicht erwarteter Proxy zurückgegeben. Wenn der Proxy ein JavaScript-Objekt mit einer Kombination aus Literalen Eigenschaften und Funktionseigenschaften darstellt, wird eine Kopie des Objekts mit einigen Eigenschaften als Hostobjekt Proxys zurückgegeben.

Alle anderen Eigenschaften-und Methodenaufrufe (außer den oben genannten Methoden für Remote Objektproxy, forceLocalProperties-Liste und Eigenschaften für Funktions-und Objekt Prototypen) werden Remote ausgeführt. Asynchrone Hostobjekt Proxys geben eine Versprechung zurück, die den asynchronen Abschluss des Remoteaufrufs der Methode oder das Abrufen der Eigenschaft darstellt. Das Versprechen wird aufgelöst, nachdem die Remotevorgänge abgeschlossen sind und die Zusagen in den resultierenden Wert des Vorgangs aufgelöst werden. Synchrone Hostobjekt Proxys funktionieren ähnlich, blockieren aber die JavaScript-Ausführung und warten, bis der Remotevorgang abgeschlossen ist.

Das Festlegen einer Eigenschaft für einen asynchronen Hostobjekt Proxy funktioniert etwas anders. Der Satz wird sofort zurückgegeben, und der Rückgabewert ist der Wert, der festgesetzt wird. Dies ist eine Anforderung des JavaScript-Proxy Objekts. Wenn Sie asynchron warten müssen, bis der Eigenschaftssatz abgeschlossen ist, verwenden Sie die sethostproperty-Methode, die eine Verheißung zurückgibt, wie oben beschrieben. Eigenschaft für synchrone Objekteigenschaft festlegen synchron blockiert, bis die Eigenschaft gesetzt ist.

Angenommen, Sie verfügen über ein COM-Objekt mit der folgenden Schnittstelle.

```idl
    [uuid(3a14c9c0-bc3e-453f-a314-4ce4a0ec81d8), object, local]
    interface IHostObjectSample : IUnknown
    {
        // Demonstrate basic method call with some parameters and a return value.
        HRESULT MethodWithParametersAndReturnValue([in] BSTR stringParameter, [in] INT integerParameter, [out, retval] BSTR* stringResult);

        // Demonstrate getting and setting a property.
        [propget] HRESULT Property([out, retval] BSTR* stringResult);
        [propput] HRESULT Property([in] BSTR stringValue);

        [propget] HRESULT IndexedProperty(INT index, [out, retval] BSTR * stringResult);
        [propput] HRESULT IndexedProperty(INT index, [in] BSTR stringValue);

        // Demonstrate native calling back into JavaScript.
        HRESULT CallCallbackAsynchronously([in] IDispatch* callbackParameter);

    };
```
 Wir können eine Instanz dieser Schnittstelle in unserem JavaScript mit hinzufügen `AddHostObjectToScript` . In diesem Fall nennen wir `sample` Folgendes:

```cpp
            VARIANT remoteObjectAsVariant = {};
            m_hostObject.query_to<IDispatch>(&remoteObjectAsVariant.pdispVal);
            remoteObjectAsVariant.vt = VT_DISPATCH;

            // We can call AddHostObjectToScript multiple times in a row without
            // calling RemoveHostObject first. This will replace the previous object
            // with the new object. In our case this is the same object and everything
            // is fine.
            CHECK_FAILURE(
                m_webView->AddHostObjectToScript(L"sample", &remoteObjectAsVariant));
            remoteObjectAsVariant.pdispVal->Release();
```
 Im HTML-Dokument können wir dieses COM-Objekt dann über `chrome.webview.hostObjects.sample` Folgendes verwenden:

```html
        document.getElementById("getPropertyAsyncButton").addEventListener("click", async () => {
        const propertyValue = await chrome.webview.hostObjects.sample.property;
        document.getElementById("getPropertyAsyncOutput").textContent = propertyValue;
        });

        document.getElementById("getPropertySyncButton").addEventListener("click", () => {
        const propertyValue = chrome.webview.hostObjects.sync.sample.property;
        document.getElementById("getPropertySyncOutput").textContent = propertyValue;
        });

        document.getElementById("setPropertyAsyncButton").addEventListener("click", async () => {
        const propertyValue = document.getElementById("setPropertyAsyncInput").value;
        // The following line will work but it will return immediately before the property value has actually been set.
        // If you need to set the property and wait for the property to change value, use the setRemote function.
        chrome.webview.hostObjects.sample.property = propertyValue;
        document.getElementById("setPropertyAsyncOutput").textContent = "Set";
        });

        document.getElementById("setPropertyExplicitAsyncButton").addEventListener("click", async () => {
        const propertyValue = document.getElementById("setPropertyExplicitAsyncInput").value;
        // If you care about waiting until the property has actually changed value use the setRemote function.
        await chrome.webview.hostObjects.sample.setRemote("property", propertyValue);
        document.getElementById("setPropertyExplicitAsyncOutput").textContent = "Set";
        });

        document.getElementById("setPropertySyncButton").addEventListener("click", () => {
        const propertyValue = document.getElementById("setPropertySyncInput").value;
        chrome.webview.hostObjects.sync.sample.property = propertyValue;
        document.getElementById("setPropertySyncOutput").textContent = "Set";
        });

        document.getElementById("getIndexedPropertyAsyncButton").addEventListener("click", async () => {
        const index = parseInt(document.getElementById("getIndexedPropertyAsyncParam").value);
        const resultValue = await chrome.webview.hostObjects.sample.IndexedProperty[index];
        document.getElementById("getIndexedPropertyAsyncOutput").textContent = resultValue;
        });
        document.getElementById("setIndexedPropertyAsyncButton").addEventListener("click", async () => {
        const index = parseInt(document.getElementById("setIndexedPropertyAsyncParam1").value);
        const value = document.getElementById("setIndexedPropertyAsyncParam2").value;;
        chrome.webview.hostObjects.sample.IndexedProperty[index] = value;
        document.getElementById("setIndexedPropertyAsyncOutput").textContent = "Set";
        });
        document.getElementById("invokeMethodAsyncButton").addEventListener("click", async () => {
        const paramValue1 = document.getElementById("invokeMethodAsyncParam1").value;
        const paramValue2 = parseInt(document.getElementById("invokeMethodAsyncParam2").value);
        const resultValue = await chrome.webview.hostObjects.sample.MethodWithParametersAndReturnValue(paramValue1, paramValue2);
        document.getElementById("invokeMethodAsyncOutput").textContent = resultValue;
        });

        document.getElementById("invokeMethodSyncButton").addEventListener("click", () => {
        const paramValue1 = document.getElementById("invokeMethodSyncParam1").value;
        const paramValue2 = parseInt(document.getElementById("invokeMethodSyncParam2").value);
        const resultValue = chrome.webview.hostObjects.sync.sample.MethodWithParametersAndReturnValue(paramValue1, paramValue2);
        document.getElementById("invokeMethodSyncOutput").textContent = resultValue;
        });

        let callbackCount = 0;
        document.getElementById("invokeCallbackButton").addEventListener("click", async () => {
        chrome.webview.hostObjects.sample.CallCallbackAsynchronously(() => {
        document.getElementById("invokeCallbackOutput").textContent = "Native object called the callback " + (++callbackCount) + " time(s).";
        });
        });
```
Das verfügbar machen von Host Objekten für Skripts hat ein Sicherheitsrisiko. Befolgen Sie die [bewährten Methoden](https://docs.microsoft.com/microsoft-edge/webview2/concepts/security).

#### AddScriptToExecuteOnDocumentCreated 

Fügen Sie das bereitgestellte JavaScript einer Liste von Skripts hinzu, die ausgeführt werden sollen, nachdem das globale Objekt erstellt wurde, aber bevor das HTML-Dokument analysiert wurde und bevor ein anderes Skript ausgeführt wird, das vom HTML-Dokument eingeschlossen ist.

> Public HRESULT [AddScriptToExecuteOnDocumentCreated](#addscripttoexecuteondocumentcreated)(LPCWSTR javaScript, [ICoreWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler](icorewebview2addscripttoexecuteondocumentcreatedcompletedhandler.md) * Handler)

Mit dieser Methode wird ein Skript eingefügt, das auf allen Dokument-und untergeordneten Frameseiten Navigationen auf oberster Ebene ausgeführt wird. Diese Methode wird asynchron ausgeführt, und Sie müssen warten, bis der vervollständigungshandler fertig ist, bevor das eingefügte Skript ausgeführt werden kann. Nach Abschluss dieser Methode wird die Methode des Handlers `Invoke` mit dem `id` injizierten Skript aufgerufen. `id` ist eine Zeichenfolge. Wenn Sie das eingefügte Skript entfernen möchten, verwenden Sie `RemoveScriptToExecuteOnDocumentCreated` .

Beachten Sie, dass sich dies auf das hier ausgeführte Skript auswirkt, wenn ein HTML-Dokument über Sandbox [-Eigenschaften oder über den](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/iframe#attr-sandbox) [Content-Security-Policy-HTTP-Header](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Content-Security-Policy) eine Art Sandbox hat. Wenn also beispielsweise das Schlüsselwort "Allow-modals" nicht festgesetzt ist, werden Aufrufe der `alert` Funktion ignoriert.

```cpp
// Prompt the user for some script and register it to execute whenever a new page loads.
void ScriptComponent::AddInitializeScript()
{
    TextInputDialog dialog(
        m_appWindow->GetMainWindow(),
        L"Add Initialize Script",
        L"Initialization Script:",
        L"Enter the JavaScript code to run as the initialization script that "
            L"runs before any script in the HTML document.",
    // This example script stops child frames from opening new windows.  Because
    // the initialization script runs before any script in the HTML document, we
    // can trust the results of our checks on window.parent and window.top.
        L"if (window.parent !== window.top) {\r\n"
        L"    delete window.open;\r\n"
        L"}");
    if (dialog.confirmed)
    {
        m_webView->AddScriptToExecuteOnDocumentCreated(
            dialog.input.c_str(),
            Callback<ICoreWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler>(
                [this](HRESULT error, PCWSTR id) -> HRESULT
        {
            m_lastInitializeScriptId = id;
            MessageBox(nullptr, id, L"AddScriptToExecuteOnDocumentCreated Id", MB_OK);
            return S_OK;
        }).Get());

    }
}
```

#### AddWebResourceRequestedFilter 

Fügt dem WebResourceRequested-Ereignis einen URI-und Ressourcenkontext Filter hinzu.

> Public HRESULT [AddWebResourceRequestedFilter](#addwebresourcerequestedfilter)(LPCWSTR const URI, [COREWEBVIEW2_WEB_RESOURCE_CONTEXT](#corewebview2_web_resource_context) const resourcecontext)

Der URI-Parameter kann eine Platzhalterzeichenfolge (' ': 0 oder mehr; '? ': genau eins) sein. nullptr entspricht L "". Eine Beschreibung der Ressourcenkontext Filter finden Sie unter COREWEBVIEW2_WEB_RESOURCE_CONTEXT Enum.

#### CallDevToolsProtocolMethod 

Rufen Sie eine asynchrone DevToolsProtocol-Methode auf.

> Public HRESULT [CallDevToolsProtocolMethod](#calldevtoolsprotocolmethod)(LPCWSTR MethodName, LPCWSTR parametersAsJson, [ICoreWebView2CallDevToolsProtocolMethodCompletedHandler](icorewebview2calldevtoolsprotocolmethodcompletedhandler.md) * Handler)

Eine Liste und eine Beschreibung der verfügbaren Methoden finden Sie im [devtools-Protokoll-Viewer](https://aka.ms/DevToolsProtocolDocs) . Der MethodName-Parameter ist der vollständige Name der Methode im Format `{domain}.{method}` . Der parametersAsJson-Parameter ist eine JSON-formatierte Zeichenfolge, die die Parameter für die entsprechende Methode enthält. Die Invoke-Methode des Handlers wird aufgerufen, wenn die Methode asynchron abgeschlossen wird. Invoke wird mit dem Rückgabeobjekt der Methode als JSON-Zeichenfolge aufgerufen.

```cpp
// Prompt the user for the name and parameters of a CDP method, then call it.
void ScriptComponent::CallCdpMethod()
{
    TextInputDialog dialog(
        m_appWindow->GetMainWindow(),
        L"Call CDP Method",
        L"CDP method name:",
        L"Enter the CDP method name to call, followed by a space,\r\n"
            L"followed by the parameters in JSON format.",
        L"Runtime.evaluate {\"expression\":\"alert(\\\"test\\\")\"}");
    if (dialog.confirmed)
    {
        size_t delimiterPos = dialog.input.find(L' ');
        std::wstring methodName = dialog.input.substr(0, delimiterPos);
        std::wstring methodParams =
            (delimiterPos < dialog.input.size()
                ? dialog.input.substr(delimiterPos + 1)
                : L"{}");

        m_webView->CallDevToolsProtocolMethod(
            methodName.c_str(),
            methodParams.c_str(),
            Callback<ICoreWebView2CallDevToolsProtocolMethodCompletedHandler>(
                [](HRESULT error, PCWSTR resultJson) -> HRESULT
                {
                    MessageBox(nullptr, resultJson, L"CDP Method Result", MB_OK);
                    return S_OK;
                }).Get());
    }
}
```

#### CapturePreview 

Erfassen Sie ein Bild von der Anzeige von WebView.

> Public HRESULT [CapturePreview](#capturepreview)([COREWEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT](#corewebview2_capture_preview_image_format) Image Format, IStream * ImageStream, [ICoreWebView2CapturePreviewCompletedHandler](icorewebview2capturepreviewcompletedhandler.md) *-Handler)

Geben Sie das Format des Bilds mit dem ImageFormat-Parameter an. Die resultierenden Bild Binärdaten werden in den bereitgestellten ImageStream-Parameter geschrieben. Wenn CapturePreview den Schreibvorgang in den Datenstrom abgeschlossen hat, wird die Invoke-Methode für den bereitgestellten Handler-Parameter aufgerufen.

```cpp
// Show the user a file selection dialog, then save a screenshot of the WebView
// to the selected file.
void FileComponent::SaveScreenshot()
{
    OPENFILENAME openFileName = {};
    openFileName.lStructSize = sizeof(openFileName);
    openFileName.hwndOwner = nullptr;
    openFileName.hInstance = nullptr;
    WCHAR fileName[MAX_PATH] = L"WebView2_Screenshot.png";
    openFileName.lpstrFile = fileName;
    openFileName.lpstrFilter = L"PNG File\0*.png\0";
    openFileName.nMaxFile = ARRAYSIZE(fileName);
    openFileName.Flags = OFN_OVERWRITEPROMPT;

    if (GetSaveFileName(&openFileName))
    {
        wil::com_ptr<IStream> stream;
        CHECK_FAILURE(SHCreateStreamOnFileEx(
            fileName, STGM_READWRITE | STGM_CREATE, FILE_ATTRIBUTE_NORMAL, TRUE, nullptr,
            &stream));

        HWND mainWindow = m_appWindow->GetMainWindow();

        CHECK_FAILURE(m_webView->CapturePreview(
            COREWEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT_PNG, stream.get(),
            Callback<ICoreWebView2CapturePreviewCompletedHandler>(
                [mainWindow](HRESULT error_code) -> HRESULT {
                    CHECK_FAILURE(error_code);

                    MessageBox(mainWindow, L"Preview Captured", L"Preview Captured", MB_OK);
                    return S_OK;
                })
                .Get()));
    }
}
```

#### ExecuteScript 

Führen Sie JavaScript-Code aus dem JavaScript-Parameter im aktuellen Dokument der obersten Ebene aus, das in der WebView gerendert wird.

> Public HRESULT [executeScript](#executescript)(LPCWSTR javaScript, [ICoreWebView2ExecuteScriptCompletedHandler](icorewebview2executescriptcompletedhandler.md) * Handler)

Dies wird asynchron ausgeführt, und wenn ein Handler im ExecuteScriptCompletedHandler-Parameter bereitgestellt wird, wird die Invoke-Methode mit dem Ergebnis der Auswertung des bereitgestellten JavaScript aufgerufen. Der Ergebniswert ist eine JSON-codierte Zeichenfolge. Wenn das Ergebnis undefiniert ist, einen Referenz Zyklus enthält oder in JSON nicht codiert werden kann, wird der JSON-NULL-Wert als Zeichenfolge "Null" zurückgegeben. Beachten Sie, dass eine Funktion, die keinen expliziten Rückgabewert aufweist, undefined zurückgibt. Wenn das ausgeführte Skript eine nicht behandelte Ausnahme auslöst, ist das Ergebnis auch "Null". Diese Methode wird asynchron angewendet. Wenn die Methode nach dem NavigationStarting-Ereignis während einer Navigation aufgerufen wird, wird das Skript beim Laden des Skripts im neuen Dokument ausgeführt, und zwar um den Zeitpunkt, zu dem ContentLoading ausgelöst wird. ExecuteScript funktioniert auch dann, wenn IsScriptEnabled auf "false" festgelegt ist.

```cpp
// Prompt the user for some script and then execute it.
void ScriptComponent::InjectScript()
{
    TextInputDialog dialog(
        m_appWindow->GetMainWindow(),
        L"Inject Script",
        L"Enter script code:",
        L"Enter the JavaScript code to run in the webview.",
        L"window.getComputedStyle(document.body).backgroundColor");
    if (dialog.confirmed)
    {
        m_webView->ExecuteScript(dialog.input.c_str(),
            Callback<ICoreWebView2ExecuteScriptCompletedHandler>(
                [](HRESULT error, PCWSTR result) -> HRESULT
        {
            if (error != S_OK) {
                ShowFailure(error, L"ExecuteScript failed");
            }
            MessageBox(nullptr, result, L"ExecuteScript Result", MB_OK);
            return S_OK;
        }).Get());
    }
}
```

#### get_BrowserProcessId 

Die Prozess-ID des Browser Prozesses, der die WebView hostet.

> Public HRESULT [get_BrowserProcessId](#get_browserprocessid)(UInt32 *-Wert)

#### get_CanGoBack 

Gibt "true" zurück, wenn die WebView zu einer vorherigen Seite im Navigationsverlauf navigieren kann.

> Public HRESULT [get_CanGoBack](#get_cangoback)(bool * CanGoBack)

Das History-Ereignis wird ausgelöst, wenn der Wert von CanGoBack geändert wird.

#### get_CanGoForward 

Gibt "true" zurück, wenn die WebView zu einer nächsten Seite im Navigationsverlauf navigieren kann.

> Public HRESULT [get_CanGoForward](#get_cangoforward)(bool * CanGoForward)

Das History-Ereignis wird ausgelöst, wenn der Wert von CanGoForward geändert wird.

#### get_ContainsFullScreenElement 

Gibt an, ob die WebView ein HTML-Vollbild-Element enthält.

> Public HRESULT [get_ContainsFullScreenElement](#get_containsfullscreenelement)(bool * ContainsFullScreenElement)

#### get_DocumentTitle 

Der Titel für das aktuelle Dokument der obersten Ebene.

> öffentliche HRESULT- [get_DocumentTitle](#get_documenttitle)(LPWSTR * Title)

Wenn das Dokument keinen expliziten Titel hat oder sonst leer ist, wird ein Standardwert verwendet, der möglicherweise nicht mit dem URI des Dokuments übereinstimmt.

#### get_Settings 

Das [ICoreWebView2Settings](icorewebview2settings.md) -Objekt enthält verschiedene änderbare Einstellungen für den ausgeführten WebView.

> öffentliche HRESULT- [get_Settings](#get_settings)([ICoreWebView2Settings](icorewebview2settings.md) * *-Einstellungen)

#### get_Source 

Der URI des aktuellen Dokuments auf oberster Ebene.

> Public HRESULT [get_Source](#get_source)(LPWSTR * URI)

Dieser Wert ändert sich möglicherweise als Teil der Ereignis Befeuerungs Quelle für einige Fälle, beispielsweise das Navigieren zu einer anderen Website oder zu einer anderen Fragment-Navigation. Sie bleibt bei anderen Navigations Typen wie "Seiten-Reload" oder "History. pushState" unverändert, wobei dieselbe URL wie die aktuelle Seite angezeigt wird.

```cpp
    // Register a handler for the SourceChanged event.
    // This handler will read the webview's source URI and update
    // the app's address bar.
    CHECK_FAILURE(m_webView->add_SourceChanged(
        Callback<ICoreWebView2SourceChangedEventHandler>(
            [this](ICoreWebView2* sender, ICoreWebView2SourceChangedEventArgs* args)
                -> HRESULT {
                wil::unique_cotaskmem_string uri;
                sender->get_Source(&uri);
                if (wcscmp(uri.get(), L"about:blank") == 0)
                {
                    uri = wil::make_cotaskmem_string(L"");
                }
                SetWindowText(GetAddressBar(), uri.get());

                return S_OK;
            })
            .Get(),
        &m_sourceChangedToken));
```

#### GetDevToolsProtocolEventReceiver 

Rufen Sie einen devtools-Protokollereignis Empfänger ab, mit dem Sie ein devtools-Protokollereignis abonnieren können.

> Public HRESULT [GetDevToolsProtocolEventReceiver](#getdevtoolsprotocoleventreceiver)(LPCWSTR EventName, [ICoreWebView2DevToolsProtocolEventReceiver](icorewebview2devtoolsprotocoleventreceiver.md) * * Receiver)

Der eventName-Parameter ist der vollständige Name des Ereignisses im Format `{domain}.{event}` . Eine Liste der Beschreibungen von devtools-Protokollereignissen und Ereignis args finden Sie im [devtools-Protokoll-Viewer](https://aka.ms/DevToolsProtocolDocs) .

```cpp
// Prompt the user to name a CDP event, and then subscribe to that event.
void ScriptComponent::SubscribeToCdpEvent()
{
    TextInputDialog dialog(
        m_appWindow->GetMainWindow(),
        L"Subscribe to CDP Event",
        L"CDP event name:",
        L"Enter the name of the CDP event to subscribe to.\r\n"
            L"You may also have to call the \"enable\" method of the\r\n"
            L"event's domain to receive events (for example \"Log.enable\").\r\n",
        L"Log.entryAdded");
    if (dialog.confirmed)
    {
        std::wstring eventName = dialog.input;
        wil::com_ptr<ICoreWebView2DevToolsProtocolEventReceiver> receiver;
        CHECK_FAILURE(
            m_webView->GetDevToolsProtocolEventReceiver(eventName.c_str(), &receiver));

        // If we are already subscribed to this event, unsubscribe first.
        auto preexistingToken = m_devToolsProtocolEventReceivedTokenMap.find(eventName);
        if (preexistingToken != m_devToolsProtocolEventReceivedTokenMap.end())
        {
            CHECK_FAILURE(receiver->remove_DevToolsProtocolEventReceived(
                preexistingToken->second));
        }

        CHECK_FAILURE(receiver->add_DevToolsProtocolEventReceived(
            Callback<ICoreWebView2DevToolsProtocolEventReceivedEventHandler>(
                [eventName](
                    ICoreWebView2* sender,
                    ICoreWebView2DevToolsProtocolEventReceivedEventArgs* args) -> HRESULT {
                    wil::unique_cotaskmem_string parameterObjectAsJson;
                    CHECK_FAILURE(args->get_ParameterObjectAsJson(&parameterObjectAsJson));
                    MessageBox(
                        nullptr, parameterObjectAsJson.get(),
                        (L"CDP Event Fired: " + eventName).c_str(), MB_OK);
                    return S_OK;
                })
                .Get(),
            &m_devToolsProtocolEventReceivedTokenMap[eventName]));
    }
}
```

#### GoBack 

Navigiert die WebView zur vorherigen Seite im Navigationsverlauf.

> Public HRESULT [GoBack](#goback)()

#### GoForward 

Navigiert die WebView zur nächsten Seite im Navigationsverlauf.

> Public HRESULT [GoForward](#goforward)()

#### %%amp;quot;Navigate%%amp;quot;
 

Führen Sie eine Navigation des Dokuments auf oberster Ebene zum angegebenen URI.

> öffentliche HRESULT- [Navigation](#navigate)(LPCWSTR-URI)

Weitere Informationen finden Sie in den Navigations Ereignissen. Beachten Sie, dass dadurch eine Navigation gestartet wird und das entsprechende NavigationStarting-Ereignis irgendwann ausgelöst wird, nachdem dieser Navigate-Aufruf abgeschlossen ist.

```cpp
void ControlComponent::NavigateToAddressBar()
{
    int length = GetWindowTextLength(GetAddressBar());
    std::wstring uri(length, 0);
    PWSTR buffer = const_cast<PWSTR>(uri.data());
    GetWindowText(GetAddressBar(), buffer, length + 1);

    HRESULT hr = m_webView->Navigate(uri.c_str());
    if (hr == E_INVALIDARG)
    {
        // An invalid URI was provided.
        if (uri.find(L' ') == std::wstring::npos
            && uri.find(L'.') != std::wstring::npos)
        {
            // If it contains a dot and no spaces, try tacking http:// on the front.
            hr = m_webView->Navigate((L"http://" + uri).c_str());
        }
        else
        {
            // Otherwise treat it as a web search. We aren't bothering to escape
            // URL syntax characters such as & and #
            hr = m_webView->Navigate((L"https://bing.com/search?q=" + uri).c_str());
        }
    }
    if (hr != E_INVALIDARG) {
        CHECK_FAILURE(hr);
    }
}
```

#### NavigateToString 

Initiiert eine Navigation zu htmlContent als HTML-Code für ein neues Dokument.

> Public HRESULT [NavigateToString](#navigatetostring)(LPCWSTR htmlContent)

Der htmlContent-Parameter darf nicht größer als 2 MB Zeichen sein. Der Ursprung der neuen Seite lautet: leer.

```cpp
            static const PCWSTR htmlContent =
              L"<h1>Domain Blocked</h1>"
              L"<p>You've attempted to navigate to a domain in the blocked "
              L"sites list. Press back to return to the previous page.</p>";
            CHECK_FAILURE(sender->NavigateToString(htmlContent));
```

#### OpenDevToolsWindow 

Öffnet das devtools-Fenster für das aktuelle Dokument in der WebView.

> Public HRESULT [OpenDevToolsWindow](#opendevtoolswindow)()

Wenn das devtools-Fenster bereits geöffnet ist, wird nichts aufgerufen

#### PostWebMessageAsJson 

Posten Sie die angegebene Webnachricht im Dokument der obersten Ebene in dieser WebView.

> Public HRESULT [PostWebMessageAsJson](#postwebmessageasjson)(LPCWSTR webMessageAsJson)

Das Nachrichtenereignis des Fensters "Window. Chrome. WebView" des obersten Dokuments wird ausgelöst. JavaScript in diesem Dokument kann das Ereignis über Folgendes abonnieren und kündigen:

```
window.chrome.webview.addEventListener('message', handler)
window.chrome.webview.removeEventListener('message', handler)
```

Das Ereignis args ist eine Instanz von `MessageEvent` . Die ICoreWebView2Settings:: IsWebMessageEnabled-Einstellung muss wahr sein, oder diese Methode schlägt mit E_INVALIDARG fehl. Die Dateneigenschaft des Ereignisses arg ist der webmessage-Zeichenfolgenparameter, der als JSON-Zeichenfolge in ein JavaScript-Objekt analysiert wurde. Die Source-Eigenschaft des Ereignisses arg ist ein Verweis auf das `window.chrome.webview` Objekt. Informationen zum Senden von Nachrichten aus dem HTML-Dokument in der WebView an den Host finden Sie unter SetWebMessageReceivedEventHandler. Diese Nachricht wird asynchron gesendet. Wenn eine Navigation erfolgt, bevor die Nachricht auf der Seite veröffentlicht wird, wird die Nachricht nicht gesendet.

```cpp
    // Setup the web message received event handler before navigating to
    // ensure we don't miss any messages.
    CHECK_FAILURE(m_webView->add_WebMessageReceived(
        Microsoft::WRL::Callback<ICoreWebView2WebMessageReceivedEventHandler>(
            [this](ICoreWebView2* sender, ICoreWebView2WebMessageReceivedEventArgs* args)
    {
        wil::unique_cotaskmem_string uri;
        CHECK_FAILURE(args->get_Source(&uri));

        // Always validate that the origin of the message is what you expect.
        if (uri.get() != m_sampleUri)
        {
            return S_OK;
        }
        wil::unique_cotaskmem_string messageRaw;
        CHECK_FAILURE(args->TryGetWebMessageAsString(&messageRaw));
        std::wstring message = messageRaw.get();

        if (message.compare(0, 13, L"SetTitleText ") == 0)
        {
            m_appWindow->SetTitleText(message.substr(13).c_str());
        }
        else if (message.compare(L"GetWindowBounds") == 0)
        {
            RECT bounds = m_appWindow->GetWindowBounds();
            std::wstring reply =
                L"{\"WindowBounds\":\"Left:" + std::to_wstring(bounds.left)
                + L"\\nTop:" + std::to_wstring(bounds.top)
                + L"\\nRight:" + std::to_wstring(bounds.right)
                + L"\\nBottom:" + std::to_wstring(bounds.bottom)
                + L"\"}";
            CHECK_FAILURE(sender->PostWebMessageAsJson(reply.c_str()));
        }
        return S_OK;
    }).Get(), &m_webMessageReceivedToken));
```

#### PostWebMessageAsString 

Dies ist ein Helfer zum Posten einer Nachricht, bei der es sich um eine einfache Zeichenfolge und nicht um eine JSON-Zeichenfolgendarstellung eines JavaScript-Objekts handelt.

> Public HRESULT [PostWebMessageAsString](#postwebmessageasstring)(LPCWSTR webMessageAsString)

Dies verhält sich auf die gleiche Weise wie PostWebMessageAsJson, aber die `window.chrome.webview` Dateneigenschaft des Nachrichtenereignisses arg ist eine Zeichenfolge mit dem gleichen Wert wie webMessageAsString. Verwenden Sie diese anstelle von PostWebMessageAsJson, wenn Sie über einfache Zeichenfolgen anstelle von JSON-Objekten kommunizieren möchten.

#### Laden 

Laden Sie die aktuelle Seite neu.

> Public HRESULT [Reload](#reload)()

Dies ähnelt der Navigation zum URI des aktuellen Dokuments auf oberster Ebene, einschließlich aller Navigationsereignisse, die alle Einträge im HTTP-Cache auslösen und respektieren. Das zurück/weiter-Protokoll wird jedoch nicht geändert.

#### remove_ContainsFullScreenElementChanged 

Entfernen Sie einen Ereignishandler, der zuvor mit der entsprechenden add_-Ereignismethode hinzugefügt wurde.

> Public HRESULT [remove_ContainsFullScreenElementChanged](#remove_containsfullscreenelementchanged)(EventRegistrationToken-Token)

#### remove_ContentLoading 

Entfernen Sie einen Ereignishandler, der zuvor mit add_ContentLoading hinzugefügt wurde.

> Public HRESULT [remove_ContentLoading](#remove_contentloading)(EventRegistrationToken-Token)

#### remove_DocumentTitleChanged 

Entfernen Sie einen Ereignishandler, der zuvor mit add_DocumentTitleChanged hinzugefügt wurde.

> Public HRESULT [remove_DocumentTitleChanged](#remove_documenttitlechanged)(EventRegistrationToken-Token)

#### remove_FrameNavigationCompleted 

Entfernen Sie einen Ereignishandler, der zuvor mit add_FrameNavigationCompleted hinzugefügt wurde.

> Public HRESULT [remove_FrameNavigationCompleted](#remove_framenavigationcompleted)(EventRegistrationToken-Token)

#### remove_FrameNavigationStarting 

Entfernen Sie einen Ereignishandler, der zuvor mit add_FrameNavigationStarting hinzugefügt wurde.

> Public HRESULT [remove_FrameNavigationStarting](#remove_framenavigationstarting)(EventRegistrationToken-Token)

#### remove_HistoryChanged 

Entfernen Sie einen Ereignishandler, der zuvor mit add_HistoryChanged hinzugefügt wurde.

> Public HRESULT [remove_HistoryChanged](#remove_historychanged)(EventRegistrationToken-Token)

#### remove_NavigationCompleted 

Entfernen Sie einen Ereignishandler, der zuvor mit add_NavigationCompleted hinzugefügt wurde.

> Public HRESULT [remove_NavigationCompleted](#remove_navigationcompleted)(EventRegistrationToken-Token)

#### remove_NavigationStarting 

Entfernen Sie einen Ereignishandler, der zuvor mit add_NavigationStarting hinzugefügt wurde.

> Public HRESULT [remove_NavigationStarting](#remove_navigationstarting)(EventRegistrationToken-Token)

#### remove_NewWindowRequested 

Entfernen Sie einen Ereignishandler, der zuvor mit add_NewWindowRequested hinzugefügt wurde.

> Public HRESULT [remove_NewWindowRequested](#remove_newwindowrequested)(EventRegistrationToken-Token)

#### remove_PermissionRequested 

Entfernen Sie einen Ereignishandler, der zuvor mit add_PermissionRequested hinzugefügt wurde.

> Public HRESULT [remove_PermissionRequested](#remove_permissionrequested)(EventRegistrationToken-Token)

#### remove_ProcessFailed 

Entfernen Sie einen Ereignishandler, der zuvor mit add_ProcessFailed hinzugefügt wurde.

> Public HRESULT [remove_ProcessFailed](#remove_processfailed)(EventRegistrationToken-Token)

#### remove_ScriptDialogOpening 

Entfernen Sie einen Ereignishandler, der zuvor mit add_ScriptDialogOpening hinzugefügt wurde.

> Public HRESULT [remove_ScriptDialogOpening](#remove_scriptdialogopening)(EventRegistrationToken-Token)

#### remove_SourceChanged 

Entfernen Sie einen Ereignishandler, der zuvor mit add_SourceChanged hinzugefügt wurde.

> Public HRESULT [remove_SourceChanged](#remove_sourcechanged)(EventRegistrationToken-Token)

#### remove_WebMessageReceived 

Entfernen Sie einen Ereignishandler, der zuvor mit add_WebMessageReceived hinzugefügt wurde.

> Public HRESULT [remove_WebMessageReceived](#remove_webmessagereceived)(EventRegistrationToken-Token)

#### remove_WebResourceRequested 

Entfernen Sie einen Ereignishandler, der zuvor mit add_WebResourceRequested hinzugefügt wurde.

> Public HRESULT [remove_WebResourceRequested](#remove_webresourcerequested)(EventRegistrationToken-Token)

#### remove_WindowCloseRequested 

Entfernen Sie einen Ereignishandler, der zuvor mit add_WindowCloseRequested hinzugefügt wurde.

> Public HRESULT [remove_WindowCloseRequested](#remove_windowcloserequested)(EventRegistrationToken-Token)

#### RemoveHostObjectFromScript 

Entfernen Sie das vom Namen angegebene Hostobjekt, damit es nicht mehr über JavaScript-Code in der WebView zugänglich ist.

> Public HRESULT [RemoveHostObjectFromScript](#removehostobjectfromscript)(LPCWSTR Name)

Während neue Zugriffsversuche verweigert werden, wenn das Objekt bereits durch JavaScript-Code in der WebView abgerufen wird, hat der JavaScript-Code weiterhin Zugriff auf das Objekt. Das Aufrufen dieser Methode für einen Namen, der bereits entfernt oder nie hinzugefügt wird, schlägt fehl.

#### RemoveScriptToExecuteOnDocumentCreated 

Entfernen Sie das entsprechende JavaScript `AddScriptToExecuteOnDocumentCreated` , das mit der angegebenen Skript-ID hinzugefügt wurde.

> Public HRESULT [RemoveScriptToExecuteOnDocumentCreated](#removescripttoexecuteondocumentcreated)(LPCWSTR-ID)

#### RemoveWebResourceRequestedFilter 

Entfernt einen übereinstimmenden Webressourcen Filter, der zuvor für das WebResourceRequested-Ereignis hinzugefügt wurde.

> Public HRESULT [RemoveWebResourceRequestedFilter](#removewebresourcerequestedfilter)(LPCWSTR const URI, [COREWEBVIEW2_WEB_RESOURCE_CONTEXT](#corewebview2_web_resource_context) const resourcecontext)

Wenn derselbe Filter mehrmals hinzugefügt wurde, muss er so oft entfernt werden, wie er hinzugefügt wurde, damit er wirksam wird. Gibt E_INVALIDARG für einen Filter zurück, der nie hinzugefügt wurde.

#### Stop 

Beenden Sie alle Navigations-und ausstehenden Ressourcen Abrufe.

> öffentlicher HRESULT- [Stopp](#stop)()

Skripts werden nicht angehalten.

#### COREWEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT 

Bildformat, das von der ICoreWebView2:: CapturePreview-Methode verwendet wird.

> Enum- [COREWEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT](#corewebview2_capture_preview_image_format)

 Werte                         | Beschreibungen
--------------------------------|---------------------------------------------
COREWEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT_PNG            | PNG-Bildformat.
COREWEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT_JPEG            | JPEG-Bildformat.

#### COREWEBVIEW2_KEY_EVENT_KIND 

Der Typ des Schlüssel Ereignisses, das ein AcceleratorKeyPressed-Ereignis ausgelöst hat.

> Enum- [COREWEBVIEW2_KEY_EVENT_KIND](#corewebview2_key_event_kind)

 Werte                         | Beschreibungen
--------------------------------|---------------------------------------------
COREWEBVIEW2_KEY_EVENT_KIND_KEY_DOWN            | Dem Fenster Nachrichten WM_KEYDOWN entsprechen.
COREWEBVIEW2_KEY_EVENT_KIND_KEY_UP            | Dem Fenster Nachrichten WM_KEYUP entsprechen.
COREWEBVIEW2_KEY_EVENT_KIND_SYSTEM_KEY_DOWN            | Dem Fenster Nachrichten WM_SYSKEYDOWN entsprechen.
COREWEBVIEW2_KEY_EVENT_KIND_SYSTEM_KEY_UP            | Dem Fenster Nachrichten WM_SYSKEYUP entsprechen.

#### COREWEBVIEW2_MOVE_FOCUS_REASON 

Grund für das Verschieben des Fokus

> Enum- [COREWEBVIEW2_MOVE_FOCUS_REASON](#corewebview2_move_focus_reason)

 Werte                         | Beschreibungen
--------------------------------|---------------------------------------------
COREWEBVIEW2_MOVE_FOCUS_REASON_PROGRAMMATIC            | Der Fokus für die Code Einstellung in WebView.
COREWEBVIEW2_MOVE_FOCUS_REASON_NEXT            | Verschieben des Fokus aufgrund von Tabstopps vorwärts
COREWEBVIEW2_MOVE_FOCUS_REASON_PREVIOUS            | Verschieben des Fokus aufgrund von Tabstopps rückwärts

#### COREWEBVIEW2_PERMISSION_KIND 

Der Typ einer Berechtigungsanforderung.

> Enum- [COREWEBVIEW2_PERMISSION_KIND](#corewebview2_permission_kind)

 Werte                         | Beschreibungen
--------------------------------|---------------------------------------------
COREWEBVIEW2_PERMISSION_KIND_UNKNOWN_PERMISSION            | Unbekannte Berechtigung.
COREWEBVIEW2_PERMISSION_KIND_MICROPHONE            | Berechtigung zum Aufzeichnen von Audio.
COREWEBVIEW2_PERMISSION_KIND_CAMERA            | Berechtigung zum Aufzeichnen von Videos.
COREWEBVIEW2_PERMISSION_KIND_GEOLOCATION            | Berechtigung für den Zugriff auf Geolocation.
COREWEBVIEW2_PERMISSION_KIND_NOTIFICATIONS            | Berechtigung zum Senden von webbenachrichtigungen.
COREWEBVIEW2_PERMISSION_KIND_OTHER_SENSORS            | Berechtigung für den Zugriff auf den generischen Sensor.
COREWEBVIEW2_PERMISSION_KIND_CLIPBOARD_READ            | Berechtigung zum Lesen der Systemzwischenablage ohne Benutzergeste

#### COREWEBVIEW2_PERMISSION_STATE 

Antwort auf eine Berechtigungsanforderung.

> Enum- [COREWEBVIEW2_PERMISSION_STATE](#corewebview2_permission_state)

 Werte                         | Beschreibungen
--------------------------------|---------------------------------------------
COREWEBVIEW2_PERMISSION_STATE_DEFAULT            | Verwenden Sie das Standardbrowser Verhalten, das die Benutzer normalerweise zur Entscheidung auffordert.
COREWEBVIEW2_PERMISSION_STATE_ALLOW            | Erteilen Sie die Berechtigungsanforderung.
COREWEBVIEW2_PERMISSION_STATE_DENY            | Verweigern Sie die Berechtigungsanforderung.

#### COREWEBVIEW2_PHYSICAL_KEY_STATUS 

Eine Struktur, die die Informationen darstellt, die in lParam verpackt sind, die einem Win32-Schlüsselereignis zugewiesen wurden.

> typedef [COREWEBVIEW2_PHYSICAL_KEY_STATUS](#corewebview2_physical_key_status)

Weitere Informationen finden Sie in der Dokumentation zu WM_KEYDOWN.[https://docs.microsoft.com/windows/win32/inputdev/wm-keydown](https://docs.microsoft.com/windows/win32/inputdev/wm-keydown)

#### COREWEBVIEW2_PROCESS_FAILED_KIND 

Art des in der ICoreWebView2ProcessFailedEventHandler-Schnittstelle verwendeten Prozess Fehlers.

> Enum- [COREWEBVIEW2_PROCESS_FAILED_KIND](#corewebview2_process_failed_kind)

 Werte                         | Beschreibungen
--------------------------------|---------------------------------------------
COREWEBVIEW2_PROCESS_FAILED_KIND_BROWSER_PROCESS_EXITED            | Gibt an, dass der Browserprozess unerwartet beendet wurde.
COREWEBVIEW2_PROCESS_FAILED_KIND_RENDER_PROCESS_EXITED            | Gibt an, dass der Renderprozess unerwartet beendet wurde.
COREWEBVIEW2_PROCESS_FAILED_KIND_RENDER_PROCESS_UNRESPONSIVE            | Gibt an, dass der Renderprozess nicht mehr reagiert.

#### COREWEBVIEW2_SCRIPT_DIALOG_KIND 

Art des in der ICoreWebView2ScriptDialogOpeningEventHandler-Schnittstelle verwendeten JavaScript-Dialogfelds.

> Enum- [COREWEBVIEW2_SCRIPT_DIALOG_KIND](#corewebview2_script_dialog_kind)

 Werte                         | Beschreibungen
--------------------------------|---------------------------------------------
COREWEBVIEW2_SCRIPT_DIALOG_KIND_ALERT            | Ein Dialogfeld, das über die JavaScript-Funktion "Window. Alert" aufgerufen wird.
COREWEBVIEW2_SCRIPT_DIALOG_KIND_CONFIRM            | Ein Dialogfeld, das über die JavaScript-Funktion "Fenster. bestätigen" aufgerufen wird.
COREWEBVIEW2_SCRIPT_DIALOG_KIND_PROMPT            | Ein Dialogfeld, das über die JavaScript-Funktion "Window. prompt" aufgerufen wird.
COREWEBVIEW2_SCRIPT_DIALOG_KIND_BEFOREUNLOAD            | Ein Dialogfeld, das über das beforeunload-JavaScript-Ereignis aufgerufen wird.

#### COREWEBVIEW2_WEB_ERROR_STATUS 

Fehlerstatus Werte für Web-Navigationselemente.

> Enum- [COREWEBVIEW2_WEB_ERROR_STATUS](#corewebview2_web_error_status)

 Werte                         | Beschreibungen
--------------------------------|---------------------------------------------
COREWEBVIEW2_WEB_ERROR_STATUS_UNKNOWN            | Ein unbekannter Fehler ist aufgetreten.
COREWEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_COMMON_NAME_IS_INCORRECT            | Der allgemeine Name des SSL-Zertifikats entspricht nicht der Webadresse.
COREWEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_EXPIRED            | Das SSL-Zertifikat ist abgelaufen.
COREWEBVIEW2_WEB_ERROR_STATUS_CLIENT_CERTIFICATE_CONTAINS_ERRORS            | Das SSL-Clientzertifikat enthält Fehler.
COREWEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_REVOKED            | Das SSL-Zertifikat wurde gesperrt.
COREWEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_IS_INVALID            | Das SSL-Zertifikat ist ungültig &ndash; Dies könnte bedeuten, dass das Zertifikat nicht mit den öffentlichen Schlüssel Pins für den Hostnamen übereinstimmte. das Zertifikat wird von einer nicht vertrauenswürdigen Zertifizierungsstelle signiert oder mit einem schwachen Vorzeichen Algorithmus, das Zertifikat behauptet, dass DNS-Namen gegen Namenseinschränkungen verstoßen, das Zertifikat einen schwachen Schlüssel enthält, der Gültigkeitszeitraum des Zertifikats zu lang ist, fehlender Sperrungsinformationen oder Sperrungs Mechanismus, nicht eindeutiger [legacy Symantec root](https://security.googleblog.com/2018/03/distrust-of-symantec-pki-immediate.html)Hostname, fehlender Zertifikat Transparenzinformationen oder das Zertifikat an
COREWEBVIEW2_WEB_ERROR_STATUS_SERVER_UNREACHABLE            | Der Host ist nicht erreichbar.
COREWEBVIEW2_WEB_ERROR_STATUS_TIMEOUT            | Die Verbindung hat ein Zeitlimit überschritten.
COREWEBVIEW2_WEB_ERROR_STATUS_ERROR_HTTP_INVALID_SERVER_RESPONSE            | Der Server hat eine ungültige oder unbekannte Antwort zurückgegeben.
COREWEBVIEW2_WEB_ERROR_STATUS_CONNECTION_ABORTED            | Die Verbindung wurde abgebrochen.
COREWEBVIEW2_WEB_ERROR_STATUS_CONNECTION_RESET            | Die Verbindung wurde zurückgesetzt.
COREWEBVIEW2_WEB_ERROR_STATUS_DISCONNECTED            | Die Internet Verbindung wurde unterbrochen.
COREWEBVIEW2_WEB_ERROR_STATUS_CANNOT_CONNECT            | Verbindung mit Ziel kann nicht hergestellt werden.
COREWEBVIEW2_WEB_ERROR_STATUS_HOST_NAME_NOT_RESOLVED            | Der angegebene Hostname konnte nicht aufgelöst werden.
COREWEBVIEW2_WEB_ERROR_STATUS_OPERATION_CANCELED            | Der Vorgang wurde abgebrochen.
COREWEBVIEW2_WEB_ERROR_STATUS_REDIRECT_FAILED            | Die Anforderungs Umleitung ist fehlgeschlagen.
COREWEBVIEW2_WEB_ERROR_STATUS_UNEXPECTED_ERROR            | Ein unerwarteter Fehler ist aufgetreten.

#### COREWEBVIEW2_WEB_RESOURCE_CONTEXT 

Enum für Webressourcen-anforderungskontexte.

> Enum- [COREWEBVIEW2_WEB_RESOURCE_CONTEXT](#corewebview2_web_resource_context)

 Werte                         | Beschreibungen
--------------------------------|---------------------------------------------
COREWEBVIEW2_WEB_RESOURCE_CONTEXT_ALL            | Alle Ressourcen.
COREWEBVIEW2_WEB_RESOURCE_CONTEXT_DOCUMENT            | Dokument Ressourcen.
COREWEBVIEW2_WEB_RESOURCE_CONTEXT_STYLESHEET            | CSS-Ressourcen.
COREWEBVIEW2_WEB_RESOURCE_CONTEXT_IMAGE            | Bildressourcen.
COREWEBVIEW2_WEB_RESOURCE_CONTEXT_MEDIA            | Andere Medienressourcen wie Videos.
COREWEBVIEW2_WEB_RESOURCE_CONTEXT_FONT            | Schriftartressourcen.
COREWEBVIEW2_WEB_RESOURCE_CONTEXT_SCRIPT            | Skriptressourcen.
COREWEBVIEW2_WEB_RESOURCE_CONTEXT_XML_HTTP_REQUEST            | XML-HTTP-Anforderungen.
COREWEBVIEW2_WEB_RESOURCE_CONTEXT_FETCH            | Abrufen der API-Kommunikation.
COREWEBVIEW2_WEB_RESOURCE_CONTEXT_TEXT_TRACK            | Texttracking-Ressourcen.
COREWEBVIEW2_WEB_RESOURCE_CONTEXT_EVENT_SOURCE            | EventSource-API-Kommunikation.
COREWEBVIEW2_WEB_RESOURCE_CONTEXT_WEBSOCKET            | WebSocket-API-Kommunikation.
COREWEBVIEW2_WEB_RESOURCE_CONTEXT_MANIFEST            | Web App-Manifeste
COREWEBVIEW2_WEB_RESOURCE_CONTEXT_SIGNED_EXCHANGE            | Signierte http-Exchanges.
COREWEBVIEW2_WEB_RESOURCE_CONTEXT_PING            | Ping-Anforderungen.
COREWEBVIEW2_WEB_RESOURCE_CONTEXT_CSP_VIOLATION_REPORT            | Berichte zu CSP-Verstößen
COREWEBVIEW2_WEB_RESOURCE_CONTEXT_OTHER            | Andere Ressourcen.

