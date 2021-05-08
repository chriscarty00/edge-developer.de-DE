---
description: Erfahren Sie, wie Sie das Chrome DevTools-Protokoll in Ihren WebView2-Apps mithilfe des Microsoft Edge WebView2-Chromium DevTools-NuGet verwenden.
title: Verwenden des Chrome DevTools-Protokolls in WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/06/2021
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, webview, edge, ICoreWebView2, ICoreWebView2Controller, Chrome DevTools Protocol
ms.openlocfilehash: cd59bc0d177d17680222fcff8452c2cf8d56b195
ms.sourcegitcommit: 777b16ef10363f2dfd755f115ee2d4c81a8de46f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/07/2021
ms.locfileid: "11535984"
---
# <a name="use-chromium-devtools-protocol-in-webview2"></a><span data-ttu-id="d5942-104">Verwenden des Chromium DevTools-Protokolls in WebView2</span><span class="sxs-lookup"><span data-stu-id="d5942-104">Use Chromium DevTools Protocol in WebView2</span></span>  

<span data-ttu-id="d5942-105">Das [Chromium DevTools-Protokoll][GitHubChromedevtoolsDevtoolsProtocol] stellt APIs zum Instrumentieren, Überprüfen, Debuggen und Profil von Chromium Browsern zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="d5942-105">The [Chromium DevTools Protocol][GitHubChromedevtoolsDevtoolsProtocol] provides APIs to instrument, inspect, debug, and profile Chromium-based browsers.</span></span>  <span data-ttu-id="d5942-106">Das Chromium DevTools-Protokoll ist die Grundlage für die Microsoft Edge \(Chromium\) DevTools.</span><span class="sxs-lookup"><span data-stu-id="d5942-106">The Chromium DevTools Protocol is the foundation for the Microsoft Edge \(Chromium\) DevTools.</span></span>  <span data-ttu-id="d5942-107">Verwenden Sie Chromium DevTools-Protokoll für Features, die nicht in der WebView2-Plattform implementiert sind.</span><span class="sxs-lookup"><span data-stu-id="d5942-107">Use the Chromium DevTools Protocol for features that aren't implemented in the WebView2 platform.</span></span>  <span data-ttu-id="d5942-108">Weitere Informationen zur Funktion Chromium DevTools-Protokoll finden Sie unter [Chromium DevTools-Protokoll][GitHubChromedevtoolsDevtoolsProtocol].</span><span class="sxs-lookup"><span data-stu-id="d5942-108">For more information about the Chromium DevTools Protocol functionality, navigate to [Chromium DevTools Protocol][GitHubChromedevtoolsDevtoolsProtocol].</span></span>  

> [!CAUTION]
> <span data-ttu-id="d5942-109">Das Microsoft Edge WebView2-Team bietet keine Unterstützung für das Chromium DevTools-Protokoll.</span><span class="sxs-lookup"><span data-stu-id="d5942-109">The Microsoft Edge WebView2 team does not maintain or support the Chromium DevTools Protocol.</span></span>  <span data-ttu-id="d5942-110">Das Chromium DevTools-Protokoll wird vom Open Source-Chromium verwaltet.</span><span class="sxs-lookup"><span data-stu-id="d5942-110">The Chromium DevTools Protocol is maintained by the open source Chromium project.</span></span>  
> 
> <span data-ttu-id="d5942-111">Um Ihre Vorschläge für zukünftige WebView2-Plattformfeatures zu senden, navigieren Sie zu [WebView Feedback,][GithubMicrosoftedgeWebview2feedback] und übermitteln Sie ein Problem.</span><span class="sxs-lookup"><span data-stu-id="d5942-111">To send your suggestions for future WebView2 platform features, navigate to [WebView Feedback][GithubMicrosoftedgeWebview2feedback] and submit an issue.</span></span>  

<span data-ttu-id="d5942-112">Verwenden Sie eine der folgenden Chromium, um die DevTools-Protokoll-API in WebView2 zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="d5942-112">To use the Chromium DevTools Protocol API in WebView2, use either of the following actions.</span></span>  

