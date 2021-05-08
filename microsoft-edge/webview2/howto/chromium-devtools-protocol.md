---
description: Erfahren Sie, wie Sie das Chrome DevTools-Protokoll in Ihren WebView2-Apps mithilfe des Microsoft Edge WebView2-Chromium DevTools-NuGet verwenden.
title: Verwenden des Chrome DevTools-Protokolls in WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/17/2021
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, webview, edge, ICoreWebView2, ICoreWebView2Controller, Chrome DevTools Protocol
ms.openlocfilehash: 86846ee195406f78d5fd7c369f375ed1e359101a
ms.sourcegitcommit: e3cd336c9448277e0dde3b9da1521b5cbc7c44d2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/07/2021
ms.locfileid: "11536513"
---
# <a name="use-chromium-devtools-protocol-in-webview2"></a>Verwenden des Chromium DevTools-Protokolls in WebView2  

Das [Chromium DevTools-Protokoll][GitHubChromedevtoolsDevtoolsProtocol] stellt APIs zum Instrumentieren, Überprüfen, Debuggen und Profil von Chromium Browsern zur Verfügung.  Das Chromium DevTools-Protokoll ist die Grundlage für die Microsoft Edge \(Chromium\) DevTools.  Verwenden Sie Chromium DevTools-Protokoll für Features, die nicht in der WebView2-Plattform implementiert sind.  Weitere Informationen zur Funktion Chromium DevTools-Protokoll finden Sie unter [Chromium DevTools-Protokoll][GitHubChromedevtoolsDevtoolsProtocol].  

> [!CAUTION]
> Das Microsoft Edge WebView2-Team bietet keine Unterstützung für das Chromium DevTools-Protokoll.  Das Chromium DevTools-Protokoll wird vom Open Source-Chromium verwaltet.  
> 
> Um Ihre Vorschläge für zukünftige WebView2-Plattformfeatures zu senden, navigieren Sie zu [WebView Feedback,][GithubMicrosoftedgeWebview2feedback] und übermitteln Sie ein Problem.  

Verwenden Sie eine der folgenden Chromium, um die DevTools-Protokoll-API in WebView2 zu verwenden.  

*   Installieren und verwenden Sie [das Microsoft.Web.WebView2.DevToolsProtocolExtension (Preview)][NugetPackagesMicrosoftWebWebView2DevToolsprotocolextension] NuGet -Paket \(.NET\).  
*   Führen Sie eine der folgenden Methoden aus.  
    *   .NET:  [CallDevToolsProtocolAsync][DotnetApiMicrosoftWebWebview2CoreCorewebview2CalldevtoolsprotocolmethodasyncViewWebview2Dotnet1077444MicrosoftWebWebView2CoreCorewebview2CalldevtoolsprotocolmethodsyncSystemStringSystemString], [GetDevToolsProtocolEventReceiver][DotnetApiMicrosoftWebWebview2CoreCorewebview2GetdevtoolsprotocoleventreceiverViewWebview2Dotnet1077444]  
    *   Win32 C/C++:  [CallDevToolsProtocolMethod][Webview2ReferenceWin32Icorewebview2ViewWebview21077444Calldevtoolsprotocolmethod], [ICoreWebView2DevToolsProtocolEventReceiver][Webview2ReferenceWin32Icorewebview2devtoolsprotocoleventreceiverViewWebview21077444]  
    
## <a name="use-devtoolsprotocolhelper-preview"></a>Verwenden von DevToolsProtocolHelper (Vorschau)

> [!NOTE]
> Das [Microsoft.Web.WebView2.DevToolsProtocolExtension NuGet-Paket][NugetPackagesMicrosoftWebWebView2DevToolsprotocolextension] befindet sich derzeit in der technischen Vorschau.  Verzichten Sie in der Vorschau auf die Verwendung des Pakets in Produktions-Apps.

