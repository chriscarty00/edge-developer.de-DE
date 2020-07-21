---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.8.355-WebView2 Win32 C++ IWebView2WebView
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge
ms.openlocfilehash: 5711a1dbf501df55fefc9709763c1fe225865e11
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/20/2020
ms.locfileid: "10886430"
---
# 0.8.355-Interface-IWebView2WebView 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2WebView
  : public IUnknown
```

WebView2 ermöglicht Ihnen das Hosten von Webinhalten mithilfe der neuesten Edge-Webbrowser Technologie.

## Zusammenfassung

 Member                        | Beschreibungen
--------------------------------|---------------------------------------------
[get_Settings](#get_settings) | Das [IWebView2Settings](IWebView2Settings.md) -Objekt enthält verschiedene änderbare Einstellungen für den ausgeführten WebView.
[get_Source](#get_source) | Der URI des aktuellen Dokuments auf oberster Ebene.
[%%amp;quot;Navigate%%amp;quot;
](#navigate) | Führen Sie eine Navigation des Dokuments auf oberster Ebene zum angegebenen URI.
[MoveFocus](#movefocus) | Verschieben des Fokus in WebView
[NavigateToString](#navigatetostring) | Initiiert eine Navigation zu htmlContent als HTML-Code für ein neues Dokument.
[add_NavigationStarting](#add_navigationstarting) | Fügen Sie einen Ereignishandler für das NavigationStarting-Ereignis hinzu.
[remove_NavigationStarting](#remove_navigationstarting) | Entfernen Sie einen Ereignishandler, der zuvor mit add_NavigationStarting hinzugefügt wurde.
[add_DocumentStateChanged](#add_documentstatechanged) | Fügen Sie einen Ereignishandler für das DocumentStateChanged-Ereignis hinzu.
[remove_DocumentStateChanged](#remove_documentstatechanged) | Entfernen Sie einen Ereignishandler, der zuvor mit add_DocumentStateChanged hinzugefügt wurde.
[add_NavigationCompleted](#add_navigationcompleted) | Fügen Sie einen Ereignishandler für das NavigationCompleted-Ereignis hinzu.
[remove_NavigationCompleted](#remove_navigationcompleted) | Entfernen Sie einen Ereignishandler, der zuvor mit add_NavigationCompleted hinzugefügt wurde.
[add_FrameNavigationStarting](#add_framenavigationstarting) | Fügen Sie einen Ereignishandler für das FrameNavigationStarting-Ereignis hinzu.
[remove_FrameNavigationStarting](#remove_framenavigationstarting) | Entfernen Sie einen Ereignishandler, der zuvor mit add_FrameNavigationStarting hinzugefügt wurde.
[add_MoveFocusRequested](#add_movefocusrequested) | Fügen Sie einen Ereignishandler für das MoveFocusRequested-Ereignis hinzu.
[remove_MoveFocusRequested](#remove_movefocusrequested) | Entfernen Sie einen Ereignishandler, der zuvor mit add_MoveFocusRequested hinzugefügt wurde.
[add_GotFocus](#add_gotfocus) | Fügen Sie einen Ereignishandler für das GotFocus-Ereignis hinzu.
[remove_GotFocus](#remove_gotfocus) | Entfernen Sie einen Ereignishandler, der zuvor mit add_GotFocus hinzugefügt wurde.
[add_LostFocus](#add_lostfocus) | Fügen Sie einen Ereignishandler für das LostFocus-Ereignis hinzu.
[remove_LostFocus](#remove_lostfocus) | Entfernen Sie einen Ereignishandler, der zuvor mit add_LostFocus hinzugefügt wurde.
[add_WebResourceRequested_deprecated](#add_webresourcerequested_deprecated) | Diese API wird als veraltet markiert, bitte verwenden Sie die neue add_WebResourceRequested-API.
[remove_WebResourceRequested](#remove_webresourcerequested) | Entfernen Sie einen Ereignishandler, der zuvor mit add_WebResourceRequested hinzugefügt wurde.
[add_ScriptDialogOpening](#add_scriptdialogopening) | Fügen Sie einen Ereignishandler für das ScriptDialogOpening-Ereignis hinzu.
[remove_ScriptDialogOpening](#remove_scriptdialogopening) | Entfernen Sie einen Ereignishandler, der zuvor mit add_ScriptDialogOpening hinzugefügt wurde.
[add_ZoomFactorChanged](#add_zoomfactorchanged) | Fügen Sie einen Ereignishandler für das ZoomFactorChanged-Ereignis hinzu.
[remove_ZoomFactorChanged](#remove_zoomfactorchanged) | Entfernen Sie einen Ereignishandler, der zuvor mit add_ZoomFactorChanged hinzugefügt wurde.
[add_PermissionRequested](#add_permissionrequested) | Fügen Sie einen Ereignishandler für das PermissionRequested-Ereignis hinzu.
[remove_PermissionRequested](#remove_permissionrequested) | Entfernen Sie einen Ereignishandler, der zuvor mit add_PermissionRequested hinzugefügt wurde.
[add_ProcessFailed](#add_processfailed) | Fügen Sie einen Ereignishandler für das ProcessFailed-Ereignis hinzu.
[remove_ProcessFailed](#remove_processfailed) | Entfernen Sie einen Ereignishandler, der zuvor mit add_ProcessFailed hinzugefügt wurde.
[AddScriptToExecuteOnDocumentCreated](#addscripttoexecuteondocumentcreated) | Fügen Sie das bereitgestellte JavaScript einer Liste von Skripts hinzu, die ausgeführt werden sollen, nachdem das globale Objekt erstellt wurde, aber bevor das HTML-Dokument analysiert wurde und bevor ein anderes Skript ausgeführt wird, das vom HTML-Dokument eingeschlossen ist.
[RemoveScriptToExecuteOnDocumentCreated](#removescripttoexecuteondocumentcreated) | Entfernen Sie das entsprechende JavaScript, das über AddScriptToExecuteOnDocumentCreated hinzugefügt wurde.
[ExecuteScript](#executescript) | Führen Sie JavaScript-Code aus dem JavaScript-Parameter im aktuellen Dokument der obersten Ebene aus, das in der WebView gerendert wird.
[CapturePreview](#capturepreview) | Erfassen Sie ein Bild von der Anzeige von WebView.
[Laden](#reload) | Laden Sie die aktuelle Seite neu.
[get_Bounds](#get_bounds) | Die WebView-Begrenzungen.
[put_Bounds](#put_bounds) | Die Bounds-Eigenschaft festlegen.
[get_ZoomFactor](#get_zoomfactor) | Der Zoomfaktor für die aktuelle Seite im WebView.
[put_ZoomFactor](#put_zoomfactor) | Festlegen der ZoomFactor-Eigenschaft
[get_IsVisible](#get_isvisible) | Die IsVisible-Eigenschaft bestimmt, ob die WebView angezeigt oder ausgeblendet werden soll.
[put_IsVisible](#put_isvisible) | Festlegen der IsVisible-Eigenschaft
[PostWebMessageAsJson](#postwebmessageasjson) | Posten Sie die angegebene Webnachricht im Dokument der obersten Ebene in diesem [IWebView2WebView]().
[PostWebMessageAsString](#postwebmessageasstring) | Dies ist ein Helfer zum Posten einer Nachricht, bei der es sich um eine einfache Zeichenfolge und nicht um eine JSON-Zeichenfolgendarstellung eines JavaScript-Objekts handelt.
[add_WebMessageReceived](#add_webmessagereceived) | Dieses Ereignis wird ausgelöst, wenn die IsWebMessageEnabled-Einstellung festgelegt ist, und das Dokument auf oberster Ebene des WebView-Anrufs `window.chrome.webview.postMessage` .
[remove_WebMessageReceived](#remove_webmessagereceived) | Entfernen Sie einen Ereignishandler, der zuvor mit add_WebMessageReceived hinzugefügt wurde.
[Schließen](#close) | Schließt die WebView und bereinigt die zugrunde liegende Browserinstanz.
[CallDevToolsProtocolMethod](#calldevtoolsprotocolmethod) | Rufen Sie eine asynchrone DevToolsProtocol-Methode auf.
[add_DevToolsProtocolEventReceived](#add_devtoolsprotocoleventreceived) | Abonnieren eines DevToolsProtocol-Ereignisses
[remove_DevToolsProtocolEventReceived](#remove_devtoolsprotocoleventreceived) | Entfernen Sie einen Ereignishandler, der zuvor mit add_DevToolsProtocolEventReceived hinzugefügt wurde.
[get_BrowserProcessId](#get_browserprocessid) | Die Prozess-ID des Browser Prozesses, der die WebView hostet.
[get_CanGoBack](#get_cangoback) | Kann im WebView zur vorherigen Seite im Navigationsverlauf navigieren.
[get_CanGoForward](#get_cangoforward) | Kann im WebView zur nächsten Seite im Navigationsverlauf navigieren.
[GoBack](#goback) | Navigiert die WebView zur vorherigen Seite im Navigationsverlauf.
[GoForward](#goforward) | Navigiert die WebView zur nächsten Seite im Navigationsverlauf.
[WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT](#webview2_capture_preview_image_format) | Bildformat, das von der [IWebView2WebView:: CapturePreview](#capturepreview) -Methode verwendet wird.
[WEBVIEW2_SCRIPT_DIALOG_KIND](#webview2_script_dialog_kind) | Art des in der [IWebView2ScriptDialogOpeningEventHandler](IWebView2ScriptDialogOpeningEventHandler.md) -Schnittstelle verwendeten JavaScript-Dialogfelds.
[WEBVIEW2_PROCESS_FAILED_KIND](#webview2_process_failed_kind) | Art des in der [IWebView2ProcessFailedEventHandler](IWebView2ProcessFailedEventHandler.md) -Schnittstelle verwendeten Prozess Fehlers.
[WEBVIEW2_PERMISSION_TYPE](#webview2_permission_type) | Der Typ einer Berechtigungsanforderung.
[WEBVIEW2_PERMISSION_STATE](#webview2_permission_state) | Antwort auf eine Berechtigungsanforderung.
[WEBVIEW2_MOVE_FOCUS_REASON](#webview2_move_focus_reason) | Grund für das Verschieben des Fokus
[WEBVIEW2_WEB_ERROR_STATUS](#webview2_web_error_status) | Fehlerstatus Werte für Web-Navigationselemente.
[WEBVIEW2_WEB_RESOURCE_CONTEXT](#webview2_web_resource_context) | Enum für Webressourcen-anforderungskontexte.

## Navigationsereignisse

Die normale Abfolge von Navigations Ereignissen lautet NavigationStarting, DocumentStateChanged und dann NavigationCompleted.

![dot-inline-dotgraph-1.png](media/dot-inline-dotgraph-1.png)

Beachten Sie, dass dies für Navigationsereignisse mit dem gleichen Navigations-Event-arg gilt. Navigationsereignisse mit unterschiedlichen Navigations-Event-args können sich überlappen. Wenn Sie beispielsweise eine Navigation auf das NavigationStarting-Ereignis warten und dann eine andere Navigation starten, sehen Sie die NavigationStarting für die erste Navigation, gefolgt von der NavigationStarting der zweiten Navigation, gefolgt von der NavigationCompleted für die erste Navigation und dann allen anderen geeigneten Navigations Ereignissen für die zweite Navigation. In Fehlerfällen kann es sich um ein DocumentStateChanged-Ereignis handeln, das davon abhängt, ob die Navigation auf einer Fehlerseite fortgesetzt wird. Im Fall einer HTTP-Umleitung gibt es mehrere NavigationStarting-Ereignisse in einer Zeile, wobei für diejenigen, die dem ersten Folgen, das isredirect-Flag festzulegen ist.

Bei untergeordneten Frames in WebView ist das einzige ausgelöste Navigations Ereignis das NavigationStarting-Ereignis, das Host die Möglichkeit gibt, unter Frame-Navigationselemente zu blockieren.

## Prozessmodell

WebView2 verwendet das gleiche Prozessmodell wie der Edge-Webbrowser. Es gibt einen Edge-Browserprozess pro angegebenen Benutzerdatenverzeichnis in einer Benutzersitzung, die jedem WebView2-Aufrufprozess dient, der das Benutzerdatenverzeichnis angibt. Dies bedeutet, dass ein Edge-Browser-Prozess möglicherweise mehrere Anruf Prozesse bedient, und ein Aufrufprozess möglicherweise mehrere Edge-Browser-Prozesse verwendet.

![dot-inline-dotgraph-2.png](media/dot-inline-dotgraph-2.png)

In einem Browserprozess gibt es eine Reihe von Renderer-Prozessen. Diese werden nach Bedarf erstellt, um potenziell mehrere Frames in verschiedenen Webansichten zu bedienen. Die Anzahl der Renderer-Prozesse variiert basierend auf dem Feature "Website Isolierungs Browser" und der Anzahl der unterschiedlichen getrennten Ursprünge, die in verknüpften Webansichten gerendert werden.

![dot-inline-dotgraph-3.png](media/dot-inline-dotgraph-3.png)

Mithilfe des ProcessFailure-Ereignisses können Sie auf Abstürze reagieren und in diesen Browser-und Renderer-Prozessen hängen bleiben.

Sie können zugeordnete Browser-und Renderer-Prozesse mit der Close-Methode sicher Herunterfahren.

## Threadingmodell

Der WebView2 muss in einem UI-Thread erstellt werden. Insbesondere ein Thread mit einer Nachrichten Pumpe. Alle Rückrufe werden in diesem Thread ausgeführt, und Aufrufe an die WebView müssen in diesem Thread ausgeführt werden. Es ist nicht sicher, die WebView aus einem anderen Thread zu verwenden.

Rückrufe, einschließlich Ereignishandlern und Vervollständigungs Handlern, werden seriell ausgeführt. Das heißt, wenn Sie einen Ereignishandler ausführen und eine Nachrichtenschleife beginnen, werden keine anderen Ereignishandler oder Abschluss Rückrufe erneut ausgeführt.

## Sicherheit

Überprüfen Sie immer die Source-Eigenschaft von WebView, bevor Sie executeScript, PostWebMessageAsJson, PostWebMessageAsString oder eine andere Methode verwenden, um Informationen an die WebView zu senden. Die WebView kann über den Endbenutzer, der mit der Seite oder dem Skript auf der Seite interagiert, die Navigation verursacht hat, zu einer anderen Seite navigieren. Achten Sie auf ähnliche Weise auf AddScriptToExecuteOnDocumentCreated. Alle zukünftigen Navigationselemente führen dieses Skript aus, und wenn es Zugriff auf Informationen bietet, die nur für einen bestimmten Ursprung vorgesehen sind, kann jedes HTML-Dokumentzugriff haben.

Bei der Untersuchung des Ergebnisses eines executeScript-Methodenaufrufs, eines WebMessageReceived-Ereignisses, immer überprüfen der Quelle des Absenders oder eines anderen Mechanismus zum Empfangen von Informationen aus einem HTML-Dokument in einer WebView überprüfen Sie, ob der URI des HTML-Dokuments Ihren Erwartungen entspricht.

Wenn Sie eine Nachricht erstellen, die Sie in eine WebView senden möchten, verwenden Sie PostWebMessageAsJson, und erstellen Sie den JSON-Zeichenfolgenparameter mithilfe einer JSON-Bibliothek. Dadurch werden potenzielle Unfälle von Codierungsinformationen in eine JSON-Zeichenfolge oder ein Skript vermieden, und sichergestellt, dass keine von Angreifern gesteuerte Eingabe den restlichen Teil der JSON-Nachricht ändern oder ein beliebiges Skript ausführen kann.

## Zeichenfolgentypen

Zeichenfolgenparameter sind LPWSTR NULL-terminierte Zeichenfolgen. Der aufgerufene ordnet die Zeichenfolge mithilfe von CoTaskMemAlloc zu. Der Besitz wird an den Anrufer übertragen, und es ist dem Anrufer überlassen, den Speicher mit CoTaskMemFree zu befreien.

Zeichenfolge in Parametern sind LPCWSTR NULL-terminierte Zeichenfolgen. Der Aufrufer stellt sicher, dass die Zeichenfolge für die Dauer des synchronen Funktionsaufrufs gültig ist. Wenn der aufgerufene diesen Wert nach Abschluss des Funktionsaufrufs bis zu einem gewissen Punkt beibehalten muss, muss der aufgerufene eine eigene Kopie des Zeichenfolgenwerts zuweisen.

## URI-und JSON-Analyse

Verschiedene Methoden stellen URIs und JSON als Zeichenfolgen bereit oder akzeptieren Sie. Verwenden Sie für die Analyse und Generierung dieser Zeichenfolgen ihre eigene bevorzugte Bibliothek.

Wenn WinRT für Ihre app verfügbar ist, können Sie `RuntimeClass_Windows_Data_Json_JsonObject` JSON-Zeichenfolgen verwenden und erstellen oder URIs analysieren und `IJsonObjectStatics` `RuntimeClass_Windows_Foundation_Uri` `IUriRuntimeClassFactory` erstellen. Beide arbeiten in Win32-apps.

Wenn Sie IUri und CreateUri zum Analysieren von URIs verwenden, sollten Sie möglicherweise die folgenden URI-Erstellungs Flags verwenden, damit CreateUri-Verhalten der URI-Analyse in der WebView genauer entspricht: `Uri_CREATE_ALLOW_IMPLICIT_FILE_SCHEME | Uri_CREATE_NO_DECODE_EXTRA_INFO`

## Debuggen

Öffnen Sie devtools mit den normalen Tastenkombinationen: `F12` oder `Ctrl+Shift+I` . Sie können die `--auto-open-devtools-for-tabs` Befehlsargument Schalter verwenden, um das devtools-Fenster sofort zu öffnen, wenn Sie das erste Mal eine WebView erstellen. Informationen zum Bereitstellen zusätzlicher Befehlszeilenargumente für den Browserprozess finden Sie unter Dokumentation zu WebView. Schauen Sie sich den LoaderOverride-Registrierungsschlüssel an, um verschiedene Builds von WebView2 zu testen, ohne die Anwendung in der WebView-Dokumentation zu ändern.

## Versionsverwaltung

Nachdem Sie eine bestimmte Version des SDK zum Erstellen Ihrer APP verwendet haben, wird Ihre APP möglicherweise mit einer älteren oder neueren Version der installierten Browser-Binärdateien ausgeführt. Bis Version 1.0.0.0 von WebView2 können sich während der Updates Änderungen ändern, die verhindern, dass Ihr SDK mit unterschiedlichen Versionen der installierten Browser-Binärdateien funktioniert. Nach der Version 1.0.0.0 können verschiedene Versionen des SDKs mit unterschiedlichen Versionen des installierten Browsers funktionieren, indem Sie die folgenden bewährten Methoden verwenden:

Wenn Sie Änderungen an der API berücksichtigen möchten, müssen Sie sicherstellen, dass Sie beim Aufrufen der DLL-Export CreateWebView2Environment und beim Aufrufen von QueryInterface für ein beliebiges WebView2-Objekt auf Fehler überprüfen. Ein Rückgabewert von E_NOINTERFACE kann darauf hindeuten, dass das SDK nicht mit den Binärdateien des Edge-Browsers kompatibel ist.

Das Überprüfen auf Fehler von QueryInterface berücksichtigt auch Fälle, in denen das SDK neuer als die Version des Edge-Browsers ist und Ihre APP versucht, eine Schnittstelle zu verwenden, von der der Edge-Browser nichts weiß.

Wenn eine Schnittstelle nicht zur Verfügung steht, können Sie das zugeordnete Feature nach Möglichkeit deaktivieren oder den Endbenutzer anderweitig darüber informieren, dass Sie den Browser aktualisieren müssen.

## Member

#### get_Settings 

Das [IWebView2Settings](IWebView2Settings.md) -Objekt enthält verschiedene änderbare Einstellungen für den ausgeführten WebView.

> öffentliche HRESULT- [get_Settings](#get_settings)([IWebView2Settings](IWebView2Settings.md) * *-Einstellungen)

#### get_Source 

Der URI des aktuellen Dokuments auf oberster Ebene.

> Public HRESULT [get_Source](#get_source)(LPWSTR * URI)

Dieser Wert ändert sich möglicherweise als Teil des DocumentStateChanged-Ereignis Auslösens für einige Fälle wie das Navigieren zu einem anderen Website-oder Fragment-Navigationsbereich. Sie bleibt bei anderen Navigations Typen wie "Seiten-Reload" oder "History. pushState" unverändert, wobei dieselbe URL wie die aktuelle Seite angezeigt wird.

```cpp
    // Register a handler for the DocumentStateChanged event.
    // This handler will read the webview's source URI and update
    // the app's address bar.
    CHECK_FAILURE(m_webView->add_DocumentStateChanged(
        Callback<IWebView2DocumentStateChangedEventHandler>(
            [this](IWebView2WebView* sender, IWebView2DocumentStateChangedEventArgs* args)
                -> HRESULT {
                wil::unique_cotaskmem_string uri;
                sender->get_Source(&uri);
                if (wcscmp(uri.get(), L"about:blank") == 0)
                {
                    uri = wil::make_cotaskmem_string(L"");
                }
                SetWindowText(m_toolbar->addressBarWindow, uri.get());

                return S_OK;
            })
            .Get(),
        &m_documentStateChangedToken));
