---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Host, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: 6fce29c2df69abc8d55d91c267b282702e567453
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/15/2020
ms.locfileid: "10881207"
---
# 0.9.430-Interface-ICoreWebView2 

> [!NOTE]
> Diese Schnittstelle kann nach der SDK-Version 0.9.430 geändert oder für Versionen nicht verfügbar sein. Die neueste API-Referenz finden Sie unter [Referenz](../../../webview2-api-reference.md) .

```
interface ICoreWebView2
  : public IUnknown
```

WebView2 ermöglicht Ihnen das Hosten von Webinhalten mithilfe der neuesten Edge-Webbrowser Technologie.

## Zusammenfassung

 Member                        | Beschreibungen
--------------------------------|---------------------------------------------
[get_Settings](#get_settings) | Das ICoreWebView2Settings-Objekt enthält verschiedene änderbare Einstellungen für den ausgeführten WebView.
[get_Source](#get_source) | Der URI des aktuellen Dokuments auf oberster Ebene.
[%%amp;quot;Navigate%%amp;quot;
](#navigate) | Führen Sie eine Navigation des Dokuments auf oberster Ebene zum angegebenen URI.
[NavigateToString](#navigatetostring) | Initiiert eine Navigation zu htmlContent als HTML-Code für ein neues Dokument.
[add_NavigationStarting](#add_navigationstarting) | Fügen Sie einen Ereignishandler für das NavigationStarting-Ereignis hinzu.
[remove_NavigationStarting](#remove_navigationstarting) | Entfernen Sie einen Ereignishandler, der zuvor mit add_NavigationStarting hinzugefügt wurde.
[add_ContentLoading](#add_contentloading) | Fügen Sie einen Ereignishandler für das ContentLoading-Ereignis hinzu.
[remove_ContentLoading](#remove_contentloading) | Entfernen Sie einen Ereignishandler, der zuvor mit add_ContentLoading hinzugefügt wurde.
[add_SourceChanged](#add_sourcechanged) | Die Quelle wird ausgelöst, wenn die Quelleigenschaft geändert wird.
[remove_SourceChanged](#remove_sourcechanged) | Entfernen Sie einen Ereignishandler, der zuvor mit add_SourceChanged hinzugefügt wurde.
[add_HistoryChanged](#add_historychanged) | Abrechnungshistorieändern hören Sie sich die Änderung des Navigationsverlaufs für das Dokument der obersten Ebene an.
[remove_HistoryChanged](#remove_historychanged) | Entfernen Sie einen Ereignishandler, der zuvor mit add_HistoryChanged hinzugefügt wurde.
[add_NavigationCompleted](#add_navigationcompleted) | Fügen Sie einen Ereignishandler für das NavigationCompleted-Ereignis hinzu.
[remove_NavigationCompleted](#remove_navigationcompleted) | Entfernen Sie einen Ereignishandler, der zuvor mit add_NavigationCompleted hinzugefügt wurde.
[add_FrameNavigationStarting](#add_framenavigationstarting) | Fügen Sie einen Ereignishandler für das FrameNavigationStarting-Ereignis hinzu.
[remove_FrameNavigationStarting](#remove_framenavigationstarting) | Entfernen Sie einen Ereignishandler, der zuvor mit add_FrameNavigationStarting hinzugefügt wurde.
[add_ScriptDialogOpening](#add_scriptdialogopening) | Fügen Sie einen Ereignishandler für das ScriptDialogOpening-Ereignis hinzu.
[remove_ScriptDialogOpening](#remove_scriptdialogopening) | Entfernen Sie einen Ereignishandler, der zuvor mit add_ScriptDialogOpening hinzugefügt wurde.
[add_PermissionRequested](#add_permissionrequested) | Fügen Sie einen Ereignishandler für das PermissionRequested-Ereignis hinzu.
[remove_PermissionRequested](#remove_permissionrequested) | Entfernen Sie einen Ereignishandler, der zuvor mit add_PermissionRequested hinzugefügt wurde.
[add_ProcessFailed](#add_processfailed) | Fügen Sie einen Ereignishandler für das ProcessFailed-Ereignis hinzu.
[remove_ProcessFailed](#remove_processfailed) | Entfernen Sie einen Ereignishandler, der zuvor mit add_ProcessFailed hinzugefügt wurde.
[AddScriptToExecuteOnDocumentCreated](#addscripttoexecuteondocumentcreated) | Fügen Sie das bereitgestellte JavaScript einer Liste von Skripts hinzu, die ausgeführt werden sollen, nachdem das globale Objekt erstellt wurde, aber bevor das HTML-Dokument analysiert wurde und bevor ein anderes Skript ausgeführt wird, das vom HTML-Dokument eingeschlossen ist.
[RemoveScriptToExecuteOnDocumentCreated](#removescripttoexecuteondocumentcreated) | Entfernen Sie das entsprechende JavaScript, das über AddScriptToExecuteOnDocumentCreated hinzugefügt wurde.
[ExecuteScript](#executescript) | Führen Sie JavaScript-Code aus dem JavaScript-Parameter im aktuellen Dokument der obersten Ebene aus, das in der WebView gerendert wird.
[CapturePreview](#capturepreview) | Erfassen Sie ein Bild von der Anzeige von WebView.
[Laden](#reload) | Laden Sie die aktuelle Seite neu.
[PostWebMessageAsJson](#postwebmessageasjson) | Posten Sie die angegebene Webnachricht im Dokument der obersten Ebene in dieser WebView.
[PostWebMessageAsString](#postwebmessageasstring) | Dies ist ein Helfer zum Posten einer Nachricht, bei der es sich um eine einfache Zeichenfolge und nicht um eine JSON-Zeichenfolgendarstellung eines JavaScript-Objekts handelt.
[add_WebMessageReceived](#add_webmessagereceived) | Dieses Ereignis wird ausgelöst, wenn die IsWebMessageEnabled-Einstellung festgelegt ist, und das Dokument auf oberster Ebene des WebView-Anrufs `window.chrome.webview.postMessage` .
[remove_WebMessageReceived](#remove_webmessagereceived) | Entfernen Sie einen Ereignishandler, der zuvor mit add_WebMessageReceived hinzugefügt wurde.
[CallDevToolsProtocolMethod](#calldevtoolsprotocolmethod) | Rufen Sie eine asynchrone DevToolsProtocol-Methode auf.
[get_BrowserProcessId](#get_browserprocessid) | Die Prozess-ID des Browser Prozesses, der die WebView hostet.
[get_CanGoBack](#get_cangoback) | Gibt "true" zurück, wenn die WebView zu einer vorherigen Seite im Navigationsverlauf navigieren kann.
[get_CanGoForward](#get_cangoforward) | Gibt "true" zurück, wenn die WebView zu einer nächsten Seite im Navigationsverlauf navigieren kann.
[GoBack](#goback) | Navigiert die WebView zur vorherigen Seite im Navigationsverlauf.
[GoForward](#goforward) | Navigiert die WebView zur nächsten Seite im Navigationsverlauf.
[GetDevToolsProtocolEventReceiver](#getdevtoolsprotocoleventreceiver) | Rufen Sie einen devtools-Protokollereignis Empfänger ab, mit dem Sie ein devtools-Protokollereignis abonnieren können.
[Stop](#stop) | Beenden Sie alle Navigations-und ausstehenden Ressourcen Abrufe.
[add_NewWindowRequested](#add_newwindowrequested) | Fügen Sie einen Ereignishandler für das mswebviewnewwindowrequested-Ereignis hinzu.
[remove_NewWindowRequested](#remove_newwindowrequested) | Entfernen Sie einen Ereignishandler, der zuvor mit add_NewWindowRequested hinzugefügt wurde.
[add_DocumentTitleChanged](#add_documenttitlechanged) | Fügen Sie einen Ereignishandler für das DocumentTitleChanged-Ereignis hinzu.
[remove_DocumentTitleChanged](#remove_documenttitlechanged) | Entfernen Sie einen Ereignishandler, der zuvor mit add_DocumentTitleChanged hinzugefügt wurde.
[get_DocumentTitle](#get_documenttitle) | Der Titel für das aktuelle Dokument der obersten Ebene.
[Addremoteobject](#addremoteobject) | Fügen Sie das bereitgestellte Hostobjekt zu Skript hinzu, das in der WebView mit dem angegebenen Namen ausgeführt wird.
[RemoveRemoteObject](#removeremoteobject) | Entfernen Sie das vom Namen angegebene Hostobjekt, damit es nicht mehr über JavaScript-Code in der WebView zugänglich ist.
[OpenDevToolsWindow](#opendevtoolswindow) | Öffnet das devtools-Fenster für das aktuelle Dokument in der WebView.
[add_ContainsFullScreenElementChanged](#add_containsfullscreenelementchanged) | Benachrichtigt, wenn sich die ContainsFullScreenElement-Eigenschaft ändert.
[remove_ContainsFullScreenElementChanged](#remove_containsfullscreenelementchanged) | Entfernen Sie einen Ereignishandler, der zuvor mit der entsprechenden add_-Ereignismethode hinzugefügt wurde.
[get_ContainsFullScreenElement](#get_containsfullscreenelement) | Gibt an, ob die WebView ein HTML-Vollbild-Element enthält.
[add_WebResourceRequested](#add_webresourcerequested) | Fügen Sie einen Ereignishandler für das WebResourceRequested-Ereignis hinzu.
[remove_WebResourceRequested](#remove_webresourcerequested) | Entfernen Sie einen Ereignishandler, der zuvor mit add_WebResourceRequested hinzugefügt wurde.
[AddWebResourceRequestedFilter](#addwebresourcerequestedfilter) | Fügt dem WebResourceRequested-Ereignis einen URI-und Ressourcenkontext Filter hinzu.
[RemoveWebResourceRequestedFilter](#removewebresourcerequestedfilter) | Entfernt einen übereinstimmenden Webressourcen Filter, der zuvor für das WebResourceRequested-Ereignis hinzugefügt wurde.
[add_WindowCloseRequested](#add_windowcloserequested) | Fügen Sie einen Ereignishandler für das WindowCloseRequested-Ereignis hinzu.
[remove_WindowCloseRequested](#remove_windowcloserequested) | Entfernen Sie einen Ereignishandler, der zuvor mit add_WindowCloseRequested hinzugefügt wurde.
[CORE_WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT](#core_webview2_capture_preview_image_format) | Bildformat, das von der ICoreWebView2:: CapturePreview-Methode verwendet wird.
[CORE_WEBVIEW2_SCRIPT_DIALOG_KIND](#core_webview2_script_dialog_kind) | Art des in der ICoreWebView2ScriptDialogOpeningEventHandler-Schnittstelle verwendeten JavaScript-Dialogfelds.
[CORE_WEBVIEW2_PROCESS_FAILED_KIND](#core_webview2_process_failed_kind) | Art des in der ICoreWebView2ProcessFailedEventHandler-Schnittstelle verwendeten Prozess Fehlers.
[CORE_WEBVIEW2_PERMISSION_KIND](#core_webview2_permission_kind) | Der Typ einer Berechtigungsanforderung.
[CORE_WEBVIEW2_PERMISSION_STATE](#core_webview2_permission_state) | Antwort auf eine Berechtigungsanforderung.
[CORE_WEBVIEW2_WEB_ERROR_STATUS](#core_webview2_web_error_status) | Fehlerstatus Werte für Web-Navigationselemente.
[CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT](#core_webview2_web_resource_context) | Enum für Webressourcen-anforderungskontexte.

## Navigationsereignisse

Die normale Abfolge von Navigations Ereignissen lautet NavigationStarting, sourced, ContentLoading und dann NavigationCompleted.

![dot-inline-dotgraph-1.png](media/dot-inline-dotgraph-1.png)

Beachten Sie, dass dies für Navigationsereignisse mit dem gleichen Navigations-Event-arg gilt. Navigationsereignisse mit unterschiedlichen Navigations-Event-args können sich überlappen. Wenn Sie beispielsweise eine Navigation auf das NavigationStarting-Ereignis warten und dann eine andere Navigation starten, sehen Sie die NavigationStarting für die erste Navigation, gefolgt von der NavigationStarting der zweiten Navigation, gefolgt von der NavigationCompleted für die erste Navigation und dann allen anderen geeigneten Navigations Ereignissen für die zweite Navigation. In Fehlerfällen kann es sich um ein ContentLoading-Ereignis handeln, das davon abhängt, ob die Navigation auf einer Fehlerseite fortgesetzt wird. Im Fall einer HTTP-Umleitung gibt es mehrere NavigationStarting-Ereignisse in einer Zeile, wobei für diejenigen, die dem ersten Folgen, das isredirect-Flag festzulegen ist.

Verwenden Sie FrameNavigationStarting, um die Navigation innerhalb von unter Frames in der WebView zu überwachen oder abzubrechen.

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

Öffnen Sie devtools mit den normalen Tastenkombinationen: `F12` oder `Ctrl+Shift+I` . Sie können die `--auto-open-devtools-for-tabs` Befehlsargument Schalter verwenden, um das devtools-Fenster sofort zu öffnen, wenn Sie das erste Mal eine WebView erstellen. Informationen zum Bereitstellen zusätzlicher Befehlszeilenargumente für den Browserprozess finden Sie in der CreateCoreWebView2Host-Dokumentation. Schauen Sie sich den LoaderOverride-Registrierungsschlüssel an, um verschiedene Builds von WebView2 zu testen, ohne die Anwendung in der CreateCoreWebView2Host-Dokumentation zu ändern.

## Versionsverwaltung

Nachdem Sie eine bestimmte Version des SDK zum Erstellen Ihrer APP verwendet haben, wird Ihre APP möglicherweise mit einer älteren oder neueren Version der installierten Browser-Binärdateien ausgeführt. Bis Version 1.0.0.0 von WebView2 können sich während der Updates Änderungen ändern, die verhindern, dass Ihr SDK mit unterschiedlichen Versionen der installierten Browser-Binärdateien funktioniert. Nach der Version 1.0.0.0 können verschiedene Versionen des SDKs mit unterschiedlichen Versionen des installierten Browsers funktionieren, indem Sie die folgenden bewährten Methoden verwenden:

Wenn Sie Änderungen an der API berücksichtigen möchten, müssen Sie sicherstellen, dass Sie beim Aufrufen der DLL-Export CreateCoreWebView2Environment und beim Aufrufen von QueryInterface für ein beliebiges CoreWebView2-Objekt auf Fehler überprüfen. Ein Rückgabewert von E_NOINTERFACE kann darauf hindeuten, dass das SDK nicht mit den Binärdateien des Edge-Browsers kompatibel ist.

Das Überprüfen auf Fehler von QueryInterface berücksichtigt auch Fälle, in denen das SDK neuer als die Version des Edge-Browsers ist und Ihre APP versucht, eine Schnittstelle zu verwenden, von der der Edge-Browser nichts weiß.

Wenn eine Schnittstelle nicht zur Verfügung steht, können Sie das zugeordnete Feature nach Möglichkeit deaktivieren oder den Endbenutzer anderweitig darüber informieren, dass Sie den Browser aktualisieren müssen.

## Member

#### get_Settings 

Das ICoreWebView2Settings-Objekt enthält verschiedene änderbare Einstellungen für den ausgeführten WebView.

> öffentliche HRESULT- [get_Settings](#get_settings)(ICoreWebView2Settings * *-Einstellungen)

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
                SetWindowText(m_toolbar->addressBarWindow, uri.get());

                return S_OK;
            })
            .Get(),
        &m_sourceChangedToken));
```

#### %%amp;quot;Navigate%%amp;quot;
 

Führen Sie eine Navigation des Dokuments auf oberster Ebene zum angegebenen URI.

> öffentliche HRESULT- [Navigation](#navigate)(LPCWSTR-URI)

Weitere Informationen finden Sie in den Navigations Ereignissen. Beachten Sie, dass dadurch eine Navigation gestartet wird und das entsprechende NavigationStarting-Ereignis irgendwann ausgelöst wird, nachdem dieser Navigate-Aufruf abgeschlossen ist.

```cpp
void ControlComponent::NavigateToAddressBar()
{
    int length = GetWindowTextLength(m_toolbar->addressBarWindow);
    std::wstring uri(length, 0);
    PWSTR buffer = const_cast<PWSTR>(uri.data());
    GetWindowText(m_toolbar->addressBarWindow, buffer, length + 1);

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

#### add_NavigationStarting 

Fügen Sie einen Ereignishandler für das NavigationStarting-Ereignis hinzu.

> Public HRESULT [add_NavigationStarting](#add_navigationstarting)([ICoreWebView2NavigationStartingEventHandler](ICoreWebView2NavigationStartingEventHandler.md) * EventHandler, EventRegistrationToken * Token)

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

#### remove_NavigationStarting 

Entfernen Sie einen Ereignishandler, der zuvor mit add_NavigationStarting hinzugefügt wurde.

> Public HRESULT [remove_NavigationStarting](#remove_navigationstarting)(EventRegistrationToken-Token)

#### add_ContentLoading 

Fügen Sie einen Ereignishandler für das ContentLoading-Ereignis hinzu.

> Public HRESULT [add_ContentLoading](#add_contentloading)([ICoreWebView2ContentLoadingEventHandler](ICoreWebView2ContentLoadingEventHandler.md) * EventHandler, EventRegistrationToken * Token)

ContentLoading wird ausgelöst, bevor Inhalte geladen werden, einschließlich Skripten, die mit AddScriptToExecuteOnDocumentCreated hinzugefügt wurden ContentLoading werden nicht ausgelöst, wenn dieselbe Seitennavigation erfolgt (beispielsweisedurch Fragment-Navigation oder History. pushState-Navigation). Dies folgt auf das NavigationStarting-Ereignis und das Source-Ereignis und steht vor den Ereignissen "History" und "NavigationCompleted".

#### remove_ContentLoading 

Entfernen Sie einen Ereignishandler, der zuvor mit add_ContentLoading hinzugefügt wurde.

> Public HRESULT [remove_ContentLoading](#remove_contentloading)(EventRegistrationToken-Token)

#### add_SourceChanged 

Die Quelle wird ausgelöst, wenn die Quelleigenschaft geändert wird.

> Public HRESULT [add_SourceChanged](#add_sourcechanged)([ICoreWebView2SourceChangedEventHandler](ICoreWebView2SourceChangedEventHandler.md) * EventHandler, EventRegistrationToken * Token)

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
                SetWindowText(m_toolbar->addressBarWindow, uri.get());

                return S_OK;
            })
            .Get(),
        &m_sourceChangedToken));
```

#### remove_SourceChanged 

Entfernen Sie einen Ereignishandler, der zuvor mit add_SourceChanged hinzugefügt wurde.

> Public HRESULT [remove_SourceChanged](#remove_sourcechanged)(EventRegistrationToken-Token)

#### add_HistoryChanged 

Abrechnungshistorieändern hören Sie sich die Änderung des Navigationsverlaufs für das Dokument der obersten Ebene an.

> Public HRESULT [add_HistoryChanged](#add_historychanged)([ICoreWebView2HistoryChangedEventHandler](ICoreWebView2HistoryChangedEventHandler.md) * EventHandler, EventRegistrationToken * Token)

Verwenden Sie abrechnungshistorieändern, um zu überprüfen, ob sich get_CanGoBack/get_CanGoForward Wert geändert hat. "History" wird auch für die Verwendung von GoBack/GoForward ausgelöst. "History" wird nach "sourcely" und "ContentLoading" ausgelöst. Fügen Sie einen Ereignishandler für das History-Ereignis hinzu. 

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
                EnableWindow(m_toolbar->backWindow, canGoBack);
                EnableWindow(m_toolbar->forwardWindow, canGoForward);

                return S_OK;
            })
            .Get(),
        &m_historyChangedToken));
```

#### remove_HistoryChanged 

Entfernen Sie einen Ereignishandler, der zuvor mit add_HistoryChanged hinzugefügt wurde.

> Public HRESULT [remove_HistoryChanged](#remove_historychanged)(EventRegistrationToken-Token)

#### add_NavigationCompleted 

Fügen Sie einen Ereignishandler für das NavigationCompleted-Ereignis hinzu.

> Public HRESULT [add_NavigationCompleted](#add_navigationcompleted)([ICoreWebView2NavigationCompletedEventHandler](ICoreWebView2NavigationCompletedEventHandler.md) * EventHandler, EventRegistrationToken * Token)

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
                    CORE_WEBVIEW2_WEB_ERROR_STATUS webErrorStatus;
                    CHECK_FAILURE(args->get_WebErrorStatus(&webErrorStatus));
                    if (webErrorStatus == CORE_WEBVIEW2_WEB_ERROR_STATUS_DISCONNECTED)
                    {
                        // Do something here if you want to handle a specific error case.
                        // In most cases this isn't necessary, because the WebView will
                        // display its own error page automatically.
                    }
                }
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

> Public HRESULT [add_FrameNavigationStarting](#add_framenavigationstarting)([ICoreWebView2NavigationStartingEventHandler](ICoreWebView2NavigationStartingEventHandler.md) * EventHandler, EventRegistrationToken * Token)

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

#### remove_FrameNavigationStarting 

Entfernen Sie einen Ereignishandler, der zuvor mit add_FrameNavigationStarting hinzugefügt wurde.

> Public HRESULT [remove_FrameNavigationStarting](#remove_framenavigationstarting)(EventRegistrationToken-Token)

#### add_ScriptDialogOpening 

Fügen Sie einen Ereignishandler für das ScriptDialogOpening-Ereignis hinzu.

> Public HRESULT [add_ScriptDialogOpening](#add_scriptdialogopening)([ICoreWebView2ScriptDialogOpeningEventHandler](ICoreWebView2ScriptDialogOpeningEventHandler.md) * EventHandler, EventRegistrationToken * Token)

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
            CORE_WEBVIEW2_SCRIPT_DIALOG_KIND type;
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
                /* readonly */ type != CORE_WEBVIEW2_SCRIPT_DIALOG_KIND_PROMPT);
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

#### remove_ScriptDialogOpening 

Entfernen Sie einen Ereignishandler, der zuvor mit add_ScriptDialogOpening hinzugefügt wurde.

> Public HRESULT [remove_ScriptDialogOpening](#remove_scriptdialogopening)(EventRegistrationToken-Token)

#### add_PermissionRequested 

Fügen Sie einen Ereignishandler für das PermissionRequested-Ereignis hinzu.

> Public HRESULT [add_PermissionRequested](#add_permissionrequested)([ICoreWebView2PermissionRequestedEventHandler](ICoreWebView2PermissionRequestedEventHandler.md) * EventHandler, EventRegistrationToken * Token)

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
        CORE_WEBVIEW2_PERMISSION_KIND kind = CORE_WEBVIEW2_PERMISSION_KIND_UNKNOWN_PERMISSION;
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

        CORE_WEBVIEW2_PERMISSION_STATE state =
              response == IDYES ? CORE_WEBVIEW2_PERMISSION_STATE_ALLOW
            : response == IDNO  ? CORE_WEBVIEW2_PERMISSION_STATE_DENY
            :                     CORE_WEBVIEW2_PERMISSION_STATE_DEFAULT;
        CHECK_FAILURE(args->put_State(state));

        return S_OK;
    }).Get(), &m_permissionRequestedToken));
```

#### remove_PermissionRequested 

Entfernen Sie einen Ereignishandler, der zuvor mit add_PermissionRequested hinzugefügt wurde.

> Public HRESULT [remove_PermissionRequested](#remove_permissionrequested)(EventRegistrationToken-Token)

#### add_ProcessFailed 

Fügen Sie einen Ereignishandler für das ProcessFailed-Ereignis hinzu.

> Public HRESULT [add_ProcessFailed](#add_processfailed)([ICoreWebView2ProcessFailedEventHandler](ICoreWebView2ProcessFailedEventHandler.md) * EventHandler, EventRegistrationToken * Token)

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
        CORE_WEBVIEW2_PROCESS_FAILED_KIND failureType;
        CHECK_FAILURE(args->get_ProcessFailedKind(&failureType));
        if (failureType == CORE_WEBVIEW2_PROCESS_FAILED_KIND_BROWSER_PROCESS_EXITED)
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
        else if (failureType == CORE_WEBVIEW2_PROCESS_FAILED_KIND_RENDER_PROCESS_UNRESPONSIVE)
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
        return S_OK;
    }).Get(), &m_processFailedToken));
```

#### remove_ProcessFailed 

Entfernen Sie einen Ereignishandler, der zuvor mit add_ProcessFailed hinzugefügt wurde.

> Public HRESULT [remove_ProcessFailed](#remove_processfailed)(EventRegistrationToken-Token)

#### AddScriptToExecuteOnDocumentCreated 

Fügen Sie das bereitgestellte JavaScript einer Liste von Skripts hinzu, die ausgeführt werden sollen, nachdem das globale Objekt erstellt wurde, aber bevor das HTML-Dokument analysiert wurde und bevor ein anderes Skript ausgeführt wird, das vom HTML-Dokument eingeschlossen ist.

> Public HRESULT [AddScriptToExecuteOnDocumentCreated](#addscripttoexecuteondocumentcreated)(LPCWSTR javaScript,[ICoreWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler](ICoreWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler.md) * Handler)

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

#### RemoveScriptToExecuteOnDocumentCreated 

Entfernen Sie das entsprechende JavaScript, das über AddScriptToExecuteOnDocumentCreated hinzugefügt wurde.

> Public HRESULT [RemoveScriptToExecuteOnDocumentCreated](#removescripttoexecuteondocumentcreated)(LPCWSTR-ID)

#### ExecuteScript 

Führen Sie JavaScript-Code aus dem JavaScript-Parameter im aktuellen Dokument der obersten Ebene aus, das in der WebView gerendert wird.

> Public HRESULT [executeScript](#executescript)(LPCWSTR javaScript,[ICoreWebView2ExecuteScriptCompletedHandler](ICoreWebView2ExecuteScriptCompletedHandler.md) * Handler)

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

#### CapturePreview 

Erfassen Sie ein Bild von der Anzeige von WebView.

> Public HRESULT [CapturePreview](#capturepreview)([CORE_WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT](#core_webview2_capture_preview_image_format) Image Format, IStream * ImageStream,[ICoreWebView2CapturePreviewCompletedHandler](ICoreWebView2CapturePreviewCompletedHandler.md) *-Handler)

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
            CORE_WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT_PNG, stream.get(),
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

#### Laden 

Laden Sie die aktuelle Seite neu.

> Public HRESULT [Reload](#reload)()

Dies ähnelt der Navigation zum URI des aktuellen Dokuments auf oberster Ebene, einschließlich aller Navigationsereignisse, die alle Einträge im HTTP-Cache auslösen und respektieren. Das zurück/weiter-Protokoll wird jedoch nicht geändert.

#### PostWebMessageAsJson 

Posten Sie die angegebene Webnachricht im Dokument der obersten Ebene in dieser WebView.

> Public HRESULT [PostWebMessageAsJson](#postwebmessageasjson)(LPCWSTR webMessageAsJson)

Das Nachrichtenereignis des Fensters "Window. Chrome. WebView" des obersten Dokuments wird ausgelöst. JavaScript in diesem Dokument kann das Ereignis über Folgendes abonnieren und kündigen: 

```cpp
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

#### add_WebMessageReceived 

Dieses Ereignis wird ausgelöst, wenn die IsWebMessageEnabled-Einstellung festgelegt ist, und das Dokument auf oberster Ebene des WebView-Anrufs `window.chrome.webview.postMessage` .

> öffentliche HRESULT- [add_WebMessageReceived](#add_webmessagereceived)([ICoreWebView2WebMessageReceivedEventHandler](ICoreWebView2WebMessageReceivedEventHandler.md) *-Handler, EventRegistrationToken *-Token)

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

 Wenn PostMessage aufgerufen wird, wird der [ICoreWebView2WebMessageReceivedEventHandler](ICoreWebView2WebMessageReceivedEventHandler.md) -Satz über diese SetWebMessageReceivedEventHandler-Methode aufgerufen, wobei der Objektparameter der PostMessage in eine JSON-Zeichenfolge konvertiert wird.

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

#### remove_WebMessageReceived 

Entfernen Sie einen Ereignishandler, der zuvor mit add_WebMessageReceived hinzugefügt wurde.

> Public HRESULT [remove_WebMessageReceived](#remove_webmessagereceived)(EventRegistrationToken-Token)

#### CallDevToolsProtocolMethod 

Rufen Sie eine asynchrone DevToolsProtocol-Methode auf.

> Public HRESULT [CallDevToolsProtocolMethod](#calldevtoolsprotocolmethod)(LPCWSTR MethodName, LPCWSTR parametersAsJson,[ICoreWebView2CallDevToolsProtocolMethodCompletedHandler](ICoreWebView2CallDevToolsProtocolMethodCompletedHandler.md) * Handler)

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

#### get_BrowserProcessId 

Die Prozess-ID des Browser Prozesses, der die WebView hostet.

> Public HRESULT [get_BrowserProcessId](#get_browserprocessid)(UInt32 *-Wert)

#### get_CanGoBack 

Gibt "true" zurück, wenn die WebView zu einer vorherigen Seite im Navigationsverlauf navigieren kann.

> Public HRESULT [get_CanGoBack](#get_cangoback)(bool * CanGoBack)

Das History-Ereignis wird ausgelöst, wenn der Wert von get_CanGoBack geändert wird.

#### get_CanGoForward 

Gibt "true" zurück, wenn die WebView zu einer nächsten Seite im Navigationsverlauf navigieren kann.

> Public HRESULT [get_CanGoForward](#get_cangoforward)(bool * CanGoForward)

Das History-Ereignis wird ausgelöst, wenn der Wert von get_CanGoForward geändert wird.

#### GoBack 

Navigiert die WebView zur vorherigen Seite im Navigationsverlauf.

> Public HRESULT [GoBack](#goback)()

#### GoForward 

Navigiert die WebView zur nächsten Seite im Navigationsverlauf.

> Public HRESULT [GoForward](#goforward)()

#### GetDevToolsProtocolEventReceiver 

Rufen Sie einen devtools-Protokollereignis Empfänger ab, mit dem Sie ein devtools-Protokollereignis abonnieren können.

> Public HRESULT [GetDevToolsProtocolEventReceiver](#getdevtoolsprotocoleventreceiver)(LPCWSTR EventName,[ICoreWebView2DevToolsProtocolEventReceiver](ICoreWebView2DevToolsProtocolEventReceiver.md) * * Receiver)

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

#### Stop 

Beenden Sie alle Navigations-und ausstehenden Ressourcen Abrufe.

> öffentlicher HRESULT- [Stopp](#stop)()

Skripts werden nicht angehalten.

#### add_NewWindowRequested 

Fügen Sie einen Ereignishandler für das mswebviewnewwindowrequested-Ereignis hinzu.

> Public HRESULT [add_NewWindowRequested](#add_newwindowrequested)([ICoreWebView2NewWindowRequestedEventHandler](ICoreWebView2NewWindowRequestedEventHandler.md) * EventHandler, EventRegistrationToken * Token)

Wird ausgelöst, wenn der Inhalt in der WebView zum Öffnen eines neuen Fensters angefordert wird, beispielsweisedurch Window. Open. Die APP kann eine Ziel-WebView übergeben, die als das geöffnete Fenster angesehen wird.

```cpp
    // Register a handler for the NewWindowRequested event.
    // This handler will defer the event, create a new app window, and then once the
    // new window is ready, it'll provide that new window's WebView as the response to
    // the request.
    CHECK_FAILURE(m_webView->add_NewWindowRequested(
        Callback<ICoreWebView2NewWindowRequestedEventHandler>(
            [this](
                ICoreWebView2* sender,
                ICoreWebView2NewWindowRequestedEventArgs* args) {
                wil::com_ptr<ICoreWebView2Deferral> deferral;
                CHECK_FAILURE(args->GetDeferral(&deferral));

                auto newAppWindow = new AppWindow(L"");
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

#### remove_NewWindowRequested 

Entfernen Sie einen Ereignishandler, der zuvor mit add_NewWindowRequested hinzugefügt wurde.

> Public HRESULT [remove_NewWindowRequested](#remove_newwindowrequested)(EventRegistrationToken-Token)

#### add_DocumentTitleChanged 

Fügen Sie einen Ereignishandler für das DocumentTitleChanged-Ereignis hinzu.

> Public HRESULT [add_DocumentTitleChanged](#add_documenttitlechanged)([ICoreWebView2DocumentTitleChangedEventHandler](ICoreWebView2DocumentTitleChangedEventHandler.md) * EventHandler, EventRegistrationToken * Token)

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

#### remove_DocumentTitleChanged 

Entfernen Sie einen Ereignishandler, der zuvor mit add_DocumentTitleChanged hinzugefügt wurde.

> Public HRESULT [remove_DocumentTitleChanged](#remove_documenttitlechanged)(EventRegistrationToken-Token)

#### get_DocumentTitle 

Der Titel für das aktuelle Dokument der obersten Ebene.

> öffentliche HRESULT- [get_DocumentTitle](#get_documenttitle)(LPWSTR * Title)

Wenn das Dokument keinen expliziten Titel hat oder sonst leer ist, wird ein Standardwert verwendet, der möglicherweise nicht mit dem URI des Dokuments übereinstimmt.

#### Addremoteobject 

Fügen Sie das bereitgestellte Hostobjekt zu Skript hinzu, das in der WebView mit dem angegebenen Namen ausgeführt wird.

> Public HRESULT [addremoteobject](#addremoteobject)(LPCWSTR-Name, Variant *-Objekt)

Host Objekte werden als Remoteobjekt Proxys über bereitgestellt `window.chrome.webview.remoteObjects.<name>` . Remote Objektproxys sind Versprechungen und werden in ein Objekt aufgelöst, das das Hostobjekt darstellt. Das Versprechen wird abgelehnt, wenn die APP kein Objekt mit dem Namen hinzugefügt hat. Wenn JavaScript-Code auf eine Eigenschaft oder Methode des Objekts zugreift, wird eine Zusage zurückgegeben, die in den Wert aufgelöst wird, der vom Host für die Eigenschaft oder Methode zurückgegeben wird, oder im Fall eines Fehlers abgelehnt wird, beispielsweise wenn keine solche Eigenschaft oder Methode für das Objekt vorhanden ist oder Parameter ungültig sind. Wenn der Anwendungscode beispielsweise Folgendes durchführt: 

```cpp
VARIANT object;
object.vt = VT_DISPATCH;
object.pdispVal = appObject;
webview->AddRemoteObject(L"host_object", &host);
```

 JavaScript-Code in der WebView kann auf appObject wie folgt zugreifen und dann auf Attribute und Methoden von appObject zugreifen: 

```js
let app_object = await window.chrome.webview.remoteObjects.host_object;
let attr1 = await app_object.attr1;
let result = await app_object.method1(parameters);
```

 Beachten Sie, dass einfache Typen, IDispatch und Array unterstützt werden, generische IUnknown, VT_DECIMAL oder VT_RECORD Variant nicht unterstützt werden. Remote-JavaScript-Objekte wie Rückruffunktionen werden als VT_DISPATCH Variante mit dem Object-Implementierungs-IDispatch dargestellt. Die JavaScript-Rückrufmethode kann mit DISPID_VALUE für die DISPID aufgerufen werden. Geschachtelte Arrays werden bis zu einer Tiefe von 3 unterstützt. Arrays von nach Verweistypen werden nicht unterstützt. VT_EMPTY und VT_NULL werden JavaScript als NULL zugeordnet. In JavaScript werden NULL und undefined VT_EMPTY zugeordnet.

Darüber hinaus werden alle Remoteobjekte als verfügbar gemacht `window.chrome.webview.remoteObjects.sync.<name>` . Hier werden die Hostobjekte als synchrone Remoteobjekt Proxys verfügbar gemacht. Hierbei handelt es sich nicht um Versprechungen und Aufrufe von Funktionen oder des Eigenschafts Zugriffs, die ein synchrones Blockieren des ausgeführten Skripts warten, um die Ausführung des Host Codes zu kommunizieren. Dementsprechend kann dies zu Zuverlässigkeitsproblemen führen, und es wird empfohlen, dass Sie die oben beschriebene Versprechen-basierte asynchrone `window.chrome.webview.remoteObjects.<name>` API verwenden.

Synchrone Remoteobjekt Proxys und asynchrone Remoteobjekt Proxys können sowohl Proxys für dasselbe Remoteobjekt als auch Proxys sein. Remote Änderungen, die von einem Proxy durchgeführt werden, werden in jedem anderen Proxy desselben Remoteobjekts widergespiegelt, unabhängig davon, ob die anderen Proxys synchron oder asynchron sind.

Während JavaScript bei einem synchronen Aufruf von systemeigenem Code blockiert wird, kann dieser systemeigene Code nicht mehr in JavaScript zurückrufen. Der Versuch, dies zu tun, schlägt mit HRESULT_FROM_WIN32 (ERROR_POSSIBLE_DEADLOCK) fehl.

Remote Objektproxys sind JavaScript-Proxy Objekte, die alle Eigenschaften abrufen, Eigenschaftensätze und Methodenaufrufe abfangen. Eigenschaften oder Methoden, die Teil des Funktions-oder Objekt Prototyps sind, werden lokal ausgeführt. Darüber hinaus werden alle Eigenschaften oder Methoden im Array `chrome.webview.remoteObjects.options.forceLocalProperties` lokal ausgeführt. Diese Option enthält standardmäßig optionale Methoden, die in JavaScript wie und in Bedeutung sind `toJSON` `Symbol.toPrimitive` . Sie können diesem Array nach Bedarf weitere hinzufügen.

Es gibt eine Methode `chrome.webview.remoteObjects.cleanupSome` , mit der die Garbage Collection von Remoteobjekt Proxys am besten abläuft.

Für Remote Objektproxys gibt es zusätzlich die folgenden Methoden, die lokal ausgeführt werden:

* applyRemote, getRemote, setremote: Durchführen eines Methodenaufrufs, eines Eigenschaften Abstands oder eines Eigenschaftssatzes für das Remoteobjekt. Mit diesen können Sie explizit erzwingen, dass eine Methode oder Eigenschaft Remote ausgeführt wird, wenn eine in Konflikt stehende lokale Methode oder Eigenschaft vorhanden ist. Beispielsweise führt `proxy.toString()` die lokale ToString-Methode für das Proxyobjekt aus. `proxy.applyRemote('toString')`Wird aber `toString` stattdessen auf dem Remoteproxy Objekt ausgeführt.

* getLocal, setlocal: führt Eigenschaften abrufen oder Eigenschaftssatz lokal aus. Sie können diese Methoden verwenden, um das Abrufen oder Festlegen einer Eigenschaft für den Remoteobjekt Proxy selbst und nicht für das Remoteobjekt zu erzwingen, das es darstellt. Beispielsweise `proxy.unknownProperty` wird die Eigenschaft abgerufen, die `unknownProperty` aus dem Remoteproxy Objekt benannt wurde. `proxy.getLocal('unknownProperty')`Der Wert der Eigenschaft wird jedoch `unknownProperty` für das Proxyobjekt selbst abgerufen.

* Synchronisierung: asynchrone Remoteobjekt Proxys machen eine Synchronisierungsmethode verfügbar, die ein Versprechen für einen synchronen Remoteobjekt Proxy für das gleiche Remoteobjekt zurückgibt. Gibt beispielsweise `chrome.webview.remoteObjects.sample.methodCall()` einen asynchronen Remoteobjekt Proxy zurück. Sie können stattdessen die `sync` Methode zum Abrufen eines synchronen Remoteobjekt Proxys verwenden: `const syncProxy = await chrome.webview.remoteObjects.sample.methodCall().sync()`

* Async: synchrone Remoteobjekt Proxys machen eine asynchrone Methode verfügbar, die einen asynchronen Remoteobjekt Proxy für das gleiche Remoteobjekt blockiert und zurückgibt. Gibt beispielsweise `chrome.webview.remoteObjects.sync.sample.methodCall()` einen synchronen Remoteobjekt Proxy zurück. Aufruf der `async` Methode für diesen Block und anschließendes zurückgeben eines asynchronen Remoteobjekt Proxys für dasselbe Remoteobjekt: `const asyncProxy = chrome.webview.remoteObjects.sync.sample.methodCall().async()`

* dann: asynchrone Remoteobjekt Proxys verfügen über eine then-Methode. Auf diese Weise können Sie warten. `then` gibt eine Verheißung zurück, die mit einer Darstellung des Remoteobjekts aufgelöst wird. Wenn der Proxy ein JavaScript-Literal darstellt, wird eine Kopie davon lokal zurückgegeben. Wenn der Proxy eine Funktion darstellt, wird ein nicht erwarteter Proxy zurückgegeben. Wenn der Proxy ein JavaScript-Objekt mit einer Kombination aus Literalen Eigenschaften und Funktionseigenschaften darstellt, wird eine Kopie des Objekts mit einigen Eigenschaften als Remoteobjekt Proxys zurückgegeben.

Alle anderen Eigenschaften-und Methodenaufrufe (außer den oben genannten Methoden für Remote Objektproxy, forceLocalProperties-Liste und Eigenschaften für Funktions-und Objekt Prototypen) werden Remote ausgeführt. Asynchrone Remoteobjekt Proxys geben eine Versprechung zurück, die den asynchronen Abschluss des Remoteaufrufs der Methode oder das Abrufen der Eigenschaft darstellt. Das Versprechen wird aufgelöst, nachdem die Remotevorgänge abgeschlossen sind und die Zusagen in den resultierenden Wert des Vorgangs aufgelöst werden. Synchrone Remoteobjekt Proxys funktionieren ähnlich, blockieren aber die JavaScript-Ausführung und warten, bis der Remotevorgang abgeschlossen ist.

Das Festlegen einer Eigenschaft für einen asynchronen Remoteobjekt Proxy funktioniert etwas anders. Der Satz wird sofort zurückgegeben, und der Rückgabewert ist der Wert, der festgesetzt wird. Dies ist eine Anforderung des JavaScript-Proxy Objekts. Wenn Sie asynchron warten müssen, bis die Eigenschaft auf Complete gesetzt ist, verwenden Sie die setremote-Methode, die eine Verheißung zurückgibt, wie oben beschrieben. Eigenschaft für synchrone Objekteigenschaft festlegen synchron blockiert, bis die Eigenschaft gesetzt ist.

Angenommen, Sie verfügen über ein COM-Objekt mit der folgenden Schnittstelle.

```IDL
    [uuid(3a14c9c0-bc3e-453f-a314-4ce4a0ec81d8), object, local]
    interface IRemoteObjectSample : IUnknown
    {
        // Demonstrate basic method call with some parameters and a return value.
        HRESULT MethodWithParametersAndReturnValue([in] BSTR stringParameter, [in] INT integerParameter, [out, retval] BSTR* stringResult);

        // Demonstrate getting and setting a property.
        [propget] HRESULT Property([out, retval] BSTR* stringResult);
        [propput] HRESULT Property([in] BSTR stringValue);

        // Demonstrate native calling back into JavaScript.
        HRESULT CallCallbackAsynchronously([in] IDispatch* callbackParameter);
    };
```

 Wir können eine Instanz dieser Schnittstelle in unserem JavaScript mit hinzufügen `AddRemoteObject` . In diesem Fall nennen wir `sample` Folgendes:

```cpp
            VARIANT remoteObjectAsVariant = {};
            m_remoteObject.query_to<IDispatch>(&remoteObjectAsVariant.pdispVal);
            remoteObjectAsVariant.vt = VT_DISPATCH;

            // We can call AddRemoteObject multiple times in a row without
            // calling RemoveRemoteObject first. This will replace the previous object
            // with the new object. In our case this is the same object and everything
            // is fine.
            CHECK_FAILURE(m_webView->AddRemoteObject(L"sample", &remoteObjectAsVariant));
            remoteObjectAsVariant.pdispVal->Release();
```

 Im HTML-Dokument können wir dieses COM-Objekt dann über `chrome.webview.remoteObjects.sample` Folgendes verwenden:

```js
        document.getElementById("getPropertyAsyncButton").addEventListener("click", async () => {
            const propertyValue = await chrome.webview.remoteObjects.sample.property;
            document.getElementById("getPropertyAsyncOutput").textContent = propertyValue;
        });

        document.getElementById("getPropertySyncButton").addEventListener("click", () => {
            const propertyValue = chrome.webview.remoteObjects.sync.sample.property;
            document.getElementById("getPropertySyncOutput").textContent = propertyValue;
        });

        document.getElementById("setPropertyAsyncButton").addEventListener("click", async () => {
            const propertyValue = document.getElementById("setPropertyAsyncInput").value;
            // The following line will work but it will return immediately before the property value has actually been set.
            // If you need to set the property and wait for the property to change value, use the setRemote function.
            chrome.webview.remoteObjects.sample.property = propertyValue;
            document.getElementById("setPropertyAsyncOutput").textContent = "Set";
        });

        document.getElementById("setPropertyExplicitAsyncButton").addEventListener("click", async () => {
            const propertyValue = document.getElementById("setPropertyExplicitAsyncInput").value;
            // If you care about waiting until the property has actually changed value use the setRemote function.
            await chrome.webview.remoteObjects.sample.setRemote("property", propertyValue);
            document.getElementById("setPropertyExplicitAsyncOutput").textContent = "Set";
        });

        document.getElementById("setPropertySyncButton").addEventListener("click", () => {
            const propertyValue = document.getElementById("setPropertySyncInput").value;
            chrome.webview.remoteObjects.sync.sample.property = propertyValue;
            document.getElementById("setPropertySyncOutput").textContent = "Set";
        });

        document.getElementById("invokeMethodAsyncButton").addEventListener("click", async () => {
            const paramValue1 = document.getElementById("invokeMethodAsyncParam1").value;
            const paramValue2 = parseInt(document.getElementById("invokeMethodAsyncParam2").value);
            const resultValue = await chrome.webview.remoteObjects.sample.MethodWithParametersAndReturnValue(paramValue1, paramValue2);
            document.getElementById("invokeMethodAsyncOutput").textContent = resultValue;
        });

        document.getElementById("invokeMethodSyncButton").addEventListener("click", () => {
            const paramValue1 = document.getElementById("invokeMethodSyncParam1").value;
            const paramValue2 = parseInt(document.getElementById("invokeMethodSyncParam2").value);
            const resultValue = chrome.webview.remoteObjects.sync.sample.MethodWithParametersAndReturnValue(paramValue1, paramValue2);
            document.getElementById("invokeMethodSyncOutput").textContent = resultValue;
        });

        let callbackCount = 0;
        document.getElementById("invokeCallbackButton").addEventListener("click", async () => {
            chrome.webview.remoteObjects.sample.CallCallbackAsynchronously(() => {
                document.getElementById("invokeCallbackOutput").textContent = "Native object called the callback " + (++callbackCount) + " time(s).";
            });
        });
```

#### RemoveRemoteObject 

Entfernen Sie das vom Namen angegebene Hostobjekt, damit es nicht mehr über JavaScript-Code in der WebView zugänglich ist.

> Public HRESULT [RemoveRemoteObject](#removeremoteobject)(LPCWSTR Name)

Während neue Zugriffsversuche verweigert werden, wenn das Objekt bereits durch JavaScript-Code in der WebView abgerufen wird, hat der JavaScript-Code weiterhin Zugriff auf das Objekt. Das Aufrufen dieser Methode für einen Namen, der bereits entfernt oder nie hinzugefügt wird, schlägt fehl.

#### OpenDevToolsWindow 

Öffnet das devtools-Fenster für das aktuelle Dokument in der WebView.

> Public HRESULT [OpenDevToolsWindow](#opendevtoolswindow)()

Wenn das devtools-Fenster bereits geöffnet ist, wird nichts aufgerufen

#### add_ContainsFullScreenElementChanged 

Benachrichtigt, wenn sich die ContainsFullScreenElement-Eigenschaft ändert.

> Public HRESULT [add_ContainsFullScreenElementChanged](#add_containsfullscreenelementchanged)([ICoreWebView2ContainsFullScreenElementChangedEventHandler](ICoreWebView2ContainsFullScreenElementChangedEventHandler.md) * EventHandler, EventRegistrationToken * Token)

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

#### remove_ContainsFullScreenElementChanged 

Entfernen Sie einen Ereignishandler, der zuvor mit der entsprechenden add_-Ereignismethode hinzugefügt wurde.

> Public HRESULT [remove_ContainsFullScreenElementChanged](#remove_containsfullscreenelementchanged)(EventRegistrationToken-Token)

#### get_ContainsFullScreenElement 

Gibt an, ob die WebView ein HTML-Vollbild-Element enthält.

> Public HRESULT [get_ContainsFullScreenElement](#get_containsfullscreenelement)(bool * ContainsFullScreenElement)

#### add_WebResourceRequested 

Fügen Sie einen Ereignishandler für das WebResourceRequested-Ereignis hinzu.

> Public HRESULT [add_WebResourceRequested](#add_webresourcerequested)([ICoreWebView2WebResourceRequestedEventHandler](ICoreWebView2WebResourceRequestedEventHandler.md) * EventHandler, EventRegistrationToken * Token)

Wird ausgelöst, wenn die WebView eine HTTP-Anforderung an einen übereinstimmenden URL-und Ressourcenkontext Filter ausführt, der mit AddWebResourceRequestedFilter hinzugefügt wurde. Es muss mindestens ein Filter hinzugefügt werden, damit das Ereignis ausgelöst wird.

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

#### remove_WebResourceRequested 

Entfernen Sie einen Ereignishandler, der zuvor mit add_WebResourceRequested hinzugefügt wurde.

> Public HRESULT [remove_WebResourceRequested](#remove_webresourcerequested)(EventRegistrationToken-Token)

#### AddWebResourceRequestedFilter 

Fügt dem WebResourceRequested-Ereignis einen URI-und Ressourcenkontext Filter hinzu.

> Public HRESULT [AddWebResourceRequestedFilter](#addwebresourcerequestedfilter)(LPCWSTR const URI,[CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT](#core_webview2_web_resource_context) const resourcecontext)

Der URI-Parameter kann eine Platzhalterzeichenfolge (' ': 0 oder mehr; '? ': genau eins) sein. nullptr entspricht L "". Eine Beschreibung der Ressourcenkontext Filter finden Sie unter CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT Enum.

#### RemoveWebResourceRequestedFilter 

Entfernt einen übereinstimmenden Webressourcen Filter, der zuvor für das WebResourceRequested-Ereignis hinzugefügt wurde.

> Public HRESULT [RemoveWebResourceRequestedFilter](#removewebresourcerequestedfilter)(LPCWSTR const URI,[CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT](#core_webview2_web_resource_context) const resourcecontext)

Wenn derselbe Filter mehrmals hinzugefügt wurde, muss er so oft entfernt werden, wie er hinzugefügt wurde, damit er wirksam wird. Gibt E_INVALIDARG für einen Filter zurück, der nie hinzugefügt wurde.

#### add_WindowCloseRequested 

Fügen Sie einen Ereignishandler für das WindowCloseRequested-Ereignis hinzu.

> Public HRESULT [add_WindowCloseRequested](#add_windowcloserequested)([ICoreWebView2WindowCloseRequestedEventHandler](ICoreWebView2WindowCloseRequestedEventHandler.md) * EventHandler, EventRegistrationToken * Token)

Wird ausgelöst, wenn der Inhalt in der WebView zum Schließen des Fensters angefordert wird, beispielsweise nach dem Aufruf von Window. Close. Die APP sollte das Fenster WebView und verwandte APP schließen, wenn dies für die APP sinnvoll ist.

```cpp
    // Register a handler for the WindowCloseRequested event.
    // This handler will close the app window if it is not the main window.
    CHECK_FAILURE(m_webView->add_WindowCloseRequested(
        Callback<ICoreWebView2WindowCloseRequestedEventHandler>(
            [this](ICoreWebView2* sender, IUnknown* args) {
                if (m_isPopupWindow)
                {
                    CloseAppWindow();
                }
                return S_OK;
            })
            .Get(),
        nullptr));
```

#### remove_WindowCloseRequested 

Entfernen Sie einen Ereignishandler, der zuvor mit add_WindowCloseRequested hinzugefügt wurde.

> Public HRESULT [remove_WindowCloseRequested](#remove_windowcloserequested)(EventRegistrationToken-Token)

#### CORE_WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT 

Bildformat, das von der ICoreWebView2:: CapturePreview-Methode verwendet wird.

> Enum- [CORE_WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT](#core_webview2_capture_preview_image_format)

 Werte                         | Beschreibungen
--------------------------------|---------------------------------------------
CORE_WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT_PNG            | PNG-Bildformat.
CORE_WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT_JPEG            | JPEG-Bildformat.

#### CORE_WEBVIEW2_SCRIPT_DIALOG_KIND 

Art des in der ICoreWebView2ScriptDialogOpeningEventHandler-Schnittstelle verwendeten JavaScript-Dialogfelds.

> Enum- [CORE_WEBVIEW2_SCRIPT_DIALOG_KIND](#core_webview2_script_dialog_kind)

 Werte                         | Beschreibungen
--------------------------------|---------------------------------------------
CORE_WEBVIEW2_SCRIPT_DIALOG_KIND_ALERT            | Ein Dialogfeld, das über die JavaScript-Funktion "Window. Alert" aufgerufen wird.
CORE_WEBVIEW2_SCRIPT_DIALOG_KIND_CONFIRM            | Ein Dialogfeld, das über die JavaScript-Funktion "Fenster. bestätigen" aufgerufen wird.
CORE_WEBVIEW2_SCRIPT_DIALOG_KIND_PROMPT            | Ein Dialogfeld, das über die JavaScript-Funktion "Window. prompt" aufgerufen wird.
CORE_WEBVIEW2_SCRIPT_DIALOG_KIND_BEFOREUNLOAD            | Ein Dialogfeld, das über das beforeunload-JavaScript-Ereignis aufgerufen wird.

#### CORE_WEBVIEW2_PROCESS_FAILED_KIND 

Art des in der ICoreWebView2ProcessFailedEventHandler-Schnittstelle verwendeten Prozess Fehlers.

> Enum- [CORE_WEBVIEW2_PROCESS_FAILED_KIND](#core_webview2_process_failed_kind)

 Werte                         | Beschreibungen
--------------------------------|---------------------------------------------
CORE_WEBVIEW2_PROCESS_FAILED_KIND_BROWSER_PROCESS_EXITED            | Gibt an, dass der Browserprozess unerwartet beendet wurde.
CORE_WEBVIEW2_PROCESS_FAILED_KIND_RENDER_PROCESS_EXITED            | Gibt an, dass der Renderprozess unerwartet beendet wurde.
CORE_WEBVIEW2_PROCESS_FAILED_KIND_RENDER_PROCESS_UNRESPONSIVE            | Gibt an, dass der Renderprozess nicht mehr reagiert.

#### CORE_WEBVIEW2_PERMISSION_KIND 

Der Typ einer Berechtigungsanforderung.

> Enum- [CORE_WEBVIEW2_PERMISSION_KIND](#core_webview2_permission_kind)

 Werte                         | Beschreibungen
--------------------------------|---------------------------------------------
CORE_WEBVIEW2_PERMISSION_KIND_UNKNOWN_PERMISSION            | Unbekannte Berechtigung.
CORE_WEBVIEW2_PERMISSION_KIND_MICROPHONE            | Berechtigung zum Aufzeichnen von Audio.
CORE_WEBVIEW2_PERMISSION_KIND_CAMERA            | Berechtigung zum Aufzeichnen von Videos.
CORE_WEBVIEW2_PERMISSION_KIND_GEOLOCATION            | Berechtigung für den Zugriff auf Geolocation.
CORE_WEBVIEW2_PERMISSION_KIND_NOTIFICATIONS            | Berechtigung zum Senden von webbenachrichtigungen.
CORE_WEBVIEW2_PERMISSION_KIND_OTHER_SENSORS            | Berechtigung für den Zugriff auf den generischen Sensor.
CORE_WEBVIEW2_PERMISSION_KIND_CLIPBOARD_READ            | Berechtigung zum Lesen der Systemzwischenablage ohne Benutzergeste

#### CORE_WEBVIEW2_PERMISSION_STATE 

Antwort auf eine Berechtigungsanforderung.

> Enum- [CORE_WEBVIEW2_PERMISSION_STATE](#core_webview2_permission_state)

 Werte                         | Beschreibungen
--------------------------------|---------------------------------------------
CORE_WEBVIEW2_PERMISSION_STATE_DEFAULT            | Verwenden Sie das Standardbrowser Verhalten, das die Benutzer normalerweise zur Entscheidung auffordert.
CORE_WEBVIEW2_PERMISSION_STATE_ALLOW            | Erteilen Sie die Berechtigungsanforderung.
CORE_WEBVIEW2_PERMISSION_STATE_DENY            | Verweigern Sie die Berechtigungsanforderung.

#### CORE_WEBVIEW2_WEB_ERROR_STATUS 

Fehlerstatus Werte für Web-Navigationselemente.

> Enum- [CORE_WEBVIEW2_WEB_ERROR_STATUS](#core_webview2_web_error_status)

 Werte                         | Beschreibungen
--------------------------------|---------------------------------------------
CORE_WEBVIEW2_WEB_ERROR_STATUS_UNKNOWN            | Ein unbekannter Fehler ist aufgetreten.
CORE_WEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_COMMON_NAME_IS_INCORRECT            | Der allgemeine Name des SSL-Zertifikats entspricht nicht der Webadresse.
CORE_WEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_EXPIRED            | Das SSL-Zertifikat ist abgelaufen.
CORE_WEBVIEW2_WEB_ERROR_STATUS_CLIENT_CERTIFICATE_CONTAINS_ERRORS            | Das SSL-Clientzertifikat enthält Fehler.
CORE_WEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_REVOKED            | Das SSL-Zertifikat wurde gesperrt.
CORE_WEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_IS_INVALID            | Das SSL-Zertifikat ist ungültig &ndash; Dies könnte bedeuten, dass das Zertifikat nicht mit den öffentlichen Schlüssel Pins für den Hostnamen übereinstimmte. das Zertifikat wird von einer nicht vertrauenswürdigen Zertifizierungsstelle signiert oder mit einem schwachen Vorzeichen Algorithmus, das Zertifikat behauptet, dass DNS-Namen gegen Namenseinschränkungen verstoßen, das Zertifikat einen schwachen Schlüssel enthält, der Gültigkeitszeitraum des Zertifikats zu lang ist, fehlender Sperrungsinformationen oder Sperrungs Mechanismus, nicht eindeutiger [legacy Symantec root](https://security.googleblog.com/2018/03/distrust-of-symantec-pki-immediate.html)Hostname, fehlender Zertifikat Transparenzinformationen oder das Zertifikat an
CORE_WEBVIEW2_WEB_ERROR_STATUS_SERVER_UNREACHABLE            | Der Host ist nicht erreichbar.
CORE_WEBVIEW2_WEB_ERROR_STATUS_TIMEOUT            | Die Verbindung hat ein Zeitlimit überschritten.
CORE_WEBVIEW2_WEB_ERROR_STATUS_ERROR_HTTP_INVALID_SERVER_RESPONSE            | Der Server hat eine ungültige oder unbekannte Antwort zurückgegeben.
CORE_WEBVIEW2_WEB_ERROR_STATUS_CONNECTION_ABORTED            | Die Verbindung wurde abgebrochen.
CORE_WEBVIEW2_WEB_ERROR_STATUS_CONNECTION_RESET            | Die Verbindung wurde zurückgesetzt.
CORE_WEBVIEW2_WEB_ERROR_STATUS_DISCONNECTED            | Die Internet Verbindung wurde unterbrochen.
CORE_WEBVIEW2_WEB_ERROR_STATUS_CANNOT_CONNECT            | Verbindung mit Ziel kann nicht hergestellt werden.
CORE_WEBVIEW2_WEB_ERROR_STATUS_HOST_NAME_NOT_RESOLVED            | Der angegebene Hostname konnte nicht aufgelöst werden.
CORE_WEBVIEW2_WEB_ERROR_STATUS_OPERATION_CANCELED            | Der Vorgang wurde abgebrochen.
CORE_WEBVIEW2_WEB_ERROR_STATUS_REDIRECT_FAILED            | Die Anforderungs Umleitung ist fehlgeschlagen.
CORE_WEBVIEW2_WEB_ERROR_STATUS_UNEXPECTED_ERROR            | Ein unerwarteter Fehler ist aufgetreten.

#### CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT 

Enum für Webressourcen-anforderungskontexte.

> Enum- [CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT](#core_webview2_web_resource_context)

 Werte                         | Beschreibungen
--------------------------------|---------------------------------------------
CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_ALL            | Alle Ressourcen.
CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_DOCUMENT            | Dokument Ressourcen.
CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_STYLESHEET            | CSS-Ressourcen.
CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_IMAGE            | Bildressourcen.
CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_MEDIA            | Andere Medienressourcen wie Videos.
CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_FONT            | Schriftartressourcen.
CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_SCRIPT            | Skriptressourcen.
CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_XML_HTTP_REQUEST            | XML-HTTP-Anforderungen.
CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_FETCH            | Abrufen der API-Kommunikation.
CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_TEXT_TRACK            | Texttracking-Ressourcen.
CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_EVENT_SOURCE            | EventSource-API-Kommunikation.
CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_WEBSOCKET            | WebSocket-API-Kommunikation.
CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_MANIFEST            | Web App-Manifeste
CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_SIGNED_EXCHANGE            | Signierte http-Exchanges.
CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_PING            | Ping-Anforderungen.
CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_CSP_VIOLATION_REPORT            | Berichte zu CSP-Verstößen
CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_OTHER            | Andere Ressourcen.