[Microsoft.Web.WebView2.DevToolsProtocolExtension (Preview)][NugetPackagesMicrosoftWebWebView2DevToolsprotocolextension] ist ein vom WebView2-Team erstelltes NuGet-Paket, das einfachen Zugriff auf Chromium DevTools-Protokollfeatures bietet.  In den folgenden Beispielen wird beschrieben, wie Sie die Geolocation-Funktionalität in Chromium DevTools-Protokoll in Ihrem WebView2-Steuerelement verwenden.  Sie können ein ähnliches Muster verwenden, um andere DevTools-Chromium verwenden.  

## <a name="step-1-create-a-webpage-to-find-your-geolocation"></a>Schritt 1: Erstellen einer Webseite zur Suche nach Ihrem Geografischen Standort  

Um eine zu `HTML file` erstellen, um Ihre Geolocation zu finden, führen Sie die folgenden Aktionen aus.  

1.  Öffnen Visual Studio Code \(oder eine IDE Ihrer Wahl\).  
1.  Erstellen Sie eine neue `.html` Datei.  
1.  Kopieren Sie den folgenden Codeausschnitt, und fügen Sie ihn in die neue Datei `.html` ein.  
    
    ```html
    <!DOCTYPE html>
    <html lang="en">
    <head>
        <title>Geolocation Finder</title>
    </head>
    <body>
        <button id="display">Display Location</button>
        <div id="message"></div>
    </body>
    
    <script>
        const btn = document.getElementById('display');
        // Find the user location.
        btn.addEventListener('click', function () {
            navigator.geolocation.getCurrentPosition(onSuccess, onError);
        });
        
        // Update message to display the latitude and longitude coordinates.
        function onSuccess(position) {
            const {latitude, longitude} = position.coords;
            message.textContent = `Your location: (${latitude},${longitude})`;
        }
        
        function onError() {
            message.textContent = `Operation Failed`;
        }
    </script>
    </html>
    ```  
    