*   <span data-ttu-id="d5942-113">Installieren und verwenden Sie [das Microsoft.Web.WebView2.DevToolsProtocolExtension (Preview)][NugetPackagesMicrosoftWebWebView2DevToolsprotocolextension] NuGet -Paket \(.NET\).</span><span class="sxs-lookup"><span data-stu-id="d5942-113">Install and use the [Microsoft.Web.WebView2.DevToolsProtocolExtension (Preview)][NugetPackagesMicrosoftWebWebView2DevToolsprotocolextension] NuGet package \(.NET\).</span></span>  
*   <span data-ttu-id="d5942-114">Führen Sie eine der folgenden Methoden aus.</span><span class="sxs-lookup"><span data-stu-id="d5942-114">Run one of the following methods.</span></span>  
    *   <span data-ttu-id="d5942-115">.NET:  [CallDevToolsProtocolAsync][DotnetApiMicrosoftWebWebview2CoreCorewebview2CalldevtoolsprotocolmethodasyncViewWebview2Dotnet1077444MicrosoftWebWebView2CoreCorewebview2CalldevtoolsprotocolmethodsyncSystemStringSystemString], [GetDevToolsProtocolEventReceiver][DotnetApiMicrosoftWebWebview2CoreCorewebview2GetdevtoolsprotocoleventreceiverViewWebview2Dotnet1077444]</span><span class="sxs-lookup"><span data-stu-id="d5942-115">.NET:  [CallDevToolsProtocolAsync][DotnetApiMicrosoftWebWebview2CoreCorewebview2CalldevtoolsprotocolmethodasyncViewWebview2Dotnet1077444MicrosoftWebWebView2CoreCorewebview2CalldevtoolsprotocolmethodsyncSystemStringSystemString], [GetDevToolsProtocolEventReceiver][DotnetApiMicrosoftWebWebview2CoreCorewebview2GetdevtoolsprotocoleventreceiverViewWebview2Dotnet1077444]</span></span>  
    *   <span data-ttu-id="d5942-116">Win32 C/C++:  [CallDevToolsProtocolMethod][Webview2ReferenceWin32Icorewebview2ViewWebview21077444Calldevtoolsprotocolmethod], [ICoreWebView2DevToolsProtocolEventReceiver][Webview2ReferenceWin32Icorewebview2devtoolsprotocoleventreceiverViewWebview21077444]</span><span class="sxs-lookup"><span data-stu-id="d5942-116">Win32 C/C++:  [CallDevToolsProtocolMethod][Webview2ReferenceWin32Icorewebview2ViewWebview21077444Calldevtoolsprotocolmethod], [ICoreWebView2DevToolsProtocolEventReceiver][Webview2ReferenceWin32Icorewebview2devtoolsprotocoleventreceiverViewWebview21077444]</span></span>  
    
## <a name="use-devtoolsprotocolhelper-preview"></a><span data-ttu-id="d5942-117">Verwenden von DevToolsProtocolHelper (Vorschau)</span><span class="sxs-lookup"><span data-stu-id="d5942-117">Use DevToolsProtocolHelper (Preview)</span></span>

> [!NOTE]
> <span data-ttu-id="d5942-118">Das [Microsoft.Web.WebView2.DevToolsProtocolExtension NuGet-Paket][NugetPackagesMicrosoftWebWebView2DevToolsprotocolextension] befindet sich derzeit in der technischen Vorschau.</span><span class="sxs-lookup"><span data-stu-id="d5942-118">The [Microsoft.Web.WebView2.DevToolsProtocolExtension][NugetPackagesMicrosoftWebWebView2DevToolsprotocolextension] NuGet package is currently in technical preview.</span></span>  <span data-ttu-id="d5942-119">Verzichten Sie in der Vorschau auf die Verwendung des Pakets in Produktions-Apps.</span><span class="sxs-lookup"><span data-stu-id="d5942-119">While in preview, refrain from using the package in production apps.</span></span>

