---
description: Leitfaden für erste Schritte mit WebView2 für Win32-apps
title: Erste Schritte mit WebView2 für Win32-apps
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/14/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: 906ddbea08440aaa0f1fd7e32550c3b1790ba8a1
ms.sourcegitcommit: 61cc15d2fc89aee3e09cec48ef1e0e5bbf8d289a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/15/2020
ms.locfileid: "11119101"
---
# Erste Schritte mit WebView2 (Entwicklervorschau)  

Der folgende Inhalt führt Sie durch die häufig verwendeten Funktionen von [WebView2 (Developer Preview)][Webview2Index] und stellt einen Ausgangspunkt zum Erstellen Ihrer ersten WebView2-App bereit.  Weitere Informationen zu einzelnen WebView2-APIs finden Sie unter [API-Referenz][Webview2ReferenceWin32].  

## Voraussetzungen  

*   [Microsoft Edge (Chrom)][MicrosoftedgeinsiderDownload] ist auf unterstützten Betriebssystemen installiert \ (derzeit Windows 10, Windows 8,1 und Windows 7).  
    
    > [!NOTE]
    > Das WebView-Team empfiehlt die Verwendung des Canary-Kanals, und die erforderliche Mindestversion ist 82.0.488.0.  
    
*   [Visual Studio][MicrosoftVisualstudioMain] 2015 oder höher mit installierter C++-Unterstützung.  

## Schritt 1 – Erstellen einer Win32-App für ein einzelnes Fenster  

Beginnen Sie mit einem einfachen Desktopprojekt, das ein einzelnes Hauptfenster enthält.  Um die exemplarische Vorgehensweise besser zu fokussieren, verwenden Sie den geänderten Beispielcode aus [Exemplarische Vorgehensweise: Erstellen einer herkömmlichen Windows-Desktop Anwendung (C++)][CppWindowsWalkthroughCreatingDesktopApplication] für Ihre Beispiel-app.  Informationen zum Herunterladen des geänderten Beispiels und erste Schritte finden Sie unter [WebView2-Beispiele][GithubMicrosoftedgeWebview2samplesGettingStartedGuide].  

Öffnen Sie in Visual Studio `WebView2GettingStarted.sln` .  Wenn Sie eine ältere Version von Visual Studio verwenden, zeigen Sie mit der Maus auf das **WebView2GettingStarted** -Projekt, öffnen Sie das Kontextmenü \ (Klicken Sie mit der rechten Maustaste auf \), und wählen Sie **Eigenschaften**aus.  Ändern Sie unter **Konfigurationseigenschaften**  >  **Allgemein**die **Windows SDK-Version** und das **Platform-Toolset** , um das Win10-SDK und das Visual Studio-Toolset \ (vs Toolset \) zu verwenden, das Ihnen zur Verfügung steht.  

:::image type="complex" source="../media/tool-version.png" alt-text="Tool Version":::
   Tool Version  
:::image-end:::  

In Visual Studio werden möglicherweise Fehler aufgrund fehlender WebView2-Headerdatei angezeigt, die nach Abschluss von Schritt 2 verschwinden sollten.  

## Schritt 2 – Installieren des WebView2 SDK  

Fügen Sie das WebView2-SDK in das Projekt ein.  Für die Entwicklervorschau können Sie das Win32-SDK mithilfe von Nuget installieren.  

1.  Zeigen Sie mit der Maus auf das Projekt, öffnen Sie das Kontextmenü \ (Klicken Sie mit der rechten Maustaste auf \), und wählen Sie **Nuget-Pakete verwalten**aus.  
    
    :::image type="complex" source="../media/manage-nuget-packages.png" alt-text="Tool Version":::
       Verwalten von Nuget-Paketen  
    :::image-end:::  
    
1.  Installieren Sie die Windows-Implementierungs Bibliothek.  
    1.  Geben Sie `Microsoft.Windows.ImplementationLibrary` in der Suchleiste **Microsoft. Windows. ImplementationLibrary** aus den Ergebnissen ein, und wählen Sie im rechten Fenster **Installieren** aus.  Nuget downloadet das SDK auf Ihren Computer.  
        
        > [!NOTE] 
        > Die [Windows-Implementierungs Bibliothek][GithubMicrosoftWilMain] und die [Windows-Runtime-C++-Vorlagenbibliothek][CppCxWrlTemplateLibraryVS2019] sind optional und wurden hinzugefügt, um die Arbeit mit com für das Beispiel zu vereinfachen.  
        
        :::image type="complex" source="../media/wil.png" alt-text="Tool Version":::
           Windows-Implementierungs Bibliothek  
        :::image-end:::  
        