```

#### %%amp;quot;Navigate%%amp;quot;
 

Führen Sie eine Navigation des Dokuments auf oberster Ebene zum angegebenen URI.

> öffentliche HRESULT- [Navigation](#navigate)(LPCWSTR-URI)

Weitere Informationen finden Sie in den Navigations Ereignissen. Beachten Sie, dass dadurch eine Navigation gestartet wird und das entsprechende NavigationStarting-Ereignis irgendwann ausgelöst wird, nachdem dieser Navigate-Aufruf abgeschlossen ist.

```cpp
void ControlComponent::NavigateToAddressBar()
{
    WCHAR uri[2048] = L"";
    GetWindowText(m_toolbar->addressBarWindow, uri, ARRAYSIZE(uri));
    CHECK_FAILURE(m_webView->Navigate(uri));
}
```

#### MoveFocus 

Verschieben des Fokus in WebView

> öffentliche HRESULT- [MoveFocus](#movefocus)([WEBVIEW2_MOVE_FOCUS_REASON](#webview2_move_focus_reason) Grund)

WebView erhält den Fokus, und der Fokus wird auf das korrespondierende Element auf der Seite gesetzt, die in der WebView gehostet wird. Aus Programm Gründen wird der Fokus auf das zuvor fokussierte Element oder auf das Standardelement gesetzt, wenn kein zuvor fokussiertes Element vorhanden ist. Aus dem nächsten Grund wird der Fokus auf das erste Element gesetzt. Aus vorherigen Gründen wird der Fokus auf das letzte Element gesetzt. WebView kann auch den Fokus über die Benutzerinteraktion erhalten, wie das Klicken in WebView oder die Tab-Taste. Für die Tab-Taste kann die APP MoveFocus mit der nächsten oder vorherigen aufrufen, um mit Tab und UMSCHALT + TAB auszurichten, wenn Sie beschließt, dass die WebView das nächste Tabbed-Element ist. Oder die APP kann IsDialogMessage als Teil der Nachrichtenschleife aufrufen, damit die Plattform die Tab-Funktion automatisch verarbeiten kann. Die Plattform wird durch alle Fenster mit WS_TABSTOP gedreht. Wenn die WebView den Fokus von IsDialogMessage erhält, wird der Fokus intern auf das erste oder letzte Element für Tab und UMSCHALT + TAB gesetzt.

```cpp
    while (GetMessage(&msg, nullptr, 0, 0))
    {
        if (!TranslateAccelerator(msg.hwnd, hAccelTable, &msg))
        {
            // Calling IsDialogMessage handles Tab traversal automatically. If the
            // app wants the platform to auto handle tab, then call IsDialogMessage
            // before calling TranslateMessage/DispatchMessage. If the app wants to
            // handle tabbing itself, then skip calling IsDialogMessage and call
            // TranslateMessage/DispatchMessage directly.
            if (!g_autoTabHandle || !IsDialogMessage(GetAncestor(msg.hwnd, GA_ROOT), &msg))
            {
                TranslateMessage(&msg);
                DispatchMessage(&msg);
            }
        }
    }