<span data-ttu-id="d5942-120">[Microsoft.Web.WebView2.DevToolsProtocolExtension (Preview)][NugetPackagesMicrosoftWebWebView2DevToolsprotocolextension] ist ein vom WebView2-Team erstelltes NuGet-Paket, das einfachen Zugriff auf Chromium DevTools-Protokollfeatures bietet.</span><span class="sxs-lookup"><span data-stu-id="d5942-120">[Microsoft.Web.WebView2.DevToolsProtocolExtension (Preview)][NugetPackagesMicrosoftWebWebView2DevToolsprotocolextension] is a NuGet package created by the WebView2 team that provides easy access to Chromium DevTools Protocol features.</span></span>  <span data-ttu-id="d5942-121">In den folgenden Beispielen wird beschrieben, wie Sie die Geolocation-Funktionalität in Chromium DevTools-Protokoll in Ihrem WebView2-Steuerelement verwenden.</span><span class="sxs-lookup"><span data-stu-id="d5942-121">The following examples describe how to use the geolocation functionality in Chromium DevTools Protocol in your WebView2 control.</span></span>  <span data-ttu-id="d5942-122">Sie können ein ähnliches Muster verwenden, um andere DevTools-Chromium verwenden.</span><span class="sxs-lookup"><span data-stu-id="d5942-122">You may follow a similar pattern to use other Chromium DevTools Protocol features.</span></span>  

## <a name="step-1-create-a-webpage-to-find-your-geolocation"></a><span data-ttu-id="d5942-123">Schritt 1: Erstellen einer Webseite zur Suche nach Ihrem Geografischen Standort</span><span class="sxs-lookup"><span data-stu-id="d5942-123">Step 1: Create a webpage to find your geolocation</span></span>  

<span data-ttu-id="d5942-124">Um eine zu `HTML file` erstellen, um Ihre Geolocation zu finden, führen Sie die folgenden Aktionen aus.</span><span class="sxs-lookup"><span data-stu-id="d5942-124">To create an `HTML file` to find your geolocation, complete following the actions.</span></span>  

1.  <span data-ttu-id="d5942-125">Öffnen Visual Studio Code \(oder eine IDE Ihrer Wahl\).</span><span class="sxs-lookup"><span data-stu-id="d5942-125">Open Visual Studio Code \(or an IDE of your choice\).</span></span>  
1.  <span data-ttu-id="d5942-126">Erstellen Sie eine neue `.html` Datei.</span><span class="sxs-lookup"><span data-stu-id="d5942-126">Create a new `.html` file.</span></span>  
1.  <span data-ttu-id="d5942-127">Kopieren Sie den folgenden Codeausschnitt, und fügen Sie ihn in die neue Datei `.html` ein.</span><span class="sxs-lookup"><span data-stu-id="d5942-127">Copy and paste the following code snippet in your new `.html` file.</span></span>  
    
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
    