1.  Installieren Sie das WebView2-SDK.  
    1.  Geben Sie `Microsoft.Web.WebView2` in der Suchleiste **Microsoft. Web. WebView2** aus den Ergebnissen ein, und wählen Sie im rechten Fenster **Installieren** aus.  Nuget downloadet das SDK auf Ihren Computer.  
        
        :::image type="complex" source="../media/nuget.png" alt-text="Tool Version":::
           Nuget-Paket-Manager
        :::image-end:::  
        
1.  Fügen Sie WebView2-Kopfzeile zu Ihrem Projekt hinzu.  
    :::row:::
       :::column span="1":::
          Öffnen `HelloWebView.cpp` , kopieren Sie den folgenden Codeausschnitt, und fügen Sie ihn `HelloWebView.cpp` nach der letzten `#include` Zeile ein.  
          
          ```cpp
          // include WebView2 header
          #include "WebView2.h"
          ```  
       :::column-end:::
       :::column span="1":::
          Der Abschnitt include sollte ähnlich wie der folgende Codeausschnitt aussehen.  
          
          ```cpp
          ...
          #include <wrl.h>
          #include <wil/com.h>
          // include WebView2 header
          #include "WebView2.h"
          ```  
       :::column-end:::
    :::row-end:::
    
Sie sind für die Verwendung und Erstellung von WebView2-APIs eingestellt.  

### Erstellen der leeren Beispiel-App  

Drücken Sie `F5` , um die Beispiel-APP zu erstellen und auszuführen.  Es sollte eine App angezeigt werden, die ein leeres Fenster anzeigt.  

:::image type="complex" source="../media/empty-app.png" alt-text="Tool Version":::
   Leere App  
:::image-end:::  

## Schritt 3 – Erstellen einer einzelnen WebView im übergeordneten Fenster  

Fügen Sie dem Hauptfenster eine WebView hinzu.  Verwenden Sie die `CreateCoreWebView2Environment` Methode zum Einrichten der Umgebung, und suchen Sie den Microsoft Edge \ (Chrom \)-Browser, der das Steuerelement steuert.  Sie können die Methode auch verwenden, `CreateCoreWebView2EnvironmentWithOptions` Wenn Sie den Browser Speicherort, den Benutzerordner, die Browser Kennzeichnung usw. angeben möchten, anstatt die Standardeinstellung zu verwenden.  Nach Abschluss der `CreateCoreWebView2Environment` Methode können Sie die `ICoreWebView2Environment::CreateCoreWebView2Controller` Methode innerhalb des `ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler` Rückrufs ausführen und die Methode ausführen, `ICoreWebView2Controller::get_CoreWebView2` um die zugeordnete WebView abzurufen.  

Legen Sie im Rückruf einige zusätzliche Einstellungen an, ändern Sie die Größe der WebView, um 100% des übergeordneten Fensters zu übernehmen, und navigieren Sie zu Bing.  

Kopieren Sie den folgenden Codeausschnitt, und fügen Sie ihn `HelloWebView.cpp` nach der `// <-- WebView2 sample code starts here -->` Notiz und vor der `// <-- WebView2 sample code ends here -->` Notiz ein.  

```cpp
// Step 3 - Create a single WebView within the parent window
// Locate the browser and set up the environment for WebView
CreateCoreWebView2EnvironmentWithOptions(nullptr, nullptr, nullptr,
    Callback<ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler>(
        [hWnd](HRESULT result, ICoreWebView2Environment* env) -> HRESULT {
        
            // Create a CoreWebView2Controller and get the associated CoreWebView2 whose parent is the main window hWnd
            env->CreateCoreWebView2Controller(hWnd, Callback<ICoreWebView2CreateCoreWebView2ControllerCompletedHandler>(
                [hWnd](HRESULT result, ICoreWebView2Controller* controller) -> HRESULT {
                if (controller != nullptr) {
                    webviewController = controller;
                    webviewController->get_CoreWebView2(&webviewWindow);
                }
                
                // Add a few settings for the webview
                // The demo step is redundant since the values are the default settings
                ICoreWebView2Settings* Settings;
                webviewWindow->get_Settings(&Settings);
                Settings->put_IsScriptEnabled(TRUE);
                Settings->put_AreDefaultScriptDialogsEnabled(TRUE);
                Settings->put_IsWebMessageEnabled(TRUE);
                
                // Resize WebView to fit the bounds of the parent window
                RECT bounds;
                GetClientRect(hWnd, &bounds);
                webviewController->put_Bounds(bounds);
                
                // Schedule an async task to navigate to Bing
                webviewWindow->Navigate(L"https://www.bing.com/");
                
                // Step 4 - Navigation events
                
                // Step 5 - Scripting
                
                // Step 6 - Communication between host and web content
                
                return S_OK;
            }).Get());
        return S_OK;
    }).Get());
```  


