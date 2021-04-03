---
description: Erste Schritte mit WebView2 für Win32-Apps
title: Erste Schritte mit WebView2 für Win32-Apps
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/29/2021
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, webview, win32 apps, win32, edge, ICoreWebView2, ICoreWebView2Controller, browser control, edge html
ms.openlocfilehash: 19bc0c5600ebd072ad9a6aa61d2a965e999865ce
ms.sourcegitcommit: 2ddfd98d1e871be9c61380a8ca57da398d38bd54
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/02/2021
ms.locfileid: "11306159"
---
# <a name="getting-started-with-webview2"></a>Erste Schritte mit WebView2  

Beginnen Sie in diesem Artikel mit dem Erstellen Ihrer ersten WebView2-App, und erfahren Sie mehr über die Hauptfeatures von [WebView2][MicrosoftDeveloperMicrosoftEdgeWebview2].  Weitere Informationen zu einzelnen WebView2-APIs finden Sie unter [API-Referenz][Webview2ReferenceWin32].  

## <a name="prerequisites"></a>Voraussetzungen  

Stellen Sie sicher, dass Sie die folgende Liste der Voraussetzungen installieren, bevor Sie fortfahren.  

*   [WebView2-Laufzeit][Webview2Installer] oder ein nicht stabiler [Microsoft Edge (Chromium)-Kanal,][MicrosoftedgeinsiderDownload] der unter unterstützten Betriebssystemen installiert ist \(derzeit Windows 10, Windows 8.1 und Windows 7\).  
    
    > [!NOTE]
    > Das WebView-Team empfiehlt die Verwendung des Canary-Kanals, und die erforderliche Mindestversion ist 82.0.488.0.  
    
*   [Visual Studio][MicrosoftVisualstudioMain] 2015 oder höher mit installierter C++-Unterstützung.  
    
## <a name="step-1---create-a-single-window-app"></a>Schritt 1 : Erstellen einer App mit einem Fenster  

Beginnen Sie mit einem einfachen Desktopprojekt, das ein einzelnes Hauptfenster enthält.  

> [!IMPORTANT]
> Um die exemplarische Vorgehensweise besser zu fokussieren, verwenden Sie geänderten Beispielcode aus [Walkthrough: Create a traditional Windows Desktop application (C++)][CppWindowsWalkthroughCreatingDesktopApplication] for your sample app.  Um das geänderte Beispiel herunterzuladen und zu beginnen, navigieren Sie zu [WebView2 Samples][GithubMicrosoftedgeWebview2samplesGettingStartedGuide].  

1.  Öffnen Visual Studio in der Datei `WebView2GettingStarted.sln` .  
    Wenn Sie eine ältere Version von Visual Studio verwenden, zeigen Sie auf das **WebView2GettingStarted-Projekt,** öffnen Sie das Kontextmenü \(rechtsklicken\), und wählen Sie **Eigenschaften aus.**  Ändern **Sie unter Konfigurationseigenschaften**Allgemein windows SDK Version und Platform Toolset so, dass sie das  >  **** Win10 SDK und Visual Studio toolset verwenden, das Ihnen zur **** Verfügung steht. ****  

:::image type="complex" source="../media/tool-version.png" alt-text="Toolversion" lightbox="../media/tool-version.png":::
   Toolversion  
:::image-end:::  