1.  <span data-ttu-id="d5942-128">Speichern Sie `.html` die Datei mit dem Dateinamen `geolocation.html` .</span><span class="sxs-lookup"><span data-stu-id="d5942-128">Save the `.html` file with the filename `geolocation.html`.</span></span>  
1.  <span data-ttu-id="d5942-129">Öffnen Sie Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="d5942-129">Open Microsoft Edge.</span></span>  
1.  <span data-ttu-id="d5942-130">Öffnen Sie die Datei `geolocation.html`.</span><span class="sxs-lookup"><span data-stu-id="d5942-130">Open the `geolocation.html` file.</span></span>  
1.  <span data-ttu-id="d5942-131">Wählen Sie zum Anzeigen der Breiten- und Längengradkoordinaten die Schaltfläche **Anzeigeposition** aus.</span><span class="sxs-lookup"><span data-stu-id="d5942-131">To display your latitude and longitude coordinates, choose the **Display Location** button.</span></span>  <span data-ttu-id="d5942-132">Wenn Sie Ihre Geolocation überprüfen und vergleichen möchten, kopieren und fügen Sie ihre Koordinaten in [https://www.bing.com/maps][BingMaps] ein.</span><span class="sxs-lookup"><span data-stu-id="d5942-132">To verify and compare your geolocation, copy and paste your coordinates in [https://www.bing.com/maps][BingMaps].</span></span>  
    
    :::image type="complex" source="./media/geolocater-browser.png" alt-text="Anzeigen der Geolocationkoordinaten des Benutzers in Microsoft Edge" lightbox="./media/geolocater-browser.png":::
       <span data-ttu-id="d5942-134">Anzeigen der Geolocationkoordinaten des Benutzers in Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="d5942-134">Display the geolocation coordinates of the user in Microsoft Edge</span></span>  
    :::image-end:::  
    
## <a name="step-2-display-geolocationhtml-in-a-webview2"></a><span data-ttu-id="d5942-135">Schritt 2: Anzeigen geolocation.html in einer WebView2</span><span class="sxs-lookup"><span data-stu-id="d5942-135">Step 2: Display geolocation.html in a WebView2</span></span>  

1.  <span data-ttu-id="d5942-136">Verwenden Sie zum Erstellen einer WebView2-App eine der folgenden Anleitungen für erste Schritte oder WebView2-Beispiele.</span><span class="sxs-lookup"><span data-stu-id="d5942-136">To create a WebView2 app, use either of the following get started guides or WebView2 samples.</span></span>  
    *   [<span data-ttu-id="d5942-137">Erste Schritte mit WebView2 in Windows Formularen</span><span class="sxs-lookup"><span data-stu-id="d5942-137">Get Started with WebView2 in Windows Forms</span></span>][Webview2GetStartedWinforms]  
    *   [<span data-ttu-id="d5942-138">Erste Schritte mit WebView2 in WPF</span><span class="sxs-lookup"><span data-stu-id="d5942-138">Get Started with WebView2 in WPF</span></span>][Webview2GetStartedWpf]  
    *   [<span data-ttu-id="d5942-139">WebView2-Beispiele</span><span class="sxs-lookup"><span data-stu-id="d5942-139">WebView2 samples</span></span>][GithubMicrosoftedgeWebview2samples]  
        
1.  <span data-ttu-id="d5942-140">Legen Sie die anfängliche Navigation des WebView2-Steuerelements auf `geolocation.html` .</span><span class="sxs-lookup"><span data-stu-id="d5942-140">Set the initial navigation of the WebView2 control to `geolocation.html`.</span></span>  
    
    ```csharp
    webView.CoreWebView2.Navigate(@"C:\{path\to\file}\geolocation.html");
    ```  
    
1.  <span data-ttu-id="d5942-141">Stellen Sie `geolocation.html` sicher, dass die Datei in Ihrer WebView2-Steuerelement-App angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="d5942-141">Ensure the `geolocation.html` file displays in your WebView2 control app.</span></span>  
    
    :::image type="complex" source="./media/initial-geolocate.png" alt-text="Anzeigen der geolocater.html-Datei in Ihrer WebView2-Steuerelement-App" lightbox="./media/initial-geolocate.png":::
       <span data-ttu-id="d5942-143">Anzeigen der `geolocation.html` Datei in Ihrer WebView2-Steuerelement-App</span><span class="sxs-lookup"><span data-stu-id="d5942-143">Display the `geolocation.html` file in your WebView2 control app</span></span>  
    :::image-end:::  
    
## <a name="step-3-install-the-devtoolsprotocolhelper-nuget-package"></a><span data-ttu-id="d5942-144">Schritt 3: Installieren des DevToolsProtocolHelper NuGet Pakets</span><span class="sxs-lookup"><span data-stu-id="d5942-144">Step 3: Install the DevToolsProtocolHelper NuGet package</span></span>  

<span data-ttu-id="d5942-145">Verwenden NuGet zum Herunterladen `Microsoft.Web.WebView2.DevToolsProtocolExtension` .</span><span class="sxs-lookup"><span data-stu-id="d5942-145">Use NuGet to download `Microsoft.Web.WebView2.DevToolsProtocolExtension`.</span></span>  <span data-ttu-id="d5942-146">Führen Sie zum Installieren des Pakets die folgenden Aktionen aus.</span><span class="sxs-lookup"><span data-stu-id="d5942-146">To install the package, complete the following actions.</span></span>  

1.  <span data-ttu-id="d5942-147">Wählen **Project**  >  **Verwalten NuGet Pakete**durchsuchen  >  **aus.**</span><span class="sxs-lookup"><span data-stu-id="d5942-147">Choose **Project** > **Manage NuGet Packages** > **Browse**.</span></span>  
1.  <span data-ttu-id="d5942-148">Geben `Microsoft.Web.WebView2.DevToolsProtocolExtension` Sie **Microsoft.Web.WebView2.DevToolsProtocolExtension**Install ein, und wählen Sie diese  >  **aus.**</span><span class="sxs-lookup"><span data-stu-id="d5942-148">Type `Microsoft.Web.WebView2.DevToolsProtocolExtension` and choose **Microsoft.Web.WebView2.DevToolsProtocolExtension** > **Install**.</span></span>   
    
:::image type="complex" source="./media/cdp-nuget.png" alt-text="Stellen Sie sicher, dass Microsoft.Web.WebView2.DevToolsProtocolExtension im Visual Studio NuGet Paket-Manager" lightbox="./media/cdp-nuget.png":::
   <span data-ttu-id="d5942-150">Stellen **Sie sicher, dass Microsoft.Web.WebView2.DevToolsProtocolExtension** im Visual Studio NuGet Paket-Manager</span><span class="sxs-lookup"><span data-stu-id="d5942-150">Ensure **Microsoft.Web.WebView2.DevToolsProtocolExtension** displays in the Visual Studio NuGet Package Manager</span></span>  
:::image-end:::    

## <a name="step-4-use-devtools-protocol-helper"></a><span data-ttu-id="d5942-151">Schritt 4: Verwenden der DevTools-Protokollhilfe</span><span class="sxs-lookup"><span data-stu-id="d5942-151">Step 4: Use DevTools Protocol Helper</span></span>  

1.  <span data-ttu-id="d5942-152">Fügen Sie `DevToolsProtocolExtension` ihrem Projekt den Namespace hinzu.</span><span class="sxs-lookup"><span data-stu-id="d5942-152">Add the `DevToolsProtocolExtension` namespace to your project.</span></span>  
    
    ```csharp
    using Microsoft.Web.WebView2.Core;
    using Microsoft.Web.WebView2.Core.DevToolsProtocolExtension;
    ```  
    
1.  <span data-ttu-id="d5942-153">Instanziieren Sie das `DevToolsProtocolHelper` Objekt, und navigieren Sie zu `geolocation.html` .</span><span class="sxs-lookup"><span data-stu-id="d5942-153">Instantiate the `DevToolsProtocolHelper` object and navigate to `geolocation.html`.</span></span>  
    
    ```csharp
    async void InitializeAsync()
    {
        await webView.EnsureCoreWebView2Async(null);
        DevToolsProtocolHelper helper = webView.CoreWebView2.GetDevToolsProtocolHelper(); 
        
        webView.CoreWebView2.Navigate(@"C:\{path\to\file}\geolocation.html");
    }
    ```  
    
1.  <span data-ttu-id="d5942-154">Führen Sie [die setGeoLocationOverrideAsync-Methode][GithubChromedevtoolsDevtoolsProtocolTotEmulationMethodSetgeolocationoverride] aus.</span><span class="sxs-lookup"><span data-stu-id="d5942-154">Run the [setGeoLocationOverrideAsync][GithubChromedevtoolsDevtoolsProtocolTotEmulationMethodSetgeolocationoverride] method.</span></span>  <span data-ttu-id="d5942-155">Weitere Informationen finden Sie unter [setGeolocationOverride][GithubChromedevtoolsDevtoolsProtocolTotEmulationMethodSetgeolocationoverride].</span><span class="sxs-lookup"><span data-stu-id="d5942-155">For more information, navigate to [setGeolocationOverride][GithubChromedevtoolsDevtoolsProtocolTotEmulationMethodSetgeolocationoverride].</span></span>  
    
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
    
1.  <span data-ttu-id="d5942-156">Führen Sie Ihre App aus.</span><span class="sxs-lookup"><span data-stu-id="d5942-156">Run your app.</span></span>  
1.  <span data-ttu-id="d5942-157">Um die Koordinaten von Paris, Frankreich, anzeigen zu können, wählen Sie die Schaltfläche **Standort** anzeigen aus.</span><span class="sxs-lookup"><span data-stu-id="d5942-157">To display the coordinates of Paris, France, choose the **Display Location** button.</span></span>  
    
    :::image type="complex" source="./media/final-location-cdp.png" alt-text="Anzeigen der .html in einem WebView2-Steuerelement mit den Koordinaten für Paris" lightbox="./media/final-location-cdp.png":::
       <span data-ttu-id="d5942-159">Anzeigen der `.html` Datei in einem WebView2-Steuerelement mit den Koordinaten für Paris</span><span class="sxs-lookup"><span data-stu-id="d5942-159">Display the `.html` file in a WebView2 control with the coordinates for Paris</span></span>  
    :::image-end:::  
    
## <a name="file-a-chromium-devtools-protocol-bug"></a><span data-ttu-id="d5942-160">Datei eines Chromium DevTools-Protokollfehlers</span><span class="sxs-lookup"><span data-stu-id="d5942-160">File a Chromium DevTools Protocol bug</span></span>  

<span data-ttu-id="d5942-161">Das WebView2-Team besitzt nicht das Chromium DevTools-Protokoll.</span><span class="sxs-lookup"><span data-stu-id="d5942-161">The WebView2 team doesn't own the Chromium DevTools Protocol.</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="d5942-162">Direktes Feedback und Fehler an das Chromium Problem-Repository.</span><span class="sxs-lookup"><span data-stu-id="d5942-162">Direct feedback and bugs to the Chromium Issues repo.</span></span>  

<span data-ttu-id="d5942-163">Führen Sie die folgenden Aktionen aus, um Chromium devTools-Protokollfehler oder -problem zu melden.</span><span class="sxs-lookup"><span data-stu-id="d5942-163">To file a Chromium DevTools Protocol bug or issue, complete the following actions.</span></span>  

1.  <span data-ttu-id="d5942-164">Melden Sie [einen Fehlerbericht][ChromiumBugsChromiumIssuesEntryComponentsPlatformDevtoolsPlatform]an.</span><span class="sxs-lookup"><span data-stu-id="d5942-164">File a [bug report][ChromiumBugsChromiumIssuesEntryComponentsPlatformDevtoolsPlatform].</span></span>  
1.  <span data-ttu-id="d5942-165">Navigieren Sie zu [WebView Feedback,][GithubMicrosoftedgeWebview2feedback] und öffnen Sie ein neues Problem.</span><span class="sxs-lookup"><span data-stu-id="d5942-165">Navigate to [WebView Feedback][GithubMicrosoftedgeWebview2feedback] and open a new issue.</span></span>  
    
## <a name="see-also"></a><span data-ttu-id="d5942-166">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="d5942-166">See also</span></span>  

*   [<span data-ttu-id="d5942-167">WebView2-Beispiele</span><span class="sxs-lookup"><span data-stu-id="d5942-167">WebView2 samples</span></span>][GithubMicrosoftedgeWebview2samples]  
    
 <!-- links -->  

[Webview2GetStartedWinforms]: /microsoft-edge/webview2/get-started/winforms "Erste Schritte mit WebView2 in Windows Forms | Microsoft Docs"  
[Webview2GetStartedWpf]: /microsoft-edge/webview2/get-started/wpf "Erste Schritte mit WebView2 in WPF | Microsoft Docs"  

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