### Erstellen einer Bing-Beispiel-App  

Drücken Sie `F5` , um die APP zu erstellen und auszuführen.  Nun wird ein WebView-Fenster mit der Bing-Seite angezeigt.  

:::image type="complex" source="../media/bing-window.png" alt-text="Tool Version":::
   Bing-Fenster  
:::image-end:::  

## Schritt 4 – Navigationsereignisse  

Das WebView-Team hat bereits die Navigation zur URL unter Verwendung der `ICoreWebView2::Navigate` Methode im letzten Schritt abgedeckt.  Während der Navigation löst WebView eine Abfolge von Ereignissen aus, an die der Host möglicherweise lauscht.  

1.  `NavigationStarting`  
1.  `SourceChanged`  
1.  `ContentLoading`  
1.  `HistoryChanged`   
1.  `NavigationCompleted`   

Weitere Informationen finden Sie unter [Navigationsereignisse][Webview2ConceptsNavigationEvents].  

:::image type="complex" source="../media/navigation-events.png" alt-text="Tool Version":::
   Navigationsereignisse  
:::image-end:::  

In Fehlerfällen können eines oder mehrere der folgenden Ereignisse auftreten, je nachdem, ob die Navigation auf einer Fehlerseite fortgesetzt wird.  

*   `SourceChanged`  
*   `ContentLoading`  
*   `HistoryChanged`

Im Fall einer HTTP-Umleitung gibt es mehrere `NavigationStarting` Ereignisse in einer Zeile.  

Als Beispiel für die Verwendung der Ereignisse registrieren Sie einen Handler für das `NavigationStarting` Ereignis, um nicht-HTTPS-Anforderungen abzubrechen.  Kopieren Sie den folgenden Codeausschnitt, und fügen Sie ihn in ein `HelloWebView.cpp` .  

```cpp
// register an ICoreWebView2NavigationStartingEventHandler to cancel any non-https navigation
EventRegistrationToken token;
webviewWindow->add_NavigationStarting(Callback<ICoreWebView2NavigationStartingEventHandler>(
    [](ICoreWebView2* webview, ICoreWebView2NavigationStartingEventArgs * args) -> HRESULT {
        PWSTR uri;
        args->get_Uri(&uri);
        std::wstring source(uri);
        if (source.substr(0, 5) != L"https") {
            args->put_Cancel(true);
        }
        CoTaskMemFree(uri);
        return S_OK;
    }).Get(), &token);
```  

Jetzt wird die APP nicht zu allen nicht-HTTPS-Websites navigiert.  Sie können einen ähnlichen Mechanismus verwenden, um andere Aufgaben auszuführen, wie etwa das Einschränken der Navigation in ihrer eigenen Domäne.  

## Schritt 5 – Skripting  

Die Host-App kann auch JavaScript in WebView einfügen.  Sie können mit der Aufgabe WebView beliebiges JavaScript ausführen oder Initialisierungsskripts hinzufügen.  Hinzugefügte Initialisierungsskripts gelten für alle zukünftigen Dokument-und untergeordneten Frame-Navigationselemente auf oberster Ebene, bis Sie entfernt werden, und werden nach dem Erstellen des globalen Objekts und vor dem Ausführen anderer Skripts ausgeführt, die im HTML-Dokument enthalten sind.  

Kopieren Sie den folgenden Codeausschnitt, und fügen Sie ihn in ein `HelloWebView.cpp` .  

```cpp
// Schedule an async task to add initialization script that freezes the Object object
webviewWindow->AddScriptToExecuteOnDocumentCreated(L"Object.freeze(Object);", nullptr);
// Schedule an async task to get the document URL
webviewWindow->ExecuteScript(L"window.document.URL;", Callback<ICoreWebView2ExecuteScriptCompletedHandler>(
    [](HRESULT errorCode, LPCWSTR resultObjectAsJson) -> HRESULT {
        LPCWSTR URL = resultObjectAsJson;
        //doSomethingWithURL(URL);
        return S_OK;
    }).Get());
```  

WebView sollte das Objekt nun immer fixieren `Object` und das Seiten Dokument einmal zurückgeben.  

> [!NOTE] 
> Die Skript Injektions-APIs \ (und einige andere WebView2-APIs \) sind asynchron, Sie sollten Rückrufe verwenden, wenn Code in einer bestimmten Reihenfolge ausgeführt werden muss.  

## Schritt 6 – Kommunikation zwischen Host-und Webinhalten  