```

```cpp
        if (wParam == VK_TAB)
        {
            // Find out if the window is one we've customized for tab handling
            for (int i = 0; i < m_tabbableWindows.size(); i++)
            {
                if (m_tabbableWindows[i].first == hWnd)
                {
                    if (GetKeyState(VK_SHIFT) < 0)
                    {
                        TabBackwards(i);
                    }
                    else
                    {
                        TabForwards(i);
                    }
                    return true;
                }
            }
        }
```

```cpp
void ControlComponent::TabForwards(int currentIndex)
{
    // Find first enabled window after the active one
    for (int i = currentIndex + 1; i < m_tabbableWindows.size(); i++)
    {
        HWND hwnd = m_tabbableWindows.at(i).first;
        if (IsWindowEnabled(hwnd))
        {
            SetFocus(hwnd);
            return;
        }
    }
    // If this is the last enabled window, tab forwards into the WebView.
    m_webView->MoveFocus(WEBVIEW2_MOVE_FOCUS_REASON_NEXT);
}

void ControlComponent::TabBackwards(int currentIndex)
{
    // Find first enabled window before the active one
    for (int i = currentIndex - 1; i >= 0; i--)
    {
        HWND hwnd = m_tabbableWindows.at(i).first;
        if (IsWindowEnabled(hwnd))
        {
            SetFocus(hwnd);
            return;
        }
    }
    // If this is the last enabled window, tab forwards into the WebView.
    CHECK_FAILURE(m_webView->MoveFocus(WEBVIEW2_MOVE_FOCUS_REASON_PREVIOUS));
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

#### add_NavigationStarting 

Fügen Sie einen Ereignishandler für das NavigationStarting-Ereignis hinzu.

> Public HRESULT [add_NavigationStarting](#add_navigationstarting)([IWebView2NavigationStartingEventHandler](IWebView2NavigationStartingEventHandler.md) * EventHandler, EventRegistrationToken * Token)

NavigationStarting wird ausgelöst, wenn der WebView-Hauptframe die Berechtigung zum Navigieren zu einem anderen URI anfordert. Dies wird auch für Umleitungen ausgelöst.

```cpp
    // Register a handler for the NavigationStarting event.
    // This handler will check the domain being navigated to, and if the domain
    // matches a list of blocked sites, it will cancel the navigation and
    // possibly display a warning page.  It will also disable JavaScript on
    // selected websites.
    CHECK_FAILURE(m_webView->add_NavigationStarting(
        Callback<IWebView2NavigationStartingEventHandler>(
            [this](IWebView2WebView* sender,
                   IWebView2NavigationStartingEventArgs* args) -> HRESULT
    {
        wil::unique_cotaskmem_string uri;
        CHECK_FAILURE(args->get_Uri(&uri));

        if (ShouldBlockUri(uri.get()))
        {
            CHECK_FAILURE(args->put_Cancel(true));

            // If the user clicked a link to navigate, show a warning page.
            BOOL userInitiated;
            CHECK_FAILURE(args->get_IsUserInitiated(&userInitiated));
            if (userInitiated)
            {
                static const PCWSTR htmlContent =
                    L"<h1>Domain Blocked</h1>"
                    L"<p>You've attempted to navigate to a domain in the blocked "
                    L"sites list. Press back to return to the previous page.</p>";
                CHECK_FAILURE(sender->NavigateToString(htmlContent));
            }
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

#### remove_NavigationStarting 

Entfernen Sie einen Ereignishandler, der zuvor mit add_NavigationStarting hinzugefügt wurde.

> Public HRESULT [remove_NavigationStarting](#remove_navigationstarting)(EventRegistrationToken-Token)

#### add_DocumentStateChanged 

Fügen Sie einen Ereignishandler für das DocumentStateChanged-Ereignis hinzu.

> Public HRESULT [add_DocumentStateChanged](#add_documentstatechanged)([IWebView2DocumentStateChangedEventHandler](IWebView2DocumentStateChangedEventHandler.md) * EventHandler, EventRegistrationToken * Token)

DocumentStateChanged wird ausgelöst, wenn neuer Inhalt im Hauptframe der WebView geladen wird oder wenn dieselbe Seitennavigation ausgeführt wird (beispielsweisedurch Fragment-Navigation oder History. pushState-Navigation). Dies folgt dem NavigationStarting-Ereignis und geht dem NavigationCompleted-Ereignis voraus.

```cpp
    // Register a handler for the DocumentStateChanged event.
    // This handler will read the webview's source URI and update
    // the app's address bar.
    CHECK_FAILURE(m_webView->add_DocumentStateChanged(
        Callback<IWebView2DocumentStateChangedEventHandler>(
            [this](IWebView2WebView* sender, IWebView2DocumentStateChangedEventArgs* args)
                -> HRESULT {
                wil::unique_cotaskmem_string uri;
                sender->get_Source(&uri);
                if (wcscmp(uri.get(), L"about:blank") == 0)
                {
                    uri = wil::make_cotaskmem_string(L"");
                }
                SetWindowText(m_toolbar->addressBarWindow, uri.get());

                return S_OK;
            })
            .Get(),
        &m_documentStateChangedToken));
```

#### remove_DocumentStateChanged 

Entfernen Sie einen Ereignishandler, der zuvor mit add_DocumentStateChanged hinzugefügt wurde.

> Public HRESULT [remove_DocumentStateChanged](#remove_documentstatechanged)(EventRegistrationToken-Token)

#### add_NavigationCompleted 

Fügen Sie einen Ereignishandler für das NavigationCompleted-Ereignis hinzu.

> Public HRESULT [add_NavigationCompleted](#add_navigationcompleted)([IWebView2NavigationCompletedEventHandler](IWebView2NavigationCompletedEventHandler.md) * EventHandler, EventRegistrationToken * Token)

Das NavigationCompleted-Ereignis wird ausgelöst, wenn die WebView vollständig geladen wurde (Body. OnLoad wurde ausgelöst) oder das Laden mit einem Fehler beendet wurde.

```cpp
    // Register a handler for the NavigationCompleted event.
    // Check whether the navigation succeeded, and if not, do something.
    // Also update the Back, Forward, and Cancel buttons.
    CHECK_FAILURE(m_webView->add_NavigationCompleted(
        Callback<IWebView2NavigationCompletedEventHandler>(
            [this](IWebView2WebView* sender, IWebView2NavigationCompletedEventArgs* args)
                -> HRESULT {
                BOOL success;
                CHECK_FAILURE(args->get_IsSuccess(&success));
                if (!success)
                {
                    WEBVIEW2_WEB_ERROR_STATUS webErrorStatus;
                    CHECK_FAILURE(args->get_WebErrorStatus(&webErrorStatus));
                    if (webErrorStatus == WEBVIEW2_WEB_ERROR_STATUS_DISCONNECTED)
                    {
                        // Do something here if you want to handle a specific error case.
                        // In most cases this isn't necessary, because the WebView will
                        // display its own error page automatically.
                    }
                }

                BOOL canGoBack;
                BOOL canGoForward;
                sender->get_CanGoBack(&canGoBack);
                sender->get_CanGoForward(&canGoForward);
                EnableWindow(m_toolbar->backWindow, canGoBack);
                EnableWindow(m_toolbar->forwardWindow, canGoForward);
                EnableWindow(m_toolbar->cancelWindow, FALSE);
                return S_OK;
            })
            .Get(),
        &m_navigationCompletedToken));
```

#### remove_NavigationCompleted 

Entfernen Sie einen Ereignishandler, der zuvor mit add_NavigationCompleted hinzugefügt wurde.

> Public HRESULT [remove_NavigationCompleted](#remove_navigationcompleted)(EventRegistrationToken-Token)

#### add_FrameNavigationStarting 

Fügen Sie einen Ereignishandler für das FrameNavigationStarting-Ereignis hinzu.

> Public HRESULT [add_FrameNavigationStarting](#add_framenavigationstarting)([IWebView2NavigationStartingEventHandler](IWebView2NavigationStartingEventHandler.md) * EventHandler, EventRegistrationToken * Token)

FrameNavigationStarting wird ausgelöst, wenn ein untergeordneter Frame in der WebView die Berechtigung zum Navigieren zu einem anderen URI anfordert. Dies wird auch für Umleitungen ausgelöst.

```cpp
    // Register a handler for the FrameNavigationStarting event.
    // This handler will prevent a frame from navigating to a blocked domain.
    CHECK_FAILURE(m_webView->add_FrameNavigationStarting(
        Callback<IWebView2NavigationStartingEventHandler>(
            [this](IWebView2WebView* sender,
                   IWebView2NavigationStartingEventArgs* args) -> HRESULT
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

#### remove_FrameNavigationStarting 

Entfernen Sie einen Ereignishandler, der zuvor mit add_FrameNavigationStarting hinzugefügt wurde.

> Public HRESULT [remove_FrameNavigationStarting](#remove_framenavigationstarting)(EventRegistrationToken-Token)

#### add_MoveFocusRequested 

Fügen Sie einen Ereignishandler für das MoveFocusRequested-Ereignis hinzu.

> Public HRESULT [add_MoveFocusRequested](#add_movefocusrequested)([IWebView2MoveFocusRequestedEventHandler](IWebView2MoveFocusRequestedEventHandler.md) * EventHandler, EventRegistrationToken * Token)

MoveFocusRequested wird ausgelöst, wenn der Benutzer versucht, die Tab-Taste aus der WebView zu ziehen. Der Fokus der WebView wurde nicht geändert, wenn dieses Ereignis ausgelöst wird.

```cpp
    // Register a handler for the MoveFocusRequested event.
    // This event will be fired when the user tabs out of the webview.
    // The handler will focus another window in the app, depending on which
    // direction the focus is being shifted.
    CHECK_FAILURE(m_webView->add_MoveFocusRequested(
        Callback<IWebView2MoveFocusRequestedEventHandler>(
            [this](IWebView2WebView* sender, IWebView2MoveFocusRequestedEventArgs* args)
                -> HRESULT {
                if (!g_autoTabHandle)
                {
                    WEBVIEW2_MOVE_FOCUS_REASON reason;
                    CHECK_FAILURE(args->get_Reason(&reason));

                    if (reason == WEBVIEW2_MOVE_FOCUS_REASON_NEXT)
                    {
                        TabForwards(-1);
                    }
                    else if (reason == WEBVIEW2_MOVE_FOCUS_REASON_PREVIOUS)
                    {
                        TabBackwards(int(m_tabbableWindows.size()));
                    }
                    CHECK_FAILURE(args->put_Handled(TRUE));
                }
                return S_OK;
            })
            .Get(),
        &m_moveFocusRequestedToken));
```

#### remove_MoveFocusRequested 

Entfernen Sie einen Ereignishandler, der zuvor mit add_MoveFocusRequested hinzugefügt wurde.

> Public HRESULT [remove_MoveFocusRequested](#remove_movefocusrequested)(EventRegistrationToken-Token)

#### add_GotFocus 

Fügen Sie einen Ereignishandler für das GotFocus-Ereignis hinzu.

> Public HRESULT [add_GotFocus](#add_gotfocus)([IWebView2FocusChangedEventHandler](IWebView2FocusChangedEventHandler.md) * EventHandler, EventRegistrationToken * Token)

GotFocus wird ausgelöst, wenn WebView den Fokus erhält.

#### remove_GotFocus 

Entfernen Sie einen Ereignishandler, der zuvor mit add_GotFocus hinzugefügt wurde.

> Public HRESULT [remove_GotFocus](#remove_gotfocus)(EventRegistrationToken-Token)

#### add_LostFocus 

Fügen Sie einen Ereignishandler für das LostFocus-Ereignis hinzu.

> Public HRESULT [add_LostFocus](#add_lostfocus)([IWebView2FocusChangedEventHandler](IWebView2FocusChangedEventHandler.md) * EventHandler, EventRegistrationToken * Token)

LostFocus wird ausgelöst, wenn WebView den Fokus verloren hat. In dem Fall, in dem das MoveFocusRequested-Ereignis ausgelöst wird, liegt der Fokus weiterhin auf WebView, wenn das MoveFocusRequested-Ereignis ausgelöst wird. Der verlorene Fokus wird erst dann ausgelöst, wenn der app-Code oder die Standardaktion des MoveFocusRequested-Ereignisses den Fokus von WebView absetzen.

#### remove_LostFocus 

Entfernen Sie einen Ereignishandler, der zuvor mit add_LostFocus hinzugefügt wurde.

> Public HRESULT [remove_LostFocus](#remove_lostfocus)(EventRegistrationToken-Token)

#### add_WebResourceRequested_deprecated 

Diese API wird als veraltet markiert, bitte verwenden Sie die neue add_WebResourceRequested-API.

> Public HRESULT [add_WebResourceRequested_deprecated](#add_webresourcerequested_deprecated)(LPCWSTR * const urlFilter,[WEBVIEW2_WEB_RESOURCE_CONTEXT](#webview2_web_resource_context) * const resourceContextFilter, size_t filterLength,[IWebView2WebResourceRequestedEventHandler](IWebView2WebResourceRequestedEventHandler.md) * EventHandler, EventRegistrationToken * Token)

Fügen Sie einen Ereignishandler für das WebResourceRequested-Ereignis hinzu. Wird ausgelöst, wenn die WebView eine HTTP-Anforderung ausführt. Verwenden Sie urlFilter, um eine Liste mit der Größe filterLength von URLs zu übergeben, auf die Sie lauschen möchten. Jeder URL-Eintrag unterstützt auch Platzhalter: "*" entspricht NULL oder mehr Zeichen, und "?" entspricht genau einem Zeichen. Stellen Sie für jeden urlFilter-Eintrag eine übereinstimmende resourceContextFilter bereit, die die Ressourcentypen darstellt, für die WebResourceRequested ausgelöst werden soll. Ist filterLength 0, wird das Ereignis für alle Netzwerkanforderungen ausgelöst. Die unterstützten Ressourcen Kontexte sind: Document, Stylesheet, Image, Media, Font, Script, XMLHttpRequest, FETCH.

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

#### remove_WebResourceRequested 

Entfernen Sie einen Ereignishandler, der zuvor mit add_WebResourceRequested hinzugefügt wurde.

> Public HRESULT [remove_WebResourceRequested](#remove_webresourcerequested)(EventRegistrationToken-Token)

#### add_ScriptDialogOpening 

Fügen Sie einen Ereignishandler für das ScriptDialogOpening-Ereignis hinzu.

> Public HRESULT [add_ScriptDialogOpening](#add_scriptdialogopening)([IWebView2ScriptDialogOpeningEventHandler](IWebView2ScriptDialogOpeningEventHandler.md) * EventHandler, EventRegistrationToken * Token)

Das Ereignis wird ausgelöst, wenn ein JavaScript-Dialogfeld (Benachrichtigung, Bestätigung oder Eingabeaufforderung) für die WebView angezeigt wird. Dieses Ereignis wird nur ausgelöst, wenn die IWebView2Settings:: AreDefaultScriptDialogsEnabled-Eigenschaft auf false festgelegt ist.

```cpp
    // Register a handler for the ScriptDialogOpening event.
    // This handler will set up a custom prompt dialog for the user,
    // and may defer the event if the setting to defer dialogs is enabled.
    CHECK_FAILURE(m_webView->add_ScriptDialogOpening(
        Callback<IWebView2ScriptDialogOpeningEventHandler>(
            [this](
                IWebView2WebView* sender,
                IWebView2ScriptDialogOpeningEventArgs* args) -> HRESULT
    {
        wil::com_ptr<IWebView2ScriptDialogOpeningEventArgs> eventArgs = args;
        auto showDialog = [this, eventArgs]
        {
            wil::unique_cotaskmem_string uri;
            WEBVIEW2_SCRIPT_DIALOG_KIND type;
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
                /* readonly */ type != WEBVIEW2_SCRIPT_DIALOG_KIND_PROMPT);
            if (dialog.confirmed)
            {
                CHECK_FAILURE(eventArgs->put_ResultText(dialog.input.c_str()));
                CHECK_FAILURE(eventArgs->Accept());
            }
        };

        if (m_deferScriptDialogs)
        {
            wil::com_ptr<IWebView2Deferral> deferral;
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

#### remove_ScriptDialogOpening 

Entfernen Sie einen Ereignishandler, der zuvor mit add_ScriptDialogOpening hinzugefügt wurde.

> Public HRESULT [remove_ScriptDialogOpening](#remove_scriptdialogopening)(EventRegistrationToken-Token)

#### add_ZoomFactorChanged 

Fügen Sie einen Ereignishandler für das ZoomFactorChanged-Ereignis hinzu.

> Public HRESULT [add_ZoomFactorChanged](#add_zoomfactorchanged)([IWebView2ZoomFactorChangedEventHandler](IWebView2ZoomFactorChangedEventHandler.md) * EventHandler, EventRegistrationToken * Token)

Das Ereignis wird ausgelöst, wenn die ZoomFactor-Eigenschaft des WebView geändert wird. Das Ereignis konnte ausgelöst werden, weil der Aufrufer die ZoomFactor-Eigenschaft geändert hat, oder weil der Benutzer den Zoom manuell geändert hat. Wenn Sie vom Aufrufer über die ZoomFactor-Eigenschaft geändert wird, wird der interne Zoomfaktor sofort aktualisiert, und es gibt kein ZoomFactorChanged-Ereignis. WebView ordnet den zuletzt verwendeten Zoomfaktor für jede Website zu. Daher ist es möglich, dass sich der Zoomfaktor ändert, wenn Sie zu einer anderen Seite navigieren. Wenn sich der Zoomfaktor aufgrund dieser Änderung ändert, wird das ZoomFactorChanged-Ereignis direkt hinter dem DocumentStateChanged-Ereignis ausgelöst.

```cpp
    // Register a handler for the ZoomFactorChanged event.
    // This handler just announces the new level of zoom on the window's title bar.
    CHECK_FAILURE(m_webView->add_ZoomFactorChanged(
        Callback<IWebView2ZoomFactorChangedEventHandler>(
            [this](IWebView2WebView* sender, IUnknown* args) -> HRESULT {
                double zoomFactor;
                CHECK_FAILURE(sender->get_ZoomFactor(&zoomFactor));

                std::wstring message = L"WebView2APISample (Zoom: " +
                                       std::to_wstring(int(zoomFactor * 100)) + L"%)";
                SetWindowText(m_appWindow->GetMainWindow(), message.c_str());
                return S_OK;
            })
            .Get(),
        &m_zoomFactorChangedToken));
```

#### remove_ZoomFactorChanged 

Entfernen Sie einen Ereignishandler, der zuvor mit add_ZoomFactorChanged hinzugefügt wurde.

> Public HRESULT [remove_ZoomFactorChanged](#remove_zoomfactorchanged)(EventRegistrationToken-Token)

#### add_PermissionRequested 

Fügen Sie einen Ereignishandler für das PermissionRequested-Ereignis hinzu.

> Public HRESULT [add_PermissionRequested](#add_permissionrequested)([IWebView2PermissionRequestedEventHandler](IWebView2PermissionRequestedEventHandler.md) * EventHandler, EventRegistrationToken * Token)

Wird ausgelöst, wenn Inhalt in einer WebView-Anforderung die Berechtigung für den Zugriff auf einige Privilegierte Ressourcen anfordert.

```cpp
    // Register a handler for the PermissionRequested event.
    // This handler prompts the user to allow or deny the request.
    CHECK_FAILURE(m_webView->add_PermissionRequested(
        Callback<IWebView2PermissionRequestedEventHandler>(
            [this](
                IWebView2WebView* sender,
                IWebView2PermissionRequestedEventArgs* args) -> HRESULT
    {
        wil::unique_cotaskmem_string uri;
        WEBVIEW2_PERMISSION_TYPE type = WEBVIEW2_PERMISSION_TYPE_UNKNOWN_PERMISSION;
        BOOL userInitiated = FALSE;

        CHECK_FAILURE(args->get_Uri(&uri));
        CHECK_FAILURE(args->get_PermissionType(&type));
        CHECK_FAILURE(args->get_IsUserInitiated(&userInitiated));

        std::wstring message = L"Do you want to grant permission for ";
        message += NameOfPermissionType(type);
        message += L" to the website at ";
        message += uri.get();
        message += L"?\n\n";
        message += (userInitiated
            ? L"This request came from a user gesture."
            : L"This request did not come from a user gesture.");

        int response = MessageBox(nullptr, message.c_str(), L"Permission Request",
                                   MB_YESNOCANCEL | MB_ICONWARNING);

        WEBVIEW2_PERMISSION_STATE state =
              response == IDYES ? WEBVIEW2_PERMISSION_STATE_ALLOW
            : response == IDNO  ? WEBVIEW2_PERMISSION_STATE_DENY
            :                     WEBVIEW2_PERMISSION_STATE_DEFAULT;
        CHECK_FAILURE(args->put_State(state));

        return S_OK;
    }).Get(), &m_permissionRequestedToken));
```

#### remove_PermissionRequested 

Entfernen Sie einen Ereignishandler, der zuvor mit add_PermissionRequested hinzugefügt wurde.

> Public HRESULT [remove_PermissionRequested](#remove_permissionrequested)(EventRegistrationToken-Token)

#### add_ProcessFailed 

Fügen Sie einen Ereignishandler für das ProcessFailed-Ereignis hinzu.

> Public HRESULT [add_ProcessFailed](#add_processfailed)([IWebView2ProcessFailedEventHandler](IWebView2ProcessFailedEventHandler.md) * EventHandler, EventRegistrationToken * Token)

Wird ausgelöst, wenn ein WebView-Prozess unerwartet beendet wird oder nicht mehr reagiert.

```cpp
    // Register a handler for the ProcessFailed event.
    // This handler checks if the browser process failed, and asks the user if
    // they want to recreate the webview.
    CHECK_FAILURE(m_webView->add_ProcessFailed(
        Callback<IWebView2ProcessFailedEventHandler>(
            [this](IWebView2WebView* sender,
                IWebView2ProcessFailedEventArgs* args) -> HRESULT
    {
        WEBVIEW2_PROCESS_FAILED_KIND failureType;
        CHECK_FAILURE(args->get_ProcessFailedKind(&failureType));
        if (failureType == WEBVIEW2_PROCESS_FAILED_KIND_BROWSER_PROCESS_EXITED)
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
        return S_OK;
    }).Get(), &m_processFailedToken));
```

#### remove_ProcessFailed 

Entfernen Sie einen Ereignishandler, der zuvor mit add_ProcessFailed hinzugefügt wurde.

> Public HRESULT [remove_ProcessFailed](#remove_processfailed)(EventRegistrationToken-Token)

#### AddScriptToExecuteOnDocumentCreated 

Fügen Sie das bereitgestellte JavaScript einer Liste von Skripts hinzu, die ausgeführt werden sollen, nachdem das globale Objekt erstellt wurde, aber bevor das HTML-Dokument analysiert wurde und bevor ein anderes Skript ausgeführt wird, das vom HTML-Dokument eingeschlossen ist.

> Public HRESULT [AddScriptToExecuteOnDocumentCreated](#addscripttoexecuteondocumentcreated)(LPCWSTR javaScript,[IWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler](IWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler.md) * Handler)

Das eingefügte Skript gilt für alle zukünftigen Dokumente und untergeordneten Frame-Navigationselemente auf oberster Ebene, bis Sie mit RemoveScriptToExecuteOnDocumentCreated entfernt werden. Diese wird asynchron angewendet, und Sie müssen warten, bis der vervollständigungshandler ausgeführt wird, bevor Sie sicher sein können, dass das Skript für zukünftige Navigationen ausgeführt werden kann.

Beachten Sie, dass sich dies auf das hier ausgeführte Skript auswirkt, wenn ein HTML-Dokument über Sandbox [-Eigenschaften oder über den](https://developer.mozilla.org/docs/Web/HTML/Element/iframe#attr-sandbox) [Content-Security-Policy-HTTP-Header](https://developer.mozilla.org/docs/Web/HTTP/Headers/Content-Security-Policy) eine Art Sandbox hat. Wenn also beispielsweise das Schlüsselwort "Allow-modals" nicht festgesetzt ist, werden Aufrufe der `alert` Funktion ignoriert.

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
            Callback<IWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler>(
                [this](HRESULT error, PCWSTR id) -> HRESULT
        {
            m_lastInitializeScriptId = id;
            MessageBox(nullptr, id, L"AddScriptToExecuteOnDocumentCreated Id", MB_OK);
            return S_OK;
        }).Get());

    }
}
```

#### RemoveScriptToExecuteOnDocumentCreated 

Entfernen Sie das entsprechende JavaScript, das über AddScriptToExecuteOnDocumentCreated hinzugefügt wurde.

> Public HRESULT [RemoveScriptToExecuteOnDocumentCreated](#removescripttoexecuteondocumentcreated)(LPCWSTR-ID)

#### ExecuteScript 

Führen Sie JavaScript-Code aus dem JavaScript-Parameter im aktuellen Dokument der obersten Ebene aus, das in der WebView gerendert wird.

> Public HRESULT [executeScript](#executescript)(LPCWSTR javaScript,[IWebView2ExecuteScriptCompletedHandler](IWebView2ExecuteScriptCompletedHandler.md) * Handler)

Dies wird asynchron ausgeführt, und wenn ein Handler im ExecuteScriptCompletedHandler-Parameter bereitgestellt wird, wird die Invoke-Methode mit dem Ergebnis der Auswertung des bereitgestellten JavaScript aufgerufen. Der Ergebniswert ist eine JSON-codierte Zeichenfolge. Wenn das Ergebnis undefiniert ist, einen Referenz Zyklus enthält oder in JSON nicht codiert werden kann, wird der JSON-NULL-Wert als Zeichenfolge "Null" zurückgegeben. Beachten Sie, dass eine Funktion, die keinen expliziten Rückgabewert aufweist, undefined zurückgibt. Wenn das ausgeführte Skript eine nicht behandelte Ausnahme auslöst, ist das Ergebnis auch "Null". Diese Methode wird asynchron angewendet. Wenn der Aufruf erfolgt, während sich die WebView in einem Dokument befindet und eine Navigation nach dem Aufruf erfolgt, aber bevor das JavaScript ausgeführt wird, wird das Skript nicht ausgeführt, und der Handler wird mit E_FAIL für seinen errorCode-Parameter aufgerufen. ExecuteScript funktioniert auch dann, wenn IsScriptEnabled auf "false" festgelegt ist.

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
            Callback<IWebView2ExecuteScriptCompletedHandler>(
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

#### CapturePreview 

Erfassen Sie ein Bild von der Anzeige von WebView.

> Public HRESULT [CapturePreview](#capturepreview)([WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT](#webview2_capture_preview_image_format) Image Format, IStream * ImageStream,[IWebView2CapturePreviewCompletedHandler](IWebView2CapturePreviewCompletedHandler.md) *-Handler)

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
            WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT_PNG, stream.get(),
            Callback<IWebView2CapturePreviewCompletedHandler>(
                [mainWindow](HRESULT error_code) -> HRESULT {
                    CHECK_FAILURE(error_code);

                    MessageBox(mainWindow, L"Preview Captured", L"Preview Captured", MB_OK);
                    return S_OK;
                })
                .Get()));
    }
}
```

#### Laden 

Laden Sie die aktuelle Seite neu.

> Public HRESULT [Reload](#reload)()

Dies ähnelt der Navigation zum URI des aktuellen Dokuments auf oberster Ebene, einschließlich aller Navigationsereignisse, die alle Einträge im HTTP-Cache auslösen und respektieren. Das zurück/weiter-Protokoll wird jedoch nicht geändert.

#### get_Bounds 

Die WebView-Begrenzungen.

> öffentliche HRESULT- [get_Bounds](#get_bounds)(Rect * bounds)

Begrenzungen sind relativ zum übergeordneten HWND. Die APP hat zwei Möglichkeiten, um eine WebView-Position zu positionieren:

1. Erstellen Sie ein untergeordnetes HWND, das das übergeordnete HWND von WebView ist. Positionieren Sie dieses Fenster, in dem sich die WebView befinden soll. Verwenden Sie in diesem Fall (0, 0) für die Bound's obere linke Ecke des Webviews (den Offset).

1. Verwenden Sie das oberste Fenster der App als übergeordnetes WebView-HWND. Stellen Sie die Bound's-obere linke Ecke der WebView so ein, dass die WebView in der APP richtig positioniert ist. Die Werte der Bounds befinden sich im Koordinatenbereich des Hosts.

#### put_Bounds 

Die Bounds-Eigenschaft festlegen.

> öffentliche HRESULT- [put_Bounds](#put_bounds)(Rect-Begrenzungen)

```cpp
// Update the bounds of the WebView window to fit available space.
void ViewComponent::ResizeWebView()
{
    RECT desiredBounds = m_webViewBounds;
    desiredBounds.bottom = LONG(
        (m_webViewBounds.bottom - m_webViewBounds.top) * m_webViewRatio + m_webViewBounds.top);
    desiredBounds.right = LONG(
        (m_webViewBounds.right - m_webViewBounds.left) * m_webViewRatio + m_webViewBounds.left);

    m_webView->put_Bounds(desiredBounds);
}
```

#### get_ZoomFactor 

Der Zoomfaktor für die aktuelle Seite im WebView.

> öffentliche HRESULT- [get_ZoomFactor](#get_zoomfactor)(Double * ZoomFactor)

Der Zoomfaktor wird pro Website beibehalten. Beachten Sie, dass das Ändern des Zoomfaktors `window.innerWidth/innerHeight` zu einer Änderung des Seitenlayouts führen kann. Wenn WebView von einer anderen Website zu einer Seite navigiert, wird der Zoomfaktor für die vorherige Seite nicht angewendet. Wenn die APP den Zoomfaktor für eine bestimmte Seite einstellen möchte, befindet sich der früheste Ort im DocumentStateChanged-Ereignishandler. Wenn dies der Fall ist, wird möglicherweise ein ZoomFactorChanged-Ereignis für den beibehaltenen Zoomfaktor empfangen, bevor das ZoomFactorChanged-Ereignis für den angegebenen Zoomfaktor empfangen wird. Die Angabe einer ZoomFactor kleiner oder gleich 0 ist nicht zulässig. WebView verfügt auch über einen internen unterstützten Zoomfaktor Bereich. Wenn sich ein angegebener Zoomfaktor außerhalb dieses Bereichs befindet, wird er normalisiert, sodass er innerhalb des Bereichs liegt, und ein ZoomFactorChanged-Ereignis wird für den tatsächlich angewendeten Zoomfaktor ausgelöst. Wenn diese Bereichs Normalisierung erfolgt, meldet die ZoomFactor-Eigenschaft den Zoomfaktor, der während der vorherigen Änderung der ZoomFactor-Eigenschaft angegeben wird, bis das ZoomFactorChanged-Ereignis empfangen wird, nachdem WebView den normalisierten Zoomfaktor angewendet hat.

#### put_ZoomFactor 

Festlegen der ZoomFactor-Eigenschaft

> öffentliche HRESULT- [put_ZoomFactor](#put_zoomfactor)(Double ZoomFactor)

#### get_IsVisible 

Die IsVisible-Eigenschaft bestimmt, ob die WebView angezeigt oder ausgeblendet werden soll.

> öffentliche HRESULT- [get_IsVisible](#get_isvisible)(bool * isVisible)

Wenn IsVisible auf "false" festgelegt ist, ist die WebView transparent und wird nicht gerendert. Dies wirkt sich jedoch nicht auf das Fenster aus, das die WebView enthält (den HWND-Parameter, der an CreateView übergeben wurde). Wenn Sie möchten, dass das Fenster ebenfalls ausgeblendet wird, rufen Sie ShowWindow direkt zusätzlich zum Ändern der IsVisible-Eigenschaft auf. WebView als untergeordnetes Fenster ruft keine Fenster Meldungen ab, wenn das oberste Fenster minimiert oder wiederhergestellt wird. Aus Leistungsgründen sollte Entwickler die IsVisible-Eigenschaft der WebView-Eigenschaft auf "false" festlegen, wenn das App-Fenster minimiert wird, und zurück zu "true", wenn das App-Fenster wiederhergestellt wird. Das App-Fenster kann dies tun, indem SC_MINIMIZE und SC_RESTORE Befehl beim empfangen WM_SYSCOMMAND Nachricht behandelt werden.

```cpp
void ViewComponent::ToggleVisibility()
{
    BOOL visible;
    m_webView->get_IsVisible(&visible);
    m_isVisible = !visible;
    m_webView->put_IsVisible(m_isVisible);
}
```

#### put_IsVisible 

Festlegen der IsVisible-Eigenschaft

> öffentliche HRESULT- [put_IsVisible](#put_isvisible)(bool isVisible)

```cpp
    if (message == WM_SYSCOMMAND)
    {
        if (wParam == SC_MINIMIZE)
        {
            // Hide the webview when the app window is minimized.
            m_webView->put_IsVisible(FALSE);
        }
        else if (wParam == SC_RESTORE)
        {
            // When the app window is restored, show the webview
            // (unless the user has toggle visibility off).
            if (m_isVisible)
            {
                m_webView->put_IsVisible(TRUE);
            }
        }
    }
```

#### PostWebMessageAsJson 

Posten Sie die angegebene Webnachricht im Dokument der obersten Ebene in diesem [IWebView2WebView]().

> Public HRESULT [PostWebMessageAsJson](#postwebmessageasjson)(LPCWSTR webMessageAsJson)

Das Nachrichtenereignis des Fensters "Window. Chrome. WebView" des obersten Dokuments wird ausgelöst. JavaScript in diesem Dokument kann das Ereignis über Folgendes abonnieren und kündigen: 

```cpp
window.chrome.webview.addEventListener('message', handler)
window.chrome.webview.removeEventListener('message', handler)
```

 Das Ereignis args ist eine Instanz von `MessageEvent` . Die IWebView2Settings:: IsWebMessageEnabled-Einstellung muss wahr sein, oder diese Methode schlägt mit E_INVALIDARG fehl. Die Dateneigenschaft des Ereignisses arg ist der webmessage-Zeichenfolgenparameter, der als JSON-Zeichenfolge in ein JavaScript-Objekt analysiert wurde. Die Source-Eigenschaft des Ereignisses arg ist ein Verweis auf das `window.chrome.webview` Objekt. Informationen zum Senden von Nachrichten aus dem HTML-Dokument in der WebView an den Host finden Sie unter SetWebMessageReceivedEventHandler. Diese Nachricht wird asynchron gesendet. Wenn eine Navigation erfolgt, bevor die Nachricht auf der Seite veröffentlicht wird, wird die Nachricht nicht gesendet.

```cpp
    // Setup the web message received event handler before navigating to
    // ensure we don't miss any messages.
    CHECK_FAILURE(m_webView->add_WebMessageReceived(
        Microsoft::WRL::Callback<IWebView2WebMessageReceivedEventHandler>(
            [this](IWebView2WebView* sender, IWebView2WebMessageReceivedEventArgs* args)
    {
        wil::unique_cotaskmem_string uri;
        CHECK_FAILURE(args->get_Source(&uri));

        // Always validate that the origin of the message is what you expect.
        if (uri.get() != m_sampleUri)
        {
            return S_OK;
        }
        wil::unique_cotaskmem_string messageRaw;
        CHECK_FAILURE(args->get_WebMessageAsString(&messageRaw));
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

#### add_WebMessageReceived 

Dieses Ereignis wird ausgelöst, wenn die IsWebMessageEnabled-Einstellung festgelegt ist, und das Dokument auf oberster Ebene des WebView-Anrufs `window.chrome.webview.postMessage` .

> öffentliche HRESULT- [add_WebMessageReceived](#add_webmessagereceived)([IWebView2WebMessageReceivedEventHandler](IWebView2WebMessageReceivedEventHandler.md) *-Handler, EventRegistrationToken *-Token)

Bei der Funktion PostMessage handelt es sich um `void postMessage(object)` ein Objekt, das von der JSON-Konvertierung unterstützt wird.

```cpp
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

 Wenn PostMessage aufgerufen wird, wird der [IWebView2WebMessageReceivedEventHandler](IWebView2WebMessageReceivedEventHandler.md) -Satz über diese SetWebMessageReceivedEventHandler-Methode aufgerufen, wobei der Objektparameter der PostMessage in eine JSON-Zeichenfolge konvertiert wird.

```cpp
    // Setup the web message received event handler before navigating to
    // ensure we don't miss any messages.
    CHECK_FAILURE(m_webView->add_WebMessageReceived(
        Microsoft::WRL::Callback<IWebView2WebMessageReceivedEventHandler>(
            [this](IWebView2WebView* sender, IWebView2WebMessageReceivedEventArgs* args)
    {
        wil::unique_cotaskmem_string uri;
        CHECK_FAILURE(args->get_Source(&uri));

        // Always validate that the origin of the message is what you expect.
        if (uri.get() != m_sampleUri)
        {
            return S_OK;
        }
        wil::unique_cotaskmem_string messageRaw;
        CHECK_FAILURE(args->get_WebMessageAsString(&messageRaw));
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

#### remove_WebMessageReceived 

Entfernen Sie einen Ereignishandler, der zuvor mit add_WebMessageReceived hinzugefügt wurde.

> Public HRESULT [remove_WebMessageReceived](#remove_webmessagereceived)(EventRegistrationToken-Token)

#### Schließen 

Schließt die WebView und bereinigt die zugrunde liegende Browserinstanz.

> Public HRESULT [Close](#close)()

Durch Bereinigen des Browsers Instanz werden die Ressourcen freigegeben, die die WebView-Ansicht einschalten. Die Browserinstanz wird heruntergefahren, wenn keine anderen Webansichten verwendet werden.

Nach dem Aufruf von Close werden alle Methodenaufrufe fehlschlagen, und die Ereignishandler werden nicht mehr ausgelöst. Insbesondere gibt die WebView Ihre Verweise auf die Ereignishandler frei, wenn Close aufgerufen wird.

Close wird implizit aufgerufen, wenn die WebView den endgültigen Bezug verliert und zerstört wird. Es empfiehlt sich jedoch, explizit Close aufzurufen, um einen zufälligen Zyklus von Verweisen zwischen WebView und app-Code zu vermeiden. Insbesondere wenn Sie einen Verweis auf die WebView in einem Ereignishandler aufzeichnen, erstellen Sie einen Referenz Zyklus zwischen WebView und dem Ereignishandler. Schließen bricht diesen Zyklus ab, indem alle Ereignishandler freigegeben werden. Um diese Situation zu vermeiden, empfiehlt es sich jedoch, sowohl explizit Close für die WebView aufzurufen und keinen Verweis auf die WebView zu erfassen, um sicherzustellen, dass die WebView ordnungsgemäß bereinigt werden kann.

```cpp
// Close the WebView and deinitialize related state. This doesn't close the app window.
void AppWindow::CloseWebView()
{
    DeleteAllComponents();
    if (m_webView)
    {
        m_webView->Close();
        m_webView = nullptr;
    }
    m_webViewEnvironment = nullptr;
}
```

#### CallDevToolsProtocolMethod 

Rufen Sie eine asynchrone DevToolsProtocol-Methode auf.

> Public HRESULT [CallDevToolsProtocolMethod](#calldevtoolsprotocolmethod)(LPCWSTR MethodName, LPCWSTR parametersAsJson,[IWebView2CallDevToolsProtocolMethodCompletedHandler](IWebView2CallDevToolsProtocolMethodCompletedHandler.md) * Handler)

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
            Callback<IWebView2CallDevToolsProtocolMethodCompletedHandler>(
                [](HRESULT error, PCWSTR resultJson) -> HRESULT
                {
                    MessageBox(nullptr, resultJson, L"CDP Method Result", MB_OK);
                    return S_OK;
                }).Get());
    }
}
```

#### add_DevToolsProtocolEventReceived 

Abonnieren eines DevToolsProtocol-Ereignisses

> Public HRESULT [add_DevToolsProtocolEventReceived](#add_devtoolsprotocoleventreceived)(LPCWSTR EventName,[IWebView2DevToolsProtocolEventReceivedEventHandler](IWebView2DevToolsProtocolEventReceivedEventHandler.md) * Handler, EventRegistrationToken * Token)

Eine Liste und eine Beschreibung der verfügbaren Ereignisse finden Sie im [devtools-Protokoll-Viewer](https://aka.ms/DevToolsProtocolDocs) . Der eventName-Parameter ist der vollständige Name des Ereignisses im Format `{domain}.{event}` . Die Invoke-Methode des Handlers wird aufgerufen, wenn das entsprechende DevToolsProtocol-Ereignis ausgelöst wird. Invoke wird mit dem Ereignis args-Objekt aufgerufen, das das Parameter-Objekt des CDP-Ereignisses als JSON-Zeichenfolge enthält.

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
        // If we are already subscribed to this event, unsubscribe first.
        auto preexistingToken = m_devToolsProtocolEventReceivedTokenMap.find(eventName);
        if (preexistingToken != m_devToolsProtocolEventReceivedTokenMap.end())
        {
            CHECK_FAILURE(m_webView->remove_DevToolsProtocolEventReceived(
                eventName.c_str(),
                preexistingToken->second));
        }

        CHECK_FAILURE(m_webView->add_DevToolsProtocolEventReceived(
            eventName.c_str(),
            Callback<IWebView2DevToolsProtocolEventReceivedEventHandler>(
                [eventName](IWebView2WebView* sender,
                            IWebView2DevToolsProtocolEventReceivedEventArgs* args)
                -> HRESULT
        {
            wil::unique_cotaskmem_string parameterObjectAsJson;
            CHECK_FAILURE(args->get_ParameterObjectAsJson(&parameterObjectAsJson));
            MessageBox(nullptr, parameterObjectAsJson.get(),
                       (L"CDP Event Fired: " + eventName).c_str(), MB_OK);
            return S_OK;
        }).Get(), &m_devToolsProtocolEventReceivedTokenMap[eventName]));
    }
}
```

#### remove_DevToolsProtocolEventReceived 

Entfernen Sie einen Ereignishandler, der zuvor mit add_DevToolsProtocolEventReceived hinzugefügt wurde.

> Public HRESULT [remove_DevToolsProtocolEventReceived](#remove_devtoolsprotocoleventreceived)(LPCWSTR EventName, EventRegistrationToken-Token)

#### get_BrowserProcessId 

Die Prozess-ID des Browser Prozesses, der die WebView hostet.

> Public HRESULT [get_BrowserProcessId](#get_browserprocessid)(UInt32 *-Wert)

#### get_CanGoBack 

Kann im WebView zur vorherigen Seite im Navigationsverlauf navigieren.

> Public HRESULT [get_CanGoBack](#get_cangoback)(bool * CanGoBack)

get_CanGoBack ändern Sie den Wert mit dem DocumentStateChanged-Ereignis.

#### get_CanGoForward 

Kann im WebView zur nächsten Seite im Navigationsverlauf navigieren.

> Public HRESULT [get_CanGoForward](#get_cangoforward)(bool * CanGoForward)

get_CanGoForward ändern Sie den Wert mit dem DocumentStateChanged-Ereignis.

#### GoBack 

Navigiert die WebView zur vorherigen Seite im Navigationsverlauf.

> Public HRESULT [GoBack](#goback)()

#### GoForward 

Navigiert die WebView zur nächsten Seite im Navigationsverlauf.

> Public HRESULT [GoForward](#goforward)()

#### WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT 

Bildformat, das von der [IWebView2WebView:: CapturePreview](#capturepreview) -Methode verwendet wird.

> Enum- [WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT](#webview2_capture_preview_image_format)

 Werte                         | Beschreibungen
--------------------------------|---------------------------------------------
WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT_PNG            | PNG-Bildformat.
WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT_JPEG            | JPEG-Bildformat.

#### WEBVIEW2_SCRIPT_DIALOG_KIND 

Art des in der [IWebView2ScriptDialogOpeningEventHandler](IWebView2ScriptDialogOpeningEventHandler.md) -Schnittstelle verwendeten JavaScript-Dialogfelds.

> Enum- [WEBVIEW2_SCRIPT_DIALOG_KIND](#webview2_script_dialog_kind)

 Werte                         | Beschreibungen
--------------------------------|---------------------------------------------
WEBVIEW2_SCRIPT_DIALOG_KIND_ALERT            | Ein Dialogfeld, das über die JavaScript-Funktion "Window. Alert" aufgerufen wird.
WEBVIEW2_SCRIPT_DIALOG_KIND_CONFIRM            | Ein Dialogfeld, das über die JavaScript-Funktion "Fenster. bestätigen" aufgerufen wird.
WEBVIEW2_SCRIPT_DIALOG_KIND_PROMPT            | Ein Dialogfeld, das über die JavaScript-Funktion "Window. prompt" aufgerufen wird.

#### WEBVIEW2_PROCESS_FAILED_KIND 

Art des in der [IWebView2ProcessFailedEventHandler](IWebView2ProcessFailedEventHandler.md) -Schnittstelle verwendeten Prozess Fehlers.

> Enum- [WEBVIEW2_PROCESS_FAILED_KIND](#webview2_process_failed_kind)

 Werte                         | Beschreibungen
--------------------------------|---------------------------------------------
WEBVIEW2_PROCESS_FAILED_KIND_BROWSER_PROCESS_EXITED            | Gibt an, dass der Browserprozess unerwartet beendet wurde.
WEBVIEW2_PROCESS_FAILED_KIND_RENDER_PROCESS_EXITED            | Gibt an, dass der Renderprozess unerwartet beendet wurde.
WEBVIEW2_PROCESS_FAILED_KIND_RENDER_PROCESS_UNRESPONSIVE            | Gibt an, dass der Renderprozess nicht mehr reagiert.

#### WEBVIEW2_PERMISSION_TYPE 

Der Typ einer Berechtigungsanforderung.

> Enum- [WEBVIEW2_PERMISSION_TYPE](#webview2_permission_type)

 Werte                         | Beschreibungen
--------------------------------|---------------------------------------------
WEBVIEW2_PERMISSION_TYPE_UNKNOWN_PERMISSION            | Unbekannte Berechtigung.
WEBVIEW2_PERMISSION_TYPE_MICROPHONE            | Berechtigung zum Aufzeichnen von Audio.
WEBVIEW2_PERMISSION_TYPE_CAMERA            | Berechtigung zum Aufzeichnen von Videos.
WEBVIEW2_PERMISSION_TYPE_GEOLOCATION            | Berechtigung für den Zugriff auf Geolocation.
WEBVIEW2_PERMISSION_TYPE_NOTIFICATIONS            | Berechtigung zum Senden von webbenachrichtigungen.
WEBVIEW2_PERMISSION_TYPE_OTHER_SENSORS            | Berechtigung für den Zugriff auf den generischen Sensor.
WEBVIEW2_PERMISSION_TYPE_CLIPBOARD_READ            | Berechtigung zum Lesen der Systemzwischenablage ohne Benutzergeste

#### WEBVIEW2_PERMISSION_STATE 

Antwort auf eine Berechtigungsanforderung.

> Enum- [WEBVIEW2_PERMISSION_STATE](#webview2_permission_state)

 Werte                         | Beschreibungen
--------------------------------|---------------------------------------------
WEBVIEW2_PERMISSION_STATE_DEFAULT            | Verwenden Sie das Standardbrowser Verhalten, das die Benutzer normalerweise zur Entscheidung auffordert.
WEBVIEW2_PERMISSION_STATE_ALLOW            | Erteilen Sie die Berechtigungsanforderung.
WEBVIEW2_PERMISSION_STATE_DENY            | Verweigern Sie die Berechtigungsanforderung.

#### WEBVIEW2_MOVE_FOCUS_REASON 

Grund für das Verschieben des Fokus

> Enum- [WEBVIEW2_MOVE_FOCUS_REASON](#webview2_move_focus_reason)

 Werte                         | Beschreibungen
--------------------------------|---------------------------------------------
WEBVIEW2_MOVE_FOCUS_REASON_PROGRAMMATIC            | Der Fokus für die Code Einstellung in WebView.
WEBVIEW2_MOVE_FOCUS_REASON_NEXT            | Verschieben des Fokus aufgrund von Tabstopps vorwärts
WEBVIEW2_MOVE_FOCUS_REASON_PREVIOUS            | Verschieben des Fokus aufgrund von Tabstopps rückwärts

#### WEBVIEW2_WEB_ERROR_STATUS 

Fehlerstatus Werte für Web-Navigationselemente.

> Enum- [WEBVIEW2_WEB_ERROR_STATUS](#webview2_web_error_status)

 Werte                         | Beschreibungen
--------------------------------|---------------------------------------------
WEBVIEW2_WEB_ERROR_STATUS_UNKNOWN            | Ein unbekannter Fehler ist aufgetreten.
WEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_COMMON_NAME_IS_INCORRECT            | Der allgemeine Name des SSL-Zertifikats entspricht nicht der Webadresse.
WEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_EXPIRED            | Das SSL-Zertifikat ist abgelaufen.
WEBVIEW2_WEB_ERROR_STATUS_CLIENT_CERTIFICATE_CONTAINS_ERRORS            | Das SSL-Clientzertifikat enthält Fehler.
WEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_REVOKED            | Das SSL-Zertifikat wurde gesperrt.
WEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_IS_INVALID            | Das SSL-Zertifikat ist ungültig.
WEBVIEW2_WEB_ERROR_STATUS_SERVER_UNREACHABLE            | Der Host ist nicht erreichbar.
WEBVIEW2_WEB_ERROR_STATUS_TIMEOUT            | Die Verbindung hat ein Zeitlimit überschritten.
WEBVIEW2_WEB_ERROR_STATUS_ERROR_HTTP_INVALID_SERVER_RESPONSE            | Der Server hat eine ungültige oder unbekannte Antwort zurückgegeben.
WEBVIEW2_WEB_ERROR_STATUS_CONNECTION_ABORTED            | Die Verbindung wurde abgebrochen.
WEBVIEW2_WEB_ERROR_STATUS_CONNECTION_RESET            | Die Verbindung wurde zurückgesetzt.
WEBVIEW2_WEB_ERROR_STATUS_DISCONNECTED            | Die Internet Verbindung wurde unterbrochen.
WEBVIEW2_WEB_ERROR_STATUS_CANNOT_CONNECT            | Verbindung mit Ziel kann nicht hergestellt werden.
WEBVIEW2_WEB_ERROR_STATUS_HOST_NAME_NOT_RESOLVED            | Der angegebene Hostname konnte nicht aufgelöst werden.
WEBVIEW2_WEB_ERROR_STATUS_OPERATION_CANCELED            | Der Vorgang wurde abgebrochen.
WEBVIEW2_WEB_ERROR_STATUS_REDIRECT_FAILED            | Die Anforderungs Umleitung ist fehlgeschlagen.
WEBVIEW2_WEB_ERROR_STATUS_UNEXPECTED_ERROR            | Ein unerwarteter Fehler ist aufgetreten.

#### WEBVIEW2_WEB_RESOURCE_CONTEXT 

Enum für Webressourcen-anforderungskontexte.

> Enum- [WEBVIEW2_WEB_RESOURCE_CONTEXT](#webview2_web_resource_context)

 Werte                         | Beschreibungen
--------------------------------|---------------------------------------------
WEBVIEW2_WEB_RESOURCE_CONTEXT_ALL            | Alle Ressourcen.
WEBVIEW2_WEB_RESOURCE_CONTEXT_DOCUMENT            | Dokument Ressourcen.
WEBVIEW2_WEB_RESOURCE_CONTEXT_STYLESHEET            | CSS-Ressourcen.
WEBVIEW2_WEB_RESOURCE_CONTEXT_IMAGE            | Bildressourcen.
WEBVIEW2_WEB_RESOURCE_CONTEXT_MEDIA            | Andere Medienressourcen wie Videos.
WEBVIEW2_WEB_RESOURCE_CONTEXT_FONT            | Schriftartressourcen.
WEBVIEW2_WEB_RESOURCE_CONTEXT_SCRIPT            | Skriptressourcen.
WEBVIEW2_WEB_RESOURCE_CONTEXT_XML_HTTP_REQUEST            | XML-HTTP-Anforderungen.
WEBVIEW2_WEB_RESOURCE_CONTEXT_FETCH            | Abrufen der API-Kommunikation.
WEBVIEW2_WEB_RESOURCE_CONTEXT_TEXT_TRACK            | Texttracking-Ressourcen.
WEBVIEW2_WEB_RESOURCE_CONTEXT_EVENT_SOURCE            | 
WEBVIEW2_WEB_RESOURCE_CONTEXT_WEBSOCKET            | 
WEBVIEW2_WEB_RESOURCE_CONTEXT_MANIFEST            | 
WEBVIEW2_WEB_RESOURCE_CONTEXT_SIGNED_EXCHANGE            | 
WEBVIEW2_WEB_RESOURCE_CONTEXT_PING            | 
WEBVIEW2_WEB_RESOURCE_CONTEXT_CSP_VIOLATION_REPORT            | 
WEBVIEW2_WEB_RESOURCE_CONTEXT_OTHER            | Andere Ressourcen.