Visual Studio können Fehler angezeigt werden, da in Ihrem Projekt die WebView2-Headerdatei fehlt.  Die Fehler sollten nach [Schritt 2 behoben werden.](#step-2---install-webview2-sdk)  

## <a name="step-2---install-webview2-sdk"></a>Schritt 2 : Installieren des WebView2 SDK  

Fügen Sie dem Projekt das WebView2 SDK hinzu.  Verwenden Sie NuGet, um das Win32 SDK zu installieren.  

1.  Zeigen Sie auf das Projekt, öffnen Sie das Kontextmenü \(klicken Sie mit der rechten Maustaste\), und wählen Sie **NuGet-Pakete verwalten aus.**  
    
    :::image type="complex" source="../media/manage-nuget-packages.png" alt-text="NuGet-Pakete verwalten" lightbox="../media/manage-nuget-packages.png":::
       NuGet-Pakete verwalten  
    :::image-end:::  
    
1.  Installieren Sie die Windows-Implementierungsbibliothek.  
    1.  Geben Sie in der Suchleiste `Microsoft.Windows.ImplementationLibrary` > Wählen Sie **Microsoft.Windows.ImplementationLibrary aus.**  
    1.  Wählen Sie im rechten Fenster Installieren **aus.**  NuGet lädt die Bibliothek auf Ihren Computer herunter.  
        
        > [!NOTE]
        > Die [Windows-Implementierungsbibliothek][GithubMicrosoftWilMain] und [die Windows-Runtime-C++-Vorlagenbibliothek][CppCxWrlTemplateLibraryVS2019] sind optional und erleichtern das Arbeiten mit COM für das Beispiel.  
        
        :::image type="complex" source="../media/wil.png" alt-text="Windows-Implementierungsbibliothek" lightbox="../media/wil.png":::
           Windows-Implementierungsbibliothek  
        :::image-end:::  
        
1.  Installieren Sie das WebView2 SDK.  
    1.  Geben Sie in der Suchleiste `Microsoft.Web.WebView2` > Wählen Sie **Microsoft.Web.WebView2 aus.**  
    1.  Wählen Sie im rechten Fenster Installieren **aus.**  NuGet lädt das SDK auf Ihren Computer herunter.  
        
        :::image type="complex" source="../media/nuget.png" alt-text="NuGet Paket-Manager" lightbox="../media/nuget.png":::
           NuGet Paket-Manager
        :::image-end:::  
        
1.  Fügen Sie Ihrem Projekt WebView2-Header hinzu.  
    :::row:::
       :::column span="1":::
          Kopieren Sie `HelloWebView.cpp` in der Datei den folgenden Codeausschnitt, und fügen Sie ihn nach der letzten Zeile `#include` ein.  
          
          ```cpp
          // include WebView2 header
          #include "WebView2.h"
          ```  
       :::column-end:::
       :::column span="1":::
          Der Include-Abschnitt sollte dem folgenden Codeausschnitt ähnlich aussehen.  
          
          ```cpp
          ...
          #include <wrl.h>
          #include <wil/com.h>
          // include WebView2 header
          #include "WebView2.h"
          ```  
       :::column-end:::
    :::row-end:::
    
Bereit für die Verwendung und Erstellung für die WebView2-API.  

### <a name="build-your-empty-sample-app"></a>Erstellen Einer leeren Beispiel-App  

Wählen Sie aus, um die Beispiel-App zu erstellen und `F5` ausführen.  Ihre App zeigt ein leeres Fenster an.  

:::image type="complex" source="../media/empty-app.png" alt-text="Leere App" lightbox="../media/empty-app.png":::
   Leere App  
:::image-end:::  

## <a name="step-3---create-a-single-webview-within-the-parent-window"></a>Schritt 3: Erstellen einer einzelnen WebView im übergeordneten Fenster  

Fügen Sie dem Hauptfenster eine WebView hinzu.  

 Verwenden Sie die -Methode, um die Umgebung zu einrichten und `CreateCoreWebView2Environment` den Microsoft Edge \(Chromium\)-Browser zu finden, der das Steuerelement unterstützt.  Sie können die Methode auch verwenden, wenn Sie browser location, user folder, browser flags und so weiter angeben möchten, anstatt die `CreateCoreWebView2EnvironmentWithOptions` Standardeinstellung zu verwenden.  Führen Sie nach Abschluss der Methode die Methode im Rückruf aus, und führen Sie die `CreateCoreWebView2Environment` -Methode aus, `ICoreWebView2Environment::CreateCoreWebView2Controller` um die `ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler` `ICoreWebView2Controller::get_CoreWebView2` zugeordnete WebView zu erhalten.  

Legen Sie im Rückruf einige weitere Einstellungen ein, ändern Sie die Größe der WebView auf 100 % des übergeordneten Fensters, und navigieren Sie zu Bing.  

Kopieren Sie den folgenden Codeausschnitt, und fügen Sie ihn `HelloWebView.cpp` nach dem Kommentar und vor dem Kommentar `// <-- WebView2 sample code starts here -->` `// <-- WebView2 sample code ends here -->` ein.  

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

### <a name="build-your-bing-sample-app"></a>Erstellen Ihrer Bing-Beispiel-App  

Wählen Sie zum Erstellen und Ausführen der App `F5` aus.  Jetzt haben Sie ein WebView-Fenster, in dem die Bing-Seite angezeigt wird.  

:::image type="complex" source="../media/bing-window.png" alt-text="Bing-Fenster" lightbox="../media/bing-window.png":::
   Bing-Fenster  
:::image-end:::  

## <a name="step-4---navigation-events"></a>Schritt 4 – Navigationsereignisse  

Das WebView-Team hat bereits im letzten Schritt die Navigation zu URL mithilfe der `ICoreWebView2::Navigate` -Methode behandelt.  Während der Navigation gibt WebView eine Abfolge von Ereignissen aus, auf die der Host lauschen kann.  

1.  `NavigationStarting`  
1.  `SourceChanged`  
1.  `ContentLoading`  
1.  `HistoryChanged`   
1.  `NavigationCompleted`   

Weitere Informationen finden Sie unter [Navigationsereignisse][Webview2ConceptsNavigationEvents].  

:::image type="complex" source="../media/navigation-events.png" alt-text="Navigationsereignisse" lightbox="../media/navigation-events.png":::
   Navigationsereignisse  
:::image-end:::  

In Fehlerfällen kann eines oder mehrere der folgenden Ereignisse auftreten, je nachdem, ob die Navigation zu einer Fehlerwebseite fortgesetzt wird.  

*   `SourceChanged`  
*   `ContentLoading`  
*   `HistoryChanged`

> [!NOTE]
> Wenn eine HTTP-Umleitung auftritt, gibt es mehrere `NavigationStarting` Ereignisse in einer Zeile.  

Registrieren Sie als Beispiel für die Verwendung der Ereignisse einen Handler für das Ereignis, `NavigationStarting` um alle Nicht-https-Anforderungen abbricht.  Kopieren Sie den folgenden Codeausschnitt, und fügen Sie ihn in `HelloWebView.cpp` ein.  

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

Jetzt navigiert die App nicht zu nicht https-Websites.  Sie können einen ähnlichen Mechanismus verwenden, um andere Aufgaben auszuführen, z. B. die Beschränkung der Navigation auf innerhalb Ihrer eigenen Domäne.  

## <a name="step-5---scripting"></a>Schritt 5 – Skripterstellung  

Sie können Host-Apps verwenden, um Zur Laufzeit JavaScript-Code in WebView2-Steuerelemente zu injizieren.  Sie können WebView zum Ausführen beliebiger JavaScript- oder Initialisierungsskripts aufgaben.  Das injizierte JavaScript gilt für alle neuen Dokumente der obersten Ebene und alle untergeordneten Frames, bis das JavaScript entfernt wird.  Das injizierte JavaScript wird mit einem bestimmten Timing ausgeführt.  

*   Führen Sie es nach der Erstellung des globalen Objekts aus.  
*   Führen Sie es aus, bevor ein anderes Skript ausgeführt wird, das im HTML-Dokument enthalten ist.  

Kopieren Sie den folgenden Codeausschnitt, und fügen Sie ihn in `HelloWebView.cpp` ein.  

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

Jetzt sollte WebView das Objekt immer fixieren `Object` und das Seitendokument einmal zurückgibt.  

> [!NOTE] 
> Die Skriptinjektions-APIs \(und einige andere WebView2-APIs\) sind asynchron. Sie sollten Rückrufe verwenden, wenn Code in einer bestimmten Reihenfolge ausgeführt werden muss.  

## <a name="step-6---communication-between-host-and-web-content"></a>Schritt 6 – Kommunikation zwischen Host- und Webinhalten  

Der Host und der Webinhalt können auch über die Methode miteinander `postMessage` kommunizieren.  Der in einer WebView ausgeführte Webinhalt kann über die -Methode an den Host gesendet werden, und die Nachricht wird von allen registrierten Ereignishandlern auf `window.chrome.webview.postMessage` `ICoreWebView2WebMessageReceivedEventHandler` dem Host verarbeitet.  Ebenso kann der Host den Webinhalt über oder die -Methode senden, die von Handlern erfasst wird, die vom `ICoreWebView2::PostWebMessageAsString` `ICoreWebView2::PostWebMessageAsJSON` Listener hinzugefügt `window.chrome.webview.addEventListener` wurden.  Der Kommunikationsmechanismus ermöglicht es dem Webinhalt, systemeigene Funktionen zu verwenden, indem Nachrichten übergeben werden, um den Host zum Ausführen systemeigener APIs zu bitten.  

Um den Mechanismus zu verstehen, führen Sie die folgenden Schritte aus, wenn Sie versuchen, die Dokument-URL in WebView auszuprobieren.  

1.  Der Host registriert einen Handler, um empfangene Nachrichten an den Webinhalt zurückzukehren  
1.  Der Host injiziert ein Skript in den Webinhalt, der einen Handler zum Drucken von Nachrichten vom Host registriert  
1.  Der Host injiziert ein Skript in den Webinhalt, der die URL auf dem Host veröffentlicht  
1.  Der Handler des Hosts wird ausgelöst und gibt die Nachricht \(die URL\) an den Webinhalt zurück.  
1.  Der Handler des Webinhalts wird ausgelöst und druckt die Nachricht vom Host \(die URL\)  

Kopieren Sie den folgenden Codeausschnitt, und fügen Sie ihn in `HelloWebView.cpp` ein.  

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

### <a name="build-your-display-url-sample-app"></a>Erstellen Der Beispiel-App für die Anzeige-URL  

Wählen Sie zum Erstellen und Ausführen der App `F5` aus.  Die URL wird in einem Popupfenster angezeigt, bevor sie zu einer Webseite navigiert.  

:::image type="complex" source="../media/show-url.png" alt-text="Anzeige-URL" lightbox="../media/show-url.png":::
   Anzeige-URL  
:::image-end:::  

Herzlichen Glückwunsch, Sie haben Ihre erste WebView2-App erstellt.  

## <a name="next-steps"></a>Nächste Schritte  

Viele der WebView2-Funktionen werden in diesem Artikel nicht behandelt, der folgende Abschnitt enthält weitere Ressourcen.  

### <a name="see-also"></a>Weitere Informationen  

*   Ein umfassendes Beispiel für WebView2-Funktionen finden Sie unter [WebView2-API-Beispiel][GithubMicrosoftedgeWebview2samplesApisample].  
*   Navigieren Sie zu [WebView2Browser,][GithubMicrosoftedgeWebview2browser]um eine mit WebView2 erstellte Beispiel-App zu navigieren.  
*   Ausführliche Informationen zur WebView2-API finden Sie unter [API-Referenz][Webview2ReferenceWin32].  

## <a name="getting-in-touch-with-the-microsoft-edge-webview-team"></a>Kontakt mit dem Microsoft Edge WebView-Team  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  

<!-- links -->  

[MicrosoftDeveloperMicrosoftEdgeWebview2]: https://developer.microsoft.com/microsoft-edge/webview2 " WebView2-| Microsoft Edge Developer"  

[Webview2ReferenceWin32]: /microsoft-edge/webview2/reference/win32 "WebView2 Win32 C++-Referenz | Microsoft Docs"  
[Webview2ConceptsNavigationEvents]: ../concepts/navigation-events.md "Navigationsereignisse | Microsoft Docs"  

[CppCxWrlTemplateLibraryVS2019]: /cpp/cppcx/wrl/windows-runtime-cpp-template-library-wrl?view=vs-2019&preserve-view=true "Windows Runtime C++ Template Library (WRL) | Microsoft Docs"  
[CppWindowsWalkthroughCreatingDesktopApplication]: /cpp/windows/walkthrough-creating-windows-desktop-applications-cpp?view=vs-2019&preserve-view=true "Exemplarische Vorgehensweise: Erstellen einer herkömmlichen Windows #A0 (C++) | Microsoft Docs"  

[GithubMicrosoftedgeWebview2browser]: https://github.com/MicrosoftEdge/WebView2Browser "WebView2Browser – MicrosoftEdge/WebView2Browser | GitHub"  

[GithubMicrosoftedgeWebviewfeedback]: https://github.com/MicrosoftEdge/WebViewFeedback "WebView Feedback – MicrosoftEdge/WebViewFeedback | GitHub"  

[GithubMicrosoftedgeWebview2samplesMain]: https://github.com/MicrosoftEdge/WebView2Samples "WebView2-Beispiele – MicrosoftEdge/WebView2Samples | GitHub"  

[GithubMicrosoftedgeWebview2samplesApisample]: https://github.com/MicrosoftEdge/WebView2Samples/blob/master/SampleApps/WebView2APISample/README.md "WebView2-API-Beispiel – MicrosoftEdge/WebView2Samples | GitHub"  
[GithubMicrosoftedgeWebview2samplesGettingStartedGuide]: https://github.com/MicrosoftEdge/WebView2Samples#1-getting-started-guide "WebView2-Beispiele – MicrosoftEdge/WebView2Samples | GitHub"  

[GithubMicrosoftWilMain]: https://github.com/Microsoft/wil "Windows Implementation Libraries (WIL) – microsoft/wil | GitHub"  

[MicrosoftedgeinsiderDownload]: https://www.microsoftedgeinsider.com/download "Herunterladen von Microsoft Edge Insider Channels"  

[MicrosoftVisualstudioMain]: https://visualstudio.microsoft.com "Visual Studio"  

[Webview2Installer]: https://developer.microsoft.com/microsoft-edge/webview2 "WebView2 Installer"  