Der Host und der Webinhalt können über die Methode auch miteinander kommunizieren `postMessage` .  Die Webinhalte, die in einer WebView ausgeführt werden, können über die Methode an den Host gesendet werden `window.chrome.webview.postMessage` , und die Nachricht wird von jedem registrierten `ICoreWebView2WebMessageReceivedEventHandler` Ereignishandler auf dem Host verarbeitet.  Ebenso kann der Host den Webinhalt über oder die `ICoreWebView2::PostWebMessageAsString` `ICoreWebView2::PostWebMessageAsJSON` Methode Nachrichten, die von Handlern abgefangen wird, die vom Listener hinzugefügt werden `window.chrome.webview.addEventListener` .  Mithilfe des Kommunikationsmechanismus können Webinhalte systemeigene Funktionen verwenden, indem Sie Nachrichten übergeben, um den Host zu bitten, systemeigene APIs aufzurufen.  

Als Beispiel, um den Mechanismus zu verstehen, treten die folgenden Schritte auf, wenn Sie versuchen, die Dokument-URL in WebView zu drucken.  

1.  Der Host registriert einen Handler, um die empfangene Nachricht zurück an den Webinhalt zurückzugeben  
1.  Der Host injiziert einem Webinhalt ein Skript, das einen Handler registriert, um eine Nachricht vom Host zu drucken.  
1.  Der Host injiziert einem Webinhalt ein Skript, das die URL an den Host sendet.  
1.  Der Handler des Hosts wird ausgelöst und gibt die Nachricht \ (die URL \) an den Webinhalt zurück.  
1.  Der Handler des Webinhalts wird ausgelöst, und die Nachricht wird vom Host \ (der URL \) gedruckt.  

Kopieren Sie den folgenden Codeausschnitt, und fügen Sie ihn in ein `HelloWebView.cpp` .    

```cpp
// Set an event handler for the host to return received message back to the web content
webviewWindow->add_WebMessageReceived(Callback<ICoreWebView2WebMessageReceivedEventHandler>(
    [](ICoreWebView2* webview, ICoreWebView2WebMessageReceivedEventArgs * args) -> HRESULT {
        PWSTR message;
        args->TryGetWebMessageAsString(&message);
        // processMessage(&message);
        webview->PostWebMessageAsString(message);
        CoTaskMemFree(message);
        return S_OK;
    }).Get(), &token);

// Schedule an async task to add initialization script that
// 1) Add an listener to print message from the host
// 2) Post document URL to the host
webviewWindow->AddScriptToExecuteOnDocumentCreated(
    L"window.chrome.webview.addEventListener(\'message\', event => alert(event.data));" \
    L"window.chrome.webview.postMessage(window.document.URL);",
nullptr);
```  

### Erstellen einer Beispiel-App für die Show-URL  

Drücken Sie `F5` , um die APP zu erstellen und auszuführen.  Sie sollten die URL in einem Popupfenster sehen, bevor Sie zu einer Seite navigieren.  

:::image type="complex" source="../media/show-url.png" alt-text="Tool Version"  

[CppCxWrlTemplateLibraryVS2019]: /cpp/cppcx/wrl/windows-runtime-cpp-template-library-wrl?view=vs-2019&preserve-view=true "Windows-Runtime C++-Vorlagenbibliothek (WRL) | Microsoft docs"  
[CppWindowsWalkthroughCreatingDesktopApplication]: /cpp/windows/walkthrough-creating-windows-desktop-applications-cpp?view=vs-2019&preserve-view=true "Exemplarische Vorgehensweise: Erstellen einer herkömmlichen Windows-Desktop Anwendung (C++) | Microsoft docs"  

[GithubMicrosoftedgeWebview2browser]: https://github.com/MicrosoftEdge/WebView2Browser "WebView2Browser-MicrosoftEdge/WebView2Browser | GitHub"  

[GithubMicrosoftedgeWebviewfeedback]: https://github.com/MicrosoftEdge/WebViewFeedback "WebView-Feedback-MicrosoftEdge/WebViewFeedback | GitHub"  

[GithubMicrosoftedgeWebview2samplesApisample]: https://github.com/MicrosoftEdge/WebView2Samples/blob/master/SampleApps/WebView2APISample/README.md "WebView2-API-Beispiel-MicrosoftEdge/WebView2Samples | GitHub"  
[GithubMicrosoftedgeWebview2samplesGettingStartedGuide]: https://github.com/MicrosoftEdge/WebView2Samples#1-getting-started-guide "WebView2-Beispiele-MicrosoftEdge/WebView2Samples | GitHub"  

[GithubMicrosoftWilMain]: https://github.com/Microsoft/wil "Windows-Implementierungs Bibliotheken (Wil) – Microsoft/Wil | GitHub"  

[MicrosoftedgeinsiderDownload]: https://www.microsoftedgeinsider.com/download "Herunterladen von Microsoft Edge-Insider Kanälen"  

[MicrosoftVisualstudioMain]: https://visualstudio.microsoft.com "Visual Studio"  