1.  Speichern Sie `.html` die Datei mit dem Dateinamen `geolocation.html` .  
1.  Öffnen Sie Microsoft Edge.  
1.  Öffnen Sie die Datei `geolocation.html`.  
1.  Wählen Sie zum Anzeigen der Breiten- und Längengradkoordinaten die Schaltfläche **Anzeigeposition** aus.  Wenn Sie Ihre Geolocation überprüfen und vergleichen möchten, kopieren und fügen Sie ihre Koordinaten in [https://www.bing.com/maps][BingMaps] ein.  
    
    :::image type="complex" source="./media/geolocater-browser.png" alt-text="Anzeigen der Geolocationkoordinaten des Benutzers in Microsoft Edge" lightbox="./media/geolocater-browser.png":::
       Anzeigen der Geolocationkoordinaten des Benutzers in Microsoft Edge  
    :::image-end:::  
    
## <a name="step-2-display-geolocationhtml-in-a-webview2"></a>Schritt 2: Anzeigen geolocation.html in einer WebView2  

1.  Verwenden Sie zum Erstellen einer WebView2-App eine der folgenden Anleitungen für erste Schritte oder WebView2-Beispiele.  
    *   [Erste Schritte mit WebView2 in Windows Formularen][Webview2GettingstartedWinforms]  
    *   [Erste Schritte mit WebView2 in WPF][Webview2GettingstartedWpf]  
    *   [WebView2-Beispiele][GithubMicrosoftedgeWebview2samples]  
        
1.  Legen Sie die anfängliche Navigation des WebView2-Steuerelements auf `geolocation.html` .  
    
    ```csharp
    webView.CoreWebView2.Navigate(@"C:\{path\to\file}\geolocation.html");
    ```  
    
1.  Stellen Sie `geolocation.html` sicher, dass die Datei in Ihrer WebView2-Steuerelement-App angezeigt wird.  
    
    :::image type="complex" source="./media/initial-geolocate.png" alt-text="Anzeigen der geolocater.html-Datei in Ihrer WebView2-Steuerelement-App" lightbox="./media/initial-geolocate.png":::
       Anzeigen der `geolocation.html` Datei in Ihrer WebView2-Steuerelement-App  
    :::image-end:::  
    
## <a name="step-3-install-the-devtoolsprotocolhelper-nuget-package"></a>Schritt 3: Installieren des DevToolsProtocolHelper NuGet Pakets  

Verwenden NuGet zum Herunterladen `Microsoft.Web.WebView2.DevToolsProtocolExtension` .  Führen Sie zum Installieren des Pakets die folgenden Aktionen aus.  

1.  Wählen **Project**  >  **Verwalten NuGet Pakete**durchsuchen  >  **aus.**  
1.  Geben `Microsoft.Web.WebView2.DevToolsProtocolExtension` Sie **Microsoft.Web.WebView2.DevToolsProtocolExtension**Install ein, und wählen Sie diese  >  **aus.**   
    
:::image type="complex" source="./media/cdpnuget.png" alt-text="Stellen Sie sicher, dass Microsoft.Web.WebView2.DevToolsProtocolExtension im Visual Studio NuGet Paket-Manager" lightbox="./media/cdpnuget.png":::
   Stellen **Sie sicher, dass Microsoft.Web.WebView2.DevToolsProtocolExtension** im Visual Studio NuGet Paket-Manager  
:::image-end:::  

## <a name="step-4-use-devtools-protocol-helper"></a>Schritt 4: Verwenden der DevTools-Protokollhilfe  

1.  Fügen Sie `DevToolsProtocolExtension` ihrem Projekt den Namespace hinzu.  
    
    ```csharp
    using Microsoft.Web.WebView2.Core;
    using Microsoft.Web.WebView2.Core.DevToolsProtocolExtension;
    ```  
    
1.  Instanziieren Sie das `DevToolsProtocolHelper` Objekt, und navigieren Sie zu `geolocation.html` .  
    
    ```csharp
    async void InitializeAsync()
    {
        await webView.EnsureCoreWebView2Async(null);
        DevToolsProtocolHelper helper = webView.CoreWebView2.GetDevToolsProtocolHelper(); 
        
        webView.CoreWebView2.Navigate(@"C:\{path\to\file}\geolocation.html");
    }
    ```  
    
1.  Führen Sie [die setGeoLocationOverrideAsync-Methode][GithubChromedevtoolsDevtoolsProtocolTotEmulationMethodSetgeolocationoverride] aus.  Weitere Informationen finden Sie unter [setGeolocationOverride][GithubChromedevtoolsDevtoolsProtocolTotEmulationMethodSetgeolocationoverride].  
    
    ```csharp
    async void InitializeAsync()
    {
        await webView.EnsureCoreWebView2Async(null);
        DevToolsProtocolHelper helper = webview.CoreWebView2.GetDevToolsProtocolHelper();
        
        webView.CoreWebView2.Navigate(@"C:\{path\to\file}\geolocation.html");
        
        // Latitude and longitude for Paris, France.
        double latitude = 48.857024082572565;  
        double longitude = 2.3161581601457386;  
        double accuracy = 1;
        await helper.Emulation.setGeolocationOverrideAsync(latitude, longitude, accuracy);
        
    }
    ```  
    
1.  Führen Sie Ihre App aus.  
1.  Um die Koordinaten von Paris, Frankreich, anzeigen zu können, wählen Sie die Schaltfläche **Standort** anzeigen aus.  
    
    :::image type="complex" source="./media/finallocation-cdp.png" alt-text="Anzeigen der .html in einem WebView2-Steuerelement mit den Koordinaten für Paris" lightbox="./media/finallocation-cdp.png":::
       Anzeigen der `.html` Datei in einem WebView2-Steuerelement mit den Koordinaten für Paris  
    :::image-end:::  
    
## <a name="file-a-chromium-devtools-protocol-bug"></a>Datei eines Chromium DevTools-Protokollfehlers  

Das WebView2-Team besitzt nicht das Chromium DevTools-Protokoll.  

> [!IMPORTANT]
> Direktes Feedback und Fehler an das Chromium Problem-Repository.  

Führen Sie die folgenden Aktionen aus, um Chromium devTools-Protokollfehler oder -problem zu melden.  

1.  Melden Sie [einen Fehlerbericht][ChromiumBugsChromiumIssuesEntryComponentsPlatformDevtoolsPlatform]an.  
1.  Navigieren Sie zu [WebView Feedback,][GithubMicrosoftedgeWebview2feedback] und öffnen Sie ein neues Problem.  
    
## <a name="see-also"></a>Weitere Informationen  

*   [WebView2-Beispiele][GithubMicrosoftedgeWebview2samples]  
    
 <!-- links -->  

[Webview2GettingstartedWinforms]: /microsoft-edge/webview2/gettingstarted/winforms "Erste Schritte mit WebView2 in Windows Forms | Microsoft Docs"  
[Webview2GettingstartedWpf]: /microsoft-edge/webview2/gettingstarted/wpf "Erste Schritte mit WebView2 in WPF | Microsoft Docs"  

[DotnetApiMicrosoftWebWebview2CoreCorewebview2GetdevtoolsprotocoleventreceiverViewWebview2Dotnet1077444]: /dotnet/api/microsoft.web.webview2.core.corewebview2.getdevtoolsprotocoleventreceiver?view=webview2-dotnet-1.0.774.44&preserve-view=true "CoreWebView2.GetDevToolsProtocolEventReceiver(String)-Methode | Microsoft Docs"  
[DotnetApiMicrosoftWebWebview2CoreCorewebview2CalldevtoolsprotocolmethodasyncViewWebview2Dotnet1077444MicrosoftWebWebView2CoreCorewebview2CalldevtoolsprotocolmethodsyncSystemStringSystemString]: /dotnet/api/microsoft.web.webview2.core.corewebview2.calldevtoolsprotocolmethodasync?view=webview2-dotnet-1.0.774.44&preserve-view=true#Microsoft_Web_WebView2_Core_CoreWebView2_CallDevToolsProtocolMethodAsync_System_String_System_String_ "CoreWebView2.CallDevToolsProtocolMethodAsync(String, String) Method | Microsoft Docs"  

[Webview2ReferenceWin32Icorewebview2ViewWebview21077444Calldevtoolsprotocolmethod]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-1.0.774.44&preserve-view=true#calldevtoolsprotocolmethod "CallDevToolsProtocolMethod - Schnittstelle ICoreWebView2 | Microsoft Docs"  
[Webview2ReferenceWin32Icorewebview2devtoolsprotocoleventreceiverViewWebview21077444]: /microsoft-edge/webview2/reference/win32/icorewebview2devtoolsprotocoleventreceiver?view=webview2-1.0.774.44&preserve-view=true "Schnittstelle ICoreWebView2DevToolsProtocolEventReceiver | Microsoft Docs"  

[BingMaps]: https://www.bing.com/maps "Bing Karten"  

[GitHubChromedevtoolsDevtoolsProtocol]: https://chromedevtools.github.io/devtools-protocol "Chrome DevTools Protocol | GitHub"  
[GithubChromedevtoolsDevtoolsProtocolTotEmulationMethodSetgeolocationoverride]: https://chromedevtools.github.io/devtools-protocol/tot/Emulation/#method-setGeolocationOverride "Emulation.setGeolocationOverride – Chrome DevTools Protocol | GitHub"  

[GithubMicrosoftedgeWebview2feedback]: https://github.com/MicrosoftEdge/WebView2Feedback "WebView Feedback | GitHub"  
[GithubMicrosoftedgeWebview2samples]: https://github.com/MicrosoftEdge/WebView2Samples "WebView2-| GitHub"  

[ChromiumBugsChromiumIssuesEntryComponentsPlatformDevtoolsPlatform]: https://bugs.chromium.org/p/chromium/issues/entry?components=Platform%3EDevTools%3EPlatform "Fehlerbericht | Chromium Bugs"  

[NugetPackagesMicrosoftWebWebView2DevToolsprotocolextension]: https://www.nuget.org/packages/Microsoft.Web.WebView2.DevToolsProtocolExtension "Microsoft.Web.WebView2.DevToolsProtocolExtension | NuGet QA-Katalog"  
